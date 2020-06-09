---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 84ff41eeb30d5c3561666a71f989e02163419152
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697965"
---
# <span data-ttu-id="78e2d-104">interface ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="78e2d-104">interface ICoreWebView2DocumentTitleChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="78e2d-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="78e2d-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="78e2d-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="78e2d-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="78e2d-107">L’appelant implémente cette interface pour recevoir des événements DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="78e2d-107">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="78e2d-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="78e2d-108">Summary</span></span>

 <span data-ttu-id="78e2d-109">Ses</span><span class="sxs-lookup"><span data-stu-id="78e2d-109">Members</span></span>                        | <span data-ttu-id="78e2d-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="78e2d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="78e2d-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="78e2d-111">Invoke</span></span>](#invoke) | <span data-ttu-id="78e2d-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="78e2d-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="78e2d-113">Utilisez la propriété DocumentTitle pour obtenir le titre modifié.</span><span class="sxs-lookup"><span data-stu-id="78e2d-113">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="78e2d-114">Ses</span><span class="sxs-lookup"><span data-stu-id="78e2d-114">Members</span></span>

#### <span data-ttu-id="78e2d-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="78e2d-115">Invoke</span></span> 

<span data-ttu-id="78e2d-116">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="78e2d-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="78e2d-117">[appel](#invoke)de HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="78e2d-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="78e2d-118">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="78e2d-118">There are no event args and the args parameter will be null.</span></span>

