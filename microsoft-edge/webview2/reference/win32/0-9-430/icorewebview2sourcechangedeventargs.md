---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 8a9f1b1e44353796c6d3b57d3f4c6f3d4997aad5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880198"
---
# <span data-ttu-id="7d282-104">0.9.430-interface ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="7d282-104">0.9.430 - interface ICoreWebView2SourceChangedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="7d282-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="7d282-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="7d282-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="7d282-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="7d282-107">Arguments d’événement pour l’événement SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="7d282-107">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="7d282-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="7d282-108">Summary</span></span>

 <span data-ttu-id="7d282-109">Ses</span><span class="sxs-lookup"><span data-stu-id="7d282-109">Members</span></span>                        | <span data-ttu-id="7d282-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="7d282-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7d282-111">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="7d282-111">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="7d282-112">True si la page vers laquelle vous naviguez est un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="7d282-112">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="7d282-113">Ses</span><span class="sxs-lookup"><span data-stu-id="7d282-113">Members</span></span>

#### <span data-ttu-id="7d282-114">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="7d282-114">get_IsNewDocument</span></span> 

<span data-ttu-id="7d282-115">True si la page vers laquelle vous naviguez est un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="7d282-115">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="7d282-116">valeur publique HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="7d282-116">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

