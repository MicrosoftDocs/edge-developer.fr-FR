---
description: Utilisation de Windows Runtime en JavaScript
title: Utilisation de Windows Runtime en JavaScript
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime
ms.assetid: 90658546-f746-4e34-a7d1-71cf9ee322a2
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4e137526ce147cdeb82749474bd43d1b3697361b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399322"
---
# <a name="using-the-windows-runtime-in-javascript"></a>Utilisation de Windows Runtime en JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Lorsque vous écrivez une application de plateforme Windows universelle \(UWP\), vous pouvez utiliser les classes, méthodes et propriétés Windows Runtime de la même manière que vous utiliseriez les objets, méthodes et propriétés JavaScript natifs.  Cette rubrique fournit des informations d’introduction et des liens vers des rubriques qui expliquent les concepts de base de l’utilisation des API Windows Runtime en JavaScript, notamment une explication de la façon dont les types Windows Runtime sont représentés, comment utiliser des méthodes Windows Runtime asynchrones et comment écouter et gérer les événements Windows Runtime.  

Pour obtenir une documentation générale sur les langues, consultez la bibliothèque de référence [JavaScript de MDN.][MDNJavascriptReference]  

> [!IMPORTANT]
> Les fonctionnalités Windows Runtime ne sont pas disponibles pour les applications qui s’exécutent dans Internet Explorer.  

## <a name="windows-runtime-reference-documentation"></a>Documentation de référence sur Windows Runtime  

Pour obtenir une documentation de référence, voir [référence Windows Runtime.][UwpApiIndex]  Des exemples de code sont disponibles en JavaScript et également en C++, C# et Visual Basic.  

## <a name="writing-windows-runtime-components-in-c-c-or-visual-basic"></a>Écriture de composants Windows Runtime en C++, C# ou Visual Basic  

Pour obtenir des instructions et des instructions sur l’écriture de composants Windows Runtime qui peuvent être consommés en JavaScript, voir Création de [composants Windows Runtime en C++][WindowsUwpWinrtCpp] et création de [composants Windows Runtime][WindowsUwpWinrtCsharpVb]dans C# et Visual Basic .  

## <a name="casing-conventions-with-windows-runtime-features"></a>Conventions de cassation avec les fonctionnalités Windows Runtime  

Les conventions de casing pour les fonctionnalités Windows Runtime en JavaScript diffèrent légèrement de celles des autres langages :  

*   Les espaces de noms et les classes sont dans le cas DeNte :  
    
    ```javascript
    Windows.Deployment.PackageInfo;
    ```  
    
*   Les membres des classes, y compris les méthodes et les propriétés, ainsi que les membres de structures et d’éumérations, sont en cas de caméo :  
    
    ```javascript
    Deployment.PackageInfo.createPackage();
    ```  
    
*   Les noms d’événements sont dans les cas inférieurs :  
    
    ```javascript
    dataTransferManager.ontargetapplicationchosen;
    ```  
    
## <a name="see-also"></a>Voir également  

[Considérations relatives à l’utilisation de l’API Windows Runtime][WindowsRuntimeConsiderationsApi]  
[Utilisation des méthodes asynchrones Windows Runtime][WindowsRuntimeAsynchronousMethods]   
[Gestion des événements Windows Runtime dans JavaScript][WindowsRuntimeEventsJavascript]   
[Représentation JavaScript des types Windows Runtime][WindowsRuntimeJavascriptTypes]   
[Projection JavaScript de Windows Runtime DateTime et TimeSpan][WindowsRuntimeDatetimeTimespan]  

<!-- links -->  

[WindowsRuntimeConsiderationsApi]: ./considerations-when-using-the-windows-runtime-api.md "Considérations lors de l’utilisation de l’API Windows Runtime | Documents Microsoft"  
[WindowsRuntimeEventsJavascript]: ./handling-windows-runtime-events-in-javascript.md "Gestion des événements Windows Runtime dans javaScript | Documents Microsoft"  
[WindowsRuntimeJavascriptTypes]: ./javascript-representation-of-windows-runtime-types.md "Représentation JavaScript des types Windows Runtime | Documents Microsoft"  
[WindowsRuntimeAsynchronousMethods]: ./using-windows-runtime-asynchronous-methods.md "Utilisation des méthodes asynchrones Windows Runtime | Documents Microsoft"  
[WindowsRuntimeDatetimeTimespan]: ./windows-runtime-datetime-and-timespan-representations.md "Représentations DateTime et TimeSpan Windows Runtime | Documents Microsoft"  

[UwpApiIndex]: /uwp/api/index "Espaces de noms Windows UWP | Documents Microsoft"  
[WindowsUwpWinrtCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Composants Windows Runtime avec C++/CX | Documents Microsoft"  
[WindowsUwpWinrtCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Composants Windows Runtime avec C# et Visual Basic | Documents Microsoft"  

[MDNJavascriptReference]: https://developer.mozilla.org/docs/Web/JavaScript/Reference "Référence JavaScript | MDN"  
