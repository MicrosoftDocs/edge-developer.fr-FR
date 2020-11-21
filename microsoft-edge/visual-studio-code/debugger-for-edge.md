---
description: Comment déboguer Microsoft Edge (chrome) et Microsoft Edge (EdgeHTML) à partir du code Visual Studio
title: Déboguer Microsoft Edge (chrome) à partir du code Visual Studio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, code vs, code Visual Studio, débogueur
ms.openlocfilehash: df15b76cc26ad01d3b8508362aa4b86998f8b41b
ms.sourcegitcommit: acf8ad7cb6c8ecf83a6170f8eeb9bec32878f8ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182504"
---
# Débogueur de l’extension de code Visual Studio Visual Studio  

Avec le [débogueur de][VisualstudioMarketplaceDebuggerMicrosoftEdge] l’extension de code Visual Studio de Microsoft Edge, déboguez votre ligne de code JavaScript frontal par ligne et consultez les `console.log()` instructions directement à partir du [code Visual Studio][VisualstudioCode]!  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Débogueur pour l’extension de code Visual Studio de Microsoft Edge au bureau" lightbox="./media/debugger-for-edge.gif":::
   Débogueur pour l’extension de code Visual Studio de Microsoft Edge au bureau  
:::image-end:::

<!--![Debugger for Edge Visual Studio Code extension at work][ImageGifDebuggerEdge]  -->  

## Lancement de Microsoft Edge  

Accédez à la vue de débogage \ ( `Ctrl` + `Shift` + `D` sous Windows ou `Command` + `Shift` + `D` Mac \) dans la **barre d’activité**.  Si vous n’avez pas de configurations dans le code Visual Studio, appuyez `F5` sur Windows ou MacOS ou sélectionnez le bouton de **lecture** de couleur verte.  Dans la liste déroulante, sélectionnez **Edge** .  Vous devez voir un `launch.json` fichier avec la configuration suivante.  

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "type": "edge",
            "request": "launch",
            "name": "Launch Edge against localhost",
            "url": "http://localhost:8080",
            "webRoot": "${workspaceFolder}"
        }
    ]
}
```  

Si vous appuyez `F5` une nouvelle fois sur Windows ou MacOS ou sélectionnez le bouton de **lecture** vert, le code Visual Studio lance Microsoft Edge \ (EdgeHTML \) et vous pouvez déboguer n’importe quel projet Web exécuté sur un port `8080` directement à partir du code Visual Studio!  

### Microsoft Edge (Chromium)  

Si vous voulez lancer Microsoft Edge \ (chrome \), le nouveau Microsoft Edge, au lieu de Microsoft Edge \ (EdgeHTML \), ajoutez simplement un `version` attribut à votre configuration existante avec la version de Microsoft Edge \ (chrome \) que vous voulez lancer \ ( `dev` , `beta` ou `canary` \).  La configuration suivante suivante lance la version Canaries de Microsoft Edge \ (chrome \).  

```json
{
    "type": "edge",
    "request": "launch",
    "version": "canary",
    "name": "Launch Edge against localhost",
    "url": "http://localhost:8080",
    "webRoot": "${workspaceFolder}"
}
```  

## Joindre à Microsoft Edge  

Associez le code Visual Studio à Microsoft Edge \ (chrome \).  À partir de votre terminal, exécutez la commande suivante.  

```shell
start msedge --remote-debugging-port=9222
```  

Ajoutez la configuration ci-dessous à votre `launch.json` fichier.   

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```  

Si vous exécutez désormais cette configuration, le code Visual Studio est attaché à Microsoft Edge \ (chrome \) et démarre le débogage.  

## En savoir plus sur les éléments de l’équipe extension de code Visual Studio de Microsoft Edge    

Envoyez vos commentaires en envoyant [un problème][GithubMicrosoftVscodeEdgeDebug2NewIssue] à l’aide de la [GitHub référentiel Samples][GithubMicrosoftVscodeEdgeDebug2] de l’extension.  Incluez le fichier journal de l’adaptateur de débogage, qui est créé pour chaque exécution de l' `%temp%` Annuaire portant le nom `vscode-edge-debug2.txt` .  Faites glisser ce fichier dans un commentaire de problème pour le télécharger sur GitHub.  

Pour vous aider à améliorer les éléments de l’extension de code Visual Studio Visual Studio, vos contributions sont les bienvenues.  Trouvez tout ce dont vous avez besoin pour commencer à utiliser [GitHub référentiel Samples][GithubMicrosoftVscodeEdgeDebug2] de l’extension.  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge Visual Studio Code extension in action"  -->  
[ImagePngDebuggerEdge]:./Media/debugger-for-edge.png "Debugger pour l’extension de code Visual Studio en action"  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Code Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentation | Code Visual Studio"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "Microsoft/vscode-Edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Nouveau problème-Microsoft/vscode-Edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Débogueur pour Microsoft Edge | Visual Studio Marketplace"  
