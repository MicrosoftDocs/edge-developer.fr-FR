---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: a2ecd4bdb2d27a5e881f52791ae21290c748966a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886492"
---
# <span data-ttu-id="12c49-104">0.9.515-interface ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="12c49-104">0.9.515 - interface ICoreWebView2Settings</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2Settings
  : public IUnknown
```

<span data-ttu-id="12c49-105">Définit les propriétés permettant, de désactiver ou de modifier les fonctionnalités WebView.</span><span class="sxs-lookup"><span data-stu-id="12c49-105">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="12c49-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="12c49-106">Summary</span></span>

 <span data-ttu-id="12c49-107">Ses</span><span class="sxs-lookup"><span data-stu-id="12c49-107">Members</span></span>                        | <span data-ttu-id="12c49-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="12c49-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="12c49-109">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-109">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="12c49-110">La propriété AreDefaultContextMenusEnabled est utilisée pour empêcher l’affichage des menus contextuels par défaut pour les utilisateurs dans WebView.</span><span class="sxs-lookup"><span data-stu-id="12c49-110">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="12c49-111">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-111">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="12c49-112">AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="12c49-112">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="12c49-113">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-113">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="12c49-114">AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="12c49-114">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="12c49-115">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="12c49-115">get_AreRemoteObjectsAllowed</span></span>](#get_areremoteobjectsallowed) | <span data-ttu-id="12c49-116">La propriété AreRemoteObjectsAllowed est utilisée pour contrôler si les objets hôtes sont accessibles à partir de la page dans WebView.</span><span class="sxs-lookup"><span data-stu-id="12c49-116">The AreRemoteObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="12c49-117">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-117">get_IsBuiltInErrorPageEnabled</span></span>](#get_isbuiltinerrorpageenabled) | <span data-ttu-id="12c49-118">La propriété IsBuiltInErrorPageEnabled est utilisée pour désactiver la page d’erreur intégrée à un échec de navigation et un échec de processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="12c49-118">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="12c49-119">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-119">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="12c49-120">Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.</span><span class="sxs-lookup"><span data-stu-id="12c49-120">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="12c49-121">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-121">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="12c49-122">IsStatusBarEnabled vérifie si la barre d’État s’affiche.</span><span class="sxs-lookup"><span data-stu-id="12c49-122">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="12c49-123">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-123">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="12c49-124">La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="12c49-124">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="12c49-125">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-125">get_IsZoomControlEnabled</span></span>](#get_iszoomcontrolenabled) | <span data-ttu-id="12c49-126">La propriété IsZoomControlEnabled est utilisée pour empêcher l’utilisateur d’influer sur le zoom du WebView.</span><span class="sxs-lookup"><span data-stu-id="12c49-126">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>
[<span data-ttu-id="12c49-127">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-127">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="12c49-128">Définissez la propriété AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="12c49-128">Set the AreDefaultContextMenusEnabled property.</span></span>
[<span data-ttu-id="12c49-129">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-129">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="12c49-130">Définissez la propriété AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="12c49-130">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="12c49-131">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-131">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="12c49-132">Définissez la propriété AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="12c49-132">Set the AreDevToolsEnabled property.</span></span>
[<span data-ttu-id="12c49-133">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="12c49-133">put_AreRemoteObjectsAllowed</span></span>](#put_areremoteobjectsallowed) | <span data-ttu-id="12c49-134">Définissez la propriété AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="12c49-134">Set the AreRemoteObjectsAllowed property.</span></span>
[<span data-ttu-id="12c49-135">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-135">put_IsBuiltInErrorPageEnabled</span></span>](#put_isbuiltinerrorpageenabled) | <span data-ttu-id="12c49-136">Définissez la propriété IsBuiltInErrorPageEnabled.</span><span class="sxs-lookup"><span data-stu-id="12c49-136">Set the IsBuiltInErrorPageEnabled property.</span></span>
[<span data-ttu-id="12c49-137">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-137">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="12c49-138">Définissez la propriété IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="12c49-138">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="12c49-139">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-139">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="12c49-140">Définissez la propriété IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="12c49-140">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="12c49-141">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-141">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="12c49-142">Définissez la propriété IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="12c49-142">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="12c49-143">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-143">put_IsZoomControlEnabled</span></span>](#put_iszoomcontrolenabled) | <span data-ttu-id="12c49-144">Définissez la propriété IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="12c49-144">Set the IsZoomControlEnabled property.</span></span>

<span data-ttu-id="12c49-145">Les modifications apportées après l’événement NavigationStarting ne s’appliquent pas tant que la navigation de niveau supérieur suivante n’est pas appliquée.</span><span class="sxs-lookup"><span data-stu-id="12c49-145">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="12c49-146">Ses</span><span class="sxs-lookup"><span data-stu-id="12c49-146">Members</span></span>

#### <span data-ttu-id="12c49-147">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-147">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="12c49-148">La propriété AreDefaultContextMenusEnabled est utilisée pour empêcher l’affichage des menus contextuels par défaut pour les utilisateurs dans WebView.</span><span class="sxs-lookup"><span data-stu-id="12c49-148">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="12c49-149">[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)publique HRESULT (bool \* activé)</span><span class="sxs-lookup"><span data-stu-id="12c49-149">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="12c49-150">Par défaut, la valeur est TRUE.</span><span class="sxs-lookup"><span data-stu-id="12c49-150">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="12c49-151">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-151">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="12c49-152">AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="12c49-152">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="12c49-153">valeur publique HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="12c49-153">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="12c49-154">Si elle a la valeur false, le WebView n’affichera pas la boîte de dialogue JavaScript par défaut (en particulier, celles qui sont affichées par l’alerte JavaScript, les fonctions confirmer, invites et événement beforeunload).</span><span class="sxs-lookup"><span data-stu-id="12c49-154">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="12c49-155">Au lieu de cela, si un gestionnaire d’événements est défini par SetScriptDialogOpeningEventHandler, WebView envoie un événement qui contient toutes les informations pour la boîte de dialogue et autorise l’application hôte à afficher sa propre interface utilisateur personnalisée.</span><span class="sxs-lookup"><span data-stu-id="12c49-155">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="12c49-156">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-156">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="12c49-157">AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="12c49-157">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="12c49-158">valeur publique HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="12c49-158">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="12c49-159">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="12c49-159">It is true by default.</span></span>

#### <span data-ttu-id="12c49-160">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="12c49-160">get_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="12c49-161">La propriété AreRemoteObjectsAllowed est utilisée pour contrôler si les objets hôtes sont accessibles à partir de la page dans WebView.</span><span class="sxs-lookup"><span data-stu-id="12c49-161">The AreRemoteObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="12c49-162">valeur publique HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(bool \* autorisé)</span><span class="sxs-lookup"><span data-stu-id="12c49-162">public HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(BOOL \* allowed)</span></span>

<span data-ttu-id="12c49-163">Par défaut, la valeur est TRUE.</span><span class="sxs-lookup"><span data-stu-id="12c49-163">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="12c49-164">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-164">get_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="12c49-165">La propriété IsBuiltInErrorPageEnabled est utilisée pour désactiver la page d’erreur intégrée à un échec de navigation et un échec de processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="12c49-165">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="12c49-166">[get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)publique HRESULT (bool \* activé)</span><span class="sxs-lookup"><span data-stu-id="12c49-166">public HRESULT [get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="12c49-167">Par défaut, la valeur est TRUE.</span><span class="sxs-lookup"><span data-stu-id="12c49-167">Defaults to TRUE.</span></span> <span data-ttu-id="12c49-168">Lorsqu’elle est désactivée, une page vide s’affiche lorsque l’erreur associée se produit.</span><span class="sxs-lookup"><span data-stu-id="12c49-168">When disabled, blank page will be shown when related error happens.</span></span>

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

#### <span data-ttu-id="12c49-169">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-169">get_IsScriptEnabled</span></span> 

<span data-ttu-id="12c49-170">Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.</span><span class="sxs-lookup"><span data-stu-id="12c49-170">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="12c49-171">valeur publique HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="12c49-171">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="12c49-172">Cela ne concerne que les scripts du document. les scripts injectés avec ExecuteScript s’exécutent même si le script est désactivé.</span><span class="sxs-lookup"><span data-stu-id="12c49-172">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="12c49-173">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="12c49-173">It is true by default.</span></span>

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

#### <span data-ttu-id="12c49-174">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-174">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="12c49-175">IsStatusBarEnabled vérifie si la barre d’État s’affiche.</span><span class="sxs-lookup"><span data-stu-id="12c49-175">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="12c49-176">valeur publique HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="12c49-176">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="12c49-177">La barre d’État est généralement affichée dans le coin inférieur gauche de l’affichage WebView et présente des éléments tels que l’URI d’un lien lorsque l’utilisateur pointe dessus et d’autres informations.</span><span class="sxs-lookup"><span data-stu-id="12c49-177">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="12c49-178">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="12c49-178">It is true by default.</span></span>

#### <span data-ttu-id="12c49-179">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-179">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="12c49-180">La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="12c49-180">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="12c49-181">valeur publique HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="12c49-181">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="12c49-182">Si elle a la valeur true, la communication de l’hôte vers le document HTML de niveau supérieur de l’hôte est autorisée via PostWebMessageAsJson, PostWebMessageAsString et Window. chrome. événement de message (voir la documentation PostWebMessageAsJson pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="12c49-182">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="12c49-183">La communication du document HTML de niveau supérieur d’un WebView à l’hôte est autorisée via la fonction postMessage de Window. chrome. WebView et la méthode SetWebMessageReceivedEventHandler (voir la documentation SetWebMessageReceivedEventHandler pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="12c49-183">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="12c49-184">Si elle est définie sur false, la communication n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="12c49-184">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="12c49-185">PostWebMessageAsJson et PostWebMessageAsString échoueront avec E_ACCESSDENIED et Window. chrome. WebView. postMessage échoue en levant une instance d’objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="12c49-185">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="12c49-186">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="12c49-186">It is true by default.</span></span>

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="12c49-187">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-187">get_IsZoomControlEnabled</span></span> 

<span data-ttu-id="12c49-188">La propriété IsZoomControlEnabled est utilisée pour empêcher l’utilisateur d’influer sur le zoom du WebView.</span><span class="sxs-lookup"><span data-stu-id="12c49-188">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="12c49-189">[get_IsZoomControlEnabled](#get_iszoomcontrolenabled)publique HRESULT (bool \* activé)</span><span class="sxs-lookup"><span data-stu-id="12c49-189">public HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="12c49-190">Par défaut, la valeur est TRUE.</span><span class="sxs-lookup"><span data-stu-id="12c49-190">Defaults to TRUE.</span></span> <span data-ttu-id="12c49-191">Lorsqu’il est désactivé, l’utilisateur ne peut pas effectuer un zoom à l’aide de Ctrl +/-ou Ctrl + molette, mais le zoom peut être défini via l’API ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="12c49-191">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

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

#### <span data-ttu-id="12c49-192">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-192">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="12c49-193">Définissez la propriété AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="12c49-193">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="12c49-194">[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)publiques HRESULT</span><span class="sxs-lookup"><span data-stu-id="12c49-194">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="12c49-195">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-195">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="12c49-196">Définissez la propriété AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="12c49-196">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="12c49-197">[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="12c49-197">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="12c49-198">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-198">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="12c49-199">Définissez la propriété AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="12c49-199">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="12c49-200">[put_AreDevToolsEnabled](#put_aredevtoolsenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="12c49-200">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

#### <span data-ttu-id="12c49-201">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="12c49-201">put_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="12c49-202">Définissez la propriété AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="12c49-202">Set the AreRemoteObjectsAllowed property.</span></span>

> <span data-ttu-id="12c49-203">[put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)publiques HRESULT</span><span class="sxs-lookup"><span data-stu-id="12c49-203">public HRESULT [put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)(BOOL allowed)</span></span>

#### <span data-ttu-id="12c49-204">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-204">put_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="12c49-205">Définissez la propriété IsBuiltInErrorPageEnabled.</span><span class="sxs-lookup"><span data-stu-id="12c49-205">Set the IsBuiltInErrorPageEnabled property.</span></span>

> <span data-ttu-id="12c49-206">[put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)publiques HRESULT</span><span class="sxs-lookup"><span data-stu-id="12c49-206">public HRESULT [put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="12c49-207">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-207">put_IsScriptEnabled</span></span> 

<span data-ttu-id="12c49-208">Définissez la propriété IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="12c49-208">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="12c49-209">[put_IsScriptEnabled](#put_isscriptenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="12c49-209">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="12c49-210">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-210">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="12c49-211">Définissez la propriété IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="12c49-211">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="12c49-212">[put_IsStatusBarEnabled](#put_isstatusbarenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="12c49-212">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="12c49-213">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-213">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="12c49-214">Définissez la propriété IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="12c49-214">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="12c49-215">[put_IsWebMessageEnabled](#put_iswebmessageenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="12c49-215">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="12c49-216">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="12c49-216">put_IsZoomControlEnabled</span></span> 

<span data-ttu-id="12c49-217">Définissez la propriété IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="12c49-217">Set the IsZoomControlEnabled property.</span></span>

> <span data-ttu-id="12c49-218">[put_IsZoomControlEnabled](#put_iszoomcontrolenabled)publiques HRESULT</span><span class="sxs-lookup"><span data-stu-id="12c49-218">public HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(BOOL enabled)</span></span>

