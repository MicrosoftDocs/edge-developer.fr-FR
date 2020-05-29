---
description: Représente une demande différée d’autorisation utilisateur pour accéder aux fonctionnalités d’appareil
title: Objet DeferredPermissionRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/15/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 6013f20195fc0f5d4f33b871a9c1b01392bf023e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565112"
---
# Objet DeferredPermissionRequest

Représente une requête différée par le contenu du [WebView](../webview.md) pour l’autorisation de l’utilisateur final pour accéder à des fonctionnalités d’appareil spécialisées (par exemple, géolocalisation ou verrouillage de pointeur).

```js
// In this sample, when we receive a permission request we construct some basic UI to ask the
// user if they want to give permission.
webview.addEventListener("MSWebViewPermissionRequested", permissionRequestedEventArgs => {
    const permissionRequest = permissionRequestedEventArgs.permissionRequest;
    const requestContainer = document.createElement("div");

    // We use this function as the handler for the allow and deny buttons.
    function completeDeferredPermissionRequest(allow) {
        // Find the DeferredPermissionRequest using the id of the PermissionRequest we deferred.
        const deferredPermissionRequest = webview.getDeferredPermissionRequestById(permissionRequest.id);
        if (allow) {
            deferredPermissionRequest.allow();
        }
        else {
            deferredPermissionRequest.deny();
        }
        requestContainer.parentElement.removeChild(requestContainer);
    }

    // Construct some simple UI to tell the user about the permission request and get their
    // feedback via the allow and deny buttons
    const description = document.createElement("span");
    description.textContent = "Allow " + uri + " to access " + type + "?";

    const allow = document.createElement("button");
    allow.textContent = "Allow";
    allow.addEventListener("click", () => completeDeferredPermissionRequest(true));

    const deny = document.createElement("button");
    deny.textContent = "Deny";
    deny.addEventListener("click", () => completeDeferredPermissionRequest(false));

    requestContainer.appendChild(description);
    requestContainer.appendChild(allow);
    requestContainer.appendChild(deny);
    document.body.appendChild(requestContainer);

    permissionRequest.defer();
});
```

## Méthodes

### verte

Autorise la demande d’autorisation.

```js
deferredPermissionRequest.allow();
```

#### Parameters

Cette méthode n’a aucun paramètre.

#### Valeur renvoyée

Cette méthode ne renvoie pas de valeur.

### deny

Refuse la demande d’autorisation.

```js
deferredPermissionRequest.deny();
```

#### Parameters

Cette méthode n’a aucun paramètre.

#### Valeur renvoyée

Cette méthode ne renvoie pas de valeur.

## Propriétés

### id

ID unique qui peut être utilisé pour mettre en corrélation le DeferredPermissionRequest actuel avec un objet PermissionRequest à partir d’un événement MSWebViewPermissionRequested précédent. Voir la méthode **PermissionRequested. Defer** .

Cette propriété est en lecture seule.

```js
var id = deferredPermissionRequest.id;
```

##### Valeur de propriété

Type: **longue non signée**

### type

Type d’autorisation demandée. Il s’agit de l’une des valeurs de chaîne suivantes:

- **géolocalisation**: accès aux données d’emplacement par le biais de Navigator. géolocalisation.
- **unlimitedIndexedDBQuota**: autoriser les API IndexedDB à ignorer la limite de taille des données stockées habituellement.
- **média**: accès au microphone et à la caméra par le biais de Navigator. getUserMedia.
- **pointerlock**: possibilité de verrouiller et de contrôler le pointeur de la souris via l’élément. requestPointerLock.
- **webnotifications**: possibilité d’afficher les notifications sur le bureau via une fenêtre. Message.
- **écran**: possibilité de prendre des captures d’écran à l’aide de l’API de capture multimédia.
- **immersiveview**: possibilité de contrôler un affichage VR.

Cette propriété est en lecture seule.

```js
var type = deferredPermissionRequest.type;
```

#### Valeur de propriété

Type: **chaîne**

### uri

URI (Uniform Resource Identifier) du document demandant l’autorisation.

Cette propriété est en lecture seule.

```js
var uri = deferredPermissionRequest.uri;
```

##### Valeur de propriété

Type: **chaîne**

## Configuration requise

|                                           |                                      |
|-------------------------------------------|--------------------------------------|
| <strong>Client minimal pris en charge</strong> | Windows 10 (applications du Windows Store uniquement) |
| <strong>Serveur minimal pris en charge</strong> |            Non pris en charge             |
| <strong>Téléphone minimum pris en charge</strong>  |            Non pris en charge             |
