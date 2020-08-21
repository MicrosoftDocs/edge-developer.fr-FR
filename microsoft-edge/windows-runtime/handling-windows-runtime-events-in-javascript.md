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
# Gestion des événements Windows Runtime en JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Les événements Windows Runtime ne sont pas représentés de la même manière dans JavaScript en C++ ou .NET Framework.  Il ne s’agit pas de propriétés de classe, mais sont des identificateurs de chaîne \ (minuscules) qui sont transmis aux `addEventListener` méthodes et au cours `removeEventListener` .  Par exemple, vous pouvez ajouter un gestionnaire d’événements pour l’événement [géolocateur. PositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] en transmettant la chaîne `positionchanged` à la `Geolocator.addEventListener` méthode:  

```javascript  
var locator = new Windows.Devices.Geolocation.Geolocator();
locator.addEventListener(
    "positionchanged",
    function (ev) {
        console.log("Got event");
    });
```  

Vous pouvez également définir la `locator.onpositionchanged` propriété:  

```javascript
locator.onpositionchanged =
    function (ev) {
        console.log("Got event");
    };
```  

Une autre différence entre .NET/C++ et JavaScript est le nombre de paramètres effectués par un gestionnaire d’événements.  Dans .NET/C++, un gestionnaire utilise deux éléments: l’expéditeur de l’événement et les données d’événement.  Dans JavaScript, les deux sont regroupées comme un `Event` objet unique.  Dans l’exemple suivant, le `ev` paramètre contient à la fois l’expéditeur de l’événement \ (la `target` propriété \) et les propriétés des données d’événements (ici, uniquement `position` \).  Les propriétés de données d’événements sont décrites dans chaque événement.  

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

## Voir également  

[Utilisation de Windows Runtime en JavaScript][WindowsRuntimeJavascript]  

 <!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Utilisation de Windows Runtime en JavaScript | Documents Microsoft"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Classe de géolocalisation | Documents Microsoft"  
