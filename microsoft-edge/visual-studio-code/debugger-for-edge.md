---
description: Comment déboguer Microsoft Edge (Chromium) et Microsoft Edge (EdgeHTML) à partir de Visual Studio Code
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
# <a name="debugger-for-microsoft-edge-visual-studio-code-extension"></a><span data-ttu-id="7ba8f-104">Débogger pour l’extension de code Visual Studio Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7ba8f-104">Debugger For Microsoft Edge Visual Studio Code Extension</span></span>  

<span data-ttu-id="7ba8f-105">Avec l’extension [Debugger][VisualstudioMarketplaceDebuggerMicrosoftEdge] pour Microsoft Edge Visual Studio Code, déboguer votre code JavaScript frontal ligne par ligne et voir les instructions directement à partir Visual Studio `console.log()` [Code][VisualstudioCode]!</span><span class="sxs-lookup"><span data-stu-id="7ba8f-105">With the [Debugger for Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Code extension, debug your front-end JavaScript code line by line and see `console.log()` statements directly from [Visual Studio Code][VisualstudioCode]!</span></span>  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Débogger pour l’extension Visual Studio Edge au travail" lightbox="./media/debugger-for-edge.gif":::
   <span data-ttu-id="7ba8f-107">Débogger pour l’extension de code Visual Studio Edge au travail</span><span class="sxs-lookup"><span data-stu-id="7ba8f-107">Debugger for Edge Visual Studio Code extension at work</span></span>  
:::image-end:::

<!--![Debugger for Edge Visual Studio Code extension at work][ImageGifDebuggerEdge]  -->  

## <a name="launching-microsoft-edge"></a><span data-ttu-id="7ba8f-108">Lancement de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7ba8f-108">Launching Microsoft Edge</span></span>  

<span data-ttu-id="7ba8f-109">Accédez à la vue Débogage \( `Ctrl` + `Shift` + `D` sur Windows ou `Command` + `Shift` + `D` sur macOS\) dans la barre **d’activité.**</span><span class="sxs-lookup"><span data-stu-id="7ba8f-109">Navigate to the Debug view \(`Ctrl`+`Shift`+`D` on Windows or `Command`+`Shift`+`D` on macOS\) in the **Activity Bar**.</span></span>  <span data-ttu-id="7ba8f-110">Si vous n’avez aucune configuration dans Visual Studio Code, sélectionnez Sur Windows ou macOS ou sélectionnez le `F5` bouton **vert Lire.**</span><span class="sxs-lookup"><span data-stu-id="7ba8f-110">If you do not have any configurations in Visual Studio Code, select `F5` on Windows or macOS or select the green **Play** button.</span></span>  <span data-ttu-id="7ba8f-111">Sélectionnez **Edge** dans ladown.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-111">Select **Edge** in the dropdown.</span></span>  <span data-ttu-id="7ba8f-112">Vous devriez voir un `launch.json` fichier avec la configuration suivante.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-112">You should see a `launch.json` file with the following configuration.</span></span>  

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

<span data-ttu-id="7ba8f-113">Si vous sélectionnez sur Windows ou macOS ou sélectionnez de nouveau le bouton vert Lire, Visual Studio Code lance `F5` Microsoft Edge \(EdgeHTML\) et vous pouvez déboguer tout projet web que vous avez en cours d’exécution sur le port directement à partir de Visual Studio  Code `8080` !</span><span class="sxs-lookup"><span data-stu-id="7ba8f-113">If you select `F5` on Windows or macOS or select the green **Play** button again, Visual Studio Code launches Microsoft Edge \(EdgeHTML\) and you are able to debug any web project you have running on port `8080` directly from Visual Studio Code!</span></span>  

### <a name="microsoft-edge-chromium"></a><span data-ttu-id="7ba8f-114">Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="7ba8f-114">Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="7ba8f-115">Si vous souhaitez lancer Microsoft Edge \(Chromium\), le nouveau Microsoft Edge, au lieu de Microsoft Edge \(EdgeHTML\), ajoutez simplement un attribut à votre configuration existante avec la version de Microsoft Edge \(Chromium\) que vous souhaitez lancer `version` \( `dev` , ou `beta` `canary` \).</span><span class="sxs-lookup"><span data-stu-id="7ba8f-115">If you want to launch Microsoft Edge \(Chromium\), the new Microsoft Edge, instead of Microsoft Edge \(EdgeHTML\), simply add a `version` attribute to your existing configuration with the version of Microsoft Edge \(Chromium\) you want to launch \(`dev`, `beta`, or `canary`\).</span></span>  <span data-ttu-id="7ba8f-116">La configuration suivante lance la version Canary de Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="7ba8f-116">The following configuration below launches the Canary version of Microsoft Edge \(Chromium\).</span></span>  

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

## <a name="attaching-to-microsoft-edge"></a><span data-ttu-id="7ba8f-117">Attachement à Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7ba8f-117">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="7ba8f-118">Attachez Visual Studio Code à Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="7ba8f-118">Attach Visual Studio Code to Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="7ba8f-119">À partir de votre terminal, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-119">From your terminal, run the following command.</span></span>  

```shell
start msedge --remote-debugging-port=9222
```  

<span data-ttu-id="7ba8f-120">Ajoutez la configuration ci-dessous à `launch.json` votre fichier.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-120">Add the configuration below to your `launch.json` file.</span></span>   

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```  

<span data-ttu-id="7ba8f-121">Si vous exécutez maintenant cette configuration, Visual Studio code s’attache à Microsoft Edge \(Chromium\) et démarre le débogage.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-121">If you now run this configuration, Visual Studio Code attaches to Microsoft Edge \(Chromium\) and start debugging.</span></span>  

## <a name="getting-in-touch-with-the-elements-for-microsoft-edge-visual-studio-code-extension-team"></a><span data-ttu-id="7ba8f-122">Mise en contact avec l’équipe d’extension de code Visual Studio Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7ba8f-122">Getting in touch with the Elements for Microsoft Edge Visual Studio Code extension team</span></span>    

<span data-ttu-id="7ba8f-123">Envoyez vos commentaires en [classant un problème][GithubMicrosoftVscodeEdgeDebug2NewIssue] dans le référentiel [GitHub][GithubMicrosoftVscodeEdgeDebug2] de l’extension.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-123">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDebug2NewIssue] against in the [GitHub repo][GithubMicrosoftVscodeEdgeDebug2] of the extension.</span></span>  <span data-ttu-id="7ba8f-124">Veuillez inclure le fichier journal de l’adaptateur de débogage, qui est créé pour chaque run dans le `%temp%` répertoire avec le nom `vscode-edge-debug2.txt` .</span><span class="sxs-lookup"><span data-stu-id="7ba8f-124">Please include the debug adapter log file, which is created for each run in the `%temp%` directory with the name `vscode-edge-debug2.txt`.</span></span>  <span data-ttu-id="7ba8f-125">Faites glisser ce fichier dans un commentaire de problème pour le télécharger sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-125">Drag this file into an issue comment to upload it to GitHub.</span></span>  

<span data-ttu-id="7ba8f-126">Pour améliorer les éléments de l’extension de code Visual Studio Microsoft Edge, vos contributions sont les bienvenues !</span><span class="sxs-lookup"><span data-stu-id="7ba8f-126">To help make the Elements for Microsoft Edge Visual Studio Code extension better, your contributions are welcome!</span></span>  <span data-ttu-id="7ba8f-127">Recherchez tout ce dont vous avez besoin pour commencer dans le [référentiel GitHub][GithubMicrosoftVscodeEdgeDebug2] de l’extension.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-127">Find everything you need to get started in [GitHub repo][GithubMicrosoftVscodeEdgeDebug2] of the extension.</span></span>  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge Visual Studio Code extension in action"  -->  
[ImagePngDebuggerEdge]: ./media/debugger-for-edge.png «Debugger for Edge Visual Studio Code extension in action»  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentation | Visual Studio Code"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "microsoft/vscode-edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Nouveau problème : microsoft/vscode-edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Débogger pour Microsoft Edge | Visual Studio Marketplace"  
