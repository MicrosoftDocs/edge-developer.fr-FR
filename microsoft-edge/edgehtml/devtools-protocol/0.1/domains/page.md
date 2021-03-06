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
# <a name="page-domain---devtools-protocol-version-01-edgehtml"></a><span data-ttu-id="e6547-104">Domaine de page - DevTools Protocol Version 0.1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="e6547-104">Page Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="e6547-105">Les actions et événements liés à la page inspectée appartiennent au domaine de page.</span><span class="sxs-lookup"><span data-stu-id="e6547-105">Actions and events related to the inspected page belong to the page domain.</span></span>  

| <span data-ttu-id="e6547-106">Classification</span><span class="sxs-lookup"><span data-stu-id="e6547-106">Classification</span></span> | <span data-ttu-id="e6547-107">Membres</span><span class="sxs-lookup"><span data-stu-id="e6547-107">Members</span></span> |  
|:--- |:--- |  
| [**<span data-ttu-id="e6547-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e6547-108">Methods</span></span>**](#methods) | <span data-ttu-id="e6547-109">[activer,](#enable) [désactiver,](#disable) [naviguer](#navigate)</span><span class="sxs-lookup"><span data-stu-id="e6547-109">[enable](#enable), [disable](#disable), [navigate](#navigate)</span></span> |  
| [**<span data-ttu-id="e6547-110">Types</span><span class="sxs-lookup"><span data-stu-id="e6547-110">Types</span></span>**](#types) | [<span data-ttu-id="e6547-111">FrameId</span><span class="sxs-lookup"><span data-stu-id="e6547-111">FrameId</span></span>](#frameid) |  

## <a name="methods"></a><span data-ttu-id="e6547-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e6547-112">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="e6547-113">activer</span><span class="sxs-lookup"><span data-stu-id="e6547-113">enable</span></span>  

<span data-ttu-id="e6547-114">Active les notifications de domaine de page.</span><span class="sxs-lookup"><span data-stu-id="e6547-114">Enables page domain notifications.</span></span>  

&nbsp;  

---  

### <a name="disable"></a><span data-ttu-id="e6547-115">désactiver </span><span class="sxs-lookup"><span data-stu-id="e6547-115">disable</span></span>  

<span data-ttu-id="e6547-116">Désactive les notifications de domaine de page.</span><span class="sxs-lookup"><span data-stu-id="e6547-116">Disables page domain notifications.</span></span>  

&nbsp;  

---  

### <a name="navigate"></a><span data-ttu-id="e6547-117">naviguer</span><span class="sxs-lookup"><span data-stu-id="e6547-117">navigate</span></span>  

<span data-ttu-id="e6547-118">Navigue vers la page actuelle jusqu’à l’URL donnée.</span><span class="sxs-lookup"><span data-stu-id="e6547-118">Navigates current page to the given URL.</span></span>  

| <span data-ttu-id="e6547-119">Parameters</span><span class="sxs-lookup"><span data-stu-id="e6547-119">Parameters</span></span> | <span data-ttu-id="e6547-120">Type</span><span class="sxs-lookup"><span data-stu-id="e6547-120">Type</span></span> | <span data-ttu-id="e6547-121">Détails</span><span class="sxs-lookup"><span data-stu-id="e6547-121">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e6547-122">url</span><span class="sxs-lookup"><span data-stu-id="e6547-122">url</span></span> | `string` | <span data-ttu-id="e6547-123">URL vers qui accéder à la page.</span><span class="sxs-lookup"><span data-stu-id="e6547-123">URL to navigate the page to.</span></span> |  

| <span data-ttu-id="e6547-124">Renvoie</span><span class="sxs-lookup"><span data-stu-id="e6547-124">Returns</span></span> | <span data-ttu-id="e6547-125">Type</span><span class="sxs-lookup"><span data-stu-id="e6547-125">Type</span></span> | <span data-ttu-id="e6547-126">Détails</span><span class="sxs-lookup"><span data-stu-id="e6547-126">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e6547-127">frameId</span><span class="sxs-lookup"><span data-stu-id="e6547-127">frameId</span></span> | [<span data-ttu-id="e6547-128">FrameId</span><span class="sxs-lookup"><span data-stu-id="e6547-128">FrameId</span></span>](#frameid) | <span data-ttu-id="e6547-129">**Expérimental**.</span><span class="sxs-lookup"><span data-stu-id="e6547-129">**Experimental**.</span></span>  <span data-ttu-id="e6547-130">ID d’image à parcourir.</span><span class="sxs-lookup"><span data-stu-id="e6547-130">Frame ID that will be navigated.</span></span> |  

---  

## <a name="types"></a><span data-ttu-id="e6547-131">Types</span><span class="sxs-lookup"><span data-stu-id="e6547-131">Types</span></span>  

### <a name="frameid-string"></a><span data-ttu-id="e6547-132">Chaîne FrameId</span><span class="sxs-lookup"><span data-stu-id="e6547-132">FrameId string</span></span>  

<a name="frameid"></a>  

<span data-ttu-id="e6547-133">Identificateur d’image unique.</span><span class="sxs-lookup"><span data-stu-id="e6547-133">Unique frame identifier.</span></span>  

&nbsp;  

---  
