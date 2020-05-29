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
# WebView (EdgeHTML) pour les applications Windows 10

Le contrôle WebView (EdgeHTML) vous permet d’héberger le contenu Web dans votre application Windows 10. 

Vous pouvez l’utiliser en tant qu’élément XAML (pour les [applications de plateforme Windows universelle (UWP)](/uwp/api/Windows.UI.Xaml.Controls.WebView) et les [applications de bureau Windows Forms](/windows/communitytoolkit/controls/wpf-winforms/webview), ou dans un élément HTML (x-ms-WebView)/DOM pour les applications Windows 10, comme décrit ici.

| | |
|-|-|
| [**Événements**](#events) | [departingFocus](#departingfocus), [MSWebViewContainsFullScreenElementChanged](#mswebviewcontainsfullscreenelementchanged), [MSWebViewContentLoading](#mswebviewcontentloading), [MSWebViewDOMContentLoaded](#mswebviewdomcontentloaded), [MSWebViewFrameContentLoading](#mswebviewframecontentloading), [MSWebViewFrameDOMContentLoaded](#mswebviewframedomcontentloaded), [MSWebViewFrameNavigationCompleted](#mswebviewframenavigationcompleted), [MSWebViewFrameNavigationStarting](#mswebviewframenavigationstarting), [MSWebViewLongRunningScriptDetected](#mswebviewlongrunningscriptdetected), [MSWebViewNavigationCompleted](#mswebviewnavigationcompleted), [MSWebViewNavigationStarting](#mswebviewnavigationstarting), [MSWebViewNewWindowRequested](#mswebviewnewwindowrequested), [MSWebViewPermissionRequested, MSWebViewProcessExited](#mswebviewpermissionrequested) [, MSWebViewWebResourceRequested](#mswebviewprocessexited), MSWebViewScriptNotify [, MSWebViewUnsafeContentWarningDisplaying](#mswebviewscriptnotify), [MSWebViewUnsupportedUriSchemeIdentified](#mswebviewunsupportedurischemeidentified) [MSWebViewUnsupportedUriSchemeIdentified](#mswebviewunsafecontentwarningdisplaying), [MSWebViewUnviewableContentIdentified](#mswebviewunviewablecontentidentified) [MSWebViewUnviewableContentIdentified](#mswebviewwebresourcerequested)
| [**Méthodes**](#methods) | [addWebAllowedObject](#addweballowedobject), [buildlocalStreamUri](#buildlocalstreamuri), [capturePreviewToBlobAsync](#capturepreviewtoblobasync), [captureSelectedContentToDataPackageAsync](#captureselectedcontenttodatapackageasync), [invokeScriptAsync](#invokescriptasync), [getDeferredPermissionRequests](#getdeferredpermissionrequests), [getDeferredPermissionRequestById](#getdeferredpermissionrequestbyid), [GoBack](#goback), [goForward](#goforward), [navigation](#navigate), [navigateFocus](#navigatefocus), [navigateTolocalStreamUri](#navigatetolocalstreamuri), [navigateToString](#navigatetostring), [navigateWithHttpRequestMessage](#navigatewithhttprequestmessage), [Refresh](#refresh), [Stop](#stop) |
| [**Propriétés**](#properties) | [canGoBack](#cangoback), [canGoForward](#cangoforward), [containsFullScreenElement](#containsfullscreenelement), [DocumentTitle](#documenttitle), [Height](#height), [Process](#process), [Settings](#settings), [src](#src), [Width](#width) |

## Syntaxe

```js
// Feature detect for webview support
if (MSHTMLWebViewElement) {
    let wv = document.createElement('x-ms-webview'); // Use CSS to set width, height and other styles
    wv.navigate("https://www.example.com");
    document.body.appendChild(wv);
}
```

## Remarques

### WebView et IFRAME

À l’instar d’un élément [IFRAME](https://developer.mozilla.org/docs/Web/HTML/Element/iframe) HTML standard, vous pouvez utiliser WebView pour charger les pages distantes sur http et les pages locales (*MS-AppX-Web///*) à partir de votre package d’application. Toutefois, le WebView peut également:

 - Charger des pages et des ressources à partir de vos dossiers [ApplicationData](/uwp/api/Windows.Storage.ApplicationData) (local, Roaming, Temp) (*MS-AppData:/*/) et [des flux en mémoire](/microsoft-edge/hosting/webview#buildlocalstreamuri) (*MS-local-Stream:///*)

 - Fournissez des contrôles de type navigateur: pour la navigation [vers l’arrière](#goback) et [vers](#goforward) l’arrière dans l’historique de navigation, et pour l' [arrêt](#stop) ou l' [actualisation](#refresh) de la page active. 

 - [Capture de captures d’écran d’un contenu Web](#capturepreviewtoblobasync) simplifiant l’implémentation du contrat de [partage](/windows/uwp/app-to-app/share-data) d’application Windows 10.

 - Autorisez l’exécution du code JavaScript dans un WebView pour déclencher des événements personnalisés ([MSWebViewScriptNotify](#mswebviewscriptnotify)) dans votre application et permettre à votre application d’exécuter JavaScript dans le WebView ([invokeScriptAsync](#invokescriptasync)).

 - Vous fournir des événements de contenu d’affichage de manière précise:
    
    Événement DOM WebView | Description
    --------- | ------
    [MSWebViewNavigationStarting](#mswebviewnavigationstarting) | Indique que l’affichage du WebView commence
    [MSWebViewContentLoading](#mswebviewcontentloading) | Le contenu HTML est téléchargé et est en cours de chargement dans le contrôle
    [MSWebViewDOMContentLoaded](#mswebviewdomcontentloaded) | Indique que les éléments DOM principaux ont fini de se charger
    [MSWebViewNavigationCompleted](#mswebviewnavigationcompleted) | Indique que la navigation est terminée et que tous les éléments multimédias sont affichés
    [MSWebViewUnviewableContentIdentified](#mswebviewunviewablecontentidentified) | Le contenu du WebView ne s’est pas affiché en HTML
    [UnsafeContentWarningDisplaying](#mswebviewunsafecontentwarningdisplaying) | Le WebView affiche une page d’avertissement pour le contenu signalé comme non sécurisé par le *filtre Windows SmartScreen*.

    ... incluant des [événements](#events) correspondants pour le contenu iframe chargé dans un WebView (par exemple, [MSWebView**Frame**NavigationStarting](#mswebviewframenavigationstarting) , etc.)

### Impression

Quand une application Windows utilisant JavaScript est imprimée, les `<x-ms-webview>` balises sont transformées en `<iframe>` balises avant l’impression. Outre la différence normale entre l’affichage à l’écran et le rendu pour l’impression, les styles CSS appliqués aux `<iframe>` éléments sont ensuite applicables à la `<iframe>` transformation de `<x-ms-webview>` .

### Travailleurs de service

À partir de la [mise à jour 2018 de Windows 10 d’octobre](/windows/uwp/whats-new/windows-10-build-17763) (EdgeHTML 18), [les travailleurs de services sont pris en charge dans le contrôle WebView](/microsoft-edge/dev-guide#service-workers) (en plus du navigateur Microsoft Edge et des applications Windows 10 avec JavaScript).

les architectures d’applications x64 requièrent des packages de type neutre (n’importe quel processeur) ou x64, car les travailleurs de services ne sont pas pris en charge dans les processus WoW64. (Pour économiser de l’espace disque, la version de WoW des dll requises n’est pas fournie en natif dans Windows.)

### Modèle de thread et fiabilité

La création d’un WebView via `document.createElement("x-ms-webview")` ou par le biais `<x-ms-webview>` du balisage crée un WebView sur un nouveau thread unique dans le processus de l’application. L’exécution sur un nouveau thread unique implique que du temps d’exécution du script d’un WebView ne peut pas bloquer l’application ou d’autres vues. La création d’un WebView via le `new MSWebView()` constructeur crée un WebView dans un processus distinct d’affichage. L’exécution d’un processus unique implique qu’en plus de la protection du script de grande durée d’exécution, l’application est également protégée du contenu Web qui bloque le processus WebView. La création d’un WebView par le biais de la [`MSWebViewProcess.createWebViewAsync`](./webview/MSWebViewProcess.md#createwebviewasync) méthode permet également de créer un WebView dans un processus distinct tout en permettant à l’appelant de contrôler davantage les paramètres de processus et de regrouper les vues WebView dans les processus WebView. Si vous souhaitez en savoir plus, consultez `MSWebViewProcess`. 

### Accès à l’API WinRT

Une application UWP peut permettre aux documents HTML dans les WebView d’avoir accès aux API WinRT. C’est par le biais de l’attribut WindowsRuntimeAccess des éléments enfants Rule de l’élément ApplicationContentUriRules du AppxManifest. XML de l’application UWP. Définissez WindowsRuntimeAccess sur «All» et les documents HTML avec URI correspondants seront autorisés à utiliser WinRT. Il en s’agit de la même façon que le fait de fournir un accès WinRT au contenu HTML dans les applications UWP JavaScript pour voir comment [appeler des API WinRT de votre PWA](/microsoft-edge/progressive-web-apps-edgehtml/windows-features#call-winrt-apis-from-your-pwa) pour plus d’informations.

Les API WinRT associées à l’interface utilisateur risquent de ne pas fonctionner en cas d’appel à partir d’un WebView exécuté sur son propre thread, mais cela risque de fonctionner en cas d’appel à partir d’un WebView exécuté dans un processus WebView distinct. Lorsque vous utilisez un WebView sur son propre thread unique, il ne s’agit pas du thread d’affichage de l’application. Certaines API WinRT associées à l’interface utilisateur nécessitent d’être appelées à partir du thread d’affichage de l’application. Les webaffichages créés dans un processus WebView distinct s’exécutent sur un thread d’affichage et ne doivent donc pas être confrontés aux mêmes restrictions que celles exécutées dans WebView sur leur propre thread unique. Si vous rencontrez des problèmes avec les API WinRT associées à l’interface utilisateur dans un WebView, assurez-vous que vous utilisez un WebView dans son propre processus WebView, comme décrit ci-dessus.

### Limites de stockage AppCache

Les applications qui utilisent la prise en charge JavaScript de l’API de cache d’application (ou AppCache), telles qu’elles sont définies dans la [spécification HTML5](https://go.microsoft.com/fwlink/p/?LinkId=228542), doivent respecter les limitations de stockage disponibles. Ceci est particulièrement vrai dans les appareils dont l’espace mémoire est limité. Les limites pratiques en matière de taille des AppCache sont toujours une fonction d’espace de stockage sur disque disponible. Les recommandations générales sont décrites ci-dessous.

| Taille du volume         |AppCache par domaine | AppCache par utilisateur   | 
|---------------|---------------|-------------------------|
Jusqu’à 4 Go | ATTEINDRE | 50Mo |
4 Go à 16 Go | 50Mo | MINIMUM | 
16 Go à 32 Go | 50Mo | 1 Go |

Toutes les applications Windows 10 sont conçues pour utiliser le même modèle de quota AppCache, de sorte que la limitation de stockage disque disponible s’applique aux applications de bureau et de téléphone. Le seuil est également limité après que les pages chargées dans **WebView** aient consommé 1 Go d’espace *AppCache* ; demandes d’espace de stockage *AppCache* supplémentaire au-delà de cette limite sera refusée. 

Pour plus d’informations, consultez l' [exemple de contrôle WebView html](https://go.microsoft.com/fwlink/p/?linkid=309825) et l’JSBrowser de la documentation sur [le contrôle WebView](https://github.com/MicrosoftEdge/JSBrowser#harnessing-the-webview-control) .

## Événements

### departingFocus

Indique le focus sur le **WebView** dans l’application. Se déclenche lorsque le document de niveau supérieur d’un WebView est appelé. departFocus. Les arguments FocusNavigationEvent de l’événement departingFocus correspondent aux paramètres fournis à departFocus, sauf que les paramètres d’origine sont convertis à partir de l’espace de coordonnées document’s du WebView dans l’espace de coordonnées du document hôte de WebView. Voir la méthode WebView. navigateFocus et l’événement navigatingFocus de fenêtre correspondant pour transférer le focus d’un hôte vers un WebView. Pour obtenir un exemple d’implémentation de la navigation au focus par le biais d’un clavier ou d’un boîtier de empilements qui gère cet événement, voir la [bibliothèque de navigation](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) dans l’TVJS.

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("departingFocus", handler);
webview.removeEventListener("departingFocus", handler);
```

#### Informations sur l’événement

|            |      |
|------------|------|
|**Interface** | [FocusNavigationEvent](./webview/FocusNavigationEvent.md) |
|**Synchrone** |Oui |    
|**BD**     |Oui |   
|**Annulable**  |Non |            

### MSWebViewContainsFullScreenElementChanged

Se produit lorsque l’état change, qu’il s’agisse d’un élément de l' **affichage** plein écran. Utilisez la propriété containsFullScreenElement sur la valeur actuelle. Un élément à l’écran complet fait référence à la notion d' [API DOM fullscreen](https://developer.mozilla.org/docs/Web/API/Fullscreen_API) d’un élément à l’écran complet via les fonctions DOM Element. requestFullScreen et document. exitFullScreen.

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

#### Informations sur l’événement

|            |      |
|------------|------|
|**Interface** | **Événement** |
|**Synchrone** |Oui |    
|**BD**     |Non |   
|**Annulable**  |Non |  

### MSWebViewContentLoading

Indique que le contenu HTML est téléchargé et est en cours de chargement dans le contrôle.

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewContentLoading", handler);
webview.removeEventListener("MSWebViewContentLoading", handler);
```

#### Informations sur l’événement

|            |      |
|------------|------|
|**Interface** | [NavigationEvent](./webview/NavigationEvent.md) |
|**Synchrone** |Oui  |    
|**BD**     |Non |   
|**Annulable**  |Non |    

### MSWebViewDOMContentLoaded

Indique que les éléments DOM principaux ont fini de se charger.


```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewDOMContentLoaded", handler);
webview.removeEventListener("MSWebViewDOMContentLoaded", handler);
```

#### Informations sur l’événement

|            |      |
|------------|------|
|**Interface** | [NavigationEvent](./webview/NavigationEvent.md) |
|**Synchrone** |Oui  |    
|**BD**     |Non |   
|**Annulable**  |Non |                 

### MSWebViewFrameContentLoading

Indique que le contenu HTML est téléchargé et est en cours de chargement dans le `<iframe>` contrôle.

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameContentLoading", handler);
webview.removeEventListener("MSWebViewFrameContentLoading", handler);
```

#### Informations sur l’événement

|            |      |
|------------|------|
|**Interface** | [NavigationEvent](./webview/NavigationEvent.md) |
|**Synchrone** |Oui  |    
|**BD**     |Non |   
|**Annulable**  |Non |                 

### MSWebViewFrameDOMContentLoaded

Indique que les éléments DOM principaux ont fini de se charger dans le `<iframe>` .

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameDOMContentLoaded", handler);
webview.removeEventListener("MSWebViewFrameDOMContentLoaded", handler);
```

#### Informations sur l’événement

|            |      |
|------------|------|
|**Interface** | [NavigationEvent](./webview/NavigationEvent.md) |
|**Synchrone** |Oui  |    
|**BD**     |Non |   
|**Annulable**  |Non |    


### MSWebViewFrameNavigationCompleted

Indique que la navigation est terminée et que tous les éléments multimédias sont restitués dans la `<iframe>` .

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameNavigationCompleted", handler);
webview.removeEventListener("MSWebViewFrameNavigationCompleted", handler);
```

#### Informations sur l’événement

|            |      |
|------------|------|
|**Interface** | [NavigationCompletedEvent](./webview/NavigationCompletedEvent.md) |
|**Synchrone** |Oui |    
|**BD**     |Non |   
|**Annulable**  |Non |       

### MSWebViewFrameNavigationStarting

Indique `<iframe>` qu’une partie d’un **WebView** commence à se déplacer. Ce problème est déclenché avant d’obtenir des ressources du réseau pour la navigation. La navigation n’a pas commencé tant que tous les gestionnaires d’événements MSWebViewFrameNavigationStarting n’ont pas terminé. Cet événement peut être annulé par le biais de l’appel `eventArgs.preventDefault()` . S’il est annulé, le WebView n’effectue pas de navigation.


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

#### Informations sur l’événement

|            |      |
|------------|------|
|**Interface** | [NavigationEvent](./webview/NavigationEvent.md) |
|**Synchrone** |Oui  |    
|**BD**     |Non |   
|**Annulable**  |Oui |                 
          
### MSWebViewLongRunningScriptDetected

Se produit régulièrement pendant l’exécution d’un script ininterrompu dans le **WebView**, ce qui vous permet d’arrêter le script.

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

#### Informations sur l’événement

|            |      |
|------------|------|
|**Interface** | [LongRunningScriptDetectedEvent](./webview/LongRunningScriptDetectedEvent.md) |
|**Synchrone** |Oui |    
|**BD**     |Non |   
|**Annulable**  |Non |            

### MSWebViewNavigationCompleted

Indique que la navigation est terminée et que tous les éléments multimédias sont affichés ou qu’il y a eu une erreur de navigation. Pour savoir si la navigation a abouti et la propriété webErrorStatus pour plus d’informations sur l’erreur de navigation, consultez la propriété propriétés IsSuccess de l’événement. Des erreurs de navigation peuvent se produire avant d’obtenir du contenu du réseau, par exemple si le nom d’hôte d’un URI n’est pas résolu dans le cas où l’événement MSWebViewNavigationStarted se déclenche, suivi de l’événement MSWebViewNavigationCompleted. Des erreurs de navigation peuvent également se produire après avoir reçu une page d’erreur d’un serveur Web, par exemple une page 404 d’un serveur HTTP dans lequel tous les événements de navigation sont déclenchés, MSWebViewNavigationStarting, MSWebViewContentLoading, MSWebViewDOMContentLoaded, puis MSWebViewNavigationCompleted. Pour indiquer la présence d’une page d’erreur de navigation dans les cas où le serveur Web n’a pas fourni de page d’erreur, vous devez vérifier si MSWebViewContentLoading n’a pas été activé pour une navigation en échec indiquant qu’il n’y a pas de page d’erreur fournie par le serveur.

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

#### Informations sur l’événement

|            |      |
|------------|------|
|**Interface** | [NavigationCompletedEvent](./webview/NavigationCompletedEvent.md) |
|**Synchrone** |Oui  |    
|**BD**     |Non |   
|**Annulable**  |Non |                 
         

### MSWebViewNavigationStarting

Indique que l' **affichage du WebView** commence. Ce problème est déclenché avant d’obtenir des ressources du réseau pour la navigation. La navigation n’a pas commencé tant que tous les gestionnaires d’événements MSWebViewNavigationStarting n’ont pas terminé. Cet événement peut être annulé par le biais de l’appel `eventArgs.preventDefault()` . S’il est annulé, le WebView n’effectue pas de navigation.


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

#### Informations sur l’événement

|            |      |
|------------|------|
|**Interface** | [NavigationEvent](./webview/NavigationEvent.md) |
|**Synchrone** |Non  |    
|**BD**     |Oui |   
|**Annulable**  |Oui |      

### MSWebViewNewWindowRequested

Déclenché lorsque le contenu du **WebView** tente d’ouvrir une nouvelle fenêtre. Si l’événement n’est pas annulé, le WebView lancera l’URI de la nouvelle demande de fenêtre dans le navigateur par défaut de l’utilisateur.

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

#### Informations sur l’événement

|            |      |
|------------|------|
|**Interface** | [NavigationEventWithReferrer](./webview/NavigationEventWithReferrer.md) |
|**Synchrone** |Oui  |    
|**BD**     |Non |   
|**Annulable**  |Oui |                 
           

### MSWebViewPermissionRequested

Indique que le contenu du **WebView** tente d’accéder à des fonctionnalités (par exemple, géolocalisation ou accès par verrouillage de pointeur) qui nécessitent une autorisation de l’utilisateur final. Si aucun gestionnaire d’événements n’est inscrit ou si le gestionnaire d’événements n’appelle pas eventArgs. permissionRequest. allow (), ajourne () ou Deny (), par défaut, la demande d’autorisation est refusée. Si vous avez besoin de décider si une autorisation est accordée ou refusée de manière asynchrone par exemple, si vous avez besoin d’inviter l’utilisateur, utilisez eventArgs. permissionRequest. Defer (). La demande d’autorisation est différée jusqu’à ce que vous utilisiez WebView. getDeferredPermissionRequestById ou WebView. getDeferredPermissionRequests, et appelez allow () ou Deny () sur le DeferredPermissionRequest avec la valeur ID correspondante.

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

#### Informations sur l’événement

|            |      |
|------------|------|
|**Interface** | [PermissionRequestedEvent](./webview/PermissionRequestedEvent.md) |
|**Synchrone** |Oui  |    
|**BD**     |Non |   
|**Annulable**  |Non |    


### MSWebViewProcessExited

Indique que le processus du composant **WebView** a crashé. Cela ne s’applique qu’à un WebView hors processus. Reportez-vous à la section Remarques sur la création d’un WebView hors processus plutôt qu’un WebView in-process. Après le déclenchement de cet événement, le WebView correspondant est mis dans un État bloqué. L’appel de la plupart des méthodes spécifiques d’affichage WebView ou l’accès à la plupart des propriétés spécifiques d’affichage sur un WebView bloqué lèvera une exception. Pour résoudre ce problème, supprimez le WebView bloqué du DOM et remplacez-le par un nouveau WebView.

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewProcessExited", handler);
webview.removeEventListener("MSWebViewProcessExited", handler);
```

#### Informations sur l’événement

|            |      |
|------------|------|
|**Interface** | **Événement** |
|**Synchrone** |Oui |    
|**BD**     |Non |   
|**Annulable**  |Non |      


### MSWebViewWebResourceRequested

Déclenché lorsqu’une page à l’intérieur de l’élément **WebView** demande une ressource.

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

#### Informations sur l’événement

|            |      |
|------------|------|
|**Interface** | [WebResourceRequestedEvent](./webview/WebResourceRequestedEvent.md) |
|**Synchrone** |Oui |    
|**BD**     |Non |   
|**Annulable**  |Non |      


### MSWebViewScriptNotify

Déclenché lorsqu’une page à l’intérieur de l’élément **WebView** appelle la méthode **Window. external. Notify** . La méthode Window. external. Notify est uniquement disponible pour les documents comportant des URI qui correspondent aux règles du ApplicationContentUriRules manifest’s de l’application ou qui a été autorisé par programmation via la définition de WebView. Settings. isScriptNotifyAllowed sur true. Par ailleurs, Window. external. Notify n’est disponible que pour le document de niveau supérieur de la WebView.

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

#### Informations sur l’événement

|            |      |
|------------|------|
|**Interface** | [ScriptNotifyEvent](./webview/ScriptNotifyEvent.md) |
|**Synchrone** |Oui  |    
|**BD**     |Non |   
|**Annulable**  |Non |      

### MSWebViewUnsafeContentWarningDisplaying

Se produit lorsque l' **affichage** Web affiche un avertissement pour le contenu signalé comme non sécurisé par le filtre SmartScreen.

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewUnsafeContentWarningDisplaying", handler);
webview.removeEventListener("MSWebViewUnsafeContentWarningDisplaying", handler);
```

#### Informations sur l’événement

|            |      |
|------------|------|
|**Interface** | **Événement** |
|**Synchrone** |Oui |    
|**BD**     |Non |   
|**Annulable**  |Non |    

### MSWebViewUnsupportedUriSchemeIdentified

Déclenché lors de la navigation vers un URI (Uniform Resource Identifier) que le **WebView** ne prend pas en charge.

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewUnsupportedUriSchemeIdentified", handler);
webview.removeEventListener("MSWebViewUnsupportedUriSchemeIdentified", handler);
```

#### Informations sur l’événement

|            |      |
|------------|------|
|**Interface** | [NavigationEvent](./webview/NavigationEvent.md) |
|**Synchrone** |Oui  |    
|**BD**     |Non |   
|**Annulable**  |Oui |     

### MSWebViewUnviewableContentIdentified

Déclenché lorsque le **WebView** tente d’accéder au contenu Web avec un type de contenu non pris en charge. Par exemple, les fichiers PDF ne sont actuellement pas pris en charge par le biais de l’affichage WebView et des navigations vers des documents PDF et déclenchent plutôt cet événement.

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

#### Informations sur l’événement

|            |      |
|------------|------|
|**Interface** | [UnviewableContentIdentifiedEvent](./webview/UnviewableContentIdentifiedEvent.md) |
|**Synchrone** |Oui  |    
|**BD**     |Non |   
|**Annulable**  |Non |                 
         

## Méthodes

### addWebAllowedObject

Ajoute un objet Windows Runtime natif en tant que paramètre global au document de niveau supérieur au sein d’un **WebView**.

L’objet n’est pas injecté dans le document actuel, mais plutôt dans le document de niveau supérieur suivant sur lequel l’affichage WebView se déplace. L’objet est injecté avant qu’un script du document HTML ne s’exécute, afin que vous puissiez compter sur l’objet dans le script global de votre document.

Vous devez utiliser addWebAllowedObject pendant un événement MSWebViewNavigationStarting ou avant d’appeler explicitement une méthode Navigate. Dans ces cas, l’objet est injecté dans le document de la navigation correspondante. Dans un autre contexte, vous ne pouvez pas être sûr de savoir quel document vous injectera.

L’appel de addWebAllowedObject plusieurs fois dans une ligne permet d’injecter plusieurs objets dans le document. Si vous l’appelez à la fois avant un appel de navigation explicite, puis de nouveau pendant l’événement MSWebViewNavigationStarting correspondant, les deux appels aboutissent et vous avez plusieurs objets injectés. Si vous appelez plusieurs fois avec le même paramètre de nom, le dernier appel WINS et les appels précédents avec ce nom sont ignorés.

En cas d’échec de la navigation ou d’une redirection, les appels addWebAllowedObject pour cette navigation sont ignorés. Si vous souhaitez gérer les redirections, vous pouvez vous abonner à l’événement MSWebViewNavigationStarting pour rediriger et appeler de nouveau addWebAllowedObject en fonction de ce qui est approprié pour votre application. De même, une fois qu’un document navigue vers l’extérieur, les objets injectés via addWebAllowedObject pour ce document ne seront pas reportés au document suivant et vous devrez appeler addWebAllowedObject explicitement si vous souhaitez qu’ils reportent le contrôle.

Si vous appelez addWebAllowedObject pour un document sans accès WinRT, ou s’il dispose d' [AllowForWebOnly accès via ApplicationContentUriRules](/uwp/schemas/appxpackage/uapmanifestschema/element-uap-rule) , l’objet sera injecté uniquement si l’objet a l’attribut de métadonnées Windows. Foundation. Metadata. AllowForWeb. Dans le cas contraire, une erreur est signalée et une erreur est signalée à la console développeur JavaScript. S’il est appelé sur un document qui dispose d’un accès WinRT complet, l’objet sera injecté indépendamment de l’attribut AllowForWeb. 

Par ailleurs, l’objet doit implémenter l’interface IAgileObject. En effet, les éléments WebView HTML et HTML s’exécutent sur les threads d’affichage de votre application et le thread JavaScript de l’application WebView est un thread thread asta différent et nous voulons encourager les développeurs d’applications à s’assurer que leur objet peut s’exécuter sur le thread JavaScript sans bloquer le thread d’affichage d’application, dans la mesure du possible.

Le paramètre Name doit être un nom de propriété JavaScript valide, sinon l’appel échoue en silence. S’il s’agit d’une propriété qui existe déjà sur l’objet global, cette propriété est écrasée si la propriété est configurable. Les propriétés non configurables sur l’objet global ne sont pas écrasées et l’appel addWebAllowedObject échoue en silence. Les propriétés JavaScript créées via addWebAllowedObject sont modifiables, configurables et Enumerable.

```js
let name = "exampleProperty";
webview.addWebAllowedObject(name, applicationObject);
webview.navigate("https://example.com/"); // applicationObject will be available as window.exampleProperty on https://example.com
```

#### Parameters
*name*
* Type: **chaîne**
* Nom de l’objet à exposer au document dans le **WebView**.

*applicationObject*
* Type: **objet**
* Objet à exposer dans le document dans le **WebView**.

#### Valeur renvoyée
Cette méthode ne renvoie pas de valeur.

#### Fonctionnalités et exigences supplémentaires

|            |      |
|------------|------|
|**Client minimal pris en charge** |Windows 10 [applications du Windows Store uniquement] |    
|**Serveur minimal pris en charge** |Aucun pris en charge |   
|**Téléphone minimum pris en charge**  |Aucun pris en charge |  

### buildLocalStreamUri

Crée un URI que vous pouvez transmettre à [navigateToLocalStreamUri](#methods).

```js
var string = webview.buildLocalStreamUri(contentIdentifier, relativePath);
```

#### Parameters
*contentIdentifier*
* Type: **chaîne**
* Identificateur unique pour le contenu référencé par l’URI. Cela définit la racine de l’URI.

*Entraîne*
* Type: **chaîne**
* Le chemin d’accès à la ressource, par rapport à la racine.

#### Valeur renvoyée
Type: **chaîne**

URI créé en combinant et en normalisant *contentIdentifier* et *relativePath*.

#### Exemple

L’exemple suivant illustre un cas d’utilisation classique. 

```js
var webview = document.createElement("x-ms-webview"); //Instantiate the webview element
var localStreamUri = webview.buildLocalStreamUri(contentIdentifier, relativePath); //Create URI to pass to navigateToLocalStreamUri method
webview.navigateToLocalStreamUri(localStreamUri, streamResolver); //Load the local web content 
```  

### capturePreviewToBlobAsync

Crée une image de l' [élément WebView](./webview.md) actuel et l’écrit dans l’élément image spécifié.

```js
var capturePreviewToBlobAsync = webview.capturePreviewToBlobAsync();
```

#### Parameters
Cette méthode n’a aucun paramètre.

#### Valeur renvoyée
Type: **MSWebViewAsyncOperation**

Un objet **MSWebViewAsyncOperation** qui, lorsqu’il se termine, fournit un objet **BLOB** contenant l’image. Lorsque vous utilisez **capturePreviewToBlobAsync**, vous devez définir des gestionnaires de réussite et d’erreur après la définition de l’opération. Après avoir appliqué les gestionnaires d’événements, appelez la méthode Start sur l’objet [MSWebViewAsyncOperation](./webview/MSWebViewAsyncOperation.md) pour exécuter l’opération.

### captureSelectedContentToDataPackageAsync 

> [!IMPORTANT]
> Cette méthode a été déconseillée et présente un problème connu. Évitez d’utiliser cette méthode dans votre code de production. 

Obtient de manière asynchrone un [DataPackage](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) qui contient le contenu sélectionné dans le **WebView**.

```js
var msWebViewAsyncOperation = webview.captureSelectedContentToDataPackageAsync();
```

#### Parameters
Cette méthode n’a aucun paramètre.

#### Valeur renvoyée
Type: **MSWebViewAsyncOperation**

Un objet **MSWebViewAsyncOperation** qui, lorsqu’il se termine, fournit un objet [DataPackage](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) contenant l’image. Lorsque vous utilisez **captureSelectedContentToDataPackageAsync**, vous devez définir des gestionnaires de réussite et d’erreur après la définition de l’opération. Après avoir appliqué les gestionnaires d’événements, appelez la méthode Start sur l’objet MSWebViewAsyncOperation pour exécuter l’opération.

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

### invokeScriptAsync

En tant qu’action asynchrone, exécute la fonction de script spécifiée à partir du code HTML actuellement chargé, avec des arguments spécifiques.

```js
webview.invokeScriptAsync(functionName, ...args)
```

#### Parameters

**Admises**
* Type: **chaîne**
* Nom de la fonction à appeler. Il s’agit d’un nom de propriété dans l’objet fenêtre globale du document de niveau supérieur de l’affichage. Il peut s’agir d’une fonction globale intégrée telle que Eval ou Open, ou d’une fonction définie par script sur l’objet Window global. Seules les fonctions figurant dans le document de niveau supérieur de l’affichage WebView sont parfois appelées.

**args**
* Type: **chaîne**
* Paramètres de chaîne facultatifs à passer à la fonction appelée. À l’issue de nomfonction, tout paramètre supplémentaire à invokeScriptAsync est une chaîne transmise à la fonction appelée.

#### Valeur renvoyée
Type: **MSWebViewAsyncOperation**

Lorsque vous utilisez **invokeScriptAsync**, vous devez définir des gestionnaires de réussite et d’erreur après la définition de l’opération. Après avoir appliqué les gestionnaires d’événements, appelez **MSWebViewAsyncOperation. Start** pour exécuter l’opération. Si l’événement complet de MSWebViewAsyncOperation se déclenche, la propriété Result de MSWebViewAsyncOperation est la valeur de retour de chaîne de l’appel de la fonction. L’utilisation de la valeur de retour de la fonction invoked permet à la communication par le biais du WebView de se reconnecter à l’hôte WebView de manière synchrone. Pour que le contenu WebView communique de manière asynchrone à l’hôte WebView, voir l’événement MSWebViewScriptNotify. Si la fonction appelée lève une exception non gérée, l’événement d’erreur de MSWebViewAsyncOperation se déclenche. 

```js
const functionName = "eval";
const args = ["'Current URL: ' + document.location.href"];

const asyncOp = webview.invokeScriptAsync(functionName, ...args);

asyncOp.onerror = () => console.error("Error: " + asyncOp.error);
asyncOp.oncomplete = () => console.log("Result: " + asyncOp.result); // Logs 'Current URL: about:blank'
asyncOp.start();
```

### getDeferredPermissionRequests

Renvoie une liste de demandes d’autorisation différées émises par le contenu du contrôle **WebView** .

```js
var sequence<PermissionRequest> = x-ms-webview.getDeferredPermissionRequests();
```

#### Parameters
Cette méthode n’a aucun paramètre.

#### Valeur renvoyée
Type: [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)

Demande d’autorisation différée spécifiée.

#### Fonctionnalités et exigences supplémentaires

|            |      |
|------------|------|
|**Client minimal pris en charge** |Windows 10 [applications du Windows Store uniquement] |    
|**Serveur minimal pris en charge** |Aucun pris en charge|   
|**Téléphone minimum pris en charge**  |Aucun pris en charge |    


### getDeferredPermissionRequestById

Renvoie la demande d’autorisation différée spécifiée. 

```js
var deferredPermissionRequest = x-ms-webview.getDeferredPermissionRequestById(id);
```

#### Parameters
*id*
* Type: **longue non signée**
* ID de la demande d’autorisation différée que vous souhaitez obtenir.

#### Valeur renvoyée
Type: [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)

Demande d’autorisation différée spécifiée.

#### Fonctionnalités et exigences supplémentaires

|            |      |
|------------|------|
|**Client minimal pris en charge** |Windows 10 [applications du Windows Store uniquement] |    
|**Serveur minimal pris en charge** |Aucun pris en charge|   
|**Téléphone minimum pris en charge**  |Aucun pris en charge | 

### goBack

Permet d’accéder à la page précédente de l’historique de navigation via le **WebView** . 

```js
webview.goBack();
```

#### Parameters
Cette méthode n’a aucun paramètre.

#### Valeur renvoyée
Cette méthode ne renvoie pas de valeur.

### goForward

Navigue vers la page suivante de l’historique de navigation du **WebView** . 

```js
webview.goForward();
```

#### Parameters
Cette méthode n’a aucun paramètre.

#### Valeur renvoyée
Cette méthode ne renvoie pas de valeur.

### naviguer

Charge le contenu HTML à l’URI (Uniform Resource Identifier) spécifié. 

```js
webview.navigate(uri);
```

#### Parameters

**uri**
* Type: **chaîne**
* URI à charger.

#### Valeur renvoyée
Cette méthode ne renvoie pas de valeur.

### navigateFocus

Déplace le focus sur le **WebView**. Déclenche l’événement navigatingfocus window’s du document de niveau supérieur de l’affichage. Les arguments FocusNavigationEvent utilisés dans l’événement navigatingfocus correspondent aux paramètres fournis à navigateFocus, sauf que les paramètres d’origine sont convertis à partir de l’espace de coordonnées du document hôte vers l’espace de coordonnées du document de niveau supérieur de la WebView. Voir l’événement WebView departingFocus et la méthode Window. departFocus correspondante pour transférer le focus du WebView vers l’hôte. Pour obtenir un exemple d’implémentation de la navigation au focus par le biais d’un clavier ou d’un boîtier de empilement qui utilise cette méthode, voir la [bibliothèque de navigation par TVJS](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) .

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

#### Parameters
*navigationReason*
* Type: **chaîne**
* Raison de la navigation. La valeur doit être «gauche», «haut», «droite» ou «bas». C’est la direction dans laquelle le focus quitte l’élément actuellement sélectionné.

*prêts*
* Type: **objet**
* Origine de la navigation. Il s’agit d’un objet JavaScript avec les propriétés «originLeft», «originTop», «originWidth» et «originHeight». Ces valeurs doivent décrire la position et la taille de l’élément actuellement sélectionné hors du mouvement.

#### Valeur renvoyée
Cette méthode ne renvoie pas de valeur.

### navigateToLocalStreamUri

Charge le contenu Web local à l’URI spécifié à l’aide d’un [**UriToStreamResolver**](/uwp/api/windows.web.iuritostreamresolver.uritostreamasync).

```js
webview.navigateToLocalStreamUri(source, streamResolver); 
```

#### Parameters

*origine*
* Type: **chaîne**
* URI MS-local-Stream qui identifie le contenu HTML local à charger. Créez cette chaîne à l’aide de [**buildLocalStreamUri**](/uwp/api/windows.web.ui.iwebviewcontrol.buildlocalstreamuri).

*streamResolver*
* Tapez: tout
* Un résolveur qui convertit l’URI en flux à charger.

#### Valeur renvoyée
Cette méthode ne renvoie pas de valeur.

### navigateToString

Charge le contenu HTML spécifié sous la forme d’un nouveau document. 

```js
webview.navigateToString(contents);
```

#### Parameters

*teneur*
* Type: **chaîne**
* Contenu HTML à afficher.

#### Valeur renvoyée
Cette méthode ne renvoie pas de valeur.

### navigateWithHttpRequestMessage

Accède au WebView à un URI (Uniform Resource Identifier) avec un en-tête de requête POST et des en-têtes HTTP. 

```js
webview.navigateWithHttpRequestMessage(requestMessage);
```

#### Parameters

*Collection RequestMessage*
* Type: **HttpRequestMessage**
* Détails de la requête HTTP. 

#### Valeur renvoyée
Cette méthode ne renvoie pas de valeur.

#### Remarques

> [!WARNING]
> Si vous ajoutez des en-têtes supplémentaires à cette requête, tels que les informations d’identification d’authentification, n’oubliez pas que ces en-têtes seront également inclus dans toutes les demandes enfant ultérieures. Faites preuve de prudence pour éviter toute divulgation accidentelle de renseignements confidentiels ou personnels. 


### mise 

Recharge le contenu actuel dans **WebView**. 

```js
webview.refresh();
```

#### Parameters
Cette méthode n’a aucun paramètre.

#### Valeur renvoyée
Cette méthode ne renvoie pas de valeur.


### stop

Arrête la navigation ou le téléchargement de l' **affichage WebView** actuel. 

```js
webview.stop();
```

#### Parameters
Cette méthode n’a aucun paramètre.

#### Valeur renvoyée
Cette méthode ne renvoie pas de valeur.


## Propriétés

### canGoBack

Obtient une valeur qui indique si le **WebView** peut naviguer vers l’arrière.

Cette propriété est en lecture seule.

```js
var canGoBack = webview.canGoBack;
```

#### Valeur de propriété
Type: **booléen**

**True** si **WebView** peut naviguer vers l’arrière; Sinon, **false**.

### canGoForward

Obtient une valeur qui indique s’il est possible d’accéder à **WebView** en aval.

Cette propriété est en lecture seule.

```js
var canGoForward = webview.canGoForward;
```

#### Valeur de propriété
Type: **booléen**

**True** si **WebView** peut naviguer vers l’avant; Sinon, **false**.

### containsFullScreenElement

Obtient une valeur qui indique si le **WebView** contient un élément qui prend en charge le plein écran. Pour plus d’informations, voir l’événement MSWebViewContainsFullScreenElementChanged.

Cette propriété est en lecture seule.

```js
var containsFullScreenElement = webview.containsFullScreenElement;
```

#### Valeur de propriété
Type: **booléen**

**True** si **WebView** contient un élément qui prend en charge le plein écran; Sinon, **false**.


### documentTitle

Obtient le titre de la page actuellement affichée dans le **WebView**. 

Cette propriété est en lecture seule.

```js
var documentTitle = webview.documentTitle;
```

#### Valeur de propriété
Type: **chaîne**

Le titre de la page.

### hauteur

Obtient ou définit la hauteur du **WebView**. 

```js
var height = webview.height;
webview.height = height;

```

#### Valeur de propriété
Type: **nombre**

Hauteur du **WebView**. 


### processus

Obtient le processus **WebView** .

Cette propriété est en lecture seule.

```js
var process = webview.process;
webview.process = process;
```

#### Valeur de propriété
Type: [MSWebViewProcess](./webview/MSWebViewProcess.md)


### settings

Obtient un objet [MSWebViewSettings](./webview/MSWebViewSettings.md) qui contient les propriétés permettant d’activer ou de désactiver les fonctionnalités **WebView** .

Cette propriété est en lecture seule.

```js
var settings = webview.settings;
webview.settings = settings;
```

#### Valeur de propriété
Type: [MSWebViewSettings](./webview/MSWebViewSettings.md)

Objet [MSWebViewSettings](./webview/MSWebViewSettings.md) qui contient les propriétés permettant d’activer ou de désactiver les fonctionnalités d' **affichage WebView** .

### src

Obtient ou définit la source URI (Uniform Resource Identifier) du contenu HTML à afficher dans le contrôle **WebView** . 

```js
var src = webview.src;
webview.src = src;
```

#### Valeur de propriété
Type: **chaîne**

Source URI du contenu HTML à afficher dans le contrôle **WebView** . 


### largeur

Obtient ou définit la largeur du **WebView**.

```js
var width = webview.width;
webview.width = width;
```

#### Valeur de propriété
Type: **nombre**

La largeur du **WebView**.
