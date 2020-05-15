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
ms.openlocfilehash: cf321ff1091883827b7ce6cda7248a06f1128867
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653506"
---
# <span data-ttu-id="c189d-104">interface IWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="c189d-104">interface IWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="c189d-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="c189d-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="c189d-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="c189d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="c189d-107">Arguments d’événement pour l’événement DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="c189d-107">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="c189d-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="c189d-108">Summary</span></span>

 <span data-ttu-id="c189d-109">Ses</span><span class="sxs-lookup"><span data-stu-id="c189d-109">Members</span></span>                        | <span data-ttu-id="c189d-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="c189d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c189d-111">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="c189d-111">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="c189d-112">Objet paramètre de l’événement DevToolsProtocol correspondant représenté sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="c189d-112">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="c189d-113">Ses</span><span class="sxs-lookup"><span data-stu-id="c189d-113">Members</span></span>

#### <span data-ttu-id="c189d-114">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="c189d-114">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="c189d-115">Objet paramètre de l’événement DevToolsProtocol correspondant représenté sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="c189d-115">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="c189d-116">valeur publique HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="c189d-116">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

