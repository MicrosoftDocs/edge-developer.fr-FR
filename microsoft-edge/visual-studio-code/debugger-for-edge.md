---
description: Comment déboguer des Microsoft Edge (Chromium) et des Microsoft Edge (EdgeHTML) à partir de Visual Studio Code
title: Déboguer Microsoft Edge (Chromium) à partir de Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, développement web, outils f12, devtools, vs code, visual studio code, débogueur
ms.openlocfilehash: e36348fc1ef5e30a511e6eda73c7646a85d8717e
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399294"
---
# <a name="debugger-for-microsoft-edge-visual-studio-code-extension"></a>Débogger for Microsoft Edge Visual Studio Code Extension  

Avec [l’extension Déboguer pour Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Code, déboguer votre code JavaScript frontal ligne par ligne et voir les instructions directement à partir Visual Studio Code `console.log()` ! [][VisualstudioCode]  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Débogger pour l’extension Visual Studio Code Edge au travail" lightbox="./media/debugger-for-edge.gif":::
   Débogger pour l’extension Visual Studio Code Edge au travail  
:::image-end:::

<!--![Debugger for Edge Visual Studio Code extension at work][ImageGifDebuggerEdge]  -->  

## <a name="launching-microsoft-edge"></a>Lancement Microsoft Edge  

Accédez à la vue Débogage \( `Ctrl` + `Shift` + `D` sur Windows ou `Command` + `Shift` + `D` sur macOS\) dans la **barre d’activité.**  Si vous n’avez aucune configuration dans Visual Studio Code, sélectionnez Windows ou macOS ou sélectionnez le `F5` bouton **vert Lire.**  Sélectionnez **Edge** dans ladown.  Vous devriez voir un `launch.json` fichier avec la configuration suivante.  

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

Si vous sélectionnez sur Windows ou macOS ou sélectionnez de nouveau le bouton vert Lire, Visual Studio Code lance `F5` Microsoft Edge \(EdgeHTML\) **** et vous pouvez déboguer tout projet web que vous avez en cours d’exécution sur le port directement à partir de `8080` Visual Studio Code !  

### <a name="microsoft-edge-chromium"></a>Microsoft Edge (Chromium)  

Si vous souhaitez lancer Microsoft Edge \(Chromium\), la nouvelle Microsoft Edge, au lieu de Microsoft Edge \(EdgeHTML\), ajoute simplement un attribut à votre configuration existante avec la version de Microsoft Edge \(Chromium\) que vous souhaitez lancer `version` \( `dev` ou `beta` `canary` \).  La configuration suivante lance la version Canary de Microsoft Edge \(Chromium\).  

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

## <a name="attaching-to-microsoft-edge"></a>Attachement à un Microsoft Edge  

Attachez Visual Studio Code Microsoft Edge \(Chromium\).  À partir de votre terminal, exécutez la commande suivante.  

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

Si vous exécutez maintenant cette configuration, Visual Studio Code joint à Microsoft Edge \(Chromium\) et démarrer le débogage.  

## <a name="getting-in-touch-with-the-elements-for-microsoft-edge-visual-studio-code-extension-team"></a>Entrer en contact avec l’équipe d’extension Microsoft Edge Visual Studio Code éléments    

Envoyez vos commentaires en [classant un problème][GithubMicrosoftVscodeEdgeDebug2NewIssue] dans le [GitHub de][GithubMicrosoftVscodeEdgeDebug2] l’extension.  Veuillez inclure le fichier journal de l’adaptateur de débogage, qui est créé pour chaque run dans le `%temp%` répertoire avec le nom `vscode-edge-debug2.txt` .  Faites glisser ce fichier dans un commentaire de problème pour le télécharger vers GitHub.  

Pour améliorer les éléments de l’extension Microsoft Edge Visual Studio Code, vos contributions sont les bienvenues !  Recherchez tout ce dont vous avez besoin pour [commencer GitHub de][GithubMicrosoftVscodeEdgeDebug2] l’extension.  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge Visual Studio Code extension in action"  -->  
[ImagePngDebuggerEdge] : ./media/debugger-for-edge.png « Débogueur pour l’extension Visual Studio Code Edge en action »  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentation | Visual Studio Code"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "microsoft/vscode-edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Nouveau problème : microsoft/vscode-edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Débogueur pour Microsoft Edge | Visual Studio Marketplace"  
