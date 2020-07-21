---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 22c5e558238e4542ebe70855c3d20837838bebb8
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883960"
---
# <span data-ttu-id="41c1a-104">0.9.430-interface ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="41c1a-104">0.9.430 - interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="41c1a-105">L’appelant implémente cette interface pour recevoir des événements ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="41c1a-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="41c1a-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="41c1a-106">Summary</span></span>

 <span data-ttu-id="41c1a-107">Ses</span><span class="sxs-lookup"><span data-stu-id="41c1a-107">Members</span></span>                        | <span data-ttu-id="41c1a-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="41c1a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="41c1a-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="41c1a-109">Invoke</span></span>](#invoke) | <span data-ttu-id="41c1a-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="41c1a-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="41c1a-111">Utilisez la propriété ICoreWebView2Host. ZoomFactor pour obtenir le facteur de zoom modifié.</span><span class="sxs-lookup"><span data-stu-id="41c1a-111">Use the ICoreWebView2Host.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="41c1a-112">Ses</span><span class="sxs-lookup"><span data-stu-id="41c1a-112">Members</span></span>

#### <span data-ttu-id="41c1a-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="41c1a-113">Invoke</span></span> 

<span data-ttu-id="41c1a-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="41c1a-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="41c1a-115">[appel](#invoke)de HRESULT public ([ICoreWebView2Host](ICoreWebView2Host.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="41c1a-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="41c1a-116">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="41c1a-116">There are no event args and the args parameter will be null.</span></span>

