---
description: Affichage 3D, Visual Studio’intégration à Microsoft Edge, et bien plus encore.
title: Nouveautés de DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 03b17f524e9be55e1ed37147ce46b7a15fc3a17d
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564958"
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

Les sections suivantes sont une liste des annonces que vous avez peut-être manquées de l’équipe Microsoft Edge DevTools.  Consultez les annonces pour essayer de nouvelles fonctionnalités dans DevTools, Microsoft Visual Studio extensions de code, etc.  Pour rester à jour sur toutes les fonctionnalités les plus récentes et les plus importantes de vos outils de développement, téléchargez les canaux d’aperçu [Microsoft Edge][MicrosoftEdgePreviewChannels] et suivez-nous [sur Twitter.][EdgeDevToolsTwitterAccount]  

### <a name="accessibility-improvements-to-the-devtools"></a>Améliorations de l’accessibilité de DevTools  

L’équipe DevTools a apporté 170 modifications à Chromium pour résoudre les problèmes de contraste de couleur, de clavier et de lecteur d’écran à fort impact dans DevTools.  Chaque développeur qui construit le web doit être en mesure d’utiliser DevTools.  

:::image type="complex" source="../../images/2020/01/a11y-performance-tool.msft.gif" alt-text="L’outil Performances dans DevTools avec les améliorations apportées à la navigation au clavier et au lecteur d’écran" lightbox="../../images/2020/01/a11y-performance-tool.msft.gif":::
   **L’outil Performances** dans DevTools avec les améliorations apportées à la navigation au clavier et au lecteur d’écran  
:::image-end:::  

Vous souhaitez découvrir comment rendre votre page web accessible à tous vos utilisateurs ?  Téléchargez [les informations sur l’accessibilité][AccessibilityInsights] et les extensions web [pour][WebhintBrowserExtension] Microsoft Edge commencer.  

Si vous utilisez des lecteurs d’écran ou le clavier pour naviguer dans DevTools, envoyez-nous vos commentaires en nous faisant part de vos [commentaires][PostTweetEdgeDevTools] ou en criant l’icône Envoyer [des](#getting-in-touch-with-microsoft-edge-devtools-team) commentaires !  

Chromium problème [#963183][CR963183]  

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

DevTools correspond automatiquement à la langue que vous utilisez pour Microsoft Edge `edge://settings/languages` dans .  

Si vous souhaitez que Microsoft Edge soit dans une langue et que vos DevTools restent en anglais, sélectionnez `F1` dans DevTools pour ouvrir [Paramètres][DevtoolsCustomizeIndexSettings] et désactiver la langue du navigateur **Match.**  

:::image type="complex" source="../../images/2020/01/localized-devtools.msft.png" alt-text="DevTools en allemand" lightbox="../../images/2020/01/localized-devtools.msft.png":::
   DevTools en allemand  
:::image-end:::  

**Les** messages de la console ne sont pas localisées.  Seules les chaînes utilisées dans l’interface utilisateur de DevTools sont affichées dans la langue que vous utilisez pour Microsoft Edge.  

Si vous souhaitez utiliser les DevTools dans une autre langue que celles [disponibles,][PostTweetEdgeDevTools] tweetez-nous ou sélectionnez l’icône Envoyer [des](#getting-in-touch-with-microsoft-edge-devtools-team) commentaires.  

Chromium problème [#941561][CR941561]  

### <a name="webhint-microsoft-edge-extension"></a>extension de Microsoft Edge webhint  

L’extension de Microsoft Edge web vous permet d’analyser facilement votre page web et d’obtenir des commentaires sur l’accessibilité, la compatibilité du navigateur, la sécurité, les performances et bien plus encore dans DevTools.  Pour plus d’informations, [https://webhint.io][Webhint] voir .  

:::image type="complex" source="../../images/2020/01/webhint-browser-extension.msft.png" alt-text="Outil Hints dans DevTools lors de l’installation de l’extension de navigateur webhint" lightbox="../../images/2020/01/webhint-browser-extension.msft.png":::
   Outil **Hints** dans DevTools lors de l’installation de l’extension de navigateur webhint  
:::image-end:::  

[Essayez l’extension de navigateur webhint dans Microsoft Edge][MicrosoftEdgeInsiderAddons].  Une fois l’extension installée, ouvrez DevTools et choisissez **l’outil Hints.**  À partir de là, exécutez une analyse de site personnalisable.  Pour en savoir [plus, webhint.io][WebhintBrowserExtension] plus d’informations.  

### <a name="3d-view"></a>Vue 3D  

Utilisez la vue **3D** pour déboguer votre application web en naviguant dans le modèle objet de document [\(DOM\)][MDNDocumentObjectModel] ou le contexte d’empilement [d’index z.][MDNZIndex]  

:::image type="complex" source="../../images/2020/01/3dview.msft.png" alt-text="Affichage 3D dans devTools" lightbox="../../images/2020/01/3dview.msft.png":::
   Affichage 3D dans devTools  
:::image-end:::  

Pour accéder à la vue 3D, sélectionnez , tapez en mode `Ctrl`  +  `Shift`  +  `P` **3D,** puis **sélectionnez Afficher la vue 3D.**  

L Microsoft Edge l’équipe Chromium sur l’interface utilisateur et ajoute des fonctionnalités à l’affichage 3D. Envoyez donc vos [commentaires.](#getting-in-touch-with-microsoft-edge-devtools-team)  

Chromium problème [#987787][CR987787]  

### <a name="visual-studio-code-extensions"></a>Visual Studio Code extensions  

L’équipe DevTools a également publié certaines extensions pour [Visual Studio Code][VisualStudioCode] qui vous permet d’utiliser la puissance de DevTools directement à partir de votre éditeur de texte ! Consultez les extensions ci-dessous :  

#### <a name="elements-for-microsoft-edge"></a>Éléments pour Microsoft Edge  

Utilisez l’outil Éléments à partir de Visual Studio Code en ajoutant l’extension Microsoft Edge [\(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code extension.  

:::image type="complex" source="../../images/2020/01/elements-for-edge.msft.png" alt-text="L’outil Elements dans Visual Studio Code à l’aide de l’extension Elements for Microsoft Edge" lightbox="../../images/2020/01/elements-for-edge.msft.png":::
   **L’outil Elements** dans Visual Studio Code l’aide de l’extension Elements for Microsoft Edge  
:::image-end:::  

Pour plus d’informations, consultez [Éléments pour Microsoft Edge Visual Studio Code extension.][VisualStudioCodeElementEdgeExtension]  

#### <a name="debugger-for-microsoft-edge"></a>Débogger pour Microsoft Edge  

Avec [l’extension Déboguer pour Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code, déboguer JavaScript en cours d’exécution Microsoft Edge directement à partir Visual Studio Code.  

:::image type="complex" source="../../images/2020/01/vscode-debugger.msft.png" alt-text="Débogger pour l’extension Microsoft Edge dans Visual Studio Code" lightbox="../../images/2020/01/vscode-debugger.msft.png":::
   Débogger pour l’extension Microsoft Edge dans Visual Studio Code  
:::image-end:::  

Pour plus d’informations, [découvrez comment déboguer][VisualStudioCodeDebuggerEdgeExtension]des Microsoft Edge à partir Visual Studio Code .  

#### <a name="webhint"></a>webhint  

[L’extension de Visual Studio Code][VisualStudioMarketplaceWebhintExtension] web utilise pour améliorer votre page web pendant que vous `webhint` l’écrivez.  Cette extension s’exécute et signale les diagnostics sur vos fichiers d’espace de travail en fonction de `webhint` l’analyse.  

:::image type="complex" source="../../images/2020/01/webhint-vscode-extension.msft.png" alt-text="Extension webhint Visual Studio Code’analyse d’un fichier .tsx dans Visual Studio Code" lightbox="../../images/2020/01/webhint-vscode-extension.msft.png":::
   Extension webhint Visual Studio Code’analyse `.tsx` d’un fichier dans Visual Studio Code  
:::image-end:::  

[En savoir plus sur l’extension Visual Studio Code webhint.][WebhintVisualStudioCodeExtension]  

### <a name="visual-studio-integration"></a>Visual Studio’intégration  

Dans Visual Studio version 2019 16.2 ou ultérieure, utilisez le déboguer Visual Studio déboguer JavaScript en cours d’exécution Microsoft Edge.  [Téléchargez Visual Studio 2019][MicrosoftVisualStudioDownloads] pour tester cette fonctionnalité !  

:::image type="complex" source="../../images/2020/01/vs.msft.png" alt-text="Visual Studio avec la possibilité de lancer votre application web dans Microsoft Edge Canary, Dev ou Beta" lightbox="../../images/2020/01/vs.msft.png":::
   Visual Studio avec la possibilité de lancer votre application web dans Microsoft Edge Canary, Dev ou Beta  
:::image-end:::  

[En savoir plus sur le débogage Microsoft Edge à partir Visual Studio][VisualStudioIndex].  

### <a name="tracking-prevention-console-messages"></a>Suivi des messages de la console de prévention  

La prévention du suivi est une fonctionnalité unique dans Microsoft Edge qui vous protège contre le suivi par les sites web que vous n’avez pas visités auparavant.  Le paramètre de prévention du suivi par défaut est le mode équilibré, qui bloque les suivis tiers et les suivis malveillants connus pour une expérience qui équilibre la confidentialité et la compatibilité web.  Pour vous donner plus d’informations sur la compatibilité de votre page web lorsque certains suivis sont bloqués, des messages d’avertissement ont été ajoutés dans la **console** lorsqu’un suivi est bloqué.  

:::image type="complex" source="../../images/2020/01/tracking-prevention.msft.png" alt-text="Messages dans la console lorsque la prévention du suivi bloque l’accès au stockage pour un suivi" lightbox="../../images/2020/01/tracking-prevention.msft.png":::
   Messages dans la **console lorsque la prévention** du suivi bloque l’accès au stockage pour un suivi  
:::image-end:::  

[En savoir plus sur la prévention du suivi et l’équilibre entre la confidentialité et la compatibilité web.][TrackingPrevention]  

## <a name="announcements-from-the-chromium-project"></a>Annonces du projet de Chromium  

Les sections suivantes annoncent des fonctionnalités supplémentaires disponibles dans Microsoft Edge 81 qui ont été contribués au projet d’Chromium open source.  

### <a name="moto-g4-support-in-device-mode"></a>Prise en charge du G4 dans le mode appareil  

Après [avoir activé la barre d’outils][DevtoolsDeviceModeIndexSimulateMobileViewport]de l’appareil, simulez les dimensions d’uneport d’affichage g4 à partir de la liste **des** périphériques.  

:::image type="complex" source="../../images/2020/01/motog4.msft.png" alt-text="Simulation d’uneport d’affichage G4" lightbox="../../images/2020/01/motog4.msft.png":::
   Simulation d’uneport d’affichage G4  
:::image-end:::  

Sélectionnez [Afficher le cadre de][DevtoolsDeviceModeIndexShowDeviceFrame] l’appareil pour afficher le matériel de LaG4 autour de la fenêtre d’affichage.  

:::image type="complex" source="../../images/2020/01/motog4frame.msft.png" alt-text="Affichage du matériel Du G4" lightbox="../../images/2020/01/motog4frame.msft.png":::
   Affichage du matériel Du G4  
:::image-end:::  

Fonctionnalités connexes :  

*   Ouvrez [le menu Commande][DevtoolsCommandMenuIndex] et exécutez la commande pour prendre une capture d’écran de la fenêtre d’affichage qui inclut le matériel de Contrôle G4 (après l’activation de l’activation de l’affichage du cadre de `Capture screenshot` **périphérique).**  
*   [Limiter le réseau et le processeur][DevtoolsDeviceModeIndexThrottleNetworkCpu] pour simuler plus précisément les conditions de navigation web d’un utilisateur mobile.  

Chromium problème [#924693][CR924693]  

### <a name="cookie-related-updates"></a>Mises à jour relatives aux cookies  

#### <a name="blocked-cookies-in-the-cookies-pane"></a>Cookies bloqués dans le volet Cookies  

Le volet Cookies du panneau Application affiche désormais les cookies bloqués avec un arrière-plan jaune.  

:::image type="complex" source="../../images/2020/01/blockedcookies.msft.png" alt-text="Cookies bloqués dans le volet Cookies du panneau Application" lightbox="../../images/2020/01/blockedcookies.msft.png":::
   Cookies bloqués dans le volet Cookies du panneau Application  
:::image-end:::  

Chromium problème [#1030258][CR1030258]  <!-- inaccessible  -->  

#### <a name="cookie-priority-in-the-cookie-pane"></a>Priorité des cookies dans le volet Cookie  

Les tableaux Cookies des **outils** Réseau et **Application** incluent désormais une **colonne** Priorité.  

> [!CAUTION]
> Chromium navigateurs, tels que Microsoft Edge, sont les seuls navigateurs qui utilisent la priorité des cookies.  

Chromium problème [#1026879][CR1026879]  

#### <a name="edit-all-cookie-values"></a>Modifier toutes les valeurs de cookie  

Toutes les cellules des tableaux cookies sont modifiables maintenant, à l’exception des cellules de la colonne **Size,** car cette colonne représente la taille réseau du cookie, en octets.  Pour obtenir une explication de chaque colonne, accédez à [Champs.][DevtoolsStorageCookiesFields]  

:::image type="complex" source="../../images/2020/01/editcookie.msft.png" alt-text="Modification d’une valeur de cookie" lightbox="../../images/2020/01/editcookie.msft.png":::
   Modification d’une valeur de cookie  
:::image-end:::  

#### <a name="copy-as-nodejs-fetch-to-include-cookie-data"></a>Copier en tant que Node.js pour inclure des données de cookie  

Pour obtenir une expression qui inclut des données de cookie, pointez sur une demande réseau, ouvrez le menu contextuel `fetch` \(clic droit\), puis choisissez Copier comme Node.js ****  >  **récupérer.**  

:::image type="complex" source="../../images/2020/01/fetchcookies.msft.png" alt-text="Copier en tant Node.js récupérer" lightbox="../../images/2020/01/fetchcookies.msft.png":::
   Copier en tant Node.js récupérer  
:::image-end:::  

Chromium problème [#1029826][CR1029826]  

### <a name="more-accurate-web-app-manifest-icons"></a>Icônes de manifeste d’application web plus précises  

Auparavant, le volet Manifeste du panneau Application envoyait ses propres demandes afin d’afficher les icônes de manifeste d’application web.  DevTools affiche maintenant la même icône de manifeste que celle Microsoft Edge utilise.  

:::image type="complex" source="../../images/2020/01/manifesticons.msft.png" alt-text="Icônes dans le volet manifeste" lightbox="../../images/2020/01/manifesticons.msft.png":::
   Icônes dans le volet manifeste  
:::image-end:::  

Chromium problème [#985402][CR985402]  

### <a name="hover-on-css-content-properties-to-display-unescaped-values"></a>Pointer sur les propriétés de contenu CSS pour afficher des valeurs non scaped  

Pointez sur la valeur d’une propriété pour afficher la `content` version non érosée de la valeur.  

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

Ouvrez [Paramètres][DevtoolsCustomizeIndexSettings] puis désactivez Préférences **** Sources Autoriser le défilement au-delà de la fin du fichier pour désactiver le comportement d’interface utilisateur par défaut qui vous permet de faire défiler bien au-delà de la fin d’un fichier dans le panneau  >  ****  >  **** **Sources.**  

:::image type="complex" source="../../images/2020/01/settings.msft.png" alt-text="Désactivation de l’utilisation du défilement au-delà de la fin du fichier" lightbox="../../images/2020/01/settings.msft.png":::
   Désactivation de **l’utilisation du défilement au-delà de la fin du** fichier dans Paramètres  
:::image-end:::  

:::image type="complex" source="../../images/2020/01/scrollingsources.msft.png" alt-text="Le défilement au-delà de la fin d’un fichier est désormais désactivé dans le panneau Sources" lightbox="../../images/2020/01/scrollingsources.msft.png":::
   Le défilement au-delà de la fin d’un fichier est désormais désactivé dans le panneau Sources  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Télécharger les canaux d’aperçu Microsoft Edge  

Si vous êtes sur Windows ou macOS, envisagez d’utiliser les canaux d Microsoft Edge [d’aperçu][MicrosoftEdgePreviewChannels] comme navigateur de développement par défaut.  Les canaux de prévisualisation vous donnent accès aux dernières fonctionnalités de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Contacter l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Simuler une port d’affichage mobile : simuler des appareils mobiles en mode Microsoft Edge devTools | Documents Microsoft"
[DevtoolsDeviceModeIndexShowDeviceFrame]: ../../../device-mode/index.md#show-device-frame "Afficher l’image de l’appareil : simuler des appareils mobiles en mode Microsoft Edge devTools | Documents Microsoft"
[DevtoolsCommandMenuIndex]: ../../../command-menu/index.md "Exécuter des commandes avec le menu de commande DevTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsDeviceModeIndexThrottleNetworkCpu]: ../../../device-mode/index.md#throttle-the-network-and-cpu "Limiter le réseau et le processeur : simuler des appareils mobiles en mode appareil Microsoft Edge devTools | Documents Microsoft"
[DevtoolsCustomizeIndexSettings]: ../../../customize/index.md#settings "Paramètres - Personnaliser Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsStorageCookiesFields]: ../../../storage/cookies.md#fields "Champs : afficher, modifier et supprimer des cookies avec Microsoft Edge devTools | Documents Microsoft"  

[VisualStudioIndex]: ../../../../visual-studio/index.md "Visual Studio | Documents Microsoft"  

[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Débogger pour les Microsoft Edge Visual Studio Code d’extension | Documents Microsoft"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Éléments pour les Microsoft Edge Visual Studio Code d’extension | Documents Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux de préversion de Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioMarketplaceDebuggerEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Débogger pour Microsoft Edge | Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Éléments pour Microsoft Edge \(Chromium\) | Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"

[TrackingPrevention]: https://blogs.windows.com/msedgedev/2019/12/03/improving-tracking-prevention-microsoft-edge-79 "Amélioration de la prévention du suivi dans Microsoft Edge billet de blog"

[MicrosoftEdgeInsiderAddons]: https://microsoftedge.microsoft.com/addons/detail/webhint/mlgfbihcfnkaenjpdcngdnhcpkdmcdee "Microsoft Edge Insider Addons"  
[MicrosoftVisualStudioDownloads]: https://visualstudio.microsoft.com/downloads "Télécharger Visual Studio 2019 pour Windows & Mac"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publier un tweet"  

[CR924693]: https://crbug.com/924693 "Demande de fonctionnalité : ajouter Le G4 à la liste des modes d’appareil | Chromium Bogues"  
[CR1030258]: https://crbug.com/1030258 "Cr 1030258 | Chromium Bogues"  
[CR1026879]: https://crbug.com/1026879 "L’onglet Cookie de la console dev n’affiche plus la priorité | Chromium Bogues"  
[CR1029826]: https://crbug.com/1029826 "onglet réseau -> choisir de demander -> copie -> copie, car l’extraction ne copie pas les cookies | Chromium Bogues"  
[CR985402]: https://crbug.com/985402 "Les chaînes d’erreur d’icône de manifeste d’application web | Chromium Bogues"  
[CR963183]: https://crbug.com/963183 "Les devTools ne sont pas conformes AUX WCAG | Chromium Bogues"  
[CR941561]: https://crbug.com/941561 "Localisabilité du | DevTools Chromium Bogues"  
[CR987787]: https://crbug.com/987787 "Vue Dom 3D | Chromium Bogues"  

[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Démonstration du contenu CSS sans paysage"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Nouveau problème : MicrosoftDocs/edge-developer"  

[TheWebWeWant]: https://webwewant.fyi "Le site web que nous voulons"  
[AccessibilityInsights]: https://accessibilityinsights.io "Informations sur l’accessibilité"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Document Object Model (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-index | MDN"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools compte Twitter"  

[Webhint]: https://webhint.io "webhint"  

[WebhintBrowserExtension]: https://webhint.io/docs/user-guide/extensions/extension-browser "Webhint Browser Extension | documentation webhint"  
[WebhintVisualStudioCodeExtension]: https://webhint.io/docs/user-guide/extensions/vscode-webhint "Webhint Visual Studio Code extension | documentation webhint"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developer.chrome.com/blog/new-in-devtools-81) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  