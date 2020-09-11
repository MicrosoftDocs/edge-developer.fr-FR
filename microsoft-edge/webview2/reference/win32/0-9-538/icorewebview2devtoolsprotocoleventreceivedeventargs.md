---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2DevToolsProtocolEventReceivedEventArgs
ms.openlocfilehash: 79af7b28b8b8ab7e2e2b6612f121208b8d917725
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010269"
---
# <span data-ttu-id="b79e5-104">0.9.579-interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="b79e5-104">0.9.579 - interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="b79e5-105">Arguments d’événement pour l’événement DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="b79e5-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="b79e5-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="b79e5-106">Summary</span></span>

 <span data-ttu-id="b79e5-107">Ses</span><span class="sxs-lookup"><span data-stu-id="b79e5-107">Members</span></span>                        | <span data-ttu-id="b79e5-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="b79e5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b79e5-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="b79e5-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="b79e5-110">Objet paramètre de l’événement DevToolsProtocol correspondant représenté sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="b79e5-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="b79e5-111">Ses</span><span class="sxs-lookup"><span data-stu-id="b79e5-111">Members</span></span>

#### <span data-ttu-id="b79e5-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="b79e5-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="b79e5-113">Objet paramètre de l’événement DevToolsProtocol correspondant représenté sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="b79e5-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="b79e5-114">valeur publique HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="b79e5-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

