---
title: Utiliser le manifeste Web App pour intégrer votre application Web progressive au système d’exploitation
description: Découvrez comment utiliser le manifeste Web App pour intégrer votre application Web progressive dans votre système d’exploitation.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/15/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: applications Web progressives, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: f493ae0c3cef3a1950b2207d66fef65055b2d959
ms.sourcegitcommit: d9cc829deb709b0866f6b43a5f4733682ddae5ca
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/16/2020
ms.locfileid: "10659292"
---
# Utiliser le manifeste Web App pour intégrer votre application Web progressive au système d’exploitation

Un manifeste de l’application Web d’un site Web détermine le fonctionnement et le comportement de votre application Web multifonction de votre application sur un appareil.  Au niveau le plus simple, le manifeste fournit des détails sur le nom de votre application, des icônes à utiliser pour représenter votre application dans les menus système et des couleurs de thème utilisées dans la barre de titre.  Le manifeste vous permet également de déverrouiller des fonctionnalités puissantes qui permettent à votre application de se comporter comme d’autres applications natives sur le système.  

## Utiliser des raccourcis pour fournir un accès rapide aux fonctionnalités  

La plupart des systèmes d’exploitation fournissent un accès rapide aux fonctionnalités d’application principales à l’aide de raccourcis dans le menu contextuel associé à l’icône de l’application.  Pour utiliser des raccourcis dans votre fichier Project Web App, incluez la `shortcuts` propriété dans le manifeste de votre application Web.  L’extrait de code suivant montre comment définir un raccourci dans le manifeste de votre application Web.  

```json
"shortcuts": [
    {
        "name": "Play Later",
        "description": "View the list of podcasts you saved for later",
        "url": "/play-later",
        "icons": [
            {
                "src": "/icons/play-later.svg",
                "type": "image/svg+xml",
                "purpose": "any"
            }
        ]
    },
    {
        "name": "Subscriptions",
        "description": "View the list of podcasts available in your subscription",
        "url": "/subscriptions?sort=desc"
    }
]
```  

Lors de l’ajout d’un manifeste d’application Web complet, l’ajout de l’extrait de code précédent permet d’activer deux raccourcis dans le menu contextuel de l’icône de l’application.  Le premier est nommé `Play Later` et possède une icône personnalisée.  Le second est nommé `Subscriptions` et ne comporte pas d’icône, car la `icons` propriété est facultative.  La `description` propriété est également facultative et peut être utilisée pour fournir des informations supplémentaires à des fins d’accessibilité.  

## Identifier votre application en tant que cible de partage

De nombreux systèmes d’exploitation permettent aux utilisateurs de partager rapidement des liens et des fichiers avec des applications natives. Les applications Web progressives peuvent également participer à cette fonction par le biais du `share_target` manifeste de l’application Web. À l’aide de share_target, vous définissez la page «action» (similaire à un formulaire) et les paramètres que vous vous attendez à y transmettre. L’extrait de code suivant montre un exemple de l’utilisation de `share_target` .

```json
"share_target": {
    "action": "/share.html",
    "params": {
        "title": "name",
        "text": "description",
        "url": "link"
    }
}
```

Lors de l’ajout du manifeste de l’application Web, cette action établit «/share.html» en tant que page d’action du partage. Par ailleurs, il définit trois paramètres qui seraient transmis à cette page d’action: «Title», «Text» et «URL». Ces paramètres sont stockés dans les propriétés «Name», «description» et «Link» de l’objet [ShareData](https://wicg.github.io/web-share#dom-sharedata) . Par défaut, la page d’action reçoit ces paramètres dans le cadre d’une demande GET, mais vous pouvez spécifier la requête `method` et le codage \ (en tant que `enctype` \), comme vous le feriez sur un formulaire Web.

## Voir également  

Pour en savoir plus sur les manifestes de l’application Web, consultez la liste suivante de rubriques connexes.  

* [Manifestes de l’application Web][MDNWebAppManifests]  
* [Cible de partage Web][WICGShareTarget]
* [Partager sur le Web][WICGShare]

<!-- links -->  

[MDNWebAppManifests]: https://developer.mozilla.org/docs/Web/Manifest "Manifestes de l’application Web | MDN"  
[WICGShareTarget]: https://wicg.github.io/web-share-target/ "API cible de partage Web | WICG"
[WICGShare]: https://w3c.github.io/web-share/ "API de partage Web | WICG"
