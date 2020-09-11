---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2Deferral
ms.openlocfilehash: 62cd86772d45e1bf9eee7d1821a90b723e1af7db
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011047"
---
# <span data-ttu-id="698d6-104">0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="698d6-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="698d6-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="698d6-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="698d6-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="698d6-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="698d6-107">Cette classe est utilisée pour effectuer des reports sur des arguments d’événement qui prennent en charge l’affichage des reports via leur méthode GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="698d6-107">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="698d6-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="698d6-108">Summary</span></span>

 <span data-ttu-id="698d6-109">Ses</span><span class="sxs-lookup"><span data-stu-id="698d6-109">Members</span></span>                        | <span data-ttu-id="698d6-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="698d6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="698d6-111">Complete</span><span class="sxs-lookup"><span data-stu-id="698d6-111">Complete</span></span>](#complete) | <span data-ttu-id="698d6-112">Termine l’événement différé associé.</span><span class="sxs-lookup"><span data-stu-id="698d6-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="698d6-113">Ses</span><span class="sxs-lookup"><span data-stu-id="698d6-113">Members</span></span>

#### <span data-ttu-id="698d6-114">Complete</span><span class="sxs-lookup"><span data-stu-id="698d6-114">Complete</span></span> 

<span data-ttu-id="698d6-115">Termine l’événement différé associé.</span><span class="sxs-lookup"><span data-stu-id="698d6-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="698d6-116">annulation publique [terminée](#complete)()</span><span class="sxs-lookup"><span data-stu-id="698d6-116">public void [Complete](#complete)()</span></span>

<span data-ttu-id="698d6-117">Complète doit être appelé une seule fois pour chaque Report.</span><span class="sxs-lookup"><span data-stu-id="698d6-117">Complete should only be called once for each deferral taken.</span></span>

