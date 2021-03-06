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
# <a name="using-the-windows-runtime-in-javascript"></a><span data-ttu-id="59164-103">Utilisation de Windows Runtime en JavaScript</span><span class="sxs-lookup"><span data-stu-id="59164-103">Using the Windows Runtime in JavaScript</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="59164-104">Lorsque vous écrivez une application de plateforme Windows universelle \(UWP\), vous pouvez utiliser les classes, méthodes et propriétés Windows Runtime de la même manière que vous utiliseriez les objets, méthodes et propriétés JavaScript natifs.</span><span class="sxs-lookup"><span data-stu-id="59164-104">When you write a Universal Windows Platform \(UWP\) app, you can use Windows Runtime classes, methods, and properties in much the same way that you would use native JavaScript objects, methods, and properties.</span></span>  <span data-ttu-id="59164-105">Cette rubrique fournit des informations d’introduction et des liens vers des rubriques qui expliquent les concepts de base de l’utilisation des API Windows Runtime en JavaScript, notamment une explication de la façon dont les types Windows Runtime sont représentés, comment utiliser des méthodes Windows Runtime asynchrones et comment écouter et gérer les événements Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="59164-105">This topic provides introductory information and links to topics that explain the basic concepts of using Windows Runtime APIs in JavaScript, including an explanation of how Windows Runtime types are represented, how to use asynchronous Windows Runtime methods, and how to listen to and handle Windows Runtime events.</span></span>  

<span data-ttu-id="59164-106">Pour obtenir une documentation générale sur les langues, consultez la bibliothèque de référence [JavaScript de MDN.][MDNJavascriptReference]</span><span class="sxs-lookup"><span data-stu-id="59164-106">For general language documentation, check out MDN's [JavaScript reference][MDNJavascriptReference] library.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="59164-107">Les fonctionnalités Windows Runtime ne sont pas disponibles pour les applications qui s’exécutent dans Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="59164-107">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <a name="windows-runtime-reference-documentation"></a><span data-ttu-id="59164-108">Documentation de référence sur Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="59164-108">Windows Runtime reference documentation</span></span>  

<span data-ttu-id="59164-109">Pour obtenir une documentation de référence, voir [référence Windows Runtime.][UwpApiIndex]</span><span class="sxs-lookup"><span data-stu-id="59164-109">For reference documentation, see [Windows Runtime Reference][UwpApiIndex].</span></span>  <span data-ttu-id="59164-110">Des exemples de code sont disponibles en JavaScript et également en C++, C# et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="59164-110">Code examples are available in JavaScript and also in C++, C#, and Visual Basic.</span></span>  

## <a name="writing-windows-runtime-components-in-c-c-or-visual-basic"></a><span data-ttu-id="59164-111">Écriture de composants Windows Runtime en C++, C# ou Visual Basic</span><span class="sxs-lookup"><span data-stu-id="59164-111">Writing Windows Runtime components in C++, C#, or Visual Basic</span></span>  

<span data-ttu-id="59164-112">Pour obtenir des instructions et des instructions sur l’écriture de composants Windows Runtime qui peuvent être consommés en JavaScript, voir Création de [composants Windows Runtime en C++][WindowsUwpWinrtCpp] et création de [composants Windows Runtime][WindowsUwpWinrtCsharpVb]dans C# et Visual Basic .</span><span class="sxs-lookup"><span data-stu-id="59164-112">For instructions and guidelines for writing Windows Runtime components that can be consumed in JavaScript, see [Creating Windows Runtime Components in C++][WindowsUwpWinrtCpp] and [Creating Windows Runtime Components in C# and Visual Basic][WindowsUwpWinrtCsharpVb].</span></span>  

## <a name="casing-conventions-with-windows-runtime-features"></a><span data-ttu-id="59164-113">Conventions de cassation avec les fonctionnalités Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="59164-113">Casing conventions with Windows Runtime features</span></span>  

<span data-ttu-id="59164-114">Les conventions de casing pour les fonctionnalités Windows Runtime en JavaScript diffèrent légèrement de celles des autres langages :</span><span class="sxs-lookup"><span data-stu-id="59164-114">Casing conventions for Windows Runtime features in JavaScript differ slightly from those for other languages:</span></span>  

*   <span data-ttu-id="59164-115">Les espaces de noms et les classes sont dans le cas DeNte :</span><span class="sxs-lookup"><span data-stu-id="59164-115">Namespaces and classes are in Pascal case:</span></span>  
    
    ```javascript
    Windows.Deployment.PackageInfo;
    ```  
    
*   <span data-ttu-id="59164-116">Les membres des classes, y compris les méthodes et les propriétés, ainsi que les membres de structures et d’éumérations, sont en cas de caméo :</span><span class="sxs-lookup"><span data-stu-id="59164-116">Members of classes, including methods and properties, and members of structures and enumerations, are in camel case:</span></span>  
    
    ```javascript
    Deployment.PackageInfo.createPackage();
    ```  
    
*   <span data-ttu-id="59164-117">Les noms d’événements sont dans les cas inférieurs :</span><span class="sxs-lookup"><span data-stu-id="59164-117">Event names are in lower case:</span></span>  
    
    ```javascript
    dataTransferManager.ontargetapplicationchosen;
    ```  
    
## <a name="see-also"></a><span data-ttu-id="59164-118">Voir également</span><span class="sxs-lookup"><span data-stu-id="59164-118">See also</span></span>  

[<span data-ttu-id="59164-119">Considérations relatives à l’utilisation de l’API Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="59164-119">Considerations when Using the Windows Runtime API</span></span>][WindowsRuntimeConsiderationsApi]  
[<span data-ttu-id="59164-120">Utilisation des méthodes asynchrones Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="59164-120">Using Windows Runtime Asynchronous Methods</span></span>][WindowsRuntimeAsynchronousMethods]   
[<span data-ttu-id="59164-121">Gestion des événements Windows Runtime dans JavaScript</span><span class="sxs-lookup"><span data-stu-id="59164-121">Handling Windows Runtime Events in JavaScript</span></span>][WindowsRuntimeEventsJavascript]   
[<span data-ttu-id="59164-122">Représentation JavaScript des types Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="59164-122">JavaScript Representation of Windows Runtime Types</span></span>][WindowsRuntimeJavascriptTypes]   
[<span data-ttu-id="59164-123">Projection JavaScript de Windows Runtime DateTime et TimeSpan</span><span class="sxs-lookup"><span data-stu-id="59164-123">JavaScript Projection of Windows Runtime DateTime and TimeSpan</span></span>][WindowsRuntimeDatetimeTimespan]  

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
