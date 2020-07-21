---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2DocumentTitleChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 77cf5ffce5eb6fbb6d310968c998a3f65c08b11a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884217"
---
# <span data-ttu-id="6bb9e-104">0.9.430-interface ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="6bb9e-104">0.9.430 - interface ICoreWebView2DocumentTitleChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="6bb9e-105">L’appelant implémente cette interface pour recevoir des événements DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="6bb9e-105">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="6bb9e-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="6bb9e-106">Summary</span></span>

 <span data-ttu-id="6bb9e-107">Ses</span><span class="sxs-lookup"><span data-stu-id="6bb9e-107">Members</span></span>                        | <span data-ttu-id="6bb9e-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="6bb9e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6bb9e-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="6bb9e-109">Invoke</span></span>](#invoke) | <span data-ttu-id="6bb9e-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="6bb9e-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="6bb9e-111">Utilisez la propriété DocumentTitle pour obtenir le titre modifié.</span><span class="sxs-lookup"><span data-stu-id="6bb9e-111">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="6bb9e-112">Ses</span><span class="sxs-lookup"><span data-stu-id="6bb9e-112">Members</span></span>

#### <span data-ttu-id="6bb9e-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="6bb9e-113">Invoke</span></span> 

<span data-ttu-id="6bb9e-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="6bb9e-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="6bb9e-115">[appel](#invoke)de HRESULT public ([ICoreWebView2](ICoreWebView2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="6bb9e-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="6bb9e-116">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="6bb9e-116">There are no event args and the args parameter will be null.</span></span>

