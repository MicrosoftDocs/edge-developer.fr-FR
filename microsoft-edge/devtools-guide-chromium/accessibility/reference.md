---
title: Référence sur l’accessibilité
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: a338e78957d664a4552e5882f1ae7882f0eee89a
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986086"
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

# Référence sur l’accessibilité  

Cette page est une référence complète des fonctionnalités d’accessibilité dans Microsoft Edge DevTools.  Ce service est destiné aux développeurs Web qui:  

*   Découvrir les notions de base de DevTools, par exemple pour l’ouvrir.  
*   Vous connaissez les [principes et les pratiques d’accessibilité][MDNAccessibility].  
    
Cette référence a pour but de vous aider à découvrir les outils disponibles dans DevTools qui vous aident à examiner l’accessibilité d’une page.  

Pour plus d’informations sur la navigation dans DevTools à l’aide d’une technologie d’assistance telle qu’un lecteur d’écran, reportez-vous à la rubrique [navigation dans Microsoft Edge devtools avec la technologie d’assistance][DevtoolsAccessibilityNavigation] .  

## Vue d’ensemble des fonctionnalités d’accessibilité dans Microsoft Edge DevTools  

Cette section décrit la façon dont DevTools s’inscrit dans votre kit de fonctions d’accessibilité global.  

Lorsque vous déterminez s’il est possible d’accéder à une page, vous devez avoir 2 questions générales à retenir:  

1.  Êtes-vous en mesure de naviguer sur la page à l’aide d’un clavier ou d’un [lecteur d’écran][MDNScreenReader]?  
1.  Les éléments de la page sont-ils correctement marqués pour les lecteurs d’écran?  
    
En général, DevTools devrait vous aider à résoudre les erreurs liées aux questions #2, car ces erreurs sont faciles à détecter de manière automatisée.  Le #1 de questions est comme important, mais malheureusement DevTools ne vous permet pas de le faire.  La seule façon de rechercher les erreurs liées aux questions #1 est d’essayer d’utiliser une page à l’aide d’un clavier ou d’un lecteur d’écran.  <!--See [How To Do An Accessibility Review][AccessibilityReview] to learn more.  -->  

<!--[AccessibilityReview]: /web/fundamentals/accessibility/how-to-review  -->  

## Auditer l’accessibilité d’une page  

> [!NOTE]
> Le volet **audits** fournit des liens vers du contenu hébergé sur des sites Web tiers.  Microsoft n’est pas responsable et n’a aucun contrôle sur le contenu de ces sites et sur les données qui pourraient être collectées.  

En règle générale, utilisez le volet audits pour déterminer si:  

*   Une page est correctement marquée pour les lecteurs d’écran.  
*   Les éléments de texte sur une page présentent des coefficients de contraste suffisants.  Voir [afficher le coefficient de contraste d’un élément de texte dans le sélecteur de couleurs](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).  

Pour auditer une page:  

1.  Accédez à l’URL que vous voulez auditer.  
1.  Dans DevTools, cliquez sur l’onglet **audits** .  DevTools vous présente diverses options de configuration.  
    
    :::image type="complex" source="../media/accessibility-audits-pane.msft.png" alt-text="Configurer les audits" lightbox="../media/accessibility-audits-pane.msft.png":::
       Configurer les audits  
    :::image-end:::  
    
    > [!NOTE]
    > Les captures d’écran de cette section ont été effectuées avec la version 79 de Microsoft Edge.  Vous pouvez vérifier la version que vous utilisez `edge://version` .  L’interface utilisateur du panneau **audits** est différente dans les versions antérieures de Microsoft Edge, mais le flux de travail général est le même.  
    
1.  Pour **appareil**, sélectionnez **mobile** si vous voulez simuler un appareil mobile.  Cette option modifie votre chaîne d’agent utilisateur et redimensionne la fenêtre d’affichage.  Si la version mobile de la page ne s’affiche pas comme la version de bureau, cette option peut avoir un effet notable sur les résultats de votre audit.  
1.  Dans la section **audits** , vérifiez que l’option **accessibilité** est activée.  Désactivez les autres catégories si vous voulez les exclure de votre rapport.  Laissez-les activés si vous voulez découvrir d’autres façons d’améliorer la qualité de votre page.  
1.  La section **limitation** vous permet de limiter le réseau et le processeur, ce qui est utile lors de l’analyse des performances de chargement.  Cette option n’est pas adaptée à votre score d’accessibilité, donc vous pouvez utiliser ce que vous préférez.  
1.  La case à cocher **Clear Storage** vous permet d’effacer tout le stockage avant de charger la page ou de conserver le stockage entre les chargements de pages.  Cette option n’est pas non plus pertinente pour votre score d’accessibilité, vous pouvez donc utiliser ce que vous préférez.  
1.  Cliquez sur **exécuter les audits**. Après 10 à 30 secondes, DevTools fournit un rapport.  Votre rapport vous donne différentes astuces pour améliorer l’accessibilité de la page.  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result.msft.png" alt-text="Un rapport" lightbox="../media/accessibility-audits-run-audits-result.msft.png":::
       Un rapport  
    :::image-end:::  
    
1.  Cliquez sur un audit pour en savoir plus à son sujet.  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png" alt-text="Plus d’informations sur un audit" lightbox="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png":::
       Plus d’informations sur un audit  
    :::image-end:::  
    
1.  Cliquez sur **en savoir plus** pour afficher la documentation de ce contrôle.  
    
    :::image type="complex" source="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png" alt-text="Afficher la documentation d’un audit" lightbox="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png":::
       Afficher la documentation d’un audit  
    :::image-end:::  
    
### Voir aussi: extension de la hache  

Il est possible que vous préfériez utiliser l’extension de la [hache][ChromeWebStoreAxe] plutôt que le panneau **audits** .  
L’extension de la hache fournit généralement les mêmes informations, car il s’agit du moteur sous-jacent qui alimente le panneau audits.  L’extension de aXe a une interface utilisateur différente et décrit les audits légèrement différemment.  
Un des avantages que l’extension de aXe a sur le panneau **d’audit** est qu’il vous permet d’inspecter et de mettre en surbrillance les nœuds défectueux.  

:::image type="complex" source="../media/accessibility-devtools-extension-axe-panel.msft.png" alt-text="Extension de la hache" lightbox="../media/accessibility-devtools-extension-axe-panel.msft.png":::
   Extension de la hache  
:::image-end:::  

## Volet accessibilité  

Le volet **accessibilité** vous permet d’afficher l’arborescence d’accessibilité, les attributs Aria et les propriétés d’accessibilité calculée des nœuds DOM.  

Pour ouvrir le volet **accessibilité** :  

1.  Cliquez sur l’onglet **éléments** .  
1.  Dans l' **arborescence DOM**, sélectionnez l’élément que vous voulez inspecter.  
1.  Cliquez sur l’onglet **accessibilité** .  Il est possible qu’il soit masqué derrière le bouton **plus d’onglets** \ ( ![ plus d’onglets ][ImageMoreTabsIcon] \).  

:::image type="complex" source="../media/accessibility-elements-accessibility.msft.png" alt-text="Inspecter l’élément H1 de la page d’accueil de DevTools dans le volet accessibilité" lightbox="../media/accessibility-elements-accessibility.msft.png":::
   Inspecter l' `h1` élément de la page d’accueil devtools dans le volet **accessibilité**  
:::image-end:::  

### Afficher la position d’un élément dans l’arborescence d’accessibilité  

L' [arborescence d’accessibilité][MDNAccessibilityTree] est un sous-ensemble de l’arborescence DOM.  Il contient uniquement des éléments de l’arborescence DOM qui sont pertinents et utiles pour afficher le contenu d’une page dans un lecteur d’écran.  

Inspectez la position d’un élément dans l’arborescence d’accessibilité à partir du [volet accessibilité](#the-accessibility-pane).  

:::image type="complex" source="../media/accessibility-elements-accessibility-tree.msft.png" alt-text="Section arborescence d’accessibilité" lightbox="../media/accessibility-elements-accessibility-tree.msft.png":::
   Section **arborescence d’accessibilité**  
:::image-end:::  

### Afficher les attributs ARIA d’un élément  

Les attributs ARIA garantissent que les lecteurs d’écran disposent de toutes les informations dont ils ont besoin pour représenter correctement le contenu d’une page.  

Affichez les attributs ARIA d’un élément dans le [volet accessibilité](#the-accessibility-pane).  

:::image type="complex" source="../media/accessibility-elements-accessibility-aria-attributes.msft.png" alt-text="Section attributs ARIA" lightbox="../media/accessibility-elements-accessibility-aria-attributes.msft.png":::
   Section **attributs Aria**  
:::image-end:::  

### Afficher les propriétés d’accessibilité calculées d’un élément  

> [!NOTE]
> Si vous recherchez des propriétés CSS calculées, voir l' [onglet calculé][DevtoolsCssReferenceViewActuallyAppliedElements].  

Certaines propriétés d’accessibilité sont calculées de manière dynamique par le navigateur.  Ces propriétés sont affichées dans la section **propriétés calculées** du volet **accessibilité** .  

Afficher les propriétés d’accessibilité calculées d’un élément dans le [volet accessibilité](#the-accessibility-pane).  

:::image type="complex" source="../media/accessibility-elements-accessibility-computed-properties.msft.png" alt-text="Section Propriétés calculées du volet accessibilité" lightbox="../media/accessibility-elements-accessibility-computed-properties.msft.png":::
   Section **propriétés calculées** du volet **accessibilité**  
:::image-end:::  

## Afficher le coefficient de contraste d’un élément de texte dans le sélecteur de couleurs  

Certaines personnes souffrant de troubles de la vue ne voient pas les zones comme très brillantes ou très sombres.  Tout a tendance à apparaître à la même luminosité, ce qui permet de distinguer les plans et les bords.  

Coefficient de contraste mesure la différence de luminosité entre le premier plan et l’arrière-plan du texte.  Si votre texte a un coefficient de contraste faible, il est possible que les utilisateurs malvoyants puissent littéralement voir votre site comme un écran vierge.  

Le sélecteur de couleurs permet de vérifier que votre texte répond aux niveaux de contraste recommandés:  

1.  Cliquez sur l’onglet **éléments** .  
1.  Dans l' **arborescence DOM**, sélectionnez l’élément de texte que vous voulez inspecter.  
    
    :::image type="complex" source="../media/accessibility-elements-paragraph-highlight.msft.png" alt-text="Inspecter un paragraphe dans l’arborescence DOM" lightbox="../media/accessibility-elements-paragraph-highlight.msft.png":::
       Inspecter un paragraphe dans l' **arborescence DOM**  
    :::image-end:::  
    
1.  Dans le volet **styles** , cliquez sur le carré de couleur en regard de la `color` valeur de l’élément.  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png" alt-text="La propriété Color de l’élément" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png":::
       La `color` propriété de l’élément  
    :::image-end:::  
    
1.  Vérifiez la section **coefficient de contraste** du sélecteur de couleurs.  Une coche signifie que l’élément est conforme à la [recommandation minimum][W3CContrastMinimum].  Deux coches signifient qu’il est conforme à la [recommandation améliorée][W3CContrastEnhanced].  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png" alt-text="La section coefficient de contraste du sélecteur de couleurs affiche 2 coches et une valeur de 13,97" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png":::
       La section **coefficient de contraste** du sélecteur de couleurs affiche 2 coches et une valeur de `13.97`  
    :::image-end:::  
    
1.  Cliquez sur la section **coefficient de contraste** pour afficher des informations supplémentaires.  Une ligne s’affiche dans le sélecteur de visuels en haut du sélecteur de couleurs.  Si la couleur actuelle répond aux recommandations, tout ce qui se trouve sur le même côté de la ligne répond également aux recommandations.  Si la couleur en cours ne répond pas aux recommandations, tout ce qui se trouve dans le même côté ne répond pas aux recommandations.  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png" alt-text="Ligne de coefficient de contraste dans le sélecteur visuel" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png":::
       Ligne de **coefficient de contraste** dans le sélecteur visuel  
    :::image-end:::  
    
<!--## Feedback   -->  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  

<!-- links -->  

[DevtoolsAccessibilityNavigation]: ./navigation.md "Navigation dans Microsoft Edge DevTools avec la technologie d’assistance | Documents Microsoft"  
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Afficher uniquement les feuilles CSS appliquées actuellement à une référence d’élément CSS | Documents Microsoft"  

[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "axe-tests d’accessibilité sur le Web-chrome Web Store"  

[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Arborescence d’accessibilité (AOM) | MDN"  
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Accessibilité | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Lecteur d’écran | MDN"  

[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Niveau de contraste (amélioré) AAA | W3C"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Contraste (minimum) niveau AA | W3C"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
