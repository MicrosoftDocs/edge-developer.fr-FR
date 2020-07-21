---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: c42e353c80335b6dccdad49b470e68fa5ae2f559
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884252"
---
# <span data-ttu-id="3fd4f-104">0.9.430-interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="3fd4f-104">0.9.430 - interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="3fd4f-105">Arguments d’événement pour l’événement DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="3fd4f-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="3fd4f-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="3fd4f-106">Summary</span></span>

 <span data-ttu-id="3fd4f-107">Ses</span><span class="sxs-lookup"><span data-stu-id="3fd4f-107">Members</span></span>                        | <span data-ttu-id="3fd4f-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="3fd4f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3fd4f-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="3fd4f-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="3fd4f-110">Objet paramètre de l’événement DevToolsProtocol correspondant représenté sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="3fd4f-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="3fd4f-111">Ses</span><span class="sxs-lookup"><span data-stu-id="3fd4f-111">Members</span></span>

#### <span data-ttu-id="3fd4f-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="3fd4f-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="3fd4f-113">Objet paramètre de l’événement DevToolsProtocol correspondant représenté sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="3fd4f-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="3fd4f-114">valeur publique HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="3fd4f-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

