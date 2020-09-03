---
description: Affichage 3D, intégration de Visual Studio à Microsoft Edge, et bien plus encore.
title: Nouveautés de DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 9dd47a38f345601f2d459d39e3ee7b1728df8971
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993414"
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

# Nouveautés de DevTools (Microsoft Edge 81)  

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
| Chinese (Simplified) - 中文(简体)（简体）| Chinese (Traditional) - 中文(繁體)（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

Le DevTools correspond automatiquement à la langue que vous utilisez pour Microsoft Edge dans `edge://settings/languages` .  

Si vous voulez que Microsoft Edge soit dans une langue et que votre DevTools reste en anglais, appuyez sur `F1` la devtools pour ouvrir les [paramètres][Settings] et désactiver respecter la **langue du navigateur**.  

> ##### Figure 2  
> DevTools en allemand  
> ![DevTools en allemand][ImageLocalizedGerman]  

Les messages de **console** ne sont pas localisés.  Seules les chaînes utilisées dans l’interface utilisateur DevTools sont affichées dans la langue que vous utilisez pour Microsoft Edge.  

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

Pour accéder à l’affichage 3D, appuyez sur la touche `Ctrl`  +  `Shift`  +  `P` **affichage** 3D et sélectionnez **afficher la vue 3D**.  

Nous travaillons sur l’interface utilisateur et nous ajoutons d’autres fonctionnalités à l’affichage 3D; nous vous envoyons donc votre [avis](#getting-in-touch-with-microsoft-edge-devtools-team).  

[#987787][crbug987787] problème de chrome  

### Extensions de code Visual Studio  

L’équipe DevTools a également émis certaines extensions pour le [code Visual Studio \ (vs code \)][VisualStudioCode] qui vous permettent d’utiliser la puissance de devtools directement à partir de votre éditeur de texte. Consultez les extensions suivantes:  

#### Éléments pour Microsoft Edge  

Utilisez l’outil éléments du code VS, en ajoutant les éléments de l’extension du code [Microsoft Edge \ (chrome \)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] .  

> ##### Figure 5  
> L’outil éléments dans le code VS en utilisant les éléments pour l’extension Microsoft Edge et l' ![ outil éléments en utilisant les éléments de l’extension Microsoft Edge][ImageElementsVisualStudioCode]  

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

[Apprenez-en davantage sur le débogage de Microsoft Edge à partir de Visual Studio][MicrosoftVisualStudio].  

### Suivi des messages de la console de prévention  

La prévention de suivi est une fonctionnalité unique de Microsoft Edge qui vous protège du suivi par des sites Web que vous n’avez pas encore visités.  Le paramètre de prévention du suivi par défaut est le mode équilibré, qui permet de bloquer des suivis tiers et des pistes malveillantes connues pour une interface qui équilibre la confidentialité et la compatibilité Web.  Pour plus d’informations sur la compatibilité de votre page Web lorsque certains suivis sont bloqués, nous avons également ajouté des messages d’avertissement dans la console lorsqu’un suivi est bloqué.  

> ##### Figure9  
> Messages dans la console lors du suivi de la prévention bloquer l’accès au stockage pour un suivi  
> ![Messages dans la console lors du suivi de la prévention bloquer l’accès au stockage pour un suivi][ImageTrackingPrevention]  

[En savoir plus sur la prévention de suivi et le compromis entre la confidentialité et la compatibilité Web][TrackingPrevention].  

## Annonces du projet de chrome  

Les sections suivantes annoncent des fonctionnalités supplémentaires disponibles dans Microsoft Edge 81 qui ont été fournies au projet de chrome Open source.  

### Prise en charge de moto G4 en mode appareil  

Après l' [activation de la barre d’outils de l’appareil][DeviceToolbar], simulez les dimensions d’une fenêtre d’affichage moto G4 de la liste des **appareils** .  

> ##### Figure10  
> Simulation d’une fenêtre d’affichage moto G4  
> ![Simulation d’une fenêtre d’affichage moto G4][ImageMotoG4]  

Cliquez sur [afficher le cadre][DeviceFrame] de l’appareil pour afficher le matériel moto G4 dans la fenêtre d’affichage.  

> ##### Figure11  
> Affichage du matériel moto G4  
> ![Affichage du matériel moto G4][ImageMotoG4Frame]  

Fonctionnalités connexes:  

*   Ouvrez le [menu de commandes][CommandMenu] et exécutez la `Capture screenshot` commande pour effectuer une capture d’écran de la fenêtre d’affichage qui inclut le matériel moto G4 (après avoir activé l’option **afficher le cadre**de l’appareil).  
*   [Limitez le réseau et le processeur][ThrottleNetworkAndCpu] pour simuler plus précisément les conditions de navigation sur le Web des utilisateurs mobiles.  

[#924693][crbug924693] problème de chrome  

### Mises à jour associées au cookie;  

#### Cookies bloqués dans le volet cookies  

Le volet cookies du panneau application affiche désormais les cookies bloqués avec un arrière-plan jaune.  

> ##### Figure12  
> Cookies bloqués dans le volet cookies du panneau application  
> ![Cookies bloqués dans le volet cookies du panneau application][ImageBlockedCookies]  

[#1030258][crbug|::ref1::|] problème de chrome  

#### Priorité de cookie dans le volet cookie  

Les tables cookies dans les panneaux réseau et application incluent désormais une colonne de **priorité** .  

> [!CAUTION]
> Les navigateurs de type chrome, tels que Microsoft Edge, sont les seuls navigateurs qui prennent en charge la priorité des cookies.  

[#1026879][crbug1026879] problème de chrome  

#### Modifier toutes les valeurs de cookie  

Toutes les cellules des tables cookie sont modifiables, à l’exception des cellules de la colonne **taille** , car cette colonne représente la taille du réseau du cookie, en octets.  Pour obtenir une description de chaque colonne, voir [champs][CookiesFields] .  

> ##### Figure13  
> Modification d’une valeur de cookie  
> ![Modification d’une valeur de cookie][ImageEditCookie]  

#### Copy As Node.js FETCH pour inclure des données de cookie  

Cliquez avec le bouton droit sur une demande réseau et sélectionnez **copier**la  >  **copie sous Node.js récupérer** pour obtenir une `fetch` expression incluant des données de cookie.  

> ##### Figure14  
> Copy As Node.js Fetch  
> ![Copy As Node.js Fetch][ImageCopyFetch]  

[#1029826][crbug1029826] problème de chrome  

### Icônes de manifeste d’application Web plus précises  

Auparavant, le volet manifeste du panneau d’application a envoyé ses propres demandes pour afficher les icônes du manifeste de l’application Web.  DevTools affiche maintenant la même icône de manifeste que celle utilisée par Microsoft Edge.  

> ##### Figure15  
> Icônes du volet manifeste  
> ![Icônes du volet manifeste][ImageManifestIcon]  

[#985402][crbug985402] problème de chrome  

### Survol des propriétés de contenu CSS pour afficher les valeurs sans échappement  

Placez le pointeur de la souris sur la valeur d’une `content` propriété pour afficher la version sans échappement de la valeur.  

Par exemple, dans cette [démonstration][CSSContentDemo] , lorsque vous examinez le `p::after` Pseudo-élément, vous voyez une chaîne d’échappement dans le volet styles:  

> ##### Figure16  
> Chaîne d’échappement  
> ![Chaîne d’échappement][ImageEscapedString]  

Lorsque vous pointez sur la `content` valeur, vous voyez la valeur sans séquence d’échappement:  

> ##### Figure17  
> Valeur sans échappement  
> ![Valeur sans échappement][ImageUnescapedString]  

### Erreurs de carte source plus détaillées dans la console  

La console donne désormais plus de détails sur la raison pour laquelle une table source n’a pas pu être chargée ou analysée.  Auparavant, il vous suffit de fournir une erreur sans expliquer ce qui s’est passé.  

> ##### Figure 18  
> Erreur de chargement du mappage source dans la console  
> ![Erreur de chargement du mappage source dans la console][ImageSourcemapError]  

### Paramètre permettant de désactiver le défilement au-delà de la fin d’un fichier  

Ouvrez [paramètres][Settings] , puis désactivez l’option les sources de **Préférences**  >  **Sources**  >  **autorisent le défilement au-delà de la fin du fichier** pour désactiver le comportement de l’interface utilisateur par défaut qui vous permet de faire défiler le fichier dans le volet **sources** .  

> ##### Figure 19  
> Désactivation de l’option autoriser le défilement au- **delà de la fin du fichier** dans les paramètres  
> ![Désactivation de l’option autoriser le défilement au-delà de la fin du fichier][ImageSettings]  

> ##### Figure 20  
> Le défilement au-delà de la fin d’un fichier est désormais désactivé dans le panneau sources  
> ![Le défilement au-delà de la fin d’un fichier est désormais désactivé dans le panneau sources][ImageScroll]  

## Télécharger les canaux Microsoft Edge preview  

Si vous utilisez Windows ou macOS, envisagez d’utiliser les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] comme navigateur par défaut.  Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.  

## Contacter l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- <<../../_shared/devtools-feedback.md>>  

<<../../_shared/canary.md>>  

<<../../_shared/discover.md>> -->  

<!-- image links -->  

[ImagePerformanceToolKeyboardReaderImprovements]: ../../images/2020/01/a11y-performance-tool.msft.gif "Figure 1: l’outil performance dans le DevTools avec les améliorations de la navigation au clavier et du lecteur d’écran"  
[ImageLocalizedGerman]: ../../images/2020/01/localized-devtools.msft.png "Figure 2: DevTools en allemand"  
[ImageHintsTabWebhintExtension]: ../../images/2020/01/webhint-browser-extension.msft.png "Figure 3: onglet hints de Microsoft Edge DevTools lorsque l’extension de navigateur webhint est installée"  
[Image3DView]: ../../images/2020/01/3dview.msft.png "Figure 4: affichage 3D dans Microsoft Edge DevTools"  
[ImageElementsVisualStudioCode]: ../../images/2020/01/elements-for-edge.msft.png "Figure 5: outil éléments du code VS utilisant les éléments de l’extension Microsoft Edge"  
[ImageDebuggerExtensionVisualStudioCode]: ../../images/2020/01/vscode-debugger.msft.png "Figure 6: débogueur de l’extension Microsoft Edge dans le code VS"  
[ImageWebhintVisualStudioCodeExtensionWorkspace]: ../../images/2020/01/webhint-vscode-extension.msft.png "Figure 7: l’extension de code webhint VS analyse des fichiers. TSX dans le code VS"  
[ImageVisualStudioLaunchWebApp]: ../../images/2020/01/vs.msft.png "Figure 8: Visual Studio avec l’option de lancement de votre application Web dans Microsoft Edge Canaries, dev ou Beta"  
[ImageTrackingPrevention]: ../../images/2020/01/tracking-prevention.msft.png "Figure 9: messages dans la console lors du suivi de la prévention blocage de l’accès au stockage pour un suivi" 
[ImageMotoG4]: ../../images/2020/01/motog4.msft.png "Figure 10: simulation d’une fenêtre d’affichage moto G4" 
[ImageMotoG4Frame]: ../../images/2020/01/motog4frame.msft.png "Figure 11: affichage du matériel moto G4" 
[ImageBlockedCookies]: ../../images/2020/01/blockedcookies.msft.png "Figure 12: cookies bloqués dans le volet cookies du panneau application"
[ImageEditCookie]: ../../images/2020/01/editcookie.msft.png "Figure 13: modification d’une valeur de cookie"
[ImageCopyFetch]: ../../images/2020/01/fetchcookies.msft.png "Figure 14: copier en tant que Node.js récupérer"
[ImageManifestIcon]: ../../images/2020/01/manifesticons.msft.png "Figure 15: icônes dans le volet manifeste"
[ImageEscapedString]: ../../images/2020/01/escapedstring.msft.png "Figure 16: chaîne d’échappement"
[ImageUnescapedString]: ../../images/2020/01/unescapedstring.msft.png "Figure 17: valeur sans échappement"
[ImageSourcemapError]: ../../images/2020/01/sourcemap.msft.png "Figure 18: erreur de chargement d’une carte source dans la console"
[ImageSettings]: ../../images/2020/01/settings.msft.png "Figure 19: désactivation de l’option autoriser le défilement au-delà de la fin du fichier dans les paramètres"
[ImageScroll]: ../../images/2020/01/scrollingsources.msft.png "Figure 20: le défilement au-delà de la fin d’un fichier est désormais désactivé dans le panneau sources"

<!-- links -->  

[DeviceToolbar]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Simuler une fenêtre d’affichage mobile avec le mode appareil dans Microsoft Edge DevTools"
[DeviceFrame]: ../../../device-mode/index.md#show-device-frame "Sélectionnez Afficher l’image de l’appareil pour afficher l’image de l’appareil physique à l’intérieur de la fenêtre d’affichage."
[CommandMenu]: ../../../command-menu/index.md "Exécuter des commandes à l’aide du menu de commande de Microsoft Edge DevTools"  
[ThrottleNetworkAndCpu]: ../../../device-mode/index.md#throttle-the-network-and-cpu "Limitation du réseau et du processeur pour simuler plus précisément les conditions de navigation sur le Web des utilisateurs mobiles."
[crbug924693]: https://crbug.com/924693 "924693: demande de fonctionnalité: Ajouter moto G4 à la liste du mode appareil"
[crbug1030258]: https://crbug.com/1030258 "1030258"
[crbug1026879]: https://crbug.com/1026879 "1026879: l’onglet cookie de la console dev ne montre plus de priorité"
[CookiesFields]: ../../../storage/cookies.md#fields "Les champs de la table cookies"
[crbug1029826]: https://crbug.com/1029826 "1029826: onglet réseau-> cliquez avec le bouton droit pour demander-> copier-> Copy en tant que FETCH ne copie aucun cookie"
[crbug985402]: https://crbug.com/985402 "985402: les chaînes d’erreur d’icône de manifeste Web App sont confuses"
[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Démo pour le contenu CSS sans échappement"
[Settings]: ../../../customize/index.md#settings "Personnaliser Microsoft Edge DevTools avec des paramètres"
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publiez un tweet"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nouveau problème-MicrosoftDocs/Edge-développeur"  
[TheWebWeWant]: https://aka.ms/webwewant "Le site Web de votre choix"
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canaux Microsoft Edge preview"  
[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Débogueur pour l’extension de code Microsoft Edge VS"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Éléments pour l’extension de code Microsoft Edge VS"  
[crbug963183]: https://crbug.com/963183 "963183-DevTools n’est pas conforme à la norme WCAG"
[crbug941561]: https://crbug.com/941561 "941561-localization du DevTools"
[crbug987787]: https://crbug.com/987787 "987787-affichage 3D de Dom"
[AccessibilityInsights]: https://aka.ms/a11yinsights "Insights sur l’accessibilité"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Compléments Microsoft Edge Insider"  
[MicrosoftVisualStudio]: ../../../../visual-studio/index.md "Visual Studio"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Télécharger Visual Studio 2019 pour Windows \ & Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "DOM (Document Object Model) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "index z | MDN"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools compte Twitter"
[VisualStudioCode]: https://aka.ms/vscode "Code Visual Studio"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Débogueur pour Microsoft Edge-Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Éléments pour Microsoft Edge \ (chrome \)-Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint-Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "Astuce"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Extension du navigateur webhint | documentation webhint"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Extension de code webhint et documentation webhint"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Amélioration de la prévention du suivi dans le billet de blog Microsoft Edge"

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/updates/2020/01/devtools/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  