---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2NavigationCompletedEventArgs
ms.openlocfilehash: d40ee75eb77e8de6eab1188e6c17edacce00f635
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879806"
---
# <span data-ttu-id="03f94-104">interface ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="03f94-104">interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="03f94-105">Arguments d’événement pour l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="03f94-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="03f94-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="03f94-106">Summary</span></span>

 <span data-ttu-id="03f94-107">Ses</span><span class="sxs-lookup"><span data-stu-id="03f94-107">Members</span></span>                        | <span data-ttu-id="03f94-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="03f94-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="03f94-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="03f94-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="03f94-110">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="03f94-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="03f94-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="03f94-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="03f94-112">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="03f94-112">The ID of the navigation.</span></span>
[<span data-ttu-id="03f94-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="03f94-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="03f94-114">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="03f94-114">The error code if the navigation failed.</span></span>

## <span data-ttu-id="03f94-115">Ses</span><span class="sxs-lookup"><span data-stu-id="03f94-115">Members</span></span>

#### <span data-ttu-id="03f94-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="03f94-116">get_IsSuccess</span></span> 

<span data-ttu-id="03f94-117">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="03f94-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="03f94-118">valeur publique HRESULT [get_IsSuccess](#get_issuccess)(bool \* propriétés IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="03f94-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="03f94-119">Il s’agit de la valeur false pour une navigation qui s’est produite dans une page d’erreur (échecs en raison d’un réseau, échec de recherche DNS, serveur HTTP répond avec 4xx), mais peut également avoir la valeur false pour des éléments supplémentaires tels que Window. Stop () appelé sur la page de navigation.</span><span class="sxs-lookup"><span data-stu-id="03f94-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="03f94-120">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="03f94-120">get_NavigationId</span></span> 

<span data-ttu-id="03f94-121">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="03f94-121">The ID of the navigation.</span></span>

> <span data-ttu-id="03f94-122">navigation_id [get_NavigationId](#get_navigationid)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="03f94-122">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="03f94-123">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="03f94-123">get_WebErrorStatus</span></span> 

<span data-ttu-id="03f94-124">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="03f94-124">The error code if the navigation failed.</span></span>

> <span data-ttu-id="03f94-125">[get_WebErrorStatus](#get_weberrorstatus)par le biais du public HRESULT (COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="03f94-125">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span></span>

