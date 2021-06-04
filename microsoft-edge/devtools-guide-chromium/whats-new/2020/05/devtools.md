---
description: Utilisez devTools en mode Windows contraste élevé, mettre en correspondance les raccourcis clavier dans DevTools pour Visual Studio Code, et bien plus encore.
title: Nouveautés de DevTools (Microsoft Edge 84)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 2537495ad14462aac70bfb1b5873aaa0b6e21cdf
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564671"
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
# <a name="whats-new-in-devtools-microsoft-edge-84"></a>Nouveautés de DevTools (Microsoft Edge 84)  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Annonces de l’équipe Microsoft Edge DevTools  

Les sections suivantes sont une liste des annonces que vous avez peut-être manquées de l’équipe Microsoft Edge DevTools.  Consultez les annonces pour essayer de nouvelles fonctionnalités dans DevTools, Microsoft Visual Studio extensions de code, etc.  Pour rester à jour sur toutes les fonctionnalités les plus récentes et les plus importantes de vos outils de développement, téléchargez les canaux d’aperçu [Microsoft Edge][MicrosoftEdgePreviewChannels] et suivez-nous [sur Twitter.][EdgeDevToolsTwitterAccount]  

### <a name="use-the-devtools-in-windows-high-contrast-mode"></a>Utiliser DevTools en mode Windows contraste élevé

Les Microsoft Edge DevTools sont désormais affichés en mode de contraste élevé lorsque Windows est en mode de contraste élevé.  

:::image type="complex" source="../../media/2020/05/high-contrast.msft.png" alt-text="Le Microsoft Edge DevTools en mode de contraste élevé" lightbox="../../media/2020/05/high-contrast.msft.png":::
   Le Microsoft Edge DevTools en mode de contraste élevé  
:::image-end:::  

[Suivez les instructions pour activer le mode de contraste élevé dans Windows][MicrosoftSupportWindows10HighContrastMode].  Pour ouvrir devTools dans Microsoft Edge, sélectionnez `F12` ou `Ctrl` + `Shift` + `I` .  Les DevTools sont affichés en mode de contraste élevé.  

> [!NOTE]
> Le Microsoft Edge DevTools actuellement prise en charge le mode de contraste élevé sur Windows mais pas sur macOS.  

Chromium problème [#1048378][CR1048378]  

### <a name="match-keyboard-shortcuts-in-the-devtools-to-visual-studio-code"></a>Faire correspondre les raccourcis clavier dans devTools à Visual Studio Code  

À [](#getting-in-touch-with-microsoft-edge-devtools-team) partir de vos commentaires et de l’Chromium suivi des problèmes publics, l’équipe Microsoft Edge DevTools [a][CRIssuesList]appris que vous souhaitiez personnaliser les raccourcis clavier dans DevTools.  Dans Microsoft Edge 84, vous pouvez désormais faire correspondre les raccourcis clavier de DevTools à [Visual Studio Code,][VisualStudioCodeMain]qui n’est qu’une des fonctionnalités sur lesquelles l’équipe travaille pour la personnalisation des raccourcis.  

:::image type="complex" source="../../media/2020/05/keyboard-shortcut.msft.png" alt-text="Faire correspondre les raccourcis clavier dans devTools à Visual Studio Code" lightbox="../../media/2020/05/keyboard-shortcut.msft.png":::
   Le Microsoft Edge DevTools en mode de contraste élevé  
:::image-end:::  

Pour essayer l’expérience, ouvrez DevTools Paramètres en sélectionnant ou en choisissant l’icône Devtools Paramètres dans le coin supérieur droit de `?` ![ ](../../../media/settings-icon.msft.png) DevTools.  Accédez à la section **Expériences** et cochez l’onglet Activer les paramètres des **raccourcis clavier personnalisés (nécessite un rechargement).**  À présent, rechargez DevTools, Paramètres à nouveau et accédez à la section **Raccourcis.**  

Choose **DevTools (Default)** in the **Match shortcuts from preset** dropdown and select **Visual Studio Code**.  Les raccourcis clavier dans devTools correspondent désormais aux raccourcis pour les actions équivalentes dans Visual Studio Code.  

Par exemple, le raccourci clavier pour mettre en pause ou poursuivre l’exécution d’un script [Visual Studio Code][VisualStudioCodeShortcuts] `F5` est .  Avec **devTools (par défaut)** prédéfiny, ce même raccourci dans DevTools n’est qu’avec le `F8` **Visual Studio Code** prédéfiny, ce raccourci est désormais également `F5` .  

La fonctionnalité est actuellement disponible dans Microsoft Edge 84 en tant qu’expérience. Veuillez donc partager vos commentaires [avec](#getting-in-touch-with-microsoft-edge-devtools-team) l’équipe !  

Chromium problème [#174309][CR174309]  

### <a name="remote-debug-surface-duo-emulators"></a>Débogage à distance des émulateurs Surface Duo  

Vous pouvez désormais déboguer à distance votre contenu web en cours d’exécution dans l’émulateur [Surface Duo][DualScreensAndroidEmulator] à l’aide de la puissance totale du [Microsoft Edge DevTools][DevtoolsIndex].  

Avec [l’émulateur Surface Duo,][DualScreensAndroidEmulator]vous pouvez tester le rendu de votre contenu web sur une nouvelle classe d’appareils pliables et à double écran.  L’émulateur exécute le système d’exploitation Android et fournit [l’Microsoft Edge’application Android.][AndroidEdge]  Chargez votre contenu web dans [l’application Microsoft Edge et][AndroidEdge] déboguer avec le [Microsoft Edge DevTools][DevtoolsIndex].  

:::image type="complex" source="../../media/2020/05/surface-duo-emulator.msft.png" alt-text="Application Microsoft Edge’exécution sur l’émulateur Surface Duo" lightbox="../../media/2020/05/surface-duo-emulator.msft.png":::
   Application Microsoft Edge sur l’émulateur Surface Duo  
:::image-end:::  

La page d’une instance de bureau de Microsoft Edge affiche l’appareil `edge://inspect` **SurfaceDuoEmulator** [][DesktopEdge] avec une liste des onglets ouverts ou des applications de bureau en cours d’exécution sur l’émulateur [Surface Duo.][DualScreensAndroidEmulator] [][PwaIndex]  

:::image type="complex" source="../../media/2020/05/edge-inspect.msft.png" alt-text="La page edge://inspect affiche la liste des onglets ouverts dans l’application Microsoft Edge’exécution sur l’émulateur" lightbox="../../media/2020/05/edge-inspect.msft.png":::
   La page affiche la liste des onglets ouverts dans `edge://inspect` l’application Microsoft Edge’exécution sur l’émulateur
:::image-end:::  

Choisissez **inspectez** l’onglet ou PWA que vous souhaitez déboguer pour ouvrir le [Microsoft Edge DevTools][DevtoolsIndex].  Suivez le guide pas à pas pour déboguer à distance votre contenu [web sur l’émulateur Surface Duo.][DevtoolsRemoteDebugDuoEmulator]  

### <a name="resize-the-devtools-drawer-more-easily"></a>Resize the DevTools drawer more easily  

Dans Microsoft Edge 83 ou une précédente, vous n’avez pu resizer le caisse de [dévtools][DevtoolsDrawer] qu’en pointant à l’intérieur de la barre d’outils de la caisse.  Le drawer se comporte différemment des autres contrôles de re resize pour les volets des DevTools où vous placez le pointeur sur la bordure du volet pour le resizer.  Choisissez l’image suivante pour afficher le resizing the Drawer worked in version 83 or earlier of Microsoft Edge.  

:::image type="complex" source="../../media/2020/05/drawer-83.msft.png" alt-text="Resizing the DevTools Drawer in Microsoft Edge 83" lightbox="../../media/2020/05/drawer-83.msft.gif":::
   Resizing the DevTools Drawer in Microsoft Edge 83
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

À partir Microsoft Edge 84, vous pouvez maintenant re resizer le caisse en pointant sur la bordure de la caisse.  Cette modification aligne le comportement de resizing the DevTools Drawer with the way you resize other panes in the DevTools.  Choisissez l’image suivante pour afficher le re re resserrement en action dans Microsoft Edge 84.  

:::image type="complex" source="../../media/2020/05/drawer-84.msft.png" alt-text="Resizing the DevTools Drawer in Microsoft Edge 84" lightbox="../../media/2020/05/drawer-84.msft.gif":::
   Resizing the DevTools Drawer in Microsoft Edge 84
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

Chromium problème [#1076112][CR1076112]  

### <a name="screencasting-navigation-buttons-display-focus"></a>Les boutons de navigation par capture vidéo affichent le focus  

Lors du débogage à distance d’un appareil [Android,][DevtoolsRemoteDebugAndroid]d’un appareil [Windows 10][DevtoolsRemoteDebugWindows]ou d’un émulateur [Surface Duo,][DevtoolsRemoteDebugDuoEmulator]vous pouvez faire basculer la capture vidéo avec l’icône Deggle Screencast dans le coin supérieur gauche de ![ ](../../../media/toggle-screencast-icon.msft.png) DevTools.  Avec la capture vidéo activée, vous pouvez naviguer dans l’onglet Microsoft Edge sur l’appareil distant à partir de la fenêtre DevTools.  Dans Microsoft Edge 84, ces boutons de navigation sont désormais également accessibles au clavier.  

:::image type="complex" source="../../media/2020/05/screencasting-nav.msft.png" alt-text="Select Shift+Tab from the screencasted URL bar shows focus on the Refresh button" lightbox="../../media/2020/05/screencasting-nav.msft.png":::
   La `Shift` + `Tab` sélection dans la barre d’URL par capture vidéo affiche le focus sur le **bouton Actualiser**
:::image-end:::  

Chromium problème [#1081486][CR1081486]  

### <a name="network-panel-details-pane-is-now-accessible"></a>Le volet Détails du panneau réseau est désormais accessible  

Dans Microsoft Edge 84, le volet [Détails][DevtoolsNetworkDetails] **** de l’outil Réseau prend désormais le focus lorsque vous l’ouvrez pour une ressource dans le [journal réseau.][DevtoolsNetworkLog]  Cette modification permet aux lecteurs d’écran de lire et d’interagir avec le contenu du volet **d’informations.**  

:::image type="complex" source="../../media/2020/05/network-details.msft.png" alt-text="Le volet Détails du panneau Réseau prend le focus à l’ouverture" lightbox="../../media/2020/05/network-details.msft.png":::
   Le **volet Détails** de **l’outil** Réseau prend le focus à l’ouverture
:::image-end:::  

Chromium problème [#963183][CR963183]  

## <a name="announcements-from-the-chromium-project"></a>Annonces du projet de Chromium  

Les sections suivantes annoncent des fonctionnalités supplémentaires disponibles dans Microsoft Edge 84 qui ont été contribués au projet d’Chromium open source.  

### <a name="fix-site-issues-with-the-new-issues-tool-in-the-devtools-drawer"></a>Résoudre les problèmes de site avec le nouvel outil Problèmes dans le caisse de DevTools

Le nouvel outil Problèmes dans le caisse DevTools a été conçu pour vous aider à réduire la fatigue et l’encombrement des **notifications** de la **console.**  Actuellement, la **console** est l’endroit central pour les développeurs de sites web, les bibliothèques, les frameworks et les Microsoft Edge journaux des messages, des avertissements et des erreurs.  L’outil Problèmes regroupe les avertissements du navigateur de manière structurée, agrégée et actionnable, les liens vers les ressources affectées dans Microsoft Edge DevTools et fournit des conseils sur la façon de résoudre les problèmes. ****  Au fil du temps, de plus en plus **** d’avertissements sont publiés dans Microsoft Edge dans l’outil Problèmes plutôt que dans la **console,** ce qui devrait aider à réduire l’encombrement dans la **console.**  

To get started, navigate to [Find and Fix Problems With The Microsoft Edge devTools Issues tool][DevtoolsIssuesIndex].  

:::image type="complex" source="../../media/2020/05/issues.msft.png" alt-text="L’outil Problèmes dans le caisse de DevTools" lightbox="../../media/2020/05/issues.msft.png":::
   **L’outil Problèmes** dans le caisse de DevTools  
:::image-end:::  

Chromium problème [#1068116][CR1068116]  

### <a name="view-accessibility-information-in-the-inspect-mode-tooltip"></a>Afficher les informations d’accessibilité dans l’info-bulle Inspect Mode  

**L’tip d’outils** Inspect Mode indique maintenant si l’élément a un nom [et][WebhintHintsAxeNameRoleValue] un rôle accessibles et est accessible [au clavier.][WebhintHintsAxeKeyboard]  

<!--todo:  add link inspect mode tooltip (WebdevCls) when section is live  -->  
<!--todo:  add link name and role (WebdevLabelsText) when section is live  -->  
<!--todo:  add link keyboard-focusable (WebdevControlFocus) when section is live  -->  

:::image type="complex" source="../../media/2020/05/a11y.msft.png" alt-text="Info-bulle Inspecter le mode avec des informations d’accessibilité" lightbox="../../media/2020/05/a11y.msft.png":::
  **Info-bulle Inspecter le mode** avec des informations d’accessibilité  
:::image-end:::  

Chromium problème [#1040025][CR1040025]  

### <a name="performance-panel-updates"></a>Mises à jour du panneau de performances  

#### <a name="view-total-blocking-time-information-in-the-footer"></a>Afficher le nombre total d’informations sur le temps de blocage dans le pied de groupe  

Après avoir enregistré vos performances de chargement, le panneau **Performances** affiche désormais le temps de blocage total \(TBT\) informations dans le pied de groupe.  TBT est une mesure de performances de charge qui permet de quantifier le temps qu’une page prend pour devenir utilisable.  Elle mesure essentiellement la durée pendant combien de temps une page semble utilisable \(car le contenu est restituer à l’écran\) ; mais n’est pas réellement utilisable, car JavaScript bloque le thread principal et par conséquent, la page ne répond pas aux entrées de l’utilisateur.  TBT est la mesure principale pour l’approximation du premier délai d’entrée.  

<!--todo:  add link Total Blocking Time (TBT) (WebdevTbt) when section is live  -->  
<!--todo:  add link lab metric (WebdevMeasureSpeedLabField) when section is live  -->  
<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  

Pour obtenir les informations sur le **** temps total de blocage, n’utilisez pas le flux de travail d’icône Actualiser la page Actualiser la page pour enregistrer les ![ performances de chargement de ](../../../media/refresh-page-icon.msft.png) page.  

Sélectionnez plutôt **l’icône Enregistrement** , rechargez manuellement la page, attendez le chargement de la ![ ](../../../media/record-icon.msft.png) page, puis arrêtez l’enregistrement.  

`Total Blocking Time: Unavailable`S’il est affiché, Microsoft Edge DevTools n’a pas eu les informations requises des données de profilage internes dans Microsoft Edge.  

:::image type="complex" source="../../media/2020/05/tbt.msft.png" alt-text="Total Blocking Time information in the footer of a Performance panel recording" lightbox="../../media/2020/05/tbt.msft.png":::
   Total Blocking Time information in the footer of a **Performance** panel recording  
:::image-end:::  

Chromium [problème][CR1054381] #1054381  

#### <a name="layout-shift-events-in-the-new-experience-section"></a>Événements Layout Shift dans la nouvelle section Expérience  

La nouvelle section **Expérience** du panneau **Performances** vous permet de détecter les changements de disposition.  La mise en page cumulative Shift \(CLS\) est une mesure qui vous permet de quantifier l’instabilité visuelle indésirable.

<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  
<!--todo:  add link layout shifts (WebdevCls) when section is live  -->  

Choisissez **l’événement Layout Shift** pour afficher les détails de l’équipe de disposition dans le **volet** Résumé.  Pointez sur les **champs Déplacé d’et** Déplacé **vers** pour visualiser l’endroit où le changement de disposition s’est produit.  

:::image type="complex" source="../../media/2020/05/cls.msft.png" alt-text="Détails d’un changement de disposition" lightbox="../../media/2020/05/cls.msft.png":::
   Détails d’un changement de disposition  
:::image-end:::  

### <a name="more-accurate-promise-terminology-in-the-console"></a>Terminologie des promesses plus précise dans la console  

Lors de la `Promise` journalisation d’un , **la console** a fourni de `PromiseStatus` manière incorrecte la valeur définie sur `resolved` .  

:::image type="complex" source="../../media/2020/05/resolved.msft.png" alt-text="Exemple de console utilisant l’ancienne terminologie résolue" lightbox="../../media/2020/05/resolved.msft.png":::
   Exemple de console **utilisant** l’ancienne `resolved` terminologie  
:::image-end:::  

La **console** utilise désormais le terme `fulfilled` , qui s’aligne sur la `Promise` spécification.  Pour plus d’informations sur `Promise` la spécification, accédez à [États et aux états GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).  

:::image type="complex" source="../../media/2020/05/fulfilled.msft.png" alt-text="Exemple de console utilisant la nouvelle terminologie utilisée" lightbox="../../media/2020/05/fulfilled.msft.png":::
  Exemple de console **utilisant** la nouvelle `fulfilled` terminologie  
:::image-end:::  

Problème V8 [#6751][CRV86751]  

### <a name="styles-pane-updates"></a>Mises à jour du volet Styles  

#### <a name="support-for-the-revert-keyword"></a>Prise en charge du mot clé de revert  

L’interface utilisateur de la mise à jour automatique du volet **Styles** détecte désormais le mot clé [CSS][MDNRevert] qui permet de revenir à la valeur en cascade d’une propriété à la valeur précédente appliquée au style de l’élément.  

:::image type="complex" source="../../media/2020/05/revert.msft.png" alt-text="Définition de la valeur d’une propriété à inverser" lightbox="../../media/2020/05/revert.msft.png":::
  Définition de la valeur d’une propriété à inverser  
:::image-end:::  

Chromium problème [#1075437][CR1075437]  

#### <a name="image-previews"></a>Aperçus d’image  

Pointez sur une valeur dans le volet Styles pour afficher un aperçu de `background-image` l’image **** dans une boîte à outils.  

:::image type="complex" source="../../media/2020/05/image-preview.msft.png" alt-text="Pointage sur une valeur d’image d’arrière-plan" lightbox="../../media/2020/05/image-preview.msft.png":::
  Pointage sur une `background-image` valeur  
:::image-end:::  

Chromium problème [#1040019][CR1040019]  

#### <a name="color-picker-now-uses-space-separated-functional-color-notation"></a>Le s sélectionneur de couleurs utilise désormais la notation de couleur fonctionnelle séparée par des espaces  

Le module [de couleur CSS de niveau 4][CSSWGDraftsColor4Changes3] spécifie que les fonctions de couleur, telles que , doivent prendre en charge les `rgb()` arguments séparés par des espaces.  Par exemple, `rgb(0, 0, 0)` revient à spécifier `rbg(0 0 0)`.  

Lorsque vous choisissez [][DevtoolsCssReferenceColorPicker] des couleurs avec le sélecateur de couleurs ou si vous choisissez une autre représentation des couleurs dans le volet **Styles** en maintenant et en sélectionnant la valeur, la syntaxe de l’argument séparé par des espaces `Shift` `background-color` s’affiche.  

:::image type="complex" source="../../media/2020/05/color.msft.png" alt-text="Utilisation d’arguments séparés par des espaces dans le volet Styles" lightbox="../../media/2020/05/color.msft.png":::
  Utilisation d’arguments séparés par des espaces dans le **volet Styles**  
:::image-end:::  

Vous devez également afficher la syntaxe dans le volet **Calculé** et **l’info-bulle du mode** Inspect.  

Microsoft Edge DevTools utilise la nouvelle syntaxe, car les fonctionnalités CSS à venir, telles que [color()][CSSWGDraftsColor4Property] ne la prise en charge de la syntaxe d’arguments séparées par des virgules.  

La syntaxe de l’argument séparé par des espaces est prise en charge dans la plupart des navigateurs depuis un certain temps.  Pour plus d’informations, accédez à [Can I use: Space-separated functional color notations?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]  

Chromium problème [#1072952][CR1072952]  

### <a name="deprecation-of-the-properties-pane-in-the-elements-panel"></a>Désopation du volet Propriétés dans le panneau Éléments  

Le **volet Propriétés** de **l’outil Éléments** est supprimé.  `console.dir($0)`Exécutez-la **dans la console** à la place.  

:::image type="complex" source="../../media/2020/05/properties.msft.png" alt-text="Volet Propriétés déprécié" lightbox="../../media/2020/05/properties.msft.png":::
   Volet Propriétés **** déprécié  
:::image-end:::  

#### <a name="references"></a>Références  

*   [console.dir()][DevtoolsConsoleApiDir]  
*   [$0][DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject]  

### <a name="app-shortcuts-support-in-the-manifest-pane"></a>Prise en charge des raccourcis d’application dans le volet manifeste  

Les raccourcis d’application aident les utilisateurs à démarrer rapidement des tâches courantes ou recommandées dans une application web.  Le menu des raccourcis de l’application s’affiche uniquement pour les applications [web][PwaIndex] progressives installées sur le bureau ou l’appareil mobile de l’utilisateur.  

<!--For more information, navigate to [Get things done quickly with app shortcuts][WebdevAppShortcuts].  -->  

<!--todo:  add link Get things done quickly with app shortcuts (WebdevAppShortcuts) when section is live -->  

:::image type="complex" source="../../media/2020/05/app-shortcuts.msft.png" alt-text="Raccourcis d’application dans le volet manifeste" lightbox="../../media/2020/05/app-shortcuts.msft.png":::
  Raccourcis d’application dans le **volet** manifeste  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Télécharger les canaux d’aperçu Microsoft Edge  

Si vous êtes sur Windows ou macOS, envisagez d’utiliser les canaux d Microsoft Edge [d’aperçu][MicrosoftEdgePreviewChannels] comme navigateur de développement par défaut.  Les canaux de prévisualisation vous donnent accès aux dernières fonctionnalités de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Mise en contact avec Microsoft Edge devtools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

<!--[DevtoolsWhatsNew201901Inspect]: ../../../whats-new/2019/01/devtools.md#inspect "Detailed tooltips in Inspect Mode - What's New In DevTools (Edge 73) | Microsoft Docs"  -->  

[DevtoolsConsoleApiDir]: ../../../console/api.md#dir "dir - Console API Reference | Documents Microsoft"  
[DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject]: ../../../console/utilities.md#recently-chosen-element-or-javascript-object "Élément ou objet JavaScript récemment choisi : référence de l’API des utilitaires de console | Documents Microsoft"  
[DevtoolsCssReferenceColorPicker]: ../../../css/reference.md#change-colors-with-the-color-picker "Modifier les couleurs à l'| Documents Microsoft"  
[DevtoolsDrawer]: ../../../customize/index.md#drawer "Drawer - Customize Overview | Documents Microsoft"  
[DevtoolsIndex]: ../../../index.md "Microsoft Edge outils de développement (Chromium) | Documents Microsoft"  
[DevtoolsIssuesIndex]: ../../../issues/index.md "Rechercher et résoudre les problèmes liés à l’Microsoft Edge’onglet Problèmes de DevTools | Documents Microsoft"  
[DevtoolsNetworkDetails]: ../../../network/index.md#inspect-the-details-of-the-resource "Inspecter les détails de la ressource | Documents Microsoft"  
[DevtoolsNetworkLog]: ../../../network/index.md#log-network-activity "Journal de l’activité réseau | Documents Microsoft"  
[DevtoolsRemoteDebugAndroid]: ../../../remote-debugging/index.md "Prise en main avec les appareils Android de débogage à distance | Documents Microsoft"  
[DevtoolsRemoteDebugDuoEmulator]: ../../../remote-debugging/surface-duo-emulator.md "Prise en main avec des émulateurs Surface Duo de débogage à distance | Documents Microsoft"  
[DevtoolsRemoteDebugWindows]: ../../../remote-debugging/windows.md "Prise en main le débogage à distance Windows 10 appareils | Documents Microsoft"  

[PwaIndex]: ../../../../progressive-web-apps-chromium/index.md "Applications web progressives sur Windows | Microsoft Docs"  

[DualScreensAndroidEmulator]: /dual-screen/android/use-emulator "Utiliser l’émulateur Surface Duo | Documents Microsoft"

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge Application Android"

[CaniuseMDNSpaceSeparatedFunctionalColorNotations]: https://caniuse.com/#feat=mdn-css_types_color_space_separated_functional_notation "Notations de couleur fonctionnelles séparées par des espaces : | Puis-je utiliser"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bogues Chromium"

[CR174309]: https://crbug.com/174309 "DevTools : autoriser la personnalisation des raccourcis clavier/des liaisons de touches | Chromium bogues"  
[CR963183]: https://crbug.com/963183 "Les devTools ne sont pas conformes AUX WCAG | Chromium bogues"  
[CR1040019]: https://crbug.com/1040019 "DevTools : afficher facilement un aperçu des images et des images d’arrière-plan dans le volet Styles | Chromium bogues"  
[CR1040025]: https://crbug.com/1040025 "DevTools : afficher les informations a11y de base dans la fenêtre de | Chromium bogues"  
[CR1048378]: https://crbug.com/1048378 "Prise en charge de l’interface utilisateur DevTools pour les | Chromium bogues"  
[CR1054381]: https://crbug.com/1054381 "CR 1054381 | Chromium bogues"  
[CR1068116]: https://crbug.com/1068116 "Ship issues panel | Chromium bogues"  
[CR1072952]: https://crbug.com/1072952 "DevTools: color picker should produce modern CSS color syntax | Chromium bogues"  
[CR1075437]: https://crbug.com/1075437 "DevTools : ajoutez la prise en charge du mot clé/valeur CSS « revert » | Chromium bogues"  
[CR1076112]: https://crbug.com/1076112 "Personnalisation des dévtools : resiseur de caisse"  
[CR1081486]: https://crbug.com/1081486 "Le focus du clavier n’est pas visible pour les boutons de navigation en mode de capture d’écran | Chromium bogues"  
[CRV86751]: https://bugs.chromium.org/p/v8/issues/detail?id=6751 "PromiseStatus doit être « rempli » et non « résolu » | Bogues V8"  

[CSSWGDraftsColor4Changes3]: https://drafts.csswg.org/css-color#changes-from-3 "Modifications apportées à Couleurs 3 - Module de couleur CSS niveau 4 | Brouillons de l’éditeur de groupe de travail CSS W3C"  
[CSSWGDraftsColor4Property]: https://drafts.csswg.org/css-color#the-color-property "3. Couleur de premier plan : la couleur - Module de couleur CSS niveau 4 | Brouillons de l’éditeur de groupe de travail CSS W3C"  

[DesktopEdge]: https://www.microsoft.com/edge/ "Présentation de la nouvelle Microsoft Edge"  

[GithubDomenicPromiseUnwrappingStatesFates]: https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md "États-et-Unis - domenic/promises-unwrapping | GitHub"  

[MDNRevert]: https://developer.mozilla.org/docs/Web/CSS/revert "| MDN"  
[MDNRevertBrowserCompatibility]: https://developer.mozilla.org/docs/Web/CSS/revert#Browser_compatibility "Compatibilité des navigateurs | MDN"  

[VisualStudioCodeMain]: https://code.visualstudio.com/ "Visual Studio Code"  
[VisualStudioCodeShortcuts]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio Code Raccourcis clavier pour Windows"  

[WebhintHintsAxeKeyboard]: https://webhint.io/docs/user-guide/hints/hint-axe/keyboard/ "Axe : clavier | WebHint"  
[WebhintHintsAxeNameRoleValue]: https://webhint.io/docs/user-guide/hints/hint-axe/name-role-value/ "Axe : valeur de rôle de nom | WebHint"  

[MicrosoftSupportWindows10HighContrastMode]: https://support.microsoft.com/help/4026951/windows-10-turn-high-contrast-mode-on-or-off "Activer ou désactiver le mode contraste élevé dans Windows | Windows prise en charge"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publier un Tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nouveau problème : MicrosoftDocs/edge-developer"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Microsoft Edge Canaux d’aperçu"  
[TheWebWeWantMain]: https://aka.ms/webwewant "Le site Web de votre choix"  

<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebdevCoreWebVitals]: https://alphabet-dev/vitals#core-web-vitals "Core Web Vitals | alphabet-dev"  -->  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developer.chrome.com/blog/new-in-devtools-84) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
