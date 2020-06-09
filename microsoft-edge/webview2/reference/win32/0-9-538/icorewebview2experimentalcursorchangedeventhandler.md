---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: b44bd47f5352179abcc06ef5fd5b8f613bde455e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698636"
---
# <span data-ttu-id="07754-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="07754-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="07754-105">Cette API expérimentale qui est fournie avec notre version bêta du SDK version 0.9.538.</span><span class="sxs-lookup"><span data-stu-id="07754-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="07754-106">L’appelant implémente cette interface pour recevoir des événements CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="07754-106">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="07754-107">Résumé</span><span class="sxs-lookup"><span data-stu-id="07754-107">Summary</span></span>

 <span data-ttu-id="07754-108">Ses</span><span class="sxs-lookup"><span data-stu-id="07754-108">Members</span></span>                        | <span data-ttu-id="07754-109">Descriptions</span><span class="sxs-lookup"><span data-stu-id="07754-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="07754-110">Invoke</span><span class="sxs-lookup"><span data-stu-id="07754-110">Invoke</span></span>](#invoke) | <span data-ttu-id="07754-111">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="07754-111">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="07754-112">Utilisez la propriété Cursor pour obtenir le nouveau curseur.</span><span class="sxs-lookup"><span data-stu-id="07754-112">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="07754-113">Ses</span><span class="sxs-lookup"><span data-stu-id="07754-113">Members</span></span>

#### <span data-ttu-id="07754-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="07754-114">Invoke</span></span> 

<span data-ttu-id="07754-115">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="07754-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="07754-116">[appel](#invoke)de HRESULT public ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="07754-116">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="07754-117">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="07754-117">There are no event args and the args parameter will be null.</span></span>

