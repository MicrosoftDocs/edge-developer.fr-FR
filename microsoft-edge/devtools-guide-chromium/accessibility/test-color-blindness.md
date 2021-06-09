---
description: Vérifiez que les pages web sont utilisables par les personnes daltonies à l’aide de la liste liste de listes de listes listes des émuler les faiblesses de vision dans l’outil de rendu.
title: Vérifier que la page est utilisable par les personnes daltonismes
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 54cd7230f0402bfeb4b5ee28d2bcd0947794676f
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597367"
---
# <a name="verify-that-the-page-is-usable-by-people-with-color-blindness"></a><span data-ttu-id="ac542-104">Vérifier que la page est utilisable par les personnes daltonismes</span><span class="sxs-lookup"><span data-stu-id="ac542-104">Verify that the page is usable by people with color blindness</span></span>

<!-- Rendering tool: Emulate vision deficiencies: Protanopia -->

<span data-ttu-id="ac542-105">Pour vérifier qu’une page web est utilisable par \*\*\*\* des personnes daltonies, dans l’outil de rendu, utilisez la liste liste de listes des problèmes de **vision** émuler.</span><span class="sxs-lookup"><span data-stu-id="ac542-105">To check that a webpage is usable by people with color blindness, in the **Rendering** tool, use the **Emulate vision deficiencies** dropdown list.</span></span>

<span data-ttu-id="ac542-106">Sur la page web de démonstration des tests d’accessibilité, les différents états de don utilisent la couleur comme seul moyen de différenciation.</span><span class="sxs-lookup"><span data-stu-id="ac542-106">On the accessibility-testing demo webpage, the different donation states use color as the only means of differentiation.</span></span>
*  <span data-ttu-id="ac542-107">Vert signifie qu’un montant élevé de dons a été reçu.</span><span class="sxs-lookup"><span data-stu-id="ac542-107">Green means a high amount of donations have been received.</span></span>
*  <span data-ttu-id="ac542-108">Le jaune signifie qu’un montant moyen de dons a été reçu.</span><span class="sxs-lookup"><span data-stu-id="ac542-108">Yellow means a medium amount of donations have been received.</span></span>
*  <span data-ttu-id="ac542-109">Le rouge signifie qu’un faible montant de dons a été reçu.</span><span class="sxs-lookup"><span data-stu-id="ac542-109">Red means a low amount of donations have been received.</span></span>

<span data-ttu-id="ac542-110">Mais vous ne pouvez pas vous attendre à ce que tous vos utilisateurs utilisent ces couleurs comme prévu.</span><span class="sxs-lookup"><span data-stu-id="ac542-110">But you can't expect all of your users to experience these colors as intended.</span></span>  <span data-ttu-id="ac542-111">En utilisant la fonctionnalité Émuler \*\*\*\* les défauts de **vision** de l’outil de rendu, vous pouvez découvrir que cette conception n’est pas suffisamment bonne, en simulant la façon dont les personnes ayant une vision différente persoraient votre conception.</span><span class="sxs-lookup"><span data-stu-id="ac542-111">By using the **Emulate vision deficiencies** feature of the **Rendering** tool, you can find out that this design is not good enough, by simulating how people with different vision would perceive your design.</span></span>


<span data-ttu-id="ac542-112">Pour vérifier si une page web est utilisable par des personnes daltonisme :</span><span class="sxs-lookup"><span data-stu-id="ac542-112">To check whether a webpage is usable by people with color blindness:</span></span>

1.  <span data-ttu-id="ac542-113">Ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration des tests d’accessibilité dans un nouvel onglet du navigateur, puis sélectionnez **F12** pour ouvrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="ac542-113">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="ac542-114">Sélectionnez **Échap** pour ouvrir le caisse en bas de DevTools.</span><span class="sxs-lookup"><span data-stu-id="ac542-114">Select **Esc** to open the Drawer at the bottom of DevTools.</span></span>  <span data-ttu-id="ac542-115">Sélectionnez l’icône en haut du caisse pour voir la liste des outils, puis **+** sélectionnez **Rendu.**</span><span class="sxs-lookup"><span data-stu-id="ac542-115">Select the **+** icon at the top of the Drawer to see the list of tools, and then select **Rendering**.</span></span>  

1.  <span data-ttu-id="ac542-116">Dans la liste liste de listes des **défaillances** de vision Émuler, sélectionnez **Protanopia**.</span><span class="sxs-lookup"><span data-stu-id="ac542-116">In the **Emulate vision deficiencies** dropdown list, select **Protanopia**.</span></span>  <span data-ttu-id="ac542-117">_La protanopie_ est une réduction de la sensibilité à la lumière rouge, ce qui rend difficile la différenciation du vert, du rouge et du jaune.</span><span class="sxs-lookup"><span data-stu-id="ac542-117">_Protanopia_ is reduced sensitivity to red light, making it hard to differentiate green, red, and yellow.</span></span>

    :::image type="complex" source="../media/a11y-testing-simulating-protanopia.msft.png" alt-text="Affichage du document comme une personne avec une protanopie le verra" lightbox="../media/a11y-testing-simulating-protanopia.msft.png":::
        <span data-ttu-id="ac542-119">Affichage du document comme une personne avec une protanopie le verra</span><span class="sxs-lookup"><span data-stu-id="ac542-119">Showing the document as someone with protanopia would see it</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="ac542-120">Dans **l’outil de** rendu, sous Émuler les **défaillances visuelles,** sélectionnez Aucune **émulation** pour supprimer la simulation.</span><span class="sxs-lookup"><span data-stu-id="ac542-120">In the **Rendering** tool, below **Emulate vision deficiencies**, select **No emulation** to remove the simulation.</span></span>


## <a name="see-also"></a><span data-ttu-id="ac542-121">Articles associés</span><span class="sxs-lookup"><span data-stu-id="ac542-121">See also</span></span>

*  <span data-ttu-id="ac542-122">[Émuler][DevToolsVisionDeficiencies] les défaillances visuelles : définit les éléments de la liste de listes de défaillances de **vision** Émuler, y compris Protanopia, Deuteranopia, Tritanopia et Achromatopsia.</span><span class="sxs-lookup"><span data-stu-id="ac542-122">[Emulate vision deficiencies][DevToolsVisionDeficiencies] - Defines the items in the **Emulate vision deficiencies** dropdown list, including Protanopia, Deuteranopia, Tritanopia, and Achromatopsia.</span></span>
*  [<span data-ttu-id="ac542-123">Vue d’ensemble des tests d’accessibilité à l’aide de DevTools</span><span class="sxs-lookup"><span data-stu-id="ac542-123">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="ac542-124">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="ac542-124">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsVisionDeficiencies]: ./emulate-vision-deficiencies.md "Émuler les défaillances visuelles | Documents Microsoft"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page web de démonstration de test d’accessibilité | GitHub"
