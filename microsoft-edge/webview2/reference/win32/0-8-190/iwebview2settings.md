---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 649506b28e0ecdbff33b44bbd8010ddb3d2a66b0
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885799"
---
# <span data-ttu-id="d0e35-104">0.8.355-interface IWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="d0e35-104">0.8.355 - interface IWebView2Settings</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Settings
  : public IUnknown
```

<span data-ttu-id="d0e35-105">Définit les propriétés permettant, de désactiver ou de modifier les fonctionnalités WebView.</span><span class="sxs-lookup"><span data-stu-id="d0e35-105">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="d0e35-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="d0e35-106">Summary</span></span>

 <span data-ttu-id="d0e35-107">Ses</span><span class="sxs-lookup"><span data-stu-id="d0e35-107">Members</span></span>                        | <span data-ttu-id="d0e35-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="d0e35-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d0e35-109">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="d0e35-109">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="d0e35-110">Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.</span><span class="sxs-lookup"><span data-stu-id="d0e35-110">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="d0e35-111">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="d0e35-111">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="d0e35-112">Définissez la propriété IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="d0e35-112">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="d0e35-113">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="d0e35-113">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="d0e35-114">La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="d0e35-114">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="d0e35-115">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="d0e35-115">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="d0e35-116">Définissez la propriété IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="d0e35-116">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="d0e35-117">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="d0e35-117">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="d0e35-118">AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="d0e35-118">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="d0e35-119">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="d0e35-119">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="d0e35-120">Définissez la propriété AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="d0e35-120">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="d0e35-121">get_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="d0e35-121">get_IsFullscreenAllowed_deprecated</span></span>](#get_isfullscreenallowed_deprecated) | <span data-ttu-id="d0e35-122">Ce paramètre est déconseillé et renverra toujours false.</span><span class="sxs-lookup"><span data-stu-id="d0e35-122">This setting is deprecated and will always return false.</span></span>
[<span data-ttu-id="d0e35-123">put_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="d0e35-123">put_IsFullscreenAllowed_deprecated</span></span>](#put_isfullscreenallowed_deprecated) | <span data-ttu-id="d0e35-124">Ce paramètre est déconseillé et n’aura aucun effet.</span><span class="sxs-lookup"><span data-stu-id="d0e35-124">This setting is deprecated and will have no effect.</span></span>
[<span data-ttu-id="d0e35-125">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="d0e35-125">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="d0e35-126">IsStatusBarEnabled vérifie si la barre d’État s’affiche.</span><span class="sxs-lookup"><span data-stu-id="d0e35-126">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="d0e35-127">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="d0e35-127">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="d0e35-128">Définissez la propriété IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="d0e35-128">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="d0e35-129">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="d0e35-129">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="d0e35-130">AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="d0e35-130">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="d0e35-131">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="d0e35-131">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="d0e35-132">Définissez la propriété AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="d0e35-132">Set the AreDevToolsEnabled property.</span></span>

<span data-ttu-id="d0e35-133">Les modifications apportées après l’événement NavigationStarting ne s’appliquent pas tant que la navigation de niveau supérieur suivante n’est pas appliquée.</span><span class="sxs-lookup"><span data-stu-id="d0e35-133">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="d0e35-134">Ses</span><span class="sxs-lookup"><span data-stu-id="d0e35-134">Members</span></span>

#### <span data-ttu-id="d0e35-135">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="d0e35-135">get_IsScriptEnabled</span></span> 

<span data-ttu-id="d0e35-136">Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.</span><span class="sxs-lookup"><span data-stu-id="d0e35-136">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="d0e35-137">valeur publique HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="d0e35-137">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="d0e35-138">Cela ne concerne que les scripts du document. les scripts injectés avec ExecuteScript s’exécutent même si le script est désactivé.</span><span class="sxs-lookup"><span data-stu-id="d0e35-138">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="d0e35-139">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="d0e35-139">It is true by default.</span></span>

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

#### <span data-ttu-id="d0e35-140">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="d0e35-140">put_IsScriptEnabled</span></span> 

<span data-ttu-id="d0e35-141">Définissez la propriété IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="d0e35-141">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="d0e35-142">[put_IsScriptEnabled](#put_isscriptenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="d0e35-142">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="d0e35-143">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="d0e35-143">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="d0e35-144">La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="d0e35-144">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="d0e35-145">valeur publique HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="d0e35-145">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="d0e35-146">Si elle a la valeur true, la communication de l’hôte vers le document HTML de niveau supérieur de l’hôte est autorisée via PostWebMessageAsJson, PostWebMessageAsString et Window. chrome. événement de message (voir la documentation PostWebMessageAsJson pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="d0e35-146">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="d0e35-147">La communication du document HTML de niveau supérieur d’un WebView à l’hôte est autorisée via la fonction postMessage de Window. chrome. WebView et la méthode SetWebMessageReceivedEventHandler (voir la documentation SetWebMessageReceivedEventHandler pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="d0e35-147">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="d0e35-148">Si elle est définie sur false, la communication n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="d0e35-148">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="d0e35-149">PostWebMessageAsJson et PostWebMessageAsString échoueront avec E_ACCESSDENIED et Window. chrome. WebView. postMessage échoue en levant une instance d’objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d0e35-149">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="d0e35-150">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="d0e35-150">It is true by default.</span></span>

```cpp
    ComPtr<IWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="d0e35-151">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="d0e35-151">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="d0e35-152">Définissez la propriété IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="d0e35-152">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="d0e35-153">[put_IsWebMessageEnabled](#put_iswebmessageenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="d0e35-153">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="d0e35-154">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="d0e35-154">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="d0e35-155">AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="d0e35-155">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="d0e35-156">valeur publique HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="d0e35-156">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="d0e35-157">Si cette valeur est définie sur false, le WebView n’affichera pas la boîte de dialogue JavaScript par défaut (en particulier, les fonctions d’alerte, de confirmation et de confirmation JavaScript).</span><span class="sxs-lookup"><span data-stu-id="d0e35-157">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, and prompt functions).</span></span> <span data-ttu-id="d0e35-158">Au lieu de cela, si un gestionnaire d’événements est défini par SetScriptDialogOpeningEventHandler, WebView envoie un événement qui contient toutes les informations pour la boîte de dialogue et autorise l’application hôte à afficher sa propre interface utilisateur personnalisée.</span><span class="sxs-lookup"><span data-stu-id="d0e35-158">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="d0e35-159">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="d0e35-159">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="d0e35-160">Définissez la propriété AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="d0e35-160">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="d0e35-161">[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="d0e35-161">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="d0e35-162">get_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="d0e35-162">get_IsFullscreenAllowed_deprecated</span></span> 

<span data-ttu-id="d0e35-163">Ce paramètre est déconseillé et renverra toujours false.</span><span class="sxs-lookup"><span data-stu-id="d0e35-163">This setting is deprecated and will always return false.</span></span>

> <span data-ttu-id="d0e35-164">valeur publique HRESULT [get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)(bool \* IsFullscreenAllowed)</span><span class="sxs-lookup"><span data-stu-id="d0e35-164">public HRESULT [get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)(BOOL \* isFullscreenAllowed)</span></span>

<span data-ttu-id="d0e35-165">Cela signifie que les éléments du WebView ne remplissent que les limites de la WebView.</span><span class="sxs-lookup"><span data-stu-id="d0e35-165">That means elements in the WebView will only fill the WebView bounds.</span></span> <span data-ttu-id="d0e35-166">Cette propriété sera alors entièrement supprimée.</span><span class="sxs-lookup"><span data-stu-id="d0e35-166">This property will then be completely removed.</span></span> <span data-ttu-id="d0e35-167">À la place, écoutez l’événement ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="d0e35-167">Please listen to the ContainsFullScreenElementChanged event instead.</span></span>

<span data-ttu-id="d0e35-168">Détermine si la commande plein écran est autorisée pour les éléments du WebView.</span><span class="sxs-lookup"><span data-stu-id="d0e35-168">Controls if fullscreen is allowed for elements in the WebView.</span></span> <span data-ttu-id="d0e35-169">Lorsqu’il est autorisé, le contenu Web tel qu’un élément vidéo dans le WebView est autorisé à s’afficher en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="d0e35-169">When it is allowed, web content such as a video element in the WebView is allowed to be displayed full screen.</span></span> <span data-ttu-id="d0e35-170">Lorsqu’il n’est pas autorisé, ce type d’élément remplit les limites du WebView lorsque l’élément est demandé en plein écran.</span><span class="sxs-lookup"><span data-stu-id="d0e35-170">When it is not allowed, such element will fill the WebView bounds when the element requests full screen.</span></span> <span data-ttu-id="d0e35-171">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="d0e35-171">It is true by default.</span></span>

#### <span data-ttu-id="d0e35-172">put_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="d0e35-172">put_IsFullscreenAllowed_deprecated</span></span> 

<span data-ttu-id="d0e35-173">Ce paramètre est déconseillé et n’aura aucun effet.</span><span class="sxs-lookup"><span data-stu-id="d0e35-173">This setting is deprecated and will have no effect.</span></span>

> <span data-ttu-id="d0e35-174">[put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="d0e35-174">public HRESULT [put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)(BOOL isFullscreenAllowed)</span></span>

<span data-ttu-id="d0e35-175">À la place, écoutez l’événement ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="d0e35-175">Please listen to the ContainsFullScreenElementChanged event instead.</span></span>

<span data-ttu-id="d0e35-176">Définissez la propriété IsFullscreenAllowed.</span><span class="sxs-lookup"><span data-stu-id="d0e35-176">Set the IsFullscreenAllowed property.</span></span>

#### <span data-ttu-id="d0e35-177">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="d0e35-177">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="d0e35-178">IsStatusBarEnabled vérifie si la barre d’État s’affiche.</span><span class="sxs-lookup"><span data-stu-id="d0e35-178">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="d0e35-179">valeur publique HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="d0e35-179">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="d0e35-180">La barre d’État est généralement affichée dans le coin inférieur gauche de l’affichage WebView et présente des éléments tels que l’URI d’un lien lorsque l’utilisateur pointe dessus et d’autres informations.</span><span class="sxs-lookup"><span data-stu-id="d0e35-180">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="d0e35-181">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="d0e35-181">It is true by default.</span></span>

#### <span data-ttu-id="d0e35-182">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="d0e35-182">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="d0e35-183">Définissez la propriété IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="d0e35-183">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="d0e35-184">[put_IsStatusBarEnabled](#put_isstatusbarenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="d0e35-184">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="d0e35-185">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="d0e35-185">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="d0e35-186">AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="d0e35-186">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="d0e35-187">valeur publique HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="d0e35-187">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="d0e35-188">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="d0e35-188">It is true by default.</span></span>

#### <span data-ttu-id="d0e35-189">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="d0e35-189">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="d0e35-190">Définissez la propriété AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="d0e35-190">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="d0e35-191">[put_AreDevToolsEnabled](#put_aredevtoolsenabled)de passe par le public HRESULT</span><span class="sxs-lookup"><span data-stu-id="d0e35-191">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

