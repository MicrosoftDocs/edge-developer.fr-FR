---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 9ea8f860d637c5d9e49e68917d167380c0418b87
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877370"
---
# <span data-ttu-id="de345-104">0.9.515-interface ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="de345-104">0.9.515 - interface ICoreWebView2SourceChangedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="de345-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="de345-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="de345-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="de345-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="de345-107">Arguments d’événement pour l’événement SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="de345-107">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="de345-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="de345-108">Summary</span></span>

 <span data-ttu-id="de345-109">Ses</span><span class="sxs-lookup"><span data-stu-id="de345-109">Members</span></span>                        | <span data-ttu-id="de345-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="de345-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="de345-111">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="de345-111">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="de345-112">True si la page vers laquelle vous naviguez est un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="de345-112">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="de345-113">Ses</span><span class="sxs-lookup"><span data-stu-id="de345-113">Members</span></span>

#### <span data-ttu-id="de345-114">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="de345-114">get_IsNewDocument</span></span> 

<span data-ttu-id="de345-115">True si la page vers laquelle vous naviguez est un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="de345-115">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="de345-116">valeur publique HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="de345-116">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

