---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2NewBrowserVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: f59b5acac510b66eae0e1ada51e28b6dd9363ca8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877853"
---
# <span data-ttu-id="c15b6-104">0.9.430-interface ICoreWebView2NewBrowserVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="c15b6-104">0.9.430 - interface ICoreWebView2NewBrowserVersionAvailableEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="c15b6-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="c15b6-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="c15b6-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="c15b6-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewBrowserVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="c15b6-107">Arguments d’événement pour l’événement NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="c15b6-107">Event args for the NewBrowserVersionAvailable event.</span></span>

## <span data-ttu-id="c15b6-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="c15b6-108">Summary</span></span>

 <span data-ttu-id="c15b6-109">Ses</span><span class="sxs-lookup"><span data-stu-id="c15b6-109">Members</span></span>                        | <span data-ttu-id="c15b6-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="c15b6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c15b6-111">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="c15b6-111">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="c15b6-112">Les informations de la version du navigateur du [ICoreWebView2Environment](ICoreWebView2Environment.md)actuel.</span><span class="sxs-lookup"><span data-stu-id="c15b6-112">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

## <span data-ttu-id="c15b6-113">Ses</span><span class="sxs-lookup"><span data-stu-id="c15b6-113">Members</span></span>

#### <span data-ttu-id="c15b6-114">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="c15b6-114">get_NewVersion</span></span> 

<span data-ttu-id="c15b6-115">Les informations de la version du navigateur du [ICoreWebView2Environment](ICoreWebView2Environment.md)actuel.</span><span class="sxs-lookup"><span data-stu-id="c15b6-115">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

> <span data-ttu-id="c15b6-116">valeur publique HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* NewVersion)</span><span class="sxs-lookup"><span data-stu-id="c15b6-116">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>

