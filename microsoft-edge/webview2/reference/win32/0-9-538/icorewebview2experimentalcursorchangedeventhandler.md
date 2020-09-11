---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2ExperimentalCursorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ExperimentalCursorChangedEventHandler
ms.openlocfilehash: e9bf743f9417645bee7a5692f5ef9ca9b646e7ab
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010221"
---
# <span data-ttu-id="c3530-104">0.9.579-interface ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="c3530-104">0.9.579 - interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="c3530-105">L’appelant implémente cette interface pour recevoir des événements CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="c3530-105">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="c3530-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="c3530-106">Summary</span></span>

 <span data-ttu-id="c3530-107">Ses</span><span class="sxs-lookup"><span data-stu-id="c3530-107">Members</span></span>                        | <span data-ttu-id="c3530-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="c3530-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c3530-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="c3530-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c3530-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="c3530-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="c3530-111">Utilisez la propriété Cursor pour obtenir le nouveau curseur.</span><span class="sxs-lookup"><span data-stu-id="c3530-111">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="c3530-112">Ses</span><span class="sxs-lookup"><span data-stu-id="c3530-112">Members</span></span>

#### <span data-ttu-id="c3530-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="c3530-113">Invoke</span></span> 

<span data-ttu-id="c3530-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="c3530-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c3530-115">[appel](#invoke)de HRESULT public ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="c3530-115">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="c3530-116">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="c3530-116">There are no event args and the args parameter will be null.</span></span>

