---
description: Microsoft Edge (chrome) et code Visual Studio
title: VisualStudioCode
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, code vs, code Visual Studio, débogueur, webhint
ms.openlocfilehash: 1aa5b66043e87ebb0f1b848dcd60e2553b378f36
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230690"
---
# <span data-ttu-id="250f6-104">Présentation du code Visual Studio</span><span class="sxs-lookup"><span data-stu-id="250f6-104">Visual Studio Code overview</span></span>  

<span data-ttu-id="250f6-105">Le [code Visual Studio][VisualStudioCodeDocs] est un éditeur de code source léger, mais puissant.</span><span class="sxs-lookup"><span data-stu-id="250f6-105">[Visual Studio Code][VisualStudioCodeDocs] is a lightweight, but powerful source code editor.</span></span>  <span data-ttu-id="250f6-106">Le [code Visual Studio][VisualStudioCodeDocs] est disponible pour Windows, Linux et MacOS.</span><span class="sxs-lookup"><span data-stu-id="250f6-106">[Visual Studio Code][VisualStudioCodeDocs] is available for Windows, Linux, and macOS.</span></span>  <span data-ttu-id="250f6-107">Il inclut une prise en charge intégrée pour JavaScript, la machine à écrire et Node.js, donc c’est un excellent outil pour les développeurs Web avant de le personnaliser.</span><span class="sxs-lookup"><span data-stu-id="250f6-107">It includes built-in support for JavaScript, TypeScript, and Node.js, so it is a great tool for web developers before you customize it.</span></span>  <span data-ttu-id="250f6-108">Si vous ne l’utilisez pas encore, téléchargez le [code Visual Studio][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="250f6-108">If you are not using it yet, download [Visual Studio Code][VisualstudioCode].</span></span>  

## <span data-ttu-id="250f6-109">Extensions</span><span class="sxs-lookup"><span data-stu-id="250f6-109">Extensions</span></span>  

<!--todo: We want to put something like the tiles for extensions Visual Studio Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page.  I think it's a web page.  I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->  

<span data-ttu-id="250f6-110">Pour acquérir les extensions mises en surbrillance ci-dessous, accédez à extensions \(sélectionnez `Ctrl` + `Shift` + `X` sur Windows/Linux ou `Command` + `Shift` + `X` Mac \) dans le code Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="250f6-110">To acquire any of the extensions highlighted below, navigate to Extensions \(select `Ctrl`+`Shift`+`X` on Windows/Linux or `Command`+`Shift`+`X` on macOS\) in Visual Studio Code.</span></span>  

<span data-ttu-id="250f6-111">Recherchez l’extension dans Marketplace et sélectionnez **installer**.</span><span class="sxs-lookup"><span data-stu-id="250f6-111">Search the Marketplace for the specific extension and choose **Install**.</span></span>  

:::image type="complex" source="./media/vscode-debugger-install.png" alt-text="Installer le débogueur pour l’extension de code Visual Studio Visual Studio" lightbox="./media/vscode-debugger-install.png":::
   <span data-ttu-id="250f6-113">Installer le **débogueur pour** l’extension de code Visual Studio Visual Studio</span><span class="sxs-lookup"><span data-stu-id="250f6-113">Install the **Debugger for Microsoft Edge** Visual Studio Code extension</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png" alt-text="Débogueur de l’extension de code Visual Studio Visual Studio" lightbox="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png":::
         <span data-ttu-id="250f6-115">**Débogueur pour Microsoft Edge** Extension de code Visual Studio</span><span class="sxs-lookup"><span data-stu-id="250f6-115">**Debugger for Microsoft Edge** Visual Studio Code extension</span></span>  
      :::image-end:::  
      [<span data-ttu-id="250f6-116">Débogueur pour Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="250f6-116">Debugger for Microsoft Edge</span></span>](#debugger-for-microsoft-edge)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png" alt-text="Extensions de code Visual Studio Microsoft Edge Tools pour Visual Studio" lightbox="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png":::
         <span data-ttu-id="250f6-118">**Microsoft Edge Tools pour le code Visual Studio** Extension de code Visual Studio</span><span class="sxs-lookup"><span data-stu-id="250f6-118">**Microsoft Edge Tools for Visual Studio Code** Visual Studio Code extension</span></span>  
      :::image-end:::  
      [<span data-ttu-id="250f6-119">Microsoft Edge Tools pour le code Visual Studio</span><span class="sxs-lookup"><span data-stu-id="250f6-119">Microsoft Edge Tools for Visual Studio Code</span></span>](#microsoft-edge-tools-for-visual-studio-code)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-webhint.msft.png" alt-text="extension de code Visual Studio webhint" lightbox="./media/visual-studio-code-extension-webhint.msft.png":::
         <span data-ttu-id="250f6-121">**Astuce** Extension de code Visual Studio</span><span class="sxs-lookup"><span data-stu-id="250f6-121">**webhint** Visual Studio Code extension</span></span>  
      :::image-end:::  
      [<span data-ttu-id="250f6-122">webhint</span><span class="sxs-lookup"><span data-stu-id="250f6-122">webhint</span></span>](#webhint)  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="250f6-123">Débogueur pour Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="250f6-123">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="250f6-124">Avec le [débogueur de][VisualstudioMarketplaceDebuggerMicrosoftEdge] l’extension de code Visual Studio Microsoft Edge, déboguez votre code JavaScript frontal par ligne et consultez les `console.log()` instructions directement à partir du [code Visual Studio][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="250f6-124">With the [Debugger for Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Code extension, debug your front-end JavaScript code line-by-line and see `console.log()` statements directly from [Visual Studio Code][VisualstudioCode].</span></span>  
      
<span data-ttu-id="250f6-125">À l’aide de l’outil de débogage, vous pouvez lancer une connexion à Microsoft Edge \(EdgeHTML \) et à Microsoft Edge \(chrome \).</span><span class="sxs-lookup"><span data-stu-id="250f6-125">Using the Debugger tool, you may launch or attach to both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="250f6-126">Pour obtenir une procédure pas à pas de débogage de Microsoft Edge à partir de l’exemple de code et de configurations Visual Studio `launch.json` , accédez à [débogueur pour l’extension de code Visual Studio Visual Studio][VisualStudioCodeDebuggerEdge].</span><span class="sxs-lookup"><span data-stu-id="250f6-126">For a walkthrough of debugging Microsoft Edge from Visual Studio Code and sample `launch.json` configurations, navigate to [Debugger For Microsoft Edge Visual Studio Code Extension][VisualStudioCodeDebuggerEdge].</span></span>  <span data-ttu-id="250f6-127">Cliquez sur l’image suivante pour afficher l’extension en action.</span><span class="sxs-lookup"><span data-stu-id="250f6-127">Choose the following image to see the extension in action.</span></span>  

:::image type="complex" source="./media/debugger-for-edge.png" alt-text="Débogueur pour l’extension de code Visual Studio de Microsoft Edge en action" lightbox="./media/debugger-for-edge.gif":::
   <span data-ttu-id="250f6-129">**Débogueur pour Microsoft Edge** Extension de code Visual Studio en action</span><span class="sxs-lookup"><span data-stu-id="250f6-129">**Debugger for Microsoft Edge** Visual Studio Code extension in action</span></span>  
:::image-end:::  

## <span data-ttu-id="250f6-130">Microsoft Edge Tools pour le code Visual Studio</span><span class="sxs-lookup"><span data-stu-id="250f6-130">Microsoft Edge Tools for Visual Studio Code</span></span>

<span data-ttu-id="250f6-131">Avec l’extension de code Visual Studio [Microsoft Edge Tools pour Visual Studio][VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode] , utilisez l’outil **éléments** du navigateur Microsoft Edge dans le code Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="250f6-131">With the [Microsoft Edge Tools for Visual Studio Code][VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode] Visual Studio Code extension, use the **Elements** tool of the Microsoft Edge browser within Visual Studio Code.</span></span>  <span data-ttu-id="250f6-132">Utilisez-le pour les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="250f6-132">Use it for the following actions.</span></span>  

*   <span data-ttu-id="250f6-133">Joignez-vous à une instance ou lancez une instance de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="250f6-133">Attach to an instance or launch an instance of Microsoft Edge.</span></span>  
*   <span data-ttu-id="250f6-134">Affichez la structure HTML Runtime.</span><span class="sxs-lookup"><span data-stu-id="250f6-134">Display the runtime HTML structure.</span></span>  
*   <span data-ttu-id="250f6-135">Mettez à jour la mise en page.</span><span class="sxs-lookup"><span data-stu-id="250f6-135">Update the layout.</span></span>  
*   <span data-ttu-id="250f6-136">Résoudre les problèmes de stylisation.</span><span class="sxs-lookup"><span data-stu-id="250f6-136">Fix styling issues.</span></span>  
    
<span data-ttu-id="250f6-137">Pour plus d’informations, accédez à [outils Microsoft Edge pour l’extension de code Visual][VisualStudioCodeMicrosoftEdgeDevtoolsExtension]Studio.</span><span class="sxs-lookup"><span data-stu-id="250f6-137">For more information, navigate to [Microsoft Edge Tools for Visual Studio Code Visual Studio Code extension][VisualStudioCodeMicrosoftEdgeDevtoolsExtension].</span></span>  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/microsoft-edge-tools-for-visual-studio-code.png" alt-text="Outils Microsoft Edge pour l’extension de code Visual Studio code Visual Studio en action" lightbox="./media/microsoft-edge-tools-for-visual-studio-code.png":::
   <span data-ttu-id="250f6-139">**Microsoft Edge Tools pour le code Visual Studio** Extension de code Visual Studio en action</span><span class="sxs-lookup"><span data-stu-id="250f6-139">**Microsoft Edge Tools for Visual Studio Code** Visual Studio Code extension in action</span></span>  
:::image-end:::  

## <span data-ttu-id="250f6-140">webhint</span><span class="sxs-lookup"><span data-stu-id="250f6-140">webhint</span></span>  
      
<span data-ttu-id="250f6-141">Utilisez [webhint][WebhintMain], un outil de désutilisation personnalisable pour améliorer les fonctionnalités suivantes de votre site.</span><span class="sxs-lookup"><span data-stu-id="250f6-141">Use [webhint][WebhintMain], a customizable linting tool, to improve the following functionality of your site.</span></span>  

*   <span data-ttu-id="250f6-142">Accessibilité</span><span class="sxs-lookup"><span data-stu-id="250f6-142">Accessibility</span></span>
*   <span data-ttu-id="250f6-143">Niveau de performance</span><span class="sxs-lookup"><span data-stu-id="250f6-143">Performance</span></span>
*   <span data-ttu-id="250f6-144">Compatibilité entre les navigateurs</span><span class="sxs-lookup"><span data-stu-id="250f6-144">Cross-browser compatibility</span></span>
*   <span data-ttu-id="250f6-145">Compatibilité avec Project Web App</span><span class="sxs-lookup"><span data-stu-id="250f6-145">PWA compatibility</span></span>
*   <span data-ttu-id="250f6-146">Sécurité</span><span class="sxs-lookup"><span data-stu-id="250f6-146">Security</span></span>

<span data-ttu-id="250f6-147">Il recherche dans votre code des pratiques de codage et des erreurs courantes.</span><span class="sxs-lookup"><span data-stu-id="250f6-147">It checks your code for coding practices and common errors.</span></span> <span data-ttu-id="250f6-148">Le projet open-source de webhint, développé initialement par l’équipe Microsoft Edge, fait désormais partie de [OpenJS Foundation][OpenjsFoundation].</span><span class="sxs-lookup"><span data-stu-id="250f6-148">The webhint open-source project, initially developed by the Microsoft Edge team, is now part of the [OpenJS Foundation][OpenjsFoundation].</span></span>  <span data-ttu-id="250f6-149">L’équipe Microsoft Edge cesse de contribuer à la communauté et aux développeurs Web de la communauté.</span><span class="sxs-lookup"><span data-stu-id="250f6-149">The Microsoft Edge team continues to contribute to webhint alongside web developers in the community.</span></span>  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/webhint-extension.png" alt-text="Capture d’écran de l’extension de code Visual Studio webhint" lightbox="./media/webhint-extension.png":::
   <span data-ttu-id="250f6-151">Capture d’écran de l’extension de code Visual Studio **webhint**</span><span class="sxs-lookup"><span data-stu-id="250f6-151">Screenshot of **webhint** Visual Studio Code extension</span></span>  
:::image-end:::  
      
<span data-ttu-id="250f6-152">Identifiez et corrigez les problèmes de votre site Web en ajoutant l' [extension webhint pour le code Visual Studio][VisualstudioMarketplaceWebhint].</span><span class="sxs-lookup"><span data-stu-id="250f6-152">Identify and fix problems in your website by adding the [webhint extension for Visual Studio Code][VisualstudioMarketplaceWebhint].</span></span>  <span data-ttu-id="250f6-153">Conseils examinez HTML, CSS, JavaScript, écrire, etc.</span><span class="sxs-lookup"><span data-stu-id="250f6-153">Hints examine HTML, CSS, JavaScript, TypeScript, and more.</span></span>  <span data-ttu-id="250f6-154">Les indications apparaissent sous forme de soulignements inline et sont synthétisées dans le volet **problèmes** .</span><span class="sxs-lookup"><span data-stu-id="250f6-154">Hints appear as inline underlines and are summarized in the **Problems** pane.</span></span>  
      
<span data-ttu-id="250f6-155">Pour plus d’informations, accédez à [l’utilisation de webhint dans le code Visual Studio][VisualStudioCodeWebhint].</span><span class="sxs-lookup"><span data-stu-id="250f6-155">For more information, navigate to [How to use webhint in Visual Studio Code][VisualStudioCodeWebhint].</span></span>  

<!--links -->  

[VisualStudioCodeDebuggerEdge]: ./debugger-for-edge.md "Débogueur de l’extension de code Visual Studio Microsoft Edge | Documents Microsoft"  
[VisualStudioCodeMicrosoftEdgeDevtoolsExtension]: ./microsoft-edge-devtools-extension.md "Extension de code Microsoft Edge DevTools pour Visual Studio | Documents Microsoft"  
[VisualStudioCodeWebhint]: ./webhint.md "Extension de code Visual Studio webhint | Documents Microsoft"  

[VisualstudioCode]: https://code.visualstudio.com "Code Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentation | Code Visual Studio"   

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Débogueur pour Microsoft Edge | Visual Studio Marketplace"  
[VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools pour le code Visual Studio | Visual Studio Marketplace"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[WebhintMain]:  https://webhint.io "webhint"  
[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  
