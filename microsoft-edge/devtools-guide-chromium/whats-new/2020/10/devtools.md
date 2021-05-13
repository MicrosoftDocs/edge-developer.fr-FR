---
description: Nouveaux outils de débogage grille CSS, outil Webauthn, outils moveables et panneau de barre latérale calculé.
title: Nouveautés de DevTools (Microsoft Edge 87)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: c7859631327fc031909cd25736fddb8cff3cff45
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564895"
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
# <a name="whats-new-in-devtools-microsoft-edge-87"></a>Nouveautés de DevTools (Microsoft Edge 87)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="improving-devtools-localization"></a>Amélioration de la localisation de DevTools  

Pour répondre à vos besoins en traduction, l Microsoft Edge’équipe DevTools se concentre sur l’amélioration de la qualité de la traduction.  À partir Microsoft Edge version 87, plusieurs chaînes et termes sont verrouillés et ne changent pas même lorsque le reste des DevTools sont affichés dans d’autres langues.  La liste des chaînes et des termes affectés est la suivante.  

*   Les chaînes de **l’outil Dente.**  
*   Le terme `service worker` .  
*   Certains filtres **de l’outil** réseau tels `URL` que , et `XHR` `JS` `CSS` .  
*   API des utilitaires de console [$0.][DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject]  
    
[$0][DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject] est désormais disponible dans la [console pour][DevtoolsConsoleIndex] les utilisateurs sur les versions localisées de DevTools.   Merci à la communauté internationale de développeurs d’aider à améliorer la localisation du Microsoft Edge DevTools.  Continuez à [envoyer des commentaires sur la qualité de](#getting-in-touch-with-microsoft-edge-devtools-team) localisation pour améliorer la prise en charge de DevTools dans tous les paramètres régionaux.  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans Chromium projet open source, accédez à [Problème #1136655][CR1136655].  


:::image type="complex" source="../../media/2020/10/bing-network-japanese.msft.png" alt-text="Outil réseau avec filtres non localisées" lightbox="../../media/2020/10/bing-network-japanese.msft.png":::
   **Volet** réseau avec filtres non localisées  
:::image-end:::  

## <a name="move-tools-between-top-and-bottom-panels"></a>Déplacer des outils entre les panneaux supérieur et inférieur  

DevTools prend désormais en charge le déplacement d’outils entre les panneaux supérieur et inférieur.  Personnalisez vos DevTools et améliorez votre productivité en combinant deux outils en même temps.  Par exemple, affichez les outils **Éléments** et **Sources** en même temps \(en déplaçant l’outil **Sources** vers le bas\).  Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez à [Problème #1075732][CR1075732].  

:::row:::
   :::column span="":::
      Pour déplacer n’importe quel outil supérieur vers le bas, pointez sur un onglet, ouvrez le menu contextuel \(clic droit\), puis choisissez **Déplacer vers le bas.**  
      
      :::image type="complex" source="../../media/2020/10/move-to-bottom.msft.png" alt-text="Déplacer vers le bas" lightbox="../../media/2020/10/move-to-bottom.msft.png":::
         Déplacer vers le bas  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Pour déplacer n’importe quel outil inférieur vers le haut, pointez sur un onglet, ouvrez le menu contextuel \(clic droit\), puis choisissez **Déplacer vers le haut.**  
      
      :::image type="complex" source="../../media/2020/10/move-to-top.msft.png" alt-text="Se déplacer vers le haut" lightbox="../../media/2020/10/move-to-top.msft.png":::
         Se déplacer vers le haut  
      :::image-end:::  
   :::column-end:::
:::row-end:::

## <a name="save-and-export-using-the-network-console"></a>Enregistrer et exporter à l’aide de la console réseau  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalité expérimentale":::
   Fonctionnalité expérimentale  
:::image-end:::  

**L’outil Console** réseau a désormais une meilleure compatibilité avec les schémas [Postman v2.1][PostmanSchemaJsonCollectionv210Index] et [OpenAPI v2.][SwaggerSpecificationV2]  To enable the experiment, navigate to [Turn on Experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable Network Console**.  Pour plus d’informations sur la **console**réseau, accédez à [Activer la fonctionnalité Expérimentation de console réseau][DevtoolsExperimentalFeaturesEnableNetworkConsole].  Cette expérience prend désormais en charge les actions suivantes.  

*   Enregistrer et exporter des collections et des environnements.  
*   Modifier et exporter des ensembles de variables d’environnement dans **l’outil Console** réseau.  
    
Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans Chromium projet open source, accédez à [Problème #1093687][CR1093687].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-name.msft.png" alt-text="Entrez le nom du nouvel environnement" lightbox="../../media/2020/10/network-console-environments-new-name.msft.png":::
         Entrez le nom du nouvel environnement  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-format.msft.png" alt-text="Choisir le format du nouvel environnement" lightbox="../../media/2020/10/network-console-environments-new-format.msft.png":::
         Choisir le format du nouvel environnement  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="improved-css-grid-tooling"></a>Outils de grille CSS améliorés  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalité expérimentale":::
   Fonctionnalité expérimentale  
:::image-end:::  

Le Microsoft Edge DevTools permet désormais d’inspecter, d’afficher et de déboguer vos grilles CSS.  

*   Affichez une superposition de grille simplifiée à l’aide de l’outil **Inspect** ou obtenez des informations plus détaillées avec des superpositions persistantes.  
*   Pour activer les superpositions de grille persistantes, choisissez l’icône de grille en face d’un élément conteneur de grille dans l’outil **Éléments** ou choisissez la grille dans l’outil **De** disposition.  
*   Vous pouvez activer les superpositions persistantes pour plusieurs grilles.  
*   Le nouvel **outil de** disposition vous permet de facilement faire basculer les superpositions de grilles et de configurer l’apparence et le contenu de chacune d’elles.  
    
Les fonctionnalités sont désactivées par défaut.  Pour plus d’informations sur les fonctionnalités, accédez à [grilles CSS][DevtoolsCssGrid].  Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez à [Problème #1047356][CR1047356].  En outre, l’équipe Microsoft Edge DevTools collabore avec l’équipe Chrome DevTools et la communauté Chromium pour ajouter de nouvelles fonctionnalités d’outils flexbox à DevTools.  Pour les mises à jour sur les outils flexbox dans Chromium projet open source, accédez à [Problème #1136394][CR1136394].  

:::image type="complex" source="../../media/2020/10/grid-layout-pane.msft.png" alt-text="Outil de disposition avec grilles" lightbox="../../media/2020/10/grid-layout-pane.msft.png":::
   **Outil de** disposition avec grilles  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a>Personnaliser les raccourcis clavier dans les paramètres  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalité expérimentale":::
   Fonctionnalité expérimentale  
:::image-end:::  

Vous pouvez désormais personnaliser le raccourci clavier pour toute action dans DevTools.  Depuis Microsoft Edge version 84, vous pouvez choisir entre les présets **Visual Studio Code** et **DevTools (par défaut)** pour les [raccourcis clavier.][DevtoolsCustomizeShortcuts]  À partir Microsoft Edge version 87, vous pouvez **** activer l’expérience d’éditeur de raccourci clavier pour personnaliser davantage les [raccourcis clavier.][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]  

Pour activer l’expérience, accédez à [Activer les fonctionnalités expérimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] et cochez la case en regard de l’éditeur de raccourci clavier. ****  Pour plus d’informations sur la personnalisation et la modification des raccourcis, accédez à Modifier les raccourcis clavier pour toute action dans [DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools].  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans Chromium projet open source, accédez à [Problème #174309][CR174309].  

:::image type="complex" source="../../media/2020/10/custom-shortcut-pause-script.msft.png" alt-text="Raccourci personnalisé pour la suspension d’un script" lightbox="../../media/2020/10/custom-shortcut-pause-script.msft.png":::
   Raccourci personnalisé pour la suspension d’un script  
:::image-end:::  

## <a name="introducing-the-microsoft-edge-tools-for-visual-studio-code-extension"></a>Présentation des outils Microsoft Edge pour Visual Studio Code extension  

Les **éléments pour Visual Studio Code** et réseau pour les extensions **Visual Studio Code** sont désormais fusionnés dans la nouvelle extension Outils de développement Microsoft Edge pour [Visual Studio Code][VisualStudioCodeMarketplaceMsEdgedevtools] de développement.  Utilisez la Microsoft Edge DevTools pour les activités suivantes sans quitter Microsoft Visual Studio Code.  

*   Déboguer le DOM  
*   Modifier CSS  
*   Inspecter le trafic réseau  

Avec l’extension, lancez Microsoft Edge, connectez-vous à une instance existante du navigateur ou utilisez un navigateur sans en-tête directement à partir de votre éditeur.  Pour commencer à contribuer et classer les problèmes avec vos commentaires sur cette extension, accédez au dépôt des outils de développement [Microsoft Edge][GithubMicrosoftVscodeEdgeDevtools] pour Visual Studio Code sur GitHub.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png" alt-text="Utilisation de l’extension en mode navigateur complet" lightbox="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png":::
         Utilisation de l’extension en mode navigateur complet  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-headless.msft.png" alt-text="Utilisation de l’extension en mode sans en-tête" lightbox="../../media/2020/10/microsoft-edge-tools-headless.msft.png":::
         Utilisation de l’extension en mode sans en-tête  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="announcements-from-the-chromium-project"></a>Annonces du projet de Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-webauthn-tool"></a>Nouvel outil WebAuthn  

Dans les versions antérieures de Microsoft Edge, il n’y avait aucune prise en charge du débogage WebAuthn natif.  Vous avez besoin d’authentifiés physiques pour tester votre application web avec [l’API d’authentification web.][GithubW3cWebauthn]  Avec le nouvel **outil WebAuthn,** vous pouvez faire les actions suivantes sans utiliser d’authentifiés physiques.

*   Émuler des authentifiés
*   Personnaliser les attributs des authentifiés
*   Inspecter les états des authentifiés
    
Pour plus d’informations sur la fonctionnalité **WebAuthn,** accédez à [Émuler les authentateurs et déboguer WebAuthn dans Microsoft Edge DevTools][DevtoolsWebauthnIndex].  

Vous pouvez émuler les authentifiés et déboguer [l’API][GithubW3cWebauthn] d’authentification web avec le nouvel outil [WebAuthn][DevtoolsWebauthnIndex].  Pour ouvrir **l’outil WebAuthn,** choisissez l’icône Personnaliser et contrôler **DevTools** \( \) > `...` **outils**  >  **WebAuthn**.  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans Chromium projet open source, accédez à [Problème #1034663][CR1034663].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/more-tools-webauthn.msft.png" alt-text="Ouvrir l’outil WebAuthn" lightbox="../../media/2020/10/more-tools-webauthn.msft.png":::
         Ouvrir **l’outil WebAuthn**  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/webauthn-enable-virtual-auth.msft.png" alt-text="Outil WebAuthn" lightbox="../../media/2020/10/webauthn-enable-virtual-auth.msft.png":::
         **Outil WebAuthn**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="elements-tool-updates"></a>Mises à jour de l’outil Éléments  

#### <a name="view-the-computed-sidebar-pane-in-the-styles-pane"></a>Afficher le volet De la barre latérale calculé dans le volet Styles  

Basculez le **volet Calculé** dans le volet **Styles.**  Le **volet Calculé** dans le volet **Styles** est réduire par défaut.  Pour le faire bascule, sélectionnez le bouton.  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans Chromium projet open source, accédez à [Problème #1073899][CR1073899].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane.msft.png" alt-text="Ouvrir le volet De la barre latérale calculé" lightbox="../../media/2020/10/computed-sidebar-pane.msft.png":::
         Ouvrir le **volet De la barre latérale** calculé  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane-open.msft.png" alt-text="Volet de barre latérale calculé" lightbox="../../media/2020/10/computed-sidebar-pane-open.msft.png":::
         **Volet de barre latérale** calculé  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="grouping-css-properties-in-the-computed-panel"></a>Regroupement des propriétés CSS dans le panneau calculé  

Pour afficher votre feuille CSS appliquée avec moins de défilement, groupez les propriétés CSS par catégories dans le **volet** calculé.  Vous pouvez également vous concentrer de manière sélective sur un ensemble de propriétés associées pendant que vous inspectez votre CSS.  Dans **l’outil Éléments,** choisissez un élément.  Pour regrouper \(ou ungrouper\) les propriétés CSS, basculez la case **à** cocher Groupe.  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans le projet open source Chromium, accédez à Problèmes [#1096230,][CR1096230] [#1084673][CR1084673]et [#1106251][CR1106251].  

:::image type="complex" source="../../media/2020/10/grouping-css-prop.msft.png" alt-text="Regroupement des propriétés CSS" lightbox="../../media/2020/10/grouping-css-prop.msft.png":::
   Regroupement des propriétés CSS  
:::image-end:::  

### <a name="lighthouse-64-in-the-lighthouse-tool"></a>Île 6.4 dans l’outil Îles  

**L’outil Îles** exécute à présent Ce dernier 6.4.  Pour obtenir la liste complète des modifications, accédez aux notes de [publication de Cerr.][GithubGoogleChromeLighthouseReleasesV641]  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans Chromium projet open source, accédez à [Problème #772558][CR772558].  

### <a name="performancemark-events-in-the-timings-section"></a>événements performance.mark() dans la section Timings  

La **section Minutages** d’un enregistrement dans l’outil [Performance][DevtoolsEvaluatePerformanceReference] marque désormais les `performance.mark()` événements.  Pour essayer cette fonctionnalité et mesurer les performances de votre code JavaScript, ajoutez des `performance.mark()` événements à votre code.  Par exemple, l’extrait de code suivant ajoute des marqueurs avant et après une boucle qui itérera de 0 à `for` 1 000 à l’aide d’incréments de 7.  

```javascript
performance.mark('start');
for (var i = 0; i < 1000; i+=7;){
  console.log(i);
}
performance.mark('end');
```  

Ensuite, ouvrez [l’outil Performance][DevtoolsEvaluatePerformanceReference] et accédez à la **section Minutages** pour enregistrer votre code JavaScript.  Les `performance.mark()` événements que vous avez ajoutés sont désormais affichés dans l’enregistrement.  

:::image type="complex" source="../../media/2020/10/perf-mark.msft.png" alt-text="Événements Performance.mark" lightbox="../../media/2020/10/perf-mark.msft.png":::
   `performance.mark` événements  
:::image-end:::  

### <a name="new-resource-type-and-url-filters-in-the-network-tool"></a>Nouveaux filtres de type de ressource et d’URL dans l’outil Réseau  

Utilisez les mots clés et `resource-type` les nouveaux mots clés dans `url` **l’outil** Réseau pour filtrer les demandes réseau.  Par exemple, utilisez cette fonction `resource-type:image` pour vous concentrer sur les demandes réseau qui sont des images.  

:::image type="complex" source="../../media/2020/10/network-resource-type-filter.msft.png" alt-text="filtre de type ressource" lightbox="../../media/2020/10/network-resource-type-filter.msft.png":::
   filtre de type ressource  
:::image-end:::  

Pour découvrir des mots clés plus spéciaux tels que et , accédez à [filtrer les demandes par `resource-type` `url` propriétés][DevtoolsNetworkReferenceFilterRequestsProperties].  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans Chromium projet open source, accédez à Problèmes #1121141 [et][CR1121141] [#1104188][CR1104188].  

### <a name="frame-details-view-updates"></a>Mises à jour de l’affichage des détails du cadre  

#### <a name="display-coep-and-coop-reporting-to-endpoint"></a>Afficher les rapports COEP et REPORTING sur le point de terminaison  

Affichez le point de terminaison De la stratégie d’incorporation d’origine croisée \(COEP\) et de la stratégie d’ouverture d’origine croisée \(PRINCIPAL\) sous la section Isolation & `reporting to` sécurité. ****  [L’API][MdnReportingApi] De rapports définit , un nouvel en-tête HTTP, qui vous permet de spécifier les points de terminaison du serveur pour le navigateur pour envoyer des `Report-To` avertissements et des erreurs.  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans Chromium projet open source, accédez à [Problème #1051466][CR1051466].  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png" alt-text="Rapport au point de terminaison" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png":::
   Point `reporting to` de terminaison  
:::image-end:::  

#### <a name="display-coep-and-coop-report-only-mode"></a>Affichage du mode de rapport COEP et BIP uniquement  

DevTools affiche désormais l’étiquette pour COEP et `report-only` PRINCIPAL qui sont définies en `report-only` mode.  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans Chromium projet open source, accédez à [Problème #1051466][CR1051466].  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png" alt-text="Étiquette du mode rapport uniquement" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png":::
   Étiquette `report-only` du mode  
:::image-end:::  

### <a name="view-and-fix-color-contrast-issues-in-the-css-overview-tool"></a>Afficher et résoudre les problèmes de contraste de couleur dans l’outil Vue d’ensemble du CSS  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalité expérimentale":::
   Fonctionnalité expérimentale  
:::image-end:::  

**L’outil Vue d’ensemble CSS** affiche désormais une liste d’éléments sur votre page qui ont des problèmes de contraste de couleur.  La page de démonstration suivante présente un exemple de problème de contraste de couleur.  

[Démonstration des couleurs accessibles de vue d’ensemble du CSS][GlitchCssOverviewAccessibleColorsDemo]  

Pour activer cette expérience, sous **Paramètres**expériences, activez la case à cocher Vue d’ensemble  >  **** **du CSS.**  Pour afficher la liste des éléments qui ont un problème de contraste de couleur, sur **les problèmes de contraste,** choisissez **Texte**.  Pour ouvrir l’élément dans **l’outil Elements,** choisissez un élément dans la liste.  Pour résoudre les problèmes de contraste, les Microsoft Edge DevTools fournissent [automatiquement des suggestions de couleur.][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans Chromium projet open source, accédez à [Problème #1120316][CR1120316].  

:::image type="complex" source="../../media/2020/10/css-overview.msft.png" alt-text="Problèmes de contraste de couleur faible" lightbox="../../media/2020/10/css-overview.msft.png":::
   Problèmes de contraste de couleur faible  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Télécharger les canaux d’aperçu Microsoft Edge  

Si vous êtes sur Windows ou macOS, envisagez d’utiliser les canaux d Microsoft Edge [d’aperçu][MicrosoftEdgePreviewChannels] comme navigateur de développement par défaut.  Les canaux de prévisualisation vous donnent accès aux dernières fonctionnalités de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Contacter l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsTool]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-tool "Annulation du volet Propriétés dans l’outil Éléments - Nouveautés de DevTools (Microsoft Edge 84) | Documents Microsoft"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Fonctionnalités de débogage de grille CSS - Nouveautés de DevTools (Microsoft Edge 85) | Documents Microsoft"  
[DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]: ../08/devtools.md#accessible-color-suggestion-in-the-styles-pane "Suggestion de couleurs accessibles dans le volet Styles - Nouveautés de DevTools (Microsoft Edge 86) | Documents Microsoft"  

[DevtoolsConsoleIndex]: ../../../console/index.md "Utiliser la console | Documents Microsoft"  
[DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject]:  ../../../console/utilities.md#recently-chosen-element-or-javascript-object "Élément ou objet JavaScript récemment choisi - Référence de l’API des utilitaires de console | Documents Microsoft"  
[DevtoolsCustomizeShortcuts]: ../../../customize/shortcuts.md "Personnaliser les raccourcis clavier dans Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]: ../../../customize/shortcuts.md#edit-keyboard-shortcuts-for-any-action-in-the-devtools "Modifier les raccourcis clavier pour toute action dans la | Documents Microsoft"  
[DevtoolsDeviceModeIndex]: ../../../device-mode/index.md "Émuler des appareils mobiles dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsEvaluatePerformanceReference]: ../../../evaluate-performance/reference.md "Référence de l’analyse des performances | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: ../../../experimental-features/index.md#emulation-support-dual-screen-mode "Émulation : prise en charge du mode double écran - Fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: ../../../experimental-features.md#enable-experimental-apis "Activer les API expérimentales : fonctionnalités expérimentales | Documents Microsoft"  
<!--  [DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: ../../../experimental-features/index.md#enable-keyboard-shortcut-editor "Enable keyboard shortcut editor - Experimental features | Microsoft Docs"  -->  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: .. /.. /.. /experimental-features/index.md#enable-new-css-grid-debugging-features «Emulation: Support dual screen mode - Experimental features | Microsoft Docs »  
[DevtoolsExperimentalFeaturesEnableNetworkConsole]: .. /.. /.. /experimental-features/index.md#enable-network-console «Enable Network Console - Experimental features | Microsoft Docs »  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: .. /.. /.. /experimental-features/index.md#enable-source-order-viewer «Enable Source Order Viewer - Experimental features | Microsoft Docs» [DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: .. /.. /.. /experimental-features/index.md#testing-on-foldable-and-dual-screen-devices «Testing on foldable and dual-screen devices - Experimental features | Microsoft Docs »  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: .. /.. /.. /experimental-features/index.md#turn-on-experimental-features " Turn on Experimental features - Experimental features | Microsoft Docs »  
[DevtoolsConsoleApiTable]: .. /.. /.. /console/api.md#table «table - Référence api console | Microsoft Docs »  
[DevtoolsCoverageIndex]: .. /.. /.. /coverage/index.md " Rechercher du code JavaScript et CSS inutilisé avec l’onglet Couverture dans Microsoft Edge devTools | Microsoft Docs »  
[DevtoolsCssGrid]: .. /.. /.. /css/grid.md " Inspect CSS Grid | Microsoft Docs »  
[DevtoolsCustomizeIndexDrawer]: .. /.. /.. /customize/index.md#drawer «Drawer - Customize Microsoft Edge DevTools | Microsoft Docs »  
[DevtoolsCustomizeIndexSettings]: .. /.. /.. /customize/index.md#settings «Paramètres - Customize Microsoft Edge DevTools | Microsoft Docs »  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: .. /.. /.. /evaluate-performance/reference.md#analyze-rendering-performance-with-the-rendering-tab " Analyser les performances de rendu avec l’onglet Rendu - Référence de l’analyse des performances | Microsoft Docs »  
[DevtoolsMediaIndex]: .. /.. /.. /media/index.md « Afficher et déboguer les informations des joueurs multimédias | Microsoft Docs »  
[DevtoolsNetworkReferenceFilterRequestsProperties]: .. /.. /.. /network/reference.md#filter-requests-by-properties «Filter requests by properties - Network Analysis reference | Microsoft Docs »  
[DevtoolsWebauthnIndex]: .. /.. /.. /webauthn/index.md « Émuler les authentateurs et déboguer WebAuthn dans Microsoft Edge devTools | Microsoft Docs »  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux d’aperçu Microsoft Edge"  

[VisualStudioCodeMain]: https://code.visualstudio.com "Code Visual Studio"  

[VisualStudioCodeMarketplaceMsEdgedevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Outils pour Visual Studio Code | Visual Studio Code"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bogues Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools : autoriser la personnalisation des raccourcis clavier/des liaisons de touches | Chromium bogues"
[CR772558]: https://crbug.com/772558 "DevTools : mise à jour vers la dernière version de | Chromium bogues"  
[CR1034663]: https://crbug.com/1034663 "Créer un serveur frontal pour l’API de test WebAuthn | Chromium bogues"  
[CR1047356]: https://crbug.com/1047356 "Outils Grille CSS/Flexbox/Tableau | Chromium bogues"  
[CR1051466]: https://crbug.com/1051466 "Prise en charge du débogage PUNAISE/COEP dans DevTools | Chromium bogues"  
[CR1073899]: https://crbug.com/1073899 "L’onglet Style calculé disparaît en mode | Chromium bogues"  
[CR1075732]: https://crbug.com/1075732 "Personnalisation de DevTools : onglets amovibles | Chromium bogues"  
[CR1084673]: https://crbug.com/1084673 "DevTools : améliorer la façon dont nous présentons les propriétés personnalisées CSS (également appelées). Variables CSS) et leurs valeurs | Chromium bogues"  
[CR1093687]: https://crbug.com/1093687 "Créer un outil pour créer et relire des demandes de réseau synthétique | Chromium bogues"  
[CR1096230]: https://crbug.com/1096230 "Group CSS properties by categories in Computed Styles pane | Chromium bogues"  
[CR1104188]: https://crbug.com/1104188 "La recherche de l’outil réseau ne trouve pas de résultats lors de la recherche d’URL complètes | Chromium bogues"  
[CR1106251]: https://crbug.com/1106251 "☂ DevTools : améliorer l’onglet Styles calculés | Chromium bogues"  
[CR1120316]: https://crbug.com/1120316 "Mettre en surbrillez le mauvais contraste sous Vue d’ensemble de CSS > couleurs | Chromium Bogues"  
[CR1121141]: https://crbug.com/1121141 "Autoriser le filtrage par type de ressource dans les journaux | Chromium bogues"  
[CR1121312]: https://crbug.com/1121312 "Paramètres être supprimé du menu Plus d’outils | Chromium bogues"  
[CR1136394]: https://crbug.com/1136394 "Outils Flexbox | Chromium Bogues"  
[CR1136655]: https://crbug.com/1136655 "Devtools : localisation v2 | Chromium bogues"  

[MdnReportingApi]: https://developer.mozilla.org/docs/Web/API/Reporting_API "Informations sur les API de | MDN"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubGoogleChromeLighthouseReleasesV641]: https://github.com/GoogleChrome/lighthouse/releases/v6.4.1 "v6.4.1 - GoogleChrome/| GitHub"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Serveur d’authentification web | GitHub"  

[GlitchCssOverviewAccessibleColorsDemo]: https://css-overview-accessible-colors-demo.glitch.me "Bonjour ! | Glitch"  

[PostmanSchemaJsonCollectionv210Index]: https://schema.getpostman.com/json/collection/v2.1.0/docs/index.html "Postman Collection Format v2.1.0 | Postman"  

[SwaggerSpecificationV2]: https://swagger.io/specification/v2 "Spécification OpenAPI | Swagger"  

<!--[JecFyiDemoPerfMark]: https://jec.fyi/demo/perf-mark "" -->  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developer.chrome.com/blog/new-in-devtools-87) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
