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
ms.openlocfilehash: fec7fd7399222d8223d1022cd1e528bc9ed0d161
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653572"
---
# <span data-ttu-id="19de6-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="19de6-104">Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

<span data-ttu-id="19de6-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="19de6-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="19de6-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="19de6-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="19de6-107">Cette classe est utilisée pour effectuer des reports sur des arguments d’événement qui prennent en charge l’affichage des reports via leur méthode GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="19de6-107">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="19de6-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="19de6-108">Summary</span></span>

 <span data-ttu-id="19de6-109">Ses</span><span class="sxs-lookup"><span data-stu-id="19de6-109">Members</span></span>                        | <span data-ttu-id="19de6-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="19de6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="19de6-111">Complete</span><span class="sxs-lookup"><span data-stu-id="19de6-111">Complete</span></span>](#complete) | <span data-ttu-id="19de6-112">Termine l’événement différé associé.</span><span class="sxs-lookup"><span data-stu-id="19de6-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="19de6-113">Ses</span><span class="sxs-lookup"><span data-stu-id="19de6-113">Members</span></span>

#### <span data-ttu-id="19de6-114">Complete</span><span class="sxs-lookup"><span data-stu-id="19de6-114">Complete</span></span> 

<span data-ttu-id="19de6-115">Termine l’événement différé associé.</span><span class="sxs-lookup"><span data-stu-id="19de6-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="19de6-116">annulation publique [terminée](#complete)()</span><span class="sxs-lookup"><span data-stu-id="19de6-116">public void [Complete](#complete)()</span></span>

<span data-ttu-id="19de6-117">Complète doit être appelé une seule fois pour chaque Report.</span><span class="sxs-lookup"><span data-stu-id="19de6-117">Complete should only be called once for each deferral taken.</span></span>

