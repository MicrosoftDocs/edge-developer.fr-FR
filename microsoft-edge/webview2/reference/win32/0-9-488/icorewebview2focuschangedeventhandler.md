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
ms.openlocfilehash: e80dca6411534968822d9994f9911828a4fddeeb
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653485"
---
# <span data-ttu-id="61bf4-104">interface ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="61bf4-104">interface ICoreWebView2FocusChangedEventHandler</span></span> 

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="61bf4-105">L’appelant implémente cette méthode pour recevoir les événements GotFocus et LostFocus.</span><span class="sxs-lookup"><span data-stu-id="61bf4-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="61bf4-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="61bf4-106">Summary</span></span>

 <span data-ttu-id="61bf4-107">Ses</span><span class="sxs-lookup"><span data-stu-id="61bf4-107">Members</span></span>                        | <span data-ttu-id="61bf4-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="61bf4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="61bf4-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="61bf4-109">Invoke</span></span>](#invoke) | <span data-ttu-id="61bf4-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="61bf4-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="61bf4-111">Il n’existe aucun argument d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="61bf4-111">There are no event args for this event.</span></span>

## <span data-ttu-id="61bf4-112">Ses</span><span class="sxs-lookup"><span data-stu-id="61bf4-112">Members</span></span>

#### <span data-ttu-id="61bf4-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="61bf4-113">Invoke</span></span> 

<span data-ttu-id="61bf4-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="61bf4-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="61bf4-115">[appel](#invoke)de HRESULT public ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="61bf4-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="61bf4-116">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="61bf4-116">There are no event args and the args parameter will be null.</span></span>

