---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: b0df25ffe3b00267dfff15cd50d1d3db6a7e38bb
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698217"
---
# <span data-ttu-id="cd0b6-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="cd0b6-104">Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="cd0b6-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="cd0b6-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="cd0b6-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="cd0b6-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="cd0b6-107">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="cd0b6-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="cd0b6-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="cd0b6-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="cd0b6-109">Arguments d’événement pour l’événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="cd0b6-109">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="cd0b6-110">Résumé</span><span class="sxs-lookup"><span data-stu-id="cd0b6-110">Summary</span></span>

 <span data-ttu-id="cd0b6-111">Ses</span><span class="sxs-lookup"><span data-stu-id="cd0b6-111">Members</span></span>                        | <span data-ttu-id="cd0b6-112">Descriptions</span><span class="sxs-lookup"><span data-stu-id="cd0b6-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cd0b6-113">Handled</span><span class="sxs-lookup"><span data-stu-id="cd0b6-113">Handled</span></span>](#handled) | <span data-ttu-id="cd0b6-114">Lors de l’appel du gestionnaire AcceleratorKeyPressedEvent, le WebView est bloqué en attente de la décision du moment où l’accélérateur est géré par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="cd0b6-114">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="cd0b6-115">KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="cd0b6-115">KeyEventKind</span></span>](#keyeventkind) | <span data-ttu-id="cd0b6-116">Type d’événement de touche qui a entraîné le déclenchement de l’événement.</span><span class="sxs-lookup"><span data-stu-id="cd0b6-116">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="cd0b6-117">KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="cd0b6-117">KeyEventLParam</span></span>](#keyeventlparam) | <span data-ttu-id="cd0b6-118">Valeur LPARAM qui s’accompagne du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cd0b6-118">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="cd0b6-119">PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="cd0b6-119">PhysicalKeyStatus</span></span>](#physicalkeystatus) | <span data-ttu-id="cd0b6-120">Structure représentant les informations transmises dans le LPARAM du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cd0b6-120">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="cd0b6-121">VirtualKey</span><span class="sxs-lookup"><span data-stu-id="cd0b6-121">VirtualKey</span></span>](#virtualkey) | <span data-ttu-id="cd0b6-122">Le code de clé virtuelle Win32 de la clé ayant été pressée ou publiée.</span><span class="sxs-lookup"><span data-stu-id="cd0b6-122">The Win32 virtual key code of the key that was pressed or released.</span></span>

## <span data-ttu-id="cd0b6-123">Ses</span><span class="sxs-lookup"><span data-stu-id="cd0b6-123">Members</span></span>

#### <span data-ttu-id="cd0b6-124">Handled</span><span class="sxs-lookup"><span data-stu-id="cd0b6-124">Handled</span></span> 

<span data-ttu-id="cd0b6-125">Lors de l’appel du gestionnaire AcceleratorKeyPressedEvent, le WebView est bloqué en attente de la décision du moment où l’accélérateur est géré par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="cd0b6-125">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="cd0b6-126">propriété booléenne [gérée](#handled)</span><span class="sxs-lookup"><span data-stu-id="cd0b6-126">public bool [Handled](#handled)</span></span>

<span data-ttu-id="cd0b6-127">Si la propriété Handled est définie sur TRUE, cela empêchera le WebView d’exécuter l’action par défaut pour cette touche accélérateur.</span><span class="sxs-lookup"><span data-stu-id="cd0b6-127">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="cd0b6-128">Dans le cas contraire, le WebView exécute l’action par défaut pour la touche accélérateur.</span><span class="sxs-lookup"><span data-stu-id="cd0b6-128">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="cd0b6-129">KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="cd0b6-129">KeyEventKind</span></span> 

<span data-ttu-id="cd0b6-130">Type d’événement de touche qui a entraîné le déclenchement de l’événement.</span><span class="sxs-lookup"><span data-stu-id="cd0b6-130">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="cd0b6-131">public [CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) [KeyEventKind](#keyeventkind)</span><span class="sxs-lookup"><span data-stu-id="cd0b6-131">public [CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) [KeyEventKind](#keyeventkind)</span></span>

#### <span data-ttu-id="cd0b6-132">KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="cd0b6-132">KeyEventLParam</span></span> 

<span data-ttu-id="cd0b6-133">Valeur LPARAM qui s’accompagne du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cd0b6-133">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="cd0b6-134">public ent [KeyEventLParam](#keyeventlparam)</span><span class="sxs-lookup"><span data-stu-id="cd0b6-134">public int [KeyEventLParam](#keyeventlparam)</span></span>

<span data-ttu-id="cd0b6-135">Pour plus d’informations, consultez la documentation relative au WM_KEYDOWN et aux messages WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="cd0b6-135">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="cd0b6-136">PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="cd0b6-136">PhysicalKeyStatus</span></span> 

<span data-ttu-id="cd0b6-137">Structure représentant les informations transmises dans le LPARAM du message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cd0b6-137">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="cd0b6-138">public [CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) [PhysicalKeyStatus](#physicalkeystatus)</span><span class="sxs-lookup"><span data-stu-id="cd0b6-138">public [CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) [PhysicalKeyStatus](#physicalkeystatus)</span></span>

#### <span data-ttu-id="cd0b6-139">VirtualKey</span><span class="sxs-lookup"><span data-stu-id="cd0b6-139">VirtualKey</span></span> 

<span data-ttu-id="cd0b6-140">Le code de clé virtuelle Win32 de la clé ayant été pressée ou publiée.</span><span class="sxs-lookup"><span data-stu-id="cd0b6-140">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="cd0b6-141">public uint [VirtualKey](#virtualkey)</span><span class="sxs-lookup"><span data-stu-id="cd0b6-141">public uint [VirtualKey](#virtualkey)</span></span>

<span data-ttu-id="cd0b6-142">Il s’agira de l’une des constantes de clé virtuelle Win32, comme VK_RETURN ou une valeur ASCII (majuscule), telle que «A».</span><span class="sxs-lookup"><span data-stu-id="cd0b6-142">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="cd0b6-143">Vous pouvez vérifier que l’utilisateur appuie sur CTRL ou Alt en appelant GetKeyState (VK_CONTROL) ou GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="cd0b6-143">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

