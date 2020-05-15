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
ms.openlocfilehash: 5b15d6205306e558d1d8709cceed8b7a68a77bce
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653461"
---
# <span data-ttu-id="b3a45-104">interface IWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="b3a45-104">interface IWebView2AcceleratorKeyPressedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="b3a45-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="b3a45-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="b3a45-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="b3a45-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="b3a45-107">Arguments d’événement pour l’événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="b3a45-107">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="b3a45-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="b3a45-108">Summary</span></span>

 <span data-ttu-id="b3a45-109">Ses</span><span class="sxs-lookup"><span data-stu-id="b3a45-109">Members</span></span>                        | <span data-ttu-id="b3a45-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="b3a45-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b3a45-111">get_KeyEventType</span><span class="sxs-lookup"><span data-stu-id="b3a45-111">get_KeyEventType</span></span>](#get_keyeventtype) | <span data-ttu-id="b3a45-112">Type d’événement de touche qui a entraîné le déclenchement de l’événement.</span><span class="sxs-lookup"><span data-stu-id="b3a45-112">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="b3a45-113">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="b3a45-113">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="b3a45-114">Le code de clé virtuelle Win32 de la clé ayant été pressée ou publiée.</span><span class="sxs-lookup"><span data-stu-id="b3a45-114">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="b3a45-115">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="b3a45-115">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="b3a45-116">Valeur LPARAM qui s’accompagne du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b3a45-116">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="b3a45-117">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="b3a45-117">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="b3a45-118">Structure représentant les informations transmises dans le LPARAM du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b3a45-118">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="b3a45-119">Poignée</span><span class="sxs-lookup"><span data-stu-id="b3a45-119">Handle</span></span>](#handle) | <span data-ttu-id="b3a45-120">Les appels permettent au processus de navigateur de continuer.</span><span class="sxs-lookup"><span data-stu-id="b3a45-120">Calling this will allow the browser process to continue.</span></span>

## <span data-ttu-id="b3a45-121">Ses</span><span class="sxs-lookup"><span data-stu-id="b3a45-121">Members</span></span>

#### <span data-ttu-id="b3a45-122">get_KeyEventType</span><span class="sxs-lookup"><span data-stu-id="b3a45-122">get_KeyEventType</span></span> 

<span data-ttu-id="b3a45-123">Type d’événement de touche qui a entraîné le déclenchement de l’événement.</span><span class="sxs-lookup"><span data-stu-id="b3a45-123">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="b3a45-124">[get_KeyEventType](#get_keyeventtype)par le biais du public HRESULT (WEBVIEW2_KEY_EVENT_TYPE \* KeyEventType)</span><span class="sxs-lookup"><span data-stu-id="b3a45-124">public HRESULT [get_KeyEventType](#get_keyeventtype)(WEBVIEW2_KEY_EVENT_TYPE \* keyEventType)</span></span>

<span data-ttu-id="b3a45-125">Il s’agit de l’une des WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN ou WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.</span><span class="sxs-lookup"><span data-stu-id="b3a45-125">This is one of WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN, or WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.</span></span>

#### <span data-ttu-id="b3a45-126">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="b3a45-126">get_VirtualKey</span></span> 

<span data-ttu-id="b3a45-127">Le code de clé virtuelle Win32 de la clé ayant été pressée ou publiée.</span><span class="sxs-lookup"><span data-stu-id="b3a45-127">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="b3a45-128">valeur publique HRESULT [get_VirtualKey](#get_virtualkey)(uint \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="b3a45-128">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="b3a45-129">Il s’agira de l’une des constantes de clé virtuelle Win32, comme VK_RETURN ou une valeur ASCII (majuscule), telle que «A».</span><span class="sxs-lookup"><span data-stu-id="b3a45-129">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="b3a45-130">Vous pouvez vérifier que l’utilisateur appuie sur CTRL ou Alt en appelant GetKeyState (VK_CONTROL) ou GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="b3a45-130">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="b3a45-131">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="b3a45-131">get_KeyEventLParam</span></span> 

<span data-ttu-id="b3a45-132">Valeur LPARAM qui s’accompagne du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b3a45-132">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="b3a45-133">valeur publique HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int \* lParam)</span><span class="sxs-lookup"><span data-stu-id="b3a45-133">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="b3a45-134">Pour plus d’informations, consultez la documentation relative au WM_KEYDOWN et aux messages WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="b3a45-134">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="b3a45-135">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="b3a45-135">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="b3a45-136">Structure représentant les informations transmises dans le LPARAM du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b3a45-136">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="b3a45-137">[get_PhysicalKeyStatus](#get_physicalkeystatus)par le biais du public HRESULT (WEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="b3a45-137">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(WEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="b3a45-138">Poignée</span><span class="sxs-lookup"><span data-stu-id="b3a45-138">Handle</span></span> 

<span data-ttu-id="b3a45-139">Les appels permettent au processus de navigateur de continuer.</span><span class="sxs-lookup"><span data-stu-id="b3a45-139">Calling this will allow the browser process to continue.</span></span>

> <span data-ttu-id="b3a45-140">[handle](#handle)HRESULT public (bool géré)</span><span class="sxs-lookup"><span data-stu-id="b3a45-140">public HRESULT [Handle](#handle)(BOOL handled)</span></span>

<span data-ttu-id="b3a45-141">Le passage de la valeur TRUE empêchera le navigateur d’exécuter l’action par défaut pour cette touche accélérateur.</span><span class="sxs-lookup"><span data-stu-id="b3a45-141">Passing TRUE will prevent the browser from performing the default action for this accelerator key.</span></span> <span data-ttu-id="b3a45-142">Si le gestionnaire d’événements renvoie sans appeler [handle ()](#handle), il est équivalent au handle d’appel (false).</span><span class="sxs-lookup"><span data-stu-id="b3a45-142">If the event handler returns without calling [Handle()](#handle), it is equivalent to calling Handle(FALSE).</span></span> <span data-ttu-id="b3a45-143">Le [handle d’appel ()](#handle) après son appel ou le gestionnaire d’événements renvoyé ne fera rien.</span><span class="sxs-lookup"><span data-stu-id="b3a45-143">Calling [Handle()](#handle) after it has already been called or the event handler has returned will do nothing.</span></span>

