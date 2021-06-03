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
# <span data-ttu-id="0aeb5-104">Portage de votre extension</span><span class="sxs-lookup"><span data-stu-id="0aeb5-104">Port your extension</span></span>  

<span data-ttu-id="0aeb5-105">Microsoft Edge vous permet de porter votre extension Chrome avec des modifications minimales.</span><span class="sxs-lookup"><span data-stu-id="0aeb5-105">Microsoft Edge allows you to port your Chrome extension with minimal changes.</span></span>  <span data-ttu-id="0aeb5-106">Les API d’extension et les clés de manifeste pris en charge par Chrome sont compatibles avec le code Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0aeb5-106">The Extension APIs and manifest keys supported by Chrome are code-compatible with Microsoft Edge.</span></span>  <span data-ttu-id="0aeb5-107">Pour obtenir la liste des API pris en charge par Microsoft Edge, accédez à [la prise en charge de l’API.][ExtensionApiSupport]</span><span class="sxs-lookup"><span data-stu-id="0aeb5-107">For a list of APIs supported by Microsoft Edge, navigate to [API support][ExtensionApiSupport].</span></span>  

<span data-ttu-id="0aeb5-108">Pour portez votre extension Chrome, complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="0aeb5-108">To port your Chrome extension, complete the following steps.</span></span>  

1.  <span data-ttu-id="0aeb5-109">Examinez les API d’extension Chrome utilisées dans vos extensions avec la liste Microsoft Edge d’extensions de chrome [pris en][ExtensionApiSupport] charge.</span><span class="sxs-lookup"><span data-stu-id="0aeb5-109">Review the Chrome extension APIs used in your extensions with the Microsoft Edge extensions [supported APIs][ExtensionApiSupport] list.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="0aeb5-110">Si votre extension utilise des API qui ne sont pas Microsoft Edge, il se peut qu’elle ne soit pas portée directement.</span><span class="sxs-lookup"><span data-stu-id="0aeb5-110">If your extension uses APIs that are not supported by Microsoft Edge, it may not port directly.</span></span>  
    
1.  <span data-ttu-id="0aeb5-111">Dans le fichier manifeste, définissez le `update_URL` champ sur `https://edge.microsoft.com/extensionwebstorebase/v1/crx` .</span><span class="sxs-lookup"><span data-stu-id="0aeb5-111">In the manifest file, set the `update_URL` field to `https://edge.microsoft.com/extensionwebstorebase/v1/crx`.</span></span>  <span data-ttu-id="0aeb5-112">La valeur pointe vers le fichier de votre extension dans le magasin d’extensions Microsoft Edge et permet Microsoft Edge vérifier les mises à jour `.crx` d’extension.</span><span class="sxs-lookup"><span data-stu-id="0aeb5-112">The value points to the `.crx` file of your extension in the Microsoft Edge Add-ons store and allows Microsoft Edge to check for extension updates.</span></span>  
1.  <span data-ttu-id="0aeb5-113">Si elle est utilisée dans le nom ou la description de `Chrome` votre extension, renommer votre extension à l’aide `Microsoft Edge` de .</span><span class="sxs-lookup"><span data-stu-id="0aeb5-113">If `Chrome` is used in either the name or the description of your extension, rebrand your extension using `Microsoft Edge`.</span></span>  <span data-ttu-id="0aeb5-114">Pour réussir le processus de certification, les modifications sont requises.</span><span class="sxs-lookup"><span data-stu-id="0aeb5-114">To pass the certification process, the changes are required.</span></span>  
1.  <span data-ttu-id="0aeb5-115">Testez votre extension pour vérifier si elle fonctionne dans Microsoft Edge en [chargeant une version test de votre extension.][ExtensionsGettingStartedExtensionSideloading]</span><span class="sxs-lookup"><span data-stu-id="0aeb5-115">Test your extension to check if it works in Microsoft Edge by [sideloading your extension][ExtensionsGettingStartedExtensionSideloading].</span></span>  
1.  <span data-ttu-id="0aeb5-116">Si vous faites face à des problèmes, vous pouvez déboguer vos extensions dans Microsoft Edge à l’aide de DevTools, ou [contactez-nous.][mailtoExtensionMicrosoft]</span><span class="sxs-lookup"><span data-stu-id="0aeb5-116">If you face any issues, you may debug your extensions in Microsoft Edge by using the DevTools, or [contact us][mailtoExtensionMicrosoft].</span></span>  
1.  <span data-ttu-id="0aeb5-117">Suivez les [instructions de publication][ExtensionsPublishPublishExtension] pour publier votre extension sur Microsoft Edge magasin d’extensions.</span><span class="sxs-lookup"><span data-stu-id="0aeb5-117">Follow the [publishing guidelines][ExtensionsPublishPublishExtension] to publish your extension on Microsoft Edge Add-ons store.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="0aeb5-118">Si votre extension échange des messages avec une application native à l’aide, assurez-vous que vous définissez sur dans votre fichier manifeste hôte de messagerie `chrome.runtime.connectNative` `allowed_origins` `extension://[Microsoft-Catalog-extensionID]` native.</span><span class="sxs-lookup"><span data-stu-id="0aeb5-118">If your extension exchanges messages with a native app using `chrome.runtime.connectNative`, ensure that you set `allowed_origins` to `extension://[Microsoft-Catalog-extensionID]` in your native messaging host manifest file.</span></span>  <span data-ttu-id="0aeb5-119">Le paramètre permet à l’application d’identifier votre extension.</span><span class="sxs-lookup"><span data-stu-id="0aeb5-119">The setting allows the app to identify your extension.</span></span>  
    
## <span data-ttu-id="0aeb5-120">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="0aeb5-120">Next steps</span></span>  

<span data-ttu-id="0aeb5-121">Une fois que votre package d’extension est prêt à être publié dans le magasin Microsoft Edge, créez un compte de développeur [et][ExtensionsPublishCreateDevAccount] [publiez votre extension.][ExtensionsPublishPublishExtension]</span><span class="sxs-lookup"><span data-stu-id="0aeb5-121">After your extension package is ready to publish in the Microsoft Edge Add-ons store, [create a developer account][ExtensionsPublishCreateDevAccount] and [publish your extension][ExtensionsPublishPublishExtension].</span></span>  

<!-- links -->  

[ExtensionApiSupport]: ./api-support.md "Prise en charge des API | Documents Microsoft"  
[ExtensionsGettingStartedExtensionSideloading]: ../getting-started/extension-sideloading.md "Chargement de version de version | Documents Microsoft"  
[ExtensionsPublishCreateDevAccount]: ../publish/create-dev-account.md "Inscription du développeur | Documents Microsoft"  
[ExtensionsPublishPublishExtension]: ../publish/publish-extension.md "Publier votre extension | Documents Microsoft"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Paiements | Développeur Chrome"  

[mailtoExtensionMicrosoft]: mailto:ext_dev_support@microsoft.com "ext_dev_support@microsoft.com"  
