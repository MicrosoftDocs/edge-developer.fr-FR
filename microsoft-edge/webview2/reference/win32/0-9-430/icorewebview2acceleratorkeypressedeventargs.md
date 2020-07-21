---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 280df2816696ce4abce118976b3eb9abf76267e3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884413"
---
# <span data-ttu-id="48ed9-104">0.9.430-interface ICoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="48ed9-104">0.9.430 - interface ICoreWebView2AcceleratorKeyPressedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="48ed9-105">Arguments d’événement pour l’événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="48ed9-105">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="48ed9-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="48ed9-106">Summary</span></span>

 <span data-ttu-id="48ed9-107">Ses</span><span class="sxs-lookup"><span data-stu-id="48ed9-107">Members</span></span>                        | <span data-ttu-id="48ed9-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="48ed9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="48ed9-109">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="48ed9-109">get_KeyEventKind</span></span>](#get_keyeventkind) | <span data-ttu-id="48ed9-110">Type d’événement de touche qui a entraîné le déclenchement de l’événement.</span><span class="sxs-lookup"><span data-stu-id="48ed9-110">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="48ed9-111">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="48ed9-111">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="48ed9-112">Le code de clé virtuelle Win32 de la clé ayant été pressée ou publiée.</span><span class="sxs-lookup"><span data-stu-id="48ed9-112">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="48ed9-113">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="48ed9-113">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="48ed9-114">Valeur LPARAM qui s’accompagne du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="48ed9-114">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="48ed9-115">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="48ed9-115">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="48ed9-116">Structure représentant les informations transmises dans le LPARAM du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="48ed9-116">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="48ed9-117">get_Handled</span><span class="sxs-lookup"><span data-stu-id="48ed9-117">get_Handled</span></span>](#get_handled) | <span data-ttu-id="48ed9-118">Lors de l’appel du gestionnaire AcceleratorKeyPressedEvent, le WebView est bloqué en attente de la décision du moment où l’accélérateur est géré par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="48ed9-118">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="48ed9-119">put_Handled</span><span class="sxs-lookup"><span data-stu-id="48ed9-119">put_Handled</span></span>](#put_handled) | <span data-ttu-id="48ed9-120">Définit la propriété Handled.</span><span class="sxs-lookup"><span data-stu-id="48ed9-120">Sets the Handled property.</span></span>

## <span data-ttu-id="48ed9-121">Ses</span><span class="sxs-lookup"><span data-stu-id="48ed9-121">Members</span></span>

#### <span data-ttu-id="48ed9-122">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="48ed9-122">get_KeyEventKind</span></span> 

<span data-ttu-id="48ed9-123">Type d’événement de touche qui a entraîné le déclenchement de l’événement.</span><span class="sxs-lookup"><span data-stu-id="48ed9-123">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="48ed9-124">[get_KeyEventKind](#get_keyeventkind)par le biais du public HRESULT (CORE_WEBVIEW2_KEY_EVENT_KIND \* KeyEventKind)</span><span class="sxs-lookup"><span data-stu-id="48ed9-124">public HRESULT [get_KeyEventKind](#get_keyeventkind)(CORE_WEBVIEW2_KEY_EVENT_KIND \* keyEventKind)</span></span>

#### <span data-ttu-id="48ed9-125">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="48ed9-125">get_VirtualKey</span></span> 

<span data-ttu-id="48ed9-126">Le code de clé virtuelle Win32 de la clé ayant été pressée ou publiée.</span><span class="sxs-lookup"><span data-stu-id="48ed9-126">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="48ed9-127">valeur publique HRESULT [get_VirtualKey](#get_virtualkey)(uint \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="48ed9-127">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="48ed9-128">Il s’agira de l’une des constantes de clé virtuelle Win32, comme VK_RETURN ou une valeur ASCII (majuscule), telle que «A».</span><span class="sxs-lookup"><span data-stu-id="48ed9-128">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="48ed9-129">Vous pouvez vérifier que l’utilisateur appuie sur CTRL ou Alt en appelant GetKeyState (VK_CONTROL) ou GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="48ed9-129">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="48ed9-130">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="48ed9-130">get_KeyEventLParam</span></span> 

<span data-ttu-id="48ed9-131">Valeur LPARAM qui s’accompagne du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="48ed9-131">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="48ed9-132">valeur publique HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int \* lParam)</span><span class="sxs-lookup"><span data-stu-id="48ed9-132">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="48ed9-133">Pour plus d’informations, consultez la documentation relative au WM_KEYDOWN et aux messages WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="48ed9-133">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="48ed9-134">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="48ed9-134">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="48ed9-135">Structure représentant les informations transmises dans le LPARAM du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="48ed9-135">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="48ed9-136">[get_PhysicalKeyStatus](#get_physicalkeystatus)par le biais du public HRESULT (CORE_WEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="48ed9-136">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(CORE_WEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="48ed9-137">get_Handled</span><span class="sxs-lookup"><span data-stu-id="48ed9-137">get_Handled</span></span> 

<span data-ttu-id="48ed9-138">Lors de l’appel du gestionnaire AcceleratorKeyPressedEvent, le WebView est bloqué en attente de la décision du moment où l’accélérateur est géré par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="48ed9-138">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="48ed9-139">[get_Handled](#get_handled)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="48ed9-139">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

<span data-ttu-id="48ed9-140">Si la propriété Handled est définie sur TRUE, cela empêchera le WebView d’exécuter l’action par défaut pour cette touche accélérateur.</span><span class="sxs-lookup"><span data-stu-id="48ed9-140">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="48ed9-141">Dans le cas contraire, le WebView exécute l’action par défaut pour la touche accélérateur.</span><span class="sxs-lookup"><span data-stu-id="48ed9-141">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="48ed9-142">put_Handled</span><span class="sxs-lookup"><span data-stu-id="48ed9-142">put_Handled</span></span> 

<span data-ttu-id="48ed9-143">Définit la propriété Handled.</span><span class="sxs-lookup"><span data-stu-id="48ed9-143">Sets the Handled property.</span></span>

> <span data-ttu-id="48ed9-144">[put_Handleds](#put_handled)HRESULT publiques (bool géré)</span><span class="sxs-lookup"><span data-stu-id="48ed9-144">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

