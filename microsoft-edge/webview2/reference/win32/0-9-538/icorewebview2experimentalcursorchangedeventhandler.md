---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2ExperimentalCursorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ExperimentalCursorChangedEventHandler
ms.openlocfilehash: 67d0e6e05fb3640e141ec1ae7193746a1200bbd0
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884882"
---
# <span data-ttu-id="3d2ac-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="3d2ac-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="3d2ac-105">L’appelant implémente cette interface pour recevoir des événements CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-105">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="3d2ac-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="3d2ac-106">Summary</span></span>

 <span data-ttu-id="3d2ac-107">Ses</span><span class="sxs-lookup"><span data-stu-id="3d2ac-107">Members</span></span>                        | <span data-ttu-id="3d2ac-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="3d2ac-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3d2ac-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="3d2ac-109">Invoke</span></span>](#invoke) | <span data-ttu-id="3d2ac-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="3d2ac-111">Utilisez la propriété Cursor pour obtenir le nouveau curseur.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-111">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="3d2ac-112">Ses</span><span class="sxs-lookup"><span data-stu-id="3d2ac-112">Members</span></span>

#### <span data-ttu-id="3d2ac-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="3d2ac-113">Invoke</span></span> 

<span data-ttu-id="3d2ac-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="3d2ac-115">[appel](#invoke)de HRESULT public ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="3d2ac-115">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="3d2ac-116">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-116">There are no event args and the args parameter will be null.</span></span>

