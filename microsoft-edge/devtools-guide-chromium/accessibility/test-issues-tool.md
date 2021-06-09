---
description: Testez automatiquement une page web pour les problèmes d’accessibilité à l’aide de la section Accessibilité de l’outil Problèmes.
title: Tester automatiquement une page web pour les problèmes d’accessibilité
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 986a021d2fd390cd45bd53dcfc37a83d58ed2338
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597334"
---
# <a name="automatically-test-a-webpage-for-accessibility-issues"></a>Tester automatiquement une page web pour les problèmes d’accessibilité

**L’outil** Problèmes inclut une **section** Accessibilité qui signale automatiquement des problèmes tels que l’absence de texte de remplacement sur les images, l’absence d’étiquettes dans les champs du formulaire et le contraste insuffisant des couleurs du texte.  **L’outil Problèmes** se trouve dans le **caisse** en bas de DevTools.  Cet article utilise la page web de démonstration des tests d’accessibilité pour passer pas à pas à l’aide de la section **Accessibilité** de **l’outil** Problèmes.

Il existe plusieurs façons d’ouvrir **l’outil Problèmes, telles** que :
*  Sélectionnez **le compteur Problèmes** \( Compteur de problèmes \) dans le coin supérieur droit de ![ ](../media/issues-counter-icon.msft.png) DevTools.
*  Dans **l’outil Elements,** dans l’arborescence DOM, **cliquez** sur un soulignement ondulé sur un élément.
*  Dans le **menu Commande,** `issues` tapez, puis sélectionnez **Afficher les problèmes.**


## <a name="view-the-accessibility-section-of-the-issues-tool"></a>Afficher la section Accessibilité de l’outil Problèmes

1.  Ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration des tests d’accessibilité dans un nouvel onglet du navigateur, puis sélectionnez **F12** pour ouvrir DevTools.  Dans le coin supérieur droit, le compteur Problèmes **\(** Compteur de problèmes \) apparaît sous la forme d’une icône de bulle vocale avec le nombre de problèmes ![ ](../media/issues-counter-icon.msft.png) détectés automatiquement.  Un autre numéro peut apparaître dans votre navigateur et le numéro peut être mis à jour lorsque vous utilisez DevTools.

    :::image type="complex" source="../media/a11y-testing-issues-tracker.msft.png" alt-text="Compteur Problèmes dans DevTools, indiquant le nombre de problèmes présents dans le document actuel" lightbox="../media/a11y-testing-issues-tracker.msft.png":::
        Compteur **Problèmes dans** DevTools, indiquant le nombre de problèmes présents dans le document actuel
    :::image-end:::

1.  Sélectionnez **le compteur Problèmes.**  **L’outil** Problèmes s’ouvre, dans le **caisse** en bas de DevTools.

    :::image type="complex" source="../media/a11y-testing-accessibility-issues.msft.png" alt-text="Avertissements d’accessibilité affichés dans l’outil Problèmes" lightbox="../media/a11y-testing-accessibility-issues.msft.png":::
        Avertissements d’accessibilité affichés dans l’outil Problèmes
    :::image-end:::

1.  Sous **l’onglet Problèmes,** développez la section **Accessibilité.**


## <a name="verify-that-input-fields-have-labels"></a>Vérifier que les champs d’entrée ont des étiquettes

Pour vérifier si des étiquettes sont **connectées** aux champs d’entrée, utilisez l’outil Problèmes, qui vérifie automatiquement l’intégralité de la page web et signale ce problème dans la **section** Accessibilité.

1.  Ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration des tests d’accessibilité dans un nouvel onglet du navigateur, puis sélectionnez **F12** pour ouvrir DevTools.

1.  Dans le coin supérieur droit, sélectionnez le compteur **Problèmes** \( ![ Compteur de problèmes ](../media/issues-counter-icon.msft.png) \).  **L’outil** Problèmes s’ouvre, dans le **caisse** en bas de DevTools.

1.  Sous **l’onglet Problèmes,** développez la section **Accessibilité.**

1.  Développez **l’avertissement** `Form elements must have labels: Element has no title attribute Element has no placeholder attribute` .

1. Sélectionnez **le lien Ouvrir dans les éléments.**

    :::image type="complex" source="../media/a11y-testing-inspect-problematic-element.msft.png" alt-text="Outil Éléments affichant le code HTML problématique après la sélection du lien dans l’outil Problèmes" lightbox="../media/a11y-testing-inspect-problematic-element.msft.png":::
        Outil Éléments affichant le code HTML problématique après la sélection du lien dans **l’outil** Problèmes :::image-end:::

    **L’outil Elements** s’ouvre, avec l’élément mis en surbrillant dans l’arborescence DOM.  Le **volet Styles** affiche les règles CSS appliquées pour l’élément.  Le code suivant s’affiche maintenant.

    ```html
    <label>Search</label>
    <input type="search">
    <input type="submit" value="go">
    ```

    Dans le code ci-dessus, l’élément est utilisé de manière incorrecte, car il n’existe aucune connexion entre l’élément `label` `label` et un élément `input` particulier.  Pour connecter `label` l’élément à un élément `input` spécifique, utilisez l’une des options suivantes.
    *   Imbribrier `input` l’élément dans `label` l’élément.
    *   Dans `label` l’élément, ajoutez `for` un attribut qui correspond à un attribut de `id` `input` l’élément.

    Il existe également une autre façon de tester l’absence de connexions entre les éléments. Dans **l’outil Elements,** sélectionnez `<label>Search</label>` l’élément dans l’arborescence DOM.  Sur la page web, notez que le focus apparaît uniquement sur l’étiquette **de** recherche, et non sur la zone de texte d’entrée.  L’implémentation correcte met le focus sur la zone `search` de texte d’entrée et **l’étiquette** de recherche.

1.  Comme exemple de connexion correcte, sélectionnez **l’étiquette Other** dans le formulaire de don.  Une zone d’indicateur de focus s’affiche correctement dans la zone de texte d’entrée à côté de l’étiquette **Autre,** car il existe des valeurs de correspondance et `for` `id` d’attribut.

1.  Dans **l’outil Problèmes,** sélectionnez **Lecture supplémentaire** pour en savoir plus sur le problème.  Pour ouvrir le lien dans un nouvel onglet, **Ctrl**cliquez sur le lien sur Windows/Linux, ou commande cliquez sur le lien + **** **** + **** sur macOS.

    :::image type="complex" source="../media/a11y-testing-more-information-links.msft.png" alt-text="Lien sous l’onglet Problèmes pointant vers des informations plus détaillées sur le problème" lightbox="../media/a11y-testing-more-information-links.msft.png":::
        Lien sous **l’onglet Problèmes** pointant vers des informations plus détaillées sur le problème
    :::image-end:::


## <a name="verify-that-images-have-alt-text"></a>Vérifier que les images ont un texte de alt

Le test d’accessibilité de base nécessite de s’assurer que du texte de remplacement (également appelé _texte_de remplacement) est fourni pour les images.

Pour vérifier automatiquement si un texte de alt est fourni pour les images, utilisez l’outil **Problèmes,** qui contient une section **Accessibilité.**  **L’outil Problèmes** se trouve dans le **caisse** en bas de DevTools.

1.  Ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration des tests d’accessibilité dans un nouvel onglet du navigateur, puis sélectionnez **F12** pour ouvrir DevTools.

1.  Pour ouvrir **l’outil Problèmes,** sélectionnez le compteur **Problèmes** dans le coin supérieur droit de DevTools.

1.  Sous **l’onglet Problèmes,** développez `Images must have alternate text: Element has no title attribute` l’avertissement.  Il existe quatre instances d’images qui n’ont pas de texte de alt.

    :::image type="complex" source="../media/a11y-testing-images-without-alt.msft.png" alt-text="L’outil Problèmes signalant des images qui ne manquent pas de texte de remplacement" lightbox="../media/a11y-testing-images-without-alt.msft.png":::
        L’outil Problèmes signalant des images qui ne manquent pas de texte de remplacement
    :::image-end:::

Pour plus d’informations, [accédez à Images qui doivent avoir un texte de remplacement.](https://dequeuniversity.com/rules/axe/4.1/image-alt)


## <a name="verify-that-text-colors-have-enough-contrast"></a>Vérifier que le contraste des couleurs du texte est suffisant

Pour vérifier automatiquement si les couleurs de texte ont un contraste suffisant, utilisez l’outil **Problèmes,** qui possède une section **Accessibilité.**  **L’outil Problèmes** se trouve dans le **caisse** en bas de DevTools.

1.  Ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration des tests d’accessibilité dans un nouvel onglet du navigateur, puis sélectionnez **F12** pour ouvrir DevTools.

1.  Pour ouvrir **l’outil Problèmes,** sélectionnez le compteur **Problèmes** dans le coin supérieur droit de DevTools.  Vous pouvez recevoir des avertissements signalant que deux éléments de la page web de démonstration ne sont pas assez contrastés.

    :::image type="complex" source="../media/a11y-testing-contrast-issues.msft.png" alt-text="Problèmes de contraste signalés dans l’outil Problèmes" lightbox="../media/a11y-testing-contrast-issues.msft.png":::
        Problèmes de contraste signalés dans l’outil Problèmes
    :::image-end:::

1.  En fonction de vos paramètres, l’onglet Problèmes peut avoir un avertissement, car les **utilisateurs** peuvent avoir des difficultés à lire le contenu du texte en raison d’un **contraste de couleur insuffisant.**   Vous pouvez développer cet avertissement, puis développer les **ressources affectées.**  Une liste d’éléments apparaît avec une liste d’éléments qui n’ont pas assez de contraste.


1.  Sélectionnez `li.high` l’élément.  Dans la page web rendue, le lien **Chiens** de la section **Tronçon** est mis en surbrillence, affichant une petite superposition d’informations.  Il s’agit de la même superposition qui s’affiche lorsque vous pointez sur un élément dans l’arborescence DOM de **l’outil Elements.**

    :::image type="complex" source="../media/a11y-testing-element-with-contrast-issues.msft.png" alt-text="Élément de la page web mis en évidence après la sélection d’un lien dans la section Ressources affectées" lightbox="../media/a11y-testing-element-with-contrast-issues.msft.png":::
        Élément de la page web mis en évidence après la sélection d’un lien dans la section **Ressources** affectées
    :::image-end:::


### <a name="wavy-underlines-in-the-dom-tree-indicate-automatically-detected-issues"></a>Les soulignements ondulés dans l’arborescence DOM indiquent des problèmes détectés automatiquement 

L’arborescence DOM de l’outil **Éléments** indicateur les problèmes directement dans le code HTML avec des soulignements ondulés.  Ces problèmes sont signalés par **l’outil Problèmes.**  Lorsque vous cliquez sur Un élément avec un soulignement **ondulé,** l’outil Problèmes **** s’affiche.

1.  Dans **l’outil Elements,** dans l’arborescence DOM, **Shift+cliquez** sur l’élément, qui a une ligne ondulée sous `<input type="search">` `input` .  **L’outil Problèmes s’affiche** et indique le problème pour cet élément.

    :::image type="complex" source="../media/a11y-testing-wavy-underlines.msft.png" alt-text="Un élément avec un soulignement ondulé dans l’affichage DOM présente un problème" lightbox="../media/a11y-testing-wavy-underlines.msft.png":::
        Un élément avec un soulignement ondulé dans l’affichage DOM présente un problème
    :::image-end:::


## <a name="see-also"></a>Articles associés

*  [Rechercher et résoudre les problèmes liés à Microsoft Edge’outil Problèmes de DevTools][DevToolsIssuesTool]
*  [Vue d’ensemble des tests d’accessibilité à l’aide de DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsIssuesTool]: ../issues/index.md "Recherchez et corrigez les problèmes liés à l’outil des problèmes de Microsoft Edge DevTools | Documents Microsoft"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page web de démonstration de test d’accessibilité | GitHub"
