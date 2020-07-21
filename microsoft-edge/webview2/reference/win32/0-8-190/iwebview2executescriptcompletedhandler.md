---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 9a075cf5e5d3e5222e76b9ba7550636a67e5696a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886009"
---
# <span data-ttu-id="44a06-104">0.8.355-interface IWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="44a06-104">0.8.355 - interface IWebView2ExecuteScriptCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="44a06-105">L’appelant implémente cette interface pour recevoir le résultat de la méthode ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="44a06-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="44a06-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="44a06-106">Summary</span></span>

 <span data-ttu-id="44a06-107">Ses</span><span class="sxs-lookup"><span data-stu-id="44a06-107">Members</span></span>                        | <span data-ttu-id="44a06-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="44a06-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="44a06-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="44a06-109">Invoke</span></span>](#invoke) | <span data-ttu-id="44a06-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="44a06-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="44a06-111">Ses</span><span class="sxs-lookup"><span data-stu-id="44a06-111">Members</span></span>

#### <span data-ttu-id="44a06-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="44a06-112">Invoke</span></span> 

<span data-ttu-id="44a06-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="44a06-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="44a06-114">[appel](#invoke)HRESULT public (HRESULT CODEERREUR, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="44a06-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR resultObjectAsJson)</span></span>

