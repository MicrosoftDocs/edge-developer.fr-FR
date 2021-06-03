---
description: Les soulignements ondulés mettent en évidence les problèmes de code dans l’outil Éléments, la chronologie de mise à jour du service de travail, etc.
title: Nouveautés de DevTools (Microsoft Edge 91)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 5f499a6c9f1109f80a9d459edf94ed2226734f19
ms.sourcegitcommit: 87ba918b0910373bb645615377709bf140dc9b19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "11583458"
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
# <a name="whats-new-in-devtools-microsoft-edge-91"></a>Nouveautés de DevTools (Microsoft Edge 91)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="wavy-underlines-highlight-code-issues-and-improvements-in-elements-tool"></a>Les soulignements ondulés mettent en évidence les problèmes de code et les améliorations apportées à l’outil Elements  

<!--  Title: Get code hints in Elements tool  -->  
<!--  Subtitle: Wavy underlines like the ones you see in Visual Studio Code now display in the Elements tool.  Underlines alert you to code issues related to accessibility, compatibility, security, performance, and  so on.  -->  

Dans la plupart des IDE modernes, les soulignements ondulés sous le texte indiquent des erreurs de syntaxe.   Dans Microsoft Edge version 91 ou ultérieure, les soulignements ondulés s’affichent sous HTML dans la vue **DOM** de **l’outil Elements.**  Les soulignements ondulés indiquent des problèmes de code et des suggestions liés à l’accessibilité, la compatibilité, les performances, etc.  Pour plus d’informations sur la façon de passer en revue et de modifier les problèmes, accédez à Rechercher et résoudre les problèmes avec [l’outil Microsoft Edge DevTools Issues][DevtoolsIssuesIndex].  

Pour ouvrir **l’outil Problèmes** et en savoir plus sur le problème et comment le résoudre, effectuer l’une des actions suivantes.  

*   Sélectionnez et `Shift` maintenez, puis choisissez un soulignement ondulé.  
*   Effectuer les actions suivantes.  
    1.  Pointez sur n’importe quel soulignement ondulé.  
    1.  Ouvrez le menu contextuel \(cliquez avec le bouton droit\).  
    1.  Choose **Show in Issues**.  
        
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues.msft.png" alt-text="Choisir l’erreur soulignée dans l’outil Éléments" lightbox="../../media/2021/04/elements-iframe-highlight-issues.msft.png":::
         Choisir l’erreur soulignée dans **l’outil Éléments**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png" alt-text="Afficher les détails des erreurs dans l’outil Problèmes" lightbox="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png":::
         Afficher les détails des erreurs dans **l’outil Problèmes**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a>En savoir plus sur DevTools grâce à des infobulles informatives  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<!--  Title: Learn more about DevTools with DevTools Tooltips  -->  
<!--  Subtitle: Informative overlays are now available in the default DevTools interface.  -->  

La fonctionnalité d’outils DevTools vous permet d’en savoir plus sur les différents outils et volets de DevTools.  Pour désactiver les bulles, sélectionnez `Esc` .  Pour activer les bulles, effectuer l’une des actions suivantes.  

*   Sélectionnez `Ctrl` + `Shift` + `H` \(Windows/Linux\) ou `Cmd` + `Shift` + `H` \(macOS\).  
*   [Ouvrez le menu Commande,][DevtoolsCommandMenuIndexOpenCommandMenu] puis tapez `tooltips` .  
*   Choose **Customize and control DevTools** \( `...` \) > **Help**  >  **Toggle the DevTools Tooltips**.  

En outre, si vous activer le mode Focus et l’expérience d’bulles d’outils [DevTools,][DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode] vous pouvez également choisir le bouton Basculer le bouton d’outils **DevTools** \( \) en bas de la barre `?` d’activité. ****  

Pour afficher plus d’informations sur l’utilisation de DevTools, allumez les info-bulles, puis pointez sur chaque région en plan des DevTools.  

:::image type="complex" source="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png" alt-text="Pointez n’importe où dans la région mise en surbrillez de l’outil Problèmes pour afficher plus de détails" lightbox="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png":::
   Pointez n’importe où dans **** la région mise en surbrillez de l’outil Problèmes pour afficher plus de détails  
:::image-end:::  

## <a name="service-worker-update-timeline"></a>Chronologie de mise à jour du service de travail  

<!--todo:  Update the linked [Service Worker improvements][DevtoolsServiceWorkerIndex] article.  -->  

<!--  Title: The tasks associated with your Service Worker  -->  
<!--  Subtitle: Debug with Service Worker Update Cycle  -->  

Dans Microsoft Edge version 91 ou ultérieure, si vous êtes développeur Progressive Web App ou Service Worker, affichez le cycle de vie de mise à jour de vos employés de service sous forme de chronologie dans l’outil **Application.**  Cette fonctionnalité vous permet de comprendre le temps que votre service de travail passe à chacune des étapes suivantes.  

*   **Install**  
*   **Attendre**  
*   **Activer**  
    
:::image type="complex" source="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png" alt-text="Passer en revue la chronologie du cycle de mise à jour pour votre service de travail" lightbox="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png":::
   Passer en revue **la chronologie** du cycle de mise **à jour** pour votre service de travail  
:::image-end:::  

Pour plus d’informations sur le cycle de vie de vos employés de service, accédez au cycle de vie des travailleurs [de service.][ProgressiveWebAppsServiceworkerServiceWorkerLifecycle]  Pour plus d’informations sur les outils de débogage pour les applications web progressives et les travailleurs de service dans DevTools, accédez aux améliorations apportées aux services [de travail.][DevtoolsServiceWorkerIndex]  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans Chromium projet open source, accédez au problème [1066604][CR1066604].  

## <a name="progressive-web-apps-no-longer-display-warnings-for-non-square-icons"></a>Les applications web progressives n’affichent plus d’avertissements pour les icônes non carrées  

<!--  Title: Non-square icons in app manifest no longer produce warnings  -->  
<!--  Subtitle: As long as square icons are included in the app manifest, non-square icons no longer produce warnings  -->  

Dans [Microsoft Edge version 90][DevtoolsWhatsNew202102Devtools] ou antérieure, si le manifeste d’application web de votre PWA incluait une icône non carrée, un avertissement s’affichait dans la section Erreurs et **avertissements** pour chaque icône non carrée.  Dans Microsoft Edge version 91 ou ultérieure, la **section** Manifeste de l’outil **Application** n’affiche aucun avertissement si vous fournissez au moins une icône carrée.  Si vous ne fournissez aucune icône carrée, un avertissement affiche le message suivant.  

```output
Most operating systems require square icons.  Please include at least one square icon in the array.  
```  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png" alt-text="Dans Microsoft Edge version 90 ou antérieure, une erreur s’affiche pour chaque icône non carrée" lightbox="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png":::
         Dans Microsoft Edge version 90 ou antérieure, une erreur s’affiche pour chaque icône non carrée  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png" alt-text="Dans Microsoft Edge version 91 ou ultérieure, aucune erreur ne s’affiche lorsque vous fournissez au moins une icône carrée" lightbox="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png":::
         Dans Microsoft Edge version 91 ou ultérieure, aucune erreur ne s’affiche lorsque vous fournissez au moins une icône carrée  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Pour passer en revue les erreurs et les avertissements dans votre manifeste d’application web, accédez à l’outil **Application** et choisissez la section **Manifeste.**  Les erreurs et avertissements sont répertoriés sous le titre **Erreurs et avertissements.**  Pour plus d’informations sur le manifeste d’application web, accédez à Utiliser le manifeste d’application web pour intégrer votre application Web progressive [dans le système d’exploitation.][ProgressiveWebAppsWebappmanifests]  Pour créer des icônes à inclure dans votre manifeste d’application web, accédez au générateur [d’images PWABuilder.][PwabuilderImagegenerator]  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans le projet open source Chromium, accédez à Problème [1185945][CR1185945].  

## <a name="localized-devtools-now-supported-in-chromium-based-browsers"></a>DevTools localisées désormais prise en charge dans Chromium navigateurs basés sur les navigateurs  

<!--  Title: Localization for all  -->  
<!--  Subtitle: Match browser language enabled to all Chromium-based browsers  -->  

À partir [Microsoft Edge version 81,][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages]Microsoft Edge DevTools s’affiche dans votre propre langue.  De nombreux développeurs utilisent d’autres outils de développement tels que StackOverflow et Visual Studio Code dans leur langue native, et pas seulement en anglais.  L Microsoft Edge’équipe DevTools, l’équipe Chrome DevTools et l’équipe Google Chrome ont travaillé pour offrir la même expérience dans tous les navigateurs basés sur Chromium.  Pour plus d’informations sur l’utilisation de DevTools dans votre langue, accédez à Modifier les paramètres de langue [de DevTools.][DevtoolsCustomizeLocalization]  Pour plus d’informations sur la collaboration sur cette fonctionnalité dans le projet open source Chromium, accédez à [1136655][CR1136655].  

:::image type="complex" source="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png" alt-text="Microsoft Edge navigateur et DevTools sont définies sur japonais" lightbox="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png":::
   Microsoft Edge navigateur et DevTools sont définies sur japonais  
:::image-end:::  

## <a name="use-the-keyboard-to-navigate-to-css-variables"></a>Utiliser le clavier pour accéder aux variables CSS  

<!--  Title: Navigate to CSS variables with the arrow keys  -->  
<!--  Subtitle: In the Styles pane, use the arrow keys to choose CSS variables.  Select `Enter` to see the variable definition.  -->  

À partir [Microsoft Edge version 88,][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]le volet **Styles** affiche les variables CSS et fournit un lien directement vers la définition de chaque variable.  Dans Microsoft Edge version 91 ou ultérieure, vous pouvez utiliser les touches de direction pour accéder facilement aux variables CSS.  Pour ouvrir la définition dans le volet **Styles,** pointez sur une variable, puis sélectionnez `Enter` .  Pour plus d’informations sur les variables CSS, accédez à [l’utilisation de propriétés personnalisées CSS (variables).][MdnDocsWebCssUsingCssCustomProperties]  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans le projet open source Chromium, accédez à Problème [1187735][CR1187735].  

:::image type="complex" source="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png" alt-text="Variable CSS --theme-body-background mise en évidence dans le volet Styles" lightbox="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png":::
   Variable `--theme-body-background` CSS mise en évidence dans le **volet Styles**  
:::image-end:::  

## <a name="issues-are-automatically-sorted-by-severity"></a>Les problèmes sont automatiquement triés par gravité  

<!-- Title: Display Issues in severity order  -->  
<!-- Subtitle: Entries in the Issues tool now display in severity order and allow you to focus your updates on the most important issues. -->  

**L’outil Problèmes** affiche des recommandations pour améliorer votre site web, notamment l’accessibilité, les performances, la sécurité, etc. En fonction de vos commentaires, les problèmes sont désormais automatiquement triés par gravité.  Dans chaque catégorie de commentaires, **** chaque problème marqué comme erreur apparaît en premier, suivi de chaque problème marqué comme **avertissement,** puis de chaque problème marqué comme **conseil.**  Pour vous aider à affiner vos problèmes, des options de filtre supplémentaires sont prévues pour une prochaine mise à jour.  Pour plus d’informations sur la façon de passer en revue les problèmes, accédez à Rechercher et résoudre les problèmes avec [l’outil Microsoft Edge DevTools Issues][DevtoolsIssuesIndex].  

:::image type="complex" source="../../media/2021/04/elements-issues-ordered-issues.msft.png" alt-text="L’outil Problèmes affiche les problèmes triés par gravité" lightbox="../../media/2021/04/elements-issues-ordered-issues.msft.png":::
   **L’outil Problèmes** affiche les problèmes triés par gravité  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-117"></a>Microsoft Edge Outils de développement Visual Studio Code version 1.1.7  

<!-- Title: Microsoft Edge DevTools for Visual Studio version 1.1.7  -->  
<!-- Subtitle: Increased target closure reliability, automatically update the side panel, new contextual menu for settings and Changelog, and more. -->  

Les [outils][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] Microsoft Edge pour Visual Studio Code version 1.1.7 fournissent les outils DevTools de [Microsoft Edge version 88.][DevtoolsWhatsNew202011Devtools]  Cette extension prend désormais en charge ARM et ne dépend plus du débogger [pour Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerForEdge] extension.  La version 1.1.7 inclut les correctifs et améliorations de bogue suivants.  

*   Mise à jour de la fiabilité de la fermeture cible.  
*   Mise à jour du panneau latéral pour qu’il soit actualisé automatiquement lorsque vous déboguer des cibles créées ou détruites.  
*   Ajout d’un nouveau menu contextuel qui vous permet d’accéder plus rapidement aux paramètres d’extension et au dernier changelog.  
*   Mise à jour et simplification de la publication de la documentation d’extension, y compris les fonctionnalités les plus nouvelles.  
    
Pour mettre à jour manuellement la version 1.1.7, accédez à Mettre à jour [une extension manuellement.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  Vous pouvez signaler des problèmes, puis contribuer à l’extension sur le référentiel [GitHub vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools].  

## <a name="announcements-from-the-chromium-project"></a>Annonces du projet de Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="visualize-css-scroll-snap"></a>Afficher l’achemin de défilement CSS  

Vous pouvez maintenant faire bascule le badge dans l’outil Elements pour inspecter l’alignement de l’alignement en `scroll-snap` défilement CSS. ****  Lorsqu’un élément HTML de votre page web s’y est appliqué, un badge s’affiche à côté de `scroll-snap-type` `scroll-snap` celui-ci dans **l’outil Elements.**  Choisissez le badge pour activer \(ou désactiver\) l’affichage d’une superposition d’un défilement sur la page web.  Pour consulter un exemple de page web, [accédez à Scroll Ancrer Demo][GlitchMicrosoftEdgeChromiumDevtoolsCssDbgStoriesCssScrollSnapHtml].  Dans l’exemple, les points s’affichent sur les bords en snap.  Le port de défilement a un plan plein tandis que les éléments d’a snap ont des tirets.  Le remplissage de défilement est rempli en vert tandis que la marge de défilement est remplie en orange.  Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez au problème [862450][CR862450].  

:::image type="complex" source="../../media/2021/04/elements-scroll-snap-highlight.msft.png" alt-text="CSS scroll-snap" lightbox="../../media/2021/04/elements-scroll-snap-highlight.msft.png":::
   CSS scroll-snap  
:::image-end:::  

### <a name="new-memory-inspector-tool"></a>Nouvel outil Inspecteur de mémoire  

Utilisez le nouvel outil **Inspecteur de** mémoire pour inspecter une `ArrayBuffer` mémoire JavaScript et Wasm.  Ouvrez la [page web de démonstration Mémoire dans JS.][GlitchMemoryInspectorDemoJsHtml]  Dans **l’outil Sources,** ouvrez `memory-write-wasm` le fichier et définissez un point d’arrêt à la `0x03c` ligne.  Actualisez la page web.  Développez la section **Étendue** dans le volet débogger.  La nouvelle icône s’affiche à côté de la valeur **de la mémoire** tampon.  Choisissez-le pour ouvrir le nouvel outil **Inspecteur de** mémoire.  

Pour en savoir plus sur le débogage dans l’outil **Sources,** accédez au volet Utilisation du déboguer pour déboguer du [code JavaScript.][DevtoolsSourcesUsingDebuggerPaneToDebugJavascriptCode]  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problème [1166577][CR1166577].  

:::image type="complex" source="../../media/2021/04/sources-memory-write-wasm-breakpoint-scope-reveal-in-memory-inspector-panel.msft.png" alt-text="Outil Inspecteur de mémoire" lightbox="../../media/2021/04/sources-memory-write-wasm-breakpoint-scope-reveal-in-memory-inspector-panel.msft.png":::
   **Outil Inspecteur de** mémoire  
:::image-end:::  

### <a name="new-badge-settings-pane-in-the-elements-tool"></a>Volet Nouveaux paramètres de badge dans l’outil Éléments  

À présent, utilisez les **paramètres de badge dans** l’outil **Éléments** pour activer \(ou désactiver\) les badges individuels.  Utilisez cette fonctionnalité pour personnaliser et rester concentré sur les badges importants pendant que vous inspectez les pages web.  Pour afficher le volet des paramètres de badge en haut de l’outil **Éléments,** effectuer les actions suivantes.  

1.  Pointez sur n’importe quel élément.  
1.  Ouvrez le menu contextuel \(cliquez avec le bouton droit\).  
1.  Choisissez **les paramètres de badge...**.  
    
Pour afficher \(ou masquer\) les badges, sélectionnez \(ou supprimez\) la case à cocher en regard du nom du badge.  

<!--  To review the history of this feature in the Chromium open-source project, navigate to Issue [1066772][CR1066772].  -->  

:::image type="complex" source="../../media/2021/04/elements-contextual-menu-badge-settings.msft.png" alt-text="Volet Paramètres du badge dans l’outil Éléments" lightbox="../../media/2021/04/elements-contextual-menu-badge-settings.msft.png":::
   **Volet Paramètres du** badge dans l’outil **Éléments**  
:::image-end:::  

### <a name="enhanced-image-preview-with-aspect-ratio-information"></a>Aperçu d’image amélioré avec des informations sur les proportions  

Les aperçus d’image dans devTools ont été améliorés pour afficher plus d’informations, notamment les détails suivants.  

*   Taille rendue  
*   Proportions rendues  
*   Taille intrinsèque  
*   Proportions intrinsèques  
*   Taille du fichier  
    
Ces informations vous aident à mieux comprendre vos images et à appliquer l’optimisation.  Les informations sur les proportions d’image sont également disponibles dans l’outil **Réseau,** lorsque vous choisissez un aperçu d’image.  

:::row:::
   :::column span="":::
      Dans **l’outil Éléments,** l’aperçu d’image affiche désormais plus d’informations sur l’image.  
   :::column-end:::
   :::column span="":::
      En outre, les informations sur les proportions d’image sont disponibles dans l’outil **Réseau,** lorsque vous choisissez un aperçu d’image.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-inspect-image-src-hover-preview.msft.png" alt-text="Aperçu d’image avec des informations sur les proportions dans l’outil Element" lightbox="../../media/2021/04/elements-inspect-image-src-hover-preview.msft.png":::
         Aperçu d’image avec des informations sur les proportions dans **l’outil Element**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/network-img-name-filters-preview.msft.png" alt-text="Informations sur les proportions d’image dans l’outil Réseau" lightbox="../../media/2021/04/network-img-name-filters-preview.msft.png":::
         Informations sur les proportions d’image dans **l’outil** Réseau  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problèmes [1149832][CR1149832] et [1170656][CR1170656].  

### <a name="new-options-to-configure-content-encodings-in-the-network-conditions-tool"></a>Nouvelles options de configuration des codages de contenu dans l’outil Conditions réseau 

Dans **l’outil** Réseau, sélectionnez le nouveau **** bouton Plus **de conditions réseau...** en haut du menu déroulant Limitation pour ouvrir l’outil **Conditions réseau.**  Pour tester si les réponses du serveur sont correctement codées pour les navigateurs qui ne peuvent pas prendre en charge [gzip,][GnuSoftwareGzipManual] [brotli][|::ref1::|Main]ou un autre futur, effectuer les `Content-Encoding` actions suivantes.  

1.  Ouvrir **l’outil Conditions réseau**
1.  Accédez **à Encodages de contenu acceptés.** 
1.  Supprimez la case à cocher en regard `Content-Encoding` de la case à cocher que vous souhaitez tester.  
    
Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez à Problème [1162042][CR1162042].  

:::image type="complex" source="../../media/2021/04/network-more-network-conditions-accepted-content-encodings.msft.png" alt-text="Nouvelles conditions réseau... ouvre l’outil Conditions réseau pour configurer l’encodage de contenu" lightbox="../../media/2021/04/network-more-network-conditions-accepted-content-encodings.msft.png":::
   Le **bouton Nouvelles conditions réseau...** ouvre l’outil **Conditions** réseau à configurer `Content-Encoding`  
:::image-end:::  

### <a name="styles-pane-enhancements"></a>Améliorations apportées au volet Styles  

#### <a name="new-shortcut-to-display-computed-value-in-the-styles-pane"></a>Nouveau raccourci pour afficher la valeur calculée dans le volet Styles  

Maintenant, pour afficher la valeur CSS calculée dans le volet **Styles,** effectuer les actions suivantes.  

1.  Pointez sur une propriété CSS.  
1.  Ouvrez le menu contextuel \(cliquez avec le bouton droit\).  
1.  Choose **View computed value**.  
    
Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problème [1076198][CR1076198].  

:::image type="complex" source="../../media/2021/04/elements-styles-highlight-view-computed-value.msft.png" alt-text="Nouveau raccourci pour afficher la valeur calculée" lightbox="../../media/2021/04/elements-styles-highlight-view-computed-value.msft.png":::
   Nouveau raccourci pour afficher la valeur calculée  
:::image-end:::  

#### <a name="support-for-the-accent-color-keyword"></a>Prise en charge du mot clé accent-color  

L’interface utilisateur de la mise à jour automatique du volet **Styles** détecte désormais le mot clé CSS, qui vous permet de spécifier la couleur d’accentuence pour les contrôles d’interface utilisateur générés par `accent-color` l’élément.  Les contrôles d’interface utilisateur générés par un élément sont, par exemple, des case à cocher ou des boutons d’radio. Pour plus d’informations sur l’état de l Chromium l’implémentation, accédez à Fonctionnalité : propriété CSS de couleur [accentuée.][ChromestatusFeature4752739957473280]  Pour activer cette fonctionnalité, accédez à la case à cocher et définissez-la `edge://flags#enable-experimental-web-platform-features` **sur Activé.**  Pour passer en revue l’historique de cette fonctionnalité dans le Chromium open source, accédez à Problème [1092093][CR1092093].  

:::image type="complex" source="../../media/2021/04/elements-styles-accent-color.msft.png" alt-text="mot clé CSS de couleur d’accent" lightbox="../../media/2021/04/elements-styles-accent-color.msft.png":::
   `accent-color` Mot clé CSS
:::image-end:::  

### <a name="display-details-about-blocked-features-in-the-frame-details-view"></a>Afficher les détails sur les fonctionnalités bloquées dans l’affichage Détails de l’image  

La stratégie d’autorisations est une API de plateforme web qui permet à un site web d’autoriser ou de bloquer l’utilisation des fonctionnalités de navigateur dans une image individuelle ou dans un site qu’il `iframe` incorpore. Pour plus d’informations, [accédez à l’Explication de la stratégie d’autorisations.][GithubW3cWebappsecPermissionsPolicyPermissionsPolicyExplainerMd]  Pour afficher les détails sur la raison pour laquelle une fonctionnalité est bloquée, effectuer les actions suivantes.  

1.  Accédez à [stratégie d’autorisations OOPIF.][GlitchPermissionPolicyDemoMain]  
1.  Accédez à **l’outil Application.**  
1.  Choisissez un cadre.  
1.  Accédez à la section **Stratégie des autorisations.**  
1.  Accédez à la **propriété Fonctionnalités désactivées.**  
1.  Choose **Show details**.  
1.  Sélectionnez l’icône en fonction de chaque stratégie pour accéder à la demande réseau qui `iframe` a bloqué la fonctionnalité.  
    
Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problème [1158827][CR1158827].  

:::image type="complex" source="../../media/2021/04/application-frames-top-permission-policy-disabled-features-show-details-highlight.msft.png" alt-text="Fonctionnalités bloquées dans l’affichage Détails de l’image" lightbox="../../media/2021/04/application-frames-top-permission-policy-disabled-features-show-details-highlight.msft.png":::
   Fonctionnalités bloquées dans l’affichage Détails de l’image  
:::image-end:::  

### <a name="filter-experiments-in-the-experiments-setting"></a>Filtrer les expériences dans le paramètre Expériences  

Recherchez des expériences plus rapidement avec le nouveau filtre d’expérience.  Par exemple, pour activer de nouvelles expériences pour les problèmes de code, effectuer les actions suivantes.
``

1.  Accédez **à Paramètres**  >  **expériences.**  
1.  Accédez à la **boîte de** texte Filtrer.  
1.  Tapez `issues`.  
    
:::image type="complex" source="../../media/2021/04/settings-experiments-filter-by-issues.msft.png" alt-text="Filtrer les expériences dans le paramètre Expériences" lightbox="../../media/2021/04/settings-experiments-filter-by-issues.msft.png":::
   Filtrer les expériences dans le **paramètre Expériences**  
:::image-end:::  

### <a name="new-vary-header-column-in-the-cache-storage-pane"></a>Nouvelle colonne d’en-tête Vary dans le volet de stockage du cache  

Utilisez la nouvelle colonne dans le volet Stockage cache pour afficher les valeurs d’en-tête de réponse `Vary Header` HTTP [Vary.][HttpwgSpecsRfc7231HtmlHeaderVary] ****  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problème [1186049][CR1186049].  

:::image type="complex" source="../../media/2021/04/application-cache-cache-storage-highlighted-vary-header.msft.png" alt-text="Colonne d’en-tête Vary" lightbox="../../media/2021/04/application-cache-cache-storage-highlighted-vary-header.msft.png":::
   Colonne d’en-tête Vary  
:::image-end:::  

### <a name="sources-tool-improvements"></a>Améliorations apportées à l’outil Sources  

#### <a name="support-for-new-javascript-features"></a>Prise en charge des nouvelles fonctionnalités JavaScript  

DevTools désormais prise en charge de la nouvelle marque privée [contrôles a.k.a.][V8DevFeaturesPrivateBrandChecks] #foo en javaScript obj fonctionnalité de langage.  La fonctionnalité de vérification de marque privée étend [l’opérateur in][MdnDocsWebJavascriptReferenceOperatorsIn] pour prendre en charge [les champs de classe Privé][V8DevFeaturesClassFieldsPrivateClassFields] sur un objet spécifique.  Essayez-le dans les **outils Console** **et Sources.**  En outre, pour inspecter les champs privés, effectuer les actions suivantes.  

1.  Accédez **au volet débogger.**  
1.  Accédez à la section **Étendue.**  
    
Pour passer en revue l’historique de cette fonctionnalité dans Chromium projet open source, accédez au problème [11374][CR11374].  

:::image type="complex" source="../../media/2021/04/sources-page-pen-js-breakpoint-scope-script-dog.msft.png" alt-text="Vérifications de marque privée JavaScript" lightbox="../../media/2021/04/sources-page-pen-js-breakpoint-scope-script-dog.msft.png":::
   Vérifications de marque privée JavaScript  
:::image-end:::  

#### <a name="enhanced-support-for-breakpoints-debugging"></a>Prise en charge améliorée du débogage des points d’arrêt  

Les bundlers JavaScript modernes tels que [Webpack][WebpackJsMain]et [Rollup][RollupjsMain] prise en charge le fractionnement de code.  Pour en savoir plus sur le fractionnement de code, accédez [au fractionnement de code.][JsWebpackGuidesCodeSplittingTextThereAreThreeGeneralApproachesToCodeSplittingSplitCodeViaInlineFunctionCallsWithinModules]  Dans Microsoft Edge version 90 ou antérieure, DevTools ne définisse les points d’arrêt que dans un seul ensemble.  Dans Microsoft Edge version 91 ou ultérieure, DevTools définit correctement les points d’arrêt dans plusieurs groupes lorsque vous déboguer un composant partagé.  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problèmes [1142705][CR1142705], [979000][CR979000]et [1180794][CR1180794].  

#### <a name="support-hover-preview-with-bracket-notation"></a>Prise en charge de l’aperçu de pointage avec une notation entre crochets  

DevTools désormais la prise en charge de l’aperçu de pointage sur les expressions de membre JavaScript qui utilisent la `[]` notation dans **l’outil Sources.**  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problème [1178305][CR1178305].  

:::image type="complex" source="../../media/2021/04/sources-page-pen.js-breakpoint-arr-i-a.msft.png" alt-text="Prise en charge de l’aperçu de pointage avec notation []" lightbox="../../media/2021/04/sources-page-pen.js-breakpoint-arr-i-a.msft.png":::
   Prise en charge de l’aperçu de pointage avec `[]` notation  
:::image-end:::  

#### <a name="improved-outline-of-html-files"></a>Amélioration du plan des fichiers HTML  

DevTools dispose désormais d’une meilleure prise en charge de plan pour les `.html` fichiers.  Dans **l’outil Sources,** ouvrez le `.html` fichier.  Pour activer \(ou désactiver\) le plan de code, sélectionnez `Ctrl` + `Shift` + `O` Windows/Linux `Cmd` + `Shift` + `O` ou sur macOS.  Dans la figure suivante, DevTools liste maintenant correctement toutes les fonctions dans le plan.  Auparavant, DevTools affichait uniquement certaines fonctions.  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problèmes [761019][CR761019] et [1191465][CR1191465].  

:::image type="complex" source="../../media/2021/04/sources-page-jobobbx-at.msft.png" alt-text=" Amélioration du plan des fichiers HTML" lightbox="../../media/2021/04/sources-page-jobobbx-at.msft.png":::
   Amélioration du plan des fichiers HTML  
:::image-end:::  

#### <a name="proper-error-stack-traces-for-wasm-debugging"></a>Traces de pile d’erreurs correctes pour le débogage Wasm  

Dans Microsoft Edge version 90 ou antérieure, DevTools affichait uniquement des références Wasm génériques dans les traces de pile d’erreurs.  Dans Microsoft Edge version 91 ou ultérieure, DevTools résout les demandes de fonction en ligne et affiche l’emplacement source dans les traces de pile d’erreurs pour le débogage Wasm.  Pour en savoir plus sur les traces de pile d’erreurs dans la **console,** accédez à [erreur.][DevtoolsConsoleApiError]  

Dans Microsoft Edge version 91 ou ultérieure, DevTools résout les demandes de fonction en ligne et affiche les traces de pile d’erreurs correctes pour le débogage Wasm.  

:::row:::
   :::column span="":::
      Dans Microsoft Edge version 90 et antérieures, l’emplacement source ne s’affiche pas dans les traces de pile d’erreurs.  Les emplacements sources incluent `dsquare` .  
   :::column-end:::
   :::column span="":::
      Dans Microsoft Edge version 91 et ultérieures, l’emplacement source s’affiche dans les traces de pile d’erreurs.
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error-old.msft.png" alt-text="Traces de pile d’erreurs précédentes pour le débogage Wasm" lightbox="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error-old.msft.png":::
         Traces de pile d’erreurs correctes pour le débogage Wasm  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error.msft.png" alt-text="Traces de pile d’erreurs correctes pour le débogage Wasm" lightbox="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error.msft.png":::
         Traces de pile d’erreurs correctes pour le débogage Wasm  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problème [1189161][CR1189161].  

## <a name="download-the-microsoft-edge-preview-channels"></a>Télécharger les canaux d’aperçu Microsoft Edge  

Si vous êtes sous Windows, Linux ou macOS, envisagez d'utiliser les [canaux d'aperçu de Microsoft][MicrosoftEdgePreviewChannels] Edge comme navigateur de développement par défaut.  Les canaux de prévisualisation vous donnent accès aux dernières fonctionnalités de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Contacter l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages]: ../../2020/01/devtools.md#using-the-devtools-in-other-languages "Utilisation de DevTools dans d’autres langues : nouveautés de DevTools (Microsoft Edge 81) | Documents Microsoft"  
[DevtoolsWhatsNew202011Devtools]: ../../2020/11/devtools.md "Nouveautés de DevTools (Microsoft Edge 88) | Documents Microsoft"  
[DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]: ../../2020/11/devtools.md#css-variable-definitions-in-styles-pane "Définitions de variables CSS dans le volet Styles - Nouveautés de DevTools (Microsoft Edge 88) | Documents Microsoft"  
[DevtoolsWhatsNew202102Devtools]: ../02/devtools.md "Nouveautés de DevTools (Microsoft Edge 90) | Documents Microsoft"  
[DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode]: ../02/devtools.md#group-tools-together-in-focus-mode "Group tools together in Focus Mode - What’s New In DevTools (Microsoft Edge 90) | Documents Microsoft"  

[DevtoolsCommandMenuIndexOpenCommandMenu]: ../../../command-menu/index.md#open-the-command-menu "Ouvrez le menu Commande - Exécutez les commandes avec le menu Microsoft Edge commande DevTools | Documents Microsoft"  
[DevtoolsConsoleApiError]: ../../../console/api.md#error "error - Console API reference | Documents Microsoft"  
[DevtoolsCustomizeLocalization]: ../../../customize/localization.md "Modifier les paramètres de langue de DevTools | Microsoft Docs"  
[DevtoolsIssuesIndex]: ../../../issues/index.md "Recherchez et corrigez les problèmes liés à l’outil des problèmes de Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsServiceWorkerIndex]: ../../../service-workers/index.md "Améliorations apportées aux services | Documents Microsoft"  
[DevtoolsSourcesUsingDebuggerPaneToDebugJavascriptCode]: ../../../sources/index.md#using-the-debugger-pane-to-debug-javascript-code "Utilisation du volet Déboguer le code JavaScript - Sources : vue d’ensemble de l’outil | Documents Microsoft"  

[ProgressiveWebAppsServiceworkerServiceWorkerLifecycle]: ../../../../progressive-web-apps-chromium/serviceworker.md#the-service-worker-lifecycle "Cycle de vie des travailleurs du service : utiliser les travailleurs de service pour gérer les demandes réseau et les notifications Push | Documents Microsoft"  
[ProgressiveWebAppsWebappmanifests]: ../../../../progressive-web-apps-chromium/webappmanifests.md "Utiliser le manifeste d’application web pour intégrer votre application Web progressive au système d’exploitation | Documents Microsoft"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
<!--[GithubMicrosoftVscodeEdgeDevtoolsPullxxx]: https://github.com/microsoft/vscode-edge-devtools/pull/xxx "Pull xxx: Lorem al Ipsum | GitHub"  -->  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux de préversion de Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Mettre à jour une extension manuellement - Extension Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Outils Microsoft Edge pour Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerForEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Débogueur pour Microsoft Edge | Visual Studio Marketplace"  

[BrotliMain]: https://www.brotli.org "Brotli"  

[ChromestatusFeature4752739957473280]: https://chromestatus.com/feature/4752739957473280 "Fonctionnalité : propriété CSS de couleur d’accentu | État de la plateforme Chrome"  

[CsswgDraftsCssUi4WidgetAccent]: https://drafts.csswg.org/css-ui-4/#widget-accent "Couleurs d’accentuage de widget : propriété couleur d’accentuage - Module d’interface utilisateur de base CSS niveau 4 | Brouillons de l’éditeur de groupe de travail CSS"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bogues Chromium"  
[CR11374]: https://crbug.com/v8/11374 "Problème 11374 : implémenter la vérification de marque d’une marque d’une marque pour les champs privés"  
[CR761019]: https://crbug.com/761019 "Problème 761019 : « Passer au symbole » rate la première fonction et préfère une correspondance pire si elle contient tous les caractères tapés"  
[CR862450]: https://crbug.com/862450 "Problème 862450 : [css-scroll-snap] Envisagez d’ajouter la fonctionnalité Devtools pour l’snap de défilement css"  
[CR979000]: https://crbug.com/979000 "Problème 979000 : les cartes sources avec des chemins d’accès aux sources entrent en conflit ne fonctionnent pas."  
[CR1066604]: https://crbug.com/1066604 "Problème 1066604 : DevTools : voir les détails sur l’installation et l’activation des événements par ServiceWorker | Chromium bogues"  
<!--  [CR1066772]: https://crbug.com/1066772 "Issue 1066772: "  locked  -->  
[CR1076198]: https://crbug.com/1076198 «Problème 1076198: [Feature Request] Jump to computed property from `styles` tab»  
[CR1092093]: «Problème 1092093 : rendre les contrôles de formulaire plus color-stylables en appuyant sur la propriété CSS « accent-color » » https://crbug.com/1092093  
[CR1136655] : « Problème https://crbug.com/1136655 1136655 : Devtools : localisation v2 | Chromium bogues »  
[CR1142705]: «Problème 1142705 : les points d’arrêt cessent de fonctionner lorsque 2 sourcesmaps pointent vers le même fichier virtuel lors de l’utilisation de https://crbug.com/1142705 webpack»  
[CR1149832]: «Problème 1149832 : Demande de fonctionnalité : l’aperçu d’image doit également afficher la taille https://crbug.com/1149832 du fichier»  
[CR1158827]: «Problème 1158827 : [Stratégie d’autorisations] Implémenter la prise en charge de devtool pour la stratégie https://crbug.com/1158827 d’autorisations»  
[CR1162042]: «Problème 1162042 : DevTools : prise en charge de la désactivation du codage de contenu https://crbug.com/1162042 gzip/brotli/jxl»  
[CR1166577]: https://crbug.com/1166577 «Problème 1166577 : ☂️ Linear Memory Inspector 1.0»  
[CR1170656]: https://crbug.com/1170656 «Problème 1170656 : afficher les proportions intrinsèques»  
[CR1178305]: «Problème 1178305 : le débogger n’affiche pas la valeur de propriété https://crbug.com/1178305 d’un élément indexé lorsqu’il est survolé»  
[CR1180794] : « Problème 1180794 : les points d’arrêt ne fonctionnent pas avec l’optimisation du compilateur de https://crbug.com/1180794 fermeture »  
[CR1185945]: «Problème 1185945 : l’avertissement de manifeste implique que toutes les icônes doivent être https://crbug.com/1185945 carrées | Chromium bogues »  
[CR1186049] : « Problème 1186049 : Colonne pour Vary : en-tête dans la visionneuse Stockage https://crbug.com/1186049 cache »  
[CR1187735]: https://crbug.com/1187735 «Problème 1187735 : Accessibilité : MAS2.1.1 : Clavier : Impossible d’appeler la fonction « Var(..) » à l’aide du clavier | Chromium bogues »  
[CR1189161]: https://crbug.com/1189161 «Problème 1189161 : les stacktraces ne sont pas `new Error` transformés via LAXIT»  
[CR1191465]: https://crbug.com/1191465 «Problème 1191465 : Ctrl+Shift+O rompu sur HTML»  

[GithubW3cWebappsecPermissionsPolicyPermissionsPolicyExplainerMd]: https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md "Explication de la stratégie d'autorisation | GitHub"  

[GlitchMemoryInspectorDemoJsHtml]: https://memory-inspector.glitch.me/demo-js.html "Mémoire dans les | JS Glitch"  
[GlitchMemoryInspectorDemoWasmHtml]: https://memory-inspector.glitch.me/demo-wasm.html "Mémoire dans wasm | Glitch"  

[GlitchMicrosoftEdgeChromiumDevtoolsCssDbgStoriesCssScrollSnapHtml]: https://microsoft-edge-chromium-devtools.glitch.me/css-dbg-stories/css-scroll-snap.html "Scroll Ancrer Demo | Glitch"  

[GlitchPermissionPolicyDemoMain]: http://permission-policy-demo.glitch.me "Stratégie d’autorisations OOPIF | Glitch"  

[GnuSoftwareGzipManual]: https://www.gnu.org/software/gzip/manual "gzip : programme de compression de | Système d’exploitation GNU"  

[HttpwgSpecsRfc7231HtmlHeaderVary]: https://httpwg.org/specs/rfc7231.html#header.vary "Vary - Protocole HTTP (Hypertext Transfer Protocol) : sémantique et contenu | Groupe de travail HTTP IETF"  

[JsWebpackGuidesCodeSplittingTextThereAreThreeGeneralApproachesToCodeSplittingSplitCodeViaInlineFunctionCallsWithinModules]: https://webpack.js.org/guides/code-splitting/#:~:text=There%20are%20three%20general%20approaches%20to%20code%20splitting,Split%20code%20via%20inline%20function%20calls%20within%20modules. "Il existe trois approches générales pour le fractionnement de code : points d’entrée : fractionner manuellement le code à l’aide de la configuration d’entrée.  Empêcher la duplication : utilisez des dépendances d’entrée ou SplitChunksPlugin pour dédupliquer et fractionner des blocs.  Importations dynamiques : fractionnement de code via des appels de fonction inline au sein de modules. - Partage de code | webpack"  

[MdnDocsWebCssUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Utilisation des propriétés personnalisées CSS (variables) | MDN"  

[MdnDocsWebJavascriptReferenceOperatorsIn]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/in "dans l’opérateur | MDN"  

[PwabuilderImagegenerator]: https://www.pwabuilder.com/imageGenerator "Image Generator | PWABuilder"  

[RollupjsMain]: https://rollupjs.org "rollup.js"  

[V8DevFeaturesPrivateBrandChecks]: https://v8.dev/features/private-brand-checks "La marque privée vérifie l’identité #foo dans obj | V8"  
[V8DevFeaturesClassFieldsPrivateClassFields]: https://v8.dev/features/class-fields#private-class-fields "Champs de classe privés : champs de classes publiques et privées | V8"  

[WebpackJsMain]: https://webpack.js.org "webpack"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developer.chrome.com/blog/new-in-devtools-91) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est sous [licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
