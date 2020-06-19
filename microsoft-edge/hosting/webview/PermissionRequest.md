---
description: Fournit des informations sur une demande d’autorisation.
title: Objet PermissionRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: c769bf122c3ca116d5783b73d0ff4f183d2cd52d
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752115"
---
# Objet PermissionRequest  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Fournit des informations sur une demande d’autorisation. Cet objet est disponible à partir de la propriété permissionRequest des arguments d’événement à partir de l’événement WebView [MSWebViewPermissionRequested](../webview.md#mswebviewpermissionrequested) .  

```javascript
webview.addEventListener("MSWebViewPermissionRequested", permissionRequestedEventArgs => {
    const permissionRequest = permissionRequestedEventArgs.permissionRequest;
    switch (permissionRequest.type) {
        case "geolocation":
        case "media":
        case "pointerlock":
        case "webnotifications":
        case "screen":
        case "immersiveview":
            if (permissionRequest.uri.startsWith("https://www.example.com/")) {
                // Implicitly trust particular URI
                permissionRequest.allow();
            }
            else if (permissionRequest.uri.startsWith("https://")) {
                // Defer the request so we can ask the user to allow or deny the request
                permissionRequest.defer();
                // Later we'll need to use webview.getDeferredPermissionRequestById for this
                // request and call allow or deny.
                promptUserForDeferredPermissionRequest(
                    permissionRequest.id,
                    permissionRequest.uri,
                    permissionRequest.type);
            }
            else {
                // Implicitly deny non-https URIs
                permissionRequest.deny();
            }
            break;

        case "unlimitedIndexedDBQuota":
        default:
            permissionRequest.deny();
            break;
    }
});
```  

## Méthodes  

### verte  

Autorise la demande d’autorisation.  

#### Parameters  

Cette méthode n’a aucun paramètre.  

#### Valeur renvoyée  

Cette méthode ne renvoie pas de valeur.  

### différer  

Si, au lieu de autoriser ou non une PermissionRequest de manière synchrone, vous avez besoin d’un temps pour interagir avec l’utilisateur ou effectuer une autre action asynchrone, appeler différer () sur le PermissionRequest.  Le PermissionRequest sera désormais disponible en tant que DeferredPermissionRequest à partir de getDeferredPermissionRequests et d’getDeferredPermissionRequestById.  Vous pouvez mettre en corrélation le PermissionRequest actif avec le DeferredPermissionRequest correspondant par le biais de la propriété ID correspondante.  

#### Parameters  

Cette méthode n’a aucun paramètre.  

#### Valeur renvoyée  

Cette méthode ne renvoie pas de valeur.  

### deny  

Refuse la demande d’autorisation.  

#### Parameters  

Cette méthode n’a aucun paramètre.  

#### Valeur renvoyée  

Cette méthode ne renvoie pas de valeur.  

## Propriétés  

### id  

ID unique qui peut être utilisé pour mettre en corrélation le PermissionRequest en cours avec un DeferredPermissionRequest correspondant si la méthode defer est utilisée.  Voir la méthode defer.  

Cette propriété est en lecture seule.  

##### Valeur de propriété  

Type: **longue non signée**  

### traité  

Renvoie «Unknown», «Defer», «Allow» ou «Deny» pour indiquer l’état actuel de la demande d’autorisation.  La chaîne d’état correspond à la méthode Allow, Deny ou différ appelée Last ou «Unknown» si aucune des méthodes n’a été appelée.  

Cette propriété est en lecture seule.  

#### Valeur de propriété  

Type: **chaîne**  

### type  

Type d’autorisation demandée. Il s’agit de l’une des valeurs de chaîne suivantes:  

*   **géolocalisation**: accès aux données d’emplacement par le biais de Navigator. géolocalisation.  
*   **unlimitedIndexedDBQuota**: autoriser les API IndexedDB à ignorer la limite de taille des données stockées habituellement.  
*   **média**: accès au microphone et à la caméra par le biais de Navigator. getUserMedia.  
*   **pointerlock**: possibilité de verrouiller et de contrôler le pointeur de la souris via l’élément. requestPointerLock.  
*   **webnotifications**: possibilité d’afficher les notifications sur le bureau via une fenêtre. Message.  
*   **écran**: possibilité de prendre des captures d’écran à l’aide de l’API de capture multimédia.  
*   **immersiveview**: possibilité de contrôler un affichage VR.  

Cette propriété est en lecture seule.  

#### Valeur de propriété  

Type: **chaîne**  

### uri  

URI (Uniform Resource Identifier) du document demandant l’autorisation.  

Cette propriété est en lecture seule.  

#### Valeur de propriété  

Type: **chaîne**  
