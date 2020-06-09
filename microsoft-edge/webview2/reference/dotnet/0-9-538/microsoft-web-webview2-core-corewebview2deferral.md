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
ms.openlocfilehash: 935e8edb4db54e7bbb707cb2dc704ba312ed3196
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698609"
---
# <span data-ttu-id="11d55-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="11d55-104">Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

<span data-ttu-id="11d55-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="11d55-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="11d55-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="11d55-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="11d55-107">Cette classe est utilisée pour effectuer des reports sur des arguments d’événement qui prennent en charge l’affichage des reports via leur méthode GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="11d55-107">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="11d55-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="11d55-108">Summary</span></span>

 <span data-ttu-id="11d55-109">Ses</span><span class="sxs-lookup"><span data-stu-id="11d55-109">Members</span></span>                        | <span data-ttu-id="11d55-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="11d55-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="11d55-111">Complete</span><span class="sxs-lookup"><span data-stu-id="11d55-111">Complete</span></span>](#complete) | <span data-ttu-id="11d55-112">Termine l’événement différé associé.</span><span class="sxs-lookup"><span data-stu-id="11d55-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="11d55-113">Ses</span><span class="sxs-lookup"><span data-stu-id="11d55-113">Members</span></span>

#### <span data-ttu-id="11d55-114">Complete</span><span class="sxs-lookup"><span data-stu-id="11d55-114">Complete</span></span> 

<span data-ttu-id="11d55-115">Termine l’événement différé associé.</span><span class="sxs-lookup"><span data-stu-id="11d55-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="11d55-116">annulation publique [terminée](#complete)()</span><span class="sxs-lookup"><span data-stu-id="11d55-116">public void [Complete](#complete)()</span></span>

<span data-ttu-id="11d55-117">Complète doit être appelé une seule fois pour chaque Report.</span><span class="sxs-lookup"><span data-stu-id="11d55-117">Complete should only be called once for each deferral taken.</span></span>

