---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: b44724f8e18e11374f88ed2cd22711f06f59f12d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653497"
---
# <span data-ttu-id="4bc94-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="4bc94-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="4bc94-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="4bc94-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="4bc94-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="4bc94-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="4bc94-107">L’appelant implémente cette interface pour recevoir des événements NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="4bc94-107">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="4bc94-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="4bc94-108">Summary</span></span>

 <span data-ttu-id="4bc94-109">Ses</span><span class="sxs-lookup"><span data-stu-id="4bc94-109">Members</span></span>                        | <span data-ttu-id="4bc94-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="4bc94-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4bc94-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="4bc94-111">Invoke</span></span>](#invoke) | <span data-ttu-id="4bc94-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="4bc94-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="4bc94-113">Utilisez la méthode get_NewVersion de [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) pour obtenir le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="4bc94-113">Use the get_NewVersion method of [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) to get the new version number.</span></span>

## <span data-ttu-id="4bc94-114">Ses</span><span class="sxs-lookup"><span data-stu-id="4bc94-114">Members</span></span>

#### <span data-ttu-id="4bc94-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="4bc94-115">Invoke</span></span> 

<span data-ttu-id="4bc94-116">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="4bc94-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="4bc94-117">[appel](#invoke)HRESULT public ([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="4bc94-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span></span>

