---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: d4e565db43e9f528b690ab32a784bfd5e40f787b
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877286"
---
# <span data-ttu-id="78db3-104">0.9.515-interface ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="78db3-104">0.9.515 - interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="78db3-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="78db3-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="78db3-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="78db3-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="78db3-107">L’appelant implémente cette interface pour recevoir des événements ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="78db3-107">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="78db3-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="78db3-108">Summary</span></span>

 <span data-ttu-id="78db3-109">Ses</span><span class="sxs-lookup"><span data-stu-id="78db3-109">Members</span></span>                        | <span data-ttu-id="78db3-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="78db3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="78db3-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="78db3-111">Invoke</span></span>](#invoke) | <span data-ttu-id="78db3-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="78db3-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="78db3-113">Utilisez la propriété ICoreWebView2Controller. ZoomFactor pour obtenir le facteur de zoom modifié.</span><span class="sxs-lookup"><span data-stu-id="78db3-113">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="78db3-114">Ses</span><span class="sxs-lookup"><span data-stu-id="78db3-114">Members</span></span>

#### <span data-ttu-id="78db3-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="78db3-115">Invoke</span></span> 

<span data-ttu-id="78db3-116">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="78db3-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="78db3-117">[appel](#invoke)de HRESULT public ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="78db3-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="78db3-118">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="78db3-118">There are no event args and the args parameter will be null.</span></span>

