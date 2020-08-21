---
title: Propriétés d’erreur particulières des méthodes Windows Runtime asynchrones
ms.custom: ''
ms.date: 07/29/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 45155584-06d8-4e7f-93a6-8564a93f643d
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: a1fccf1cec811501b94e7da4aa20b69d93754f62
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942065"
---
# <span data-ttu-id="41eee-102">Propriétés d’erreur particulières des méthodes Windows Runtime asynchrones</span><span class="sxs-lookup"><span data-stu-id="41eee-102">Special error properties from asynchronous Windows Runtime methods</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="41eee-103">Il peut être difficile de déboguer des méthodes Windows Runtime asynchrones en JavaScript, car l’erreur peut être levée à partir d’une pile d’appels plus profonde.</span><span class="sxs-lookup"><span data-stu-id="41eee-103">It can be difficult to debug asynchronous Windows Runtime methods in JavaScript, because the error may be thrown from somewhere deep in the call stack.</span></span>  <span data-ttu-id="41eee-104">L' `Error` objet JavaScript comporte des propriétés supplémentaires qui s’affichent uniquement lorsque l’erreur est levée à partir d’une méthode Windows Runtime asynchrone lorsque l’application s’exécute en mode débogage.</span><span class="sxs-lookup"><span data-stu-id="41eee-104">The JavaScript `Error` object has extra properties that appear only when the error is thrown from an asynchronous Windows Runtime method when the app is running in debug mode.</span></span>  
  
## <span data-ttu-id="41eee-105">Propriétés d’erreur spéciales</span><span class="sxs-lookup"><span data-stu-id="41eee-105">Special error properties</span></span>  

<span data-ttu-id="41eee-106">Un objet erreur qui résulte d’une opération asynchrone Windows Runtime en échec en mode débogage comporte les propriétés spéciales suivantes:</span><span class="sxs-lookup"><span data-stu-id="41eee-106">An error object that results from a failed Windows Runtime asynchronous operation in debug mode has the following special properties:</span></span>  

*   `asyncOpSource` <span data-ttu-id="41eee-107">\ (Objet \) obtient des informations sur l’emplacement d’origine de l’appel ayant produit une erreur.</span><span class="sxs-lookup"><span data-stu-id="41eee-107">\(Object\) Gets information about the original location where the call that produced an error was made.</span></span>  <span data-ttu-id="41eee-108">La propriété `asyncOpSource.originatingCall` \ (chaîne \) affiche l’emplacement dans le code de l’utilisateur à l’origine de l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="41eee-108">The property `asyncOpSource.originatingCall` \(String\) displays the location in the user's code that originated the asynchronous operation.</span></span>  
*   <span data-ttu-id="41eee-109">asyncOpType \ (chaîne \) obtient le nom du type d’opération asynchrone qui a déclenché l’erreur.</span><span class="sxs-lookup"><span data-stu-id="41eee-109">asyncOpType \(String\) Gets the name of the asynchronous operation type that raised the error.</span></span>  
    
<span data-ttu-id="41eee-110">Pour plus d’informations sur les erreurs liées aux opérations asynchrones, voir:</span><span class="sxs-lookup"><span data-stu-id="41eee-110">For more information about errors with asynchronous operations, see:</span></span>  
  
*   [<span data-ttu-id="41eee-111">Gestion des erreurs liées aux promesses</span><span class="sxs-lookup"><span data-stu-id="41eee-111">How to handle errors with promises</span></span>][PreviousVersionsWindowsAppsHh700337]  
*   [<span data-ttu-id="41eee-112">Résolution des erreurs Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="41eee-112">Troubleshooting Windows Runtime errors</span></span>][PreviousVersionsWindowsAppsHh974350]  

<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Gestion des erreurs liées aux promesses Documents Microsoft"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Résolution des erreurs Windows Runtime (HTML) | Documents Microsoft"  
