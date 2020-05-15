---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 342716da2cded9c903f1edd13fb3400c779a9b39
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653500"
---
# <span data-ttu-id="26d88-104">interface IWebView2DocumentStateChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="26d88-104">interface IWebView2DocumentStateChangedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="26d88-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="26d88-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="26d88-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="26d88-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DocumentStateChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="26d88-107">Arguments d’événement pour l’événement DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="26d88-107">Event args for the DocumentStateChanged event.</span></span>

## <span data-ttu-id="26d88-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="26d88-108">Summary</span></span>

 <span data-ttu-id="26d88-109">Ses</span><span class="sxs-lookup"><span data-stu-id="26d88-109">Members</span></span>                        | <span data-ttu-id="26d88-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="26d88-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="26d88-111">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="26d88-111">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="26d88-112">True si la page vers laquelle vous naviguez est un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="26d88-112">True if the page being navigated to is a new document.</span></span>
[<span data-ttu-id="26d88-113">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="26d88-113">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="26d88-114">True si le contenu chargé est une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="26d88-114">True if the loaded content is an error page.</span></span>

## <span data-ttu-id="26d88-115">Ses</span><span class="sxs-lookup"><span data-stu-id="26d88-115">Members</span></span>

#### <span data-ttu-id="26d88-116">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="26d88-116">get_IsNewDocument</span></span> 

<span data-ttu-id="26d88-117">True si la page vers laquelle vous naviguez est un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="26d88-117">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="26d88-118">valeur publique HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="26d88-118">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

#### <span data-ttu-id="26d88-119">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="26d88-119">get_IsErrorPage</span></span> 

<span data-ttu-id="26d88-120">True si le contenu chargé est une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="26d88-120">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="26d88-121">valeur publique HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="26d88-121">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

