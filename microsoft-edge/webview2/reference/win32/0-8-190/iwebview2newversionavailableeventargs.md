---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2NewVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: e8965ebe2e0434d83b4d6e8eabe74466adb7cec6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878343"
---
# <span data-ttu-id="7a8b4-104">0.8.355-interface IWebView2NewVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="7a8b4-104">0.8.355 - interface IWebView2NewVersionAvailableEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="7a8b4-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="7a8b4-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="7a8b4-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="7a8b4-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NewVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="7a8b4-107">Arguments d’événement pour l’événement NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="7a8b4-107">Event args for the NewVersionAvailable event.</span></span>

## <span data-ttu-id="7a8b4-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="7a8b4-108">Summary</span></span>

 <span data-ttu-id="7a8b4-109">Ses</span><span class="sxs-lookup"><span data-stu-id="7a8b4-109">Members</span></span>                        | <span data-ttu-id="7a8b4-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="7a8b4-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7a8b4-111">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="7a8b4-111">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="7a8b4-112">Les informations de la version du navigateur du [IWebView2Environment](IWebView2Environment.md)actuel.</span><span class="sxs-lookup"><span data-stu-id="7a8b4-112">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="7a8b4-113">Ses</span><span class="sxs-lookup"><span data-stu-id="7a8b4-113">Members</span></span>

#### <span data-ttu-id="7a8b4-114">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="7a8b4-114">get_NewVersion</span></span> 

<span data-ttu-id="7a8b4-115">Les informations de la version du navigateur du [IWebView2Environment](IWebView2Environment.md)actuel.</span><span class="sxs-lookup"><span data-stu-id="7a8b4-115">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

> <span data-ttu-id="7a8b4-116">valeur publique HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* NewVersion)</span><span class="sxs-lookup"><span data-stu-id="7a8b4-116">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>

