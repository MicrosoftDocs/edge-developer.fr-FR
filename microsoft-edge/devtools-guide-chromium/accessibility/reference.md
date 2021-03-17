---
description: Référence complète des fonctionnalités d’accessibilité dans Microsoft Edge DevTools.
title: Référence d’accessibilité
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: fce6dec3883cbcc758780a9fedb4c0fb2a8d0a4c
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439253"
---
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

# <a name="accessibility-reference"></a>Référence d’accessibilité  

Cette page est une référence complète des fonctionnalités d’accessibilité dans Microsoft Edge DevTools.  Il est destiné aux développeurs web qui :  

*   Avoir une connaissance de base de DevTools, par exemple comment l’ouvrir.  
*   Familiarisez-vous [avec les principes d’accessibilité et les meilleures pratiques.][MDNAccessibility]  
    
L’objectif de cette référence est de vous aider à découvrir tous les outils disponibles dans DevTools qui vous aident à examiner l’accessibilité d’une page.  

Si vous recherchez de l’aide sur la navigation de DevTools avec une technologie d’assistance telle qu’un lecteur d’écran, accédez à Navigation dans [Microsoft Edge DevTools avec][DevtoolsAccessibilityNavigation]technologie d’assistance.  

## <a name="overview-of-accessibility-features-in-microsoft-edge-devtools"></a>Vue d’ensemble des fonctionnalités d’accessibilité dans Microsoft Edge DevTools  

Cette section explique comment DevTools s’inscrit dans votre kit de ressources d’accessibilité global.  

Lorsque vous déterminez si une page est accessible, vous devez avoir 2 questions générales à l’esprit :  

1.  Êtes-vous en mesure de naviguer dans la page à l’aide d’un clavier ou [d’un lecteur d’écran][MDNScreenReader]?  
1.  Les éléments de la page sont-ils correctement marqués pour les lecteurs d’écran ?  
    
En règle générale, DevTools doit vous aider à résoudre les erreurs liées aux #2, car ces erreurs sont faciles à détecter de manière automatisée.  La question #1 est tout aussi importante, mais malheureusement, DevTools ne vous aide pas.  La seule façon de rechercher les erreurs liées aux #1 question consiste à essayer d’utiliser une page avec un clavier ou un lecteur d’écran vous-même.  <!--To learn more, navigate to [How To Do An Accessibility Review][AccessibilityReview].  -->  

<!--[AccessibilityReview]: /web/fundamentals/accessibility/how-to-review  -->  

## <a name="audit-the-accessibility-of-a-page"></a>Auditer l’accessibilité d’une page  

> [!NOTE]
> **L’outil Audits** fournit des liens vers du contenu hébergé sur des sites web tiers.  Microsoft n’est pas responsable et n’a aucun contrôle sur le contenu de ces sites et les données qui peuvent être collectées.  

En règle générale, utilisez le panneau Audits pour déterminer si :  

*   Une page est correctement marquée pour les lecteurs d’écran.  
*   Les éléments de texte d’une page ont des coefficients de contraste suffisants.  Accédez [à Afficher le coefficient de contraste d’un élément de texte dans le s sélectionneur de couleurs.](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker)  

Pour auditer une page :  

1.  Accédez à l’URL que vous souhaitez auditer.  
1.  Dans DevTools, choisissez **l’outil Audits.**  DevTools vous présente différentes options de configuration.  
    
    :::image type="complex" source="../media/accessibility-audits-pane.msft.png" alt-text="Configurer les audits" lightbox="../media/accessibility-audits-pane.msft.png":::
       Configurer les audits  
    :::image-end:::  
    
    > [!NOTE]
    > Les captures d’écran de cette section ont été prises avec Microsoft Edge version 79.  Vous pouvez vérifier la version à partir de quelle version vous `edge://version` exécutez.  L’interface utilisateur de l’outil **Audits** est différente dans les versions antérieures de Microsoft Edge, mais le flux de travail général est le même.  
    
1.  Pour **l’appareil,** **choisissez Mobile** si vous souhaitez simuler un appareil mobile.  Cette option modifie la chaîne de votre agent utilisateur et resize laport d’affichage.  Si la version mobile de la page s’affiche différemment de la version de bureau, cette option peut avoir un impact significatif sur les résultats de votre audit.  
1.  Dans la section **Audits,** assurez-vous que **l’accessibilité** est activée.  Désactivez les autres catégories si vous souhaitez les exclure de votre rapport.  Laissez-les activées si vous souhaitez découvrir d’autres façons d’améliorer la qualité de votre page.  
1.  La section **Limitation vous** permet de limiter le réseau et le processeur, ce qui est utile lors de l’analyse des performances de charge.  Cette option ne doit pas être pertinente pour votre score d’accessibilité. Vous pouvez donc utiliser ce que vous préférez.  
1.  La **case à cocher** Effacer le stockage vous permet d’effacer tout le stockage avant de charger la page ou de conserver le stockage entre les chargements de page.  Cette option n’est probablement pas pertinente pour votre score d’accessibilité. Vous pouvez donc utiliser ce que vous préférez.  
1.  Choose **Run Audits**. Après 10 à 30 secondes, DevTools fournit un rapport.  Votre rapport vous donne différents conseils sur l’amélioration de l’accessibilité de la page.  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result.msft.png" alt-text="Un rapport" lightbox="../media/accessibility-audits-run-audits-result.msft.png":::
       Un rapport  
    :::image-end:::  
    
1.  Choisissez un audit pour en savoir plus à ce sujet.  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png" alt-text="Plus d’informations sur un audit" lightbox="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png":::
       Plus d’informations sur un audit  
    :::image-end:::  
    
1.  Sélectionnez **En savoir plus** pour afficher la documentation de cet audit.  
    
    :::image type="complex" source="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png" alt-text="Afficher la documentation d’un audit" lightbox="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png":::
       Afficher la documentation d’un audit  
    :::image-end:::  
    
### <a name="see-also-axe-extension"></a>Voir aussi : extension aXe  

Vous pouvez préférer utiliser [l’extension aXe plutôt][ChromeWebStoreAxe] que l’outil **Audits.**  
L’extension aXe fournit généralement les mêmes informations, car il s’agit du moteur sous-jacent qui alimente le panneau Audits.  L’extension aXe a une interface utilisateur différente et décrit les audits légèrement différemment.  
L’un des avantages de l’extension aXe par rapport à l’outil **Audits** est qu’elle vous permet d’inspecter et de mettre en surbrillez les points d’échec.  

:::image type="complex" source="../media/accessibility-devtools-extension-axe-panel.msft.png" alt-text="Extension aXe" lightbox="../media/accessibility-devtools-extension-axe-panel.msft.png":::
   Extension aXe  
:::image-end:::  

## <a name="the-accessibility-panel"></a>Panneau Accessibilité  

Le **panneau Accessibilité** vous permet d’afficher l’arborescence d’accessibilité, les attributs ARIA et les propriétés d’accessibilité calculées des nodes DOM.  

Pour ouvrir le panneau **Accessibilité** :  

1.  Choisissez **l’outil Éléments.**  
1.  Dans **l’arborescence DOM,** sélectionnez l’élément que vous souhaitez inspecter.  
1.  Choisissez le **panneau Accessibilité.**  Ce panneau peut être masqué derrière le bouton **Autres onglets** \( ![ Autres onglets ](../media/more-tabs-icon.msft.png) \).  

:::image type="complex" source="../media/accessibility-elements-accessibility.msft.png" alt-text="Inspecter l’élément h1 de la page d’accueil DevTools dans le panneau Accessibilité" lightbox="../media/accessibility-elements-accessibility.msft.png":::
   Inspecter `h1` l’élément de la page d’accueil DevTools dans le **panneau Accessibilité**  
:::image-end:::  

### <a name="view-the-position-of-an-element-in-the-accessibility-tree"></a>Afficher la position d’un élément dans l’arborescence d’accessibilité  

[L’arborescence d’accessibilité][MDNAccessibilityTree] est un sous-ensemble de l’arborescence DOM.  Il contient uniquement les éléments de l’arborescence DOM qui sont pertinents et utiles pour afficher le contenu d’une page dans un lecteur d’écran.  

Inspectez la position d’un élément dans l’arborescence d’accessibilité à partir du [panneau Accessibilité.](#the-accessibility-panel)  

:::image type="complex" source="../media/accessibility-elements-accessibility-tree.msft.png" alt-text="Section Arborescence de l’accessibilité" lightbox="../media/accessibility-elements-accessibility-tree.msft.png":::
   Section Arborescence **de l’accessibilité**  
:::image-end:::  

### <a name="view-the-aria-attributes-of-an-element"></a>Afficher les attributs ARIA d’un élément  

Les attributs ARIA garantissent que les lecteurs d’écran ont toutes les informations dont ils ont besoin pour représenter correctement le contenu d’une page.  

Afficher les attributs ARIA d’un élément dans le [panneau Accessibilité.](#the-accessibility-panel)  

:::image type="complex" source="../media/accessibility-elements-accessibility-aria-attributes.msft.png" alt-text="Section Attributs ARIA" lightbox="../media/accessibility-elements-accessibility-aria-attributes.msft.png":::
   Section **Attributs ARIA**  
:::image-end:::  

### <a name="view-the-computed-accessibility-properties-of-an-element"></a>Afficher les propriétés d’accessibilité calculées d’un élément  

> [!NOTE]
> Si vous recherchez des propriétés CSS calculées, accédez au [panneau][DevtoolsCssReferenceViewActuallyAppliedElements] calculé.  

Certaines propriétés d’accessibilité sont calculées dynamiquement par le navigateur.  Ces propriétés sont affichées dans la section **Propriétés** calculées du panneau **Accessibilité.**  

Afficher les propriétés d’accessibilité calculées d’un élément dans le [panneau Accessibilité.](#the-accessibility-panel)  

:::image type="complex" source="../media/accessibility-elements-accessibility-computed-properties.msft.png" alt-text="Section Propriétés calculées du panneau Accessibilité" lightbox="../media/accessibility-elements-accessibility-computed-properties.msft.png":::
   Section **Propriétés calculées** du panneau **Accessibilité**  
:::image-end:::  

## <a name="view-the-contrast-ratio-of-a-text-element-in-the-color-picker"></a>Afficher le coefficient de contraste d’un élément de texte dans le s sélectionneur de couleurs  

Certaines personnes ayant une vision faible ne voient pas les zones comme étant très claires ou très sombres.  Tout a tendance à apparaître à peu près à la même luminosité, ce qui rend difficile la distinction entre les contours et les bords.  

Le coefficient de contraste mesure la différence de luminosité entre le premier plan et l’arrière-plan du texte.  Si votre texte présente un faible coefficient de contraste, ces utilisateurs à faible vision peuvent littéralement voir votre site comme un écran vide.  

Le s picker de couleur vous permet de vérifier que votre texte répond aux niveaux de coefficient de contraste recommandés :  

1.  Choisissez **l’outil Éléments.**  
1.  Dans **l’arborescence DOM,** sélectionnez l’élément de texte à inspecter.  
    
    :::image type="complex" source="../media/accessibility-elements-paragraph-highlight.msft.png" alt-text="Inspecter un paragraphe dans l’arborescence DOM" lightbox="../media/accessibility-elements-paragraph-highlight.msft.png":::
       Inspecter un paragraphe dans l’arborescence **DOM**  
    :::image-end:::  
    
1.  Dans le **panneau Styles,** choisissez le carré de couleur en face de la `color` valeur de l’élément.  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png" alt-text="Propriété de couleur de l’élément" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png":::
       Propriété `color` de l’élément  
    :::image-end:::  
    
1.  Consultez la section **Coefficient de** contraste du s sélectionneur de couleurs.  Une coche signifie que l’élément répond à la [recommandation minimale.][W3CContrastMinimum]  Deux coches signifient qu’elle répond à la [recommandation améliorée][W3CContrastEnhanced].  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png" alt-text="La section Coefficient de contraste du s picker de couleur affiche 2 coches et une valeur de 13,97" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png":::
       La section **Coefficient de** contraste du s picker de couleur affiche 2 coches et une valeur de `13.97`  
    :::image-end:::  
    
1.  Pour plus d’informations, sélectionnez la section **Coefficient de** contraste.  Une ligne apparaît dans le s picker visuel en haut du s picker de couleurs.  Si la couleur actuelle répond aux recommandations, tout ce qui se place du même côté de la ligne répond également à des recommandations.  Si la couleur actuelle ne répond pas aux recommandations, tout ce qui se présente du même côté ne répond pas non plus aux recommandations.  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png" alt-text="Ligne coefficient de contraste dans le s picker visuel" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png":::
       Ligne **coefficient de contraste** dans le s picker visuel  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsAccessibilityNavigation]: ./navigation.md "Naviguer dans Microsoft Edge DevTools avec la technologie d’assistance | Documents Microsoft"  
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Afficher uniquement le CSS réellement appliqué à un élément - CSS Reference | Documents Microsoft"  

[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "axe - Test d’accessibilité web - Chrome Web Store"  

[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Arborescence d’accessibilité (AOM) | MDN"  
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Accessibilité | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Lecteur d’écran | MDN"  

[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Contraste (amélioré) Niveau AAA | W3C"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Contraste (Minimum) Niveau AA | W3C"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
