---
title: Utilisation de Windows Runtime en JavaScript
ms.custom: ''
ms.date: 04/01/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime
ms.assetid: 90658546-f746-4e34-a7d1-71cf9ee322a2
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: bffde93aa973f492189aedcfcaa9c3694d9e61bc
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566645"
---
# Utilisation de Windows Runtime en JavaScript  

Lorsque vous écrivez une application de plateforme Windows universelle (UWP), vous pouvez utiliser les classes, méthodes et propriétés Windows Runtime de la même manière que vous utilisez des objets, méthodes et propriétés JavaScript natifs.  Cette rubrique fournit des informations d’introduction et des liens vers des rubriques qui décrivent les concepts de base de l’utilisation des API Windows Runtime en JavaScript, y compris une explication de la façon dont les types Windows Runtime sont représentés, l’utilisation des méthodes Windows Runtime asynchrones et l’écoute et la gestion des événements Windows Runtime.  

Pour obtenir une documentation de langue générale, voir la bibliothèque de [référence JavaScript][MDNJavascriptReference] de MDN.  

> [!IMPORTANT]
> Les fonctionnalités Windows Runtime ne sont pas disponibles pour les applications qui s’exécutent dans Internet Explorer.  

## Documentation de référence sur Windows Runtime  

Pour obtenir une documentation de référence, voir informations de [référence sur Windows Runtime][UwpApiIndex].  Des exemples de code sont disponibles en JavaScript et en C++, C# et Visual Basic.  

## Rédaction de composants Windows Runtime en C++, C# ou Visual Basic  

Pour obtenir des instructions et des instructions pour écrire des composants Windows Runtime qui peuvent être utilisés dans JavaScript, voir [création de composants Windows Runtime en C++][WindowsUwpWinrtCpp] et [création de composants Windows Runtime en C# et Visual Basic][WindowsUwpWinrtCsharpVb].  

## Conventions de casse avec les fonctionnalités Windows Runtime  

Les conventions de casse des fonctionnalités Windows Runtime en JavaScript diffèrent légèrement de celles des autres langages:  

*   Les espaces de noms et les classes sont en majuscules pascales:  
    
    ```javascript
    Windows.Deployment.PackageInfo;
    ```  
    
*   Les membres des classes, y compris les méthodes et les propriétés, ainsi que les membres des structures et énumérations, sont en casse mixte:  
    
    ```javascript
    Deployment.PackageInfo.createPackage();
    ```  
    
*   Les noms d’événements sont en minuscules:  
    
    ```javascript
    dataTransferManager.ontargetapplicationchosen;
    ```  

## Voir aussi  

[Éléments à prendre en compte lors de l’utilisation de l’API Windows Runtime][WindowsRuntimeConsiderationsApi]  
[Utilisation de méthodes asynchrones Windows Runtime][WindowsRuntimeAsynchronousMethods]   
[Gestion des événements Windows Runtime en JavaScript][WindowsRuntimeEventsJavascript]   
[Représentation JavaScript des types Windows Runtime][WindowsRuntimeJavascriptTypes]   
[Projection JavaScript de DateTime et TimeSpan Windows Runtime][WindowsRuntimeDatetimeTimespan]  
 
<!-- image links -->  

<!-- links  -->  

[WindowsRuntimeConsiderationsApi]: /microsoft-edge/windows-runtime/considerations-when-using-the-windows-runtime-api "Éléments à prendre en compte lors de l’utilisation de l’API Windows Runtime"  
[WindowsRuntimeEventsJavascript]: /microsoft-edge/windows-runtime/handling-windows-runtime-events-in-javascript "Gestion des événements Windows Runtime en JavaScript"  
[WindowsRuntimeJavascriptTypes]: /microsoft-edge/windows-runtime/javascript-representation-of-windows-runtime-types "Représentation JavaScript des types Windows Runtime"  
[WindowsRuntimeAsynchronousMethods]: /microsoft-edge/windows-runtime/using-windows-runtime-asynchronous-methods "Utilisation de méthodes asynchrones Windows Runtime"  
[WindowsRuntimeDatetimeTimespan]: /microsoft-edge/windows-runtime/windows-runtime-datetime-and-timespan-representations "Représentations DateTime et TimeSpan Windows Runtime"  

[UwpApiIndex]: /uwp/api/index "Espaces de noms UWP Windows"  
[WindowsUwpWinrtCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Composants Windows Runtime avec C++/CX"  
[WindowsUwpWinrtCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Composants Windows Runtime avec C# et Visual Basic"  

[MDNJavascriptReference]: https://developer.mozilla.org/docs/Web/JavaScript/Reference "Référence JavaScript | MDN"  
