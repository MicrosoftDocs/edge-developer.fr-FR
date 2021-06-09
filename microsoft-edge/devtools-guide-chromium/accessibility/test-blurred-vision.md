---
description: Pour vérifier qu’une page web est utilisable avec une vision floue, dans l’outil de rendu, utilisez la liste de listes de listes des défaillances de vision Émuler.
title: Vérifier que la page est utilisable avec une vision floue
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 2fc1a1cf7746591573fce07946c7fb11abf42705
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597369"
---
# <a name="verify-that-the-page-is-usable-with-blurred-vision"></a><span data-ttu-id="3c7da-104">Vérifier que la page est utilisable avec une vision floue</span><span class="sxs-lookup"><span data-stu-id="3c7da-104">Verify that the page is usable with blurred vision</span></span>

<!-- Rendering tool: Emulate vision deficiencies: Blurred vision -->

<span data-ttu-id="3c7da-105">Pour simuler une vision floue, dans l’outil **de** rendu, utilisez le menu Émuler les **faiblesses de la** vision.</span><span class="sxs-lookup"><span data-stu-id="3c7da-105">To simulate blurred vision, in the **Rendering** tool, use the **Emulate vision deficiencies** menu.</span></span>  <span data-ttu-id="3c7da-106">Lorsque vous utilisez cette fonctionnalité avec la page web de démonstration, vous pouvez voir que l’ombre portée du texte dans le menu supérieur complique la lecture des éléments de menu.</span><span class="sxs-lookup"><span data-stu-id="3c7da-106">When you use this feature with the demo webpage, you can see that the drop shadow on the text in the upper menu makes it hard to read the menu items.</span></span>

<span data-ttu-id="3c7da-107">Pour vérifier si une page web est utilisable avec une vision floue :</span><span class="sxs-lookup"><span data-stu-id="3c7da-107">To check whether a webpage is usable with blurred vision:</span></span>

1.  <span data-ttu-id="3c7da-108">Ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration des tests d’accessibilité dans un nouvel onglet du navigateur, puis sélectionnez **F12** pour ouvrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="3c7da-108">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="3c7da-109">Sélectionnez **Échap** pour ouvrir le caisse en bas de DevTools.</span><span class="sxs-lookup"><span data-stu-id="3c7da-109">Select **Esc** to open the Drawer at the bottom of DevTools.</span></span>  <span data-ttu-id="3c7da-110">Sélectionnez l’icône en haut du caisse pour afficher la liste des outils, puis **+** sélectionnez **Rendu.**</span><span class="sxs-lookup"><span data-stu-id="3c7da-110">Select the **+** icon at the top of the Drawer to display the list of tools, and then select **Rendering**.</span></span>  

1.  <span data-ttu-id="3c7da-111">Dans la liste liste de listes des **défaillances** de vision Émuler, **sélectionnez Vision floue.**</span><span class="sxs-lookup"><span data-stu-id="3c7da-111">In the **Emulate vision deficiencies** dropdown list, select **Blurred vision**.</span></span>

    :::image type="complex" source="../media/a11y-testing-simulating-blur.msft.png" alt-text="Simulation d’une page floue" lightbox="../media/a11y-testing-simulating-blur.msft.png":::
        <span data-ttu-id="3c7da-113">Simulation d’une page floue</span><span class="sxs-lookup"><span data-stu-id="3c7da-113">Simulating a blurred page</span></span>
    :::image-end:::

    <span data-ttu-id="3c7da-114">Notez que la propriété CSS complique la lecture du texte des éléments `text-shadow` de menu dans le menu supérieur.</span><span class="sxs-lookup"><span data-stu-id="3c7da-114">Notice that the `text-shadow` CSS property makes the text of the menu items difficult to read on the upper menu.</span></span> <span data-ttu-id="3c7da-115">Par exemple, examinez **la page d’accueil**, **Adopter un**enfant de compagnie et d’autres éléments de menu.</span><span class="sxs-lookup"><span data-stu-id="3c7da-115">For example, review the **Home**, **Adopt a Pet**, and other menu items.</span></span>
    
1.  <span data-ttu-id="3c7da-116">Dans **l’outil de** rendu, dans Émuler les **défaillances visuelles,** sélectionnez Aucune **émulation** pour supprimer la simulation de vision floue.</span><span class="sxs-lookup"><span data-stu-id="3c7da-116">In the **Rendering** tool, in **Emulate vision deficiencies**, select **No emulation** to remove the blurred vision simulation.</span></span>


## <a name="see-also"></a><span data-ttu-id="3c7da-117">Articles associés</span><span class="sxs-lookup"><span data-stu-id="3c7da-117">See also</span></span>

*  [<span data-ttu-id="3c7da-118">Émuler les faiblesses de la vision</span><span class="sxs-lookup"><span data-stu-id="3c7da-118">Emulate vision deficiencies</span></span>](emulate-vision-deficiencies.md)
*  [<span data-ttu-id="3c7da-119">Vue d’ensemble des tests d’accessibilité à l’aide de DevTools</span><span class="sxs-lookup"><span data-stu-id="3c7da-119">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="3c7da-120">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="3c7da-120">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page web de démonstration de test d’accessibilité | GitHub"
