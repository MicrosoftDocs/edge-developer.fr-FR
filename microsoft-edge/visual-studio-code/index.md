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
# Présentation du code Visual Studio  

Le [code Visual Studio][VisualStudioCodeDocs] est un éditeur de code source léger, mais puissant.  Le [code Visual Studio][VisualStudioCodeDocs] est disponible pour Windows, Linux et MacOS.  Il inclut une prise en charge intégrée pour JavaScript, la machine à écrire et Node.js, donc c’est un excellent outil pour les développeurs Web avant de le personnaliser.  Si vous ne l’utilisez pas encore, téléchargez le [code Visual Studio][VisualstudioCode].  

## Extensions  

<!--todo: We want to put something like the tiles for extensions Visual Studio Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page.  I think it's a web page.  I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->  

Pour acquérir les extensions mises en surbrillance ci-dessous, accédez à extensions \(sélectionnez `Ctrl` + `Shift` + `X` sur Windows/Linux ou `Command` + `Shift` + `X` Mac \) dans le code Visual Studio.  

Recherchez l’extension dans Marketplace et sélectionnez **installer**.  

:::image type="complex" source="./media/vscode-debugger-install.png" alt-text="Installer le débogueur pour l’extension de code Visual Studio Visual Studio" lightbox="./media/vscode-debugger-install.png":::
   Installer le **débogueur pour** l’extension de code Visual Studio Visual Studio  
:::image-end:::  

:::row:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png" alt-text="Débogueur de l’extension de code Visual Studio Visual Studio" lightbox="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png":::
         **Débogueur pour Microsoft Edge** Extension de code Visual Studio  
      :::image-end:::  
      [Débogueur pour Microsoft Edge](#debugger-for-microsoft-edge)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png" alt-text="Extensions de code Visual Studio Microsoft Edge Tools pour Visual Studio" lightbox="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png":::
         **Microsoft Edge Tools pour le code Visual Studio** Extension de code Visual Studio  
      :::image-end:::  
      [Microsoft Edge Tools pour le code Visual Studio](#microsoft-edge-tools-for-visual-studio-code)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-webhint.msft.png" alt-text="extension de code Visual Studio webhint" lightbox="./media/visual-studio-code-extension-webhint.msft.png":::
         **Astuce** Extension de code Visual Studio  
      :::image-end:::  
      [webhint](#webhint)  
   :::column-end:::
:::row-end:::  

## Débogueur pour Microsoft Edge  

Avec le [débogueur de][VisualstudioMarketplaceDebuggerMicrosoftEdge] l’extension de code Visual Studio Microsoft Edge, déboguez votre code JavaScript frontal par ligne et consultez les `console.log()` instructions directement à partir du [code Visual Studio][VisualstudioCode].  
      
À l’aide de l’outil de débogage, vous pouvez lancer une connexion à Microsoft Edge \(EdgeHTML \) et à Microsoft Edge \(chrome \).  Pour obtenir une procédure pas à pas de débogage de Microsoft Edge à partir de l’exemple de code et de configurations Visual Studio `launch.json` , accédez à [débogueur pour l’extension de code Visual Studio Visual Studio][VisualStudioCodeDebuggerEdge].  Cliquez sur l’image suivante pour afficher l’extension en action.  

:::image type="complex" source="./media/debugger-for-edge.png" alt-text="Débogueur pour l’extension de code Visual Studio de Microsoft Edge en action" lightbox="./media/debugger-for-edge.gif":::
   **Débogueur pour Microsoft Edge** Extension de code Visual Studio en action  
:::image-end:::  

## Microsoft Edge Tools pour le code Visual Studio

Avec l’extension de code Visual Studio [Microsoft Edge Tools pour Visual Studio][VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode] , utilisez l’outil **éléments** du navigateur Microsoft Edge dans le code Visual Studio.  Utilisez-le pour les actions suivantes.  

*   Joignez-vous à une instance ou lancez une instance de Microsoft Edge.  
*   Affichez la structure HTML Runtime.  
*   Mettez à jour la mise en page.  
*   Résoudre les problèmes de stylisation.  
    
Pour plus d’informations, accédez à [outils Microsoft Edge pour l’extension de code Visual][VisualStudioCodeMicrosoftEdgeDevtoolsExtension]Studio.  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/microsoft-edge-tools-for-visual-studio-code.png" alt-text="Outils Microsoft Edge pour l’extension de code Visual Studio code Visual Studio en action" lightbox="./media/microsoft-edge-tools-for-visual-studio-code.png":::
   **Microsoft Edge Tools pour le code Visual Studio** Extension de code Visual Studio en action  
:::image-end:::  

## webhint  
      
Utilisez [webhint][WebhintMain], un outil de désutilisation personnalisable pour améliorer les fonctionnalités suivantes de votre site.  

*   Accessibilité
*   Niveau de performance
*   Compatibilité entre les navigateurs
*   Compatibilité avec Project Web App
*   Sécurité

Il recherche dans votre code des pratiques de codage et des erreurs courantes. Le projet open-source de webhint, développé initialement par l’équipe Microsoft Edge, fait désormais partie de [OpenJS Foundation][OpenjsFoundation].  L’équipe Microsoft Edge cesse de contribuer à la communauté et aux développeurs Web de la communauté.  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/webhint-extension.png" alt-text="Capture d’écran de l’extension de code Visual Studio webhint" lightbox="./media/webhint-extension.png":::
   Capture d’écran de l’extension de code Visual Studio **webhint**  
:::image-end:::  
      
Identifiez et corrigez les problèmes de votre site Web en ajoutant l' [extension webhint pour le code Visual Studio][VisualstudioMarketplaceWebhint].  Conseils examinez HTML, CSS, JavaScript, écrire, etc.  Les indications apparaissent sous forme de soulignements inline et sont synthétisées dans le volet **problèmes** .  
      
Pour plus d’informations, accédez à [l’utilisation de webhint dans le code Visual Studio][VisualStudioCodeWebhint].  

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
