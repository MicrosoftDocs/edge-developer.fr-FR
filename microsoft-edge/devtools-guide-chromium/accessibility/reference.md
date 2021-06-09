---
description: Liste des fonctionnalités de test d’accessibilité Microsoft Edge DevTools.
title: Fonctionnalités de test de l’accessibilité dans DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: a906d60bb74d927fd86c21af1535a8f62eb93cad
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597039"
---
# <a name="accessibility-testing-features-in-devtools"></a>Fonctionnalités de test de l’accessibilité dans DevTools

Pour tester l’accessibilité de vos pages web, faites d’abord une liste de vérification des aspects d’accessibilité à tester, puis utilisez les fonctionnalités DevTools pertinentes pour vérifier chaque aspect.

| Aspect accessibilité à vérifier | Fonctionnalité de DevTools | Article ou sous-titre |
|---|---|---|
| Vérifier que les images ont un texte de alt | **Outil Problèmes >** **section Accessibilité** du rapport | [Vérifier que les images ont un texte de alt](test-issues-tool.md#verify-that-images-have-alt-text) |
| Vérifier la prise en charge du clavier | **Inspect tool** > **Accessibility** section of overlay | [Utiliser l’outil Inspect pour détecter les problèmes d’accessibilité en pointant sur la page web](test-inspect-tool.md) |
| Vérifier la prise en charge du clavier | `Tab`, `Shift+Tab` et `Enter` clés | [Vérifier la prise en charge du clavier à l’aide des touches Tab et Entrée](test-tab-enter-keys.md) |
| Vérifier la prise en charge du clavier : vérifiez que le focus est indiqué | **Outil Inspect,** **onglet Styles** et **outil Sources** | [Analyser l’absence d’indication du focus du clavier dans un menu de barre latérale](test-analyze-no-focus-indicator.md) |
| Vérifier la prise en charge du clavier : vérifier que les boutons de formulaire peuvent être utilisés avec le clavier | **Inspecter** l’outil, **l’arborescence DOM** dans l’outil **Éléments** et l’onglet **Écouteurs d’événements** | [Analyser l’absence de prise en charge du clavier dans un formulaire](test-analyze-no-keyboard-support.md) |
| Vérifier la prise en charge du clavier : vérifier `Tab` l’ordre des touches | **Outil Éléments de** **>'onglet Accessibilité** > **l’Observateur de commandes source** | [Tester la prise en charge du clavier à l’aide de l’Observateur de commandes source](test-tab-key-source-order-viewer.md) |
| Vérifiez que le texte présente un contraste suffisant (automatiquement, pour la page entière) | **Outil Problèmes >** **section Accessibilité** du rapport | [Vérifier que le contraste des couleurs du texte est suffisant](test-issues-tool.md#verify-that-text-colors-have-enough-contrast) |
| Vérifier que le texte présente un contraste suffisant | **Outil Éléments** > **onglet Styles** > **s’il s’est s’il s’est choisi** | [Tester le contraste de couleur du texte à l’aide du s sélectionneur de couleurs](color-picker.md) |
| Vérifier que le texte présente un contraste suffisant | **Inspect tool** > **Accessibility** section of overlay > **Contrast** row | [Utiliser l’outil Inspect pour détecter les problèmes d’accessibilité en pointant sur la page web](test-inspect-tool.md) |
| Vérifiez que le texte présente un contraste suffisant : dans l’état de pointer | **Outil Éléments** > **onglet Styles** > **l’état de l’élément Bascule** | [Vérifier l’accessibilité de tous les états d’éléments](test-inspect-states.md) |
| Vérifiez que le texte présente un contraste suffisant : avec thème foncé (mode sombre) et thème clair | **Outil de** rendu > émuler la fonctionnalité **multimédia CSS prefers-color-scheme** | [Vérifier les problèmes de contraste avec le thème foncé et le thème clair](test-dark-mode.md) |
| Vérifier la prise en charge des lecteurs d’écran : vérifier que les champs d’entrée ont des étiquettes | **Outil Problèmes >** **section Accessibilité** du rapport | [Vérifier que les champs d’entrée ont des étiquettes](test-issues-tool.md#verify-that-input-fields-have-labels) |
| Vérifier la prise en charge des lecteurs d’écran | **Inspect** tool > **Accessibility** section of overlay > **Name** and **Role** | [Utiliser l’outil Inspect pour détecter les problèmes d’accessibilité en pointant sur la page web](test-inspect-tool.md) |
| Vérifier la prise en charge des lecteurs d’écran | **Outil Éléments** de **>'onglet Accessibilité** **>'arborescence d’accessibilité** | [Vérifiez l’arborescence d’accessibilité](test-accessibility-tree.md)pour la prise en charge du clavier et du lecteur d’écran, et testez l’accessibilité à l’aide de [l’onglet Accessibilité.](accessibility-tab.md) |
| Vérifier que la page web est utilisable par les personnes daltonismes | **Outil de** rendu > liste de listes **listes des défaillances** visuelles émuler | [Vérifier que la page est utilisable par les personnes daltonismes](test-color-blindness.md) |
| Vérifier que la page web est utilisable avec une vision floue | **Outil de** rendu > liste de listes **listes des défaillances** visuelles émuler | [Vérifier que la page est utilisable avec une vision floue](test-blurred-vision.md) |
| Vérifiez que la page web est utilisable avec l’animation de l’interface utilisateur désactivée (mouvement réduit) | **Outil de** rendu > émuler la fonctionnalité **multimédia CSS préfère un mouvement réduit** | [Vérifier que la page est utilisable avec l’animation de l’interface utilisateur désactivée](test-reduced-ui-motion.md) |
| Vérifier que la mise en page web est utilisable lorsqu’elle est étroite | **Outil Device Emulation** | [Vérifiez que la disposition de la page web est utilisable](accessibility-testing-in-devtools.md#verify-that-the-webpage-layout-is-usable-when-narrow)lorsqu’elle est étroite et émulez les appareils mobiles dans Microsoft Edge [DevTools](../device-mode/index.md) |


## <a name="see-also"></a>Articles associés

*   [Vue d’ensemble des tests d’accessibilité à l’aide de DevTools][DevtoolsAccessibilityAccessibilitytestingindevtools]
*   [Naviguer Microsoft Edge DevTools avec la technologie d’assistance][DevtoolsAccessibilityNavigation]
*   [Test de l’accessibilité][DevtoolsAccessibilityTest]
*   [Principes et meilleures pratiques en matière d’accessibilité][MDNAccessibility]
*   [Lecteur d’écran][MDNScreenReader]


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->  
[DevtoolsAccessibilityTest]: ../../accessibility/test.md "Test d’accessibilité | Documents Microsoft"
[DevtoolsAccessibilityAccessibilitytestingindevtools]: accessibility-testing-in-devtools.md "Vue d’ensemble des tests d’accessibilité à l’aide de DevTools | Documents Microsoft"
[DevtoolsAccessibilityNavigation]: ./navigation.md "Naviguer Microsoft Edge DevTools avec la technologie d’assistance | Documents Microsoft"  
<!-- external -->
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Accessibilité | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Lecteur d’écran | MDN"  
