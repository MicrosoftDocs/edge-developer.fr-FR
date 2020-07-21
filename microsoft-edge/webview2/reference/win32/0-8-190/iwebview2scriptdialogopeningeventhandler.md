---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2ScriptDialogOpeningEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 58e76c377d8d5709c006cb3a4da2e0edf73ec8fb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884910"
---
# <span data-ttu-id="d3bc2-104">0.8.355-interface IWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="d3bc2-104">0.8.355 - interface IWebView2ScriptDialogOpeningEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="d3bc2-105">L’appelant implémente cette interface pour recevoir l’événement ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="d3bc2-105">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="d3bc2-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="d3bc2-106">Summary</span></span>

 <span data-ttu-id="d3bc2-107">Ses</span><span class="sxs-lookup"><span data-stu-id="d3bc2-107">Members</span></span>                        | <span data-ttu-id="d3bc2-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="d3bc2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d3bc2-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="d3bc2-109">Invoke</span></span>](#invoke) | <span data-ttu-id="d3bc2-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="d3bc2-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="d3bc2-111">Ses</span><span class="sxs-lookup"><span data-stu-id="d3bc2-111">Members</span></span>

#### <span data-ttu-id="d3bc2-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="d3bc2-112">Invoke</span></span> 

<span data-ttu-id="d3bc2-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="d3bc2-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d3bc2-114">[appel](#invoke)HRESULT public ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2ScriptDialogOpeningEventArgs](IWebView2ScriptDialogOpeningEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="d3bc2-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2ScriptDialogOpeningEventArgs](IWebView2ScriptDialogOpeningEventArgs.md) \* args)</span></span>

