---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2Settings
ms.openlocfilehash: 1ad6754d2ff59a92e107c66644e389582ff6053b
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011931"
---
# <span data-ttu-id="9d65a-104">interface ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="9d65a-104">interface ICoreWebView2Settings</span></span> 

```
interface ICoreWebView2Settings
  : public IUnknown
```

<span data-ttu-id="9d65a-105">Définit les propriétés permettant, de désactiver ou de modifier les fonctionnalités WebView.</span><span class="sxs-lookup"><span data-stu-id="9d65a-105">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="9d65a-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="9d65a-106">Summary</span></span>

 <span data-ttu-id="9d65a-107">Ses</span><span class="sxs-lookup"><span data-stu-id="9d65a-107">Members</span></span>                        | <span data-ttu-id="9d65a-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="9d65a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9d65a-109">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-109">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="9d65a-110">La propriété AreDefaultContextMenusEnabled est utilisée pour empêcher l’affichage des menus contextuels par défaut pour les utilisateurs dans WebView.</span><span class="sxs-lookup"><span data-stu-id="9d65a-110">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in WebView.</span></span>
[<span data-ttu-id="9d65a-111">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-111">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="9d65a-112">AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="9d65a-112">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="9d65a-113">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-113">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="9d65a-114">AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="9d65a-114">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="9d65a-115">get_AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="9d65a-115">get_AreHostObjectsAllowed</span></span>](#get_arehostobjectsallowed) | <span data-ttu-id="9d65a-116">La propriété AreHostObjectsAllowed est utilisée pour contrôler si les objets hôtes sont accessibles à partir de la page dans WebView.</span><span class="sxs-lookup"><span data-stu-id="9d65a-116">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in WebView.</span></span>
[<span data-ttu-id="9d65a-117">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-117">get_IsBuiltInErrorPageEnabled</span></span>](#get_isbuiltinerrorpageenabled) | <span data-ttu-id="9d65a-118">La propriété IsBuiltInErrorPageEnabled est utilisée pour désactiver la page d’erreur intégrée à un échec de navigation et un échec de processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="9d65a-118">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="9d65a-119">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-119">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="9d65a-120">Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.</span><span class="sxs-lookup"><span data-stu-id="9d65a-120">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="9d65a-121">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-121">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="9d65a-122">IsStatusBarEnabled vérifie si la barre d’État s’affiche.</span><span class="sxs-lookup"><span data-stu-id="9d65a-122">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="9d65a-123">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-123">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="9d65a-124">La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="9d65a-124">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="9d65a-125">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-125">get_IsZoomControlEnabled</span></span>](#get_iszoomcontrolenabled) | <span data-ttu-id="9d65a-126">La propriété IsZoomControlEnabled est utilisée pour empêcher l’utilisateur d’influer sur le zoom du WebView.</span><span class="sxs-lookup"><span data-stu-id="9d65a-126">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>
[<span data-ttu-id="9d65a-127">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-127">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="9d65a-128">Définissez la propriété AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="9d65a-128">Set the AreDefaultContextMenusEnabled property.</span></span>
[<span data-ttu-id="9d65a-129">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-129">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="9d65a-130">Définissez la propriété AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="9d65a-130">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="9d65a-131">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-131">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="9d65a-132">Définissez la propriété AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="9d65a-132">Set the AreDevToolsEnabled property.</span></span>
[<span data-ttu-id="9d65a-133">put_AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="9d65a-133">put_AreHostObjectsAllowed</span></span>](#put_arehostobjectsallowed) | <span data-ttu-id="9d65a-134">Définissez la propriété AreHostObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="9d65a-134">Set the AreHostObjectsAllowed property.</span></span>
[<span data-ttu-id="9d65a-135">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-135">put_IsBuiltInErrorPageEnabled</span></span>](#put_isbuiltinerrorpageenabled) | <span data-ttu-id="9d65a-136">Définissez la propriété IsBuiltInErrorPageEnabled.</span><span class="sxs-lookup"><span data-stu-id="9d65a-136">Set the IsBuiltInErrorPageEnabled property.</span></span>
[<span data-ttu-id="9d65a-137">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-137">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="9d65a-138">Définissez la propriété IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="9d65a-138">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="9d65a-139">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-139">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="9d65a-140">Définissez la propriété IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="9d65a-140">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="9d65a-141">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-141">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="9d65a-142">Définissez la propriété IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="9d65a-142">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="9d65a-143">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-143">put_IsZoomControlEnabled</span></span>](#put_iszoomcontrolenabled) | <span data-ttu-id="9d65a-144">Définissez la propriété IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="9d65a-144">Set the IsZoomControlEnabled property.</span></span>

<span data-ttu-id="9d65a-145">Les modifications apportées après l’événement NavigationStarting ne s’appliquent pas tant que la navigation de niveau supérieur suivante n’est pas appliquée.</span><span class="sxs-lookup"><span data-stu-id="9d65a-145">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="9d65a-146">Ses</span><span class="sxs-lookup"><span data-stu-id="9d65a-146">Members</span></span>

#### <span data-ttu-id="9d65a-147">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-147">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="9d65a-148">La propriété AreDefaultContextMenusEnabled est utilisée pour empêcher l’affichage des menus contextuels par défaut pour les utilisateurs dans WebView.</span><span class="sxs-lookup"><span data-stu-id="9d65a-148">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in WebView.</span></span>

> <span data-ttu-id="9d65a-149">[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)publique HRESULT (bool \* activé)</span><span class="sxs-lookup"><span data-stu-id="9d65a-149">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="9d65a-150">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="9d65a-150">It is true by default.</span></span>

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

#### <span data-ttu-id="9d65a-151">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-151">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="9d65a-152">AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="9d65a-152">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="9d65a-153">valeur publique HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="9d65a-153">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="9d65a-154">Si elle a la valeur false, le WebView n’affichera pas la boîte de dialogue JavaScript par défaut (en particulier, celles qui sont affichées par l’alerte JavaScript, les fonctions confirmer, invites et événement beforeunload).</span><span class="sxs-lookup"><span data-stu-id="9d65a-154">If set to false, then WebView won't render the default JavaScript dialog box (Specifically those shown by the JavaScript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="9d65a-155">Au lieu de cela, si un gestionnaire d’événements est défini via add_ScriptDialogOpening, WebView envoie un événement qui contient toutes les informations pour la boîte de dialogue et autorise l’application hôte à afficher sa propre interface utilisateur personnalisée.</span><span class="sxs-lookup"><span data-stu-id="9d65a-155">Instead, if an event handler is set via add_ScriptDialogOpening, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span> <span data-ttu-id="9d65a-156">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="9d65a-156">It is true by default.</span></span>

#### <span data-ttu-id="9d65a-157">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-157">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="9d65a-158">AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="9d65a-158">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="9d65a-159">valeur publique HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="9d65a-159">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="9d65a-160">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="9d65a-160">It is true by default.</span></span>

#### <span data-ttu-id="9d65a-161">get_AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="9d65a-161">get_AreHostObjectsAllowed</span></span> 

<span data-ttu-id="9d65a-162">La propriété AreHostObjectsAllowed est utilisée pour contrôler si les objets hôtes sont accessibles à partir de la page dans WebView.</span><span class="sxs-lookup"><span data-stu-id="9d65a-162">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in WebView.</span></span>

> <span data-ttu-id="9d65a-163">valeur publique HRESULT [get_AreHostObjectsAllowed](#get_arehostobjectsallowed)(bool \* autorisé)</span><span class="sxs-lookup"><span data-stu-id="9d65a-163">public HRESULT [get_AreHostObjectsAllowed](#get_arehostobjectsallowed)(BOOL \* allowed)</span></span>

<span data-ttu-id="9d65a-164">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="9d65a-164">It is true by default.</span></span>

```cpp
            BOOL allowHostObjects;
            CHECK_FAILURE(m_settings->get_AreHostObjectsAllowed(&allowHostObjects));
            if (allowHostObjects)
            {
                CHECK_FAILURE(m_settings->put_AreHostObjectsAllowed(FALSE));
                MessageBox(
                    nullptr, L"Access to host objects will be denied after the next navigation.",
                    L"Settings change", MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_AreHostObjectsAllowed(TRUE));
                MessageBox(
                    nullptr, L"Access to host objects will be allowed after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### <span data-ttu-id="9d65a-165">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-165">get_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="9d65a-166">La propriété IsBuiltInErrorPageEnabled est utilisée pour désactiver la page d’erreur intégrée à un échec de navigation et un échec de processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="9d65a-166">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="9d65a-167">[get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)publique HRESULT (bool \* activé)</span><span class="sxs-lookup"><span data-stu-id="9d65a-167">public HRESULT [get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="9d65a-168">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="9d65a-168">It is true by default.</span></span> <span data-ttu-id="9d65a-169">Lorsqu’elle est désactivée, une page vide s’affiche lorsque l’erreur associée se produit.</span><span class="sxs-lookup"><span data-stu-id="9d65a-169">When disabled, blank page will be shown when related error happens.</span></span>

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

#### <span data-ttu-id="9d65a-170">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-170">get_IsScriptEnabled</span></span> 

<span data-ttu-id="9d65a-171">Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.</span><span class="sxs-lookup"><span data-stu-id="9d65a-171">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="9d65a-172">valeur publique HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="9d65a-172">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="9d65a-173">Cela ne concerne que les scripts du document. les scripts injectés avec ExecuteScript s’exécutent même si le script est désactivé.</span><span class="sxs-lookup"><span data-stu-id="9d65a-173">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="9d65a-174">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="9d65a-174">It is true by default.</span></span>

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

#### <span data-ttu-id="9d65a-175">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-175">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="9d65a-176">IsStatusBarEnabled vérifie si la barre d’État s’affiche.</span><span class="sxs-lookup"><span data-stu-id="9d65a-176">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="9d65a-177">valeur publique HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="9d65a-177">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="9d65a-178">La barre d’État est généralement affichée dans le coin inférieur gauche de l’affichage WebView et présente des éléments tels que l’URI d’un lien lorsque l’utilisateur pointe dessus et d’autres informations.</span><span class="sxs-lookup"><span data-stu-id="9d65a-178">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="9d65a-179">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="9d65a-179">It is true by default.</span></span>

#### <span data-ttu-id="9d65a-180">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-180">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="9d65a-181">La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="9d65a-181">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="9d65a-182">valeur publique HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="9d65a-182">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="9d65a-183">Si elle a la valeur true, la communication de l’hôte vers le document HTML de niveau supérieur de l’hôte est autorisée via PostWebMessageAsJson, PostWebMessageAsString et Window. chrome. événement de message (voir la documentation PostWebMessageAsJson pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="9d65a-183">If set to true, communication from the host to the WebView's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="9d65a-184">La communication du document HTML de niveau supérieur de la WebView à l’hôte est autorisée via la fonction postMessage de Window. chrome. WebView et la méthode add_WebMessageReceived (voir la documentation add_WebMessageReceived pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="9d65a-184">Communication from the WebView's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and add_WebMessageReceived method (see add_WebMessageReceived documentation for details).</span></span> <span data-ttu-id="9d65a-185">Si elle est définie sur false, la communication n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="9d65a-185">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="9d65a-186">PostWebMessageAsJson et PostWebMessageAsString échoueront avec E_ACCESSDENIED et Window. chrome. WebView. postMessage échoue en levant une instance d’objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="9d65a-186">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="9d65a-187">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="9d65a-187">It is true by default.</span></span>

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="9d65a-188">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-188">get_IsZoomControlEnabled</span></span> 

<span data-ttu-id="9d65a-189">La propriété IsZoomControlEnabled est utilisée pour empêcher l’utilisateur d’influer sur le zoom du WebView.</span><span class="sxs-lookup"><span data-stu-id="9d65a-189">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="9d65a-190">[get_IsZoomControlEnabled](#get_iszoomcontrolenabled)publique HRESULT (bool \* activé)</span><span class="sxs-lookup"><span data-stu-id="9d65a-190">public HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="9d65a-191">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="9d65a-191">It is true by default.</span></span> <span data-ttu-id="9d65a-192">Lorsqu’il est désactivé, l’utilisateur ne peut pas effectuer un zoom à l’aide de Ctrl +/-ou Ctrl + molette, mais le zoom peut être défini via l’API ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="9d65a-192">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

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

#### <span data-ttu-id="9d65a-193">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-193">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="9d65a-194">Définissez la propriété AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="9d65a-194">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="9d65a-195">[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)publiques HRESULT</span><span class="sxs-lookup"><span data-stu-id="9d65a-195">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="9d65a-196">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-196">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="9d65a-197">Définissez la propriété AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="9d65a-197">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="9d65a-198">[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="9d65a-198">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="9d65a-199">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-199">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="9d65a-200">Définissez la propriété AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="9d65a-200">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="9d65a-201">[put_AreDevToolsEnabled](#put_aredevtoolsenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="9d65a-201">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

#### <span data-ttu-id="9d65a-202">put_AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="9d65a-202">put_AreHostObjectsAllowed</span></span> 

<span data-ttu-id="9d65a-203">Définissez la propriété AreHostObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="9d65a-203">Set the AreHostObjectsAllowed property.</span></span>

> <span data-ttu-id="9d65a-204">[put_AreHostObjectsAllowed](#put_arehostobjectsallowed)publiques HRESULT</span><span class="sxs-lookup"><span data-stu-id="9d65a-204">public HRESULT [put_AreHostObjectsAllowed](#put_arehostobjectsallowed)(BOOL allowed)</span></span>

#### <span data-ttu-id="9d65a-205">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-205">put_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="9d65a-206">Définissez la propriété IsBuiltInErrorPageEnabled.</span><span class="sxs-lookup"><span data-stu-id="9d65a-206">Set the IsBuiltInErrorPageEnabled property.</span></span>

> <span data-ttu-id="9d65a-207">[put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)publiques HRESULT</span><span class="sxs-lookup"><span data-stu-id="9d65a-207">public HRESULT [put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="9d65a-208">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-208">put_IsScriptEnabled</span></span> 

<span data-ttu-id="9d65a-209">Définissez la propriété IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="9d65a-209">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="9d65a-210">[put_IsScriptEnabled](#put_isscriptenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="9d65a-210">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="9d65a-211">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-211">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="9d65a-212">Définissez la propriété IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="9d65a-212">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="9d65a-213">[put_IsStatusBarEnabled](#put_isstatusbarenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="9d65a-213">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="9d65a-214">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-214">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="9d65a-215">Définissez la propriété IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="9d65a-215">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="9d65a-216">[put_IsWebMessageEnabled](#put_iswebmessageenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="9d65a-216">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="9d65a-217">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="9d65a-217">put_IsZoomControlEnabled</span></span> 

<span data-ttu-id="9d65a-218">Définissez la propriété IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="9d65a-218">Set the IsZoomControlEnabled property.</span></span>

> <span data-ttu-id="9d65a-219">[put_IsZoomControlEnabled](#put_iszoomcontrolenabled)publiques HRESULT</span><span class="sxs-lookup"><span data-stu-id="9d65a-219">public HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(BOOL enabled)</span></span>

