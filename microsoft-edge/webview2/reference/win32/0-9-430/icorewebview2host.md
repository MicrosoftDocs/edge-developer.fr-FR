---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2Host
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 9202c17d83ad7d0750dbf76724b550d73ecca434
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881032"
---
# <span data-ttu-id="e1428-104">0.9.430-interface ICoreWebView2Host</span><span class="sxs-lookup"><span data-stu-id="e1428-104">0.9.430 - interface ICoreWebView2Host</span></span> 

> [!NOTE]
> <span data-ttu-id="e1428-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="e1428-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="e1428-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="e1428-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Host
  : public IUnknown
```

<span data-ttu-id="e1428-107">Cette interface est le propriétaire de l’objet CoreWebView2 et prend en charge le redimensionnement, l’affichage et le masquage, le focus, ainsi que d’autres fonctionnalités relatives à la fenêtre et à la composition.</span><span class="sxs-lookup"><span data-stu-id="e1428-107">This interface is the owner of the CoreWebView2 object, and provides support for resizing, showing and hiding, focusing, and other functionality related to windowing and composition.</span></span>

## <span data-ttu-id="e1428-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="e1428-108">Summary</span></span>

 <span data-ttu-id="e1428-109">Ses</span><span class="sxs-lookup"><span data-stu-id="e1428-109">Members</span></span>                        | <span data-ttu-id="e1428-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="e1428-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e1428-111">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="e1428-111">get_IsVisible</span></span>](#get_isvisible) | <span data-ttu-id="e1428-112">La propriété IsVisible détermine s’il faut afficher ou masquer le WebView.</span><span class="sxs-lookup"><span data-stu-id="e1428-112">The IsVisible property determines whether to show or hide the webview.</span></span>
[<span data-ttu-id="e1428-113">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="e1428-113">put_IsVisible</span></span>](#put_isvisible) | <span data-ttu-id="e1428-114">Définissez la propriété IsVisible.</span><span class="sxs-lookup"><span data-stu-id="e1428-114">Set the IsVisible property.</span></span>
[<span data-ttu-id="e1428-115">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="e1428-115">get_Bounds</span></span>](#get_bounds) | <span data-ttu-id="e1428-116">Les limites de l’affichage WebView.</span><span class="sxs-lookup"><span data-stu-id="e1428-116">The webview bounds.</span></span>
[<span data-ttu-id="e1428-117">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="e1428-117">put_Bounds</span></span>](#put_bounds) | <span data-ttu-id="e1428-118">Définissez la propriété Bounds.</span><span class="sxs-lookup"><span data-stu-id="e1428-118">Set the Bounds property.</span></span>
[<span data-ttu-id="e1428-119">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="e1428-119">get_ZoomFactor</span></span>](#get_zoomfactor) | <span data-ttu-id="e1428-120">Facteur de zoom pour le WebView.</span><span class="sxs-lookup"><span data-stu-id="e1428-120">The zoom factor for the WebView.</span></span>
[<span data-ttu-id="e1428-121">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="e1428-121">put_ZoomFactor</span></span>](#put_zoomfactor) | <span data-ttu-id="e1428-122">Définissez la propriété ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="e1428-122">Set the ZoomFactor property.</span></span>
[<span data-ttu-id="e1428-123">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="e1428-123">add_ZoomFactorChanged</span></span>](#add_zoomfactorchanged) | <span data-ttu-id="e1428-124">Ajoutez un gestionnaire d’événements pour l’événement ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="e1428-124">Add an event handler for the ZoomFactorChanged event.</span></span>
[<span data-ttu-id="e1428-125">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="e1428-125">remove_ZoomFactorChanged</span></span>](#remove_zoomfactorchanged) | <span data-ttu-id="e1428-126">Supprimez un gestionnaire d’événements préalablement ajouté à add_ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="e1428-126">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>
[<span data-ttu-id="e1428-127">SetBoundsAndZoomFactor</span><span class="sxs-lookup"><span data-stu-id="e1428-127">SetBoundsAndZoomFactor</span></span>](#setboundsandzoomfactor) | <span data-ttu-id="e1428-128">Mettez à jour les propriétés de limites et de ZoomFactor en même temps.</span><span class="sxs-lookup"><span data-stu-id="e1428-128">Update Bounds and ZoomFactor properties at the same time.</span></span>
[<span data-ttu-id="e1428-129">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="e1428-129">MoveFocus</span></span>](#movefocus) | <span data-ttu-id="e1428-130">Déplacer le focus sur le WebView.</span><span class="sxs-lookup"><span data-stu-id="e1428-130">Move focus into WebView.</span></span>
[<span data-ttu-id="e1428-131">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="e1428-131">add_MoveFocusRequested</span></span>](#add_movefocusrequested) | <span data-ttu-id="e1428-132">Ajoutez un gestionnaire d’événements pour l’événement MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="e1428-132">Add an event handler for the MoveFocusRequested event.</span></span>
[<span data-ttu-id="e1428-133">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="e1428-133">remove_MoveFocusRequested</span></span>](#remove_movefocusrequested) | <span data-ttu-id="e1428-134">Supprimez un gestionnaire d’événements préalablement ajouté à add_MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="e1428-134">Remove an event handler previously added with add_MoveFocusRequested.</span></span>
[<span data-ttu-id="e1428-135">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="e1428-135">add_GotFocus</span></span>](#add_gotfocus) | <span data-ttu-id="e1428-136">Ajoutez un gestionnaire d’événements pour l’événement GotFocus.</span><span class="sxs-lookup"><span data-stu-id="e1428-136">Add an event handler for the GotFocus event.</span></span>
[<span data-ttu-id="e1428-137">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="e1428-137">remove_GotFocus</span></span>](#remove_gotfocus) | <span data-ttu-id="e1428-138">Supprimez un gestionnaire d’événements préalablement ajouté à add_GotFocus.</span><span class="sxs-lookup"><span data-stu-id="e1428-138">Remove an event handler previously added with add_GotFocus.</span></span>
[<span data-ttu-id="e1428-139">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="e1428-139">add_LostFocus</span></span>](#add_lostfocus) | <span data-ttu-id="e1428-140">Ajoutez un gestionnaire d’événements pour l’événement LostFocus.</span><span class="sxs-lookup"><span data-stu-id="e1428-140">Add an event handler for the LostFocus event.</span></span>
[<span data-ttu-id="e1428-141">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="e1428-141">remove_LostFocus</span></span>](#remove_lostfocus) | <span data-ttu-id="e1428-142">Supprimez un gestionnaire d’événements préalablement ajouté à add_LostFocus.</span><span class="sxs-lookup"><span data-stu-id="e1428-142">Remove an event handler previously added with add_LostFocus.</span></span>
[<span data-ttu-id="e1428-143">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="e1428-143">add_AcceleratorKeyPressed</span></span>](#add_acceleratorkeypressed) | <span data-ttu-id="e1428-144">Ajoutez un gestionnaire d’événements pour l’événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="e1428-144">Add an event handler for the AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="e1428-145">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="e1428-145">remove_AcceleratorKeyPressed</span></span>](#remove_acceleratorkeypressed) | <span data-ttu-id="e1428-146">Supprimez un gestionnaire d’événements préalablement ajouté à add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="e1428-146">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>
[<span data-ttu-id="e1428-147">get_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="e1428-147">get_ParentWindow</span></span>](#get_parentwindow) | <span data-ttu-id="e1428-148">Fenêtre parent fournie par l’application utilisée par ce WebView pour afficher le contenu.</span><span class="sxs-lookup"><span data-stu-id="e1428-148">The parent window provided by the app that this WebView is using to render content.</span></span>
[<span data-ttu-id="e1428-149">put_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="e1428-149">put_ParentWindow</span></span>](#put_parentwindow) | <span data-ttu-id="e1428-150">Définissez la fenêtre parente pour le WebView.</span><span class="sxs-lookup"><span data-stu-id="e1428-150">Set the parent window for the WebView.</span></span>
[<span data-ttu-id="e1428-151">NotifyParentWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="e1428-151">NotifyParentWindowPositionChanged</span></span>](#notifyparentwindowpositionchanged) | <span data-ttu-id="e1428-152">Il s’agit d’une notification distincte de put_Bounds indiquant à WebView son parent (ou n’importe quel ancêtre) déplacé.</span><span class="sxs-lookup"><span data-stu-id="e1428-152">This is a notification separate from put_Bounds that tells WebView its parent (or any ancestor) HWND moved.</span></span>
[<span data-ttu-id="e1428-153">Fermer</span><span class="sxs-lookup"><span data-stu-id="e1428-153">Close</span></span>](#close) | <span data-ttu-id="e1428-154">Ferme le WebView et nettoie l’instance de navigateur sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="e1428-154">Closes the WebView and cleans up the underlying browser instance.</span></span>
[<span data-ttu-id="e1428-155">get_CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="e1428-155">get_CoreWebView2</span></span>](#get_corewebview2) | <span data-ttu-id="e1428-156">Obtient le CoreWebView2 associé à cet CoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="e1428-156">Gets the CoreWebView2 associated with this CoreWebView2Host.</span></span>
[<span data-ttu-id="e1428-157">CORE_WEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="e1428-157">CORE_WEBVIEW2_MOVE_FOCUS_REASON</span></span>](#core_webview2_move_focus_reason) | <span data-ttu-id="e1428-158">Raison du déplacement du focus.</span><span class="sxs-lookup"><span data-stu-id="e1428-158">Reason for moving focus.</span></span>
[<span data-ttu-id="e1428-159">CORE_WEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="e1428-159">CORE_WEBVIEW2_KEY_EVENT_KIND</span></span>](#core_webview2_key_event_kind) | <span data-ttu-id="e1428-160">Type d’événement de touche qui déclenchait un événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="e1428-160">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="e1428-161">CORE_WEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="e1428-161">CORE_WEBVIEW2_PHYSICAL_KEY_STATUS</span></span>](#core_webview2_physical_key_status) | <span data-ttu-id="e1428-162">Structure représentant les informations contenues dans le LPARAM fourni à un événement de touche Win32.</span><span class="sxs-lookup"><span data-stu-id="e1428-162">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

<span data-ttu-id="e1428-163">Le CoreWebView2Host possède CoreWebView2, et si toutes les références au CoreWebView2Host disparaissent, le WebView sera fermé.</span><span class="sxs-lookup"><span data-stu-id="e1428-163">The CoreWebView2Host owns the CoreWebView2, and if all references to the CoreWebView2Host go away, the WebView will be closed.</span></span>

## <span data-ttu-id="e1428-164">Ses</span><span class="sxs-lookup"><span data-stu-id="e1428-164">Members</span></span>

#### <span data-ttu-id="e1428-165">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="e1428-165">get_IsVisible</span></span> 

<span data-ttu-id="e1428-166">La propriété IsVisible détermine s’il faut afficher ou masquer le WebView.</span><span class="sxs-lookup"><span data-stu-id="e1428-166">The IsVisible property determines whether to show or hide the webview.</span></span>

> <span data-ttu-id="e1428-167">valeur publique HRESULT [get_IsVisible](#get_isvisible)(bool \* IsVisible)</span><span class="sxs-lookup"><span data-stu-id="e1428-167">public HRESULT [get_IsVisible](#get_isvisible)(BOOL \* isVisible)</span></span>

<span data-ttu-id="e1428-168">Si la valeur de l’argument IsVisible est définie sur false, le WebView sera transparent et ne sera pas affiché.</span><span class="sxs-lookup"><span data-stu-id="e1428-168">If IsVisible is set to false, the webview will be transparent and will not be rendered.</span></span> <span data-ttu-id="e1428-169">Toutefois, cela n’affecte pas la fenêtre qui contient le WebView (le paramètre HWND transmis à CreateCoreWebView2Host).</span><span class="sxs-lookup"><span data-stu-id="e1428-169">However, this will not affect the window containing the webview (the HWND parameter that was passed to CreateCoreWebView2Host).</span></span> <span data-ttu-id="e1428-170">Si vous souhaitez que cette fenêtre disparaisse également, appelez la fonction ShowWindow sur celle-ci directement en plus de modifier la propriété IsVisible.</span><span class="sxs-lookup"><span data-stu-id="e1428-170">If you want that window to disappear too, call ShowWindow on it directly in addition to modifying the IsVisible property.</span></span> <span data-ttu-id="e1428-171">Le mode webaffichage sous forme de fenêtre enfant ne recevra pas de messages de fenêtre lorsque la fenêtre supérieure est réduite ou restaurée.</span><span class="sxs-lookup"><span data-stu-id="e1428-171">WebView as a child window won't get window messages when the top window is minimized or restored.</span></span> <span data-ttu-id="e1428-172">Pour des raisons de performances, le développeur doit définir la propriété IsVisible du WebView sur false lorsque la fenêtre de l’application est réduite, puis revenir à la valeur true lorsque la fenêtre de l’application est restaurée.</span><span class="sxs-lookup"><span data-stu-id="e1428-172">For performance reason, developer should set IsVisible property of the WebView to false when the app window is minimized and back to true when app window is restored.</span></span> <span data-ttu-id="e1428-173">Pour cela, la fenêtre de l’application peut gérer les SC_MINIMIZE et de SC_RESTORE commande lors de la réception d’WM_SYSCOMMAND message.</span><span class="sxs-lookup"><span data-stu-id="e1428-173">App window can do this by handling SC_MINIMIZE and SC_RESTORE command upon receiving WM_SYSCOMMAND message.</span></span>

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_host->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_host->put_IsVisible(m_isVisible);
}
```

#### <span data-ttu-id="e1428-174">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="e1428-174">put_IsVisible</span></span> 

<span data-ttu-id="e1428-175">Définissez la propriété IsVisible.</span><span class="sxs-lookup"><span data-stu-id="e1428-175">Set the IsVisible property.</span></span>

> <span data-ttu-id="e1428-176">valeur HRESULT publique [put_IsVisible](#put_isvisible)(bool IsVisible)</span><span class="sxs-lookup"><span data-stu-id="e1428-176">public HRESULT [put_IsVisible](#put_isvisible)(BOOL isVisible)</span></span>

```cpp
    if (message == WM_SYSCOMMAND)
    {
        if (wParam == SC_MINIMIZE)
        {
            // Hide the webview when the app window is minimized.
            m_host->put_IsVisible(FALSE);
        }
        else if (wParam == SC_RESTORE)
        {
            // When the app window is restored, show the webview
            // (unless the user has toggle visibility off).
            if (m_isVisible)
            {
                m_host->put_IsVisible(TRUE);
            }
        }
    }
```

#### <span data-ttu-id="e1428-177">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="e1428-177">get_Bounds</span></span> 

<span data-ttu-id="e1428-178">Les limites de l’affichage WebView.</span><span class="sxs-lookup"><span data-stu-id="e1428-178">The webview bounds.</span></span>

> <span data-ttu-id="e1428-179">[get_Boundss](#get_bounds)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="e1428-179">public HRESULT [get_Bounds](#get_bounds)(RECT \* bounds)</span></span>

<span data-ttu-id="e1428-180">Les limites sont relatives au HWND parent.</span><span class="sxs-lookup"><span data-stu-id="e1428-180">Bounds are relative to the parent HWND.</span></span> <span data-ttu-id="e1428-181">L’application peut positionner un WebView de deux manières:</span><span class="sxs-lookup"><span data-stu-id="e1428-181">The app has two ways it can position a WebView:</span></span>

1. <span data-ttu-id="e1428-182">Créer un HWND enfant qui est le HWND parent WebView.</span><span class="sxs-lookup"><span data-stu-id="e1428-182">Create a child HWND that is the WebView parent HWND.</span></span> <span data-ttu-id="e1428-183">Positionnez cette fenêtre dans laquelle le WebView devrait être.</span><span class="sxs-lookup"><span data-stu-id="e1428-183">Position this window where the WebView should be.</span></span> <span data-ttu-id="e1428-184">Dans le cas présent, utilisez (0, 0) pour le coin supérieur gauche de la vue de Bound’s (offset).</span><span class="sxs-lookup"><span data-stu-id="e1428-184">In this case, use (0, 0) for the WebView's Bound's top left corner (the offset).</span></span>

1. <span data-ttu-id="e1428-185">Utilisez la plus grande fenêtre de l’application en tant que HWND parent d’affichage.</span><span class="sxs-lookup"><span data-stu-id="e1428-185">Use the app's top most window as the WebView parent HWND.</span></span> <span data-ttu-id="e1428-186">Définissez le coin supérieur gauche de l’Bound’s WebView de sorte que le contrôle WebView soit correctement positionné dans l’application.</span><span class="sxs-lookup"><span data-stu-id="e1428-186">Set the WebView's Bound's top left corner so that the WebView is positioned correctly in the app.</span></span> <span data-ttu-id="e1428-187">Les valeurs de limites se trouvent dans l’espace de coordonnées de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="e1428-187">The Bound's values are in the host's coordinate space.</span></span>

#### <span data-ttu-id="e1428-188">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="e1428-188">put_Bounds</span></span> 

<span data-ttu-id="e1428-189">Définissez la propriété Bounds.</span><span class="sxs-lookup"><span data-stu-id="e1428-189">Set the Bounds property.</span></span>

> <span data-ttu-id="e1428-190">[put_Bounds](#put_bounds)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="e1428-190">public HRESULT [put_Bounds](#put_bounds)(RECT bounds)</span></span>

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

    m_host->put_Bounds(desiredBounds);
}
```

#### <span data-ttu-id="e1428-191">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="e1428-191">get_ZoomFactor</span></span> 

<span data-ttu-id="e1428-192">Facteur de zoom pour le WebView.</span><span class="sxs-lookup"><span data-stu-id="e1428-192">The zoom factor for the WebView.</span></span>

> <span data-ttu-id="e1428-193">valeur publique HRESULT [get_ZoomFactor](#get_zoomfactor)(double \* ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="e1428-193">public HRESULT [get_ZoomFactor](#get_zoomfactor)(double \* zoomFactor)</span></span>

<span data-ttu-id="e1428-194">Notez que la modification du facteur de zoom peut entraîner la modification de la `window.innerWidth/innerHeight` mise en page.</span><span class="sxs-lookup"><span data-stu-id="e1428-194">Note that changing zoom factor could cause `window.innerWidth/innerHeight` and page layout to change.</span></span> <span data-ttu-id="e1428-195">Le facteur de zoom appliqué par l’hôte en appelant put_ZoomFactor devient le nouveau zoom par défaut de l’affichage WebView.</span><span class="sxs-lookup"><span data-stu-id="e1428-195">A zoom factor that is applied by the host by calling put_ZoomFactor becomes the new default zoom for the WebView.</span></span> <span data-ttu-id="e1428-196">Ce facteur de zoom s’applique aux différentes navigations et le facteur de zoom est renvoyé lorsque l’utilisateur appuie sur Ctrl + 0.</span><span class="sxs-lookup"><span data-stu-id="e1428-196">This zoom factor applies across navigations and is the zoom factor WebView is returned to when the user presses ctrl+0.</span></span> <span data-ttu-id="e1428-197">Lorsque le facteur de zoom est modifié par l’utilisateur (ce qui permet à l’application de recevoir ZoomFactorChanged), ce zoom s’applique uniquement à la page active.</span><span class="sxs-lookup"><span data-stu-id="e1428-197">When the zoom factor is changed by the user (resulting in the app receiving ZoomFactorChanged), that zoom applies only for the current page.</span></span> <span data-ttu-id="e1428-198">Tout zoom appliqué à un utilisateur est réservé uniquement à la page active et est réinitialisé sur une navigation.</span><span class="sxs-lookup"><span data-stu-id="e1428-198">Any user applied zoom is only for the current page and is reset on a navigation.</span></span> <span data-ttu-id="e1428-199">La spécification d’un zoomFactor inférieur ou égal à 0 n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="e1428-199">Specifying a zoomFactor less than or equal to 0 is not allowed.</span></span> <span data-ttu-id="e1428-200">WebView possède également une plage de facteur de zoom prise en charge interne.</span><span class="sxs-lookup"><span data-stu-id="e1428-200">WebView also has an internal supported zoom factor range.</span></span> <span data-ttu-id="e1428-201">Lorsque le facteur de zoom spécifié est en dehors de cette plage, il est normalisé pour être dans la plage et un événement ZoomFactorChanged est déclenché pour le facteur de zoom réel appliqué.</span><span class="sxs-lookup"><span data-stu-id="e1428-201">When a specified zoom factor is out of that range, it will be normalized to be within the range, and a ZoomFactorChanged event will be fired for the real applied zoom factor.</span></span> <span data-ttu-id="e1428-202">Lorsque cette situation se produit, la propriété ZoomFactor indique le facteur de zoom spécifié lors de la modification précédente de la propriété ZoomFactor jusqu’à ce que l’événement ZoomFactorChanged soit reçu lorsque WebView applique le facteur de zoom normalisé.</span><span class="sxs-lookup"><span data-stu-id="e1428-202">When this range normalization happens, the ZoomFactor property will report the zoom factor specified during the previous modification of the ZoomFactor property until the ZoomFactorChanged event is received after webview applies the normalized zoom factor.</span></span>

#### <span data-ttu-id="e1428-203">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="e1428-203">put_ZoomFactor</span></span> 

<span data-ttu-id="e1428-204">Définissez la propriété ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="e1428-204">Set the ZoomFactor property.</span></span>

> <span data-ttu-id="e1428-205">[put_ZoomFactor](#put_zoomfactor)par le biais du public HRESULT (double ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="e1428-205">public HRESULT [put_ZoomFactor](#put_zoomfactor)(double zoomFactor)</span></span>

#### <span data-ttu-id="e1428-206">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="e1428-206">add_ZoomFactorChanged</span></span> 

<span data-ttu-id="e1428-207">Ajoutez un gestionnaire d’événements pour l’événement ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="e1428-207">Add an event handler for the ZoomFactorChanged event.</span></span>

> <span data-ttu-id="e1428-208">[add_ZoomFactorChanged](#add_zoomfactorchanged)par le biais du[mot de passe](ICoreWebView2ZoomFactorChangedEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="e1428-208">public HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([ICoreWebView2ZoomFactorChangedEventHandler](ICoreWebView2ZoomFactorChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="e1428-209">L’événement se déclenche lorsque la propriété ZoomFactor de l’élément WebView change.</span><span class="sxs-lookup"><span data-stu-id="e1428-209">The event fires when the ZoomFactor property of the WebView changes.</span></span> <span data-ttu-id="e1428-210">L’événement peut être déclenché en raison du fait que l’appelant a modifié la propriété ZoomFactor, ou en raison de l’utilisateur modifiant manuellement le zoom.</span><span class="sxs-lookup"><span data-stu-id="e1428-210">The event could fire because the caller modified the ZoomFactor property, or due to the user manually modifying the zoom.</span></span> <span data-ttu-id="e1428-211">Lorsqu’il est modifié par l’appelant par le biais de la propriété ZoomFactor, le facteur de zoom interne est mis à jour immédiatement et il n’y a pas d’événement ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="e1428-211">When it is modified by the caller via the ZoomFactor property, the internal zoom factor is updated immediately and there will be no ZoomFactorChanged event.</span></span> <span data-ttu-id="e1428-212">WebView associe le dernier facteur de zoom utilisé pour chaque site.</span><span class="sxs-lookup"><span data-stu-id="e1428-212">WebView associates the last used zoom factor for each site.</span></span> <span data-ttu-id="e1428-213">Par conséquent, il est possible de modifier le facteur de zoom lorsque vous naviguez vers une autre page.</span><span class="sxs-lookup"><span data-stu-id="e1428-213">Therefore, it is possible for the zoom factor to change when navigating to a different page.</span></span> <span data-ttu-id="e1428-214">Lorsque le facteur de zoom change en raison de cela, l’événement ZoomFactorChanged se déclenche immédiatement après l’événement ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="e1428-214">When the zoom factor changes due to this, the ZoomFactorChanged event fires right after the ContentLoading event.</span></span>

```cpp
    // Register a handler for the ZoomFactorChanged event.
    // This handler just announces the new level of zoom on the window's title bar.
    CHECK_FAILURE(m_host->add_ZoomFactorChanged(
        Callback<ICoreWebView2ZoomFactorChangedEventHandler>(
            [this](ICoreWebView2Host* sender, IUnknown* args) -> HRESULT {
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

#### <span data-ttu-id="e1428-215">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="e1428-215">remove_ZoomFactorChanged</span></span> 

<span data-ttu-id="e1428-216">Supprimez un gestionnaire d’événements préalablement ajouté à add_ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="e1428-216">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>

> <span data-ttu-id="e1428-217">[remove_ZoomFactorChanged](#remove_zoomfactorchanged)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="e1428-217">public HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="e1428-218">SetBoundsAndZoomFactor</span><span class="sxs-lookup"><span data-stu-id="e1428-218">SetBoundsAndZoomFactor</span></span> 

<span data-ttu-id="e1428-219">Mettez à jour les propriétés de limites et de ZoomFactor en même temps.</span><span class="sxs-lookup"><span data-stu-id="e1428-219">Update Bounds and ZoomFactor properties at the same time.</span></span>

> <span data-ttu-id="e1428-220">public HRESULT [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(limites de Rect, double ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="e1428-220">public HRESULT [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(RECT bounds,double zoomFactor)</span></span>

<span data-ttu-id="e1428-221">Cette opération est atomique de l’application perspec de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="e1428-221">This operation is atomic from the host's perspecive.</span></span> <span data-ttu-id="e1428-222">Après avoir retourné la fonction, les limites et les propriétés ZoomFactor ont été mises à jour si la fonction est réussie, ou ne sont pas mises à jour en cas d’échec de la fonction.</span><span class="sxs-lookup"><span data-stu-id="e1428-222">After returning from this function, the Bounds and ZoomFactor properties will have both been updated if the function is successful, or neither will be updated if the function fails.</span></span> <span data-ttu-id="e1428-223">Si les limites et ZoomFactor sont toutes deux mises à jour par la même échelle (c’est-à-dire que les limites et ZoomFactor sont tous deux doublées), la page ne verra aucune modification apportée à Window. innerWidth/innerHeight et le WebView fera apparaître le contenu aux nouvelles tailles et zooms sans rendu intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="e1428-223">If Bounds and ZoomFactor are both updated by the same scale (i.e. Bounds and ZoomFactor are both doubled), then the page will not see a change in window.innerWidth/innerHeight and the WebView will render the content at the new size and zoom without intermediate renderings.</span></span> <span data-ttu-id="e1428-224">Cette fonction peut également être utilisée pour mettre à jour une seule de ZoomFactor ou de limites en passant la nouvelle valeur pour une et la valeur actuelle pour l’autre.</span><span class="sxs-lookup"><span data-stu-id="e1428-224">This function can also be used to update just one of ZoomFactor or Bounds by passing in the new value for one and the current value for the other.</span></span>

```cpp
void ViewComponent::SetScale(float scale)
{
    RECT bounds;
    CHECK_FAILURE(m_host->get_Bounds(&bounds));
    double scaleChange = scale / m_webViewScale;

    bounds.bottom = LONG(
        (bounds.bottom - bounds.top) * scaleChange + bounds.top);
    bounds.right = LONG(
        (bounds.right - bounds.left) * scaleChange + bounds.left);

    m_webViewScale = scale;
    m_host->SetBoundsAndZoomFactor(bounds, scale);
}
```

#### <span data-ttu-id="e1428-225">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="e1428-225">MoveFocus</span></span> 

<span data-ttu-id="e1428-226">Déplacer le focus sur le WebView.</span><span class="sxs-lookup"><span data-stu-id="e1428-226">Move focus into WebView.</span></span>

> <span data-ttu-id="e1428-227">public HRESULT [MoveFocus](#movefocus)([CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason) raison)</span><span class="sxs-lookup"><span data-stu-id="e1428-227">public HRESULT [MoveFocus](#movefocus)([CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason) reason)</span></span>

<span data-ttu-id="e1428-228">WebView va mettre le focus et le focus sur l’élément correspondant dans la page hébergée dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="e1428-228">WebView will get focus and focus will be set to correspondent element in the page hosted in the WebView.</span></span> <span data-ttu-id="e1428-229">Pour des raisons de programmation, le focus est défini sur l’élément précédemment prioritaire ou l’élément par défaut s’il n’y a pas d’élément prioritaire auparavant.</span><span class="sxs-lookup"><span data-stu-id="e1428-229">For Programmatic reason, focus is set to previously focused element or the default element if there is no previously focused element.</span></span> <span data-ttu-id="e1428-230">Pour une raison suivante, le focus est défini sur le premier élément.</span><span class="sxs-lookup"><span data-stu-id="e1428-230">For Next reason, focus is set to the first element.</span></span> <span data-ttu-id="e1428-231">Pour une raison précédente, le focus est défini sur le dernier élément.</span><span class="sxs-lookup"><span data-stu-id="e1428-231">For Previous reason, focus is set to the last element.</span></span> <span data-ttu-id="e1428-232">Le mode webaffichage peut également mettre le focus sur une interaction utilisateur telle que cliquer sur le WebView ou sur Tab.</span><span class="sxs-lookup"><span data-stu-id="e1428-232">WebView can also got focus through user interaction like clicking into WebView or Tab into it.</span></span> <span data-ttu-id="e1428-233">Pour la fonction de tabulation, l’application peut appeler MoveFocus avec Next ou Previous pour s’aligner sur TAB et Maj + Tab lorsqu’elle décide que le WebView est l’élément tabbable suivant.</span><span class="sxs-lookup"><span data-stu-id="e1428-233">For tabbing, the app can call MoveFocus with Next or Previous to align with tab and shift+tab respectively when it decides the WebView is the next tabbable element.</span></span> <span data-ttu-id="e1428-234">Par exemple, l’application peut appeler IsDialogMessage dans le cadre de sa boucle de messages pour permettre à la plateforme de gérer automatiquement la tabulation.</span><span class="sxs-lookup"><span data-stu-id="e1428-234">Or, the app can call IsDialogMessage as part of its message loop to allow the platform to auto handle tabbing.</span></span> <span data-ttu-id="e1428-235">La plateforme est pivotée sur toutes les fenêtres avec WS_TABSTOP.</span><span class="sxs-lookup"><span data-stu-id="e1428-235">The platform will rotate through all windows with WS_TABSTOP.</span></span> <span data-ttu-id="e1428-236">Lorsque le WebView obtient le focus de IsDialogMessage, il positionne en interne le focus sur le premier ou le dernier élément de Tab et Maj + Tab respectivement.</span><span class="sxs-lookup"><span data-stu-id="e1428-236">When the WebView gets focus from IsDialogMessage, it will internally put the focus on the first or last element for tab and shift+tab respectively.</span></span>

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
            for (int i = 0; i < m_tabbableWindows.size(); i++)
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
    for (int i = currentIndex + 1; i < m_tabbableWindows.size(); i++)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    m_host->MoveFocus(CORE_WEBVIEW2_MOVE_FOCUS_REASON_NEXT);
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
    CHECK_FAILURE(m_host->MoveFocus(CORE_WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS));
}
```

#### <span data-ttu-id="e1428-237">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="e1428-237">add_MoveFocusRequested</span></span> 

<span data-ttu-id="e1428-238">Ajoutez un gestionnaire d’événements pour l’événement MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="e1428-238">Add an event handler for the MoveFocusRequested event.</span></span>

> <span data-ttu-id="e1428-239">[add_MoveFocusRequested](#add_movefocusrequested)par le biais du[mot de passe](ICoreWebView2MoveFocusRequestedEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="e1428-239">public HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([ICoreWebView2MoveFocusRequestedEventHandler](ICoreWebView2MoveFocusRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="e1428-240">MoveFocusRequested est déclenché lorsque l’utilisateur tente d’accéder à l’onglet du WebView.</span><span class="sxs-lookup"><span data-stu-id="e1428-240">MoveFocusRequested fires when user tries to tab out of the WebView.</span></span> <span data-ttu-id="e1428-241">Le focus du WebView n’a pas changé lors du déclenchement de cet événement.</span><span class="sxs-lookup"><span data-stu-id="e1428-241">The WebView's focus has not changed when this event is fired.</span></span>

```cpp
    // Register a handler for the MoveFocusRequested event.
    // This event will be fired when the user tabs out of the webview.
    // The handler will focus another window in the app, depending on which
    // direction the focus is being shifted.
    CHECK_FAILURE(m_host->add_MoveFocusRequested(
        Callback<ICoreWebView2MoveFocusRequestedEventHandler>(
            [this](
                ICoreWebView2Host* sender,
                ICoreWebView2MoveFocusRequestedEventArgs* args) -> HRESULT {
                if (!g_autoTabHandle)
                {
                    CORE_WEBVIEW2_MOVE_FOCUS_REASON reason;
                    CHECK_FAILURE(args->get_Reason(&reason));

                    if (reason == CORE_WEBVIEW2_MOVE_FOCUS_REASON_NEXT)
                    {
                        TabForwards(-1);
                    }
                    else if (reason == CORE_WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS)
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

#### <span data-ttu-id="e1428-242">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="e1428-242">remove_MoveFocusRequested</span></span> 

<span data-ttu-id="e1428-243">Supprimez un gestionnaire d’événements préalablement ajouté à add_MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="e1428-243">Remove an event handler previously added with add_MoveFocusRequested.</span></span>

> <span data-ttu-id="e1428-244">[remove_MoveFocusRequested](#remove_movefocusrequested)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="e1428-244">public HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="e1428-245">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="e1428-245">add_GotFocus</span></span> 

<span data-ttu-id="e1428-246">Ajoutez un gestionnaire d’événements pour l’événement GotFocus.</span><span class="sxs-lookup"><span data-stu-id="e1428-246">Add an event handler for the GotFocus event.</span></span>

> <span data-ttu-id="e1428-247">[add_GotFocus](#add_gotfocus)par le biais du[mot de passe](ICoreWebView2FocusChangedEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="e1428-247">public HRESULT [add_GotFocus](#add_gotfocus)([ICoreWebView2FocusChangedEventHandler](ICoreWebView2FocusChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="e1428-248">GotFocus se déclenche lorsque WebView a le focus.</span><span class="sxs-lookup"><span data-stu-id="e1428-248">GotFocus fires when WebView got focus.</span></span>

#### <span data-ttu-id="e1428-249">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="e1428-249">remove_GotFocus</span></span> 

<span data-ttu-id="e1428-250">Supprimez un gestionnaire d’événements préalablement ajouté à add_GotFocus.</span><span class="sxs-lookup"><span data-stu-id="e1428-250">Remove an event handler previously added with add_GotFocus.</span></span>

> <span data-ttu-id="e1428-251">[remove_GotFocus](#remove_gotfocus)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="e1428-251">public HRESULT [remove_GotFocus](#remove_gotfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="e1428-252">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="e1428-252">add_LostFocus</span></span> 

<span data-ttu-id="e1428-253">Ajoutez un gestionnaire d’événements pour l’événement LostFocus.</span><span class="sxs-lookup"><span data-stu-id="e1428-253">Add an event handler for the LostFocus event.</span></span>

> <span data-ttu-id="e1428-254">[add_LostFocus](#add_lostfocus)par le biais du[mot de passe](ICoreWebView2FocusChangedEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="e1428-254">public HRESULT [add_LostFocus](#add_lostfocus)([ICoreWebView2FocusChangedEventHandler](ICoreWebView2FocusChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="e1428-255">LostFocus se déclenche lorsque WebView perd le focus.</span><span class="sxs-lookup"><span data-stu-id="e1428-255">LostFocus fires when WebView lost focus.</span></span> <span data-ttu-id="e1428-256">Dans le cas où l’événement MoveFocusRequested est déclenché, le focus est toujours sur le WebView lors du déclenchement de l’événement MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="e1428-256">In the case where MoveFocusRequested event is fired, the focus is still on WebView when MoveFocusRequested event fires.</span></span> <span data-ttu-id="e1428-257">Le focus perdu ne se déclenche que lorsque le code de l’application ou l’action par défaut de l’événement MoveFocusRequested a défini le focus hors du WebView.</span><span class="sxs-lookup"><span data-stu-id="e1428-257">Lost focus only fires afterwards when app's code or default action of MoveFocusRequested event set focus away from WebView.</span></span>

#### <span data-ttu-id="e1428-258">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="e1428-258">remove_LostFocus</span></span> 

<span data-ttu-id="e1428-259">Supprimez un gestionnaire d’événements préalablement ajouté à add_LostFocus.</span><span class="sxs-lookup"><span data-stu-id="e1428-259">Remove an event handler previously added with add_LostFocus.</span></span>

> <span data-ttu-id="e1428-260">[remove_LostFocus](#remove_lostfocus)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="e1428-260">public HRESULT [remove_LostFocus](#remove_lostfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="e1428-261">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="e1428-261">add_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="e1428-262">Ajoutez un gestionnaire d’événements pour l’événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="e1428-262">Add an event handler for the AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="e1428-263">[add_AcceleratorKeyPressed](#add_acceleratorkeypressed)par le biais du[mot de passe](ICoreWebView2AcceleratorKeyPressedEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="e1428-263">public HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([ICoreWebView2AcceleratorKeyPressedEventHandler](ICoreWebView2AcceleratorKeyPressedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="e1428-264">AcceleratorKeyPressed se déclenche quand une touche d’accès rapide ou une touche de raccourci est enfoncée ou relâche lorsque le WebView est ciblé.</span><span class="sxs-lookup"><span data-stu-id="e1428-264">AcceleratorKeyPressed fires when an accelerator key or key combo is pressed or released while the WebView is focused.</span></span> <span data-ttu-id="e1428-265">Un raccourci est considéré comme un accélérateur s’il s’agit de l’un des éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="e1428-265">A key is considered an accelerator if either:</span></span>

1. <span data-ttu-id="e1428-266">Ctrl ou Alt est en cours de conservation ou</span><span class="sxs-lookup"><span data-stu-id="e1428-266">Ctrl or Alt is currently being held, or</span></span>

1. <span data-ttu-id="e1428-267">la touche appuyée ne correspond pas à un caractère.</span><span class="sxs-lookup"><span data-stu-id="e1428-267">the pressed key does not map to a character.</span></span> <span data-ttu-id="e1428-268">Quelques touches spécifiques ne sont jamais considérées comme des accélérateurs, comme Shift.</span><span class="sxs-lookup"><span data-stu-id="e1428-268">A few specific keys are never considered accelerators, such as Shift.</span></span> <span data-ttu-id="e1428-269">La touche Échap est toujours considérée comme un accélérateur.</span><span class="sxs-lookup"><span data-stu-id="e1428-269">The Escape key is always considered an accelerator.</span></span>

<span data-ttu-id="e1428-270">Les événements de touches répétées déclenchés suite à la fermeture de la clé entraînent également le déclenchement de cet événement.</span><span class="sxs-lookup"><span data-stu-id="e1428-270">Autorepeated key events caused by holding the key down will also fire this event.</span></span> <span data-ttu-id="e1428-271">Vous pouvez les filtrer en vérifiant les arguments d’événements «KeyEventLParam ou PhysicalKeyStatus.</span><span class="sxs-lookup"><span data-stu-id="e1428-271">You can filter these out by checking the event args' KeyEventLParam or PhysicalKeyStatus.</span></span>

<span data-ttu-id="e1428-272">En mode fenêtre, ce gestionnaire d’événements est appelé de manière synchrone.</span><span class="sxs-lookup"><span data-stu-id="e1428-272">In windowed mode, this event handler is called synchronously.</span></span> <span data-ttu-id="e1428-273">Tant que vous n’avez pas appelé handle () sur les arguments d’événement ou que le gestionnaire d’événements renvoie, le processus de navigateur sera bloqué et les appels COM entre processus entrants échoueront avec RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span><span class="sxs-lookup"><span data-stu-id="e1428-273">Until you call Handle() on the event args or the event handler returns, the browser process will be blocked and outgoing cross-process COM calls will fail with RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span></span> <span data-ttu-id="e1428-274">Toutes les méthodes de l’API CoreWebView2 fonctionneront toutefois.</span><span class="sxs-lookup"><span data-stu-id="e1428-274">All CoreWebView2 API methods will work, however.</span></span>

<span data-ttu-id="e1428-275">En mode sans fenêtre, le gestionnaire d’événements est appelé de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e1428-275">In windowless mode, the event handler is called asynchronously.</span></span> <span data-ttu-id="e1428-276">L’entrée supplémentaire n’atteint pas le navigateur tant que le gestionnaire d’événements n’a pas renvoyé ou que le gestionnaire d’événements n’est pas appelé, mais que le processus du navigateur proprement dit ne sera pas bloqué et que les appels COM sortants fonctionneront normalement.</span><span class="sxs-lookup"><span data-stu-id="e1428-276">Further input will not reach the browser until the event handler returns or Handle() is called, but the browser process itself will not be blocked, and outgoing COM calls will work normally.</span></span>

<span data-ttu-id="e1428-277">Il est recommandé d’appeler handle (vrai) dès que vous en savez que vous voulez gérer la touche accélérateur.</span><span class="sxs-lookup"><span data-stu-id="e1428-277">It is recommended to call Handle(TRUE) as early as you can know that you want to handle the accelerator key.</span></span>

```cpp
    // Register a handler for the AcceleratorKeyPressed event.
    CHECK_FAILURE(m_host->add_AcceleratorKeyPressed(
        Callback<ICoreWebView2AcceleratorKeyPressedEventHandler>(
            [this](
                ICoreWebView2Host* sender,
                ICoreWebView2AcceleratorKeyPressedEventArgs* args) -> HRESULT {
                CORE_WEBVIEW2_KEY_EVENT_KIND kind;
                CHECK_FAILURE(args->get_KeyEventKind(&kind));
                // We only care about key down events.
                if (kind == CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_DOWN ||
                    kind == CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN)
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
                        CORE_WEBVIEW2_PHYSICAL_KEY_STATUS status;
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

#### <span data-ttu-id="e1428-278">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="e1428-278">remove_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="e1428-279">Supprimez un gestionnaire d’événements préalablement ajouté à add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="e1428-279">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>

> <span data-ttu-id="e1428-280">[remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="e1428-280">public HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="e1428-281">get_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="e1428-281">get_ParentWindow</span></span> 

<span data-ttu-id="e1428-282">Fenêtre parent fournie par l’application utilisée par ce WebView pour afficher le contenu.</span><span class="sxs-lookup"><span data-stu-id="e1428-282">The parent window provided by the app that this WebView is using to render content.</span></span>

> <span data-ttu-id="e1428-283">valeur publique HRESULT [get_ParentWindow](#get_parentwindow)(HWND \* topLevelWindow)</span><span class="sxs-lookup"><span data-stu-id="e1428-283">public HRESULT [get_ParentWindow](#get_parentwindow)(HWND \* topLevelWindow)</span></span>

<span data-ttu-id="e1428-284">Cette API renvoie initialement la fenêtre transmise à CreateCoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="e1428-284">This API initially returns the window passed into CreateCoreWebView2Host.</span></span>

#### <span data-ttu-id="e1428-285">put_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="e1428-285">put_ParentWindow</span></span> 

<span data-ttu-id="e1428-286">Définissez la fenêtre parente pour le WebView.</span><span class="sxs-lookup"><span data-stu-id="e1428-286">Set the parent window for the WebView.</span></span>

> <span data-ttu-id="e1428-287">[put_ParentWindow](#put_parentwindow)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="e1428-287">public HRESULT [put_ParentWindow](#put_parentwindow)(HWND topLevelWindow)</span></span>

<span data-ttu-id="e1428-288">Cela a pour effet de refaire de la fenêtre de l’affichage de nouveau dans la fenêtre qui vient d’être fournie.</span><span class="sxs-lookup"><span data-stu-id="e1428-288">This will cause the WebView to reparent its window to the newly provided window.</span></span>

#### <span data-ttu-id="e1428-289">NotifyParentWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="e1428-289">NotifyParentWindowPositionChanged</span></span> 

<span data-ttu-id="e1428-290">Il s’agit d’une notification distincte de put_Bounds indiquant à WebView son parent (ou n’importe quel ancêtre) déplacé.</span><span class="sxs-lookup"><span data-stu-id="e1428-290">This is a notification separate from put_Bounds that tells WebView its parent (or any ancestor) HWND moved.</span></span>

> <span data-ttu-id="e1428-291">public HRESULT [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()</span><span class="sxs-lookup"><span data-stu-id="e1428-291">public HRESULT [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()</span></span>

<span data-ttu-id="e1428-292">Cela est nécessaire pour l’accessibilité et certaines boîtes de dialogue dans WebView pour fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="e1428-292">This is needed for accessibility and certain dialogs in WebView to work correctly.</span></span> 

```cpp
    if (message == WM_MOVE || message == WM_MOVING)
    {
        m_host->NotifyParentWindowPositionChanged();
        return true;
    }
```

#### <span data-ttu-id="e1428-293">Fermer</span><span class="sxs-lookup"><span data-stu-id="e1428-293">Close</span></span> 

<span data-ttu-id="e1428-294">Ferme le WebView et nettoie l’instance de navigateur sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="e1428-294">Closes the WebView and cleans up the underlying browser instance.</span></span>

> <span data-ttu-id="e1428-295">valeur publique [HRESULT (](#close))</span><span class="sxs-lookup"><span data-stu-id="e1428-295">public HRESULT [Close](#close)()</span></span>

<span data-ttu-id="e1428-296">Le nettoyage de l’option de suppression de navigateur entraîne la mise à jour des ressources par le biais du WebView.</span><span class="sxs-lookup"><span data-stu-id="e1428-296">Cleaning up the browser instace will release the resources powering the WebView.</span></span> <span data-ttu-id="e1428-297">L’instance du navigateur sera arrêtée s’il n’y a aucune autre WebView.</span><span class="sxs-lookup"><span data-stu-id="e1428-297">The browser instance will be shut down if there are no other WebViews using it.</span></span>

<span data-ttu-id="e1428-298">Après avoir appelé Close, tous les appels de méthode échouent et les gestionnaires d’événements cessent de se déclencher.</span><span class="sxs-lookup"><span data-stu-id="e1428-298">After calling Close, all method calls will fail and event handlers will stop firing.</span></span> <span data-ttu-id="e1428-299">Plus précisément, le WebView publie ses références à ses gestionnaires d’événements lorsque la méthode Close est appelée.</span><span class="sxs-lookup"><span data-stu-id="e1428-299">Specifically, the WebView will release its references to its event handlers when Close is called.</span></span>

<span data-ttu-id="e1428-300">Close est appelé implicitement lorsque CoreWebView2Host perd sa référence finale et est détruit.</span><span class="sxs-lookup"><span data-stu-id="e1428-300">Close is implicitly called when the CoreWebView2Host loses its final reference and is destructed.</span></span> <span data-ttu-id="e1428-301">Mais il est conseillé d’appeler explicitement Close pour éviter tout cycle accidentel de références entre le WebView et le code de l’application.</span><span class="sxs-lookup"><span data-stu-id="e1428-301">But it is best practice to explicitly call Close to avoid any accidental cycle of references between the WebView and the app code.</span></span> <span data-ttu-id="e1428-302">En particulier, si vous capturez une référence à WebView dans un gestionnaire d’événements, vous créerez un cycle de référence entre le WebView et le gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="e1428-302">Specifically, if you capture a reference to the WebView in an event handler you will create a reference cycle between the WebView and the event handler.</span></span> <span data-ttu-id="e1428-303">L’appel de la fermeture rompt ce cycle en libérant tous les gestionnaires d’événements.</span><span class="sxs-lookup"><span data-stu-id="e1428-303">Calling Close will break this cycle by releasing all event handlers.</span></span> <span data-ttu-id="e1428-304">Néanmoins, pour éviter ce problème, il est préférable d’appeler explicitement l’application WebView et de ne pas capturer de référence à WebView pour s’assurer que le WebView peut être nettoyé correctement.</span><span class="sxs-lookup"><span data-stu-id="e1428-304">But to avoid this situation it is best practice both to explicitly call Close on the WebView and to not capture a reference to the WebView to ensure the WebView can be cleaned up correctly.</span></span>

```cpp
// Close the WebView and deinitialize related state. This doesn't close the app window.
void AppWindow::CloseWebView(bool cleanupUserDataFolder)
{
    DeleteAllComponents();
    if (m_host)
    {
        m_host->Close();
        m_host = nullptr;
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
        // https://docs.microsoft.com/microsoft-edge/hosting/webview2/reference/win32/0-9-488/webview2.idl#createwebview2environmentwithdetails
        WCHAR userDataFolder[MAX_PATH] = L"";
        // Obtain the absolute path for relative paths that include "./" or "../"
        _wfullpath(
            userDataFolder, GetLocalPath(L"WebView2APISample.exe.WebView2").c_str(), MAX_PATH);
        std::wstring userDataFolderPath(userDataFolder);

        std::wstring message = L"Are you sure you want to clean up the user data folder at\n";
        message += userDataFolderPath;
        message += L"\n?\nWarning: This action is not reversible.\n\n";
        message += L"Click No if there are other open WebView instnaces.\n";

        if (MessageBox(m_mainWindow, message.c_str(), L"Cleanup User Data Folder", MB_YESNO) ==
            IDYES)
        {
            CHECK_FAILURE(DeleteFileRecursive(userDataFolderPath));
        }
    }
}
```

#### <span data-ttu-id="e1428-305">get_CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="e1428-305">get_CoreWebView2</span></span> 

<span data-ttu-id="e1428-306">Obtient le CoreWebView2 associé à cet CoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="e1428-306">Gets the CoreWebView2 associated with this CoreWebView2Host.</span></span>

> <span data-ttu-id="e1428-307">[get_CoreWebView2](#get_corewebview2)par le biais du public HRESULT ([ICoreWebView2](ICoreWebView2.md) \* \* CoreWebView2)</span><span class="sxs-lookup"><span data-stu-id="e1428-307">public HRESULT [get_CoreWebView2](#get_corewebview2)([ICoreWebView2](ICoreWebView2.md) \*\* coreWebView2)</span></span>

#### <span data-ttu-id="e1428-308">CORE_WEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="e1428-308">CORE_WEBVIEW2_MOVE_FOCUS_REASON</span></span> 

<span data-ttu-id="e1428-309">Raison du déplacement du focus.</span><span class="sxs-lookup"><span data-stu-id="e1428-309">Reason for moving focus.</span></span>

> <span data-ttu-id="e1428-310">énumération [CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason)</span><span class="sxs-lookup"><span data-stu-id="e1428-310">enum [CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason)</span></span>

 <span data-ttu-id="e1428-311">Doubl</span><span class="sxs-lookup"><span data-stu-id="e1428-311">Values</span></span>                         | <span data-ttu-id="e1428-312">Descriptions</span><span class="sxs-lookup"><span data-stu-id="e1428-312">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="e1428-313">CORE_WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span><span class="sxs-lookup"><span data-stu-id="e1428-313">CORE_WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span></span>            | <span data-ttu-id="e1428-314">Paramètre de code axé sur le WebView.</span><span class="sxs-lookup"><span data-stu-id="e1428-314">Code setting focus into WebView.</span></span>
<span data-ttu-id="e1428-315">CORE_WEBVIEW2_MOVE_FOCUS_REASON_NEXT</span><span class="sxs-lookup"><span data-stu-id="e1428-315">CORE_WEBVIEW2_MOVE_FOCUS_REASON_NEXT</span></span>            | <span data-ttu-id="e1428-316">Déplacement du focus en raison d’une touche Tab.</span><span class="sxs-lookup"><span data-stu-id="e1428-316">Moving focus due to Tab traversal forward.</span></span>
<span data-ttu-id="e1428-317">CORE_WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span><span class="sxs-lookup"><span data-stu-id="e1428-317">CORE_WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span></span>            | <span data-ttu-id="e1428-318">Déplacement du focus en partant du haut de l’onglet.</span><span class="sxs-lookup"><span data-stu-id="e1428-318">Moving focus due to Tab traversal backward.</span></span>

#### <span data-ttu-id="e1428-319">CORE_WEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="e1428-319">CORE_WEBVIEW2_KEY_EVENT_KIND</span></span> 

<span data-ttu-id="e1428-320">Type d’événement de touche qui déclenchait un événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="e1428-320">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="e1428-321">énumération [CORE_WEBVIEW2_KEY_EVENT_KIND](#core_webview2_key_event_kind)</span><span class="sxs-lookup"><span data-stu-id="e1428-321">enum [CORE_WEBVIEW2_KEY_EVENT_KIND](#core_webview2_key_event_kind)</span></span>

 <span data-ttu-id="e1428-322">Doubl</span><span class="sxs-lookup"><span data-stu-id="e1428-322">Values</span></span>                         | <span data-ttu-id="e1428-323">Descriptions</span><span class="sxs-lookup"><span data-stu-id="e1428-323">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="e1428-324">CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="e1428-324">CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span></span>            | <span data-ttu-id="e1428-325">Correspond à WM_KEYDOWN de messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e1428-325">Correspond to window message WM_KEYDOWN.</span></span>
<span data-ttu-id="e1428-326">CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="e1428-326">CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_UP</span></span>            | <span data-ttu-id="e1428-327">Correspond à WM_KEYUP de messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e1428-327">Correspond to window message WM_KEYUP.</span></span>
<span data-ttu-id="e1428-328">CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="e1428-328">CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span></span>            | <span data-ttu-id="e1428-329">Correspond à WM_SYSKEYDOWN de messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e1428-329">Correspond to window message WM_SYSKEYDOWN.</span></span>
<span data-ttu-id="e1428-330">CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="e1428-330">CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span></span>            | <span data-ttu-id="e1428-331">Correspond à WM_SYSKEYUP de messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e1428-331">Correspond to window message WM_SYSKEYUP.</span></span>

#### <span data-ttu-id="e1428-332">CORE_WEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="e1428-332">CORE_WEBVIEW2_PHYSICAL_KEY_STATUS</span></span> 

<span data-ttu-id="e1428-333">Structure représentant les informations contenues dans le LPARAM fourni à un événement de touche Win32.</span><span class="sxs-lookup"><span data-stu-id="e1428-333">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

> <span data-ttu-id="e1428-334">[CORE_WEBVIEW2_PHYSICAL_KEY_STATUS](#core_webview2_physical_key_status) typedef</span><span class="sxs-lookup"><span data-stu-id="e1428-334">typedef [CORE_WEBVIEW2_PHYSICAL_KEY_STATUS](#core_webview2_physical_key_status)</span></span>

<span data-ttu-id="e1428-335">Pour plus d’informations, consultez la documentation de WM_KEYDOWN[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span><span class="sxs-lookup"><span data-stu-id="e1428-335">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span></span>

