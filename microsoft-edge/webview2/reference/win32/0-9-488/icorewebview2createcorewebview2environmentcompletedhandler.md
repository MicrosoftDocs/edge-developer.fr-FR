---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: e838c851df54a7af5e4afe6352abef6d1044c8be
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698084"
---
# <span data-ttu-id="c7f91-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="c7f91-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="c7f91-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="c7f91-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="c7f91-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="c7f91-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="c7f91-107">L’appelant implémente cette interface pour recevoir les WebView2Environment créées via CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="c7f91-107">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="c7f91-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="c7f91-108">Summary</span></span>

 <span data-ttu-id="c7f91-109">Ses</span><span class="sxs-lookup"><span data-stu-id="c7f91-109">Members</span></span>                        | <span data-ttu-id="c7f91-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="c7f91-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c7f91-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="c7f91-111">Invoke</span></span>](#invoke) | <span data-ttu-id="c7f91-112">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="c7f91-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="c7f91-113">Ses</span><span class="sxs-lookup"><span data-stu-id="c7f91-113">Members</span></span>

#### <span data-ttu-id="c7f91-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="c7f91-114">Invoke</span></span> 

<span data-ttu-id="c7f91-115">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="c7f91-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="c7f91-116">[appel](#invoke)HRESULT public (résultat HRESULT, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="c7f91-116">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span></span>

