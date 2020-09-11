---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ZoomFactorChangedEventHandler
ms.openlocfilehash: c941629ab8ee87c0c964b00798878bb69265669a
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011390"
---
# <span data-ttu-id="d90f9-104">0.9.579-interface ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="d90f9-104">0.9.579 - interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="d90f9-105">L’appelant implémente cette interface pour recevoir des événements ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="d90f9-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="d90f9-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="d90f9-106">Summary</span></span>

 <span data-ttu-id="d90f9-107">Ses</span><span class="sxs-lookup"><span data-stu-id="d90f9-107">Members</span></span>                        | <span data-ttu-id="d90f9-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="d90f9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d90f9-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="d90f9-109">Invoke</span></span>](#invoke) | <span data-ttu-id="d90f9-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="d90f9-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="d90f9-111">Utilisez la propriété ICoreWebView2Controller. ZoomFactor pour obtenir le facteur de zoom modifié.</span><span class="sxs-lookup"><span data-stu-id="d90f9-111">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="d90f9-112">Ses</span><span class="sxs-lookup"><span data-stu-id="d90f9-112">Members</span></span>

#### <span data-ttu-id="d90f9-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="d90f9-113">Invoke</span></span> 

<span data-ttu-id="d90f9-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="d90f9-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d90f9-115">[appel](#invoke)de HRESULT public ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="d90f9-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="d90f9-116">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="d90f9-116">There are no event args and the args parameter will be null.</span></span>

