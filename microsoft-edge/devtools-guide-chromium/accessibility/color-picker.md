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
# <a name="test-text-color-contrast-using-the-color-picker"></a>Tester le contraste de couleur du texte à l’aide du s sélectionneur de couleurs

Les personnes ayant une vision faible peuvent ne pas voir les zones qui sont très claires ou très sombres.  Tout a tendance à apparaître au même niveau de luminosité, ce qui rend difficile la distinction entre les contours et les bords.  

Le coefficient de contraste mesure la différence de luminosité entre le premier plan et l’arrière-plan du texte.  Si votre texte présente un faible coefficient de contraste, les personnes ayant une vision faible peuvent voir votre site comme un écran vide.  

Dans DevTools, l’une des façons d’afficher le coefficient de contraste d’un élément de texte consiste à utiliser le s picker de couleur, à partir de **l’onglet Styles.**  Le s picker de couleur vous permet de vérifier que votre texte répond aux niveaux de coefficient de contraste recommandés.

**Pour vérifier le contraste de couleur du texte à l’aide du s picker de couleur :**

1.  Dans DevTools, sélectionnez **l’outil Elements.**  
1.  Dans **l’arborescence DOM,** sélectionnez l’élément de texte à inspecter.  
    
    :::image type="complex" source="../media/accessibility-elements-paragraph-highlight.msft.png" alt-text="Inspecter un paragraphe dans l’arborescence DOM" lightbox="../media/accessibility-elements-paragraph-highlight.msft.png":::
       Inspecter un paragraphe dans **l’arborescence DOM**  
    :::image-end:::  
    
1.  Sous **l’onglet Styles,** recherchez la propriété de couleur qui est appliquée à l’élément, puis sélectionnez le carré de couleur à côté de la **propriété de** couleur. ****
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png" alt-text="Propriété de couleur de l’élément" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png":::
       Propriété `color` de l’élément  
    :::image-end:::  
    
1.  Examinez la section **Coefficient de** contraste du s sélectionneur de couleurs.  Une coche signifie que l’élément répond à la [recommandation minimale.][W3CContrastMinimum]  Deux coches signifient qu’elle répond à la [recommandation améliorée.][W3CContrastEnhanced]  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png" alt-text="La section Coefficient de contraste du s picker de couleur affiche 2 coches et une valeur de 13,97" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png":::
       La section **Coefficient de** contraste du s picker de couleur affiche 2 coches et une valeur de `13.97`  
    :::image-end:::  
    
1.  Pour plus d’informations, sélectionnez la section **Coefficient de** contraste pour la développer.  Dans le s picker visuel en haut du s picker de couleurs, deux lignes s’affichent, s’exécutant sur le s picker visuel, ainsi qu’un cercle pour la couleur actuelle.  Si la couleur actuelle répond aux recommandations, tout ce qui se place du même côté de la ligne répond également à des recommandations.  Si la couleur actuelle ne répond pas aux recommandations, tout ce qui se présente du même côté ne répond pas non plus aux recommandations.  

    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png" alt-text="Ligne coefficient de contraste dans le s picker visuel" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png":::
       Ligne **coefficient de contraste** dans le s picker visuel  
    :::image-end:::  

1. Pour essayer différentes couleurs, sélectionnez dans le sélecateur visuel ou sélectionnez un échantillon de couleur en bas du sélecateur de couleurs.
    

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est sous [licence internationale Creative Commons Attribution 4.0][CCA4IL].  


<!-- links -->  
[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Contraste (amélioré) Niveau AAA | W3C"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Contraste (Minimum) Niveau AA | W3C"  
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
