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
# <a name="using-windows-runtime-asynchronous-methods"></a>Utilisation des méthodes asynchrones Windows Runtime  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

De nombreuses méthodes Windows Runtime, notamment les méthodes qui peuvent prendre beaucoup de temps, sont asynchrones.  Ces méthodes retournent généralement une action ou une opération asynchrone \(par exemple, `Windows.Foundation.IAsyncAction` `Windows.Foundation.IAsyncOperation` , , ou `Windows.Foundation.IAsyncActionWithProgress` `Windows.Foundation.IAsyncOperationWithProgress` \).  Ces méthodes sont représentées dans JavaScript par le [modèle CommonJS/Promises/A][CommonjsWikiPromises].  Autrement dit, ils retournent un objet Promise qui a une fonction [then,][PreviousVersionsWindowsAppsBr229728]pour laquelle vous devez fournir une fonction qui gère le résultat si l’opération `completed` réussit.  Si vous ne souhaitez pas fournir de handler d’erreurs, vous devez utiliser la fonction [done][PreviousVersionsWindowsAppsHr701079] au lieu de la `then` fonction.  

> [!IMPORTANT]
> Les fonctionnalités Windows Runtime ne sont pas disponibles pour les applications qui s’exécutent dans Internet Explorer.  

## <a name="examples-of-asynchronous-methods"></a>Exemples de méthodes asynchrones  

Dans l’exemple suivant, la fonction prend un paramètre qui `then` représente la valeur terminée de la `createResourceAsync` méthode.  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
        console.log("New item is: " + newItem.id);
            });
```  

Dans ce cas, si la méthode échoue, elle renvoie une promesse à l’état d’erreur, mais ne renvoie `createResourceAsync` pas d’exception.  Vous pouvez gérer une erreur en utilisant la `then` fonction comme suit.  

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

Si vous ne souhaitez pas gérer l’erreur explicitement, mais que vous souhaitez qu’elle lance une exception, vous pouvez utiliser la `done` fonction à la place.  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .done(function(newItem) {
               console.log("New item is: " + newItem.id);
            });
```  

Vous pouvez également afficher la progression vers l’achèvement à l’aide d’une troisième fonction.  

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

Pour plus d’informations sur la programmation asynchrone, voir [Programmation asynchrone en JavaScript][PreviousVersionsWindowsAppsHh700330].  

## <a name="see-also"></a>Voir également  

[Utilisation de Windows Runtime en JavaScript][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Utilisation de Windows Runtime en JavaScript | Documents Microsoft"  

[PreviousVersionsWindowsAppsBr229728]: /previous-versions/windows/apps/br229728(v=win.10) "Méthode Promise.then | Documents Microsoft"  
[PreviousVersionsWindowsAppsHh700330]: /previous-versions/windows/apps/hh700330(v=win.10) "Programmation asynchrone en JavaScript (HTML) | Documents Microsoft"
[PreviousVersionsWindowsAppsHr701079]: /previous-versions/windows/apps/hh701079(v=win.10) "Méthode Promise.done | Documents Microsoft"  

[CommonjsWikiPromises]: http://wiki.commonjs.org/wiki/Promises "Promesses | CommonJS Spec Wiki"  
