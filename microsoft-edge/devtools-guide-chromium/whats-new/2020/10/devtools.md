---
description: Nouveaux outils de débogage grille CSS, outil Webauthn, outils moveables et panneau de barre latérale calculé.
title: Nouveautés de DevTools (Microsoft Edge 87)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: cf3a685a1a4e9a3f13d2401a6294058a71dd5104
ms.sourcegitcommit: 12c30ad4ab2664d17c9b7e9d59d7a3cda60ff65c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313029"
---
# Nouveautés de DevTools (Microsoft Edge 87)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## Amélioration de la localisation de DevTools  

Pour répondre à vos besoins de traduction, l’équipe Microsoft Edge DevTools se concentre sur l’amélioration de la qualité de la traduction.  À partir de la version 87 de Microsoft Edge, plusieurs chaînes et termes sont verrouillés et ne changent pas même lorsque le reste des DevTools sont affichés dans d’autres langues.  La liste des chaînes et des termes affectés est la suivante.  

*   Les chaînes de **l’outil Dente.**  
*   Le terme `service worker` .  
*   Certains filtres **de l’outil** réseau tels `URL` que , et `XHR` `JS` `CSS` .  
*   API des utilitaires de console [$0.][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]  
    
[$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] est désormais disponible dans la [console pour](/microsoft-edge/devtools-guide-chromium/console/index.md) les utilisateurs sur les versions localisées de DevTools.   Merci à la communauté internationale des développeurs pour vous aider à améliorer la localisation de Microsoft Edge DevTools.  Continuez à [envoyer des commentaires sur la qualité de](#getting-in-touch-with-microsoft-edge-devtools-team) localisation pour améliorer la prise en charge de DevTools dans tous les paramètres régionaux.  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans le projet open source Chromium, accédez à [Problème #1136655][CR1136655].  

:::image type="complex" source="../../media/2020/10/bing-network-japanese.msft.png" alt-text="Outil réseau avec filtres non localisées" lightbox="../../media/2020/10/bing-network-japanese.msft.png":::
   **Volet** réseau avec filtres non localisées  
:::image-end:::  

## Déplacer des outils entre les panneaux supérieur et inférieur  

DevTools prend désormais en charge le déplacement d’outils entre les panneaux supérieur et inférieur.  Personnalisez vos DevTools et améliorez votre productivité en combinant deux outils en même temps.  Par exemple, affichez les outils **Éléments** et **Sources** en même temps \(en déplaçant l’outil **Sources** vers le bas\).  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à [Problème #1075732][CR1075732].  

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

## Enregistrer et exporter à l’aide de la console réseau  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalité expérimentale":::
   Fonctionnalité expérimentale  
:::image-end:::  

**L’outil Console** réseau a désormais une meilleure compatibilité avec les schémas [Postman v2.1][PostmanSchemaJsonCollectionv210Index] et [OpenAPI v2.][SwaggerSpecificationV2]  Pour activer l’expérience, [accédez à Activer][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] les fonctionnalités expérimentales et cochez la case en regard de **Activer la console réseau.**  Pour plus d’informations sur la **console**réseau, accédez à la fonctionnalité [Activer la console réseau expérimentale.][DevtoolsExperimentalFeaturesEnableNetworkConsole]  Cette expérience prend désormais en charge les actions suivantes.  

*   Enregistrer et exporter des collections et des environnements.  
*   Modifier et exporter des ensembles de variables d’environnement dans **l’outil Console** réseau.  
    
Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans le projet open source Chromium, accédez à [Problème #1093687][CR1093687].  

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

## Outils de grille CSS améliorés  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalité expérimentale":::
   Fonctionnalité expérimentale  
:::image-end:::  

Microsoft Edge DevTools utilise désormais les fonctionnalités suivantes pour l’inspection, l’affichage et le débogage de vos grilles CSS.  

*   Affichez une superposition de grille simplifiée à l’aide de l’outil **Inspect** ou obtenez des informations plus détaillées avec des superpositions persistantes.  
*   Pour activer les superpositions de grille persistantes, choisissez l’icône de grille en face d’un élément conteneur de grille dans l’outil **Éléments** ou choisissez la grille dans l’outil **De** disposition.  
*   Vous pouvez activer les superpositions persistantes pour plusieurs grilles.  
*   Le nouvel **outil de** disposition vous permet de facilement faire basculer les superpositions de grilles et de configurer l’apparence et le contenu de chacune d’elles.  
    
Les fonctionnalités sont désactivées par défaut.  Pour plus d’informations sur les fonctionnalités, accédez aux [grilles CSS.][DevtoolsCssGrid]  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à [Problème #1047356][CR1047356].  En outre, l’équipe Microsoft Edge DevTools collabore avec l’équipe Chrome DevTools et la communauté Chromium pour ajouter de nouvelles fonctionnalités d’outils flexbox à DevTools.  Pour les mises à jour sur les outils flexbox dans le projet open source Chromium, accédez à [Problème #1136394][CR1136394].  

:::image type="complex" source="../../media/2020/10/grid-layout-pane.msft.png" alt-text="Outil de disposition avec grilles" lightbox="../../media/2020/10/grid-layout-pane.msft.png":::
   **Outil de** disposition avec grilles  
:::image-end:::  

## Personnaliser les raccourcis clavier dans paramètres  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalité expérimentale":::
   Fonctionnalité expérimentale  
:::image-end:::  

Vous pouvez désormais personnaliser le raccourci clavier pour toute action dans DevTools.  Depuis La version 84 de Microsoft Edge, vous pouvez choisir entre les présets **Visual Studio Code** et **DevTools (par défaut)** pour les [raccourcis clavier.][DevtoolsCustomizeShortcuts]  À partir de la version 87 **** de Microsoft Edge, vous pouvez activer l’expérience d’éditeur de raccourci clavier pour personnaliser davantage les [raccourcis clavier.][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]  

Pour activer l’expérience, [accédez à Activer][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] les fonctionnalités expérimentales et activez la case à cocher en regard de **l’éditeur de raccourci clavier.**  Pour plus d’informations sur la personnalisation et la modification des raccourcis, accédez à [activer la fonctionnalité expérimentale de l’éditeur de raccourcis clavier][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans le projet open source Chromium, accédez à [Problème #174309][CR174309].  

:::image type="complex" source="../../media/2020/10/custom-shortcut-pause-script.msft.png" alt-text="Raccourci personnalisé pour la suspension d’un script" lightbox="../../media/2020/10/custom-shortcut-pause-script.msft.png":::
   Raccourci personnalisé pour la suspension d’un script  
:::image-end:::  

## Présentation des outils Microsoft Edge pour l’extension Visual Studio code  

Les **éléments pour Visual Studio code** et réseau pour les extensions Visual Studio **Code** sont désormais fusionnés dans les nouveaux outils de développement Microsoft Edge pour l’extension Visual Studio [Code.][VisualStudioCodeMarketplaceMsEdgedevtools]  Utilisez Microsoft Edge DevTools pour les activités suivantes sans quitter Visual Studio Code.  

*   Déboguer le DOM  
*   Modifier CSS  
*   Inspecter le trafic réseau  

Avec l’extension, lancez Microsoft Edge, connectez-vous à une instance existante du navigateur ou utilisez un navigateur sans en-tête directement à partir de votre éditeur.  Pour commencer à contribuer et classer les problèmes avec vos commentaires sur cette extension, accédez au référentiel Outils de développement [Microsoft Edge Visual Studio code][GithubMicrosoftVscodeEdgeDevtools] sur GitHub.  

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

## Annonces du projet de Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Nouvel outil WebAuthn  

Dans les versions antérieures de Microsoft Edge, il n’y avait aucune prise en charge du débogage WebAuthn natif.  Vous avez besoin d’authentifiés physiques pour tester votre application web avec [l’API d’authentification web.][GithubW3cWebauthn]  Avec le nouvel **outil WebAuthn,** vous pouvez faire les actions suivantes sans utiliser d’authentifiés physiques.

*   Émuler des authentifiés
*   Personnaliser les attributs des authentifiés
*   Inspecter les états des authentifiés
    
Pour plus d’informations sur la fonctionnalité **WebAuthn,** accédez à Émuler les authentifiés et [déboguer WebAuthn dans Microsoft Edge DevTools.][DevtoolsWebauthnIndex]  

Vous pouvez émuler les authentifiés et déboguer [l’API][GithubW3cWebauthn] d’authentification web avec le nouvel [outil WebAuthn.][DevtoolsWebauthnIndex]  Pour ouvrir **l’outil WebAuthn,** choisissez l’icône Personnaliser et contrôler **DevTools** \( \) > `...` **outils**  >  **WebAuthn**.  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans le projet open source Chromium, accédez à [Problème #1034663][CR1034663].  

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

### Mises à jour de l’outil Éléments  

#### Afficher le volet De la barre latérale calculé dans le volet Styles  

Basculez le **volet Calculé** dans le volet **Styles.**  Le **volet Calculé** dans le volet **Styles** est réduire par défaut.  Pour le faire bascule, sélectionnez le bouton.  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans le projet open source Chromium, accédez à [Problème #1073899][CR1073899].  

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

#### Regroupement des propriétés CSS dans le panneau calculé  

Pour afficher votre feuille CSS appliquée avec moins de défilement, groupez les propriétés CSS par catégories dans le **volet** calculé.  Vous pouvez également vous concentrer de manière sélective sur un ensemble de propriétés associées pendant que vous inspectez votre CSS.  Dans **l’outil Elements,** choisissez un élément.  Pour regrouper \(ou ungrouper\) les propriétés CSS, cochez **la** case Groupe.  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans le projet open source Chromium, accédez à Problèmes [#1096230,][CR1096230] [#1084673][CR1084673]et [#1106251][CR1106251].  

:::image type="complex" source="../../media/2020/10/grouping-css-prop.msft.png" alt-text="Regroupement des propriétés CSS" lightbox="../../media/2020/10/grouping-css-prop.msft.png":::
   Regroupement des propriétés CSS  
:::image-end:::  

### Île 6.4 dans l’outil Îles  

**L’outil Îles** exécute à présent Ce dernier 6.4.  Pour obtenir la liste complète des modifications, accédez aux notes de [publication de Cerr.][GithubGoogleChromeLighthouseReleasesV641]  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans le projet open source Chromium, accédez à [Problème #772558][CR772558].  

### événements performance.mark() dans la section Timings  

La **section Minutages** d’un enregistrement dans l’outil [Performance][DevtoolsGuideChromiumEvaluatePerformanceReference] marque désormais les `performance.mark()` événements.  Pour essayer cette fonctionnalité et mesurer les performances de votre code JavaScript, ajoutez des `performance.mark()` événements à votre code.  Par exemple, l’extrait de code suivant ajoute des marqueurs avant et après une boucle qui itérera de 0 à `for` 1 000 à l’aide d’incréments de 7.  

```javascript
performance.mark('start');
for (var i = 0; i < 1000; i+=7;){
  console.log(i);
}
performance.mark('end');
```  

Ensuite, ouvrez [l’outil Performance][DevtoolsGuideChromiumEvaluatePerformanceReference] et accédez à la **section Minutages** pour enregistrer votre code JavaScript.  Les `performance.mark()` événements que vous avez ajoutés sont désormais affichés dans l’enregistrement.  

:::image type="complex" source="../../media/2020/10/perf-mark.msft.png" alt-text="Événements Performance.mark" lightbox="../../media/2020/10/perf-mark.msft.png":::
   `performance.mark` événements  
:::image-end:::  

### Nouveaux filtres de type de ressource et d’URL dans l’outil Réseau  

Utilisez les mots clés et `resource-type` les nouveaux mots clés dans `url` **l’outil** Réseau pour filtrer les demandes réseau.  Par exemple, utilisez cette `resource-type:image` fonction pour vous concentrer sur les demandes réseau qui sont des images.  

:::image type="complex" source="../../media/2020/10/network-resource-type-filter.msft.png" alt-text="filtre de type ressource" lightbox="../../media/2020/10/network-resource-type-filter.msft.png":::
   filtre de type ressource  
:::image-end:::  

Pour découvrir des mots clés plus spéciaux tels que et `resource-type` `url` , accédez à [filtrer les demandes par propriétés.][DevtoolsNetworkReferenceFilterRequestsProperties]  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans le projet open source Chromium, accédez à Problèmes #1121141 [et][CR1121141] [#1104188][CR1104188].  

### Mises à jour de l’affichage des détails du cadre  

#### Afficher les rapports COEP et REPORTING sur le point de terminaison  

Affichez le point de terminaison De la stratégie d’incorporation d’origine croisée \(COEP\) et de la stratégie d’ouverture d’origine croisée \(PRINCIPAL\) sous la section Isolation & `reporting to` sécurité. ****  [L’API][MdnReportingApi] De rapports définit , un nouvel en-tête HTTP, qui vous permet de spécifier les points de terminaison du serveur pour le navigateur pour envoyer des `Report-To` avertissements et des erreurs.  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans le projet open source Chromium, accédez à [Problème #1051466][CR1051466].  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png" alt-text="Rapport au point de terminaison" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png":::
   Point `reporting to` de terminaison  
:::image-end:::  

#### Affichage du mode de rapport COEP et BIP uniquement  

DevTools affiche désormais l’étiquette pour COEP et `report-only` PRINCIPAL qui sont définies en `report-only` mode.  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans le projet open source Chromium, accédez à [Problème #1051466][CR1051466].  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png" alt-text="Étiquette du mode rapport uniquement" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png":::
   Étiquette `report-only` du mode  
:::image-end:::  

### Afficher et résoudre les problèmes de contraste de couleur dans l’outil Vue d’ensemble du CSS  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalité expérimentale":::
   Fonctionnalité expérimentale  
:::image-end:::  

L’outil Vue d’ensemble **CSS** affiche désormais une liste d’éléments sur votre page qui ont des problèmes de contraste de couleur.  La page de démonstration suivante présente un exemple de problème de contraste de couleur.  

[Démonstration des couleurs accessibles de vue d’ensemble du CSS][GlitchCssOverviewAccessibleColorsDemo]  

Pour activer cette expérience, sous **Expériences**de  >  **paramètres,** activez la case à cocher Vue d’ensemble **du CSS.**  Pour afficher la liste des éléments qui ont un problème de contraste de couleur, sur **les problèmes de contraste,** choisissez **Texte**.  Pour ouvrir l’élément dans **l’outil Elements,** choisissez un élément dans la liste.  Pour résoudre les problèmes de contraste, Microsoft Edge DevTools fournit automatiquement [des suggestions de couleur.][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans le projet open source Chromium, accédez à [Problème #1120316][CR1120316].  

:::image type="complex" source="../../media/2020/10/css-overview.msft.png" alt-text="Problèmes de contraste de couleur faible" lightbox="../../media/2020/10/css-overview.msft.png":::
   Problèmes de contraste de couleur faible  
:::image-end:::  

## Télécharger les canaux d’aperçu Microsoft Edge  

Si vous utilisez Windows ou macOS, envisagez d’utiliser les canaux d’aperçu [Microsoft Edge][MicrosoftEdgePreviewChannels] comme navigateur de développement par défaut.  Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.  

## Contacter l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-tool "Annulation du volet Propriétés dans l’outil Éléments - Nouveautés de DevTools (Microsoft Edge 84) | Documents Microsoft"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Fonctionnalités de débogage de grille CSS - Nouveautés de DevTools (Microsoft Edge 85) | Documents Microsoft"  
[DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]: ../08/devtools.md#accessible-color-suggestion-in-the-styles-pane "Suggestion de couleurs accessibles dans le volet Styles - Nouveautés de DevTools (Microsoft Edge 86) | Documents Microsoft"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Émuler des appareils mobiles dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]:  https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Élément récemment sélectionné ou objet JavaScript - Référence de l’API des utilitaires de console | Documents Microsoft"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personnaliser les raccourcis clavier dans l'| Microsoft Edge DevTools Documents Microsoft"  
[DevtoolsGuideChromiumEvaluatePerformanceReference]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference "Référence de l’analyse des performances | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: /microsoft-edge/devtools-guide-chromium/experimental-features#emulation-support-dual-screen-mode "Émulation : prise en charge du mode double écran - Fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Activer les API expérimentales : fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Activer l’éditeur de raccourci clavier - Fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Émulation : prise en charge du mode double écran - Fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableNetworkConsole]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-network-console "Activer la console réseau - Fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Activer la visionneuse de commandes sources - Fonctionnalités expérimentales | Documents Microsoft"
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Test sur des appareils pliables et à double écran : fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Activer les fonctionnalités expérimentales : fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "tableau - Référence de l’API de console | Documents Microsoft"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Recherchez du code JavaScript et CSS inutilisé avec l’onglet Couverture dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCssGrid]:  /microsoft-edge/devtools-guide-chromium/css/grid "Inspecter la grille CSS | Documents Microsoft"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Caisse : personnaliser l'| Microsoft Edge DevTools Documents Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analyser les performances de rendu avec l’onglet Rendu - Référence de l’analyse des performances | Documents Microsoft"  
[DevtoolsMediaIndex]: /microsoft-edge/devtools-guide-chromium/media/index "Afficher et déboguer les informations des joueurs multimédias | Documents Microsoft"  
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties  "Filtrer les demandes par propriétés : référence de l’analyse | Documents Microsoft"  
[DevtoolsWebauthnIndex]: /microsoft-edge/devtools-guide-chromium/webauthn/index "Émuler les authentifiés et déboguer WebAuthn dans Microsoft Edge DevTools | Documents Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux d’aperçu Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Code Visual Studio"  

[VisualStudioCodeMarketplaceMsEdgedevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Outils Microsoft Edge pour Visual Studio code | Visual Studio Code"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bogues Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools : autoriser la personnalisation des raccourcis clavier/des liaisons de touches | Bogues Chromium"
[CR772558]: https://crbug.com/772558 "DevTools : mise à jour vers la dernière version de | Bogues Chromium"  
[CR1034663]: https://crbug.com/1034663 "Créer un serveur frontal pour l’API de test WebAuthn | Bogues Chromium"  
[CR1047356]: https://crbug.com/1047356 "Outils Grille CSS/Flexbox/Tableau | Bogues Chromium"  
[CR1051466]: https://crbug.com/1051466 "Prise en charge du débogage PUNAISE/COEP dans DevTools | Bogues Chromium"  
[CR1073899]: https://crbug.com/1073899 "L’onglet Style calculé disparaît en mode | Bogues Chromium"  
[CR1075732]: https://crbug.com/1075732 "Personnalisation de DevTools : onglets amovibles | Bogues Chromium"  
[CR1084673]: https://crbug.com/1084673 "DevTools : améliorer la façon dont nous présentons les propriétés personnalisées CSS (également appelées). Variables CSS) et leurs valeurs | Bogues Chromium"  
[CR1093687]: https://crbug.com/1093687 "Créer un outil pour créer et relire des demandes de réseau synthétique | Bogues Chromium"  
[CR1096230]: https://crbug.com/1096230 "Group CSS properties by categories in Computed Styles pane | Bogues Chromium"  
[CR1104188]: https://crbug.com/1104188 "La recherche de l’outil réseau ne trouve pas de résultats lors de la recherche d’URL complètes | Bogues Chromium"  
[CR1106251]: https://crbug.com/1106251 "☂ DevTools : améliorer l’onglet Styles calculés | Bogues Chromium"  
[CR1120316]: https://crbug.com/1120316 "Mettre en surbrillez le mauvais contraste sous Vue d’ensemble de CSS > couleurs | Bogues Chromium"  
[CR1121141]: https://crbug.com/1121141 "Autoriser le filtrage par type de ressource dans les journaux | Bogues Chromium"  
[CR1121312]: https://crbug.com/1121312 "Les paramètres doivent être supprimés du menu Plus d’outils | Bogues Chromium"  
[CR1136394]: https://crbug.com/1136394 "Outils Flexbox | Bogues Chromium"  
[CR1136655]: https://crbug.com/1136655 "Devtools : localisation v2 | Bogues Chromium"  

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
> La page d’origine est disponible [ici](https://developers.google.com/web/updates/2020/10/devtools/index) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen