---
description: Référence du protocole DevTools version 0.1 (EdgeHTML) pour le domaine de page. Les actions et événements liés à la page inspectée appartiennent au domaine de page.
title: Domaine de page - DevTools Protocol Version 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b04b0685a6b465d40e999a2a48d370573a3058d8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399147"
---
# <a name="page-domain---devtools-protocol-version-01-edgehtml"></a>Domaine de page - DevTools Protocol Version 0.1 (EdgeHTML)  

Les actions et événements liés à la page inspectée appartiennent au domaine de page.  

| Classification | Membres |  
|:--- |:--- |  
| [**Méthodes**](#methods) | [activer,](#enable) [désactiver,](#disable) [naviguer](#navigate) |  
| [**Types**](#types) | [FrameId](#frameid) |  

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

| Renvoie | Type | Détails |  
|:--- |:--- |:--- |  
| frameId | [FrameId](#frameid) | **Expérimental**.  ID d’image à parcourir. |  

---  

## <a name="types"></a>Types  

### <a name="frameid-string"></a>Chaîne FrameId  

<a name="frameid"></a>  

Identificateur d’image unique.  

&nbsp;  

---  
