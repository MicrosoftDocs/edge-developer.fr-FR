---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2NewVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 3a9af31477e7b4155bece55ec2faef85efccbd0d
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884980"
---
# <span data-ttu-id="eb9ab-104">0.8.355-interface IWebView2NewVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="eb9ab-104">0.8.355 - interface IWebView2NewVersionAvailableEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NewVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="eb9ab-105">L’appelant implémente cette interface pour recevoir des événements NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="eb9ab-105">The caller implements this interface to receive NewVersionAvailable events.</span></span>

## <span data-ttu-id="eb9ab-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="eb9ab-106">Summary</span></span>

 <span data-ttu-id="eb9ab-107">Ses</span><span class="sxs-lookup"><span data-stu-id="eb9ab-107">Members</span></span>                        | <span data-ttu-id="eb9ab-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="eb9ab-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="eb9ab-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="eb9ab-109">Invoke</span></span>](#invoke) | <span data-ttu-id="eb9ab-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="eb9ab-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="eb9ab-111">Utilisez la méthode get_NewVersion de [IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) pour obtenir le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="eb9ab-111">Use the get_NewVersion method of [IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) to get the new version number.</span></span>

## <span data-ttu-id="eb9ab-112">Ses</span><span class="sxs-lookup"><span data-stu-id="eb9ab-112">Members</span></span>

#### <span data-ttu-id="eb9ab-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="eb9ab-113">Invoke</span></span> 

<span data-ttu-id="eb9ab-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="eb9ab-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="eb9ab-115">[appel](#invoke)HRESULT public ([IWebView2Environment](IWebView2Environment.md) \* webviewEnvironment,[IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="eb9ab-115">public HRESULT [Invoke](#invoke)([IWebView2Environment](IWebView2Environment.md) \* webviewEnvironment,[IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) \* args)</span></span>

