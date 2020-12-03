---
description: Processus de portage de l’extension chrome vers Microsoft Edge.
title: Extension du chrome port sur Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-chrome, développement d’extensions, extensions de navigateur, compléments, Centre des partenaires, développeur
ms.openlocfilehash: 0f767107bfb259476d1ab35d081fb9bb05c81b46
ms.sourcegitcommit: e79503c6c53ea9b7de58f8cf1532b5c82116a6eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/03/2020
ms.locfileid: "11195158"
---
# Porter votre extension  

Microsoft Edge vous permet de porter votre extension chrome avec les modifications minimales.  Les API d’extension et les clés de manifeste prises en charge par chrome sont compatibles avec le code Microsoft Edge.  Pour obtenir la liste des API prises en charge par Microsoft Edge, accédez à la [prise en charge des API][ExtensionApiSupport].  

Pour porter votre extension chrome, procédez comme suit.  

1.  Passez en revue les API d’extension chrome utilisées dans vos extensions à l’aide de la liste des [API prises en charge][ExtensionApiSupport] par Microsoft Edge extensions.  
    
    > [!NOTE]
    > Si votre extension utilise des API qui ne sont pas prises en charge par Microsoft Edge, il est possible qu’elle ne soit pas portée directement.  
    
1.  Si le nom `Chrome` est utilisé dans le nom ou la description de l’extension, remarquez l’extension de `Microsoft Edge` .  Cette étape est nécessaire pour réussir le processus de certification.  
1.  Testez votre extension pour vérifier qu’elle fonctionne dans Microsoft Edge [chargement indépendant votre extension][ExtensionsGettingStartedExtensionSideloading].  
1.  Si vous rencontrez des problèmes, vous pouvez déboguer vos extensions dans Microsoft Edge à l’aide du DevTools ou [nous contacter][mailtoExtensionMicrosoft].  
1.  Suivez les [recommandations][ExtensionsPublishPublishExtension] en matière de publication pour publier votre extension sur le magasin de modules complémentaires Microsoft Edge.  
    
    > [!NOTE]
    > Si l’extension échange des messages avec une application native en utilisant une `chrome.runtime.connectNative` API, assurez-vous que vous avez défini `allowed_origins` `extension://[Microsoft-Catalog-extensionID]` dans le fichier manifeste de votre hôte de messagerie natif.  Cela permet à l’application d’identifier l’extension.  
    
## Étapes suivantes  

Dès lors que votre package d’extension est prêt à être publié dans le magasin de modules complémentaires Microsoft Edge, [créez un compte de développeur][ExtensionsPublishCreateDevAccount] et [publiez votre extension][ExtensionsPublishPublishExtension].  

<!-- links -->  

[ExtensionApiSupport]: ./api-support.md "Support des API | Documents Microsoft"  
[ExtensionsGettingStartedExtensionSideloading]: ../getting-started/extension-sideloading.md "Charger votre extension | Documents Microsoft"  
[ExtensionsPublishCreateDevAccount]: ../publish/create-dev-account.md "Inscription du développeur | Documents Microsoft"  
[ExtensionsPublishPublishExtension]: ../publish/publish-extension.md "Publier votre extension | Documents Microsoft"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Paiements à la fois | Développeur de chrome"  

[mailtoExtensionMicrosoft]: mailto:ext_dev_support@microsoft.com "ext_dev_support@microsoft.com"  
