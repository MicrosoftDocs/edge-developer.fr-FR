---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2WindowCloseRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 98f3e114e52dd9b8a044e34e7f24067c0b68148b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884581"
---
# <span data-ttu-id="fbeb0-104">0.9.430-interface ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="fbeb0-104">0.9.430 - interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="fbeb0-105">L’appelant implémente cette interface pour recevoir des événements NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="fbeb0-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="fbeb0-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="fbeb0-106">Summary</span></span>

 <span data-ttu-id="fbeb0-107">Ses</span><span class="sxs-lookup"><span data-stu-id="fbeb0-107">Members</span></span>                        | <span data-ttu-id="fbeb0-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="fbeb0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fbeb0-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="fbeb0-109">Invoke</span></span>](#invoke) | <span data-ttu-id="fbeb0-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="fbeb0-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="fbeb0-111">Ses</span><span class="sxs-lookup"><span data-stu-id="fbeb0-111">Members</span></span>

#### <span data-ttu-id="fbeb0-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="fbeb0-112">Invoke</span></span> 

<span data-ttu-id="fbeb0-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="fbeb0-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="fbeb0-114">[appel](#invoke)de HRESULT public ([ICoreWebView2](ICoreWebView2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="fbeb0-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="fbeb0-115">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="fbeb0-115">There are no event args and the args parameter will be null.</span></span>

