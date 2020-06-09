---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 743cd0fc6a1a9b21605dfa427273a7a457f806d7
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697608"
---
# <span data-ttu-id="f712c-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f712c-104">Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="f712c-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="f712c-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="f712c-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="f712c-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="f712c-107">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="f712c-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="f712c-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="f712c-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="f712c-109">Arguments d’événement pour l’événement PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="f712c-109">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="f712c-110">Résumé</span><span class="sxs-lookup"><span data-stu-id="f712c-110">Summary</span></span>

 <span data-ttu-id="f712c-111">Ses</span><span class="sxs-lookup"><span data-stu-id="f712c-111">Members</span></span>                        | <span data-ttu-id="f712c-112">Descriptions</span><span class="sxs-lookup"><span data-stu-id="f712c-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f712c-113">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="f712c-113">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="f712c-114">True lors du déclenchement de la demande d’autorisation par le biais d’un mouvement utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f712c-114">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="f712c-115">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="f712c-115">PermissionKind</span></span>](#permissionkind) | <span data-ttu-id="f712c-116">Type de l’autorisation demandée.</span><span class="sxs-lookup"><span data-stu-id="f712c-116">The type of the permission that is requested.</span></span>
[<span data-ttu-id="f712c-117">État</span><span class="sxs-lookup"><span data-stu-id="f712c-117">State</span></span>](#state) | <span data-ttu-id="f712c-118">État d’une demande d’autorisation, c.-à-d.</span><span class="sxs-lookup"><span data-stu-id="f712c-118">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="f712c-119">URI</span><span class="sxs-lookup"><span data-stu-id="f712c-119">Uri</span></span>](#uri) | <span data-ttu-id="f712c-120">Origine du contenu Web qui demande l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="f712c-120">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="f712c-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="f712c-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="f712c-122">GetDeferral peut être appelé pour retourner un objet CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="f712c-122">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="f712c-123">Ses</span><span class="sxs-lookup"><span data-stu-id="f712c-123">Members</span></span>

#### <span data-ttu-id="f712c-124">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="f712c-124">IsUserInitiated</span></span> 

<span data-ttu-id="f712c-125">True lors du déclenchement de la demande d’autorisation par le biais d’un mouvement utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f712c-125">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="f712c-126">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="f712c-126">public bool [IsUserInitiated](#isuserinitiated)</span></span>

<span data-ttu-id="f712c-127">Notez que le déclenchement par le biais d’un mouvement utilisateur ne signifie pas que l’utilisateur a accès à la ressource associée.</span><span class="sxs-lookup"><span data-stu-id="f712c-127">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="f712c-128">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="f712c-128">PermissionKind</span></span> 

<span data-ttu-id="f712c-129">Type de l’autorisation demandée.</span><span class="sxs-lookup"><span data-stu-id="f712c-129">The type of the permission that is requested.</span></span>

> <span data-ttu-id="f712c-130">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span><span class="sxs-lookup"><span data-stu-id="f712c-130">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span></span>

#### <span data-ttu-id="f712c-131">État</span><span class="sxs-lookup"><span data-stu-id="f712c-131">State</span></span> 

<span data-ttu-id="f712c-132">État d’une demande d’autorisation, c.-à-d.</span><span class="sxs-lookup"><span data-stu-id="f712c-132">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="f712c-133">[État](#state) CoreWebView2PermissionState public</span><span class="sxs-lookup"><span data-stu-id="f712c-133">public CoreWebView2PermissionState [State](#state)</span></span>

<span data-ttu-id="f712c-134">l’octroi de la requête.</span><span class="sxs-lookup"><span data-stu-id="f712c-134">whether the request is granted.</span></span>

<span data-ttu-id="f712c-135">La valeur par défaut est CoreWebView2PermissionState. default.</span><span class="sxs-lookup"><span data-stu-id="f712c-135">Default value is CoreWebView2PermissionState.Default.</span></span>

#### <span data-ttu-id="f712c-136">URI</span><span class="sxs-lookup"><span data-stu-id="f712c-136">Uri</span></span> 

<span data-ttu-id="f712c-137">Origine du contenu Web qui demande l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="f712c-137">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="f712c-138">[URI](#uri) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="f712c-138">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="f712c-139">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="f712c-139">GetDeferral</span></span> 

<span data-ttu-id="f712c-140">GetDeferral peut être appelé pour retourner un objet CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="f712c-140">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="f712c-141">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="f712c-141">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="f712c-142">Un développeur peut utiliser l’objet de report pour prendre la décision d’autorisation ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="f712c-142">Developer can use the deferral object to make the permission decision at a later time.</span></span>

