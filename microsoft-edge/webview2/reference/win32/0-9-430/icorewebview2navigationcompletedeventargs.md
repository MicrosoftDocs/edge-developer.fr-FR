---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 099a022fef47beca0e0163e6e0e070aa37520a06
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883727"
---
# <span data-ttu-id="65580-104">0.9.430-interface ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="65580-104">0.9.430 - interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="65580-105">Arguments d’événement pour l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="65580-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="65580-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="65580-106">Summary</span></span>

 <span data-ttu-id="65580-107">Ses</span><span class="sxs-lookup"><span data-stu-id="65580-107">Members</span></span>                        | <span data-ttu-id="65580-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="65580-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="65580-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="65580-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="65580-110">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="65580-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="65580-111">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="65580-111">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="65580-112">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="65580-112">The error code if the navigation failed.</span></span>
[<span data-ttu-id="65580-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="65580-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="65580-114">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="65580-114">The ID of the navigation.</span></span>

## <span data-ttu-id="65580-115">Ses</span><span class="sxs-lookup"><span data-stu-id="65580-115">Members</span></span>

#### <span data-ttu-id="65580-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="65580-116">get_IsSuccess</span></span> 

<span data-ttu-id="65580-117">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="65580-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="65580-118">valeur publique HRESULT [get_IsSuccess](#get_issuccess)(bool \* propriétés IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="65580-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="65580-119">Il s’agit de la valeur false pour une navigation qui s’est produite dans une page d’erreur (échecs en raison d’un réseau, échec de recherche DNS, serveur HTTP répond avec 4xx), mais peut également avoir la valeur false pour des éléments supplémentaires tels que Window. Stop () appelé sur la page de navigation.</span><span class="sxs-lookup"><span data-stu-id="65580-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="65580-120">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="65580-120">get_WebErrorStatus</span></span> 

<span data-ttu-id="65580-121">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="65580-121">The error code if the navigation failed.</span></span>

> <span data-ttu-id="65580-122">[get_WebErrorStatus](#get_weberrorstatus)par le biais du public HRESULT (CORE_WEBVIEW2_WEB_ERROR_STATUS \* CORE_WEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="65580-122">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(CORE_WEBVIEW2_WEB_ERROR_STATUS \* CORE_WEBVIEW2_WEB_ERROR_STATUS)</span></span>

#### <span data-ttu-id="65580-123">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="65580-123">get_NavigationId</span></span> 

<span data-ttu-id="65580-124">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="65580-124">The ID of the navigation.</span></span>

> <span data-ttu-id="65580-125">navigation_id [get_NavigationId](#get_navigationid)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="65580-125">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

