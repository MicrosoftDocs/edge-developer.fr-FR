---
description: Comment déboguer Microsoft Edge (chrome) et Microsoft Edge (EdgeHTML) du code VS
title: Déboguer Microsoft Edge (chrome) à partir du code VS
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/10/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, code vs, code Visual Studio, débogueur
ms.openlocfilehash: 7d8d2f87500b3e81866b49de32db91c0a525baf2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566603"
---
# <span data-ttu-id="e52fb-104">Débogueur pour l’extension de code Microsoft Edge VS</span><span class="sxs-lookup"><span data-stu-id="e52fb-104">Debugger for Microsoft Edge VS Code extension</span></span>

<span data-ttu-id="e52fb-105">Le [débogueur de l’extension de code Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs vous permet de déboguer votre ligne de code JavaScript frontal par ligne et de voir les instructions qui s’affichent `console.log()` directement à partir de [code Visual Studio](https://code.visualstudio.com/)!</span><span class="sxs-lookup"><span data-stu-id="e52fb-105">With the [Debugger for Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS Code extension, you can debug your front-end JavaScript code line by line and see `console.log()` statements all directly from [Visual Studio Code](https://code.visualstudio.com/)!</span></span>

![Image GIF du débogueur pour l’extension de code Edge et au bureau](./media/debugger-for-edge.gif)

## <span data-ttu-id="e52fb-107">Lancement de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e52fb-107">Launching Microsoft Edge</span></span>

<span data-ttu-id="e52fb-108">Accédez à la vue débogage ( `Ctrl`  +  `Shift`  +  `D` sous Windows ou `Command`  +  `Shift`  +  `D` sur Mac) dans la **barre d’activité**.</span><span class="sxs-lookup"><span data-stu-id="e52fb-108">Navigate to the Debug view (`Ctrl` + `Shift` + `D` on Windows or `Command` + `Shift` + `D` on Mac) in the **Activity Bar**.</span></span> <span data-ttu-id="e52fb-109">Si vous n’avez pas de configurations dans le code VS, appuyez `F5` sur Windows ou Mac ou cliquez sur le bouton de **lecture** de couleur verte.</span><span class="sxs-lookup"><span data-stu-id="e52fb-109">If you do not have any configurations in VS Code, press `F5` on Windows or Mac or click the green **Play** button.</span></span> <span data-ttu-id="e52fb-110">Dans la liste déroulante, sélectionnez «Edge».</span><span class="sxs-lookup"><span data-stu-id="e52fb-110">Select "Edge" in the dropdown.</span></span> <span data-ttu-id="e52fb-111">Un fichier **Launch. JSON** s’affiche alors avec la configuration suivante:</span><span class="sxs-lookup"><span data-stu-id="e52fb-111">You will now see a **launch.json** file with the following configuration:</span></span>

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

<span data-ttu-id="e52fb-112">Si vous avez à présent appuyé `F5` sur Windows ou Mac ou cliquez de nouveau sur le bouton de **lecture** de couleur verte, le code est lancé par le biais de Microsoft Edge (EdgeHTML) et vous pourrez déboguer n’importe quel projet Web exécuté sur le port **8080** directement à partir du code vs.</span><span class="sxs-lookup"><span data-stu-id="e52fb-112">If you now press `F5` on Windows or Mac or click the green **Play** button again, VS Code will launch Microsoft Edge (EdgeHTML) and you will be able to debug any web project you have running on port **8080** directly from VS Code!</span></span>

### <span data-ttu-id="e52fb-113">Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="e52fb-113">Microsoft Edge (Chromium)</span></span>

<span data-ttu-id="e52fb-114">Si vous voulez lancer Microsoft Edge (chrome), la nouvelle version de Microsoft Edge, au lieu de Microsoft Edge (EdgeHTML), vous devez simplement ajouter un `version` attribut à votre configuration existante avec la version de Microsoft Edge (chrome) que vous voulez lancer ( `dev` , `beta` ou `canary` ).</span><span class="sxs-lookup"><span data-stu-id="e52fb-114">If you want to launch Microsoft Edge (Chromium), the next version of Microsoft Edge, instead of Microsoft Edge (EdgeHTML), simply add a `version` attribute to your existing configuration with the version of Microsoft Edge (Chromium) you want to launch (`dev`, `beta`, or `canary`).</span></span> <span data-ttu-id="e52fb-115">La configuration suivante entraîne le lancement de la version Canaries de Microsoft Edge (chrome):</span><span class="sxs-lookup"><span data-stu-id="e52fb-115">The configuration below will launch the Canary version of Microsoft Edge (Chromium):</span></span>

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

## <span data-ttu-id="e52fb-116">Joindre à Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e52fb-116">Attaching to Microsoft Edge</span></span>

<span data-ttu-id="e52fb-117">Vous pouvez également joindre le code VS à Microsoft Edge (chrome).</span><span class="sxs-lookup"><span data-stu-id="e52fb-117">You can also attach VS Code to Microsoft Edge (Chromium).</span></span> <span data-ttu-id="e52fb-118">À partir de votre terminal, exécutez la commande suivante:</span><span class="sxs-lookup"><span data-stu-id="e52fb-118">From your terminal, run the following command:</span></span>

`start msedge --remote-debugging-port=9222`

<span data-ttu-id="e52fb-119">Ajoutez la configuration ci-dessous à votre fichier **Launch. JSON** :</span><span class="sxs-lookup"><span data-stu-id="e52fb-119">Add the configuration below to your **launch.json** file:</span></span>

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```

<span data-ttu-id="e52fb-120">S’il s’agit de la configuration, le code VS sera attaché à Microsoft Edge (chrome) et vous pourrez démarrer le débogage.</span><span class="sxs-lookup"><span data-stu-id="e52fb-120">If you now run this configuration, VS Code will attach to Microsoft Edge (Chromium) and you can start debugging!</span></span>

## <span data-ttu-id="e52fb-121">Commentaires</span><span class="sxs-lookup"><span data-stu-id="e52fb-121">Feedback</span></span>

<span data-ttu-id="e52fb-122">Envoyez-nous vos commentaires en envoyant [un problème](https://github.com/Microsoft/vscode-edge-debug2/issues/new) à l’aide de cette extension [GitHub référentiel Samples](https://github.com/Microsoft/vscode-edge-debug2).</span><span class="sxs-lookup"><span data-stu-id="e52fb-122">Send us your feedback by [filing an issue](https://github.com/Microsoft/vscode-edge-debug2/issues/new) against this extension's [GitHub repo](https://github.com/Microsoft/vscode-edge-debug2).</span></span> <span data-ttu-id="e52fb-123">Incluez le fichier journal de l’adaptateur de débogage, qui est créé pour chaque exécution du répertoire% Temp% avec le nom `vscode-edge-debug2.txt` .</span><span class="sxs-lookup"><span data-stu-id="e52fb-123">Please include the debug adapter log file, which is created for each run in the %temp% directory with the name `vscode-edge-debug2.txt`.</span></span> <span data-ttu-id="e52fb-124">Vous pouvez faire glisser ce fichier dans un commentaire de problème pour le télécharger sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="e52fb-124">You can drag this file into an issue comment to upload it to GitHub.</span></span>

<span data-ttu-id="e52fb-125">Si vous souhaitez nous aider à améliorer cette extension, nous accueillons vos contributions.</span><span class="sxs-lookup"><span data-stu-id="e52fb-125">If you want to help us make this extension better, we welcome your contributions!</span></span> <span data-ttu-id="e52fb-126">Vous trouverez tout ce dont vous avez besoin pour commencer à utiliser [notre GitHub référentiel Samples](https://github.com/Microsoft/vscode-edge-debug2).</span><span class="sxs-lookup"><span data-stu-id="e52fb-126">You can find everything you need to get started in [our GitHub repo](https://github.com/Microsoft/vscode-edge-debug2).</span></span>