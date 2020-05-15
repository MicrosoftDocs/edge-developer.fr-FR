---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 8ca8de3c430eda3bde089ca53501d880f4d8e35e
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653481"
---
# <span data-ttu-id="05598-104">interface ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="05598-104">interface ICoreWebView2MoveFocusRequestedEventArgs</span></span> 

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="05598-105">Arguments d’événement pour l’événement MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="05598-105">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="05598-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="05598-106">Summary</span></span>

 <span data-ttu-id="05598-107">Ses</span><span class="sxs-lookup"><span data-stu-id="05598-107">Members</span></span>                        | <span data-ttu-id="05598-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="05598-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="05598-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="05598-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="05598-110">Indiquez si l’événement a été géré par l’application.</span><span class="sxs-lookup"><span data-stu-id="05598-110">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="05598-111">get_Reason</span><span class="sxs-lookup"><span data-stu-id="05598-111">get_Reason</span></span>](#get_reason) | <span data-ttu-id="05598-112">La raison pour laquelle WebView a déclenché l’événement MoveFocus demandé.</span><span class="sxs-lookup"><span data-stu-id="05598-112">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="05598-113">put_Handled</span><span class="sxs-lookup"><span data-stu-id="05598-113">put_Handled</span></span>](#put_handled) | <span data-ttu-id="05598-114">Définissez la propriété Handled.</span><span class="sxs-lookup"><span data-stu-id="05598-114">Set the Handled property.</span></span>

## <span data-ttu-id="05598-115">Ses</span><span class="sxs-lookup"><span data-stu-id="05598-115">Members</span></span>

#### <span data-ttu-id="05598-116">get_Handled</span><span class="sxs-lookup"><span data-stu-id="05598-116">get_Handled</span></span> 

<span data-ttu-id="05598-117">Indiquez si l’événement a été géré par l’application.</span><span class="sxs-lookup"><span data-stu-id="05598-117">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="05598-118">valeur publique HRESULT [get_Handled](#get_handled)(bool \* value)</span><span class="sxs-lookup"><span data-stu-id="05598-118">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="05598-119">Si l’application a déplacé le focus vers l’emplacement souhaité, elle doit définir la propriété Handled sur TRUE.</span><span class="sxs-lookup"><span data-stu-id="05598-119">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="05598-120">Lorsque la propriété Handled a la valeur false après le retour du gestionnaire d’événements, une action par défaut est effectuée.</span><span class="sxs-lookup"><span data-stu-id="05598-120">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="05598-121">L’action par défaut consiste à essayer de rechercher la fenêtre enfant d’arrêt de tabulation suivante dans l’application et d’essayer de déplacer le focus sur cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="05598-121">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="05598-122">S’il n’y a aucune autre fenêtre dans laquelle déplacer le focus, le focus sera placé dans le contenu Web de WebView.</span><span class="sxs-lookup"><span data-stu-id="05598-122">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="05598-123">get_Reason</span><span class="sxs-lookup"><span data-stu-id="05598-123">get_Reason</span></span> 

<span data-ttu-id="05598-124">La raison pour laquelle WebView a déclenché l’événement MoveFocus demandé.</span><span class="sxs-lookup"><span data-stu-id="05598-124">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="05598-125">valeur publique HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \* value)</span><span class="sxs-lookup"><span data-stu-id="05598-125">public HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="05598-126">put_Handled</span><span class="sxs-lookup"><span data-stu-id="05598-126">put_Handled</span></span> 

<span data-ttu-id="05598-127">Définissez la propriété Handled.</span><span class="sxs-lookup"><span data-stu-id="05598-127">Set the Handled property.</span></span>

> <span data-ttu-id="05598-128">[put_Handled](#put_handled)des valeurs HRESULT publiques (valeur booléenne)</span><span class="sxs-lookup"><span data-stu-id="05598-128">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>

