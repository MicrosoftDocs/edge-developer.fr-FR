---
title: Nouveautés de DevTools (Microsoft Edge 80)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 03fd78eddf54b68d072ba11401a897ad9f109058
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942148"
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

# Nouveautés de DevTools (Microsoft Edge 80)  

## Annonces de l’équipe Microsoft Edge DevTools  

Les sections suivantes répertorient les annonces que vous pouvez avoir manquées de l’équipe Microsoft Edge DevTools. Découvrez-les pour essayer de nouvelles fonctionnalités dans les extensions de code DevTools, VS, etc.  Pour vous tenir au courant de toutes les fonctionnalités les plus récentes et les plus récentes de vos outils de développement, téléchargez les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] et [Suivez-nous sur Twitter][EdgeDevToolsTwitterAccount].  

### Améliorations de l’accessibilité dans DevTools  

L’équipe DevTools a 170 contribué aux modifications apportées à Chrome pour répondre aux problèmes de contraste des couleurs, de clavier et de lecteur d’écran à forte incidence dans DevTools.  Tout développeur bâtiment sur le Web doit être en mesure d’utiliser le DevTools.  

> ##### Figure1  
> Outil performance dans le DevTools avec les améliorations de la navigation au clavier et du lecteur d’écran  
> ![Outil performance dans le DevTools avec les améliorations de la navigation au clavier et du lecteur d’écran][ImagePerformanceToolKeyboardReaderImprovements]  

Vous voulez savoir comment rendre votre page Web accessible à tous vos utilisateurs?  Téléchargez les informations [d’accessibilité][AccessibilityInsights] et les extensions [Webhint][WebhintBrowserExtension] pour Microsoft Edge pour commencer.  

Si vous utilisez un lecteur d’écran ou le clavier pour naviguer dans DevTools, envoyez-nous vos commentaires en nous appuyant sur un [Tweet][PostTweetEdgeDevTools] ou en cliquant sur l’icône d' [envoi de commentaires](#getting-in-touch-with-microsoft-edge-devtools-team) .  

[#963183][crbug963183] problème de chrome  

### Utiliser le DevTools dans d’autres langues  

De nombreux développeurs utilisent d’autres outils de développement tels que StackOverflow et le code VS, dans leur langue maternelle, et pas seulement en anglais.  Nous sommes heureux d’annoncer la localisation de DevTools, que vous pouvez désormais utiliser dans l’un des 10 langues autres que l’anglais:  

:::row:::
   :::column span="":::
      Chinois (simplifié)- &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;
   :::column-end:::
   :::column span="":::
      Chinois (traditionnel)- &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Français-Fran&#231;AIS
   :::column-end:::
   :::column span="":::
      Allemand-Deutsch
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Italien-Italiano
   :::column-end:::
   :::column span="":::
      Japonais- &#26085;&#26412;&#35486;
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Coréen- &#54620;&#44397;&#50612;
   :::column-end:::
   :::column span="":::
      Portugais-portugu&#234;s
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Russe- &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;
   :::column-end:::
   :::column span="":::
      Espagnol-ESPA&#241;ol
   :::column-end:::
:::row-end:::

<!--  
|  |  |  
|:--- |:--- |  
| Chinese (Simplified) - 中文（简体）| Chinese (Traditional) - 中文（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

Accédez à `edge://flags` l’indicateur d' **activation des outils de développement localisé** et définissez-le sur **activé**.  Définissez également l’indicateur **expériences des outils de développement** sur **activé**.  Redémarrez Microsoft Edge et ouvrez le DevTools.  <!-- Press `F1` in the DevTools or go to Settings > Experiments and check the **Match browser language** checkbox.  -->  Le DevTools correspond à la langue que vous utilisez pour Microsoft Edge dans `edge://settings/languages` .  

> ##### Figure 2  
> DevTools en allemand  
> ![DevTools en allemand][ImageLocalizedGerman]  

Si vous souhaitez utiliser le DevTools dans une autre langue que celle proposée, vous pouvez utiliser le [Tweet][PostTweetEdgeDevTools] ou cliquez sur l’icône d' [envoi de commentaires](#getting-in-touch-with-microsoft-edge-devtools-team) .  

[#941561][crbug941561] problème de chrome  

### extension Microsoft Edge de webhint  

L’extension Microsoft Edge de Microsoft vous permet d’analyser facilement votre page Web et de faire des commentaires sur l’accessibilité, la compatibilité avec les navigateurs, la sécurité et les performances, etc., dans le DevTools.  Pour en savoir plus [https://webhint.io][Webhint] , voir.  

> ##### Figure3  
> Onglet Hints dans le DevTools lorsque l’extension de navigateur webhint est installée  
> ![Onglet Hints dans le DevTools lorsque l’extension de navigateur webhint est installée][ImageHintsTabWebhintExtension]  

[Essayez l’extension de navigateur webhint dans Microsoft Edge][MicrosoftEdgeInsiderAddons].  Une fois l’extension installée, ouvrez le DevTools et sélectionnez l’onglet conseils.  À partir de là, effectuez une analyse de site personnalisable.  Accédez à [webhint.IO][WebhintBrowserExtension] pour en savoir plus.

### Vue 3D  

Utilisez la **vue 3D** pour déboguer votre application Web en naviguant dans le [modèle d’objet de document \ (DOM \)][MDNDocumentObjectModel] ou le contexte de pile [de l’index z][MDNZIndex] .  

> ##### Figure 4  
> Affichage 3D dans le DevTools  
> ![Affichage 3D dans le DevTools][Image3DView]  

Pour accéder à la vue 3D, accédez à l' `edge://flags` indicateur d' **expériences outils de développement** et vérifiez qu’il est défini sur **activé**.  Redémarrez Microsoft Edge et ouvrez le DevTools.  Appuyez sur `F1` le devtools ou accédez à **paramètres**, accédez à la section **expériences** , puis activez la case à cocher **activer le mode 3D** .  À présent, appuyez sur la touche `Ctrl`  +  `Shift`  +  `P` **affichage 3D** et sélectionnez **afficher la vue 3D**.  

Nous travaillons sur l’interface utilisateur et nous ajoutons d’autres fonctionnalités à la vue 3D; nous vous envoyons donc votre [avis](#getting-in-touch-with-microsoft-edge-devtools-team).  

[#987787][crbug987787] problème de chrome

### Extensions de code Visual Studio  

L’équipe DevTools a également émis certaines extensions pour le [code Visual Studio \ (vs code \)][VisualStudioCode] qui vous permettent d’utiliser la puissance de devtools directement à partir de votre éditeur de texte. Consultez les extensions suivantes:  

#### Éléments pour Microsoft Edge  

Utilisez l’outil éléments du code VS, en ajoutant les éléments de l’extension du code [Microsoft Edge \ (chrome \)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] .  

> ##### Figure 5  
> Outil éléments du code VS utilisant les éléments de l’extension Microsoft Edge  
> ![Outil éléments du code VS utilisant les éléments de l’extension Microsoft Edge][ImageElementsVisualStudioCode]  

Pour plus d’informations, consultez les [éléments pour l’extension de code Microsoft Edge vs][VisualStudioCodeElementEdgeExtension].  

#### Débogueur pour Microsoft Edge  

Avec le [débogueur pour l’extension de code Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] vs, déboguez JavaScript en cours d’exécution dans Microsoft Edge directement à partir du code vs.  

> ##### Figure 6  
> Débogueur de l’extension Microsoft Edge dans le code VS  
> ![Débogueur de l’extension Microsoft Edge dans le code VS][ImageDebuggerExtensionVisualStudioCode]  

Pour plus d’informations, voir [Comment déboguer Microsoft Edge du code vs][VisualStudioCodeDebuggerEdgeExtension].  

#### webhint  

L’extension de code [webhint][VisualStudioMarketplaceWebhintExtension] et `webhint` de code vous permet d’améliorer votre page Web lorsque vous rédigez un message. Cette extension exécute et signale les diagnostics de vos fichiers d’espace de travail en fonction de l' `webhint` analyse.  

> ##### Figure 7  
> Extension de code webhint et analyse d’un fichier. TSX dans le code VS  
> ![Extension de code webhint et analyse d’un fichier. TSX dans le code VS][ImageWebhintVisualStudioCodeExtensionWorkspace]  

[En savoir plus sur l’extension du webhint code vs][WebhintVisualStudioCodeExtension].  

### Intégration de Visual Studio
Dans Visual Studio 2019 version 16,2 ou ultérieure, utilisez le débogueur Visual Studio pour déboguer JavaScript en cours d’exécution dans Microsoft Edge.  [Téléchargez Visual Studio 2019][MicrosoftVisualStudioDownloads] pour essayer cette fonctionnalité.  

> ##### Figure8  
> Visual Studio avec l’option de lancement de votre application Web dans Microsoft Edge Canaries, dev ou Beta  
> ![Visual Studio avec l’option de lancement de votre application Web dans Microsoft Edge Canaries, dev ou Beta][ImageVisualStudioLaunchWebApp]  

[Pour plus d’informations sur le débogage de Microsoft Edge à partir de Visual Studio, consultez notre billet de blog][MicrosoftVisualStudioBlogDebugJavascript].  

### Suivi des messages de la console de prévention  

La prévention de suivi est une fonctionnalité unique de Microsoft Edge qui vous protège du suivi par des sites Web que vous n’avez pas encore visités.  Le paramètre de prévention du suivi par défaut est le mode équilibré, qui permet de bloquer des suivis tiers et des pistes malveillantes connues pour une interface qui équilibre la confidentialité et la compatibilité Web.  Pour plus d’informations sur la compatibilité de votre page Web lorsque certains suivis sont bloqués, nous avons également ajouté des messages d’avertissement dans la console lorsqu’un suivi est bloqué.  

> ##### Figure9  
> Messages dans la console lors du suivi de la prévention bloquer l’accès au stockage pour un suivi  
> ![Messages dans la console lors du suivi de la prévention bloquer l’accès au stockage pour un suivi][ImageTrackingPrevention]  

[En savoir plus sur la prévention de suivi et le compromis entre la confidentialité et la compatibilité Web][TrackingPrevention].  

## Annonces du projet de chrome  

Les sections suivantes annoncent des fonctionnalités supplémentaires disponibles dans Microsoft Edge 80 qui ont été fournies au projet de chrome Open source.  

### Prise en charge de la redéclaration de la classe et des classes dans la console  

La console prend désormais en charge les redéclarations `let` et les `class` instructions.  L’impossibilité de redéclarer est une gêne pour les développeurs Web qui utilisent la console pour tester le nouveau code JavaScript.  

> [!WARNING]
> La redéclaration d’une `let` instruction ou d’un `class` script en dehors de la console, ou au sein d’une seule et même entrée de console entraîne une `SyntaxError` .  

Par exemple, auparavant, lors de la redéclaration d’une variable locale avec `let` , la console a renvoyé une erreur:  

> ##### Figure10  
> La console dans Microsoft Edge 79 indiquant l’échec de la redéclaration  
> ![La console dans Microsoft Edge 79 indiquant l’échec de la redéclaration][ImageConsoleRedeclarationFails]  

À présent, la console autorise la redéclaration:  

> ##### Figure11  
> Console dans Microsoft Edge 80 indiquant que la redéclaration de réussite est réussie  
> ![Console dans Microsoft Edge 80 indiquant que la redéclaration de réussite est réussie][ImageConsoleRedeclarationSucceeds]  

[#1004193][crbug1004193] problème de chrome  

### Débogage d’assembly améliorée  

DevTools a commencé à prendre en charge la [norme de débogage de nain][DwarfHome], ce qui signifie qu’il s’agit d’une prise en charge accrue pour le code pas à pas, la définition de points d’arrêt et la résolution de traces de pile dans vos langages sources dans devtools.  

<!-- [TODO: Add this link back] -->  
<!--Check out [Improved WebAssembly debugging in Microsoft Edge DevTools][201912Webassembly] for the full story.  -->  

<!-- [TODO: Replace this image with screenshot in Edge] -->  
<!--
> ##### Figure  
> The new DWARF-powered WebAssembly debugging  
> ![The new DWARF-powered WebAssembly debugging][ImageDwarfPoweredWebAssemblyDebugging]  
-->  

### Mises à jour du panneau réseau  

#### Chaînes d’initiateur de requête dans l’onglet initiateur  

Vous pouvez à présent afficher les initiateurs et les dépendances d’une demande réseau en tant que liste imbriquée.  Cela risque de vous aider à comprendre la raison pour laquelle une ressource a été demandée ou l’activité réseau pour laquelle une ressource (par exemple, un script) a été créée.  

> ##### Figure12  
> Chaîne d’initiateur de requête dans l’onglet initiateur  
> ![Chaîne d’initiateur de requête dans l’onglet initiateur][ImageRequestInitiatorChain]  

Après la [journalisation de l’activité réseau dans le panneau réseau][DevToolsNetworkIndex], cliquez sur une ressource, puis accédez à l’onglet **initiateur** pour afficher la chaîne d’initiateur de la **requête**:  

*   La **ressource inspectée** est en gras.  Dans la capture d’écran ci-dessus, `ai.2.min.js` figure la ressource inspectée.  
*   Les ressources au-dessus de la ressource inspectée sont les **initiateurs**.  Dans la capture d’écran ci-dessus, `https://www.microsoftedgeinsider.com` est l’initiateur de `ai.2.min.js` .  En d’autres termes, à `https://www.microsoftedgeinsider.com` l’origine de la demande de réseau `ai.2.min.js` .  
*   Les ressources sous la ressource inspectée sont les **dépendances**.  Dans la capture d’écran ci-dessus, `https://dc.services.visualstudio.com/v2/track` il existe une dépendance `ai.2.min.js` .  En d’autres termes, à `ai.2.min.js` l’origine de la demande de réseau `https://dc.services.visualstudio.com/v2/track` .  

> [!NOTE]
> Il est également possible d’accéder à des informations d’initiateur et de dépendance en Holding `Shift` puis en pointant sur les ressources réseau.  Voir [les initiateurs de vues et les dépendances][DevToolsNetworkReferenceViewInitiatorsDependencies].  

[#842488][crbug842488] problème de chrome  

#### Mettre en surbrillance la demande réseau sélectionnée dans la vue d’ensemble  

Après avoir cliqué sur une ressource réseau pour la vérifier, le panneau réseau place désormais une bordure bleue autour de celle-ci dans la **vue d’ensemble**.  Cela peut vous aider à détecter si la demande de réseau se produit avant ou après la fin prévue.  

> ##### Figure13  
> Volet vue d’ensemble mettant en évidence la ressource inspectée  
> ![Volet vue d’ensemble mettant en évidence la ressource inspectée][ImageOverviewPaneInspectedResource]  

[#988253][crbug988253] problème de chrome  

#### Colonnes d’URL et de chemin d’accès dans le panneau réseau  

Utilisez les nouvelles colonnes **path** et **URL** du panneau **réseau** pour afficher le chemin d’accès absolu ou l’URL complète de chaque ressource réseau.  

> ##### Figure14  
> Les nouvelles colonnes Path et URL du panneau réseau  
> ![Les nouvelles colonnes Path et URL du panneau réseau][ImagePathNetworkPanel]  

Cliquez avec le bouton droit sur l’en-tête de tableau en **cascade** , puis sélectionnez **chemin** ou **URL** pour afficher les nouvelles colonnes.  

[#993366][crbug993366] problème de chrome  

#### Chaînes d’agent utilisateur mises à jour  

DevTools prend en charge la définition d’une chaîne d’agent utilisateur personnalisée par le biais de l’onglet **conditions réseau** .  La chaîne de l’agent utilisateur affecte l' `User-Agent` en-tête http attaché aux ressources réseau, ainsi que la valeur de `navigator.userAgent` .  

Les chaînes d’agent utilisateur prédéfinies ont été mises à jour pour refléter les versions modernes du navigateur.  

> ##### Figure15  
> Menu agent utilisateur de l’onglet conditions réseau  
> ![Menu agent utilisateur de l’onglet conditions réseau][ImageUserAgentNetworkConditionsTab]  

Pour accéder aux **conditions du réseau**, [Ouvrez le menu de commandes][DevToolsCommandMenuIndex] et exécutez la `Show Network Conditions` commande.  

> [!NOTE]
> Vous pouvez également [définir des chaînes d’agent utilisateur en mode appareil][DevToolsDeviceModeIndex].  

[#1029031][crbug1029031] problème de chrome  

### Mises à jour du volet d’audit  

#### Nouvelle interface utilisateur de configuration  

L’interface utilisateur de configuration dispose d’une nouvelle conception réactive, et les options de configuration de limitation ont été simplifiées.  Pour plus d’informations sur les modifications de l’interface utilisateur de limitation, voir [limitation du panneau d’audit][GitHubGoogleChromeDevToolsAuditsPanelThrottling] .  

> ##### Figure16  
> Nouvelle interface utilisateur de configuration  
> ![Nouvelle interface utilisateur de configuration][ImageConfigurationUI]  

### Mises à jour de l’onglet couverture  

#### Modes de couverture par fonction ou par bloc  

Dans le menu déroulant de l' [onglet couverture][DevToolsCoverageIndex] , vous pouvez spécifier si les données de couverture du code doivent être collectées **par fonction** ou **par bloc**.  La couverture **par bloc** est plus détaillée, mais aussi bien plus coûteuse à rassembler.  DevTools utilise par défaut une couverture par **fonction** .  

> [!CAUTION]
> Il est possible que vous voyiez des différences de couverture de code importantes dans les fichiers HTML selon que vous utilisez la **fonction par fonction** ou **par bloc** .  Lorsque vous utilisez le mode **par fonction** , les scripts inline dans les fichiers HTML sont traités en tant que fonctions.  Si le script s’exécute tout de même, DevTools marque tout le script en tant que code utilisé.  Par exemple, si le script n’est pas exécuté, DevTools le marquer comme étant du code inutilisé.  

> ##### Figure17  
> Menu déroulant du mode couverture  
> ![Menu déroulant du mode couverture][ImageCoverageMode]  

#### La couverture doit maintenant être initiée par un recharge de page  

Le basculement de la couverture du code sans recharge de page a été supprimé car les données de couverture étaient instables.  Par exemple, une fonction peut être signalée comme n’étant pas utilisée si le runtime était depuis longtemps et si le nettoyage de la mémoire a nettoyé celle-ci.  

[#1004203][crbug1004203] problème de chrome  

## Télécharger les canaux Microsoft Edge preview  

Si vous utilisez Windows ou macOS, envisagez d’utiliser les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] comme navigateur par défaut.  Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.  

## Contacter l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!--<<../../_shared/devtools-feedback.md>> -->

<!--<<../../_shared/canary.md>> -->

<!--<<../../_shared/discover.md>> -->

<!-- image links -->  

[ImagePerformanceToolKeyboardReaderImprovements]: ../../images/2019/12/a11y-performance-tool.msft.gif "Figure 1: l’outil performance dans le DevTools avec les améliorations de la navigation au clavier et du lecteur d’écran"  
[ImageLocalizedGerman]: ../../images/2019/12/localized-devtools.msft.png "Figure 2: DevTools en allemand"  
[ImageHintsTabWebhintExtension]: ../../images/2019/12/webhint-browser-extension.msft.png "Figure 3: onglet hints de Microsoft Edge DevTools lorsque l’extension de navigateur webhint est installée"  
[Image3DView]: ../../images/2019/12/3dview.msft.png "Figure 4: affichage 3D dans Microsoft Edge DevTools"  
[ImageElementsVisualStudioCode]: ../../images/2019/12/elements-for-edge.msft.png "Figure 5: outil éléments du code VS utilisant les éléments de l’extension Microsoft Edge"  
[ImageDebuggerExtensionVisualStudioCode]: ../../images/2019/12/vscode-debugger.msft.png "Figure 6: débogueur de l’extension Microsoft Edge dans le code VS"  
[ImageWebhintVisualStudioCodeExtensionWorkspace]: ../../images/2019/12/webhint-vscode-extension.msft.png "Figure 7: l’extension de code webhint VS analyse des fichiers. TSX dans le code VS"  
[ImageVisualStudioLaunchWebApp]: ../../images/2019/12/vs.msft.png "Figure 8: Visual Studio avec l’option de lancement de votre application Web dans Microsoft Edge Canaries, dev ou Beta"  
[ImageTrackingPrevention]: ../../images/2019/12/tracking-prevention.msft.png "Figure 9: messages dans la console lors du suivi de la prévention blocage de l’accès au stockage pour un suivi"  
[ImageConsoleRedeclarationFails]: ../../images/2019/12/letbefore.msft.png "Figure 10: la console dans Microsoft Edge 79 indiquant que la redéclaration d’échec"  
[ImageConsoleRedeclarationSucceeds]: ../../images/2019/12/letafter.msft.png "Figure 11: console dans Microsoft Edge 80 indiquant que la redéclaration de réussite a réussi"  
[ImageRequestInitiatorChain]: ../../images/2019/12/initiators.msft.png "Figure 12: chaîne d’initiateur de requête dans l’onglet initiateur"  
[ImageOverviewPaneInspectedResource]: ../../images/2019/12/overview.msft.png "Figure 13: volet vue d’ensemble mettant en évidence la ressource inspectée"  
[ImagePathNetworkPanel]: ../../images/2019/12/columns.msft.png "Figure 14: nouvelles colonnes Path et URL dans le panneau réseau"  
[ImageUserAgentNetworkConditionsTab]: ../../images/2019/12/useragent.msft.png "Figure 15: menu agent utilisateur dans l’onglet conditions réseau"  
[ImageConfigurationUI]: ../../images/2019/12/start.msft.png "Figure 16: nouvelle interface utilisateur de configuration"  
[ImageCoverageMode]: ../../images/2019/12/modes.msft.png "Figure 17: menu déroulant du mode couverture"  

<!--[ImageDwarfPoweredWebAssemblyDebugging]: ../../images/2019/12/wasm.msft.png "Figure: The new DWARF-powered WebAssembly debugging"  -->

<!-- links -->  

[DevToolsCommandMenuIndex]: ../../../command-menu/index.md "Exécuter des commandes à l’aide du menu de commande de Microsoft Edge DevTools"  
[DevToolsCoverageIndex]: ../../../coverage/index.md "Rechercher du code JavaScript et CSS inutilisé avec l’onglet couverture dans Microsoft Edge DevTools"  
[DevToolsDeviceModeIndex]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Simuler une fenêtre d’affichage mobile-simuler des appareils mobiles avec le mode appareil dans Microsoft Edge DevTools"  
[DevToolsNetworkIndex]: ../../../network/index.md "Examiner l’activité réseau dans Microsoft Edge DevTools"  
[DevToolsNetworkReferenceViewInitiatorsDependencies]: ../../../network/reference.md#view-initiators-and-dependencies "Afficher les initiateurs et les dépendances-référence d’analyse du réseau"  
[DevGuideEdgeHtmlWhatsNew]: ../../../../dev-guide/whats-new.md "Nouveautés de EdgeHTML"  
[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Débogueur pour l’extension de code Microsoft Edge VS"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Éléments pour l’extension de code Microsoft Edge VS"  

<!--  [201912Webassembly]: webassembly.md "Improved WebAssembly debugging in Microsoft Edge DevTools"  -->  

[crbug842488]: https://crbug.com/842488 "842488-ajoutez le champ Initiator à l’onglet en-têtes-monorail"  
[crbug988253]: https://crbug.com/988253 "988253-bogue DevTools-aucune association entre la demande réseau et le graphique de chronologie-monorail"  
[crbug993366]: https://crbug.com/993366 "993366-Affichez la partie chemin d’URL dans la liste des demandes du panneau réseau-monorail"  
[crbug1004193]: https://crbug.com/1004193 "1004193-mode REPL pour V8-monorail"  
[crbug1004203]: https://crbug.com/1004203 "1004203-monorail"  
[crbug1029031]: https://crbug.com/1029031 "1029031-les chaînes UA sont obsolètes-monorail" 
[crbug963183]: https://crbug.com/963183 "963183-DevTools n’est pas conforme à la norme WCAG"
[crbug941561]: https://crbug.com/941561 "941561-localization du DevTools"
[crbug987787]: https://crbug.com/987787 "987787-affichage 3D de Dom"

[AccessibilityInsights]: https://aka.ms/a11yinsights "Insights sur l’accessibilité"  

[DwarfHome]: https://dwarfstd.org "Onglet Accueil"  
[GitHubGoogleChromeDevToolsAuditsPanelThrottling]: https://github.com/GoogleChrome/lighthouse/blob/master/docs/throttling.md#devtools-audits-panel-throttling "DevTools’limitation du panneau d’audit-GoogleChrome/phare | GitHub"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nouveau problème-MicrosoftDocs/Edge-développeur"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canaux Microsoft Edge preview"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Compléments Microsoft Edge Insider"  
[MicrosoftVisualStudio]: https://aka.ms/vs "Visual Studio"  
[MicrosoftVisualStudioBlogDebugJavascript]: https://aka.ms/vs/debug-edge "Déboguer JavaScript dans Microsoft Edge à partir de Visual Studio | Blog Visual Studio"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Télécharger Visual Studio 2019 pour Windows \ & Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "DOM (Document Object Model) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "index z | MDN"  
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publiez un tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools compte Twitter"
[VisualStudioCode]: https://aka.ms/vscode "Code Visual Studio"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Débogueur pour Microsoft Edge-Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Éléments pour Microsoft Edge \ (chrome \)-Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint-Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "Astuce"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Extension du navigateur webhint | documentation webhint"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Extension de code webhint et documentation webhint"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Amélioration de la prévention du suivi dans le billet de blog Microsoft Edge"
[TheWebWeWant]: https://aka.ms/webwewant "Le site Web de votre choix"

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/updates/2019/12/devtools/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
