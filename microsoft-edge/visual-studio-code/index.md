---
description: Microsoft Edge (Chromium) et Visual Studio Code
title: Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, développement web, outils f12, devtools, vs code, visual studio code, débogueur, webhint
ms.openlocfilehash: 1aa5b66043e87ebb0f1b848dcd60e2553b378f36
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230690"
---
# <span data-ttu-id="c0d81-104">Vue d’ensemble du Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="c0d81-104">Visual Studio Code overview</span></span>  

<span data-ttu-id="c0d81-105">[Visual Studio Code][VisualStudioCodeDocs] est un éditeur de code source léger mais puissant.</span><span class="sxs-lookup"><span data-stu-id="c0d81-105">[Visual Studio Code][VisualStudioCodeDocs] is a lightweight, but powerful source code editor.</span></span>  <span data-ttu-id="c0d81-106">[Visual Studio Code][VisualStudioCodeDocs] est disponible pour Windows, Linux et macOS.</span><span class="sxs-lookup"><span data-stu-id="c0d81-106">[Visual Studio Code][VisualStudioCodeDocs] is available for Windows, Linux, and macOS.</span></span>  <span data-ttu-id="c0d81-107">Il inclut la prise en charge intégrée de JavaScript, TypeScript et Node.js, c’est donc un excellent outil pour les développeurs web avant de le personnaliser.</span><span class="sxs-lookup"><span data-stu-id="c0d81-107">It includes built-in support for JavaScript, TypeScript, and Node.js, so it is a great tool for web developers before you customize it.</span></span>  <span data-ttu-id="c0d81-108">Si vous ne l’utilisez pas encore, [téléchargez Visual Studio Code][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="c0d81-108">If you are not using it yet, download [Visual Studio Code][VisualstudioCode].</span></span>  

## <span data-ttu-id="c0d81-109">Extensions</span><span class="sxs-lookup"><span data-stu-id="c0d81-109">Extensions</span></span>  

<!--todo: We want to put something like the tiles for extensions Visual Studio Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page.  I think it's a web page.  I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->  

<span data-ttu-id="c0d81-110">Pour acquérir l’une des extensions mises en évidence ci-dessous, accédez à Extensions \(sélectionnez sur Windows/Linux ou sur `Ctrl` + `Shift` + `X` `Command` + `Shift` + `X` macOS\) dans Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="c0d81-110">To acquire any of the extensions highlighted below, navigate to Extensions \(select `Ctrl`+`Shift`+`X` on Windows/Linux or `Command`+`Shift`+`X` on macOS\) in Visual Studio Code.</span></span>  

<span data-ttu-id="c0d81-111">Recherchez l’extension spécifique sur Marketplace et choisissez **Installer.**</span><span class="sxs-lookup"><span data-stu-id="c0d81-111">Search the Marketplace for the specific extension and choose **Install**.</span></span>  

:::image type="complex" source="./media/vscode-debugger-install.png" alt-text="Installer le débogger pour l Microsoft Edge Visual Studio Code extension" lightbox="./media/vscode-debugger-install.png":::
   <span data-ttu-id="c0d81-113">Installer le **débogger pour l Microsoft Edge** Visual Studio Code extension</span><span class="sxs-lookup"><span data-stu-id="c0d81-113">Install the **Debugger for Microsoft Edge** Visual Studio Code extension</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png" alt-text="Débogger pour l Microsoft Edge Visual Studio Code extension" lightbox="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png":::
         <span data-ttu-id="c0d81-115">**Débogger pour l Microsoft Edge** Visual Studio Code extension</span><span class="sxs-lookup"><span data-stu-id="c0d81-115">**Debugger for Microsoft Edge** Visual Studio Code extension</span></span>  
      :::image-end:::  
      [<span data-ttu-id="c0d81-116">Débogger pour Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c0d81-116">Debugger for Microsoft Edge</span></span>](#debugger-for-microsoft-edge)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png" alt-text="Microsoft Edge Outils pour l Visual Studio Code Visual Studio Code extension" lightbox="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png":::
         <span data-ttu-id="c0d81-118">**Microsoft Edge outils pour l Visual Studio Code** Visual Studio Code extension</span><span class="sxs-lookup"><span data-stu-id="c0d81-118">**Microsoft Edge Tools for Visual Studio Code** Visual Studio Code extension</span></span>  
      :::image-end:::  
      [<span data-ttu-id="c0d81-119">Microsoft Edge Outils pour Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="c0d81-119">Microsoft Edge Tools for Visual Studio Code</span></span>](#microsoft-edge-tools-for-visual-studio-code)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-webhint.msft.png" alt-text="extension de Visual Studio Code webhint" lightbox="./media/visual-studio-code-extension-webhint.msft.png":::
         <span data-ttu-id="c0d81-121">**extension de Visual Studio Code webhint**</span><span class="sxs-lookup"><span data-stu-id="c0d81-121">**webhint** Visual Studio Code extension</span></span>  
      :::image-end:::  
      [<span data-ttu-id="c0d81-122">webhint</span><span class="sxs-lookup"><span data-stu-id="c0d81-122">webhint</span></span>](#webhint)  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="c0d81-123">Débogger pour Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c0d81-123">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="c0d81-124">Avec l’extension [Déboguer pour Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Code, déboguer votre code JavaScript frontal ligne par ligne et voir les instructions directement à partir `console.log()` [Visual Studio Code][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="c0d81-124">With the [Debugger for Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Code extension, debug your front-end JavaScript code line-by-line and see `console.log()` statements directly from [Visual Studio Code][VisualstudioCode].</span></span>  
      
<span data-ttu-id="c0d81-125">À l’aide de l’outil Débogger, vous pouvez lancer ou attacher les deux Microsoft Edge \(EdgeHTML\) et Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="c0d81-125">Using the Debugger tool, you may launch or attach to both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="c0d81-126">Pour une walkthrough de débogage de Microsoft Edge à partir de Visual Studio Code et d’exemples de configurations, accédez à `launch.json` [Déboguer][VisualStudioCodeDebuggerEdge]pour Microsoft Edge Visual Studio Code extension .</span><span class="sxs-lookup"><span data-stu-id="c0d81-126">For a walkthrough of debugging Microsoft Edge from Visual Studio Code and sample `launch.json` configurations, navigate to [Debugger For Microsoft Edge Visual Studio Code Extension][VisualStudioCodeDebuggerEdge].</span></span>  <span data-ttu-id="c0d81-127">Choisissez l’image suivante pour voir l’extension en action.</span><span class="sxs-lookup"><span data-stu-id="c0d81-127">Choose the following image to see the extension in action.</span></span>  

:::image type="complex" source="./media/debugger-for-edge.png" alt-text="Débogger pour l’extension Visual Studio Code Edge en action" lightbox="./media/debugger-for-edge.gif":::
   <span data-ttu-id="c0d81-129">**Débogger pour l Microsoft Edge** Visual Studio Code extension en action</span><span class="sxs-lookup"><span data-stu-id="c0d81-129">**Debugger for Microsoft Edge** Visual Studio Code extension in action</span></span>  
:::image-end:::  

## <span data-ttu-id="c0d81-130">Microsoft Edge Outils pour Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="c0d81-130">Microsoft Edge Tools for Visual Studio Code</span></span>

<span data-ttu-id="c0d81-131">Avec [l’extension Microsoft Edge Outils][VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode] Visual Studio Code Visual Studio Code, utilisez l’outil **Éléments** du navigateur Microsoft Edge dans Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="c0d81-131">With the [Microsoft Edge Tools for Visual Studio Code][VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode] Visual Studio Code extension, use the **Elements** tool of the Microsoft Edge browser within Visual Studio Code.</span></span>  <span data-ttu-id="c0d81-132">Utilisez-le pour les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="c0d81-132">Use it for the following actions.</span></span>  

*   <span data-ttu-id="c0d81-133">Attacher à une instance ou lancer une instance de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c0d81-133">Attach to an instance or launch an instance of Microsoft Edge.</span></span>  
*   <span data-ttu-id="c0d81-134">Afficher la structure HTML d’runtime.</span><span class="sxs-lookup"><span data-stu-id="c0d81-134">Display the runtime HTML structure.</span></span>  
*   <span data-ttu-id="c0d81-135">Mettez à jour la disposition.</span><span class="sxs-lookup"><span data-stu-id="c0d81-135">Update the layout.</span></span>  
*   <span data-ttu-id="c0d81-136">Résoudre les problèmes de style.</span><span class="sxs-lookup"><span data-stu-id="c0d81-136">Fix styling issues.</span></span>  
    
<span data-ttu-id="c0d81-137">Pour plus d’informations, [accédez à Microsoft Edge Outils pour Visual Studio Code Visual Studio Code extension .][VisualStudioCodeMicrosoftEdgeDevtoolsExtension]</span><span class="sxs-lookup"><span data-stu-id="c0d81-137">For more information, navigate to [Microsoft Edge Tools for Visual Studio Code Visual Studio Code extension][VisualStudioCodeMicrosoftEdgeDevtoolsExtension].</span></span>  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/microsoft-edge-tools-for-visual-studio-code.png" alt-text="Microsoft Edge Outils pour Visual Studio Code Visual Studio Code extension en action" lightbox="./media/microsoft-edge-tools-for-visual-studio-code.png":::
   <span data-ttu-id="c0d81-139">**Microsoft Edge outils pour Visual Studio Code** Visual Studio Code extension en action</span><span class="sxs-lookup"><span data-stu-id="c0d81-139">**Microsoft Edge Tools for Visual Studio Code** Visual Studio Code extension in action</span></span>  
:::image-end:::  

## <span data-ttu-id="c0d81-140">webhint</span><span class="sxs-lookup"><span data-stu-id="c0d81-140">webhint</span></span>  
      
<span data-ttu-id="c0d81-141">Utilisez [webhint,][WebhintMain]un outil de linting personnalisable, pour améliorer les fonctionnalités suivantes de votre site.</span><span class="sxs-lookup"><span data-stu-id="c0d81-141">Use [webhint][WebhintMain], a customizable linting tool, to improve the following functionality of your site.</span></span>  

*   <span data-ttu-id="c0d81-142">Accessibilité</span><span class="sxs-lookup"><span data-stu-id="c0d81-142">Accessibility</span></span>
*   <span data-ttu-id="c0d81-143">Performances</span><span class="sxs-lookup"><span data-stu-id="c0d81-143">Performance</span></span>
*   <span data-ttu-id="c0d81-144">Compatibilité entre navigateurs</span><span class="sxs-lookup"><span data-stu-id="c0d81-144">Cross-browser compatibility</span></span>
*   <span data-ttu-id="c0d81-145">PWA compatibilité</span><span class="sxs-lookup"><span data-stu-id="c0d81-145">PWA compatibility</span></span>
*   <span data-ttu-id="c0d81-146">Sécurité</span><span class="sxs-lookup"><span data-stu-id="c0d81-146">Security</span></span>

<span data-ttu-id="c0d81-147">Il vérifie les pratiques de codage et les erreurs courantes dans votre code.</span><span class="sxs-lookup"><span data-stu-id="c0d81-147">It checks your code for coding practices and common errors.</span></span> <span data-ttu-id="c0d81-148">Le projet open source webhint, initialement développé par l’équipe Microsoft Edge, fait désormais partie [d’OpenJS Foundation.][OpenjsFoundation]</span><span class="sxs-lookup"><span data-stu-id="c0d81-148">The webhint open-source project, initially developed by the Microsoft Edge team, is now part of the [OpenJS Foundation][OpenjsFoundation].</span></span>  <span data-ttu-id="c0d81-149">L Microsoft Edge de recherche continue de contribuer à lahint web aux côtés des développeurs web de la communauté.</span><span class="sxs-lookup"><span data-stu-id="c0d81-149">The Microsoft Edge team continues to contribute to webhint alongside web developers in the community.</span></span>  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/webhint-extension.png" alt-text="Capture d’écran de l’extension Visual Studio Code webhint" lightbox="./media/webhint-extension.png":::
   <span data-ttu-id="c0d81-151">Capture d’écran de l’extension Visual Studio Code **webhint**</span><span class="sxs-lookup"><span data-stu-id="c0d81-151">Screenshot of **webhint** Visual Studio Code extension</span></span>  
:::image-end:::  
      
<span data-ttu-id="c0d81-152">Identifiez et corrigez les problèmes dans votre site web en ajoutant [l’extension dehint web pour Visual Studio Code][VisualstudioMarketplaceWebhint].</span><span class="sxs-lookup"><span data-stu-id="c0d81-152">Identify and fix problems in your website by adding the [webhint extension for Visual Studio Code][VisualstudioMarketplaceWebhint].</span></span>  <span data-ttu-id="c0d81-153">Les conseils examinent le code HTML, CSS, JavaScript, TypeScript, etc.</span><span class="sxs-lookup"><span data-stu-id="c0d81-153">Hints examine HTML, CSS, JavaScript, TypeScript, and more.</span></span>  <span data-ttu-id="c0d81-154">Les conseils apparaissent comme des soulignements inline et sont résumés **dans** le volet Problèmes.</span><span class="sxs-lookup"><span data-stu-id="c0d81-154">Hints appear as inline underlines and are summarized in the **Problems** pane.</span></span>  
      
<span data-ttu-id="c0d81-155">Pour plus d’informations, accédez [à Comment utiliser lahint web dans Visual Studio Code][VisualStudioCodeWebhint].</span><span class="sxs-lookup"><span data-stu-id="c0d81-155">For more information, navigate to [How to use webhint in Visual Studio Code][VisualStudioCodeWebhint].</span></span>  

<!--links -->  

[VisualStudioCodeDebuggerEdge]: ./debugger-for-edge.md "Débogger for Microsoft Edge Visual Studio Code Extension | Documents Microsoft"  
[VisualStudioCodeMicrosoftEdgeDevtoolsExtension]: ./microsoft-edge-devtools-extension.md "Microsoft Edge DevTools pour les Visual Studio Code d’extension | Documents Microsoft"  
[VisualStudioCodeWebhint]: ./webhint.md "Webhint Visual Studio Code extension | Documents Microsoft"  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentation | Visual Studio Code"   

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Débogger pour Microsoft Edge | Visual Studio Marketplace"  
[VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Outils Microsoft Edge pour Visual Studio Code | Visual Studio Marketplace"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[WebhintMain]:  https://webhint.io "webhint"  
[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  
