---
description: Mode IE et Microsoft Edge (chrome) DevTools
title: Le mode Internet Explorer et le DevTools
author: robpaveza
ms.author: ropaveza
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, ie11, Internet Explorer 11, mode IE
ms.openlocfilehash: 18e5f029d277e446857ec48b9cf129149f219256
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566229"
---
# Le mode Internet Explorer et le DevTools

Ce document décrit comment le mode d’affichage d’Internet Explorer (le mode IE) est intégré à Microsoft Edge (chrome) DevTools.

## Présentation du mode IE

Le mode IE est un mécanisme par lequel les entreprises pourront spécifier un ensemble de sites Web qui, à l’heure actuelle, ne fonctionnaient qu’avec Internet Explorer 11. Lorsque ces sites Web sont consultés dans Microsoft Edge (chrome), une instance complète d’Internet Explorer 11 s’exécute et s’affiche dans l’onglet. Cela permet aux entreprises de gérer la compatibilité du mode document d’Internet Explorer, des contrôles ActiveX et des autres composants hérités actuellement non compatibles avec les navigateurs Web modernes.

Dans le mode IE, le processus de rendu s’appuie entièrement sur Internet Explorer 11. Le processus Gestionnaire Microsoft Edge (chrome) gère la durée de vie du processus de rendu, mais il est contraint en fonction de la durée de vie de l’onglet sur un site ou une application donnée. Lorsque le mode d’affichage d’un onglet est affiché en mode IE, un badge s’affiche dans la barre d’adresses de l’onglet donné:

![Badge du mode IE dans la barre d’adresses](./media/ie-mode-badge.png)

Le mode IE est actuellement disponible sur Windows 10, version 1903 (mise à jour de 2019), mais bientôt disponible sur toutes les plateformes Windows prises en charge.

## Lancement de DevTools sur un onglet du mode IE

Si vous essayez d’afficher le mode document d’un site Web dans le mode IE, vous pouvez cliquer sur le badge dans la barre d’adresses.

![Afficher le mode document via le mode IE](./media/ie-mode-badge-doc-mode.png)

Dans un onglet du mode IE, le DevTools ne fonctionnera pas. Appuyer sur `F12` ou `Ctrl` + `Shift` + `I` lancer une instance vide de Microsoft Edge (chrome) devtools avec un message qui indique: «les outils de développement ne sont pas disponibles en mode Internet Explorer. Pour déboguer la page, ouvrez-la dans Internet Explorer 11. La **source d’affichage** démarre le bloc-notes et **inspecter l’élément** ne sera pas visible dans le menu contextuel du mode IE.

Cela est dû au fait qu’un certain nombre de composants dans le DevTools (par exemple, les outils réseau et performance) s’arrête lorsque le moteur de rendu bascule du chrome vers Internet Explorer 11 en mode IE. Pour nous envoyer des commentaires, cliquez sur l' `:)` icône.

![DevTools lancée en mode IE](./media/ie-mode-devtools.png)

Si vous développez ou maintenez une application ou un site Web Internet Explorer 11, nous vous conseillons d’accéder à la même page dans Internet Explorer 11. Sur Windows 10, le raccourci vers Internet Explorer 11 se trouve dans le menu Démarrer, sous accessoires Windows. Sur Windows 7, le menu Démarrer principal vous permet d’accéder à Internet Explorer 11. Vous pouvez ensuite lancer Internet Explorer DevTools en appuyant `F12` ou en cliquant sur **inspecter l’élément** dans le menu contextuel. Pour en savoir plus sur l’utilisation de ces outils, cliquez [ici](/previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85)).

## Débogage à distance et mode IE

Vous pouvez lancer Microsoft Edge (chrome) sur lequel le débogage à distance est activé, qui est généralement le mode d’affichage des outils tels que Visual Studio ou la version latérale du code VS, à partir de la ligne de commande:

`start msedge --remote-debugging-port=9222`

Lorsque Microsoft Edge (chrome) est lancé avec cet argument de ligne de commande, le mode IE ne sera pas disponible. Vous pouvez toujours accéder à des sites Web ou des applications qui seraient autrement dans le mode IE, mais le contenu s’affichera par chrome, pas par Internet Explorer 11. Vous pouvez vous attendre à ce que les parties de ces pages qui s’appuient sur IE11, comme les contrôles ActiveX, ne s’affichent pas correctement. Le badge du mode IE ne s’affichera plus dans la barre d’adresses.

Le mode IE ne sera pas disponible tant que vous n’aurez pas complètement fermé Microsoft Edge (chrome).