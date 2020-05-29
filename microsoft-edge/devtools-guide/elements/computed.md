---
description: Utiliser le volet calculé pour comprendre la manière dont votre CSS effectue une cascade et des calculs sur des éléments de page
title: DevTools-éléments calculés
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/10/2017
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, éléments, CSS, valeur calculée, zone modèle
ms.custom: seodec18
ms.openlocfilehash: c7b1b7c86f30e6947442c9b3d0e8856074ce4c8e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566348"
---
# Calculée

Regardez un diagramme de modèle de cadre (Width, Padding, bordure, marge et valeurs de décalage) de l’élément sélectionné. Si vous activez l’outil de **mise en surbrillance des éléments** ( `Ctrl+Shift+L` ), les mêmes régions de couleur que vous avez affichées dans le diagramme (pour Width, Padding, etc.) qui s’affichent à l’écran. Vous pouvez modifier n’importe quelle valeur dans le diagramme en cliquant dessus. 

Le diagramme de modèle de cadre est une liste filtrable et éditable de propriétés de style calculées. La désactivation d’une propriété active active la propriété Next dans la cascade, s’il en existe une. Vous pouvez afficher vos modifications dans le volet [**modifications**](./changes.md) .

Le bouton **afficher uniquement les styles utilisateur** est activé par défaut. La pression sur le bouton inclut les styles de la *feuille de calcul par défaut* de Microsoft Edge dans la liste styles calculés.

![Volet calculé](../media/elements_computed.png)