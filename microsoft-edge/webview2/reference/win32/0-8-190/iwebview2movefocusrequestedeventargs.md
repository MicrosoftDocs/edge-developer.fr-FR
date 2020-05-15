---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 2e3afec26b0e09a80182118f74b6f50733b0c71a
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653447"
---
# <span data-ttu-id="0a29e-104">interface IWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="0a29e-104">interface IWebView2MoveFocusRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="0a29e-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="0a29e-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="0a29e-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="0a29e-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="0a29e-107">Arguments d’événement pour l’événement MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="0a29e-107">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="0a29e-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="0a29e-108">Summary</span></span>

 <span data-ttu-id="0a29e-109">Ses</span><span class="sxs-lookup"><span data-stu-id="0a29e-109">Members</span></span>                        | <span data-ttu-id="0a29e-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="0a29e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0a29e-111">get_Reason</span><span class="sxs-lookup"><span data-stu-id="0a29e-111">get_Reason</span></span>](#get_reason) | <span data-ttu-id="0a29e-112">La raison pour laquelle WebView a déclenché l’événement MoveFocus demandé.</span><span class="sxs-lookup"><span data-stu-id="0a29e-112">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="0a29e-113">get_Handled</span><span class="sxs-lookup"><span data-stu-id="0a29e-113">get_Handled</span></span>](#get_handled) | <span data-ttu-id="0a29e-114">Indiquez si l’événement a été géré par l’application.</span><span class="sxs-lookup"><span data-stu-id="0a29e-114">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="0a29e-115">put_Handled</span><span class="sxs-lookup"><span data-stu-id="0a29e-115">put_Handled</span></span>](#put_handled) | <span data-ttu-id="0a29e-116">Définissez la propriété Handled.</span><span class="sxs-lookup"><span data-stu-id="0a29e-116">Set the Handled property.</span></span>

## <span data-ttu-id="0a29e-117">Ses</span><span class="sxs-lookup"><span data-stu-id="0a29e-117">Members</span></span>

#### <span data-ttu-id="0a29e-118">get_Reason</span><span class="sxs-lookup"><span data-stu-id="0a29e-118">get_Reason</span></span> 

<span data-ttu-id="0a29e-119">La raison pour laquelle WebView a déclenché l’événement MoveFocus demandé.</span><span class="sxs-lookup"><span data-stu-id="0a29e-119">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="0a29e-120">valeur publique HRESULT [get_Reason](#get_reason)(WEBVIEW2_MOVE_FOCUS_REASON \* value)</span><span class="sxs-lookup"><span data-stu-id="0a29e-120">public HRESULT [get_Reason](#get_reason)(WEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="0a29e-121">get_Handled</span><span class="sxs-lookup"><span data-stu-id="0a29e-121">get_Handled</span></span> 

<span data-ttu-id="0a29e-122">Indiquez si l’événement a été géré par l’application.</span><span class="sxs-lookup"><span data-stu-id="0a29e-122">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="0a29e-123">valeur publique HRESULT [get_Handled](#get_handled)(bool \* value)</span><span class="sxs-lookup"><span data-stu-id="0a29e-123">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="0a29e-124">Si l’application a déplacé le focus vers l’emplacement souhaité, elle doit définir la propriété Handled sur TRUE.</span><span class="sxs-lookup"><span data-stu-id="0a29e-124">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="0a29e-125">Lorsque la propriété Handled a la valeur false après le retour du gestionnaire d’événements, une action par défaut est effectuée.</span><span class="sxs-lookup"><span data-stu-id="0a29e-125">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="0a29e-126">L’action par défaut consiste à essayer de rechercher la fenêtre enfant d’arrêt de tabulation suivante dans l’application et d’essayer de déplacer le focus sur cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="0a29e-126">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="0a29e-127">S’il n’y a aucune autre fenêtre dans laquelle déplacer le focus, le focus sera placé dans le contenu Web de WebView.</span><span class="sxs-lookup"><span data-stu-id="0a29e-127">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="0a29e-128">put_Handled</span><span class="sxs-lookup"><span data-stu-id="0a29e-128">put_Handled</span></span> 

<span data-ttu-id="0a29e-129">Définissez la propriété Handled.</span><span class="sxs-lookup"><span data-stu-id="0a29e-129">Set the Handled property.</span></span>

> <span data-ttu-id="0a29e-130">[put_Handled](#put_handled)des valeurs HRESULT publiques (valeur booléenne)</span><span class="sxs-lookup"><span data-stu-id="0a29e-130">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>

