---
description: Découvrez comment déboguer des contrôles WebView2.
title: Débogage de WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 386bc237257be0ade8c48bc1c737b0151a882719
ms.sourcegitcommit: 5bdffe91a6594f77eeffa4e864fda90a02784771
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2020
ms.locfileid: "10659692"
---
# <span data-ttu-id="3b95d-104">Débogage lors du développement avec des contrôles WebView2</span><span class="sxs-lookup"><span data-stu-id="3b95d-104">How to Debug when developing with WebView2 controls</span></span>  

<span data-ttu-id="3b95d-105">L’objectif du contrôle Microsoft Edge WebView2 combine les fonctionnalités de développement d’applications et les outils de développement d’applications Web et natives.</span><span class="sxs-lookup"><span data-stu-id="3b95d-105">The goal of the Microsoft Edge WebView2 control is combining the best of both the web and native application development features and developer tools.</span></span>  <span data-ttu-id="3b95d-106">Cet article présente les différents outils à utiliser pour le développement de contrôles WebView2.</span><span class="sxs-lookup"><span data-stu-id="3b95d-106">This article outlines the different tools to use when developing with WebView2 controls.</span></span>  

## <span data-ttu-id="3b95d-107">Outils Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="3b95d-107">Microsoft Edge DevTools</span></span>  

<span data-ttu-id="3b95d-108">Utilisez les [outils de développement Microsoft Edge (chrome)](/microsoft-edge/devtools-guide-chromium) pour déboguer le contenu Web affiché dans les contrôles WebView2, de la même façon que si vous utilisiez Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3b95d-108">Use [Microsoft Edge (Chromium) Developer Tools](/microsoft-edge/devtools-guide-chromium) to debug web content displayed in WebView2 controls, in the same way that you would if you were using Microsoft Edge.</span></span>  <span data-ttu-id="3b95d-109">Pour ouvrir le DevTools, positionnez le focus sur la fenêtre WebView, puis utilisez l’une des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="3b95d-109">To open the DevTools, set focus on the WebView window and then use any of the following options.</span></span>  
*   <span data-ttu-id="3b95d-110">Sélectionnez `F12` .</span><span class="sxs-lookup"><span data-stu-id="3b95d-110">Select `F12`.</span></span>  
*   <span data-ttu-id="3b95d-111">Sélectionnez `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="3b95d-111">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="3b95d-112">Ouvrez le menu contextuel (cliquez avec le bouton droit sur \) > sélectionnez `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="3b95d-112">Open the context menu \(right-click\) > select `Inspect`.</span></span>  

:::image type="complex" source="../media/f12.png" alt-text="Outils Microsoft Edge Dev":::
   <span data-ttu-id="3b95d-114">Outils Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="3b95d-114">Microsoft Edge DevTools</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="3b95d-115">Quand vous déboguez votre application dans Visual Studio avec le débogueur natif en pièce jointe, la sélection `F12` de l’application risque de déclencher le débogueur natif au lieu des outils de développement.</span><span class="sxs-lookup"><span data-stu-id="3b95d-115">When you debug your application in Visual Studio with the native debugger attached, selecting `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="3b95d-116">Utilisez `Ctrl` + `Shift` + `I` , ou utilisez le menu contextuel (cliquez avec le bouton droit sur \) pour éviter cette situation.</span><span class="sxs-lookup"><span data-stu-id="3b95d-116">Use `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid this situation.</span></span>  

## <span data-ttu-id="3b95d-117">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3b95d-117">Visual Studio</span></span>  

<span data-ttu-id="3b95d-118">Utilisez le débogueur de script dans Visual Studio 2019 version 16,4 Preview 2 ou version ultérieure pour déboguer votre script dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3b95d-118">Use the script debugger in Visual Studio 2019 version 16.4 Preview 2 or later to debug your script in Visual Studio.</span></span>  <span data-ttu-id="3b95d-119">Vérifiez que le composant de **Diagnostics JavaScript** du **développement de bureau avec charge de** travail en C++ est installé.</span><span class="sxs-lookup"><span data-stu-id="3b95d-119">Verify the **JavaScript diagnostics** component in **Desktop development with C++** workload is installed.</span></span>  

:::image type="complex" source="../media/vs-js-diagnostics.jpg" alt-text="Diagnostics JavaScript Visual Studio":::
   <span data-ttu-id="3b95d-121">Diagnostics JavaScript Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3b95d-121">Visual Studio JavaScript diagnostics</span></span>  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

<span data-ttu-id="3b95d-122">Pour activer le débogage de script WebView2, ouvrez le menu contextuel (cliquez avec le bouton droit sur \) dans votre projet > sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="3b95d-122">To enable WebView2 script debugging, open the context menu \(right-click\) on your project > select **Properties**.</span></span>  <span data-ttu-id="3b95d-123">Dans **Propriétés de configuration**, sélectionnez **débogage**.</span><span class="sxs-lookup"><span data-stu-id="3b95d-123">On **Configuration Properties**, select **Debugging**.</span></span>  <span data-ttu-id="3b95d-124">Dans la propriété **type de débogueur** , choisissez **JavaScript (WebView2)** dans la liste des options.</span><span class="sxs-lookup"><span data-stu-id="3b95d-124">On the **Debugger Type** property, choose **JavaScript (WebView2)** from the list of options.</span></span> 

:::image type="complex" source="../media/vs-script-debugger.jpg" alt-text="Débogueur JavaScript Visual Studio":::
   <span data-ttu-id="3b95d-126">Débogueur JavaScript Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3b95d-126">Visual Studio JavaScript Debugger</span></span>  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

## <span data-ttu-id="3b95d-127">VisualStudioCode</span><span class="sxs-lookup"><span data-stu-id="3b95d-127">Visual Studio Code</span></span>  

<span data-ttu-id="3b95d-128">Vous pouvez utiliser du code Visual Studio pour déboguer des scripts qui s’exécutent dans des contrôles WebView2.</span><span class="sxs-lookup"><span data-stu-id="3b95d-128">You may use Visual Studio Code to debug scripts that run in WebView2 controls.</span></span>  <span data-ttu-id="3b95d-129">Pour plus d’informations, reportez-vous à la rubrique [applications WebView de Microsoft Edge (chrome)](https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications).</span><span class="sxs-lookup"><span data-stu-id="3b95d-129">For more information, see [Microsoft Edge (Chromium) WebView Applications](https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications).</span></span>  

<!--todo:  add See also heading  -->  

## <span data-ttu-id="3b95d-130">Contacter l’équipe WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3b95d-130">Getting in touch with the Microsoft Edge WebView team</span></span>  

<span data-ttu-id="3b95d-131">Aidez-vous à créer une expérience WebView2 plus riche en partageant vos commentaires.</span><span class="sxs-lookup"><span data-stu-id="3b95d-131">Help build a richer WebView2 experience by sharing your feedback.</span></span>  <span data-ttu-id="3b95d-132">Visitez le site de [Commentaires référentiel Samples](https://aka.ms/webviewfeedback) pour envoyer des demandes de fonctionnalité ou des rapports de bogues.</span><span class="sxs-lookup"><span data-stu-id="3b95d-132">Visit the [feedback repo](https://aka.ms/webviewfeedback) to submit feature requests or bug reports.</span></span>  
