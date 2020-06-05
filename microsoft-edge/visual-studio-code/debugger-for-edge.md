---
description: Comment déboguer Microsoft Edge (chrome) et Microsoft Edge (EdgeHTML) du code VS
title: Déboguer Microsoft Edge (chrome) à partir du code VS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, code vs, code Visual Studio, débogueur
ms.openlocfilehash: 58bcbc927505f4c5a1f493349c3e9475cb75e1be
ms.sourcegitcommit: c1b5fdd48d39d874a76c9b8f68309eb1b507fd0b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2020
ms.locfileid: "10695865"
---
# <span data-ttu-id="a4172-104">Débogueur pour l’extension de code Microsoft Edge VS</span><span class="sxs-lookup"><span data-stu-id="a4172-104">Debugger For Microsoft Edge VS Code Extension</span></span>  

<span data-ttu-id="a4172-105">Avec le [débogueur pour l’extension de code Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] vs, déboguez votre ligne de code JavaScript frontal par ligne et consultez les `console.log()` instructions directement à partir du [code Visual Studio][VisualstudioCode]!</span><span class="sxs-lookup"><span data-stu-id="a4172-105">With the [Debugger for Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] VS Code extension, debug your front-end JavaScript code line by line and see `console.log()` statements directly from [Visual Studio Code][VisualstudioCode]!</span></span>  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Débogueur pour l’extension de code Edge VS au bureau":::
   <span data-ttu-id="a4172-107">Débogueur pour l’extension de code Edge VS au bureau</span><span class="sxs-lookup"><span data-stu-id="a4172-107">Debugger for Edge VS Code extension at work</span></span>  
:::image-end:::

<!--![Debugger for Edge VS Code extension at work][ImageGifDebuggerEdge]  -->  

## <span data-ttu-id="a4172-108">Lancement de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a4172-108">Launching Microsoft Edge</span></span>  

<span data-ttu-id="a4172-109">Accédez à la vue de débogage \ ( `Ctrl` + `Shift` + `D` sous Windows ou `Command` + `Shift` + `D` Mac \) dans la **barre d’activité**.</span><span class="sxs-lookup"><span data-stu-id="a4172-109">Navigate to the Debug view \(`Ctrl`+`Shift`+`D` on Windows or `Command`+`Shift`+`D` on macOS\) in the **Activity Bar**.</span></span>  <span data-ttu-id="a4172-110">Si vous n’avez pas de configurations dans le code VS, appuyez `F5` sur Windows ou MacOS ou sélectionnez le bouton de **lecture** de couleur verte.</span><span class="sxs-lookup"><span data-stu-id="a4172-110">If you do not have any configurations in VS Code, press `F5` on Windows or macOS or select the green **Play** button.</span></span>  <span data-ttu-id="a4172-111">Dans la liste déroulante, sélectionnez **Edge** .</span><span class="sxs-lookup"><span data-stu-id="a4172-111">Select **Edge** in the dropdown.</span></span>  <span data-ttu-id="a4172-112">Vous devez voir un `launch.json` fichier avec la configuration suivante.</span><span class="sxs-lookup"><span data-stu-id="a4172-112">You should see a `launch.json` file with the following configuration.</span></span>  

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

<span data-ttu-id="a4172-113">Si vous appuyez `F5` une nouvelle fois sur Windows ou MacOS ou sélectionnez le bouton de **lecture** vert, le code est lancé sur le serveur Microsoft Edge \ (EdgeHTML \) et vous pouvez déboguer n’importe quel projet Web exécuté sur un port `8080` directement à partir du code vs.</span><span class="sxs-lookup"><span data-stu-id="a4172-113">If you press `F5` on Windows or macOS or select the green **Play** button again, VS Code launches Microsoft Edge \(EdgeHTML\) and you are able to debug any web project you have running on port `8080` directly from VS Code!</span></span>  

### <span data-ttu-id="a4172-114">Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="a4172-114">Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="a4172-115">Si vous voulez lancer Microsoft Edge \ (chrome \), la nouvelle version de Microsoft Edge, au lieu de Microsoft Edge \ (EdgeHTML), vous devez simplement ajouter un `version` attribut à votre configuration existante avec la version de Microsoft Edge \ (chrome \) que vous voulez lancer \ ( `dev` , `beta` ou `canary` \).</span><span class="sxs-lookup"><span data-stu-id="a4172-115">If you want to launch Microsoft Edge \(Chromium\), the next version of Microsoft Edge, instead of Microsoft Edge \(EdgeHTML\), simply add a `version` attribute to your existing configuration with the version of Microsoft Edge \(Chromium\) you want to launch \(`dev`, `beta`, or `canary`\).</span></span> <span data-ttu-id="a4172-116">La configuration suivante suivante lance la version Canaries de Microsoft Edge \ (chrome \).</span><span class="sxs-lookup"><span data-stu-id="a4172-116">The following configuration below launches the Canary version of Microsoft Edge \(Chromium\).</span></span>  

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

## <span data-ttu-id="a4172-117">Joindre à Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a4172-117">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="a4172-118">Joignez le code VS à Microsoft Edge \ (chrome \).</span><span class="sxs-lookup"><span data-stu-id="a4172-118">Attach VS Code to Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="a4172-119">À partir de votre terminal, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="a4172-119">From your terminal, run the following command.</span></span>  

```console
start msedge --remote-debugging-port=9222
```  

<span data-ttu-id="a4172-120">Ajoutez la configuration ci-dessous à votre `launch.json` fichier.</span><span class="sxs-lookup"><span data-stu-id="a4172-120">Add the configuration below to your `launch.json` file.</span></span>   

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```  

<span data-ttu-id="a4172-121">S’il s’agit de la configuration, vous pouvez utiliser le code VS pour Microsoft Edge \ (chrome \) et démarrer le débogage.</span><span class="sxs-lookup"><span data-stu-id="a4172-121">If you now run this configuration, VS Code attaches to Microsoft Edge \(Chromium\) and start debugging!</span></span>  

## <span data-ttu-id="a4172-122">Accès aux éléments de l’équipe d’extension du code Microsoft Edge VS</span><span class="sxs-lookup"><span data-stu-id="a4172-122">Getting in touch with the Elements for Microsoft Edge VS Code extension team</span></span>    

<span data-ttu-id="a4172-123">Envoyez vos commentaires en envoyant [un problème][GithubMicrosoftVscodeEdgeDebug2NewIssue] à l’aide de la [GitHub référentiel Samples][GithubMicrosoftVscodeEdgeDebug2] de l’extension.</span><span class="sxs-lookup"><span data-stu-id="a4172-123">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDebug2NewIssue] against in the [GitHub repo][GithubMicrosoftVscodeEdgeDebug2] of the extension.</span></span>  <span data-ttu-id="a4172-124">Incluez le fichier journal de l’adaptateur de débogage, qui est créé pour chaque exécution de l' `%temp%` Annuaire portant le nom `vscode-edge-debug2.txt` .</span><span class="sxs-lookup"><span data-stu-id="a4172-124">Please include the debug adapter log file, which is created for each run in the `%temp%` directory with the name `vscode-edge-debug2.txt`.</span></span>  <span data-ttu-id="a4172-125">Faites glisser ce fichier dans un commentaire de problème pour le télécharger sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="a4172-125">Drag this file into an issue comment to upload it to GitHub.</span></span>  

<span data-ttu-id="a4172-126">Pour vous aider à améliorer les éléments de l’extension du code Microsoft Edge et celle du code, vos contributions sont les bienvenues.</span><span class="sxs-lookup"><span data-stu-id="a4172-126">To help make the Elements for Microsoft Edge VS Code extension better, your contributions are welcome!</span></span>  <span data-ttu-id="a4172-127">Trouvez tout ce dont vous avez besoin pour commencer à utiliser [GitHub référentiel Samples][GithubMicrosoftVscodeEdgeDebug2] de l’extension.</span><span class="sxs-lookup"><span data-stu-id="a4172-127">Find everything you need to get started in [GitHub repo][GithubMicrosoftVscodeEdgeDebug2] of the extension.</span></span>  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge VS Code extension in action"  -->  
[ImagePngDebuggerEdge]:./Media/Debugger-for-Edge.png "débogueur pour l’extension de code Edge et VS en action"  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Code Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentation | Code Visual Studio"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "Microsoft/vscode-Edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Nouveau problème-Microsoft/vscode-Edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Débogueur pour Microsoft Edge | Visual Studio Marketplace"  
