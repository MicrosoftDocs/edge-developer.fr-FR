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
ms.openlocfilehash: ec48b8659a5778b7f552695ee511b5af61d38d9c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653450"
---
# <span data-ttu-id="8a2ce-104">interface ICoreWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8a2ce-104">interface ICoreWebView2PermissionRequestedEventHandler</span></span> 

```
interface ICoreWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="8a2ce-105">L’appelant implémente cette interface pour recevoir l’événement PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="8a2ce-105">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="8a2ce-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="8a2ce-106">Summary</span></span>

 <span data-ttu-id="8a2ce-107">Ses</span><span class="sxs-lookup"><span data-stu-id="8a2ce-107">Members</span></span>                        | <span data-ttu-id="8a2ce-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="8a2ce-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8a2ce-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="8a2ce-109">Invoke</span></span>](#invoke) | <span data-ttu-id="8a2ce-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="8a2ce-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="8a2ce-111">Ses</span><span class="sxs-lookup"><span data-stu-id="8a2ce-111">Members</span></span>

#### <span data-ttu-id="8a2ce-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="8a2ce-112">Invoke</span></span> 

<span data-ttu-id="8a2ce-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="8a2ce-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="8a2ce-114">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="8a2ce-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span></span>

