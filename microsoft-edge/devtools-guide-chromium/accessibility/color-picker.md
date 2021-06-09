---
description: Test du contraste de couleur du texte à l’aide du s sélectionneur de couleurs.
title: Tester le contraste de couleur du texte à l’aide du s sélectionneur de couleurs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: f4ba5f3706460c443ae06a393e5ef63e5d336229
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597398"
---
<!-- this article was created on 05/11/2021 by moving a section out from the "Accessibility reference" article (reference.md) -->
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="test-text-color-contrast-using-the-color-picker"></a><span data-ttu-id="219d2-104">Tester le contraste de couleur du texte à l’aide du s sélectionneur de couleurs</span><span class="sxs-lookup"><span data-stu-id="219d2-104">Test text-color contrast using the Color Picker</span></span>

<span data-ttu-id="219d2-105">Les personnes ayant une vision faible peuvent ne pas voir les zones qui sont très claires ou très sombres.</span><span class="sxs-lookup"><span data-stu-id="219d2-105">People with low vision may not see areas that are very bright or very dark.</span></span>  <span data-ttu-id="219d2-106">Tout a tendance à apparaître au même niveau de luminosité, ce qui rend difficile la distinction entre les contours et les bords.</span><span class="sxs-lookup"><span data-stu-id="219d2-106">Everything tends to appear at about the same level of brightness, which makes it hard to distinguish outlines and edges.</span></span>  

<span data-ttu-id="219d2-107">Le coefficient de contraste mesure la différence de luminosité entre le premier plan et l’arrière-plan du texte.</span><span class="sxs-lookup"><span data-stu-id="219d2-107">Contrast ratio measures the difference in brightness between the foreground and background of text.</span></span>  <span data-ttu-id="219d2-108">Si votre texte présente un faible coefficient de contraste, les personnes ayant une vision faible peuvent voir votre site comme un écran vide.</span><span class="sxs-lookup"><span data-stu-id="219d2-108">If your text has a low contrast ratio, then people with low vision may experience your site as a blank screen.</span></span>  

<span data-ttu-id="219d2-109">Dans DevTools, l’une des façons d’afficher le coefficient de contraste d’un élément de texte consiste à utiliser le s picker de couleur, à partir de **l’onglet Styles.**  Le s picker de couleur vous permet de vérifier que votre texte répond aux niveaux de coefficient de contraste recommandés.</span><span class="sxs-lookup"><span data-stu-id="219d2-109">In DevTools, one way to view the contrast ratio of a text element is to use the Color Picker, from the **Styles** tab.  The Color Picker helps you verify that your text meets recommended contrast ratio levels.</span></span>

**<span data-ttu-id="219d2-110">Pour vérifier le contraste de couleur du texte à l’aide du s picker de couleur :</span><span class="sxs-lookup"><span data-stu-id="219d2-110">To check the text-color contrast using the Color Picker:</span></span>**

1.  <span data-ttu-id="219d2-111">Dans DevTools, sélectionnez **l’outil Elements.**</span><span class="sxs-lookup"><span data-stu-id="219d2-111">In DevTools, select the **Elements** tool.</span></span>  
1.  <span data-ttu-id="219d2-112">Dans **l’arborescence DOM,** sélectionnez l’élément de texte à inspecter.</span><span class="sxs-lookup"><span data-stu-id="219d2-112">In the **DOM Tree**, select the text element that you want to inspect.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-paragraph-highlight.msft.png" alt-text="Inspecter un paragraphe dans l’arborescence DOM" lightbox="../media/accessibility-elements-paragraph-highlight.msft.png":::
       <span data-ttu-id="219d2-114">Inspecter un paragraphe dans **l’arborescence DOM**</span><span class="sxs-lookup"><span data-stu-id="219d2-114">Inspect a paragraph in the **DOM Tree**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="219d2-115">Sous **l’onglet Styles,** recherchez la propriété de couleur qui est appliquée à l’élément, puis sélectionnez le carré de couleur à côté de la **propriété de** couleur. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="219d2-115">On the **Styles** tab, locate the **color** property that's applied to the element, and then select the color square next to the **color** property.</span></span>
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png" alt-text="Propriété de couleur de l’élément" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png":::
       <span data-ttu-id="219d2-117">Propriété `color` de l’élément</span><span class="sxs-lookup"><span data-stu-id="219d2-117">The `color` property of the element</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="219d2-118">Examinez la section **Coefficient de** contraste du s sélectionneur de couleurs.</span><span class="sxs-lookup"><span data-stu-id="219d2-118">Examine the **Contrast Ratio** section of the Color Picker.</span></span>  <span data-ttu-id="219d2-119">Une coche signifie que l’élément répond à la [recommandation minimale.][W3CContrastMinimum]</span><span class="sxs-lookup"><span data-stu-id="219d2-119">One check mark means that the element meets the [minimum recommendation][W3CContrastMinimum].</span></span>  <span data-ttu-id="219d2-120">Deux coches signifient qu’elle répond à la [recommandation améliorée.][W3CContrastEnhanced]</span><span class="sxs-lookup"><span data-stu-id="219d2-120">Two check marks means that it meets the [enhanced recommendation][W3CContrastEnhanced].</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png" alt-text="La section Coefficient de contraste du s picker de couleur affiche 2 coches et une valeur de 13,97" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png":::
       <span data-ttu-id="219d2-122">La section **Coefficient de** contraste du s picker de couleur affiche 2 coches et une valeur de</span><span class="sxs-lookup"><span data-stu-id="219d2-122">The **Contrast Ratio** section of the Color Picker shows 2 check marks and a value of</span></span> `13.97`  
    :::image-end:::  
    
1.  <span data-ttu-id="219d2-123">Pour plus d’informations, sélectionnez la section **Coefficient de** contraste pour la développer.</span><span class="sxs-lookup"><span data-stu-id="219d2-123">For more information, select the **Contrast ratio** section to expand it.</span></span>  <span data-ttu-id="219d2-124">Dans le s picker visuel en haut du s picker de couleurs, deux lignes s’affichent, s’exécutant sur le s picker visuel, ainsi qu’un cercle pour la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="219d2-124">In the visual picker at the top of the Color Picker, two lines appear, running across the visual picker, along with a circle for the current color.</span></span>  <span data-ttu-id="219d2-125">Si la couleur actuelle répond aux recommandations, tout ce qui se place du même côté de la ligne répond également à des recommandations.</span><span class="sxs-lookup"><span data-stu-id="219d2-125">If the current color meets recommendations, then anything on the same side of the line also meets recommendations.</span></span>  <span data-ttu-id="219d2-126">Si la couleur actuelle ne répond pas aux recommandations, tout ce qui se présente du même côté ne répond pas non plus aux recommandations.</span><span class="sxs-lookup"><span data-stu-id="219d2-126">If the current color does not meet recommendations, then anything on the same side also does not meet recommendations.</span></span>  

    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png" alt-text="Ligne coefficient de contraste dans le s picker visuel" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png":::
       <span data-ttu-id="219d2-128">Ligne **coefficient de contraste** dans le s picker visuel</span><span class="sxs-lookup"><span data-stu-id="219d2-128">The **Contrast Ratio** Line in the visual picker</span></span>  
    :::image-end:::  

1. <span data-ttu-id="219d2-129">Pour essayer différentes couleurs, sélectionnez dans le sélecateur visuel ou sélectionnez un échantillon de couleur en bas du sélecateur de couleurs.</span><span class="sxs-lookup"><span data-stu-id="219d2-129">To try different colors, select within the visual picker, or select a color swatch at the bottom of the Color Picker.</span></span>
    

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="219d2-130">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="219d2-130">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


> [!NOTE]
> <span data-ttu-id="219d2-131">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="219d2-131">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="219d2-132">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="219d2-132">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="219d2-134">Ce travail est sous [licence internationale Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="219d2-134">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  


<!-- links -->  
[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Contraste (amélioré) Niveau AAA | W3C"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Contraste (Minimum) Niveau AA | W3C"  
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
