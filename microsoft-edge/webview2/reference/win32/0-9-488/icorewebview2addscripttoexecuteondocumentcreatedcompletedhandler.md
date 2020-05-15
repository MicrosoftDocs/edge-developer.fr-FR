---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: e9f98b43463fe5259d2f9f723b62b78c1d1a4758
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653554"
---
# <span data-ttu-id="b7943-104">interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="b7943-104">interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

```
interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="b7943-105">L’appelant implémente cette interface pour recevoir le résultat de la méthode AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="b7943-105">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="b7943-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="b7943-106">Summary</span></span>

 <span data-ttu-id="b7943-107">Ses</span><span class="sxs-lookup"><span data-stu-id="b7943-107">Members</span></span>                        | <span data-ttu-id="b7943-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="b7943-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b7943-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b7943-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b7943-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="b7943-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="b7943-111">Ses</span><span class="sxs-lookup"><span data-stu-id="b7943-111">Members</span></span>

#### <span data-ttu-id="b7943-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="b7943-112">Invoke</span></span> 

<span data-ttu-id="b7943-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="b7943-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="b7943-114">[appel](#invoke)HRESULT public (HRESULT codeerreur, ID LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="b7943-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR id)</span></span>

