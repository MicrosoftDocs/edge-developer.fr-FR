---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 2429c519858aa9c55e52d47bea64fc182b6beb73
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698652"
---
# <span data-ttu-id="bddcd-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="bddcd-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="bddcd-105">Arguments d’événement pour l’événement DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="bddcd-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="bddcd-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="bddcd-106">Summary</span></span>

 <span data-ttu-id="bddcd-107">Ses</span><span class="sxs-lookup"><span data-stu-id="bddcd-107">Members</span></span>                        | <span data-ttu-id="bddcd-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="bddcd-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bddcd-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="bddcd-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="bddcd-110">Objet paramètre de l’événement DevToolsProtocol correspondant représenté sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="bddcd-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="bddcd-111">Ses</span><span class="sxs-lookup"><span data-stu-id="bddcd-111">Members</span></span>

#### <span data-ttu-id="bddcd-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="bddcd-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="bddcd-113">Objet paramètre de l’événement DevToolsProtocol correspondant représenté sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="bddcd-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="bddcd-114">valeur publique HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="bddcd-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

