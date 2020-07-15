---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 5d052488d23f3d016ba2fd71eb929d5aa2ebea6e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877363"
---
# <span data-ttu-id="fc5c0-104">0.8.355-interface IWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="fc5c0-104">0.8.355 - interface IWebView2AcceleratorKeyPressedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="fc5c0-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="fc5c0-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="fc5c0-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="fc5c0-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="fc5c0-107">Arguments d’événement pour l’événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="fc5c0-107">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="fc5c0-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="fc5c0-108">Summary</span></span>

 <span data-ttu-id="fc5c0-109">Ses</span><span class="sxs-lookup"><span data-stu-id="fc5c0-109">Members</span></span>                        | <span data-ttu-id="fc5c0-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="fc5c0-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fc5c0-111">get_KeyEventType</span><span class="sxs-lookup"><span data-stu-id="fc5c0-111">get_KeyEventType</span></span>](#get_keyeventtype) | <span data-ttu-id="fc5c0-112">Type d’événement de touche qui a entraîné le déclenchement de l’événement.</span><span class="sxs-lookup"><span data-stu-id="fc5c0-112">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="fc5c0-113">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="fc5c0-113">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="fc5c0-114">Le code de clé virtuelle Win32 de la clé ayant été pressée ou publiée.</span><span class="sxs-lookup"><span data-stu-id="fc5c0-114">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="fc5c0-115">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="fc5c0-115">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="fc5c0-116">Valeur LPARAM qui s’accompagne du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="fc5c0-116">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="fc5c0-117">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="fc5c0-117">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="fc5c0-118">Structure représentant les informations transmises dans le LPARAM du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="fc5c0-118">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="fc5c0-119">Poignée</span><span class="sxs-lookup"><span data-stu-id="fc5c0-119">Handle</span></span>](#handle) | <span data-ttu-id="fc5c0-120">Les appels permettent au processus de navigateur de continuer.</span><span class="sxs-lookup"><span data-stu-id="fc5c0-120">Calling this will allow the browser process to continue.</span></span>

## <span data-ttu-id="fc5c0-121">Ses</span><span class="sxs-lookup"><span data-stu-id="fc5c0-121">Members</span></span>

#### <span data-ttu-id="fc5c0-122">get_KeyEventType</span><span class="sxs-lookup"><span data-stu-id="fc5c0-122">get_KeyEventType</span></span> 

<span data-ttu-id="fc5c0-123">Type d’événement de touche qui a entraîné le déclenchement de l’événement.</span><span class="sxs-lookup"><span data-stu-id="fc5c0-123">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="fc5c0-124">[get_KeyEventType](#get_keyeventtype)par le biais du public HRESULT (WEBVIEW2_KEY_EVENT_TYPE \* KeyEventType)</span><span class="sxs-lookup"><span data-stu-id="fc5c0-124">public HRESULT [get_KeyEventType](#get_keyeventtype)(WEBVIEW2_KEY_EVENT_TYPE \* keyEventType)</span></span>

<span data-ttu-id="fc5c0-125">Il s’agit de l’une des WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN ou WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.</span><span class="sxs-lookup"><span data-stu-id="fc5c0-125">This is one of WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN, or WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.</span></span>

#### <span data-ttu-id="fc5c0-126">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="fc5c0-126">get_VirtualKey</span></span> 

<span data-ttu-id="fc5c0-127">Le code de clé virtuelle Win32 de la clé ayant été pressée ou publiée.</span><span class="sxs-lookup"><span data-stu-id="fc5c0-127">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="fc5c0-128">valeur publique HRESULT [get_VirtualKey](#get_virtualkey)(uint \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="fc5c0-128">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="fc5c0-129">Il s’agira de l’une des constantes de clé virtuelle Win32, comme VK_RETURN ou une valeur ASCII (majuscule), telle que «A».</span><span class="sxs-lookup"><span data-stu-id="fc5c0-129">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="fc5c0-130">Vous pouvez vérifier que l’utilisateur appuie sur CTRL ou Alt en appelant GetKeyState (VK_CONTROL) ou GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="fc5c0-130">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="fc5c0-131">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="fc5c0-131">get_KeyEventLParam</span></span> 

<span data-ttu-id="fc5c0-132">Valeur LPARAM qui s’accompagne du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="fc5c0-132">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="fc5c0-133">valeur publique HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int \* lParam)</span><span class="sxs-lookup"><span data-stu-id="fc5c0-133">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="fc5c0-134">Pour plus d’informations, consultez la documentation relative au WM_KEYDOWN et aux messages WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="fc5c0-134">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="fc5c0-135">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="fc5c0-135">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="fc5c0-136">Structure représentant les informations transmises dans le LPARAM du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="fc5c0-136">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="fc5c0-137">[get_PhysicalKeyStatus](#get_physicalkeystatus)par le biais du public HRESULT (WEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="fc5c0-137">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(WEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="fc5c0-138">Poignée</span><span class="sxs-lookup"><span data-stu-id="fc5c0-138">Handle</span></span> 

<span data-ttu-id="fc5c0-139">Les appels permettent au processus de navigateur de continuer.</span><span class="sxs-lookup"><span data-stu-id="fc5c0-139">Calling this will allow the browser process to continue.</span></span>

> <span data-ttu-id="fc5c0-140">[handle](#handle)HRESULT public (bool géré)</span><span class="sxs-lookup"><span data-stu-id="fc5c0-140">public HRESULT [Handle](#handle)(BOOL handled)</span></span>

<span data-ttu-id="fc5c0-141">Le passage de la valeur TRUE empêchera le navigateur d’exécuter l’action par défaut pour cette touche accélérateur.</span><span class="sxs-lookup"><span data-stu-id="fc5c0-141">Passing TRUE will prevent the browser from performing the default action for this accelerator key.</span></span> <span data-ttu-id="fc5c0-142">Si le gestionnaire d’événements renvoie sans appeler [handle ()](#handle), il est équivalent au handle d’appel (false).</span><span class="sxs-lookup"><span data-stu-id="fc5c0-142">If the event handler returns without calling [Handle()](#handle), it is equivalent to calling Handle(FALSE).</span></span> <span data-ttu-id="fc5c0-143">Le [handle d’appel ()](#handle) après son appel ou le gestionnaire d’événements renvoyé ne fera rien.</span><span class="sxs-lookup"><span data-stu-id="fc5c0-143">Calling [Handle()](#handle) after it has already been called or the event handler has returned will do nothing.</span></span>

