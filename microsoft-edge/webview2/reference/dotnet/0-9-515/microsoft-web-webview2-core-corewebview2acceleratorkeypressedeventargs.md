---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 10694292c7943f87753ae87f6129655b27f425f3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885141"
---
# <span data-ttu-id="3c1bd-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="3c1bd-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="3c1bd-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="3c1bd-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="3c1bd-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="3c1bd-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="3c1bd-107">Arguments d’événement pour l’événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="3c1bd-107">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="3c1bd-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="3c1bd-108">Summary</span></span>

 <span data-ttu-id="3c1bd-109">Ses</span><span class="sxs-lookup"><span data-stu-id="3c1bd-109">Members</span></span>                        | <span data-ttu-id="3c1bd-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="3c1bd-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3c1bd-111">Handled</span><span class="sxs-lookup"><span data-stu-id="3c1bd-111">Handled</span></span>](#handled) | <span data-ttu-id="3c1bd-112">Lors de l’appel du gestionnaire AcceleratorKeyPressedEvent, le WebView est bloqué en attente de la décision du moment où l’accélérateur est géré par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="3c1bd-112">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="3c1bd-113">KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="3c1bd-113">KeyEventKind</span></span>](#keyeventkind) | <span data-ttu-id="3c1bd-114">Type d’événement de touche qui a entraîné le déclenchement de l’événement.</span><span class="sxs-lookup"><span data-stu-id="3c1bd-114">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="3c1bd-115">KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="3c1bd-115">KeyEventLParam</span></span>](#keyeventlparam) | <span data-ttu-id="3c1bd-116">Valeur LPARAM qui s’accompagne du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3c1bd-116">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="3c1bd-117">PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="3c1bd-117">PhysicalKeyStatus</span></span>](#physicalkeystatus) | <span data-ttu-id="3c1bd-118">Structure représentant les informations transmises dans le LPARAM du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3c1bd-118">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="3c1bd-119">VirtualKey</span><span class="sxs-lookup"><span data-stu-id="3c1bd-119">VirtualKey</span></span>](#virtualkey) | <span data-ttu-id="3c1bd-120">Le code de clé virtuelle Win32 de la clé ayant été pressée ou publiée.</span><span class="sxs-lookup"><span data-stu-id="3c1bd-120">The Win32 virtual key code of the key that was pressed or released.</span></span>

## <span data-ttu-id="3c1bd-121">Ses</span><span class="sxs-lookup"><span data-stu-id="3c1bd-121">Members</span></span>

#### <span data-ttu-id="3c1bd-122">Handled</span><span class="sxs-lookup"><span data-stu-id="3c1bd-122">Handled</span></span> 

<span data-ttu-id="3c1bd-123">Lors de l’appel du gestionnaire AcceleratorKeyPressedEvent, le WebView est bloqué en attente de la décision du moment où l’accélérateur est géré par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="3c1bd-123">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="3c1bd-124">propriété booléenne [gérée](#handled)</span><span class="sxs-lookup"><span data-stu-id="3c1bd-124">public bool [Handled](#handled)</span></span>

<span data-ttu-id="3c1bd-125">Si la propriété Handled est définie sur TRUE, cela empêchera le WebView d’exécuter l’action par défaut pour cette touche accélérateur.</span><span class="sxs-lookup"><span data-stu-id="3c1bd-125">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="3c1bd-126">Dans le cas contraire, le WebView exécute l’action par défaut pour la touche accélérateur.</span><span class="sxs-lookup"><span data-stu-id="3c1bd-126">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="3c1bd-127">KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="3c1bd-127">KeyEventKind</span></span> 

<span data-ttu-id="3c1bd-128">Type d’événement de touche qui a entraîné le déclenchement de l’événement.</span><span class="sxs-lookup"><span data-stu-id="3c1bd-128">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="3c1bd-129">public [CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) [KeyEventKind](#keyeventkind)</span><span class="sxs-lookup"><span data-stu-id="3c1bd-129">public [CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) [KeyEventKind](#keyeventkind)</span></span>

#### <span data-ttu-id="3c1bd-130">KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="3c1bd-130">KeyEventLParam</span></span> 

<span data-ttu-id="3c1bd-131">Valeur LPARAM qui s’accompagne du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3c1bd-131">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="3c1bd-132">public ent [KeyEventLParam](#keyeventlparam)</span><span class="sxs-lookup"><span data-stu-id="3c1bd-132">public int [KeyEventLParam](#keyeventlparam)</span></span>

<span data-ttu-id="3c1bd-133">Pour plus d’informations, consultez la documentation relative au WM_KEYDOWN et aux messages WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="3c1bd-133">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="3c1bd-134">PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="3c1bd-134">PhysicalKeyStatus</span></span> 

<span data-ttu-id="3c1bd-135">Structure représentant les informations transmises dans le LPARAM du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3c1bd-135">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="3c1bd-136">public [CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) [PhysicalKeyStatus](#physicalkeystatus)</span><span class="sxs-lookup"><span data-stu-id="3c1bd-136">public [CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) [PhysicalKeyStatus](#physicalkeystatus)</span></span>

#### <span data-ttu-id="3c1bd-137">VirtualKey</span><span class="sxs-lookup"><span data-stu-id="3c1bd-137">VirtualKey</span></span> 

<span data-ttu-id="3c1bd-138">Le code de clé virtuelle Win32 de la clé ayant été pressée ou publiée.</span><span class="sxs-lookup"><span data-stu-id="3c1bd-138">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="3c1bd-139">public uint [VirtualKey](#virtualkey)</span><span class="sxs-lookup"><span data-stu-id="3c1bd-139">public uint [VirtualKey](#virtualkey)</span></span>

<span data-ttu-id="3c1bd-140">Il s’agira de l’une des constantes de clé virtuelle Win32, comme VK_RETURN ou une valeur ASCII (majuscule), telle que «A».</span><span class="sxs-lookup"><span data-stu-id="3c1bd-140">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="3c1bd-141">Vous pouvez vérifier que l’utilisateur appuie sur CTRL ou Alt en appelant GetKeyState (VK_CONTROL) ou GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="3c1bd-141">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

