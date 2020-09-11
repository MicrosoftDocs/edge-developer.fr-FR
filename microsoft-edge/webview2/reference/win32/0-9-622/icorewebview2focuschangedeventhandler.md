---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2FocusChangedEventHandler
ms.openlocfilehash: f94e6f8323862d092bf9157061333f5e801db891
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011917"
---
# <span data-ttu-id="0c0eb-104">interface ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="0c0eb-104">interface ICoreWebView2FocusChangedEventHandler</span></span> 

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="0c0eb-105">L’appelant implémente cette méthode pour recevoir les événements GotFocus et LostFocus.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="0c0eb-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="0c0eb-106">Summary</span></span>

 <span data-ttu-id="0c0eb-107">Ses</span><span class="sxs-lookup"><span data-stu-id="0c0eb-107">Members</span></span>                        | <span data-ttu-id="0c0eb-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="0c0eb-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0c0eb-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="0c0eb-109">Invoke</span></span>](#invoke) | <span data-ttu-id="0c0eb-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="0c0eb-111">Il n’existe aucun argument d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-111">There are no event args for this event.</span></span>

## <span data-ttu-id="0c0eb-112">Ses</span><span class="sxs-lookup"><span data-stu-id="0c0eb-112">Members</span></span>

#### <span data-ttu-id="0c0eb-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="0c0eb-113">Invoke</span></span> 

<span data-ttu-id="0c0eb-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="0c0eb-115">[appel](#invoke)de HRESULT public ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="0c0eb-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="0c0eb-116">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-116">There are no event args and the args parameter will be null.</span></span>

