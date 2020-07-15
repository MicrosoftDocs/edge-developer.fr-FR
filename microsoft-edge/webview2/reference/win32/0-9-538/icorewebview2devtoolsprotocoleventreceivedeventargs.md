---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2DevToolsProtocolEventReceivedEventArgs
ms.openlocfilehash: de10adbfe7e74a1679aa8b77cb96775561d87a17
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880128"
---
# <span data-ttu-id="e4196-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e4196-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="e4196-105">Arguments d’événement pour l’événement DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="e4196-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="e4196-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="e4196-106">Summary</span></span>

 <span data-ttu-id="e4196-107">Ses</span><span class="sxs-lookup"><span data-stu-id="e4196-107">Members</span></span>                        | <span data-ttu-id="e4196-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="e4196-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e4196-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="e4196-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="e4196-110">Objet paramètre de l’événement DevToolsProtocol correspondant représenté sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="e4196-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="e4196-111">Ses</span><span class="sxs-lookup"><span data-stu-id="e4196-111">Members</span></span>

#### <span data-ttu-id="e4196-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="e4196-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="e4196-113">Objet paramètre de l’événement DevToolsProtocol correspondant représenté sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="e4196-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="e4196-114">valeur publique HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="e4196-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

