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
# <span data-ttu-id="4d6b9-104">Porter votre extension</span><span class="sxs-lookup"><span data-stu-id="4d6b9-104">Port your extension</span></span>  

<span data-ttu-id="4d6b9-105">Microsoft Edge vous permet de porter votre extension chrome avec les modifications minimales.</span><span class="sxs-lookup"><span data-stu-id="4d6b9-105">Microsoft Edge allows you to port your Chrome extension with minimal changes.</span></span>  <span data-ttu-id="4d6b9-106">Les API d’extension et les clés de manifeste prises en charge par chrome sont compatibles avec le code Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4d6b9-106">The Extension APIs and manifest keys supported by Chrome are code-compatible with Microsoft Edge.</span></span>  <span data-ttu-id="4d6b9-107">Pour obtenir la liste des API prises en charge par Microsoft Edge, accédez à la [prise en charge des API][ExtensionApiSupport].</span><span class="sxs-lookup"><span data-stu-id="4d6b9-107">For a list of APIs supported by Microsoft Edge, navigate to [API support][ExtensionApiSupport].</span></span>  

<span data-ttu-id="4d6b9-108">Pour porter votre extension chrome, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="4d6b9-108">To port your Chrome extension, complete the following steps.</span></span>  

1.  <span data-ttu-id="4d6b9-109">Passez en revue les API d’extension chrome utilisées dans vos extensions à l’aide de la liste des [API prises en charge][ExtensionApiSupport] par Microsoft Edge extensions.</span><span class="sxs-lookup"><span data-stu-id="4d6b9-109">Review the Chrome extension APIs used in your extensions with the Microsoft Edge extensions [supported APIs][ExtensionApiSupport] list.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="4d6b9-110">Si votre extension utilise des API qui ne sont pas prises en charge par Microsoft Edge, il est possible qu’elle ne soit pas portée directement.</span><span class="sxs-lookup"><span data-stu-id="4d6b9-110">If your extension uses APIs that are not supported by Microsoft Edge, it may not port directly.</span></span>  
    
1.  <span data-ttu-id="4d6b9-111">Si le nom `Chrome` est utilisé dans le nom ou la description de l’extension, remarquez l’extension de `Microsoft Edge` .</span><span class="sxs-lookup"><span data-stu-id="4d6b9-111">If the name `Chrome` is being used in either the name or the description of the extension, rebrand the extension for `Microsoft Edge`.</span></span>  <span data-ttu-id="4d6b9-112">Cette étape est nécessaire pour réussir le processus de certification.</span><span class="sxs-lookup"><span data-stu-id="4d6b9-112">This step is required to pass the certification process.</span></span>  
1.  <span data-ttu-id="4d6b9-113">Testez votre extension pour vérifier qu’elle fonctionne dans Microsoft Edge [chargement indépendant votre extension][ExtensionsGettingStartedExtensionSideloading].</span><span class="sxs-lookup"><span data-stu-id="4d6b9-113">Test your extension to check if it works in Microsoft Edge by [sideloading your extension][ExtensionsGettingStartedExtensionSideloading].</span></span>  
1.  <span data-ttu-id="4d6b9-114">Si vous rencontrez des problèmes, vous pouvez déboguer vos extensions dans Microsoft Edge à l’aide du DevTools ou [nous contacter][mailtoExtensionMicrosoft].</span><span class="sxs-lookup"><span data-stu-id="4d6b9-114">If you face any issues, you may debug your extensions in Microsoft Edge by using the DevTools, or [contact us][mailtoExtensionMicrosoft].</span></span>  
1.  <span data-ttu-id="4d6b9-115">Suivez les [recommandations][ExtensionsPublishPublishExtension] en matière de publication pour publier votre extension sur le magasin de modules complémentaires Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4d6b9-115">Follow the [publishing guidelines][ExtensionsPublishPublishExtension] to publish your extension on Microsoft Edge Add-ons store.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="4d6b9-116">Si l’extension échange des messages avec une application native en utilisant une `chrome.runtime.connectNative` API, assurez-vous que vous avez défini `allowed_origins` `extension://[Microsoft-Catalog-extensionID]` dans le fichier manifeste de votre hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="4d6b9-116">If the extension exchanges messages with a native app using `chrome.runtime.connectNative` API, ensure that you set `allowed_origins` to `extension://[Microsoft-Catalog-extensionID]` in your native messaging host manifest file.</span></span>  <span data-ttu-id="4d6b9-117">Cela permet à l’application d’identifier l’extension.</span><span class="sxs-lookup"><span data-stu-id="4d6b9-117">This enables the app to identify the extension.</span></span>  
    
## <span data-ttu-id="4d6b9-118">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="4d6b9-118">Next steps</span></span>  

<span data-ttu-id="4d6b9-119">Dès lors que votre package d’extension est prêt à être publié dans le magasin de modules complémentaires Microsoft Edge, [créez un compte de développeur][ExtensionsPublishCreateDevAccount] et [publiez votre extension][ExtensionsPublishPublishExtension].</span><span class="sxs-lookup"><span data-stu-id="4d6b9-119">Once your extension package is ready to be published to Microsoft Edge add-ons store, [create a developer account][ExtensionsPublishCreateDevAccount] and [publish your extension][ExtensionsPublishPublishExtension].</span></span>  

<!-- links -->  

[ExtensionApiSupport]: ./api-support.md "Support des API | Documents Microsoft"  
[ExtensionsGettingStartedExtensionSideloading]: ../getting-started/extension-sideloading.md "Charger votre extension | Documents Microsoft"  
[ExtensionsPublishCreateDevAccount]: ../publish/create-dev-account.md "Inscription du développeur | Documents Microsoft"  
[ExtensionsPublishPublishExtension]: ../publish/publish-extension.md "Publier votre extension | Documents Microsoft"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Paiements à la fois | Développeur de chrome"  

[mailtoExtensionMicrosoft]: mailto:ext_dev_support@microsoft.com "ext_dev_support@microsoft.com"  
