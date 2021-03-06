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
# <a name="handling-windows-runtime-events-in-javascript"></a>Gestion des événements Windows Runtime dans JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Les événements Windows Runtime ne sont pas représentés de la même manière en JavaScript qu’en C++ ou dans le .NET Framework.  Ce ne sont pas des propriétés de classe, mais plutôt des identificateurs de chaîne \(minuscules\) qui sont transmis aux méthodes et à la `addEventListener` `removeEventListener` classe.  Par exemple, vous pouvez ajouter un handler d’événements pour l’événement [Geolocator.PositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] en passant la chaîne `positionchanged` à la méthode `Geolocator.addEventListener` :  

```javascript  
var locator = new Windows.Devices.Geolocation.Geolocator();
locator.addEventListener(
    "positionchanged",
    function (ev) {
        console.log("Got event");
    });
```  

Vous pouvez également définir la `locator.onpositionchanged` propriété :  

```javascript
locator.onpositionchanged =
    function (ev) {
        console.log("Got event");
    };
```  

Une autre différence entre .NET/C++ et JavaScript est le nombre de paramètres pris par un handler d’événements.  Dans .NET/C++, un handler en prend deux : l’expéditeur de l’événement et les données d’événement.  Dans JavaScript, les deux sont regroupés en tant qu’objet `Event` unique.  Dans l’exemple suivant, le paramètre contient à la fois l’expéditeur de l’événement \(la propriété\) et les propriétés de données d’événement `ev` `target` \(ici, juste `position` \).  Les propriétés de données d’événement sont les propriétés documentées pour chaque événement.  

```javascript
function (ev) {
    console.log("Sender: " + ev.target);
    console.log("Position: " +
        ev.position.latitude + "," +
        ev.position.longitude);
};
```  

> [!IMPORTANT]
> Les fonctionnalités Windows Runtime ne sont pas disponibles pour les applications qui s’exécutent dans Internet Explorer.  

## <a name="see-also"></a>Voir également  

[Utilisation de Windows Runtime en JavaScript][WindowsRuntimeJavascript]  

 <!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Utilisation de Windows Runtime en JavaScript | Documents Microsoft"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Classe Geolocator | Documents Microsoft"  
