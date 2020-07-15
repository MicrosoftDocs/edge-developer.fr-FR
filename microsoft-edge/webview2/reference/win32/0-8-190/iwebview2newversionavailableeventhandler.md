---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2NewVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: da17bad643ac7f0a9614754bf57c7d208c265ace
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878357"
---
# <span data-ttu-id="33afd-104">0.8.355-interface IWebView2NewVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="33afd-104">0.8.355 - interface IWebView2NewVersionAvailableEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="33afd-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="33afd-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="33afd-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="33afd-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NewVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="33afd-107">L’appelant implémente cette interface pour recevoir des événements NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="33afd-107">The caller implements this interface to receive NewVersionAvailable events.</span></span>

## <span data-ttu-id="33afd-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="33afd-108">Summary</span></span>

 <span data-ttu-id="33afd-109">Ses</span><span class="sxs-lookup"><span data-stu-id="33afd-109">Members</span></span>                        | <span data-ttu-id="33afd-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="33afd-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="33afd-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="33afd-111">Invoke</span></span>](#invoke) | <span data-ttu-id="33afd-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="33afd-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="33afd-113">Utilisez la méthode get_NewVersion de [IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) pour obtenir le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="33afd-113">Use the get_NewVersion method of [IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) to get the new version number.</span></span>

## <span data-ttu-id="33afd-114">Ses</span><span class="sxs-lookup"><span data-stu-id="33afd-114">Members</span></span>

#### <span data-ttu-id="33afd-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="33afd-115">Invoke</span></span> 

<span data-ttu-id="33afd-116">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="33afd-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="33afd-117">[appel](#invoke)HRESULT public ([IWebView2Environment](IWebView2Environment.md) \* webviewEnvironment,[IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="33afd-117">public HRESULT [Invoke](#invoke)([IWebView2Environment](IWebView2Environment.md) \* webviewEnvironment,[IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) \* args)</span></span>

