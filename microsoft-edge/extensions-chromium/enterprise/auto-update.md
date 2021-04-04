---
description: En savoir plus sur les mises à jour automatiques des extensions dans Microsoft Edge
title: Mise à jour automatique des extensions dans Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/17/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, développement d’extensions, extensions de navigateur, extensions, extensions, centre de partenaires, développeur
ms.openlocfilehash: 0f3f140cd3a2a079cd09f4d61e46a420342e15e0
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461513"
---
<!-- Copyright A. W. Fuchs

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="auto-update-extensions-in-microsoft-edge"></a>Mise à jour automatique des extensions dans Microsoft Edge  

La mise à jour automatique des extensions offre les mêmes avantages que la mise à jour automatique de Microsoft Edge :   

*   Incorporer des correctifs de bogue et de sécurité.  
*   Ajoutez de nouvelles fonctionnalités ou améliorations de performances.  
*   Améliorez l’interface utilisateur.  

Auparavant, lorsque les extensions non stockées étaient pris en charge, il était possible de mettre à jour les binaires natifs et l’extension en même temps.  À présent, ces extensions sont hébergées dans le magasin de modules extensions Microsoft Edge et les mises à jour sont réalisées à l’aide du même mécanisme que celui utilisé par Microsoft Edge, que vous ne pouvez pas contrôler.  Soyez prudent lors de la mise à jour des extensions qui ont une dépendance sur les binaires natifs.  

> [!NOTE]
> Cette rubrique ne s’applique pas aux extensions publiées à l’aide du tableau [de bord de l’Centre][MicrosoftPartnerCenter] partenaires.  Vous pouvez utiliser le tableau de bord pour publier des versions mises à jour pour vos utilisateurs et dans le magasin de modules microsoft Edge.

## <a name="overview"></a>Vue d'ensemble  

Toutes les quelques heures, Microsoft Edge vérifie si chaque extension ou application installée dispose d’une URL de mise à jour.  Les extensions peuvent spécifier une URL de mise à jour à l’aide du champ dans le manifeste, qui pointe vers un emplacement `update_url` pour effectuer une vérification de mise à jour.  Pour chaque `update_url` fichier manifeste, il envoie des demandes pour les fichiers XML de manifeste mis à jour.  Si le fichier XML de manifeste de mise à jour répertorie une version plus récente que celle installée, Microsoft Edge télécharge et installe la version la plus récente.  Le même processus fonctionne pour les mises à jour manuelles, où le nouveau fichier doit être signé avec la même clé privée que la `.crx` version actuellement installée.  

> [!NOTE]
> Afin de maintenir la confidentialité des utilisateurs, Microsoft Edge n’envoie aucun en-tête avec des demandes de manifeste de mise à jour automatique et ignore les en-têtes dans les réponses à `Cookie` `Set-Cookie` ces demandes.  

## <a name="update-url"></a>URL de mise à jour  

Si vous hébergez votre propre extension ou application, vous devez ajouter le `update_url` champ à votre `manifest.json` fichier.  Examinez l’extrait de code suivant pour obtenir un exemple de `update_url` .  

```json
{
  "name": "My extension",
  ... 
  "update_url": "http://contoso.com/mytestextension/updates.xml",
  ... 
}
```  

## <a name="updated-manifest"></a>Manifeste mis à jour  

Le manifeste mis à jour renvoyé par le serveur doit être un document XML.  Examinez l’extrait de code suivant pour obtenir un exemple du fichier manifeste XML mis à jour.  

```xml
<?xml version='1.0' encoding='UTF-8'?>
<gupdate xmlns='http://www.microsoft.com/update2/response' protocol='2.0'>
  <app appid='aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'>
    <updatecheck codebase='http://contoso.com/mytestextension/mte_v2.crx' version='2.0' />
  </app>
</gupdate>
```  

Le tableau suivant décrit les attributs du fichier manifeste XML mis à jour.  

| Attribut | Détails | 
|:--- |:--- |  
| `appid` | L’ID d’extension est généré en fonction d’un hachage de la clé publique.  Pour trouver l’ID d’une extension, ouvrez Microsoft Edge et accédez à `edge://extensions` . |  
| `codebase` | URL du `.crx` fichier. |  
| `version` | Cette valeur d’attribut est utilisée par Microsoft Edge pour déterminer s’il doit télécharger le `.crx` fichier spécifié par `codebase` .  Elle doit correspondre à la valeur `version` du fichier `manifest.json` du `.crx` fichier. |  

Le fichier XML de manifeste de mise à jour peut contenir des informations sur plusieurs extensions en incluant plusieurs éléments.  

## <a name="testing"></a>Test  

La fréquence de vérification des mises à jour par défaut est de plusieurs heures.  Pour forcer une mise à jour, accédez au bouton Mettre à jour `edge://extensions` **les extensions et choisissez-le maintenant.**  

## <a name="advanced-usage-request-parameters"></a>Utilisation avancée : paramètres de requête  

Le mécanisme de mise à jour automatique de base est aussi simple que de déposer un fichier XML statique sur n’importe quel serveur web tel qu’Apache et de mettre à jour le fichier XML lorsque vous publiez de nouvelles versions de vos extensions.  

Vous pouvez tirer parti du fait que des paramètres sont ajoutés à la demande de manifeste de mise à jour qui indiquent l’ID d’extension et la version. Vous pouvez utiliser la même URL de mise à jour pour toutes vos extensions au lieu d’un fichier XML statique.  Pour utiliser la même URL de mise à jour pour toutes vos extensions, pointez sur une URL qui exécute du code dynamique côté serveur pour tester ces paramètres.  

L’exemple suivant illustre le format des paramètres de requête de l’URL de mise à jour : `?x={extension_data}` .

Dans cet exemple, `{extension_data}` est une chaîne codée en URL qui utilise le format suivant : `id={id}&v={version}` .

Par exemple, les deux extensions suivantes pointent vers la même URL de mise à `http://contoso.com/extension_updates.php` jour.  

*  Extension 1 - ID : « aaaaaaaaaaaaaaaaaaaa » Version : « 1.1 »
*  Extension 2 - ID : « bbbbbbbbbbbbbbbbbbbbbbbb » Version : « 0,4 »


Voici les demandes de mise à jour de chaque extension.  

```https
http://contoso.com/extension_updates.php?x=id%3Daaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa%26v%3D1.1
```  

```https
http://contoso.com/extension_updates.php?x=id%3Dbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb%26v%3D0.4
```  

Vous pouvez également ré lister plusieurs extensions dans une seule demande pour chaque URL de mise à jour unique.  L’exemple suivant fusionne les demandes précédentes en une seule requête.  

```https
http://contoso.com/extension_updates.php?x=id%3Daaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa%26v%3D1.1&x=id%3Dbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb%26v%3D0.4
```  

Si vous envoyez une seule demande et que le nombre d’extensions installées qui utilisent la même URL de mise à jour est trop long, la vérification de mise à jour envoie davantage de `GET` demandes.  Une `GET` URL de demande est trop longue si elle fait environ 2 000 caractères.  

> [!NOTE]
> À l’avenir, une seule `POST` demande peut remplacer plusieurs `GET` demandes.  La `POST` demande peut contenir les paramètres de la demande dans le `POST` corps.  

## <a name="advanced-usage-minimum-browser-version"></a>Utilisation avancée : version minimale du navigateur  

À mesure que de nouvelles API sont publiées pour le système d’extensions Microsoft Edge, vous pouvez publier une version mise à jour de votre extension ou de votre application qui fonctionne uniquement avec les versions plus récentes de Microsoft Edge.  Lorsque Microsoft Edge est mis à jour automatiquement, la mise à jour vers cette nouvelle version peut prendre quelques jours.  Pour vous assurer qu’une mise à jour spécifique s’applique uniquement aux versions de Microsoft Edge actuelles ou plus récentes qu’une version spécifique, ajoutez l’attribut `prodversionmin` dans votre manifeste de mise à jour.  Dans l’extrait de code suivant, la valeur d’attribut de spécifie que votre application se met automatiquement à jour vers la version uniquement lorsque l’utilisateur exécute Microsoft Edge ou `prodversionmin` `3.0.193.0` une version plus `2.0` `3.0.193.0` récente.  

```xml
<?xml version='1.0' encoding='UTF-8'?>
<gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'>
  <app appid='aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'>
    <updatecheck codebase='http://contoso.com/mytestextension/mte_v2.crx' version='2.0' prodversionmin='3.0.193.0' />
  </app>
</gupdate>
```  

<!-- links -->  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine se trouve [ici.](https://developer.chrome.com/docs/apps/autoupdate/)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  