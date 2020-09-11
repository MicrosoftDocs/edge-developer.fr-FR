---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
ms.openlocfilehash: 1580f119a83a171f304b7b05ecbc88edfe31e26d
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011964"
---
# <span data-ttu-id="66818-104">interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="66818-104">interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

```
interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="66818-105">L’appelant implémente cette interface pour recevoir le résultat de la méthode AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="66818-105">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="66818-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="66818-106">Summary</span></span>

 <span data-ttu-id="66818-107">Ses</span><span class="sxs-lookup"><span data-stu-id="66818-107">Members</span></span>                        | <span data-ttu-id="66818-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="66818-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="66818-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="66818-109">Invoke</span></span>](#invoke) | <span data-ttu-id="66818-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="66818-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="66818-111">Ses</span><span class="sxs-lookup"><span data-stu-id="66818-111">Members</span></span>

#### <span data-ttu-id="66818-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="66818-112">Invoke</span></span> 

<span data-ttu-id="66818-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="66818-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="66818-114">[appel](#invoke)HRESULT public (HRESULT codeerreur, ID LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="66818-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR id)</span></span>

