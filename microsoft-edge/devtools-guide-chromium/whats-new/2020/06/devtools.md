---
title: Nouveautés de DevTools (Microsoft Edge 85)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: f569414a95336278c93b1bbafd57153ca902df12
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942197"
---
# Nouveautés de DevTools (Microsoft Edge 85)  

## Annonces de l’équipe Microsoft Edge DevTools  

Les sections suivantes répertorient les annonces que vous pouvez avoir manquées dans l’équipe Microsoft Edge DevTools.  Consultez les annonces pour essayer de nouvelles fonctionnalités dans les extensions de code DevTools, VS, etc.  Pour rester à jour sur les fonctionnalités les plus récentes de vos outils de développement, téléchargez les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] et [suivez l’équipe Microsoft Edge devtools sur Twitter][EdgeDevToolsTwitterAccount].  

### Fonctionnalités de débogage de grille CSS  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalités expérimentales":::
   Fonctionnalités expérimentales  
:::image-end:::  

L’équipe Microsoft Edge DevTools collabore avec les membres de l’équipe chrome DevTools et de la communauté de chrome pour ajouter de nouvelles fonctionnalités de débogage de grille CSS à DevTools.  Vous pouvez désormais afficher les numéros des lignes de la grille, les espaces de la grille et les quadrillages étendus en tant que superposition sur la page.  De plus, d’autres améliorations apportées aux outils de grille seront bientôt possibles.  

:::image type="complex" source="../../media/2020/06/experiments-grid.msft.png" alt-text="Fonctionnalités de débogage de grille CSS" lightbox="../../media/2020/06/experiments-grid.msft.png":::
   Fonctionnalités de débogage de grille CSS
:::image-end:::  

> [!NOTE]
> Pour activer l’expérience, voir [activer les fonctionnalités expérimentales][DevtoolsExperimentalFeaturesTurnOn] , puis activez la case à cocher en regard de **activer de nouvelles fonctionnalités de débogage de grille CSS**.  
> 
> Pour tester l’expérience à l’aide d’un exemple, voir [exemple de planificateur de grille CSS][CodepenRachelweilYzwBzKM].  

[#1047356][CR1047356] problème de chrome  

### Modification et lecture de requêtes avec la console réseau  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalités expérimentales":::
   Fonctionnalités expérimentales  
:::image-end:::  

Vous pouvez désormais utiliser les requêtes **modification et lecture** dans le [Journal du réseau][DevtoolsNetworkIndexLogActivity] à l’aide de la **console réseau**.  

:::image type="complex" source="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png" alt-text="Modification et lecture d’une demande dans le NetworkLog avec la console réseau" lightbox="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png":::
   Modification et lecture d’une demande dans le [NetworkLog][DevtoolsNetworkIndexLogActivity] avec la **console réseau**  
:::image-end:::  

Un nouveau panneau, la **console réseau** s’ouvre dans le [tiroir devtools][DevtoolsCustomizeIndexDrawer] et remplit automatiquement les informations pour la requête http.  Pour afficher la réponse renvoyée par le serveur, modifiez-la si nécessaire, puis sélectionnez **Envoyer**.  

Vous pouvez également utiliser la **console réseau** pour créer et envoyer des demandes http directement à partir du devtools.  

:::image type="complex" source="../../media/2020/06/experiments-network-console.msft.png" alt-text="Panneau de la console réseau" lightbox="../../media/2020/06/experiments-network-console.msft.png":::
   Panneau de la **console réseau**  
:::image-end:::  

> [!TIP]
> Pour afficher la **console réseau** dans le volet principal \ (en haut de la fenêtre) au lieu du [tiroir devtools][DevtoolsCustomizeIndexDrawer], voir [déplacement d’outils entre les panneaux](#move-tools-between-panels).  

> [!NOTE]
> Pour activer l’expérience, voir [activation des fonctionnalités expérimentales][DevtoolsExperimentalFeaturesTurnOn] , puis activez la case à cocher en regard de **activer la console réseau**.  
> 
> Ouvrez le [Journal du réseau][DevtoolsNetworkIndexLogActivity], ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez **modifier puis relire**.  

[#1093687][CR1093687] problème de chrome  

### Événements de respondWith du travailleur de service sous l’onglet Minutage  

L’onglet **minutage** du panneau **réseau** comporte désormais des `respondWith` événements de travailleur de service.  L' `respondWith` événement de travailleur de service affiche la durée du temps immédiatement avant que le `fetch` Gestionnaire d’événements du travailleur de service démarre, au moment où la `respondWith` promesse du `fetch` gestionnaire est finalisée.  

:::image type="complex" source="../../media/2020/06/timing-tab.msft.png" alt-text="Événement du travailleur de service respondWith dans l’onglet Minutage du panneau réseau" lightbox="../../media/2020/06/timing-tab.msft.png":::
   `respondWith`Événement du travailleur de service sous l’onglet **minutage** du panneau **réseau**  
:::image-end:::  

Développez **Response received** pour afficher d’autres informations de la `fetch` réponse comme `CacheStorageCacheName` , `serviceWorkerResponseSource` et `ResponseTime` .  

:::image type="complex" source="../../media/2020/06/timing-tab2.msft.png" alt-text="Développer la réponse reçue pour afficher des informations supplémentaires dans la réponse de récupération" lightbox="../../media/2020/06/timing-tab2.msft.png":::
   Développer la **réponse reçue** pour afficher des informations supplémentaires dans la `fetch` réponse  
:::image-end:::  

[#1066579][CR1066579] problème de chrome  

### Commentaires de webhint dans le volet problèmes  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalités expérimentales":::
   Fonctionnalités expérimentales  
:::image-end:::  

[webhint][WebhintMain] est un outil open source qui fournit des commentaires en temps réel sur l’accessibilité, la compatibilité entre les navigateurs, la sécurité, les performances, PWAS, ainsi que d’autres problèmes courants liés au développement Web sur les sites Web.  Vous pouvez à présent afficher des commentaires sur le webhint dans le volet [problèmes][DevtoolsIssues] .  

:::image type="complex" source="../../media/2020/06/experiments-webhint.msft.png" alt-text="Commentaires de webhint dans le volet problèmes" lightbox="../../media/2020/06/experiments-webhint.msft.png":::
   Commentaires de webhint dans le volet problèmes  
:::image-end:::  

> [!NOTE]
> Pour activer l’expérience, voir [activation des fonctionnalités expérimentales][DevtoolsExperimentalFeaturesTurnOn] , puis activez la case à cocher en regard de **activer webhint**.  
> 
> Ouvrez le volet [problèmes][DevtoolsIssues] pour afficher les commentaires du webhint.  

[#1070378][CR1070378] problème de chrome  

### Déplacer des outils entre les panneaux  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalités expérimentales":::
   Fonctionnalités expérimentales  
:::image-end:::  

En règle générale, il est possible d’ouvrir des outils tels que des **éléments** et un **réseau** uniquement dans le panneau principal \ (Top \) de devtools.  De même, il est possible d’ouvrir des outils tels que la vue et les **problèmes** en **3D** uniquement dans le panneau tiroir \ (en bas) de devtools.  Vous pouvez désormais personnaliser votre disposition DevTools en déplaçant des outils entre les volets supérieur et inférieur.  

:::image type="complex" source="../../media/2020/06/experiments-move-panels.msft.png" alt-text="Déplacement d’un onglet entre les panneaux" lightbox="../../media/2020/06/experiments-move-panels.msft.png":::
   Déplacement d’un onglet entre les panneaux  
:::image-end:::  

> [!NOTE]
> Pour activer l’expérience, voir [activer les fonctionnalités expérimentales][DevtoolsExperimentalFeaturesTurnOn] , puis cochez la case **en regard de permettre la prise en charge du déplacement des onglets entre les volets**.  

[#897944][CR897944] problème de chrome  

### Info-bulle améliorée de l’initiateur dans le panneau réseau  

Dans Microsoft Edge 83 et 84, les info-bulles de la colonne Initiator, qui indique la cause de la demande de ressource, dans le [Journal de réseau][DevtoolsNetworkIndexLogActivity] affiché avec une barre de défilement horizontale.  Vous pouvez uniquement afficher la pile d’appels à l’origine de la demande en effectuant un défilement horizontal dans l’info-bulle.  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-84.msft.png" alt-text="Info-bulle de l’initiateur dans Microsoft Edge 84" lightbox="../../media/2020/06/initiator-tooltip-84.msft.png":::
   Info-bulle de l’initiateur dans Microsoft Edge 84  
:::image-end:::  

À partir de Microsoft Edge 85, vous pouvez maintenant voir la pile d’appels d’initiateur dans l’info-bulle sans faire défiler l’affichage horizontalement.  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-85.msft.png" alt-text="Info-bulle de l’initiateur dans Microsoft Edge 85" lightbox="../../media/2020/06/initiator-tooltip-85.msft.png":::
   Info-bulle de l’initiateur dans Microsoft Edge 85
:::image-end:::  

[#1069404][CR1069404] problème de chrome  

## Annonces du projet de chrome  

Les sections suivantes annoncent des fonctionnalités supplémentaires disponibles dans Microsoft Edge 85 qui ont été fournies au projet de chrome Open source.  

### Modification de styles pour les infrastructures CSS-in-JS  

Le volet **styles** dispose désormais d’une meilleure prise en charge de l’édition des styles qui ont été créés avec les API [CSSOM (CSS Object Model)][CsswgDraftsCssom] .  De nombreux infrastructures et bibliothèques CSS-in-JS utilisent les API CSSOM du capot pour créer des styles.  

Vous pouvez à présent modifier les styles ajoutés en JavaScript à l’aide de [feuilles de style de construction][WicgConstructStylesheet].  Les feuilles de style construites constituent un nouveau moyen de créer et de répartir des styles réutilisables lors de l’utilisation de l' [ombre DOM][MdnShadowDom].  

Par exemple, les `h1` styles ajoutés avec `CSSStyleSheet` \ (API CSSOM \) ne sont pas modifiables auparavant.  Les styles sont désormais modifiables dans le volet **styles** .  

:::image type="complex" source="../../media/2020/06/css-in-js.msft.png" alt-text="Modification de la propriété Background des styles H1 ajoutés avec CSSStyleSheet de rose à LightBlue égale" lightbox="../../media/2020/06/css-in-js.msft.png":::
   Modification `background` de la propriété des `h1` styles ajoutés à `CSSStyleSheet` partir de `pink` à `lightblue` .
:::image-end:::  

Pour ce faire, utilisez un [exemple qui utilise CSS-in-js][CodepenZoherghadyaliAbdgrpz].

[#946975][CR946975] problème de chrome  

### Panneau de signalisation 6  

Le panneau de **signalisation** est désormais exécuté sur le phare 6.  Pour obtenir la liste complète des modifications, voir [notes de publication pour v 6.0.0][GithubGoogleChromeLighthouse600].  

Le phare 6,0 introduit trois nouvelles mesures pour le rapport: le plus grand nombre de contenus (LCP \), le décalage de la disposition cumulé \ (CLS \) et le temps de blocage total \ (TBT \).  

La formule d’indice de performance a également été pondérée pour mieux refléter l’expérience de chargement de l’utilisateur.  

[#772558][CR772558] problème de chrome  

#### Première dépréciation significative de Paint  

Tout d’abord, Paint (FMP \) est déconseillé dans la couleur de la 6,0.  Le FMP a également été supprimé du panneau **performances** .  Le **plus grand** nombre de peintures est le remplacement recommandé pour le logiciel FMP.  <!--See [First Meaningful Paint][WebDevFirstMeaningfulPaint] for an explanation of why it was deprecated.  -->  

<!--todo: add Largest Contentful Paint when section available  -->  
<!--todo: add First Meaningful Paint link and note when available  -->  

[#1096008][CR1096008] problème de chrome  

### Prise en charge des nouvelles fonctionnalités JavaScript  

DevTools possède désormais une meilleure prise en charge de certaines des fonctionnalités de langage JavaScript les plus récentes.  

:::row:::
   :::column span="1":::
      Saisie semi-automatique de syntaxe de [chaînage facultative][V8DevOptionalChaining]  
   :::column-end:::
   :::column span="2":::
      La saisie semi-automatique de propriété dans la **console** prend désormais en charge la syntaxe de chaînage facultative, par exemple,  `name?.` fonctionne désormais en plus de `name.` et `name[` .  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Mise en surbrillance de syntaxe pour les [champs privés][V8DevClassFieldsPrivate]  
   :::column-end:::
   :::column span="2":::
      la syntaxe des champs de classe privée est désormais correcte, mise en évidence et à l’impression dans le panneau **sources** .  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Mise en surbrillance de syntaxe pour l' [opérateur de fusion Null][V8DevNullishCoalescing]
   :::column-end:::
   :::column span="2":::
      DevTools est désormais correctement à l’impression de l’opérateur de fusion Null dans le panneau **sources** .  
   :::column-end:::
:::row-end:::  

Problèmes de chrome [#1073903][CR1073903], [#1083214][CR1083214] [#1083797][CR1083797]  

### Avertissements relatifs aux nouveaux raccourcis d’application dans le volet manifeste  

Les **raccourcis d’application** permettent aux utilisateurs de démarrer rapidement des tâches courantes ou recommandées au sein d’une application Web.  

<!--todo: add App shortcuts when section is live  -->  

Le volet **manifeste** affiche désormais des avertissements pour les conditions suivantes.  

* Les icônes de raccourci de l’application sont inférieures à 96 x 96 pixels  
* Les icônes de raccourci de l’application et les icônes du manifeste ne sont pas carrées \ (dans la mesure où les icônes sont ignorées \)  

:::image type="complex" source="../../media/2020/06/app-shortcut-warnings.msft.png" alt-text="Avertissements relatifs aux raccourcis d’application" lightbox="../../media/2020/06/app-shortcut-warnings.msft.png":::
   Avertissements relatifs aux raccourcis d’application  
:::image-end:::  

[#955497][CR955497] problème de chrome  

### Affichage cohérent du volet calculé  

Le volet **calculé** dans le panneau des **éléments** s’affiche désormais comme un volet dans toutes les tailles de fenêtre d’affichage.  Auparavant, le volet **calculé** fusionné à l’intérieur du volet **styles** lorsque la largeur de la fenêtre d’affichage de devtools était étroite.  

:::image type="complex" source="../../media/2020/06/computed-pane.msft.png" alt-text="Le volet calculé s’affiche de façon cohérente sous forme de volet distinct même lorsque le DevTools est étroit." lightbox="../../media/2020/06/computed-pane.msft.png":::
   Le volet **calculé** s’affiche de façon cohérente sous forme de volet distinct même lorsque le devtools est étroit.
:::image-end:::  

[#1073899][CR1073899] problème de chrome  

### Décalages du bytecode pour les fichiers webassembly  

DevTools utilise désormais les décalages du bytecode pour afficher les numéros de ligne de l’WASM de démontage.  
Les numéros de ligne permettent de clarifier le fait que vous examinez les données binaires et qu’ils se conservent de manière plus cohérente sur la manière dont WASM Runtime référence les emplacements.  

[#1071432][CR1071432] problème de chrome  

### Copies par ligne et couper dans le panneau sources  

Lorsque vous effectuez une opération de copie ou de coupe sans sélection dans l' [éditeur du panneau sources][DevtoolsSourcesEditCssJavascript], devtools copie ou coupe la ligne de contenu actuelle.  

:::image type="complex" source="../../media/2020/06/line-wise-cut.msft.png" alt-text="Lorsque le curseur se trouve à la fin de la ligne 5, en copiant l’ensemble de la ligne à partir de pen.js dans le DevTools et en la collant dans le code VS" lightbox="../../media/2020/06/line-wise-cut.msft.png":::
   Le curseur étant placé à la fin de la ligne 5, copiez l’ensemble de la ligne à partir de **pen.js** dans le devtools et collez-la dans le [code vs][VSCode].
:::image-end:::  

[#800028][CR800028] problème de chrome

### Mises à jour des paramètres de la console  

#### Dissocier les mêmes messages de console  

Le bouton bascule **similaire** dans les paramètres de la console s’applique désormais aux messages en double.  Auparavant, il vient d’être appliqué à des messages similaires.  

Par exemple, auparavant, DevTools n’a pas dissocier les `hello` messages même si le **groupe similaire** n’est pas activé.  Les `hello` messages sont désormais dissociés.  

:::image type="complex" source="../../media/2020/06/ungroup-similar.msft.png" alt-text="Lorsque le groupe similaire n’est pas activé, les messages Hello ne sont pas regroupés" lightbox="../../media/2020/06/ungroup-similar.msft.png":::
   Lorsque le **groupe similaire** est désactivé, les `hello` messages ne sont pas regroupés.
:::image-end:::  

[Pour ce faire, utilisez un exemple qui envoie des messages en double à la console][CodepenZoherghadyaliZyrjgdJ].  

[#1082963][CR1082963] problème de chrome  

### Conservation des paramètres de contexte sélectionnés uniquement  

Les paramètres de **contexte sélectionnés uniquement** dans les paramètres de la console sont désormais conservés.  Auparavant, les paramètres étaient réinitialisés chaque fois que vous avez fermé et rouvert DevTools.  La modification fait en sorte que le comportement de la configuration soit cohérent avec d’autres options de paramètres de la console.  

:::image type="complex" source="../../media/2020/06/selected-context.msft.png" alt-text="Paramètre de contexte sélectionné uniquement" lightbox="../../media/2020/06/selected-context.msft.png":::
   Paramètre de **contexte sélectionné uniquement**  
:::image-end:::  

[#1055875][CR1055875] problème de chrome  

### Mises à jour du panneau de performance  

#### Informations du cache de compilation JavaScript dans le panneau performances  

Les [informations du cache de compilation JavaScript][V8DevCodeCaching] sont désormais toujours affichées sous l’onglet Résumé du panneau performance.  Auparavant, DevTools n’affichait aucune information liée à la mise en cache du code si la mise en cache du code ne s’est pas produit.  

:::image type="complex" source="../../media/2020/06/js-compilation-cache.msft.png" alt-text="Informations du cache de compilation JavaScript" lightbox="../../media/2020/06/js-compilation-cache.msft.png":::
   Informations du cache de compilation JavaScript  
:::image-end:::  

[#912581][CR912581] problème de chrome  

#### Alignement du minutage de la navigation dans le panneau performance  

Panneau **performance** permettant de montrer les heures dans les règles en fonction de la date de début de l’enregistrement.  Le minutage est désormais modifié pour les enregistrements dans lesquels l’utilisateur navigue, où DevTools affiche désormais les heures de règle relatives à la navigation à la place.  

:::image type="complex" source="../../media/2020/06/nav-timing.msft.png" alt-text="Aligner le minutage de la navigation dans le panneau performances" lightbox="../../media/2020/06/nav-timing.msft.png":::
   Aligner le minutage de la navigation dans le panneau **performances**  
:::image-end:::  

Les heures pour `DOMContentLoaded` , première peinture, première image de dessin, et les événements de peinture volumineux le plus volumineux sont mis à jour de manière à être par rapport au début de la navigation, ce qui signifie que le minutage correspond au minutage indiqué par `PerformanceObserver` .  

[#974550][CR974550] problème de chrome  

### Nouvelles icônes pour les points d’arrêt, les points d’arrêt conditionnel et la logpoints  

Le panneau **sources** comporte de nouvelles conceptions pour les points d’arrêt, les points d’arrêt conditionnel et la logpoints.  Les points d’arrêt sont représentés par un cercle rouge, comme le [code vs][VSCode] et [Visual Studio][VS].  Des icônes sont ajoutées pour différencier les points d’arrêt conditionnels et logpoints.  

:::image type="complex" source="../../media/2020/06/breakpoints.msft.png" alt-text="Points d’arrêt" lightbox="../../media/2020/06/breakpoints.msft.png":::
   Points d’arrêt  
:::image-end:::  

[#1041830][CR1041830] problème de chrome  

## Télécharger les canaux Microsoft Edge preview  

Si vous utilisez Windows ou macOS, envisagez d’utiliser les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] comme navigateur par défaut.  Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.  

## Contacter l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  
[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu "Exécuter des commandes à l’aide du menu de commandes de Microsoft Edge DevTools | Documents Microsoft"
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Tiroir-personnaliser Microsoft Edge DevTools | Documents Microsoft"
[DevtoolsExperimentalFeaturesTurnOn]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Activer les fonctionnalités expérimentales-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsIssues]: /microsoft-edge/devtools-guide-chromium/issues "Recherchez et corrigez les problèmes liés à l’outil problèmes dans Microsoft Edge DevTools Documents Microsoft"
[DevtoolsSourcesEditCssJavascript]: /microsoft-edge/devtools-guide-chromium/sources#edit-css-and-javascript "Présentation de la modification du panneau CSS et JavaScript-sources | Documents Microsoft"  
[DevtoolsNetworkIndexLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Journalisation de l’activité du réseau-Inspectez l’activité réseau dans Microsoft Edge DevTools | Documents Microsoft"

[CodepenZoherghadyaliAbdgrpz]: https://codepen.io/zoherghadyali/full/abdGrPZ "Modification de styles pour les infrastructures CSS-in-JS | CodePen"
[CodepenZoherghadyaliZyrjgdJ]: https://codepen.io/zoherghadyali/full/zYrjgdJ "Envoyer des messages en double à la console | CodePen"
[CodepenRachelweilYzwBzKM]: https://codepen.io/hxlnt/full/YzwBzKM "Exemple de planificateur de grille CSS | CodePen"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bugs du chrome"  

[CR772558]: https://crbug.com/772558 "DevTools: mise à jour vers la dernière version de phare | Bugs du chrome"  
[CR800028]: https://crbug.com/800028 "Le raccourci de ligne dupliqué dans l’éditeur des outils de développeur ne fonctionne pas après la mise à jour de chrome | Bugs du chrome"  
[CR912581]: https://crbug.com/912581 "Exposez les scripts dont le code a été mis en cache par V8 dans DevTools/à propos de. Bugs du chrome"  
[CR946975]: https://crbug.com/946975 "L’encadré styles DevTools ne fonctionne pas avec les feuilles de style construites | Bugs du chrome"  
[CR955497]: https://crbug.com/955497 "Menu contextuel de l’icône d’application pour PWAs | Bugs du chrome"  
[CR974550]: https://crbug.com/974550 "Incompatibilité métrique entre le panneau perf et performanceObserver | Bugs du chrome"  
[CR1041830]: https://crbug.com/1041830 "Amélioration des couleurs pour les points d’arrêt | Bugs du chrome"  
[CR1055875]: https://crbug.com/1055875 "La valeur du paramètre de console de contexte sélectionné ne persiste pas après la fermeture et la réouverture des outils de développement | Bugs du chrome"  
[CR1066579]: https://crbug.com/1066579 "DevTools: afficher ServiceWorkers de récupération de la chronologie par requête dans le panneau réseau | Bugs du chrome"  
[CR1071432]: https://crbug.com/1071432 "WASM Basic Basic Developer Bugs du chrome"  
[CR1073899]: https://crbug.com/1073899 "L’onglet style calculé disparaît en mode réactif | Bugs du chrome"  
[CR1073903]: https://crbug.com/1073903 "DevTools: la surbrillance de syntaxe ne fonctionne pas avec les champs privés | Bugs du chrome"  
[CR1082963]: https://crbug.com/1082963 "Impossible de désactiver le comportement des messages similaires du groupe de la console | Bugs du chrome"  
[CR1083214]: https://crbug.com/1083214 "Acorn ne prend pas en charge le chaînage facultatif. Bugs du chrome"  
[CR1083797]: https://crbug.com/1083797 "Impression incorrecte pour une fusion nulle Bugs du chrome"  
[CR1096008]: https://crbug.com/1096008 "Supprimer le FMP | Bugs du chrome"  
[CR1047356]: https://crbug.com/1047356 "Outils CSS Grid/Flexbox/tableau | Bugs du chrome"  
[CR1093687]: https://crbug.com/1093687 "Créer un outil permettant de créer et de relire des demandes de réseau synthétique Bugs du chrome"  
[CR1070378]: https://crbug.com/1070378 "Intégration de webhint dans DevTools | Bugs du chrome"  
[CR1069404]: https://crbug.com/1069404 "[Outils de développement] les fenêtres contextuelles de widgets sont trop étroites | Bugs du chrome"  
[CR897944]: https://crbug.com/897944 "Panneaux devtool déplaçables | Bugs du chrome"

[GithubGoogleChromeLighthouse600]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.0.0 "v 6.0.0-GoogleChrome/phare | GitHub"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Nouveau problème-MicrosoftDocs/Edge-développeur"  

[MdnShadowDom]: https://developer.mozilla.org/docs/Web/Web_Components/Using_shadow_DOM "Utilisation de l’ombre DOM | MDN"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download/ "Canaux Microsoft Edge preview"  

[VS]: https://visualstudio.microsoft.com/ "Visual Studio"
[VSCode]: https://code.visualstudio.com/ "Code Visual Studio"  

[CsswgDraftsCssom]: https://drafts.csswg.org/cssom "Modèle d’objet CSS (CSSOM) | Brouillons de l’éditeur de groupe de travail CSS W3C"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publiez un tweet"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools compte Twitter"  

[V8DevClassFieldsPrivate]: https://v8.dev/features/class-fields#private-class-fields "Champs de classe privée-champs de classe publique et privée | V8. Développeur"  
[V8DevCodeCaching]: https://v8.dev/blog/code-caching-for-devs "Mise en cache de code pour les développeurs JavaScript | V8. Développeur"  
[V8DevNullishCoalescing]: https://v8.dev/features/nullish-coalescing "Fusion par zéro | V8. Développeur"  
[V8DevOptionalChaining]: https://v8.dev/features/optional-chaining "Chaînage facultatif | V8. Développeur"  

[WebhintMain]: https://webhint.io "Astuce"  

[WicgConstructStylesheet]: https://wicg.github.io/construct-stylesheets/ "Objets StyleSheet de construction | CG"

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
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/updates/2020/06/devtools/index) et est créée par [Jecelyn Yeen][JecelynYeen] \ (développeurs, chrome devtools \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
