---
description: Améliorations de l’accessibilité, à l’aide de DevTools dans d’autres langues, et bien plus encore.
title: Nouveautés de DevTools (Microsoft Edge 80)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 58e5bf43720c7ba94a721804eb44d82ba657b599
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564993"
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
# <a name="whats-new-in-devtools-microsoft-edge-80"></a>Nouveautés de DevTools (Microsoft Edge 80)  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Annonces de l’équipe Microsoft Edge DevTools  

Les sections suivantes sont une liste d’annonces que vous avez peut-être manquées de l’équipe Microsoft Edge DevTools.  Consultez les annonces pour essayer de nouvelles fonctionnalités dans DevTools, Microsoft Visual Studio extensions de code, etc.  Pour rester à jour sur toutes les fonctionnalités les plus récentes et les plus importantes de vos outils de développement, téléchargez les canaux d’aperçu [Microsoft Edge][MicrosoftEdgePreviewChannels] et suivez-nous [sur Twitter.][EdgeDevToolsTwitterAccount]  

### <a name="accessibility-improvements-to-the-devtools"></a>Améliorations de l’accessibilité de DevTools  

L’équipe DevTools a apporté 170 modifications à Chromium pour résoudre les problèmes de contraste de couleur, de clavier et de lecteur d’écran à fort impact dans DevTools.  Chaque développeur qui construit le web doit être en mesure d’utiliser DevTools.  

:::image type="complex" source="../../images/2019/12/a11y-performance-tool.msft.gif" alt-text="L’outil Performances dans DevTools avec les améliorations apportées à la navigation au clavier et au lecteur d’écran" lightbox="../../images/2019/12/a11y-performance-tool.msft.gif":::
   **L’outil Performances** dans DevTools avec les améliorations apportées à la navigation au clavier et au lecteur d’écran  
:::image-end:::  

Vous souhaitez découvrir comment rendre votre page web accessible à tous vos utilisateurs ?  Téléchargez [les informations sur l’accessibilité][AccessibilityInsights] et les extensions web [pour][WebhintBrowserExtension] Microsoft Edge commencer.  

Si vous utilisez des lecteurs d’écran ou le clavier pour naviguer dans DevTools, envoyez vos commentaires en [tweetant][PostTweetEdgeDevTools] sur nous ou en cinglant l’icône Envoyer [des](#getting-in-touch-with-microsoft-edge-devtools-team) commentaires !  

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
| Chinese (Simplified) - 中文（简体）| Chinese (Traditional) - 中文（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

Accédez à l’indicateur Activer les outils de développement localisées et `edge://flags` définissez-le **sur Activé.** ****  Définissez également **l’indicateur d’expériences Outils** de développement **sur Activé.**  Redémarrez Microsoft Edge et ouvrez DevTools.  <!-- Select `F1` in the DevTools or navigate to Settings > Experiments and check the **Match browser language** checkbox.  -->  Les DevTools correspondent à la langue que vous utilisez pour Microsoft Edge `edge://settings/languages` dans .  

:::image type="complex" source="../../images/2019/12/localized-devtools.msft.png" alt-text="DevTools en allemand" lightbox="../../images/2019/12/localized-devtools.msft.png":::
   DevTools en allemand  
:::image-end:::  

Si vous souhaitez utiliser les DevTools dans une autre langue que celles [disponibles,][PostTweetEdgeDevTools] tweetez-nous ou sélectionnez l’icône Envoyer [des](#getting-in-touch-with-microsoft-edge-devtools-team) commentaires.  

Chromium problème [#941561][CR941561]  

### <a name="webhint-microsoft-edge-extension"></a>extension de Microsoft Edge webhint  

L’extension de Microsoft Edge web vous permet d’analyser facilement votre page web et d’obtenir des commentaires sur l’accessibilité, la compatibilité du navigateur, la sécurité, les performances et bien plus encore dans DevTools.  Pour plus d’informations, [https://webhint.io][Webhint] voir .  

:::image type="complex" source="../../images/2019/12/webhint-browser-extension.msft.png" alt-text="Outil Hints dans DevTools lors de l’installation de l’extension de navigateur webhint" lightbox="../../images/2019/12/webhint-browser-extension.msft.png":::
   Outil **Hints** dans DevTools lors de l’installation de l’extension de navigateur webhint  
:::image-end:::  

[Essayez l’extension de navigateur webhint dans Microsoft Edge][MicrosoftEdgeInsiderAddons].  Une fois l’extension installée, ouvrez DevTools et choisissez l’outil **Hints.**  À partir de là, exécutez une analyse de site personnalisable.  Pour en savoir [plus, webhint.io][WebhintBrowserExtension] plus d’informations.

### <a name="3d-view"></a>Vue 3D  

Utilisez la vue **3D** pour déboguer votre application web en naviguant dans le modèle objet de document [\(DOM\)][MDNDocumentObjectModel] ou le contexte d’empilement [d’index z.][MDNZIndex]  

:::image type="complex" source="../../images/2019/12/3dview.msft.png" alt-text="Affichage 3D dans devTools" lightbox="../../images/2019/12/3dview.msft.png":::
   Affichage **3D** dans devTools  
:::image-end:::  

Pour accéder à la vue 3D, accédez à l’indicateur d’expériences Outils de développement et assurez-vous qu’il `edge://flags` est activé. **** ****  Redémarrez Microsoft Edge et ouvrez DevTools.  Sélectionnez dans DevTools ou ouvrez la section Paramètres Expériences, puis activez la case à cocher Activer l’affichage `F1` ****  >  **** **3D.**  Maintenant, `Ctrl`  +  `Shift`  +  `P` sélectionnez , tapez **en mode 3D et** **sélectionnez Afficher la vue 3D.**  

Nous travaillons sur l’interface utilisateur et ajoutons des fonctionnalités à l’affichage 3D. Veuillez donc nous envoyer vos [commentaires.](#getting-in-touch-with-microsoft-edge-devtools-team)  

Chromium problème [#987787][CR987787]

### <a name="visual-studio-code-extensions"></a>Visual Studio Code extensions  

L’équipe DevTools a également publié certaines extensions pour [Visual Studio Code][VisualStudioCode] qui vous permet d’utiliser la puissance de DevTools directement à partir de votre éditeur de texte. Consultez les extensions suivantes.  

#### <a name="elements-for-microsoft-edge"></a>Éléments pour Microsoft Edge  

Utilisez l’outil Elements depuis Visual Studio Code en ajoutant l’extension de Microsoft Edge [(Chromium)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code éléments.  

:::image type="complex" source="../../images/2019/12/elements-for-edge.msft.png" alt-text="L’outil Elements dans Visual Studio Code l’aide de l’extension Elements for Microsoft Edge" lightbox="../../images/2019/12/elements-for-edge.msft.png":::
   **L’outil Elements** dans Visual Studio Code l’aide de l’extension Elements for Microsoft Edge  
:::image-end:::  

Pour plus d’informations, consultez [Éléments pour Microsoft Edge Visual Studio Code extension.][VisualStudioCodeElementEdgeExtension]  

#### <a name="debugger-for-microsoft-edge"></a>Débogger pour Microsoft Edge  

Avec [l’extension Déboguer pour Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code, déboguer JavaScript en cours d’exécution Microsoft Edge directement à partir Visual Studio Code.  

:::image type="complex" source="../../images/2019/12/vscode-debugger.msft.png" alt-text="Débogger pour l’extension Microsoft Edge dans Visual Studio Code" lightbox="../../images/2019/12/vscode-debugger.msft.png":::
   Débogger pour l’extension Microsoft Edge dans Visual Studio Code  
:::image-end:::  

Pour plus d’informations, [découvrez comment déboguer][VisualStudioCodeDebuggerEdgeExtension]des Microsoft Edge à partir Visual Studio Code .  

#### <a name="webhint"></a>webhint  

[L’extension de][VisualStudioMarketplaceWebhintExtension] Visual Studio Code web utilise pour améliorer votre page web pendant `webhint` que vous l’écrivez ! Cette extension s’exécute et signale les diagnostics sur vos fichiers d’espace de travail en fonction de `webhint` l’analyse.  

:::image type="complex" source="../../images/2019/12/webhint-vscode-extension.msft.png" alt-text="Extension webhint Visual Studio Code’analyse d’un fichier .tsx dans Visual Studio Code" lightbox="../../images/2019/12/webhint-vscode-extension.msft.png":::
   Extension webhint Visual Studio Code’analyse `.tsx` d’un fichier dans Visual Studio Code  
:::image-end:::  

[En savoir plus sur l’extension Visual Studio Code webhint.][WebhintVisualStudioCodeExtension]  

### <a name="visual-studio-integration"></a>Visual Studio’intégration  

Dans Visual Studio version 2019 16.2 ou ultérieure, utilisez le déboguer Visual Studio déboguer JavaScript en cours d’exécution Microsoft Edge.  [Téléchargez Visual Studio 2019][MicrosoftVisualStudioDownloads] pour tester cette fonctionnalité.  

:::image type="complex" source="../../images/2019/12/vs.msft.png" alt-text="Visual Studio avec la possibilité de lancer votre application web dans Microsoft Edge Canary, Dev ou Beta" lightbox="../../images/2019/12/vs.msft.png":::
   Visual Studio avec la possibilité de lancer votre application web dans Microsoft Edge Canary, Dev ou Beta  
:::image-end:::  

[Lisez notre billet de blog pour découvrir comment déboguer][MicrosoftVisualStudioBlogDebugJavascript]des Microsoft Edge à partir Visual Studio .  

### <a name="tracking-prevention-console-messages"></a>Suivi des messages de la console de prévention  

La prévention du suivi est une fonctionnalité unique dans Microsoft Edge qui vous empêche d’être suivi par un site web avant de l’avoir visité.  Le paramètre de prévention du suivi par défaut est le mode équilibré, qui bloque les suivis tiers et les suivis malveillants connus pour une expérience qui équilibre la confidentialité et la compatibilité web.  Pour vous donner plus d’informations sur la compatibilité de votre page web lorsque certains suivis sont bloqués, l’équipe Microsoft Edge a ajouté des messages d’avertissement dans la **console** lorsqu’un suivi est bloqué.  

:::image type="complex" source="../../images/2019/12/tracking-prevention.msft.png" alt-text="Messages dans la console lorsque la prévention du suivi bloque l’accès au stockage pour un suivi" lightbox="../../images/2019/12/tracking-prevention.msft.png":::
   Messages dans la **console lorsque la prévention** du suivi bloque l’accès au stockage pour un suivi  
:::image-end:::  

[En savoir plus sur la prévention du suivi et l’équilibre entre la confidentialité et la compatibilité web.][TrackingPrevention]  

## <a name="announcements-from-the-chromium-project"></a>Annonces du projet de Chromium  

Les sections suivantes annoncent des fonctionnalités supplémentaires disponibles dans Microsoft Edge 80 qui ont été contribués au projet d’Chromium open source.  

### <a name="support-for-let-and-class-redeclarations-in-the-console"></a>Prise en charge des redéclarations de classes et de let dans la console  

La **console prend** désormais en charge les déclarations et les `let` `class` instructions.  L’impossibilité de redéclarer était une gêne courante pour les développeurs web qui utilisent la console pour expérimenter du nouveau code JavaScript.  

> [!WARNING]
> La déclaration d’une `let` ou `class` d’une instruction dans un script en dehors de la console ou au sein d’une seule entrée de console provoque toujours une `SyntaxError` .  

Par exemple, précédemment, lors de la nouvelle déclaration d’une variable locale avec `let` , la console a lancé une erreur :  

:::image type="complex" source="../../images/2019/12/letbefore.msft.png" alt-text="La console dans Microsoft Edge 79 indiquant que la déclaration let échoue" lightbox="../../images/2019/12/letbefore.msft.png":::
   Console **dans** Microsoft Edge 79 indiquant que la nouvelle déclaration échoue  
:::image-end:::  

À présent, la console autorise la déclaration :  

:::image type="complex" source="../../images/2019/12/letafter.msft.png" alt-text="La console dans Microsoft Edge 80 indiquant que la redéclaration a réussi" lightbox="../../images/2019/12/letafter.msft.png":::
   **Console dans** Microsoft Edge 80 indiquant que la nouvelle déclaration réussit  
:::image-end:::  

Chromium problème [#1004193][CR1004193]  

### <a name="improved-webassembly-debugging"></a>Débogage WebAssembly amélioré  

DevTools a commencé à prendre en charge la norme DE DÉBOGAGE EN COURS, ce qui signifie une prise en charge accrue du code pas à pas, de la définition de points d’arrêt et de la résolution des traces de pile dans vos langues sources dans DevTools.  

<!-- [TODO: Add this link back] -->  
<!--Check out [Improved WebAssembly debugging in Microsoft Edge DevTools][201912Webassembly] for the full story.  -->  

<!-- [TODO: Replace this image with screenshot in Edge] -->  
<!--
:::image type="complex" source="../../images/2019/12/wasm.msft.png" alt-text="The new DWARF-powered WebAssembly debugging" lightbox="../../images/2019/12/wasm.msft.png":::
   The new DWARF-powered WebAssembly debugging  
:::image-end:::  
-->  

### <a name="network-panel-updates"></a>Mises à jour du panneau réseau  

#### <a name="request-initiator-chains-in-the-initiator-panel"></a>Chaînes d’initiateur de demande dans le panneau Initiateur  

Vous pouvez désormais afficher les initiateurs et les dépendances d’une demande réseau en tant que liste imbriée.  Cela peut vous aider à comprendre pourquoi une ressource a été demandée ou l’activité réseau qu’une certaine ressource \(par exemple, un script\) a provoqué.  

:::image type="complex" source="../../images/2019/12/initiators.msft.png" alt-text="Chaîne de l’initiateur de la demande dans le panneau Initiateur" lightbox="../../images/2019/12/initiators.msft.png":::
   Chaîne de l’initiateur de la demande dans le **panneau Initiateur**  
:::image-end:::  

Après [avoir consigné l’activité][DevToolsNetworkIndex]réseau dans le **** panneau Réseau, choisissez une ressource, puis accédez au panneau Initiateur pour afficher la chaîne de **l’initiateur de demande**:  

*   La **ressource inspectée est** en gras.  Dans la capture d’écran `ai.2.min.js` ci-dessus, se trouve la ressource inspectée.  
*   Les ressources au-dessus de la ressource inspectée sont **les initiateurs.**  Dans la capture d’écran `https://www.microsoftedgeinsider.com` ci-dessus, est l’initiateur de `ai.2.min.js` .  En d’autres termes, `https://www.microsoftedgeinsider.com` a provoqué la demande réseau pour `ai.2.min.js` .  
*   Les ressources sous la ressource inspectée sont **les dépendances.**  Dans la capture d’écran `https://dc.services.visualstudio.com/v2/track` ci-dessus, est une dépendance de `ai.2.min.js` .  En d’autres termes, `ai.2.min.js` a provoqué la demande réseau pour `https://dc.services.visualstudio.com/v2/track` .  

> [!NOTE]
> Les informations d’initiateur et de dépendance peuvent également être accessibles en maintenant les ressources réseau en place, `Shift` puis en pointant dessus.  Accédez à [Afficher les initiateurs et les dépendances.][DevToolsNetworkReferenceDisplayInitiatorsDependencies]  

Chromium problème [#842488][CR842488]  

#### <a name="highlight-the-selected-network-request-in-the-overview"></a>Mettre en évidence la demande réseau sélectionnée dans la vue d’ensemble  

Une fois que vous avez choisi une ressource réseau pour l’inspecter, le panneau Réseau place maintenant une bordure bleue autour de cette ressource dans la vue **d’ensemble.**  Cela vous permet de détecter si la demande réseau se produit plus tôt ou plus tard que prévu.  

:::image type="complex" source="../../images/2019/12/overview.msft.png" alt-text="Volet Vue d’ensemble mettant en surbrillance la ressource inspectée" lightbox="../../images/2019/12/overview.msft.png":::
   Volet **Vue d’ensemble** mettant en surbrillance la ressource inspectée  
:::image-end:::  

Chromium problème [#988253][CR988253]  

#### <a name="url-and-path-columns-in-the-network-panel"></a>Colonnes d’URL et de chemin d’accès dans le panneau Réseau  

Utilisez les nouvelles **colonnes** **** Chemin d’accès et **URL** dans l’outil Réseau pour afficher le chemin d’accès absolu ou l’URL complète de chaque ressource réseau.  

:::image type="complex" source="../../images/2019/12/columns.msft.png" alt-text="Les nouvelles colonnes Chemin d’accès et URL dans le panneau Réseau" lightbox="../../images/2019/12/columns.msft.png":::
   Les nouvelles colonnes Chemin d’accès et URL dans **l’outil** Réseau  
:::image-end:::  

Pour afficher les nouvelles colonnes, pointez sur l’en-tête du tableau **Cascade,** ouvrez le menu contextuel \(righ-click\), puis choisissez **Chemin** d’accès ou **URL.**  

Chromium problème [#993366][CR993366]  

#### <a name="updated-user-agent-strings"></a>Mise à jour User-Agent chaînes  

DevTools prend en charge la définition d’une chaîne User-Agent personnalisée via le **panneau Conditions réseau.**  La User-Agent affecte l’en-tête HTTP attaché aux ressources réseau, ainsi que la `User-Agent` valeur de `navigator.userAgent` .  

Les chaînes de User-Agent prédéfines ont été mises à jour pour refléter les versions modernes du navigateur.  

:::image type="complex" source="../../images/2019/12/useragent.msft.png" alt-text="Menu Agent utilisateur dans le panneau Conditions réseau" lightbox="../../images/2019/12/useragent.msft.png":::
   Menu Agent utilisateur dans le **panneau Conditions réseau**  
:::image-end:::  

Pour accéder **aux conditions réseau,** [ouvrez le menu Commande][DevToolsCommandMenuIndex] et exécutez la `Show Network Conditions` commande.  

> [!NOTE]
> Vous pouvez également [définir des User-Agent en mode appareil.][DevToolsDeviceModeIndex]  

Chromium problème [#1029031][CR1029031]  

### <a name="audits-panel-updates"></a>Audits panel updates  

#### <a name="new-configuration-ui"></a>Nouvelle interface utilisateur de configuration  

L’interface utilisateur de configuration a une nouvelle conception réactive et les options de configuration de limitation ont été simplifiées.  Pour plus d’informations sur les modifications apportées à l’interface utilisateur de limitation, accédez à Limitation du panneau [Audits.][GitHubGoogleChromeDevToolsAuditsPanelThrottling]  

:::image type="complex" source="../../images/2019/12/start.msft.png" alt-text="Nouvelle interface utilisateur de configuration" lightbox="../../images/2019/12/start.msft.png":::
   Nouvelle interface utilisateur de configuration  
:::image-end:::  

### <a name="coverage-tool-updates"></a>Mises à jour de l’outil de couverture  

#### <a name="per-function-or-per-block-coverage-modes"></a>Modes de couverture par fonction ou par bloc  

[L’outil][DevToolsCoverageIndex] Couverture propose un nouveau menu déroulant qui vous permet de spécifier si les données de couverture de code doivent être collectées **par** fonction ou **par bloc.**  **La couverture** par bloc est plus détaillée, mais elle est également beaucoup plus coûteuse à collecter.  DevTools utilise désormais **la couverture par** fonction par défaut.  

> [!CAUTION]
> Vous remarquerez peut-être des différences importantes de couverture de code dans les fichiers HTML selon que vous utilisez **par** fonction ou **par** mode bloc.  Lors de **l’utilisation par** mode fonction, les scripts en ligne dans les fichiers HTML sont traités comme des fonctions.  Si le script s’exécute, DevTools marque l’intégralité du script en tant que code utilisé.  C’est seulement si le script ne s’exécute pas du tout que DevTools marque le script comme du code inutilisé.  

:::image type="complex" source="../../images/2019/12/modes.msft.png" alt-text="Menu déroulant du mode couverture" lightbox="../../images/2019/12/modes.msft.png":::
   Menu déroulant du mode couverture  
:::image-end:::  

#### <a name="coverage-must-now-be-initiated-by-a-page-refresh"></a>La couverture doit maintenant être lancée par une actualisation de page  

Le basculement de la couverture de code sans actualisation de page a été supprimé car les données de couverture n’étaient pas fiables.  Par exemple, une fonction peut être signalée comme inutilisée si le runtime date d’il y a longtemps et si le garbage collector V8 l’a nettoyé.  

Chromium problème [#1004203][CR1004203]  

## <a name="download-the-microsoft-edge-preview-channels"></a>Télécharger les canaux d’aperçu Microsoft Edge  

Si vous êtes sur Windows ou macOS, envisagez d’utiliser les canaux d Microsoft Edge [d’aperçu][MicrosoftEdgePreviewChannels] comme navigateur de développement par défaut.  Les canaux de prévisualisation vous donnent accès aux dernières fonctionnalités de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Contacter l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevToolsCommandMenuIndex]: ../../../command-menu/index.md "Exécuter des commandes avec le menu de commande DevTools de Microsoft Edge | Microsoft Docs"  
[DevToolsCoverageIndex]: ../../../coverage/index.md "Recherchez du code JavaScript et CSS inutilisé avec l’outil Couverture dans Microsoft Edge de | Documents Microsoft"  
[DevToolsDeviceModeIndex]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Simuler une port d’affichage mobile : simuler des appareils mobiles en mode Microsoft Edge devTools | Documents Microsoft"  
[DevToolsNetworkIndex]: ../../../network/index.md "Inspecter l’activité réseau dans Microsoft Edge devTools | Documents Microsoft"  
[DevToolsNetworkReferenceDisplayInitiatorsDependencies]: ../../../network/reference.md#display-initiators-and-dependencies "Afficher les initiateurs et les dépendances - Référence de l’analyse réseau | Documents Microsoft"  
[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Débogger pour les Microsoft Edge Visual Studio Code extension | Documents Microsoft"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Éléments pour les Microsoft Edge Visual Studio Code d’extension | Documents Microsoft"  

<!--  [201912Webassembly]: webassembly.md "Improved WebAssembly debugging in Microsoft Edge DevTools"  -->  

[CR842488]: https://crbug.com/842488 "Ajoutez le champ Initiateur à l’onglet En-têtes | Chromium Bogues"  
[CR988253]: https://crbug.com/988253 "Bug DevTools - Aucune association entre la demande réseau et la Graph | Chromium Bogues"  
[CR993366]: https://crbug.com/993366 "Veuillez afficher la partie du chemin d’accès de l’URL dans les listes de demandes du panneau réseau | Chromium Bogues"  
[CR1004193]: https://crbug.com/1004193 "Mode REPL pour les | V8 Chromium Bogues"  
[CR1004203]: https://crbug.com/1004203 "Faire en sorte que la couverture du code soit | Chromium Bogues"  
[CR1029031]: https://crbug.com/1029031 "Les chaînes UA sont obsolètes | Chromium Bogues" 
[CR963183]: https://crbug.com/963183 "Les devTools ne sont pas conformes AUX WCAG | Chromium Bogues"
[CR941561]: https://crbug.com/941561 "Localisabilité du | DevTools Chromium Bogues"
[CR987787]: https://crbug.com/987787 "Vue Dom 3D | Chromium Bogues"

[AccessibilityInsights]: https://aka.ms/a11yinsights "Informations sur l’accessibilité"  

[GitHubGoogleChromeDevToolsAuditsPanelThrottling]: https://github.com/GoogleChrome/lighthouse/blob/master/docs/throttling.md#devtools-audits-panel-throttling "Limitation du panneau Audits de DevTools - GoogleChrome/| GitHub"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nouveau problème : MicrosoftDocs/edge-developer"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Microsoft Edge Canaux d’aperçu"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Microsoft Edge Insider Addons"  
[MicrosoftVisualStudio]: https://aka.ms/vs "Visual Studio"  
[MicrosoftVisualStudioBlogDebugJavascript]: https://aka.ms/vs/debug-edge "Déboguer JavaScript dans Microsoft Edge à partir Visual Studio | Visual Studio Blog"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Télécharger Visual Studio 2019 pour Windows \& Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Modèle objet de document (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-index | MDN"  
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publier un Tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools compte Twitter"
[VisualStudioCode]: https://aka.ms/vscode "Visual Studio Code"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Débogger pour Microsoft Edge - Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Éléments pour Microsoft Edge \(Chromium\) - Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint - Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "webhint"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Webhint Browser Extension | documentation webhint"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Webhint Visual Studio Code extension | documentation webhint"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Amélioration de la prévention du suivi dans Microsoft Edge billet de blog"
[TheWebWeWant]: https://aka.ms/webwewant "Le site Web de votre choix"

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developer.chrome.com/blog/new-in-devtools-80) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
