---
description: Affichage 3D, intégration de Visual Studio à Microsoft Edge, et bien plus encore.
title: Nouveautés de DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 3081ebb256a9ede637aaaddc3c3cdf7a70a201bb
ms.sourcegitcommit: b337717957529239434b4e8e1e167aebf0543518
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015474"
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

Les sections suivantes répertorient les annonces que vous pouvez avoir manquées de l’équipe Microsoft Edge DevTools. Découvrez-les pour essayer de nouvelles fonctionnalités dans le DevTools, les extensions de code Visual Studio, etc.  Pour vous tenir au courant de toutes les fonctionnalités les plus récentes et les plus récentes de vos outils de développement, téléchargez les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] et [Suivez-nous sur Twitter][EdgeDevToolsTwitterAccount].  

### Améliorations de l’accessibilité dans DevTools  

L’équipe DevTools a 170 contribué aux modifications apportées à Chrome pour répondre aux problèmes de contraste des couleurs, de clavier et de lecteur d’écran à forte incidence dans DevTools.  Tout développeur bâtiment sur le Web doit être en mesure d’utiliser le DevTools.  

:::image type="complex" source="../../images/2020/01/a11y-performance-tool.msft.gif" alt-text="Outil performance dans le DevTools avec les améliorations de la navigation au clavier et du lecteur d’écran" lightbox="../../images/2020/01/a11y-performance-tool.msft.gif":::
   Outil **performance** dans le devtools avec les améliorations de la navigation au clavier et du lecteur d’écran  
:::image-end:::  

Vous voulez savoir comment rendre votre page Web accessible à tous vos utilisateurs?  Téléchargez les informations [d’accessibilité][AccessibilityInsights] et les extensions [Webhint][WebhintBrowserExtension] pour Microsoft Edge pour commencer.  

Si vous utilisez un lecteur d’écran ou le clavier pour naviguer dans DevTools, envoyez-nous vos commentaires en nous appuyant sur un [Tweet][PostTweetEdgeDevTools] ou en cliquant sur l’icône d' [envoi de commentaires](#getting-in-touch-with-microsoft-edge-devtools-team) .  

[#963183][CR963183] problème de chrome  

### Utiliser le DevTools dans d’autres langues  

De nombreux développeurs utilisent d’autres outils de développement tels que StackOverflow et Visual Studio, dans leur langue maternelle, et non uniquement en anglais.  Nous sommes heureux d’annoncer la localisation de DevTools, que vous pouvez désormais utiliser dans l’un des 10 langues autres que l’anglais:  

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

:::image type="complex" source="../../images/2020/01/localized-devtools.msft.png" alt-text="DevTools en allemand" lightbox="../../images/2020/01/localized-devtools.msft.png":::
   DevTools en allemand  
:::image-end:::  

Les messages de **console** ne sont pas localisés.  Seules les chaînes utilisées dans l’interface utilisateur DevTools sont affichées dans la langue que vous utilisez pour Microsoft Edge.  

Si vous souhaitez utiliser le DevTools dans une autre langue que celle proposée, vous pouvez utiliser le [Tweet][PostTweetEdgeDevTools] ou cliquez sur l’icône d' [envoi de commentaires](#getting-in-touch-with-microsoft-edge-devtools-team) .  

[#941561][CR941561] problème de chrome  

### extension Microsoft Edge de webhint  

L’extension Microsoft Edge de Microsoft vous permet d’analyser facilement votre page Web et de faire des commentaires sur l’accessibilité, la compatibilité avec les navigateurs, la sécurité et les performances, etc., dans le DevTools.  Pour en savoir plus [https://webhint.io][Webhint] , voir.  

:::image type="complex" source="../../images/2020/01/webhint-browser-extension.msft.png" alt-text="Onglet Hints dans le DevTools lorsque l’extension de navigateur webhint est installée" lightbox="../../images/2020/01/webhint-browser-extension.msft.png":::
   Onglet **Hints** dans le devtools lorsque l’extension de navigateur webhint est installée  
:::image-end:::  

[Essayez l’extension de navigateur webhint dans Microsoft Edge][MicrosoftEdgeInsiderAddons].  Une fois l’extension installée, ouvrez le DevTools et sélectionnez l’onglet conseils.  À partir de là, effectuez une analyse de site personnalisable.  Accédez à [webhint.IO][WebhintBrowserExtension] pour en savoir plus.  

### Vue 3D  

Utilisez la **vue 3D** pour déboguer votre application Web en naviguant dans le [modèle d’objet de document \ (DOM \)][MDNDocumentObjectModel] ou le contexte de pile [de l’index z][MDNZIndex] .  

:::image type="complex" source="../../images/2020/01/3dview.msft.png" alt-text="Affichage 3D dans le DevTools" lightbox="../../images/2020/01/3dview.msft.png":::
   Affichage 3D dans le DevTools  
:::image-end:::  

Pour accéder à l’affichage 3D, appuyez sur la touche `Ctrl`  +  `Shift`  +  `P` **affichage** 3D et sélectionnez **afficher la vue 3D**.  

Nous travaillons sur l’interface utilisateur et nous ajoutons d’autres fonctionnalités à l’affichage 3D; nous vous envoyons donc votre [avis](#getting-in-touch-with-microsoft-edge-devtools-team).  

[#987787][CR987787] problème de chrome  

### Extensions de code Visual Studio  

L’équipe DevTools a également émis quelques extensions pour le [code Visual Studio][VisualStudioCode] qui vous permettent d’utiliser la puissance de devtools directement à partir de votre éditeur de texte. Consultez les extensions suivantes:  

#### Éléments pour Microsoft Edge  

Pour ce faire, utilisez l’outil éléments dans le code Visual Studio en ajoutant les éléments pour l’extension de code Visual Studio [Microsoft Edge \ (chrome \)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] .  

:::image type="complex" source="../../images/2020/01/elements-for-edge.msft.png" alt-text="Outil éléments dans le code Visual Studio utilisant les éléments de l’extension Microsoft Edge" lightbox="../../images/2020/01/elements-for-edge.msft.png":::
   Outil **éléments** dans le code Visual Studio utilisant les éléments de l’extension Microsoft Edge  
:::image-end:::  

Pour plus d’informations, consultez les [éléments pour l’extension de code Visual Studio Visual Studio][VisualStudioCodeElementEdgeExtension].  

#### Débogueur pour Microsoft Edge  

Avec le [débogueur pour][VisualStudioMarketplaceDebuggerEdge] l’extension de code Visual Studio Visual Studio, déboguez JavaScript en cours d’exécution dans Microsoft Edge directement à partir de code Visual Studio.  

:::image type="complex" source="../../images/2020/01/vscode-debugger.msft.png" alt-text="Le débogueur pour l’extension Microsoft Edge dans le code Visual Studio" lightbox="../../images/2020/01/vscode-debugger.msft.png":::
   Le débogueur pour l’extension Microsoft Edge dans le code Visual Studio  
:::image-end:::  

Pour plus d’informations, voir [Comment déboguer Microsoft Edge à partir de code Visual Studio][VisualStudioCodeDebuggerEdgeExtension].  

#### webhint  

L’extension de code [webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio utilise `webhint` pour améliorer votre page Web pendant que vous rédigez un message. Cette extension exécute et signale les diagnostics de vos fichiers d’espace de travail en fonction de l' `webhint` analyse.  

:::image type="complex" source="../../images/2020/01/webhint-vscode-extension.msft.png" alt-text="Extension de code Visual Studio webhint qui analyse un fichier. TSX dans le code Visual Studio" lightbox="../../images/2020/01/webhint-vscode-extension.msft.png":::
   Extension de code Visual Studio webhint qui analyse un `.tsx` fichier dans le code Visual Studio  
:::image-end:::  

[En savoir plus sur l’extension Visual Studio code webhint][WebhintVisualStudioCodeExtension].  

### Intégration de Visual Studio  

Dans Visual Studio 2019 version 16,2 ou ultérieure, utilisez le débogueur Visual Studio pour déboguer JavaScript en cours d’exécution dans Microsoft Edge.  [Téléchargez Visual Studio 2019][MicrosoftVisualStudioDownloads] pour essayer cette fonctionnalité.  

:::image type="complex" source="../../images/2020/01/vs.msft.png" alt-text="Visual Studio avec l’option de lancement de votre application Web dans Microsoft Edge Canaries, dev ou Beta" lightbox="../../images/2020/01/vs.msft.png":::
   Visual Studio avec l’option de lancement de votre application Web dans Microsoft Edge Canaries, dev ou Beta  
:::image-end:::  

[Apprenez-en davantage sur le débogage de Microsoft Edge à partir de Visual Studio][MicrosoftVisualStudio].  

### Suivi des messages de la console de prévention  

La prévention de suivi est une fonctionnalité unique de Microsoft Edge qui vous protège du suivi par des sites Web que vous n’avez pas encore visités.  Le paramètre de prévention du suivi par défaut est le mode équilibré, qui permet de bloquer des suivis tiers et des pistes malveillantes connues pour une interface qui équilibre la confidentialité et la compatibilité Web.  Pour plus d’informations sur la compatibilité de votre page Web lorsque certains suivis sont bloqués, nous avons également ajouté des messages d’avertissement dans la console lorsqu’un suivi est bloqué.  

:::image type="complex" source="../../images/2020/01/tracking-prevention.msft.png" alt-text="Messages dans la console lors du suivi de la prévention bloquer l’accès au stockage pour un suivi" lightbox="../../images/2020/01/tracking-prevention.msft.png":::
   Messages dans la console lors du suivi de la prévention bloquer l’accès au stockage pour un suivi  
:::image-end:::  

[En savoir plus sur la prévention de suivi et le compromis entre la confidentialité et la compatibilité Web][TrackingPrevention].  

## Annonces du projet de chrome  

Les sections suivantes annoncent des fonctionnalités supplémentaires disponibles dans Microsoft Edge 81 qui ont été fournies au projet de chrome Open source.  

### Prise en charge de moto G4 en mode appareil  

Après l' [activation de la barre d’outils de l’appareil][DeviceToolbar], simulez les dimensions d’une fenêtre d’affichage moto G4 de la liste des **appareils** .  

:::image type="complex" source="../../images/2020/01/motog4.msft.png" alt-text="Simulation d’une fenêtre d’affichage moto G4" lightbox="../../images/2020/01/motog4.msft.png":::
   Simulation d’une fenêtre d’affichage moto G4  
:::image-end:::  

Cliquez sur [afficher le cadre][DeviceFrame] de l’appareil pour afficher le matériel moto G4 dans la fenêtre d’affichage.  

:::image type="complex" source="../../images/2020/01/motog4frame.msft.png" alt-text="Affichage du matériel moto G4" lightbox="../../images/2020/01/motog4frame.msft.png":::
   Affichage du matériel moto G4  
:::image-end:::  

Fonctionnalités connexes:  

*   Ouvrez le [menu de commandes][CommandMenu] et exécutez la `Capture screenshot` commande pour effectuer une capture d’écran de la fenêtre d’affichage qui inclut le matériel moto G4 (après avoir activé l’option **afficher le cadre**de l’appareil).  
*   [Limitez le réseau et le processeur][ThrottleNetworkAndCpu] pour simuler plus précisément les conditions de navigation sur le Web des utilisateurs mobiles.  

[#924693][CR924693] problème de chrome  

### Mises à jour associées au cookie;  

#### Cookies bloqués dans le volet cookies  

Le volet cookies du panneau application affiche désormais les cookies bloqués avec un arrière-plan jaune.  

:::image type="complex" source="../../images/2020/01/blockedcookies.msft.png" alt-text="Cookies bloqués dans le volet cookies du panneau application" lightbox="../../images/2020/01/blockedcookies.msft.png":::
   Cookies bloqués dans le volet cookies du panneau application  
:::image-end:::  

[#1030258][CR1030258] problème de chrome  <!-- inaccessible  -->  

#### Priorité de cookie dans le volet cookie  

Les tables cookies dans les panneaux réseau et application incluent désormais une colonne de **priorité** .  

> [!CAUTION]
> Les navigateurs de type chrome, tels que Microsoft Edge, sont les seuls navigateurs qui prennent en charge la priorité des cookies.  

[#1026879][CR1026879] problème de chrome  

#### Modifier toutes les valeurs de cookie  

Toutes les cellules des tables cookie sont modifiables, à l’exception des cellules de la colonne **taille** , car cette colonne représente la taille du réseau du cookie, en octets.  Pour obtenir une description de chaque colonne, voir [champs][CookiesFields] .  

:::image type="complex" source="../../images/2020/01/editcookie.msft.png" alt-text="Modification d’une valeur de cookie" lightbox="../../images/2020/01/editcookie.msft.png":::
   Modification d’une valeur de cookie  
:::image-end:::  

#### Copy As Node.js FETCH pour inclure des données de cookie  

Cliquez avec le bouton droit sur une demande réseau et sélectionnez **copier**la  >  **copie sous Node.js récupérer** pour obtenir une `fetch` expression incluant des données de cookie.  

:::image type="complex" source="../../images/2020/01/fetchcookies.msft.png" alt-text="Copy As Node.js Fetch" lightbox="../../images/2020/01/fetchcookies.msft.png":::
   Copy As Node.js Fetch  
:::image-end:::  

[#1029826][CR1029826] problème de chrome  

### Icônes de manifeste d’application Web plus précises  

Auparavant, le volet manifeste du panneau d’application a envoyé ses propres demandes pour afficher les icônes du manifeste de l’application Web.  DevTools affiche maintenant la même icône de manifeste que celle utilisée par Microsoft Edge.  

:::image type="complex" source="../../images/2020/01/manifesticons.msft.png" alt-text="Icônes du volet manifeste" lightbox="../../images/2020/01/manifesticons.msft.png":::
   Icônes du volet manifeste  
:::image-end:::  

[#985402][CR985402] problème de chrome  

### Survol des propriétés de contenu CSS pour afficher les valeurs sans échappement  

Placez le pointeur de la souris sur la valeur d’une `content` propriété pour afficher la version sans échappement de la valeur.  

Par exemple, dans cette [démonstration][CSSContentDemo] , lorsque vous examinez le `p::after` Pseudo-élément, vous voyez une chaîne d’échappement dans le volet styles:  

:::image type="complex" source="../../images/2020/01/escapedstring.msft.png" alt-text="Chaîne d’échappement" lightbox="../../images/2020/01/escapedstring.msft.png":::
   Chaîne d’échappement  
:::image-end:::  

Lorsque vous pointez sur la `content` valeur, vous voyez la valeur sans séquence d’échappement:  

:::image type="complex" source="../../images/2020/01/unescapedstring.msft.png" alt-text="Valeur sans échappement" lightbox="../../images/2020/01/unescapedstring.msft.png":::
   Valeur sans échappement  
:::image-end:::  

### Erreurs de carte source plus détaillées dans la console  

La console donne désormais plus de détails sur la raison pour laquelle une table source n’a pas pu être chargée ou analysée.  Auparavant, il vous suffit de fournir une erreur sans expliquer ce qui s’est passé.  

:::image type="complex" source="../../images/2020/01/sourcemap.msft.png" alt-text="Erreur de chargement du mappage source dans la console" lightbox="../../images/2020/01/sourcemap.msft.png":::
   Erreur de chargement du mappage source dans la console  
:::image-end:::  

### Paramètre permettant de désactiver le défilement au-delà de la fin d’un fichier  

Ouvrez [paramètres][Settings] , puis désactivez l’option les sources de **Préférences**  >  **Sources**  >  **autorisent le défilement au-delà de la fin du fichier** pour désactiver le comportement de l’interface utilisateur par défaut qui vous permet de faire défiler le fichier dans le volet **sources** .  

:::image type="complex" source="../../images/2020/01/settings.msft.png" alt-text="Désactivation de l’option autoriser le défilement au-delà de la fin du fichier" lightbox="../../images/2020/01/settings.msft.png":::
   Désactivation de l’option autoriser le défilement au- **delà de la fin du fichier** dans les paramètres  
:::image-end:::  

:::image type="complex" source="../../images/2020/01/scrollingsources.msft.png" alt-text="Le défilement au-delà de la fin d’un fichier est désormais désactivé dans le panneau sources" lightbox="../../images/2020/01/scrollingsources.msft.png":::
   Le défilement au-delà de la fin d’un fichier est désormais désactivé dans le panneau sources  
:::image-end:::  

## Télécharger les canaux Microsoft Edge preview  

Si vous utilisez Windows ou macOS, envisagez d’utiliser les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] comme navigateur par défaut.  Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.  

## Contacter l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DeviceToolbar]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simuler une fenêtre d’affichage mobile-simuler des appareils mobiles avec le mode appareil dans Microsoft Edge DevTools | Documents Microsoft"
[DeviceFrame]: /microsoft-edge/devtools-guide-chromium/device-mode/index#show-device-frame "Afficher le cadre de l’appareil: simuler les appareils mobiles avec le mode appareil dans Microsoft Edge DevTools | Documents Microsoft"
[CommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Exécuter des commandes à l’aide du menu de commandes de Microsoft Edge DevTools | Documents Microsoft"  
[ThrottleNetworkAndCpu]: /microsoft-edge/devtools-guide-chromium/device-mode/index#throttle-the-network-and-cpu "Limiter la vitesse du réseau et de l’UC-simuler les appareils mobiles avec le mode périphérique dans Microsoft Edge DevTools | Documents Microsoft"
[Settings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"
[MicrosoftVisualStudio]: /microsoft-edge/visual-studio/index "Visual Studio | Documents Microsoft"  
[CookiesFields]: /microsoft-edge/devtools-guide-chromium/storage/cookies#fields "Champs: afficher, modifier et supprimer des cookies avec Microsoft Edge DevTools | Documents Microsoft"  

[VisualStudioCodeDebuggerEdgeExtension]: /microsoft-edge/visual-studio-code/debugger-for-edge "Débogueur de l’extension de code Visual Studio Visual Studio"  
[VisualStudioCodeElementEdgeExtension]: /microsoft-edge/visual-studio-code/elements-for-edge "Éléments de l’extension de code Visual Studio Visual Studio"  

[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canaux Microsoft Edge preview"  

[VisualStudioCode]: https://aka.ms/vscode "Code Visual Studio"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Débogueur pour Microsoft Edge-Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Éléments pour Microsoft Edge \ (chrome \)-Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint-Visual Studio Marketplace"

[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Amélioration de la prévention du suivi dans le billet de blog Microsoft Edge"

[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Compléments Microsoft Edge Insider"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Télécharger Visual Studio 2019 pour Windows & Mac"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publiez un tweet"  

[CR924693]: https://crbug.com/924693 "Demande de fonctionnalité: Ajouter moto G4 à la liste du mode appareil | Bugs du chrome"  
[CR1030258]: https://crbug.com/1030258 "CR 1030258 | Bugs du chrome"  
[CR1026879]: https://crbug.com/1026879 "L’onglet cookie dans la console de développement ne montre plus de priorité | Bugs du chrome"  
[CR1029826]: https://crbug.com/1029826 "onglet réseau-> cliquez avec le bouton droit pour demander-> copier-> copier comme FETCH ne copie pas les cookies | Bugs du chrome"  
[CR985402]: https://crbug.com/985402 "les chaînes d’erreur d’icône du manifeste de l’application Web sont confuses | Bugs du chrome"  
[CR963183]: https://crbug.com/963183 "DevTools ne respectent pas la norme WCAG | Bugs du chrome"  
[CR941561]: https://crbug.com/941561 "Localization du DevTools | Bugs du chrome"  
[CR987787]: https://crbug.com/987787 "Affichage 3D DOM | Bugs du chrome"  

[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Démo pour le contenu CSS sans échappement"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nouveau problème-MicrosoftDocs/Edge-développeur"  

[TheWebWeWant]: https://aka.ms/webwewant "Le site Web de votre choix"  
[AccessibilityInsights]: https://aka.ms/a11yinsights "Insights sur l’accessibilité"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "DOM (Document Object Model) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "index z | MDN"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools compte Twitter"  

[Webhint]: https://aka.ms/webhint "Astuce"  

[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Extension du navigateur webhint | documentation webhint"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Extension de code Visual Studio webhint | documentation webhint"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/updates/2020/01/devtools/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  