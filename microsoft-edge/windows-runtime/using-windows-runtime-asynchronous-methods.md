---
title: Utilisation de méthodes asynchrones Windows Runtime
ms.custom: ''
ms.date: 04/01/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime asynchronous methods
ms.assetid: 70756833-44f7-4383-827f-2ac781558082
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6d0f174d22d0d13571d78bc215356ad90a0ae7fa
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566642"
---
# <span data-ttu-id="1fbb6-102">Utilisation de méthodes asynchrones Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="1fbb6-102">Using Windows Runtime Asynchronous Methods</span></span>  

<span data-ttu-id="1fbb6-103">De nombreuses méthodes Windows Runtime, notamment les méthodes qui peuvent nécessiter un certain temps, sont asynchrones.</span><span class="sxs-lookup"><span data-stu-id="1fbb6-103">Many Windows Runtime methods, especially methods that might take a long time to complete, are asynchronous.</span></span>  <span data-ttu-id="1fbb6-104">Ces méthodes renvoient généralement une action ou une opération asynchrone (par exemple,,, `Windows.Foundation.IAsyncAction` `Windows.Foundation.IAsyncOperation` `Windows.Foundation.IAsyncActionWithProgress` ou `Windows.Foundation.IAsyncOperationWithProgress` ).</span><span class="sxs-lookup"><span data-stu-id="1fbb6-104">These methods generally return an asynchronous action or operation (for example, `Windows.Foundation.IAsyncAction`, `Windows.Foundation.IAsyncOperation`, `Windows.Foundation.IAsyncActionWithProgress`, or `Windows.Foundation.IAsyncOperationWithProgress`).</span></span>  <span data-ttu-id="1fbb6-105">Ces méthodes sont représentées dans JavaScript par le [modèle CommonJS/promet/A][CommonjsWikiPromises].</span><span class="sxs-lookup"><span data-stu-id="1fbb6-105">These methods are represented in JavaScript by the [CommonJS/Promises/A pattern][CommonjsWikiPromises].</span></span>  <span data-ttu-id="1fbb6-106">En d’autres cas, elle renvoie un objet promise qui dispose d’une [fonction Then][PreviousVersionsWindowsAppsBr229728]pour laquelle vous devez fournir une `completed` fonction qui gère le résultat si l’opération aboutit.</span><span class="sxs-lookup"><span data-stu-id="1fbb6-106">That is, they return a Promise object that has a [then function][PreviousVersionsWindowsAppsBr229728], for which you must provide a `completed` function that handles the result if the operation succeeds.</span></span>  <span data-ttu-id="1fbb6-107">Si vous ne souhaitez pas fournir de gestionnaire d’erreur, vous devez utiliser la [fonction réalisé][PreviousVersionsWindowsAppsHr701079] au lieu de la `then` fonction.</span><span class="sxs-lookup"><span data-stu-id="1fbb6-107">If you don't want to provide an error handler, you should use the [done function][PreviousVersionsWindowsAppsHr701079] instead of the `then` function.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="1fbb6-108">Les fonctionnalités Windows Runtime ne sont pas disponibles pour les applications qui s’exécutent dans Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="1fbb6-108">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <span data-ttu-id="1fbb6-109">Exemples de méthodes asynchrones</span><span class="sxs-lookup"><span data-stu-id="1fbb6-109">Examples of Asynchronous Methods</span></span>  

<span data-ttu-id="1fbb6-110">Dans l’exemple suivant, la `then` fonction prend un paramètre qui représente la valeur achevée de la `createResourceAsync` méthode.</span><span class="sxs-lookup"><span data-stu-id="1fbb6-110">In the following example, the `then` function takes a parameter that represents the completed value of the `createResourceAsync` method.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
        console.log("New item is: " + newItem.id);
            });
```  

<span data-ttu-id="1fbb6-111">Dans ce cas, si la `createResourceAsync` méthode échoue, elle renvoie une promesse dans l’état d’erreur, mais ne lève pas d’exception.</span><span class="sxs-lookup"><span data-stu-id="1fbb6-111">In this case, if the `createResourceAsync` method fails, it returns a promise in the error state, but does not throw an exception.</span></span>  <span data-ttu-id="1fbb6-112">Vous pouvez gérer une erreur à l’aide de la `then` fonction comme suit.</span><span class="sxs-lookup"><span data-stu-id="1fbb6-112">You can handle an error by using the `then` function as follows.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
              console.log("New item is: " + newItem.id);
          }
          function(err) {
              console.log("Got error: " + err.message);
          });
```  

<span data-ttu-id="1fbb6-113">Si vous ne souhaitez pas gérer l’erreur explicitement, mais que vous souhaitez qu’elle lève une exception, vous pouvez utiliser la fonction à la `done` place.</span><span class="sxs-lookup"><span data-stu-id="1fbb6-113">If you don't want to handle the error explicitly, but do want it to throw an exception, you can use the `done` function instead.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .done(function(newItem) {
               console.log("New item is: " + newItem.id);
            });
```  

<span data-ttu-id="1fbb6-114">Vous pouvez également afficher l’avancement réalisé vers la fin à l’aide d’une troisième fonction.</span><span class="sxs-lookup"><span data-stu-id="1fbb6-114">You can also display the progress made towards completion by using a third function.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .then(function(newItem) {
               console.log("New item is: " + newItem.id);
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

<span data-ttu-id="1fbb6-115">Pour plus d’informations sur la programmation asynchrone, voir [programmation asynchrone en JavaScript][PreviousVersionsWindowsAppsHh700330].</span><span class="sxs-lookup"><span data-stu-id="1fbb6-115">For more information about asynchronous programming, see [Asynchronous Programming in JavaScript][PreviousVersionsWindowsAppsHh700330].</span></span>  

## <span data-ttu-id="1fbb6-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fbb6-116">See Also</span></span>  

[<span data-ttu-id="1fbb6-117">Utilisation de Windows Runtime en JavaScript</span><span class="sxs-lookup"><span data-stu-id="1fbb6-117">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

<!-- image links -->  

<!-- links -->  

[WindowsRuntimeJavascript]: /microsoft-edge/windows-runtime/using-the-windows-runtime-in-javascript "Utilisation de Windows Runtime en JavaScript"  

[PreviousVersionsWindowsAppsBr229728]: /previous-versions/windows/apps/br229728(v=win.10) "Promesse. Then"  
[PreviousVersionsWindowsAppsHh700330]: /previous-versions/windows/apps/hh700330(v=win.10) "Programmation asynchrone en JavaScript (HTML)"
[PreviousVersionsWindowsAppsHr701079]: /previous-versions/windows/apps/hh701079(v=win.10) "Méthode promise. réalisé"  

[CommonjsWikiPromises]: http://wiki.commonjs.org/wiki/Promises "Promet | Wiki spec CommonJS"  
