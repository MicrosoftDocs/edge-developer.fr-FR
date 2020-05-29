---
description: Utiliser des éléments pour Microsoft Edge (chrome) à partir du code VS
title: Éléments de Microsoft Edge (chrome) issus du code VS
author: erdraud
ms.author: erdraud
ms.date: 08/08/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, code vs, code Visual Studio, éléments
ms.openlocfilehash: 4875a4665fe1561ecf587a050bbd44e116d9ce5e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566607"
---
# Éléments pour l’extension de code Microsoft Edge VS

En ajoutant les [éléments de l’extension de code Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools) vs, vous pouvez utiliser l’outil éléments du navigateur dans le [code Visual Studio](https://code.visualstudio.com/). Par le biais d’un lancement ou d’une attachement, l’outil éléments se connecte à une instance de Microsoft Edge, affiche la structure HTML d’exécution et vous permet de modifier la disposition ou de résoudre les problèmes de style.

![Image GIF des éléments pour l’extension du code Edge et au bureau](./media/elements-for-edge.gif)

## Lancement de Microsoft Edge à partir de l’extension d’éléments 

Accédez aux éléments dans la **barre d’activité**. À côté de la mention «éléments pour Microsoft Edge: cibles», il existe un signe plus qui ouvre le navigateur de votre application. Si vous avez sélectionné l’option *à propos de: vide* , vous devrez accéder à votre application Web dans le navigateur pour qu’elle apparaisse dans le panneau d’éléments du code vs.

## Lancement de Microsoft Edge à partir de la vue de débogage

Si vous avez l’habitude d’utiliser le mode débogage dans du code Visual Studio, vous pouvez accéder à des éléments à partir de cet outil. Accédez à la vue de débogage ( `Ctrl`  +  `Shift`  +  `D` sous Windows ou `Command`  +  `Shift`  +  `D` sur Mac). 

Si vous n’avez pas de configurations dans le code VS, appuyez `F5` sur Windows ou Mac ou cliquez sur le bouton de **lecture** de couleur verte. Dans la liste déroulante, sélectionnez «Edge». Un fichier **Launch. JSON** s’affiche alors avec la configuration suivante:

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            
            "name": "Launch Microsoft Edge and open the Elements tool",
            "request": "launch",
            "type": "vscode-edge-devtools.debug",
            "url": "http://localhost:3000"
        
        }
    ]
}
```

À présent que vous avez chargé la configuration appropriée, appuyez sur `F5` Windows ou Mac ou cliquez sur le bouton de **lecture** vert. L’outil éléments qui vous est familier dans le navigateur Microsoft Edge sera lancé dans le code VS, ce qui vous permet d’accéder à un enregistrement de votre navigateur et d’examiner les composants de votre page.

## Joindre à Microsoft Edge
Si vous voulez joindre le code VS à une instance de Microsoft Edge (chrome), vous devez démarrer le navigateur en exécutant la commande suivante à partir de votre teminal:

`start msedge --remote-debugging-port=9222`

Une fois l’application lancée, ajoutez la configuration ci-dessous à votre fichier **Launch. JSON** :

```json
{
    "type": "vscode-edge-devtools.debug",
    "request": "attach",
    "name": "Attach to Microsoft Edge and open the Elements tool",
    "url": "http://localhost:3000/",
    "webRoot": "${workspaceFolder}/out",
    "port": 9222
}
```

Sélectionnez «joindre à Microsoft Edge et ouvrir l’outil éléments» dans le menu déroulant débogueur. Ensuite, appuyez sur `F5` Windows ou Mac ou cliquez sur le bouton de **lecture** de couleur verte. Le code est lancé par le biais de l’outil éléments, ce qui vous permet d’accéder à un enregistrement de votre navigateur, de vérifier le DOM et de styliser les composants sur votre page.

## Commentaires
Envoyez-nous vos commentaires en envoyant [un problème](https://github.com/microsoft/vscode-edge-devtools/issues/new) à l’aide de cette extension [GitHub référentiel Samples](https://github.com/microsoft/vscode-edge-devtools). 

Si vous souhaitez nous aider à améliorer cette extension, nous accueillons vos contributions. Vous trouverez tout ce dont vous avez besoin pour commencer à utiliser [notre GitHub référentiel Samples](https://github.com/microsoft/vscode-edge-devtools).