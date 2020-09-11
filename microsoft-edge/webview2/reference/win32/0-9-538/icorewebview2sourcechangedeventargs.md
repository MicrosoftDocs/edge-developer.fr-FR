---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2SourceChangedEventArgs
ms.openlocfilehash: b9350db7d59c0369bfb16d10e30a23ef3f6bffa5
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010459"
---
# <span data-ttu-id="8fd1d-104">0.9.579-interface ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8fd1d-104">0.9.579 - interface ICoreWebView2SourceChangedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="8fd1d-105">Arguments d’événement pour l’événement SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="8fd1d-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="8fd1d-106">Summary</span></span>

 <span data-ttu-id="8fd1d-107">Ses</span><span class="sxs-lookup"><span data-stu-id="8fd1d-107">Members</span></span>                        | <span data-ttu-id="8fd1d-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="8fd1d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8fd1d-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="8fd1d-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="8fd1d-110">True si la page vers laquelle vous naviguez est un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="8fd1d-111">Ses</span><span class="sxs-lookup"><span data-stu-id="8fd1d-111">Members</span></span>

#### <span data-ttu-id="8fd1d-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="8fd1d-112">get_IsNewDocument</span></span> 

<span data-ttu-id="8fd1d-113">True si la page vers laquelle vous naviguez est un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="8fd1d-114">valeur publique HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="8fd1d-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

