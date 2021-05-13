---
description: Référence sur toutes les façons d’enregistrer et d’analyser les performances dans Microsoft Edge DevTools.
title: Référence d’analyse des performances
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 5cd7c4aee6eb5f0c48f783e250efa1ef69010fc4
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564349"
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
# <a name="performance-analysis-reference"></a>Référence d’analyse des performances  

Cette page est une référence complète des fonctionnalités Microsoft Edge DevTools relatives à l’analyse des performances.  

Accédez [à Prise en main][DevtoolsEvaluatePerformanceGettingStarted] Avec analyse des performances d’exécution pour un didacticiel guidé sur l’analyse des performances d’une page à l’aide Microsoft Edge [DevTools][MicrosoftEdgeDevTools].  

## <a name="record-performance"></a>Performances d’enregistrement  

### <a name="record-runtime-performance"></a>Performances d’exécution d’enregistrement  

Enregistrez les performances d’exécution lorsque vous souhaitez analyser les performances d’une page en cours d’exécution, par opposition au chargement.  

1.  Accédez à la page que vous souhaitez analyser.  
1.  Ouvrez **l’outil** Performance dans DevTools.  
1.  Choose **Record** \( ![ Record icon ](../media/record-icon.msft.png) \).  
    
    :::image type="complex" source="../media/evaluate-performance-performance-record-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-record-highlight.msft.png":::
       **Record**  
    :::image-end:::  
    
1.  Interagir avec la page.  DevTools enregistre toutes les activités de page qui se produisent suite à vos interactions.  
1.  Choose **Record** again or choose **Stop** to stop recording.  
    
### <a name="record-load-performance"></a>Performances de chargement d’enregistrement  

Enregistrez les performances de chargement lorsque vous souhaitez analyser les performances d’une page en cours de chargement, par opposition à l’exécution.  

1.  Accédez à la page que vous souhaitez analyser.  
1.  Ouvrez **le panneau Performances** de DevTools.  
1.  Choose **Refresh page** \( Refresh Page ![ ](../media/refresh-page-icon.msft.png) \).  DevTools enregistre les mesures de performances pendant l’actualisation de la page, puis arrête automatiquement l’enregistrement quelques secondes après la fin du chargement.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-refresh-button.msft.png" alt-text="Page Actualiser" lightbox="../media/evaluate-performance-performance-refresh-button.msft.png":::
       **Page Actualiser**  
    :::image-end:::  
    
DevTools effectue automatiquement un zoom avant sur la partie de l’enregistrement où la majeure partie de l’activité s’est produite.  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed.msft.png" alt-text="Un enregistrement de chargement de page" lightbox="../media/evaluate-performance-performance-refreshed.msft.png":::
   Un enregistrement de chargement de page  
:::image-end:::  

### <a name="capture-screenshots-while-recording"></a>Capture d’écran pendant l’enregistrement  

Activer la case à cocher **Captures** d’écran pour capturer une capture d’écran de chaque image pendant l’enregistrement.  

:::image type="complex" source="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png" alt-text="Case à cocher Captures d’écran" lightbox="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png":::
   Case **à cocher Captures d’écran**  
:::image-end:::  

Accédez à [Afficher une capture d’écran](#view-a-screenshot) pour apprendre à interagir avec les captures d’écran.  

### <a name="force-garbage-collection-while-recording"></a>Forcer le collecte de la garbage lors de l’enregistrement  

Pendant l’enregistrement d’une page, sélectionnez Collecter la **garbage** \( Collect garbage icon \) pour forcer le ![ collecte de la ](../media/collect-garbage-icon.msft.png) garbage.  

:::image type="complex" source="../media/evaluate-performance-performance-collect-garbage-button.msft.png" alt-text="Collecter la garbage" lightbox="../media/evaluate-performance-performance-collect-garbage-button.msft.png":::
   Collecter la garbage  
:::image-end:::  

### <a name="show-recording-settings"></a>Afficher les paramètres d’enregistrement  

Choose **Capture settings** \( ![ Capture settings ](../media/capture-settings-icon.msft.png) \) to expose more settings related to how DevTools captures performance recordings.  

:::image type="complex" source="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png" alt-text="Section Capture Paramètres" lightbox="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png":::
   Section **Capture Paramètres**  
:::image-end:::  

### <a name="disable-javascript-samples"></a>Désactiver les exemples JavaScript  

Par défaut, la section **Main** d’un enregistrement affiche des piles d’appels détaillées de fonctions JavaScript qui ont été appelées pendant l’enregistrement.  Pour désactiver ces piles d’appels :  

1.  Ouvrez le menu **Paramètres de** capture.  Accédez à [Afficher les paramètres d’enregistrement.](#show-recording-settings)  
1.  Activer la case **à cocher Désactiver les exemples JavaScript.**  
1.  Prenez un enregistrement de la page.  
    
Les 2 figures suivantes affichent la différence entre la désactivation et l’activation des exemples JavaScript.  La section **Main** de l’enregistrement est beaucoup plus courte lorsque l’échantillonnage est désactivé, car elle omet toutes les piles d’appels JavaScript.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png" alt-text="Exemple d’enregistrement lorsque les exemples JS sont désactivés" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png":::
         Exemple d’enregistrement lorsque les exemples JS sont désactivés  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png" alt-text="Exemple d’enregistrement lorsque les exemples JS sont allumés" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png":::
         Exemple d’enregistrement lorsque les exemples JS sont allumés  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### <a name="throttle-the-network-while-recording"></a>Limiter le réseau lors de l’enregistrement  

Pour limiter le réseau lors de l’enregistrement :  

1.  Ouvrez le menu **Paramètres de** capture.  Accédez à [Afficher les paramètres d’enregistrement.](#show-recording-settings)  
1.  Définissez **le** réseau sur le niveau de limitation souhaité.  
    
### <a name="throttle-the-cpu-while-recording"></a>Limiter l’UC lors de l’enregistrement  

Pour limiter le processeur lors de l’enregistrement :  

1.  Ouvrez le menu **Paramètres de** capture.  Accédez à [Afficher les paramètres d’enregistrement.](#show-recording-settings)  
1.  Définissez **le processeur** sur le niveau de limitation souhaité.  
    
La limitation est relative aux fonctionnalités de votre ordinateur.  Par exemple, l’option **de ralentissement 2x** ralentit le fonctionnement de votre processeur 2 fois plus lent que la normale.  DevTools ne simule pas véritablement les processeurs des appareils mobiles, car l’architecture des appareils mobiles est très différente de celle des ordinateurs de bureau et des ordinateurs portables.  

### <a name="turn-on-advanced-paint-instrumentation"></a>Activer l’instrumentation de pinceau avancée  

Pour afficher l’instrumentation de la couleur détaillée :  

1.  Ouvrez le menu **Paramètres de** capture.  Accédez à [Afficher les paramètres d’enregistrement.](#show-recording-settings)  
1.  Activez **la case à cocher Activer l’instrumentation de pinceau avancée (lente).**  

Pour apprendre à interagir avec les informations de paint, accédez à [Afficher](#view-layers-information) les couches et [afficher le profileur de paint.](#view-paint-profiler)  

## <a name="save-a-recording"></a>Enregistrer un enregistrement  

Pour enregistrer un enregistrement, ouvrez le menu contextuel \(clic droit\), puis choisissez **Enregistrer le profil.**  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png" alt-text="Enregistrer le profil" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png":::
   **Enregistrer le profil**  
:::image-end:::  

## <a name="load-a-recording"></a>Charger un enregistrement  

Pour charger un enregistrement, ouvrez le menu contextuel \(clic droit\), puis choisissez **Charger le profil.**  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png" alt-text="Charger le profil" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png":::
   **Charger le profil**  
:::image-end:::  

## <a name="clear-the-previous-recording"></a>Effacer l’enregistrement précédent  

Après avoir enregistré l’enregistrement, sélectionnez **Effacer l’enregistrement** \( Effacer l’icône d’enregistrement \) pour effacer cet enregistrement à ![ partir du panneau ](../media/clear-recording-icon.msft.png) **Performances.**  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png" alt-text="Effacer l’enregistrement" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png":::
   **Effacer l’enregistrement**  
:::image-end:::  

## <a name="analyze-a-performance-recording"></a>Analyser un enregistrement des performances  

Une fois que vous avez enregistré **** [les](#record-runtime-performance) performances d’exécution ou les performances de chargement d’enregistrement, [](#record-load-performance)le panneau Performances fournit un grand nombre de données pour analyser les performances de ce qui vient de se produire.  

### <a name="select-a-portion-of-a-recording"></a>Sélectionner une partie d’un enregistrement  

Faites glisser votre souris vers la gauche ou la droite dans la **vue d’ensemble** pour sélectionner une partie d’un enregistrement.  La **vue d’ensemble** est la section qui contient **les graphiques FPS,** **CPU**et **NET.**  

:::image type="complex" source="../media/evaluate-performance-performance-zoom-highlighted.msft.png" alt-text="Faire glisser la souris sur la vue d’ensemble pour effectuer un zoom" lightbox="../media/evaluate-performance-performance-zoom-highlighted.msft.png":::
   Faire glisser la souris sur la **vue d’ensemble** pour effectuer un zoom  
:::image-end:::  

Pour sélectionner une partie à l’aide du clavier :  

1.  Choisissez l’arrière-plan de la section **Main** ou l’une des sections en de côté, telles que **Interactions,** **Réseau**ou **GPU.**  Ce flux de travail de clavier ne fonctionne que lorsque l’une de ces sections est en focus.  
1.  Utilisez les `W` touches `A` , , , `S` pour `D` zoomer, déplacer vers la gauche, zoom arrière et déplacer vers la droite, respectivement.  

Pour sélectionner une partie à l’aide d’un trackpad, effectuer les actions suivantes.  

1.  Pointez votre souris sur la section **Vue** d’ensemble ou la section **Détails.**  La section **Vue d’ensemble** est la zone contenant **les graphiques FPS,** **CPU**et **NET.**  La section **Détails** est la zone contenant la section **Main,** la section **Interactions,** etc.  
1.  À l’aide de deux doigts, effectuez un balayage vers le haut pour effectuer un zoom arrière, un balayage vers la gauche pour se déplacer vers la gauche, un balayage vers le bas pour effectuer un zoom avant et un balayage vers la droite pour se déplacer vers la droite.  

Pour faire défiler un graphique long dans la section **Main** ou l’un des voisins, choisissez et maintenez tout en faisant glisser vers le haut et vers le bas.  Faites glisser vers la gauche et la droite pour déplacer la partie de l’enregistrement choisie.  

### <a name="search-activities"></a>Activités de recherche  

Sélectionnez `Control` + `F` \(Windows, Linux\) ou `Command` + `F` \(macOS\) **** pour ouvrir la zone de recherche en bas du panneau Performances.  

:::image type="complex" source="../media/evaluate-performance-performance-search-regex.msft.png" alt-text="Zone de recherche" lightbox="../media/evaluate-performance-performance-search-regex.msft.png":::
   Zone de recherche  
:::image-end:::  

Pour naviguer dans les activités qui correspondent à votre requête :  

*   Utilisez les **boutons** Précédent \( ![ Précédent ](../media/previous-icon.msft.png) \) et **Suivant** \( ![ Suivant ](../media/next-icon.msft.png) \).  
*   Sélectionnez `Shift` + `Enter` le précédent ou `Enter` le suivant.  

Pour modifier les paramètres de requête :  

*   Choose **Case sensitive** \( Case sensitive ![ ](../media/search-case-icon.msft.png) \) to make the query case sensitive.  
*   Choisissez **Regex** \( ![ Regex ](../media/search-regex-icon.msft.png) \) pour utiliser une expression régulière dans votre requête.  

Pour masquer la zone de recherche, choisissez **Annuler.**  

### <a name="view-main-thread-activity"></a>Afficher l’activité du thread principal  

Utilisez la section **Main** pour afficher l’activité qui s’est produite sur le thread principal de la page.  

:::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Section Principale" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
   Section **Principale**  
:::image-end:::  

Choisissez un événement pour afficher plus d’informations à son sujet dans le **panneau Résumé.**  DevTools décrit l’événement sélectionné.  

:::image type="complex" source="../media/evaluate-performance-performance-summary-me.msft.png" alt-text="Plus d’informations sur la fonction anonyme dans le panneau Résumé" lightbox="../media/evaluate-performance-performance-summary-me.msft.png":::
   Plus d’informations sur `anonymous` la fonction dans le panneau **Résumé**  
:::image-end:::  

DevTools représente l’activité de thread principale avec un graphique graphique.  L’axe X représente l’enregistrement au fil du temps.  L’axe Y représente la pile d’appels.  Les événements en haut provoquent les événements en dessous.  

:::image type="complex" source="../media/evaluate-performance-performance-main-flame-chart.msft.png" alt-text="Graphique de graphique" lightbox="../media/evaluate-performance-performance-main-flame-chart.msft.png":::
   Graphique de graphique  
:::image-end:::  

Dans la figure précédente, un événement a `click` provoqué un événement sur la ligne `Function Call` `activitytabs.js` 53.  Vous trouverez `Function Call` ci-dessous un avis sur le fait qu’une fonction anonyme a été exécuté.  La fonction anonyme demandée `a` , qui a demandé , qui a demandé `wait` `Minor GC` .  

DevTools affecte des couleurs aléatoires aux scripts.  Dans la figure précédente, les demandes de fonction d’un script sont colorées en vert clair.  Les demandes provenant d’un autre script sont colorées.  Le jaune foncé représente l’activité de script et l’événement violet représente l’activité de rendu.  Ces événements jaunes et violets plus foncés sont cohérents dans tous les enregistrements.  

Accédez [à Désactiver les exemples JavaScript si](#disable-javascript-samples) vous souhaitez masquer le graphique détaillé des requêtes JavaScript.  Lorsque les exemples JS sont désactivés, seuls les événements de haut niveau tels que la figure précédente `Event: choose` `Function Call` `str` s’affichent.  

### <a name="view-activities-in-a-table"></a>Afficher les activités dans un tableau  

Après avoir enregistré une page, vous n’avez pas besoin de vous appuyer uniquement sur la section **Main** pour analyser les activités.  DevTools fournit également trois vues tabulaires pour l’analyse des activités.  Chaque affichage vous donne une perspective différente sur les activités :  

*   Lorsque vous souhaitez afficher les activités racine qui causent le plus de travail, utilisez le panneau Arborescence [des](#the-call-tree-panel) appels.  
*   Lorsque vous souhaitez afficher les activités où le plus de temps a été passé directement, utilisez le [panneau de bas](#the-bottom-up-panel) en haut.  
*   Lorsque vous souhaitez afficher les activités dans l’ordre dans lequel elles se sont produites pendant l’enregistrement, utilisez le panneau [Journal des](#the-event-log-panel) événements.  
    
> [!NOTE]
> Les trois sections suivantes font toutes référence à la même démonstration.  Exécutez la démonstration vous-même [à la démonstration des onglets d’activité.][ActivityTabsDemo]  

#### <a name="root-activities"></a>Activités racine  

Voici une explication **du concept** d’activités racine **** mentionné dans le panneau Arborescence des **appels,** le panneau inférieur vers le haut et le panneau **Journal des** événements.  

Les activités racines sont celles qui entraînent le travail du navigateur.  Par exemple, lorsque vous choisissez une page web, le navigateur exécute une `Event` activité en tant qu’activité racine.  Cela `Event` peut entraîner l’exécuter, et ainsi de suite.  

Dans le graphique graphique de la section **Main,** les activités racine sont en haut du graphique.  Dans les **panneaux Arborescence des appels** **et Journal des** événements, les activités racines sont les éléments de niveau supérieur.  

Accédez au panneau [Arborescence des](#the-call-tree-panel) appels pour obtenir un exemple d’activités racine.  

#### <a name="the-call-tree-panel"></a>Panneau Arborescence des appels  

Utilisez le **panneau Arborescence des** appels pour afficher les [activités racine qui](#root-activities) sont à l’origine du travail le plus important.  

Le **panneau Arborescence** des appels affiche uniquement les activités pendant la partie sélectionnée de l’enregistrement.  Accédez [à Sélectionner une partie d’un enregistrement](#select-a-portion-of-a-recording) pour découvrir comment sélectionner des parties.  

:::image type="complex" source="../media/evaluate-performance-performance-call-tree.msft.png" alt-text="Panneau Arborescence des appels" lightbox="../media/evaluate-performance-performance-call-tree.msft.png":::
   Panneau **Arborescence des** appels  
:::image-end:::  

Dans la figure précédente, le niveau **** supérieur des éléments dans la colonne Activité, tels que les activités racine, `Evaluate Script` et sont des activités `Parse HTML` racine.  L’imbrmbrage représente la pile d’appels.  Par exemple, dans la figure précédente, ce `Parse HTML` qui a provoqué et `Evaluate Script` `Compile Script` `(anonymous)` .  

**Le temps libre** représente le temps passé directement dans cette activité.  **Le temps** total représente le temps consacré à cette activité ou à l’un des enfants.  

Choisissez **Temps libre,** **Temps total**ou **Activité** pour trier le tableau par colonne.  

Utilisez la zone de texte **Filtrer** pour filtrer les événements par nom d’activité.  

Par défaut, le menu **De** regroupement est définie sur **Aucun regroupement.**  Utilisez le menu **Regroupement pour** trier le tableau d’activité en fonction de différents critères.  

Choose **Show Heaviest Stack** \( Show ![ Heaviest Stack ](../media/show-heaviest-stack-icon.msft.png) \) to reveal another table to the right of the **Activity** table.  Choisissez une activité pour remplir la table **Stack la plus** lourde.  Le **tableau Stack le plus lourd** affiche les enfants de l’activité sélectionnée qui ont mis le plus de temps à s’exécuter.  

#### <a name="the-bottom-up-panel"></a>Panneau de Bottom-Up  

Utilisez le **panneau Bas vers le** haut pour afficher les activités qui ont pris le plus de temps dans l’agrégation.  

Le **panneau Inférieur vers le** haut affiche uniquement les activités pendant la partie sélectionnée de l’enregistrement.  Accédez [à Sélectionner une partie d’un enregistrement](#select-a-portion-of-a-recording) pour découvrir comment sélectionner des parties.  

:::image type="complex" source="../media/evaluate-performance-performance-bottoms-up.msft.png" alt-text="Panneau de Bottom-Up" lightbox="../media/evaluate-performance-performance-bottoms-up.msft.png":::
   Panneau **bas vers le** haut  
:::image-end:::  

Dans le **graphique de** la section Main de la figure précédente, accédez à cette quasi-totalité du temps passé en cours d’exécution. `Parse HTML`  L’activité la plus importante dans **le panneau De** bas en haut de la figure précédente est `Parse HTML` .  <!--In the flame chart of the previous figure, the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  Accédez au **panneau De bas en** haut, l’activité la plus coûteuse suivante est `Layout` .  

La **colonne Temps** libre représente le temps agrégé passé directement dans cette activité, dans toutes les occurrences.  

La **colonne Temps total** représente le temps agrégé passé dans cette activité ou n’importe quel enfant.  

#### <a name="the-event-log-panel"></a>Panneau Journal des événements  

Utilisez le **panneau Journal des** événements pour afficher les activités dans l’ordre dans lequel elles se sont produites pendant l’enregistrement.  

Le **panneau Journal des** événements affiche uniquement les activités pendant la partie sélectionnée de l’enregistrement.  Accédez [à Sélectionner une partie d’un enregistrement](#select-a-portion-of-a-recording) pour découvrir comment sélectionner des parties.  

:::image type="complex" source="../media/evaluate-performance-performance-event-log.msft.png" alt-text="Panneau Journal des événements" lightbox="../media/evaluate-performance-performance-event-log.msft.png":::
   Panneau **Journal des événements**  
:::image-end:::  

La **colonne Heure** de début représente le point auquel cette activité a démarré, par rapport au début de l’enregistrement.  Par exemple, l’heure de début de l’élément sélectionné dans la figure précédente signifie que l’activité a démarré 175,7 ms après le démarrage de `175.7 ms` l’enregistrement.  

La **colonne Temps** libre représente le temps passé directement dans cette activité.  

Les **colonnes Temps** total représentent le temps passé directement dans cette activité ou dans l’un des enfants.  

Choisissez **Heure de début,** **Temps**libre ou **Durée totale** pour trier le tableau par colonne.

Utilisez la **zone de** texte Filtrer pour filtrer les activités par nom.  

Utilisez le menu **Durée** pour filtrer toutes les activités dont la durée est inférieure à 1 ms ou 15 ms.  Par défaut, le menu **Durée** est définie sur **Tous,** ce qui signifie que toutes les activités sont affichées.  

Désactivez les case à cocher **Chargement,** **Script,** **** **Rendu**ou Dessin pour filtrer toutes les activités de ces catégories.  

### <a name="view-gpu-activity"></a>Afficher l’activité GPU  

Afficher l’activité GPU dans la section **GPU.**  

:::image type="complex" source="../media/evaluate-performance-performance-gpu-zoomed.msft.png" alt-text="Section GPU" lightbox="../media/evaluate-performance-performance-gpu-zoomed.msft.png":::
   Section **GPU**  
:::image-end:::  

### <a name="view-raster-activity"></a>Afficher l’activité de raster  

Afficher l’activité de raster dans la section **Raster.**  

:::image type="complex" source="../media/evaluate-performance-performance-raster.msft.png" alt-text="Section Raster" lightbox="../media/evaluate-performance-performance-raster.msft.png":::
   Section **Raster**  
:::image-end:::  

### <a name="view-interactions"></a>Afficher les interactions  

Utilisez la section **Interactions pour** rechercher et analyser les interactions utilisateur qui se sont produites pendant l’enregistrement.  

:::image type="complex" source="../media/evaluate-performance-performance-interactions-animation.msft.png" alt-text="Section Interactions" lightbox="../media/evaluate-performance-performance-interactions-animation.msft.png":::
   Section **Interactions**  
:::image-end:::  

Une ligne rouge au bas d’une interaction représente le temps passé à attendre le thread principal.  

Choisissez une interaction pour afficher plus d’informations à ce sujet dans le **panneau Résumé.**  

### <a name="analyze-frames-per-second-fps"></a>Analyser les images par seconde (FPS)  

DevTools offre de nombreuses façons d’analyser les images par seconde :  

*   Utilisez [le graphique FPS pour](#the-fps-chart) obtenir une vue d’ensemble du service FPS pendant toute la durée de l’enregistrement.  
*   Utilisez [la section Frames pour](#the-frames-section) afficher la durée d’un cadre particulier.  
*   Utilisez la **jauge FPS** pour une estimation en temps réel du service FPS lors de l’utilisation de la page.  Accédez à [Afficher les images par seconde en temps réel avec la jauge FPS.](#view-frames-per-second-in-realtime-with-the-fps-meter)  
    
#### <a name="the-fps-chart"></a>Graphique FPS  

Le **graphique FPS** fournit une vue d’ensemble de la fréquence d’images pendant toute la durée d’un enregistrement.  En règle générale, plus la barre verte est élevée, plus la fréquence d’images est élevée.  

Une barre rouge au-dessus **du graphique FPS** est un avertissement signalant que la fréquence d’images a été si faible qu’elle a probablement nuire à l’expérience de l’utilisateur.  

:::image type="complex" source="../media/evaluate-performance-performance-fps-highlight.msft.png" alt-text="Graphique FPS" lightbox="../media/evaluate-performance-performance-fps-highlight.msft.png":::
   Graphique **FPS**  
:::image-end:::  

#### <a name="the-frames-section"></a>Section Cadres  

La section **Frames** vous indique exactement la durée d’un cadre particulier.  

Pointez sur un cadre pour afficher une info-bulle avec plus d’informations à son sujet.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-hover.msft.png" alt-text="Pointer sur un cadre" lightbox="../media/evaluate-performance-performance-frames-hover.msft.png":::
   Pointer sur un cadre  
:::image-end:::  

Choisissez un cadre pour afficher plus d’informations sur le cadre dans le **panneau Résumé.**  DevTools présente le cadre sélectionné en bleu.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-summary.msft.png" alt-text="Afficher un cadre dans le panneau Résumé" lightbox="../media/evaluate-performance-performance-frames-summary.msft.png":::
   Afficher un cadre dans le **panneau Résumé**  
:::image-end:::  

### <a name="view-network-requests"></a>Afficher les demandes réseau  

Développez la section **Réseau** pour afficher une cascade de demandes réseau qui se sont produites pendant l’enregistrement.  

:::image type="complex" source="../media/evaluate-performance-performance-network.msft.png" alt-text="Section Réseau" lightbox="../media/evaluate-performance-performance-network.msft.png":::
   Section **Réseau**  
:::image-end:::  

Les demandes sont codées en couleur comme suit :  

*   HTML : Bleu  
*   CSS : Violet  
*   JS : Jaune  
*   Images : vert  
    
Choisissez une demande pour afficher plus d’informations à son sujet dans le **panneau De** synthèse.  Par exemple, dans la **** figure précédente, le panneau Résumé affiche plus d’informations sur la demande bleue sélectionnée dans la section **Réseau.**  

Un carré bleu foncé dans le haut à gauche d’une demande signifie qu’il s’agit d’une demande de priorité supérieure.  Un carré bleu clair signifie une priorité inférieure.  Par exemple, dans la figure précédente, la demande sélectionnée en bleu est de priorité supérieure et la demande verte en dessous est de priorité inférieure.  

Dans la première des figures suivantes, la demande est représentée par une ligne à gauche, une barre au milieu avec une partie sombre et une partie claire, et une ligne à `www.bing.com` droite.  La deuxième des figures suivantes montre la représentation correspondante **** de la même demande dans le panneau Minutage de **l’outil** Réseau.  Voici comment ces deux représentations se maient l’une à l’autre :

*   La ligne de gauche est tout jusqu’au `Connection Start` groupe d’événements, inclus.  En d’autres termes, il s’agit de tout ce qui est `Request Sent` avant , exclusif.  
*   La partie claire de la barre est `Request Sent` et `Waiting (TTFB)` .  
*   La partie sombre de la barre est `Content Download` .  
*   La droite est essentiellement le temps passé à attendre le thread principal.  Cela n’est pas représenté dans le **panneau Minutage.**  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-performance-network.msft.png" alt-text="Représentation de la barre de lignes de la demande www.bing.com ligne" lightbox="../media/evaluate-performance-bing-performance-network.msft.png":::
         Représentation de la demande dans la barre de `www.bing.com` lignes  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-network-timing.msft.png" alt-text="L’outil Réseau" lightbox="../media/evaluate-performance-bing-network-timing.msft.png":::
         **L’outil** Réseau  
: ::image-end:::  
   :::column-end:::
:::row-end:::

### <a name="view-memory-metrics"></a>Afficher les mesures de mémoire  

Activer la case **à** cocher Mémoire pour afficher les mesures de mémoire du dernier enregistrement.  

:::image type="complex" source="../media/evaluate-performance-performance-memory-highlight.msft.png" alt-text="Case à cocher Mémoire" lightbox="../media/evaluate-performance-performance-memory-highlight.msft.png":::
   Case **à** cocher Mémoire  
:::image-end:::  

DevTools affiche un **** nouveau graphique mémoire, au-dessus du **panneau Résumé.**  Il existe également un nouveau graphique sous le **graphique NET,** appelé **TAS**.  Le **graphique HEAP** fournit les mêmes informations que la ligne Tas **JS** dans le **graphique mémoire.**  

:::image type="complex" source="../media/evaluate-performance-performance-memory-chart.msft.png" alt-text="Mesures de mémoire" lightbox="../media/evaluate-performance-performance-memory-chart.msft.png":::
   Mesures de mémoire  
:::image-end:::  

Les lignes de couleur sur le graphique sont m interactives avec les case à cocher colorées au-dessus du graphique.  
Désactivez une case à cocher pour masquer cette catégorie dans le graphique.  

Le graphique affiche uniquement la région de l’enregistrement actuellement sélectionné.  Par exemple, dans la **** figure précédente, le graphique Mémoire affiche uniquement l’utilisation de la mémoire d’environ 400 ms à la marque 1750 ms.  

### <a name="view-the-duration-of-a-portion-of-a-recording"></a>Afficher la durée d’une partie d’un enregistrement  

Lors de l’analyse d’une section telle que **Réseau** ou **Main,** vous avez parfois besoin d’une estimation plus précise de la durée de certains événements.  `Shift`Maintenez, choisissez et maintenez, puis faites glisser vers la gauche ou la droite pour sélectionner une partie de l’enregistrement.  En bas de votre sélection, DevTools indique la durée de cette portion.  

:::image type="complex" source="../media/evaluate-performance-performance-main-duration.msft.png" alt-text="Afficher la durée d’une partie d’un enregistrement" lightbox="../media/evaluate-performance-performance-main-duration.msft.png":::
   Afficher la durée d’une partie d’un enregistrement  
:::image-end:::  

### <a name="view-a-screenshot"></a>Afficher une capture d’écran  

Accédez à [Capture d’écran lors de l’enregistrement](#capture-screenshots-while-recording) pour découvrir comment activer les captures d’écran.  

Pointez sur la **vue d’ensemble** pour afficher une capture d’écran de l’affichage de la page pendant ce moment de l’enregistrement.  La **vue d’ensemble** est la section qui contient les graphiques **UC,** **FPS**et **NET.**  

:::image type="complex" source="../media/evaluate-performance-performance-screenshots-hover.msft.png" alt-text="Afficher une capture d’écran" lightbox="../media/evaluate-performance-performance-screenshots-hover.msft.png":::
   Afficher une capture d’écran  
:::image-end:::  

Vous pouvez également afficher des captures d’écran en choisissant un cadre dans la section **Cadres.**  DevTools affiche une petite version de la capture d’écran dans le **panneau Résumé.**  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview.msft.png" alt-text="Afficher une capture d’écran dans le panneau Résumé" lightbox="../media/evaluate-performance-performance-summary-preview.msft.png":::
   Afficher une capture d’écran dans le **panneau Résumé**  
:::image-end:::  

Choisissez la miniature du panneau Résumé **pour** effectuer un zoom avant sur la capture d’écran.  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview-select.msft.png" alt-text="Zoom sur une capture d’écran à partir du panneau Résumé" lightbox="../media/evaluate-performance-performance-summary-preview-select.msft.png":::
   Zoom sur une capture d’écran à partir du **panneau Résumé**  
:::image-end:::  

### <a name="view-layers-information"></a>Afficher les informations sur les couches  

Pour afficher les informations sur les couches avancées sur un cadre :  

1.  [Activer l’instrumentation de pinceau avancée.](#turn-on-advanced-paint-instrumentation)  
1.  Choisissez un cadre dans la section **Cadres.**  DevTools affiche des informations sur les couches du nouveau panneau **Calques,** à côté du panneau **Journal des** événements.  
    
    :::image type="complex" source="../media/evaluate-performance-layers-all.msft.png" alt-text="Volet Calques" lightbox="../media/evaluate-performance-layers-all.msft.png":::
       Volet **Calques**  
    :::image-end:::  
    
Pointez sur un calque pour le surligner dans le diagramme.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png" alt-text="Surligner un calque" lightbox="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png":::
   Surligner un calque  
:::image-end:::  

Pour déplacer le diagramme :  

*   Choisissez **Pan Mode** \( Pan Mode ![ ](../media/pan-mode-icon.msft.png) \) pour vous déplacer le long des axes X et Y.  
*   Choisissez **Le mode Rotation** \( Mode rotation ![ ](../media/rotate-mode-icon.msft.png) \) pour faire pivoter le long de l’axe Z.  
*   Choisissez **Réinitialiser la transformation** \( ![ Réinitialiser la transformation \) pour rétablir la position ](../media/reset-transform-icon.msft.png) d’origine du diagramme.  
    
### <a name="view-paint-profiler"></a>Afficher le profileur de pinceau  

Pour afficher des informations avancées sur un événement de pinceau :  

1.  [Activer](#turn-on-advanced-paint-instrumentation).  
1.  Choisissez un **Paint** dans la section **Main.**  
    
    :::image type="complex" source="../media/evaluate-performance-paint-profiler.msft.png" alt-text="Panneau Paint profileur" lightbox="../media/evaluate-performance-paint-profiler.msft.png":::
       Panneau **Paint profileur**  
    :::image-end:::  
    
## <a name="analyze-rendering-performance-with-the-rendering-tool"></a>Analyser les performances de rendu à l’aide de l’outil de rendu  

Utilisez les fonctionnalités du panneau **de** rendu pour visualiser les performances de rendu de votre page.  

Pour ouvrir **l’outil de** rendu :  

1.  [Ouvrez le menu Commande.][DevToolsCommandMenu]  
1.  Commencez à taper `Rendering` et sélectionnez `Show Rendering` .  DevTools affiche l’outil **de** rendu en bas de votre fenêtre DevTools.  
    
    :::image type="complex" source="../media/evaluate-performance-console-drawer-rendering.msft.png" alt-text="Outil de rendu" lightbox="../media/evaluate-performance-console-drawer-rendering.msft.png":::
       Outil **de rendu**  
    :::image-end:::  
    
### <a name="view-frames-per-second-in-realtime-with-the-fps-meter"></a>Afficher les images par seconde en temps réel avec la jauge FPS  

La **jauge FPS** est une superposition qui apparaît dans le coin supérieur droit de votre vue.  Il fournit une estimation en temps réel du service FPS à mesure que la page s’exécute.  Pour ouvrir la **jauge FPS**:  

1.  Ouvrez **l’outil de** rendu.  [Analysez les performances de rendu à l’aide de l’outil de rendu.](#analyze-rendering-performance-with-the-rendering-tool)  
1.  Activer la case **à cocher Indicateur FPS.**  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png" alt-text="Indicateur FPS" lightbox="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png":::
       Indicateur **FPS**  
    :::image-end:::  
    
### <a name="view-painting-events-in-realtime-with-paint-flashing"></a>Afficher les événements de dessin en temps réel avec Paint clignotement  

Utilisez Paint clignotement pour obtenir une vue en temps réel de tous les événements de pinceau sur la page.  Chaque fois qu’une partie de la page est peint à nouveau, DevTools souligne cette section en vert.  

Pour activer Paint clignotement, effectuer les actions suivantes.  

1.  Ouvrez **l’outil de** rendu.  Accédez à [Analyser les performances de rendu à l’aide de l’outil de rendu.](#analyze-rendering-performance-with-the-rendering-tool)  
1.  Activer la case **à Paint clignotement.**  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png" alt-text="Paint Clignotement" lightbox="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png":::
       **Paint Clignotement**  
    :::image-end:::  
    
### <a name="view-an-overlay-of-layers-with-layer-borders"></a>Afficher une superposition de couches avec des bordures de calque  

Utilisez **les bordures de** calque pour afficher une superposition de bordures de calque et de vignettes au-dessus de la page.  

Pour activer les bordures de calque, effectuer les actions suivantes :  

1.  Ouvrez **l’outil de** rendu.  Accédez à [Analyser les performances de rendu à l’aide de l’outil de rendu.](#analyze-rendering-performance-with-the-rendering-tool)  
1.  Activer la case **à cocher Bordures** de calque.  
    
    :::image type="complex" source="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png" alt-text="Bordures de calque" lightbox="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png":::
       **Bordures de calque**  
    :::image-end:::  
    
Accédez aux commentaires dans [debug_colors.cc][ChromiumDebugColors] pour obtenir une explication des codages de couleurs.  

### <a name="find-scroll-performance-issues-in-realtime"></a>Rechercher les problèmes de performances de défilement en temps réel  

Utilisez les problèmes de performances de défilement pour identifier les éléments de la page qui ont des écouteurs d’événements liés au défilement qui peuvent nuire aux performances de la page.  
DevTools décrit les éléments potentiellement problématiques dans le teal.  

Pour afficher les problèmes de performances de défilement, effectuer les actions suivantes. 

1.  Ouvrez **l’outil de** rendu.  Accédez à [Analyser les performances de rendu à l’aide de l’outil de rendu.](#analyze-rendering-performance-with-the-rendering-tool)  
1.  Activer la case **à cocher Problèmes de performances de** défilement.  
    
    :::image type="complex" source="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png" alt-text="Des problèmes de performances de défilement indiquent que les objets non soumis à la contrainte de la vue de couche peuvent nuire aux performances de défilement" lightbox="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png":::
       **Des problèmes de performances de** défilement indiquent que les objets non soumis à la contrainte de la vue de couche peuvent nuire aux performances de défilement  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  
[DevToolsCommandMenu]: ../command-menu/index.md#open-the-command-menu "Ouvrez le menu Commande - Exécutez les commandes avec la Microsoft Edge menu de commande DevTools | Documents Microsoft"  
[DevtoolsEvaluatePerformanceGettingStarted]: ./index.md "Commencer à analyser les performances d’exécution | Documents Microsoft"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Démonstration des onglets Activité | glitch"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors.cc - Recherche de code"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
