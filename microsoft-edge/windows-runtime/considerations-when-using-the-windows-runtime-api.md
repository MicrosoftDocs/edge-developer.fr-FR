---
title: Éléments à prendre en compte lors de l’utilisation de l’API Windows Runtime
ms.custom: ''
ms.date: 04/01/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime API
ms.assetid: 2f56d70c-c80d-4876-8e6a-8ae031d31c22
caps.latest.revision: 8
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 95b082e27c4f247b841a9540e13bd49bd4c8bd67
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566660"
---
# <span data-ttu-id="568bb-102">Éléments à prendre en compte lors de l’utilisation de l’API Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="568bb-102">Considerations when Using the Windows Runtime API</span></span>  

<span data-ttu-id="568bb-103">Vous pouvez utiliser presque tous les éléments de l’API Windows Runtime en JavaScript.</span><span class="sxs-lookup"><span data-stu-id="568bb-103">You can use nearly every element of the Windows Runtime API in JavaScript.</span></span>  <span data-ttu-id="568bb-104">Néanmoins, il existe certains aspects de la représentation JavaScript des éléments Windows Runtime que vous devez garder à l’esprit.</span><span class="sxs-lookup"><span data-stu-id="568bb-104">However, there are some aspects of the JavaScript representation of Windows Runtime elements that you should keep in mind.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="568bb-105">Pour plus d’informations sur la création de composants Windows Runtime en C++, C# ou Visual Basic et pour les consommer en JavaScript, voir [création de composants Windows Runtime en c++][WindowsUwpComponentsCreatingCpp] et [création de composants Windows Runtime en C# et Visual Basic][WindowsUwpComponentsCreatingCsharpVb].</span><span class="sxs-lookup"><span data-stu-id="568bb-105">For information about creating Windows Runtime components in C++, C#, or Visual Basic and consuming them in JavaScript, see [Creating Windows Runtime Components in C++][WindowsUwpComponentsCreatingCpp] and [Creating Windows Runtime Components in C# and Visual Basic][WindowsUwpComponentsCreatingCsharpVb].</span></span>  

## <span data-ttu-id="568bb-106">Cas particuliers dans la représentation JavaScript des types Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="568bb-106">Special Cases in the JavaScript Representation of Windows Runtime Types</span></span>  

*   <span data-ttu-id="568bb-107">Chaînes: une chaîne non initialisée est transmise à une méthode Windows Runtime en tant que chaîne «non définie» et une chaîne définie sur `null` est transmise en tant que chaîne «NULL».</span><span class="sxs-lookup"><span data-stu-id="568bb-107">Strings: An uninitialized string is passed to a Windows Runtime method as the string "undefined", and a string set to `null` is passed as the string "null".</span></span>  <span data-ttu-id="568bb-108">\ (C’est vrai chaque fois qu’une `null` `undefined` valeur ou est forcée en une chaîne. \) avant de transmettre une chaîne à une méthode Windows Runtime, vous devez l’initialiser comme chaîne vide \ ("" \).</span><span class="sxs-lookup"><span data-stu-id="568bb-108">\(This is true whenever a `null` or `undefined` value is coerced to a string.\)  Before you pass a string to a Windows Runtime method, you should initialize it as the empty string \(""\).</span></span>  
*   <span data-ttu-id="568bb-109">Interfaces: il est impossible d’implémenter une interface Windows Runtime en JavaScript.</span><span class="sxs-lookup"><span data-stu-id="568bb-109">Interfaces: You cannot implement a Windows Runtime interface in JavaScript.</span></span>  
*   <span data-ttu-id="568bb-110">Tableaux: les tableaux Windows Runtime ne sont pas redimensionnables, de sorte que les méthodes permettant de redimensionner des tableaux en JavaScript ne fonctionnent pas sur les tableaux Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="568bb-110">Arrays: Windows Runtime arrays are not resizable, so methods that resize arrays in JavaScript do not work on Windows Runtime arrays.</span></span>  
*   <span data-ttu-id="568bb-111">Tableaux: Si vous passez une valeur de tableau JavaScript à une méthode Windows Runtime, le tableau est copié.</span><span class="sxs-lookup"><span data-stu-id="568bb-111">Arrays: If you pass a JavaScript array value to a Windows Runtime method, the array is copied.</span></span>  <span data-ttu-id="568bb-112">La méthode Windows Runtime n’est pas en mesure de modifier le tableau ou ses membres, et de les retourner dans votre application JavaScript.</span><span class="sxs-lookup"><span data-stu-id="568bb-112">The Windows Runtime method is not able to modify the array or its members and return it to your JavaScript app.</span></span>  <span data-ttu-id="568bb-113">Toutefois, vous pouvez utiliser des tableaux typés (par exemple, l' [objet Int32Array][MDNInt32array]\) qui ne sont pas copiés.</span><span class="sxs-lookup"><span data-stu-id="568bb-113">However, you can use typed arrays \(for example, [Int32Array Object][MDNInt32array]\), which are not copied.</span></span>  
*   <span data-ttu-id="568bb-114">Structures: les structures Windows Runtime sont des objets en JavaScript.</span><span class="sxs-lookup"><span data-stu-id="568bb-114">Structures: Windows Runtime structures are objects in JavaScript.</span></span>  <span data-ttu-id="568bb-115">Si vous souhaitez transmettre une structure Windows Runtime à une méthode Windows Runtime, n’instanciez pas la structure avec le `new` mot-clé.</span><span class="sxs-lookup"><span data-stu-id="568bb-115">If you want to pass a Windows Runtime structure to a Windows Runtime method, don't instantiate the structure with the `new` keyword.</span></span>  <span data-ttu-id="568bb-116">Créez plutôt un objet, puis ajoutez les membres pertinents et leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="568bb-116">Instead, create an object and add the relevant members and their values.</span></span>  <span data-ttu-id="568bb-117">Les noms des membres doivent être en majuscules mixtes: `SomeStruct.firstMember` .</span><span class="sxs-lookup"><span data-stu-id="568bb-117">The names of the members should be in camel case: `SomeStruct.firstMember`.</span></span>  
*   <span data-ttu-id="568bb-118">Objets: les objets JavaScript ne sont pas identiques aux objets de code managé \ ( `System.Object` \).</span><span class="sxs-lookup"><span data-stu-id="568bb-118">Objects: JavaScript objects aren't the same as managed code objects \(`System.Object`\).</span></span>  <span data-ttu-id="568bb-119">Vous ne pouvez pas transmettre un objet JavaScript à une méthode Windows Runtime qui nécessite a `System.Object` .</span><span class="sxs-lookup"><span data-stu-id="568bb-119">You can't pass a JavaScript object to a Windows Runtime method that requires a `System.Object`.</span></span>  
*   <span data-ttu-id="568bb-120">Identité de l’objet: dans la plupart des cas, les objets transmis entre Windows Runtime et JavaScript ne changent pas.</span><span class="sxs-lookup"><span data-stu-id="568bb-120">Object identity: In most cases, the objects passed back and forth between the Windows Runtime and JavaScript do not change.</span></span>  <span data-ttu-id="568bb-121">Le moteur JavaScript maintient une carte d’objets connus.</span><span class="sxs-lookup"><span data-stu-id="568bb-121">The JavaScript engine maintains a map of known objects.</span></span>  <span data-ttu-id="568bb-122">Lorsqu’un objet est retourné à partir du Windows Runtime, il est mis en correspondance avec la carte et, s’il n’existe pas, un nouvel objet est créé.</span><span class="sxs-lookup"><span data-stu-id="568bb-122">When an object is returned from the Windows Runtime it is matched against the map, and if it does not exist a new object is created.</span></span>  <span data-ttu-id="568bb-123">La même procédure est suivie pour les objets qui représentent des interfaces qui sont renvoyées par des méthodes Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="568bb-123">The same procedure is followed for objects that represent interfaces that are returned by Windows Runtime methods.</span></span>  <span data-ttu-id="568bb-124">Il existe deux types d’exceptions:</span><span class="sxs-lookup"><span data-stu-id="568bb-124">There are two kinds of exceptions:</span></span>  

    *   <span data-ttu-id="568bb-125">Les objets renvoyés par un appel Windows Runtime, puis dotés de nouvelles propriétés \ (expando \) ajoutés, ne conservent pas leurs nouvelles propriétés lorsqu’elles sont transmises au Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="568bb-125">Objects that are returned from a Windows Runtime call, and then have new \(expando\) properties added, don't retain their new properties when they are passed back to the Windows Runtime.</span></span>  <span data-ttu-id="568bb-126">Néanmoins, lorsque ces objets sont retournés à l’application JavaScript, car ils sont associés à l’objet existant, l’objet renvoyé possède les propriétés expando.</span><span class="sxs-lookup"><span data-stu-id="568bb-126">However, when they are returned to the JavaScript app, because they're matched to the existing object, the returned object does have the expando properties.</span></span>  
    *   <span data-ttu-id="568bb-127">Dans Windows Runtime, les structures et délégués ne peuvent pas être identifiés comme identiques aux structures ou délégués déjà utilisés.</span><span class="sxs-lookup"><span data-stu-id="568bb-127">Structures and delegates in Windows Runtime can't be identified as identical to previously-used structures or delegates.</span></span>  <span data-ttu-id="568bb-128">Chaque fois qu’une structure ou un délégué est retourné, elle obtient une nouvelle référence.</span><span class="sxs-lookup"><span data-stu-id="568bb-128">Every time a structure or delegate is returned, it gets a new reference.</span></span>  

*   <span data-ttu-id="568bb-129">Conflits de nom: plusieurs interfaces Windows Runtime peuvent avoir des membres du même nom.</span><span class="sxs-lookup"><span data-stu-id="568bb-129">Name collisions: Multiple Windows Runtime interfaces may have members with the same names.</span></span>  <span data-ttu-id="568bb-130">S’ils sont combinés dans un seul objet JavaScript (qui peut être une représentation d’une classe Runtime ou d’une interface), les membres sont représentés par des noms complets.</span><span class="sxs-lookup"><span data-stu-id="568bb-130">If they are combined in a single JavaScript object (which can be a representation of a runtime class or an interface), the members are represented with fully-qualified names.</span></span>  <span data-ttu-id="568bb-131">Vous pouvez appeler ces membres en utilisant la syntaxe suivante:</span><span class="sxs-lookup"><span data-stu-id="568bb-131">You can call these members by using the following syntax:</span></span>  
    
    ```cpp
    Class["MemberName"](parameter)
    ```  
    
    <span data-ttu-id="568bb-132">Dans le code suivant, deux interfaces disposent d’une méthode Draw, et une classe Runtime implémente les deux interfaces.</span><span class="sxs-lookup"><span data-stu-id="568bb-132">In the following code, two interfaces have a Draw method, and a runtime class implements both interfaces.</span></span>  
    
    ```cpp
    namespace CollisionExample {
        interface InterfaceA
        {
            HRESULT Draw([in] Int32 a);
        }
        interface InterfaceB
        {
            HRESULT Draw([in] HString a);
        }
        runtimeclass ExampleObject {
          interface InterfaceA
          interface InterfaceB
        }
    }
    ```  
    
    <span data-ttu-id="568bb-133">Voici comment vous pouvez appeler le code ci-dessus en JavaScript.</span><span class="sxs-lookup"><span data-stu-id="568bb-133">Here is how you can call the above code in JavaScript.</span></span>  
    
    ```javascript
    var example = new ExampleObject();
    example["CollisionExample.InterfaceA.draw"](12);
    example["CollisionExample.InterfaceB.draw"]("hello");
    ```  
    
*   `Out` <span data-ttu-id="568bb-134">paramètres: si une méthode Windows Runtime comporte plusieurs `out` paramètres, en JavaScript, la méthode possède un objet JavaScript comme valeur de retour et l’objet possède des propriétés qui correspondent au `out` paramètre.</span><span class="sxs-lookup"><span data-stu-id="568bb-134">parameters: If a Windows Runtime method has multiple `out` parameters, in JavaScript the method has a JavaScript object as its return value, and the object has properties that correspond to the `out` parameter.</span></span>  <span data-ttu-id="568bb-135">Par exemple, considérez la signature Windows Runtime suivante en C++.</span><span class="sxs-lookup"><span data-stu-id="568bb-135">For example, consider the following Windows Runtime signature in C++.</span></span>  
    
    ```cpp
    void ExampleMethod(
      [OutAttribute] char^ first,
      [OutAttribute] char^ second
    )
    ```  
    
    <span data-ttu-id="568bb-136">La version JavaScript de cette signature est la suivante:</span><span class="sxs-lookup"><span data-stu-id="568bb-136">The JavaScript version of this signature is:</span></span>  
    
    ```javascript
    var returnValue = exampleMethod();
    ```  
    
    <span data-ttu-id="568bb-137">Dans cet exemple, `returnValue` est un objet JavaScript qui comporte deux champs: `first` et `second` .</span><span class="sxs-lookup"><span data-stu-id="568bb-137">In this example, `returnValue` is a JavaScript object that has two fields: `first` and `second`.</span></span>  
    
*   <span data-ttu-id="568bb-138">Membres statiques: Windows Runtime définit à la fois les membres statiques et les membres d’instance.</span><span class="sxs-lookup"><span data-stu-id="568bb-138">Static members: The Windows Runtime defines both static members and instance members.</span></span>  <span data-ttu-id="568bb-139">Dans JavaScript, les membres statiques sont ajoutés à l’objet associé à la classe ou à l’interface Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="568bb-139">In JavaScript, static members are added to the object that is associated with the Windows Runtime class or interface.</span></span>  
    
    ```javascript
    // Static method.
    var accel = Windows.Devices.Sensors.Accelerometer.getDefault();
    // Instance method.
    var reading = accel.getCurrentReading();
    ```  
    
<span data-ttu-id="568bb-140">Pour plus d’informations sur la représentation JavaScript des types Windows Runtime basique, voir [représentation JavaScript des types Windows Runtime][WindowsRuntimeJavascriptTypes].</span><span class="sxs-lookup"><span data-stu-id="568bb-140">For more information about the JavaScript representation of Windows Runtime basic types, see [JavaScript Representation of Windows Runtime Types][WindowsRuntimeJavascriptTypes].</span></span>  

<!-- image links -->  

<!-- links -->  
 
[WindowsRuntimeJavascriptTypes]: /microsoft-edge/windows-runtime/javascript-representation-of-windows-runtime-types "Représentation JavaScript des types Windows Runtime"

[WindowsUwpComponentsCreatingCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Composants Windows Runtime avec C++/CX"  
[WindowsUwpComponentsCreatingCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Composants Windows Runtime avec C# et Visual Basic"  

[MDNInt32array]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Int32Array "Int32Array | MDN"  