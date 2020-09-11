---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2HistoryChangedEventHandler
ms.openlocfilehash: 909b055af0f9594bb3c85b215cb8e02f13606aa0
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011916"
---
# <span data-ttu-id="841b4-104">interface ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="841b4-104">interface ICoreWebView2HistoryChangedEventHandler</span></span> 

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="841b4-105">L’appelant implémente cette interface pour recevoir l’événement HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="841b4-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="841b4-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="841b4-106">Summary</span></span>

 <span data-ttu-id="841b4-107">Ses</span><span class="sxs-lookup"><span data-stu-id="841b4-107">Members</span></span>                        | <span data-ttu-id="841b4-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="841b4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="841b4-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="841b4-109">Invoke</span></span>](#invoke) | <span data-ttu-id="841b4-110">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="841b4-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="841b4-111">Ses</span><span class="sxs-lookup"><span data-stu-id="841b4-111">Members</span></span>

#### <span data-ttu-id="841b4-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="841b4-112">Invoke</span></span> 

<span data-ttu-id="841b4-113">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="841b4-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="841b4-114">[appel](#invoke)de HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="841b4-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

