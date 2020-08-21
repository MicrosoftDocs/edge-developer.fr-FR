---
title: Référence sur les API MSApp
description: Fournit des fonctions d’assistance qui vous permettent de créer des objets BLOB et MSStream.  Les objets et membres MSApp sont pris en charge pour les applications Windows en JavaScript.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/29/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: MSapp, PWA, téléchargement de fichier, blog, MSStream, applications Windows 10, UWP, Edge
ms.openlocfilehash: 4966f6afbe4e971d6a366de7e9b4f5a6cd2305e0
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942165"
---
# MSApp  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

L’objet MSApp et ses membres sont uniquement pris en charge pour les applications Windows en JavaScript \ (y compris les PWAs d’accès aux fonctionnalités de l’API Windows).  L’objet MSApp existe uniquement dans le contexte local d’un document HTML dans une application Windows chargée via le schéma d’URI MS-Appx. dans le cas contraire, l’objet n’existe pas (et par conséquent, aucune de ses méthodes et propriétés n’est disponible).  

Il fournit des fonctions d’assistance qui vous permettent de créer des objets [BLOB](https://developer.mozilla.org/docs/Web/API/Blob) et [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) .  

```javascript
var result = MSApp.method;
```  

:::row:::
   :::column span="1":::
      [Méthodes](#msapp-methods)  
   :::column-end:::
   :::column span="2":::
      [clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher, pageHandlesAllApplicationActivations](#istaskscheduledatpriorityorhigher), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp.](#terminateapp) [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Constantes](#msapp-constants)  
   :::column-end:::
   :::column span="2":::
      [actuel](#current), [élevé](#high), [inactif](#idle), [normal](#normal).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Interface MSAppAsyncOperation](#msappasyncoperation)  
   :::column-end:::
   :::column span="2":::
      [start](#start)  
   :::column-end:::
:::row-end:::  

## Méthodes MSApp  

### clearTemporaryWebDataAsync  

:::row:::
   :::column span="":::
      Efface les données mises en cache et indexedDB pour l’application ou le [WebView](../../webview.md).  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.clearTemporaryWebDataAsync(#); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      Cette méthode n’a aucun paramètre.  
   :::column-end:::
   :::column span="":::
      **Valeur renvoyée**  
      
      Type: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)  
      
      Représente une action asynchrone.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceptions**  
      
      Aucune.  
   :::column-end:::
   :::column span="":::
      **Remarques**  
      
      Aucune.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemple**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### createBlobFromRandomAccessStream  

:::row:::
   :::column span="":::
      Crée un objet [BLOB](https://developer.mozilla.org/docs/Web/API/Blob) à partir d’un objet [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) .  Cette méthode doit être utilisée pour gérer des `IRandomAccessStream` objets dans des applications afin de créer un objet basé sur W3C à partir du flux.  Une fois l’objet BLOB créé, il peut être utilisé avec les API [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [URL](https://developer.mozilla.org/docs/Web/API/URL)et [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      `type` complémentaire  
      
      | Type | Description |  
      |:---- |:--- |  
      | Chaîne | Type de contenu des données.  Cette chaîne doit être au format spécifié dans le jeton de type de média défini dans la section 3,7 de RFC 2616.  |  
      
      `stream` complémentaire  
      
      | Type | Description |  
      |:---- |:--- |  
      | Indifférent | [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) stocker dans l’objet BLOB.  |  
   :::column-end:::
   :::column span="":::
      **Valeur renvoyée**  
      
      | Type | Description |  
      |:---- |:--- |  
      | Destiné | Nouvel objet BLOB qui contient le flux.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceptions**  
      
      | Sauf | Condition |  
      |:---- |:--- |  
      | TypeMismatchError | Le type de nœud n’est pas compatible avec le type de paramètre attendu.  TYPE_MISMATCH_ERR est retourné pour les versions antérieures à Internet Explorer 10.  |  
   :::column-end:::
   :::column span="":::
      **Remarques**  
      
      Crée un objet blob à partir des types Windows Runtime via l’espace de noms MSApp sur l’objet Window.  Cette méthode crée un objet BLOB qui est essentiellement un wrapper léger par le biais de l’objet [RandomAccessStream](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) qui lui est fourni.  L’objet BLOB possède la durée de vie du flux et le flux sera fermé lorsque l’objet blob est détruit.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemple**  
      
      ```javascript
      var randomAccessStream = dataPackage.GetData("image/bmp");
      var blob = window.MSApp.createBlobFromRandomAccessStream("image/bmp", randomAccessStream);
      var url = window.URL.createObjectURL(blob, {oneTimeOnly:true});
      
      document.getElementById("imagetag").src = url; 
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### createDataPackage  

:::row:::
   :::column span="":::
      Convertit la plage spécifiée de l’utilisateur ou de l’application en fragment HTML qui peut être partagé.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackage(object); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      `object` complémentaire  
      
      | Type | Description |  
      |:---- |:--- |  
      | Indifférent | Ce type de plage peut être créé à partir d’un objet Selection, par exemple: `window.selection.getRangeAt(0)` , ou manuellement.  |  
   :::column-end:::
   :::column span="":::
      **Valeur renvoyée**  
      
      | Type | Description |  
      |:---- |:--- |  
      | Indifférent | Contient le balisage HTML pour la plage spécifiée.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceptions**  
      
      Aucune.  
   :::column-end:::
   :::column span="":::
      **Remarques**  
      
      Cette méthode prend uniquement en charge la [plage DOM](https://developer.mozilla.org/docs/Web/API/Range)et non [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).  Le package de données retourné pour la plage spécifiée contient le balisage HTML au format Clipboard.  
      
      Aucune propriété n’est disponible pour le package de données renvoyées.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemple**  
      
      Aucune.  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### createDataPackageFromSelection  

:::row:::
   :::column span="":::
      Convertit la sélection de l’utilisateur ou de l’application en fragment HTML qui peut être partagé.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackageFromSelection(); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      Cette méthode n’a aucun paramètre.  
   :::column-end:::
   :::column span="":::
      **Valeur renvoyée**  
      
      | Type | Description |  
      |:---- |:--- |  
      | Indifférent | Contient le balisage HTML pour la plage spécifiée.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceptions**  
      
      Aucune.  
   :::column-end:::
   :::column span="":::
      **Remarques**  
      
      Le package de données retourné pour la sélection contient le balisage HTML au format Clipboard.  S’il n’y a aucune sélection d’utilisateur n’importe où dans l’interface utilisateur de l’application, le `createDataPackageFromSelection` retour `null` .  
      
      Aucune propriété n’est disponible pour le package de données renvoyées.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemple**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
 
### createFileFromStorageFile  

:::row:::
   :::column span="":::
      Convertit un [StorageFile](/uwp/api/windows.storage.storagefile) [WinRT](/uwp/api/) en un objet de [fichier](https://developer.mozilla.org/docs/Web/API/File) W3C standard.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createFileFromStorageFile(storageFile); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      `storageFile` complémentaire
      
      | Type | Description |  
      |:---- |:--- |  
      | Indifférent | Contient le fichier de stockage.  |  
   :::column-end:::
   :::column span="":::
      **Valeur renvoyée**
      
      None    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceptions**  
      
      | Sauf | Condition |  
      |:---- |:--- |  
      | TypeMismatchError | La référence de fichier W3C spécifiée n’est pas valide.  Pour les versions antérieures à Internet Explorer 10, `TYPE_MISMATCH_ERR` est retourné.  |  
   :::column-end:::
   :::column span="":::
      **Remarques**  
      
      Aucune.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemple**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### createStreamFromInputStream  

:::row:::
   :::column span="":::
      Crée un [MSStream](https://msdn.microsoft.com/library/hh772328) à partir d’un [InputStream](https://msdn.microsoft.com/library/hh772327).  
   :::column-end:::
   :::column span="":::
      ```javascript
      var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      `type` complémentaire
      
      | Type | Description |  
      |:---- |:--- |  
      | DOMString | Type de contenu des données.  Cette chaîne doit être au format spécifié dans le jeton de type de média défini dans la section 3,7 de RFC 2616.  \ ([Voir types MIME] (comme https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) `text/plain` ,,, `text/html` , `image/jpeg` `image/png` `audio/mpeg` , `audio/ogg` , `audio/*` , `video/mp4` et ainsi de suite).  
      
      `inputStream` complémentaire
      
      | Type | Description |  
      |:---- |:--- |  
      | Indifférent | Le [IInputStream](/uwp/api/Windows.Storage.Streams.IInputStream) que vous voulez stocker dans le `MSStream` .  |  
   :::column-end:::
   :::column span="":::
      **Valeur renvoyée**
      
      Aucune.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceptions**  
      
      Aucune.  
   :::column-end:::
   :::column span="":::
      **Remarques**  
      
      Cette méthode prend un type de contenu et la `IInputStream` référence.  La méthode vérifie que la référence de flux transmise est une instance de type `IInputStream` et si ce n’est pas le cas, lève `DOMException TYPE_MISMATCH_ERR` .  S’il n’y a aucune erreur, `createStreamFromInputStream` crée un `MSStream` \ (à partir de ses entrées \).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemple**  
      
      Un `IInputStream` peut être utilisé pour créer un `MSStream` .  Comme `MSStreams` ces objets font l’objet d’une utilisation par nature, toutes les URL créées par `URL.createObjectURL` sont révoquées la première fois qu’il est résolu par l’élément image.  De plus, les demandes d’une deuxième URL sur cet objet après que le flux a été utilisé échoueront.  
      
      ```javascript
      var inputStream = myInputStream; //get InputStream from socket API, and so on
      var stream = MSApp.createStreamFromInputStream("image/bmp", inputstream);
      document.getElementById("imagetag").src = URL.createObjectURL(stream); 
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### execAsyncAtPriority  

:::row:::
   :::column span="":::
      Planifie l’exécution d’un rappel à un moment ultérieur en fonction de la priorité donnée.  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      `asynchronousCallback` complémentaire
      
      | Type | Description |  
      |:---- |:--- |  
      | Fonction | Fonction callback qui s’exécute de manière asynchrone et est distribuée à la priorité de priorité spécifiée.  |  
      
      `priority` complémentaire
      
      | Type | Description |  
      |:---- |:--- |  
      | DOMString | Valeur de priorité contextuelle à laquelle le rappel asynchronousCallback est exécuté.  Voir [constantes MSApp](#msapp-constants).  |  
      
      `args` complémentaire
      
      | Type | Description |  
      |:---- |:--- |   
      | Indifférent | Série d’arguments facultatives transmis à la fonction de rappel synchronousCallback \ (en tant que paramètres 1 et ainsi de suite).  |  
   :::column-end:::
   :::column span="":::
      **Valeur renvoyée**  
      
      Cette méthode ne renvoie pas de valeur.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceptions**  
      
      Aucune.  
   :::column-end:::
   :::column span="":::
      **Remarques**  
      
      La `asynchronousCallback` fonction de rappel fournie s’exécute de manière asynchrone plus tard.  `asynchronousCallback` sera distribué en fonction de la priorité fournie.  La priorité normale équivaut à la méthode [setImmediate](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) existante.  Lorsque le rappel est exécuté, la priorité contextuelle actuelle est définie sur la valeur de paramètre de priorité fournie pour la durée de l’exécution du rappel.  
      
      Le `asynchronousCallback` paramètre callback peut être n’importe quelle fonction.  Si des arguments sont fournis après le `priority` paramètre, ils sont tous transmis à la fonction callback.  
      
      `execAtPriority`À la différence, tout objet renvoyé par la `asynchronousCallback` fonction de rappel est ignoré et n’est pas renvoyé via `execAsyncAtPriority` \.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemple**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### execAtPriority  

:::row:::
   :::column span="":::
      Exécute la fonction de rappel spécifiée dans la priorité contextuelle spécifiée.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      `synchronousCallback` complémentaire  
      
      | Type | Description |  
      |:---- |:--- |  
      | Fonction | Fonction callback qui s’exécute de façon synchrone selon la priorité contextuelle spécifiée.  |  
      
      `priority` complémentaire  
      
      | Type | Description |  
      |:---- |:--- |  
      | DOMString | Valeur de priorité spécifiée à laquelle la valeur de priorité contextuelle actuelle sera définie lors de l’exécution de la `synchronousCallback` fonction de rappel.  Voir [constantes MSApp](#msapp-constants).  |  
      
      `args` complémentaire  
      
      | Type | Description |  
      |:---- |:--- |  
      | Indifférent | Série facultative d’arguments transmis à la `synchronousCallback` fonction de rappel \ (en tant que paramètres 1 et ainsi de suite).  
   :::column-end:::
   :::column span="":::
      **Valeur renvoyée**  
      
      | Type | Description |  
      |:---- |:--- |  
      | Indifférent | Renvoie la valeur de retour du `synchronousCallback` rappel \ (le cas échéant).  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceptions**  
      
      Aucune.  
   :::column-end:::
   :::column span="":::
      **Remarques**  
      
      La `synchronousCallback` méthode de rappel fournie s’exécute de façon synchrone.  La priorité contextuelle actuelle est remplacée par la valeur de priorité fournie (fournie par l’argument Priority) pour la durée de la fonction de rappel fournie.  Après l’exécution de la fonction de rappel, Priority est retourné à la valeur précédente avant l' `execAtPriority` appel.  La valeur de retour de `execAtPriority` correspond à la valeur de retour de la méthode de rappel \ (fournie \).  
      
      Le `synchronousCallback` paramètre callback peut être n’importe quelle fonction.  Si un argument est fourni après le paramètre Priority, il est transmis à la méthode de rappel fournie.  Si le paramètre callback renvoie une valeur, cette valeur devient également la valeur de retour `execAtPriority` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemple**  
      
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
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### getCurrentPriority  

:::row:::
   :::column span="":::
      Renvoie la priorité contextuelle actuelle.  

   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getCurrentPriority();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      Aucune.  
   :::column-end:::
   :::column span="":::
      **Valeur renvoyée**  
      
      | Type | Description |  
      |:---- |:--- |  
      | DOMString | La valeur de retour est l’une des chaînes `MSApp.HIGH` , `MSApp.NORMAL` ou `MSApp.IDLE` .  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceptions**  
      
      Aucune.  
   :::column-end:::
   :::column span="":::
      **Remarques**  
      
      Cette méthode renvoie la priorité contextuelle actuelle \ (voir [constantes MSApp](#msapp-constants)\), qui peut être modifié via `execAtPriority` et `execAsyncAtPriority` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemple**  
      
      ```javascript
      if (MSApp.getCurrentPriority() === MSApp.IDLE) { 
          // YOUR CODE HERE
      }
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### getHtmlPrintDocumentSource  

API synchrone qui est déconseillée.  Pour Windows 10, voir `getHtmlPrintDocumentSourceAsync` .  Pour les applications Windows 8 et 8,1, consultez le site Web entrée pour [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).  

### getHtmlPrintDocumentSourceAsync  

:::row:::
   :::column span="":::
      Renvoie le contenu source à imprimer.  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.getHtmlPrintDocumentSourceAsync(document);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      `htmlDoc` complémentaire  
      
      | Type | Description |  
      |:---- |:--- |  
      | Document | Le document HTML à imprimer.  Il peut s’agir du document racine, du document dans un IFRAME, d’un fragment de document ou d’un document SVG.  Sachez que htmlDoc doit être un document et non un élément.  |  
   :::column-end:::
   :::column span="":::
      **Valeur renvoyée**
      
      Aucune.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceptions**  
      
      Aucune.  
   :::column-end:::
   :::column span="":::
      **Remarques**  
      
      Aucune.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemple1**  
      
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
   :::column-end:::
   :::column span="":::
      **Exemple2**  
      
      ```javascript
      function registerForPrintContract() {
              var printManager = Windows.Graphics.Printing.PrintManager.getForCurrentView();
              printManager.onprinttaskrequested = onPrintTaskRequested;
              console.log("Print Contract registered.  Use the Print button to print.", "sample", "status");
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
   :::column-end:::
:::row-end:::  

### getViewId  

:::row:::
   :::column span="":::
      Prise en charge de plusieurs fenêtres.  
      
      > [!NOTE] 
      > Dans les applications UWP JavaScript de Win 8.1 prises en charge plusieurs fenêtres utilisant des API MSApp DOM qui sont désormais depricated.  Pour Windows 10, utilisez `window.open` , `window` et le nouveau `MSApp.getViewId` .  
      
      | Description |Windows 10 | Windows 8.1 |  
      |:---- |:---- |:--- |  
      | Créer une fenêtre | [fenêtre. ouvrir](https://developer.mozilla.org/docs/Web/API/Window/open) | [MSApp. createNewView](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
      |Nouvel objet Window | [fenêtre](https://developer.mozilla.org/docs/Web/API/Window) |[MSAppView](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getViewId(window); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      `window`
      
      | Type | Description |  
      |:---- |:--- |  
      | DOMString | Objet représentant une fenêtre contenant un document DOM.  |  
   :::column-end:::
   :::column span="":::
      **Valeur renvoyée**  
      
      `viewId`
      
      | Type | Description |  
      |:---- |:--- |  
      | Nombre | Peut être utilisé avec les diverses API [Windows. UI. ViewManagement. ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) .  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceptions**  
      
      Aucune.  
   :::column-end:::
   :::column span="":::
      **Remarques**  
      
      Utilisez [Window. Open](https://developer.mozilla.org/docs/Web/API/Window/open) et [Window](https://developer.mozilla.org/docs/Web/API/Window) pour créer des fenêtres, mais pour interagir avec des API WinRT, ajoutez l' `MSApp.getViewId` API.  Il accepte un `window` objet en tant que paramètre et renvoie un `viewId` nombre qui peut être utilisé avec les diverses API [Windows. UI. ViewManagement. ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) .  
      
      *   Retardement de la visibilité  
          
          Dans le cas d’un affichage complet, les vues sont masquées et le développeur `TryShowAsStandaloneAsync` doit afficher l’affichage une fois qu’il est entièrement préparé.  Dans le monde Web, `window.open` affiche une fenêtre immédiatement et l’utilisateur final peut voir le contenu chargé et affiché.  Pour que votre nouvelle Windows serve de vues dans WinRT et qu’elle ne soit pas affichée immédiatement, nous avons ajouté une `window.open` option.  Par exemple:  
          
          ```javascript
          let newWindow = window.open("https://example.com", null, "msHideView=yes");
          ```  
          
      *   Différences entre les fenêtres principales  
          
          La fenêtre principale ouverte par le système d’exploitation agit de la même manière que celle des fenêtres secondaires qui s’affichent:  
          
          | Description | Principal | Secondaire |  
          |:---- |:--- |:--- |  
          | fenêtre. ouvrir | Autorisée | Non autorisé |  
          | Window. Close | Fermer l’application | Fermer la fenêtre |  
          | Restrictions de navigation | FORME règles ACUR uniquement | Aucune restriction |  
          
          Il est possible que l’ouverture d’un autre Windows ne puisse changer dans le futur en fonction de votre [avis](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).  
      
      *   Restrictions de communication d’origine identiques  
          
          La prise en charge d’un problème technique unique empêche une prise en charge de la prise en charge de la synchronisation, des appels entre les scripts.  Lorsque vous ouvrez une fenêtre qui est identique à l’origine, le script d’une fenêtre est autorisé à appeler directement les fonctions dans l’autre fenêtre, et certains de ces appels échouent.  `postMessage` les appels fonctionnent parfaitement et il est recommandé de procéder comme vous le souhaitez.  Le travail pour améliorer ce problème est en cours.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemple**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
    
### isTaskScheduledAtPriorityOrHigher  

:::row:::
   :::column span="":::
      Renvoie une donnée de type booléen indiquant s’il existe une tâche en attente au niveau de priorité donné ou une valeur supérieure.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      `priority` complémentaire
      
      | Type | Description |  
      |:---- |:--- |  
      | DOMString | Valeur de priorité \ (voir [constantes MSApp](#msapp-constants)\) spécifiant le niveau de priorité et au-dessus pour rechercher tout Work en attente.  |  
   :::column-end:::
   :::column span="":::
      **Valeur renvoyée**  
      
      | Type | Description |  
      |:---- |:--- |  
      | Booléen | Renvoie `true` s’il existe un fonctionnement en file d’attente au niveau de priorité spécifié, `false` sinon.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceptions**  
      
      Aucune.  
   :::column-end:::
   :::column span="":::
      **Remarques**  
      
      Cette `isTaskScheduledAtPriorityOrHigher` méthode fournit un moyen pour le code JavaScript de déterminer s’il existe des tâches en attente aux différents niveaux de priorité \ (ou au-dessus de \), ce qui permet à la personne d’appeler du code JavaScript de manière à utiliser une priorité plus élevée.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemple**  
      
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
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### pageHandlesAllApplicationActivations  

:::row:::
   :::column span="":::
      Permet d’éviter une actualisation de la trajectoire de début (rechargement de la page) avant chaque événement d’activation (par exemple, en cliquant sur une notification ou sur une vignette épinglée).  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.pageHandlesAllApplicationActivations(boolean);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      | Type | Description |  
      |:---- |:--- |  
      | Booléen | Utilisez `MSApp.pageHandlesAllApplicationActivations(true)` cette méthode pour toujours éviter d’actualiser la trajectoire de début (rechargement de la page) et de passer directement au déclenchement de l' `WebUIApplication` événement Activated.  Nécessite que toutes les pages gèrent les événements d’activation séparément.  En définissant cette méthode `true` , en cliquant sur un événement Activated (par exemple, une notification) ne déclenche pas le recharge, une application essentielle pour les applications à page unique veut éviter les recharges de pages.  |  
   :::column-end:::
   :::column span="":::
      **Valeur renvoyée**
      
      Aucune.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceptions**  
      
      Aucune.  
   :::column-end:::
   :::column span="":::
      **Remarques**  
      
      Aucune.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemple**  
      
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
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### suppressSubdownloadCredentialPrompts  

:::row:::
   :::column span="":::
      Détermine si une application supprime les invites d’authentification possibles lors du téléchargement de ressources.  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.suppressSubdownloadCredentialPrompts(suppress);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
     
      `suppress` complémentaire
      
      | Type | Description |  
      |:---- |:--- |  
      | Booléen | La valeur true supprime les invites d’authentification potentielles.  La valeur false ne supprime pas les invites d’authentification potentielles de l’utilisateur.  |  
   :::column-end:::
   :::column span="":::
      **Valeur renvoyée**  
      
      Aucune.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceptions**  
      
      Aucune.  
   :::column-end:::
   :::column span="":::
      **Remarques**  
      
      La `suppressSubdownloadCredentialPrompts` méthode contrôle si une application supprime les invites d’authentification potentielles lors du téléchargement de ressources.  Le comportement par défaut consiste à ne pas supprimer les invites d’informations d’identification.  
      
      `suppressSubdownloadCredentialPrompts` est destiné à être utilisé par des applications susceptibles de charger un nombre excessif de ressources qui nécessitent une authentification, par exemple une application de messagerie (qui peut contenir un bulletin d’informations contenant un certain nombre d’images nécessitant une authentification \).  
      
      Lorsque vous supprimez des invites d’informations d’identification, les boîtes de dialogue d’authentification aux serveurs ne s’afficheront pas lors de l’accès aux ressources qui nécessitent une authentification et la ressource ne sera pas téléchargée.  Notez que `suppressSubdownloadCredentialPrompts` l’authentification proxy ou les boîtes de dialogue de demande de certification du client n’ont pas d’impact sur les autres invites possibles, comme l’authentification du proxy ou les boîtes de dialogue de demande de certification  
      
      Sachez que cela a un `suppressSubdownloadCredentialPrompts` impact sur tout le contenu de l’application, y compris le contenu hébergé dans l' `webview` élément.  
      
      > [!IMPORTANT]
      > Les décisions d’instructions d’identification sont mises en cache.  Par conséquent, si vous supprimez des invites d’informations d’identification, celles-ci peuvent être prises en compte immédiatement, permettant ainsi aux invites d’informations d’identification d’être supprimées.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemple**  
      
      ```javascript
      // Set to true to suppress potential credential prompts:
      MSApp.suppressSubdownloadCredentialPrompts(true);
      // Now one can load content or navigate iframe/webview to some other site.
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### terminateApp  


:::row:::
   :::column span="":::
      Arrête l’application actuelle et génère un rapport d’échec.  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.terminateApp(error);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      `error` complémentaire
      
      | Type | Description |  
      |:---- |:--- |  
      | Erreur | Un `Error` objet que vous pouvez utiliser pour décrire l’erreur à l’origine de l’arrêt.  L' `Error` objet doit contenir les propriétés Number, description et Stack; un rapport d’échec n’est pas généré si l’objet ne contient pas ces propriétés.  |  
   :::column-end:::
   :::column span="":::
      **Valeur renvoyée**
      
      Aucune.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceptions**  
      
      Aucune.  
   :::column-end:::
   :::column span="":::
      **Remarques**  
      
      Si le problème signalé par `terminateApp` devient l’un des 5 premiers problèmes de votre application, il apparaît sur la page qualité de l’application.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemple**  
      
      Cet exemple appelle `terminateApp` quand une exception est rencontrée.  Il utilise l' `Error` objet fourni lors de la capture d’une exception.  
      
      ```javascript
      try {  
          var obj2 = null;  
          obj2.val = 5;  
      }  
      catch(e) {  
          window.MSApp.terminateApp(e);  
      }  
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### Constantes MSApp  

:::row:::
   :::column span="":::
      Valeurs de priorité autorisées associées à `execAsyncAtPriority` , `execAtPriority` , `getCurrentPriority` et `isTaskScheduldAtPriorityOrHigher` .  
   :::column-end:::
   :::column span="":::
      #### Actuel  
      
      `current`  
      
      | Type | Description |  
      |:---- |:--- |  
      | DOMString | Lorsque `current` est utilisé avec la méthode appropriée \ (voir aussi section \), la méthode utilise la priorité contextuelle actuelle lors de l’exécution de l’opération demandée.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### High  
      
      `high`  
      
      | Type | Description |  
      |:---- |:--- |  
      | DOMString | Lorsque `high` est utilisé avec la méthode appropriée \ (voir aussi section \), la méthode utilisera une priorité supérieure à la valeur normale lors de l’exécution de l’opération demandée et sera retirée de l’opération avant tout fonctionnement de priorité normale existant.  |  
   :::column-end:::
   :::column span="":::
      #### Inactif  
      
      `idle`  
      
      | Type | Description |  
      |:---- |:--- |  
      | DOMString | Lorsque `ideal` est utilisé avec la méthode appropriée \ (voir aussi section \), la méthode utilise une priorité inférieure à la valeur normale lors de l’exécution de l’opération demandée et sera retirée de l’opération après tout fonctionnement prioritaire normal.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### Normal  
      
      `normal`  
      
      | Type | Description |  
      |:---- |:--- |  
      | DOMString | Lorsque `normal` est utilisé avec la méthode appropriée (voir aussi section), la méthode utilise la priorité actuelle normale lors de l’exécution de l’opération demandée.  |  
   :::column-end:::
   :::column span="":::
      **Exemple**  
      
      ```javascript
      if (window.MSApp.CURRENT) {
          document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
      }
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Configuration requise**  
      
      | Type | Description |  
      |:---- |:--- |  
      | MIDL | Mshtml. idl |  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

## MSAppAsyncOperation  

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```  

### start  

:::row:::
   :::column span="":::
      Démarre `MSAppAsyncOperation` .  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSAppAsyncOperation.start();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      Aucune.  
   :::column-end:::
   :::column span="":::
      **Valeur renvoyée**
      
      Aucune.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      
      **Propriétés**  
      
      `error` Propriétés  
      
      | Type | Description |  
      |:---- |:--- |  
      | DOMError | Représente une erreur dans `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.error
      ```  
      
      `oncomplete` Propriétés  
      
      | Type | Description |  
      |:---- |:--- |  
      | EventHandler | Propriété permettant de définir un gestionnaire d’événements à l’achèvement de `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.oncomplete
      ```  
      
      `onerror` Propriétés  
      
      | Type | Description |  
      |:---- |:--- |  
      | EventHandler | Propriété permettant de définir un gestionnaire d’événements sur une erreur au cours de l’appel `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.onerror
      ```  
      
      `readyState` Propriétés  
      
      | Type | Description |  
      |:---- |:--- |  
      | Nombre | Représente l’état de l’opération asynchrone dans l’application Windows en JavaScript.  Les valeurs incluent `Started[0]` : `Completed[1]` , `Error[2]` .  |  
      
      ```javascript
      p = object.readyState
      ```  
      
      `result` Propriétés  
      
      | Type | Description |  
      |:---- |:--- |  
      | Indifférent |Représente le résultat de `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.result
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
