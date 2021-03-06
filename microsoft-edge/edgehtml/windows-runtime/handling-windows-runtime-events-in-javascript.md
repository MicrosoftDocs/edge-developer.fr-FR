---
description: Gestion des événements Windows Runtime dans JavaScript
title: Gestion des événements Windows Runtime dans JavaScript
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime events
- Windows Runtime events [JavaScript]
ms.assetid: d9436aff-2c30-4846-b8df-eaa3e63fd75c
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 08562f7ebff0c02b96bfc8229238a62463b95451
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397523"
---
# <a name="handling-windows-runtime-events-in-javascript"></a><span data-ttu-id="9fd29-103">Gestion des événements Windows Runtime dans JavaScript</span><span class="sxs-lookup"><span data-stu-id="9fd29-103">Handling Windows Runtime events in JavaScript</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="9fd29-104">Les événements Windows Runtime ne sont pas représentés de la même manière en JavaScript qu’en C++ ou dans le .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="9fd29-104">Windows Runtime events are not represented in the same way in JavaScript as they are in C++ or the .NET Framework.</span></span>  <span data-ttu-id="9fd29-105">Ce ne sont pas des propriétés de classe, mais plutôt des identificateurs de chaîne \(minuscules\) qui sont transmis aux méthodes et à la `addEventListener` `removeEventListener` classe.</span><span class="sxs-lookup"><span data-stu-id="9fd29-105">They are not class properties, but rather are represented as \(lowercase\) string identifiers that are passed to the class's `addEventListener` and `removeEventListener` methods.</span></span>  <span data-ttu-id="9fd29-106">Par exemple, vous pouvez ajouter un handler d’événements pour l’événement [Geolocator.PositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] en passant la chaîne `positionchanged` à la méthode `Geolocator.addEventListener` :</span><span class="sxs-lookup"><span data-stu-id="9fd29-106">For example, you can add an event handler for the [Geolocator.PositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] event by passing the string `positionchanged` to the `Geolocator.addEventListener` method:</span></span>  

```javascript  
var locator = new Windows.Devices.Geolocation.Geolocator();
locator.addEventListener(
    "positionchanged",
    function (ev) {
        console.log("Got event");
    });
```  

<span data-ttu-id="9fd29-107">Vous pouvez également définir la `locator.onpositionchanged` propriété :</span><span class="sxs-lookup"><span data-stu-id="9fd29-107">You can also set the `locator.onpositionchanged` property:</span></span>  

```javascript
locator.onpositionchanged =
    function (ev) {
        console.log("Got event");
    };
```  

<span data-ttu-id="9fd29-108">Une autre différence entre .NET/C++ et JavaScript est le nombre de paramètres pris par un handler d’événements.</span><span class="sxs-lookup"><span data-stu-id="9fd29-108">Another difference between .NET/C++ and JavaScript is the number of parameters taken by an event handler.</span></span>  <span data-ttu-id="9fd29-109">Dans .NET/C++, un handler en prend deux : l’expéditeur de l’événement et les données d’événement.</span><span class="sxs-lookup"><span data-stu-id="9fd29-109">In .NET/C++, a handler takes two:  the event sender, and the event data.</span></span>  <span data-ttu-id="9fd29-110">Dans JavaScript, les deux sont regroupés en tant qu’objet `Event` unique.</span><span class="sxs-lookup"><span data-stu-id="9fd29-110">In JavaScript, the two are bundled as a single `Event` object.</span></span>  <span data-ttu-id="9fd29-111">Dans l’exemple suivant, le paramètre contient à la fois l’expéditeur de l’événement \(la propriété\) et les propriétés de données d’événement `ev` `target` \(ici, juste `position` \).</span><span class="sxs-lookup"><span data-stu-id="9fd29-111">In the following example, the `ev` parameter contains both the sender of the event \(the `target` property\) and the event data properties \(here, just `position`\).</span></span>  <span data-ttu-id="9fd29-112">Les propriétés de données d’événement sont les propriétés documentées pour chaque événement.</span><span class="sxs-lookup"><span data-stu-id="9fd29-112">The event data properties are the ones that are documented for each event.</span></span>  

```javascript
function (ev) {
    console.log("Sender: " + ev.target);
    console.log("Position: " +
        ev.position.latitude + "," +
        ev.position.longitude);
};
```  

> [!IMPORTANT]
> <span data-ttu-id="9fd29-113">Les fonctionnalités Windows Runtime ne sont pas disponibles pour les applications qui s’exécutent dans Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="9fd29-113">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9fd29-114">Voir également</span><span class="sxs-lookup"><span data-stu-id="9fd29-114">See also</span></span>  

[<span data-ttu-id="9fd29-115">Utilisation de Windows Runtime en JavaScript</span><span class="sxs-lookup"><span data-stu-id="9fd29-115">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

 <!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Utilisation de Windows Runtime en JavaScript | Documents Microsoft"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Classe Geolocator | Documents Microsoft"  
