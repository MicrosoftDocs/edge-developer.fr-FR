---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 3c799e97f8e85927e1c11b30be747d7649faeca0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653400"
---
# <span data-ttu-id="49d94-104">interface IWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="49d94-104">interface IWebView2Settings</span></span> 

> [!NOTE]
> <span data-ttu-id="49d94-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="49d94-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="49d94-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="49d94-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Settings
  : public IUnknown
```

<span data-ttu-id="49d94-107">Définit les propriétés permettant, de désactiver ou de modifier les fonctionnalités WebView.</span><span class="sxs-lookup"><span data-stu-id="49d94-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="49d94-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="49d94-108">Summary</span></span>

 <span data-ttu-id="49d94-109">Ses</span><span class="sxs-lookup"><span data-stu-id="49d94-109">Members</span></span>                        | <span data-ttu-id="49d94-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="49d94-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="49d94-111">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="49d94-111">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="49d94-112">Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.</span><span class="sxs-lookup"><span data-stu-id="49d94-112">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="49d94-113">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="49d94-113">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="49d94-114">Définissez la propriété IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="49d94-114">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="49d94-115">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="49d94-115">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="49d94-116">La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="49d94-116">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="49d94-117">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="49d94-117">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="49d94-118">Définissez la propriété IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="49d94-118">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="49d94-119">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="49d94-119">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="49d94-120">AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="49d94-120">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="49d94-121">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="49d94-121">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="49d94-122">Définissez la propriété AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="49d94-122">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="49d94-123">get_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="49d94-123">get_IsFullscreenAllowed_deprecated</span></span>](#get_isfullscreenallowed_deprecated) | <span data-ttu-id="49d94-124">Ce paramètre est déconseillé et renverra toujours false.</span><span class="sxs-lookup"><span data-stu-id="49d94-124">This setting is deprecated and will always return false.</span></span>
[<span data-ttu-id="49d94-125">put_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="49d94-125">put_IsFullscreenAllowed_deprecated</span></span>](#put_isfullscreenallowed_deprecated) | <span data-ttu-id="49d94-126">Ce paramètre est déconseillé et n’aura aucun effet.</span><span class="sxs-lookup"><span data-stu-id="49d94-126">This setting is deprecated and will have no effect.</span></span>
[<span data-ttu-id="49d94-127">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="49d94-127">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="49d94-128">IsStatusBarEnabled vérifie si la barre d’État s’affiche.</span><span class="sxs-lookup"><span data-stu-id="49d94-128">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="49d94-129">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="49d94-129">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="49d94-130">Définissez la propriété IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="49d94-130">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="49d94-131">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="49d94-131">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="49d94-132">AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="49d94-132">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="49d94-133">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="49d94-133">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="49d94-134">Définissez la propriété AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="49d94-134">Set the AreDevToolsEnabled property.</span></span>

<span data-ttu-id="49d94-135">Les modifications apportées après l’événement NavigationStarting ne s’appliquent pas tant que la navigation de niveau supérieur suivante n’est pas appliquée.</span><span class="sxs-lookup"><span data-stu-id="49d94-135">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="49d94-136">Ses</span><span class="sxs-lookup"><span data-stu-id="49d94-136">Members</span></span>

#### <span data-ttu-id="49d94-137">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="49d94-137">get_IsScriptEnabled</span></span> 

<span data-ttu-id="49d94-138">Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.</span><span class="sxs-lookup"><span data-stu-id="49d94-138">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="49d94-139">valeur publique HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="49d94-139">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="49d94-140">Cela ne concerne que les scripts du document. les scripts injectés avec ExecuteScript s’exécutent même si le script est désactivé.</span><span class="sxs-lookup"><span data-stu-id="49d94-140">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="49d94-141">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="49d94-141">It is true by default.</span></span>

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

#### <span data-ttu-id="49d94-142">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="49d94-142">put_IsScriptEnabled</span></span> 

<span data-ttu-id="49d94-143">Définissez la propriété IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="49d94-143">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="49d94-144">[put_IsScriptEnabled](#put_isscriptenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="49d94-144">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="49d94-145">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="49d94-145">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="49d94-146">La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="49d94-146">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="49d94-147">valeur publique HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="49d94-147">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="49d94-148">Si elle a la valeur true, la communication de l’hôte vers le document HTML de niveau supérieur de l’hôte est autorisée via PostWebMessageAsJson, PostWebMessageAsString et Window. chrome. événement de message (voir la documentation PostWebMessageAsJson pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="49d94-148">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="49d94-149">La communication du document HTML de niveau supérieur d’un WebView à l’hôte est autorisée via la fonction postMessage de Window. chrome. WebView et la méthode SetWebMessageReceivedEventHandler (voir la documentation SetWebMessageReceivedEventHandler pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="49d94-149">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="49d94-150">Si elle est définie sur false, la communication n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="49d94-150">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="49d94-151">PostWebMessageAsJson et PostWebMessageAsString échoueront avec E_ACCESSDENIED et Window. chrome. WebView. postMessage échoue en levant une instance d’objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="49d94-151">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="49d94-152">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="49d94-152">It is true by default.</span></span>

```cpp
    ComPtr<IWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="49d94-153">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="49d94-153">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="49d94-154">Définissez la propriété IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="49d94-154">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="49d94-155">[put_IsWebMessageEnabled](#put_iswebmessageenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="49d94-155">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="49d94-156">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="49d94-156">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="49d94-157">AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="49d94-157">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="49d94-158">valeur publique HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="49d94-158">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="49d94-159">Si cette valeur est définie sur false, le WebView n’affichera pas la boîte de dialogue JavaScript par défaut (en particulier, les fonctions d’alerte, de confirmation et de confirmation JavaScript).</span><span class="sxs-lookup"><span data-stu-id="49d94-159">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, and prompt functions).</span></span> <span data-ttu-id="49d94-160">Au lieu de cela, si un gestionnaire d’événements est défini par SetScriptDialogOpeningEventHandler, WebView envoie un événement qui contient toutes les informations pour la boîte de dialogue et autorise l’application hôte à afficher sa propre interface utilisateur personnalisée.</span><span class="sxs-lookup"><span data-stu-id="49d94-160">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="49d94-161">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="49d94-161">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="49d94-162">Définissez la propriété AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="49d94-162">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="49d94-163">[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="49d94-163">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="49d94-164">get_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="49d94-164">get_IsFullscreenAllowed_deprecated</span></span> 

<span data-ttu-id="49d94-165">Ce paramètre est déconseillé et renverra toujours false.</span><span class="sxs-lookup"><span data-stu-id="49d94-165">This setting is deprecated and will always return false.</span></span>

> <span data-ttu-id="49d94-166">valeur publique HRESULT [get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)(bool \* IsFullscreenAllowed)</span><span class="sxs-lookup"><span data-stu-id="49d94-166">public HRESULT [get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)(BOOL \* isFullscreenAllowed)</span></span>

<span data-ttu-id="49d94-167">Cela signifie que les éléments du WebView ne remplissent que les limites de la WebView.</span><span class="sxs-lookup"><span data-stu-id="49d94-167">That means elements in the WebView will only fill the WebView bounds.</span></span> <span data-ttu-id="49d94-168">Cette propriété sera alors entièrement supprimée.</span><span class="sxs-lookup"><span data-stu-id="49d94-168">This property will then be completely removed.</span></span> <span data-ttu-id="49d94-169">À la place, écoutez l’événement ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="49d94-169">Please listen to the ContainsFullScreenElementChanged event instead.</span></span>

<span data-ttu-id="49d94-170">Détermine si la commande plein écran est autorisée pour les éléments du WebView.</span><span class="sxs-lookup"><span data-stu-id="49d94-170">Controls if fullscreen is allowed for elements in the WebView.</span></span> <span data-ttu-id="49d94-171">Lorsqu’il est autorisé, le contenu Web tel qu’un élément vidéo dans le WebView est autorisé à s’afficher en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="49d94-171">When it is allowed, web content such as a video element in the WebView is allowed to be displayed full screen.</span></span> <span data-ttu-id="49d94-172">Lorsqu’il n’est pas autorisé, ce type d’élément remplit les limites du WebView lorsque l’élément est demandé en plein écran.</span><span class="sxs-lookup"><span data-stu-id="49d94-172">When it is not allowed, such element will fill the WebView bounds when the element requests full screen.</span></span> <span data-ttu-id="49d94-173">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="49d94-173">It is true by default.</span></span>

#### <span data-ttu-id="49d94-174">put_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="49d94-174">put_IsFullscreenAllowed_deprecated</span></span> 

<span data-ttu-id="49d94-175">Ce paramètre est déconseillé et n’aura aucun effet.</span><span class="sxs-lookup"><span data-stu-id="49d94-175">This setting is deprecated and will have no effect.</span></span>

> <span data-ttu-id="49d94-176">[put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="49d94-176">public HRESULT [put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)(BOOL isFullscreenAllowed)</span></span>

<span data-ttu-id="49d94-177">À la place, écoutez l’événement ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="49d94-177">Please listen to the ContainsFullScreenElementChanged event instead.</span></span>

<span data-ttu-id="49d94-178">Définissez la propriété IsFullscreenAllowed.</span><span class="sxs-lookup"><span data-stu-id="49d94-178">Set the IsFullscreenAllowed property.</span></span>

#### <span data-ttu-id="49d94-179">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="49d94-179">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="49d94-180">IsStatusBarEnabled vérifie si la barre d’État s’affiche.</span><span class="sxs-lookup"><span data-stu-id="49d94-180">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="49d94-181">valeur publique HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="49d94-181">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="49d94-182">La barre d’État est généralement affichée dans le coin inférieur gauche de l’affichage WebView et présente des éléments tels que l’URI d’un lien lorsque l’utilisateur pointe dessus et d’autres informations.</span><span class="sxs-lookup"><span data-stu-id="49d94-182">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="49d94-183">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="49d94-183">It is true by default.</span></span>

#### <span data-ttu-id="49d94-184">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="49d94-184">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="49d94-185">Définissez la propriété IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="49d94-185">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="49d94-186">[put_IsStatusBarEnabled](#put_isstatusbarenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="49d94-186">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="49d94-187">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="49d94-187">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="49d94-188">AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="49d94-188">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="49d94-189">valeur publique HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="49d94-189">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="49d94-190">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="49d94-190">It is true by default.</span></span>

#### <span data-ttu-id="49d94-191">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="49d94-191">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="49d94-192">Définissez la propriété AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="49d94-192">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="49d94-193">[put_AreDevToolsEnabled](#put_aredevtoolsenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="49d94-193">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

