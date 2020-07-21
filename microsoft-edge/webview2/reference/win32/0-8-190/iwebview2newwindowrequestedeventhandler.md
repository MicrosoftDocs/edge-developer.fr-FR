---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2NewWindowRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 2fe743f0ffe39107252a184e2e98cc2904e3c640
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884973"
---
# <span data-ttu-id="13316-104">0.8.355-interface IWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="13316-104">0.8.355 - interface IWebView2NewWindowRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="13316-105">L’appelant implémente cette interface pour recevoir des événements NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="13316-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="13316-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="13316-106">Summary</span></span>

 <span data-ttu-id="13316-107">Ses</span><span class="sxs-lookup"><span data-stu-id="13316-107">Members</span></span>                        | <span data-ttu-id="13316-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="13316-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="13316-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="13316-109">Invoke</span></span>](#invoke) | <span data-ttu-id="13316-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="13316-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="13316-111">Ses</span><span class="sxs-lookup"><span data-stu-id="13316-111">Members</span></span>

#### <span data-ttu-id="13316-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="13316-112">Invoke</span></span> 

<span data-ttu-id="13316-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="13316-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="13316-114">[appel](#invoke)HRESULT public ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2NewWindowRequestedEventArgs](IWebView2NewWindowRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="13316-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2NewWindowRequestedEventArgs](IWebView2NewWindowRequestedEventArgs.md) \* args)</span></span>

