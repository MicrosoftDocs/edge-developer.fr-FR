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
# <a name="schema-domain---devtools-protocol-version-01-edgehtml"></a><span data-ttu-id="0aa5c-104">Domaine de schéma - DevTools Protocol Version 0.1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="0aa5c-104">Schema Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="0aa5c-105">Fournit des informations sur le schéma de protocole.</span><span class="sxs-lookup"><span data-stu-id="0aa5c-105">Provides information about the protocol schema.</span></span>  

| <span data-ttu-id="0aa5c-106">Classification</span><span class="sxs-lookup"><span data-stu-id="0aa5c-106">Classification</span></span> | <span data-ttu-id="0aa5c-107">Membres</span><span class="sxs-lookup"><span data-stu-id="0aa5c-107">Members</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="0aa5c-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0aa5c-108">Methods</span></span>](#methods) | [<span data-ttu-id="0aa5c-109">getDomains</span><span class="sxs-lookup"><span data-stu-id="0aa5c-109">getDomains</span></span>](#getdomains) |  
| [<span data-ttu-id="0aa5c-110">Types</span><span class="sxs-lookup"><span data-stu-id="0aa5c-110">Types</span></span>](#types) | [<span data-ttu-id="0aa5c-111">Domaine</span><span class="sxs-lookup"><span data-stu-id="0aa5c-111">Domain</span></span>](#domain) |  

## <a name="methods"></a><span data-ttu-id="0aa5c-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0aa5c-112">Methods</span></span>  

### <a name="getdomains"></a><span data-ttu-id="0aa5c-113">getDomains</span><span class="sxs-lookup"><span data-stu-id="0aa5c-113">getDomains</span></span>  

<span data-ttu-id="0aa5c-114">Renvoie les domaines pris en charge.</span><span class="sxs-lookup"><span data-stu-id="0aa5c-114">Returns supported domains.</span></span>  

| <span data-ttu-id="0aa5c-115">Renvoie</span><span class="sxs-lookup"><span data-stu-id="0aa5c-115">Returns</span></span> | <span data-ttu-id="0aa5c-116">Type</span><span class="sxs-lookup"><span data-stu-id="0aa5c-116">Type</span></span> | <span data-ttu-id="0aa5c-117">Détails</span><span class="sxs-lookup"><span data-stu-id="0aa5c-117">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0aa5c-118">domains</span><span class="sxs-lookup"><span data-stu-id="0aa5c-118">domains</span></span> | [<span data-ttu-id="0aa5c-119">Domaine[]</span><span class="sxs-lookup"><span data-stu-id="0aa5c-119">Domain[]</span></span>](#domain) | <span data-ttu-id="0aa5c-120">Liste des domaines pris en charge.</span><span class="sxs-lookup"><span data-stu-id="0aa5c-120">List of supported domains.</span></span> |  

---  

## <a name="types"></a><span data-ttu-id="0aa5c-121">Types</span><span class="sxs-lookup"><span data-stu-id="0aa5c-121">Types</span></span>  

### <a name="domain-object"></a><span data-ttu-id="0aa5c-122">Objet Domain</span><span class="sxs-lookup"><span data-stu-id="0aa5c-122">Domain object</span></span>  

<a name="domain"></a>  

<span data-ttu-id="0aa5c-123">Description du domaine de protocole.</span><span class="sxs-lookup"><span data-stu-id="0aa5c-123">Description of the protocol domain.</span></span>  

| <span data-ttu-id="0aa5c-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0aa5c-124">Properties</span></span> | <span data-ttu-id="0aa5c-125">Type</span><span class="sxs-lookup"><span data-stu-id="0aa5c-125">Type</span></span> | <span data-ttu-id="0aa5c-126">Détails</span><span class="sxs-lookup"><span data-stu-id="0aa5c-126">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0aa5c-127">name</span><span class="sxs-lookup"><span data-stu-id="0aa5c-127">name</span></span> | `string` | <span data-ttu-id="0aa5c-128">Nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="0aa5c-128">Domain name.</span></span> |  
| <span data-ttu-id="0aa5c-129">version</span><span class="sxs-lookup"><span data-stu-id="0aa5c-129">version</span></span> | `string` | <span data-ttu-id="0aa5c-130">Version du domaine.</span><span class="sxs-lookup"><span data-stu-id="0aa5c-130">Domain version.</span></span> |  

---  
