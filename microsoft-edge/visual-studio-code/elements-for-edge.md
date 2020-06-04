---
description: Utiliser des éléments pour Microsoft Edge (chrome) à partir du code VS
title: Éléments de Microsoft Edge (chrome) issus du code VS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, code vs, code Visual Studio, éléments
ms.openlocfilehash: ef516d8364c68b550f889bcad0fe762a73ce5f99
ms.sourcegitcommit: 652009c5cea9e75c22b077f0cbcdc0d96bd337ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2020
ms.locfileid: "10694861"
---
# Éléments pour l’extension de code Microsoft Edge VS  

À l’aide des éléments de l’extension de code [Microsoft Edge][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] vs, utilisez l’outil éléments du navigateur Microsoft Edge à partir de [code Visual Studio][VisualstudioCode].  Par le biais d’un lancement ou d’une attachement, l’outil éléments se connecte à une instance de Microsoft Edge, affiche la structure HTML d’exécution et vous permet de modifier la disposition ou de résoudre les problèmes de style.  

:::image type="complex" source="./media/elements-for-edge.gif" alt-text="Éléments pour l’extension latérale et du code au bureau":::
   Éléments pour l’extension latérale et du code au bureau  
:::image-end:::

<!--![Elements for Edge VS Code extension at work][ImageGifElementsEdge]  -->  

## Lancement de Microsoft Edge à partir de l’extension d’éléments  

Accédez aux éléments dans la **barre d’activité**.  À côté de la mention **éléments pour Microsoft Edge: cibles,** il existe un signe plus qui ouvre le navigateur de votre application.  Si vous avez sélectionné l’option **à propos** de, vous devez accéder à votre application Web dans le navigateur pour qu’elle apparaisse dans le panneau éléments du code vs.  

## Lancement de Microsoft Edge à partir de la vue de débogage  

Si vous avez l’habitude d’utiliser le mode débogage dans du code Visual Studio, accédez à des éléments à partir de cet outil.  Accédez à la vue de débogage \ ( `Ctrl` + `Shift` + `D` sous Windows ou `Command` + `Shift` + `D` Mac \).  

Si vous n’avez pas de configurations dans le code VS, appuyez `F5` sur Windows ou MacOS ou sélectionnez le bouton de **lecture** de couleur verte. Dans la liste déroulante, sélectionnez **Edge** . Vous devez voir un `launch.json` fichier avec la configuration suivante.  

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            
            "name": "Launch Microsoft Edge and open the Elements tool",
            "request": "launch",
            "type": "vscode-edge-devtools.debug",
            "url": "http://localhost:3000"
        
        }
    ]
}
```  

À présent que vous avez chargé la configuration appropriée, appuyez `F5` sur Windows ou MacOS ou sélectionnez le bouton de **lecture** vert. L’outil éléments qui vous est familier, sur le navigateur Microsoft Edge, démarre dans le code VS, ce qui vous permet d’accéder à un enregistrement de votre navigateur et d’examiner les composants de votre page.  

## Joindre à Microsoft Edge  

Pour joindre le code VS à une instance de Microsoft Edge \ (chrome \), vous devez démarrer le navigateur en exécutant la commande suivante à partir de votre terminal.  

`start msedge --remote-debugging-port=9222`  

Une fois l’application lancée, ajoutez la configuration ci-dessous à votre fichier **Launch. JSON** :  

```json
{
    "type": "vscode-edge-devtools.debug",
    "request": "attach",
    "name": "Attach to Microsoft Edge and open the Elements tool",
    "url": "http://localhost:3000/",
    "webRoot": "${workspaceFolder}/out",
    "port": 9222
}
```  

Sélectionnez **joindre à Microsoft Edge, puis ouvrez l’outil éléments** à partir du menu déroulant débogueur.  Appuyez ensuite `F5` sur Windows ou MacOS ou sélectionnez le bouton de **lecture** vert.  Le code VS lance l’outil éléments, ce qui vous permet d’accéder à la vidéo de votre navigateur, de vérifier le DOM et de styliser les composants sur votre page.  

## Accès aux éléments de l’équipe d’extension du code Microsoft Edge VS  

Envoyez vos commentaires en envoyant [un problème][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] à l’aide de la [GitHub référentiel Samples][GithubMicrosoftVscodeEdgeDevtools] de l’extension.  

Si vous souhaitez améliorer l’extension du code Microsoft Edge et celle du code, vos contributions sont les bienvenues.  Trouvez tout ce dont vous avez besoin pour commencer à utiliser le [GitHub référentiel Samples][GithubMicrosoftVscodeEdgeDevtools] de l’extension.  

<!-- image links -->  

<!--[ImageGifElementsEdge]: ./media/elements-for-edge.gif "Elements for Edge VS Code extension in action"  -->  
[ImagePngElementsEdge]:./Media/Elements-for-Edge.png "éléments pour l’extension Edge et code en action"  

<!--links -->  

[VscodeElementsEdge]: ./elements-for-edge.md "Éléments pour l’extension de code Microsoft Edge VS | Documents Microsoft"  

[VisualstudioCode]: https://code.visualstudio.com "Code Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentation | Code Visual Studio"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Nouveau problème-Microsoft/vscode-Edge-devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Éléments pour Microsoft Edge (chrome) | Visual Studio Marketplace"  
