---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 643e2e998cc8ca70bfd90fbcb9bbf1f6c690322b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884546"
---
# <span data-ttu-id="d2f05-104">0.9.430-interface ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d2f05-104">0.9.430 - interface ICoreWebView2MoveFocusRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="d2f05-105">Arguments d’événement pour l’événement MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="d2f05-105">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="d2f05-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="d2f05-106">Summary</span></span>

 <span data-ttu-id="d2f05-107">Ses</span><span class="sxs-lookup"><span data-stu-id="d2f05-107">Members</span></span>                        | <span data-ttu-id="d2f05-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="d2f05-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d2f05-109">get_Reason</span><span class="sxs-lookup"><span data-stu-id="d2f05-109">get_Reason</span></span>](#get_reason) | <span data-ttu-id="d2f05-110">La raison pour laquelle WebView a déclenché l’événement MoveFocus demandé.</span><span class="sxs-lookup"><span data-stu-id="d2f05-110">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="d2f05-111">get_Handled</span><span class="sxs-lookup"><span data-stu-id="d2f05-111">get_Handled</span></span>](#get_handled) | <span data-ttu-id="d2f05-112">Indiquez si l’événement a été géré par l’application.</span><span class="sxs-lookup"><span data-stu-id="d2f05-112">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="d2f05-113">put_Handled</span><span class="sxs-lookup"><span data-stu-id="d2f05-113">put_Handled</span></span>](#put_handled) | <span data-ttu-id="d2f05-114">Définissez la propriété Handled.</span><span class="sxs-lookup"><span data-stu-id="d2f05-114">Set the Handled property.</span></span>

## <span data-ttu-id="d2f05-115">Ses</span><span class="sxs-lookup"><span data-stu-id="d2f05-115">Members</span></span>

#### <span data-ttu-id="d2f05-116">get_Reason</span><span class="sxs-lookup"><span data-stu-id="d2f05-116">get_Reason</span></span> 

<span data-ttu-id="d2f05-117">La raison pour laquelle WebView a déclenché l’événement MoveFocus demandé.</span><span class="sxs-lookup"><span data-stu-id="d2f05-117">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="d2f05-118">valeur publique HRESULT [get_Reason](#get_reason)(CORE_WEBVIEW2_MOVE_FOCUS_REASON \* value)</span><span class="sxs-lookup"><span data-stu-id="d2f05-118">public HRESULT [get_Reason](#get_reason)(CORE_WEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="d2f05-119">get_Handled</span><span class="sxs-lookup"><span data-stu-id="d2f05-119">get_Handled</span></span> 

<span data-ttu-id="d2f05-120">Indiquez si l’événement a été géré par l’application.</span><span class="sxs-lookup"><span data-stu-id="d2f05-120">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="d2f05-121">valeur publique HRESULT [get_Handled](#get_handled)(bool \* value)</span><span class="sxs-lookup"><span data-stu-id="d2f05-121">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="d2f05-122">Si l’application a déplacé le focus vers l’emplacement souhaité, elle doit définir la propriété Handled sur TRUE.</span><span class="sxs-lookup"><span data-stu-id="d2f05-122">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="d2f05-123">Lorsque la propriété Handled a la valeur false après le retour du gestionnaire d’événements, une action par défaut est effectuée.</span><span class="sxs-lookup"><span data-stu-id="d2f05-123">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="d2f05-124">L’action par défaut consiste à essayer de rechercher la fenêtre enfant d’arrêt de tabulation suivante dans l’application et d’essayer de déplacer le focus sur cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d2f05-124">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="d2f05-125">S’il n’y a aucune autre fenêtre dans laquelle déplacer le focus, le focus sera placé dans le contenu Web de WebView.</span><span class="sxs-lookup"><span data-stu-id="d2f05-125">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="d2f05-126">put_Handled</span><span class="sxs-lookup"><span data-stu-id="d2f05-126">put_Handled</span></span> 

<span data-ttu-id="d2f05-127">Définissez la propriété Handled.</span><span class="sxs-lookup"><span data-stu-id="d2f05-127">Set the Handled property.</span></span>

> <span data-ttu-id="d2f05-128">[put_Handled](#put_handled)des valeurs HRESULT publiques (valeur booléenne)</span><span class="sxs-lookup"><span data-stu-id="d2f05-128">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>

