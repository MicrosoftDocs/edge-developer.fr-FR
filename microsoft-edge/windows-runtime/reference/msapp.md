---
title: Référence sur les API MSApp
description: Fournit des fonctions d’assistance qui vous permettent de créer des objets BLOB et MSStream. Les objets et membres MSApp sont pris en charge pour les applications Windows en JavaScript.
author: mattwojo
ms.author: mattwoj
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: MSapp, PWA, téléchargement de fichier, blog, MSStream, applications Windows 10, UWP, Edge
ms.openlocfilehash: 0ed8cefa918bd44f3b2c4e8312d2c1d3b4ace8fc
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566653"
---
# MSApp

L’objet MSApp et ses membres sont uniquement pris en charge pour les applications Windows en JavaScript (y compris les fonctionnalités d’accès PWAs aux fonctionnalités de l’API Windows). L’objet MSApp existe uniquement dans le contexte local d’un document HTML dans une application Windows chargée via le schéma d’URI MS-Appx. dans le cas contraire, l’objet n’existe pas (et par conséquent, aucune de ses méthodes et propriétés n’est disponible).

Il fournit des fonctions d’assistance qui vous permettent de créer des objets [BLOB](https://developer.mozilla.org/docs/Web/API/Blob) et [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) .

```javascript
var result = MSApp.method;
```

| | |
| :--- | :--- |
| [**Méthodes**](#msapp-methods) | [clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher, pageHandlesAllApplicationActivations](#istaskscheduledatpriorityorhigher), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp.](#terminateapp) [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations) |

| | |
| :--- | :--- |
| [**Constantes**](#msapp-constants) | [actuel](#current), [élevé](#high), [inactif](#idle), [normal](#normal).|

| | |
| :--- | :--- |
| [Interface **MSAppAsyncOperation**](#msappasyncoperation) | [start](#start) |

## Méthodes MSApp

### clearTemporaryWebDataAsync 
Efface les données mises en cache et indexedDB pour l’application ou le [WebView](../../webview.md).

```javascript
var retval = MSApp.clearTemporaryWebDataAsync(#); 
```

#### Parameters
Cette méthode n’a aucun paramètre.

#### Valeur renvoyée
Nouveau[`IAsyncAction`](/uwp/api/windows.foundation.iasyncaction)

Représente une action asynchrone.

### createBlobFromRandomAccessStream
Crée un objet [BLOB](https://developer.mozilla.org/docs/Web/API/Blob) à partir d’un [`IRandomAccessStream`](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) objet. Cette méthode doit être utilisée pour gérer des `IRandomAccessStream` objets dans des applications afin de créer un objet basé sur W3C à partir du flux. Une fois l’objet BLOB créé, il peut être utilisé avec les API [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [URL](https://developer.mozilla.org/docs/Web/API/URL)et [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest). 

```javascript
var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
```

#### Parameters

`type` complémentaire

|Type | Description |
|:---- |:--- |
|Chaîne | Type de contenu des données. Cette chaîne doit être au format spécifié dans le jeton de type de média défini dans la section 3,7 de RFC 2616.

`stream` complémentaire

|Type | Description |
|:---- |:--- |
|Indifférent | [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) stocker dans l’objet BLOB.

#### Valeur renvoyée
|Type | Description |
|:---- |:--- |
|Destiné | Nouvel objet BLOB qui contient le flux.

#### Exceptions
|Sauf | Condition |
|:---- |:--- |
|TypeMismatchError | Le type de nœud n’est pas compatible avec le type de paramètre attendu. TYPE_MISMATCH_ERR est retourné pour les versions antérieures à Internet Explorer 10.

#### Remarques
Crée un objet blob à partir des types Windows Runtime via l’espace de noms MSApp sur l’objet Window. Cette méthode crée un objet BLOB qui est essentiellement un wrapper léger sur l' [`RandomAccessStream`](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) objet qui lui est fourni. L’objet BLOB possède la durée de vie du flux et le flux sera fermé lorsque l’objet blob est détruit. 

#### Exemple

```javascript
var randomAccessStream = dataPackage.GetData("image/bmp");
var blob = window.MSApp.createBlobFromRandomAccessStream("image/bmp", randomAccessStream);
var url = window.URL.createObjectURL(blob, {oneTimeOnly:true});

document.getElementById("imagetag").src = url; 
```

### createDataPackage
Convertit la plage spécifiée de l’utilisateur ou de l’application en fragment HTML qui peut être partagé.

```javascript
var retVal = MSApp.createDataPackage(object); 
```

#### Parameters
`object` complémentaire

|Type | Description |
|:---- |:--- |
|Indifférent | Ce type de plage peut être créé à partir d’un objet Selection, par exemple: `window.selection.getRangeAt(0)` , ou manuellement.

#### Valeur renvoyée
|Type | Description |
|:---- |:--- |
|Indifférent | Contient le balisage HTML pour la plage spécifiée.

#### Remarques
Cette méthode prend uniquement en charge la [plage DOM](https://developer.mozilla.org/docs/Web/API/Range)et non [TextRange](/uwp/api/windows.ui.xaml.documents.textrange). Le package de données retourné pour la plage spécifiée contient le balisage HTML au format Clipboard.

Aucune propriété n’est disponible pour le package de données renvoyées.

### createDataPackageFromSelection 
Convertit la sélection de l’utilisateur ou de l’application en fragment HTML qui peut être partagé.

```javascript
var retVal = MSApp.createDataPackageFromSelection(); 
```

#### Parameters
Cette méthode n’a aucun paramètre.

#### Valeur renvoyée
|Type | Description |
|:---- |:--- |
|Indifférent | Contient le balisage HTML pour la plage spécifiée.

#### Remarques
Le package de données retourné pour la sélection contient le balisage HTML au format Clipboard. S’il n’y a pas de sélection d’utilisateur n’importe où dans l’interface utilisateur de l’application, la fonction `createDataPackageFromSelection` renvoie la valeur null.

Aucune propriété n’est disponible pour le package de données renvoyées.
 
### createFileFromStorageFile 
Convertit un objet [WinRT](/uwp/api/) [`StorageFile`](/uwp/api/windows.storage.storagefile) en objet W3C standard [`File`](https://developer.mozilla.org/docs/Web/API/File) .

```javascript
var retVal = MSApp.createFileFromStorageFile(storageFile); 
```

#### Parameters
`storageFile` complémentaire

|Type | Description |
|:---- |:--- |
|Indifférent | Contient le fichier de stockage.

#### Exceptions
|Sauf | Condition |
|:---- |:--- |
|TypeMismatchError | La référence de fichier W3C spécifiée n’est pas valide. TYPE_MISMATCH_ERR est retourné pour les versions antérieures à Internet Explorer 10.

### createStreamFromInputStream  

Crée un [`MSStream`](https://msdn.microsoft.com/library/hh772328) à partir de [`InputStream`](https://msdn.microsoft.com/library/hh772327) .  


```javascript
var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
```

#### Parameters
`type` complémentaire

|Type | Description |
|:---- |:--- |
|DOMString | Type de contenu des données. Cette chaîne doit être au format spécifié dans le jeton de type de média défini dans la section 3,7 de RFC 2616. (Pour plus d’outils,[voir types MIME,](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types) IE. text/plain, text/html, image/JPEG, image/png, audio/MPEG, audio/OGG, audio/*, vidéo/MP4, etc.). 

`inputStream` complémentaire

|Type | Description |
|:---- |:--- |
|Indifférent | [`IInputStream`](/uwp/api/Windows.Storage.Streams.IInputStream)À stocker dans le `MSStream` .

#### Remarques
Cette méthode prend un type de contenu et la `IInputStream` référence. La méthode vérifie que la référence de flux transmise est une instance de type `IInputStream` et si ce n’est pas le cas, lève `DOMException TYPE_MISMATCH_ERR` . S’il n’y a aucune erreur, `createStreamFromInputStream` crée un `MSStream` (à partir de ses entrées).

#### Exemple
Un `IInputStream` peut être utilisé pour créer un `MSStream` . Comme `MSStreams` ces objets font l’objet d’une utilisation par nature, toutes les URL créées par `URL.createObjectURL` sont révoquées la première fois qu’il est résolu par l’élément image. De plus, les demandes d’une deuxième URL sur cet objet après que le flux a été utilisé échoueront.

```javascript
var inputStream = myInputStream; //get InputStream from socket API, etc.
var stream = MSApp.createStreamFromInputStream("image/bmp", inputstream);
document.getElementById("imagetag").src = URL.createObjectURL(stream); 
```

### execAsyncAtPriority 
Planifie l’exécution d’un rappel à un moment ultérieur en fonction de la priorité donnée. 

```javascript
MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
```

#### Parameters
`asynchronousCallback` complémentaire

|Type | Description |
|:---- |:--- |
|Fonction | Fonction callback qui s’exécute de manière asynchrone et est distribuée à la priorité de priorité spécifiée.

`priority` complémentaire

|Type | Description |
|:---- |:--- |
|DOMString | Valeur de priorité contextuelle à laquelle le rappel asynchronousCallback est exécuté. Voir [constantes MSApp](#msapp-constants).

`args` complémentaire

|Type | Description |
|:---- |:--- |
|Indifférent | Série d’arguments facultatives transmis à la fonction de rappel synchronousCallback (en tant que paramètres 1 et activé).

#### Valeur renvoyée
Cette méthode ne renvoie pas de valeur.

#### Remarques
La `asynchronousCallback` fonction de rappel fournie s’exécute de manière asynchrone plus tard. `asynchronousCallback` sera distribué en fonction de la priorité fournie. La priorité normale équivaut à la [`setImmediate`](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) méthode existante. Lorsque le rappel est exécuté, la priorité contextuelle actuelle est définie sur la valeur de paramètre de priorité fournie pour la durée de l’exécution du rappel.

Le `asynchronousCallback` paramètre callback peut être n’importe quelle fonction. Si des arguments sont fournis après le `priority` paramètre, ils sont tous transmis à la fonction callback.

`execAtPriority`À la différence, tout objet renvoyé par la `asynchronousCallback` fonction de rappel est ignoré (et non renvoyé par le biais de `execAsyncAtPriority` ).

### execAtPriority 
Exécute la fonction de rappel spécifiée dans la priorité contextuelle spécifiée.

```javascript
var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
```

#### Parameters
`synchronousCallback` complémentaire

|Type | Description |
|:---- |:--- |
|Fonction | Fonction callback qui s’exécute de façon synchrone selon la priorité contextuelle spécifiée.

`priority` complémentaire

|Type | Description |
|:---- |:--- |
|DOMString | Valeur de priorité spécifiée à laquelle la valeur de priorité contextuelle actuelle sera définie lors de l’exécution de la `synchronousCallback` fonction de rappel. Voir [constantes MSApp](#msapp-constants).

`args` complémentaire

|Type | Description |
|:---- |:--- |
|Indifférent | Série d’arguments facultatives transmis à la fonction de `synchronousCallback` rappel (en tant que paramètres 1 et activés).

#### Valeur renvoyée
|Type | Description |
|:---- |:--- |
|Indifférent | Renvoie la valeur de retour du `synchronousCallback` rappel (le cas échéant).

#### Remarques
La `synchronousCallback` méthode de rappel fournie s’exécute de façon synchrone. La priorité contextuelle actuelle est remplacée par la valeur de priorité fournie (fournie par l’argument Priority) pour la durée de la fonction de rappel fournie. Après l’exécution de la fonction de rappel, Priority est retourné à la valeur précédente avant l' `execAtPriority` appel. La valeur de retour de `execAtPriority` correspond à la valeur de retour de la méthode de rappel (telle qu’elle est fournie).
 
Le `synchronousCallback` paramètre callback peut être n’importe quelle fonction. Si un argument est fourni après le paramètre Priority, il est transmis à la méthode de rappel fournie. Si le paramètre callback renvoie une valeur, cette valeur devient également la valeur de retour `execAtPriority` .

#### Exemple

```javascript
var user = Windows.System.UserProfile.UserInformation;

MSApp.execAtPriority(function () { // This callback executes synchronously.
  user.getFirstNameAsync().then(function () { // Dispatches at high priority.
    return user.getLastNameAsync();
  }).done(function () { // Dispatches at high priority.
    // USEFUL CODE HERE
  });
}, MSApp.HIGH); // The second argument of the execAtPriority method.
```

### getCurrentPriority 
Renvoie la priorité contextuelle actuelle.

```javascript
var retval = MSApp.getCurrentPriority();
```

#### Parameters
Aucune. 

#### Valeur renvoyée
|Type | Description |
|:---- |:--- |
|DOMString | La valeur de retour est l’une des chaînes `MSApp.HIGH` , `MSApp.NORMAL` ou `MSApp.IDLE` .

#### Remarques
Cette méthode renvoie la priorité contextuelle actuelle (voir [`MSApp Constants`](#msapp-constants) ), qui peut être modifiée via `execAtPriority` et `execAsyncAtPriority` .

#### Exemple

```javascript
if (MSApp.getCurrentPriority() === MSApp.IDLE) { 
  // YOUR CODE HERE
}
```

### getHtmlPrintDocumentSource  

API synchrone qui est déconseillée. Pour Windows 10, voir `getHtmlPrintDocumentSourceAsync` . Pour les applications Windows 8 et 8,1, consultez le site Web entrée pour [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).  

### getHtmlPrintDocumentSourceAsync
Renvoie le contenu source à imprimer.

#### Parameters
`htmlDoc` complémentaire

|Type | Description |
|:---- |:--- |
|Document | Le document HTML à imprimer. Il peut s’agir du document racine, du document dans un IFRAME, d’un fragment de document ou d’un document SVG. Sachez que htmlDoc doit être un document et non un élément.

#### Exemple1

```javascript
var printTask = event.request.createPrintTask(title, function (args) {
                var deferral = args.getDeferral();
                var getPrintDocumentSourceAsync;
                if (MSApp.getHtmlPrintDocumentSourceAsync) { // Windows 10
                    getPrintDocumentSourceAsync = MSApp.getHtmlPrintDocumentSourceAsync(document);
                } else {
                    getPrintDocumentSourceAsync = WinJS.Promise.as(MSApp.getHtmlPrintDocumentSource(document));
                }
                getPrintDocumentSourceAsync.then(function (source) {
                    args.setSource(source);
                    deferral.complete();
                }, function (error) {
                    console.error(error);
                    deferral.complete();
                });
            });
```

#### Exemple2

```javascript
    function registerForPrintContract() {
            var printManager = Windows.Graphics.Printing.PrintManager.getForCurrentView();
            printManager.onprinttaskrequested = onPrintTaskRequested;
            console.log("Print Contract registered. Use the Print button to print.", "sample", "status");
    }
    
    // Variable to hold the document source to print
    var gHtmlPrintDocumentSource = null;
    
    // Print event handler for printing via the PrintManager API.
    function onPrintTaskRequested(printEvent) {
        var printTask = printEvent.request.createPrintTask("Print Sample", function (args) {
            args.setSource(gHtmlPrintDocumentSource);
    
            // Register the handler for print task completion event
            printTask.oncompleted = onPrintTaskCompleted;
        });
    }
    
    // Print Task event handler is invoked when the print job is completed.
    function onPrintTaskCompleted(printTaskCompletionEvent) {
        // Notify the user about the failure
        if (printTaskCompletionEvent.completion === Windows.Graphics.Printing.PrintTaskCompletion.failed) {
            console.log("Failed to print.", "sample", "error");
        }
    }
    
    // Executed just before printing.
    var beforePrint = function () {
        // Replace with code to be executed just before printing the current document:
    };
    
    // Executed immediately after printing.
    var afterPrint = function () {
        // Replace with code to be executed immediately after printing the current document:
    };
    
    function printButtonHandler() {
        // Optionally, functions to be executed immediately before and after printing can be configured as following:
        window.document.body.onbeforeprint = beforePrint;
        window.document.body.onafterprint = afterPrint;
    
        // Get document source to print
        MSApp.getHtmlPrintDocumentSourceAsync(document).then(function (htmlPrintDocumentSource) {
            gHtmlPrintDocumentSource = htmlPrintDocumentSource;
    
            // If the print contract is registered, the print experience is invoked.
            Windows.Graphics.Printing.PrintManager.showPrintUIAsync();
        });
    }
```

### getViewId 
Prise en charge de plusieurs fenêtres. 

> [!NOTE] 
> Dans les applications UWP JavaScript de Win 8.1 prises en charge plusieurs fenêtres utilisant des API MSApp DOM qui sont désormais depricated. Pour Windows 10, utilisez `window.open` , `window` et le nouveau `MSApp.getViewId` .

| Description |Windows 10 | Windows 8.1 |  
|:---- |:---- |:--- |  
| Créer une fenêtre | [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) | [`MSApp.createNewView`](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
|Nouvel objet Window | [`window`](https://developer.mozilla.org/docs/Web/API/Window) |[`MSAppView`](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  

```javascript
var retval = MSApp.getViewId(window); 
```

#### Parameters
`window`

|Type | Description |
|:---- |:--- |
|DOMString | Objet représentant une fenêtre contenant un document DOM. | 

#### Valeur renvoyée

`viewId`

|Type | Description |
|:---- |:--- |
|Nombre | Peut être utilisé avec les diverses [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) API. 

#### Remarques
Utiliser [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) et [`window`](https://developer.mozilla.org/docs/Web/API/Window) pour créer des fenêtres, mais pour interagir avec des API WinRT, ajoutez l' `MSApp.getViewId` API. Il accepte un `window` objet en tant que paramètre et renvoie un `viewId` nombre qui peut être utilisé avec les diverses [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) API. 

##### Retardement de la visibilité 
Dans le cas d’un affichage complet, les vues sont masquées et le développeur `TryShowAsStandaloneAsync` doit afficher l’affichage une fois qu’il est entièrement préparé. Dans le monde Web, `window.open` affiche une fenêtre immédiatement et l’utilisateur final peut voir le contenu chargé et affiché. Pour que votre nouvelle Windows serve de vues dans WinRT et qu’elle ne soit pas affichée immédiatement, nous avons ajouté une `window.open` option. Exemple:
`let newWindow = window.open("https://example.com", null, "msHideView=yes");`

##### Différences entre les fenêtres principales
La fenêtre principale ouverte par le système d’exploitation agit de la même manière que celle des fenêtres secondaires qui s’affichent: 

|Description | Principal | Secondaire |
|:---- |:--- |:--- |
|fenêtre. ouvrir | Autorisée | Non autorisé |
|Window. Close | Fermer l’application | Fermer la fenêtre |
| Restrictions de navigation | FORME règles ACUR uniquement | Aucune restriction |

Il est possible que l’ouverture d’un autre Windows ne puisse changer dans le futur en fonction de votre [avis](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).

##### Restrictions de communication d’origine identiques 
La prise en charge d’un problème technique unique empêche une prise en charge de la prise en charge de la synchronisation, des appels entre les scripts. Lorsque vous ouvrez une fenêtre qui est identique à l’origine, le script d’une fenêtre est autorisé à appeler directement les fonctions dans l’autre fenêtre, et certains de ces appels échouent. `postMessage` les appels fonctionnent parfaitement et il est recommandé de procéder comme vous le souhaitez. Le travail pour améliorer ce problème est en cours.


### isTaskScheduledAtPriorityOrHigher 
Renvoie une donnée de type booléen indiquant s’il existe une tâche en attente au niveau de priorité donné ou une valeur supérieure.

```javascript
var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
```

#### Parameters
`priority` complémentaire

|Type | Description |
|:---- |:--- |
|DOMString | Valeur de priorité (voir [constantes MSApp](#msapp-constants)) spécifiant le niveau de priorité et au-dessus pour rechercher tout Work en attente.

#### Valeur renvoyée
|Type | Description |
|:---- |:--- |
|Booléen | Renvoie `true` s’il existe un fonctionnement en file d’attente au niveau de priorité spécifié, `false` sinon.

#### Remarques
Cette `isTaskScheduledAtPriorityOrHigher` méthode fournit un moyen pour le code JavaScript de déterminer s’il existe des tâches en attente aux différents niveaux de priorité (ou au-dessus), de manière à ce que le code JavaScript de l’appel puisse décider de produire une plus grande priorité.

#### Exemple

```javascript
function performIdleWork(array_in) {
  var idx = 0;

  function performIdleWorkHelper() {
    for (; idx < array_in.length; ++idx) {

      // USEFUL CODE HERE 

      if (MSApp.isTaskScheduledAtPriorityOrHigher(MSApp.NORMAL)) {
        MSApp.execAsyncAtPriority(performIdleWorkHelper, msPriority.IDLE);
        break;
      } // if
    } // for
  } // performIdleWorkHelper

  performIdleWorkHelper();
} // performIdleWork
```

### pageHandlesAllApplicationActivations
Permet d’éviter une actualisation du chemin de démarrage (rechargement de la page) avant chaque événement d’activation (IE, en cliquant sur une notification ou sur une vignette épinglée). 

#### Parameters

|Type | Description |
|:---- |:--- |
Booléen | Utilisez `MSApp.pageHandlesAllApplicationActivations(true)` cette méthode pour toujours éviter d’actualiser la trajectoire de début (rechargement de la page) et de passer directement au déclenchement de l' `WebUIApplication` événement Activated. Nécessite que toutes les pages gèrent les événements d’activation séparément. En définissant cette méthode `true` , en cliquant sur un événement Activated (par exemple, un notificaiton) ne déclenche pas la recharge, une application essentielle pour les applications sur une page unique veut éviter les recharges de pages.

#### Exemple 

```javascript
// Without this, the app will first refresh to the start path before every activate event
window.MSApp.pageHandlesAllApplicationActivations(true); 

// This must not be deffered so that it can receive the initial `activated` event in time
window.Windows.UI.WebUI.WebUIApplication.addEventListener(
    `activated`,
    e =>
        microsoftInterface.handleActivatedEvent(e);
    }),
    false
);
```

### suppressSubdownloadCredentialPrompts 
Détermine si une application supprime les invites d’authentification possibles lors du téléchargement de ressources.

```javascript
MSApp.suppressSubdownloadCredentialPrompts(suppress); 
```

#### Parameters
`suppress` complémentaire

|Type | Description |
|:---- |:--- |
|Booléen | La valeur true supprime les invites d’authentification potentielles. La valeur false ne supprime pas les invites d’authentification potentielles de l’utilisateur.

#### Valeur Returan
Aucune.

#### Remarques
La `suppressSubdownloadCredentialPrompts` méthode contrôle si une application supprime les invites d’authentification potentielles lors du téléchargement de ressources. Le comportement par défaut consiste à ne pas supprimer les invites d’informations d’identification.

`suppressSubdownloadCredentialPrompts` est destiné à être utilisé par des applications susceptibles de charger un nombre excessif de ressources qui nécessitent une authentification, par exemple une application de messagerie (qui peut contenir un bulletin d’informations contenant un nombre d’images nécessitant une authentification).

Lorsque vous supprimez des invites d’informations d’identification, les boîtes de dialogue d’authentification aux serveurs ne s’afficheront pas lors de l’accès aux ressources qui nécessitent une authentification et la ressource ne sera pas téléchargée. Notez que `suppressSubdownloadCredentialPrompts` l’authentification proxy ou les boîtes de dialogue de demande de certification du client n’ont pas d’impact sur les autres invites possibles, comme l’authentification du proxy ou les boîtes de dialogue de demande de certification

Sachez que cela a un `suppressSubdownloadCredentialPrompts` impact sur tout le contenu de l’application, y compris le contenu hébergé dans l' `webview` élément.
 
**Important:**  Les décisions d’instructions d’identification sont mises en cache. Par conséquent, si vous supprimez des invites d’informations d’identification, celles-ci peuvent être prises en compte immédiatement, permettant ainsi aux invites d’informations d’identification d’être supprimées.

#### Exemple

```javascript
/ Set to true to suppress potenial credential prompts:
MSApp.suppressSubdownloadCredentialPrompts(true); 
// Now one can load content or navigate iframe/webview to some other site.
```

### terminateApp
Arrête l’application actuelle et génère un rapport d’échec. 

```javascript
MSApp.terminateApp(error); 
```

#### Parameters
`error` complémentaire

Type | Description |
|:---- |:--- |
|Erreur | Un `Error` objet que vous pouvez utiliser pour décrire l’erreur à l’origine de l’arrêt. L' `Error` objet doit contenir les propriétés Number, description et Stack; un rapport d’échec n’est pas généré si l’objet ne contient pas ces propriétés.

#### Valeur renvoyée
Aucune.

#### Remarques
Si le problème signalé par `terminateApp` devient l’un des 5 premiers problèmes de votre application, il apparaît sur la page qualité de l’application.

#### Exemple
Cet exemple appelle `terminateApp` quand une exception est rencontrée. Il utilise l' `Error` objet fourni lors de la capture d’une exception. 

```javascript
try {  
        var obj2 = null;  
        obj2.val = 5;  
    }  
    catch(e) {  
        window.MSApp.terminateApp(e);  
    }  
```

### Constantes MSApp
Valeurs de priorité autorisées associées à `execAsyncAtPriority` , `execAtPriority` , `getCurrentPriority` et `isTaskScheduldAtPriorityOrHigher` .

#### Actuel
`current`

|Type | Description |
|:---- |:--- |
|DOMString | Lorsque `current` est utilisée avec la méthode appropriée (voir aussi section), la méthode utilise la priorité contextuelle actuelle lors de l’exécution de l’opération demandée.

#### High
`high`

|Type | Description |
|:---- |:--- |
|DOMString | Lorsque `high` est utilisé avec la méthode appropriée (voir aussi section), la méthode utilise une priorité supérieure à la valeur normale lors de l’exécution de l’opération demandée et distribue l’opération avant tout fonctionnement de priorité normale existant.

#### Inactif
`idle`

|Type | Description |
|:---- |:--- |
|DOMString | Lorsque `ideal` est utilisé avec la méthode appropriée (voir aussi section), la méthode utilise une priorité inférieure à la valeur normale lors de l’exécution de l’opération demandée et sera répartie de l’opération après tout fonctionnement prioritaire normal.

#### Normal
`normal`

|Type | Description |
|:---- |:--- |
|DOMString | Lorsque `normal` est utilisé avec la méthode appropriée (voir aussi section), la méthode utilise la priorité actuelle normale lors de l’exécution de l’opération demandée.

#### Exemple

```javascript
if (window.MSApp.CURRENT) {
  document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
}
```

#### Configuration requise
|MIDL | Mshtml. idl |
|:---- |:--- |

## MSAppAsyncOperation

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```

### start
Démarre `MSAppAsyncOperation` .

```javascript
var retval = MSAppAsyncOperation.start();
```

#### Parameters
Aucune.

#### Valeur renvoyée
Aucune.

#### Propriétés
`error` Propriétés

|Type | Description |
|:---- |:--- |
|DOMError | Représente une erreur dans `MSAppAsyncOperation` .

```javascript
p = object.error
```

`oncomplete` Propriétés

|Type | Description |
|:---- |:--- |
|EventHandler | Propriété permettant de définir un gestionnaire d’événements à l’achèvement de `MSAppAsyncOperation` .

```javascript
p = object.oncomplete
```

`onerror` Propriétés

|Type | Description |
|:---- |:--- |
|EventHandler | Propriété permettant de définir un gestionnaire d’événements sur une erreur au cours de l’appel `MSAppAsyncOperation` .

```javascript
p = object.onerror
```

`readyState` Propriétés

|Type | Description |
|:---- |:--- |
|Nombre | Représente l’état de l’opération asynchrone dans l’application Windows en JavaScript. Les valeurs incluent: Started [0], Completed [1], erreur [2].

```javascript
p = object.readyState
```

`result` Propriétés

|Type | Description |
|:---- |:--- |
|Indifférent |Représente le résultat de `MSAppAsyncOperation` .

```javascript
p = object.result
```
