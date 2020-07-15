---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: fe0c0fae0ec33cbc5ba50ca163b3f4fc8baa61b9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880954"
---
# <span data-ttu-id="6f8c9-104">0.9.430-interface ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="6f8c9-104">0.9.430 - interface ICoreWebView2MoveFocusRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="6f8c9-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="6f8c9-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="6f8c9-107">Arguments d’événement pour l’événement MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-107">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="6f8c9-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="6f8c9-108">Summary</span></span>

 <span data-ttu-id="6f8c9-109">Ses</span><span class="sxs-lookup"><span data-stu-id="6f8c9-109">Members</span></span>                        | <span data-ttu-id="6f8c9-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="6f8c9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6f8c9-111">get_Reason</span><span class="sxs-lookup"><span data-stu-id="6f8c9-111">get_Reason</span></span>](#get_reason) | <span data-ttu-id="6f8c9-112">La raison pour laquelle WebView a déclenché l’événement MoveFocus demandé.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-112">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="6f8c9-113">get_Handled</span><span class="sxs-lookup"><span data-stu-id="6f8c9-113">get_Handled</span></span>](#get_handled) | <span data-ttu-id="6f8c9-114">Indiquez si l’événement a été géré par l’application.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-114">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="6f8c9-115">put_Handled</span><span class="sxs-lookup"><span data-stu-id="6f8c9-115">put_Handled</span></span>](#put_handled) | <span data-ttu-id="6f8c9-116">Définissez la propriété Handled.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-116">Set the Handled property.</span></span>

## <span data-ttu-id="6f8c9-117">Ses</span><span class="sxs-lookup"><span data-stu-id="6f8c9-117">Members</span></span>

#### <span data-ttu-id="6f8c9-118">get_Reason</span><span class="sxs-lookup"><span data-stu-id="6f8c9-118">get_Reason</span></span> 

<span data-ttu-id="6f8c9-119">La raison pour laquelle WebView a déclenché l’événement MoveFocus demandé.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-119">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="6f8c9-120">valeur publique HRESULT [get_Reason](#get_reason)(CORE_WEBVIEW2_MOVE_FOCUS_REASON \* value)</span><span class="sxs-lookup"><span data-stu-id="6f8c9-120">public HRESULT [get_Reason](#get_reason)(CORE_WEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="6f8c9-121">get_Handled</span><span class="sxs-lookup"><span data-stu-id="6f8c9-121">get_Handled</span></span> 

<span data-ttu-id="6f8c9-122">Indiquez si l’événement a été géré par l’application.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-122">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="6f8c9-123">valeur publique HRESULT [get_Handled](#get_handled)(bool \* value)</span><span class="sxs-lookup"><span data-stu-id="6f8c9-123">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="6f8c9-124">Si l’application a déplacé le focus vers l’emplacement souhaité, elle doit définir la propriété Handled sur TRUE.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-124">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="6f8c9-125">Lorsque la propriété Handled a la valeur false après le retour du gestionnaire d’événements, une action par défaut est effectuée.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-125">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="6f8c9-126">L’action par défaut consiste à essayer de rechercher la fenêtre enfant d’arrêt de tabulation suivante dans l’application et d’essayer de déplacer le focus sur cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-126">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="6f8c9-127">S’il n’y a aucune autre fenêtre dans laquelle déplacer le focus, le focus sera placé dans le contenu Web de WebView.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-127">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="6f8c9-128">put_Handled</span><span class="sxs-lookup"><span data-stu-id="6f8c9-128">put_Handled</span></span> 

<span data-ttu-id="6f8c9-129">Définissez la propriété Handled.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-129">Set the Handled property.</span></span>

> <span data-ttu-id="6f8c9-130">[put_Handled](#put_handled)des valeurs HRESULT publiques (valeur booléenne)</span><span class="sxs-lookup"><span data-stu-id="6f8c9-130">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>

