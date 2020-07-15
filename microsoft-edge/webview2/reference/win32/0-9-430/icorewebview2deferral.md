---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 3edc94e4e659e8b2bb1971c240ba95736a631938
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877965"
---
# <span data-ttu-id="56aec-104">0.9.430-interface ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="56aec-104">0.9.430 - interface ICoreWebView2Deferral</span></span> 

> [!NOTE]
> <span data-ttu-id="56aec-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="56aec-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="56aec-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="56aec-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="56aec-107">Cette interface est utilisée pour effectuer des reports sur des arguments d’événement qui prennent en charge l’affichage des reports via leur méthode GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="56aec-107">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="56aec-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="56aec-108">Summary</span></span>

 <span data-ttu-id="56aec-109">Ses</span><span class="sxs-lookup"><span data-stu-id="56aec-109">Members</span></span>                        | <span data-ttu-id="56aec-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="56aec-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="56aec-111">Complete</span><span class="sxs-lookup"><span data-stu-id="56aec-111">Complete</span></span>](#complete) | <span data-ttu-id="56aec-112">Termine l’événement différé associé.</span><span class="sxs-lookup"><span data-stu-id="56aec-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="56aec-113">Ses</span><span class="sxs-lookup"><span data-stu-id="56aec-113">Members</span></span>

#### <span data-ttu-id="56aec-114">Complete</span><span class="sxs-lookup"><span data-stu-id="56aec-114">Complete</span></span> 

<span data-ttu-id="56aec-115">Termine l’événement différé associé.</span><span class="sxs-lookup"><span data-stu-id="56aec-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="56aec-116">valeur publique HRESULT [achevée](#complete)()</span><span class="sxs-lookup"><span data-stu-id="56aec-116">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="56aec-117">Complète doit être appelé une seule fois pour chaque Report.</span><span class="sxs-lookup"><span data-stu-id="56aec-117">Complete should only be called once for each deferral taken.</span></span>

