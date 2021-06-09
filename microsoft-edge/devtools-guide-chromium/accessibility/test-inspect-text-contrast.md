---
description: Vérifiez le contraste de couleur du texte dans l’état par défaut à l’aide de la superposition d’informations de l’outil Inspect sur la page, qui comporte une section Accessibilité qui inclut les informations de contraste.
title: Vérifier le contraste de couleur du texte à l’état par défaut à l’aide de l’outil Inspect
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: ade9fd6d685f6f7cea6311b1645a527ece352a38
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597332"
---
# <a name="check-text-color-contrast-in-the-default-state-using-the-inspect-tool"></a>Vérifier le contraste de couleur du texte à l’état par défaut à l’aide de l’outil Inspect

<!-- Inspect tool: information overlay: Accessibility section: Contrast row -->

Vérifiez le contraste de couleur du texte dans l’état par défaut à l’aide de **l’outil Inspect.**  La **superposition** des informations de l’outil Inspect sur la page web comporte une section **Accessibilité** qui inclut les **informations de** contraste.

Pour vérifier le contraste de couleur du texte à l’état par défaut à l’aide de la superposition d’informations de l’outil Inspect, effectuez les étapes suivantes.

<!-- Inspect tool -->
Pour les éléments qui ont du texte, **la** superposition des informations de l’outil Inspect affiche les éléments suivants :
*  Coefficient de contraste entre les couleurs de texte et d’arrière-plan.
*  Icône de coche verte pour les éléments avec un contraste suffisant.
*  Icône d’alerte jaune pour les éléments qui n’ont pas assez de contraste.

Dans certains cas, le contraste est affecté par la définition du navigateur sur le thème clair ou le thème foncé.

Par exemple, sur la page de démonstration, les liens bleus du menu **** de navigation de la barre latérale ont un contraste suffisant, mais le lien vert De la **section** État du don n’a pas assez de contraste.  Examinez ces éléments à l’aide **de l’outil Inspect,** comme suit :

1.  Ouvrez la [page web de démonstration des tests d’accessibilité][DevToolsA11yErrorsDemopage] dans un nouvel onglet.  Sélectionnez **ensuite F12** pour ouvrir DevTools.

1.  Sélectionnez **le bouton Inspect** \( Inspect button \) dans le coin supérieur gauche de ![ DevTools afin que l’icône soit mise en surbrillant ](../media/inspect-icon.msft.png) (bleu).

1.  Dans la page web rendue, pointez sur le lien **chats** bleus du menu de navigation de la barre latérale.  La **superposition des** informations de l’outil Inspect s’affiche.  Dans la section **Accessibilité** de la superposition d’informations, une coche verte apparaît sur la ligne **Contrast,** indiquant que cet élément présente un contraste suffisant entre la couleur du texte et la couleur d’arrière-plan.

    :::image type="complex" source="../media/a11y-testing-enough-contrast.msft.png" alt-text="Les éléments de menu ont un contraste suffisant, comme illustré dans l’outil Inspect" lightbox="../media/a11y-testing-enough-contrast.msft.png":::
        Les éléments de menu ont un contraste suffisant, comme illustré dans l’outil Inspect
    :::image-end:::

1.  Dans la page web rendue, dans la section **État du** don, pointez sur le lien **Chiens.**  La **superposition** des informations de l’outil Inspect affiche un point d’exclamation orange sur la ligne **Contrast,** indiquant que cet élément ne présente pas suffisamment de contraste entre le texte et les couleurs d’arrière-plan.

    :::image type="complex" source="../media/a11y-testing-not-enough-contrast.msft.png" alt-text="Un élément qui n’a pas assez de contraste, comme illustré par l’avertissement dans l’outil Inspect" lightbox="../media/a11y-testing-not-enough-contrast.msft.png":::
        Un élément qui n’a pas assez de contraste, comme illustré par l’avertissement dans l’outil Inspect
    :::image-end:::


## <a name="different-options-to-inspect-text-color-contrast-in-devtools"></a>Différentes options pour inspecter le contraste de couleur du texte dans DevTools

Utilisez les fonctionnalités DevTools suivantes pour inspecter le contraste de couleur du texte.

*  Utilisez **l’outil Inspect** (comme superposition d’informations sur la page web) pour vérifier si un élément de page individuel possède un contraste de couleur de texte suffisant.  La **superposition** des informations de l’outil Inspect inclut une section **Accessibilité** qui comporte une ligne **d’informations** de contraste.  **L’outil Inspect** affiche uniquement les informations de contraste de texte pour l’état actuel.  Cette approche est décrite dans l’article actuel.

*  **L’outil Problèmes** signale automatiquement les problèmes de contraste de couleur pour la page web entière, lorsque le texte et la couleur d’arrière-plan ne sont pas suffisamment contrastées.  Cette approche est décrite dans [Vérifier que les couleurs du texte ont un contraste suffisant.](test-issues-tool.md#verify-that-text-colors-have-enough-contrast)

*  Émuler un état autre que l’état par défaut, tel que l’état, en utilisant l’état de l’élément bascule dans le volet Styles, décrit dans Vérifier l’accessibilité de tous les états des `hover` [éléments.](test-inspect-states.md) **** ****


## <a name="see-also"></a>Articles associés

*  [Vérifier l’accessibilité de tous les états d’éléments][DevtoolsAccessibilityTestInspectStates]
*  [Utiliser l’outil Inspect pour détecter les problèmes d’accessibilité en pointant sur la page web](test-inspect-tool.md)
*  [Vue d’ensemble des tests d’accessibilité à l’aide de DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevtoolsAccessibilityTestInspectStates]: test-inspect-states.md "Vérifier l’accessibilité de tous les états des éléments | Documents Microsoft"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page web de démonstration de test d’accessibilité | GitHub"
