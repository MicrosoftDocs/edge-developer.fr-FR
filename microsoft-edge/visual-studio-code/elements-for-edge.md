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
# <span data-ttu-id="bd33e-104">Éléments pour l’extension de code Microsoft Edge VS</span><span class="sxs-lookup"><span data-stu-id="bd33e-104">Elements For Microsoft Edge VS Code Extension</span></span>  

<span data-ttu-id="bd33e-105">À l’aide des éléments de l’extension de code [Microsoft Edge][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] vs, utilisez l’outil éléments du navigateur Microsoft Edge à partir de [code Visual Studio][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="bd33e-105">With the [Elements for Microsoft Edge][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] VS Code extension, use the Elements tool of the Microsoft Edge browser from within [Visual Studio Code][VisualstudioCode].</span></span>  <span data-ttu-id="bd33e-106">Par le biais d’un lancement ou d’une attachement, l’outil éléments se connecte à une instance de Microsoft Edge, affiche la structure HTML d’exécution et vous permet de modifier la disposition ou de résoudre les problèmes de style.</span><span class="sxs-lookup"><span data-stu-id="bd33e-106">By either launching or attaching, the Elements tool connects to an instance of Microsoft Edge, displays the runtime HTML structure, and allows you to alter the layout or fix styling issues.</span></span>  

:::image type="complex" source="./media/elements-for-edge.gif" alt-text="Éléments pour l’extension latérale et du code au bureau":::
   <span data-ttu-id="bd33e-108">Éléments pour l’extension latérale et du code au bureau</span><span class="sxs-lookup"><span data-stu-id="bd33e-108">Elements for Edge VS Code extension at work</span></span>  
:::image-end:::

<!--![Elements for Edge VS Code extension at work][ImageGifElementsEdge]  -->  

## <span data-ttu-id="bd33e-109">Lancement de Microsoft Edge à partir de l’extension d’éléments</span><span class="sxs-lookup"><span data-stu-id="bd33e-109">Launching Microsoft Edge From the Elements extension</span></span>  

<span data-ttu-id="bd33e-110">Accédez aux éléments dans la **barre d’activité**.</span><span class="sxs-lookup"><span data-stu-id="bd33e-110">Navigate to Elements in the **Activity Bar**.</span></span>  <span data-ttu-id="bd33e-111">À côté de la mention **éléments pour Microsoft Edge: cibles,** il existe un signe plus qui ouvre le navigateur de votre application.</span><span class="sxs-lookup"><span data-stu-id="bd33e-111">Next to where it says **Elements for Microsoft Edge: Targets,** there is a plus sign that opens the browser for your app.</span></span>  <span data-ttu-id="bd33e-112">Si vous avez sélectionné l’option **à propos** de, vous devez accéder à votre application Web dans le navigateur pour qu’elle apparaisse dans le panneau éléments du code vs.</span><span class="sxs-lookup"><span data-stu-id="bd33e-112">If you selected the **about:blank** option, you must navigate to your web app in the browser for it to appear in the Elements panel in VS Code.</span></span>  

## <span data-ttu-id="bd33e-113">Lancement de Microsoft Edge à partir de la vue de débogage</span><span class="sxs-lookup"><span data-stu-id="bd33e-113">Launching Microsoft Edge from the Debug view</span></span>  

<span data-ttu-id="bd33e-114">Si vous avez l’habitude d’utiliser le mode débogage dans du code Visual Studio, accédez à des éléments à partir de cet outil.</span><span class="sxs-lookup"><span data-stu-id="bd33e-114">If you are accustomed to using the Debug view in Visual Studio Code, access Elements from that tool.</span></span>  <span data-ttu-id="bd33e-115">Accédez à la vue de débogage \ ( `Ctrl` + `Shift` + `D` sous Windows ou `Command` + `Shift` + `D` Mac \).</span><span class="sxs-lookup"><span data-stu-id="bd33e-115">Navigate to the Debug view \(`Ctrl`+`Shift`+`D` on Windows or `Command`+`Shift`+`D` on macOS\).</span></span>  

<span data-ttu-id="bd33e-116">Si vous n’avez pas de configurations dans le code VS, appuyez `F5` sur Windows ou MacOS ou sélectionnez le bouton de **lecture** de couleur verte.</span><span class="sxs-lookup"><span data-stu-id="bd33e-116">If you do not have any configurations in VS Code, press `F5` on Windows or macOS or select the green **Play** button.</span></span> <span data-ttu-id="bd33e-117">Dans la liste déroulante, sélectionnez **Edge** .</span><span class="sxs-lookup"><span data-stu-id="bd33e-117">Select **Edge** in the dropdown.</span></span> <span data-ttu-id="bd33e-118">Vous devez voir un `launch.json` fichier avec la configuration suivante.</span><span class="sxs-lookup"><span data-stu-id="bd33e-118">You should see a `launch.json` file with the following configuration.</span></span>  

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

<span data-ttu-id="bd33e-119">À présent que vous avez chargé la configuration appropriée, appuyez `F5` sur Windows ou MacOS ou sélectionnez le bouton de **lecture** vert.</span><span class="sxs-lookup"><span data-stu-id="bd33e-119">Now that you have loaded the correct configuration, either press `F5` on Windows or macOS or select the green **Play** button.</span></span> <span data-ttu-id="bd33e-120">L’outil éléments qui vous est familier, sur le navigateur Microsoft Edge, démarre dans le code VS, ce qui vous permet d’accéder à un enregistrement de votre navigateur et d’examiner les composants de votre page.</span><span class="sxs-lookup"><span data-stu-id="bd33e-120">The Elements tool, that is familiar to you, from the Microsoft Edge browser launches in VS Code, allowing you to access a screencast of your browser and examine the components of your page.</span></span>  

## <span data-ttu-id="bd33e-121">Joindre à Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bd33e-121">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="bd33e-122">Pour joindre le code VS à une instance de Microsoft Edge \ (chrome \), vous devez démarrer le navigateur en exécutant la commande suivante à partir de votre terminal.</span><span class="sxs-lookup"><span data-stu-id="bd33e-122">To attach VS Code to an instance of Microsoft Edge\(Chromium\), you must start the browser by running the following command from your terminal.</span></span>  

`start msedge --remote-debugging-port=9222`  

<span data-ttu-id="bd33e-123">Une fois l’application lancée, ajoutez la configuration ci-dessous à votre fichier **Launch. JSON** :</span><span class="sxs-lookup"><span data-stu-id="bd33e-123">Once the app has launched, add the configuration below to your **launch.json** file:</span></span>  

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

<span data-ttu-id="bd33e-124">Sélectionnez **joindre à Microsoft Edge, puis ouvrez l’outil éléments** à partir du menu déroulant débogueur.</span><span class="sxs-lookup"><span data-stu-id="bd33e-124">Select **Attach to Microsoft Edge and open the Elements tool** from the Debugger drop-down menu.</span></span>  <span data-ttu-id="bd33e-125">Appuyez ensuite `F5` sur Windows ou MacOS ou sélectionnez le bouton de **lecture** vert.</span><span class="sxs-lookup"><span data-stu-id="bd33e-125">Next, either press `F5` on Windows or macOS or select the green **Play** button.</span></span>  <span data-ttu-id="bd33e-126">Le code VS lance l’outil éléments, ce qui vous permet d’accéder à la vidéo de votre navigateur, de vérifier le DOM et de styliser les composants sur votre page.</span><span class="sxs-lookup"><span data-stu-id="bd33e-126">VS Code launches the Elements tool, allowing you to access a screencast of your browser, inspect the DOM, and the styling of the components on your page.</span></span>  

## <span data-ttu-id="bd33e-127">Accès aux éléments de l’équipe d’extension du code Microsoft Edge VS</span><span class="sxs-lookup"><span data-stu-id="bd33e-127">Getting in touch with the Elements for Microsoft Edge VS Code extension team</span></span>  

<span data-ttu-id="bd33e-128">Envoyez vos commentaires en envoyant [un problème][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] à l’aide de la [GitHub référentiel Samples][GithubMicrosoftVscodeEdgeDevtools] de l’extension.</span><span class="sxs-lookup"><span data-stu-id="bd33e-128">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] against the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<span data-ttu-id="bd33e-129">Si vous souhaitez améliorer l’extension du code Microsoft Edge et celle du code, vos contributions sont les bienvenues.</span><span class="sxs-lookup"><span data-stu-id="bd33e-129">If you want to help make the Elements for Microsoft Edge VS Code extension better, your contributions are welcome!</span></span>  <span data-ttu-id="bd33e-130">Trouvez tout ce dont vous avez besoin pour commencer à utiliser le [GitHub référentiel Samples][GithubMicrosoftVscodeEdgeDevtools] de l’extension.</span><span class="sxs-lookup"><span data-stu-id="bd33e-130">Find everything you need to get started in the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

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
