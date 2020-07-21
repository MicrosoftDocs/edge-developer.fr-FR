---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2DocumentStateChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 75741c1ba1d835d1c26c7d1db0845071216e0705
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886121"
---
# <span data-ttu-id="eb7f4-104">0.8.355-interface IWebView2DocumentStateChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="eb7f4-104">0.8.355 - interface IWebView2DocumentStateChangedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2DocumentStateChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="eb7f4-105">Arguments d’événement pour l’événement DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-105">Event args for the DocumentStateChanged event.</span></span>

## <span data-ttu-id="eb7f4-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="eb7f4-106">Summary</span></span>

 <span data-ttu-id="eb7f4-107">Ses</span><span class="sxs-lookup"><span data-stu-id="eb7f4-107">Members</span></span>                        | <span data-ttu-id="eb7f4-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="eb7f4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="eb7f4-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="eb7f4-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="eb7f4-110">True si la page vers laquelle vous naviguez est un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-110">True if the page being navigated to is a new document.</span></span>
[<span data-ttu-id="eb7f4-111">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="eb7f4-111">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="eb7f4-112">True si le contenu chargé est une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-112">True if the loaded content is an error page.</span></span>

## <span data-ttu-id="eb7f4-113">Ses</span><span class="sxs-lookup"><span data-stu-id="eb7f4-113">Members</span></span>

#### <span data-ttu-id="eb7f4-114">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="eb7f4-114">get_IsNewDocument</span></span> 

<span data-ttu-id="eb7f4-115">True si la page vers laquelle vous naviguez est un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-115">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="eb7f4-116">valeur publique HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="eb7f4-116">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

#### <span data-ttu-id="eb7f4-117">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="eb7f4-117">get_IsErrorPage</span></span> 

<span data-ttu-id="eb7f4-118">True si le contenu chargé est une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-118">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="eb7f4-119">valeur publique HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="eb7f4-119">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

