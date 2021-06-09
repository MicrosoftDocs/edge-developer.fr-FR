---
description: Test de l’accessibilité à l’aide de l’onglet Accessibilité.
title: Tester l’accessibilité à l’aide de l’onglet Accessibilité
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 839feed56fc82af2b4d96a081c476696166075b9
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597402"
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
# <a name="test-accessibility-using-the-accessibility-tab"></a><span data-ttu-id="6aa4f-104">Tester l’accessibilité à l’aide de l’onglet Accessibilité</span><span class="sxs-lookup"><span data-stu-id="6aa4f-104">Test accessibility using the Accessibility tab</span></span>

<span data-ttu-id="6aa4f-105">**L’onglet** Accessibilité vous permet d’afficher l’arborescence d’accessibilité, les attributs ARIA et les propriétés d’accessibilité calculées des nodes DOM.</span><span class="sxs-lookup"><span data-stu-id="6aa4f-105">The **Accessibility** tab is where you view the accessibility tree, ARIA attributes, and computed accessibility properties of DOM nodes.</span></span>  

<span data-ttu-id="6aa4f-106">Pour ouvrir **l’onglet** Accessibilité :</span><span class="sxs-lookup"><span data-stu-id="6aa4f-106">To open the **Accessibility** tab:</span></span>

1.  <span data-ttu-id="6aa4f-107">Sélectionnez **l’outil Éléments.**</span><span class="sxs-lookup"><span data-stu-id="6aa4f-107">Select the **Elements** tool.</span></span>  
1.  <span data-ttu-id="6aa4f-108">Dans **l’arborescence DOM,** sélectionnez l’élément que vous souhaitez inspecter.</span><span class="sxs-lookup"><span data-stu-id="6aa4f-108">In the **DOM Tree**, select the element which you want to inspect.</span></span>  
1.  <span data-ttu-id="6aa4f-109">Sélectionnez **l’onglet** Accessibilité.  Vous devrez peut-être d’abord sélectionner le bouton Plus **d’onglets** \( le bouton Autres onglets \) à droite de ![ ](../media/more-tabs-icon.msft.png) **l’onglet Styles.**</span><span class="sxs-lookup"><span data-stu-id="6aa4f-109">Select the **Accessibility** tab.  You might need to first select the **More tabs** \(![the More tabs button](../media/more-tabs-icon.msft.png)\) button to the right of the **Styles** tab.</span></span>

:::image type="complex" source="../media/accessibility-elements-accessibility.msft.png" alt-text="Inspecter l’élément h1 de la page d’accueil DevTools dans l’onglet Accessibilité" lightbox="../media/accessibility-elements-accessibility.msft.png":::
   <span data-ttu-id="6aa4f-111">Inspecter `h1` l’élément de la page d’accueil DevTools dans **l’onglet** Accessibilité</span><span class="sxs-lookup"><span data-stu-id="6aa4f-111">Inspect the `h1` element of the DevTools homepage in the **Accessibility** tab</span></span>
:::image-end:::  


## <a name="view-the-position-of-an-element-in-the-accessibility-tree"></a><span data-ttu-id="6aa4f-112">Afficher la position d’un élément dans l’arborescence d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="6aa4f-112">View the position of an element in the Accessibility Tree</span></span>

<span data-ttu-id="6aa4f-113">[L’arborescence d’accessibilité][MDNAccessibilityTree] est un sous-ensemble de l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="6aa4f-113">The [accessibility tree][MDNAccessibilityTree] is a subset of the DOM tree.</span></span>  <span data-ttu-id="6aa4f-114">L’arborescence d’accessibilité contient uniquement les éléments de l’arborescence DOM qui sont pertinents et utiles pour afficher le contenu d’une page par le biais de technologies d’assistance telles que les lecteurs d’écran.</span><span class="sxs-lookup"><span data-stu-id="6aa4f-114">The accessibility tree only contains elements from the DOM tree that are relevant and useful for displaying the contents of a page through assistive technologies such as screen readers.</span></span>

<span data-ttu-id="6aa4f-115">Examinez la position d’un élément dans l’arborescence d’accessibilité à partir de **l’onglet** Accessibilité.</span><span class="sxs-lookup"><span data-stu-id="6aa4f-115">Inspect the position of an element in the accessibility tree from the **Accessibility** tab.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-tree.msft.png" alt-text="Section Arborescence de l’accessibilité" lightbox="../media/accessibility-elements-accessibility-tree.msft.png":::
   <span data-ttu-id="6aa4f-117">Section Arborescence **de l’accessibilité**</span><span class="sxs-lookup"><span data-stu-id="6aa4f-117">The **Accessibility Tree** section</span></span>  
:::image-end:::  


## <a name="view-the-aria-attributes-of-an-element"></a><span data-ttu-id="6aa4f-118">Afficher les attributs ARIA d’un élément</span><span class="sxs-lookup"><span data-stu-id="6aa4f-118">View the ARIA attributes of an element</span></span>  

<span data-ttu-id="6aa4f-119">Les attributs ARIA garantissent que les technologies d’assistance telles que les lecteurs d’écran ont toutes les informations dont ils ont besoin pour représenter correctement le contenu d’une page.</span><span class="sxs-lookup"><span data-stu-id="6aa4f-119">ARIA attributes ensure that assistive technologies such as screen readers have all of the information that they need in order to properly represent the contents of a page.</span></span>  

<span data-ttu-id="6aa4f-120">Affichez les attributs ARIA d’un élément dans **l’onglet** Accessibilité.</span><span class="sxs-lookup"><span data-stu-id="6aa4f-120">View the ARIA attributes of an element in the **Accessibility** tab.</span></span>

:::image type="complex" source="../media/accessibility-elements-accessibility-aria-attributes.msft.png" alt-text="Section Attributs ARIA" lightbox="../media/accessibility-elements-accessibility-aria-attributes.msft.png":::
   <span data-ttu-id="6aa4f-122">Section **Attributs ARIA**</span><span class="sxs-lookup"><span data-stu-id="6aa4f-122">The **ARIA Attributes** section</span></span>  
:::image-end:::  


## <a name="view-the-computed-accessibility-properties-of-an-element"></a><span data-ttu-id="6aa4f-123">Afficher les propriétés d’accessibilité calculées d’un élément</span><span class="sxs-lookup"><span data-stu-id="6aa4f-123">View the computed accessibility properties of an element</span></span>  


<span data-ttu-id="6aa4f-124">Certaines propriétés d’accessibilité sont calculées dynamiquement par le navigateur.</span><span class="sxs-lookup"><span data-stu-id="6aa4f-124">Some accessibility properties are dynamically calculated by the browser.</span></span>  <span data-ttu-id="6aa4f-125">Ces propriétés sont affichées dans la section **Propriétés** calculées de **l’onglet** Accessibilité.</span><span class="sxs-lookup"><span data-stu-id="6aa4f-125">These properties are displayed in the **Computed Properties** section of the **Accessibility** tab.</span></span>  

<span data-ttu-id="6aa4f-126">Affichez les propriétés d’accessibilité calculées d’un élément dans **l’onglet** Accessibilité.</span><span class="sxs-lookup"><span data-stu-id="6aa4f-126">View the computed accessibility properties of an element in the **Accessibility** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="6aa4f-127">Pour les propriétés CSS calculées, utilisez [l’onglet][DevtoolsCssReferenceViewActuallyAppliedElements] Calculé.</span><span class="sxs-lookup"><span data-stu-id="6aa4f-127">For computed CSS properties, use the [Computed][DevtoolsCssReferenceViewActuallyAppliedElements] tab.</span></span>

:::image type="complex" source="../media/accessibility-elements-accessibility-computed-properties.msft.png" alt-text="Section Propriétés calculées de l’onglet Accessibilité" lightbox="../media/accessibility-elements-accessibility-computed-properties.msft.png":::
   <span data-ttu-id="6aa4f-129">Section **Propriétés calculées** de l’onglet Accessibilité \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="6aa4f-129">The **Computed Properties** section of the **Accessibility** tab</span></span>  
:::image-end:::  


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="6aa4f-130">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="6aa4f-130">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


> [!NOTE]
> <span data-ttu-id="6aa4f-131">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6aa4f-131">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6aa4f-132">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="6aa4f-132">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="6aa4f-134">Ce travail est sous [licence internationale Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6aa4f-134">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  


<!-- links -->
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Afficher uniquement le CSS réellement appliqué à un élément - CSS Reference | Documents Microsoft"  
[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Arborescence d’accessibilité (AOM) | MDN"  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
