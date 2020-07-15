---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
ms.openlocfilehash: ede6cef20a1a0f5fcd0780376b5ddec07bf05d26
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878798"
---
# <span data-ttu-id="c76d5-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="c76d5-104">Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs class</span></span> 

<span data-ttu-id="c76d5-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="c76d5-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="c76d5-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="c76d5-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="c76d5-107">Arguments d’événement pour l’événement PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="c76d5-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="c76d5-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="c76d5-108">Summary</span></span>

 <span data-ttu-id="c76d5-109">Ses</span><span class="sxs-lookup"><span data-stu-id="c76d5-109">Members</span></span>                        | <span data-ttu-id="c76d5-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="c76d5-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c76d5-111">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="c76d5-111">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="c76d5-112">True lors du déclenchement de la demande d’autorisation par le biais d’un mouvement utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c76d5-112">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="c76d5-113">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="c76d5-113">PermissionKind</span></span>](#permissionkind) | <span data-ttu-id="c76d5-114">Type de l’autorisation demandée.</span><span class="sxs-lookup"><span data-stu-id="c76d5-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="c76d5-115">État</span><span class="sxs-lookup"><span data-stu-id="c76d5-115">State</span></span>](#state) | <span data-ttu-id="c76d5-116">État d’une demande d’autorisation, c.-à-d.</span><span class="sxs-lookup"><span data-stu-id="c76d5-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="c76d5-117">URI</span><span class="sxs-lookup"><span data-stu-id="c76d5-117">Uri</span></span>](#uri) | <span data-ttu-id="c76d5-118">Origine du contenu Web qui demande l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="c76d5-118">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="c76d5-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="c76d5-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="c76d5-120">GetDeferral peut être appelé pour retourner un objet CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="c76d5-120">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="c76d5-121">Ses</span><span class="sxs-lookup"><span data-stu-id="c76d5-121">Members</span></span>

#### <span data-ttu-id="c76d5-122">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="c76d5-122">IsUserInitiated</span></span> 

<span data-ttu-id="c76d5-123">True lors du déclenchement de la demande d’autorisation par le biais d’un mouvement utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c76d5-123">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="c76d5-124">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="c76d5-124">public bool [IsUserInitiated](#isuserinitiated)</span></span>

<span data-ttu-id="c76d5-125">Notez que le déclenchement par le biais d’un mouvement utilisateur ne signifie pas que l’utilisateur a accès à la ressource associée.</span><span class="sxs-lookup"><span data-stu-id="c76d5-125">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="c76d5-126">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="c76d5-126">PermissionKind</span></span> 

<span data-ttu-id="c76d5-127">Type de l’autorisation demandée.</span><span class="sxs-lookup"><span data-stu-id="c76d5-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="c76d5-128">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span><span class="sxs-lookup"><span data-stu-id="c76d5-128">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span></span>

#### <span data-ttu-id="c76d5-129">État</span><span class="sxs-lookup"><span data-stu-id="c76d5-129">State</span></span> 

<span data-ttu-id="c76d5-130">État d’une demande d’autorisation, c.-à-d.</span><span class="sxs-lookup"><span data-stu-id="c76d5-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="c76d5-131">[État](#state) CoreWebView2PermissionState public</span><span class="sxs-lookup"><span data-stu-id="c76d5-131">public CoreWebView2PermissionState [State](#state)</span></span>

<span data-ttu-id="c76d5-132">l’octroi de la requête.</span><span class="sxs-lookup"><span data-stu-id="c76d5-132">whether the request is granted.</span></span>

<span data-ttu-id="c76d5-133">La valeur par défaut est CoreWebView2PermissionState. default.</span><span class="sxs-lookup"><span data-stu-id="c76d5-133">Default value is CoreWebView2PermissionState.Default.</span></span>

#### <span data-ttu-id="c76d5-134">URI</span><span class="sxs-lookup"><span data-stu-id="c76d5-134">Uri</span></span> 

<span data-ttu-id="c76d5-135">Origine du contenu Web qui demande l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="c76d5-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="c76d5-136">[URI](#uri) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="c76d5-136">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="c76d5-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="c76d5-137">GetDeferral</span></span> 

<span data-ttu-id="c76d5-138">GetDeferral peut être appelé pour retourner un objet CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="c76d5-138">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="c76d5-139">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="c76d5-139">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="c76d5-140">Un développeur peut utiliser l’objet de report pour prendre la décision d’autorisation ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="c76d5-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>

