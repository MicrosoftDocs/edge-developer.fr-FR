---
description: Utiliser des points d’arrêt DOM pour déboguer visuellement des problèmes de disposition sur votre page
title: Éléments DevTools-points d’arrêt DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, éléments, points d’arrêt DOM et mutation DOM
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cb60fa0497c98c152ca2c5adf28e9dee5d7c9f98
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233074"
---
# Points d’arrêt DOM

Gérez vos points d’arrêt de mutation DOM depuis ce volet, y compris la désactivation, la suppression et la reliaison.

Vous pouvez utiliser des points d’arrêt de mutation DOM pour vous arrêter dans le débogueur dès qu’un nœud d’élément sélectionné change. Cela s’avère utile pour identifier le code responsable de l’origine des problèmes visuels liés à votre interface utilisateur, sans avoir à définir des points d’arrêt individuels sur chacune des API 450 + DOM dans *EdgeHTML* qui peut déclencher de telles modifications. 

Pour définir un point d’arrêt DOM, cliquez avec le bouton droit sur un élément dans l' *arborescence html* du panneau **éléments** pour ouvrir le menu contextuel.

![Menu contextuel des points d’arrêt DOM](../media/elements_dom_breakpoints_contextmenu.png)

Vous pouvez définir n’importe quel points d’arrêt suivants:

 - **Arrêt du nœud supprimé**: arrêter dans le débogueur lorsque l’élément sélectionné est supprimé du document (arborescence DOM).

 - **Saut de la sous-arborescence modifié**: s’arrête dans le débogueur lorsque l’un des descendants de l’élément sélectionné est modifié (ajouté, supprimé ou ses sous-arbres sont modifiés). Cela ne sera pas interrompu lors de la modification des attributs (Voir l’option suivante).

 - **Arrêt sur l’attribut modifié**: s’arrête dans le débogueur lors de l’ajout, de la suppression ou de la modification d’un attribut de l’élément sélectionné.

Le volet **points d’arrêt DOM** répertorie les éléments sélectionnés (en générant un sélecteur décrivant son emplacement dans le DOM) et les types de points d’arrêt que vous avez définis (*nœud supprimé, sous-arborescence modifié, attribut modifié*). À partir de cet emplacement, vous pouvez également *relier*, *Désactiver*ou *supprimer* vos points d’arrêt, individuellement (à partir du menu contextuel de RT-clic) ou tous à la fois (à l’aide des boutons).

![Volet points d’arrêt DOM](../media/elements_dom_breakpoints.png)

## Persistance de point d’arrêt

Les points d’arrêt sont stockés (et associés à l’URL de la page dans laquelle ils sont définis) dans le cadre de vos paramètres DevTools. Lors du rechargement de la page ou de la fermeture et de la réouverture des outils, DevTools tente de lier vos points d’arrêt aux éléments associés.

Les points d’arrêt qui ne peuvent pas être automatiquement réliés sont indiqués par une icône d’avertissement sur le cercle de point d’arrêt. Pour ces derniers, vous pouvez attendre de lier de nouveau l’élément manuellement (à l’aide du bouton **rélier le point d’arrêt** et/ou de l’option de menu contextuel) une fois qu’un élément correspondant apparaît dans le DOM (et que l’icône de point d’arrêt n’affiche plus l’indicateur d’avertissement) ou que vous **supprimez** le point d’arrêt.

![Indicateur de point d’arrêt indépendant](../media/elements_dom_breakpoint_unbound.png)

Outre ce volet de *points d’arrêt DOM* , vous pouvez également gérer vos [points d’arrêt DOM](../debugger.md#dom-breakpoints) à partir du **débogueur**.

## Limitations actuelles

Gardez à l’esprit les limitations suivantes relatives au débogage de points d’arrêt DOM dans Edge DevTools:

- Edge DevTools ne prend actuellement pas en charge les points d’arrêt de reliaison au sein de [ `<iframe>` s](https://developer.mozilla.org/docs/Web/HTML/Element/iframe). Si vous définissez un point d’arrêt dans un IFRAME et fermez le DevTools de bord ou actualisez la page, le point d’arrêt sera perdu.

- Si votre script rencontre un point d’arrêt asynchrone avant la fin de l’exécution du DOM [`readyState`](https://developer.mozilla.org/docs/Web/API/Document/readyState) , vous ne serez pas en mesure de définir un point d’arrêt DOM lorsque le débogueur est suspendu. En règle générale, vous pouvez résoudre ce problème en définissant les [`defer`](https://developer.mozilla.org/docs/Web/HTML/Element/script#Attributes) attributs ou les [`async`](https://developer.mozilla.org/docs/Web/HTML/Element/script#Attributes) attributs de script.

- Pour les scripts synchrones, nous déclencherons la reliaison automatique des points d’arrêt lorsque l' [`window.onload`](https://developer.mozilla.org/docs/Web/API/GlobalEventHandlers/onload) événement est appelé. Dans le cas présent, il est possible que nous manquerons des points d’arrêt de liaison qui déclenchent la génération initiale du DOM par script. Pour les scripts asynchrones, nous déclenchons une tentative de reliaison avant que le premier script ne s’exécute, afin que vos points d’arrêt puissent se relier et déclencher le déclenchement souhaité.
