---
description: Référence sur l’ensemble des méthodes permettant d’enregistrer et d’analyser des performances dans Microsoft Edge DevTools.
title: Référence d’analyse des performances
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: d5b6be92c1419ba880a94c62c3f586a740816622
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230760"
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

# Référence d’analyse des performances  

Cette page est une référence complète des fonctionnalités de Microsoft Edge DevTools liées à l’analyse des performances.  

Naviguez jusqu’à l' [analyse des performances][DevtoolsEvaluatePerformanceGettingStarted] de l’exécution d’un didacticiel dirigé sur l’analyse des performances d’une page à l’aide de [Microsoft Edge devtools][MicrosoftEdgeDevTools].  

## Performance enregistrement  

### Enregistrer les performances d’exécution  

Enregistrez les performances d’exécution lorsque vous souhaitez analyser les performances d’une page en cours d’exécution, plutôt que de procéder au chargement.  

1.  Accédez à la page que vous voulez analyser.  
1.  Sélectionnez l’onglet **performance** dans devtools.  
1.  Cliquez sur **Enregistrer** \ ( ![ icône d’enregistrement ][ImageRecordIcon] \).  
    
    :::image type="complex" source="../media/evaluate-performance-performance-record-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-record-highlight.msft.png":::
       **Record**  
    :::image-end:::  
    
1.  Interagir avec la page.  DevTools enregistre toutes les activités de page résultant de vos interactions.  
1.  Cliquez de nouveau sur **enregistrement** ou sélectionnez **arrêter** pour arrêter l’enregistrement.  
    
### Enregistrer les performances de chargement  

Enregistrez les performances de chargement lorsque vous souhaitez analyser les performances d’une page lors du chargement, plutôt que d’être en cours d’exécution.  

1.  Accédez à la page que vous voulez analyser.  
1.  Ouvrez le panneau **performances** de devtools.  
1.  Sélectionnez **Actualiser la page** \ ( ![ Actualiser la page ][ImageRefreshPageIcon] \).  DevTools enregistre les métriques de performances pendant que la page est actualisée, puis arrête automatiquement l’enregistrement de quelques secondes après la fin de la charge.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-refresh-button.msft.png" alt-text="Actualiser la page" lightbox="../media/evaluate-performance-performance-refresh-button.msft.png":::
       **Actualiser la page**  
    :::image-end:::  
    
DevTools effectue automatiquement un zoom avant sur la partie de l’enregistrement où la majeure partie de l’activité s’est produite.  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed.msft.png" alt-text="Un enregistrement de chargement de page" lightbox="../media/evaluate-performance-performance-refreshed.msft.png":::
   Un enregistrement de chargement de page  
:::image-end:::  

### Capture des captures d’écran lors de l’enregistrement  

Activez la case à cocher **captures d’écran** pour capturer une capture d’écran de chaque image lors de l’enregistrement.  

:::image type="complex" source="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png" alt-text="Case à cocher captures d’écran" lightbox="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png":::
   Case à cocher **captures d’écran**  
:::image-end:::  

Accédez à l' [affichage d’une capture d’écran](#view-a-screenshot) pour savoir comment interagir avec les captures d’écran.  

### Forcer le nettoyage de la mémoire lors de l’enregistrement  

Lors de l’enregistrement d’une page, sélectionnez **collecter le nettoyage** de la mémoire (en-dessous ![ ][ImageCollectGarbageIcon] ) pour forcer le nettoyage de la mémoire.  

:::image type="complex" source="../media/evaluate-performance-performance-collect-garbage-button.msft.png" alt-text="Collecter les nettoyages de la mémoire" lightbox="../media/evaluate-performance-performance-collect-garbage-button.msft.png":::
   Collecter les nettoyages de la mémoire  
:::image-end:::  

### Afficher les paramètres d’enregistrement  

Choisissez **paramètres de capture** \ ( ![ paramètres de capture ][ImageCaptureSettingsIcon] \) pour exposer d’autres paramètres liés à la manière dont devtools capture les enregistrements de performances.  

:::image type="complex" source="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png" alt-text="Section paramètres de capture" lightbox="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png":::
   Section **paramètres de capture**  
:::image-end:::  

### Désactiver les exemples JavaScript  

Par défaut, la section **principale** d’un enregistrement affiche des piles d’appels détaillées des fonctions JavaScript qui ont été appelées lors de l’enregistrement.  Pour désactiver ces piles d’appels:  

1.  Ouvrir le menu **paramètres de capture** .  Accédez à [afficher les paramètres d’enregistrement](#show-recording-settings).  
1.  Activez la case à cocher **Désactiver les exemples JavaScript** .  
1.  Prenez un enregistrement de la page.  
    
Les 2 figures suivantes présentent la différence entre la désactivation et l’activation des exemples JavaScript.  La section **principale** de l’enregistrement est beaucoup plus courte lorsque l’échantillonnage est désactivé, car il omet toutes les piles d’appels JavaScript.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png" alt-text="Un exemple d’enregistrement lorsque les exemples de JS sont désactivés" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png":::
         Un exemple d’enregistrement lorsque les exemples de JS sont désactivés  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png" alt-text="Exemple d’enregistrement lorsque les exemples de JS sont activés" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png":::
         Exemple d’enregistrement lorsque les exemples de JS sont activés  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### Limiter le réseau lors de l’enregistrement  

Pour limiter le réseau lors de l’enregistrement:  

1.  Ouvrir le menu **paramètres de capture** .  Accédez à [afficher les paramètres d’enregistrement](#show-recording-settings).  
1.  Définissez **réseau** sur le niveau de limitation souhaité.  
    
### Limiter le processeur lors de l’enregistrement  

Pour limiter le processeur lors de l’enregistrement:  

1.  Ouvrir le menu **paramètres de capture** .  Accédez à [afficher les paramètres d’enregistrement](#show-recording-settings).  
1.  Définissez **UC** sur le niveau de limitation souhaité.  
    
La limitation est relative aux fonctionnalités de votre ordinateur.  Par exemple, l’option **2x Slowdown** permet à votre processeur de fonctionner 2 fois plus lent que d’habitude.  DevTools ne simulez pas vraiment les UC des appareils mobiles, car l’architecture des appareils mobiles est très différente de celle des ordinateurs de bureau et des ordinateurs portables.  

### Activer l’instrumentation avancée de Paint  

Pour afficher une instrumentation détaillée de Paint:  

1.  Ouvrir le menu **paramètres de capture** .  Accédez à [afficher les paramètres d’enregistrement](#show-recording-settings).  
1.  Cochez la case **activer l’instrumentation avancée de peinture (lente)** .  

Pour plus d’informations sur l’interaction entre les informations de Paint, voir [afficher les couches](#view-layers-information) et afficher le [Générateur de profils Paint](#view-paint-profiler).  

## Enregistrer un enregistrement  

Pour enregistrer un enregistrement, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez **enregistrer le profil**.  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png" alt-text="Enregistrer le profil" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png":::
   **Enregistrer le profil**  
:::image-end:::  

## Charger un enregistrement  

Pour charger un enregistrement, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez **charger le profil**.  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png" alt-text="Profil de chargement" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png":::
   **Profil de chargement**  
:::image-end:::  

## Effacer l’enregistrement précédent  

Après avoir effectué un enregistrement, appuyez sur **effacer l’enregistrement** \ ( ![ icône Effacer l’enregistrement ][ImageClearRecordingIcon] \) pour effacer cet enregistrement du panneau **performances** .  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png" alt-text="Effacer l’enregistrement" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png":::
   **Effacer l’enregistrement**  
:::image-end:::  

## Analyser un enregistrement de performance  

Une fois que vous avez [enregistré des performances d’exécution](#record-runtime-performance) ou enregistré des performances de [chargement](#record-load-performance), le panneau **performance** fournit un grand nombre de données pour l’analyse des performances de ce qui s’est produit.  

### Sélectionner une partie d’un enregistrement  

Faites glisser le pointeur de la souris vers la gauche ou la droite dans la **vue d’ensemble** pour sélectionner une partie d’un enregistrement.  La section **vue d’ensemble** contient les graphiques **fps**, **UC**et **net** .  

:::image type="complex" source="../media/evaluate-performance-performance-zoom-highlighted.msft.png" alt-text="Faites glisser le pointeur de la souris sur la vue d’ensemble pour effectuer un zoom" lightbox="../media/evaluate-performance-performance-zoom-highlighted.msft.png":::
   Faites glisser le pointeur de la souris sur la **vue d’ensemble** pour effectuer un zoom  
:::image-end:::  

Pour sélectionner une partie à l’aide du clavier:  

1.  Choisissez l’arrière-plan de la section **principale** ou de n’importe quelle section en regard de celle-ci, par exemple, **interactions**, **réseau**ou **GPU**.  Ce flux de travail de clavier fonctionne uniquement lorsque l’une de ces sections est activée.  
1.  Utilisez les `W` touches,,, `A` `S` `D` pour effectuer un zoom avant, vous déplacer vers la gauche, effectuer un zoom arrière et vous déplacer à droite, respectivement.  

Pour sélectionner une partie à l’aide d’un pavé tactile, effectuez les actions suivantes.  

1.  Positionnez le pointeur de la souris sur la section **Présentation** ou la section **Détails** .  La section **vue d’ensemble** est la zone contenant les graphiques **fps**, **UC**et **net** .  La section **Détails** représente la zone contenant la section **principale** , la section **interactions** , etc.  
1.  Avec deux doigts, balayez vers le haut pour effectuer un zoom arrière, balayez vers la gauche pour vous déplacer vers la gauche, balayez vers le bas pour effectuer un zoom avant, puis balayez vers la droite pour avancer.  

Pour faire défiler un grand graphique en flamme dans la section **principale** ou sur l’un des voisins, sélectionnez et maintenez le bouton enfoncé tout en faisant glisser vers le haut et vers le bas.  Faites glisser vers la gauche et vers la droite pour déplacer la partie de l’enregistrement sélectionnée.  

### Activités de recherche  

`Control` + `F` `Command` + `F` Pour ouvrir la zone de recherche située en bas du panneau de **performance** , sélectionnez \ (Windows, Linux \) ou \ (MacOS \).  

:::image type="complex" source="../media/evaluate-performance-performance-search-regex.msft.png" alt-text="Zone de recherche" lightbox="../media/evaluate-performance-performance-search-regex.msft.png":::
   Zone de recherche  
:::image-end:::  

Pour parcourir les activités qui correspondent à votre requête:  

*   Utilisez les boutons **précédent** \ ( ![ précédent ][ImagePreviousIcon] \) et **suivant** \ ( ![ suivant ][ImageNextIcon] \).  
*   Sélectionner `Shift` + `Enter` pour sélectionner le précédent ou `Enter` pour en sélectionner un autre.  

Pour modifier les paramètres d’une requête:  

*   Appuyer sur respecter la **casse** (respecter la casse ![ ][ImageSearchCaseIcon] ) pour respecter la casse.  
*   **** ![ ][ImageSearchRegexIcon] Pour utiliser une expression régulière dans votre requête, appuyez sur Regex.  

Pour masquer la zone de recherche, appuyez sur **Annuler**.  

### Afficher l’activité du thread principal  

Utilisez la section **principale** pour afficher l’activité qui s’est produite sur le thread principal de la page.  

:::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Section principale" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
   Section **principale**  
:::image-end:::  

Sélectionnez un événement pour afficher des informations supplémentaires le concernant sous l’onglet **Résumé** .  DevTools souligne l’événement sélectionné.  

:::image type="complex" source="../media/evaluate-performance-performance-summary-me.msft.png" alt-text="Plus d’informations sur la fonction anonyme sous l’onglet Résumé" lightbox="../media/evaluate-performance-performance-summary-me.msft.png":::
   Plus d’informations sur la `anonymous` fonction sous l’onglet **Résumé**  
:::image-end:::  

DevTools représente l’activité du thread principal avec un graphique à flamme.  L’axe x représente l’enregistrement dans le temps.  L’axe y représente la pile d’appels.  Les événements en haut déclenchent les événements situés au-dessous.  

:::image type="complex" source="../media/evaluate-performance-performance-main-flame-chart.msft.png" alt-text="Un graphique en flamme" lightbox="../media/evaluate-performance-performance-main-flame-chart.msft.png":::
   Un graphique en flamme  
:::image-end:::  

Dans l’illustration précédente, un `click` événement a entraîné `Function Call` une `activitytabs.js` 53 sur ligne.  Vous trouverez ci-dessous `Function Call` un avis d’exécution d’une fonction anonyme.  La fonction anonyme demandée `a` , qui a été demandée `wait` `Minor GC` .  

DevTools attribue des couleurs aléatoires aux scripts.  Dans la figure ci-dessus, les demandes de fonction d’un script apparaissent en vert clair.  Les requêtes d’un autre script sont colorées au beige.  Le jaune foncé représente l’activité de création de scripts et l’événement violet représente l’activité de rendu.  Ces événements en jaune et violet plus foncés sont cohérents dans tous les enregistrements.  

Accédez à [Désactiver les exemples JavaScript](#disable-javascript-samples) si vous souhaitez masquer le graphique de flamme détaillé des requêtes JavaScript.  Lorsque les exemples de JS sont désactivés, seuls les événements de haut niveau tels que `Event: click` et `Function Call` de la figure précédente `str` apparaissent.  

### Afficher les activités d’un tableau  

Après avoir enregistré une page, il n’est pas nécessaire de dépendre uniquement de la section **principale** permettant d’analyser les activités.  DevTools fournit également trois vues tabulaires pour l’analyse des activités.  Chaque affichage vous offre une perspective différente des activités:  

*   Pour afficher les activités racines qui génèrent le plus de tâches, utilisez [l’onglet arborescence des appels](#the-call-tree-tab).  
*   Pour afficher les activités pour lesquelles le plus de temps est passé directement, utilisez [l’onglet Bottom-Up](#the-bottom-up-tab).  
*   Si vous voulez afficher les activités dans l’ordre dans lequel elles se sont produites lors de l’enregistrement, utilisez [l’onglet journal des événements](#the-event-log-tab).  
    
> [!NOTE]
> Les trois sections suivantes se réfèrent à la même démonstration.  Exécutez la démonstration vous-même dans les [onglets activité][ActivityTabsDemo].  

#### Activités racines  

Voici une description du concept d' **activités racines** mentionné dans les sections de l’onglet **arborescence des appels** , de **bas en haut** et **Journal des événements** .  

Les activités racines peuvent entraîner le fonctionnement du navigateur.  Par exemple, lorsque vous choisissez une page Web, le navigateur exécute une `Event` activité en tant qu’activité racine.  Cela `Event` risque de provoquer l’exécution d’un gestionnaire et ainsi de suite.  

Dans le graphique en flamme de la section **principale** , les activités racines se trouvent en haut du graphique.  Dans les onglets **arborescence des appels** et **Journal des événements** , les activités racines sont les éléments de niveau supérieur.  

Accédez à [l’onglet arborescence des appels](#the-call-tree-tab) pour obtenir un exemple d’activités racines.  

#### Onglet arborescence des appels  

Utilisez l’onglet **arborescence des appels** pour afficher les [activités racines](#root-activities) qui sont à l’origine du problème.  

L’onglet **arborescence des appels** affiche uniquement les activités effectuées au cours de la partie sélectionnée de l’enregistrement.  Naviguez jusqu’à [Sélectionner une portion d’un enregistrement](#select-a-portion-of-a-recording) pour savoir comment sélectionner des parties.  

:::image type="complex" source="../media/evaluate-performance-performance-call-tree.msft.png" alt-text="Onglet arborescence des appels" lightbox="../media/evaluate-performance-performance-call-tree.msft.png":::
   Onglet **arborescence des appels**  
:::image-end:::  

Dans l’illustration précédente, le niveau supérieur des éléments de la colonne **Activity** , par exemple, `Evaluate Script` les `Parse HTML` activités racines.  L’imbrication représente la pile d’appels.  Par exemple, dans l’illustration précédente, `Parse HTML` ce qui a provoqué `Evaluate Script` `Compile Script` et `(anonymous)` .  

Le **temps libre** représente le temps passé directement dans cette activité.  **Durée totale** représente le temps passé à cette activité ou à un des enfants.  

Choisissez **temps libre**, **durée totale**ou **activité** pour trier le tableau selon la colonne.  

Utilisez la zone de texte **filtre** pour filtrer les événements par nom d’activité.  

Par défaut, le menu de **regroupement** a la valeur **aucun regroupement**.  Utilisez le menu de **regroupement** pour trier la table d’activité en fonction de différents critères.  

Pour **** afficher ![ ][ImageShowHeaviestStackIcon] une autre table à droite de la table **Activity** , sélectionnez Afficher la pile la plus lourde.  Choisissez une activité pour remplir la table des piles les plus **lourdes** .  La table des piles les plus **lourdes** affiche les enfants de l’activité sélectionnée qui ont duré le plus longtemps.  

#### Onglet Bottom-Up  

Utilisez l’onglet **inférieur** pour afficher les activités qui consomment directement le plus de temps dans l’agrégat.  

L’onglet **inférieur** affiche uniquement les activités effectuées au cours de la partie sélectionnée de l’enregistrement.  Naviguez jusqu’à [Sélectionner une portion d’un enregistrement](#select-a-portion-of-a-recording) pour savoir comment sélectionner des parties.  

:::image type="complex" source="../media/evaluate-performance-performance-bottoms-up.msft.png" alt-text="Onglet Bottom-Up" lightbox="../media/evaluate-performance-performance-bottoms-up.msft.png":::
   Onglet **inférieur**  
:::image-end:::  

Dans le graphique en forme de flamme **de la figure** précédente, naviguez jusqu’à ce que presque en tout le temps soit passé `Parse HTML` .  Dans l’onglet **inférieur** de la figure précédente, l’activité supérieure `Parse HTML` .  <!--In the flame chart of the previous figure, the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  Accédez à l’onglet inférieur vers le **haut** , l’activité la plus coûteuse suivante `Layout` .  

La colonne de **temps libre** représente le temps agrégé passé directement dans cette activité, sur l’ensemble des occurrences.  

La colonne **temps total** représente le temps agrégé dépensé dans cette activité ou sur n’importe quel enfant.  

#### Onglet journal des événements  

Utilisez l’onglet **Journal des événements** pour afficher les activités dans l’ordre dans lequel elles se sont produites lors de l’enregistrement.  

L’onglet **Journal des événements** affiche uniquement les activités effectuées au cours de la partie sélectionnée de l’enregistrement.  Naviguez jusqu’à [Sélectionner une portion d’un enregistrement](#select-a-portion-of-a-recording) pour savoir comment sélectionner des parties.  

:::image type="complex" source="../media/evaluate-performance-performance-event-log.msft.png" alt-text="Onglet journal des événements" lightbox="../media/evaluate-performance-performance-event-log.msft.png":::
   Onglet **Journal des événements**  
:::image-end:::  

La colonne **heure de début** représente le point auquel cette activité a commencé, par rapport au début de l’enregistrement.  Par exemple, l’heure de début de `175.7 ms` l’élément sélectionné dans la figure précédente signifie que l’activité a démarré 175,7 ms après le début de l’enregistrement.  

La colonne **temps libre** représente le temps passé directement dans cette activité.  

Le **nombre total** de colonnes durée représente le temps passé directement dans cette activité ou dans n’importe quel enfant.  

Sélectionnez **heure de début**, **durée automatique**ou **durée totale** pour trier le tableau selon la colonne.

Utilisez la zone de texte **filtre** pour filtrer les activités par nom.  

Utilisez le menu **durée** pour filtrer les activités ayant eu moins de 1 ms ou 15 ms.  Par défaut, le menu **durée** est défini sur **tout**, ce qui signifie que toutes les activités sont affichées.  

Désactivez les cases à cocher **chargement**, **script**, **rendu**ou **peinture** pour filtrer toutes les activités de ces catégories.  

### Afficher l’activité GPU  

Afficher l’activité GPU dans la section **GPU** .  

:::image type="complex" source="../media/evaluate-performance-performance-gpu-zoomed.msft.png" alt-text="Section GPU" lightbox="../media/evaluate-performance-performance-gpu-zoomed.msft.png":::
   Section **GPU**  
:::image-end:::  

### Afficher les activités pixellisées  

Affichez les activités pixellisées dans la section **Raster** .  

:::image type="complex" source="../media/evaluate-performance-performance-raster.msft.png" alt-text="Section raster" lightbox="../media/evaluate-performance-performance-raster.msft.png":::
   Section **Raster**  
:::image-end:::  

### Afficher les interactions  

Utilisez la section **interactions** pour rechercher et analyser les interactions utilisateur qui se sont produites lors de l’enregistrement.  

:::image type="complex" source="../media/evaluate-performance-performance-interactions-animation.msft.png" alt-text="Section interactions" lightbox="../media/evaluate-performance-performance-interactions-animation.msft.png":::
   Section **interactions**  
:::image-end:::  

Une ligne rouge en bas d’une interaction représente le temps passé à attendre le thread principal.  

Choisissez une interaction pour afficher des informations supplémentaires sur celle-ci sous l’onglet **Résumé** .  

### Analyser les images par seconde (FPS)  

DevTools offre de nombreuses façons d’analyser les images par seconde:  

*   Utilisez [le graphique fps](#the-fps-chart) pour obtenir une vue d’ensemble des images par seconde au fil de la durée de l’enregistrement.  
*   Utilisez [la section cadres](#the-frames-section) pour afficher la durée d’une image particulière.  
*   Utilisez le **compteur fps** pour une estimation en temps réel de FPS lors de l’exécution de la page.  Naviguez jusqu’à [l’affichage des images par seconde en temps réel à l’aide du vumètre fps](#view-frames-per-second-in-realtime-with-the-fps-meter).  
    
#### Graphique FPS  

Le graphique **fps** fournit une vue d’ensemble de la fréquence d’images sur la durée d’un enregistrement.  En règle générale, plus la barre verte est élevée, plus la fréquence d’images est élevée.  

Une barre rouge au-dessus du graphique **fps** est une alerte indiquant que le taux d’images a été interrompu comme faible et qu’il a probablement été lésé par l’utilisateur.  

:::image type="complex" source="../media/evaluate-performance-performance-fps-highlight.msft.png" alt-text="Graphique FPS" lightbox="../media/evaluate-performance-performance-fps-highlight.msft.png":::
   Graphique **fps**  
:::image-end:::  

#### Section cadres  

La section **trames** vous indique exactement le temps qu’une image donnée a duré.  

Pointez sur un cadre pour afficher une info-bulle contenant des informations supplémentaires à son sujet.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-hover.msft.png" alt-text="Survol d’un cadre" lightbox="../media/evaluate-performance-performance-frames-hover.msft.png":::
   Survol d’un cadre  
:::image-end:::  

Choisissez une image pour afficher davantage d’informations sur le cadre sous l’onglet **Résumé** .  DevTools plan le cadre sélectionné en bleu.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-summary.msft.png" alt-text="Afficher un cadre sous l’onglet Résumé" lightbox="../media/evaluate-performance-performance-frames-summary.msft.png":::
   Afficher un cadre sous l’onglet **Résumé**  
:::image-end:::  

### Afficher les requêtes réseau  

Développez la section **réseau** pour afficher une cascade de requêtes réseau qui se sont produites lors de l’enregistrement.  

:::image type="complex" source="../media/evaluate-performance-performance-network.msft.png" alt-text="Section réseau" lightbox="../media/evaluate-performance-performance-network.msft.png":::
   Section **réseau**  
:::image-end:::  

Les requêtes sont codées en couleur comme suit:  

*   HTML: bleu  
*   CSS: pourpre  
*   JS: jaune  
*   Images: vert  
    
Choisissez une demande pour afficher davantage d’informations sur celle-ci sous l’onglet **Résumé** .  Par exemple, dans l’illustration précédente, l’onglet **Résumé** affiche des informations supplémentaires sur la requête bleue sélectionnée dans la section **réseau** .  

Dans le coin supérieur gauche d’une demande, un carré plus foncé est une demande de priorité élevée.  Le carré bleu plus clair correspond à un niveau de priorité inférieur.  Par exemple, dans l’illustration précédente, la requête bleue, sélectionnée est d’une priorité plus élevée et celle du vert au-dessous, de priorité inférieure.  

Dans le 1er des figures suivantes, la requête pour `www.bing.com` est représentée par une ligne située sur la gauche, une barre au milieu avec une partie sombre et une partie claire, et une ligne à droite.  Dans la deuxième des figures suivantes, la représentation correspondante de la même demande apparaît dans l’onglet **minutage** du panneau **réseau** .  Voici à quoi correspondent les deux représentations suivantes:

*   La ligne gauche représente tout ce qui concerne le `Connection Start` groupe d’événements compris.  En d’autres termes, il s’agit de tout ce qui est auparavant `Request Sent` , exclusif.  
*   La partie claire de la barre est `Request Sent` et `Waiting (TTFB)` .  
*   La partie sombre de la barre est `Content Download` .  
*   La ligne droite correspond essentiellement au délai passé pour le thread principal.  Cette opération n’est pas représentée dans l’onglet **minutage** .  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-performance-network.msft.png" alt-text="Représentation de la barre de lignes de la requête www.bing.com" lightbox="../media/evaluate-performance-bing-performance-network.msft.png":::
         Représentation de la barre de lignes de la `www.bing.com` requête  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-network-timing.msft.png" alt-text="Outil réseau" lightbox="../media/evaluate-performance-bing-network-timing.msft.png":::
         Outil **réseau**  
:::: image-fin:::  
   :::column-end:::
:::row-end:::

### Afficher les métriques de mémoire  

Activez la case à cocher **mémoire** pour afficher les mesures de mémoire du dernier enregistrement.  

:::image type="complex" source="../media/evaluate-performance-performance-memory-highlight.msft.png" alt-text="Case à cocher mémoire" lightbox="../media/evaluate-performance-performance-memory-highlight.msft.png":::
   Case à cocher **mémoire**  
:::image-end:::  

DevTools affiche un nouveau graphique **mémoire** , au-dessus de l’onglet **Résumé** .  Il existe également un nouveau graphique sous le graphique **net** , appelé **tas**.  Le graphique de **tas** fournit les mêmes informations que la ligne de segment de **mémoire** **js** dans le graphique mémoire.  

:::image type="complex" source="../media/evaluate-performance-performance-memory-chart.msft.png" alt-text="Métriques de mémoire" lightbox="../media/evaluate-performance-performance-memory-chart.msft.png":::
   Métriques de mémoire  
:::image-end:::  

Les lignes de couleur sur le graphique correspondent aux cases à cocher en plus de la couleur du graphique.  
Désactivez une case à cocher pour masquer cette catégorie dans le graphique.  

Le graphique affiche uniquement la zone de l’enregistrement actuellement sélectionné.  Par exemple, dans l’illustration précédente, le graphique **mémoire** affiche uniquement l’utilisation de la mémoire de la marque 400 ms au 1750 ms.  

### Affichage de la durée d’une portion d’un enregistrement  

Lors de l’analyse d’une section comme **Network** ou **principal**, il est possible que vous ayez besoin d’une estimation plus précise de la durée de certains événements.  Maintenez la touche enfoncée, `Shift` puis faites glisser vers la gauche ou la droite pour sélectionner une partie de l’enregistrement.  Dans la partie inférieure de votre sélection, DevTools indique la durée de la partie.  

:::image type="complex" source="../media/evaluate-performance-performance-main-duration.msft.png" alt-text="Affichage de la durée d’une portion d’un enregistrement" lightbox="../media/evaluate-performance-performance-main-duration.msft.png":::
   Affichage de la durée d’une portion d’un enregistrement  
:::image-end:::  

### Affichage d’une capture d’écran  

Pour plus d’informations sur l’activation des captures d’écran, accédez à la section capturer les captures d' [écran lors de l’enregistrement](#capture-screenshots-while-recording) .  

Placez le pointeur de la souris sur la **vue d’ensemble** pour afficher une capture d’écran illustrant l’apparence de la page pendant ce moment de l’enregistrement.  La section **vue d’ensemble** contient les graphiques **UC**, **fps**et **net** .  

:::image type="complex" source="../media/evaluate-performance-performance-screenshots-hover.msft.png" alt-text="Affichage d’une capture d’écran" lightbox="../media/evaluate-performance-performance-screenshots-hover.msft.png":::
   Affichage d’une capture d’écran  
:::image-end:::  

Vous pouvez également afficher les captures d’écran en choisissant une image dans la section **trames** .  DevTools affiche une version miniature de la capture d’écran sous l’onglet **Résumé** .  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview.msft.png" alt-text="Affichage d’une capture d’écran sous l’onglet Résumé" lightbox="../media/evaluate-performance-performance-summary-preview.msft.png":::
   Affichage d’une capture d’écran sous l’onglet **Résumé**  
:::image-end:::  

Pour effectuer un zoom avant dans la capture d’écran, cliquez sur la miniature sous l’onglet **Résumé** .  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview-select.msft.png" alt-text="Effectuer un zoom avant sur une capture d’écran à partir de l’onglet Résumé" lightbox="../media/evaluate-performance-performance-summary-preview-select.msft.png":::
   Effectuer un zoom avant sur une capture d’écran à partir de l’onglet **Résumé**  
:::image-end:::  

### Afficher les informations sur les couches  

Pour afficher des informations sur les couches avancées d’une image:  

1.  [Activez l’instrumentation avancée de Paint](#turn-on-advanced-paint-instrumentation).  
1.  Sélectionnez une image dans la section **cadre** .  DevTools affiche des informations sur les calques sous l’onglet nouveau **calques** , en regard de l’onglet **Journal des événements** .  
    
    :::image type="complex" source="../media/evaluate-performance-layers-all.msft.png" alt-text="Volet couches" lightbox="../media/evaluate-performance-layers-all.msft.png":::
       Volet **couches**  
    :::image-end:::  
    
Pointez sur un calque pour le mettre en surbrillance dans le diagramme.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png" alt-text="Mettre un calque en surbrillance" lightbox="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png":::
   Mettre un calque en surbrillance  
:::image-end:::  

Pour déplacer le diagramme:  

*   Sélectionnez **mode panoramique** \ ( ![ mode panoramique ][ImagePanModeIcon] \) pour vous déplacer le long des axes X et Y.  
*   **** ![ ][ImageRotateModeIcon] Pour faire pivoter le long de l’axe Z, sélectionnez mode de rotation.  
*   Sélectionnez **Réinitialiser la transformation** \ ( ![ Réinitialiser la transformation ][ImageResetTransformIcon] \) pour rétablir la position d’origine du diagramme.  
    
### Afficher le générateur de dessin Paint  

Pour afficher des informations détaillées sur un événement Paint:  

1.  [Activez](#turn-on-advanced-paint-instrumentation).  
1.  Sélectionnez un événement **Paint** dans la section **principale** .  
    
    :::image type="complex" source="../media/evaluate-performance-paint-profiler.msft.png" alt-text="Onglet Paint Profiler1.1" lightbox="../media/evaluate-performance-paint-profiler.msft.png":::
       Onglet **Paint Profiler1.1**  
    :::image-end:::  
    
## Analyser les performances de rendu à l’aide de l’onglet rendu  

Utilisez les fonctionnalités de l’onglet **rendu** pour visualiser les performances de rendu de votre page.  

Pour ouvrir l’onglet **rendu** :  

1.  [Ouvrir le menu de commandes][DevToolsCommandMenu].  
1.  Commencez à taper `Rendering` et sélectionnez `Show Rendering` .  DevTools affiche l’onglet **rendu** en bas de votre fenêtre devtools.  
    
    :::image type="complex" source="../media/evaluate-performance-console-drawer-rendering.msft.png" alt-text="Onglet rendu" lightbox="../media/evaluate-performance-console-drawer-rendering.msft.png":::
       Onglet **rendu**  
    :::image-end:::  
    
### Afficher les images par seconde en temps réel avec le compteur FPS  

Le **compteur fps** est une superposition qui s’affiche dans le coin supérieur droit de votre fenêtre d’affichage.  Il fournit une estimation en temps réel de FPS lors de l’exécution de la page.  Pour ouvrir le **compteur fps**:  

1.  Ouvrez l’onglet **rendu** .  Na [analyse des performances de rendu à l’aide de l’onglet rendu](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Activez la case à cocher **vumètre** .  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png" alt-text="Vumètre FPS" lightbox="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png":::
       **Vumètre fps**  
    :::image-end:::  
    
### Afficher les événements de peinture en temps réel avec le clignotement de la peinture  

Utilisez la fonction Paint clignotante pour obtenir une vue en temps réel de tous les événements de peinture sur la page.  Dès qu’une partie de la page est de nouveau peinte, DevTools la place en vert.  

Pour activer le clignotement de Paint, effectuez les actions suivantes.  

1.  Ouvrez l’onglet **rendu** .  Naviguez jusqu’à [l’analyse des performances de rendu avec l’onglet rendu](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Activez la case à cocher **Paint clignotant** .  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png" alt-text="Paint clignotant" lightbox="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png":::
       **Paint clignotant**  
    :::image-end:::  
    
### Afficher une superposition de calques avec des bordures de calque  

Utilisez les **bordures de calque** pour afficher une superposition des bordures et des vignettes du calque en haut de la page.  

Pour activer les bordures de calque, procédez comme suit:  

1.  Ouvrez l’onglet **rendu** .  Naviguez jusqu’à [l’analyse des performances de rendu avec l’onglet rendu](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Activez la case à cocher **bordures de calque** .  
    
    :::image type="complex" source="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png" alt-text="Bordures de calque" lightbox="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png":::
       **Bordures de calque**  
    :::image-end:::  
    
Accédez aux commentaires figurant dans [debug_colors. cc][ChromiumDebugColors] pour obtenir une description des codes de couleur.  

### Rechercher des problèmes de performances de défilement en temps réel  

Utilisez des problèmes de performances de défilement pour identifier les éléments de la page qui comportent des écouteurs d’événements liés au défilement qui peuvent nuire aux performances de la page.  
DevTools souligne les éléments potentiellement posant problème en bleu-vert.  

Pour afficher les problèmes de performances de défilement, effectuez les actions suivantes. 

1.  Ouvrez l’onglet **rendu** .  Naviguez jusqu’à [l’analyse des performances de rendu avec l’onglet rendu](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Activez la case à cocher **problèmes de performances de défilement** .  
    
    :::image type="complex" source="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png" alt-text="Les problèmes de performances de défilement indiquent que les objets dotés de l’affichage sans calque risquent de nuire aux performances de défilement" lightbox="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png":::
       Les **problèmes de performances de défilement** indiquent que les objets dotés de l’affichage sans calque risquent de nuire aux performances de défilement  
    :::image-end:::  
    
## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureSettingsIcon]: ../media/capture-settings-icon.msft.png  
[ImageClearRecordingIcon]: ../media/clear-recording-icon.msft.png  
[ImageCollectGarbageIcon]: ../media/collect-garbage-icon.msft.png  
[ImageNextIcon]: ../media/next-icon.msft.png  
[ImagePanModeIcon]: ../media/pan-mode-icon.msft.png  
[ImagePreviousIcon]: ../media/previous-icon.msft.png  
[ImageRecordIcon]: ../media/record-icon.msft.png
[ImageRefreshPageIcon]: ../media/refresh-page-icon.msft.png  
[ImageResetTransformIcon]: ../media/reset-transform-icon.msft.png  
[ImageRotateModeIcon]: ../media/rotate-mode-icon.msft.png  
[ImageSearchCaseIcon]: ../media/search-case-icon.msft.png  
[ImageSearchRegexIcon]: ../media/search-regex-icon.msft.png  
[ImageShowHeaviestStackIcon]: ../media/show-heaviest-stack-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  
[DevToolsCommandMenu]: ../command-menu/index.md#open-the-command-menu "Ouvrez le menu de commandes et exécutez les commandes à l’aide du menu de commandes Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsEvaluatePerformanceGettingStarted]: ./index.md "Prendre en main l’analyse des performances d’exécution | Documents Microsoft"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Démo des onglets activité | problème"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors. cc-recherche de code"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
