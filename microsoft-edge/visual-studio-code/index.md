---
description: Microsoft Edge (chrome) et code Visual Studio
title: VisualStudioCode
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/12/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, code vs, code Visual Studio, débogueur, webhint
ms.openlocfilehash: 94148864edbd43adbe2dc9f3d0c2fa0c1f7f0b43
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566606"
---
# <span data-ttu-id="a8722-104">VisualStudioCode</span><span class="sxs-lookup"><span data-stu-id="a8722-104">Visual Studio Code</span></span>

<span data-ttu-id="a8722-105">Le [code Visual Studio](https://code.visualstudio.com/Docs) est un éditeur de code source léger mais puissant qui s’exécute sur votre ordinateur de bureau et est disponible pour Windows, MacOS et Linux.</span><span class="sxs-lookup"><span data-stu-id="a8722-105">[Visual Studio Code](https://code.visualstudio.com/Docs) is a lightweight but powerful source code editor which runs on your desktop and is available for Windows, macOS and Linux.</span></span> <span data-ttu-id="a8722-106">Il s’agit d’une prise en charge intégrée de JavaScript, de connexion et de node. js pour qu’il s’agit d’un excellent outil pour les développeurs Web.</span><span class="sxs-lookup"><span data-stu-id="a8722-106">It comes with built-in support for JavaScript, TypeScript and Node.js so it's a great tool for web developers right out of the box!</span></span> <span data-ttu-id="a8722-107">Accédez à [cette page](https://code.visualstudio.com/) pour télécharger le code Visual Studio si vous ne l’utilisez pas encore.</span><span class="sxs-lookup"><span data-stu-id="a8722-107">Head to [this page](https://code.visualstudio.com/) to download Visual Studio Code if you aren't using it yet.</span></span>

## <span data-ttu-id="a8722-108">Extensions</span><span class="sxs-lookup"><span data-stu-id="a8722-108">Extensions</span></span>

<!-- We want to put something like the tiles for extensions VS Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page. I think it's a web page. I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->

<span data-ttu-id="a8722-109">Pour acquérir les extensions mises en surbrillance ci-dessous, accédez à extensions ( `Ctrl`  +  `Shift`  +  `X` Windows ou `Command`  +  `Shift`  +  `X` Mac) en code vs.</span><span class="sxs-lookup"><span data-stu-id="a8722-109">To acquire any of the extensions highlighted below, navigate to Extensions (`Ctrl` + `Shift` + `X` on Windows or `Command` + `Shift` + `X` on Mac) in VS Code.</span></span>

<span data-ttu-id="a8722-110">Recherchez l’extension dans Marketplace Marketplace et sélectionnez **installer**.</span><span class="sxs-lookup"><span data-stu-id="a8722-110">Search the Marketplace for the specific extension and select **Install**.</span></span>

![Installation du débogueur pour l’extension de code Microsoft Edge VS](./media/vscode-debugger-install.png)

## <span data-ttu-id="a8722-112">Débogueur pour Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a8722-112">Debugger for Microsoft Edge</span></span>

<span data-ttu-id="a8722-113">Déboguez votre ligne de code JavaScript frontal par ligne et les `console.log()` instructions d’affichage directement dans le [code Visual Studio](https://code.visualstudio.com/) à l’aide du [débogueur de l’extension de code Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs.</span><span class="sxs-lookup"><span data-stu-id="a8722-113">Debug your front-end JavaScript code line by line and display `console.log()` statements directly in [Visual Studio Code](https://code.visualstudio.com/) using the the [Debugger for Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS Code extension!</span></span>

<span data-ttu-id="a8722-114">Utilisez le [débogueur pour](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) l’extension de code Microsoft Edge vs pour lancer une extension ou l’attacher à Microsoft Edge (EdgeHTML) et Microsoft Edge (chrome).</span><span class="sxs-lookup"><span data-stu-id="a8722-114">Use the [Debugger for Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS Code extension to launch or attach to both Microsoft Edge (EdgeHTML) and Microsoft Edge (Chromium).</span></span> <span data-ttu-id="a8722-115">Consultez [cette page](./debugger-for-edge.md) pour obtenir une procédure pas à pas de débogage de Microsoft Edge à partir de code vs et d’exemples de configurations de **Launch. JSON** .</span><span class="sxs-lookup"><span data-stu-id="a8722-115">Check out [this page](./debugger-for-edge.md) for a walkthrough of debugging Microsoft Edge from VS Code and sample **launch.json** configurations.</span></span>

![Image GIF du débogueur pour l’extension de code Edge et en action](./media/debugger-for-edge.gif)

## <span data-ttu-id="a8722-117">Éléments pour Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a8722-117">Elements for Microsoft Edge</span></span>

<span data-ttu-id="a8722-118">En ajoutant les [éléments de l’extension de code Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools) vs, vous pouvez utiliser l’outil éléments du navigateur dans le code Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a8722-118">By adding the [Elements for Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools) VS Code extension, you can use the browser's Elements tool from within Visual Studio Code.</span></span> <span data-ttu-id="a8722-119">Par le biais d’un lancement ou d’une attachement, l’outil éléments se connecte à une instance de Microsoft Edge, affiche la structure HTML d’exécution et vous permet de modifier la disposition ou de résoudre les problèmes de style.</span><span class="sxs-lookup"><span data-stu-id="a8722-119">By either launching or attaching, the Elements tool will connect to an instance of Microsoft Edge, display the runtime HTML structure, and allow you to alter the layout or fix styling issues.</span></span>

<span data-ttu-id="a8722-120">Pour plus d’informations, consultez [cette page](./elements-for-edge.md).</span><span class="sxs-lookup"><span data-stu-id="a8722-120">For more information, check out [this page](./elements-for-edge.md).</span></span>

![Image GIF de tous les éléments de l’extension du code Edge et de l’action.](./media/elements-for-edge.gif)

## <span data-ttu-id="a8722-122">Astuce</span><span class="sxs-lookup"><span data-stu-id="a8722-122">webhint</span></span>

<span data-ttu-id="a8722-123">Utilisez [webhint](https://webhint.io), un outil de débordement personnalisable pour améliorer l’accessibilité, les performances, la compatibilité entre les navigateurs, la compatibilité de Project Web App et la sécurité de votre site.</span><span class="sxs-lookup"><span data-stu-id="a8722-123">Use [webhint](https://webhint.io), a customizable linting tool, to improve the accessibility, performance, cross-browser compatibility, PWA compatibility, and security of your site.</span></span> <span data-ttu-id="a8722-124">Il recherche les meilleures pratiques et les erreurs courantes dans votre code.</span><span class="sxs-lookup"><span data-stu-id="a8722-124">It checks your code for best practices and common errors.</span></span> <span data-ttu-id="a8722-125">Ce projet open-source développé au départ par l’équipe Microsoft Edge, fait désormais partie de [OpenJS Foundation](https://openjsf.org/).</span><span class="sxs-lookup"><span data-stu-id="a8722-125">This open-source project, initially developed by the Microsoft Edge team, is now part of the [OpenJS Foundation](https://openjsf.org/).</span></span> <span data-ttu-id="a8722-126">L’équipe Microsoft Edge cesse de contribuer à la communauté et aux développeurs Web de la communauté.</span><span class="sxs-lookup"><span data-stu-id="a8722-126">The Microsoft Edge team continues to contribute to webhint alongside web developers in the community.</span></span>

![Capture d’écran de l’extension de code webhint VS](./media/webhint-extension.png)

<span data-ttu-id="a8722-128">Identifiez et corrigez les problèmes de votre code HTML, de CSS, de JavaScript, de la machine à écrire et bien plus encore en ajoutant l' [extension webhint pour le code vs](https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint).</span><span class="sxs-lookup"><span data-stu-id="a8722-128">Identify and fix problems in your HTML, CSS, JavaScript, TypeScript, and more by adding the [webhint extension for VS Code](https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint).</span></span> <span data-ttu-id="a8722-129">Les indications apparaissent sous forme de soulignements inline et sont synthétisées dans le volet problèmes.</span><span class="sxs-lookup"><span data-stu-id="a8722-129">Hints appear as inline underlines and are summarized in the Problems pane.</span></span>

<span data-ttu-id="a8722-130">Pour plus d’informations, voir [utilisation de webhint dans le code Visual Studio](./webhint.md).</span><span class="sxs-lookup"><span data-stu-id="a8722-130">For more information, see [How to use webhint in Visual Studio Code](./webhint.md).</span></span>
