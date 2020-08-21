---
title: Gestion des événements Windows Runtime dans JavaScript
ms.custom: ''
ms.date: 07/29/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime events
- Windows Runtime events [JavaScript]
ms.assetid: d9436aff-2c30-4846-b8df-eaa3e63fd75c
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: fe44457206569c1e32c40514b4b186bec50d1e3c
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942161"
---
# <span data-ttu-id="741d8-102">Gestion des événements Windows Runtime en JavaScript</span><span class="sxs-lookup"><span data-stu-id="741d8-102">Handling Windows Runtime events in JavaScript</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="741d8-103">Les événements Windows Runtime ne sont pas représentés de la même manière dans JavaScript en C++ ou .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="741d8-103">Windows Runtime events are not represented in the same way in JavaScript as they are in C++ or the .NET Framework.</span></span>  <span data-ttu-id="741d8-104">Il ne s’agit pas de propriétés de classe, mais sont des identificateurs de chaîne \ (minuscules) qui sont transmis aux `addEventListener` méthodes et au cours `removeEventListener` .</span><span class="sxs-lookup"><span data-stu-id="741d8-104">They are not class properties, but rather are represented as \(lowercase\) string identifiers that are passed to the class's `addEventListener` and `removeEventListener` methods.</span></span>  <span data-ttu-id="741d8-105">Par exemple, vous pouvez ajouter un gestionnaire d’événements pour l’événement [géolocateur. PositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] en transmettant la chaîne `positionchanged` à la `Geolocator.addEventListener` méthode:</span><span class="sxs-lookup"><span data-stu-id="741d8-105">For example, you can add an event handler for the [Geolocator.PositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] event by passing the string `positionchanged` to the `Geolocator.addEventListener` method:</span></span>  

```javascript  
var locator = new Windows.Devices.Geolocation.Geolocator();
locator.addEventListener(
    "positionchanged",
    function (ev) {
        console.log("Got event");
    });
```  

<span data-ttu-id="741d8-106">Vous pouvez également définir la `locator.onpositionchanged` propriété:</span><span class="sxs-lookup"><span data-stu-id="741d8-106">You can also set the `locator.onpositionchanged` property:</span></span>  

```javascript
locator.onpositionchanged =
    function (ev) {
        console.log("Got event");
    };
```  

<span data-ttu-id="741d8-107">Une autre différence entre .NET/C++ et JavaScript est le nombre de paramètres effectués par un gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="741d8-107">Another difference between .NET/C++ and JavaScript is the number of parameters taken by an event handler.</span></span>  <span data-ttu-id="741d8-108">Dans .NET/C++, un gestionnaire utilise deux éléments: l’expéditeur de l’événement et les données d’événement.</span><span class="sxs-lookup"><span data-stu-id="741d8-108">In .NET/C++, a handler takes two:  the event sender, and the event data.</span></span>  <span data-ttu-id="741d8-109">Dans JavaScript, les deux sont regroupées comme un `Event` objet unique.</span><span class="sxs-lookup"><span data-stu-id="741d8-109">In JavaScript, the two are bundled as a single `Event` object.</span></span>  <span data-ttu-id="741d8-110">Dans l’exemple suivant, le `ev` paramètre contient à la fois l’expéditeur de l’événement \ (la `target` propriété \) et les propriétés des données d’événements (ici, uniquement `position` \).</span><span class="sxs-lookup"><span data-stu-id="741d8-110">In the following example, the `ev` parameter contains both the sender of the event \(the `target` property\) and the event data properties \(here, just `position`\).</span></span>  <span data-ttu-id="741d8-111">Les propriétés de données d’événements sont décrites dans chaque événement.</span><span class="sxs-lookup"><span data-stu-id="741d8-111">The event data properties are the ones that are documented for each event.</span></span>  

```javascript
function (ev) {
    console.log("Sender: " + ev.target);
    console.log("Position: " +
        ev.position.latitude + "," +
        ev.position.longitude);
};
```  

> [!IMPORTANT]
> <span data-ttu-id="741d8-112">Les fonctionnalités Windows Runtime ne sont pas disponibles pour les applications qui s’exécutent dans Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="741d8-112">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <span data-ttu-id="741d8-113">Voir également</span><span class="sxs-lookup"><span data-stu-id="741d8-113">See also</span></span>  

[<span data-ttu-id="741d8-114">Utilisation de Windows Runtime en JavaScript</span><span class="sxs-lookup"><span data-stu-id="741d8-114">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

 <!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Utilisation de Windows Runtime en JavaScript | Documents Microsoft"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Classe de géolocalisation | Documents Microsoft"  
