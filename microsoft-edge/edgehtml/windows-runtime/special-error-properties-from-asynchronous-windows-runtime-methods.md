---
description: Propriétés d’erreur particulières des méthodes Windows Runtime asynchrones
title: Propriétés d’erreur particulières des méthodes Windows Runtime asynchrones
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
ms.assetid: 45155584-06d8-4e7f-93a6-8564a93f643d
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d9f2fdb007f00c2ab1d1a2050378af80f0075db6
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398839"
---
# <a name="special-error-properties-from-asynchronous-windows-runtime-methods"></a>Propriétés d’erreur particulières des méthodes Windows Runtime asynchrones  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Il peut être difficile de déboguer des méthodes Windows Runtime asynchrones en JavaScript, car l’erreur peut être lancée à partir d’un endroit profond dans la pile d’appels.  L’objet JavaScript possède des propriétés supplémentaires qui apparaissent uniquement lorsque l’erreur est lancée à partir d’une méthode Windows Runtime asynchrone lorsque l’application s’exécute en `Error` mode débogage.  
  
## <a name="special-error-properties"></a>Propriétés d’erreur spéciales  

Un objet d’erreur qui résulte d’une opération asynchrone Windows Runtime en mode débogage a les propriétés spéciales suivantes :  

*   `asyncOpSource` \(Object\) Obtient des informations sur l’emplacement d’origine où l’appel qui a produit une erreur a été effectué.  La propriété \(String\) affiche l’emplacement dans le code de `asyncOpSource.originatingCall` l’utilisateur à l’origine de l’opération asynchrone.  
*   asyncOpType \(String\) Obtient le nom du type d’opération asynchrone qui a levé l’erreur.  
    
Pour plus d’informations sur les erreurs avec des opérations asynchrones, voir :  

*   [Comment gérer les erreurs avec les promesses][PreviousVersionsWindowsAppsHh700337]  
*   [Résolution des erreurs Windows Runtime][PreviousVersionsWindowsAppsHh974350]  
    
<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Comment gérer les erreurs avec des promesses (HTML) | Documents Microsoft"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Résolution des erreurs Windows Runtime (HTML) | Documents Microsoft"  
