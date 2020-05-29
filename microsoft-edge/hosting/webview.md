---
description: Hébergement de contenu Web dans votre application Windows 10 avec le contrôle WebView (EdgeHTML)
title: Applications WebView Microsoft Edge pour les applications Windows 10
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: x-ms-WebView, MSHTMLWebViewElement, WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 08efb1bb87877e0b11cbc3bee1061f9be6c9ab3f
ms.sourcegitcommit: 831fc41ea347e2d1160b1804fb5e5a427dc3070d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2020
ms.locfileid: "10629548"
---
# <span data-ttu-id="04da2-104">WebView (EdgeHTML) pour les applications Windows 10</span><span class="sxs-lookup"><span data-stu-id="04da2-104">WebView (EdgeHTML) for Windows 10 apps</span></span>

<span data-ttu-id="04da2-105">Le contrôle WebView (EdgeHTML) vous permet d’héberger le contenu Web dans votre application Windows 10.</span><span class="sxs-lookup"><span data-stu-id="04da2-105">The WebView (EdgeHTML) control enables you to host web content in your Windows 10 app.</span></span> 

<span data-ttu-id="04da2-106">Vous pouvez l’utiliser en tant qu’élément XAML (pour les [applications de plateforme Windows universelle (UWP)](/uwp/api/Windows.UI.Xaml.Controls.WebView) et les [applications de bureau Windows Forms](/windows/communitytoolkit/controls/wpf-winforms/webview), ou dans un élément HTML (x-ms-WebView)/DOM pour les applications Windows 10, comme décrit ici.</span><span class="sxs-lookup"><span data-stu-id="04da2-106">You can use it as a XAML element (for [Universal Windows Platform (UWP) apps](/uwp/api/Windows.UI.Xaml.Controls.WebView) and [Windows Forms and WPF desktop applications](/windows/communitytoolkit/controls/wpf-winforms/webview)), or an HTML element (x-ms-webview)/DOM object (MSHTMLWebViewElement) for JavaScript-based Windows 10 apps, as described here.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="04da2-107">Événements</span><span class="sxs-lookup"><span data-stu-id="04da2-107">Events</span></span>**](#events) | <span data-ttu-id="04da2-108">[departingFocus](#departingfocus), [MSWebViewContainsFullScreenElementChanged](#mswebviewcontainsfullscreenelementchanged), [MSWebViewContentLoading](#mswebviewcontentloading), [MSWebViewDOMContentLoaded](#mswebviewdomcontentloaded), [MSWebViewFrameContentLoading](#mswebviewframecontentloading), [MSWebViewFrameDOMContentLoaded](#mswebviewframedomcontentloaded), [MSWebViewFrameNavigationCompleted](#mswebviewframenavigationcompleted), [MSWebViewFrameNavigationStarting](#mswebviewframenavigationstarting), [MSWebViewLongRunningScriptDetected](#mswebviewlongrunningscriptdetected), [MSWebViewNavigationCompleted](#mswebviewnavigationcompleted), [MSWebViewNavigationStarting](#mswebviewnavigationstarting), [MSWebViewNewWindowRequested](#mswebviewnewwindowrequested), [MSWebViewPermissionRequested, MSWebViewProcessExited](#mswebviewpermissionrequested) [, MSWebViewWebResourceRequested](#mswebviewprocessexited), MSWebViewScriptNotify [, MSWebViewUnsafeContentWarningDisplaying](#mswebviewscriptnotify), [MSWebViewUnsupportedUriSchemeIdentified](#mswebviewunsupportedurischemeidentified) [MSWebViewUnsupportedUriSchemeIdentified](#mswebviewunsafecontentwarningdisplaying), [MSWebViewUnviewableContentIdentified](#mswebviewunviewablecontentidentified) [MSWebViewUnviewableContentIdentified](#mswebviewwebresourcerequested)</span><span class="sxs-lookup"><span data-stu-id="04da2-108">[departingFocus](#departingfocus), [MSWebViewContainsFullScreenElementChanged](#mswebviewcontainsfullscreenelementchanged), [MSWebViewContentLoading](#mswebviewcontentloading), [MSWebViewDOMContentLoaded](#mswebviewdomcontentloaded), [MSWebViewFrameContentLoading](#mswebviewframecontentloading), [MSWebViewFrameDOMContentLoaded](#mswebviewframedomcontentloaded), [MSWebViewFrameNavigationCompleted](#mswebviewframenavigationcompleted), [MSWebViewFrameNavigationStarting](#mswebviewframenavigationstarting), [MSWebViewLongRunningScriptDetected](#mswebviewlongrunningscriptdetected), [MSWebViewNavigationCompleted](#mswebviewnavigationcompleted), [MSWebViewNavigationStarting](#mswebviewnavigationstarting), [MSWebViewNewWindowRequested](#mswebviewnewwindowrequested), [MSWebViewPermissionRequested](#mswebviewpermissionrequested), [MSWebViewProcessExited](#mswebviewprocessexited), [MSWebViewWebResourceRequested](#mswebviewwebresourcerequested), [MSWebViewScriptNotify](#mswebviewscriptnotify), [MSWebViewUnsafeContentWarningDisplaying](#mswebviewunsafecontentwarningdisplaying), [MSWebViewUnsupportedUriSchemeIdentified](#mswebviewunsupportedurischemeidentified), [MSWebViewUnviewableContentIdentified](#mswebviewunviewablecontentidentified)</span></span>
| [**<span data-ttu-id="04da2-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="04da2-109">Methods</span></span>**](#methods) | <span data-ttu-id="04da2-110">[addWebAllowedObject](#addweballowedobject), [buildlocalStreamUri](#buildlocalstreamuri), [capturePreviewToBlobAsync](#capturepreviewtoblobasync), [captureSelectedContentToDataPackageAsync](#captureselectedcontenttodatapackageasync), [invokeScriptAsync](#invokescriptasync), [getDeferredPermissionRequests](#getdeferredpermissionrequests), [getDeferredPermissionRequestById](#getdeferredpermissionrequestbyid), [GoBack](#goback), [goForward](#goforward), [navigation](#navigate), [navigateFocus](#navigatefocus), [navigateTolocalStreamUri](#navigatetolocalstreamuri), [navigateToString](#navigatetostring), [navigateWithHttpRequestMessage](#navigatewithhttprequestmessage), [Refresh](#refresh), [Stop](#stop)</span><span class="sxs-lookup"><span data-stu-id="04da2-110">[addWebAllowedObject](#addweballowedobject), [buildlocalStreamUri](#buildlocalstreamuri), [capturePreviewToBlobAsync](#capturepreviewtoblobasync), [captureSelectedContentToDataPackageAsync](#captureselectedcontenttodatapackageasync), [invokeScriptAsync](#invokescriptasync), [getDeferredPermissionRequests](#getdeferredpermissionrequests), [getDeferredPermissionRequestById](#getdeferredpermissionrequestbyid), [goBack](#goback), [goForward](#goforward), [navigate](#navigate), [navigateFocus](#navigatefocus), [navigateTolocalStreamUri](#navigatetolocalstreamuri), [navigateToString](#navigatetostring), [navigateWithHttpRequestMessage](#navigatewithhttprequestmessage), [refresh](#refresh), [stop](#stop)</span></span> |
| [**<span data-ttu-id="04da2-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="04da2-111">Properties</span></span>**](#properties) | <span data-ttu-id="04da2-112">[canGoBack](#cangoback), [canGoForward](#cangoforward), [containsFullScreenElement](#containsfullscreenelement), [DocumentTitle](#documenttitle), [Height](#height), [Process](#process), [Settings](#settings), [src](#src), [Width](#width)</span><span class="sxs-lookup"><span data-stu-id="04da2-112">[canGoBack](#cangoback), [canGoForward](#cangoforward), [containsFullScreenElement](#containsfullscreenelement), [documentTitle](#documenttitle), [height](#height), [process](#process), [settings](#settings), [src](#src), [width](#width)</span></span> |

## <span data-ttu-id="04da2-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04da2-113">Syntax</span></span>

```js
// Feature detect for webview support
if (MSHTMLWebViewElement) {
    let wv = document.createElement('x-ms-webview'); // Use CSS to set width, height and other styles
    wv.navigate("https://www.example.com");
    document.body.appendChild(wv);
}
```

## <span data-ttu-id="04da2-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="04da2-114">Remarks</span></span>

### <span data-ttu-id="04da2-115">WebView et IFRAME</span><span class="sxs-lookup"><span data-stu-id="04da2-115">WebView versus iframe</span></span>

<span data-ttu-id="04da2-116">À l’instar d’un élément [IFRAME](https://developer.mozilla.org/docs/Web/HTML/Element/iframe) HTML standard, vous pouvez utiliser WebView pour charger les pages distantes sur http et les pages locales (*MS-AppX-Web///*) à partir de votre package d’application.</span><span class="sxs-lookup"><span data-stu-id="04da2-116">Like a standard HTML [iframe](https://developer.mozilla.org/docs/Web/HTML/Element/iframe) element,  you can use WebView to load remote pages over HTTP and local pages (*ms-appx-web:///*) from your app package.</span></span> <span data-ttu-id="04da2-117">Toutefois, le WebView peut également:</span><span class="sxs-lookup"><span data-stu-id="04da2-117">However, the WebView can also:</span></span>

 - <span data-ttu-id="04da2-118">Charger des pages et des ressources à partir de vos dossiers [ApplicationData](/uwp/api/Windows.Storage.ApplicationData) (local, Roaming, Temp) (*MS-AppData:/*/) et [des flux en mémoire](/microsoft-edge/hosting/webview#buildlocalstreamuri) (*MS-local-Stream:///*)</span><span class="sxs-lookup"><span data-stu-id="04da2-118">Load pages and resources from your [ApplicationData](/uwp/api/Windows.Storage.ApplicationData) (local, roaming, temp) folders (*ms-appdata:///*) and [in-memory streams](/microsoft-edge/hosting/webview#buildlocalstreamuri) (*ms-local-stream:///*)</span></span>

 - <span data-ttu-id="04da2-119">Fournissez des contrôles de type navigateur: pour la navigation [vers l’arrière](#goback) et [vers](#goforward) l’arrière dans l’historique de navigation, et pour l' [arrêt](#stop) ou l' [actualisation](#refresh) de la page active.</span><span class="sxs-lookup"><span data-stu-id="04da2-119">Provide browser-like controls: for going [back](#goback) and [forward](#goforward) in navigation history, and [stopping](#stop) or [refreshing](#refresh) the current page.</span></span> 

 - <span data-ttu-id="04da2-120">[Capture de captures d’écran d’un contenu Web](#capturepreviewtoblobasync) simplifiant l’implémentation du contrat de [partage](/windows/uwp/app-to-app/share-data) d’application Windows 10.</span><span class="sxs-lookup"><span data-stu-id="04da2-120">[Capture screenshots of web content](#capturepreviewtoblobasync) making it easy to implement the Windows 10 app [Share](/windows/uwp/app-to-app/share-data) contract.</span></span>

 - <span data-ttu-id="04da2-121">Autorisez l’exécution du code JavaScript dans un WebView pour déclencher des événements personnalisés ([MSWebViewScriptNotify](#mswebviewscriptnotify)) dans votre application et permettre à votre application d’exécuter JavaScript dans le WebView ([invokeScriptAsync](#invokescriptasync)).</span><span class="sxs-lookup"><span data-stu-id="04da2-121">Allow JavaScript code running within a webview to raise custom events ([MSWebViewScriptNotify](#mswebviewscriptnotify)) to your app, and allow your app to run JavaScript within the webview ([invokeScriptAsync](#invokescriptasync)).</span></span>

 - <span data-ttu-id="04da2-122">Vous fournir des événements de contenu d’affichage de manière précise:</span><span class="sxs-lookup"><span data-stu-id="04da2-122">Provide you with fine-tuned webview content events:</span></span>
    
    <span data-ttu-id="04da2-123">Événement DOM WebView</span><span class="sxs-lookup"><span data-stu-id="04da2-123">WebView DOM event</span></span> | <span data-ttu-id="04da2-124">Description</span><span class="sxs-lookup"><span data-stu-id="04da2-124">Description</span></span>
    --------- | ------
    [<span data-ttu-id="04da2-125">MSWebViewNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="04da2-125">MSWebViewNavigationStarting</span></span>](#mswebviewnavigationstarting) | <span data-ttu-id="04da2-126">Indique que l’affichage du WebView commence</span><span class="sxs-lookup"><span data-stu-id="04da2-126">Indicates the WebView is starting to navigate</span></span>
    [<span data-ttu-id="04da2-127">MSWebViewContentLoading</span><span class="sxs-lookup"><span data-stu-id="04da2-127">MSWebViewContentLoading</span></span>](#mswebviewcontentloading) | <span data-ttu-id="04da2-128">Le contenu HTML est téléchargé et est en cours de chargement dans le contrôle</span><span class="sxs-lookup"><span data-stu-id="04da2-128">The HTML content is downloaded and is being loaded into the control</span></span>
    [<span data-ttu-id="04da2-129">MSWebViewDOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="04da2-129">MSWebViewDOMContentLoaded</span></span>](#mswebviewdomcontentloaded) | <span data-ttu-id="04da2-130">Indique que les éléments DOM principaux ont fini de se charger</span><span class="sxs-lookup"><span data-stu-id="04da2-130">Indicates that the main DOM elements have finished loading</span></span>
    [<span data-ttu-id="04da2-131">MSWebViewNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="04da2-131">MSWebViewNavigationCompleted</span></span>](#mswebviewnavigationcompleted) | <span data-ttu-id="04da2-132">Indique que la navigation est terminée et que tous les éléments multimédias sont affichés</span><span class="sxs-lookup"><span data-stu-id="04da2-132">Indicates the navigation is complete, and all media elements are rendered</span></span>
    [<span data-ttu-id="04da2-133">MSWebViewUnviewableContentIdentified</span><span class="sxs-lookup"><span data-stu-id="04da2-133">MSWebViewUnviewableContentIdentified</span></span>](#mswebviewunviewablecontentidentified) | <span data-ttu-id="04da2-134">Le contenu du WebView ne s’est pas affiché en HTML</span><span class="sxs-lookup"><span data-stu-id="04da2-134">The WebView found the content was not HTML</span></span>
    [<span data-ttu-id="04da2-135">UnsafeContentWarningDisplaying</span><span class="sxs-lookup"><span data-stu-id="04da2-135">UnsafeContentWarningDisplaying</span></span>](#mswebviewunsafecontentwarningdisplaying) | <span data-ttu-id="04da2-136">Le WebView affiche une page d’avertissement pour le contenu signalé comme non sécurisé par le *filtre Windows SmartScreen*.</span><span class="sxs-lookup"><span data-stu-id="04da2-136">The WebView shows a warning page for content that was reported as unsafe by Windows *SmartScreen Filter*.</span></span>

    <span data-ttu-id="04da2-137">... incluant des [événements](#events) correspondants pour le contenu iframe chargé dans un WebView (par exemple, [MSWebView**Frame**NavigationStarting](#mswebviewframenavigationstarting) , etc.)</span><span class="sxs-lookup"><span data-stu-id="04da2-137">...including corresponding [events](#events) for iframe content loaded within a WebView (such as [MSWebView**Frame**NavigationStarting](#mswebviewframenavigationstarting) and so on.)</span></span>

### <span data-ttu-id="04da2-138">Impression</span><span class="sxs-lookup"><span data-stu-id="04da2-138">Printing</span></span>

<span data-ttu-id="04da2-139">Quand une application Windows utilisant JavaScript est imprimée, les `<x-ms-webview>` balises sont transformées en `<iframe>` balises avant l’impression.</span><span class="sxs-lookup"><span data-stu-id="04da2-139">When a Windows app using JavaScript is printed, the `<x-ms-webview>` tags are transformed into `<iframe>` tags before printing.</span></span> <span data-ttu-id="04da2-140">Outre la différence normale entre l’affichage à l’écran et le rendu pour l’impression, les styles CSS appliqués aux `<iframe>` éléments sont ensuite applicables à la `<iframe>` transformation de `<x-ms-webview>` .</span><span class="sxs-lookup"><span data-stu-id="04da2-140">Besides the normal difference between displaying on screen and rendered for print, CSS styles applied to `<iframe>` elements are then applicable to the `<iframe>` transformed from `<x-ms-webview>`.</span></span>

### <span data-ttu-id="04da2-141">Travailleurs de service</span><span class="sxs-lookup"><span data-stu-id="04da2-141">Service workers</span></span>

<span data-ttu-id="04da2-142">À partir de la [mise à jour 2018 de Windows 10 d’octobre](/windows/uwp/whats-new/windows-10-build-17763) (EdgeHTML 18), [les travailleurs de services sont pris en charge dans le contrôle WebView](/microsoft-edge/dev-guide#service-workers) (en plus du navigateur Microsoft Edge et des applications Windows 10 avec JavaScript).</span><span class="sxs-lookup"><span data-stu-id="04da2-142">Starting with the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) (EdgeHTML 18), [service workers are supported in the WebView control](/microsoft-edge/dev-guide#service-workers) (in addition to the Microsoft Edge browser and Windows 10 apps with JavaScript).</span></span>

<span data-ttu-id="04da2-143">les architectures d’applications x64 requièrent des packages de type neutre (n’importe quel processeur) ou x64, car les travailleurs de services ne sont pas pris en charge dans les processus WoW64.</span><span class="sxs-lookup"><span data-stu-id="04da2-143">x64 app architectures require Neutral (Any CPU) or x64 packages, as service workers are not supported in WoW64 processes.</span></span> <span data-ttu-id="04da2-144">(Pour économiser de l’espace disque, la version de WoW des dll requises n’est pas fournie en natif dans Windows.)</span><span class="sxs-lookup"><span data-stu-id="04da2-144">(To conserve disk space, the WoW version of the required DLLs are not natively included in Windows.)</span></span>

### <span data-ttu-id="04da2-145">Modèle de thread et fiabilité</span><span class="sxs-lookup"><span data-stu-id="04da2-145">Threading model and reliability</span></span>

<span data-ttu-id="04da2-146">La création d’un WebView via `document.createElement("x-ms-webview")` ou par le biais `<x-ms-webview>` du balisage crée un WebView sur un nouveau thread unique dans le processus de l’application.</span><span class="sxs-lookup"><span data-stu-id="04da2-146">Creating a WebView via `document.createElement("x-ms-webview")` or via `<x-ms-webview>` markup creates a WebView on a new unique thread in the app's process.</span></span> <span data-ttu-id="04da2-147">L’exécution sur un nouveau thread unique implique que du temps d’exécution du script d’un WebView ne peut pas bloquer l’application ou d’autres vues.</span><span class="sxs-lookup"><span data-stu-id="04da2-147">Running on a new unique thread means that long running script from one WebView is unable to hang the app or other WebViews.</span></span> <span data-ttu-id="04da2-148">La création d’un WebView via le `new MSWebView()` constructeur crée un WebView dans un processus distinct d’affichage.</span><span class="sxs-lookup"><span data-stu-id="04da2-148">Creating a WebView via the `new MSWebView()` constructor creates a WebView in a separate WebView process.</span></span> <span data-ttu-id="04da2-149">L’exécution d’un processus unique implique qu’en plus de la protection du script de grande durée d’exécution, l’application est également protégée du contenu Web qui bloque le processus WebView.</span><span class="sxs-lookup"><span data-stu-id="04da2-149">Running in a unique process means that in addition to protection from long running script, the app is also protected from web content that crashes the WebView process.</span></span> <span data-ttu-id="04da2-150">La création d’un WebView par le biais de la [`MSWebViewProcess.createWebViewAsync`](./webview/MSWebViewProcess.md#createwebviewasync) méthode permet également de créer un WebView dans un processus distinct tout en permettant à l’appelant de contrôler davantage les paramètres de processus et de regrouper les vues WebView dans les processus WebView.</span><span class="sxs-lookup"><span data-stu-id="04da2-150">Creating a WebView via the [`MSWebViewProcess.createWebViewAsync`](./webview/MSWebViewProcess.md#createwebviewasync) method also creates a WebView in a separate process but allows the caller more control over process settings and grouping WebViews in WebView processes.</span></span> <span data-ttu-id="04da2-151">Si vous souhaitez en savoir plus, consultez `MSWebViewProcess`.</span><span class="sxs-lookup"><span data-stu-id="04da2-151">See `MSWebViewProcess` for more information.</span></span> 

### <span data-ttu-id="04da2-152">Accès à l’API WinRT</span><span class="sxs-lookup"><span data-stu-id="04da2-152">WinRT API access</span></span>

<span data-ttu-id="04da2-153">Une application UWP peut permettre aux documents HTML dans les WebView d’avoir accès aux API WinRT.</span><span class="sxs-lookup"><span data-stu-id="04da2-153">A UWP app may allow HTML documents inside WebViews to have access to WinRT APIs.</span></span> <span data-ttu-id="04da2-154">C’est par le biais de l’attribut WindowsRuntimeAccess des éléments enfants Rule de l’élément ApplicationContentUriRules du AppxManifest. XML de l’application UWP.</span><span class="sxs-lookup"><span data-stu-id="04da2-154">This is via the WindowsRuntimeAccess attribute of the Rule child elements of the ApplicationContentUriRules element of the AppxManifest.xml of the UWP app.</span></span> <span data-ttu-id="04da2-155">Définissez WindowsRuntimeAccess sur «All» et les documents HTML avec URI correspondants seront autorisés à utiliser WinRT.</span><span class="sxs-lookup"><span data-stu-id="04da2-155">Set WindowsRuntimeAccess to 'all' and HTML documents with matching URIs will be allowed to use WinRT.</span></span> <span data-ttu-id="04da2-156">Il en s’agit de la même façon que le fait de fournir un accès WinRT au contenu HTML dans les applications UWP JavaScript pour voir comment [appeler des API WinRT de votre PWA](/microsoft-edge/progressive-web-apps-edgehtml/windows-features#call-winrt-apis-from-your-pwa) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="04da2-156">This is the same as providing WinRT access to HTML content in JavaScript UWP apps so see [Call WinRT APIs from your PWA](/microsoft-edge/progressive-web-apps-edgehtml/windows-features#call-winrt-apis-from-your-pwa) for more information.</span></span>

<span data-ttu-id="04da2-157">Les API WinRT associées à l’interface utilisateur risquent de ne pas fonctionner en cas d’appel à partir d’un WebView exécuté sur son propre thread, mais cela risque de fonctionner en cas d’appel à partir d’un WebView exécuté dans un processus WebView distinct.</span><span class="sxs-lookup"><span data-stu-id="04da2-157">UI related WinRT APIs may not work when called from a WebView running on its own thread but may work when called from a WebView running in a separate WebView process.</span></span> <span data-ttu-id="04da2-158">Lorsque vous utilisez un WebView sur son propre thread unique, il ne s’agit pas du thread d’affichage de l’application.</span><span class="sxs-lookup"><span data-stu-id="04da2-158">When using a WebView on its own unique thread, that thread is not the app's view thread.</span></span> <span data-ttu-id="04da2-159">Certaines API WinRT associées à l’interface utilisateur nécessitent d’être appelées à partir du thread d’affichage de l’application.</span><span class="sxs-lookup"><span data-stu-id="04da2-159">Some UI related WinRT APIs require to be called from the app's view thread.</span></span> <span data-ttu-id="04da2-160">Les webaffichages créés dans un processus WebView distinct s’exécutent sur un thread d’affichage et ne doivent donc pas être confrontés aux mêmes restrictions que celles exécutées dans WebView sur leur propre thread unique.</span><span class="sxs-lookup"><span data-stu-id="04da2-160">WebViews created in a separate WebView process do run on a view thread and so should not face the same restrictions as WebView's running on their own unique thread.</span></span> <span data-ttu-id="04da2-161">Si vous rencontrez des problèmes avec les API WinRT associées à l’interface utilisateur dans un WebView, assurez-vous que vous utilisez un WebView dans son propre processus WebView, comme décrit ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="04da2-161">If you have trouble with UI related WinRT APIs in a WebView ensure that you're using a WebView in its own WebView process as described above.</span></span>

### <span data-ttu-id="04da2-162">Limites de stockage AppCache</span><span class="sxs-lookup"><span data-stu-id="04da2-162">AppCache storage limitations</span></span>

<span data-ttu-id="04da2-163">Les applications qui utilisent la prise en charge JavaScript de l’API de cache d’application (ou AppCache), telles qu’elles sont définies dans la [spécification HTML5](https://go.microsoft.com/fwlink/p/?LinkId=228542), doivent respecter les limitations de stockage disponibles.</span><span class="sxs-lookup"><span data-stu-id="04da2-163">Applications using JavaScript support of the Application Cache API (or AppCache), as defined in the [HTML5 specification](https://go.microsoft.com/fwlink/p/?LinkId=228542), to create offline web applications must observe available storage limitations.</span></span> <span data-ttu-id="04da2-164">Ceci est particulièrement vrai dans les appareils dont l’espace mémoire est limité.</span><span class="sxs-lookup"><span data-stu-id="04da2-164">This is especially true in devices with limited memory space.</span></span> <span data-ttu-id="04da2-165">Les limites pratiques en matière de taille des AppCache sont toujours une fonction d’espace de stockage sur disque disponible.</span><span class="sxs-lookup"><span data-stu-id="04da2-165">The practical limits on the size of the AppCache are always a function of available disk storage space.</span></span> <span data-ttu-id="04da2-166">Les recommandations générales sont décrites ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="04da2-166">The general guidelines are shown below.</span></span>

| <span data-ttu-id="04da2-167">Taille du volume</span><span class="sxs-lookup"><span data-stu-id="04da2-167">Volume size</span></span>         |<span data-ttu-id="04da2-168">AppCache par domaine</span><span class="sxs-lookup"><span data-stu-id="04da2-168">AppCache per domain</span></span> | <span data-ttu-id="04da2-169">AppCache par utilisateur</span><span class="sxs-lookup"><span data-stu-id="04da2-169">AppCache per user</span></span>   | 
|---------------|---------------|-------------------------|
<span data-ttu-id="04da2-170">Jusqu’à 4 Go</span><span class="sxs-lookup"><span data-stu-id="04da2-170">Up to 4GB</span></span> | <span data-ttu-id="04da2-171">ATTEINDRE</span><span class="sxs-lookup"><span data-stu-id="04da2-171">10MB</span></span> | <span data-ttu-id="04da2-172">50Mo</span><span class="sxs-lookup"><span data-stu-id="04da2-172">50MB</span></span> |
<span data-ttu-id="04da2-173">4 Go à 16 Go</span><span class="sxs-lookup"><span data-stu-id="04da2-173">4GB to 16GB</span></span> | <span data-ttu-id="04da2-174">50Mo</span><span class="sxs-lookup"><span data-stu-id="04da2-174">50MB</span></span> | <span data-ttu-id="04da2-175">MINIMUM</span><span class="sxs-lookup"><span data-stu-id="04da2-175">500MB</span></span> | 
<span data-ttu-id="04da2-176">16 Go à 32 Go</span><span class="sxs-lookup"><span data-stu-id="04da2-176">16GB to 32 GB</span></span> | <span data-ttu-id="04da2-177">50Mo</span><span class="sxs-lookup"><span data-stu-id="04da2-177">50MB</span></span> | <span data-ttu-id="04da2-178">1 Go</span><span class="sxs-lookup"><span data-stu-id="04da2-178">1GB</span></span> |

<span data-ttu-id="04da2-179">Toutes les applications Windows 10 sont conçues pour utiliser le même modèle de quota AppCache, de sorte que la limitation de stockage disque disponible s’applique aux applications de bureau et de téléphone.</span><span class="sxs-lookup"><span data-stu-id="04da2-179">All Windows10 apps are intended to use the same AppCache quota model, so the available disk storage limitation applies to both desktop and phone apps.</span></span> <span data-ttu-id="04da2-180">Le seuil est également limité après que les pages chargées dans **WebView** aient consommé 1 Go d’espace *AppCache* ; demandes d’espace de stockage *AppCache* supplémentaire au-delà de cette limite sera refusée.</span><span class="sxs-lookup"><span data-stu-id="04da2-180">The is also a hard limit after pages loaded inside **WebView** together have consumed 1 GB of *AppCache* space; requests for additional *AppCache* storage above this limit will be denied.</span></span> 

<span data-ttu-id="04da2-181">Pour plus d’informations, consultez l' [exemple de contrôle WebView html](https://go.microsoft.com/fwlink/p/?linkid=309825) et l’JSBrowser de la documentation sur [le contrôle WebView](https://github.com/MicrosoftEdge/JSBrowser#harnessing-the-webview-control) .</span><span class="sxs-lookup"><span data-stu-id="04da2-181">For more information, see the [HTML WebView control sample](https://go.microsoft.com/fwlink/p/?linkid=309825) and the JSBrowser's [Harnessing the WebView control](https://github.com/MicrosoftEdge/JSBrowser#harnessing-the-webview-control) documentation.</span></span>

## <span data-ttu-id="04da2-182">Événements</span><span class="sxs-lookup"><span data-stu-id="04da2-182">Events</span></span>

### <span data-ttu-id="04da2-183">departingFocus</span><span class="sxs-lookup"><span data-stu-id="04da2-183">departingFocus</span></span>

<span data-ttu-id="04da2-184">Indique le focus sur le **WebView** dans l’application.</span><span class="sxs-lookup"><span data-stu-id="04da2-184">Indicates focus departing from the **webview** into the app.</span></span> <span data-ttu-id="04da2-185">Se déclenche lorsque le document de niveau supérieur d’un WebView est appelé. departFocus.</span><span class="sxs-lookup"><span data-stu-id="04da2-185">Fires when the webview's top level document calls window.departFocus.</span></span> <span data-ttu-id="04da2-186">Les arguments FocusNavigationEvent de l’événement departingFocus correspondent aux paramètres fournis à departFocus, sauf que les paramètres d’origine sont convertis à partir de l’espace de coordonnées document’s du WebView dans l’espace de coordonnées du document hôte de WebView.</span><span class="sxs-lookup"><span data-stu-id="04da2-186">The FocusNavigationEvent args in the departingFocus event match the parameters provided to departFocus except the origin parameters are translated from the webview's document's coordinate space to the coordinate space of the webview host document.</span></span> <span data-ttu-id="04da2-187">Voir la méthode WebView. navigateFocus et l’événement navigatingFocus de fenêtre correspondant pour transférer le focus d’un hôte vers un WebView.</span><span class="sxs-lookup"><span data-stu-id="04da2-187">See the webview.navigateFocus method and corresponding window navigatingFocus event for transferring focus from host to webview.</span></span> <span data-ttu-id="04da2-188">Pour obtenir un exemple d’implémentation de la navigation au focus par le biais d’un clavier ou d’un boîtier de empilements qui gère cet événement, voir la [bibliothèque de navigation](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) dans l’TVJS.</span><span class="sxs-lookup"><span data-stu-id="04da2-188">See the [TVJS's Direction Navigation library](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) for an example of an implementation of focus navigation via keyboard or gamepad that handles this event.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("departingFocus", handler);
webview.removeEventListener("departingFocus", handler);
```

#### <span data-ttu-id="04da2-189">Informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="04da2-189">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="04da2-190">Interface</span><span class="sxs-lookup"><span data-stu-id="04da2-190">Interface</span></span>** | [<span data-ttu-id="04da2-191">FocusNavigationEvent</span><span class="sxs-lookup"><span data-stu-id="04da2-191">FocusNavigationEvent</span></span>](./webview/FocusNavigationEvent.md) |
|**<span data-ttu-id="04da2-192">Synchrone</span><span class="sxs-lookup"><span data-stu-id="04da2-192">Synchronous</span></span>** |<span data-ttu-id="04da2-193">Oui</span><span class="sxs-lookup"><span data-stu-id="04da2-193">Yes</span></span> |    
|**<span data-ttu-id="04da2-194">BD</span><span class="sxs-lookup"><span data-stu-id="04da2-194">Bubbles</span></span>**     |<span data-ttu-id="04da2-195">Oui</span><span class="sxs-lookup"><span data-stu-id="04da2-195">Yes</span></span> |   
|**<span data-ttu-id="04da2-196">Annulable</span><span class="sxs-lookup"><span data-stu-id="04da2-196">Cancelable</span></span>**  |<span data-ttu-id="04da2-197">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-197">No</span></span> |            

### <span data-ttu-id="04da2-198">MSWebViewContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="04da2-198">MSWebViewContainsFullScreenElementChanged</span></span>

<span data-ttu-id="04da2-199">Se produit lorsque l’état change, qu’il s’agisse d’un élément de l' **affichage** plein écran.</span><span class="sxs-lookup"><span data-stu-id="04da2-199">Occurs when the status changes of whether or not the **webview** currently contains a full screen element.</span></span> <span data-ttu-id="04da2-200">Utilisez la propriété containsFullScreenElement sur la valeur actuelle.</span><span class="sxs-lookup"><span data-stu-id="04da2-200">Use the containsFullScreenElement property to the current value.</span></span> <span data-ttu-id="04da2-201">Un élément à l’écran complet fait référence à la notion d' [API DOM fullscreen](https://developer.mozilla.org/docs/Web/API/Fullscreen_API) d’un élément à l’écran complet via les fonctions DOM Element. requestFullScreen et document. exitFullScreen.</span><span class="sxs-lookup"><span data-stu-id="04da2-201">Full screen element here refers to the [Fullscreen DOM APIs](https://developer.mozilla.org/docs/Web/API/Fullscreen_API) notion of a full screen element via the element.requestFullScreen and document.exitFullScreen DOM functions.</span></span>

```js
function containsFullScreenElementChangedHandler(eventInfo) {
    const applicationView = Windows.UI.ViewManagement.ApplicationView.getForCurrentView();
    if (webview.containsFullScreenElement) {
        webview.classList.add("fullscreen"); // Have the webview fill the app view
        applicationView.tryEnterFullScreenMode(); // Have the app view fill the screen
    }
    else {
        webview.classList.remove("fullscreen"); // Return webview to normal
        applicationView.exitFullScreenMode(); // Return app view to normal
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewContainsFullScreenElementChanged", containsFullScreenElementChangedHandler);
webview.removeEventListener("MSWebViewContainsFullScreenElementChanged", containsFullScreenElementChangedHandler);
```

#### <span data-ttu-id="04da2-202">Informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="04da2-202">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="04da2-203">Interface</span><span class="sxs-lookup"><span data-stu-id="04da2-203">Interface</span></span>** | **<span data-ttu-id="04da2-204">Événement</span><span class="sxs-lookup"><span data-stu-id="04da2-204">Event</span></span>** |
|**<span data-ttu-id="04da2-205">Synchrone</span><span class="sxs-lookup"><span data-stu-id="04da2-205">Synchronous</span></span>** |<span data-ttu-id="04da2-206">Oui</span><span class="sxs-lookup"><span data-stu-id="04da2-206">Yes</span></span> |    
|**<span data-ttu-id="04da2-207">BD</span><span class="sxs-lookup"><span data-stu-id="04da2-207">Bubbles</span></span>**     |<span data-ttu-id="04da2-208">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-208">No</span></span> |   
|**<span data-ttu-id="04da2-209">Annulable</span><span class="sxs-lookup"><span data-stu-id="04da2-209">Cancelable</span></span>**  |<span data-ttu-id="04da2-210">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-210">No</span></span> |  

### <span data-ttu-id="04da2-211">MSWebViewContentLoading</span><span class="sxs-lookup"><span data-stu-id="04da2-211">MSWebViewContentLoading</span></span>

<span data-ttu-id="04da2-212">Indique que le contenu HTML est téléchargé et est en cours de chargement dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="04da2-212">Indicates that the HTML content is downloaded and is being loaded into the control.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewContentLoading", handler);
webview.removeEventListener("MSWebViewContentLoading", handler);
```

#### <span data-ttu-id="04da2-213">Informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="04da2-213">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="04da2-214">Interface</span><span class="sxs-lookup"><span data-stu-id="04da2-214">Interface</span></span>** | [<span data-ttu-id="04da2-215">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="04da2-215">NavigationEvent</span></span>](./webview/NavigationEvent.md) |
|**<span data-ttu-id="04da2-216">Synchrone</span><span class="sxs-lookup"><span data-stu-id="04da2-216">Synchronous</span></span>** |<span data-ttu-id="04da2-217">Oui</span><span class="sxs-lookup"><span data-stu-id="04da2-217">Yes</span></span>  |    
|**<span data-ttu-id="04da2-218">BD</span><span class="sxs-lookup"><span data-stu-id="04da2-218">Bubbles</span></span>**     |<span data-ttu-id="04da2-219">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-219">No</span></span> |   
|**<span data-ttu-id="04da2-220">Annulable</span><span class="sxs-lookup"><span data-stu-id="04da2-220">Cancelable</span></span>**  |<span data-ttu-id="04da2-221">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-221">No</span></span> |    

### <span data-ttu-id="04da2-222">MSWebViewDOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="04da2-222">MSWebViewDOMContentLoaded</span></span>

<span data-ttu-id="04da2-223">Indique que les éléments DOM principaux ont fini de se charger.</span><span class="sxs-lookup"><span data-stu-id="04da2-223">Indicates that the main DOM elements have finished loading.</span></span>


```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewDOMContentLoaded", handler);
webview.removeEventListener("MSWebViewDOMContentLoaded", handler);
```

#### <span data-ttu-id="04da2-224">Informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="04da2-224">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="04da2-225">Interface</span><span class="sxs-lookup"><span data-stu-id="04da2-225">Interface</span></span>** | [<span data-ttu-id="04da2-226">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="04da2-226">NavigationEvent</span></span>](./webview/NavigationEvent.md) |
|**<span data-ttu-id="04da2-227">Synchrone</span><span class="sxs-lookup"><span data-stu-id="04da2-227">Synchronous</span></span>** |<span data-ttu-id="04da2-228">Oui</span><span class="sxs-lookup"><span data-stu-id="04da2-228">Yes</span></span>  |    
|**<span data-ttu-id="04da2-229">BD</span><span class="sxs-lookup"><span data-stu-id="04da2-229">Bubbles</span></span>**     |<span data-ttu-id="04da2-230">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-230">No</span></span> |   
|**<span data-ttu-id="04da2-231">Annulable</span><span class="sxs-lookup"><span data-stu-id="04da2-231">Cancelable</span></span>**  |<span data-ttu-id="04da2-232">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-232">No</span></span> |                 

### <span data-ttu-id="04da2-233">MSWebViewFrameContentLoading</span><span class="sxs-lookup"><span data-stu-id="04da2-233">MSWebViewFrameContentLoading</span></span>

<span data-ttu-id="04da2-234">Indique que le contenu HTML est téléchargé et est en cours de chargement dans le `<iframe>` contrôle.</span><span class="sxs-lookup"><span data-stu-id="04da2-234">Indicates that the HTML content downloaded and is being loaded into the `<iframe>` control.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameContentLoading", handler);
webview.removeEventListener("MSWebViewFrameContentLoading", handler);
```

#### <span data-ttu-id="04da2-235">Informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="04da2-235">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="04da2-236">Interface</span><span class="sxs-lookup"><span data-stu-id="04da2-236">Interface</span></span>** | [<span data-ttu-id="04da2-237">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="04da2-237">NavigationEvent</span></span>](./webview/NavigationEvent.md) |
|**<span data-ttu-id="04da2-238">Synchrone</span><span class="sxs-lookup"><span data-stu-id="04da2-238">Synchronous</span></span>** |<span data-ttu-id="04da2-239">Oui</span><span class="sxs-lookup"><span data-stu-id="04da2-239">Yes</span></span>  |    
|**<span data-ttu-id="04da2-240">BD</span><span class="sxs-lookup"><span data-stu-id="04da2-240">Bubbles</span></span>**     |<span data-ttu-id="04da2-241">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-241">No</span></span> |   
|**<span data-ttu-id="04da2-242">Annulable</span><span class="sxs-lookup"><span data-stu-id="04da2-242">Cancelable</span></span>**  |<span data-ttu-id="04da2-243">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-243">No</span></span> |                 

### <span data-ttu-id="04da2-244">MSWebViewFrameDOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="04da2-244">MSWebViewFrameDOMContentLoaded</span></span>

<span data-ttu-id="04da2-245">Indique que les éléments DOM principaux ont fini de se charger dans le `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="04da2-245">Indicates that the main DOM elements have finished loading in the `<iframe>`.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameDOMContentLoaded", handler);
webview.removeEventListener("MSWebViewFrameDOMContentLoaded", handler);
```

#### <span data-ttu-id="04da2-246">Informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="04da2-246">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="04da2-247">Interface</span><span class="sxs-lookup"><span data-stu-id="04da2-247">Interface</span></span>** | [<span data-ttu-id="04da2-248">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="04da2-248">NavigationEvent</span></span>](./webview/NavigationEvent.md) |
|**<span data-ttu-id="04da2-249">Synchrone</span><span class="sxs-lookup"><span data-stu-id="04da2-249">Synchronous</span></span>** |<span data-ttu-id="04da2-250">Oui</span><span class="sxs-lookup"><span data-stu-id="04da2-250">Yes</span></span>  |    
|**<span data-ttu-id="04da2-251">BD</span><span class="sxs-lookup"><span data-stu-id="04da2-251">Bubbles</span></span>**     |<span data-ttu-id="04da2-252">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-252">No</span></span> |   
|**<span data-ttu-id="04da2-253">Annulable</span><span class="sxs-lookup"><span data-stu-id="04da2-253">Cancelable</span></span>**  |<span data-ttu-id="04da2-254">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-254">No</span></span> |    


### <span data-ttu-id="04da2-255">MSWebViewFrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="04da2-255">MSWebViewFrameNavigationCompleted</span></span>

<span data-ttu-id="04da2-256">Indique que la navigation est terminée et que tous les éléments multimédias sont restitués dans la `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="04da2-256">Indicates the navigation is complete, and all media elements are rendered in the `<iframe>`.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameNavigationCompleted", handler);
webview.removeEventListener("MSWebViewFrameNavigationCompleted", handler);
```

#### <span data-ttu-id="04da2-257">Informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="04da2-257">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="04da2-258">Interface</span><span class="sxs-lookup"><span data-stu-id="04da2-258">Interface</span></span>** | [<span data-ttu-id="04da2-259">NavigationCompletedEvent</span><span class="sxs-lookup"><span data-stu-id="04da2-259">NavigationCompletedEvent</span></span>](./webview/NavigationCompletedEvent.md) |
|**<span data-ttu-id="04da2-260">Synchrone</span><span class="sxs-lookup"><span data-stu-id="04da2-260">Synchronous</span></span>** |<span data-ttu-id="04da2-261">Oui</span><span class="sxs-lookup"><span data-stu-id="04da2-261">Yes</span></span> |    
|**<span data-ttu-id="04da2-262">BD</span><span class="sxs-lookup"><span data-stu-id="04da2-262">Bubbles</span></span>**     |<span data-ttu-id="04da2-263">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-263">No</span></span> |   
|**<span data-ttu-id="04da2-264">Annulable</span><span class="sxs-lookup"><span data-stu-id="04da2-264">Cancelable</span></span>**  |<span data-ttu-id="04da2-265">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-265">No</span></span> |       

### <span data-ttu-id="04da2-266">MSWebViewFrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="04da2-266">MSWebViewFrameNavigationStarting</span></span>

<span data-ttu-id="04da2-267">Indique `<iframe>` qu’une partie d’un **WebView** commence à se déplacer.</span><span class="sxs-lookup"><span data-stu-id="04da2-267">Indicates a `<iframe>` within a **webview** is starting to navigate.</span></span> <span data-ttu-id="04da2-268">Ce problème est déclenché avant d’obtenir des ressources du réseau pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="04da2-268">This is fired before obtaining any resources from the network for the navigation.</span></span> <span data-ttu-id="04da2-269">La navigation n’a pas commencé tant que tous les gestionnaires d’événements MSWebViewFrameNavigationStarting n’ont pas terminé.</span><span class="sxs-lookup"><span data-stu-id="04da2-269">The navigation is not started until all MSWebViewFrameNavigationStarting event handlers complete.</span></span> <span data-ttu-id="04da2-270">Cet événement peut être annulé par le biais de l’appel `eventArgs.preventDefault()` .</span><span class="sxs-lookup"><span data-stu-id="04da2-270">This event is cancellable via calling `eventArgs.preventDefault()`.</span></span> <span data-ttu-id="04da2-271">S’il est annulé, le WebView n’effectue pas de navigation.</span><span class="sxs-lookup"><span data-stu-id="04da2-271">If cancelled, the WebView will not perform the navigation.</span></span>


```js
function frameNavigationStartingHandler(navigationEventArgs) {
    // Cancel all navigations that don't meet some criteria.
    if (!navigationEventArgs.uri.startsWith("https://example.com/")) {
        navigationEventArgs.preventDefault();
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameNavigationStarting", frameNavigationStartingHandler);
webview.removeEventListener("MSWebViewFrameNavigationStarting", frameNavigationStartingHandler);
```

#### <span data-ttu-id="04da2-272">Informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="04da2-272">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="04da2-273">Interface</span><span class="sxs-lookup"><span data-stu-id="04da2-273">Interface</span></span>** | [<span data-ttu-id="04da2-274">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="04da2-274">NavigationEvent</span></span>](./webview/NavigationEvent.md) |
|**<span data-ttu-id="04da2-275">Synchrone</span><span class="sxs-lookup"><span data-stu-id="04da2-275">Synchronous</span></span>** |<span data-ttu-id="04da2-276">Oui</span><span class="sxs-lookup"><span data-stu-id="04da2-276">Yes</span></span>  |    
|**<span data-ttu-id="04da2-277">BD</span><span class="sxs-lookup"><span data-stu-id="04da2-277">Bubbles</span></span>**     |<span data-ttu-id="04da2-278">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-278">No</span></span> |   
|**<span data-ttu-id="04da2-279">Annulable</span><span class="sxs-lookup"><span data-stu-id="04da2-279">Cancelable</span></span>**  |<span data-ttu-id="04da2-280">Oui</span><span class="sxs-lookup"><span data-stu-id="04da2-280">Yes</span></span> |                 
          
### <span data-ttu-id="04da2-281">MSWebViewLongRunningScriptDetected</span><span class="sxs-lookup"><span data-stu-id="04da2-281">MSWebViewLongRunningScriptDetected</span></span>

<span data-ttu-id="04da2-282">Se produit régulièrement pendant l’exécution d’un script ininterrompu dans le **WebView**, ce qui vous permet d’arrêter le script.</span><span class="sxs-lookup"><span data-stu-id="04da2-282">Occurs periodically during uninterrupted script execution in the **webview**, letting you halt the script.</span></span>

```js
function handler(eventInfo) {
    const stopPageScriptThreshold = 5 * 1000;
    if (eventInfo.executionTime > stopPageScriptThreshold) {
        eventInfo.stopPageScriptExecution = true; // Stop the long running script if it goes over our threshold
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewLongRunningScriptDetected", handler);
webview.removeEventListener("MSWebViewLongRunningScriptDetected", handler);
```

#### <span data-ttu-id="04da2-283">Informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="04da2-283">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="04da2-284">Interface</span><span class="sxs-lookup"><span data-stu-id="04da2-284">Interface</span></span>** | [<span data-ttu-id="04da2-285">LongRunningScriptDetectedEvent</span><span class="sxs-lookup"><span data-stu-id="04da2-285">LongRunningScriptDetectedEvent</span></span>](./webview/LongRunningScriptDetectedEvent.md) |
|**<span data-ttu-id="04da2-286">Synchrone</span><span class="sxs-lookup"><span data-stu-id="04da2-286">Synchronous</span></span>** |<span data-ttu-id="04da2-287">Oui</span><span class="sxs-lookup"><span data-stu-id="04da2-287">Yes</span></span> |    
|**<span data-ttu-id="04da2-288">BD</span><span class="sxs-lookup"><span data-stu-id="04da2-288">Bubbles</span></span>**     |<span data-ttu-id="04da2-289">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-289">No</span></span> |   
|**<span data-ttu-id="04da2-290">Annulable</span><span class="sxs-lookup"><span data-stu-id="04da2-290">Cancelable</span></span>**  |<span data-ttu-id="04da2-291">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-291">No</span></span> |            

### <span data-ttu-id="04da2-292">MSWebViewNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="04da2-292">MSWebViewNavigationCompleted</span></span>

<span data-ttu-id="04da2-293">Indique que la navigation est terminée et que tous les éléments multimédias sont affichés ou qu’il y a eu une erreur de navigation.</span><span class="sxs-lookup"><span data-stu-id="04da2-293">Indicates the navigation is complete, and all media elements are rendered or there was a navigation error.</span></span> <span data-ttu-id="04da2-294">Pour savoir si la navigation a abouti et la propriété webErrorStatus pour plus d’informations sur l’erreur de navigation, consultez la propriété propriétés IsSuccess de l’événement.</span><span class="sxs-lookup"><span data-stu-id="04da2-294">Check the event args isSuccess property to tell if the navigation was successful and the webErrorStatus property for details on the navigation error.</span></span> <span data-ttu-id="04da2-295">Des erreurs de navigation peuvent se produire avant d’obtenir du contenu du réseau, par exemple si le nom d’hôte d’un URI n’est pas résolu dans le cas où l’événement MSWebViewNavigationStarted se déclenche, suivi de l’événement MSWebViewNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="04da2-295">Navigation errors can occur before obtaining any content from the network for instance if the hostname of a URI does not resolve in which case the MSWebViewNavigationStarted event will fire followed by the MSWebViewNavigationCompleted event.</span></span> <span data-ttu-id="04da2-296">Des erreurs de navigation peuvent également se produire après avoir reçu une page d’erreur d’un serveur Web, par exemple une page 404 d’un serveur HTTP dans lequel tous les événements de navigation sont déclenchés, MSWebViewNavigationStarting, MSWebViewContentLoading, MSWebViewDOMContentLoaded, puis MSWebViewNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="04da2-296">Navigation errors may also occur after receiving an error page from a web server, for instance a 404 page from an HTTP server in which case all navigation events will fire, MSWebViewNavigationStarting, MSWebViewContentLoading, MSWebViewDOMContentLoaded, and then MSWebViewNavigationCompleted.</span></span> <span data-ttu-id="04da2-297">Pour indiquer la présence d’une page d’erreur de navigation dans les cas où le serveur Web n’a pas fourni de page d’erreur, vous devez vérifier si MSWebViewContentLoading n’a pas été activé pour une navigation en échec indiquant qu’il n’y a pas de page d’erreur fournie par le serveur.</span><span class="sxs-lookup"><span data-stu-id="04da2-297">To provide an app navigation error page for cases where the web server hasn't provided an error page, you'll need to check if MSWebViewContentLoading hasn't fired for a failed navigation which indicates there is no server provided error page.</span></span>

```js
let hasContent = false;
webview.addEventListener("MSWebViewNavigationStarting", () => { hasContent = false; });
webview.addEventListener("MSWebViewContentLoading", () => { hasContent = true; });

webview.addEventListener("MSWebViewNavigationCompleted", navigationCompletedEventArgs => {
    // Navigation failures may or may not come after getting an error page from the web server.
    // We keep track of the ContentLoading event with hasContent to tell if we have an error page from the server.
    // So we only navigate to our app error page when there's no server provided error page.
    if (!navigationCompletedEventArgs.isSuccess && !hasContent) {
        // Pass our failed URI and error details in the query and the error page script can read it as appropriate.
        webview.navigate("ms-appx-web:///appErrorPage.html?" + 
            "uri=" + encodeURIComponent(navigationCompletedEventArgs.uri) + "&" +
            "webErrorStatus=" + encodeURIComponent(navigationCompletedEventArgs.webErrorStatus));
    }
});
 
// addEventListener syntax
webview.addEventListener("MSWebViewNavigationCompleted", handler);
webview.removeEventListener("MSWebViewNavigationCompleted", handler);
```

#### <span data-ttu-id="04da2-298">Informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="04da2-298">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="04da2-299">Interface</span><span class="sxs-lookup"><span data-stu-id="04da2-299">Interface</span></span>** | [<span data-ttu-id="04da2-300">NavigationCompletedEvent</span><span class="sxs-lookup"><span data-stu-id="04da2-300">NavigationCompletedEvent</span></span>](./webview/NavigationCompletedEvent.md) |
|**<span data-ttu-id="04da2-301">Synchrone</span><span class="sxs-lookup"><span data-stu-id="04da2-301">Synchronous</span></span>** |<span data-ttu-id="04da2-302">Oui</span><span class="sxs-lookup"><span data-stu-id="04da2-302">Yes</span></span>  |    
|**<span data-ttu-id="04da2-303">BD</span><span class="sxs-lookup"><span data-stu-id="04da2-303">Bubbles</span></span>**     |<span data-ttu-id="04da2-304">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-304">No</span></span> |   
|**<span data-ttu-id="04da2-305">Annulable</span><span class="sxs-lookup"><span data-stu-id="04da2-305">Cancelable</span></span>**  |<span data-ttu-id="04da2-306">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-306">No</span></span> |                 
         

### <span data-ttu-id="04da2-307">MSWebViewNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="04da2-307">MSWebViewNavigationStarting</span></span>

<span data-ttu-id="04da2-308">Indique que l' **affichage du WebView** commence.</span><span class="sxs-lookup"><span data-stu-id="04da2-308">Indicates the **webview** is starting to navigate.</span></span> <span data-ttu-id="04da2-309">Ce problème est déclenché avant d’obtenir des ressources du réseau pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="04da2-309">This is fired before obtaining any resources from the network for the navigation.</span></span> <span data-ttu-id="04da2-310">La navigation n’a pas commencé tant que tous les gestionnaires d’événements MSWebViewNavigationStarting n’ont pas terminé.</span><span class="sxs-lookup"><span data-stu-id="04da2-310">The navigation is not started until all MSWebViewNavigationStarting event handlers complete.</span></span> <span data-ttu-id="04da2-311">Cet événement peut être annulé par le biais de l’appel `eventArgs.preventDefault()` .</span><span class="sxs-lookup"><span data-stu-id="04da2-311">This event is cancellable via calling `eventArgs.preventDefault()`.</span></span> <span data-ttu-id="04da2-312">S’il est annulé, le WebView n’effectue pas de navigation.</span><span class="sxs-lookup"><span data-stu-id="04da2-312">If cancelled, the WebView will not perform the navigation.</span></span>


```js
function navigationStartingHandler(navigationEventArgs) {
    // Cancel all navigations that don't meet some criteria.
    if (!navigationEventArgs.uri.startsWith("https://example.com/")) {
        navigationEventArgs.preventDefault();
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewNavigationStarting", navigationStartingHandler);
webview.removeEventListener("MSWebViewNavigationStarting", navigationStartingHandler);
```

#### <span data-ttu-id="04da2-313">Informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="04da2-313">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="04da2-314">Interface</span><span class="sxs-lookup"><span data-stu-id="04da2-314">Interface</span></span>** | [<span data-ttu-id="04da2-315">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="04da2-315">NavigationEvent</span></span>](./webview/NavigationEvent.md) |
|**<span data-ttu-id="04da2-316">Synchrone</span><span class="sxs-lookup"><span data-stu-id="04da2-316">Synchronous</span></span>** |<span data-ttu-id="04da2-317">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-317">No</span></span>  |    
|**<span data-ttu-id="04da2-318">BD</span><span class="sxs-lookup"><span data-stu-id="04da2-318">Bubbles</span></span>**     |<span data-ttu-id="04da2-319">Oui</span><span class="sxs-lookup"><span data-stu-id="04da2-319">Yes</span></span> |   
|**<span data-ttu-id="04da2-320">Annulable</span><span class="sxs-lookup"><span data-stu-id="04da2-320">Cancelable</span></span>**  |<span data-ttu-id="04da2-321">Oui</span><span class="sxs-lookup"><span data-stu-id="04da2-321">Yes</span></span> |      

### <span data-ttu-id="04da2-322">MSWebViewNewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="04da2-322">MSWebViewNewWindowRequested</span></span>

<span data-ttu-id="04da2-323">Déclenché lorsque le contenu du **WebView** tente d’ouvrir une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="04da2-323">Raised when content in **webview** is trying to open a new window.</span></span> <span data-ttu-id="04da2-324">Si l’événement n’est pas annulé, le WebView lancera l’URI de la nouvelle demande de fenêtre dans le navigateur par défaut de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="04da2-324">If the event isn't cancelled the webview will launch the URI of the new window request in the user's default browser.</span></span>

```js
function handler(eventInfo) {
    // Prevent the webview from opening URIs in the default browser.
    eventInfo.preventDefault();
    
    // Only allow https://example.com/ to open new windows.
    if (eventInfo.referer === "https://example.com/") {
        // Perform some custom handling of the URI.
        openUri(eventInfo.uri);
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewNewWindowRequested", handler);
webview.removeEventListener("MSWebViewNewWindowRequested", handler);
```

#### <span data-ttu-id="04da2-325">Informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="04da2-325">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="04da2-326">Interface</span><span class="sxs-lookup"><span data-stu-id="04da2-326">Interface</span></span>** | [<span data-ttu-id="04da2-327">NavigationEventWithReferrer</span><span class="sxs-lookup"><span data-stu-id="04da2-327">NavigationEventWithReferrer</span></span>](./webview/NavigationEventWithReferrer.md) |
|**<span data-ttu-id="04da2-328">Synchrone</span><span class="sxs-lookup"><span data-stu-id="04da2-328">Synchronous</span></span>** |<span data-ttu-id="04da2-329">Oui</span><span class="sxs-lookup"><span data-stu-id="04da2-329">Yes</span></span>  |    
|**<span data-ttu-id="04da2-330">BD</span><span class="sxs-lookup"><span data-stu-id="04da2-330">Bubbles</span></span>**     |<span data-ttu-id="04da2-331">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-331">No</span></span> |   
|**<span data-ttu-id="04da2-332">Annulable</span><span class="sxs-lookup"><span data-stu-id="04da2-332">Cancelable</span></span>**  |<span data-ttu-id="04da2-333">Oui</span><span class="sxs-lookup"><span data-stu-id="04da2-333">Yes</span></span> |                 
           

### <span data-ttu-id="04da2-334">MSWebViewPermissionRequested</span><span class="sxs-lookup"><span data-stu-id="04da2-334">MSWebViewPermissionRequested</span></span>

<span data-ttu-id="04da2-335">Indique que le contenu du **WebView** tente d’accéder à des fonctionnalités (par exemple, géolocalisation ou accès par verrouillage de pointeur) qui nécessitent une autorisation de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="04da2-335">Indicates that content in the **webview**  is trying to access functionality (such as geolocation, or pointer lock access) that normally requires end-user permissions.</span></span> <span data-ttu-id="04da2-336">Si aucun gestionnaire d’événements n’est inscrit ou si le gestionnaire d’événements n’appelle pas eventArgs. permissionRequest. allow (), ajourne () ou Deny (), par défaut, la demande d’autorisation est refusée.</span><span class="sxs-lookup"><span data-stu-id="04da2-336">If no event handler is registered or if the event handler doesn't call eventArgs.permissionRequest.allow(), defer(), or deny(), then by default the permission request will be denied.</span></span> <span data-ttu-id="04da2-337">Si vous avez besoin de décider si une autorisation est accordée ou refusée de manière asynchrone par exemple, si vous avez besoin d’inviter l’utilisateur, utilisez eventArgs. permissionRequest. Defer ().</span><span class="sxs-lookup"><span data-stu-id="04da2-337">If you need to decide if permission is allowed or denied asynchronously for instance if you need to prompt the user, use eventArgs.permissionRequest.defer().</span></span> <span data-ttu-id="04da2-338">La demande d’autorisation est différée jusqu’à ce que vous utilisiez WebView. getDeferredPermissionRequestById ou WebView. getDeferredPermissionRequests, et appelez allow () ou Deny () sur le DeferredPermissionRequest avec la valeur ID correspondante.</span><span class="sxs-lookup"><span data-stu-id="04da2-338">The permission request will be deferred until you use webview.getDeferredPermissionRequestById or webview.getDeferredPermissionRequests and call allow() or deny() on the DeferredPermissionRequest with the corresponding id value.</span></span>

```js
webview.addEventListener("MSWebViewPermissionRequested", permissionRequestedEventArgs => {
    const permissionRequest = permissionRequestedEventArgs.permissionRequest;
    switch (permissionRequest.type) {
        case "geolocation":
        case "media":
        case "pointerlock":
        case "webnotifications":
        case "screen":
        case "immersiveview":
            if (permissionRequest.uri.startsWith("https://www.example.com/")) {
                // Implicitly trust particular URI
                permissionRequest.allow();
            }
            else if (permissionRequest.uri.startsWith("https://")) {
                // Defer the request so we can ask the user to allow or deny the request
                permissionRequest.defer();
                // Later we'll need to use webview.getDeferredPermissionRequestById for this
                // request and call allow or deny.
                promptUserForDeferredPermissionRequest(
                    permissionRequest.id,
                    permissionRequest.uri,
                    permissionRequest.type);
            }
            else {
                // Implicitly deny non-https URIs
                permissionRequest.deny();
            }
            break;

        case "unlimitedIndexedDBQuota":
        default:
            permissionRequest.deny();
            break;
    }
});

// addEventListener syntax
webview.addEventListener("MSWebViewPermissionRequested", handler);
webview.removeEventListener("MSWebViewPermissionRequested", handler);
```

#### <span data-ttu-id="04da2-339">Informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="04da2-339">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="04da2-340">Interface</span><span class="sxs-lookup"><span data-stu-id="04da2-340">Interface</span></span>** | [<span data-ttu-id="04da2-341">PermissionRequestedEvent</span><span class="sxs-lookup"><span data-stu-id="04da2-341">PermissionRequestedEvent</span></span>](./webview/PermissionRequestedEvent.md) |
|**<span data-ttu-id="04da2-342">Synchrone</span><span class="sxs-lookup"><span data-stu-id="04da2-342">Synchronous</span></span>** |<span data-ttu-id="04da2-343">Oui</span><span class="sxs-lookup"><span data-stu-id="04da2-343">Yes</span></span>  |    
|**<span data-ttu-id="04da2-344">BD</span><span class="sxs-lookup"><span data-stu-id="04da2-344">Bubbles</span></span>**     |<span data-ttu-id="04da2-345">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-345">No</span></span> |   
|**<span data-ttu-id="04da2-346">Annulable</span><span class="sxs-lookup"><span data-stu-id="04da2-346">Cancelable</span></span>**  |<span data-ttu-id="04da2-347">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-347">No</span></span> |    


### <span data-ttu-id="04da2-348">MSWebViewProcessExited</span><span class="sxs-lookup"><span data-stu-id="04da2-348">MSWebViewProcessExited</span></span>

<span data-ttu-id="04da2-349">Indique que le processus du composant **WebView** a crashé.</span><span class="sxs-lookup"><span data-stu-id="04da2-349">Indicates that the **webview** component process crashsed.</span></span> <span data-ttu-id="04da2-350">Cela ne s’applique qu’à un WebView hors processus.</span><span class="sxs-lookup"><span data-stu-id="04da2-350">This is only relevant for an out-of-process WebView.</span></span> <span data-ttu-id="04da2-351">Reportez-vous à la section Remarques sur la création d’un WebView hors processus plutôt qu’un WebView in-process.</span><span class="sxs-lookup"><span data-stu-id="04da2-351">See the Remarks section for how to create an out-of-process WebView as opposed to an in-process WebView.</span></span> <span data-ttu-id="04da2-352">Après le déclenchement de cet événement, le WebView correspondant est mis dans un État bloqué.</span><span class="sxs-lookup"><span data-stu-id="04da2-352">After this event fires, the corresponding WebView is put into a crashed state.</span></span> <span data-ttu-id="04da2-353">L’appel de la plupart des méthodes spécifiques d’affichage WebView ou l’accès à la plupart des propriétés spécifiques d’affichage sur un WebView bloqué lèvera une exception.</span><span class="sxs-lookup"><span data-stu-id="04da2-353">Calling most WebView specific methods or accessing most WebView specific properties on a crashed WebView will throw an exception.</span></span> <span data-ttu-id="04da2-354">Pour résoudre ce problème, supprimez le WebView bloqué du DOM et remplacez-le par un nouveau WebView.</span><span class="sxs-lookup"><span data-stu-id="04da2-354">To recover from this event, remove the crashed WebView from the DOM and replace it with a new WebView.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewProcessExited", handler);
webview.removeEventListener("MSWebViewProcessExited", handler);
```

#### <span data-ttu-id="04da2-355">Informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="04da2-355">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="04da2-356">Interface</span><span class="sxs-lookup"><span data-stu-id="04da2-356">Interface</span></span>** | **<span data-ttu-id="04da2-357">Événement</span><span class="sxs-lookup"><span data-stu-id="04da2-357">Event</span></span>** |
|**<span data-ttu-id="04da2-358">Synchrone</span><span class="sxs-lookup"><span data-stu-id="04da2-358">Synchronous</span></span>** |<span data-ttu-id="04da2-359">Oui</span><span class="sxs-lookup"><span data-stu-id="04da2-359">Yes</span></span> |    
|**<span data-ttu-id="04da2-360">BD</span><span class="sxs-lookup"><span data-stu-id="04da2-360">Bubbles</span></span>**     |<span data-ttu-id="04da2-361">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-361">No</span></span> |   
|**<span data-ttu-id="04da2-362">Annulable</span><span class="sxs-lookup"><span data-stu-id="04da2-362">Cancelable</span></span>**  |<span data-ttu-id="04da2-363">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-363">No</span></span> |      


### <span data-ttu-id="04da2-364">MSWebViewWebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="04da2-364">MSWebViewWebResourceRequested</span></span>

<span data-ttu-id="04da2-365">Déclenché lorsqu’une page à l’intérieur de l’élément **WebView** demande une ressource.</span><span class="sxs-lookup"><span data-stu-id="04da2-365">Raised when a page inside the **webview** element requests a resource.</span></span>

```js
// A handler that completes synchronously with a custom HTTP response built from a string.
function handlerWithSyncString(webResourceRequestedEventArgs) {
    // Only provide custom HTTP responses for particular HTTP requests
    if (webResourceRequestedEventArgs.args.request.requestUri.absoluteUri === "https://www.bing.com/") {
        const Http = Windows.Web.Http;
        // Create the custom response using a string
        webResourceRequestedEventArgs.args.response = new Http.HttpResponseMessage(Http.HttpStatusCode.ok);
        webResourceRequestedEventArgs.args.response.content = new Http.HttpStringContent("<H1>Example</H1>");
    }
});

// A more complicated handler that completes asynchronously with a custom HTTP response built from a stream.
function handlerWithAsyncStream(webResourceRequestedEventArgs) {
    // Only provide custom HTTP responses for particular HTTP requests
    if (webResourceRequestedEventArgs.args.request.requestUri.absoluteUri === "https://www.bing.com/") {
        // Take a deferral on the WebResourceRequested event so that we can create the custom HTTP response asynchronously.
        const deferral = webResourceRequestedEventArgs.args.getDeferral();

        // Use fetch to get a Blob of the content of the URI
        fetch("ms-appx:///replacement.html").then(fetchResponse => {
            return fetchResponse.blob();
        }).then(fetchResponseBlob => {
            const Http = Windows.Web.Http;
            webResourceRequestedEventArgs.args.response = new Http.HttpResponseMessage(
                Http.HttpStatusCode.ok);

            // Use Blob.msDetachStream to convert the Blob to a Windows.Storage.Streams.IInputStream
            webResourceRequestedEventArgs.args.response.content = new Http.HttpStreamContent(
                fetchResponseBlob.msDetachStream());

        }).finally(() => {
            // Use a finally call to complete the deferral so even if there is an error we will unblock the event.
            deferral.complete();
        });
    }
});
 
// addEventListener syntax
webview.addEventListener("MSWebViewWebResourceRequested", handler);
webview.removeEventListener("MSWebViewWebResourceRequested", handler);
```

#### <span data-ttu-id="04da2-366">Informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="04da2-366">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="04da2-367">Interface</span><span class="sxs-lookup"><span data-stu-id="04da2-367">Interface</span></span>** | [<span data-ttu-id="04da2-368">WebResourceRequestedEvent</span><span class="sxs-lookup"><span data-stu-id="04da2-368">WebResourceRequestedEvent</span></span>](./webview/WebResourceRequestedEvent.md) |
|**<span data-ttu-id="04da2-369">Synchrone</span><span class="sxs-lookup"><span data-stu-id="04da2-369">Synchronous</span></span>** |<span data-ttu-id="04da2-370">Oui</span><span class="sxs-lookup"><span data-stu-id="04da2-370">Yes</span></span> |    
|**<span data-ttu-id="04da2-371">BD</span><span class="sxs-lookup"><span data-stu-id="04da2-371">Bubbles</span></span>**     |<span data-ttu-id="04da2-372">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-372">No</span></span> |   
|**<span data-ttu-id="04da2-373">Annulable</span><span class="sxs-lookup"><span data-stu-id="04da2-373">Cancelable</span></span>**  |<span data-ttu-id="04da2-374">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-374">No</span></span> |      


### <span data-ttu-id="04da2-375">MSWebViewScriptNotify</span><span class="sxs-lookup"><span data-stu-id="04da2-375">MSWebViewScriptNotify</span></span>

<span data-ttu-id="04da2-376">Déclenché lorsqu’une page à l’intérieur de l’élément **WebView** appelle la méthode **Window. external. Notify** .</span><span class="sxs-lookup"><span data-stu-id="04da2-376">Raised when a page inside the **webview** element calls the **window.external.notify** method.</span></span> <span data-ttu-id="04da2-377">La méthode Window. external. Notify est uniquement disponible pour les documents comportant des URI qui correspondent aux règles du ApplicationContentUriRules manifest’s de l’application ou qui a été autorisé par programmation via la définition de WebView. Settings. isScriptNotifyAllowed sur true.</span><span class="sxs-lookup"><span data-stu-id="04da2-377">The window.external.notify method is only available to documents with URIs that match rules in the app's manifest's ApplicationContentUriRules or that has been programatically allowed via setting webview.settings.isScriptNotifyAllowed to true.</span></span> <span data-ttu-id="04da2-378">Par ailleurs, Window. external. Notify n’est disponible que pour le document de niveau supérieur de la WebView.</span><span class="sxs-lookup"><span data-stu-id="04da2-378">Additionally window.external.notify is only available to the webview's top level document.</span></span>

```js
webview.addEventListener("MSWebViewScriptNotify", eventInfo => {
    console.log("The URI " + eventInfo.callingUri + 
        " has sent notification " + eventInfo.value);
});

// Allow the next URI to which we navigate access to window.external.notify
webview.settings.isScriptNotifyAllowed = true;
webview.navigate("https://example.com/");

webview.addEventListener("MSWebViewNavigationCompleted", () => {
    // Inject script to the webview that will send a notification back.
    const asyncOp = webview.invokeScriptAsync("eval", "window.external.notify('example notification')");
    asyncOp.start();
});
```

#### <span data-ttu-id="04da2-379">Informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="04da2-379">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="04da2-380">Interface</span><span class="sxs-lookup"><span data-stu-id="04da2-380">Interface</span></span>** | [<span data-ttu-id="04da2-381">ScriptNotifyEvent</span><span class="sxs-lookup"><span data-stu-id="04da2-381">ScriptNotifyEvent</span></span>](./webview/ScriptNotifyEvent.md) |
|**<span data-ttu-id="04da2-382">Synchrone</span><span class="sxs-lookup"><span data-stu-id="04da2-382">Synchronous</span></span>** |<span data-ttu-id="04da2-383">Oui</span><span class="sxs-lookup"><span data-stu-id="04da2-383">Yes</span></span>  |    
|**<span data-ttu-id="04da2-384">BD</span><span class="sxs-lookup"><span data-stu-id="04da2-384">Bubbles</span></span>**     |<span data-ttu-id="04da2-385">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-385">No</span></span> |   
|**<span data-ttu-id="04da2-386">Annulable</span><span class="sxs-lookup"><span data-stu-id="04da2-386">Cancelable</span></span>**  |<span data-ttu-id="04da2-387">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-387">No</span></span> |      

### <span data-ttu-id="04da2-388">MSWebViewUnsafeContentWarningDisplaying</span><span class="sxs-lookup"><span data-stu-id="04da2-388">MSWebViewUnsafeContentWarningDisplaying</span></span>

<span data-ttu-id="04da2-389">Se produit lorsque l' **affichage** Web affiche un avertissement pour le contenu signalé comme non sécurisé par le filtre SmartScreen.</span><span class="sxs-lookup"><span data-stu-id="04da2-389">Occurs when the **webview** shows a warning page for content that was reported as unsafe by SmartScreen Filter.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewUnsafeContentWarningDisplaying", handler);
webview.removeEventListener("MSWebViewUnsafeContentWarningDisplaying", handler);
```

#### <span data-ttu-id="04da2-390">Informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="04da2-390">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="04da2-391">Interface</span><span class="sxs-lookup"><span data-stu-id="04da2-391">Interface</span></span>** | **<span data-ttu-id="04da2-392">Événement</span><span class="sxs-lookup"><span data-stu-id="04da2-392">Event</span></span>** |
|**<span data-ttu-id="04da2-393">Synchrone</span><span class="sxs-lookup"><span data-stu-id="04da2-393">Synchronous</span></span>** |<span data-ttu-id="04da2-394">Oui</span><span class="sxs-lookup"><span data-stu-id="04da2-394">Yes</span></span> |    
|**<span data-ttu-id="04da2-395">BD</span><span class="sxs-lookup"><span data-stu-id="04da2-395">Bubbles</span></span>**     |<span data-ttu-id="04da2-396">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-396">No</span></span> |   
|**<span data-ttu-id="04da2-397">Annulable</span><span class="sxs-lookup"><span data-stu-id="04da2-397">Cancelable</span></span>**  |<span data-ttu-id="04da2-398">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-398">No</span></span> |    

### <span data-ttu-id="04da2-399">MSWebViewUnsupportedUriSchemeIdentified</span><span class="sxs-lookup"><span data-stu-id="04da2-399">MSWebViewUnsupportedUriSchemeIdentified</span></span>

<span data-ttu-id="04da2-400">Déclenché lors de la navigation vers un URI (Uniform Resource Identifier) que le **WebView** ne prend pas en charge.</span><span class="sxs-lookup"><span data-stu-id="04da2-400">Raised when there is navigation to an Uniform Resource Identifier (URI) that the **webview** does not support.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewUnsupportedUriSchemeIdentified", handler);
webview.removeEventListener("MSWebViewUnsupportedUriSchemeIdentified", handler);
```

#### <span data-ttu-id="04da2-401">Informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="04da2-401">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="04da2-402">Interface</span><span class="sxs-lookup"><span data-stu-id="04da2-402">Interface</span></span>** | [<span data-ttu-id="04da2-403">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="04da2-403">NavigationEvent</span></span>](./webview/NavigationEvent.md) |
|**<span data-ttu-id="04da2-404">Synchrone</span><span class="sxs-lookup"><span data-stu-id="04da2-404">Synchronous</span></span>** |<span data-ttu-id="04da2-405">Oui</span><span class="sxs-lookup"><span data-stu-id="04da2-405">Yes</span></span>  |    
|**<span data-ttu-id="04da2-406">BD</span><span class="sxs-lookup"><span data-stu-id="04da2-406">Bubbles</span></span>**     |<span data-ttu-id="04da2-407">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-407">No</span></span> |   
|**<span data-ttu-id="04da2-408">Annulable</span><span class="sxs-lookup"><span data-stu-id="04da2-408">Cancelable</span></span>**  |<span data-ttu-id="04da2-409">Oui</span><span class="sxs-lookup"><span data-stu-id="04da2-409">Yes</span></span> |     

### <span data-ttu-id="04da2-410">MSWebViewUnviewableContentIdentified</span><span class="sxs-lookup"><span data-stu-id="04da2-410">MSWebViewUnviewableContentIdentified</span></span>

<span data-ttu-id="04da2-411">Déclenché lorsque le **WebView** tente d’accéder au contenu Web avec un type de contenu non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="04da2-411">Raised when the **webview** attempts to navigate to web content with an unsupported content type.</span></span> <span data-ttu-id="04da2-412">Par exemple, les fichiers PDF ne sont actuellement pas pris en charge par le biais de l’affichage WebView et des navigations vers des documents PDF et déclenchent plutôt cet événement.</span><span class="sxs-lookup"><span data-stu-id="04da2-412">For example, PDFs are currently not supported by webview and navigations to PDF documents will not navigate and instead raise this event.</span></span>

```js
function handler(args) {
    if (args.mediaType === "application/pdf") {
        Windows.System.Launcher.launchUriAsync(new Windows.Foundation.Uri(args.uri));
    }
}

// addEventListener syntax
webview.addEventListener("MSWebViewUnviewableContentIdentified", handler);
webview.removeEventListener("MSWebViewUnviewableContentIdentified", handler);
```

#### <span data-ttu-id="04da2-413">Informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="04da2-413">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="04da2-414">Interface</span><span class="sxs-lookup"><span data-stu-id="04da2-414">Interface</span></span>** | [<span data-ttu-id="04da2-415">UnviewableContentIdentifiedEvent</span><span class="sxs-lookup"><span data-stu-id="04da2-415">UnviewableContentIdentifiedEvent</span></span>](./webview/UnviewableContentIdentifiedEvent.md) |
|**<span data-ttu-id="04da2-416">Synchrone</span><span class="sxs-lookup"><span data-stu-id="04da2-416">Synchronous</span></span>** |<span data-ttu-id="04da2-417">Oui</span><span class="sxs-lookup"><span data-stu-id="04da2-417">Yes</span></span>  |    
|**<span data-ttu-id="04da2-418">BD</span><span class="sxs-lookup"><span data-stu-id="04da2-418">Bubbles</span></span>**     |<span data-ttu-id="04da2-419">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-419">No</span></span> |   
|**<span data-ttu-id="04da2-420">Annulable</span><span class="sxs-lookup"><span data-stu-id="04da2-420">Cancelable</span></span>**  |<span data-ttu-id="04da2-421">Non</span><span class="sxs-lookup"><span data-stu-id="04da2-421">No</span></span> |                 
         

## <span data-ttu-id="04da2-422">Méthodes</span><span class="sxs-lookup"><span data-stu-id="04da2-422">Methods</span></span>

### <span data-ttu-id="04da2-423">addWebAllowedObject</span><span class="sxs-lookup"><span data-stu-id="04da2-423">addWebAllowedObject</span></span>

<span data-ttu-id="04da2-424">Ajoute un objet Windows Runtime natif en tant que paramètre global au document de niveau supérieur au sein d’un **WebView**.</span><span class="sxs-lookup"><span data-stu-id="04da2-424">Adds a native Windows Runtime object as a global parameter to the top-level document inside of a **webview**.</span></span>

<span data-ttu-id="04da2-425">L’objet n’est pas injecté dans le document actuel, mais plutôt dans le document de niveau supérieur suivant sur lequel l’affichage WebView se déplace.</span><span class="sxs-lookup"><span data-stu-id="04da2-425">The object is not injected into the current document, but rather the next top-level document to which the webview navigates.</span></span> <span data-ttu-id="04da2-426">L’objet est injecté avant qu’un script du document HTML ne s’exécute, afin que vous puissiez compter sur l’objet dans le script global de votre document.</span><span class="sxs-lookup"><span data-stu-id="04da2-426">The object is injected before any script from the HTML document runs so you can rely on the object in your document's global script.</span></span>

<span data-ttu-id="04da2-427">Vous devez utiliser addWebAllowedObject pendant un événement MSWebViewNavigationStarting ou avant d’appeler explicitement une méthode Navigate.</span><span class="sxs-lookup"><span data-stu-id="04da2-427">You should use addWebAllowedObject either during an MSWebViewNavigationStarting event or before explicitly calling a navigate method.</span></span> <span data-ttu-id="04da2-428">Dans ces cas, l’objet est injecté dans le document de la navigation correspondante.</span><span class="sxs-lookup"><span data-stu-id="04da2-428">In these cases the object is injected into the document of the corresponding navigation.</span></span> <span data-ttu-id="04da2-429">Dans un autre contexte, vous ne pouvez pas être sûr de savoir quel document vous injectera.</span><span class="sxs-lookup"><span data-stu-id="04da2-429">Calling it in some other context, you don't have a way to be certain into what document you'll inject your object.</span></span>

<span data-ttu-id="04da2-430">L’appel de addWebAllowedObject plusieurs fois dans une ligne permet d’injecter plusieurs objets dans le document.</span><span class="sxs-lookup"><span data-stu-id="04da2-430">Calling addWebAllowedObject multiple times in a row will inject multiple objects into the document.</span></span> <span data-ttu-id="04da2-431">Si vous l’appelez à la fois avant un appel de navigation explicite, puis de nouveau pendant l’événement MSWebViewNavigationStarting correspondant, les deux appels aboutissent et vous avez plusieurs objets injectés.</span><span class="sxs-lookup"><span data-stu-id="04da2-431">If you call it both before an explicit navigate call and then again during the corresponding MSWebViewNavigationStarting event, both calls will succeed and you'll have multiple objects injected.</span></span> <span data-ttu-id="04da2-432">Si vous appelez plusieurs fois avec le même paramètre de nom, le dernier appel WINS et les appels précédents avec ce nom sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="04da2-432">If you call multiple times with the same name parameter, the last call wins and the previous calls with that name are ignored.</span></span>

<span data-ttu-id="04da2-433">En cas d’échec de la navigation ou d’une redirection, les appels addWebAllowedObject pour cette navigation sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="04da2-433">If a navigate fails or is redirected, the addWebAllowedObject calls for that navigation are ignored.</span></span> <span data-ttu-id="04da2-434">Si vous souhaitez gérer les redirections, vous pouvez vous abonner à l’événement MSWebViewNavigationStarting pour rediriger et appeler de nouveau addWebAllowedObject en fonction de ce qui est approprié pour votre application.</span><span class="sxs-lookup"><span data-stu-id="04da2-434">If you want to handle redirects you can subscribe to the MSWebViewNavigationStarting event watch for redirects and call addWebAllowedObject again according to whatever criteria is appropriate for your application.</span></span> <span data-ttu-id="04da2-435">De même, une fois qu’un document navigue vers l’extérieur, les objets injectés via addWebAllowedObject pour ce document ne seront pas reportés au document suivant et vous devrez appeler addWebAllowedObject explicitement si vous souhaitez qu’ils reportent le contrôle.</span><span class="sxs-lookup"><span data-stu-id="04da2-435">Similarly, once a document navigates away any objects injected via addWebAllowedObject for that document will not carry over to the next document and you'll need to explicitly call addWebAllowedObject if you want them to carry over.</span></span>

<span data-ttu-id="04da2-436">Si vous appelez addWebAllowedObject pour un document sans accès WinRT, ou s’il dispose d' [AllowForWebOnly accès via ApplicationContentUriRules](/uwp/schemas/appxpackage/uapmanifestschema/element-uap-rule) , l’objet sera injecté uniquement si l’objet a l’attribut de métadonnées Windows. Foundation. Metadata. AllowForWeb.</span><span class="sxs-lookup"><span data-stu-id="04da2-436">If you call addWebAllowedObject for a document that has no WinRT access otherwise, or if it has [AllowForWebOnly access via ApplicationContentUriRules](/uwp/schemas/appxpackage/uapmanifestschema/element-uap-rule) then the object will only be injected if the object has the Windows.Foundation.Metadata.AllowForWeb metadata attribute.</span></span> <span data-ttu-id="04da2-437">Dans le cas contraire, une erreur est signalée et une erreur est signalée à la console développeur JavaScript.</span><span class="sxs-lookup"><span data-stu-id="04da2-437">Otherwise injection will fail and an error will be reported to the JavaScript developer console.</span></span> <span data-ttu-id="04da2-438">S’il est appelé sur un document qui dispose d’un accès WinRT complet, l’objet sera injecté indépendamment de l’attribut AllowForWeb.</span><span class="sxs-lookup"><span data-stu-id="04da2-438">If called on a document that has full WinRT access, then the object will be injected regardless of the AllowForWeb attribute.</span></span> 

<span data-ttu-id="04da2-439">Par ailleurs, l’objet doit implémenter l’interface IAgileObject.</span><span class="sxs-lookup"><span data-stu-id="04da2-439">Additionally, the object must implement the IAgileObject interface.</span></span> <span data-ttu-id="04da2-440">En effet, les éléments WebView HTML et HTML s’exécutent sur les threads d’affichage de votre application et le thread JavaScript de l’application WebView est un thread thread asta différent et nous voulons encourager les développeurs d’applications à s’assurer que leur objet peut s’exécuter sur le thread JavaScript sans bloquer le thread d’affichage d’application, dans la mesure du possible.</span><span class="sxs-lookup"><span data-stu-id="04da2-440">This is because the XAML and HTML webview elements run on their app's ASTA view threads and the WebView's JavaScript thread is a different ASTA thread and we want to encourage app developers to ensure their object can run on the JavaScript thread without blocking the app view thread if possible.</span></span>

<span data-ttu-id="04da2-441">Le paramètre Name doit être un nom de propriété JavaScript valide, sinon l’appel échoue en silence.</span><span class="sxs-lookup"><span data-stu-id="04da2-441">The name parameter must be a valid JavaScript property name otherwise the call will fail silently.</span></span> <span data-ttu-id="04da2-442">S’il s’agit d’une propriété qui existe déjà sur l’objet global, cette propriété est écrasée si la propriété est configurable.</span><span class="sxs-lookup"><span data-stu-id="04da2-442">If the name is of a property that already exists on the global object then that property is overwritten if the property is configurable.</span></span> <span data-ttu-id="04da2-443">Les propriétés non configurables sur l’objet global ne sont pas écrasées et l’appel addWebAllowedObject échoue en silence.</span><span class="sxs-lookup"><span data-stu-id="04da2-443">Non-configurable properties on the global object are not overwritten and the addWebAllowedObject call fails silently.</span></span> <span data-ttu-id="04da2-444">Les propriétés JavaScript créées via addWebAllowedObject sont modifiables, configurables et Enumerable.</span><span class="sxs-lookup"><span data-stu-id="04da2-444">JavaScript properties created via addWebAllowedObject are writable, configurable, and enumerable.</span></span>

```js
let name = "exampleProperty";
webview.addWebAllowedObject(name, applicationObject);
webview.navigate("https://example.com/"); // applicationObject will be available as window.exampleProperty on https://example.com
```

#### <span data-ttu-id="04da2-445">Parameters</span><span class="sxs-lookup"><span data-stu-id="04da2-445">Parameters</span></span>
*<span data-ttu-id="04da2-446">name</span><span class="sxs-lookup"><span data-stu-id="04da2-446">name</span></span>*
* <span data-ttu-id="04da2-447">Type: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="04da2-447">Type: **String**</span></span>
* <span data-ttu-id="04da2-448">Nom de l’objet à exposer au document dans le **WebView**.</span><span class="sxs-lookup"><span data-stu-id="04da2-448">The name of the object to expose to the document in the **webview**.</span></span>

*<span data-ttu-id="04da2-449">applicationObject</span><span class="sxs-lookup"><span data-stu-id="04da2-449">applicationObject</span></span>*
* <span data-ttu-id="04da2-450">Type: **objet**</span><span class="sxs-lookup"><span data-stu-id="04da2-450">Type: **Object**</span></span>
* <span data-ttu-id="04da2-451">Objet à exposer dans le document dans le **WebView**.</span><span class="sxs-lookup"><span data-stu-id="04da2-451">The object to expose to the document in the **webview**.</span></span>

#### <span data-ttu-id="04da2-452">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="04da2-452">Return value</span></span>
<span data-ttu-id="04da2-453">Cette méthode ne renvoie pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="04da2-453">This method does not return a value.</span></span>

#### <span data-ttu-id="04da2-454">Fonctionnalités et exigences supplémentaires</span><span class="sxs-lookup"><span data-stu-id="04da2-454">Additional features and requirements</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="04da2-455">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04da2-455">Minimum supported client</span></span>** |<span data-ttu-id="04da2-456">Windows 10 [applications du Windows Store uniquement]</span><span class="sxs-lookup"><span data-stu-id="04da2-456">Windows10 [Windows Store apps only]</span></span> |    
|**<span data-ttu-id="04da2-457">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04da2-457">Minimum supported server</span></span>** |<span data-ttu-id="04da2-458">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="04da2-458">None supported</span></span> |   
|**<span data-ttu-id="04da2-459">Téléphone minimum pris en charge</span><span class="sxs-lookup"><span data-stu-id="04da2-459">Minimum supported phone</span></span>**  |<span data-ttu-id="04da2-460">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="04da2-460">None supported</span></span> |  

### <span data-ttu-id="04da2-461">buildLocalStreamUri</span><span class="sxs-lookup"><span data-stu-id="04da2-461">buildLocalStreamUri</span></span>

<span data-ttu-id="04da2-462">Crée un URI que vous pouvez transmettre à [navigateToLocalStreamUri](#methods).</span><span class="sxs-lookup"><span data-stu-id="04da2-462">Creates a URI that you can pass to [navigateToLocalStreamUri](#methods).</span></span>

```js
var string = webview.buildLocalStreamUri(contentIdentifier, relativePath);
```

#### <span data-ttu-id="04da2-463">Parameters</span><span class="sxs-lookup"><span data-stu-id="04da2-463">Parameters</span></span>
*<span data-ttu-id="04da2-464">contentIdentifier</span><span class="sxs-lookup"><span data-stu-id="04da2-464">contentIdentifier</span></span>*
* <span data-ttu-id="04da2-465">Type: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="04da2-465">Type: **String**</span></span>
* <span data-ttu-id="04da2-466">Identificateur unique pour le contenu référencé par l’URI.</span><span class="sxs-lookup"><span data-stu-id="04da2-466">A unique identifier for the content the URI is referencing.</span></span> <span data-ttu-id="04da2-467">Cela définit la racine de l’URI.</span><span class="sxs-lookup"><span data-stu-id="04da2-467">This defines the root of the URI.</span></span>

*<span data-ttu-id="04da2-468">Entraîne</span><span class="sxs-lookup"><span data-stu-id="04da2-468">relativePath</span></span>*
* <span data-ttu-id="04da2-469">Type: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="04da2-469">Type: **String**</span></span>
* <span data-ttu-id="04da2-470">Le chemin d’accès à la ressource, par rapport à la racine.</span><span class="sxs-lookup"><span data-stu-id="04da2-470">The path to the resource, relative to the root.</span></span>

#### <span data-ttu-id="04da2-471">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="04da2-471">Return value</span></span>
<span data-ttu-id="04da2-472">Type: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="04da2-472">Type: **String**</span></span>

<span data-ttu-id="04da2-473">URI créé en combinant et en normalisant *contentIdentifier* et *relativePath*.</span><span class="sxs-lookup"><span data-stu-id="04da2-473">The URI created by combining and normalizing the *contentIdentifier* and *relativePath*.</span></span>

#### <span data-ttu-id="04da2-474">Exemple</span><span class="sxs-lookup"><span data-stu-id="04da2-474">Example</span></span>

<span data-ttu-id="04da2-475">L’exemple suivant illustre un cas d’utilisation classique.</span><span class="sxs-lookup"><span data-stu-id="04da2-475">The following example illustrates a typical use case.</span></span> 

```js
var webview = document.createElement("x-ms-webview"); //Instantiate the webview element
var localStreamUri = webview.buildLocalStreamUri(contentIdentifier, relativePath); //Create URI to pass to navigateToLocalStreamUri method
webview.navigateToLocalStreamUri(localStreamUri, streamResolver); //Load the local web content 
```  

### <span data-ttu-id="04da2-476">capturePreviewToBlobAsync</span><span class="sxs-lookup"><span data-stu-id="04da2-476">capturePreviewToBlobAsync</span></span>

<span data-ttu-id="04da2-477">Crée une image de l' [élément WebView](./webview.md) actuel et l’écrit dans l’élément image spécifié.</span><span class="sxs-lookup"><span data-stu-id="04da2-477">Creates an image of the current [webview element](./webview.md) and write it to the specified image element.</span></span>

```js
var capturePreviewToBlobAsync = webview.capturePreviewToBlobAsync();
```

#### <span data-ttu-id="04da2-478">Parameters</span><span class="sxs-lookup"><span data-stu-id="04da2-478">Parameters</span></span>
<span data-ttu-id="04da2-479">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="04da2-479">This method has no parameters.</span></span>

#### <span data-ttu-id="04da2-480">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="04da2-480">Return value</span></span>
<span data-ttu-id="04da2-481">Type: **MSWebViewAsyncOperation**</span><span class="sxs-lookup"><span data-stu-id="04da2-481">Type: **MSWebViewAsyncOperation**</span></span>

<span data-ttu-id="04da2-482">Un objet **MSWebViewAsyncOperation** qui, lorsqu’il se termine, fournit un objet **BLOB** contenant l’image.</span><span class="sxs-lookup"><span data-stu-id="04da2-482">An **MSWebViewAsyncOperation** object that, when it completes, provides a **Blob** object that contains the image.</span></span> <span data-ttu-id="04da2-483">Lorsque vous utilisez **capturePreviewToBlobAsync**, vous devez définir des gestionnaires de réussite et d’erreur après la définition de l’opération.</span><span class="sxs-lookup"><span data-stu-id="04da2-483">When using **capturePreviewToBlobAsync**, you need to define success and error handlers after defining the operation.</span></span> <span data-ttu-id="04da2-484">Après avoir appliqué les gestionnaires d’événements, appelez la méthode Start sur l’objet [MSWebViewAsyncOperation](./webview/MSWebViewAsyncOperation.md) pour exécuter l’opération.</span><span class="sxs-lookup"><span data-stu-id="04da2-484">After applying the event handlers, call the start method on the [MSWebViewAsyncOperation](./webview/MSWebViewAsyncOperation.md) object to execute the operation.</span></span>

### <span data-ttu-id="04da2-485">captureSelectedContentToDataPackageAsync</span><span class="sxs-lookup"><span data-stu-id="04da2-485">captureSelectedContentToDataPackageAsync</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="04da2-486">Cette méthode a été déconseillée et présente un problème connu.</span><span class="sxs-lookup"><span data-stu-id="04da2-486">This method has been deprecated and has a known issue.</span></span> <span data-ttu-id="04da2-487">Évitez d’utiliser cette méthode dans votre code de production.</span><span class="sxs-lookup"><span data-stu-id="04da2-487">Avoid using this method in your production code.</span></span> 

<span data-ttu-id="04da2-488">Obtient de manière asynchrone un [DataPackage](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) qui contient le contenu sélectionné dans le **WebView**.</span><span class="sxs-lookup"><span data-stu-id="04da2-488">Asynchronously gets a [DataPackage](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) that contains the selected content within the **webview**.</span></span>

```js
var msWebViewAsyncOperation = webview.captureSelectedContentToDataPackageAsync();
```

#### <span data-ttu-id="04da2-489">Parameters</span><span class="sxs-lookup"><span data-stu-id="04da2-489">Parameters</span></span>
<span data-ttu-id="04da2-490">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="04da2-490">This method has no parameters.</span></span>

#### <span data-ttu-id="04da2-491">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="04da2-491">Return value</span></span>
<span data-ttu-id="04da2-492">Type: **MSWebViewAsyncOperation**</span><span class="sxs-lookup"><span data-stu-id="04da2-492">Type: **MSWebViewAsyncOperation**</span></span>

<span data-ttu-id="04da2-493">Un objet **MSWebViewAsyncOperation** qui, lorsqu’il se termine, fournit un objet [DataPackage](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) contenant l’image.</span><span class="sxs-lookup"><span data-stu-id="04da2-493">An **MSWebViewAsyncOperation** object that, when it completes, provides a [DataPackage](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) object that contains the image.</span></span> <span data-ttu-id="04da2-494">Lorsque vous utilisez **captureSelectedContentToDataPackageAsync**, vous devez définir des gestionnaires de réussite et d’erreur après la définition de l’opération.</span><span class="sxs-lookup"><span data-stu-id="04da2-494">When using **captureSelectedContentToDataPackageAsync**, you need to define success and error handlers after defining the operation.</span></span> <span data-ttu-id="04da2-495">Après avoir appliqué les gestionnaires d’événements, appelez la méthode Start sur l’objet MSWebViewAsyncOperation pour exécuter l’opération.</span><span class="sxs-lookup"><span data-stu-id="04da2-495">After applying the event handlers, call the start method on the MSWebViewAsyncOperation object to execute the operation.</span></span>

```js
 var operation = webview.captureSelectedContentToDataPackageAsync();
    operation.oncomplete = function () {
        // operation.result is a package object that contains the selected data.
        var url = URL.createObjectURL(operation.result, { oneTimeOnly: true });
        // After converting the package to a URI, put it in an image element.
        document.getElementById('webviewPreview').src = url;
    };
    operation.start();  

```

### <span data-ttu-id="04da2-496">invokeScriptAsync</span><span class="sxs-lookup"><span data-stu-id="04da2-496">invokeScriptAsync</span></span>

<span data-ttu-id="04da2-497">En tant qu’action asynchrone, exécute la fonction de script spécifiée à partir du code HTML actuellement chargé, avec des arguments spécifiques.</span><span class="sxs-lookup"><span data-stu-id="04da2-497">As an asynchronous action, executes the specified script function from the currently loaded HTML, with specific arguments.</span></span>

```js
webview.invokeScriptAsync(functionName, ...args)
```

#### <span data-ttu-id="04da2-498">Parameters</span><span class="sxs-lookup"><span data-stu-id="04da2-498">Parameters</span></span>

**<span data-ttu-id="04da2-499">Admises</span><span class="sxs-lookup"><span data-stu-id="04da2-499">functionName</span></span>**
* <span data-ttu-id="04da2-500">Type: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="04da2-500">Type: **String**</span></span>
* <span data-ttu-id="04da2-501">Nom de la fonction à appeler.</span><span class="sxs-lookup"><span data-stu-id="04da2-501">The name of the function to invoke.</span></span> <span data-ttu-id="04da2-502">Il s’agit d’un nom de propriété dans l’objet fenêtre globale du document de niveau supérieur de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="04da2-502">This is a property name on the global window object of the WebView's top level document.</span></span> <span data-ttu-id="04da2-503">Il peut s’agir d’une fonction globale intégrée telle que Eval ou Open, ou d’une fonction définie par script sur l’objet Window global.</span><span class="sxs-lookup"><span data-stu-id="04da2-503">This can be a built-in global function like eval or open, or it can be a script defined function on the global window object.</span></span> <span data-ttu-id="04da2-504">Seules les fonctions figurant dans le document de niveau supérieur de l’affichage WebView sont parfois appelées.</span><span class="sxs-lookup"><span data-stu-id="04da2-504">Only functions in the top level document of the WebView may be invoked.</span></span>

**<span data-ttu-id="04da2-505">args</span><span class="sxs-lookup"><span data-stu-id="04da2-505">args</span></span>**
* <span data-ttu-id="04da2-506">Type: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="04da2-506">Type: **String**</span></span>
* <span data-ttu-id="04da2-507">Paramètres de chaîne facultatifs à passer à la fonction appelée.</span><span class="sxs-lookup"><span data-stu-id="04da2-507">Optional string parameters to pass to the invoked function.</span></span> <span data-ttu-id="04da2-508">À l’issue de nomfonction, tout paramètre supplémentaire à invokeScriptAsync est une chaîne transmise à la fonction appelée.</span><span class="sxs-lookup"><span data-stu-id="04da2-508">After functionName, any additional parameters to invokeScriptAsync are strings passed to the invoked function.</span></span>

#### <span data-ttu-id="04da2-509">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="04da2-509">Return value</span></span>
<span data-ttu-id="04da2-510">Type: **MSWebViewAsyncOperation**</span><span class="sxs-lookup"><span data-stu-id="04da2-510">Type: **MSWebViewAsyncOperation**</span></span>

<span data-ttu-id="04da2-511">Lorsque vous utilisez **invokeScriptAsync**, vous devez définir des gestionnaires de réussite et d’erreur après la définition de l’opération.</span><span class="sxs-lookup"><span data-stu-id="04da2-511">When using **invokeScriptAsync**, you need to define success and error handlers after defining the operation.</span></span> <span data-ttu-id="04da2-512">Après avoir appliqué les gestionnaires d’événements, appelez **MSWebViewAsyncOperation. Start** pour exécuter l’opération.</span><span class="sxs-lookup"><span data-stu-id="04da2-512">After applying the event handlers, call **MSWebViewAsyncOperation.start** to execute the operation.</span></span> <span data-ttu-id="04da2-513">Si l’événement complet de MSWebViewAsyncOperation se déclenche, la propriété Result de MSWebViewAsyncOperation est la valeur de retour de chaîne de l’appel de la fonction.</span><span class="sxs-lookup"><span data-stu-id="04da2-513">If the MSWebViewAsyncOperation's complete event fires then the MSWebViewAsyncOperation's result property is the string return value from invoking the function.</span></span> <span data-ttu-id="04da2-514">L’utilisation de la valeur de retour de la fonction invoked permet à la communication par le biais du WebView de se reconnecter à l’hôte WebView de manière synchrone.</span><span class="sxs-lookup"><span data-stu-id="04da2-514">Using the invoked function's return value allows for the WebView content to communication synchronously back to the WebView host.</span></span> <span data-ttu-id="04da2-515">Pour que le contenu WebView communique de manière asynchrone à l’hôte WebView, voir l’événement MSWebViewScriptNotify.</span><span class="sxs-lookup"><span data-stu-id="04da2-515">To instead have the WebView content communicate asynchronously back to the WebView host see the MSWebViewScriptNotify event.</span></span> <span data-ttu-id="04da2-516">Si la fonction appelée lève une exception non gérée, l’événement d’erreur de MSWebViewAsyncOperation se déclenche.</span><span class="sxs-lookup"><span data-stu-id="04da2-516">If the function invoked throws an unhandled exception then the MSWebViewAsyncOperation's error event will fire.</span></span> 

```js
const functionName = "eval";
const args = ["'Current URL: ' + document.location.href"];

const asyncOp = webview.invokeScriptAsync(functionName, ...args);

asyncOp.onerror = () => console.error("Error: " + asyncOp.error);
asyncOp.oncomplete = () => console.log("Result: " + asyncOp.result); // Logs 'Current URL: about:blank'
asyncOp.start();
```

### <span data-ttu-id="04da2-517">getDeferredPermissionRequests</span><span class="sxs-lookup"><span data-stu-id="04da2-517">getDeferredPermissionRequests</span></span>

<span data-ttu-id="04da2-518">Renvoie une liste de demandes d’autorisation différées émises par le contenu du contrôle **WebView** .</span><span class="sxs-lookup"><span data-stu-id="04da2-518">Returns a list of deferred permission requests issued by content in the **webview** control.</span></span>

```js
var sequence<PermissionRequest> = x-ms-webview.getDeferredPermissionRequests();
```

#### <span data-ttu-id="04da2-519">Parameters</span><span class="sxs-lookup"><span data-stu-id="04da2-519">Parameters</span></span>
<span data-ttu-id="04da2-520">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="04da2-520">This method has no parameters.</span></span>

#### <span data-ttu-id="04da2-521">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="04da2-521">Return value</span></span>
<span data-ttu-id="04da2-522">Type: [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)</span><span class="sxs-lookup"><span data-stu-id="04da2-522">Type: [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)</span></span>

<span data-ttu-id="04da2-523">Demande d’autorisation différée spécifiée.</span><span class="sxs-lookup"><span data-stu-id="04da2-523">The specified deferred permission request.</span></span>

#### <span data-ttu-id="04da2-524">Fonctionnalités et exigences supplémentaires</span><span class="sxs-lookup"><span data-stu-id="04da2-524">Additional features and requirements</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="04da2-525">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04da2-525">Minimum supported client</span></span>** |<span data-ttu-id="04da2-526">Windows 10 [applications du Windows Store uniquement]</span><span class="sxs-lookup"><span data-stu-id="04da2-526">Windows10 [Windows Store apps only]</span></span> |    
|**<span data-ttu-id="04da2-527">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04da2-527">Minimum supported server</span></span>** |<span data-ttu-id="04da2-528">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="04da2-528">None supported</span></span>|   
|**<span data-ttu-id="04da2-529">Téléphone minimum pris en charge</span><span class="sxs-lookup"><span data-stu-id="04da2-529">Minimum supported phone</span></span>**  |<span data-ttu-id="04da2-530">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="04da2-530">None supported</span></span> |    


### <span data-ttu-id="04da2-531">getDeferredPermissionRequestById</span><span class="sxs-lookup"><span data-stu-id="04da2-531">getDeferredPermissionRequestById</span></span>

<span data-ttu-id="04da2-532">Renvoie la demande d’autorisation différée spécifiée.</span><span class="sxs-lookup"><span data-stu-id="04da2-532">Returns the specified deferred permission request.</span></span> 

```js
var deferredPermissionRequest = x-ms-webview.getDeferredPermissionRequestById(id);
```

#### <span data-ttu-id="04da2-533">Parameters</span><span class="sxs-lookup"><span data-stu-id="04da2-533">Parameters</span></span>
*<span data-ttu-id="04da2-534">id</span><span class="sxs-lookup"><span data-stu-id="04da2-534">id</span></span>*
* <span data-ttu-id="04da2-535">Type: **longue non signée**</span><span class="sxs-lookup"><span data-stu-id="04da2-535">Type: **unsigned long**</span></span>
* <span data-ttu-id="04da2-536">ID de la demande d’autorisation différée que vous souhaitez obtenir.</span><span class="sxs-lookup"><span data-stu-id="04da2-536">The ID of the deferred permission request you wish to get.</span></span>

#### <span data-ttu-id="04da2-537">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="04da2-537">Return value</span></span>
<span data-ttu-id="04da2-538">Type: [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)</span><span class="sxs-lookup"><span data-stu-id="04da2-538">Type: [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)</span></span>

<span data-ttu-id="04da2-539">Demande d’autorisation différée spécifiée.</span><span class="sxs-lookup"><span data-stu-id="04da2-539">The specified deferred permission request.</span></span>

#### <span data-ttu-id="04da2-540">Fonctionnalités et exigences supplémentaires</span><span class="sxs-lookup"><span data-stu-id="04da2-540">Additional features and requirements</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="04da2-541">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04da2-541">Minimum supported client</span></span>** |<span data-ttu-id="04da2-542">Windows 10 [applications du Windows Store uniquement]</span><span class="sxs-lookup"><span data-stu-id="04da2-542">Windows10 [Windows Store apps only]</span></span> |    
|**<span data-ttu-id="04da2-543">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04da2-543">Minimum supported server</span></span>** |<span data-ttu-id="04da2-544">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="04da2-544">None supported</span></span>|   
|**<span data-ttu-id="04da2-545">Téléphone minimum pris en charge</span><span class="sxs-lookup"><span data-stu-id="04da2-545">Minimum supported phone</span></span>**  |<span data-ttu-id="04da2-546">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="04da2-546">None supported</span></span> | 

### <span data-ttu-id="04da2-547">goBack</span><span class="sxs-lookup"><span data-stu-id="04da2-547">goBack</span></span>

<span data-ttu-id="04da2-548">Permet d’accéder à la page précédente de l’historique de navigation via le **WebView** .</span><span class="sxs-lookup"><span data-stu-id="04da2-548">Navigates the **webview** to the previous page in the navigation history.</span></span> 

```js
webview.goBack();
```

#### <span data-ttu-id="04da2-549">Parameters</span><span class="sxs-lookup"><span data-stu-id="04da2-549">Parameters</span></span>
<span data-ttu-id="04da2-550">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="04da2-550">This method has no parameters.</span></span>

#### <span data-ttu-id="04da2-551">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="04da2-551">Return value</span></span>
<span data-ttu-id="04da2-552">Cette méthode ne renvoie pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="04da2-552">This method does not return a value.</span></span>

### <span data-ttu-id="04da2-553">goForward</span><span class="sxs-lookup"><span data-stu-id="04da2-553">goForward</span></span>

<span data-ttu-id="04da2-554">Navigue vers la page suivante de l’historique de navigation du **WebView** .</span><span class="sxs-lookup"><span data-stu-id="04da2-554">Navigates the **webview** to the next page in the navigation history.</span></span> 

```js
webview.goForward();
```

#### <span data-ttu-id="04da2-555">Parameters</span><span class="sxs-lookup"><span data-stu-id="04da2-555">Parameters</span></span>
<span data-ttu-id="04da2-556">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="04da2-556">This method has no parameters.</span></span>

#### <span data-ttu-id="04da2-557">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="04da2-557">Return value</span></span>
<span data-ttu-id="04da2-558">Cette méthode ne renvoie pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="04da2-558">This method does not return a value.</span></span>

### <span data-ttu-id="04da2-559">naviguer</span><span class="sxs-lookup"><span data-stu-id="04da2-559">navigate</span></span>

<span data-ttu-id="04da2-560">Charge le contenu HTML à l’URI (Uniform Resource Identifier) spécifié.</span><span class="sxs-lookup"><span data-stu-id="04da2-560">Loads the HTML content at the specified Uniform Resource Identifier (URI).</span></span> 

```js
webview.navigate(uri);
```

#### <span data-ttu-id="04da2-561">Parameters</span><span class="sxs-lookup"><span data-stu-id="04da2-561">Parameters</span></span>

**<span data-ttu-id="04da2-562">uri</span><span class="sxs-lookup"><span data-stu-id="04da2-562">uri</span></span>**
* <span data-ttu-id="04da2-563">Type: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="04da2-563">Type: **String**</span></span>
* <span data-ttu-id="04da2-564">URI à charger.</span><span class="sxs-lookup"><span data-stu-id="04da2-564">The URI to load.</span></span>

#### <span data-ttu-id="04da2-565">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="04da2-565">Return value</span></span>
<span data-ttu-id="04da2-566">Cette méthode ne renvoie pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="04da2-566">This  method does not return a value.</span></span>

### <span data-ttu-id="04da2-567">navigateFocus</span><span class="sxs-lookup"><span data-stu-id="04da2-567">navigateFocus</span></span>

<span data-ttu-id="04da2-568">Déplace le focus sur le **WebView**.</span><span class="sxs-lookup"><span data-stu-id="04da2-568">Navigates focus onto the **webview**.</span></span> <span data-ttu-id="04da2-569">Déclenche l’événement navigatingfocus window’s du document de niveau supérieur de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="04da2-569">Fires the webview's top level document's window's navigatingfocus event.</span></span> <span data-ttu-id="04da2-570">Les arguments FocusNavigationEvent utilisés dans l’événement navigatingfocus correspondent aux paramètres fournis à navigateFocus, sauf que les paramètres d’origine sont convertis à partir de l’espace de coordonnées du document hôte vers l’espace de coordonnées du document de niveau supérieur de la WebView.</span><span class="sxs-lookup"><span data-stu-id="04da2-570">The FocusNavigationEvent args used in the navigatingfocus event match the parameters provided to navigateFocus except the origin parameters are translated from the host document's coordinate space to the coordinate space of the webview's top level document.</span></span> <span data-ttu-id="04da2-571">Voir l’événement WebView departingFocus et la méthode Window. departFocus correspondante pour transférer le focus du WebView vers l’hôte.</span><span class="sxs-lookup"><span data-stu-id="04da2-571">See the webview departingFocus event and corresponding window.departFocus method for transferring focus from the webview to the host.</span></span> <span data-ttu-id="04da2-572">Pour obtenir un exemple d’implémentation de la navigation au focus par le biais d’un clavier ou d’un boîtier de empilement qui utilise cette méthode, voir la [bibliothèque de navigation par TVJS](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) .</span><span class="sxs-lookup"><span data-stu-id="04da2-572">See the [TVJS's Direction Navigation library](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) for an example of an implementation of focus navigation via keyboard or gamepad that uses this method.</span></span>

```js
const activeElementBounds = document.activeElement.getBoundingClientRect();
const origin = { 
    originLeft: activeElementBounds.left,
    originTop: activeElementBounds.top,
    originWidth: activeElementBounds.width,
    originHeight: activeElementBounds.height
};
webview.navigateFocus(navigationReason, origin);
```

#### <span data-ttu-id="04da2-573">Parameters</span><span class="sxs-lookup"><span data-stu-id="04da2-573">Parameters</span></span>
*<span data-ttu-id="04da2-574">navigationReason</span><span class="sxs-lookup"><span data-stu-id="04da2-574">navigationReason</span></span>*
* <span data-ttu-id="04da2-575">Type: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="04da2-575">Type: **String**</span></span>
* <span data-ttu-id="04da2-576">Raison de la navigation.</span><span class="sxs-lookup"><span data-stu-id="04da2-576">The reason for the navigation.</span></span> <span data-ttu-id="04da2-577">La valeur doit être «gauche», «haut», «droite» ou «bas».</span><span class="sxs-lookup"><span data-stu-id="04da2-577">The value should be either "left", "up", "right", or "down".</span></span> <span data-ttu-id="04da2-578">C’est la direction dans laquelle le focus quitte l’élément actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="04da2-578">It is the direction in which focus is moving away from the currently focused element.</span></span>

*<span data-ttu-id="04da2-579">prêts</span><span class="sxs-lookup"><span data-stu-id="04da2-579">origin</span></span>*
* <span data-ttu-id="04da2-580">Type: **objet**</span><span class="sxs-lookup"><span data-stu-id="04da2-580">Type: **Object**</span></span>
* <span data-ttu-id="04da2-581">Origine de la navigation.</span><span class="sxs-lookup"><span data-stu-id="04da2-581">The origin of the navigation.</span></span> <span data-ttu-id="04da2-582">Il s’agit d’un objet JavaScript avec les propriétés «originLeft», «originTop», «originWidth» et «originHeight».</span><span class="sxs-lookup"><span data-stu-id="04da2-582">This is a JavaScript object with properties "originLeft", "originTop", "originWidth", and "originHeight".</span></span> <span data-ttu-id="04da2-583">Ces valeurs doivent décrire la position et la taille de l’élément actuellement sélectionné hors du mouvement.</span><span class="sxs-lookup"><span data-stu-id="04da2-583">These values should describe the position and size of the currently focused element away from which focus is moving.</span></span>

#### <span data-ttu-id="04da2-584">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="04da2-584">Return value</span></span>
<span data-ttu-id="04da2-585">Cette méthode ne renvoie pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="04da2-585">This method does not return a value.</span></span>

### <span data-ttu-id="04da2-586">navigateToLocalStreamUri</span><span class="sxs-lookup"><span data-stu-id="04da2-586">navigateToLocalStreamUri</span></span>

<span data-ttu-id="04da2-587">Charge le contenu Web local à l’URI spécifié à l’aide d’un [**UriToStreamResolver**](/uwp/api/windows.web.iuritostreamresolver.uritostreamasync).</span><span class="sxs-lookup"><span data-stu-id="04da2-587">Loads local web content at the specified URI using a [**UriToStreamResolver**](/uwp/api/windows.web.iuritostreamresolver.uritostreamasync).</span></span>

```js
webview.navigateToLocalStreamUri(source, streamResolver); 
```

#### <span data-ttu-id="04da2-588">Parameters</span><span class="sxs-lookup"><span data-stu-id="04da2-588">Parameters</span></span>

*<span data-ttu-id="04da2-589">origine</span><span class="sxs-lookup"><span data-stu-id="04da2-589">source</span></span>*
* <span data-ttu-id="04da2-590">Type: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="04da2-590">Type: **String**</span></span>
* <span data-ttu-id="04da2-591">URI MS-local-Stream qui identifie le contenu HTML local à charger.</span><span class="sxs-lookup"><span data-stu-id="04da2-591">An ms-local-stream URI identifying the local HTML content to load.</span></span> <span data-ttu-id="04da2-592">Créez cette chaîne à l’aide de [**buildLocalStreamUri**](/uwp/api/windows.web.ui.iwebviewcontrol.buildlocalstreamuri).</span><span class="sxs-lookup"><span data-stu-id="04da2-592">Create this string using [**buildLocalStreamUri**](/uwp/api/windows.web.ui.iwebviewcontrol.buildlocalstreamuri).</span></span>

*<span data-ttu-id="04da2-593">streamResolver</span><span class="sxs-lookup"><span data-stu-id="04da2-593">streamResolver</span></span>*
* <span data-ttu-id="04da2-594">Tapez: tout</span><span class="sxs-lookup"><span data-stu-id="04da2-594">Type: any</span></span>
* <span data-ttu-id="04da2-595">Un résolveur qui convertit l’URI en flux à charger.</span><span class="sxs-lookup"><span data-stu-id="04da2-595">A resolver that converts the URI into a stream to load.</span></span>

#### <span data-ttu-id="04da2-596">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="04da2-596">Return value</span></span>
<span data-ttu-id="04da2-597">Cette méthode ne renvoie pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="04da2-597">This method does not return a value.</span></span>

### <span data-ttu-id="04da2-598">navigateToString</span><span class="sxs-lookup"><span data-stu-id="04da2-598">navigateToString</span></span>

<span data-ttu-id="04da2-599">Charge le contenu HTML spécifié sous la forme d’un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="04da2-599">Loads the specified HTML content as a new document.</span></span> 

```js
webview.navigateToString(contents);
```

#### <span data-ttu-id="04da2-600">Parameters</span><span class="sxs-lookup"><span data-stu-id="04da2-600">Parameters</span></span>

*<span data-ttu-id="04da2-601">teneur</span><span class="sxs-lookup"><span data-stu-id="04da2-601">contents</span></span>*
* <span data-ttu-id="04da2-602">Type: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="04da2-602">Type: **String**</span></span>
* <span data-ttu-id="04da2-603">Contenu HTML à afficher.</span><span class="sxs-lookup"><span data-stu-id="04da2-603">The HTML content to display.</span></span>

#### <span data-ttu-id="04da2-604">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="04da2-604">Return value</span></span>
<span data-ttu-id="04da2-605">Cette méthode ne renvoie pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="04da2-605">This method does not return a value.</span></span>

### <span data-ttu-id="04da2-606">navigateWithHttpRequestMessage</span><span class="sxs-lookup"><span data-stu-id="04da2-606">navigateWithHttpRequestMessage</span></span>

<span data-ttu-id="04da2-607">Accède au WebView à un URI (Uniform Resource Identifier) avec un en-tête de requête POST et des en-têtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="04da2-607">Navigates the webview to a Uniform Resource Identifier (URI) with a POST request and HTTP headers.</span></span> 

```js
webview.navigateWithHttpRequestMessage(requestMessage);
```

#### <span data-ttu-id="04da2-608">Parameters</span><span class="sxs-lookup"><span data-stu-id="04da2-608">Parameters</span></span>

*<span data-ttu-id="04da2-609">Collection RequestMessage</span><span class="sxs-lookup"><span data-stu-id="04da2-609">requestMessage</span></span>*
* <span data-ttu-id="04da2-610">Type: **HttpRequestMessage**</span><span class="sxs-lookup"><span data-stu-id="04da2-610">Type: **HttpRequestMessage**</span></span>
* <span data-ttu-id="04da2-611">Détails de la requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="04da2-611">The details of the HTTP request.</span></span> 

#### <span data-ttu-id="04da2-612">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="04da2-612">Return value</span></span>
<span data-ttu-id="04da2-613">Cette méthode ne renvoie pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="04da2-613">This method does not return a value.</span></span>

#### <span data-ttu-id="04da2-614">Remarques</span><span class="sxs-lookup"><span data-stu-id="04da2-614">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="04da2-615">Si vous ajoutez des en-têtes supplémentaires à cette requête, tels que les informations d’identification d’authentification, n’oubliez pas que ces en-têtes seront également inclus dans toutes les demandes enfant ultérieures.</span><span class="sxs-lookup"><span data-stu-id="04da2-615">If you add additional headers to this request, such as authentication credentials, remember that those headers will also be included with any subsequent child requests.</span></span> <span data-ttu-id="04da2-616">Faites preuve de prudence pour éviter toute divulgation accidentelle de renseignements confidentiels ou personnels.</span><span class="sxs-lookup"><span data-stu-id="04da2-616">Use caution to prevent accidental disclosure of confidential or personal information.</span></span> 


### <span data-ttu-id="04da2-617">mise</span><span class="sxs-lookup"><span data-stu-id="04da2-617">refresh</span></span> 

<span data-ttu-id="04da2-618">Recharge le contenu actuel dans **WebView**.</span><span class="sxs-lookup"><span data-stu-id="04da2-618">Reloads the current content in the **webview**.</span></span> 

```js
webview.refresh();
```

#### <span data-ttu-id="04da2-619">Parameters</span><span class="sxs-lookup"><span data-stu-id="04da2-619">Parameters</span></span>
<span data-ttu-id="04da2-620">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="04da2-620">This method has no parameters.</span></span>

#### <span data-ttu-id="04da2-621">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="04da2-621">Return value</span></span>
<span data-ttu-id="04da2-622">Cette méthode ne renvoie pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="04da2-622">This method does not return a value.</span></span>


### <span data-ttu-id="04da2-623">stop</span><span class="sxs-lookup"><span data-stu-id="04da2-623">stop</span></span>

<span data-ttu-id="04da2-624">Arrête la navigation ou le téléchargement de l' **affichage WebView** actuel.</span><span class="sxs-lookup"><span data-stu-id="04da2-624">Halts the current **webview** navigation or download.</span></span> 

```js
webview.stop();
```

#### <span data-ttu-id="04da2-625">Parameters</span><span class="sxs-lookup"><span data-stu-id="04da2-625">Parameters</span></span>
<span data-ttu-id="04da2-626">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="04da2-626">This method has no parameters.</span></span>

#### <span data-ttu-id="04da2-627">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="04da2-627">Return value</span></span>
<span data-ttu-id="04da2-628">Cette méthode ne renvoie pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="04da2-628">This method does not return a value.</span></span>


## <span data-ttu-id="04da2-629">Propriétés</span><span class="sxs-lookup"><span data-stu-id="04da2-629">Properties</span></span>

### <span data-ttu-id="04da2-630">canGoBack</span><span class="sxs-lookup"><span data-stu-id="04da2-630">canGoBack</span></span>

<span data-ttu-id="04da2-631">Obtient une valeur qui indique si le **WebView** peut naviguer vers l’arrière.</span><span class="sxs-lookup"><span data-stu-id="04da2-631">Gets a value that indicates whether the **webview** can navigate backward.</span></span>

<span data-ttu-id="04da2-632">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="04da2-632">This property is read-only.</span></span>

```js
var canGoBack = webview.canGoBack;
```

#### <span data-ttu-id="04da2-633">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="04da2-633">Property value</span></span>
<span data-ttu-id="04da2-634">Type: **booléen**</span><span class="sxs-lookup"><span data-stu-id="04da2-634">Type: **Boolean**</span></span>

<span data-ttu-id="04da2-635">**True** si **WebView** peut naviguer vers l’arrière; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="04da2-635">**True** if the **webview** can navigate backward; otherwise, **false**.</span></span>

### <span data-ttu-id="04da2-636">canGoForward</span><span class="sxs-lookup"><span data-stu-id="04da2-636">canGoForward</span></span>

<span data-ttu-id="04da2-637">Obtient une valeur qui indique s’il est possible d’accéder à **WebView** en aval.</span><span class="sxs-lookup"><span data-stu-id="04da2-637">Gets a value that indicates whether the **webview** can navigate forward.</span></span>

<span data-ttu-id="04da2-638">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="04da2-638">This property is read-only.</span></span>

```js
var canGoForward = webview.canGoForward;
```

#### <span data-ttu-id="04da2-639">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="04da2-639">Property value</span></span>
<span data-ttu-id="04da2-640">Type: **booléen**</span><span class="sxs-lookup"><span data-stu-id="04da2-640">Type: **Boolean**</span></span>

<span data-ttu-id="04da2-641">**True** si **WebView** peut naviguer vers l’avant; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="04da2-641">**True** if the **webview** can navigate forward; otherwise, **false**.</span></span>

### <span data-ttu-id="04da2-642">containsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="04da2-642">containsFullScreenElement</span></span>

<span data-ttu-id="04da2-643">Obtient une valeur qui indique si le **WebView** contient un élément qui prend en charge le plein écran.</span><span class="sxs-lookup"><span data-stu-id="04da2-643">Gets a value that indicates whether the **webview** contains an element that supports full screen.</span></span> <span data-ttu-id="04da2-644">Pour plus d’informations, voir l’événement MSWebViewContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="04da2-644">See the MSWebViewContainsFullScreenElementChanged event for more info.</span></span>

<span data-ttu-id="04da2-645">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="04da2-645">This property is read-only.</span></span>

```js
var containsFullScreenElement = webview.containsFullScreenElement;
```

#### <span data-ttu-id="04da2-646">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="04da2-646">Property value</span></span>
<span data-ttu-id="04da2-647">Type: **booléen**</span><span class="sxs-lookup"><span data-stu-id="04da2-647">Type: **Boolean**</span></span>

<span data-ttu-id="04da2-648">**True** si **WebView** contient un élément qui prend en charge le plein écran; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="04da2-648">**True** if the **webview** contains an element that supports full screen; otherwise, **false**.</span></span>


### <span data-ttu-id="04da2-649">documentTitle</span><span class="sxs-lookup"><span data-stu-id="04da2-649">documentTitle</span></span>

<span data-ttu-id="04da2-650">Obtient le titre de la page actuellement affichée dans le **WebView**.</span><span class="sxs-lookup"><span data-stu-id="04da2-650">Gets the title of the page currently displayed in the **webview**.</span></span> 

<span data-ttu-id="04da2-651">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="04da2-651">This property is read-only.</span></span>

```js
var documentTitle = webview.documentTitle;
```

#### <span data-ttu-id="04da2-652">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="04da2-652">Property value</span></span>
<span data-ttu-id="04da2-653">Type: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="04da2-653">Type: **String**</span></span>

<span data-ttu-id="04da2-654">Le titre de la page.</span><span class="sxs-lookup"><span data-stu-id="04da2-654">The page title.</span></span>

### <span data-ttu-id="04da2-655">hauteur</span><span class="sxs-lookup"><span data-stu-id="04da2-655">height</span></span>

<span data-ttu-id="04da2-656">Obtient ou définit la hauteur du **WebView**.</span><span class="sxs-lookup"><span data-stu-id="04da2-656">Gets or sets the height of the **webview**.</span></span> 

```js
var height = webview.height;
webview.height = height;

```

#### <span data-ttu-id="04da2-657">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="04da2-657">Property value</span></span>
<span data-ttu-id="04da2-658">Type: **nombre**</span><span class="sxs-lookup"><span data-stu-id="04da2-658">Type: **Number**</span></span>

<span data-ttu-id="04da2-659">Hauteur du **WebView**.</span><span class="sxs-lookup"><span data-stu-id="04da2-659">The height of the **webview**.</span></span> 


### <span data-ttu-id="04da2-660">processus</span><span class="sxs-lookup"><span data-stu-id="04da2-660">process</span></span>

<span data-ttu-id="04da2-661">Obtient le processus **WebView** .</span><span class="sxs-lookup"><span data-stu-id="04da2-661">Gets the **webview** process.</span></span>

<span data-ttu-id="04da2-662">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="04da2-662">This property is read-only.</span></span>

```js
var process = webview.process;
webview.process = process;
```

#### <span data-ttu-id="04da2-663">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="04da2-663">Property value</span></span>
<span data-ttu-id="04da2-664">Type: [MSWebViewProcess](./webview/MSWebViewProcess.md)</span><span class="sxs-lookup"><span data-stu-id="04da2-664">Type: [MSWebViewProcess](./webview/MSWebViewProcess.md)</span></span>


### <span data-ttu-id="04da2-665">settings</span><span class="sxs-lookup"><span data-stu-id="04da2-665">settings</span></span>

<span data-ttu-id="04da2-666">Obtient un objet [MSWebViewSettings](./webview/MSWebViewSettings.md) qui contient les propriétés permettant d’activer ou de désactiver les fonctionnalités **WebView** .</span><span class="sxs-lookup"><span data-stu-id="04da2-666">Gets a [MSWebViewSettings](./webview/MSWebViewSettings.md) object that contains properties to enable or disable **webview** features.</span></span>

<span data-ttu-id="04da2-667">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="04da2-667">This property is read-only.</span></span>

```js
var settings = webview.settings;
webview.settings = settings;
```

#### <span data-ttu-id="04da2-668">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="04da2-668">Property value</span></span>
<span data-ttu-id="04da2-669">Type: [MSWebViewSettings](./webview/MSWebViewSettings.md)</span><span class="sxs-lookup"><span data-stu-id="04da2-669">Type: [MSWebViewSettings](./webview/MSWebViewSettings.md)</span></span>

<span data-ttu-id="04da2-670">Objet [MSWebViewSettings](./webview/MSWebViewSettings.md) qui contient les propriétés permettant d’activer ou de désactiver les fonctionnalités d' **affichage WebView** .</span><span class="sxs-lookup"><span data-stu-id="04da2-670">A [MSWebViewSettings](./webview/MSWebViewSettings.md) object that contains properties to enable or disable **webview** features.</span></span>

### <span data-ttu-id="04da2-671">src</span><span class="sxs-lookup"><span data-stu-id="04da2-671">src</span></span>

<span data-ttu-id="04da2-672">Obtient ou définit la source URI (Uniform Resource Identifier) du contenu HTML à afficher dans le contrôle **WebView** .</span><span class="sxs-lookup"><span data-stu-id="04da2-672">Gets or sets the Uniform Resource Identifier (URI) source of the HTML content to display in the **webview** control.</span></span> 

```js
var src = webview.src;
webview.src = src;
```

#### <span data-ttu-id="04da2-673">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="04da2-673">Property value</span></span>
<span data-ttu-id="04da2-674">Type: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="04da2-674">Type: **String**</span></span>

<span data-ttu-id="04da2-675">Source URI du contenu HTML à afficher dans le contrôle **WebView** .</span><span class="sxs-lookup"><span data-stu-id="04da2-675">The URI source of the HTML content to display in the **webview** control.</span></span> 


### <span data-ttu-id="04da2-676">largeur</span><span class="sxs-lookup"><span data-stu-id="04da2-676">width</span></span>

<span data-ttu-id="04da2-677">Obtient ou définit la largeur du **WebView**.</span><span class="sxs-lookup"><span data-stu-id="04da2-677">Gets or sets the width of the **webview**.</span></span>

```js
var width = webview.width;
webview.width = width;
```

#### <span data-ttu-id="04da2-678">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="04da2-678">Property value</span></span>
<span data-ttu-id="04da2-679">Type: **nombre**</span><span class="sxs-lookup"><span data-stu-id="04da2-679">Type: **Number**</span></span>

<span data-ttu-id="04da2-680">La largeur du **WebView**.</span><span class="sxs-lookup"><span data-stu-id="04da2-680">The width of the **webview**.</span></span>
