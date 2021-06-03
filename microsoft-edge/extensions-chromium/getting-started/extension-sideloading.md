---
description: Testez votre extension en la chargeant de nouveau dans le navigateur
title: Chargement de version de version secondaire de votre extension
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, développement web, html, css, javascript, développeur, extensions
ms.openlocfilehash: 7070878b9608e6d239179078390f2315e0b289a1
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104771"
---
# <span data-ttu-id="6101c-104">Charger une version test d’une extension</span><span class="sxs-lookup"><span data-stu-id="6101c-104">Sideload an extension</span></span>

<span data-ttu-id="6101c-105">Pendant le développement, vous pouvez utiliser le navigateur Microsoft Edge \(Chromium\) pour exécuter et déboguer votre extension en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="6101c-105">During development, you may use the Microsoft Edge \(Chromium\) browser to run and debug your extension safely.</span></span> <span data-ttu-id="6101c-106">En chargeant une version test de votre extension localement dans votre navigateur, vous pouvez exécuter et tester votre extension.</span><span class="sxs-lookup"><span data-stu-id="6101c-106">By sideloading your extension locally in your browser, you can run and test your extension.</span></span> <span data-ttu-id="6101c-107">Cet article explique comment chargement de version de chargement des extensions dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6101c-107">This article explains how to sideload extensions into Microsoft Edge.</span></span>

<span data-ttu-id="6101c-108">Pour recharger une version de votre extension, suivez ces étapes.</span><span class="sxs-lookup"><span data-stu-id="6101c-108">To sideload your extension, follow these steps.</span></span>

1.  <span data-ttu-id="6101c-109">Ouvrez la page en choisissant les trois points en haut de votre navigateur, puis en sélectionnant `edge://extensions` **Extensions.**</span><span class="sxs-lookup"><span data-stu-id="6101c-109">Open the `edge://extensions` page by choosing the three dots at the top of your browser, and then selecting **Extensions**.</span></span>

       :::image type="complex" source="./media/part1-threedots.png" alt-text="Ouvrir la page edge://extensions page":::
          <span data-ttu-id="6101c-111">Ouvrir la page edge://extensions page</span><span class="sxs-lookup"><span data-stu-id="6101c-111">Open the edge://extensions page</span></span> :::image-end:::

1.  <span data-ttu-id="6101c-112">Dans la page gestion des extensions, dans , activer le mode développeur à l’aide du basculement en `edge://extensions` bas à gauche de la page. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="6101c-112">On the extension management page at `edge://extensions`, turn on **Developer mode** using the toggle at the bottom left of the page.</span></span>

       :::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Activer le mode développeur":::
          <span data-ttu-id="6101c-114">Activer le mode développeur</span><span class="sxs-lookup"><span data-stu-id="6101c-114">Turn on Developer Mode</span></span> :::image-end:::

1.  <span data-ttu-id="6101c-115">Lors de l’installation de votre extension pour la première fois, choisissez **Charger décompressé.**</span><span class="sxs-lookup"><span data-stu-id="6101c-115">When installing your extension for the first time, choose **Load Unpacked**.</span></span>  <span data-ttu-id="6101c-116">You’ll be prompted for the directory with your extension source files.</span><span class="sxs-lookup"><span data-stu-id="6101c-116">You'll be prompted for the directory with your extension source files.</span></span>  <span data-ttu-id="6101c-117">Votre extension est installée dans votre navigateur, comme les extensions installées à partir du store.</span><span class="sxs-lookup"><span data-stu-id="6101c-117">Your extension is installed in your browser, similar to extensions installed from the store.</span></span>  

       :::image type="complex" source="./media/part1-installed-extension.png" alt-text="Page Des extensions installées affichant une extension installée":::
          <span data-ttu-id="6101c-119">Page Des extensions installées affichant une extension installée</span><span class="sxs-lookup"><span data-stu-id="6101c-119">Installed extensions page showing a sideloaded extension</span></span> :::image-end:::

<span data-ttu-id="6101c-120">Lors du développement, vous devrez peut-être également effectuer les tâches suivantes.</span><span class="sxs-lookup"><span data-stu-id="6101c-120">During development, you may also need to perform the following tasks.</span></span>
* <span data-ttu-id="6101c-121">Mettez à jour l’extension.</span><span class="sxs-lookup"><span data-stu-id="6101c-121">Update the extension.</span></span> <span data-ttu-id="6101c-122">Accédez `edge://extensions` à , puis sélectionnez **Recharger** pour mettre à jour votre extension.</span><span class="sxs-lookup"><span data-stu-id="6101c-122">Navigate to `edge://extensions`, and then select **Reload** to update your extension.</span></span>  
* <span data-ttu-id="6101c-123">Supprimez l’extension de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="6101c-123">Remove the extension from your browser.</span></span> <span data-ttu-id="6101c-124">Accédez `edge://extensions` à , puis sélectionnez votre `Remove` extension.</span><span class="sxs-lookup"><span data-stu-id="6101c-124">Navigate to `edge://extensions`, and then select `Remove` on your extension.</span></span>