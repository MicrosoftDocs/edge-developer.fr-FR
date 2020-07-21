---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: c31e81fba190d9c8c72d344c7fa1e442d5365d4e
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886401"
---
# <span data-ttu-id="a95bd-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="a95bd-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2Settings class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="a95bd-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="a95bd-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="a95bd-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="a95bd-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="a95bd-107">Définit les propriétés permettant, de désactiver ou de modifier les fonctionnalités WebView.</span><span class="sxs-lookup"><span data-stu-id="a95bd-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="a95bd-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="a95bd-108">Summary</span></span>

 <span data-ttu-id="a95bd-109">Ses</span><span class="sxs-lookup"><span data-stu-id="a95bd-109">Members</span></span>                        | <span data-ttu-id="a95bd-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="a95bd-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a95bd-111">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="a95bd-111">AreDefaultContextMenusEnabled</span></span>](#aredefaultcontextmenusenabled) | <span data-ttu-id="a95bd-112">La propriété AreDefaultContextMenusEnabled est utilisée pour empêcher l’affichage des menus contextuels par défaut pour les utilisateurs dans WebView.</span><span class="sxs-lookup"><span data-stu-id="a95bd-112">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="a95bd-113">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="a95bd-113">AreDefaultScriptDialogsEnabled</span></span>](#aredefaultscriptdialogsenabled) | <span data-ttu-id="a95bd-114">AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="a95bd-114">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="a95bd-115">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="a95bd-115">AreDevToolsEnabled</span></span>](#aredevtoolsenabled) | <span data-ttu-id="a95bd-116">AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="a95bd-116">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="a95bd-117">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="a95bd-117">AreHostObjectsAllowed</span></span>](#arehostobjectsallowed) | <span data-ttu-id="a95bd-118">La propriété AreHostObjectsAllowed est utilisée pour contrôler si les objets hôtes sont accessibles à partir de la page dans WebView.</span><span class="sxs-lookup"><span data-stu-id="a95bd-118">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="a95bd-119">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="a95bd-119">IsBuiltInErrorPageEnabled</span></span>](#isbuiltinerrorpageenabled) | <span data-ttu-id="a95bd-120">La propriété IsBuiltInErrorPageEnabled est utilisée pour désactiver la page d’erreur intégrée à un échec de navigation et un échec de processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="a95bd-120">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="a95bd-121">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="a95bd-121">IsScriptEnabled</span></span>](#isscriptenabled) | <span data-ttu-id="a95bd-122">Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.</span><span class="sxs-lookup"><span data-stu-id="a95bd-122">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="a95bd-123">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="a95bd-123">IsStatusBarEnabled</span></span>](#isstatusbarenabled) | <span data-ttu-id="a95bd-124">IsStatusBarEnabled vérifie si la barre d’État s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a95bd-124">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="a95bd-125">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="a95bd-125">IsWebMessageEnabled</span></span>](#iswebmessageenabled) | <span data-ttu-id="a95bd-126">La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="a95bd-126">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="a95bd-127">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="a95bd-127">IsZoomControlEnabled</span></span>](#iszoomcontrolenabled) | <span data-ttu-id="a95bd-128">La propriété IsZoomControlEnabled est utilisée pour empêcher l’utilisateur d’influer sur le zoom du WebView.</span><span class="sxs-lookup"><span data-stu-id="a95bd-128">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

<span data-ttu-id="a95bd-129">Les modifications apportées après l’événement NavigationStarting ne s’appliquent pas tant que la navigation de niveau supérieur suivante n’est pas appliquée.</span><span class="sxs-lookup"><span data-stu-id="a95bd-129">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="a95bd-130">Ses</span><span class="sxs-lookup"><span data-stu-id="a95bd-130">Members</span></span>

#### <span data-ttu-id="a95bd-131">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="a95bd-131">AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="a95bd-132">La propriété AreDefaultContextMenusEnabled est utilisée pour empêcher l’affichage des menus contextuels par défaut pour les utilisateurs dans WebView.</span><span class="sxs-lookup"><span data-stu-id="a95bd-132">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="a95bd-133">public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span><span class="sxs-lookup"><span data-stu-id="a95bd-133">public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span></span>

<span data-ttu-id="a95bd-134">Par défaut, la valeur est TRUE.</span><span class="sxs-lookup"><span data-stu-id="a95bd-134">Defaults to TRUE.</span></span>

#### <span data-ttu-id="a95bd-135">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="a95bd-135">AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="a95bd-136">AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="a95bd-136">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="a95bd-137">public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span><span class="sxs-lookup"><span data-stu-id="a95bd-137">public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span></span>

<span data-ttu-id="a95bd-138">Si elle a la valeur false, le WebView n’affichera pas la boîte de dialogue JavaScript par défaut (en particulier, celles qui sont affichées par l’alerte JavaScript, les fonctions confirmer, invites et événement beforeunload).</span><span class="sxs-lookup"><span data-stu-id="a95bd-138">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="a95bd-139">Au lieu de cela, si un gestionnaire d’événements est défini par SetScriptDialogOpeningEventHandler, WebView envoie un événement qui contient toutes les informations pour la boîte de dialogue et autorise l’application hôte à afficher sa propre interface utilisateur personnalisée.</span><span class="sxs-lookup"><span data-stu-id="a95bd-139">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="a95bd-140">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="a95bd-140">AreDevToolsEnabled</span></span> 

<span data-ttu-id="a95bd-141">AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="a95bd-141">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="a95bd-142">public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span><span class="sxs-lookup"><span data-stu-id="a95bd-142">public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span></span>

<span data-ttu-id="a95bd-143">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="a95bd-143">It is true by default.</span></span>

#### <span data-ttu-id="a95bd-144">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="a95bd-144">AreHostObjectsAllowed</span></span> 

<span data-ttu-id="a95bd-145">La propriété AreHostObjectsAllowed est utilisée pour contrôler si les objets hôtes sont accessibles à partir de la page dans WebView.</span><span class="sxs-lookup"><span data-stu-id="a95bd-145">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="a95bd-146">public bool [AreHostObjectsAllowed](#arehostobjectsallowed)</span><span class="sxs-lookup"><span data-stu-id="a95bd-146">public bool [AreHostObjectsAllowed](#arehostobjectsallowed)</span></span>

<span data-ttu-id="a95bd-147">Par défaut, la valeur est TRUE.</span><span class="sxs-lookup"><span data-stu-id="a95bd-147">Defaults to TRUE.</span></span>

#### <span data-ttu-id="a95bd-148">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="a95bd-148">IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="a95bd-149">La propriété IsBuiltInErrorPageEnabled est utilisée pour désactiver la page d’erreur intégrée à un échec de navigation et un échec de processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="a95bd-149">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="a95bd-150">public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span><span class="sxs-lookup"><span data-stu-id="a95bd-150">public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span></span>

<span data-ttu-id="a95bd-151">Par défaut, la valeur est TRUE.</span><span class="sxs-lookup"><span data-stu-id="a95bd-151">Defaults to TRUE.</span></span> <span data-ttu-id="a95bd-152">Lorsqu’elle est désactivée, une page vide s’affiche lorsque l’erreur associée se produit.</span><span class="sxs-lookup"><span data-stu-id="a95bd-152">When disabled, blank page will be shown when related error happens.</span></span>

#### <span data-ttu-id="a95bd-153">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="a95bd-153">IsScriptEnabled</span></span> 

<span data-ttu-id="a95bd-154">Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.</span><span class="sxs-lookup"><span data-stu-id="a95bd-154">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="a95bd-155">public bool [IsScriptEnabled](#isscriptenabled)</span><span class="sxs-lookup"><span data-stu-id="a95bd-155">public bool [IsScriptEnabled](#isscriptenabled)</span></span>

<span data-ttu-id="a95bd-156">Cela ne concerne que les scripts du document. les scripts injectés avec ExecuteScript s’exécutent même si le script est désactivé.</span><span class="sxs-lookup"><span data-stu-id="a95bd-156">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="a95bd-157">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="a95bd-157">It is true by default.</span></span>

#### <span data-ttu-id="a95bd-158">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="a95bd-158">IsStatusBarEnabled</span></span> 

<span data-ttu-id="a95bd-159">IsStatusBarEnabled vérifie si la barre d’État s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a95bd-159">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="a95bd-160">public bool [IsStatusBarEnabled](#isstatusbarenabled)</span><span class="sxs-lookup"><span data-stu-id="a95bd-160">public bool [IsStatusBarEnabled](#isstatusbarenabled)</span></span>

<span data-ttu-id="a95bd-161">La barre d’État est généralement affichée dans le coin inférieur gauche de l’affichage WebView et présente des éléments tels que l’URI d’un lien lorsque l’utilisateur pointe dessus et d’autres informations.</span><span class="sxs-lookup"><span data-stu-id="a95bd-161">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="a95bd-162">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="a95bd-162">It is true by default.</span></span>

#### <span data-ttu-id="a95bd-163">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="a95bd-163">IsWebMessageEnabled</span></span> 

<span data-ttu-id="a95bd-164">La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.</span><span class="sxs-lookup"><span data-stu-id="a95bd-164">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="a95bd-165">public bool [IsWebMessageEnabled](#iswebmessageenabled)</span><span class="sxs-lookup"><span data-stu-id="a95bd-165">public bool [IsWebMessageEnabled](#iswebmessageenabled)</span></span>

<span data-ttu-id="a95bd-166">Si elle a la valeur true, la communication de l’hôte vers le document HTML de niveau supérieur de l’hôte est autorisée via PostWebMessageAsJson, PostWebMessageAsString et Window. chrome. événement de message (voir la documentation PostWebMessageAsJson pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="a95bd-166">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="a95bd-167">La communication du document HTML de niveau supérieur d’un WebView à l’hôte est autorisée via la fonction postMessage de Window. chrome. WebView et la méthode SetWebMessageReceivedEventHandler (voir la documentation SetWebMessageReceivedEventHandler pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="a95bd-167">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="a95bd-168">Si elle est définie sur false, la communication n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="a95bd-168">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="a95bd-169">PostWebMessageAsJson et PostWebMessageAsString échoueront avec E_ACCESSDENIED et Window. chrome. WebView. postMessage échoue en levant une instance d’objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="a95bd-169">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="a95bd-170">C’est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="a95bd-170">It is true by default.</span></span>

#### <span data-ttu-id="a95bd-171">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="a95bd-171">IsZoomControlEnabled</span></span> 

<span data-ttu-id="a95bd-172">La propriété IsZoomControlEnabled est utilisée pour empêcher l’utilisateur d’influer sur le zoom du WebView.</span><span class="sxs-lookup"><span data-stu-id="a95bd-172">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="a95bd-173">public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span><span class="sxs-lookup"><span data-stu-id="a95bd-173">public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span></span>

<span data-ttu-id="a95bd-174">Par défaut, la valeur est TRUE.</span><span class="sxs-lookup"><span data-stu-id="a95bd-174">Defaults to TRUE.</span></span> <span data-ttu-id="a95bd-175">Lorsqu’il est désactivé, l’utilisateur ne peut pas effectuer un zoom à l’aide de Ctrl +/-ou Ctrl + molette, mais le zoom peut être défini via l’API ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="a95bd-175">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

