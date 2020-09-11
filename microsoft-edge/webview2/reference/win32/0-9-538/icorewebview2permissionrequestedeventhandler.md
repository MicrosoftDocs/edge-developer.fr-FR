---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2PermissionRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2PermissionRequestedEventHandler
ms.openlocfilehash: 809524e55a610dcd157860cfa9ed88f86ee63dca
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010039"
---
# <span data-ttu-id="f225f-104">0.9.579-interface ICoreWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f225f-104">0.9.579 - interface ICoreWebView2PermissionRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="f225f-105">L’appelant implémente cette interface pour recevoir l’événement PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="f225f-105">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="f225f-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="f225f-106">Summary</span></span>

 <span data-ttu-id="f225f-107">Ses</span><span class="sxs-lookup"><span data-stu-id="f225f-107">Members</span></span>                        | <span data-ttu-id="f225f-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="f225f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f225f-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="f225f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f225f-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="f225f-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="f225f-111">Ses</span><span class="sxs-lookup"><span data-stu-id="f225f-111">Members</span></span>

#### <span data-ttu-id="f225f-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="f225f-112">Invoke</span></span> 

<span data-ttu-id="f225f-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="f225f-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f225f-114">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="f225f-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span></span>

