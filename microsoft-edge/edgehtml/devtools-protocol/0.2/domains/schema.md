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
# <a name="schema-domain---devtools-protocol-version-02-edgehtml"></a><span data-ttu-id="7ed7f-104">Domaine de schéma - DevTools Protocol Version 0.2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="7ed7f-104">Schema Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="7ed7f-105">Fournit des informations sur le schéma de protocole.</span><span class="sxs-lookup"><span data-stu-id="7ed7f-105">Provides information about the protocol schema.</span></span>  

| <span data-ttu-id="7ed7f-106">Classification</span><span class="sxs-lookup"><span data-stu-id="7ed7f-106">Classification</span></span> | <span data-ttu-id="7ed7f-107">Membres</span><span class="sxs-lookup"><span data-stu-id="7ed7f-107">Members</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="7ed7f-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7ed7f-108">Methods</span></span>](#methods) | [<span data-ttu-id="7ed7f-109">getDomains</span><span class="sxs-lookup"><span data-stu-id="7ed7f-109">getDomains</span></span>](#getdomains) |  
| [<span data-ttu-id="7ed7f-110">Types</span><span class="sxs-lookup"><span data-stu-id="7ed7f-110">Types</span></span>](#types) | [<span data-ttu-id="7ed7f-111">Objet Domain</span><span class="sxs-lookup"><span data-stu-id="7ed7f-111">Domain object</span></span>](#domain) |  

## <a name="methods"></a><span data-ttu-id="7ed7f-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7ed7f-112">Methods</span></span>  

### <a name="getdomains"></a><span data-ttu-id="7ed7f-113">getDomains</span><span class="sxs-lookup"><span data-stu-id="7ed7f-113">getDomains</span></span>  

<span data-ttu-id="7ed7f-114">Renvoie les domaines pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7ed7f-114">Returns supported domains.</span></span>  

| <span data-ttu-id="7ed7f-115">Renvoie</span><span class="sxs-lookup"><span data-stu-id="7ed7f-115">Returns</span></span> | <span data-ttu-id="7ed7f-116">Type</span><span class="sxs-lookup"><span data-stu-id="7ed7f-116">Type</span></span> | <span data-ttu-id="7ed7f-117">Détails</span><span class="sxs-lookup"><span data-stu-id="7ed7f-117">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="7ed7f-118">domains</span><span class="sxs-lookup"><span data-stu-id="7ed7f-118">domains</span></span> | [<span data-ttu-id="7ed7f-119">Domaine[]</span><span class="sxs-lookup"><span data-stu-id="7ed7f-119">Domain[]</span></span>](#domain) | <span data-ttu-id="7ed7f-120">Liste des domaines pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7ed7f-120">List of supported domains.</span></span> |  

---  

## <a name="types"></a><span data-ttu-id="7ed7f-121">Types</span><span class="sxs-lookup"><span data-stu-id="7ed7f-121">Types</span></span>  

### <a name="domain-object"></a><span data-ttu-id="7ed7f-122">Objet Domain</span><span class="sxs-lookup"><span data-stu-id="7ed7f-122">Domain object</span></span>  

<a name="domain"></a>  

<span data-ttu-id="7ed7f-123">Description du domaine de protocole.</span><span class="sxs-lookup"><span data-stu-id="7ed7f-123">Description of the protocol domain.</span></span>  

| <span data-ttu-id="7ed7f-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7ed7f-124">Properties</span></span> | <span data-ttu-id="7ed7f-125">Type</span><span class="sxs-lookup"><span data-stu-id="7ed7f-125">Type</span></span> | <span data-ttu-id="7ed7f-126">Détails</span><span class="sxs-lookup"><span data-stu-id="7ed7f-126">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="7ed7f-127">name</span><span class="sxs-lookup"><span data-stu-id="7ed7f-127">name</span></span> | `string` | <span data-ttu-id="7ed7f-128">Nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="7ed7f-128">Domain name.</span></span> |  
| <span data-ttu-id="7ed7f-129">version</span><span class="sxs-lookup"><span data-stu-id="7ed7f-129">version</span></span> | `string` | <span data-ttu-id="7ed7f-130">Version du domaine.</span><span class="sxs-lookup"><span data-stu-id="7ed7f-130">Domain version.</span></span> |  

---  
