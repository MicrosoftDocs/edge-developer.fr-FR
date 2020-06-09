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
ms.openlocfilehash: 68cde818ee62462aac663b66dcfc0a1ec95bf08e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697797"
---
# <span data-ttu-id="bda87-104">interface ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="bda87-104">interface ICoreWebView2ScriptDialogOpeningEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="bda87-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="bda87-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="bda87-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="bda87-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="bda87-107">L’appelant implémente cette interface pour recevoir l’événement ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="bda87-107">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="bda87-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="bda87-108">Summary</span></span>

 <span data-ttu-id="bda87-109">Ses</span><span class="sxs-lookup"><span data-stu-id="bda87-109">Members</span></span>                        | <span data-ttu-id="bda87-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="bda87-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bda87-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="bda87-111">Invoke</span></span>](#invoke) | <span data-ttu-id="bda87-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="bda87-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="bda87-113">Ses</span><span class="sxs-lookup"><span data-stu-id="bda87-113">Members</span></span>

#### <span data-ttu-id="bda87-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="bda87-114">Invoke</span></span> 

<span data-ttu-id="bda87-115">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="bda87-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="bda87-116">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="bda87-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span></span>

