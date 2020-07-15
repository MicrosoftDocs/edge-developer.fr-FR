---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 42f63855c97363dab1a19cc784cf654afc40de74
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877846"
---
# <span data-ttu-id="d2c20-104">0.9.430-interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="d2c20-104">0.9.430 - interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="d2c20-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="d2c20-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="d2c20-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="d2c20-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="d2c20-107">L’appelant implémente cette interface pour recevoir des événements NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="d2c20-107">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="d2c20-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="d2c20-108">Summary</span></span>

 <span data-ttu-id="d2c20-109">Ses</span><span class="sxs-lookup"><span data-stu-id="d2c20-109">Members</span></span>                        | <span data-ttu-id="d2c20-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="d2c20-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d2c20-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="d2c20-111">Invoke</span></span>](#invoke) | <span data-ttu-id="d2c20-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="d2c20-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="d2c20-113">Utilisez la méthode get_NewVersion de [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) pour obtenir le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="d2c20-113">Use the get_NewVersion method of [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) to get the new version number.</span></span>

## <span data-ttu-id="d2c20-114">Ses</span><span class="sxs-lookup"><span data-stu-id="d2c20-114">Members</span></span>

#### <span data-ttu-id="d2c20-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="d2c20-115">Invoke</span></span> 

<span data-ttu-id="d2c20-116">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="d2c20-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d2c20-117">[appel](#invoke)HRESULT public ([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="d2c20-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span></span>

