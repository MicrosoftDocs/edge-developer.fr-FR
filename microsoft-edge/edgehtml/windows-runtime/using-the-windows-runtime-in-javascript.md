---
description: Utilisation de Windows Runtime en JavaScript.
title: Utilisation de Windows Runtime en JavaScript
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime
ms.assetid: 90658546-f746-4e34-a7d1-71cf9ee322a2
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 10c90a225816cf32e01bc33648571c13a1aae090
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233090"
---
# <span data-ttu-id="b1418-103">Utilisation de Windows Runtime en JavaScript</span><span class="sxs-lookup"><span data-stu-id="b1418-103">Using the Windows Runtime in JavaScript</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="b1418-104">Lorsque vous écrivez une application de plateforme Windows universelle (UWP), vous pouvez utiliser les classes, méthodes et propriétés Windows Runtime de la même manière que vous utilisez des objets, méthodes et propriétés JavaScript natifs.</span><span class="sxs-lookup"><span data-stu-id="b1418-104">When you write a Universal Windows Platform \(UWP\) app, you can use Windows Runtime classes, methods, and properties in much the same way that you would use native JavaScript objects, methods, and properties.</span></span>  <span data-ttu-id="b1418-105">Cette rubrique fournit des informations d’introduction et des liens vers des rubriques qui décrivent les concepts de base de l’utilisation des API Windows Runtime en JavaScript, y compris une explication de la façon dont les types Windows Runtime sont représentés, l’utilisation des méthodes Windows Runtime asynchrones et l’écoute et la gestion des événements Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="b1418-105">This topic provides introductory information and links to topics that explain the basic concepts of using Windows Runtime APIs in JavaScript, including an explanation of how Windows Runtime types are represented, how to use asynchronous Windows Runtime methods, and how to listen to and handle Windows Runtime events.</span></span>  

<span data-ttu-id="b1418-106">Pour obtenir une documentation de langue générale, voir la bibliothèque de [référence JavaScript][MDNJavascriptReference] de MDN.</span><span class="sxs-lookup"><span data-stu-id="b1418-106">For general language documentation, check out MDN's [JavaScript reference][MDNJavascriptReference] library.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="b1418-107">Les fonctionnalités Windows Runtime ne sont pas disponibles pour les applications qui s’exécutent dans Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="b1418-107">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <span data-ttu-id="b1418-108">Documentation de référence sur Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="b1418-108">Windows Runtime reference documentation</span></span>  

<span data-ttu-id="b1418-109">Pour obtenir une documentation de référence, voir informations de [référence sur Windows Runtime][UwpApiIndex].</span><span class="sxs-lookup"><span data-stu-id="b1418-109">For reference documentation, see [Windows Runtime Reference][UwpApiIndex].</span></span>  <span data-ttu-id="b1418-110">Des exemples de code sont disponibles en JavaScript et en C++, C# et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b1418-110">Code examples are available in JavaScript and also in C++, C#, and Visual Basic.</span></span>  

## <span data-ttu-id="b1418-111">Rédaction de composants Windows Runtime en C++, C# ou Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b1418-111">Writing Windows Runtime components in C++, C#, or Visual Basic</span></span>  

<span data-ttu-id="b1418-112">Pour obtenir des instructions et des instructions pour écrire des composants Windows Runtime qui peuvent être utilisés dans JavaScript, voir [création de composants Windows Runtime en C++][WindowsUwpWinrtCpp] et [création de composants Windows Runtime en C# et Visual Basic][WindowsUwpWinrtCsharpVb].</span><span class="sxs-lookup"><span data-stu-id="b1418-112">For instructions and guidelines for writing Windows Runtime components that can be consumed in JavaScript, see [Creating Windows Runtime Components in C++][WindowsUwpWinrtCpp] and [Creating Windows Runtime Components in C# and Visual Basic][WindowsUwpWinrtCsharpVb].</span></span>  

## <span data-ttu-id="b1418-113">Conventions de casse avec les fonctionnalités Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="b1418-113">Casing conventions with Windows Runtime features</span></span>  

<span data-ttu-id="b1418-114">Les conventions de casse des fonctionnalités Windows Runtime en JavaScript diffèrent légèrement de celles des autres langages:</span><span class="sxs-lookup"><span data-stu-id="b1418-114">Casing conventions for Windows Runtime features in JavaScript differ slightly from those for other languages:</span></span>  

*   <span data-ttu-id="b1418-115">Les espaces de noms et les classes sont en majuscules pascales:</span><span class="sxs-lookup"><span data-stu-id="b1418-115">Namespaces and classes are in Pascal case:</span></span>  
    
    ```javascript
    Windows.Deployment.PackageInfo;
    ```  
    
*   <span data-ttu-id="b1418-116">Les membres des classes, y compris les méthodes et les propriétés, ainsi que les membres des structures et énumérations, sont en casse mixte:</span><span class="sxs-lookup"><span data-stu-id="b1418-116">Members of classes, including methods and properties, and members of structures and enumerations, are in camel case:</span></span>  
    
    ```javascript
    Deployment.PackageInfo.createPackage();
    ```  
    
*   <span data-ttu-id="b1418-117">Les noms d’événements sont en minuscules:</span><span class="sxs-lookup"><span data-stu-id="b1418-117">Event names are in lower case:</span></span>  
    
    ```javascript
    dataTransferManager.ontargetapplicationchosen;
    ```  

## <span data-ttu-id="b1418-118">Voir également</span><span class="sxs-lookup"><span data-stu-id="b1418-118">See also</span></span>  

[<span data-ttu-id="b1418-119">Considérations relatives à l’utilisation de l’API Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="b1418-119">Considerations when Using the Windows Runtime API</span></span>][WindowsRuntimeConsiderationsApi]  
[<span data-ttu-id="b1418-120">Utilisation des méthodes asynchrones Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="b1418-120">Using Windows Runtime Asynchronous Methods</span></span>][WindowsRuntimeAsynchronousMethods]   
[<span data-ttu-id="b1418-121">Gestion des événements Windows Runtime dans JavaScript</span><span class="sxs-lookup"><span data-stu-id="b1418-121">Handling Windows Runtime Events in JavaScript</span></span>][WindowsRuntimeEventsJavascript]   
[<span data-ttu-id="b1418-122">Représentation JavaScript des types Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="b1418-122">JavaScript Representation of Windows Runtime Types</span></span>][WindowsRuntimeJavascriptTypes]   
[<span data-ttu-id="b1418-123">Projection JavaScript de DateTime et TimeSpan Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="b1418-123">JavaScript Projection of Windows Runtime DateTime and TimeSpan</span></span>][WindowsRuntimeDatetimeTimespan]  

<!-- links  -->  

[WindowsRuntimeConsiderationsApi]: ./considerations-when-using-the-windows-runtime-api.md "Éléments à prendre en compte lors de l’utilisation de l’API Windows Runtime | Documents Microsoft"  
[WindowsRuntimeEventsJavascript]: ./handling-windows-runtime-events-in-javascript.md "Gestion des événements Windows Runtime en JavaScript | Documents Microsoft"  
[WindowsRuntimeJavascriptTypes]: ./javascript-representation-of-windows-runtime-types.md "Représentation JavaScript des types Windows Runtime | Documents Microsoft"  
[WindowsRuntimeAsynchronousMethods]: ./using-windows-runtime-asynchronous-methods.md "Utilisation de méthodes asynchrones Windows Runtime | Documents Microsoft"  
[WindowsRuntimeDatetimeTimespan]: ./windows-runtime-datetime-and-timespan-representations.md "Représentations DateTime et TimeSpan Windows Runtime | Documents Microsoft"  

[UwpApiIndex]: /uwp/api/index "Espaces de noms UWP Windows | Documents Microsoft"  
[WindowsUwpWinrtCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Composants Windows Runtime avec C++/CX | Documents Microsoft"  
[WindowsUwpWinrtCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Composants Windows Runtime avec C# et Visual Basic | Documents Microsoft"  

[MDNJavascriptReference]: https://developer.mozilla.org/docs/Web/JavaScript/Reference "Référence JavaScript | MDN"  
