---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2
ms.openlocfilehash: 6717542349cff327875b609168dff0b82a933668
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011969"
---
# <span data-ttu-id="41db2-104">interface ICoreWebView2</span><span class="sxs-lookup"><span data-stu-id="41db2-104">interface ICoreWebView2</span></span> 

```
interface ICoreWebView2
  : public IUnknown
```

<span data-ttu-id="41db2-105">WebView2 vous permet d’héberger le contenu Web à l’aide de la technologie de navigateur Web la plus récente.</span><span class="sxs-lookup"><span data-stu-id="41db2-105">WebView2 enables you to host web content using the latest Edge web browser technology.</span></span>

## <span data-ttu-id="41db2-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="41db2-106">Summary</span></span>

 <span data-ttu-id="41db2-107">Ses</span><span class="sxs-lookup"><span data-stu-id="41db2-107">Members</span></span>                        | <span data-ttu-id="41db2-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="41db2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="41db2-109">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="41db2-109">add_ContainsFullScreenElementChanged</span></span>](#add_containsfullscreenelementchanged) | <span data-ttu-id="41db2-110">Ajoutez un gestionnaire d’événements pour l’événement ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="41db2-110">Add an event handler for the ContainsFullScreenElementChanged event.</span></span>
[<span data-ttu-id="41db2-111">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="41db2-111">add_ContentLoading</span></span>](#add_contentloading) | <span data-ttu-id="41db2-112">Ajoutez un gestionnaire d’événements pour l’événement ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="41db2-112">Add an event handler for the ContentLoading event.</span></span>
[<span data-ttu-id="41db2-113">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="41db2-113">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="41db2-114">Ajoutez un gestionnaire d’événements pour l’événement DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="41db2-114">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="41db2-115">add_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="41db2-115">add_FrameNavigationCompleted</span></span>](#add_framenavigationcompleted) | <span data-ttu-id="41db2-116">Ajoutez un gestionnaire d’événements pour l’événement FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="41db2-116">Add an event handler for the FrameNavigationCompleted event.</span></span>
[<span data-ttu-id="41db2-117">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="41db2-117">add_FrameNavigationStarting</span></span>](#add_framenavigationstarting) | <span data-ttu-id="41db2-118">Ajoutez un gestionnaire d’événements pour l’événement FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="41db2-118">Add an event handler for the FrameNavigationStarting event.</span></span>
[<span data-ttu-id="41db2-119">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="41db2-119">add_HistoryChanged</span></span>](#add_historychanged) | <span data-ttu-id="41db2-120">Ajoutez un gestionnaire d’événements pour l’événement HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="41db2-120">Add an event handler for the HistoryChanged event.</span></span>
[<span data-ttu-id="41db2-121">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="41db2-121">add_NavigationCompleted</span></span>](#add_navigationcompleted) | <span data-ttu-id="41db2-122">Ajoutez un gestionnaire d’événements pour l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="41db2-122">Add an event handler for the NavigationCompleted event.</span></span>
[<span data-ttu-id="41db2-123">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="41db2-123">add_NavigationStarting</span></span>](#add_navigationstarting) | <span data-ttu-id="41db2-124">Ajoutez un gestionnaire d’événements pour l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="41db2-124">Add an event handler for the NavigationStarting event.</span></span>
[<span data-ttu-id="41db2-125">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="41db2-125">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="41db2-126">Ajoutez un gestionnaire d’événements pour l’événement NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="41db2-126">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="41db2-127">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="41db2-127">add_PermissionRequested</span></span>](#add_permissionrequested) | <span data-ttu-id="41db2-128">Ajoutez un gestionnaire d’événements pour l’événement PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="41db2-128">Add an event handler for the PermissionRequested event.</span></span>
[<span data-ttu-id="41db2-129">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="41db2-129">add_ProcessFailed</span></span>](#add_processfailed) | <span data-ttu-id="41db2-130">Ajoutez un gestionnaire d’événements pour l’événement ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="41db2-130">Add an event handler for the ProcessFailed event.</span></span>
[<span data-ttu-id="41db2-131">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="41db2-131">add_ScriptDialogOpening</span></span>](#add_scriptdialogopening) | <span data-ttu-id="41db2-132">Ajoutez un gestionnaire d’événements pour l’événement ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="41db2-132">Add an event handler for the ScriptDialogOpening event.</span></span>
[<span data-ttu-id="41db2-133">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="41db2-133">add_SourceChanged</span></span>](#add_sourcechanged) | <span data-ttu-id="41db2-134">Ajoutez un gestionnaire d’événements pour l’événement SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="41db2-134">Add an event handler for the SourceChanged event.</span></span>
[<span data-ttu-id="41db2-135">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="41db2-135">add_WebMessageReceived</span></span>](#add_webmessagereceived) | <span data-ttu-id="41db2-136">Ajoutez un gestionnaire d’événements pour l’événement WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="41db2-136">Add an event handler for the WebMessageReceived event.</span></span>
[<span data-ttu-id="41db2-137">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="41db2-137">add_WebResourceRequested</span></span>](#add_webresourcerequested) | <span data-ttu-id="41db2-138">Ajoutez un gestionnaire d’événements pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="41db2-138">Add an event handler for the WebResourceRequested event.</span></span>
[<span data-ttu-id="41db2-139">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="41db2-139">add_WindowCloseRequested</span></span>](#add_windowcloserequested) | <span data-ttu-id="41db2-140">Ajoutez un gestionnaire d’événements pour l’événement WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="41db2-140">Add an event handler for the WindowCloseRequested event.</span></span>
[<span data-ttu-id="41db2-141">AddHostObjectToScript</span><span class="sxs-lookup"><span data-stu-id="41db2-141">AddHostObjectToScript</span></span>](#addhostobjecttoscript) | <span data-ttu-id="41db2-142">Ajoutez l’objet hôte fourni au script qui s’exécute sur le WebView avec le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="41db2-142">Add the provided host object to script running in the WebView with the specified name.</span></span>
[<span data-ttu-id="41db2-143">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="41db2-143">AddScriptToExecuteOnDocumentCreated</span></span>](#addscripttoexecuteondocumentcreated) | <span data-ttu-id="41db2-144">Ajoutez le code JavaScript fourni à une liste de scripts qui doivent être exécutés après la création de l’objet global, mais avant l’analyse du document HTML et avant l’exécution de tout autre script fourni par le document HTML.</span><span class="sxs-lookup"><span data-stu-id="41db2-144">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>
[<span data-ttu-id="41db2-145">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="41db2-145">AddWebResourceRequestedFilter</span></span>](#addwebresourcerequestedfilter) | <span data-ttu-id="41db2-146">Ajoute un URI et un filtre de contexte de ressources à l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="41db2-146">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>
[<span data-ttu-id="41db2-147">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="41db2-147">CallDevToolsProtocolMethod</span></span>](#calldevtoolsprotocolmethod) | <span data-ttu-id="41db2-148">Appelez une méthode DevToolsProtocol asynchrone.</span><span class="sxs-lookup"><span data-stu-id="41db2-148">Call an asynchronous DevToolsProtocol method.</span></span>
[<span data-ttu-id="41db2-149">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="41db2-149">CapturePreview</span></span>](#capturepreview) | <span data-ttu-id="41db2-150">Capturez une image de l’affichage du WebView.</span><span class="sxs-lookup"><span data-stu-id="41db2-150">Capture an image of what WebView is displaying.</span></span>
[<span data-ttu-id="41db2-151">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="41db2-151">ExecuteScript</span></span>](#executescript) | <span data-ttu-id="41db2-152">Exécutez le code JavaScript du paramètre JavaScript du document de niveau supérieur actuel affiché dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="41db2-152">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="41db2-153">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="41db2-153">get_BrowserProcessId</span></span>](#get_browserprocessid) | <span data-ttu-id="41db2-154">ID de processus du processus de navigation qui héberge le WebView.</span><span class="sxs-lookup"><span data-stu-id="41db2-154">The process id of the browser process that hosts the WebView.</span></span>
[<span data-ttu-id="41db2-155">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="41db2-155">get_CanGoBack</span></span>](#get_cangoback) | <span data-ttu-id="41db2-156">Renvoie vrai si le WebView peut accéder à une page précédente de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="41db2-156">Returns true if the WebView can navigate to a previous page in the navigation history.</span></span>
[<span data-ttu-id="41db2-157">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="41db2-157">get_CanGoForward</span></span>](#get_cangoforward) | <span data-ttu-id="41db2-158">Cette fonction renvoie la valeur vrai si le WebView peut accéder à une page suivante de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="41db2-158">Returns true if the WebView can navigate to a next page in the navigation history.</span></span>
[<span data-ttu-id="41db2-159">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="41db2-159">get_ContainsFullScreenElement</span></span>](#get_containsfullscreenelement) | <span data-ttu-id="41db2-160">Indique si le WebView contient un élément HTML fullscreen.</span><span class="sxs-lookup"><span data-stu-id="41db2-160">Indicates if the WebView contains a fullscreen HTML element.</span></span>
[<span data-ttu-id="41db2-161">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="41db2-161">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="41db2-162">Titre du document de niveau supérieur actuel.</span><span class="sxs-lookup"><span data-stu-id="41db2-162">The title for the current top level document.</span></span>
[<span data-ttu-id="41db2-163">get_Settings</span><span class="sxs-lookup"><span data-stu-id="41db2-163">get_Settings</span></span>](#get_settings) | <span data-ttu-id="41db2-164">L’objet [ICoreWebView2Settings](icorewebview2settings.md) contient différents paramètres modifiables pour le WebView en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="41db2-164">The [ICoreWebView2Settings](icorewebview2settings.md) object contains various modifiable settings for the running WebView.</span></span>
[<span data-ttu-id="41db2-165">get_Source</span><span class="sxs-lookup"><span data-stu-id="41db2-165">get_Source</span></span>](#get_source) | <span data-ttu-id="41db2-166">URI du document de niveau supérieur actuel.</span><span class="sxs-lookup"><span data-stu-id="41db2-166">The URI of the current top level document.</span></span>
[<span data-ttu-id="41db2-167">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="41db2-167">GetDevToolsProtocolEventReceiver</span></span>](#getdevtoolsprotocoleventreceiver) | <span data-ttu-id="41db2-168">Obtenez un destinataire d’événement de protocole DevTools qui vous permet de vous abonner à un événement de protocole DevTools.</span><span class="sxs-lookup"><span data-stu-id="41db2-168">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>
[<span data-ttu-id="41db2-169">GoBack</span><span class="sxs-lookup"><span data-stu-id="41db2-169">GoBack</span></span>](#goback) | <span data-ttu-id="41db2-170">Permet d’accéder à la page précédente de l’historique de navigation via le WebView.</span><span class="sxs-lookup"><span data-stu-id="41db2-170">Navigates the WebView to the previous page in the navigation history.</span></span>
[<span data-ttu-id="41db2-171">GoForward</span><span class="sxs-lookup"><span data-stu-id="41db2-171">GoForward</span></span>](#goforward) | <span data-ttu-id="41db2-172">Navigue vers la page suivante de l’historique de navigation du WebView.</span><span class="sxs-lookup"><span data-stu-id="41db2-172">Navigates the WebView to the next page in the navigation history.</span></span>
[<span data-ttu-id="41db2-173">Rechercher</span><span class="sxs-lookup"><span data-stu-id="41db2-173">Navigate</span></span>](#navigate) | <span data-ttu-id="41db2-174">Entraîner une navigation du document de niveau supérieur sur l’URI spécifié.</span><span class="sxs-lookup"><span data-stu-id="41db2-174">Cause a navigation of the top level document to the specified URI.</span></span>
[<span data-ttu-id="41db2-175">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="41db2-175">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="41db2-176">Lance une navigation vers htmlContent en tant que code HTML source d’un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="41db2-176">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="41db2-177">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="41db2-177">OpenDevToolsWindow</span></span>](#opendevtoolswindow) | <span data-ttu-id="41db2-178">Ouvre la fenêtre DevTools pour le document actif dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="41db2-178">Opens the DevTools window for the current document in the WebView.</span></span>
[<span data-ttu-id="41db2-179">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="41db2-179">PostWebMessageAsJson</span></span>](#postwebmessageasjson) | <span data-ttu-id="41db2-180">Publier le WebMessage spécifié sur le document de niveau supérieur dans ce WebView.</span><span class="sxs-lookup"><span data-stu-id="41db2-180">Post the specified webMessage to the top level document in this WebView.</span></span>
[<span data-ttu-id="41db2-181">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="41db2-181">PostWebMessageAsString</span></span>](#postwebmessageasstring) | <span data-ttu-id="41db2-182">Il s’agit d’un programme d’assistance pour publier un message qui est une chaîne simple plutôt qu’une représentation de chaîne JSON d’un objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="41db2-182">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>
[<span data-ttu-id="41db2-183">Recharger</span><span class="sxs-lookup"><span data-stu-id="41db2-183">Reload</span></span>](#reload) | <span data-ttu-id="41db2-184">Recharger la page active.</span><span class="sxs-lookup"><span data-stu-id="41db2-184">Reload the current page.</span></span>
[<span data-ttu-id="41db2-185">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="41db2-185">remove_ContainsFullScreenElementChanged</span></span>](#remove_containsfullscreenelementchanged) | <span data-ttu-id="41db2-186">Supprimez un gestionnaire d’événements préalablement ajouté à add_ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="41db2-186">Remove an event handler previously added with add_ContainsFullScreenElementChanged.</span></span>
[<span data-ttu-id="41db2-187">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="41db2-187">remove_ContentLoading</span></span>](#remove_contentloading) | <span data-ttu-id="41db2-188">Supprimez un gestionnaire d’événements préalablement ajouté à add_ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="41db2-188">Remove an event handler previously added with add_ContentLoading.</span></span>
[<span data-ttu-id="41db2-189">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="41db2-189">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="41db2-190">Supprimez un gestionnaire d’événements préalablement ajouté à add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="41db2-190">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="41db2-191">remove_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="41db2-191">remove_FrameNavigationCompleted</span></span>](#remove_framenavigationcompleted) | <span data-ttu-id="41db2-192">Supprimez un gestionnaire d’événements préalablement ajouté à add_FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="41db2-192">Remove an event handler previously added with add_FrameNavigationCompleted.</span></span>
[<span data-ttu-id="41db2-193">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="41db2-193">remove_FrameNavigationStarting</span></span>](#remove_framenavigationstarting) | <span data-ttu-id="41db2-194">Supprimez un gestionnaire d’événements préalablement ajouté à add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="41db2-194">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>
[<span data-ttu-id="41db2-195">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="41db2-195">remove_HistoryChanged</span></span>](#remove_historychanged) | <span data-ttu-id="41db2-196">Supprimez un gestionnaire d’événements préalablement ajouté à add_HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="41db2-196">Remove an event handler previously added with add_HistoryChanged.</span></span>
[<span data-ttu-id="41db2-197">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="41db2-197">remove_NavigationCompleted</span></span>](#remove_navigationcompleted) | <span data-ttu-id="41db2-198">Supprimez un gestionnaire d’événements préalablement ajouté à add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="41db2-198">Remove an event handler previously added with add_NavigationCompleted.</span></span>
[<span data-ttu-id="41db2-199">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="41db2-199">remove_NavigationStarting</span></span>](#remove_navigationstarting) | <span data-ttu-id="41db2-200">Supprimez un gestionnaire d’événements préalablement ajouté à add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="41db2-200">Remove an event handler previously added with add_NavigationStarting.</span></span>
[<span data-ttu-id="41db2-201">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="41db2-201">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="41db2-202">Supprimez un gestionnaire d’événements préalablement ajouté à add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="41db2-202">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="41db2-203">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="41db2-203">remove_PermissionRequested</span></span>](#remove_permissionrequested) | <span data-ttu-id="41db2-204">Supprimez un gestionnaire d’événements préalablement ajouté à add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="41db2-204">Remove an event handler previously added with add_PermissionRequested.</span></span>
[<span data-ttu-id="41db2-205">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="41db2-205">remove_ProcessFailed</span></span>](#remove_processfailed) | <span data-ttu-id="41db2-206">Supprimez un gestionnaire d’événements préalablement ajouté à add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="41db2-206">Remove an event handler previously added with add_ProcessFailed.</span></span>
[<span data-ttu-id="41db2-207">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="41db2-207">remove_ScriptDialogOpening</span></span>](#remove_scriptdialogopening) | <span data-ttu-id="41db2-208">Supprimez un gestionnaire d’événements préalablement ajouté à add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="41db2-208">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>
[<span data-ttu-id="41db2-209">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="41db2-209">remove_SourceChanged</span></span>](#remove_sourcechanged) | <span data-ttu-id="41db2-210">Supprimez un gestionnaire d’événements préalablement ajouté à add_SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="41db2-210">Remove an event handler previously added with add_SourceChanged.</span></span>
[<span data-ttu-id="41db2-211">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="41db2-211">remove_WebMessageReceived</span></span>](#remove_webmessagereceived) | <span data-ttu-id="41db2-212">Supprimez un gestionnaire d’événements préalablement ajouté à add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="41db2-212">Remove an event handler previously added with add_WebMessageReceived.</span></span>
[<span data-ttu-id="41db2-213">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="41db2-213">remove_WebResourceRequested</span></span>](#remove_webresourcerequested) | <span data-ttu-id="41db2-214">Supprimez un gestionnaire d’événements préalablement ajouté à add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="41db2-214">Remove an event handler previously added with add_WebResourceRequested.</span></span>
[<span data-ttu-id="41db2-215">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="41db2-215">remove_WindowCloseRequested</span></span>](#remove_windowcloserequested) | <span data-ttu-id="41db2-216">Supprimez un gestionnaire d’événements préalablement ajouté à add_WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="41db2-216">Remove an event handler previously added with add_WindowCloseRequested.</span></span>
[<span data-ttu-id="41db2-217">RemoveHostObjectFromScript</span><span class="sxs-lookup"><span data-stu-id="41db2-217">RemoveHostObjectFromScript</span></span>](#removehostobjectfromscript) | <span data-ttu-id="41db2-218">Supprimez l’objet hôte spécifié par le nom afin qu’il ne soit plus accessible à partir du code JavaScript du WebView.</span><span class="sxs-lookup"><span data-stu-id="41db2-218">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>
[<span data-ttu-id="41db2-219">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="41db2-219">RemoveScriptToExecuteOnDocumentCreated</span></span>](#removescripttoexecuteondocumentcreated) | <span data-ttu-id="41db2-220">Supprimez le JavaScript correspondant ajouté à l’aide `AddScriptToExecuteOnDocumentCreated` de l’ID de script spécifié.</span><span class="sxs-lookup"><span data-stu-id="41db2-220">Remove the corresponding JavaScript added using `AddScriptToExecuteOnDocumentCreated` with the specified script id.</span></span>
[<span data-ttu-id="41db2-221">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="41db2-221">RemoveWebResourceRequestedFilter</span></span>](#removewebresourcerequestedfilter) | <span data-ttu-id="41db2-222">Supprime un filtre de ressources correspondant précédemment ajouté pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="41db2-222">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>
[<span data-ttu-id="41db2-223">Stop</span><span class="sxs-lookup"><span data-stu-id="41db2-223">Stop</span></span>](#stop) | <span data-ttu-id="41db2-224">Arrêtez toutes les navigations et les extractions de ressources en attente.</span><span class="sxs-lookup"><span data-stu-id="41db2-224">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="41db2-225">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="41db2-225">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span>](#corewebview2_capture_preview_image_format) | <span data-ttu-id="41db2-226">Format d’image utilisé par la méthode ICoreWebView2:: CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="41db2-226">Image format used by the ICoreWebView2::CapturePreview method.</span></span>
[<span data-ttu-id="41db2-227">COREWEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="41db2-227">COREWEBVIEW2_KEY_EVENT_KIND</span></span>](#corewebview2_key_event_kind) | <span data-ttu-id="41db2-228">Type d’événement de touche qui déclenchait un événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="41db2-228">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="41db2-229">COREWEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="41db2-229">COREWEBVIEW2_MOVE_FOCUS_REASON</span></span>](#corewebview2_move_focus_reason) | <span data-ttu-id="41db2-230">Raison du déplacement du focus.</span><span class="sxs-lookup"><span data-stu-id="41db2-230">Reason for moving focus.</span></span>
[<span data-ttu-id="41db2-231">COREWEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="41db2-231">COREWEBVIEW2_PERMISSION_KIND</span></span>](#corewebview2_permission_kind) | <span data-ttu-id="41db2-232">Le type d’une demande d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="41db2-232">The type of a permission request.</span></span>
[<span data-ttu-id="41db2-233">COREWEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="41db2-233">COREWEBVIEW2_PERMISSION_STATE</span></span>](#corewebview2_permission_state) | <span data-ttu-id="41db2-234">Réponse à une demande d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="41db2-234">Response to a permission request.</span></span>
[<span data-ttu-id="41db2-235">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="41db2-235">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span></span>](#corewebview2_physical_key_status) | <span data-ttu-id="41db2-236">Structure représentant les informations contenues dans le LPARAM fourni à un événement de touche Win32.</span><span class="sxs-lookup"><span data-stu-id="41db2-236">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>
[<span data-ttu-id="41db2-237">COREWEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="41db2-237">COREWEBVIEW2_PROCESS_FAILED_KIND</span></span>](#corewebview2_process_failed_kind) | <span data-ttu-id="41db2-238">Type d’échec de processus utilisé dans l’interface ICoreWebView2ProcessFailedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="41db2-238">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>
[<span data-ttu-id="41db2-239">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="41db2-239">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span></span>](#corewebview2_script_dialog_kind) | <span data-ttu-id="41db2-240">Type de boîte de dialogue JavaScript utilisée dans l’interface ICoreWebView2ScriptDialogOpeningEventHandler.</span><span class="sxs-lookup"><span data-stu-id="41db2-240">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>
[<span data-ttu-id="41db2-241">COREWEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="41db2-241">COREWEBVIEW2_WEB_ERROR_STATUS</span></span>](#corewebview2_web_error_status) | <span data-ttu-id="41db2-242">Valeurs d’état d’erreur pour les navigations Web.</span><span class="sxs-lookup"><span data-stu-id="41db2-242">Error status values for web navigations.</span></span>
[<span data-ttu-id="41db2-243">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="41db2-243">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span></span>](#corewebview2_web_resource_context) | <span data-ttu-id="41db2-244">Énum pour les contextes de demande de ressources Web.</span><span class="sxs-lookup"><span data-stu-id="41db2-244">Enum for web resource request contexts.</span></span>

## <span data-ttu-id="41db2-245">Ses</span><span class="sxs-lookup"><span data-stu-id="41db2-245">Members</span></span>

#### <span data-ttu-id="41db2-246">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="41db2-246">add_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="41db2-247">Ajoutez un gestionnaire d’événements pour l’événement ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="41db2-247">Add an event handler for the ContainsFullScreenElementChanged event.</span></span>

> <span data-ttu-id="41db2-248">[add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)par le biais du[mot de passe](icorewebview2containsfullscreenelementchangedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="41db2-248">public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](icorewebview2containsfullscreenelementchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="41db2-249">ContainsFullScreenElementChanged se déclenche lorsque la propriété ContainsFullScreenElement change.</span><span class="sxs-lookup"><span data-stu-id="41db2-249">ContainsFullScreenElementChanged fires when the ContainsFullScreenElement property changes.</span></span> <span data-ttu-id="41db2-250">Cela signifie qu’un élément HTML à l’intérieur du WebView est entré en plein écran jusqu’à la taille de l’affichage WebView ou en laissant le plein écran.</span><span class="sxs-lookup"><span data-stu-id="41db2-250">This means that an HTML element inside the WebView is entering fullscreen to the size of the WebView or leaving fullscreen.</span></span> <span data-ttu-id="41db2-251">Cet événement est utile, par exemple, lorsqu’un élément vidéo demande d’être placé en plein écran.</span><span class="sxs-lookup"><span data-stu-id="41db2-251">This event is useful when, for example, a video element requests to go fullscreen.</span></span> <span data-ttu-id="41db2-252">L’écouteur de ContainsFullScreenElementChanged peut alors redimensionner le WebView en réponse.</span><span class="sxs-lookup"><span data-stu-id="41db2-252">The listener of ContainsFullScreenElementChanged can then resize the WebView in response.</span></span>

```cpp
    // Register a handler for the ContainsFullScreenChanged event.
    CHECK_FAILURE(m_webView->add_ContainsFullScreenElementChanged(
        Callback<ICoreWebView2ContainsFullScreenElementChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                if (m_fullScreenAllowed)
                {
                    CHECK_FAILURE(
                        sender->get_ContainsFullScreenElement(&m_containsFullscreenElement));
                    if (m_containsFullscreenElement)
                    {
                        EnterFullScreen();
                    }
                    else
                    {
                        ExitFullScreen();
                    }
                }
                return S_OK;
            })
            .Get(),
        nullptr));
```

#### <span data-ttu-id="41db2-253">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="41db2-253">add_ContentLoading</span></span> 

<span data-ttu-id="41db2-254">Ajoutez un gestionnaire d’événements pour l’événement ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="41db2-254">Add an event handler for the ContentLoading event.</span></span>

> <span data-ttu-id="41db2-255">[add_ContentLoading](#add_contentloading)par le biais du[mot de passe](icorewebview2contentloadingeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="41db2-255">public HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](icorewebview2contentloadingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="41db2-256">ContentLoading se déclenche avant le chargement du contenu, y compris les scripts ajoutés avec AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="41db2-256">ContentLoading fires before any content is loaded, including scripts added with AddScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="41db2-257">ContentLoading ne se déclenchera pas si une même navigation de page se produit (par exemple par le biais des navigations par fragments ou de l’historique. pushState).</span><span class="sxs-lookup"><span data-stu-id="41db2-257">ContentLoading will not fire if a same page navigation occurs (such as through fragment navigations or history.pushState navigations).</span></span> <span data-ttu-id="41db2-258">Cela suit les événements NavigationStarting et SourceChanged, ainsi que les événements HistoryChanged et NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="41db2-258">This follows the NavigationStarting and SourceChanged events and precedes the HistoryChanged and NavigationCompleted events.</span></span>

#### <span data-ttu-id="41db2-259">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="41db2-259">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="41db2-260">Ajoutez un gestionnaire d’événements pour l’événement DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="41db2-260">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="41db2-261">[add_DocumentTitleChanged](#add_documenttitlechanged)par le biais du[mot de passe](icorewebview2documenttitlechangedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="41db2-261">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](icorewebview2documenttitlechangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="41db2-262">DocumentTitleChanged se déclenche lorsque la propriété DocumentTitle de WebView change et qu’elle est susceptible de se déclencher avant ou après l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="41db2-262">DocumentTitleChanged fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

```cpp
    // Register a handler for the DocumentTitleChanged event.
    // This handler just announces the new title on the window's title bar.
    CHECK_FAILURE(m_webView->add_DocumentTitleChanged(
        Callback<ICoreWebView2DocumentTitleChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                wil::unique_cotaskmem_string title;
                CHECK_FAILURE(sender->get_DocumentTitle(&title));
                SetWindowText(m_appWindow->GetMainWindow(), title.get());
                return S_OK;
            })
            .Get(),
        &m_documentTitleChangedToken));
```

#### <span data-ttu-id="41db2-263">add_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="41db2-263">add_FrameNavigationCompleted</span></span> 

<span data-ttu-id="41db2-264">Ajoutez un gestionnaire d’événements pour l’événement FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="41db2-264">Add an event handler for the FrameNavigationCompleted event.</span></span>

> <span data-ttu-id="41db2-265">[add_FrameNavigationCompleted](#add_framenavigationcompleted)par le biais du[mot de passe](icorewebview2navigationcompletedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="41db2-265">public HRESULT [add_FrameNavigationCompleted](#add_framenavigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="41db2-266">FrameNavigationCompleted se déclenche lorsqu’une image enfant est complètement chargée (le corps. OnLoad a été déclenché) ou que le chargement s’est arrêté avec une erreur.</span><span class="sxs-lookup"><span data-stu-id="41db2-266">FrameNavigationCompleted fires when a child frame has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

```cpp
    // Register a handler for the FrameNavigationCompleted event.
    // Check whether the navigation succeeded, and if not, do something.
    CHECK_FAILURE(m_webView->add_FrameNavigationCompleted(
        Callback<ICoreWebView2NavigationCompletedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2NavigationCompletedEventArgs* args)
                -> HRESULT {
                BOOL success;
                CHECK_FAILURE(args->get_IsSuccess(&success));
                if (!success)
                {
                    COREWEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    std::wstring error_msg = WebErrorStatusToString(webErrorStatus);
                    MessageBox(nullptr,
                       (std::wstring(L"IFrame navigation failed with the ") +
                         L"give in error " + error_msg).c_str(),
                       L"Navigation Failure", MB_OK);
                    if (webErrorStatus == COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }
                return S_OK;
            })
            .Get(),
        &m_frameNavigationCompletedToken));
```

#### <span data-ttu-id="41db2-267">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="41db2-267">add_FrameNavigationStarting</span></span> 

<span data-ttu-id="41db2-268">Ajoutez un gestionnaire d’événements pour l’événement FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="41db2-268">Add an event handler for the FrameNavigationStarting event.</span></span>

> <span data-ttu-id="41db2-269">[add_FrameNavigationStarting](#add_framenavigationstarting)par le biais du[mot de passe](icorewebview2navigationstartingeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="41db2-269">public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="41db2-270">FrameNavigationStarting se déclenche quand une Frame enfant dans le WebView demande l’autorisation d’accéder à un URI différent.</span><span class="sxs-lookup"><span data-stu-id="41db2-270">FrameNavigationStarting fires when a child frame in the WebView requests permission to navigate to a different URI.</span></span> <span data-ttu-id="41db2-271">Cela se déclenche également pour les redirections.</span><span class="sxs-lookup"><span data-stu-id="41db2-271">This will fire for redirects as well.</span></span>

<span data-ttu-id="41db2-272">Les navigations correspondantes peuvent être bloquées jusqu’à ce que le gestionnaire d’événements renvoie.</span><span class="sxs-lookup"><span data-stu-id="41db2-272">Corresponding navigations can be blocked until the event handler returns.</span></span>

```cpp
    // Register a handler for the FrameNavigationStarting event.
    // This handler will prevent a frame from navigating to a blocked domain.
    CHECK_FAILURE(m_webView->add_FrameNavigationStarting(
        Callback<ICoreWebView2NavigationStartingEventHandler>(
            [this](ICoreWebView2* sender,
                   ICoreWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));
        }
        return S_OK;
    }).Get(), &m_frameNavigationStartingToken));
```

#### <span data-ttu-id="41db2-273">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="41db2-273">add_HistoryChanged</span></span> 

<span data-ttu-id="41db2-274">Ajoutez un gestionnaire d’événements pour l’événement HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="41db2-274">Add an event handler for the HistoryChanged event.</span></span>

> <span data-ttu-id="41db2-275">[add_HistoryChanged](#add_historychanged)par le biais du[mot de passe](icorewebview2historychangedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="41db2-275">public HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](icorewebview2historychangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="41db2-276">HistoryChanged écoute la modification de l’historique de navigation du document de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="41db2-276">HistoryChanged listens to the change of navigation history for the top level document.</span></span> <span data-ttu-id="41db2-277">Utilisez HistoryChanged pour vérifier si la valeur CanGoBack/CanGoForward a changé.</span><span class="sxs-lookup"><span data-stu-id="41db2-277">Use HistoryChanged to check if CanGoBack/CanGoForward value has changed.</span></span> <span data-ttu-id="41db2-278">HistoryChanged est également déclenché pour l’utilisation de GoBack/GoForward.</span><span class="sxs-lookup"><span data-stu-id="41db2-278">HistoryChanged also fires for using GoBack/GoForward.</span></span> <span data-ttu-id="41db2-279">HistoryChanged se déclenche après SourceChanged et ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="41db2-279">HistoryChanged fires after SourceChanged and ContentLoading.</span></span>

```cpp
    // Register a handler for the HistoryChanged event.
    // Update the Back, Forward buttons.
    CHECK_FAILURE(m_webView->add_HistoryChanged(
        Callback<ICoreWebView2HistoryChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                BOOL canGoBack;
                BOOL canGoForward;
                sender->get_CanGoBack(&canGoBack);
                sender->get_CanGoForward(&canGoForward);
                m_toolbar->SetItemEnabled(Toolbar::Item_BackButton, canGoBack);
                m_toolbar->SetItemEnabled(Toolbar::Item_ForwardButton, canGoForward);

                return S_OK;
            })
            .Get(),
        &m_historyChangedToken));
```

#### <span data-ttu-id="41db2-280">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="41db2-280">add_NavigationCompleted</span></span> 

<span data-ttu-id="41db2-281">Ajoutez un gestionnaire d’événements pour l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="41db2-281">Add an event handler for the NavigationCompleted event.</span></span>

> <span data-ttu-id="41db2-282">[add_NavigationCompleted](#add_navigationcompleted)par le biais du[mot de passe](icorewebview2navigationcompletedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="41db2-282">public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="41db2-283">NavigationCompleted se déclenche lorsque l’affichage du WebView est complètement chargé (le corps. OnLoad a été déclenché) ou le chargement s’est arrêté avec une erreur.</span><span class="sxs-lookup"><span data-stu-id="41db2-283">NavigationCompleted fires when the WebView has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

```cpp
    // Register a handler for the NavigationCompleted event.
    // Check whether the navigation succeeded, and if not, do something.
    // Also update the Cancel buttons.
    CHECK_FAILURE(m_webView->add_NavigationCompleted(
        Callback<ICoreWebView2NavigationCompletedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2NavigationCompletedEventArgs* args)
                -> HRESULT {
                BOOL success;
                CHECK_FAILURE(args->get_IsSuccess(&success));
                if (!success)
                {
                    COREWEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    if (webErrorStatus == COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }
                m_toolbar->SetItemEnabled(Toolbar::Item_CancelButton, false);
                m_toolbar->SetItemEnabled(Toolbar::Item_ReloadButton, true);
                return S_OK;
            })
            .Get(),
        &m_navigationCompletedToken));
```

#### <span data-ttu-id="41db2-284">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="41db2-284">add_NavigationStarting</span></span> 

<span data-ttu-id="41db2-285">Ajoutez un gestionnaire d’événements pour l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="41db2-285">Add an event handler for the NavigationStarting event.</span></span>

> <span data-ttu-id="41db2-286">[add_NavigationStarting](#add_navigationstarting)par le biais du[mot de passe](icorewebview2navigationstartingeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="41db2-286">public HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="41db2-287">NavigationStarting se déclenche lorsque le frame principal WebView demande une autorisation pour accéder à un URI différent.</span><span class="sxs-lookup"><span data-stu-id="41db2-287">NavigationStarting fires when the WebView main frame is requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="41db2-288">Cela se déclenche également pour les redirections.</span><span class="sxs-lookup"><span data-stu-id="41db2-288">This will fire for redirects as well.</span></span>

<span data-ttu-id="41db2-289">Les navigations correspondantes peuvent être bloquées jusqu’à ce que le gestionnaire d’événements renvoie.</span><span class="sxs-lookup"><span data-stu-id="41db2-289">Corresponding navigations can be blocked until the event handler returns.</span></span>

```cpp
    // Register a handler for the NavigationStarting event.
    // This handler will check the domain being navigated to, and if the domain
    // matches a list of blocked sites, it will cancel the navigation and
    // possibly display a warning page.  It will also disable JavaScript on
    // selected websites.
    CHECK_FAILURE(m_webView->add_NavigationStarting(
        Callback<ICoreWebView2NavigationStartingEventHandler>(
            [this](ICoreWebView2* sender,
                   ICoreWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));

            // If the user clicked a link to navigate, show a warning page.
            BOOL userInitiated;
            CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
        }
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
        return S_OK;
    }).Get(), &m_navigationStartingToken));
```

#### <span data-ttu-id="41db2-290">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="41db2-290">add_NewWindowRequested</span></span> 

<span data-ttu-id="41db2-291">Ajoutez un gestionnaire d’événements pour l’événement NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="41db2-291">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="41db2-292">[add_NewWindowRequested](#add_newwindowrequested)par le biais du[mot de passe](icorewebview2newwindowrequestedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="41db2-292">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](icorewebview2newwindowrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="41db2-293">NewWindowRequested se déclenche lorsque le contenu à l’intérieur des requêtes WebView permet d’ouvrir une nouvelle fenêtre, par exemple par le biais de Window. Open.</span><span class="sxs-lookup"><span data-stu-id="41db2-293">NewWindowRequested fires when content inside the WebView requests to open a new window, such as through window.open.</span></span> <span data-ttu-id="41db2-294">L’application peut transmettre un WebView cible qui sera considéré comme la fenêtre ouverte.</span><span class="sxs-lookup"><span data-stu-id="41db2-294">The app can pass a target WebView that will be considered the opened window.</span></span>

<span data-ttu-id="41db2-295">Les scripts générés dans la nouvelle fenêtre demandée peuvent être bloqués jusqu’à ce que le gestionnaire d’événements renvoie une valeur de report qui n’est pas prise sur les arguments d’événement.</span><span class="sxs-lookup"><span data-stu-id="41db2-295">Scripts resulted in the new window requested can be blocked until the event handler returns if a deferral is not taken on the event args.</span></span> <span data-ttu-id="41db2-296">Si un report est effectué, les scripts sont bloqués tant que le report n’est pas terminé.</span><span class="sxs-lookup"><span data-stu-id="41db2-296">If a deferral is taken, then scripts are blocked until the deferral is completed.</span></span>

```cpp
    // Register a handler for the NewWindowRequested event.
    // This handler will defer the event, create a new app window, and then once the
    // new window is ready, it'll provide that new window's WebView as the response to
    // the request.
    CHECK_FAILURE(m_webView->add_NewWindowRequested(
        Callback<ICoreWebView2NewWindowRequestedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2NewWindowRequestedEventArgs* args) {
                wil::com_ptr<ICoreWebView2Deferral> deferral;
                CHECK_FAILURE(args->GetDeferral(&deferral));
                AppWindow* newAppWindow;

                wil::com_ptr<ICoreWebView2WindowFeatures> windowFeatures;
                CHECK_FAILURE(args->get_WindowFeatures(&windowFeatures));

                RECT windowRect = {0};
                UINT32 left = 0;
                UINT32 top = 0;
                UINT32 height = 0;
                UINT32 width = 0;
                BOOL shouldHaveToolbar = true;

                BOOL hasPosition = FALSE;
                BOOL hasSize = FALSE;
                CHECK_FAILURE(windowFeatures->HasPosition(&hasPosition));
                CHECK_FAILURE(windowFeatures->HasSize(&hasSize));

                bool useDefaultWindow = true;

                if (!!hasPosition && !!hasSize)
                {
                    CHECK_FAILURE(windowFeatures->get_Left(&left));
                    CHECK_FAILURE(windowFeatures->get_Top(&top));
                    CHECK_FAILURE(windowFeatures->get_Height(&height));
                    CHECK_FAILURE(windowFeatures->get_Width(&width));
                    useDefaultWindow = false;
                }
                CHECK_FAILURE(windowFeatures->get_Toolbar(&shouldHaveToolbar));

                windowRect.left = left;
                windowRect.right = left + (width < s_minNewWindowSize ? s_minNewWindowSize : width);
                windowRect.top = top;
                windowRect.bottom = top + (height < s_minNewWindowSize ? s_minNewWindowSize : height);

                if (!useDefaultWindow)
                {
                  newAppWindow = new AppWindow(m_creationModeId, L"", false, nullptr, true, windowRect, !!shouldHaveToolbar);
                }
                else
                {
                  newAppWindow = new AppWindow(m_creationModeId, L"");
                }
                newAppWindow->m_isPopupWindow = true;
                newAppWindow->m_onWebViewFirstInitialized = [args, deferral, newAppWindow]() {
                    CHECK_FAILURE(args->put_NewWindow(newAppWindow->m_webView.get()));
                    CHECK_FAILURE(args->put_Handled(TRUE));
                    CHECK_FAILURE(deferral->Complete());
                };

                return S_OK;
            })
            .Get(),
        nullptr));
```

#### <span data-ttu-id="41db2-297">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="41db2-297">add_PermissionRequested</span></span> 

<span data-ttu-id="41db2-298">Ajoutez un gestionnaire d’événements pour l’événement PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="41db2-298">Add an event handler for the PermissionRequested event.</span></span>

> <span data-ttu-id="41db2-299">[add_PermissionRequested](#add_permissionrequested)par le biais du[mot de passe](icorewebview2permissionrequestedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="41db2-299">public HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](icorewebview2permissionrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="41db2-300">PermissionRequested se déclenche lorsque le contenu d’un WebView demande l’autorisation d’accéder à des ressources privilégiées.</span><span class="sxs-lookup"><span data-stu-id="41db2-300">PermissionRequested fires when content in a WebView requests permission to access some privileged resources.</span></span>

<span data-ttu-id="41db2-301">Si aucun report n’est appliqué sur les arguments d’événement, les scripts suivants peuvent être bloqués jusqu’à ce que le gestionnaire d’événements renvoie.</span><span class="sxs-lookup"><span data-stu-id="41db2-301">If a deferral is not taken on the event args, the subsequent scripts can be blocked until the event handler returns.</span></span> <span data-ttu-id="41db2-302">Si un report est effectué, les scripts sont bloqués tant que le report n’est pas terminé.</span><span class="sxs-lookup"><span data-stu-id="41db2-302">If a deferral is taken, then the scripts are blocked until the deferral is completed.</span></span>

```cpp
    // Register a handler for the PermissionRequested event.
    // This handler prompts the user to allow or deny the request.
    CHECK_FAILURE(m_webView->add_PermissionRequested(
        Callback<ICoreWebView2PermissionRequestedEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2PermissionRequestedEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        COREWEBVIEW2_PERMISSION_KIND kind = COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION;
        BOOL userInitiated = FALSE;

        CHECK_FAILURE(args->get_Uri(&uri));
        CHECK_FAILURE(args->get_PermissionKind(&kind));
        CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));

        std::wstring message = L"Do you want to grant permission for ";
        message += NameOfPermissionKind(kind);
        message += L" to the website at ";
        message += uri.get();
        message += L"?\n\n";
        message += (userInitiated
            ? L"This request came from a user gesture."
            : L"This request did not come from a user gesture.");

        int response = MessageBox(nullptr, message.c_str(), L"Permission Request",
                                   MB_YESNOCANCEL | MB_ICONWARNING);

        COREWEBVIEW2_PERMISSION_STATE state =
              response == IDYES ? COREWEBVIEW2_PERMISSION_STATE_ALLOW
            : response == IDNO  ? COREWEBVIEW2_PERMISSION_STATE_DENY
            :                     COREWEBVIEW2_PERMISSION_STATE_DEFAULT;
        CHECK_FAILURE(args->put_State(state));

        return S_OK;
    }).Get(), &m_permissionRequestedToken));
```

#### <span data-ttu-id="41db2-303">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="41db2-303">add_ProcessFailed</span></span> 

<span data-ttu-id="41db2-304">Ajoutez un gestionnaire d’événements pour l’événement ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="41db2-304">Add an event handler for the ProcessFailed event.</span></span>

> <span data-ttu-id="41db2-305">[add_ProcessFailed](#add_processfailed)par le biais du[mot de passe](icorewebview2processfailedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="41db2-305">public HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](icorewebview2processfailedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="41db2-306">ProcessFailed se déclenche quand un processus WebView est arrêté de manière inattendue ou cesse de répondre.</span><span class="sxs-lookup"><span data-stu-id="41db2-306">ProcessFailed fires when a WebView process is terminated unexpectedly or becomes unresponsive.</span></span>

```cpp
    // Register a handler for the ProcessFailed event.
    // This handler checks if the browser process failed, and asks the user if
    // they want to recreate the webview.
    CHECK_FAILURE(m_webView->add_ProcessFailed(
        Callback<ICoreWebView2ProcessFailedEventHandler>(
            [this](ICoreWebView2* sender,
                ICoreWebView2ProcessFailedEventArgs* args) -> HRESULT
    {
        COREWEBVIEW2_PROCESS_FAILED_KIND failureType;
        CHECK_FAILURE(args->get_ProcessFailedKind(&failureType));
        if (failureType == COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED)
        {
            int button = MessageBox(
                m_appWindow->GetMainWindow(),
                L"Browser process exited unexpectedly.  Recreate webview?",
                L"Browser process exited",
                MB_YESNO);
            if (button == IDYES)
            {
                m_appWindow->ReinitializeWebView();
            }
        }
        else if (failureType == COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE)
        {
            int button = MessageBox(
                m_appWindow->GetMainWindow(),
                L"Browser render process has stopped responding.  Recreate webview?",
                L"Web page unresponsive", MB_YESNO);
            if (button == IDYES)
            {
                m_appWindow->ReinitializeWebView();
            }
        }
        else if (failureType == COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED)
        {
            int button = MessageBox(
                m_appWindow->GetMainWindow(),
                L"Browser render process exited unexpectedly. Reload page?",
                L"Web page unresponsive", MB_YESNO);
            if (button == IDYES)
            {
                CHECK_FAILURE(m_webView->Reload());
            }
        }
        return S_OK;
    }).Get(), &m_processFailedToken));
```

#### <span data-ttu-id="41db2-307">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="41db2-307">add_ScriptDialogOpening</span></span> 

<span data-ttu-id="41db2-308">Ajoutez un gestionnaire d’événements pour l’événement ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="41db2-308">Add an event handler for the ScriptDialogOpening event.</span></span>

> <span data-ttu-id="41db2-309">[add_ScriptDialogOpening](#add_scriptdialogopening)par le biais du[mot de passe](icorewebview2scriptdialogopeningeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="41db2-309">public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](icorewebview2scriptdialogopeningeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="41db2-310">ScriptDialogOpening se déclenche quand une boîte de dialogue JavaScript (alerte, confirmation, invite ou beforeunload) s’affiche pour le WebView.</span><span class="sxs-lookup"><span data-stu-id="41db2-310">ScriptDialogOpening fires when a JavaScript dialog (alert, confirm, prompt, or beforeunload) will show for the webview.</span></span> <span data-ttu-id="41db2-311">Cet événement est déclenché uniquement si la propriété ICoreWebView2Settings:: AreDefaultScriptDialogsEnabled est définie sur false.</span><span class="sxs-lookup"><span data-stu-id="41db2-311">This event only fires if the ICoreWebView2Settings::AreDefaultScriptDialogsEnabled property is set to false.</span></span> <span data-ttu-id="41db2-312">L’événement ScriptDialogOpening peut être utilisé pour supprimer des boîtes de dialogue ou remplacer les boîtes de dialogue par défaut par des boîtes de dialogue personnalisées.</span><span class="sxs-lookup"><span data-stu-id="41db2-312">The ScriptDialogOpening event can be used to suppress dialogs or replace default dialogs with custom dialogs.</span></span>

<span data-ttu-id="41db2-313">Si aucun report n’est appliqué sur les arguments d’événement, les scripts suivants peuvent être bloqués jusqu’à ce que le gestionnaire d’événements renvoie.</span><span class="sxs-lookup"><span data-stu-id="41db2-313">If a deferral is not taken on the event args, the subsequent scripts can be blocked until the event handler returns.</span></span> <span data-ttu-id="41db2-314">Si un report est effectué, les scripts sont bloqués tant que le report n’est pas terminé.</span><span class="sxs-lookup"><span data-stu-id="41db2-314">If a deferral is taken, then the scripts are blocked until the deferral is completed.</span></span>

```cpp
    // Register a handler for the ScriptDialogOpening event.
    // This handler will set up a custom prompt dialog for the user,
    // and may defer the event if the setting to defer dialogs is enabled.
    CHECK_FAILURE(m_webView->add_ScriptDialogOpening(
        Callback<ICoreWebView2ScriptDialogOpeningEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2ScriptDialogOpeningEventArgs* args) -> HRESULT
    {
        wil::com_ptr<ICoreWebView2ScriptDialogOpeningEventArgs> eventArgs = args;
        auto showDialog = [this, eventArgs]
        {
            wil::unique_cotaskmem_string uri;
            COREWEBVIEW2_SCRIPT_DIALOG_KIND type;
            wil::unique_cotaskmem_string message;
            wil::unique_cotaskmem_string defaultText;

            CHECK_FAILURE(eventArgs->get_Uri(&uri));
            CHECK_FAILURE(eventArgs->get_Kind(&type));
            CHECK_FAILURE(eventArgs->get_Message(&message));
            CHECK_FAILURE(eventArgs->get_DefaultText(&defaultText));

            std::wstring promptString = std::wstring(L"The page at '")
                + uri.get() + L"' says:";
            TextInputDialog dialog(
                m_appWindow->GetMainWindow(),
                L"Script Dialog",
                promptString.c_str(),
                message.get(),
                defaultText.get(),
                /* readonly */ type != COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT);
            if (dialog.confirmed)
            {
                CHECK_FAILURE(eventArgs->put_ResultText(dialog.input.c_str()));
                CHECK_FAILURE(eventArgs->Accept());
            }
        };

        if (m_deferScriptDialogs)
        {
            wil::com_ptr<ICoreWebView2Deferral> deferral;
            CHECK_FAILURE(args->GetDeferral(&deferral));
            m_completeDeferredDialog = [showDialog, deferral]
            {
                showDialog();
                CHECK_FAILURE(deferral->Complete());
            };
        }
        else
        {
            showDialog();
        }

        return S_OK;
    }).Get(), &m_scriptDialogOpeningToken));
```

#### <span data-ttu-id="41db2-315">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="41db2-315">add_SourceChanged</span></span> 

<span data-ttu-id="41db2-316">Ajoutez un gestionnaire d’événements pour l’événement SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="41db2-316">Add an event handler for the SourceChanged event.</span></span>

> <span data-ttu-id="41db2-317">[add_SourceChanged](#add_sourcechanged)par le biais du[mot de passe](icorewebview2sourcechangedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="41db2-317">public HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](icorewebview2sourcechangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="41db2-318">SourceChanged se déclenche lorsque la propriété source change.</span><span class="sxs-lookup"><span data-stu-id="41db2-318">SourceChanged fires when the Source property changes.</span></span> <span data-ttu-id="41db2-319">L’utilisation de l’fonction SourceChanged est déclenchée pour accéder à un site ou à un fragment de navigation différent.</span><span class="sxs-lookup"><span data-stu-id="41db2-319">SourceChanged fires for navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="41db2-320">Il ne se déclenchera pas pour les autres types de navigation, tels que les recharges de page ou l’historique. pushState avec la même URL que la page active.</span><span class="sxs-lookup"><span data-stu-id="41db2-320">It will not fire for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span> <span data-ttu-id="41db2-321">SourceChanged se déclenche avant ContentLoading pour la navigation vers un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="41db2-321">SourceChanged fires before ContentLoading for navigation to a new document.</span></span>

```cpp
    // Register a handler for the SourceChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_SourceChanged(
        Callback<ICoreWebView2SourceChangedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2SourceChangedEventArgs* args)
                -> HRESULT {
                wil::unique_cotaskmem_string uri;
                sender->get_Source(&uri);
                if (wcscmp(uri.get(), L"about:blank") == 0)
                {
                    uri = wil::make_cotaskmem_string(L"");
                }
                SetWindowText(GetAddressBar(), uri.get());

                return S_OK;
            })
            .Get(),
        &m_sourceChangedToken));
```

#### <span data-ttu-id="41db2-322">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="41db2-322">add_WebMessageReceived</span></span> 

<span data-ttu-id="41db2-323">Ajoutez un gestionnaire d’événements pour l’événement WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="41db2-323">Add an event handler for the WebMessageReceived event.</span></span>

> <span data-ttu-id="41db2-324">[add_WebMessageReceived](#add_webmessagereceived)par le biais[ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="41db2-324">public HRESULT [add_WebMessageReceived](#add_webmessagereceived)([ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) \* handler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="41db2-325">WebMessageReceived se déclenche lorsque le paramètre ICoreWebView2Settings:: IsWebMessageEnabled est défini et que le document de niveau supérieur de l’appel WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="41db2-325">WebMessageReceived fires when the ICoreWebView2Settings::IsWebMessageEnabled setting is set and the top level document of the WebView calls `window.chrome.webview.postMessage`.</span></span> <span data-ttu-id="41db2-326">La fonction postMessage est l' `void postMessage(object)` emplacement de tout objet pris en charge par la conversion JSON.</span><span class="sxs-lookup"><span data-stu-id="41db2-326">The postMessage function is `void postMessage(object)` where object is any object supported by JSON conversion.</span></span>

```html
        window.chrome.webview.addEventListener('message', arg => {
            if ("SetColor" in arg.data) {
                document.getElementById("colorable").style.color = arg.data.SetColor;
            }
            if ("WindowBounds" in arg.data) {
                document.getElementById("window-bounds").value = arg.data.WindowBounds;
            }
        });

        function SetTitleText() {
            let titleText = document.getElementById("title-text");
            window.chrome.webview.postMessage(`SetTitleText ${titleText.value}`);
        }
        function GetWindowBounds() {
            window.chrome.webview.postMessage("GetWindowBounds");
        }
```
 <span data-ttu-id="41db2-327">Lorsque postMessage est appelé, la méthode Invoke du gestionnaire est appelée avec le paramètre d’objet postMessage converti en chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="41db2-327">When postMessage is called, the handler's Invoke method will be called with the postMessage's object parameter converted to a JSON string.</span></span>

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<ICoreWebView2WebMessageReceivedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->TryGetWebMessageAsString(&messageRaw));
        std::wstring message = messageRaw.get();

        if (message.compare(0, 13, L"SetTitleText ") == 0)
        {
            m_appWindow->SetTitleText(message.substr(13).c_str());
        }
        else if (message.compare(L"GetWindowBounds") == 0)
        {
            RECT bounds = m_appWindow->GetWindowBounds();
            std::wstring reply =
                L"{\"WindowBounds\":\"Left:" + std::to_wstring(bounds.left)
                + L"\\nTop:" + std::to_wstring(bounds.top)
                + L"\\nRight:" + std::to_wstring(bounds.right)
                + L"\\nBottom:" + std::to_wstring(bounds.bottom)
                + L"\"}";
            CHECK_FAILURE(sender->PostWebMessageAsJson(reply.c_str()));
        }
        return S_OK;
    }).Get(), &m_webMessageReceivedToken));
```

#### <span data-ttu-id="41db2-328">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="41db2-328">add_WebResourceRequested</span></span> 

<span data-ttu-id="41db2-329">Ajoutez un gestionnaire d’événements pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="41db2-329">Add an event handler for the WebResourceRequested event.</span></span>

> <span data-ttu-id="41db2-330">[add_WebResourceRequested](#add_webresourcerequested)par le biais du[mot de passe](icorewebview2webresourcerequestedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="41db2-330">public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](icorewebview2webresourcerequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="41db2-331">WebResourceRequested se déclenche lorsque WebView effectue une demande d’URL à un filtre d’URL et de contexte de ressources correspondant qui a été ajouté à l’aide de AddWebResourceRequestedFilter.</span><span class="sxs-lookup"><span data-stu-id="41db2-331">WebResourceRequested fires when the WebView is performing a URL request to a matching URL and resource context filter that was added with AddWebResourceRequestedFilter.</span></span> <span data-ttu-id="41db2-332">Au moins un filtre doit être ajouté pour que l’événement se déclenche.</span><span class="sxs-lookup"><span data-stu-id="41db2-332">At least one filter must be added for the event to fire.</span></span>

<span data-ttu-id="41db2-333">La ressource Web demandée peut être bloquée jusqu’à ce que le gestionnaire d’événements renvoie une valeur qui n’est pas prise sur les arguments d’événement.</span><span class="sxs-lookup"><span data-stu-id="41db2-333">The web resource requested can be blocked until the event handler returns if a deferral is not taken on the event args.</span></span> <span data-ttu-id="41db2-334">Si un report est effectué, la ressource Web demandée est bloquée jusqu’à ce que le report soit terminé.</span><span class="sxs-lookup"><span data-stu-id="41db2-334">If a deferral is taken, then the web resource requested is blocked until the deferral is completed.</span></span>

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<ICoreWebView2WebResourceRequestedEventHandler>(
                    [this](
                        ICoreWebView2* sender,
                        ICoreWebView2WebResourceRequestedEventArgs* args) {
                        COREWEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            args->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<ICoreWebView2WebResourceResponse> response;
                        CHECK_FAILURE(m_webViewEnvironment->CreateWebResourceResponse(
                            nullptr, 403 /*NoContent*/, L"Blocked", L"", &response));
                        CHECK_FAILURE(args->put_Response(response.get()));
                        return S_OK;
                    })
                    .Get(),
                &m_webResourceRequestedTokenForImageBlocking));
        }
        else
        {
            CHECK_FAILURE(m_webView->remove_WebResourceRequested(
                m_webResourceRequestedTokenForImageBlocking));
        }
```

#### <span data-ttu-id="41db2-335">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="41db2-335">add_WindowCloseRequested</span></span> 

<span data-ttu-id="41db2-336">Ajoutez un gestionnaire d’événements pour l’événement WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="41db2-336">Add an event handler for the WindowCloseRequested event.</span></span>

> <span data-ttu-id="41db2-337">[add_WindowCloseRequested](#add_windowcloserequested)par le biais du[mot de passe](icorewebview2windowcloserequestedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="41db2-337">public HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](icorewebview2windowcloserequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="41db2-338">WindowCloseRequested se déclenche lorsque le contenu à l’intérieur du WebView est requis pour fermer la fenêtre, par exemple, après l’appel de Window. Close.</span><span class="sxs-lookup"><span data-stu-id="41db2-338">WindowCloseRequested fires when content inside the WebView requested to close the window, such as after window.close is called.</span></span> <span data-ttu-id="41db2-339">L’application doit fermer la fenêtre WebView et la fenêtre de l’application associée si cela est pertinent pour l’application.</span><span class="sxs-lookup"><span data-stu-id="41db2-339">The app should close the WebView and related app window if that makes sense to the app.</span></span>

```cpp
    // Register a handler for the WindowCloseRequested event.
    // This handler will close the app window if it is not the main window.
    CHECK_FAILURE(m_webView->add_WindowCloseRequested(
        Callback<ICoreWebView2WindowCloseRequestedEventHandler>([this](
                                                                    ICoreWebView2* sender,
                                                                    IUnknown* args) {
            if (m_isPopupWindow)
            {
                CloseAppWindow();
            }
            return S_OK;
        }).Get(),
        nullptr));
```

#### <span data-ttu-id="41db2-340">AddHostObjectToScript</span><span class="sxs-lookup"><span data-stu-id="41db2-340">AddHostObjectToScript</span></span> 

<span data-ttu-id="41db2-341">Ajoutez l’objet hôte fourni au script qui s’exécute sur le WebView avec le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="41db2-341">Add the provided host object to script running in the WebView with the specified name.</span></span>

> <span data-ttu-id="41db2-342">public HRESULT [AddHostObjectToScript](#addhostobjecttoscript)(LPCWSTR Name, variant \* Object)</span><span class="sxs-lookup"><span data-stu-id="41db2-342">public HRESULT [AddHostObjectToScript](#addhostobjecttoscript)(LPCWSTR name, VARIANT \* object)</span></span>

<span data-ttu-id="41db2-343">Les objets hôtes sont exposés en tant que proxy d’objet hôte via `window.chrome.webview.hostObjects.<name>` .</span><span class="sxs-lookup"><span data-stu-id="41db2-343">Host objects are exposed as host object proxies via `window.chrome.webview.hostObjects.<name>`.</span></span> <span data-ttu-id="41db2-344">Les proxies d’objet hôte sont promet et sont résolus en objet représentant l’objet hôte.</span><span class="sxs-lookup"><span data-stu-id="41db2-344">Host object proxies are promises and will resolve to an object representing the host object.</span></span> <span data-ttu-id="41db2-345">La promesse est refusée si l’application n’a pas ajouté d’objet portant le nom.</span><span class="sxs-lookup"><span data-stu-id="41db2-345">The promise is rejected if the app has not added an object with the name.</span></span> <span data-ttu-id="41db2-346">Lorsque le code JavaScript accède à une propriété ou une méthode de l’objet, une promesse est renvoyée, qui est résolue en fonction de la valeur renvoyée par l’hôte de la propriété ou de la méthode, ou rejetée en cas d’erreur, comme il n’y a pas de propriété ou de méthode sur l’objet ou les paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="41db2-346">When JavaScript code access a property or method of the object, a promise is return, which will resolve to the value returned from the host for the property or method, or rejected in case of error such as there is no such property or method on the object or parameters are invalid.</span></span> <span data-ttu-id="41db2-347">Par exemple, lorsque le code de l’application effectue les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="41db2-347">For example, when the application code does the following:</span></span>

```
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddHostObjectToScript(L"host_object", &host);
```

<span data-ttu-id="41db2-348">Le code JavaScript de l’affichage WebView sera en mesure d’accéder à appObject comme suit, puis d’accéder aux attributs et méthodes de appObject:</span><span class="sxs-lookup"><span data-stu-id="41db2-348">JavaScript code in the WebView will be able to access appObject as following and then access attributes and methods of appObject:</span></span>

```
let app_object = await window.chrome.webview.hostObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

<span data-ttu-id="41db2-349">Notez qu’en ce qui concerne les types simples, IDispatch et Array sont pris en charge, le type IUnknown, VT_DECIMAL ou VT_RECORD variant n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="41db2-349">Note that while simple types, IDispatch and array are supported, generic IUnknown, VT_DECIMAL, or VT_RECORD variant is not supported.</span></span> <span data-ttu-id="41db2-350">Les objets JavaScript distants comme les fonctions de rappel sont représentés sous la forme d’un VT_DISPATCH VARIANT avec l’objet qui implémente IDispatch.</span><span class="sxs-lookup"><span data-stu-id="41db2-350">Remote JavaScript objects like callback functions are represented as an VT_DISPATCH VARIANT with the object implementing IDispatch.</span></span> <span data-ttu-id="41db2-351">La méthode de rappel JavaScript doit être appelée à l’aide de DISPID_VALUE pour le DISPID.</span><span class="sxs-lookup"><span data-stu-id="41db2-351">The JavaScript callback method may be invoked using DISPID_VALUE for the DISPID.</span></span> <span data-ttu-id="41db2-352">Les tableaux imbriqués sont pris en charge jusqu’à une profondeur de 3.</span><span class="sxs-lookup"><span data-stu-id="41db2-352">Nested arrays are supported up to a depth of 3.</span></span> <span data-ttu-id="41db2-353">Les matrices de par types de référence ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="41db2-353">Arrays of by reference types are not supported.</span></span> <span data-ttu-id="41db2-354">VT_EMPTY et VT_NULL sont mappés dans JavaScript en tant que valeurs NULL.</span><span class="sxs-lookup"><span data-stu-id="41db2-354">VT_EMPTY and VT_NULL are mapped into JavaScript as null.</span></span> <span data-ttu-id="41db2-355">Dans JavaScript, les valeurs NULL et non définies sont mappées à VT_EMPTY.</span><span class="sxs-lookup"><span data-stu-id="41db2-355">In JavaScript null and undefined are mapped to VT_EMPTY.</span></span>

<span data-ttu-id="41db2-356">De plus, tous les objets hôtes sont exposés en tant que `window.chrome.webview.hostObjects.sync.<name>` .</span><span class="sxs-lookup"><span data-stu-id="41db2-356">Additionally, all host objects are exposed as `window.chrome.webview.hostObjects.sync.<name>`.</span></span> <span data-ttu-id="41db2-357">Ici, les objets hôtes sont exposés en tant que proxy d’objets hôtes synchrones.</span><span class="sxs-lookup"><span data-stu-id="41db2-357">Here the host objects are exposed as synchronous host object proxies.</span></span> <span data-ttu-id="41db2-358">Celles-ci ne sont pas promesse et les appels de fonctions ou d’accès aux propriétés empêchent de manière synchrone l’exécution d’un script en attente de communication croisée pour que le code hôte s’exécute.</span><span class="sxs-lookup"><span data-stu-id="41db2-358">These are not promises and calls to functions or property access synchronously block running script waiting to communicate cross process for the host code to run.</span></span> <span data-ttu-id="41db2-359">En conséquence, cela peut entraîner des problèmes de fiabilité et nous vous conseillons d’utiliser l’API asynchrone basée sur la promesse `window.chrome.webview.hostObjects.<name>` décrite ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="41db2-359">Accordingly this can result in reliability issues and it is recommended that you use the promise based asynchronous `window.chrome.webview.hostObjects.<name>` API described above.</span></span>

<span data-ttu-id="41db2-360">Les proxies d’objet hôte synchrone et les proxys d’objets hôtes asynchrones peuvent à la fois proxy le même objet hôte.</span><span class="sxs-lookup"><span data-stu-id="41db2-360">Synchronous host object proxies and asynchronous host object proxies can both proxy the same host object.</span></span> <span data-ttu-id="41db2-361">Les modifications distantes apportées par un proxy seront reflétées dans tout autre proxy de ce même objet hôte, qu’il s’agisse de proxys et synchrones ou asynchrones.</span><span class="sxs-lookup"><span data-stu-id="41db2-361">Remote changes made by one proxy will be reflected in any other proxy of that same host object whether the other proxies and synchronous or asynchronous.</span></span>

<span data-ttu-id="41db2-362">Si JavaScript est bloqué lors d’un appel asynchrone au code natif, ce code natif ne peut pas rappeler JavaScript.</span><span class="sxs-lookup"><span data-stu-id="41db2-362">While JavaScript is blocked on a synchronous call to native code, that native code is unable to call back to JavaScript.</span></span> <span data-ttu-id="41db2-363">Les tentatives d’une telle opération échoueront avec HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).</span><span class="sxs-lookup"><span data-stu-id="41db2-363">Attempts to do so will fail with HRESULT_FROM_WIN32(ERROR_POSSIBLE_DEADLOCK).</span></span>

<span data-ttu-id="41db2-364">Les proxies d’objets hôtes sont des objets proxy JavaScript qui interceptent l’ensemble des appels de propriété Get, de jeu de propriétés et de méthode.</span><span class="sxs-lookup"><span data-stu-id="41db2-364">Host object proxies are JavaScript Proxy objects that intercept all property get, property set, and method invocations.</span></span> <span data-ttu-id="41db2-365">Les propriétés ou méthodes qui font partie du prototype de fonction ou d’objet sont exécutées localement.</span><span class="sxs-lookup"><span data-stu-id="41db2-365">Properties or methods that are a part of the Function or Object prototype are run locally.</span></span> <span data-ttu-id="41db2-366">De plus, toute propriété ou méthode du tableau `chrome.webview.hostObjects.options.forceLocalProperties` sera également exécutée localement.</span><span class="sxs-lookup"><span data-stu-id="41db2-366">Additionally any property or method in the array `chrome.webview.hostObjects.options.forceLocalProperties` will also be run locally.</span></span> <span data-ttu-id="41db2-367">Par exemple, vous pouvez inclure des méthodes facultatives ayant une signification dans JavaScript comme `toJSON` et `Symbol.toPrimitive` .</span><span class="sxs-lookup"><span data-stu-id="41db2-367">This defaults to including optional methods that have meaning in JavaScript like `toJSON` and `Symbol.toPrimitive`.</span></span> <span data-ttu-id="41db2-368">Vous pouvez en ajouter d’autres à ce tableau selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="41db2-368">You can add more to this array as required.</span></span>

<span data-ttu-id="41db2-369">Il existe une méthode `chrome.webview.hostObjects.cleanupSome` qui consiste à utiliser au mieux le nettoyage de la mémoire proxy d’objet hôte.</span><span class="sxs-lookup"><span data-stu-id="41db2-369">There's a method `chrome.webview.hostObjects.cleanupSome` that will best effort garbage collect host object proxies.</span></span>

<span data-ttu-id="41db2-370">Les proxys d’objets hôtes possèdent également les méthodes suivantes qui s’exécutent en local:</span><span class="sxs-lookup"><span data-stu-id="41db2-370">Host object proxies additionally have the following methods which run locally:</span></span>

* <span data-ttu-id="41db2-371">applyHostFunction, getHostProperty, setHostProperty: effectue un appel de méthode, Get de propriété ou jeu de propriétés sur l’objet hôte.</span><span class="sxs-lookup"><span data-stu-id="41db2-371">applyHostFunction, getHostProperty, setHostProperty: Perform a method invocation, property get, or property set on the host object.</span></span> <span data-ttu-id="41db2-372">Vous pouvez utiliser ces éléments pour forcer explicitement une méthode ou une propriété à s’exécuter à distance en cas de conflit entre une méthode locale ou une propriété.</span><span class="sxs-lookup"><span data-stu-id="41db2-372">You can use these to explicitly force a method or property to run remotely if there is a conflicting local method or property.</span></span> <span data-ttu-id="41db2-373">Par exemple, `proxy.toString()` exécute la méthode ToString locale sur l’objet proxy.</span><span class="sxs-lookup"><span data-stu-id="41db2-373">For instance, `proxy.toString()` will run the local toString method on the proxy object.</span></span> <span data-ttu-id="41db2-374">Mais `proxy.applyHostFunction('toString')` s’exécute `toString` plutôt sur l’objet proxy de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="41db2-374">But `proxy.applyHostFunction('toString')` runs `toString` on the host proxied object instead.</span></span>

* <span data-ttu-id="41db2-375">getLocalProperty, setLocalProperty: exécuter une propriété Get ou Property Set localement.</span><span class="sxs-lookup"><span data-stu-id="41db2-375">getLocalProperty, setLocalProperty: Perform property get, or property set locally.</span></span> <span data-ttu-id="41db2-376">Vous pouvez utiliser ces méthodes pour forcer l’affichage ou la définition d’une propriété sur le proxy d’objet hôte lui-même plutôt que sur l’objet hôte qu’elle représente.</span><span class="sxs-lookup"><span data-stu-id="41db2-376">You can use these methods to force getting or setting a property on the host object proxy itself rather than on the host object it represents.</span></span> <span data-ttu-id="41db2-377">Par exemple, obtiendrez `proxy.unknownProperty` la propriété nommée `unknownProperty` de l’objet proxy de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="41db2-377">For instance, `proxy.unknownProperty` will get the property named `unknownProperty` from the host proxied object.</span></span> <span data-ttu-id="41db2-378">Toutefois `proxy.getLocalProperty('unknownProperty')` , vous obtiendrez la valeur de la propriété `unknownProperty` sur l’objet proxy lui-même.</span><span class="sxs-lookup"><span data-stu-id="41db2-378">But `proxy.getLocalProperty('unknownProperty')` will get the value of the property `unknownProperty` on the proxy object itself.</span></span>

* <span data-ttu-id="41db2-379">synchronisation: les proxys d’objets hôtes asynchrones exposent une méthode de synchronisation qui renvoie une promesse de proxy d’objet hôte synchrone pour le même objet hôte.</span><span class="sxs-lookup"><span data-stu-id="41db2-379">sync: Asynchronous host object proxies expose a sync method which returns a promise for a synchronous host object proxy for the same host object.</span></span> <span data-ttu-id="41db2-380">Par exemple, `chrome.webview.hostObjects.sample.methodCall()` retourne un proxy d’objet hôte asynchrone.</span><span class="sxs-lookup"><span data-stu-id="41db2-380">For example, `chrome.webview.hostObjects.sample.methodCall()` returns an asynchronous host object proxy.</span></span> <span data-ttu-id="41db2-381">Vous pouvez utiliser la `sync` méthode pour obtenir un proxy d’objet hôte synchrone à la place:</span><span class="sxs-lookup"><span data-stu-id="41db2-381">You can use the `sync` method to obtain a synchronous host object proxy instead:</span></span> `const syncProxy = await chrome.webview.hostObjects.sample.methodCall().sync()`

* <span data-ttu-id="41db2-382">Async: les proxys d’objets d’hôte synchrones présentent une méthode Async qui bloque et retourne un proxy d’objet hôte asynchrone pour le même objet hôte.</span><span class="sxs-lookup"><span data-stu-id="41db2-382">async: Synchronous host object proxies expose an async method which blocks and returns an asynchronous host object proxy for the same host object.</span></span> <span data-ttu-id="41db2-383">Par exemple, `chrome.webview.hostObjects.sync.sample.methodCall()` retourne un proxy d’objet hôte synchrone.</span><span class="sxs-lookup"><span data-stu-id="41db2-383">For example, `chrome.webview.hostObjects.sync.sample.methodCall()` returns a synchronous host object proxy.</span></span> <span data-ttu-id="41db2-384">Appel de la `async` méthode sur ce bloc, puis retour d’un proxy d’objet hôte asynchrone pour le même objet hôte:</span><span class="sxs-lookup"><span data-stu-id="41db2-384">Calling the `async` method on this blocks and then returns an asynchronous host object proxy for the same host object:</span></span> `const asyncProxy = chrome.webview.hostObjects.sync.sample.methodCall().async()`

* <span data-ttu-id="41db2-385">ensuite: les proxies d’objet hôte asynchrone possèdent une méthode Then.</span><span class="sxs-lookup"><span data-stu-id="41db2-385">then: Asynchronous host object proxies have a then method.</span></span> <span data-ttu-id="41db2-386">Cela leur permet d’être await.</span><span class="sxs-lookup"><span data-stu-id="41db2-386">This allows them to be awaitable.</span></span> `then` <span data-ttu-id="41db2-387">renverra une promesse qui est résolue en une représentation de l’objet hôte.</span><span class="sxs-lookup"><span data-stu-id="41db2-387">will return a promise that resolves with a representation of the host object.</span></span> <span data-ttu-id="41db2-388">Si le proxy représente un littéral JavaScript, une copie de celui-ci est renvoyée localement.</span><span class="sxs-lookup"><span data-stu-id="41db2-388">If the proxy represents a JavaScript literal then a copy of that is returned locally.</span></span> <span data-ttu-id="41db2-389">Si le proxy représente une fonction, un proxy non-await est retourné.</span><span class="sxs-lookup"><span data-stu-id="41db2-389">If the proxy represents a function then a non-awaitable proxy is returned.</span></span> <span data-ttu-id="41db2-390">Si le proxy représente un objet JavaScript avec une combinaison de propriétés littérales et de propriétés de fonctions, une copie de l’objet est renvoyée avec des propriétés en tant que proxy d’objet hôte.</span><span class="sxs-lookup"><span data-stu-id="41db2-390">If the proxy represents a JavaScript object with a mix of literal properties and function properties, then the a copy of the object is returned with some properties as host object proxies.</span></span>

<span data-ttu-id="41db2-391">Tous les autres appels de propriété et de méthode (autres que les méthodes de proxy d’objet distant, la liste forceLocalProperties et les propriétés des prototypes de fonction et d’objet) s’exécutent à distance.</span><span class="sxs-lookup"><span data-stu-id="41db2-391">All other property and method invocations (other than the above Remote object proxy methods, forceLocalProperties list, and properties on Function and Object prototypes) are run remotely.</span></span> <span data-ttu-id="41db2-392">Les proxys d’objets hôtes asynchrones retournent une promesse qui représente la complétion asynchrone d’appeler la méthode à distance ou d’obtenir la propriété.</span><span class="sxs-lookup"><span data-stu-id="41db2-392">Asynchronous host object proxies return a promise representing asynchronous completion of remotely invoking the method, or getting the property.</span></span> <span data-ttu-id="41db2-393">La promesse se résout une fois les opérations distantes terminées et la promesse de la valeur de l’opération.</span><span class="sxs-lookup"><span data-stu-id="41db2-393">The promise resolves after the remote operations complete and the promises resolve to the resulting value of the operation.</span></span> <span data-ttu-id="41db2-394">Les proxys d’objets hôtes synchrones fonctionnent de la même façon, mais bloquent l’exécution JavaScript et attendez la fin de l’opération à distance.</span><span class="sxs-lookup"><span data-stu-id="41db2-394">Synchronous host object proxies work similarly but block JavaScript execution and wait for the remote operation to complete.</span></span>

<span data-ttu-id="41db2-395">La définition d’une propriété sur un proxy d’objet hôte asynchrone fonctionne légèrement différemment.</span><span class="sxs-lookup"><span data-stu-id="41db2-395">Setting a property on an asynchronous host object proxy works slightly differently.</span></span> <span data-ttu-id="41db2-396">Le jeu renvoie immédiatement et la valeur de retour est la valeur qui sera définie.</span><span class="sxs-lookup"><span data-stu-id="41db2-396">The set returns immediately and the return value is the value that will be set.</span></span> <span data-ttu-id="41db2-397">Il s’agit d’une condition requise de l’objet proxy JavaScript.</span><span class="sxs-lookup"><span data-stu-id="41db2-397">This is a requirement of the JavaScript Proxy object.</span></span> <span data-ttu-id="41db2-398">Si vous avez besoin d’attendre que le jeu de propriétés soit terminé, utilisez la méthode setHostProperty qui renvoie une promesse comme décrit ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="41db2-398">If you need to asynchronously wait for the property set to complete, use the setHostProperty method which returns a promise as described above.</span></span> <span data-ttu-id="41db2-399">La propriété du jeu de propriétés d’objet synchrone se bloque de manière synchrone tant que la propriété est définie.</span><span class="sxs-lookup"><span data-stu-id="41db2-399">Synchronous object property set property synchronously blocks until the property is set.</span></span>

<span data-ttu-id="41db2-400">Par exemple, supposons que vous disposiez d’un objet COM avec l’interface suivante.</span><span class="sxs-lookup"><span data-stu-id="41db2-400">For example, suppose you have a COM object with the following interface</span></span>

```idl
    [uuid(3a14c9c0-bc3e-453f-a314-4ce4a0ec81d8), object, local]
    interface IHostObjectSample : IUnknown
    {
        // Demonstrate basic method call with some parameters and a return value.
        HRESULT MethodWithParametersAndReturnValue([in] BSTR stringParameter, [in] INT integerParameter, [out, retval] BSTR* stringResult);

        // Demonstrate getting and setting a property.
        [propget] HRESULT Property([out, retval] BSTR* stringResult);
        [propput] HRESULT Property([in] BSTR stringValue);

        [propget] HRESULT IndexedProperty(INT index, [out, retval] BSTR * stringResult);
        [propput] HRESULT IndexedProperty(INT index, [in] BSTR stringValue);

        // Demonstrate native calling back into JavaScript.
        HRESULT CallCallbackAsynchronously([in] IDispatch* callbackParameter);

    };
```
 <span data-ttu-id="41db2-401">Nous pouvons ajouter une instance de cette interface dans notre JavaScript avec `AddHostObjectToScript` .</span><span class="sxs-lookup"><span data-stu-id="41db2-401">We can add an instance of this interface into our JavaScript with `AddHostObjectToScript`.</span></span> <span data-ttu-id="41db2-402">Dans le cas présent, vous nommerez ce message `sample` :</span><span class="sxs-lookup"><span data-stu-id="41db2-402">In this case we name it `sample`:</span></span>

```cpp
            VARIANT remoteObjectAsVariant = {};
            m_hostObject.query_to<IDispatch>(&remoteObjectAsVariant.pdispVal);
            remoteObjectAsVariant.vt = VT_DISPATCH;

            // We can call AddHostObjectToScript multiple times in a row without
            // calling RemoveHostObject first. This will replace the previous object
            // with the new object. In our case this is the same object and everything
            // is fine.
            CHECK_FAILURE(
                m_webView->AddHostObjectToScript(L"sample", &remoteObjectAsVariant));
            remoteObjectAsVariant.pdispVal->Release();
```
 <span data-ttu-id="41db2-403">Ensuite, dans le document HTML, vous pouvez utiliser cet objet COM via `chrome.webview.hostObjects.sample` :</span><span class="sxs-lookup"><span data-stu-id="41db2-403">Then in the HTML document we can use this COM object via `chrome.webview.hostObjects.sample`:</span></span>

```html
        document.getElementById("getPropertyAsyncButton").addEventListener("click", async () => {
        const propertyValue = await chrome.webview.hostObjects.sample.property;
        document.getElementById("getPropertyAsyncOutput").textContent = propertyValue;
        });

        document.getElementById("getPropertySyncButton").addEventListener("click", () => {
        const propertyValue = chrome.webview.hostObjects.sync.sample.property;
        document.getElementById("getPropertySyncOutput").textContent = propertyValue;
        });

        document.getElementById("setPropertyAsyncButton").addEventListener("click", async () => {
        const propertyValue = document.getElementById("setPropertyAsyncInput").value;
        // The following line will work but it will return immediately before the property value has actually been set.
        // If you need to set the property and wait for the property to change value, use the setHostProperty function.
        chrome.webview.hostObjects.sample.property = propertyValue;
        document.getElementById("setPropertyAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertyExplicitAsyncButton").addEventListener("click", async () => {
        const propertyValue = document.getElementById("setPropertyExplicitAsyncInput").value;
        // If you care about waiting until the property has actually changed value use the setHostProperty function.
        await chrome.webview.hostObjects.sample.setHostProperty("property", propertyValue);
        document.getElementById("setPropertyExplicitAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertySyncButton").addEventListener("click", () => {
        const propertyValue = document.getElementById("setPropertySyncInput").value;
        chrome.webview.hostObjects.sync.sample.property = propertyValue;
        document.getElementById("setPropertySyncOutput").textContent = "Set";
        });

        document.getElementById("getIndexedPropertyAsyncButton").addEventListener("click", async () => {
        const index = parseInt(document.getElementById("getIndexedPropertyAsyncParam").value);
        const resultValue = await chrome.webview.hostObjects.sample.IndexedProperty[index];
        document.getElementById("getIndexedPropertyAsyncOutput").textContent = resultValue;
        });
        document.getElementById("setIndexedPropertyAsyncButton").addEventListener("click", async () => {
        const index = parseInt(document.getElementById("setIndexedPropertyAsyncParam1").value);
        const value = document.getElementById("setIndexedPropertyAsyncParam2").value;;
        chrome.webview.hostObjects.sample.IndexedProperty[index] = value;
        document.getElementById("setIndexedPropertyAsyncOutput").textContent = "Set";
        });
        document.getElementById("invokeMethodAsyncButton").addEventListener("click", async () => {
        const paramValue1 = document.getElementById("invokeMethodAsyncParam1").value;
        const paramValue2 = parseInt(document.getElementById("invokeMethodAsyncParam2").value);
        const resultValue = await chrome.webview.hostObjects.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
        document.getElementById("invokeMethodAsyncOutput").textContent = resultValue;
        });

        document.getElementById("invokeMethodSyncButton").addEventListener("click", () => {
        const paramValue1 = document.getElementById("invokeMethodSyncParam1").value;
        const paramValue2 = parseInt(document.getElementById("invokeMethodSyncParam2").value);
        const resultValue = chrome.webview.hostObjects.sync.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
        document.getElementById("invokeMethodSyncOutput").textContent = resultValue;
        });

        let callbackCount = 0;
        document.getElementById("invokeCallbackButton").addEventListener("click", async () => {
        chrome.webview.hostObjects.sample.CallCallbackAsynchronously(() => {
        document.getElementById("invokeCallbackOutput").textContent = "Native object called the callback " + (++callbackCount) + " time(s).";
        });
        });
```
<span data-ttu-id="41db2-404">L’exposition d’objets hôtes au script présente des risques en matière de sécurité.</span><span class="sxs-lookup"><span data-stu-id="41db2-404">Exposing host objects to script has security risk.</span></span> <span data-ttu-id="41db2-405">Suivez ces [meilleures pratiques](https://docs.microsoft.com/microsoft-edge/webview2/concepts/security).</span><span class="sxs-lookup"><span data-stu-id="41db2-405">Please follow [best practices](https://docs.microsoft.com/microsoft-edge/webview2/concepts/security).</span></span>

#### <span data-ttu-id="41db2-406">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="41db2-406">AddScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="41db2-407">Ajoutez le code JavaScript fourni à une liste de scripts qui doivent être exécutés après la création de l’objet global, mais avant l’analyse du document HTML et avant l’exécution de tout autre script fourni par le document HTML.</span><span class="sxs-lookup"><span data-stu-id="41db2-407">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>

> <span data-ttu-id="41db2-408">public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR JavaScript, gestionnaire [ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md) \*)</span><span class="sxs-lookup"><span data-stu-id="41db2-408">public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript, [ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="41db2-409">Cette méthode injecte un script qui s’exécute sur tous les navigateurs de documents de niveau supérieur et de page Frame enfant.</span><span class="sxs-lookup"><span data-stu-id="41db2-409">This method injects a script that runs on all top-level document and child frame page navigations.</span></span> <span data-ttu-id="41db2-410">Cette méthode s’exécute de manière asynchrone, et vous devez attendre que le gestionnaire d’achèvement se termine avant l’exécution du script injecté.</span><span class="sxs-lookup"><span data-stu-id="41db2-410">This method runs asynchronously, and you must wait for the completion handler to finish before the injected script is ready to run.</span></span> <span data-ttu-id="41db2-411">Lorsque cette méthode se termine, la méthode du gestionnaire `Invoke` est appelée avec le `id` script injecté.</span><span class="sxs-lookup"><span data-stu-id="41db2-411">When this method completes, the handler's `Invoke` method is called with the `id` of the injected script.</span></span> `id` <span data-ttu-id="41db2-412">est une chaîne.</span><span class="sxs-lookup"><span data-stu-id="41db2-412">is a string.</span></span> <span data-ttu-id="41db2-413">Pour supprimer le script injecté, utilisez `RemoveScriptToExecuteOnDocumentCreated` .</span><span class="sxs-lookup"><span data-stu-id="41db2-413">To remove the injected script, use `RemoveScriptToExecuteOnDocumentCreated`.</span></span>

<span data-ttu-id="41db2-414">Notez que si un document HTML comporte un sandbox d’un type quelconque via les propriétés [sandbox](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) ou l' [en-tête HTTP Content-Security-Policy](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) , ce dernier affectera l’exécution du script.</span><span class="sxs-lookup"><span data-stu-id="41db2-414">Note that if an HTML document has sandboxing of some kind via [sandbox](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) properties or the [Content-Security-Policy HTTP header](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) this will affect the script run here.</span></span> <span data-ttu-id="41db2-415">Par exemple, si le mot clé «allow-modaux» n’est pas défini, les appels à la `alert` fonction seront ignorés.</span><span class="sxs-lookup"><span data-stu-id="41db2-415">So, for example, if the 'allow-modals' keyword is not set then calls to the `alert` function will be ignored.</span></span>

```cpp
// Prompt the user for some script and register it to execute whenever a new page loads.
void ScriptComponent::AddInitializeScript()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Add Initialize Script",
        L"Initialization Script:",
        L"Enter the JavaScript code to run as the initialization script that "
            L"runs before any script in the HTML document.",
    // This example script stops child frames from opening new windows.  Because
    // the initialization script runs before any script in the HTML document, we
    // can trust the results of our checks on window.parent and window.top.
        L"if (window.parent !== window.top) {\r\n"
        L"    delete window.open;\r\n"
        L"}");
    if (dialog.confirmed)
    {
        m_webView->AddScriptToExecuteOnDocumentCreated(
            dialog.input.c_str(),
            Callback<ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler>(
                [this](HRESULT error, PCWSTR id) -> HRESULT
        {
            m_lastInitializeScriptId = id;
            MessageBox(nullptr, id, L"AddScriptToExecuteOnDocumentCreated Id", MB_OK);
            return S_OK;
        }).Get());

    }
}
```

#### <span data-ttu-id="41db2-416">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="41db2-416">AddWebResourceRequestedFilter</span></span> 

<span data-ttu-id="41db2-417">Ajoute un URI et un filtre de contexte de ressources à l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="41db2-417">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>

> <span data-ttu-id="41db2-418">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) constante resourceContext)</span><span class="sxs-lookup"><span data-stu-id="41db2-418">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="41db2-419">Le paramètre URI peut être une chaîne de caractères génériques (' \* ': zéro ou plusieurs; '? ': exactement 1).</span><span class="sxs-lookup"><span data-stu-id="41db2-419">The URI parameter can be a wildcard string ('\*': zero or more, '?': exactly one).</span></span> <span data-ttu-id="41db2-420">nullptr est l’équivalent de L "".</span><span class="sxs-lookup"><span data-stu-id="41db2-420">nullptr is equivalent to L"".</span></span> <span data-ttu-id="41db2-421">Pour plus d’détails sur les filtres de contexte de ressources, voir COREWEBVIEW2_WEB_RESOURCE_CONTEXT Enum.</span><span class="sxs-lookup"><span data-stu-id="41db2-421">See COREWEBVIEW2_WEB_RESOURCE_CONTEXT enum for description of resource context filters.</span></span>

#### <span data-ttu-id="41db2-422">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="41db2-422">CallDevToolsProtocolMethod</span></span> 

<span data-ttu-id="41db2-423">Appelez une méthode DevToolsProtocol asynchrone.</span><span class="sxs-lookup"><span data-stu-id="41db2-423">Call an asynchronous DevToolsProtocol method.</span></span>

> <span data-ttu-id="41db2-424">public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR METHODNAME, LPCWSTR parametersAsJson, gestionnaire [ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](icorewebview2calldevtoolsprotocolmethodcompletedhandler.md) \*)</span><span class="sxs-lookup"><span data-stu-id="41db2-424">public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR methodName, LPCWSTR parametersAsJson, [ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](icorewebview2calldevtoolsprotocolmethodcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="41db2-425">Voir la [visionneuse de protocoles devtools](https://aka.ms/DevToolsProtocolDocs) pour obtenir une liste et une description des méthodes disponibles.</span><span class="sxs-lookup"><span data-stu-id="41db2-425">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list and description of available methods.</span></span> <span data-ttu-id="41db2-426">Le paramètre methodName est le nom complet de la méthode au format `{domain}.{method}` .</span><span class="sxs-lookup"><span data-stu-id="41db2-426">The methodName parameter is the full name of the method in the format `{domain}.{method}`.</span></span> <span data-ttu-id="41db2-427">Le paramètre parametersAsJson est une chaîne au format JSON contenant les paramètres de la méthode correspondante.</span><span class="sxs-lookup"><span data-stu-id="41db2-427">The parametersAsJson parameter is a JSON formatted string containing the parameters for the corresponding method.</span></span> <span data-ttu-id="41db2-428">La méthode Invoke du gestionnaire est appelée lorsque la méthode est terminée de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="41db2-428">The handler's Invoke method will be called when the method asynchronously completes.</span></span> <span data-ttu-id="41db2-429">Invoke sera appelé avec l’objet de retour de la méthode sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="41db2-429">Invoke will be called with the method's return object as a JSON string.</span></span>

```cpp
// Prompt the user for the name and parameters of a CDP method, then call it.
void ScriptComponent::CallCdpMethod()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Call CDP Method",
        L"CDP method name:",
        L"Enter the CDP method name to call, followed by a space,\r\n"
            L"followed by the parameters in JSON format.",
        L"Runtime.evaluate {\"expression\":\"alert(\\\"test\\\")\"}");
    if (dialog.confirmed)
    {
        size_t delimiterPos = dialog.input.find(L' ');
        std::wstring methodName = dialog.input.substr(0, delimiterPos);
        std::wstring methodParams =
            (delimiterPos < dialog.input.size()
                ? dialog.input.substr(delimiterPos + 1)
                : L"{}");

        m_webView->CallDevToolsProtocolMethod(
            methodName.c_str(),
            methodParams.c_str(),
            Callback<ICoreWebView2CallDevToolsProtocolMethodCompletedHandler>(
                [](HRESULT error, PCWSTR resultJson) -> HRESULT
                {
                    MessageBox(nullptr, resultJson, L"CDP Method Result", MB_OK);
                    return S_OK;
                }).Get());
    }
}
```

#### <span data-ttu-id="41db2-430">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="41db2-430">CapturePreview</span></span> 

<span data-ttu-id="41db2-431">Capturez une image de l’affichage du WebView.</span><span class="sxs-lookup"><span data-stu-id="41db2-431">Capture an image of what WebView is displaying.</span></span>

> <span data-ttu-id="41db2-432">public HRESULT [CapturePreview](#capturepreview)([COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) ImageFormat, IStream \* ImageStream, gestionnaire [ICoreWebView2CapturePreviewCompletedHandler](icorewebview2capturepreviewcompletedhandler.md) \*)</span><span class="sxs-lookup"><span data-stu-id="41db2-432">public HRESULT [CapturePreview](#capturepreview)([COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) imageFormat, IStream \* imageStream, [ICoreWebView2CapturePreviewCompletedHandler](icorewebview2capturepreviewcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="41db2-433">Spécifiez le format de l’image avec le paramètre imageFormat.</span><span class="sxs-lookup"><span data-stu-id="41db2-433">Specify the format of the image with the imageFormat parameter.</span></span> <span data-ttu-id="41db2-434">Les données binaires d’image obtenues sont écrites dans le paramètre imageStream fourni.</span><span class="sxs-lookup"><span data-stu-id="41db2-434">The resulting image binary data is written to the provided imageStream parameter.</span></span> <span data-ttu-id="41db2-435">Lorsque CapturePreview finit d’écrire dans le flux, la méthode Invoke du paramètre de gestionnaire fourni est appelée.</span><span class="sxs-lookup"><span data-stu-id="41db2-435">When CapturePreview finishes writing to the stream, the Invoke method on the provided handler parameter is called.</span></span>

```cpp
// Show the user a file selection dialog, then save a screenshot of the WebView
// to the selected file.
void FileComponent::SaveScreenshot()
{
    OPENFILENAME openFileName = {};
    openFileName.lStructSize = sizeof(openFileName);
    openFileName.hwndOwner = nullptr;
    openFileName.hInstance = nullptr;
    WCHAR fileName[MAX_PATH] = L"WebView2_Screenshot.png";
    openFileName.lpstrFile = fileName;
    openFileName.lpstrFilter = L"PNG File\0*.png\0";
    openFileName.nMaxFile = ARRAYSIZE(fileName);
    openFileName.Flags = OFN_OVERWRITEPROMPT;

    if (GetSaveFileName(&openFileName))
    {
        wil::com_ptr<IStream> stream;
        CHECK_FAILURE(SHCreateStreamOnFileEx(
            fileName, STGM_READWRITE | STGM_CREATE, FILE_ATTRIBUTE_NORMAL, TRUE, nullptr,
            &stream));

        HWND mainWindow = m_appWindow->GetMainWindow();

        CHECK_FAILURE(m_webView->CapturePreview(
            COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG, stream.get(),
            Callback<ICoreWebView2CapturePreviewCompletedHandler>(
                [mainWindow](HRESULT error_code) -> HRESULT {
                    CHECK_FAILURE(error_code);

                    MessageBox(mainWindow, L"Preview Captured", L"Preview Captured", MB_OK);
                    return S_OK;
                })
                .Get()));
    }
}
```

#### <span data-ttu-id="41db2-436">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="41db2-436">ExecuteScript</span></span> 

<span data-ttu-id="41db2-437">Exécutez le code JavaScript du paramètre JavaScript du document de niveau supérieur actuel affiché dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="41db2-437">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="41db2-438">public HRESULT [ExecuteScript](#executescript)(LPCWSTR JavaScript, gestionnaire [ICoreWebView2ExecuteScriptCompletedHandler](icorewebview2executescriptcompletedhandler.md) \*)</span><span class="sxs-lookup"><span data-stu-id="41db2-438">public HRESULT [ExecuteScript](#executescript)(LPCWSTR javaScript, [ICoreWebView2ExecuteScriptCompletedHandler](icorewebview2executescriptcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="41db2-439">Cela s’exécute de manière asynchrone et, si un gestionnaire est fourni dans le paramètre ExecuteScriptCompletedHandler, sa méthode Invoke est appelée avec le résultat de l’évaluation du JavaScript fourni.</span><span class="sxs-lookup"><span data-stu-id="41db2-439">This will execute asynchronously and when complete, if a handler is provided in the ExecuteScriptCompletedHandler parameter, its Invoke method will be called with the result of evaluating the provided JavaScript.</span></span> <span data-ttu-id="41db2-440">La valeur de résultat est une chaîne codée au format JSON.</span><span class="sxs-lookup"><span data-stu-id="41db2-440">The result value is a JSON encoded string.</span></span> <span data-ttu-id="41db2-441">Si le résultat n’est pas défini, contient un cycle de référence ou ne peut pas être encodé dans JSON, la valeur null JSON sera renvoyée comme chaîne «NULL».</span><span class="sxs-lookup"><span data-stu-id="41db2-441">If the result is undefined, contains a reference cycle, or otherwise cannot be encoded into JSON, the JSON null value will be returned as the string 'null'.</span></span> <span data-ttu-id="41db2-442">Notez qu’une fonction qui ne contient aucune valeur de retour explicite renvoie une valeur non définie.</span><span class="sxs-lookup"><span data-stu-id="41db2-442">Note that a function that has no explicit return value returns undefined.</span></span> <span data-ttu-id="41db2-443">Si le script exécuté lève une exception non gérée, le résultat est également «null».</span><span class="sxs-lookup"><span data-stu-id="41db2-443">If the executed script throws an unhandled exception, then the result is also 'null'.</span></span> <span data-ttu-id="41db2-444">Cette méthode est appliquée de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="41db2-444">This method is applied asynchronously.</span></span> <span data-ttu-id="41db2-445">Si la méthode est appelée après l’événement NavigationStarting pendant une navigation, le script est exécuté dans le nouveau document lors du chargement de celui-ci, au cours du démarrage de ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="41db2-445">If the method is called after NavigationStarting event during a navigation, the script will be executed in the new document when loading it, around the time ContentLoading is fired.</span></span> <span data-ttu-id="41db2-446">ExecuteScript fonctionne même si ICoreWebView2Settings:: IsScriptEnabled est défini sur FALSe.</span><span class="sxs-lookup"><span data-stu-id="41db2-446">ExecuteScript will work even if ICoreWebView2Settings::IsScriptEnabled is set to FALSE.</span></span>

```cpp
// Prompt the user for some script and then execute it.
void ScriptComponent::InjectScript()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Inject Script",
        L"Enter script code:",
        L"Enter the JavaScript code to run in the webview.",
        L"window.getComputedStyle(document.body).backgroundColor");
    if (dialog.confirmed)
    {
        m_webView->ExecuteScript(dialog.input.c_str(),
            Callback<ICoreWebView2ExecuteScriptCompletedHandler>(
                [](HRESULT error, PCWSTR result) -> HRESULT
        {
            if (error != S_OK) {
                ShowFailure(error, L"ExecuteScript failed");
            }
            MessageBox(nullptr, result, L"ExecuteScript Result", MB_OK);
            return S_OK;
        }).Get());
    }
}
```

#### <span data-ttu-id="41db2-447">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="41db2-447">get_BrowserProcessId</span></span> 

<span data-ttu-id="41db2-448">ID de processus du processus de navigation qui héberge le WebView.</span><span class="sxs-lookup"><span data-stu-id="41db2-448">The process id of the browser process that hosts the WebView.</span></span>

> <span data-ttu-id="41db2-449">valeur publique HRESULT [get_BrowserProcessId](#get_browserprocessid)(valeur UInt32 \*)</span><span class="sxs-lookup"><span data-stu-id="41db2-449">public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* value)</span></span>

#### <span data-ttu-id="41db2-450">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="41db2-450">get_CanGoBack</span></span> 

<span data-ttu-id="41db2-451">Renvoie vrai si le WebView peut accéder à une page précédente de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="41db2-451">Returns true if the WebView can navigate to a previous page in the navigation history.</span></span>

> <span data-ttu-id="41db2-452">valeur publique HRESULT [get_CanGoBack](#get_cangoback)(bool \* CanGoBack)</span><span class="sxs-lookup"><span data-stu-id="41db2-452">public HRESULT [get_CanGoBack](#get_cangoback)(BOOL \* canGoBack)</span></span>

<span data-ttu-id="41db2-453">L’événement HistoryChanged se déclenche si CanGoBack change value.</span><span class="sxs-lookup"><span data-stu-id="41db2-453">The HistoryChanged event will fire if CanGoBack changes value.</span></span>

#### <span data-ttu-id="41db2-454">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="41db2-454">get_CanGoForward</span></span> 

<span data-ttu-id="41db2-455">Cette fonction renvoie la valeur vrai si le WebView peut accéder à une page suivante de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="41db2-455">Returns true if the WebView can navigate to a next page in the navigation history.</span></span>

> <span data-ttu-id="41db2-456">valeur publique HRESULT [get_CanGoForward](#get_cangoforward)(bool \* CanGoForward)</span><span class="sxs-lookup"><span data-stu-id="41db2-456">public HRESULT [get_CanGoForward](#get_cangoforward)(BOOL \* canGoForward)</span></span>

<span data-ttu-id="41db2-457">L’événement HistoryChanged se déclenche si CanGoForward change value.</span><span class="sxs-lookup"><span data-stu-id="41db2-457">The HistoryChanged event will fire if CanGoForward changes value.</span></span>

#### <span data-ttu-id="41db2-458">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="41db2-458">get_ContainsFullScreenElement</span></span> 

<span data-ttu-id="41db2-459">Indique si le WebView contient un élément HTML fullscreen.</span><span class="sxs-lookup"><span data-stu-id="41db2-459">Indicates if the WebView contains a fullscreen HTML element.</span></span>

> <span data-ttu-id="41db2-460">valeur publique HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(bool \* ContainsFullScreenElement)</span><span class="sxs-lookup"><span data-stu-id="41db2-460">public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(BOOL \* containsFullScreenElement)</span></span>

#### <span data-ttu-id="41db2-461">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="41db2-461">get_DocumentTitle</span></span> 

<span data-ttu-id="41db2-462">Titre du document de niveau supérieur actuel.</span><span class="sxs-lookup"><span data-stu-id="41db2-462">The title for the current top level document.</span></span>

> <span data-ttu-id="41db2-463">valeur publique HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span><span class="sxs-lookup"><span data-stu-id="41db2-463">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="41db2-464">Si le document ne comporte pas de titre explicite ou s’il est vide, une valeur par défaut qui peut ou ne correspond pas à l’URI du document sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="41db2-464">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

#### <span data-ttu-id="41db2-465">get_Settings</span><span class="sxs-lookup"><span data-stu-id="41db2-465">get_Settings</span></span> 

<span data-ttu-id="41db2-466">L’objet [ICoreWebView2Settings](icorewebview2settings.md) contient différents paramètres modifiables pour le WebView en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="41db2-466">The [ICoreWebView2Settings](icorewebview2settings.md) object contains various modifiable settings for the running WebView.</span></span>

> <span data-ttu-id="41db2-467">valeurs publiques HRESULT [get_Settings](#get_settings)([ICoreWebView2Settings](icorewebview2settings.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="41db2-467">public HRESULT [get_Settings](#get_settings)([ICoreWebView2Settings](icorewebview2settings.md) \*\* settings)</span></span>

#### <span data-ttu-id="41db2-468">get_Source</span><span class="sxs-lookup"><span data-stu-id="41db2-468">get_Source</span></span> 

<span data-ttu-id="41db2-469">URI du document de niveau supérieur actuel.</span><span class="sxs-lookup"><span data-stu-id="41db2-469">The URI of the current top level document.</span></span>

> <span data-ttu-id="41db2-470">valeur publique HRESULT [get_Source](#get_source)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="41db2-470">public HRESULT [get_Source](#get_source)(LPWSTR \* uri)</span></span>

<span data-ttu-id="41db2-471">Cette valeur peut éventuellement changer dans le cadre du déclenchement de l’événement SourceChanged dans certains cas, par exemple pour accéder à un site ou à un fragment de navigation différent.</span><span class="sxs-lookup"><span data-stu-id="41db2-471">This value potentially changes as a part of the SourceChanged event firing for some cases such as navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="41db2-472">Il restera identique pour les autres types de navigation, tels que les recharges de page ou l’historique. pushState avec la même URL que la page active.</span><span class="sxs-lookup"><span data-stu-id="41db2-472">It will remain the same for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span>

```cpp
    // Register a handler for the SourceChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_SourceChanged(
        Callback<ICoreWebView2SourceChangedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2SourceChangedEventArgs* args)
                -> HRESULT {
                wil::unique_cotaskmem_string uri;
                sender->get_Source(&uri);
                if (wcscmp(uri.get(), L"about:blank") == 0)
                {
                    uri = wil::make_cotaskmem_string(L"");
                }
                SetWindowText(GetAddressBar(), uri.get());

                return S_OK;
            })
            .Get(),
        &m_sourceChangedToken));
```

#### <span data-ttu-id="41db2-473">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="41db2-473">GetDevToolsProtocolEventReceiver</span></span> 

<span data-ttu-id="41db2-474">Obtenez un destinataire d’événement de protocole DevTools qui vous permet de vous abonner à un événement de protocole DevTools.</span><span class="sxs-lookup"><span data-stu-id="41db2-474">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>

> <span data-ttu-id="41db2-475">public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR NomÉvénement; [ICoreWebView2DevToolsProtocolEventReceiver](icorewebview2devtoolsprotocoleventreceiver.md) \* \* Receiver)</span><span class="sxs-lookup"><span data-stu-id="41db2-475">public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR eventName, [ICoreWebView2DevToolsProtocolEventReceiver](icorewebview2devtoolsprotocoleventreceiver.md) \*\* receiver)</span></span>

<span data-ttu-id="41db2-476">Le paramètre eventName est le nom complet de l’événement au format `{domain}.{event}` .</span><span class="sxs-lookup"><span data-stu-id="41db2-476">The eventName parameter is the full name of the event in the format `{domain}.{event}`.</span></span> <span data-ttu-id="41db2-477">Voir la [visionneuse de protocoles devtools](https://aka.ms/DevToolsProtocolDocs) pour obtenir une liste des événements de protocole devtools et des arguments d’événement.</span><span class="sxs-lookup"><span data-stu-id="41db2-477">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list of DevTools Protocol events description, and event args.</span></span>

```cpp
// Prompt the user to name a CDP event, and then subscribe to that event.
void ScriptComponent::SubscribeToCdpEvent()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Subscribe to CDP Event",
        L"CDP event name:",
        L"Enter the name of the CDP event to subscribe to.\r\n"
            L"You may also have to call the \"enable\" method of the\r\n"
            L"event's domain to receive events (for example \"Log.enable\").\r\n",
        L"Log.entryAdded");
    if (dialog.confirmed)
    {
        std::wstring eventName = dialog.input;
        wil::com_ptr<ICoreWebView2DevToolsProtocolEventReceiver> receiver;
        CHECK_FAILURE(
            m_webView->GetDevToolsProtocolEventReceiver(eventName.c_str(), &receiver));

        // If we are already subscribed to this event, unsubscribe first.
        auto preexistingToken = m_devToolsProtocolEventReceivedTokenMap.find(eventName);
        if (preexistingToken != m_devToolsProtocolEventReceivedTokenMap.end())
        {
            CHECK_FAILURE(receiver->remove_DevToolsProtocolEventReceived(
                preexistingToken->second));
        }

        CHECK_FAILURE(receiver->add_DevToolsProtocolEventReceived(
            Callback<ICoreWebView2DevToolsProtocolEventReceivedEventHandler>(
                [eventName](
                    ICoreWebView2* sender,
                    ICoreWebView2DevToolsProtocolEventReceivedEventArgs* args) -> HRESULT {
                    wil::unique_cotaskmem_string parameterObjectAsJson;
                    CHECK_FAILURE(args->get_ParameterObjectAsJson(&parameterObjectAsJson));
                    MessageBox(
                        nullptr, parameterObjectAsJson.get(),
                        (L"CDP Event Fired: " + eventName).c_str(), MB_OK);
                    return S_OK;
                })
                .Get(),
            &m_devToolsProtocolEventReceivedTokenMap[eventName]));
    }
}
```

#### <span data-ttu-id="41db2-478">GoBack</span><span class="sxs-lookup"><span data-stu-id="41db2-478">GoBack</span></span> 

<span data-ttu-id="41db2-479">Permet d’accéder à la page précédente de l’historique de navigation via le WebView.</span><span class="sxs-lookup"><span data-stu-id="41db2-479">Navigates the WebView to the previous page in the navigation history.</span></span>

> <span data-ttu-id="41db2-480">public HRESULT [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="41db2-480">public HRESULT [GoBack](#goback)()</span></span>

#### <span data-ttu-id="41db2-481">GoForward</span><span class="sxs-lookup"><span data-stu-id="41db2-481">GoForward</span></span> 

<span data-ttu-id="41db2-482">Navigue vers la page suivante de l’historique de navigation du WebView.</span><span class="sxs-lookup"><span data-stu-id="41db2-482">Navigates the WebView to the next page in the navigation history.</span></span>

> <span data-ttu-id="41db2-483">valeur publique HRESULT [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="41db2-483">public HRESULT [GoForward](#goforward)()</span></span>

#### <span data-ttu-id="41db2-484">Rechercher</span><span class="sxs-lookup"><span data-stu-id="41db2-484">Navigate</span></span> 

<span data-ttu-id="41db2-485">Entraîner une navigation du document de niveau supérieur sur l’URI spécifié.</span><span class="sxs-lookup"><span data-stu-id="41db2-485">Cause a navigation of the top level document to the specified URI.</span></span>

> <span data-ttu-id="41db2-486">public HRESULT [Navigate](#navigate)(Uri LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="41db2-486">public HRESULT [Navigate](#navigate)(LPCWSTR uri)</span></span>

<span data-ttu-id="41db2-487">Pour plus d’informations, voir événements de navigation.</span><span class="sxs-lookup"><span data-stu-id="41db2-487">See the navigation events for more information.</span></span> <span data-ttu-id="41db2-488">Notez que cela démarre une navigation et que l’événement NavigationStarting correspondant est déclenché après la fin de l’appel.</span><span class="sxs-lookup"><span data-stu-id="41db2-488">Note that this starts a navigation and the corresponding NavigationStarting event will fire sometime after this Navigate call completes.</span></span>

```cpp
void ControlComponent::NavigateToAddressBar()
{
    int length = GetWindowTextLength(GetAddressBar());
    std::wstring uri(length, 0);
    PWSTR buffer = const_cast<PWSTR>(uri.data());
    GetWindowText(GetAddressBar(), buffer, length + 1);

    HRESULT hr = m_webView->Navigate(uri.c_str());
    if (hr == E_INVALIDARG)
    {
        // An invalid URI was provided.
        if (uri.find(L' ') == std::wstring::npos
            && uri.find(L'.') != std::wstring::npos)
        {
            // If it contains a dot and no spaces, try tacking http:// on the front.
            hr = m_webView->Navigate((L"http://" + uri).c_str());
        }
        else
        {
            // Otherwise treat it as a web search. We aren't bothering to escape
            // URL syntax characters such as & and #
            hr = m_webView->Navigate((L"https://bing.com/search?q=" + uri).c_str());
        }
    }
    if (hr != E_INVALIDARG) {
        CHECK_FAILURE(hr);
    }
}
```

#### <span data-ttu-id="41db2-489">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="41db2-489">NavigateToString</span></span> 

<span data-ttu-id="41db2-490">Lance une navigation vers htmlContent en tant que code HTML source d’un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="41db2-490">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="41db2-491">public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span><span class="sxs-lookup"><span data-stu-id="41db2-491">public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span></span>

<span data-ttu-id="41db2-492">La taille du paramètre htmlContent n’est pas supérieure à 2 Mo.</span><span class="sxs-lookup"><span data-stu-id="41db2-492">The htmlContent parameter may not be larger than 2 MB in total size.</span></span> <span data-ttu-id="41db2-493">L’origine de la nouvelle page va être vide.</span><span class="sxs-lookup"><span data-stu-id="41db2-493">The origin of the new page will be about:blank.</span></span>

```cpp
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
```

#### <span data-ttu-id="41db2-494">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="41db2-494">OpenDevToolsWindow</span></span> 

<span data-ttu-id="41db2-495">Ouvre la fenêtre DevTools pour le document actif dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="41db2-495">Opens the DevTools window for the current document in the WebView.</span></span>

> <span data-ttu-id="41db2-496">public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span><span class="sxs-lookup"><span data-stu-id="41db2-496">public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span></span>

<span data-ttu-id="41db2-497">Ne peut pas être appelé lorsque la fenêtre DevTools est déjà ouverte.</span><span class="sxs-lookup"><span data-stu-id="41db2-497">Does nothing if called when the DevTools window is already open.</span></span>

#### <span data-ttu-id="41db2-498">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="41db2-498">PostWebMessageAsJson</span></span> 

<span data-ttu-id="41db2-499">Publier le WebMessage spécifié sur le document de niveau supérieur dans ce WebView.</span><span class="sxs-lookup"><span data-stu-id="41db2-499">Post the specified webMessage to the top level document in this WebView.</span></span>

> <span data-ttu-id="41db2-500">public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="41db2-500">public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span></span>

<span data-ttu-id="41db2-501">Le document de niveau supérieur de la fenêtre du document. chrome. WebView est déclenché.</span><span class="sxs-lookup"><span data-stu-id="41db2-501">The top level document's window.chrome.webview's message event fires.</span></span> <span data-ttu-id="41db2-502">JavaScript dans ce document est susceptible de s’abonner à l’événement et de s’en désabonner via la commande suivante:</span><span class="sxs-lookup"><span data-stu-id="41db2-502">JavaScript in that document may subscribe and unsubscribe to the event via the following:</span></span>

```
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

<span data-ttu-id="41db2-503">Les arguments d’événement sont une instance de `MessageEvent` .</span><span class="sxs-lookup"><span data-stu-id="41db2-503">The event args is an instance of `MessageEvent`.</span></span> <span data-ttu-id="41db2-504">Le paramètre ICoreWebView2Settings:: IsWebMessageEnabled doit avoir la valeur true, ou cette méthode échoue avec E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="41db2-504">The ICoreWebView2Settings::IsWebMessageEnabled setting must be true or this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="41db2-505">La propriété Data du arg est le paramètre de chaîne WebMessage électronique analysé comme chaîne JSON dans un objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="41db2-505">The event arg's data property is the webMessage string parameter parsed as a JSON string into a JavaScript object.</span></span> <span data-ttu-id="41db2-506">La propriété source de l’objet Event est une référence à l' `window.chrome.webview` objet.</span><span class="sxs-lookup"><span data-stu-id="41db2-506">The event arg's source property is a reference to the `window.chrome.webview` object.</span></span> <span data-ttu-id="41db2-507">Pour plus d’informations sur l’envoi de messages à partir du document HTML sur le WebView à l’hôte, voir add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="41db2-507">See add_WebMessageReceived for information on sending messages from the HTML document in the WebView to the host.</span></span> <span data-ttu-id="41db2-508">Ce message est envoyé de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="41db2-508">This message is sent asynchronously.</span></span> <span data-ttu-id="41db2-509">Si une navigation se produit avant que le message ne soit publié sur la page, le message ne sera pas envoyé.</span><span class="sxs-lookup"><span data-stu-id="41db2-509">If a navigation occurs before the message is posted to the page, then the message will not be sent.</span></span>

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<ICoreWebView2WebMessageReceivedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->TryGetWebMessageAsString(&messageRaw));
        std::wstring message = messageRaw.get();

        if (message.compare(0, 13, L"SetTitleText ") == 0)
        {
            m_appWindow->SetTitleText(message.substr(13).c_str());
        }
        else if (message.compare(L"GetWindowBounds") == 0)
        {
            RECT bounds = m_appWindow->GetWindowBounds();
            std::wstring reply =
                L"{\"WindowBounds\":\"Left:" + std::to_wstring(bounds.left)
                + L"\\nTop:" + std::to_wstring(bounds.top)
                + L"\\nRight:" + std::to_wstring(bounds.right)
                + L"\\nBottom:" + std::to_wstring(bounds.bottom)
                + L"\"}";
            CHECK_FAILURE(sender->PostWebMessageAsJson(reply.c_str()));
        }
        return S_OK;
    }).Get(), &m_webMessageReceivedToken));
```

#### <span data-ttu-id="41db2-510">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="41db2-510">PostWebMessageAsString</span></span> 

<span data-ttu-id="41db2-511">Il s’agit d’un programme d’assistance pour publier un message qui est une chaîne simple plutôt qu’une représentation de chaîne JSON d’un objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="41db2-511">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>

> <span data-ttu-id="41db2-512">public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="41db2-512">public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span></span>

<span data-ttu-id="41db2-513">Ce comportement se comporte exactement de la même façon que PostWebMessageAsJson, mais la `window.chrome.webview` propriété Data de arg du message est une chaîne ayant la même valeur que webMessageAsString.</span><span class="sxs-lookup"><span data-stu-id="41db2-513">This behaves in exactly the same manner as PostWebMessageAsJson but the `window.chrome.webview` message event arg's data property will be a string with the same value as webMessageAsString.</span></span> <span data-ttu-id="41db2-514">Utilisez cette fonction au lieu de PostWebMessageAsJson si vous souhaitez communiquer via des chaînes simples plutôt que des objets JSON.</span><span class="sxs-lookup"><span data-stu-id="41db2-514">Use this instead of PostWebMessageAsJson if you want to communicate via simple strings rather than JSON objects.</span></span>

#### <span data-ttu-id="41db2-515">Recharger</span><span class="sxs-lookup"><span data-stu-id="41db2-515">Reload</span></span> 

<span data-ttu-id="41db2-516">Recharger la page active.</span><span class="sxs-lookup"><span data-stu-id="41db2-516">Reload the current page.</span></span>

> <span data-ttu-id="41db2-517">[rechargement](#reload)du HRESULT public ()</span><span class="sxs-lookup"><span data-stu-id="41db2-517">public HRESULT [Reload](#reload)()</span></span>

<span data-ttu-id="41db2-518">Il s’agit de la même façon que d’accéder à l’URI du document de niveau supérieur actuel, y compris tous les événements de navigation déclenchant et respectant les entrées dans le cache HTTP.</span><span class="sxs-lookup"><span data-stu-id="41db2-518">This is similar to navigating to the URI of current top level document including all navigation events firing and respecting any entries in the HTTP cache.</span></span> <span data-ttu-id="41db2-519">Toutefois, l’historique en arrière-plan ne sera pas modifié.</span><span class="sxs-lookup"><span data-stu-id="41db2-519">But, the back/forward history will not be modified.</span></span>

#### <span data-ttu-id="41db2-520">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="41db2-520">remove_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="41db2-521">Supprimez un gestionnaire d’événements préalablement ajouté à add_ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="41db2-521">Remove an event handler previously added with add_ContainsFullScreenElementChanged.</span></span>

> <span data-ttu-id="41db2-522">[remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="41db2-522">public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="41db2-523">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="41db2-523">remove_ContentLoading</span></span> 

<span data-ttu-id="41db2-524">Supprimez un gestionnaire d’événements préalablement ajouté à add_ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="41db2-524">Remove an event handler previously added with add_ContentLoading.</span></span>

> <span data-ttu-id="41db2-525">[remove_ContentLoading](#remove_contentloading)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="41db2-525">public HRESULT [remove_ContentLoading](#remove_contentloading)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="41db2-526">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="41db2-526">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="41db2-527">Supprimez un gestionnaire d’événements préalablement ajouté à add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="41db2-527">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="41db2-528">[remove_DocumentTitleChanged](#remove_documenttitlechanged)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="41db2-528">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="41db2-529">remove_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="41db2-529">remove_FrameNavigationCompleted</span></span> 

<span data-ttu-id="41db2-530">Supprimez un gestionnaire d’événements préalablement ajouté à add_FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="41db2-530">Remove an event handler previously added with add_FrameNavigationCompleted.</span></span>

> <span data-ttu-id="41db2-531">[remove_FrameNavigationCompleted](#remove_framenavigationcompleted)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="41db2-531">public HRESULT [remove_FrameNavigationCompleted](#remove_framenavigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="41db2-532">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="41db2-532">remove_FrameNavigationStarting</span></span> 

<span data-ttu-id="41db2-533">Supprimez un gestionnaire d’événements préalablement ajouté à add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="41db2-533">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>

> <span data-ttu-id="41db2-534">[remove_FrameNavigationStarting](#remove_framenavigationstarting)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="41db2-534">public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="41db2-535">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="41db2-535">remove_HistoryChanged</span></span> 

<span data-ttu-id="41db2-536">Supprimez un gestionnaire d’événements préalablement ajouté à add_HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="41db2-536">Remove an event handler previously added with add_HistoryChanged.</span></span>

> <span data-ttu-id="41db2-537">[remove_HistoryChanged](#remove_historychanged)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="41db2-537">public HRESULT [remove_HistoryChanged](#remove_historychanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="41db2-538">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="41db2-538">remove_NavigationCompleted</span></span> 

<span data-ttu-id="41db2-539">Supprimez un gestionnaire d’événements préalablement ajouté à add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="41db2-539">Remove an event handler previously added with add_NavigationCompleted.</span></span>

> <span data-ttu-id="41db2-540">[remove_NavigationCompleted](#remove_navigationcompleted)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="41db2-540">public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="41db2-541">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="41db2-541">remove_NavigationStarting</span></span> 

<span data-ttu-id="41db2-542">Supprimez un gestionnaire d’événements préalablement ajouté à add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="41db2-542">Remove an event handler previously added with add_NavigationStarting.</span></span>

> <span data-ttu-id="41db2-543">[remove_NavigationStarting](#remove_navigationstarting)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="41db2-543">public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="41db2-544">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="41db2-544">remove_NewWindowRequested</span></span> 

<span data-ttu-id="41db2-545">Supprimez un gestionnaire d’événements préalablement ajouté à add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="41db2-545">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="41db2-546">[remove_NewWindowRequested](#remove_newwindowrequested)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="41db2-546">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="41db2-547">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="41db2-547">remove_PermissionRequested</span></span> 

<span data-ttu-id="41db2-548">Supprimez un gestionnaire d’événements préalablement ajouté à add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="41db2-548">Remove an event handler previously added with add_PermissionRequested.</span></span>

> <span data-ttu-id="41db2-549">[remove_PermissionRequested](#remove_permissionrequested)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="41db2-549">public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="41db2-550">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="41db2-550">remove_ProcessFailed</span></span> 

<span data-ttu-id="41db2-551">Supprimez un gestionnaire d’événements préalablement ajouté à add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="41db2-551">Remove an event handler previously added with add_ProcessFailed.</span></span>

> <span data-ttu-id="41db2-552">[remove_ProcessFailed](#remove_processfailed)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="41db2-552">public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="41db2-553">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="41db2-553">remove_ScriptDialogOpening</span></span> 

<span data-ttu-id="41db2-554">Supprimez un gestionnaire d’événements préalablement ajouté à add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="41db2-554">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>

> <span data-ttu-id="41db2-555">[remove_ScriptDialogOpening](#remove_scriptdialogopening)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="41db2-555">public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="41db2-556">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="41db2-556">remove_SourceChanged</span></span> 

<span data-ttu-id="41db2-557">Supprimez un gestionnaire d’événements préalablement ajouté à add_SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="41db2-557">Remove an event handler previously added with add_SourceChanged.</span></span>

> <span data-ttu-id="41db2-558">[remove_SourceChanged](#remove_sourcechanged)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="41db2-558">public HRESULT [remove_SourceChanged](#remove_sourcechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="41db2-559">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="41db2-559">remove_WebMessageReceived</span></span> 

<span data-ttu-id="41db2-560">Supprimez un gestionnaire d’événements préalablement ajouté à add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="41db2-560">Remove an event handler previously added with add_WebMessageReceived.</span></span>

> <span data-ttu-id="41db2-561">[remove_WebMessageReceived](#remove_webmessagereceived)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="41db2-561">public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="41db2-562">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="41db2-562">remove_WebResourceRequested</span></span> 

<span data-ttu-id="41db2-563">Supprimez un gestionnaire d’événements préalablement ajouté à add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="41db2-563">Remove an event handler previously added with add_WebResourceRequested.</span></span>

> <span data-ttu-id="41db2-564">[remove_WebResourceRequested](#remove_webresourcerequested)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="41db2-564">public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="41db2-565">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="41db2-565">remove_WindowCloseRequested</span></span> 

<span data-ttu-id="41db2-566">Supprimez un gestionnaire d’événements préalablement ajouté à add_WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="41db2-566">Remove an event handler previously added with add_WindowCloseRequested.</span></span>

> <span data-ttu-id="41db2-567">[remove_WindowCloseRequested](#remove_windowcloserequested)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="41db2-567">public HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="41db2-568">RemoveHostObjectFromScript</span><span class="sxs-lookup"><span data-stu-id="41db2-568">RemoveHostObjectFromScript</span></span> 

<span data-ttu-id="41db2-569">Supprimez l’objet hôte spécifié par le nom afin qu’il ne soit plus accessible à partir du code JavaScript du WebView.</span><span class="sxs-lookup"><span data-stu-id="41db2-569">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>

> <span data-ttu-id="41db2-570">public HRESULT [RemoveHostObjectFromScript](#removehostobjectfromscript)(nom LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="41db2-570">public HRESULT [RemoveHostObjectFromScript](#removehostobjectfromscript)(LPCWSTR name)</span></span>

<span data-ttu-id="41db2-571">Même si de nouvelles tentatives d’accès seront refusées, si l’objet est déjà obtenu par le code JavaScript du WebView, le code JavaScript continuera à avoir accès à cet objet.</span><span class="sxs-lookup"><span data-stu-id="41db2-571">While new access attempts will be denied, if the object is already obtained by JavaScript code in the WebView, the JavaScript code will continue to have access to that object.</span></span> <span data-ttu-id="41db2-572">Il n’est pas nécessaire d’appeler cette méthode pour un nom qui a déjà été supprimé ou n’ayant jamais été ajouté.</span><span class="sxs-lookup"><span data-stu-id="41db2-572">Calling this method for a name that is already removed or never added will fail.</span></span>

#### <span data-ttu-id="41db2-573">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="41db2-573">RemoveScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="41db2-574">Supprimez le JavaScript correspondant ajouté à l’aide `AddScriptToExecuteOnDocumentCreated` de l’ID de script spécifié.</span><span class="sxs-lookup"><span data-stu-id="41db2-574">Remove the corresponding JavaScript added using `AddScriptToExecuteOnDocumentCreated` with the specified script id.</span></span>

> <span data-ttu-id="41db2-575">public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(ID LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="41db2-575">public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR id)</span></span>

#### <span data-ttu-id="41db2-576">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="41db2-576">RemoveWebResourceRequestedFilter</span></span> 

<span data-ttu-id="41db2-577">Supprime un filtre de ressources correspondant précédemment ajouté pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="41db2-577">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

> <span data-ttu-id="41db2-578">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) constante resourceContext)</span><span class="sxs-lookup"><span data-stu-id="41db2-578">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="41db2-579">Si le même filtre a été ajouté plusieurs fois, il doit être supprimé autant de fois que ce dernier a été ajouté pour que la suppression soit effective.</span><span class="sxs-lookup"><span data-stu-id="41db2-579">If the same filter was added multiple times, then it will need to be removed as many times as it was added for the removal to be effective.</span></span> <span data-ttu-id="41db2-580">Renvoie E_INVALIDARG pour un filtre qui n’a jamais été ajouté.</span><span class="sxs-lookup"><span data-stu-id="41db2-580">Returns E_INVALIDARG for a filter that was never added.</span></span>

#### <span data-ttu-id="41db2-581">Stop</span><span class="sxs-lookup"><span data-stu-id="41db2-581">Stop</span></span> 

<span data-ttu-id="41db2-582">Arrêtez toutes les navigations et les extractions de ressources en attente.</span><span class="sxs-lookup"><span data-stu-id="41db2-582">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="41db2-583">point d' [arrêt](#stop)public HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="41db2-583">public HRESULT [Stop](#stop)()</span></span>

<span data-ttu-id="41db2-584">Ne permet pas d’arrêter les scripts.</span><span class="sxs-lookup"><span data-stu-id="41db2-584">Does not stop scripts.</span></span>

#### <span data-ttu-id="41db2-585">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="41db2-585">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span> 

<span data-ttu-id="41db2-586">Format d’image utilisé par la méthode ICoreWebView2:: CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="41db2-586">Image format used by the ICoreWebView2::CapturePreview method.</span></span>

> <span data-ttu-id="41db2-587">énumération [COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format)</span><span class="sxs-lookup"><span data-stu-id="41db2-587">enum [COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format)</span></span>

 <span data-ttu-id="41db2-588">Doubl</span><span class="sxs-lookup"><span data-stu-id="41db2-588">Values</span></span>                         | <span data-ttu-id="41db2-589">Descriptions</span><span class="sxs-lookup"><span data-stu-id="41db2-589">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="41db2-590">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span><span class="sxs-lookup"><span data-stu-id="41db2-590">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span></span>            | <span data-ttu-id="41db2-591">Format d’image PNG.</span><span class="sxs-lookup"><span data-stu-id="41db2-591">PNG image format.</span></span>
<span data-ttu-id="41db2-592">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span><span class="sxs-lookup"><span data-stu-id="41db2-592">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span></span>            | <span data-ttu-id="41db2-593">Format d’image JPEG.</span><span class="sxs-lookup"><span data-stu-id="41db2-593">JPEG image format.</span></span>

#### <span data-ttu-id="41db2-594">COREWEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="41db2-594">COREWEBVIEW2_KEY_EVENT_KIND</span></span> 

<span data-ttu-id="41db2-595">Type d’événement de touche qui déclenchait un événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="41db2-595">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="41db2-596">énumération [COREWEBVIEW2_KEY_EVENT_KIND](#corewebview2_key_event_kind)</span><span class="sxs-lookup"><span data-stu-id="41db2-596">enum [COREWEBVIEW2_KEY_EVENT_KIND](#corewebview2_key_event_kind)</span></span>

 <span data-ttu-id="41db2-597">Doubl</span><span class="sxs-lookup"><span data-stu-id="41db2-597">Values</span></span>                         | <span data-ttu-id="41db2-598">Descriptions</span><span class="sxs-lookup"><span data-stu-id="41db2-598">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="41db2-599">COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="41db2-599">COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span></span>            | <span data-ttu-id="41db2-600">Correspond à WM_KEYDOWN de messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="41db2-600">Correspond to window message WM_KEYDOWN.</span></span>
<span data-ttu-id="41db2-601">COREWEBVIEW2_KEY_EVENT_KIND_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="41db2-601">COREWEBVIEW2_KEY_EVENT_KIND_KEY_UP</span></span>            | <span data-ttu-id="41db2-602">Correspond à WM_KEYUP de messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="41db2-602">Correspond to window message WM_KEYUP.</span></span>
<span data-ttu-id="41db2-603">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="41db2-603">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span></span>            | <span data-ttu-id="41db2-604">Correspond à WM_SYSKEYDOWN de messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="41db2-604">Correspond to window message WM_SYSKEYDOWN.</span></span>
<span data-ttu-id="41db2-605">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="41db2-605">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span></span>            | <span data-ttu-id="41db2-606">Correspond à WM_SYSKEYUP de messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="41db2-606">Correspond to window message WM_SYSKEYUP.</span></span>

#### <span data-ttu-id="41db2-607">COREWEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="41db2-607">COREWEBVIEW2_MOVE_FOCUS_REASON</span></span> 

<span data-ttu-id="41db2-608">Raison du déplacement du focus.</span><span class="sxs-lookup"><span data-stu-id="41db2-608">Reason for moving focus.</span></span>

> <span data-ttu-id="41db2-609">énumération [COREWEBVIEW2_MOVE_FOCUS_REASON](#corewebview2_move_focus_reason)</span><span class="sxs-lookup"><span data-stu-id="41db2-609">enum [COREWEBVIEW2_MOVE_FOCUS_REASON](#corewebview2_move_focus_reason)</span></span>

 <span data-ttu-id="41db2-610">Doubl</span><span class="sxs-lookup"><span data-stu-id="41db2-610">Values</span></span>                         | <span data-ttu-id="41db2-611">Descriptions</span><span class="sxs-lookup"><span data-stu-id="41db2-611">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="41db2-612">COREWEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span><span class="sxs-lookup"><span data-stu-id="41db2-612">COREWEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span></span>            | <span data-ttu-id="41db2-613">Paramètre de code axé sur le WebView.</span><span class="sxs-lookup"><span data-stu-id="41db2-613">Code setting focus into WebView.</span></span>
<span data-ttu-id="41db2-614">COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT</span><span class="sxs-lookup"><span data-stu-id="41db2-614">COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT</span></span>            | <span data-ttu-id="41db2-615">Déplacement du focus en raison d’une touche Tab.</span><span class="sxs-lookup"><span data-stu-id="41db2-615">Moving focus due to Tab traversal forward.</span></span>
<span data-ttu-id="41db2-616">COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span><span class="sxs-lookup"><span data-stu-id="41db2-616">COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span></span>            | <span data-ttu-id="41db2-617">Déplacement du focus en partant du haut de l’onglet.</span><span class="sxs-lookup"><span data-stu-id="41db2-617">Moving focus due to Tab traversal backward.</span></span>

#### <span data-ttu-id="41db2-618">COREWEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="41db2-618">COREWEBVIEW2_PERMISSION_KIND</span></span> 

<span data-ttu-id="41db2-619">Le type d’une demande d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="41db2-619">The type of a permission request.</span></span>

> <span data-ttu-id="41db2-620">énumération [COREWEBVIEW2_PERMISSION_KIND](#corewebview2_permission_kind)</span><span class="sxs-lookup"><span data-stu-id="41db2-620">enum [COREWEBVIEW2_PERMISSION_KIND](#corewebview2_permission_kind)</span></span>

 <span data-ttu-id="41db2-621">Doubl</span><span class="sxs-lookup"><span data-stu-id="41db2-621">Values</span></span>                         | <span data-ttu-id="41db2-622">Descriptions</span><span class="sxs-lookup"><span data-stu-id="41db2-622">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="41db2-623">COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="41db2-623">COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span></span>            | <span data-ttu-id="41db2-624">Autorisation inconnue.</span><span class="sxs-lookup"><span data-stu-id="41db2-624">Unknown permission.</span></span>
<span data-ttu-id="41db2-625">COREWEBVIEW2_PERMISSION_KIND_MICROPHONE</span><span class="sxs-lookup"><span data-stu-id="41db2-625">COREWEBVIEW2_PERMISSION_KIND_MICROPHONE</span></span>            | <span data-ttu-id="41db2-626">Autorisation de capture audio.</span><span class="sxs-lookup"><span data-stu-id="41db2-626">Permission to capture audio.</span></span>
<span data-ttu-id="41db2-627">COREWEBVIEW2_PERMISSION_KIND_CAMERA</span><span class="sxs-lookup"><span data-stu-id="41db2-627">COREWEBVIEW2_PERMISSION_KIND_CAMERA</span></span>            | <span data-ttu-id="41db2-628">Autorisation de capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="41db2-628">Permission to capture video.</span></span>
<span data-ttu-id="41db2-629">COREWEBVIEW2_PERMISSION_KIND_GEOLOCATION</span><span class="sxs-lookup"><span data-stu-id="41db2-629">COREWEBVIEW2_PERMISSION_KIND_GEOLOCATION</span></span>            | <span data-ttu-id="41db2-630">Autorisation d’accès à la géolocalisation.</span><span class="sxs-lookup"><span data-stu-id="41db2-630">Permission to access geolocation.</span></span>
<span data-ttu-id="41db2-631">COREWEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="41db2-631">COREWEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span></span>            | <span data-ttu-id="41db2-632">Autorisation d’envoyer des notifications Web.</span><span class="sxs-lookup"><span data-stu-id="41db2-632">Permission to send web notifications.</span></span>
<span data-ttu-id="41db2-633">COREWEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span><span class="sxs-lookup"><span data-stu-id="41db2-633">COREWEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span></span>            | <span data-ttu-id="41db2-634">Autorisation d’accès au capteur générique.</span><span class="sxs-lookup"><span data-stu-id="41db2-634">Permission to access generic sensor.</span></span>
<span data-ttu-id="41db2-635">COREWEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span><span class="sxs-lookup"><span data-stu-id="41db2-635">COREWEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span></span>            | <span data-ttu-id="41db2-636">Autorisation de lecture du presse-papiers système sans mouvement utilisateur.</span><span class="sxs-lookup"><span data-stu-id="41db2-636">Permission to read system clipboard without a user gesture.</span></span>

#### <span data-ttu-id="41db2-637">COREWEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="41db2-637">COREWEBVIEW2_PERMISSION_STATE</span></span> 

<span data-ttu-id="41db2-638">Réponse à une demande d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="41db2-638">Response to a permission request.</span></span>

> <span data-ttu-id="41db2-639">énumération [COREWEBVIEW2_PERMISSION_STATE](#corewebview2_permission_state)</span><span class="sxs-lookup"><span data-stu-id="41db2-639">enum [COREWEBVIEW2_PERMISSION_STATE](#corewebview2_permission_state)</span></span>

 <span data-ttu-id="41db2-640">Doubl</span><span class="sxs-lookup"><span data-stu-id="41db2-640">Values</span></span>                         | <span data-ttu-id="41db2-641">Descriptions</span><span class="sxs-lookup"><span data-stu-id="41db2-641">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="41db2-642">COREWEBVIEW2_PERMISSION_STATE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="41db2-642">COREWEBVIEW2_PERMISSION_STATE_DEFAULT</span></span>            | <span data-ttu-id="41db2-643">Utilisez le comportement par défaut du navigateur, qui invite en principe les utilisateurs à la décision.</span><span class="sxs-lookup"><span data-stu-id="41db2-643">Use default browser behavior, which normally prompt users for decision.</span></span>
<span data-ttu-id="41db2-644">COREWEBVIEW2_PERMISSION_STATE_ALLOW</span><span class="sxs-lookup"><span data-stu-id="41db2-644">COREWEBVIEW2_PERMISSION_STATE_ALLOW</span></span>            | <span data-ttu-id="41db2-645">Accordez la demande d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="41db2-645">Grant the permission request.</span></span>
<span data-ttu-id="41db2-646">COREWEBVIEW2_PERMISSION_STATE_DENY</span><span class="sxs-lookup"><span data-stu-id="41db2-646">COREWEBVIEW2_PERMISSION_STATE_DENY</span></span>            | <span data-ttu-id="41db2-647">Refusez la demande d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="41db2-647">Deny the permission request.</span></span>

#### <span data-ttu-id="41db2-648">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="41db2-648">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span></span> 

<span data-ttu-id="41db2-649">Structure représentant les informations contenues dans le LPARAM fourni à un événement de touche Win32.</span><span class="sxs-lookup"><span data-stu-id="41db2-649">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

> <span data-ttu-id="41db2-650">[COREWEBVIEW2_PHYSICAL_KEY_STATUS](#corewebview2_physical_key_status) typedef</span><span class="sxs-lookup"><span data-stu-id="41db2-650">typedef [COREWEBVIEW2_PHYSICAL_KEY_STATUS](#corewebview2_physical_key_status)</span></span>

<span data-ttu-id="41db2-651">Pour plus d’informations, consultez la documentation de WM_KEYDOWN [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span><span class="sxs-lookup"><span data-stu-id="41db2-651">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span></span>

#### <span data-ttu-id="41db2-652">COREWEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="41db2-652">COREWEBVIEW2_PROCESS_FAILED_KIND</span></span> 

<span data-ttu-id="41db2-653">Type d’échec de processus utilisé dans l’interface ICoreWebView2ProcessFailedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="41db2-653">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>

> <span data-ttu-id="41db2-654">énumération [COREWEBVIEW2_PROCESS_FAILED_KIND](#corewebview2_process_failed_kind)</span><span class="sxs-lookup"><span data-stu-id="41db2-654">enum [COREWEBVIEW2_PROCESS_FAILED_KIND](#corewebview2_process_failed_kind)</span></span>

 <span data-ttu-id="41db2-655">Doubl</span><span class="sxs-lookup"><span data-stu-id="41db2-655">Values</span></span>                         | <span data-ttu-id="41db2-656">Descriptions</span><span class="sxs-lookup"><span data-stu-id="41db2-656">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="41db2-657">COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="41db2-657">COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span></span>            | <span data-ttu-id="41db2-658">Indique que le processus du navigateur s’est arrêté de manière inattendue.</span><span class="sxs-lookup"><span data-stu-id="41db2-658">Indicates the browser process terminated unexpectedly.</span></span>
<span data-ttu-id="41db2-659">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="41db2-659">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span></span>            | <span data-ttu-id="41db2-660">Indique le processus de rendu arrêté de manière inattendue.</span><span class="sxs-lookup"><span data-stu-id="41db2-660">Indicates the render process terminated unexpectedly.</span></span>
<span data-ttu-id="41db2-661">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span><span class="sxs-lookup"><span data-stu-id="41db2-661">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span></span>            | <span data-ttu-id="41db2-662">Indique que le processus de rendu ne répond pas.</span><span class="sxs-lookup"><span data-stu-id="41db2-662">Indicates the render process becomes unresponsive.</span></span>

#### <span data-ttu-id="41db2-663">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="41db2-663">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span></span> 

<span data-ttu-id="41db2-664">Type de boîte de dialogue JavaScript utilisée dans l’interface ICoreWebView2ScriptDialogOpeningEventHandler.</span><span class="sxs-lookup"><span data-stu-id="41db2-664">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>

> <span data-ttu-id="41db2-665">énumération [COREWEBVIEW2_SCRIPT_DIALOG_KIND](#corewebview2_script_dialog_kind)</span><span class="sxs-lookup"><span data-stu-id="41db2-665">enum [COREWEBVIEW2_SCRIPT_DIALOG_KIND](#corewebview2_script_dialog_kind)</span></span>

 <span data-ttu-id="41db2-666">Doubl</span><span class="sxs-lookup"><span data-stu-id="41db2-666">Values</span></span>                         | <span data-ttu-id="41db2-667">Descriptions</span><span class="sxs-lookup"><span data-stu-id="41db2-667">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="41db2-668">COREWEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span><span class="sxs-lookup"><span data-stu-id="41db2-668">COREWEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span></span>            | <span data-ttu-id="41db2-669">Une boîte de dialogue appelée par le biais de la fonction JavaScript window. Alert.</span><span class="sxs-lookup"><span data-stu-id="41db2-669">A dialog invoked via the window.alert JavaScript function.</span></span>
<span data-ttu-id="41db2-670">COREWEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span><span class="sxs-lookup"><span data-stu-id="41db2-670">COREWEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span></span>            | <span data-ttu-id="41db2-671">Une boîte de dialogue appelée via la fonction de fenêtre. confirmer JavaScript.</span><span class="sxs-lookup"><span data-stu-id="41db2-671">A dialog invoked via the window.confirm JavaScript function.</span></span>
<span data-ttu-id="41db2-672">COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span><span class="sxs-lookup"><span data-stu-id="41db2-672">COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span></span>            | <span data-ttu-id="41db2-673">Une boîte de dialogue appelée via la fonction JavaScript window. prompt.</span><span class="sxs-lookup"><span data-stu-id="41db2-673">A dialog invoked via the window.prompt JavaScript function.</span></span>
<span data-ttu-id="41db2-674">COREWEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span><span class="sxs-lookup"><span data-stu-id="41db2-674">COREWEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span></span>            | <span data-ttu-id="41db2-675">Une boîte de dialogue appelée via l’événement JavaScript beforeunload.</span><span class="sxs-lookup"><span data-stu-id="41db2-675">A dialog invoked via the beforeunload JavaScript event.</span></span>

#### <span data-ttu-id="41db2-676">COREWEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="41db2-676">COREWEBVIEW2_WEB_ERROR_STATUS</span></span> 

<span data-ttu-id="41db2-677">Valeurs d’état d’erreur pour les navigations Web.</span><span class="sxs-lookup"><span data-stu-id="41db2-677">Error status values for web navigations.</span></span>

> <span data-ttu-id="41db2-678">énumération [COREWEBVIEW2_WEB_ERROR_STATUS](#corewebview2_web_error_status)</span><span class="sxs-lookup"><span data-stu-id="41db2-678">enum [COREWEBVIEW2_WEB_ERROR_STATUS](#corewebview2_web_error_status)</span></span>

 <span data-ttu-id="41db2-679">Doubl</span><span class="sxs-lookup"><span data-stu-id="41db2-679">Values</span></span>                         | <span data-ttu-id="41db2-680">Descriptions</span><span class="sxs-lookup"><span data-stu-id="41db2-680">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="41db2-681">COREWEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="41db2-681">COREWEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span></span>            | <span data-ttu-id="41db2-682">Une erreur inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="41db2-682">An unknown error occurred.</span></span>
<span data-ttu-id="41db2-683">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span><span class="sxs-lookup"><span data-stu-id="41db2-683">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span></span>            | <span data-ttu-id="41db2-684">Le nom usuel du certificat SSL ne correspond pas à l’adresse Web.</span><span class="sxs-lookup"><span data-stu-id="41db2-684">The SSL certificate common name does not match the web address.</span></span>
<span data-ttu-id="41db2-685">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span><span class="sxs-lookup"><span data-stu-id="41db2-685">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span></span>            | <span data-ttu-id="41db2-686">Le certificat SSL a expiré.</span><span class="sxs-lookup"><span data-stu-id="41db2-686">The SSL certificate has expired.</span></span>
<span data-ttu-id="41db2-687">COREWEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span><span class="sxs-lookup"><span data-stu-id="41db2-687">COREWEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span></span>            | <span data-ttu-id="41db2-688">Le certificat client SSL comporte des erreurs.</span><span class="sxs-lookup"><span data-stu-id="41db2-688">The SSL client certificate contains errors.</span></span>
<span data-ttu-id="41db2-689">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span><span class="sxs-lookup"><span data-stu-id="41db2-689">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span></span>            | <span data-ttu-id="41db2-690">Le certificat SSL a été révoqué.</span><span class="sxs-lookup"><span data-stu-id="41db2-690">The SSL certificate has been revoked.</span></span>
<span data-ttu-id="41db2-691">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span><span class="sxs-lookup"><span data-stu-id="41db2-691">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span></span>            | <span data-ttu-id="41db2-692">Le certificat SSL n’est pas valide &ndash; cela peut signifier que le certificat ne correspond pas aux codes confidentiels de clé publique du nom d’hôte. le certificat est signé par une autorité non approuvée ou à l’aide d’un algorithme de signature faible, le certificat ayant revendiqué des noms DNS enfreignant les contraintes de nom, le certificat contient une clé faible, la période de validité du certificat est trop longue, l’absence de données de révocation ou du mécanisme de révocation, le [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html)nom d’hôte non unique, l’absence de données de transparence de</span><span class="sxs-lookup"><span data-stu-id="41db2-692">The SSL certificate is invalid &ndash; this could mean the certificate did not match the public key pins for the host name, the certificate is signed by an untrusted authority or using a weak sign algorithm, the certificate claimed DNS names violate name constraints, the certificate contains a weak key, the certificate's validity period is too long, lack of revocation information or revocation mechanism, non-unique host name, lack of certificate transparency information, or the certificate is chained to a [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).</span></span>
<span data-ttu-id="41db2-693">COREWEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="41db2-693">COREWEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span></span>            | <span data-ttu-id="41db2-694">L’hôte n’est pas joignable.</span><span class="sxs-lookup"><span data-stu-id="41db2-694">The host is unreachable.</span></span>
<span data-ttu-id="41db2-695">COREWEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="41db2-695">COREWEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span></span>            | <span data-ttu-id="41db2-696">La connexion a expiré.</span><span class="sxs-lookup"><span data-stu-id="41db2-696">The connection has timed out.</span></span>
<span data-ttu-id="41db2-697">COREWEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span><span class="sxs-lookup"><span data-stu-id="41db2-697">COREWEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span></span>            | <span data-ttu-id="41db2-698">Le serveur a renvoyé une réponse non valide ou non reconnue.</span><span class="sxs-lookup"><span data-stu-id="41db2-698">The server returned an invalid or unrecognized response.</span></span>
<span data-ttu-id="41db2-699">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span><span class="sxs-lookup"><span data-stu-id="41db2-699">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span></span>            | <span data-ttu-id="41db2-700">La connexion a été annulée.</span><span class="sxs-lookup"><span data-stu-id="41db2-700">The connection was aborted.</span></span>
<span data-ttu-id="41db2-701">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span><span class="sxs-lookup"><span data-stu-id="41db2-701">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span></span>            | <span data-ttu-id="41db2-702">La connexion a été réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="41db2-702">The connection was reset.</span></span>
<span data-ttu-id="41db2-703">COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span><span class="sxs-lookup"><span data-stu-id="41db2-703">COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span></span>            | <span data-ttu-id="41db2-704">La connexion Internet a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="41db2-704">The Internet connection has been lost.</span></span>
<span data-ttu-id="41db2-705">COREWEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span><span class="sxs-lookup"><span data-stu-id="41db2-705">COREWEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span></span>            | <span data-ttu-id="41db2-706">Connexion impossible à la destination.</span><span class="sxs-lookup"><span data-stu-id="41db2-706">Cannot connect to destination.</span></span>
<span data-ttu-id="41db2-707">COREWEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="41db2-707">COREWEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span></span>            | <span data-ttu-id="41db2-708">Impossible de résoudre le nom d’hôte fourni.</span><span class="sxs-lookup"><span data-stu-id="41db2-708">Could not resolve provided host name.</span></span>
<span data-ttu-id="41db2-709">COREWEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span><span class="sxs-lookup"><span data-stu-id="41db2-709">COREWEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span></span>            | <span data-ttu-id="41db2-710">L’opération a été annulée.</span><span class="sxs-lookup"><span data-stu-id="41db2-710">The operation was canceled.</span></span>
<span data-ttu-id="41db2-711">COREWEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span><span class="sxs-lookup"><span data-stu-id="41db2-711">COREWEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span></span>            | <span data-ttu-id="41db2-712">Échec de la redirection de la requête.</span><span class="sxs-lookup"><span data-stu-id="41db2-712">The request redirect failed.</span></span>
<span data-ttu-id="41db2-713">COREWEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span><span class="sxs-lookup"><span data-stu-id="41db2-713">COREWEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span></span>            | <span data-ttu-id="41db2-714">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="41db2-714">An unexpected error occurred.</span></span>

#### <span data-ttu-id="41db2-715">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="41db2-715">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span></span> 

<span data-ttu-id="41db2-716">Énum pour les contextes de demande de ressources Web.</span><span class="sxs-lookup"><span data-stu-id="41db2-716">Enum for web resource request contexts.</span></span>

> <span data-ttu-id="41db2-717">énumération [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context)</span><span class="sxs-lookup"><span data-stu-id="41db2-717">enum [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context)</span></span>

 <span data-ttu-id="41db2-718">Doubl</span><span class="sxs-lookup"><span data-stu-id="41db2-718">Values</span></span>                         | <span data-ttu-id="41db2-719">Descriptions</span><span class="sxs-lookup"><span data-stu-id="41db2-719">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="41db2-720">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span><span class="sxs-lookup"><span data-stu-id="41db2-720">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span></span>            | <span data-ttu-id="41db2-721">Toutes les ressources.</span><span class="sxs-lookup"><span data-stu-id="41db2-721">All resources.</span></span>
<span data-ttu-id="41db2-722">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="41db2-722">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span></span>            | <span data-ttu-id="41db2-723">Ressources de documents.</span><span class="sxs-lookup"><span data-stu-id="41db2-723">Document resources.</span></span>
<span data-ttu-id="41db2-724">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span><span class="sxs-lookup"><span data-stu-id="41db2-724">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span></span>            | <span data-ttu-id="41db2-725">Des ressources CSS;</span><span class="sxs-lookup"><span data-stu-id="41db2-725">CSS resources.</span></span>
<span data-ttu-id="41db2-726">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span><span class="sxs-lookup"><span data-stu-id="41db2-726">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span></span>            | <span data-ttu-id="41db2-727">Ressources d’image.</span><span class="sxs-lookup"><span data-stu-id="41db2-727">Image resources.</span></span>
<span data-ttu-id="41db2-728">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span><span class="sxs-lookup"><span data-stu-id="41db2-728">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span></span>            | <span data-ttu-id="41db2-729">Autres ressources multimédias telles que les vidéos.</span><span class="sxs-lookup"><span data-stu-id="41db2-729">Other media resources such as videos.</span></span>
<span data-ttu-id="41db2-730">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span><span class="sxs-lookup"><span data-stu-id="41db2-730">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span></span>            | <span data-ttu-id="41db2-731">Ressources de police.</span><span class="sxs-lookup"><span data-stu-id="41db2-731">Font resources.</span></span>
<span data-ttu-id="41db2-732">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="41db2-732">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span></span>            | <span data-ttu-id="41db2-733">Ressources de script.</span><span class="sxs-lookup"><span data-stu-id="41db2-733">Script resources.</span></span>
<span data-ttu-id="41db2-734">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="41db2-734">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span></span>            | <span data-ttu-id="41db2-735">Requêtes HTTP XML.</span><span class="sxs-lookup"><span data-stu-id="41db2-735">XML HTTP requests.</span></span>
<span data-ttu-id="41db2-736">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span><span class="sxs-lookup"><span data-stu-id="41db2-736">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span></span>            | <span data-ttu-id="41db2-737">Extraire la communication de l’API.</span><span class="sxs-lookup"><span data-stu-id="41db2-737">Fetch API communication.</span></span>
<span data-ttu-id="41db2-738">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span><span class="sxs-lookup"><span data-stu-id="41db2-738">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span></span>            | <span data-ttu-id="41db2-739">Ressources TextTrack.</span><span class="sxs-lookup"><span data-stu-id="41db2-739">TextTrack resources.</span></span>
<span data-ttu-id="41db2-740">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span><span class="sxs-lookup"><span data-stu-id="41db2-740">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span></span>            | <span data-ttu-id="41db2-741">Communication API EventSource.</span><span class="sxs-lookup"><span data-stu-id="41db2-741">EventSource API communication.</span></span>
<span data-ttu-id="41db2-742">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span><span class="sxs-lookup"><span data-stu-id="41db2-742">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span></span>            | <span data-ttu-id="41db2-743">Communication de l’API WebSocket.</span><span class="sxs-lookup"><span data-stu-id="41db2-743">WebSocket API communication.</span></span>
<span data-ttu-id="41db2-744">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span><span class="sxs-lookup"><span data-stu-id="41db2-744">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span></span>            | <span data-ttu-id="41db2-745">Manifestes de l’application Web.</span><span class="sxs-lookup"><span data-stu-id="41db2-745">Web App Manifests.</span></span>
<span data-ttu-id="41db2-746">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span><span class="sxs-lookup"><span data-stu-id="41db2-746">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span></span>            | <span data-ttu-id="41db2-747">Échange HTTP signé.</span><span class="sxs-lookup"><span data-stu-id="41db2-747">Signed HTTP Exchanges.</span></span>
<span data-ttu-id="41db2-748">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span><span class="sxs-lookup"><span data-stu-id="41db2-748">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span></span>            | <span data-ttu-id="41db2-749">Demandes ping.</span><span class="sxs-lookup"><span data-stu-id="41db2-749">Ping requests.</span></span>
<span data-ttu-id="41db2-750">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span><span class="sxs-lookup"><span data-stu-id="41db2-750">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span></span>            | <span data-ttu-id="41db2-751">Rapports de violation des CSP.</span><span class="sxs-lookup"><span data-stu-id="41db2-751">CSP Violation Reports.</span></span>
<span data-ttu-id="41db2-752">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span><span class="sxs-lookup"><span data-stu-id="41db2-752">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span></span>            | <span data-ttu-id="41db2-753">Autres ressources.</span><span class="sxs-lookup"><span data-stu-id="41db2-753">Other resources.</span></span>

