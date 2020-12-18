---
description: Notes de publication de la version 0,2 du protocole Microsoft Edge DevTools
title: Notes de publication de la version 0,2 du protocole Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 61d8f5b00dca3505594ca41db6c80c5ba4157092
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232848"
---
# Notes de publication de la version 0,2 du protocole DevTools

> [!NOTE]
> La version 0,2 du protocole Microsoft Edge DevTools fonctionne uniquement avec la [mise à jour de Windows 10 d’octobre 2018](/windows/uwp/whats-new/windows-10-build-17763) et les versions ultérieures de [Windows Insider Preview](https://insider.windows.com/getting-started/) .

La version 0,2 du **protocole Microsoft Edge devtools** fournit un aperçu de test de l’instrumentation EdgeHTML et de la version de débogage à distance de base dans la nouvelle application [Microsoft Edge devtools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) autonome. C’est pourquoi il est nécessaire d’exécuter la [mise à jour de Windows 10 octobre 2018](/windows/uwp/whats-new/windows-10-build-17763) ou une version ultérieure de [Windows Insider Preview](https://insider.windows.com/getting-started/) .

Les objectifs situés derrière le protocole DevTools sont à trois volets:

 - Fournir une API publique pour notre application DevTools à associer à Microsoft Edge
 - Développer l’accès à la fonctionnalité DevTools aux clients d’outils externes
 - Activez le débogage à distance sur la gamme d’appareils Windows 10 exécutant Microsoft Edge 

La version 0,2 du protocole DevTools inclut de nouveaux domaines pour le débogage de style et de mise en page (lecture seule) et les API de console, en plus de la fonctionnalité de débogage de script principal introduite dans la version 0,1. Dans l’interface utilisateur de DevTools Edge, cela se traduit par une fonctionnalité disponible dans les panneaux [**éléments**](../../devtools-guide/elements.md), [**console**](../../devtools-guide/console.md) et [**débogueur**](../../devtools-guide/debugger.md)  .
