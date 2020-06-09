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
ms.openlocfilehash: 1d91bb767045179a5d8de3700f86ff6d92a9ef36
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698757"
---
# <span data-ttu-id="c39ef-104">interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="c39ef-104">interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="c39ef-105">Cette API expérimentale qui est fournie avec notre version bêta du SDK version 0.9.538.</span><span class="sxs-lookup"><span data-stu-id="c39ef-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="c39ef-106">Arguments d’événement pour l’événement NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="c39ef-106">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="c39ef-107">Résumé</span><span class="sxs-lookup"><span data-stu-id="c39ef-107">Summary</span></span>

 <span data-ttu-id="c39ef-108">Ses</span><span class="sxs-lookup"><span data-stu-id="c39ef-108">Members</span></span>                        | <span data-ttu-id="c39ef-109">Descriptions</span><span class="sxs-lookup"><span data-stu-id="c39ef-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c39ef-110">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="c39ef-110">get_WindowFeatures</span></span>](#get_windowfeatures) | <span data-ttu-id="c39ef-111">Fonctionnalités de fenêtre spécifiées par l’appel Window. Open.</span><span class="sxs-lookup"><span data-stu-id="c39ef-111">Window features specified by the window.open call.</span></span>

<span data-ttu-id="c39ef-112">L’événement est déclenché lorsque le contenu de l’affichage WebView est demandé à une nouvelle fenêtre (via Window. Open () et ainsi de suite.)</span><span class="sxs-lookup"><span data-stu-id="c39ef-112">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="c39ef-113">Ses</span><span class="sxs-lookup"><span data-stu-id="c39ef-113">Members</span></span>

#### <span data-ttu-id="c39ef-114">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="c39ef-114">get_WindowFeatures</span></span> 

<span data-ttu-id="c39ef-115">Fonctionnalités de fenêtre spécifiées par l’appel Window. Open.</span><span class="sxs-lookup"><span data-stu-id="c39ef-115">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="c39ef-116">[get_WindowFeatures](#get_windowfeatures)par le biais du public HRESULT ([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \* \* WindowFeatures)</span><span class="sxs-lookup"><span data-stu-id="c39ef-116">public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \*\* windowFeatures)</span></span>

<span data-ttu-id="c39ef-117">Ces fonctionnalités peuvent être envisagées pour le positionnement et le dimensionnement des nouvelles fenêtres WebView.</span><span class="sxs-lookup"><span data-stu-id="c39ef-117">These features can be considered for positioning and sizing of new webview windows.</span></span>

