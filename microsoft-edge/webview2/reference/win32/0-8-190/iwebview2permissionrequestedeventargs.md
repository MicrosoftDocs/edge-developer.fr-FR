---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 92c08d199aa607dae9cc575955a1eb0bf016a9c0
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878329"
---
# <span data-ttu-id="2d0fd-104">0.8.355-interface IWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2d0fd-104">0.8.355 - interface IWebView2PermissionRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="2d0fd-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="2d0fd-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="2d0fd-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="2d0fd-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="2d0fd-107">Arguments d’événement pour l’événement PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="2d0fd-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="2d0fd-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="2d0fd-108">Summary</span></span>

 <span data-ttu-id="2d0fd-109">Ses</span><span class="sxs-lookup"><span data-stu-id="2d0fd-109">Members</span></span>                        | <span data-ttu-id="2d0fd-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="2d0fd-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2d0fd-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="2d0fd-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="2d0fd-112">Origine du contenu Web qui demande l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="2d0fd-112">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="2d0fd-113">get_PermissionType</span><span class="sxs-lookup"><span data-stu-id="2d0fd-113">get_PermissionType</span></span>](#get_permissiontype) | <span data-ttu-id="2d0fd-114">Type de l’autorisation demandée.</span><span class="sxs-lookup"><span data-stu-id="2d0fd-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="2d0fd-115">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="2d0fd-115">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="2d0fd-116">True lors du déclenchement de la demande d’autorisation par le biais d’un mouvement utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2d0fd-116">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="2d0fd-117">get_State</span><span class="sxs-lookup"><span data-stu-id="2d0fd-117">get_State</span></span>](#get_state) | <span data-ttu-id="2d0fd-118">État d’une demande d’autorisation, c.-à-d.</span><span class="sxs-lookup"><span data-stu-id="2d0fd-118">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="2d0fd-119">put_State</span><span class="sxs-lookup"><span data-stu-id="2d0fd-119">put_State</span></span>](#put_state) | <span data-ttu-id="2d0fd-120">Définissez la propriété État.</span><span class="sxs-lookup"><span data-stu-id="2d0fd-120">Set the State property.</span></span>
[<span data-ttu-id="2d0fd-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2d0fd-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="2d0fd-122">GetDeferral peut être appelé pour retourner un objet [IWebView2Deferral](IWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="2d0fd-122">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="2d0fd-123">Ses</span><span class="sxs-lookup"><span data-stu-id="2d0fd-123">Members</span></span>

#### <span data-ttu-id="2d0fd-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="2d0fd-124">get_Uri</span></span> 

<span data-ttu-id="2d0fd-125">Origine du contenu Web qui demande l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="2d0fd-125">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="2d0fd-126">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="2d0fd-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="2d0fd-127">get_PermissionType</span><span class="sxs-lookup"><span data-stu-id="2d0fd-127">get_PermissionType</span></span> 

<span data-ttu-id="2d0fd-128">Type de l’autorisation demandée.</span><span class="sxs-lookup"><span data-stu-id="2d0fd-128">The type of the permission that is requested.</span></span>

> <span data-ttu-id="2d0fd-129">valeur publique HRESULT [get_PermissionType](#get_permissiontype)(WEBVIEW2_PERMISSION_TYPE \* value)</span><span class="sxs-lookup"><span data-stu-id="2d0fd-129">public HRESULT [get_PermissionType](#get_permissiontype)(WEBVIEW2_PERMISSION_TYPE \* value)</span></span>

#### <span data-ttu-id="2d0fd-130">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="2d0fd-130">get_IsUserInitiated</span></span> 

<span data-ttu-id="2d0fd-131">True lors du déclenchement de la demande d’autorisation par le biais d’un mouvement utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2d0fd-131">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="2d0fd-132">valeur publique HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="2d0fd-132">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="2d0fd-133">Notez que le déclenchement par le biais d’un mouvement utilisateur ne signifie pas que l’utilisateur a accès à la ressource associée.</span><span class="sxs-lookup"><span data-stu-id="2d0fd-133">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="2d0fd-134">get_State</span><span class="sxs-lookup"><span data-stu-id="2d0fd-134">get_State</span></span> 

<span data-ttu-id="2d0fd-135">État d’une demande d’autorisation, c.-à-d.</span><span class="sxs-lookup"><span data-stu-id="2d0fd-135">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="2d0fd-136">valeur publique HRESULT [get_state](#get_state)(WEBVIEW2_PERMISSION_STATE \* value)</span><span class="sxs-lookup"><span data-stu-id="2d0fd-136">public HRESULT [get_State](#get_state)(WEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="2d0fd-137">l’octroi de la requête.</span><span class="sxs-lookup"><span data-stu-id="2d0fd-137">whether the request is granted.</span></span> <span data-ttu-id="2d0fd-138">La valeur par défaut est WEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="2d0fd-138">Default value is WEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="2d0fd-139">put_State</span><span class="sxs-lookup"><span data-stu-id="2d0fd-139">put_State</span></span> 

<span data-ttu-id="2d0fd-140">Définissez la propriété État.</span><span class="sxs-lookup"><span data-stu-id="2d0fd-140">Set the State property.</span></span>

> <span data-ttu-id="2d0fd-141">[put_State](#put_state)des valeurs HRESULT publiques (WEBVIEW2_PERMISSION_STATE valeur)</span><span class="sxs-lookup"><span data-stu-id="2d0fd-141">public HRESULT [put_State](#put_state)(WEBVIEW2_PERMISSION_STATE value)</span></span>

#### <span data-ttu-id="2d0fd-142">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2d0fd-142">GetDeferral</span></span> 

<span data-ttu-id="2d0fd-143">GetDeferral peut être appelé pour retourner un objet [IWebView2Deferral](IWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="2d0fd-143">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="2d0fd-144">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="2d0fd-144">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="2d0fd-145">Un développeur peut utiliser l’objet de report pour prendre la décision d’autorisation ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="2d0fd-145">Developer can use the deferral object to make the permission decision at a later time.</span></span>

