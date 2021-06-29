---
description: Utilisez l’outil Problèmes pour identifier et résoudre les problèmes liés à la page web actuelle.
title: Rechercher et résoudre les problèmes à l’aide de l’outil Problèmes
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/24/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 86277c509aa4b67635661ba3a316fb5b1e3b9d14
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624695"
---
<!-- Copyright Sam Dutton

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="find-and-fix-problems-using-the-issues-tool"></a>Rechercher et résoudre les problèmes à l’aide de l’outil Problèmes

Dans Microsoft Edge DevTools, l’outil **Problèmes** analyse automatiquement la page web actuelle, signale les problèmes regroupés par type et fournit une documentation pour expliquer et résoudre les problèmes.

**L’outil Problèmes** fournit des commentaires dans les catégories suivantes :
*  Accessibilité.
*  Compatibilité entre les navigateurs.
*  Performances.
*  Applications web progressives.
*  Sécurité.
*  Autre.

Les commentaires **** dans l’outil Problèmes sont fournis par plusieurs sources, notamment la plateforme Chromium, la axe de laque, les données de compatibilité du navigateur MDN et lahint web.  Pour plus d’informations sur ces sources de commentaires qui remplit l’outil **Problèmes,** accédez à :
*  [Vue d’ensemble des outils axe][DequeAxe]
*  [browser-compat-data repo][MDNCompat]
*  [webhint][webhintIo]


## <a name="open-the-issues-tool"></a>Ouvrir l’outil Problèmes

Effectuez les étapes suivantes pour ouvrir **l’outil Problèmes** à l’aide d’une page de démonstration.


1.  Accédez à une page web qui contient des problèmes à résoudre.  Par exemple, ouvrez la [page de][A11ytestingPagewitherrors] démonstration des tests d’accessibilité dans un nouvel onglet ou une nouvelle fenêtre.

1.  Ouvrez DevTools.  Après quelques **secondes,** le compteur Problèmes \( Compteur de problèmes \) apparaît dans le coin supérieur droit ![ ](../media/issues-counter-icon.msft.png) de DevTools.  Le nombre de problèmes dans votre compteur Problèmes peut être différent.

1.  Sélectionnez **le compteur Problèmes.**  **L’outil Problèmes** s’ouvre avec des problèmes regroupés en différentes catégories.

    :::image type="complex" source="../media/issues-tool-categories.msft.png" alt-text="Catégories de problèmes dans l’outil Problèmes de la page de démonstration" lightbox="../media/issues-tool-categories.msft.png":::
       Catégories de problèmes dans l’outil Problèmes de la page de démonstration
    :::image-end:::

### <a name="other-ways-to-open-the-issues-tool"></a>Autres façons d’ouvrir l’outil Problèmes

Il existe plusieurs façons supplémentaires d’ouvrir **l’outil Problèmes** :
*  Sélectionnez le menu **Plus d’outils** ( ) dans le panneau principal ou le panneau, puis **+** sélectionnez **Problèmes.** ****
*  Sélectionnez **Personnaliser et contrôler les problèmes des outils DevTools**  >  **More.**  >  ****
*  Dans l’arborescence DOM de l’outil **Elements,** sélectionnez, puis cliquez sur un nom d’élément souligné de forme `Shift` ondulée.  Vous pouvez également ouvrir le menu contextif sur un élément souligné de forme ondulée, puis sélectionner **Afficher les problèmes.**

### <a name="issues-are-automatically-ordered-by-severity"></a>Les problèmes sont automatiquement ordonnés par gravité

Dans chaque catégorie de problèmes, les erreurs sont d’abord répertoriées, puis les avertissements, puis les conseils.

:::image type="complex" source="../media/issues-ordered-by-severity.msft.png" alt-text="L’outil Problèmes affiche les problèmes de performances triés par gravité" lightbox="../media/issues-ordered-by-severity.msft.png":::
   **L’outil Problèmes** affiche les problèmes de performances triés par gravité
:::image-end:::

### <a name="include-third-party-issues"></a>Inclure des problèmes de tiers

Pour inclure les problèmes causés par des sites tiers, en haut **** de l’outil Problèmes, cochez la case Inclure les problèmes tiers. ****


## <a name="expand-entries-in-the-issues-tool"></a>Développer les entrées dans l’outil Problèmes

**L’outil Problèmes** présente une documentation supplémentaire et des correctifs recommandés à appliquer à chaque problème.  Pour développer un problème afin d’obtenir ces informations supplémentaires, sélectionnez un problème, comme suit.

1.  Ouvrez la [page de démonstration][A11ytestingPagewitherrors] dans une nouvelle fenêtre ou nouvel onglet, puis ouvrez DevTools.

1.  Ouvrez **l’outil Problèmes** en sélectionnant le compteur **Problèmes** \( Compteur de ![ problèmes ](../media/issues-counter-icon.msft.png) \).

1.  Sélectionnez un problème pour développer le problème.

    :::image type="complex" source="../media/issues-tool-initial-view-accessibility-page.msft.png" alt-text="Outil Problèmes affichant des informations supplémentaires sur la façon de résoudre le problème" lightbox="../media/issues-tool-initial-view-accessibility-page.msft.png":::
       Outil **Problèmes affichant** des informations supplémentaires sur la façon de résoudre le problème
    :::image-end:::

Chaque problème affiché présente les composants suivants :
*   Titre décrivant le problème.
*   Description fournissant davantage de contexte et des solutions proposées.
*   Section **RESSOURCES AFFECTÉEs** qui fait lien vers des ressources dans DevTools, telles que l’outil **Éléments,** **Sources** **ou** Réseau.
*   Liens vers une documentation plus complète.


## <a name="view-issues-in-context-of-an-associated-tool"></a>Afficher les problèmes dans le contexte d’un outil associé

Un problème dans l’outil Problèmes peut inclure un ou plusieurs liens qui ouvrent différents **outils,** tels que l’outil **Éléments,** **Sources** **ou** Réseau. Vous pouvez ouvrir l’un de ces outils pour effectuer des étapes de dépannage supplémentaires. Pour ouvrir un outil lié à partir de **l’outil Problèmes,** effectuez les étapes suivantes.

1.  Comme décrit dans la section précédente, ouvrez la page de démonstration, puis développez un problème dans **l’outil** Problèmes.

1.  Dans **RESSOURCES AFFECTÉEs,**  >  **ouvrez**dans , sélectionnez le nom de l’outil.  La ressource affectée s’affiche dans l’outil sélectionné.

    :::image type="complex" source="../media/issues-tool-affected-resource-opens-elements-tool.msft.png" alt-text="Sélectionner un outil pour ouvrir une ressource concernée à partir de l’outil Problèmes" lightbox="../media/issues-tool-affected-resource-opens-elements-tool.msft.png":::
       Sélectionner un outil pour ouvrir une ressource concernée à partir de l’outil Problèmes
    :::image-end:::

    Un problème développé peut avoir une **liaison** réseau pour afficher la ressource concernée dans **l’outil** Réseau.

    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="L’outil Réseau s’ouvre lorsque vous sélectionnez un lien de ressources réseau" lightbox="../media/issues-tab-view-issue.msft.png":::
    **L’outil** Réseau s’ouvre lorsque vous sélectionnez un **lien de** ressources réseau
    :::image-end:::


## <a name="open-issues-from-the-dom-tree"></a>Problèmes d’ouverture à partir de l’arborescence DOM

Si un élément est associé à un problème, l’arborescence DOM de l’outil **Elements** affiche un soulignement ondulé sous le nom de l’élément.  Vous pouvez ouvrir le menu contextif (clic droit) sur l’élément, puis sélectionner Afficher les **problèmes,** ou sélectionner et cliquer avec le bouton gauche sur l’élément avec le `Shift` soulignement ondulé.

Pour afficher un problème pour les éléments avec des soulignements ondulés dans l’arborescence DOM, effectuez les étapes suivantes.

1.  Ouvrez une page, telle que la [page de démonstration,][A11ytestingPagewitherrors]dans un nouvel onglet ou une nouvelle fenêtre.

1.  Ouvrez DevTools, puis sélectionnez **l’onglet Éléments.**

1.  Dans l’arborescence DOM, développez `<body>`  >  `<header>`  >  `<form>` .  Notez que `<input>` l’élément présente un soulignement ondulé.

    :::image type="complex" source="../media/issues-wavy-underlines-dom-tree.msft.png" alt-text="Problèmes soulignés ondulés dans l’arborescence DOM de l’outil Elements" lightbox="../media/issues-wavy-underlines-dom-tree.msft.png":::
       Problèmes soulignés ondulés dans l’arborescence **DOM de** **l’outil Elements**
    :::image-end:::

1.  Pointez sur `<input>` l’élément.  Une info-bulle affiche des informations sur le problème.

1.  Ouvrez le menu contextif sur l’élément avec le soulignement ondulé, puis sélectionnez **Afficher les problèmes.**  **L’outil** Problèmes s’ouvre et affiche le problème associé à cet élément.

    :::image type="complex" source="../media/issues-opened-from-dom-tree-wavy-underline.msft.png" alt-text="Détails sur les problèmes sur un élément ondulé souligné dans l’arborescence DOM" lightbox="../media/issues-opened-from-dom-tree-wavy-underline.msft.png":::
       Détails sur les problèmes sur un élément ondulé souligné dans **l’arborescence DOM**
    :::image-end:::


## <a name="see-also"></a>Voir également

* [Tester automatiquement les problèmes d’accessibilité d’une page web](../accessibility/test-issues-tool.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]

<!-- links -->
[DevtoolsOpenIndex]: ../open/index.md "Ouvrez Microsoft Edge devTools | Documents Microsoft"
<!-- external links -->
[A11ytestingPagewitherrors]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page de démonstration des tests d’accessibilité | Documents Microsoft"
[DequeAxe]: https://www.deque.com/axe "Vue d’ensemble des outils axe | Deque"
[MDNCompat]: https://github.com/mdn/browser-compat-data "Gestion des données de compatibilité des navigateurs MDN | GitHub"
[webhintIo]: https://webhint.io "webhint.io"

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].
> La page d’origine est [trouvée ici](https://developers.google.com/web/tools/chrome-devtools/issues/index) et est cochée par [Sam Dutton][SamDutton] \(Developer Advocate\).
[ ![ Creative Commons License][CCby4Image]][CCA4IL] This work is licensed under a Creative Commons Attribution [4.0 International License][CCA4IL].

[CCA4IL]: https://creativecommons.org/licenses/by/4.0
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques
[SamDutton]: https://developers.google.com/web/resources/contributors#sam-dutton
