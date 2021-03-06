---
description: Match keyboard shortcuts to Visual Studio Code, emulate Surface Duo and Samsung Samsung Fold, CSS grid overlay improvements, and more.
title: Nouveautés de DevTools (Microsoft Edge 86)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: ec2219e9ebdd5d79c61bcaa813f7784246b1f5d0
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564944"
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

Dans Microsoft Edge 86, vous pouvez faire correspondre les raccourcis clavier dans DevTools à vos raccourcis dans [Microsoft Visual Studio Code .][VisualStudioCodeMain]  

:::image type="complex" source="../../media/2020/08/keyboard-shortcut.msft.png" alt-text="Faire correspondre les raccourcis clavier dans devTools à Visual Studio Code" lightbox="../../media/2020/08/keyboard-shortcut.msft.png":::
   Faire correspondre les raccourcis clavier dans devTools à Visual Studio Code  
:::image-end:::  

Pour activer cette fonctionnalité, accédez à Personnaliser les raccourcis clavier dans la [Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].  

Par exemple, le raccourci clavier pour mettre en pause ou poursuivre l’exécution d’un script [Visual Studio Code][VisualStudioCodeShortcutsKeyboardWindows] `F5` est .  Avec **devTools (par défaut)** prédéfiny, ce même raccourci dans DevTools est , mais lorsque vous choisissez l’Visual Studio Code `F8` prédéfiny, ce raccourci est désormais également **** `F5` .  

Chromium problème [#174309][CR174309]  

### <a name="emulate-surface-duo-and-samsung-galaxy-fold"></a>Émuler Surface Duo et Samsung Galaxy Fold  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalité expérimentale":::
   Fonctionnalité expérimentale  
:::image-end:::  

Vous pouvez maintenant tester l’apparence de votre site web ou de votre application sur deux nouveaux appareils : [Surface Duo][MicrosoftSurfaceDevicesDuo] et Samsung [Samsung Fold][SamsungMobileGalaxyFold] en Microsoft Edge.  

Pour contribuer à améliorer votre site web ou votre application pour les appareils à double écran et pliables, utilisez les fonctionnalités suivantes lors de [l’émulation de l’appareil][DevtoolsDeviceModeIndex].  

*   [Couvrant,][DevtoolsDeviceModeDualScreenAndFoldables], c’est-à-dire lorsque votre site web \(ou application\) apparaît sur les deux écrans.
*   [Rendu de la jointure][DualScreenIntroductionHowWorkSeam], à savoir l’espace entre les deux écrans.
*   Permettre aux API de plateforme Web expérimentales d’accéder à la nouvelle fonctionnalité multimédia [CSS][DualScreenWebCssMediaSpanning] couvrant l’écran et à l’API [JavaScript getWindowSegments][DualScreenWebJavascriptGetwindowsegments].  

:::image type="complex" source="../../media/2020/08/surface-duo-device-emulation.msft.png" alt-text="Émulation d’appareil pour Surface Duo" lightbox="../../media/2020/08/surface-duo-device-emulation.msft.png":::
   Émulation d’appareil pour Surface Duo  
:::image-end:::  

Pour activer cette fonctionnalité expérimentale, accédez à [Activer les fonctionnalités expérimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] et cochez la case en regard **d’Émulation :** prendre en charge le mode double écran.  

Pour plus d’informations sur cette fonctionnalité, accédez à Émuler les appareils à double écran et [pliables dans Microsoft Edge DevTools][DevtoolsDeviceModeDualScreenAndFoldables].  

Chromium problème : [#1054281][CR1054281]  

### <a name="css-grid-overlay-improvements-and-new-experimental-grid-features"></a>Améliorations de la superposition de grille CSS et nouvelles fonctionnalités de grille expérimentale  

Merci pour les commentaires positifs concernant les superpositions de grille CSS améliorées.  Les superpositions de grille CSS sont désormais activées par défaut et ne vous obligent pas à activer une expérience.  

:::image type="complex" source="../../media/2020/08/css-grid-overlay-article.msft.png" alt-text="Superposition de grille CSS pour l’élément article" lightbox="../../media/2020/08/css-grid-overlay-article.msft.png":::
   Superposition de grille CSS pour `article` l’élément  
:::image-end:::  

> [!NOTE]
> Pour plus d’informations sur les superpositions de grille, accédez aux fonctionnalités de débogage de grille [CSS.][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]  

L Microsoft Edge de DevTools et l’équipe Chrome DevTools collaborent sur des fonctionnalités supplémentaires.  Les nouvelles fonctionnalités incluent plusieurs superpositions persistantes et configurables à partir d’un **nouveau** volet Disposition de **l’outil Éléments.**  

Pour activer cette fonctionnalité expérimentale, accédez à [Activer les fonctionnalités expérimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] et cochez la case en regard de Activer les nouvelles fonctionnalités de débogage de la grille **CSS (options**de configuration disponibles dans le volet de barre latérale de disposition dans les éléments après redémarrage).  

Pour plus d’informations sur cette fonctionnalité, accédez à [Inspect CSS Grid dans Microsoft Edge DevTools][DevtoolsCssGrid].  

Chromium problème : [#1047356][CR1047356]  

### <a name="table-copied-from-the-console-preserves-formatting"></a>Le tableau copié à partir de la console conserve la mise en forme  

Dans Microsoft Edge 85 ou une antérieure, la mise en forme d’une copie a `console.table` été perdue.  Si vous avez copié la sortie de l’API console de [tableau][DevtoolsConsoleApiTable] et que vous l’avez copiée, seul le texte de la table a été conservé.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta.msft.png" alt-text="sortie de l’API console de tableau Microsoft Edge 85 ou antérieure" lightbox="../../media/2020/08/console-table-beta.msft.png":::
         `table` Sortie de l’API de console Microsoft Edge 85 ou antérieure  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png" alt-text="sortie de l’API console de Microsoft Edge 85 ou antérieures dans Visual Studio Code" lightbox="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png":::
         `table` Sortie de l’API de la console Microsoft Edge 85 ou antérieures dans un Visual Studio Code  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Dans Microsoft Edge 86 ou version ultérieure, lorsque vous copiez un tableau à partir de la **console,** la mise en forme est désormais conservée.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary.msft.png" alt-text="table Console API output in Microsoft Edge 86 or later" lightbox="../../media/2020/08/console-table-canary.msft.png":::
         `table` Sortie de l’API console Microsoft Edge 86 ou ultérieure  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png" alt-text="sortie de l’API de console de Microsoft Edge 86 ou ultérieures dans Visual Studio Code" lightbox="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png":::
         `table` Sortie de l’API console Microsoft Edge 86 ou ultérieures dans Visual Studio Code  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Chromium problème : [#1115011][CR1115011]  

### <a name="source-order-viewer-for-easier-accessibility-testing"></a>Visionneuse d’ordre source pour faciliter les tests d’accessibilité  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalité expérimentale":::
   Fonctionnalité expérimentale  
:::image-end:::  

Le nouvel élément d’aide sur l’accessibilité affiche l’ordre des éléments dans la source.  

:::image type="complex" source="../../media/2020/08/source-order-viewer.msft.png" alt-text="Activer Afficher l’ordre de la source" lightbox="../../media/2020/08/source-order-viewer.msft.png":::
   Activer **Afficher l’ordre de la source**  
:::image-end:::  

Cette fonctionnalité facilite le test de l’expérience des utilisateurs de lecteur d’écran et de clavier sur votre site web ou votre application.  Les lecteurs d’écran et la navigation au clavier dépendent du contenu placé dans un ordre particulier dans le code source de votre site web ou de votre application, afin qu’il corresponde à la page rendue.  L’Afficheur des commandes sources affiche les différences potentielles dans l’ordre entre la page rendue et le code source.  

Pour activer cette fonctionnalité expérimentale, accédez à [Activer les fonctionnalités expérimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] et cochez la case en regard de Activer la visionneuse de commandes **source.**  

Pour plus d’informations sur cette expérience, accédez à [Visionneuse de commandes source][DevtoolsExperimentalFeaturesSourceOrderViewer].  

Chromium problème : [#1094406][CR1094406]  

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

### <a name="highlight-all-search-results-in-elements-tool"></a>Mettre en surbrill niveau tous les résultats de recherche dans l’outil Éléments  

Dans Microsoft Edge 84 et 85, le premier résultat de recherche dans l’outil **Éléments** n’a pas été mis en surbrillant.  Les résultats de recherche restants ont été mis en surbrillant correctement.  

Merci d’avoir envoyé vos commentaires et d’avoir amélioré Chromium.  Vos commentaires ont révélé un [problème #1103316][CR1103316] dans le projet de Chromium open source.  

:::image type="complex" source="../../media/2020/08/elements- search-highlight-fixed.msft.png" alt-text="Premier résultat de recherche mis en surbrillant dans le panneau Éléments Microsoft Edge 84 ou ultérieur" lightbox="../../media/2020/08/elements- search-highlight-fixed.msft.png":::
   Premier résultat de recherche mis en surbrillant sur **l’outil Elements** Microsoft Edge 84 ou ultérieur  
:::image-end:::  

Le problème est désormais résolu dans toutes les versions de Microsoft Edge.  

Chromium problème : [#1103316][CR1103316]  

## <a name="announcements-from-the-chromium-project"></a>Annonces du projet de Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-media-tool"></a>Outil Nouveau média  

DevTools affiche désormais les informations des joueurs multimédias dans l’outil [Media][DevtoolsMediaPanelIndex].  

Pour ouvrir le nouvel **outil Multimédia,** terminez l’étape suivante.  

1.  Choose **Customize and control DevTools** \( `...` \) > More **tools**  >  **Media**.  
    
    :::image type="complex" source="../../media/2020/08/media-panel.msft.png" alt-text="Outil Nouveau média" lightbox="../../media/2020/08/media-panel.msft.png":::
       Outil **Nouveau** média  
    :::image-end:::  

Avant le nouvel **outil Multimédia** dans DevTools, les informations de journalisation et de débogage sur les joueurs vidéo se trouvaient sous le paramètre **Joueurs récents.**  Pour ouvrir le **paramètre Joueurs récents,** accédez `edge://media-internals` à l’outil Players et **choisissez-le.**  

Affichez le contenu en direct et examinez les problèmes potentiels plus rapidement, y compris les exemples suivants.  

*   Pourquoi les images sont-elles abandonnées ?  
*   Pourquoi JavaScript interagit-il avec le joueur de manière inattendue ?  

### <a name="capture-node-screenshots-using-the-elements-tool-context-menu"></a>Capture d’écran de nœud à l’aide du menu contextique de l’outil Éléments  

Vous pouvez maintenant capturer des captures d’écran de nœud à l’aide du menu contextique de **l’outil Éléments.**  

Par exemple, pour prendre une capture d’écran de la table des matières, pointez sur l’élément, ouvrez le menu contextuel \(clic droit\), puis sélectionnez **Capture d’écran du nœud**.  

:::image type="complex" source="../../media/2020/08/capture-node-screenshot.msft.png" alt-text="Capture d’écran de nœud" lightbox="../../media/2020/08/capture-node-screenshot.msft.png":::
   Capture d’écran de nœud  
:::image-end:::  

Chromium problème : [#1100253][CR1100253]  

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

Chromium problèmes : [1096481,][CR1096481] [1068116][CR1068116], [1080589][CR1080589]  

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

Chromium problème : [#384968][CR384968]  

### <a name="emulate-inactive-users"></a>Émuler les utilisateurs inactifs  

[L’API de détection d’inactivité][WebDevIdleDetection] permet aux développeurs de détecter les utilisateurs inactifs et de réagir aux changements d’état d’inactivité.  Vous pouvez désormais utiliser DevTools pour émuler les changements d’état d’inactivité dans l’outil **Sensors** pour l’état utilisateur et l’état de l’écran au lieu d’attendre que l’état d’inactivité réel change.  Vous pouvez ouvrir **l’outil Capteurs** à partir du [caisse.][DevtoolsCustomizeIndexDrawer]  

:::image type="complex" source="../../media/2020/08/emulate-idle.msft.png" alt-text="Émuler les utilisateurs inactifs" lightbox="../../media/2020/08/emulate-idle.msft.png":::
   Émuler les utilisateurs inactifs  
:::image-end:::  

Chromium problème : [#1090802][CR1090802]  

### <a name="emulate-prefers-reduced-data"></a>Émuler prefers-reduced-data  

> [!NOTE]
> Dans Microsoft Edge 86, pour activer cette fonctionnalité, accédez à l’indicateur de fonctionnalités de plateforme Web expérimentale et `edge://flags#enable-experimental-web-platform-features` **activez-le.**  L’option d’émulation s’affiche uniquement si l’indicateur est activé.  

La requête multimédia préférer les données [réduites][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] détecte les préférences de contenu utilisateur pour les données réduites.  S’il est sélectionné, l’utilisateur reçoit un contenu de page de remplacement qui utilise moins de données.  

Vous pouvez maintenant utiliser DevTools pour émuler la `prefers-reduced-data` requête multimédia.  

:::image type="complex" source="../../media/2020/08/emulate-prefers-reduced-data.msft.png" alt-text="Émuler prefers-reduced-data" lightbox="../../media/2020/08/emulate-prefers-reduced-data.msft.png":::
   Émuler prefers-reduced-data  
:::image-end:::  

Chromium problème : [#1096068][CR1096068]  

### <a name="support-for-new-javascript-features"></a>Prise en charge des nouvelles fonctionnalités JavaScript  

Les devTools ont désormais mieux pris en charge les fonctionnalités de langage JavaScript suivantes.  

| Fonctionnalité de langage JavaScript | Détails |  
|:--- |:--- |  
| [Opérateurs d’affectation logique][V8FeaturesLogicalAssignment] | DevTools prend désormais en charge l’affectation logique avec le nouveau , et les opérateurs dans les outils `&&=` `||=` Console et `??=` **Sources.** ****  |  
| Séparateurs [numériques][V8FeaturesNumericSeparators] à impression assez large | DevTools imprime maintenant correctement les séparateurs numériques dans l’outil **Sources.**  |  

Chromium problèmes : [1086817][CR1086817], [1080569][CR1080569]  

### <a name="lighthouse-62-in-the-lighthouse-panel"></a>Île 6.2 dans le panneau Panneau de sélection  

**L’outil Îles** exécute à présent Ce dernier 6.2.  Pour obtenir la liste complète des modifications, accédez aux notes de [publication de Cerr.][GithubGooglechromeLighthouseV620]  

Chromium problème : [#772558][CR772558]  

### <a name="deprecation-of-other-origins-listing-in-the-service-workers-pane"></a>Désérision d’autres origines dans le volet Travailleurs du service  

DevTools fournit désormais un **** lien à partir du volet Travailleurs **** du service \(**Outil** d’application > Volet Travailleurs du service\) pour afficher la liste complète des travailleurs de service provenant d’autres origines.  Pour accéder à la liste sans ouvrir de DevTools, accédez à `edge://service-worker-internals/?devtools` .  

Auparavant, DevTools affichait une liste imbriée sous l’outil **Application** pour > **de travail du service.**  

:::image type="complex" source="../../media/2020/08/sw-other-origins.msft.png" alt-text="Lien vers d’autres origines" lightbox="../../media/2020/08/sw-other-origins.msft.png":::
   Lien vers d’autres origines  
:::image-end:::  

Chromium problème : [#807440][CR807440]  

### <a name="show-coverage-summary-for-filtered-items"></a>Afficher le résumé de la couverture pour les éléments filtrés  

DevTools recalcule maintenant et affiche dynamiquement un résumé des informations de couverture.  L’affichage dynamique est déclenché lorsque des filtres sont appliqués dans l’outil [Couverture.][DevtoolsCoverageIndex]  Avant que **l’outil** Couverture affiche toujours un résumé de toutes les informations de couverture.  

Dans la première des figures suivantes, le résumé s’affiche initialement et dans la seconde figure, le résumé s’affiche après l’application du filtrage `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` CSS.  

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

Chromium problème : [#1061385][CR1090802]  

### <a name="new-frame-details-view-in-application-panel"></a>Affichage des détails d’une nouvelle image dans le panneau Application  

DevTools affiche désormais une vue détaillée pour chaque image.  Pour y accéder, choisissez un cadre sous le menu **Cadres** de **l’outil Application.**  

:::image type="complex" source="../../media/2020/08/frame-details.msft.png" alt-text="Nouvelle vue détaillée d’un cadre dans le panneau Application" lightbox="../../media/2020/08/frame-details.msft.png":::
   Nouvelle vue détaillée d’un cadre dans **l’outil Application**  
:::image-end:::  

Chromium problème : [#1093247][CR1093247]  

#### <a name="frame-details-for-opened-windows"></a>Détails du cadre pour les fenêtres ouvertes  

Les fenêtres ouvertes et les fenêtres pop-up s’affichent désormais également sous l’arborescence d’images.  L’affichage détaillé des fenêtres ouvertes inclut des informations de sécurité supplémentaires.  

:::image type="complex" source="../../media/2020/08/window-opener.msft.png" alt-text="Nouveau cadre en affichage détaillé pour les fenêtres ouvertes" lightbox="../../media/2020/08/window-opener.msft.png":::
   Nouveau cadre en affichage détaillé pour les fenêtres ouvertes  
:::image-end:::  

Chromium problème : [#1107766][CR1107766]  

#### <a name="security-and-isolation-information"></a>Informations de sécurité et d’isolation  

Le contexte sécurisé, la stratégie [COEP (Cross-Origin-Embedder-Policy)][WebDevCoopCoep]et la stratégie [DNS (Cross-Origin-Opener-Policy)][WebDevCoopCoep] sont désormais affichés dans les détails de l’image.  

:::image type="complex" source="../../media/2020/08/coep-coop.msft.png" alt-text="Informations de sécurité et d’isolation" lightbox="../../media/2020/08/coep-coop.msft.png":::
   Informations de sécurité et d’isolation  
:::image-end:::  

À l’avenir, l’équipe Microsoft Edge DevTools et l’équipe Chrome DevTools prévoient d’ajouter des informations de sécurité supplémentaires aux détails de l’image.  

Chromium problème : [#1051466][CR1051466]  

### <a name="elements-and-network-panel-updates"></a>Éléments et mises à jour du panneau réseau  

#### <a name="accessible-color-suggestion-in-the-styles-pane"></a>Suggestion de couleurs accessibles dans le volet Styles  

DevTools fournit désormais des suggestions de couleur pour le texte à contraste faible.  

Dans l’exemple ci-dessous, `h1` le texte est à faible contraste.  Pour résoudre ce problème, ouvrez le s sélectionneur de couleurs de la `color` propriété dans le volet **Styles.**  Après avoir développé la section **Coefficient de contraste,** DevTools fournit des suggestions de couleurs AA et AAA.  Choisissez la couleur suggérée pour appliquer la couleur.  

:::image type="complex" source="../../media/2020/08/contrast-color-suggestion.msft.png" alt-text="Le s picker de couleur suggère des suggestions de couleurS AA et AAA" lightbox="../../media/2020/08/contrast-color-suggestion.msft.png":::
   Le s picker de couleur suggère des suggestions de couleurS AA et AAA  
:::image-end:::  

Chromium problème : [#1093227][CR1093227]  

#### <a name="reinstate-properties-pane-in-the-elements-panel"></a>Rétablir le volet Propriétés dans le volet Éléments  

Le **volet Propriétés** est de retour.  Elle a [été Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].  L Microsoft Edge’équipe DevTools et l’équipe Chrome DevTools planifient des améliorations pour l’inspection des propriétés des éléments.  

:::image type="complex" source="../../media/2020/08/properties-pane.msft.png" alt-text="Volet Propriétés du panneau Éléments" lightbox="../../media/2020/08/properties-pane.msft.png":::
   **Volet Propriétés** de **l’outil Éléments**  
:::image-end:::  

Chromium problème :  <!--  [#1105205][CR1105205],  -->  [#1116085] [CR1116085]  

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

Par exemple, si une police personnalisée est installée sur l’ordinateur local, elle s’affiche dans la liste d’achèvement `monospace` CSS.  Dans les versions précédentes Microsoft Edge, la police n’était pas affichée.

:::image type="complex" source="../../media/2020/08/font-auto-complete.msft.png" alt-text="Autocomplete custom fonts" lightbox="../../media/2020/08/font-auto-complete.msft.png":::
   Autocomplete custom fonts  
:::image-end:::  

Chromium problème : [#1106221][CR1106221]  

#### <a name="consistently-display-resource-type-in-network-panel"></a>Afficher systématiquement le type de ressource dans le panneau Réseau  

DevTools affiche désormais de manière cohérente le même type de ressource que la demande réseau d’origine et s’affiche à la valeur de colonne Type lorsque la redirection \(code d’état `/ Redirect` HTTP 302\) se produit. ****  

Auparavant, DevTools a parfois modifié le `Other` type.  

:::image type="complex" source="../../media/2020/08/network-redirect.msft.png" alt-text="Afficher le type de ressource de redirection" lightbox="../../media/2020/08/network-redirect.msft.png":::
   Afficher le type de ressource de redirection  
:::image-end:::  

Chromium problème : [#997694][CR997694]  

#### <a name="clear-buttons-in-the-elements-and-network-tools"></a>Effacer les boutons dans les outils Éléments et réseau  

Les zones de texte suivantes ont désormais **des boutons** Effacer.  

*   Zones de texte de filtre dans le **volet Styles** et **l’outil** Réseau.  
*   Zone de texte de recherche DOM dans **l’outil Éléments.**  

Sélectionnez **le bouton** Effacer pour supprimer tout texte en entrée.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-elements.msft.png" alt-text="Effacer les boutons dans les panneaux Éléments" lightbox="../../media/2020/08/clear-button-elements.msft.png":::
         Effacer les boutons dans les **outils Éléments**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-network.msft.png" alt-text="Effacer les boutons dans les panneaux Réseau" lightbox="../../media/2020/08/clear-button-network.msft.png":::
         Effacer les boutons dans les  **outils** réseau  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Chromium problème : [#1067184][CR1067184]  

## <a name="download-the-microsoft-edge-preview-channels"></a>Télécharger les canaux d’aperçu Microsoft Edge  

Si vous êtes sur Windows ou macOS, envisagez d’utiliser les canaux d Microsoft Edge [d’aperçu][MicrosoftEdgePreviewChannels] comme navigateur de développement par défaut.  Les canaux de prévisualisation vous donnent accès aux dernières fonctionnalités de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Contacter l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-panel "Annulation du volet Propriétés dans le panneau Éléments : nouveautés de DevTools (Microsoft Edge 84) | Documents Microsoft"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Fonctionnalités de débogage de grille CSS - Nouveautés de DevTools (Microsoft Edge 85) | Documents Microsoft"  

[DevtoolsConsoleApiTable]: ../../../console/api.md#table "tableau - Référence de l’API de console | Documents Microsoft"  
[DevtoolsCoverageIndex]: ../../../coverage/index.md "Recherchez du code JavaScript et CSS inutilisé avec l’onglet Couverture dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCssGrid]: ../../../css/grid.md "Inspect CSS Grid in Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCustomizeIndexDrawer]: ../../../customize/index.md#drawer "Caisse : personnaliser Microsoft Edge devTools | Documents Microsoft"  
[DevtoolsCustomizeShortcuts]: ../../../customize/shortcuts.md "Personnaliser les raccourcis clavier dans les DevTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: ../../../device-mode/index.md "Émuler des appareils mobiles dans Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeDualScreenAndFoldables]: ../../../device-mode/dual-screen-and-foldables.md "Émuler les appareils à double écran et pliables dans Microsoft Edge devTools | Documents Microsoft"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: ../../../evaluate-performance/reference.md#analyze-rendering-performance-with-the-rendering-tool "Analyser les performances de rendu à l’aide de l’outil de rendu – Référence de l’analyse des performances | Documents Microsoft"  
<!--  [DevtoolsExperimentalFeaturesEnableExperimentalApis]: ../../../experimental-features/index.md#enable-experimental-apis "Enable experimental APIs - Experimental features | Microsoft Docs"  -->  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: .. /.. /.. /experimental-features/index.md#emulation-support-dual-screen-mode «Emulation: Support double screen mode - Experimental features | Microsoft Docs »  
[DevtoolsExperimentalFeaturesSourceOrderViewer]: .. /.. /.. /experimental-features/index.md#source-order-viewer «Source Order Viewer - Experimental features | Microsoft Docs »
<!--  [DevtoolsExperimentalFeaturesTestOnFoldableDualScreenDevices]: ../../../experimental-features/index.md#test-on-foldable-and-dual-screen-devices "Test on foldable and dual-screen devices - Experimental features | Microsoft Docs"  -->  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: .. /.. /.. /experimental-features/index.md#turn-on-experimental-features " Activer les fonctionnalités expérimentales - Fonctionnalités expérimentales | Microsoft Docs »  
[DevtoolsMediaPanelIndex]: .. /.. /.. /media-panel/index.md « Afficher et déboguer les informations des joueurs multimédias | Microsoft Docs »  

[DualScreenIntroductionHowWorkSeam]:  /dual-screen/introduction#how-to-work-with-the-seam "Utilisation de la jointure - Introduction aux appareils à double écran | Microsoft Docs"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Fonctionnalité couvrant l’écran multimédia CSS pour la détection à double écran | Microsoft Docs"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "API JavaScript getWindowSegments pour appareils à double écran | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux de préversion de Microsoft Edge"  

[VisualStudioCodeMain]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio Code Raccourcis clavier pour Windows"  

[MicrosoftSurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Le nouveau Surface Duo"  

[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools compte Twitter"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bogues Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools : autoriser la personnalisation des raccourcis clavier/des liaisons de touches | Chromium bogues"
[CR384968]: https://crbug.com/384968 "Option pour ignorer les polices locales () | Chromium bogues"  
[CR772558]: https://crbug.com/772558 "DevTools : mise à jour vers la dernière version de | Chromium bogues"  
[CR807440]: https://crbug.com/807440 "Chrome se verrouille avec un grand nombre de SW | Chromium bogues"  
[CR997694]: https://crbug.com/997694 "Les demandes XHR avec l’état 302 ne sont pas affichées sous le filtre \"xhr\» dans le panneau réseau | Chromium bogues"  
[CR1047356]: https://crbug.com/1047356 "Outils Grille CSS/Flexbox/Tableau | Chromium bogues"  
[CR1051466]: https://crbug.com/1051466 "Prise en charge du débogage PUNAISE/COEP dans DevTools | Chromium bogues"  
[CR1054281]: https://crbug.com/1054281 "Demande de fonctionnalité : DevTools doit émuler les appareils pliables et à double écran | Chromium bogues"  
[CR1067184]: https://crbug.com/1067184 "Demande de fonctionnalité : effacer le bouton filtre sur les éléments & réseau - > filtre de style | Chromium bogues"  
[CR1068116]: https://crbug.com/1068116 "☂ panneau d’expédition des problèmes | Chromium bogues"  
[CR1080569]: https://crbug.com/1080569 "acorn ne prend pas en charge les opérateurs d’affectation logique | Chromium bogues"  
[CR1080589]: https://crbug.com/1080589 "Classifier les problèmes par des tiers/des | Chromium bogues"  
[CR1086817]: https://crbug.com/1086817 "acorn ne prend pas en charge les séparateurs numériques | Chromium bogues"  
[CR1090802]: https://crbug.com/1090802 "Simuler les changements d’état d’inactivité à partir des api de détection d’inactivité | Chromium bogues"  
[CR1093227]: https://crbug.com/1093227 "DevTools : suggérer les couleurs les plus proches accessibles | Chromium bogues"  
[CR1093247]: https://crbug.com/1093247 "Afficher des informations sur les cadres dans le panneau d'| Chromium bogues"  
[CR1094406]: https://crbug.com/1094406 "Les développeurs veulent une visionneuse de commande source pour AT https://webwewant.fyi/wants/64/"  
[CR1096068]: https://crbug.com/1096068 "DevTools : prise en charge de l’émulation de la fonctionnalité multimédia « prefers-reduced-data | Chromium bogues"  
[CR1096481]: https://crbug.com/1096481 "Problèmes de positionnement des bannières | Chromium bogues"  
[CR1100253]: https://crbug.com/1100253 "Ajouter un raccourci de nœud de capture d’écran dans le menu context | Chromium bogues"  
[CR1103316]: https://crbug.com/1103316 "La recherche d’éléments ne résout pasNode (mettre en surbrillon le texte, etc.) sur le premier résultat de | Chromium bogues"  
[CR1103854]: https://crbug.com/1103854 "De-obfuscate X-Client-Data values in Developer Tools | Chromium bogues"  
<!--  [CR1105205]: https://crbug.com/1105205 "Issue 1105205 | Chromium bugs"  -->  
[CR1106221] : « Ajouter des polices importées à lacompletion automatique de la famille de polices dans le panneau https://crbug.com/1106221 Styles | Chromium bogues »  
[CR1107766] : « Afficher des informations sur les images générées par ' window.open() » dans l’arborescence https://crbug.com/1107766 d’images | Chromium bogues »  
[CR1115011] : « Lors de la copie d’un tableau à partir de la console, la structure de la table n’est pas https://crbug.com/1115011 conservée | Chromium bogues »  
[CR1116085] : « Veuillez retourner l’inspecteur de https://crbug.com/1116085 propriétés DevTools | Chromium bogues »  

[CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData]: https://drafts.csswg.org/mediaqueries-5#descdef-media-prefers-reduced-data "prefers-reduced-data - Media Queries Level 5 | Brouillons de l’éditeur de groupe de travail CSS W3C"  

[GithubGooglechromeLighthouseV620]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.2.0 "v6.2.0 - GoogleChrome/| GitHub"  

[GoogleDevelopersProtocolBuffers]: https://developers.google.com/protocol-buffers "Mémoires tampons de protocole | Développeurs Google"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Galaxy Fold | Samsung États-Unis"  

[V8FeaturesLogicalAssignment]: https://v8.dev/features/logical-assignment "Affectation logique | V8"  
[V8FeaturesNumericSeparators]: https://v8.dev/features/numeric-separators "Séparateurs numériques | V8"  

[WebDevCoopCoep]: https://web.dev/coop-coep "Rendre votre site web \ « cross-origin isolated\ » à l’aide de LA TECHNOLOGIE | web.dev"  
[WebDevIdleDetection]: https://web.dev/idle-detection "Détecter les utilisateurs inactifs avec l’API de détection d’inactivité | web.dev"  
[WebDevNonCompositedAnimations]: https://web.dev/non-composited-animations "Évitez les animations non composites | web.dev"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developer.chrome.com/blog/new-in-devtools-86) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
