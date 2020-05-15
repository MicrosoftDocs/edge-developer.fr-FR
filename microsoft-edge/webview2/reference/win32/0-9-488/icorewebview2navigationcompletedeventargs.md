---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 21c78d88237e525f6e0ff8d9c604cd023209599c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653347"
---
# <span data-ttu-id="6b671-104">interface ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="6b671-104">interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="6b671-105">Arguments d’événement pour l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="6b671-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="6b671-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="6b671-106">Summary</span></span>

 <span data-ttu-id="6b671-107">Ses</span><span class="sxs-lookup"><span data-stu-id="6b671-107">Members</span></span>                        | <span data-ttu-id="6b671-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="6b671-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6b671-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="6b671-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="6b671-110">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="6b671-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="6b671-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="6b671-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="6b671-112">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="6b671-112">The ID of the navigation.</span></span>
[<span data-ttu-id="6b671-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="6b671-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="6b671-114">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="6b671-114">The error code if the navigation failed.</span></span>

## <span data-ttu-id="6b671-115">Ses</span><span class="sxs-lookup"><span data-stu-id="6b671-115">Members</span></span>

#### <span data-ttu-id="6b671-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="6b671-116">get_IsSuccess</span></span> 

<span data-ttu-id="6b671-117">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="6b671-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="6b671-118">valeur publique HRESULT [get_IsSuccess](#get_issuccess)(bool \* propriétés IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="6b671-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="6b671-119">Il s’agit de la valeur false pour une navigation qui s’est produite dans une page d’erreur (échecs en raison d’un réseau, échec de recherche DNS, serveur HTTP répond avec 4xx), mais peut également avoir la valeur false pour des éléments supplémentaires tels que Window. Stop () appelé sur la page de navigation.</span><span class="sxs-lookup"><span data-stu-id="6b671-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="6b671-120">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="6b671-120">get_NavigationId</span></span> 

<span data-ttu-id="6b671-121">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="6b671-121">The ID of the navigation.</span></span>

> <span data-ttu-id="6b671-122">navigation_id [get_NavigationId](#get_navigationid)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="6b671-122">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="6b671-123">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="6b671-123">get_WebErrorStatus</span></span> 

<span data-ttu-id="6b671-124">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="6b671-124">The error code if the navigation failed.</span></span>

> <span data-ttu-id="6b671-125">[get_WebErrorStatus](#get_weberrorstatus)par le biais du public HRESULT (COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="6b671-125">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span></span>

