---
description: Les soulignements ondulés mettent en évidence les problèmes de code dans l'outil Éléments, la chronologie de mise à jour du service de travail, etc.
title: Nouveautés de DevTools (Microsoft Edge 91)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/21/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 3a2be4d309432de4421af73ca7b4d21734ad5221
ms.sourcegitcommit: de75fda30bb8964e9a184228d068b4402ec59c3e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "11514445"
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

## <a name="wavy-underlines-highlight-code-issues-and-improvements-in-elements-tool"></a>Les soulignements ondulés mettent en évidence les problèmes de code et les améliorations apportées à l'outil Elements  

<!--  Title: Get code hints in Elements tool  -->  
<!--  Subtitle: Wavy underlines like the ones you see in Visual Studio Code now display in the Elements tool.  Underlines alert you to code issues related to accessibility, compatibility, security, performance, and  so on.  -->  

Dans la plupart des IDE modernes, les soulignements ondulés sous le texte indiquent des erreurs de syntaxe.   Dans Microsoft Edge version 91 ou ultérieure, les soulignements ondulés s'affichent sous HTML dans la vue **DOM** de **l'outil Elements.**  Les soulignements ondulés indiquent des problèmes de code et des suggestions liés à l'accessibilité, la compatibilité, les performances, etc.  Pour plus d'informations sur la façon de passer en revue et de modifier les problèmes, accédez à Rechercher et résoudre les problèmes avec l'outil Problèmes [DevTools][DevtoolsIssuesIndex]de Microsoft Edge.  

Pour ouvrir **l'outil Problèmes** et en savoir plus sur le problème et comment le résoudre, effectuer l'une des actions suivantes.  

*   Sélectionnez et `Shift` maintenez, puis choisissez un soulignement ondulé.  
*   Effectuer les actions suivantes.  
    1.  Pointez sur n'importe quel soulignement ondulé.  
    1.  Ouvrez le menu contextuel \(cliquez avec le bouton droit\).  
    1.  Choose **Show in Issues**.  
        
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues.msft.png" alt-text="Choisir l'erreur soulignée dans l'outil Éléments" lightbox="../../media/2021/04/elements-iframe-highlight-issues.msft.png":::
         Choisir l'erreur soulignée dans **l'outil Éléments**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png" alt-text="Afficher les détails des erreurs dans l'outil Problèmes" lightbox="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png":::
         Afficher les détails des erreurs dans **l'outil Problèmes**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a>En savoir plus sur DevTools grâce à des infobulles informatives  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<!--  Title: Learn more about DevTools with DevTools Tooltips  -->  
<!--  Subtitle: Informative overlays are now available in the default DevTools interface.  -->  

La fonctionnalité d'outils DevTools vous permet d'en savoir plus sur les différents outils et volets de DevTools.  Pour désactiver les bulles, sélectionnez `Esc` .  Pour activer les bulles, effectuer l'une des actions suivantes.  

*   Sélectionnez `Ctrl` + `Shift` + `H` \(Windows/Linux\) ou `Cmd` + `Shift` + `H` \(macOS\).  
*   [Ouvrez le menu Commande,][DevtoolsCommandMenuIndexOpenCommandMenu] puis tapez `tooltips` .  
*   Choose **Customize and control DevTools** \( `...` \) > **Help**  >  **Toggle the DevTools Tooltips**.  

En outre, si vous allumez l'expérience d'bulles d'outils Mode Focus et [DevTools,][DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode] vous pouvez également choisir le bouton Basculer le bouton d'outils **DevTools** \( \) en bas de la barre `?` d'activité. ****  

Pour afficher plus d'informations sur l'utilisation de DevTools, allumez les info-bulles, puis pointez sur chaque région en plan des DevTools.  

:::image type="complex" source="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png" alt-text="Pointez n'importe où dans la région mise en surbrillez de l'outil Problèmes pour afficher plus de détails" lightbox="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png":::
   Pointez n'importe où dans **** la région mise en surbrillez de l'outil Problèmes pour afficher plus de détails  
:::image-end:::  

## <a name="service-worker-update-timeline"></a>Chronologie de mise à jour du service de travail  

<!--todo:  Update the linked [Service Worker improvements][DevtoolsServiceWorkerIndex] article.  -->  

<!--  Title: The tasks associated with your Service Worker  -->  
<!--  Subtitle: Debug with Service Worker Update Cycle  -->  

Dans Microsoft Edge version 91 ou ultérieure, si vous êtes développeur Progressive Web App ou Service Worker, vous pouvez afficher le cycle de vie des mises à jour de vos employés de service sous forme de chronologie dans l'outil **Application.**  Cette fonctionnalité vous permet de comprendre le temps que votre service de travail passe à chacune des étapes suivantes.  

*   **Install**  
*   **Attendre**  
*   **Activer**  
    
:::image type="complex" source="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png" alt-text="Passer en revue la chronologie du cycle de mise à jour pour votre service de travail" lightbox="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png":::
   Passer en revue **la chronologie** du cycle de mise **à jour** pour votre service de travail  
:::image-end:::  

Pour plus d'informations sur le cycle de vie de vos employés de service, accédez au cycle de vie des travailleurs [de service.][ProgressiveWebAppsServiceworkerServiceWorkerLifecycle]  Pour plus d'informations sur les outils de débogage pour les applications web progressives et les travailleurs de service dans DevTools, accédez aux améliorations apportées aux services [de travail.][DevtoolsServiceWorkerIndex]  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans le projet open source Chromium, accédez à Problème [1066604][CR1066604].  

## <a name="progressive-web-apps-no-longer-display-warnings-for-non-square-icons"></a>Les applications web progressives n'affichent plus d'avertissements pour les icônes non carrées  

<!--  Title: Non-square icons in app manifest no longer produce warnings  -->  
<!--  Subtitle: As long as square icons are included in the app manifest, non-square icons no longer produce warnings  -->  

Dans [Microsoft Edge version 90][DevtoolsWhatsNew202102Devtools] ou antérieure, si vous avez inclus une icône non carrée dans le manifeste d'application web de votre application PWA, la section Manifeste de l'outil **Application** a affiché un avertissement sous Erreurs et **** **avertissements** pour chaque icône non carrée.  Dans Microsoft Edge version 91 ou ultérieure, la **section** Manifeste de l'outil **Application** n'affiche aucun avertissement si vous fournissez au moins une icône carrée.  Si vous ne fournissez aucune icône carrée, un avertissement affiche le message suivant.  

```output
Most operating systems require square icons.  Please include at least one square icon in the array.  
```  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png" alt-text="Dans Microsoft Edge version 90 ou antérieure, une erreur s'affiche pour chaque icône non carrée" lightbox="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png":::
         Dans Microsoft Edge version 90 ou antérieure, une erreur s'affiche pour chaque icône non carrée  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png" alt-text="Dans Microsoft Edge version 91 ou ultérieure, aucune erreur ne s'affiche lorsque vous fournissez au moins une icône carrée" lightbox="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png":::
         Dans Microsoft Edge version 91 ou ultérieure, aucune erreur ne s'affiche lorsque vous fournissez au moins une icône carrée  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Pour passer en revue les erreurs et les avertissements dans votre manifeste d'application web, accédez à l'outil **Application** et choisissez la section **Manifeste.**  Les erreurs et avertissements sont répertoriés sous le titre **Erreurs et avertissements.**  Pour plus d'informations sur le manifeste de l'application Web, accédez à Utiliser le manifeste d'application web pour intégrer votre application Web progressive [dans le système d'exploitation.][ProgressiveWebAppsWebappmanifests]  Pour créer des icônes à inclure dans votre manifeste d'application web, accédez au générateur [d'images PWABuilder.][PwabuilderImagegenerator]  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1185945][CR1185945].  

## <a name="localized-devtools-now-supported-in-chromium-based-browsers"></a>DevTools localisée désormais prise en charge dans les navigateurs basés sur Chromium  

<!--  Title: Localization for all  -->  
<!--  Subtitle: Match browser language enabled to all Chromium-based browsers  -->  

À partir [de Microsoft Edge version 81,][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages]Microsoft Edge DevTools s'affiche dans votre propre langue.  De nombreux développeurs utilisent d'autres outils de développement tels que StackOverflow et Visual Studio code dans leur langue native, et pas seulement en anglais.  L'équipe Microsoft Edge DevTools, l'équipe Chrome DevTools et l'équipe Google Chrome ont travaillé pour offrir la même expérience dans tous les navigateurs basés sur Chromium.  Pour plus d'informations sur l'utilisation de DevTools dans votre langue, accédez à Modifier les paramètres de langue [de DevTools.][DevtoolsCustomizeLocalization]  Pour plus d'informations sur la collaboration sur cette fonctionnalité dans le projet open source Chromium, accédez à [1136655.][CR1136655]  

:::image type="complex" source="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png" alt-text="Navigateur Microsoft Edge et DevTools en japonais" lightbox="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png":::
   Navigateur Microsoft Edge et DevTools en japonais  
:::image-end:::  

## <a name="use-the-keyboard-to-navigate-to-css-variables"></a>Utiliser le clavier pour accéder aux variables CSS  

<!--  Title: Navigate to CSS variables with the arrow keys  -->  
<!--  Subtitle: In the Styles pane, use the arrow keys to choose CSS variables.  Select `Enter` to see the variable definition.  -->  

À partir [de la version 88][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]de Microsoft Edge, le volet **Styles** affiche les variables CSS et fournit un lien directement vers la définition de chaque variable.  Dans Microsoft Edge version 91 ou ultérieure, vous pouvez utiliser les touches de direction pour accéder facilement aux variables CSS.  Pour ouvrir la définition dans le volet **Styles,** pointez sur une variable, puis sélectionnez `Enter` .  Pour plus d'informations sur les variables CSS, accédez à [l'utilisation de propriétés personnalisées CSS (variables).][MdnDocsWebCssUsingCssCustomProperties]  Pour passer en revue les mises à jour en temps réel de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1187735.][CR1187735]  

:::image type="complex" source="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png" alt-text="Variable CSS --theme-body-background mise en évidence dans le volet Styles" lightbox="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png":::
   Variable `--theme-body-background` CSS mise en évidence dans le **volet Styles**  
:::image-end:::  

## <a name="issues-are-automatically-sorted-by-severity"></a>Les problèmes sont automatiquement triés par gravité  

<!-- Title: Display Issues in severity order  -->  
<!-- Subtitle: Entries in the Issues tool now display in severity order and allow you to focus your updates on the most important issues. -->  

**L'outil Problèmes** affiche des recommandations pour améliorer votre site web, notamment l'accessibilité, les performances, la sécurité, etc. En fonction de vos commentaires, les problèmes sont désormais automatiquement triés par gravité.  Dans chaque catégorie de commentaires, **** chaque problème marqué comme erreur apparaît en premier, suivi de chaque problème marqué comme **avertissement,** puis de chaque problème marqué comme **conseil.**  Pour vous aider à affiner vos problèmes, des options de filtre supplémentaires sont prévues pour une prochaine mise à jour.  Pour plus d'informations sur la façon de passer en revue les problèmes, accédez à Rechercher et résoudre les problèmes avec l'outil Problèmes [DevTools][DevtoolsIssuesIndex]de Microsoft Edge.  

:::image type="complex" source="../../media/2021/04/elements-issues-ordered-issues.msft.png" alt-text="L'outil Problèmes affiche les problèmes triés par gravité" lightbox="../../media/2021/04/elements-issues-ordered-issues.msft.png":::
   **L'outil Problèmes** affiche les problèmes triés par gravité  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-117"></a>Outils de développement Microsoft Edge Visual Studio Code version 1.1.7  

<!-- Title: Microsoft Edge DevTools for Visual Studio version 1.1.7  -->  
<!-- Subtitle: Increased target closure reliability, automatically update the side panel, new contextual menu for settings and Changelog, and more. -->  

Microsoft [Edge Tools for Visual Studio Code extension][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] version 1.1.7 fournit devTools de Microsoft Edge version [88][DevtoolsWhatsNew202011Devtools].  Cette extension prend désormais en charge ARM et ne dépend plus [de l'extension Debugger pour Microsoft Edge.][VisualstudioMarketplaceMsjsdiagDebuggerForEdge]  La version 1.1.7 inclut les correctifs et améliorations de bogue suivants.  

*   Mise à jour de la fiabilité de la fermeture cible.  
*   Mise à jour du panneau latéral pour qu'il soit actualisé automatiquement lorsque vous déboguer des cibles créées ou détruites.  
*   Ajout d'un nouveau menu contextuel qui vous permet d'accéder plus rapidement aux paramètres d'extension et au dernier changelog.  
*   Mise à jour et simplification de la publication de la documentation d'extension, y compris les fonctionnalités les plus nouvelles.  
    
Pour mettre à jour manuellement la version 1.1.7, accédez à Mettre à jour [une extension manuellement.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  Vous pouvez signaler des problèmes, puis contribuer à l’extension sur le référentiel [GitHub vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools].  

<!--## Announcements from the Chromium project  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Ipsum et Chromium  

Lorem al lorem et Chromium  To review the history of this feature in the Chromium open-source project, navigate to Issue [xxxxxxx][CRxxxxxxx].  

:::image type="complex" source="../../media/2021/04/lorem-et-chromium.msft.png" alt-text="Ipsum et Chromium" lightbox="../../media/2021/04/lorem-et-chromium.msft.png":::
   Ipsum et Chromium  
:::image-end:::  -->  

## <a name="download-the-microsoft-edge-preview-channels"></a>Télécharger les canaux d’aperçu Microsoft Edge  

Si vous êtes sous Windows, Linux ou macOS, envisagez d'utiliser les [canaux d'aperçu de Microsoft][MicrosoftEdgePreviewChannels] Edge comme navigateur de développement par défaut.  Les canaux de prévisualisation vous donnent accès aux dernières fonctionnalités de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Contacter l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages]: ../../2020/01/devtools.md#using-the-devtools-in-other-languages "Utilisation de DevTools dans d'autres langues : nouveautés de DevTools (Microsoft Edge 81) | Documents Microsoft"  
[DevtoolsWhatsNew202011Devtools]: ../../2020/11/devtools.md "Nouveautés de DevTools (Microsoft Edge 88) | Documents Microsoft"  
[DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/11/devtools#css-variable-definitions-in-styles-pane "Définitions de variables CSS dans le volet Styles - Nouveautés de DevTools (Microsoft Edge 88) | Documents Microsoft"  
[DevtoolsWhatsNew202102Devtools]: ../02/devtools.md "Nouveautés de DevTools (Microsoft Edge 90) | Documents Microsoft"  
[DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode]: ../02/devtools.md#group-tools-together-in-focus-mode "Group tools together in Focus Mode - What's New In DevTools (Microsoft Edge 90) | Documents Microsoft"  

[DevtoolsCommandMenuIndexOpenCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index#open-the-command-menu "Ouvrez le menu Commande - Exécutez des commandes avec le menu DevTools Command de Microsoft Edge | Documents Microsoft"  
[DevtoolsCustomizeLocalization]: /microsoft-edge/devtools-guide-chromium/customize/localization "Modifier les paramètres de langue de DevTools | Documents Microsoft"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Recherchez et corrigez les problèmes liés à l’outil des problèmes de Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsServiceWorkerIndex]: /microsoft-edge/devtools-guide-chromium/service-workers/index "Améliorations apportées aux services | Documents Microsoft"  

[ProgressiveWebAppsServiceworkerServiceWorkerLifecycle]: /microsoft-edge/progressive-web-apps-chromium/serviceworker#the-service-worker-lifecycle "Cycle de vie des travailleurs du service : utiliser les travailleurs de service pour gérer les demandes réseau et les notifications Push | Documents Microsoft"  
[ProgressiveWebAppsWebappmanifests]: /microsoft-edge/progressive-web-apps-chromium/webappmanifests "Utiliser le manifeste de l'application Web pour intégrer votre application Web progressive au système d'exploitation | Documents Microsoft"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
<!--[GithubMicrosoftVscodeEdgeDevtoolsPullxxx]: https://github.com/microsoft/vscode-edge-devtools/pull/xxx "Pull xxx: Lorem al Ipsum | GitHub"  -->  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux de préversion de Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Mettre à jour une extension manuellement - Extension Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Outils Microsoft Edge pour Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerForEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Débogueur pour Microsoft Edge | Visual Studio Marketplace"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bogues Chromium"  
[CR1066604]: https://crbug.com/1066604 "Problème 1066604 : DevTools : voir les détails sur l'installation et l'activation des événements par ServiceWorker | Bogues Chromium"  
[CR1136655]: https://crbug.com/1136655 "Problème 1136655 : Devtools : localisation v2 | Bogues Chromium"  
[CR1185945]: https://crbug.com/1185945 "Problème 1185945 : l'avertissement de manifeste implique que toutes les icônes doivent être carrées | Bogues Chromium"  
[CR1187735]: https://crbug.com/1187735 "Problème 1187735 : Accessibilité : MAS2.1.1 : Clavier : Impossible d'appeler la fonction « Var(..) » à l'aide du clavier | Bogues Chromium"  

[MdnDocsWebCssUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Utilisation des propriétés personnalisées CSS (variables) | MDN"  

[PwabuilderImagegenerator]: https://www.pwabuilder.com/imageGenerator "Image Generator | PWABuilder"  

<!--  > [!NOTE]
> Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].  
> The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-91) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen
-->
