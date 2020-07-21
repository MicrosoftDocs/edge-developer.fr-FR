---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 2eb2749b71cd9be9dfd25bb686b4ea57e728f179
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883980"
---
# <span data-ttu-id="7733c-104">0.9.430-interface ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="7733c-104">0.9.430 - interface ICoreWebView2SourceChangedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="7733c-105">Arguments d’événement pour l’événement SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="7733c-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="7733c-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="7733c-106">Summary</span></span>

 <span data-ttu-id="7733c-107">Ses</span><span class="sxs-lookup"><span data-stu-id="7733c-107">Members</span></span>                        | <span data-ttu-id="7733c-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="7733c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7733c-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="7733c-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="7733c-110">True si la page vers laquelle vous naviguez est un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="7733c-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="7733c-111">Ses</span><span class="sxs-lookup"><span data-stu-id="7733c-111">Members</span></span>

#### <span data-ttu-id="7733c-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="7733c-112">get_IsNewDocument</span></span> 

<span data-ttu-id="7733c-113">True si la page vers laquelle vous naviguez est un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="7733c-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="7733c-114">valeur publique HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="7733c-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

