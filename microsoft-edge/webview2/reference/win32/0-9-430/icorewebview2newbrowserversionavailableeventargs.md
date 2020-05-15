---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 3ac37f7d90fc03214381b991c8becae602bac738
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653495"
---
# <span data-ttu-id="88375-104">interface ICoreWebView2NewBrowserVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="88375-104">interface ICoreWebView2NewBrowserVersionAvailableEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="88375-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="88375-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="88375-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="88375-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewBrowserVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="88375-107">Arguments d’événement pour l’événement NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="88375-107">Event args for the NewBrowserVersionAvailable event.</span></span>

## <span data-ttu-id="88375-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="88375-108">Summary</span></span>

 <span data-ttu-id="88375-109">Ses</span><span class="sxs-lookup"><span data-stu-id="88375-109">Members</span></span>                        | <span data-ttu-id="88375-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="88375-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="88375-111">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="88375-111">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="88375-112">Les informations de la version du navigateur du [ICoreWebView2Environment](ICoreWebView2Environment.md)actuel.</span><span class="sxs-lookup"><span data-stu-id="88375-112">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

## <span data-ttu-id="88375-113">Ses</span><span class="sxs-lookup"><span data-stu-id="88375-113">Members</span></span>

#### <span data-ttu-id="88375-114">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="88375-114">get_NewVersion</span></span> 

<span data-ttu-id="88375-115">Les informations de la version du navigateur du [ICoreWebView2Environment](ICoreWebView2Environment.md)actuel.</span><span class="sxs-lookup"><span data-stu-id="88375-115">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

> <span data-ttu-id="88375-116">valeur publique HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* NewVersion)</span><span class="sxs-lookup"><span data-stu-id="88375-116">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>

