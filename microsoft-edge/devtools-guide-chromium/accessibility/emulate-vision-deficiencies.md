---
title: Émuler les déficiences de la vision dans Microsoft Edge DevTools (cécité des couleurs)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: b70499fa189d162fa7589966bab183f4c12f68f7
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843920"
---
# <span data-ttu-id="82ed7-103">Émuler les déficiences de la vision</span><span class="sxs-lookup"><span data-stu-id="82ed7-103">Emulate vision deficiencies</span></span>

<span data-ttu-id="82ed7-104">Pour mieux répondre aux besoins de vos utilisateurs grâce à la déficience de la [couleur][ColorblindawarenessMain] (en aveugle \), [Microsoft Edge devtools][MicrosoftEdgeDevTools] vous permet de simuler des défauts de vision spécifiques.</span><span class="sxs-lookup"><span data-stu-id="82ed7-104">To better meet the needs of your users with [color vision deficiency][ColorblindawarenessMain] \(color blindness\), [Microsoft Edge DevTools][MicrosoftEdgeDevTools] enable you to simulate specific color vision deficiencies.</span></span>  <span data-ttu-id="82ed7-105">L’outil **émuler les déficiences** de la vision simule les catégories suivantes.</span><span class="sxs-lookup"><span data-stu-id="82ed7-105">The **Emulate vision deficiencies** tool simulates the following categories.</span></span>  

| <span data-ttu-id="82ed7-106">Déficience de la vision couleur</span><span class="sxs-lookup"><span data-stu-id="82ed7-106">Color vision deficiency</span></span> | <span data-ttu-id="82ed7-107">Détails</span><span class="sxs-lookup"><span data-stu-id="82ed7-107">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="82ed7-108">Vision floue</span><span class="sxs-lookup"><span data-stu-id="82ed7-108">Blurred vision</span></span> | <span data-ttu-id="82ed7-109">L’utilisateur a des difficultés à se focaliser sur des détails précis.</span><span class="sxs-lookup"><span data-stu-id="82ed7-109">The user has difficulty focusing on fine details.</span></span> |   
| <span data-ttu-id="82ed7-110">Protanopia</span><span class="sxs-lookup"><span data-stu-id="82ed7-110">Protanopia</span></span> | <span data-ttu-id="82ed7-111">L’utilisateur ne peut percevoir aucun éclairage rouge.</span><span class="sxs-lookup"><span data-stu-id="82ed7-111">The user is unable to perceive any red light.</span></span> |  
| <span data-ttu-id="82ed7-112">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="82ed7-112">Deuteranopia</span></span> | <span data-ttu-id="82ed7-113">L’utilisateur ne peut percevoir aucun éclairage vert.</span><span class="sxs-lookup"><span data-stu-id="82ed7-113">The user is unable to perceive any green light.</span></span> |  
| <span data-ttu-id="82ed7-114">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="82ed7-114">Tritanopia</span></span> | <span data-ttu-id="82ed7-115">L’utilisateur ne peut pas percevoir de lumière bleue.</span><span class="sxs-lookup"><span data-stu-id="82ed7-115">The user is unable to perceive any blue light.</span></span> |  
| <span data-ttu-id="82ed7-116">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="82ed7-116">Achromatopsia</span></span> | <span data-ttu-id="82ed7-117">L’utilisateur ne peut pas percevoir une couleur, ce qui réduit toute la couleur en nuance de gris.</span><span class="sxs-lookup"><span data-stu-id="82ed7-117">The user is unable to perceive any color, which reduces all color to a shade of grey.</span></span> |  

## <span data-ttu-id="82ed7-118">Accéder aux outils de rendu</span><span class="sxs-lookup"><span data-stu-id="82ed7-118">Navigate to the Rendering Tools</span></span>  

<span data-ttu-id="82ed7-119">Pour simuler une déficience de vision pour votre produit Web, ouvrez les [outils de rendu][RenderingTools].</span><span class="sxs-lookup"><span data-stu-id="82ed7-119">To simulate a vision deficiency being applied for your web product, open the [Rendering Tools][RenderingTools].</span></span>  

1.  <span data-ttu-id="82ed7-120">Ouvrir les outils de rendu en sélectionnant l' `...` élément de menu dans la barre d’outils</span><span class="sxs-lookup"><span data-stu-id="82ed7-120">Open the Rendering Tools by selecting the `...` menu item in the toolbar</span></span>  
1.  <span data-ttu-id="82ed7-121">Sélectionner</span><span class="sxs-lookup"><span data-stu-id="82ed7-121">Select</span></span> `More tools`  
1.  <span data-ttu-id="82ed7-122">Sélectionner</span><span class="sxs-lookup"><span data-stu-id="82ed7-122">Select</span></span> `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Ouverture des outils de rendu" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       <span data-ttu-id="82ed7-124">Ouverture des **outils de rendu**</span><span class="sxs-lookup"><span data-stu-id="82ed7-124">Opening the **Rendering Tools**</span></span>  
    :::image-end:::  

<span data-ttu-id="82ed7-125">Le menu **rendu** s’affiche dans le tiroir.</span><span class="sxs-lookup"><span data-stu-id="82ed7-125">The **Rendering** menu appears in the drawer.</span></span>  

1.  <span data-ttu-id="82ed7-126">Faites défiler vers le bas jusqu’à l' `Emulate vision deficiencies` élément de menu, puis sélectionnez le menu déroulant pour afficher les options.</span><span class="sxs-lookup"><span data-stu-id="82ed7-126">Scroll down to the `Emulate vision deficiencies` menu item and select the drop-down menu to display the options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Menu émuler les déficiences de la vision sur le tiroir de rendu" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       <span data-ttu-id="82ed7-128">Menu **émuler les déficiences** de la vision sur le tiroir de **rendu**</span><span class="sxs-lookup"><span data-stu-id="82ed7-128">The **Emulate vision deficiencies** menu on the **Rendering** drawer</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="82ed7-129">Choisissez une option.</span><span class="sxs-lookup"><span data-stu-id="82ed7-129">Choose an option.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Options de menu émuler la vision carences" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       <span data-ttu-id="82ed7-131">Options de menu **émuler la vision carences**</span><span class="sxs-lookup"><span data-stu-id="82ed7-131">The **Emulate vision deficiencies** menu options</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="82ed7-132">La fenêtre principale de Windows affiche la simulation de l’option sélectionnée appliquée à la page active.</span><span class="sxs-lookup"><span data-stu-id="82ed7-132">The main windows displays the simulation of your selected option applied to the current page.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Affichage à l’aide de \* \* vision floue \* \* simulation" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             <span data-ttu-id="82ed7-134">Affichage avec simulation de **vision floue**</span><span class="sxs-lookup"><span data-stu-id="82ed7-134">Display using **Blurred Vision** simulation</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Affichage à l’aide de \* \* achromatopsia \* \* simulation" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             <span data-ttu-id="82ed7-136">Affichage à l’aide de la simulation **achromatopsia**</span><span class="sxs-lookup"><span data-stu-id="82ed7-136">Display using **Achromatopsia** simulation</span></span> :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <span data-ttu-id="82ed7-137">Utiliser le menu de commandes</span><span class="sxs-lookup"><span data-stu-id="82ed7-137">Use the Command Menu</span></span>  

<span data-ttu-id="82ed7-138">Vous pouvez également utiliser le **menu de commandes** pour accéder aux différentes simulations.</span><span class="sxs-lookup"><span data-stu-id="82ed7-138">You may also use **Command Menu** to access the different simulations.</span></span>  

1.  <span data-ttu-id="82ed7-139">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.</span><span class="sxs-lookup"><span data-stu-id="82ed7-139">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menu de commandes" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="82ed7-141">**Menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="82ed7-141">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="82ed7-142">Tapez `emulate` , sélectionnez ce que vous voulez simuler et appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="82ed7-142">Type `emulate`, choose what you want to simulate and press `Enter`.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Différentes options de simulation disponibles dans le menu de commandes" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       <span data-ttu-id="82ed7-144">Différentes options de simulation disponibles dans le **menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="82ed7-144">The different simulation options available in the **Command Menu**</span></span>  
    :::image-end:::  
    
> [!IMPORTANT]
> <span data-ttu-id="82ed7-145">Les outils d’déficience de la **vision** simulent des approximations de la façon dont une personne avec chaque déficience risque de voir votre produit.</span><span class="sxs-lookup"><span data-stu-id="82ed7-145">The **Emulate vision deficiencies** tools simulate approximations of how a person with each deficiency may see your product.</span></span>  <span data-ttu-id="82ed7-146">Chaque personne est différente, par conséquent, les déficiences de vision varient en fonction du niveau de gravité d’une personne à l’autre.</span><span class="sxs-lookup"><span data-stu-id="82ed7-146">Each person is different, therefore vision deficiencies vary in severity from person to person.</span></span>  <span data-ttu-id="82ed7-147">Pour mieux répondre aux besoins de vos utilisateurs, évitez les combinaisons de couleurs susceptibles de résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="82ed7-147">To better meet the needs of your users, avoid any color combination that may be an issue.</span></span>  <span data-ttu-id="82ed7-148">Les outils d’déficience de la **vision** ne constituent pas une évaluation complète de votre produit.</span><span class="sxs-lookup"><span data-stu-id="82ed7-148">The **Emulate vision deficiencies** tools are not a full accessibility assessment of your product.</span></span>  <span data-ttu-id="82ed7-149">Au lieu de cela, les outils **émuler les déficiences** de la vision doivent vous offrir une bonne première étape pour éviter les problèmes.</span><span class="sxs-lookup"><span data-stu-id="82ed7-149">Instead, the **Emulate vision deficiencies** tools should  give you a good first step to avoid problems.</span></span>  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome)"  
[ColorblindawarenessMain]: http://www.colourblindawareness.org "Organisme de sensibilisation couleur aveugle"  
[AmfcbMain]: https://www.amfcb.org "L’American Foundation pour les aveugles en couleur (AFCB)"  
[RenderingTools]: /microsoft-edge/devtools-guide-chromium/rendering-tools "Outils de rendu Microsoft Edge (chrome)"  
