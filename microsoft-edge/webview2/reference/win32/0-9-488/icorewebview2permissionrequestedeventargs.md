---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 85cba958c5c918bb99f14cb7202c7645b0ae6c52
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885204"
---
# <span data-ttu-id="587b4-104">0.9.515-interface ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="587b4-104">0.9.515 - interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="587b4-105">Arguments d’événement pour l’événement PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="587b4-105">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="587b4-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="587b4-106">Summary</span></span>

 <span data-ttu-id="587b4-107">Ses</span><span class="sxs-lookup"><span data-stu-id="587b4-107">Members</span></span>                        | <span data-ttu-id="587b4-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="587b4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="587b4-109">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="587b4-109">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="587b4-110">True lors du déclenchement de la demande d’autorisation par le biais d’un mouvement utilisateur.</span><span class="sxs-lookup"><span data-stu-id="587b4-110">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="587b4-111">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="587b4-111">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="587b4-112">Type de l’autorisation demandée.</span><span class="sxs-lookup"><span data-stu-id="587b4-112">The type of the permission that is requested.</span></span>
[<span data-ttu-id="587b4-113">get_State</span><span class="sxs-lookup"><span data-stu-id="587b4-113">get_State</span></span>](#get_state) | <span data-ttu-id="587b4-114">État d’une demande d’autorisation, c.-à-d.</span><span class="sxs-lookup"><span data-stu-id="587b4-114">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="587b4-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="587b4-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="587b4-116">Origine du contenu Web qui demande l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="587b4-116">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="587b4-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="587b4-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="587b4-118">GetDeferral peut être appelé pour retourner un objet [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="587b4-118">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="587b4-119">put_State</span><span class="sxs-lookup"><span data-stu-id="587b4-119">put_State</span></span>](#put_state) | <span data-ttu-id="587b4-120">Définissez la propriété État.</span><span class="sxs-lookup"><span data-stu-id="587b4-120">Set the State property.</span></span>

## <span data-ttu-id="587b4-121">Ses</span><span class="sxs-lookup"><span data-stu-id="587b4-121">Members</span></span>

#### <span data-ttu-id="587b4-122">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="587b4-122">get_IsUserInitiated</span></span> 

<span data-ttu-id="587b4-123">True lors du déclenchement de la demande d’autorisation par le biais d’un mouvement utilisateur.</span><span class="sxs-lookup"><span data-stu-id="587b4-123">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="587b4-124">valeur publique HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="587b4-124">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="587b4-125">Notez que le déclenchement par le biais d’un mouvement utilisateur ne signifie pas que l’utilisateur a accès à la ressource associée.</span><span class="sxs-lookup"><span data-stu-id="587b4-125">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="587b4-126">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="587b4-126">get_PermissionKind</span></span> 

<span data-ttu-id="587b4-127">Type de l’autorisation demandée.</span><span class="sxs-lookup"><span data-stu-id="587b4-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="587b4-128">valeur publique HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \* value)</span><span class="sxs-lookup"><span data-stu-id="587b4-128">public HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \* value)</span></span>

#### <span data-ttu-id="587b4-129">get_State</span><span class="sxs-lookup"><span data-stu-id="587b4-129">get_State</span></span> 

<span data-ttu-id="587b4-130">État d’une demande d’autorisation, c.-à-d.</span><span class="sxs-lookup"><span data-stu-id="587b4-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="587b4-131">valeur publique HRESULT [get_state](#get_state)(COREWEBVIEW2_PERMISSION_STATE \* value)</span><span class="sxs-lookup"><span data-stu-id="587b4-131">public HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="587b4-132">l’octroi de la requête.</span><span class="sxs-lookup"><span data-stu-id="587b4-132">whether the request is granted.</span></span> <span data-ttu-id="587b4-133">La valeur par défaut est COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="587b4-133">Default value is COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="587b4-134">get_Uri</span><span class="sxs-lookup"><span data-stu-id="587b4-134">get_Uri</span></span> 

<span data-ttu-id="587b4-135">Origine du contenu Web qui demande l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="587b4-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="587b4-136">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="587b4-136">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="587b4-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="587b4-137">GetDeferral</span></span> 

<span data-ttu-id="587b4-138">GetDeferral peut être appelé pour retourner un objet [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="587b4-138">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="587b4-139">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="587b4-139">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="587b4-140">Un développeur peut utiliser l’objet de report pour prendre la décision d’autorisation ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="587b4-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>

#### <span data-ttu-id="587b4-141">put_State</span><span class="sxs-lookup"><span data-stu-id="587b4-141">put_State</span></span> 

<span data-ttu-id="587b4-142">Définissez la propriété État.</span><span class="sxs-lookup"><span data-stu-id="587b4-142">Set the State property.</span></span>

> <span data-ttu-id="587b4-143">[put_State](#put_state)des valeurs HRESULT publiques (COREWEBVIEW2_PERMISSION_STATE valeur)</span><span class="sxs-lookup"><span data-stu-id="587b4-143">public HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE value)</span></span>

