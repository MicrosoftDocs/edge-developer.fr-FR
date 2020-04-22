---
description: Découvrez comment ajouter et supprimer des extensions, et déplacer le bouton d’une extension en regard de la barre d’adresse.
title: Ajout et suppression d’extensions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur, extension
ms.custom: seodec18
localization_priority: Priority
ms.openlocfilehash: fdc6950962e7ce7e0a720d0bafa7e2c63ebd7098
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565364"
---
# <span data-ttu-id="dddae-104">Ajout, déplacement et suppression d’extensions pour Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="dddae-104">Adding, moving, and removing extensions for Microsoft Edge</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="dddae-105">La prise en charge de Microsoft Edge pour extensions a été introduite dans la **mise à jour anniversaire Windows 10**.</span><span class="sxs-lookup"><span data-stu-id="dddae-105">Microsoft Edge support for extensions was introduced in the **Windows 10 Anniversary Update**.</span></span> <span data-ttu-id="dddae-106">Si vous développez une extension Microsoft Edge et que vous souhaitez la charger, ou si vous souhaitez la supprimer maintenant, consultez les étapes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="dddae-106">If you're developing a Microsoft Edge extension and want to load it up, or if you already have and now want to remove it, check out the steps below.</span></span>
<span data-ttu-id="dddae-107">Vous trouverez également des informations sur la façon de modifier l’emplacement de l’icône d’extension dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="dddae-107">Also included are details on how to change your extension icon's location in the browser.</span></span>

## <span data-ttu-id="dddae-108">Ajout d’une extension</span><span class="sxs-lookup"><span data-stu-id="dddae-108">Adding an extension</span></span>

1. <span data-ttu-id="dddae-109">Ouvrez Microsoft Edge et tapez «à propos de: indicateurs» dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="dddae-109">Open Microsoft Edge and type 'about:flags' into the address bar.</span></span>

2. <span data-ttu-id="dddae-110">Cochez la case **activer les fonctionnalités de développement d’extensions** .</span><span class="sxs-lookup"><span data-stu-id="dddae-110">Select the **Enable extension developer features** checkbox.</span></span>

   ![à propos: indicateurs activez les fonctionnalités de développement](./../media/sideload-aboutflags.png)
   > [!NOTE]
   > <span data-ttu-id="dddae-112">Si vous n’avez pas la mise à jour anniversaire Windows 10 ou version ultérieure, cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="dddae-112">If you don't have the Windows 10 Anniversary Update or later, this option will not be available.</span></span>

3. <span data-ttu-id="dddae-113">Sélectionnez **plus (...)** pour ouvrir le menu.</span><span class="sxs-lookup"><span data-stu-id="dddae-113">Select **More (...)** to open the menu.</span></span>

   ![bouton plus](./../media/morebutton.png)  

4. <span data-ttu-id="dddae-115">Sélectionnez **Extensions** dans le menu.</span><span class="sxs-lookup"><span data-stu-id="dddae-115">Select **Extensions** from the menu.</span></span>

5. <span data-ttu-id="dddae-116">Cliquez sur le bouton **charger une extension** .</span><span class="sxs-lookup"><span data-stu-id="dddae-116">Select the **Load extension** button.</span></span>

   ![sélection de l’extension de chargement](./../media/sideload-load-extension.png)

6. <span data-ttu-id="dddae-118">Accédez au dossier de votre extension et sélectionnez le bouton **Sélectionner un dossier** .</span><span class="sxs-lookup"><span data-stu-id="dddae-118">Navigate to your extension's folder and select the  **Select folder** button.</span></span>
   ![sélection du dossier d’extension à charger](./../media/sideload-select-extension.png)
   > [!NOTE]
   > <span data-ttu-id="dddae-120">Si vous rencontrez un message d’erreur lors du chargement de votre extension, reportez-vous à la page de [résolution des problèmes](./../troubleshooting.md) .</span><span class="sxs-lookup"><span data-stu-id="dddae-120">If you encounter an error message when loading your extension, refer to the [troubleshooting](./../troubleshooting.md) page for guidance.</span></span>


**<span data-ttu-id="dddae-121">Voilà, c’est fini!</span><span class="sxs-lookup"><span data-stu-id="dddae-121">You're all set!</span></span> <span data-ttu-id="dddae-122">L’extension doit maintenant apparaître dans le volet extension de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="dddae-122">You should now see the extension listed in Microsoft Edge's extension pane.</span></span>**

![extension dans le volet extension](./../media/sideload-extension-installed.png)

> [!NOTE]
> <span data-ttu-id="dddae-124">Les extensions non signées sont automatiquement désactivées lors du lancement ultérieur de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="dddae-124">Unsigned extensions are automatically turned off on subsequent launches of Microsoft Edge.</span></span> <span data-ttu-id="dddae-125">Lorsque le navigateur passe à un état inactif (au bout de 10 secondes d’inactivité), vous verrez la notification suivante en bas de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="dddae-125">When the browser enters an idle state (after approximately 10 seconds of inactivity) you will see the following notification at the bottom of the window.</span></span> ![<span data-ttu-id="dddae-126">notification](./../media/riskynotification.png) risquée pour activer les extensions non signées, cliquez sur «Activer quand même».</span><span class="sxs-lookup"><span data-stu-id="dddae-126">risky notification](./../media/riskynotification.png) To turn on the unsigned extensions, click "Turn on anyway".</span></span>



## <span data-ttu-id="dddae-127">Déplacement du bouton extension</span><span class="sxs-lookup"><span data-stu-id="dddae-127">Moving the extension button</span></span>
<span data-ttu-id="dddae-128">En fonction des paramètres de votre extension, il est possible qu’elle apparaisse dans le menu **plus (...)** .</span><span class="sxs-lookup"><span data-stu-id="dddae-128">Depending on your extension's settings, it could appear in the **More (...)** menu.</span></span>

   ![menu actions](./../media/browseraction.png)  


<span data-ttu-id="dddae-130">Pour plus d’informations sur le déplacement du menu, voir:</span><span class="sxs-lookup"><span data-stu-id="dddae-130">If you want to move the button out of this menu for easier access:</span></span>

1. <span data-ttu-id="dddae-131">Cliquez avec le bouton droit sur le bouton extension.</span><span class="sxs-lookup"><span data-stu-id="dddae-131">Right-click the extension button.</span></span>

2. <span data-ttu-id="dddae-132">Sélectionner le **bouton afficher en regard de la barre d’adresse**.</span><span class="sxs-lookup"><span data-stu-id="dddae-132">Select **Show button next to address bar**.</span></span>

   ![menu actions](./../media/browseraction_contextmenu.png)  

<span data-ttu-id="dddae-134">Vous pouvez également effectuer cette opération à partir de la page Détails de l’extension:</span><span class="sxs-lookup"><span data-stu-id="dddae-134">Alternatively, you may do this from the extensions details page:</span></span>

1. <span data-ttu-id="dddae-135">Cliquez sur le bouton extension.</span><span class="sxs-lookup"><span data-stu-id="dddae-135">Click on the extension button.</span></span>
2. <span data-ttu-id="dddae-136">Activer/désactiver le **bouton afficher en regard de la barre d’adresse** .</span><span class="sxs-lookup"><span data-stu-id="dddae-136">Toggle **Show button next to address bar** to on.</span></span>

   ![bouton bascule bouton bascule activé](./../media/show-button-toggle.png)

> [!NOTE]
> <span data-ttu-id="dddae-138">Vous pouvez toujours déplacer le bouton dans le menu **autres (...)** en cliquant dessus avec le bouton droit et en désélectionnant **afficher en regard de la barre d’adresse** ou en accédant à la page Détails de l’extension et en activant le **bouton afficher en regard de la barre d’adresses** .</span><span class="sxs-lookup"><span data-stu-id="dddae-138">You can always move the button back to the **More (...)** menu by right-clicking it and unselecting **Show next to address bar** or by going to the extension details page and toggling **Show button next to address bar** to off.</span></span>


## <span data-ttu-id="dddae-139">Suppression d’une extension</span><span class="sxs-lookup"><span data-stu-id="dddae-139">Removing an extension</span></span>

1. <span data-ttu-id="dddae-140">Ouvrez MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="dddae-140">Open Microsoft Edge.</span></span>

2. <span data-ttu-id="dddae-141">Sélectionnez **plus (...)** pour ouvrir le menu.</span><span class="sxs-lookup"><span data-stu-id="dddae-141">Select **More (...)** to open the menu.</span></span>

3. <span data-ttu-id="dddae-142">Sélectionnez **Extensions** dans le menu.</span><span class="sxs-lookup"><span data-stu-id="dddae-142">Select **Extensions** from the menu.</span></span>

4. <span data-ttu-id="dddae-143">Cliquez avec le bouton droit sur l’extension que vous voulez supprimer, sélectionnez **supprimer**, ou sélectionnez l’extension, puis cliquez sur le bouton **supprimer** .</span><span class="sxs-lookup"><span data-stu-id="dddae-143">Right-click the extension you want to remove and select **Remove**, or select the extension and click the **Remove** button.</span></span>

   ![menu actions](./../media/remove.png)  

**<span data-ttu-id="dddae-145">L’extension doit disparaître de la liste dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="dddae-145">The extension should disappear from the list in Microsoft Edge.</span></span>**
