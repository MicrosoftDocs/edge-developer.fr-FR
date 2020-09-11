---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2WebResourceRequestedEventHandler
ms.openlocfilehash: a1bf9e05e403df10fc8e45ff5b5bc19f28558e3c
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010371"
---
# <span data-ttu-id="f821c-104">0.9.579-interface ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f821c-104">0.9.579 - interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="f821c-105">Se déclenche quand une requête d’URL (par le biais d’un réseau, un fichier, etc.) est effectuée dans le WebView pour un filtre de ressources Web correspondant à une URL spécifiée dans AddWebResourceRequestedFilter.</span><span class="sxs-lookup"><span data-stu-id="f821c-105">Fires when a URL request (through network, file etc.) is made in the webview for a Web resource matching resource context filter and URL specified in AddWebResourceRequestedFilter.</span></span>

## <span data-ttu-id="f821c-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="f821c-106">Summary</span></span>

 <span data-ttu-id="f821c-107">Ses</span><span class="sxs-lookup"><span data-stu-id="f821c-107">Members</span></span>                        | <span data-ttu-id="f821c-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="f821c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f821c-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="f821c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f821c-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="f821c-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="f821c-111">L’hôte peut afficher et modifier la demande ou fournir une réponse sous la forme d’un modèle similaire à HTTP, auquel cas la requête est immédiatement terminée.</span><span class="sxs-lookup"><span data-stu-id="f821c-111">The host can view and modify the request or provide a response in a similar pattern to HTTP, in which case the request immediately completed.</span></span> <span data-ttu-id="f821c-112">Il est possible qu’elle ne contienne aucun en-tête de requête ajouté par la pile réseau, par exemple les en-têtes d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="f821c-112">This may not contain any request headers that are added by the network stack, such as Authorization headers.</span></span>

## <span data-ttu-id="f821c-113">Ses</span><span class="sxs-lookup"><span data-stu-id="f821c-113">Members</span></span>

#### <span data-ttu-id="f821c-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="f821c-114">Invoke</span></span> 

<span data-ttu-id="f821c-115">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="f821c-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f821c-116">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="f821c-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>

