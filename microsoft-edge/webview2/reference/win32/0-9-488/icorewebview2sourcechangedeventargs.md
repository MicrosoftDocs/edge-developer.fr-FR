---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 9a98e2afa5b15452d7521183abebc019d51e3a3c
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885456"
---
# <span data-ttu-id="6a9ae-104">0.9.515-interface ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="6a9ae-104">0.9.515 - interface ICoreWebView2SourceChangedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="6a9ae-105">Arguments d’événement pour l’événement SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="6a9ae-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="6a9ae-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="6a9ae-106">Summary</span></span>

 <span data-ttu-id="6a9ae-107">Ses</span><span class="sxs-lookup"><span data-stu-id="6a9ae-107">Members</span></span>                        | <span data-ttu-id="6a9ae-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="6a9ae-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6a9ae-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="6a9ae-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="6a9ae-110">True si la page vers laquelle vous naviguez est un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="6a9ae-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="6a9ae-111">Ses</span><span class="sxs-lookup"><span data-stu-id="6a9ae-111">Members</span></span>

#### <span data-ttu-id="6a9ae-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="6a9ae-112">get_IsNewDocument</span></span> 

<span data-ttu-id="6a9ae-113">True si la page vers laquelle vous naviguez est un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="6a9ae-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="6a9ae-114">valeur publique HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="6a9ae-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

