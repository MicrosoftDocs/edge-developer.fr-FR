---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2Environment2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: d127af61bfdc9bf692fa48489d7982bf2c6cad86
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878546"
---
# <span data-ttu-id="d633b-104">0.8.355-interface IWebView2Environment2</span><span class="sxs-lookup"><span data-stu-id="d633b-104">0.8.355 - interface IWebView2Environment2</span></span> 

> [!NOTE]
> <span data-ttu-id="d633b-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="d633b-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="d633b-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="d633b-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Environment2
  : public IWebView2Environment
```

<span data-ttu-id="d633b-107">Fonctionnalités supplémentaires implémentées par l’objet Environment.</span><span class="sxs-lookup"><span data-stu-id="d633b-107">Additional functionality implemented by the Environment object.</span></span>

## <span data-ttu-id="d633b-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="d633b-108">Summary</span></span>

 <span data-ttu-id="d633b-109">Ses</span><span class="sxs-lookup"><span data-stu-id="d633b-109">Members</span></span>                        | <span data-ttu-id="d633b-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="d633b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d633b-111">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d633b-111">get_BrowserVersionInfo</span></span>](#get_browserversioninfo) | <span data-ttu-id="d633b-112">Les informations de la version du navigateur du [IWebView2Environment](IWebView2Environment.md)actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.</span><span class="sxs-lookup"><span data-stu-id="d633b-112">The browser version info of the current [IWebView2Environment](IWebView2Environment.md), including channel name if it is not the stable channel.</span></span>

<span data-ttu-id="d633b-113">Pour plus d’informations, consultez l’interface [IWebView2Environment](IWebView2Environment.md) .</span><span class="sxs-lookup"><span data-stu-id="d633b-113">See the [IWebView2Environment](IWebView2Environment.md) interface for more details.</span></span> <span data-ttu-id="d633b-114">Vous pouvez QueryInterface pour cette interface à partir de l’objet qui implémente [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="d633b-114">You can QueryInterface for this interface from the object that implements [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="d633b-115">Ses</span><span class="sxs-lookup"><span data-stu-id="d633b-115">Members</span></span>

#### <span data-ttu-id="d633b-116">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d633b-116">get_BrowserVersionInfo</span></span> 

<span data-ttu-id="d633b-117">Les informations de la version du navigateur du [IWebView2Environment](IWebView2Environment.md)actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.</span><span class="sxs-lookup"><span data-stu-id="d633b-117">The browser version info of the current [IWebView2Environment](IWebView2Environment.md), including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="d633b-118">valeur publique HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* VERSIONINFO)</span><span class="sxs-lookup"><span data-stu-id="d633b-118">public HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="d633b-119">Il correspond au format de l’API GetWebView2BrowserVersionInfo.</span><span class="sxs-lookup"><span data-stu-id="d633b-119">This matches the format of the GetWebView2BrowserVersionInfo API.</span></span> <span data-ttu-id="d633b-120">Les noms de canaux sont «bêta», «dev» et «Canaries».</span><span class="sxs-lookup"><span data-stu-id="d633b-120">Channel names are 'beta', 'dev', and 'canary'.</span></span>

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionInfo(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

