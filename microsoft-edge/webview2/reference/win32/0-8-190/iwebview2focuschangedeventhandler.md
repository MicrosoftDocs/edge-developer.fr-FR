---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 8b7a588122b93cf56f7ce4473db87a0df16522b7
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885995"
---
# <span data-ttu-id="7589d-104">0.8.355-interface IWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="7589d-104">0.8.355 - interface IWebView2FocusChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="7589d-105">L’appelant implémente cette méthode pour recevoir les événements GotFocus et LostFocus.</span><span class="sxs-lookup"><span data-stu-id="7589d-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="7589d-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="7589d-106">Summary</span></span>

 <span data-ttu-id="7589d-107">Ses</span><span class="sxs-lookup"><span data-stu-id="7589d-107">Members</span></span>                        | <span data-ttu-id="7589d-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="7589d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7589d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="7589d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="7589d-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="7589d-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="7589d-111">Il n’existe aucun argument d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="7589d-111">There are no event args for this event.</span></span>

## <span data-ttu-id="7589d-112">Ses</span><span class="sxs-lookup"><span data-stu-id="7589d-112">Members</span></span>

#### <span data-ttu-id="7589d-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="7589d-113">Invoke</span></span> 

<span data-ttu-id="7589d-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="7589d-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="7589d-115">[appel](#invoke)vers un HRESULT public ([IWebView2WebView](IWebView2WebView.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="7589d-115">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="7589d-116">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="7589d-116">There are no event args and the args parameter will be null.</span></span>

