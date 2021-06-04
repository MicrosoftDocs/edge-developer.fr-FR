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
# Vue d’ensemble du Visual Studio Code  

[Visual Studio Code][VisualStudioCodeDocs] est un éditeur de code source léger mais puissant.  [Visual Studio Code][VisualStudioCodeDocs] est disponible pour Windows, Linux et macOS.  Il inclut la prise en charge intégrée de JavaScript, TypeScript et Node.js, c’est donc un excellent outil pour les développeurs web avant de le personnaliser.  Si vous ne l’utilisez pas encore, [téléchargez Visual Studio Code][VisualstudioCode].  

##  <a name="extensions"></a>Extensions  

<!--todo: We want to put something like the tiles for extensions Visual Studio Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page.  I think it's a web page.  I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->  

Pour acquérir l’une des extensions mises en évidence ci-dessous, accédez à Extensions \(sélectionnez sur Windows/Linux ou sur `Ctrl` + `Shift` + `X` `Command` + `Shift` + `X` macOS\) dans Visual Studio Code.  

Recherchez l’extension spécifique sur Marketplace et choisissez **Installer.**  

:::image type="complex" source="./media/vscode-debugger-install.png" alt-text="Installer le débogger pour l Microsoft Edge Visual Studio Code extension" lightbox="./media/vscode-debugger-install.png":::
   Installer le **débogger pour l Microsoft Edge** Visual Studio Code extension  
:::image-end:::  

:::row:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png" alt-text="Débogger pour l Microsoft Edge Visual Studio Code extension" lightbox="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png":::
         **Débogger pour l Microsoft Edge** Visual Studio Code extension  
      :::image-end:::  
      [Débogger pour Microsoft Edge](#debugger-for-microsoft-edge)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png" alt-text="Microsoft Edge Outils pour l Visual Studio Code Visual Studio Code extension" lightbox="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png":::
         **Microsoft Edge outils pour l Visual Studio Code** Visual Studio Code extension  
      :::image-end:::  
      [Microsoft Edge Outils pour Visual Studio Code](#microsoft-edge-tools-for-visual-studio-code)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-webhint.msft.png" alt-text="extension de Visual Studio Code webhint" lightbox="./media/visual-studio-code-extension-webhint.msft.png":::
         **extension de Visual Studio Code webhint**  
      :::image-end:::  
      [webhint](#webhint)  
   :::column-end:::
:::row-end:::  

##  <a name="debugger-for-microsoft-edge"></a>Débogger pour Microsoft Edge  

Avec l’extension [Déboguer pour Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Code, déboguer votre code JavaScript frontal ligne par ligne et voir les instructions directement à partir `console.log()` [Visual Studio Code][VisualstudioCode].  
      
À l’aide de l’outil Débogger, vous pouvez lancer ou attacher les deux Microsoft Edge \(EdgeHTML\) et Microsoft Edge \(Chromium\).  Pour une walkthrough de débogage de Microsoft Edge à partir de Visual Studio Code et d’exemples de configurations, accédez à `launch.json` [Déboguer][VisualStudioCodeDebuggerEdge]pour Microsoft Edge Visual Studio Code extension .  Choisissez l’image suivante pour voir l’extension en action.  

:::image type="complex" source="./media/debugger-for-edge.png" alt-text="Débogger pour l’extension Visual Studio Code Edge en action" lightbox="./media/debugger-for-edge.gif":::
   **Débogger pour l Microsoft Edge** Visual Studio Code extension en action  
:::image-end:::  

##  <a name="microsoft-edge-tools-for-visual-studio-code"></a>Microsoft Edge Outils pour Visual Studio Code

Avec [l’extension Microsoft Edge Outils][VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode] Visual Studio Code Visual Studio Code, utilisez l’outil **Éléments** du navigateur Microsoft Edge dans Visual Studio Code.  Utilisez-le pour les actions suivantes.  

*   Attacher à une instance ou lancer une instance de Microsoft Edge.  
*   Afficher la structure HTML d’runtime.  
*   Mettez à jour la disposition.  
*   Résoudre les problèmes de style.  
    
Pour plus d’informations, [accédez à Microsoft Edge Outils pour Visual Studio Code Visual Studio Code extension .][VisualStudioCodeMicrosoftEdgeDevtoolsExtension]  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/microsoft-edge-tools-for-visual-studio-code.png" alt-text="Microsoft Edge Outils pour Visual Studio Code Visual Studio Code extension en action" lightbox="./media/microsoft-edge-tools-for-visual-studio-code.png":::
   **Microsoft Edge outils pour Visual Studio Code** Visual Studio Code extension en action  
:::image-end:::  

##  <a name="webhint--"></a>webhint  
      
Utilisez [webhint,][WebhintMain]un outil de linting personnalisable, pour améliorer les fonctionnalités suivantes de votre site.  

*   Accessibilité
*   Performances
*   Compatibilité entre navigateurs
*   PWA compatibilité
*   Sécurité

Il vérifie les pratiques de codage et les erreurs courantes dans votre code. Le projet open source webhint, initialement développé par l’équipe Microsoft Edge, fait désormais partie [d’OpenJS Foundation.][OpenjsFoundation]  L Microsoft Edge de recherche continue de contribuer à lahint web aux côtés des développeurs web de la communauté.  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/webhint-extension.png" alt-text="Capture d’écran de l’extension Visual Studio Code webhint" lightbox="./media/webhint-extension.png":::
   Capture d’écran de l’extension Visual Studio Code **webhint**  
:::image-end:::  
      
Identifiez et corrigez les problèmes dans votre site web en ajoutant [l’extension dehint web pour Visual Studio Code][VisualstudioMarketplaceWebhint].  Les conseils examinent le code HTML, CSS, JavaScript, TypeScript, etc.  Les conseils apparaissent comme des soulignements inline et sont résumés **dans** le volet Problèmes.  
      
Pour plus d’informations, accédez [à Comment utiliser lahint web dans Visual Studio Code][VisualStudioCodeWebhint].  

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
