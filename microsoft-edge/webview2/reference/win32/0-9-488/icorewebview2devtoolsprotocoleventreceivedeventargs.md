---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 1397fb15963cadd508082e39a735a8f0f64a8e91
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698070"
---
# <span data-ttu-id="9ef4f-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="9ef4f-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="9ef4f-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="9ef4f-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="9ef4f-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="9ef4f-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="9ef4f-107">Arguments d’événement pour l’événement DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="9ef4f-107">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="9ef4f-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="9ef4f-108">Summary</span></span>

 <span data-ttu-id="9ef4f-109">Ses</span><span class="sxs-lookup"><span data-stu-id="9ef4f-109">Members</span></span>                        | <span data-ttu-id="9ef4f-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="9ef4f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9ef4f-111">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="9ef4f-111">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="9ef4f-112">Objet paramètre de l’événement DevToolsProtocol correspondant représenté sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="9ef4f-112">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="9ef4f-113">Ses</span><span class="sxs-lookup"><span data-stu-id="9ef4f-113">Members</span></span>

#### <span data-ttu-id="9ef4f-114">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="9ef4f-114">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="9ef4f-115">Objet paramètre de l’événement DevToolsProtocol correspondant représenté sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="9ef4f-115">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="9ef4f-116">valeur publique HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="9ef4f-116">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

