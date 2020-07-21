---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 135289994bdfe5481018c479b7a1d9c372ecb256
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885108"
---
# <span data-ttu-id="6b515-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="6b515-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="6b515-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="6b515-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="6b515-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="6b515-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="6b515-107">Cette classe est utilisée pour effectuer des reports sur des arguments d’événement qui prennent en charge l’affichage des reports via leur méthode GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="6b515-107">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="6b515-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="6b515-108">Summary</span></span>

 <span data-ttu-id="6b515-109">Ses</span><span class="sxs-lookup"><span data-stu-id="6b515-109">Members</span></span>                        | <span data-ttu-id="6b515-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="6b515-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6b515-111">Complete</span><span class="sxs-lookup"><span data-stu-id="6b515-111">Complete</span></span>](#complete) | <span data-ttu-id="6b515-112">Termine l’événement différé associé.</span><span class="sxs-lookup"><span data-stu-id="6b515-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="6b515-113">Ses</span><span class="sxs-lookup"><span data-stu-id="6b515-113">Members</span></span>

#### <span data-ttu-id="6b515-114">Complete</span><span class="sxs-lookup"><span data-stu-id="6b515-114">Complete</span></span> 

<span data-ttu-id="6b515-115">Termine l’événement différé associé.</span><span class="sxs-lookup"><span data-stu-id="6b515-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="6b515-116">annulation publique [terminée](#complete)()</span><span class="sxs-lookup"><span data-stu-id="6b515-116">public void [Complete](#complete)()</span></span>

<span data-ttu-id="6b515-117">Complète doit être appelé une seule fois pour chaque Report.</span><span class="sxs-lookup"><span data-stu-id="6b515-117">Complete should only be called once for each deferral taken.</span></span>

