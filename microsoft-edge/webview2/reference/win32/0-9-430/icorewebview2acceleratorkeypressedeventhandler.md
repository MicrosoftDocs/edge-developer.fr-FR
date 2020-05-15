---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 8dfb39da070a5c43ce98057830f75f939e86f029
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653435"
---
# <span data-ttu-id="66299-104">interface ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="66299-104">interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="66299-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="66299-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="66299-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="66299-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="66299-107">L’appelant implémente cette interface pour recevoir l’événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="66299-107">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="66299-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="66299-108">Summary</span></span>

 <span data-ttu-id="66299-109">Ses</span><span class="sxs-lookup"><span data-stu-id="66299-109">Members</span></span>                        | <span data-ttu-id="66299-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="66299-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="66299-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="66299-111">Invoke</span></span>](#invoke) | <span data-ttu-id="66299-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="66299-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="66299-113">Ses</span><span class="sxs-lookup"><span data-stu-id="66299-113">Members</span></span>

#### <span data-ttu-id="66299-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="66299-114">Invoke</span></span> 

<span data-ttu-id="66299-115">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="66299-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="66299-116">[appel](#invoke)HRESULT public ([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,[ICoreWebView2AcceleratorKeyPressedEventArgs](ICoreWebView2AcceleratorKeyPressedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="66299-116">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,[ICoreWebView2AcceleratorKeyPressedEventArgs](ICoreWebView2AcceleratorKeyPressedEventArgs.md) \* args)</span></span>

