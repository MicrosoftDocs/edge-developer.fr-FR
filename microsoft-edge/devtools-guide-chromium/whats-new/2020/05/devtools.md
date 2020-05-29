---
title: Nouveautés de DevTools (Microsoft Edge 84)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: f07639d3c5cd246704f3d489c0e59714a938f13d
ms.sourcegitcommit: a5392ab44133d742c0e1fa500ad9a872989b7c3f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2020
ms.locfileid: "10684805"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# Nouveautés de DevTools (Microsoft Edge 84)  

## Annonces de l’équipe Microsoft Edge DevTools  

Les sections suivantes répertorient les annonces que vous pouvez avoir manquées de l’équipe Microsoft Edge DevTools. Découvrez-les pour essayer de nouvelles fonctionnalités dans les extensions de code DevTools, VS, etc.  Pour vous tenir au courant de toutes les fonctionnalités les plus récentes et les plus récentes de vos outils de développement, téléchargez les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] et [Suivez-nous sur Twitter][EdgeDevToolsTwitterAccount].  

### Utiliser le DevTools en mode contraste élevé Windows

Le DevTools de Microsoft Edge est désormais affiché en mode contraste élevé lorsque Windows est en mode contraste élevé.  

:::image type="complex" source="../../media/2020/05/high-contrast.msft.png" alt-text="Microsoft Edge DevTools en mode de contraste élevé" lightbox="../../media/2020/05/high-contrast.msft.png":::
   Microsoft Edge DevTools en mode de contraste élevé  
:::image-end:::  

[Suivez les instructions pour activer le mode contraste élevé dans Windows][MicrosoftSupportWindows10HighContrastMode].  Ouvrez le DevTools dans Microsoft Edge en appuyant sur `F12` ou `Ctrl` + `Shift` + `I` .  Le DevTools est affiché en mode contraste élevé.  

> [!NOTE]
> Le Microsoft Edge DevTools prend actuellement en charge le mode de contraste élevé sur Windows, mais pas sur macOS. 

[#1048378][CR1048378] problème de chrome  

### Faire correspondre les raccourcis clavier du DevTools au code VS  

À partir de vos [Commentaires](#getting-in-touch-with-microsoft-edge-devtools-team) et du suivi d’une [émission publique de chrome][CRIssuesList], l’équipe Microsoft Edge devtools a appris à la possibilité de personnaliser les raccourcis clavier dans devtools.  Dans Microsoft Edge 84, vous pouvez maintenant faire correspondre les raccourcis clavier du DevTools au [code vs][VSCode], qui est uniquement l’une des fonctionnalités sur lesquelles l’équipe travaille pour la personnalisation du raccourci.  

:::image type="complex" source="../../media/2020/05/keyboard-shortcut.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code VS" lightbox="../../media/2020/05/keyboard-shortcut.msft.png":::
   Microsoft Edge DevTools en mode de contraste élevé  
:::image-end:::  

Pour tester l’expérience, ouvrez DevTools paramètres en appuyant sur `?` ou en sélectionnant l' ![ icône d’icône Paramètres devtools ][ImageSettingsIcon] dans le coin supérieur droit du devtools.  Accédez à la section **expérimentations** et **activez l’option Activer l’onglet Paramètres des raccourcis clavier personnalisés (nécessite un recharge)**.  Rechargez maintenant le DevTools, rouvrez paramètres, puis accédez à la section **raccourcis** .  

Sélectionnez **devtools (par défaut)** dans le menu déroulant **correspondant aux raccourcis de** la liste déroulante, puis sélectionnez **Visual Studio code**.  Les raccourcis clavier dans le DevTools correspondent désormais aux raccourcis pour les actions équivalentes dans le code VS.  

Par exemple, le raccourci clavier pour suspendre ou continuer à exécuter un script en [code vs][VSCodeShortcuts] est `F5` .  Avec la valeur prédéfinie **devtools (par défaut)** , ce raccourci est le même dans devtools qu' `F8` avec le **code prédéfini Visual Studio** , ce raccourci est désormais également disponible `F5` .  

Pour l’instant, cette fonctionnalité est actuellement disponible dans le [cadre de l'](#getting-in-touch-with-microsoft-edge-devtools-team) expérience Microsoft Edge 84.  

[#174309][CR174309] problème de chrome  

### Émulateurs de surface duo de débogage à distance  

Vous pouvez maintenant déboguer à distance votre contenu Web exécuté dans l' [émulateur de surface Duo][DualScreensAndroidEmulator] en utilisant toute la puissance de [Microsoft Edge devtools][DevToolsChromiumGuide].  

Avec l' [émulateur de surface Duo][DualScreensAndroidEmulator], vous pouvez tester le rendu de votre contenu Web sur une nouvelle classe de périphériques pliants et à deux écrans.  L’émulateur exécute le système d’exploitation Android et fournit l' [application Android Microsoft Edge][AndroidEdge].  Chargez votre contenu Web dans l' [application Microsoft Edge][AndroidEdge] et déboguez-le avec [Microsoft Edge devtools][DevToolsChromiumGuide].  

:::image type="complex" source="../../media/2020/05/surface-duo-emulator.msft.png" alt-text="Application Microsoft Edge en cours d’exécution sur l’émulateur Duo surface" lightbox="../../media/2020/05/surface-duo-emulator.msft.png":::
   Application Microsoft Edge sur l’émulateur de surface Duo  
:::image-end:::  

La `edge://inspect` page dans une instance de bureau de [Microsoft Edge][DesktopEdge] affiche le **SurfaceDuoEmulator** avec une liste des onglets ouverts ou [PWAS][PwaIndex] qui s’exécutent sur l’émulateur de [surface Duo][DualScreensAndroidEmulator].  

:::image type="complex" source="../../media/2020/05/edge-inspect.msft.png" alt-text="La page edge://inspect affiche une liste des onglets ouverts dans l’application Microsoft Edge qui s’exécute sur l’émulateur." lightbox="../../media/2020/05/edge-inspect.msft.png":::
   La `edge://inspect` page affiche une liste des onglets ouverts dans l’application Microsoft Edge qui s’exécute sur l’émulateur.
:::image-end:::  

Sélectionner **Inspect** pour l’onglet ou PWA que vous voulez déboguer ouvre le [Microsoft Edge devtools][DevToolsChromiumGuide].  [Suivez le guide étape par étape pour déboguer à distance votre contenu Web sur l’émulateur de surface Duo][DevToolsRemoteDebugDuoEmulator].  

### Redimensionnez le tiroir DevTools plus facilement  

Dans Microsoft Edge 83 ou version antérieure, vous pouvez uniquement redimensionner le [tiroir-devtools][DevToolsDrawer] en pointant à l’intérieur de la barre d’outils du tiroir.  Le tiroir ne se comporte pas de la même façon que les autres commandes de redimensionnement pour les volets du DevTools où vous placez le pointeur sur la bordure du volet pour le redimensionner.  Sélectionnez l’image suivante pour voir comment le redimensionnement du tiroir a fonctionné dans la version 83 ou une version antérieure de Microsoft Edge.  

:::image type="complex" source="../../media/2020/05/drawer-83.msft.png" alt-text="Redimensionnement du tiroir DevTools dans Microsoft Edge 83" lightbox="../../media/2020/05/drawer-83.msft.gif":::
   Redimensionnement du tiroir DevTools dans Microsoft Edge 83
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

À partir de Microsoft Edge 84, vous pouvez désormais redimensionner le tiroir en pointant sur la bordure du tiroir.  Cette modification aligne le comportement redimensionnement du tiroir DevTools avec la façon dont vous redimensionnez d’autres volets dans DevTools.  Sélectionnez l’image suivante pour afficher le redimensionnement en action dans Microsoft Edge 84.  

:::image type="complex" source="../../media/2020/05/drawer-84.msft.png" alt-text="Redimensionnement du tiroir DevTools dans Microsoft Edge 84" lightbox="../../media/2020/05/drawer-84.msft.gif":::
   Redimensionnement du tiroir DevTools dans Microsoft Edge 84
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

[#1076112][CR1076112] problème de chrome  

### Les boutons de navigation de capture d’écran indiquent le focus  

Lors du débogage à distance d’un [appareil Android][DevToolsRemoteDebugAndroid], d’un [appareil Windows 10][DevToolsRemoteDebugWindows]ou d’un [émulateur duo de surface][DevToolsRemoteDebugDuoEmulator], vous pouvez activer ou désactiver la vidéo à l’aide de l' ![ icône d’enregistrement de la capture d’écran située ][ImageScreencastingIcon] dans le coin supérieur gauche du devtools.  Lorsque la fonction de capture d’écran est activée, vous pouvez naviguer dans l’onglet dans Microsoft Edge sur l’appareil distant à partir de la fenêtre DevTools.  Dans Microsoft Edge 84, ces boutons de navigation sont désormais également accessibles au clavier.  

:::image type="complex" source="../../media/2020/05/screencasting-nav.msft.png" alt-text="Appuyer sur les touches Maj + Tab de la barre d’URL de capture d’image affiche le focus sur le bouton actualiser" lightbox="../../media/2020/05/screencasting-nav.msft.png":::
   `Shift` + `Tab` Le bouton Actualiser de la barre d’URL de capture d’image indique le focus sur le bouton **Actualiser**
:::image-end:::  

[#1081486][CR1081486] problème de chrome  

### Le volet des détails du panneau réseau prend le focus  

Dans Microsoft Edge 84, le [volet d’informations][DevToolsNetworkDetails] du panneau **réseau** prend le focus lorsque vous l’ouvrez pour une ressource dans le [Journal du réseau][DevToolsNetworkLog].  Cette modification permet aux lecteurs d’écran de lire et d’interagir avec le contenu du volet **Détails** .  

:::image type="complex" source="../../media/2020/05/network-details.msft.png" alt-text="Le volet Détails du panneau réseau prend le focus lorsqu’il est ouvert" lightbox="../../media/2020/05/network-details.msft.png":::
   Le volet **Détails** du panneau **réseau** prend le focus lorsqu’il est ouvert
:::image-end:::  

[#963183][CR963183] problème de chrome  

## Annonces du projet de chrome  

Les sections suivantes annoncent des fonctionnalités supplémentaires disponibles dans Microsoft Edge 84 qui ont été fournies au projet de chrome Open source.  

### Résoudre les problèmes de site grâce au nouvel outil problèmes du tiroir DevTools

L’outil nouveaux **problèmes** du tiroir-devtools a été conçu pour vous aider à réduire la fatigue de la **console**.  Pour l’instant, la **console** est l’emplacement central pour les développeurs, les bibliothèques, les infrastructures et Microsoft Edge pour consigner des messages, des avertissements et des erreurs.  L’outil **problèmes** agrège les avertissements du navigateur dans un sens structuré, agrégé et interactif, des liens vers les ressources affectées dans Microsoft Edge devtools et fournit des recommandations pour la résolution des problèmes.  Au fil du temps, vous devriez voir d’autres avertissements dans l’environnement Microsoft Edge dans l’outil **problèmes** plutôt que la **console**, ce qui devrait vous aider à réduire le encombrement de la **console**.  

Pour commencer, voir [Rechercher et corriger les problèmes liés à l’outil problèmes dans Microsoft Edge devtools][DevtoolsIssuesIndex].  

:::image type="complex" source="../../media/2020/05/issues.msft.png" alt-text="Outil problèmes dans le tiroir DevTools" lightbox="../../media/2020/05/issues.msft.png":::
   Outil **problèmes** dans le tiroir devtools  
:::image-end:::  

[#1068116][CR1068116] problème de chrome  

### Afficher les informations sur l’accessibilité dans l’info-bulle du mode Inspect  

L’info-bulle du **mode Inspect** indique désormais si l’élément a un [nom et un rôle][WebhintHintsAxeNameRoleValue] accessibles et qu’il est [actif au clavier][WebhintHintsAxeKeyboard].  

<!--todo:  add link inspect mode tooltip (WebdevCls) when section is live  -->  
<!--todo:  add link name and role (WebdevLabelsText) when section is live  -->  
<!--todo:  add link keyboard-focusable (WebdevControlFocus) when section is live  -->  

:::image type="complex" source="../../media/2020/05/a11y.msft.png" alt-text="Info-bulle du mode Inspect avec les informations d’accessibilité" lightbox="../../media/2020/05/a11y.msft.png":::
  Info-bulle du **mode Inspect** avec les informations d’accessibilité  
:::image-end:::  

[#1040025][CR1040025] problème de chrome  

### Mises à jour du panneau de performance  

#### Afficher les informations de temps de blocage total dans le pied de page  

Après avoir enregistré vos performances de chargement, le panneau de **performance** montre désormais le temps de blocage total \ (TBT \) informations du pied de page.  TBT est une métrique de performance de chargement qui permet de mesurer le temps nécessaire pour rendre la page plus lisible.  Il mesure essentiellement la durée pendant laquelle une page s’affiche, dont le contenu est affiché à l’écran. mais il n’est pas vraiment utilisable, car JavaScript bloque le thread principal et par conséquent, la page ne répond pas aux entrées de l’utilisateur.  Le TBT est la principale mesure pour un délai approximatif de première entrée.  

<!--todo:  add link Total Blocking Time (TBT) (WebdevTbt) when section is live  -->  
<!--todo:  add link lab metric (WebdevMeasureSpeedLabField) when section is live  -->  
<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  

Pour obtenir des informations **sur le temps** de blocage total, n’utilisez pas le ![ flux de travail d’icône Actualiser la page actualiser la page ][ImageRefreshPageIcon] pour l’enregistrement des performances de chargement des pages.  

Au lieu de cela, sélectionnez l’icône **Enregistrer** ![ ][ImageRecordIcon] l’enregistrement, rechargez manuellement la page, attendez que la page se charge, puis arrêtez l’enregistrement.  

Si vous voyez `Total Blocking Time: Unavailable` , Microsoft Edge devtools n’a pas reçu les informations requises des données de profilage internes dans Microsoft Edge.  

:::image type="complex" source="../../media/2020/05/tbt.msft.png" alt-text="Total du temps de blocage dans le pied de page d’un enregistrement du panneau de performance" lightbox="../../media/2020/05/tbt.msft.png":::
   Total du temps de blocage dans le pied de page d’un enregistrement du panneau de **performance**  
:::image-end:::  

[#1054381][CR1054381] problème de chrome  

#### Événements de décalage de disposition dans la section nouvelle expertise  

La nouvelle section de l' **interface** du panneau **performances** permet de détecter les décalages de disposition.  Le décalage de disposition cumulé \ (CLS \) est une métrique qui vous permet de quantifier l’instabilité visuelle indésirable.

<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  
<!--todo:  add link layout shifts (WebdevCls) when section is live  -->  

Pour afficher les détails de la mise en page dans le volet **Résumé** , sélectionnez l’événement de **décalage de disposition** .  Placez le pointeur sur les champs **déplacé de** et **déplacé vers** pour visualiser l’emplacement de la disposition.  

:::image type="complex" source="../../media/2020/05/cls.msft.png" alt-text="Détails d’une équipe de disposition" lightbox="../../media/2020/05/cls.msft.png":::
   Détails d’une équipe de disposition  
:::image-end:::  

### Terminologie d’une promesse plus précise dans la console  

Lors de l’enregistrement de a `Promise` , la **console** n’est pas correctement fournie `PromiseStatus` avec la valeur `resolved` .  

:::image type="complex" source="../../media/2020/05/resolved.msft.png" alt-text="Exemple de la console à l’aide de l’ancienne terminologie résolue" lightbox="../../media/2020/05/resolved.msft.png":::
   Exemple de **console** utilisant l’ancienne `resolved` terminologie  
:::image-end:::  

La **console** utilise désormais le terme `fulfilled` , qui s’aligne avec la `Promise` spécification.  Pour plus d’informations sur la `Promise` spécification, voir [États et devenir sur GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).  

:::image type="complex" source="../../media/2020/05/fulfilled.msft.png" alt-text="Exemple de console utilisant la nouvelle terminologie satisfaite" lightbox="../../media/2020/05/fulfilled.msft.png":::
  Exemple de la **console** utilisant la nouvelle `fulfilled` terminologie  
:::image-end:::  

V8 problème [#6751][CRV86751]  

### Mises à jour du volet styles  

#### Prise en charge du mot-clé de rétablissement  

L’interface utilisateur de saisie semi-automatique du volet **styles** détecte désormais le mot clé CSS de [rétablissement][MDNRevert] , qui ramène la valeur en cascade d’une propriété à la valeur précédente appliquée au style de l’élément.  

:::image type="complex" source="../../media/2020/05/revert.msft.png" alt-text="Définition de la valeur d’une propriété pour la rétablir" lightbox="../../media/2020/05/revert.msft.png":::
  Définition de la valeur d’une propriété pour la rétablir  
:::image-end:::  

[#1075437][CR1075437] problème de chrome  

#### Aperçus d’images  

Pointez sur une `background-image` valeur dans le volet **styles** pour afficher un aperçu de l’image dans une info-bulle.  

:::image type="complex" source="../../media/2020/05/image-preview.msft.png" alt-text="Survol d’une valeur d’image d’arrière-plan" lightbox="../../media/2020/05/image-preview.msft.png":::
  Survol d’une `background-image` valeur  
:::image-end:::  

[#1040019][CR1040019] problème de chrome  

#### Le sélecteur de couleurs utilise désormais une notation de couleur fonctionnelle séparée par des espaces  

Le [module de couleurs CSS-niveau 4][CSSWGDraftsColor4Changes3] spécifie que les fonctions de couleur, telles que `rgb()` , doivent prendre en charge les arguments séparés par des espaces.  Par exemple, `rgb(0, 0, 0)` revient à spécifier `rbg(0 0 0)`.  

Lorsque vous choisissez des couleurs à l’aide du [Sélecteur de couleurs][DevtoolsCssReferenceColorPicker] ou alterner entre les représentations de couleurs dans le volet **styles** , en maintenant la touche enfoncée `Shift` et en sélectionnant la `background-color` valeur, vous devez voir la syntaxe d’argument séparée par un espace.  

:::image type="complex" source="../../media/2020/05/color.msft.png" alt-text="Utilisation d’arguments séparés par des espaces dans le volet styles" lightbox="../../media/2020/05/color.msft.png":::
  Utilisation d’arguments séparés par des espaces dans le volet **styles**  
:::image-end:::  

Vous devez également voir la syntaxe dans le volet **calculé** et l’info-bulle du **mode inspecter** .  

Microsoft Edge DevTools utilise la nouvelle syntaxe, car les fonctionnalités CSS à venir, telles que [Color ()][CSSWGDraftsColor4Property] ne prennent pas en charge la syntaxe d’argument séparée par des virgules.  

La syntaxe d’argument séparée par un espace est prise en charge dans la plupart des navigateurs pendant un certain temps.  Pour plus d’informations, reportez-vous à la section [puis-je utiliser des notations de couleur fonctionnelle séparées par un espace.][CaniuseMDNSpaceSeparatedFunctionalColorNotations]  

[#1072952][CR1072952] problème de chrome  

### Déconseillé du volet Propriétés dans le panneau éléments  

Le volet **Propriétés** du panneau **éléments** est déconseillé.  Exécutez `console.dir($0)` plutôt sur la **console** .  

:::image type="complex" source="../../media/2020/05/properties.msft.png" alt-text="Volet de propriétés déconseillées" lightbox="../../media/2020/05/properties.msft.png":::
   Volet de **Propriétés** déconseillées  
:::image-end:::  

#### Références  

*   [Console. dir ()][DevtoolsConsoleApiDir]  
*   [$0][DevtoolsConsoleUtilitiesDom]  

### Prise en charge des raccourcis d’application dans le volet manifeste  

Les raccourcis d’application permettent aux utilisateurs de démarrer rapidement des tâches courantes ou recommandées au sein d’une application Web.  Le menu Raccourcis de l’application s’affiche uniquement pour les [applications Web progressives][PwaIndex] installées sur le bureau ou l’appareil mobile de l’utilisateur.  

<!--For more information, see [Get things done quickly with app shortcuts][WebdevAppShortcuts].  -->  

<!--todo:  add link Get things done quickly with app shortcuts (WebdevAppShortcuts) when section is live -->  

:::image type="complex" source="../../media/2020/05/app-shortcuts.msft.png" alt-text="Raccourcis d’application dans le volet manifeste" lightbox="../../media/2020/05/app-shortcuts.msft.png":::
  Raccourcis d’application dans le volet **manifeste**  
:::image-end:::  

## Télécharger les canaux Microsoft Edge preview   

Si vous utilisez Windows ou macOS, envisagez d’utiliser les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] comme navigateur par défaut.  Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.  

## Contacter l’équipe Microsoft Edge devtools  

  

Découvrir les nouvelles fonctionnalités et les modifications apportées au billet ou tout autre sujet lié à DevTools:  

*   Envoyez vos commentaires à l’aide de l’icône de **Commentaires** dans le devtools  
*   Tweeter sur [@EdgeDevTools][PostTweetEdgeDevTools]  
*   Envoyez une suggestion au [site Web de votre choix][TheWebWeWant]  
*   Classer les bogues sur cette page dans le référentiel [Edge-développeurs][GitHubMicrosoftDocsEdgeDeveloperNewIssue]  

:::image type="complex" source="../../media/2020/05/feedback-icon.msft.png" alt-text="Icône de commentaires dans le Microsoft Edge DevTools" lightbox="../../media/2020/05/feedback-icon.msft.png":::
  Icône de **Commentaires** dans le Microsoft Edge devtools  
:::image-end:::  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png "Icône Paramètres de DevTools"
[ImageScreencastingIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/images/toggle-screencast-icon.msft.png "Icône de DevTools bascule"
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-page-icon.msft.png "Icône de page actualiser du panneau performances DevTools"
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png "Icône d’enregistrement du panneau de performance DevTools"

<!-- links -->  

[DualScreensAndroidEmulator]: /dual-screen/android/use-emulator "Utiliser l’émulateur de surface Duo | Documents Microsoft"

[DevtoolsConsoleApiDir]: /microsoft-edge/devtools-guide-chromium/console/api#dir "Référence sur l’API dir-console | Documents Microsoft"  
[DevtoolsConsoleUtilitiesDom]: /microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Éléments récemment sélectionnés ou JavaScript objet-référence des API des utilitaires de la console | Documents Microsoft"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Changer les couleurs à l’aide du sélecteur de couleurs-Référence CSS | Documents Microsoft"  
[DevToolsDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Tiroir-présentation de la personnalisation | Documents Microsoft"  
[DevToolsChromiumGuide]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Recherchez et corrigez les problèmes liés à l’onglet problèmes dans Microsoft Edge DevTools Documents Microsoft"  
[DevToolsRemoteDebugAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Commencer à utiliser le débogage à distance des appareils Android | Documents Microsoft"  
[DevToolsRemoteDebugDuoEmulator]: /microsoft-edge/devtools-guide-chromium/remote-debugging/surface-duo-emulator "Commencer avec les émulateurs de surface duo pour le débogage à distance Documents Microsoft"  
[DevToolsRemoteDebugWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Commencer à utiliser le débogage à distance des appareils Windows 10 | Documents Microsoft"  
[DevToolsNetworkDetails]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Inspecter les détails de la ressource | Documents Microsoft"  
[DevToolsNetworkLog]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Journalisation de l’activité du réseau | Documents Microsoft"  
[PwaIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Applications Web progressives sur Windows | Documents Microsoft"  
<!--[DevtoolsWhatsNew201901Inspect]: /microsoft-edge/devtools-guide-chromium/whats-new/2019/01/devtools#inspect "Detailed tooltips in Inspect Mode - What's New In DevTools (Edge 73) | Microsoft Docs"  -->  

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Application Microsoft Edge Android"

[CaniuseMDNSpaceSeparatedFunctionalColorNotations]: https://caniuse.com/#feat=mdn-css_types_color_space_separated_functional_notation "Notations de couleur fonctionnelle séparées par un espace-MDN | Puis-je utiliser"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bugs du chrome"

[CR174309]: https://crbug.com/174309 "DevTools: autoriser pour personnaliser les raccourcis clavier/les combinaisons de touches | Bugs du chrome"  
[CR963183]: https://crbug.com/963183 "DevTools ne respectent pas la norme WCAG | Bugs du chrome"  
[CR1040019]: https://crbug.com/1040019 "DevTools: Affichez un aperçu des images et images d’arrière-plan facilement dans le volet styles | Bugs du chrome"  
[CR1040025]: https://crbug.com/1040025 "DevTools: afficher les informations a11y de base dans l’élément popover | Bugs du chrome"  
[CR1048378]: https://crbug.com/1048378 "Prise en charge de l’interface utilisateur DevTools pour le mode contraste élevé | Bugs du chrome"  
[CR1054381]: https://crbug.com/1054381 "CR 1054381 | Bugs du chrome"  
[CR1068116]: https://crbug.com/1068116 "Panneau problèmes d’expédition | Bugs du chrome"  
[CR1072952]: https://crbug.com/1072952 "DevTools: le sélecteur de couleurs doit générer une syntaxe de couleur CSS moderne | Bugs du chrome"  
[CR1075437]: https://crbug.com/1075437 "DevTools: ajoutez la prise en charge du mot-clé/valeur CSS «rétablir». Bugs du chrome"  
[CR1076112]: https://crbug.com/1076112 "Personalization devtools-tiroir du tiroir"  
[CR1081486]: https://crbug.com/1081486 "Le focus clavier n’est pas visible pour les boutons de navigation en mode screencast | Bugs du chrome"  
[CRV86751]: https://bugs.chromium.org/p/v8/issues/detail?id=6751 "PromiseStatus doit être «respecté», et non «résolu» | V8 bogues"  

[CSSWGDraftsColor4Changes3]: https://drafts.csswg.org/css-color#changes-from-3 "Modifications des couleurs 3-CSS-module de couleurs-niveau 4 | Brouillons de l’éditeur de groupe de travail CSS W3C"  
[CSSWGDraftsColor4Property]: https://drafts.csswg.org/css-color#the-color-property "3. couleur de premier plan: «couleur»-module de couleur CSS-niveau 4 | Brouillons de l’éditeur de groupe de travail CSS W3C"  

[DesktopEdge]: https://www.microsoft.com/edge/ "Présentation du nouveau Microsoft Edge"  

[GithubDomenicPromiseUnwrappingStatesFates]: https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md "États et-Domenic/promet-déconditionnement | GitHub"  

[MDNRevert]: https://developer.mozilla.org/docs/Web/CSS/revert "rétablir | MDN"  
[MDNRevertBrowserCompatibility]: https://developer.mozilla.org/docs/Web/CSS/revert#Browser_compatibility "Compatibilité du navigateur | MDN"  

[VSCode]: https://code.visualstudio.com/ "Code Visual Studio"  
[VSCodeShortcuts]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Raccourcis clavier dans Visual Studio code pour Windows"  

[WebhintHintsAxeKeyboard]: https://webhint.io/docs/user-guide/hints/hint-axe/keyboard/ "Axe: clavier | Astuce"  
[WebhintHintsAxeNameRoleValue]: https://webhint.io/docs/user-guide/hints/hint-axe/name-role-value/ "Axe: valeur du rôle de nom | Astuce"  

[MicrosoftSupportWindows10HighContrastMode]: https://support.microsoft.com/help/4026951/windows-10-turn-high-contrast-mode-on-or-off "Activer ou désactiver le mode contraste élevé dans Windows | Support Windows"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publiez un tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools compte Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nouveau problème-MicrosoftDocs/Edge-développeur"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canaux Microsoft Edge preview"  
[TheWebWeWant]: https://aka.ms/webwewant "Le site Web de votre choix"  

<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebdevCoreWebVitals]: https://alphabet-dev/vitals#core-web-vitals "Core Web Vitals | alphabet-dev"  -->  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/updates/2020/05/devtools/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
