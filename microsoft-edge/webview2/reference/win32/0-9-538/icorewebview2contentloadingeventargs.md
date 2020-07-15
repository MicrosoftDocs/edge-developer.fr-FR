---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ContentLoadingEventArgs
ms.openlocfilehash: 571aae9e1e00938c9bf0f3fb872fccf340269105
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877454"
---
# <span data-ttu-id="aed94-104">interface ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="aed94-104">interface ICoreWebView2ContentLoadingEventArgs</span></span> 

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="aed94-105">Arguments d’événement pour l’événement ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="aed94-105">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="aed94-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="aed94-106">Summary</span></span>

 <span data-ttu-id="aed94-107">Ses</span><span class="sxs-lookup"><span data-stu-id="aed94-107">Members</span></span>                        | <span data-ttu-id="aed94-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="aed94-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="aed94-109">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="aed94-109">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="aed94-110">True si le contenu chargé est une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="aed94-110">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="aed94-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="aed94-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="aed94-112">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="aed94-112">The ID of the navigation.</span></span>

## <span data-ttu-id="aed94-113">Ses</span><span class="sxs-lookup"><span data-stu-id="aed94-113">Members</span></span>

#### <span data-ttu-id="aed94-114">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="aed94-114">get_IsErrorPage</span></span> 

<span data-ttu-id="aed94-115">True si le contenu chargé est une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="aed94-115">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="aed94-116">valeur publique HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="aed94-116">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="aed94-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="aed94-117">get_NavigationId</span></span> 

<span data-ttu-id="aed94-118">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="aed94-118">The ID of the navigation.</span></span>

> <span data-ttu-id="aed94-119">navigation_id [get_NavigationId](#get_navigationid)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="aed94-119">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

