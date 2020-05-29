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
# <span data-ttu-id="1bcc9-105">MSApp</span><span class="sxs-lookup"><span data-stu-id="1bcc9-105">MSApp</span></span>

<span data-ttu-id="1bcc9-106">L’objet MSApp et ses membres sont uniquement pris en charge pour les applications Windows en JavaScript (y compris les fonctionnalités d’accès PWAs aux fonctionnalités de l’API Windows).</span><span class="sxs-lookup"><span data-stu-id="1bcc9-106">The MSApp object and its members are supported only for Windows apps using JavaScript (including PWAs accessing Windows API features).</span></span> <span data-ttu-id="1bcc9-107">L’objet MSApp existe uniquement dans le contexte local d’un document HTML dans une application Windows chargée via le schéma d’URI MS-Appx. dans le cas contraire, l’objet n’existe pas (et par conséquent, aucune de ses méthodes et propriétés n’est disponible).</span><span class="sxs-lookup"><span data-stu-id="1bcc9-107">The MSApp object only exists in the local context of an HTML document in a Windows app loaded via the ms-appx URI scheme; otherwise, the object doesn't exist (and consequently, none of its methods and properties are available).</span></span>

<span data-ttu-id="1bcc9-108">Il fournit des fonctions d’assistance qui vous permettent de créer des objets [BLOB](https://developer.mozilla.org/docs/Web/API/Blob) et [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="1bcc9-108">It provides helper functions that enable you to create [Blob](https://developer.mozilla.org/docs/Web/API/Blob) and [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) objects.</span></span>

```javascript
var result = MSApp.method;
```

| | |
| :--- | :--- |
| [**<span data-ttu-id="1bcc9-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1bcc9-109">Methods</span></span>**](#msapp-methods) | <span data-ttu-id="1bcc9-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher, pageHandlesAllApplicationActivations](#istaskscheduledatpriorityorhigher), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp.](#terminateapp) [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations)</span><span class="sxs-lookup"><span data-stu-id="1bcc9-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).</span></span> |

| | |
| :--- | :--- |
| [**<span data-ttu-id="1bcc9-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="1bcc9-111">Constants</span></span>**](#msapp-constants) | <span data-ttu-id="1bcc9-112">[actuel](#current), [élevé](#high), [inactif](#idle), [normal](#normal).</span><span class="sxs-lookup"><span data-stu-id="1bcc9-112">[current](#current), [high](#high), [idle](#idle), [normal](#normal).</span></span>|

| | |
| :--- | :--- |
| [<span data-ttu-id="1bcc9-113">Interface **MSAppAsyncOperation**</span><span class="sxs-lookup"><span data-stu-id="1bcc9-113">**MSAppAsyncOperation** interface</span></span>](#msappasyncoperation) | [<span data-ttu-id="1bcc9-114">start</span><span class="sxs-lookup"><span data-stu-id="1bcc9-114">start</span></span>](#start) |

## <span data-ttu-id="1bcc9-115">Méthodes MSApp</span><span class="sxs-lookup"><span data-stu-id="1bcc9-115">MSApp Methods</span></span>

### <span data-ttu-id="1bcc9-116">clearTemporaryWebDataAsync</span><span class="sxs-lookup"><span data-stu-id="1bcc9-116">clearTemporaryWebDataAsync</span></span> 
<span data-ttu-id="1bcc9-117">Efface les données mises en cache et indexedDB pour l’application ou le [WebView](../../webview.md).</span><span class="sxs-lookup"><span data-stu-id="1bcc9-117">Clears cache and indexedDB data for the app or [WebView](../../webview.md).</span></span>

```javascript
var retval = MSApp.clearTemporaryWebDataAsync(#); 
```

#### <span data-ttu-id="1bcc9-118">Parameters</span><span class="sxs-lookup"><span data-stu-id="1bcc9-118">Parameters</span></span>
<span data-ttu-id="1bcc9-119">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-119">This method has no parameters.</span></span>

#### <span data-ttu-id="1bcc9-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1bcc9-120">Return value</span></span>
<span data-ttu-id="1bcc9-121">Nouveau[`IAsyncAction`](/uwp/api/windows.foundation.iasyncaction)</span><span class="sxs-lookup"><span data-stu-id="1bcc9-121">Type: [`IAsyncAction`](/uwp/api/windows.foundation.iasyncaction)</span></span>

<span data-ttu-id="1bcc9-122">Représente une action asynchrone.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-122">Represents an asynchronous action.</span></span>

### <span data-ttu-id="1bcc9-123">createBlobFromRandomAccessStream</span><span class="sxs-lookup"><span data-stu-id="1bcc9-123">createBlobFromRandomAccessStream</span></span>
<span data-ttu-id="1bcc9-124">Crée un objet [BLOB](https://developer.mozilla.org/docs/Web/API/Blob) à partir d’un [`IRandomAccessStream`](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) objet.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-124">Creates a [Blob](https://developer.mozilla.org/docs/Web/API/Blob) from an [`IRandomAccessStream`](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) object.</span></span> <span data-ttu-id="1bcc9-125">Cette méthode doit être utilisée pour gérer des `IRandomAccessStream` objets dans des applications afin de créer un objet basé sur W3C à partir du flux.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-125">This method should be used when dealing with `IRandomAccessStream` objects in apps in order to create a W3C based object from the stream.</span></span> <span data-ttu-id="1bcc9-126">Une fois l’objet BLOB créé, il peut être utilisé avec les API [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [URL](https://developer.mozilla.org/docs/Web/API/URL)et [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).</span><span class="sxs-lookup"><span data-stu-id="1bcc9-126">Once the blob is created, it can be used with the [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [URL APIs](https://developer.mozilla.org/docs/Web/API/URL), and [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).</span></span> 

```javascript
var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
```

#### <span data-ttu-id="1bcc9-127">Parameters</span><span class="sxs-lookup"><span data-stu-id="1bcc9-127">Parameters</span></span>

`type` <span data-ttu-id="1bcc9-128">complémentaire</span><span class="sxs-lookup"><span data-stu-id="1bcc9-128">[in]</span></span>

|<span data-ttu-id="1bcc9-129">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-129">Type</span></span> | <span data-ttu-id="1bcc9-130">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-130">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-131">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1bcc9-131">String</span></span> | <span data-ttu-id="1bcc9-132">Type de contenu des données.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-132">Content type of the data.</span></span> <span data-ttu-id="1bcc9-133">Cette chaîne doit être au format spécifié dans le jeton de type de média défini dans la section 3,7 de RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-133">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>

`stream` <span data-ttu-id="1bcc9-134">complémentaire</span><span class="sxs-lookup"><span data-stu-id="1bcc9-134">[in]</span></span>

|<span data-ttu-id="1bcc9-135">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-135">Type</span></span> | <span data-ttu-id="1bcc9-136">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-136">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-137">Indifférent</span><span class="sxs-lookup"><span data-stu-id="1bcc9-137">Any</span></span> | <span data-ttu-id="1bcc9-138">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) stocker dans l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-138">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) to be stored in the Blob.</span></span>

#### <span data-ttu-id="1bcc9-139">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1bcc9-139">Return value</span></span>
|<span data-ttu-id="1bcc9-140">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-140">Type</span></span> | <span data-ttu-id="1bcc9-141">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-141">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-142">Destiné</span><span class="sxs-lookup"><span data-stu-id="1bcc9-142">Blob</span></span> | <span data-ttu-id="1bcc9-143">Nouvel objet BLOB qui contient le flux.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-143">New blob object that contains the stream.</span></span>

#### <span data-ttu-id="1bcc9-144">Exceptions</span><span class="sxs-lookup"><span data-stu-id="1bcc9-144">Exceptions</span></span>
|<span data-ttu-id="1bcc9-145">Sauf</span><span class="sxs-lookup"><span data-stu-id="1bcc9-145">Exception</span></span> | <span data-ttu-id="1bcc9-146">Condition</span><span class="sxs-lookup"><span data-stu-id="1bcc9-146">Condition</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-147">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="1bcc9-147">TypeMismatchError</span></span> | <span data-ttu-id="1bcc9-148">Le type de nœud n’est pas compatible avec le type de paramètre attendu.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-148">The node type is incompatible with the expected parameter type.</span></span> <span data-ttu-id="1bcc9-149">TYPE_MISMATCH_ERR est retourné pour les versions antérieures à Internet Explorer 10.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-149">For versions earlier than Internet Explorer 10, TYPE_MISMATCH_ERR is returned.</span></span>

#### <span data-ttu-id="1bcc9-150">Remarques</span><span class="sxs-lookup"><span data-stu-id="1bcc9-150">Remarks</span></span>
<span data-ttu-id="1bcc9-151">Crée un objet blob à partir des types Windows Runtime via l’espace de noms MSApp sur l’objet Window.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-151">Creates a Blob from Windows Runtime types via the MSApp namespace on the window object.</span></span> <span data-ttu-id="1bcc9-152">Cette méthode crée un objet BLOB qui est essentiellement un wrapper léger sur l' [`RandomAccessStream`](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) objet qui lui est fourni.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-152">This method will create a blob that is essentially a light wrapper over the [`RandomAccessStream`](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) object provided to it.</span></span> <span data-ttu-id="1bcc9-153">L’objet BLOB possède la durée de vie du flux et le flux sera fermé lorsque l’objet blob est détruit.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-153">The blob owns the lifetime of this stream and the stream will be closed when the blob is destroyed.</span></span> 

#### <span data-ttu-id="1bcc9-154">Exemple</span><span class="sxs-lookup"><span data-stu-id="1bcc9-154">Example</span></span>

```javascript
var randomAccessStream = dataPackage.GetData("image/bmp");
var blob = window.MSApp.createBlobFromRandomAccessStream("image/bmp", randomAccessStream);
var url = window.URL.createObjectURL(blob, {oneTimeOnly:true});

document.getElementById("imagetag").src = url; 
```

### <span data-ttu-id="1bcc9-155">createDataPackage</span><span class="sxs-lookup"><span data-stu-id="1bcc9-155">createDataPackage</span></span>
<span data-ttu-id="1bcc9-156">Convertit la plage spécifiée de l’utilisateur ou de l’application en fragment HTML qui peut être partagé.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-156">Converts the user's or the application's specified range to an HTML fragment that can be shared.</span></span>

```javascript
var retVal = MSApp.createDataPackage(object); 
```

#### <span data-ttu-id="1bcc9-157">Parameters</span><span class="sxs-lookup"><span data-stu-id="1bcc9-157">Parameters</span></span>
`object` <span data-ttu-id="1bcc9-158">complémentaire</span><span class="sxs-lookup"><span data-stu-id="1bcc9-158">[in]</span></span>

|<span data-ttu-id="1bcc9-159">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-159">Type</span></span> | <span data-ttu-id="1bcc9-160">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-160">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-161">Indifférent</span><span class="sxs-lookup"><span data-stu-id="1bcc9-161">Any</span></span> | <span data-ttu-id="1bcc9-162">Ce type de plage peut être créé à partir d’un objet Selection, par exemple: `window.selection.getRangeAt(0)` , ou manuellement.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-162">This range can be created either from a selection object, for example: `window.selection.getRangeAt(0)`, or manually.</span></span>

#### <span data-ttu-id="1bcc9-163">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1bcc9-163">Return value</span></span>
|<span data-ttu-id="1bcc9-164">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-164">Type</span></span> | <span data-ttu-id="1bcc9-165">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-165">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-166">Indifférent</span><span class="sxs-lookup"><span data-stu-id="1bcc9-166">Any</span></span> | <span data-ttu-id="1bcc9-167">Contient le balisage HTML pour la plage spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-167">Contains the HTML markup for the specified range.</span></span>

#### <span data-ttu-id="1bcc9-168">Remarques</span><span class="sxs-lookup"><span data-stu-id="1bcc9-168">Remarks</span></span>
<span data-ttu-id="1bcc9-169">Cette méthode prend uniquement en charge la [plage DOM](https://developer.mozilla.org/docs/Web/API/Range)et non [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span><span class="sxs-lookup"><span data-stu-id="1bcc9-169">This method supports only [Document Object Model (DOM) Range](https://developer.mozilla.org/docs/Web/API/Range), not [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span></span> <span data-ttu-id="1bcc9-170">Le package de données retourné pour la plage spécifiée contient le balisage HTML au format Clipboard.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-170">The returned data package for the specified range contains HTML markup in clipboard format.</span></span>

<span data-ttu-id="1bcc9-171">Aucune propriété n’est disponible pour le package de données renvoyées.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-171">There are no available properties for the returned data package.</span></span>

### <span data-ttu-id="1bcc9-172">createDataPackageFromSelection</span><span class="sxs-lookup"><span data-stu-id="1bcc9-172">createDataPackageFromSelection</span></span> 
<span data-ttu-id="1bcc9-173">Convertit la sélection de l’utilisateur ou de l’application en fragment HTML qui peut être partagé.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-173">Converts the user's or the application's selection to an HTML fragment that can be shared.</span></span>

```javascript
var retVal = MSApp.createDataPackageFromSelection(); 
```

#### <span data-ttu-id="1bcc9-174">Parameters</span><span class="sxs-lookup"><span data-stu-id="1bcc9-174">Parameters</span></span>
<span data-ttu-id="1bcc9-175">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-175">This method has no parameters.</span></span>

#### <span data-ttu-id="1bcc9-176">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1bcc9-176">Return value</span></span>
|<span data-ttu-id="1bcc9-177">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-177">Type</span></span> | <span data-ttu-id="1bcc9-178">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-178">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-179">Indifférent</span><span class="sxs-lookup"><span data-stu-id="1bcc9-179">Any</span></span> | <span data-ttu-id="1bcc9-180">Contient le balisage HTML pour la plage spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-180">Contains the HTML markup for the specified range.</span></span>

#### <span data-ttu-id="1bcc9-181">Remarques</span><span class="sxs-lookup"><span data-stu-id="1bcc9-181">Remarks</span></span>
<span data-ttu-id="1bcc9-182">Le package de données retourné pour la sélection contient le balisage HTML au format Clipboard.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-182">The returned data package for the selection contains HTML markup in clipboard format.</span></span> <span data-ttu-id="1bcc9-183">S’il n’y a pas de sélection d’utilisateur n’importe où dans l’interface utilisateur de l’application, la fonction `createDataPackageFromSelection` renvoie la valeur null.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-183">If there is no user selection anywhere within the application's UI, the `createDataPackageFromSelection` returns null.</span></span>

<span data-ttu-id="1bcc9-184">Aucune propriété n’est disponible pour le package de données renvoyées.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-184">There are no available properties for the returned data package.</span></span>
 
### <span data-ttu-id="1bcc9-185">createFileFromStorageFile</span><span class="sxs-lookup"><span data-stu-id="1bcc9-185">createFileFromStorageFile</span></span> 
<span data-ttu-id="1bcc9-186">Convertit un objet [WinRT](/uwp/api/) [`StorageFile`](/uwp/api/windows.storage.storagefile) en objet W3C standard [`File`](https://developer.mozilla.org/docs/Web/API/File) .</span><span class="sxs-lookup"><span data-stu-id="1bcc9-186">Converts a [WinRT](/uwp/api/) [`StorageFile`](/uwp/api/windows.storage.storagefile) to a standard W3C [`File`](https://developer.mozilla.org/docs/Web/API/File) object.</span></span>

```javascript
var retVal = MSApp.createFileFromStorageFile(storageFile); 
```

#### <span data-ttu-id="1bcc9-187">Parameters</span><span class="sxs-lookup"><span data-stu-id="1bcc9-187">Parameters</span></span>
`storageFile` <span data-ttu-id="1bcc9-188">complémentaire</span><span class="sxs-lookup"><span data-stu-id="1bcc9-188">[in]</span></span>

|<span data-ttu-id="1bcc9-189">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-189">Type</span></span> | <span data-ttu-id="1bcc9-190">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-190">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-191">Indifférent</span><span class="sxs-lookup"><span data-stu-id="1bcc9-191">Any</span></span> | <span data-ttu-id="1bcc9-192">Contient le fichier de stockage.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-192">Contains the storage file.</span></span>

#### <span data-ttu-id="1bcc9-193">Exceptions</span><span class="sxs-lookup"><span data-stu-id="1bcc9-193">Exceptions</span></span>
|<span data-ttu-id="1bcc9-194">Sauf</span><span class="sxs-lookup"><span data-stu-id="1bcc9-194">Exception</span></span> | <span data-ttu-id="1bcc9-195">Condition</span><span class="sxs-lookup"><span data-stu-id="1bcc9-195">Condition</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-196">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="1bcc9-196">TypeMismatchError</span></span> | <span data-ttu-id="1bcc9-197">La référence de fichier W3C spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-197">The specified W3C file reference is invalid.</span></span> <span data-ttu-id="1bcc9-198">TYPE_MISMATCH_ERR est retourné pour les versions antérieures à Internet Explorer 10.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-198">For versions earlier than Internet Explorer 10, TYPE_MISMATCH_ERR is returned.</span></span>

### <span data-ttu-id="1bcc9-199">createStreamFromInputStream</span><span class="sxs-lookup"><span data-stu-id="1bcc9-199">createStreamFromInputStream</span></span>  

<span data-ttu-id="1bcc9-200">Crée un [`MSStream`](https://msdn.microsoft.com/library/hh772328) à partir de [`InputStream`](https://msdn.microsoft.com/library/hh772327) .</span><span class="sxs-lookup"><span data-stu-id="1bcc9-200">Creates an [`MSStream`](https://msdn.microsoft.com/library/hh772328) from an [`InputStream`](https://msdn.microsoft.com/library/hh772327).</span></span>  


```javascript
var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
```

#### <span data-ttu-id="1bcc9-201">Parameters</span><span class="sxs-lookup"><span data-stu-id="1bcc9-201">Parameters</span></span>
`type` <span data-ttu-id="1bcc9-202">complémentaire</span><span class="sxs-lookup"><span data-stu-id="1bcc9-202">[in]</span></span>

|<span data-ttu-id="1bcc9-203">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-203">Type</span></span> | <span data-ttu-id="1bcc9-204">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-204">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-205">DOMString</span><span class="sxs-lookup"><span data-stu-id="1bcc9-205">DOMString</span></span> | <span data-ttu-id="1bcc9-206">Type de contenu des données.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-206">Content type of the data.</span></span> <span data-ttu-id="1bcc9-207">Cette chaîne doit être au format spécifié dans le jeton de type de média défini dans la section 3,7 de RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-207">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span> <span data-ttu-id="1bcc9-208">(Pour plus d’outils,[voir types MIME,](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types) IE. text/plain, text/html, image/JPEG, image/png, audio/MPEG, audio/OGG, audio/\*, vidéo/MP4, etc.).</span><span class="sxs-lookup"><span data-stu-id="1bcc9-208">([See MIME types,](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types) ie. text/plain, text/html, image/jpeg, image/png, audio/mpeg, audio/ogg, audio/\*, video/mp4, etc.).</span></span> 

`inputStream` <span data-ttu-id="1bcc9-209">complémentaire</span><span class="sxs-lookup"><span data-stu-id="1bcc9-209">[in]</span></span>

|<span data-ttu-id="1bcc9-210">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-210">Type</span></span> | <span data-ttu-id="1bcc9-211">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-211">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-212">Indifférent</span><span class="sxs-lookup"><span data-stu-id="1bcc9-212">Any</span></span> | <span data-ttu-id="1bcc9-213">[`IInputStream`](/uwp/api/Windows.Storage.Streams.IInputStream)À stocker dans le `MSStream` .</span><span class="sxs-lookup"><span data-stu-id="1bcc9-213">The [`IInputStream`](/uwp/api/Windows.Storage.Streams.IInputStream) to be stored in the `MSStream`.</span></span>

#### <span data-ttu-id="1bcc9-214">Remarques</span><span class="sxs-lookup"><span data-stu-id="1bcc9-214">Remarks</span></span>
<span data-ttu-id="1bcc9-215">Cette méthode prend un type de contenu et la `IInputStream` référence.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-215">This method takes a content-type, and the `IInputStream` reference.</span></span> <span data-ttu-id="1bcc9-216">La méthode vérifie que la référence de flux transmise est une instance de type `IInputStream` et si ce n’est pas le cas, lève `DOMException TYPE_MISMATCH_ERR` .</span><span class="sxs-lookup"><span data-stu-id="1bcc9-216">The method then verifies that the stream reference passed in is an instance of type `IInputStream` and if not, throws `DOMException TYPE_MISMATCH_ERR`.</span></span> <span data-ttu-id="1bcc9-217">S’il n’y a aucune erreur, `createStreamFromInputStream` crée un `MSStream` (à partir de ses entrées).</span><span class="sxs-lookup"><span data-stu-id="1bcc9-217">If no error occurs, `createStreamFromInputStream` creates an `MSStream` (from its inputs).</span></span>

#### <span data-ttu-id="1bcc9-218">Exemple</span><span class="sxs-lookup"><span data-stu-id="1bcc9-218">Example</span></span>
<span data-ttu-id="1bcc9-219">Un `IInputStream` peut être utilisé pour créer un `MSStream` .</span><span class="sxs-lookup"><span data-stu-id="1bcc9-219">An `IInputStream` can be used to create an `MSStream`.</span></span> <span data-ttu-id="1bcc9-220">Comme `MSStreams` ces objets font l’objet d’une utilisation par nature, toutes les URL créées par `URL.createObjectURL` sont révoquées la première fois qu’il est résolu par l’élément image.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-220">As `MSStreams` are inherently one-time-use objects, all URLs created by `URL.createObjectURL` are revoked the first time it's resolved by the image element.</span></span> <span data-ttu-id="1bcc9-221">De plus, les demandes d’une deuxième URL sur cet objet après que le flux a été utilisé échoueront.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-221">Additionally, requests for a second URL on this object after the stream has been used will fail.</span></span>

```javascript
var inputStream = myInputStream; //get InputStream from socket API, etc.
var stream = MSApp.createStreamFromInputStream("image/bmp", inputstream);
document.getElementById("imagetag").src = URL.createObjectURL(stream); 
```

### <span data-ttu-id="1bcc9-222">execAsyncAtPriority</span><span class="sxs-lookup"><span data-stu-id="1bcc9-222">execAsyncAtPriority</span></span> 
<span data-ttu-id="1bcc9-223">Planifie l’exécution d’un rappel à un moment ultérieur en fonction de la priorité donnée.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-223">Schedules a callback to be executed at a later time according to the given priority.</span></span> 

```javascript
MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
```

#### <span data-ttu-id="1bcc9-224">Parameters</span><span class="sxs-lookup"><span data-stu-id="1bcc9-224">Parameters</span></span>
`asynchronousCallback` <span data-ttu-id="1bcc9-225">complémentaire</span><span class="sxs-lookup"><span data-stu-id="1bcc9-225">[in]</span></span>

|<span data-ttu-id="1bcc9-226">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-226">Type</span></span> | <span data-ttu-id="1bcc9-227">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-227">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-228">Fonction</span><span class="sxs-lookup"><span data-stu-id="1bcc9-228">Function</span></span> | <span data-ttu-id="1bcc9-229">Fonction callback qui s’exécute de manière asynchrone et est distribuée à la priorité de priorité spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-229">The callback function to run asynchronously, dispatched at the given priority priority.</span></span>

`priority` <span data-ttu-id="1bcc9-230">complémentaire</span><span class="sxs-lookup"><span data-stu-id="1bcc9-230">[in]</span></span>

|<span data-ttu-id="1bcc9-231">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-231">Type</span></span> | <span data-ttu-id="1bcc9-232">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-232">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-233">DOMString</span><span class="sxs-lookup"><span data-stu-id="1bcc9-233">DOMString</span></span> | <span data-ttu-id="1bcc9-234">Valeur de priorité contextuelle à laquelle le rappel asynchronousCallback est exécuté.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-234">The contextual priority value at which the asynchronousCallback callback is run.</span></span> <span data-ttu-id="1bcc9-235">Voir [constantes MSApp](#msapp-constants).</span><span class="sxs-lookup"><span data-stu-id="1bcc9-235">See [MSApp Constants](#msapp-constants).</span></span>

`args` <span data-ttu-id="1bcc9-236">complémentaire</span><span class="sxs-lookup"><span data-stu-id="1bcc9-236">[in]</span></span>

|<span data-ttu-id="1bcc9-237">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-237">Type</span></span> | <span data-ttu-id="1bcc9-238">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-238">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-239">Indifférent</span><span class="sxs-lookup"><span data-stu-id="1bcc9-239">Any</span></span> | <span data-ttu-id="1bcc9-240">Série d’arguments facultatives transmis à la fonction de rappel synchronousCallback (en tant que paramètres 1 et activé).</span><span class="sxs-lookup"><span data-stu-id="1bcc9-240">An optional series of arguments that are passed to the synchronousCallback callback function (as parameters 1 and on).</span></span>

#### <span data-ttu-id="1bcc9-241">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1bcc9-241">Return value</span></span>
<span data-ttu-id="1bcc9-242">Cette méthode ne renvoie pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-242">This method does not return a value.</span></span>

#### <span data-ttu-id="1bcc9-243">Remarques</span><span class="sxs-lookup"><span data-stu-id="1bcc9-243">Remarks</span></span>
<span data-ttu-id="1bcc9-244">La `asynchronousCallback` fonction de rappel fournie s’exécute de manière asynchrone plus tard.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-244">The provided `asynchronousCallback` callback function is executed asynchronously later.</span></span> `asynchronousCallback` <span data-ttu-id="1bcc9-245">sera distribué en fonction de la priorité fournie.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-245">will be dispatched according to the provided priority.</span></span> <span data-ttu-id="1bcc9-246">La priorité normale équivaut à la [`setImmediate`](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) méthode existante.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-246">Normal priority is equivalent to the existing [`setImmediate`](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) method.</span></span> <span data-ttu-id="1bcc9-247">Lorsque le rappel est exécuté, la priorité contextuelle actuelle est définie sur la valeur de paramètre de priorité fournie pour la durée de l’exécution du rappel.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-247">When the callback is run, the current contextual priority is set to the provided priority parameter value for the duration of the callback's execution.</span></span>

<span data-ttu-id="1bcc9-248">Le `asynchronousCallback` paramètre callback peut être n’importe quelle fonction.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-248">The `asynchronousCallback` callback parameter can be any function.</span></span> <span data-ttu-id="1bcc9-249">Si des arguments sont fournis après le `priority` paramètre, ils sont tous transmis à la fonction callback.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-249">If arguments are provided after the `priority` parameter, they will all be passed to the callback function.</span></span>

<span data-ttu-id="1bcc9-250">`execAtPriority`À la différence, tout objet renvoyé par la `asynchronousCallback` fonction de rappel est ignoré (et non renvoyé par le biais de `execAsyncAtPriority` ).</span><span class="sxs-lookup"><span data-stu-id="1bcc9-250">Unlike `execAtPriority`, any object returned by the `asynchronousCallback` callback function is ignored (and not returned via `execAsyncAtPriority`).</span></span>

### <span data-ttu-id="1bcc9-251">execAtPriority</span><span class="sxs-lookup"><span data-stu-id="1bcc9-251">execAtPriority</span></span> 
<span data-ttu-id="1bcc9-252">Exécute la fonction de rappel spécifiée dans la priorité contextuelle spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-252">Runs the specified callback function at the given contextual priority.</span></span>

```javascript
var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
```

#### <span data-ttu-id="1bcc9-253">Parameters</span><span class="sxs-lookup"><span data-stu-id="1bcc9-253">Parameters</span></span>
`synchronousCallback` <span data-ttu-id="1bcc9-254">complémentaire</span><span class="sxs-lookup"><span data-stu-id="1bcc9-254">[in]</span></span>

|<span data-ttu-id="1bcc9-255">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-255">Type</span></span> | <span data-ttu-id="1bcc9-256">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-256">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-257">Fonction</span><span class="sxs-lookup"><span data-stu-id="1bcc9-257">Function</span></span> | <span data-ttu-id="1bcc9-258">Fonction callback qui s’exécute de façon synchrone selon la priorité contextuelle spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-258">The callback function to run synchronously at the given priority contextual priority.</span></span>

`priority` <span data-ttu-id="1bcc9-259">complémentaire</span><span class="sxs-lookup"><span data-stu-id="1bcc9-259">[in]</span></span>

|<span data-ttu-id="1bcc9-260">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-260">Type</span></span> | <span data-ttu-id="1bcc9-261">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-261">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-262">DOMString</span><span class="sxs-lookup"><span data-stu-id="1bcc9-262">DOMString</span></span> | <span data-ttu-id="1bcc9-263">Valeur de priorité spécifiée à laquelle la valeur de priorité contextuelle actuelle sera définie lors de l’exécution de la `synchronousCallback` fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-263">The specified priority value to which the current contextual priority value will be set when running the `synchronousCallback` callback function.</span></span> <span data-ttu-id="1bcc9-264">Voir [constantes MSApp](#msapp-constants).</span><span class="sxs-lookup"><span data-stu-id="1bcc9-264">See [MSApp Constants](#msapp-constants).</span></span>

`args` <span data-ttu-id="1bcc9-265">complémentaire</span><span class="sxs-lookup"><span data-stu-id="1bcc9-265">[in]</span></span>

|<span data-ttu-id="1bcc9-266">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-266">Type</span></span> | <span data-ttu-id="1bcc9-267">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-267">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-268">Indifférent</span><span class="sxs-lookup"><span data-stu-id="1bcc9-268">Any</span></span> | <span data-ttu-id="1bcc9-269">Série d’arguments facultatives transmis à la fonction de `synchronousCallback` rappel (en tant que paramètres 1 et activés).</span><span class="sxs-lookup"><span data-stu-id="1bcc9-269">An optional series of arguments that are passed to the `synchronousCallback` callback function (as parameters 1 and on).</span></span>

#### <span data-ttu-id="1bcc9-270">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1bcc9-270">Return value</span></span>
|<span data-ttu-id="1bcc9-271">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-271">Type</span></span> | <span data-ttu-id="1bcc9-272">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-272">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-273">Indifférent</span><span class="sxs-lookup"><span data-stu-id="1bcc9-273">Any</span></span> | <span data-ttu-id="1bcc9-274">Renvoie la valeur de retour du `synchronousCallback` rappel (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="1bcc9-274">Returns the return value of the `synchronousCallback` callback (as applicable).</span></span>

#### <span data-ttu-id="1bcc9-275">Remarques</span><span class="sxs-lookup"><span data-stu-id="1bcc9-275">Remarks</span></span>
<span data-ttu-id="1bcc9-276">La `synchronousCallback` méthode de rappel fournie s’exécute de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-276">The provided `synchronousCallback` callback method is execute synchronously.</span></span> <span data-ttu-id="1bcc9-277">La priorité contextuelle actuelle est remplacée par la valeur de priorité fournie (fournie par l’argument Priority) pour la durée de la fonction de rappel fournie.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-277">The current contextual priority is changed to the provided priority value (given by the priority argument) for the duration of the provided callback function.</span></span> <span data-ttu-id="1bcc9-278">Après l’exécution de la fonction de rappel, Priority est retourné à la valeur précédente avant l' `execAtPriority` appel.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-278">Once the callback function finishes executing, priority is returned to the previous value prior to the `execAtPriority` call.</span></span> <span data-ttu-id="1bcc9-279">La valeur de retour de `execAtPriority` correspond à la valeur de retour de la méthode de rappel (telle qu’elle est fournie).</span><span class="sxs-lookup"><span data-stu-id="1bcc9-279">The return value from `execAtPriority` is the return value of the callback method (as provided).</span></span>
 
<span data-ttu-id="1bcc9-280">Le `synchronousCallback` paramètre callback peut être n’importe quelle fonction.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-280">The `synchronousCallback` callback parameter can be any function.</span></span> <span data-ttu-id="1bcc9-281">Si un argument est fourni après le paramètre Priority, il est transmis à la méthode de rappel fournie.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-281">If any arguments are provided after the priority parameter, they will be passed to the provided callback method.</span></span> <span data-ttu-id="1bcc9-282">Si le paramètre callback renvoie une valeur, cette valeur devient également la valeur de retour `execAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="1bcc9-282">If the callback parameter returns a value, this value becomes the return value for `execAtPriority` as well.</span></span>

#### <span data-ttu-id="1bcc9-283">Exemple</span><span class="sxs-lookup"><span data-stu-id="1bcc9-283">Example</span></span>

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

### <span data-ttu-id="1bcc9-284">getCurrentPriority</span><span class="sxs-lookup"><span data-stu-id="1bcc9-284">getCurrentPriority</span></span> 
<span data-ttu-id="1bcc9-285">Renvoie la priorité contextuelle actuelle.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-285">Returns the current contextual priority.</span></span>

```javascript
var retval = MSApp.getCurrentPriority();
```

#### <span data-ttu-id="1bcc9-286">Parameters</span><span class="sxs-lookup"><span data-stu-id="1bcc9-286">Parameters</span></span>
<span data-ttu-id="1bcc9-287">Aucune.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-287">None.</span></span> 

#### <span data-ttu-id="1bcc9-288">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1bcc9-288">Return value</span></span>
|<span data-ttu-id="1bcc9-289">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-289">Type</span></span> | <span data-ttu-id="1bcc9-290">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-290">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-291">DOMString</span><span class="sxs-lookup"><span data-stu-id="1bcc9-291">DOMString</span></span> | <span data-ttu-id="1bcc9-292">La valeur de retour est l’une des chaînes `MSApp.HIGH` , `MSApp.NORMAL` ou `MSApp.IDLE` .</span><span class="sxs-lookup"><span data-stu-id="1bcc9-292">The return value is one of the strings `MSApp.HIGH`, `MSApp.NORMAL`, or `MSApp.IDLE`.</span></span>

#### <span data-ttu-id="1bcc9-293">Remarques</span><span class="sxs-lookup"><span data-stu-id="1bcc9-293">Remarks</span></span>
<span data-ttu-id="1bcc9-294">Cette méthode renvoie la priorité contextuelle actuelle (voir [`MSApp Constants`](#msapp-constants) ), qui peut être modifiée via `execAtPriority` et `execAsyncAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="1bcc9-294">This method returns the current contextual priority (see [`MSApp Constants`](#msapp-constants)), which can be changed via `execAtPriority` and `execAsyncAtPriority`.</span></span>

#### <span data-ttu-id="1bcc9-295">Exemple</span><span class="sxs-lookup"><span data-stu-id="1bcc9-295">Example</span></span>

```javascript
if (MSApp.getCurrentPriority() === MSApp.IDLE) { 
  // YOUR CODE HERE
}
```

### <span data-ttu-id="1bcc9-296">getHtmlPrintDocumentSource</span><span class="sxs-lookup"><span data-stu-id="1bcc9-296">getHtmlPrintDocumentSource</span></span>  

<span data-ttu-id="1bcc9-297">API synchrone qui est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-297">Synchronous API that has been deprecated.</span></span> <span data-ttu-id="1bcc9-298">Pour Windows 10, voir `getHtmlPrintDocumentSourceAsync` .</span><span class="sxs-lookup"><span data-stu-id="1bcc9-298">For Windows 10, see `getHtmlPrintDocumentSourceAsync`.</span></span> <span data-ttu-id="1bcc9-299">Pour les applications Windows 8 et 8,1, consultez le site Web entrée pour [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span><span class="sxs-lookup"><span data-stu-id="1bcc9-299">For Windows 8 and 8.1 apps, see the MSDN entry for [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span></span>  

### <span data-ttu-id="1bcc9-300">getHtmlPrintDocumentSourceAsync</span><span class="sxs-lookup"><span data-stu-id="1bcc9-300">getHtmlPrintDocumentSourceAsync</span></span>
<span data-ttu-id="1bcc9-301">Renvoie le contenu source à imprimer.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-301">Returns the source content that is to be printed.</span></span>

#### <span data-ttu-id="1bcc9-302">Parameters</span><span class="sxs-lookup"><span data-stu-id="1bcc9-302">Parameters</span></span>
`htmlDoc` <span data-ttu-id="1bcc9-303">complémentaire</span><span class="sxs-lookup"><span data-stu-id="1bcc9-303">[in]</span></span>

|<span data-ttu-id="1bcc9-304">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-304">Type</span></span> | <span data-ttu-id="1bcc9-305">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-305">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-306">Document</span><span class="sxs-lookup"><span data-stu-id="1bcc9-306">Document</span></span> | <span data-ttu-id="1bcc9-307">Le document HTML à imprimer.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-307">The HTML document to be printed.</span></span> <span data-ttu-id="1bcc9-308">Il peut s’agir du document racine, du document dans un IFRAME, d’un fragment de document ou d’un document SVG.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-308">This can be the root document, the document in an iframe, a document fragment, or a SVG document.</span></span> <span data-ttu-id="1bcc9-309">Sachez que htmlDoc doit être un document et non un élément.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-309">Be aware that htmlDoc must be a document, not an element.</span></span>

#### <span data-ttu-id="1bcc9-310">Exemple1</span><span class="sxs-lookup"><span data-stu-id="1bcc9-310">Example 1</span></span>

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

#### <span data-ttu-id="1bcc9-311">Exemple2</span><span class="sxs-lookup"><span data-stu-id="1bcc9-311">Example 2</span></span>

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

### <span data-ttu-id="1bcc9-312">getViewId</span><span class="sxs-lookup"><span data-stu-id="1bcc9-312">getViewId</span></span> 
<span data-ttu-id="1bcc9-313">Prise en charge de plusieurs fenêtres.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-313">Support for multiple windows.</span></span> 

> [!NOTE] 
> <span data-ttu-id="1bcc9-314">Dans les applications UWP JavaScript de Win 8.1 prises en charge plusieurs fenêtres utilisant des API MSApp DOM qui sont désormais depricated.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-314">In Win8.1 JavaScript UWP apps supported multiple windows using MSApp DOM APIs which are now depricated.</span></span> <span data-ttu-id="1bcc9-315">Pour Windows 10, utilisez `window.open` , `window` et le nouveau `MSApp.getViewId` .</span><span class="sxs-lookup"><span data-stu-id="1bcc9-315">For Windows 10, use `window.open`, `window`, and the new `MSApp.getViewId`.</span></span>

| <span data-ttu-id="1bcc9-316">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-316">Description</span></span> |<span data-ttu-id="1bcc9-317">Windows 10</span><span class="sxs-lookup"><span data-stu-id="1bcc9-317">Windows 10</span></span> | <span data-ttu-id="1bcc9-318">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1bcc9-318">Windows 8.1</span></span> |  
|:---- |:---- |:--- |  
| <span data-ttu-id="1bcc9-319">Créer une fenêtre</span><span class="sxs-lookup"><span data-stu-id="1bcc9-319">Create new window</span></span> | [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) | [`MSApp.createNewView`](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
|<span data-ttu-id="1bcc9-320">Nouvel objet Window</span><span class="sxs-lookup"><span data-stu-id="1bcc9-320">New window object</span></span> | [`window`](https://developer.mozilla.org/docs/Web/API/Window) |[`MSAppView`](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  

```javascript
var retval = MSApp.getViewId(window); 
```

#### <span data-ttu-id="1bcc9-321">Parameters</span><span class="sxs-lookup"><span data-stu-id="1bcc9-321">Parameters</span></span>
`window`

|<span data-ttu-id="1bcc9-322">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-322">Type</span></span> | <span data-ttu-id="1bcc9-323">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-323">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-324">DOMString</span><span class="sxs-lookup"><span data-stu-id="1bcc9-324">DOMString</span></span> | <span data-ttu-id="1bcc9-325">Objet représentant une fenêtre contenant un document DOM.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-325">An object representing a window containing a DOM document.</span></span> | 

#### <span data-ttu-id="1bcc9-326">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1bcc9-326">Return value</span></span>

`viewId`

|<span data-ttu-id="1bcc9-327">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-327">Type</span></span> | <span data-ttu-id="1bcc9-328">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-328">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-329">Nombre</span><span class="sxs-lookup"><span data-stu-id="1bcc9-329">Number</span></span> | <span data-ttu-id="1bcc9-330">Peut être utilisé avec les diverses [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) API.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-330">Can be used with the various [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span> 

#### <span data-ttu-id="1bcc9-331">Remarques</span><span class="sxs-lookup"><span data-stu-id="1bcc9-331">Remarks</span></span>
<span data-ttu-id="1bcc9-332">Utiliser [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) et [`window`](https://developer.mozilla.org/docs/Web/API/Window) pour créer des fenêtres, mais pour interagir avec des API WinRT, ajoutez l' `MSApp.getViewId` API.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-332">Use [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) and [`window`](https://developer.mozilla.org/docs/Web/API/Window) for creating new windows, but then to interact with WinRT APIs, add the `MSApp.getViewId` API.</span></span> <span data-ttu-id="1bcc9-333">Il accepte un `window` objet en tant que paramètre et renvoie un `viewId` nombre qui peut être utilisé avec les diverses [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) API.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-333">It takes a `window` object as a parameter and returns a `viewId` number that can be used with the various [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span> 

##### <span data-ttu-id="1bcc9-334">Retardement de la visibilité</span><span class="sxs-lookup"><span data-stu-id="1bcc9-334">Delaying Visibility</span></span> 
<span data-ttu-id="1bcc9-335">Dans le cas d’un affichage complet, les vues sont masquées et le développeur `TryShowAsStandaloneAsync` doit afficher l’affichage une fois qu’il est entièrement préparé.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-335">Views in WinRT normally start hidden and the end developer uses something like `TryShowAsStandaloneAsync` to display the view once it is fully prepared.</span></span> <span data-ttu-id="1bcc9-336">Dans le monde Web, `window.open` affiche une fenêtre immédiatement et l’utilisateur final peut voir le contenu chargé et affiché.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-336">In the web world, `window.open` shows a window immediately and the end user can watch as content is loaded and rendered.</span></span> <span data-ttu-id="1bcc9-337">Pour que votre nouvelle Windows serve de vues dans WinRT et qu’elle ne soit pas affichée immédiatement, nous avons ajouté une `window.open` option.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-337">To have your new windows act like views in WinRT and not display immediately we have added a `window.open` option.</span></span> <span data-ttu-id="1bcc9-338">Exemple:</span><span class="sxs-lookup"><span data-stu-id="1bcc9-338">For example:</span></span>
`let newWindow = window.open("https://example.com", null, "msHideView=yes");`

##### <span data-ttu-id="1bcc9-339">Différences entre les fenêtres principales</span><span class="sxs-lookup"><span data-stu-id="1bcc9-339">Primary Window Differences</span></span>
<span data-ttu-id="1bcc9-340">La fenêtre principale ouverte par le système d’exploitation agit de la même manière que celle des fenêtres secondaires qui s’affichent:</span><span class="sxs-lookup"><span data-stu-id="1bcc9-340">The primary window that is initially opened by the OS acts differently than the secondary windows that it opens:</span></span> 

|<span data-ttu-id="1bcc9-341">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-341">Description</span></span> | <span data-ttu-id="1bcc9-342">Principal</span><span class="sxs-lookup"><span data-stu-id="1bcc9-342">Primary</span></span> | <span data-ttu-id="1bcc9-343">Secondaire</span><span class="sxs-lookup"><span data-stu-id="1bcc9-343">Secondary</span></span> |
|:---- |:--- |:--- |
|<span data-ttu-id="1bcc9-344">fenêtre. ouvrir</span><span class="sxs-lookup"><span data-stu-id="1bcc9-344">window.open</span></span> | <span data-ttu-id="1bcc9-345">Autorisée</span><span class="sxs-lookup"><span data-stu-id="1bcc9-345">Allowed</span></span> | <span data-ttu-id="1bcc9-346">Non autorisé</span><span class="sxs-lookup"><span data-stu-id="1bcc9-346">Disallowed</span></span> |
|<span data-ttu-id="1bcc9-347">Window. Close</span><span class="sxs-lookup"><span data-stu-id="1bcc9-347">window.close</span></span> | <span data-ttu-id="1bcc9-348">Fermer l’application</span><span class="sxs-lookup"><span data-stu-id="1bcc9-348">Close app</span></span> | <span data-ttu-id="1bcc9-349">Fermer la fenêtre</span><span class="sxs-lookup"><span data-stu-id="1bcc9-349">Close window</span></span> |
| <span data-ttu-id="1bcc9-350">Restrictions de navigation</span><span class="sxs-lookup"><span data-stu-id="1bcc9-350">Navigation restrictions</span></span> | <span data-ttu-id="1bcc9-351">FORME règles ACUR uniquement</span><span class="sxs-lookup"><span data-stu-id="1bcc9-351">ACUR only</span></span> | <span data-ttu-id="1bcc9-352">Aucune restriction</span><span class="sxs-lookup"><span data-stu-id="1bcc9-352">No restrictions</span></span> |

<span data-ttu-id="1bcc9-353">Il est possible que l’ouverture d’un autre Windows ne puisse changer dans le futur en fonction de votre [avis](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).</span><span class="sxs-lookup"><span data-stu-id="1bcc9-353">The restriction to not allow secondary windows to open could change in the future depending on [feedback](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).</span></span>

##### <span data-ttu-id="1bcc9-354">Restrictions de communication d’origine identiques</span><span class="sxs-lookup"><span data-stu-id="1bcc9-354">Same Origin Communication Restrictions</span></span> 
<span data-ttu-id="1bcc9-355">La prise en charge d’un problème technique unique empêche une prise en charge de la prise en charge de la synchronisation, des appels entre les scripts.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-355">There is a difficult technical issue preventing proper support for synchronous, same-origin, cross-window, script calls.</span></span> <span data-ttu-id="1bcc9-356">Lorsque vous ouvrez une fenêtre qui est identique à l’origine, le script d’une fenêtre est autorisé à appeler directement les fonctions dans l’autre fenêtre, et certains de ces appels échouent.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-356">When you open a window that is same origin, script in one window is allowed to directly call functions in the other window, and some of these calls will fail.</span></span> `postMessage` <span data-ttu-id="1bcc9-357">les appels fonctionnent parfaitement et il est recommandé de procéder comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-357">calls work just fine and is the recommended way to do things if possible.</span></span> <span data-ttu-id="1bcc9-358">Le travail pour améliorer ce problème est en cours.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-358">Work to improve this issue is in progress.</span></span>


### <span data-ttu-id="1bcc9-359">isTaskScheduledAtPriorityOrHigher</span><span class="sxs-lookup"><span data-stu-id="1bcc9-359">isTaskScheduledAtPriorityOrHigher</span></span> 
<span data-ttu-id="1bcc9-360">Renvoie une donnée de type booléen indiquant s’il existe une tâche en attente au niveau de priorité donné ou une valeur supérieure.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-360">Returns a Boolean value indicating whether there is pending work at the given priority level or higher.</span></span>

```javascript
var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
```

#### <span data-ttu-id="1bcc9-361">Parameters</span><span class="sxs-lookup"><span data-stu-id="1bcc9-361">Parameters</span></span>
`priority` <span data-ttu-id="1bcc9-362">complémentaire</span><span class="sxs-lookup"><span data-stu-id="1bcc9-362">[in]</span></span>

|<span data-ttu-id="1bcc9-363">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-363">Type</span></span> | <span data-ttu-id="1bcc9-364">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-364">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-365">DOMString</span><span class="sxs-lookup"><span data-stu-id="1bcc9-365">DOMString</span></span> | <span data-ttu-id="1bcc9-366">Valeur de priorité (voir [constantes MSApp](#msapp-constants)) spécifiant le niveau de priorité et au-dessus pour rechercher tout Work en attente.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-366">A priority value (see [MSApp Constants](#msapp-constants)) specifying the priority level and above to query for any outstanding queued work.</span></span>

#### <span data-ttu-id="1bcc9-367">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1bcc9-367">Return value</span></span>
|<span data-ttu-id="1bcc9-368">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-368">Type</span></span> | <span data-ttu-id="1bcc9-369">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-369">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-370">Booléen</span><span class="sxs-lookup"><span data-stu-id="1bcc9-370">Boolean</span></span> | <span data-ttu-id="1bcc9-371">Renvoie `true` s’il existe un fonctionnement en file d’attente au niveau de priorité spécifié, `false` sinon.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-371">Returns `true` if there is any queued work at the specified priority level or above, `false` otherwise.</span></span>

#### <span data-ttu-id="1bcc9-372">Remarques</span><span class="sxs-lookup"><span data-stu-id="1bcc9-372">Remarks</span></span>
<span data-ttu-id="1bcc9-373">Cette `isTaskScheduledAtPriorityOrHigher` méthode fournit un moyen pour le code JavaScript de déterminer s’il existe des tâches en attente aux différents niveaux de priorité (ou au-dessus), de manière à ce que le code JavaScript de l’appel puisse décider de produire une plus grande priorité.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-373">The `isTaskScheduledAtPriorityOrHigher` method provides a means for JavaScript code to determine if there is pending work at the various priority levels (or above) with the intent that the calling JavaScript code can then decide to yield to higher priority work.</span></span>

#### <span data-ttu-id="1bcc9-374">Exemple</span><span class="sxs-lookup"><span data-stu-id="1bcc9-374">Example</span></span>

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

### <span data-ttu-id="1bcc9-375">pageHandlesAllApplicationActivations</span><span class="sxs-lookup"><span data-stu-id="1bcc9-375">pageHandlesAllApplicationActivations</span></span>
<span data-ttu-id="1bcc9-376">Permet d’éviter une actualisation du chemin de démarrage (rechargement de la page) avant chaque événement d’activation (IE, en cliquant sur une notification ou sur une vignette épinglée).</span><span class="sxs-lookup"><span data-stu-id="1bcc9-376">Used to avoid a refresh of the start path (page reload) before every activate event (ie. clicking a notification or a pinned tile).</span></span> 

#### <span data-ttu-id="1bcc9-377">Parameters</span><span class="sxs-lookup"><span data-stu-id="1bcc9-377">Parameters</span></span>

|<span data-ttu-id="1bcc9-378">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-378">Type</span></span> | <span data-ttu-id="1bcc9-379">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-379">Description</span></span> |
|:---- |:--- |
<span data-ttu-id="1bcc9-380">Booléen</span><span class="sxs-lookup"><span data-stu-id="1bcc9-380">Boolean</span></span> | <span data-ttu-id="1bcc9-381">Utilisez `MSApp.pageHandlesAllApplicationActivations(true)` cette méthode pour toujours éviter d’actualiser la trajectoire de début (rechargement de la page) et de passer directement au déclenchement de l' `WebUIApplication` événement Activated.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-381">Use `MSApp.pageHandlesAllApplicationActivations(true)` to always skip refreshing the start path (page reload) and instead jump straight to firing the `WebUIApplication` activated event.</span></span> <span data-ttu-id="1bcc9-382">Nécessite que toutes les pages gèrent les événements d’activation séparément.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-382">Requires that all pages handle activation events separately.</span></span> <span data-ttu-id="1bcc9-383">En définissant cette méthode `true` , en cliquant sur un événement Activated (par exemple, un notificaiton) ne déclenche pas la recharge, une application essentielle pour les applications sur une page unique veut éviter les recharges de pages.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-383">By defining this method as `true`, clicking an activated event (like a notificaiton) will not trigger the reload, an essential for single-page apps wishing to avoid page reloads.</span></span>

#### <span data-ttu-id="1bcc9-384">Exemple</span><span class="sxs-lookup"><span data-stu-id="1bcc9-384">Example</span></span> 

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

### <span data-ttu-id="1bcc9-385">suppressSubdownloadCredentialPrompts</span><span class="sxs-lookup"><span data-stu-id="1bcc9-385">suppressSubdownloadCredentialPrompts</span></span> 
<span data-ttu-id="1bcc9-386">Détermine si une application supprime les invites d’authentification possibles lors du téléchargement de ressources.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-386">Controls whether an app suppresses possible authentication prompts during the download of resources.</span></span>

```javascript
MSApp.suppressSubdownloadCredentialPrompts(suppress); 
```

#### <span data-ttu-id="1bcc9-387">Parameters</span><span class="sxs-lookup"><span data-stu-id="1bcc9-387">Parameters</span></span>
`suppress` <span data-ttu-id="1bcc9-388">complémentaire</span><span class="sxs-lookup"><span data-stu-id="1bcc9-388">[in]</span></span>

|<span data-ttu-id="1bcc9-389">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-389">Type</span></span> | <span data-ttu-id="1bcc9-390">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-390">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-391">Booléen</span><span class="sxs-lookup"><span data-stu-id="1bcc9-391">Boolean</span></span> | <span data-ttu-id="1bcc9-392">La valeur true supprime les invites d’authentification potentielles.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-392">A value of true suppresses potential authentication prompts.</span></span> <span data-ttu-id="1bcc9-393">La valeur false ne supprime pas les invites d’authentification potentielles de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-393">A value of false does not suppress any potential authentication prompts from the user.</span></span>

#### <span data-ttu-id="1bcc9-394">Valeur Returan</span><span class="sxs-lookup"><span data-stu-id="1bcc9-394">Returan value</span></span>
<span data-ttu-id="1bcc9-395">Aucune.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-395">None.</span></span>

#### <span data-ttu-id="1bcc9-396">Remarques</span><span class="sxs-lookup"><span data-stu-id="1bcc9-396">Remarks</span></span>
<span data-ttu-id="1bcc9-397">La `suppressSubdownloadCredentialPrompts` méthode contrôle si une application supprime les invites d’authentification potentielles lors du téléchargement de ressources.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-397">The `suppressSubdownloadCredentialPrompts` method controls whether an app suppresses potential authentication prompts during the download of resources.</span></span> <span data-ttu-id="1bcc9-398">Le comportement par défaut consiste à ne pas supprimer les invites d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-398">The default behavior is to not suppress credential prompts.</span></span>

`suppressSubdownloadCredentialPrompts` <span data-ttu-id="1bcc9-399">est destiné à être utilisé par des applications susceptibles de charger un nombre excessif de ressources qui nécessitent une authentification, par exemple une application de messagerie (qui peut contenir un bulletin d’informations contenant un nombre d’images nécessitant une authentification).</span><span class="sxs-lookup"><span data-stu-id="1bcc9-399">is intended for use by apps which may load an excessive number of resources that require authentication, such as a mail app (which could contain a newsletter containing a number of images where each image requires authentication).</span></span>

<span data-ttu-id="1bcc9-400">Lorsque vous supprimez des invites d’informations d’identification, les boîtes de dialogue d’authentification aux serveurs ne s’afficheront pas lors de l’accès aux ressources qui nécessitent une authentification et la ressource ne sera pas téléchargée.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-400">When suppressing credential prompts, dialogs for authenticating to servers will not be shown when accessing resources that require authentication, and the resource will not be downloaded.</span></span> <span data-ttu-id="1bcc9-401">Notez que `suppressSubdownloadCredentialPrompts` l’authentification proxy ou les boîtes de dialogue de demande de certification du client n’ont pas d’impact sur les autres invites possibles, comme l’authentification du proxy ou les boîtes de dialogue de demande de certification</span><span class="sxs-lookup"><span data-stu-id="1bcc9-401">Note that `suppressSubdownloadCredentialPrompts` does not impact other possible prompts such as proxy authentication or client certification request dialogs, nor does it impact XHR.</span></span>

<span data-ttu-id="1bcc9-402">Sachez que cela a un `suppressSubdownloadCredentialPrompts` impact sur tout le contenu de l’application, y compris le contenu hébergé dans l' `webview` élément.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-402">Be aware that `suppressSubdownloadCredentialPrompts` impacts all content in the application, including content hosted in the `webview` element.</span></span>
 
<span data-ttu-id="1bcc9-403">**Important:**  Les décisions d’instructions d’identification sont mises en cache.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-403">**Important:**  Credential prompt decisions are cached.</span></span> <span data-ttu-id="1bcc9-404">Par conséquent, si vous supprimez des invites d’informations d’identification, celles-ci peuvent être prises en compte immédiatement, permettant ainsi aux invites d’informations d’identification d’être supprimées.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-404">Therefore, while suppressing credential prompts will take effect immediately, allowing credential prompts after suppressing them may need a reload of the document to take effect.</span></span>

#### <span data-ttu-id="1bcc9-405">Exemple</span><span class="sxs-lookup"><span data-stu-id="1bcc9-405">Example</span></span>

```javascript
/ Set to true to suppress potenial credential prompts:
MSApp.suppressSubdownloadCredentialPrompts(true); 
// Now one can load content or navigate iframe/webview to some other site.
```

### <span data-ttu-id="1bcc9-406">terminateApp</span><span class="sxs-lookup"><span data-stu-id="1bcc9-406">terminateApp</span></span>
<span data-ttu-id="1bcc9-407">Arrête l’application actuelle et génère un rapport d’échec.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-407">Terminates the current application and generates a failure report.</span></span> 

```javascript
MSApp.terminateApp(error); 
```

#### <span data-ttu-id="1bcc9-408">Parameters</span><span class="sxs-lookup"><span data-stu-id="1bcc9-408">Parameters</span></span>
`error` <span data-ttu-id="1bcc9-409">complémentaire</span><span class="sxs-lookup"><span data-stu-id="1bcc9-409">[in]</span></span>

<span data-ttu-id="1bcc9-410">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-410">Type</span></span> | <span data-ttu-id="1bcc9-411">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-411">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-412">Erreur</span><span class="sxs-lookup"><span data-stu-id="1bcc9-412">Error</span></span> | <span data-ttu-id="1bcc9-413">Un `Error` objet que vous pouvez utiliser pour décrire l’erreur à l’origine de l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-413">An `Error` object that you can use to describe the error that triggered the termination.</span></span> <span data-ttu-id="1bcc9-414">L' `Error` objet doit contenir les propriétés Number, description et Stack; un rapport d’échec n’est pas généré si l’objet ne contient pas ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-414">The `Error` object must contain the number, description, and stack properties; a failure report won't be generated if the object doesn't contain these properties.</span></span>

#### <span data-ttu-id="1bcc9-415">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1bcc9-415">Return value</span></span>
<span data-ttu-id="1bcc9-416">Aucune.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-416">None.</span></span>

#### <span data-ttu-id="1bcc9-417">Remarques</span><span class="sxs-lookup"><span data-stu-id="1bcc9-417">Remarks</span></span>
<span data-ttu-id="1bcc9-418">Si le problème signalé par `terminateApp` devient l’un des 5 premiers problèmes de votre application, il apparaît sur la page qualité de l’application.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-418">If the issue reported by `terminateApp` becomes one of your app's top 5 issues, it will show up on the app's Quality page.</span></span>

#### <span data-ttu-id="1bcc9-419">Exemple</span><span class="sxs-lookup"><span data-stu-id="1bcc9-419">Example</span></span>
<span data-ttu-id="1bcc9-420">Cet exemple appelle `terminateApp` quand une exception est rencontrée.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-420">This example calls `terminateApp` when an exception is encountered.</span></span> <span data-ttu-id="1bcc9-421">Il utilise l' `Error` objet fourni lors de la capture d’une exception.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-421">It uses the `Error` object provided when you catch an exception.</span></span> 

```javascript
try {  
        var obj2 = null;  
        obj2.val = 5;  
    }  
    catch(e) {  
        window.MSApp.terminateApp(e);  
    }  
```

### <span data-ttu-id="1bcc9-422">Constantes MSApp</span><span class="sxs-lookup"><span data-stu-id="1bcc9-422">MSApp Constants</span></span>
<span data-ttu-id="1bcc9-423">Valeurs de priorité autorisées associées à `execAsyncAtPriority` , `execAtPriority` , `getCurrentPriority` et `isTaskScheduldAtPriorityOrHigher` .</span><span class="sxs-lookup"><span data-stu-id="1bcc9-423">Allowed priority values associated with `execAsyncAtPriority`, `execAtPriority`, `getCurrentPriority`, and `isTaskScheduldAtPriorityOrHigher`.</span></span>

#### <span data-ttu-id="1bcc9-424">Actuel</span><span class="sxs-lookup"><span data-stu-id="1bcc9-424">Current</span></span>
`current`

|<span data-ttu-id="1bcc9-425">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-425">Type</span></span> | <span data-ttu-id="1bcc9-426">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-426">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-427">DOMString</span><span class="sxs-lookup"><span data-stu-id="1bcc9-427">DOMString</span></span> | <span data-ttu-id="1bcc9-428">Lorsque `current` est utilisée avec la méthode appropriée (voir aussi section), la méthode utilise la priorité contextuelle actuelle lors de l’exécution de l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-428">When `current` is used with the appropriate method (See also section), the method will use the current contextual priority when executing the requested operation.</span></span>

#### <span data-ttu-id="1bcc9-429">High</span><span class="sxs-lookup"><span data-stu-id="1bcc9-429">High</span></span>
`high`

|<span data-ttu-id="1bcc9-430">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-430">Type</span></span> | <span data-ttu-id="1bcc9-431">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-431">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-432">DOMString</span><span class="sxs-lookup"><span data-stu-id="1bcc9-432">DOMString</span></span> | <span data-ttu-id="1bcc9-433">Lorsque `high` est utilisé avec la méthode appropriée (voir aussi section), la méthode utilise une priorité supérieure à la valeur normale lors de l’exécution de l’opération demandée et distribue l’opération avant tout fonctionnement de priorité normale existant.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-433">When `high` is used with the appropriate method (See also section), the method will use higher than normal priority when executing the requested operation and will be dispatch the operation before any existing normal priority work.</span></span>

#### <span data-ttu-id="1bcc9-434">Inactif</span><span class="sxs-lookup"><span data-stu-id="1bcc9-434">Idle</span></span>
`idle`

|<span data-ttu-id="1bcc9-435">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-435">Type</span></span> | <span data-ttu-id="1bcc9-436">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-436">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-437">DOMString</span><span class="sxs-lookup"><span data-stu-id="1bcc9-437">DOMString</span></span> | <span data-ttu-id="1bcc9-438">Lorsque `ideal` est utilisé avec la méthode appropriée (voir aussi section), la méthode utilise une priorité inférieure à la valeur normale lors de l’exécution de l’opération demandée et sera répartie de l’opération après tout fonctionnement prioritaire normal.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-438">When `ideal` is used with the appropriate method (See also section), the method will use lower than normal priority when executing the requested operation and will be dispatch the operation after any existing normal priority work.</span></span>

#### <span data-ttu-id="1bcc9-439">Normal</span><span class="sxs-lookup"><span data-stu-id="1bcc9-439">Normal</span></span>
`normal`

|<span data-ttu-id="1bcc9-440">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-440">Type</span></span> | <span data-ttu-id="1bcc9-441">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-441">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-442">DOMString</span><span class="sxs-lookup"><span data-stu-id="1bcc9-442">DOMString</span></span> | <span data-ttu-id="1bcc9-443">Lorsque `normal` est utilisé avec la méthode appropriée (voir aussi section), la méthode utilise la priorité actuelle normale lors de l’exécution de l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-443">When `normal` is used with the appropriate method (See also section), the method will use the normal existing priority when executing the requested operation.</span></span>

#### <span data-ttu-id="1bcc9-444">Exemple</span><span class="sxs-lookup"><span data-stu-id="1bcc9-444">Example</span></span>

```javascript
if (window.MSApp.CURRENT) {
  document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
}
```

#### <span data-ttu-id="1bcc9-445">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1bcc9-445">Requirements</span></span>
|<span data-ttu-id="1bcc9-446">MIDL</span><span class="sxs-lookup"><span data-stu-id="1bcc9-446">IDL</span></span> | <span data-ttu-id="1bcc9-447">Mshtml. idl</span><span class="sxs-lookup"><span data-stu-id="1bcc9-447">Mshtml.idl</span></span> |
|:---- |:--- |

## <span data-ttu-id="1bcc9-448">MSAppAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="1bcc9-448">MSAppAsyncOperation</span></span>

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```

### <span data-ttu-id="1bcc9-449">start</span><span class="sxs-lookup"><span data-stu-id="1bcc9-449">start</span></span>
<span data-ttu-id="1bcc9-450">Démarre `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="1bcc9-450">Starts the `MSAppAsyncOperation`.</span></span>

```javascript
var retval = MSAppAsyncOperation.start();
```

#### <span data-ttu-id="1bcc9-451">Parameters</span><span class="sxs-lookup"><span data-stu-id="1bcc9-451">Parameters</span></span>
<span data-ttu-id="1bcc9-452">Aucune.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-452">None.</span></span>

#### <span data-ttu-id="1bcc9-453">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1bcc9-453">Return value</span></span>
<span data-ttu-id="1bcc9-454">Aucune.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-454">None.</span></span>

#### <span data-ttu-id="1bcc9-455">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1bcc9-455">Properties</span></span>
`error` <span data-ttu-id="1bcc9-456">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1bcc9-456">property</span></span>

|<span data-ttu-id="1bcc9-457">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-457">Type</span></span> | <span data-ttu-id="1bcc9-458">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-458">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-459">DOMError</span><span class="sxs-lookup"><span data-stu-id="1bcc9-459">DOMError</span></span> | <span data-ttu-id="1bcc9-460">Représente une erreur dans `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="1bcc9-460">Represents an error in `MSAppAsyncOperation`.</span></span>

```javascript
p = object.error
```

`oncomplete` <span data-ttu-id="1bcc9-461">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1bcc9-461">property</span></span>

|<span data-ttu-id="1bcc9-462">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-462">Type</span></span> | <span data-ttu-id="1bcc9-463">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-463">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-464">EventHandler</span><span class="sxs-lookup"><span data-stu-id="1bcc9-464">EventHandler</span></span> | <span data-ttu-id="1bcc9-465">Propriété permettant de définir un gestionnaire d’événements à l’achèvement de `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="1bcc9-465">Property for setting an event handler on completion of `MSAppAsyncOperation`.</span></span>

```javascript
p = object.oncomplete
```

`onerror` <span data-ttu-id="1bcc9-466">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1bcc9-466">property</span></span>

|<span data-ttu-id="1bcc9-467">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-467">Type</span></span> | <span data-ttu-id="1bcc9-468">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-468">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-469">EventHandler</span><span class="sxs-lookup"><span data-stu-id="1bcc9-469">EventHandler</span></span> | <span data-ttu-id="1bcc9-470">Propriété permettant de définir un gestionnaire d’événements sur une erreur au cours de l’appel `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="1bcc9-470">Property for setting an event handler upon an error during `MSAppAsyncOperation`.</span></span>

```javascript
p = object.onerror
```

`readyState` <span data-ttu-id="1bcc9-471">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1bcc9-471">property</span></span>

|<span data-ttu-id="1bcc9-472">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-472">Type</span></span> | <span data-ttu-id="1bcc9-473">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-473">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-474">Nombre</span><span class="sxs-lookup"><span data-stu-id="1bcc9-474">Number</span></span> | <span data-ttu-id="1bcc9-475">Représente l’état de l’opération asynchrone dans l’application Windows en JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1bcc9-475">Represents the state of the asynchronous operation within the Windows app using JavaScript.</span></span> <span data-ttu-id="1bcc9-476">Les valeurs incluent: Started [0], Completed [1], erreur [2].</span><span class="sxs-lookup"><span data-stu-id="1bcc9-476">Values include: Started[0], Completed[1], Error[2].</span></span>

```javascript
p = object.readyState
```

`result` <span data-ttu-id="1bcc9-477">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1bcc9-477">property</span></span>

|<span data-ttu-id="1bcc9-478">Type</span><span class="sxs-lookup"><span data-stu-id="1bcc9-478">Type</span></span> | <span data-ttu-id="1bcc9-479">Description</span><span class="sxs-lookup"><span data-stu-id="1bcc9-479">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="1bcc9-480">Indifférent</span><span class="sxs-lookup"><span data-stu-id="1bcc9-480">Any</span></span> |<span data-ttu-id="1bcc9-481">Représente le résultat de `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="1bcc9-481">Represents the result of `MSAppAsyncOperation`.</span></span>

```javascript
p = object.result
```
