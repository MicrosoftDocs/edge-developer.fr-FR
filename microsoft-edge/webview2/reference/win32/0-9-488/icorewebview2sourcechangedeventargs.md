---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 6d4c5e7893f9be78baca25e8976ca889ef9826c0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653603"
---
# <span data-ttu-id="d9b8a-104">interface ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d9b8a-104">interface ICoreWebView2SourceChangedEventArgs</span></span> 

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="d9b8a-105">Arguments d’événement pour l’événement SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="d9b8a-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="d9b8a-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="d9b8a-106">Summary</span></span>

 <span data-ttu-id="d9b8a-107">Ses</span><span class="sxs-lookup"><span data-stu-id="d9b8a-107">Members</span></span>                        | <span data-ttu-id="d9b8a-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="d9b8a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d9b8a-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="d9b8a-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="d9b8a-110">True si la page vers laquelle vous naviguez est un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="d9b8a-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="d9b8a-111">Ses</span><span class="sxs-lookup"><span data-stu-id="d9b8a-111">Members</span></span>

#### <span data-ttu-id="d9b8a-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="d9b8a-112">get_IsNewDocument</span></span> 

<span data-ttu-id="d9b8a-113">True si la page vers laquelle vous naviguez est un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="d9b8a-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="d9b8a-114">valeur publique HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="d9b8a-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

