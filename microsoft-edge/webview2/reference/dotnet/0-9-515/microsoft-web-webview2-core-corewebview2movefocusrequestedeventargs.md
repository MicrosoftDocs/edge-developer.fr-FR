---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 37d64a18589df936383efe05317c1a625b841a6e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877657"
---
# <span data-ttu-id="4c0fd-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="4c0fd-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2MoveFocusRequestedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="4c0fd-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="4c0fd-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="4c0fd-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="4c0fd-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="4c0fd-107">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="4c0fd-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="4c0fd-108">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="4c0fd-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="4c0fd-109">Arguments d’événement pour l’événement MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="4c0fd-109">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="4c0fd-110">Résumé</span><span class="sxs-lookup"><span data-stu-id="4c0fd-110">Summary</span></span>

 <span data-ttu-id="4c0fd-111">Ses</span><span class="sxs-lookup"><span data-stu-id="4c0fd-111">Members</span></span>                        | <span data-ttu-id="4c0fd-112">Descriptions</span><span class="sxs-lookup"><span data-stu-id="4c0fd-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4c0fd-113">Handled</span><span class="sxs-lookup"><span data-stu-id="4c0fd-113">Handled</span></span>](#handled) | <span data-ttu-id="4c0fd-114">Indiquez si l’événement a été géré par l’application.</span><span class="sxs-lookup"><span data-stu-id="4c0fd-114">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="4c0fd-115">Raison</span><span class="sxs-lookup"><span data-stu-id="4c0fd-115">Reason</span></span>](#reason) | <span data-ttu-id="4c0fd-116">La raison pour laquelle WebView a déclenché l’événement MoveFocus demandé.</span><span class="sxs-lookup"><span data-stu-id="4c0fd-116">The reason for WebView to fire the MoveFocus Requested event.</span></span>

## <span data-ttu-id="4c0fd-117">Ses</span><span class="sxs-lookup"><span data-stu-id="4c0fd-117">Members</span></span>

#### <span data-ttu-id="4c0fd-118">Handled</span><span class="sxs-lookup"><span data-stu-id="4c0fd-118">Handled</span></span> 

<span data-ttu-id="4c0fd-119">Indiquez si l’événement a été géré par l’application.</span><span class="sxs-lookup"><span data-stu-id="4c0fd-119">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="4c0fd-120">propriété booléenne [gérée](#handled)</span><span class="sxs-lookup"><span data-stu-id="4c0fd-120">public bool [Handled](#handled)</span></span>

<span data-ttu-id="4c0fd-121">Si l’application a déplacé le focus vers l’emplacement souhaité, elle doit définir la propriété Handled sur TRUE.</span><span class="sxs-lookup"><span data-stu-id="4c0fd-121">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="4c0fd-122">Lorsque la propriété Handled a la valeur false après le retour du gestionnaire d’événements, une action par défaut est effectuée.</span><span class="sxs-lookup"><span data-stu-id="4c0fd-122">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="4c0fd-123">L’action par défaut consiste à essayer de rechercher la fenêtre enfant d’arrêt de tabulation suivante dans l’application et d’essayer de déplacer le focus sur cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4c0fd-123">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="4c0fd-124">S’il n’y a aucune autre fenêtre dans laquelle déplacer le focus, le focus sera placé dans le contenu Web de WebView.</span><span class="sxs-lookup"><span data-stu-id="4c0fd-124">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="4c0fd-125">Raison</span><span class="sxs-lookup"><span data-stu-id="4c0fd-125">Reason</span></span> 

<span data-ttu-id="4c0fd-126">La raison pour laquelle WebView a déclenché l’événement MoveFocus demandé.</span><span class="sxs-lookup"><span data-stu-id="4c0fd-126">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="4c0fd-127">[raison](#reason) du CoreWebView2MoveFocusReason public</span><span class="sxs-lookup"><span data-stu-id="4c0fd-127">public CoreWebView2MoveFocusReason [Reason](#reason)</span></span>

