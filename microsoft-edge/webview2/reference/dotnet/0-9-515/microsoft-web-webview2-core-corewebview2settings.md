---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 6adc494c63d0bd7adc2fd578fcb877e0bf75307f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879365"
---
# <span data-ttu-id="f85b7-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="f85b7-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2Settings class</span></span> 

> [!NOTE]
> <span data-ttu-id="f85b7-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="f85b7-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="f85b7-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="f85b7-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="f85b7-107">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="f85b7-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="f85b7-108">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="f85b7-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="f85b7-109">Définit les propriétés permettant, de désactiver ou de modifier les fonctionnalités WebView.</span><span class="sxs-lookup"><span data-stu-id="f85b7-109">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="f85b7-110">Résumé</span><span class="sxs-lookup"><span data-stu-id="f85b7-110">Summary</span></span>

 <span data-ttu-id="f85b7-111">Ses</span><span class="sxs-lookup"><span data-stu-id="f85b7-111">Members</span></span>                        | <span data-ttu-id="f85b7-112">Descriptions</span><span class="sxs-lookup"><span data-stu-id="f85b7-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f85b7-113">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="f85b7-113">AreDefaultContextMenusEnabled</span></span>](#aredefaultcontextmenusenabled) | <span data-ttu-id="f85b7-114">La propriété AreDefaultContextMenusEnabled est utilisée pour empêcher l’affichage des menus contextuels par défaut pour les utilisateurs dans WebView.</span><span class="sxs-lookup"><span data-stu-id="f85b7-114">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="f85b7-115">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="f85b7-115">AreDefaultScriptDialogsEnabled</span></span>](#aredefaultscriptdialogsenabled) | <span data-ttu-id="f85b7-116">AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="f85b7-116">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="f85b7-117">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="f85b7-117">AreDevToolsEnabled</span></span>](#aredevtoolsenabled) | <span data-ttu-id="f85b7-118">AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="f85b7-118">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="f85b7-119">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="f85b7-119">AreHostObjectsAllowed</span></span>](#arehostobjectsallowed) | <span data-ttu-id="f85b7-120">La propriété AreHostObjectsAllowed est utilisée pour contrôler si les objets hôtes sont accessibles à partir de la page dans WebView.</span><span class="sxs-lookup"><span data-stu-id="f85b7-120">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="f85b7-121">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="f85b7-121">IsBuiltInErrorPageEnabled</span></span>](#isbuiltinerrorpageenabled) | <span data-ttu-id="f85b7-122">La propriété IsBuiltInErrorPageEnabled est utilisée pour désactiver la page d’erreur intégrée à un échec de navigation et un échec de processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="f85b7-122">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="f85b7-123">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="f85b7-123">IsScriptEnabled</span></span>](#isscriptenabled) | <span data-ttu-id="f85b7-124">Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.</span><span class="sxs-lookup"><span data-stu-id="f85b7-124">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="f85b7-125">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="f85b7-125">IsStatusBarEnabled</span></span>](#isstatusbarenabled) | <span data-ttu-id="f85b7-126">IsStatusBarEnabled vérifie si la barre d’État s’affiche.</span><span class="sxs-lookup"><span data-stu-id="f85b7-126">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="f85b7-127">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="f85b7-127">IsWebMessageEnabled</span></span>](#iswebmessageenabled) | <span data-ttu-id="f85b7-128">La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="f85b7-128">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="f85b7-129">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="f85b7-129">IsZoomControlEnabled</span></span>](#iszoomcontrolenabled) | <span data-ttu-id="f85b7-130">La propriété IsZoomControlEnabled est utilisée pour empêcher l’utilisateur d’influer sur le zoom du WebView.</span><span class="sxs-lookup"><span data-stu-id="f85b7-130">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

<span data-ttu-id="f85b7-131">Les modifications apportées après l’événement NavigationStarting ne s’appliquent pas tant que la navigation de niveau supérieur suivante n’est pas appliquée.</span><span class="sxs-lookup"><span data-stu-id="f85b7-131">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="f85b7-132">Ses</span><span class="sxs-lookup"><span data-stu-id="f85b7-132">Members</span></span>

#### <span data-ttu-id="f85b7-133">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="f85b7-133">AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="f85b7-134">La propriété AreDefaultContextMenusEnabled est utilisée pour empêcher l’affichage des menus contextuels par défaut pour les utilisateurs dans WebView.</span><span class="sxs-lookup"><span data-stu-id="f85b7-134">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="f85b7-135">public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span><span class="sxs-lookup"><span data-stu-id="f85b7-135">public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span></span>

<span data-ttu-id="f85b7-136">Par défaut, la valeur est TRUE.</span><span class="sxs-lookup"><span data-stu-id="f85b7-136">Defaults to TRUE.</span></span>

#### <span data-ttu-id="f85b7-137">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="f85b7-137">AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="f85b7-138">AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="f85b7-138">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="f85b7-139">public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span><span class="sxs-lookup"><span data-stu-id="f85b7-139">public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span></span>

<span data-ttu-id="f85b7-140">Si elle a la valeur false, le WebView n’affichera pas la boîte de dialogue JavaScript par défaut (en particulier, celles qui sont affichées par l’alerte JavaScript, les fonctions confirmer, invites et événement beforeunload).</span><span class="sxs-lookup"><span data-stu-id="f85b7-140">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="f85b7-141">Au lieu de cela, si un gestionnaire d’événements est défini par SetScriptDialogOpeningEventHandler, WebView envoie un événement qui contient toutes les informations pour la boîte de dialogue et autorise l’application hôte à afficher sa propre interface utilisateur personnalisée.</span><span class="sxs-lookup"><span data-stu-id="f85b7-141">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="f85b7-142">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="f85b7-142">AreDevToolsEnabled</span></span> 

<span data-ttu-id="f85b7-143">AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="f85b7-143">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="f85b7-144">public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span><span class="sxs-lookup"><span data-stu-id="f85b7-144">public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span></span>

<span data-ttu-id="f85b7-145">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="f85b7-145">It is true by default.</span></span>

#### <span data-ttu-id="f85b7-146">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="f85b7-146">AreHostObjectsAllowed</span></span> 

<span data-ttu-id="f85b7-147">La propriété AreHostObjectsAllowed est utilisée pour contrôler si les objets hôtes sont accessibles à partir de la page dans WebView.</span><span class="sxs-lookup"><span data-stu-id="f85b7-147">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="f85b7-148">public bool [AreHostObjectsAllowed](#arehostobjectsallowed)</span><span class="sxs-lookup"><span data-stu-id="f85b7-148">public bool [AreHostObjectsAllowed](#arehostobjectsallowed)</span></span>

<span data-ttu-id="f85b7-149">Par défaut, la valeur est TRUE.</span><span class="sxs-lookup"><span data-stu-id="f85b7-149">Defaults to TRUE.</span></span>

#### <span data-ttu-id="f85b7-150">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="f85b7-150">IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="f85b7-151">La propriété IsBuiltInErrorPageEnabled est utilisée pour désactiver la page d’erreur intégrée à un échec de navigation et un échec de processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="f85b7-151">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="f85b7-152">public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span><span class="sxs-lookup"><span data-stu-id="f85b7-152">public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span></span>

<span data-ttu-id="f85b7-153">Par défaut, la valeur est TRUE.</span><span class="sxs-lookup"><span data-stu-id="f85b7-153">Defaults to TRUE.</span></span> <span data-ttu-id="f85b7-154">Lorsqu’elle est désactivée, une page vide s’affiche lorsque l’erreur associée se produit.</span><span class="sxs-lookup"><span data-stu-id="f85b7-154">When disabled, blank page will be shown when related error happens.</span></span>

#### <span data-ttu-id="f85b7-155">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="f85b7-155">IsScriptEnabled</span></span> 

<span data-ttu-id="f85b7-156">Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.</span><span class="sxs-lookup"><span data-stu-id="f85b7-156">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="f85b7-157">public bool [IsScriptEnabled](#isscriptenabled)</span><span class="sxs-lookup"><span data-stu-id="f85b7-157">public bool [IsScriptEnabled](#isscriptenabled)</span></span>

<span data-ttu-id="f85b7-158">Cela ne concerne que les scripts du document. les scripts injectés avec ExecuteScript s’exécutent même si le script est désactivé.</span><span class="sxs-lookup"><span data-stu-id="f85b7-158">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="f85b7-159">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="f85b7-159">It is true by default.</span></span>

#### <span data-ttu-id="f85b7-160">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="f85b7-160">IsStatusBarEnabled</span></span> 

<span data-ttu-id="f85b7-161">IsStatusBarEnabled vérifie si la barre d’État s’affiche.</span><span class="sxs-lookup"><span data-stu-id="f85b7-161">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="f85b7-162">public bool [IsStatusBarEnabled](#isstatusbarenabled)</span><span class="sxs-lookup"><span data-stu-id="f85b7-162">public bool [IsStatusBarEnabled](#isstatusbarenabled)</span></span>

<span data-ttu-id="f85b7-163">La barre d’État est généralement affichée dans le coin inférieur gauche de l’affichage WebView et présente des éléments tels que l’URI d’un lien lorsque l’utilisateur pointe dessus et d’autres informations.</span><span class="sxs-lookup"><span data-stu-id="f85b7-163">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="f85b7-164">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="f85b7-164">It is true by default.</span></span>

#### <span data-ttu-id="f85b7-165">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="f85b7-165">IsWebMessageEnabled</span></span> 

<span data-ttu-id="f85b7-166">La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="f85b7-166">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="f85b7-167">public bool [IsWebMessageEnabled](#iswebmessageenabled)</span><span class="sxs-lookup"><span data-stu-id="f85b7-167">public bool [IsWebMessageEnabled](#iswebmessageenabled)</span></span>

<span data-ttu-id="f85b7-168">Si elle a la valeur true, la communication de l’hôte vers le document HTML de niveau supérieur de l’hôte est autorisée via PostWebMessageAsJson, PostWebMessageAsString et Window. chrome. événement de message (voir la documentation PostWebMessageAsJson pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="f85b7-168">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="f85b7-169">La communication du document HTML de niveau supérieur d’un WebView à l’hôte est autorisée via la fonction postMessage de Window. chrome. WebView et la méthode SetWebMessageReceivedEventHandler (voir la documentation SetWebMessageReceivedEventHandler pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="f85b7-169">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="f85b7-170">Si elle est définie sur false, la communication n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="f85b7-170">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="f85b7-171">PostWebMessageAsJson et PostWebMessageAsString échoueront avec E_ACCESSDENIED et Window. chrome. WebView. postMessage échoue en levant une instance d’objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="f85b7-171">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="f85b7-172">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="f85b7-172">It is true by default.</span></span>

#### <span data-ttu-id="f85b7-173">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="f85b7-173">IsZoomControlEnabled</span></span> 

<span data-ttu-id="f85b7-174">La propriété IsZoomControlEnabled est utilisée pour empêcher l’utilisateur d’influer sur le zoom du WebView.</span><span class="sxs-lookup"><span data-stu-id="f85b7-174">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="f85b7-175">public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span><span class="sxs-lookup"><span data-stu-id="f85b7-175">public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span></span>

<span data-ttu-id="f85b7-176">Par défaut, la valeur est TRUE.</span><span class="sxs-lookup"><span data-stu-id="f85b7-176">Defaults to TRUE.</span></span> <span data-ttu-id="f85b7-177">Lorsqu’il est désactivé, l’utilisateur ne peut pas effectuer un zoom à l’aide de Ctrl +/-ou Ctrl + molette, mais le zoom peut être défini via l’API ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="f85b7-177">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

