---
description: Prise en charge du débogage de CSS Flexbox, affichage à tête haute des performances sur la page web, mises à jour de l’outil problèmes, et bien plus encore
title: Nouveautés de DevTools (Microsoft Edge 90)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 4222bcf7284b69269691ec9fb78094e5efb95793
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408483"
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
# <a name="whats-new-in-devtools-microsoft-edge-90"></a>Nouveautés de DevTools (Microsoft Edge 90)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="group-tools-together-in-focus-mode"></a>Regroupement d’outils en mode Focus  

<!-- Title: Grouping the tools in Focus Mode  -->  
<!-- Subtitle: Organize your favorite tools into groups with the new Focus Mode UI.  -->  

Le mode Focus est une interface expérimentale qui vous permet de grouper différents outils en fonction de vos propres scénarios de débogage.  La nouvelle **barre d’activité** affichée à gauche inclut des groupes d’outils prédéfinie tels que **la** disposition et **le débogage.**  Pour personnaliser chaque groupe d’outils, fermez les outils avec l’icône **Fermer** \( \) ou ajoutez de nouveaux outils avec l’icône Plus d’outils `X` **** `+` \( \).  

Pour activer l’expérience, [][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] accédez à Activer les fonctionnalités expérimentales et activez les case à cocher en regard du mode Focus et des **bulles d’outils DevTools** et activez **les menus**onglets de bouton + pour ouvrir d’autres outils.  Pour plus d’informations sur cette fonctionnalité ou pour commenter avec des questions et des idées, accédez à [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].  

:::image type="complex" source="../../media/2021/02/focus-mode.msft.png" alt-text="Afficher la barre d’activité" lightbox="../../media/2021/02/focus-mode.msft.png":::
   Afficher la barre **d’activité**  
:::image-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a>En savoir plus sur DevTools avec des conseils d’information  

<!-- Title: DevTools Tooltips  -->  
<!-- Subtitle: Learn more about how to use DevTools with informative DevTools tooltips.  -->  

La fonctionnalité d’outils DevTools vous permet d’en savoir plus sur les différents outils et volets.  Choisissez l’icône Aide \( \) en bas de la barre d’activité pour faire bascule les bulles dans `?` DevTools. ****  Lorsque des bulles sont en cours, pointez sur chaque région de DevTools en plan pour en savoir plus sur l’utilisation de l’outil.  Pour activer l’expérience, [][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] accédez à Activer les fonctionnalités expérimentales et activez les case à cocher en regard du mode Focus et des **bulles d’outils DevTools** et activez **les menus**d’onglets de bouton + pour ouvrir d’autres outils.  Pour plus d’informations sur cette fonctionnalité ou pour commenter avec des questions et des idées, accédez à [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].  

:::image type="complex" source="../../media/2021/02/focus-mode-and-tooltips-help.msft.png" alt-text="Sélectionnez l’icône Aide (?) dans la barre d’activité pour afficher des bulles" lightbox="../../media/2021/02/focus-mode-and-tooltips-help.msft.png":::
   Sélectionnez l’icône Aide \( \) dans la barre `?` **d’activité** pour afficher des bulles  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a>Personnaliser les raccourcis clavier dans paramètres  

<!-- Title: Change keyboard shortcuts in Settings  -->  
<!-- TODO:  Rachel's feedback is about the fact that this experimental feature is turned on by default, may have separate section in What's New for experimental features)  -->  
<!-- Subtitle: Make DevTools work better for you by creating new keyboard shortcuts for any action in the DevTools.  -->  

Vous pouvez maintenant personnaliser le raccourci clavier pour toute action dans DevTools.  Pour modifier un raccourci clavier, effectuer les actions suivantes.  

1.  Ouvrez DevTools, puis **** choisissez  >  **Raccourcis des paramètres.**  
1.  Choisissez l’action que vous souhaitez personnaliser.  
1.  Choose the Edit \(![Icône Modifier le raccourci clavier](../../media/2021/02/edit-keyboard-shortcut-icon.msft.png)\) icône.  
1.  Sélectionnez les clés que vous souhaitez lier à l’action.  
1.  Sélectionnez la coche \(![Cochez l’icône Raccourci clavier](../../media/2021/02/checkmark-keyboard-shortcut-icon.msft.png)\) icône.  
    
Pour plus d’informations sur la personnalisation et la modification des raccourcis, accédez à Personnaliser les raccourcis clavier dans [Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans le projet open source Chromium, accédez au problème [174309.][CR174309]  

:::image type="complex" source="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png" alt-text="Personnaliser les raccourcis clavier dans les paramètres DevTools sur les raccourcis à l’aide d’un raccourci en mode édition" lightbox="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png":::
   Personnaliser les raccourcis clavier dans les [paramètres DevTools][DevtoolsCustomizeIndexSettings] sur les raccourcis à l’aide d’un raccourci en mode édition  
:::image-end:::  

## <a name="microsoft-edge-devtools-for-visual-studio-code-extension-update-114"></a>Microsoft Edge DevTools for Visual Studio Code extension update 1.1.4  

<!-- Title: Edge Devtools for Visual Studio code extension update 1.1.4  -->  
<!-- Subtitle: Latest changes including a favicon is displayed next to each of the instances and console messages from the browser are displayed in the console of Visual Studio Code.  -->  

Les outils de développement Microsoft Edge pour [l’extension][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] de code Visual Studio version 1.1.4 pour Microsoft Visual Studio Code affichent désormais un côté favorite à côté de chacune des instances DevTools.  Les messages de console de Microsoft Edge s’affichent désormais dans la **console DevTools** sous **Sortie** de Microsoft Visual Studio Code.  Microsoft Visual Studio code met automatiquement à jour les extensions.  Pour mettre à jour manuellement la version 1.1.4, accédez à Mettre à jour [une extension manuellement.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  Vous pouvez déposer des problèmes et contribuer à l’extension sur le référentiel GitHub [vscode-edge-devtools.][GithubMicrosoftVscodeEdgeDevtools]  

:::row:::
   :::column span="":::
      La figure suivante affiche les messages d’un exemple de page web enregistrée dans l’outil **Console** dans Microsoft Edge.  
   :::column-end:::
   :::column span="":::
      La figure suivante affiche les mêmes messages de l’exemple de page **** web enregistrée dans la **console DevTools** sous Sortie de Microsoft Visual Studio Code.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png" alt-text="Afficher un message dans la console dans Microsoft Edge DevTools" lightbox="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png":::
         Afficher un message dans la console dans Microsoft Edge DevTools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png" alt-text="Afficher le même message dans la console DevTools sous Sortie de Microsoft Visual Studio Code" lightbox="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png":::
         Afficher le même message dans la console DevTools sous Sortie de Microsoft Visual Studio Code  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="improved-css-flexbox-editing-with-visual-flexbox-editor-and-multiple-overlays"></a>Modification améliorée de la flexbox CSS avec l’éditeur visual flexbox et plusieurs superpositions  

<!-- Title: Try different CSS flexbox layouts with the visual flexbox editor  -->  
<!-- Subtitle: In the Styles pane, choose the icon that appears next to display: flex to try different layout properties for flex containers.  -->  

DevTools dispose désormais d’outils de débogage flexbox CSS dédiés.  Si le style ou CSS est appliqué à un élément HTML, une icône s’affiche à côté de cet élément `display: flex` `display: inline-flex` dans `flex` **l’outil Elements.**  Pour afficher \(ou masquer\) une superposition flexible sur la page web, choisissez `flex` l’icône.  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problèmes [1166710][CR1166710] et [1175699][CR1175699].  

:::row:::
   :::column span="":::
      Pour ouvrir **l’éditeur Flexbox,** accédez au volet **Styles** et choisissez la nouvelle icône à côté du `display: flex` style ou du `display: inline-flex` style.  **L’éditeur Flexbox** permet de modifier rapidement les propriétés de flexbox.  
   :::column-end:::
   :::column span="":::
      En outre, la section **** **Flexbox** du volet Disposition affiche tous les éléments flexbox sur la page web.  Vous pouvez faire bascule la superposition de chaque élément.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-styles-display-flex-window.msft.png" alt-text="Outils de débogage CSS flexbox" lightbox="../../media/2021/02/elements-styles-display-flex-window.msft.png":::
         Outils de débogage CSS flexbox  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png" alt-text="Section Flexbox dans le volet De disposition" lightbox="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png":::
         **Section Flexbox** dans le **volet** De disposition  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="keyboard-navigation-improvements-for-network-requests"></a>Améliorations de la navigation au clavier pour les demandes réseau  

<!-- Title: Navigate the request initiator chain in the Network tool with the keyboard  -->  
<!-- Subtitle: The Initiator pane may now be expanded or collapsed with the arrow keys.  -->  

Auparavant, vous n’étiez pas en mesure de développer ou **** de réduire la chaîne de demandes à l’aide des touches de direction du clavier dans le volet Initiateur, contrairement au DOM de l’outil **Elements.**  Lorsqu’une demande réseau est **** sélectionnée dans l’outil Réseau, le volet **Initiateur** affiche la chaîne de demandes qui a initié la demande actuellement sélectionnée.  

Dans Microsoft Edge version 90, vous pouvez développer ou réduire la chaîne de demandes à l’aide des touches de direction du clavier dans le **volet Initiateur.**  La demande réseau mise en évidence dans la chaîne est désormais également mise en évidence.  Pour en savoir plus sur les initiateurs dans l’outil **Réseau,** accédez à [Afficher les initiateurs et les dépendances.][DevtoolsNetworkReferenceDisplayInitiatorsDependencies]  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problèmes [1158276][CR1158276] et [1160637][CR1160637].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain.msft.png" alt-text="Choose a Network request and choose the Initiator pane" lightbox="../../media/2021/02/network-request-initiator-chain.msft.png":::
         Choose a Network request and choose the **Initiator** pane  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png" alt-text="Développer ou réduire la chaîne de l’initiateur de la demande et suivre la ligne mise en surbrill" lightbox="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png":::
         Développer ou réduire la chaîne de l’initiateur de la demande et suivre la ligne mise en surbrill  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="filtering-in-the-console-is-more-consistent"></a>Le filtrage dans la console est plus cohérent  

<!-- Title: Console improvements make filtering more consistent  -->  
<!-- Subtitle: The Log Levels dropdown is more clearly disabled when using filters in the Console sidebar.  -->  

Pendant que vous filtrez avec la [barre latérale de la console,][DevtoolsConsoleReferenceOpenConsoleSidebar]les filtres de la dropdown Log [Levels][DevtoolsConsoleReferenceFilterByLogLevel] ne sont pas disponibles.  Auparavant, la dropdown **Log Levels** (Niveaux des journaux) était mise en surbrilllette lorsque vous pointiez dessus, même lorsqu’un filtre de la barre latérale de **la console** a été choisi.  Dans Microsoft Edge version 90, la dropdown **Log Levels** n’est plus sélectionnée lorsque vous pointez dessus pendant qu’un filtre de la **barre latérale de la console** est choisi.  Pour en savoir plus sur le filtrage dans la **console,** accédez [à Filtrer les messages.][DevtoolsConsoleReferenceFilterMessages]  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-old.msft.png" alt-text="Auparavant, si vous ouvrez la barre latérale de la console et que vous pointez sur les niveaux par défaut, elle a été mise en surbrill" lightbox="../../media/2021/02/console-sidebar-default-levels-old.msft.png":::
         Auparavant, si vous ouvrez la **barre latérale de la console** et que vous pointez sur les **niveaux par défaut,** elle a été mise en surbrill  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-new.msft.png" alt-text="À partir de Microsoft Edge 90, si vous choisissez la barre latérale console et que vous pointez sur les niveaux par défaut, elle ne se met pas en surbrill" lightbox="../../media/2021/02/console-sidebar-default-levels-new.msft.png":::
         À partir de Microsoft Edge 90, si vous choisissez la **barre** latérale console et que vous pointez sur les niveaux par **défaut,** elle ne met pas en surbrill  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="announcements-from-the-chromium-project"></a>Annonces du projet de Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="the-console-now-escapes-double-quote-characters"></a>La console échappe désormais les guillemets doubles  

Auparavant, la **console n’a** pas produit de guillemets doubles valides \( `"` \) caractères dans les chaînes JavaScript.  À partir de La version 90 de Microsoft Edge, la **console** produit des chaînes JavaScript à l’aide de guillemets doubles d’échadé \( `"` \).  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1178530][CR1178530].  

:::image type="complex" source="../../media/2021/02/console-string-formatted-double-quotes.msft.png" alt-text="La console produit des chaînes JavaScript à l’aide de guillemets doubles (&#0022;)" lightbox="../../media/2021/02/console-string-formatted-double-quotes.msft.png":::
   La **console produit des** chaînes JavaScript à l’aide de guillemets doubles d’échadé \( `"` \) caractères  
:::image-end:::  

### <a name="emulate-the-css-color-gamut-media-feature"></a>Émuler la fonctionnalité multimédia de palette de couleurs CSS  

La [requête multimédia de gamme][ChromestatusFeature5354410980933632] de couleurs émule la plage approximative de couleurs prise en charge par le navigateur et l’appareil que vous testez.  La dropdown sous Émuler la gamme de couleurs des fonctionnalités multimédias **CSS** contient des espaces de couleur que DevTools peut émuler.  Par exemple, pour déclencher une requête `color-gamut: p3` multimédia, choisissez **color-gamut: p3** dans ladown.  

Pour émuler la fonctionnalité multimédia de palette de couleurs CSS, effectuer les actions suivantes.  

1.  Ouvrez [le menu Commande.][DevtoolsCommandMenuIndex]  
1.  Entrez `Rendering`.  
1.  Exécutez la **commande Afficher le rendu.**  
1.  Accédez à Émuler la gamme de couleurs des fonctionnalités multimédias **CSS** et choisissez une option.  

Pour en savoir plus sur la fonctionnalité, accédez à Qualité de l’affichage des couleurs : la fonctionnalité `color-gamut` [« color-gamut][CsswgDraftsMediaqueries4ColorGamut]».  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1073887][CR1073887].  

:::image type="complex" source="../../media/2021/02/rendering-css-color-gamut.msft.png" alt-text="Émuler la fonctionnalité multimédia de palette de couleurs CSS" lightbox="../../media/2021/02/rendering-css-color-gamut.msft.png":::
   Émuler la fonctionnalité multimédia de palette de couleurs CSS  
:::image-end:::  

### <a name="improved-progressive-web-apps-tooling"></a>Outils d’applications web progressives améliorés  

#### <a name="pwa-installability-warning-in-the-console"></a>Avertissement d’installabilité PWA dans la console  

La **console affiche** désormais un message d’avertissement d’installation [PWA (Progressive Web Apps)][ProgressiveWebAppsIndex] plus détaillé avec un lien vers l’amélioration de la détection de prise en charge en mode hors connexion de [l’application web progressive.][ChromeDeveloperBlogImprovedPwaOfflineDetection]  

:::image type="complex" source="../../media/2021/02/console-pwa-installability.msft.png" alt-text="Avertissement d’installabilité PWA dans l’outil Console" lightbox="../../media/2021/02/console-pwa-installability.msft.png":::
   Avertissement d’installabilité PWA dans **l’outil Console**  
:::image-end:::  

#### <a name="pwa-description-length-warning-in-the-manifest-pane"></a>Avertissement de longueur de description PWA dans le volet manifeste

Le **volet** Manifeste affiche maintenant un message d’avertissement si la description du manifeste dépasse 324 caractères.  

:::image type="complex" source="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png" alt-text="Avertissement de tronqué de description PWA" lightbox="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png":::
   Avertissement de tronqué de description PWA  
:::image-end:::  

Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problèmes [965802][CR965802], [1146450][CR1146450]et [1169689][CR1169689].  

### <a name="new-remote-address-space-column-in-the-network-tool"></a>Nouvelle colonne Espace d’adressalage distant dans l’outil Réseau  

<!-- does not work in canary 90.0.813.0 -->  
La nouvelle **colonne Espace d’adressag** distant affiche l’espace d’adressag IP réseau de chaque ressource réseau.  Pour afficher la nouvelle colonne Espace d’adressas distant, effectuer les actions suivantes.  

1.  Accédez à **l’outil** Réseau.  
1.  Dans le tableau Demandes, pointez sur la ligne d’en-tête et ouvrez le menu contextuel \(clic droit\).  Pour savoir comment ajouter ou supprimer des colonnes de la table Requests, accédez [à Ajouter ou supprimer des colonnes.][DevtoolsNetworkReferenceAddRemoveColumns]  
1.  Choose **Remote Address Space**.  
    
La table Requests affiche désormais une nouvelle colonne avec l’en-tête nommé **Espace d’adressare distant.**  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1128885.][CR1128885]  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png" alt-text="Dans le menu contextuel, choisissez Espace d’adressas distant" lightbox="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png":::
         Dans le menu contextuel, choisissez **l’espace d’adressas distant**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-remote-address-space.msft.png" alt-text="La table Demandes affiche désormais la colonne Espace d’adressas distant" lightbox="../../media/2021/02/network-requests-remote-address-space.msft.png":::
         La table Demandes affiche désormais la colonne **Espace d’adressas distant** :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-allowed-and-disallowed-features-in-the-frame-details-view"></a>Afficher les fonctionnalités autorisées et non autorisées dans l’affichage Détails de l’image  

L’affichage Détails de l’image affiche désormais une liste des fonctionnalités de navigateur autorisées et non autorisées contrôlées par la stratégie [d’autorisations.][GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer]  La stratégie d’autorisations est une API de plateforme web qui autorise \(ou bloque\) une page web à utiliser les fonctionnalités de navigateur dans une image individuelle ou dans des iframes qu’elle incorpore.  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1158827][CR1158827].  

:::image type="complex" source="../../media/2021/02/application-frames-permissions-policy.msft.png" alt-text="Fonctionnalités autorisées et non autorisées basées sur la stratégie d’autorisation" lightbox="../../media/2021/02/application-frames-permissions-policy.msft.png":::
   Fonctionnalités autorisées et non autorisées basées sur la stratégie d’autorisation  
:::image-end:::  

### <a name="new-sameparty-column-in-the-cookies-pane"></a>Nouvelle colonne SameParty dans le volet Cookies  

Le **volet Cookies** de l’outil **Application** affiche désormais l’attribut de `SameParty` chaque cookie.  L’attribut est un nouvel attribut booléen pour indiquer si un cookie est inclus dans les demandes aux origines des mêmes jeux de première `SameParty` [partie][GithubPrivacycgFirstPartySets].  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1161427][CR1161427].  

:::image type="complex" source="../../media/2021/02/application-storage-cookies-sameparty.msft.png" alt-text="Colonne SameParty dans le volet Cookies" lightbox="../../media/2021/02/application-storage-cookies-sameparty.msft.png":::
   **Colonne SameParty** dans le **volet Cookies**  
:::image-end:::  

### <a name="fndisplayname-property-in-the-console-tool-is-now-deprecated"></a>la propriété fn.displayName dans l’outil Console est désormais désacdessée  

Auparavant, la propriété vous permettait de contrôler les noms de débogage pour les fonctions à afficher dans et dans les traces de pile `fn.displayName` `error.stack` DevTools.  À compter de la version 90 de Microsoft Edge, la propriété est désormais remplacée par la `fn.displayName` `fn.name` propriété.  Utilisez la méthode standard `Object.defineProperty` pour définir la `fn.name` propriété.  Pour en savoir `fn.name` plus, accédez [à Function.name][MdnJavascriptReferenceGlobalObjectsFunctionName].  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1177685.][CR1177685]  

:::image type="complex" source="../../media/2021/02/console-display-name-name.msft.png" alt-text="Exemple de propriété fn.name pour contrôler les noms de débogage pour les fonctions" lightbox="../../media/2021/02/console-display-name-name.msft.png":::
   Exemple de propriété `fn.name` pour contrôler les noms de débogage pour les fonctions  
:::image-end:::  

### <a name="full-accessibility-tree-view-in-the-elements-tool"></a>Arborescence d’accessibilité complète dans l’outil Éléments  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Cette expérience fournit une arborescence **d’accessibilité complète** dans **l’outil Elements.**  Le [volet Accessibilité][DevtoolsAccessibilityReferenceTheAccessibilityPane] fournit une arborescence d’accessibilité partielle, qui affiche la chaîne ancêtre direct du nœud racine au nœud inspecté.  
Après avoir activer cette expérience et rechargé de DevTools, choisissez l’un des boutons suivants pour basculer l’affichage dans l’outil Éléments pour tous les éléments de la page web.  

*   Pour afficher l’arborescence d’accessibilité complète, choisissez l’arborescence Basculer vers **l’arborescence d’accessibilité.**  
*   Pour afficher l’arborescence DOM, choisissez l’arborescence Basculer vers **l’arborescence DOM.**  
    
Pour activer l’expérience, [][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] accédez à Activer les fonctionnalités expérimentales et activez la case à cocher en regard de l’arborescence Activer l’accessibilité complète dans le **volet Éléments.**  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au [problème 887173][CR887173].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png" alt-text="Afficher l’arborescence DOM" lightbox="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png":::
         Affichage de **l’affichage DOM**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png" alt-text="Afficher l’arborescence d’accessibilité complète" lightbox="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png":::
         Afficher **l’arborescence d’accessibilité complète**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Télécharger les canaux d’aperçu Microsoft Edge  

Si vous utilisez Windows, Linux ou macOS, envisagez d’utiliser les canaux d’aperçu [Microsoft Edge][MicrosoftEdgePreviewChannels] comme navigateur de développement par défaut.  Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Contacter l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsAccessibilityReferenceTheAccessibilityPane]: /microsoft-edge/devtools-guide-chromium/accessibility/reference#the-accessibility-pane "Volet Accessibilité : référence sur l’accessibilité | Documents Microsoft"  
[DevtoolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Exécuter des commandes avec le menu de commande Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsConsoleReferenceFilterByLogLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Filtrer par niveau de journal - Référence de la console | Documents Microsoft"  
[DevtoolsConsoleReferenceFilterMessages]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-messages "Filter messages - Console Reference | Documents Microsoft"  
[DevtoolsConsoleReferenceOpenConsoleSidebar]: /microsoft-edge/devtools-guide-chromium/console/reference#open-the-console-sidebar "Ouvrez la barre latérale de la console - Référence de la console | Documents Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personnaliser les raccourcis clavier dans l'| Microsoft Edge DevTools Documents Microsoft"  
[DevtoolsExperimentalFeaturesIndexEnablePlusButtonTabMenusToOpenMoreTools]: /microsoft-edge/devtools-guide-chromium/experimental-features/index#enable--button-tab-menus-to-open-more-tools "Activer + les menus onglet de bouton pour ouvrir d’autres outils - Fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features/index#turn-on-experimental-features "Activer les fonctionnalités expérimentales : fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsNetworkReferenceAddRemoveColumns]: /microsoft-edge/devtools-guide-chromium/network/reference#add-or-remove-columns "Ajouter ou supprimer des colonnes : référence de l’analyse | Documents Microsoft"  
[DevtoolsNetworkReferenceDisplayInitiatorsDependencies]: /microsoft-edge/devtools-guide-chromium/network/reference#display-initiators-and-dependencies "Afficher les initiateurs et les dépendances - Référence de l’analyse | Documents Microsoft"  

[ProgressiveWebAppsIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Présentation progressive des applications web sur Windows | Documents Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux d’aperçu Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Mettre à jour une extension manuellement - Extension Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Outils Microsoft Edge pour Visual Studio code | Visual Studio Marketplace"  

[ChromeDeveloperBlogImprovedPwaOfflineDetection]: https://developer.chrome.com/blog/improved-pwa-offline-detection "Amélioration de la détection de détection de la prise en charge en mode hors connexion de Progressive Web App | Développeurs Chrome"  

[ChromestatusFeature5354410980933632]: https://www.chromestatus.com/feature/5354410980933632 "color-gamut media query | État de la plateforme Chrome"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bogues Chromium"  
[CR174309]: https://crbug.com/174309 "Problème 174309: DevTools: Autoriser la personnalisation des raccourcis clavier/les combinaisons de touches | Bogues Chromium"  
[CR887173]: https://crbug.com/887173 "Problème 887173 : DevTools : inspection complète de l’arborescence d’accessibilité | Bogues Chromium"  
[CR965802]: https://crbug.com/965802 "Problème 965802 : implémenter la détection des fonctionnalités hors connexion du service plus précise | Bogues Chromium"  
[CR1073887]: https://crbug.com/1073887 "Problème 1073887 : DevTools : @media (color-gamut: ...) colorspace emulation | Bogues Chromium"  
[CR1128885]: https://crbug.com/1128885 "Problème 1128885 : Prise en charge de DevTools pour cors-RFC1918 | Bogues Chromium"  
[CR1146450]: https://crbug.com/1146450 "Problème 1146450 : [Android] Implémenter les installations de feuille inférieure | Bogues Chromium"  
[CR1158276]: https://crbug.com/1158276 "Problème 1158276 : Impossible de développer/de contracter le volet « Chaîne de l’initiateur de la demande » à l’aide des touches de direction dans la section « Réseau » de DevTools | Bogues Chromium"  
[CR1158827]: https://crbug.com/1158827 "Problème 1158827 : [Stratégie d’autorisations] Implémenter la prise en charge de la dévtool pour les stratégies d’autorisations | Bogues Chromium"  
[CR1160637]: https://crbug.com/1160637 "Problème 1160637 : la section « Réseau » de la fenêtre « Outils de développement » de la fenêtre « Demander une chaîne d’initiateur » est incomplète | Bogues Chromium"  
[CR1161427]: https://crbug.com/1161427 "Problème 1161427 : &#9730; prise en charge du débogage d’attribut de cookie SameParty dans DevTools | Bogues Chromium"  
[CR1166710]: https://crbug.com/1166710 "Problème 1166710 : activer l’expérience d’outils flexbox par défaut | Bogues Chromium"  
[CR1169689]: https://crbug.com/1169689 "Problème 1169689 : la feuille inférieure de l’installation PWA ne doit pas être une catégorie de fonctionnalités | Bogues Chromium"  
[CR1175699]: https://crbug.com/1175699 "Problème 1175699 : éditeur Flexbox | Bogues Chromium"  
[CR1177685]: https://crbug.com/1177685 "Problème 1177685 : supprimer la prise en charge de fn.displayName non standard | Bogues Chromium"  
[CR1178530]: https://crbug.com/1178530 "Problème 1178530 : la console n’échappe pas aux doublequotes lors de l’impression de chaînes | Bogues Chromium"  

[CsswgDraftsMediaqueries4ColorGamut]: https://drafts.csswg.org/mediaqueries-4#color-gamut "Qualité de l’affichage des couleurs : fonctionnalité « color-gamut » | Brouillons de l’éditeur de groupe de travail CSS"  

[GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/main/DevTools/FocusMode/explainer.md "DevTools : interface utilisateur du mode Focus - MicrosoftEdge/MSEdgeExplainers | GitHub"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubPrivacycgFirstPartySets]: https://github.com/privacycg/first-party-sets "Jeux de groupes | GitHub"  

[GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer]: https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md "Expliqueur de stratégie d’autorisations | GitHub"  

[MdnJavascriptReferenceGlobalObjectsFunctionName]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Function/name "Function.name | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/updates/2021/02/devtools/index) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
