---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: b30b6e35388ab01433b2c879db82d9c4136fae99
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885423"
---
# <span data-ttu-id="bab2b-104">0.9.515-interface ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="bab2b-104">0.9.515 - interface ICoreWebView2Deferral</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="bab2b-105">Cette interface est utilisée pour effectuer des reports sur des arguments d’événement qui prennent en charge l’affichage des reports via leur méthode GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="bab2b-105">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="bab2b-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="bab2b-106">Summary</span></span>

 <span data-ttu-id="bab2b-107">Ses</span><span class="sxs-lookup"><span data-stu-id="bab2b-107">Members</span></span>                        | <span data-ttu-id="bab2b-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="bab2b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bab2b-109">Complete</span><span class="sxs-lookup"><span data-stu-id="bab2b-109">Complete</span></span>](#complete) | <span data-ttu-id="bab2b-110">Termine l’événement différé associé.</span><span class="sxs-lookup"><span data-stu-id="bab2b-110">Completes the associated deferred event.</span></span>

## <span data-ttu-id="bab2b-111">Ses</span><span class="sxs-lookup"><span data-stu-id="bab2b-111">Members</span></span>

#### <span data-ttu-id="bab2b-112">Complete</span><span class="sxs-lookup"><span data-stu-id="bab2b-112">Complete</span></span> 

<span data-ttu-id="bab2b-113">Termine l’événement différé associé.</span><span class="sxs-lookup"><span data-stu-id="bab2b-113">Completes the associated deferred event.</span></span>

> <span data-ttu-id="bab2b-114">valeur publique HRESULT [achevée](#complete)()</span><span class="sxs-lookup"><span data-stu-id="bab2b-114">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="bab2b-115">Complète doit être appelé une seule fois pour chaque Report.</span><span class="sxs-lookup"><span data-stu-id="bab2b-115">Complete should only be called once for each deferral taken.</span></span>

