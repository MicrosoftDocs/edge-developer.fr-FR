---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 8acec97ec6060cd53adc3821f6a51db2048935fb
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698666"
---
# <span data-ttu-id="88ba1-104">interface ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="88ba1-104">interface ICoreWebView2ContentLoadingEventArgs</span></span> 

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="88ba1-105">Arguments d’événement pour l’événement ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="88ba1-105">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="88ba1-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="88ba1-106">Summary</span></span>

 <span data-ttu-id="88ba1-107">Ses</span><span class="sxs-lookup"><span data-stu-id="88ba1-107">Members</span></span>                        | <span data-ttu-id="88ba1-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="88ba1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="88ba1-109">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="88ba1-109">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="88ba1-110">True si le contenu chargé est une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="88ba1-110">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="88ba1-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="88ba1-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="88ba1-112">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="88ba1-112">The ID of the navigation.</span></span>

## <span data-ttu-id="88ba1-113">Ses</span><span class="sxs-lookup"><span data-stu-id="88ba1-113">Members</span></span>

#### <span data-ttu-id="88ba1-114">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="88ba1-114">get_IsErrorPage</span></span> 

<span data-ttu-id="88ba1-115">True si le contenu chargé est une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="88ba1-115">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="88ba1-116">valeur publique HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="88ba1-116">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="88ba1-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="88ba1-117">get_NavigationId</span></span> 

<span data-ttu-id="88ba1-118">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="88ba1-118">The ID of the navigation.</span></span>

> <span data-ttu-id="88ba1-119">navigation_id [get_NavigationId](#get_navigationid)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="88ba1-119">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

