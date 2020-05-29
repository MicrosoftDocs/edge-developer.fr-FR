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
# <span data-ttu-id="717ce-104">Extension de chrome de port vers Microsoft \ (chrome \)</span><span class="sxs-lookup"><span data-stu-id="717ce-104">Port Chrome Extension To Microsoft \(Chromium\) Edge</span></span>  

<span data-ttu-id="717ce-105">Le processus de Portage d’une extension chrome vers Microsoft Edge est très simple.</span><span class="sxs-lookup"><span data-stu-id="717ce-105">The process of porting a Chrome Extension to Microsoft Edge is very straightforward.</span></span>  <span data-ttu-id="717ce-106">Extensions écrites pour le chrome, dans la plupart des cas, s’exécutent sur Microsoft Edge avec des modifications minimales.</span><span class="sxs-lookup"><span data-stu-id="717ce-106">Extensions written for Chromium, in most cases, run on Microsoft Edge with minimal changes.</span></span>  <span data-ttu-id="717ce-107">Les API d’extension et les clés de manifeste prises en charge par chrome sont compatibles avec le code Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="717ce-107">The Extension APIs and manifest keys supported by Chrome are code-compatible with Microsoft Edge.</span></span>  <span data-ttu-id="717ce-108">Toutefois, Microsoft Edge ne prend pas en charge les API d’extension suivantes:</span><span class="sxs-lookup"><span data-stu-id="717ce-108">However, Microsoft Edge does not support the following Extension APIs:</span></span>  

*   `chrome.gcm`  
*   `chrome.identity.getAccounts`  
*   `chrome.identity.getAuthToken`  
*   `chrome.instanceID`  

> [!Note]
> <span data-ttu-id="717ce-109">Pour pouvoir utiliser l’API, l’utilisateur doit être connecté à Microsoft Edge à l’aide d’un compte MSA ou AAD `chrome.identity.getProfileUserInfo` .</span><span class="sxs-lookup"><span data-stu-id="717ce-109">The user must be signed into Microsoft Edge using an MSA or AAD account in order to use the `chrome.identity.getProfileUserInfo` API.</span></span>  <span data-ttu-id="717ce-110">Si l’utilisateur est connecté à Microsoft Edge à l’aide **d’une annonce locale**, l’API renvoie les `null` valeurs de messagerie et d’ID.</span><span class="sxs-lookup"><span data-stu-id="717ce-110">If the user is signed into Microsoft Edge using **On-premise AD**, the API returns `null` for the email and ID values.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="717ce-111">**Paiements**: Microsoft Edge n’a pas de prise en charge directe d’une extension qui utilise les paiements du Windows [Store chrome][ChromeDeveloperWebStorePayments] en raison de la nécessité d’utiliser la `identity.getAuthtoken` requête pour obtenir le jeton des utilisateurs connectés afin d’envoyer la demande d’API de gestion de licences Rest.</span><span class="sxs-lookup"><span data-stu-id="717ce-111">**Payments**:  Microsoft Edge does not directly support an Extension that uses [Chrome Web Store payments][ChromeDeveloperWebStorePayments] due to the requirement to use the `identity.getAuthtoken` request to get the token for signed-in users to send the REST-based licensing API request.</span></span>  <span data-ttu-id="717ce-112">Microsoft Edge ne prend pas en charge la `getAuthtoken` requête, donc ce flux ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="717ce-112">Microsoft Edge does not support the `getAuthtoken` request, so this flow does not work.</span></span>  

<span data-ttu-id="717ce-113">Pour porter votre extension chrome, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="717ce-113">To port your Chrome Extension, follow these steps:</span></span>  

1.  <span data-ttu-id="717ce-114">Passez en revue les API d’extension chrome utilisées dans vos extensions.</span><span class="sxs-lookup"><span data-stu-id="717ce-114">Review the Chrome Extension APIs used in your Extensions.</span></span>  <span data-ttu-id="717ce-115">Si vous utilisez des fonctionnalités ou des API qui ne sont pas prises en charge par Microsoft Edge, il est possible que vous ne puissiez pas porter votre extension.</span><span class="sxs-lookup"><span data-stu-id="717ce-115">If you are using features or APIs that are not supported by Microsoft Edge, you may not be able to port your Extension.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="717ce-116">L' `getAuthToken` API ne fonctionne pas avec Microsoft Edge, mais vous pouvez l’utiliser `launchWebAuthFlow` pour récupérer un jeton OAuth2 pour authentifier les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="717ce-116">The `getAuthToken` API does not work with Microsoft Edge, however you may use `launchWebAuthFlow` to fetch an OAuth2 token to authenticate users.</span></span>  
    
1.  <span data-ttu-id="717ce-117">Si vous utilisez `Chrome` le nom ou la description de votre poste, remarquez l’extension de `Microsoft Edge` .</span><span class="sxs-lookup"><span data-stu-id="717ce-117">If you are using `Chrome` in the name or description of your Extension, re-brand the Extension for `Microsoft Edge`.</span></span>  <span data-ttu-id="717ce-118">Vous devez réussir le processus de certification.</span><span class="sxs-lookup"><span data-stu-id="717ce-118">You must pass the certification process.</span></span>  
    
1.  <span data-ttu-id="717ce-119">Testez votre extension pour vérifier qu’elle fonctionne dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="717ce-119">Test your Extension to check if it works in Microsoft Edge.</span></span>  <span data-ttu-id="717ce-120">Pour cela, la première étape consiste à vérifier que vous avez activé les fonctionnalités de développement d’extensions.</span><span class="sxs-lookup"><span data-stu-id="717ce-120">The first step to do this is to ensure that you have Extension developer features turned on.</span></span>  <span data-ttu-id="717ce-121">Cela vous permet de charger les fichiers d’extension dans Microsoft Edge pour pouvoir tester votre extension lors de sa création.</span><span class="sxs-lookup"><span data-stu-id="717ce-121">This enables you to side load Extension files in Microsoft Edge so that you are able to test your Extension while developing it.</span></span>  
    
1.  <span data-ttu-id="717ce-122">Si vous rencontrez des problèmes, Déboguez vos extensions dans Microsoft Edge à l’aide du DevTools ou [Contactez-nous][mailtoExtensionPartnerOpsMicrosoft].</span><span class="sxs-lookup"><span data-stu-id="717ce-122">If you have any issues, debug your Extensions in Microsoft Edge by using the DevTools, or [contact us][mailtoExtensionPartnerOpsMicrosoft].</span></span>  
    
1.  <span data-ttu-id="717ce-123">À présent, votre extension est finalement impeccable et prête à être empaquetée.</span><span class="sxs-lookup"><span data-stu-id="717ce-123">Now your Extension is finally polished up and ready to be packaged.</span></span>  <span data-ttu-id="717ce-124">Si vous souhaitez préparer la soumission au catalogue de compléments Microsoft Edge (Microsoft Edge addons), vous n’avez pas besoin de empaqueter votre extension.</span><span class="sxs-lookup"><span data-stu-id="717ce-124">If you wish to prepare for submission to the Microsoft Edge Addons catalog \(Microsoft Edge Addons\), you do not need to package your Extension.</span></span>  <span data-ttu-id="717ce-125">Vous pouvez également suivre nos recommandations en matière de [publication][ExtensionsPublishExtension] pour publier votre extension sur les modules complémentaires Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="717ce-125">Further, follow our [publishing guidelines][ExtensionsPublishExtension] to publish your Extension on Microsoft Edge Addons.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="717ce-126">Si votre extension échange des messages avec une application native utilisant une `chrome.runtime.connectNative` API, assurez-vous de définir `allowedorigins` « `extension://[Microsoft-Catalog-extensionID]` » dans le fichier manifeste de votre hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="717ce-126">If your Extension exchanges messages with a native application using `chrome.runtime.connectNative` API, ensure that you set `allowedorigins` to "`extension://[Microsoft-Catalog-extensionID]`" in your native messaging host manifest file.</span></span>  <span data-ttu-id="717ce-127">Cela permet à l’application d’identifier l’extension.</span><span class="sxs-lookup"><span data-stu-id="717ce-127">This enables the app to identify the Extension.</span></span>  

<!-- image links -->  

<!-- links -->  

[ExtensionsPublishExtension]: ../publish/publish-extension.md "Publier une extension"  

[mailtoExtensionPartnerOpsMicrosoft]: mailto:extensionpartnerops@microsoft.com "ExtensionPartnerOps@microsoft.com"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Paiements ponctuels-Google Chrome"  
