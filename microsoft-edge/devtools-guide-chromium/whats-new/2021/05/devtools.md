---
description: Bouton Plus d’outils, documentation en contexte pour commencer à utiliser l’extension DevTools, prise en charge accrue des lecteurs d’écran dans la console, etc.
title: Nouveautés de DevTools (Microsoft Edge 92)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 09e1438ae7fd6547a7dd14757f54f370c9008773
ms.sourcegitcommit: 1dd6376784c394087fe2938acaa069212cf7656e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/16/2021
ms.locfileid: "11659427"
---
# <a name="whats-new-in-devtools-microsoft-edge-92"></a>Nouveautés de DevTools (Microsoft Edge 92)

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]

> [!TIP]
> La **conférence Microsoft Build 2021** s’est tenue du 25 au 27 mai.  Voici une vidéo de Build sur les mises à jour de DevTools : [Microsoft Edge | État de la plateforme][YoutubeEdgeStateOfThePlatform] : Microsoft Edge une plateforme attrayante et cohérente avec des outils pour les développeurs.  À mesure que nos navigateurs hérités ne seront plus pris en charge, Edge sera bientôt le seul navigateur pris en charge par Microsoft sur Windows 10.  Rejoignez-nous pour en savoir plus sur la dernière version de la plateforme Edge, des outils et des applications web.


## <a name="the-close-button-is-no-longer-hidden-when-devtools-is-narrow"></a>Le bouton Fermer n’est plus masqué lorsque DevTools est étroit

<!-- Title: DevTools is now easier to close -->
<!-- Subtitle: The Close button in DevTools is always displayed, even when DevTools is docked to the right and the DevTools viewport is narrow. -->

Dans Microsoft Edge version 91 ou antérieure, **** le bouton Fermer pour fermer DevTools n’est pas affiché lorsque la vue DevTools est étroite.  Dans Microsoft Edge version 92, **** le bouton Fermer dans DevTools est toujours présent, quelle que soit la largeur de laport d’affichage DevTools.

:::image type="complex" source="../../media/2021/05/close-devtools-button-always-displayed.msft.png" alt-text="Le bouton Fermer DevTools est désormais présent, même lorsque laport d’affichage est étroite" lightbox="../../media/2021/05/close-devtools-button-always-displayed.msft.png":::
   Le **bouton Fermer** DevTools est désormais présent, même lorsque laport d’affichage est étroite
:::image-end:::


## <a name="add-tools-quickly-with-the-new-more-tools-button"></a>Ajouter rapidement des outils avec le nouveau bouton Plus d’outils

<!-- Title: Add tools quickly with the new More Tools button -->
<!-- Subtitle: Learn about a new convenient way to open tools in Microsoft Edge DevTools. -->

Il existe une nouvelle façon d’ouvrir d’autres outils dans **** Microsoft Edge DevTools : le menu Plus d’outils `+` (). Le menu **Plus d’outils** apparaît dans la barre d’outils du panneau principal et dans la barre d’outils du panneau. La sélection d’un outil dans le menu **Plus d’outils** l’ajoute à la barre d’outils.

Pour réorder les onglets de l’une ou l’autre barre d’outils, sélectionnez les onglets et faites-les glisser.

Le menu **Plus d’outils** était disponible sous la forme d’une expérience Microsoft Edge version 89 et est désormais toujours présent.

:::image type="complex" source="../../media/2021/05/more-tools-button.msft.png" alt-text="Bouton Plus d’outils dans la barre d’outils supérieure et la barre d’outils de caisse" lightbox="../../media/2021/05/more-tools-button.msft.png":::
   Bouton **Plus d’outils** dans la barre d’outils supérieure et la barre d’outils de caisse
:::image-end:::

:::image type="complex" source="../../media/2021/05/more-tools-menu.msft.png" alt-text="Menu Plus d’outils" lightbox="../../media/2021/05/more-tools-menu.msft.png":::
   Menu **Plus d’outils**
:::image-end:::


## <a name="improvements-for-hovering-selecting-and-closing-tools"></a>Améliorations apportées aux outils de pointage, de sélection et de fermeture

<!-- Title: Improvements to tab interactions -->
<!-- Subtitle: Interactions related to hovering, selecting, and closing tools are more predictable. -->

Les onglets de chaque outil ont été reformatés pour réduire les risques de fermeture accidentelle d’un outil.  Dans chaque onglet de la barre d’outils principale et dans la barre d’outils du caisse, nous avons ajouté :
*  Espacement autour de l’onglet.
*  Espacement autour du bouton fermer `x` () dans l’onglet.
*  Couleur d’arrière-plan lorsque vous placez le pointage sur l’onglet.
*  Une boîte à outils pour le bouton fermer ( `x` ) de l’onglet.
*  Contraste plus élevé pour le bouton fermer ( `x` ) de l’onglet.

Par exemple, lorsque vous êtes dans l’outil **Performances** et que vous pointez sur l’onglet de l’outil Réseau, ces améliorations permettent d’éviter la fermeture accidentelle de l’outil Réseau. **** ****

:::row:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/hovering-on-tool-tab-before.msft.png" alt-text="Onglets avant la reformatage" lightbox="../../media/2021/05/hovering-on-tool-tab-before.msft.png":::
           Onglets avant la reformatage :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/hovering-on-tool-tab-after.msft.png" alt-text="Onglets après la reformatage" lightbox="../../media/2021/05/hovering-on-tool-tab-after.msft.png":::
           Onglets après la reformatage :::image-end:::
    :::column-end:::
:::row-end:::

Ces améliorations sont particulièrement pertinentes pour les utilisateurs de DevTools localisées, dans lesquelles les onglets peuvent être plus étroits et plus faciles à fermer accidentellement.

:::image type="complex" source="../../media/2021/05/hovering-reduced-chance-of-closing-tab.msft.png" alt-text="DevTools localisées avec onglets étroits" lightbox="../../media/2021/05/hovering-reduced-chance-of-closing-tab.msft.png":::
   DevTools localisées avec onglets étroits
:::image-end:::

Nous avons également facilité la ré-ajout d’un outil que vous avez fermé en ajoutant un [menu](#add-tools-quickly-with-the-new-more-tools-button) Plus d’outils à la barre d’outils principale et à la barre d’outils des caisses.


## <a name="better-support-for-screen-readers-in-the-console"></a>Meilleure prise en charge des lecteurs d’écran dans la console

<!-- Title: Better screen reader support in the Console -->
<!-- Subtitle: Assistive technologies can now announce autocomplete suggestions and evaluated expressions in the Console. -->

Avant Microsoft Edge version 92, dans la **console,** les technologies d’assistance telles que les lecteurs d’écran n’annoncaient pas les suggestions de mise à jour automatique ou les résultats des expressions évaluées. This has been fixed now.

:::row:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/screen-reader-support-in-console-autocomplete.msft.png" alt-text="Dans la console, les lecteurs d’écran annoncent maintenant la suggestion de mise à l’écran sélectionnée" lightbox="../../media/2021/05/screen-reader-support-in-console-autocomplete.msft.png":::
           Dans la **console,** les lecteurs d’écran annoncent désormais la suggestion de mise à l’écran sélectionnée :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/screen-reader-support-in-console-evaluated-expression.msft.png" alt-text="Dans la console, les lecteurs d’écran annoncent désormais le résultat d’une expression évaluée" lightbox="../../media/2021/05/screen-reader-support-in-console-evaluated-expression.msft.png":::
           Dans la **console,** les lecteurs d’écran annoncent désormais le résultat d’une expression évaluée :::image-end:::
    :::column-end:::
:::row-end:::


## <a name="source-order-viewer"></a>Visionneuse de commandes source

<!--  Title: Source Order Viewer -->
<!--  Subtitle: The new Source Order Viewer displays numbers on the webpage indicating the order of page elements in the source file, independently of how the page sections are positioned by CSS. -->

Vous pouvez désormais afficher l’ordre des éléments source superposés sur la page web rendue, pour une meilleure inspection de l’accessibilité.

L’ordre du contenu dans un document HTML est important pour l’optimisation et l’accessibilité du moteur de recherche.  CSS permet aux développeurs de créer du contenu dont l’ordre à l’écran est différent de celui du document source HTML.  Il s’agit d’un problème d’accessibilité, car les utilisateurs de lecteur d’écran peuvent obtenir une expérience confuse.

:::image type="complex" source="../../media/2021/05/source-order-viewer.msft.png" alt-text="L’activation de l’Afficheur des commandes sources affiche l’ordre des éléments dans la source sous la la mesure où ils sont superposés sur la page" lightbox="../../media/2021/05/source-order-viewer.msft.png":::
   L’activation de **l’Afficheur** des commandes sources affiche l’ordre des éléments dans la source sous la mesure de superpositions sur la page
:::image-end:::

Pour plus d’informations, accédez à Tester la [prise en charge du clavier à l’aide de l’Observateur de commandes source.](../../../accessibility/test-tab-key-source-order-viewer.md)

Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez à [Problème 1094406][CR1094406].


## <a name="user-agent-client-hints-for-devices-in-the-network-conditions-tab"></a>User-Agent client pour les appareils dans l’onglet Conditions réseau

<!--  Title: User-Agent Client Hints -->
<!--  Subtitle: Access information about a user's browser in an ergonomic way that preserves privacy. -->

User-Agent conseils client sont désormais appliqués pour les appareils dans le champ **Agent** utilisateur de l’outil **Conditions réseau.**  User-Agent conseils au client est une nouvelle extension de l’API Client Hints qui vous permet d’accéder aux informations sur le navigateur d’un utilisateur de manière conviviale, tout en préservez la confidentialité.

:::image type="complex" source="../../media/2021/05/user-agent.msft.png" alt-text="Agent utilisateur" lightbox="../../media/2021/05/user-agent.msft.png":::
   Agent utilisateur
:::image-end:::

Pour plus d’informations, accédez [à User-Agent Client Hints](../../../../web-platform/user-agent-guidance.md#user-agent-client-hints).

Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez à [Problème 1174299][CR1174299].


## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-118"></a>Microsoft Edge Outils de développement Visual Studio Code version 1.1.8

Les [outils Microsoft Edge][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] développeur pour Visual Studio Code version 1.1.8 pour Microsoft Visual Studio Code ont les modifications suivantes depuis la version précédente.  Microsoft Visual Studio Code met automatiquement à jour les extensions.  Pour mettre à jour manuellement la version 1.1.8, accédez à Mettre à jour [une extension manuellement.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]

Vous pouvez déposer des problèmes et contribuer à l’extension sur le GitHub [vscode-edge-devtools.][GithubMicrosoftVscodeEdgeDevtools]

### <a name="in-context-documentation-and-ui-to-make-it-easier-to-use-the-devtools-extension"></a>Documentation et interface utilisateur en contexte pour faciliter l’utilisation de l’extension DevTools

<!-- Title: In-context documentation and UI make it easier to get started using the Developer Tools extension -->
<!-- Subtitle: The Microsoft Edge Developer Tools for Visual Studio Code extension now presents helpful text, buttons, and links, and opens a documentation page with guidance on how to get started. -->

La version 1.1.8 de l’extension [outils][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] de développement Microsoft Edge pour Visual Studio Code offre désormais un moyen plus simple de démarrer une nouvelle instance de Microsoft Edge, en présentant des instructions, des boutons, des liens et une page de documentation pour vous guider.

*  Lorsque vous sélectionnez le bouton **Outils Microsoft Edge** dans la barre d’activité de Visual Studio Code, le panneau **** **Outils Microsoft Edge** : Cibles présente désormais un texte explicatif, des boutons et des liens pour vous guider, au lieu d’un panneau vide.

*  Lorsque vous ouvrez une nouvelle instance de Microsoft Edge à partir de Visual Studio Code, Microsoft Edge affiche désormais une page de démarrage qui explique comment utiliser l’extension Outils de développement, au lieu d’une page vierge.

*  Le **panneau Microsoft Edge Outils** : Cibles possède désormais une launch.jsgénérer une **launch.js** sur le bouton et des instructions, pour vous aider à lancer votre projet pour le débogage dans Microsoft Edge.

Pour plus d’informations, accédez à [Utiliser les outils.][GithubIoDevToolsUsing]


## <a name="announcements-from-the-chromium-project"></a>Annonces du projet de Chromium

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]


### <a name="css-grid-editor"></a>Éditeur CSS Grid

Vous pouvez désormais prévisualiser et éditer des dispositions de grille CSS à l’aide du nouvel éditeur CSS Grid.

Lorsqu’un élément HTML de votre page s’y est appliqué, une icône de grille s’affiche en de côté dans l’onglet Styles. Cliquez sur l’icône de grille pour afficher ou masquer l’éditeur de grille `display: grid` `display: inline-grid` CSS. **** Dans l’éditeur de grille CSS, sélectionnez l’une des icônes (par exemple) pour afficher un aperçu de la mise en page dans `justify-content: space-around` la page rendue.  La disposition flexible fonctionne de la même manière.

:::image type="complex" source="../../media/2021/05/css-grid-editor.msft.png" alt-text="Éditeur CSS Grid" lightbox="../../media/2021/05/css-grid-editor.msft.png":::
   Éditeur CSS Grid
:::image-end:::

<!-- screenshot uses https://jec.fyi -->

Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez à [Problème 1203241][CR1203241].


### <a name="support-for-const-redeclarations-in-the-console"></a>Prise en charge des déclarations de const dans la console

La console prend désormais en charge la déclaration des variables dans des scripts REPL distincts (par exemple, lorsque vous exécutez une instruction dans la console), en plus des `const` `let` déclarations existantes et `class` redéclarations.  Cette prise en charge vous permet d’expérimenter différentes déclarations pour `const` les variables sans actualisation de la page.  Auparavant, DevTools a lancé une erreur de syntaxe si vous avez redéclaré une `const` liaison.

Reportez-vous à l’exemple ci-dessous. `const` la redéclaration est prise en charge dans des scripts REPL distincts (reportez-vous à la `a` variable).  Notez que les scénarios suivants ne sont pas pris en charge, par conception :

*  `const` la redéclaration des scripts de page n’est pas autorisée dans les scripts REPL.
*  `const` la redéclaration dans le même script REPL n’est pas autorisée (faire référence à la variable `b` ).

:::image type="complex" source="../../media/2021/05/support-for-const-redeclaration.msft.png" alt-text="La déclaration d’une variable const est autorisée dans la console" lightbox="../../media/2021/05/support-for-const-redeclaration.msft.png":::
   La déclaration d’une variable const est autorisée dans la console
:::image-end:::

Pour découvrir comment exécuter un script REPL unique ou un script REPL multi-ligne, accédez à la console en tant [qu’environnement JavaScript.](../../../console/console-javascript.md)
    
Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez à [Problème 1076427][CR1076427].


### <a name="new-shortcut-to-view-iframe-details"></a>Nouveau raccourci pour afficher les détails de l’iframe

Pour afficher rapidement les détails, vous pouvez maintenant cliquer avec le bouton droit sur un élément dans l’outil Éléments, puis sélectionner Afficher les `iframe` `iframe` **détails de l’iframe.** ****

:::image type="complex" source="../../media/2021/05/show-iframe-details.msft.png" alt-text="Affichage des détails de l’iframe" lightbox="../../media/2021/05/show-iframe-details.msft.png":::
   Affichage des détails de l’iframe
:::image-end:::

Cela permet d’afficher les détails sur `iframe` l’outil **Application.**  Dans **l’outil Application,** vous pouvez examiner les détails du document, l’état de sécurité et d’isolation, la stratégie d’autorisations, etc., pour déboguer les problèmes potentiels.

:::image type="complex" source="../../media/2021/05/show-iframe-details-application-tool.msft.png" alt-text="Détails du cadre dans l’outil Application" lightbox="../../media/2021/05/show-iframe-details-application-tool.msft.png":::
   Détails du cadre dans **l’outil Application**
:::image-end:::

<!-- demo page: https://wolfib.github.io/web-demos/ esp https://wolfib.github.io/web-demos/jsIframe.html -->

Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez à [Problème 1192084][CR1192084].


### <a name="enhanced-cors-debugging-support"></a>Prise en charge améliorée du débogage CORS

Les erreurs de partage de ressources d’origine croisée (CORS) sont désormais **émises** dans l’onglet Problèmes.  Il existe différentes causes potentielles d’erreurs CORS.  Cliquez pour développer chaque problème afin de comprendre les causes et solutions potentielles.

:::image type="complex" source="../../media/2021/05/cors-debugging-support.msft.png" alt-text="Problèmes CORS dans l’onglet Problèmes" lightbox="../../media/2021/05/cors-debugging-support.msft.png":::
   Problèmes CORS dans l’onglet Problèmes
:::image-end:::

<!-- screenshot uses http://cors-errors.glitch.me -->

Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez à [Problème 1141824][CR1141824].


### <a name="renamed-xhr-filter-to-fetchxhr"></a>Filtre XHR renommé Fetch\/XHR

Dans **l’outil** Réseau, le **filtre XHR** est maintenant renommé **Fetch/XHR**. Cette modification rend plus clair que ce filtre inclut les demandes réseau `XMLHttpRequest` `Fetch` d’API et à la fois.

:::image type="complex" source="../../media/2021/05/fetch-xhr.msft.png" alt-text="L’outil Réseau affiche désormais Fetch/XHR au lieu de XHR" lightbox="../../media/2021/05/fetch-xhr.msft.png":::
   **L’outil** Réseau affiche désormais **Fetch/XHR** au lieu de **XHR**
:::image-end:::

Pour plus d’informations, accédez à :
*  [Spécifications XMLHttpRequest][XhrSpecWhatwgOrg]
*  [Fetch spec][FetchSpecWhatwgOrg]

Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez à [Problème 1201398][CR1201398].


### <a name="filter-wasm-resource-type-in-the-network-tool"></a>Type de ressource Filter Wasm dans l’outil Réseau

Dans **l’outil** Réseau, vous pouvez maintenant sélectionner le nouveau filtre **Wasm** pour filtrer les demandes réseau WebAssembly.

:::image type="complex" source="../../media/2021/05/wasm-network-requests.msft.png" alt-text="Filtrer par Wasm" lightbox="../../media/2021/05/wasm-network-requests.msft.png":::
   Filtrer par Wasm
:::image-end:::

<!-- screenshot uses http://memory-inspector.glitch.me/demo-wasm.html -->

Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez à [Problème 1103638][CR1103638].


### <a name="compute-intersections-are-now-included-in-the-performance-tool"></a>Les intersections de calcul sont désormais incluses dans l’outil Performance

Dans **l’outil Performance,** DevTools affiche désormais **les intersections** de calcul dans le graphique graphique. Ces modifications vous aident à identifier les événements d’observateurs d’intersections et à déboguer la charge de performances potentielle des observateurs d’intersections.

:::image type="complex" source="../../media/2021/05/compute-intersections-in-perf-tool.msft.png" alt-text="Calcul des intersections dans l’outil Performance" lightbox="../../media/2021/05/compute-intersections-in-perf-tool.msft.png":::
   Calcul des intersections dans **l’outil Performance**
:::image-end:::

<!-- screenshot uses https://googlechrome.github.io/samples/intersectionobserver -->

Pour plus d’informations sur les observateurs d’intersection, [accédez à Confiance, l’observation est préférable : Intersection Observer v2][WebDevIntersectionObserverV2].  Pour plus d’informations sur l’utilisation du graphique graphique, accédez [à Analyser un enregistrement des performances.][DevtoolsEvaluatePerfRefAnalyzeAPerfRecording]  Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez à [Problème 1199137][CR1199137].


## <a name="download-the-microsoft-edge-preview-channels"></a>Télécharger les canaux d’aperçu Microsoft Edge

Si vous êtes sous Windows, Linux ou macOS, envisagez d'utiliser les [canaux d'aperçu de Microsoft][MicrosoftEdgePreviewChannels] Edge comme navigateur de développement par défaut.  Les canaux de prévisualisation vous donnent accès aux dernières fonctionnalités de DevTools.


## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Contacter l’équipe Microsoft Edge DevTools

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]


<!-- links -->
[DevtoolsEvaluatePerfRefAnalyzeAPerfRecording]: ../../../evaluate-performance/reference.md#analyze-a-performance-recording "Analyser un enregistrement des performances | Documents Microsoft"
<!-- external links -->
[XhrSpecWhatwgOrg]: https://xhr.spec.whatwg.org "Spécifications XMLHttpRequest | WHATWG"
[FetchSpecWhatwgOrg]: https://fetch.spec.whatwg.org "Récupérer les spécifications | WHATWG"

[WebDevIntersectionObserverV2]: https://web.dev/intersectionobserver-v2 "La confiance est bonne, l’observation est préférable : Intersection Observer v2 | web.dev"

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"
[GithubIoDevToolsUsing]: https://microsoft.github.io/vscode-edge-devtools/using.html "Utilisation des outils | GitHub"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux de préversion de Microsoft Edge"

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Mettre à jour une extension manuellement - Extension Marketplace | Visual Studio Code"

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Outils de développement Visual Studio Code | Visual Studio Marketplace"

[YoutubeEdgeStateOfThePlatform]: https://www.youtube.com/watch?v=sU0WRZ0kkNo "Microsoft Edge : état de la plateforme | YouTube"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bogues Chromium"
[CR1094406]: https://crbug.com/1094406 "Problème 1094406 : les développeurs souhaitent qu’une visionneuse de commandes sources soit | Chromium bogues"
[CR1174299]: https://crbug.com/1174299 "Problème 1174299 : les conseils client UA ont été supprimés lors du remplacement de la chaîne UA via l’onglet Conditions réseau de Chrome DevTools | Chromium bogues"
[CR1203241]: https://crbug.com/1203241 "Problème 1203241 : éditeur CSS Grid | Chromium bogues"
[CR1076427]: https://crbug.com/1076427 "Problème 1076427 : la console DevTools doit prendre en charge la | Chromium bogues"
[CR1192084]: https://crbug.com/1192084 "Problème 1192084 : ajouter l’option de clic droit « Afficher les détails du cadre » à des balises html/iframe dans les éléments d’affichage | Chromium bogues"
[CR1141824]: https://crbug.com/1141824 "Problème 1141824 : améliorer le signalement des erreurs CORS dans DevTools | Bogues Chromium"
[CR1201398]: https://crbug.com/1201398 "Problème 1201398 : Demande de fonctionnalité : renommer le filtre de type XHR dans le panneau | Chromium bogues"
[CR1103638]: https://crbug.com/1103638 "Problème 1103638 : panneau réseau pour l’affichage des ressources WebAssembly | Chromium bogues"
[CR1199137]: https://crbug.com/1199137 "Problème 1199137 : afficher le coût intersectionObserveur dans le panneau de | Chromium bogues"

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].
> La page d’origine est disponible [ici](https://developer.chrome.com/blog/new-in-devtools-xx) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)

[ ![ Creative Commons License][CCby4Image]][CCA4IL] This work is licensed under a Creative Commons Attribution [4.0 International License][CCA4IL].

[CCA4IL]: https://creativecommons.org/licenses/by/4.0
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen
