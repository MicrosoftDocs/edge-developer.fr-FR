---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2ExperimentalNewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ExperimentalNewWindowRequestedEventArgs
ms.openlocfilehash: 39d52b1231e767739b63b3759cdd08e4c9b26be3
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879988"
---
# <span data-ttu-id="e32cb-104">interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e32cb-104">interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="e32cb-105">Cette API expérimentale qui est fournie avec notre version bêta du SDK version 0.9.538.</span><span class="sxs-lookup"><span data-stu-id="e32cb-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="e32cb-106">Arguments d’événement pour l’événement NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="e32cb-106">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="e32cb-107">Résumé</span><span class="sxs-lookup"><span data-stu-id="e32cb-107">Summary</span></span>

 <span data-ttu-id="e32cb-108">Ses</span><span class="sxs-lookup"><span data-stu-id="e32cb-108">Members</span></span>                        | <span data-ttu-id="e32cb-109">Descriptions</span><span class="sxs-lookup"><span data-stu-id="e32cb-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e32cb-110">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="e32cb-110">get_WindowFeatures</span></span>](#get_windowfeatures) | <span data-ttu-id="e32cb-111">Fonctionnalités de fenêtre spécifiées par l’appel Window. Open.</span><span class="sxs-lookup"><span data-stu-id="e32cb-111">Window features specified by the window.open call.</span></span>

<span data-ttu-id="e32cb-112">L’événement est déclenché lorsque le contenu de l’affichage WebView est demandé à une nouvelle fenêtre (via Window. Open () et ainsi de suite.)</span><span class="sxs-lookup"><span data-stu-id="e32cb-112">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="e32cb-113">Ses</span><span class="sxs-lookup"><span data-stu-id="e32cb-113">Members</span></span>

#### <span data-ttu-id="e32cb-114">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="e32cb-114">get_WindowFeatures</span></span> 

<span data-ttu-id="e32cb-115">Fonctionnalités de fenêtre spécifiées par l’appel Window. Open.</span><span class="sxs-lookup"><span data-stu-id="e32cb-115">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="e32cb-116">[get_WindowFeatures](#get_windowfeatures)par le biais du public HRESULT ([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \* \* WindowFeatures)</span><span class="sxs-lookup"><span data-stu-id="e32cb-116">public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \*\* windowFeatures)</span></span>

<span data-ttu-id="e32cb-117">Ces fonctionnalités peuvent être envisagées pour le positionnement et le dimensionnement des nouvelles fenêtres WebView.</span><span class="sxs-lookup"><span data-stu-id="e32cb-117">These features can be considered for positioning and sizing of new webview windows.</span></span>

