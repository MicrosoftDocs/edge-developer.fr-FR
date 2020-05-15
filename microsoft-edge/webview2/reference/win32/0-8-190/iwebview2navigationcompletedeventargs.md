---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: fa1debd3b212492eea03e4ecf6e5daff5751f89b
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653462"
---
# <span data-ttu-id="40ec3-104">interface IWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="40ec3-104">interface IWebView2NavigationCompletedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="40ec3-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="40ec3-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="40ec3-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="40ec3-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="40ec3-107">Arguments d’événement pour l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="40ec3-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="40ec3-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="40ec3-108">Summary</span></span>

 <span data-ttu-id="40ec3-109">Ses</span><span class="sxs-lookup"><span data-stu-id="40ec3-109">Members</span></span>                        | <span data-ttu-id="40ec3-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="40ec3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="40ec3-111">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="40ec3-111">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="40ec3-112">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="40ec3-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="40ec3-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="40ec3-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="40ec3-114">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="40ec3-114">The error code if the navigation failed.</span></span>

## <span data-ttu-id="40ec3-115">Ses</span><span class="sxs-lookup"><span data-stu-id="40ec3-115">Members</span></span>

#### <span data-ttu-id="40ec3-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="40ec3-116">get_IsSuccess</span></span> 

<span data-ttu-id="40ec3-117">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="40ec3-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="40ec3-118">valeur publique HRESULT [get_IsSuccess](#get_issuccess)(bool \* propriétés IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="40ec3-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="40ec3-119">Il s’agit de la valeur false pour une navigation qui s’est produite dans une page d’erreur (échecs en raison d’un réseau, échec de recherche DNS, serveur HTTP répond avec 4xx), mais peut également avoir la valeur false pour des éléments supplémentaires tels que Window. Stop () appelé sur la page de navigation.</span><span class="sxs-lookup"><span data-stu-id="40ec3-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="40ec3-120">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="40ec3-120">get_WebErrorStatus</span></span> 

<span data-ttu-id="40ec3-121">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="40ec3-121">The error code if the navigation failed.</span></span>

> <span data-ttu-id="40ec3-122">[get_WebErrorStatus](#get_weberrorstatus)par le biais du public HRESULT (WEBVIEW2_WEB_ERROR_STATUS \* WEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="40ec3-122">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(WEBVIEW2_WEB_ERROR_STATUS \* WEBVIEW2_WEB_ERROR_STATUS)</span></span>

