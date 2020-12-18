---
description: Propriétés d’erreur particulières des méthodes Windows Runtime asynchrones.
title: Propriétés d’erreur particulières des méthodes Windows Runtime asynchrones
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
ms.assetid: 45155584-06d8-4e7f-93a6-8564a93f643d
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3557d0097d632f4058e46acbff748f7177d24ab1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233093"
---
# Propriétés d’erreur particulières des méthodes Windows Runtime asynchrones  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Il peut être difficile de déboguer des méthodes Windows Runtime asynchrones en JavaScript, car l’erreur peut être levée à partir d’une pile d’appels plus profonde.  L' `Error` objet JavaScript comporte des propriétés supplémentaires qui s’affichent uniquement lorsque l’erreur est levée à partir d’une méthode Windows Runtime asynchrone lorsque l’application s’exécute en mode débogage.  
  
## Propriétés d’erreur spéciales  

Un objet erreur qui résulte d’une opération asynchrone Windows Runtime en échec en mode débogage comporte les propriétés spéciales suivantes:  

*   `asyncOpSource` \ (Objet \) obtient des informations sur l’emplacement d’origine de l’appel ayant produit une erreur.  La propriété `asyncOpSource.originatingCall` \ (chaîne \) affiche l’emplacement dans le code de l’utilisateur à l’origine de l’opération asynchrone.  
*   asyncOpType \ (chaîne \) obtient le nom du type d’opération asynchrone qui a déclenché l’erreur.  
    
Pour plus d’informations sur les erreurs liées aux opérations asynchrones, voir:  
  
*   [Gestion des erreurs liées aux promesses][PreviousVersionsWindowsAppsHh700337]  
*   [Résolution des erreurs Windows Runtime][PreviousVersionsWindowsAppsHh974350]  

<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Gestion des erreurs liées aux promesses Documents Microsoft"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Résolution des erreurs Windows Runtime (HTML) | Documents Microsoft"  
