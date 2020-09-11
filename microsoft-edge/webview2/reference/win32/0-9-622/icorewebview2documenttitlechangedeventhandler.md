---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2DocumentTitleChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2DocumentTitleChangedEventHandler
ms.openlocfilehash: 9332786935ba79adfd6ef215c9e11afa24c5ceb2
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011813"
---
# <span data-ttu-id="ce7f0-104">interface ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ce7f0-104">interface ICoreWebView2DocumentTitleChangedEventHandler</span></span> 

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="ce7f0-105">L’appelant implémente cette interface pour recevoir des événements DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-105">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="ce7f0-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="ce7f0-106">Summary</span></span>

 <span data-ttu-id="ce7f0-107">Ses</span><span class="sxs-lookup"><span data-stu-id="ce7f0-107">Members</span></span>                        | <span data-ttu-id="ce7f0-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="ce7f0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ce7f0-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="ce7f0-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ce7f0-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="ce7f0-111">Utilisez la propriété DocumentTitle pour obtenir le titre modifié.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-111">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="ce7f0-112">Ses</span><span class="sxs-lookup"><span data-stu-id="ce7f0-112">Members</span></span>

#### <span data-ttu-id="ce7f0-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="ce7f0-113">Invoke</span></span> 

<span data-ttu-id="ce7f0-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ce7f0-115">[appel](#invoke)de HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="ce7f0-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="ce7f0-116">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-116">There are no event args and the args parameter will be null.</span></span>

