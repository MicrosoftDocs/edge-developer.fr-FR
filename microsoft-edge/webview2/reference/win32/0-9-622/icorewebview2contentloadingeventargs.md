---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ContentLoadingEventArgs
ms.openlocfilehash: 229389c6859363ef9a7c3fbf7719dbe30a061875
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011997"
---
# <span data-ttu-id="4b1ae-104">interface ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="4b1ae-104">interface ICoreWebView2ContentLoadingEventArgs</span></span> 

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="4b1ae-105">Arguments d’événement pour l’événement ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="4b1ae-105">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="4b1ae-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="4b1ae-106">Summary</span></span>

 <span data-ttu-id="4b1ae-107">Ses</span><span class="sxs-lookup"><span data-stu-id="4b1ae-107">Members</span></span>                        | <span data-ttu-id="4b1ae-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="4b1ae-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4b1ae-109">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="4b1ae-109">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="4b1ae-110">True si le contenu chargé est une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4b1ae-110">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="4b1ae-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="4b1ae-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="4b1ae-112">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="4b1ae-112">The ID of the navigation.</span></span>

## <span data-ttu-id="4b1ae-113">Ses</span><span class="sxs-lookup"><span data-stu-id="4b1ae-113">Members</span></span>

#### <span data-ttu-id="4b1ae-114">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="4b1ae-114">get_IsErrorPage</span></span> 

<span data-ttu-id="4b1ae-115">True si le contenu chargé est une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4b1ae-115">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="4b1ae-116">valeur publique HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="4b1ae-116">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="4b1ae-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="4b1ae-117">get_NavigationId</span></span> 

<span data-ttu-id="4b1ae-118">ID de la navigation.</span><span class="sxs-lookup"><span data-stu-id="4b1ae-118">The ID of the navigation.</span></span>

> <span data-ttu-id="4b1ae-119">[get_NavigationIds](#get_navigationid)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="4b1ae-119">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigationId)</span></span>

