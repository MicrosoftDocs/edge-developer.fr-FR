---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 70ccef9e99b3649ceca49b736570ba416cf73ebd
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883986"
---
# <span data-ttu-id="d1eb7-104">0.9.430-interface ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="d1eb7-104">0.9.430 - interface ICoreWebView2Settings</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2Settings
  : public IUnknown
```

<span data-ttu-id="d1eb7-105">Définit les propriétés permettant, de désactiver ou de modifier les fonctionnalités WebView.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-105">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="d1eb7-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="d1eb7-106">Summary</span></span>

 <span data-ttu-id="d1eb7-107">Ses</span><span class="sxs-lookup"><span data-stu-id="d1eb7-107">Members</span></span>                        | <span data-ttu-id="d1eb7-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="d1eb7-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d1eb7-109">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-109">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="d1eb7-110">Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-110">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="d1eb7-111">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-111">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="d1eb7-112">Définissez la propriété IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-112">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="d1eb7-113">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-113">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="d1eb7-114">La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-114">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="d1eb7-115">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-115">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="d1eb7-116">Définissez la propriété IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-116">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="d1eb7-117">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-117">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="d1eb7-118">AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-118">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="d1eb7-119">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-119">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="d1eb7-120">Définissez la propriété AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-120">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="d1eb7-121">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-121">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="d1eb7-122">IsStatusBarEnabled vérifie si la barre d’État s’affiche.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-122">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="d1eb7-123">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-123">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="d1eb7-124">Définissez la propriété IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-124">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="d1eb7-125">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-125">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="d1eb7-126">AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-126">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="d1eb7-127">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-127">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="d1eb7-128">Définissez la propriété AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-128">Set the AreDevToolsEnabled property.</span></span>
[<span data-ttu-id="d1eb7-129">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-129">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="d1eb7-130">La propriété AreDefaultContextMenusEnabled est utilisée pour empêcher l’affichage des menus contextuels par défaut pour les utilisateurs dans WebView.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-130">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="d1eb7-131">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-131">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="d1eb7-132">Définissez la propriété AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-132">Set the AreDefaultContextMenusEnabled property.</span></span>
[<span data-ttu-id="d1eb7-133">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="d1eb7-133">get_AreRemoteObjectsAllowed</span></span>](#get_areremoteobjectsallowed) | <span data-ttu-id="d1eb7-134">La propriété AreRemoteObjectsAllowed est utilisée pour contrôler si les objets distants sont accessibles à partir de la page dans WebView.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-134">The AreRemoteObjectsAllowed property is used to control whether remote objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="d1eb7-135">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="d1eb7-135">put_AreRemoteObjectsAllowed</span></span>](#put_areremoteobjectsallowed) | <span data-ttu-id="d1eb7-136">Définissez la propriété AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-136">Set the AreRemoteObjectsAllowed property.</span></span>
[<span data-ttu-id="d1eb7-137">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-137">get_IsZoomControlEnabled</span></span>](#get_iszoomcontrolenabled) | <span data-ttu-id="d1eb7-138">La propriété IsZoomControlEnabled est utilisée pour empêcher l’utilisateur d’influer sur le zoom du WebView.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-138">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>
[<span data-ttu-id="d1eb7-139">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-139">put_IsZoomControlEnabled</span></span>](#put_iszoomcontrolenabled) | <span data-ttu-id="d1eb7-140">Définissez la propriété IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-140">Set the IsZoomControlEnabled property.</span></span>

<span data-ttu-id="d1eb7-141">Les modifications apportées après l’événement NavigationStarting ne s’appliquent pas tant que la navigation de niveau supérieur suivante n’est pas appliquée.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-141">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="d1eb7-142">Ses</span><span class="sxs-lookup"><span data-stu-id="d1eb7-142">Members</span></span>

#### <span data-ttu-id="d1eb7-143">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-143">get_IsScriptEnabled</span></span> 

<span data-ttu-id="d1eb7-144">Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-144">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="d1eb7-145">valeur publique HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="d1eb7-145">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="d1eb7-146">Cela ne concerne que les scripts du document. les scripts injectés avec ExecuteScript s’exécutent même si le script est désactivé.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-146">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="d1eb7-147">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-147">It is true by default.</span></span>

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

#### <span data-ttu-id="d1eb7-148">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-148">put_IsScriptEnabled</span></span> 

<span data-ttu-id="d1eb7-149">Définissez la propriété IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-149">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="d1eb7-150">[put_IsScriptEnabled](#put_isscriptenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="d1eb7-150">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="d1eb7-151">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-151">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="d1eb7-152">La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-152">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="d1eb7-153">valeur publique HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="d1eb7-153">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="d1eb7-154">Si elle a la valeur true, la communication de l’hôte vers le document HTML de niveau supérieur de l’hôte est autorisée via PostWebMessageAsJson, PostWebMessageAsString et Window. chrome. événement de message (voir la documentation PostWebMessageAsJson pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="d1eb7-154">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="d1eb7-155">La communication du document HTML de niveau supérieur d’un WebView à l’hôte est autorisée via la fonction postMessage de Window. chrome. WebView et la méthode SetWebMessageReceivedEventHandler (voir la documentation SetWebMessageReceivedEventHandler pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="d1eb7-155">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="d1eb7-156">Si elle est définie sur false, la communication n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-156">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="d1eb7-157">PostWebMessageAsJson et PostWebMessageAsString échoueront avec E_ACCESSDENIED et Window. chrome. WebView. postMessage échoue en levant une instance d’objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-157">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="d1eb7-158">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-158">It is true by default.</span></span>

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="d1eb7-159">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-159">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="d1eb7-160">Définissez la propriété IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-160">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="d1eb7-161">[put_IsWebMessageEnabled](#put_iswebmessageenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="d1eb7-161">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="d1eb7-162">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-162">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="d1eb7-163">AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-163">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="d1eb7-164">valeur publique HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="d1eb7-164">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="d1eb7-165">Si elle a la valeur false, le WebView n’affichera pas la boîte de dialogue JavaScript par défaut (en particulier, celles qui sont affichées par l’alerte JavaScript, les fonctions confirmer, invites et événement beforeunload).</span><span class="sxs-lookup"><span data-stu-id="d1eb7-165">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="d1eb7-166">Au lieu de cela, si un gestionnaire d’événements est défini par SetScriptDialogOpeningEventHandler, WebView envoie un événement qui contient toutes les informations pour la boîte de dialogue et autorise l’application hôte à afficher sa propre interface utilisateur personnalisée.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-166">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="d1eb7-167">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-167">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="d1eb7-168">Définissez la propriété AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-168">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="d1eb7-169">[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="d1eb7-169">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="d1eb7-170">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-170">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="d1eb7-171">IsStatusBarEnabled vérifie si la barre d’État s’affiche.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-171">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="d1eb7-172">valeur publique HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="d1eb7-172">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="d1eb7-173">La barre d’État est généralement affichée dans le coin inférieur gauche de l’affichage WebView et présente des éléments tels que l’URI d’un lien lorsque l’utilisateur pointe dessus et d’autres informations.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-173">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="d1eb7-174">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-174">It is true by default.</span></span>

#### <span data-ttu-id="d1eb7-175">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-175">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="d1eb7-176">Définissez la propriété IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-176">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="d1eb7-177">[put_IsStatusBarEnabled](#put_isstatusbarenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="d1eb7-177">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="d1eb7-178">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-178">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="d1eb7-179">AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-179">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="d1eb7-180">valeur publique HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="d1eb7-180">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="d1eb7-181">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-181">It is true by default.</span></span>

#### <span data-ttu-id="d1eb7-182">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-182">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="d1eb7-183">Définissez la propriété AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-183">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="d1eb7-184">[put_AreDevToolsEnabled](#put_aredevtoolsenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="d1eb7-184">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

#### <span data-ttu-id="d1eb7-185">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-185">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="d1eb7-186">La propriété AreDefaultContextMenusEnabled est utilisée pour empêcher l’affichage des menus contextuels par défaut pour les utilisateurs dans WebView.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-186">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="d1eb7-187">[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)publique HRESULT (bool \* activé)</span><span class="sxs-lookup"><span data-stu-id="d1eb7-187">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="d1eb7-188">Par défaut, la valeur est TRUE.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-188">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="d1eb7-189">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-189">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="d1eb7-190">Définissez la propriété AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-190">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="d1eb7-191">[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)publiques HRESULT</span><span class="sxs-lookup"><span data-stu-id="d1eb7-191">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="d1eb7-192">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="d1eb7-192">get_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="d1eb7-193">La propriété AreRemoteObjectsAllowed est utilisée pour contrôler si les objets distants sont accessibles à partir de la page dans WebView.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-193">The AreRemoteObjectsAllowed property is used to control whether remote objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="d1eb7-194">valeur publique HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(bool \* autorisé)</span><span class="sxs-lookup"><span data-stu-id="d1eb7-194">public HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(BOOL \* allowed)</span></span>

<span data-ttu-id="d1eb7-195">Par défaut, la valeur est TRUE.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-195">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="d1eb7-196">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="d1eb7-196">put_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="d1eb7-197">Définissez la propriété AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-197">Set the AreRemoteObjectsAllowed property.</span></span>

> <span data-ttu-id="d1eb7-198">[put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)publiques HRESULT</span><span class="sxs-lookup"><span data-stu-id="d1eb7-198">public HRESULT [put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)(BOOL allowed)</span></span>

#### <span data-ttu-id="d1eb7-199">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-199">get_IsZoomControlEnabled</span></span> 

<span data-ttu-id="d1eb7-200">La propriété IsZoomControlEnabled est utilisée pour empêcher l’utilisateur d’influer sur le zoom du WebView.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-200">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="d1eb7-201">[get_IsZoomControlEnabled](#get_iszoomcontrolenabled)publique HRESULT (bool \* activé)</span><span class="sxs-lookup"><span data-stu-id="d1eb7-201">public HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="d1eb7-202">Par défaut, la valeur est TRUE.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-202">Defaults to TRUE.</span></span> <span data-ttu-id="d1eb7-203">Lorsqu’il est désactivé, l’utilisateur ne peut pas effectuer un zoom à l’aide de Ctrl +/-ou Ctrl + molette, mais le zoom peut être défini via une API de put_ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-203">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via put_ZoomFactor API.</span></span>

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

#### <span data-ttu-id="d1eb7-204">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="d1eb7-204">put_IsZoomControlEnabled</span></span> 

<span data-ttu-id="d1eb7-205">Définissez la propriété IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="d1eb7-205">Set the IsZoomControlEnabled property.</span></span>

> <span data-ttu-id="d1eb7-206">[put_IsZoomControlEnabled](#put_iszoomcontrolenabled)publiques HRESULT</span><span class="sxs-lookup"><span data-stu-id="d1eb7-206">public HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(BOOL enabled)</span></span>

