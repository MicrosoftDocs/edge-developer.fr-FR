---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 91cd4245ff6c75e72457410211deefd9ab7f09d1
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883692"
---
# <span data-ttu-id="1b587-104">0.9.515-interface ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1b587-104">0.9.515 - interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="1b587-105">L’appelant implémente cette interface pour recevoir des événements ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="1b587-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="1b587-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="1b587-106">Summary</span></span>

 <span data-ttu-id="1b587-107">Ses</span><span class="sxs-lookup"><span data-stu-id="1b587-107">Members</span></span>                        | <span data-ttu-id="1b587-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="1b587-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1b587-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="1b587-109">Invoke</span></span>](#invoke) | <span data-ttu-id="1b587-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="1b587-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="1b587-111">Utilisez la propriété ICoreWebView2Controller. ZoomFactor pour obtenir le facteur de zoom modifié.</span><span class="sxs-lookup"><span data-stu-id="1b587-111">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="1b587-112">Ses</span><span class="sxs-lookup"><span data-stu-id="1b587-112">Members</span></span>

#### <span data-ttu-id="1b587-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="1b587-113">Invoke</span></span> 

<span data-ttu-id="1b587-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="1b587-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="1b587-115">[appel](#invoke)de HRESULT public ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="1b587-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="1b587-116">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="1b587-116">There are no event args and the args parameter will be null.</span></span>

