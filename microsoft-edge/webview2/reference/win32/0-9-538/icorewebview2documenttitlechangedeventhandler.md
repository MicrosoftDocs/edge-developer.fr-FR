---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2DocumentTitleChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2DocumentTitleChangedEventHandler
ms.openlocfilehash: 674b97cce835721f3ffa622115d237ef81939a91
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010277"
---
# <span data-ttu-id="feaf7-104">0.9.579-interface ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="feaf7-104">0.9.579 - interface ICoreWebView2DocumentTitleChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="feaf7-105">L’appelant implémente cette interface pour recevoir des événements DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="feaf7-105">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="feaf7-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="feaf7-106">Summary</span></span>

 <span data-ttu-id="feaf7-107">Ses</span><span class="sxs-lookup"><span data-stu-id="feaf7-107">Members</span></span>                        | <span data-ttu-id="feaf7-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="feaf7-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="feaf7-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="feaf7-109">Invoke</span></span>](#invoke) | <span data-ttu-id="feaf7-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="feaf7-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="feaf7-111">Utilisez la propriété DocumentTitle pour obtenir le titre modifié.</span><span class="sxs-lookup"><span data-stu-id="feaf7-111">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="feaf7-112">Ses</span><span class="sxs-lookup"><span data-stu-id="feaf7-112">Members</span></span>

#### <span data-ttu-id="feaf7-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="feaf7-113">Invoke</span></span> 

<span data-ttu-id="feaf7-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="feaf7-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="feaf7-115">[appel](#invoke)de HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="feaf7-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="feaf7-116">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="feaf7-116">There are no event args and the args parameter will be null.</span></span>

