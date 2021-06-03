---
description: Fonctionnalités de débogage de grille CSS, demandes de modification et de relecture avec la console réseau, etc.
title: Nouveautés de DevTools (Microsoft Edge 85)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 75642a7f0fa8d6fae2f4daead84e2fc77df21e29
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564927"
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
# <a name="whats-new-in-devtools-microsoft-edge-85"></a>Nouveautés de DevTools (Microsoft Edge 85)  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Annonces de l’équipe Microsoft Edge DevTools  

Les sections suivantes sont une liste des annonces que vous avez peut-être manquées de l’équipe Microsoft Edge DevTools.  Consultez les annonces pour essayer de nouvelles fonctionnalités dans DevTools, Microsoft Visual Studio extensions de code, etc.  Pour rester à jour sur toutes les fonctionnalités les plus récentes et les plus importantes de vos outils de développement, téléchargez les canaux d’aperçu [Microsoft Edge][MicrosoftEdgePreviewChannels] et suivez l’équipe [Microsoft Edge DevTools][EdgeDevToolsTwitterAccount]sur Twitter.  

### <a name="css-grid-debugging-features"></a>Fonctionnalités de débogage de grille CSS  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalité expérimentale":::
   Fonctionnalité expérimentale  
:::image-end:::  

L’équipe Microsoft Edge DevTools collabore avec l’équipe Chrome DevTools et la communauté Chromium pour ajouter de nouvelles fonctionnalités de débogage de grille CSS à DevTools.  Vous pouvez désormais afficher les numéros de ligne de grille, les intervalles de grille et les lignes de grille étendue sous la mesure d’une superposition sur la page.  De plus, d’autres améliorations des outils de grille seront bientôt disponibles.  

:::image type="complex" source="../../media/2020/06/experiments-grid.msft.png" alt-text="Fonctionnalités de débogage de grille CSS" lightbox="../../media/2020/06/experiments-grid.msft.png":::
   Fonctionnalités de débogage de grille CSS
:::image-end:::  

> [!NOTE]
> Pour activer l’expérience, accédez à Activer les fonctionnalités expérimentales et activez la case à cocher en regard de Activer les nouvelles fonctionnalités de débogage de la **grille CSS.** [][DevtoolsExperimentalFeaturesTurnOn]  
> 
> Pour tester l’expérience avec un exemple, accédez à l’exemple de [planificateur CSS Grid.][CodepenRachelweilYzwBzKM]  

Chromium problème [#1047356][CR1047356]  

### <a name="edit-and-replay-requests-with-the-network-console"></a>Modifier et relire des demandes à l’aide de la console réseau  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalité expérimentale":::
   Fonctionnalité expérimentale  
:::image-end:::  

Vous pouvez désormais **** utiliser la modification et la relecture sur les demandes dans le journal [réseau][DevtoolsNetworkIndexLogActivity] à l’aide de la **console réseau.**  

:::image type="complex" source="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png" alt-text="Modifier et relire une demande dans NetworkLog avec la console réseau" lightbox="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png":::
   Modifier et relire une demande dans [NetworkLog][DevtoolsNetworkIndexLogActivity] avec la **console réseau**  
:::image-end:::  

Dans un nouveau panneau, la **console** réseau s’ouvre dans le panneau [DevTools][DevtoolsCustomizeIndexDrawer] et remplit automatiquement les informations de la requête HTTP.  Pour afficher la réponse renvoyée par le serveur, modifiez la demande \(si nécessaire\) et sélectionnez **Envoyer**.  

Vous pouvez également utiliser la **console réseau pour** créer et envoyer des demandes HTTP directement à partir de DevTools.  

:::image type="complex" source="../../media/2020/06/experiments-network-console.msft.png" alt-text="Panneau Console réseau" lightbox="../../media/2020/06/experiments-network-console.msft.png":::
   Panneau **Console** réseau  
:::image-end:::  

> [!TIP]
> Pour afficher **la console** réseau dans le panneau principal \(top\) au lieu du panneau [DevTools,][DevtoolsCustomizeIndexDrawer]accédez à déplacer des outils entre [des panneaux.](#move-tools-between-panels)  

> [!NOTE]
> Pour activer l’expérience, [accédez à Activer][DevtoolsExperimentalFeaturesTurnOn] les fonctionnalités expérimentales et cochez la case en regard de **Activer la console réseau.**  
> 
> Ouvrez [le journal réseau,][DevtoolsNetworkIndexLogActivity]ouvrez le menu contextuel \(clic droit\), puis choisissez **Modifier et relire.**  

Chromium problème [#1093687][CR1093687]  

### <a name="service-worker-respondwith-events-in-the-timing-tab"></a>Événements respondWith du service de travail dans l’onglet Minutage  

**L’onglet Calendrier** de **l’outil Réseau** inclut désormais les `respondWith` événements de travail de service.  L’événement de travail de service indique la durée entre l’heure immédiatement avant le début de l’exécution du handler d’événements de travail de service et le moment où la promesse du `respondWith` `fetch` `respondWith` `fetch` handler est réglée.  

:::image type="complex" source="../../media/2020/06/timing-tab.msft.png" alt-text="Événement de travail de service respondWith dans l’onglet Minutage du panneau Réseau" lightbox="../../media/2020/06/timing-tab.msft.png":::
   Événement `respondWith` de travail de service dans **l’onglet Minutage** de **l’outil** Réseau  
:::image-end:::  

Développez **la réponse reçue** pour afficher des informations supplémentaires à partir de la réponse telle que , et `fetch` `CacheStorageCacheName` `serviceWorkerResponseSource` `ResponseTime` .  

:::image type="complex" source="../../media/2020/06/timing-tab2.msft.png" alt-text="Développer la réponse reçue pour afficher des informations supplémentaires à partir de la réponse d’extraction" lightbox="../../media/2020/06/timing-tab2.msft.png":::
   Développer **la réponse reçue** pour afficher des informations supplémentaires à partir de la `fetch` réponse  
:::image-end:::  

Chromium problème [#1066579][CR1066579]  

### <a name="webhint-feedback-in-the-issues-panel"></a>commentaires webhint dans le panneau Problèmes  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalité expérimentale":::
   Fonctionnalité expérimentale  
:::image-end:::  

[webhint][WebhintMain] est un outil open source qui fournit des commentaires en temps réel sur l’accessibilité, la compatibilité entre navigateurs, la sécurité, les performances, les applications de bureau à long terme et d’autres problèmes de développement web courants liés aux sites web.  Pour passer en revue les commentaires sur les sites web dans [le panneau Problèmes.][DevtoolsIssues]  

:::image type="complex" source="../../media/2020/06/experiments-webhint.msft.png" alt-text="commentaires webhint dans le panneau Problèmes" lightbox="../../media/2020/06/experiments-webhint.msft.png":::
   commentaires webhint dans le panneau Problèmes  
:::image-end:::  

> [!NOTE]
> Pour activer l’expérience, [accédez à Activer][DevtoolsExperimentalFeaturesTurnOn] les fonctionnalités expérimentales et cochez la case en regard de **Activer lahint web.**  
> 
> Ouvrez [le panneau Problèmes][DevtoolsIssues] pour afficher les commentaires provenant de lahint web.  

Chromium problème [#1070378][CR1070378]  

### <a name="move-tools-between-panels"></a>Déplacer des outils entre des panneaux  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalité expérimentale":::
   Fonctionnalité expérimentale  
:::image-end:::  

Normalement, les outils **** tels que **Éléments** et Réseau peuvent uniquement être ouverts dans le panneau principal \(top\) de DevTools.  De même, les **outils** tels que l’affichage **3D** et les problèmes peuvent uniquement être ouverts dans le panneau de caisse \(bas\) de DevTools.  Vous pouvez désormais personnaliser votre disposition DevTools en déplaçant les outils entre les panneaux supérieur et inférieur.  

:::image type="complex" source="../../media/2020/06/experiments-move-panels.msft.png" alt-text="Déplacer des outils entre des panneaux" lightbox="../../media/2020/06/experiments-move-panels.msft.png":::
   Déplacer des outils entre des panneaux  
:::image-end:::  

> [!NOTE]
> Pour activer l’expérience, accédez à Activer les fonctionnalités expérimentales et activez la case à cocher en regard de Activer la prise en charge pour déplacer des onglets entre **les panneaux.** [][DevtoolsExperimentalFeaturesTurnOn]  

Chromium problème [#897944][CR897944]  

### <a name="improved-initiator-tooltip-in-the-network-panel"></a>Amélioration de l’aide de l’initiateur dans le panneau Réseau  

Dans Microsoft Edge 83 et 84, les bulles de la colonne Initiator, qui [][DevtoolsNetworkIndexLogActivity] indique la cause de la demande de ressource, dans le journal réseau affiché avec une barre de défilement horizontale.  Vous n’avez pu afficher la pile d’appels à l’origine de la demande qu’en faisant défiler horizontalement l’information dans l’bulle.  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-84.msft.png" alt-text="L’aide de l’initiateur Microsoft Edge 84" lightbox="../../media/2020/06/initiator-tooltip-84.msft.png":::
   L’aide de l’initiateur Microsoft Edge 84  
:::image-end:::  

À partir Microsoft Edge 85, vous pouvez désormais afficher la pile d’appels de l’initiateur dans l’bulle sans faire défiler horizontalement.  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-85.msft.png" alt-text="L’aide de l’initiateur Microsoft Edge 85" lightbox="../../media/2020/06/initiator-tooltip-85.msft.png":::
   L’aide de l’initiateur Microsoft Edge 85
:::image-end:::  

Chromium problème [#1069404][CR1069404]  

## <a name="announcements-from-the-chromium-project"></a>Annonces du projet de Chromium  

Les sections suivantes annoncent des fonctionnalités supplémentaires disponibles dans Microsoft Edge 85 qui ont été contribués au projet d’Chromium open source.  

### <a name="style-editing-for-css-in-js-frameworks"></a>Modification du style pour les frameworks CSS-in-JS  

Le **volet Styles** a désormais une meilleure prise en charge de l’édition des styles créés avec les API [CSS Object Model (CSSOM).][CsswgDraftsCssom]  De nombreuses bibliothèques et infrastructure CSS-in-JS utilisent les API CSSOM sous-programme pour construire des styles.  

Vous pouvez désormais modifier les styles ajoutés dans JavaScript à l’aide [de feuilles de style constructables.][WicgConstructStylesheet]  Les feuilles de style constructables sont un nouveau moyen de créer et de distribuer des styles réutilisables lors de l’utilisation [du DOM d’ombre.][MdnShadowDom]  

Par exemple, les `h1` styles ajoutés avec `CSSStyleSheet` \(API CSSOM\) n’étaient pas modifiables précédemment.  Les styles sont désormais modifiables dans le **panneau Styles.**  

:::image type="complex" source="../../media/2020/06/css-in-js.msft.png" alt-text="Modification de la propriété d’arrière-plan des styles h1 ajoutés avec CSSStyleSheet de rose à lightblue" lightbox="../../media/2020/06/css-in-js.msft.png":::
   Modification de `background` la propriété des styles `h1` ajoutés à partir de `CSSStyleSheet` `pink` `lightblue` .
:::image-end:::  

Essayez cette fonctionnalité avec un [exemple qui utilise CSS-in-JS][CodepenZoherghadyaliAbdgrpz].

Chromium problème [#946975][CR946975]  

### <a name="lighthouse-6-in-the-lighthouse-panel"></a>Phare 6 dans le panneau Panneau de sélection  

Le **panneau Panneau** de bord exécute désormais Le Phare 6.  Pour obtenir la liste complète de toutes les modifications, accédez aux notes de publication [v6.0.0.][GithubGoogleChromeLighthouse600]  

La classe 6.0 présente trois nouvelles mesures dans le rapport : Largest Contentful Paint \(LCP\), Cumulative Layout Shift \(CLS\) et Total Blocking Time \(TBT\).  

La formule de score de performance a également été reweightée pour mieux refléter l’expérience de chargement de l’utilisateur.  

Chromium problème [#772558][CR772558]  

#### <a name="first-meaningful-paint-deprecation"></a>Première désintécation Paint significative  

First Meaningful Paint \(FMP\) is deprecated in Cev 6.0.  FMP a également été supprimé du panneau **Performances.**  **La plus grande Paint** contentful est le remplacement recommandé pour le FMP.  <!--For an explanation of why it was deprecated, navigate to [First Meaningful Paint][WebDevFirstMeaningfulPaint].  -->  

<!--todo: add Largest Contentful Paint when section available  -->  
<!--todo: add First Meaningful Paint link and note when available  -->  

Chromium problème [#1096008][CR1096008]  

### <a name="support-for-new-javascript-features"></a>Prise en charge des nouvelles fonctionnalités JavaScript  

DevTools offre désormais une meilleure prise en charge de certaines des dernières fonctionnalités de langage JavaScript.  

:::row:::
   :::column span="1":::
      [Autocompletion automatique][V8DevOptionalChaining] de la syntaxe de chaînage facultative  
   :::column-end:::
   :::column span="2":::
      L’achèvement automatique de propriété dans la **console prend** désormais en charge la syntaxe de chaînage facultative, par exemple, fonctionne désormais en plus de  `name?.` et `name.` `name[` .  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Mise en surbrillance de [syntaxe pour les champs privés][V8DevClassFieldsPrivate]  
   :::column-end:::
   :::column span="2":::
      les champs de classe privés sont désormais correctement mis en surbrillantes et assez imprimés dans le **panneau Sources.**  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Mise en surbrillance de la [syntaxe pour l’opérateur de hillage nullish][V8DevNullishCoalescing]
   :::column-end:::
   :::column span="2":::
      DevTools imprime maintenant correctement l’opérateur de houillement nullish dans le **panneau Sources.**  
   :::column-end:::
:::row-end:::  

Chromium [problèmes][CR1073903]#1073903, [#1083214,][CR1083214] [#1083797][CR1083797]  

### <a name="new-app-shortcut-warnings-in-the-manifest-pane"></a>Avertissements de raccourcis de nouvelle application dans le volet manifeste  

**Les raccourcis d’application** aident les utilisateurs à démarrer rapidement des tâches courantes ou recommandées dans une application web.  

<!--todo: add App shortcuts when section is live  -->  

Le **volet Manifeste** affiche désormais des avertissements pour les conditions suivantes.  

* Les icônes de raccourci de l’application sont plus petites que 96 x 96 pixels  
* Les icônes de raccourci de l’application et les icônes de manifeste ne sont pas carrées \(étant donné que les icônes sont ignorées\)  

:::image type="complex" source="../../media/2020/06/app-shortcut-warnings.msft.png" alt-text="Avertissements de raccourcis d’application" lightbox="../../media/2020/06/app-shortcut-warnings.msft.png":::
   Avertissements de raccourcis d’application  
:::image-end:::  

Chromium problème [#955497][CR955497]  

### <a name="consistent-display-of-the-computed-pane"></a>Affichage cohérent du volet calculé  

Le **volet Calculé** de l’outil **Éléments** s’affiche désormais de manière cohérente sous la forme d’un volet dans toutes les tailles de laport d’affichage.  **Auparavant, le volet Calculé** fusionnait à l’intérieur du volet **Styles** lorsque la largeur de laport d’affichage DevTools était étroite.  

:::image type="complex" source="../../media/2020/06/computed-pane.msft.png" alt-text="Le volet Calculé s’affiche de manière cohérente sous la forme d’un volet distinct, même lorsque les DevTools sont étroits" lightbox="../../media/2020/06/computed-pane.msft.png":::
   Le **volet Calculé** s’affiche de manière cohérente sous la forme d’un volet distinct, même lorsque les DevTools sont étroits.
:::image-end:::  

Chromium problème [#1073899][CR1073899]  

### <a name="bytecode-offsets-for-webassembly-files"></a>Décalages de bytecode pour les fichiers WebAssembly  

DevTools utilise désormais des décalages de bytecode pour afficher les numéros de ligne wasm disassembly.  
Les numéros de ligne vous indiquent plus clairement que vous regardez les données binaires et sont plus cohérents avec la façon dont le runtime Wasm référence les emplacements.  

Chromium problème [#1071432][CR1071432]  

### <a name="line-wise-copy-and-cut-in-sources-panel"></a>Copier et couper au sens de la ligne dans le panneau Sources  

Lorsque vous effectuez une copie ou une coupure sans sélection dans l’éditeur du panneau [Sources,][DevtoolsSourcesIndexUsingEditorPaneToViewEditFiles]DevTools copie ou coupe la ligne de contenu actuelle.  

:::image type="complex" source="../../media/2020/06/line-wise-cut.msft.png" alt-text="Avec le curseur à la fin de la ligne 5, copiez la ligne entière à partir de pen.js dans devTools et coller dans Visual Studio Code" lightbox="../../media/2020/06/line-wise-cut.msft.png":::
   Avec le curseur à la fin de la ligne 5, copiez la ligne entière à partir de **pen.js** dans devTools et coller dans [Visual Studio Code][VisualStudioCode].
:::image-end:::  

Chromium problème [#800028][CR800028]

### <a name="console-settings-updates"></a>Mises à jour Paramètres console  

#### <a name="ungroup-same-console-messages"></a>Dégrouper les mêmes messages de console  

Le **basculement de groupe** similaire dans console Paramètres s’applique désormais aux messages en double.  Auparavant, il vient d’être appliqué à des messages similaires.  

Par exemple, auparavant, DevTools n’a pas désgroupé les messages même si le groupe similaire `hello` est désactivé. ****  À présent, `hello` les messages sont désgroupés.  

:::image type="complex" source="../../media/2020/06/ungroup-similar.msft.png" alt-text="Lorsque le groupe similaire est désactivé, les messages Hello sont désgroupés" lightbox="../../media/2020/06/ungroup-similar.msft.png":::
   Lorsque **le groupe similaire** est désactivé, les messages sont `hello` désgroupés
:::image-end:::  

Essayez cette fonctionnalité avec un [exemple qui envoie des messages en double à la console.][CodepenZoherghadyaliZyrjgdJ]  

Chromium problème [#1082963][CR1082963]  

### <a name="persisting-selected-context-only-settings"></a>Persistance des paramètres de contexte sélectionné uniquement  

Les **paramètres de contexte sélectionnés** uniquement dans console Paramètres sont désormais persistants.  Auparavant, les paramètres étaient réinitialisés chaque fois que vous avez fermé et rouvert DevTools.  La modification rend le comportement du paramètre cohérent avec les autres options Paramètres console.  

:::image type="complex" source="../../media/2020/06/selected-context.msft.png" alt-text="Paramètre de contexte uniquement sélectionné" lightbox="../../media/2020/06/selected-context.msft.png":::
   **Paramètre de contexte uniquement** sélectionné  
:::image-end:::  

Chromium problème [#1055875][CR1055875]  

### <a name="performance-panel-updates"></a>Mises à jour du panneau de performances  

#### <a name="javascript-compilation-cache-information-in-performance-tool"></a>Informations sur le cache de compilation JavaScript dans **l’outil Performance**  

[Les informations du cache de compilation JavaScript][V8DevCodeCaching] sont désormais toujours affichées dans le panneau Résumé de l’outil **** **Performance.**  Auparavant, DevTools n’avait rien à voir avec la mise en cache du code si la mise en cache du code ne s’était pas produit.  

:::image type="complex" source="../../media/2020/06/js-compilation-cache.msft.png" alt-text="Informations sur le cache de compilation JavaScript" lightbox="../../media/2020/06/js-compilation-cache.msft.png":::
   Informations sur le cache de compilation JavaScript  
:::image-end:::  

Chromium problème [#912581][CR912581]  

#### <a name="navigation-timing-alignment-in-the-performance-panel"></a>Alignement du minutage de navigation dans le panneau Performances  

Panneau **Performances** utilisé pour afficher les heures dans les règles en fonction du moment où l’enregistrement a démarré.  Le minutage a changé pour les enregistrements où l’utilisateur navigue, où DevTools affiche désormais les heures de règle par rapport à la navigation.  

:::image type="complex" source="../../media/2020/06/nav-timing.msft.png" alt-text="Aligner le minutage de navigation dans l’outil Performances" lightbox="../../media/2020/06/nav-timing.msft.png":::
   Aligner le minutage de navigation dans **l’outil Performances**  
:::image-end:::  

Les heures des événements , First Paint, First Contentful Paint et Largest Contentful Paint sont mises à jour pour être relatives au début de la navigation, ce qui signifie que le minutage correspond aux minutages signalés par `DOMContentLoaded` `PerformanceObserver` .  

Chromium problème [#974550][CR974550]  

### <a name="new-icons-for-breakpoints-conditional-breakpoints-and-logpoints"></a>Nouvelles icônes pour les points d’arrêt, les points d’arrêt conditionnels et les points d’accès  

Le **panneau Sources** offre de nouvelles conceptions pour les points d’arrêt, les points d’arrêt conditionnels et les points d’accès.  Les points d’arrêt sont représentés par un cercle rouge, comme [Visual Studio Code][VisualStudioCode] et [Visual Studio][VisualStudio].  Des icônes sont ajoutées pour différencier les points d’arrêt conditionnels et les points d’accès.  

:::image type="complex" source="../../media/2020/06/breakpoints.msft.png" alt-text="Points d’arrêt" lightbox="../../media/2020/06/breakpoints.msft.png":::
   Points d’arrêt  
:::image-end:::  

Chromium problème [#1041830][CR1041830]  

## <a name="download-the-microsoft-edge-preview-channels"></a>Télécharger les canaux d’aperçu Microsoft Edge  

Si vous êtes sur Windows ou macOS, envisagez d’utiliser les canaux d Microsoft Edge [d’aperçu][MicrosoftEdgePreviewChannels] comme navigateur de développement par défaut.  Les canaux de prévisualisation vous donnent accès aux dernières fonctionnalités de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Contacter l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsIndex]: ../../../index.md "Microsoft Edge outils de développement (Chromium) | Documents Microsoft"  
[DevtoolsCommandMenu]: ../../../command-menu.md "Exécuter des commandes avec le menu de Microsoft Edge DevTools | Documents Microsoft"
[DevtoolsCustomizeIndexDrawer]: ../../../customize/index.md#drawer "Caisse : personnaliser Microsoft Edge devTools | Documents Microsoft"
[DevtoolsExperimentalFeaturesTurnOn]: ../../../experimental-features/index.md#turn-on-experimental-features "Activer les fonctions expérimentales – Fonctions expérimentales | Microsoft Docs"  
[DevtoolsIssues]: ../../../issues/index.md "Recherchez et corrigez les problèmes liés à l’outil des problèmes de Microsoft Edge DevTools | Documents Microsoft"
[DevtoolsSourcesIndexUsingEditorPaneToViewEditFiles]: ../../../sources/index.md#using-the-editor-pane-to-view-or-edit-files "Utilisation du volet Éditeur pour afficher ou modifier des fichiers - Vue d’ensemble du panneau Sources | Documents Microsoft"  
[DevtoolsNetworkIndexLogActivity]: ../../../network/index.md#log-network-activity "Journal de l’activité réseau : inspecter l’activité réseau dans Microsoft Edge devTools | Documents Microsoft"

[CodepenZoherghadyaliAbdgrpz]: https://codepen.io/zoherghadyali/full/abdGrPZ "Modification du style pour les frameworks CSS-in-JS | CodePen"
[CodepenZoherghadyaliZyrjgdJ]: https://codepen.io/zoherghadyali/full/zYrjgdJ "Envoyer des messages en double à la console | CodePen"
[CodepenRachelweilYzwBzKM]: https://codepen.io/hxlnt/full/YzwBzKM "Exemple de planificateur CSS Grid | CodePen"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bogues Chromium"  

[CR772558]: https://crbug.com/772558 "DevTools : mise à jour vers la dernière version de | Chromium bogues"  
[CR800028]: https://crbug.com/800028 "Le raccourci de ligne en double dans l’éditeur outils de développement ne fonctionne pas après la mise à jour de Chrome | Chromium bogues"  
[CR912581]: https://crbug.com/912581 "Exposer les scripts qui ont été mis en cache par code par V8 dans DevTools/about:tracing | Chromium bogues"  
[CR946975]: https://crbug.com/946975 "La barre latérale Styles DevTools ne fonctionne pas avec les feuilles de style | Chromium bogues"  
[CR955497]: https://crbug.com/955497 "Menu raccourci d’icône d’application pour les applications de | Chromium bogues"  
[CR974550]: https://crbug.com/974550 "Non-matisation des mesures entre le panneau Perf et performanceObserver | Chromium bogues"  
[CR1041830]: https://crbug.com/1041830 "Améliorer les couleurs des points d’arrêt | Chromium bogues"  
[CR1055875]: https://crbug.com/1055875 "La valeur du paramètre de console Contexte uniquement sélectionné ne persiste pas après la fermeture et la réouverture des outils de développement | Chromium bogues"  
[CR1066579]: https://crbug.com/1066579 "DevTools : afficher la chronologie d’extraction serviceWorkers par demande dans le panneau | Chromium bogues"  
[CR1071432]: https://crbug.com/1071432 "Wasm Basic Developer Experience | Chromium bogues"  
[CR1073899]: https://crbug.com/1073899 "L’onglet Style calculé disparaît en mode | Chromium bogues"  
[CR1073903]: https://crbug.com/1073903 "DevTools : la mise en surbrillance de la syntaxe ne fonctionne pas avec les champs privés | Chromium bogues"  
[CR1082963]: https://crbug.com/1082963 "Can’t disable console’s Group similar messages behavior | Chromium bogues"  
[CR1083214]: https://crbug.com/1083214 "acorn ne prend pas en charge le chaînage facultatif | Chromium bogues"  
[CR1083797]: https://crbug.com/1083797 "Impression assez rompue pour la | Chromium bogues"  
[CR1096008]: https://crbug.com/1096008 "Supprimer les | FMP Chromium bogues"  
[CR1047356]: https://crbug.com/1047356 "Outils Grille CSS/Flexbox/Tableau | Chromium bogues"  
[CR1093687]: https://crbug.com/1093687 "Créer un outil pour créer et relire des demandes de réseau synthétique | Chromium bogues"  
[CR1070378]: https://crbug.com/1070378 "Intégrer webhint dans devTools | Chromium bogues"  
[CR1069404]: https://crbug.com/1069404 "Les fenêtres pop-up de widget [Outils de développement] sont trop | Chromium bogues"  
[CR897944]: https://crbug.com/897944 "Panneaux de | Chromium bogues"

[GithubGoogleChromeLighthouse600]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.0.0 "v6.0.0 - GoogleChrome/| GitHub"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Nouveau problème : MicrosoftDocs/edge-developer"  

[MdnShadowDom]: https://developer.mozilla.org/docs/Web/Web_Components/Using_shadow_DOM "Utilisation du dom d’ombre | MDN"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download/ "Canaux de préversion de Microsoft Edge"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"
[VisualStudioCode]: https://code.visualstudio.com/ "Code Visual Studio"  

[CsswgDraftsCssom]: https://drafts.csswg.org/cssom "Modèle objet CSS (CSSOM) | Brouillons de l’éditeur de groupe de travail CSS W3C"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publier un Tweet"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools compte Twitter"  

[V8DevClassFieldsPrivate]: https://v8.dev/features/class-fields#private-class-fields "Champs de classe privés : champs de classes publiques et privées | V8. Dev"  
[V8DevCodeCaching]: https://v8.dev/blog/code-caching-for-devs "Mise en cache du code pour les développeurs JavaScript | V8. Dev"  
[V8DevNullishCoalescing]: https://v8.dev/features/nullish-coalescing "A la fois null et | V8. Dev"  
[V8DevOptionalChaining]: https://v8.dev/features/optional-chaining "Chaîne facultative | V8. Dev"  

[WebhintMain]: https://webhint.io "webhint"  

[WicgConstructStylesheet]: https://wicg.github.io/construct-stylesheets/ "Objets Stylesheet constructables | Groupe de recherche de contenu Web (CG) Web"

<!--[WebDevLighthouseWhatsNew60]: https://web.dev/lighthouse-whats-new-6.0 "What's New in Lighthouse 6.0 | Web.Dev"  -->  
<!--[WebDevVitalsCoreWeb]: https://web.dev/vitals#core-web-vitals "Core Web Vitals - Web Vitals | Web.Dev"  -->  
<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebFundamentalComponentsShadowdom]: /web/fundamentals/web-components/shadowdom  -->  
<!--[WebDevLcp]: https://web.dev/lcp "Largest Contentful Paint (LCP) | Web.Dev"  -->  
<!--[WebDevFirstMeaningfulPaint]: https://web.dev/first-meaningful-paint "First Meaningful Paint | Web.Dev"  -->  
<!--[WhatsNew201902ConstructableStylesheets]: ../../2019/02/constructable-stylesheets.md "Constructable Stylesheets: seamless reusable styles | Microsoft Docs"  -->  

[TheWebWeWant]: https://webwewant.fyi/ "Le site Web de votre choix"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developer.chrome.com/blog/new-in-devtools-85) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
