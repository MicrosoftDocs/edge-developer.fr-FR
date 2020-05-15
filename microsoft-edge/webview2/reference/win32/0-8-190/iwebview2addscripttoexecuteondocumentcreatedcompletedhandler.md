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
ms.openlocfilehash: 262add6a545f5bac53021dfe1970df1c73e7d758
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653638"
---
# <span data-ttu-id="4d924-104">interface IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="4d924-104">interface IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="4d924-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="4d924-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="4d924-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="4d924-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="4d924-107">L’appelant implémente cette interface pour recevoir le résultat de la méthode AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="4d924-107">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="4d924-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="4d924-108">Summary</span></span>

 <span data-ttu-id="4d924-109">Ses</span><span class="sxs-lookup"><span data-stu-id="4d924-109">Members</span></span>                        | <span data-ttu-id="4d924-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="4d924-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4d924-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="4d924-111">Invoke</span></span>](#invoke) | <span data-ttu-id="4d924-112">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="4d924-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="4d924-113">Ses</span><span class="sxs-lookup"><span data-stu-id="4d924-113">Members</span></span>

#### <span data-ttu-id="4d924-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="4d924-114">Invoke</span></span> 

<span data-ttu-id="4d924-115">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="4d924-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="4d924-116">[appel](#invoke)HRESULT public (HRESULT codeerreur, ID LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="4d924-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR id)</span></span>

