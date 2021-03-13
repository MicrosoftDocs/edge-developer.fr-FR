---
description: Match keyboard shortcuts to Visual Studio Code, emulate Surface Duo and Samsung Postal Fold, CSS grid overlay improvements, and more.
title: Nouveautés de DevTools (Microsoft Edge 86)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: a981c8b1a2658ba8cf771096e63001f7d6f69616
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408345"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-86"></a>Nouveautés de DevTools (Microsoft Edge 86)  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Annonces de l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

### <a name="match-keyboard-shortcuts-in-devtools-to-visual-studio-code"></a>Faire correspondre les raccourcis clavier dans DevTools à Visual Studio Code  

Dans Microsoft Edge 86, vous pouvez faire correspondre les raccourcis clavier des DevTools à vos raccourcis dans [Microsoft Visual Studio Code][VisualStudioCode].  

:::image type="complex" source="../../media/2020/08/keyboard-shortcut.msft.png" alt-text="Faire correspondre les raccourcis clavier dans DevTools à Visual Studio Code" lightbox="../../media/2020/08/keyboard-shortcut.msft.png":::
   Faire correspondre les raccourcis clavier dans DevTools à Visual Studio Code  
:::image-end:::  

Pour activer cette fonctionnalité, accédez à Personnaliser les raccourcis clavier dans [Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].  

Par exemple, le raccourci clavier pour mettre en pause ou poursuivre l’exécution d’un script [dans Visual Studio Code][VisualStudioCodeShortcutsKeyboardWindows] est `F5` .  Avec **devTools (par défaut)** prédéfiny, ce même raccourci dans DevTools est , mais lorsque vous choisissez l’Visual Studio `F8` **Code** prédéfiny, ce raccourci est désormais également `F5` .  

Problème de chrome [#174309][CR174309]  

### <a name="emulate-surface-duo-and-samsung-galaxy-fold"></a>Émuler Surface Duo et Samsung Samsung Fold  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalité expérimentale":::
   Fonctionnalité expérimentale  
:::image-end:::  

Vous pouvez maintenant tester l’apparence de votre site web ou de votre application sur deux nouveaux appareils :  [Surface Duo][MicrosoftSurfaceDevicesDuo] et Samsung [Contrôle Fold][SamsungMobileGalaxyFold] dans Microsoft Edge.  

Pour améliorer votre site web ou votre application pour les appareils à double écran et pliables, utilisez les fonctionnalités suivantes lors de [l’émulation de l’appareil.][DevtoolsDeviceModeIndex]  

*   [Couvrant,][DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]c’est-à-dit lorsque votre site web \(ou application\) apparaît sur les deux écrans.
*   [Rendu de la séam,][DualScreenIntroductionHowWorkSeam]qui est l’espace entre les deux écrans.
*   [Permettre aux][DevtoolsExperimentalFeaturesEnableExperimentalApis] API de plateforme Web expérimentales d’accéder à la nouvelle fonctionnalité multimédia [CSS][DualScreenWebCssMediaSpanning] couvrant l’écran et à l’API [JavaScript getWindowSegments][DualScreenWebJavascriptGetwindowsegments].  

:::image type="complex" source="../../media/2020/08/surface-duo-device-emulation.msft.png" alt-text="Émulation d’appareil pour Surface Duo" lightbox="../../media/2020/08/surface-duo-device-emulation.msft.png":::
   Émulation d’appareil pour Surface Duo  
:::image-end:::  

Pour activer cette fonctionnalité expérimentale, accédez à Activer les fonctionnalités expérimentales et cochez la case en regard d’Émulation : prendre en charge le **mode double écran.** [][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]  

Pour plus d’informations sur cette expérience, accédez à [Émulation : prendre en charge le mode double écran.][DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]  

Problème de chrome : [#1054281][CR1054281]  

### <a name="css-grid-overlay-improvements-and-new-experimental-grid-features"></a>Améliorations de la superposition de grille CSS et nouvelles fonctionnalités de grille expérimentale  

Merci pour les commentaires positifs sur les superpositions de grille CSS améliorées.  Les superpositions de grille CSS sont désormais activées par défaut et ne vous obligent pas à activer une expérience.  

:::image type="complex" source="../../media/2020/08/css-grid-overlay-article.msft.png" alt-text="Superposition de grille CSS pour l’élément article" lightbox="../../media/2020/08/css-grid-overlay-article.msft.png":::
   Superposition de grille CSS pour `article` l’élément  
:::image-end:::  

> [!NOTE]
> Pour plus d’informations sur les superpositions de grille, accédez aux fonctionnalités de débogage de grille [CSS.][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]  

L’équipe Microsoft Edge DevTools et l’équipe Chrome DevTools collaborent sur des fonctionnalités supplémentaires.  Les nouvelles fonctionnalités incluent plusieurs superpositions persistantes et configurables à partir d’un **nouveau** volet Disposition de **l’outil Elements.**  

Pour activer cette fonctionnalité expérimentale, accédez à Activer les fonctionnalités expérimentales et activez la case à cocher en regard de Activer les nouvelles fonctionnalités de débogage de la grille **CSS (options**de configuration disponibles dans le volet de barre latérale de disposition dans les éléments après le redémarrage). [][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]  

Pour plus d’informations sur cette expérience, accédez à Activer les nouvelles fonctionnalités de débogage de grille [CSS.][DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]  

Problème de chrome : [#1047356][CR1047356]  

### <a name="table-copied-from-the-console-preserves-formatting"></a>Le tableau copié à partir de la console conserve la mise en forme  

Dans Microsoft Edge 85 ou une antérieure, la mise en forme d’une copie `console.table` a été perdue.  Si vous avez copié la sortie de l’API console de [tableau][DevtoolsConsoleApiTable] et que vous l’avez copiée, seul le texte de la table a été conservé.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta.msft.png" alt-text="sortie de l’API console de tableau dans Microsoft Edge 85 ou une antérieure" lightbox="../../media/2020/08/console-table-beta.msft.png":::
         `table` Sortie de l’API console dans Microsoft Edge 85 ou une antérieure  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png" alt-text="table Console API output from Microsoft Edge 85 or earlier pasted into Visual Studio Code" lightbox="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png":::
         `table` Sortie de l’API console à partir de Microsoft Edge 85 ou d’une Visual Studio Code  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Dans Microsoft Edge 86 ou version ultérieure, lorsque vous copiez un tableau à partir de la **console,** la mise en forme est désormais conservée.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary.msft.png" alt-text="table Console API output in Microsoft Edge 86 or later" lightbox="../../media/2020/08/console-table-canary.msft.png":::
         `table` Sortie de l’API console dans Microsoft Edge 86 ou une ultérieure  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png" alt-text="table Console API output from Microsoft Edge 86 or later pasted into Visual Studio Code" lightbox="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png":::
         `table` Sortie de l’API console de Microsoft Edge 86 ou ultérieurement Visual Studio Code  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Problème de chrome : [#1115011][CR1115011]  

### <a name="source-order-viewer-for-easier-accessibility-testing"></a>Visionneuse d’ordre source pour faciliter les tests d’accessibilité  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalité expérimentale":::
   Fonctionnalité expérimentale  
:::image-end:::  

Le nouvel élément d’aide sur l’accessibilité affiche l’ordre des éléments dans la source.  

:::image type="complex" source="../../media/2020/08/source-order-viewer.msft.png" alt-text="Activer Afficher l’ordre de la source" lightbox="../../media/2020/08/source-order-viewer.msft.png":::
   Activer **Afficher l’ordre de la source**  
:::image-end:::  

Cette fonctionnalité facilite le test de l’expérience des utilisateurs de lecteur d’écran et de clavier sur votre site web ou votre application.  Les lecteurs d’écran et la navigation au clavier dépendent du contenu placé dans un ordre particulier dans le code source de votre site web ou de votre application, afin qu’il corresponde à la page rendue.  L’Afficheur des commandes sources affiche les différences potentielles dans l’ordre entre la page rendue et le code source.  

Pour activer cette fonctionnalité expérimentale, accédez à Activer les fonctionnalités expérimentales et activez la case à cocher en regard de Activer la visionneuse de commandes **source.** [][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]  

Pour plus d’informations sur cette expérience, accédez à [Activer l’Observateur de commandes source.][DevtoolsExperimentalFeaturesEnableSourceOrderViewer]  

Problème de chrome : [#1094406][CR1094406]  

<!--
### DevTools language enhancements  

Your feedback and internal discoveries uncovered which text strings used in the Microsoft Edge feedback should remain untranslated or create confusion when translated.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-stable.msft.png" alt-text="Microsoft Edge DevTools in Traditional Chinese" lightbox="localization-improvements-chinese-complex-stable.msft.png":::
         Microsoft Edge DevTools 85 and earlier in Traditional Chinese  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png" alt-text="Microsoft Edge DevTools in Japanese" lightbox="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png":::
         Microsoft Edge DevTools 86  or later in Traditional Chinese  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.  

The current effort to improve translation quality enables easier support for more languages in the future.  
-->  

### <a name="highlight-all-search-results-in-elements-tool"></a>Mettre en surbrill valeur tous les résultats de recherche dans l’outil Éléments  

Dans Microsoft Edge 84 et 85, le premier résultat de recherche dans l’outil **Éléments** n’a pas été mis en surbrillant.  Les résultats de recherche restants ont été mis en surbrillant correctement.  

Merci d’avoir envoyé vos commentaires et d’avoir amélioré Chromium.  Vos commentaires ont révélé un [problème #1103316][CR1103316] dans le projet Chromium open source.  

:::image type="complex" source="../../media/2020/08/elements- search-highlight-fixed.msft.png" alt-text="Premier résultat de recherche mis en surbrillant dans le panneau Éléments dans Microsoft Edge 84 ou ultérieur" lightbox="../../media/2020/08/elements- search-highlight-fixed.msft.png":::
   Premier résultat de recherche mis en surbrillant sur **l’outil Éléments** dans Microsoft Edge 84 ou une ultérieure  
:::image-end:::  

Le problème est désormais résolu dans toutes les versions de Microsoft Edge.  

Problème de chrome : [#1103316][CR1103316]  

## <a name="announcements-from-the-chromium-project"></a>Annonces du projet de Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-media-tool"></a>Outil Nouveau média  

DevTools affiche désormais les informations des joueurs multimédias dans [l’outil Multimédia.][DevtoolsMediaPanelIndex]  

Pour ouvrir le nouvel **outil Multimédia,** terminez l’étape suivante.  

1.  Choose **Customize and control DevTools** \( `...` \) > More **tools**  >  **Media**.  
    
    :::image type="complex" source="../../media/2020/08/media-panel.msft.png" alt-text="Outil Nouveau média" lightbox="../../media/2020/08/media-panel.msft.png":::
       Outil **Nouveau** média  
    :::image-end:::  

Avant le nouvel **outil Multimédia** dans DevTools, les informations de journalisation et de débogage sur les joueurs vidéo se trouvaient sous le paramètre **Joueurs récents.**  Pour ouvrir le **paramètre Joueurs** récents, accédez à l’outil Players et `edge://media-internals` **choisissez-le.**  

Affichez le contenu en direct et examinez les problèmes potentiels plus rapidement, y compris les exemples suivants.  

*   Pourquoi les images sont-elles abandonnées ?  
*   Pourquoi JavaScript interagit-il avec le joueur de manière inattendue ?  

### <a name="capture-node-screenshots-using-the-elements-tool-context-menu"></a>Capture d’écran de nœud à l’aide du menu contextique de l’outil Éléments  

Vous pouvez maintenant capturer des captures d’écran de nœud à l’aide du menu contextique de **l’outil Éléments.**  

Par exemple, pour prendre une capture d’écran de la table des matières, pointez sur l’élément, ouvrez le menu contextuel \(clic droit\), puis sélectionnez **Capture d’écran du nœud**.  

:::image type="complex" source="../../media/2020/08/capture-node-screenshot.msft.png" alt-text="Capture d’écran de nœud" lightbox="../../media/2020/08/capture-node-screenshot.msft.png":::
   Capture d’écran de nœud  
:::image-end:::  

Problème de chrome : [#1100253][CR1100253]  

### <a name="issues-tool-updates"></a>Mises à jour de l’outil Problèmes  

La barre d’avertissement Problèmes de l’outil **Console** est désormais remplacée par un message normal.  

<!--todo: this figure need to be updated  -->  

:::image type="complex" source="../../media/2020/08/issue-console-msg.msft.png" alt-text="Problèmes dans le message de la console" lightbox="../../media/2020/08/issue-console-msg.msft.png":::
   Problèmes dans le message de la console  
:::image-end:::  

Les problèmes de cookie tiers sont désormais masqués par défaut dans **l’outil Problèmes.**  Activez la nouvelle **case à cocher Inclure les problèmes de cookie tiers** pour afficher les problèmes.  

:::image type="complex" source="../../media/2020/08/third-party-cookies.msft.png" alt-text="Case à cocher problèmes de cookie tiers" lightbox="../../media/2020/08/third-party-cookies.msft.png":::
   Case à cocher problèmes de cookie tiers  
:::image-end:::  

Problèmes de chrome : [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]  

### <a name="emulate-missing-local-fonts"></a>Émuler les polices locales manquantes  

Ouvrez [l’outil de rendu][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] et utilisez la nouvelle fonctionnalité Désactiver les **polices locales** pour émuler les `local()` sources manquantes dans les `@font-face` règles.  

Par exemple, lorsque la police est installée sur votre appareil et que la règle l’utilise comme police, Microsoft Edge utilise le fichier de police `Rubik` `@font-face src` local de votre `local()` appareil.  

Lorsque **disable local fonts** is enabled, DevTools ignores the `local()` fonts and fetches each from the network.  

:::image type="complex" source="../../media/2020/08/disable-font.msft.png" alt-text="Émuler les polices locales manquantes" lightbox="../../media/2020/08/disable-font.msft.png":::
   Émuler les polices locales manquantes  
:::image-end:::  

Si vous utilisez deux copies différentes de la même police lors du développement, telles que les exemples suivants.  

*   Police locale pour vos outils de conception.  
*   Police web pour votre code.  

Utilisez **Désactiver les polices locales** pour faciliter l’effectuer.  

*   Déboguer et mesurer les performances de chargement et l’optimisation des polices web.  
*   Vérifiez la précision de vos règles `@font-face` CSS.  
*   Découvrez les différences entre les versions locales installées sur votre appareil et une police web.  

Problème de chrome : [#384968][CR384968]  

### <a name="emulate-inactive-users"></a>Émuler les utilisateurs inactifs  

[L’API de détection d’inactivité][WebDevIdleDetection] permet aux développeurs de détecter les utilisateurs inactifs et de réagir aux changements d’état d’inactivité.  Vous pouvez désormais utiliser DevTools pour émuler les changements d’état d’inactivité dans l’outil **Sensors** pour l’état de l’utilisateur et de l’écran au lieu d’attendre que l’état d’inactivité réel change.  Vous pouvez ouvrir **l’outil Capteurs** à partir du [caisse.][DevtoolsCustomizeIndexDrawer]  

:::image type="complex" source="../../media/2020/08/emulate-idle.msft.png" alt-text="Émuler les utilisateurs inactifs" lightbox="../../media/2020/08/emulate-idle.msft.png":::
   Émuler les utilisateurs inactifs  
:::image-end:::  

Problème de chrome : [#1090802][CR1090802]  

### <a name="emulate-prefers-reduced-data"></a>Émuler prefers-reduced-data  

> [!NOTE]
> Dans Microsoft Edge 86, pour activer cette fonctionnalité, accédez à l’indicateur de fonctionnalités de plateforme Web expérimentale et `edge://flags#enable-experimental-web-platform-features` **activez-le.**  L’option d’émulation s’affiche uniquement si l’indicateur est activé.  

La requête multimédia préférer les données [réduites][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] détecte les préférences de contenu utilisateur pour les données réduites.  S’il est sélectionné, l’utilisateur reçoit un contenu de page de remplacement qui utilise moins de données.  

Vous pouvez maintenant utiliser DevTools pour émuler la `prefers-reduced-data` requête multimédia.  

:::image type="complex" source="../../media/2020/08/emulate-prefers-reduced-data.msft.png" alt-text="Émuler prefers-reduced-data" lightbox="../../media/2020/08/emulate-prefers-reduced-data.msft.png":::
   Émuler prefers-reduced-data  
:::image-end:::  

Problème de chrome : [#1096068][CR1096068]  

### <a name="support-for-new-javascript-features"></a>Prise en charge des nouvelles fonctionnalités JavaScript  

Les devTools ont désormais mieux pris en charge les fonctionnalités de langage JavaScript suivantes.  

| Fonctionnalité de langage JavaScript | Détails |  
|:--- |:--- |  
| [Opérateurs d’affectation logique][V8FeaturesLogicalAssignment] | DevTools prend désormais en charge l’affectation logique avec le nouveau , et les opérateurs dans les outils `&&=` `||=` Console et `??=` **Sources.** ****  |  
| Séparateurs [numériques][V8FeaturesNumericSeparators] à impression courte | DevTools imprime maintenant correctement les séparateurs numériques dans l’outil **Sources.**  |  

Problèmes de chrome : [1086817][CR1086817], [1080569][CR1080569]  

### <a name="lighthouse-62-in-the-lighthouse-panel"></a>Île 6.2 dans le panneau Panneau de sélection  

**L’outil Îles** exécute à présent Ce dernier 6.2.  Pour obtenir la liste complète des modifications, accédez aux notes de [publication de Cerr.][GithubGooglechromeLighthouseV620]  

Problème de chrome : [#772558][CR772558]  

### <a name="deprecation-of-other-origins-listing-in-the-service-workers-pane"></a>Désérision d’autres origines dans le volet Travailleurs du service  

DevTools fournit désormais un **** lien à partir du volet Travailleurs **** du service \(**Outil** d’application > Volet Travailleurs du service\) pour afficher la liste complète des travailleurs de service provenant d’autres origines.  Pour accéder à la liste sans ouvrir de DevTools, accédez à `edge://service-worker-internals/?devtools` .  

Auparavant, DevTools affichait une liste imbriée sous l’outil **Application** pour > **de travail du service.**  

:::image type="complex" source="../../media/2020/08/sw-other-origins.msft.png" alt-text="Lien vers d’autres origines" lightbox="../../media/2020/08/sw-other-origins.msft.png":::
   Lien vers d’autres origines  
:::image-end:::  

Problème de chrome : [#807440][CR807440]  

### <a name="show-coverage-summary-for-filtered-items"></a>Afficher le résumé de la couverture pour les éléments filtrés  

DevTools recalcule maintenant et affiche dynamiquement un résumé des informations de couverture.  L’affichage dynamique est déclenché lorsque des filtres sont appliqués dans [l’outil Couverture.][DevtoolsCoverageIndex]  Avant que **l’outil** Couverture affiche toujours un résumé de toutes les informations de couverture.  

Dans la première des figures suivantes, le résumé s’affiche initialement et, dans la seconde des figures suivantes, le résumé s’affiche après l’application du filtrage `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` CSS.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare.msft.png" alt-text="Résumé de la couverture" lightbox="../../media/2020/08/coverage-compare.msft.png":::
         Résumé de la couverture  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare-css-filter.msft.png" alt-text="Résumé de la couverture pour les éléments filtrés" lightbox="../../media/2020/08/coverage-compare-css-filter.msft.png":::
         Résumé de la couverture pour les éléments filtrés  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Problème de chrome : [#1061385][CR1090802]  

### <a name="new-frame-details-view-in-application-panel"></a>Affichage des détails d’une nouvelle image dans le panneau Application  

DevTools affiche désormais une vue détaillée pour chaque image.  Pour y accéder, choisissez un cadre sous le menu **Cadres** de **l’outil Application.**  

:::image type="complex" source="../../media/2020/08/frame-details.msft.png" alt-text="Nouvelle vue détaillée d’un cadre dans le panneau Application" lightbox="../../media/2020/08/frame-details.msft.png":::
   Nouvelle vue détaillée d’un cadre dans **l’outil Application**  
:::image-end:::  

Problème de chrome : [#1093247][CR1093247]  

#### <a name="frame-details-for-opened-windows"></a>Détails du cadre pour les fenêtres ouvertes  

Les fenêtres ouvertes et les fenêtres pop-up s’affichent désormais également sous l’arborescence d’images.  L’affichage détaillé des fenêtres ouvertes inclut des informations de sécurité supplémentaires.  

:::image type="complex" source="../../media/2020/08/window-opener.msft.png" alt-text="Nouveau cadre en affichage détaillé pour les fenêtres ouvertes" lightbox="../../media/2020/08/window-opener.msft.png":::
   Nouveau cadre en affichage détaillé pour les fenêtres ouvertes  
:::image-end:::  

Problème de chrome : [#1107766][CR1107766]  

#### <a name="security-and-isolation-information"></a>Informations de sécurité et d’isolation  

Le contexte sécurisé, la stratégie [COEP (Cross-Origin-Embedder-Policy)][WebDevCoopCoep]et la stratégie [DNS (Cross-Origin-Opener-Policy)][WebDevCoopCoep] sont désormais affichés dans les détails de l’image.  

:::image type="complex" source="../../media/2020/08/coep-coop.msft.png" alt-text="Informations de sécurité et d’isolation" lightbox="../../media/2020/08/coep-coop.msft.png":::
   Informations de sécurité et d’isolation  
:::image-end:::  

À l’avenir, l’équipe Microsoft Edge DevTools et l’équipe Chrome DevTools prévoient d’ajouter des informations de sécurité supplémentaires aux détails de l’image.  

Problème de chrome : [#1051466][CR1051466]  

### <a name="elements-and-network-panel-updates"></a>Éléments et mises à jour du panneau réseau  

#### <a name="accessible-color-suggestion-in-the-styles-pane"></a>Suggestion de couleurs accessibles dans le volet Styles  

DevTools fournit désormais des suggestions de couleur pour le texte à contraste faible.  

Dans l’exemple ci-dessous, `h1` le texte est à faible contraste.  Pour résoudre ce problème, ouvrez le s sélectionneur de couleurs de la `color` propriété dans le volet **Styles.**  Après avoir développé la section **Coefficient de contraste,** DevTools fournit des suggestions de couleurs AA et AAA.  Choisissez la couleur suggérée pour appliquer la couleur.  

:::image type="complex" source="../../media/2020/08/contrast-color-suggestion.msft.png" alt-text="Le s picker de couleur suggère des suggestions de couleurS AA et AAA" lightbox="../../media/2020/08/contrast-color-suggestion.msft.png":::
   Le s picker de couleur suggère des suggestions de couleurS AA et AAA  
:::image-end:::  

Problème de chrome : [#1093227][CR1093227]  

#### <a name="reinstate-properties-pane-in-the-elements-panel"></a>Rétablir le volet Propriétés dans le volet Éléments  

Le **volet Propriétés** est de retour.  Il a [été supprimé dans Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].  L’équipe Microsoft Edge DevTools et l’équipe Chrome DevTools planifient des améliorations pour l’inspection des propriétés des éléments.  

:::image type="complex" source="../../media/2020/08/properties-pane.msft.png" alt-text="Volet Propriétés du panneau Éléments" lightbox="../../media/2020/08/properties-pane.msft.png":::
   **Volet Propriétés** de **l’outil Éléments**  
:::image-end:::  

Problème de chrome :  <!--  [#1105205][CR1105205],  -->  [#1116085] [CR1116085]  

<!--  
#### Human-readable X-Client-Data header values in the Network panel  

When inspecting a network resource in the Network panel, DevTools now formats any `X-Client-Data` header values in **Headers** pane as code.  

The `X-Client-Data` HTTP header contains a list of experiment IDs and Microsoft Edge flags that are enabled in your browser.  The raw header values look like opaque strings since the values are `base-64-encoded`, serialized [protocol buffers][GoogleDevelopersProtocolBuffers].  To make the contents more transparent to developers, DevTools now shows the decoded values.  

:::image type="complex" source="../../media/2020/08/x-client-data.msft.png" alt-text="Human-readable `X-Client-Data` header values" lightbox="../../media/2020/08/x-client-data.msft.png":::
   Human-readable `X-Client-Data` header values  
:::image-end:::  

Chromium issue: [#1103854][CR1103854]  
-->  

#### <a name="autocomplete-custom-fonts-in-the-styles-pane"></a>Autocomplete custom fonts in the Styles pane  

Les polices importées sont désormais ajoutées à la liste de lacompletion automatique CSS lors de la modification de la propriété dans le `font-family` **volet Styles.**  

Par exemple, si une police personnalisée est installée sur l’ordinateur local, elle s’affiche dans la liste d’achèvement `monospace` CSS.  Dans les versions précédentes de Microsoft Edge, la police n’était pas affichée.

:::image type="complex" source="../../media/2020/08/font-auto-complete.msft.png" alt-text="Autocomplete custom fonts" lightbox="../../media/2020/08/font-auto-complete.msft.png":::
   Autocomplete custom fonts  
:::image-end:::  

Problème de chrome : [#1106221][CR1106221]  

#### <a name="consistently-display-resource-type-in-network-panel"></a>Afficher systématiquement le type de ressource dans le panneau réseau  

DevTools affiche désormais de manière cohérente le même type de ressource que la demande réseau d’origine et s’affiche à la valeur de colonne Type lorsque la redirection \(code d’état `/ Redirect` HTTP 302\) se produit. ****  

Auparavant, DevTools a parfois modifié le `Other` type.  

:::image type="complex" source="../../media/2020/08/network-redirect.msft.png" alt-text="Afficher le type de ressource de redirection" lightbox="../../media/2020/08/network-redirect.msft.png":::
   Afficher le type de ressource de redirection  
:::image-end:::  

Problème de chrome : [#997694][CR997694]  

#### <a name="clear-buttons-in-the-elements-and-network-tools"></a>Effacer les boutons dans les outils Éléments et réseau  

Les zones de texte suivantes ont désormais **des boutons** Effacer.  

*   Zones de texte de filtre dans le **volet Styles** et **l’outil** Réseau.  
*   Zone de texte de recherche DOM dans **l’outil Éléments.**  

Sélectionnez **le bouton** Effacer pour supprimer tout texte en entrée.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-elements.msft.png" alt-text="Effacer les boutons des panneaux Éléments" lightbox="../../media/2020/08/clear-button-elements.msft.png":::
         Effacer les boutons dans les **outils Éléments**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-network.msft.png" alt-text="Effacer les boutons dans les panneaux Réseau" lightbox="../../media/2020/08/clear-button-network.msft.png":::
         Effacer les boutons dans les  **outils** réseau  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Problème de chrome : [#1067184][CR1067184]  

## <a name="download-the-microsoft-edge-preview-channels"></a>Télécharger les canaux d’aperçu Microsoft Edge  

Si vous utilisez Windows ou macOS, envisagez d’utiliser les canaux d’aperçu [Microsoft Edge][MicrosoftEdgePreviewChannels] comme navigateur de développement par défaut.  Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Contacter l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png "Icône Paramètres DevTools"  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-panel "Annulation du volet Propriétés dans le panneau Éléments - Nouveautés de DevTools (Microsoft Edge 84) | Documents Microsoft"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Fonctionnalités de débogage de grille CSS - Nouveautés de DevTools (Microsoft Edge 85) | Documents Microsoft"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Émuler des appareils mobiles dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personnaliser les raccourcis clavier dans l'| Microsoft Edge DevTools Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Activer les API expérimentales : fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Émulation : prise en charge du mode double écran - Fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Activer la visionneuse de commandes sources - Fonctionnalités expérimentales | Documents Microsoft"
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: https://review.docs.microsoft.com/microsoft-edge/devtools-guide-chromium/experimental-features?branch=user/zoghadya/dual-screen-experiment#emulation-support-dual-screen-mode "Émulation : prise en charge du mode double écran - Fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Test sur des appareils pliables et à double écran : fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Activer les fonctionnalités expérimentales : fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "tableau - Référence de l’API de console | Documents Microsoft"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Recherchez du code JavaScript et CSS inutilisé avec l’onglet Couverture dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Caisse : personnaliser les paramètres DevTools de Microsoft Edge | Documents Microsoft"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analyser les performances de rendu avec l’onglet Rendu - Référence de l’analyse des performances | Documents Microsoft"  
[DevtoolsMediaPanelIndex]: /microsoft-edge/devtools-guide-chromium/media-panel/index "Afficher et déboguer les informations des joueurs multimédias | Documents Microsoft"  

[DualScreenIntroductionHowWorkSeam]:  /dual-screen/introduction#how-to-work-with-the-seam "Comment travailler avec le seam : introduction aux appareils à double écran | Documents Microsoft"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Fonctionnalité d’écran multimédia CSS pour la détection à double écran | Documents Microsoft"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "L’API JavaScript getWindowSegments pour les appareils à double écran | Documents Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux d’aperçu Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio Code "  
[VisualStudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio clavier du code pour Windows"  

[MicrosoftSurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Le nouveau Surface Duo"  

[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools compte Twitter"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bogues Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools : autoriser la personnalisation des raccourcis clavier/des liaisons de touches | Bogues Chromium"
[CR384968]: https://crbug.com/384968 "Option pour ignorer les polices locales () | Bogues Chromium"  
[CR772558]: https://crbug.com/772558 "DevTools : mise à jour vers la dernière version de | Bogues Chromium"  
[CR807440]: https://crbug.com/807440 "Chrome se verrouille avec un grand nombre de SW | Bogues Chromium"  
[CR997694]: https://crbug.com/997694 "Les demandes XHR avec l’état 302 ne sont pas affichées sous le filtre \"xhr\» dans le panneau réseau | Bogues Chromium"  
[CR1047356]: https://crbug.com/1047356 "Outils Grille CSS/Flexbox/Tableau | Bogues Chromium"  
[CR1051466]: https://crbug.com/1051466 "Prise en charge du débogage PUNAISE/COEP dans DevTools | Bogues Chromium"  
[CR1054281]: https://crbug.com/1054281 "Demande de fonctionnalité : DevTools doit émuler les appareils pliables et à double écran | Bogues Chromium"  
[CR1067184]: https://crbug.com/1067184 "Demande de fonctionnalité : effacer le bouton filtre sur les éléments & réseau - > filtre de style | Bogues Chromium"  
[CR1068116]: https://crbug.com/1068116 "☂ panneau d’expédition des problèmes | Bogues Chromium"  
[CR1080569]: https://crbug.com/1080569 "acorn ne prend pas en charge les opérateurs d’affectation logique | Bogues Chromium"  
[CR1080589]: https://crbug.com/1080589 "Classifier les problèmes par des tiers/des | Bogues Chromium"  
[CR1086817]: https://crbug.com/1086817 "acorn ne prend pas en charge les séparateurs numériques | Bogues Chromium"  
[CR1090802]: https://crbug.com/1090802 "Simuler les changements d’état d’inactivité à partir des api de détection d’inactivité | Bogues Chromium"  
[CR1093227]: https://crbug.com/1093227 "DevTools : suggérer les couleurs les plus proches accessibles | Bogues Chromium"  
[CR1093247]: https://crbug.com/1093247 "Afficher des informations sur les cadres dans le panneau d'| Bogues Chromium"  
[CR1094406]: https://crbug.com/1094406 "Les développeurs veulent une visionneuse de commande source pour AT https://webwewant.fyi/wants/64/"  
[CR1096068]: https://crbug.com/1096068 "DevTools : prise en charge de l’émulation de la fonctionnalité multimédia « prefers-reduced-data | Bogues Chromium"  
[CR1096481]: https://crbug.com/1096481 "Problèmes de positionnement des bannières | Bogues Chromium"  
[CR1100253]: https://crbug.com/1100253 "Ajouter un raccourci de nœud de capture d’écran dans le menu context | Bogues Chromium"  
[CR1103316]: https://crbug.com/1103316 "La recherche d’éléments ne résout pasNode (mettre en surbrillon le texte, etc.) sur le premier résultat de | Bogues Chromium"  
[CR1103854]: https://crbug.com/1103854 "De-obfuscate X-Client-Data values in Developer Tools | Bogues Chromium"  
<!--  [CR1105205]: https://crbug.com/1105205 "Issue 1105205 | Chromium bugs"  -->  
[CR1106221] : « Ajouter des polices importées à lacomplétion automatique de la famille de polices dans le panneau https://crbug.com/1106221 Styles | Bogues Chromium »  
[CR1107766] : « Afficher des informations sur les images générées par ' window.open() » dans l’arborescence https://crbug.com/1107766 d’images | Bogues Chromium »  
[CR1115011] : « Lors de la copie d’un tableau à partir de la console, la structure de la table n’est pas https://crbug.com/1115011 conservée | Bogues Chromium »  
[CR1116085] : « Veuillez retourner l’inspecteur de https://crbug.com/1116085 propriétés DevTools | Bogues Chromium »  

[CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData]: https://drafts.csswg.org/mediaqueries-5#descdef-media-prefers-reduced-data "prefers-reduced-data - Media Queries Level 5 | Brouillons de l’éditeur de groupe de travail CSS W3C"  

[GithubGooglechromeLighthouseV620]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.2.0 "v6.2.0 - GoogleChrome/| GitHub"  

[GoogleDevelopersProtocolBuffers]: https://developers.google.com/protocol-buffers "Mémoires tampons de protocole | Développeurs Google"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "| Samsung (États-Unis)"  

[V8FeaturesLogicalAssignment]: https://v8.dev/features/logical-assignment "Affectation logique | V8"  
[V8FeaturesNumericSeparators]: https://v8.dev/features/numeric-separators "Séparateurs numériques | V8"  

[WebDevCoopCoep]: https://web.dev/coop-coep "Rendre votre site web \ « cross-origin isolated\ » à l’aide de LA TECHNOLOGIE | web.dev"  
[WebDevIdleDetection]: https://web.dev/idle-detection "Détecter les utilisateurs inactifs avec l’API de détection d’inactivité | web.dev"  
[WebDevNonCompositedAnimations]: https://web.dev/non-composited-animations "Évitez les animations non composites | web.dev"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/updates/2020/08/devtools/index) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
