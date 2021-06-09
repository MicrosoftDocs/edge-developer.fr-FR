---
description: Pour voir rapidement l’ordre de tabulation des sections d’une page, utilisez l’Observateur de commandes source dans l’outil Accessibilité, à droite de l’onglet Styles.
title: Tester la prise en charge du clavier à l’aide de l’Observateur de commandes source
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 7e90221b581280a6eb63cee4d073622a80871903
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597330"
---
# <a name="test-keyboard-support-using-the-source-order-viewer"></a><span data-ttu-id="6225e-104">Tester la prise en charge du clavier à l’aide de l’Observateur de commandes source</span><span class="sxs-lookup"><span data-stu-id="6225e-104">Test keyboard support using the Source Order Viewer</span></span>

<span data-ttu-id="6225e-105">L’ordre source d’un document est important pour la technologie d’assistance et peut être différent de l’ordre dans lequel les éléments apparaissent sur la page rendue.</span><span class="sxs-lookup"><span data-stu-id="6225e-105">The source order of a document is important for assistive technology, and can be different than the order in which elements appear on the rendered page.</span></span>  <span data-ttu-id="6225e-106">À l’aide de CSS, vous pouvez ré orderer les éléments de page d’une manière visuelle, mais cela ne signifie pas que les technologies d’assistance telles que les lecteurs d’écran représentent les éléments de page dans le même ordre.</span><span class="sxs-lookup"><span data-stu-id="6225e-106">Using CSS, you can re-order page elements in a visual way, but that doesn't mean that assistive technology such as screen readers would represent page elements in the same order.</span></span>  

<span data-ttu-id="6225e-107">Pour vous assurer que le document possède \*\*\*\* un ordre logique, vous pouvez utiliser l’Observateur de commandes source pour étiqueter différents éléments de page avec des nombres spécifiant l’ordre dans le code source du document.</span><span class="sxs-lookup"><span data-stu-id="6225e-107">To ensure that the document has a logical order, you can use the **Source Order Viewer** to label different page elements with numbers that specify the order in the source code of the document.</span></span>  <span data-ttu-id="6225e-108">**L’Observateur de commandes source** se trouve dans **l’onglet** Accessibilité (près de **l’onglet Styles).**</span><span class="sxs-lookup"><span data-stu-id="6225e-108">The **Source Order Viewer** is in the **Accessibility** tab (near the **Styles** tab).</span></span>


## <a name="analyzing-the-order-of-keyboard-access-through-sections-of-the-page"></a><span data-ttu-id="6225e-109">Analyse de l’ordre d’accès au clavier par le biais de sections de la page</span><span class="sxs-lookup"><span data-stu-id="6225e-109">Analyzing the order of keyboard access through sections of the page</span></span>

<span data-ttu-id="6225e-110">La page web de démonstration de test d’accessibilité a un ordre de tabulation [contre-intuitif,][DevToolsA11yErrorsDemopage] où les utilisateurs du clavier accèdent au menu de navigation de la barre latérale uniquement après avoir effectué une tabulation sur tous les liens **Plus.**</span><span class="sxs-lookup"><span data-stu-id="6225e-110">The [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] has a counterintuitive tabbing order, where keyboard users access the sidebar navigation menu only after tabbing through all the **More** links.</span></span>  <span data-ttu-id="6225e-111">Le menu de navigation de la barre latérale est destiné à être un raccourci pour atteindre le contenu de la page.</span><span class="sxs-lookup"><span data-stu-id="6225e-111">The sidebar navigation menu is meant to be a shortcut to reach deep into the page content.</span></span>  <span data-ttu-id="6225e-112">Toutefois, étant donné que vous devez passer par la page entière avant d’atteindre le menu de navigation de la barre latérale, ce menu de navigation est inefficace pour les utilisateurs du clavier.</span><span class="sxs-lookup"><span data-stu-id="6225e-112">But because you need to go through the entire page before you reach the sidebar navigation menu, that navigation menu is ineffective for keyboard users.</span></span>

<span data-ttu-id="6225e-113">`Tab`L’ordre de clé de la page de démonstration est le suivante :</span><span class="sxs-lookup"><span data-stu-id="6225e-113">The `Tab` key order on the demo page is:</span></span>
1. <span data-ttu-id="6225e-114">Le **champ** Recherche, puis le **bouton Aller** pour le **champ** De recherche.</span><span class="sxs-lookup"><span data-stu-id="6225e-114">The **Search** field, then the **go** button for the **Search** field.</span></span>
1. <span data-ttu-id="6225e-115">Bouton **Plus** dans la section **Chats,** pour accéder à une page web « Chats ».</span><span class="sxs-lookup"><span data-stu-id="6225e-115">The **More** button in the **Cats** section, to navigate to a "Cats" webpage.</span></span>  <span data-ttu-id="6225e-116">Ensuite, les **autres boutons Plus,** pour les chiens, la chasse, la capacité, puis les espaces alpacas.</span><span class="sxs-lookup"><span data-stu-id="6225e-116">Then the other **More** buttons, for Dogs, Sheep, Horses, and then Alpacas.</span></span>
1. <span data-ttu-id="6225e-117">Les liens bleus du menu de navigation de la barre latérale : **Chats,** **Chats,** **Chats, Chats,** **Rythme,** puis **Alpacas**.</span><span class="sxs-lookup"><span data-stu-id="6225e-117">The blue links of the sidebar navigation menu: **Cats**, **Dogs**, **Sheep**, **Horses**, and then **Alpacas**.</span></span>
1. <span data-ttu-id="6225e-118">La boîte de texte du don dans le formulaire de don.</span><span class="sxs-lookup"><span data-stu-id="6225e-118">The donation textbox in the donation form.</span></span>
1. <span data-ttu-id="6225e-119">Les boutons dans la barre de navigation supérieure : **Accueil,** Adopter un enfant de **compagnie,** **Sons,** **Travaux,** puis **À propos de nous**.</span><span class="sxs-lookup"><span data-stu-id="6225e-119">The buttons in the top navigation bar: **Home**, **Adopt a pet**, **Donate**, **Jobs**, and then **About Us**.</span></span>
1. <span data-ttu-id="6225e-120">Interface haut de fenêtre du navigateur.</span><span class="sxs-lookup"><span data-stu-id="6225e-120">The browser's top-of-window interface.</span></span>

<span data-ttu-id="6225e-121">La raison pour laquelle l’ordre des touches est déroutant est que l’ordre utilisé lors de l’utilisation d’un clavier est déterminé par l’ordre `Tab` source du document.</span><span class="sxs-lookup"><span data-stu-id="6225e-121">The reason for the confusing `Tab` key order is that the order experienced when using a keyboard is determined by the source order of the document.</span></span>  <span data-ttu-id="6225e-122">L’ordre utilisé à l’aide d’un clavier peut être modifié à l’aide de l’attribut sur les éléments, ce qui permet de sortir cet élément de `tabindex` l’ordre source.</span><span class="sxs-lookup"><span data-stu-id="6225e-122">The order experienced using a keyboard can be modified using the `tabindex` attribute on elements, which takes that element out of the source order.</span></span>

<span data-ttu-id="6225e-123">Dans le code source du document, le menu de navigation de la barre latérale apparaît après le contenu principal de la page web.</span><span class="sxs-lookup"><span data-stu-id="6225e-123">In the source code of the document, the sidebar navigation menu appears after the main content of the webpage.</span></span>  <span data-ttu-id="6225e-124">CSS a été utilisé pour positionner le menu de navigation de barre latérale au-dessus de la plupart du contenu principal de la page web.</span><span class="sxs-lookup"><span data-stu-id="6225e-124">CSS was used to position the sidebar navigation menu above most of the main content of the webpage.</span></span> 

<span data-ttu-id="6225e-125">Vous pouvez tester l’ordre des éléments de page à l’aide de l’Observateur de commandes **source** dans **l’onglet** Accessibilité.  **L’Observateur de commandes source** est une fonctionnalité expérimentale.</span><span class="sxs-lookup"><span data-stu-id="6225e-125">You can test the order of page elements by using the **Source Order Viewer** in the **Accessibility** tab.  The **Source Order Viewer** is an experimental feature.</span></span> <span data-ttu-id="6225e-126">Pour plus d’informations, accédez à [l’Observateur de commandes source.](../experimental-features/index.md#source-order-viewer)</span><span class="sxs-lookup"><span data-stu-id="6225e-126">For more information, navigate to [Source Order Viewer](../experimental-features/index.md#source-order-viewer).</span></span>


<span data-ttu-id="6225e-127">Pour activer l’Observateur de commandes source :</span><span class="sxs-lookup"><span data-stu-id="6225e-127">To turn on the Source Order Viewer:</span></span>

1.  <span data-ttu-id="6225e-128">Dans DevTools, dans le coin supérieur droit, sélectionnez le **bouton Paramètres** \( Paramètres ![ bouton ](../media/settings-button-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="6225e-128">In DevTools, in the upper right, select the **Settings** \(![Settings button](../media/settings-button-icon.msft.png)\) button.</span></span>  

1.  <span data-ttu-id="6225e-129">Sous **Paramètres,** sélectionnez **Expériences.**</span><span class="sxs-lookup"><span data-stu-id="6225e-129">Below **Settings**, select **Experiments**.</span></span>  

1.  <span data-ttu-id="6225e-130">Cochez la **case De l’Observateur de commandes** source.</span><span class="sxs-lookup"><span data-stu-id="6225e-130">Select the **Source Order Viewer** checkbox.</span></span>

1.  <span data-ttu-id="6225e-131">Dans le coin supérieur droit de la page **Paramètres** page, sélectionnez **X** pour fermer la page Paramètres page.</span><span class="sxs-lookup"><span data-stu-id="6225e-131">In the upper-right corner of the **Settings** page, select **X** to close the Settings page.</span></span>  <span data-ttu-id="6225e-132">En haut de DevTools, les paramètres du message Un ou plusieurs ont changé, ce qui nécessite un **rechargement pour prendre effet.**</span><span class="sxs-lookup"><span data-stu-id="6225e-132">At the top of DevTools, the message **One or more settings have changed which require a reload to take effect.**</span></span> <span data-ttu-id="6225e-133">s’affiche.</span><span class="sxs-lookup"><span data-stu-id="6225e-133">is displayed.</span></span>  <span data-ttu-id="6225e-134">Sélectionnez **le bouton Recharger DevTools.**</span><span class="sxs-lookup"><span data-stu-id="6225e-134">Select the **Reload DevTools** button.</span></span>



<span data-ttu-id="6225e-135">Pour activer et utiliser l’Observateur de commandes source, avec la page de démonstration :</span><span class="sxs-lookup"><span data-stu-id="6225e-135">To activate and use the Source Order Viewer, with the demo page:</span></span>

1.  <span data-ttu-id="6225e-136">Ouvrez la [page web de démonstration des tests d’accessibilité][DevToolsA11yErrorsDemopage] dans un nouvel onglet.  Sélectionnez **ensuite F12** pour ouvrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="6225e-136">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab.  Then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="6225e-137">Dans **l’outil Éléments,** à droite de l’onglet **Styles,** sélectionnez **l’onglet** Accessibilité.</span><span class="sxs-lookup"><span data-stu-id="6225e-137">In the **Elements** tool, to the right of the **Styles** tab, select the **Accessibility** tab.</span></span>

1.  <span data-ttu-id="6225e-138">Dans la section **Visionneuse de commandes** source, cochez la case Afficher la **commande source.**</span><span class="sxs-lookup"><span data-stu-id="6225e-138">In the **Source Order Viewer** section, select the **Show source order** checkbox.</span></span>  <span data-ttu-id="6225e-139">Dans la page web rendue, des nombres apparaissent, indiquant l’ordre contrôlé par l’ordre des lignes de `Tab` code dans le fichier source.</span><span class="sxs-lookup"><span data-stu-id="6225e-139">In the rendered webpage, numbers appear, indicating the `Tab` order as controlled by the order of lines of code in the source file.</span></span>

1.  <span data-ttu-id="6225e-140">Dans l’arborescence DOM de **l’outil Elements,** sélectionnez un élément de disposition principal, tel que `header` l’élément.</span><span class="sxs-lookup"><span data-stu-id="6225e-140">In the DOM tree in the **Elements** tool, select a major layout element, such as the `header` element.</span></span>  <span data-ttu-id="6225e-141">Les superpositions numériques sont désormais affichées sur les sections de la page rendue, ce qui indique l’ordre source des différents éléments.</span><span class="sxs-lookup"><span data-stu-id="6225e-141">Numeric overlays are now displayed on sections of the rendered page, which indicate the source order of the different elements.</span></span> 

    :::image type="complex" source="../media/a11y-testing-source-order-viewer.msft.png" alt-text="L’activation de l’Afficheur des commandes sources affiche l’ordre des éléments dans la source sous la la mesure où ils sont superposés sur la page" lightbox="../media/a11y-testing-source-order-viewer.msft.png":::
        <span data-ttu-id="6225e-143">L’activation de **l’Afficheur** des commandes sources affiche l’ordre des éléments dans la source sous la la mesure où ils sont superposés sur la page</span><span class="sxs-lookup"><span data-stu-id="6225e-143">Activating the **Source Order Viewer** shows the order of the elements in the source as overlays on the page</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="6225e-144">Faites défiler la page pour voir toutes les superpositions numériques, y compris dans la section pied de page.</span><span class="sxs-lookup"><span data-stu-id="6225e-144">Scroll the page to see all of the numeric overlays, including on the page footer section.</span></span>


## <a name="see-also"></a><span data-ttu-id="6225e-145">Articles associés</span><span class="sxs-lookup"><span data-stu-id="6225e-145">See also</span></span>

*  [<span data-ttu-id="6225e-146">Vue d’ensemble des tests d’accessibilité à l’aide de DevTools</span><span class="sxs-lookup"><span data-stu-id="6225e-146">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="6225e-147">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="6225e-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page web de démonstration de test d’accessibilité | GitHub"
