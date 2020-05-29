---
description: Processus de portage de l’extension chrome vers Microsoft Edge.
title: Extension du chrome port sur le bord Microsoft (chrome)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-chrome, développement d’extensions, extensions de navigateur, compléments, Centre des partenaires, développeur
ms.openlocfilehash: 794e8806a95ce0a70069c65c306c30131b01e24d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565446"
---
# Extension de chrome de port vers Microsoft \ (chrome \)  

Le processus de Portage d’une extension chrome vers Microsoft Edge est très simple.  Extensions écrites pour le chrome, dans la plupart des cas, s’exécutent sur Microsoft Edge avec des modifications minimales.  Les API d’extension et les clés de manifeste prises en charge par chrome sont compatibles avec le code Microsoft Edge.  Toutefois, Microsoft Edge ne prend pas en charge les API d’extension suivantes:  

*   `chrome.gcm`  
*   `chrome.identity.getAccounts`  
*   `chrome.identity.getAuthToken`  
*   `chrome.instanceID`  

> [!Note]
> Pour pouvoir utiliser l’API, l’utilisateur doit être connecté à Microsoft Edge à l’aide d’un compte MSA ou AAD `chrome.identity.getProfileUserInfo` .  Si l’utilisateur est connecté à Microsoft Edge à l’aide **d’une annonce locale**, l’API renvoie les `null` valeurs de messagerie et d’ID.  

> [!IMPORTANT]
> **Paiements**: Microsoft Edge n’a pas de prise en charge directe d’une extension qui utilise les paiements du Windows [Store chrome][ChromeDeveloperWebStorePayments] en raison de la nécessité d’utiliser la `identity.getAuthtoken` requête pour obtenir le jeton des utilisateurs connectés afin d’envoyer la demande d’API de gestion de licences Rest.  Microsoft Edge ne prend pas en charge la `getAuthtoken` requête, donc ce flux ne fonctionne pas.  

Pour porter votre extension chrome, procédez comme suit:  

1.  Passez en revue les API d’extension chrome utilisées dans vos extensions.  Si vous utilisez des fonctionnalités ou des API qui ne sont pas prises en charge par Microsoft Edge, il est possible que vous ne puissiez pas porter votre extension.  
    
    > [!NOTE]
    > L' `getAuthToken` API ne fonctionne pas avec Microsoft Edge, mais vous pouvez l’utiliser `launchWebAuthFlow` pour récupérer un jeton OAuth2 pour authentifier les utilisateurs.  
    
1.  Si vous utilisez `Chrome` le nom ou la description de votre poste, remarquez l’extension de `Microsoft Edge` .  Vous devez réussir le processus de certification.  
    
1.  Testez votre extension pour vérifier qu’elle fonctionne dans Microsoft Edge.  Pour cela, la première étape consiste à vérifier que vous avez activé les fonctionnalités de développement d’extensions.  Cela vous permet de charger les fichiers d’extension dans Microsoft Edge pour pouvoir tester votre extension lors de sa création.  
    
1.  Si vous rencontrez des problèmes, Déboguez vos extensions dans Microsoft Edge à l’aide du DevTools ou [Contactez-nous][mailtoExtensionPartnerOpsMicrosoft].  
    
1.  À présent, votre extension est finalement impeccable et prête à être empaquetée.  Si vous souhaitez préparer la soumission au catalogue de compléments Microsoft Edge (Microsoft Edge addons), vous n’avez pas besoin de empaqueter votre extension.  Vous pouvez également suivre nos recommandations en matière de [publication][ExtensionsPublishExtension] pour publier votre extension sur les modules complémentaires Microsoft Edge.  
    
    > [!NOTE]
    > Si votre extension échange des messages avec une application native utilisant une `chrome.runtime.connectNative` API, assurez-vous de définir `allowedorigins` « `extension://[Microsoft-Catalog-extensionID]` » dans le fichier manifeste de votre hôte de messagerie natif.  Cela permet à l’application d’identifier l’extension.  

<!-- image links -->  

<!-- links -->  

[ExtensionsPublishExtension]: ../publish/publish-extension.md "Publier une extension"  

[mailtoExtensionPartnerOpsMicrosoft]: mailto:extensionpartnerops@microsoft.com "ExtensionPartnerOps@microsoft.com"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Paiements ponctuels-Google Chrome"  
