---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: b3d6cc14ccaa6a803e0e987b68a74851a6c5f2f9
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698730"
---
# <span data-ttu-id="08b8f-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="08b8f-104">Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs class</span></span> 

<span data-ttu-id="08b8f-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="08b8f-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="08b8f-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="08b8f-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="08b8f-107">Arguments d’événement pour l’événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="08b8f-107">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="08b8f-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="08b8f-108">Summary</span></span>

 <span data-ttu-id="08b8f-109">Ses</span><span class="sxs-lookup"><span data-stu-id="08b8f-109">Members</span></span>                        | <span data-ttu-id="08b8f-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="08b8f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="08b8f-111">Handled</span><span class="sxs-lookup"><span data-stu-id="08b8f-111">Handled</span></span>](#handled) | <span data-ttu-id="08b8f-112">Lors de l’appel du gestionnaire AcceleratorKeyPressedEvent, le WebView est bloqué en attente de la décision du moment où l’accélérateur est géré par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="08b8f-112">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="08b8f-113">KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="08b8f-113">KeyEventKind</span></span>](#keyeventkind) | <span data-ttu-id="08b8f-114">Type d’événement de touche qui a entraîné le déclenchement de l’événement.</span><span class="sxs-lookup"><span data-stu-id="08b8f-114">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="08b8f-115">KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="08b8f-115">KeyEventLParam</span></span>](#keyeventlparam) | <span data-ttu-id="08b8f-116">Valeur LPARAM qui s’accompagne du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="08b8f-116">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="08b8f-117">PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="08b8f-117">PhysicalKeyStatus</span></span>](#physicalkeystatus) | <span data-ttu-id="08b8f-118">Structure représentant les informations transmises dans le LPARAM du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="08b8f-118">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="08b8f-119">VirtualKey</span><span class="sxs-lookup"><span data-stu-id="08b8f-119">VirtualKey</span></span>](#virtualkey) | <span data-ttu-id="08b8f-120">Le code de clé virtuelle Win32 de la clé ayant été pressée ou publiée.</span><span class="sxs-lookup"><span data-stu-id="08b8f-120">The Win32 virtual key code of the key that was pressed or released.</span></span>

## <span data-ttu-id="08b8f-121">Ses</span><span class="sxs-lookup"><span data-stu-id="08b8f-121">Members</span></span>

#### <span data-ttu-id="08b8f-122">Handled</span><span class="sxs-lookup"><span data-stu-id="08b8f-122">Handled</span></span> 

<span data-ttu-id="08b8f-123">Lors de l’appel du gestionnaire AcceleratorKeyPressedEvent, le WebView est bloqué en attente de la décision du moment où l’accélérateur est géré par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="08b8f-123">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="08b8f-124">propriété booléenne [gérée](#handled)</span><span class="sxs-lookup"><span data-stu-id="08b8f-124">public bool [Handled](#handled)</span></span>

<span data-ttu-id="08b8f-125">Si la propriété Handled est définie sur TRUE, cela empêchera le WebView d’exécuter l’action par défaut pour cette touche accélérateur.</span><span class="sxs-lookup"><span data-stu-id="08b8f-125">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="08b8f-126">Dans le cas contraire, le WebView exécute l’action par défaut pour la touche accélérateur.</span><span class="sxs-lookup"><span data-stu-id="08b8f-126">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="08b8f-127">KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="08b8f-127">KeyEventKind</span></span> 

<span data-ttu-id="08b8f-128">Type d’événement de touche qui a entraîné le déclenchement de l’événement.</span><span class="sxs-lookup"><span data-stu-id="08b8f-128">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="08b8f-129">public [CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) [KeyEventKind](#keyeventkind)</span><span class="sxs-lookup"><span data-stu-id="08b8f-129">public [CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) [KeyEventKind](#keyeventkind)</span></span>

#### <span data-ttu-id="08b8f-130">KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="08b8f-130">KeyEventLParam</span></span> 

<span data-ttu-id="08b8f-131">Valeur LPARAM qui s’accompagne du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="08b8f-131">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="08b8f-132">public ent [KeyEventLParam](#keyeventlparam)</span><span class="sxs-lookup"><span data-stu-id="08b8f-132">public int [KeyEventLParam](#keyeventlparam)</span></span>

<span data-ttu-id="08b8f-133">Pour plus d’informations, consultez la documentation relative au WM_KEYDOWN et aux messages WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="08b8f-133">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="08b8f-134">PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="08b8f-134">PhysicalKeyStatus</span></span> 

<span data-ttu-id="08b8f-135">Structure représentant les informations transmises dans le LPARAM du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="08b8f-135">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="08b8f-136">public [CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) [PhysicalKeyStatus](#physicalkeystatus)</span><span class="sxs-lookup"><span data-stu-id="08b8f-136">public [CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) [PhysicalKeyStatus](#physicalkeystatus)</span></span>

#### <span data-ttu-id="08b8f-137">VirtualKey</span><span class="sxs-lookup"><span data-stu-id="08b8f-137">VirtualKey</span></span> 

<span data-ttu-id="08b8f-138">Le code de clé virtuelle Win32 de la clé ayant été pressée ou publiée.</span><span class="sxs-lookup"><span data-stu-id="08b8f-138">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="08b8f-139">public uint [VirtualKey](#virtualkey)</span><span class="sxs-lookup"><span data-stu-id="08b8f-139">public uint [VirtualKey](#virtualkey)</span></span>

<span data-ttu-id="08b8f-140">Il s’agira de l’une des constantes de clé virtuelle Win32, comme VK_RETURN ou une valeur ASCII (majuscule), telle que «A».</span><span class="sxs-lookup"><span data-stu-id="08b8f-140">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="08b8f-141">Vous pouvez vérifier que l’utilisateur appuie sur CTRL ou Alt en appelant GetKeyState (VK_CONTROL) ou GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="08b8f-141">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

