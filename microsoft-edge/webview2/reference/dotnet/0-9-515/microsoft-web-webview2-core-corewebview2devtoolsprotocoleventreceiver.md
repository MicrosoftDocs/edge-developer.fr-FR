---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 5e6e2d955dd0d52a093eea116a01961e1ee58c76
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877769"
---
# <span data-ttu-id="144ce-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="144ce-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2DevToolsProtocolEventReceiver class</span></span> 

> [!NOTE]
> <span data-ttu-id="144ce-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="144ce-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="144ce-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="144ce-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="144ce-107">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="144ce-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="144ce-108">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="144ce-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="144ce-109">Un destinataire est créé pour un événement de protocole DevTools particulier et vous permet de vous abonner à cet événement et de vous désabonner.</span><span class="sxs-lookup"><span data-stu-id="144ce-109">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.</span></span>

## <span data-ttu-id="144ce-110">Résumé</span><span class="sxs-lookup"><span data-stu-id="144ce-110">Summary</span></span>

 <span data-ttu-id="144ce-111">Ses</span><span class="sxs-lookup"><span data-stu-id="144ce-111">Members</span></span>                        | <span data-ttu-id="144ce-112">Descriptions</span><span class="sxs-lookup"><span data-stu-id="144ce-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="144ce-113">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="144ce-113">DevToolsProtocolEventReceived</span></span>](#devtoolsprotocoleventreceived) | <span data-ttu-id="144ce-114">S’abonner à un événement DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="144ce-114">Subscribe to a DevToolsProtocol event.</span></span>

<span data-ttu-id="144ce-115">Obtenu à partir de l’objet WebView par le biais de GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="144ce-115">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="144ce-116">Ses</span><span class="sxs-lookup"><span data-stu-id="144ce-116">Members</span></span>

#### <span data-ttu-id="144ce-117">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="144ce-117">DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="144ce-118">S’abonner à un événement DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="144ce-118">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="144ce-119">événement public EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md)  >  [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span><span class="sxs-lookup"><span data-stu-id="144ce-119">public event EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md) > [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span></span>

<span data-ttu-id="144ce-120">La méthode Invoke du gestionnaire est appelée chaque fois que l’événement DevToolsProtocol correspondant est déclenché.</span><span class="sxs-lookup"><span data-stu-id="144ce-120">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="144ce-121">Invoke sera appelé à l’aide d’un objet args d’événement contenant l’objet de paramètre de l’événement de protocole DevTools sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="144ce-121">Invoke will be called with the an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

