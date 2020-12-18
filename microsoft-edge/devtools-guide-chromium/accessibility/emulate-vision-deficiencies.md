---
description: Émuler les déficiences de la vision dans Microsoft Edge DevTools.
title: Émuler les déficiences de la vision dans Microsoft Edge DevTools (cécité des couleurs)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 5343d32992880f8c60501a86db6cb3a92f417331
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230823"
---
# <span data-ttu-id="1510f-104">Émuler les faiblesses de la vision</span><span class="sxs-lookup"><span data-stu-id="1510f-104">Emulate vision deficiencies</span></span>

<span data-ttu-id="1510f-105">Pour mieux répondre aux besoins de vos utilisateurs grâce à la déficience de la [couleur][ColorblindawarenessMain] (en aveugle \), [Microsoft Edge devtools][DevtoolsIndex] vous permet de simuler des défauts de vision spécifiques.</span><span class="sxs-lookup"><span data-stu-id="1510f-105">To better meet the needs of your users with [color vision deficiency][ColorblindawarenessMain] \(color blindness\), [Microsoft Edge DevTools][DevtoolsIndex] enable you to simulate specific color vision deficiencies.</span></span>  <span data-ttu-id="1510f-106">L’outil **émuler les déficiences** de la vision simule les catégories suivantes.</span><span class="sxs-lookup"><span data-stu-id="1510f-106">The **Emulate vision deficiencies** tool simulates the following categories.</span></span>  

| <span data-ttu-id="1510f-107">Déficience de la vision couleur</span><span class="sxs-lookup"><span data-stu-id="1510f-107">Color vision deficiency</span></span> | <span data-ttu-id="1510f-108">Détails</span><span class="sxs-lookup"><span data-stu-id="1510f-108">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="1510f-109">Vision floue</span><span class="sxs-lookup"><span data-stu-id="1510f-109">Blurred vision</span></span> | <span data-ttu-id="1510f-110">L’utilisateur a des difficultés à se focaliser sur des détails précis.</span><span class="sxs-lookup"><span data-stu-id="1510f-110">The user has difficulty focusing on fine details.</span></span> |   
| <span data-ttu-id="1510f-111">Protanopia</span><span class="sxs-lookup"><span data-stu-id="1510f-111">Protanopia</span></span> | <span data-ttu-id="1510f-112">L’utilisateur ne peut percevoir aucun éclairage rouge.</span><span class="sxs-lookup"><span data-stu-id="1510f-112">The user is unable to perceive any red light.</span></span> |  
| <span data-ttu-id="1510f-113">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="1510f-113">Deuteranopia</span></span> | <span data-ttu-id="1510f-114">L’utilisateur ne peut percevoir aucun éclairage vert.</span><span class="sxs-lookup"><span data-stu-id="1510f-114">The user is unable to perceive any green light.</span></span> |  
| <span data-ttu-id="1510f-115">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="1510f-115">Tritanopia</span></span> | <span data-ttu-id="1510f-116">L’utilisateur ne peut pas percevoir de lumière bleue.</span><span class="sxs-lookup"><span data-stu-id="1510f-116">The user is unable to perceive any blue light.</span></span> |  
| <span data-ttu-id="1510f-117">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="1510f-117">Achromatopsia</span></span> | <span data-ttu-id="1510f-118">L’utilisateur ne peut pas percevoir une couleur, ce qui réduit toute la couleur en nuance de gris.</span><span class="sxs-lookup"><span data-stu-id="1510f-118">The user is unable to perceive any color, which reduces all color to a shade of grey.</span></span> |  

## <span data-ttu-id="1510f-119">Accéder aux outils de rendu</span><span class="sxs-lookup"><span data-stu-id="1510f-119">Navigate to the Rendering Tools</span></span>  

<span data-ttu-id="1510f-120">Pour simuler une déficience de vision pour votre produit Web, ouvrez les [outils de rendu][DevtoolsRenderingToolsIndex].</span><span class="sxs-lookup"><span data-stu-id="1510f-120">To simulate a vision deficiency being applied for your web product, open the [Rendering Tools][DevtoolsRenderingToolsIndex].</span></span>  

1.  <span data-ttu-id="1510f-121">Pour ouvrir les outils de rendu, en choisissant l' `...` élément de menu dans la barre d’outils</span><span class="sxs-lookup"><span data-stu-id="1510f-121">To open the Rendering Tools, by choose the `...` menu item in the toolbar</span></span>  
1.  <span data-ttu-id="1510f-122">Choisir</span><span class="sxs-lookup"><span data-stu-id="1510f-122">Choose</span></span> `More tools`  
1.  <span data-ttu-id="1510f-123">Choisir</span><span class="sxs-lookup"><span data-stu-id="1510f-123">Choose</span></span> `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Ouverture des outils de rendu" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       <span data-ttu-id="1510f-125">Ouverture des **outils de rendu**</span><span class="sxs-lookup"><span data-stu-id="1510f-125">Opening the **Rendering Tools**</span></span>  
    :::image-end:::  

<span data-ttu-id="1510f-126">Le menu **rendu** s’affiche dans le tiroir.</span><span class="sxs-lookup"><span data-stu-id="1510f-126">The **Rendering** menu appears in the drawer.</span></span>  

1.  <span data-ttu-id="1510f-127">Faites défiler vers le bas jusqu’à l' `Emulate vision deficiencies` élément de menu, puis sélectionnez le menu déroulant pour afficher les options.</span><span class="sxs-lookup"><span data-stu-id="1510f-127">Scroll down to the `Emulate vision deficiencies` menu item and choose the drop-down menu to display the options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Menu émuler les déficiences de la vision sur le tiroir de rendu" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       <span data-ttu-id="1510f-129">Menu **émuler les déficiences** de la vision sur le tiroir de **rendu**</span><span class="sxs-lookup"><span data-stu-id="1510f-129">The **Emulate vision deficiencies** menu on the **Rendering** drawer</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1510f-130">Choisissez une option.</span><span class="sxs-lookup"><span data-stu-id="1510f-130">Choose an option.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Options de menu émuler la vision carences" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       <span data-ttu-id="1510f-132">Options de menu **émuler la vision carences**</span><span class="sxs-lookup"><span data-stu-id="1510f-132">The **Emulate vision deficiencies** menu options</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1510f-133">La fenêtre principale de Windows affiche la simulation de l’option choisie appliquée à la page active.</span><span class="sxs-lookup"><span data-stu-id="1510f-133">The main windows displays the simulation of your chosen option applied to the current page.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Affichage à l’aide de \* \* vision floue \* \* simulation" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             <span data-ttu-id="1510f-135">Affichage avec simulation de **vision floue**</span><span class="sxs-lookup"><span data-stu-id="1510f-135">Display using **Blurred Vision** simulation</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Affichage à l’aide de \* \* achromatopsia \* \* simulation" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             <span data-ttu-id="1510f-137">Affichage à l’aide de la simulation **achromatopsia**</span><span class="sxs-lookup"><span data-stu-id="1510f-137">Display using **Achromatopsia** simulation</span></span> :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <span data-ttu-id="1510f-138">Utiliser le menu de commandes</span><span class="sxs-lookup"><span data-stu-id="1510f-138">Use the Command Menu</span></span>  

<span data-ttu-id="1510f-139">Vous pouvez également utiliser le **menu de commandes** pour accéder aux différentes simulations.</span><span class="sxs-lookup"><span data-stu-id="1510f-139">You may also use **Command Menu** to access the different simulations.</span></span>  

1.  <span data-ttu-id="1510f-140">Sélectionnez `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.</span><span class="sxs-lookup"><span data-stu-id="1510f-140">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menu de commandes" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="1510f-142">**Menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="1510f-142">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1510f-143">Tapez `emulate` , sélectionnez ce que vous voulez simuler et sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="1510f-143">Type `emulate`, choose what you want to simulate and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Différentes options de simulation disponibles dans le menu de commandes" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       <span data-ttu-id="1510f-145">Différentes options de simulation disponibles dans le **menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="1510f-145">The different simulation options available in the **Command Menu**</span></span>  
    :::image-end:::  
    
> [!IMPORTANT]
> <span data-ttu-id="1510f-146">Les outils d’déficience de la **vision** simulent des approximations de la façon dont une personne avec chaque déficience risque de voir votre produit.</span><span class="sxs-lookup"><span data-stu-id="1510f-146">The **Emulate vision deficiencies** tools simulate approximations of how a person with each deficiency may see your product.</span></span>  <span data-ttu-id="1510f-147">Chaque personne est différente, par conséquent, les déficiences de vision varient en fonction du niveau de gravité d’une personne à l’autre.</span><span class="sxs-lookup"><span data-stu-id="1510f-147">Each person is different, therefore vision deficiencies vary in severity from person to person.</span></span>  <span data-ttu-id="1510f-148">Pour mieux répondre aux besoins de vos utilisateurs, évitez les combinaisons de couleurs susceptibles de résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="1510f-148">To better meet the needs of your users, avoid any color combination that may be an issue.</span></span>  <span data-ttu-id="1510f-149">Les outils d’déficience de la **vision** ne constituent pas une évaluation complète de votre produit.</span><span class="sxs-lookup"><span data-stu-id="1510f-149">The **Emulate vision deficiencies** tools are not a full accessibility assessment of your product.</span></span>  <span data-ttu-id="1510f-150">Au lieu de cela, les outils **émuler les déficiences** de la vision doivent vous offrir une bonne première étape pour éviter les problèmes.</span><span class="sxs-lookup"><span data-stu-id="1510f-150">Instead, the **Emulate vision deficiencies** tools should  give you a good first step to avoid problems.</span></span>  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  
[DevtoolsRenderingToolsIndex]: ../rendering-tools/index.md "Analyser les performances au moment de l’exécution | Documents Microsoft"  

[ColorblindawarenessMain]: http://www.colourblindawareness.org "Organisme de sensibilisation couleur aveugle"  

[AmfcbMain]: https://www.amfcb.org "L’American Foundation pour les aveugles en couleur (AFCB)"  

