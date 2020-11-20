---
description: Comment déboguer Microsoft Edge (chrome) et Microsoft Edge (EdgeHTML) du code VS
title: Déboguer Microsoft Edge (chrome) à partir du code VS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, code vs, code Visual Studio, débogueur
ms.openlocfilehash: d9f33a17db7083a6a7cbb013dbf9886755f92c5e
ms.sourcegitcommit: 56cb5821d1b8e96f55bfa14a4ce87a3845b009c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182300"
---
# Débogueur pour l’extension de code Microsoft Edge VS  

Avec le [débogueur pour l’extension de code Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] vs, déboguez votre ligne de code JavaScript frontal par ligne et consultez les `console.log()` instructions directement à partir du [code Visual Studio][VisualstudioCode]!  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Débogueur pour l’extension de code Edge VS au bureau":::
   Débogueur pour l’extension de code Edge VS au bureau  
:::image-end:::

<!--![Debugger for Edge VS Code extension at work][ImageGifDebuggerEdge]  -->  

## Lancement de Microsoft Edge  

Accédez à la vue de débogage \ ( `Ctrl` + `Shift` + `D` sous Windows ou `Command` + `Shift` + `D` Mac \) dans la **barre d’activité**.  Si vous n’avez pas de configurations dans le code VS, appuyez `F5` sur Windows ou MacOS ou sélectionnez le bouton de **lecture** de couleur verte.  Dans la liste déroulante, sélectionnez **Edge** .  Vous devez voir un `launch.json` fichier avec la configuration suivante.  

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

Si vous appuyez `F5` une nouvelle fois sur Windows ou MacOS ou sélectionnez le bouton de **lecture** vert, le code est lancé sur le serveur Microsoft Edge \ (EdgeHTML \) et vous pouvez déboguer n’importe quel projet Web exécuté sur un port `8080` directement à partir du code vs.  

### Microsoft Edge (Chromium)  

Si vous voulez lancer Microsoft Edge \ (chrome \), la nouvelle version de Microsoft Edge, au lieu de Microsoft Edge \ (EdgeHTML \), il vous suffit d’ajouter un `version` attribut à votre configuration existante avec la version de Microsoft Edge \ (chrome \) que vous voulez lancer \ ( `stable` , `dev` , `beta` ou `canary` \). La configuration suivante suivante lance la version Canaries de Microsoft Edge \ (chrome \).  

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

Joignez le code VS à Microsoft Edge \ (chrome \).  À partir de votre terminal, exécutez la commande suivante.  

```console
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

S’il s’agit de la configuration, vous pouvez utiliser le code VS pour Microsoft Edge \ (chrome \) et démarrer le débogage.  

## Accès aux éléments de l’équipe d’extension du code Microsoft Edge VS    

Envoyez vos commentaires en envoyant [un problème][GithubMicrosoftVscodeEdgeDebug2NewIssue] à l’aide de la [GitHub référentiel Samples][GithubMicrosoftVscodeEdgeDebug2] de l’extension.  Incluez le fichier journal de l’adaptateur de débogage, qui est créé pour chaque exécution de l' `%temp%` Annuaire portant le nom `vscode-edge-debug2.txt` .  Faites glisser ce fichier dans un commentaire de problème pour le télécharger sur GitHub.  

Pour vous aider à améliorer les éléments de l’extension du code Microsoft Edge et celle du code, vos contributions sont les bienvenues.  Trouvez tout ce dont vous avez besoin pour commencer à utiliser [GitHub référentiel Samples][GithubMicrosoftVscodeEdgeDebug2] de l’extension.  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge VS Code extension in action"  -->  
[ImagePngDebuggerEdge]:./Media/debugger-for-edge.png "débogueur pour l’extension du code Edge VS en action"  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Code Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentation | Code Visual Studio"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "Microsoft/vscode-Edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Nouveau problème-Microsoft/vscode-Edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Débogueur pour Microsoft Edge | Visual Studio Marketplace"  
