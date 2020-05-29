---
description: Microsoft Edge (chrome) et code Visual Studio
title: VisualStudioCode
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/12/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, code vs, code Visual Studio, débogueur, webhint
ms.openlocfilehash: 94148864edbd43adbe2dc9f3d0c2fa0c1f7f0b43
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566606"
---
# VisualStudioCode

Le [code Visual Studio](https://code.visualstudio.com/Docs) est un éditeur de code source léger mais puissant qui s’exécute sur votre ordinateur de bureau et est disponible pour Windows, MacOS et Linux. Il s’agit d’une prise en charge intégrée de JavaScript, de connexion et de node. js pour qu’il s’agit d’un excellent outil pour les développeurs Web. Accédez à [cette page](https://code.visualstudio.com/) pour télécharger le code Visual Studio si vous ne l’utilisez pas encore.

## Extensions

<!-- We want to put something like the tiles for extensions VS Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page. I think it's a web page. I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->

Pour acquérir les extensions mises en surbrillance ci-dessous, accédez à extensions ( `Ctrl`  +  `Shift`  +  `X` Windows ou `Command`  +  `Shift`  +  `X` Mac) en code vs.

Recherchez l’extension dans Marketplace Marketplace et sélectionnez **installer**.

![Installation du débogueur pour l’extension de code Microsoft Edge VS](./media/vscode-debugger-install.png)

## Débogueur pour Microsoft Edge

Déboguez votre ligne de code JavaScript frontal par ligne et les `console.log()` instructions d’affichage directement dans le [code Visual Studio](https://code.visualstudio.com/) à l’aide du [débogueur de l’extension de code Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs.

Utilisez le [débogueur pour](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) l’extension de code Microsoft Edge vs pour lancer une extension ou l’attacher à Microsoft Edge (EdgeHTML) et Microsoft Edge (chrome). Consultez [cette page](./debugger-for-edge.md) pour obtenir une procédure pas à pas de débogage de Microsoft Edge à partir de code vs et d’exemples de configurations de **Launch. JSON** .

![Image GIF du débogueur pour l’extension de code Edge et en action](./media/debugger-for-edge.gif)

## Éléments pour Microsoft Edge

En ajoutant les [éléments de l’extension de code Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools) vs, vous pouvez utiliser l’outil éléments du navigateur dans le code Visual Studio. Par le biais d’un lancement ou d’une attachement, l’outil éléments se connecte à une instance de Microsoft Edge, affiche la structure HTML d’exécution et vous permet de modifier la disposition ou de résoudre les problèmes de style.

Pour plus d’informations, consultez [cette page](./elements-for-edge.md).

![Image GIF de tous les éléments de l’extension du code Edge et de l’action.](./media/elements-for-edge.gif)

## Astuce

Utilisez [webhint](https://webhint.io), un outil de débordement personnalisable pour améliorer l’accessibilité, les performances, la compatibilité entre les navigateurs, la compatibilité de Project Web App et la sécurité de votre site. Il recherche les meilleures pratiques et les erreurs courantes dans votre code. Ce projet open-source développé au départ par l’équipe Microsoft Edge, fait désormais partie de [OpenJS Foundation](https://openjsf.org/). L’équipe Microsoft Edge cesse de contribuer à la communauté et aux développeurs Web de la communauté.

![Capture d’écran de l’extension de code webhint VS](./media/webhint-extension.png)

Identifiez et corrigez les problèmes de votre code HTML, de CSS, de JavaScript, de la machine à écrire et bien plus encore en ajoutant l' [extension webhint pour le code vs](https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint). Les indications apparaissent sous forme de soulignements inline et sont synthétisées dans le volet problèmes.

Pour plus d’informations, voir [utilisation de webhint dans le code Visual Studio](./webhint.md).
