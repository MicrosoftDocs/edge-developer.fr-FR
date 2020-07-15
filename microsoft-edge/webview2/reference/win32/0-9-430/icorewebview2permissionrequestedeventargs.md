---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 75f88a08f5a94df85a471658704fcd77a5926417
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877790"
---
# <span data-ttu-id="4f857-104">0.9.430-interface ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="4f857-104">0.9.430 - interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="4f857-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="4f857-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="4f857-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="4f857-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="4f857-107">Arguments d’événement pour l’événement PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="4f857-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="4f857-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="4f857-108">Summary</span></span>

 <span data-ttu-id="4f857-109">Ses</span><span class="sxs-lookup"><span data-stu-id="4f857-109">Members</span></span>                        | <span data-ttu-id="4f857-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="4f857-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4f857-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="4f857-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="4f857-112">Origine du contenu Web qui demande l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="4f857-112">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="4f857-113">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="4f857-113">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="4f857-114">Type de l’autorisation demandée.</span><span class="sxs-lookup"><span data-stu-id="4f857-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="4f857-115">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="4f857-115">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="4f857-116">True lors du déclenchement de la demande d’autorisation par le biais d’un mouvement utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4f857-116">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="4f857-117">get_State</span><span class="sxs-lookup"><span data-stu-id="4f857-117">get_State</span></span>](#get_state) | <span data-ttu-id="4f857-118">État d’une demande d’autorisation, c.-à-d.</span><span class="sxs-lookup"><span data-stu-id="4f857-118">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="4f857-119">put_State</span><span class="sxs-lookup"><span data-stu-id="4f857-119">put_State</span></span>](#put_state) | <span data-ttu-id="4f857-120">Définissez la propriété État.</span><span class="sxs-lookup"><span data-stu-id="4f857-120">Set the State property.</span></span>
[<span data-ttu-id="4f857-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="4f857-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="4f857-122">GetDeferral peut être appelé pour retourner un objet [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="4f857-122">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="4f857-123">Ses</span><span class="sxs-lookup"><span data-stu-id="4f857-123">Members</span></span>

#### <span data-ttu-id="4f857-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="4f857-124">get_Uri</span></span> 

<span data-ttu-id="4f857-125">Origine du contenu Web qui demande l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="4f857-125">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="4f857-126">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="4f857-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="4f857-127">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="4f857-127">get_PermissionKind</span></span> 

<span data-ttu-id="4f857-128">Type de l’autorisation demandée.</span><span class="sxs-lookup"><span data-stu-id="4f857-128">The type of the permission that is requested.</span></span>

> <span data-ttu-id="4f857-129">valeur publique HRESULT [get_PermissionKind](#get_permissionkind)(CORE_WEBVIEW2_PERMISSION_KIND \* value)</span><span class="sxs-lookup"><span data-stu-id="4f857-129">public HRESULT [get_PermissionKind](#get_permissionkind)(CORE_WEBVIEW2_PERMISSION_KIND \* value)</span></span>

#### <span data-ttu-id="4f857-130">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="4f857-130">get_IsUserInitiated</span></span> 

<span data-ttu-id="4f857-131">True lors du déclenchement de la demande d’autorisation par le biais d’un mouvement utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4f857-131">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="4f857-132">valeur publique HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="4f857-132">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="4f857-133">Notez que le déclenchement par le biais d’un mouvement utilisateur ne signifie pas que l’utilisateur a accès à la ressource associée.</span><span class="sxs-lookup"><span data-stu-id="4f857-133">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="4f857-134">get_State</span><span class="sxs-lookup"><span data-stu-id="4f857-134">get_State</span></span> 

<span data-ttu-id="4f857-135">État d’une demande d’autorisation, c.-à-d.</span><span class="sxs-lookup"><span data-stu-id="4f857-135">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="4f857-136">valeur publique HRESULT [get_state](#get_state)(CORE_WEBVIEW2_PERMISSION_STATE \* value)</span><span class="sxs-lookup"><span data-stu-id="4f857-136">public HRESULT [get_State](#get_state)(CORE_WEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="4f857-137">l’octroi de la requête.</span><span class="sxs-lookup"><span data-stu-id="4f857-137">whether the request is granted.</span></span> <span data-ttu-id="4f857-138">La valeur par défaut est CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="4f857-138">Default value is CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="4f857-139">put_State</span><span class="sxs-lookup"><span data-stu-id="4f857-139">put_State</span></span> 

<span data-ttu-id="4f857-140">Définissez la propriété État.</span><span class="sxs-lookup"><span data-stu-id="4f857-140">Set the State property.</span></span>

> <span data-ttu-id="4f857-141">[put_State](#put_state)des valeurs HRESULT publiques (CORE_WEBVIEW2_PERMISSION_STATE valeur)</span><span class="sxs-lookup"><span data-stu-id="4f857-141">public HRESULT [put_State](#put_state)(CORE_WEBVIEW2_PERMISSION_STATE value)</span></span>

#### <span data-ttu-id="4f857-142">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="4f857-142">GetDeferral</span></span> 

<span data-ttu-id="4f857-143">GetDeferral peut être appelé pour retourner un objet [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="4f857-143">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="4f857-144">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="4f857-144">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="4f857-145">Un développeur peut utiliser l’objet de report pour prendre la décision d’autorisation ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="4f857-145">Developer can use the deferral object to make the permission decision at a later time.</span></span>

