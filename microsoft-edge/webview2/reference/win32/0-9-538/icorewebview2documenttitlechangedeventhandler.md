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
ms.openlocfilehash: 2908ad851a7899d2ea053bfa50616c8b244bca6c
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698646"
---
# <span data-ttu-id="867a0-104">interface ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="867a0-104">interface ICoreWebView2DocumentTitleChangedEventHandler</span></span> 

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="867a0-105">L’appelant implémente cette interface pour recevoir des événements DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="867a0-105">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="867a0-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="867a0-106">Summary</span></span>

 <span data-ttu-id="867a0-107">Ses</span><span class="sxs-lookup"><span data-stu-id="867a0-107">Members</span></span>                        | <span data-ttu-id="867a0-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="867a0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="867a0-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="867a0-109">Invoke</span></span>](#invoke) | <span data-ttu-id="867a0-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="867a0-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="867a0-111">Utilisez la propriété DocumentTitle pour obtenir le titre modifié.</span><span class="sxs-lookup"><span data-stu-id="867a0-111">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="867a0-112">Ses</span><span class="sxs-lookup"><span data-stu-id="867a0-112">Members</span></span>

#### <span data-ttu-id="867a0-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="867a0-113">Invoke</span></span> 

<span data-ttu-id="867a0-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="867a0-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="867a0-115">[appel](#invoke)de HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="867a0-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="867a0-116">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="867a0-116">There are no event args and the args parameter will be null.</span></span>

