---
title: Accélérer le runtime JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 2f05ef2911c855df39d60fa732ff5f784ab49473
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984855"
---
<!-- Copyright Kayce Basques and Meggin Kearney

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License. -->





# Accélérer le runtime JavaScript   




Identifiez les fonctions onéreuses à l’aide du panneau **mémoire** .  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Échantillonnage des profils" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   Échantillonnage des profils  
:::image-end:::  

### Résumé  

*   Enregistrez exactement les fonctions qui ont été appelées et la quantité de mémoire requise par l’échantillonnage d’allocation dans le panneau **mémoire** .  
*   Visualisez vos profils sous forme de graphique à flamme.  
    
## Enregistrer un profil d’échantillonnage  

Si vous remarquez Jank dans votre code JavaScript, recueillez un profil d’échantillonnage.  Les profils d’échantillonnage montrent où le temps d’exécution est passé sur les fonctions de votre page.  

1.  Accédez au panneau **mémoire** de devtools.  
1.  Sélectionnez la case d’option d’échantillonnage de l' **attribution** .  
1.  Sélectionnez **Démarrer**.  
1.  En fonction de ce que vous essayez d’analyser, vous pouvez recharger la page, interagir avec la page ou laisser la page s’exécuter.  
1.  Lorsque vous avez terminé, cliquez sur le bouton **arrêter** .  
    
> [!NOTE]
> Vous pouvez également utiliser l' [API utilitaires][DevtoolsConsoleUtilities] de la console pour enregistrer et grouper des profils à partir de la ligne de commande.  

## Afficher le profil d’échantillonnage  

Lorsque vous avez terminé l’enregistrement, DevTools renseigne automatiquement le panneau **mémoire** sous les **profils d’échantillonnage** avec les données de votre enregistrement.  

Le mode par défaut est « **gros» (bas)**.  Cet affichage vous permet de voir quelles fonctions ont le plus d’impact sur les performances et examine les chemins d’appel vers ces fonctions.  

### Changer l’ordre de tri   

Pour modifier l’ordre de tri, sélectionnez le menu déroulant en regard de la **fonction sélectionner le focus** , ![ ][ImageFocusIcon] puis sélectionnez l’une des options suivantes.

**Graphique**.  Affiche un graphique chronologique de l’enregistrement.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Graphique à flamme" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   Graphique à flamme  
:::image-end:::  

**Gros (haut)**.  Répertorie les fonctions en conséquence sur les performances et vous permet d’examiner les chemins d’appel aux fonctions.  Il s’agit de l’affichage par défaut.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Graphique gros" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   Graphique gros  
:::image-end:::  

**Arborescence (haut vers le bas)**.  Affiche une image globale de la structure de l’appel, en commençant par la partie supérieure de la pile d’appels.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png" alt-text="Arborescence" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png":::
   Arborescence  
:::image-end:::  

### Exclure des fonctions   

Pour exclure une fonction de votre profil d’échantillonnage, sélectionnez celle-ci pour la sélectionner, puis cliquez sur l’icône **exclure la fonction sélectionnée** ![ ][ImageExcludeIcon] .  La fonction de requête \ (parent \) de la fonction exclue \ (enfant \) est imputée à la mémoire allouée à la fonction exclue \ (enfant \).  

Sélectionnez l’icône **restaurer toutes les fonctions** \ ( ![ restaurer toutes les fonctions ][ImageRestoreIcon] \) pour restaurer toutes les fonctions exclues dans l’enregistrement.  

## Afficher le profil d’échantillonnage sous forme de graphique   

Le mode graphique fournit une représentation visuelle du profil d’échantillonnage au fil du temps.  

Après avoir [enregistré un profil d’échantillonnage](#record-a-sampling-profile), vous pouvez l’afficher en tant que graphique de type flamme en [modifiant l’ordre de tri](#change-sort-order) en **graphique**.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Affichage de graphique à flamme" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   Affichage de graphique à flamme  
:::image-end:::  

Le graphique à flamme est divisé en deux parties.  

| | Quatrième | Description |  
| --- |:--- |:--- |  
| 1 | Vue d'ensemble | Un affichage attractif des oiseaux de l’ensemble de l’enregistrement.  La hauteur des barres correspond à la profondeur de la pile d’appels.  C’est pourquoi, plus la barre est grande, plus la pile d’appels est profonde.  |  
| deuxième | Piles d’appels | Il s’agit d’une vue détaillée des fonctions qui ont été appelées lors de l’enregistrement.  L’axe horizontal est le temps et l’axe vertical est la pile d’appels.  Les piles sont organisées de haut en bas.  Par conséquent, la fonction en haut appelle celle qui s’en trouve au-dessous, et ainsi de suite.  |  

Les fonctions apparaissent de façon aléatoire.  Il n’existe aucune corrélation avec les couleurs utilisées dans les autres panneaux.  Toutefois, les fonctions sont toujours les mêmes coloriées entre les appels, afin que vous puissiez voir les modèles dans chaque Runtime.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png" alt-text="Graphique à flamme annotée" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png":::
   Graphique à flamme annotée  
:::image-end:::  

Une pile d’appels de haut niveau n’est pas nécessairement importante, cela signifie simplement que de nombreuses fonctions étaient appelées.  Mais une barre larges signifie qu’une fonction a duré un certain temps.  Ces suggestions peuvent être optimisées.  

### Effectuer un zoom avant sur des parties spécifiques de l’enregistrement   

Maintenez la touche CTRL enfoncée, puis faites glisser la souris vers la gauche et la droite pour effectuer un zoom avant sur certaines parties de la pile d’appels.  Après le zoom, la pile d’appels affiche automatiquement la partie de l’enregistrement que vous avez sélectionnée.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png" alt-text="Zoom de graphique" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png":::
   Zoom de graphique  
:::image-end:::  

### Afficher les détails de la fonction   

Sélectionnez sur une fonction pour afficher la définition dans le panneau **sources** .  

Pointez sur une fonction pour afficher les données de nom et de minutage.  Les informations suivantes sont fournies.  

| Données | Description |  
|:--- |:--- |  
| **Name** | Nom de la fonction.  |  
| **Dimensionnement automatique** | Taille de l’appel actif de la fonction, y compris uniquement les instructions de la fonction.  |  
| **Taille totale** | La taille de l’appel en cours de cette fonction et des fonctions qu’elle appelle.  |  
| **URL** | L’emplacement de la définition de la fonction sous la forme `base.js:261` où `base.js` est le nom du fichier où la fonction est définie et `261` représente le numéro de ligne de la définition.  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png" alt-text="Affichage des détails de fonctions dans le graphique" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png":::
   Affichage des détails de fonctions dans le graphique  
:::image-end:::  

<!--  
## Feedback   


-->  

<!-- image links -->  

[ImageExcludeIcon]: ../media/exclude-icon.msft.png  
[ImageFocusIcon]: ../media/focus-icon.msft.png  
[ImageRestoreIcon]: ../media/restore-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleUtilities]: ../console/utilities.md "Référence sur l’API des utilitaires de console | Documents Microsoft"  
[DevtoolsConsoleUtilitiesProfile]: ../console/utilities.md#profile "XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX Documents Microsoft"  
[DevtoolsConsoleUtilitiesProfileEnd]: ../console/utilities.md#profileend "profileEnd-xxx XXXXXXX XXXXXXX xxx xxxxxxx Documents Microsoft"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \) et [Meggin Kearney][MegginKearney] \ (Technical Writer \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
