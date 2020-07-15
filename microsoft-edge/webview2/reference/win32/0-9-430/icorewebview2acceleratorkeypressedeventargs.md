---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: e7a512201c1ef7917a54b93dbd06587294e76f78
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881178"
---
# <span data-ttu-id="d95b8-104">0.9.430-interface ICoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d95b8-104">0.9.430 - interface ICoreWebView2AcceleratorKeyPressedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="d95b8-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="d95b8-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="d95b8-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="d95b8-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="d95b8-107">Arguments d’événement pour l’événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="d95b8-107">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="d95b8-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="d95b8-108">Summary</span></span>

 <span data-ttu-id="d95b8-109">Ses</span><span class="sxs-lookup"><span data-stu-id="d95b8-109">Members</span></span>                        | <span data-ttu-id="d95b8-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="d95b8-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d95b8-111">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="d95b8-111">get_KeyEventKind</span></span>](#get_keyeventkind) | <span data-ttu-id="d95b8-112">Type d’événement de touche qui a entraîné le déclenchement de l’événement.</span><span class="sxs-lookup"><span data-stu-id="d95b8-112">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="d95b8-113">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="d95b8-113">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="d95b8-114">Le code de clé virtuelle Win32 de la clé ayant été pressée ou publiée.</span><span class="sxs-lookup"><span data-stu-id="d95b8-114">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="d95b8-115">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="d95b8-115">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="d95b8-116">Valeur LPARAM qui s’accompagne du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d95b8-116">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="d95b8-117">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="d95b8-117">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="d95b8-118">Structure représentant les informations transmises dans le LPARAM du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d95b8-118">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="d95b8-119">get_Handled</span><span class="sxs-lookup"><span data-stu-id="d95b8-119">get_Handled</span></span>](#get_handled) | <span data-ttu-id="d95b8-120">Lors de l’appel du gestionnaire AcceleratorKeyPressedEvent, le WebView est bloqué en attente de la décision du moment où l’accélérateur est géré par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="d95b8-120">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="d95b8-121">put_Handled</span><span class="sxs-lookup"><span data-stu-id="d95b8-121">put_Handled</span></span>](#put_handled) | <span data-ttu-id="d95b8-122">Définit la propriété Handled.</span><span class="sxs-lookup"><span data-stu-id="d95b8-122">Sets the Handled property.</span></span>

## <span data-ttu-id="d95b8-123">Ses</span><span class="sxs-lookup"><span data-stu-id="d95b8-123">Members</span></span>

#### <span data-ttu-id="d95b8-124">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="d95b8-124">get_KeyEventKind</span></span> 

<span data-ttu-id="d95b8-125">Type d’événement de touche qui a entraîné le déclenchement de l’événement.</span><span class="sxs-lookup"><span data-stu-id="d95b8-125">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="d95b8-126">[get_KeyEventKind](#get_keyeventkind)par le biais du public HRESULT (CORE_WEBVIEW2_KEY_EVENT_KIND \* KeyEventKind)</span><span class="sxs-lookup"><span data-stu-id="d95b8-126">public HRESULT [get_KeyEventKind](#get_keyeventkind)(CORE_WEBVIEW2_KEY_EVENT_KIND \* keyEventKind)</span></span>

#### <span data-ttu-id="d95b8-127">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="d95b8-127">get_VirtualKey</span></span> 

<span data-ttu-id="d95b8-128">Le code de clé virtuelle Win32 de la clé ayant été pressée ou publiée.</span><span class="sxs-lookup"><span data-stu-id="d95b8-128">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="d95b8-129">valeur publique HRESULT [get_VirtualKey](#get_virtualkey)(uint \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="d95b8-129">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="d95b8-130">Il s’agira de l’une des constantes de clé virtuelle Win32, comme VK_RETURN ou une valeur ASCII (majuscule), telle que «A».</span><span class="sxs-lookup"><span data-stu-id="d95b8-130">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="d95b8-131">Vous pouvez vérifier que l’utilisateur appuie sur CTRL ou Alt en appelant GetKeyState (VK_CONTROL) ou GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="d95b8-131">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="d95b8-132">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="d95b8-132">get_KeyEventLParam</span></span> 

<span data-ttu-id="d95b8-133">Valeur LPARAM qui s’accompagne du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d95b8-133">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="d95b8-134">valeur publique HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int \* lParam)</span><span class="sxs-lookup"><span data-stu-id="d95b8-134">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="d95b8-135">Pour plus d’informations, consultez la documentation relative au WM_KEYDOWN et aux messages WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="d95b8-135">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="d95b8-136">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="d95b8-136">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="d95b8-137">Structure représentant les informations transmises dans le LPARAM du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d95b8-137">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="d95b8-138">[get_PhysicalKeyStatus](#get_physicalkeystatus)par le biais du public HRESULT (CORE_WEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="d95b8-138">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(CORE_WEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="d95b8-139">get_Handled</span><span class="sxs-lookup"><span data-stu-id="d95b8-139">get_Handled</span></span> 

<span data-ttu-id="d95b8-140">Lors de l’appel du gestionnaire AcceleratorKeyPressedEvent, le WebView est bloqué en attente de la décision du moment où l’accélérateur est géré par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="d95b8-140">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="d95b8-141">[get_Handled](#get_handled)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="d95b8-141">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

<span data-ttu-id="d95b8-142">Si la propriété Handled est définie sur TRUE, cela empêchera le WebView d’exécuter l’action par défaut pour cette touche accélérateur.</span><span class="sxs-lookup"><span data-stu-id="d95b8-142">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="d95b8-143">Dans le cas contraire, le WebView exécute l’action par défaut pour la touche accélérateur.</span><span class="sxs-lookup"><span data-stu-id="d95b8-143">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="d95b8-144">put_Handled</span><span class="sxs-lookup"><span data-stu-id="d95b8-144">put_Handled</span></span> 

<span data-ttu-id="d95b8-145">Définit la propriété Handled.</span><span class="sxs-lookup"><span data-stu-id="d95b8-145">Sets the Handled property.</span></span>

> <span data-ttu-id="d95b8-146">[put_Handleds](#put_handled)HRESULT publiques (bool géré)</span><span class="sxs-lookup"><span data-stu-id="d95b8-146">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

