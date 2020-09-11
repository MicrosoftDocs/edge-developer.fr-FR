---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2Settings
ms.openlocfilehash: 87b78956c29dac74bd023556a8c495222d248e9f
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011857"
---
# <span data-ttu-id="8435b-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="8435b-104">Microsoft.Web.WebView2.Core.CoreWebView2Settings class</span></span> 

<span data-ttu-id="8435b-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="8435b-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="8435b-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="8435b-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="8435b-107">Définit les propriétés permettant, de désactiver ou de modifier les fonctionnalités WebView.</span><span class="sxs-lookup"><span data-stu-id="8435b-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="8435b-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="8435b-108">Summary</span></span>

 <span data-ttu-id="8435b-109">Ses</span><span class="sxs-lookup"><span data-stu-id="8435b-109">Members</span></span>                        | <span data-ttu-id="8435b-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="8435b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8435b-111">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="8435b-111">AreDefaultContextMenusEnabled</span></span>](#aredefaultcontextmenusenabled) | <span data-ttu-id="8435b-112">La propriété AreDefaultContextMenusEnabled est utilisée pour empêcher l’affichage des menus contextuels par défaut pour les utilisateurs dans WebView.</span><span class="sxs-lookup"><span data-stu-id="8435b-112">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in WebView.</span></span>
[<span data-ttu-id="8435b-113">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="8435b-113">AreDefaultScriptDialogsEnabled</span></span>](#aredefaultscriptdialogsenabled) | <span data-ttu-id="8435b-114">AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="8435b-114">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="8435b-115">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="8435b-115">AreDevToolsEnabled</span></span>](#aredevtoolsenabled) | <span data-ttu-id="8435b-116">AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="8435b-116">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="8435b-117">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="8435b-117">AreHostObjectsAllowed</span></span>](#arehostobjectsallowed) | <span data-ttu-id="8435b-118">La propriété AreHostObjectsAllowed est utilisée pour contrôler si les objets hôtes sont accessibles à partir de la page dans WebView.</span><span class="sxs-lookup"><span data-stu-id="8435b-118">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in WebView.</span></span>
[<span data-ttu-id="8435b-119">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="8435b-119">IsBuiltInErrorPageEnabled</span></span>](#isbuiltinerrorpageenabled) | <span data-ttu-id="8435b-120">La propriété IsBuiltInErrorPageEnabled est utilisée pour désactiver la page d’erreur intégrée à un échec de navigation et un échec de processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="8435b-120">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="8435b-121">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="8435b-121">IsScriptEnabled</span></span>](#isscriptenabled) | <span data-ttu-id="8435b-122">Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.</span><span class="sxs-lookup"><span data-stu-id="8435b-122">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="8435b-123">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="8435b-123">IsStatusBarEnabled</span></span>](#isstatusbarenabled) | <span data-ttu-id="8435b-124">IsStatusBarEnabled vérifie si la barre d’État s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8435b-124">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="8435b-125">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="8435b-125">IsWebMessageEnabled</span></span>](#iswebmessageenabled) | <span data-ttu-id="8435b-126">La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="8435b-126">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="8435b-127">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="8435b-127">IsZoomControlEnabled</span></span>](#iszoomcontrolenabled) | <span data-ttu-id="8435b-128">La propriété IsZoomControlEnabled est utilisée pour empêcher l’utilisateur d’influer sur le zoom du WebView.</span><span class="sxs-lookup"><span data-stu-id="8435b-128">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

<span data-ttu-id="8435b-129">Les modifications apportées après l’événement NavigationStarting ne s’appliquent pas tant que la navigation de niveau supérieur suivante n’est pas appliquée.</span><span class="sxs-lookup"><span data-stu-id="8435b-129">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="8435b-130">Ses</span><span class="sxs-lookup"><span data-stu-id="8435b-130">Members</span></span>

#### <span data-ttu-id="8435b-131">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="8435b-131">AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="8435b-132">La propriété AreDefaultContextMenusEnabled est utilisée pour empêcher l’affichage des menus contextuels par défaut pour les utilisateurs dans WebView.</span><span class="sxs-lookup"><span data-stu-id="8435b-132">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in WebView.</span></span>

> <span data-ttu-id="8435b-133">public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span><span class="sxs-lookup"><span data-stu-id="8435b-133">public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span></span>

<span data-ttu-id="8435b-134">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="8435b-134">It is true by default.</span></span>

#### <span data-ttu-id="8435b-135">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="8435b-135">AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="8435b-136">AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="8435b-136">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="8435b-137">public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span><span class="sxs-lookup"><span data-stu-id="8435b-137">public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span></span>

<span data-ttu-id="8435b-138">Si elle a la valeur false, le WebView n’affichera pas la boîte de dialogue JavaScript par défaut (en particulier, celles qui sont affichées par l’alerte JavaScript, les fonctions confirmer, invites et événement beforeunload).</span><span class="sxs-lookup"><span data-stu-id="8435b-138">If set to false, then WebView won't render the default JavaScript dialog box (Specifically those shown by the JavaScript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="8435b-139">S’il est défini sur true, l’un peut également s’abonner à l’événement ScriptDialogOpening qui contiendra toutes les informations pour la boîte de dialogue et permettre à l’application hôte d’afficher sa propre interface utilisateur personnalisée.</span><span class="sxs-lookup"><span data-stu-id="8435b-139">If set to true, one can also subscribe to ScriptDialogOpening event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span> <span data-ttu-id="8435b-140">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="8435b-140">It is true by default.</span></span>

#### <span data-ttu-id="8435b-141">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="8435b-141">AreDevToolsEnabled</span></span> 

<span data-ttu-id="8435b-142">AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="8435b-142">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="8435b-143">public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span><span class="sxs-lookup"><span data-stu-id="8435b-143">public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span></span>

<span data-ttu-id="8435b-144">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="8435b-144">It is true by default.</span></span>

#### <span data-ttu-id="8435b-145">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="8435b-145">AreHostObjectsAllowed</span></span> 

<span data-ttu-id="8435b-146">La propriété AreHostObjectsAllowed est utilisée pour contrôler si les objets hôtes sont accessibles à partir de la page dans WebView.</span><span class="sxs-lookup"><span data-stu-id="8435b-146">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in WebView.</span></span>

> <span data-ttu-id="8435b-147">public bool [AreHostObjectsAllowed](#arehostobjectsallowed)</span><span class="sxs-lookup"><span data-stu-id="8435b-147">public bool [AreHostObjectsAllowed](#arehostobjectsallowed)</span></span>

<span data-ttu-id="8435b-148">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="8435b-148">It is true by default.</span></span>

#### <span data-ttu-id="8435b-149">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="8435b-149">IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="8435b-150">La propriété IsBuiltInErrorPageEnabled est utilisée pour désactiver la page d’erreur intégrée à un échec de navigation et un échec de processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="8435b-150">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="8435b-151">public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span><span class="sxs-lookup"><span data-stu-id="8435b-151">public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span></span>

<span data-ttu-id="8435b-152">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="8435b-152">It is true by default.</span></span> <span data-ttu-id="8435b-153">Lorsqu’elle est désactivée, une page vide s’affiche lorsque l’erreur associée se produit.</span><span class="sxs-lookup"><span data-stu-id="8435b-153">When disabled, blank page will be shown when related error happens.</span></span>

#### <span data-ttu-id="8435b-154">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="8435b-154">IsScriptEnabled</span></span> 

<span data-ttu-id="8435b-155">Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.</span><span class="sxs-lookup"><span data-stu-id="8435b-155">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="8435b-156">public bool [IsScriptEnabled](#isscriptenabled)</span><span class="sxs-lookup"><span data-stu-id="8435b-156">public bool [IsScriptEnabled](#isscriptenabled)</span></span>

<span data-ttu-id="8435b-157">Cela ne concerne que les scripts du document. les scripts injectés avec ExecuteScript s’exécutent même si le script est désactivé.</span><span class="sxs-lookup"><span data-stu-id="8435b-157">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="8435b-158">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="8435b-158">It is true by default.</span></span>

#### <span data-ttu-id="8435b-159">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="8435b-159">IsStatusBarEnabled</span></span> 

<span data-ttu-id="8435b-160">IsStatusBarEnabled vérifie si la barre d’État s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8435b-160">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="8435b-161">public bool [IsStatusBarEnabled](#isstatusbarenabled)</span><span class="sxs-lookup"><span data-stu-id="8435b-161">public bool [IsStatusBarEnabled](#isstatusbarenabled)</span></span>

<span data-ttu-id="8435b-162">La barre d’État est généralement affichée dans le coin inférieur gauche de l’affichage WebView et présente des éléments tels que l’URI d’un lien lorsque l’utilisateur pointe dessus et d’autres informations.</span><span class="sxs-lookup"><span data-stu-id="8435b-162">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="8435b-163">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="8435b-163">It is true by default.</span></span>

#### <span data-ttu-id="8435b-164">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="8435b-164">IsWebMessageEnabled</span></span> 

<span data-ttu-id="8435b-165">La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="8435b-165">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="8435b-166">public bool [IsWebMessageEnabled](#iswebmessageenabled)</span><span class="sxs-lookup"><span data-stu-id="8435b-166">public bool [IsWebMessageEnabled](#iswebmessageenabled)</span></span>

<span data-ttu-id="8435b-167">Si elle a la valeur true, la communication de l’hôte vers le document HTML de niveau supérieur de l’hôte est autorisée via PostWebMessageAsJson, PostWebMessageAsString et Window. chrome. événement de message (voir la documentation PostWebMessageAsJson pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="8435b-167">If set to true, communication from the host to the WebView's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="8435b-168">La communication du document HTML de niveau supérieur d’un WebView à l’hôte est autorisée via la fonction postMessage de Window. chrome. WebView et l’événement WebMessageReceived (voir la documentation WebMessageReceived pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="8435b-168">Communication from the WebView's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the WebMessageReceived event (see WebMessageReceived documentation for details).</span></span> <span data-ttu-id="8435b-169">Si elle est définie sur false, la communication n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="8435b-169">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="8435b-170">PostWebMessageAsJson et PostWebMessageAsString échoueront avec E_ACCESSDENIED et Window. chrome. WebView. postMessage échoue en levant une instance d’objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="8435b-170">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="8435b-171">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="8435b-171">It is true by default.</span></span>

#### <span data-ttu-id="8435b-172">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="8435b-172">IsZoomControlEnabled</span></span> 

<span data-ttu-id="8435b-173">La propriété IsZoomControlEnabled est utilisée pour empêcher l’utilisateur d’influer sur le zoom du WebView.</span><span class="sxs-lookup"><span data-stu-id="8435b-173">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="8435b-174">public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span><span class="sxs-lookup"><span data-stu-id="8435b-174">public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span></span>

<span data-ttu-id="8435b-175">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="8435b-175">It is true by default.</span></span> <span data-ttu-id="8435b-176">Lorsqu’il est désactivé, l’utilisateur ne peut pas effectuer un zoom à l’aide de Ctrl +/-ou Ctrl + molette, mais le zoom peut être défini via l’API ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="8435b-176">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

