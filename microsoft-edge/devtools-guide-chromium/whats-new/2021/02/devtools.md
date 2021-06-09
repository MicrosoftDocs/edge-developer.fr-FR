---
description: Prise en charge du débogage de CSS Flexbox, affichage des performances sur la page web, mise à jour des outils de résolution des problèmes, etc.
title: Nouveautés de DevTools (Microsoft Edge 90)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, développement web, outils f12, devtools
ms.localizationpriority: high
ms.openlocfilehash: a13c344bb31cdfb7d0402132e3be82e4c330c612
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597163"
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
# <a name="whats-new-in-devtools-microsoft-edge-90"></a>Quoi de neuf dans DevTools (Microsoft Edge 90)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="group-tools-together-in-focus-mode"></a>Regrouper les outils en mode Focus  

<!-- Title: Grouping the tools in Focus Mode  -->  
<!-- Subtitle: Organize your favorite tools into groups with the new Focus Mode UI.  -->  

Focus Mode est une interface expérimentale qui vous permet de regrouper différents outils en fonction de vos propres scénarios de débogage.  La nouvelle **barre d'activités** affichée à gauche comprend des groupes d'outils prédéfinis tels que la **disposition** et le **débogage**.  Pour personnaliser chaque groupe d'outils, fermez les outils à l'aide de l'icône **Fermer** ((`X`\ )) ou ajoutez de nouveaux outils à l'aide de l'icône **Autres outils** (`+`\ ).  

Pour activer l'expérience, naviguez jusqu'à [Activer les fonctions][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] expérimentales et cochez les cases situées à côté de **Focus Mode et DevTools Tooltips** et **Activez les menus de l'onglet du bouton + pour ouvrir plus d'outils **.  Pour plus d'informations sur cette fonctionnalité ou pour commenter avec des questions et des idées, naviguez vers [DevTools : Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].  

:::image type="complex" source="../../media/2021/02/focus-mode.msft.png" alt-text="Afficher la barre d'activité" lightbox="../../media/2021/02/focus-mode.msft.png":::
   Afficher la barre **d'activité**   
:::image-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a>En savoir plus sur DevTools grâce à des infobulles informatives  

<!-- Title: DevTools Tooltips  -->  
<!-- Subtitle: Learn more about how to use DevTools with informative DevTools tooltips.  -->  

La fonctionnalité DevTools Tooltips vous aide à connaître les différents outils et volets.  Cliquez sur l'icône Aide \(`?`\) en bas de la **barre d'activités** pour activer les infobulles dans les outils de développement.  Lorsque les infobulles sont activées, passez la souris sur chaque région délimitée de DevTools pour en savoir plus sur l'utilisation de l'outil.  Pour activer l'expérience, naviguez jusqu'à [Activer les fonctions][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] expérimentales et cochez les cases situées à côté de **Focus Mode et DevTools Tooltips** et **Activez les menus de l'onglet du bouton + pour ouvrir plus d'outils **.  Pour plus d'informations sur cette fonctionnalité ou pour commenter avec des questions et des idées, naviguez vers [DevTools : Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].  

:::image type="complex" source="../../media/2021/02/focus-mode-and-tooltips-help.msft.png" alt-text="Choisissez l'icône d'aide ( ?) dans la barre d'activités pour afficher les infobulles." lightbox="../../media/2021/02/focus-mode-and-tooltips-help.msft.png":::
   Choisissez l'icône Aide \(`?`\) dans la **barre d'activités** pour afficher les infobulles.  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a>Personnaliser les raccourcis clavier dans les paramètres  

<!-- Title: Change keyboard shortcuts in Settings  -->  
<!-- TODO:  Rachel's feedback is about the fact that this experimental feature is turned on by default, may have separate section in What's New for experimental features)  -->  
<!-- Subtitle: Make DevTools work better for you by creating new keyboard shortcuts for any action in the DevTools.  -->  

Vous pouvez désormais personnaliser le raccourci clavier pour toute action dans les DevTools.  Pour modifier un raccourci clavier, effectuez les actions suivantes.  

1.  Ouvrez le DevTools, puis choisissez** Paramètres** > ** Raccourcis **.  
1.  Choisissez l'action que vous voulez personnaliser.  
1.  Choisissez l'option Modifier (![Icône de raccourci clavier pour l'édition](../../media/2021/02/edit-keyboard-shortcut-icon.msft.png)\icône.  
1.  Sélectionnez les touches que vous voulez lier à l'action.  
1.  Choisissez la coche \(![Cochez l'icône du raccourci clavier](../../media/2021/02/checkmark-keyboard-shortcut-icon.msft.png)\icône.  
    
Pour plus d'informations sur la personnalisation et la modification des raccourcis, consultez la section [Personnaliser les raccourcis clavier dans les DevTools de Microsoft Edge ][DevtoolsCustomizeShortcuts].  Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source Chromium, consultez le numéro [174309][CR174309].  

:::image type="complex" source="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png" alt-text="Personnaliser les raccourcis clavier dans les Paramètres DevTools sur Raccourcis avec un raccourci en mode édition" lightbox="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png":::
   Personnaliser les raccourcis clavier dans les [Paramètres DevTools][DevtoolsCustomizeIndexSettings] sur Raccourcis avec un raccourci en mode édition  
:::image-end:::  

## <a name="microsoft-edge-devtools-for-visual-studio-code-extension-update-114"></a>Mise à jour de l'extension Microsoft Edge DevTools pour Visual Studio Code 1.1.4  

<!-- Title: Edge Devtools for Visual Studio code extension update 1.1.4  -->  
<!-- Subtitle: Latest changes including a favicon is displayed next to each of the instances and console messages from the browser are displayed in the console of Visual Studio Code.  -->  

Les [outils de développement Microsoft Edge pour Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools], version 1.1.4 de l'extension Microsoft Visual Studio Code, affichent désormais un favicon à côté de chacune des instances DevTools.  Les messages de console de Microsoft Edge s'affichent désormais dans la **console DevTools** sous la rubrique **Sortie** du code Microsoft Visual Studio.  Microsoft Visual Studio Code met automatiquement à jour les extensions.  Pour mettre à jour manuellement la version 1.1.4, naviguez [jusqu'à Mettre à jour une extension manuellement ][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].  Vous pouvez déposer des questions et contribuer à l'extension sur le [repo GitHub de ][GithubMicrosoftVscodeEdgeDevtools]vscode-edge-devtools.  

:::row:::
   :::column span="":::
      La figure suivante affiche les messages d'un exemple de page Web enregistrée dans l'outil **Console** de Microsoft Edge.  
   :::column-end:::
   :::column span="":::
      La figure suivante affiche les mêmes messages de la page Web d'exemple enregistrés dans la **DevTools Console** sous **Sortie** du code Microsoft Visual Studio.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png" alt-text="Afficher un message dans la console dans Microsoft Edge DevTools" lightbox="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png":::
         Afficher un message dans la console dans Microsoft Edge DevTools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png" alt-text="Affichez le même message dans la console DevTools sous Sortie du code Microsoft Visual Studio." lightbox="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png":::
         Affichez le même message dans la console DevTools sous Sortie du code Microsoft Visual Studio.  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="improved-css-flexbox-editing-with-visual-flexbox-editor-and-multiple-overlays"></a>Amélioration de l'édition de CSS flexbox avec un éditeur visuel de flexbox et des superpositions multiples  

<!-- Title: Try different CSS flexbox layouts with the visual flexbox editor  -->  
<!-- Subtitle: In the Styles pane, choose the icon that appears next to display: flex to try different layout properties for flex containers.  -->  

DevTools dispose désormais d'outils de débogage CSS flexbox dédiés.  Si le style `display: flex`ou`display: inline-flex` CSS est appliqué à un élément HTML, une `flex`icône s'affiche à côté de cet élément dans l'outil **Éléments**.  Pour afficher (ou masquer) une superposition flexible sur la page Web, cliquez sur `flex`l'icône.  Pour connaître l'historique de cette fonctionnalité dans le projet open-source Chromium, consultez les numéros[1166710][CR1166710] et [1175699][CR1175699].  

:::row:::
   :::column span="":::
      Pour ouvrir l'éditeur **Flexbox**, accédez au volet **Styles** et cliquez sur la nouvelle icône située à côté du `display: flex`style`display: inline-flex` ou.  L'éditeur **Flexbox** offre un moyen rapide de modifier les propriétés de la boîte flexible.  
   :::column-end:::
   :::column span="":::
      De plus, la section **Flexbox** du volet **Mise en page affiche** tous les éléments Flexbox de la page Web.  Vous pouvez basculer la superposition de chaque élément.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-styles-display-flex-window.msft.png" alt-text="Outils de débogage CSS flexbox" lightbox="../../media/2021/02/elements-styles-display-flex-window.msft.png":::
         Outils de débogage CSS flexbox  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png" alt-text="Section Flexbox dans le volet Mise en page" lightbox="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png":::
         **Section Flexbox** dans le **volet** De disposition  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="keyboard-navigation-improvements-for-network-requests"></a>Amélioration de la navigation au clavier pour les demandes de réseau  

<!-- Title: Navigate the request initiator chain in the Network tool with the keyboard  -->  
<!-- Subtitle: The Initiator pane may now be expanded or collapsed with the arrow keys.  -->  

Auparavant, vous ne pouviez pas développer ou réduire la chaîne de demandes à l'aide des touches fléchées du clavier dans le volet **Initiateur**, contrairement au DOM dans l'outil** Éléments**.  Lorsqu'une demande de **réseau** est sélectionnée dans l'outil Réseau, le volet **Initiateur** affiche la chaîne des demandes qui ont initié la demande actuellement sélectionnée.  

Dans Microsoft Edge version 90, vous pouvez développer ou réduire la chaîne de demandes à l'aide des touches fléchées du clavier dans le volet **Initiateur**.  La demande de réseau ciblée dans la chaîne est également mise en évidence.  Pour en savoir plus sur les initiateurs dans l'outil **Réseau**, naviguez [jusqu'à Afficher les initiateurs et les dépendances][DevtoolsNetworkReferenceDisplayInitiatorsDependencies].  Pour revoir l'historique de cette fonctionnalité dans le projet open-source Chromium, consultez les numéros [1158276][CR1158276] et [1160637][CR1160637].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain.msft.png" alt-text="Choisissez une demande de réseau et sélectionnez le volet Initiateur." lightbox="../../media/2021/02/network-request-initiator-chain.msft.png":::
         Choisissez une demande de réseau et sélectionnez le volet **Initiateur**.  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png" alt-text="Développez ou réduisez la chaîne des initiateurs de demande et suivez la ligne en surbrillance." lightbox="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png":::
         Développez ou réduisez la chaîne des initiateurs de demande et suivez la ligne en surbrillance.  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="filtering-in-the-console-is-more-consistent"></a>Le filtrage dans la console est plus cohérent  

<!-- Title: Console improvements make filtering more consistent  -->  
<!-- Subtitle: The Log Levels dropdown is more clearly disabled when using filters in the Console sidebar.  -->  

Lorsque vous filtrez dans la [barre latérale de la console][DevtoolsConsoleReferenceOpenConsoleSidebar], les filtres de la liste déroulante des [niveaux de journal][DevtoolsConsoleReferenceFilterByLogLevel] ne sont pas disponibles.  Auparavant, la liste déroulante des **niveaux de journal** s'affichait en surbrillance lorsque vous la survoliez, même si un filtre de la **barre latérale de la console** était sélectionné.  Dans la version 90 de Microsoft Edge, la liste déroulante des **niveaux de journal** ne s'affiche plus lorsque vous la survolez alors qu'un filtre de la **barre latérale de la console** est sélectionné.  Pour en savoir plus sur le filtrage dans la **console**, allez à [Filtrer les messages][DevtoolsConsoleReferenceFilterMessages].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-old.msft.png" alt-text="Auparavant, si vous ouvrez la barre latérale de la console et que vous survolez les niveaux par défaut, ils étaient mis en évidence." lightbox="../../media/2021/02/console-sidebar-default-levels-old.msft.png":::
         Auparavant, si vous ouvrez **la barre latérale de la console** et que vous survolez les **niveaux par défaut**, ils étaient mis en évidence.  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-new.msft.png" alt-text="À partir de Microsoft Edge 90, si vous choisissez la barre latérale Console et que vous survolez les niveaux par défaut, ils ne sont pas mis en évidence." lightbox="../../media/2021/02/console-sidebar-default-levels-new.msft.png":::
         À partir de Microsoft Edge 90, si vous choisissez la **barre latérale Console** et survolez les **niveaux par défaut**, ils ne sont pas mis en évidence.  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="announcements-from-the-chromium-project"></a>Annonces du projet Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="the-console-now-escapes-double-quote-characters"></a>La console échappe désormais les caractères de guillemets doubles  

Auparavant, la **console** n'affichait pas les \(`"`\)caractères guillemets doubles valides dans les chaînes JavaScript.  À partir de la version 90 de Microsoft Edge, la **console** produit des chaînes JavaScript en utilisant des \(`"`\)caractères guillemets doubles échappés.  Pour revoir l'historique de cette fonctionnalité dans le projet open-source Chromium, consultez le numéro [1178530][CR1178530].  

:::image type="complex" source="../../media/2021/02/console-string-formatted-double-quotes.msft.png" alt-text="La console produit des chaînes JavaScript en utilisant des caractères de guillemets doubles échappés (&#0022 ;)." lightbox="../../media/2021/02/console-string-formatted-double-quotes.msft.png":::
   La **console** produit des chaînes JavaScript en utilisant des \(`"`\)caractères échappés de type guillemets doubles.  
:::image-end:::  

### <a name="emulate-the-css-color-gamut-media-feature"></a>Emuler la fonction CSS color-gamut media  

La [requête média][ChromestatusFeature5354410980933632] color-gamut émule la gamme approximative de couleurs prises en charge par le navigateur et le périphérique que vous testez.  La liste déroulante située sous** la fonction de média CSS Emulate color-gamut** contient les espaces de couleur que DevTools peut émuler.  Par exemple, pour déclencher une `color-gamut: p3`requête média, choisissez **color-gamut : p3** dans la liste déroulante.  

Pour émuler la fonction de média CSS color-gamut, effectuez les actions suivantes.  

1.  Ouvrez [le menu Commande.][DevtoolsCommandMenuIndex]  
1.  Tapez `Rendering`.  
1.  Exécutez la **commande Afficher le rendu**.  
1.  Naviguez jusqu'à la fonction de média CSS **Emulate color-gamut** et choisissez une option.  

Pour en savoir plus sur cette `color-gamut`fonction, consultez la rubrique Qualité de l'affichage des [couleurs : la fonction][CsswgDraftsMediaqueries4ColorGamut] «color-gamut» .  Pour revoir l'historique de cette fonctionnalité dans le projet open-source Chromium, consultez le numéro [1073887 ][CR1073887].  

:::image type="complex" source="../../media/2021/02/rendering-css-color-gamut.msft.png" alt-text="Emuler la fonction CSS color-gamut media" lightbox="../../media/2021/02/rendering-css-color-gamut.msft.png":::
   Emuler la fonction CSS color-gamut media  
:::image-end:::  

### <a name="improved-progressive-web-apps-tooling"></a>Amélioration de l'outil Progressive Web Apps  

#### <a name="pwa-installability-warning-in-the-console"></a>Avertissement sur l'installabilité de PWA dans la Console  

La **console** affiche désormais un message [d'avertissement plus détaillé sur l' installabilité des Progressive][ProgressiveWebAppsIndex] Web Apps (PWA) avec un lien vers [l'amélioration de la détection du support hors ligne des Progressive Web Apps][ChromeDeveloperBlogImprovedPwaOfflineDetection].  

:::image type="complex" source="../../media/2021/02/console-pwa-installability.msft.png" alt-text="Avertissement sur l'installabilité de PWA dans l'outil Console" lightbox="../../media/2021/02/console-pwa-installability.msft.png":::
   Avertissement sur l'installabilité de PWA dans l'outil **Console**  
:::image-end:::  

#### <a name="pwa-description-length-warning-in-the-manifest-pane"></a>Avertissement sur la longueur de la description du PWA dans le volet du manifeste

Le **volet Manifest** affiche désormais un message d'avertissement si la description du manifeste dépasse 324 caractères.  

:::image type="complex" source="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png" alt-text="Avertissement de troncature de la description PWA" lightbox="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png":::
   Avertissement de troncature de la description PWA  
:::image-end:::  

Pour revoir l'historique de cette fonctionnalité dans le projet open-source Chromium, consultez les numéros [965802 ][CR965802], [1146450][CR1146450] , et [1169689][CR1169689] .  

### <a name="new-remote-address-space-column-in-the-network-tool"></a>Nouvelle colonne Espace d'adressage distant dans l'outil Réseau  

<!-- does not work in canary 90.0.813.0 -->  
La nouvelle **colonne Espace** d'adressage distant affiche l'espace d'adressage IP de chaque ressource réseau.  Pour afficher la nouvelle colonne Espace d'adressage distant, effectuez les actions suivantes.  

1.  Naviguez vers l'outil **Réseau**.  
1.  Dans le tableau des demandes, survolez la ligne d'en-tête et ouvrez le menu contextuel (clic droit).  Pour savoir comment ajouter ou supprimer des colonnes dans le tableau des demandes, consultez la rubrique [Ajouter ou supprimer des colonnes][DevtoolsNetworkReferenceAddRemoveColumns].  
1.  Choisissez **Espace d'adressage distant** .  
    
Le tableau des demandes affiche maintenant une nouvelle colonne dont l'en-tête est **Espace d'adressage distant**.  Pour revoir l'historique de cette fonctionnalité dans le projet open-source Chromium, consultez le numéro [1128885][CR1128885].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png" alt-text="Dans le menu contextuel, choisissez Espace d'adressage distant." lightbox="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png":::
         Dans le menu contextuel, choisissez **l'espace d'adressage distant**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-remote-address-space.msft.png" alt-text="Le tableau des demandes affiche désormais la colonne Espace d'adressage distant." lightbox="../../media/2021/02/network-requests-remote-address-space.msft.png":::
         Le tableau des demandes affiche désormais la colonne **Espace d'adressage distant**. :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-allowed-and-disallowed-features-in-the-frame-details-view"></a>Afficher les fonctionnalités autorisées et non autorisées dans la vue détaillée du cadre.  

La vue détaillée du cadre affiche désormais une liste des fonctionnalités de navigateur autorisées et interdites, contrôlées par la [stratégie de permissions][GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer].  La stratégie de permissions est une API de plate-forme Web qui permet de bloquer l'utilisation des fonctionnalités du navigateur dans un cadre individuel ou dans les iframes qu'il intègre à une page Web.  Pour revoir l'historique de cette fonctionnalité dans le projet open-source Chromium, consultez le numéro [1158827][CR1158827].  

:::image type="complex" source="../../media/2021/02/application-frames-permissions-policy.msft.png" alt-text="Fonctionnalités autorisées et non autorisées en fonction de la stratégie d'autorisation." lightbox="../../media/2021/02/application-frames-permissions-policy.msft.png":::
   Fonctionnalités autorisées et non autorisées en fonction de la stratégie d'autorisation.  
:::image-end:::  

### <a name="new-sameparty-column-in-the-cookies-pane"></a>Nouvelle colonne SameParty dans le volet Cookies  

Le **volet Cookies** de l'outil **Application** affiche désormais `SameParty`l'attribut de chaque cookie.  Cet `SameParty`attribut est un nouvel attribut booléen permettant d'indiquer si un cookie est inclus dans les demandes adressées aux origines des mêmes ensembles de [première partie][GithubPrivacycgFirstPartySets].  Pour revoir l'historique de cette fonctionnalité dans le projet open-source Chromium, consultez le numéro [1161427][CR1161427].  

:::image type="complex" source="../../media/2021/02/application-storage-cookies-sameparty.msft.png" alt-text="Colonne SameParty dans le volet Cookies" lightbox="../../media/2021/02/application-storage-cookies-sameparty.msft.png":::
   **Colonne SameParty** dans le volet **Cookies**  
:::image-end:::  

### <a name="fndisplayname-property-in-the-console-tool-is-now-deprecated"></a>La propriété fn.displayName de l'outil Console est désormais obsolète.  

Auparavant, cette `fn.displayName`propriété vous permettait de contrôler les noms de débogage des fonctions à afficher dans `error.stack`et dans les traces de pile de DevTools.  À partir de la version 90 de Microsoft Edge, cette`fn.displayName` propriété est désormais dépréciée et remplacée par la`fn.name` propriété .  Utilisez la`Object.defineProperty` méthode standard pour définir la`fn.name` propriété.  Pour en savoir plus`fn.name`, consultez le site [Function.name][MdnJavascriptReferenceGlobalObjectsFunctionName].  Pour revoir l'historique de cette fonctionnalité dans le projet open-source Chromium, consultez le numéro [1177685][CR1177685].  

:::image type="complex" source="../../media/2021/02/console-display-name-name.msft.png" alt-text="Un exemple de la propriété fn.name pour contrôler les noms de débogage des fonctions" lightbox="../../media/2021/02/console-display-name-name.msft.png":::
   Un exemple de la `fn.name`propriété permettant de contrôler les noms de débogage pour les fonctions  
:::image-end:::  

### <a name="full-accessibility-tree-view-in-the-elements-tool"></a>Arborescence d'accessibilité complète dans l'outil Éléments  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Cette expérience **permet d'obtenir une arborescence d'accessibilité complète **dans l'outil **Éléments**.  Le [volet Accessibilité][DevtoolsAccessibilityTab] propose une arborescence d'accessibilité partielle, qui affiche la chaîne d'ancêtres directs du nœud racine au nœud inspecté.  
Après avoir activé cette expérience et rechargé les DevTools, choisissez l'un des boutons suivants pour changer l'affichage dans l'outil Éléments pour tous les éléments de la page Web.  

*   Pour afficher l'arborescence d'accessibilité complète, cliquez sur le bouton **Passer à l'arborescence d'accessibilité**.  
*   Pour afficher l'arborescence DOM, choisissez l'option **Passer à l'arborescence DOM**.  
    
Pour activer l'expérience, accédez à la [section Activer les fonctions][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] expérimentales et cochez la case située à côté de **Activer l'arborescence d'accessibilité complète dans le volet Éléments**.  Pour voir l'historique de cette fonctionnalité dans le projet open-source Chromium, consultez le numéro [887173][CR887173].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png" alt-text="Afficher l'arborescence DOM" lightbox="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png":::
         Afficher l'**arborescence DOM**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png" alt-text="Afficher l'arborescence complète de l'accessibilité" lightbox="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png":::
         Afficher **l'arborescence complète de l'accessibilité**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Téléchargez les canaux de l'aperçu de Microsoft Edge  

Si vous êtes sous Windows, Linux ou macOS, envisagez d'utiliser les [canaux d'aperçu de Microsoft][MicrosoftEdgePreviewChannels] Edge comme navigateur de développement par défaut.  Les canaux de prévisualisation vous donnent accès aux dernières fonctionnalités de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Entrer en contact avec l'équipe DevTools Microsoft Edge  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsAccessibilityTab]: ../../../accessibility/accessibility-tab.md "Tester l’accessibilité à l’aide de l’onglet Accessibilité | Microsoft Docs"  
[DevtoolsCommandMenuIndex]: ../../../command-menu/index.md "Exécuter des commandes avec le menu de commande DevTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsConsoleReferenceFilterByLogLevel]: ../../../console/reference.md#filter-by-log-level "Filtrer par niveau de journal – Référence de la console | Microsoft Docs"  
[DevtoolsConsoleReferenceFilterMessages]: ../../../console/reference.md#filter-messages "Filtrer les messages – Référence Console | Microsoft Docs"  
[DevtoolsConsoleReferenceOpenConsoleSidebar]: ../../../console/reference.md#open-the-console-sidebar "Ouvrir la barre latérale de la console – Référence de la console | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: ../../../customize/index.md#settings "Paramètres – Personnalisation de Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: ../../../customize/shortcuts.md "Personnaliser les raccourcis clavier dans les DevTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexEnablePlusButtonTabMenusToOpenMoreTools]: ../../../experimental-features/index.md#enable--button-tab-menus-to-open-more-tools "Activer les menus d'onglet du bouton + pour ouvrir plus d'outils – Fonctionnalités expérimentales | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: ../../../experimental-features/index.md#turn-on-experimental-features "Activer les fonctions expérimentales – Fonctions expérimentales | Microsoft Docs"  
[DevtoolsNetworkReferenceAddRemoveColumns]: ../../../network/reference.md#add-or-remove-columns "Ajouter ou supprimer des colonnes – Référence en matière d'analyse de réseau | Microsoft Docs"  
[DevtoolsNetworkReferenceDisplayInitiatorsDependencies]: ../../../network/reference.md#display-initiators-and-dependencies "Afficher les initiateurs et les dépendances – Référence en matière d'analyse de réseau | Microsoft Docs"  

[ProgressiveWebAppsIndex]: ../../../../progressive-web-apps-chromium/index.md "Aperçu des Progressive Web Apps sur Windows | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux de l'aperçu de Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Mise à jour manuelle d'une extension – Extension Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Outils Microsoft Edge pour Visual Studio Code | Visual Studio Marketplace"  

[ChromeDeveloperBlogImprovedPwaOfflineDetection]: https://developer.chrome.com/blog/improved-pwa-offline-detection "Amélioration de la détection du support hors ligne des Progressive Web App | Développeurs Chrome"  

[ChromestatusFeature5354410980933632]: https://www.chromestatus.com/feature/5354410980933632 "color-gamut media query | État de la plate-forme Chrome"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bogues de chrome"  
[CR174309]: https://crbug.com/174309 "Problème 174309 : DevTools : Permettre de personnaliser les raccourcis clavier/liaisons de touches | Bogues de Chromium"  
[CR887173]: https://crbug.com/887173 "Problème 887173 : DevTools : Inspection complète de l'arbre d'accessibilité | Bogues Chromium"  
[CR965802]: https://crbug.com/965802 "Problème 965802 : Implémentation d'une détection plus précise de la capacité hors ligne du travailleur de service | Bogues Chromium"  
[CR1073887]: https://crbug.com/1073887 "Problème 1073887 : DevTools : émulation de l'espace colorimétrique @media (color-gamut : ...) | bogues de Chromium"  
[CR1128885]: https://crbug.com/1128885 "Problème 1128885 : Prise en charge par DevTools de CORS-RFC1918 | Bogues de Chromium"  
[CR1146450]: https://crbug.com/1146450 "Problème 1146450 : [Android] Implémentation de l'installation de la feuille de fond | Bogues Chromium"  
[CR1158276]: https://crbug.com/1158276 "Problème 1158276 : impossible de développer/contratr le volet « Chaîne du initiateur de la demande » à l’aide des touches de direction dans la section « Réseau » des outils de développement | Bogues Chromium"  
[CR1158827]: https://crbug.com/1158827 "Problème 1158827 : [Stratégie d’autorisations] Implémenter la prise en charge des outils de développement pour les stratégies d'| Bogues Chromium"  
[CR1160637]: https://crbug.com/1160637 "Problème 1160637 : le focus sur la chaîne du initiateur de demande est considéré incomplet dans la section « Réseau » de la fenêtre « Outils de développement » | Bogues Chromium"  
[CR1161427]: https://crbug.com/1161427 "Problème 1161427 : &#9730 ; Prise en charge du débogage de l'attribut de cookie SameParty dans DevTools | Bogues Chromium"  
[CR1166710]: https://crbug.com/1166710 "Problème 1166710 : activer l'expérience de l'outil Flexbox par défaut | Bogues Chromium"  
[CR1169689]: https://crbug.com/1169689 "Problème 1169689 : La feuille de fond de l'installation de la PWA ne devrait pas comporter de catégories | Bogues de Chrome"  
[CR1175699]: https://crbug.com/1175699 "Numéro 1175699 : Éditeur Flexbox | Bogues Chromium"  
[CR1177685]: https://crbug.com/1177685 "Problème 1177685 : Suppression de la prise en charge non standard de fn.displayName | bogues Chromium"  
[CR1178530]: https://crbug.com/1178530 "Problème 1178530 : La console n'échappe pas les guillemets doubles lors de l'impression de chaînes de caractères | Bogues Chromium"  

[CsswgDraftsMediaqueries4ColorGamut]: https://drafts.csswg.org/mediaqueries-4#color-gamut "Qualité de l'affichage des couleurs : la fonction « color-gamut» | Projets de rédaction du groupe de travail CSS"  

[GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/main/DevTools/FocusMode/explainer.md "DevTools : Interface utilisateur du mode Focus – MicrosoftEdge/MSEdgeExplainers | GitHub"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubPrivacycgFirstPartySets]: https://github.com/privacycg/first-party-sets "Jeux de première partie | GitHub"  

[GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer]: https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md "Explication de la stratégie d'autorisation | GitHub"  

[MdnJavascriptReferenceGlobalObjectsFunctionName]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Function/name "Nom de la fonction | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developer.chrome.com/blog/new-in-devtools-90) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
