---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 1d3cae59c0906a94414ff135ef8d84fac7cc89b4
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885071"
---
# <span data-ttu-id="cd283-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="cd283-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2MoveFocusRequestedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="cd283-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="cd283-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="cd283-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="cd283-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="cd283-107">Arguments d’événement pour l’événement MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="cd283-107">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="cd283-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="cd283-108">Summary</span></span>

 <span data-ttu-id="cd283-109">Ses</span><span class="sxs-lookup"><span data-stu-id="cd283-109">Members</span></span>                        | <span data-ttu-id="cd283-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="cd283-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cd283-111">Handled</span><span class="sxs-lookup"><span data-stu-id="cd283-111">Handled</span></span>](#handled) | <span data-ttu-id="cd283-112">Indiquez si l’événement a été géré par l’application.</span><span class="sxs-lookup"><span data-stu-id="cd283-112">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="cd283-113">Raison</span><span class="sxs-lookup"><span data-stu-id="cd283-113">Reason</span></span>](#reason) | <span data-ttu-id="cd283-114">La raison pour laquelle WebView a déclenché l’événement MoveFocus demandé.</span><span class="sxs-lookup"><span data-stu-id="cd283-114">The reason for WebView to fire the MoveFocus Requested event.</span></span>

## <span data-ttu-id="cd283-115">Ses</span><span class="sxs-lookup"><span data-stu-id="cd283-115">Members</span></span>

#### <span data-ttu-id="cd283-116">Handled</span><span class="sxs-lookup"><span data-stu-id="cd283-116">Handled</span></span> 

<span data-ttu-id="cd283-117">Indiquez si l’événement a été géré par l’application.</span><span class="sxs-lookup"><span data-stu-id="cd283-117">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="cd283-118">propriété booléenne [gérée](#handled)</span><span class="sxs-lookup"><span data-stu-id="cd283-118">public bool [Handled](#handled)</span></span>

<span data-ttu-id="cd283-119">Si l’application a déplacé le focus vers l’emplacement souhaité, elle doit définir la propriété Handled sur TRUE.</span><span class="sxs-lookup"><span data-stu-id="cd283-119">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="cd283-120">Lorsque la propriété Handled a la valeur false après le retour du gestionnaire d’événements, une action par défaut est effectuée.</span><span class="sxs-lookup"><span data-stu-id="cd283-120">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="cd283-121">L’action par défaut consiste à essayer de rechercher la fenêtre enfant d’arrêt de tabulation suivante dans l’application et d’essayer de déplacer le focus sur cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cd283-121">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="cd283-122">S’il n’y a aucune autre fenêtre dans laquelle déplacer le focus, le focus sera placé dans le contenu Web de WebView.</span><span class="sxs-lookup"><span data-stu-id="cd283-122">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="cd283-123">Raison</span><span class="sxs-lookup"><span data-stu-id="cd283-123">Reason</span></span> 

<span data-ttu-id="cd283-124">La raison pour laquelle WebView a déclenché l’événement MoveFocus demandé.</span><span class="sxs-lookup"><span data-stu-id="cd283-124">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="cd283-125">[raison](#reason) du CoreWebView2MoveFocusReason public</span><span class="sxs-lookup"><span data-stu-id="cd283-125">public CoreWebView2MoveFocusReason [Reason](#reason)</span></span>

