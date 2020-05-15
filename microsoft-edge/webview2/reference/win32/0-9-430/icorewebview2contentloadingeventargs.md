---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: c3ba6ac3a2478861abb7b26e726a9cbd606b0eb9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653429"
---
# <span data-ttu-id="06f14-104">interface ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="06f14-104">interface ICoreWebView2ContentLoadingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="06f14-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="06f14-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="06f14-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="06f14-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="06f14-107">Arguments d’événement pour l’événement ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="06f14-107">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="06f14-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="06f14-108">Summary</span></span>

 <span data-ttu-id="06f14-109">Ses</span><span class="sxs-lookup"><span data-stu-id="06f14-109">Members</span></span>                        | <span data-ttu-id="06f14-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="06f14-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="06f14-111">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="06f14-111">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="06f14-112">True si le contenu chargé est une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="06f14-112">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="06f14-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="06f14-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="06f14-114">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="06f14-114">The ID of the navigation.</span></span>

## <span data-ttu-id="06f14-115">Ses</span><span class="sxs-lookup"><span data-stu-id="06f14-115">Members</span></span>

#### <span data-ttu-id="06f14-116">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="06f14-116">get_IsErrorPage</span></span> 

<span data-ttu-id="06f14-117">True si le contenu chargé est une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="06f14-117">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="06f14-118">valeur publique HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="06f14-118">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="06f14-119">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="06f14-119">get_NavigationId</span></span> 

<span data-ttu-id="06f14-120">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="06f14-120">The ID of the navigation.</span></span>

> <span data-ttu-id="06f14-121">navigation_id [get_NavigationId](#get_navigationid)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="06f14-121">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

