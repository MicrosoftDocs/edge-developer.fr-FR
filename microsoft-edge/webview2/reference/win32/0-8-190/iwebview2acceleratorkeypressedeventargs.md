---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 885ad6b161fbde6721e1812735ab50d7e0c3e8d9
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885051"
---
# <span data-ttu-id="10b83-104">0.8.355-interface IWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="10b83-104">0.8.355 - interface IWebView2AcceleratorKeyPressedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="10b83-105">Arguments d’événement pour l’événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="10b83-105">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="10b83-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="10b83-106">Summary</span></span>

 <span data-ttu-id="10b83-107">Ses</span><span class="sxs-lookup"><span data-stu-id="10b83-107">Members</span></span>                        | <span data-ttu-id="10b83-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="10b83-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="10b83-109">get_KeyEventType</span><span class="sxs-lookup"><span data-stu-id="10b83-109">get_KeyEventType</span></span>](#get_keyeventtype) | <span data-ttu-id="10b83-110">Type d’événement de touche qui a entraîné le déclenchement de l’événement.</span><span class="sxs-lookup"><span data-stu-id="10b83-110">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="10b83-111">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="10b83-111">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="10b83-112">Le code de clé virtuelle Win32 de la clé ayant été pressée ou publiée.</span><span class="sxs-lookup"><span data-stu-id="10b83-112">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="10b83-113">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="10b83-113">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="10b83-114">Valeur LPARAM qui s’accompagne du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="10b83-114">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="10b83-115">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="10b83-115">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="10b83-116">Structure représentant les informations transmises dans le LPARAM du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="10b83-116">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="10b83-117">Poignée</span><span class="sxs-lookup"><span data-stu-id="10b83-117">Handle</span></span>](#handle) | <span data-ttu-id="10b83-118">Les appels permettent au processus de navigateur de continuer.</span><span class="sxs-lookup"><span data-stu-id="10b83-118">Calling this will allow the browser process to continue.</span></span>

## <span data-ttu-id="10b83-119">Ses</span><span class="sxs-lookup"><span data-stu-id="10b83-119">Members</span></span>

#### <span data-ttu-id="10b83-120">get_KeyEventType</span><span class="sxs-lookup"><span data-stu-id="10b83-120">get_KeyEventType</span></span> 

<span data-ttu-id="10b83-121">Type d’événement de touche qui a entraîné le déclenchement de l’événement.</span><span class="sxs-lookup"><span data-stu-id="10b83-121">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="10b83-122">[get_KeyEventType](#get_keyeventtype)par le biais du public HRESULT (WEBVIEW2_KEY_EVENT_TYPE \* KeyEventType)</span><span class="sxs-lookup"><span data-stu-id="10b83-122">public HRESULT [get_KeyEventType](#get_keyeventtype)(WEBVIEW2_KEY_EVENT_TYPE \* keyEventType)</span></span>

<span data-ttu-id="10b83-123">Il s’agit de l’une des WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN ou WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.</span><span class="sxs-lookup"><span data-stu-id="10b83-123">This is one of WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN, or WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.</span></span>

#### <span data-ttu-id="10b83-124">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="10b83-124">get_VirtualKey</span></span> 

<span data-ttu-id="10b83-125">Le code de clé virtuelle Win32 de la clé ayant été pressée ou publiée.</span><span class="sxs-lookup"><span data-stu-id="10b83-125">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="10b83-126">valeur publique HRESULT [get_VirtualKey](#get_virtualkey)(uint \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="10b83-126">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="10b83-127">Il s’agira de l’une des constantes de clé virtuelle Win32, comme VK_RETURN ou une valeur ASCII (majuscule), telle que «A».</span><span class="sxs-lookup"><span data-stu-id="10b83-127">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="10b83-128">Vous pouvez vérifier que l’utilisateur appuie sur CTRL ou Alt en appelant GetKeyState (VK_CONTROL) ou GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="10b83-128">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="10b83-129">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="10b83-129">get_KeyEventLParam</span></span> 

<span data-ttu-id="10b83-130">Valeur LPARAM qui s’accompagne du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="10b83-130">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="10b83-131">valeur publique HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int \* lParam)</span><span class="sxs-lookup"><span data-stu-id="10b83-131">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="10b83-132">Pour plus d’informations, consultez la documentation relative au WM_KEYDOWN et aux messages WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="10b83-132">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="10b83-133">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="10b83-133">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="10b83-134">Structure représentant les informations transmises dans le LPARAM du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="10b83-134">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="10b83-135">[get_PhysicalKeyStatus](#get_physicalkeystatus)par le biais du public HRESULT (WEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="10b83-135">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(WEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="10b83-136">Poignée</span><span class="sxs-lookup"><span data-stu-id="10b83-136">Handle</span></span> 

<span data-ttu-id="10b83-137">Les appels permettent au processus de navigateur de continuer.</span><span class="sxs-lookup"><span data-stu-id="10b83-137">Calling this will allow the browser process to continue.</span></span>

> <span data-ttu-id="10b83-138">[handle](#handle)HRESULT public (bool géré)</span><span class="sxs-lookup"><span data-stu-id="10b83-138">public HRESULT [Handle](#handle)(BOOL handled)</span></span>

<span data-ttu-id="10b83-139">Le passage de la valeur TRUE empêchera le navigateur d’exécuter l’action par défaut pour cette touche accélérateur.</span><span class="sxs-lookup"><span data-stu-id="10b83-139">Passing TRUE will prevent the browser from performing the default action for this accelerator key.</span></span> <span data-ttu-id="10b83-140">Si le gestionnaire d’événements renvoie sans appeler [handle ()](#handle), il est équivalent au handle d’appel (false).</span><span class="sxs-lookup"><span data-stu-id="10b83-140">If the event handler returns without calling [Handle()](#handle), it is equivalent to calling Handle(FALSE).</span></span> <span data-ttu-id="10b83-141">Le [handle d’appel ()](#handle) après son appel ou le gestionnaire d’événements renvoyé ne fera rien.</span><span class="sxs-lookup"><span data-stu-id="10b83-141">Calling [Handle()](#handle) after it has already been called or the event handler has returned will do nothing.</span></span>

