---
description: Microsoft Edge (chrome) et code Visual Studio
title: VisualStudioCode
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, code vs, code Visual Studio, débogueur, webhint
ms.openlocfilehash: e178612d9db8ce3223bb5158c4557675d3314e15
ms.sourcegitcommit: c1b5fdd48d39d874a76c9b8f68309eb1b507fd0b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2020
ms.locfileid: "10695878"
---
# VisualStudioCode  

Le [code Visual Studio][VisualStudioCodeDocs] est un éditeur de code source léger, mais puissant qui s’exécute sur votre ordinateur de bureau et est disponible pour Windows, MacOS et Linux.  Ce service est fourni avec une prise en charge intégrée de JavaScript, de connexion et de node. js; il s’agit donc d’un excellent outil pour les développeurs Web.  Si vous ne l’utilisez pas encore, téléchargez le [code Visual Studio][VisualstudioCode].  

## Extensions  

<!--Todo: We want to put something like the tiles for extensions VS Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page.  I think it's a web page.  I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->  

Pour acquérir les extensions mises en surbrillance ci-dessous, accédez à extensions \ ( `Ctrl` + `Shift` + `X` sous Windows ou `Command` + `Shift` + `X` Mac \) en code vs.  

Recherchez l’extension dans Marketplace Marketplace et sélectionnez **installer**.  

:::image type="complex" source="./media/vscode-debugger-install.png" alt-text="Installation du débogueur pour l’extension de code Microsoft Edge VS":::
   Installation du débogueur pour l’extension de code Microsoft Edge VS  
:::image-end:::  

:::row:::
   :::column span="1":::
      ### Débogueur pour Microsoft Edge  

      Avec le [débogueur pour l’extension de code Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] vs, déboguez votre code JavaScript frontal par ligne et consultez les `console.log()` instructions directement à partir du [code Visual Studio][VisualstudioCode]!  
      
      À l’aide de l’outil de débogage, vous pouvez lancer une connexion à Microsoft Edge \ (EdgeHTML \) et à Microsoft Edge \ (chrome \).  Pour obtenir une procédure pas à pas illustrant le débogage de Microsoft Edge à partir du code VS et des exemples de `launch.json` configuration, voir [débogueur pour l’extension de code Microsoft Edge vs][VscodeDebuggerEdge].  Sélectionnez l’image suivante pour afficher l’extension en action.  

      :::image type="content" source="./media/debugger-for-edge.png" alt-text="Débogueur pour l’extension du code Edge VS en action" lightbox="./media/debugger-for-edge.gif":::  
   :::column-end:::
   :::column span="1":::
      ### Éléments pour Microsoft Edge  
      
      À l’aide des éléments de l’extension de code [Microsoft Edge][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] vs, utilisez l’outil éléments du navigateur Microsoft Edge à partir de code Visual Studio.  Par le biais d’un lancement ou d’une attachement, l’outil éléments se connecte à une instance de Microsoft Edge, affiche la structure HTML d’exécution et vous permet de modifier la disposition ou de résoudre les problèmes de style.  
      
      Pour plus d’informations, voir [éléments pour l’extension de code Microsoft Edge vs][VscodeElementsEdge].  Sélectionnez l’image suivante pour afficher l’extension en action.  
      
      :::image type="content" source="./media/elements-for-edge.png" alt-text="Éléments pour l’extension du code Edge et en action" lightbox="./media/elements-for-edge.gif":::  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      ### webhint
      
      Utilisez [webhint][WebhintMain], un outil de débordement personnalisable pour améliorer l’accessibilité, les performances, la compatibilité entre les navigateurs, la compatibilité de Project Web App et la sécurité de votre site.  Il recherche les meilleures pratiques et les erreurs courantes dans votre code. Le projet open-source de webhint, développé initialement par l’équipe Microsoft Edge, fait désormais partie de [OpenJS Foundation][OpenjsFoundation].  L’équipe Microsoft Edge cesse de contribuer à la communauté et aux développeurs Web de la communauté.  <!--Select the following image to see the extension in action.  -->  
      
      :::image type="content" source="./media/webhint-extension.png" alt-text="Capture d’écran de l’extension de code webhint VS" lightbox="./media/webhint-extension.png":::  
      
      Identifiez et corrigez les problèmes de votre code HTML, de CSS, de JavaScript, de la machine à écrire et bien plus encore en ajoutant l' [extension webhint pour le code vs][VisualstudioMarketplaceWebhint].  Les indications apparaissent sous forme de soulignements inline et sont synthétisées dans le volet **problèmes** .  
      
      Pour plus d’informations, voir [utilisation de webhint dans le code Visual Studio][VscodeWebhint].  
   :::column-end:::
   :::column span="1":::
      <!--Empty to retain grid  -->  
   :::column-end:::
:::row-end:::

<!-- image links -->  

<!--links -->  

[VscodeDebuggerEdge]: ./debugger-for-edge.md "Débogueur pour l’extension de code Microsoft Edge VS | Documents Microsoft"  
[VscodeElementsEdge]: ./elements-for-edge.md "Éléments pour l’extension de code Microsoft Edge VS | Documents Microsoft"  
[VscodeWebhint]: ./webhint.md "Extension de code webhint et Documents Microsoft"  

[VisualstudioCode]: https://code.visualstudio.com "Code Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentation | Code Visual Studio"   

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Débogueur pour Microsoft Edge | Visual Studio Marketplace"  
[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Éléments pour Microsoft Edge (chrome) | Visual Studio Marketplace"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[WebhintMain]:  https://webhint.io "Astuce"  
[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  
