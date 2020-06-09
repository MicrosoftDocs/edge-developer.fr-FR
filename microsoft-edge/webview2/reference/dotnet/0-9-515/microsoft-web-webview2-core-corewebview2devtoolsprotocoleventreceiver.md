---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 9b54f9f519c76440d3556bb67f5ab7ad186ba290
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697664"
---
# <span data-ttu-id="0e660-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="0e660-104">Microsoft.Web.WebView2.Core.CoreWebView2DevToolsProtocolEventReceiver class</span></span> 

> [!NOTE]
> <span data-ttu-id="0e660-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="0e660-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="0e660-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="0e660-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="0e660-107">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="0e660-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="0e660-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="0e660-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="0e660-109">Un destinataire est créé pour un événement de protocole DevTools particulier et vous permet de vous abonner à cet événement et de vous désabonner.</span><span class="sxs-lookup"><span data-stu-id="0e660-109">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.</span></span>

## <span data-ttu-id="0e660-110">Résumé</span><span class="sxs-lookup"><span data-stu-id="0e660-110">Summary</span></span>

 <span data-ttu-id="0e660-111">Ses</span><span class="sxs-lookup"><span data-stu-id="0e660-111">Members</span></span>                        | <span data-ttu-id="0e660-112">Descriptions</span><span class="sxs-lookup"><span data-stu-id="0e660-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0e660-113">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="0e660-113">DevToolsProtocolEventReceived</span></span>](#devtoolsprotocoleventreceived) | <span data-ttu-id="0e660-114">S’abonner à un événement DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="0e660-114">Subscribe to a DevToolsProtocol event.</span></span>

<span data-ttu-id="0e660-115">Obtenu à partir de l’objet WebView par le biais de GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="0e660-115">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="0e660-116">Ses</span><span class="sxs-lookup"><span data-stu-id="0e660-116">Members</span></span>

#### <span data-ttu-id="0e660-117">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="0e660-117">DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="0e660-118">S’abonner à un événement DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="0e660-118">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="0e660-119">événement public EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md)  >  [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span><span class="sxs-lookup"><span data-stu-id="0e660-119">public event EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md) > [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span></span>

<span data-ttu-id="0e660-120">La méthode Invoke du gestionnaire est appelée chaque fois que l’événement DevToolsProtocol correspondant est déclenché.</span><span class="sxs-lookup"><span data-stu-id="0e660-120">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="0e660-121">Invoke sera appelé à l’aide d’un objet args d’événement contenant l’objet de paramètre de l’événement de protocole DevTools sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="0e660-121">Invoke will be called with the an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

