---
description: Learn how to statically link the WebView2 loader library.
title: How to Statically link the WebView2 loader library
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/01/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: b7e0ec70cb00f318d4eb67254f37fcec79a5fcf6
ms.sourcegitcommit: 903524ab85321ade278facd741d6487e8cabe33f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/06/2020
ms.locfileid: "11100302"
---
# <span data-ttu-id="f42b5-104">How to Statically link the WebView2 loader library</span><span class="sxs-lookup"><span data-stu-id="f42b5-104">How to Statically link the WebView2 loader library</span></span>  

## <span data-ttu-id="f42b5-105">Context</span><span class="sxs-lookup"><span data-stu-id="f42b5-105">Context</span></span>  

<span data-ttu-id="f42b5-106">What is the WebView2Loader.dll?</span><span class="sxs-lookup"><span data-stu-id="f42b5-106">What is the WebView2Loader.dll?</span></span>  

*   <span data-ttu-id="f42b5-107">The WebView2 SDK contains a header file, `WebView2Loader.dll.`, and the `IDL` file.</span><span class="sxs-lookup"><span data-stu-id="f42b5-107">The WebView2 SDK contains a header file, `WebView2Loader.dll.`, and the `IDL` file.</span></span> `WebView2Loader.dll` <span data-ttu-id="f42b5-108">is a small component that helps apps locate the WebView2 Runtime (or non-stable Microsoft Edge channels) on the device.</span><span class="sxs-lookup"><span data-stu-id="f42b5-108">is a small component that helps apps locate the WebView2 Runtime (or non-stable Microsoft Edge channels) on the device.</span></span>  

<span data-ttu-id="f42b5-109">For apps that have a single runtime, and do not want to ship a `WebView2Loader.dll`, complete the following **Procedure** steps.</span><span class="sxs-lookup"><span data-stu-id="f42b5-109">For apps that have a single runtime, and do not want to ship a `WebView2Loader.dll`, complete the following **Procedure** steps.</span></span>  

## <span data-ttu-id="f42b5-110">Procedure</span><span class="sxs-lookup"><span data-stu-id="f42b5-110">Procedure</span></span>  

1.  <span data-ttu-id="f42b5-111">Open the `.vcxproj` project file for your app in a text editor, such as Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="f42b5-111">Open the `.vcxproj` project file for your app in a text editor, such as Visual Studio Code.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f42b5-112">The `.vcproj` project file may be a hidden file, meaning it does not display in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f42b5-112">The `.vcproj` project file may be a hidden file, meaning it does not display in Visual Studio.</span></span>  <span data-ttu-id="f42b5-113">Use the command-line to find a hidden file.</span><span class="sxs-lookup"><span data-stu-id="f42b5-113">Use the command-line to find a hidden file.</span></span>  
    
1.  <span data-ttu-id="f42b5-114">Locate the section in the code where you include the WebView2 NuGet package target files.</span><span class="sxs-lookup"><span data-stu-id="f42b5-114">Locate the section in the code where you include the WebView2 NuGet package target files.</span></span>  <span data-ttu-id="f42b5-115">The location in the code is highlighted in the following figure.</span><span class="sxs-lookup"><span data-stu-id="f42b5-115">The location in the code is highlighted in the following figure.</span></span>  
    
    :::image type="complex" source="./media/inserthere.png" alt-text="Project Files code snippet" lightbox="./media/inserthere.png"::: 
       <span data-ttu-id="f42b5-117">Project Files code snippet</span><span class="sxs-lookup"><span data-stu-id="f42b5-117">Project Files code snippet</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f42b5-118">Copy the following code snippet and paste it everywhere the `Microsoft.Web.WebView2.targets` is included.</span><span class="sxs-lookup"><span data-stu-id="f42b5-118">Copy the following code snippet and paste it everywhere the `Microsoft.Web.WebView2.targets` is included.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="f42b5-119">For example, include it after the following code block.</span><span class="sxs-lookup"><span data-stu-id="f42b5-119">For example, include it after the following code block.</span></span>  
    > 
    > ```csharp
    > <Import Project="..\packages\Microsoft.Web.WebView2.0.9.579-prerelease\build\native\Microsoft.Web.WebView2.targets" Condition="Exists('..\packages\Microsoft.Web.WebView2.0.9.579-prerelease\build\native\Microsoft.Web.WebView2.targets')" />
    > ```  
    
    ```csharp
    <PropertyGroup> <WebView2LoaderPreference>Static</WebView2LoaderPreference> </PropertyGroup>
    ```
    
    :::image type="complex" source="./media/staticlib.png" alt-text="Project Files code snippet" lightbox="./media/staticlib.png"::: 
       <span data-ttu-id="f42b5-121">Inserted code snippet</span><span class="sxs-lookup"><span data-stu-id="f42b5-121">Inserted code snippet</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f42b5-122">Edit the additional dependencies of the build configuration for your app.</span><span class="sxs-lookup"><span data-stu-id="f42b5-122">Edit the additional dependencies of the build configuration for your app.</span></span>  <span data-ttu-id="f42b5-123">To begin, find all of the `<AdditionalDependencies>` tags.</span><span class="sxs-lookup"><span data-stu-id="f42b5-123">To begin, find all of the `<AdditionalDependencies>` tags.</span></span>  
1.  <span data-ttu-id="f42b5-124">Add `version.lib` as an additional dependency to every different build configuration in the `.vcxproj` file for your app.</span><span class="sxs-lookup"><span data-stu-id="f42b5-124">Add `version.lib` as an additional dependency to every different build configuration in the `.vcxproj` file for your app.</span></span>  
    
    :::image type="complex" source="./media/versionlib.png" alt-text="Project Files code snippet" lightbox="./media/versionlib.png"::: 
       <span data-ttu-id="f42b5-126">Adding `version.lib` to</span><span class="sxs-lookup"><span data-stu-id="f42b5-126">Adding `version.lib` to</span></span> `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="f42b5-127">The WebView2 team aims to automate the additional dependency step in future releases.</span><span class="sxs-lookup"><span data-stu-id="f42b5-127">The WebView2 team aims to automate the additional dependency step in future releases.</span></span>  
    
<span data-ttu-id="f42b5-128">Compile and deploy your app.</span><span class="sxs-lookup"><span data-stu-id="f42b5-128">Compile and deploy your app.</span></span>  <span data-ttu-id="f42b5-129">Success.</span><span class="sxs-lookup"><span data-stu-id="f42b5-129">Success.</span></span>  

## <span data-ttu-id="f42b5-130">See also</span><span class="sxs-lookup"><span data-stu-id="f42b5-130">See also</span></span>  

*   <span data-ttu-id="f42b5-131">To get started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="f42b5-131">To get started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="f42b5-132">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samples] on GitHub.</span><span class="sxs-lookup"><span data-stu-id="f42b5-132">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>
*   <span data-ttu-id="f42b5-133">For more detailed information about WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="f42b5-133">For more detailed information about WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="f42b5-134">For more information about WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="f42b5-134">For more information about WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>

## <span data-ttu-id="f42b5-135">Getting in touch with the WebView2 team</span><span class="sxs-lookup"><span data-stu-id="f42b5-135">Getting in touch with the WebView2 team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  

[Webview2ReferenceDotnet09628MicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: ../reference/dotnet/0-9-628/microsoft-web-webview2-core-corewebview2environmentoptions.md#additionalbrowserarguments "AdditionalBrowserArguments - 0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2EnvironmentOptions class | Microsoft Docs"  
[Webview2ReferenceWin3209622Webview2IdlParameters]: ../reference/win32/0-9-622/webview2-idl.md#createcorewebview2environment  "CreateCoreWebView2Environment - Globals | Microsoft Docs"  
[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2 API Reference | Microsoft Docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Next steps - Introduction to Microsoft Edge WebView2 (Preview) | Microsoft Docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Getting started - Introduction to Microsoft Edge WebView2 (Preview) | Microsoft Docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback - MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "What's new? - JavaScript debugger for Visual Studio Code - microsoft/vscode-js-debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft Edge (Chromium) WebView applications - Visual Studio Code - Debugger for Microsoft Edge - microsoft/vscode-edge-debug2 | GitHub"  
