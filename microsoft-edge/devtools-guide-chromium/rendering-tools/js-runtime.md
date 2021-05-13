---
description: Identifiez les fonctions coûteuses à l’aide Microsoft Edge panneau Mémoire DevTools.
title: Accélérer le runtime JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: bbac00ab46e205fb692cc3de3e5f08ba854b0911
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565084"
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
# <a name="speed-up-javascript-runtime"></a>Accélérer le runtime JavaScript  

Identifiez les fonctions coûteuses à l’aide **de l’outil** Mémoire.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Exemples de profils" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   Exemples de profils  
:::image-end:::  

### <a name="summary"></a>Résumé  

*   Enregistrez exactement les fonctions qui ont été appelées et la quantité de mémoire nécessaire avec l’échantillonnage d’allocation dans **l’outil Mémoire.**  
*   Visualisez vos profils en tant que graphique graphique graphique.  
    
## <a name="record-a-sampling-profile"></a>Enregistrer un profil d’échantillonnage  

Si vous remarquez jank dans votre JavaScript, collectez un profil d’échantillonnage.  Les profils d’échantillonnage indiquent où le temps d’exécution est passé sur les fonctions de votre page.  

1.  Accédez à **l’outil** Mémoire de DevTools.  
1.  Choisissez la **radio d’échantillonnage** d’allocation.  
1.  Choose **Start**.  
1.  Selon ce que vous essayez d’analyser, vous pouvez soit actualiser la page, interagir avec la page, soit laisser la page s’exécuter.  
1.  Lorsque **vous** avez terminé, sélectionnez le bouton Arrêter.  
    
> [!NOTE]
> Vous pouvez également utiliser [l’API des utilitaires console][DevtoolsConsoleUtilities] pour enregistrer et grouper des profils à partir de la ligne de commande.  

## <a name="view-sampling-profile"></a>Afficher le profil d’échantillonnage  

Lorsque vous avez terminé l’enregistrement, DevTools remplit automatiquement le panneau Mémoire sous **PROFILS D’ÉCHANTILLONNAGE** avec les données de votre enregistrement. ****  

L’affichage par défaut **est Heavy \(Bottom Up\).**  Cette vue vous permet d’examiner les fonctions qui ont eu le plus d’impact sur les performances et d’examiner le chemin d’accès à la demande pour chaque fonction.  

### <a name="change-sort-order"></a>Modifier l’ordre de tri  

Pour modifier l’ordre de tri, sélectionnez le menu déroulant en face de l’icône de la fonction sélectionnée du **focus** \( focus selected function \), puis choisissez l’une des ![ options ](../media/focus-icon.msft.png) suivantes.

**Graphique**.  Affiche un graphique chronologique de l’enregistrement.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Graphique de chart chart" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   Graphique de chart chart  
:::image-end:::  

**Heavy \(Bottom Up\)**.  Répertorie les fonctions par impact sur les performances et vous permet d’examiner les chemins d’accès appelants aux fonctions.  Il s’agit de l’affichage par défaut.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Graphique épais" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   Graphique épais  
:::image-end:::  

**Tree \(Top Down\)**.  Affiche une image globale de la structure d’appel, en commençant en haut de la pile d’appels.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png" alt-text="Graphique d’arborescence" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png":::
   Graphique d’arborescence  
:::image-end:::  

### <a name="exclude-functions"></a>Exclure des fonctions  

Pour exclure une fonction de votre profil d’échantillonnage, choisissez-la, puis choisissez le bouton exclure la fonction sélectionnée **\(** exclure la ![ fonction sélectionnée ](../media/exclude-icon.msft.png) \).  La fonction de demande \(parent\) de la fonction exclue \(enfant\) est chargée de la mémoire allouée affectée à la fonction exclue \(enfant\).  

Sélectionnez le bouton restaurer **toutes les fonctions** \( restaurer toutes les fonctions \) pour restaurer toutes les fonctions ![ ](../media/restore-icon.msft.png) exclues dans l’enregistrement.  

## <a name="view-sampling-profile-as-chart"></a>Afficher le profil d’échantillonnage en tant que graphique  

L’affichage Graphique fournit une représentation visuelle du profil d’échantillonnage au fil du temps.  

Après avoir [enregistré un profil d’échantillonnage,](#record-a-sampling-profile)affichez l’enregistrement sous la forme d’un graphique à graphiques en modifiant l’ordre [de tri](#change-sort-order) en **graphique.**  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Affichage Graphique de graphique" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   Affichage Graphique de graphique  
:::image-end:::  

Le graphique en graphiques est divisé en deux parties.  

| index | Partie | Description |  
| --- |:--- |:--- |  
| 1 | Vue d'ensemble | Vue oculaire de l’intégralité de l’enregistrement.  La hauteur des barres correspond à la profondeur de la pile d’appels.  Ainsi, plus la barre est élevée, plus la pile d’appels est profonde.  |  
| 2 | Pile des appels | Il s’agit d’une vue détaillée des fonctions qui ont été appelées pendant l’enregistrement.  L’axe horizontal est le temps et l’axe vertical est la pile d’appels.  Les piles sont organisées de haut en bas.  Ainsi, la fonction au-dessus appelait celle en dessous, et ainsi de suite.  |  

Les fonctions sont colorées de manière aléatoire.  Il n’existe aucune corrélation avec les couleurs utilisées dans les autres panneaux.  Toutefois, les fonctions sont toujours colorées de la même façon entre les appels, de sorte que vous pouvez observer les modèles dans chaque runtime.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png" alt-text="Graphique en graphiques à graphiques à annoter" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png":::
   Graphique en graphiques à graphiques à annoter  
:::image-end:::  

Une pile d’appels de grande taille n’est pas nécessairement significative, cela signifie simplement que de nombreuses fonctions ont été appelées.  Toutefois, une barre large signifie qu’une fonction a mis beaucoup de temps à se terminer.  Ce sont des candidats à l’optimisation.  

### <a name="zoom-in-on-specific-parts-of-recording"></a>Zoom sur des parties spécifiques de l’enregistrement  

Choisissez, maintenez la souris à gauche et à droite dans la vue d’ensemble, puis faites glisser la souris vers la gauche pour zoomer sur des parties particulières de la pile d’appels.  Après avoir zoomé, la pile d’appels affiche automatiquement la partie de l’enregistrement que vous avez sélectionnée.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png" alt-text="Graphique avec zoom" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png":::
   Graphique avec zoom  
:::image-end:::  

### <a name="view-function-details"></a>Afficher les détails de la fonction  

Choisissez une fonction pour afficher la définition dans **l’outil Sources.**  

Pointez sur une fonction pour afficher le nom et les données de minutage.  Les informations suivantes sont fournies.  

| Détail | Description |  
|:--- |:--- |  
| **Name** | Nom de la fonction.  |  
| **Taille autonome** | Taille de l’appel actuel de la fonction, y compris uniquement les instructions dans la fonction.  |  
| **Taille totale** | Taille de l’appel actuel de cette fonction et de toutes les fonctions qu’elle a appelées.  |  
| **URL** | L’emplacement de la définition de fonction sous la forme où est le nom du fichier où la fonction est définie et est le numéro de ligne `base.js:261` `base.js` de la `261` définition.  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png" alt-text="Afficher les détails des fonctions dans le graphique" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png":::
   Afficher les détails des fonctions dans le graphique  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleUtilities]: ../console/utilities.md "Référence de l’API des utilitaires de console | Documents Microsoft"  
[DevtoolsConsoleUtilitiesProfile]: ../console/utilities.md#profile "profile - Console utilities API reference | Documents Microsoft"  
[DevtoolsConsoleUtilitiesProfileEnd]: ../console/utilities.md#profileend "profileEnd - Référence de l’API des utilitaires de console | Documents Microsoft"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est trouvée ici et est co-auteure par [Les Basques DeCénais (Rédacteur][KayceBasques] technique, Chrome DevTools \& Writer\) et [Meggin Kearney][MegginKearney] \(Tech Writer\). [](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
