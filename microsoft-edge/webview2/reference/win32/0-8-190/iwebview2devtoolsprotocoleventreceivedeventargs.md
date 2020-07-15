---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 0df2ea043a95c8cca24c0b9bbe3091c490b4ea3d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878602"
---
# <span data-ttu-id="54af4-104">0.8.355-interface IWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="54af4-104">0.8.355 - interface IWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="54af4-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="54af4-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="54af4-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="54af4-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="54af4-107">Arguments d’événement pour l’événement DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="54af4-107">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="54af4-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="54af4-108">Summary</span></span>

 <span data-ttu-id="54af4-109">Ses</span><span class="sxs-lookup"><span data-stu-id="54af4-109">Members</span></span>                        | <span data-ttu-id="54af4-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="54af4-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="54af4-111">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="54af4-111">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="54af4-112">Objet paramètre de l’événement DevToolsProtocol correspondant représenté sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="54af4-112">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="54af4-113">Ses</span><span class="sxs-lookup"><span data-stu-id="54af4-113">Members</span></span>

#### <span data-ttu-id="54af4-114">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="54af4-114">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="54af4-115">Objet paramètre de l’événement DevToolsProtocol correspondant représenté sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="54af4-115">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="54af4-116">valeur publique HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="54af4-116">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

