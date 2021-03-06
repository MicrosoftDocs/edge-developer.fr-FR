---
description: Référence du protocole DevTools Version 0.2 (EdgeHTML) pour le domaine de page. Les actions et événements liés à la page inspectée appartiennent au domaine de page.
title: Domaine de page - DevTools Protocol Version 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d969dd100164ace61445a4618174cfa943dcfd2b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398846"
---
# <a name="page-domain---devtools-protocol-version-02-edgehtml"></a>Domaine de page - DevTools Protocol Version 0.2 (EdgeHTML)  

Les actions et événements liés à la page inspectée appartiennent au domaine de page.  

| Classification | Membres |  
|:--- |:--- |  
| [Méthodes](#methods) | [activer,](#enable) [désactiver,](#disable) [naviguer,](#navigate) [getFrameTree](#getframetree) |  
| [Événements](#events) | [frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired) |  
| [Types](#types) | [FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree) |  

## <a name="methods"></a>Méthodes  

### <a name="enable"></a>activer  

Active les notifications de domaine de page.  

&nbsp;  

---  

### <a name="disable"></a>désactiver   

Désactive les notifications de domaine de page.  

&nbsp;  

---  

### <a name="navigate"></a>naviguer  

Navigue vers la page actuelle jusqu’à l’URL donnée.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| url | `string` | URL vers qui accéder à la page. |  
| frameId \(facultatif\) | [FrameId](#frameid) | ID d’image à parcourir.  S’il n’est pas spécifié, navigue vers la page supérieure. |  

| Renvoie | Type | Détails |  
|:--- |:--- |:--- |  
| frameId | [FrameId](#frameid) | ID d’image à parcourir. |  

---  

### <a name="getframetree"></a>getFrameTree  

Renvoie la structure de l’arborescence d’images présente.  

| Renvoie | Type | Détails |  
|:--- |:--- |:--- |  
| frameTree | [FrameTree](#frametree) | Structure d’arborescence de cadres présente. |  

---  

## <a name="events"></a>Événements  

### <a name="frameattached"></a>frameAttached  

Déclenché lorsque l’image a été attachée à son parent.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| frameId | [FrameId](#frameid) | ID du cadre attaché. |  
| parentFrameId | [FrameId](#frameid) | Identificateur d’image parent. |  
| stack \(optional\) | [Runtime.StackTrace](./runtime.md#stacktrace) | Suivi de la pile JavaScript du moment où l’image a été attachée, uniquement définie si l’image a été initiée à partir d’un script. |  

---  

### <a name="framedetached"></a>frameDetached  

Déclenché lorsque l’image a été détachée de son parent.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| frameId | [FrameId](#frameid) | ID du cadre qui a été détaché. |  

---  

### <a name="framenavigated"></a>frameNavigated  

Déclenché une fois la navigation de l’image terminée.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| frame | [Trame](#frame) | Objet Frame. |  

---  

### <a name="loadeventfired"></a>loadEventFired  

Correspond à `window.onload` l’événement.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| timestamp | `number` | Nombre de millisecondes depuis l’époque. |  

---  

### <a name="domcontenteventfired"></a>domContentEventFired  

Correspond à `document.onDOMContentLoaded` l’événement.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| timestamp | `number` | Nombre de millisecondes depuis l’époque. |  

---  

## <a name="types"></a>Types  

### <a name="frameid-string"></a>Chaîne FrameId  

<a name="frameid"></a>  

Identificateur d’image unique.  

&nbsp;  

---  

### <a name="frame-object"></a>Objet Frame  

<a name="frame"></a>  

Informations sur le cadre de la page.  

| Propriétés | Type | Détails |  
|:--- |:--- |:--- |  
| id | [FrameId](#frameid) | Identificateur unique de trame. |  
| parentId \(facultatif\) | [FrameId](#frameid) | Identificateur unique du cadre parent. |  
| name \(optional\) | `string` | Nom du cadre tel que spécifié dans la balise. |  
| url | `string` | URL du document frame. |  
| securityOrigin | `string` | Origine de la sécurité du document frame. |  
| mimeType | `string` | MimeType du document frame tel que déterminé par le navigateur. |  

---  

### <a name="frametree-object"></a>Objet FrameTree  

<a name="frametree"></a>  

Informations sur la hiérarchie frame.  

| Propriétés | Type | Détails |  
|:--- |:--- |:--- |  
| frame | [Trame](#frame) | Informations d’image pour cet élément d’arborescence. |  
| childFrames \(optional\) | [FrameTree[]](#frametree) | Images enfants. |  

---  
