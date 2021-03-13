---
description: Affichage 3D, Visual Studio’intégration à Microsoft Edge, et bien plus encore.
title: Nouveautés de DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 204a596e2497415eefeeb8aa819106635ff30caa
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408359"
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
# <a name="whats-new-in-devtools-microsoft-edge-81"></a>Nouveautés de DevTools (Microsoft Edge 81)  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Annonces de l’équipe Microsoft Edge DevTools  

Les sections suivantes sont une liste des annonces que vous avez peut-être manquées de l’équipe Microsoft Edge DevTools.  Consultez les annonces pour essayer de nouvelles fonctionnalités des extensions DevTools, Microsoft Visual Studio Code, etc.  Pour rester à jour sur toutes les fonctionnalités les plus récentes et les plus importantes de vos outils de développement, téléchargez les canaux d’aperçu [Microsoft Edge][MicrosoftEdgePreviewChannels] et [suivez-nous sur Twitter.][EdgeDevToolsTwitterAccount]  

### <a name="accessibility-improvements-to-the-devtools"></a>Améliorations de l’accessibilité de DevTools  

L’équipe DevTools a apporté 170 modifications à Chromium pour résoudre les problèmes de contraste de couleur, de clavier et de lecteur d’écran à fort impact dans DevTools.  Chaque développeur qui construit le web doit être en mesure d’utiliser DevTools.  

:::image type="complex" source="../../images/2020/01/a11y-performance-tool.msft.gif" alt-text="L’outil Performances dans DevTools avec les améliorations apportées à la navigation au clavier et au lecteur d’écran" lightbox="../../images/2020/01/a11y-performance-tool.msft.gif":::
   **L’outil Performances** dans DevTools avec les améliorations apportées à la navigation au clavier et au lecteur d’écran  
:::image-end:::  

Vous souhaitez découvrir comment rendre votre page web accessible à tous vos utilisateurs ?  Téléchargez [les informations sur l’accessibilité][AccessibilityInsights] et les extensions web [pour][WebhintBrowserExtension] que Microsoft Edge commence.  

Si vous utilisez des lecteurs d’écran ou le clavier pour naviguer dans DevTools, envoyez-nous vos commentaires en nous faisant part de vos [commentaires][PostTweetEdgeDevTools] ou en criant l’icône Envoyer [des](#getting-in-touch-with-microsoft-edge-devtools-team) commentaires !  

Problème de chrome [#963183][CR963183]  

### <a name="using-the-devtools-in-other-languages"></a>Utilisation de DevTools dans d’autres langues  

De nombreux développeurs utilisent d’autres outils de développement, tels que StackOverflow et Visual Studio Code, dans leur langue native, et pas seulement en anglais.  Nous sommes ravis d’annoncer la localisation de DevTools, que vous pouvez désormais utiliser dans l’une des 10 langues en plus de l’anglais :  

:::row:::
   :::column span="":::
      Chinois \(Simplifié\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;
   :::column-end:::
   :::column span="":::
      Chinois \(Traditionnel\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Français –&#231;ais
   :::column-end:::
   :::column span="":::
      Allemand - deu deutsche
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Italien - italiano
   :::column-end:::
   :::column span="":::
      Japonais - &#26085;&#26412;&#35486;
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Coréen - &#54620;&#44397;&#50612;
   :::column-end:::
   :::column span="":::
      Portugais - portugu&#234;s
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Russe – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;
   :::column-end:::
   :::column span="":::
      Espagnol - espa&#241;ol
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

DevTools correspond automatiquement à la langue que vous utilisez pour Microsoft Edge dans `edge://settings/languages` .  

Si vous souhaitez que Microsoft Edge soit dans une langue et que vos DevTools restent en anglais, sélectionnez `F1` dans DevTools pour ouvrir [Paramètres][Settings] et désactiver la langue du navigateur Match. ****  

:::image type="complex" source="../../images/2020/01/localized-devtools.msft.png" alt-text="DevTools en allemand" lightbox="../../images/2020/01/localized-devtools.msft.png":::
   DevTools en allemand  
:::image-end:::  

**Les** messages de la console ne sont pas localisées.  Seules les chaînes utilisées dans l’interface utilisateur de DevTools sont affichées dans la langue que vous utilisez pour Microsoft Edge.  

Si vous souhaitez utiliser les DevTools dans une autre langue que celles [disponibles,][PostTweetEdgeDevTools] tweetez-nous ou sélectionnez l’icône Envoyer [des](#getting-in-touch-with-microsoft-edge-devtools-team) commentaires.  

Problème de chrome [#941561][CR941561]  

### <a name="webhint-microsoft-edge-extension"></a>extension Webhint Microsoft Edge  

L’extension Microsoft Edge webhint vous permet d’analyser facilement votre page web et d’obtenir des commentaires sur l’accessibilité, la compatibilité du navigateur, la sécurité, les performances et bien plus encore dans DevTools.  Pour plus d’informations, [https://webhint.io][Webhint] voir .  

:::image type="complex" source="../../images/2020/01/webhint-browser-extension.msft.png" alt-text="Outil Hints dans DevTools lors de l’installation de l’extension de navigateur webhint" lightbox="../../images/2020/01/webhint-browser-extension.msft.png":::
   Outil **Hints** dans DevTools lors de l’installation de l’extension de navigateur webhint  
:::image-end:::  

[Essayez l’extension de navigateur webhint dans Microsoft Edge.][MicrosoftEdgeInsiderAddons]  Une fois l’extension installée, ouvrez DevTools et choisissez **l’outil Hints.**  À partir de là, exécutez une analyse de site personnalisable.  Pour en savoir [plus, webhint.io][WebhintBrowserExtension] plus d’informations.  

### <a name="3d-view"></a>Vue 3D  

Utilisez la vue **3D** pour déboguer votre application web en naviguant dans le modèle objet de document [\(DOM\)][MDNDocumentObjectModel] ou le contexte d’empilement [d’index z.][MDNZIndex]  

:::image type="complex" source="../../images/2020/01/3dview.msft.png" alt-text="Affichage 3D dans devTools" lightbox="../../images/2020/01/3dview.msft.png":::
   Affichage 3D dans devTools  
:::image-end:::  

Pour accéder à la vue 3D, sélectionnez , tapez en mode `Ctrl`  +  `Shift`  +  `P` **3D** et **sélectionnez Afficher la vue 3D.**  

L’équipe Microsoft Edge travaille avec l’équipe Chromium sur l’interface utilisateur et ajoute des fonctionnalités à la vue 3D, donc veuillez envoyer vos [commentaires.](#getting-in-touch-with-microsoft-edge-devtools-team)  

Problème de chrome [#987787][CR987787]  

### <a name="visual-studio-code-extensions"></a>Visual Studio extensions de code  

L’équipe DevTools a également publié certaines extensions pour [Visual Studio Code][VisualStudioCode] qui vous permet d’utiliser la puissance de DevTools directement à partir de votre éditeur de texte ! Consultez les extensions ci-dessous :  

#### <a name="elements-for-microsoft-edge"></a>Éléments pour Microsoft Edge  

Utilisez l’outil Elements à partir Visual Studio Code en ajoutant les éléments pour [Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio l’extension de code.  

:::image type="complex" source="../../images/2020/01/elements-for-edge.msft.png" alt-text="L’outil Elements dans Visual Studio Code à l’aide de l’extension Elements pour Microsoft Edge" lightbox="../../images/2020/01/elements-for-edge.msft.png":::
   **L’outil Elements** dans Visual Studio Code à l’aide de l’extension Elements pour Microsoft Edge  
:::image-end:::  

Pour plus d’informations, consultez [Éléments pour l’extension][VisualStudioCodeElementEdgeExtension]de code Visual Studio Microsoft Edge.  

#### <a name="debugger-for-microsoft-edge"></a>Débogger pour Microsoft Edge  

Avec le [déboguer pour l’extension][VisualStudioMarketplaceDebuggerEdge] de code Visual Studio Microsoft Edge, déboguer JavaScript en cours d’exécution dans Microsoft Edge directement à partir Visual Studio Code.  

:::image type="complex" source="../../images/2020/01/vscode-debugger.msft.png" alt-text="Débogger pour l’extension Microsoft Edge dans Visual Studio Code" lightbox="../../images/2020/01/vscode-debugger.msft.png":::
   Débogger pour l’extension Microsoft Edge dans Visual Studio Code  
:::image-end:::  

Pour plus d’informations, [découvrez comment déboguer Microsoft Edge][VisualStudioCodeDebuggerEdgeExtension]à partir de Visual Studio Code.  

#### <a name="webhint"></a>webhint  

La [Visual Studio][VisualStudioMarketplaceWebhintExtension] l’extension de code utilise pour améliorer votre `webhint` page web pendant que vous l’écrivez.  Cette extension s’exécute et signale les diagnostics sur vos fichiers d’espace de travail en fonction de `webhint` l’analyse.  

:::image type="complex" source="../../images/2020/01/webhint-vscode-extension.msft.png" alt-text="The webhint Visual Studio Code extension analyzing a .tsx file in Visual Studio Code" lightbox="../../images/2020/01/webhint-vscode-extension.msft.png":::
   La Visual Studio l’extension de code qui analyse un `.tsx` fichier dans Visual Studio Code  
:::image-end:::  

[En savoir plus sur l Visual Studio’extension web code.][WebhintVisualStudioCodeExtension]  

### <a name="visual-studio-integration"></a>Visual Studio’intégration  

Dans Visual Studio version 2019 16.2 ou ultérieure, utilisez le déboguer Visual Studio déboguer JavaScript en cours d’exécution dans Microsoft Edge.  [Téléchargez Visual Studio 2019][MicrosoftVisualStudioDownloads] pour tester cette fonctionnalité !  

:::image type="complex" source="../../images/2020/01/vs.msft.png" alt-text="Visual Studio avec la possibilité de lancer votre application web dans Microsoft Edge Canary, Dev ou Beta" lightbox="../../images/2020/01/vs.msft.png":::
   Visual Studio avec la possibilité de lancer votre application web dans Microsoft Edge Canary, Dev ou Beta  
:::image-end:::  

[En savoir plus sur le débogage de Microsoft Edge à partir Visual Studio][MicrosoftVisualStudio].  

### <a name="tracking-prevention-console-messages"></a>Suivi des messages de la console de prévention  

La prévention du suivi est une fonctionnalité unique de Microsoft Edge qui vous empêche d’être suivi par des sites web que vous n’avez pas visités auparavant.  Le paramètre de prévention du suivi par défaut est le mode équilibré, qui bloque les suivis tiers et les suivis malveillants connus pour une expérience qui équilibre la confidentialité et la compatibilité web.  Pour vous donner plus d’informations sur la compatibilité de votre page web lorsque certains suivis sont bloqués, des messages d’avertissement ont été ajoutés dans la **console** lorsqu’un suivi est bloqué.  

:::image type="complex" source="../../images/2020/01/tracking-prevention.msft.png" alt-text="Messages dans la console lorsque la prévention du suivi bloque l’accès au stockage pour un suivi" lightbox="../../images/2020/01/tracking-prevention.msft.png":::
   Messages dans la **console lorsque la prévention** du suivi bloque l’accès au stockage pour un suivi  
:::image-end:::  

[En savoir plus sur la prévention du suivi et l’équilibre entre la confidentialité et la compatibilité web.][TrackingPrevention]  

## <a name="announcements-from-the-chromium-project"></a>Annonces du projet de Chromium  

Les sections suivantes annoncent des fonctionnalités supplémentaires disponibles dans Microsoft Edge 81 qui ont été contribués au projet Chromium open source.  

### <a name="moto-g4-support-in-device-mode"></a>Prise en charge du G4 dans le mode appareil  

Après [avoir activé la barre d’outils][DeviceToolbar]de l’appareil, simulez les dimensions d’uneport d’affichage g4 à partir de la liste **des** appareils.  

:::image type="complex" source="../../images/2020/01/motog4.msft.png" alt-text="Simulation d’uneport d’affichage G4" lightbox="../../images/2020/01/motog4.msft.png":::
   Simulation d’uneport d’affichage G4  
:::image-end:::  

Choisissez [Afficher l’image de l’appareil][DeviceFrame] pour afficher le matériel De LaG4 autour de la fenêtre d’affichage.  

:::image type="complex" source="../../images/2020/01/motog4frame.msft.png" alt-text="Affichage du matériel Du G4" lightbox="../../images/2020/01/motog4frame.msft.png":::
   Affichage du matériel Du G4  
:::image-end:::  

Fonctionnalités connexes :  

*   Ouvrez [le menu De][CommandMenu] commande et exécutez la commande pour prendre une capture d’écran de la fenêtre d’affichage qui inclut le matériel de Contrôle G4 (après l’activation de l’activation de l’affichage du cadre de `Capture screenshot` **périphérique).**  
*   [Limiter le réseau et le processeur][ThrottleNetworkAndCpu] pour simuler plus précisément les conditions de navigation web d’un utilisateur mobile.  

Problème de chrome [#924693][CR924693]  

### <a name="cookie-related-updates"></a>Mises à jour relatives aux cookies  

#### <a name="blocked-cookies-in-the-cookies-pane"></a>Cookies bloqués dans le volet Cookies  

Le volet Cookies du panneau Application affiche désormais les cookies bloqués avec un arrière-plan jaune.  

:::image type="complex" source="../../images/2020/01/blockedcookies.msft.png" alt-text="Cookies bloqués dans le volet Cookies du panneau Application" lightbox="../../images/2020/01/blockedcookies.msft.png":::
   Cookies bloqués dans le volet Cookies du panneau Application  
:::image-end:::  

Problème de chrome [#1030258][CR1030258]  <!-- inaccessible  -->  

#### <a name="cookie-priority-in-the-cookie-pane"></a>Priorité des cookies dans le volet Cookie  

Les tableaux Cookies des **outils** Réseau et **Application** incluent désormais une **colonne** Priorité.  

> [!CAUTION]
> Les navigateurs basés sur Chromium, tels que Microsoft Edge, sont les seuls à prise en charge de la priorité des cookies.  

Problème de chrome [#1026879][CR1026879]  

#### <a name="edit-all-cookie-values"></a>Modifier toutes les valeurs de cookie  

Toutes les cellules des tableaux cookies sont modifiables maintenant, à l’exception des cellules de la colonne **Size,** car cette colonne représente la taille réseau du cookie, en octets.  Pour obtenir une explication de chaque colonne, accédez à [Champs.][CookiesFields]  

:::image type="complex" source="../../images/2020/01/editcookie.msft.png" alt-text="Modification d’une valeur de cookie" lightbox="../../images/2020/01/editcookie.msft.png":::
   Modification d’une valeur de cookie  
:::image-end:::  

#### <a name="copy-as-nodejs-fetch-to-include-cookie-data"></a>Copier en tant que Node.js pour inclure des données de cookie  

Pour obtenir une expression qui inclut des données de cookie, pointez sur une demande réseau, ouvrez le menu contextuel `fetch` \(clic droit\), puis choisissez Copier comme Node.js ****  >  **récupérer.**  

:::image type="complex" source="../../images/2020/01/fetchcookies.msft.png" alt-text="Copier en tant Node.js récupérer" lightbox="../../images/2020/01/fetchcookies.msft.png":::
   Copier en tant Node.js récupérer  
:::image-end:::  

Problème de chrome [#1029826][CR1029826]  

### <a name="more-accurate-web-app-manifest-icons"></a>Icônes de manifeste d’application web plus précises  

Auparavant, le volet Manifeste du panneau Application envoyait ses propres demandes afin d’afficher les icônes de manifeste d’application web.  DevTools affiche désormais la même icône de manifeste que Microsoft Edge utilise.  

:::image type="complex" source="../../images/2020/01/manifesticons.msft.png" alt-text="Icônes dans le volet manifeste" lightbox="../../images/2020/01/manifesticons.msft.png":::
   Icônes dans le volet manifeste  
:::image-end:::  

Problème de chrome [#985402][CR985402]  

### <a name="hover-on-css-content-properties-to-display-unescaped-values"></a>Pointer sur les propriétés de contenu CSS pour afficher des valeurs non scaped  

Pointez sur la valeur d’une propriété pour afficher la `content` version sans paysage de la valeur.  

Par exemple, dans cette [démonstration,][CSSContentDemo] lorsque vous examinez le pseudo-élément, une chaîne d’échappée s’affiche `p::after` dans le volet **Styles** :  

:::image type="complex" source="../../images/2020/01/escapedstring.msft.png" alt-text="Chaîne d’échadé" lightbox="../../images/2020/01/escapedstring.msft.png":::
   Chaîne d’échadé  
:::image-end:::  

Lorsque vous pointez sur la `content` valeur, la valeur non érosée s’affiche.  

:::image type="complex" source="../../images/2020/01/unescapedstring.msft.png" alt-text="Valeur non scaped" lightbox="../../images/2020/01/unescapedstring.msft.png":::
   Valeur non scaped  
:::image-end:::  

### <a name="more-detailed-source-map-errors-in-the-console"></a>Erreurs de carte source plus détaillées dans la console  

La console fournit désormais plus de détails sur les raisons pour lesquelles un MAP source n’a pas pu être chargé ou l’analyse.  Auparavant, il a simplement fourni une erreur sans expliquer ce qui s’est passé.  

:::image type="complex" source="../../images/2020/01/sourcemap.msft.png" alt-text="Erreur de chargement d’une carte source dans la console" lightbox="../../images/2020/01/sourcemap.msft.png":::
   Erreur de chargement d’une carte source dans la console  
:::image-end:::  

### <a name="setting-for-disabling-scrolling-past-the-end-of-a-file"></a>Paramètre de désactivation du défilement au-delà de la fin d’un fichier  

Ouvrez [Paramètres,][Settings] **** puis désactivez Préférences Sources Autoriser le défilement au-delà de la fin du fichier pour désactiver le comportement de l’interface utilisateur par défaut qui vous permet de faire défiler bien au-delà de la fin d’un fichier dans le panneau  >  ****  >  **** **Sources.**  

:::image type="complex" source="../../images/2020/01/settings.msft.png" alt-text="Désactivation de l’utilisation du défilement au-delà de la fin du fichier" lightbox="../../images/2020/01/settings.msft.png":::
   Désactivation de **l’utilisation du défilement au-delà de la fin du fichier** dans paramètres  
:::image-end:::  

:::image type="complex" source="../../images/2020/01/scrollingsources.msft.png" alt-text="Le défilement au-delà de la fin d’un fichier est désormais désactivé dans le panneau Sources" lightbox="../../images/2020/01/scrollingsources.msft.png":::
   Le défilement au-delà de la fin d’un fichier est désormais désactivé dans le panneau Sources  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Télécharger les canaux d’aperçu Microsoft Edge  

Si vous utilisez Windows ou macOS, envisagez d’utiliser les canaux d’aperçu [Microsoft Edge][MicrosoftEdgePreviewChannels] comme navigateur de développement par défaut.  Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Contacter l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DeviceToolbar]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simuler une port d’affichage mobile : simuler des appareils mobiles avec le mode appareil dans Microsoft Edge DevTools | Documents Microsoft"
[DeviceFrame]: /microsoft-edge/devtools-guide-chromium/device-mode/index#show-device-frame "Afficher l’image de l’appareil : simuler des appareils mobiles avec le mode appareil dans Microsoft Edge DevTools | Documents Microsoft"
[CommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Exécuter des commandes avec le menu de commandes Microsoft Edge DevTools | Documents Microsoft"  
[ThrottleNetworkAndCpu]: /microsoft-edge/devtools-guide-chromium/device-mode/index#throttle-the-network-and-cpu "Limiter le réseau et le processeur : simuler des appareils mobiles en mode appareil dans Microsoft Edge DevTools | Documents Microsoft"
[Settings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"
[MicrosoftVisualStudio]: /microsoft-edge/visual-studio/index "Visual Studio | Documents Microsoft"  
[CookiesFields]: /microsoft-edge/devtools-guide-chromium/storage/cookies#fields "Champs : afficher, modifier et supprimer des cookies avec Microsoft Edge DevTools | Documents Microsoft"  

[VisualStudioCodeDebuggerEdgeExtension]: /microsoft-edge/visual-studio-code/debugger-for-edge "Débogger pour l’extension de code Visual Studio Microsoft Edge"  
[VisualStudioCodeElementEdgeExtension]: /microsoft-edge/visual-studio-code/elements-for-edge "Éléments de l’extension de code Visual Studio Microsoft Edge"  

[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canaux d’aperçu Microsoft Edge"  

[VisualStudioCode]: https://aka.ms/vscode "Visual Studio Code"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Débogger pour Microsoft Edge - Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Éléments pour Microsoft Edge \(Chromium\) - Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint - Visual Studio Marketplace"

[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Amélioration de la prévention du suivi dans le billet de blog de Microsoft Edge"

[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Microsoft Edge Insider Addons"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Télécharger Visual Studio 2019 pour Windows & Mac"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publier un tweet"  

[CR924693]: https://crbug.com/924693 "Demande de fonctionnalité : ajouter Le G4 à la liste des modes d’appareil | Bogues Chromium"  
[CR1030258]: https://crbug.com/1030258 "Cr 1030258 | Bogues Chromium"  
[CR1026879]: https://crbug.com/1026879 "L’onglet Cookie de la console dev n’affiche plus la priorité | Bogues Chromium"  
[CR1029826]: https://crbug.com/1029826 "onglet réseau -> choisir de demander -> copie -> copie, car l’extraction ne copie pas les cookies | Bogues Chromium"  
[CR985402]: https://crbug.com/985402 "Les chaînes d’erreur d’icône de manifeste d’application web | Bogues Chromium"  
[CR963183]: https://crbug.com/963183 "DevTools ne sont pas conformes WCAG | Bogues Chromium"  
[CR941561]: https://crbug.com/941561 "Localisabilité du | DevTools Bogues Chromium"  
[CR987787]: https://crbug.com/987787 "Vue Dom 3D | Bogues Chromium"  

[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Démonstration du contenu CSS sans paysage"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nouveau problème : MicrosoftDocs/edge-developer"  

[TheWebWeWant]: https://aka.ms/webwewant "Le site web que nous voulons"  
[AccessibilityInsights]: https://aka.ms/a11yinsights "Informations sur l’accessibilité"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Document Object Model (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-index | MDN"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools compte Twitter"  

[Webhint]: https://aka.ms/webhint "webhint"  

[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Webhint Browser Extension | documentation webhint"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Webhint Visual Studio extension de code | documentation webhint"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/updates/2020/01/devtools/index) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  