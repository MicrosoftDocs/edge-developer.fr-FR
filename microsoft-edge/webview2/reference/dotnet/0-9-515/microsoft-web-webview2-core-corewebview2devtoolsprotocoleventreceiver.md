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
ms.openlocfilehash: 23ee363fd90416d07c76644879a5f4b6cc2acabe
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653573"
---
# <span data-ttu-id="4db93-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="4db93-104">Microsoft.Web.WebView2.Core.CoreWebView2DevToolsProtocolEventReceiver class</span></span> 

<span data-ttu-id="4db93-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="4db93-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="4db93-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="4db93-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="4db93-107">Un destinataire est créé pour un événement de protocole DevTools particulier et vous permet de vous abonner à cet événement et de vous désabonner.</span><span class="sxs-lookup"><span data-stu-id="4db93-107">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.</span></span>

## <span data-ttu-id="4db93-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="4db93-108">Summary</span></span>

 <span data-ttu-id="4db93-109">Ses</span><span class="sxs-lookup"><span data-stu-id="4db93-109">Members</span></span>                        | <span data-ttu-id="4db93-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="4db93-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4db93-111">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="4db93-111">DevToolsProtocolEventReceived</span></span>](#devtoolsprotocoleventreceived) | <span data-ttu-id="4db93-112">S’abonner à un événement DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="4db93-112">Subscribe to a DevToolsProtocol event.</span></span>

<span data-ttu-id="4db93-113">Obtenu à partir de l’objet WebView par le biais de GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="4db93-113">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="4db93-114">Ses</span><span class="sxs-lookup"><span data-stu-id="4db93-114">Members</span></span>

#### <span data-ttu-id="4db93-115">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="4db93-115">DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="4db93-116">S’abonner à un événement DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="4db93-116">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="4db93-117">événement public EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md)  >  [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span><span class="sxs-lookup"><span data-stu-id="4db93-117">public event EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md) > [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span></span>

<span data-ttu-id="4db93-118">La méthode Invoke du gestionnaire est appelée chaque fois que l’événement DevToolsProtocol correspondant est déclenché.</span><span class="sxs-lookup"><span data-stu-id="4db93-118">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="4db93-119">Invoke sera appelé à l’aide d’un objet args d’événement contenant l’objet de paramètre de l’événement de protocole DevTools sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="4db93-119">Invoke will be called with the an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

