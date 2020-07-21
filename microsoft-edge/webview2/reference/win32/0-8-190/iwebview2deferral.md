---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: a1c00c29a3e063cd995c9f0eb287d870fd1211dc
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886144"
---
# <span data-ttu-id="138b1-104">0.8.355-interface IWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="138b1-104">0.8.355 - interface IWebView2Deferral</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="138b1-105">Cette interface est utilisée pour effectuer des reports sur des arguments d’événement qui prennent en charge l’affichage des reports via leur méthode GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="138b1-105">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="138b1-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="138b1-106">Summary</span></span>

 <span data-ttu-id="138b1-107">Ses</span><span class="sxs-lookup"><span data-stu-id="138b1-107">Members</span></span>                        | <span data-ttu-id="138b1-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="138b1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="138b1-109">Complete</span><span class="sxs-lookup"><span data-stu-id="138b1-109">Complete</span></span>](#complete) | <span data-ttu-id="138b1-110">Termine l’événement différé associé.</span><span class="sxs-lookup"><span data-stu-id="138b1-110">Completes the associated deferred event.</span></span>

## <span data-ttu-id="138b1-111">Ses</span><span class="sxs-lookup"><span data-stu-id="138b1-111">Members</span></span>

#### <span data-ttu-id="138b1-112">Complete</span><span class="sxs-lookup"><span data-stu-id="138b1-112">Complete</span></span> 

<span data-ttu-id="138b1-113">Termine l’événement différé associé.</span><span class="sxs-lookup"><span data-stu-id="138b1-113">Completes the associated deferred event.</span></span>

> <span data-ttu-id="138b1-114">valeur publique HRESULT [achevée](#complete)()</span><span class="sxs-lookup"><span data-stu-id="138b1-114">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="138b1-115">Complète doit être appelé une seule fois pour chaque Report.</span><span class="sxs-lookup"><span data-stu-id="138b1-115">Complete should only be called once for each deferral taken.</span></span>

