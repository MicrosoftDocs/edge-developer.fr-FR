---
title: Référence de l’API MSApp
description: Fournit des fonctions d’aide qui vous permettent de créer des objets Blob et MSStream.  Les objets et les membres MSApp sont pris en charge pour les applications Windows utilisant JavaScript.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
keywords: MSapp, PWA, chargement de fichiers, blog, MSStream, applications Windows 10, uwp, edge
ms.date: 03/16/2021
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0607929971b1dd2956571304230f69f756497e32
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439723"
---
# <a name="msapp"></a>MSApp  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

L’objet MSApp et ses membres sont pris en charge uniquement pour les applications Windows utilisant JavaScript \(y compris les applications P.A.S. accédant aux fonctionnalités de l’API Windows\).  L’objet MSApp existe uniquement dans le contexte local d’un document HTML dans une application Windows chargée via le schéma d’URI ms-appx ; sinon, l’objet n’existe pas (et par conséquent, aucune de ses méthodes et propriétés n’est disponible).  

Il fournit des fonctions d’aide qui vous permettent de créer des objets [Blob](https://developer.mozilla.org/docs/Web/API/Blob) et [MSStream.](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx)  

```javascript
var result = MSApp.method;
```  

:::row:::
   :::column span="1":::
      [Méthodes](#msapp-methods)  
   :::column-end:::
   :::column span="2":::
      [clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Constantes](#msapp-constants)  
   :::column-end:::
   :::column span="2":::
      [current](#current), [high](#high), [idle](#idle), [normal](#normal).  
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

## <a name="msapp-methods"></a>Méthodes MSApp  

### <a name="cleartemporarywebdataasync"></a>clearTemporaryWebDataAsync  

:::row:::
   :::column span="":::
      Clears cache and indexedDB data for the app or [WebView](../../hosting/webview/index.md).  
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
      
      Cette méthode ne possède aucun paramètre.  
   :::column-end:::
   :::column span="":::
      **Valeur renvoyée**  
      
      Type : [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)  
      
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

### <a name="createblobfromrandomaccessstream"></a>createBlobFromRandomAccessStream  

:::row:::
   :::column span="":::
      Crée un [objet Blob](https://developer.mozilla.org/docs/Web/API/Blob) à partir d’un [objet IRandomAccessStream.](/uwp/api/Windows.Storage.Streams.IRandomAccessStream)  Cette méthode doit être utilisée lorsque vous traitez des objets dans des applications afin de créer un objet `IRandomAccessStream` W3C à partir du flux.  Une fois l’objet blob créé, il peut être utilisé avec [les API FileReader,](https://developer.mozilla.org/docs/Web/API/FileReader) [URL](https://developer.mozilla.org/docs/Web/API/URL)et [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).  
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
      
      `type` [in]  
      
      | Type | Description |  
      |:---- |:--- |  
      | Chaîne | Type de contenu des données.  Cette chaîne doit être au format spécifié dans le jeton de type multimédia défini dans la section 3.7 de la RFC 2616.  |  
      
      `stream` [in]  
      
      | Type | Description |  
      |:---- |:--- |  
      | Indifférent | [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) à stocker dans l’objet Blob.  |  
   :::column-end:::
   :::column span="":::
      **Valeur renvoyée**  
      
      | Type | Description |  
      |:---- |:--- |  
      | Blob | Nouvel objet blob qui contient le flux.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceptions**  
      
      | Exception | Condition |  
      |:---- |:--- |  
      | TypeMismatchError | Le type de nœud est incompatible avec le type de paramètre attendu.  Pour les versions antérieures à Internet Explorer 10, TYPE_MISMATCH_ERR est renvoyé.  |  
   :::column-end:::
   :::column span="":::
      **Remarques**  
      
      Crée un objet Blob à partir de types Windows Runtime via l’espace de noms MSApp sur l’objet fenêtre.  Cette méthode crée un blob qui est essentiellement un wrapper clair sur l’objet [RandomAccessStream](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) qui lui est fourni.  Le blob est propriétaire de la durée de vie de ce flux et le flux est fermé lorsque l’objet blob est détruit.  
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

### <a name="createdatapackage"></a>createDataPackage  

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
      
      `object` [in]  
      
      | Type | Description |  
      |:---- |:--- |  
      | Indifférent | Cette plage peut être créée à partir d’un objet de sélection, par exemple `window.selection.getRangeAt(0)` : ou manuellement.  |  
   :::column-end:::
   :::column span="":::
      **Valeur renvoyée**  
      
      | Type | Description |  
      |:---- |:--- |  
      | Indifférent | Contient le code HTML de la plage spécifiée.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceptions**  
      
      Aucune.  
   :::column-end:::
   :::column span="":::
      **Remarques**  
      
      Cette méthode prend uniquement [en charge la plage DOM (Document Object Model),](https://developer.mozilla.org/docs/Web/API/Range)et non [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).  Le package de données renvoyé pour la plage spécifiée contient du code HTML au format Presse-papiers.  
      
      Il n’existe aucune propriété disponible pour le package de données renvoyé.  
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

### <a name="createdatapackagefromselection"></a>createDataPackageFromSelection  

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
      
      Cette méthode ne possède aucun paramètre.  
   :::column-end:::
   :::column span="":::
      **Valeur renvoyée**  
      
      | Type | Description |  
      |:---- |:--- |  
      | Indifférent | Contient le code HTML de la plage spécifiée.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceptions**  
      
      Aucune.  
   :::column-end:::
   :::column span="":::
      **Remarques**  
      
      Le package de données renvoyé pour la sélection contient le code HTML au format Presse-papiers.  S’il n’y a aucune sélection d’utilisateur dans l’interface utilisateur de l’application, le `createDataPackageFromSelection` retour `null` est fait.  
      
      Il n’existe aucune propriété disponible pour le package de données renvoyé.  
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
 
### <a name="createfilefromstoragefile"></a>createFileFromStorageFile  

:::row:::
   :::column span="":::
      Convertit un [fichier de stockage WinRT](/uwp/api/) [en](/uwp/api/windows.storage.storagefile) objet W3C [File](https://developer.mozilla.org/docs/Web/API/File) standard.  
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
      
      `storageFile` [in]
      
      | Type | Description |  
      |:---- |:--- |  
      | Indifférent | Contient le fichier de stockage.  |  
   :::column-end:::
   :::column span="":::
      **Valeur renvoyée**
      
      Aucun(e)    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceptions**  
      
      | Exception | Condition |  
      |:---- |:--- |  
      | TypeMismatchError | La référence de fichier W3C spécifiée n’est pas valide.  Pour les versions antérieures à Internet Explorer 10, `TYPE_MISMATCH_ERR` est renvoyée.  |  
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

### <a name="createstreamfrominputstream"></a>createStreamFromInputStream  

:::row:::
   :::column span="":::
      Crée un [flux MSStream](https://msdn.microsoft.com/library/hh772328) à partir d’un [flux d’entrée.](https://msdn.microsoft.com/library/hh772327)  
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
      
      `type` [in]
      
      | Type | Description |  
      |:---- |:--- |  
      | DOMString | Type de contenu des données.  Cette chaîne doit être au format spécifié dans le jeton de type multimédia défini dans la section 3.7 de la RFC 2616.  \([Voir les types MIME,]( https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) par `text/plain` `text/html` exemple, , `image/jpeg` , , , , , et ainsi de `image/png` `audio/mpeg` `audio/ogg` `audio/*` `video/mp4` suite\).  
      
      `inputStream` [in]
      
      | Type | Description |  
      |:---- |:--- |  
      | Indifférent | [IInputStream](/uwp/api/Windows.Storage.Streams.IInputStream) à stocker dans `MSStream` le .  |  
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
      
      Cette méthode prend un type de contenu et la `IInputStream` référence.  La méthode vérifie ensuite que la référence de flux transmise est une instance de type et, si ce n’est pas le `IInputStream` cas, elle le `DOMException TYPE_MISMATCH_ERR` fait.  Si aucune erreur ne se produit, `createStreamFromInputStream` crée `MSStream` un \(à partir de ses entrées\).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemple**  
      
      Un `IInputStream` peut être utilisé pour créer un `MSStream` .  Tout comme les objets à usage seul, toutes les URL créées par sont révoquées la première fois qu’elles sont résolues par `MSStreams` `URL.createObjectURL` l’élément image.  En outre, les demandes pour une deuxième URL sur cet objet après l’utilisation du flux échoueront.  
      
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

### <a name="execasyncatpriority"></a>execAsyncAtPriority  

:::row:::
   :::column span="":::
      Planifier l’exécution d’un rappel ultérieurement en fonction de la priorité donnée.  
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
      
      `asynchronousCallback` [in]
      
      | Type | Description |  
      |:---- |:--- |  
      | Fonction | Fonction de rappel à exécuter de manière asynchrone, répartie selon la priorité donnée.  |  
      
      `priority` [in]
      
      | Type | Description |  
      |:---- |:--- |  
      | DOMString | Valeur de priorité contextuelle à laquelle le rappel asynchroneCallback est exécuté.  Voir [les constantes MSApp.](#msapp-constants)  |  
      
      `args` [in]
      
      | Type | Description |  
      |:---- |:--- |   
      | Indifférent | Série facultative d’arguments transmis à la fonction de rappel SynchronousCallback \(en tant que paramètres 1 et ainsi de suite\).  |  
   :::column-end:::
   :::column span="":::
      **Valeur renvoyée**  
      
      Cette méthode ne retourne pas de valeur.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceptions**  
      
      Aucune.  
   :::column-end:::
   :::column span="":::
      **Remarques**  
      
      La fonction de rappel fournie est exécutée de manière `asynchronousCallback` asynchrone ultérieurement.  `asynchronousCallback` sera distribué en fonction de la priorité fournie.  La priorité normale équivaut à la méthode [setImmediate](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) existante.  Lorsque le rappel est exécuté, la priorité contextuelle actuelle est définie sur la valeur de paramètre de priorité fournie pour la durée de l’exécution du rappel.  
      
      Le `asynchronousCallback` paramètre de rappel peut être n’importe quelle fonction.  Si des arguments sont fournis après le paramètre, ils sont tous transmis `priority` à la fonction de rappel.  
      
      Contrairement à , tout objet renvoyé par la fonction de rappel `execAtPriority` `asynchronousCallback` est ignoré \(et n’est pas renvoyé via `execAsyncAtPriority` \).  
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

### <a name="execatpriority"></a>execAtPriority  

:::row:::
   :::column span="":::
      Exécute la fonction de rappel spécifiée à la priorité contextuelle donnée.  
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
      
      `synchronousCallback` [in]  
      
      | Type | Description |  
      |:---- |:--- |  
      | Fonction | Fonction de rappel à exécuter de manière synchrone selon la priorité donnée.  |  
      
      `priority` [in]  
      
      | Type | Description |  
      |:---- |:--- |  
      | DOMString | Valeur de priorité spécifiée à laquelle la valeur de priorité contextuelle actuelle sera définie lors de l’exécution de la fonction `synchronousCallback` de rappel.  Voir [les constantes MSApp.](#msapp-constants)  |  
      
      `args` [in]  
      
      | Type | Description |  
      |:---- |:--- |  
      | Indifférent | Série facultative d’arguments transmis à la fonction de rappel \(en tant que `synchronousCallback` paramètres 1 et ainsi de suite\).  
   :::column-end:::
   :::column span="":::
      **Valeur renvoyée**  
      
      | Type | Description |  
      |:---- |:--- |  
      | Indifférent | Renvoie la valeur de retour du `synchronousCallback` rappel \(le cas échéant\).  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceptions**  
      
      Aucune.  
   :::column-end:::
   :::column span="":::
      **Remarques**  
      
      La méthode de `synchronousCallback` rappel fournie est exécuté de manière synchrone.  La priorité contextuelle actuelle est modifiée en valeur de priorité fournie (donnée par l’argument de priorité) pour la durée de la fonction de rappel fournie.  Une fois l’exécution de la fonction de rappel exécutée, la priorité est renvoyée à la valeur précédente avant `execAtPriority` l’appel.  La valeur de retour est la valeur de retour de la méthode de rappel `execAtPriority` \(tel que fourni\).  
      
      Le `synchronousCallback` paramètre de rappel peut être n’importe quelle fonction.  Si des arguments sont fournis après le paramètre de priorité, ils sont transmis à la méthode de rappel fournie.  Si le paramètre de rappel renvoie une valeur, cette valeur devient également la valeur de `execAtPriority` retour.  
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

### <a name="getcurrentpriority"></a>getCurrentPriority  

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
      | DOMString | La valeur de retour est l’une des chaînes `MSApp.HIGH` `MSApp.NORMAL` , ou `MSApp.IDLE` .  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceptions**  
      
      Aucune.  
   :::column-end:::
   :::column span="":::
      **Remarques**  
      
      Cette méthode renvoie la priorité contextuelle actuelle \(voir [constantes MSApp](#msapp-constants)\), qui peut être modifiée via `execAtPriority` et `execAsyncAtPriority` .  
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

### <a name="gethtmlprintdocumentsource"></a>getHtmlPrintDocumentSource  

API synchrone qui a été dépréciée.  Pour Windows 10, voir `getHtmlPrintDocumentSourceAsync` .  Pour les applications Windows 8 et 8.1, consultez l’entrée MSDN pour [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).  

### <a name="gethtmlprintdocumentsourceasync"></a>getHtmlPrintDocumentSourceAsync  

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
      
      `htmlDoc` [in]  
      
      | Type | Description |  
      |:---- |:--- |  
      | Document | Document HTML à imprimer.  Il peut s’agit du document racine, du document dans un iFrame, d’un fragment de document ou d’un document SVG.  N’ignorez pas que htmlDoc doit être un document, et non un élément.  |  
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

### <a name="getviewid"></a>getViewId  

:::row:::
   :::column span="":::
      Prise en charge de plusieurs fenêtres.  
      
      > [!NOTE] 
      > Dans les applications UWP JavaScript Win8.1, plusieurs fenêtres étaient prise en charge à l’aide des API DOM MSApp qui sont désormais désapprouvées.  Pour Windows 10, utilisez `window.open` , et le nouveau `window` `MSApp.getViewId` .  
      
      | Description |Windows 10 | Windows 8.1 |  
      |:---- |:---- |:--- |  
      | Créer une fenêtre | [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) | [MSApp.createNewView](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
      |Nouvel objet window | [fenêtre](https://developer.mozilla.org/docs/Web/API/Window) |[MSAppView](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  
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
      | Nombre | Peut être utilisé avec les différentes [API Windows.UI.ViewManagement.ApplicationViewSwitcher.](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher)  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceptions**  
      
      Aucune.  
   :::column-end:::
   :::column span="":::
      **Remarques**  
      
      Utilisez [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) et [window](https://developer.mozilla.org/docs/Web/API/Window) pour créer de nouvelles fenêtres, puis pour interagir avec les API WinRT, ajoutez `MSApp.getViewId` l’API.  Elle prend un objet comme paramètre et renvoie un nombre qui peut être utilisé avec les différentes `window` `viewId` API [Windows.UI.ViewManagement.ApplicationViewSwitcher.](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher)  
      
      *   Retarder la visibilité  
          
          Les affichages dans WinRT démarrent normalement masqués et le développeur final utilise quelque chose comme pour afficher l’affichage une fois `TryShowAsStandaloneAsync` qu’il est entièrement préparé.  Dans le monde web, affiche une fenêtre immédiatement et l’utilisateur final peut observer le chargement et `window.open` le rendu du contenu.  Pour que vos nouvelles fenêtres agissent comme des vues dans WinRT et qu’ils ne s’affichent pas immédiatement, nous avons ajouté une `window.open` option.  Par exemple:  
          
          ```javascript
          let newWindow = window.open("https://example.com", null, "msHideView=yes");
          ```  
          
      *   Différences de fenêtre principale  
          
          La fenêtre principale initialement ouverte par le système d’exploitation agit différemment des fenêtres secondaires qu’elle ouvre :  
          
          | Description | Principal | Secondaire |  
          |:---- |:--- |:--- |  
          | window.open | Autorisée | Non autorisé |  
          | window.close | Fermer l’application | Fermer la fenêtre |  
          | Restrictions de navigation | ACUR uniquement | Aucune restriction |  
          
         <!-- The restriction to not allow secondary windows to open could change in the future depending on [feedback](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).  -->  
      
      *   Restrictions de communication d’origine identique  
          
          Il existe un problème technique difficile qui empêche la prise en charge appropriée des appels de script synchrones, de même origine, entre fenêtres.  Lorsque vous ouvrez une fenêtre de la même origine, le script d’une fenêtre est autorisé à appeler directement des fonctions dans l’autre fenêtre, et certains de ces appels échouent.  `postMessage` Les appels fonctionnent très bien et sont la façon recommandée d’y faire des choses si possible.  Des travaux sont en cours pour améliorer ce problème.  
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
    
### <a name="istaskscheduledatpriorityorhigher"></a>isTaskScheduledAtPriorityOrHigher  

:::row:::
   :::column span="":::
      Renvoie une valeur boolé nationale indiquant s’il existe un travail en attente au niveau de priorité donné ou supérieur.  
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
      
      `priority` [in]
      
      | Type | Description |  
      |:---- |:--- |  
      | DOMString | Une valeur de priorité \(voir [constantes MSApp](#msapp-constants)\) spécifiant le niveau de priorité et au-dessus pour interroger tout travail en file d’attente en attente.  |  
   :::column-end:::
   :::column span="":::
      **Valeur renvoyée**  
      
      | Type | Description |  
      |:---- |:--- |  
      | Booléen | Renvoie s’il existe des travaux en file d’attente au niveau de priorité spécifié ou supérieur, dans `true` le `false` cas contraire.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceptions**  
      
      Aucune.  
   :::column-end:::
   :::column span="":::
      **Remarques**  
      
      La méthode fournit un moyen pour le code JavaScript de déterminer s’il existe un travail en attente aux différents niveaux de priorité \(ou au-dessus\) dans l’intention que le code JavaScript appelant puisse ensuite décider de donner lieu à un travail `isTaskScheduledAtPriorityOrHigher` prioritaire.  
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

### <a name="pagehandlesallapplicationactivations"></a>pageHandlesAllApplicationActivations  

:::row:::
   :::column span="":::
      Permet d’éviter une actualisation du chemin d’accès de démarrage (rechargement de page) avant chaque événement d’activation \(par exemple, en cliquant sur une notification ou une vignette épinglée\).  
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
      | Booléen | Utilisez cette fonction pour toujours ignorer l’actualisation du chemin d’accès de démarrage (rechargement de page) et passer directement au tir de `MSApp.pageHandlesAllApplicationActivations(true)` `WebUIApplication` l’événement activé.  Nécessite que toutes les pages gèrent les événements d’activation séparément.  En définissant cette méthode comme étant , le fait de cliquer sur un événement activé \(comme une notification\) ne déclenche pas le rechargement, ce qui est essentiel pour les applications mono-page qui souhaitent éviter les `true` rechargements de page.  |  
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

### <a name="suppresssubdownloadcredentialprompts"></a>suppressSubdownloadCredentialPrompts  

:::row:::
   :::column span="":::
      Contrôle si une application supprime les invites d’authentification possibles pendant le téléchargement des ressources.  
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
     
      `suppress` [in]
      
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
      
      La `suppressSubdownloadCredentialPrompts` méthode contrôle si une application supprime les invites d’authentification potentielles pendant le téléchargement des ressources.  Le comportement par défaut consiste à ne pas supprimer les invites d’informations d’identification.  
      
      `suppressSubdownloadCredentialPrompts` est destiné à être utilisé par les applications qui peuvent charger un nombre excessif de ressources nécessitant une authentification, telles qu’une application de messagerie \(qui peut contenir un bulletin contenant un certain nombre d’images où chaque image requiert une authentification\).  
      
      Lors de la suppression des invites d’informations d’identification, les boîtes de dialogue d’authentification sur les serveurs ne s’afficheront pas lors de l’accès aux ressources nécessitant une authentification et la ressource ne sera pas téléchargée.  Notez que cela n’a pas d’impact sur les autres invites possibles telles que l’authentification proxy ou les boîtes de dialogue de demande de certification du client, ni sur `suppressSubdownloadCredentialPrompts` XHR.  
      
      N’ignorez pas `suppressSubdownloadCredentialPrompts` que cela a un impact sur tout le contenu de l’application, y compris le contenu hébergé dans l’élément. `webview`  
      
      > [!IMPORTANT]
      > Les décisions relatives aux invites d’informations d’identification sont mises en cache.  Par conséquent, bien que la suppression des invites d’informations d’identification prenne effet immédiatement, l’application des invites d’informations d’identification après leur suppression peut avoir besoin d’un rechargement du document pour prendre effet.  
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

### <a name="terminateapp"></a>terminateApp  


:::row:::
   :::column span="":::
      Met fin à l’application actuelle et génère un rapport d’échec.  
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
      
      `error` [in]
      
      | Type | Description |  
      |:---- |:--- |  
      | Erreur | Objet `Error` que vous pouvez utiliser pour décrire l’erreur qui a déclenché l’arrêt.  L’objet doit contenir le nombre, la description et les propriétés de pile ; un rapport d’échec ne sera pas généré si l’objet ne contient `Error` pas ces propriétés.  |  
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
      
      Si le problème signalé par devient l’un des 5 principaux problèmes de votre application, il s’affiche sur la page Qualité de `terminateApp` l’application.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemple**  
      
      Cet exemple appelle `terminateApp` lorsqu’une exception est rencontrée.  Il utilise `Error` l’objet fourni lorsque vous capturez une exception.  
      
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

### <a name="msapp-constants"></a>Constantes MSApp  

:::row:::
   :::column span="":::
      Valeurs de priorité autorisées `execAsyncAtPriority` associées `execAtPriority` à , et `getCurrentPriority` `isTaskScheduldAtPriorityOrHigher` .  
   :::column-end:::
   :::column span="":::
      #### <a name="current"></a>Actuel  
      
      `current`  
      
      | Type | Description |  
      |:---- |:--- |  
      | DOMString | Lorsqu’elle est utilisée avec la méthode appropriée \(voir aussi section\), la méthode utilise la priorité contextuelle actuelle lors de l’exécution de `current` l’opération demandée.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <a name="high"></a>High  
      
      `high`  
      
      | Type | Description |  
      |:---- |:--- |  
      | DOMString | Lorsqu’elle est utilisée avec la méthode appropriée \(voir aussi section\), la méthode utilise une priorité supérieure à la normale lors de l’exécution de l’opération demandée et l’exécute avant tout travail de priorité `high` normal existant.  |  
   :::column-end:::
   :::column span="":::
      #### <a name="idle"></a>Inactif  
      
      `idle`  
      
      | Type | Description |  
      |:---- |:--- |  
      | DOMString | Lorsqu’elle est utilisée avec la méthode appropriée \(voir aussi section\), la méthode utilise une priorité inférieure à la normale lors de l’exécution de l’opération demandée et répartit l’opération après tout travail de priorité `ideal` normale existant.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <a name="normal"></a>Normal  
      
      `normal`  
      
      | Type | Description |  
      |:---- |:--- |  
      | DOMString | Lorsqu’elle est utilisée avec la méthode appropriée (voir aussi la section), la méthode utilise la priorité normale existante lors de l’exécution de `normal` l’opération demandée.  |  
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
      | IDL | Mshtml.idl |  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

## <a name="msappasyncoperation"></a>MSAppAsyncOperation  

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```  

### <a name="start"></a>start  

:::row:::
   :::column span="":::
      Démarre `MSAppAsyncOperation` le .  
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
      
      `error` property  
      
      | Type | Description |  
      |:---- |:--- |  
      | DOMError | Représente une erreur dans `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.error
      ```  
      
      `oncomplete` property  
      
      | Type | Description |  
      |:---- |:--- |  
      | EventHandler | Propriété pour la définition d’un handler d’événements à l’achèvement de `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.oncomplete
      ```  
      
      `onerror` property  
      
      | Type | Description |  
      |:---- |:--- |  
      | EventHandler | Propriété pour la définition d’un handler d’événements sur une erreur pendant `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.onerror
      ```  
      
      `readyState` property  
      
      | Type | Description |  
      |:---- |:--- |  
      | Nombre | Représente l’état de l’opération asynchrone dans l’application Windows à l’aide de JavaScript.  Les valeurs sont `Started[0]` les suivantes : , `Completed[1]` , `Error[2]` .  |  
      
      ```javascript
      p = object.readyState
      ```  
      
      `result` property  
      
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
