---
description: Découvrez comment ajouter et supprimer des extensions, ainsi que déplacer le bouton d’une extension en regard de la barre d’adresses.
title: Ajout et suppression d’extensions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, développement web, html, css, javascript, développeur, extension
ms.custom: seodec18
ms.date: 12/15/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3473108918ec3cb3945e0999b27873ddea40aa5c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233450"
---
# <span data-ttu-id="69c07-104">Ajout, déplacement et suppression d’extensions pour Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="69c07-104">Adding, moving, and removing extensions for Microsoft Edge</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="69c07-105">La prise en charge des extensions par Microsoft Edge a été introduite dans la **mise à jour du 10e anniversaire de Windows**.</span><span class="sxs-lookup"><span data-stu-id="69c07-105">Microsoft Edge support for extensions was introduced in the **Windows 10 Anniversary Update**.</span></span> <span data-ttu-id="69c07-106">Si vous développez une extension Microsoft Edge et que vous voulez la charger, ou si vous l'avez déjà et que vous voulez maintenant la supprimer, consultez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="69c07-106">If you're developing a Microsoft Edge extension and want to load it up, or if you already have and now want to remove it, check out the steps below.</span></span>
<span data-ttu-id="69c07-107">Vous y trouverez également des détails sur la modification de l'emplacement de l'icône de votre extension dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="69c07-107">Also included are details on how to change your extension icon's location in the browser.</span></span>

## <span data-ttu-id="69c07-108">Ajout d’une extension</span><span class="sxs-lookup"><span data-stu-id="69c07-108">Adding an extension</span></span>

1. <span data-ttu-id="69c07-109">Ouvrez Microsoft Edge et tapez «à propos de: indicateurs» dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="69c07-109">Open Microsoft Edge and type 'about:flags' into the address bar.</span></span>

2. <span data-ttu-id="69c07-110">Activez la case à cocher **Activer les fonctionnalités de développeur d’extension**.</span><span class="sxs-lookup"><span data-stu-id="69c07-110">Select the **Enable extension developer features** checkbox.</span></span>

   ![à propos de: indicateurs activer les fonctionnalités de développeur](./../media/sideload-aboutflags.png)
   > [!NOTE]
   > <span data-ttu-id="69c07-112">Si vous n’avez pas la mise à jour anniversaire Windows10 ou version ultérieure, cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="69c07-112">If you don't have the Windows 10 Anniversary Update or later, this option will not be available.</span></span>

3. <span data-ttu-id="69c07-113">Pour ouvrir le menu, sélectionnez **Plus (...)**.</span><span class="sxs-lookup"><span data-stu-id="69c07-113">Select **More (...)** to open the menu.</span></span>

   ![Bouton plus](./../media/morebutton.png)  

4. <span data-ttu-id="69c07-115">Dans le menu, sélectionnez **Extensions**.</span><span class="sxs-lookup"><span data-stu-id="69c07-115">Select **Extensions** from the menu.</span></span>

5. <span data-ttu-id="69c07-116">Sélectionnez le bouton **Charger une extension**.</span><span class="sxs-lookup"><span data-stu-id="69c07-116">Select the **Load extension** button.</span></span>

   ![sélection de charger une extension](./../media/sideload-load-extension.png)

6. <span data-ttu-id="69c07-118">Accédez au dossier de votre extension, puis sélectionnez le bouton **Sélectionner un dossier**.</span><span class="sxs-lookup"><span data-stu-id="69c07-118">Navigate to your extension's folder and select the  **Select folder** button.</span></span>
   ![sélection du dossier d’extension à charger](./../media/sideload-select-extension.png)
   > [!NOTE]
   > <span data-ttu-id="69c07-120">Si vous rencontrez un message d’erreur lors du chargement de votre extension, consultez la page [Résolution des problèmes](./../troubleshooting.md) pour obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="69c07-120">If you encounter an error message when loading your extension, refer to the [troubleshooting](./../troubleshooting.md) page for guidance.</span></span>


**<span data-ttu-id="69c07-121">Vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="69c07-121">You're all set!</span></span> <span data-ttu-id="69c07-122">Vous devez maintenant voir l’extension répertoriée dans le volet extension de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="69c07-122">You should now see the extension listed in Microsoft Edge's extension pane.</span></span>**

![extension dans le volet extension](./../media/sideload-extension-installed.png)

> [!NOTE]
> <span data-ttu-id="69c07-124">Les extensions non signées sont automatiquement désactivées lors du lancement ultérieur de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="69c07-124">Unsigned extensions are automatically turned off on subsequent launches of Microsoft Edge.</span></span> <span data-ttu-id="69c07-125">Lorsque le navigateur entre dans un état d’inactivité (après environ 10secondes d’inactivité), la notification suivante s’affiche au bas de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="69c07-125">When the browser enters an idle state (after approximately 10 seconds of inactivity) you will see the following notification at the bottom of the window.</span></span> ![<span data-ttu-id="69c07-126">notification risquée](./../media/riskynotification.png) Pour activer les extensions non signées, cliquez sur «Activer quand même».</span><span class="sxs-lookup"><span data-stu-id="69c07-126">risky notification](./../media/riskynotification.png) To turn on the unsigned extensions, click "Turn on anyway".</span></span>



## <span data-ttu-id="69c07-127">Déplacement du bouton d’extension</span><span class="sxs-lookup"><span data-stu-id="69c07-127">Moving the extension button</span></span>
<span data-ttu-id="69c07-128">Selon les paramètres de votre extension, celui-ci peut s’afficher dans le menu **Plus (...)**.</span><span class="sxs-lookup"><span data-stu-id="69c07-128">Depending on your extension's settings, it could appear in the **More (...)** menu.</span></span>

   ![menu actions-navigateur](./../media/browseraction.png)  


<span data-ttu-id="69c07-130">Si vous voulez déplacer le bouton hors du menu pour y accéder plus facilement:</span><span class="sxs-lookup"><span data-stu-id="69c07-130">If you want to move the button out of this menu for easier access:</span></span>

1. <span data-ttu-id="69c07-131">Cliquez avec le bouton droit sur le bouton d’extension.</span><span class="sxs-lookup"><span data-stu-id="69c07-131">Right-click the extension button.</span></span>

2. <span data-ttu-id="69c07-132">Sélectionnez **Afficher le bouton en regard de barre d’adresses**.</span><span class="sxs-lookup"><span data-stu-id="69c07-132">Select **Show button next to address bar**.</span></span>

   ![menu contextuel du navigateur](./../media/browseraction_contextmenu.png)  

<span data-ttu-id="69c07-134">Vous pouvez également effectuer cette opération à partir de la page Détails de l’extension:</span><span class="sxs-lookup"><span data-stu-id="69c07-134">Alternatively, you may do this from the extensions details page:</span></span>

1. <span data-ttu-id="69c07-135">Cliquez sur le bouton extension.</span><span class="sxs-lookup"><span data-stu-id="69c07-135">Click on the extension button.</span></span>
2. <span data-ttu-id="69c07-136">Activer **Afficher le bouton en regard de la barre d’adresses**.</span><span class="sxs-lookup"><span data-stu-id="69c07-136">Toggle **Show button next to address bar** to on.</span></span>

   ![bouton activer/désactiver le bouton bascule](./../media/show-button-toggle.png)

> [!NOTE]
> <span data-ttu-id="69c07-138">Vous pouvez toujours déplacer le bouton vers le menu **Plus (...)** en cliquant dessus avec le bouton droit et en désélectionnant la case à cocher **Afficher en regard de la barre d’adresses** ou en accédant à la page Détails de l’extension et en désactivant la case à cocher **Afficher le bouton en regard de la barre d’adresses**.</span><span class="sxs-lookup"><span data-stu-id="69c07-138">You can always move the button back to the **More (...)** menu by right-clicking it and unselecting **Show next to address bar** or by going to the extension details page and toggling **Show button next to address bar** to off.</span></span>


## <span data-ttu-id="69c07-139">Suppression d’une extension</span><span class="sxs-lookup"><span data-stu-id="69c07-139">Removing an extension</span></span>

1. <span data-ttu-id="69c07-140">Ouvrez MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="69c07-140">Open Microsoft Edge.</span></span>

2. <span data-ttu-id="69c07-141">Pour ouvrir le menu, sélectionnez **Plus (...)**.</span><span class="sxs-lookup"><span data-stu-id="69c07-141">Select **More (...)** to open the menu.</span></span>

3. <span data-ttu-id="69c07-142">Dans le menu, sélectionnez **Extensions**.</span><span class="sxs-lookup"><span data-stu-id="69c07-142">Select **Extensions** from the menu.</span></span>

4. <span data-ttu-id="69c07-143">Cliquez avec le bouton droit sur l’extension que vous voulez supprimer, puis sélectionnez **Supprimer**, ou sélectionnez l’extension et cliquez sur le bouton **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="69c07-143">Right-click the extension you want to remove and select **Remove**, or select the extension and click the **Remove** button.</span></span>

   ![menu actions-supprimer](./../media/remove.png)  

**<span data-ttu-id="69c07-145">L’extension doit disparaître de la liste dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="69c07-145">The extension should disappear from the list in Microsoft Edge.</span></span>**
