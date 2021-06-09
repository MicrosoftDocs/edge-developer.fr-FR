---
description: Vérifiez que les pages web sont utilisables avec l’animation de l’interface utilisateur désactivée (mouvement réduit) à l’aide de la fonctionnalité multimédia Émuler CSS préférant une liste de listes de déplacement avec mouvement réduit dans l’outil de rendu.
title: Vérifier que la page est utilisable avec l’animation de l’interface utilisateur désactivée
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: ec30925b706b4b1c6dfaaa6ce66a38fab8759ac2
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597333"
---
# <a name="verify-that-the-page-is-usable-with-ui-animation-turned-off"></a><span data-ttu-id="b4a35-104">Vérifier que la page est utilisable avec l’animation de l’interface utilisateur désactivée</span><span class="sxs-lookup"><span data-stu-id="b4a35-104">Verify that the page is usable with UI animation turned off</span></span>

<span data-ttu-id="b4a35-105">Une page web ne doit pas afficher d’animations pour un utilisateur qui a désactivé les animations dans le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b4a35-105">A webpage should not show animations to a user who turned off animations in the operating system.</span></span>  <span data-ttu-id="b4a35-106">Les animations peuvent faciliter l’utilisation d’un produit, mais elles peuvent également provoquer une distraction, une confusion ou une confusion.</span><span class="sxs-lookup"><span data-stu-id="b4a35-106">Animations can help the usability of a product, but they can also cause distraction, confusion, or nausea.</span></span>

<span data-ttu-id="b4a35-107">Pour vérifier qu’une page web est utilisable avec l’animation \*\*\*\* de l’interface utilisateur désactivée (mouvement réduit), dans l’outil de rendu, utilisez la fonctionnalité émuler la fonctionnalité multimédia **CSS** préférant la liste de listes de présentation à mouvement réduit.</span><span class="sxs-lookup"><span data-stu-id="b4a35-107">To check that a webpage is usable with UI animation turned off (reduced motion), in the **Rendering** tool, use the **Emulate CSS media feature prefers-reduced-motion** dropdown list.</span></span>

<span data-ttu-id="b4a35-108">Dans la page web de démonstration des tests d’accessibilité, lorsque vous désélectez les animations dans le système d’exploitation ou émulez ces paramètres à l’aide de DevTools, la page web n’utilise pas le défilement fluide lorsque vous sélectionnez les liens du menu de navigation de la barre latérale.</span><span class="sxs-lookup"><span data-stu-id="b4a35-108">In the accessibility-testing demo webpage, when you turn off animations in the operating system, or emulate that settings by using DevTools, the webpage doesn't use smooth scrolling when you select the links of the sidebar navigation menu.</span></span>  <span data-ttu-id="b4a35-109">Pour ce faire, vous pouvez ingériser le paramètre de défilement \*\*\*\* fluide dans CSS dans une requête multimédia, puis utiliser l’outil de rendu pour émuler le paramètre du système d’exploitation pour réduire l’animation.</span><span class="sxs-lookup"><span data-stu-id="b4a35-109">This is achieved by wrapping the smooth-scrolling setting in CSS in a media query, and then using the **Rendering** tool to emulate the operating system setting for reduced animation.</span></span>

<span data-ttu-id="b4a35-110">Pour vérifier si la page est utilisable avec des animations désactivées :</span><span class="sxs-lookup"><span data-stu-id="b4a35-110">To check whether the page is usable with animations turned off:</span></span>

1.  <span data-ttu-id="b4a35-111">Ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration des tests d’accessibilité dans un nouvel onglet du navigateur, puis sélectionnez **F12** pour ouvrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="b4a35-111">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="b4a35-112">En haut de DevTools, sélectionnez l’outil **Sources,** puis, dans le volet de **navigation** à gauche, sélectionnez `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="b4a35-112">At the top of DevTools, select the **Sources** tool, and then in the **Navigation** pane on the left, select `styles.css`.</span></span>  <span data-ttu-id="b4a35-113">Le fichier CSS apparaît dans **le** volet Éditeur.</span><span class="sxs-lookup"><span data-stu-id="b4a35-113">The CSS file appears in the **Editor** pane.</span></span>

1.  <span data-ttu-id="b4a35-114">Sélectionnez **Ctrl+F** sur Windows/Linux ou **Command+F** sur macOS, puis entrez `@media` .</span><span class="sxs-lookup"><span data-stu-id="b4a35-114">Select **Ctrl+F** on Windows/Linux or **Command+F** on macOS, and then enter `@media`.</span></span>  <span data-ttu-id="b4a35-115">La requête multimédia CSS suivante s’affiche, ce qui confirme qu’elle est utilisée sur la page web.</span><span class="sxs-lookup"><span data-stu-id="b4a35-115">The following CSS media query is displayed, which confirms that it is used on the webpage.</span></span>

    ```css
    @media (prefers-reduced-motion: no-preference) {
      html {
        scroll-behavior: smooth;
      }
    }
    ```

    <span data-ttu-id="b4a35-116">Ensuite, émulez le paramètre du système d’exploitation pour réduire l’animation, comme suit.</span><span class="sxs-lookup"><span data-stu-id="b4a35-116">Next, emulate the operating system setting to reduce animation, as follows.</span></span>

1.  <span data-ttu-id="b4a35-117">Sélectionnez **Échap** pour ouvrir le caisse en bas de DevTools.</span><span class="sxs-lookup"><span data-stu-id="b4a35-117">Select **Esc** to open the Drawer at the bottom of DevTools.</span></span>  <span data-ttu-id="b4a35-118">Sélectionnez **le bouton Plus d’outils** () en haut du caisse pour voir la liste des outils, puis **+** sélectionnez **Rendu.**</span><span class="sxs-lookup"><span data-stu-id="b4a35-118">Select the **More tools** (**+**) button at the top of the Drawer to see the list of tools, and then select **Rendering**.</span></span>  

1.  <span data-ttu-id="b4a35-119">Dans la **fonctionnalité émuler le support CSS préférant la** liste de listes de déplacement à mouvement réduit, sélectionnez **prefers-reduced-motion: reduced**.</span><span class="sxs-lookup"><span data-stu-id="b4a35-119">In the **Emulate CSS media feature prefers-reduced-motion** dropdown list, select **prefers-reduced-motion: reduced**.</span></span>

    :::image type="complex" source="../media/a11y-testing-simulating-reduced-motion.msft.png" alt-text="Simulation d’un mouvement réduit et du CSS qui permet de s’assurer que le défilement fluide se produit uniquement lorsque l’utilisateur le souhaite" lightbox="../media/a11y-testing-simulating-reduced-motion.msft.png":::
        <span data-ttu-id="b4a35-121">Simulation d’un mouvement réduit et du CSS qui permet de s’assurer que le défilement fluide se produit uniquement lorsque l’utilisateur le souhaite</span><span class="sxs-lookup"><span data-stu-id="b4a35-121">Simulating reduced motion and the CSS that makes sure that smooth scrolling only happens when the user wants it</span></span>
    :::image-end:::

1.  <span data-ttu-id="b4a35-122">Dans la page web, sélectionnez les éléments de menu bleu, tels que **La maison ou** les **espaces.**</span><span class="sxs-lookup"><span data-stu-id="b4a35-122">In the webpage, select the blue menu items, such as **Horses** or **Alpacas**.</span></span>  <span data-ttu-id="b4a35-123">À présent, la page web défile instantanément jusqu’à la section sélectionnée, au lieu d’utiliser l’animation à défilement fluide.</span><span class="sxs-lookup"><span data-stu-id="b4a35-123">Now the webpage instantly scrolls to the selected section, rather than using the smooth-scrolling animation.</span></span>

1.  <span data-ttu-id="b4a35-124">Dans **l’outil de** rendu, sous Émuler la fonctionnalité multimédia **CSS préférer le**mouvement réduit, sélectionnez Aucune **émulation** pour supprimer ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="b4a35-124">In the **Rendering** tool, below **Emulate CSS media feature prefers-reduced-motion**, select **No emulation** to remove this setting.</span></span>
   
<span data-ttu-id="b4a35-125">Notez que la page web de démonstration exécute toujours les animations suivantes, même avec les paramètres de requête et d’émulation multimédia ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="b4a35-125">Notice that the demo webpage still runs the following animations, even with the above media query and emulation settings.</span></span> <span data-ttu-id="b4a35-126">Lorsque vous construisez votre produit web, veillez à corriger toutes les animations similaires.</span><span class="sxs-lookup"><span data-stu-id="b4a35-126">When building your web product, ensure you fix all similar animations.</span></span>  
*  <span data-ttu-id="b4a35-127">Animation des éléments de menu bleu lorsque vous pointez dessus.</span><span class="sxs-lookup"><span data-stu-id="b4a35-127">Animation of the blue menu items when you hover over them.</span></span>
*  <span data-ttu-id="b4a35-128">Animation des cercles sur les **liens Plus** lorsque vous pointez dessus.</span><span class="sxs-lookup"><span data-stu-id="b4a35-128">Animation of the circles on the **More** links when you hover over them.</span></span>



## <a name="see-also"></a><span data-ttu-id="b4a35-129">Articles associés</span><span class="sxs-lookup"><span data-stu-id="b4a35-129">See also</span></span>

*  [<span data-ttu-id="b4a35-130">Simulation de mouvement réduit</span><span class="sxs-lookup"><span data-stu-id="b4a35-130">Reduced motion simulation</span></span>](reduced-motion-simulation.md)
*  [<span data-ttu-id="b4a35-131">Vue d’ensemble des tests d’accessibilité à l’aide de DevTools</span><span class="sxs-lookup"><span data-stu-id="b4a35-131">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="b4a35-132">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="b4a35-132">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page web de démonstration de test d’accessibilité | GitHub"
