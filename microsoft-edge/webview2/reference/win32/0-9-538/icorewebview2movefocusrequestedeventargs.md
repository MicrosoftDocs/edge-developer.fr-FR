---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2MoveFocusRequestedEventArgs
ms.openlocfilehash: 7d86b0129c126b39ae8200550a024819e2004b49
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010025"
---
# <span data-ttu-id="c601e-104">0.9.579-interface ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="c601e-104">0.9.579 - interface ICoreWebView2MoveFocusRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="c601e-105">Arguments d’événement pour l’événement MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="c601e-105">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="c601e-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="c601e-106">Summary</span></span>

 <span data-ttu-id="c601e-107">Ses</span><span class="sxs-lookup"><span data-stu-id="c601e-107">Members</span></span>                        | <span data-ttu-id="c601e-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="c601e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c601e-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="c601e-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="c601e-110">Indiquez si l’événement a été géré par l’application.</span><span class="sxs-lookup"><span data-stu-id="c601e-110">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="c601e-111">get_Reason</span><span class="sxs-lookup"><span data-stu-id="c601e-111">get_Reason</span></span>](#get_reason) | <span data-ttu-id="c601e-112">La raison pour laquelle WebView a déclenché l’événement MoveFocus demandé.</span><span class="sxs-lookup"><span data-stu-id="c601e-112">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="c601e-113">put_Handled</span><span class="sxs-lookup"><span data-stu-id="c601e-113">put_Handled</span></span>](#put_handled) | <span data-ttu-id="c601e-114">Définissez la propriété Handled.</span><span class="sxs-lookup"><span data-stu-id="c601e-114">Set the Handled property.</span></span>

## <span data-ttu-id="c601e-115">Ses</span><span class="sxs-lookup"><span data-stu-id="c601e-115">Members</span></span>

#### <span data-ttu-id="c601e-116">get_Handled</span><span class="sxs-lookup"><span data-stu-id="c601e-116">get_Handled</span></span> 

<span data-ttu-id="c601e-117">Indiquez si l’événement a été géré par l’application.</span><span class="sxs-lookup"><span data-stu-id="c601e-117">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="c601e-118">valeur publique HRESULT [get_Handled](#get_handled)(bool \* value)</span><span class="sxs-lookup"><span data-stu-id="c601e-118">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="c601e-119">Si l’application a déplacé le focus vers l’emplacement souhaité, elle doit définir la propriété Handled sur TRUE.</span><span class="sxs-lookup"><span data-stu-id="c601e-119">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="c601e-120">Lorsque la propriété Handled a la valeur false après le retour du gestionnaire d’événements, une action par défaut est effectuée.</span><span class="sxs-lookup"><span data-stu-id="c601e-120">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="c601e-121">L’action par défaut consiste à essayer de rechercher la fenêtre enfant d’arrêt de tabulation suivante dans l’application et d’essayer de déplacer le focus sur cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c601e-121">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="c601e-122">S’il n’y a aucune autre fenêtre dans laquelle déplacer le focus, le focus sera placé dans le contenu Web de WebView.</span><span class="sxs-lookup"><span data-stu-id="c601e-122">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="c601e-123">get_Reason</span><span class="sxs-lookup"><span data-stu-id="c601e-123">get_Reason</span></span> 

<span data-ttu-id="c601e-124">La raison pour laquelle WebView a déclenché l’événement MoveFocus demandé.</span><span class="sxs-lookup"><span data-stu-id="c601e-124">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="c601e-125">valeur publique HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \* value)</span><span class="sxs-lookup"><span data-stu-id="c601e-125">public HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="c601e-126">put_Handled</span><span class="sxs-lookup"><span data-stu-id="c601e-126">put_Handled</span></span> 

<span data-ttu-id="c601e-127">Définissez la propriété Handled.</span><span class="sxs-lookup"><span data-stu-id="c601e-127">Set the Handled property.</span></span>

> <span data-ttu-id="c601e-128">[put_Handled](#put_handled)des valeurs HRESULT publiques (valeur booléenne)</span><span class="sxs-lookup"><span data-stu-id="c601e-128">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>

