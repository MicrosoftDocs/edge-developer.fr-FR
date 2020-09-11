---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs
ms.openlocfilehash: c7f318f44ce0469a216fe8dda7870c4adbdebcc0
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011893"
---
# <span data-ttu-id="feffb-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="feffb-104">Microsoft.Web.WebView2.Core.CoreWebView2MoveFocusRequestedEventArgs class</span></span> 

<span data-ttu-id="feffb-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="feffb-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="feffb-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="feffb-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="feffb-107">Arguments d’événement pour l’événement MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="feffb-107">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="feffb-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="feffb-108">Summary</span></span>

 <span data-ttu-id="feffb-109">Ses</span><span class="sxs-lookup"><span data-stu-id="feffb-109">Members</span></span>                        | <span data-ttu-id="feffb-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="feffb-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="feffb-111">Handled</span><span class="sxs-lookup"><span data-stu-id="feffb-111">Handled</span></span>](#handled) | <span data-ttu-id="feffb-112">Indiquez si l’événement a été géré par l’application.</span><span class="sxs-lookup"><span data-stu-id="feffb-112">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="feffb-113">Raison</span><span class="sxs-lookup"><span data-stu-id="feffb-113">Reason</span></span>](#reason) | <span data-ttu-id="feffb-114">La raison pour laquelle WebView a déclenché l’événement MoveFocus demandé.</span><span class="sxs-lookup"><span data-stu-id="feffb-114">The reason for WebView to fire the MoveFocus Requested event.</span></span>

## <span data-ttu-id="feffb-115">Ses</span><span class="sxs-lookup"><span data-stu-id="feffb-115">Members</span></span>

#### <span data-ttu-id="feffb-116">Handled</span><span class="sxs-lookup"><span data-stu-id="feffb-116">Handled</span></span> 

<span data-ttu-id="feffb-117">Indiquez si l’événement a été géré par l’application.</span><span class="sxs-lookup"><span data-stu-id="feffb-117">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="feffb-118">propriété booléenne [gérée](#handled)</span><span class="sxs-lookup"><span data-stu-id="feffb-118">public bool [Handled](#handled)</span></span>

<span data-ttu-id="feffb-119">Si l’application a déplacé le focus vers l’emplacement souhaité, elle doit définir la propriété Handled sur TRUE.</span><span class="sxs-lookup"><span data-stu-id="feffb-119">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="feffb-120">Lorsque la propriété Handled a la valeur false après le retour du gestionnaire d’événements, une action par défaut est effectuée.</span><span class="sxs-lookup"><span data-stu-id="feffb-120">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="feffb-121">L’action par défaut consiste à essayer de rechercher la fenêtre enfant d’arrêt de tabulation suivante dans l’application et d’essayer de déplacer le focus sur cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="feffb-121">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="feffb-122">S’il n’y a aucune autre fenêtre dans laquelle déplacer le focus, le focus sera placé dans le contenu Web de WebView.</span><span class="sxs-lookup"><span data-stu-id="feffb-122">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="feffb-123">Raison</span><span class="sxs-lookup"><span data-stu-id="feffb-123">Reason</span></span> 

<span data-ttu-id="feffb-124">La raison pour laquelle WebView a déclenché l’événement MoveFocus demandé.</span><span class="sxs-lookup"><span data-stu-id="feffb-124">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="feffb-125">[raison](#reason) du CoreWebView2MoveFocusReason public</span><span class="sxs-lookup"><span data-stu-id="feffb-125">public CoreWebView2MoveFocusReason [Reason](#reason)</span></span>

