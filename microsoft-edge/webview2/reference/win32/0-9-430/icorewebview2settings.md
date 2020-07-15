---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 2596b2352f36dce6773de2e60e0442ff5fa3b6d5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880219"
---
# <span data-ttu-id="1ff97-104">0.9.430-interface ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="1ff97-104">0.9.430 - interface ICoreWebView2Settings</span></span> 

> [!NOTE]
> <span data-ttu-id="1ff97-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="1ff97-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="1ff97-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="1ff97-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Settings
  : public IUnknown
```

<span data-ttu-id="1ff97-107">Définit les propriétés permettant, de désactiver ou de modifier les fonctionnalités WebView.</span><span class="sxs-lookup"><span data-stu-id="1ff97-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="1ff97-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="1ff97-108">Summary</span></span>

 <span data-ttu-id="1ff97-109">Ses</span><span class="sxs-lookup"><span data-stu-id="1ff97-109">Members</span></span>                        | <span data-ttu-id="1ff97-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="1ff97-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1ff97-111">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-111">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="1ff97-112">Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.</span><span class="sxs-lookup"><span data-stu-id="1ff97-112">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="1ff97-113">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-113">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="1ff97-114">Définissez la propriété IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="1ff97-114">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="1ff97-115">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-115">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="1ff97-116">La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="1ff97-116">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="1ff97-117">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-117">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="1ff97-118">Définissez la propriété IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="1ff97-118">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="1ff97-119">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-119">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="1ff97-120">AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="1ff97-120">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="1ff97-121">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-121">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="1ff97-122">Définissez la propriété AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="1ff97-122">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="1ff97-123">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-123">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="1ff97-124">IsStatusBarEnabled vérifie si la barre d’État s’affiche.</span><span class="sxs-lookup"><span data-stu-id="1ff97-124">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="1ff97-125">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-125">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="1ff97-126">Définissez la propriété IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="1ff97-126">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="1ff97-127">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-127">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="1ff97-128">AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="1ff97-128">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="1ff97-129">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-129">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="1ff97-130">Définissez la propriété AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="1ff97-130">Set the AreDevToolsEnabled property.</span></span>
[<span data-ttu-id="1ff97-131">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-131">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="1ff97-132">La propriété AreDefaultContextMenusEnabled est utilisée pour empêcher l’affichage des menus contextuels par défaut pour les utilisateurs dans WebView.</span><span class="sxs-lookup"><span data-stu-id="1ff97-132">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="1ff97-133">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-133">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="1ff97-134">Définissez la propriété AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="1ff97-134">Set the AreDefaultContextMenusEnabled property.</span></span>
[<span data-ttu-id="1ff97-135">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="1ff97-135">get_AreRemoteObjectsAllowed</span></span>](#get_areremoteobjectsallowed) | <span data-ttu-id="1ff97-136">La propriété AreRemoteObjectsAllowed est utilisée pour contrôler si les objets distants sont accessibles à partir de la page dans WebView.</span><span class="sxs-lookup"><span data-stu-id="1ff97-136">The AreRemoteObjectsAllowed property is used to control whether remote objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="1ff97-137">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="1ff97-137">put_AreRemoteObjectsAllowed</span></span>](#put_areremoteobjectsallowed) | <span data-ttu-id="1ff97-138">Définissez la propriété AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="1ff97-138">Set the AreRemoteObjectsAllowed property.</span></span>
[<span data-ttu-id="1ff97-139">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-139">get_IsZoomControlEnabled</span></span>](#get_iszoomcontrolenabled) | <span data-ttu-id="1ff97-140">La propriété IsZoomControlEnabled est utilisée pour empêcher l’utilisateur d’influer sur le zoom du WebView.</span><span class="sxs-lookup"><span data-stu-id="1ff97-140">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>
[<span data-ttu-id="1ff97-141">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-141">put_IsZoomControlEnabled</span></span>](#put_iszoomcontrolenabled) | <span data-ttu-id="1ff97-142">Définissez la propriété IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="1ff97-142">Set the IsZoomControlEnabled property.</span></span>

<span data-ttu-id="1ff97-143">Les modifications apportées après l’événement NavigationStarting ne s’appliquent pas tant que la navigation de niveau supérieur suivante n’est pas appliquée.</span><span class="sxs-lookup"><span data-stu-id="1ff97-143">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="1ff97-144">Ses</span><span class="sxs-lookup"><span data-stu-id="1ff97-144">Members</span></span>

#### <span data-ttu-id="1ff97-145">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-145">get_IsScriptEnabled</span></span> 

<span data-ttu-id="1ff97-146">Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.</span><span class="sxs-lookup"><span data-stu-id="1ff97-146">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="1ff97-147">valeur publique HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="1ff97-147">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="1ff97-148">Cela ne concerne que les scripts du document. les scripts injectés avec ExecuteScript s’exécutent même si le script est désactivé.</span><span class="sxs-lookup"><span data-stu-id="1ff97-148">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="1ff97-149">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="1ff97-149">It is true by default.</span></span>

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

#### <span data-ttu-id="1ff97-150">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-150">put_IsScriptEnabled</span></span> 

<span data-ttu-id="1ff97-151">Définissez la propriété IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="1ff97-151">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="1ff97-152">[put_IsScriptEnabled](#put_isscriptenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="1ff97-152">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="1ff97-153">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-153">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="1ff97-154">La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="1ff97-154">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="1ff97-155">valeur publique HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="1ff97-155">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="1ff97-156">Si elle a la valeur true, la communication de l’hôte vers le document HTML de niveau supérieur de l’hôte est autorisée via PostWebMessageAsJson, PostWebMessageAsString et Window. chrome. événement de message (voir la documentation PostWebMessageAsJson pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="1ff97-156">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="1ff97-157">La communication du document HTML de niveau supérieur d’un WebView à l’hôte est autorisée via la fonction postMessage de Window. chrome. WebView et la méthode SetWebMessageReceivedEventHandler (voir la documentation SetWebMessageReceivedEventHandler pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="1ff97-157">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="1ff97-158">Si elle est définie sur false, la communication n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="1ff97-158">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="1ff97-159">PostWebMessageAsJson et PostWebMessageAsString échoueront avec E_ACCESSDENIED et Window. chrome. WebView. postMessage échoue en levant une instance d’objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="1ff97-159">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="1ff97-160">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="1ff97-160">It is true by default.</span></span>

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="1ff97-161">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-161">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="1ff97-162">Définissez la propriété IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="1ff97-162">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="1ff97-163">[put_IsWebMessageEnabled](#put_iswebmessageenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="1ff97-163">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="1ff97-164">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-164">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="1ff97-165">AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="1ff97-165">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="1ff97-166">valeur publique HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="1ff97-166">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="1ff97-167">Si elle a la valeur false, le WebView n’affichera pas la boîte de dialogue JavaScript par défaut (en particulier, celles qui sont affichées par l’alerte JavaScript, les fonctions confirmer, invites et événement beforeunload).</span><span class="sxs-lookup"><span data-stu-id="1ff97-167">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="1ff97-168">Au lieu de cela, si un gestionnaire d’événements est défini par SetScriptDialogOpeningEventHandler, WebView envoie un événement qui contient toutes les informations pour la boîte de dialogue et autorise l’application hôte à afficher sa propre interface utilisateur personnalisée.</span><span class="sxs-lookup"><span data-stu-id="1ff97-168">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="1ff97-169">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-169">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="1ff97-170">Définissez la propriété AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="1ff97-170">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="1ff97-171">[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="1ff97-171">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="1ff97-172">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-172">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="1ff97-173">IsStatusBarEnabled vérifie si la barre d’État s’affiche.</span><span class="sxs-lookup"><span data-stu-id="1ff97-173">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="1ff97-174">valeur publique HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="1ff97-174">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="1ff97-175">La barre d’État est généralement affichée dans le coin inférieur gauche de l’affichage WebView et présente des éléments tels que l’URI d’un lien lorsque l’utilisateur pointe dessus et d’autres informations.</span><span class="sxs-lookup"><span data-stu-id="1ff97-175">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="1ff97-176">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="1ff97-176">It is true by default.</span></span>

#### <span data-ttu-id="1ff97-177">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-177">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="1ff97-178">Définissez la propriété IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="1ff97-178">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="1ff97-179">[put_IsStatusBarEnabled](#put_isstatusbarenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="1ff97-179">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="1ff97-180">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-180">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="1ff97-181">AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="1ff97-181">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="1ff97-182">valeur publique HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="1ff97-182">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="1ff97-183">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="1ff97-183">It is true by default.</span></span>

#### <span data-ttu-id="1ff97-184">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-184">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="1ff97-185">Définissez la propriété AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="1ff97-185">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="1ff97-186">[put_AreDevToolsEnabled](#put_aredevtoolsenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="1ff97-186">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

#### <span data-ttu-id="1ff97-187">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-187">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="1ff97-188">La propriété AreDefaultContextMenusEnabled est utilisée pour empêcher l’affichage des menus contextuels par défaut pour les utilisateurs dans WebView.</span><span class="sxs-lookup"><span data-stu-id="1ff97-188">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="1ff97-189">[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)publique HRESULT (bool \* activé)</span><span class="sxs-lookup"><span data-stu-id="1ff97-189">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="1ff97-190">Par défaut, la valeur est TRUE.</span><span class="sxs-lookup"><span data-stu-id="1ff97-190">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="1ff97-191">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-191">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="1ff97-192">Définissez la propriété AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="1ff97-192">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="1ff97-193">[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)publiques HRESULT</span><span class="sxs-lookup"><span data-stu-id="1ff97-193">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="1ff97-194">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="1ff97-194">get_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="1ff97-195">La propriété AreRemoteObjectsAllowed est utilisée pour contrôler si les objets distants sont accessibles à partir de la page dans WebView.</span><span class="sxs-lookup"><span data-stu-id="1ff97-195">The AreRemoteObjectsAllowed property is used to control whether remote objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="1ff97-196">valeur publique HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(bool \* autorisé)</span><span class="sxs-lookup"><span data-stu-id="1ff97-196">public HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(BOOL \* allowed)</span></span>

<span data-ttu-id="1ff97-197">Par défaut, la valeur est TRUE.</span><span class="sxs-lookup"><span data-stu-id="1ff97-197">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="1ff97-198">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="1ff97-198">put_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="1ff97-199">Définissez la propriété AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="1ff97-199">Set the AreRemoteObjectsAllowed property.</span></span>

> <span data-ttu-id="1ff97-200">[put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)publiques HRESULT</span><span class="sxs-lookup"><span data-stu-id="1ff97-200">public HRESULT [put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)(BOOL allowed)</span></span>

#### <span data-ttu-id="1ff97-201">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-201">get_IsZoomControlEnabled</span></span> 

<span data-ttu-id="1ff97-202">La propriété IsZoomControlEnabled est utilisée pour empêcher l’utilisateur d’influer sur le zoom du WebView.</span><span class="sxs-lookup"><span data-stu-id="1ff97-202">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="1ff97-203">[get_IsZoomControlEnabled](#get_iszoomcontrolenabled)publique HRESULT (bool \* activé)</span><span class="sxs-lookup"><span data-stu-id="1ff97-203">public HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="1ff97-204">Par défaut, la valeur est TRUE.</span><span class="sxs-lookup"><span data-stu-id="1ff97-204">Defaults to TRUE.</span></span> <span data-ttu-id="1ff97-205">Lorsqu’il est désactivé, l’utilisateur ne peut pas effectuer un zoom à l’aide de Ctrl +/-ou Ctrl + molette, mais le zoom peut être défini via une API de put_ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="1ff97-205">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via put_ZoomFactor API.</span></span>

```cpp
            BOOL zoomControlEnabled;
            CHECK_FAILURE(m_settings->get_IsZoomControlEnabled(&zoomControlEnabled));
            if (zoomControlEnabled)
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(FALSE));
                MessageBox(
                    nullptr, L"Zoom control is disabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(TRUE));
                MessageBox(
                    nullptr, L"Zoom control is enabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
```

#### <span data-ttu-id="1ff97-206">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="1ff97-206">put_IsZoomControlEnabled</span></span> 

<span data-ttu-id="1ff97-207">Définissez la propriété IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="1ff97-207">Set the IsZoomControlEnabled property.</span></span>

> <span data-ttu-id="1ff97-208">[put_IsZoomControlEnabled](#put_iszoomcontrolenabled)publiques HRESULT</span><span class="sxs-lookup"><span data-stu-id="1ff97-208">public HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(BOOL enabled)</span></span>

