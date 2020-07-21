---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2DocumentTitleChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 0dc9886bc2282d08855ccb40cb8b06b4ffadb659
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886111"
---
# <span data-ttu-id="9d275-104">0.8.355-interface IWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="9d275-104">0.8.355 - interface IWebView2DocumentTitleChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="9d275-105">L’appelant implémente cette interface pour recevoir des événements DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="9d275-105">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="9d275-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="9d275-106">Summary</span></span>

 <span data-ttu-id="9d275-107">Ses</span><span class="sxs-lookup"><span data-stu-id="9d275-107">Members</span></span>                        | <span data-ttu-id="9d275-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="9d275-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9d275-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="9d275-109">Invoke</span></span>](#invoke) | <span data-ttu-id="9d275-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="9d275-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="9d275-111">Utilisez la propriété DocumentTitle pour obtenir le titre modifié.</span><span class="sxs-lookup"><span data-stu-id="9d275-111">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="9d275-112">Ses</span><span class="sxs-lookup"><span data-stu-id="9d275-112">Members</span></span>

#### <span data-ttu-id="9d275-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="9d275-113">Invoke</span></span> 

<span data-ttu-id="9d275-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="9d275-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="9d275-115">[appel](#invoke)vers un HRESULT public ([IWebView2WebView3](IWebView2WebView3.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="9d275-115">public HRESULT [Invoke](#invoke)([IWebView2WebView3](IWebView2WebView3.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="9d275-116">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="9d275-116">There are no event args and the args parameter will be null.</span></span>

