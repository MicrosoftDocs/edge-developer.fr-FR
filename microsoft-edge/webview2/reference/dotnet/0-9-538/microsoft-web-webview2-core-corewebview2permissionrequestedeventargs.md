---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 58d87d1815b81969c4424eacfcec26ffe425192e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698597"
---
# <span data-ttu-id="4bbd7-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="4bbd7-104">Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs class</span></span> 

<span data-ttu-id="4bbd7-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="4bbd7-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="4bbd7-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="4bbd7-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="4bbd7-107">Arguments d’événement pour l’événement PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="4bbd7-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="4bbd7-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="4bbd7-108">Summary</span></span>

 <span data-ttu-id="4bbd7-109">Ses</span><span class="sxs-lookup"><span data-stu-id="4bbd7-109">Members</span></span>                        | <span data-ttu-id="4bbd7-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="4bbd7-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4bbd7-111">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="4bbd7-111">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="4bbd7-112">True lors du déclenchement de la demande d’autorisation par le biais d’un mouvement utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4bbd7-112">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="4bbd7-113">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="4bbd7-113">PermissionKind</span></span>](#permissionkind) | <span data-ttu-id="4bbd7-114">Type de l’autorisation demandée.</span><span class="sxs-lookup"><span data-stu-id="4bbd7-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="4bbd7-115">État</span><span class="sxs-lookup"><span data-stu-id="4bbd7-115">State</span></span>](#state) | <span data-ttu-id="4bbd7-116">État d’une demande d’autorisation, c.-à-d.</span><span class="sxs-lookup"><span data-stu-id="4bbd7-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="4bbd7-117">URI</span><span class="sxs-lookup"><span data-stu-id="4bbd7-117">Uri</span></span>](#uri) | <span data-ttu-id="4bbd7-118">Origine du contenu Web qui demande l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="4bbd7-118">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="4bbd7-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="4bbd7-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="4bbd7-120">GetDeferral peut être appelé pour retourner un objet CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="4bbd7-120">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="4bbd7-121">Ses</span><span class="sxs-lookup"><span data-stu-id="4bbd7-121">Members</span></span>

#### <span data-ttu-id="4bbd7-122">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="4bbd7-122">IsUserInitiated</span></span> 

<span data-ttu-id="4bbd7-123">True lors du déclenchement de la demande d’autorisation par le biais d’un mouvement utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4bbd7-123">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="4bbd7-124">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="4bbd7-124">public bool [IsUserInitiated](#isuserinitiated)</span></span>

<span data-ttu-id="4bbd7-125">Notez que le déclenchement par le biais d’un mouvement utilisateur ne signifie pas que l’utilisateur a accès à la ressource associée.</span><span class="sxs-lookup"><span data-stu-id="4bbd7-125">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="4bbd7-126">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="4bbd7-126">PermissionKind</span></span> 

<span data-ttu-id="4bbd7-127">Type de l’autorisation demandée.</span><span class="sxs-lookup"><span data-stu-id="4bbd7-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="4bbd7-128">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span><span class="sxs-lookup"><span data-stu-id="4bbd7-128">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span></span>

#### <span data-ttu-id="4bbd7-129">État</span><span class="sxs-lookup"><span data-stu-id="4bbd7-129">State</span></span> 

<span data-ttu-id="4bbd7-130">État d’une demande d’autorisation, c.-à-d.</span><span class="sxs-lookup"><span data-stu-id="4bbd7-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="4bbd7-131">[État](#state) CoreWebView2PermissionState public</span><span class="sxs-lookup"><span data-stu-id="4bbd7-131">public CoreWebView2PermissionState [State](#state)</span></span>

<span data-ttu-id="4bbd7-132">l’octroi de la requête.</span><span class="sxs-lookup"><span data-stu-id="4bbd7-132">whether the request is granted.</span></span>

<span data-ttu-id="4bbd7-133">La valeur par défaut est CoreWebView2PermissionState. default.</span><span class="sxs-lookup"><span data-stu-id="4bbd7-133">Default value is CoreWebView2PermissionState.Default.</span></span>

#### <span data-ttu-id="4bbd7-134">URI</span><span class="sxs-lookup"><span data-stu-id="4bbd7-134">Uri</span></span> 

<span data-ttu-id="4bbd7-135">Origine du contenu Web qui demande l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="4bbd7-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="4bbd7-136">[URI](#uri) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="4bbd7-136">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="4bbd7-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="4bbd7-137">GetDeferral</span></span> 

<span data-ttu-id="4bbd7-138">GetDeferral peut être appelé pour retourner un objet CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="4bbd7-138">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="4bbd7-139">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="4bbd7-139">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="4bbd7-140">Un développeur peut utiliser l’objet de report pour prendre la décision d’autorisation ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="4bbd7-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>

