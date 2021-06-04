---
description: Processus de portage de l’extension Chrome vers Microsoft Edge
title: Portage de l’extension Chrome vers Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, développement d’extensions, extensions de navigateur, addons, centre de partenaires, développeur
ms.openlocfilehash: 6be7d788ac22232475e278ae9a5b04de9b6e17f7
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343135"
---
# Portage de votre extension  

Microsoft Edge vous permet de porter votre extension Chrome avec des modifications minimales.  Les API d’extension et les clés de manifeste pris en charge par Chrome sont compatibles avec le code Microsoft Edge.  Pour obtenir la liste des API pris en charge par Microsoft Edge, accédez à [la prise en charge de l’API.][ExtensionApiSupport]  

Pour portez votre extension Chrome, complétez les étapes suivantes.  

1.  Examinez les API d’extension Chrome utilisées dans vos extensions avec la liste Microsoft Edge d’extensions de chrome [pris en][ExtensionApiSupport] charge.  
    
    > [!NOTE]
    > Si votre extension utilise des API qui ne sont pas Microsoft Edge, il se peut qu’elle ne soit pas portée directement.  
    
1.  Dans le fichier manifeste, définissez le `update_URL` champ sur `https://edge.microsoft.com/extensionwebstorebase/v1/crx` .  La valeur pointe vers le fichier de votre extension dans le magasin d’extensions Microsoft Edge et permet Microsoft Edge vérifier les mises à jour `.crx` d’extension.  
1.  Si elle est utilisée dans le nom ou la description de `Chrome` votre extension, renommer votre extension à l’aide `Microsoft Edge` de .  Pour réussir le processus de certification, les modifications sont requises.  
1.  Testez votre extension pour vérifier si elle fonctionne dans Microsoft Edge en [chargeant une version test de votre extension.][ExtensionsGettingStartedExtensionSideloading]  
1.  Si vous faites face à des problèmes, vous pouvez déboguer vos extensions dans Microsoft Edge à l’aide de DevTools, ou [contactez-nous.][mailtoExtensionMicrosoft]  
1.  Suivez les [instructions de publication][ExtensionsPublishPublishExtension] pour publier votre extension sur Microsoft Edge magasin d’extensions.  
    
    > [!NOTE]
    > Si votre extension échange des messages avec une application native à l’aide, assurez-vous que vous définissez sur dans votre fichier manifeste hôte de messagerie `chrome.runtime.connectNative` `allowed_origins` `extension://[Microsoft-Catalog-extensionID]` native.  Le paramètre permet à l’application d’identifier votre extension.  
    
##  <a name="next-steps"></a>Étapes suivantes  

Une fois que votre package d’extension est prêt à être publié dans le magasin Microsoft Edge, créez un compte de développeur [et][ExtensionsPublishCreateDevAccount] [publiez votre extension.][ExtensionsPublishPublishExtension]  

<!-- links -->  

[ExtensionApiSupport]: ./api-support.md "Prise en charge des API | Documents Microsoft"  
[ExtensionsGettingStartedExtensionSideloading]: ../getting-started/extension-sideloading.md "Chargement de version de version | Documents Microsoft"  
[ExtensionsPublishCreateDevAccount]: ../publish/create-dev-account.md "Inscription du développeur | Documents Microsoft"  
[ExtensionsPublishPublishExtension]: ../publish/publish-extension.md "Publier votre extension | Documents Microsoft"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Paiements | Développeur Chrome"  

[mailtoExtensionMicrosoft]: mailto:ext_dev_support@microsoft.com "ext_dev_support@microsoft.com"  
