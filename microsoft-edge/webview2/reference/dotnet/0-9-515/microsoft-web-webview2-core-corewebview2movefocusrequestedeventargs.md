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
ms.openlocfilehash: 69835f6fe22246f43e3df9c45a7fde7a674ac0e5
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697643"
---
# <span data-ttu-id="8fec4-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8fec4-104">Microsoft.Web.WebView2.Core.CoreWebView2MoveFocusRequestedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="8fec4-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="8fec4-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="8fec4-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="8fec4-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="8fec4-107">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="8fec4-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="8fec4-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="8fec4-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="8fec4-109">Arguments d’événement pour l’événement MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="8fec4-109">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="8fec4-110">Résumé</span><span class="sxs-lookup"><span data-stu-id="8fec4-110">Summary</span></span>

 <span data-ttu-id="8fec4-111">Ses</span><span class="sxs-lookup"><span data-stu-id="8fec4-111">Members</span></span>                        | <span data-ttu-id="8fec4-112">Descriptions</span><span class="sxs-lookup"><span data-stu-id="8fec4-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8fec4-113">Handled</span><span class="sxs-lookup"><span data-stu-id="8fec4-113">Handled</span></span>](#handled) | <span data-ttu-id="8fec4-114">Indiquez si l’événement a été géré par l’application.</span><span class="sxs-lookup"><span data-stu-id="8fec4-114">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="8fec4-115">Raison</span><span class="sxs-lookup"><span data-stu-id="8fec4-115">Reason</span></span>](#reason) | <span data-ttu-id="8fec4-116">La raison pour laquelle WebView a déclenché l’événement MoveFocus demandé.</span><span class="sxs-lookup"><span data-stu-id="8fec4-116">The reason for WebView to fire the MoveFocus Requested event.</span></span>

## <span data-ttu-id="8fec4-117">Ses</span><span class="sxs-lookup"><span data-stu-id="8fec4-117">Members</span></span>

#### <span data-ttu-id="8fec4-118">Handled</span><span class="sxs-lookup"><span data-stu-id="8fec4-118">Handled</span></span> 

<span data-ttu-id="8fec4-119">Indiquez si l’événement a été géré par l’application.</span><span class="sxs-lookup"><span data-stu-id="8fec4-119">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="8fec4-120">propriété booléenne [gérée](#handled)</span><span class="sxs-lookup"><span data-stu-id="8fec4-120">public bool [Handled](#handled)</span></span>

<span data-ttu-id="8fec4-121">Si l’application a déplacé le focus vers l’emplacement souhaité, elle doit définir la propriété Handled sur TRUE.</span><span class="sxs-lookup"><span data-stu-id="8fec4-121">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="8fec4-122">Lorsque la propriété Handled a la valeur false après le retour du gestionnaire d’événements, une action par défaut est effectuée.</span><span class="sxs-lookup"><span data-stu-id="8fec4-122">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="8fec4-123">L’action par défaut consiste à essayer de rechercher la fenêtre enfant d’arrêt de tabulation suivante dans l’application et d’essayer de déplacer le focus sur cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8fec4-123">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="8fec4-124">S’il n’y a aucune autre fenêtre dans laquelle déplacer le focus, le focus sera placé dans le contenu Web de WebView.</span><span class="sxs-lookup"><span data-stu-id="8fec4-124">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="8fec4-125">Raison</span><span class="sxs-lookup"><span data-stu-id="8fec4-125">Reason</span></span> 

<span data-ttu-id="8fec4-126">La raison pour laquelle WebView a déclenché l’événement MoveFocus demandé.</span><span class="sxs-lookup"><span data-stu-id="8fec4-126">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="8fec4-127">[raison](#reason) du CoreWebView2MoveFocusReason public</span><span class="sxs-lookup"><span data-stu-id="8fec4-127">public CoreWebView2MoveFocusReason [Reason](#reason)</span></span>

