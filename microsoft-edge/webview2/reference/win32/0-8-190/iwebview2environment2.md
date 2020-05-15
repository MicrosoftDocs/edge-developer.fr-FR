---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 00b19d1174a5d5ac643a04038ecdd60c82211194
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653512"
---
# <span data-ttu-id="2f2eb-104">interface IWebView2Environment2</span><span class="sxs-lookup"><span data-stu-id="2f2eb-104">interface IWebView2Environment2</span></span> 

> [!NOTE]
> <span data-ttu-id="2f2eb-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="2f2eb-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="2f2eb-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="2f2eb-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Environment2
  : public IWebView2Environment
```

<span data-ttu-id="2f2eb-107">Fonctionnalités supplémentaires implémentées par l’objet Environment.</span><span class="sxs-lookup"><span data-stu-id="2f2eb-107">Additional functionality implemented by the Environment object.</span></span>

## <span data-ttu-id="2f2eb-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="2f2eb-108">Summary</span></span>

 <span data-ttu-id="2f2eb-109">Ses</span><span class="sxs-lookup"><span data-stu-id="2f2eb-109">Members</span></span>                        | <span data-ttu-id="2f2eb-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="2f2eb-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2f2eb-111">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="2f2eb-111">get_BrowserVersionInfo</span></span>](#get_browserversioninfo) | <span data-ttu-id="2f2eb-112">Les informations de la version du navigateur du [IWebView2Environment](IWebView2Environment.md)actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.</span><span class="sxs-lookup"><span data-stu-id="2f2eb-112">The browser version info of the current [IWebView2Environment](IWebView2Environment.md), including channel name if it is not the stable channel.</span></span>

<span data-ttu-id="2f2eb-113">Pour plus d’informations, consultez l’interface [IWebView2Environment](IWebView2Environment.md) .</span><span class="sxs-lookup"><span data-stu-id="2f2eb-113">See the [IWebView2Environment](IWebView2Environment.md) interface for more details.</span></span> <span data-ttu-id="2f2eb-114">Vous pouvez QueryInterface pour cette interface à partir de l’objet qui implémente [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="2f2eb-114">You can QueryInterface for this interface from the object that implements [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="2f2eb-115">Ses</span><span class="sxs-lookup"><span data-stu-id="2f2eb-115">Members</span></span>

#### <span data-ttu-id="2f2eb-116">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="2f2eb-116">get_BrowserVersionInfo</span></span> 

<span data-ttu-id="2f2eb-117">Les informations de la version du navigateur du [IWebView2Environment](IWebView2Environment.md)actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.</span><span class="sxs-lookup"><span data-stu-id="2f2eb-117">The browser version info of the current [IWebView2Environment](IWebView2Environment.md), including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="2f2eb-118">valeur publique HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* VERSIONINFO)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-118">public HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="2f2eb-119">Il correspond au format de l’API GetWebView2BrowserVersionInfo.</span><span class="sxs-lookup"><span data-stu-id="2f2eb-119">This matches the format of the GetWebView2BrowserVersionInfo API.</span></span> <span data-ttu-id="2f2eb-120">Les noms de canaux sont «bêta», «dev» et «Canaries».</span><span class="sxs-lookup"><span data-stu-id="2f2eb-120">Channel names are 'beta', 'dev', and 'canary'.</span></span>

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionInfo(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

