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
# <span data-ttu-id="5b171-102">Utilisation de Windows Runtime en JavaScript</span><span class="sxs-lookup"><span data-stu-id="5b171-102">Using the Windows Runtime in JavaScript</span></span>  

<span data-ttu-id="5b171-103">Lorsque vous écrivez une application de plateforme Windows universelle (UWP), vous pouvez utiliser les classes, méthodes et propriétés Windows Runtime de la même manière que vous utilisez des objets, méthodes et propriétés JavaScript natifs.</span><span class="sxs-lookup"><span data-stu-id="5b171-103">When you write a Universal Windows Platform \(UWP\) app, you can use Windows Runtime classes, methods, and properties in much the same way that you would use native JavaScript objects, methods, and properties.</span></span>  <span data-ttu-id="5b171-104">Cette rubrique fournit des informations d’introduction et des liens vers des rubriques qui décrivent les concepts de base de l’utilisation des API Windows Runtime en JavaScript, y compris une explication de la façon dont les types Windows Runtime sont représentés, l’utilisation des méthodes Windows Runtime asynchrones et l’écoute et la gestion des événements Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="5b171-104">This topic provides introductory information and links to topics that explain the basic concepts of using Windows Runtime APIs in JavaScript, including an explanation of how Windows Runtime types are represented, how to use asynchronous Windows Runtime methods, and how to listen to and handle Windows Runtime events.</span></span>  

<span data-ttu-id="5b171-105">Pour obtenir une documentation de langue générale, voir la bibliothèque de [référence JavaScript][MDNJavascriptReference] de MDN.</span><span class="sxs-lookup"><span data-stu-id="5b171-105">For general language documentation, check out MDN's [JavaScript reference][MDNJavascriptReference] library.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="5b171-106">Les fonctionnalités Windows Runtime ne sont pas disponibles pour les applications qui s’exécutent dans Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="5b171-106">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <span data-ttu-id="5b171-107">Documentation de référence sur Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="5b171-107">Windows Runtime Reference Documentation</span></span>  

<span data-ttu-id="5b171-108">Pour obtenir une documentation de référence, voir informations de [référence sur Windows Runtime][UwpApiIndex].</span><span class="sxs-lookup"><span data-stu-id="5b171-108">For reference documentation, see [Windows Runtime Reference][UwpApiIndex].</span></span>  <span data-ttu-id="5b171-109">Des exemples de code sont disponibles en JavaScript et en C++, C# et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5b171-109">Code examples are available in JavaScript and also in C++, C#, and Visual Basic.</span></span>  

## <span data-ttu-id="5b171-110">Rédaction de composants Windows Runtime en C++, C# ou Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5b171-110">Writing Windows Runtime Components in C++, C#, or Visual Basic</span></span>  

<span data-ttu-id="5b171-111">Pour obtenir des instructions et des instructions pour écrire des composants Windows Runtime qui peuvent être utilisés dans JavaScript, voir [création de composants Windows Runtime en C++][WindowsUwpWinrtCpp] et [création de composants Windows Runtime en C# et Visual Basic][WindowsUwpWinrtCsharpVb].</span><span class="sxs-lookup"><span data-stu-id="5b171-111">For instructions and guidelines for writing Windows Runtime components that can be consumed in JavaScript, see [Creating Windows Runtime Components in C++][WindowsUwpWinrtCpp] and [Creating Windows Runtime Components in C# and Visual Basic][WindowsUwpWinrtCsharpVb].</span></span>  

## <span data-ttu-id="5b171-112">Conventions de casse avec les fonctionnalités Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="5b171-112">Casing Conventions with Windows Runtime Features</span></span>  

<span data-ttu-id="5b171-113">Les conventions de casse des fonctionnalités Windows Runtime en JavaScript diffèrent légèrement de celles des autres langages:</span><span class="sxs-lookup"><span data-stu-id="5b171-113">Casing conventions for Windows Runtime features in JavaScript differ slightly from those for other languages:</span></span>  

*   <span data-ttu-id="5b171-114">Les espaces de noms et les classes sont en majuscules pascales:</span><span class="sxs-lookup"><span data-stu-id="5b171-114">Namespaces and classes are in Pascal case:</span></span>  
    
    ```javascript
    Windows.Deployment.PackageInfo;
    ```  
    
*   <span data-ttu-id="5b171-115">Les membres des classes, y compris les méthodes et les propriétés, ainsi que les membres des structures et énumérations, sont en casse mixte:</span><span class="sxs-lookup"><span data-stu-id="5b171-115">Members of classes, including methods and properties, and members of structures and enumerations, are in camel case:</span></span>  
    
    ```javascript
    Deployment.PackageInfo.createPackage();
    ```  
    
*   <span data-ttu-id="5b171-116">Les noms d’événements sont en minuscules:</span><span class="sxs-lookup"><span data-stu-id="5b171-116">Event names are in lower case:</span></span>  
    
    ```javascript
    dataTransferManager.ontargetapplicationchosen;
    ```  

## <span data-ttu-id="5b171-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b171-117">See Also</span></span>  

[<span data-ttu-id="5b171-118">Éléments à prendre en compte lors de l’utilisation de l’API Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="5b171-118">Considerations when Using the Windows Runtime API</span></span>][WindowsRuntimeConsiderationsApi]  
[<span data-ttu-id="5b171-119">Utilisation de méthodes asynchrones Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="5b171-119">Using Windows Runtime Asynchronous Methods</span></span>][WindowsRuntimeAsynchronousMethods]   
[<span data-ttu-id="5b171-120">Gestion des événements Windows Runtime en JavaScript</span><span class="sxs-lookup"><span data-stu-id="5b171-120">Handling Windows Runtime Events in JavaScript</span></span>][WindowsRuntimeEventsJavascript]   
[<span data-ttu-id="5b171-121">Représentation JavaScript des types Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="5b171-121">JavaScript Representation of Windows Runtime Types</span></span>][WindowsRuntimeJavascriptTypes]   
[<span data-ttu-id="5b171-122">Projection JavaScript de DateTime et TimeSpan Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="5b171-122">JavaScript Projection of Windows Runtime DateTime and TimeSpan</span></span>][WindowsRuntimeDatetimeTimespan]  
 
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
