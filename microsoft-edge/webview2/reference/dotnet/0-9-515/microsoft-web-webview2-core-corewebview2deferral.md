---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: bf198781d67761e9d6c29ee9c6a274462e92a61d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697671"
---
# <span data-ttu-id="3af64-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="3af64-104">Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

> [!NOTE]
> <span data-ttu-id="3af64-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="3af64-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="3af64-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="3af64-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="3af64-107">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="3af64-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="3af64-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="3af64-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="3af64-109">Cette classe est utilisée pour effectuer des reports sur des arguments d’événement qui prennent en charge l’affichage des reports via leur méthode GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="3af64-109">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="3af64-110">Résumé</span><span class="sxs-lookup"><span data-stu-id="3af64-110">Summary</span></span>

 <span data-ttu-id="3af64-111">Ses</span><span class="sxs-lookup"><span data-stu-id="3af64-111">Members</span></span>                        | <span data-ttu-id="3af64-112">Descriptions</span><span class="sxs-lookup"><span data-stu-id="3af64-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3af64-113">Complete</span><span class="sxs-lookup"><span data-stu-id="3af64-113">Complete</span></span>](#complete) | <span data-ttu-id="3af64-114">Termine l’événement différé associé.</span><span class="sxs-lookup"><span data-stu-id="3af64-114">Completes the associated deferred event.</span></span>

## <span data-ttu-id="3af64-115">Ses</span><span class="sxs-lookup"><span data-stu-id="3af64-115">Members</span></span>

#### <span data-ttu-id="3af64-116">Complete</span><span class="sxs-lookup"><span data-stu-id="3af64-116">Complete</span></span> 

<span data-ttu-id="3af64-117">Termine l’événement différé associé.</span><span class="sxs-lookup"><span data-stu-id="3af64-117">Completes the associated deferred event.</span></span>

> <span data-ttu-id="3af64-118">annulation publique [terminée](#complete)()</span><span class="sxs-lookup"><span data-stu-id="3af64-118">public void [Complete](#complete)()</span></span>

<span data-ttu-id="3af64-119">Complète doit être appelé une seule fois pour chaque Report.</span><span class="sxs-lookup"><span data-stu-id="3af64-119">Complete should only be called once for each deferral taken.</span></span>

