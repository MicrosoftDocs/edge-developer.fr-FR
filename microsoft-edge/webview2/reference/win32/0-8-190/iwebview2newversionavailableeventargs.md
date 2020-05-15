---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 0314c796865d3d745b831d050498f59868e38e8f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653594"
---
# <span data-ttu-id="09176-104">interface IWebView2NewVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="09176-104">interface IWebView2NewVersionAvailableEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="09176-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="09176-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="09176-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="09176-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NewVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="09176-107">Arguments d’événement pour l’événement NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="09176-107">Event args for the NewVersionAvailable event.</span></span>

## <span data-ttu-id="09176-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="09176-108">Summary</span></span>

 <span data-ttu-id="09176-109">Ses</span><span class="sxs-lookup"><span data-stu-id="09176-109">Members</span></span>                        | <span data-ttu-id="09176-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="09176-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="09176-111">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="09176-111">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="09176-112">Les informations de la version du navigateur du [IWebView2Environment](IWebView2Environment.md)actuel.</span><span class="sxs-lookup"><span data-stu-id="09176-112">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="09176-113">Ses</span><span class="sxs-lookup"><span data-stu-id="09176-113">Members</span></span>

#### <span data-ttu-id="09176-114">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="09176-114">get_NewVersion</span></span> 

<span data-ttu-id="09176-115">Les informations de la version du navigateur du [IWebView2Environment](IWebView2Environment.md)actuel.</span><span class="sxs-lookup"><span data-stu-id="09176-115">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

> <span data-ttu-id="09176-116">valeur publique HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* NewVersion)</span><span class="sxs-lookup"><span data-stu-id="09176-116">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>

