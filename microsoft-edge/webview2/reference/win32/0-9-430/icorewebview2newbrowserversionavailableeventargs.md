---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2NewBrowserVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 9f56ba33534c76cb1bd60c01a88eedfced45f1fb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884861"
---
# <span data-ttu-id="e7d7f-104">0.9.430-interface ICoreWebView2NewBrowserVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="e7d7f-104">0.9.430 - interface ICoreWebView2NewBrowserVersionAvailableEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewBrowserVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="e7d7f-105">Arguments d’événement pour l’événement NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="e7d7f-105">Event args for the NewBrowserVersionAvailable event.</span></span>

## <span data-ttu-id="e7d7f-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="e7d7f-106">Summary</span></span>

 <span data-ttu-id="e7d7f-107">Ses</span><span class="sxs-lookup"><span data-stu-id="e7d7f-107">Members</span></span>                        | <span data-ttu-id="e7d7f-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="e7d7f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e7d7f-109">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="e7d7f-109">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="e7d7f-110">Les informations de la version du navigateur du [ICoreWebView2Environment](ICoreWebView2Environment.md)actuel.</span><span class="sxs-lookup"><span data-stu-id="e7d7f-110">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

## <span data-ttu-id="e7d7f-111">Ses</span><span class="sxs-lookup"><span data-stu-id="e7d7f-111">Members</span></span>

#### <span data-ttu-id="e7d7f-112">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="e7d7f-112">get_NewVersion</span></span> 

<span data-ttu-id="e7d7f-113">Les informations de la version du navigateur du [ICoreWebView2Environment](ICoreWebView2Environment.md)actuel.</span><span class="sxs-lookup"><span data-stu-id="e7d7f-113">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

> <span data-ttu-id="e7d7f-114">valeur publique HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* NewVersion)</span><span class="sxs-lookup"><span data-stu-id="e7d7f-114">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>

