---
description: Utiliser des éléments pour Microsoft Edge (chrome) à partir du code VS
title: Éléments de Microsoft Edge (chrome) issus du code VS
author: erdraud
ms.author: erdraud
ms.date: 08/08/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, code vs, code Visual Studio, éléments
ms.openlocfilehash: 4875a4665fe1561ecf587a050bbd44e116d9ce5e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566607"
---
# <span data-ttu-id="86a33-104">Éléments pour l’extension de code Microsoft Edge VS</span><span class="sxs-lookup"><span data-stu-id="86a33-104">Elements for Microsoft Edge VS Code extension</span></span>

<span data-ttu-id="86a33-105">En ajoutant les [éléments de l’extension de code Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools) vs, vous pouvez utiliser l’outil éléments du navigateur dans le [code Visual Studio](https://code.visualstudio.com/).</span><span class="sxs-lookup"><span data-stu-id="86a33-105">By adding the [Elements for Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools) VS Code extension, you can use the browser's Elements tool from within [Visual Studio Code](https://code.visualstudio.com/).</span></span> <span data-ttu-id="86a33-106">Par le biais d’un lancement ou d’une attachement, l’outil éléments se connecte à une instance de Microsoft Edge, affiche la structure HTML d’exécution et vous permet de modifier la disposition ou de résoudre les problèmes de style.</span><span class="sxs-lookup"><span data-stu-id="86a33-106">By either launching or attaching, the Elements tool will connect to an instance of Microsoft Edge, display the runtime HTML structure, and allow you to alter the layout or fix styling issues.</span></span>

![Image GIF des éléments pour l’extension du code Edge et au bureau](./media/elements-for-edge.gif)

## <span data-ttu-id="86a33-108">Lancement de Microsoft Edge à partir de l’extension d’éléments</span><span class="sxs-lookup"><span data-stu-id="86a33-108">Launching Microsoft Edge From the Elements extension</span></span> 

<span data-ttu-id="86a33-109">Accédez aux éléments dans la **barre d’activité**.</span><span class="sxs-lookup"><span data-stu-id="86a33-109">Navigate to Elements in the **Activity Bar**.</span></span> <span data-ttu-id="86a33-110">À côté de la mention «éléments pour Microsoft Edge: cibles», il existe un signe plus qui ouvre le navigateur de votre application.</span><span class="sxs-lookup"><span data-stu-id="86a33-110">Next to where it says "Elements for Microsoft Edge: Targets," there is a plus sign that will open the browser for your app.</span></span> <span data-ttu-id="86a33-111">Si vous avez sélectionné l’option *à propos de: vide* , vous devrez accéder à votre application Web dans le navigateur pour qu’elle apparaisse dans le panneau d’éléments du code vs.</span><span class="sxs-lookup"><span data-stu-id="86a33-111">If you selected the *about:blank* option, you will have to navigate to your web app in the browser for it to appear in the Elements panel in VS Code.</span></span>

## <span data-ttu-id="86a33-112">Lancement de Microsoft Edge à partir de la vue de débogage</span><span class="sxs-lookup"><span data-stu-id="86a33-112">Launching Microsoft Edge from the Debug view</span></span>

<span data-ttu-id="86a33-113">Si vous avez l’habitude d’utiliser le mode débogage dans du code Visual Studio, vous pouvez accéder à des éléments à partir de cet outil.</span><span class="sxs-lookup"><span data-stu-id="86a33-113">If you are accustomed to using the Debug view in Visual Studio Code, you can access Elements from that tool.</span></span> <span data-ttu-id="86a33-114">Accédez à la vue de débogage ( `Ctrl`  +  `Shift`  +  `D` sous Windows ou `Command`  +  `Shift`  +  `D` sur Mac).</span><span class="sxs-lookup"><span data-stu-id="86a33-114">Navigate to the Debug view (`Ctrl` + `Shift` + `D` on Windows or `Command` + `Shift` + `D` on Mac).</span></span> 

<span data-ttu-id="86a33-115">Si vous n’avez pas de configurations dans le code VS, appuyez `F5` sur Windows ou Mac ou cliquez sur le bouton de **lecture** de couleur verte.</span><span class="sxs-lookup"><span data-stu-id="86a33-115">If you do not have any configurations in VS Code, press `F5` on Windows or Mac or click the green **Play** button.</span></span> <span data-ttu-id="86a33-116">Dans la liste déroulante, sélectionnez «Edge».</span><span class="sxs-lookup"><span data-stu-id="86a33-116">Select "Edge" in the dropdown.</span></span> <span data-ttu-id="86a33-117">Un fichier **Launch. JSON** s’affiche alors avec la configuration suivante:</span><span class="sxs-lookup"><span data-stu-id="86a33-117">You will now see a **launch.json** file with the following configuration:</span></span>

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

<span data-ttu-id="86a33-118">À présent que vous avez chargé la configuration appropriée, appuyez sur `F5` Windows ou Mac ou cliquez sur le bouton de **lecture** vert.</span><span class="sxs-lookup"><span data-stu-id="86a33-118">Now that you have loaded the correct configuration, either press `F5` on Windows or Mac or click the green **Play** button.</span></span> <span data-ttu-id="86a33-119">L’outil éléments qui vous est familier dans le navigateur Microsoft Edge sera lancé dans le code VS, ce qui vous permet d’accéder à un enregistrement de votre navigateur et d’examiner les composants de votre page.</span><span class="sxs-lookup"><span data-stu-id="86a33-119">The Elements tool you are familiar with from the Microsoft Edge browser will now launch in VS Code, allowing you to access a screencast of your browser and examine the components of your page.</span></span>

## <span data-ttu-id="86a33-120">Joindre à Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="86a33-120">Attaching to Microsoft Edge</span></span>
<span data-ttu-id="86a33-121">Si vous voulez joindre le code VS à une instance de Microsoft Edge (chrome), vous devez démarrer le navigateur en exécutant la commande suivante à partir de votre teminal:</span><span class="sxs-lookup"><span data-stu-id="86a33-121">If you'd like to attach VS Code to an instance of Microsoft Edge (Chromium), you must start the browser by running the following command from your teminal:</span></span>

`start msedge --remote-debugging-port=9222`

<span data-ttu-id="86a33-122">Une fois l’application lancée, ajoutez la configuration ci-dessous à votre fichier **Launch. JSON** :</span><span class="sxs-lookup"><span data-stu-id="86a33-122">Once the app has launched, add the configuration below to your **launch.json** file:</span></span>

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

<span data-ttu-id="86a33-123">Sélectionnez «joindre à Microsoft Edge et ouvrir l’outil éléments» dans le menu déroulant débogueur.</span><span class="sxs-lookup"><span data-stu-id="86a33-123">Select "Attach to Microsoft Edge and open the Elements tool" from the Debugger drop-down menu.</span></span> <span data-ttu-id="86a33-124">Ensuite, appuyez sur `F5` Windows ou Mac ou cliquez sur le bouton de **lecture** de couleur verte.</span><span class="sxs-lookup"><span data-stu-id="86a33-124">Next, either press `F5` on Windows or Mac or click the green **Play** button.</span></span> <span data-ttu-id="86a33-125">Le code est lancé par le biais de l’outil éléments, ce qui vous permet d’accéder à un enregistrement de votre navigateur, de vérifier le DOM et de styliser les composants sur votre page.</span><span class="sxs-lookup"><span data-stu-id="86a33-125">VS Code will launch the Elements tool, allowing you to access a screencast of your browser, inspect the DOM, and the styling of the components on your page.</span></span>

## <span data-ttu-id="86a33-126">Commentaires</span><span class="sxs-lookup"><span data-stu-id="86a33-126">Feedback</span></span>
<span data-ttu-id="86a33-127">Envoyez-nous vos commentaires en envoyant [un problème](https://github.com/microsoft/vscode-edge-devtools/issues/new) à l’aide de cette extension [GitHub référentiel Samples](https://github.com/microsoft/vscode-edge-devtools).</span><span class="sxs-lookup"><span data-stu-id="86a33-127">Send us your feedback by [filing an issue](https://github.com/microsoft/vscode-edge-devtools/issues/new) against this extension's [GitHub repo](https://github.com/microsoft/vscode-edge-devtools).</span></span> 

<span data-ttu-id="86a33-128">Si vous souhaitez nous aider à améliorer cette extension, nous accueillons vos contributions.</span><span class="sxs-lookup"><span data-stu-id="86a33-128">If you want to help us make this extension better, we welcome your contributions!</span></span> <span data-ttu-id="86a33-129">Vous trouverez tout ce dont vous avez besoin pour commencer à utiliser [notre GitHub référentiel Samples](https://github.com/microsoft/vscode-edge-devtools).</span><span class="sxs-lookup"><span data-stu-id="86a33-129">You can find everything you need to get started in [our GitHub repo](https://github.com/microsoft/vscode-edge-devtools).</span></span>