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
ms.openlocfilehash: 7d21db7c3f0a66f60f32e92b3951151b8d13a002
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698077"
---
# <span data-ttu-id="27e5e-104">interface ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="27e5e-104">interface ICoreWebView2Deferral</span></span> 

> [!NOTE]
> <span data-ttu-id="27e5e-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="27e5e-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="27e5e-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="27e5e-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="27e5e-107">Cette interface est utilisée pour effectuer des reports sur des arguments d’événement qui prennent en charge l’affichage des reports via leur méthode GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="27e5e-107">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="27e5e-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="27e5e-108">Summary</span></span>

 <span data-ttu-id="27e5e-109">Ses</span><span class="sxs-lookup"><span data-stu-id="27e5e-109">Members</span></span>                        | <span data-ttu-id="27e5e-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="27e5e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="27e5e-111">Complete</span><span class="sxs-lookup"><span data-stu-id="27e5e-111">Complete</span></span>](#complete) | <span data-ttu-id="27e5e-112">Termine l’événement différé associé.</span><span class="sxs-lookup"><span data-stu-id="27e5e-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="27e5e-113">Ses</span><span class="sxs-lookup"><span data-stu-id="27e5e-113">Members</span></span>

#### <span data-ttu-id="27e5e-114">Complete</span><span class="sxs-lookup"><span data-stu-id="27e5e-114">Complete</span></span> 

<span data-ttu-id="27e5e-115">Termine l’événement différé associé.</span><span class="sxs-lookup"><span data-stu-id="27e5e-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="27e5e-116">valeur publique HRESULT [achevée](#complete)()</span><span class="sxs-lookup"><span data-stu-id="27e5e-116">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="27e5e-117">Complète doit être appelé une seule fois pour chaque Report.</span><span class="sxs-lookup"><span data-stu-id="27e5e-117">Complete should only be called once for each deferral taken.</span></span>

