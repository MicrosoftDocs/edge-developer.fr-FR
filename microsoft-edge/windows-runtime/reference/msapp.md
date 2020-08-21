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
# <span data-ttu-id="9507b-105">MSApp</span><span class="sxs-lookup"><span data-stu-id="9507b-105">MSApp</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="9507b-106">L’objet MSApp et ses membres sont uniquement pris en charge pour les applications Windows en JavaScript \ (y compris les PWAs d’accès aux fonctionnalités de l’API Windows).</span><span class="sxs-lookup"><span data-stu-id="9507b-106">The MSApp object and its members are supported only for Windows apps using JavaScript \(including PWAs accessing Windows API features\).</span></span>  <span data-ttu-id="9507b-107">L’objet MSApp existe uniquement dans le contexte local d’un document HTML dans une application Windows chargée via le schéma d’URI MS-Appx. dans le cas contraire, l’objet n’existe pas (et par conséquent, aucune de ses méthodes et propriétés n’est disponible).</span><span class="sxs-lookup"><span data-stu-id="9507b-107">The MSApp object only exists in the local context of an HTML document in a Windows app loaded via the ms-appx URI scheme; otherwise, the object doesn't exist (and consequently, none of its methods and properties are available).</span></span>  

<span data-ttu-id="9507b-108">Il fournit des fonctions d’assistance qui vous permettent de créer des objets [BLOB](https://developer.mozilla.org/docs/Web/API/Blob) et [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="9507b-108">It provides helper functions that enable you to create [Blob](https://developer.mozilla.org/docs/Web/API/Blob) and [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) objects.</span></span>  

```javascript
var result = MSApp.method;
```  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="9507b-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9507b-109">Methods</span></span>](#msapp-methods)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="9507b-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher, pageHandlesAllApplicationActivations](#istaskscheduledatpriorityorhigher), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp.](#terminateapp) [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations)</span><span class="sxs-lookup"><span data-stu-id="9507b-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="9507b-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="9507b-111">Constants</span></span>](#msapp-constants)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="9507b-112">[actuel](#current), [élevé](#high), [inactif](#idle), [normal](#normal).</span><span class="sxs-lookup"><span data-stu-id="9507b-112">[current](#current), [high](#high), [idle](#idle), [normal](#normal).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="9507b-113">Interface MSAppAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="9507b-113">MSAppAsyncOperation interface</span></span>](#msappasyncoperation)  
   :::column-end:::
   :::column span="2":::
      [<span data-ttu-id="9507b-114">start</span><span class="sxs-lookup"><span data-stu-id="9507b-114">start</span></span>](#start)  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="9507b-115">Méthodes MSApp</span><span class="sxs-lookup"><span data-stu-id="9507b-115">MSApp methods</span></span>  

### <span data-ttu-id="9507b-116">clearTemporaryWebDataAsync</span><span class="sxs-lookup"><span data-stu-id="9507b-116">clearTemporaryWebDataAsync</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="9507b-117">Efface les données mises en cache et indexedDB pour l’application ou le [WebView](../../webview.md).</span><span class="sxs-lookup"><span data-stu-id="9507b-117">Clears cache and indexedDB data for the app or [WebView](../../webview.md).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.clearTemporaryWebDataAsync(#); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-118">Parameters</span><span class="sxs-lookup"><span data-stu-id="9507b-118">Parameters</span></span>**  
      
      <span data-ttu-id="9507b-119">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="9507b-119">This method has no parameters.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9507b-120">Return value</span></span>**  
      
      <span data-ttu-id="9507b-121">Type: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)</span><span class="sxs-lookup"><span data-stu-id="9507b-121">Type: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)</span></span>  
      
      <span data-ttu-id="9507b-122">Représente une action asynchrone.</span><span class="sxs-lookup"><span data-stu-id="9507b-122">Represents an asynchronous action.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-123">Exceptions</span><span class="sxs-lookup"><span data-stu-id="9507b-123">Exceptions</span></span>**  
      
      <span data-ttu-id="9507b-124">Aucune.</span><span class="sxs-lookup"><span data-stu-id="9507b-124">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="9507b-125">Remarks</span></span>**  
      
      <span data-ttu-id="9507b-126">Aucune.</span><span class="sxs-lookup"><span data-stu-id="9507b-126">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="9507b-127">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="9507b-128">createBlobFromRandomAccessStream</span><span class="sxs-lookup"><span data-stu-id="9507b-128">createBlobFromRandomAccessStream</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="9507b-129">Crée un objet [BLOB](https://developer.mozilla.org/docs/Web/API/Blob) à partir d’un objet [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) .</span><span class="sxs-lookup"><span data-stu-id="9507b-129">Creates a [Blob](https://developer.mozilla.org/docs/Web/API/Blob) from an [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) object.</span></span>  <span data-ttu-id="9507b-130">Cette méthode doit être utilisée pour gérer des `IRandomAccessStream` objets dans des applications afin de créer un objet basé sur W3C à partir du flux.</span><span class="sxs-lookup"><span data-stu-id="9507b-130">This method should be used when dealing with `IRandomAccessStream` objects in apps in order to create a W3C based object from the stream.</span></span>  <span data-ttu-id="9507b-131">Une fois l’objet BLOB créé, il peut être utilisé avec les API [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [URL](https://developer.mozilla.org/docs/Web/API/URL)et [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).</span><span class="sxs-lookup"><span data-stu-id="9507b-131">Once the blob is created, it can be used with the [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [URL APIs](https://developer.mozilla.org/docs/Web/API/URL), and [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-132">Parameters</span><span class="sxs-lookup"><span data-stu-id="9507b-132">Parameters</span></span>**  
      
      `type` <span data-ttu-id="9507b-133">complémentaire</span><span class="sxs-lookup"><span data-stu-id="9507b-133">[in]</span></span>  
      
      | <span data-ttu-id="9507b-134">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-134">Type</span></span> | <span data-ttu-id="9507b-135">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-135">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-136">Chaîne</span><span class="sxs-lookup"><span data-stu-id="9507b-136">String</span></span> | <span data-ttu-id="9507b-137">Type de contenu des données.</span><span class="sxs-lookup"><span data-stu-id="9507b-137">Content type of the data.</span></span>  <span data-ttu-id="9507b-138">Cette chaîne doit être au format spécifié dans le jeton de type de média défini dans la section 3,7 de RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="9507b-138">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>  |  
      
      `stream` <span data-ttu-id="9507b-139">complémentaire</span><span class="sxs-lookup"><span data-stu-id="9507b-139">[in]</span></span>  
      
      | <span data-ttu-id="9507b-140">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-140">Type</span></span> | <span data-ttu-id="9507b-141">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-141">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-142">Indifférent</span><span class="sxs-lookup"><span data-stu-id="9507b-142">Any</span></span> | <span data-ttu-id="9507b-143">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) stocker dans l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="9507b-143">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) to be stored in the Blob.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-144">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9507b-144">Return value</span></span>**  
      
      | <span data-ttu-id="9507b-145">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-145">Type</span></span> | <span data-ttu-id="9507b-146">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-146">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-147">Destiné</span><span class="sxs-lookup"><span data-stu-id="9507b-147">Blob</span></span> | <span data-ttu-id="9507b-148">Nouvel objet BLOB qui contient le flux.</span><span class="sxs-lookup"><span data-stu-id="9507b-148">New blob object that contains the stream.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-149">Exceptions</span><span class="sxs-lookup"><span data-stu-id="9507b-149">Exceptions</span></span>**  
      
      | <span data-ttu-id="9507b-150">Sauf</span><span class="sxs-lookup"><span data-stu-id="9507b-150">Exception</span></span> | <span data-ttu-id="9507b-151">Condition</span><span class="sxs-lookup"><span data-stu-id="9507b-151">Condition</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-152">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="9507b-152">TypeMismatchError</span></span> | <span data-ttu-id="9507b-153">Le type de nœud n’est pas compatible avec le type de paramètre attendu.</span><span class="sxs-lookup"><span data-stu-id="9507b-153">The node type is incompatible with the expected parameter type.</span></span>  <span data-ttu-id="9507b-154">TYPE_MISMATCH_ERR est retourné pour les versions antérieures à Internet Explorer 10.</span><span class="sxs-lookup"><span data-stu-id="9507b-154">For versions earlier than Internet Explorer 10, TYPE_MISMATCH_ERR is returned.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-155">Remarques</span><span class="sxs-lookup"><span data-stu-id="9507b-155">Remarks</span></span>**  
      
      <span data-ttu-id="9507b-156">Crée un objet blob à partir des types Windows Runtime via l’espace de noms MSApp sur l’objet Window.</span><span class="sxs-lookup"><span data-stu-id="9507b-156">Creates a Blob from Windows Runtime types via the MSApp namespace on the window object.</span></span>  <span data-ttu-id="9507b-157">Cette méthode crée un objet BLOB qui est essentiellement un wrapper léger par le biais de l’objet [RandomAccessStream](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) qui lui est fourni.</span><span class="sxs-lookup"><span data-stu-id="9507b-157">This method will create a blob that is essentially a light wrapper over the [RandomAccessStream](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) object provided to it.</span></span>  <span data-ttu-id="9507b-158">L’objet BLOB possède la durée de vie du flux et le flux sera fermé lorsque l’objet blob est détruit.</span><span class="sxs-lookup"><span data-stu-id="9507b-158">The blob owns the lifetime of this stream and the stream will be closed when the blob is destroyed.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-159">Exemple</span><span class="sxs-lookup"><span data-stu-id="9507b-159">Example</span></span>**  
      
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

### <span data-ttu-id="9507b-160">createDataPackage</span><span class="sxs-lookup"><span data-stu-id="9507b-160">createDataPackage</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="9507b-161">Convertit la plage spécifiée de l’utilisateur ou de l’application en fragment HTML qui peut être partagé.</span><span class="sxs-lookup"><span data-stu-id="9507b-161">Converts the user's or the application's specified range to an HTML fragment that can be shared.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackage(object); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-162">Parameters</span><span class="sxs-lookup"><span data-stu-id="9507b-162">Parameters</span></span>**  
      
      `object` <span data-ttu-id="9507b-163">complémentaire</span><span class="sxs-lookup"><span data-stu-id="9507b-163">[in]</span></span>  
      
      | <span data-ttu-id="9507b-164">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-164">Type</span></span> | <span data-ttu-id="9507b-165">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-165">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-166">Indifférent</span><span class="sxs-lookup"><span data-stu-id="9507b-166">Any</span></span> | <span data-ttu-id="9507b-167">Ce type de plage peut être créé à partir d’un objet Selection, par exemple: `window.selection.getRangeAt(0)` , ou manuellement.</span><span class="sxs-lookup"><span data-stu-id="9507b-167">This range can be created either from a selection object, for example: `window.selection.getRangeAt(0)`, or manually.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-168">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9507b-168">Return value</span></span>**  
      
      | <span data-ttu-id="9507b-169">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-169">Type</span></span> | <span data-ttu-id="9507b-170">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-170">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-171">Indifférent</span><span class="sxs-lookup"><span data-stu-id="9507b-171">Any</span></span> | <span data-ttu-id="9507b-172">Contient le balisage HTML pour la plage spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9507b-172">Contains the HTML markup for the specified range.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-173">Exceptions</span><span class="sxs-lookup"><span data-stu-id="9507b-173">Exceptions</span></span>**  
      
      <span data-ttu-id="9507b-174">Aucune.</span><span class="sxs-lookup"><span data-stu-id="9507b-174">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-175">Remarques</span><span class="sxs-lookup"><span data-stu-id="9507b-175">Remarks</span></span>**  
      
      <span data-ttu-id="9507b-176">Cette méthode prend uniquement en charge la [plage DOM](https://developer.mozilla.org/docs/Web/API/Range)et non [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span><span class="sxs-lookup"><span data-stu-id="9507b-176">This method supports only [Document Object Model (DOM) Range](https://developer.mozilla.org/docs/Web/API/Range), not [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span></span>  <span data-ttu-id="9507b-177">Le package de données retourné pour la plage spécifiée contient le balisage HTML au format Clipboard.</span><span class="sxs-lookup"><span data-stu-id="9507b-177">The returned data package for the specified range contains HTML markup in clipboard format.</span></span>  
      
      <span data-ttu-id="9507b-178">Aucune propriété n’est disponible pour le package de données renvoyées.</span><span class="sxs-lookup"><span data-stu-id="9507b-178">There are no available properties for the returned data package.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-179">Exemple</span><span class="sxs-lookup"><span data-stu-id="9507b-179">Example</span></span>**  
      
      <span data-ttu-id="9507b-180">Aucune.</span><span class="sxs-lookup"><span data-stu-id="9507b-180">None.</span></span>  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="9507b-181">createDataPackageFromSelection</span><span class="sxs-lookup"><span data-stu-id="9507b-181">createDataPackageFromSelection</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="9507b-182">Convertit la sélection de l’utilisateur ou de l’application en fragment HTML qui peut être partagé.</span><span class="sxs-lookup"><span data-stu-id="9507b-182">Converts the user's or the application's selection to an HTML fragment that can be shared.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackageFromSelection(); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-183">Parameters</span><span class="sxs-lookup"><span data-stu-id="9507b-183">Parameters</span></span>**  
      
      <span data-ttu-id="9507b-184">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="9507b-184">This method has no parameters.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-185">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9507b-185">Return value</span></span>**  
      
      | <span data-ttu-id="9507b-186">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-186">Type</span></span> | <span data-ttu-id="9507b-187">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-187">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-188">Indifférent</span><span class="sxs-lookup"><span data-stu-id="9507b-188">Any</span></span> | <span data-ttu-id="9507b-189">Contient le balisage HTML pour la plage spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9507b-189">Contains the HTML markup for the specified range.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-190">Exceptions</span><span class="sxs-lookup"><span data-stu-id="9507b-190">Exceptions</span></span>**  
      
      <span data-ttu-id="9507b-191">Aucune.</span><span class="sxs-lookup"><span data-stu-id="9507b-191">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-192">Remarques</span><span class="sxs-lookup"><span data-stu-id="9507b-192">Remarks</span></span>**  
      
      <span data-ttu-id="9507b-193">Le package de données retourné pour la sélection contient le balisage HTML au format Clipboard.</span><span class="sxs-lookup"><span data-stu-id="9507b-193">The returned data package for the selection contains HTML markup in clipboard format.</span></span>  <span data-ttu-id="9507b-194">S’il n’y a aucune sélection d’utilisateur n’importe où dans l’interface utilisateur de l’application, le `createDataPackageFromSelection` retour `null` .</span><span class="sxs-lookup"><span data-stu-id="9507b-194">If there is no user selection anywhere within the application's UI, the `createDataPackageFromSelection` returns `null`.</span></span>  
      
      <span data-ttu-id="9507b-195">Aucune propriété n’est disponible pour le package de données renvoyées.</span><span class="sxs-lookup"><span data-stu-id="9507b-195">There are no available properties for the returned data package.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-196">Exemple</span><span class="sxs-lookup"><span data-stu-id="9507b-196">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
 
### <span data-ttu-id="9507b-197">createFileFromStorageFile</span><span class="sxs-lookup"><span data-stu-id="9507b-197">createFileFromStorageFile</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="9507b-198">Convertit un [StorageFile](/uwp/api/windows.storage.storagefile) [WinRT](/uwp/api/) en un objet de [fichier](https://developer.mozilla.org/docs/Web/API/File) W3C standard.</span><span class="sxs-lookup"><span data-stu-id="9507b-198">Converts a [WinRT](/uwp/api/) [StorageFile](/uwp/api/windows.storage.storagefile) to a standard W3C [File](https://developer.mozilla.org/docs/Web/API/File) object.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createFileFromStorageFile(storageFile); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-199">Parameters</span><span class="sxs-lookup"><span data-stu-id="9507b-199">Parameters</span></span>**  
      
      `storageFile` <span data-ttu-id="9507b-200">complémentaire</span><span class="sxs-lookup"><span data-stu-id="9507b-200">[in]</span></span>
      
      | <span data-ttu-id="9507b-201">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-201">Type</span></span> | <span data-ttu-id="9507b-202">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-202">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-203">Indifférent</span><span class="sxs-lookup"><span data-stu-id="9507b-203">Any</span></span> | <span data-ttu-id="9507b-204">Contient le fichier de stockage.</span><span class="sxs-lookup"><span data-stu-id="9507b-204">Contains the storage file.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-205">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9507b-205">Return value</span></span>**
      
      <span data-ttu-id="9507b-206">None</span><span class="sxs-lookup"><span data-stu-id="9507b-206">None</span></span>    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-207">Exceptions</span><span class="sxs-lookup"><span data-stu-id="9507b-207">Exceptions</span></span>**  
      
      | <span data-ttu-id="9507b-208">Sauf</span><span class="sxs-lookup"><span data-stu-id="9507b-208">Exception</span></span> | <span data-ttu-id="9507b-209">Condition</span><span class="sxs-lookup"><span data-stu-id="9507b-209">Condition</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-210">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="9507b-210">TypeMismatchError</span></span> | <span data-ttu-id="9507b-211">La référence de fichier W3C spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="9507b-211">The specified W3C file reference is invalid.</span></span>  <span data-ttu-id="9507b-212">Pour les versions antérieures à Internet Explorer 10, `TYPE_MISMATCH_ERR` est retourné.</span><span class="sxs-lookup"><span data-stu-id="9507b-212">For versions earlier than Internet Explorer 10, `TYPE_MISMATCH_ERR` is returned.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-213">Remarques</span><span class="sxs-lookup"><span data-stu-id="9507b-213">Remarks</span></span>**  
      
      <span data-ttu-id="9507b-214">Aucune.</span><span class="sxs-lookup"><span data-stu-id="9507b-214">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-215">Exemple</span><span class="sxs-lookup"><span data-stu-id="9507b-215">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="9507b-216">createStreamFromInputStream</span><span class="sxs-lookup"><span data-stu-id="9507b-216">createStreamFromInputStream</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="9507b-217">Crée un [MSStream](https://msdn.microsoft.com/library/hh772328) à partir d’un [InputStream](https://msdn.microsoft.com/library/hh772327).</span><span class="sxs-lookup"><span data-stu-id="9507b-217">Creates an [MSStream](https://msdn.microsoft.com/library/hh772328) from an [InputStream](https://msdn.microsoft.com/library/hh772327).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-218">Parameters</span><span class="sxs-lookup"><span data-stu-id="9507b-218">Parameters</span></span>**  
      
      `type` <span data-ttu-id="9507b-219">complémentaire</span><span class="sxs-lookup"><span data-stu-id="9507b-219">[in]</span></span>
      
      | <span data-ttu-id="9507b-220">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-220">Type</span></span> | <span data-ttu-id="9507b-221">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-221">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-222">DOMString</span><span class="sxs-lookup"><span data-stu-id="9507b-222">DOMString</span></span> | <span data-ttu-id="9507b-223">Type de contenu des données.</span><span class="sxs-lookup"><span data-stu-id="9507b-223">Content type of the data.</span></span>  <span data-ttu-id="9507b-224">Cette chaîne doit être au format spécifié dans le jeton de type de média défini dans la section 3,7 de RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="9507b-224">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>  <span data-ttu-id="9507b-225">\ ([Voir types MIME] (comme https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) `text/plain` ,,, `text/html` , `image/jpeg` `image/png` `audio/mpeg` , `audio/ogg` , `audio/*` , `video/mp4` et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="9507b-225">\([See MIME types,](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) such as `text/plain`, `text/html`, `image/jpeg`, `image/png`, `audio/mpeg`, `audio/ogg`, `audio/*`, `video/mp4`, and so on\).</span></span>  
      
      `inputStream` <span data-ttu-id="9507b-226">complémentaire</span><span class="sxs-lookup"><span data-stu-id="9507b-226">[in]</span></span>
      
      | <span data-ttu-id="9507b-227">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-227">Type</span></span> | <span data-ttu-id="9507b-228">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-228">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-229">Indifférent</span><span class="sxs-lookup"><span data-stu-id="9507b-229">Any</span></span> | <span data-ttu-id="9507b-230">Le [IInputStream](/uwp/api/Windows.Storage.Streams.IInputStream) que vous voulez stocker dans le `MSStream` .</span><span class="sxs-lookup"><span data-stu-id="9507b-230">The [IInputStream](/uwp/api/Windows.Storage.Streams.IInputStream) to be stored in the `MSStream`.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-231">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9507b-231">Return value</span></span>**
      
      <span data-ttu-id="9507b-232">Aucune.</span><span class="sxs-lookup"><span data-stu-id="9507b-232">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-233">Exceptions</span><span class="sxs-lookup"><span data-stu-id="9507b-233">Exceptions</span></span>**  
      
      <span data-ttu-id="9507b-234">Aucune.</span><span class="sxs-lookup"><span data-stu-id="9507b-234">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-235">Remarques</span><span class="sxs-lookup"><span data-stu-id="9507b-235">Remarks</span></span>**  
      
      <span data-ttu-id="9507b-236">Cette méthode prend un type de contenu et la `IInputStream` référence.</span><span class="sxs-lookup"><span data-stu-id="9507b-236">This method takes a content-type, and the `IInputStream` reference.</span></span>  <span data-ttu-id="9507b-237">La méthode vérifie que la référence de flux transmise est une instance de type `IInputStream` et si ce n’est pas le cas, lève `DOMException TYPE_MISMATCH_ERR` .</span><span class="sxs-lookup"><span data-stu-id="9507b-237">The method then verifies that the stream reference passed in is an instance of type `IInputStream` and if not, throws `DOMException TYPE_MISMATCH_ERR`.</span></span>  <span data-ttu-id="9507b-238">S’il n’y a aucune erreur, `createStreamFromInputStream` crée un `MSStream` \ (à partir de ses entrées \).</span><span class="sxs-lookup"><span data-stu-id="9507b-238">If no error occurs, `createStreamFromInputStream` creates an `MSStream` \(from its inputs\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-239">Exemple</span><span class="sxs-lookup"><span data-stu-id="9507b-239">Example</span></span>**  
      
      <span data-ttu-id="9507b-240">Un `IInputStream` peut être utilisé pour créer un `MSStream` .</span><span class="sxs-lookup"><span data-stu-id="9507b-240">An `IInputStream` can be used to create an `MSStream`.</span></span>  <span data-ttu-id="9507b-241">Comme `MSStreams` ces objets font l’objet d’une utilisation par nature, toutes les URL créées par `URL.createObjectURL` sont révoquées la première fois qu’il est résolu par l’élément image.</span><span class="sxs-lookup"><span data-stu-id="9507b-241">As `MSStreams` are inherently one-time-use objects, all URLs created by `URL.createObjectURL` are revoked the first time it's resolved by the image element.</span></span>  <span data-ttu-id="9507b-242">De plus, les demandes d’une deuxième URL sur cet objet après que le flux a été utilisé échoueront.</span><span class="sxs-lookup"><span data-stu-id="9507b-242">Additionally, requests for a second URL on this object after the stream has been used will fail.</span></span>  
      
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

### <span data-ttu-id="9507b-243">execAsyncAtPriority</span><span class="sxs-lookup"><span data-stu-id="9507b-243">execAsyncAtPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="9507b-244">Planifie l’exécution d’un rappel à un moment ultérieur en fonction de la priorité donnée.</span><span class="sxs-lookup"><span data-stu-id="9507b-244">Schedules a callback to be executed at a later time according to the given priority.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-245">Parameters</span><span class="sxs-lookup"><span data-stu-id="9507b-245">Parameters</span></span>**  
      
      `asynchronousCallback` <span data-ttu-id="9507b-246">complémentaire</span><span class="sxs-lookup"><span data-stu-id="9507b-246">[in]</span></span>
      
      | <span data-ttu-id="9507b-247">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-247">Type</span></span> | <span data-ttu-id="9507b-248">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-248">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-249">Fonction</span><span class="sxs-lookup"><span data-stu-id="9507b-249">Function</span></span> | <span data-ttu-id="9507b-250">Fonction callback qui s’exécute de manière asynchrone et est distribuée à la priorité de priorité spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9507b-250">The callback function to run asynchronously, dispatched at the given priority priority.</span></span>  |  
      
      `priority` <span data-ttu-id="9507b-251">complémentaire</span><span class="sxs-lookup"><span data-stu-id="9507b-251">[in]</span></span>
      
      | <span data-ttu-id="9507b-252">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-252">Type</span></span> | <span data-ttu-id="9507b-253">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-253">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-254">DOMString</span><span class="sxs-lookup"><span data-stu-id="9507b-254">DOMString</span></span> | <span data-ttu-id="9507b-255">Valeur de priorité contextuelle à laquelle le rappel asynchronousCallback est exécuté.</span><span class="sxs-lookup"><span data-stu-id="9507b-255">The contextual priority value at which the asynchronousCallback callback is run.</span></span>  <span data-ttu-id="9507b-256">Voir [constantes MSApp](#msapp-constants).</span><span class="sxs-lookup"><span data-stu-id="9507b-256">See [MSApp Constants](#msapp-constants).</span></span>  |  
      
      `args` <span data-ttu-id="9507b-257">complémentaire</span><span class="sxs-lookup"><span data-stu-id="9507b-257">[in]</span></span>
      
      | <span data-ttu-id="9507b-258">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-258">Type</span></span> | <span data-ttu-id="9507b-259">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-259">Description</span></span> |  
      |:---- |:--- |   
      | <span data-ttu-id="9507b-260">Indifférent</span><span class="sxs-lookup"><span data-stu-id="9507b-260">Any</span></span> | <span data-ttu-id="9507b-261">Série d’arguments facultatives transmis à la fonction de rappel synchronousCallback \ (en tant que paramètres 1 et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="9507b-261">An optional series of arguments that are passed to the synchronousCallback callback function \(as parameters 1 and so on\).</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-262">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9507b-262">Return value</span></span>**  
      
      <span data-ttu-id="9507b-263">Cette méthode ne renvoie pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9507b-263">This method does not return a value.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-264">Exceptions</span><span class="sxs-lookup"><span data-stu-id="9507b-264">Exceptions</span></span>**  
      
      <span data-ttu-id="9507b-265">Aucune.</span><span class="sxs-lookup"><span data-stu-id="9507b-265">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-266">Remarques</span><span class="sxs-lookup"><span data-stu-id="9507b-266">Remarks</span></span>**  
      
      <span data-ttu-id="9507b-267">La `asynchronousCallback` fonction de rappel fournie s’exécute de manière asynchrone plus tard.</span><span class="sxs-lookup"><span data-stu-id="9507b-267">The provided `asynchronousCallback` callback function is executed asynchronously later.</span></span>  `asynchronousCallback` <span data-ttu-id="9507b-268">sera distribué en fonction de la priorité fournie.</span><span class="sxs-lookup"><span data-stu-id="9507b-268">will be dispatched according to the provided priority.</span></span>  <span data-ttu-id="9507b-269">La priorité normale équivaut à la méthode [setImmediate](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) existante.</span><span class="sxs-lookup"><span data-stu-id="9507b-269">Normal priority is equivalent to the existing [setImmediate](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) method.</span></span>  <span data-ttu-id="9507b-270">Lorsque le rappel est exécuté, la priorité contextuelle actuelle est définie sur la valeur de paramètre de priorité fournie pour la durée de l’exécution du rappel.</span><span class="sxs-lookup"><span data-stu-id="9507b-270">When the callback is run, the current contextual priority is set to the provided priority parameter value for the duration of the callback's execution.</span></span>  
      
      <span data-ttu-id="9507b-271">Le `asynchronousCallback` paramètre callback peut être n’importe quelle fonction.</span><span class="sxs-lookup"><span data-stu-id="9507b-271">The `asynchronousCallback` callback parameter can be any function.</span></span>  <span data-ttu-id="9507b-272">Si des arguments sont fournis après le `priority` paramètre, ils sont tous transmis à la fonction callback.</span><span class="sxs-lookup"><span data-stu-id="9507b-272">If arguments are provided after the `priority` parameter, they will all be passed to the callback function.</span></span>  
      
      <span data-ttu-id="9507b-273">`execAtPriority`À la différence, tout objet renvoyé par la `asynchronousCallback` fonction de rappel est ignoré et n’est pas renvoyé via `execAsyncAtPriority` \.</span><span class="sxs-lookup"><span data-stu-id="9507b-273">Unlike `execAtPriority`, any object returned by the `asynchronousCallback` callback function is ignored \(and not returned via `execAsyncAtPriority`\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-274">Exemple</span><span class="sxs-lookup"><span data-stu-id="9507b-274">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="9507b-275">execAtPriority</span><span class="sxs-lookup"><span data-stu-id="9507b-275">execAtPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="9507b-276">Exécute la fonction de rappel spécifiée dans la priorité contextuelle spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9507b-276">Runs the specified callback function at the given contextual priority.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-277">Parameters</span><span class="sxs-lookup"><span data-stu-id="9507b-277">Parameters</span></span>**  
      
      `synchronousCallback` <span data-ttu-id="9507b-278">complémentaire</span><span class="sxs-lookup"><span data-stu-id="9507b-278">[in]</span></span>  
      
      | <span data-ttu-id="9507b-279">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-279">Type</span></span> | <span data-ttu-id="9507b-280">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-280">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-281">Fonction</span><span class="sxs-lookup"><span data-stu-id="9507b-281">Function</span></span> | <span data-ttu-id="9507b-282">Fonction callback qui s’exécute de façon synchrone selon la priorité contextuelle spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9507b-282">The callback function to run synchronously at the given priority contextual priority.</span></span>  |  
      
      `priority` <span data-ttu-id="9507b-283">complémentaire</span><span class="sxs-lookup"><span data-stu-id="9507b-283">[in]</span></span>  
      
      | <span data-ttu-id="9507b-284">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-284">Type</span></span> | <span data-ttu-id="9507b-285">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-285">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-286">DOMString</span><span class="sxs-lookup"><span data-stu-id="9507b-286">DOMString</span></span> | <span data-ttu-id="9507b-287">Valeur de priorité spécifiée à laquelle la valeur de priorité contextuelle actuelle sera définie lors de l’exécution de la `synchronousCallback` fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="9507b-287">The specified priority value to which the current contextual priority value will be set when running the `synchronousCallback` callback function.</span></span>  <span data-ttu-id="9507b-288">Voir [constantes MSApp](#msapp-constants).</span><span class="sxs-lookup"><span data-stu-id="9507b-288">See [MSApp Constants](#msapp-constants).</span></span>  |  
      
      `args` <span data-ttu-id="9507b-289">complémentaire</span><span class="sxs-lookup"><span data-stu-id="9507b-289">[in]</span></span>  
      
      | <span data-ttu-id="9507b-290">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-290">Type</span></span> | <span data-ttu-id="9507b-291">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-291">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-292">Indifférent</span><span class="sxs-lookup"><span data-stu-id="9507b-292">Any</span></span> | <span data-ttu-id="9507b-293">Série facultative d’arguments transmis à la `synchronousCallback` fonction de rappel \ (en tant que paramètres 1 et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="9507b-293">An optional series of arguments that are passed to the `synchronousCallback` callback function \(as parameters 1 and so on\).</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-294">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9507b-294">Return value</span></span>**  
      
      | <span data-ttu-id="9507b-295">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-295">Type</span></span> | <span data-ttu-id="9507b-296">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-296">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-297">Indifférent</span><span class="sxs-lookup"><span data-stu-id="9507b-297">Any</span></span> | <span data-ttu-id="9507b-298">Renvoie la valeur de retour du `synchronousCallback` rappel \ (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="9507b-298">Returns the return value of the `synchronousCallback` callback \(as applicable\).</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-299">Exceptions</span><span class="sxs-lookup"><span data-stu-id="9507b-299">Exceptions</span></span>**  
      
      <span data-ttu-id="9507b-300">Aucune.</span><span class="sxs-lookup"><span data-stu-id="9507b-300">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-301">Remarques</span><span class="sxs-lookup"><span data-stu-id="9507b-301">Remarks</span></span>**  
      
      <span data-ttu-id="9507b-302">La `synchronousCallback` méthode de rappel fournie s’exécute de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="9507b-302">The provided `synchronousCallback` callback method is execute synchronously.</span></span>  <span data-ttu-id="9507b-303">La priorité contextuelle actuelle est remplacée par la valeur de priorité fournie (fournie par l’argument Priority) pour la durée de la fonction de rappel fournie.</span><span class="sxs-lookup"><span data-stu-id="9507b-303">The current contextual priority is changed to the provided priority value (given by the priority argument) for the duration of the provided callback function.</span></span>  <span data-ttu-id="9507b-304">Après l’exécution de la fonction de rappel, Priority est retourné à la valeur précédente avant l' `execAtPriority` appel.</span><span class="sxs-lookup"><span data-stu-id="9507b-304">Once the callback function finishes executing, priority is returned to the previous value prior to the `execAtPriority` call.</span></span>  <span data-ttu-id="9507b-305">La valeur de retour de `execAtPriority` correspond à la valeur de retour de la méthode de rappel \ (fournie \).</span><span class="sxs-lookup"><span data-stu-id="9507b-305">The return value from `execAtPriority` is the return value of the callback method \(as provided\).</span></span>  
      
      <span data-ttu-id="9507b-306">Le `synchronousCallback` paramètre callback peut être n’importe quelle fonction.</span><span class="sxs-lookup"><span data-stu-id="9507b-306">The `synchronousCallback` callback parameter can be any function.</span></span>  <span data-ttu-id="9507b-307">Si un argument est fourni après le paramètre Priority, il est transmis à la méthode de rappel fournie.</span><span class="sxs-lookup"><span data-stu-id="9507b-307">If any arguments are provided after the priority parameter, they will be passed to the provided callback method.</span></span>  <span data-ttu-id="9507b-308">Si le paramètre callback renvoie une valeur, cette valeur devient également la valeur de retour `execAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="9507b-308">If the callback parameter returns a value, this value becomes the return value for `execAtPriority` as well.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-309">Exemple</span><span class="sxs-lookup"><span data-stu-id="9507b-309">Example</span></span>**  
      
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

### <span data-ttu-id="9507b-310">getCurrentPriority</span><span class="sxs-lookup"><span data-stu-id="9507b-310">getCurrentPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="9507b-311">Renvoie la priorité contextuelle actuelle.</span><span class="sxs-lookup"><span data-stu-id="9507b-311">Returns the current contextual priority.</span></span>  

   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getCurrentPriority();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-312">Parameters</span><span class="sxs-lookup"><span data-stu-id="9507b-312">Parameters</span></span>**  
      
      <span data-ttu-id="9507b-313">Aucune.</span><span class="sxs-lookup"><span data-stu-id="9507b-313">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-314">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9507b-314">Return value</span></span>**  
      
      | <span data-ttu-id="9507b-315">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-315">Type</span></span> | <span data-ttu-id="9507b-316">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-316">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-317">DOMString</span><span class="sxs-lookup"><span data-stu-id="9507b-317">DOMString</span></span> | <span data-ttu-id="9507b-318">La valeur de retour est l’une des chaînes `MSApp.HIGH` , `MSApp.NORMAL` ou `MSApp.IDLE` .</span><span class="sxs-lookup"><span data-stu-id="9507b-318">The return value is one of the strings `MSApp.HIGH`, `MSApp.NORMAL`, or `MSApp.IDLE`.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-319">Exceptions</span><span class="sxs-lookup"><span data-stu-id="9507b-319">Exceptions</span></span>**  
      
      <span data-ttu-id="9507b-320">Aucune.</span><span class="sxs-lookup"><span data-stu-id="9507b-320">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-321">Remarques</span><span class="sxs-lookup"><span data-stu-id="9507b-321">Remarks</span></span>**  
      
      <span data-ttu-id="9507b-322">Cette méthode renvoie la priorité contextuelle actuelle \ (voir [constantes MSApp](#msapp-constants)\), qui peut être modifié via `execAtPriority` et `execAsyncAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="9507b-322">This method returns the current contextual priority \(see [MSApp Constants](#msapp-constants)\), which can be changed via `execAtPriority` and `execAsyncAtPriority`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-323">Exemple</span><span class="sxs-lookup"><span data-stu-id="9507b-323">Example</span></span>**  
      
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

### <span data-ttu-id="9507b-324">getHtmlPrintDocumentSource</span><span class="sxs-lookup"><span data-stu-id="9507b-324">getHtmlPrintDocumentSource</span></span>  

<span data-ttu-id="9507b-325">API synchrone qui est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="9507b-325">Synchronous API that has been deprecated.</span></span>  <span data-ttu-id="9507b-326">Pour Windows 10, voir `getHtmlPrintDocumentSourceAsync` .</span><span class="sxs-lookup"><span data-stu-id="9507b-326">For Windows 10, see `getHtmlPrintDocumentSourceAsync`.</span></span>  <span data-ttu-id="9507b-327">Pour les applications Windows 8 et 8,1, consultez le site Web entrée pour [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span><span class="sxs-lookup"><span data-stu-id="9507b-327">For Windows 8 and 8.1 apps, see the MSDN entry for [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span></span>  

### <span data-ttu-id="9507b-328">getHtmlPrintDocumentSourceAsync</span><span class="sxs-lookup"><span data-stu-id="9507b-328">getHtmlPrintDocumentSourceAsync</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="9507b-329">Renvoie le contenu source à imprimer.</span><span class="sxs-lookup"><span data-stu-id="9507b-329">Returns the source content that is to be printed.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.getHtmlPrintDocumentSourceAsync(document);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-330">Parameters</span><span class="sxs-lookup"><span data-stu-id="9507b-330">Parameters</span></span>**  
      
      `htmlDoc` <span data-ttu-id="9507b-331">complémentaire</span><span class="sxs-lookup"><span data-stu-id="9507b-331">[in]</span></span>  
      
      | <span data-ttu-id="9507b-332">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-332">Type</span></span> | <span data-ttu-id="9507b-333">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-333">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-334">Document</span><span class="sxs-lookup"><span data-stu-id="9507b-334">Document</span></span> | <span data-ttu-id="9507b-335">Le document HTML à imprimer.</span><span class="sxs-lookup"><span data-stu-id="9507b-335">The HTML document to be printed.</span></span>  <span data-ttu-id="9507b-336">Il peut s’agir du document racine, du document dans un IFRAME, d’un fragment de document ou d’un document SVG.</span><span class="sxs-lookup"><span data-stu-id="9507b-336">This can be the root document, the document in an iframe, a document fragment, or a SVG document.</span></span>  <span data-ttu-id="9507b-337">Sachez que htmlDoc doit être un document et non un élément.</span><span class="sxs-lookup"><span data-stu-id="9507b-337">Be aware that htmlDoc must be a document, not an element.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-338">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9507b-338">Return value</span></span>**
      
      <span data-ttu-id="9507b-339">Aucune.</span><span class="sxs-lookup"><span data-stu-id="9507b-339">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-340">Exceptions</span><span class="sxs-lookup"><span data-stu-id="9507b-340">Exceptions</span></span>**  
      
      <span data-ttu-id="9507b-341">Aucune.</span><span class="sxs-lookup"><span data-stu-id="9507b-341">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-342">Remarques</span><span class="sxs-lookup"><span data-stu-id="9507b-342">Remarks</span></span>**  
      
      <span data-ttu-id="9507b-343">Aucune.</span><span class="sxs-lookup"><span data-stu-id="9507b-343">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-344">Exemple1</span><span class="sxs-lookup"><span data-stu-id="9507b-344">Example 1</span></span>**  
      
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
      **<span data-ttu-id="9507b-345">Exemple2</span><span class="sxs-lookup"><span data-stu-id="9507b-345">Example 2</span></span>**  
      
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

### <span data-ttu-id="9507b-346">getViewId</span><span class="sxs-lookup"><span data-stu-id="9507b-346">getViewId</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="9507b-347">Prise en charge de plusieurs fenêtres.</span><span class="sxs-lookup"><span data-stu-id="9507b-347">Support for multiple windows.</span></span>  
      
      > [!NOTE] 
      > <span data-ttu-id="9507b-348">Dans les applications UWP JavaScript de Win 8.1 prises en charge plusieurs fenêtres utilisant des API MSApp DOM qui sont désormais depricated.</span><span class="sxs-lookup"><span data-stu-id="9507b-348">In Win8.1 JavaScript UWP apps supported multiple windows using MSApp DOM APIs which are now depricated.</span></span>  <span data-ttu-id="9507b-349">Pour Windows 10, utilisez `window.open` , `window` et le nouveau `MSApp.getViewId` .</span><span class="sxs-lookup"><span data-stu-id="9507b-349">For Windows 10, use `window.open`, `window`, and the new `MSApp.getViewId`.</span></span>  
      
      | <span data-ttu-id="9507b-350">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-350">Description</span></span> |<span data-ttu-id="9507b-351">Windows 10</span><span class="sxs-lookup"><span data-stu-id="9507b-351">Windows 10</span></span> | <span data-ttu-id="9507b-352">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9507b-352">Windows 8.1</span></span> |  
      |:---- |:---- |:--- |  
      | <span data-ttu-id="9507b-353">Créer une fenêtre</span><span class="sxs-lookup"><span data-stu-id="9507b-353">Create new window</span></span> | [<span data-ttu-id="9507b-354">fenêtre. ouvrir</span><span class="sxs-lookup"><span data-stu-id="9507b-354">window.open</span></span>](https://developer.mozilla.org/docs/Web/API/Window/open) | [<span data-ttu-id="9507b-355">MSApp. createNewView</span><span class="sxs-lookup"><span data-stu-id="9507b-355">MSApp.createNewView</span></span>](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
      |<span data-ttu-id="9507b-356">Nouvel objet Window</span><span class="sxs-lookup"><span data-stu-id="9507b-356">New window object</span></span> | [<span data-ttu-id="9507b-357">fenêtre</span><span class="sxs-lookup"><span data-stu-id="9507b-357">window</span></span>](https://developer.mozilla.org/docs/Web/API/Window) |[<span data-ttu-id="9507b-358">MSAppView</span><span class="sxs-lookup"><span data-stu-id="9507b-358">MSAppView</span></span>](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getViewId(window); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-359">Parameters</span><span class="sxs-lookup"><span data-stu-id="9507b-359">Parameters</span></span>**  
      
      `window`
      
      | <span data-ttu-id="9507b-360">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-360">Type</span></span> | <span data-ttu-id="9507b-361">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-361">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-362">DOMString</span><span class="sxs-lookup"><span data-stu-id="9507b-362">DOMString</span></span> | <span data-ttu-id="9507b-363">Objet représentant une fenêtre contenant un document DOM.</span><span class="sxs-lookup"><span data-stu-id="9507b-363">An object representing a window containing a DOM document.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-364">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9507b-364">Return value</span></span>**  
      
      `viewId`
      
      | <span data-ttu-id="9507b-365">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-365">Type</span></span> | <span data-ttu-id="9507b-366">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-366">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-367">Nombre</span><span class="sxs-lookup"><span data-stu-id="9507b-367">Number</span></span> | <span data-ttu-id="9507b-368">Peut être utilisé avec les diverses API [Windows. UI. ViewManagement. ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) .</span><span class="sxs-lookup"><span data-stu-id="9507b-368">Can be used with the various [Windows.UI.ViewManagement.ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-369">Exceptions</span><span class="sxs-lookup"><span data-stu-id="9507b-369">Exceptions</span></span>**  
      
      <span data-ttu-id="9507b-370">Aucune.</span><span class="sxs-lookup"><span data-stu-id="9507b-370">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-371">Remarques</span><span class="sxs-lookup"><span data-stu-id="9507b-371">Remarks</span></span>**  
      
      <span data-ttu-id="9507b-372">Utilisez [Window. Open](https://developer.mozilla.org/docs/Web/API/Window/open) et [Window](https://developer.mozilla.org/docs/Web/API/Window) pour créer des fenêtres, mais pour interagir avec des API WinRT, ajoutez l' `MSApp.getViewId` API.</span><span class="sxs-lookup"><span data-stu-id="9507b-372">Use [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) and [window](https://developer.mozilla.org/docs/Web/API/Window) for creating new windows, but then to interact with WinRT APIs, add the `MSApp.getViewId` API.</span></span>  <span data-ttu-id="9507b-373">Il accepte un `window` objet en tant que paramètre et renvoie un `viewId` nombre qui peut être utilisé avec les diverses API [Windows. UI. ViewManagement. ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) .</span><span class="sxs-lookup"><span data-stu-id="9507b-373">It takes a `window` object as a parameter and returns a `viewId` number that can be used with the various [Windows.UI.ViewManagement.ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span>  
      
      *   <span data-ttu-id="9507b-374">Retardement de la visibilité</span><span class="sxs-lookup"><span data-stu-id="9507b-374">Delaying Visibility</span></span>  
          
          <span data-ttu-id="9507b-375">Dans le cas d’un affichage complet, les vues sont masquées et le développeur `TryShowAsStandaloneAsync` doit afficher l’affichage une fois qu’il est entièrement préparé.</span><span class="sxs-lookup"><span data-stu-id="9507b-375">Views in WinRT normally start hidden and the end developer uses something like `TryShowAsStandaloneAsync` to display the view once it is fully prepared.</span></span>  <span data-ttu-id="9507b-376">Dans le monde Web, `window.open` affiche une fenêtre immédiatement et l’utilisateur final peut voir le contenu chargé et affiché.</span><span class="sxs-lookup"><span data-stu-id="9507b-376">In the web world, `window.open` shows a window immediately and the end user can watch as content is loaded and rendered.</span></span>  <span data-ttu-id="9507b-377">Pour que votre nouvelle Windows serve de vues dans WinRT et qu’elle ne soit pas affichée immédiatement, nous avons ajouté une `window.open` option.</span><span class="sxs-lookup"><span data-stu-id="9507b-377">To have your new windows act like views in WinRT and not display immediately we have added a `window.open` option.</span></span>  <span data-ttu-id="9507b-378">Par exemple:</span><span class="sxs-lookup"><span data-stu-id="9507b-378">For example:</span></span>  
          
          ```javascript
          let newWindow = window.open("https://example.com", null, "msHideView=yes");
          ```  
          
      *   <span data-ttu-id="9507b-379">Différences entre les fenêtres principales</span><span class="sxs-lookup"><span data-stu-id="9507b-379">Primary Window Differences</span></span>  
          
          <span data-ttu-id="9507b-380">La fenêtre principale ouverte par le système d’exploitation agit de la même manière que celle des fenêtres secondaires qui s’affichent:</span><span class="sxs-lookup"><span data-stu-id="9507b-380">The primary window that is initially opened by the OS acts differently than the secondary windows that it opens:</span></span>  
          
          | <span data-ttu-id="9507b-381">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-381">Description</span></span> | <span data-ttu-id="9507b-382">Principal</span><span class="sxs-lookup"><span data-stu-id="9507b-382">Primary</span></span> | <span data-ttu-id="9507b-383">Secondaire</span><span class="sxs-lookup"><span data-stu-id="9507b-383">Secondary</span></span> |  
          |:---- |:--- |:--- |  
          | <span data-ttu-id="9507b-384">fenêtre. ouvrir</span><span class="sxs-lookup"><span data-stu-id="9507b-384">window.open</span></span> | <span data-ttu-id="9507b-385">Autorisée</span><span class="sxs-lookup"><span data-stu-id="9507b-385">Allowed</span></span> | <span data-ttu-id="9507b-386">Non autorisé</span><span class="sxs-lookup"><span data-stu-id="9507b-386">Disallowed</span></span> |  
          | <span data-ttu-id="9507b-387">Window. Close</span><span class="sxs-lookup"><span data-stu-id="9507b-387">window.close</span></span> | <span data-ttu-id="9507b-388">Fermer l’application</span><span class="sxs-lookup"><span data-stu-id="9507b-388">Close app</span></span> | <span data-ttu-id="9507b-389">Fermer la fenêtre</span><span class="sxs-lookup"><span data-stu-id="9507b-389">Close window</span></span> |  
          | <span data-ttu-id="9507b-390">Restrictions de navigation</span><span class="sxs-lookup"><span data-stu-id="9507b-390">Navigation restrictions</span></span> | <span data-ttu-id="9507b-391">FORME règles ACUR uniquement</span><span class="sxs-lookup"><span data-stu-id="9507b-391">ACUR only</span></span> | <span data-ttu-id="9507b-392">Aucune restriction</span><span class="sxs-lookup"><span data-stu-id="9507b-392">No restrictions</span></span> |  
          
          <span data-ttu-id="9507b-393">Il est possible que l’ouverture d’un autre Windows ne puisse changer dans le futur en fonction de votre [avis](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).</span><span class="sxs-lookup"><span data-stu-id="9507b-393">The restriction to not allow secondary windows to open could change in the future depending on [feedback](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).</span></span>  
      
      *   <span data-ttu-id="9507b-394">Restrictions de communication d’origine identiques</span><span class="sxs-lookup"><span data-stu-id="9507b-394">Same Origin Communication Restrictions</span></span>  
          
          <span data-ttu-id="9507b-395">La prise en charge d’un problème technique unique empêche une prise en charge de la prise en charge de la synchronisation, des appels entre les scripts.</span><span class="sxs-lookup"><span data-stu-id="9507b-395">There is a difficult technical issue preventing proper support for synchronous, same-origin, cross-window, script calls.</span></span>  <span data-ttu-id="9507b-396">Lorsque vous ouvrez une fenêtre qui est identique à l’origine, le script d’une fenêtre est autorisé à appeler directement les fonctions dans l’autre fenêtre, et certains de ces appels échouent.</span><span class="sxs-lookup"><span data-stu-id="9507b-396">When you open a window that is same origin, script in one window is allowed to directly call functions in the other window, and some of these calls will fail.</span></span>  `postMessage` <span data-ttu-id="9507b-397">les appels fonctionnent parfaitement et il est recommandé de procéder comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="9507b-397">calls work just fine and is the recommended way to do things if possible.</span></span>  <span data-ttu-id="9507b-398">Le travail pour améliorer ce problème est en cours.</span><span class="sxs-lookup"><span data-stu-id="9507b-398">Work to improve this issue is in progress.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-399">Exemple</span><span class="sxs-lookup"><span data-stu-id="9507b-399">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
    
### <span data-ttu-id="9507b-400">isTaskScheduledAtPriorityOrHigher</span><span class="sxs-lookup"><span data-stu-id="9507b-400">isTaskScheduledAtPriorityOrHigher</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="9507b-401">Renvoie une donnée de type booléen indiquant s’il existe une tâche en attente au niveau de priorité donné ou une valeur supérieure.</span><span class="sxs-lookup"><span data-stu-id="9507b-401">Returns a Boolean value indicating whether there is pending work at the given priority level or higher.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-402">Parameters</span><span class="sxs-lookup"><span data-stu-id="9507b-402">Parameters</span></span>**  
      
      `priority` <span data-ttu-id="9507b-403">complémentaire</span><span class="sxs-lookup"><span data-stu-id="9507b-403">[in]</span></span>
      
      | <span data-ttu-id="9507b-404">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-404">Type</span></span> | <span data-ttu-id="9507b-405">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-405">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-406">DOMString</span><span class="sxs-lookup"><span data-stu-id="9507b-406">DOMString</span></span> | <span data-ttu-id="9507b-407">Valeur de priorité \ (voir [constantes MSApp](#msapp-constants)\) spécifiant le niveau de priorité et au-dessus pour rechercher tout Work en attente.</span><span class="sxs-lookup"><span data-stu-id="9507b-407">A priority value \(see [MSApp Constants](#msapp-constants)\) specifying the priority level and above to query for any outstanding queued work.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-408">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9507b-408">Return value</span></span>**  
      
      | <span data-ttu-id="9507b-409">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-409">Type</span></span> | <span data-ttu-id="9507b-410">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-410">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-411">Booléen</span><span class="sxs-lookup"><span data-stu-id="9507b-411">Boolean</span></span> | <span data-ttu-id="9507b-412">Renvoie `true` s’il existe un fonctionnement en file d’attente au niveau de priorité spécifié, `false` sinon.</span><span class="sxs-lookup"><span data-stu-id="9507b-412">Returns `true` if there is any queued work at the specified priority level or above, `false` otherwise.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-413">Exceptions</span><span class="sxs-lookup"><span data-stu-id="9507b-413">Exceptions</span></span>**  
      
      <span data-ttu-id="9507b-414">Aucune.</span><span class="sxs-lookup"><span data-stu-id="9507b-414">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-415">Remarques</span><span class="sxs-lookup"><span data-stu-id="9507b-415">Remarks</span></span>**  
      
      <span data-ttu-id="9507b-416">Cette `isTaskScheduledAtPriorityOrHigher` méthode fournit un moyen pour le code JavaScript de déterminer s’il existe des tâches en attente aux différents niveaux de priorité \ (ou au-dessus de \), ce qui permet à la personne d’appeler du code JavaScript de manière à utiliser une priorité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="9507b-416">The `isTaskScheduledAtPriorityOrHigher` method provides a means for JavaScript code to determine if there is pending work at the various priority levels \(or above\) with the intent that the calling JavaScript code can then decide to yield to higher priority work.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-417">Exemple</span><span class="sxs-lookup"><span data-stu-id="9507b-417">Example</span></span>**  
      
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

### <span data-ttu-id="9507b-418">pageHandlesAllApplicationActivations</span><span class="sxs-lookup"><span data-stu-id="9507b-418">pageHandlesAllApplicationActivations</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="9507b-419">Permet d’éviter une actualisation de la trajectoire de début (rechargement de la page) avant chaque événement d’activation (par exemple, en cliquant sur une notification ou sur une vignette épinglée).</span><span class="sxs-lookup"><span data-stu-id="9507b-419">Used to avoid a refresh of the start path (page reload) before every activate event \(such as clicking a notification or a pinned tile\).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.pageHandlesAllApplicationActivations(boolean);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-420">Parameters</span><span class="sxs-lookup"><span data-stu-id="9507b-420">Parameters</span></span>**  
      
      | <span data-ttu-id="9507b-421">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-421">Type</span></span> | <span data-ttu-id="9507b-422">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-422">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-423">Booléen</span><span class="sxs-lookup"><span data-stu-id="9507b-423">Boolean</span></span> | <span data-ttu-id="9507b-424">Utilisez `MSApp.pageHandlesAllApplicationActivations(true)` cette méthode pour toujours éviter d’actualiser la trajectoire de début (rechargement de la page) et de passer directement au déclenchement de l' `WebUIApplication` événement Activated.</span><span class="sxs-lookup"><span data-stu-id="9507b-424">Use `MSApp.pageHandlesAllApplicationActivations(true)` to always skip refreshing the start path (page reload) and instead jump straight to firing the `WebUIApplication` activated event.</span></span>  <span data-ttu-id="9507b-425">Nécessite que toutes les pages gèrent les événements d’activation séparément.</span><span class="sxs-lookup"><span data-stu-id="9507b-425">Requires that all pages handle activation events separately.</span></span>  <span data-ttu-id="9507b-426">En définissant cette méthode `true` , en cliquant sur un événement Activated (par exemple, une notification) ne déclenche pas le recharge, une application essentielle pour les applications à page unique veut éviter les recharges de pages.</span><span class="sxs-lookup"><span data-stu-id="9507b-426">By defining this method as `true`, clicking an activated event \(like a notification\) will not trigger the reload, an essential for single-page apps wishing to avoid page reloads.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-427">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9507b-427">Return value</span></span>**
      
      <span data-ttu-id="9507b-428">Aucune.</span><span class="sxs-lookup"><span data-stu-id="9507b-428">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-429">Exceptions</span><span class="sxs-lookup"><span data-stu-id="9507b-429">Exceptions</span></span>**  
      
      <span data-ttu-id="9507b-430">Aucune.</span><span class="sxs-lookup"><span data-stu-id="9507b-430">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-431">Remarques</span><span class="sxs-lookup"><span data-stu-id="9507b-431">Remarks</span></span>**  
      
      <span data-ttu-id="9507b-432">Aucune.</span><span class="sxs-lookup"><span data-stu-id="9507b-432">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-433">Exemple</span><span class="sxs-lookup"><span data-stu-id="9507b-433">Example</span></span>**  
      
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

### <span data-ttu-id="9507b-434">suppressSubdownloadCredentialPrompts</span><span class="sxs-lookup"><span data-stu-id="9507b-434">suppressSubdownloadCredentialPrompts</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="9507b-435">Détermine si une application supprime les invites d’authentification possibles lors du téléchargement de ressources.</span><span class="sxs-lookup"><span data-stu-id="9507b-435">Controls whether an app suppresses possible authentication prompts during the download of resources.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.suppressSubdownloadCredentialPrompts(suppress);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-436">Parameters</span><span class="sxs-lookup"><span data-stu-id="9507b-436">Parameters</span></span>**  
     
      `suppress` <span data-ttu-id="9507b-437">complémentaire</span><span class="sxs-lookup"><span data-stu-id="9507b-437">[in]</span></span>
      
      | <span data-ttu-id="9507b-438">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-438">Type</span></span> | <span data-ttu-id="9507b-439">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-439">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-440">Booléen</span><span class="sxs-lookup"><span data-stu-id="9507b-440">Boolean</span></span> | <span data-ttu-id="9507b-441">La valeur true supprime les invites d’authentification potentielles.</span><span class="sxs-lookup"><span data-stu-id="9507b-441">A value of true suppresses potential authentication prompts.</span></span>  <span data-ttu-id="9507b-442">La valeur false ne supprime pas les invites d’authentification potentielles de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9507b-442">A value of false does not suppress any potential authentication prompts from the user.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-443">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9507b-443">Return value</span></span>**  
      
      <span data-ttu-id="9507b-444">Aucune.</span><span class="sxs-lookup"><span data-stu-id="9507b-444">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-445">Exceptions</span><span class="sxs-lookup"><span data-stu-id="9507b-445">Exceptions</span></span>**  
      
      <span data-ttu-id="9507b-446">Aucune.</span><span class="sxs-lookup"><span data-stu-id="9507b-446">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-447">Remarques</span><span class="sxs-lookup"><span data-stu-id="9507b-447">Remarks</span></span>**  
      
      <span data-ttu-id="9507b-448">La `suppressSubdownloadCredentialPrompts` méthode contrôle si une application supprime les invites d’authentification potentielles lors du téléchargement de ressources.</span><span class="sxs-lookup"><span data-stu-id="9507b-448">The `suppressSubdownloadCredentialPrompts` method controls whether an app suppresses potential authentication prompts during the download of resources.</span></span>  <span data-ttu-id="9507b-449">Le comportement par défaut consiste à ne pas supprimer les invites d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="9507b-449">The default behavior is to not suppress credential prompts.</span></span>  
      
      `suppressSubdownloadCredentialPrompts` <span data-ttu-id="9507b-450">est destiné à être utilisé par des applications susceptibles de charger un nombre excessif de ressources qui nécessitent une authentification, par exemple une application de messagerie (qui peut contenir un bulletin d’informations contenant un certain nombre d’images nécessitant une authentification \).</span><span class="sxs-lookup"><span data-stu-id="9507b-450">is intended for use by apps which may load an excessive number of resources that require authentication, such as a mail app \(which could contain a newsletter containing a number of images where each image requires authentication\).</span></span>  
      
      <span data-ttu-id="9507b-451">Lorsque vous supprimez des invites d’informations d’identification, les boîtes de dialogue d’authentification aux serveurs ne s’afficheront pas lors de l’accès aux ressources qui nécessitent une authentification et la ressource ne sera pas téléchargée.</span><span class="sxs-lookup"><span data-stu-id="9507b-451">When suppressing credential prompts, dialogs for authenticating to servers will not be shown when accessing resources that require authentication, and the resource will not be downloaded.</span></span>  <span data-ttu-id="9507b-452">Notez que `suppressSubdownloadCredentialPrompts` l’authentification proxy ou les boîtes de dialogue de demande de certification du client n’ont pas d’impact sur les autres invites possibles, comme l’authentification du proxy ou les boîtes de dialogue de demande de certification</span><span class="sxs-lookup"><span data-stu-id="9507b-452">Note that `suppressSubdownloadCredentialPrompts` does not impact other possible prompts such as proxy authentication or client certification request dialogs, nor does it impact XHR.</span></span>  
      
      <span data-ttu-id="9507b-453">Sachez que cela a un `suppressSubdownloadCredentialPrompts` impact sur tout le contenu de l’application, y compris le contenu hébergé dans l' `webview` élément.</span><span class="sxs-lookup"><span data-stu-id="9507b-453">Be aware that `suppressSubdownloadCredentialPrompts` impacts all content in the application, including content hosted in the `webview` element.</span></span>  
      
      > [!IMPORTANT]
      > <span data-ttu-id="9507b-454">Les décisions d’instructions d’identification sont mises en cache.</span><span class="sxs-lookup"><span data-stu-id="9507b-454">Credential prompt decisions are cached.</span></span>  <span data-ttu-id="9507b-455">Par conséquent, si vous supprimez des invites d’informations d’identification, celles-ci peuvent être prises en compte immédiatement, permettant ainsi aux invites d’informations d’identification d’être supprimées.</span><span class="sxs-lookup"><span data-stu-id="9507b-455">Therefore, while suppressing credential prompts will take effect immediately, allowing credential prompts after suppressing them may need a reload of the document to take effect.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-456">Exemple</span><span class="sxs-lookup"><span data-stu-id="9507b-456">Example</span></span>**  
      
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

### <span data-ttu-id="9507b-457">terminateApp</span><span class="sxs-lookup"><span data-stu-id="9507b-457">terminateApp</span></span>  


:::row:::
   :::column span="":::
      <span data-ttu-id="9507b-458">Arrête l’application actuelle et génère un rapport d’échec.</span><span class="sxs-lookup"><span data-stu-id="9507b-458">Terminates the current application and generates a failure report.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.terminateApp(error);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-459">Parameters</span><span class="sxs-lookup"><span data-stu-id="9507b-459">Parameters</span></span>**  
      
      `error` <span data-ttu-id="9507b-460">complémentaire</span><span class="sxs-lookup"><span data-stu-id="9507b-460">[in]</span></span>
      
      | <span data-ttu-id="9507b-461">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-461">Type</span></span> | <span data-ttu-id="9507b-462">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-462">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-463">Erreur</span><span class="sxs-lookup"><span data-stu-id="9507b-463">Error</span></span> | <span data-ttu-id="9507b-464">Un `Error` objet que vous pouvez utiliser pour décrire l’erreur à l’origine de l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="9507b-464">An `Error` object that you can use to describe the error that triggered the termination.</span></span>  <span data-ttu-id="9507b-465">L' `Error` objet doit contenir les propriétés Number, description et Stack; un rapport d’échec n’est pas généré si l’objet ne contient pas ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="9507b-465">The `Error` object must contain the number, description, and stack properties; a failure report won't be generated if the object doesn't contain these properties.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-466">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9507b-466">Return value</span></span>**
      
      <span data-ttu-id="9507b-467">Aucune.</span><span class="sxs-lookup"><span data-stu-id="9507b-467">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-468">Exceptions</span><span class="sxs-lookup"><span data-stu-id="9507b-468">Exceptions</span></span>**  
      
      <span data-ttu-id="9507b-469">Aucune.</span><span class="sxs-lookup"><span data-stu-id="9507b-469">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-470">Remarques</span><span class="sxs-lookup"><span data-stu-id="9507b-470">Remarks</span></span>**  
      
      <span data-ttu-id="9507b-471">Si le problème signalé par `terminateApp` devient l’un des 5 premiers problèmes de votre application, il apparaît sur la page qualité de l’application.</span><span class="sxs-lookup"><span data-stu-id="9507b-471">If the issue reported by `terminateApp` becomes one of your app's top 5 issues, it will show up on the app's Quality page.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-472">Exemple</span><span class="sxs-lookup"><span data-stu-id="9507b-472">Example</span></span>**  
      
      <span data-ttu-id="9507b-473">Cet exemple appelle `terminateApp` quand une exception est rencontrée.</span><span class="sxs-lookup"><span data-stu-id="9507b-473">This example calls `terminateApp` when an exception is encountered.</span></span>  <span data-ttu-id="9507b-474">Il utilise l' `Error` objet fourni lors de la capture d’une exception.</span><span class="sxs-lookup"><span data-stu-id="9507b-474">It uses the `Error` object provided when you catch an exception.</span></span>  
      
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

### <span data-ttu-id="9507b-475">Constantes MSApp</span><span class="sxs-lookup"><span data-stu-id="9507b-475">MSApp Constants</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="9507b-476">Valeurs de priorité autorisées associées à `execAsyncAtPriority` , `execAtPriority` , `getCurrentPriority` et `isTaskScheduldAtPriorityOrHigher` .</span><span class="sxs-lookup"><span data-stu-id="9507b-476">Allowed priority values associated with `execAsyncAtPriority`, `execAtPriority`, `getCurrentPriority`, and `isTaskScheduldAtPriorityOrHigher`.</span></span>  
   :::column-end:::
   :::column span="":::
      #### <span data-ttu-id="9507b-477">Actuel</span><span class="sxs-lookup"><span data-stu-id="9507b-477">Current</span></span>  
      
      `current`  
      
      | <span data-ttu-id="9507b-478">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-478">Type</span></span> | <span data-ttu-id="9507b-479">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-479">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-480">DOMString</span><span class="sxs-lookup"><span data-stu-id="9507b-480">DOMString</span></span> | <span data-ttu-id="9507b-481">Lorsque `current` est utilisé avec la méthode appropriée \ (voir aussi section \), la méthode utilise la priorité contextuelle actuelle lors de l’exécution de l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="9507b-481">When `current` is used with the appropriate method \(See also section\), the method will use the current contextual priority when executing the requested operation.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <span data-ttu-id="9507b-482">High</span><span class="sxs-lookup"><span data-stu-id="9507b-482">High</span></span>  
      
      `high`  
      
      | <span data-ttu-id="9507b-483">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-483">Type</span></span> | <span data-ttu-id="9507b-484">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-484">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-485">DOMString</span><span class="sxs-lookup"><span data-stu-id="9507b-485">DOMString</span></span> | <span data-ttu-id="9507b-486">Lorsque `high` est utilisé avec la méthode appropriée \ (voir aussi section \), la méthode utilisera une priorité supérieure à la valeur normale lors de l’exécution de l’opération demandée et sera retirée de l’opération avant tout fonctionnement de priorité normale existant.</span><span class="sxs-lookup"><span data-stu-id="9507b-486">When `high` is used with the appropriate method \(See also section\), the method will use higher than normal priority when executing the requested operation and will be dispatch the operation before any existing normal priority work.</span></span>  |  
   :::column-end:::
   :::column span="":::
      #### <span data-ttu-id="9507b-487">Inactif</span><span class="sxs-lookup"><span data-stu-id="9507b-487">Idle</span></span>  
      
      `idle`  
      
      | <span data-ttu-id="9507b-488">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-488">Type</span></span> | <span data-ttu-id="9507b-489">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-489">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-490">DOMString</span><span class="sxs-lookup"><span data-stu-id="9507b-490">DOMString</span></span> | <span data-ttu-id="9507b-491">Lorsque `ideal` est utilisé avec la méthode appropriée \ (voir aussi section \), la méthode utilise une priorité inférieure à la valeur normale lors de l’exécution de l’opération demandée et sera retirée de l’opération après tout fonctionnement prioritaire normal.</span><span class="sxs-lookup"><span data-stu-id="9507b-491">When `ideal` is used with the appropriate method \(See also section\), the method will use lower than normal priority when executing the requested operation and will be dispatch the operation after any existing normal priority work.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <span data-ttu-id="9507b-492">Normal</span><span class="sxs-lookup"><span data-stu-id="9507b-492">Normal</span></span>  
      
      `normal`  
      
      | <span data-ttu-id="9507b-493">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-493">Type</span></span> | <span data-ttu-id="9507b-494">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-494">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-495">DOMString</span><span class="sxs-lookup"><span data-stu-id="9507b-495">DOMString</span></span> | <span data-ttu-id="9507b-496">Lorsque `normal` est utilisé avec la méthode appropriée (voir aussi section), la méthode utilise la priorité actuelle normale lors de l’exécution de l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="9507b-496">When `normal` is used with the appropriate method (See also section), the method will use the normal existing priority when executing the requested operation.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-497">Exemple</span><span class="sxs-lookup"><span data-stu-id="9507b-497">Example</span></span>**  
      
      ```javascript
      if (window.MSApp.CURRENT) {
          document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
      }
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-498">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9507b-498">Requirements</span></span>**  
      
      | <span data-ttu-id="9507b-499">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-499">Type</span></span> | <span data-ttu-id="9507b-500">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-500">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-501">MIDL</span><span class="sxs-lookup"><span data-stu-id="9507b-501">IDL</span></span> | <span data-ttu-id="9507b-502">Mshtml. idl</span><span class="sxs-lookup"><span data-stu-id="9507b-502">Mshtml.idl</span></span> |  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="9507b-503">MSAppAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="9507b-503">MSAppAsyncOperation</span></span>  

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```  

### <span data-ttu-id="9507b-504">start</span><span class="sxs-lookup"><span data-stu-id="9507b-504">start</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="9507b-505">Démarre `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="9507b-505">Starts the `MSAppAsyncOperation`.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSAppAsyncOperation.start();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="9507b-506">Parameters</span><span class="sxs-lookup"><span data-stu-id="9507b-506">Parameters</span></span>**  
      
      <span data-ttu-id="9507b-507">Aucune.</span><span class="sxs-lookup"><span data-stu-id="9507b-507">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="9507b-508">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9507b-508">Return value</span></span>**
      
      <span data-ttu-id="9507b-509">Aucune.</span><span class="sxs-lookup"><span data-stu-id="9507b-509">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      
      **<span data-ttu-id="9507b-510">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9507b-510">Properties</span></span>**  
      
      `error` <span data-ttu-id="9507b-511">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9507b-511">property</span></span>  
      
      | <span data-ttu-id="9507b-512">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-512">Type</span></span> | <span data-ttu-id="9507b-513">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-513">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-514">DOMError</span><span class="sxs-lookup"><span data-stu-id="9507b-514">DOMError</span></span> | <span data-ttu-id="9507b-515">Représente une erreur dans `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="9507b-515">Represents an error in `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.error
      ```  
      
      `oncomplete` <span data-ttu-id="9507b-516">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9507b-516">property</span></span>  
      
      | <span data-ttu-id="9507b-517">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-517">Type</span></span> | <span data-ttu-id="9507b-518">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-518">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-519">EventHandler</span><span class="sxs-lookup"><span data-stu-id="9507b-519">EventHandler</span></span> | <span data-ttu-id="9507b-520">Propriété permettant de définir un gestionnaire d’événements à l’achèvement de `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="9507b-520">Property for setting an event handler on completion of `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.oncomplete
      ```  
      
      `onerror` <span data-ttu-id="9507b-521">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9507b-521">property</span></span>  
      
      | <span data-ttu-id="9507b-522">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-522">Type</span></span> | <span data-ttu-id="9507b-523">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-523">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-524">EventHandler</span><span class="sxs-lookup"><span data-stu-id="9507b-524">EventHandler</span></span> | <span data-ttu-id="9507b-525">Propriété permettant de définir un gestionnaire d’événements sur une erreur au cours de l’appel `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="9507b-525">Property for setting an event handler upon an error during `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.onerror
      ```  
      
      `readyState` <span data-ttu-id="9507b-526">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9507b-526">property</span></span>  
      
      | <span data-ttu-id="9507b-527">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-527">Type</span></span> | <span data-ttu-id="9507b-528">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-528">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-529">Nombre</span><span class="sxs-lookup"><span data-stu-id="9507b-529">Number</span></span> | <span data-ttu-id="9507b-530">Représente l’état de l’opération asynchrone dans l’application Windows en JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9507b-530">Represents the state of the asynchronous operation within the Windows app using JavaScript.</span></span>  <span data-ttu-id="9507b-531">Les valeurs incluent `Started[0]` : `Completed[1]` , `Error[2]` .</span><span class="sxs-lookup"><span data-stu-id="9507b-531">Values include: `Started[0]`, `Completed[1]`, `Error[2]`.</span></span>  |  
      
      ```javascript
      p = object.readyState
      ```  
      
      `result` <span data-ttu-id="9507b-532">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9507b-532">property</span></span>  
      
      | <span data-ttu-id="9507b-533">Type</span><span class="sxs-lookup"><span data-stu-id="9507b-533">Type</span></span> | <span data-ttu-id="9507b-534">Description</span><span class="sxs-lookup"><span data-stu-id="9507b-534">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="9507b-535">Indifférent</span><span class="sxs-lookup"><span data-stu-id="9507b-535">Any</span></span> |<span data-ttu-id="9507b-536">Représente le résultat de `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="9507b-536">Represents the result of `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.result
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
