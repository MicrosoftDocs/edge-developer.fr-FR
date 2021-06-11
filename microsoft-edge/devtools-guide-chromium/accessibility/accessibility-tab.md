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
# <a name="test-accessibility-using-the-accessibility-tab"></a>Tester l’accessibilité à l’aide de l’onglet Accessibilité

**L’onglet** Accessibilité vous permet d’afficher l’arborescence d’accessibilité, les attributs ARIA et les propriétés d’accessibilité calculées des nodes DOM.  

Pour ouvrir **l’onglet** Accessibilité :

1.  Sélectionnez **l’outil Éléments.**  
1.  Dans **l’arborescence DOM,** sélectionnez l’élément que vous souhaitez inspecter.  
1.  Sélectionnez **l’onglet** Accessibilité.  Vous devrez peut-être d’abord sélectionner le bouton Plus **d’onglets** \( le bouton Autres onglets \) à droite de ![ ](../media/more-tabs-icon.msft.png) **l’onglet Styles.**

:::image type="complex" source="../media/accessibility-elements-accessibility.msft.png" alt-text="Inspecter l’élément h1 de la page d’accueil DevTools dans l’onglet Accessibilité" lightbox="../media/accessibility-elements-accessibility.msft.png":::
   Inspecter `h1` l’élément de la page d’accueil DevTools dans **l’onglet** Accessibilité
:::image-end:::  


## <a name="view-the-position-of-an-element-in-the-accessibility-tree"></a>Afficher la position d’un élément dans l’arborescence d’accessibilité

[L’arborescence d’accessibilité][MDNAccessibilityTree] est un sous-ensemble de l’arborescence DOM.  L’arborescence d’accessibilité contient uniquement les éléments de l’arborescence DOM qui sont pertinents et utiles pour afficher le contenu d’une page par le biais de technologies d’assistance telles que les lecteurs d’écran.

Examinez la position d’un élément dans l’arborescence d’accessibilité à partir de **l’onglet** Accessibilité.  

:::image type="complex" source="../media/accessibility-elements-accessibility-tree.msft.png" alt-text="Section Arborescence de l’accessibilité" lightbox="../media/accessibility-elements-accessibility-tree.msft.png":::
   Section Arborescence **de l’accessibilité**  
:::image-end:::  


## <a name="view-the-aria-attributes-of-an-element"></a>Afficher les attributs ARIA d’un élément  

Les attributs ARIA garantissent que les technologies d’assistance telles que les lecteurs d’écran ont toutes les informations dont ils ont besoin pour représenter correctement le contenu d’une page.  

Affichez les attributs ARIA d’un élément dans **l’onglet** Accessibilité.

:::image type="complex" source="../media/accessibility-elements-accessibility-aria-attributes.msft.png" alt-text="Section Attributs ARIA" lightbox="../media/accessibility-elements-accessibility-aria-attributes.msft.png":::
   Section **Attributs ARIA**  
:::image-end:::  


## <a name="view-the-computed-accessibility-properties-of-an-element"></a>Afficher les propriétés d’accessibilité calculées d’un élément  


Certaines propriétés d’accessibilité sont calculées dynamiquement par le navigateur.  Ces propriétés sont affichées dans la section **Propriétés** calculées de **l’onglet** Accessibilité.  

Affichez les propriétés d’accessibilité calculées d’un élément dans **l’onglet** Accessibilité.

> [!NOTE]
> Pour les propriétés CSS calculées, utilisez [l’onglet][DevtoolsCssReferenceViewActuallyAppliedElements] Calculé.

:::image type="complex" source="../media/accessibility-elements-accessibility-computed-properties.msft.png" alt-text="Section Propriétés calculées de l’onglet Accessibilité" lightbox="../media/accessibility-elements-accessibility-computed-properties.msft.png":::
   Section **Propriétés calculées** de l’onglet Accessibilité ****  
:::image-end:::  


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est sous [licence internationale Creative Commons Attribution 4.0][CCA4IL].  


<!-- links -->
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Afficher uniquement le CSS réellement appliqué à un élément - CSS Reference | Documents Microsoft"  
[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Arborescence d’accessibilité (AOM) | MDN"  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
