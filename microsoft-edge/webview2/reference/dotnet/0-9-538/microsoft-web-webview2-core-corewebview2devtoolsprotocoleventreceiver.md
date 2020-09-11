---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver
ms.openlocfilehash: a3ba4a66ab48a7fb5d2184fa404365e77cb574a3
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011012"
---
# <span data-ttu-id="f4106-104">0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="f4106-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2DevToolsProtocolEventReceiver class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="f4106-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="f4106-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="f4106-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="f4106-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="f4106-107">Un destinataire est créé pour un événement de protocole DevTools particulier et vous permet de vous abonner à cet événement et de vous désabonner.</span><span class="sxs-lookup"><span data-stu-id="f4106-107">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.</span></span>

## <span data-ttu-id="f4106-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="f4106-108">Summary</span></span>

 <span data-ttu-id="f4106-109">Ses</span><span class="sxs-lookup"><span data-stu-id="f4106-109">Members</span></span>                        | <span data-ttu-id="f4106-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="f4106-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f4106-111">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="f4106-111">DevToolsProtocolEventReceived</span></span>](#devtoolsprotocoleventreceived) | <span data-ttu-id="f4106-112">S’abonner à un événement DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="f4106-112">Subscribe to a DevToolsProtocol event.</span></span>

<span data-ttu-id="f4106-113">Obtenu à partir de l’objet WebView par le biais de GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="f4106-113">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="f4106-114">Ses</span><span class="sxs-lookup"><span data-stu-id="f4106-114">Members</span></span>

#### <span data-ttu-id="f4106-115">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="f4106-115">DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="f4106-116">S’abonner à un événement DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="f4106-116">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="f4106-117">événement public EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md)  >  [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span><span class="sxs-lookup"><span data-stu-id="f4106-117">public event EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md) > [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span></span>

<span data-ttu-id="f4106-118">La méthode Invoke du gestionnaire est appelée chaque fois que l’événement DevToolsProtocol correspondant est déclenché.</span><span class="sxs-lookup"><span data-stu-id="f4106-118">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="f4106-119">Invoke sera appelé à l’aide d’un objet args d’événement contenant l’objet de paramètre de l’événement de protocole DevTools sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="f4106-119">Invoke will be called with the an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

