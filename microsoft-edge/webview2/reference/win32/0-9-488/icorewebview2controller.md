---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 02128001f208f15d4e33c1f3f2cef6c8d662d357
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653537"
---
# <span data-ttu-id="18b04-104">interface ICoreWebView2Controller</span><span class="sxs-lookup"><span data-stu-id="18b04-104">interface ICoreWebView2Controller</span></span> 

```
interface ICoreWebView2Controller
  : public IUnknown
```

<span data-ttu-id="18b04-105">Cette interface est le propriétaire de l’objet CoreWebView2 et prend en charge le redimensionnement, l’affichage et le masquage, le focus, ainsi que d’autres fonctionnalités relatives à la fenêtre et à la composition.</span><span class="sxs-lookup"><span data-stu-id="18b04-105">This interface is the owner of the CoreWebView2 object, and provides support for resizing, showing and hiding, focusing, and other functionality related to windowing and composition.</span></span>

## <span data-ttu-id="18b04-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="18b04-106">Summary</span></span>

 <span data-ttu-id="18b04-107">Ses</span><span class="sxs-lookup"><span data-stu-id="18b04-107">Members</span></span>                        | <span data-ttu-id="18b04-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="18b04-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="18b04-109">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="18b04-109">add_AcceleratorKeyPressed</span></span>](#add_acceleratorkeypressed) | <span data-ttu-id="18b04-110">Ajoutez un gestionnaire d’événements pour l’événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="18b04-110">Add an event handler for the AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="18b04-111">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="18b04-111">add_GotFocus</span></span>](#add_gotfocus) | <span data-ttu-id="18b04-112">Ajoutez un gestionnaire d’événements pour l’événement GotFocus.</span><span class="sxs-lookup"><span data-stu-id="18b04-112">Add an event handler for the GotFocus event.</span></span>
[<span data-ttu-id="18b04-113">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="18b04-113">add_LostFocus</span></span>](#add_lostfocus) | <span data-ttu-id="18b04-114">Ajoutez un gestionnaire d’événements pour l’événement LostFocus.</span><span class="sxs-lookup"><span data-stu-id="18b04-114">Add an event handler for the LostFocus event.</span></span>
[<span data-ttu-id="18b04-115">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="18b04-115">add_MoveFocusRequested</span></span>](#add_movefocusrequested) | <span data-ttu-id="18b04-116">Ajoutez un gestionnaire d’événements pour l’événement MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="18b04-116">Add an event handler for the MoveFocusRequested event.</span></span>
[<span data-ttu-id="18b04-117">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="18b04-117">add_ZoomFactorChanged</span></span>](#add_zoomfactorchanged) | <span data-ttu-id="18b04-118">Ajoutez un gestionnaire d’événements pour l’événement ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="18b04-118">Add an event handler for the ZoomFactorChanged event.</span></span>
[<span data-ttu-id="18b04-119">Fermer</span><span class="sxs-lookup"><span data-stu-id="18b04-119">Close</span></span>](#close) | <span data-ttu-id="18b04-120">Ferme le WebView et nettoie l’instance de navigateur sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="18b04-120">Closes the WebView and cleans up the underlying browser instance.</span></span>
[<span data-ttu-id="18b04-121">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="18b04-121">get_Bounds</span></span>](#get_bounds) | <span data-ttu-id="18b04-122">Les limites de l’affichage WebView.</span><span class="sxs-lookup"><span data-stu-id="18b04-122">The webview bounds.</span></span>
[<span data-ttu-id="18b04-123">get_CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="18b04-123">get_CoreWebView2</span></span>](#get_corewebview2) | <span data-ttu-id="18b04-124">Obtient le CoreWebView2 associé à cet CoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="18b04-124">Gets the CoreWebView2 associated with this CoreWebView2Controller.</span></span>
[<span data-ttu-id="18b04-125">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="18b04-125">get_IsVisible</span></span>](#get_isvisible) | <span data-ttu-id="18b04-126">La propriété IsVisible détermine s’il faut afficher ou masquer le WebView.</span><span class="sxs-lookup"><span data-stu-id="18b04-126">The IsVisible property determines whether to show or hide the webview.</span></span>
[<span data-ttu-id="18b04-127">get_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="18b04-127">get_ParentWindow</span></span>](#get_parentwindow) | <span data-ttu-id="18b04-128">Fenêtre parent fournie par l’application utilisée par ce WebView pour afficher le contenu.</span><span class="sxs-lookup"><span data-stu-id="18b04-128">The parent window provided by the app that this WebView is using to render content.</span></span>
[<span data-ttu-id="18b04-129">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="18b04-129">get_ZoomFactor</span></span>](#get_zoomfactor) | <span data-ttu-id="18b04-130">Facteur de zoom pour le WebView.</span><span class="sxs-lookup"><span data-stu-id="18b04-130">The zoom factor for the WebView.</span></span>
[<span data-ttu-id="18b04-131">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="18b04-131">MoveFocus</span></span>](#movefocus) | <span data-ttu-id="18b04-132">Déplacer le focus sur le WebView.</span><span class="sxs-lookup"><span data-stu-id="18b04-132">Move focus into WebView.</span></span>
[<span data-ttu-id="18b04-133">NotifyParentWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="18b04-133">NotifyParentWindowPositionChanged</span></span>](#notifyparentwindowpositionchanged) | <span data-ttu-id="18b04-134">Il s’agit d’une notification distincte des limites qui indiquent à WebView son parent (ou n’importe quel ancêtre) déplacé.</span><span class="sxs-lookup"><span data-stu-id="18b04-134">This is a notification separate from Bounds that tells WebView its parent (or any ancestor) HWND moved.</span></span>
[<span data-ttu-id="18b04-135">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="18b04-135">put_Bounds</span></span>](#put_bounds) | <span data-ttu-id="18b04-136">Définissez la propriété Bounds.</span><span class="sxs-lookup"><span data-stu-id="18b04-136">Set the Bounds property.</span></span>
[<span data-ttu-id="18b04-137">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="18b04-137">put_IsVisible</span></span>](#put_isvisible) | <span data-ttu-id="18b04-138">Définissez la propriété IsVisible.</span><span class="sxs-lookup"><span data-stu-id="18b04-138">Set the IsVisible property.</span></span>
[<span data-ttu-id="18b04-139">put_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="18b04-139">put_ParentWindow</span></span>](#put_parentwindow) | <span data-ttu-id="18b04-140">Définissez la fenêtre parente pour le WebView.</span><span class="sxs-lookup"><span data-stu-id="18b04-140">Set the parent window for the WebView.</span></span>
[<span data-ttu-id="18b04-141">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="18b04-141">put_ZoomFactor</span></span>](#put_zoomfactor) | <span data-ttu-id="18b04-142">Définissez la propriété ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="18b04-142">Set the ZoomFactor property.</span></span>
[<span data-ttu-id="18b04-143">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="18b04-143">remove_AcceleratorKeyPressed</span></span>](#remove_acceleratorkeypressed) | <span data-ttu-id="18b04-144">Supprimez un gestionnaire d’événements préalablement ajouté à add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="18b04-144">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>
[<span data-ttu-id="18b04-145">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="18b04-145">remove_GotFocus</span></span>](#remove_gotfocus) | <span data-ttu-id="18b04-146">Supprimez un gestionnaire d’événements préalablement ajouté à add_GotFocus.</span><span class="sxs-lookup"><span data-stu-id="18b04-146">Remove an event handler previously added with add_GotFocus.</span></span>
[<span data-ttu-id="18b04-147">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="18b04-147">remove_LostFocus</span></span>](#remove_lostfocus) | <span data-ttu-id="18b04-148">Supprimez un gestionnaire d’événements préalablement ajouté à add_LostFocus.</span><span class="sxs-lookup"><span data-stu-id="18b04-148">Remove an event handler previously added with add_LostFocus.</span></span>
[<span data-ttu-id="18b04-149">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="18b04-149">remove_MoveFocusRequested</span></span>](#remove_movefocusrequested) | <span data-ttu-id="18b04-150">Supprimez un gestionnaire d’événements préalablement ajouté à add_MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="18b04-150">Remove an event handler previously added with add_MoveFocusRequested.</span></span>
[<span data-ttu-id="18b04-151">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="18b04-151">remove_ZoomFactorChanged</span></span>](#remove_zoomfactorchanged) | <span data-ttu-id="18b04-152">Supprimez un gestionnaire d’événements préalablement ajouté à add_ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="18b04-152">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>
[<span data-ttu-id="18b04-153">SetBoundsAndZoomFactor</span><span class="sxs-lookup"><span data-stu-id="18b04-153">SetBoundsAndZoomFactor</span></span>](#setboundsandzoomfactor) | <span data-ttu-id="18b04-154">Mettez à jour les propriétés de limites et de ZoomFactor en même temps.</span><span class="sxs-lookup"><span data-stu-id="18b04-154">Update Bounds and ZoomFactor properties at the same time.</span></span>

<span data-ttu-id="18b04-155">Le CoreWebView2Controller possède CoreWebView2, et si toutes les références au CoreWebView2Controller disparaissent, le WebView sera fermé.</span><span class="sxs-lookup"><span data-stu-id="18b04-155">The CoreWebView2Controller owns the CoreWebView2, and if all references to the CoreWebView2Controller go away, the WebView will be closed.</span></span>

## <span data-ttu-id="18b04-156">Ses</span><span class="sxs-lookup"><span data-stu-id="18b04-156">Members</span></span>

#### <span data-ttu-id="18b04-157">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="18b04-157">add_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="18b04-158">Ajoutez un gestionnaire d’événements pour l’événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="18b04-158">Add an event handler for the AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="18b04-159">[add_AcceleratorKeyPressed](#add_acceleratorkeypressed)par le biais du[mot de passe](icorewebview2acceleratorkeypressedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="18b04-159">public HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([ICoreWebView2AcceleratorKeyPressedEventHandler](icorewebview2acceleratorkeypressedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="18b04-160">AcceleratorKeyPressed se déclenche quand une touche d’accès rapide ou une touche de raccourci est enfoncée ou relâche lorsque le WebView est ciblé.</span><span class="sxs-lookup"><span data-stu-id="18b04-160">AcceleratorKeyPressed fires when an accelerator key or key combo is pressed or released while the WebView is focused.</span></span> <span data-ttu-id="18b04-161">Un raccourci est considéré comme un accélérateur s’il s’agit de l’un des éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="18b04-161">A key is considered an accelerator if either:</span></span>

1. <span data-ttu-id="18b04-162">Ctrl ou Alt est en cours de conservation ou</span><span class="sxs-lookup"><span data-stu-id="18b04-162">Ctrl or Alt is currently being held, or</span></span>

1. <span data-ttu-id="18b04-163">la touche appuyée ne correspond pas à un caractère.</span><span class="sxs-lookup"><span data-stu-id="18b04-163">the pressed key does not map to a character.</span></span> <span data-ttu-id="18b04-164">Quelques touches spécifiques ne sont jamais considérées comme des accélérateurs, comme Shift.</span><span class="sxs-lookup"><span data-stu-id="18b04-164">A few specific keys are never considered accelerators, such as Shift.</span></span> <span data-ttu-id="18b04-165">La touche Échap est toujours considérée comme un accélérateur.</span><span class="sxs-lookup"><span data-stu-id="18b04-165">The Escape key is always considered an accelerator.</span></span>

<span data-ttu-id="18b04-166">Les événements de touches répétées déclenchés suite à la fermeture de la clé entraînent également le déclenchement de cet événement.</span><span class="sxs-lookup"><span data-stu-id="18b04-166">Autorepeated key events caused by holding the key down will also fire this event.</span></span> <span data-ttu-id="18b04-167">Vous pouvez les filtrer en vérifiant les arguments d’événements «KeyEventLParam ou PhysicalKeyStatus.</span><span class="sxs-lookup"><span data-stu-id="18b04-167">You can filter these out by checking the event args' KeyEventLParam or PhysicalKeyStatus.</span></span>

<span data-ttu-id="18b04-168">En mode fenêtre, ce gestionnaire d’événements est appelé de manière synchrone.</span><span class="sxs-lookup"><span data-stu-id="18b04-168">In windowed mode, this event handler is called synchronously.</span></span> <span data-ttu-id="18b04-169">Tant que vous n’avez pas appelé handle () sur les arguments d’événement ou que le gestionnaire d’événements renvoie, le processus de navigateur sera bloqué et les appels COM entre processus entrants échoueront avec RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span><span class="sxs-lookup"><span data-stu-id="18b04-169">Until you call Handle() on the event args or the event handler returns, the browser process will be blocked and outgoing cross-process COM calls will fail with RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span></span> <span data-ttu-id="18b04-170">Toutes les méthodes de l’API CoreWebView2 fonctionneront toutefois.</span><span class="sxs-lookup"><span data-stu-id="18b04-170">All CoreWebView2 API methods will work, however.</span></span>

<span data-ttu-id="18b04-171">En mode sans fenêtre, le gestionnaire d’événements est appelé de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="18b04-171">In windowless mode, the event handler is called asynchronously.</span></span> <span data-ttu-id="18b04-172">L’entrée supplémentaire n’atteint pas le navigateur tant que le gestionnaire d’événements n’a pas renvoyé ou que le gestionnaire d’événements n’est pas appelé, mais que le processus du navigateur proprement dit ne sera pas bloqué et que les appels COM sortants fonctionneront normalement.</span><span class="sxs-lookup"><span data-stu-id="18b04-172">Further input will not reach the browser until the event handler returns or Handle() is called, but the browser process itself will not be blocked, and outgoing COM calls will work normally.</span></span>

<span data-ttu-id="18b04-173">Il est recommandé d’appeler handle (vrai) dès que vous en savez que vous voulez gérer la touche accélérateur.</span><span class="sxs-lookup"><span data-stu-id="18b04-173">It is recommended to call Handle(TRUE) as early as you can know that you want to handle the accelerator key.</span></span>

```cpp
    // Register a handler for the AcceleratorKeyPressed event.
    CHECK_FAILURE(m_controller->add_AcceleratorKeyPressed(
        Callback<ICoreWebView2AcceleratorKeyPressedEventHandler>(
            [this](
                ICoreWebView2Controller* sender,
                ICoreWebView2AcceleratorKeyPressedEventArgs* args) -> HRESULT {
                COREWEBVIEW2_KEY_EVENT_KIND kind;
                CHECK_FAILURE(args->get_KeyEventKind(&kind));
                // We only care about key down events.
                if (kind == COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN ||
                    kind == COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN)
                {
                    UINT key;
                    CHECK_FAILURE(args->get_VirtualKey(&key));
                    // Check if the key is one we want to handle.
                    if (std::function<void()> action =
                            m_appWindow->GetAcceleratorKeyFunction(key))
                    {
                        // Keep the browser from handling this key, whether it's autorepeated or
                        // not.
                        CHECK_FAILURE(args->put_Handled(TRUE));

                        // Filter out autorepeated keys.
                        COREWEBVIEW2_PHYSICAL_KEY_STATUS status;
                        CHECK_FAILURE(args->get_PhysicalKeyStatus(&status));
                        if (!status.WasKeyDown)
                        {
                            // Perform the action asynchronously to avoid blocking the
                            // browser process's event queue.
                            m_appWindow->RunAsync(action);
                        }
                    }
                }
                return S_OK;
            })
            .Get(),
        &m_acceleratorKeyPressedToken));
```

#### <span data-ttu-id="18b04-174">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="18b04-174">add_GotFocus</span></span> 

<span data-ttu-id="18b04-175">Ajoutez un gestionnaire d’événements pour l’événement GotFocus.</span><span class="sxs-lookup"><span data-stu-id="18b04-175">Add an event handler for the GotFocus event.</span></span>

> <span data-ttu-id="18b04-176">[add_GotFocus](#add_gotfocus)par le biais du[mot de passe](icorewebview2focuschangedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="18b04-176">public HRESULT [add_GotFocus](#add_gotfocus)([ICoreWebView2FocusChangedEventHandler](icorewebview2focuschangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="18b04-177">GotFocus se déclenche lorsque WebView a le focus.</span><span class="sxs-lookup"><span data-stu-id="18b04-177">GotFocus fires when WebView got focus.</span></span>

#### <span data-ttu-id="18b04-178">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="18b04-178">add_LostFocus</span></span> 

<span data-ttu-id="18b04-179">Ajoutez un gestionnaire d’événements pour l’événement LostFocus.</span><span class="sxs-lookup"><span data-stu-id="18b04-179">Add an event handler for the LostFocus event.</span></span>

> <span data-ttu-id="18b04-180">[add_LostFocus](#add_lostfocus)par le biais du[mot de passe](icorewebview2focuschangedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="18b04-180">public HRESULT [add_LostFocus](#add_lostfocus)([ICoreWebView2FocusChangedEventHandler](icorewebview2focuschangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="18b04-181">LostFocus se déclenche lorsque WebView perd le focus.</span><span class="sxs-lookup"><span data-stu-id="18b04-181">LostFocus fires when WebView lost focus.</span></span> <span data-ttu-id="18b04-182">Dans le cas où l’événement MoveFocusRequested est déclenché, le focus est toujours sur le WebView lors du déclenchement de l’événement MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="18b04-182">In the case where MoveFocusRequested event is fired, the focus is still on WebView when MoveFocusRequested event fires.</span></span> <span data-ttu-id="18b04-183">Le focus perdu ne se déclenche que lorsque le code de l’application ou l’action par défaut de l’événement MoveFocusRequested a défini le focus hors du WebView.</span><span class="sxs-lookup"><span data-stu-id="18b04-183">Lost focus only fires afterwards when app's code or default action of MoveFocusRequested event set focus away from WebView.</span></span>

#### <span data-ttu-id="18b04-184">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="18b04-184">add_MoveFocusRequested</span></span> 

<span data-ttu-id="18b04-185">Ajoutez un gestionnaire d’événements pour l’événement MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="18b04-185">Add an event handler for the MoveFocusRequested event.</span></span>

> <span data-ttu-id="18b04-186">[add_MoveFocusRequested](#add_movefocusrequested)par le biais du[mot de passe](icorewebview2movefocusrequestedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="18b04-186">public HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([ICoreWebView2MoveFocusRequestedEventHandler](icorewebview2movefocusrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="18b04-187">MoveFocusRequested est déclenché lorsque l’utilisateur tente d’accéder à l’onglet du WebView.</span><span class="sxs-lookup"><span data-stu-id="18b04-187">MoveFocusRequested fires when user tries to tab out of the WebView.</span></span> <span data-ttu-id="18b04-188">Le focus du WebView n’a pas changé lors du déclenchement de cet événement.</span><span class="sxs-lookup"><span data-stu-id="18b04-188">The WebView's focus has not changed when this event is fired.</span></span>

```cpp
    // Register a handler for the MoveFocusRequested event.
    // This event will be fired when the user tabs out of the webview.
    // The handler will focus another window in the app, depending on which
    // direction the focus is being shifted.
    CHECK_FAILURE(m_controller->add_MoveFocusRequested(
        Callback<ICoreWebView2MoveFocusRequestedEventHandler>(
            [this](
                ICoreWebView2Controller* sender,
                ICoreWebView2MoveFocusRequestedEventArgs* args) -> HRESULT {
                if (!g_autoTabHandle)
                {
                    COREWEBVIEW2_MOVE_FOCUS_REASON reason;
                    CHECK_FAILURE(args->get_Reason(&reason));

                    if (reason == COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT)
                    {
                        TabForwards(-1);
                    }
                    else if (reason == COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS)
                    {
                        TabBackwards(int(m_tabbableWindows.size()));
                    }
                    CHECK_FAILURE(args->put_Handled(TRUE));
                }
                return S_OK;
            })
            .Get(),
        &m_moveFocusRequestedToken));
```

#### <span data-ttu-id="18b04-189">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="18b04-189">add_ZoomFactorChanged</span></span> 

<span data-ttu-id="18b04-190">Ajoutez un gestionnaire d’événements pour l’événement ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="18b04-190">Add an event handler for the ZoomFactorChanged event.</span></span>

> <span data-ttu-id="18b04-191">[add_ZoomFactorChanged](#add_zoomfactorchanged)par le biais du[mot de passe](icorewebview2zoomfactorchangedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="18b04-191">public HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([ICoreWebView2ZoomFactorChangedEventHandler](icorewebview2zoomfactorchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="18b04-192">L’événement se déclenche lorsque la propriété ZoomFactor de l’élément WebView change.</span><span class="sxs-lookup"><span data-stu-id="18b04-192">The event fires when the ZoomFactor property of the WebView changes.</span></span> <span data-ttu-id="18b04-193">L’événement peut être déclenché en raison du fait que l’appelant a modifié la propriété ZoomFactor, ou en raison de l’utilisateur modifiant manuellement le zoom.</span><span class="sxs-lookup"><span data-stu-id="18b04-193">The event could fire because the caller modified the ZoomFactor property, or due to the user manually modifying the zoom.</span></span> <span data-ttu-id="18b04-194">Lorsqu’il est modifié par l’appelant par le biais de la propriété ZoomFactor, le facteur de zoom interne est mis à jour immédiatement et il n’y a pas d’événement ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="18b04-194">When it is modified by the caller via the ZoomFactor property, the internal zoom factor is updated immediately and there will be no ZoomFactorChanged event.</span></span> <span data-ttu-id="18b04-195">WebView associe le dernier facteur de zoom utilisé pour chaque site.</span><span class="sxs-lookup"><span data-stu-id="18b04-195">WebView associates the last used zoom factor for each site.</span></span> <span data-ttu-id="18b04-196">Par conséquent, il est possible de modifier le facteur de zoom lorsque vous naviguez vers une autre page.</span><span class="sxs-lookup"><span data-stu-id="18b04-196">Therefore, it is possible for the zoom factor to change when navigating to a different page.</span></span> <span data-ttu-id="18b04-197">Lorsque le facteur de zoom change en raison de cela, l’événement ZoomFactorChanged se déclenche immédiatement après l’événement ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="18b04-197">When the zoom factor changes due to this, the ZoomFactorChanged event fires right after the ContentLoading event.</span></span>

```cpp
    // Register a handler for the ZoomFactorChanged event.
    // This handler just announces the new level of zoom on the window's title bar.
    CHECK_FAILURE(m_controller->add_ZoomFactorChanged(
        Callback<ICoreWebView2ZoomFactorChangedEventHandler>(
            [this](ICoreWebView2Controller* sender, IUnknown* args) -> HRESULT {
                double zoomFactor;
                CHECK_FAILURE(sender->get_ZoomFactor(&zoomFactor));

                std::wstring message = L"WebView2APISample (Zoom: " +
                                       std::to_wstring(int(zoomFactor * 100)) + L"%)";
                SetWindowText(m_appWindow->GetMainWindow(), message.c_str());
                return S_OK;
            })
            .Get(),
        &m_zoomFactorChangedToken));
```

#### <span data-ttu-id="18b04-198">Fermer</span><span class="sxs-lookup"><span data-stu-id="18b04-198">Close</span></span> 

<span data-ttu-id="18b04-199">Ferme le WebView et nettoie l’instance de navigateur sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="18b04-199">Closes the WebView and cleans up the underlying browser instance.</span></span>

> <span data-ttu-id="18b04-200">valeur publique [HRESULT (](#close))</span><span class="sxs-lookup"><span data-stu-id="18b04-200">public HRESULT [Close](#close)()</span></span>

<span data-ttu-id="18b04-201">Le nettoyage de l’instance du navigateur entraîne la libération des ressources du WebView.</span><span class="sxs-lookup"><span data-stu-id="18b04-201">Cleaning up the browser instance will release the resources powering the WebView.</span></span> <span data-ttu-id="18b04-202">L’instance du navigateur sera arrêtée s’il n’y a aucune autre WebView.</span><span class="sxs-lookup"><span data-stu-id="18b04-202">The browser instance will be shut down if there are no other WebViews using it.</span></span>

<span data-ttu-id="18b04-203">Après avoir appelé Close, tous les appels de méthode échouent et les gestionnaires d’événements cessent de se déclencher.</span><span class="sxs-lookup"><span data-stu-id="18b04-203">After calling Close, all method calls will fail and event handlers will stop firing.</span></span> <span data-ttu-id="18b04-204">Plus précisément, le WebView publie ses références à ses gestionnaires d’événements lorsque la méthode Close est appelée.</span><span class="sxs-lookup"><span data-stu-id="18b04-204">Specifically, the WebView will release its references to its event handlers when Close is called.</span></span>

<span data-ttu-id="18b04-205">Close est appelé implicitement lorsque CoreWebView2Controller perd sa référence finale et est détruit.</span><span class="sxs-lookup"><span data-stu-id="18b04-205">Close is implicitly called when the CoreWebView2Controller loses its final reference and is destructed.</span></span> <span data-ttu-id="18b04-206">Mais il est conseillé d’appeler explicitement Close pour éviter tout cycle accidentel de références entre le WebView et le code de l’application.</span><span class="sxs-lookup"><span data-stu-id="18b04-206">But it is best practice to explicitly call Close to avoid any accidental cycle of references between the WebView and the app code.</span></span> <span data-ttu-id="18b04-207">En particulier, si vous capturez une référence à WebView dans un gestionnaire d’événements, vous créerez un cycle de référence entre le WebView et le gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="18b04-207">Specifically, if you capture a reference to the WebView in an event handler you will create a reference cycle between the WebView and the event handler.</span></span> <span data-ttu-id="18b04-208">L’appel de la fermeture rompt ce cycle en libérant tous les gestionnaires d’événements.</span><span class="sxs-lookup"><span data-stu-id="18b04-208">Calling Close will break this cycle by releasing all event handlers.</span></span> <span data-ttu-id="18b04-209">Néanmoins, pour éviter ce problème, il est préférable d’appeler explicitement l’application WebView et de ne pas capturer de référence à WebView pour s’assurer que le WebView peut être nettoyé correctement.</span><span class="sxs-lookup"><span data-stu-id="18b04-209">But to avoid this situation it is best practice both to explicitly call Close on the WebView and to not capture a reference to the WebView to ensure the WebView can be cleaned up correctly.</span></span>

```cpp
// Close the WebView and deinitialize related state. This doesn't close the app window.
void AppWindow::CloseWebView(bool cleanupUserDataFolder)
{
    DeleteAllComponents();
    if (m_controller)
    {
        m_controller->Close();
        m_controller = nullptr;
        m_webView = nullptr;
    }
    m_webViewEnvironment = nullptr;
    if (cleanupUserDataFolder)
    {
        // For non-UWP apps, the default user data folder {Executable File Name}.WebView2
        // is in the same directory next to the app executable. If end
        // developers specify userDataFolder during WebView environment
        // creation, they would need to pass in that explicit value here.
        // For more information about userDataFolder:
        // https://docs.microsoft.com/microsoft-edge/hosting/webview2/reference/win32/0-9-488/webview2-idl#createwebview2environmentwithoptions
        WCHAR userDataFolder[MAX_PATH] = L"";
        // Obtain the absolute path for relative paths that include "./" or "../"
        _wfullpath(
            userDataFolder, GetLocalPath(L"WebView2APISample.exe.WebView2").c_str(), MAX_PATH);
        std::wstring userDataFolderPath(userDataFolder);

        std::wstring message = L"Are you sure you want to clean up the user data folder at\n";
        message += userDataFolderPath;
        message += L"\n?\nWarning: This action is not reversible.\n\n";
        message += L"Click No if there are other open WebView instances.\n";

        if (MessageBox(m_mainWindow, message.c_str(), L"Cleanup User Data Folder", MB_YESNO) ==
            IDYES)
        {
            CHECK_FAILURE(DeleteFileRecursive(userDataFolderPath));
        }
    }
}
```

#### <span data-ttu-id="18b04-210">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="18b04-210">get_Bounds</span></span> 

<span data-ttu-id="18b04-211">Les limites de l’affichage WebView.</span><span class="sxs-lookup"><span data-stu-id="18b04-211">The webview bounds.</span></span>

> <span data-ttu-id="18b04-212">[get_Boundss](#get_bounds)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="18b04-212">public HRESULT [get_Bounds](#get_bounds)(RECT \* bounds)</span></span>

<span data-ttu-id="18b04-213">Les limites sont relatives au HWND parent.</span><span class="sxs-lookup"><span data-stu-id="18b04-213">Bounds are relative to the parent HWND.</span></span> <span data-ttu-id="18b04-214">L’application peut positionner un WebView de deux manières:</span><span class="sxs-lookup"><span data-stu-id="18b04-214">The app has two ways it can position a WebView:</span></span>

1. <span data-ttu-id="18b04-215">Créer un HWND enfant qui est le HWND parent WebView.</span><span class="sxs-lookup"><span data-stu-id="18b04-215">Create a child HWND that is the WebView parent HWND.</span></span> <span data-ttu-id="18b04-216">Positionnez cette fenêtre dans laquelle le WebView devrait être.</span><span class="sxs-lookup"><span data-stu-id="18b04-216">Position this window where the WebView should be.</span></span> <span data-ttu-id="18b04-217">Dans le cas présent, utilisez (0, 0) pour le coin supérieur gauche de la vue de Bound’s (offset).</span><span class="sxs-lookup"><span data-stu-id="18b04-217">In this case, use (0, 0) for the WebView's Bound's top left corner (the offset).</span></span>

1. <span data-ttu-id="18b04-218">Utilisez la plus grande fenêtre de l’application en tant que HWND parent d’affichage.</span><span class="sxs-lookup"><span data-stu-id="18b04-218">Use the app's top most window as the WebView parent HWND.</span></span> <span data-ttu-id="18b04-219">Définissez le coin supérieur gauche de l’Bound’s WebView de sorte que le contrôle WebView soit correctement positionné dans l’application.</span><span class="sxs-lookup"><span data-stu-id="18b04-219">Set the WebView's Bound's top left corner so that the WebView is positioned correctly in the app.</span></span> <span data-ttu-id="18b04-220">Les valeurs de limites se trouvent dans l’espace de coordonnées de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="18b04-220">The Bound's values are in the host's coordinate space.</span></span>

#### <span data-ttu-id="18b04-221">get_CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="18b04-221">get_CoreWebView2</span></span> 

<span data-ttu-id="18b04-222">Obtient le CoreWebView2 associé à cet CoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="18b04-222">Gets the CoreWebView2 associated with this CoreWebView2Controller.</span></span>

> <span data-ttu-id="18b04-223">[get_CoreWebView2](#get_corewebview2)par le biais du public HRESULT ([ICoreWebView2](icorewebview2.md) \* \* CoreWebView2)</span><span class="sxs-lookup"><span data-stu-id="18b04-223">public HRESULT [get_CoreWebView2](#get_corewebview2)([ICoreWebView2](icorewebview2.md) \*\* coreWebView2)</span></span>

#### <span data-ttu-id="18b04-224">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="18b04-224">get_IsVisible</span></span> 

<span data-ttu-id="18b04-225">La propriété IsVisible détermine s’il faut afficher ou masquer le WebView.</span><span class="sxs-lookup"><span data-stu-id="18b04-225">The IsVisible property determines whether to show or hide the webview.</span></span>

> <span data-ttu-id="18b04-226">valeur publique HRESULT [get_IsVisible](#get_isvisible)(bool \* IsVisible)</span><span class="sxs-lookup"><span data-stu-id="18b04-226">public HRESULT [get_IsVisible](#get_isvisible)(BOOL \* isVisible)</span></span>

<span data-ttu-id="18b04-227">Si la valeur de l’argument IsVisible est définie sur false, le WebView sera transparent et ne sera pas affiché.</span><span class="sxs-lookup"><span data-stu-id="18b04-227">If IsVisible is set to false, the webview will be transparent and will not be rendered.</span></span> <span data-ttu-id="18b04-228">Toutefois, cela n’affecte pas la fenêtre qui contient le WebView (le paramètre HWND transmis à CreateCoreWebView2Controller).</span><span class="sxs-lookup"><span data-stu-id="18b04-228">However, this will not affect the window containing the webview (the HWND parameter that was passed to CreateCoreWebView2Controller).</span></span> <span data-ttu-id="18b04-229">Si vous souhaitez que cette fenêtre disparaisse également, appelez la fonction ShowWindow sur celle-ci directement en plus de modifier la propriété IsVisible.</span><span class="sxs-lookup"><span data-stu-id="18b04-229">If you want that window to disappear too, call ShowWindow on it directly in addition to modifying the IsVisible property.</span></span> <span data-ttu-id="18b04-230">Le mode webaffichage sous forme de fenêtre enfant ne recevra pas de messages de fenêtre lorsque la fenêtre supérieure est réduite ou restaurée.</span><span class="sxs-lookup"><span data-stu-id="18b04-230">WebView as a child window won't get window messages when the top window is minimized or restored.</span></span> <span data-ttu-id="18b04-231">Pour des raisons de performances, le développeur doit définir la propriété IsVisible du WebView sur false lorsque la fenêtre de l’application est réduite, puis revenir à la valeur true lorsque la fenêtre de l’application est restaurée.</span><span class="sxs-lookup"><span data-stu-id="18b04-231">For performance reason, developer should set IsVisible property of the WebView to false when the app window is minimized and back to true when app window is restored.</span></span> <span data-ttu-id="18b04-232">Pour cela, la fenêtre de l’application peut gérer les SC_MINIMIZE et de SC_RESTORE commande lors de la réception d’WM_SYSCOMMAND message.</span><span class="sxs-lookup"><span data-stu-id="18b04-232">App window can do this by handling SC_MINIMIZE and SC_RESTORE command upon receiving WM_SYSCOMMAND message.</span></span>

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_controller->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_controller->put_IsVisible(m_isVisible);
}
```

#### <span data-ttu-id="18b04-233">get_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="18b04-233">get_ParentWindow</span></span> 

<span data-ttu-id="18b04-234">Fenêtre parent fournie par l’application utilisée par ce WebView pour afficher le contenu.</span><span class="sxs-lookup"><span data-stu-id="18b04-234">The parent window provided by the app that this WebView is using to render content.</span></span>

> <span data-ttu-id="18b04-235">valeur publique HRESULT [get_ParentWindow](#get_parentwindow)(HWND \* topLevelWindow)</span><span class="sxs-lookup"><span data-stu-id="18b04-235">public HRESULT [get_ParentWindow](#get_parentwindow)(HWND \* topLevelWindow)</span></span>

<span data-ttu-id="18b04-236">Cette API renvoie initialement la fenêtre transmise à CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="18b04-236">This API initially returns the window passed into CreateCoreWebView2Controller.</span></span>

#### <span data-ttu-id="18b04-237">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="18b04-237">get_ZoomFactor</span></span> 

<span data-ttu-id="18b04-238">Facteur de zoom pour le WebView.</span><span class="sxs-lookup"><span data-stu-id="18b04-238">The zoom factor for the WebView.</span></span>

> <span data-ttu-id="18b04-239">valeur publique HRESULT [get_ZoomFactor](#get_zoomfactor)(double \* ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="18b04-239">public HRESULT [get_ZoomFactor](#get_zoomfactor)(double \* zoomFactor)</span></span>

<span data-ttu-id="18b04-240">Notez que la modification du facteur de zoom peut entraîner la modification de la `window.innerWidth/innerHeight` mise en page.</span><span class="sxs-lookup"><span data-stu-id="18b04-240">Note that changing zoom factor could cause `window.innerWidth/innerHeight` and page layout to change.</span></span> <span data-ttu-id="18b04-241">Le facteur de zoom appliqué par l’hôte en appelant ZoomFactor devient le nouveau zoom par défaut de l’affichage WebView.</span><span class="sxs-lookup"><span data-stu-id="18b04-241">A zoom factor that is applied by the host by calling ZoomFactor becomes the new default zoom for the WebView.</span></span> <span data-ttu-id="18b04-242">Ce facteur de zoom s’applique aux différentes navigations et le facteur de zoom est renvoyé lorsque l’utilisateur appuie sur Ctrl + 0.</span><span class="sxs-lookup"><span data-stu-id="18b04-242">This zoom factor applies across navigations and is the zoom factor WebView is returned to when the user presses ctrl+0.</span></span> <span data-ttu-id="18b04-243">Lorsque le facteur de zoom est modifié par l’utilisateur (ce qui permet à l’application de recevoir ZoomFactorChanged), ce zoom s’applique uniquement à la page active.</span><span class="sxs-lookup"><span data-stu-id="18b04-243">When the zoom factor is changed by the user (resulting in the app receiving ZoomFactorChanged), that zoom applies only for the current page.</span></span> <span data-ttu-id="18b04-244">Tout zoom appliqué à un utilisateur est réservé uniquement à la page active et est réinitialisé sur une navigation.</span><span class="sxs-lookup"><span data-stu-id="18b04-244">Any user applied zoom is only for the current page and is reset on a navigation.</span></span> <span data-ttu-id="18b04-245">La spécification d’un zoomFactor inférieur ou égal à 0 n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="18b04-245">Specifying a zoomFactor less than or equal to 0 is not allowed.</span></span> <span data-ttu-id="18b04-246">WebView possède également une plage de facteur de zoom prise en charge interne.</span><span class="sxs-lookup"><span data-stu-id="18b04-246">WebView also has an internal supported zoom factor range.</span></span> <span data-ttu-id="18b04-247">Lorsque le facteur de zoom spécifié est en dehors de cette plage, il est normalisé pour être dans la plage et un événement ZoomFactorChanged est déclenché pour le facteur de zoom réel appliqué.</span><span class="sxs-lookup"><span data-stu-id="18b04-247">When a specified zoom factor is out of that range, it will be normalized to be within the range, and a ZoomFactorChanged event will be fired for the real applied zoom factor.</span></span> <span data-ttu-id="18b04-248">Lorsque cette situation se produit, la propriété ZoomFactor indique le facteur de zoom spécifié lors de la modification précédente de la propriété ZoomFactor jusqu’à ce que l’événement ZoomFactorChanged soit reçu lorsque WebView applique le facteur de zoom normalisé.</span><span class="sxs-lookup"><span data-stu-id="18b04-248">When this range normalization happens, the ZoomFactor property will report the zoom factor specified during the previous modification of the ZoomFactor property until the ZoomFactorChanged event is received after webview applies the normalized zoom factor.</span></span>

#### <span data-ttu-id="18b04-249">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="18b04-249">MoveFocus</span></span> 

<span data-ttu-id="18b04-250">Déplacer le focus sur le WebView.</span><span class="sxs-lookup"><span data-stu-id="18b04-250">Move focus into WebView.</span></span>

> <span data-ttu-id="18b04-251">public HRESULT [MoveFocus](#movefocus)(COREWEBVIEW2_MOVE_FOCUS_REASON raison)</span><span class="sxs-lookup"><span data-stu-id="18b04-251">public HRESULT [MoveFocus](#movefocus)(COREWEBVIEW2_MOVE_FOCUS_REASON reason)</span></span>

<span data-ttu-id="18b04-252">WebView va mettre le focus et le focus sur l’élément correspondant dans la page hébergée dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="18b04-252">WebView will get focus and focus will be set to correspondent element in the page hosted in the WebView.</span></span> <span data-ttu-id="18b04-253">Pour des raisons de programmation, le focus est défini sur l’élément précédemment prioritaire ou l’élément par défaut s’il n’y a pas d’élément prioritaire auparavant.</span><span class="sxs-lookup"><span data-stu-id="18b04-253">For Programmatic reason, focus is set to previously focused element or the default element if there is no previously focused element.</span></span> <span data-ttu-id="18b04-254">Pour une raison suivante, le focus est défini sur le premier élément.</span><span class="sxs-lookup"><span data-stu-id="18b04-254">For Next reason, focus is set to the first element.</span></span> <span data-ttu-id="18b04-255">Pour une raison précédente, le focus est défini sur le dernier élément.</span><span class="sxs-lookup"><span data-stu-id="18b04-255">For Previous reason, focus is set to the last element.</span></span> <span data-ttu-id="18b04-256">Le mode webaffichage peut également mettre le focus sur une interaction utilisateur telle que cliquer sur le WebView ou sur Tab.</span><span class="sxs-lookup"><span data-stu-id="18b04-256">WebView can also got focus through user interaction like clicking into WebView or Tab into it.</span></span> <span data-ttu-id="18b04-257">Pour la fonction de tabulation, l’application peut appeler MoveFocus avec Next ou Previous pour s’aligner sur TAB et Maj + Tab lorsqu’elle décide que le WebView est l’élément tabbable suivant.</span><span class="sxs-lookup"><span data-stu-id="18b04-257">For tabbing, the app can call MoveFocus with Next or Previous to align with tab and shift+tab respectively when it decides the WebView is the next tabbable element.</span></span> <span data-ttu-id="18b04-258">Par exemple, l’application peut appeler IsDialogMessage dans le cadre de sa boucle de messages pour permettre à la plateforme de gérer automatiquement la tabulation.</span><span class="sxs-lookup"><span data-stu-id="18b04-258">Or, the app can call IsDialogMessage as part of its message loop to allow the platform to auto handle tabbing.</span></span> <span data-ttu-id="18b04-259">La plateforme est pivotée sur toutes les fenêtres avec WS_TABSTOP.</span><span class="sxs-lookup"><span data-stu-id="18b04-259">The platform will rotate through all windows with WS_TABSTOP.</span></span> <span data-ttu-id="18b04-260">Lorsque le WebView obtient le focus de IsDialogMessage, il positionne en interne le focus sur le premier ou le dernier élément de Tab et Maj + Tab respectivement.</span><span class="sxs-lookup"><span data-stu-id="18b04-260">When the WebView gets focus from IsDialogMessage, it will internally put the focus on the first or last element for tab and shift+tab respectively.</span></span>

```cpp
    while (GetMessage(&msg, nullptr, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            // Calling IsDialogMessage handles Tab traversal automatically. If the
            // app wants the platform to auto handle tab, then call IsDialogMessage
            // before calling TranslateMessage/DispatchMessage. If the app wants to
            // handle tabbing itself, then skip calling IsDialogMessage and call
            // TranslateMessage/DispatchMessage directly.
            if (!g_autoTabHandle || !IsDialogMessage(GetAncestor(msg.hwnd, GA_ROOT), &msg))
            {
                TranslateMessage(&msg);
                DispatchMessage(&msg);
            }
        }
    }
```

```cpp
        if (wParam == VK_TAB)
        {
            // Find out if the window is one we've customized for tab handling
            for (size_t i = 0; i < m_tabbableWindows.size(); i++)
            {
                if (m_tabbableWindows[i].first == hWnd)
                {
                    if (GetKeyState(VK_SHIFT) < 0)
                    {
                        TabBackwards(i);
                    }
                    else
                    {
                        TabForwards(i);
                    }
                    return true;
                }
            }
        }
```

```cpp
void ControlComponent::TabForwards(int currentIndex)
{
    // Find first enabled window after the active one
    for (size_t i = currentIndex + 1; i < m_tabbableWindows.size(); i++)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    m_controller->MoveFocus(COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT);
}

void ControlComponent::TabBackwards(int currentIndex)
{
    // Find first enabled window before the active one
    for (int i = currentIndex - 1; i >= 0; i--)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    CHECK_FAILURE(m_controller->MoveFocus(COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS));
}
```

#### <span data-ttu-id="18b04-261">NotifyParentWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="18b04-261">NotifyParentWindowPositionChanged</span></span> 

<span data-ttu-id="18b04-262">Il s’agit d’une notification distincte des limites qui indiquent à WebView son parent (ou n’importe quel ancêtre) déplacé.</span><span class="sxs-lookup"><span data-stu-id="18b04-262">This is a notification separate from Bounds that tells WebView its parent (or any ancestor) HWND moved.</span></span>

> <span data-ttu-id="18b04-263">public HRESULT [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()</span><span class="sxs-lookup"><span data-stu-id="18b04-263">public HRESULT [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()</span></span>

<span data-ttu-id="18b04-264">Cela est nécessaire pour l’accessibilité et certaines boîtes de dialogue dans WebView pour fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="18b04-264">This is needed for accessibility and certain dialogs in WebView to work correctly.</span></span> 
```cpp
    if (message == WM_MOVE || message == WM_MOVING)
    {
        m_controller->NotifyParentWindowPositionChanged();
        return true;
    }
```

#### <span data-ttu-id="18b04-265">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="18b04-265">put_Bounds</span></span> 

<span data-ttu-id="18b04-266">Définissez la propriété Bounds.</span><span class="sxs-lookup"><span data-stu-id="18b04-266">Set the Bounds property.</span></span>

> <span data-ttu-id="18b04-267">[put_Bounds](#put_bounds)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="18b04-267">public HRESULT [put_Bounds](#put_bounds)(RECT bounds)</span></span>

```cpp
// Update the bounds of the WebView window to fit available space.
void ViewComponent::ResizeWebView()
{
    SIZE webViewSize = {
            LONG((m_webViewBounds.right - m_webViewBounds.left) * m_webViewRatio * m_webViewScale),
            LONG((m_webViewBounds.bottom - m_webViewBounds.top) * m_webViewRatio * m_webViewScale) };

    RECT desiredBounds = m_webViewBounds;
    desiredBounds.bottom = LONG(
        webViewSize.cy + m_webViewBounds.top);
    desiredBounds.right = LONG(
        webViewSize.cx + m_webViewBounds.left);

    m_controller->put_Bounds(desiredBounds);
    if (m_compositionController)
    {
        POINT webViewOffset = {m_webViewBounds.left, m_webViewBounds.top};

        if (m_dcompDevice)
        {
            CHECK_FAILURE(m_dcompRootVisual->SetOffsetX(float(webViewOffset.x)));
            CHECK_FAILURE(m_dcompRootVisual->SetOffsetY(float(webViewOffset.y)));
            CHECK_FAILURE(m_dcompRootVisual->SetClip(
                {0, 0, float(webViewSize.cx), float(webViewSize.cy)}));
            CHECK_FAILURE(m_dcompDevice->Commit());
        }
        else if (m_wincompHelper)
        {
            m_wincompHelper->UpdateSizeAndPosition(webViewOffset, webViewSize);
        }
    }
}
```

#### <span data-ttu-id="18b04-268">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="18b04-268">put_IsVisible</span></span> 

<span data-ttu-id="18b04-269">Définissez la propriété IsVisible.</span><span class="sxs-lookup"><span data-stu-id="18b04-269">Set the IsVisible property.</span></span>

> <span data-ttu-id="18b04-270">valeur HRESULT publique [put_IsVisible](#put_isvisible)(bool IsVisible)</span><span class="sxs-lookup"><span data-stu-id="18b04-270">public HRESULT [put_IsVisible](#put_isvisible)(BOOL isVisible)</span></span>

```cpp
    if (message == WM_SYSCOMMAND)
    {
        if (wParam == SC_MINIMIZE)
        {
            // Hide the webview when the app window is minimized.
            m_controller->put_IsVisible(FALSE);
        }
        else if (wParam == SC_RESTORE)
        {
            // When the app window is restored, show the webview
            // (unless the user has toggle visibility off).
            if (m_isVisible)
            {
                m_controller->put_IsVisible(TRUE);
            }
        }
    }
```

#### <span data-ttu-id="18b04-271">put_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="18b04-271">put_ParentWindow</span></span> 

<span data-ttu-id="18b04-272">Définissez la fenêtre parente pour le WebView.</span><span class="sxs-lookup"><span data-stu-id="18b04-272">Set the parent window for the WebView.</span></span>

> <span data-ttu-id="18b04-273">[put_ParentWindow](#put_parentwindow)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="18b04-273">public HRESULT [put_ParentWindow](#put_parentwindow)(HWND topLevelWindow)</span></span>

<span data-ttu-id="18b04-274">Cela a pour effet de refaire de la fenêtre de l’affichage de nouveau dans la fenêtre qui vient d’être fournie.</span><span class="sxs-lookup"><span data-stu-id="18b04-274">This will cause the WebView to reparent its window to the newly provided window.</span></span>

#### <span data-ttu-id="18b04-275">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="18b04-275">put_ZoomFactor</span></span> 

<span data-ttu-id="18b04-276">Définissez la propriété ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="18b04-276">Set the ZoomFactor property.</span></span>

> <span data-ttu-id="18b04-277">[put_ZoomFactor](#put_zoomfactor)par le biais du public HRESULT (double ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="18b04-277">public HRESULT [put_ZoomFactor](#put_zoomfactor)(double zoomFactor)</span></span>

#### <span data-ttu-id="18b04-278">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="18b04-278">remove_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="18b04-279">Supprimez un gestionnaire d’événements préalablement ajouté à add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="18b04-279">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>

> <span data-ttu-id="18b04-280">[remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="18b04-280">public HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="18b04-281">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="18b04-281">remove_GotFocus</span></span> 

<span data-ttu-id="18b04-282">Supprimez un gestionnaire d’événements préalablement ajouté à add_GotFocus.</span><span class="sxs-lookup"><span data-stu-id="18b04-282">Remove an event handler previously added with add_GotFocus.</span></span>

> <span data-ttu-id="18b04-283">[remove_GotFocus](#remove_gotfocus)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="18b04-283">public HRESULT [remove_GotFocus](#remove_gotfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="18b04-284">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="18b04-284">remove_LostFocus</span></span> 

<span data-ttu-id="18b04-285">Supprimez un gestionnaire d’événements préalablement ajouté à add_LostFocus.</span><span class="sxs-lookup"><span data-stu-id="18b04-285">Remove an event handler previously added with add_LostFocus.</span></span>

> <span data-ttu-id="18b04-286">[remove_LostFocus](#remove_lostfocus)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="18b04-286">public HRESULT [remove_LostFocus](#remove_lostfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="18b04-287">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="18b04-287">remove_MoveFocusRequested</span></span> 

<span data-ttu-id="18b04-288">Supprimez un gestionnaire d’événements préalablement ajouté à add_MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="18b04-288">Remove an event handler previously added with add_MoveFocusRequested.</span></span>

> <span data-ttu-id="18b04-289">[remove_MoveFocusRequested](#remove_movefocusrequested)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="18b04-289">public HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="18b04-290">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="18b04-290">remove_ZoomFactorChanged</span></span> 

<span data-ttu-id="18b04-291">Supprimez un gestionnaire d’événements préalablement ajouté à add_ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="18b04-291">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>

> <span data-ttu-id="18b04-292">[remove_ZoomFactorChanged](#remove_zoomfactorchanged)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="18b04-292">public HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="18b04-293">SetBoundsAndZoomFactor</span><span class="sxs-lookup"><span data-stu-id="18b04-293">SetBoundsAndZoomFactor</span></span> 

<span data-ttu-id="18b04-294">Mettez à jour les propriétés de limites et de ZoomFactor en même temps.</span><span class="sxs-lookup"><span data-stu-id="18b04-294">Update Bounds and ZoomFactor properties at the same time.</span></span>

> <span data-ttu-id="18b04-295">public HRESULT [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(limites de Rect, double ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="18b04-295">public HRESULT [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(RECT bounds, double zoomFactor)</span></span>

<span data-ttu-id="18b04-296">Cette opération est atomique du point de vue de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="18b04-296">This operation is atomic from the host's perspective.</span></span> <span data-ttu-id="18b04-297">Après avoir retourné la fonction, les limites et les propriétés ZoomFactor ont été mises à jour si la fonction est réussie, ou ne sont pas mises à jour en cas d’échec de la fonction.</span><span class="sxs-lookup"><span data-stu-id="18b04-297">After returning from this function, the Bounds and ZoomFactor properties will have both been updated if the function is successful, or neither will be updated if the function fails.</span></span> <span data-ttu-id="18b04-298">Si les limites et ZoomFactor sont toutes deux mises à jour par la même échelle (c’est-à-dire que les limites et ZoomFactor sont tous deux doublées), la page ne verra aucune modification apportée à Window. innerWidth/innerHeight et le WebView fera apparaître le contenu aux nouvelles tailles et zooms sans rendu intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="18b04-298">If Bounds and ZoomFactor are both updated by the same scale (i.e. Bounds and ZoomFactor are both doubled), then the page will not see a change in window.innerWidth/innerHeight and the WebView will render the content at the new size and zoom without intermediate renderings.</span></span> <span data-ttu-id="18b04-299">Cette fonction peut également être utilisée pour mettre à jour une seule de ZoomFactor ou de limites en passant la nouvelle valeur pour une et la valeur actuelle pour l’autre.</span><span class="sxs-lookup"><span data-stu-id="18b04-299">This function can also be used to update just one of ZoomFactor or Bounds by passing in the new value for one and the current value for the other.</span></span>

```cpp
void ViewComponent::SetScale(float scale)
{
    RECT bounds;
    CHECK_FAILURE(m_controller->get_Bounds(&bounds));
    double scaleChange = scale / m_webViewScale;

    bounds.bottom = LONG(
        (bounds.bottom - bounds.top) * scaleChange + bounds.top);
    bounds.right = LONG(
        (bounds.right - bounds.left) * scaleChange + bounds.left);

    m_webViewScale = scale;
    m_controller->SetBoundsAndZoomFactor(bounds, scale);
}
```

