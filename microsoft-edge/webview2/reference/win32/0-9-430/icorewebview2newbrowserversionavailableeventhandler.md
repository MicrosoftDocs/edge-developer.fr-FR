---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 04859c0a22e8571a4fe8015a089c9b7d708c1dd3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884875"
---
# <span data-ttu-id="8876c-104">0.9.430-interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="8876c-104">0.9.430 - interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="8876c-105">L’appelant implémente cette interface pour recevoir des événements NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="8876c-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="8876c-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="8876c-106">Summary</span></span>

 <span data-ttu-id="8876c-107">Ses</span><span class="sxs-lookup"><span data-stu-id="8876c-107">Members</span></span>                        | <span data-ttu-id="8876c-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="8876c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8876c-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="8876c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="8876c-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="8876c-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="8876c-111">Utilisez la méthode get_NewVersion de [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) pour obtenir le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="8876c-111">Use the get_NewVersion method of [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) to get the new version number.</span></span>

## <span data-ttu-id="8876c-112">Ses</span><span class="sxs-lookup"><span data-stu-id="8876c-112">Members</span></span>

#### <span data-ttu-id="8876c-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="8876c-113">Invoke</span></span> 

<span data-ttu-id="8876c-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="8876c-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="8876c-115">[appel](#invoke)HRESULT public ([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="8876c-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span></span>

