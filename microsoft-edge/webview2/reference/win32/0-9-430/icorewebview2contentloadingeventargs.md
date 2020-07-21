---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 7bccd93aeec2c5cfbc181ce5ab1cf58e29da48ce
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884294"
---
# <span data-ttu-id="a0e13-104">0.9.430-interface ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="a0e13-104">0.9.430 - interface ICoreWebView2ContentLoadingEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="a0e13-105">Arguments d’événement pour l’événement ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="a0e13-105">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="a0e13-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="a0e13-106">Summary</span></span>

 <span data-ttu-id="a0e13-107">Ses</span><span class="sxs-lookup"><span data-stu-id="a0e13-107">Members</span></span>                        | <span data-ttu-id="a0e13-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="a0e13-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a0e13-109">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="a0e13-109">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="a0e13-110">True si le contenu chargé est une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="a0e13-110">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="a0e13-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="a0e13-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="a0e13-112">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="a0e13-112">The ID of the navigation.</span></span>

## <span data-ttu-id="a0e13-113">Ses</span><span class="sxs-lookup"><span data-stu-id="a0e13-113">Members</span></span>

#### <span data-ttu-id="a0e13-114">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="a0e13-114">get_IsErrorPage</span></span> 

<span data-ttu-id="a0e13-115">True si le contenu chargé est une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="a0e13-115">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="a0e13-116">valeur publique HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="a0e13-116">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="a0e13-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="a0e13-117">get_NavigationId</span></span> 

<span data-ttu-id="a0e13-118">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="a0e13-118">The ID of the navigation.</span></span>

> <span data-ttu-id="a0e13-119">navigation_id [get_NavigationId](#get_navigationid)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="a0e13-119">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

