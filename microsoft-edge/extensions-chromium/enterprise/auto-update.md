---
description: Découvrez les mises à jour automatiques des extensions dans Microsoft Edge
title: Mettre à jour automatiquement les extensions dans Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, développement d’extensions, extensions de navigateur, extensions, extensions, centre de partenaires, développeur
ms.openlocfilehash: d9901f9c39dabfab111eb7e0c34a3e267a317110
ms.sourcegitcommit: 59d8043e37b89da814f63bc85daf84e0e7167eab
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2021
ms.locfileid: "11586387"
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
# <a name="automatically-update-extensions-in-microsoft-edge"></a>Mettre à jour automatiquement les extensions dans Microsoft Edge  

Lorsque vous définissez votre extension pour qu’elle soit automatiquement mise à jour, elle partage les avantages suivants avec les Microsoft Edge lorsque ce dernier est automatiquement mis à jour.  

*   Incorporer des correctifs de bogue et de sécurité.  
*   Ajoutez de nouvelles fonctionnalités ou des améliorations de performances.  
*   Améliorez l’interface utilisateur.  

Auparavant, les extensions non stockées étaient pris en charge.  En outre, vous avez mis à jour les binaires natifs et l’extension en même temps.  

À présent, le magasin Microsoft Edge des extensions héberge vos extensions et vous mettez à jour votre extension à l’aide du même mécanisme que Microsoft Edge.  Vous ne contrôlez pas le mécanisme de mise à jour.  Soyez prudent lorsque vous mettez à jour les extensions qui ont une dépendance sur les binaires natifs.  

> [!NOTE]
> Cet article ne s’applique pas aux extensions que vous publiez à l’aide du tableau [de bord de l’Centre][MicrosoftPartnerDashboardMicrosoftedgePublicLoginRefDd] partenaires.  Vous pouvez utiliser le tableau de bord pour publier des versions mises à jour pour vos utilisateurs et le magasin Microsoft Edge de modules.  Pour plus d’informations, [accédez à Mettre à jour ou supprimer votre extension.][ExtensionsPublishUpdateExtension]  

## <a name="overview"></a>Vue d'ensemble  

Toutes les quelques heures, Microsoft Edge si chaque extension ou application installée dispose d’une URL de mise à jour.  Pour spécifier une URL de mise à jour pour votre extension, utilisez `update_url` le champ dans le manifeste.  Le `update_url` champ dans le manifeste pointe vers un emplacement pour effectuer une vérification de mise à jour.  Pour chaque `update_url` fichier manifeste, il envoie des demandes pour les fichiers XML de manifeste mis à jour.  Si le fichier XML de manifeste de mise à jour répertorie une version plus récente que celle installée, Microsoft Edge télécharge et installe la version la plus récente.  Le même processus fonctionne pour les mises à jour manuelles, où le nouveau fichier doit être signé avec la même clé privée que la `.crx` version actuellement installée.  

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
<gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'>
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
| `version` | Cette valeur d’attribut est utilisée Microsoft Edge pour déterminer si elle doit télécharger le `.crx` fichier spécifié par `codebase` .  Elle doit correspondre à la valeur `version` du fichier `manifest.json` du `.crx` fichier. |  

Le fichier XML de manifeste de mise à jour peut contenir des informations sur plusieurs extensions en incluant plusieurs éléments.  

## <a name="testing"></a>Test  

La fréquence de vérification des mises à jour par défaut est de plusieurs heures.  Pour forcer une mise à jour, accédez au bouton Mettre à jour `edge://extensions` **les extensions et choisissez-le maintenant.**  

## <a name="advanced-usage-request-parameters"></a>Utilisation avancée : paramètres de requête  

Le mécanisme de base est simple.  Pour mettre à jour automatiquement votre extension, effectuez les actions suivantes.  

1.  Télécharger votre fichier XML statique sur votre serveur web, tel qu’Apache.  
1.  Mettez à jour le fichier XML à mesure que vous publiez de nouvelles versions de vos extensions.  
    
Tirez parti du fait que certains paramètres ajoutés à la demande de manifeste de mise à jour indiquent l’extension `ID` et `version` .  Vous pouvez utiliser la même chose pour toutes vos extensions au `update URL` lieu d’un fichier XML statique.  Pour utiliser la même valeur pour toutes vos extensions, pointez sur une URL qui exécute du code dynamique côté serveur `update URL` pour tester les paramètres.  

L’exemple suivant illustre le format des paramètres de demande de l’URL de mise à jour.  

```url
?x={extension_data}
```  

Dans cet exemple, il s’agit d’une chaîne codée au format `{extension_data}` URL qui utilise le format suivant.  

```url
id={id}&v={version}
```  

Par exemple, les deux extensions suivantes pointent vers la même URL de mise à `http://contoso.com/extension_updates.php` jour.  

*   Extension 1  
    *   ID: `aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa`  
    *   URL de mise à jour : `http://contoso.com/extension_updates.php`
    *   Version: `1.1`  
*   Extension 2  
    *   ID: `bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb`  
    *   URL de mise à jour : `http://contoso.com/extension_updates.php`
    *   Version: `0.4`  


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
> À l’avenir, une `POST` seule demande peut remplacer plusieurs `GET` demandes.  La `POST` demande peut contenir les paramètres de la demande dans le `POST` corps.  

## <a name="advanced-usage-minimum-browser-version"></a>Utilisation avancée : version minimale du navigateur  

À mesure que de nouvelles API sont publiées pour le système d’extensions Microsoft Edge, vous pouvez publier une version mise à jour de votre extension ou application qui fonctionne uniquement avec les versions Microsoft Edge plus récentes.  Lorsque Microsoft Edge mise à jour automatique, la mise à jour de la plupart de vos utilisateurs vers cette nouvelle version peut prendre quelques jours.  Pour vous assurer qu’une mise à jour spécifique s’applique uniquement Microsoft Edge versions actuelles ou plus récentes qu’une version spécifique, ajoutez l’attribut dans votre manifeste `prodversionmin` de mise à jour.  Dans l’extrait de code suivant, la valeur d’attribut de spécifie que votre application est automatiquement mise à jour vers la version uniquement lorsque l’utilisateur exécute une Microsoft Edge ou `prodversionmin` `3.0.193.0` une version plus `2.0` `3.0.193.0` récente.  

```xml
<?xml version='1.0' encoding='UTF-8'?>
<gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'>
  <app appid='aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'>
    <updatecheck codebase='http://contoso.com/mytestextension/mte_v2.crx' version='2.0' prodversionmin='3.0.193.0' />
  </app>
</gupdate>
```  

<!-- links -->  

[ExtensionsPublishUpdateExtension]: ../publish/update-extension.md "Mettre à jour ou supprimer votre extension | Documents Microsoft"  

[MicrosoftPartnerDashboardMicrosoftedgePublicLoginRefDd]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine se trouve [ici.](https://developer.chrome.com/docs/apps/autoupdate)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
