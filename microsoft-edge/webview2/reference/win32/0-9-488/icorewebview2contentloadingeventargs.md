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
ms.openlocfilehash: c720b700257554891f13477f5f3508e331ac6b25
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698203"
---
# <span data-ttu-id="08adc-104">interface ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="08adc-104">interface ICoreWebView2ContentLoadingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="08adc-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="08adc-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="08adc-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="08adc-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="08adc-107">Arguments d’événement pour l’événement ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="08adc-107">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="08adc-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="08adc-108">Summary</span></span>

 <span data-ttu-id="08adc-109">Ses</span><span class="sxs-lookup"><span data-stu-id="08adc-109">Members</span></span>                        | <span data-ttu-id="08adc-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="08adc-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="08adc-111">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="08adc-111">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="08adc-112">True si le contenu chargé est une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="08adc-112">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="08adc-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="08adc-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="08adc-114">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="08adc-114">The ID of the navigation.</span></span>

## <span data-ttu-id="08adc-115">Ses</span><span class="sxs-lookup"><span data-stu-id="08adc-115">Members</span></span>

#### <span data-ttu-id="08adc-116">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="08adc-116">get_IsErrorPage</span></span> 

<span data-ttu-id="08adc-117">True si le contenu chargé est une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="08adc-117">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="08adc-118">valeur publique HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="08adc-118">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="08adc-119">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="08adc-119">get_NavigationId</span></span> 

<span data-ttu-id="08adc-120">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="08adc-120">The ID of the navigation.</span></span>

> <span data-ttu-id="08adc-121">navigation_id [get_NavigationId](#get_navigationid)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="08adc-121">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

