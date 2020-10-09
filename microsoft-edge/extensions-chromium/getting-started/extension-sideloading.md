---
description: Testez votre extension en la chargement indépendant dans le navigateur
title: Charger votre extension
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-chrome, développement Web, html, CSS, JavaScript, développeur, extensions
ms.openlocfilehash: 7070878b9608e6d239179078390f2315e0b289a1
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104771"
---
# <span data-ttu-id="f5e9a-104">Charger une extension</span><span class="sxs-lookup"><span data-stu-id="f5e9a-104">Sideload an extension</span></span>

<span data-ttu-id="f5e9a-105">Pendant le développement, vous pouvez utiliser le navigateur Microsoft Edge \ (chrome \) pour exécuter et déboguer votre extension en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="f5e9a-105">During development, you may use the Microsoft Edge \(Chromium\) browser to run and debug your extension safely.</span></span> <span data-ttu-id="f5e9a-106">Chargement indépendant votre extension locale dans votre navigateur, vous pouvez exécuter et tester votre extension.</span><span class="sxs-lookup"><span data-stu-id="f5e9a-106">By sideloading your extension locally in your browser, you can run and test your extension.</span></span> <span data-ttu-id="f5e9a-107">Cet article explique comment charger les extensions dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f5e9a-107">This article explains how to sideload extensions into Microsoft Edge.</span></span>

<span data-ttu-id="f5e9a-108">Pour charger votre extension, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="f5e9a-108">To sideload your extension, follow these steps.</span></span>

1.  <span data-ttu-id="f5e9a-109">Ouvrez la `edge://extensions` page en cliquant sur les points de suspension en haut de votre navigateur, puis sélectionnez **Extensions**.</span><span class="sxs-lookup"><span data-stu-id="f5e9a-109">Open the `edge://extensions` page by choosing the three dots at the top of your browser, and then selecting **Extensions**.</span></span>

       :::image type="complex" source="./media/part1-threedots.png" alt-text="Ouvrir la page edge://extensions":::
          <span data-ttu-id="f5e9a-111">Ouvrir la page edge://extensions</span><span class="sxs-lookup"><span data-stu-id="f5e9a-111">Open the edge://extensions page</span></span> :::image-end:::

1.  <span data-ttu-id="f5e9a-112">Dans la page gestion des extensions à `edge://extensions` , activez le **mode développeur** à l’aide du bouton bascule en bas à gauche de la page.</span><span class="sxs-lookup"><span data-stu-id="f5e9a-112">On the extension management page at `edge://extensions`, turn on **Developer mode** using the toggle at the bottom left of the page.</span></span>

       :::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Ouvrir la page edge://extensions":::
          <span data-ttu-id="f5e9a-114">Activer le mode développeur</span><span class="sxs-lookup"><span data-stu-id="f5e9a-114">Turn on Developer Mode</span></span> :::image-end:::

1.  <span data-ttu-id="f5e9a-115">Lorsque vous installez votre extension pour la première fois, sélectionnez **charger**.</span><span class="sxs-lookup"><span data-stu-id="f5e9a-115">When installing your extension for the first time, choose **Load Unpacked**.</span></span>  <span data-ttu-id="f5e9a-116">Vous serez invité à entrer le répertoire contenant vos fichiers sources d’extension.</span><span class="sxs-lookup"><span data-stu-id="f5e9a-116">You'll be prompted for the directory with your extension source files.</span></span>  <span data-ttu-id="f5e9a-117">Votre extension est installée dans votre navigateur, de la même façon que dans le Windows Store.</span><span class="sxs-lookup"><span data-stu-id="f5e9a-117">Your extension is installed in your browser, similar to extensions installed from the store.</span></span>  

       :::image type="complex" source="./media/part1-installed-extension.png" alt-text="Ouvrir la page edge://extensions":::
          <span data-ttu-id="f5e9a-119">Page extensions installés montrant une extension chargée</span><span class="sxs-lookup"><span data-stu-id="f5e9a-119">Installed extensions page showing a sideloaded extension</span></span> :::image-end:::

<span data-ttu-id="f5e9a-120">Pendant le développement, il est possible que vous deviez effectuer les tâches suivantes.</span><span class="sxs-lookup"><span data-stu-id="f5e9a-120">During development, you may also need to perform the following tasks.</span></span>
* <span data-ttu-id="f5e9a-121">Mettez à jour l’extension.</span><span class="sxs-lookup"><span data-stu-id="f5e9a-121">Update the extension.</span></span> <span data-ttu-id="f5e9a-122">Accédez à `edge://extensions` , puis sélectionnez **recharger** pour mettre à jour votre extension.</span><span class="sxs-lookup"><span data-stu-id="f5e9a-122">Navigate to `edge://extensions`, and then select **Reload** to update your extension.</span></span>  
* <span data-ttu-id="f5e9a-123">Supprimez l’extension de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="f5e9a-123">Remove the extension from your browser.</span></span> <span data-ttu-id="f5e9a-124">Accédez à `edge://extensions` , puis sélectionnez `Remove` sur votre extension.</span><span class="sxs-lookup"><span data-stu-id="f5e9a-124">Navigate to `edge://extensions`, and then select `Remove` on your extension.</span></span>