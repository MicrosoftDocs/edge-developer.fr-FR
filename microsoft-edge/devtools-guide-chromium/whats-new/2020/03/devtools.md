---
description: Déboguez à distance Microsoft Edge sur les appareils Windows 10, de nouvelles méthodes d’accès aux paramètres, etc.
title: Nouveautés de DevTools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 94b8d067738a1749f136edf2a562652bece183a9
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993428"
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

# Nouveautés de DevTools (Microsoft Edge 83)  

Suite à la mise à jour de la planification de chrome, nous devons nous ajuster notre planning pour les versions à venir de Microsoft Edge et en annulant la version 82 de Microsoft Edge. Pour plus d’informations, consultez le [billet de blog][WindowsBlogStableRelease] .  

Voici les nouvelles fonctionnalités disponibles dans le DevTools de Microsoft Edge 83.  

## Annonces de l’équipe Microsoft Edge DevTools  

Les sections suivantes répertorient les annonces que vous pouvez avoir manquées de l’équipe Microsoft Edge DevTools. Découvrez-les pour essayer de nouvelles fonctionnalités dans les extensions de code DevTools, VS, etc.  Pour vous tenir au courant de toutes les fonctionnalités les plus récentes et les plus récentes de vos outils de développement, téléchargez les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] et [Suivez-nous sur Twitter][EdgeDevToolsTwitterAccount].  

### Déboguer à distance Microsoft Edge sur les appareils Windows 10  

L’application [outils de contrôle à distance pour Microsoft Edge \ (Beta)][RemoteTools] est désormais disponible dans le [Microsoft Store][MicrosoftStore].  À l’aide de cette application, qui étend [Windows Device Portal][WindowsUwpDebugTestPerfDevicePortal], vous pouvez vous connecter à partir de l’instance de Microsoft Edge qui s’exécute sur votre ordinateur de développement sur un appareil Windows 10 distant, afficher une liste des cibles \ (tous les onglets dans Microsoft Edge et [PWAS][PprgressiveWebAppsChromiumIndex] s’ouvrent sur l’appareil Windows 10) et utiliser devtools sur votre ordinateur de développement sur une cible qui s’exécute sur  

:::image type="complex" source="../../media/2020/03/remote-tools.msft.png" alt-text="Application outils de contrôle à distance pour Microsoft Edge (Beta) disponible dans le Microsoft Store" lightbox="../../media/2020/03/remote-tools.msft.png":::
   Figure 1: application [outils de contrôle à distance pour Microsoft Edge (Beta)][RemoteTools] disponible dans le [Microsoft Store][MicrosoftStore]  
:::image-end:::  

[Consultez notre guide de configuration de votre appareil Windows 10 et de votre ordinateur de développement pour le débogage à distance][DevtoolsRemoteDebuggingWindows].  Donnez-nous votre avis concernant le débogage à distance par le biais de [Tweet][PostTweetEdgeDevTools] ou en cliquant sur l’icône d' [envoi de commentaires](#getting-in-touch-with-microsoft-edge-devtools-team) .  

### Nouvelles méthodes d’accès aux paramètres  

Il existe de nombreux paramètres pour le DevTools que vous pouvez personnaliser pour améliorer l’aspect et l’apparence de DevTools, ainsi que les tâches dont vous avez besoin. Dans Microsoft Edge 83, il est désormais plus facile d’accéder aux [paramètres][DevtoolsCustomizeIndexSettings] dans le devtools. Ouvrez les paramètres à l’aide de l’icône d’engrenage en regard des alertes de console et du menu principal.  

:::image type="complex" source="../../media/2020/03/settings.msft.png" alt-text="L’icône d’engrenage s’ouvre pour afficher les paramètres dans le DevTools" lightbox="../../media/2020/03/settings.msft.png":::
   Figure 2: l’icône d’engrenage s’ouvre pour afficher les **paramètres** dans le devtools  
:::image-end:::  

Vous pouvez également ouvrir les [paramètres][DevtoolsCustomizeIndexSettings] à partir du **menu principal** sous **autres outils**.

:::image type="complex" source="../../media/2020/03/settings2.msft.png" alt-text="Menu principal > plus d’outils > paramètres" lightbox="../../media/2020/03/settings2.msft.png":::
   Figure 3: **menu principal**  >  **plus**  >  **paramètres** d’outils  
:::image-end:::  

[#1050855][CR1050855] problème de chrome

### Infobars nouveau et amélioré

Les barres de notification d’information \ (infobars \) dans DevTools présentent désormais une meilleure interface et de nouvelles fonctionnalités. Dans Microsoft Edge 83, infobars est plus facile à lire et à proposer des boutons pour vous permettre d’effectuer l’action appropriée immédiatement.  

:::image type="complex" source="../../media/2020/03/infobar.msft.png" alt-text="Barre d’informations pour l’impression d’un fichier minified dans Microsoft Edge 83" lightbox="../../media/2020/03/infobar.msft.png":::
   Figure 4: barre d’informations pour l’impression d’un fichier minified dans Microsoft Edge version 83  
:::image-end:::  

[#1056348][CR1056348] problème de chrome

### Parcourir le sélecteur de couleurs à l’aide du clavier  

Le [Sélecteur de couleurs][DevtoolsCssReferenceColorPicker] est une interface utilisateur du [panneau éléments][DevtoolsCssIndex] permettant de changer et de faire des `color` `background-color` déclarations.  Dans les versions précédentes de Microsoft Edge, vous ne parvenez pas à naviguer dans la section **nuances** du [Sélecteur de couleur][DevtoolsCssReferenceColorPicker] à l’aide du clavier.  

:::image type="complex" source="../../media/2020/03/color-picker.msft.png" alt-text="Vous pouvez maintenant utiliser votre clavier pour déplacer le sélecteur dans la section nuances du sélecteur de couleurs." lightbox="../../media/2020/03/color-picker.msft.png":::
   Figure 5: vous pouvez maintenant utiliser votre clavier pour déplacer le sélecteur dans la section **tons** du [Sélecteur de couleurs][DevtoolsCssReferenceColorPicker]  
:::image-end:::  

Dans Microsoft Edge 83, vous pouvez maintenant utiliser le clavier pour déplacer le sélecteur dans la section **tons** du sélecteur de couleurs.  

[#963183][CR963183] problème de chrome  

### L’onglet Propriétés est désormais rempli après une actualisation de page  

Dans Microsoft Edge 81 et les versions antérieures, l' **onglet Propriétés** dans le [panneau éléments][DevtoolsCssIndex] a été rompu par l’actualisation de la page.  Lorsque vous actualisez la page, l' **onglet Propriétés** ne remplissait pas les propriétés de l’élément actuellement sélectionné.  

:::image type="complex" source="../../media/2020/03/properties-in-81.msft.png" alt-text="Dans Microsoft Edge 81 et versions antérieures, l’onglet Propriétés était vide après une actualisation de page" lightbox="../../media/2020/03/properties-in-81.msft.png":::
   Figure 6: image de l' **onglet Propriétés** dans Microsoft Edge 81 et versions antérieures  
:::image-end:::  

Dans Microsoft Edge 83, vous pouvez désormais voir les propriétés de l’élément actuellement sélectionné après une actualisation de page dans l' **onglet Propriétés**.  

:::image type="complex" source="../../media/2020/03/properties-in-82.msft.png" alt-text="Dans Microsoft Edge 83, l’onglet Propriétés affiche les propriétés de l’élément actuellement sélectionné après une actualisation de la page" lightbox="../../media/2020/03/properties-in-82.msft.png":::
   Figure 7: dans le 83 Microsoft Edge, l' **onglet Propriétés** affiche les propriétés de l’élément actuellement sélectionné après une actualisation de la page  
:::image-end:::  

[#1050999][CR1050999] problème de chrome  

### Utiliser les touches de direction pour faire défiler l’outil modifications  

L' **outil modifications** effectue le suivi des modifications que vous avez apportées à CSS ou JavaScript dans le devtools.  Vous pouvez utiliser l' **outil modifications** pour afficher rapidement toutes vos modifications et revenir à votre éditeur/IDE.  

Ouvrez l' **outil modifications** en appuyant sur `Ctrl` + `Shift` + `P` la devtools pour ouvrir le [menu de commandes][DevToolsCommandMenuIndex] et en tapant `changes` .  Activez et exécutez la commande **afficher les modifications** pour ouvrir l' **outil modifications** dans le tiroir devtools.  

Lorsque vous avez apporté une modification à un fichier minified, l' **outil modifications** vous permet de faire défiler horizontalement pour afficher l’ensemble de votre code minified.  À partir de Microsoft Edge 83, vous pouvez à présent faire défiler les touches de direction de votre clavier.  

:::image type="complex" source="../../media/2020/03/changes.msft.png" alt-text="Dans Microsoft Edge 83, vous pouvez faire défiler horizontalement avec les touches de direction pour afficher votre code minified dans l’outil modifications." lightbox="../../media/2020/03/changes.msft.png":::
   Figure 8: dans Microsoft Edge 83, vous pouvez faire défiler horizontalement avec les touches de direction pour voir les modifications que vous avez apportées à votre code minified dans l' **outil modifications** .  
:::image-end:::  

Si vous utilisez un lecteur d’écran ou le clavier pour naviguer dans DevTools, envoyez-nous vos commentaires en nous appuyant sur un [Tweet][PostTweetEdgeDevTools] ou en cliquant sur l’icône d' [envoi de commentaires](#getting-in-touch-with-microsoft-edge-devtools-team) .  

[#963183][CR963183] problème de chrome  

## Annonces du projet de chrome  

Les sections suivantes annoncent des fonctionnalités supplémentaires disponibles dans Microsoft Edge 83 qui ont été fournies au projet de chrome Open source.  

### Émuler les déficiences de la vision  

Ouvrez l' [onglet rendu][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] , puis utilisez la nouvelle fonctionnalité **émuler les déficiences** de la vision pour mieux comprendre comment les personnes présentant différents types d’déficiences de la vision connaissent votre site.  

:::image type="complex" source="../../media/2020/03/vision.msft.png" alt-text="Émulation d’une vision floue" lightbox="../../media/2020/03/vision.msft.png":::
   Figure 9: émulation d’une vision floue  
:::image-end:::  

DevTools est en mesure d’émuler une vision floue et des [types de troubles de la vision couleur][ColorBlindnessTypes]suivants.  

| Déficience de la vision couleur | Détails |  
|:--- |:--- |  
| Protanopia | L’impossibilité de percevoir des lumières rouges. |  
| Deuteranopia | L’impossibilité de percevoir une lumière verte. |  
| Tritanopia | L’impossibilité de percevoir une lumière bleue. |  
| Achromatopsia | L’impossibilité de percevoir une couleur, à l’exception des nuances de gris. |  

Il existe des versions moins extrêmes de ces déficiences de vision couleur, et en fait, elles sont plus courantes.  
Par exemple, protanomaly est une sensibilité réduite de l’éclairage rouge (par opposition à protanopia, qui est la possibilité d’obtenir une lumière rouge). Toutefois, ces déficiences en matière de vision omaly n’ont pas été aussi clairement définies: chaque personne ayant une déficience de la vision est différente et peut voir ce qui se passe d’un point de vue différent (il est en mesure de percevoir plus ou moins des couleurs pertinentes).  

En concevant des simulations plus extrêmes dans DevTools, il est garanti que les applications Web sont accessibles aux personnes utilisant protanomaly, Deuteranomaly, tritanomaly et achromatomaly.  

Envoyez vos commentaires en utilisant un [tweetation][PostTweetEdgeDevTools] ou en cliquant sur l’icône d' [envoi de commentaires](#getting-in-touch-with-microsoft-edge-devtools-team) .  

[#1003700][CR1003700] problème de chrome  

### Émuler des paramètres régionaux  

Émulez des paramètres régionaux en définissant un **Sensors**emplacement dans la  >  **zone**capteurs. [Ouvrez le **menu de commandes** ][DevToolsCommandMenuIndex] et tapez `Sensors` pour accéder à l’onglet **capteurs** .  Après avoir effectué ces actions, DevTools modifie les paramètres régionaux par défaut actuels en affectant le code suivant.  

*   `Intl.*` Par exemple: `new Intl.NumberFormat().resolvedOptions().locale`  
*   Autres API JavaScript prenant en charge des paramètres régionaux tels que `String.prototype.localeCompare` et `*.prototype.toLocaleString` , par exemple: `123_456..toLocaleString()`  
*   API DOM telles que `navigator.language` et `navigator.languages`  
*   [`Accept-Language`][MDNAcceptLanguage]En-tête de requête http  

> [!NOTE]
> Les mises à jour de `navigator.language` et ne `navigator.languages` sont pas visibles immédiatement, mais uniquement après la prochaine navigation ou actualisation de page.  Les modifications apportées à l' `Accept-Language` en-tête http sont uniquement répercutées pour les demandes suivantes.  

:::image type="complex" source="../../media/2020/03/locale.msft.png" alt-text="Émulation d’un paramètre régional" lightbox="../../media/2020/03/locale.msft.png":::
   Figure 10: émulation d’un paramètre régional  
:::image-end:::  

Pour essayer une démonstration, voir [exemple de code dépendant des paramètres régionaux][MathiasByensLocaleDemo].

[#1051822][CR1051822] problème de chrome

### Débogage de la stratégie d’intégration COEP (Cross-Origin)  

Le panneau réseau fournit désormais des informations de débogage de la [stratégie d’incorporation][COEP] à l’origine.  

La colonne **État** donne désormais une explication rapide de la raison pour laquelle une requête a été bloquée ainsi qu’un lien pour afficher les en-têtes de cette requête pour un débogage supplémentaire:  

:::image type="complex" source="../../media/2020/03/status.msft.png" alt-text="Demandes bloquées dans la colonne * * Status * *" lightbox="../../media/2020/03/status.msft.png":::
   Figure 11: demandes bloquées dans la colonne État  
:::image-end:::  

La section **en-têtes de réponse** de l’onglet **en-têtes** fournit davantage d’instructions pour résoudre les problèmes:  

:::image type="complex" source="../../media/2020/03/guidance.msft.png" alt-text="Conseils supplémentaires dans la section en-têtes de réponse" lightbox="../../media/2020/03/guidance.msft.png":::
   Figure 12: conseils supplémentaires dans la section en-têtes de réponse  
:::image-end:::  

Envoyez vos commentaires en utilisant un [tweetation][PostTweetEdgeDevTools] ou en cliquant sur l’icône d' [envoi de commentaires](#getting-in-touch-with-microsoft-edge-devtools-team) .  

[#1051466][CR1051466] problème de chrome  

### Nouvelles icônes pour les points d’arrêt, les points d’arrêt conditionnel et la logpoints  

Le panneau sources comporte de nouvelles icônes pour les points d’arrêt, les points d’arrêt conditionnel et logpoints:  

*   Points d’arrêt \ (![Interruption](../../media/2020/03/breakpoint.msft.png)\) sont représentés par des cercles rouges.  
*   Points d’arrêt conditionnels![Point d’arrêt conditionnel](../../media/2020/03/conditional.msft.png)\) sont représentés par des cercles demi-rouges.  
*   Logpoints \(![Logpoint](../../media/2020/03/logpoint.msft.png)\) sont représentés par des cercles rouges grâce aux icônes de la console.  

La motivation des nouvelles icônes fut de rendre l’interface utilisateur plus cohérente avec les autres outils de débogage de l’interface utilisateur (qui sont généralement des points d’arrêt de couleur rouges \) et de faciliter la distinction entre les trois fonctionnalités en un clin d’œil.  

[#1041830][CR1041830] problème de chrome  

### Afficher les requêtes réseau qui définissent un chemin de cookie spécifique  

Utilisez le nouveau `cookie-path` mot clé de filtre dans le panneau **réseau** pour vous concentrer sur les requêtes réseau qui définissent un [chemin de cookie][MDNCookiePath]spécifique.  

Consultez les [demandes de filtre par propriétés][DevtoolsNetworkReferenceFilterRequestsProperties] pour découvrir d’autres mots clés comme `cookie-path` .

### Ancrer à gauche à partir du menu de commandes  

Ouvrez le [menu de commandes][DevToolsCommandMenuIndex] et exécutez la `Dock to left` commande pour déplacer devtools à gauche de votre fenêtre d’affichage.  

:::image type="complex" source="../../media/2020/03/dock-to-left.msft.png" alt-text="DevTools ancré à gauche de la fenêtre d’affichage" lightbox="../../media/2020/03/dock-to-left.msft.png":::
   Figure 13: DevTools fixé à gauche de la fenêtre d’affichage  
:::image-end:::  

> [!NOTE]
> La fonctionnalité **ancrer à gauche** est disponible depuis Microsoft Edge 75, mais elle n’est auparavant accessible qu’à partir du [**menu principal**][DevtoolsCustomizePlacementsChangeMainMenu].  La nouvelle fonctionnalité de Microsoft Edge 83 est que vous pouvez maintenant accéder à cette fonctionnalité à partir du menu de commandes.  

Envoyez vos commentaires en utilisant un [tweetation][PostTweetEdgeDevTools] ou en cliquant sur l’icône d' [envoi de commentaires](#getting-in-touch-with-microsoft-edge-devtools-team) .  

[#1011679][CR1011679] problème de chrome  

### Le panneau d’audit est désormais le panneau de signalisation.  

L’équipe DevTools a fréquemment reçu des commentaires de la part des développeurs Web, alors qu’il était possible d’exécuter un [phare][GithubGoogleChromeLighthouse] à partir de devtools, **lorsque l’utilisateur** a essayé le panneau de configuration, il n’a pas été en mesure de trouver le panneau de **signalisation.**  

:::image type="complex" source="../../media/2020/03/lighthouse.msft.png" alt-text="Panneau de signalisation" lightbox="../../media/2020/03/lighthouse.msft.png":::
   Figure 14: panneau de signalisation  
:::image-end:::  

> [!NOTE]
> Le panneau de **signalisation** comporte des liens vers du contenu hébergé sur des sites Web tiers.  Microsoft n’est pas responsable et n’a aucun contrôle sur le contenu de ces sites et sur les données qu’ils peuvent recueillir.  

### Supprimer tous les remplacements locaux dans un dossier  

Après avoir configuré les **remplacements locaux** , vous pouvez cliquer avec le bouton droit sur un dossier et sélectionner l’option **supprimer toutes les substitutions** dans ce dossier.  

:::image type="complex" source="../../media/2020/03/overrides.msft.png" alt-text="Supprimer tous les remplacements" lightbox="../../media/2020/03/overrides.msft.png":::
   Figure 15: supprimer tous les remplacements  
:::image-end:::  

Envoyez vos commentaires en utilisant un [tweetation][PostTweetEdgeDevTools] ou en cliquant sur l’icône d' [envoi de commentaires](#getting-in-touch-with-microsoft-edge-devtools-team) .  

[#1016501][CR1016501] problème de chrome  

### Interface utilisateur de tâches longues mise à jour  

Une **tâche longue** correspond à du code JavaScript qui monopolit le thread principal pendant un certain temps, provoquant le gel d’une page Web.  

Vous avez la possibilité de [visualiser de longs tâches dans le panneau de performance][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] pour un certain temps, mais dans Microsoft Edge 83, l’interface utilisateur d’une visualisation de tâches longues du panneau de performance a été mise à jour.  La partie tâches longues d’une tâche est désormais colorée avec un arrière-plan rouge rayé.  

:::image type="complex" source="../../media/2020/03/long-task.msft.png" alt-text="Nouvelle interface utilisateur de tâche longue" lightbox="../../media/2020/03/long-task.msft.png":::
   Figure 16: interface utilisateur de nouvelle tâche longue  
:::image-end:::  

Envoyez vos commentaires en utilisant un [tweetation][PostTweetEdgeDevTools] ou en cliquant sur l’icône d' [envoi de commentaires](#getting-in-touch-with-microsoft-edge-devtools-team) .  

[#1054447][CR1054447] problème de chrome  

### Icône masquable dans le volet manifeste  

Android Oreo introduit des icônes adaptatives qui affichent des icônes d’application dans différentes formes sur différents modèles d’appareil.  Les icônes qui peuvent être **masquées** sont un nouveau format d’icône qui prend en charge les icônes adaptatives, qui vous permettent de vous assurer que votre icône [PWA][PprgressiveWebAppsChromiumIndex] fonctionne correctement sur les appareils qui prennent en charge la norme d’icônes masquées.  

Activez la case à cocher nouveau **afficher uniquement la zone sécurisée minimum pour les icônes masquées** dans le volet **manifeste** pour vérifier que votre icône MASKABLE fonctionne correctement sur les appareils Android Oreo.  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

:::image type="complex" source="../../media/2020/03/maskable-icons.msft.png" alt-text="Case à cocher Afficher uniquement la zone sécurisée minimum pour les icônes masquées" lightbox="../../media/2020/03/maskable-icons.msft.png":::
   Figure 17: activez la case à cocher **afficher uniquement la zone sécurisée minimum pour les icônes masquées** .  
:::image-end:::  

> [!NOTE]
> Cette fonctionnalité est lancée dans Microsoft Edge 81.  Les mises à jour abordées ici dans Microsoft Edge 83 n’ont pas été abordées dans [les nouveautés de devtools (Microsoft edge 81)][WhatsNew81].  

## Télécharger les canaux Microsoft Edge preview  

Si vous utilisez Windows ou macOS, envisagez d’utiliser les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] comme navigateur par défaut.  Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.  

## Contacter l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publiez un tweet"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools compte Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Nouveau problème-MicrosoftDocs/Edge-développeur-GitHub"  
[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux Microsoft Edge preview"  
[TheWebWeWant]: https://webwewant.fyi "Le site Web de votre choix"  

[WhatsNew81]: ../01/devtools.md "Nouveautés de DevTools (Microsoft Edge 81) | Documents Microsoft"  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Exécuter des commandes à l’aide du menu de commandes de Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Changer les couleurs avec le sélecteur de couleurs | Documents Microsoft"  
[DevtoolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Découvrir comment afficher et modifier des feuilles CSS | Documents Microsoft"  
[DevtoolsCustomizePlacementsChangeMainMenu]: /microsoft-edge/devtools-guide-chromium/customize/placement#change-placement-from-the-main-menu "Changer le positionnement dans le menu principal | Documents Microsoft"  
[DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#view-main-thread-activity "Afficher l’activité du thread principal | Documents Microsoft"  
[DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analyser les performances de rendu à l’aide de l’onglet rendu | Documents Microsoft"  
[PprgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Applications Web progressives sur Windows | Documents Microsoft"  
[DevtoolsRemoteDebuggingWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Commencer à utiliser le débogage à distance des appareils Windows 10 | Documents Microsoft"  
[DevtoolsJavascriptBreakpointsLineCode]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Points d’arrêt de la ligne de code: comment mettre en pause votre code avec des points d’arrêt dans Microsoft Edge DevTools | Documents Microsoft"
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Demandes de filtre par propriétés-référence d’analyse du réseau | Documents Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"  

[WindowsUwpDebugTestPerfDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Vue d’ensemble de Windows Device Portal"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Outils de contrôle à distance pour Microsoft Edge (bêta)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  

[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20 "Mise à jour sur les versions de canal stable pour Microsoft Edge"

[MicrosoftVisualstudio]: https://visualstudio.microsoft.com "Visual Studio"  

[VisualstudioCode]: https://code.visualstudio.com "Code Visual Studio"  

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness "Types de cécité du Colour"  
[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Accept-Language"
[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Exemple de code dépendant des paramètres régionaux"
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives

[CR963183]: https://crbug.com/963183 "Problème 963183: DevTools n’est pas conforme à la norme WCAG"  
[CR1003700]: https://crbug.com/1003700 "Problème 1003700: ajout de la prise en charge de DevTools pour la simulation d’déficience de vision couleur"  
[CR1011679]: https://crbug.com/1011679 "Problème 1011679: Introduisez l’option ancrer à gauche dans le menu de commandes"  
[CR1016501]: https://crbug.com/1016501 "Problème 1016501: demande de fonctionnalité: bouton permettant de supprimer tous les remplacements locaux"  
[CR1050999]: https://crbug.com/1050999 "Problème 1050999: onglet Propriétés"  
[CR1051466]: https://crbug.com/1051466 "Problème 1051466: prendre en charge le débogage de COOP/COEP dans DevTools"  
[CR1054447]: https://crbug.com/1054447 "Problème 1054447: mettre à jour les métriques de performance dans DevTools Timeline"  
[CR1051822]: https://crbug.com/1051822 "Problème 1051822: DevTools: ajouter une interface utilisateur pour émuler des paramètres régionaux"
[CR1041830]: https://crbug.com/1041830 "Problème 1041830: améliorer les couleurs pour les points d’arrêt"
[CR1050855]: https://crbug.com/1050855 "Problème 1050855: l’affichage des paramètres est difficile à découvrir"
[CR1056348]: https://crbug.com/1056348 "Problème 1056348: actualisation du composant barre d’informations"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "Explication de COOP et de COEP-explication-la politique d’ouverture"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 "Explication de la stratégie d’intégration de COOP et COEP"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "Phare GitHub référentiel Samples"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/updates/2020/03/devtools/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
