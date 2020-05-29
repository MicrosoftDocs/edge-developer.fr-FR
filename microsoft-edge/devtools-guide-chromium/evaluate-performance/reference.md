---
title: Référence d’analyse des performances
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: acd6e3e68f89096cf80c08f0d0c3430ab31eaec1
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611747"
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

Pour plus d’informations sur l’analyse des performances d’une page à l’aide de [Microsoft Edge devtools][MicrosoftEdgeDevTools], voir mise [en route][DevtoolsEvaluatePerformanceGettingStarted] de l’analyse des performances de l’exécution d’une page.  

## Performance enregistrement   

### Enregistrer les performances d’exécution   

Enregistrez les performances d’exécution lorsque vous souhaitez analyser les performances d’une page en cours d’exécution, plutôt que de procéder au chargement.  

1.  Accédez à la page que vous voulez analyser.  
1.  Cliquez sur l’onglet **performance** dans devtools.  
1.  Cliquez sur **Enregistrer** l' ![ enregistrement ][ImageRecordIcon] .  
    
    > ##### Figure1  
    > **Record**  
    > ![Record][ImageRecord]  

1.  Interagir avec la page.  DevTools enregistre toutes les activités de page résultant de vos interactions.  
1.  Cliquez de nouveau sur **Enregistrer** ou cliquez sur **arrêter** pour arrêter l’enregistrement.  

### Enregistrer les performances de chargement   

Enregistrez les performances de chargement lorsque vous souhaitez analyser les performances d’une page lors du chargement, plutôt que d’être en cours d’exécution.  

1.  Accédez à la page que vous voulez analyser.  
1.  Ouvrez le panneau **performances** de devtools.  
1.  Cliquez sur **Actualiser** la page ![ Actualiser la page ][ImageRefreshPageIcon] .  DevTools enregistre les métriques de performances pendant que la page est actualisée, puis arrête automatiquement l’enregistrement de quelques secondes après la fin de la charge.  
    
    > ##### Figure 2  
    > **Actualiser la page**  
    > ![Actualiser la page][ImageRefreshPage]  

DevTools effectue automatiquement un zoom avant sur la partie de l’enregistrement où la majeure partie de l’activité s’est produite.  

> ##### Figure3  
> Un enregistrement de chargement de page  
> ![Un enregistrement de chargement de page][ImageLoadRecording]  

### Capture des captures d’écran lors de l’enregistrement   

Activez la case à cocher **captures d’écran** pour capturer une capture d’écran de chaque image lors de l’enregistrement.  

> ##### Figure 4  
> Case à cocher **captures d’écran**  
> ![Case à cocher captures d’écran][ImageScreenshots]  

Pour plus d’informations sur l’interaction avec les captures d’écran, voir [afficher une capture d’écran](#view-a-screenshot) .  

### Forcer le nettoyage de la mémoire lors de l’enregistrement   

Pendant que vous enregistrez une page, cliquez sur **collecter** le nettoyage de la mémoire ![ ][ImageCollectGarbageIcon] pour forcer le nettoyage de la mémoire.  

> ##### Figure 5  
> Collecter les nettoyages de la mémoire  
> ![Collecter les nettoyages de la mémoire][ImageCollectGarbage]  

### Afficher les paramètres d’enregistrement   

Cliquez sur **paramètres** ![ de capture ][ImageCaptureSettingsIcon] pour afficher d’autres paramètres liés à la manière dont devtools capture les enregistrements de performances.  

> ##### Figure 6  
> Section **paramètres de capture**  
> ![Section paramètres de capture][ImageCaptureSettings]  

### Désactiver les exemples JavaScript   

Par défaut, la section **principale** d’un enregistrement affiche des piles d’appels détaillées des fonctions JavaScript qui ont été appelées lors de l’enregistrement.  Pour désactiver ces piles d’appels:  

1.  Ouvrir le menu **paramètres de capture** .  Voir [afficher les paramètres d’enregistrement](#show-recording-settings).  
1.  Activez la case à cocher **Désactiver les exemples JavaScript** .  
1.  Prenez un enregistrement de la page.  

La [figure 7](#figure-7) et la [figure 8](#figure-8) montrent la différence entre la désactivation et l’activation des exemples JavaScript.  La section **principale** de l’enregistrement est beaucoup plus courte lorsque l’échantillonnage est désactivé, car il omet toutes les piles d’appels JavaScript.  

> ##### Figure 7  
> Un exemple d’enregistrement lorsque les exemples de JS sont désactivés  
> ![Un exemple d’enregistrement lorsque les exemples de JS sont désactivés][ImageJSSamplesDisabled]  

> ##### Figure8  
> Exemple d’enregistrement lorsque les exemples de JS sont activés  
> ![Exemple d’enregistrement lorsque les exemples de JS sont activés][ImageJSSamplesEnabled]  

### Limiter le réseau lors de l’enregistrement   

Pour limiter le réseau lors de l’enregistrement:  

1.  Ouvrir le menu **paramètres de capture** .  Voir [afficher les paramètres d’enregistrement](#show-recording-settings).  
1.  Définissez **réseau** sur le niveau de limitation souhaité.  

### Limiter le processeur lors de l’enregistrement   

Pour limiter le processeur lors de l’enregistrement:  

1.  Ouvrir le menu **paramètres de capture** .  Voir [afficher les paramètres d’enregistrement](#show-recording-settings).  
1.  Définissez **UC** sur le niveau de limitation souhaité.  

La limitation est relative aux fonctionnalités de votre ordinateur.  Par exemple, l’option **2x Slowdown** permet à votre processeur de fonctionner 2 fois plus lent que d’habitude.  DevTools ne simulez pas vraiment les UC des appareils mobiles, car l’architecture des appareils mobiles est très différente de celle des ordinateurs de bureau et des ordinateurs portables.  

### Activer l’instrumentation avancée de peinture   

Pour afficher une instrumentation détaillée de Paint:  

1.  Ouvrir le menu **paramètres de capture** .  Voir [afficher les paramètres d’enregistrement](#show-recording-settings).  
1.  Cochez la case **activer l’instrumentation avancée de peinture (lente)** .  

Pour plus d’informations sur l’interaction avec les informations de Paint, voir [afficher les couches](#view-layers-information) et afficher le [Générateur de profils Paint](#view-paint-profiler).  

## Enregistrer un enregistrement   

Pour enregistrer un enregistrement, cliquez avec le bouton droit et sélectionnez **enregistrer le profil**.  

> ##### Figure9  
> **Enregistrer le profil**  
> ![Enregistrer le profil][ImageSaveProfile]  

## Charger un enregistrement   

Pour charger un enregistrement, cliquez avec le bouton droit et sélectionnez **charger le profil**.  

> ##### Figure10  
> **Profil de chargement**  
> ![Profil de chargement][ImageLoadProfile]  

## Effacer l’enregistrement précédent   

Une fois l’enregistrement terminé, cliquez sur **effacer l'** enregistrement effacer l’enregistrement ![ ][ImageClearRecordingIcon] pour effacer cet enregistrement du panneau **performances** .  

> ##### Figure11  
> Effacer l’enregistrement  
> ![Effacer l’enregistrement][ImageClearRecording]  

## Analyser un enregistrement de performance   

Une fois que vous avez [enregistré des performances d’exécution](#record-runtime-performance) ou enregistré des performances de [chargement](#record-load-performance), le panneau **performance** fournit un grand nombre de données pour l’analyse des performances de ce qui s’est produit.  

### Sélectionner une partie d’un enregistrement   

Faites glisser le pointeur de la souris vers la gauche ou la droite dans la **vue d’ensemble** pour sélectionner une partie d’un enregistrement.  La section **vue d’ensemble** contient les graphiques **fps**, **UC**et **net** .  

> ##### Figure12  
> Faire glisser la souris sur la vue d’ensemble pour effectuer un zoom  
> ![Faire glisser la souris sur la vue d’ensemble pour effectuer un zoom][ImageZoom]  

Pour sélectionner une partie à l’aide du clavier:  

1.  Cliquez sur l’arrière-plan de la section **principale** ou de n’importe quelle section en regard de celle-ci, comme **interactions**, **réseau**ou **GPU**.  Ce flux de travail de clavier fonctionne uniquement lorsque l’une de ces sections est activée.  
1.  Utilisez les `W` touches,,, `A` `S` `D` pour effectuer un zoom avant, vous déplacer vers la gauche, effectuer un zoom arrière et vous déplacer à droite, respectivement.  

Pour sélectionner une partie à l’aide d’une pavé tactile:  

1.  Positionnez le pointeur de la souris sur la section **Présentation** ou la section **Détails** .  La section **vue d’ensemble** est la zone contenant les graphiques **fps**, **UC**et **net** .  La section **Détails** représente la zone contenant la section **principale** , la section **interactions** , etc.  
1.  Avec deux doigts, balayez vers le haut pour effectuer un zoom arrière, balayez vers la gauche pour vous déplacer vers la gauche, balayez vers le bas pour effectuer un zoom avant, puis balayez vers la droite pour avancer.  

Pour faire défiler un grand graphique en flamme dans la section **principale** ou sur l’un des voisins, cliquez et maintenez le bouton enfoncé tout en faisant glisser le curseur vers le haut et le bas.  Faites glisser vers la gauche et vers la droite pour déplacer la partie de l’enregistrement sélectionnée.  

### Activités de recherche   

`Control` + `F` `Command` + `F` Pour ouvrir la zone de recherche située en bas du panneau de **performance** , appuyez sur \ (Windows \) ou \ (MacOS \).  

> ##### Figure13  
> Utilisation de Regex dans la zone de recherche située en bas de la fenêtre pour rechercher les activités qui commencent par `E`  
> ![Zone de recherche][ImageSearch]  

Pour parcourir les activités qui correspondent à votre requête:  

*   Utilisez les **Previous** ![ boutons précédent ][ImagePreviousIcon] et **suivant** ![ ][ImageNextIcon] .  
*   Appuyez `Shift` + `Enter` pour sélectionner le précédent ou `Enter` pour en sélectionner un autre.  

Pour modifier les paramètres d’une requête:  

*   Respect **Case sensitive** ![ ][ImageSearchCaseIcon] de la casse en tenant compte de la casse.  
*   Appuyez **sur Regex Regex** ![ ][ImageSearchRegexIcon] pour utiliser une expression régulière dans votre requête.  

Pour masquer la zone de recherche, appuyez sur **Annuler**.  

### Afficher l’activité du thread principal   

Utilisez la section **principale** pour afficher l’activité qui s’est produite sur le thread principal de la page.  

> ##### Figure14  
> Section **principale**  
> ![Section principale][ImageMain]  

Cliquez sur un événement pour afficher des informations supplémentaires le concernant sous l’onglet **Résumé** .  DevTools souligne l’événement sélectionné.  

> ##### Figure15  
> Plus d’informations sur la `anonymous` fonction sous l’onglet **Résumé**  
> ![Plus d’informations sur la fonction anonyme sous l’onglet Résumé][ImageMainEventSummary]  

DevTools représente l’activité du thread principal avec un graphique à flamme.  L’axe x représente l’enregistrement dans le temps.  L’axe y représente la pile d’appels.  Les événements en haut déclenchent les événements situés au-dessous.  

> ##### Figure16  
> Graphique à flamme dans la section **principale**  
> ![Un graphique en flamme][ImageFlameChart]  

Dans la [figure 16](#figure-16), un `click` événement a entraîné une `Function Call` `activitytabs.js` 53 sur ligne.  `Function Call`Vous pouvez voir ci-dessous qu’une fonction anonyme a été appelée.  Fonction anonyme appelée, qui a été appelée `a` `wait` `Minor GC` .  

DevTools attribue des couleurs aléatoires aux scripts.  Dans la [figure 16](#figure-16), les appels de fonction à partir d’un script apparaissent en vert clair.  Les appels d’un autre script sont de couleur beige.  Le jaune foncé représente l’activité de création de scripts et l’événement violet représente l’activité de rendu.  Ces événements en jaune et violet plus foncés sont cohérents dans tous les enregistrements.  

Pour masquer le graphique de flamme d’appels JavaScript, voir [Désactiver les exemples JavaScript](#disable-javascript-samples) .  Lorsque les exemples de JS sont désactivés, vous ne voyez que les événements de haut niveau, par exemple `Event: click` et `Function Call` de la [figure 16](#figure-16).  

### Afficher les activités d’un tableau   

Après avoir enregistré une page, il n’est pas nécessaire de dépendre uniquement de la section **principale** permettant d’analyser les activités.  DevTools fournit également trois vues tabulaires pour l’analyse des activités.  Chaque affichage vous offre une perspective différente des activités:  

*   Pour afficher les activités racines qui génèrent le plus de tâches, utilisez [l’onglet **arborescence des appels** ](#the-call-tree-tab).  
*   Pour afficher les activités pour lesquelles le plus de temps est passé directement, utilisez [l’onglet **inférieur** ](#the-bottom-up-tab).  
*   Si vous voulez afficher les activités dans l’ordre dans lequel elles se sont produites lors de l’enregistrement, utilisez [l’onglet **Journal des événements** ](#the-event-log-tab).  

> [!NOTE]
> Les trois sections suivantes se réfèrent à la même démonstration.  Exécutez la démonstration vous-même dans les [onglets activité][ActivityTabsDemo].  

#### Activités racines   

Voici une description du concept d' **activités racines** mentionné dans les sections de l’onglet **arborescence des appels** , de **bas en haut** et **Journal des événements** .  

Les activités racines peuvent entraîner le fonctionnement du navigateur.  Par exemple, lorsque vous cliquez sur une page, le navigateur déclenche une `Event` activité en tant qu’activité racine.  Cela `Event` peut entraîner l’exécution d’un gestionnaire et ainsi de suite.  

Dans le graphique en flamme de la section **principale** , les activités racines se trouvent en haut du graphique.  Dans les onglets **arborescence des appels** et **Journal des événements** , les activités racines sont les éléments de niveau supérieur.  

Voir [l’onglet arborescence des appels](#the-call-tree-tab) pour obtenir un exemple d’activités racines.  

#### Onglet arborescence des appels   

Utilisez l’onglet **arborescence des appels** pour afficher les [activités racines](#root-activities) qui sont à l’origine du problème.  

L’onglet **arborescence des appels** affiche uniquement les activités effectuées au cours de la partie sélectionnée de l’enregistrement.  Pour plus d’informations sur la sélection de parties, voir [Sélectionner une portion d’un enregistrement](#select-a-portion-of-a-recording) .  

> ##### Figure17  
> Onglet **arborescence des appels**  
> ![Onglet arborescence des appels][ImageCallTree]  

Dans la [figure 17](#figure-17), le niveau supérieur des éléments de la colonne **Activity** , par exemple, les `Evaluate Script` `Parse HTML` activités racines.  L’imbrication représente la pile d’appels.  Par exemple, dans la [figure 17](#figure-17), `Parse HTML` qui a entraîné `Evaluate Script` `Compile Script` et `(anonymous)` .  

Le **temps libre** représente le temps passé directement dans cette activité.  **Durée totale** représente le temps passé à cette activité ou à un des enfants.  

Cliquez sur **durée automatique**, **durée totale**ou **activité** pour trier le tableau selon la colonne.  

Utilisez la zone de texte **filtre** pour filtrer les événements par nom d’activité.  

Par défaut, le menu de **regroupement** a la valeur **aucun regroupement**.  Utilisez le menu de **regroupement** pour trier la table d’activité en fonction de différents critères.  

Cliquez sur Afficher la pile la plus **lourde** ![ ][ImageShowHeaviestStackIcon] pour afficher une autre table à droite de la table **activité** .  Cliquez sur une activité pour remplir la table de pile la plus **lourde** .  La table des piles les plus **lourdes** vous indique les enfants de l’activité sélectionnée qui prenaient le plus de temps à s’exécuter.  

#### Onglet inférieur   

Utilisez l’onglet **inférieur** pour afficher les activités qui consomment directement le plus de temps dans l’agrégat.  

L’onglet **inférieur** affiche uniquement les activités effectuées au cours de la partie sélectionnée de l’enregistrement.  Pour plus d’informations sur la sélection de parties, voir [Sélectionner une portion d’un enregistrement](#select-a-portion-of-a-recording) .  

> ##### Figure 18  
> Onglet **inférieur**  
> ![Onglet inférieur][ImageBottomUp]  

Dans le **graphique** en forme de flamme de la [figure 18](#figure-18), observez que presque tout le temps est passé en temps `Parse HTML` .  Dans l’onglet **inférieur** de la [figure 18](#figure-18) , l’activité supérieure `Parse HTML` .  <!--In the flame chart of [Figure 18](#figure-18), the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  Reportez-vous à la rubrique dans l’onglet en **bas** , l’activité la plus coûteuse suivante `Layout` .  

La colonne de **temps libre** représente le temps agrégé passé directement dans cette activité, sur l’ensemble des occurrences.  

La colonne **temps total** représente le temps agrégé dépensé dans cette activité ou sur n’importe quel enfant.  

#### Onglet journal des événements   

Utilisez l’onglet **Journal des événements** pour afficher les activités dans l’ordre dans lequel elles se sont produites lors de l’enregistrement.  

L’onglet **Journal des événements** affiche uniquement les activités effectuées au cours de la partie sélectionnée de l’enregistrement.  Pour plus d’informations sur la sélection de parties, voir [Sélectionner une portion d’un enregistrement](#select-a-portion-of-a-recording) .  

> ##### Figure 19  
> Onglet **Journal des événements**  
> ![Onglet journal des événements][ImageEventLog]  

La colonne **heure de début** représente le point auquel cette activité a commencé, par rapport au début de l’enregistrement.  Par exemple, l’heure de début de `175.7 ms` l’élément sélectionné dans la [figure 19](#figure-19) signifie que l’activité a démarré 175,7 ms après le début de l’enregistrement.  

La colonne **temps libre** représente le temps passé directement dans cette activité.  

Le **nombre total** de colonnes durée représente le temps passé directement dans cette activité ou dans n’importe quel enfant.  

Cliquez sur **heure de début**, **durée automatique**ou **durée totale** pour trier le tableau selon la colonne.

Utilisez la zone de texte **filtre** pour filtrer les activités par nom.  

Utilisez le menu **durée** pour filtrer les activités ayant eu moins de 1 ms ou 15 ms.  Par défaut, le menu **durée** est défini sur **tout**, ce qui signifie que toutes les activités sont affichées.  

Désactivez les cases à cocher **chargement**, **script**, **rendu**ou **peinture** pour filtrer toutes les activités de ces catégories.  

### Afficher l’activité GPU   

Afficher l’activité GPU dans la section **GPU** .  

> ##### Figure 20  
> Section **GPU**  
> ![Section GPU][ImageGpu]  

### Afficher les activités pixellisées   

Affichez les activités pixellisées dans la section **Raster** .  

> ##### Figure 21  
> Section **Raster**  
> ![Section raster][ImageRaster]  

### Afficher les interactions   

Utilisez la section **interactions** pour rechercher et analyser les interactions utilisateur qui se sont produites lors de l’enregistrement.  

> ##### Figure 22  
> Section **interactions**  
> ![Section interactions][ImageInteractions]  

Une ligne rouge en bas d’une interaction représente le temps passé à attendre le thread principal.  

Cliquez sur une interaction pour afficher davantage d’informations sur celle-ci sous l’onglet **Résumé** .  

### Analyser les images par seconde (FPS)   

DevTools offre de nombreuses façons d’analyser les images par seconde:  

*   Utilisez [le graphique **fps** ](#the-fps-chart) pour obtenir une vue d’ensemble des images par seconde au fil de la durée de l’enregistrement.  
*   Utilisez [la section **cadres** ](#the-frames-section) pour afficher la durée d’une image particulière.  
*   Utilisez le **compteur fps** pour une estimation en temps réel de FPS lors de l’exécution de la page.  Voir [trames d’affichage par seconde en temps réel avec le compteur fps](#view-frames-per-second-in-realtime-with-the-fps-meter).  

#### Graphique FPS   

Le graphique **fps** fournit une vue d’ensemble de la fréquence d’images sur la durée d’un enregistrement.  En règle générale, plus la barre verte est élevée, plus la fréquence d’images est élevée.  

Une barre rouge au-dessus du graphique **fps** est une alerte indiquant que le taux d’images a été interrompu comme faible et qu’il a probablement été lésé par l’utilisateur.  

> ##### Figure 23  
> Graphique FPS  
> ![Graphique FPS][ImageFpsChart]  

#### Section cadres   

La section **trames** vous indique exactement le temps qu’une image donnée a duré.  

Pointez sur un cadre pour afficher une info-bulle contenant des informations supplémentaires à son sujet.  

> ##### Figure 24  
> Survol d’un cadre  
> ![Survol d’un cadre][ImageFramesSection]  

Cliquez sur un cadre pour afficher encore plus d’informations sur le cadre sous l’onglet **Résumé** .  DevTools plan le cadre sélectionné en bleu.  

> ##### Figure 25  
> Affichage d’un cadre sous l’onglet **Résumé**  
> ![Affichage d’un cadre sous l’onglet Résumé][ImageFrameSummary]  

### Afficher les requêtes réseau   

Développez la section **réseau** pour afficher une cascade de requêtes réseau qui se sont produites lors de l’enregistrement.  

> ##### Figure 26  
> Section **réseau**  
> ![Section réseau][ImageNetworkRequest]  

Les requêtes sont codées en couleur comme suit:  

*   HTML: bleu  
*   CSS: pourpre  
*   JS: jaune  
*   Images: vert  

Cliquez sur une demande pour afficher davantage d’informations sur celle-ci sous l’onglet **Résumé** .  Par exemple, dans l' [illustration 26](#figure-26) , l’onglet **synthèse** affiche des informations supplémentaires sur la requête bleue sélectionnée dans la section **réseau** .  

Dans le coin supérieur gauche d’une demande, un carré plus foncé est une demande de priorité élevée.  Le carré bleu plus clair correspond à un niveau de priorité inférieur.  Par exemple, dans l' [illustration 26](#figure-26) , le bleu, la requête sélectionnée est d’une priorité plus élevée et le vert au-dessous, de priorité inférieure.  

Dans la [figure 27](#figure-27), la requête pour `www.bing.com` est représentée par une ligne à gauche, une barre au milieu avec une partie sombre et une partie claire, et une ligne à droite.  La [figure 28](#figure-28) montre la représentation correspondante de la même requête dans l’onglet **minutage** du panneau **réseau** .  Voici à quoi correspondent les deux représentations suivantes:

*   La ligne gauche représente tout ce qui concerne le `Connection Start` groupe d’événements compris.  En d’autres termes, il s’agit de tout ce qui est auparavant `Request Sent` , exclusif.  
*   La partie claire de la barre est `Request Sent` et `Waiting (TTFB)` .  
*   La partie sombre de la barre est `Content Download` .  
*   La ligne droite correspond essentiellement au délai passé pour le thread principal.  Cette opération n’est pas représentée dans l’onglet **minutage** .  

> ##### Figure 27  
> Représentation de la barre de lignes de la `www.bing.com` requête  
> ![Représentation de la barre de lignes de la requête www.bing.com][ImageLineBar]  

> ##### Figure 28  
> Représentation de l’onglet **minutage** de la `www.bing.com` requête  
> ![Section réseau][ImageTiming]  

### Afficher les métriques de mémoire   

Activez la case à cocher **mémoire** pour afficher les mesures de mémoire du dernier enregistrement.  

> ##### Figure 29  
> Case à cocher **mémoire**  
> ![Case à cocher mémoire][ImageMemory]  

DevTools affiche un nouveau graphique **mémoire** , au-dessus de l’onglet **Résumé** .  Il existe également un nouveau graphique sous le graphique **net** , appelé **tas**.  Le graphique de **tas** fournit les mêmes informations que la ligne de segment de **mémoire** **js** dans le graphique mémoire.  

> ##### Figure 30  
> Métriques de mémoire, au-dessus de l’onglet **Résumé**  
> ![Métriques de mémoire][ImageMemoryMetrics]  

Les lignes de couleur sur le graphique correspondent aux cases à cocher en plus de la couleur du graphique.  
Désactivez une case à cocher pour masquer cette catégorie dans le graphique.  

Le graphique affiche uniquement la zone de l’enregistrement actuellement sélectionné.  Par exemple, dans la [figure 30](#figure-30), le graphique **mémoire** affiche uniquement l’utilisation de la mémoire de la marque 400 MS au 1750 ms.  

### Affichage de la durée d’une portion d’un enregistrement   

Lors de l’analyse d’une section comme **Network** ou **principal**, il est possible que vous ayez besoin d’une estimation plus précise de la durée de certains événements.  Maintenez la touche enfoncée, `Shift` puis faites glisser vers la gauche ou la droite pour sélectionner une partie de l’enregistrement.  Dans la partie inférieure de votre sélection, DevTools indique la durée de la partie.  

> ##### Figure 31  
> L' `9.47ms` horodatage en bas de la partie sélectionnée indique la durée de la partie.  
> ![Affichage de la durée d’une portion d’un enregistrement][ImageDuration]  

### Affichage d’une capture d’écran   

Pour plus d’informations sur l’activation des captures d’écran, voir capturer des captures [d’écran lors de l’enregistrement](#capture-screenshots-while-recording) .  

Placez le pointeur de la souris sur la **vue d’ensemble** pour afficher une capture d’écran illustrant l’apparence de la page pendant ce moment de l’enregistrement.  La section **vue d’ensemble** contient les graphiques **UC**, **fps**et **net** .  

> ##### Figure 32  
> Affichage d’une capture d’écran  
> ![Affichage d’une capture d’écran][ImageViewScreenshot]  

Vous pouvez également afficher les captures d’écran en cliquant sur un cadre dans la section **cadres** .  DevTools affiche une version miniature de la capture d’écran sous l’onglet **Résumé** .  

> ##### Figure 33  
> Après avoir cliqué sur le `233.9ms` cadre **Frames** dans la section cadre, la capture d’écran de ce cadre est affichée sous l’onglet **Résumé** .  
> ![Affichage d’une capture d’écran sous l’onglet Résumé][ImageFrameScreenshotSummary]  

Pour effectuer un zoom avant dans la capture d’écran, cliquez sur la miniature sous l’onglet **Résumé** .  

> ##### Figure 34  
> Après avoir cliqué sur la miniature sous l’onglet **Résumé** , devtools effectue un zoom avant dans la capture d’écran  
> ![Zoom avant d’une capture d’écran à partir de l’onglet Résumé][ImageFrameScreenshotZoom]  

### Afficher les informations sur les couches   

Pour afficher des informations sur les couches avancées d’une image:  

1.  [Activez Advanced Paint instrumentation](#enable-advanced-paint-instrumentation).  
1.  Sélectionnez une image dans la section **cadre** .  DevTools affiche des informations sur les calques sous l’onglet nouveau **calques** , en regard de l’onglet **Journal des événements** .  
    
    > ##### Figure 35  
    > Volet **couches**  
    > ![Volet couches][ImageLayers]  
    
Pointez sur un calque pour le mettre en surbrillance dans le diagramme.  

> ##### Figure 36  
> Mise en surbrillance du calque **#39**  
> ![Mise en surbrillance d’un calque][ImageLayerHover]  

Pour déplacer le diagramme:  

*   Cliquez sur le mode panoramique **mode panoramique** ![ ][ImagePanModeIcon] pour vous déplacer sur les axes X et Y.  
*   **Rotate Mode** ![ ][ImageRotateModeIcon] Pour faire pivoter le mode de rotation, cliquez sur l’axe Z.  
*   Cliquez sur **Réinitialiser** ![ la transformation réinitialiser ][ImageResetTransformIcon] la transformation pour rétablir la position d’origine du diagramme.  

### Afficher le générateur de dessin Paint   

Pour afficher des informations détaillées sur un événement Paint:  

1.  [Activez Advanced Paint instrumentation](#enable-advanced-paint-instrumentation).  
1.  Sélectionnez un événement **Paint** dans la section **principale** .  
    
    > ##### Figure 37  
    > Onglet **Paint Profiler1.1**  
    > ![Onglet Paint Profiler1.1][ImagePaintProfiler]  
    
## Analyser les performances de rendu à l’aide de l’onglet rendu   

Utilisez les fonctionnalités de l’onglet **rendu** pour visualiser les performances de rendu de votre page.  

Pour ouvrir l’onglet **rendu** :  

1.  [Ouvrir le menu de commandes][DevToolsCommandMenu].  
1.  Commencez à taper `Rendering` et sélectionnez `Show Rendering` .  DevTools affiche l’onglet **rendu** en bas de votre fenêtre devtools.  
    
    > ##### Figure 38  
    > Onglet **rendu**  
    > ![Onglet rendu][ImageRenderingTab]  
    
### Afficher les images par seconde en temps réel avec le compteur FPS   

Le **compteur fps** est une superposition qui s’affiche dans le coin supérieur droit de votre fenêtre d’affichage.  Il fournit une estimation en temps réel de FPS lors de l’exécution de la page.  Pour ouvrir le **compteur fps**:  

1.  Ouvrez l’onglet **rendu** .  [Pour plus d’efficacité, voir analyser les performances de rendu avec l’onglet rendu](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Activez la case à cocher **vumètre** .  
    
    > ##### Figure 39  
    > Vumètre FPS  
    > ![Vumètre FPS][ImageFpsMeter]  
    
### Afficher les événements de peinture en temps réel avec le clignotement de la peinture   

Utilisez la fonction Paint clignotante pour obtenir une vue en temps réel de tous les événements de peinture sur la page.  Dès qu’une partie de la page est de nouveau peinte, DevTools la place en vert.  

Pour activer le clignotement des peintures:  

1.  Ouvrez l’onglet **rendu** .  [Pour plus d’efficacité, voir analyser les performances de rendu avec l’onglet rendu](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Activez la case à cocher **Paint clignotant** .  
    
    > ##### Figure 40  
    > **Paint clignotant**  
    > ![Paint clignotant][ImagePaintFlashing]  
    
### Afficher une superposition de calques avec des bordures de calque   

Utilisez les **bordures de calque** pour afficher une superposition des bordures et des vignettes du calque en haut de la page.  

Pour activer les bordures de calque:  

1.  Ouvrez l’onglet **rendu** .  [Pour plus d’efficacité, voir analyser les performances de rendu avec l’onglet rendu](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Activez la case à cocher **bordures de calque** .  
    
    > ##### Figure 41  
    > **Bordures de calque**  
    > ![Bordures de calque][ImageLayerBorders]  
    
[`debug_colors.cc`][ChromiumDebugColors]Pour obtenir une description des codes de couleur, voir les commentaires.  

### Rechercher des problèmes de performances de défilement en temps réel   

Utilisez des problèmes de performances de défilement pour identifier les éléments de la page qui comportent des écouteurs d’événements liés au défilement qui peuvent nuire aux performances de la page.  
DevTools souligne les éléments potentiellement posant problème en bleu-vert.  

Pour afficher les problèmes de performances de défilement:  

1.  Ouvrez l’onglet **rendu** .  [Pour plus d’efficacité, voir analyser les performances de rendu avec l’onglet rendu](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Activez la case à cocher **problèmes de performances de défilement** .  
 
    > ##### Figure 42  
    > Les **problèmes de performances de défilement** indiquent que les objets dotés de l’affichage sans calque risquent de nuire aux performances de défilement  
    > ![Les problèmes de performances de défilement indiquent que les objets dotés de l’affichage sans calque risquent de nuire aux performances de défilement][ImageScrollingPerformanceIssues]  
    

<!--    -->  



<!-- image links -->  

[ImageCaptureSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageClearRecordingIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-recording-icon.msft.png  
[ImageCollectGarbageIcon]: /microsoft-edge/devtools-guide-chromium/media/collect-garbage-icon.msft.png  
[ImageNextIcon]: /microsoft-edge/devtools-guide-chromium/media/next-icon.msft.png  
[ImagePanModeIcon]: /microsoft-edge/devtools-guide-chromium/media/pan-mode-icon.msft.png  
[ImagePreviousIcon]: /microsoft-edge/devtools-guide-chromium/media/previous-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-page-icon.msft.png  
[ImageResetTransformIcon]: /microsoft-edge/devtools-guide-chromium/media/reset-transform-icon.msft.png  
[ImageRotateModeIcon]: /microsoft-edge/devtools-guide-chromium/media/rotate-mode-icon.msft.png  
[ImageSearchCaseIcon]: /microsoft-edge/devtools-guide-chromium/media/search-case-icon.msft.png  
[ImageSearchRegexIcon]: /microsoft-edge/devtools-guide-chromium/media/search-regex-icon.msft.png  
[ImageShowHeaviestStackIcon]: /microsoft-edge/devtools-guide-chromium/media/show-heaviest-stack-icon.msft.png  

[ImageRecord]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-record-highlight.msft.png "Figure 1: enregistrement"  
[ImageRefreshPage]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refresh-button.msft.png "Figure 2: actualiser la page"  
[ImageLoadRecording]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed.msft.png "Figure 3: enregistrement de chargement de page"  
[ImageScreenshots]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png "Figure 4: cases à cocher captures d’écran"  
[ImageCollectGarbage]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-collect-garbage-button.msft.png "Figure 5: collecter les éléments nettoyés"  
[ImageCaptureSettings]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png "Figure 6: section paramètres de capture"  
[ImageJSSamplesDisabled]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png "Figure 7: exemple d’enregistrement lorsque les exemples de JS sont désactivés"  
[ImageJSSamplesEnabled]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png "Figure 8: exemple d’enregistrement lorsque les exemples de JS sont activés"  
[ImageSaveProfile]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png "Figure 9: enregistrement du profil"  
[ImageLoadProfile]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png "Figure 10: profil de chargement"  
[ImageClearRecording]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png "Figure 11: effacer l’enregistrement"  
[ImageZoom]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-zoom-highlighted.msft.png "Figure 12: glissement de la souris sur la présentation pour effectuer un zoom"  
[ImageSearch]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-search-regex.msft.png "Figure 13: zone de recherche"  
[ImageMain]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-zoomed.msft.png "Figure 14: section principale"  
[ImageMainEventSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-me.msft.png "Figure 15: informations supplémentaires sur la fonction anonyme sous l’onglet Résumé"  
[ImageFlameChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-flame-chart.msft.png "Figure 16: graphique en flamme"  
[ImageCallTree]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-call-tree.msft.png "Figure 17: onglet de l’arborescence des appels"  
[ImageBottomUp]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-bottoms-up.msft.png "Figure 18: onglet inférieur"  
[ImageEventLog]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-event-log.msft.png "Figure 19: onglet journal des événements"  
[ImageGpu]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-gpu-zoomed.msft.png "Figure 20: section GPU"  
[ImageRaster]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-raster.msft.png "Figure 21: section de pixellisation"  
[ImageInteractions]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-interactions-animation.msft.png "Figure 22: section interactions"  
[ImageFpsChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-fps-highlight.msft.png "Figure 23: graphique FPS"  
[ImageFramesSection]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-hover.msft.png "Figure 24: survol d’un cadre"  
[ImageFrameSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-summary.msft.png "Figure 25: affichage d’un cadre sous l’onglet Résumé"  
[ImageNetworkRequest]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-network.msft.png "Figure 26: section réseau"  
[ImageLineBar]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-performance-network.msft.png "Figure 27: représentation de la barre de lignes de la requête www.bing.com"  
[ImageTiming]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-network-timing.msft.png "Figure 28: section réseau"  
[ImageMemory]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-memory-highlight.msft.png "Figure 29: cases à cocher de la mémoire"  
[ImageMemoryMetrics]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-memory-chart.msft.png "Figure 30: métriques de mémoire"  
[ImageDuration]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-duration.msft.png "Figure 31: affichage de la durée d’une portion d’un enregistrement"  
[ImageViewScreenshot]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-screenshots-hover.msft.png "Figure 32: affichage d’une capture d’écran"  
[ImageFrameScreenshotSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-preview.msft.png "Figure 33: affichage d’une capture d’écran sous l’onglet Résumé"  
[ImageFrameScreenshotZoom]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-preview-select.msft.png "Figure 34: zoom avant d’une capture d’écran à partir de l’onglet Résumé"  
[ImageLayers]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-layers-all.msft.png "Figure 35: volet couches"  
[ImageLayerHover]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png "Figure 36: mise en surbrillance d’un calque"  
[ImagePaintProfiler]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-paint-profiler.msft.png "Figure 37: onglet Paint Profiler1.1"  
[ImageRenderingTab]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-console-drawer-rendering.msft.png "Figure 38: onglet rendu"  
[ImageFpsMeter]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-jank-console-rendering-frame-rate.msft.png "Figure 39: vumètre d’FPS"  
[ImagePaintFlashing]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png "Figure 40: couleur clignotante"  
[ImageLayerBorders]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png "Figure 41: bordures de calque"  
[ImageScrollingPerformanceIssues]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png "Figure 42: les problèmes de performances de défilement indiquent qu’il est possible que les objets dotés de l’affichage en mode sans couches nuisent aux performances de défilement"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome)"  
[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index#open-the-command-menu "Ouvrir le menu de commandes-exécuter les commandes avec le menu de commandes Microsoft Edge DevTools"  
[DevtoolsEvaluatePerformanceGettingStarted]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/index "Commencer à analyser les performances de l’exécution"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Démo des onglets d’activité"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors. cc-recherche de code"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
