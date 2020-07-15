---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2MoveFocusRequestedEventArgs
ms.openlocfilehash: eda4d00db8e8c52f9ce0b6511acb3d89b497fb1a
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878735"
---
# <span data-ttu-id="d339c-104">interface ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d339c-104">interface ICoreWebView2MoveFocusRequestedEventArgs</span></span> 

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="d339c-105">Arguments d’événement pour l’événement MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="d339c-105">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="d339c-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="d339c-106">Summary</span></span>

 <span data-ttu-id="d339c-107">Ses</span><span class="sxs-lookup"><span data-stu-id="d339c-107">Members</span></span>                        | <span data-ttu-id="d339c-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="d339c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d339c-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="d339c-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="d339c-110">Indiquez si l’événement a été géré par l’application.</span><span class="sxs-lookup"><span data-stu-id="d339c-110">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="d339c-111">get_Reason</span><span class="sxs-lookup"><span data-stu-id="d339c-111">get_Reason</span></span>](#get_reason) | <span data-ttu-id="d339c-112">La raison pour laquelle WebView a déclenché l’événement MoveFocus demandé.</span><span class="sxs-lookup"><span data-stu-id="d339c-112">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="d339c-113">put_Handled</span><span class="sxs-lookup"><span data-stu-id="d339c-113">put_Handled</span></span>](#put_handled) | <span data-ttu-id="d339c-114">Définissez la propriété Handled.</span><span class="sxs-lookup"><span data-stu-id="d339c-114">Set the Handled property.</span></span>

## <span data-ttu-id="d339c-115">Ses</span><span class="sxs-lookup"><span data-stu-id="d339c-115">Members</span></span>

#### <span data-ttu-id="d339c-116">get_Handled</span><span class="sxs-lookup"><span data-stu-id="d339c-116">get_Handled</span></span> 

<span data-ttu-id="d339c-117">Indiquez si l’événement a été géré par l’application.</span><span class="sxs-lookup"><span data-stu-id="d339c-117">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="d339c-118">valeur publique HRESULT [get_Handled](#get_handled)(bool \* value)</span><span class="sxs-lookup"><span data-stu-id="d339c-118">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="d339c-119">Si l’application a déplacé le focus vers l’emplacement souhaité, elle doit définir la propriété Handled sur TRUE.</span><span class="sxs-lookup"><span data-stu-id="d339c-119">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="d339c-120">Lorsque la propriété Handled a la valeur false après le retour du gestionnaire d’événements, une action par défaut est effectuée.</span><span class="sxs-lookup"><span data-stu-id="d339c-120">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="d339c-121">L’action par défaut consiste à essayer de rechercher la fenêtre enfant d’arrêt de tabulation suivante dans l’application et d’essayer de déplacer le focus sur cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d339c-121">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="d339c-122">S’il n’y a aucune autre fenêtre dans laquelle déplacer le focus, le focus sera placé dans le contenu Web de WebView.</span><span class="sxs-lookup"><span data-stu-id="d339c-122">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="d339c-123">get_Reason</span><span class="sxs-lookup"><span data-stu-id="d339c-123">get_Reason</span></span> 

<span data-ttu-id="d339c-124">La raison pour laquelle WebView a déclenché l’événement MoveFocus demandé.</span><span class="sxs-lookup"><span data-stu-id="d339c-124">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="d339c-125">valeur publique HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \* value)</span><span class="sxs-lookup"><span data-stu-id="d339c-125">public HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="d339c-126">put_Handled</span><span class="sxs-lookup"><span data-stu-id="d339c-126">put_Handled</span></span> 

<span data-ttu-id="d339c-127">Définissez la propriété Handled.</span><span class="sxs-lookup"><span data-stu-id="d339c-127">Set the Handled property.</span></span>

> <span data-ttu-id="d339c-128">[put_Handled](#put_handled)des valeurs HRESULT publiques (valeur booléenne)</span><span class="sxs-lookup"><span data-stu-id="d339c-128">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>

