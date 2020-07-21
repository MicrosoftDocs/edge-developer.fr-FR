---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: e29765a4b8a3e620b8c627c7b05b9f0b4ff63f95
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886415"
---
# <span data-ttu-id="2cb12-104">0.9.430-interface ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2cb12-104">0.9.430 - interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="2cb12-105">Arguments d’événement pour l’événement PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="2cb12-105">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="2cb12-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="2cb12-106">Summary</span></span>

 <span data-ttu-id="2cb12-107">Ses</span><span class="sxs-lookup"><span data-stu-id="2cb12-107">Members</span></span>                        | <span data-ttu-id="2cb12-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="2cb12-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2cb12-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="2cb12-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="2cb12-110">Origine du contenu Web qui demande l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="2cb12-110">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="2cb12-111">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="2cb12-111">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="2cb12-112">Type de l’autorisation demandée.</span><span class="sxs-lookup"><span data-stu-id="2cb12-112">The type of the permission that is requested.</span></span>
[<span data-ttu-id="2cb12-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="2cb12-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="2cb12-114">True lors du déclenchement de la demande d’autorisation par le biais d’un mouvement utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2cb12-114">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="2cb12-115">get_State</span><span class="sxs-lookup"><span data-stu-id="2cb12-115">get_State</span></span>](#get_state) | <span data-ttu-id="2cb12-116">État d’une demande d’autorisation, c.-à-d.</span><span class="sxs-lookup"><span data-stu-id="2cb12-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="2cb12-117">put_State</span><span class="sxs-lookup"><span data-stu-id="2cb12-117">put_State</span></span>](#put_state) | <span data-ttu-id="2cb12-118">Définissez la propriété État.</span><span class="sxs-lookup"><span data-stu-id="2cb12-118">Set the State property.</span></span>
[<span data-ttu-id="2cb12-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2cb12-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="2cb12-120">GetDeferral peut être appelé pour retourner un objet [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="2cb12-120">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="2cb12-121">Ses</span><span class="sxs-lookup"><span data-stu-id="2cb12-121">Members</span></span>

#### <span data-ttu-id="2cb12-122">get_Uri</span><span class="sxs-lookup"><span data-stu-id="2cb12-122">get_Uri</span></span> 

<span data-ttu-id="2cb12-123">Origine du contenu Web qui demande l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="2cb12-123">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="2cb12-124">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="2cb12-124">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="2cb12-125">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="2cb12-125">get_PermissionKind</span></span> 

<span data-ttu-id="2cb12-126">Type de l’autorisation demandée.</span><span class="sxs-lookup"><span data-stu-id="2cb12-126">The type of the permission that is requested.</span></span>

> <span data-ttu-id="2cb12-127">valeur publique HRESULT [get_PermissionKind](#get_permissionkind)(CORE_WEBVIEW2_PERMISSION_KIND \* value)</span><span class="sxs-lookup"><span data-stu-id="2cb12-127">public HRESULT [get_PermissionKind](#get_permissionkind)(CORE_WEBVIEW2_PERMISSION_KIND \* value)</span></span>

#### <span data-ttu-id="2cb12-128">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="2cb12-128">get_IsUserInitiated</span></span> 

<span data-ttu-id="2cb12-129">True lors du déclenchement de la demande d’autorisation par le biais d’un mouvement utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2cb12-129">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="2cb12-130">valeur publique HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="2cb12-130">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="2cb12-131">Notez que le déclenchement par le biais d’un mouvement utilisateur ne signifie pas que l’utilisateur a accès à la ressource associée.</span><span class="sxs-lookup"><span data-stu-id="2cb12-131">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="2cb12-132">get_State</span><span class="sxs-lookup"><span data-stu-id="2cb12-132">get_State</span></span> 

<span data-ttu-id="2cb12-133">État d’une demande d’autorisation, c.-à-d.</span><span class="sxs-lookup"><span data-stu-id="2cb12-133">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="2cb12-134">valeur publique HRESULT [get_state](#get_state)(CORE_WEBVIEW2_PERMISSION_STATE \* value)</span><span class="sxs-lookup"><span data-stu-id="2cb12-134">public HRESULT [get_State](#get_state)(CORE_WEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="2cb12-135">l’octroi de la requête.</span><span class="sxs-lookup"><span data-stu-id="2cb12-135">whether the request is granted.</span></span> <span data-ttu-id="2cb12-136">La valeur par défaut est CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="2cb12-136">Default value is CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="2cb12-137">put_State</span><span class="sxs-lookup"><span data-stu-id="2cb12-137">put_State</span></span> 

<span data-ttu-id="2cb12-138">Définissez la propriété État.</span><span class="sxs-lookup"><span data-stu-id="2cb12-138">Set the State property.</span></span>

> <span data-ttu-id="2cb12-139">[put_State](#put_state)des valeurs HRESULT publiques (CORE_WEBVIEW2_PERMISSION_STATE valeur)</span><span class="sxs-lookup"><span data-stu-id="2cb12-139">public HRESULT [put_State](#put_state)(CORE_WEBVIEW2_PERMISSION_STATE value)</span></span>

#### <span data-ttu-id="2cb12-140">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2cb12-140">GetDeferral</span></span> 

<span data-ttu-id="2cb12-141">GetDeferral peut être appelé pour retourner un objet [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="2cb12-141">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="2cb12-142">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="2cb12-142">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="2cb12-143">Un développeur peut utiliser l’objet de report pour prendre la décision d’autorisation ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="2cb12-143">Developer can use the deferral object to make the permission decision at a later time.</span></span>

