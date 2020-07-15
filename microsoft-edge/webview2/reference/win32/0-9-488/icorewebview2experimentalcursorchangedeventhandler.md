---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2ExperimentalCursorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 6fbcc82409791bc3d2da3bb2f7985732cb344a97
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880625"
---
# <span data-ttu-id="f4c96-104">0.9.515-interface ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f4c96-104">0.9.515 - interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="f4c96-105">Cette API expérimentale qui est fournie avec notre version bêta du SDK version 0.9.488.</span><span class="sxs-lookup"><span data-stu-id="f4c96-105">This an experimental API that is shipped with our prerelease SDK version 0.9.488.</span></span>

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="f4c96-106">L’appelant implémente cette interface pour recevoir des événements CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="f4c96-106">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="f4c96-107">Résumé</span><span class="sxs-lookup"><span data-stu-id="f4c96-107">Summary</span></span>

 <span data-ttu-id="f4c96-108">Ses</span><span class="sxs-lookup"><span data-stu-id="f4c96-108">Members</span></span>                        | <span data-ttu-id="f4c96-109">Descriptions</span><span class="sxs-lookup"><span data-stu-id="f4c96-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f4c96-110">Invoke</span><span class="sxs-lookup"><span data-stu-id="f4c96-110">Invoke</span></span>](#invoke) | <span data-ttu-id="f4c96-111">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="f4c96-111">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="f4c96-112">Utilisez la propriété Cursor pour obtenir le nouveau curseur.</span><span class="sxs-lookup"><span data-stu-id="f4c96-112">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="f4c96-113">Ses</span><span class="sxs-lookup"><span data-stu-id="f4c96-113">Members</span></span>

#### <span data-ttu-id="f4c96-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="f4c96-114">Invoke</span></span> 

<span data-ttu-id="f4c96-115">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="f4c96-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f4c96-116">[appel](#invoke)de HRESULT public ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="f4c96-116">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="f4c96-117">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="f4c96-117">There are no event args and the args parameter will be null.</span></span>

