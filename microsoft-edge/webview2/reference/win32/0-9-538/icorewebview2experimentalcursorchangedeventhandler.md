---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2ExperimentalCursorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ExperimentalCursorChangedEventHandler
ms.openlocfilehash: f58279d1a3c404715be5aad8bf1be5ef120e1d94
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880002"
---
# <span data-ttu-id="e1dde-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e1dde-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="e1dde-105">Cette API expérimentale qui est fournie avec notre version bêta du SDK version 0.9.538.</span><span class="sxs-lookup"><span data-stu-id="e1dde-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="e1dde-106">L’appelant implémente cette interface pour recevoir des événements CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="e1dde-106">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="e1dde-107">Résumé</span><span class="sxs-lookup"><span data-stu-id="e1dde-107">Summary</span></span>

 <span data-ttu-id="e1dde-108">Ses</span><span class="sxs-lookup"><span data-stu-id="e1dde-108">Members</span></span>                        | <span data-ttu-id="e1dde-109">Descriptions</span><span class="sxs-lookup"><span data-stu-id="e1dde-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e1dde-110">Invoke</span><span class="sxs-lookup"><span data-stu-id="e1dde-110">Invoke</span></span>](#invoke) | <span data-ttu-id="e1dde-111">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="e1dde-111">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="e1dde-112">Utilisez la propriété Cursor pour obtenir le nouveau curseur.</span><span class="sxs-lookup"><span data-stu-id="e1dde-112">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="e1dde-113">Ses</span><span class="sxs-lookup"><span data-stu-id="e1dde-113">Members</span></span>

#### <span data-ttu-id="e1dde-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="e1dde-114">Invoke</span></span> 

<span data-ttu-id="e1dde-115">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="e1dde-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e1dde-116">[appel](#invoke)de HRESULT public ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="e1dde-116">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="e1dde-117">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="e1dde-117">There are no event args and the args parameter will be null.</span></span>

