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
ms.openlocfilehash: 0d02fb1c8605bc6817085748154055cdfa489da8
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698711"
---
# <span data-ttu-id="6648c-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="6648c-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="6648c-105">L’appelant implémente cette interface pour recevoir des événements NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="6648c-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="6648c-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="6648c-106">Summary</span></span>

 <span data-ttu-id="6648c-107">Ses</span><span class="sxs-lookup"><span data-stu-id="6648c-107">Members</span></span>                        | <span data-ttu-id="6648c-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="6648c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6648c-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="6648c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="6648c-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="6648c-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="6648c-111">Ses</span><span class="sxs-lookup"><span data-stu-id="6648c-111">Members</span></span>

#### <span data-ttu-id="6648c-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="6648c-112">Invoke</span></span> 

<span data-ttu-id="6648c-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="6648c-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="6648c-114">[appel](#invoke)de HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="6648c-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="6648c-115">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="6648c-115">There are no event args and the args parameter will be null.</span></span>

