---
description: Nouveaux outils de débogage de grille CSS, outil webauthn, outils mobiles et volet barre latérale calculée.
title: Nouveautés de DevTools (Microsoft Edge 87)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: b972468ad21f3a64985a00aecbe29836032b3334
ms.sourcegitcommit: 080759f68a0a158f10dc20d20c14e222ace1be84
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "11190004"
---
# Nouveautés de DevTools (Microsoft Edge 87)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## Amélioration de la localisation DevTools  

Pour répondre à vos besoins en matière de traduction, l’équipe Microsoft Edge DevTools est axée sur l’amélioration de la qualité de la traduction.  À partir de la version 87 de Microsoft Edge, plusieurs chaînes et termes sont verrouillés et ne changent pas même lorsque le reste du DevTools est affiché dans d’autres langues.  La liste des chaînes et termes concernés est la suivante.  

*   Les chaînes dans l’outil **phare** .  
*   Le terme `service worker` .  
*   Certains filtres d’outils **réseau** tels que `URL` ,, `XHR` `JS` et `CSS` .  
*   API de la console [$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] .  
    
[$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] est désormais disponible dans la [console](/microsoft-edge/devtools-guide-chromium/console/index.md) pour les utilisateurs des versions localisées du devtools.   Nous vous remercions de la communauté globale des développeurs pour vous aider à améliorer la localisation de Microsoft Edge DevTools.  Continuez à [Envoyer des commentaires sur la qualité](#getting-in-touch-with-microsoft-edge-devtools-team) de la localisation pour améliorer la prise en charge de devtools dans tous les pays.  Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à l' [#1136655][CR1136655]du problème.  

:::image type="complex" source="../../media/2020/10/bing-network-japanese.msft.png" alt-text="Outil réseau avec filtres non localisés" lightbox="../../media/2020/10/bing-network-japanese.msft.png":::
   Volet **réseau** avec des filtres non localisés  
:::image-end:::  

## Déplacer des outils entre les volets supérieur et inférieur  

DevTools prend désormais en charge le déplacement d’outils entre les volets supérieur et inférieur.  Personnalisez votre DevTools et améliorez votre productivité en affichant n’importe quelle combinaison de deux outils en même temps.  Par exemple, vous pouvez afficher les **éléments** et les outils **sources** en même temps (en déplaçant l’outil **sources** vers le bas).  Pour passer en revue l’historique de cette fonctionnalité dans le projet open-source de chrome, accédez à [#1075732][CR1075732]problème.  

:::row:::
   :::column span="":::
      Pour déplacer un outil du haut vers le bas, pointez sur un onglet, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez **déplacer vers le bas**.  
      
      :::image type="complex" source="../../media/2020/10/move-to-bottom.msft.png" alt-text="Déplacer vers le bas" lightbox="../../media/2020/10/move-to-bottom.msft.png":::
         Déplacer vers le bas  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Pour déplacer n’importe quel outil inférieur vers le haut, pointez sur un onglet, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez **déplacer vers le haut**.  
      
      :::image type="complex" source="../../media/2020/10/move-to-top.msft.png" alt-text="Déplacer vers le haut" lightbox="../../media/2020/10/move-to-top.msft.png":::
         Déplacer vers le haut  
      :::image-end:::  
   :::column-end:::
:::row-end:::

## Enregistrer et exporter à l’aide de la console réseau  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalités expérimentales":::
   Fonctionnalités expérimentales  
:::image-end:::  

L’outil de la **console réseau** dispose désormais d’une compatibilité améliorée avec les schémas [post-v 2.1][PostmanSchemaJsonCollectionv210Index] et [openapi v2][SwaggerSpecificationV2] .  Pour activer l’expérience, naviguez jusqu’à [activation des fonctionnalités expérimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] , puis cochez la case en regard de **activer la console réseau**.  Pour plus d’informations sur la **console réseau**, voir [activer la fonctionnalité expérimentive Network console][DevtoolsExperimentalFeaturesEnableNetworkConsole].  Cette expérience prend désormais en charge les actions suivantes.  

*   Enregistrer et exporter des collections et des environnements;  
*   Edit et export d’ensembles de variables d’environnement dans l’outil **Network console** .  
    
Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à l' [#1093687][CR1093687]du problème.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-name.msft.png" alt-text="Entrez le nom du nouvel environnement" lightbox="../../media/2020/10/network-console-environments-new-name.msft.png":::
         Entrez le nom du nouvel environnement  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-format.msft.png" alt-text="Choisir la mise en forme pour le nouvel environnement" lightbox="../../media/2020/10/network-console-environments-new-format.msft.png":::
         Choisir la mise en forme pour le nouvel environnement  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Outils de grille CSS améliorés  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalités expérimentales":::
   Fonctionnalités expérimentales  
:::image-end:::  

Microsoft Edge DevTools prend désormais en charge les fonctionnalités suivantes pour inspecter, afficher et déboguer vos grilles CSS.  

*   Affichez une superposition de grille simplifiée à l’aide de l’outil **Inspect** ou obtenez des informations plus détaillées avec des superpositions persistantes.  
*   Pour activer les superpositions de grille persistante, sélectionnez l’icône de grille en regard d’un élément de conteneur de grille dans l’outil **éléments** ou sélectionnez la grille dans l’outil de **disposition** .  
*   Vous pouvez activer les superpositions persistantes pour plusieurs grilles.  
*   Le nouvel outil **mise en page** vous permet d’activer ou de désactiver facilement les superpositions de grille et de configurer son apparence et son contenu.  
    
Les fonctionnalités sont activées par défaut.  Pour plus d’informations sur les fonctionnalités, accédez à [grilles CSS][DevtoolsCssGrid].  Pour passer en revue l’historique de cette fonctionnalité dans le projet open-source de chrome, accédez à [#1047356][CR1047356]problème.  Par ailleurs, l’équipe Microsoft Edge DevTools collabore avec la communauté de l’équipe chrome DevTools et la communauté de chrome pour ajouter de nouvelles fonctionnalités d’outils Flexbox à DevTools.  Pour les mises à jour apportées à l’outil Flexbox dans le projet open-source de chrome, accédez à [#1136394][CR1136394]problème.  

:::image type="complex" source="../../media/2020/10/grid-layout-pane.msft.png" alt-text="Outil disposition avec des grilles" lightbox="../../media/2020/10/grid-layout-pane.msft.png":::
   Outil **disposition** avec des grilles  
:::image-end:::  

## Personnaliser les raccourcis clavier dans les paramètres  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalités expérimentales":::
   Fonctionnalités expérimentales  
:::image-end:::  

Vous pouvez désormais personnaliser le raccourci clavier pour n’importe quelle action dans le DevTools.  Depuis la version 84 de Microsoft Edge, vous pouvez choisir entre les prédéfinis de **code Visual Studio** et **devtools (par défaut)** pour les [raccourcis clavier][DevtoolsCustomizeShortcuts].  À partir de la version 87 de Microsoft Edge, vous pouvez activer l’expérience d’activation de l' **éditeur de raccourcis** clavier pour personnaliser davantage les [raccourcis clavier][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].  

Pour activer l’expérience, naviguez jusqu’à [activation des fonctionnalités expérimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] , puis activez la case à cocher en regard de **activer l’éditeur de raccourcis clavier**.  Pour plus d’informations sur la personnalisation et la modification des raccourcis, accédez à [activer la fonctionnalité expérience de l’éditeur de raccourcis clavier][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].  Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à l' [#174309][CR174309]du problème.  

:::image type="complex" source="../../media/2020/10/custom-shortcut-pause-script.msft.png" alt-text="Raccourci personnalisé pour suspendre un script" lightbox="../../media/2020/10/custom-shortcut-pause-script.msft.png":::
   Raccourci personnalisé pour suspendre un script  
:::image-end:::  

## Présentation de l’extension de code Microsoft Edge Tools pour Visual Studio  

Les éléments du code et du réseau **Visual Studio** pour les extensions **de code Visual Studio** sont désormais fusionnés dans le nouvel [outil de développement Microsoft Edge pour l’extension de code Visual Studio][VisualStudioCodeMarketplaceMsEdgedevtools] .  Utilisez Microsoft Edge DevTools pour les activités suivantes sans quitter le code Visual Studio.  

*   Déboguer le DOM  
*   Modifier CSS  
*   Inspecter le trafic réseau  

Avec l’extension, lancez Microsoft Edge, connectez-vous à une instance existante du navigateur, ou utilisez un navigateur headless directement de votre éditeur.  Pour vous familiariser avec les commentaires concernant cette extension, accédez au [Microsoft Edge développeurs Tools pour Visual Studio code][GithubMicrosoftVscodeEdgeDevtools] référentiel Samples sur GitHub.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png" alt-text="Utilisation de l’extension dans la capture d’écran du mode navigateur complet" lightbox="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png":::
         Utilisation de l’extension dans la capture d’écran du mode navigateur complet  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-headless.msft.png" alt-text="Utilisation de l’extension dans la capture d’écran du mode headless" lightbox="../../media/2020/10/microsoft-edge-tools-headless.msft.png":::
         Utilisation de l’extension dans la capture d’écran du mode headless  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Annonces du projet de chrome  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Nouvel outil webauthn  

Dans les versions antérieures de Microsoft Edge, il n’y a pas de prise en charge du débogage de webauthn natif.  Vous avez besoin d’authentificateurs physiques pour tester votre application Web à l’aide de l' [API d’authentification Web][GithubW3cWebauthn].  Grâce au nouvel outil **Webauthn** , vous pouvez effectuer les actions suivantes sans utiliser d’authentificateurs physiques.

*   Émuler des authentificateurs
*   Personnaliser les attributs des authentificateurs
*   Inspecter les États des authentificateurs
    
Pour plus d’informations sur la fonctionnalité **Webauthn** , accédez à [émuler les authentificateurs et déboguer webauthn dans Microsoft Edge devtools][DevtoolsWebauthnIndex].  

Vous pouvez émuler les authentificateurs et déboguer l' [API d’authentification Web][GithubW3cWebauthn] avec le nouvel outil [webauthn][DevtoolsWebauthnIndex] .  Pour ouvrir l’outil **webauthn** , sélectionnez **l’icône personnaliser et contrôler devtools** \ ( `...` \) > **plus d’outils**  >  **webauth**.  Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à l' [#1034663][CR1034663]du problème.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/more-tools-webauthn.msft.png" alt-text="Ouvrir l’outil webauthn" lightbox="../../media/2020/10/more-tools-webauthn.msft.png":::
         Ouvrir l’outil **Webauthn**  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/webauthn-enable-virtual-auth.msft.png" alt-text="Outil webauthn" lightbox="../../media/2020/10/webauthn-enable-virtual-auth.msft.png":::
         Outil **Webauthn**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### Mises à jour de l’outil d’éléments  

#### Afficher le volet de barre latérale calculé dans le volet styles  

Activer/désactiver le volet **calculé** dans le volet **styles**  Le volet **calculé** dans le volet **styles** est réduit par défaut.  Pour le faire basculer, cliquez sur le bouton.  Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à l' [#1073899][CR1073899]du problème.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane.msft.png" alt-text="Ouvrir le volet de barre latérale calculée" lightbox="../../media/2020/10/computed-sidebar-pane.msft.png":::
         Ouvrir le volet de **barre latérale calculée**  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane-open.msft.png" alt-text="Volet barre latérale calculée" lightbox="../../media/2020/10/computed-sidebar-pane-open.msft.png":::
         Volet **barre latérale calculée**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### Regroupement des propriétés CSS dans le panneau calculé  

Pour afficher une feuille de style CSS appliquée moins de défilement, regrouper les propriétés CSS par catégories dans le volet **calculé** .  Vous pouvez également vous concentrer sur un ensemble de propriétés associées lorsque vous examinez votre CSS.  Dans l’outil **éléments** , sélectionnez un élément.  Pour regrouper \ (ou dissocier \) les propriétés CSS, activez la case à cocher du **groupe** .  Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à problèmes [#1096230][CR1096230], [#1084673][CR1084673]et [#1106251][CR1106251].  

:::image type="complex" source="../../media/2020/10/grouping-css-prop.msft.png" alt-text="Regroupement des propriétés CSS" lightbox="../../media/2020/10/grouping-css-prop.msft.png":::
   Regroupement des propriétés CSS  
:::image-end:::  

### Phare 6,4 dans l’outil phare  

L’outil **phare** s’exécute maintenant sur le phare 6,4.  Pour obtenir la liste complète des modifications, accédez aux [notes de publication de phare][GithubGoogleChromeLighthouseReleasesV641].  Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à l' [#772558][CR772558]du problème.  

### performance. Mark () événements dans la section minutage  

La **section minutage** d’un enregistrement dans l’outil de [performance][DevtoolsGuideChromiumEvaluatePerformanceReference] marque désormais des `performance.mark()` événements.  Pour utiliser cette fonctionnalité et mesurer les performances de votre code JavaScript, ajoutez des `performance.mark()` événements à votre code.  Par exemple, l’extrait de code suivant ajoute des marqueurs avant et après une `for` boucle qui itère de 0 à 1000 à l’aide d’incréments de 7.  

```javascript
performance.mark('start');
for (var i = 0; i < 1000; i+=7;){
  console.log(i);
}
performance.mark('end');
```  

Ensuite, ouvrez l’outil [performance][DevtoolsGuideChromiumEvaluatePerformanceReference] et naviguez jusqu’à la **section minutage** pour enregistrer votre code JavaScript.  Les `performance.mark()` événements que vous avez ajoutés apparaissent désormais dans l’enregistrement.  

:::image type="complex" source="../../media/2020/10/perf-mark.msft.png" alt-text="Performance. marquer des événements" lightbox="../../media/2020/10/perf-mark.msft.png":::
   `performance.mark` venu  
:::image-end:::  

### Nouveaux filtres d’URL et de types de ressources dans l’outil réseau  

Utilisez les nouveaux `resource-type` et `url` Mots clés de l’outil **réseau** pour filtrer les requêtes réseau.  Par exemple, utilisez `resource-type:image` pour vous concentrer sur les requêtes réseau qui sont des images.  

:::image type="complex" source="../../media/2020/10/network-resource-type-filter.msft.png" alt-text="filtre de type de ressource" lightbox="../../media/2020/10/network-resource-type-filter.msft.png":::
   filtre de type de ressource  
:::image-end:::  

Pour en savoir plus sur les mots-clés spéciaux, tels que `resource-type` et `url` , accédez aux [demandes de filtre par propriétés][DevtoolsNetworkReferenceFilterRequestsProperties].  Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à problèmes [#1121141][CR1121141] et [#1104188][CR1104188].  

### Mises à jour de l’affichage des détails du cadre  

#### Afficher les COEP et COOP la création de rapports au point de terminaison  

Affichez le point de terminaison de la stratégie d’intégrateur à l’origine \ (COEP \) et de la stratégie d’ouverture de la stratégie d’ouverture de la stratégie d’ouverture de fichiers \ (COOP \) `reporting to` dans la section **isolement du & de sécurité** .  L' [API de création de rapports][MdnReportingApi] définit `Report-To` un nouvel en-tête http, qui vous permet de spécifier les points de terminaison du serveur pour le navigateur et d’envoyer des avertissements et des erreurs.  Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à l' [#1051466][CR1051466]du problème.  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png" alt-text="Rapport au point de terminaison" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png":::
   Le `reporting to` point de terminaison  
:::image-end:::  

#### Afficher le mode de rapport COEP et COOP  

DevTools affiche maintenant l' `report-only` étiquette pour COEP et Coop définies sur `report-only` mode.  Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à l' [#1051466][CR1051466]du problème.  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png" alt-text="Étiquette du mode rapport uniquement" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png":::
   `report-only`Étiquette mode  
:::image-end:::  

### Afficher et résoudre les problèmes de contraste des couleurs dans l’outil vue d’ensemble CSS  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalités expérimentales":::
   Fonctionnalités expérimentales  
:::image-end:::  

L’outil de **vue d’ensemble CSS** affiche désormais une liste des éléments de votre page qui présentent des problèmes de contraste des couleurs.  La page de démonstration suivante présente un exemple de problème de contraste de couleur.  

[Présentation CSS-vue d’ensemble des couleurs accessibles][GlitchCssOverviewAccessibleColorsDemo]  

Pour activer cette expérience, sous **Settings**  >  **expériences**de configuration, sélectionnez la case à cocher **vue d’ensemble CSS** .  Pour afficher une liste des éléments présentant un problème de contraste de couleurs, dans la liste **problèmes de contraste**, sélectionnez **texte**.  Pour ouvrir l’élément dans l’outil **éléments** , sélectionnez un élément dans la liste.  Pour vous aider à résoudre les problèmes de contraste, le Microsoft Edge DevTools [fournit automatiquement des suggestions de couleurs][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane].  Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à l' [#1120316][CR1120316]du problème.  

:::image type="complex" source="../../media/2020/10/css-overview.msft.png" alt-text="Problèmes de contraste de faible couleur" lightbox="../../media/2020/10/css-overview.msft.png":::
   Problèmes de contraste de faible couleur  
:::image-end:::  

## Télécharger les canaux Microsoft Edge preview  

Si vous utilisez Windows ou macOS, envisagez d’utiliser les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] comme navigateur par défaut.  Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.  

## Contacter l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-tool "Désapprobation du volet Propriétés dans l’outil éléments-nouveautés de DevTools (Microsoft Edge 84) | Documents Microsoft"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Fonctionnalités de débogage de grille CSS-nouveautés dans DevTools (Microsoft Edge 85) | Documents Microsoft"  
[DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]: ../08/devtools.md#accessible-color-suggestion-in-the-styles-pane "Suggestions de couleurs accessibles dans le volet styles-nouveautés de DevTools (Microsoft Edge 86) | Documents Microsoft"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Émuler des appareils mobiles dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]:  https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Éléments récemment sélectionnés ou JavaScript objet-référence des API des utilitaires de la console | Documents Microsoft"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personnaliser les raccourcis clavier dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsGuideChromiumEvaluatePerformanceReference]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference "Référence d’analyse des performances | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: /microsoft-edge/devtools-guide-chromium/experimental-features#emulation-support-dual-screen-mode "Émulation: prise en charge du mode double affichage-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Activer les API expérimentales-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Activer l’éditeur de raccourcis clavier-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Émulation: prise en charge du mode double affichage-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableNetworkConsole]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-network-console "Activer la console réseau-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Activer la visionneuse de commandes sources-fonctionnalités expérimentales | Documents Microsoft"
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Tests sur les périphériques pliants et à deux écrans-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Activer les fonctionnalités expérimentales-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "référence sur les API table-console | Documents Microsoft"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Recherchez du code JavaScript et CSS inutilisé avec l’onglet couverture dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCssGrid]:  /microsoft-edge/devtools-guide-chromium/css/grid "Inspecter la grille CSS | Documents Microsoft"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Tiroir-personnaliser Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analyser les performances de rendu à l’aide de l’onglet rendu-référence d’analyse des performances | Documents Microsoft"  
[DevtoolsMediaIndex]: /microsoft-edge/devtools-guide-chromium/media/index "Afficher et déboguer les informations sur les lecteurs multimédias | Documents Microsoft"  
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties  "Demandes de filtre par propriétés-référence d’analyse du réseau | Documents Microsoft"  
[DevtoolsWebauthnIndex]: /microsoft-edge/devtools-guide-chromium/webauthn/index "Émuler les authentificateurs et déboguer webauthn dans Microsoft Edge DevTools | Documents Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux Microsoft Edge preview"  

[VisualStudioCode]: https://code.visualstudio.com "Code Visual Studio"  

[VisualStudioCodeMarketplaceMsEdgedevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools pour le code Visual Studio | Code Visual Studio"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bugs du chrome"  

[CR174309]: https://crbug.com/174309 "DevTools: autoriser pour personnaliser les raccourcis clavier/les combinaisons de touches | Bugs du chrome"
[CR772558]: https://crbug.com/772558 "DevTools: mise à jour vers la dernière version de phare | Bugs du chrome"  
[CR1034663]: https://crbug.com/1034663 "Créer un frontal pour l’API de tests webauthn | Bugs du chrome"  
[CR1047356]: https://crbug.com/1047356 "Outils CSS Grid/Flexbox/tableau | Bugs du chrome"  
[CR1051466]: https://crbug.com/1051466 "Prendre en charge le débogage COOP/COEP dans DevTools | Bugs du chrome"  
[CR1073899]: https://crbug.com/1073899 "L’onglet style calculé disparaît en mode réactif | Bugs du chrome"  
[CR1075732]: https://crbug.com/1075732 "Personnalisation de DevTools-onglets mobiles | Bugs du chrome"  
[CR1084673]: https://crbug.com/1084673 "DevTools: Améliorez la présentation des propriétés personnalisées CSS ((c’est-à-dire). Variables CSS) et leurs valeurs | Bugs du chrome"  
[CR1093687]: https://crbug.com/1093687 "Créer un outil permettant de créer et de relire des demandes de réseau synthétique Bugs du chrome"  
[CR1096230]: https://crbug.com/1096230 "Grouper les propriétés CSS par catégories dans le volet styles calculés | Bugs du chrome"  
[CR1104188]: https://crbug.com/1104188 "La recherche d’outils réseau ne trouve aucun résultat lors de la recherche d’URL complète | Bugs du chrome"  
[CR1106251]: https://crbug.com/1106251 "☂ DevTools: onglet améliorer les styles calculés | Bugs du chrome"  
[CR1120316]: https://crbug.com/1120316 "Mettez en surbrillance le contraste de votre application dans la vue d’ensemble CSS > couleurs | Bugs du chrome"  
[CR1121141]: https://crbug.com/1121141 "Autoriser le filtrage par type de ressource dans le journal réseau | Bugs du chrome"  
[CR1121312]: https://crbug.com/1121312 "Les paramètres doivent être supprimés du menu autres outils | Bugs du chrome"  
[CR1136394]: https://crbug.com/1136394 "Outils Flexbox | Bugs du chrome"  
[CR1136655]: https://crbug.com/1136655 "DevTools: localisation v2 | Bugs du chrome"  

[MdnReportingApi]: https://developer.mozilla.org/docs/Web/API/Reporting_API "API de création de rapports | MDN"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-devtools | GitHub"  

[GithubGoogleChromeLighthouseReleasesV641]: https://github.com/GoogleChrome/lighthouse/releases/v6.4.1 "v 6.4.1-GoogleChrome/phare | GitHub"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Authentification Web | GitHub"  

[GlitchCssOverviewAccessibleColorsDemo]: https://css-overview-accessible-colors-demo.glitch.me "Bonjour! | Problème"  

[PostmanSchemaJsonCollectionv210Index]: https://schema.getpostman.com/json/collection/v2.1.0/docs/index.html "Mise en forme de collection 2.1.0 v Poste"  

[SwaggerSpecificationV2]: https://swagger.io/specification/v2 "Spécification OpenAPI | Swagger"  

<!--[JecFyiDemoPerfMark]: https://jec.fyi/demo/perf-mark "" -->  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/updates/2020/10/devtools/index) et est créée par [Jecelyn Yeen][JecelynYeen] \ (développeurs, chrome devtools \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  