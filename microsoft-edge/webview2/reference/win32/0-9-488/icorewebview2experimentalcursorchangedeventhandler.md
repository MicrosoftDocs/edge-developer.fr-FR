---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2ExperimentalCursorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: ee6de606d6ed8a9e00dbdacee9bb07b341a6d04e
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886485"
---
# <span data-ttu-id="873b8-104">0.9.515-interface ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="873b8-104">0.9.515 - interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="873b8-105">L’appelant implémente cette interface pour recevoir des événements CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="873b8-105">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="873b8-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="873b8-106">Summary</span></span>

 <span data-ttu-id="873b8-107">Ses</span><span class="sxs-lookup"><span data-stu-id="873b8-107">Members</span></span>                        | <span data-ttu-id="873b8-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="873b8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="873b8-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="873b8-109">Invoke</span></span>](#invoke) | <span data-ttu-id="873b8-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="873b8-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="873b8-111">Utilisez la propriété Cursor pour obtenir le nouveau curseur.</span><span class="sxs-lookup"><span data-stu-id="873b8-111">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="873b8-112">Ses</span><span class="sxs-lookup"><span data-stu-id="873b8-112">Members</span></span>

#### <span data-ttu-id="873b8-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="873b8-113">Invoke</span></span> 

<span data-ttu-id="873b8-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="873b8-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="873b8-115">[appel](#invoke)de HRESULT public ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="873b8-115">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="873b8-116">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="873b8-116">There are no event args and the args parameter will be null.</span></span>

