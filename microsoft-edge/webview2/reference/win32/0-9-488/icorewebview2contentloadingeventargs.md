---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: c6bb99078b5574ba89c0d66b49e2c63cd6888d28
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653538"
---
# <span data-ttu-id="3d9c9-104">interface ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="3d9c9-104">interface ICoreWebView2ContentLoadingEventArgs</span></span> 

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="3d9c9-105">Arguments d’événement pour l’événement ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="3d9c9-105">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="3d9c9-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="3d9c9-106">Summary</span></span>

 <span data-ttu-id="3d9c9-107">Ses</span><span class="sxs-lookup"><span data-stu-id="3d9c9-107">Members</span></span>                        | <span data-ttu-id="3d9c9-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="3d9c9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3d9c9-109">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="3d9c9-109">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="3d9c9-110">True si le contenu chargé est une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="3d9c9-110">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="3d9c9-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="3d9c9-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="3d9c9-112">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="3d9c9-112">The ID of the navigation.</span></span>

## <span data-ttu-id="3d9c9-113">Ses</span><span class="sxs-lookup"><span data-stu-id="3d9c9-113">Members</span></span>

#### <span data-ttu-id="3d9c9-114">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="3d9c9-114">get_IsErrorPage</span></span> 

<span data-ttu-id="3d9c9-115">True si le contenu chargé est une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="3d9c9-115">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="3d9c9-116">valeur publique HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="3d9c9-116">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="3d9c9-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="3d9c9-117">get_NavigationId</span></span> 

<span data-ttu-id="3d9c9-118">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="3d9c9-118">The ID of the navigation.</span></span>

> <span data-ttu-id="3d9c9-119">navigation_id [get_NavigationId](#get_navigationid)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="3d9c9-119">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

