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
# <span data-ttu-id="758d0-104">Débogueur de l’extension de code Visual Studio Visual Studio</span><span class="sxs-lookup"><span data-stu-id="758d0-104">Debugger For Microsoft Edge Visual Studio Code Extension</span></span>  

<span data-ttu-id="758d0-105">Avec le [débogueur de][VisualstudioMarketplaceDebuggerMicrosoftEdge] l’extension de code Visual Studio de Microsoft Edge, déboguez votre ligne de code JavaScript frontal par ligne et consultez les `console.log()` instructions directement à partir du [code Visual Studio][VisualstudioCode]!</span><span class="sxs-lookup"><span data-stu-id="758d0-105">With the [Debugger for Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Code extension, debug your front-end JavaScript code line by line and see `console.log()` statements directly from [Visual Studio Code][VisualstudioCode]!</span></span>  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Débogueur pour l’extension de code Visual Studio de Microsoft Edge au bureau" lightbox="./media/debugger-for-edge.gif":::
   <span data-ttu-id="758d0-107">Débogueur pour l’extension de code Visual Studio de Microsoft Edge au bureau</span><span class="sxs-lookup"><span data-stu-id="758d0-107">Debugger for Edge Visual Studio Code extension at work</span></span>  
:::image-end:::

<!--![Debugger for Edge Visual Studio Code extension at work][ImageGifDebuggerEdge]  -->  

## <span data-ttu-id="758d0-108">Lancement de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="758d0-108">Launching Microsoft Edge</span></span>  

<span data-ttu-id="758d0-109">Accédez à la vue de débogage \ ( `Ctrl` + `Shift` + `D` sous Windows ou `Command` + `Shift` + `D` Mac \) dans la **barre d’activité**.</span><span class="sxs-lookup"><span data-stu-id="758d0-109">Navigate to the Debug view \(`Ctrl`+`Shift`+`D` on Windows or `Command`+`Shift`+`D` on macOS\) in the **Activity Bar**.</span></span>  <span data-ttu-id="758d0-110">Si vous n’avez pas de configurations dans le code Visual Studio, appuyez `F5` sur Windows ou MacOS ou sélectionnez le bouton de **lecture** de couleur verte.</span><span class="sxs-lookup"><span data-stu-id="758d0-110">If you do not have any configurations in Visual Studio Code, press `F5` on Windows or macOS or select the green **Play** button.</span></span>  <span data-ttu-id="758d0-111">Dans la liste déroulante, sélectionnez **Edge** .</span><span class="sxs-lookup"><span data-stu-id="758d0-111">Select **Edge** in the dropdown.</span></span>  <span data-ttu-id="758d0-112">Vous devez voir un `launch.json` fichier avec la configuration suivante.</span><span class="sxs-lookup"><span data-stu-id="758d0-112">You should see a `launch.json` file with the following configuration.</span></span>  

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

<span data-ttu-id="758d0-113">Si vous appuyez `F5` une nouvelle fois sur Windows ou MacOS ou sélectionnez le bouton de **lecture** vert, le code Visual Studio lance Microsoft Edge \ (EdgeHTML \) et vous pouvez déboguer n’importe quel projet Web exécuté sur un port `8080` directement à partir du code Visual Studio!</span><span class="sxs-lookup"><span data-stu-id="758d0-113">If you press `F5` on Windows or macOS or select the green **Play** button again, Visual Studio Code launches Microsoft Edge \(EdgeHTML\) and you are able to debug any web project you have running on port `8080` directly from Visual Studio Code!</span></span>  

### <span data-ttu-id="758d0-114">Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="758d0-114">Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="758d0-115">Si vous voulez lancer Microsoft Edge \ (chrome \), le nouveau Microsoft Edge, au lieu de Microsoft Edge \ (EdgeHTML \), ajoutez simplement un `version` attribut à votre configuration existante avec la version de Microsoft Edge \ (chrome \) que vous voulez lancer \ ( `dev` , `beta` ou `canary` \).</span><span class="sxs-lookup"><span data-stu-id="758d0-115">If you want to launch Microsoft Edge \(Chromium\), the new Microsoft Edge, instead of Microsoft Edge \(EdgeHTML\), simply add a `version` attribute to your existing configuration with the version of Microsoft Edge \(Chromium\) you want to launch \(`dev`, `beta`, or `canary`\).</span></span>  <span data-ttu-id="758d0-116">La configuration suivante suivante lance la version Canaries de Microsoft Edge \ (chrome \).</span><span class="sxs-lookup"><span data-stu-id="758d0-116">The following configuration below launches the Canary version of Microsoft Edge \(Chromium\).</span></span>  

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

## <span data-ttu-id="758d0-117">Joindre à Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="758d0-117">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="758d0-118">Associez le code Visual Studio à Microsoft Edge \ (chrome \).</span><span class="sxs-lookup"><span data-stu-id="758d0-118">Attach Visual Studio Code to Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="758d0-119">À partir de votre terminal, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="758d0-119">From your terminal, run the following command.</span></span>  

```shell
start msedge --remote-debugging-port=9222
```  

<span data-ttu-id="758d0-120">Ajoutez la configuration ci-dessous à votre `launch.json` fichier.</span><span class="sxs-lookup"><span data-stu-id="758d0-120">Add the configuration below to your `launch.json` file.</span></span>   

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```  

<span data-ttu-id="758d0-121">Si vous exécutez désormais cette configuration, le code Visual Studio est attaché à Microsoft Edge \ (chrome \) et démarre le débogage.</span><span class="sxs-lookup"><span data-stu-id="758d0-121">If you now run this configuration, Visual Studio Code attaches to Microsoft Edge \(Chromium\) and start debugging.</span></span>  

## <span data-ttu-id="758d0-122">En savoir plus sur les éléments de l’équipe extension de code Visual Studio de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="758d0-122">Getting in touch with the Elements for Microsoft Edge Visual Studio Code extension team</span></span>    

<span data-ttu-id="758d0-123">Envoyez vos commentaires en envoyant [un problème][GithubMicrosoftVscodeEdgeDebug2NewIssue] à l’aide de la [GitHub référentiel Samples][GithubMicrosoftVscodeEdgeDebug2] de l’extension.</span><span class="sxs-lookup"><span data-stu-id="758d0-123">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDebug2NewIssue] against in the [GitHub repo][GithubMicrosoftVscodeEdgeDebug2] of the extension.</span></span>  <span data-ttu-id="758d0-124">Incluez le fichier journal de l’adaptateur de débogage, qui est créé pour chaque exécution de l' `%temp%` Annuaire portant le nom `vscode-edge-debug2.txt` .</span><span class="sxs-lookup"><span data-stu-id="758d0-124">Please include the debug adapter log file, which is created for each run in the `%temp%` directory with the name `vscode-edge-debug2.txt`.</span></span>  <span data-ttu-id="758d0-125">Faites glisser ce fichier dans un commentaire de problème pour le télécharger sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="758d0-125">Drag this file into an issue comment to upload it to GitHub.</span></span>  

<span data-ttu-id="758d0-126">Pour vous aider à améliorer les éléments de l’extension de code Visual Studio Visual Studio, vos contributions sont les bienvenues.</span><span class="sxs-lookup"><span data-stu-id="758d0-126">To help make the Elements for Microsoft Edge Visual Studio Code extension better, your contributions are welcome!</span></span>  <span data-ttu-id="758d0-127">Trouvez tout ce dont vous avez besoin pour commencer à utiliser [GitHub référentiel Samples][GithubMicrosoftVscodeEdgeDebug2] de l’extension.</span><span class="sxs-lookup"><span data-stu-id="758d0-127">Find everything you need to get started in [GitHub repo][GithubMicrosoftVscodeEdgeDebug2] of the extension.</span></span>  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge Visual Studio Code extension in action"  -->  
[ImagePngDebuggerEdge]:./Media/debugger-for-edge.png "Debugger pour l’extension de code Visual Studio en action"  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Code Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentation | Code Visual Studio"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "Microsoft/vscode-Edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Nouveau problème-Microsoft/vscode-Edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Débogueur pour Microsoft Edge | Visual Studio Marketplace"  
