---
description: Utilisation des méthodes asynchrones Windows Runtime
title: Utilisation des méthodes asynchrones Windows Runtime
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime asynchronous methods
ms.assetid: 70756833-44f7-4383-827f-2ac781558082
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c7e8ac4690525ee89a06eccf843531c2c7a20324
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398153"
---
# <a name="using-windows-runtime-asynchronous-methods"></a><span data-ttu-id="f6693-103">Utilisation des méthodes asynchrones Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="f6693-103">Using Windows Runtime asynchronous methods</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="f6693-104">De nombreuses méthodes Windows Runtime, notamment les méthodes qui peuvent prendre beaucoup de temps, sont asynchrones.</span><span class="sxs-lookup"><span data-stu-id="f6693-104">Many Windows Runtime methods, especially methods that might take a long time to complete, are asynchronous.</span></span>  <span data-ttu-id="f6693-105">Ces méthodes retournent généralement une action ou une opération asynchrone \(par exemple, `Windows.Foundation.IAsyncAction` `Windows.Foundation.IAsyncOperation` , , ou `Windows.Foundation.IAsyncActionWithProgress` `Windows.Foundation.IAsyncOperationWithProgress` \).</span><span class="sxs-lookup"><span data-stu-id="f6693-105">These methods generally return an asynchronous action or operation \(for example, `Windows.Foundation.IAsyncAction`, `Windows.Foundation.IAsyncOperation`, `Windows.Foundation.IAsyncActionWithProgress`, or `Windows.Foundation.IAsyncOperationWithProgress`\).</span></span>  <span data-ttu-id="f6693-106">Ces méthodes sont représentées dans JavaScript par le [modèle CommonJS/Promises/A][CommonjsWikiPromises].</span><span class="sxs-lookup"><span data-stu-id="f6693-106">These methods are represented in JavaScript by the [CommonJS/Promises/A pattern][CommonjsWikiPromises].</span></span>  <span data-ttu-id="f6693-107">Autrement dit, ils retournent un objet Promise qui a une fonction [then,][PreviousVersionsWindowsAppsBr229728]pour laquelle vous devez fournir une fonction qui gère le résultat si l’opération `completed` réussit.</span><span class="sxs-lookup"><span data-stu-id="f6693-107">That is, they return a Promise object that has a [then function][PreviousVersionsWindowsAppsBr229728], for which you must provide a `completed` function that handles the result if the operation succeeds.</span></span>  <span data-ttu-id="f6693-108">Si vous ne souhaitez pas fournir de handler d’erreurs, vous devez utiliser la fonction [done][PreviousVersionsWindowsAppsHr701079] au lieu de la `then` fonction.</span><span class="sxs-lookup"><span data-stu-id="f6693-108">If you don't want to provide an error handler, you should use the [done function][PreviousVersionsWindowsAppsHr701079] instead of the `then` function.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="f6693-109">Les fonctionnalités Windows Runtime ne sont pas disponibles pour les applications qui s’exécutent dans Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="f6693-109">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <a name="examples-of-asynchronous-methods"></a><span data-ttu-id="f6693-110">Exemples de méthodes asynchrones</span><span class="sxs-lookup"><span data-stu-id="f6693-110">Examples of asynchronous methods</span></span>  

<span data-ttu-id="f6693-111">Dans l’exemple suivant, la fonction prend un paramètre qui `then` représente la valeur terminée de la `createResourceAsync` méthode.</span><span class="sxs-lookup"><span data-stu-id="f6693-111">In the following example, the `then` function takes a parameter that represents the completed value of the `createResourceAsync` method.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
        console.log("New item is: " + newItem.id);
            });
```  

<span data-ttu-id="f6693-112">Dans ce cas, si la méthode échoue, elle renvoie une promesse à l’état d’erreur, mais ne renvoie `createResourceAsync` pas d’exception.</span><span class="sxs-lookup"><span data-stu-id="f6693-112">In this case, if the `createResourceAsync` method fails, it returns a promise in the error state, but does not throw an exception.</span></span>  <span data-ttu-id="f6693-113">Vous pouvez gérer une erreur en utilisant la `then` fonction comme suit.</span><span class="sxs-lookup"><span data-stu-id="f6693-113">You can handle an error by using the `then` function as follows.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
              console.log("New item is: " + newItem.id);
          }
          function(err) {
              console.log("Got error: " + err.message);
          });
```  

<span data-ttu-id="f6693-114">Si vous ne souhaitez pas gérer l’erreur explicitement, mais que vous souhaitez qu’elle lance une exception, vous pouvez utiliser la `done` fonction à la place.</span><span class="sxs-lookup"><span data-stu-id="f6693-114">If you don't want to handle the error explicitly, but do want it to throw an exception, you can use the `done` function instead.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .done(function(newItem) {
               console.log("New item is: " + newItem.id);
            });
```  

<span data-ttu-id="f6693-115">Vous pouvez également afficher la progression vers l’achèvement à l’aide d’une troisième fonction.</span><span class="sxs-lookup"><span data-stu-id="f6693-115">You can also display the progress made towards completion by using a third function.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .then(function(newItem) {
               console.log("New item is: " + newItem.id);
            },
    // Error.
            function(error) {
               alert("Failed to create a resource.");
            },
    // Progress.
            function(progress, resultSoFar) {
               setProgressBar(progress);
            });
```  

<span data-ttu-id="f6693-116">Pour plus d’informations sur la programmation asynchrone, voir [Programmation asynchrone en JavaScript][PreviousVersionsWindowsAppsHh700330].</span><span class="sxs-lookup"><span data-stu-id="f6693-116">For more information about asynchronous programming, see [Asynchronous Programming in JavaScript][PreviousVersionsWindowsAppsHh700330].</span></span>  

## <a name="see-also"></a><span data-ttu-id="f6693-117">Voir également</span><span class="sxs-lookup"><span data-stu-id="f6693-117">See also</span></span>  

[<span data-ttu-id="f6693-118">Utilisation de Windows Runtime en JavaScript</span><span class="sxs-lookup"><span data-stu-id="f6693-118">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Utilisation de Windows Runtime en JavaScript | Documents Microsoft"  

[PreviousVersionsWindowsAppsBr229728]: /previous-versions/windows/apps/br229728(v=win.10) "Méthode Promise.then | Documents Microsoft"  
[PreviousVersionsWindowsAppsHh700330]: /previous-versions/windows/apps/hh700330(v=win.10) "Programmation asynchrone en JavaScript (HTML) | Documents Microsoft"
[PreviousVersionsWindowsAppsHr701079]: /previous-versions/windows/apps/hh701079(v=win.10) "Méthode Promise.done | Documents Microsoft"  

[CommonjsWikiPromises]: http://wiki.commonjs.org/wiki/Promises "Promesses | CommonJS Spec Wiki"  
