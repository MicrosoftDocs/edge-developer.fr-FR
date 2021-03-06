---
title: Utiliser le manifeste d’application web pour intégrer votre application Web progressive au système d’exploitation
description: Découvrez comment utiliser le manifeste d’application web pour intégrer votre application Web progressive à votre système d’exploitation.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: applications web progressives, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 0063323b1fde94d84e70df51170726325dd0f2a9
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399098"
---
# <a name="use-the-web-app-manifest-to-integrate-your-progressive-web-app-into-the-operating-system"></a>Utiliser le manifeste d’application web pour intégrer votre application web progressive au système d’exploitation

Un manifeste d’application web d’un site web régit l’apparence et le comportement de votre application web progressive \(PWA\) lorsqu’elle est installée sur un appareil.  Au niveau le plus élémentaire, le manifeste fournit des détails sur le nom de votre application, les icônes à utiliser pour représenter votre application dans les menus système et le thème colore le système d’exploitation \(OS\) utilise dans la barre de titre.  Le manifeste vous permet également de déverrouiller des fonctionnalités puissantes qui permettent à votre application de se comporter comme d’autres applications natives sur le système.  

## <a name="use-shortcuts-to-provide-quick-access-to-features"></a>Utiliser des raccourcis pour fournir un accès rapide aux fonctionnalités  

La plupart des systèmes d’exploitation fournissent un accès rapide aux fonctionnalités clés de l’application à l’aide de raccourcis dans le menu contextique connecté à l’icône de l’application.  Pour utiliser des raccourcis dans votre PWA, incluez `shortcuts` la propriété dans votre manifeste d’application web.  L’extrait de code suivant montre comment définir un raccourci dans le manifeste de votre application web.  

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

Lorsqu’il est ajouté à un manifeste d’application web complet, l’ajout de l’extrait de code précédent active deux raccourcis dans le menu contextique sur l’icône de l’application.  Le premier est nommé `Play Later` et possède une icône personnalisée.  Le second est nommé `Subscriptions` et n’a pas d’icône, car `icons` la propriété est facultative.  La propriété est également facultative et peut être utilisée pour fournir des informations supplémentaires à `description` des fins d’accessibilité.  

## <a name="identify-your-app-as-a-share-target"></a>Identifier votre application en tant que cible de partage

De nombreux systèmes d’exploitation permettent aux utilisateurs de partager rapidement des liens et des fichiers avec des applications natives. Les applications web progressives peuvent également participer à cette fonctionnalité, à l’aide du `share_target` membre du manifeste d’application web.  À `share_target` l’aide de , vous définissez la page \(similaire à un formulaire\) et les paramètres que vous prévoyez `"action"` d’y passer.  L’extrait de code suivant affiche un exemple `share_target` d’utilisation.

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

Lorsqu’il est ajouté au manifeste de l’application Web, il s’agit de la `"/share.html"` page d’action d’un partage. En outre, il définit trois paramètres qui seraient transmis à cette page d’action : `"title"` `"text"` , et `"url"` .  Ces paramètres sont stockés dans les propriétés et les propriétés `"name"` `"description"` de `"link"` [l’objet ShareData.][GitHubWicgWebShareDomSharedata]  Par défaut, la page d’action reçoit les paramètres dans le cadre d’une requête GET, mais vous pouvez spécifier la demande et `method` l’encodage \(en tant que \), comme vous le feriez sur un `enctype` formulaire web.

## <a name="see-also"></a>Voir également  

Pour en savoir plus sur les manifestes d’application web, accédez à la liste suivante des rubriques connexes.  

*   [Manifestes d’application web][MDNWebAppManifests]  
*   [Cible de partage web][GitHubWicgWebShareTarget]
*   [Partage web][GithubW3cWebShare]
    
<!-- links -->  

[MDNWebAppManifests]: https://developer.mozilla.org/docs/Web/Manifest "Manifestes d’application web | MDN"  

[GitHubWicgWebShareTarget]: https://wicg.github.io/web-share-target "Web Share Target API | WICG"
[GitHubWicgWebShareDomSharedata]: https://wicg.github.io/web-share#dom-sharedata "Dictionnaire ShareData - Api de partage web | WICG"  

[GithubW3cWebShare]: https://w3c.github.io/web-share/ "Web Share API | WICG"
