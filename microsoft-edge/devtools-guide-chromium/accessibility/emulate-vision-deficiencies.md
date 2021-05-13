---
description: Émuler les défaillances visuelles dans Microsoft Edge DevTools.
title: Émuler les défaillances visuelles dans Microsoft Edge DevTools (daltonisme)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 1ab224f1dc70618dbef77ec6e6dbc22a0d1f47fb
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564601"
---
# <a name="emulate-vision-deficiencies"></a><span data-ttu-id="13d06-104">Émuler les faiblesses de la vision</span><span class="sxs-lookup"><span data-stu-id="13d06-104">Emulate vision deficiencies</span></span>  

<span data-ttu-id="13d06-105">Pour mieux répondre aux besoins de vos utilisateurs ayant des problèmes de [vision][ColorblindawarenessMain] des couleurs \(daltonisme),Microsoft Edge [DevTools][DevtoolsIndex] vous permet de simuler des défaillances de vision de couleur spécifiques.</span><span class="sxs-lookup"><span data-stu-id="13d06-105">To better meet the needs of your users with [color vision deficiency][ColorblindawarenessMain] \(color blindness\), [Microsoft Edge DevTools][DevtoolsIndex] allow you to simulate specific color vision deficiencies.</span></span>  <span data-ttu-id="13d06-106">**L’outil Émuler les défauts de vision** simule les catégories suivantes.</span><span class="sxs-lookup"><span data-stu-id="13d06-106">The **Emulate vision deficiencies** tool simulates the following categories.</span></span>  

| <span data-ttu-id="13d06-107">Problèmes de vision des couleurs</span><span class="sxs-lookup"><span data-stu-id="13d06-107">Color vision deficiency</span></span> | <span data-ttu-id="13d06-108">Détails</span><span class="sxs-lookup"><span data-stu-id="13d06-108">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="13d06-109">Vision floue</span><span class="sxs-lookup"><span data-stu-id="13d06-109">Blurred vision</span></span> | <span data-ttu-id="13d06-110">L’utilisateur a des difficultés à se concentrer sur des détails précis.</span><span class="sxs-lookup"><span data-stu-id="13d06-110">The user has difficulty focusing on fine details.</span></span> |  
| <span data-ttu-id="13d06-111">Protanopia</span><span class="sxs-lookup"><span data-stu-id="13d06-111">Protanopia</span></span> | <span data-ttu-id="13d06-112">L’utilisateur ne peut pas percevoir de lumière rouge.</span><span class="sxs-lookup"><span data-stu-id="13d06-112">The user is unable to perceive any red light.</span></span> |  
| <span data-ttu-id="13d06-113">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="13d06-113">Deuteranopia</span></span> | <span data-ttu-id="13d06-114">L’utilisateur ne peut pas percevoir de lumière verte.</span><span class="sxs-lookup"><span data-stu-id="13d06-114">The user is unable to perceive any green light.</span></span> |  
| <span data-ttu-id="13d06-115">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="13d06-115">Tritanopia</span></span> | <span data-ttu-id="13d06-116">L’utilisateur ne parvient pas à percevoir la lumière bleue.</span><span class="sxs-lookup"><span data-stu-id="13d06-116">The user is unable to perceive any blue light.</span></span> |  
| <span data-ttu-id="13d06-117">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="13d06-117">Achromatopsia</span></span> | <span data-ttu-id="13d06-118">L’utilisateur ne peut percevoir aucune couleur, ce qui réduit toutes les couleurs à une nuance de gris.</span><span class="sxs-lookup"><span data-stu-id="13d06-118">The user is unable to perceive any color, which reduces all color to a shade of grey.</span></span> |  

## <a name="navigate-to-the-rendering-tools"></a><span data-ttu-id="13d06-119">Accéder aux outils de rendu</span><span class="sxs-lookup"><span data-stu-id="13d06-119">Navigate to the Rendering Tools</span></span>  

<span data-ttu-id="13d06-120">Pour simuler une défaillance visuelle appliquée à votre produit web, ouvrez les [outils de rendu.][DevtoolsRenderingToolsIndex]</span><span class="sxs-lookup"><span data-stu-id="13d06-120">To simulate a vision deficiency being applied for your web product, open the [Rendering Tools][DevtoolsRenderingToolsIndex].</span></span>  

1.  <span data-ttu-id="13d06-121">Pour ouvrir les outils de rendu, choisissez `...` l’élément de menu dans la barre d’outils</span><span class="sxs-lookup"><span data-stu-id="13d06-121">To open the Rendering Tools, choose the `...` menu item in the toolbar</span></span>  
1.  <span data-ttu-id="13d06-122">Choisir **d’autres outils**</span><span class="sxs-lookup"><span data-stu-id="13d06-122">Choose **More tools**</span></span>  
1.  <span data-ttu-id="13d06-123">Choisir le **rendu**</span><span class="sxs-lookup"><span data-stu-id="13d06-123">Choose **Rendering**</span></span>  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Ouverture des outils de rendu" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       <span data-ttu-id="13d06-125">Ouverture des **outils de rendu**</span><span class="sxs-lookup"><span data-stu-id="13d06-125">Opening the **Rendering Tools**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="13d06-126">Le menu **Rendu** s’affiche dans le bac.</span><span class="sxs-lookup"><span data-stu-id="13d06-126">The **Rendering** menu appears in the drawer.</span></span>  

1.  <span data-ttu-id="13d06-127">Faites défiler vers le bas `Emulate vision deficiencies` jusqu’à l’élément de menu et choisissez le menu déroulant pour afficher les options.</span><span class="sxs-lookup"><span data-stu-id="13d06-127">Scroll down to the `Emulate vision deficiencies` menu item and choose the drop-down menu to display the options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Menu Émuler les défaillances de la vision dans le caisse de rendu" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       <span data-ttu-id="13d06-129">Le **menu Émuler les défaillances de** la vision dans le bac **de** rendu</span><span class="sxs-lookup"><span data-stu-id="13d06-129">The **Emulate vision deficiencies** menu on the **Rendering** drawer</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="13d06-130">Choisissez une option.</span><span class="sxs-lookup"><span data-stu-id="13d06-130">Choose an option.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Options du menu Émuler les défaillances de la vision" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       <span data-ttu-id="13d06-132">La **vision Émuler les options de** menu</span><span class="sxs-lookup"><span data-stu-id="13d06-132">The **Emulate vision deficiencies** menu options</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="13d06-133">La fenêtre principale affiche la simulation de l’option choisie appliquée à la page actuelle.</span><span class="sxs-lookup"><span data-stu-id="13d06-133">The main windows displays the simulation of your chosen option applied to the current page.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Afficher à l’aide de la simulation **Vision floue**" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             <span data-ttu-id="13d06-135">Afficher à **l’aide de la simulation de vision floue**</span><span class="sxs-lookup"><span data-stu-id="13d06-135">Display using **Blurred Vision** simulation</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Afficher à l’aide de la simulation **Achromatopsia**" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             <span data-ttu-id="13d06-137">Afficher à l’aide de la simulation **Achromatopsia**</span><span class="sxs-lookup"><span data-stu-id="13d06-137">Display using **Achromatopsia** simulation</span></span> :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <a name="use-the-command-menu"></a><span data-ttu-id="13d06-138">Utiliser le menu Commande</span><span class="sxs-lookup"><span data-stu-id="13d06-138">Use the Command Menu</span></span>  

<span data-ttu-id="13d06-139">Vous pouvez également utiliser le **menu Commande** pour accéder aux différentes simulations.</span><span class="sxs-lookup"><span data-stu-id="13d06-139">You may also use **Command Menu** to access the different simulations.</span></span>  

1.  <span data-ttu-id="13d06-140">Sélectionnez `Ctrl` + `Shift` + `P` \(Windows/Linux\) ou `Command` + `Shift` + `P` \(macOS\) pour ouvrir le **menu Commande.**</span><span class="sxs-lookup"><span data-stu-id="13d06-140">Select `Ctrl`+`Shift`+`P` \(Windows/Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menu Commande" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="13d06-142">Menu **Commande**</span><span class="sxs-lookup"><span data-stu-id="13d06-142">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="13d06-143">Tapez `emulate` , choisissez ce que vous souhaitez simuler et `Enter` choisissez.</span><span class="sxs-lookup"><span data-stu-id="13d06-143">Type `emulate`, choose what you want to simulate and choose `Enter`.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Les différentes options de simulation disponibles dans le menu Commande" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       <span data-ttu-id="13d06-145">Les différentes options de simulation disponibles dans le **menu Commande**</span><span class="sxs-lookup"><span data-stu-id="13d06-145">The different simulation options available in the **Command Menu**</span></span>  
    :::image-end:::  
    
> [!IMPORTANT]
> <span data-ttu-id="13d06-146">Les **outils Émuler les défauts** de vision simulent des estimations de la façon dont une personne atteinte de chaque défaillance peut voir votre produit.</span><span class="sxs-lookup"><span data-stu-id="13d06-146">The **Emulate vision deficiencies** tools simulate approximations of how a person with each deficiency may see your product.</span></span>  <span data-ttu-id="13d06-147">Chaque personne est différente, par conséquent les défaillances visuelles varient en gravité d’une personne à l’autre.</span><span class="sxs-lookup"><span data-stu-id="13d06-147">Each person is different, therefore vision deficiencies vary in severity from person to person.</span></span>  <span data-ttu-id="13d06-148">Pour mieux répondre aux besoins de vos utilisateurs, évitez toute combinaison de couleurs qui peut être un problème.</span><span class="sxs-lookup"><span data-stu-id="13d06-148">To better meet the needs of your users, avoid any color combination that may be an issue.</span></span>  <span data-ttu-id="13d06-149">Les **outils émuler les défaillances de vision** ne sont pas une évaluation complète de l’accessibilité de votre produit.</span><span class="sxs-lookup"><span data-stu-id="13d06-149">The **Emulate vision deficiencies** tools are not a full accessibility assessment of your product.</span></span>  <span data-ttu-id="13d06-150">Au lieu de cela, les **outils émuler** les défaillances de la vision doivent vous donner une bonne première étape pour éviter les problèmes.</span><span class="sxs-lookup"><span data-stu-id="13d06-150">Instead, the **Emulate vision deficiencies** tools should  give you a good first step to avoid problems.</span></span>  

<!-- links -->  

[DevToolsIndex]: ../index.md "Microsoft Edge outils de développement (Chromium) | Documents Microsoft"  
[DevtoolsRenderingToolsIndex]: ../rendering-tools/index.md "Analyser les performances d’exécution | Documents Microsoft"  

[ColorblindawarenessMain]: https://www.colourblindawareness.org "L’organisation De sensibilisation aux personnes non voyantes"  

[AmfcbMain]: https://www.amfcb.org "American Foundation for the Color Blind (AFCB)"  
