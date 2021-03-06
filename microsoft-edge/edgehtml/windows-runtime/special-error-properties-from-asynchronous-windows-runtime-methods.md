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
# <a name="special-error-properties-from-asynchronous-windows-runtime-methods"></a><span data-ttu-id="e9be8-103">Propriétés d’erreur particulières des méthodes Windows Runtime asynchrones</span><span class="sxs-lookup"><span data-stu-id="e9be8-103">Special error properties from asynchronous Windows Runtime methods</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="e9be8-104">Il peut être difficile de déboguer des méthodes Windows Runtime asynchrones en JavaScript, car l’erreur peut être lancée à partir d’un endroit profond dans la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="e9be8-104">It can be difficult to debug asynchronous Windows Runtime methods in JavaScript, because the error may be thrown from somewhere deep in the call stack.</span></span>  <span data-ttu-id="e9be8-105">L’objet JavaScript possède des propriétés supplémentaires qui apparaissent uniquement lorsque l’erreur est lancée à partir d’une méthode Windows Runtime asynchrone lorsque l’application s’exécute en `Error` mode débogage.</span><span class="sxs-lookup"><span data-stu-id="e9be8-105">The JavaScript `Error` object has extra properties that appear only when the error is thrown from an asynchronous Windows Runtime method when the app is running in debug mode.</span></span>  
  
## <a name="special-error-properties"></a><span data-ttu-id="e9be8-106">Propriétés d’erreur spéciales</span><span class="sxs-lookup"><span data-stu-id="e9be8-106">Special error properties</span></span>  

<span data-ttu-id="e9be8-107">Un objet d’erreur qui résulte d’une opération asynchrone Windows Runtime en mode débogage a les propriétés spéciales suivantes :</span><span class="sxs-lookup"><span data-stu-id="e9be8-107">An error object that results from a failed Windows Runtime asynchronous operation in debug mode has the following special properties:</span></span>  

*   `asyncOpSource` <span data-ttu-id="e9be8-108">\(Object\) Obtient des informations sur l’emplacement d’origine où l’appel qui a produit une erreur a été effectué.</span><span class="sxs-lookup"><span data-stu-id="e9be8-108">\(Object\) Gets information about the original location where the call that produced an error was made.</span></span>  <span data-ttu-id="e9be8-109">La propriété \(String\) affiche l’emplacement dans le code de `asyncOpSource.originatingCall` l’utilisateur à l’origine de l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e9be8-109">The property `asyncOpSource.originatingCall` \(String\) displays the location in the user's code that originated the asynchronous operation.</span></span>  
*   <span data-ttu-id="e9be8-110">asyncOpType \(String\) Obtient le nom du type d’opération asynchrone qui a levé l’erreur.</span><span class="sxs-lookup"><span data-stu-id="e9be8-110">asyncOpType \(String\) Gets the name of the asynchronous operation type that raised the error.</span></span>  
    
<span data-ttu-id="e9be8-111">Pour plus d’informations sur les erreurs avec des opérations asynchrones, voir :</span><span class="sxs-lookup"><span data-stu-id="e9be8-111">For more information about errors with asynchronous operations, see:</span></span>  

*   [<span data-ttu-id="e9be8-112">Comment gérer les erreurs avec les promesses</span><span class="sxs-lookup"><span data-stu-id="e9be8-112">How to handle errors with promises</span></span>][PreviousVersionsWindowsAppsHh700337]  
*   [<span data-ttu-id="e9be8-113">Résolution des erreurs Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="e9be8-113">Troubleshooting Windows Runtime errors</span></span>][PreviousVersionsWindowsAppsHh974350]  
    
<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Comment gérer les erreurs avec des promesses (HTML) | Documents Microsoft"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Résolution des erreurs Windows Runtime (HTML) | Documents Microsoft"  
