---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2Environment2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: e3177f159ff397ee9d4781936aa32f2715d4af02
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886086"
---
# <span data-ttu-id="26b46-104">0.8.355-interface IWebView2Environment2</span><span class="sxs-lookup"><span data-stu-id="26b46-104">0.8.355 - interface IWebView2Environment2</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Environment2
  : public IWebView2Environment
```

<span data-ttu-id="26b46-105">Fonctionnalités supplémentaires implémentées par l’objet Environment.</span><span class="sxs-lookup"><span data-stu-id="26b46-105">Additional functionality implemented by the Environment object.</span></span>

## <span data-ttu-id="26b46-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="26b46-106">Summary</span></span>

 <span data-ttu-id="26b46-107">Ses</span><span class="sxs-lookup"><span data-stu-id="26b46-107">Members</span></span>                        | <span data-ttu-id="26b46-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="26b46-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="26b46-109">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="26b46-109">get_BrowserVersionInfo</span></span>](#get_browserversioninfo) | <span data-ttu-id="26b46-110">Les informations de la version du navigateur du [IWebView2Environment](IWebView2Environment.md)actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.</span><span class="sxs-lookup"><span data-stu-id="26b46-110">The browser version info of the current [IWebView2Environment](IWebView2Environment.md), including channel name if it is not the stable channel.</span></span>

<span data-ttu-id="26b46-111">Pour plus d’informations, consultez l’interface [IWebView2Environment](IWebView2Environment.md) .</span><span class="sxs-lookup"><span data-stu-id="26b46-111">See the [IWebView2Environment](IWebView2Environment.md) interface for more details.</span></span> <span data-ttu-id="26b46-112">Vous pouvez QueryInterface pour cette interface à partir de l’objet qui implémente [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="26b46-112">You can QueryInterface for this interface from the object that implements [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="26b46-113">Ses</span><span class="sxs-lookup"><span data-stu-id="26b46-113">Members</span></span>

#### <span data-ttu-id="26b46-114">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="26b46-114">get_BrowserVersionInfo</span></span> 

<span data-ttu-id="26b46-115">Les informations de la version du navigateur du [IWebView2Environment](IWebView2Environment.md)actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.</span><span class="sxs-lookup"><span data-stu-id="26b46-115">The browser version info of the current [IWebView2Environment](IWebView2Environment.md), including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="26b46-116">valeur publique HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* VERSIONINFO)</span><span class="sxs-lookup"><span data-stu-id="26b46-116">public HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="26b46-117">Il correspond au format de l’API GetWebView2BrowserVersionInfo.</span><span class="sxs-lookup"><span data-stu-id="26b46-117">This matches the format of the GetWebView2BrowserVersionInfo API.</span></span> <span data-ttu-id="26b46-118">Les noms de canaux sont «bêta», «dev» et «Canaries».</span><span class="sxs-lookup"><span data-stu-id="26b46-118">Channel names are 'beta', 'dev', and 'canary'.</span></span>

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionInfo(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

