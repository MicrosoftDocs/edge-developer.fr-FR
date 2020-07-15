---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: dc6c904150605dc05b2fef00600785b9840f0eb8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880527"
---
# <span data-ttu-id="3f4e0-104">0.9.515-interface ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="3f4e0-104">0.9.515 - interface ICoreWebView2MoveFocusRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="3f4e0-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="3f4e0-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="3f4e0-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="3f4e0-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="3f4e0-107">Arguments d’événement pour l’événement MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="3f4e0-107">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="3f4e0-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="3f4e0-108">Summary</span></span>

 <span data-ttu-id="3f4e0-109">Ses</span><span class="sxs-lookup"><span data-stu-id="3f4e0-109">Members</span></span>                        | <span data-ttu-id="3f4e0-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="3f4e0-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3f4e0-111">get_Handled</span><span class="sxs-lookup"><span data-stu-id="3f4e0-111">get_Handled</span></span>](#get_handled) | <span data-ttu-id="3f4e0-112">Indiquez si l’événement a été géré par l’application.</span><span class="sxs-lookup"><span data-stu-id="3f4e0-112">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="3f4e0-113">get_Reason</span><span class="sxs-lookup"><span data-stu-id="3f4e0-113">get_Reason</span></span>](#get_reason) | <span data-ttu-id="3f4e0-114">La raison pour laquelle WebView a déclenché l’événement MoveFocus demandé.</span><span class="sxs-lookup"><span data-stu-id="3f4e0-114">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="3f4e0-115">put_Handled</span><span class="sxs-lookup"><span data-stu-id="3f4e0-115">put_Handled</span></span>](#put_handled) | <span data-ttu-id="3f4e0-116">Définissez la propriété Handled.</span><span class="sxs-lookup"><span data-stu-id="3f4e0-116">Set the Handled property.</span></span>

## <span data-ttu-id="3f4e0-117">Ses</span><span class="sxs-lookup"><span data-stu-id="3f4e0-117">Members</span></span>

#### <span data-ttu-id="3f4e0-118">get_Handled</span><span class="sxs-lookup"><span data-stu-id="3f4e0-118">get_Handled</span></span> 

<span data-ttu-id="3f4e0-119">Indiquez si l’événement a été géré par l’application.</span><span class="sxs-lookup"><span data-stu-id="3f4e0-119">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="3f4e0-120">valeur publique HRESULT [get_Handled](#get_handled)(bool \* value)</span><span class="sxs-lookup"><span data-stu-id="3f4e0-120">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="3f4e0-121">Si l’application a déplacé le focus vers l’emplacement souhaité, elle doit définir la propriété Handled sur TRUE.</span><span class="sxs-lookup"><span data-stu-id="3f4e0-121">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="3f4e0-122">Lorsque la propriété Handled a la valeur false après le retour du gestionnaire d’événements, une action par défaut est effectuée.</span><span class="sxs-lookup"><span data-stu-id="3f4e0-122">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="3f4e0-123">L’action par défaut consiste à essayer de rechercher la fenêtre enfant d’arrêt de tabulation suivante dans l’application et d’essayer de déplacer le focus sur cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3f4e0-123">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="3f4e0-124">S’il n’y a aucune autre fenêtre dans laquelle déplacer le focus, le focus sera placé dans le contenu Web de WebView.</span><span class="sxs-lookup"><span data-stu-id="3f4e0-124">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="3f4e0-125">get_Reason</span><span class="sxs-lookup"><span data-stu-id="3f4e0-125">get_Reason</span></span> 

<span data-ttu-id="3f4e0-126">La raison pour laquelle WebView a déclenché l’événement MoveFocus demandé.</span><span class="sxs-lookup"><span data-stu-id="3f4e0-126">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="3f4e0-127">valeur publique HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \* value)</span><span class="sxs-lookup"><span data-stu-id="3f4e0-127">public HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="3f4e0-128">put_Handled</span><span class="sxs-lookup"><span data-stu-id="3f4e0-128">put_Handled</span></span> 

<span data-ttu-id="3f4e0-129">Définissez la propriété Handled.</span><span class="sxs-lookup"><span data-stu-id="3f4e0-129">Set the Handled property.</span></span>

> <span data-ttu-id="3f4e0-130">[put_Handled](#put_handled)des valeurs HRESULT publiques (valeur booléenne)</span><span class="sxs-lookup"><span data-stu-id="3f4e0-130">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>

