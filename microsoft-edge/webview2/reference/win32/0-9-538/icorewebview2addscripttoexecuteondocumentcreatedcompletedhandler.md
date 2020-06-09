---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 9777a27c1b9252d0d1a5f91a4692b9043fffc569
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698669"
---
# <span data-ttu-id="7a88c-104">interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="7a88c-104">interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

```
interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="7a88c-105">L’appelant implémente cette interface pour recevoir le résultat de la méthode AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="7a88c-105">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="7a88c-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="7a88c-106">Summary</span></span>

 <span data-ttu-id="7a88c-107">Ses</span><span class="sxs-lookup"><span data-stu-id="7a88c-107">Members</span></span>                        | <span data-ttu-id="7a88c-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="7a88c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7a88c-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="7a88c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="7a88c-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="7a88c-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="7a88c-111">Ses</span><span class="sxs-lookup"><span data-stu-id="7a88c-111">Members</span></span>

#### <span data-ttu-id="7a88c-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="7a88c-112">Invoke</span></span> 

<span data-ttu-id="7a88c-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="7a88c-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="7a88c-114">[appel](#invoke)HRESULT public (HRESULT codeerreur, ID LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="7a88c-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR id)</span></span>

