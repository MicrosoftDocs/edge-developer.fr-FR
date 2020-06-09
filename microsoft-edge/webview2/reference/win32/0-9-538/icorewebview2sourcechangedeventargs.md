---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 4ae58375f0158a3876b284e16a579149dc6db9a5
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698716"
---
# <span data-ttu-id="a3709-104">interface ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a3709-104">interface ICoreWebView2SourceChangedEventArgs</span></span> 

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="a3709-105">Arguments d’événement pour l’événement SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="a3709-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="a3709-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="a3709-106">Summary</span></span>

 <span data-ttu-id="a3709-107">Ses</span><span class="sxs-lookup"><span data-stu-id="a3709-107">Members</span></span>                        | <span data-ttu-id="a3709-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="a3709-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a3709-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="a3709-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="a3709-110">True si la page vers laquelle vous naviguez est un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="a3709-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="a3709-111">Ses</span><span class="sxs-lookup"><span data-stu-id="a3709-111">Members</span></span>

#### <span data-ttu-id="a3709-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="a3709-112">get_IsNewDocument</span></span> 

<span data-ttu-id="a3709-113">True si la page vers laquelle vous naviguez est un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="a3709-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="a3709-114">valeur publique HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="a3709-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

