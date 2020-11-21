---
description: Fonctionnalités ajoutées au DevTools Microsoft Edge (chrome) en mars 2019
title: Nouveautés de Microsoft Edge (chrome) DevTools en mars 2019
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/23/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 0b592eddbd68b3bbd8ff0a9edf9a1253bd79677e
ms.sourcegitcommit: acf8ad7cb6c8ecf83a6170f8eeb9bec32878f8ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182511"
---
# Nouveautés de Microsoft Edge (chrome) DevTools

Nous vous remercions d’avoir essayé une version d’évaluation du nouveau Microsoft Edge. Avec cette version, nous avons entrepris une équipe majeure dans la plateforme Web sous-jacente de Microsoft Edge en adoptant le projet open source de chrome. Avec cette modification, il est plus facile de créer et tester vos sites Web dans Microsoft Edge et de veiller à ce que les utilisateurs puissent continuer à travailler comme prévu, même si vos utilisateurs naviguent dans un autre navigateur de chrome, tel que Google Chrome, Vivaldi, Opera ou en 3D.

## Le nouveau Microsoft Edge (chrome) DevTools

Si vous examinez Microsoft Edge et que vous développez essentiellement dans un navigateur en chrome, il est préférable de vous sentir à la maison. Les outils de développement Microsoft Edge (chrome) sont exactement comme les outils de développement que vous connaissez et utilisez déjà.

![DevTools Microsoft Edge (chrome)](./media/devtools.png)

Si vous découvrez la nouvelle version de Microsoft Edge et que vous avez développé la version de Microsoft Edge (EdgeHTML), nous avons mis en place de nouveaux outils qui vous permettront de créer et tester plus facilement vos sites Web dans Microsoft Edge. Pour en savoir plus sur ces nouveaux outils, consultez [le Guide Microsoft Edge (chrome) devtools](../devtools-guide-chromium.md).

## Nouveaux thèmes sombres et clairs pour le DevTools

Nous avons conçu de nouvelles thèmes sombres et clairs pour le DevTools que nous pensons que vous apprécierez! Par défaut, Microsoft Edge (chrome) DevTools utilise le thème sombre. Pour modifier le thème de devtools, appuyez `Fn`  +  `F1` sur Windows ou Mac ou accédez à paramètres à l’aide du `...` bouton dans le coin supérieur droit de la devtools.

![Menu principal de Microsoft Edge (chrome) DevTools](./media/devtools-main-menu.png)

Dans les paramètres, vous pouvez modifier le thème du DevTools. Si vous avez aimé la façon dont le DevTools a été examiné dans votre navigateur de chrome, vous pouvez faire en sorte que le DevTools de Microsoft Edge (chrome) ressemble exactement à celui-ci en sélectionnant les thèmes **Dark (chrome)** ou **Light (chrome)** respectivement. 

## Déboguer Microsoft Edge (chrome) à partir du code VS

Le [débogueur de l’extension de code Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs vous permet désormais de déboguer Microsoft Edge (EdgeHTML) et Microsoft Edge (chrome) directement à partir du code vs.

![Débogueur pour l’extension de code Edge VS](./media/vscode-debugger.png)

Pour lancer Microsoft Edge (chrome) au lieu de Microsoft Edge (EdgeHTML) à partir du code VS, vous devez ajouter un `version` attribut à votre **launch.jsexistant sur** la configuration avec la version de Microsoft Edge (chrome) que vous voulez lancer ( `dev` , `beta` ou `canary` ). Voici un exemple ** delaunch.jsde** configuration qui lancera la version Canaries de Microsoft Edge (chrome) sur [Bing.com](https://www.bing.com/):

```json
{
    "type": "edge",
    "request": "launch",
    "version": "canary",
    "name": "Launch Microsoft Edge (Chromium) Canary against Bing",
    "url": "https://bing.com"
}
```

Pour plus d’informations, consultez [la procédure de débogage de Microsoft Edge (chrome) à partir du code vs](../visual-studio-code/debugger-for-edge.md).

## Mise à jour du protocole Edge DevTools

Avec le Shift dans la plateforme Web sous-jacente de Microsoft Edge, le protocole Edge DevTools ne recevra plus aucune mise à jour. Le DevTools de Microsoft Edge (chrome) utilise le protocole DevTools chrome ou le protocole CDP. Pour référencer la documentation sur les domaines et méthodes en CDP, consultez [la visionneuse CDP](https://chromedevtools.github.io/devtools-protocol/tot/Accessibility).

Dans le nouveau Microsoft Edge, toutes les méthodes qui sont préfixées ne sont `ms` pas prises en charge. Pour en savoir plus sur l’utilisation de la technologie CDP dans Microsoft Edge (chrome), consultez la rubrique [protocole devtools (chrome)](../devtools-protocol-chromium.md).

## Problèmes connus

De nombreux liens à partir de Microsoft Edge (chrome) DevTools vers du contenu hébergé sur des sites tiers ont été supprimés de manière temporaire. Dès que nous aurons la possibilité de les remplacer, nous les ajouterons au DevTools.


Lors du débogage du contenu Web sur un appareil Android à partir de Microsoft Edge (chrome), la version de l’DevTools qui s’ouvre lorsque vous cliquez sur le bouton **Inspect** de l’outil **périphériques distants** ne correspond pas à la version du navigateur sur votre appareil Android. Par conséquent, il est possible que vous voyiez de nouvelles fonctionnalités dans le DevTools qui ne fonctionnent pas sur le navigateur sur votre appareil Android. S’il s’agit d’un problème que vous rencontrez, nous aimerions le lire [.](../devtools-guide-chromium.md#getting-in-touch-with-the-microsoft-edge-devtools-team)

Enfin, Visual Studio sur Windows et Mac ne prennent pas encore en charge Microsoft Edge (chrome). Inscrivez-vous [ici](https://visualstudio.microsoft.com/vs/preview/) pour être le premier à savoir lorsque nous disposons d’une version d’évaluation de Visual Studio prenant en charge le débogage JavaScript au sein de Microsoft Edge (chrome) pour les projets ASP.net.  
