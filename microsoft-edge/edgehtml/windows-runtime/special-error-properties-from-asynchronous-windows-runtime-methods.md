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
# <span data-ttu-id="06d05-103">Propriétés d’erreur particulières des méthodes Windows Runtime asynchrones</span><span class="sxs-lookup"><span data-stu-id="06d05-103">Special error properties from asynchronous Windows Runtime methods</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="06d05-104">Il peut être difficile de déboguer des méthodes Windows Runtime asynchrones en JavaScript, car l’erreur peut être levée à partir d’une pile d’appels plus profonde.</span><span class="sxs-lookup"><span data-stu-id="06d05-104">It can be difficult to debug asynchronous Windows Runtime methods in JavaScript, because the error may be thrown from somewhere deep in the call stack.</span></span>  <span data-ttu-id="06d05-105">L' `Error` objet JavaScript comporte des propriétés supplémentaires qui s’affichent uniquement lorsque l’erreur est levée à partir d’une méthode Windows Runtime asynchrone lorsque l’application s’exécute en mode débogage.</span><span class="sxs-lookup"><span data-stu-id="06d05-105">The JavaScript `Error` object has extra properties that appear only when the error is thrown from an asynchronous Windows Runtime method when the app is running in debug mode.</span></span>  
  
## <span data-ttu-id="06d05-106">Propriétés d’erreur spéciales</span><span class="sxs-lookup"><span data-stu-id="06d05-106">Special error properties</span></span>  

<span data-ttu-id="06d05-107">Un objet erreur qui résulte d’une opération asynchrone Windows Runtime en échec en mode débogage comporte les propriétés spéciales suivantes:</span><span class="sxs-lookup"><span data-stu-id="06d05-107">An error object that results from a failed Windows Runtime asynchronous operation in debug mode has the following special properties:</span></span>  

*   `asyncOpSource` <span data-ttu-id="06d05-108">\ (Objet \) obtient des informations sur l’emplacement d’origine de l’appel ayant produit une erreur.</span><span class="sxs-lookup"><span data-stu-id="06d05-108">\(Object\) Gets information about the original location where the call that produced an error was made.</span></span>  <span data-ttu-id="06d05-109">La propriété `asyncOpSource.originatingCall` \ (chaîne \) affiche l’emplacement dans le code de l’utilisateur à l’origine de l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="06d05-109">The property `asyncOpSource.originatingCall` \(String\) displays the location in the user's code that originated the asynchronous operation.</span></span>  
*   <span data-ttu-id="06d05-110">asyncOpType \ (chaîne \) obtient le nom du type d’opération asynchrone qui a déclenché l’erreur.</span><span class="sxs-lookup"><span data-stu-id="06d05-110">asyncOpType \(String\) Gets the name of the asynchronous operation type that raised the error.</span></span>  
    
<span data-ttu-id="06d05-111">Pour plus d’informations sur les erreurs liées aux opérations asynchrones, voir:</span><span class="sxs-lookup"><span data-stu-id="06d05-111">For more information about errors with asynchronous operations, see:</span></span>  
  
*   [<span data-ttu-id="06d05-112">Gestion des erreurs liées aux promesses</span><span class="sxs-lookup"><span data-stu-id="06d05-112">How to handle errors with promises</span></span>][PreviousVersionsWindowsAppsHh700337]  
*   [<span data-ttu-id="06d05-113">Résolution des erreurs Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="06d05-113">Troubleshooting Windows Runtime errors</span></span>][PreviousVersionsWindowsAppsHh974350]  

<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Gestion des erreurs liées aux promesses Documents Microsoft"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Résolution des erreurs Windows Runtime (HTML) | Documents Microsoft"  
