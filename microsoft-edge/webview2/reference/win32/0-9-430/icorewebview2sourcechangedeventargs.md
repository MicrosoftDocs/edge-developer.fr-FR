---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 69c569be7e712d0f5cfddbaa180419be8d475ad0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653643"
---
# <span data-ttu-id="1b2e5-104">interface ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="1b2e5-104">interface ICoreWebView2SourceChangedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="1b2e5-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="1b2e5-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="1b2e5-107">Arguments d’événement pour l’événement SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-107">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="1b2e5-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="1b2e5-108">Summary</span></span>

 <span data-ttu-id="1b2e5-109">Ses</span><span class="sxs-lookup"><span data-stu-id="1b2e5-109">Members</span></span>                        | <span data-ttu-id="1b2e5-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="1b2e5-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1b2e5-111">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="1b2e5-111">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="1b2e5-112">True si la page vers laquelle vous naviguez est un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-112">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="1b2e5-113">Ses</span><span class="sxs-lookup"><span data-stu-id="1b2e5-113">Members</span></span>

#### <span data-ttu-id="1b2e5-114">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="1b2e5-114">get_IsNewDocument</span></span> 

<span data-ttu-id="1b2e5-115">True si la page vers laquelle vous naviguez est un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="1b2e5-115">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="1b2e5-116">valeur publique HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="1b2e5-116">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

