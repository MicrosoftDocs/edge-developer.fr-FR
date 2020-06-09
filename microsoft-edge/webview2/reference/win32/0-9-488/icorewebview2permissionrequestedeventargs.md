---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 3d88d4ee0a89b4690b47f67ee90756ebecdd1c78
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698189"
---
# <span data-ttu-id="56a4c-104">interface ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="56a4c-104">interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="56a4c-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="56a4c-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="56a4c-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="56a4c-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="56a4c-107">Arguments d’événement pour l’événement PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="56a4c-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="56a4c-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="56a4c-108">Summary</span></span>

 <span data-ttu-id="56a4c-109">Ses</span><span class="sxs-lookup"><span data-stu-id="56a4c-109">Members</span></span>                        | <span data-ttu-id="56a4c-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="56a4c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="56a4c-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="56a4c-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="56a4c-112">True lors du déclenchement de la demande d’autorisation par le biais d’un mouvement utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56a4c-112">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="56a4c-113">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="56a4c-113">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="56a4c-114">Type de l’autorisation demandée.</span><span class="sxs-lookup"><span data-stu-id="56a4c-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="56a4c-115">get_State</span><span class="sxs-lookup"><span data-stu-id="56a4c-115">get_State</span></span>](#get_state) | <span data-ttu-id="56a4c-116">État d’une demande d’autorisation, c.-à-d.</span><span class="sxs-lookup"><span data-stu-id="56a4c-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="56a4c-117">get_Uri</span><span class="sxs-lookup"><span data-stu-id="56a4c-117">get_Uri</span></span>](#get_uri) | <span data-ttu-id="56a4c-118">Origine du contenu Web qui demande l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="56a4c-118">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="56a4c-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="56a4c-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="56a4c-120">GetDeferral peut être appelé pour retourner un objet [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="56a4c-120">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="56a4c-121">put_State</span><span class="sxs-lookup"><span data-stu-id="56a4c-121">put_State</span></span>](#put_state) | <span data-ttu-id="56a4c-122">Définissez la propriété État.</span><span class="sxs-lookup"><span data-stu-id="56a4c-122">Set the State property.</span></span>

## <span data-ttu-id="56a4c-123">Ses</span><span class="sxs-lookup"><span data-stu-id="56a4c-123">Members</span></span>

#### <span data-ttu-id="56a4c-124">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="56a4c-124">get_IsUserInitiated</span></span> 

<span data-ttu-id="56a4c-125">True lors du déclenchement de la demande d’autorisation par le biais d’un mouvement utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56a4c-125">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="56a4c-126">valeur publique HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="56a4c-126">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="56a4c-127">Notez que le déclenchement par le biais d’un mouvement utilisateur ne signifie pas que l’utilisateur a accès à la ressource associée.</span><span class="sxs-lookup"><span data-stu-id="56a4c-127">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="56a4c-128">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="56a4c-128">get_PermissionKind</span></span> 

<span data-ttu-id="56a4c-129">Type de l’autorisation demandée.</span><span class="sxs-lookup"><span data-stu-id="56a4c-129">The type of the permission that is requested.</span></span>

> <span data-ttu-id="56a4c-130">valeur publique HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \* value)</span><span class="sxs-lookup"><span data-stu-id="56a4c-130">public HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \* value)</span></span>

#### <span data-ttu-id="56a4c-131">get_State</span><span class="sxs-lookup"><span data-stu-id="56a4c-131">get_State</span></span> 

<span data-ttu-id="56a4c-132">État d’une demande d’autorisation, c.-à-d.</span><span class="sxs-lookup"><span data-stu-id="56a4c-132">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="56a4c-133">valeur publique HRESULT [get_state](#get_state)(COREWEBVIEW2_PERMISSION_STATE \* value)</span><span class="sxs-lookup"><span data-stu-id="56a4c-133">public HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="56a4c-134">l’octroi de la requête.</span><span class="sxs-lookup"><span data-stu-id="56a4c-134">whether the request is granted.</span></span> <span data-ttu-id="56a4c-135">La valeur par défaut est COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="56a4c-135">Default value is COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="56a4c-136">get_Uri</span><span class="sxs-lookup"><span data-stu-id="56a4c-136">get_Uri</span></span> 

<span data-ttu-id="56a4c-137">Origine du contenu Web qui demande l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="56a4c-137">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="56a4c-138">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="56a4c-138">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="56a4c-139">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="56a4c-139">GetDeferral</span></span> 

<span data-ttu-id="56a4c-140">GetDeferral peut être appelé pour retourner un objet [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="56a4c-140">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="56a4c-141">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="56a4c-141">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="56a4c-142">Un développeur peut utiliser l’objet de report pour prendre la décision d’autorisation ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="56a4c-142">Developer can use the deferral object to make the permission decision at a later time.</span></span>

#### <span data-ttu-id="56a4c-143">put_State</span><span class="sxs-lookup"><span data-stu-id="56a4c-143">put_State</span></span> 

<span data-ttu-id="56a4c-144">Définissez la propriété État.</span><span class="sxs-lookup"><span data-stu-id="56a4c-144">Set the State property.</span></span>

> <span data-ttu-id="56a4c-145">[put_State](#put_state)des valeurs HRESULT publiques (COREWEBVIEW2_PERMISSION_STATE valeur)</span><span class="sxs-lookup"><span data-stu-id="56a4c-145">public HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE value)</span></span>

