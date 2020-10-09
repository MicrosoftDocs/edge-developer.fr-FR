---
description: Notes de publication de la version 0,1 du protocole Microsoft Edge DevTools
title: Notes de publication de la version 0,1 du protocole DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 3c0648467c20572a525fe257788068966efd193c
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104734"
---
# Notes de publication de la version 0,1 du protocole DevTools

> [!NOTE]
> Le protocole Microsoft Edge DevTools fonctionne uniquement sur les [mises à jour de Windows 10 d’avril 2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) et les versions ultérieures de [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .

La version 0,1 du **protocole Microsoft Edge devtools** fournit une version d’évaluation préliminaire pour le test de l’instrumentation EdgeHTML et du débogage à distance de base dans la nouvelle application [Microsoft Edge devtools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) autonome. C’est pourquoi il est nécessaire d’exécuter la [mise à jour de Windows 10 d’avril 2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) ou une version ultérieure de [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .

Les objectifs situés derrière le protocole DevTools sont à trois volets:

 - Fournir une API publique pour notre application DevTools à associer à Microsoft Edge
 - Développer l’accès à la fonctionnalité DevTools aux clients d’outils externes
 - Activez le débogage à distance sur la gamme d’appareils Windows 10 exécutant Microsoft Edge 

Cette version préliminaire fournit une fonctionnalité de débogage de base, comme la définition de points d’arrêt, l’exécution du code et l’exploration des traces de pile. Dans l’interface utilisateur de DevTools Edge, cela se traduit par une fonctionnalité disponible dans le volet [**débogueur**](../../devtools-guide/debugger.md) , l’inspection du cache (pour le stockage Web, le travailleur de service, l’API de cache et IndexedDB). 

Les fonctionnalités de débogueur supplémentaires seront ajoutées dans les versions à venir, suivies de l’instrumentation qui alimente d’autres panneaux [devtools](../../devtools-guide.md) .
