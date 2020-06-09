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
ms.openlocfilehash: b5fcd04d702483778ef31549c2e7d989ebfe3689
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698649"
---
# <span data-ttu-id="397bd-104">interface ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="397bd-104">interface ICoreWebView2Deferral</span></span> 

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="397bd-105">Cette interface est utilisée pour effectuer des reports sur des arguments d’événement qui prennent en charge l’affichage des reports via leur méthode GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="397bd-105">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="397bd-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="397bd-106">Summary</span></span>

 <span data-ttu-id="397bd-107">Ses</span><span class="sxs-lookup"><span data-stu-id="397bd-107">Members</span></span>                        | <span data-ttu-id="397bd-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="397bd-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="397bd-109">Complete</span><span class="sxs-lookup"><span data-stu-id="397bd-109">Complete</span></span>](#complete) | <span data-ttu-id="397bd-110">Termine l’événement différé associé.</span><span class="sxs-lookup"><span data-stu-id="397bd-110">Completes the associated deferred event.</span></span>

## <span data-ttu-id="397bd-111">Ses</span><span class="sxs-lookup"><span data-stu-id="397bd-111">Members</span></span>

#### <span data-ttu-id="397bd-112">Complete</span><span class="sxs-lookup"><span data-stu-id="397bd-112">Complete</span></span> 

<span data-ttu-id="397bd-113">Termine l’événement différé associé.</span><span class="sxs-lookup"><span data-stu-id="397bd-113">Completes the associated deferred event.</span></span>

> <span data-ttu-id="397bd-114">valeur publique HRESULT [achevée](#complete)()</span><span class="sxs-lookup"><span data-stu-id="397bd-114">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="397bd-115">Complète doit être appelé une seule fois pour chaque Report.</span><span class="sxs-lookup"><span data-stu-id="397bd-115">Complete should only be called once for each deferral taken.</span></span>

