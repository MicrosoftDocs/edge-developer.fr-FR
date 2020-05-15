---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 889728489b6c4b06cd224915a0e12ee0a4144653
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653303"
---
# <span data-ttu-id="84c16-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="84c16-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="84c16-105">L’appelant implémente cette interface pour recevoir des événements NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="84c16-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="84c16-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="84c16-106">Summary</span></span>

 <span data-ttu-id="84c16-107">Ses</span><span class="sxs-lookup"><span data-stu-id="84c16-107">Members</span></span>                        | <span data-ttu-id="84c16-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="84c16-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="84c16-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="84c16-109">Invoke</span></span>](#invoke) | <span data-ttu-id="84c16-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="84c16-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="84c16-111">Ses</span><span class="sxs-lookup"><span data-stu-id="84c16-111">Members</span></span>

#### <span data-ttu-id="84c16-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="84c16-112">Invoke</span></span> 

<span data-ttu-id="84c16-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="84c16-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="84c16-114">[appel](#invoke)de HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="84c16-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="84c16-115">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="84c16-115">There are no event args and the args parameter will be null.</span></span>

