---
description: Considérations relatives à l’utilisation de l’API Windows Runtime
title: Considérations relatives à l’utilisation de l’API Windows Runtime
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime API
ms.assetid: 2f56d70c-c80d-4876-8e6a-8ae031d31c22
caps.latest.revision: 8
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 170374fd109802bff0aa0fc93cea6c8d50c9d7c7
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399343"
---
# <a name="considerations-when-using-the-windows-runtime-api"></a>Considérations relatives à l’utilisation de l’API Windows Runtime  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Vous pouvez utiliser presque tous les éléments de l’API Windows Runtime en JavaScript.  Toutefois, il existe certains aspects de la représentation JavaScript des éléments Windows Runtime que vous devez garder à l’esprit.  

> [!IMPORTANT]
> Pour plus d’informations sur la création de composants Windows Runtime en C++, C# ou Visual Basic et leur consommation en JavaScript, voir Création de [composants Windows Runtime en C++][WindowsUwpComponentsCreatingCpp] et création de [composants Windows Runtime][WindowsUwpComponentsCreatingCsharpVb]dans C# et Visual Basic .  

## <a name="special-cases-in-the-javascript-representation-of-windows-runtime-types"></a>Cas particuliers dans la représentation JavaScript des types Windows Runtime  

:::row:::
   :::column span="1":::
      Chaînes  
   :::column-end:::
   :::column span="3":::
      Une chaîne non mise à jour est transmise à une méthode Windows Runtime en tant que chaîne « non définie » et une chaîne définie comme chaîne « `null` null ».  \(Ceci est vrai chaque fois qu’une ou une valeur est contrainte en chaîne.\) Avant de transmettre une chaîne à une méthode Windows Runtime, vous devez l’initialiser en tant que chaîne vide `null` `undefined` \(«\).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Interfaces  
   :::column-end:::
   :::column span="3":::
      Vous ne pouvez pas implémenter une interface Windows Runtime en JavaScript.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Tableaux  
   :::column-end:::
   :::column span="3":::
      Les tableaux Windows Runtime ne sont pas resizables, de sorte que les méthodes qui resérialisent les tableaux en JavaScript ne fonctionnent pas sur les tableaux Windows Runtime.  
      *   Tableaux : si vous passez une valeur de tableau JavaScript à une méthode Windows Runtime, le tableau est copié.  La méthode Windows Runtime n’est pas en mesure de modifier le tableau ou ses membres et de le renvoyer à votre application JavaScript.  Toutefois, vous pouvez utiliser des tableaux typés \(par exemple, Objet [Int32Array][MDNInt32array]\), qui ne sont pas copiés.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Structures  
   :::column-end:::
   :::column span="3":::
      Les structures Windows Runtime sont des objets en JavaScript.  Si vous souhaitez transmettre une structure Windows Runtime à une méthode Windows Runtime, n’inssérez pas la structure avec le `new` mot clé.  Au lieu de cela, créez un objet et ajoutez les membres pertinents et leurs valeurs.  Les noms des membres doivent être en cas de caméo : `SomeStruct.firstMember` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Objets  
   :::column-end:::
   :::column span="3":::
      Les objets JavaScript ne sont pas identiques aux objets avec code géré \( `System.Object` \).  Vous ne pouvez pas transmettre un objet JavaScript à une méthode Windows Runtime qui nécessite un `System.Object` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Identité de l’objet  
   :::column-end:::
   :::column span="3":::
      Dans la plupart des cas, les objets transmis entre Windows Runtime et JavaScript ne changent pas.  Le moteur JavaScript conserve une carte d’objets connus.  Lorsqu’un objet est renvoyé à partir de Windows Runtime, il est mis en correspondance avec la carte et, s’il n’existe pas, un nouvel objet est créé.  La même procédure est suivie pour les objets qui représentent des interfaces renvoyées par les méthodes Windows Runtime.  Il existe deux types d’exceptions :  
      
      *   Les objets qui sont renvoyés à partir d’un appel Windows Runtime, puis qui ont de nouvelles propriétés \(expando\) ajoutées, ne conservent pas leurs nouvelles propriétés lorsqu’elles sont passées à Windows Runtime.  Toutefois, lorsqu’ils sont renvoyés à l’application JavaScript, car ils sont en correspondance avec l’objet existant, l’objet renvoyé a les propriétés expando.  
      *   Les structures et délégués dans Windows Runtime ne peuvent pas être identifiés comme identiques aux structures ou délégués précédemment utilisés.  Chaque fois qu’une structure ou un délégué est renvoyé, il obtient une nouvelle référence.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Collisions de noms  
   :::column-end:::
   :::column span="3":::
      Plusieurs interfaces Windows Runtime peuvent avoir des membres du même nom.  S’ils sont combinés dans un seul objet JavaScript (qui peut être une représentation d’une classe runtime ou d’une interface), les membres sont représentés avec des noms complets.  Vous pouvez appeler ces membres à l’aide de la syntaxe suivante :  
      
      ```cpp
      Class["MemberName"](parameter)
      ```  
      
      Dans le code suivant, deux interfaces ont une méthode Draw et une classe runtime implémente les deux interfaces.  
      
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
      
      Voici comment vous pouvez appeler le code ci-dessus en JavaScript.  
      
      ```javascript
      var example = new ExampleObject();
      example["CollisionExample.InterfaceA.draw"](12);
      example["CollisionExample.InterfaceB.draw"]("hello");
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `Out` parameters  
   :::column-end:::
   :::column span="3":::
      Si une méthode Windows Runtime possède plusieurs paramètres, dans JavaScript, la méthode possède un objet JavaScript comme valeur de retour, et l’objet possède des propriétés qui `out` correspondent au `out` paramètre.  Par exemple, prenons la signature Windows Runtime suivante en C++.  
      
      ```cpp
      void ExampleMethod(
          [OutAttribute] char^ first,
          [OutAttribute] char^ second
      )
      ```  
      
      La version JavaScript de cette signature est :  
      
      ```javascript
      var returnValue = exampleMethod();
      ```  
      
      Dans cet exemple, `returnValue` est un objet JavaScript qui a deux champs : `first` et `second` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Membres statiques  
   :::column-end:::
   :::column span="3":::
      Windows Runtime définit les membres statiques et les membres d’instance.  Dans JavaScript, des membres statiques sont ajoutés à l’objet associé à la classe ou à l’interface Windows Runtime.  
      
      ```javascript
      // Static method.
      var accel = Windows.Devices.Sensors.Accelerometer.getDefault();
      // Instance method.
      var reading = accel.getCurrentReading();
      ```  
   :::column-end:::
:::row-end:::  
    
Pour plus d’informations sur la représentation JavaScript des types de base Windows Runtime, voir Représentation [JavaScript des types Windows Runtime.][WindowsRuntimeJavascriptTypes]  

<!-- links -->  
 
[WindowsRuntimeJavascriptTypes]: ./javascript-representation-of-windows-runtime-types.md "Représentation JavaScript des types Windows Runtime | Documents Microsoft"  

[WindowsUwpComponentsCreatingCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Composants Windows Runtime avec C++/CX | Documents Microsoft"  
[WindowsUwpComponentsCreatingCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Composants Windows Runtime avec C# et Visual Basic | Documents Microsoft"  

[MDNInt32array]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Int32Array "Int32Array | MDN"  
