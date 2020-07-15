---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 94c6d6c424d715d3b6b57b366b71cf8e5fb8ec42
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878210"
---
# <span data-ttu-id="e1918-104">0.8.355-interface IWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="e1918-104">0.8.355 - interface IWebView2Settings</span></span> 

> [!NOTE]
> <span data-ttu-id="e1918-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="e1918-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="e1918-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="e1918-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Settings
  : public IUnknown
```

<span data-ttu-id="e1918-107">Définit les propriétés permettant, de désactiver ou de modifier les fonctionnalités WebView.</span><span class="sxs-lookup"><span data-stu-id="e1918-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="e1918-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="e1918-108">Summary</span></span>

 <span data-ttu-id="e1918-109">Ses</span><span class="sxs-lookup"><span data-stu-id="e1918-109">Members</span></span>                        | <span data-ttu-id="e1918-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="e1918-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e1918-111">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="e1918-111">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="e1918-112">Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.</span><span class="sxs-lookup"><span data-stu-id="e1918-112">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="e1918-113">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="e1918-113">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="e1918-114">Définissez la propriété IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="e1918-114">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="e1918-115">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="e1918-115">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="e1918-116">La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="e1918-116">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="e1918-117">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="e1918-117">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="e1918-118">Définissez la propriété IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="e1918-118">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="e1918-119">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="e1918-119">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="e1918-120">AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="e1918-120">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="e1918-121">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="e1918-121">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="e1918-122">Définissez la propriété AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="e1918-122">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="e1918-123">get_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="e1918-123">get_IsFullscreenAllowed_deprecated</span></span>](#get_isfullscreenallowed_deprecated) | <span data-ttu-id="e1918-124">Ce paramètre est déconseillé et renverra toujours false.</span><span class="sxs-lookup"><span data-stu-id="e1918-124">This setting is deprecated and will always return false.</span></span>
[<span data-ttu-id="e1918-125">put_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="e1918-125">put_IsFullscreenAllowed_deprecated</span></span>](#put_isfullscreenallowed_deprecated) | <span data-ttu-id="e1918-126">Ce paramètre est déconseillé et n’aura aucun effet.</span><span class="sxs-lookup"><span data-stu-id="e1918-126">This setting is deprecated and will have no effect.</span></span>
[<span data-ttu-id="e1918-127">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="e1918-127">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="e1918-128">IsStatusBarEnabled vérifie si la barre d’État s’affiche.</span><span class="sxs-lookup"><span data-stu-id="e1918-128">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="e1918-129">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="e1918-129">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="e1918-130">Définissez la propriété IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="e1918-130">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="e1918-131">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="e1918-131">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="e1918-132">AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="e1918-132">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="e1918-133">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="e1918-133">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="e1918-134">Définissez la propriété AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="e1918-134">Set the AreDevToolsEnabled property.</span></span>

<span data-ttu-id="e1918-135">Les modifications apportées après l’événement NavigationStarting ne s’appliquent pas tant que la navigation de niveau supérieur suivante n’est pas appliquée.</span><span class="sxs-lookup"><span data-stu-id="e1918-135">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="e1918-136">Ses</span><span class="sxs-lookup"><span data-stu-id="e1918-136">Members</span></span>

#### <span data-ttu-id="e1918-137">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="e1918-137">get_IsScriptEnabled</span></span> 

<span data-ttu-id="e1918-138">Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.</span><span class="sxs-lookup"><span data-stu-id="e1918-138">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="e1918-139">valeur publique HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="e1918-139">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="e1918-140">Cela ne concerne que les scripts du document. les scripts injectés avec ExecuteScript s’exécutent même si le script est désactivé.</span><span class="sxs-lookup"><span data-stu-id="e1918-140">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="e1918-141">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="e1918-141">It is true by default.</span></span>

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

#### <span data-ttu-id="e1918-142">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="e1918-142">put_IsScriptEnabled</span></span> 

<span data-ttu-id="e1918-143">Définissez la propriété IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="e1918-143">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="e1918-144">[put_IsScriptEnabled](#put_isscriptenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="e1918-144">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="e1918-145">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="e1918-145">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="e1918-146">La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="e1918-146">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="e1918-147">valeur publique HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="e1918-147">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="e1918-148">Si elle a la valeur true, la communication de l’hôte vers le document HTML de niveau supérieur de l’hôte est autorisée via PostWebMessageAsJson, PostWebMessageAsString et Window. chrome. événement de message (voir la documentation PostWebMessageAsJson pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="e1918-148">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="e1918-149">La communication du document HTML de niveau supérieur d’un WebView à l’hôte est autorisée via la fonction postMessage de Window. chrome. WebView et la méthode SetWebMessageReceivedEventHandler (voir la documentation SetWebMessageReceivedEventHandler pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="e1918-149">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="e1918-150">Si elle est définie sur false, la communication n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="e1918-150">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="e1918-151">PostWebMessageAsJson et PostWebMessageAsString échoueront avec E_ACCESSDENIED et Window. chrome. WebView. postMessage échoue en levant une instance d’objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e1918-151">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="e1918-152">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="e1918-152">It is true by default.</span></span>

```cpp
    ComPtr<IWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="e1918-153">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="e1918-153">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="e1918-154">Définissez la propriété IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="e1918-154">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="e1918-155">[put_IsWebMessageEnabled](#put_iswebmessageenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="e1918-155">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="e1918-156">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="e1918-156">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="e1918-157">AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="e1918-157">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="e1918-158">valeur publique HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="e1918-158">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="e1918-159">Si cette valeur est définie sur false, le WebView n’affichera pas la boîte de dialogue JavaScript par défaut (en particulier, les fonctions d’alerte, de confirmation et de confirmation JavaScript).</span><span class="sxs-lookup"><span data-stu-id="e1918-159">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, and prompt functions).</span></span> <span data-ttu-id="e1918-160">Au lieu de cela, si un gestionnaire d’événements est défini par SetScriptDialogOpeningEventHandler, WebView envoie un événement qui contient toutes les informations pour la boîte de dialogue et autorise l’application hôte à afficher sa propre interface utilisateur personnalisée.</span><span class="sxs-lookup"><span data-stu-id="e1918-160">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="e1918-161">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="e1918-161">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="e1918-162">Définissez la propriété AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="e1918-162">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="e1918-163">[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="e1918-163">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="e1918-164">get_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="e1918-164">get_IsFullscreenAllowed_deprecated</span></span> 

<span data-ttu-id="e1918-165">Ce paramètre est déconseillé et renverra toujours false.</span><span class="sxs-lookup"><span data-stu-id="e1918-165">This setting is deprecated and will always return false.</span></span>

> <span data-ttu-id="e1918-166">valeur publique HRESULT [get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)(bool \* IsFullscreenAllowed)</span><span class="sxs-lookup"><span data-stu-id="e1918-166">public HRESULT [get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)(BOOL \* isFullscreenAllowed)</span></span>

<span data-ttu-id="e1918-167">Cela signifie que les éléments du WebView ne remplissent que les limites de la WebView.</span><span class="sxs-lookup"><span data-stu-id="e1918-167">That means elements in the WebView will only fill the WebView bounds.</span></span> <span data-ttu-id="e1918-168">Cette propriété sera alors entièrement supprimée.</span><span class="sxs-lookup"><span data-stu-id="e1918-168">This property will then be completely removed.</span></span> <span data-ttu-id="e1918-169">À la place, écoutez l’événement ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="e1918-169">Please listen to the ContainsFullScreenElementChanged event instead.</span></span>

<span data-ttu-id="e1918-170">Détermine si la commande plein écran est autorisée pour les éléments du WebView.</span><span class="sxs-lookup"><span data-stu-id="e1918-170">Controls if fullscreen is allowed for elements in the WebView.</span></span> <span data-ttu-id="e1918-171">Lorsqu’il est autorisé, le contenu Web tel qu’un élément vidéo dans le WebView est autorisé à s’afficher en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="e1918-171">When it is allowed, web content such as a video element in the WebView is allowed to be displayed full screen.</span></span> <span data-ttu-id="e1918-172">Lorsqu’il n’est pas autorisé, ce type d’élément remplit les limites du WebView lorsque l’élément est demandé en plein écran.</span><span class="sxs-lookup"><span data-stu-id="e1918-172">When it is not allowed, such element will fill the WebView bounds when the element requests full screen.</span></span> <span data-ttu-id="e1918-173">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="e1918-173">It is true by default.</span></span>

#### <span data-ttu-id="e1918-174">put_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="e1918-174">put_IsFullscreenAllowed_deprecated</span></span> 

<span data-ttu-id="e1918-175">Ce paramètre est déconseillé et n’aura aucun effet.</span><span class="sxs-lookup"><span data-stu-id="e1918-175">This setting is deprecated and will have no effect.</span></span>

> <span data-ttu-id="e1918-176">[put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="e1918-176">public HRESULT [put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)(BOOL isFullscreenAllowed)</span></span>

<span data-ttu-id="e1918-177">À la place, écoutez l’événement ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="e1918-177">Please listen to the ContainsFullScreenElementChanged event instead.</span></span>

<span data-ttu-id="e1918-178">Définissez la propriété IsFullscreenAllowed.</span><span class="sxs-lookup"><span data-stu-id="e1918-178">Set the IsFullscreenAllowed property.</span></span>

#### <span data-ttu-id="e1918-179">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="e1918-179">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="e1918-180">IsStatusBarEnabled vérifie si la barre d’État s’affiche.</span><span class="sxs-lookup"><span data-stu-id="e1918-180">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="e1918-181">valeur publique HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="e1918-181">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="e1918-182">La barre d’État est généralement affichée dans le coin inférieur gauche de l’affichage WebView et présente des éléments tels que l’URI d’un lien lorsque l’utilisateur pointe dessus et d’autres informations.</span><span class="sxs-lookup"><span data-stu-id="e1918-182">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="e1918-183">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="e1918-183">It is true by default.</span></span>

#### <span data-ttu-id="e1918-184">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="e1918-184">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="e1918-185">Définissez la propriété IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="e1918-185">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="e1918-186">[put_IsStatusBarEnabled](#put_isstatusbarenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="e1918-186">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="e1918-187">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="e1918-187">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="e1918-188">AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="e1918-188">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="e1918-189">valeur publique HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="e1918-189">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="e1918-190">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="e1918-190">It is true by default.</span></span>

#### <span data-ttu-id="e1918-191">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="e1918-191">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="e1918-192">Définissez la propriété AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="e1918-192">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="e1918-193">[put_AreDevToolsEnabled](#put_aredevtoolsenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="e1918-193">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

