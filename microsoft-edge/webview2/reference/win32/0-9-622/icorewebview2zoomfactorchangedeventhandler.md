---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ZoomFactorChangedEventHandler
ms.openlocfilehash: 116679e5b4168803af1c7e2909eb590af2378623
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011923"
---
# <span data-ttu-id="2295f-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2295f-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="2295f-105">L’appelant implémente cette interface pour recevoir des événements ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="2295f-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="2295f-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="2295f-106">Summary</span></span>

 <span data-ttu-id="2295f-107">Ses</span><span class="sxs-lookup"><span data-stu-id="2295f-107">Members</span></span>                        | <span data-ttu-id="2295f-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="2295f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2295f-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="2295f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="2295f-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="2295f-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="2295f-111">Utilisez la propriété ICoreWebView2Controller. ZoomFactor pour obtenir le facteur de zoom modifié.</span><span class="sxs-lookup"><span data-stu-id="2295f-111">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="2295f-112">Ses</span><span class="sxs-lookup"><span data-stu-id="2295f-112">Members</span></span>

#### <span data-ttu-id="2295f-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="2295f-113">Invoke</span></span> 

<span data-ttu-id="2295f-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="2295f-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="2295f-115">[appel](#invoke)de HRESULT public (ICoreWebView2Controller \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="2295f-115">public HRESULT [Invoke](#invoke)(ICoreWebView2Controller \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="2295f-116">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="2295f-116">There are no event args and the args parameter will be null.</span></span>

