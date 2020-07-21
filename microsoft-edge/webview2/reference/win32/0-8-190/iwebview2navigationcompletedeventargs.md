---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: b496c37949e934fadf0af736059566edcab9f5c3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885932"
---
# <span data-ttu-id="9c5f8-104">0.8.355-interface IWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="9c5f8-104">0.8.355 - interface IWebView2NavigationCompletedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="9c5f8-105">Arguments d’événement pour l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="9c5f8-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="9c5f8-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="9c5f8-106">Summary</span></span>

 <span data-ttu-id="9c5f8-107">Ses</span><span class="sxs-lookup"><span data-stu-id="9c5f8-107">Members</span></span>                        | <span data-ttu-id="9c5f8-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="9c5f8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9c5f8-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="9c5f8-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="9c5f8-110">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="9c5f8-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="9c5f8-111">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="9c5f8-111">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="9c5f8-112">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="9c5f8-112">The error code if the navigation failed.</span></span>

## <span data-ttu-id="9c5f8-113">Ses</span><span class="sxs-lookup"><span data-stu-id="9c5f8-113">Members</span></span>

#### <span data-ttu-id="9c5f8-114">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="9c5f8-114">get_IsSuccess</span></span> 

<span data-ttu-id="9c5f8-115">True lorsque la navigation est réussie.</span><span class="sxs-lookup"><span data-stu-id="9c5f8-115">True when the navigation is successful.</span></span>

> <span data-ttu-id="9c5f8-116">valeur publique HRESULT [get_IsSuccess](#get_issuccess)(bool \* propriétés IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="9c5f8-116">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="9c5f8-117">Il s’agit de la valeur false pour une navigation qui s’est produite dans une page d’erreur (échecs en raison d’un réseau, échec de recherche DNS, serveur HTTP répond avec 4xx), mais peut également avoir la valeur false pour des éléments supplémentaires tels que Window. Stop () appelé sur la page de navigation.</span><span class="sxs-lookup"><span data-stu-id="9c5f8-117">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="9c5f8-118">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="9c5f8-118">get_WebErrorStatus</span></span> 

<span data-ttu-id="9c5f8-119">Code d’erreur en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="9c5f8-119">The error code if the navigation failed.</span></span>

> <span data-ttu-id="9c5f8-120">[get_WebErrorStatus](#get_weberrorstatus)par le biais du public HRESULT (WEBVIEW2_WEB_ERROR_STATUS \* WEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="9c5f8-120">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(WEBVIEW2_WEB_ERROR_STATUS \* WEBVIEW2_WEB_ERROR_STATUS)</span></span>

