---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler
ms.openlocfilehash: 03c67160e9c10db7cf3fc88b7ecf2c84c30c4129
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011418"
---
# <span data-ttu-id="69bd7-104">0.9.579-interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="69bd7-104">0.9.579 - interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="69bd7-105">Se déclenche lors de la réception d’une réponse à une demande de ressource Web dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="69bd7-105">Fires when a response for a request is received for a Web resource in the webview.</span></span>

## <span data-ttu-id="69bd7-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="69bd7-106">Summary</span></span>

 <span data-ttu-id="69bd7-107">Ses</span><span class="sxs-lookup"><span data-stu-id="69bd7-107">Members</span></span>                        | <span data-ttu-id="69bd7-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="69bd7-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="69bd7-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="69bd7-109">Invoke</span></span>](#invoke) | <span data-ttu-id="69bd7-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="69bd7-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="69bd7-111">L’hôte peut utiliser cet événement pour afficher la demande réelle et la réponse d’une ressource Web.</span><span class="sxs-lookup"><span data-stu-id="69bd7-111">Host can use this event to view the actual request and response for a Web resource.</span></span> <span data-ttu-id="69bd7-112">Cela inclut les modifications de requête ou de réponse apportées par la pile réseau (par exemple, l’ajout d’en-têtes d’autorisation) après le déclenchement de l’événement WebResourceRequested pour la requête associée.</span><span class="sxs-lookup"><span data-stu-id="69bd7-112">This includes any request or response modifications made by the network stack (such as adding of Authorization headers) after the WebResourceRequested event for the associated request has fired.</span></span> <span data-ttu-id="69bd7-113">Les modifications apportées aux objets de requête ou de réponse sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="69bd7-113">Modifications made to the request or response objects are ignored.</span></span>

## <span data-ttu-id="69bd7-114">Ses</span><span class="sxs-lookup"><span data-stu-id="69bd7-114">Members</span></span>

#### <span data-ttu-id="69bd7-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="69bd7-115">Invoke</span></span> 

<span data-ttu-id="69bd7-116">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="69bd7-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="69bd7-117">[appel](#invoke)HRESULT public ([ICoreWebView2Experimental](icorewebview2experimental.md) \* sender, [ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs](icorewebview2experimentalwebresourceresponsereceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="69bd7-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Experimental](icorewebview2experimental.md) \* sender, [ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs](icorewebview2experimentalwebresourceresponsereceivedeventargs.md) \* args)</span></span>

