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
# Éléments à prendre en compte lors de l’utilisation de l’API Windows Runtime  

Vous pouvez utiliser presque tous les éléments de l’API Windows Runtime en JavaScript.  Néanmoins, il existe certains aspects de la représentation JavaScript des éléments Windows Runtime que vous devez garder à l’esprit.  

> [!IMPORTANT]
> Pour plus d’informations sur la création de composants Windows Runtime en C++, C# ou Visual Basic et pour les consommer en JavaScript, voir [création de composants Windows Runtime en c++][WindowsUwpComponentsCreatingCpp] et [création de composants Windows Runtime en C# et Visual Basic][WindowsUwpComponentsCreatingCsharpVb].  

## Cas particuliers dans la représentation JavaScript des types Windows Runtime  

*   Chaînes: une chaîne non initialisée est transmise à une méthode Windows Runtime en tant que chaîne «non définie» et une chaîne définie sur `null` est transmise en tant que chaîne «NULL».  \ (C’est vrai chaque fois qu’une `null` `undefined` valeur ou est forcée en une chaîne. \) avant de transmettre une chaîne à une méthode Windows Runtime, vous devez l’initialiser comme chaîne vide \ ("" \).  
*   Interfaces: il est impossible d’implémenter une interface Windows Runtime en JavaScript.  
*   Tableaux: les tableaux Windows Runtime ne sont pas redimensionnables, de sorte que les méthodes permettant de redimensionner des tableaux en JavaScript ne fonctionnent pas sur les tableaux Windows Runtime.  
*   Tableaux: Si vous passez une valeur de tableau JavaScript à une méthode Windows Runtime, le tableau est copié.  La méthode Windows Runtime n’est pas en mesure de modifier le tableau ou ses membres, et de les retourner dans votre application JavaScript.  Toutefois, vous pouvez utiliser des tableaux typés (par exemple, l' [objet Int32Array][MDNInt32array]\) qui ne sont pas copiés.  
*   Structures: les structures Windows Runtime sont des objets en JavaScript.  Si vous souhaitez transmettre une structure Windows Runtime à une méthode Windows Runtime, n’instanciez pas la structure avec le `new` mot-clé.  Créez plutôt un objet, puis ajoutez les membres pertinents et leurs valeurs.  Les noms des membres doivent être en majuscules mixtes: `SomeStruct.firstMember` .  
*   Objets: les objets JavaScript ne sont pas identiques aux objets de code managé \ ( `System.Object` \).  Vous ne pouvez pas transmettre un objet JavaScript à une méthode Windows Runtime qui nécessite a `System.Object` .  
*   Identité de l’objet: dans la plupart des cas, les objets transmis entre Windows Runtime et JavaScript ne changent pas.  Le moteur JavaScript maintient une carte d’objets connus.  Lorsqu’un objet est retourné à partir du Windows Runtime, il est mis en correspondance avec la carte et, s’il n’existe pas, un nouvel objet est créé.  La même procédure est suivie pour les objets qui représentent des interfaces qui sont renvoyées par des méthodes Windows Runtime.  Il existe deux types d’exceptions:  

    *   Les objets renvoyés par un appel Windows Runtime, puis dotés de nouvelles propriétés \ (expando \) ajoutés, ne conservent pas leurs nouvelles propriétés lorsqu’elles sont transmises au Windows Runtime.  Néanmoins, lorsque ces objets sont retournés à l’application JavaScript, car ils sont associés à l’objet existant, l’objet renvoyé possède les propriétés expando.  
    *   Dans Windows Runtime, les structures et délégués ne peuvent pas être identifiés comme identiques aux structures ou délégués déjà utilisés.  Chaque fois qu’une structure ou un délégué est retourné, elle obtient une nouvelle référence.  

*   Conflits de nom: plusieurs interfaces Windows Runtime peuvent avoir des membres du même nom.  S’ils sont combinés dans un seul objet JavaScript (qui peut être une représentation d’une classe Runtime ou d’une interface), les membres sont représentés par des noms complets.  Vous pouvez appeler ces membres en utilisant la syntaxe suivante:  
    
    ```cpp
    Class["MemberName"](parameter)
    ```  
    
    Dans le code suivant, deux interfaces disposent d’une méthode Draw, et une classe Runtime implémente les deux interfaces.  
    
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
    
*   `Out` paramètres: si une méthode Windows Runtime comporte plusieurs `out` paramètres, en JavaScript, la méthode possède un objet JavaScript comme valeur de retour et l’objet possède des propriétés qui correspondent au `out` paramètre.  Par exemple, considérez la signature Windows Runtime suivante en C++.  
    
    ```cpp
    void ExampleMethod(
      [OutAttribute] char^ first,
      [OutAttribute] char^ second
    )
    ```  
    
    La version JavaScript de cette signature est la suivante:  
    
    ```javascript
    var returnValue = exampleMethod();
    ```  
    
    Dans cet exemple, `returnValue` est un objet JavaScript qui comporte deux champs: `first` et `second` .  
    
*   Membres statiques: Windows Runtime définit à la fois les membres statiques et les membres d’instance.  Dans JavaScript, les membres statiques sont ajoutés à l’objet associé à la classe ou à l’interface Windows Runtime.  
    
    ```javascript
    // Static method.
    var accel = Windows.Devices.Sensors.Accelerometer.getDefault();
    // Instance method.
    var reading = accel.getCurrentReading();
    ```  
    
Pour plus d’informations sur la représentation JavaScript des types Windows Runtime basique, voir [représentation JavaScript des types Windows Runtime][WindowsRuntimeJavascriptTypes].  

<!-- image links -->  

<!-- links -->  
 
[WindowsRuntimeJavascriptTypes]: /microsoft-edge/windows-runtime/javascript-representation-of-windows-runtime-types "Représentation JavaScript des types Windows Runtime"

[WindowsUwpComponentsCreatingCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Composants Windows Runtime avec C++/CX"  
[WindowsUwpComponentsCreatingCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Composants Windows Runtime avec C# et Visual Basic"  

[MDNInt32array]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Int32Array "Int32Array | MDN"  