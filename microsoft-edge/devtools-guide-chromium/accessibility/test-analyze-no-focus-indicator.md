---
description: Analyse de l’absence d’indication du focus du clavier dans un menu de barre latérale, en raison de l’absence d’une règle de pseudo-classe CSS pour l’état de mise au point sur un lien, combinée avec le lien n’ayant pas de paramètre de plan.
title: Analyser l’absence d’indication du focus du clavier dans un menu de barre latérale
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 3626de9bdc2cce266efafe4b1b2e8fff501a74f7
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597380"
---
# <a name="analyze-the-lack-of-indication-of-keyboard-focus-in-a-sidebar-menu"></a><span data-ttu-id="bf986-104">Analyser l’absence d’indication du focus du clavier dans un menu de barre latérale</span><span class="sxs-lookup"><span data-stu-id="bf986-104">Analyze the lack of indication of keyboard focus in a sidebar menu</span></span>

<!-- Inspect tool, and CSS rules: pseudo-classes for states -->

<span data-ttu-id="bf986-105">Dans la page de démonstration des tests d’accessibilité, le menu de navigation de la barre latérale avec des liens bleus n’indique pas visuellement quel lien a le focus, lors de l’utilisation d’un clavier.</span><span class="sxs-lookup"><span data-stu-id="bf986-105">In the accessibility-testing demo page, the sidebar navigation menu with blue links doesn't visually indicate which link has focus, when using a keyboard.</span></span>  <span data-ttu-id="bf986-106">Pour savoir pourquoi le menu de la barre latérale est déroutant pour les utilisateurs du clavier, nous allons rechercher des règles de pseudo-classe CSS pour les états et les états, ainsi que la propriété CSS pour les contours des `hover` `focus` liens.</span><span class="sxs-lookup"><span data-stu-id="bf986-106">To find out why the sidebar menu is confusing to keyboard users, we'll look for CSS pseudo-class rules for the `hover` and `focus` states, along with the CSS property for link outlines.</span></span>  

<span data-ttu-id="bf986-107">Cette analyse trouve que l’absence d’indication du focus du clavier dans les liens du menu de navigation de la barre latérale est dû aux éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="bf986-107">This analysis finds that the lack of indication of keyboard focus in the links of the sidebar navigation menu is because:</span></span>
*  <span data-ttu-id="bf986-108">Les `a` liens ont un paramètre de propriété CSS de `outline: none` .</span><span class="sxs-lookup"><span data-stu-id="bf986-108">The `a` links have a CSS property setting of `outline: none`.</span></span>
*  <span data-ttu-id="bf986-109">Les `a` liens ne disposent pas d’une règle de pseudo-classe CSS pour l’état. `:focus`</span><span class="sxs-lookup"><span data-stu-id="bf986-109">The `a` links lack a CSS pseudo-class rule for the `:focus` state.</span></span>

<span data-ttu-id="bf986-110">Pour accéder au CSS, nous allons utiliser l’outil **Inspect** pour mettre en évidence un lien bleu dans le menu de navigation de la barre latérale, puis afficher l’arborescence DOM et CSS pour l’élément qui définit ce `a` lien.</span><span class="sxs-lookup"><span data-stu-id="bf986-110">To navigate to the CSS, we'll use the **Inspect** tool to highlight a blue link on the sidebar navigation menu, and then view the DOM tree and CSS for the `a` element that defines that link.</span></span>

1.  <span data-ttu-id="bf986-111">Ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration des tests d’accessibilité dans un nouvel onglet du navigateur, puis sélectionnez **F12** pour ouvrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="bf986-111">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="bf986-112">Sélectionnez **le bouton Inspect** \( Inspect icon \) dans le coin supérieur gauche de DevTools afin que le bouton soit mis en ![ ](../media/inspect-icon.msft.png) surbrillant (bleu).</span><span class="sxs-lookup"><span data-stu-id="bf986-112">Select the **Inspect** \(![Inspect icon](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the button is highlighted (blue).</span></span>

1.  <span data-ttu-id="bf986-113">Pointez sur le lien **chats** bleus dans le menu de navigation de la barre latérale.</span><span class="sxs-lookup"><span data-stu-id="bf986-113">Hover over the blue **Cats** link in the sidebar navigation menu.</span></span>  <span data-ttu-id="bf986-114">La superposition Inspect s’affiche, montrant que l’élément est `a` focusable au clavier.</span><span class="sxs-lookup"><span data-stu-id="bf986-114">The Inspect overlay appears, showing that the `a` element is keyboard-focusable.</span></span>  <span data-ttu-id="bf986-115">Mais la superposition ne montre pas qu’il n’y a aucune indication visuelle lorsque le lien a le focus.</span><span class="sxs-lookup"><span data-stu-id="bf986-115">But the overlay doesn't show that there's no visual indication when the link has focus.</span></span>

    <span data-ttu-id="bf986-116">Ensuite, nous allons examiner le style CSS de ce lien.</span><span class="sxs-lookup"><span data-stu-id="bf986-116">Next, we'll inspect the CSS styling of this link.</span></span>
 
1.  <span data-ttu-id="bf986-117">Sélectionnez **le lien Chats** dans le menu de navigation de la barre latérale.</span><span class="sxs-lookup"><span data-stu-id="bf986-117">Select the **Cats** link in the sidebar navigation menu.</span></span>  <span data-ttu-id="bf986-118">**L’outil Inspect** s’éteint et l’outil **Elements** s’ouvre, mettant en surbrillance le nœud dans `a` l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="bf986-118">The **Inspect** tool turns off, and the **Elements** tool opens, highlighting the `a` node in the DOM tree.</span></span>

1.  <span data-ttu-id="bf986-119">Sélectionnez **l’onglet Styles.**  La règle CSS apparaît, ainsi qu’un lien `#sidebar nav li a` vers un numéro de ligne dans `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="bf986-119">Select the **Styles** tab.  The CSS rule `#sidebar nav li a` appears, along with a link to a line number in `styles.css`.</span></span>

    :::image type="complex" source="../media/a11y-testing-menu-link.msft.png" alt-text="Inspection du code source et des styles appliqués d’un lien dans le menu" lightbox="../media/a11y-testing-menu-link.msft.png":::
        <span data-ttu-id="bf986-121">Inspection du code source et des styles appliqués d’un lien dans le menu</span><span class="sxs-lookup"><span data-stu-id="bf986-121">Inspecting the source code and the applied styles of a link in the menu</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="bf986-122">Sélectionnez le lien vers le fichier CSS.</span><span class="sxs-lookup"><span data-stu-id="bf986-122">Select the link to the CSS file.</span></span>  <span data-ttu-id="bf986-123">Le fichier CSS s’ouvre dans l’outil **Sources.**</span><span class="sxs-lookup"><span data-stu-id="bf986-123">The CSS file opens within the **Sources** tool.</span></span>

    :::image type="complex" source="../media/a11y-testing-menu-link-styles.msft.png" alt-text="Styles appliqués au lien dans l’outil Sources" lightbox="../media/a11y-testing-menu-link-styles.msft.png":::
        <span data-ttu-id="bf986-125">Styles appliqués au lien dans l’outil Sources</span><span class="sxs-lookup"><span data-stu-id="bf986-125">The styles applied to the link in the Sources tool</span></span>
    :::image-end:::
    
<span data-ttu-id="bf986-126">Les styles de la page ont une règle de pseudo-classe CSS pour l’état qui indique l’élément de menu que vous utilisez lorsque vous utilisez `hover` une souris : `#sidebar nav li a:hover` .</span><span class="sxs-lookup"><span data-stu-id="bf986-126">The styles of the page have a CSS pseudo-class rule for the `hover` state that indicates which menu item you are on when you use a mouse: `#sidebar nav li a:hover`.</span></span>  <span data-ttu-id="bf986-127">Toutefois, il n’existe aucune règle de pseudo-classe CSS pour que l’état indique visuellement l’élément de menu sur lequel vous vous trouvez lorsque vous utilisez un `focus` clavier, tel que `#sidebar nav li a:focus` .</span><span class="sxs-lookup"><span data-stu-id="bf986-127">However, there is no CSS pseudo-class rule for the `focus` state to visually indicate which menu item you are on when you use a keyboard, such as `#sidebar nav li a:focus`.</span></span>

<span data-ttu-id="bf986-128">Notez également que les liens ont un paramètre de propriété CSS de `outline: none` .</span><span class="sxs-lookup"><span data-stu-id="bf986-128">Also, notice that the links have a CSS property setting of `outline: none`.</span></span>  <span data-ttu-id="bf986-129">Il s’agit d’une pratique courante qui consiste à supprimer le plan que les navigateurs ajoutent automatiquement aux éléments lorsque vous vous concentrez sur eux à l’aide d’un clavier.</span><span class="sxs-lookup"><span data-stu-id="bf986-129">This is a common practice, to remove the outline which browsers automatically add to elements when you focus on them using a keyboard.</span></span>  <span data-ttu-id="bf986-130">Le fait de ne pas `focus` utiliser de style crée de la confusion pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="bf986-130">Not using `focus` styling causes confusion for your users.</span></span>


## <a name="see-also"></a><span data-ttu-id="bf986-131">Articles associés</span><span class="sxs-lookup"><span data-stu-id="bf986-131">See also</span></span> 

*  [<span data-ttu-id="bf986-132">Effectuer le suivi de l’élément actif</span><span class="sxs-lookup"><span data-stu-id="bf986-132">Track which element has focus</span></span>](focus.md)
*  [<span data-ttu-id="bf986-133">Vue d’ensemble des tests d’accessibilité à l’aide de DevTools</span><span class="sxs-lookup"><span data-stu-id="bf986-133">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="bf986-134">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="bf986-134">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page web de démonstration de test d’accessibilité | GitHub"
