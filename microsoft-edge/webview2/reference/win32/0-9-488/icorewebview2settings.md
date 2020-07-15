---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: a996660bb667ca0e556326e0bf2b71c15b9344c2
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880331"
---
# <span data-ttu-id="f1017-104">0.9.515-interface ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="f1017-104">0.9.515 - interface ICoreWebView2Settings</span></span> 

> [!NOTE]
> <span data-ttu-id="f1017-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="f1017-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="f1017-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="f1017-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Settings
  : public IUnknown
```

<span data-ttu-id="f1017-107">Définit les propriétés permettant, de désactiver ou de modifier les fonctionnalités WebView.</span><span class="sxs-lookup"><span data-stu-id="f1017-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="f1017-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="f1017-108">Summary</span></span>

 <span data-ttu-id="f1017-109">Ses</span><span class="sxs-lookup"><span data-stu-id="f1017-109">Members</span></span>                        | <span data-ttu-id="f1017-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="f1017-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f1017-111">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-111">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="f1017-112">La propriété AreDefaultContextMenusEnabled est utilisée pour empêcher l’affichage des menus contextuels par défaut pour les utilisateurs dans WebView.</span><span class="sxs-lookup"><span data-stu-id="f1017-112">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="f1017-113">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-113">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="f1017-114">AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="f1017-114">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="f1017-115">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-115">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="f1017-116">AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="f1017-116">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="f1017-117">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="f1017-117">get_AreRemoteObjectsAllowed</span></span>](#get_areremoteobjectsallowed) | <span data-ttu-id="f1017-118">La propriété AreRemoteObjectsAllowed est utilisée pour contrôler si les objets hôtes sont accessibles à partir de la page dans WebView.</span><span class="sxs-lookup"><span data-stu-id="f1017-118">The AreRemoteObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="f1017-119">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-119">get_IsBuiltInErrorPageEnabled</span></span>](#get_isbuiltinerrorpageenabled) | <span data-ttu-id="f1017-120">La propriété IsBuiltInErrorPageEnabled est utilisée pour désactiver la page d’erreur intégrée à un échec de navigation et un échec de processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="f1017-120">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="f1017-121">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-121">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="f1017-122">Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.</span><span class="sxs-lookup"><span data-stu-id="f1017-122">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="f1017-123">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-123">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="f1017-124">IsStatusBarEnabled vérifie si la barre d’État s’affiche.</span><span class="sxs-lookup"><span data-stu-id="f1017-124">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="f1017-125">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-125">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="f1017-126">La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="f1017-126">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="f1017-127">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-127">get_IsZoomControlEnabled</span></span>](#get_iszoomcontrolenabled) | <span data-ttu-id="f1017-128">La propriété IsZoomControlEnabled est utilisée pour empêcher l’utilisateur d’influer sur le zoom du WebView.</span><span class="sxs-lookup"><span data-stu-id="f1017-128">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>
[<span data-ttu-id="f1017-129">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-129">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="f1017-130">Définissez la propriété AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="f1017-130">Set the AreDefaultContextMenusEnabled property.</span></span>
[<span data-ttu-id="f1017-131">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-131">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="f1017-132">Définissez la propriété AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="f1017-132">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="f1017-133">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-133">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="f1017-134">Définissez la propriété AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="f1017-134">Set the AreDevToolsEnabled property.</span></span>
[<span data-ttu-id="f1017-135">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="f1017-135">put_AreRemoteObjectsAllowed</span></span>](#put_areremoteobjectsallowed) | <span data-ttu-id="f1017-136">Définissez la propriété AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="f1017-136">Set the AreRemoteObjectsAllowed property.</span></span>
[<span data-ttu-id="f1017-137">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-137">put_IsBuiltInErrorPageEnabled</span></span>](#put_isbuiltinerrorpageenabled) | <span data-ttu-id="f1017-138">Définissez la propriété IsBuiltInErrorPageEnabled.</span><span class="sxs-lookup"><span data-stu-id="f1017-138">Set the IsBuiltInErrorPageEnabled property.</span></span>
[<span data-ttu-id="f1017-139">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-139">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="f1017-140">Définissez la propriété IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="f1017-140">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="f1017-141">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-141">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="f1017-142">Définissez la propriété IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="f1017-142">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="f1017-143">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-143">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="f1017-144">Définissez la propriété IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="f1017-144">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="f1017-145">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-145">put_IsZoomControlEnabled</span></span>](#put_iszoomcontrolenabled) | <span data-ttu-id="f1017-146">Définissez la propriété IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="f1017-146">Set the IsZoomControlEnabled property.</span></span>

<span data-ttu-id="f1017-147">Les modifications apportées après l’événement NavigationStarting ne s’appliquent pas tant que la navigation de niveau supérieur suivante n’est pas appliquée.</span><span class="sxs-lookup"><span data-stu-id="f1017-147">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="f1017-148">Ses</span><span class="sxs-lookup"><span data-stu-id="f1017-148">Members</span></span>

#### <span data-ttu-id="f1017-149">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-149">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="f1017-150">La propriété AreDefaultContextMenusEnabled est utilisée pour empêcher l’affichage des menus contextuels par défaut pour les utilisateurs dans WebView.</span><span class="sxs-lookup"><span data-stu-id="f1017-150">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="f1017-151">[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)publique HRESULT (bool \* activé)</span><span class="sxs-lookup"><span data-stu-id="f1017-151">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="f1017-152">Par défaut, la valeur est TRUE.</span><span class="sxs-lookup"><span data-stu-id="f1017-152">Defaults to TRUE.</span></span>

```cpp
            BOOL allowContextMenus;
            CHECK_FAILURE(m_settings->get_AreDefaultContextMenusEnabled(
                &allowContextMenus));
            if (allowContextMenus) {
                CHECK_FAILURE(m_settings->put_AreDefaultContextMenusEnabled(FALSE));
                MessageBox(nullptr,
                L"Context menus will be disabled after the next navigation.",
                L"Settings change", MB_OK);
            }
            else {
                CHECK_FAILURE(m_settings->put_AreDefaultContextMenusEnabled(TRUE));
                MessageBox(nullptr,
                    L"Context menus will be enabled after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### <span data-ttu-id="f1017-153">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-153">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="f1017-154">AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="f1017-154">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="f1017-155">valeur publique HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="f1017-155">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="f1017-156">Si elle a la valeur false, le WebView n’affichera pas la boîte de dialogue JavaScript par défaut (en particulier, celles qui sont affichées par l’alerte JavaScript, les fonctions confirmer, invites et événement beforeunload).</span><span class="sxs-lookup"><span data-stu-id="f1017-156">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="f1017-157">Au lieu de cela, si un gestionnaire d’événements est défini par SetScriptDialogOpeningEventHandler, WebView envoie un événement qui contient toutes les informations pour la boîte de dialogue et autorise l’application hôte à afficher sa propre interface utilisateur personnalisée.</span><span class="sxs-lookup"><span data-stu-id="f1017-157">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="f1017-158">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-158">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="f1017-159">AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="f1017-159">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="f1017-160">valeur publique HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="f1017-160">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="f1017-161">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="f1017-161">It is true by default.</span></span>

#### <span data-ttu-id="f1017-162">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="f1017-162">get_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="f1017-163">La propriété AreRemoteObjectsAllowed est utilisée pour contrôler si les objets hôtes sont accessibles à partir de la page dans WebView.</span><span class="sxs-lookup"><span data-stu-id="f1017-163">The AreRemoteObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="f1017-164">valeur publique HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(bool \* autorisé)</span><span class="sxs-lookup"><span data-stu-id="f1017-164">public HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(BOOL \* allowed)</span></span>

<span data-ttu-id="f1017-165">Par défaut, la valeur est TRUE.</span><span class="sxs-lookup"><span data-stu-id="f1017-165">Defaults to TRUE.</span></span>

```cpp
            BOOL allowRemoteObjects;
            CHECK_FAILURE(m_settings->get_AreRemoteObjectsAllowed(&allowRemoteObjects));
            if (allowRemoteObjects)
            {
                CHECK_FAILURE(m_settings->put_AreRemoteObjectsAllowed(FALSE));
                MessageBox(
                    nullptr, L"Access to remote objects will be denied after the next navigation.",
                    L"Settings change", MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_AreRemoteObjectsAllowed(TRUE));
                MessageBox(
                    nullptr, L"Access to remote objects will be allowed after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### <span data-ttu-id="f1017-166">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-166">get_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="f1017-167">La propriété IsBuiltInErrorPageEnabled est utilisée pour désactiver la page d’erreur intégrée à un échec de navigation et un échec de processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="f1017-167">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="f1017-168">[get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)publique HRESULT (bool \* activé)</span><span class="sxs-lookup"><span data-stu-id="f1017-168">public HRESULT [get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="f1017-169">Par défaut, la valeur est TRUE.</span><span class="sxs-lookup"><span data-stu-id="f1017-169">Defaults to TRUE.</span></span> <span data-ttu-id="f1017-170">Lorsqu’elle est désactivée, une page vide s’affiche lorsque l’erreur associée se produit.</span><span class="sxs-lookup"><span data-stu-id="f1017-170">When disabled, blank page will be shown when related error happens.</span></span>

```cpp
            BOOL enabled;
            CHECK_FAILURE(m_settings->get_IsBuiltInErrorPageEnabled(&enabled));
            if (enabled)
            {
                CHECK_FAILURE(m_settings->put_IsBuiltInErrorPageEnabled(FALSE));
                MessageBox(
                    nullptr, L"Built-in error page will be disabled for future navigation.",
                    L"Settings change", MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_IsBuiltInErrorPageEnabled(TRUE));
                MessageBox(
                    nullptr, L"Built-in error page will be enabled for future navigation.",
                    L"Settings change", MB_OK);
            }
```

#### <span data-ttu-id="f1017-171">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-171">get_IsScriptEnabled</span></span> 

<span data-ttu-id="f1017-172">Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.</span><span class="sxs-lookup"><span data-stu-id="f1017-172">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="f1017-173">valeur publique HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="f1017-173">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="f1017-174">Cela ne concerne que les scripts du document. les scripts injectés avec ExecuteScript s’exécutent même si le script est désactivé.</span><span class="sxs-lookup"><span data-stu-id="f1017-174">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="f1017-175">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="f1017-175">It is true by default.</span></span>

```cpp
        // Changes to settings will apply at the next navigation, which includes the
        // navigation after a NavigationStarting event.  We can use this to change
        // settings according to what site we're visiting.
        if (ShouldBlockScriptForUri(uri.get()))
        {
            m_settings->put_IsScriptEnabled(FALSE);
        }
        else
        {
            m_settings->put_IsScriptEnabled(m_isScriptEnabled);
        }
```

#### <span data-ttu-id="f1017-176">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-176">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="f1017-177">IsStatusBarEnabled vérifie si la barre d’État s’affiche.</span><span class="sxs-lookup"><span data-stu-id="f1017-177">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="f1017-178">valeur publique HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="f1017-178">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="f1017-179">La barre d’État est généralement affichée dans le coin inférieur gauche de l’affichage WebView et présente des éléments tels que l’URI d’un lien lorsque l’utilisateur pointe dessus et d’autres informations.</span><span class="sxs-lookup"><span data-stu-id="f1017-179">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="f1017-180">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="f1017-180">It is true by default.</span></span>

#### <span data-ttu-id="f1017-181">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-181">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="f1017-182">La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="f1017-182">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="f1017-183">valeur publique HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="f1017-183">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="f1017-184">Si elle a la valeur true, la communication de l’hôte vers le document HTML de niveau supérieur de l’hôte est autorisée via PostWebMessageAsJson, PostWebMessageAsString et Window. chrome. événement de message (voir la documentation PostWebMessageAsJson pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="f1017-184">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="f1017-185">La communication du document HTML de niveau supérieur d’un WebView à l’hôte est autorisée via la fonction postMessage de Window. chrome. WebView et la méthode SetWebMessageReceivedEventHandler (voir la documentation SetWebMessageReceivedEventHandler pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="f1017-185">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="f1017-186">Si elle est définie sur false, la communication n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="f1017-186">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="f1017-187">PostWebMessageAsJson et PostWebMessageAsString échoueront avec E_ACCESSDENIED et Window. chrome. WebView. postMessage échoue en levant une instance d’objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="f1017-187">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="f1017-188">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="f1017-188">It is true by default.</span></span>

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="f1017-189">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-189">get_IsZoomControlEnabled</span></span> 

<span data-ttu-id="f1017-190">La propriété IsZoomControlEnabled est utilisée pour empêcher l’utilisateur d’influer sur le zoom du WebView.</span><span class="sxs-lookup"><span data-stu-id="f1017-190">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="f1017-191">[get_IsZoomControlEnabled](#get_iszoomcontrolenabled)publique HRESULT (bool \* activé)</span><span class="sxs-lookup"><span data-stu-id="f1017-191">public HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="f1017-192">Par défaut, la valeur est TRUE.</span><span class="sxs-lookup"><span data-stu-id="f1017-192">Defaults to TRUE.</span></span> <span data-ttu-id="f1017-193">Lorsqu’il est désactivé, l’utilisateur ne peut pas effectuer un zoom à l’aide de Ctrl +/-ou Ctrl + molette, mais le zoom peut être défini via l’API ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="f1017-193">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

```cpp
            BOOL zoomControlEnabled;
            CHECK_FAILURE(m_settings->get_IsZoomControlEnabled(&zoomControlEnabled));
            if (zoomControlEnabled)
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(FALSE));
                MessageBox(
                    nullptr, L"Zoom control will be disabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(TRUE));
                MessageBox(
                    nullptr, L"Zoom control will be enabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
```

#### <span data-ttu-id="f1017-194">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-194">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="f1017-195">Définissez la propriété AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="f1017-195">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="f1017-196">[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)publiques HRESULT</span><span class="sxs-lookup"><span data-stu-id="f1017-196">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="f1017-197">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-197">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="f1017-198">Définissez la propriété AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="f1017-198">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="f1017-199">[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="f1017-199">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="f1017-200">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-200">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="f1017-201">Définissez la propriété AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="f1017-201">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="f1017-202">[put_AreDevToolsEnabled](#put_aredevtoolsenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="f1017-202">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

#### <span data-ttu-id="f1017-203">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="f1017-203">put_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="f1017-204">Définissez la propriété AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="f1017-204">Set the AreRemoteObjectsAllowed property.</span></span>

> <span data-ttu-id="f1017-205">[put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)publiques HRESULT</span><span class="sxs-lookup"><span data-stu-id="f1017-205">public HRESULT [put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)(BOOL allowed)</span></span>

#### <span data-ttu-id="f1017-206">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-206">put_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="f1017-207">Définissez la propriété IsBuiltInErrorPageEnabled.</span><span class="sxs-lookup"><span data-stu-id="f1017-207">Set the IsBuiltInErrorPageEnabled property.</span></span>

> <span data-ttu-id="f1017-208">[put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)publiques HRESULT</span><span class="sxs-lookup"><span data-stu-id="f1017-208">public HRESULT [put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="f1017-209">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-209">put_IsScriptEnabled</span></span> 

<span data-ttu-id="f1017-210">Définissez la propriété IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="f1017-210">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="f1017-211">[put_IsScriptEnabled](#put_isscriptenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="f1017-211">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="f1017-212">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-212">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="f1017-213">Définissez la propriété IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="f1017-213">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="f1017-214">[put_IsStatusBarEnabled](#put_isstatusbarenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="f1017-214">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="f1017-215">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-215">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="f1017-216">Définissez la propriété IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="f1017-216">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="f1017-217">[put_IsWebMessageEnabled](#put_iswebmessageenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="f1017-217">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="f1017-218">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="f1017-218">put_IsZoomControlEnabled</span></span> 

<span data-ttu-id="f1017-219">Définissez la propriété IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="f1017-219">Set the IsZoomControlEnabled property.</span></span>

> <span data-ttu-id="f1017-220">[put_IsZoomControlEnabled](#put_iszoomcontrolenabled)publiques HRESULT</span><span class="sxs-lookup"><span data-stu-id="f1017-220">public HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(BOOL enabled)</span></span>

