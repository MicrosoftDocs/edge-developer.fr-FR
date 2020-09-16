---
description: Processus de distribution de l’extension par un mécanisme autre que les magasins validés
title: Autre méthode de distribution de l’extension
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-chrome, développement d’extensions, extensions de navigateur, compléments, Centre des partenaires, développeur
ms.openlocfilehash: e28a84fd75ad1ac0be2000a22c26371ca73d0293
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015694"
---
# Autre méthode de distribution de l’extension  

Si vous êtes un développeur qui veut distribuer une extension dans le cadre de la procédure d’installation d’autres logiciels ou d’un administrateur réseau qui souhaite distribuer une extension dans toute l’organisation, Microsoft Edge prend en charge les méthodes d’installation d’extension suivantes:  

*   **Utilisation du Registre Windows (Windows uniquement)**  

Microsoft Edge prend en charge l’installation d’une extension hébergée sur une extension `update_URL` .  Sous Windows, le `update_URL` doit pointer sur le catalogue des compléments Microsoft Edge (Microsoft Edge addons \) sur lequel l’extension doit être hébergée.  

> [!NOTE]
> Installation externe de l’extension par le biais d’un fichier JSON préférences pour macOS <!--and Linux--> ne sont pas encore pris en charge.  Cette prise en charge de cette fonctionnalité sera bientôt disponible.

## Utilisation du Registre Windows  

Tout d’abord, publiez l’extension dans les modules complémentaires Microsoft Edge ou emportez un fichier. CRX et assurez-vous que le programme s’installe correctement.  

Les étapes à suivre pour installer une extension via le registre dans Windows sont les suivantes:  

*   Recherchez ou créez la clé de Registre suivante:  
    *   Windows 32 bits:  `HKEY_LOCAL_MACHINE\Software\Microsoft\Edge\Extensions`  
    *   Windows 64 bits:  `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Edge\Extensions`  
*   Créez une nouvelle clé \ (dossier \) sous la clé extensions avec le même nom que l’ID de votre extension \ (par exemple, `aaaaaaaaaabbbbbbbbbbcccccccccc` \).  
*   Dans votre clé d’extension, créez une propriété, `update_url` et définissez-la sur la valeur: `https://edge.microsoft.com/extensionwebstorebase/v1/crx` , \ (cela pointe vers le CRX de votre extension dans les compléments Microsoft Edge). Si vous voulez installer une extension à partir du Web Store chrome, spécifiez l’URL de mise à jour du Web Store chrome `https://clients2.google.com/service/update2/crx` .  
    
    ```javascript
    {
        "update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
    }
    ```  
    
*   Lancez le navigateur et accédez à `edge://extensions` ; l’extension doit apparaître dans la liste.  

## Mise à jour et désinstallation  

Microsoft Edge analyse les entrées de métadonnées du Registre chaque fois que le navigateur démarre, puis apporte les modifications nécessaires aux extensions externes installées.  

Pour mettre à jour votre extension vers une nouvelle version, mettez à jour le fichier, puis mettez à jour la version dans le registre.  

Pour désinstaller votre extension (par exemple, si votre logiciel est désinstallé), supprimez votre fichier de préférences \ ( `aaaaaaaaaabbbbbbbbbbcccccccccc.json` \) ou les métadonnées du Registre.  

<!-- image links -->  

<!-- links -->  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developer.chrome.com/apps/external_extensions).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
