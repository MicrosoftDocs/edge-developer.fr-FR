---
title: Émuler les déficiences de la vision dans Microsoft Edge DevTools (cécité des couleurs)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 0b608f5fe67724eee81aeb993577ee9b45cbca09
ms.sourcegitcommit: d7fdb67df0fe73fa5ae96e5a69a847d07941d0a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2020
ms.locfileid: "10758084"
---
# <span data-ttu-id="34419-103">Émuler les déficiences de la vision</span><span class="sxs-lookup"><span data-stu-id="34419-103">Emulate vision deficiencies</span></span>

<span data-ttu-id="34419-104">Dans le monde entier, environ 8% des hommes et 0,5% des femmes présentent un déficience de la vision de la [couleur][ColorblindawarenessMain] qui est souvent appelée «cécité en couleur».</span><span class="sxs-lookup"><span data-stu-id="34419-104">Worldwide approximately 8% of men and 0.5% of women have a [color vision deficiency][ColorblindawarenessMain] commonly named "Color Blindness".</span></span>  <span data-ttu-id="34419-105">[Microsoft Edge devtools][MicrosoftEdgeDevTools] vous permet d’émuler différentes déficiences connues et de fournir un aperçu de votre produit pour vous permettre de le consulter.</span><span class="sxs-lookup"><span data-stu-id="34419-105">[Microsoft Edge DevTools][MicrosoftEdgeDevTools] enables you to emulate various known deficiencies and provide a preview of your product for you to review.</span></span>  

| <span data-ttu-id="34419-106">Déficience de la couleur</span><span class="sxs-lookup"><span data-stu-id="34419-106">Color Deficiency</span></span> | <span data-ttu-id="34419-107">Détails</span><span class="sxs-lookup"><span data-stu-id="34419-107">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="34419-108">Vision floue</span><span class="sxs-lookup"><span data-stu-id="34419-108">Blurred vision</span></span> |  |   
| <span data-ttu-id="34419-109">Protanopia</span><span class="sxs-lookup"><span data-stu-id="34419-109">Protanopia</span></span> | <span data-ttu-id="34419-110">L’impossibilité de percevoir des lumières rouges.</span><span class="sxs-lookup"><span data-stu-id="34419-110">The inability to perceive any red light.</span></span> |  
| <span data-ttu-id="34419-111">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="34419-111">Deuteranopia</span></span> | <span data-ttu-id="34419-112">L’impossibilité de percevoir une lumière verte.</span><span class="sxs-lookup"><span data-stu-id="34419-112">The inability to perceive any green light.</span></span> |  
| <span data-ttu-id="34419-113">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="34419-113">Tritanopia</span></span> | <span data-ttu-id="34419-114">L’impossibilité de percevoir une lumière bleue.</span><span class="sxs-lookup"><span data-stu-id="34419-114">The inability to perceive any blue light.</span></span> |  
| <span data-ttu-id="34419-115">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="34419-115">Achromatopsia</span></span> | <span data-ttu-id="34419-116">L’impossibilité de percevoir une couleur, à l’exception des nuances de gris.</span><span class="sxs-lookup"><span data-stu-id="34419-116">The inability to perceive any color, except for shades of grey.</span></span> |  

## <span data-ttu-id="34419-117">Accéder aux outils de rendu</span><span class="sxs-lookup"><span data-stu-id="34419-117">Navigate to the Rendering Tools</span></span>  

<span data-ttu-id="34419-118">Pour tester votre produit Web actuel à des fins de coloration, ouvrez les [outils de rendu][RenderingTools].</span><span class="sxs-lookup"><span data-stu-id="34419-118">To test your current web product for color deficiencies, open the [Rendering Tools][RenderingTools].</span></span>  

1.  <span data-ttu-id="34419-119">Ouvrir les outils de rendu en sélectionnant l' `...` élément de menu dans la barre d’outils</span><span class="sxs-lookup"><span data-stu-id="34419-119">Open the Rendering Tools by selecting the `...` menu item in the toolbar</span></span>  
1.  <span data-ttu-id="34419-120">Sélectionner</span><span class="sxs-lookup"><span data-stu-id="34419-120">Select</span></span> `More tools`  
1.  <span data-ttu-id="34419-121">Sélectionner</span><span class="sxs-lookup"><span data-stu-id="34419-121">Select</span></span> `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Ouverture des outils de rendu" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       <span data-ttu-id="34419-123">Ouverture des **outils de rendu**</span><span class="sxs-lookup"><span data-stu-id="34419-123">Opening the **Rendering Tools**</span></span>  
    :::image-end:::  

<span data-ttu-id="34419-124">Le menu de **rendu** s’affiche dans la partie inférieure du devtools.</span><span class="sxs-lookup"><span data-stu-id="34419-124">The **Rendering** menu appears in the bottom half of the DevTools.</span></span>  

1.  <span data-ttu-id="34419-125">Faites défiler vers le bas jusqu’à l' `Emulate Vision deficiencies` élément de menu, puis sélectionnez l’une des options proposées.</span><span class="sxs-lookup"><span data-stu-id="34419-125">Scroll down to the `Emulate Vision deficiencies` menu item and select from the options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Menu émuler les déficiences de la vision des outils de rendu" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       <span data-ttu-id="34419-127">Menu **émuler les déficiences** de la vision des outils de **rendu**</span><span class="sxs-lookup"><span data-stu-id="34419-127">The **Emulate Vision Deficiencies** menu of the **Rendering** tools</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="34419-128">Choisir une des options</span><span class="sxs-lookup"><span data-stu-id="34419-128">Choose any of the options</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Options de menu émuler la vision carences" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       <span data-ttu-id="34419-130">Options de menu **émuler la vision carences**</span><span class="sxs-lookup"><span data-stu-id="34419-130">The **Emulate Vision Deficiencies** menu options</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="34419-131">La page actuelle s’affiche dans une simulation de la façon dont elle peut s’afficher à l’utilisateur présentant le déficience choisie.</span><span class="sxs-lookup"><span data-stu-id="34419-131">The current page is displayed in a simulation of how it may appear to a user with the chosen deficiency.</span></span>  

    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Documentation des outils de développement Microsoft Edge dans l’émulation de vision floue" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             <span data-ttu-id="34419-133">Affichage à l’aide d’une émulation de **vision floue**</span><span class="sxs-lookup"><span data-stu-id="34419-133">Displayed using **Blurred Vision** emulation</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Documentation des outils de développement Microsoft Edge dans l’émulation de vision achromatopsia" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             <span data-ttu-id="34419-135">Affichage à l’aide de l’émulation de **vision achromatopsia**</span><span class="sxs-lookup"><span data-stu-id="34419-135">Display using **Achromatopsia Vision** emulation</span></span> :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <span data-ttu-id="34419-136">Utiliser le menu de commandes</span><span class="sxs-lookup"><span data-stu-id="34419-136">Using the command menu</span></span>  

<span data-ttu-id="34419-137">Vous pouvez également accéder aux différentes émulations sans utiliser les différents menus du menu de **commandes**.</span><span class="sxs-lookup"><span data-stu-id="34419-137">You may also reach the different emulations without going through the various menus using the **Command Menu**.</span></span>  

1.  <span data-ttu-id="34419-138">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.</span><span class="sxs-lookup"><span data-stu-id="34419-138">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menu de commandes" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="34419-140">**Menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="34419-140">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="34419-141">Tapez `emulate` , sélectionnez ce que vous voulez simuler et appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="34419-141">Type `emulate`, choose what you want to simulate and press `Enter`.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Différentes options d’émulation disponibles dans le menu de commandes" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       <span data-ttu-id="34419-143">Différentes options d’émulation disponibles dans le **menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="34419-143">The different emulation options available in the **Command Menu**</span></span>  
    :::image-end:::  
    
> [!IMPORTANT]
> <span data-ttu-id="34419-144">Les outils d’émulation sont des approximations de la façon dont une personne avec chaque déficience risque de voir votre produit.</span><span class="sxs-lookup"><span data-stu-id="34419-144">The emulation tools are approximations of how a person with each deficiency may see your product.</span></span>  <span data-ttu-id="34419-145">Chaque personne est différente, par conséquent, les déficiences de vision varient en fonction du niveau de gravité d’une personne à l’autre.</span><span class="sxs-lookup"><span data-stu-id="34419-145">Each person is different, therefore vision deficiencies vary in severity from person to person.</span></span>  <span data-ttu-id="34419-146">Pour mieux répondre aux besoins de vos utilisateurs, évitez les combinaisons de couleurs susceptibles de résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="34419-146">To better meet the needs of your users, avoid any color combination that may be an issue.</span></span>  <span data-ttu-id="34419-147">Les outils d’émulation ne retrouvent pas une évaluation complète de l’accessibilité de votre produit, mais il est recommandé de commencer par une bonne étape pour éviter les défauts les plus importants.</span><span class="sxs-lookup"><span data-stu-id="34419-147">The emulation tools are not a full assessment of the accessibility of your product, but you should have a good first step towards avoiding the biggest deficiencies.</span></span>  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome)"  
[ColorblindawarenessMain]: http://www.colourblindawareness.org "Organisme de sensibilisation couleur aveugle"  
[AmfcbMain]: https://www.amfcb.org "L’American Foundation pour les aveugles en couleur (AFCB)"  
[RenderingTools]: /microsoft-edge/devtools-guide-chromium/rendering-tools "Outils de rendu Microsoft Edge (chrome)"  
