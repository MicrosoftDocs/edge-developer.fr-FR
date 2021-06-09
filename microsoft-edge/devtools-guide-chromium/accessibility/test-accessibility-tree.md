---
description: Vérification de l’arborescence d’accessibilité pour la prise en charge du clavier et du lecteur d’écran.
title: Vérifier l’arborescence d’accessibilité pour la prise en charge du clavier et du lecteur d’écran
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 0ab5e5609485505d1ad5fa6e2fffced9af25edcb
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597381"
---
# <a name="check-the-accessibility-tree-for-keyboard-and-screen-reader-support"></a><span data-ttu-id="7a1f1-104">Vérifier l’arborescence d’accessibilité pour la prise en charge du clavier et du lecteur d’écran</span><span class="sxs-lookup"><span data-stu-id="7a1f1-104">Check the Accessibility Tree for keyboard and screen reader support</span></span>

<!-- Accessibility tab: Accessibility Tree -->

<span data-ttu-id="7a1f1-105">Plusieurs fonctionnalités DevTools vérifient la prise en charge du clavier et du lecteur d’écran.</span><span class="sxs-lookup"><span data-stu-id="7a1f1-105">Several DevTools features check for keyboard and screen reader support.</span></span>  <span data-ttu-id="7a1f1-106">**L’utilisation de l’outil Inspect** pour vérifier l’accessibilité de chaque élément de page individuellement peut prendre beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="7a1f1-106">Using the **Inspect** tool to check the accessibility of each page element individually can become pretty time-consuming.</span></span>  <span data-ttu-id="7a1f1-107">Une autre façon de vérifier une page web consiste à utiliser **l’arborescence d’accessibilité.**</span><span class="sxs-lookup"><span data-stu-id="7a1f1-107">An alternative way to check a webpage is to use the **Accessibility Tree**.</span></span>  <span data-ttu-id="7a1f1-108">**L’arborescence d’accessibilité** indique les informations que la page fournit aux technologies d’assistance telles que les lecteurs d’écran.</span><span class="sxs-lookup"><span data-stu-id="7a1f1-108">The **Accessibility Tree** indicates what information the page provides to assistive technology such as screen readers.</span></span>

<span data-ttu-id="7a1f1-109">**L’arborescence** d’accessibilité est un sous-ensemble de l’arborescence DOM, qui contient des éléments de l’arborescence DOM pertinents et utiles pour l’affichage du contenu d’une page dans un lecteur d’écran.</span><span class="sxs-lookup"><span data-stu-id="7a1f1-109">The **Accessibility Tree** is a subset of the DOM tree, which contains elements from the DOM tree that are relevant and useful for displaying the contents of a page in a screen reader.</span></span>  <span data-ttu-id="7a1f1-110">**L’arborescence de l’accessibilité** se trouve dans **l’onglet** Accessibilité de l’outil **Éléments** (près de l’onglet **Styles).**</span><span class="sxs-lookup"><span data-stu-id="7a1f1-110">The **Accessibility Tree** is in the **Accessibility** tab of the **Elements** tool (near the **Styles** tab).</span></span>


<span data-ttu-id="7a1f1-111">Pour explorer l’utilisation de l’arborescence d’accessibilité avec la page de démonstration :</span><span class="sxs-lookup"><span data-stu-id="7a1f1-111">To explore using the Accessibility Tree with the demo page:</span></span>

1.  <span data-ttu-id="7a1f1-112">Ouvrez la [page web de démonstration des tests d’accessibilité][DevToolsA11yErrorsDemopage] dans un nouvel onglet.  Sélectionnez **ensuite F12** pour ouvrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="7a1f1-112">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab.  Then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="7a1f1-113">Sélectionnez **le bouton Inspect** \( l’icône Inspect \) dans le coin supérieur gauche de ![ DevTools afin que le bouton soit mis en surbrillant ](../media/inspect-icon.msft.png) (bleu).</span><span class="sxs-lookup"><span data-stu-id="7a1f1-113">Select the **Inspect** \(![the Inspect icon](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the button is highlighted (blue).</span></span>

1.  <span data-ttu-id="7a1f1-114">Dans la page web rendue, dans la section **Donation,** pointez sur le **bouton 100.**</span><span class="sxs-lookup"><span data-stu-id="7a1f1-114">In the rendered webpage, in the **Donation** section, hover over the **100** button.</span></span>  <span data-ttu-id="7a1f1-115">La **superposition de** l’outil Inspect s’affiche.</span><span class="sxs-lookup"><span data-stu-id="7a1f1-115">The **Inspect** tool overlay appears.</span></span>

1.  <span data-ttu-id="7a1f1-116">Dans la page web rendue, sélectionnez le **bouton 100.**</span><span class="sxs-lookup"><span data-stu-id="7a1f1-116">In the rendered webpage, select the **100** button.</span></span>  <span data-ttu-id="7a1f1-117">Dans DevTools, l’outil **Elements** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="7a1f1-117">In DevTools, the **Elements** tool is displayed.</span></span>  <span data-ttu-id="7a1f1-118">L’arborescence DOM affiche `div` l’élément du **bouton 100.**</span><span class="sxs-lookup"><span data-stu-id="7a1f1-118">The DOM tree shows the `div` element for the **100** button.</span></span>  <span data-ttu-id="7a1f1-119">Le **volet Styles** affiche les paramètres CSS de l’élément.</span><span class="sxs-lookup"><span data-stu-id="7a1f1-119">The **Styles** pane shows the CSS settings for the element.</span></span>

1.  <span data-ttu-id="7a1f1-120">À droite de l’onglet **Styles,** sélectionnez **l’onglet** Accessibilité.  **L’arborescence d’accessibilité** de l’élément s’affiche et est étendue.</span><span class="sxs-lookup"><span data-stu-id="7a1f1-120">To the right of the **Styles** tab, select the **Accessibility** tab.  The **Accessibility Tree** for the element is displayed, and is expanded.</span></span>

:::image type="complex" source="../media/a11y-testing-accessibility-tree.msft.png" alt-text="Bouton Du formulaire de don dans l’outil Arborescence de l’accessibilité" lightbox="../media/a11y-testing-accessibility-tree.msft.png":::
    <span data-ttu-id="7a1f1-122">Bouton Du formulaire de don dans l’outil Arborescence de l’accessibilité</span><span class="sxs-lookup"><span data-stu-id="7a1f1-122">Donation form button in the Accessibility Tree tool</span></span>
:::image-end:::

<span data-ttu-id="7a1f1-123">Tout élément dans l’arborescence qui n’a pas de nom ou qui a un rôle (tel que l’élément) est un problème, car cet élément n’est pas disponible pour les utilisateurs du clavier ou pour les utilisateurs qui utilisent la technologie `generic` `div` d’assistance.</span><span class="sxs-lookup"><span data-stu-id="7a1f1-123">Any element in the tree that doesn't have a name, or has a role of `generic` (such as the `div` element) is a problem, because that element won't be available to keyboard users, or to users who are using assistive technology.</span></span>


## <a name="see-also"></a><span data-ttu-id="7a1f1-124">Articles associés</span><span class="sxs-lookup"><span data-stu-id="7a1f1-124">See also</span></span>

*  [<span data-ttu-id="7a1f1-125">Afficher la position d’un élément dans l’arborescence d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="7a1f1-125">View the position of an element in the Accessibility Tree</span></span>][DevtoolsAccessibilityAccessibilityTabViewTree]
*  [<span data-ttu-id="7a1f1-126">Vue d’ensemble des tests d’accessibilité à l’aide de DevTools</span><span class="sxs-lookup"><span data-stu-id="7a1f1-126">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="7a1f1-127">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="7a1f1-127">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevtoolsAccessibilityAccessibilityTabViewTree]: accessibility-tab.md#view-the-position-of-an-element-in-the-accessibility-tree "Afficher la position d’un élément dans l’arborescence d’accessibilité - Tester l’accessibilité à l’aide de l’onglet Accessibilité | Documents Microsoft"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page web de démonstration de test d’accessibilité | GitHub"
