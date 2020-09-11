---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
ms.openlocfilehash: 87993559d4d70daef84cbd86a2305f09cc017aa9
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011865"
---
# <span data-ttu-id="a0ff2-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a0ff2-104">Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs class</span></span> 

<span data-ttu-id="a0ff2-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="a0ff2-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="a0ff2-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="a0ff2-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="a0ff2-107">Arguments d’événement pour l’événement PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="a0ff2-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="a0ff2-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="a0ff2-108">Summary</span></span>

 <span data-ttu-id="a0ff2-109">Ses</span><span class="sxs-lookup"><span data-stu-id="a0ff2-109">Members</span></span>                        | <span data-ttu-id="a0ff2-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="a0ff2-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a0ff2-111">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="a0ff2-111">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="a0ff2-112">True lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.</span><span class="sxs-lookup"><span data-stu-id="a0ff2-112">True when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="a0ff2-113">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="a0ff2-113">PermissionKind</span></span>](#permissionkind) | <span data-ttu-id="a0ff2-114">Type de l’autorisation demandée.</span><span class="sxs-lookup"><span data-stu-id="a0ff2-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="a0ff2-115">État</span><span class="sxs-lookup"><span data-stu-id="a0ff2-115">State</span></span>](#state) | <span data-ttu-id="a0ff2-116">État d’une demande d’autorisation, c.-à-d.</span><span class="sxs-lookup"><span data-stu-id="a0ff2-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="a0ff2-117">URI</span><span class="sxs-lookup"><span data-stu-id="a0ff2-117">Uri</span></span>](#uri) | <span data-ttu-id="a0ff2-118">Origine du contenu Web qui demande l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="a0ff2-118">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="a0ff2-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="a0ff2-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="a0ff2-120">GetDeferral peut être appelé pour retourner un objet CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="a0ff2-120">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="a0ff2-121">Ses</span><span class="sxs-lookup"><span data-stu-id="a0ff2-121">Members</span></span>

#### <span data-ttu-id="a0ff2-122">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="a0ff2-122">IsUserInitiated</span></span> 

<span data-ttu-id="a0ff2-123">True lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.</span><span class="sxs-lookup"><span data-stu-id="a0ff2-123">True when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="a0ff2-124">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="a0ff2-124">public bool [IsUserInitiated](#isuserinitiated)</span></span>

<span data-ttu-id="a0ff2-125">Le bloqueur de fenêtres contextuelles Edge est désactivé pour WebView de sorte que l’application puisse utiliser cet indicateur pour bloquer les fenêtres contextuelles non-utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a0ff2-125">The Edge popup blocker is disabled for WebView so the app can use this flag to block non-user initiated popups.</span></span>

#### <span data-ttu-id="a0ff2-126">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="a0ff2-126">PermissionKind</span></span> 

<span data-ttu-id="a0ff2-127">Type de l’autorisation demandée.</span><span class="sxs-lookup"><span data-stu-id="a0ff2-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="a0ff2-128">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span><span class="sxs-lookup"><span data-stu-id="a0ff2-128">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span></span>

#### <span data-ttu-id="a0ff2-129">État</span><span class="sxs-lookup"><span data-stu-id="a0ff2-129">State</span></span> 

<span data-ttu-id="a0ff2-130">État d’une demande d’autorisation, c.-à-d.</span><span class="sxs-lookup"><span data-stu-id="a0ff2-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="a0ff2-131">[État](#state) CoreWebView2PermissionState public</span><span class="sxs-lookup"><span data-stu-id="a0ff2-131">public CoreWebView2PermissionState [State](#state)</span></span>

<span data-ttu-id="a0ff2-132">l’octroi de la requête.</span><span class="sxs-lookup"><span data-stu-id="a0ff2-132">whether the request is granted.</span></span>

<span data-ttu-id="a0ff2-133">La valeur par défaut est CoreWebView2PermissionState. default.</span><span class="sxs-lookup"><span data-stu-id="a0ff2-133">Default value is CoreWebView2PermissionState.Default.</span></span>

#### <span data-ttu-id="a0ff2-134">URI</span><span class="sxs-lookup"><span data-stu-id="a0ff2-134">Uri</span></span> 

<span data-ttu-id="a0ff2-135">Origine du contenu Web qui demande l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="a0ff2-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="a0ff2-136">[URI](#uri) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="a0ff2-136">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="a0ff2-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="a0ff2-137">GetDeferral</span></span> 

<span data-ttu-id="a0ff2-138">GetDeferral peut être appelé pour retourner un objet CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="a0ff2-138">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="a0ff2-139">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="a0ff2-139">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="a0ff2-140">Un développeur peut utiliser l’objet de report pour prendre la décision d’autorisation ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="a0ff2-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>

