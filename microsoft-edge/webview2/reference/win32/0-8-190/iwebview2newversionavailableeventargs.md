---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2NewVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 4271cc1002de70db2803a5bd6d4be73748bf5bbb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885869"
---
# <span data-ttu-id="bf57a-104">0.8.355-interface IWebView2NewVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="bf57a-104">0.8.355 - interface IWebView2NewVersionAvailableEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NewVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="bf57a-105">Arguments d’événement pour l’événement NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="bf57a-105">Event args for the NewVersionAvailable event.</span></span>

## <span data-ttu-id="bf57a-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="bf57a-106">Summary</span></span>

 <span data-ttu-id="bf57a-107">Ses</span><span class="sxs-lookup"><span data-stu-id="bf57a-107">Members</span></span>                        | <span data-ttu-id="bf57a-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="bf57a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bf57a-109">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="bf57a-109">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="bf57a-110">Les informations de la version du navigateur du [IWebView2Environment](IWebView2Environment.md)actuel.</span><span class="sxs-lookup"><span data-stu-id="bf57a-110">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="bf57a-111">Ses</span><span class="sxs-lookup"><span data-stu-id="bf57a-111">Members</span></span>

#### <span data-ttu-id="bf57a-112">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="bf57a-112">get_NewVersion</span></span> 

<span data-ttu-id="bf57a-113">Les informations de la version du navigateur du [IWebView2Environment](IWebView2Environment.md)actuel.</span><span class="sxs-lookup"><span data-stu-id="bf57a-113">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

> <span data-ttu-id="bf57a-114">valeur publique HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* NewVersion)</span><span class="sxs-lookup"><span data-stu-id="bf57a-114">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>

