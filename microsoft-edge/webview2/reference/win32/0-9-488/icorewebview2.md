---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: b40cd7558697228f4b968d5efa44b4c359af36c1
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653388"
---
# <span data-ttu-id="92122-104">interface ICoreWebView2</span><span class="sxs-lookup"><span data-stu-id="92122-104">interface ICoreWebView2</span></span> 

```
interface ICoreWebView2
  : public IUnknown
```

<span data-ttu-id="92122-105">WebView2 vous permet d’héberger le contenu Web à l’aide de la technologie de navigateur Web la plus récente.</span><span class="sxs-lookup"><span data-stu-id="92122-105">WebView2 enables you to host web content using the latest Edge web browser technology.</span></span>

## <span data-ttu-id="92122-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="92122-106">Summary</span></span>

 <span data-ttu-id="92122-107">Ses</span><span class="sxs-lookup"><span data-stu-id="92122-107">Members</span></span>                        | <span data-ttu-id="92122-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="92122-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="92122-109">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="92122-109">add_ContainsFullScreenElementChanged</span></span>](#add_containsfullscreenelementchanged) | <span data-ttu-id="92122-110">Avertit en cas de modification de la propriété ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="92122-110">Notifies when the ContainsFullScreenElement property changes.</span></span>
[<span data-ttu-id="92122-111">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="92122-111">add_ContentLoading</span></span>](#add_contentloading) | <span data-ttu-id="92122-112">Ajoutez un gestionnaire d’événements pour l’événement ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="92122-112">Add an event handler for the ContentLoading event.</span></span>
[<span data-ttu-id="92122-113">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="92122-113">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="92122-114">Ajoutez un gestionnaire d’événements pour l’événement DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="92122-114">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="92122-115">add_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="92122-115">add_FrameNavigationCompleted</span></span>](#add_framenavigationcompleted) | <span data-ttu-id="92122-116">Ajoutez un gestionnaire d’événements pour l’événement FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="92122-116">Add an event handler for the FrameNavigationCompleted event.</span></span>
[<span data-ttu-id="92122-117">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="92122-117">add_FrameNavigationStarting</span></span>](#add_framenavigationstarting) | <span data-ttu-id="92122-118">Ajoutez un gestionnaire d’événements pour l’événement FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="92122-118">Add an event handler for the FrameNavigationStarting event.</span></span>
[<span data-ttu-id="92122-119">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="92122-119">add_HistoryChanged</span></span>](#add_historychanged) | <span data-ttu-id="92122-120">Facturationmodifier écoutez la modification de l’historique de navigation du document de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="92122-120">HistoryChange listen to the change of navigation history for the top level document.</span></span>
[<span data-ttu-id="92122-121">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="92122-121">add_NavigationCompleted</span></span>](#add_navigationcompleted) | <span data-ttu-id="92122-122">Ajoutez un gestionnaire d’événements pour l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="92122-122">Add an event handler for the NavigationCompleted event.</span></span>
[<span data-ttu-id="92122-123">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="92122-123">add_NavigationStarting</span></span>](#add_navigationstarting) | <span data-ttu-id="92122-124">Ajoutez un gestionnaire d’événements pour l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="92122-124">Add an event handler for the NavigationStarting event.</span></span>
[<span data-ttu-id="92122-125">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="92122-125">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="92122-126">Ajoutez un gestionnaire d’événements pour l’événement NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="92122-126">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="92122-127">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="92122-127">add_PermissionRequested</span></span>](#add_permissionrequested) | <span data-ttu-id="92122-128">Ajoutez un gestionnaire d’événements pour l’événement PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="92122-128">Add an event handler for the PermissionRequested event.</span></span>
[<span data-ttu-id="92122-129">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="92122-129">add_ProcessFailed</span></span>](#add_processfailed) | <span data-ttu-id="92122-130">Ajoutez un gestionnaire d’événements pour l’événement ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="92122-130">Add an event handler for the ProcessFailed event.</span></span>
[<span data-ttu-id="92122-131">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="92122-131">add_ScriptDialogOpening</span></span>](#add_scriptdialogopening) | <span data-ttu-id="92122-132">Ajoutez un gestionnaire d’événements pour l’événement ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="92122-132">Add an event handler for the ScriptDialogOpening event.</span></span>
[<span data-ttu-id="92122-133">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="92122-133">add_SourceChanged</span></span>](#add_sourcechanged) | <span data-ttu-id="92122-134">SourceChanged se déclenche lorsque la propriété source change.</span><span class="sxs-lookup"><span data-stu-id="92122-134">SourceChanged fires when the Source property changes.</span></span>
[<span data-ttu-id="92122-135">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="92122-135">add_WebMessageReceived</span></span>](#add_webmessagereceived) | <span data-ttu-id="92122-136">Cet événement se déclenche lorsque le paramètre IsWebMessageEnabled est défini et au document de niveau supérieur des appels WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="92122-136">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>
[<span data-ttu-id="92122-137">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="92122-137">add_WebResourceRequested</span></span>](#add_webresourcerequested) | <span data-ttu-id="92122-138">Ajoutez un gestionnaire d’événements pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="92122-138">Add an event handler for the WebResourceRequested event.</span></span>
[<span data-ttu-id="92122-139">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="92122-139">add_WindowCloseRequested</span></span>](#add_windowcloserequested) | <span data-ttu-id="92122-140">Ajoutez un gestionnaire d’événements pour l’événement WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="92122-140">Add an event handler for the WindowCloseRequested event.</span></span>
[<span data-ttu-id="92122-141">AddHostObjectToScript</span><span class="sxs-lookup"><span data-stu-id="92122-141">AddHostObjectToScript</span></span>](#addhostobjecttoscript) | <span data-ttu-id="92122-142">Ajoutez l’objet hôte fourni au script qui s’exécute sur le WebView avec le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="92122-142">Add the provided host object to script running in the WebView with the specified name.</span></span>
[<span data-ttu-id="92122-143">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="92122-143">AddScriptToExecuteOnDocumentCreated</span></span>](#addscripttoexecuteondocumentcreated) | <span data-ttu-id="92122-144">Ajoutez le code JavaScript fourni à une liste de scripts qui doivent être exécutés après la création de l’objet global, mais avant l’analyse du document HTML et avant l’exécution de tout autre script fourni par le document HTML.</span><span class="sxs-lookup"><span data-stu-id="92122-144">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>
[<span data-ttu-id="92122-145">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="92122-145">AddWebResourceRequestedFilter</span></span>](#addwebresourcerequestedfilter) | <span data-ttu-id="92122-146">Ajoute un URI et un filtre de contexte de ressources à l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="92122-146">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>
[<span data-ttu-id="92122-147">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="92122-147">CallDevToolsProtocolMethod</span></span>](#calldevtoolsprotocolmethod) | <span data-ttu-id="92122-148">Appelez une méthode DevToolsProtocol asynchrone.</span><span class="sxs-lookup"><span data-stu-id="92122-148">Call an asynchronous DevToolsProtocol method.</span></span>
[<span data-ttu-id="92122-149">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="92122-149">CapturePreview</span></span>](#capturepreview) | <span data-ttu-id="92122-150">Capturez une image de l’affichage du WebView.</span><span class="sxs-lookup"><span data-stu-id="92122-150">Capture an image of what WebView is displaying.</span></span>
[<span data-ttu-id="92122-151">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="92122-151">ExecuteScript</span></span>](#executescript) | <span data-ttu-id="92122-152">Exécutez le code JavaScript du paramètre JavaScript du document de niveau supérieur actuel affiché dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="92122-152">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="92122-153">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="92122-153">get_BrowserProcessId</span></span>](#get_browserprocessid) | <span data-ttu-id="92122-154">ID de processus du processus de navigation qui héberge le WebView.</span><span class="sxs-lookup"><span data-stu-id="92122-154">The process id of the browser process that hosts the WebView.</span></span>
[<span data-ttu-id="92122-155">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="92122-155">get_CanGoBack</span></span>](#get_cangoback) | <span data-ttu-id="92122-156">Renvoie vrai si le WebView peut accéder à une page précédente de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="92122-156">Returns true if the webview can navigate to a previous page in the navigation history.</span></span>
[<span data-ttu-id="92122-157">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="92122-157">get_CanGoForward</span></span>](#get_cangoforward) | <span data-ttu-id="92122-158">Cette fonction renvoie la valeur vrai si le WebView peut accéder à une page suivante de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="92122-158">Returns true if the webview can navigate to a next page in the navigation history.</span></span>
[<span data-ttu-id="92122-159">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="92122-159">get_ContainsFullScreenElement</span></span>](#get_containsfullscreenelement) | <span data-ttu-id="92122-160">Indique si le WebView contient un élément HTML fullscreen.</span><span class="sxs-lookup"><span data-stu-id="92122-160">Indicates if the WebView contains a fullscreen HTML element.</span></span>
[<span data-ttu-id="92122-161">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="92122-161">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="92122-162">Titre du document de niveau supérieur actuel.</span><span class="sxs-lookup"><span data-stu-id="92122-162">The title for the current top level document.</span></span>
[<span data-ttu-id="92122-163">get_Settings</span><span class="sxs-lookup"><span data-stu-id="92122-163">get_Settings</span></span>](#get_settings) | <span data-ttu-id="92122-164">L’objet [ICoreWebView2Settings](icorewebview2settings.md) contient différents paramètres modifiables pour le WebView en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="92122-164">The [ICoreWebView2Settings](icorewebview2settings.md) object contains various modifiable settings for the running WebView.</span></span>
[<span data-ttu-id="92122-165">get_Source</span><span class="sxs-lookup"><span data-stu-id="92122-165">get_Source</span></span>](#get_source) | <span data-ttu-id="92122-166">URI du document de niveau supérieur actuel.</span><span class="sxs-lookup"><span data-stu-id="92122-166">The URI of the current top level document.</span></span>
[<span data-ttu-id="92122-167">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="92122-167">GetDevToolsProtocolEventReceiver</span></span>](#getdevtoolsprotocoleventreceiver) | <span data-ttu-id="92122-168">Obtenez un destinataire d’événement de protocole DevTools qui vous permet de vous abonner à un événement de protocole DevTools.</span><span class="sxs-lookup"><span data-stu-id="92122-168">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>
[<span data-ttu-id="92122-169">GoBack</span><span class="sxs-lookup"><span data-stu-id="92122-169">GoBack</span></span>](#goback) | <span data-ttu-id="92122-170">Permet d’accéder à la page précédente de l’historique de navigation via le WebView.</span><span class="sxs-lookup"><span data-stu-id="92122-170">Navigates the WebView to the previous page in the navigation history.</span></span>
[<span data-ttu-id="92122-171">GoForward</span><span class="sxs-lookup"><span data-stu-id="92122-171">GoForward</span></span>](#goforward) | <span data-ttu-id="92122-172">Navigue vers la page suivante de l’historique de navigation du WebView.</span><span class="sxs-lookup"><span data-stu-id="92122-172">Navigates the WebView to the next page in the navigation history.</span></span>
[<span data-ttu-id="92122-173">Rechercher</span><span class="sxs-lookup"><span data-stu-id="92122-173">Navigate</span></span>](#navigate) | <span data-ttu-id="92122-174">Entraîner une navigation du document de niveau supérieur sur l’URI spécifié.</span><span class="sxs-lookup"><span data-stu-id="92122-174">Cause a navigation of the top level document to the specified URI.</span></span>
[<span data-ttu-id="92122-175">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="92122-175">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="92122-176">Lance une navigation vers htmlContent en tant que code HTML source d’un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="92122-176">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="92122-177">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="92122-177">OpenDevToolsWindow</span></span>](#opendevtoolswindow) | <span data-ttu-id="92122-178">Ouvre la fenêtre DevTools pour le document actif dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="92122-178">Opens the DevTools window for the current document in the WebView.</span></span>
[<span data-ttu-id="92122-179">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="92122-179">PostWebMessageAsJson</span></span>](#postwebmessageasjson) | <span data-ttu-id="92122-180">Publier le WebMessage spécifié sur le document de niveau supérieur dans ce WebView.</span><span class="sxs-lookup"><span data-stu-id="92122-180">Post the specified webMessage to the top level document in this WebView.</span></span>
[<span data-ttu-id="92122-181">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="92122-181">PostWebMessageAsString</span></span>](#postwebmessageasstring) | <span data-ttu-id="92122-182">Il s’agit d’un programme d’assistance pour publier un message qui est une chaîne simple plutôt qu’une représentation de chaîne JSON d’un objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="92122-182">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>
[<span data-ttu-id="92122-183">Recharger</span><span class="sxs-lookup"><span data-stu-id="92122-183">Reload</span></span>](#reload) | <span data-ttu-id="92122-184">Recharger la page active.</span><span class="sxs-lookup"><span data-stu-id="92122-184">Reload the current page.</span></span>
[<span data-ttu-id="92122-185">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="92122-185">remove_ContainsFullScreenElementChanged</span></span>](#remove_containsfullscreenelementchanged) | <span data-ttu-id="92122-186">Supprimez le gestionnaire d’événements précédemment ajouté avec la méthode d’événement add_ correspondante.</span><span class="sxs-lookup"><span data-stu-id="92122-186">Remove an event handler previously added with the corresponding add_ event method.</span></span>
[<span data-ttu-id="92122-187">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="92122-187">remove_ContentLoading</span></span>](#remove_contentloading) | <span data-ttu-id="92122-188">Supprimez un gestionnaire d’événements préalablement ajouté à add_ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="92122-188">Remove an event handler previously added with add_ContentLoading.</span></span>
[<span data-ttu-id="92122-189">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="92122-189">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="92122-190">Supprimez un gestionnaire d’événements préalablement ajouté à add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="92122-190">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="92122-191">remove_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="92122-191">remove_FrameNavigationCompleted</span></span>](#remove_framenavigationcompleted) | <span data-ttu-id="92122-192">Supprimez un gestionnaire d’événements préalablement ajouté à add_FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="92122-192">Remove an event handler previously added with add_FrameNavigationCompleted.</span></span>
[<span data-ttu-id="92122-193">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="92122-193">remove_FrameNavigationStarting</span></span>](#remove_framenavigationstarting) | <span data-ttu-id="92122-194">Supprimez un gestionnaire d’événements préalablement ajouté à add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="92122-194">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>
[<span data-ttu-id="92122-195">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="92122-195">remove_HistoryChanged</span></span>](#remove_historychanged) | <span data-ttu-id="92122-196">Supprimez un gestionnaire d’événements préalablement ajouté à add_HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="92122-196">Remove an event handler previously added with add_HistoryChanged.</span></span>
[<span data-ttu-id="92122-197">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="92122-197">remove_NavigationCompleted</span></span>](#remove_navigationcompleted) | <span data-ttu-id="92122-198">Supprimez un gestionnaire d’événements préalablement ajouté à add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="92122-198">Remove an event handler previously added with add_NavigationCompleted.</span></span>
[<span data-ttu-id="92122-199">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="92122-199">remove_NavigationStarting</span></span>](#remove_navigationstarting) | <span data-ttu-id="92122-200">Supprimez un gestionnaire d’événements préalablement ajouté à add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="92122-200">Remove an event handler previously added with add_NavigationStarting.</span></span>
[<span data-ttu-id="92122-201">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="92122-201">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="92122-202">Supprimez un gestionnaire d’événements préalablement ajouté à add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="92122-202">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="92122-203">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="92122-203">remove_PermissionRequested</span></span>](#remove_permissionrequested) | <span data-ttu-id="92122-204">Supprimez un gestionnaire d’événements préalablement ajouté à add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="92122-204">Remove an event handler previously added with add_PermissionRequested.</span></span>
[<span data-ttu-id="92122-205">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="92122-205">remove_ProcessFailed</span></span>](#remove_processfailed) | <span data-ttu-id="92122-206">Supprimez un gestionnaire d’événements préalablement ajouté à add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="92122-206">Remove an event handler previously added with add_ProcessFailed.</span></span>
[<span data-ttu-id="92122-207">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="92122-207">remove_ScriptDialogOpening</span></span>](#remove_scriptdialogopening) | <span data-ttu-id="92122-208">Supprimez un gestionnaire d’événements préalablement ajouté à add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="92122-208">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>
[<span data-ttu-id="92122-209">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="92122-209">remove_SourceChanged</span></span>](#remove_sourcechanged) | <span data-ttu-id="92122-210">Supprimez un gestionnaire d’événements préalablement ajouté à add_SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="92122-210">Remove an event handler previously added with add_SourceChanged.</span></span>
[<span data-ttu-id="92122-211">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="92122-211">remove_WebMessageReceived</span></span>](#remove_webmessagereceived) | <span data-ttu-id="92122-212">Supprimez un gestionnaire d’événements préalablement ajouté à add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="92122-212">Remove an event handler previously added with add_WebMessageReceived.</span></span>
[<span data-ttu-id="92122-213">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="92122-213">remove_WebResourceRequested</span></span>](#remove_webresourcerequested) | <span data-ttu-id="92122-214">Supprimez un gestionnaire d’événements préalablement ajouté à add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="92122-214">Remove an event handler previously added with add_WebResourceRequested.</span></span>
[<span data-ttu-id="92122-215">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="92122-215">remove_WindowCloseRequested</span></span>](#remove_windowcloserequested) | <span data-ttu-id="92122-216">Supprimez un gestionnaire d’événements préalablement ajouté à add_WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="92122-216">Remove an event handler previously added with add_WindowCloseRequested.</span></span>
[<span data-ttu-id="92122-217">RemoveHostObjectFromScript</span><span class="sxs-lookup"><span data-stu-id="92122-217">RemoveHostObjectFromScript</span></span>](#removehostobjectfromscript) | <span data-ttu-id="92122-218">Supprimez l’objet hôte spécifié par le nom afin qu’il ne soit plus accessible à partir du code JavaScript du WebView.</span><span class="sxs-lookup"><span data-stu-id="92122-218">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>
[<span data-ttu-id="92122-219">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="92122-219">RemoveScriptToExecuteOnDocumentCreated</span></span>](#removescripttoexecuteondocumentcreated) | <span data-ttu-id="92122-220">Supprimez le JavaScript correspondant ajouté par le biais de AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="92122-220">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>
[<span data-ttu-id="92122-221">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="92122-221">RemoveWebResourceRequestedFilter</span></span>](#removewebresourcerequestedfilter) | <span data-ttu-id="92122-222">Supprime un filtre de ressources correspondant précédemment ajouté pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="92122-222">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>
[<span data-ttu-id="92122-223">Stop</span><span class="sxs-lookup"><span data-stu-id="92122-223">Stop</span></span>](#stop) | <span data-ttu-id="92122-224">Arrêtez toutes les navigations et les extractions de ressources en attente.</span><span class="sxs-lookup"><span data-stu-id="92122-224">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="92122-225">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="92122-225">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span>](#corewebview2_capture_preview_image_format) | <span data-ttu-id="92122-226">Format d’image utilisé par la méthode ICoreWebView2:: CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="92122-226">Image format used by the ICoreWebView2::CapturePreview method.</span></span>
[<span data-ttu-id="92122-227">COREWEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="92122-227">COREWEBVIEW2_KEY_EVENT_KIND</span></span>](#corewebview2_key_event_kind) | <span data-ttu-id="92122-228">Type d’événement de touche qui déclenchait un événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="92122-228">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="92122-229">COREWEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="92122-229">COREWEBVIEW2_MOVE_FOCUS_REASON</span></span>](#corewebview2_move_focus_reason) | <span data-ttu-id="92122-230">Raison du déplacement du focus.</span><span class="sxs-lookup"><span data-stu-id="92122-230">Reason for moving focus.</span></span>
[<span data-ttu-id="92122-231">COREWEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="92122-231">COREWEBVIEW2_PERMISSION_KIND</span></span>](#corewebview2_permission_kind) | <span data-ttu-id="92122-232">Le type d’une demande d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="92122-232">The type of a permission request.</span></span>
[<span data-ttu-id="92122-233">COREWEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="92122-233">COREWEBVIEW2_PERMISSION_STATE</span></span>](#corewebview2_permission_state) | <span data-ttu-id="92122-234">Réponse à une demande d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="92122-234">Response to a permission request.</span></span>
[<span data-ttu-id="92122-235">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="92122-235">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span></span>](#corewebview2_physical_key_status) | <span data-ttu-id="92122-236">Structure représentant les informations contenues dans le LPARAM fourni à un événement de touche Win32.</span><span class="sxs-lookup"><span data-stu-id="92122-236">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>
[<span data-ttu-id="92122-237">COREWEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="92122-237">COREWEBVIEW2_PROCESS_FAILED_KIND</span></span>](#corewebview2_process_failed_kind) | <span data-ttu-id="92122-238">Type d’échec de processus utilisé dans l’interface ICoreWebView2ProcessFailedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="92122-238">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>
[<span data-ttu-id="92122-239">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="92122-239">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span></span>](#corewebview2_script_dialog_kind) | <span data-ttu-id="92122-240">Type de boîte de dialogue JavaScript utilisée dans l’interface ICoreWebView2ScriptDialogOpeningEventHandler.</span><span class="sxs-lookup"><span data-stu-id="92122-240">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>
[<span data-ttu-id="92122-241">COREWEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="92122-241">COREWEBVIEW2_WEB_ERROR_STATUS</span></span>](#corewebview2_web_error_status) | <span data-ttu-id="92122-242">Valeurs d’état d’erreur pour les navigations Web.</span><span class="sxs-lookup"><span data-stu-id="92122-242">Error status values for web navigations.</span></span>
[<span data-ttu-id="92122-243">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="92122-243">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span></span>](#corewebview2_web_resource_context) | <span data-ttu-id="92122-244">Énum pour les contextes de demande de ressources Web.</span><span class="sxs-lookup"><span data-stu-id="92122-244">Enum for web resource request contexts.</span></span>

## <span data-ttu-id="92122-245">Événements de navigation</span><span class="sxs-lookup"><span data-stu-id="92122-245">Navigation events</span></span>

<span data-ttu-id="92122-246">L’ordre normal des événements de navigation est NavigationStarting, SourceChanged, ContentLoading, puis NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="92122-246">The normal sequence of navigation events is NavigationStarting, SourceChanged, ContentLoading and then NavigationCompleted.</span></span>

![dot-Inline-dotgraph-1. png](media/dot-inline-dotgraph-1.png)

<span data-ttu-id="92122-248">Notez qu’il s’agit d’événements de navigation avec le même argument d’événement NavigationId.</span><span class="sxs-lookup"><span data-stu-id="92122-248">Note that this is for navigation events with the same NavigationId event arg.</span></span> <span data-ttu-id="92122-249">Les événements de navigation avec différents arguments d’événement NavigationId risquent de se chevaucher.</span><span class="sxs-lookup"><span data-stu-id="92122-249">Navigations events with different NavigationId event args may overlap.</span></span> <span data-ttu-id="92122-250">Par exemple, si vous démarrez une navigation pour l’événement NavigationStarting, puis démarrez une autre navigation, vous verrez le NavigationStarting de la première navigation suivi par le NavigationStarting du deuxième navigation, suivi de l’NavigationCompleted de la première navigation, puis de tout le reste des événements de navigation appropriés pour la deuxième navigation.</span><span class="sxs-lookup"><span data-stu-id="92122-250">For instance, if you start a navigation wait for its NavigationStarting event and then start another navigation you'll see the NavigationStarting for the first navigate followed by the NavigationStarting of the second navigate, followed by the NavigationCompleted for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span> <span data-ttu-id="92122-251">Dans les cas d’erreur, il est possible ou non qu’un événement ContentLoading se poursuive sur une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="92122-251">In error cases there may or may not be a ContentLoading event depending on whether the navigation is continued to an error page.</span></span> <span data-ttu-id="92122-252">Dans le cas d’une redirection HTTP, plusieurs événements NavigationStarting sont disponibles dans une ligne, avec les indicateurs IsRedirect définis dans le premier.</span><span class="sxs-lookup"><span data-stu-id="92122-252">In case of an HTTP redirect, there will be multiple NavigationStarting events in a row, with ones following the first will have their IsRedirect flag set.</span></span>

<span data-ttu-id="92122-253">Pour surveiller ou annuler les navigations dans les sous-cadres du WebView, utilisez FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="92122-253">To monitor or cancel navigations inside subframes in the WebView, use FrameNavigationStarting.</span></span>

## <span data-ttu-id="92122-254">Modèle de processus</span><span class="sxs-lookup"><span data-stu-id="92122-254">Process model</span></span>

<span data-ttu-id="92122-255">WebView2 utilise le même modèle de processus que le navigateur Web Edge.</span><span class="sxs-lookup"><span data-stu-id="92122-255">WebView2 uses the same process model as the Edge web browser.</span></span> <span data-ttu-id="92122-256">Il existe un processus de navigateur Edge par répertoire de données utilisateur spécifié dans une session utilisateur qui traitera tout processus appelant WebView2 spécifiant ce répertoire de données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="92122-256">There is one Edge browser process per specified user data directory in a user session that will serve any WebView2 calling process that specifies that user data directory.</span></span> <span data-ttu-id="92122-257">Cela signifie qu’un processus de navigateur Edge est susceptible de traiter plusieurs processus d’appel et qu’un processus d’appel est susceptible d’utiliser plusieurs processus de navigation latérale.</span><span class="sxs-lookup"><span data-stu-id="92122-257">This means one Edge browser process may be serving multiple calling processes and one calling process may be using multiple Edge browser processes.</span></span>

![dot-Inline-dotgraph-2. png](media/dot-inline-dotgraph-2.png)

<span data-ttu-id="92122-259">Il y a un certain nombre de processus de convertisseur.</span><span class="sxs-lookup"><span data-stu-id="92122-259">Off of a browser process there will be some number of renderer processes.</span></span> <span data-ttu-id="92122-260">Celles-ci sont créées autant de fois que nécessaire pour traiter plusieurs trames dans différents affichages.</span><span class="sxs-lookup"><span data-stu-id="92122-260">These are created as necessary to service potentially multiple frames in different WebViews.</span></span> <span data-ttu-id="92122-261">Le nombre de processus de rendu varie en fonction de la fonctionnalité du navigateur d’isolement de site et du nombre d’origines distantes distinctes affichées dans les webvues associées.</span><span class="sxs-lookup"><span data-stu-id="92122-261">The number of renderer processes varies based on the site isolation browser feature and the number of distinct disconnected origins rendered in associated WebViews.</span></span>

![dot-Inline-dotgraph-3. png](media/dot-inline-dotgraph-3.png)

<span data-ttu-id="92122-263">Vous pouvez réagir aux blocages et se bloquer dans ces processus de navigateur et de convertisseur à l’aide de l’événement ProcessFailure.</span><span class="sxs-lookup"><span data-stu-id="92122-263">You can react to crashes and hangs in these browser and renderer processes using the ProcessFailure event.</span></span>

<span data-ttu-id="92122-264">Vous pouvez arrêter en toute sécurité les processus de navigateur et de convertisseur associés à l’aide de la méthode Close.</span><span class="sxs-lookup"><span data-stu-id="92122-264">You can safely shutdown associated browser and renderer processes using the Close method.</span></span>

## <span data-ttu-id="92122-265">Modèle de threads</span><span class="sxs-lookup"><span data-stu-id="92122-265">Threading model</span></span>

<span data-ttu-id="92122-266">WebView2 doit être créé sur un thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="92122-266">The WebView2 must be created on a UI thread.</span></span> <span data-ttu-id="92122-267">Particulièrement un thread avec une pompe de messages.</span><span class="sxs-lookup"><span data-stu-id="92122-267">Specifically a thread with a message pump.</span></span> <span data-ttu-id="92122-268">Tous les rappels se produiront sur ce thread et les appels dans le WebView doivent être effectués sur ce thread.</span><span class="sxs-lookup"><span data-stu-id="92122-268">All callbacks will occur on that thread and calls into the WebView must be done on that thread.</span></span> <span data-ttu-id="92122-269">Il n’est pas sûr d’utiliser le WebView à partir d’un autre thread.</span><span class="sxs-lookup"><span data-stu-id="92122-269">It is not safe to use the WebView from another thread.</span></span>

<span data-ttu-id="92122-270">Les rappels incluant des gestionnaires d’événements et des gestionnaires d’achèvement s’exécutent en série.</span><span class="sxs-lookup"><span data-stu-id="92122-270">Callbacks including event handlers and completion handlers execute serially.</span></span> <span data-ttu-id="92122-271">Autrement dit, si vous disposez d’un gestionnaire d’événements et commencez une boucle de message, il n’y a pas de gestionnaires d’événements ou de rappels d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="92122-271">That is, if you have an event handler running and begin a message loop no other event handlers or completion callbacks will begin executing reentrantly.</span></span>

## <span data-ttu-id="92122-272">Sécurité</span><span class="sxs-lookup"><span data-stu-id="92122-272">Security</span></span>

<span data-ttu-id="92122-273">Vérifiez toujours la propriété source de WebView avant d’utiliser ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString, ou toute autre méthode pour envoyer des informations dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="92122-273">Always check the Source property of the WebView before using ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString, or any other method to send information into the WebView.</span></span> <span data-ttu-id="92122-274">Le WebView peut avoir navigué vers une autre page par le biais de l’utilisateur final qui interagit avec la page ou le script de la page entraînant la navigation.</span><span class="sxs-lookup"><span data-stu-id="92122-274">The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation.</span></span> <span data-ttu-id="92122-275">De même, soyez prudent avec AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="92122-275">Similarly, be very careful with AddScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="92122-276">Toutes les futures navigations exécuteront ce script et, s’il donne accès à des informations destinées uniquement à un certain type d’origine, tous les documents HTML peuvent avoir accès.</span><span class="sxs-lookup"><span data-stu-id="92122-276">All future navigations will run this script and if it provides access to information intended only for a certain origin, any HTML document may have access.</span></span>

<span data-ttu-id="92122-277">Lorsque vous examinez le résultat d’un appel de méthode ExecuteScript, un événement WebMessageReceived, vérifie toujours la source de l’expéditeur ou tout autre mécanisme de réception d’informations à partir d’un document HTML dans un WebView valide l’URI du document HTML correspond à ce que vous attendez.</span><span class="sxs-lookup"><span data-stu-id="92122-277">When examining the result of an ExecuteScript method call, a WebMessageReceived event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.</span></span>

<span data-ttu-id="92122-278">Lorsque vous construisez un message à envoyer dans un WebView, préférez utilisez PostWebMessageAsJson et construisez le paramètre de chaîne JSON à l’aide d’une bibliothèque JSON.</span><span class="sxs-lookup"><span data-stu-id="92122-278">When constructing a message to send into a WebView, prefer using PostWebMessageAsJson and construct the JSON string parameter using a JSON library.</span></span> <span data-ttu-id="92122-279">Cela évite les accidents potentiels d’encoder des informations dans une chaîne ou un script JSON et garantir qu’aucune entrée contrôlée par l’attaquant ne peut modifier le reste du message JSON ou exécuter un script arbitraire.</span><span class="sxs-lookup"><span data-stu-id="92122-279">This will avoid any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script.</span></span>

## <span data-ttu-id="92122-280">Types de chaîne</span><span class="sxs-lookup"><span data-stu-id="92122-280">String types</span></span>

<span data-ttu-id="92122-281">Les paramètres de type chaîne sont des chaînes de type LPWSTR nul terminées.</span><span class="sxs-lookup"><span data-stu-id="92122-281">String out parameters are LPWSTR null terminated strings.</span></span> <span data-ttu-id="92122-282">Le l’appelant alloue la chaîne à l’aide de CoTaskMemAlloc.</span><span class="sxs-lookup"><span data-stu-id="92122-282">The callee allocates the string using CoTaskMemAlloc.</span></span> <span data-ttu-id="92122-283">La propriété est transférée à l’appelant et il revient à l’appelant de libérer de la mémoire à l’aide de CoTaskMemFree.</span><span class="sxs-lookup"><span data-stu-id="92122-283">Ownership is transferred to the caller and it is up to the caller to free the memory using CoTaskMemFree.</span></span>

<span data-ttu-id="92122-284">La chaîne figurant dans les paramètres est LPCWSTRe des chaînes arrêtées null.</span><span class="sxs-lookup"><span data-stu-id="92122-284">String in parameters are LPCWSTR null terminated strings.</span></span> <span data-ttu-id="92122-285">L’appelant vérifie que la chaîne est valide pour la durée de l’appel de fonction synchrone.</span><span class="sxs-lookup"><span data-stu-id="92122-285">The caller ensures the string is valid for the duration of the synchronous function call.</span></span> <span data-ttu-id="92122-286">Si les appelants doivent conserver cette valeur à un certain point après la fin de l’appel de fonction, l’appelant doit allouer sa propre copie de la valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="92122-286">If the callee needs to retain that value to some point after the function call completes, the callee must allocate its own copy of the string value.</span></span>

## <span data-ttu-id="92122-287">D’analyse des URI et de JSON</span><span class="sxs-lookup"><span data-stu-id="92122-287">URI and JSON parsing</span></span>

<span data-ttu-id="92122-288">Diverses méthodes fournissent ou acceptent des URI et JSON en tant que chaînes.</span><span class="sxs-lookup"><span data-stu-id="92122-288">Various methods provide or accept URIs and JSON as strings.</span></span> <span data-ttu-id="92122-289">Utilisez votre propre bibliothèque préférée pour analyser et générer ces chaînes.</span><span class="sxs-lookup"><span data-stu-id="92122-289">Please use your own preferred library for parsing and generating these strings.</span></span>

<span data-ttu-id="92122-290">Si WinRT est disponible pour votre application, vous pouvez l’utiliser `RuntimeClass_Windows_Data_Json_JsonObject` et `IJsonObjectStatics` analyser ou générer des chaînes JSON ou `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` analyser et générer des URI.</span><span class="sxs-lookup"><span data-stu-id="92122-290">If WinRT is available for your app you can use `RuntimeClass_Windows_Data_Json_JsonObject` and `IJsonObjectStatics` to parse or produce JSON strings or `RuntimeClass_Windows_Foundation_Uri` and `IUriRuntimeClassFactory` to parse and produce URIs.</span></span> <span data-ttu-id="92122-291">Ces deux fonctions fonctionnent dans les applications Win32.</span><span class="sxs-lookup"><span data-stu-id="92122-291">Both of these work in Win32 apps.</span></span>

<span data-ttu-id="92122-292">Si vous utilisez IUri et CreateUri pour analyser les URI, il est possible que vous souhaitiez utiliser les indicateurs de création d’URI suivants pour que le comportement CreateUri correspond plus étroitement à l’analyse d’URI dans le WebView:</span><span class="sxs-lookup"><span data-stu-id="92122-292">If you use IUri and CreateUri to parse URIs you may want to use the following URI creation flags to have CreateUri behavior more closely match the URI parsing in the WebView:</span></span> `Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO`

## <span data-ttu-id="92122-293">Débogage</span><span class="sxs-lookup"><span data-stu-id="92122-293">Debugging</span></span>

<span data-ttu-id="92122-294">Ouvrez DevTools avec les raccourcis normaux: `F12` ou `Ctrl+Shift+I` .</span><span class="sxs-lookup"><span data-stu-id="92122-294">Open DevTools with the normal shortcuts: `F12` or `Ctrl+Shift+I`.</span></span> <span data-ttu-id="92122-295">Vous pouvez utiliser le `--auto-open-devtools-for-tabs` commutateur d’argument de commande pour que la fenêtre devtools s’ouvre immédiatement lors de la création d’un WebView.</span><span class="sxs-lookup"><span data-stu-id="92122-295">You can use the `--auto-open-devtools-for-tabs` command argument switch to have the DevTools window open immediately when first creating a WebView.</span></span> <span data-ttu-id="92122-296">Pour plus d’informations sur le processus de navigation, voir documentation CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="92122-296">See CreateCoreWebView2Controller documentation for how to provide additional command line arguments to the browser process.</span></span> <span data-ttu-id="92122-297">Consultez la clé de Registre LoaderOverride pour essayer différentes builds de WebView2 sans modifier votre application dans la documentation CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="92122-297">Check out the LoaderOverride registry key for trying out different builds of WebView2 without modifying your application in the CreateCoreWebView2Controller documentation.</span></span>

## <span data-ttu-id="92122-298">Contrôle de version</span><span class="sxs-lookup"><span data-stu-id="92122-298">Versioning</span></span>

<span data-ttu-id="92122-299">Une fois que vous avez utilisé une version particulière du SDK pour générer votre application, l’exécution de votre application avec une version plus ancienne ou plus récente des fichiers binaires de navigateur installés sera terminée.</span><span class="sxs-lookup"><span data-stu-id="92122-299">After you've used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.</span></span> <span data-ttu-id="92122-300">Jusqu’à la version 1.0.0.0 de WebView2, des modifications peuvent être apportées lors des mises à jour qui empêchent votre SDK de fonctionner avec des versions différentes des fichiers binaires de navigateur installés.</span><span class="sxs-lookup"><span data-stu-id="92122-300">Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that will prevent your SDK from working with different versions of installed browser binaries.</span></span> <span data-ttu-id="92122-301">Après la version 1.0.0.0, vous pouvez utiliser les différentes versions du kit de développement logiciel (SDK) pour travailler avec les meilleures pratiques suivantes:</span><span class="sxs-lookup"><span data-stu-id="92122-301">After version 1.0.0.0 different versions of the SDK can work with different versions of the installed browser by following these best practices:</span></span>

<span data-ttu-id="92122-302">Pour prendre en compte les modifications apportées à l’API, veillez à vérifier l’échec lors de l’appel de la DLL d’exportation CreateCoreWebView2Environment et lors de l’appel de QueryInterface sur un objet CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="92122-302">To account for breaking changes to the API be sure to check for failure when calling the DLL export CreateCoreWebView2Environment and when calling QueryInterface on any CoreWebView2 object.</span></span> <span data-ttu-id="92122-303">La valeur de retour de E_NOINTERFACE peut indiquer que le kit de développement logiciel (SDK) n’est pas compatible avec les fichiers binaires de navigation Edge.</span><span class="sxs-lookup"><span data-stu-id="92122-303">A return value of E_NOINTERFACE can indicate the SDK is not compatible with the Edge browser binaries.</span></span>

<span data-ttu-id="92122-304">La vérification de l’échec de QueryInterface sera également comptabilisée dans les cas où le kit de développement logiciel (SDK) est plus récent que la version du navigateur Edge et que votre application tente d’utiliser une interface qui n’est pas compatible avec le navigateur Edge.</span><span class="sxs-lookup"><span data-stu-id="92122-304">Checking for failure from QueryInterface will also account for cases where the SDK is newer than the version of the Edge browser and your app attempts to use an interface of which the Edge browser is unaware.</span></span>

<span data-ttu-id="92122-305">Lorsqu’une interface n’est pas disponible, vous pouvez envisager de désactiver la fonctionnalité associée le cas échéant ou d’informer l’utilisateur final qu’il doit mettre à jour son navigateur.</span><span class="sxs-lookup"><span data-stu-id="92122-305">When an interface is unavailable, you can consider disabling the associated feature if possible, or otherwise informing the end user they need to update their browser.</span></span>

## <span data-ttu-id="92122-306">Ses</span><span class="sxs-lookup"><span data-stu-id="92122-306">Members</span></span>

#### <span data-ttu-id="92122-307">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="92122-307">add_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="92122-308">Avertit en cas de modification de la propriété ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="92122-308">Notifies when the ContainsFullScreenElement property changes.</span></span>

> <span data-ttu-id="92122-309">[add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)par le biais du[mot de passe](icorewebview2containsfullscreenelementchangedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="92122-309">public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](icorewebview2containsfullscreenelementchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="92122-310">Cela signifie qu’un élément HTML à l’intérieur du WebView est entré en plein écran jusqu’à la taille de l’affichage WebView ou en laissant le plein écran.</span><span class="sxs-lookup"><span data-stu-id="92122-310">This means that an HTML element inside the WebView is entering fullscreen to the size of the WebView or leaving fullscreen.</span></span> <span data-ttu-id="92122-311">Cet événement est utile, par exemple, lorsqu’un élément vidéo demande d’être placé en plein écran.</span><span class="sxs-lookup"><span data-stu-id="92122-311">This event is useful when, for example, a video element requests to go fullscreen.</span></span> <span data-ttu-id="92122-312">L’écouteur de ContainsFullScreenElementChanged peut alors redimensionner le WebView en réponse.</span><span class="sxs-lookup"><span data-stu-id="92122-312">The listener of ContainsFullScreenElementChanged can then resize the WebView in response.</span></span>

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

#### <span data-ttu-id="92122-313">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="92122-313">add_ContentLoading</span></span> 

<span data-ttu-id="92122-314">Ajoutez un gestionnaire d’événements pour l’événement ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="92122-314">Add an event handler for the ContentLoading event.</span></span>

> <span data-ttu-id="92122-315">[add_ContentLoading](#add_contentloading)par le biais du[mot de passe](icorewebview2contentloadingeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="92122-315">public HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](icorewebview2contentloadingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="92122-316">ContentLoading se déclenche avant le chargement du contenu, notamment les scripts ajoutés avec AddScriptToExecuteOnDocumentCreated ContentLoading ne se déclenchent pas si une même navigation de page se produit (par exemple par le biais des navigations ou de l’historique d’un fragment. pushState navigation).</span><span class="sxs-lookup"><span data-stu-id="92122-316">ContentLoading fires before any content is loaded, including scripts added with AddScriptToExecuteOnDocumentCreated ContentLoading will not fire if a same page navigation occurs (such as through fragment navigations or history.pushState navigations).</span></span> <span data-ttu-id="92122-317">Cela suit les événements NavigationStarting et SourceChanged, ainsi que les événements HistoryChanged et NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="92122-317">This follows the NavigationStarting and SourceChanged events and precedes the HistoryChanged and NavigationCompleted events.</span></span>

#### <span data-ttu-id="92122-318">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="92122-318">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="92122-319">Ajoutez un gestionnaire d’événements pour l’événement DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="92122-319">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="92122-320">[add_DocumentTitleChanged](#add_documenttitlechanged)par le biais du[mot de passe](icorewebview2documenttitlechangedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="92122-320">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](icorewebview2documenttitlechangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="92122-321">L’événement se déclenche lorsque la propriété DocumentTitle de WebView change et qu’il est susceptible de se déclencher avant ou après l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="92122-321">The event fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

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

#### <span data-ttu-id="92122-322">add_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="92122-322">add_FrameNavigationCompleted</span></span> 

<span data-ttu-id="92122-323">Ajoutez un gestionnaire d’événements pour l’événement FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="92122-323">Add an event handler for the FrameNavigationCompleted event.</span></span>

> <span data-ttu-id="92122-324">[add_FrameNavigationCompleted](#add_framenavigationcompleted)par le biais du[mot de passe](icorewebview2navigationcompletedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="92122-324">public HRESULT [add_FrameNavigationCompleted](#add_framenavigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="92122-325">L’événement FrameNavigationCompleted se déclenche quand une image enfant est complètement chargée (le corps. OnLoad a déclenché) ou si le chargement a été arrêté avec une erreur.</span><span class="sxs-lookup"><span data-stu-id="92122-325">FrameNavigationCompleted event fires when a child frame has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

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

#### <span data-ttu-id="92122-326">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="92122-326">add_FrameNavigationStarting</span></span> 

<span data-ttu-id="92122-327">Ajoutez un gestionnaire d’événements pour l’événement FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="92122-327">Add an event handler for the FrameNavigationStarting event.</span></span>

> <span data-ttu-id="92122-328">[add_FrameNavigationStarting](#add_framenavigationstarting)par le biais du[mot de passe](icorewebview2navigationstartingeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="92122-328">public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="92122-329">FrameNavigationStarting se déclenche quand une Frame enfant du WebView demande une autorisation pour accéder à un URI différent.</span><span class="sxs-lookup"><span data-stu-id="92122-329">FrameNavigationStarting fires when a child frame in the WebView requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="92122-330">Cela se déclenche également pour les redirections.</span><span class="sxs-lookup"><span data-stu-id="92122-330">This will fire for redirects as well.</span></span>

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

#### <span data-ttu-id="92122-331">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="92122-331">add_HistoryChanged</span></span> 

<span data-ttu-id="92122-332">Facturationmodifier écoutez la modification de l’historique de navigation du document de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="92122-332">HistoryChange listen to the change of navigation history for the top level document.</span></span>

> <span data-ttu-id="92122-333">[add_HistoryChanged](#add_historychanged)par le biais du[mot de passe](icorewebview2historychangedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="92122-333">public HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](icorewebview2historychangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="92122-334">Utilisez Facturationmodifier pour vérifier si la valeur CanGoBack/CanGoForward a changé.</span><span class="sxs-lookup"><span data-stu-id="92122-334">Use HistoryChange to check if CanGoBack/CanGoForward value has changed.</span></span> <span data-ttu-id="92122-335">HistoryChanged est également déclenché pour l’utilisation de GoBack/GoForward.</span><span class="sxs-lookup"><span data-stu-id="92122-335">HistoryChanged also fires for using GoBack/GoForward.</span></span> <span data-ttu-id="92122-336">HistoryChanged se déclenche après SourceChanged et ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="92122-336">HistoryChanged fires after SourceChanged and ContentLoading.</span></span> <span data-ttu-id="92122-337">Ajoutez un gestionnaire d’événements pour l’événement HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="92122-337">Add an event handler for the HistoryChanged event.</span></span> 
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
                EnableWindow(m_toolbar->backWindow, canGoBack);
                EnableWindow(m_toolbar->forwardWindow, canGoForward);

                return S_OK;
            })
            .Get(),
        &m_historyChangedToken));
```

#### <span data-ttu-id="92122-338">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="92122-338">add_NavigationCompleted</span></span> 

<span data-ttu-id="92122-339">Ajoutez un gestionnaire d’événements pour l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="92122-339">Add an event handler for the NavigationCompleted event.</span></span>

> <span data-ttu-id="92122-340">[add_NavigationCompleted](#add_navigationcompleted)par le biais du[mot de passe](icorewebview2navigationcompletedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="92122-340">public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="92122-341">L’événement NavigationCompleted se déclenche lorsque le WebView est complètement chargé (le corps. OnLoad a été déclenché) ou que le chargement s’est arrêté avec une erreur.</span><span class="sxs-lookup"><span data-stu-id="92122-341">NavigationCompleted event fires when the WebView has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

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
                EnableWindow(m_toolbar->cancelWindow, FALSE);
                return S_OK;
            })
            .Get(),
        &m_navigationCompletedToken));
```

#### <span data-ttu-id="92122-342">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="92122-342">add_NavigationStarting</span></span> 

<span data-ttu-id="92122-343">Ajoutez un gestionnaire d’événements pour l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="92122-343">Add an event handler for the NavigationStarting event.</span></span>

> <span data-ttu-id="92122-344">[add_NavigationStarting](#add_navigationstarting)par le biais du[mot de passe](icorewebview2navigationstartingeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="92122-344">public HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="92122-345">NavigationStarting se déclenche lorsque le frame principal WebView demande une autorisation pour accéder à un URI différent.</span><span class="sxs-lookup"><span data-stu-id="92122-345">NavigationStarting fires when the WebView main frame is requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="92122-346">Cela se déclenche également pour les redirections.</span><span class="sxs-lookup"><span data-stu-id="92122-346">This will fire for redirects as well.</span></span>

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

#### <span data-ttu-id="92122-347">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="92122-347">add_NewWindowRequested</span></span> 

<span data-ttu-id="92122-348">Ajoutez un gestionnaire d’événements pour l’événement NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="92122-348">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="92122-349">[add_NewWindowRequested](#add_newwindowrequested)par le biais du[mot de passe](icorewebview2newwindowrequestedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="92122-349">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](icorewebview2newwindowrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="92122-350">Se déclenche lorsque le contenu à l’intérieur du WebView est demandé pour ouvrir une nouvelle fenêtre, par exemple via Window. Open.</span><span class="sxs-lookup"><span data-stu-id="92122-350">Fires when content inside the WebView requested to open a new window, such as through window.open.</span></span> <span data-ttu-id="92122-351">L’application peut transmettre un WebView cible qui sera considéré comme la fenêtre ouverte.</span><span class="sxs-lookup"><span data-stu-id="92122-351">The app can pass a target webview that will be considered the opened window.</span></span>

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

                newAppWindow = new AppWindow(m_creationModeId, L"");
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

#### <span data-ttu-id="92122-352">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="92122-352">add_PermissionRequested</span></span> 

<span data-ttu-id="92122-353">Ajoutez un gestionnaire d’événements pour l’événement PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="92122-353">Add an event handler for the PermissionRequested event.</span></span>

> <span data-ttu-id="92122-354">[add_PermissionRequested](#add_permissionrequested)par le biais du[mot de passe](icorewebview2permissionrequestedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="92122-354">public HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](icorewebview2permissionrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="92122-355">Se déclenche lorsque le contenu d’un WebView demande l’autorisation d’accéder à des ressources privilégiées.</span><span class="sxs-lookup"><span data-stu-id="92122-355">Fires when content in a WebView requests permission to access some privileged resources.</span></span>

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

#### <span data-ttu-id="92122-356">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="92122-356">add_ProcessFailed</span></span> 

<span data-ttu-id="92122-357">Ajoutez un gestionnaire d’événements pour l’événement ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="92122-357">Add an event handler for the ProcessFailed event.</span></span>

> <span data-ttu-id="92122-358">[add_ProcessFailed](#add_processfailed)par le biais du[mot de passe](icorewebview2processfailedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="92122-358">public HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](icorewebview2processfailedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="92122-359">Se déclenche quand un processus WebView s’est arrêté de manière inattendue ou ne répond plus.</span><span class="sxs-lookup"><span data-stu-id="92122-359">Fires when a WebView process terminated unexpectedly or become unresponsive.</span></span>

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

#### <span data-ttu-id="92122-360">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="92122-360">add_ScriptDialogOpening</span></span> 

<span data-ttu-id="92122-361">Ajoutez un gestionnaire d’événements pour l’événement ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="92122-361">Add an event handler for the ScriptDialogOpening event.</span></span>

> <span data-ttu-id="92122-362">[add_ScriptDialogOpening](#add_scriptdialogopening)par le biais du[mot de passe](icorewebview2scriptdialogopeningeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="92122-362">public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](icorewebview2scriptdialogopeningeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="92122-363">L’événement se déclenche quand une boîte de dialogue JavaScript (alerte, confirmation ou invite) s’affiche pour le WebView.</span><span class="sxs-lookup"><span data-stu-id="92122-363">The event fires when a JavaScript dialog (alert, confirm, or prompt) will show for the webview.</span></span> <span data-ttu-id="92122-364">Cet événement est déclenché uniquement si la propriété ICoreWebView2Settings:: AreDefaultScriptDialogsEnabled est définie sur false.</span><span class="sxs-lookup"><span data-stu-id="92122-364">This event only fires if the ICoreWebView2Settings::AreDefaultScriptDialogsEnabled property is set to false.</span></span> <span data-ttu-id="92122-365">L’événement ScriptDialogOpening peut être utilisé pour supprimer des boîtes de dialogue ou remplacer les boîtes de dialogue par défaut par des boîtes de dialogue personnalisées.</span><span class="sxs-lookup"><span data-stu-id="92122-365">The ScriptDialogOpening event can be used to suppress dialogs or replace default dialogs with custom dialogs.</span></span>

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

#### <span data-ttu-id="92122-366">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="92122-366">add_SourceChanged</span></span> 

<span data-ttu-id="92122-367">SourceChanged se déclenche lorsque la propriété source change.</span><span class="sxs-lookup"><span data-stu-id="92122-367">SourceChanged fires when the Source property changes.</span></span>

> <span data-ttu-id="92122-368">[add_SourceChanged](#add_sourcechanged)par le biais du[mot de passe](icorewebview2sourcechangedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="92122-368">public HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](icorewebview2sourcechangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="92122-369">L’utilisation de l’fonction SourceChanged est déclenchée pour accéder à un site ou à un fragment de navigation différent.</span><span class="sxs-lookup"><span data-stu-id="92122-369">SourceChanged fires for navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="92122-370">Il ne se déclenche pas pour les autres types de navigation, tels que les recharges de page ou l’historique. pushState avec la même URL que la page active.</span><span class="sxs-lookup"><span data-stu-id="92122-370">It will not fires for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span> <span data-ttu-id="92122-371">SourceChanged se déclenche avant ContentLoading pour la navigation vers un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="92122-371">SourceChanged fires before ContentLoading for navigation to a new document.</span></span> <span data-ttu-id="92122-372">Ajoutez un gestionnaire d’événements pour l’événement SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="92122-372">Add an event handler for the SourceChanged event.</span></span> 
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
                SetWindowText(m_toolbar->addressBarWindow, uri.get());

                return S_OK;
            })
            .Get(),
        &m_sourceChangedToken));
```

#### <span data-ttu-id="92122-373">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="92122-373">add_WebMessageReceived</span></span> 

<span data-ttu-id="92122-374">Cet événement se déclenche lorsque le paramètre IsWebMessageEnabled est défini et au document de niveau supérieur des appels WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="92122-374">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>

> <span data-ttu-id="92122-375">[add_WebMessageReceived](#add_webmessagereceived)par le biais[ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="92122-375">public HRESULT [add_WebMessageReceived](#add_webmessagereceived)([ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) \* handler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="92122-376">La fonction postMessage est l' `void postMessage(object)` emplacement de tout objet pris en charge par la conversion JSON.</span><span class="sxs-lookup"><span data-stu-id="92122-376">The postMessage function is `void postMessage(object)` where object is any object supported by JSON conversion.</span></span>

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
 <span data-ttu-id="92122-377">Lorsque postMessage est appelée, le [ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) défini par le biais de cette méthode SetWebMessageReceivedEventHandler sera appelé avec le paramètre objet de PostMessage converti en chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="92122-377">When postMessage is called, the [ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) set via this SetWebMessageReceivedEventHandler method will be invoked with the postMessage's object parameter converted to a JSON string.</span></span>

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

#### <span data-ttu-id="92122-378">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="92122-378">add_WebResourceRequested</span></span> 

<span data-ttu-id="92122-379">Ajoutez un gestionnaire d’événements pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="92122-379">Add an event handler for the WebResourceRequested event.</span></span>

> <span data-ttu-id="92122-380">[add_WebResourceRequested](#add_webresourcerequested)par le biais du[mot de passe](icorewebview2webresourcerequestedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="92122-380">public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](icorewebview2webresourcerequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="92122-381">Se déclenche lorsque WebView effectue une requête HTTP à un filtre d’URL et de contexte de ressources correspondant qui a été ajouté à l’aide de AddWebResourceRequestedFilter.</span><span class="sxs-lookup"><span data-stu-id="92122-381">Fires when the WebView is performing an HTTP request to a matching URL and resource context filter that was added with AddWebResourceRequestedFilter.</span></span> <span data-ttu-id="92122-382">Au moins un filtre doit être ajouté pour que l’événement se déclenche.</span><span class="sxs-lookup"><span data-stu-id="92122-382">At least one filter must be added for the event to fire.</span></span>

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

#### <span data-ttu-id="92122-383">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="92122-383">add_WindowCloseRequested</span></span> 

<span data-ttu-id="92122-384">Ajoutez un gestionnaire d’événements pour l’événement WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="92122-384">Add an event handler for the WindowCloseRequested event.</span></span>

> <span data-ttu-id="92122-385">[add_WindowCloseRequested](#add_windowcloserequested)par le biais du[mot de passe](icorewebview2windowcloserequestedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="92122-385">public HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](icorewebview2windowcloserequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="92122-386">Se déclenche lorsque le contenu à l’intérieur du WebView est requis pour fermer la fenêtre, par exemple, après l’appel de Window. Close.</span><span class="sxs-lookup"><span data-stu-id="92122-386">Fires when content inside the WebView requested to close the window, such as after window.close is called.</span></span> <span data-ttu-id="92122-387">L’application doit fermer la fenêtre WebView et la fenêtre de l’application associée si cela est pertinent pour l’application.</span><span class="sxs-lookup"><span data-stu-id="92122-387">The app should close the WebView and related app window if that makes sense to the app.</span></span>

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

#### <span data-ttu-id="92122-388">AddHostObjectToScript</span><span class="sxs-lookup"><span data-stu-id="92122-388">AddHostObjectToScript</span></span> 

<span data-ttu-id="92122-389">Ajoutez l’objet hôte fourni au script qui s’exécute sur le WebView avec le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="92122-389">Add the provided host object to script running in the WebView with the specified name.</span></span>

> <span data-ttu-id="92122-390">public HRESULT [AddHostObjectToScript](#addhostobjecttoscript)(LPCWSTR Name, variant \* Object)</span><span class="sxs-lookup"><span data-stu-id="92122-390">public HRESULT [AddHostObjectToScript](#addhostobjecttoscript)(LPCWSTR name, VARIANT \* object)</span></span>

<span data-ttu-id="92122-391">Les objets hôtes sont exposés en tant que proxy d’objet hôte via `window.chrome.webview.hostObjects.<name>` .</span><span class="sxs-lookup"><span data-stu-id="92122-391">Host objects are exposed as host object proxies via `window.chrome.webview.hostObjects.<name>`.</span></span> <span data-ttu-id="92122-392">Les proxies d’objet hôte sont promet et sont résolus en objet représentant l’objet hôte.</span><span class="sxs-lookup"><span data-stu-id="92122-392">Host object proxies are promises and will resolve to an object representing the host object.</span></span> <span data-ttu-id="92122-393">La promesse est refusée si l’application n’a pas ajouté d’objet portant le nom.</span><span class="sxs-lookup"><span data-stu-id="92122-393">The promise is rejected if the app has not added an object with the name.</span></span> <span data-ttu-id="92122-394">Lorsque le code JavaScript accède à une propriété ou une méthode de l’objet, une promesse est renvoyée, qui est résolue en fonction de la valeur renvoyée par l’hôte de la propriété ou de la méthode, ou rejetée en cas d’erreur, comme il n’y a pas de propriété ou de méthode sur l’objet ou les paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="92122-394">When JavaScript code access a property or method of the object, a promise is return, which will resolve to the value returned from the host for the property or method, or rejected in case of error such as there is no such property or method on the object or parameters are invalid.</span></span> <span data-ttu-id="92122-395">Par exemple, lorsque le code de l’application effectue les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="92122-395">For example, when the application code does the following:</span></span>

```
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddHostObjectToScript(L"host_object", &host);
```

<span data-ttu-id="92122-396">Le code JavaScript de l’affichage WebView sera en mesure d’accéder à appObject comme suit, puis d’accéder aux attributs et méthodes de appObject:</span><span class="sxs-lookup"><span data-stu-id="92122-396">JavaScript code in the WebView will be able to access appObject as following and then access attributes and methods of appObject:</span></span>

```
let app_object = await window.chrome.webview.hostObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

<span data-ttu-id="92122-397">Notez qu’en ce qui concerne les types simples, IDispatch et Array sont pris en charge, le type IUnknown, VT_DECIMAL ou VT_RECORD variant n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="92122-397">Note that while simple types, IDispatch and array are supported, generic IUnknown, VT_DECIMAL, or VT_RECORD variant is not supported.</span></span> <span data-ttu-id="92122-398">Les objets JavaScript distants comme les fonctions de rappel sont représentés sous la forme d’un VT_DISPATCH VARIANT avec l’objet qui implémente IDispatch.</span><span class="sxs-lookup"><span data-stu-id="92122-398">Remote JavaScript objects like callback functions are represented as an VT_DISPATCH VARIANT with the object implementing IDispatch.</span></span> <span data-ttu-id="92122-399">La méthode de rappel JavaScript doit être appelée à l’aide de DISPID_VALUE pour le DISPID.</span><span class="sxs-lookup"><span data-stu-id="92122-399">The JavaScript callback method may be invoked using DISPID_VALUE for the DISPID.</span></span> <span data-ttu-id="92122-400">Les tableaux imbriqués sont pris en charge jusqu’à une profondeur de 3.</span><span class="sxs-lookup"><span data-stu-id="92122-400">Nested arrays are supported up to a depth of 3.</span></span> <span data-ttu-id="92122-401">Les matrices de par types de référence ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="92122-401">Arrays of by reference types are not supported.</span></span> <span data-ttu-id="92122-402">VT_EMPTY et VT_NULL sont mappés dans JavaScript en tant que valeurs NULL.</span><span class="sxs-lookup"><span data-stu-id="92122-402">VT_EMPTY and VT_NULL are mapped into JavaScript as null.</span></span> <span data-ttu-id="92122-403">Dans JavaScript, les valeurs NULL et non définies sont mappées à VT_EMPTY.</span><span class="sxs-lookup"><span data-stu-id="92122-403">In JavaScript null and undefined are mapped to VT_EMPTY.</span></span>

<span data-ttu-id="92122-404">De plus, tous les objets hôtes sont exposés en tant que `window.chrome.webview.hostObjects.sync.<name>` .</span><span class="sxs-lookup"><span data-stu-id="92122-404">Additionally, all host objects are exposed as `window.chrome.webview.hostObjects.sync.<name>`.</span></span> <span data-ttu-id="92122-405">Ici, les objets hôtes sont exposés en tant que proxy d’objets hôtes synchrones.</span><span class="sxs-lookup"><span data-stu-id="92122-405">Here the host objects are exposed as synchronous host object proxies.</span></span> <span data-ttu-id="92122-406">Celles-ci ne sont pas promesse et les appels de fonctions ou d’accès aux propriétés empêchent de manière synchrone l’exécution d’un script en attente de communication croisée pour que le code hôte s’exécute.</span><span class="sxs-lookup"><span data-stu-id="92122-406">These are not promises and calls to functions or property access synchronously block running script waiting to communicate cross process for the host code to run.</span></span> <span data-ttu-id="92122-407">En conséquence, cela peut entraîner des problèmes de fiabilité et nous vous conseillons d’utiliser l’API asynchrone basée sur la promesse `window.chrome.webview.hostObjects.<name>` décrite ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="92122-407">Accordingly this can result in reliability issues and it is recommended that you use the promise based asynchronous `window.chrome.webview.hostObjects.<name>` API described above.</span></span>

<span data-ttu-id="92122-408">Les proxies d’objet hôte synchrone et les proxys d’objets hôtes asynchrones peuvent à la fois proxy le même objet hôte.</span><span class="sxs-lookup"><span data-stu-id="92122-408">Synchronous host object proxies and asynchronous host object proxies can both proxy the same host object.</span></span> <span data-ttu-id="92122-409">Les modifications distantes apportées par un proxy seront reflétées dans tout autre proxy de ce même objet hôte, qu’il s’agisse de proxys et synchrones ou asynchrones.</span><span class="sxs-lookup"><span data-stu-id="92122-409">Remote changes made by one proxy will be reflected in any other proxy of that same host object whether the other proxies and synchronous or asynchronous.</span></span>

<span data-ttu-id="92122-410">Si JavaScript est bloqué lors d’un appel asynchrone au code natif, ce code natif ne peut pas rappeler JavaScript.</span><span class="sxs-lookup"><span data-stu-id="92122-410">While JavaScript is blocked on a synchronous call to native code, that native code is unable to call back to JavaScript.</span></span> <span data-ttu-id="92122-411">Les tentatives d’une telle opération échoueront avec HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).</span><span class="sxs-lookup"><span data-stu-id="92122-411">Attempts to do so will fail with HRESULT_FROM_WIN32(ERROR_POSSIBLE_DEADLOCK).</span></span>

<span data-ttu-id="92122-412">Les proxies d’objets hôtes sont des objets proxy JavaScript qui interceptent l’ensemble des appels de propriété Get, de jeu de propriétés et de méthode.</span><span class="sxs-lookup"><span data-stu-id="92122-412">Host object proxies are JavaScript Proxy objects that intercept all property get, property set, and method invocations.</span></span> <span data-ttu-id="92122-413">Les propriétés ou méthodes qui font partie du prototype de fonction ou d’objet sont exécutées localement.</span><span class="sxs-lookup"><span data-stu-id="92122-413">Properties or methods that are a part of the Function or Object prototype are run locally.</span></span> <span data-ttu-id="92122-414">De plus, toute propriété ou méthode du tableau `chrome.webview.hostObjects.options.forceLocalProperties` sera également exécutée localement.</span><span class="sxs-lookup"><span data-stu-id="92122-414">Additionally any property or method in the array `chrome.webview.hostObjects.options.forceLocalProperties` will also be run locally.</span></span> <span data-ttu-id="92122-415">Par exemple, vous pouvez inclure des méthodes facultatives ayant une signification dans JavaScript comme `toJSON` et `Symbol.toPrimitive` .</span><span class="sxs-lookup"><span data-stu-id="92122-415">This defaults to including optional methods that have meaning in JavaScript like `toJSON` and `Symbol.toPrimitive`.</span></span> <span data-ttu-id="92122-416">Vous pouvez en ajouter d’autres à ce tableau selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="92122-416">You can add more to this array as required.</span></span>

<span data-ttu-id="92122-417">Il existe une méthode `chrome.webview.hostObjects.cleanupSome` qui consiste à utiliser au mieux le nettoyage de la mémoire proxy d’objet hôte.</span><span class="sxs-lookup"><span data-stu-id="92122-417">There's a method `chrome.webview.hostObjects.cleanupSome` that will best effort garbage collect host object proxies.</span></span>

<span data-ttu-id="92122-418">Les proxys d’objets hôtes possèdent également les méthodes suivantes qui s’exécutent en local:</span><span class="sxs-lookup"><span data-stu-id="92122-418">Host object proxies additionally have the following methods which run locally:</span></span>

* <span data-ttu-id="92122-419">applyHostFunction, getHostProperty, setHostProperty: effectue un appel de méthode, Get de propriété ou jeu de propriétés sur l’objet hôte.</span><span class="sxs-lookup"><span data-stu-id="92122-419">applyHostFunction, getHostProperty, setHostProperty: Perform a method invocation, property get, or property set on the host object.</span></span> <span data-ttu-id="92122-420">Vous pouvez utiliser ces éléments pour forcer explicitement une méthode ou une propriété à s’exécuter à distance en cas de conflit entre une méthode locale ou une propriété.</span><span class="sxs-lookup"><span data-stu-id="92122-420">You can use these to explicitly force a method or property to run remotely if there is a conflicting local method or property.</span></span> <span data-ttu-id="92122-421">Par exemple, `proxy.toString()` exécute la méthode ToString locale sur l’objet proxy.</span><span class="sxs-lookup"><span data-stu-id="92122-421">For instance, `proxy.toString()` will run the local toString method on the proxy object.</span></span> <span data-ttu-id="92122-422">Mais `proxy.applyHostFunction('toString')` s’exécute `toString` plutôt sur l’objet proxy de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="92122-422">But `proxy.applyHostFunction('toString')` runs `toString` on the host proxied object instead.</span></span>

* <span data-ttu-id="92122-423">getLocalProperty, setLocalProperty: exécuter une propriété Get ou Property Set localement.</span><span class="sxs-lookup"><span data-stu-id="92122-423">getLocalProperty, setLocalProperty: Perform property get, or property set locally.</span></span> <span data-ttu-id="92122-424">Vous pouvez utiliser ces méthodes pour forcer l’affichage ou la définition d’une propriété sur le proxy d’objet hôte lui-même plutôt que sur l’objet hôte qu’elle représente.</span><span class="sxs-lookup"><span data-stu-id="92122-424">You can use these methods to force getting or setting a property on the host object proxy itself rather than on the host object it represents.</span></span> <span data-ttu-id="92122-425">Par exemple, obtiendrez `proxy.unknownProperty` la propriété nommée `unknownProperty` de l’objet proxy de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="92122-425">For instance, `proxy.unknownProperty` will get the property named `unknownProperty` from the host proxied object.</span></span> <span data-ttu-id="92122-426">Toutefois `proxy.getLocalProperty('unknownProperty')` , vous obtiendrez la valeur de la propriété `unknownProperty` sur l’objet proxy lui-même.</span><span class="sxs-lookup"><span data-stu-id="92122-426">But `proxy.getLocalProperty('unknownProperty')` will get the value of the property `unknownProperty` on the proxy object itself.</span></span>

* <span data-ttu-id="92122-427">synchronisation: les proxys d’objets hôtes asynchrones exposent une méthode de synchronisation qui renvoie une promesse de proxy d’objet hôte synchrone pour le même objet hôte.</span><span class="sxs-lookup"><span data-stu-id="92122-427">sync: Asynchronous host object proxies expose a sync method which returns a promise for a synchronous host object proxy for the same host object.</span></span> <span data-ttu-id="92122-428">Par exemple, `chrome.webview.hostObjects.sample.methodCall()` retourne un proxy d’objet hôte asynchrone.</span><span class="sxs-lookup"><span data-stu-id="92122-428">For example, `chrome.webview.hostObjects.sample.methodCall()` returns an asynchronous host object proxy.</span></span> <span data-ttu-id="92122-429">Vous pouvez utiliser la `sync` méthode pour obtenir un proxy d’objet hôte synchrone à la place:</span><span class="sxs-lookup"><span data-stu-id="92122-429">You can use the `sync` method to obtain a synchronous host object proxy instead:</span></span> `const syncProxy = await chrome.webview.hostObjects.sample.methodCall().sync()`

* <span data-ttu-id="92122-430">Async: les proxys d’objets d’hôte synchrones présentent une méthode Async qui bloque et retourne un proxy d’objet hôte asynchrone pour le même objet hôte.</span><span class="sxs-lookup"><span data-stu-id="92122-430">async: Synchronous host object proxies expose an async method which blocks and returns an asynchronous host object proxy for the same host object.</span></span> <span data-ttu-id="92122-431">Par exemple, `chrome.webview.hostObjects.sync.sample.methodCall()` retourne un proxy d’objet hôte synchrone.</span><span class="sxs-lookup"><span data-stu-id="92122-431">For example, `chrome.webview.hostObjects.sync.sample.methodCall()` returns a synchronous host object proxy.</span></span> <span data-ttu-id="92122-432">Appel de la `async` méthode sur ce bloc, puis retour d’un proxy d’objet hôte asynchrone pour le même objet hôte:</span><span class="sxs-lookup"><span data-stu-id="92122-432">Calling the `async` method on this blocks and then returns an asynchronous host object proxy for the same host object:</span></span> `const asyncProxy = chrome.webview.hostObjects.sync.sample.methodCall().async()`

* <span data-ttu-id="92122-433">ensuite: les proxies d’objet hôte asynchrone possèdent une méthode Then.</span><span class="sxs-lookup"><span data-stu-id="92122-433">then: Asynchronous host object proxies have a then method.</span></span> <span data-ttu-id="92122-434">Cela leur permet d’être await.</span><span class="sxs-lookup"><span data-stu-id="92122-434">This allows them to be awaitable.</span></span> `then` <span data-ttu-id="92122-435">renverra une promesse qui est résolue en une représentation de l’objet hôte.</span><span class="sxs-lookup"><span data-stu-id="92122-435">will return a promise that resolves with a representation of the host object.</span></span> <span data-ttu-id="92122-436">Si le proxy représente un littéral JavaScript, une copie de celui-ci est renvoyée localement.</span><span class="sxs-lookup"><span data-stu-id="92122-436">If the proxy represents a JavaScript literal then a copy of that is returned locally.</span></span> <span data-ttu-id="92122-437">Si le proxy représente une fonction, un proxy non-await est retourné.</span><span class="sxs-lookup"><span data-stu-id="92122-437">If the proxy represents a function then a non-awaitable proxy is returned.</span></span> <span data-ttu-id="92122-438">Si le proxy représente un objet JavaScript avec une combinaison de propriétés littérales et de propriétés de fonctions, une copie de l’objet est renvoyée avec des propriétés en tant que proxy d’objet hôte.</span><span class="sxs-lookup"><span data-stu-id="92122-438">If the proxy represents a JavaScript object with a mix of literal properties and function properties, then the a copy of the object is returned with some properties as host object proxies.</span></span>

<span data-ttu-id="92122-439">Tous les autres appels de propriété et de méthode (autres que les méthodes de proxy d’objet distant, la liste forceLocalProperties et les propriétés des prototypes de fonction et d’objet) s’exécutent à distance.</span><span class="sxs-lookup"><span data-stu-id="92122-439">All other property and method invocations (other than the above Remote object proxy methods, forceLocalProperties list, and properties on Function and Object prototypes) are run remotely.</span></span> <span data-ttu-id="92122-440">Les proxys d’objets hôtes asynchrones retournent une promesse qui représente la complétion asynchrone d’appeler la méthode à distance ou d’obtenir la propriété.</span><span class="sxs-lookup"><span data-stu-id="92122-440">Asynchronous host object proxies return a promise representing asynchronous completion of remotely invoking the method, or getting the property.</span></span> <span data-ttu-id="92122-441">La promesse se résout une fois les opérations distantes terminées et la promesse de la valeur de l’opération.</span><span class="sxs-lookup"><span data-stu-id="92122-441">The promise resolves after the remote operations complete and the promises resolve to the resulting value of the operation.</span></span> <span data-ttu-id="92122-442">Les proxys d’objets hôtes synchrones fonctionnent de la même façon, mais bloquent l’exécution JavaScript et attendez la fin de l’opération à distance.</span><span class="sxs-lookup"><span data-stu-id="92122-442">Synchronous host object proxies work similarly but block JavaScript execution and wait for the remote operation to complete.</span></span>

<span data-ttu-id="92122-443">La définition d’une propriété sur un proxy d’objet hôte asynchrone fonctionne légèrement différemment.</span><span class="sxs-lookup"><span data-stu-id="92122-443">Setting a property on an asynchronous host object proxy works slightly differently.</span></span> <span data-ttu-id="92122-444">Le jeu renvoie immédiatement et la valeur de retour est la valeur qui sera définie.</span><span class="sxs-lookup"><span data-stu-id="92122-444">The set returns immediately and the return value is the value that will be set.</span></span> <span data-ttu-id="92122-445">Il s’agit d’une condition requise de l’objet proxy JavaScript.</span><span class="sxs-lookup"><span data-stu-id="92122-445">This is a requirement of the JavaScript Proxy object.</span></span> <span data-ttu-id="92122-446">Si vous avez besoin d’attendre que le jeu de propriétés soit terminé, utilisez la méthode setHostProperty qui renvoie une promesse comme décrit ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="92122-446">If you need to asynchronously wait for the property set to complete, use the setHostProperty method which returns a promise as described above.</span></span> <span data-ttu-id="92122-447">La propriété du jeu de propriétés d’objet synchrone se bloque de manière synchrone tant que la propriété est définie.</span><span class="sxs-lookup"><span data-stu-id="92122-447">Synchronous object property set property synchronously blocks until the property is set.</span></span>

<span data-ttu-id="92122-448">Par exemple, supposons que vous disposiez d’un objet COM avec l’interface suivante.</span><span class="sxs-lookup"><span data-stu-id="92122-448">For example, suppose you have a COM object with the following interface</span></span>

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
 <span data-ttu-id="92122-449">Nous pouvons ajouter une instance de cette interface dans notre JavaScript avec `AddHostObjectToScript` .</span><span class="sxs-lookup"><span data-stu-id="92122-449">We can add an instance of this interface into our JavaScript with `AddHostObjectToScript`.</span></span> <span data-ttu-id="92122-450">Dans le cas présent, vous nommerez ce message `sample` :</span><span class="sxs-lookup"><span data-stu-id="92122-450">In this case we name it `sample`:</span></span>

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
 <span data-ttu-id="92122-451">Ensuite, dans le document HTML, vous pouvez utiliser cet objet COM via `chrome.webview.hostObjects.sample` :</span><span class="sxs-lookup"><span data-stu-id="92122-451">Then in the HTML document we can use this COM object via `chrome.webview.hostObjects.sample`:</span></span>

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
        // If you need to set the property and wait for the property to change value, use the setRemote function.
        chrome.webview.hostObjects.sample.property = propertyValue;
        document.getElementById("setPropertyAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertyExplicitAsyncButton").addEventListener("click", async () => {
        const propertyValue = document.getElementById("setPropertyExplicitAsyncInput").value;
        // If you care about waiting until the property has actually changed value use the setRemote function.
        await chrome.webview.hostObjects.sample.setRemote("property", propertyValue);
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

#### <span data-ttu-id="92122-452">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="92122-452">AddScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="92122-453">Ajoutez le code JavaScript fourni à une liste de scripts qui doivent être exécutés après la création de l’objet global, mais avant l’analyse du document HTML et avant l’exécution de tout autre script fourni par le document HTML.</span><span class="sxs-lookup"><span data-stu-id="92122-453">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>

> <span data-ttu-id="92122-454">public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR JavaScript, gestionnaire [ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md) \*)</span><span class="sxs-lookup"><span data-stu-id="92122-454">public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript, [ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="92122-455">Le script injecté s’applique à tous les futurs documents de niveau supérieur et navigation de Frame enfant jusqu’à sa suppression avec RemoveScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="92122-455">The injected script will apply to all future top level document and child frame navigations until removed with RemoveScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="92122-456">Cette opération est appliquée de manière asynchrone et vous devez attendre que le gestionnaire d’achèvement s’exécute avant de vérifier que le script est prêt à être exécuté sur de futurs navigations.</span><span class="sxs-lookup"><span data-stu-id="92122-456">This is applied asynchronously and you must wait for the completion handler to run before you can be sure that the script is ready to execute on future navigations.</span></span>

<span data-ttu-id="92122-457">Notez que si un document HTML comporte un sandbox d’un type quelconque via les propriétés [sandbox](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe#attr-sandbox) ou l' [en-tête HTTP Content-Security-Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy) , ce dernier affectera l’exécution du script.</span><span class="sxs-lookup"><span data-stu-id="92122-457">Note that if an HTML document has sandboxing of some kind via [sandbox](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe#attr-sandbox) properties or the [Content-Security-Policy HTTP header](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy) this will affect the script run here.</span></span> <span data-ttu-id="92122-458">Par exemple, si le mot clé «allow-modaux» n’est pas défini, les appels à la `alert` fonction seront ignorés.</span><span class="sxs-lookup"><span data-stu-id="92122-458">So, for example, if the 'allow-modals' keyword is not set then calls to the `alert` function will be ignored.</span></span>

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

#### <span data-ttu-id="92122-459">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="92122-459">AddWebResourceRequestedFilter</span></span> 

<span data-ttu-id="92122-460">Ajoute un URI et un filtre de contexte de ressources à l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="92122-460">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>

> <span data-ttu-id="92122-461">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) constante resourceContext)</span><span class="sxs-lookup"><span data-stu-id="92122-461">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="92122-462">Le paramètre URI peut être une chaîne de caractères génériques (' ': zéro ou plusieurs; '? ': exactement 1).</span><span class="sxs-lookup"><span data-stu-id="92122-462">URI parameter can be a wildcard string ('': zero or more, '?': exactly one).</span></span> <span data-ttu-id="92122-463">nullptr est l’équivalent de L "".</span><span class="sxs-lookup"><span data-stu-id="92122-463">nullptr is equivalent to L"".</span></span> <span data-ttu-id="92122-464">Pour plus d’détails sur les filtres de contexte de ressources, voir COREWEBVIEW2_WEB_RESOURCE_CONTEXT Enum.</span><span class="sxs-lookup"><span data-stu-id="92122-464">See COREWEBVIEW2_WEB_RESOURCE_CONTEXT enum for description of resource context filters.</span></span>

#### <span data-ttu-id="92122-465">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="92122-465">CallDevToolsProtocolMethod</span></span> 

<span data-ttu-id="92122-466">Appelez une méthode DevToolsProtocol asynchrone.</span><span class="sxs-lookup"><span data-stu-id="92122-466">Call an asynchronous DevToolsProtocol method.</span></span>

> <span data-ttu-id="92122-467">public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR METHODNAME, LPCWSTR parametersAsJson, gestionnaire [ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](icorewebview2calldevtoolsprotocolmethodcompletedhandler.md) \*)</span><span class="sxs-lookup"><span data-stu-id="92122-467">public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR methodName, LPCWSTR parametersAsJson, [ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](icorewebview2calldevtoolsprotocolmethodcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="92122-468">Voir la [visionneuse de protocoles devtools](https://aka.ms/DevToolsProtocolDocs) pour obtenir une liste et une description des méthodes disponibles.</span><span class="sxs-lookup"><span data-stu-id="92122-468">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list and description of available methods.</span></span> <span data-ttu-id="92122-469">Le paramètre methodName est le nom complet de la méthode au format `{domain}.{method}` .</span><span class="sxs-lookup"><span data-stu-id="92122-469">The methodName parameter is the full name of the method in the format `{domain}.{method}`.</span></span> <span data-ttu-id="92122-470">Le paramètre parametersAsJson est une chaîne au format JSON contenant les paramètres de la méthode correspondante.</span><span class="sxs-lookup"><span data-stu-id="92122-470">The parametersAsJson parameter is a JSON formatted string containing the parameters for the corresponding method.</span></span> <span data-ttu-id="92122-471">La méthode Invoke du gestionnaire est appelée lorsque la méthode est terminée de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="92122-471">The handler's Invoke method will be called when the method asynchronously completes.</span></span> <span data-ttu-id="92122-472">Invoke sera appelé avec l’objet de retour de la méthode sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="92122-472">Invoke will be called with the method's return object as a JSON string.</span></span>

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

#### <span data-ttu-id="92122-473">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="92122-473">CapturePreview</span></span> 

<span data-ttu-id="92122-474">Capturez une image de l’affichage du WebView.</span><span class="sxs-lookup"><span data-stu-id="92122-474">Capture an image of what WebView is displaying.</span></span>

> <span data-ttu-id="92122-475">public HRESULT [CapturePreview](#capturepreview)([COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) ImageFormat, IStream \* ImageStream, gestionnaire [ICoreWebView2CapturePreviewCompletedHandler](icorewebview2capturepreviewcompletedhandler.md) \*)</span><span class="sxs-lookup"><span data-stu-id="92122-475">public HRESULT [CapturePreview](#capturepreview)([COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) imageFormat, IStream \* imageStream, [ICoreWebView2CapturePreviewCompletedHandler](icorewebview2capturepreviewcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="92122-476">Spécifiez le format de l’image avec le paramètre imageFormat.</span><span class="sxs-lookup"><span data-stu-id="92122-476">Specify the format of the image with the imageFormat parameter.</span></span> <span data-ttu-id="92122-477">Les données binaires d’image obtenues sont écrites dans le paramètre imageStream fourni.</span><span class="sxs-lookup"><span data-stu-id="92122-477">The resulting image binary data is written to the provided imageStream parameter.</span></span> <span data-ttu-id="92122-478">Lorsque CapturePreview finit d’écrire dans le flux, la méthode Invoke du paramètre de gestionnaire fourni est appelée.</span><span class="sxs-lookup"><span data-stu-id="92122-478">When CapturePreview finishes writing to the stream, the Invoke method on the provided handler parameter is called.</span></span>

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

#### <span data-ttu-id="92122-479">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="92122-479">ExecuteScript</span></span> 

<span data-ttu-id="92122-480">Exécutez le code JavaScript du paramètre JavaScript du document de niveau supérieur actuel affiché dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="92122-480">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="92122-481">public HRESULT [ExecuteScript](#executescript)(LPCWSTR JavaScript, gestionnaire [ICoreWebView2ExecuteScriptCompletedHandler](icorewebview2executescriptcompletedhandler.md) \*)</span><span class="sxs-lookup"><span data-stu-id="92122-481">public HRESULT [ExecuteScript](#executescript)(LPCWSTR javaScript, [ICoreWebView2ExecuteScriptCompletedHandler](icorewebview2executescriptcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="92122-482">Cela s’exécute de manière asynchrone et, si un gestionnaire est fourni dans le paramètre ExecuteScriptCompletedHandler, sa méthode Invoke est appelée avec le résultat de l’évaluation du JavaScript fourni.</span><span class="sxs-lookup"><span data-stu-id="92122-482">This will execute asynchronously and when complete, if a handler is provided in the ExecuteScriptCompletedHandler parameter, its Invoke method will be called with the result of evaluating the provided JavaScript.</span></span> <span data-ttu-id="92122-483">La valeur de résultat est une chaîne codée au format JSON.</span><span class="sxs-lookup"><span data-stu-id="92122-483">The result value is a JSON encoded string.</span></span> <span data-ttu-id="92122-484">Si le résultat n’est pas défini, contient un cycle de référence ou ne peut pas être encodé dans JSON, la valeur null JSON sera renvoyée comme chaîne «NULL».</span><span class="sxs-lookup"><span data-stu-id="92122-484">If the result is undefined, contains a reference cycle, or otherwise cannot be encoded into JSON, the JSON null value will be returned as the string 'null'.</span></span> <span data-ttu-id="92122-485">Notez qu’une fonction qui ne contient aucune valeur de retour explicite renvoie une valeur non définie.</span><span class="sxs-lookup"><span data-stu-id="92122-485">Note that a function that has no explicit return value returns undefined.</span></span> <span data-ttu-id="92122-486">Si le script exécuté lève une exception non gérée, le résultat est également «null».</span><span class="sxs-lookup"><span data-stu-id="92122-486">If the executed script throws an unhandled exception, then the result is also 'null'.</span></span> <span data-ttu-id="92122-487">Cette méthode est appliquée de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="92122-487">This method is applied asynchronously.</span></span> <span data-ttu-id="92122-488">Si la méthode est appelée après l’événement NavigationStarting pendant une navigation, le script est exécuté dans le nouveau document lors du chargement de celui-ci, au cours du démarrage de ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="92122-488">If the method is called after NavigationStarting event during a navigation, the script will be executed in the new document when loading it, around the time ContentLoading is fired.</span></span> <span data-ttu-id="92122-489">ExecuteScript fonctionne même si IsScriptEnabled est défini sur FALSe.</span><span class="sxs-lookup"><span data-stu-id="92122-489">ExecuteScript will work even if IsScriptEnabled is set to FALSE.</span></span>

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

#### <span data-ttu-id="92122-490">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="92122-490">get_BrowserProcessId</span></span> 

<span data-ttu-id="92122-491">ID de processus du processus de navigation qui héberge le WebView.</span><span class="sxs-lookup"><span data-stu-id="92122-491">The process id of the browser process that hosts the WebView.</span></span>

> <span data-ttu-id="92122-492">valeur publique HRESULT [get_BrowserProcessId](#get_browserprocessid)(valeur UInt32 \*)</span><span class="sxs-lookup"><span data-stu-id="92122-492">public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* value)</span></span>

#### <span data-ttu-id="92122-493">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="92122-493">get_CanGoBack</span></span> 

<span data-ttu-id="92122-494">Renvoie vrai si le WebView peut accéder à une page précédente de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="92122-494">Returns true if the webview can navigate to a previous page in the navigation history.</span></span>

> <span data-ttu-id="92122-495">valeur publique HRESULT [get_CanGoBack](#get_cangoback)(bool \* CanGoBack)</span><span class="sxs-lookup"><span data-stu-id="92122-495">public HRESULT [get_CanGoBack](#get_cangoback)(BOOL \* canGoBack)</span></span>

<span data-ttu-id="92122-496">L’événement HistoryChanged se déclenche si CanGoBack change value.</span><span class="sxs-lookup"><span data-stu-id="92122-496">The HistoryChanged event will fire if CanGoBack changes value.</span></span>

#### <span data-ttu-id="92122-497">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="92122-497">get_CanGoForward</span></span> 

<span data-ttu-id="92122-498">Cette fonction renvoie la valeur vrai si le WebView peut accéder à une page suivante de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="92122-498">Returns true if the webview can navigate to a next page in the navigation history.</span></span>

> <span data-ttu-id="92122-499">valeur publique HRESULT [get_CanGoForward](#get_cangoforward)(bool \* CanGoForward)</span><span class="sxs-lookup"><span data-stu-id="92122-499">public HRESULT [get_CanGoForward](#get_cangoforward)(BOOL \* canGoForward)</span></span>

<span data-ttu-id="92122-500">L’événement HistoryChanged se déclenche si CanGoForward change value.</span><span class="sxs-lookup"><span data-stu-id="92122-500">The HistoryChanged event will fire if CanGoForward changes value.</span></span>

#### <span data-ttu-id="92122-501">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="92122-501">get_ContainsFullScreenElement</span></span> 

<span data-ttu-id="92122-502">Indique si le WebView contient un élément HTML fullscreen.</span><span class="sxs-lookup"><span data-stu-id="92122-502">Indicates if the WebView contains a fullscreen HTML element.</span></span>

> <span data-ttu-id="92122-503">valeur publique HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(bool \* ContainsFullScreenElement)</span><span class="sxs-lookup"><span data-stu-id="92122-503">public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(BOOL \* containsFullScreenElement)</span></span>

#### <span data-ttu-id="92122-504">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="92122-504">get_DocumentTitle</span></span> 

<span data-ttu-id="92122-505">Titre du document de niveau supérieur actuel.</span><span class="sxs-lookup"><span data-stu-id="92122-505">The title for the current top level document.</span></span>

> <span data-ttu-id="92122-506">valeur publique HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span><span class="sxs-lookup"><span data-stu-id="92122-506">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="92122-507">Si le document ne comporte pas de titre explicite ou s’il est vide, une valeur par défaut qui peut ou ne correspond pas à l’URI du document sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="92122-507">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

#### <span data-ttu-id="92122-508">get_Settings</span><span class="sxs-lookup"><span data-stu-id="92122-508">get_Settings</span></span> 

<span data-ttu-id="92122-509">L’objet [ICoreWebView2Settings](icorewebview2settings.md) contient différents paramètres modifiables pour le WebView en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="92122-509">The [ICoreWebView2Settings](icorewebview2settings.md) object contains various modifiable settings for the running WebView.</span></span>

> <span data-ttu-id="92122-510">valeurs publiques HRESULT [get_Settings](#get_settings)([ICoreWebView2Settings](icorewebview2settings.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="92122-510">public HRESULT [get_Settings](#get_settings)([ICoreWebView2Settings](icorewebview2settings.md) \*\* settings)</span></span>

#### <span data-ttu-id="92122-511">get_Source</span><span class="sxs-lookup"><span data-stu-id="92122-511">get_Source</span></span> 

<span data-ttu-id="92122-512">URI du document de niveau supérieur actuel.</span><span class="sxs-lookup"><span data-stu-id="92122-512">The URI of the current top level document.</span></span>

> <span data-ttu-id="92122-513">valeur publique HRESULT [get_Source](#get_source)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="92122-513">public HRESULT [get_Source](#get_source)(LPWSTR \* uri)</span></span>

<span data-ttu-id="92122-514">Cette valeur peut éventuellement changer dans le cadre du déclenchement de l’événement SourceChanged dans certains cas, par exemple pour accéder à un site ou à un fragment de navigation différent.</span><span class="sxs-lookup"><span data-stu-id="92122-514">This value potentially changes as a part of the SourceChanged event firing for some cases such as navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="92122-515">Il restera identique pour les autres types de navigation, tels que les recharges de page ou l’historique. pushState avec la même URL que la page active.</span><span class="sxs-lookup"><span data-stu-id="92122-515">It will remain the same for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span>

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
                SetWindowText(m_toolbar->addressBarWindow, uri.get());

                return S_OK;
            })
            .Get(),
        &m_sourceChangedToken));
```

#### <span data-ttu-id="92122-516">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="92122-516">GetDevToolsProtocolEventReceiver</span></span> 

<span data-ttu-id="92122-517">Obtenez un destinataire d’événement de protocole DevTools qui vous permet de vous abonner à un événement de protocole DevTools.</span><span class="sxs-lookup"><span data-stu-id="92122-517">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>

> <span data-ttu-id="92122-518">public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR NomÉvénement; [ICoreWebView2DevToolsProtocolEventReceiver](icorewebview2devtoolsprotocoleventreceiver.md) \* \* Receiver)</span><span class="sxs-lookup"><span data-stu-id="92122-518">public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR eventName, [ICoreWebView2DevToolsProtocolEventReceiver](icorewebview2devtoolsprotocoleventreceiver.md) \*\* receiver)</span></span>

<span data-ttu-id="92122-519">Le paramètre eventName est le nom complet de l’événement au format `{domain}.{event}` .</span><span class="sxs-lookup"><span data-stu-id="92122-519">The eventName parameter is the full name of the event in the format `{domain}.{event}`.</span></span> <span data-ttu-id="92122-520">Voir la [visionneuse de protocoles devtools](https://aka.ms/DevToolsProtocolDocs) pour obtenir une liste des événements de protocole devtools et des arguments d’événement.</span><span class="sxs-lookup"><span data-stu-id="92122-520">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list of DevTools Protocol events description, and event args.</span></span>

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

#### <span data-ttu-id="92122-521">GoBack</span><span class="sxs-lookup"><span data-stu-id="92122-521">GoBack</span></span> 

<span data-ttu-id="92122-522">Permet d’accéder à la page précédente de l’historique de navigation via le WebView.</span><span class="sxs-lookup"><span data-stu-id="92122-522">Navigates the WebView to the previous page in the navigation history.</span></span>

> <span data-ttu-id="92122-523">public HRESULT [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="92122-523">public HRESULT [GoBack](#goback)()</span></span>

#### <span data-ttu-id="92122-524">GoForward</span><span class="sxs-lookup"><span data-stu-id="92122-524">GoForward</span></span> 

<span data-ttu-id="92122-525">Navigue vers la page suivante de l’historique de navigation du WebView.</span><span class="sxs-lookup"><span data-stu-id="92122-525">Navigates the WebView to the next page in the navigation history.</span></span>

> <span data-ttu-id="92122-526">valeur publique HRESULT [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="92122-526">public HRESULT [GoForward](#goforward)()</span></span>

#### <span data-ttu-id="92122-527">Rechercher</span><span class="sxs-lookup"><span data-stu-id="92122-527">Navigate</span></span> 

<span data-ttu-id="92122-528">Entraîner une navigation du document de niveau supérieur sur l’URI spécifié.</span><span class="sxs-lookup"><span data-stu-id="92122-528">Cause a navigation of the top level document to the specified URI.</span></span>

> <span data-ttu-id="92122-529">public HRESULT [Navigate](#navigate)(Uri LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="92122-529">public HRESULT [Navigate](#navigate)(LPCWSTR uri)</span></span>

<span data-ttu-id="92122-530">Pour plus d’informations, voir événements de navigation.</span><span class="sxs-lookup"><span data-stu-id="92122-530">See the navigation events for more information.</span></span> <span data-ttu-id="92122-531">Notez que cela démarre une navigation et que l’événement NavigationStarting correspondant est déclenché après la fin de l’appel.</span><span class="sxs-lookup"><span data-stu-id="92122-531">Note that this starts a navigation and the corresponding NavigationStarting event will fire sometime after this Navigate call completes.</span></span>

```cpp
void ControlComponent::NavigateToAddressBar()
{
    int length = GetWindowTextLength(m_toolbar->addressBarWindow);
    std::wstring uri(length, 0);
    PWSTR buffer = const_cast<PWSTR>(uri.data());
    GetWindowText(m_toolbar->addressBarWindow, buffer, length + 1);

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

#### <span data-ttu-id="92122-532">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="92122-532">NavigateToString</span></span> 

<span data-ttu-id="92122-533">Lance une navigation vers htmlContent en tant que code HTML source d’un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="92122-533">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="92122-534">public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span><span class="sxs-lookup"><span data-stu-id="92122-534">public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span></span>

<span data-ttu-id="92122-535">Le paramètre htmlContent ne doit pas comporter plus de 2 Mo de caractères.</span><span class="sxs-lookup"><span data-stu-id="92122-535">The htmlContent parameter may not be larger than 2 MB of characters.</span></span> <span data-ttu-id="92122-536">L’origine de la nouvelle page va être vide.</span><span class="sxs-lookup"><span data-stu-id="92122-536">The origin of the new page will be about:blank.</span></span>

```cpp
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
```

#### <span data-ttu-id="92122-537">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="92122-537">OpenDevToolsWindow</span></span> 

<span data-ttu-id="92122-538">Ouvre la fenêtre DevTools pour le document actif dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="92122-538">Opens the DevTools window for the current document in the WebView.</span></span>

> <span data-ttu-id="92122-539">public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span><span class="sxs-lookup"><span data-stu-id="92122-539">public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span></span>

<span data-ttu-id="92122-540">Ne peut pas être appelé lorsque la fenêtre DevTools est déjà ouverte</span><span class="sxs-lookup"><span data-stu-id="92122-540">Does nothing if called when the DevTools window is already open</span></span>

#### <span data-ttu-id="92122-541">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="92122-541">PostWebMessageAsJson</span></span> 

<span data-ttu-id="92122-542">Publier le WebMessage spécifié sur le document de niveau supérieur dans ce WebView.</span><span class="sxs-lookup"><span data-stu-id="92122-542">Post the specified webMessage to the top level document in this WebView.</span></span>

> <span data-ttu-id="92122-543">public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="92122-543">public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span></span>

<span data-ttu-id="92122-544">Le document de niveau supérieur de la fenêtre du document. chrome. WebView est déclenché.</span><span class="sxs-lookup"><span data-stu-id="92122-544">The top level document's window.chrome.webview's message event fires.</span></span> <span data-ttu-id="92122-545">JavaScript dans ce document est susceptible de s’abonner à l’événement et de s’en désabonner via la commande suivante:</span><span class="sxs-lookup"><span data-stu-id="92122-545">JavaScript in that document may subscribe and unsubscribe to the event via the following:</span></span>

```
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

<span data-ttu-id="92122-546">Les arguments d’événement sont une instance de `MessageEvent` .</span><span class="sxs-lookup"><span data-stu-id="92122-546">The event args is an instance of `MessageEvent`.</span></span> <span data-ttu-id="92122-547">Le paramètre ICoreWebView2Settings:: IsWebMessageEnabled doit avoir la valeur true, ou cette méthode échoue avec E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="92122-547">The ICoreWebView2Settings::IsWebMessageEnabled setting must be true or this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="92122-548">La propriété Data du arg est le paramètre de chaîne WebMessage électronique analysé comme chaîne JSON dans un objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="92122-548">The event arg's data property is the webMessage string parameter parsed as a JSON string into a JavaScript object.</span></span> <span data-ttu-id="92122-549">La propriété source de l’objet Event est une référence à l' `window.chrome.webview` objet.</span><span class="sxs-lookup"><span data-stu-id="92122-549">The event arg's source property is a reference to the `window.chrome.webview` object.</span></span> <span data-ttu-id="92122-550">Pour plus d’informations sur l’envoi de messages à partir du document HTML du WebView vers l’hôte, voir SetWebMessageReceivedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="92122-550">See SetWebMessageReceivedEventHandler for information on sending messages from the HTML document in the webview to the host.</span></span> <span data-ttu-id="92122-551">Ce message est envoyé de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="92122-551">This message is sent asynchronously.</span></span> <span data-ttu-id="92122-552">Si une navigation se produit avant que le message ne soit publié sur la page, le message ne sera pas envoyé.</span><span class="sxs-lookup"><span data-stu-id="92122-552">If a navigation occurs before the message is posted to the page, then the message will not be sent.</span></span>

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

#### <span data-ttu-id="92122-553">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="92122-553">PostWebMessageAsString</span></span> 

<span data-ttu-id="92122-554">Il s’agit d’un programme d’assistance pour publier un message qui est une chaîne simple plutôt qu’une représentation de chaîne JSON d’un objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="92122-554">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>

> <span data-ttu-id="92122-555">public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="92122-555">public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span></span>

<span data-ttu-id="92122-556">Ce comportement se comporte exactement de la même façon que PostWebMessageAsJson, mais la `window.chrome.webview` propriété Data de arg du message est une chaîne ayant la même valeur que webMessageAsString.</span><span class="sxs-lookup"><span data-stu-id="92122-556">This behaves in exactly the same manner as PostWebMessageAsJson but the `window.chrome.webview` message event arg's data property will be a string with the same value as webMessageAsString.</span></span> <span data-ttu-id="92122-557">Utilisez cette fonction au lieu de PostWebMessageAsJson si vous souhaitez communiquer via des chaînes simples plutôt que des objets JSON.</span><span class="sxs-lookup"><span data-stu-id="92122-557">Use this instead of PostWebMessageAsJson if you want to communicate via simple strings rather than JSON objects.</span></span>

#### <span data-ttu-id="92122-558">Recharger</span><span class="sxs-lookup"><span data-stu-id="92122-558">Reload</span></span> 

<span data-ttu-id="92122-559">Recharger la page active.</span><span class="sxs-lookup"><span data-stu-id="92122-559">Reload the current page.</span></span>

> <span data-ttu-id="92122-560">[rechargement](#reload)du HRESULT public ()</span><span class="sxs-lookup"><span data-stu-id="92122-560">public HRESULT [Reload](#reload)()</span></span>

<span data-ttu-id="92122-561">Il s’agit de la même façon que d’accéder à l’URI du document de niveau supérieur actuel, y compris tous les événements de navigation déclenchant et respectant les entrées dans le cache HTTP.</span><span class="sxs-lookup"><span data-stu-id="92122-561">This is similar to navigating to the URI of current top level document including all navigation events firing and respecting any entries in the HTTP cache.</span></span> <span data-ttu-id="92122-562">Toutefois, l’historique en arrière-plan ne sera pas modifié.</span><span class="sxs-lookup"><span data-stu-id="92122-562">But, the back/forward history will not be modified.</span></span>

#### <span data-ttu-id="92122-563">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="92122-563">remove_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="92122-564">Supprimez le gestionnaire d’événements précédemment ajouté avec la méthode d’événement add_ correspondante.</span><span class="sxs-lookup"><span data-stu-id="92122-564">Remove an event handler previously added with the corresponding add_ event method.</span></span>

> <span data-ttu-id="92122-565">[remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="92122-565">public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="92122-566">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="92122-566">remove_ContentLoading</span></span> 

<span data-ttu-id="92122-567">Supprimez un gestionnaire d’événements préalablement ajouté à add_ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="92122-567">Remove an event handler previously added with add_ContentLoading.</span></span>

> <span data-ttu-id="92122-568">[remove_ContentLoading](#remove_contentloading)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="92122-568">public HRESULT [remove_ContentLoading](#remove_contentloading)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="92122-569">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="92122-569">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="92122-570">Supprimez un gestionnaire d’événements préalablement ajouté à add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="92122-570">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="92122-571">[remove_DocumentTitleChanged](#remove_documenttitlechanged)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="92122-571">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="92122-572">remove_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="92122-572">remove_FrameNavigationCompleted</span></span> 

<span data-ttu-id="92122-573">Supprimez un gestionnaire d’événements préalablement ajouté à add_FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="92122-573">Remove an event handler previously added with add_FrameNavigationCompleted.</span></span>

> <span data-ttu-id="92122-574">[remove_FrameNavigationCompleted](#remove_framenavigationcompleted)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="92122-574">public HRESULT [remove_FrameNavigationCompleted](#remove_framenavigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="92122-575">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="92122-575">remove_FrameNavigationStarting</span></span> 

<span data-ttu-id="92122-576">Supprimez un gestionnaire d’événements préalablement ajouté à add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="92122-576">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>

> <span data-ttu-id="92122-577">[remove_FrameNavigationStarting](#remove_framenavigationstarting)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="92122-577">public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="92122-578">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="92122-578">remove_HistoryChanged</span></span> 

<span data-ttu-id="92122-579">Supprimez un gestionnaire d’événements préalablement ajouté à add_HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="92122-579">Remove an event handler previously added with add_HistoryChanged.</span></span>

> <span data-ttu-id="92122-580">[remove_HistoryChanged](#remove_historychanged)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="92122-580">public HRESULT [remove_HistoryChanged](#remove_historychanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="92122-581">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="92122-581">remove_NavigationCompleted</span></span> 

<span data-ttu-id="92122-582">Supprimez un gestionnaire d’événements préalablement ajouté à add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="92122-582">Remove an event handler previously added with add_NavigationCompleted.</span></span>

> <span data-ttu-id="92122-583">[remove_NavigationCompleted](#remove_navigationcompleted)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="92122-583">public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="92122-584">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="92122-584">remove_NavigationStarting</span></span> 

<span data-ttu-id="92122-585">Supprimez un gestionnaire d’événements préalablement ajouté à add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="92122-585">Remove an event handler previously added with add_NavigationStarting.</span></span>

> <span data-ttu-id="92122-586">[remove_NavigationStarting](#remove_navigationstarting)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="92122-586">public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="92122-587">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="92122-587">remove_NewWindowRequested</span></span> 

<span data-ttu-id="92122-588">Supprimez un gestionnaire d’événements préalablement ajouté à add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="92122-588">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="92122-589">[remove_NewWindowRequested](#remove_newwindowrequested)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="92122-589">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="92122-590">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="92122-590">remove_PermissionRequested</span></span> 

<span data-ttu-id="92122-591">Supprimez un gestionnaire d’événements préalablement ajouté à add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="92122-591">Remove an event handler previously added with add_PermissionRequested.</span></span>

> <span data-ttu-id="92122-592">[remove_PermissionRequested](#remove_permissionrequested)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="92122-592">public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="92122-593">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="92122-593">remove_ProcessFailed</span></span> 

<span data-ttu-id="92122-594">Supprimez un gestionnaire d’événements préalablement ajouté à add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="92122-594">Remove an event handler previously added with add_ProcessFailed.</span></span>

> <span data-ttu-id="92122-595">[remove_ProcessFailed](#remove_processfailed)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="92122-595">public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="92122-596">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="92122-596">remove_ScriptDialogOpening</span></span> 

<span data-ttu-id="92122-597">Supprimez un gestionnaire d’événements préalablement ajouté à add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="92122-597">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>

> <span data-ttu-id="92122-598">[remove_ScriptDialogOpening](#remove_scriptdialogopening)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="92122-598">public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="92122-599">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="92122-599">remove_SourceChanged</span></span> 

<span data-ttu-id="92122-600">Supprimez un gestionnaire d’événements préalablement ajouté à add_SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="92122-600">Remove an event handler previously added with add_SourceChanged.</span></span>

> <span data-ttu-id="92122-601">[remove_SourceChanged](#remove_sourcechanged)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="92122-601">public HRESULT [remove_SourceChanged](#remove_sourcechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="92122-602">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="92122-602">remove_WebMessageReceived</span></span> 

<span data-ttu-id="92122-603">Supprimez un gestionnaire d’événements préalablement ajouté à add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="92122-603">Remove an event handler previously added with add_WebMessageReceived.</span></span>

> <span data-ttu-id="92122-604">[remove_WebMessageReceived](#remove_webmessagereceived)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="92122-604">public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="92122-605">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="92122-605">remove_WebResourceRequested</span></span> 

<span data-ttu-id="92122-606">Supprimez un gestionnaire d’événements préalablement ajouté à add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="92122-606">Remove an event handler previously added with add_WebResourceRequested.</span></span>

> <span data-ttu-id="92122-607">[remove_WebResourceRequested](#remove_webresourcerequested)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="92122-607">public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="92122-608">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="92122-608">remove_WindowCloseRequested</span></span> 

<span data-ttu-id="92122-609">Supprimez un gestionnaire d’événements préalablement ajouté à add_WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="92122-609">Remove an event handler previously added with add_WindowCloseRequested.</span></span>

> <span data-ttu-id="92122-610">[remove_WindowCloseRequested](#remove_windowcloserequested)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="92122-610">public HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="92122-611">RemoveHostObjectFromScript</span><span class="sxs-lookup"><span data-stu-id="92122-611">RemoveHostObjectFromScript</span></span> 

<span data-ttu-id="92122-612">Supprimez l’objet hôte spécifié par le nom afin qu’il ne soit plus accessible à partir du code JavaScript du WebView.</span><span class="sxs-lookup"><span data-stu-id="92122-612">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>

> <span data-ttu-id="92122-613">public HRESULT [RemoveHostObjectFromScript](#removehostobjectfromscript)(nom LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="92122-613">public HRESULT [RemoveHostObjectFromScript](#removehostobjectfromscript)(LPCWSTR name)</span></span>

<span data-ttu-id="92122-614">Même si de nouvelles tentatives d’accès seront refusées, si l’objet est déjà obtenu par le code JavaScript du WebView, le code JavaScript continuera à avoir accès à cet objet.</span><span class="sxs-lookup"><span data-stu-id="92122-614">While new access attempts will be denied, if the object is already obtained by JavaScript code in the WebView, the JavaScript code will continue to have access to that object.</span></span> <span data-ttu-id="92122-615">Il n’est pas nécessaire d’appeler cette méthode pour un nom qui a déjà été supprimé ou n’ayant jamais été ajouté.</span><span class="sxs-lookup"><span data-stu-id="92122-615">Calling this method for a name that is already removed or never added will fail.</span></span>

#### <span data-ttu-id="92122-616">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="92122-616">RemoveScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="92122-617">Supprimez le JavaScript correspondant ajouté par le biais de AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="92122-617">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>

> <span data-ttu-id="92122-618">public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(ID LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="92122-618">public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR id)</span></span>

#### <span data-ttu-id="92122-619">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="92122-619">RemoveWebResourceRequestedFilter</span></span> 

<span data-ttu-id="92122-620">Supprime un filtre de ressources correspondant précédemment ajouté pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="92122-620">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

> <span data-ttu-id="92122-621">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) constante resourceContext)</span><span class="sxs-lookup"><span data-stu-id="92122-621">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="92122-622">Si le même filtre a été ajouté plusieurs fois, il doit être supprimé autant de fois que ce dernier a été ajouté pour que la suppression soit effective.</span><span class="sxs-lookup"><span data-stu-id="92122-622">If the same filter was added multiple times, then it will need to be removed as many times as it was added for the removal to be effective.</span></span> <span data-ttu-id="92122-623">Renvoie E_INVALIDARG pour un filtre qui n’a jamais été ajouté.</span><span class="sxs-lookup"><span data-stu-id="92122-623">Returns E_INVALIDARG for a filter that was never added.</span></span>

#### <span data-ttu-id="92122-624">Stop</span><span class="sxs-lookup"><span data-stu-id="92122-624">Stop</span></span> 

<span data-ttu-id="92122-625">Arrêtez toutes les navigations et les extractions de ressources en attente.</span><span class="sxs-lookup"><span data-stu-id="92122-625">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="92122-626">point d' [arrêt](#stop)public HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="92122-626">public HRESULT [Stop](#stop)()</span></span>

<span data-ttu-id="92122-627">Ne permet pas d’arrêter les scripts.</span><span class="sxs-lookup"><span data-stu-id="92122-627">Does not stop scripts.</span></span>

#### <span data-ttu-id="92122-628">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="92122-628">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span> 

<span data-ttu-id="92122-629">Format d’image utilisé par la méthode ICoreWebView2:: CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="92122-629">Image format used by the ICoreWebView2::CapturePreview method.</span></span>

> <span data-ttu-id="92122-630">énumération [COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format)</span><span class="sxs-lookup"><span data-stu-id="92122-630">enum [COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format)</span></span>

 <span data-ttu-id="92122-631">Doubl</span><span class="sxs-lookup"><span data-stu-id="92122-631">Values</span></span>                         | <span data-ttu-id="92122-632">Descriptions</span><span class="sxs-lookup"><span data-stu-id="92122-632">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="92122-633">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span><span class="sxs-lookup"><span data-stu-id="92122-633">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span></span>            | <span data-ttu-id="92122-634">Format d’image PNG.</span><span class="sxs-lookup"><span data-stu-id="92122-634">PNG image format.</span></span>
<span data-ttu-id="92122-635">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span><span class="sxs-lookup"><span data-stu-id="92122-635">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span></span>            | <span data-ttu-id="92122-636">Format d’image JPEG.</span><span class="sxs-lookup"><span data-stu-id="92122-636">JPEG image format.</span></span>

#### <span data-ttu-id="92122-637">COREWEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="92122-637">COREWEBVIEW2_KEY_EVENT_KIND</span></span> 

<span data-ttu-id="92122-638">Type d’événement de touche qui déclenchait un événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="92122-638">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="92122-639">énumération [COREWEBVIEW2_KEY_EVENT_KIND](#corewebview2_key_event_kind)</span><span class="sxs-lookup"><span data-stu-id="92122-639">enum [COREWEBVIEW2_KEY_EVENT_KIND](#corewebview2_key_event_kind)</span></span>

 <span data-ttu-id="92122-640">Doubl</span><span class="sxs-lookup"><span data-stu-id="92122-640">Values</span></span>                         | <span data-ttu-id="92122-641">Descriptions</span><span class="sxs-lookup"><span data-stu-id="92122-641">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="92122-642">COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="92122-642">COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span></span>            | <span data-ttu-id="92122-643">Correspond à WM_KEYDOWN de messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="92122-643">Correspond to window message WM_KEYDOWN.</span></span>
<span data-ttu-id="92122-644">COREWEBVIEW2_KEY_EVENT_KIND_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="92122-644">COREWEBVIEW2_KEY_EVENT_KIND_KEY_UP</span></span>            | <span data-ttu-id="92122-645">Correspond à WM_KEYUP de messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="92122-645">Correspond to window message WM_KEYUP.</span></span>
<span data-ttu-id="92122-646">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="92122-646">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span></span>            | <span data-ttu-id="92122-647">Correspond à WM_SYSKEYDOWN de messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="92122-647">Correspond to window message WM_SYSKEYDOWN.</span></span>
<span data-ttu-id="92122-648">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="92122-648">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span></span>            | <span data-ttu-id="92122-649">Correspond à WM_SYSKEYUP de messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="92122-649">Correspond to window message WM_SYSKEYUP.</span></span>

#### <span data-ttu-id="92122-650">COREWEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="92122-650">COREWEBVIEW2_MOVE_FOCUS_REASON</span></span> 

<span data-ttu-id="92122-651">Raison du déplacement du focus.</span><span class="sxs-lookup"><span data-stu-id="92122-651">Reason for moving focus.</span></span>

> <span data-ttu-id="92122-652">énumération [COREWEBVIEW2_MOVE_FOCUS_REASON](#corewebview2_move_focus_reason)</span><span class="sxs-lookup"><span data-stu-id="92122-652">enum [COREWEBVIEW2_MOVE_FOCUS_REASON](#corewebview2_move_focus_reason)</span></span>

 <span data-ttu-id="92122-653">Doubl</span><span class="sxs-lookup"><span data-stu-id="92122-653">Values</span></span>                         | <span data-ttu-id="92122-654">Descriptions</span><span class="sxs-lookup"><span data-stu-id="92122-654">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="92122-655">COREWEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span><span class="sxs-lookup"><span data-stu-id="92122-655">COREWEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span></span>            | <span data-ttu-id="92122-656">Paramètre de code axé sur le WebView.</span><span class="sxs-lookup"><span data-stu-id="92122-656">Code setting focus into WebView.</span></span>
<span data-ttu-id="92122-657">COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT</span><span class="sxs-lookup"><span data-stu-id="92122-657">COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT</span></span>            | <span data-ttu-id="92122-658">Déplacement du focus en raison d’une touche Tab.</span><span class="sxs-lookup"><span data-stu-id="92122-658">Moving focus due to Tab traversal forward.</span></span>
<span data-ttu-id="92122-659">COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span><span class="sxs-lookup"><span data-stu-id="92122-659">COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span></span>            | <span data-ttu-id="92122-660">Déplacement du focus en partant du haut de l’onglet.</span><span class="sxs-lookup"><span data-stu-id="92122-660">Moving focus due to Tab traversal backward.</span></span>

#### <span data-ttu-id="92122-661">COREWEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="92122-661">COREWEBVIEW2_PERMISSION_KIND</span></span> 

<span data-ttu-id="92122-662">Le type d’une demande d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="92122-662">The type of a permission request.</span></span>

> <span data-ttu-id="92122-663">énumération [COREWEBVIEW2_PERMISSION_KIND](#corewebview2_permission_kind)</span><span class="sxs-lookup"><span data-stu-id="92122-663">enum [COREWEBVIEW2_PERMISSION_KIND](#corewebview2_permission_kind)</span></span>

 <span data-ttu-id="92122-664">Doubl</span><span class="sxs-lookup"><span data-stu-id="92122-664">Values</span></span>                         | <span data-ttu-id="92122-665">Descriptions</span><span class="sxs-lookup"><span data-stu-id="92122-665">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="92122-666">COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="92122-666">COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span></span>            | <span data-ttu-id="92122-667">Autorisation inconnue.</span><span class="sxs-lookup"><span data-stu-id="92122-667">Unknown permission.</span></span>
<span data-ttu-id="92122-668">COREWEBVIEW2_PERMISSION_KIND_MICROPHONE</span><span class="sxs-lookup"><span data-stu-id="92122-668">COREWEBVIEW2_PERMISSION_KIND_MICROPHONE</span></span>            | <span data-ttu-id="92122-669">Autorisation de capture audio.</span><span class="sxs-lookup"><span data-stu-id="92122-669">Permission to capture audio.</span></span>
<span data-ttu-id="92122-670">COREWEBVIEW2_PERMISSION_KIND_CAMERA</span><span class="sxs-lookup"><span data-stu-id="92122-670">COREWEBVIEW2_PERMISSION_KIND_CAMERA</span></span>            | <span data-ttu-id="92122-671">Autorisation de capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="92122-671">Permission to capture video.</span></span>
<span data-ttu-id="92122-672">COREWEBVIEW2_PERMISSION_KIND_GEOLOCATION</span><span class="sxs-lookup"><span data-stu-id="92122-672">COREWEBVIEW2_PERMISSION_KIND_GEOLOCATION</span></span>            | <span data-ttu-id="92122-673">Autorisation d’accès à la géolocalisation.</span><span class="sxs-lookup"><span data-stu-id="92122-673">Permission to access geolocation.</span></span>
<span data-ttu-id="92122-674">COREWEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="92122-674">COREWEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span></span>            | <span data-ttu-id="92122-675">Autorisation d’envoyer des notifications Web.</span><span class="sxs-lookup"><span data-stu-id="92122-675">Permission to send web notifications.</span></span>
<span data-ttu-id="92122-676">COREWEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span><span class="sxs-lookup"><span data-stu-id="92122-676">COREWEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span></span>            | <span data-ttu-id="92122-677">Autorisation d’accès au capteur générique.</span><span class="sxs-lookup"><span data-stu-id="92122-677">Permission to access generic sensor.</span></span>
<span data-ttu-id="92122-678">COREWEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span><span class="sxs-lookup"><span data-stu-id="92122-678">COREWEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span></span>            | <span data-ttu-id="92122-679">Autorisation de lecture du presse-papiers système sans mouvement utilisateur.</span><span class="sxs-lookup"><span data-stu-id="92122-679">Permission to read system clipboard without a user gesture.</span></span>

#### <span data-ttu-id="92122-680">COREWEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="92122-680">COREWEBVIEW2_PERMISSION_STATE</span></span> 

<span data-ttu-id="92122-681">Réponse à une demande d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="92122-681">Response to a permission request.</span></span>

> <span data-ttu-id="92122-682">énumération [COREWEBVIEW2_PERMISSION_STATE](#corewebview2_permission_state)</span><span class="sxs-lookup"><span data-stu-id="92122-682">enum [COREWEBVIEW2_PERMISSION_STATE](#corewebview2_permission_state)</span></span>

 <span data-ttu-id="92122-683">Doubl</span><span class="sxs-lookup"><span data-stu-id="92122-683">Values</span></span>                         | <span data-ttu-id="92122-684">Descriptions</span><span class="sxs-lookup"><span data-stu-id="92122-684">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="92122-685">COREWEBVIEW2_PERMISSION_STATE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="92122-685">COREWEBVIEW2_PERMISSION_STATE_DEFAULT</span></span>            | <span data-ttu-id="92122-686">Utilisez le comportement par défaut du navigateur, qui invite en principe les utilisateurs à la décision.</span><span class="sxs-lookup"><span data-stu-id="92122-686">Use default browser behavior, which normally prompt users for decision.</span></span>
<span data-ttu-id="92122-687">COREWEBVIEW2_PERMISSION_STATE_ALLOW</span><span class="sxs-lookup"><span data-stu-id="92122-687">COREWEBVIEW2_PERMISSION_STATE_ALLOW</span></span>            | <span data-ttu-id="92122-688">Accordez la demande d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="92122-688">Grant the permission request.</span></span>
<span data-ttu-id="92122-689">COREWEBVIEW2_PERMISSION_STATE_DENY</span><span class="sxs-lookup"><span data-stu-id="92122-689">COREWEBVIEW2_PERMISSION_STATE_DENY</span></span>            | <span data-ttu-id="92122-690">Refusez la demande d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="92122-690">Deny the permission request.</span></span>

#### <span data-ttu-id="92122-691">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="92122-691">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span></span> 

<span data-ttu-id="92122-692">Structure représentant les informations contenues dans le LPARAM fourni à un événement de touche Win32.</span><span class="sxs-lookup"><span data-stu-id="92122-692">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

> <span data-ttu-id="92122-693">[COREWEBVIEW2_PHYSICAL_KEY_STATUS](#corewebview2_physical_key_status) typedef</span><span class="sxs-lookup"><span data-stu-id="92122-693">typedef [COREWEBVIEW2_PHYSICAL_KEY_STATUS](#corewebview2_physical_key_status)</span></span>

<span data-ttu-id="92122-694">Pour plus d’informations, consultez la documentation de WM_KEYDOWN[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span><span class="sxs-lookup"><span data-stu-id="92122-694">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span></span>

#### <span data-ttu-id="92122-695">COREWEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="92122-695">COREWEBVIEW2_PROCESS_FAILED_KIND</span></span> 

<span data-ttu-id="92122-696">Type d’échec de processus utilisé dans l’interface ICoreWebView2ProcessFailedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="92122-696">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>

> <span data-ttu-id="92122-697">énumération [COREWEBVIEW2_PROCESS_FAILED_KIND](#corewebview2_process_failed_kind)</span><span class="sxs-lookup"><span data-stu-id="92122-697">enum [COREWEBVIEW2_PROCESS_FAILED_KIND](#corewebview2_process_failed_kind)</span></span>

 <span data-ttu-id="92122-698">Doubl</span><span class="sxs-lookup"><span data-stu-id="92122-698">Values</span></span>                         | <span data-ttu-id="92122-699">Descriptions</span><span class="sxs-lookup"><span data-stu-id="92122-699">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="92122-700">COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="92122-700">COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span></span>            | <span data-ttu-id="92122-701">Indique que le processus du navigateur s’est arrêté de manière inattendue.</span><span class="sxs-lookup"><span data-stu-id="92122-701">Indicates the browser process terminated unexpectedly.</span></span>
<span data-ttu-id="92122-702">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="92122-702">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span></span>            | <span data-ttu-id="92122-703">Indique le processus de rendu arrêté de manière inattendue.</span><span class="sxs-lookup"><span data-stu-id="92122-703">Indicates the render process terminated unexpectedly.</span></span>
<span data-ttu-id="92122-704">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span><span class="sxs-lookup"><span data-stu-id="92122-704">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span></span>            | <span data-ttu-id="92122-705">Indique que le processus de rendu ne répond pas.</span><span class="sxs-lookup"><span data-stu-id="92122-705">Indicates the render process becomes unresponsive.</span></span>

#### <span data-ttu-id="92122-706">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="92122-706">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span></span> 

<span data-ttu-id="92122-707">Type de boîte de dialogue JavaScript utilisée dans l’interface ICoreWebView2ScriptDialogOpeningEventHandler.</span><span class="sxs-lookup"><span data-stu-id="92122-707">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>

> <span data-ttu-id="92122-708">énumération [COREWEBVIEW2_SCRIPT_DIALOG_KIND](#corewebview2_script_dialog_kind)</span><span class="sxs-lookup"><span data-stu-id="92122-708">enum [COREWEBVIEW2_SCRIPT_DIALOG_KIND](#corewebview2_script_dialog_kind)</span></span>

 <span data-ttu-id="92122-709">Doubl</span><span class="sxs-lookup"><span data-stu-id="92122-709">Values</span></span>                         | <span data-ttu-id="92122-710">Descriptions</span><span class="sxs-lookup"><span data-stu-id="92122-710">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="92122-711">COREWEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span><span class="sxs-lookup"><span data-stu-id="92122-711">COREWEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span></span>            | <span data-ttu-id="92122-712">Une boîte de dialogue appelée par le biais de la fonction JavaScript window. Alert.</span><span class="sxs-lookup"><span data-stu-id="92122-712">A dialog invoked via the window.alert JavaScript function.</span></span>
<span data-ttu-id="92122-713">COREWEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span><span class="sxs-lookup"><span data-stu-id="92122-713">COREWEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span></span>            | <span data-ttu-id="92122-714">Une boîte de dialogue appelée via la fonction de fenêtre. confirmer JavaScript.</span><span class="sxs-lookup"><span data-stu-id="92122-714">A dialog invoked via the window.confirm JavaScript function.</span></span>
<span data-ttu-id="92122-715">COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span><span class="sxs-lookup"><span data-stu-id="92122-715">COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span></span>            | <span data-ttu-id="92122-716">Une boîte de dialogue appelée via la fonction JavaScript window. prompt.</span><span class="sxs-lookup"><span data-stu-id="92122-716">A dialog invoked via the window.prompt JavaScript function.</span></span>
<span data-ttu-id="92122-717">COREWEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span><span class="sxs-lookup"><span data-stu-id="92122-717">COREWEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span></span>            | <span data-ttu-id="92122-718">Une boîte de dialogue appelée via l’événement JavaScript beforeunload.</span><span class="sxs-lookup"><span data-stu-id="92122-718">A dialog invoked via the beforeunload JavaScript event.</span></span>

#### <span data-ttu-id="92122-719">COREWEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="92122-719">COREWEBVIEW2_WEB_ERROR_STATUS</span></span> 

<span data-ttu-id="92122-720">Valeurs d’état d’erreur pour les navigations Web.</span><span class="sxs-lookup"><span data-stu-id="92122-720">Error status values for web navigations.</span></span>

> <span data-ttu-id="92122-721">énumération [COREWEBVIEW2_WEB_ERROR_STATUS](#corewebview2_web_error_status)</span><span class="sxs-lookup"><span data-stu-id="92122-721">enum [COREWEBVIEW2_WEB_ERROR_STATUS](#corewebview2_web_error_status)</span></span>

 <span data-ttu-id="92122-722">Doubl</span><span class="sxs-lookup"><span data-stu-id="92122-722">Values</span></span>                         | <span data-ttu-id="92122-723">Descriptions</span><span class="sxs-lookup"><span data-stu-id="92122-723">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="92122-724">COREWEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="92122-724">COREWEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span></span>            | <span data-ttu-id="92122-725">Une erreur inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="92122-725">An unknown error occurred.</span></span>
<span data-ttu-id="92122-726">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span><span class="sxs-lookup"><span data-stu-id="92122-726">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span></span>            | <span data-ttu-id="92122-727">Le nom usuel du certificat SSL ne correspond pas à l’adresse Web.</span><span class="sxs-lookup"><span data-stu-id="92122-727">The SSL certificate common name does not match the web address.</span></span>
<span data-ttu-id="92122-728">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span><span class="sxs-lookup"><span data-stu-id="92122-728">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span></span>            | <span data-ttu-id="92122-729">Le certificat SSL a expiré.</span><span class="sxs-lookup"><span data-stu-id="92122-729">The SSL certificate has expired.</span></span>
<span data-ttu-id="92122-730">COREWEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span><span class="sxs-lookup"><span data-stu-id="92122-730">COREWEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span></span>            | <span data-ttu-id="92122-731">Le certificat client SSL comporte des erreurs.</span><span class="sxs-lookup"><span data-stu-id="92122-731">The SSL client certificate contains errors.</span></span>
<span data-ttu-id="92122-732">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span><span class="sxs-lookup"><span data-stu-id="92122-732">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span></span>            | <span data-ttu-id="92122-733">Le certificat SSL a été révoqué.</span><span class="sxs-lookup"><span data-stu-id="92122-733">The SSL certificate has been revoked.</span></span>
<span data-ttu-id="92122-734">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span><span class="sxs-lookup"><span data-stu-id="92122-734">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span></span>            | <span data-ttu-id="92122-735">Le certificat SSL n’est pas valide &ndash; cela peut signifier que le certificat ne correspond pas aux codes confidentiels de clé publique du nom d’hôte. le certificat est signé par une autorité non approuvée ou à l’aide d’un algorithme de signature faible, le certificat ayant revendiqué des noms DNS enfreignant les contraintes de nom, le certificat contient une clé faible, la période de validité du certificat est trop longue, l’absence de données de révocation ou du mécanisme de révocation, le [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html)nom d’hôte non unique, l’absence de données de transparence de</span><span class="sxs-lookup"><span data-stu-id="92122-735">The SSL certificate is invalid &ndash; this could mean the certificate did not match the public key pins for the host name, the certificate is signed by an untrusted authority or using a weak sign algorithm, the certificate claimed DNS names violate name constraints, the certificate contains a weak key, the certificate's validity period is too long, lack of revocation information or revocation mechanism, non-unique host name, lack of certificate transparency information, or the certificate is chained to a [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).</span></span>
<span data-ttu-id="92122-736">COREWEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="92122-736">COREWEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span></span>            | <span data-ttu-id="92122-737">L’hôte n’est pas joignable.</span><span class="sxs-lookup"><span data-stu-id="92122-737">The host is unreachable.</span></span>
<span data-ttu-id="92122-738">COREWEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="92122-738">COREWEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span></span>            | <span data-ttu-id="92122-739">La connexion a expiré.</span><span class="sxs-lookup"><span data-stu-id="92122-739">The connection has timed out.</span></span>
<span data-ttu-id="92122-740">COREWEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span><span class="sxs-lookup"><span data-stu-id="92122-740">COREWEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span></span>            | <span data-ttu-id="92122-741">Le serveur a renvoyé une réponse non valide ou non reconnue.</span><span class="sxs-lookup"><span data-stu-id="92122-741">The server returned an invalid or unrecognized response.</span></span>
<span data-ttu-id="92122-742">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span><span class="sxs-lookup"><span data-stu-id="92122-742">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span></span>            | <span data-ttu-id="92122-743">La connexion a été annulée.</span><span class="sxs-lookup"><span data-stu-id="92122-743">The connection was aborted.</span></span>
<span data-ttu-id="92122-744">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span><span class="sxs-lookup"><span data-stu-id="92122-744">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span></span>            | <span data-ttu-id="92122-745">La connexion a été réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="92122-745">The connection was reset.</span></span>
<span data-ttu-id="92122-746">COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span><span class="sxs-lookup"><span data-stu-id="92122-746">COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span></span>            | <span data-ttu-id="92122-747">La connexion Internet a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="92122-747">The Internet connection has been lost.</span></span>
<span data-ttu-id="92122-748">COREWEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span><span class="sxs-lookup"><span data-stu-id="92122-748">COREWEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span></span>            | <span data-ttu-id="92122-749">Connexion impossible à la destination.</span><span class="sxs-lookup"><span data-stu-id="92122-749">Cannot connect to destination.</span></span>
<span data-ttu-id="92122-750">COREWEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="92122-750">COREWEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span></span>            | <span data-ttu-id="92122-751">Impossible de résoudre le nom d’hôte fourni.</span><span class="sxs-lookup"><span data-stu-id="92122-751">Could not resolve provided host name.</span></span>
<span data-ttu-id="92122-752">COREWEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span><span class="sxs-lookup"><span data-stu-id="92122-752">COREWEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span></span>            | <span data-ttu-id="92122-753">L’opération a été annulée.</span><span class="sxs-lookup"><span data-stu-id="92122-753">The operation was canceled.</span></span>
<span data-ttu-id="92122-754">COREWEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span><span class="sxs-lookup"><span data-stu-id="92122-754">COREWEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span></span>            | <span data-ttu-id="92122-755">Échec de la redirection de la requête.</span><span class="sxs-lookup"><span data-stu-id="92122-755">The request redirect failed.</span></span>
<span data-ttu-id="92122-756">COREWEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span><span class="sxs-lookup"><span data-stu-id="92122-756">COREWEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span></span>            | <span data-ttu-id="92122-757">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="92122-757">An unexpected error occurred.</span></span>

#### <span data-ttu-id="92122-758">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="92122-758">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span></span> 

<span data-ttu-id="92122-759">Énum pour les contextes de demande de ressources Web.</span><span class="sxs-lookup"><span data-stu-id="92122-759">Enum for web resource request contexts.</span></span>

> <span data-ttu-id="92122-760">énumération [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context)</span><span class="sxs-lookup"><span data-stu-id="92122-760">enum [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context)</span></span>

 <span data-ttu-id="92122-761">Doubl</span><span class="sxs-lookup"><span data-stu-id="92122-761">Values</span></span>                         | <span data-ttu-id="92122-762">Descriptions</span><span class="sxs-lookup"><span data-stu-id="92122-762">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="92122-763">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span><span class="sxs-lookup"><span data-stu-id="92122-763">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span></span>            | <span data-ttu-id="92122-764">Toutes les ressources.</span><span class="sxs-lookup"><span data-stu-id="92122-764">All resources.</span></span>
<span data-ttu-id="92122-765">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="92122-765">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span></span>            | <span data-ttu-id="92122-766">Ressources de documents.</span><span class="sxs-lookup"><span data-stu-id="92122-766">Document resources.</span></span>
<span data-ttu-id="92122-767">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span><span class="sxs-lookup"><span data-stu-id="92122-767">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span></span>            | <span data-ttu-id="92122-768">Des ressources CSS;</span><span class="sxs-lookup"><span data-stu-id="92122-768">CSS resources.</span></span>
<span data-ttu-id="92122-769">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span><span class="sxs-lookup"><span data-stu-id="92122-769">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span></span>            | <span data-ttu-id="92122-770">Ressources d’image.</span><span class="sxs-lookup"><span data-stu-id="92122-770">Image resources.</span></span>
<span data-ttu-id="92122-771">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span><span class="sxs-lookup"><span data-stu-id="92122-771">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span></span>            | <span data-ttu-id="92122-772">Autres ressources multimédias telles que les vidéos.</span><span class="sxs-lookup"><span data-stu-id="92122-772">Other media resources such as videos.</span></span>
<span data-ttu-id="92122-773">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span><span class="sxs-lookup"><span data-stu-id="92122-773">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span></span>            | <span data-ttu-id="92122-774">Ressources de police.</span><span class="sxs-lookup"><span data-stu-id="92122-774">Font resources.</span></span>
<span data-ttu-id="92122-775">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="92122-775">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span></span>            | <span data-ttu-id="92122-776">Ressources de script.</span><span class="sxs-lookup"><span data-stu-id="92122-776">Script resources.</span></span>
<span data-ttu-id="92122-777">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="92122-777">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span></span>            | <span data-ttu-id="92122-778">Requêtes HTTP XML.</span><span class="sxs-lookup"><span data-stu-id="92122-778">XML HTTP requests.</span></span>
<span data-ttu-id="92122-779">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span><span class="sxs-lookup"><span data-stu-id="92122-779">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span></span>            | <span data-ttu-id="92122-780">Extraire la communication de l’API.</span><span class="sxs-lookup"><span data-stu-id="92122-780">Fetch API communication.</span></span>
<span data-ttu-id="92122-781">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span><span class="sxs-lookup"><span data-stu-id="92122-781">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span></span>            | <span data-ttu-id="92122-782">Ressources TextTrack.</span><span class="sxs-lookup"><span data-stu-id="92122-782">TextTrack resources.</span></span>
<span data-ttu-id="92122-783">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span><span class="sxs-lookup"><span data-stu-id="92122-783">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span></span>            | <span data-ttu-id="92122-784">Communication API EventSource.</span><span class="sxs-lookup"><span data-stu-id="92122-784">EventSource API communication.</span></span>
<span data-ttu-id="92122-785">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span><span class="sxs-lookup"><span data-stu-id="92122-785">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span></span>            | <span data-ttu-id="92122-786">Communication de l’API WebSocket.</span><span class="sxs-lookup"><span data-stu-id="92122-786">WebSocket API communication.</span></span>
<span data-ttu-id="92122-787">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span><span class="sxs-lookup"><span data-stu-id="92122-787">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span></span>            | <span data-ttu-id="92122-788">Manifestes de l’application Web.</span><span class="sxs-lookup"><span data-stu-id="92122-788">Web App Manifests.</span></span>
<span data-ttu-id="92122-789">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span><span class="sxs-lookup"><span data-stu-id="92122-789">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span></span>            | <span data-ttu-id="92122-790">Échange HTTP signé.</span><span class="sxs-lookup"><span data-stu-id="92122-790">Signed HTTP Exchanges.</span></span>
<span data-ttu-id="92122-791">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span><span class="sxs-lookup"><span data-stu-id="92122-791">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span></span>            | <span data-ttu-id="92122-792">Demandes ping.</span><span class="sxs-lookup"><span data-stu-id="92122-792">Ping requests.</span></span>
<span data-ttu-id="92122-793">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span><span class="sxs-lookup"><span data-stu-id="92122-793">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span></span>            | <span data-ttu-id="92122-794">Rapports de violation des CSP.</span><span class="sxs-lookup"><span data-stu-id="92122-794">CSP Violation Reports.</span></span>
<span data-ttu-id="92122-795">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span><span class="sxs-lookup"><span data-stu-id="92122-795">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span></span>            | <span data-ttu-id="92122-796">Autres ressources.</span><span class="sxs-lookup"><span data-stu-id="92122-796">Other resources.</span></span>

