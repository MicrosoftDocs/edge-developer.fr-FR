---
description: Émuler les défaillances de la vision des couleurs, ancrer à gauche dans le menu commande, et bien plus encore.
title: Nouveautés de DevTools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: c329dfba980b882b6e538447e52902e4d0cc985b
ms.sourcegitcommit: de75fda30bb8964e9a184228d068b4402ec59c3e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "11514416"
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
# <a name="whats-new-in-devtools-microsoft-edge-83"></a>Nouveautés de DevTools (Microsoft Edge 83)  

Après la mise à jour de la planification Chromium, nous ajustons notre planification pour les prochaines publication de Microsoft Edge et annulons la version Microsoft Edge 82. Consultez notre [billet de blog pour][WindowsBlogStableRelease] plus d'informations.  

Voici les nouvelles fonctionnalités disponibles dans DevTools dans Microsoft Edge 83.  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Annonces de l'équipe Microsoft Edge DevTools  

Les sections suivantes sont une liste des annonces que vous avez peut-être manquées de l'équipe Microsoft Edge DevTools.  Consultez les annonces pour essayer les nouvelles fonctionnalités des extensions DevTools, Microsoft Visual Studio Code, etc.  Pour rester à jour sur toutes les fonctionnalités les plus récentes et les plus importantes de vos outils de développement, téléchargez les canaux d'aperçu [Microsoft Edge][MicrosoftEdgePreviewChannels] et [suivez-nous sur Twitter.][EdgeDevToolsTwitterAccount]  

### <a name="remotely-debug-microsoft-edge-on-windows-10-devices"></a>Débogage à distance de Microsoft Edge sur les appareils Windows 10  

[L'application Outils à distance pour Microsoft Edge \(Bêta\)][RemoteTools] est désormais disponible dans le [Microsoft Store.][MicrosoftStore]  À l'aide de cette application, qui étend [Windows Device Portal,][WindowsUwpDebugTestPerfDevicePortal]vous pouvez vous connecter à partir de l'instance de Microsoft Edge en cours d'exécution sur votre ordinateur de développement à un appareil Windows 10 distant, afficher la liste des cibles \(tous les onglets de Microsoft Edge et [pwAs][ProgressiveWebAppsChromiumIndex] s'ouvrent sur l'appareil Windows 10\), et utiliser DevTools sur votre ordinateur de développement par rapport à une cible s'exécutant sur l'appareil Windows 10 distant.  

:::image type="complex" source="../../media/2020/03/remote-tools.msft.png" alt-text="Application Outils à distance pour Microsoft Edge (bêta) disponible dans le Microsoft Store" lightbox="../../media/2020/03/remote-tools.msft.png":::
   Application [Outils à distance pour Microsoft Edge (bêta)][RemoteTools] disponible dans le [Microsoft Store][MicrosoftStore]  
:::image-end:::  

Lisez notre guide pour la configuration de votre appareil Windows 10 et de votre ordinateur de [développement pour le débogage à distance.][DevtoolsRemoteDebuggingWindows]  Faites-nous part de votre expérience de débogage à distance en [tweetant][PostTweetEdgeDevTools] ou en déconant l'icône [Envoyer des](#getting-in-touch-with-microsoft-edge-devtools-team) commentaires !  

### <a name="new-ways-to-access-settings"></a>Nouvelles façons d'accéder aux paramètres  

Il existe des milliers de paramètres pour devTools que vous pouvez personnaliser pour donner à DevTools l'apparence, l'apparence et le travail dont vous avez besoin. Dans Microsoft Edge 83, l'accès aux [paramètres][DevtoolsCustomizeIndexSettings] dans DevTools est désormais beaucoup plus facile.  Ouvrez Paramètres avec l'icône d'engrenage en face des alertes de console et du menu principal.  

:::image type="complex" source="../../media/2020/03/settings.msft.png" alt-text="L'icône d'engrenage ouvre paramètres dans DevTools" lightbox="../../media/2020/03/settings.msft.png":::
   L'icône d'engrenage ouvre **paramètres** dans DevTools  
:::image-end:::  

Vous pouvez également ouvrir [Paramètres à][DevtoolsCustomizeIndexSettings] partir du **menu principal** sous **Plus d'outils.**

:::image type="complex" source="../../media/2020/03/settings2.msft.png" alt-text="Menu principal > plus d'outils > paramètres" lightbox="../../media/2020/03/settings2.msft.png":::
   **Menu principal**  >  **Autres outils**  >  **Paramètres**  
:::image-end:::  

Problème de chrome [#1050855][CR1050855]

### <a name="new-and-improved-infobars"></a>Barres d'informations nouvelles et améliorées

Les barres de notification d'information \(infobars\) dans DevTools ont désormais une apparence améliorée et des fonctionnalités supplémentaires. Dans Microsoft Edge 83, les barres d'informations sont plus faciles à lire et fournissent des boutons de sorte que vous pouvez immédiatement prendre l'action pertinente.  

:::image type="complex" source="../../media/2020/03/infobar.msft.png" alt-text="Barre d'informations pour l'impression d'un fichier minifié dans Microsoft Edge 83" lightbox="../../media/2020/03/infobar.msft.png":::
   Barre d'informations pour l'impression d'un fichier minifié dans Microsoft Edge Version 83  
:::image-end:::  

Problème de chrome [#1056348][CR1056348]

### <a name="navigate-the-color-picker-with-your-keyboard"></a>Naviguer dans le s sélectionneur de couleurs avec votre clavier  

Le [s picker de couleur][DevtoolsCssReferenceColorPicker] est une interface graphique graphique dans le panneau Éléments [pour][DevtoolsCssIndex] la modification et `color` les `background-color` déclarations.  Dans les versions précédentes de Microsoft Edge, vous n'étiez pas en mesure de naviguer dans la section **Nuances** du s [picker][DevtoolsCssReferenceColorPicker] de couleurs avec le clavier.  

:::image type="complex" source="../../media/2020/03/color-picker.msft.png" alt-text="Vous pouvez désormais utiliser votre clavier pour déplacer le sélecteur dans la section Nuances du sélecteur de couleurs" lightbox="../../media/2020/03/color-picker.msft.png":::
   Vous pouvez désormais utiliser votre clavier pour déplacer le sélecteur dans la section **Nuances** du [sélecteur de couleurs][DevtoolsCssReferenceColorPicker]  
:::image-end:::  

Dans Microsoft Edge 83, vous pouvez désormais utiliser le clavier pour déplacer le sélecteur dans la section **Nuances** du sélecteur de couleurs.  

Problème de chrome [#963183][CR963183]  

### <a name="properties-tab-now-populates-after-a-page-refresh"></a>L'onglet Propriétés se remplit maintenant après l'actualisation d'une page  

Dans Microsoft Edge 81 et **** les précédentes, l'onglet Propriétés du panneau [Éléments][DevtoolsCssIndex] a été rompu par des actualisations de page.  Lorsque vous avez actualisé la page, **l'onglet Propriétés** n'a pas rempli les propriétés de l'élément actuellement sélectionné.  

:::image type="complex" source="../../media/2020/03/properties-in-81.msft.png" alt-text="Dans Microsoft Edge 81 et les précédentes, l'onglet Propriétés était vide après l'actualisation d'une page" lightbox="../../media/2020/03/properties-in-81.msft.png":::
   Dans Microsoft Edge 81 et les précédentes, **l'onglet Propriétés** était vide après l'actualisation d'une page  
:::image-end:::  

Dans Microsoft Edge 83, vous pouvez désormais afficher les propriétés de l'élément actuellement sélectionné après une actualisation de page dans l'onglet **Propriétés.**  

:::image type="complex" source="../../media/2020/03/properties-in-82.msft.png" alt-text="Dans Microsoft Edge 83, l'onglet Propriétés affiche les propriétés de l'élément actuellement sélectionné après l'actualisation d'une page" lightbox="../../media/2020/03/properties-in-82.msft.png":::
   Dans Microsoft Edge 83, l'onglet Propriétés affiche les propriétés de l'élément actuellement sélectionné après l'actualisation d'une page ****  
:::image-end:::  

Problème de chrome [#1050999][CR1050999]  

### <a name="use-the-arrow-keys-to-scroll-in-the-changes-tool"></a>Utiliser les touches de direction pour faire défiler l'outil Modifications  

**L'outil Changes** suit toutes les modifications que vous avez apportées à CSS ou JavaScript dans DevTools.  Vous pouvez utiliser l'outil **Modifications** pour afficher rapidement toutes vos modifications et les remettre à votre éditeur/IDE.  

Pour ouvrir **l'outil Modifications,** sélectionnez `Ctrl` + `Shift` + `P` dans DevTools pour ouvrir le [menu commande][DevToolsCommandMenuIndex] et tapez `changes` .  choisissez et exécutez la **commande Afficher les modifications** pour ouvrir l'outil **Modifications** dans le caisse de DevTools.  

Lorsque vous avez apporté une modification à un fichier minifié, l'outil **Changes** vous permet de faire défiler horizontalement pour afficher l'ensemble de votre code minifié.  À partir de Microsoft Edge 83, vous pouvez désormais faire défiler horizontalement à l'aide des touches de direction de votre clavier.  

:::image type="complex" source="../../media/2020/03/changes.msft.png" alt-text="Dans Microsoft Edge 83, vous pouvez faire défiler horizontalement avec les touches de direction pour afficher votre code minifié dans l'outil Modifications" lightbox="../../media/2020/03/changes.msft.png":::
   Dans Microsoft Edge 83, vous pouvez faire défiler horizontalement avec les touches de direction pour afficher les modifications apportées à votre code minifié dans l'outil **Modifications.**  
:::image-end:::  

Si vous utilisez des lecteurs d'écran ou le clavier pour naviguer dans DevTools, envoyez-nous vos commentaires en nous faisant part de vos [commentaires][PostTweetEdgeDevTools] ou en criant l'icône Envoyer [des](#getting-in-touch-with-microsoft-edge-devtools-team) commentaires !  

Problème de chrome [#963183][CR963183]  

## <a name="announcements-from-the-chromium-project"></a>Annonces du projet de Chromium  

Les sections suivantes annoncent des fonctionnalités supplémentaires disponibles dans Microsoft Edge 83 qui ont été contribués au projet open source Chromium.  

### <a name="emulate-vision-deficiencies"></a>Émuler les faiblesses de la vision  

Ouvrez [l'onglet][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] Rendu et utilisez la nouvelle fonctionnalité Émuler les défauts de **vision** pour avoir une meilleure idée de la façon dont les personnes ayant différents types de problèmes de vision rencontrent votre site.  

:::image type="complex" source="../../media/2020/03/vision.msft.png" alt-text="Émulation d'une vision floue" lightbox="../../media/2020/03/vision.msft.png":::
   Émulation d'une vision floue  
:::image-end:::  

DevTools est en mesure d'émuler la vision floue et les types suivants de défauts [de vision de couleur.][ColorBlindnessTypes]  

| Problèmes de vision des couleurs | Détails |  
|:--- |:--- |  
| Protanopia | L'incapacité à percevoir toute lumière rouge. |  
| Deuteranopia | L'incapacité à percevoir toute lumière verte. |  
| Tritanopia | L'incapacité à percevoir la lumière bleue. |  
| Achromatopsia | L'incapacité à percevoir n'importe quelle couleur, à l'exception des nuances de gris \(extrêmement rares\). |  

Il existe des versions moins extrêmes de ces insuffisances de vision des couleurs et, en fait, elles sont plus courantes.  
Par exemple, le protanomaly est une sensibilité réduite à la lumière rouge (par opposition à la protanopie, qui est l'incapacité totale à percevoir la lumière rouge). Toutefois, ces défaillances visuelles **-omaly** ne sont pas aussi clairement définies : chaque personne atteinte d'une telle défaillance visuelle est différente et peut voir les choses différemment \(être en mesure de percevoir plus/moins les couleurs pertinentes\).  

En concevant des simulations plus extrêmes dans DevTools, vos applications web sont garanties d'être accessibles aux personnes avec protanomaly, deuteranomaly, tritanomaly et achromatomaly également.  

Envoyez vos commentaires en [tweetant][PostTweetEdgeDevTools] ou en cinglant [l'icône Envoyer des](#getting-in-touch-with-microsoft-edge-devtools-team) commentaires !  

Problème de chrome [#1003700][CR1003700]  

### <a name="emulate-locales"></a>Émuler les paramètres régionaux  

Émuler les paramètres régionaux en définir un emplacement dans **l'emplacement des**  >  **capteurs.** [Ouvrez le **menu Commande et** ][DevToolsCommandMenuIndex] tapez pour accéder à `Sensors` **l'onglet Capteurs.**  Après avoir effectué ces actions, DevTools modifie les paramètres régionaux par défaut actuels, ce qui affecte le code suivant.  

*   `Intl.*` LES API, par exemple : `new Intl.NumberFormat().resolvedOptions().locale`  
*   Autres API JavaScript sensibles aux paramètres régionaux telles `String.prototype.localeCompare` que `*.prototype.toLocaleString` et, par exemple : `123_456..toLocaleString()`  
*   API DOM telles que `navigator.language` et `navigator.languages`  
*   En-tête de requête HTTP [accept-Language][MDNAcceptLanguage]  

> [!NOTE]
> Mises à jour pour `navigator.language` et ne sont pas `navigator.languages` visibles immédiatement, mais uniquement après la navigation suivante ou l'actualisation de la page.  Les modifications apportées à `Accept-Language` l'en-tête HTTP ne sont reflétées que pour les demandes suivantes.  

:::image type="complex" source="../../media/2020/03/locale.msft.png" alt-text="Émulation d'un paramètres régionaux" lightbox="../../media/2020/03/locale.msft.png":::
   Émulation d'un paramètres régionaux  
:::image-end:::  

Pour essayer une démonstration, accédez à [l'exemple de code dépendant des paramètres régionaux.][MathiasByensLocaleDemo]

Problème de chrome [#1051822][CR1051822]

### <a name="cross-origin-embedder-policy-coep-debugging"></a>Débogage de la stratégie d'incorporation d'origine croisée (COEP)  

Le panneau Réseau fournit désormais [des informations de débogage][COEP] de stratégie d'incorporation d'origine croisée.  

La **colonne État** fournit désormais une explication rapide de la raison pour laquelle une demande a été bloquée, ainsi qu'un lien pour afficher les en-têtes de cette demande pour un débogage supplémentaire :  

:::image type="complex" source="../../media/2020/03/status.msft.png" alt-text="Demandes bloquées dans la colonne **État**" lightbox="../../media/2020/03/status.msft.png":::
   Demandes bloquées dans la **colonne État**  
:::image-end:::  

La section **En-têtes de** réponse de l'onglet **En-têtes** fournit davantage d'instructions sur la résolution des problèmes :  

:::image type="complex" source="../../media/2020/03/guidance.msft.png" alt-text="Plus d'instructions dans la section En-têtes de réponse" lightbox="../../media/2020/03/guidance.msft.png":::
   Plus d'instructions dans la section **En-têtes de** réponse  
:::image-end:::  

Envoyez vos commentaires en [tweetant][PostTweetEdgeDevTools] ou en cinglant [l'icône Envoyer des](#getting-in-touch-with-microsoft-edge-devtools-team) commentaires !  

Problème de chrome [#1051466][CR1051466]  

### <a name="new-icons-for-breakpoints-conditional-breakpoints-and-logpoints"></a>Nouvelles icônes pour les points d'arrêt, les points d'arrêt conditionnels et les points d'accès  

Le panneau Sources possède de nouvelles icônes pour les points d'arrêt, les points d'arrêt conditionnels et les points d'accès :  

*   Points d'arrêt \(![Point d'arrêt](../../media/2020/03/breakpoint.msft.png)\) sont représentés par des cercles rouges.  
*   Points d'arrêt conditionnels \(![Point d'arrêt conditionnel](../../media/2020/03/conditional.msft.png)\) sont représentés par des cercles demi-rouges demi-blancs.  
*   Logpoints \(![Logpoint](../../media/2020/03/logpoint.msft.png)\) sont représentés par des cercles rouges avec des icônes de console.  

La motivation des nouvelles icônes était de rendre l'interface utilisateur plus cohérente avec les autres outils de débogage de l'interface utilisateur graphique \(qui colorent généralement les points d'arrêt en rouge\) et de faciliter la distinction entre les 3 fonctionnalités en un coup d'œil.  

Problème de chrome [#1041830][CR1041830]  

### <a name="view-network-requests-that-set-a-specific-cookie-path"></a>Afficher les demandes réseau qui définissent un chemin d'accès de cookie spécifique  

Utilisez le nouveau mot clé de filtre dans l'outil Réseau pour vous concentrer sur les demandes réseau qui définissent `cookie-path` un chemin d'accès [de cookie spécifique.][MDNCookiePath] ****  

Consultez [filtrer les demandes par propriétés][DevtoolsNetworkReferenceFilterRequestsProperties] pour découvrir d'autres mots clés tels que `cookie-path` .

### <a name="dock-to-left-from-the-command-menu"></a>Ancrer à gauche à partir du menu Commande  

Ouvrez [le menu Commande][DevToolsCommandMenuIndex] et exécutez la commande pour déplacer `Dock to left` DevTools à gauche de votreport d'affichage.  

:::image type="complex" source="../../media/2020/03/dock-to-left.msft.png" alt-text="DevTools docked to the left of the viewport" lightbox="../../media/2020/03/dock-to-left.msft.png":::
   DevTools docked to the left of the viewport  
:::image-end:::  

> [!NOTE]
> La fonctionnalité Station **d'accueil** vers la gauche est disponible depuis Microsoft Edge 75, mais elle était auparavant accessible uniquement à partir du [menu principal.][DevtoolsCustomizePlacementsChangeMainMenu]  La nouvelle fonctionnalité de Microsoft Edge 83 est que vous pouvez désormais accéder à cette fonctionnalité à partir du menu Commande.  

Envoyez vos commentaires en [tweetant][PostTweetEdgeDevTools] ou en cinglant [l'icône Envoyer des](#getting-in-touch-with-microsoft-edge-devtools-team) commentaires !  

Problème de chrome [#1011679][CR1011679]  

### <a name="the-audits-panel-is-now-the-lighthouse-panel"></a>Le panneau Audits est désormais le panneau Panneau de sélection  

L'équipe DevTools a fréquemment reçu des commentaires des développeurs web qui ont dit que même s'il était possible d'exécuter [Lasser][GithubGoogleChromeLighthouse] à partir de DevTools, lorsqu'ils l'ont essayé, ils n'ont pas pu trouver le panneau « Course », de sorte que le panneau **Audits** est désormais le panneau DevTools. ****  

:::image type="complex" source="../../media/2020/03/lighthouse.msft.png" alt-text="Panneau de sélection" lightbox="../../media/2020/03/lighthouse.msft.png":::
   Panneau de sélection  
:::image-end:::  

> [!NOTE]
> Le **panneau Panneau de** panneau fournit des liens vers du contenu hébergé sur des sites web tiers.  Microsoft n'est pas responsable et n'a aucun contrôle sur le contenu de ces sites et les données qu'ils peuvent collecter.  

### <a name="delete-all-local-overrides-in-a-folder"></a>Supprimer toutes les substitutions locales dans un dossier  

Après avoir mis en place les **substitutions locales,** vous pouvez pointer sur un répertoire, ouvrir le menu contextuel \(clic droit\) et choisir la nouvelle option Supprimer toutes les substitutions pour supprimer toutes les **substitutions** locales dans ce dossier.  

:::image type="complex" source="../../media/2020/03/overrides.msft.png" alt-text="Supprimer toutes les substitutions" lightbox="../../media/2020/03/overrides.msft.png":::
   Supprimer toutes les substitutions  
:::image-end:::  

Envoyez vos commentaires en [tweetant][PostTweetEdgeDevTools] ou en cinglant [l'icône Envoyer des](#getting-in-touch-with-microsoft-edge-devtools-team) commentaires !  

Problème de chrome [#1016501][CR1016501]  

### <a name="updated-long-tasks-ui"></a>Interface utilisateur des tâches longues mise à jour  

Une **tâche longue** est du code JavaScript qui a pour effet de bloquer le thread principal pendant une longue période, ce qui entraîne le blocage d'une page web.  

Vous pouvez visualiser [][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] les tâches longues dans le panneau Performances depuis un certain temps, mais dans Microsoft Edge 83, l'interface utilisateur de visualisation des tâches longues dans le panneau Performances a été mise à jour.  La partie Tâche longue d'une tâche est maintenant colorée avec un arrière-plan rouge à bandes.  

:::image type="complex" source="../../media/2020/03/long-task.msft.png" alt-text="Nouvelle interface utilisateur de tâche longue" lightbox="../../media/2020/03/long-task.msft.png":::
   Nouvelle interface utilisateur de tâche longue  
:::image-end:::  

Envoyez vos commentaires en [tweetant][PostTweetEdgeDevTools] ou en cinglant [l'icône Envoyer des](#getting-in-touch-with-microsoft-edge-devtools-team) commentaires !  

Problème de chrome [#1054447][CR1054447]  

### <a name="maskable-icon-support-in-the-manifest-pane"></a>Prise en charge des icônes masquées dans le volet manifeste  

Android Oreo a introduit des icônes adaptatives, qui affichent les icônes d'application sous différentes formes sur différents modèles d'appareil.  **Les icônes masquées** sont un nouveau format d'icône qui permet de prendre en charge les icônes adaptatives, ce qui vous permet de vous assurer que votre icône [PWA][ProgressiveWebAppsChromiumIndex] s'adapte bien sur les appareils qui assurent la prise en charge de la norme des icônes masquées.  

Activez la nouvelle case à cocher Afficher uniquement **** la zone sécurisée minimale pour les **icônes** masquées dans le volet manifeste pour vérifier que votre icône masquée s'affiche bien sur les appareils Android Oreo.  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

:::image type="complex" source="../../media/2020/03/maskable-icons.msft.png" alt-text="Afficher uniquement la zone sécurisée minimale pour la case à cocher des icônes masquées" lightbox="../../media/2020/03/maskable-icons.msft.png":::
   La case à cocher Afficher uniquement **la zone sécurisée minimale pour les icônes masquées**  
:::image-end:::  

> [!NOTE]
> Cette fonctionnalité a été lancée dans Microsoft Edge 81.  Les mises à jour couvertes ici dans Microsoft Edge 83 n'ont pas été couvertes dans [Nouveautés de DevTools (Microsoft Edge 81).][WhatsNew81]  

## <a name="download-the-microsoft-edge-preview-channels"></a>Télécharger les canaux d’aperçu Microsoft Edge  

Si vous utilisez Windows ou macOS, envisagez d'utiliser les canaux d'aperçu [Microsoft Edge][MicrosoftEdgePreviewChannels] comme navigateur de développement par défaut.  Les canaux de prévisualisation vous donnent accès aux dernières fonctionnalités de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Contacter l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[WhatsNew81]: ../01/devtools.md "Nouveautés de DevTools (Microsoft Edge 81) | Documents Microsoft"  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Exécuter des commandes avec le menu de commandes Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Modifier les couleurs à l'| Documents Microsoft"  
[DevtoolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Mise en place de l'affichage et de la modification des | Documents Microsoft"  
[DevtoolsCustomizePlacementsChangeMainMenu]: /microsoft-edge/devtools-guide-chromium/customize/placement#change-placement-from-the-main-menu "Modifier l'emplacement à partir du menu | Documents Microsoft"  
[DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#view-main-thread-activity "Afficher l'activité du thread principal | Documents Microsoft"  
[DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analyser les performances de rendu à l'| Documents Microsoft"  
[ProgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Applications web progressives sur Windows | Documents Microsoft"  
[DevtoolsRemoteDebuggingWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Mise en place du débogage à distance des appareils Windows 10 | Documents Microsoft"  
[DevtoolsJavascriptBreakpointsLineCode]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Points d'arrêt de ligne de code : comment suspendre votre code avec des points d'arrêt dans Microsoft Edge DevTools | Documents Microsoft"
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Filtrer les demandes par propriétés – Référence de l'analyse réseau | Documents Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Paramètres : personnaliser les paramètres DevTools de Microsoft Edge | Documents Microsoft"  

[WindowsUwpDebugTestPerfDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Vue d'ensemble de Windows Device Portal"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Outils à distance pour Microsoft Edge (bêta)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux de préversion de Microsoft Edge"  

[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20 "Mise à jour sur les canaux stables pour Microsoft Edge"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Nouveau problème - MicrosoftDocs/Edge-développeur-GitHub"  

[MicrosoftVisualstudio]: https://visualstudio.microsoft.com "Visual Studio"  

[VisualstudioCode]: https://code.visualstudio.com "Code Visual Studio"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publier un Tweet"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools Twitter"  
[TheWebWeWant]: https://webwewant.fyi "Le site Web de votre choix"  

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness "Types de daltonisme"  

[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Accept-Language | MDN"  
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives "Set-Cookie | MDN"  

[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Exemple de code dépendant des paramètres régionaux"  

[CR963183]: https://crbug.com/963183 "Problème 963183 : Les devTools ne sont pas conformes WCAG"  
[CR1003700]: https://crbug.com/1003700 "Problème 1003700 : ajout de la prise en charge de DevTools pour la simulation de problèmes de vision des couleurs"  
[CR1011679]: https://crbug.com/1011679 "Problème 1011679 : introduire « Ancrer à gauche » à l'aide du menu Commande"  
[CR1016501]: https://crbug.com/1016501 "Problème 1016501 : Demande de fonctionnalité : bouton pour supprimer toutes les substitutions locales"  
[CR1050999]: https://crbug.com/1050999 "Problème 1050999 : onglet Propriétés"  
[CR1051466]: https://crbug.com/1051466 "Problème 1051466 : prise en charge du débogage BIP/COEP dans DevTools"  
[CR1054447]: https://crbug.com/1054447 "Problème 1054447 : mettre à jour les mesures de performances dans la chronologie DevTools"  
[CR1051822]: https://crbug.com/1051822 "Problème 1051822 : DevTools : ajouter une interface utilisateur pour émuler les paramètres régionaux"
[CR1041830]: https://crbug.com/1041830 "Problème 1041830 : Améliorer les couleurs des points d'arrêt"
[CR1050855]: https://crbug.com/1050855 "Problème 1050855 : l'affichage Paramètres est difficile à découvrir"
[CR1056348]: https://crbug.com/1056348 "Problème 1056348 : Actualisation des composants de la barre d'informations"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "EXPLICATION ET COEP - Stratégie d'ouverture d'origine croisée"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 "EXPLICATION ET COEP - Stratégie d'incorporation d'origine croisée"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "| GitHub"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developer.chrome.com/blog/new-in-devtools-83) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
