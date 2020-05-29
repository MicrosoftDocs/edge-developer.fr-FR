---
description: Comment déboguer Microsoft Edge (chrome) et Microsoft Edge (EdgeHTML) du code VS
title: Déboguer Microsoft Edge (chrome) à partir du code VS
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/10/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, code vs, code Visual Studio, débogueur
ms.openlocfilehash: 7d8d2f87500b3e81866b49de32db91c0a525baf2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566603"
---
# Débogueur pour l’extension de code Microsoft Edge VS

Le [débogueur de l’extension de code Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs vous permet de déboguer votre ligne de code JavaScript frontal par ligne et de voir les instructions qui s’affichent `console.log()` directement à partir de [code Visual Studio](https://code.visualstudio.com/)!

![Image GIF du débogueur pour l’extension de code Edge et au bureau](./media/debugger-for-edge.gif)

## Lancement de Microsoft Edge

Accédez à la vue débogage ( `Ctrl`  +  `Shift`  +  `D` sous Windows ou `Command`  +  `Shift`  +  `D` sur Mac) dans la **barre d’activité**. Si vous n’avez pas de configurations dans le code VS, appuyez `F5` sur Windows ou Mac ou cliquez sur le bouton de **lecture** de couleur verte. Dans la liste déroulante, sélectionnez «Edge». Un fichier **Launch. JSON** s’affiche alors avec la configuration suivante:

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "type": "edge",
            "request": "launch",
            "name": "Launch Edge against localhost",
            "url": "http://localhost:8080",
            "webRoot": "${workspaceFolder}"
        }
    ]
}
```

Si vous avez à présent appuyé `F5` sur Windows ou Mac ou cliquez de nouveau sur le bouton de **lecture** de couleur verte, le code est lancé par le biais de Microsoft Edge (EdgeHTML) et vous pourrez déboguer n’importe quel projet Web exécuté sur le port **8080** directement à partir du code vs.

### Microsoft Edge (Chromium)

Si vous voulez lancer Microsoft Edge (chrome), la nouvelle version de Microsoft Edge, au lieu de Microsoft Edge (EdgeHTML), vous devez simplement ajouter un `version` attribut à votre configuration existante avec la version de Microsoft Edge (chrome) que vous voulez lancer ( `dev` , `beta` ou `canary` ). La configuration suivante entraîne le lancement de la version Canaries de Microsoft Edge (chrome):

```json
{
    "type": "edge",
    "request": "launch",
    "version": "canary",
    "name": "Launch Edge against localhost",
    "url": "http://localhost:8080",
    "webRoot": "${workspaceFolder}"
}
```

## Joindre à Microsoft Edge

Vous pouvez également joindre le code VS à Microsoft Edge (chrome). À partir de votre terminal, exécutez la commande suivante:

`start msedge --remote-debugging-port=9222`

Ajoutez la configuration ci-dessous à votre fichier **Launch. JSON** :

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```

S’il s’agit de la configuration, le code VS sera attaché à Microsoft Edge (chrome) et vous pourrez démarrer le débogage.

## Commentaires

Envoyez-nous vos commentaires en envoyant [un problème](https://github.com/Microsoft/vscode-edge-debug2/issues/new) à l’aide de cette extension [GitHub référentiel Samples](https://github.com/Microsoft/vscode-edge-debug2). Incluez le fichier journal de l’adaptateur de débogage, qui est créé pour chaque exécution du répertoire% Temp% avec le nom `vscode-edge-debug2.txt` . Vous pouvez faire glisser ce fichier dans un commentaire de problème pour le télécharger sur GitHub.

Si vous souhaitez nous aider à améliorer cette extension, nous accueillons vos contributions. Vous trouverez tout ce dont vous avez besoin pour commencer à utiliser [notre GitHub référentiel Samples](https://github.com/Microsoft/vscode-edge-debug2).