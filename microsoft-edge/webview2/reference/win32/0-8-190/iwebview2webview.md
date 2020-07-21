---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2WebView
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 5711a1dbf501df55fefc9709763c1fe225865e11
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886429"
---
# <span data-ttu-id="0a278-104">0.8.355-interface IWebView2WebView</span><span class="sxs-lookup"><span data-stu-id="0a278-104">0.8.355 - interface IWebView2WebView</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebView
  : public IUnknown
```

<span data-ttu-id="0a278-105">WebView2 vous permet d’héberger le contenu Web à l’aide de la technologie de navigateur Web la plus récente.</span><span class="sxs-lookup"><span data-stu-id="0a278-105">WebView2 enables you to host web content using the latest Edge web browser technology.</span></span>

## <span data-ttu-id="0a278-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="0a278-106">Summary</span></span>

 <span data-ttu-id="0a278-107">Ses</span><span class="sxs-lookup"><span data-stu-id="0a278-107">Members</span></span>                        | <span data-ttu-id="0a278-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="0a278-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0a278-109">get_Settings</span><span class="sxs-lookup"><span data-stu-id="0a278-109">get_Settings</span></span>](#get_settings) | <span data-ttu-id="0a278-110">L’objet [IWebView2Settings](IWebView2Settings.md) contient différents paramètres modifiables pour le WebView en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="0a278-110">The [IWebView2Settings](IWebView2Settings.md) object contains various modifiable settings for the running WebView.</span></span>
[<span data-ttu-id="0a278-111">get_Source</span><span class="sxs-lookup"><span data-stu-id="0a278-111">get_Source</span></span>](#get_source) | <span data-ttu-id="0a278-112">URI du document de niveau supérieur actuel.</span><span class="sxs-lookup"><span data-stu-id="0a278-112">The URI of the current top level document.</span></span>
[<span data-ttu-id="0a278-113">Rechercher</span><span class="sxs-lookup"><span data-stu-id="0a278-113">Navigate</span></span>](#navigate) | <span data-ttu-id="0a278-114">Entraîner une navigation du document de niveau supérieur sur l’URI spécifié.</span><span class="sxs-lookup"><span data-stu-id="0a278-114">Cause a navigation of the top level document to the specified URI.</span></span>
[<span data-ttu-id="0a278-115">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="0a278-115">MoveFocus</span></span>](#movefocus) | <span data-ttu-id="0a278-116">Déplacer le focus sur le WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-116">Move focus into WebView.</span></span>
[<span data-ttu-id="0a278-117">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="0a278-117">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="0a278-118">Lance une navigation vers htmlContent en tant que code HTML source d’un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="0a278-118">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="0a278-119">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="0a278-119">add_NavigationStarting</span></span>](#add_navigationstarting) | <span data-ttu-id="0a278-120">Ajoutez un gestionnaire d’événements pour l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="0a278-120">Add an event handler for the NavigationStarting event.</span></span>
[<span data-ttu-id="0a278-121">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="0a278-121">remove_NavigationStarting</span></span>](#remove_navigationstarting) | <span data-ttu-id="0a278-122">Supprimez un gestionnaire d’événements préalablement ajouté à add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="0a278-122">Remove an event handler previously added with add_NavigationStarting.</span></span>
[<span data-ttu-id="0a278-123">add_DocumentStateChanged</span><span class="sxs-lookup"><span data-stu-id="0a278-123">add_DocumentStateChanged</span></span>](#add_documentstatechanged) | <span data-ttu-id="0a278-124">Ajoutez un gestionnaire d’événements pour l’événement DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="0a278-124">Add an event handler for the DocumentStateChanged event.</span></span>
[<span data-ttu-id="0a278-125">remove_DocumentStateChanged</span><span class="sxs-lookup"><span data-stu-id="0a278-125">remove_DocumentStateChanged</span></span>](#remove_documentstatechanged) | <span data-ttu-id="0a278-126">Supprimez un gestionnaire d’événements préalablement ajouté à add_DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="0a278-126">Remove an event handler previously added with add_DocumentStateChanged.</span></span>
[<span data-ttu-id="0a278-127">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="0a278-127">add_NavigationCompleted</span></span>](#add_navigationcompleted) | <span data-ttu-id="0a278-128">Ajoutez un gestionnaire d’événements pour l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="0a278-128">Add an event handler for the NavigationCompleted event.</span></span>
[<span data-ttu-id="0a278-129">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="0a278-129">remove_NavigationCompleted</span></span>](#remove_navigationcompleted) | <span data-ttu-id="0a278-130">Supprimez un gestionnaire d’événements préalablement ajouté à add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="0a278-130">Remove an event handler previously added with add_NavigationCompleted.</span></span>
[<span data-ttu-id="0a278-131">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="0a278-131">add_FrameNavigationStarting</span></span>](#add_framenavigationstarting) | <span data-ttu-id="0a278-132">Ajoutez un gestionnaire d’événements pour l’événement FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="0a278-132">Add an event handler for the FrameNavigationStarting event.</span></span>
[<span data-ttu-id="0a278-133">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="0a278-133">remove_FrameNavigationStarting</span></span>](#remove_framenavigationstarting) | <span data-ttu-id="0a278-134">Supprimez un gestionnaire d’événements préalablement ajouté à add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="0a278-134">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>
[<span data-ttu-id="0a278-135">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="0a278-135">add_MoveFocusRequested</span></span>](#add_movefocusrequested) | <span data-ttu-id="0a278-136">Ajoutez un gestionnaire d’événements pour l’événement MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="0a278-136">Add an event handler for the MoveFocusRequested event.</span></span>
[<span data-ttu-id="0a278-137">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="0a278-137">remove_MoveFocusRequested</span></span>](#remove_movefocusrequested) | <span data-ttu-id="0a278-138">Supprimez un gestionnaire d’événements préalablement ajouté à add_MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="0a278-138">Remove an event handler previously added with add_MoveFocusRequested.</span></span>
[<span data-ttu-id="0a278-139">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="0a278-139">add_GotFocus</span></span>](#add_gotfocus) | <span data-ttu-id="0a278-140">Ajoutez un gestionnaire d’événements pour l’événement GotFocus.</span><span class="sxs-lookup"><span data-stu-id="0a278-140">Add an event handler for the GotFocus event.</span></span>
[<span data-ttu-id="0a278-141">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="0a278-141">remove_GotFocus</span></span>](#remove_gotfocus) | <span data-ttu-id="0a278-142">Supprimez un gestionnaire d’événements préalablement ajouté à add_GotFocus.</span><span class="sxs-lookup"><span data-stu-id="0a278-142">Remove an event handler previously added with add_GotFocus.</span></span>
[<span data-ttu-id="0a278-143">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="0a278-143">add_LostFocus</span></span>](#add_lostfocus) | <span data-ttu-id="0a278-144">Ajoutez un gestionnaire d’événements pour l’événement LostFocus.</span><span class="sxs-lookup"><span data-stu-id="0a278-144">Add an event handler for the LostFocus event.</span></span>
[<span data-ttu-id="0a278-145">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="0a278-145">remove_LostFocus</span></span>](#remove_lostfocus) | <span data-ttu-id="0a278-146">Supprimez un gestionnaire d’événements préalablement ajouté à add_LostFocus.</span><span class="sxs-lookup"><span data-stu-id="0a278-146">Remove an event handler previously added with add_LostFocus.</span></span>
[<span data-ttu-id="0a278-147">add_WebResourceRequested_deprecated</span><span class="sxs-lookup"><span data-stu-id="0a278-147">add_WebResourceRequested_deprecated</span></span>](#add_webresourcerequested_deprecated) | <span data-ttu-id="0a278-148">Cette API est déconseillée, utilisez la nouvelle API add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="0a278-148">This API will be deprecated, please use the new add_WebResourceRequested API.</span></span>
[<span data-ttu-id="0a278-149">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="0a278-149">remove_WebResourceRequested</span></span>](#remove_webresourcerequested) | <span data-ttu-id="0a278-150">Supprimez un gestionnaire d’événements préalablement ajouté à add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="0a278-150">Remove an event handler previously added with add_WebResourceRequested.</span></span>
[<span data-ttu-id="0a278-151">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="0a278-151">add_ScriptDialogOpening</span></span>](#add_scriptdialogopening) | <span data-ttu-id="0a278-152">Ajoutez un gestionnaire d’événements pour l’événement ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="0a278-152">Add an event handler for the ScriptDialogOpening event.</span></span>
[<span data-ttu-id="0a278-153">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="0a278-153">remove_ScriptDialogOpening</span></span>](#remove_scriptdialogopening) | <span data-ttu-id="0a278-154">Supprimez un gestionnaire d’événements préalablement ajouté à add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="0a278-154">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>
[<span data-ttu-id="0a278-155">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="0a278-155">add_ZoomFactorChanged</span></span>](#add_zoomfactorchanged) | <span data-ttu-id="0a278-156">Ajoutez un gestionnaire d’événements pour l’événement ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="0a278-156">Add an event handler for the ZoomFactorChanged event.</span></span>
[<span data-ttu-id="0a278-157">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="0a278-157">remove_ZoomFactorChanged</span></span>](#remove_zoomfactorchanged) | <span data-ttu-id="0a278-158">Supprimez un gestionnaire d’événements préalablement ajouté à add_ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="0a278-158">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>
[<span data-ttu-id="0a278-159">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="0a278-159">add_PermissionRequested</span></span>](#add_permissionrequested) | <span data-ttu-id="0a278-160">Ajoutez un gestionnaire d’événements pour l’événement PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="0a278-160">Add an event handler for the PermissionRequested event.</span></span>
[<span data-ttu-id="0a278-161">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="0a278-161">remove_PermissionRequested</span></span>](#remove_permissionrequested) | <span data-ttu-id="0a278-162">Supprimez un gestionnaire d’événements préalablement ajouté à add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="0a278-162">Remove an event handler previously added with add_PermissionRequested.</span></span>
[<span data-ttu-id="0a278-163">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="0a278-163">add_ProcessFailed</span></span>](#add_processfailed) | <span data-ttu-id="0a278-164">Ajoutez un gestionnaire d’événements pour l’événement ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="0a278-164">Add an event handler for the ProcessFailed event.</span></span>
[<span data-ttu-id="0a278-165">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="0a278-165">remove_ProcessFailed</span></span>](#remove_processfailed) | <span data-ttu-id="0a278-166">Supprimez un gestionnaire d’événements préalablement ajouté à add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="0a278-166">Remove an event handler previously added with add_ProcessFailed.</span></span>
[<span data-ttu-id="0a278-167">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="0a278-167">AddScriptToExecuteOnDocumentCreated</span></span>](#addscripttoexecuteondocumentcreated) | <span data-ttu-id="0a278-168">Ajoutez le code JavaScript fourni à une liste de scripts qui doivent être exécutés après la création de l’objet global, mais avant l’analyse du document HTML et avant l’exécution de tout autre script fourni par le document HTML.</span><span class="sxs-lookup"><span data-stu-id="0a278-168">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>
[<span data-ttu-id="0a278-169">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="0a278-169">RemoveScriptToExecuteOnDocumentCreated</span></span>](#removescripttoexecuteondocumentcreated) | <span data-ttu-id="0a278-170">Supprimez le JavaScript correspondant ajouté par le biais de AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="0a278-170">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>
[<span data-ttu-id="0a278-171">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="0a278-171">ExecuteScript</span></span>](#executescript) | <span data-ttu-id="0a278-172">Exécutez le code JavaScript du paramètre JavaScript du document de niveau supérieur actuel affiché dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-172">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="0a278-173">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="0a278-173">CapturePreview</span></span>](#capturepreview) | <span data-ttu-id="0a278-174">Capturez une image de l’affichage du WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-174">Capture an image of what WebView is displaying.</span></span>
[<span data-ttu-id="0a278-175">Recharger</span><span class="sxs-lookup"><span data-stu-id="0a278-175">Reload</span></span>](#reload) | <span data-ttu-id="0a278-176">Recharger la page active.</span><span class="sxs-lookup"><span data-stu-id="0a278-176">Reload the current page.</span></span>
[<span data-ttu-id="0a278-177">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="0a278-177">get_Bounds</span></span>](#get_bounds) | <span data-ttu-id="0a278-178">Les limites de l’affichage WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-178">The webview bounds.</span></span>
[<span data-ttu-id="0a278-179">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="0a278-179">put_Bounds</span></span>](#put_bounds) | <span data-ttu-id="0a278-180">Définissez la propriété Bounds.</span><span class="sxs-lookup"><span data-stu-id="0a278-180">Set the Bounds property.</span></span>
[<span data-ttu-id="0a278-181">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="0a278-181">get_ZoomFactor</span></span>](#get_zoomfactor) | <span data-ttu-id="0a278-182">Facteur de zoom pour la page active dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-182">The zoom factor for the current page in the WebView.</span></span>
[<span data-ttu-id="0a278-183">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="0a278-183">put_ZoomFactor</span></span>](#put_zoomfactor) | <span data-ttu-id="0a278-184">Définissez la propriété ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="0a278-184">Set the ZoomFactor property.</span></span>
[<span data-ttu-id="0a278-185">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="0a278-185">get_IsVisible</span></span>](#get_isvisible) | <span data-ttu-id="0a278-186">La propriété IsVisible détermine s’il faut afficher ou masquer le WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-186">The IsVisible property determines whether to show or hide the webview.</span></span>
[<span data-ttu-id="0a278-187">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="0a278-187">put_IsVisible</span></span>](#put_isvisible) | <span data-ttu-id="0a278-188">Définissez la propriété IsVisible.</span><span class="sxs-lookup"><span data-stu-id="0a278-188">Set the IsVisible property.</span></span>
[<span data-ttu-id="0a278-189">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="0a278-189">PostWebMessageAsJson</span></span>](#postwebmessageasjson) | <span data-ttu-id="0a278-190">Publiez le WebMessage spécifié dans le document de niveau supérieur de cette [IWebView2WebView]().</span><span class="sxs-lookup"><span data-stu-id="0a278-190">Post the specified webMessage to the top level document in this [IWebView2WebView]().</span></span>
[<span data-ttu-id="0a278-191">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="0a278-191">PostWebMessageAsString</span></span>](#postwebmessageasstring) | <span data-ttu-id="0a278-192">Il s’agit d’un programme d’assistance pour publier un message qui est une chaîne simple plutôt qu’une représentation de chaîne JSON d’un objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0a278-192">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>
[<span data-ttu-id="0a278-193">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="0a278-193">add_WebMessageReceived</span></span>](#add_webmessagereceived) | <span data-ttu-id="0a278-194">Cet événement se déclenche lorsque le paramètre IsWebMessageEnabled est défini et au document de niveau supérieur des appels WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="0a278-194">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>
[<span data-ttu-id="0a278-195">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="0a278-195">remove_WebMessageReceived</span></span>](#remove_webmessagereceived) | <span data-ttu-id="0a278-196">Supprimez un gestionnaire d’événements préalablement ajouté à add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="0a278-196">Remove an event handler previously added with add_WebMessageReceived.</span></span>
[<span data-ttu-id="0a278-197">Fermer</span><span class="sxs-lookup"><span data-stu-id="0a278-197">Close</span></span>](#close) | <span data-ttu-id="0a278-198">Ferme le WebView et nettoie l’instance de navigateur sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="0a278-198">Closes the webview and cleans up the underlying browser instance.</span></span>
[<span data-ttu-id="0a278-199">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="0a278-199">CallDevToolsProtocolMethod</span></span>](#calldevtoolsprotocolmethod) | <span data-ttu-id="0a278-200">Appelez une méthode DevToolsProtocol asynchrone.</span><span class="sxs-lookup"><span data-stu-id="0a278-200">Call an asynchronous DevToolsProtocol method.</span></span>
[<span data-ttu-id="0a278-201">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="0a278-201">add_DevToolsProtocolEventReceived</span></span>](#add_devtoolsprotocoleventreceived) | <span data-ttu-id="0a278-202">S’abonner à un événement DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="0a278-202">Subscribe to a DevToolsProtocol event.</span></span>
[<span data-ttu-id="0a278-203">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="0a278-203">remove_DevToolsProtocolEventReceived</span></span>](#remove_devtoolsprotocoleventreceived) | <span data-ttu-id="0a278-204">Supprimez un gestionnaire d’événements préalablement ajouté à add_DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="0a278-204">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>
[<span data-ttu-id="0a278-205">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="0a278-205">get_BrowserProcessId</span></span>](#get_browserprocessid) | <span data-ttu-id="0a278-206">ID de processus du processus de navigation qui héberge le WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-206">The process id of the browser process that hosts the WebView.</span></span>
[<span data-ttu-id="0a278-207">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="0a278-207">get_CanGoBack</span></span>](#get_cangoback) | <span data-ttu-id="0a278-208">Peut parcourir le WebView vers la page précédente de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="0a278-208">Can navigate the webview to the previous page in the navigation history.</span></span>
[<span data-ttu-id="0a278-209">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="0a278-209">get_CanGoForward</span></span>](#get_cangoforward) | <span data-ttu-id="0a278-210">Peut parcourir le WebView sur la page suivante de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="0a278-210">Can navigate the webview to the next page in the navigation history.</span></span>
[<span data-ttu-id="0a278-211">GoBack</span><span class="sxs-lookup"><span data-stu-id="0a278-211">GoBack</span></span>](#goback) | <span data-ttu-id="0a278-212">Permet d’accéder à la page précédente de l’historique de navigation via le WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-212">Navigates the webview to the previous page in the navigation history.</span></span>
[<span data-ttu-id="0a278-213">GoForward</span><span class="sxs-lookup"><span data-stu-id="0a278-213">GoForward</span></span>](#goforward) | <span data-ttu-id="0a278-214">Navigue vers la page suivante de l’historique de navigation du WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-214">Navigates the webview to the next page in the navigation history.</span></span>
[<span data-ttu-id="0a278-215">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="0a278-215">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span>](#webview2_capture_preview_image_format) | <span data-ttu-id="0a278-216">Format d’image utilisé par la méthode [IWebView2WebView:: CapturePreview](#capturepreview) .</span><span class="sxs-lookup"><span data-stu-id="0a278-216">Image format used by the [IWebView2WebView::CapturePreview](#capturepreview) method.</span></span>
[<span data-ttu-id="0a278-217">WEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="0a278-217">WEBVIEW2_SCRIPT_DIALOG_KIND</span></span>](#webview2_script_dialog_kind) | <span data-ttu-id="0a278-218">Type de boîte de dialogue JavaScript utilisée dans l’interface [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) .</span><span class="sxs-lookup"><span data-stu-id="0a278-218">Kind of JavaScript dialog used in the [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) interface.</span></span>
[<span data-ttu-id="0a278-219">WEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="0a278-219">WEBVIEW2_PROCESS_FAILED_KIND</span></span>](#webview2_process_failed_kind) | <span data-ttu-id="0a278-220">Type d’échec de processus utilisé dans l’interface [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) .</span><span class="sxs-lookup"><span data-stu-id="0a278-220">Kind of process failure used in the [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) interface.</span></span>
[<span data-ttu-id="0a278-221">WEBVIEW2_PERMISSION_TYPE</span><span class="sxs-lookup"><span data-stu-id="0a278-221">WEBVIEW2_PERMISSION_TYPE</span></span>](#webview2_permission_type) | <span data-ttu-id="0a278-222">Le type d’une demande d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="0a278-222">The type of a permission request.</span></span>
[<span data-ttu-id="0a278-223">WEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="0a278-223">WEBVIEW2_PERMISSION_STATE</span></span>](#webview2_permission_state) | <span data-ttu-id="0a278-224">Réponse à une demande d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="0a278-224">Response to a permission request.</span></span>
[<span data-ttu-id="0a278-225">WEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="0a278-225">WEBVIEW2_MOVE_FOCUS_REASON</span></span>](#webview2_move_focus_reason) | <span data-ttu-id="0a278-226">Raison du déplacement du focus.</span><span class="sxs-lookup"><span data-stu-id="0a278-226">Reason for moving focus.</span></span>
[<span data-ttu-id="0a278-227">WEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="0a278-227">WEBVIEW2_WEB_ERROR_STATUS</span></span>](#webview2_web_error_status) | <span data-ttu-id="0a278-228">Valeurs d’état d’erreur pour les navigations Web.</span><span class="sxs-lookup"><span data-stu-id="0a278-228">Error status values for web navigations.</span></span>
[<span data-ttu-id="0a278-229">WEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="0a278-229">WEBVIEW2_WEB_RESOURCE_CONTEXT</span></span>](#webview2_web_resource_context) | <span data-ttu-id="0a278-230">Énum pour les contextes de demande de ressources Web.</span><span class="sxs-lookup"><span data-stu-id="0a278-230">Enum for web resource request contexts.</span></span>

## <span data-ttu-id="0a278-231">Événements de navigation</span><span class="sxs-lookup"><span data-stu-id="0a278-231">Navigation events</span></span>

<span data-ttu-id="0a278-232">L’ordre normal des événements de navigation est NavigationStarting, DocumentStateChanged, puis NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="0a278-232">The normal sequence of navigation events is NavigationStarting, DocumentStateChanged and then NavigationCompleted.</span></span>

![dot-inline-dotgraph-1.png](media/dot-inline-dotgraph-1.png)

<span data-ttu-id="0a278-234">Notez qu’il s’agit d’événements de navigation avec le même argument d’événement NavigationId.</span><span class="sxs-lookup"><span data-stu-id="0a278-234">Note that this is for navigation events with the same NavigationId event arg.</span></span> <span data-ttu-id="0a278-235">Les événements de navigation avec différents arguments d’événement NavigationId risquent de se chevaucher.</span><span class="sxs-lookup"><span data-stu-id="0a278-235">Navigations events with different NavigationId event args may overlap.</span></span> <span data-ttu-id="0a278-236">Par exemple, si vous démarrez une navigation pour l’événement NavigationStarting, puis démarrez une autre navigation, vous verrez le NavigationStarting de la première navigation suivi par le NavigationStarting du deuxième navigation, suivi de l’NavigationCompleted de la première navigation, puis de tout le reste des événements de navigation appropriés pour la deuxième navigation.</span><span class="sxs-lookup"><span data-stu-id="0a278-236">For instance, if you start a navigation wait for its NavigationStarting event and then start another navigation you'll see the NavigationStarting for the first navigate followed by the NavigationStarting of the second navigate, followed by the NavigationCompleted for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span> <span data-ttu-id="0a278-237">Dans les cas d’erreur, il est possible ou non qu’un événement DocumentStateChanged se poursuive sur une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0a278-237">In error cases there may or may not be a DocumentStateChanged event depending on whether the navigation is continued to an error page.</span></span> <span data-ttu-id="0a278-238">Dans le cas d’une redirection HTTP, plusieurs événements NavigationStarting sont disponibles dans une ligne, avec les indicateurs IsRedirect définis dans le premier.</span><span class="sxs-lookup"><span data-stu-id="0a278-238">In case of an HTTP redirect, there will be multiple NavigationStarting events in a row, with ones following the first will have their IsRedirect flag set.</span></span>

<span data-ttu-id="0a278-239">Dans le cas de sous-trames dans WebView, le seul événement de navigation déclenché est l’événement NavigationStarting qui donne à l’hôte la possibilité de bloquer les navigations de sous-bloc.</span><span class="sxs-lookup"><span data-stu-id="0a278-239">For subframes inside WebView, the only navigation event fired is the NavigationStarting event which gives host the ability to block subframe navigations.</span></span>

## <span data-ttu-id="0a278-240">Modèle de processus</span><span class="sxs-lookup"><span data-stu-id="0a278-240">Process model</span></span>

<span data-ttu-id="0a278-241">WebView2 utilise le même modèle de processus que le navigateur Web Edge.</span><span class="sxs-lookup"><span data-stu-id="0a278-241">WebView2 uses the same process model as the Edge web browser.</span></span> <span data-ttu-id="0a278-242">Il existe un processus de navigateur Edge par répertoire de données utilisateur spécifié dans une session utilisateur qui traitera tout processus appelant WebView2 spécifiant ce répertoire de données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0a278-242">There is one Edge browser process per specified user data directory in a user session that will serve any WebView2 calling process that specifies that user data directory.</span></span> <span data-ttu-id="0a278-243">Cela signifie qu’un processus de navigateur Edge est susceptible de traiter plusieurs processus d’appel et qu’un processus d’appel est susceptible d’utiliser plusieurs processus de navigation latérale.</span><span class="sxs-lookup"><span data-stu-id="0a278-243">This means one Edge browser process may be serving multiple calling processes and one calling process may be using multiple Edge browser processes.</span></span>

![dot-inline-dotgraph-2.png](media/dot-inline-dotgraph-2.png)

<span data-ttu-id="0a278-245">Il y a un certain nombre de processus de convertisseur.</span><span class="sxs-lookup"><span data-stu-id="0a278-245">Off of a browser process there will be some number of renderer processes.</span></span> <span data-ttu-id="0a278-246">Celles-ci sont créées autant de fois que nécessaire pour traiter plusieurs trames dans différents affichages.</span><span class="sxs-lookup"><span data-stu-id="0a278-246">These are created as necessary to service potentially multiple frames in different WebViews.</span></span> <span data-ttu-id="0a278-247">Le nombre de processus de rendu varie en fonction de la fonctionnalité du navigateur d’isolement de site et du nombre d’origines distantes distinctes affichées dans les webvues associées.</span><span class="sxs-lookup"><span data-stu-id="0a278-247">The number of renderer processes varies based on the site isolation browser feature and the number of distinct disconnected origins rendered in associated WebViews.</span></span>

![dot-inline-dotgraph-3.png](media/dot-inline-dotgraph-3.png)

<span data-ttu-id="0a278-249">Vous pouvez réagir aux blocages et se bloquer dans ces processus de navigateur et de convertisseur à l’aide de l’événement ProcessFailure.</span><span class="sxs-lookup"><span data-stu-id="0a278-249">You can react to crashes and hangs in these browser and renderer processes using the ProcessFailure event.</span></span>

<span data-ttu-id="0a278-250">Vous pouvez arrêter en toute sécurité les processus de navigateur et de convertisseur associés à l’aide de la méthode Close.</span><span class="sxs-lookup"><span data-stu-id="0a278-250">You can safely shutdown associated browser and renderer processes using the Close method.</span></span>

## <span data-ttu-id="0a278-251">Modèle de threads</span><span class="sxs-lookup"><span data-stu-id="0a278-251">Threading model</span></span>

<span data-ttu-id="0a278-252">WebView2 doit être créé sur un thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0a278-252">The WebView2 must be created on a UI thread.</span></span> <span data-ttu-id="0a278-253">Particulièrement un thread avec une pompe de messages.</span><span class="sxs-lookup"><span data-stu-id="0a278-253">Specifically a thread with a message pump.</span></span> <span data-ttu-id="0a278-254">Tous les rappels se produiront sur ce thread et les appels dans le WebView doivent être effectués sur ce thread.</span><span class="sxs-lookup"><span data-stu-id="0a278-254">All callbacks will occur on that thread and calls into the WebView must be done on that thread.</span></span> <span data-ttu-id="0a278-255">Il n’est pas sûr d’utiliser le WebView à partir d’un autre thread.</span><span class="sxs-lookup"><span data-stu-id="0a278-255">It is not safe to use the WebView from another thread.</span></span>

<span data-ttu-id="0a278-256">Les rappels incluant des gestionnaires d’événements et des gestionnaires d’achèvement s’exécutent en série.</span><span class="sxs-lookup"><span data-stu-id="0a278-256">Callbacks including event handlers and completion handlers execute serially.</span></span> <span data-ttu-id="0a278-257">Autrement dit, si vous disposez d’un gestionnaire d’événements et commencez une boucle de message, il n’y a pas de gestionnaires d’événements ou de rappels d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="0a278-257">That is, if you have an event handler running and begin a message loop no other event handlers or completion callbacks will begin executing reentrantly.</span></span>

## <span data-ttu-id="0a278-258">Sécurité</span><span class="sxs-lookup"><span data-stu-id="0a278-258">Security</span></span>

<span data-ttu-id="0a278-259">Vérifiez toujours la propriété source de WebView avant d’utiliser ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString, ou toute autre méthode pour envoyer des informations dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-259">Always check the Source property of the WebView before using ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString, or any other method to send information into the WebView.</span></span> <span data-ttu-id="0a278-260">Le WebView peut avoir navigué vers une autre page par le biais de l’utilisateur final qui interagit avec la page ou le script de la page entraînant la navigation.</span><span class="sxs-lookup"><span data-stu-id="0a278-260">The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation.</span></span> <span data-ttu-id="0a278-261">De même, soyez prudent avec AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="0a278-261">Similarly, be very careful with AddScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="0a278-262">Toutes les futures navigations exécuteront ce script et, s’il donne accès à des informations destinées uniquement à un certain type d’origine, tous les documents HTML peuvent avoir accès.</span><span class="sxs-lookup"><span data-stu-id="0a278-262">All future navigations will run this script and if it provides access to information intended only for a certain origin, any HTML document may have access.</span></span>

<span data-ttu-id="0a278-263">Lorsque vous examinez le résultat d’un appel de méthode ExecuteScript, un événement WebMessageReceived, vérifie toujours la source de l’expéditeur ou tout autre mécanisme de réception d’informations à partir d’un document HTML dans un WebView valide l’URI du document HTML correspond à ce que vous attendez.</span><span class="sxs-lookup"><span data-stu-id="0a278-263">When examining the result of an ExecuteScript method call, a WebMessageReceived event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.</span></span>

<span data-ttu-id="0a278-264">Lorsque vous construisez un message à envoyer dans un WebView, préférez utilisez PostWebMessageAsJson et construisez le paramètre de chaîne JSON à l’aide d’une bibliothèque JSON.</span><span class="sxs-lookup"><span data-stu-id="0a278-264">When constructing a message to send into a WebView, prefer using PostWebMessageAsJson and construct the JSON string parameter using a JSON library.</span></span> <span data-ttu-id="0a278-265">Cela évite les accidents potentiels d’encoder des informations dans une chaîne ou un script JSON et garantir qu’aucune entrée contrôlée par l’attaquant ne peut modifier le reste du message JSON ou exécuter un script arbitraire.</span><span class="sxs-lookup"><span data-stu-id="0a278-265">This will avoid any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script.</span></span>

## <span data-ttu-id="0a278-266">Types de chaîne</span><span class="sxs-lookup"><span data-stu-id="0a278-266">String types</span></span>

<span data-ttu-id="0a278-267">Les paramètres de type chaîne sont des chaînes de type LPWSTR nul terminées.</span><span class="sxs-lookup"><span data-stu-id="0a278-267">String out parameters are LPWSTR null terminated strings.</span></span> <span data-ttu-id="0a278-268">Le l’appelant alloue la chaîne à l’aide de CoTaskMemAlloc.</span><span class="sxs-lookup"><span data-stu-id="0a278-268">The callee allocates the string using CoTaskMemAlloc.</span></span> <span data-ttu-id="0a278-269">La propriété est transférée à l’appelant et il revient à l’appelant de libérer de la mémoire à l’aide de CoTaskMemFree.</span><span class="sxs-lookup"><span data-stu-id="0a278-269">Ownership is transferred to the caller and it is up to the caller to free the memory using CoTaskMemFree.</span></span>

<span data-ttu-id="0a278-270">La chaîne figurant dans les paramètres est LPCWSTRe des chaînes arrêtées null.</span><span class="sxs-lookup"><span data-stu-id="0a278-270">String in parameters are LPCWSTR null terminated strings.</span></span> <span data-ttu-id="0a278-271">L’appelant vérifie que la chaîne est valide pour la durée de l’appel de fonction synchrone.</span><span class="sxs-lookup"><span data-stu-id="0a278-271">The caller ensures the string is valid for the duration of the synchronous function call.</span></span> <span data-ttu-id="0a278-272">Si les appelants doivent conserver cette valeur à un certain point après la fin de l’appel de fonction, l’appelant doit allouer sa propre copie de la valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="0a278-272">If the callee needs to retain that value to some point after the function call completes, the callee must allocate its own copy of the string value.</span></span>

## <span data-ttu-id="0a278-273">D’analyse des URI et de JSON</span><span class="sxs-lookup"><span data-stu-id="0a278-273">URI and JSON parsing</span></span>

<span data-ttu-id="0a278-274">Diverses méthodes fournissent ou acceptent des URI et JSON en tant que chaînes.</span><span class="sxs-lookup"><span data-stu-id="0a278-274">Various methods provide or accept URIs and JSON as strings.</span></span> <span data-ttu-id="0a278-275">Utilisez votre propre bibliothèque préférée pour analyser et générer ces chaînes.</span><span class="sxs-lookup"><span data-stu-id="0a278-275">Please use your own preferred library for parsing and generating these strings.</span></span>

<span data-ttu-id="0a278-276">Si WinRT est disponible pour votre application, vous pouvez l’utiliser `RuntimeClass_Windows_Data_Json_JsonObject` et `IJsonObjectStatics` analyser ou générer des chaînes JSON ou `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` analyser et générer des URI.</span><span class="sxs-lookup"><span data-stu-id="0a278-276">If WinRT is available for your app you can use `RuntimeClass_Windows_Data_Json_JsonObject` and `IJsonObjectStatics` to parse or produce JSON strings or `RuntimeClass_Windows_Foundation_Uri` and `IUriRuntimeClassFactory` to parse and produce URIs.</span></span> <span data-ttu-id="0a278-277">Ces deux fonctions fonctionnent dans les applications Win32.</span><span class="sxs-lookup"><span data-stu-id="0a278-277">Both of these work in Win32 apps.</span></span>

<span data-ttu-id="0a278-278">Si vous utilisez IUri et CreateUri pour analyser les URI, il est possible que vous souhaitiez utiliser les indicateurs de création d’URI suivants pour que le comportement CreateUri correspond plus étroitement à l’analyse d’URI dans le WebView:</span><span class="sxs-lookup"><span data-stu-id="0a278-278">If you use IUri and CreateUri to parse URIs you may want to use the following URI creation flags to have CreateUri behavior more closely match the URI parsing in the WebView:</span></span> `Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO`

## <span data-ttu-id="0a278-279">Débogage</span><span class="sxs-lookup"><span data-stu-id="0a278-279">Debugging</span></span>

<span data-ttu-id="0a278-280">Ouvrez DevTools avec les raccourcis normaux: `F12` ou `Ctrl+Shift+I` .</span><span class="sxs-lookup"><span data-stu-id="0a278-280">Open DevTools with the normal shortcuts: `F12` or `Ctrl+Shift+I`.</span></span> <span data-ttu-id="0a278-281">Vous pouvez utiliser le `--auto-open-devtools-for-tabs` commutateur d’argument de commande pour que la fenêtre devtools s’ouvre immédiatement lors de la création d’un WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-281">You can use the `--auto-open-devtools-for-tabs` command argument switch to have the DevTools window open immediately when first creating a WebView.</span></span> <span data-ttu-id="0a278-282">Pour plus d’informations sur le processus de navigation, voir documentation CreateWebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-282">See CreateWebView documentation for how to provide additional command line arguments to the browser process.</span></span> <span data-ttu-id="0a278-283">Consultez la clé de Registre LoaderOverride pour essayer différentes builds de WebView2 sans modifier votre application dans la documentation CreateWebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-283">Check out the LoaderOverride registry key for trying out different builds of WebView2 without modifying your application in the CreateWebView documentation.</span></span>

## <span data-ttu-id="0a278-284">Contrôle de version</span><span class="sxs-lookup"><span data-stu-id="0a278-284">Versioning</span></span>

<span data-ttu-id="0a278-285">Une fois que vous avez utilisé une version particulière du SDK pour générer votre application, l’exécution de votre application avec une version plus ancienne ou plus récente des fichiers binaires de navigateur installés sera terminée.</span><span class="sxs-lookup"><span data-stu-id="0a278-285">After you've used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.</span></span> <span data-ttu-id="0a278-286">Jusqu’à la version 1.0.0.0 de WebView2, des modifications peuvent être apportées lors des mises à jour qui empêchent votre SDK de fonctionner avec des versions différentes des fichiers binaires de navigateur installés.</span><span class="sxs-lookup"><span data-stu-id="0a278-286">Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that will prevent your SDK from working with different versions of installed browser binaries.</span></span> <span data-ttu-id="0a278-287">Après la version 1.0.0.0, vous pouvez utiliser les différentes versions du kit de développement logiciel (SDK) pour travailler avec les meilleures pratiques suivantes:</span><span class="sxs-lookup"><span data-stu-id="0a278-287">After version 1.0.0.0 different versions of the SDK can work with different versions of the installed browser by following these best practices:</span></span>

<span data-ttu-id="0a278-288">Pour prendre en compte les modifications apportées à l’API, veillez à vérifier l’échec lors de l’appel de la DLL d’exportation CreateWebView2Environment et lors de l’appel de QueryInterface sur un objet WebView2.</span><span class="sxs-lookup"><span data-stu-id="0a278-288">To account for breaking changes to the API be sure to check for failure when calling the DLL export CreateWebView2Environment and when calling QueryInterface on any WebView2 object.</span></span> <span data-ttu-id="0a278-289">La valeur de retour de E_NOINTERFACE peut indiquer que le kit de développement logiciel (SDK) n’est pas compatible avec les fichiers binaires de navigation Edge.</span><span class="sxs-lookup"><span data-stu-id="0a278-289">A return value of E_NOINTERFACE can indicate the SDK is not compatible with the Edge browser binaries.</span></span>

<span data-ttu-id="0a278-290">La vérification de l’échec de QueryInterface sera également comptabilisée dans les cas où le kit de développement logiciel (SDK) est plus récent que la version du navigateur Edge et que votre application tente d’utiliser une interface qui n’est pas compatible avec le navigateur Edge.</span><span class="sxs-lookup"><span data-stu-id="0a278-290">Checking for failure from QueryInterface will also account for cases where the SDK is newer than the version of the Edge browser and your app attempts to use an interface of which the Edge browser is unaware.</span></span>

<span data-ttu-id="0a278-291">Lorsqu’une interface n’est pas disponible, vous pouvez envisager de désactiver la fonctionnalité associée le cas échéant ou d’informer l’utilisateur final qu’il doit mettre à jour son navigateur.</span><span class="sxs-lookup"><span data-stu-id="0a278-291">When an interface is unavailable, you can consider disabling the associated feature if possible, or otherwise informing the end user they need to update their browser.</span></span>

## <span data-ttu-id="0a278-292">Ses</span><span class="sxs-lookup"><span data-stu-id="0a278-292">Members</span></span>

#### <span data-ttu-id="0a278-293">get_Settings</span><span class="sxs-lookup"><span data-stu-id="0a278-293">get_Settings</span></span> 

<span data-ttu-id="0a278-294">L’objet [IWebView2Settings](IWebView2Settings.md) contient différents paramètres modifiables pour le WebView en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="0a278-294">The [IWebView2Settings](IWebView2Settings.md) object contains various modifiable settings for the running WebView.</span></span>

> <span data-ttu-id="0a278-295">valeurs publiques HRESULT [get_Settings](#get_settings)([IWebView2Settings](IWebView2Settings.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="0a278-295">public HRESULT [get_Settings](#get_settings)([IWebView2Settings](IWebView2Settings.md) \*\* settings)</span></span>

#### <span data-ttu-id="0a278-296">get_Source</span><span class="sxs-lookup"><span data-stu-id="0a278-296">get_Source</span></span> 

<span data-ttu-id="0a278-297">URI du document de niveau supérieur actuel.</span><span class="sxs-lookup"><span data-stu-id="0a278-297">The URI of the current top level document.</span></span>

> <span data-ttu-id="0a278-298">valeur publique HRESULT [get_Source](#get_source)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="0a278-298">public HRESULT [get_Source](#get_source)(LPWSTR \* uri)</span></span>

<span data-ttu-id="0a278-299">Cette valeur peut changer dans le cadre du déclenchement de l’événement DocumentStateChanged, dans certains cas, par exemple, la navigation vers un site ou un fragment de navigation différent.</span><span class="sxs-lookup"><span data-stu-id="0a278-299">This value potentially changes as a part of the DocumentStateChanged event firing for some cases such as navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="0a278-300">Il restera identique pour les autres types de navigation, tels que les recharges de page ou l’historique. pushState avec la même URL que la page active.</span><span class="sxs-lookup"><span data-stu-id="0a278-300">It will remain the same for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span>

```cpp
    // Register a handler for the DocumentStateChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_DocumentStateChanged(
        Callback<IWebView2DocumentStateChangedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2DocumentStateChangedEventArgs* args)
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
        &m_documentStateChangedToken));
```

#### <span data-ttu-id="0a278-301">Rechercher</span><span class="sxs-lookup"><span data-stu-id="0a278-301">Navigate</span></span> 

<span data-ttu-id="0a278-302">Entraîner une navigation du document de niveau supérieur sur l’URI spécifié.</span><span class="sxs-lookup"><span data-stu-id="0a278-302">Cause a navigation of the top level document to the specified URI.</span></span>

> <span data-ttu-id="0a278-303">public HRESULT [Navigate](#navigate)(Uri LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="0a278-303">public HRESULT [Navigate](#navigate)(LPCWSTR uri)</span></span>

<span data-ttu-id="0a278-304">Pour plus d’informations, voir événements de navigation.</span><span class="sxs-lookup"><span data-stu-id="0a278-304">See the navigation events for more information.</span></span> <span data-ttu-id="0a278-305">Notez que cela démarre une navigation et que l’événement NavigationStarting correspondant est déclenché après la fin de l’appel.</span><span class="sxs-lookup"><span data-stu-id="0a278-305">Note that this starts a navigation and the corresponding NavigationStarting event will fire sometime after this Navigate call completes.</span></span>

```cpp
void ControlComponent::NavigateToAddressBar()
{
    WCHAR uri[2048] = L"";
    GetWindowText(m_toolbar->addressBarWindow, uri, ARRAYSIZE(uri));
    CHECK_FAILURE(m_webView->Navigate(uri));
}
```

#### <span data-ttu-id="0a278-306">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="0a278-306">MoveFocus</span></span> 

<span data-ttu-id="0a278-307">Déplacer le focus sur le WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-307">Move focus into WebView.</span></span>

> <span data-ttu-id="0a278-308">public HRESULT [MoveFocus](#movefocus)([WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason) raison)</span><span class="sxs-lookup"><span data-stu-id="0a278-308">public HRESULT [MoveFocus](#movefocus)([WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason) reason)</span></span>

<span data-ttu-id="0a278-309">WebView va mettre le focus et le focus sur l’élément correspondant dans la page hébergée dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-309">WebView will get focus and focus will be set to correspondent element in the page hosted in the WebView.</span></span> <span data-ttu-id="0a278-310">Pour des raisons de programmation, le focus est défini sur l’élément précédemment prioritaire ou l’élément par défaut s’il n’y a pas d’élément prioritaire auparavant.</span><span class="sxs-lookup"><span data-stu-id="0a278-310">For Programmatic reason, focus is set to previously focused element or the default element if there is no previously focused element.</span></span> <span data-ttu-id="0a278-311">Pour une raison suivante, le focus est défini sur le premier élément.</span><span class="sxs-lookup"><span data-stu-id="0a278-311">For Next reason, focus is set to the first element.</span></span> <span data-ttu-id="0a278-312">Pour une raison précédente, le focus est défini sur le dernier élément.</span><span class="sxs-lookup"><span data-stu-id="0a278-312">For Previous reason, focus is set to the last element.</span></span> <span data-ttu-id="0a278-313">Le mode webaffichage peut également mettre le focus sur une interaction utilisateur telle que cliquer sur le WebView ou sur Tab.</span><span class="sxs-lookup"><span data-stu-id="0a278-313">WebView can also got focus through user interaction like clicking into WebView or Tab into it.</span></span> <span data-ttu-id="0a278-314">Pour la fonction de tabulation, l’application peut appeler MoveFocus avec Next ou Previous pour s’aligner sur TAB et Maj + Tab lorsqu’elle décide que le WebView est l’élément tabbable suivant.</span><span class="sxs-lookup"><span data-stu-id="0a278-314">For tabbing, the app can call MoveFocus with Next or Previous to align with tab and shift+tab respectively when it decides the WebView is the next tabbable element.</span></span> <span data-ttu-id="0a278-315">Par exemple, l’application peut appeler IsDialogMessage dans le cadre de sa boucle de messages pour permettre à la plateforme de gérer automatiquement la tabulation.</span><span class="sxs-lookup"><span data-stu-id="0a278-315">Or, the app can call IsDialogMessage as part of its message loop to allow the platform to auto handle tabbing.</span></span> <span data-ttu-id="0a278-316">La plateforme est pivotée sur toutes les fenêtres avec WS_TABSTOP.</span><span class="sxs-lookup"><span data-stu-id="0a278-316">The platform will rotate through all windows with WS_TABSTOP.</span></span> <span data-ttu-id="0a278-317">Lorsque le WebView obtient le focus de IsDialogMessage, il positionne en interne le focus sur le premier ou le dernier élément de Tab et Maj + Tab respectivement.</span><span class="sxs-lookup"><span data-stu-id="0a278-317">When the WebView gets focus from IsDialogMessage, it will internally put the focus on the first or last element for tab and shift+tab respectively.</span></span>

```cpp
    while (GetMessage(&msg, nullptr, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            // Calling IsDialogMessage handles Tab traversal automatically. If the
            // app wants the platform to auto handle tab, then call IsDialogMessage
            // before calling TranslateMessage/DispatchMessage. If the app wants to
            // handle tabbing itself, then skip calling IsDialogMessage and call
            // TranslateMessage/DispatchMessage directly.
            if (!g_autoTabHandle || !IsDialogMessage(GetAncestor(msg.hwnd, GA_ROOT), &msg))
            {
                TranslateMessage(&msg);
                DispatchMessage(&msg);
            }
        }
    }
```

```cpp
        if (wParam == VK_TAB)
        {
            // Find out if the window is one we've customized for tab handling
            for (int i = 0; i < m_tabbableWindows.size(); i++)
            {
                if (m_tabbableWindows[i].first == hWnd)
                {
                    if (GetKeyState(VK_SHIFT) < 0)
                    {
                        TabBackwards(i);
                    }
                    else
                    {
                        TabForwards(i);
                    }
                    return true;
                }
            }
        }
```

```cpp
void ControlComponent::TabForwards(int currentIndex)
{
    // Find first enabled window after the active one
    for (int i = currentIndex + 1; i < m_tabbableWindows.size(); i++)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    m_webView->MoveFocus(WEBVIEW2_MOVE_FOCUS_REASON_NEXT);
}

void ControlComponent::TabBackwards(int currentIndex)
{
    // Find first enabled window before the active one
    for (int i = currentIndex - 1; i >= 0; i--)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    CHECK_FAILURE(m_webView->MoveFocus(WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS));
}
```

#### <span data-ttu-id="0a278-318">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="0a278-318">NavigateToString</span></span> 

<span data-ttu-id="0a278-319">Lance une navigation vers htmlContent en tant que code HTML source d’un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="0a278-319">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="0a278-320">public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span><span class="sxs-lookup"><span data-stu-id="0a278-320">public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span></span>

<span data-ttu-id="0a278-321">Le paramètre htmlContent ne doit pas comporter plus de 2 Mo de caractères.</span><span class="sxs-lookup"><span data-stu-id="0a278-321">The htmlContent parameter may not be larger than 2 MB of characters.</span></span> <span data-ttu-id="0a278-322">L’origine de la nouvelle page va être vide.</span><span class="sxs-lookup"><span data-stu-id="0a278-322">The origin of the new page will be about:blank.</span></span>

```cpp
                static const PCWSTR htmlContent =
                    L"<h1>Domain Blocked</h1>"
                    L"<p>You've attempted to navigate to a domain in the blocked "
                    L"sites list. Press back to return to the previous page.</p>";
                CHECK_FAILURE(sender->NavigateToString(htmlContent));
```

#### <span data-ttu-id="0a278-323">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="0a278-323">add_NavigationStarting</span></span> 

<span data-ttu-id="0a278-324">Ajoutez un gestionnaire d’événements pour l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="0a278-324">Add an event handler for the NavigationStarting event.</span></span>

> <span data-ttu-id="0a278-325">[add_NavigationStarting](#add_navigationstarting)par le biais du[mot de passe](IWebView2NavigationStartingEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="0a278-325">public HRESULT [add_NavigationStarting](#add_navigationstarting)([IWebView2NavigationStartingEventHandler](IWebView2NavigationStartingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="0a278-326">NavigationStarting se déclenche lorsque le frame principal WebView demande une autorisation pour accéder à un URI différent.</span><span class="sxs-lookup"><span data-stu-id="0a278-326">NavigationStarting fires when the WebView main frame is requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="0a278-327">Cela se déclenche également pour les redirections.</span><span class="sxs-lookup"><span data-stu-id="0a278-327">This will fire for redirects as well.</span></span>

```cpp
    // Register a handler for the NavigationStarting event.
    // This handler will check the domain being navigated to, and if the domain
    // matches a list of blocked sites, it will cancel the navigation and
    // possibly display a warning page.  It will also disable JavaScript on
    // selected websites.
    CHECK_FAILURE(m_webView->add_NavigationStarting(
        Callback<IWebView2NavigationStartingEventHandler>(
            [this](IWebView2WebView* sender,
                   IWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));

            // If the user clicked a link to navigate, show a warning page.
            BOOL userInitiated;
            CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));
            if (userInitiated)
            {
                static const PCWSTR htmlContent =
                    L"<h1>Domain Blocked</h1>"
                    L"<p>You've attempted to navigate to a domain in the blocked "
                    L"sites list. Press back to return to the previous page.</p>";
                CHECK_FAILURE(sender->NavigateToString(htmlContent));
            }
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

#### <span data-ttu-id="0a278-328">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="0a278-328">remove_NavigationStarting</span></span> 

<span data-ttu-id="0a278-329">Supprimez un gestionnaire d’événements préalablement ajouté à add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="0a278-329">Remove an event handler previously added with add_NavigationStarting.</span></span>

> <span data-ttu-id="0a278-330">[remove_NavigationStarting](#remove_navigationstarting)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="0a278-330">public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="0a278-331">add_DocumentStateChanged</span><span class="sxs-lookup"><span data-stu-id="0a278-331">add_DocumentStateChanged</span></span> 

<span data-ttu-id="0a278-332">Ajoutez un gestionnaire d’événements pour l’événement DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="0a278-332">Add an event handler for the DocumentStateChanged event.</span></span>

> <span data-ttu-id="0a278-333">[add_DocumentStateChanged](#add_documentstatechanged)par le biais du[mot de passe](IWebView2DocumentStateChangedEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="0a278-333">public HRESULT [add_DocumentStateChanged](#add_documentstatechanged)([IWebView2DocumentStateChangedEventHandler](IWebView2DocumentStateChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="0a278-334">DocumentStateChanged est déclenché lorsqu’un nouveau contenu a commencé à se charger sur l’image principale du WebView ou si une même navigation de page se produit (par exemple par le biais des navigations par fragments ou de l’historique. pushState).</span><span class="sxs-lookup"><span data-stu-id="0a278-334">DocumentStateChanged fires when new content has started loading on the webview's main frame or if a same page navigation occurs (such as through fragment navigations or history.pushState navigations).</span></span> <span data-ttu-id="0a278-335">Cela suit l’événement NavigationStarting et précède l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="0a278-335">This follows the NavigationStarting event and precedes the NavigationCompleted event.</span></span>

```cpp
    // Register a handler for the DocumentStateChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_DocumentStateChanged(
        Callback<IWebView2DocumentStateChangedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2DocumentStateChangedEventArgs* args)
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
        &m_documentStateChangedToken));
```

#### <span data-ttu-id="0a278-336">remove_DocumentStateChanged</span><span class="sxs-lookup"><span data-stu-id="0a278-336">remove_DocumentStateChanged</span></span> 

<span data-ttu-id="0a278-337">Supprimez un gestionnaire d’événements préalablement ajouté à add_DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="0a278-337">Remove an event handler previously added with add_DocumentStateChanged.</span></span>

> <span data-ttu-id="0a278-338">[remove_DocumentStateChanged](#remove_documentstatechanged)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="0a278-338">public HRESULT [remove_DocumentStateChanged](#remove_documentstatechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="0a278-339">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="0a278-339">add_NavigationCompleted</span></span> 

<span data-ttu-id="0a278-340">Ajoutez un gestionnaire d’événements pour l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="0a278-340">Add an event handler for the NavigationCompleted event.</span></span>

> <span data-ttu-id="0a278-341">[add_NavigationCompleted](#add_navigationcompleted)par le biais du[mot de passe](IWebView2NavigationCompletedEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="0a278-341">public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([IWebView2NavigationCompletedEventHandler](IWebView2NavigationCompletedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="0a278-342">L’événement NavigationCompleted se déclenche lorsque le WebView est complètement chargé (le corps. OnLoad a été déclenché) ou que le chargement s’est arrêté avec une erreur.</span><span class="sxs-lookup"><span data-stu-id="0a278-342">NavigationCompleted event fires when the WebView has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

```cpp
    // Register a handler for the NavigationCompleted event.
    // Check whether the navigation succeeded, and if not, do something.
    // Also update the Back, Forward, and Cancel buttons.
    CHECK_FAILURE(m_webView->add_NavigationCompleted(
        Callback<IWebView2NavigationCompletedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2NavigationCompletedEventArgs* args)
                -> HRESULT {
                BOOL success;
                CHECK_FAILURE(args->get_IsSuccess(&success));
                if (!success)
                {
                    WEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    if (webErrorStatus == WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }

                BOOL canGoBack;
                BOOL canGoForward;
                sender->get_CanGoBack(&canGoBack);
                sender->get_CanGoForward(&canGoForward);
                EnableWindow(m_toolbar->backWindow, canGoBack);
                EnableWindow(m_toolbar->forwardWindow, canGoForward);
                EnableWindow(m_toolbar->cancelWindow, FALSE);
                return S_OK;
            })
            .Get(),
        &m_navigationCompletedToken));
```

#### <span data-ttu-id="0a278-343">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="0a278-343">remove_NavigationCompleted</span></span> 

<span data-ttu-id="0a278-344">Supprimez un gestionnaire d’événements préalablement ajouté à add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="0a278-344">Remove an event handler previously added with add_NavigationCompleted.</span></span>

> <span data-ttu-id="0a278-345">[remove_NavigationCompleted](#remove_navigationcompleted)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="0a278-345">public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="0a278-346">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="0a278-346">add_FrameNavigationStarting</span></span> 

<span data-ttu-id="0a278-347">Ajoutez un gestionnaire d’événements pour l’événement FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="0a278-347">Add an event handler for the FrameNavigationStarting event.</span></span>

> <span data-ttu-id="0a278-348">[add_FrameNavigationStarting](#add_framenavigationstarting)par le biais du[mot de passe](IWebView2NavigationStartingEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="0a278-348">public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([IWebView2NavigationStartingEventHandler](IWebView2NavigationStartingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="0a278-349">FrameNavigationStarting se déclenche quand une Frame enfant du WebView demande une autorisation pour accéder à un URI différent.</span><span class="sxs-lookup"><span data-stu-id="0a278-349">FrameNavigationStarting fires when a child frame in the WebView requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="0a278-350">Cela se déclenche également pour les redirections.</span><span class="sxs-lookup"><span data-stu-id="0a278-350">This will fire for redirects as well.</span></span>

```cpp
    // Register a handler for the FrameNavigationStarting event.
    // This handler will prevent a frame from navigating to a blocked domain.
    CHECK_FAILURE(m_webView->add_FrameNavigationStarting(
        Callback<IWebView2NavigationStartingEventHandler>(
            [this](IWebView2WebView* sender,
                   IWebView2NavigationStartingEventArgs* args) -> HRESULT
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

#### <span data-ttu-id="0a278-351">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="0a278-351">remove_FrameNavigationStarting</span></span> 

<span data-ttu-id="0a278-352">Supprimez un gestionnaire d’événements préalablement ajouté à add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="0a278-352">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>

> <span data-ttu-id="0a278-353">[remove_FrameNavigationStarting](#remove_framenavigationstarting)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="0a278-353">public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="0a278-354">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="0a278-354">add_MoveFocusRequested</span></span> 

<span data-ttu-id="0a278-355">Ajoutez un gestionnaire d’événements pour l’événement MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="0a278-355">Add an event handler for the MoveFocusRequested event.</span></span>

> <span data-ttu-id="0a278-356">[add_MoveFocusRequested](#add_movefocusrequested)par le biais du[mot de passe](IWebView2MoveFocusRequestedEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="0a278-356">public HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([IWebView2MoveFocusRequestedEventHandler](IWebView2MoveFocusRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="0a278-357">MoveFocusRequested est déclenché lorsque l’utilisateur tente d’accéder à l’onglet du WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-357">MoveFocusRequested fires when user tries to tab out of the WebView.</span></span> <span data-ttu-id="0a278-358">Le focus du WebView n’a pas changé lors du déclenchement de cet événement.</span><span class="sxs-lookup"><span data-stu-id="0a278-358">The WebView's focus has not changed when this event is fired.</span></span>

```cpp
    // Register a handler for the MoveFocusRequested event.
    // This event will be fired when the user tabs out of the webview.
    // The handler will focus another window in the app, depending on which
    // direction the focus is being shifted.
    CHECK_FAILURE(m_webView->add_MoveFocusRequested(
        Callback<IWebView2MoveFocusRequestedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2MoveFocusRequestedEventArgs* args)
                -> HRESULT {
                if (!g_autoTabHandle)
                {
                    WEBVIEW2_MOVE_FOCUS_REASON reason;
                    CHECK_FAILURE(args->get_Reason(&reason));

                    if (reason == WEBVIEW2_MOVE_FOCUS_REASON_NEXT)
                    {
                        TabForwards(-1);
                    }
                    else if (reason == WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS)
                    {
                        TabBackwards(int(m_tabbableWindows.size()));
                    }
                    CHECK_FAILURE(args->put_Handled(TRUE));
                }
                return S_OK;
            })
            .Get(),
        &m_moveFocusRequestedToken));
```

#### <span data-ttu-id="0a278-359">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="0a278-359">remove_MoveFocusRequested</span></span> 

<span data-ttu-id="0a278-360">Supprimez un gestionnaire d’événements préalablement ajouté à add_MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="0a278-360">Remove an event handler previously added with add_MoveFocusRequested.</span></span>

> <span data-ttu-id="0a278-361">[remove_MoveFocusRequested](#remove_movefocusrequested)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="0a278-361">public HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="0a278-362">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="0a278-362">add_GotFocus</span></span> 

<span data-ttu-id="0a278-363">Ajoutez un gestionnaire d’événements pour l’événement GotFocus.</span><span class="sxs-lookup"><span data-stu-id="0a278-363">Add an event handler for the GotFocus event.</span></span>

> <span data-ttu-id="0a278-364">[add_GotFocus](#add_gotfocus)par le biais du[mot de passe](IWebView2FocusChangedEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="0a278-364">public HRESULT [add_GotFocus](#add_gotfocus)([IWebView2FocusChangedEventHandler](IWebView2FocusChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="0a278-365">GotFocus se déclenche lorsque WebView a le focus.</span><span class="sxs-lookup"><span data-stu-id="0a278-365">GotFocus fires when WebView got focus.</span></span>

#### <span data-ttu-id="0a278-366">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="0a278-366">remove_GotFocus</span></span> 

<span data-ttu-id="0a278-367">Supprimez un gestionnaire d’événements préalablement ajouté à add_GotFocus.</span><span class="sxs-lookup"><span data-stu-id="0a278-367">Remove an event handler previously added with add_GotFocus.</span></span>

> <span data-ttu-id="0a278-368">[remove_GotFocus](#remove_gotfocus)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="0a278-368">public HRESULT [remove_GotFocus](#remove_gotfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="0a278-369">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="0a278-369">add_LostFocus</span></span> 

<span data-ttu-id="0a278-370">Ajoutez un gestionnaire d’événements pour l’événement LostFocus.</span><span class="sxs-lookup"><span data-stu-id="0a278-370">Add an event handler for the LostFocus event.</span></span>

> <span data-ttu-id="0a278-371">[add_LostFocus](#add_lostfocus)par le biais du[mot de passe](IWebView2FocusChangedEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="0a278-371">public HRESULT [add_LostFocus](#add_lostfocus)([IWebView2FocusChangedEventHandler](IWebView2FocusChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="0a278-372">LostFocus se déclenche lorsque WebView perd le focus.</span><span class="sxs-lookup"><span data-stu-id="0a278-372">LostFocus fires when WebView lost focus.</span></span> <span data-ttu-id="0a278-373">Dans le cas où l’événement MoveFocusRequested est déclenché, le focus est toujours sur le WebView lors du déclenchement de l’événement MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="0a278-373">In the case where MoveFocusRequested event is fired, the focus is still on WebView when MoveFocusRequested event fires.</span></span> <span data-ttu-id="0a278-374">Le focus perdu ne se déclenche que lorsque le code de l’application ou l’action par défaut de l’événement MoveFocusRequested a défini le focus hors du WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-374">Lost focus only fires afterwards when app's code or default action of MoveFocusRequested event set focus away from WebView.</span></span>

#### <span data-ttu-id="0a278-375">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="0a278-375">remove_LostFocus</span></span> 

<span data-ttu-id="0a278-376">Supprimez un gestionnaire d’événements préalablement ajouté à add_LostFocus.</span><span class="sxs-lookup"><span data-stu-id="0a278-376">Remove an event handler previously added with add_LostFocus.</span></span>

> <span data-ttu-id="0a278-377">[remove_LostFocus](#remove_lostfocus)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="0a278-377">public HRESULT [remove_LostFocus](#remove_lostfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="0a278-378">add_WebResourceRequested_deprecated</span><span class="sxs-lookup"><span data-stu-id="0a278-378">add_WebResourceRequested_deprecated</span></span> 

<span data-ttu-id="0a278-379">Cette API est déconseillée, utilisez la nouvelle API add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="0a278-379">This API will be deprecated, please use the new add_WebResourceRequested API.</span></span>

> <span data-ttu-id="0a278-380">valeur de HRESULT publique [add_WebResourceRequested_deprecated](#add_webresourcerequested_deprecated)(LPCWSTR \* constante urlFilter,[WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context) \* constante resourceContextFilter, size_t filterLength,[IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* jeton)</span><span class="sxs-lookup"><span data-stu-id="0a278-380">public HRESULT [add_WebResourceRequested_deprecated](#add_webresourcerequested_deprecated)(LPCWSTR \*const urlFilter,[WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context) \*const resourceContextFilter,SIZE_T filterLength,[IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="0a278-381">Ajoutez un gestionnaire d’événements pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="0a278-381">Add an event handler for the WebResourceRequested event.</span></span> <span data-ttu-id="0a278-382">Se déclenche lorsque le WebView effectue une requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="0a278-382">Fires when the WebView has performs any HTTP request.</span></span> <span data-ttu-id="0a278-383">Utilisez urlFilter pour transmettre une liste avec la taille filterLength d’URL à écouter.</span><span class="sxs-lookup"><span data-stu-id="0a278-383">Use urlFilter to pass in a list with size filterLength of urls to listen for.</span></span> <span data-ttu-id="0a278-384">Chaque entrée d’URL prend également en charge les caractères génériques: ' \* 'correspond à zéro, un ou plusieurs caractères et «?» correspond exactement à un caractère.</span><span class="sxs-lookup"><span data-stu-id="0a278-384">Each url entry also supports wildcards: '\*' matches zero or more characters, and '?' matches exactly one character.</span></span> <span data-ttu-id="0a278-385">Pour chaque entrée de urlFilter, fournissez un resourceContextFilter correspondant qui représente les types de ressources pour lesquels WebResourceRequested doit se déclencher.</span><span class="sxs-lookup"><span data-stu-id="0a278-385">For each urlFilter entry, provide a matching resourceContextFilter representing the types of resources for which WebResourceRequested should fire.</span></span> <span data-ttu-id="0a278-386">Si filterLength est 0, l’événement est déclenché pour toutes les requêtes réseau.</span><span class="sxs-lookup"><span data-stu-id="0a278-386">If filterLength is 0, the event will fire for all network requests.</span></span> <span data-ttu-id="0a278-387">Les contextes de ressources pris en charge sont les suivants: document, StyleSheet, image, multimédia, police, script, XHR, Fetch.</span><span class="sxs-lookup"><span data-stu-id="0a278-387">The supported resource contexts are: Document, Stylesheet, Image, Media, Font, Script, XHR, Fetch.</span></span>

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<IWebView2WebResourceRequestedEventHandler>(
                    [this](
                        IWebView2WebView* sender,
                        IWebView2WebResourceRequestedEventArgs* args) {
                        wil::com_ptr<IWebView2WebResourceRequestedEventArgs2>
                            webResourceEventArgs2;
                        args->QueryInterface(IID_PPV_ARGS(&webResourceEventArgs2));
                        WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            webResourceEventArgs2->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<IWebView2WebResourceResponse> response;
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

#### <span data-ttu-id="0a278-388">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="0a278-388">remove_WebResourceRequested</span></span> 

<span data-ttu-id="0a278-389">Supprimez un gestionnaire d’événements préalablement ajouté à add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="0a278-389">Remove an event handler previously added with add_WebResourceRequested.</span></span>

> <span data-ttu-id="0a278-390">[remove_WebResourceRequested](#remove_webresourcerequested)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="0a278-390">public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="0a278-391">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="0a278-391">add_ScriptDialogOpening</span></span> 

<span data-ttu-id="0a278-392">Ajoutez un gestionnaire d’événements pour l’événement ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="0a278-392">Add an event handler for the ScriptDialogOpening event.</span></span>

> <span data-ttu-id="0a278-393">[add_ScriptDialogOpening](#add_scriptdialogopening)par le biais du[mot de passe](IWebView2ScriptDialogOpeningEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="0a278-393">public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="0a278-394">L’événement se déclenche quand une boîte de dialogue JavaScript (alerte, confirmation ou invite) s’affiche pour le WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-394">The event fires when a JavaScript dialog (alert, confirm, or prompt) will show for the webview.</span></span> <span data-ttu-id="0a278-395">Cet événement est déclenché uniquement si la propriété IWebView2Settings:: AreDefaultScriptDialogsEnabled est définie sur false.</span><span class="sxs-lookup"><span data-stu-id="0a278-395">This event only fires if the IWebView2Settings::AreDefaultScriptDialogsEnabled property is set to false.</span></span>

```cpp
    // Register a handler for the ScriptDialogOpening event.
    // This handler will set up a custom prompt dialog for the user,
    // and may defer the event if the setting to defer dialogs is enabled.
    CHECK_FAILURE(m_webView->add_ScriptDialogOpening(
        Callback<IWebView2ScriptDialogOpeningEventHandler>(
            [this](
                IWebView2WebView* sender,
                IWebView2ScriptDialogOpeningEventArgs* args) -> HRESULT
    {
        wil::com_ptr<IWebView2ScriptDialogOpeningEventArgs> eventArgs = args;
        auto showDialog = [this, eventArgs]
        {
            wil::unique_cotaskmem_string uri;
            WEBVIEW2_SCRIPT_DIALOG_KIND type;
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
                /* readonly */ type != WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT);
            if (dialog.confirmed)
            {
                CHECK_FAILURE(eventArgs->put_ResultText(dialog.input.c_str()));
                CHECK_FAILURE(eventArgs->Accept());
            }
        };

        if (m_deferScriptDialogs)
        {
            wil::com_ptr<IWebView2Deferral> deferral;
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

#### <span data-ttu-id="0a278-396">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="0a278-396">remove_ScriptDialogOpening</span></span> 

<span data-ttu-id="0a278-397">Supprimez un gestionnaire d’événements préalablement ajouté à add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="0a278-397">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>

> <span data-ttu-id="0a278-398">[remove_ScriptDialogOpening](#remove_scriptdialogopening)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="0a278-398">public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="0a278-399">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="0a278-399">add_ZoomFactorChanged</span></span> 

<span data-ttu-id="0a278-400">Ajoutez un gestionnaire d’événements pour l’événement ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="0a278-400">Add an event handler for the ZoomFactorChanged event.</span></span>

> <span data-ttu-id="0a278-401">[add_ZoomFactorChanged](#add_zoomfactorchanged)par le biais du[mot de passe](IWebView2ZoomFactorChangedEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="0a278-401">public HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([IWebView2ZoomFactorChangedEventHandler](IWebView2ZoomFactorChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="0a278-402">L’événement se déclenche lorsque la propriété ZoomFactor de l’élément WebView change.</span><span class="sxs-lookup"><span data-stu-id="0a278-402">The event fires when the ZoomFactor property of the WebView changes.</span></span> <span data-ttu-id="0a278-403">L’événement peut être déclenché en raison du fait que l’appelant a modifié la propriété ZoomFactor, ou en raison de l’utilisateur modifiant manuellement le zoom.</span><span class="sxs-lookup"><span data-stu-id="0a278-403">The event could fire because the caller modified the ZoomFactor property, or due to the user manually modifying the zoom.</span></span> <span data-ttu-id="0a278-404">Lorsqu’il est modifié par l’appelant par le biais de la propriété ZoomFactor, le facteur de zoom interne est mis à jour immédiatement et il n’y a pas d’événement ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="0a278-404">When it is modified by the caller via the ZoomFactor property, the internal zoom factor is updated immediately and there will be no ZoomFactorChanged event.</span></span> <span data-ttu-id="0a278-405">WebView associe le dernier facteur de zoom utilisé pour chaque site.</span><span class="sxs-lookup"><span data-stu-id="0a278-405">WebView associates the last used zoom factor for each site.</span></span> <span data-ttu-id="0a278-406">Par conséquent, il est possible de modifier le facteur de zoom lorsque vous naviguez vers une autre page.</span><span class="sxs-lookup"><span data-stu-id="0a278-406">Therefore, it is possible for the zoom factor to change when navigating to a different page.</span></span> <span data-ttu-id="0a278-407">Lorsque le facteur de zoom change en raison de cela, l’événement ZoomFactorChanged se déclenche immédiatement après l’événement DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="0a278-407">When the zoom factor changes due to this, the ZoomFactorChanged event fires right after the DocumentStateChanged event.</span></span>

```cpp
    // Register a handler for the ZoomFactorChanged event.
    // This handler just announces the new level of zoom on the window's title bar.
    CHECK_FAILURE(m_webView->add_ZoomFactorChanged(
        Callback<IWebView2ZoomFactorChangedEventHandler>(
            [this](IWebView2WebView* sender, IUnknown* args) -> HRESULT {
                double zoomFactor;
                CHECK_FAILURE(sender->get_ZoomFactor(&zoomFactor));

                std::wstring message = L"WebView2APISample (Zoom: " +
                                       std::to_wstring(int(zoomFactor * 100)) + L"%)";
                SetWindowText(m_appWindow->GetMainWindow(), message.c_str());
                return S_OK;
            })
            .Get(),
        &m_zoomFactorChangedToken));
```

#### <span data-ttu-id="0a278-408">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="0a278-408">remove_ZoomFactorChanged</span></span> 

<span data-ttu-id="0a278-409">Supprimez un gestionnaire d’événements préalablement ajouté à add_ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="0a278-409">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>

> <span data-ttu-id="0a278-410">[remove_ZoomFactorChanged](#remove_zoomfactorchanged)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="0a278-410">public HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="0a278-411">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="0a278-411">add_PermissionRequested</span></span> 

<span data-ttu-id="0a278-412">Ajoutez un gestionnaire d’événements pour l’événement PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="0a278-412">Add an event handler for the PermissionRequested event.</span></span>

> <span data-ttu-id="0a278-413">[add_PermissionRequested](#add_permissionrequested)par le biais du[mot de passe](IWebView2PermissionRequestedEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="0a278-413">public HRESULT [add_PermissionRequested](#add_permissionrequested)([IWebView2PermissionRequestedEventHandler](IWebView2PermissionRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="0a278-414">Se déclenche lorsque le contenu d’un WebView demande l’autorisation d’accéder à des ressources privilégiées.</span><span class="sxs-lookup"><span data-stu-id="0a278-414">Fires when content in a WebView requests permission to access some privileged resources.</span></span>

```cpp
    // Register a handler for the PermissionRequested event.
    // This handler prompts the user to allow or deny the request.
    CHECK_FAILURE(m_webView->add_PermissionRequested(
        Callback<IWebView2PermissionRequestedEventHandler>(
            [this](
                IWebView2WebView* sender,
                IWebView2PermissionRequestedEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        WEBVIEW2_PERMISSION_TYPE type = WEBVIEW2_PERMISSION_TYPE_UNKNOWN_PERMISSION;
        BOOL userInitiated = FALSE;

        CHECK_FAILURE(args->get_Uri(&uri));
        CHECK_FAILURE(args->get_PermissionType(&type));
        CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));

        std::wstring message = L"Do you want to grant permission for ";
        message += NameOfPermissionType(type);
        message += L" to the website at ";
        message += uri.get();
        message += L"?\n\n";
        message += (userInitiated
            ? L"This request came from a user gesture."
            : L"This request did not come from a user gesture.");

        int response = MessageBox(nullptr, message.c_str(), L"Permission Request",
                                   MB_YESNOCANCEL | MB_ICONWARNING);

        WEBVIEW2_PERMISSION_STATE state =
              response == IDYES ? WEBVIEW2_PERMISSION_STATE_ALLOW
            : response == IDNO  ? WEBVIEW2_PERMISSION_STATE_DENY
            :                     WEBVIEW2_PERMISSION_STATE_DEFAULT;
        CHECK_FAILURE(args->put_State(state));

        return S_OK;
    }).Get(), &m_permissionRequestedToken));
```

#### <span data-ttu-id="0a278-415">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="0a278-415">remove_PermissionRequested</span></span> 

<span data-ttu-id="0a278-416">Supprimez un gestionnaire d’événements préalablement ajouté à add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="0a278-416">Remove an event handler previously added with add_PermissionRequested.</span></span>

> <span data-ttu-id="0a278-417">[remove_PermissionRequested](#remove_permissionrequested)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="0a278-417">public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="0a278-418">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="0a278-418">add_ProcessFailed</span></span> 

<span data-ttu-id="0a278-419">Ajoutez un gestionnaire d’événements pour l’événement ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="0a278-419">Add an event handler for the ProcessFailed event.</span></span>

> <span data-ttu-id="0a278-420">[add_ProcessFailed](#add_processfailed)par le biais du[mot de passe](IWebView2ProcessFailedEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="0a278-420">public HRESULT [add_ProcessFailed](#add_processfailed)([IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="0a278-421">Se déclenche quand un processus WebView s’est arrêté de manière inattendue ou ne répond plus.</span><span class="sxs-lookup"><span data-stu-id="0a278-421">Fires when a WebView process terminated unexpectedly or become unresponsive.</span></span>

```cpp
    // Register a handler for the ProcessFailed event.
    // This handler checks if the browser process failed, and asks the user if
    // they want to recreate the webview.
    CHECK_FAILURE(m_webView->add_ProcessFailed(
        Callback<IWebView2ProcessFailedEventHandler>(
            [this](IWebView2WebView* sender,
                IWebView2ProcessFailedEventArgs* args) -> HRESULT
    {
        WEBVIEW2_PROCESS_FAILED_KIND failureType;
        CHECK_FAILURE(args->get_ProcessFailedKind(&failureType));
        if (failureType == WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED)
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
        return S_OK;
    }).Get(), &m_processFailedToken));
```

#### <span data-ttu-id="0a278-422">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="0a278-422">remove_ProcessFailed</span></span> 

<span data-ttu-id="0a278-423">Supprimez un gestionnaire d’événements préalablement ajouté à add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="0a278-423">Remove an event handler previously added with add_ProcessFailed.</span></span>

> <span data-ttu-id="0a278-424">[remove_ProcessFailed](#remove_processfailed)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="0a278-424">public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="0a278-425">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="0a278-425">AddScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="0a278-426">Ajoutez le code JavaScript fourni à une liste de scripts qui doivent être exécutés après la création de l’objet global, mais avant l’analyse du document HTML et avant l’exécution de tout autre script fourni par le document HTML.</span><span class="sxs-lookup"><span data-stu-id="0a278-426">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>

> <span data-ttu-id="0a278-427">public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR JavaScript, gestionnaire[IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) \*)</span><span class="sxs-lookup"><span data-stu-id="0a278-427">public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript,[IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="0a278-428">Le script injecté s’applique à tous les futurs documents de niveau supérieur et navigation de Frame enfant jusqu’à sa suppression avec RemoveScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="0a278-428">The injected script will apply to all future top level document and child frame navigations until removed with RemoveScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="0a278-429">Cette opération est appliquée de manière asynchrone et vous devez attendre que le gestionnaire d’achèvement s’exécute avant de vérifier que le script est prêt à être exécuté sur de futurs navigations.</span><span class="sxs-lookup"><span data-stu-id="0a278-429">This is applied asynchronously and you must wait for the completion handler to run before you can be sure that the script is ready to execute on future navigations.</span></span>

<span data-ttu-id="0a278-430">Notez que si un document HTML comporte un sandbox d’un type quelconque via les propriétés [sandbox](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) ou l' [en-tête HTTP Content-Security-Policy](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) , ce dernier affectera l’exécution du script.</span><span class="sxs-lookup"><span data-stu-id="0a278-430">Note that if an HTML document has sandboxing of some kind via [sandbox](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) properties or the [Content-Security-Policy HTTP header](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) this will affect the script run here.</span></span> <span data-ttu-id="0a278-431">Par exemple, si le mot clé «allow-modaux» n’est pas défini, les appels à la `alert` fonction seront ignorés.</span><span class="sxs-lookup"><span data-stu-id="0a278-431">So, for example, if the 'allow-modals' keyword is not set then calls to the `alert` function will be ignored.</span></span>

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
            Callback<IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler>(
                [this](HRESULT error, PCWSTR id) -> HRESULT
        {
            m_lastInitializeScriptId = id;
            MessageBox(nullptr, id, L"AddScriptToExecuteOnDocumentCreated Id", MB_OK);
            return S_OK;
        }).Get());

    }
}
```

#### <span data-ttu-id="0a278-432">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="0a278-432">RemoveScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="0a278-433">Supprimez le JavaScript correspondant ajouté par le biais de AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="0a278-433">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>

> <span data-ttu-id="0a278-434">public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(ID LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="0a278-434">public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR id)</span></span>

#### <span data-ttu-id="0a278-435">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="0a278-435">ExecuteScript</span></span> 

<span data-ttu-id="0a278-436">Exécutez le code JavaScript du paramètre JavaScript du document de niveau supérieur actuel affiché dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-436">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="0a278-437">public HRESULT [ExecuteScript](#executescript)(LPCWSTR JavaScript, gestionnaire[IWebView2ExecuteScriptCompletedHandler](IWebView2ExecuteScriptCompletedHandler.md) \*)</span><span class="sxs-lookup"><span data-stu-id="0a278-437">public HRESULT [ExecuteScript](#executescript)(LPCWSTR javaScript,[IWebView2ExecuteScriptCompletedHandler](IWebView2ExecuteScriptCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="0a278-438">Cela s’exécute de manière asynchrone et, si un gestionnaire est fourni dans le paramètre ExecuteScriptCompletedHandler, sa méthode Invoke est appelée avec le résultat de l’évaluation du JavaScript fourni.</span><span class="sxs-lookup"><span data-stu-id="0a278-438">This will execute asynchronously and when complete, if a handler is provided in the ExecuteScriptCompletedHandler parameter, its Invoke method will be called with the result of evaluating the provided JavaScript.</span></span> <span data-ttu-id="0a278-439">La valeur de résultat est une chaîne codée au format JSON.</span><span class="sxs-lookup"><span data-stu-id="0a278-439">The result value is a JSON encoded string.</span></span> <span data-ttu-id="0a278-440">Si le résultat n’est pas défini, contient un cycle de référence ou ne peut pas être encodé dans JSON, la valeur null JSON sera renvoyée comme chaîne «NULL».</span><span class="sxs-lookup"><span data-stu-id="0a278-440">If the result is undefined, contains a reference cycle, or otherwise cannot be encoded into JSON, the JSON null value will be returned as the string 'null'.</span></span> <span data-ttu-id="0a278-441">Notez qu’une fonction qui ne contient aucune valeur de retour explicite renvoie une valeur non définie.</span><span class="sxs-lookup"><span data-stu-id="0a278-441">Note that a function that has no explicit return value returns undefined.</span></span> <span data-ttu-id="0a278-442">Si le script exécuté lève une exception non gérée, le résultat est également «null».</span><span class="sxs-lookup"><span data-stu-id="0a278-442">If the executed script throws an unhandled exception, then the result is also 'null'.</span></span> <span data-ttu-id="0a278-443">Cette méthode est appliquée de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="0a278-443">This method is applied asynchronously.</span></span> <span data-ttu-id="0a278-444">Si l’appel est effectué alors que le WebView est sur un document et qu’une navigation se produit après la fin de l’appel, mais avant l’exécution du JavaScript, le script ne sera pas exécuté et le gestionnaire sera appelé avec E_FAIL pour son paramètre codeerreur.</span><span class="sxs-lookup"><span data-stu-id="0a278-444">If the call is made while the webview is on one document, and a navigation occurs after the call is made but before the JavaScript is executed, then the script will not be executed and the handler will be called with E_FAIL for its errorCode parameter.</span></span> <span data-ttu-id="0a278-445">ExecuteScript fonctionne même si IsScriptEnabled est défini sur FALSe.</span><span class="sxs-lookup"><span data-stu-id="0a278-445">ExecuteScript will work even if IsScriptEnabled is set to FALSE.</span></span>

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
            Callback<IWebView2ExecuteScriptCompletedHandler>(
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

#### <span data-ttu-id="0a278-446">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="0a278-446">CapturePreview</span></span> 

<span data-ttu-id="0a278-447">Capturez une image de l’affichage du WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-447">Capture an image of what WebView is displaying.</span></span>

> <span data-ttu-id="0a278-448">public HRESULT [CapturePreview](#capturepreview)([WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format) ImageFormat, IStream \* ImageStream, gestionnaire[IWebView2CapturePreviewCompletedHandler](IWebView2CapturePreviewCompletedHandler.md) \*)</span><span class="sxs-lookup"><span data-stu-id="0a278-448">public HRESULT [CapturePreview](#capturepreview)([WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format) imageFormat,IStream \* imageStream,[IWebView2CapturePreviewCompletedHandler](IWebView2CapturePreviewCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="0a278-449">Spécifiez le format de l’image avec le paramètre imageFormat.</span><span class="sxs-lookup"><span data-stu-id="0a278-449">Specify the format of the image with the imageFormat parameter.</span></span> <span data-ttu-id="0a278-450">Les données binaires d’image obtenues sont écrites dans le paramètre imageStream fourni.</span><span class="sxs-lookup"><span data-stu-id="0a278-450">The resulting image binary data is written to the provided imageStream parameter.</span></span> <span data-ttu-id="0a278-451">Lorsque CapturePreview finit d’écrire dans le flux, la méthode Invoke du paramètre de gestionnaire fourni est appelée.</span><span class="sxs-lookup"><span data-stu-id="0a278-451">When CapturePreview finishes writing to the stream, the Invoke method on the provided handler parameter is called.</span></span>

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
            WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG, stream.get(),
            Callback<IWebView2CapturePreviewCompletedHandler>(
                [mainWindow](HRESULT error_code) -> HRESULT {
                    CHECK_FAILURE(error_code);

                    MessageBox(mainWindow, L"Preview Captured", L"Preview Captured", MB_OK);
                    return S_OK;
                })
                .Get()));
    }
}
```

#### <span data-ttu-id="0a278-452">Recharger</span><span class="sxs-lookup"><span data-stu-id="0a278-452">Reload</span></span> 

<span data-ttu-id="0a278-453">Recharger la page active.</span><span class="sxs-lookup"><span data-stu-id="0a278-453">Reload the current page.</span></span>

> <span data-ttu-id="0a278-454">[rechargement](#reload)du HRESULT public ()</span><span class="sxs-lookup"><span data-stu-id="0a278-454">public HRESULT [Reload](#reload)()</span></span>

<span data-ttu-id="0a278-455">Il s’agit de la même façon que d’accéder à l’URI du document de niveau supérieur actuel, y compris tous les événements de navigation déclenchant et respectant les entrées dans le cache HTTP.</span><span class="sxs-lookup"><span data-stu-id="0a278-455">This is similar to navigating to the URI of current top level document including all navigation events firing and respecting any entries in the HTTP cache.</span></span> <span data-ttu-id="0a278-456">Toutefois, l’historique en arrière-plan ne sera pas modifié.</span><span class="sxs-lookup"><span data-stu-id="0a278-456">But, the back/forward history will not be modified.</span></span>

#### <span data-ttu-id="0a278-457">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="0a278-457">get_Bounds</span></span> 

<span data-ttu-id="0a278-458">Les limites de l’affichage WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-458">The webview bounds.</span></span>

> <span data-ttu-id="0a278-459">[get_Boundss](#get_bounds)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="0a278-459">public HRESULT [get_Bounds](#get_bounds)(RECT \* bounds)</span></span>

<span data-ttu-id="0a278-460">Les limites sont relatives au HWND parent.</span><span class="sxs-lookup"><span data-stu-id="0a278-460">Bounds are relative to the parent HWND.</span></span> <span data-ttu-id="0a278-461">L’application peut positionner un WebView de deux manières:</span><span class="sxs-lookup"><span data-stu-id="0a278-461">The app has two ways it can position a WebView:</span></span>

1. <span data-ttu-id="0a278-462">Créer un HWND enfant qui est le HWND parent WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-462">Create a child HWND that is the WebView parent HWND.</span></span> <span data-ttu-id="0a278-463">Positionnez cette fenêtre dans laquelle le WebView devrait être.</span><span class="sxs-lookup"><span data-stu-id="0a278-463">Position this window where the WebView should be.</span></span> <span data-ttu-id="0a278-464">Dans le cas présent, utilisez (0, 0) pour le coin supérieur gauche de la vue de Bound’s (offset).</span><span class="sxs-lookup"><span data-stu-id="0a278-464">In this case, use (0, 0) for the WebView's Bound's top left corner (the offset).</span></span>

1. <span data-ttu-id="0a278-465">Utilisez la plus grande fenêtre de l’application en tant que HWND parent d’affichage.</span><span class="sxs-lookup"><span data-stu-id="0a278-465">Use the app's top most window as the WebView parent HWND.</span></span> <span data-ttu-id="0a278-466">Définissez le coin supérieur gauche de l’Bound’s WebView de sorte que le contrôle WebView soit correctement positionné dans l’application.</span><span class="sxs-lookup"><span data-stu-id="0a278-466">Set the WebView's Bound's top left corner so that the WebView is positioned correctly in the app.</span></span> <span data-ttu-id="0a278-467">Les valeurs de limites se trouvent dans l’espace de coordonnées de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="0a278-467">The Bound's values are in the host's coordinate space.</span></span>

#### <span data-ttu-id="0a278-468">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="0a278-468">put_Bounds</span></span> 

<span data-ttu-id="0a278-469">Définissez la propriété Bounds.</span><span class="sxs-lookup"><span data-stu-id="0a278-469">Set the Bounds property.</span></span>

> <span data-ttu-id="0a278-470">[put_Bounds](#put_bounds)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="0a278-470">public HRESULT [put_Bounds](#put_bounds)(RECT bounds)</span></span>

```cpp
// Update the bounds of the WebView window to fit available space.
void ViewComponent::ResizeWebView()
{
    RECT desiredBounds = m_webViewBounds;
    desiredBounds.bottom = LONG(
        (m_webViewBounds.bottom - m_webViewBounds.top) * m_webViewRatio + m_webViewBounds.top);
    desiredBounds.right = LONG(
        (m_webViewBounds.right - m_webViewBounds.left) * m_webViewRatio + m_webViewBounds.left);

    m_webView->put_Bounds(desiredBounds);
}
```

#### <span data-ttu-id="0a278-471">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="0a278-471">get_ZoomFactor</span></span> 

<span data-ttu-id="0a278-472">Facteur de zoom pour la page active dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-472">The zoom factor for the current page in the WebView.</span></span>

> <span data-ttu-id="0a278-473">valeur publique HRESULT [get_ZoomFactor](#get_zoomfactor)(double \* ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="0a278-473">public HRESULT [get_ZoomFactor](#get_zoomfactor)(double \* zoomFactor)</span></span>

<span data-ttu-id="0a278-474">Le facteur de zoom est conservé par site.</span><span class="sxs-lookup"><span data-stu-id="0a278-474">The zoom factor is persisted per site.</span></span> <span data-ttu-id="0a278-475">Notez que la modification du facteur de zoom peut entraîner la modification de la `window.innerWidth/innerHeight` mise en page.</span><span class="sxs-lookup"><span data-stu-id="0a278-475">Note that changing zoom factor could cause `window.innerWidth/innerHeight` and page layout to change.</span></span> <span data-ttu-id="0a278-476">Lorsque WebView accède à une page d’un site différent, le facteur de zoom défini pour la page précédente ne sera pas appliqué.</span><span class="sxs-lookup"><span data-stu-id="0a278-476">When WebView navigates to a page from a different site, the zoom factor set for the previous page will not be applied.</span></span> <span data-ttu-id="0a278-477">Si l’application veut définir le facteur de zoom pour une page spécifique, l’emplacement le plus ancien est le dans le gestionnaire d’événements DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="0a278-477">If the app wants to set the zoom factor for a certain page, the earliest place to do it is in the DocumentStateChanged event handler.</span></span> <span data-ttu-id="0a278-478">Notez que, si tel est le cas, il peut recevoir un événement ZoomFactorChanged pour le facteur de zoom persistant avant de recevoir l’événement ZoomFactorChanged pour le facteur de zoom spécifié.</span><span class="sxs-lookup"><span data-stu-id="0a278-478">Note that if it does that, it might receive a ZoomFactorChanged event for the persisted zoom factor before receiving the ZoomFactorChanged event for the specified zoom factor.</span></span> <span data-ttu-id="0a278-479">La spécification d’un zoomFactor inférieur ou égal à 0 n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="0a278-479">Specifying a zoomFactor less than or equal to 0 is not allowed.</span></span> <span data-ttu-id="0a278-480">WebView possède également une plage de facteur de zoom prise en charge interne.</span><span class="sxs-lookup"><span data-stu-id="0a278-480">WebView also has an internal supported zoom factor range.</span></span> <span data-ttu-id="0a278-481">Lorsque le facteur de zoom spécifié est en dehors de cette plage, il est normalisé pour être dans la plage et un événement ZoomFactorChanged est déclenché pour le facteur de zoom réel appliqué.</span><span class="sxs-lookup"><span data-stu-id="0a278-481">When a specified zoom factor is out of that range, it will be normalized to be within the range, and a ZoomFactorChanged event will be fired for the real applied zoom factor.</span></span> <span data-ttu-id="0a278-482">Lorsque cette situation se produit, la propriété ZoomFactor indique le facteur de zoom spécifié lors de la modification précédente de la propriété ZoomFactor jusqu’à ce que l’événement ZoomFactorChanged soit reçu lorsque WebView applique le facteur de zoom normalisé.</span><span class="sxs-lookup"><span data-stu-id="0a278-482">When this range normalization happens, the ZoomFactor property will report the zoom factor specified during the previous modification of the ZoomFactor property until the ZoomFactorChanged event is received after webview applies the normalized zoom factor.</span></span>

#### <span data-ttu-id="0a278-483">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="0a278-483">put_ZoomFactor</span></span> 

<span data-ttu-id="0a278-484">Définissez la propriété ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="0a278-484">Set the ZoomFactor property.</span></span>

> <span data-ttu-id="0a278-485">[put_ZoomFactor](#put_zoomfactor)par le biais du public HRESULT (double ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="0a278-485">public HRESULT [put_ZoomFactor](#put_zoomfactor)(double zoomFactor)</span></span>

#### <span data-ttu-id="0a278-486">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="0a278-486">get_IsVisible</span></span> 

<span data-ttu-id="0a278-487">La propriété IsVisible détermine s’il faut afficher ou masquer le WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-487">The IsVisible property determines whether to show or hide the webview.</span></span>

> <span data-ttu-id="0a278-488">valeur publique HRESULT [get_IsVisible](#get_isvisible)(bool \* IsVisible)</span><span class="sxs-lookup"><span data-stu-id="0a278-488">public HRESULT [get_IsVisible](#get_isvisible)(BOOL \* isVisible)</span></span>

<span data-ttu-id="0a278-489">Si la valeur de l’argument IsVisible est définie sur false, le WebView sera transparent et ne sera pas affiché.</span><span class="sxs-lookup"><span data-stu-id="0a278-489">If IsVisible is set to false, the webview will be transparent and will not be rendered.</span></span> <span data-ttu-id="0a278-490">Toutefois, cela n’affecte pas la fenêtre qui contient le WebView (le paramètre HWND transmis à CreateWebView).</span><span class="sxs-lookup"><span data-stu-id="0a278-490">However, this will not affect the window containing the webview (the HWND parameter that was passed to CreateWebView).</span></span> <span data-ttu-id="0a278-491">Si vous souhaitez que cette fenêtre disparaisse également, appelez la fonction ShowWindow sur celle-ci directement en plus de modifier la propriété IsVisible.</span><span class="sxs-lookup"><span data-stu-id="0a278-491">If you want that window to disappear too, call ShowWindow on it directly in addition to modifying the IsVisible property.</span></span> <span data-ttu-id="0a278-492">Le mode webaffichage sous forme de fenêtre enfant ne recevra pas de messages de fenêtre lorsque la fenêtre supérieure est réduite ou restaurée.</span><span class="sxs-lookup"><span data-stu-id="0a278-492">WebView as a child window won't get window messages when the top window is minimized or restored.</span></span> <span data-ttu-id="0a278-493">Pour des raisons de performances, le développeur doit définir la propriété IsVisible du WebView sur false lorsque la fenêtre de l’application est réduite, puis revenir à la valeur true lorsque la fenêtre de l’application est restaurée.</span><span class="sxs-lookup"><span data-stu-id="0a278-493">For performance reason, developer should set IsVisible property of the WebView to false when the app window is minimized and back to true when app window is restored.</span></span> <span data-ttu-id="0a278-494">Pour cela, la fenêtre de l’application peut gérer les SC_MINIMIZE et de SC_RESTORE commande lors de la réception d’WM_SYSCOMMAND message.</span><span class="sxs-lookup"><span data-stu-id="0a278-494">App window can do this by handling SC_MINIMIZE and SC_RESTORE command upon receiving WM_SYSCOMMAND message.</span></span>

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_webView->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_webView->put_IsVisible(m_isVisible);
}
```

#### <span data-ttu-id="0a278-495">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="0a278-495">put_IsVisible</span></span> 

<span data-ttu-id="0a278-496">Définissez la propriété IsVisible.</span><span class="sxs-lookup"><span data-stu-id="0a278-496">Set the IsVisible property.</span></span>

> <span data-ttu-id="0a278-497">valeur HRESULT publique [put_IsVisible](#put_isvisible)(bool IsVisible)</span><span class="sxs-lookup"><span data-stu-id="0a278-497">public HRESULT [put_IsVisible](#put_isvisible)(BOOL isVisible)</span></span>

```cpp
    if (message == WM_SYSCOMMAND)
    {
        if (wParam == SC_MINIMIZE)
        {
            // Hide the webview when the app window is minimized.
            m_webView->put_IsVisible(FALSE);
        }
        else if (wParam == SC_RESTORE)
        {
            // When the app window is restored, show the webview
            // (unless the user has toggle visibility off).
            if (m_isVisible)
            {
                m_webView->put_IsVisible(TRUE);
            }
        }
    }
```

#### <span data-ttu-id="0a278-498">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="0a278-498">PostWebMessageAsJson</span></span> 

<span data-ttu-id="0a278-499">Publiez le WebMessage spécifié dans le document de niveau supérieur de cette [IWebView2WebView]().</span><span class="sxs-lookup"><span data-stu-id="0a278-499">Post the specified webMessage to the top level document in this [IWebView2WebView]().</span></span>

> <span data-ttu-id="0a278-500">public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="0a278-500">public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span></span>

<span data-ttu-id="0a278-501">Le document de niveau supérieur de la fenêtre du document. chrome. WebView est déclenché.</span><span class="sxs-lookup"><span data-stu-id="0a278-501">The top level document's window.chrome.webview's message event fires.</span></span> <span data-ttu-id="0a278-502">JavaScript dans ce document est susceptible de s’abonner à l’événement et de s’en désabonner via la commande suivante:</span><span class="sxs-lookup"><span data-stu-id="0a278-502">JavaScript in that document may subscribe and unsubscribe to the event via the following:</span></span> 

```cpp
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

 <span data-ttu-id="0a278-503">Les arguments d’événement sont une instance de `MessageEvent` .</span><span class="sxs-lookup"><span data-stu-id="0a278-503">The event args is an instance of `MessageEvent`.</span></span> <span data-ttu-id="0a278-504">Le paramètre IWebView2Settings:: IsWebMessageEnabled doit avoir la valeur true, ou cette méthode échoue avec E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="0a278-504">The IWebView2Settings::IsWebMessageEnabled setting must be true or this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="0a278-505">La propriété Data du arg est le paramètre de chaîne WebMessage électronique analysé comme chaîne JSON dans un objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0a278-505">The event arg's data property is the webMessage string parameter parsed as a JSON string into a JavaScript object.</span></span> <span data-ttu-id="0a278-506">La propriété source de l’objet Event est une référence à l' `window.chrome.webview` objet.</span><span class="sxs-lookup"><span data-stu-id="0a278-506">The event arg's source property is a reference to the `window.chrome.webview` object.</span></span> <span data-ttu-id="0a278-507">Pour plus d’informations sur l’envoi de messages à partir du document HTML du WebView vers l’hôte, voir SetWebMessageReceivedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="0a278-507">See SetWebMessageReceivedEventHandler for information on sending messages from the HTML document in the webview to the host.</span></span> <span data-ttu-id="0a278-508">Ce message est envoyé de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="0a278-508">This message is sent asynchronously.</span></span> <span data-ttu-id="0a278-509">Si une navigation se produit avant que le message ne soit publié sur la page, le message ne sera pas envoyé.</span><span class="sxs-lookup"><span data-stu-id="0a278-509">If a navigation occurs before the message is posted to the page, then the message will not be sent.</span></span>

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<IWebView2WebMessageReceivedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->get_WebMessageAsString(&messageRaw));
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

#### <span data-ttu-id="0a278-510">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="0a278-510">PostWebMessageAsString</span></span> 

<span data-ttu-id="0a278-511">Il s’agit d’un programme d’assistance pour publier un message qui est une chaîne simple plutôt qu’une représentation de chaîne JSON d’un objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0a278-511">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>

> <span data-ttu-id="0a278-512">public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="0a278-512">public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span></span>

<span data-ttu-id="0a278-513">Ce comportement se comporte exactement de la même façon que PostWebMessageAsJson, mais la `window.chrome.webview` propriété Data de arg du message est une chaîne ayant la même valeur que webMessageAsString.</span><span class="sxs-lookup"><span data-stu-id="0a278-513">This behaves in exactly the same manner as PostWebMessageAsJson but the `window.chrome.webview` message event arg's data property will be a string with the same value as webMessageAsString.</span></span> <span data-ttu-id="0a278-514">Utilisez cette fonction au lieu de PostWebMessageAsJson si vous souhaitez communiquer via des chaînes simples plutôt que des objets JSON.</span><span class="sxs-lookup"><span data-stu-id="0a278-514">Use this instead of PostWebMessageAsJson if you want to communicate via simple strings rather than JSON objects.</span></span>

#### <span data-ttu-id="0a278-515">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="0a278-515">add_WebMessageReceived</span></span> 

<span data-ttu-id="0a278-516">Cet événement se déclenche lorsque le paramètre IsWebMessageEnabled est défini et au document de niveau supérieur des appels WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="0a278-516">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>

> <span data-ttu-id="0a278-517">[add_WebMessageReceived](#add_webmessagereceived)par le biais[IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="0a278-517">public HRESULT [add_WebMessageReceived](#add_webmessagereceived)([IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) \* handler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="0a278-518">La fonction postMessage est l' `void postMessage(object)` emplacement de tout objet pris en charge par la conversion JSON.</span><span class="sxs-lookup"><span data-stu-id="0a278-518">The postMessage function is `void postMessage(object)` where object is any object supported by JSON conversion.</span></span>

```cpp
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

 <span data-ttu-id="0a278-519">Lorsque postMessage est appelée, le [IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) défini par le biais de cette méthode SetWebMessageReceivedEventHandler sera appelé avec le paramètre objet de PostMessage converti en chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="0a278-519">When postMessage is called, the [IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) set via this SetWebMessageReceivedEventHandler method will be invoked with the postMessage's object parameter converted to a JSON string.</span></span>

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<IWebView2WebMessageReceivedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->get_WebMessageAsString(&messageRaw));
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

#### <span data-ttu-id="0a278-520">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="0a278-520">remove_WebMessageReceived</span></span> 

<span data-ttu-id="0a278-521">Supprimez un gestionnaire d’événements préalablement ajouté à add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="0a278-521">Remove an event handler previously added with add_WebMessageReceived.</span></span>

> <span data-ttu-id="0a278-522">[remove_WebMessageReceived](#remove_webmessagereceived)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="0a278-522">public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="0a278-523">Fermer</span><span class="sxs-lookup"><span data-stu-id="0a278-523">Close</span></span> 

<span data-ttu-id="0a278-524">Ferme le WebView et nettoie l’instance de navigateur sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="0a278-524">Closes the webview and cleans up the underlying browser instance.</span></span>

> <span data-ttu-id="0a278-525">valeur publique [HRESULT (](#close))</span><span class="sxs-lookup"><span data-stu-id="0a278-525">public HRESULT [Close](#close)()</span></span>

<span data-ttu-id="0a278-526">Le nettoyage de l’option de suppression de navigateur entraîne la mise à jour des ressources par le biais du WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-526">Cleaning up the browser instace will release the resources powering the webview.</span></span> <span data-ttu-id="0a278-527">L’instance du navigateur sera arrêtée s’il n’y a aucune autre WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-527">The browser instance will be shut down if there are no other webviews using it.</span></span>

<span data-ttu-id="0a278-528">Après avoir appelé Close, tous les appels de méthode échouent et les gestionnaires d’événements cessent de se déclencher.</span><span class="sxs-lookup"><span data-stu-id="0a278-528">After calling Close, all method calls will fail and event handlers will stop firing.</span></span> <span data-ttu-id="0a278-529">Plus précisément, le WebView publie ses références à ses gestionnaires d’événements lorsque la méthode Close est appelée.</span><span class="sxs-lookup"><span data-stu-id="0a278-529">Specifically, the WebView will release its references to its event handlers when Close is called.</span></span>

<span data-ttu-id="0a278-530">Close est appelé implicitement lorsque le WebView perd sa référence finale et est détruit.</span><span class="sxs-lookup"><span data-stu-id="0a278-530">Close is implicitly called when the WebView loses its final reference and is destructed.</span></span> <span data-ttu-id="0a278-531">Mais il est conseillé d’appeler explicitement Close pour éviter tout cycle accidentel de références entre le WebView et le code de l’application.</span><span class="sxs-lookup"><span data-stu-id="0a278-531">But it is best practice to explicitly call Close to avoid any accidental cycle of references between the WebView and the app code.</span></span> <span data-ttu-id="0a278-532">En particulier, si vous capturez une référence à WebView dans un gestionnaire d’événements, vous créerez un cycle de référence entre le WebView et le gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="0a278-532">Specifically, if you capture a reference to the WebView in an event handler you will create a reference cycle between the WebView and the event handler.</span></span> <span data-ttu-id="0a278-533">La fermeture rompt ce cycle en libérant tous les gestionnaires d’événements.</span><span class="sxs-lookup"><span data-stu-id="0a278-533">Close will break this cycle by releasing all event handlers.</span></span> <span data-ttu-id="0a278-534">Néanmoins, pour éviter ce problème, il est préférable d’appeler explicitement la fermeture sur le WebView et de ne pas capturer de référence à WebView pour s’assurer que le WebView peut être nettoyé correctement.</span><span class="sxs-lookup"><span data-stu-id="0a278-534">But to avoid this situation it is best practice to both explicitly call Close on the WebView and to not capture a reference to the WebView to ensure the WebView can be cleaned up correctly.</span></span>

```cpp
// Close the WebView and deinitialize related state. This doesn't close the app window.
void AppWindow::CloseWebView()
{
    DeleteAllComponents();
    if (m_webView)
    {
        m_webView->Close();
        m_webView = nullptr;
    }
    m_webViewEnvironment = nullptr;
}
```

#### <span data-ttu-id="0a278-535">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="0a278-535">CallDevToolsProtocolMethod</span></span> 

<span data-ttu-id="0a278-536">Appelez une méthode DevToolsProtocol asynchrone.</span><span class="sxs-lookup"><span data-stu-id="0a278-536">Call an asynchronous DevToolsProtocol method.</span></span>

> <span data-ttu-id="0a278-537">public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR METHODNAME, LPCWSTR parametersAsJson, gestionnaire[IWebView2CallDevToolsProtocolMethodCompletedHandler](IWebView2CallDevToolsProtocolMethodCompletedHandler.md) \*)</span><span class="sxs-lookup"><span data-stu-id="0a278-537">public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR methodName,LPCWSTR parametersAsJson,[IWebView2CallDevToolsProtocolMethodCompletedHandler](IWebView2CallDevToolsProtocolMethodCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="0a278-538">Voir la [visionneuse de protocoles devtools](https://aka.ms/DevToolsProtocolDocs) pour obtenir une liste et une description des méthodes disponibles.</span><span class="sxs-lookup"><span data-stu-id="0a278-538">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list and description of available methods.</span></span> <span data-ttu-id="0a278-539">Le paramètre methodName est le nom complet de la méthode au format `{domain}.{method}` .</span><span class="sxs-lookup"><span data-stu-id="0a278-539">The methodName parameter is the full name of the method in the format `{domain}.{method}`.</span></span> <span data-ttu-id="0a278-540">Le paramètre parametersAsJson est une chaîne au format JSON contenant les paramètres de la méthode correspondante.</span><span class="sxs-lookup"><span data-stu-id="0a278-540">The parametersAsJson parameter is a JSON formatted string containing the parameters for the corresponding method.</span></span> <span data-ttu-id="0a278-541">La méthode Invoke du gestionnaire est appelée lorsque la méthode est terminée de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="0a278-541">The handler's Invoke method will be called when the method asynchronously completes.</span></span> <span data-ttu-id="0a278-542">Invoke sera appelé avec l’objet de retour de la méthode sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="0a278-542">Invoke will be called with the method's return object as a JSON string.</span></span>

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
            Callback<IWebView2CallDevToolsProtocolMethodCompletedHandler>(
                [](HRESULT error, PCWSTR resultJson) -> HRESULT
                {
                    MessageBox(nullptr, resultJson, L"CDP Method Result", MB_OK);
                    return S_OK;
                }).Get());
    }
}
```

#### <span data-ttu-id="0a278-543">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="0a278-543">add_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="0a278-544">S’abonner à un événement DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="0a278-544">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="0a278-545">valeur de HRESULT publique [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)(LPCWSTR NomÉvénement, gestionnaire[IWebView2DevToolsProtocolEventReceivedEventHandler](IWebView2DevToolsProtocolEventReceivedEventHandler.md) \*, jeton EventRegistrationToken \*)</span><span class="sxs-lookup"><span data-stu-id="0a278-545">public HRESULT [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)(LPCWSTR eventName,[IWebView2DevToolsProtocolEventReceivedEventHandler](IWebView2DevToolsProtocolEventReceivedEventHandler.md) \* handler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="0a278-546">Voir la [visionneuse de protocoles devtools](https://aka.ms/DevToolsProtocolDocs) pour obtenir une liste et une description des événements disponibles.</span><span class="sxs-lookup"><span data-stu-id="0a278-546">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list and description of available events.</span></span> <span data-ttu-id="0a278-547">Le paramètre eventName est le nom complet de l’événement au format `{domain}.{event}` .</span><span class="sxs-lookup"><span data-stu-id="0a278-547">The eventName parameter is the full name of the event in the format `{domain}.{event}`.</span></span> <span data-ttu-id="0a278-548">La méthode Invoke du gestionnaire est appelée chaque fois que l’événement DevToolsProtocol correspondant est déclenché.</span><span class="sxs-lookup"><span data-stu-id="0a278-548">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="0a278-549">Invoke sera appelé à l’aide d’un objet args d’événement contenant l’objet de paramètre de l’événement CDP en tant que chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="0a278-549">Invoke will be called with the an event args object containing the CDP event's parameter object as a JSON string.</span></span>

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
        // If we are already subscribed to this event, unsubscribe first.
        auto preexistingToken = m_devToolsProtocolEventReceivedTokenMap.find(eventName);
        if (preexistingToken != m_devToolsProtocolEventReceivedTokenMap.end())
        {
            CHECK_FAILURE(m_webView->remove_DevToolsProtocolEventReceived(
                eventName.c_str(),
                preexistingToken->second));
        }

        CHECK_FAILURE(m_webView->add_DevToolsProtocolEventReceived(
            eventName.c_str(),
            Callback<IWebView2DevToolsProtocolEventReceivedEventHandler>(
                [eventName](IWebView2WebView* sender,
                            IWebView2DevToolsProtocolEventReceivedEventArgs* args)
                -> HRESULT
        {
            wil::unique_cotaskmem_string parameterObjectAsJson;
            CHECK_FAILURE(args->get_ParameterObjectAsJson(&parameterObjectAsJson));
            MessageBox(nullptr, parameterObjectAsJson.get(),
                       (L"CDP Event Fired: " + eventName).c_str(), MB_OK);
            return S_OK;
        }).Get(), &m_devToolsProtocolEventReceivedTokenMap[eventName]));
    }
}
```

#### <span data-ttu-id="0a278-550">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="0a278-550">remove_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="0a278-551">Supprimez un gestionnaire d’événements préalablement ajouté à add_DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="0a278-551">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

> <span data-ttu-id="0a278-552">[remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)par le biais du public HRESULT, EventRegistrationToken jeton</span><span class="sxs-lookup"><span data-stu-id="0a278-552">public HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(LPCWSTR eventName,EventRegistrationToken token)</span></span>

#### <span data-ttu-id="0a278-553">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="0a278-553">get_BrowserProcessId</span></span> 

<span data-ttu-id="0a278-554">ID de processus du processus de navigation qui héberge le WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-554">The process id of the browser process that hosts the WebView.</span></span>

> <span data-ttu-id="0a278-555">valeur publique HRESULT [get_BrowserProcessId](#get_browserprocessid)(valeur UInt32 \*)</span><span class="sxs-lookup"><span data-stu-id="0a278-555">public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* value)</span></span>

#### <span data-ttu-id="0a278-556">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="0a278-556">get_CanGoBack</span></span> 

<span data-ttu-id="0a278-557">Peut parcourir le WebView vers la page précédente de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="0a278-557">Can navigate the webview to the previous page in the navigation history.</span></span>

> <span data-ttu-id="0a278-558">valeur publique HRESULT [get_CanGoBack](#get_cangoback)(bool \* CanGoBack)</span><span class="sxs-lookup"><span data-stu-id="0a278-558">public HRESULT [get_CanGoBack](#get_cangoback)(BOOL \* canGoBack)</span></span>

<span data-ttu-id="0a278-559">get_CanGoBack modifier la valeur avec l’événement DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="0a278-559">get_CanGoBack change value with the DocumentStateChanged event.</span></span>

#### <span data-ttu-id="0a278-560">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="0a278-560">get_CanGoForward</span></span> 

<span data-ttu-id="0a278-561">Peut parcourir le WebView sur la page suivante de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="0a278-561">Can navigate the webview to the next page in the navigation history.</span></span>

> <span data-ttu-id="0a278-562">valeur publique HRESULT [get_CanGoForward](#get_cangoforward)(bool \* CanGoForward)</span><span class="sxs-lookup"><span data-stu-id="0a278-562">public HRESULT [get_CanGoForward](#get_cangoforward)(BOOL \* canGoForward)</span></span>

<span data-ttu-id="0a278-563">get_CanGoForward modifier la valeur avec l’événement DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="0a278-563">get_CanGoForward change value with the DocumentStateChanged event.</span></span>

#### <span data-ttu-id="0a278-564">GoBack</span><span class="sxs-lookup"><span data-stu-id="0a278-564">GoBack</span></span> 

<span data-ttu-id="0a278-565">Permet d’accéder à la page précédente de l’historique de navigation via le WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-565">Navigates the webview to the previous page in the navigation history.</span></span>

> <span data-ttu-id="0a278-566">public HRESULT [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="0a278-566">public HRESULT [GoBack](#goback)()</span></span>

#### <span data-ttu-id="0a278-567">GoForward</span><span class="sxs-lookup"><span data-stu-id="0a278-567">GoForward</span></span> 

<span data-ttu-id="0a278-568">Navigue vers la page suivante de l’historique de navigation du WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-568">Navigates the webview to the next page in the navigation history.</span></span>

> <span data-ttu-id="0a278-569">valeur publique HRESULT [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="0a278-569">public HRESULT [GoForward](#goforward)()</span></span>

#### <span data-ttu-id="0a278-570">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="0a278-570">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span> 

<span data-ttu-id="0a278-571">Format d’image utilisé par la méthode [IWebView2WebView:: CapturePreview](#capturepreview) .</span><span class="sxs-lookup"><span data-stu-id="0a278-571">Image format used by the [IWebView2WebView::CapturePreview](#capturepreview) method.</span></span>

> <span data-ttu-id="0a278-572">énumération [WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format)</span><span class="sxs-lookup"><span data-stu-id="0a278-572">enum [WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format)</span></span>

 <span data-ttu-id="0a278-573">Doubl</span><span class="sxs-lookup"><span data-stu-id="0a278-573">Values</span></span>                         | <span data-ttu-id="0a278-574">Descriptions</span><span class="sxs-lookup"><span data-stu-id="0a278-574">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="0a278-575">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span><span class="sxs-lookup"><span data-stu-id="0a278-575">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span></span>            | <span data-ttu-id="0a278-576">Format d’image PNG.</span><span class="sxs-lookup"><span data-stu-id="0a278-576">PNG image format.</span></span>
<span data-ttu-id="0a278-577">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span><span class="sxs-lookup"><span data-stu-id="0a278-577">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span></span>            | <span data-ttu-id="0a278-578">Format d’image JPEG.</span><span class="sxs-lookup"><span data-stu-id="0a278-578">JPEG image format.</span></span>

#### <span data-ttu-id="0a278-579">WEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="0a278-579">WEBVIEW2_SCRIPT_DIALOG_KIND</span></span> 

<span data-ttu-id="0a278-580">Type de boîte de dialogue JavaScript utilisée dans l’interface [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) .</span><span class="sxs-lookup"><span data-stu-id="0a278-580">Kind of JavaScript dialog used in the [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) interface.</span></span>

> <span data-ttu-id="0a278-581">énumération [WEBVIEW2_SCRIPT_DIALOG_KIND](#webview2_script_dialog_kind)</span><span class="sxs-lookup"><span data-stu-id="0a278-581">enum [WEBVIEW2_SCRIPT_DIALOG_KIND](#webview2_script_dialog_kind)</span></span>

 <span data-ttu-id="0a278-582">Doubl</span><span class="sxs-lookup"><span data-stu-id="0a278-582">Values</span></span>                         | <span data-ttu-id="0a278-583">Descriptions</span><span class="sxs-lookup"><span data-stu-id="0a278-583">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="0a278-584">WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span><span class="sxs-lookup"><span data-stu-id="0a278-584">WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span></span>            | <span data-ttu-id="0a278-585">Une boîte de dialogue appelée par le biais de la fonction JavaScript window. Alert.</span><span class="sxs-lookup"><span data-stu-id="0a278-585">A dialog invoked via the window.alert JavaScript function.</span></span>
<span data-ttu-id="0a278-586">WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span><span class="sxs-lookup"><span data-stu-id="0a278-586">WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span></span>            | <span data-ttu-id="0a278-587">Une boîte de dialogue appelée via la fonction de fenêtre. confirmer JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0a278-587">A dialog invoked via the window.confirm JavaScript function.</span></span>
<span data-ttu-id="0a278-588">WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span><span class="sxs-lookup"><span data-stu-id="0a278-588">WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span></span>            | <span data-ttu-id="0a278-589">Une boîte de dialogue appelée via la fonction JavaScript window. prompt.</span><span class="sxs-lookup"><span data-stu-id="0a278-589">A dialog invoked via the window.prompt JavaScript function.</span></span>

#### <span data-ttu-id="0a278-590">WEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="0a278-590">WEBVIEW2_PROCESS_FAILED_KIND</span></span> 

<span data-ttu-id="0a278-591">Type d’échec de processus utilisé dans l’interface [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) .</span><span class="sxs-lookup"><span data-stu-id="0a278-591">Kind of process failure used in the [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) interface.</span></span>

> <span data-ttu-id="0a278-592">énumération [WEBVIEW2_PROCESS_FAILED_KIND](#webview2_process_failed_kind)</span><span class="sxs-lookup"><span data-stu-id="0a278-592">enum [WEBVIEW2_PROCESS_FAILED_KIND](#webview2_process_failed_kind)</span></span>

 <span data-ttu-id="0a278-593">Doubl</span><span class="sxs-lookup"><span data-stu-id="0a278-593">Values</span></span>                         | <span data-ttu-id="0a278-594">Descriptions</span><span class="sxs-lookup"><span data-stu-id="0a278-594">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="0a278-595">WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="0a278-595">WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span></span>            | <span data-ttu-id="0a278-596">Indique que le processus du navigateur s’est arrêté de manière inattendue.</span><span class="sxs-lookup"><span data-stu-id="0a278-596">Indicates the browser process terminated unexpectedly.</span></span>
<span data-ttu-id="0a278-597">WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="0a278-597">WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span></span>            | <span data-ttu-id="0a278-598">Indique le processus de rendu arrêté de manière inattendue.</span><span class="sxs-lookup"><span data-stu-id="0a278-598">Indicates the render process terminated unexpectedly.</span></span>
<span data-ttu-id="0a278-599">WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span><span class="sxs-lookup"><span data-stu-id="0a278-599">WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span></span>            | <span data-ttu-id="0a278-600">Indique que le processus de rendu ne répond pas.</span><span class="sxs-lookup"><span data-stu-id="0a278-600">Indicates the render process becomes unresponsive.</span></span>

#### <span data-ttu-id="0a278-601">WEBVIEW2_PERMISSION_TYPE</span><span class="sxs-lookup"><span data-stu-id="0a278-601">WEBVIEW2_PERMISSION_TYPE</span></span> 

<span data-ttu-id="0a278-602">Le type d’une demande d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="0a278-602">The type of a permission request.</span></span>

> <span data-ttu-id="0a278-603">énumération [WEBVIEW2_PERMISSION_TYPE](#webview2_permission_type)</span><span class="sxs-lookup"><span data-stu-id="0a278-603">enum [WEBVIEW2_PERMISSION_TYPE](#webview2_permission_type)</span></span>

 <span data-ttu-id="0a278-604">Doubl</span><span class="sxs-lookup"><span data-stu-id="0a278-604">Values</span></span>                         | <span data-ttu-id="0a278-605">Descriptions</span><span class="sxs-lookup"><span data-stu-id="0a278-605">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="0a278-606">WEBVIEW2_PERMISSION_TYPE_UNKNOWN_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="0a278-606">WEBVIEW2_PERMISSION_TYPE_UNKNOWN_PERMISSION</span></span>            | <span data-ttu-id="0a278-607">Autorisation inconnue.</span><span class="sxs-lookup"><span data-stu-id="0a278-607">Unknown permission.</span></span>
<span data-ttu-id="0a278-608">WEBVIEW2_PERMISSION_TYPE_MICROPHONE</span><span class="sxs-lookup"><span data-stu-id="0a278-608">WEBVIEW2_PERMISSION_TYPE_MICROPHONE</span></span>            | <span data-ttu-id="0a278-609">Autorisation de capture audio.</span><span class="sxs-lookup"><span data-stu-id="0a278-609">Permission to capture audio.</span></span>
<span data-ttu-id="0a278-610">WEBVIEW2_PERMISSION_TYPE_CAMERA</span><span class="sxs-lookup"><span data-stu-id="0a278-610">WEBVIEW2_PERMISSION_TYPE_CAMERA</span></span>            | <span data-ttu-id="0a278-611">Autorisation de capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="0a278-611">Permission to capture video.</span></span>
<span data-ttu-id="0a278-612">WEBVIEW2_PERMISSION_TYPE_GEOLOCATION</span><span class="sxs-lookup"><span data-stu-id="0a278-612">WEBVIEW2_PERMISSION_TYPE_GEOLOCATION</span></span>            | <span data-ttu-id="0a278-613">Autorisation d’accès à la géolocalisation.</span><span class="sxs-lookup"><span data-stu-id="0a278-613">Permission to access geolocation.</span></span>
<span data-ttu-id="0a278-614">WEBVIEW2_PERMISSION_TYPE_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="0a278-614">WEBVIEW2_PERMISSION_TYPE_NOTIFICATIONS</span></span>            | <span data-ttu-id="0a278-615">Autorisation d’envoyer des notifications Web.</span><span class="sxs-lookup"><span data-stu-id="0a278-615">Permission to send web notifications.</span></span>
<span data-ttu-id="0a278-616">WEBVIEW2_PERMISSION_TYPE_OTHER_SENSORS</span><span class="sxs-lookup"><span data-stu-id="0a278-616">WEBVIEW2_PERMISSION_TYPE_OTHER_SENSORS</span></span>            | <span data-ttu-id="0a278-617">Autorisation d’accès au capteur générique.</span><span class="sxs-lookup"><span data-stu-id="0a278-617">Permission to access generic sensor.</span></span>
<span data-ttu-id="0a278-618">WEBVIEW2_PERMISSION_TYPE_CLIPBOARD_READ</span><span class="sxs-lookup"><span data-stu-id="0a278-618">WEBVIEW2_PERMISSION_TYPE_CLIPBOARD_READ</span></span>            | <span data-ttu-id="0a278-619">Autorisation de lecture du presse-papiers système sans mouvement utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0a278-619">Permission to read system clipboard without a user gesture.</span></span>

#### <span data-ttu-id="0a278-620">WEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="0a278-620">WEBVIEW2_PERMISSION_STATE</span></span> 

<span data-ttu-id="0a278-621">Réponse à une demande d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="0a278-621">Response to a permission request.</span></span>

> <span data-ttu-id="0a278-622">énumération [WEBVIEW2_PERMISSION_STATE](#webview2_permission_state)</span><span class="sxs-lookup"><span data-stu-id="0a278-622">enum [WEBVIEW2_PERMISSION_STATE](#webview2_permission_state)</span></span>

 <span data-ttu-id="0a278-623">Doubl</span><span class="sxs-lookup"><span data-stu-id="0a278-623">Values</span></span>                         | <span data-ttu-id="0a278-624">Descriptions</span><span class="sxs-lookup"><span data-stu-id="0a278-624">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="0a278-625">WEBVIEW2_PERMISSION_STATE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="0a278-625">WEBVIEW2_PERMISSION_STATE_DEFAULT</span></span>            | <span data-ttu-id="0a278-626">Utilisez le comportement par défaut du navigateur, qui invite en principe les utilisateurs à la décision.</span><span class="sxs-lookup"><span data-stu-id="0a278-626">Use default browser behavior, which normally prompt users for decision.</span></span>
<span data-ttu-id="0a278-627">WEBVIEW2_PERMISSION_STATE_ALLOW</span><span class="sxs-lookup"><span data-stu-id="0a278-627">WEBVIEW2_PERMISSION_STATE_ALLOW</span></span>            | <span data-ttu-id="0a278-628">Accordez la demande d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="0a278-628">Grant the permission request.</span></span>
<span data-ttu-id="0a278-629">WEBVIEW2_PERMISSION_STATE_DENY</span><span class="sxs-lookup"><span data-stu-id="0a278-629">WEBVIEW2_PERMISSION_STATE_DENY</span></span>            | <span data-ttu-id="0a278-630">Refusez la demande d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="0a278-630">Deny the permission request.</span></span>

#### <span data-ttu-id="0a278-631">WEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="0a278-631">WEBVIEW2_MOVE_FOCUS_REASON</span></span> 

<span data-ttu-id="0a278-632">Raison du déplacement du focus.</span><span class="sxs-lookup"><span data-stu-id="0a278-632">Reason for moving focus.</span></span>

> <span data-ttu-id="0a278-633">énumération [WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason)</span><span class="sxs-lookup"><span data-stu-id="0a278-633">enum [WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason)</span></span>

 <span data-ttu-id="0a278-634">Doubl</span><span class="sxs-lookup"><span data-stu-id="0a278-634">Values</span></span>                         | <span data-ttu-id="0a278-635">Descriptions</span><span class="sxs-lookup"><span data-stu-id="0a278-635">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="0a278-636">WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span><span class="sxs-lookup"><span data-stu-id="0a278-636">WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span></span>            | <span data-ttu-id="0a278-637">Paramètre de code axé sur le WebView.</span><span class="sxs-lookup"><span data-stu-id="0a278-637">Code setting focus into WebView.</span></span>
<span data-ttu-id="0a278-638">WEBVIEW2_MOVE_FOCUS_REASON_NEXT</span><span class="sxs-lookup"><span data-stu-id="0a278-638">WEBVIEW2_MOVE_FOCUS_REASON_NEXT</span></span>            | <span data-ttu-id="0a278-639">Déplacement du focus en raison d’une touche Tab.</span><span class="sxs-lookup"><span data-stu-id="0a278-639">Moving focus due to Tab traversal forward.</span></span>
<span data-ttu-id="0a278-640">WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span><span class="sxs-lookup"><span data-stu-id="0a278-640">WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span></span>            | <span data-ttu-id="0a278-641">Déplacement du focus en partant du haut de l’onglet.</span><span class="sxs-lookup"><span data-stu-id="0a278-641">Moving focus due to Tab traversal backward.</span></span>

#### <span data-ttu-id="0a278-642">WEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="0a278-642">WEBVIEW2_WEB_ERROR_STATUS</span></span> 

<span data-ttu-id="0a278-643">Valeurs d’état d’erreur pour les navigations Web.</span><span class="sxs-lookup"><span data-stu-id="0a278-643">Error status values for web navigations.</span></span>

> <span data-ttu-id="0a278-644">énumération [WEBVIEW2_WEB_ERROR_STATUS](#webview2_web_error_status)</span><span class="sxs-lookup"><span data-stu-id="0a278-644">enum [WEBVIEW2_WEB_ERROR_STATUS](#webview2_web_error_status)</span></span>

 <span data-ttu-id="0a278-645">Doubl</span><span class="sxs-lookup"><span data-stu-id="0a278-645">Values</span></span>                         | <span data-ttu-id="0a278-646">Descriptions</span><span class="sxs-lookup"><span data-stu-id="0a278-646">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="0a278-647">WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="0a278-647">WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span></span>            | <span data-ttu-id="0a278-648">Une erreur inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0a278-648">An unknown error occurred.</span></span>
<span data-ttu-id="0a278-649">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span><span class="sxs-lookup"><span data-stu-id="0a278-649">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span></span>            | <span data-ttu-id="0a278-650">Le nom usuel du certificat SSL ne correspond pas à l’adresse Web.</span><span class="sxs-lookup"><span data-stu-id="0a278-650">The SSL certificate common name does not match the web address.</span></span>
<span data-ttu-id="0a278-651">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span><span class="sxs-lookup"><span data-stu-id="0a278-651">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span></span>            | <span data-ttu-id="0a278-652">Le certificat SSL a expiré.</span><span class="sxs-lookup"><span data-stu-id="0a278-652">The SSL certificate has expired.</span></span>
<span data-ttu-id="0a278-653">WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span><span class="sxs-lookup"><span data-stu-id="0a278-653">WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span></span>            | <span data-ttu-id="0a278-654">Le certificat client SSL comporte des erreurs.</span><span class="sxs-lookup"><span data-stu-id="0a278-654">The SSL client certificate contains errors.</span></span>
<span data-ttu-id="0a278-655">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span><span class="sxs-lookup"><span data-stu-id="0a278-655">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span></span>            | <span data-ttu-id="0a278-656">Le certificat SSL a été révoqué.</span><span class="sxs-lookup"><span data-stu-id="0a278-656">The SSL certificate has been revoked.</span></span>
<span data-ttu-id="0a278-657">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span><span class="sxs-lookup"><span data-stu-id="0a278-657">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span></span>            | <span data-ttu-id="0a278-658">Le certificat SSL n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0a278-658">The SSL certificate is invalid.</span></span>
<span data-ttu-id="0a278-659">WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="0a278-659">WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span></span>            | <span data-ttu-id="0a278-660">L’hôte n’est pas joignable.</span><span class="sxs-lookup"><span data-stu-id="0a278-660">The host is unreachable.</span></span>
<span data-ttu-id="0a278-661">WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="0a278-661">WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span></span>            | <span data-ttu-id="0a278-662">La connexion a expiré.</span><span class="sxs-lookup"><span data-stu-id="0a278-662">The connection has timed out.</span></span>
<span data-ttu-id="0a278-663">WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span><span class="sxs-lookup"><span data-stu-id="0a278-663">WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span></span>            | <span data-ttu-id="0a278-664">Le serveur a renvoyé une réponse non valide ou non reconnue.</span><span class="sxs-lookup"><span data-stu-id="0a278-664">The server returned an invalid or unrecognized response.</span></span>
<span data-ttu-id="0a278-665">WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span><span class="sxs-lookup"><span data-stu-id="0a278-665">WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span></span>            | <span data-ttu-id="0a278-666">La connexion a été annulée.</span><span class="sxs-lookup"><span data-stu-id="0a278-666">The connection was aborted.</span></span>
<span data-ttu-id="0a278-667">WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span><span class="sxs-lookup"><span data-stu-id="0a278-667">WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span></span>            | <span data-ttu-id="0a278-668">La connexion a été réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="0a278-668">The connection was reset.</span></span>
<span data-ttu-id="0a278-669">WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span><span class="sxs-lookup"><span data-stu-id="0a278-669">WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span></span>            | <span data-ttu-id="0a278-670">La connexion Internet a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="0a278-670">The Internet connection has been lost.</span></span>
<span data-ttu-id="0a278-671">WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span><span class="sxs-lookup"><span data-stu-id="0a278-671">WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span></span>            | <span data-ttu-id="0a278-672">Connexion impossible à la destination.</span><span class="sxs-lookup"><span data-stu-id="0a278-672">Cannot connect to destination.</span></span>
<span data-ttu-id="0a278-673">WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="0a278-673">WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span></span>            | <span data-ttu-id="0a278-674">Impossible de résoudre le nom d’hôte fourni.</span><span class="sxs-lookup"><span data-stu-id="0a278-674">Could not resolve provided host name.</span></span>
<span data-ttu-id="0a278-675">WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span><span class="sxs-lookup"><span data-stu-id="0a278-675">WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span></span>            | <span data-ttu-id="0a278-676">L’opération a été annulée.</span><span class="sxs-lookup"><span data-stu-id="0a278-676">The operation was canceled.</span></span>
<span data-ttu-id="0a278-677">WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span><span class="sxs-lookup"><span data-stu-id="0a278-677">WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span></span>            | <span data-ttu-id="0a278-678">Échec de la redirection de la requête.</span><span class="sxs-lookup"><span data-stu-id="0a278-678">The request redirect failed.</span></span>
<span data-ttu-id="0a278-679">WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span><span class="sxs-lookup"><span data-stu-id="0a278-679">WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span></span>            | <span data-ttu-id="0a278-680">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0a278-680">An unexpected error occurred.</span></span>

#### <span data-ttu-id="0a278-681">WEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="0a278-681">WEBVIEW2_WEB_RESOURCE_CONTEXT</span></span> 

<span data-ttu-id="0a278-682">Énum pour les contextes de demande de ressources Web.</span><span class="sxs-lookup"><span data-stu-id="0a278-682">Enum for web resource request contexts.</span></span>

> <span data-ttu-id="0a278-683">énumération [WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context)</span><span class="sxs-lookup"><span data-stu-id="0a278-683">enum [WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context)</span></span>

 <span data-ttu-id="0a278-684">Doubl</span><span class="sxs-lookup"><span data-stu-id="0a278-684">Values</span></span>                         | <span data-ttu-id="0a278-685">Descriptions</span><span class="sxs-lookup"><span data-stu-id="0a278-685">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="0a278-686">WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span><span class="sxs-lookup"><span data-stu-id="0a278-686">WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span></span>            | <span data-ttu-id="0a278-687">Toutes les ressources.</span><span class="sxs-lookup"><span data-stu-id="0a278-687">All resources.</span></span>
<span data-ttu-id="0a278-688">WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="0a278-688">WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span></span>            | <span data-ttu-id="0a278-689">Ressources de documents.</span><span class="sxs-lookup"><span data-stu-id="0a278-689">Document resources.</span></span>
<span data-ttu-id="0a278-690">WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span><span class="sxs-lookup"><span data-stu-id="0a278-690">WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span></span>            | <span data-ttu-id="0a278-691">Des ressources CSS;</span><span class="sxs-lookup"><span data-stu-id="0a278-691">CSS resources.</span></span>
<span data-ttu-id="0a278-692">WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span><span class="sxs-lookup"><span data-stu-id="0a278-692">WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span></span>            | <span data-ttu-id="0a278-693">Ressources d’image.</span><span class="sxs-lookup"><span data-stu-id="0a278-693">Image resources.</span></span>
<span data-ttu-id="0a278-694">WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span><span class="sxs-lookup"><span data-stu-id="0a278-694">WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span></span>            | <span data-ttu-id="0a278-695">Autres ressources multimédias telles que les vidéos.</span><span class="sxs-lookup"><span data-stu-id="0a278-695">Other media resources such as videos.</span></span>
<span data-ttu-id="0a278-696">WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span><span class="sxs-lookup"><span data-stu-id="0a278-696">WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span></span>            | <span data-ttu-id="0a278-697">Ressources de police.</span><span class="sxs-lookup"><span data-stu-id="0a278-697">Font resources.</span></span>
<span data-ttu-id="0a278-698">WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="0a278-698">WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span></span>            | <span data-ttu-id="0a278-699">Ressources de script.</span><span class="sxs-lookup"><span data-stu-id="0a278-699">Script resources.</span></span>
<span data-ttu-id="0a278-700">WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="0a278-700">WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span></span>            | <span data-ttu-id="0a278-701">Requêtes HTTP XML.</span><span class="sxs-lookup"><span data-stu-id="0a278-701">XML HTTP requests.</span></span>
<span data-ttu-id="0a278-702">WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span><span class="sxs-lookup"><span data-stu-id="0a278-702">WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span></span>            | <span data-ttu-id="0a278-703">Extraire la communication de l’API.</span><span class="sxs-lookup"><span data-stu-id="0a278-703">Fetch API communication.</span></span>
<span data-ttu-id="0a278-704">WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span><span class="sxs-lookup"><span data-stu-id="0a278-704">WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span></span>            | <span data-ttu-id="0a278-705">Ressources TextTrack.</span><span class="sxs-lookup"><span data-stu-id="0a278-705">TextTrack resources.</span></span>
<span data-ttu-id="0a278-706">WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span><span class="sxs-lookup"><span data-stu-id="0a278-706">WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span></span>            | 
<span data-ttu-id="0a278-707">WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span><span class="sxs-lookup"><span data-stu-id="0a278-707">WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span></span>            | 
<span data-ttu-id="0a278-708">WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span><span class="sxs-lookup"><span data-stu-id="0a278-708">WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span></span>            | 
<span data-ttu-id="0a278-709">WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span><span class="sxs-lookup"><span data-stu-id="0a278-709">WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span></span>            | 
<span data-ttu-id="0a278-710">WEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span><span class="sxs-lookup"><span data-stu-id="0a278-710">WEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span></span>            | 
<span data-ttu-id="0a278-711">WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span><span class="sxs-lookup"><span data-stu-id="0a278-711">WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span></span>            | 
<span data-ttu-id="0a278-712">WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span><span class="sxs-lookup"><span data-stu-id="0a278-712">WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span></span>            | <span data-ttu-id="0a278-713">Autres ressources.</span><span class="sxs-lookup"><span data-stu-id="0a278-713">Other resources.</span></span>
