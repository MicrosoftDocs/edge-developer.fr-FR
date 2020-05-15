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
ms.openlocfilehash: e7fbc952a44bdd38e6e59c46adafb8e71b7904b6
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653529"
---
# <span data-ttu-id="dccbd-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="dccbd-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="dccbd-105">Arguments d’événement pour l’événement DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="dccbd-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="dccbd-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="dccbd-106">Summary</span></span>

 <span data-ttu-id="dccbd-107">Ses</span><span class="sxs-lookup"><span data-stu-id="dccbd-107">Members</span></span>                        | <span data-ttu-id="dccbd-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="dccbd-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="dccbd-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="dccbd-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="dccbd-110">Objet paramètre de l’événement DevToolsProtocol correspondant représenté sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="dccbd-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="dccbd-111">Ses</span><span class="sxs-lookup"><span data-stu-id="dccbd-111">Members</span></span>

#### <span data-ttu-id="dccbd-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="dccbd-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="dccbd-113">Objet paramètre de l’événement DevToolsProtocol correspondant représenté sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="dccbd-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="dccbd-114">valeur publique HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="dccbd-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

