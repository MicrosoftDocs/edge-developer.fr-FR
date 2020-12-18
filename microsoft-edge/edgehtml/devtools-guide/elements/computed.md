---
description: Utiliser le volet calculé pour comprendre la manière dont votre CSS effectue une cascade et des calculs sur des éléments de page
title: DevTools-éléments calculés
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, éléments, CSS, valeur calculée, zone modèle
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e88b96a08ac22c56ac6578495311931d265247bb
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232910"
---
# Calculée

Regardez un diagramme de modèle de cadre (Width, Padding, bordure, marge et valeurs de décalage) de l’élément sélectionné. Si vous activez l’outil de **mise en surbrillance des éléments** ( `Ctrl+Shift+L` ), les mêmes régions de couleur que vous avez affichées dans le diagramme (pour Width, Padding, etc.) qui s’affichent à l’écran. Vous pouvez modifier n’importe quelle valeur dans le diagramme en cliquant dessus. 

Le diagramme de modèle de cadre est une liste filtrable et éditable de propriétés de style calculées. La désactivation d’une propriété active active la propriété Next dans la cascade, s’il en existe une. Vous pouvez afficher vos modifications dans le volet [**modifications**](./changes.md) .

Le bouton **afficher uniquement les styles utilisateur** est activé par défaut. La pression sur le bouton inclut les styles de la *feuille de calcul par défaut* de Microsoft Edge dans la liste styles calculés.

![Volet calculé](../media/elements_computed.png)
