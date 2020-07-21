---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: e2a9486011d5ef3ef480271ed32a7c8b586cf9bd
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885827"
---
# <span data-ttu-id="b7e28-104">0.8.355-interface IWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="b7e28-104">0.8.355 - interface IWebView2PermissionRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="b7e28-105">Arguments d’événement pour l’événement PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="b7e28-105">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="b7e28-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="b7e28-106">Summary</span></span>

 <span data-ttu-id="b7e28-107">Ses</span><span class="sxs-lookup"><span data-stu-id="b7e28-107">Members</span></span>                        | <span data-ttu-id="b7e28-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="b7e28-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b7e28-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="b7e28-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="b7e28-110">Origine du contenu Web qui demande l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="b7e28-110">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="b7e28-111">get_PermissionType</span><span class="sxs-lookup"><span data-stu-id="b7e28-111">get_PermissionType</span></span>](#get_permissiontype) | <span data-ttu-id="b7e28-112">Type de l’autorisation demandée.</span><span class="sxs-lookup"><span data-stu-id="b7e28-112">The type of the permission that is requested.</span></span>
[<span data-ttu-id="b7e28-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="b7e28-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="b7e28-114">True lors du déclenchement de la demande d’autorisation par le biais d’un mouvement utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b7e28-114">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="b7e28-115">get_State</span><span class="sxs-lookup"><span data-stu-id="b7e28-115">get_State</span></span>](#get_state) | <span data-ttu-id="b7e28-116">État d’une demande d’autorisation, c.-à-d.</span><span class="sxs-lookup"><span data-stu-id="b7e28-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="b7e28-117">put_State</span><span class="sxs-lookup"><span data-stu-id="b7e28-117">put_State</span></span>](#put_state) | <span data-ttu-id="b7e28-118">Définissez la propriété État.</span><span class="sxs-lookup"><span data-stu-id="b7e28-118">Set the State property.</span></span>
[<span data-ttu-id="b7e28-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="b7e28-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="b7e28-120">GetDeferral peut être appelé pour retourner un objet [IWebView2Deferral](IWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="b7e28-120">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="b7e28-121">Ses</span><span class="sxs-lookup"><span data-stu-id="b7e28-121">Members</span></span>

#### <span data-ttu-id="b7e28-122">get_Uri</span><span class="sxs-lookup"><span data-stu-id="b7e28-122">get_Uri</span></span> 

<span data-ttu-id="b7e28-123">Origine du contenu Web qui demande l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="b7e28-123">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="b7e28-124">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="b7e28-124">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="b7e28-125">get_PermissionType</span><span class="sxs-lookup"><span data-stu-id="b7e28-125">get_PermissionType</span></span> 

<span data-ttu-id="b7e28-126">Type de l’autorisation demandée.</span><span class="sxs-lookup"><span data-stu-id="b7e28-126">The type of the permission that is requested.</span></span>

> <span data-ttu-id="b7e28-127">valeur publique HRESULT [get_PermissionType](#get_permissiontype)(WEBVIEW2_PERMISSION_TYPE \* value)</span><span class="sxs-lookup"><span data-stu-id="b7e28-127">public HRESULT [get_PermissionType](#get_permissiontype)(WEBVIEW2_PERMISSION_TYPE \* value)</span></span>

#### <span data-ttu-id="b7e28-128">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="b7e28-128">get_IsUserInitiated</span></span> 

<span data-ttu-id="b7e28-129">True lors du déclenchement de la demande d’autorisation par le biais d’un mouvement utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b7e28-129">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="b7e28-130">valeur publique HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="b7e28-130">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="b7e28-131">Notez que le déclenchement par le biais d’un mouvement utilisateur ne signifie pas que l’utilisateur a accès à la ressource associée.</span><span class="sxs-lookup"><span data-stu-id="b7e28-131">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="b7e28-132">get_State</span><span class="sxs-lookup"><span data-stu-id="b7e28-132">get_State</span></span> 

<span data-ttu-id="b7e28-133">État d’une demande d’autorisation, c.-à-d.</span><span class="sxs-lookup"><span data-stu-id="b7e28-133">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="b7e28-134">valeur publique HRESULT [get_state](#get_state)(WEBVIEW2_PERMISSION_STATE \* value)</span><span class="sxs-lookup"><span data-stu-id="b7e28-134">public HRESULT [get_State](#get_state)(WEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="b7e28-135">l’octroi de la requête.</span><span class="sxs-lookup"><span data-stu-id="b7e28-135">whether the request is granted.</span></span> <span data-ttu-id="b7e28-136">La valeur par défaut est WEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="b7e28-136">Default value is WEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="b7e28-137">put_State</span><span class="sxs-lookup"><span data-stu-id="b7e28-137">put_State</span></span> 

<span data-ttu-id="b7e28-138">Définissez la propriété État.</span><span class="sxs-lookup"><span data-stu-id="b7e28-138">Set the State property.</span></span>

> <span data-ttu-id="b7e28-139">[put_State](#put_state)des valeurs HRESULT publiques (WEBVIEW2_PERMISSION_STATE valeur)</span><span class="sxs-lookup"><span data-stu-id="b7e28-139">public HRESULT [put_State](#put_state)(WEBVIEW2_PERMISSION_STATE value)</span></span>

#### <span data-ttu-id="b7e28-140">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="b7e28-140">GetDeferral</span></span> 

<span data-ttu-id="b7e28-141">GetDeferral peut être appelé pour retourner un objet [IWebView2Deferral](IWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="b7e28-141">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="b7e28-142">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="b7e28-142">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="b7e28-143">Un développeur peut utiliser l’objet de report pour prendre la décision d’autorisation ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="b7e28-143">Developer can use the deferral object to make the permission decision at a later time.</span></span>

