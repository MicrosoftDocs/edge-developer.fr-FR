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
# Utilisation de méthodes asynchrones Windows Runtime  

De nombreuses méthodes Windows Runtime, notamment les méthodes qui peuvent nécessiter un certain temps, sont asynchrones.  Ces méthodes renvoient généralement une action ou une opération asynchrone (par exemple,,, `Windows.Foundation.IAsyncAction` `Windows.Foundation.IAsyncOperation` `Windows.Foundation.IAsyncActionWithProgress` ou `Windows.Foundation.IAsyncOperationWithProgress` ).  Ces méthodes sont représentées dans JavaScript par le [modèle CommonJS/promet/A][CommonjsWikiPromises].  En d’autres cas, elle renvoie un objet promise qui dispose d’une [fonction Then][PreviousVersionsWindowsAppsBr229728]pour laquelle vous devez fournir une `completed` fonction qui gère le résultat si l’opération aboutit.  Si vous ne souhaitez pas fournir de gestionnaire d’erreur, vous devez utiliser la [fonction réalisé][PreviousVersionsWindowsAppsHr701079] au lieu de la `then` fonction.  

> [!IMPORTANT]
> Les fonctionnalités Windows Runtime ne sont pas disponibles pour les applications qui s’exécutent dans Internet Explorer.  

## Exemples de méthodes asynchrones  

Dans l’exemple suivant, la `then` fonction prend un paramètre qui représente la valeur achevée de la `createResourceAsync` méthode.  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
        console.log("New item is: " + newItem.id);
            });
```  

Dans ce cas, si la `createResourceAsync` méthode échoue, elle renvoie une promesse dans l’état d’erreur, mais ne lève pas d’exception.  Vous pouvez gérer une erreur à l’aide de la `then` fonction comme suit.  

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

Si vous ne souhaitez pas gérer l’erreur explicitement, mais que vous souhaitez qu’elle lève une exception, vous pouvez utiliser la fonction à la `done` place.  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .done(function(newItem) {
               console.log("New item is: " + newItem.id);
            });
```  

Vous pouvez également afficher l’avancement réalisé vers la fin à l’aide d’une troisième fonction.  

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

Pour plus d’informations sur la programmation asynchrone, voir [programmation asynchrone en JavaScript][PreviousVersionsWindowsAppsHh700330].  

## Voir aussi  

[Utilisation de Windows Runtime en JavaScript][WindowsRuntimeJavascript]  

<!-- image links -->  

<!-- links -->  

[WindowsRuntimeJavascript]: /microsoft-edge/windows-runtime/using-the-windows-runtime-in-javascript "Utilisation de Windows Runtime en JavaScript"  

[PreviousVersionsWindowsAppsBr229728]: /previous-versions/windows/apps/br229728(v=win.10) "Promesse. Then"  
[PreviousVersionsWindowsAppsHh700330]: /previous-versions/windows/apps/hh700330(v=win.10) "Programmation asynchrone en JavaScript (HTML)"
[PreviousVersionsWindowsAppsHr701079]: /previous-versions/windows/apps/hh701079(v=win.10) "Méthode promise. réalisé"  

[CommonjsWikiPromises]: http://wiki.commonjs.org/wiki/Promises "Promet | Wiki spec CommonJS"  
