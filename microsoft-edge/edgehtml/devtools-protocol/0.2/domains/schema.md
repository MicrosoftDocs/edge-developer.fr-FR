---
description: Référence du protocole DevTools version 0.2 (EdgeHTML) pour le domaine de schéma. Fournit des informations sur le schéma de protocole.
title: Domaine de schéma - DevTools Protocol Version 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6844939f452bc96980d6d67d4652adcc7c078c7a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398146"
---
# <a name="schema-domain---devtools-protocol-version-02-edgehtml"></a>Domaine de schéma - DevTools Protocol Version 0.2 (EdgeHTML)  

Fournit des informations sur le schéma de protocole.  

| Classification | Membres |  
|:--- |:--- |  
| [Méthodes](#methods) | [getDomains](#getdomains) |  
| [Types](#types) | [Objet Domain](#domain) |  

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
