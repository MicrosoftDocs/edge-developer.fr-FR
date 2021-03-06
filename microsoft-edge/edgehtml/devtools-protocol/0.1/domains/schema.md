---
description: Référence du protocole DevTools version 0.1 (EdgeHTML) pour le domaine de schéma. Fournit des informations sur le schéma de protocole.
title: Domaine de schéma - DevTools Protocol Version 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e89f4269b4984ee49e83a23fcab9679485c49040
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398860"
---
# <a name="schema-domain---devtools-protocol-version-01-edgehtml"></a>Domaine de schéma - DevTools Protocol Version 0.1 (EdgeHTML)  

Fournit des informations sur le schéma de protocole.  

| Classification | Membres |  
|:--- |:--- |  
| [Méthodes](#methods) | [getDomains](#getdomains) |  
| [Types](#types) | [Domaine](#domain) |  

## <a name="methods"></a>Méthodes  

### <a name="getdomains"></a>getDomains  

Renvoie les domaines pris en charge.  

| Renvoie | Type | Détails |  
|:--- |:--- |:--- |  
| domains | [Domaine[]](#domain) | Liste des domaines pris en charge. |  

---  

## <a name="types"></a>Types  

### <a name="domain-object"></a>Objet Domain  

<a name="domain"></a>  

Description du domaine de protocole.  

| Propriétés | Type | Détails |  
|:--- |:--- |:--- |  
| name | `string` | Nom de domaine. |  
| version | `string` | Version du domaine. |  

---  
