---
description: Faites correspondre les raccourcis clavier aux éléments Visual Studio, à l’émulation du pli en surface Duo et au Samsung Galaxy, ainsi qu’aux améliorations apportées aux grilles CSS
title: Nouveautés de DevTools (Microsoft Edge 86)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 0e759c18b5ef547bfd490f4d525930f92809a6a1
ms.sourcegitcommit: 6e2b26d41a0aa56ac34e6edc7dddd852ddb415b1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/23/2020
ms.locfileid: "11133910"
---
# Nouveautés de DevTools (Microsoft Edge 86)  

## Annonces de l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

### Faire correspondre des raccourcis clavier dans DevTools au code Visual Studio  

Dans Microsoft Edge 86, il est possible que les raccourcis clavier figurant dans le DevTools correspondent à vos raccourcis dans le [code Visual Studio][VisualStudioCode]. 

:::image type="complex" source="../../media/2020/08/keyboard-shortcut.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/keyboard-shortcut.msft.png":::
   Faire correspondre les raccourcis clavier du DevTools au code Visual Studio  
:::image-end:::  

Pour activer cette fonctionnalité, accédez à [personnaliser les raccourcis clavier dans Microsoft Edge devtools][DevtoolsCustomizeShortcuts].  

Par exemple, le raccourci clavier pour suspendre ou continuer à exécuter un script dans le [code Visual Studio][VisualStudioCodeShortcutsKeyboardWindows] est `F5` .  Avec la valeur prédéfinie **devtools (par défaut)** , le même raccourci dans devtools est `F8` , mais lorsque vous choisissez le **code prédéfini Visual Studio** , ce raccourci est désormais également disponible `F5` .  

[#174309][CR174309] problème de chrome  

### Emulation surface Duo et Samsung Galaxy Fold  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio":::
   Fonctionnalités expérimentales  
:::image-end:::  

Vous pouvez maintenant tester l’apparence de votre site Web ou de votre application sur deux nouveaux appareils:  [surface Duo][MicrosoftSurfaceDevicesDuo] et [Samsung Galaxy Fold][SamsungMobileGalaxyFold] dans Microsoft Edge.  

Pour vous aider à améliorer votre site Web ou votre application pour les appareils à double écran et pliant, utilisez les fonctionnalités suivantes lors de [l’émulation de l’appareil][DevtoolsDeviceModeIndex].  

*   [Fractionnées][DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices], c’est-à-dire lorsque votre site Web (ou l’application) s’affiche sur les deux écrans.
*   [Rendu de la couture][DualScreenIntroductionHowWorkSeam], qui est l’espace entre les deux écrans.
*   [Activation d’API de plateforme Web expérimentale][DevtoolsExperimentalFeaturesEnableExperimentalApis] pour accéder à la nouvelle [fonctionnalité d’affichage de contenu multimédia CSS][DualScreenWebCssMediaSpanning] et à l' [API getWindowSegments JavaScript][DualScreenWebJavascriptGetwindowsegments].  

:::image type="complex" source="../../media/2020/08/surface-duo-device-emulation.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/surface-duo-device-emulation.msft.png":::
   Émulation d’appareil pour le duo de surface  
:::image-end:::  

Pour activer cette fonctionnalité expérimentale, naviguez jusqu’à [activation des fonctionnalités expérimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] , puis cochez la case en regard de **émulation: prise en charge du mode double écran**.  

Pour plus d’informations sur cette expérience, accédez à [émulation: prise en charge du mode double écran][DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode].  

Problème de chrome: [#1054281][CR1054281]  

### Améliorations de la superposition de grille CSS et nouvelles fonctionnalités de grille expérimentale  

Nous vous remercions des commentaires positifs relatifs aux superpositions de grille CSS améliorées.  Les superpositions de grille CSS sont désormais activées par défaut et ne nécessitent pas d’activation d’une expérience.  

:::image type="complex" source="../../media/2020/08/css-grid-overlay-article.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/css-grid-overlay-article.msft.png":::
   Superposition de grille CSS pour un `article` élément  
:::image-end:::  

> [!NOTE]
> Pour plus d’informations sur les superpositions de grille, voir [fonctionnalités de débogage de grille CSS][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures].  

L’équipe Microsoft Edge DevTools et l’équipe chrome DevTools collaborent sur des fonctionnalités supplémentaires.  Les nouvelles fonctionnalités incluent plusieurs superpositions qui sont permanentes et configurables à partir d’un nouveau volet de **disposition** dans le panneau **éléments** .  

Pour activer cette fonctionnalité expérimentale, accédez à [activer les fonctionnalités expérimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] , puis activez la case à cocher en regard de **activer les nouvelles fonctionnalités de débogage de grille CSS (options de configuration disponibles dans le volet barre latérale des éléments après redémarrage)**.  

Pour plus d’informations sur cette expérience, accédez aux [nouvelles fonctionnalités de débogage de grille CSS][DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures].  

Problème de chrome: [#1047356][CR1047356]  

### Le tableau copié à partir de la console conserve la mise en forme  

Dans Microsoft Edge 85 ou version antérieure, la mise en forme d’un copié `console.table` a été perdue.  Si vous avez copié la sortie de l’API de la console [table][DevtoolsConsoleApiTable] et collé celle-ci, seul le texte du tableau a été conservé.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/console-table-beta.msft.png":::
         `table` Sortie de l’API de console dans Microsoft Edge 85 ou version antérieure  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png":::
         `table` Sortie de l’API de console de Microsoft Edge 85 ou antérieure collée dans le code Visual Studio  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Dans Microsoft Edge 86 ou version ultérieure, lorsque vous copiez une table à partir de la **console**, la mise en forme est désormais préservée.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/console-table-canary.msft.png":::
         `table` Sortie de l’API de console dans Microsoft Edge 86 ou version ultérieure  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png":::
         `table` Sortie de l’API de console de Microsoft Edge 86 ou version ultérieure collée dans le code Visual Studio  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Problème de chrome: [#1115011] [CR1115011]  

### Visionneuse de commandes sources pour faciliter les tests d’accessibilité  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio":::
   Fonctionnalités expérimentales  
:::image-end:::  

Le nouveau programme d’assistance d’accessibilité affiche l’ordre des éléments dans la source.  

:::image type="complex" source="../../media/2020/08/source-order-viewer.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/source-order-viewer.msft.png":::
   Activer l' **ordre d’affichage des sources**  
:::image-end:::  

Cette fonctionnalité permet de tester plus facilement la façon dont les utilisateurs du lecteur d’écran et du clavier connaissent votre site Web ou votre application.  Les lecteurs d’écran et la navigation au clavier dépendent du contenu placé dans un ordre particulier dans le code source de votre site Web ou de votre application, de manière à ce qu’il corresponde à la page rendue.  La visionneuse de commandes source affiche des différences potentielles dans l’ordre entre la page affichée et le code source.  

Pour activer cette fonctionnalité expérimentale, accédez à l’option Activer les [fonctionnalités expérimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] , puis activez la case à cocher en regard de **activer la visionneuse de commandes sources**.  

Pour plus d’informations sur cette expérience, naviguez jusqu’à [activer la visionneuse de commandes sources][DevtoolsExperimentalFeaturesEnableSourceOrderViewer].  

Problème de chrome: [#1094406][CR1094406]  

<!--
### DevTools language enhancements  

Your feedback and internal discoveries uncovered which text strings used in the Microsoft Edge feedback should remain untranslated or create confusion when translated.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-stable.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="localization-improvements-chinese-complex-stable.msft.png":::
         Microsoft Edge DevTools 85 and earlier in Traditional Chinese  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png":::
         Microsoft Edge DevTools 86  or later in Traditional Chinese  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.  

The current effort to improve translation quality enables easier support for more languages in the future.  
-->  

### Sélectionner tous les résultats de recherche dans l’outil éléments  

Dans Microsoft Edge 84 et 85, le premier résultat de recherche dans le panneau **éléments** n’a pas été mis en surbrillance.  Les résultats de recherche restants ont été correctement mis en surbrillance.  

Nous vous remercions d’avoir envoyé vos commentaires et de nous aider à améliorer le chrome.  Votre commentaire n’a pas été détecté [#1103316][CR1103316] dans le projet de chrome Open-source.  

:::image type="complex" source="../../media/2020/08/elements- search-highlight-fixed.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/elements- search-highlight-fixed.msft.png":::
   Premiers résultats de recherche du panneau **éléments** dans Microsoft Edge 84 ou version ultérieure  
:::image-end:::  

Le problème est désormais résolu dans toutes les versions de Microsoft Edge.  

Problème de chrome: [#1103316][CR1103316]  

## Annonces du projet de chrome  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Nouvelle fenêtre multimédia  

DevTools affiche désormais les informations sur les lecteurs multimédias dans le panneau [média][DevtoolsMediaPanelIndex] .  

Pour ouvrir le nouveau panneau **multimédia** , exécutez l’étape suivante.  

1.  Sélectionnez **personnaliser et contrôler devtools** \ ( `...` \) > **plus d’outils**  >  **multimédia**.  
    
    :::image type="complex" source="../../media/2020/08/media-panel.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/media-panel.msft.png":::
       Nouvelle fenêtre **multimédia**  
    :::image-end:::  

Avant le nouveau panneau **multimédia** dans devtools, les informations de journalisation et de débogage relatives aux lecteurs vidéo se trouvent sous le paramètre **lecteurs récents** .  Pour ouvrir le paramètre **lecteurs récents** , accédez à `edge://media-internals` l’onglet **adversaires** et sélectionnez l’onglet adversaires.  

Affichez le contenu en direct et examinez les problèmes potentiels plus rapidement, en incluant les exemples suivants.  

*   Pourquoi les images sont-elles supprimées?  
*   Pourquoi JavaScript interagit-il avec le joueur d’une manière inattendue?  

### Capture d’écran de nœud à l’aide du menu contextuel du panneau éléments  

Vous pouvez désormais capturer les captures d’écran de nœud à l’aide du menu contextuel dans le panneau **éléments** .  

Par exemple, pour prendre une capture d’écran de la table des matières, pointez sur l’élément, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez **capturer le nœud de capture**.  

:::image type="complex" source="../../media/2020/08/capture-node-screenshot.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/capture-node-screenshot.msft.png":::
   Capture d’écran de nœuds  
:::image-end:::  

Problème de chrome: [#1100253][CR1100253]  

### Mises à jour de l’outil de sortie  

La barre d’avertissement problèmes du panneau de la **console** est désormais remplacée par un message normal.  

<!--todo: this figure need to be updated  -->  

:::image type="complex" source="../../media/2020/08/issue-console-msg.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/issue-console-msg.msft.png":::
   Problèmes dans le message de la console  
:::image-end:::  

Les problèmes de cookie tiers sont désormais cachés par défaut dans l’outil **problèmes** .  Activez la nouvelle case à cocher **inclure les problèmes de cookie tiers** pour afficher les problèmes.  

:::image type="complex" source="../../media/2020/08/third-party-cookies.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/third-party-cookies.msft.png":::
   case à cocher problèmes de cookie tiers  
:::image-end:::  

Problèmes de chrome: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]  

### Émuler des polices locales manquantes  

Ouvrez l' [outil de rendu][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] et utilisez la nouvelle fonctionnalité **Désactiver les polices locales** pour émuler les sources manquantes `local()` dans les `@font-face` règles.  

Par exemple, lorsque la `Rubik` police est installée sur votre appareil et qu' `@font-face src` elle l’utilise comme `local()` police, Microsoft Edge utilise le fichier de police local de votre appareil.  

Lorsque l’option **Désactiver les polices locales** est activée, devtools ignore les `local()` polices et récupère chacune du réseau.  

:::image type="complex" source="../../media/2020/08/disable-font.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/disable-font.msft.png":::
   Émuler des polices locales manquantes  
:::image-end:::  

Si vous utilisez deux copies différentes de la même police lors du développement, comme dans les exemples suivants.  

*   Police locale pour vos outils de conception.  
*   Une police Web pour votre code.  

Utilisez **Désactiver les polices locales** pour faciliter l’accomplissement des tâches suivantes.  

*   Déboguer et mesurer les performances de chargement et l’optimisation des polices Web.  
*   Vérifiez la précision de vos `@font-face` règles CSS.  
*   Découvrez les différences entre les versions locales installées sur votre appareil et une police Web.  

Problème de chrome: [#384968][CR384968]  

### Émuler des utilisateurs inactifs  

L' [API de détection de veille][WebDevIdleDetection] permet aux développeurs de détecter les utilisateurs inactifs et de réagir aux changements d’État inactifs.  Vous pouvez maintenant utiliser DevTools pour émuler les changements d’état inactif dans l’outil **capteurs** pour l’état de l’utilisateur et l’état de l’écran, au lieu d’attendre que l’état d’inactivité réelle change.  Vous pouvez ouvrir l’outil **capteurs** à partir du [tiroir][DevtoolsCustomizeIndexDrawer].  

:::image type="complex" source="../../media/2020/08/emulate-idle.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/emulate-idle.msft.png":::
   Émuler des utilisateurs inactifs  
:::image-end:::  

Problème de chrome: [#1090802][CR1090802]  

### Imitez les préférences-Reduced-Data  

> [!NOTE]
> Dans le 86 de Microsoft Edge, pour activer cette fonctionnalité, accédez à `edge://flags#enable-experimental-web-platform-features` l’indicateur **features sur les fonctionnalités de plateforme Web expérimentale** et activez-le.  L’option d’émulation est uniquement affichée si l’indicateur est activé.  

La requête Media [-Reduced-Data][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] détecte les préférences de contenu utilisateur pour réduire les données.  Si cette option est sélectionnée, l’utilisateur reçoit du contenu de page alternatif qui utilise moins de données.  

Vous pouvez maintenant utiliser DevTools pour émuler la `prefers-reduced-data` requête multimédia.  

:::image type="complex" source="../../media/2020/08/emulate-prefers-reduced-data.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/emulate-prefers-reduced-data.msft.png":::
   Imitez les préférences-Reduced-Data  
:::image-end:::  

Problème de chrome: [#1096068][CR1096068]  

### Prise en charge des nouvelles fonctionnalités JavaScript  

DevTools ont désormais une meilleure prise en charge des fonctionnalités de langage JavaScript suivantes.  

| Fonctionnalité de langage JavaScript | Détails |  
|:--- |:--- |  
| [Opérateurs d’affectation logique][V8FeaturesLogicalAssignment] | DevTools prend désormais en charge l’affectation logique avec les opérateurs nouveau et `&&=` `||=` et `??=` dans les panneaux **console** et **sources** .  |  
| [Séparateur numérique][V8FeaturesNumericSeparators] à imprimer | DevTools est désormais correctement à l’impression des séparateurs numériques dans le panneau **sources** .  |  

Problèmes de chrome: [1086817][CR1086817], [1080569][CR1080569]  

### Panneau de signalisation 6,2  

Le panneau de signalisation est désormais exécuté sur le panneau de **signalisation** 6,2.  Pour obtenir la liste complète des modifications, accédez aux [notes de publication][GithubGooglechromeLighthouseV620]de votre phare.  

Problème de chrome: [#772558][CR772558]  

### Dépréciation du Listing Other origines dans le volet travailleurs de services  

DevTools propose désormais un lien dans le volet **travailleurs de services** \ (panneau d'**application** > volet des travailleurs de **service** ) pour afficher la liste complète des travailleurs de services d’autres origines.  Pour accéder à la liste sans ouvrir le DevTools, accédez à `edge://service-worker-internals/?devtools` .  

Auparavant DevTools afficher une liste imbriquée dans le volet de l' **Application** > volet **travailleurs du service** .  

:::image type="complex" source="../../media/2020/08/sw-other-origins.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/sw-other-origins.msft.png":::
   Créer un lien vers d’autres origines  
:::image-end:::  

Problème de chrome: [#807440][CR807440]  

### Afficher le résumé de couverture des éléments filtrés  

DevTools désormais recalculer et afficher une synthèse dynamique des informations de couverture.  L’affichage dynamique est déclenché lorsque des filtres sont appliqués dans l’outil de [couverture][DevtoolsCoverageIndex] .  Pour que l’outil de **couverture** affiche toujours un résumé de toutes les informations de couverture.  

Dans la première des illustrations suivantes, le résumé s’affiche initialement `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` et dans les deux figures suivantes, le résumé s’affiche `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` lorsque le filtrage CSS est appliqué.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/coverage-compare.msft.png":::
         Résumé de couverture  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare-css-filter.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/coverage-compare-css-filter.msft.png":::
         Résumé de couverture des éléments filtrés  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Problème de chrome: [#1061385][CR1090802]  

### Nouvelle vue Détails du cadre dans le panneau application  

DevTools affiche désormais une vue détaillée pour chaque image.  Pour y accéder, sélectionnez un cadre sous le menu **cadres** dans le volet de l' **application** .  

:::image type="complex" source="../../media/2020/08/frame-details.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/frame-details.msft.png":::
   Nouvelle vue détaillée d’une image dans le panneau **application**  
:::image-end:::  

Problème de chrome: [#1093247][CR1093247]  

#### Détails du cadre pour les fenêtres ouvertes  

Les fenêtres et fenêtres contextuelles ouvertes s’affichent désormais sous l’arborescence de trames.  Le mode d’affichage détaillé des fenêtres ouvertes inclut des informations supplémentaires sur la sécurité.  

:::image type="complex" source="../../media/2020/08/window-opener.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/window-opener.msft.png":::
   Nouvelle vue détaillée du cadre pour les fenêtres ouvertes  
:::image-end:::  

Problème de chrome: [#1107766] [CR1107766]  

#### Informations de sécurité et d’isolement  

Context sécurisée, [Cross-Origin-Integration-Policy (COEP)][WebDevCoopCoep]et [Cross-Origin-Open-Policy (Coop)][WebDevCoopCoep] s’affichent désormais dans les détails de trame.  

:::image type="complex" source="../../media/2020/08/coep-coop.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/coep-coop.msft.png":::
   Informations de sécurité et d’isolement  
:::image-end:::  

À l’avenir, l’équipe Microsoft Edge DevTools et l’équipe chrome DevTools sont en voie d’ajouter des informations de sécurité aux détails de trames.  

Problème de chrome: [#1051466][CR1051466]  

### Éléments et mises à jour du panneau réseau  

#### Suggestions de couleurs accessibles dans le volet styles  

DevTools propose désormais des suggestions de couleurs pour le texte de faible contraste de couleurs.  

Dans l’exemple ci-dessous, vous `h1` avez du texte à contraste élevé.  Pour résoudre ce problème, ouvrez le sélecteur de couleurs de la `color` propriété dans le volet **styles** .  Une fois que vous avez développé la section **coefficient de contraste** , devtools fournit des suggestions couleur AA et AAA.  Pour appliquer la couleur, sélectionnez la couleur suggérée.  

:::image type="complex" source="../../media/2020/08/contrast-color-suggestion.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/contrast-color-suggestion.msft.png":::
   Le sélecteur de couleurs suggère des suggestions couleur AA et AAA  
:::image-end:::  

Problème de chrome: [#1093227][CR1093227]  

#### Volet de rétablissement des propriétés dans le panneau éléments  

Le volet **Propriétés** est en retour.  Elle a été [déconseillée dans Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].  L’équipe Microsoft Edge DevTools et l’équipe DevTools chrome présentent des améliorations en matière d’examen des propriétés des éléments.  

:::image type="complex" source="../../media/2020/08/properties-pane.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/properties-pane.msft.png":::
   Volet **Propriétés** dans le panneau **éléments**  
:::image-end:::  

Problème de chrome:  <!--  [#1105205][CR1105205],  -->  [#1116085] [CR1116085]  

<!--  
#### Human-readable X-Client-Data header values in the Network panel  

When inspecting a network resource in the Network panel, DevTools now formats any `X-Client-Data` header values in **Headers** pane as code.  

The `X-Client-Data` HTTP header contains a list of experiment IDs and Microsoft Edge flags that are enabled in your browser.  The raw header values look like opaque strings since the values are `base-64-encoded`, serialized [protocol buffers][GoogleDevelopersProtocolBuffers].  To make the contents more transparent to developers, DevTools now shows the decoded values.  

:::image type="complex" source="../../media/2020/08/x-client-data.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/x-client-data.msft.png":::
   Human-readable `X-Client-Data` header values  
:::image-end:::  

Chromium issue: [#1103854][CR1103854]  
-->  

#### Saisie semi-automatique de polices personnalisées dans le volet styles  

Les polices importées sont désormais ajoutées à la liste de la saisie semi-automatique CSS lors de la modification `font-family` de la propriété dans le volet **styles** .  

Par exemple, si `monospace` vous disposez d’une police personnalisée installée sur l’ordinateur local, celle-ci apparaît dans la liste de saisie semi-automatique CSS. Dans les versions précédentes de Microsoft Edge, la police n’est pas affichée.

:::image type="complex" source="../../media/2020/08/font-auto-complete.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/font-auto-complete.msft.png":::
   Saisie semi-automatique de polices personnalisées  
:::image-end:::  

Problème de chrome: [#1106221] [CR1106221]  

#### Affichage cohérent du type de ressource dans le panneau réseau  

DevTools affichent désormais systématiquement le même type de ressource que la requête réseau d’origine et est ajouté `/ Redirect` à la valeur de la colonne **type** lorsque la redirection \ (code d’État http 302 \) se produit.  

Auparavant DevTools modifié ce type sur `Other` parfois.  

:::image type="complex" source="../../media/2020/08/network-redirect.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/network-redirect.msft.png":::
   Afficher le type de ressource rediriger  
:::image-end:::  

Problème de chrome: [#997694][CR997694]  

#### Boutons clairs dans les panneaux éléments et réseau  

Les zones de texte suivantes disposent désormais de boutons **clairs** .  

*   Les zones de texte de filtre dans le volet **styles** et le panneau **réseau** .  
*   Zone de texte de recherche DOM dans le panneau **éléments** .  

Cliquez sur le bouton **Effacer** pour supprimer du texte entré.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-elements.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/clear-button-elements.msft.png":::
         Boutons effacer dans les panneaux d' **éléments**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-network.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="../../media/2020/08/clear-button-network.msft.png":::
         Boutons effacer dans les panneaux **réseau**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Problème de chrome: [#1067184][CR1067184]  

## Télécharger les canaux Microsoft Edge preview  

Si vous utilisez Windows ou macOS, envisagez d’utiliser les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] comme navigateur par défaut.  Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.  

## Contacter l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png "Icône Paramètres de DevTools"  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-panel "Désapprobation du volet Propriétés dans le panneau éléments nouveautés de DevTools (Microsoft Edge 84) | Documents Microsoft"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Fonctionnalités de débogage de grille CSS-nouveautés dans DevTools (Microsoft Edge 85) | Documents Microsoft"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Émuler des appareils mobiles dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personnaliser les raccourcis clavier dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Activer les API expérimentales-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Émulation: prise en charge du mode double affichage-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Activer la visionneuse de commandes sources-fonctionnalités expérimentales | Documents Microsoft"
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: https://review.docs.microsoft.com/microsoft-edge/devtools-guide-chromium/experimental-features?branch=user/zoghadya/dual-screen-experiment#emulation-support-dual-screen-mode "Émulation: prise en charge du mode double affichage-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Tests sur les périphériques pliants et à deux écrans-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Activer les fonctionnalités expérimentales-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "référence sur les API table-console | Documents Microsoft"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Recherchez du code JavaScript et CSS inutilisé avec l’onglet couverture dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Tiroir-personnaliser Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analyser les performances de rendu à l’aide de l’onglet rendu-référence d’analyse des performances | Documents Microsoft"  
[DevtoolsMediaPanelIndex]: /microsoft-edge/devtools-guide-chromium/media-panel/index "Afficher et déboguer les informations sur les lecteurs multimédias | Documents Microsoft"  

[DualScreenIntroductionHowWorkSeam]:  /dual-screen/introduction#how-to-work-with-the-seam "Comment utiliser la couture-Introduction aux périphériques à écran double Documents Microsoft"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Fonctionnalité de répartition d’écran de média CSS pour la détection sur deux écrans | Documents Microsoft"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "API JavaScript getWindowSegments pour les appareils à deux écrans | Documents Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux Microsoft Edge preview"  

[VisualStudioCode]: https://code.visualstudio.com "Code Visual Studio "  
[VisualStudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Raccourcis clavier dans Visual Studio code pour Windows"  

[MicrosoftSurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Nouvelle surface Duo"  

[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools compte Twitter"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bugs du chrome"  

[CR174309]: https://crbug.com/174309 "DevTools: autoriser pour personnaliser les raccourcis clavier/les combinaisons de touches | Bugs du chrome"
[CR384968]: https://crbug.com/384968 "Option permettant d’ignorer les polices locales () | Bugs du chrome"  
[CR772558]: https://crbug.com/772558 "DevTools: mise à jour vers la dernière version de phare | Bugs du chrome"  
[CR807440]: https://crbug.com/807440 "Blocage de chrome avec un grand nombre de SWs | Bugs du chrome"  
[CR997694]: https://crbug.com/997694 "Les requêtes XHR avec le statut 302 ne sont pas affichées sous le filtre \ «XHR \» dans le panneau réseau | Bugs du chrome"  
[CR1047356]: https://crbug.com/1047356 "Outils CSS Grid/Flexbox/tableau | Bugs du chrome"  
[CR1051466]: https://crbug.com/1051466 "Prendre en charge le débogage COOP/COEP dans DevTools | Bugs du chrome"  
[CR1054281]: https://crbug.com/1054281 "Demande de fonctionnalité: DevTools doit émuler les périphériques pliants et à deux écrans | Bugs du chrome"  
[CR1067184]: https://crbug.com/1067184 "Demande de fonctionnalité: bouton Effacer le filtre sur réseau & les éléments-> entrées de filtre de style Bugs du chrome"  
[CR1068116]: https://crbug.com/1068116 "☂ Le panneau problèmes d’expédition | Bugs du chrome"  
[CR1080569]: https://crbug.com/1080569 "Acorn ne prend pas en charge les opérateurs d’affectation logiques | Bugs du chrome"  
[CR1080589]: https://crbug.com/1080589 "Classifier les problèmes par tiers/tierce partie | Bugs du chrome"  
[CR1086817]: https://crbug.com/1086817 "Acorn ne prend pas en charge les séparateurs numériques | Bugs du chrome"  
[CR1090802]: https://crbug.com/1090802 "Simuler les changements d’état d’inactivité de l’API de détection d’inactivité | Bugs du chrome"  
[CR1093227]: https://crbug.com/1093227 "DevTools: suggérer une couleur d’accessibilité plus proche | Bugs du chrome"  
[CR1093247]: https://crbug.com/1093247 "Afficher des informations sur les trames dans le panneau application | Bugs du chrome"  
[CR1094406]: https://crbug.com/1094406 "Les développeurs doivent utiliser une visionneuse de commandes sources au https://webwewant.fyi/wants/64/"  
[CR1096068]: https://crbug.com/1096068 "DevTools: prise en charge de l’émulation de la fonctionnalité de média-Reduced-Data. Bugs du chrome"  
[CR1096481]: https://crbug.com/1096481 "Positionnement des bannières de problèmes | Bugs du chrome"  
[CR1100253]: https://crbug.com/1100253 "Raccourci du nœud ajouter une capture d’écran dans le menu contextuel de l’élément | Bugs du chrome"  
[CR1103316]: https://crbug.com/1103316 "La recherche d’éléments n’resolveNode (texte en surbrillance, etc.) sur le premier résultat de la recherche | Bugs du chrome"  
[CR1103854]: https://crbug.com/1103854 "Dé-brouiller X-client-valeurs de données dans les outils de développement | Bugs du chrome"  
<!--  [CR1105205]: https://crbug.com/1105205 "Issue 1105205 | Chromium bugs"  -->  
[CR1106221]: https://crbug.com/1106221 "Ajoutez des polices importées à la saisie semi-automatique de la famille de polices dans le panneau Styles | Bugs du chrome  
[CR1107766]: https://crbug.com/1107766 "afficher des informations sur les trames générées par’Window. Open () 'dans l’arborescence Bugs du chrome  
[CR1115011]: https://crbug.com/1115011 "lors de la copie d’une table à partir de la console la structure de la table n’est pas conservée | Bugs du chrome  
[CR1116085]: https://crbug.com/1116085 "Retournez l’inspecteur Propriétés devtools | Bugs du chrome  

[CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData]: https://drafts.csswg.org/mediaqueries-5#descdef-media-prefers-reduced-data "préfère-Reduce-des requêtes de données multimédia niveau 5 | Brouillons de l’éditeur de groupe de travail CSS W3C"  

[GithubGooglechromeLighthouseV620]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.2.0 "v 6.2.0-GoogleChrome/phare | GitHub"  

[GoogleDevelopersProtocolBuffers]: https://developers.google.com/protocol-buffers "Mémoires tampons de protocole | Développeurs Google"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Pli Galaxy | Samsung US"  

[V8FeaturesLogicalAssignment]: https://v8.dev/features/logical-assignment "Attribution logique | V8"  
[V8FeaturesNumericSeparators]: https://v8.dev/features/numeric-separators "Séparateurs numériques | V8"  

[WebDevCoopCoep]: https://web.dev/coop-coep "Faire de votre site Web «Cross-Origin isolated» à l’aide de COOP et COEP | Web. dev"  
[WebDevIdleDetection]: https://web.dev/idle-detection "Détecter les utilisateurs inactifs à l’aide de l’API de détection d’activité Web. dev"  
[WebDevNonCompositedAnimations]: https://web.dev/non-composited-animations "Évitez les animations non composites | Web. dev"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/updates/2020/08/devtools/index) et est créée par [Jecelyn Yeen][JecelynYeen] \ (développeurs, chrome devtools \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
