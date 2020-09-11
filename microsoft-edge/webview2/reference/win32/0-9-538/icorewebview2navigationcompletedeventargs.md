---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2NavigationCompletedEventArgs
ms.openlocfilehash: 482137fd0ffa10c60381d5b0f3dc3d7db6f9fdf7
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011292"
---
# <span data-ttu-id="d8564-104">0.9.579-interface ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d8564-104">0.9.579 - interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="d8564-105">Arguments d’événement pour l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="d8564-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="d8564-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="d8564-106">Summary</span></span>

 <span data-ttu-id="d8564-107">Ses</span><span class="sxs-lookup"><span data-stu-id="d8564-107">Members</span></span>                        | <span data-ttu-id="d8564-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="d8564-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d8564-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="d8564-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="d8564-110">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="d8564-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="d8564-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="d8564-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="d8564-112">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="d8564-112">The ID of the navigation.</span></span>
[<span data-ttu-id="d8564-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="d8564-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="d8564-114">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="d8564-114">The error code if the navigation failed.</span></span>

## <span data-ttu-id="d8564-115">Ses</span><span class="sxs-lookup"><span data-stu-id="d8564-115">Members</span></span>

#### <span data-ttu-id="d8564-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="d8564-116">get_IsSuccess</span></span> 

<span data-ttu-id="d8564-117">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="d8564-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="d8564-118">valeur publique HRESULT [get_IsSuccess](#get_issuccess)(bool \* propriétés IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="d8564-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="d8564-119">Il s’agit de la valeur false pour une navigation qui s’est produite dans une page d’erreur (échecs en raison d’un réseau, échec de recherche DNS, serveur HTTP répond avec 4xx), mais peut également avoir la valeur false pour des éléments supplémentaires tels que Window. Stop () appelé sur la page de navigation.</span><span class="sxs-lookup"><span data-stu-id="d8564-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="d8564-120">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="d8564-120">get_NavigationId</span></span> 

<span data-ttu-id="d8564-121">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="d8564-121">The ID of the navigation.</span></span>

> <span data-ttu-id="d8564-122">navigation_id [get_NavigationId](#get_navigationid)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="d8564-122">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="d8564-123">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="d8564-123">get_WebErrorStatus</span></span> 

<span data-ttu-id="d8564-124">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="d8564-124">The error code if the navigation failed.</span></span>

> <span data-ttu-id="d8564-125">[get_WebErrorStatus](#get_weberrorstatus)par le biais du public HRESULT (COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="d8564-125">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span></span>

