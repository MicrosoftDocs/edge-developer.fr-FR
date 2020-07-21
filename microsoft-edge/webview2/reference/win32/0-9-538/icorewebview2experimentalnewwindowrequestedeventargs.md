---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2ExperimentalNewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ExperimentalNewWindowRequestedEventArgs
ms.openlocfilehash: d18ccc91d16213cf0a915420b406b65823b3f9d9
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886450"
---
# <span data-ttu-id="21078-104">interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="21078-104">interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="21078-105">Arguments d’événement pour l’événement NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="21078-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="21078-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="21078-106">Summary</span></span>

 <span data-ttu-id="21078-107">Ses</span><span class="sxs-lookup"><span data-stu-id="21078-107">Members</span></span>                        | <span data-ttu-id="21078-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="21078-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="21078-109">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="21078-109">get_WindowFeatures</span></span>](#get_windowfeatures) | <span data-ttu-id="21078-110">Fonctionnalités de fenêtre spécifiées par l’appel Window. Open.</span><span class="sxs-lookup"><span data-stu-id="21078-110">Window features specified by the window.open call.</span></span>

<span data-ttu-id="21078-111">L’événement est déclenché lorsque le contenu de l’affichage WebView est demandé à une nouvelle fenêtre (via Window. Open () et ainsi de suite.)</span><span class="sxs-lookup"><span data-stu-id="21078-111">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="21078-112">Ses</span><span class="sxs-lookup"><span data-stu-id="21078-112">Members</span></span>

#### <span data-ttu-id="21078-113">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="21078-113">get_WindowFeatures</span></span> 

<span data-ttu-id="21078-114">Fonctionnalités de fenêtre spécifiées par l’appel Window. Open.</span><span class="sxs-lookup"><span data-stu-id="21078-114">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="21078-115">[get_WindowFeatures](#get_windowfeatures)par le biais du public HRESULT ([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \* \* WindowFeatures)</span><span class="sxs-lookup"><span data-stu-id="21078-115">public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \*\* windowFeatures)</span></span>

<span data-ttu-id="21078-116">Ces fonctionnalités peuvent être envisagées pour le positionnement et le dimensionnement des nouvelles fenêtres WebView.</span><span class="sxs-lookup"><span data-stu-id="21078-116">These features can be considered for positioning and sizing of new webview windows.</span></span>

