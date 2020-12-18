---
description: Découvrez les nouveautés de la mise à jour de Microsoft Edge DevTools de Windows 10 octobre 2018
title: Nouveautés de Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, edgehtml 18
ms.custom: RS5, seodec18
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2f1d3c6fe5bf061186d5c6593a115a8b6794c0dd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233259"
---
# DevTools dans la dernière mise à jour de Windows10 (EdgeHTML 18)

La dernière mise à jour de Microsoft Edge DevTools ajoute un certain nombre de commodités à l’interface utilisateur et au capot, y compris aux nouveaux panneaux dédiés pour les [*travailleurs de services*](#service-workers-panel) et le [*stockage*](#storage-panel), les outils de [recherche de fichiers](#source-file-search-tools) source dans le débogueur et les API de console et de débogage de type [devtools](#edge-devtools-protocol-updates) .

Voici les dernières fonctionnalités de Microsoft Edge DevTools disponibles désormais dans la [mise à jour de Windows 10 d’octobre 2018](/windows/uwp/whats-new/windows-10-build-17763) ([EdgeHTML 18](https://aka.ms/devguide_edgehtml_18)). En plus de cela, nous avons également résolu un certain nombre de bogues d’accessibilité, de fiabilité et de performance pour améliorer les notions fondamentales.

## Application DevTools

Nous avons mis à jour l' [application Microsoft Edge devtools Preview](./index.md#microsoft-store-app)autonome. La version la plus récente inclut l’accès au débogage à distance aux funtionality principaux dans le [**débogueur**](./debugger.md), les [**éléments**](./elements.md) (pour les opérations en lecture seule) et les panneaux de [**console**](./console.md) .

## Panneau des travailleurs de services

Le panneau des travailleurs de [**service**](./service-workers.md) dédié est désormais destiné à l’examen, la gestion et le débogage des travailleurs de service de votre site. Cela fournit les mêmes fonctionnalités qu’auparavant dans le volet *débogueur* (désormais avec une interface utilisateur moins encombrée).

![Panneau des travailleurs de services](./media/service_worker.png)

## Panneau de stockage

Nous avons également déplacé tous les inspecteurs de stockage local (*stockage local et de stockage de groupe, IndexedDB, cookies, cache*) auparavant dans le *débogueur* pour leur propre panneau de [**stockage**](./storage.md) dédié.

![Panneau de stockage](./media/storage_cache.png)

## Outils de recherche de fichiers sources

Le [**débogueur**](./debugger.md) comporte désormais un volet de [recherche de fichier source](./debugger.md#file-search) . Vous pouvez l’ouvrir à l’aide de la commande *Rechercher dans les fichiers* ( `Ctrl` + `Shift` + `F` ) lorsque vous recherchez une chaîne de code spécifique que vous essayez de rechercher dans la source. La barre d’outils fournit des options de recherche différentes, y compris des expressions régulières. 

![Recherche de fichier de débogueur](./media/debugger_file_search.png)

Vous pouvez également ouvrir rapidement tout fichier source chargé à l’aide de la commande *ouvrir le fichier* ( `Ctrl` + `P` ).

![Débogueur-ouvrir un fichier](./media/debugger_open_file.png)

## Mises à jour du protocole Edge DevTools

La [Version 0,2](../devtools-protocol/0.2/index.md) du protocole devtools fournit de nouveaux domaines pour le débogage de style et de mise en page (lecture seule) et les API de console, en plus de la fonctionnalité de débogage de script principal introduite dans la [version 0,1](../devtools-protocol/0.1/index.md). Dans l’interface utilisateur de DevTools Edge, cela se traduit par une fonctionnalité disponible dans les [**éléments**](../devtools-guide/elements.md) (pour les opérations en lecture seule), les panneaux de [**console**](../devtools-guide/console.md) et de [**débogueur**](../devtools-guide/debugger.md) .
