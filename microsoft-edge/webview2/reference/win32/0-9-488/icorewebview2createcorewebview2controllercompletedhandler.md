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
ms.openlocfilehash: 0fb633a45df15c5b5116d69f74f6d12894bc91c1
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698091"
---
# <span data-ttu-id="81c27-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="81c27-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="81c27-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="81c27-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="81c27-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="81c27-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="81c27-107">L’appelant implémente cette interface pour recevoir les CoreWebView2Controller créées via CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="81c27-107">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="81c27-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="81c27-108">Summary</span></span>

 <span data-ttu-id="81c27-109">Ses</span><span class="sxs-lookup"><span data-stu-id="81c27-109">Members</span></span>                        | <span data-ttu-id="81c27-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="81c27-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="81c27-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="81c27-111">Invoke</span></span>](#invoke) | <span data-ttu-id="81c27-112">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="81c27-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="81c27-113">Ses</span><span class="sxs-lookup"><span data-stu-id="81c27-113">Members</span></span>

#### <span data-ttu-id="81c27-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="81c27-114">Invoke</span></span> 

<span data-ttu-id="81c27-115">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="81c27-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="81c27-116">[appel](#invoke)HRESULT public (résultat HRESULT, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="81c27-116">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>

