---
description: Éléments à prendre en compte lors de l’utilisation de l’API Windows Runtime.
title: Considérations relatives à l’utilisation de l’API Windows Runtime
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime API
ms.assetid: 2f56d70c-c80d-4876-8e6a-8ae031d31c22
caps.latest.revision: 8
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 718a23646ec9a82c1d53a2669d7cdbf218647e41
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233154"
---
# <span data-ttu-id="60a9c-103">Considérations relatives à l’utilisation de l’API Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="60a9c-103">Considerations when using the Windows Runtime API</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="60a9c-104">Vous pouvez utiliser presque tous les éléments de l’API Windows Runtime en JavaScript.</span><span class="sxs-lookup"><span data-stu-id="60a9c-104">You can use nearly every element of the Windows Runtime API in JavaScript.</span></span>  <span data-ttu-id="60a9c-105">Néanmoins, il existe certains aspects de la représentation JavaScript des éléments Windows Runtime que vous devez garder à l’esprit.</span><span class="sxs-lookup"><span data-stu-id="60a9c-105">However, there are some aspects of the JavaScript representation of Windows Runtime elements that you should keep in mind.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="60a9c-106">Pour plus d’informations sur la création de composants Windows Runtime en C++, C# ou Visual Basic et pour les consommer en JavaScript, voir [création de composants Windows Runtime en c++][WindowsUwpComponentsCreatingCpp] et [création de composants Windows Runtime en C# et Visual Basic][WindowsUwpComponentsCreatingCsharpVb].</span><span class="sxs-lookup"><span data-stu-id="60a9c-106">For information about creating Windows Runtime components in C++, C#, or Visual Basic and consuming them in JavaScript, see [Creating Windows Runtime Components in C++][WindowsUwpComponentsCreatingCpp] and [Creating Windows Runtime Components in C# and Visual Basic][WindowsUwpComponentsCreatingCsharpVb].</span></span>  

## <span data-ttu-id="60a9c-107">Cas particuliers dans la représentation JavaScript des types Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="60a9c-107">Special cases in the JavaScript Representation of Windows Runtime types</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="60a9c-108">String</span><span class="sxs-lookup"><span data-stu-id="60a9c-108">Strings</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="60a9c-109">Une chaîne non initialisée est transmise à une méthode Windows Runtime en tant que chaîne «non définie» et une chaîne définie sur `null` est transmise en tant que chaîne «NULL».</span><span class="sxs-lookup"><span data-stu-id="60a9c-109">An uninitialized string is passed to a Windows Runtime method as the string "undefined", and a string set to `null` is passed as the string "null".</span></span>  <span data-ttu-id="60a9c-110">\ (C’est vrai chaque fois qu’une `null` `undefined` valeur ou est forcée en une chaîne. \) avant de transmettre une chaîne à une méthode Windows Runtime, vous devez l’initialiser comme chaîne vide \ ("" \).</span><span class="sxs-lookup"><span data-stu-id="60a9c-110">\(This is true whenever a `null` or `undefined` value is coerced to a string.\)  Before you pass a string to a Windows Runtime method, you should initialize it as the empty string \(""\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="60a9c-111">Implément</span><span class="sxs-lookup"><span data-stu-id="60a9c-111">Interfaces</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="60a9c-112">Il n’est pas possible d’implémenter une interface Windows Runtime en JavaScript.</span><span class="sxs-lookup"><span data-stu-id="60a9c-112">You cannot implement a Windows Runtime interface in JavaScript.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="60a9c-113">Matrices</span><span class="sxs-lookup"><span data-stu-id="60a9c-113">Arrays</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="60a9c-114">Les tableaux Windows Runtime ne sont pas redimensionnables, de sorte que les méthodes qui redimensionnent des tableaux en JavaScript ne fonctionnent pas sur les tableaux Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="60a9c-114">Windows Runtime arrays are not resizable, so methods that resize arrays in JavaScript do not work on Windows Runtime arrays.</span></span>  
      *   <span data-ttu-id="60a9c-115">Tableaux: Si vous passez une valeur de tableau JavaScript à une méthode Windows Runtime, le tableau est copié.</span><span class="sxs-lookup"><span data-stu-id="60a9c-115">Arrays: If you pass a JavaScript array value to a Windows Runtime method, the array is copied.</span></span>  <span data-ttu-id="60a9c-116">La méthode Windows Runtime n’est pas en mesure de modifier le tableau ou ses membres, et de les retourner dans votre application JavaScript.</span><span class="sxs-lookup"><span data-stu-id="60a9c-116">The Windows Runtime method is not able to modify the array or its members and return it to your JavaScript app.</span></span>  <span data-ttu-id="60a9c-117">Toutefois, vous pouvez utiliser des tableaux typés (par exemple, l' [objet Int32Array][MDNInt32array]\) qui ne sont pas copiés.</span><span class="sxs-lookup"><span data-stu-id="60a9c-117">However, you can use typed arrays \(for example, [Int32Array Object][MDNInt32array]\), which are not copied.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="60a9c-118">Structures</span><span class="sxs-lookup"><span data-stu-id="60a9c-118">Structures</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="60a9c-119">Les structures Windows Runtime sont des objets en JavaScript.</span><span class="sxs-lookup"><span data-stu-id="60a9c-119">Windows Runtime structures are objects in JavaScript.</span></span>  <span data-ttu-id="60a9c-120">Si vous souhaitez transmettre une structure Windows Runtime à une méthode Windows Runtime, n’instanciez pas la structure avec le `new` mot-clé.</span><span class="sxs-lookup"><span data-stu-id="60a9c-120">If you want to pass a Windows Runtime structure to a Windows Runtime method, don't instantiate the structure with the `new` keyword.</span></span>  <span data-ttu-id="60a9c-121">Créez plutôt un objet, puis ajoutez les membres pertinents et leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="60a9c-121">Instead, create an object and add the relevant members and their values.</span></span>  <span data-ttu-id="60a9c-122">Les noms des membres doivent être en majuscules mixtes: `SomeStruct.firstMember` .</span><span class="sxs-lookup"><span data-stu-id="60a9c-122">The names of the members should be in camel case: `SomeStruct.firstMember`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="60a9c-123">Objets</span><span class="sxs-lookup"><span data-stu-id="60a9c-123">Objects</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="60a9c-124">Les objets JavaScript ne sont pas identiques aux objets de code managé \ ( `System.Object` \).</span><span class="sxs-lookup"><span data-stu-id="60a9c-124">JavaScript objects aren't the same as managed code objects \(`System.Object`\).</span></span>  <span data-ttu-id="60a9c-125">Vous ne pouvez pas transmettre un objet JavaScript à une méthode Windows Runtime qui nécessite a `System.Object` .</span><span class="sxs-lookup"><span data-stu-id="60a9c-125">You can't pass a JavaScript object to a Windows Runtime method that requires a `System.Object`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="60a9c-126">Identité de l’objet</span><span class="sxs-lookup"><span data-stu-id="60a9c-126">Object identity</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="60a9c-127">Dans la plupart des cas, les objets transmis entre les fenêtres Runtime et JavaScript ne changent pas.</span><span class="sxs-lookup"><span data-stu-id="60a9c-127">In most cases, the objects passed back and forth between the Windows Runtime and JavaScript do not change.</span></span>  <span data-ttu-id="60a9c-128">Le moteur JavaScript maintient une carte d’objets connus.</span><span class="sxs-lookup"><span data-stu-id="60a9c-128">The JavaScript engine maintains a map of known objects.</span></span>  <span data-ttu-id="60a9c-129">Lorsqu’un objet est retourné à partir du Windows Runtime, il est mis en correspondance avec la carte et, s’il n’existe pas, un nouvel objet est créé.</span><span class="sxs-lookup"><span data-stu-id="60a9c-129">When an object is returned from the Windows Runtime it is matched against the map, and if it does not exist a new object is created.</span></span>  <span data-ttu-id="60a9c-130">La même procédure est suivie pour les objets qui représentent des interfaces qui sont renvoyées par des méthodes Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="60a9c-130">The same procedure is followed for objects that represent interfaces that are returned by Windows Runtime methods.</span></span>  <span data-ttu-id="60a9c-131">Il existe deux types d’exceptions:</span><span class="sxs-lookup"><span data-stu-id="60a9c-131">There are two kinds of exceptions:</span></span>  
      
      *   <span data-ttu-id="60a9c-132">Les objets renvoyés par un appel Windows Runtime, puis dotés de nouvelles propriétés \ (expando \) ajoutés, ne conservent pas leurs nouvelles propriétés lorsqu’elles sont transmises au Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="60a9c-132">Objects that are returned from a Windows Runtime call, and then have new \(expando\) properties added, don't retain their new properties when they are passed back to the Windows Runtime.</span></span>  <span data-ttu-id="60a9c-133">Néanmoins, lorsque ces objets sont retournés à l’application JavaScript, car ils sont associés à l’objet existant, l’objet renvoyé possède les propriétés expando.</span><span class="sxs-lookup"><span data-stu-id="60a9c-133">However, when they are returned to the JavaScript app, because they're matched to the existing object, the returned object does have the expando properties.</span></span>  
      *   <span data-ttu-id="60a9c-134">Dans Windows Runtime, les structures et délégués ne peuvent pas être identifiés comme identiques aux structures ou délégués déjà utilisés.</span><span class="sxs-lookup"><span data-stu-id="60a9c-134">Structures and delegates in Windows Runtime can't be identified as identical to previously-used structures or delegates.</span></span>  <span data-ttu-id="60a9c-135">Chaque fois qu’une structure ou un délégué est retourné, elle obtient une nouvelle référence.</span><span class="sxs-lookup"><span data-stu-id="60a9c-135">Every time a structure or delegate is returned, it gets a new reference.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="60a9c-136">Collisions de noms</span><span class="sxs-lookup"><span data-stu-id="60a9c-136">Name collisions</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="60a9c-137">Plusieurs interfaces Windows Runtime peuvent avoir des membres du même nom.</span><span class="sxs-lookup"><span data-stu-id="60a9c-137">Multiple Windows Runtime interfaces may have members with the same names.</span></span>  <span data-ttu-id="60a9c-138">S’ils sont combinés dans un seul objet JavaScript (qui peut être une représentation d’une classe Runtime ou d’une interface), les membres sont représentés par des noms complets.</span><span class="sxs-lookup"><span data-stu-id="60a9c-138">If they are combined in a single JavaScript object (which can be a representation of a runtime class or an interface), the members are represented with fully-qualified names.</span></span>  <span data-ttu-id="60a9c-139">Vous pouvez appeler ces membres en utilisant la syntaxe suivante:</span><span class="sxs-lookup"><span data-stu-id="60a9c-139">You can call these members by using the following syntax:</span></span>  
      
      ```cpp
      Class["MemberName"](parameter)
      ```  
      
      <span data-ttu-id="60a9c-140">Dans le code suivant, deux interfaces disposent d’une méthode Draw, et une classe Runtime implémente les deux interfaces.</span><span class="sxs-lookup"><span data-stu-id="60a9c-140">In the following code, two interfaces have a Draw method, and a runtime class implements both interfaces.</span></span>  
      
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
      
      <span data-ttu-id="60a9c-141">Voici comment vous pouvez appeler le code ci-dessus en JavaScript.</span><span class="sxs-lookup"><span data-stu-id="60a9c-141">Here is how you can call the above code in JavaScript.</span></span>  
      
      ```javascript
      var example = new ExampleObject();
      example["CollisionExample.InterfaceA.draw"](12);
      example["CollisionExample.InterfaceB.draw"]("hello");
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `Out` <span data-ttu-id="60a9c-142">paramètres</span><span class="sxs-lookup"><span data-stu-id="60a9c-142">parameters</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="60a9c-143">Si une méthode Windows Runtime comporte plusieurs `out` paramètres, dans JavaScript, la méthode possède un objet JavaScript comme valeur de retour, et l’objet possède des propriétés qui correspondent au `out` paramètre.</span><span class="sxs-lookup"><span data-stu-id="60a9c-143">If a Windows Runtime method has multiple `out` parameters, in JavaScript the method has a JavaScript object as its return value, and the object has properties that correspond to the `out` parameter.</span></span>  <span data-ttu-id="60a9c-144">Par exemple, considérez la signature Windows Runtime suivante en C++.</span><span class="sxs-lookup"><span data-stu-id="60a9c-144">For example, consider the following Windows Runtime signature in C++.</span></span>  
      
      ```cpp
      void ExampleMethod(
          [OutAttribute] char^ first,
          [OutAttribute] char^ second
      )
      ```  
      
      <span data-ttu-id="60a9c-145">La version JavaScript de cette signature est la suivante:</span><span class="sxs-lookup"><span data-stu-id="60a9c-145">The JavaScript version of this signature is:</span></span>  
      
      ```javascript
      var returnValue = exampleMethod();
      ```  
      
      <span data-ttu-id="60a9c-146">Dans cet exemple, `returnValue` est un objet JavaScript qui comporte deux champs: `first` et `second` .</span><span class="sxs-lookup"><span data-stu-id="60a9c-146">In this example, `returnValue` is a JavaScript object that has two fields: `first` and `second`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="60a9c-147">Membres statiques</span><span class="sxs-lookup"><span data-stu-id="60a9c-147">Static members</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="60a9c-148">Windows Runtime définit à la fois les membres statiques et les membres d’instance.</span><span class="sxs-lookup"><span data-stu-id="60a9c-148">The Windows Runtime defines both static members and instance members.</span></span>  <span data-ttu-id="60a9c-149">Dans JavaScript, les membres statiques sont ajoutés à l’objet associé à la classe ou à l’interface Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="60a9c-149">In JavaScript, static members are added to the object that is associated with the Windows Runtime class or interface.</span></span>  
      
      ```javascript
      // Static method.
      var accel = Windows.Devices.Sensors.Accelerometer.getDefault();
      // Instance method.
      var reading = accel.getCurrentReading();
      ```  
   :::column-end:::
:::row-end:::  
    
<span data-ttu-id="60a9c-150">Pour plus d’informations sur la représentation JavaScript des types Windows Runtime basique, voir [représentation JavaScript des types Windows Runtime][WindowsRuntimeJavascriptTypes].</span><span class="sxs-lookup"><span data-stu-id="60a9c-150">For more information about the JavaScript representation of Windows Runtime basic types, see [JavaScript Representation of Windows Runtime Types][WindowsRuntimeJavascriptTypes].</span></span>  

<!-- links -->  
 
[WindowsRuntimeJavascriptTypes]: ./javascript-representation-of-windows-runtime-types.md "Représentation JavaScript des types Windows Runtime | Documents Microsoft"

[WindowsUwpComponentsCreatingCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Composants Windows Runtime avec C++/CX | Documents Microsoft"  
[WindowsUwpComponentsCreatingCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Composants Windows Runtime avec C# et Visual Basic | Documents Microsoft"  

[MDNInt32array]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Int32Array "Int32Array | MDN"  
