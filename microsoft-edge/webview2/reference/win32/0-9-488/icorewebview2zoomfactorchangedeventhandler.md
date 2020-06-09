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
ms.openlocfilehash: 64211bf99873ef2e2a41aaf2fb9453e892f6536a
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698105"
---
# <span data-ttu-id="5313a-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="5313a-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="5313a-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="5313a-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="5313a-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="5313a-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="5313a-107">L’appelant implémente cette interface pour recevoir des événements ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="5313a-107">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="5313a-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="5313a-108">Summary</span></span>

 <span data-ttu-id="5313a-109">Ses</span><span class="sxs-lookup"><span data-stu-id="5313a-109">Members</span></span>                        | <span data-ttu-id="5313a-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="5313a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5313a-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="5313a-111">Invoke</span></span>](#invoke) | <span data-ttu-id="5313a-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="5313a-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="5313a-113">Utilisez la propriété ICoreWebView2Controller. ZoomFactor pour obtenir le facteur de zoom modifié.</span><span class="sxs-lookup"><span data-stu-id="5313a-113">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="5313a-114">Ses</span><span class="sxs-lookup"><span data-stu-id="5313a-114">Members</span></span>

#### <span data-ttu-id="5313a-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="5313a-115">Invoke</span></span> 

<span data-ttu-id="5313a-116">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="5313a-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="5313a-117">[appel](#invoke)de HRESULT public ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="5313a-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="5313a-118">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="5313a-118">There are no event args and the args parameter will be null.</span></span>

