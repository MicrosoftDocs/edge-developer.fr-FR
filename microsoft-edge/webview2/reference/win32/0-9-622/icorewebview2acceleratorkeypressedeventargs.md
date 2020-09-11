---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2AcceleratorKeyPressedEventArgs
ms.openlocfilehash: 7491756d5cc549f805f4f8003ac450cdc6c40b96
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011814"
---
# <span data-ttu-id="6a9c9-104">interface ICoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="6a9c9-104">interface ICoreWebView2AcceleratorKeyPressedEventArgs</span></span> 

```
interface ICoreWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="6a9c9-105">Arguments d’événement pour l’événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="6a9c9-105">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="6a9c9-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="6a9c9-106">Summary</span></span>

 <span data-ttu-id="6a9c9-107">Ses</span><span class="sxs-lookup"><span data-stu-id="6a9c9-107">Members</span></span>                        | <span data-ttu-id="6a9c9-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="6a9c9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6a9c9-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="6a9c9-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="6a9c9-110">Lors de l’appel du gestionnaire AcceleratorKeyPressedEvent, le WebView est bloqué en attente de la décision du moment où l’accélérateur est géré par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="6a9c9-110">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="6a9c9-111">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="6a9c9-111">get_KeyEventKind</span></span>](#get_keyeventkind) | <span data-ttu-id="6a9c9-112">Type d’événement de touche qui a entraîné le déclenchement de l’événement.</span><span class="sxs-lookup"><span data-stu-id="6a9c9-112">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="6a9c9-113">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="6a9c9-113">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="6a9c9-114">Valeur LPARAM qui s’accompagne du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6a9c9-114">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="6a9c9-115">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="6a9c9-115">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="6a9c9-116">Structure représentant les informations transmises dans le LPARAM du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6a9c9-116">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="6a9c9-117">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="6a9c9-117">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="6a9c9-118">Le code de clé virtuelle Win32 de la clé ayant été pressée ou publiée.</span><span class="sxs-lookup"><span data-stu-id="6a9c9-118">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="6a9c9-119">put_Handled</span><span class="sxs-lookup"><span data-stu-id="6a9c9-119">put_Handled</span></span>](#put_handled) | <span data-ttu-id="6a9c9-120">Définit la propriété Handled.</span><span class="sxs-lookup"><span data-stu-id="6a9c9-120">Sets the Handled property.</span></span>

## <span data-ttu-id="6a9c9-121">Ses</span><span class="sxs-lookup"><span data-stu-id="6a9c9-121">Members</span></span>

#### <span data-ttu-id="6a9c9-122">get_Handled</span><span class="sxs-lookup"><span data-stu-id="6a9c9-122">get_Handled</span></span> 

<span data-ttu-id="6a9c9-123">Lors de l’appel du gestionnaire AcceleratorKeyPressedEvent, le WebView est bloqué en attente de la décision du moment où l’accélérateur est géré par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="6a9c9-123">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="6a9c9-124">[get_Handled](#get_handled)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="6a9c9-124">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

<span data-ttu-id="6a9c9-125">Si la propriété Handled est définie sur TRUE, cela empêchera le WebView d’exécuter l’action par défaut pour cette touche accélérateur.</span><span class="sxs-lookup"><span data-stu-id="6a9c9-125">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="6a9c9-126">Dans le cas contraire, le WebView exécute l’action par défaut pour la touche accélérateur.</span><span class="sxs-lookup"><span data-stu-id="6a9c9-126">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="6a9c9-127">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="6a9c9-127">get_KeyEventKind</span></span> 

<span data-ttu-id="6a9c9-128">Type d’événement de touche qui a entraîné le déclenchement de l’événement.</span><span class="sxs-lookup"><span data-stu-id="6a9c9-128">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="6a9c9-129">[get_KeyEventKind](#get_keyeventkind)par le biais du public HRESULT (COREWEBVIEW2_KEY_EVENT_KIND \* KeyEventKind)</span><span class="sxs-lookup"><span data-stu-id="6a9c9-129">public HRESULT [get_KeyEventKind](#get_keyeventkind)(COREWEBVIEW2_KEY_EVENT_KIND \* keyEventKind)</span></span>

#### <span data-ttu-id="6a9c9-130">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="6a9c9-130">get_KeyEventLParam</span></span> 

<span data-ttu-id="6a9c9-131">Valeur LPARAM qui s’accompagne du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6a9c9-131">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="6a9c9-132">valeur publique HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int \* lParam)</span><span class="sxs-lookup"><span data-stu-id="6a9c9-132">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="6a9c9-133">Pour plus d’informations, consultez la documentation relative au WM_KEYDOWN et aux messages WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="6a9c9-133">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="6a9c9-134">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="6a9c9-134">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="6a9c9-135">Structure représentant les informations transmises dans le LPARAM du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6a9c9-135">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="6a9c9-136">[get_PhysicalKeyStatus](#get_physicalkeystatus)par le biais du public HRESULT (COREWEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="6a9c9-136">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(COREWEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="6a9c9-137">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="6a9c9-137">get_VirtualKey</span></span> 

<span data-ttu-id="6a9c9-138">Le code de clé virtuelle Win32 de la clé ayant été pressée ou publiée.</span><span class="sxs-lookup"><span data-stu-id="6a9c9-138">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="6a9c9-139">valeur publique HRESULT [get_VirtualKey](#get_virtualkey)(uint \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="6a9c9-139">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="6a9c9-140">Il s’agira de l’une des constantes de clé virtuelle Win32, comme VK_RETURN ou une valeur ASCII (majuscule), telle que «A».</span><span class="sxs-lookup"><span data-stu-id="6a9c9-140">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="6a9c9-141">Vous pouvez vérifier que l’utilisateur appuie sur CTRL ou Alt en appelant GetKeyState (VK_CONTROL) ou GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="6a9c9-141">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="6a9c9-142">put_Handled</span><span class="sxs-lookup"><span data-stu-id="6a9c9-142">put_Handled</span></span> 

<span data-ttu-id="6a9c9-143">Définit la propriété Handled.</span><span class="sxs-lookup"><span data-stu-id="6a9c9-143">Sets the Handled property.</span></span>

> <span data-ttu-id="6a9c9-144">[put_Handleds](#put_handled)HRESULT publiques (bool géré)</span><span class="sxs-lookup"><span data-stu-id="6a9c9-144">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

