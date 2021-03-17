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
# <a name="msapp"></a><span data-ttu-id="7760e-105">MSApp</span><span class="sxs-lookup"><span data-stu-id="7760e-105">MSApp</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="7760e-106">L’objet MSApp et ses membres sont pris en charge uniquement pour les applications Windows utilisant JavaScript \(y compris les applications P.A.S. accédant aux fonctionnalités de l’API Windows\).</span><span class="sxs-lookup"><span data-stu-id="7760e-106">The MSApp object and its members are supported only for Windows apps using JavaScript \(including PWAs accessing Windows API features\).</span></span>  <span data-ttu-id="7760e-107">L’objet MSApp existe uniquement dans le contexte local d’un document HTML dans une application Windows chargée via le schéma d’URI ms-appx ; sinon, l’objet n’existe pas (et par conséquent, aucune de ses méthodes et propriétés n’est disponible).</span><span class="sxs-lookup"><span data-stu-id="7760e-107">The MSApp object only exists in the local context of an HTML document in a Windows app loaded via the ms-appx URI scheme; otherwise, the object doesn't exist (and consequently, none of its methods and properties are available).</span></span>  

<span data-ttu-id="7760e-108">Il fournit des fonctions d’aide qui vous permettent de créer des objets [Blob](https://developer.mozilla.org/docs/Web/API/Blob) et [MSStream.](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="7760e-108">It provides helper functions that enable you to create [Blob](https://developer.mozilla.org/docs/Web/API/Blob) and [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) objects.</span></span>  

```javascript
var result = MSApp.method;
```  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="7760e-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7760e-109">Methods</span></span>](#msapp-methods)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="7760e-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).</span><span class="sxs-lookup"><span data-stu-id="7760e-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="7760e-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="7760e-111">Constants</span></span>](#msapp-constants)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="7760e-112">[current](#current), [high](#high), [idle](#idle), [normal](#normal).</span><span class="sxs-lookup"><span data-stu-id="7760e-112">[current](#current), [high](#high), [idle](#idle), [normal](#normal).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="7760e-113">Interface MSAppAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="7760e-113">MSAppAsyncOperation interface</span></span>](#msappasyncoperation)  
   :::column-end:::
   :::column span="2":::
      [<span data-ttu-id="7760e-114">start</span><span class="sxs-lookup"><span data-stu-id="7760e-114">start</span></span>](#start)  
   :::column-end:::
:::row-end:::  

## <a name="msapp-methods"></a><span data-ttu-id="7760e-115">Méthodes MSApp</span><span class="sxs-lookup"><span data-stu-id="7760e-115">MSApp methods</span></span>  

### <a name="cleartemporarywebdataasync"></a><span data-ttu-id="7760e-116">clearTemporaryWebDataAsync</span><span class="sxs-lookup"><span data-stu-id="7760e-116">clearTemporaryWebDataAsync</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="7760e-117">Clears cache and indexedDB data for the app or [WebView](../../hosting/webview/index.md).</span><span class="sxs-lookup"><span data-stu-id="7760e-117">Clears cache and indexedDB data for the app or [WebView](../../hosting/webview/index.md).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.clearTemporaryWebDataAsync(#); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-118">Parameters</span><span class="sxs-lookup"><span data-stu-id="7760e-118">Parameters</span></span>**  
      
      <span data-ttu-id="7760e-119">Cette méthode ne possède aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7760e-119">This method has no parameters.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7760e-120">Return value</span></span>**  
      
      <span data-ttu-id="7760e-121">Type : [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)</span><span class="sxs-lookup"><span data-stu-id="7760e-121">Type: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)</span></span>  
      
      <span data-ttu-id="7760e-122">Représente une action asynchrone.</span><span class="sxs-lookup"><span data-stu-id="7760e-122">Represents an asynchronous action.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-123">Exceptions</span><span class="sxs-lookup"><span data-stu-id="7760e-123">Exceptions</span></span>**  
      
      <span data-ttu-id="7760e-124">Aucune.</span><span class="sxs-lookup"><span data-stu-id="7760e-124">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="7760e-125">Remarks</span></span>**  
      
      <span data-ttu-id="7760e-126">Aucune.</span><span class="sxs-lookup"><span data-stu-id="7760e-126">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="7760e-127">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createblobfromrandomaccessstream"></a><span data-ttu-id="7760e-128">createBlobFromRandomAccessStream</span><span class="sxs-lookup"><span data-stu-id="7760e-128">createBlobFromRandomAccessStream</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="7760e-129">Crée un [objet Blob](https://developer.mozilla.org/docs/Web/API/Blob) à partir d’un [objet IRandomAccessStream.](/uwp/api/Windows.Storage.Streams.IRandomAccessStream)</span><span class="sxs-lookup"><span data-stu-id="7760e-129">Creates a [Blob](https://developer.mozilla.org/docs/Web/API/Blob) from an [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) object.</span></span>  <span data-ttu-id="7760e-130">Cette méthode doit être utilisée lorsque vous traitez des objets dans des applications afin de créer un objet `IRandomAccessStream` W3C à partir du flux.</span><span class="sxs-lookup"><span data-stu-id="7760e-130">This method should be used when dealing with `IRandomAccessStream` objects in apps in order to create a W3C based object from the stream.</span></span>  <span data-ttu-id="7760e-131">Une fois l’objet blob créé, il peut être utilisé avec [les API FileReader,](https://developer.mozilla.org/docs/Web/API/FileReader) [URL](https://developer.mozilla.org/docs/Web/API/URL)et [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).</span><span class="sxs-lookup"><span data-stu-id="7760e-131">Once the blob is created, it can be used with the [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [URL APIs](https://developer.mozilla.org/docs/Web/API/URL), and [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-132">Parameters</span><span class="sxs-lookup"><span data-stu-id="7760e-132">Parameters</span></span>**  
      
      `type` <span data-ttu-id="7760e-133">[in]</span><span class="sxs-lookup"><span data-stu-id="7760e-133">[in]</span></span>  
      
      | <span data-ttu-id="7760e-134">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-134">Type</span></span> | <span data-ttu-id="7760e-135">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-135">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-136">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7760e-136">String</span></span> | <span data-ttu-id="7760e-137">Type de contenu des données.</span><span class="sxs-lookup"><span data-stu-id="7760e-137">Content type of the data.</span></span>  <span data-ttu-id="7760e-138">Cette chaîne doit être au format spécifié dans le jeton de type multimédia défini dans la section 3.7 de la RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="7760e-138">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>  |  
      
      `stream` <span data-ttu-id="7760e-139">[in]</span><span class="sxs-lookup"><span data-stu-id="7760e-139">[in]</span></span>  
      
      | <span data-ttu-id="7760e-140">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-140">Type</span></span> | <span data-ttu-id="7760e-141">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-141">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-142">Indifférent</span><span class="sxs-lookup"><span data-stu-id="7760e-142">Any</span></span> | <span data-ttu-id="7760e-143">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) à stocker dans l’objet Blob.</span><span class="sxs-lookup"><span data-stu-id="7760e-143">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) to be stored in the Blob.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-144">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7760e-144">Return value</span></span>**  
      
      | <span data-ttu-id="7760e-145">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-145">Type</span></span> | <span data-ttu-id="7760e-146">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-146">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-147">Blob</span><span class="sxs-lookup"><span data-stu-id="7760e-147">Blob</span></span> | <span data-ttu-id="7760e-148">Nouvel objet blob qui contient le flux.</span><span class="sxs-lookup"><span data-stu-id="7760e-148">New blob object that contains the stream.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-149">Exceptions</span><span class="sxs-lookup"><span data-stu-id="7760e-149">Exceptions</span></span>**  
      
      | <span data-ttu-id="7760e-150">Exception</span><span class="sxs-lookup"><span data-stu-id="7760e-150">Exception</span></span> | <span data-ttu-id="7760e-151">Condition</span><span class="sxs-lookup"><span data-stu-id="7760e-151">Condition</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-152">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="7760e-152">TypeMismatchError</span></span> | <span data-ttu-id="7760e-153">Le type de nœud est incompatible avec le type de paramètre attendu.</span><span class="sxs-lookup"><span data-stu-id="7760e-153">The node type is incompatible with the expected parameter type.</span></span>  <span data-ttu-id="7760e-154">Pour les versions antérieures à Internet Explorer 10, TYPE_MISMATCH_ERR est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="7760e-154">For versions earlier than Internet Explorer 10, TYPE_MISMATCH_ERR is returned.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-155">Remarques</span><span class="sxs-lookup"><span data-stu-id="7760e-155">Remarks</span></span>**  
      
      <span data-ttu-id="7760e-156">Crée un objet Blob à partir de types Windows Runtime via l’espace de noms MSApp sur l’objet fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7760e-156">Creates a Blob from Windows Runtime types via the MSApp namespace on the window object.</span></span>  <span data-ttu-id="7760e-157">Cette méthode crée un blob qui est essentiellement un wrapper clair sur l’objet [RandomAccessStream](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) qui lui est fourni.</span><span class="sxs-lookup"><span data-stu-id="7760e-157">This method will create a blob that is essentially a light wrapper over the [RandomAccessStream](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) object provided to it.</span></span>  <span data-ttu-id="7760e-158">Le blob est propriétaire de la durée de vie de ce flux et le flux est fermé lorsque l’objet blob est détruit.</span><span class="sxs-lookup"><span data-stu-id="7760e-158">The blob owns the lifetime of this stream and the stream will be closed when the blob is destroyed.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-159">Exemple</span><span class="sxs-lookup"><span data-stu-id="7760e-159">Example</span></span>**  
      
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

### <a name="createdatapackage"></a><span data-ttu-id="7760e-160">createDataPackage</span><span class="sxs-lookup"><span data-stu-id="7760e-160">createDataPackage</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="7760e-161">Convertit la plage spécifiée de l’utilisateur ou de l’application en fragment HTML qui peut être partagé.</span><span class="sxs-lookup"><span data-stu-id="7760e-161">Converts the user's or the application's specified range to an HTML fragment that can be shared.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackage(object); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-162">Parameters</span><span class="sxs-lookup"><span data-stu-id="7760e-162">Parameters</span></span>**  
      
      `object` <span data-ttu-id="7760e-163">[in]</span><span class="sxs-lookup"><span data-stu-id="7760e-163">[in]</span></span>  
      
      | <span data-ttu-id="7760e-164">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-164">Type</span></span> | <span data-ttu-id="7760e-165">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-165">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-166">Indifférent</span><span class="sxs-lookup"><span data-stu-id="7760e-166">Any</span></span> | <span data-ttu-id="7760e-167">Cette plage peut être créée à partir d’un objet de sélection, par exemple `window.selection.getRangeAt(0)` : ou manuellement.</span><span class="sxs-lookup"><span data-stu-id="7760e-167">This range can be created either from a selection object, for example: `window.selection.getRangeAt(0)`, or manually.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-168">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7760e-168">Return value</span></span>**  
      
      | <span data-ttu-id="7760e-169">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-169">Type</span></span> | <span data-ttu-id="7760e-170">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-170">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-171">Indifférent</span><span class="sxs-lookup"><span data-stu-id="7760e-171">Any</span></span> | <span data-ttu-id="7760e-172">Contient le code HTML de la plage spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7760e-172">Contains the HTML markup for the specified range.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-173">Exceptions</span><span class="sxs-lookup"><span data-stu-id="7760e-173">Exceptions</span></span>**  
      
      <span data-ttu-id="7760e-174">Aucune.</span><span class="sxs-lookup"><span data-stu-id="7760e-174">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-175">Remarques</span><span class="sxs-lookup"><span data-stu-id="7760e-175">Remarks</span></span>**  
      
      <span data-ttu-id="7760e-176">Cette méthode prend uniquement [en charge la plage DOM (Document Object Model),](https://developer.mozilla.org/docs/Web/API/Range)et non [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span><span class="sxs-lookup"><span data-stu-id="7760e-176">This method supports only [Document Object Model (DOM) Range](https://developer.mozilla.org/docs/Web/API/Range), not [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span></span>  <span data-ttu-id="7760e-177">Le package de données renvoyé pour la plage spécifiée contient du code HTML au format Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="7760e-177">The returned data package for the specified range contains HTML markup in clipboard format.</span></span>  
      
      <span data-ttu-id="7760e-178">Il n’existe aucune propriété disponible pour le package de données renvoyé.</span><span class="sxs-lookup"><span data-stu-id="7760e-178">There are no available properties for the returned data package.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-179">Exemple</span><span class="sxs-lookup"><span data-stu-id="7760e-179">Example</span></span>**  
      
      <span data-ttu-id="7760e-180">Aucune.</span><span class="sxs-lookup"><span data-stu-id="7760e-180">None.</span></span>  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createdatapackagefromselection"></a><span data-ttu-id="7760e-181">createDataPackageFromSelection</span><span class="sxs-lookup"><span data-stu-id="7760e-181">createDataPackageFromSelection</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="7760e-182">Convertit la sélection de l’utilisateur ou de l’application en fragment HTML qui peut être partagé.</span><span class="sxs-lookup"><span data-stu-id="7760e-182">Converts the user's or the application's selection to an HTML fragment that can be shared.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackageFromSelection(); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-183">Parameters</span><span class="sxs-lookup"><span data-stu-id="7760e-183">Parameters</span></span>**  
      
      <span data-ttu-id="7760e-184">Cette méthode ne possède aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7760e-184">This method has no parameters.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-185">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7760e-185">Return value</span></span>**  
      
      | <span data-ttu-id="7760e-186">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-186">Type</span></span> | <span data-ttu-id="7760e-187">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-187">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-188">Indifférent</span><span class="sxs-lookup"><span data-stu-id="7760e-188">Any</span></span> | <span data-ttu-id="7760e-189">Contient le code HTML de la plage spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7760e-189">Contains the HTML markup for the specified range.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-190">Exceptions</span><span class="sxs-lookup"><span data-stu-id="7760e-190">Exceptions</span></span>**  
      
      <span data-ttu-id="7760e-191">Aucune.</span><span class="sxs-lookup"><span data-stu-id="7760e-191">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-192">Remarques</span><span class="sxs-lookup"><span data-stu-id="7760e-192">Remarks</span></span>**  
      
      <span data-ttu-id="7760e-193">Le package de données renvoyé pour la sélection contient le code HTML au format Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="7760e-193">The returned data package for the selection contains HTML markup in clipboard format.</span></span>  <span data-ttu-id="7760e-194">S’il n’y a aucune sélection d’utilisateur dans l’interface utilisateur de l’application, le `createDataPackageFromSelection` retour `null` est fait.</span><span class="sxs-lookup"><span data-stu-id="7760e-194">If there is no user selection anywhere within the application's UI, the `createDataPackageFromSelection` returns `null`.</span></span>  
      
      <span data-ttu-id="7760e-195">Il n’existe aucune propriété disponible pour le package de données renvoyé.</span><span class="sxs-lookup"><span data-stu-id="7760e-195">There are no available properties for the returned data package.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-196">Exemple</span><span class="sxs-lookup"><span data-stu-id="7760e-196">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
 
### <a name="createfilefromstoragefile"></a><span data-ttu-id="7760e-197">createFileFromStorageFile</span><span class="sxs-lookup"><span data-stu-id="7760e-197">createFileFromStorageFile</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="7760e-198">Convertit un [fichier de stockage WinRT](/uwp/api/) [en](/uwp/api/windows.storage.storagefile) objet W3C [File](https://developer.mozilla.org/docs/Web/API/File) standard.</span><span class="sxs-lookup"><span data-stu-id="7760e-198">Converts a [WinRT](/uwp/api/) [StorageFile](/uwp/api/windows.storage.storagefile) to a standard W3C [File](https://developer.mozilla.org/docs/Web/API/File) object.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createFileFromStorageFile(storageFile); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-199">Parameters</span><span class="sxs-lookup"><span data-stu-id="7760e-199">Parameters</span></span>**  
      
      `storageFile` <span data-ttu-id="7760e-200">[in]</span><span class="sxs-lookup"><span data-stu-id="7760e-200">[in]</span></span>
      
      | <span data-ttu-id="7760e-201">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-201">Type</span></span> | <span data-ttu-id="7760e-202">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-202">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-203">Indifférent</span><span class="sxs-lookup"><span data-stu-id="7760e-203">Any</span></span> | <span data-ttu-id="7760e-204">Contient le fichier de stockage.</span><span class="sxs-lookup"><span data-stu-id="7760e-204">Contains the storage file.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-205">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7760e-205">Return value</span></span>**
      
      <span data-ttu-id="7760e-206">Aucun(e)</span><span class="sxs-lookup"><span data-stu-id="7760e-206">None</span></span>    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-207">Exceptions</span><span class="sxs-lookup"><span data-stu-id="7760e-207">Exceptions</span></span>**  
      
      | <span data-ttu-id="7760e-208">Exception</span><span class="sxs-lookup"><span data-stu-id="7760e-208">Exception</span></span> | <span data-ttu-id="7760e-209">Condition</span><span class="sxs-lookup"><span data-stu-id="7760e-209">Condition</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-210">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="7760e-210">TypeMismatchError</span></span> | <span data-ttu-id="7760e-211">La référence de fichier W3C spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7760e-211">The specified W3C file reference is invalid.</span></span>  <span data-ttu-id="7760e-212">Pour les versions antérieures à Internet Explorer 10, `TYPE_MISMATCH_ERR` est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="7760e-212">For versions earlier than Internet Explorer 10, `TYPE_MISMATCH_ERR` is returned.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-213">Remarques</span><span class="sxs-lookup"><span data-stu-id="7760e-213">Remarks</span></span>**  
      
      <span data-ttu-id="7760e-214">Aucune.</span><span class="sxs-lookup"><span data-stu-id="7760e-214">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-215">Exemple</span><span class="sxs-lookup"><span data-stu-id="7760e-215">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createstreamfrominputstream"></a><span data-ttu-id="7760e-216">createStreamFromInputStream</span><span class="sxs-lookup"><span data-stu-id="7760e-216">createStreamFromInputStream</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="7760e-217">Crée un [flux MSStream](https://msdn.microsoft.com/library/hh772328) à partir d’un [flux d’entrée.](https://msdn.microsoft.com/library/hh772327)</span><span class="sxs-lookup"><span data-stu-id="7760e-217">Creates an [MSStream](https://msdn.microsoft.com/library/hh772328) from an [InputStream](https://msdn.microsoft.com/library/hh772327).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-218">Parameters</span><span class="sxs-lookup"><span data-stu-id="7760e-218">Parameters</span></span>**  
      
      `type` <span data-ttu-id="7760e-219">[in]</span><span class="sxs-lookup"><span data-stu-id="7760e-219">[in]</span></span>
      
      | <span data-ttu-id="7760e-220">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-220">Type</span></span> | <span data-ttu-id="7760e-221">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-221">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-222">DOMString</span><span class="sxs-lookup"><span data-stu-id="7760e-222">DOMString</span></span> | <span data-ttu-id="7760e-223">Type de contenu des données.</span><span class="sxs-lookup"><span data-stu-id="7760e-223">Content type of the data.</span></span>  <span data-ttu-id="7760e-224">Cette chaîne doit être au format spécifié dans le jeton de type multimédia défini dans la section 3.7 de la RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="7760e-224">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>  <span data-ttu-id="7760e-225">\([Voir les types MIME,]( https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) par `text/plain` `text/html` exemple, , `image/jpeg` , , , , , et ainsi de `image/png` `audio/mpeg` `audio/ogg` `audio/*` `video/mp4` suite\).</span><span class="sxs-lookup"><span data-stu-id="7760e-225">\([See MIME types,](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) such as `text/plain`, `text/html`, `image/jpeg`, `image/png`, `audio/mpeg`, `audio/ogg`, `audio/*`, `video/mp4`, and so on\).</span></span>  
      
      `inputStream` <span data-ttu-id="7760e-226">[in]</span><span class="sxs-lookup"><span data-stu-id="7760e-226">[in]</span></span>
      
      | <span data-ttu-id="7760e-227">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-227">Type</span></span> | <span data-ttu-id="7760e-228">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-228">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-229">Indifférent</span><span class="sxs-lookup"><span data-stu-id="7760e-229">Any</span></span> | <span data-ttu-id="7760e-230">[IInputStream](/uwp/api/Windows.Storage.Streams.IInputStream) à stocker dans `MSStream` le .</span><span class="sxs-lookup"><span data-stu-id="7760e-230">The [IInputStream](/uwp/api/Windows.Storage.Streams.IInputStream) to be stored in the `MSStream`.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-231">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7760e-231">Return value</span></span>**
      
      <span data-ttu-id="7760e-232">Aucune.</span><span class="sxs-lookup"><span data-stu-id="7760e-232">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-233">Exceptions</span><span class="sxs-lookup"><span data-stu-id="7760e-233">Exceptions</span></span>**  
      
      <span data-ttu-id="7760e-234">Aucune.</span><span class="sxs-lookup"><span data-stu-id="7760e-234">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-235">Remarques</span><span class="sxs-lookup"><span data-stu-id="7760e-235">Remarks</span></span>**  
      
      <span data-ttu-id="7760e-236">Cette méthode prend un type de contenu et la `IInputStream` référence.</span><span class="sxs-lookup"><span data-stu-id="7760e-236">This method takes a content-type, and the `IInputStream` reference.</span></span>  <span data-ttu-id="7760e-237">La méthode vérifie ensuite que la référence de flux transmise est une instance de type et, si ce n’est pas le `IInputStream` cas, elle le `DOMException TYPE_MISMATCH_ERR` fait.</span><span class="sxs-lookup"><span data-stu-id="7760e-237">The method then verifies that the stream reference passed in is an instance of type `IInputStream` and if not, throws `DOMException TYPE_MISMATCH_ERR`.</span></span>  <span data-ttu-id="7760e-238">Si aucune erreur ne se produit, `createStreamFromInputStream` crée `MSStream` un \(à partir de ses entrées\).</span><span class="sxs-lookup"><span data-stu-id="7760e-238">If no error occurs, `createStreamFromInputStream` creates an `MSStream` \(from its inputs\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-239">Exemple</span><span class="sxs-lookup"><span data-stu-id="7760e-239">Example</span></span>**  
      
      <span data-ttu-id="7760e-240">Un `IInputStream` peut être utilisé pour créer un `MSStream` .</span><span class="sxs-lookup"><span data-stu-id="7760e-240">An `IInputStream` can be used to create an `MSStream`.</span></span>  <span data-ttu-id="7760e-241">Tout comme les objets à usage seul, toutes les URL créées par sont révoquées la première fois qu’elles sont résolues par `MSStreams` `URL.createObjectURL` l’élément image.</span><span class="sxs-lookup"><span data-stu-id="7760e-241">As `MSStreams` are inherently one-time-use objects, all URLs created by `URL.createObjectURL` are revoked the first time it's resolved by the image element.</span></span>  <span data-ttu-id="7760e-242">En outre, les demandes pour une deuxième URL sur cet objet après l’utilisation du flux échoueront.</span><span class="sxs-lookup"><span data-stu-id="7760e-242">Additionally, requests for a second URL on this object after the stream has been used will fail.</span></span>  
      
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

### <a name="execasyncatpriority"></a><span data-ttu-id="7760e-243">execAsyncAtPriority</span><span class="sxs-lookup"><span data-stu-id="7760e-243">execAsyncAtPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="7760e-244">Planifier l’exécution d’un rappel ultérieurement en fonction de la priorité donnée.</span><span class="sxs-lookup"><span data-stu-id="7760e-244">Schedules a callback to be executed at a later time according to the given priority.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-245">Parameters</span><span class="sxs-lookup"><span data-stu-id="7760e-245">Parameters</span></span>**  
      
      `asynchronousCallback` <span data-ttu-id="7760e-246">[in]</span><span class="sxs-lookup"><span data-stu-id="7760e-246">[in]</span></span>
      
      | <span data-ttu-id="7760e-247">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-247">Type</span></span> | <span data-ttu-id="7760e-248">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-248">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-249">Fonction</span><span class="sxs-lookup"><span data-stu-id="7760e-249">Function</span></span> | <span data-ttu-id="7760e-250">Fonction de rappel à exécuter de manière asynchrone, répartie selon la priorité donnée.</span><span class="sxs-lookup"><span data-stu-id="7760e-250">The callback function to run asynchronously, dispatched at the given priority priority.</span></span>  |  
      
      `priority` <span data-ttu-id="7760e-251">[in]</span><span class="sxs-lookup"><span data-stu-id="7760e-251">[in]</span></span>
      
      | <span data-ttu-id="7760e-252">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-252">Type</span></span> | <span data-ttu-id="7760e-253">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-253">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-254">DOMString</span><span class="sxs-lookup"><span data-stu-id="7760e-254">DOMString</span></span> | <span data-ttu-id="7760e-255">Valeur de priorité contextuelle à laquelle le rappel asynchroneCallback est exécuté.</span><span class="sxs-lookup"><span data-stu-id="7760e-255">The contextual priority value at which the asynchronousCallback callback is run.</span></span>  <span data-ttu-id="7760e-256">Voir [les constantes MSApp.](#msapp-constants)</span><span class="sxs-lookup"><span data-stu-id="7760e-256">See [MSApp Constants](#msapp-constants).</span></span>  |  
      
      `args` <span data-ttu-id="7760e-257">[in]</span><span class="sxs-lookup"><span data-stu-id="7760e-257">[in]</span></span>
      
      | <span data-ttu-id="7760e-258">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-258">Type</span></span> | <span data-ttu-id="7760e-259">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-259">Description</span></span> |  
      |:---- |:--- |   
      | <span data-ttu-id="7760e-260">Indifférent</span><span class="sxs-lookup"><span data-stu-id="7760e-260">Any</span></span> | <span data-ttu-id="7760e-261">Série facultative d’arguments transmis à la fonction de rappel SynchronousCallback \(en tant que paramètres 1 et ainsi de suite\).</span><span class="sxs-lookup"><span data-stu-id="7760e-261">An optional series of arguments that are passed to the synchronousCallback callback function \(as parameters 1 and so on\).</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-262">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7760e-262">Return value</span></span>**  
      
      <span data-ttu-id="7760e-263">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7760e-263">This method does not return a value.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-264">Exceptions</span><span class="sxs-lookup"><span data-stu-id="7760e-264">Exceptions</span></span>**  
      
      <span data-ttu-id="7760e-265">Aucune.</span><span class="sxs-lookup"><span data-stu-id="7760e-265">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-266">Remarques</span><span class="sxs-lookup"><span data-stu-id="7760e-266">Remarks</span></span>**  
      
      <span data-ttu-id="7760e-267">La fonction de rappel fournie est exécutée de manière `asynchronousCallback` asynchrone ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="7760e-267">The provided `asynchronousCallback` callback function is executed asynchronously later.</span></span>  `asynchronousCallback` <span data-ttu-id="7760e-268">sera distribué en fonction de la priorité fournie.</span><span class="sxs-lookup"><span data-stu-id="7760e-268">will be dispatched according to the provided priority.</span></span>  <span data-ttu-id="7760e-269">La priorité normale équivaut à la méthode [setImmediate](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) existante.</span><span class="sxs-lookup"><span data-stu-id="7760e-269">Normal priority is equivalent to the existing [setImmediate](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) method.</span></span>  <span data-ttu-id="7760e-270">Lorsque le rappel est exécuté, la priorité contextuelle actuelle est définie sur la valeur de paramètre de priorité fournie pour la durée de l’exécution du rappel.</span><span class="sxs-lookup"><span data-stu-id="7760e-270">When the callback is run, the current contextual priority is set to the provided priority parameter value for the duration of the callback's execution.</span></span>  
      
      <span data-ttu-id="7760e-271">Le `asynchronousCallback` paramètre de rappel peut être n’importe quelle fonction.</span><span class="sxs-lookup"><span data-stu-id="7760e-271">The `asynchronousCallback` callback parameter can be any function.</span></span>  <span data-ttu-id="7760e-272">Si des arguments sont fournis après le paramètre, ils sont tous transmis `priority` à la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="7760e-272">If arguments are provided after the `priority` parameter, they will all be passed to the callback function.</span></span>  
      
      <span data-ttu-id="7760e-273">Contrairement à , tout objet renvoyé par la fonction de rappel `execAtPriority` `asynchronousCallback` est ignoré \(et n’est pas renvoyé via `execAsyncAtPriority` \).</span><span class="sxs-lookup"><span data-stu-id="7760e-273">Unlike `execAtPriority`, any object returned by the `asynchronousCallback` callback function is ignored \(and not returned via `execAsyncAtPriority`\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-274">Exemple</span><span class="sxs-lookup"><span data-stu-id="7760e-274">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="execatpriority"></a><span data-ttu-id="7760e-275">execAtPriority</span><span class="sxs-lookup"><span data-stu-id="7760e-275">execAtPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="7760e-276">Exécute la fonction de rappel spécifiée à la priorité contextuelle donnée.</span><span class="sxs-lookup"><span data-stu-id="7760e-276">Runs the specified callback function at the given contextual priority.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-277">Parameters</span><span class="sxs-lookup"><span data-stu-id="7760e-277">Parameters</span></span>**  
      
      `synchronousCallback` <span data-ttu-id="7760e-278">[in]</span><span class="sxs-lookup"><span data-stu-id="7760e-278">[in]</span></span>  
      
      | <span data-ttu-id="7760e-279">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-279">Type</span></span> | <span data-ttu-id="7760e-280">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-280">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-281">Fonction</span><span class="sxs-lookup"><span data-stu-id="7760e-281">Function</span></span> | <span data-ttu-id="7760e-282">Fonction de rappel à exécuter de manière synchrone selon la priorité donnée.</span><span class="sxs-lookup"><span data-stu-id="7760e-282">The callback function to run synchronously at the given priority contextual priority.</span></span>  |  
      
      `priority` <span data-ttu-id="7760e-283">[in]</span><span class="sxs-lookup"><span data-stu-id="7760e-283">[in]</span></span>  
      
      | <span data-ttu-id="7760e-284">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-284">Type</span></span> | <span data-ttu-id="7760e-285">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-285">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-286">DOMString</span><span class="sxs-lookup"><span data-stu-id="7760e-286">DOMString</span></span> | <span data-ttu-id="7760e-287">Valeur de priorité spécifiée à laquelle la valeur de priorité contextuelle actuelle sera définie lors de l’exécution de la fonction `synchronousCallback` de rappel.</span><span class="sxs-lookup"><span data-stu-id="7760e-287">The specified priority value to which the current contextual priority value will be set when running the `synchronousCallback` callback function.</span></span>  <span data-ttu-id="7760e-288">Voir [les constantes MSApp.](#msapp-constants)</span><span class="sxs-lookup"><span data-stu-id="7760e-288">See [MSApp Constants](#msapp-constants).</span></span>  |  
      
      `args` <span data-ttu-id="7760e-289">[in]</span><span class="sxs-lookup"><span data-stu-id="7760e-289">[in]</span></span>  
      
      | <span data-ttu-id="7760e-290">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-290">Type</span></span> | <span data-ttu-id="7760e-291">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-291">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-292">Indifférent</span><span class="sxs-lookup"><span data-stu-id="7760e-292">Any</span></span> | <span data-ttu-id="7760e-293">Série facultative d’arguments transmis à la fonction de rappel \(en tant que `synchronousCallback` paramètres 1 et ainsi de suite\).</span><span class="sxs-lookup"><span data-stu-id="7760e-293">An optional series of arguments that are passed to the `synchronousCallback` callback function \(as parameters 1 and so on\).</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-294">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7760e-294">Return value</span></span>**  
      
      | <span data-ttu-id="7760e-295">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-295">Type</span></span> | <span data-ttu-id="7760e-296">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-296">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-297">Indifférent</span><span class="sxs-lookup"><span data-stu-id="7760e-297">Any</span></span> | <span data-ttu-id="7760e-298">Renvoie la valeur de retour du `synchronousCallback` rappel \(le cas échéant\).</span><span class="sxs-lookup"><span data-stu-id="7760e-298">Returns the return value of the `synchronousCallback` callback \(as applicable\).</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-299">Exceptions</span><span class="sxs-lookup"><span data-stu-id="7760e-299">Exceptions</span></span>**  
      
      <span data-ttu-id="7760e-300">Aucune.</span><span class="sxs-lookup"><span data-stu-id="7760e-300">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-301">Remarques</span><span class="sxs-lookup"><span data-stu-id="7760e-301">Remarks</span></span>**  
      
      <span data-ttu-id="7760e-302">La méthode de `synchronousCallback` rappel fournie est exécuté de manière synchrone.</span><span class="sxs-lookup"><span data-stu-id="7760e-302">The provided `synchronousCallback` callback method is execute synchronously.</span></span>  <span data-ttu-id="7760e-303">La priorité contextuelle actuelle est modifiée en valeur de priorité fournie (donnée par l’argument de priorité) pour la durée de la fonction de rappel fournie.</span><span class="sxs-lookup"><span data-stu-id="7760e-303">The current contextual priority is changed to the provided priority value (given by the priority argument) for the duration of the provided callback function.</span></span>  <span data-ttu-id="7760e-304">Une fois l’exécution de la fonction de rappel exécutée, la priorité est renvoyée à la valeur précédente avant `execAtPriority` l’appel.</span><span class="sxs-lookup"><span data-stu-id="7760e-304">Once the callback function finishes executing, priority is returned to the previous value prior to the `execAtPriority` call.</span></span>  <span data-ttu-id="7760e-305">La valeur de retour est la valeur de retour de la méthode de rappel `execAtPriority` \(tel que fourni\).</span><span class="sxs-lookup"><span data-stu-id="7760e-305">The return value from `execAtPriority` is the return value of the callback method \(as provided\).</span></span>  
      
      <span data-ttu-id="7760e-306">Le `synchronousCallback` paramètre de rappel peut être n’importe quelle fonction.</span><span class="sxs-lookup"><span data-stu-id="7760e-306">The `synchronousCallback` callback parameter can be any function.</span></span>  <span data-ttu-id="7760e-307">Si des arguments sont fournis après le paramètre de priorité, ils sont transmis à la méthode de rappel fournie.</span><span class="sxs-lookup"><span data-stu-id="7760e-307">If any arguments are provided after the priority parameter, they will be passed to the provided callback method.</span></span>  <span data-ttu-id="7760e-308">Si le paramètre de rappel renvoie une valeur, cette valeur devient également la valeur de `execAtPriority` retour.</span><span class="sxs-lookup"><span data-stu-id="7760e-308">If the callback parameter returns a value, this value becomes the return value for `execAtPriority` as well.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-309">Exemple</span><span class="sxs-lookup"><span data-stu-id="7760e-309">Example</span></span>**  
      
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

### <a name="getcurrentpriority"></a><span data-ttu-id="7760e-310">getCurrentPriority</span><span class="sxs-lookup"><span data-stu-id="7760e-310">getCurrentPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="7760e-311">Renvoie la priorité contextuelle actuelle.</span><span class="sxs-lookup"><span data-stu-id="7760e-311">Returns the current contextual priority.</span></span>  

   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getCurrentPriority();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-312">Parameters</span><span class="sxs-lookup"><span data-stu-id="7760e-312">Parameters</span></span>**  
      
      <span data-ttu-id="7760e-313">Aucune.</span><span class="sxs-lookup"><span data-stu-id="7760e-313">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-314">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7760e-314">Return value</span></span>**  
      
      | <span data-ttu-id="7760e-315">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-315">Type</span></span> | <span data-ttu-id="7760e-316">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-316">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-317">DOMString</span><span class="sxs-lookup"><span data-stu-id="7760e-317">DOMString</span></span> | <span data-ttu-id="7760e-318">La valeur de retour est l’une des chaînes `MSApp.HIGH` `MSApp.NORMAL` , ou `MSApp.IDLE` .</span><span class="sxs-lookup"><span data-stu-id="7760e-318">The return value is one of the strings `MSApp.HIGH`, `MSApp.NORMAL`, or `MSApp.IDLE`.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-319">Exceptions</span><span class="sxs-lookup"><span data-stu-id="7760e-319">Exceptions</span></span>**  
      
      <span data-ttu-id="7760e-320">Aucune.</span><span class="sxs-lookup"><span data-stu-id="7760e-320">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-321">Remarques</span><span class="sxs-lookup"><span data-stu-id="7760e-321">Remarks</span></span>**  
      
      <span data-ttu-id="7760e-322">Cette méthode renvoie la priorité contextuelle actuelle \(voir [constantes MSApp](#msapp-constants)\), qui peut être modifiée via `execAtPriority` et `execAsyncAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="7760e-322">This method returns the current contextual priority \(see [MSApp Constants](#msapp-constants)\), which can be changed via `execAtPriority` and `execAsyncAtPriority`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-323">Exemple</span><span class="sxs-lookup"><span data-stu-id="7760e-323">Example</span></span>**  
      
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

### <a name="gethtmlprintdocumentsource"></a><span data-ttu-id="7760e-324">getHtmlPrintDocumentSource</span><span class="sxs-lookup"><span data-stu-id="7760e-324">getHtmlPrintDocumentSource</span></span>  

<span data-ttu-id="7760e-325">API synchrone qui a été dépréciée.</span><span class="sxs-lookup"><span data-stu-id="7760e-325">Synchronous API that has been deprecated.</span></span>  <span data-ttu-id="7760e-326">Pour Windows 10, voir `getHtmlPrintDocumentSourceAsync` .</span><span class="sxs-lookup"><span data-stu-id="7760e-326">For Windows 10, see `getHtmlPrintDocumentSourceAsync`.</span></span>  <span data-ttu-id="7760e-327">Pour les applications Windows 8 et 8.1, consultez l’entrée MSDN pour [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span><span class="sxs-lookup"><span data-stu-id="7760e-327">For Windows 8 and 8.1 apps, see the MSDN entry for [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span></span>  

### <a name="gethtmlprintdocumentsourceasync"></a><span data-ttu-id="7760e-328">getHtmlPrintDocumentSourceAsync</span><span class="sxs-lookup"><span data-stu-id="7760e-328">getHtmlPrintDocumentSourceAsync</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="7760e-329">Renvoie le contenu source à imprimer.</span><span class="sxs-lookup"><span data-stu-id="7760e-329">Returns the source content that is to be printed.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.getHtmlPrintDocumentSourceAsync(document);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-330">Parameters</span><span class="sxs-lookup"><span data-stu-id="7760e-330">Parameters</span></span>**  
      
      `htmlDoc` <span data-ttu-id="7760e-331">[in]</span><span class="sxs-lookup"><span data-stu-id="7760e-331">[in]</span></span>  
      
      | <span data-ttu-id="7760e-332">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-332">Type</span></span> | <span data-ttu-id="7760e-333">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-333">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-334">Document</span><span class="sxs-lookup"><span data-stu-id="7760e-334">Document</span></span> | <span data-ttu-id="7760e-335">Document HTML à imprimer.</span><span class="sxs-lookup"><span data-stu-id="7760e-335">The HTML document to be printed.</span></span>  <span data-ttu-id="7760e-336">Il peut s’agit du document racine, du document dans un iFrame, d’un fragment de document ou d’un document SVG.</span><span class="sxs-lookup"><span data-stu-id="7760e-336">This can be the root document, the document in an iframe, a document fragment, or a SVG document.</span></span>  <span data-ttu-id="7760e-337">N’ignorez pas que htmlDoc doit être un document, et non un élément.</span><span class="sxs-lookup"><span data-stu-id="7760e-337">Be aware that htmlDoc must be a document, not an element.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-338">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7760e-338">Return value</span></span>**
      
      <span data-ttu-id="7760e-339">Aucune.</span><span class="sxs-lookup"><span data-stu-id="7760e-339">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-340">Exceptions</span><span class="sxs-lookup"><span data-stu-id="7760e-340">Exceptions</span></span>**  
      
      <span data-ttu-id="7760e-341">Aucune.</span><span class="sxs-lookup"><span data-stu-id="7760e-341">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-342">Remarques</span><span class="sxs-lookup"><span data-stu-id="7760e-342">Remarks</span></span>**  
      
      <span data-ttu-id="7760e-343">Aucune.</span><span class="sxs-lookup"><span data-stu-id="7760e-343">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-344">Exemple1</span><span class="sxs-lookup"><span data-stu-id="7760e-344">Example 1</span></span>**  
      
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
      **<span data-ttu-id="7760e-345">Exemple2</span><span class="sxs-lookup"><span data-stu-id="7760e-345">Example 2</span></span>**  
      
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

### <a name="getviewid"></a><span data-ttu-id="7760e-346">getViewId</span><span class="sxs-lookup"><span data-stu-id="7760e-346">getViewId</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="7760e-347">Prise en charge de plusieurs fenêtres.</span><span class="sxs-lookup"><span data-stu-id="7760e-347">Support for multiple windows.</span></span>  
      
      > [!NOTE] 
      > <span data-ttu-id="7760e-348">Dans les applications UWP JavaScript Win8.1, plusieurs fenêtres étaient prise en charge à l’aide des API DOM MSApp qui sont désormais désapprouvées.</span><span class="sxs-lookup"><span data-stu-id="7760e-348">In Win8.1 JavaScript UWP apps supported multiple windows using MSApp DOM APIs which are now depricated.</span></span>  <span data-ttu-id="7760e-349">Pour Windows 10, utilisez `window.open` , et le nouveau `window` `MSApp.getViewId` .</span><span class="sxs-lookup"><span data-stu-id="7760e-349">For Windows 10, use `window.open`, `window`, and the new `MSApp.getViewId`.</span></span>  
      
      | <span data-ttu-id="7760e-350">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-350">Description</span></span> |<span data-ttu-id="7760e-351">Windows 10</span><span class="sxs-lookup"><span data-stu-id="7760e-351">Windows 10</span></span> | <span data-ttu-id="7760e-352">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7760e-352">Windows 8.1</span></span> |  
      |:---- |:---- |:--- |  
      | <span data-ttu-id="7760e-353">Créer une fenêtre</span><span class="sxs-lookup"><span data-stu-id="7760e-353">Create new window</span></span> | [<span data-ttu-id="7760e-354">window.open</span><span class="sxs-lookup"><span data-stu-id="7760e-354">window.open</span></span>](https://developer.mozilla.org/docs/Web/API/Window/open) | [<span data-ttu-id="7760e-355">MSApp.createNewView</span><span class="sxs-lookup"><span data-stu-id="7760e-355">MSApp.createNewView</span></span>](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
      |<span data-ttu-id="7760e-356">Nouvel objet window</span><span class="sxs-lookup"><span data-stu-id="7760e-356">New window object</span></span> | [<span data-ttu-id="7760e-357">fenêtre</span><span class="sxs-lookup"><span data-stu-id="7760e-357">window</span></span>](https://developer.mozilla.org/docs/Web/API/Window) |[<span data-ttu-id="7760e-358">MSAppView</span><span class="sxs-lookup"><span data-stu-id="7760e-358">MSAppView</span></span>](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getViewId(window); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-359">Parameters</span><span class="sxs-lookup"><span data-stu-id="7760e-359">Parameters</span></span>**  
      
      `window`
      
      | <span data-ttu-id="7760e-360">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-360">Type</span></span> | <span data-ttu-id="7760e-361">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-361">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-362">DOMString</span><span class="sxs-lookup"><span data-stu-id="7760e-362">DOMString</span></span> | <span data-ttu-id="7760e-363">Objet représentant une fenêtre contenant un document DOM.</span><span class="sxs-lookup"><span data-stu-id="7760e-363">An object representing a window containing a DOM document.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-364">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7760e-364">Return value</span></span>**  
      
      `viewId`
      
      | <span data-ttu-id="7760e-365">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-365">Type</span></span> | <span data-ttu-id="7760e-366">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-366">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-367">Nombre</span><span class="sxs-lookup"><span data-stu-id="7760e-367">Number</span></span> | <span data-ttu-id="7760e-368">Peut être utilisé avec les différentes [API Windows.UI.ViewManagement.ApplicationViewSwitcher.](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher)</span><span class="sxs-lookup"><span data-stu-id="7760e-368">Can be used with the various [Windows.UI.ViewManagement.ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-369">Exceptions</span><span class="sxs-lookup"><span data-stu-id="7760e-369">Exceptions</span></span>**  
      
      <span data-ttu-id="7760e-370">Aucune.</span><span class="sxs-lookup"><span data-stu-id="7760e-370">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-371">Remarques</span><span class="sxs-lookup"><span data-stu-id="7760e-371">Remarks</span></span>**  
      
      <span data-ttu-id="7760e-372">Utilisez [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) et [window](https://developer.mozilla.org/docs/Web/API/Window) pour créer de nouvelles fenêtres, puis pour interagir avec les API WinRT, ajoutez `MSApp.getViewId` l’API.</span><span class="sxs-lookup"><span data-stu-id="7760e-372">Use [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) and [window](https://developer.mozilla.org/docs/Web/API/Window) for creating new windows, but then to interact with WinRT APIs, add the `MSApp.getViewId` API.</span></span>  <span data-ttu-id="7760e-373">Elle prend un objet comme paramètre et renvoie un nombre qui peut être utilisé avec les différentes `window` `viewId` API [Windows.UI.ViewManagement.ApplicationViewSwitcher.](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher)</span><span class="sxs-lookup"><span data-stu-id="7760e-373">It takes a `window` object as a parameter and returns a `viewId` number that can be used with the various [Windows.UI.ViewManagement.ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span>  
      
      *   <span data-ttu-id="7760e-374">Retarder la visibilité</span><span class="sxs-lookup"><span data-stu-id="7760e-374">Delaying Visibility</span></span>  
          
          <span data-ttu-id="7760e-375">Les affichages dans WinRT démarrent normalement masqués et le développeur final utilise quelque chose comme pour afficher l’affichage une fois `TryShowAsStandaloneAsync` qu’il est entièrement préparé.</span><span class="sxs-lookup"><span data-stu-id="7760e-375">Views in WinRT normally start hidden and the end developer uses something like `TryShowAsStandaloneAsync` to display the view once it is fully prepared.</span></span>  <span data-ttu-id="7760e-376">Dans le monde web, affiche une fenêtre immédiatement et l’utilisateur final peut observer le chargement et `window.open` le rendu du contenu.</span><span class="sxs-lookup"><span data-stu-id="7760e-376">In the web world, `window.open` shows a window immediately and the end user can watch as content is loaded and rendered.</span></span>  <span data-ttu-id="7760e-377">Pour que vos nouvelles fenêtres agissent comme des vues dans WinRT et qu’ils ne s’affichent pas immédiatement, nous avons ajouté une `window.open` option.</span><span class="sxs-lookup"><span data-stu-id="7760e-377">To have your new windows act like views in WinRT and not display immediately we have added a `window.open` option.</span></span>  <span data-ttu-id="7760e-378">Par exemple:</span><span class="sxs-lookup"><span data-stu-id="7760e-378">For example:</span></span>  
          
          ```javascript
          let newWindow = window.open("https://example.com", null, "msHideView=yes");
          ```  
          
      *   <span data-ttu-id="7760e-379">Différences de fenêtre principale</span><span class="sxs-lookup"><span data-stu-id="7760e-379">Primary Window Differences</span></span>  
          
          <span data-ttu-id="7760e-380">La fenêtre principale initialement ouverte par le système d’exploitation agit différemment des fenêtres secondaires qu’elle ouvre :</span><span class="sxs-lookup"><span data-stu-id="7760e-380">The primary window that is initially opened by the OS acts differently than the secondary windows that it opens:</span></span>  
          
          | <span data-ttu-id="7760e-381">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-381">Description</span></span> | <span data-ttu-id="7760e-382">Principal</span><span class="sxs-lookup"><span data-stu-id="7760e-382">Primary</span></span> | <span data-ttu-id="7760e-383">Secondaire</span><span class="sxs-lookup"><span data-stu-id="7760e-383">Secondary</span></span> |  
          |:---- |:--- |:--- |  
          | <span data-ttu-id="7760e-384">window.open</span><span class="sxs-lookup"><span data-stu-id="7760e-384">window.open</span></span> | <span data-ttu-id="7760e-385">Autorisée</span><span class="sxs-lookup"><span data-stu-id="7760e-385">Allowed</span></span> | <span data-ttu-id="7760e-386">Non autorisé</span><span class="sxs-lookup"><span data-stu-id="7760e-386">Disallowed</span></span> |  
          | <span data-ttu-id="7760e-387">window.close</span><span class="sxs-lookup"><span data-stu-id="7760e-387">window.close</span></span> | <span data-ttu-id="7760e-388">Fermer l’application</span><span class="sxs-lookup"><span data-stu-id="7760e-388">Close app</span></span> | <span data-ttu-id="7760e-389">Fermer la fenêtre</span><span class="sxs-lookup"><span data-stu-id="7760e-389">Close window</span></span> |  
          | <span data-ttu-id="7760e-390">Restrictions de navigation</span><span class="sxs-lookup"><span data-stu-id="7760e-390">Navigation restrictions</span></span> | <span data-ttu-id="7760e-391">ACUR uniquement</span><span class="sxs-lookup"><span data-stu-id="7760e-391">ACUR only</span></span> | <span data-ttu-id="7760e-392">Aucune restriction</span><span class="sxs-lookup"><span data-stu-id="7760e-392">No restrictions</span></span> |  
          
         <!-- The restriction to not allow secondary windows to open could change in the future depending on [feedback](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).  -->  
      
      *   <span data-ttu-id="7760e-393">Restrictions de communication d’origine identique</span><span class="sxs-lookup"><span data-stu-id="7760e-393">Same Origin Communication Restrictions</span></span>  
          
          <span data-ttu-id="7760e-394">Il existe un problème technique difficile qui empêche la prise en charge appropriée des appels de script synchrones, de même origine, entre fenêtres.</span><span class="sxs-lookup"><span data-stu-id="7760e-394">There is a difficult technical issue preventing proper support for synchronous, same-origin, cross-window, script calls.</span></span>  <span data-ttu-id="7760e-395">Lorsque vous ouvrez une fenêtre de la même origine, le script d’une fenêtre est autorisé à appeler directement des fonctions dans l’autre fenêtre, et certains de ces appels échouent.</span><span class="sxs-lookup"><span data-stu-id="7760e-395">When you open a window that is same origin, script in one window is allowed to directly call functions in the other window, and some of these calls will fail.</span></span>  `postMessage` <span data-ttu-id="7760e-396">Les appels fonctionnent très bien et sont la façon recommandée d’y faire des choses si possible.</span><span class="sxs-lookup"><span data-stu-id="7760e-396">calls work just fine and is the recommended way to do things if possible.</span></span>  <span data-ttu-id="7760e-397">Des travaux sont en cours pour améliorer ce problème.</span><span class="sxs-lookup"><span data-stu-id="7760e-397">Work to improve this issue is in progress.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-398">Exemple</span><span class="sxs-lookup"><span data-stu-id="7760e-398">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
    
### <a name="istaskscheduledatpriorityorhigher"></a><span data-ttu-id="7760e-399">isTaskScheduledAtPriorityOrHigher</span><span class="sxs-lookup"><span data-stu-id="7760e-399">isTaskScheduledAtPriorityOrHigher</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="7760e-400">Renvoie une valeur boolé nationale indiquant s’il existe un travail en attente au niveau de priorité donné ou supérieur.</span><span class="sxs-lookup"><span data-stu-id="7760e-400">Returns a Boolean value indicating whether there is pending work at the given priority level or higher.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-401">Parameters</span><span class="sxs-lookup"><span data-stu-id="7760e-401">Parameters</span></span>**  
      
      `priority` <span data-ttu-id="7760e-402">[in]</span><span class="sxs-lookup"><span data-stu-id="7760e-402">[in]</span></span>
      
      | <span data-ttu-id="7760e-403">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-403">Type</span></span> | <span data-ttu-id="7760e-404">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-404">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-405">DOMString</span><span class="sxs-lookup"><span data-stu-id="7760e-405">DOMString</span></span> | <span data-ttu-id="7760e-406">Une valeur de priorité \(voir [constantes MSApp](#msapp-constants)\) spécifiant le niveau de priorité et au-dessus pour interroger tout travail en file d’attente en attente.</span><span class="sxs-lookup"><span data-stu-id="7760e-406">A priority value \(see [MSApp Constants](#msapp-constants)\) specifying the priority level and above to query for any outstanding queued work.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-407">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7760e-407">Return value</span></span>**  
      
      | <span data-ttu-id="7760e-408">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-408">Type</span></span> | <span data-ttu-id="7760e-409">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-409">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-410">Booléen</span><span class="sxs-lookup"><span data-stu-id="7760e-410">Boolean</span></span> | <span data-ttu-id="7760e-411">Renvoie s’il existe des travaux en file d’attente au niveau de priorité spécifié ou supérieur, dans `true` le `false` cas contraire.</span><span class="sxs-lookup"><span data-stu-id="7760e-411">Returns `true` if there is any queued work at the specified priority level or above, `false` otherwise.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-412">Exceptions</span><span class="sxs-lookup"><span data-stu-id="7760e-412">Exceptions</span></span>**  
      
      <span data-ttu-id="7760e-413">Aucune.</span><span class="sxs-lookup"><span data-stu-id="7760e-413">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-414">Remarques</span><span class="sxs-lookup"><span data-stu-id="7760e-414">Remarks</span></span>**  
      
      <span data-ttu-id="7760e-415">La méthode fournit un moyen pour le code JavaScript de déterminer s’il existe un travail en attente aux différents niveaux de priorité \(ou au-dessus\) dans l’intention que le code JavaScript appelant puisse ensuite décider de donner lieu à un travail `isTaskScheduledAtPriorityOrHigher` prioritaire.</span><span class="sxs-lookup"><span data-stu-id="7760e-415">The `isTaskScheduledAtPriorityOrHigher` method provides a means for JavaScript code to determine if there is pending work at the various priority levels \(or above\) with the intent that the calling JavaScript code can then decide to yield to higher priority work.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-416">Exemple</span><span class="sxs-lookup"><span data-stu-id="7760e-416">Example</span></span>**  
      
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

### <a name="pagehandlesallapplicationactivations"></a><span data-ttu-id="7760e-417">pageHandlesAllApplicationActivations</span><span class="sxs-lookup"><span data-stu-id="7760e-417">pageHandlesAllApplicationActivations</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="7760e-418">Permet d’éviter une actualisation du chemin d’accès de démarrage (rechargement de page) avant chaque événement d’activation \(par exemple, en cliquant sur une notification ou une vignette épinglée\).</span><span class="sxs-lookup"><span data-stu-id="7760e-418">Used to avoid a refresh of the start path (page reload) before every activate event \(such as clicking a notification or a pinned tile\).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.pageHandlesAllApplicationActivations(boolean);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-419">Parameters</span><span class="sxs-lookup"><span data-stu-id="7760e-419">Parameters</span></span>**  
      
      | <span data-ttu-id="7760e-420">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-420">Type</span></span> | <span data-ttu-id="7760e-421">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-421">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-422">Booléen</span><span class="sxs-lookup"><span data-stu-id="7760e-422">Boolean</span></span> | <span data-ttu-id="7760e-423">Utilisez cette fonction pour toujours ignorer l’actualisation du chemin d’accès de démarrage (rechargement de page) et passer directement au tir de `MSApp.pageHandlesAllApplicationActivations(true)` `WebUIApplication` l’événement activé.</span><span class="sxs-lookup"><span data-stu-id="7760e-423">Use `MSApp.pageHandlesAllApplicationActivations(true)` to always skip refreshing the start path (page reload) and instead jump straight to firing the `WebUIApplication` activated event.</span></span>  <span data-ttu-id="7760e-424">Nécessite que toutes les pages gèrent les événements d’activation séparément.</span><span class="sxs-lookup"><span data-stu-id="7760e-424">Requires that all pages handle activation events separately.</span></span>  <span data-ttu-id="7760e-425">En définissant cette méthode comme étant , le fait de cliquer sur un événement activé \(comme une notification\) ne déclenche pas le rechargement, ce qui est essentiel pour les applications mono-page qui souhaitent éviter les `true` rechargements de page.</span><span class="sxs-lookup"><span data-stu-id="7760e-425">By defining this method as `true`, clicking an activated event \(like a notification\) will not trigger the reload, an essential for single-page apps wishing to avoid page reloads.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-426">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7760e-426">Return value</span></span>**
      
      <span data-ttu-id="7760e-427">Aucune.</span><span class="sxs-lookup"><span data-stu-id="7760e-427">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-428">Exceptions</span><span class="sxs-lookup"><span data-stu-id="7760e-428">Exceptions</span></span>**  
      
      <span data-ttu-id="7760e-429">Aucune.</span><span class="sxs-lookup"><span data-stu-id="7760e-429">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-430">Remarques</span><span class="sxs-lookup"><span data-stu-id="7760e-430">Remarks</span></span>**  
      
      <span data-ttu-id="7760e-431">Aucune.</span><span class="sxs-lookup"><span data-stu-id="7760e-431">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-432">Exemple</span><span class="sxs-lookup"><span data-stu-id="7760e-432">Example</span></span>**  
      
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

### <a name="suppresssubdownloadcredentialprompts"></a><span data-ttu-id="7760e-433">suppressSubdownloadCredentialPrompts</span><span class="sxs-lookup"><span data-stu-id="7760e-433">suppressSubdownloadCredentialPrompts</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="7760e-434">Contrôle si une application supprime les invites d’authentification possibles pendant le téléchargement des ressources.</span><span class="sxs-lookup"><span data-stu-id="7760e-434">Controls whether an app suppresses possible authentication prompts during the download of resources.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.suppressSubdownloadCredentialPrompts(suppress);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-435">Parameters</span><span class="sxs-lookup"><span data-stu-id="7760e-435">Parameters</span></span>**  
     
      `suppress` <span data-ttu-id="7760e-436">[in]</span><span class="sxs-lookup"><span data-stu-id="7760e-436">[in]</span></span>
      
      | <span data-ttu-id="7760e-437">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-437">Type</span></span> | <span data-ttu-id="7760e-438">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-438">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-439">Booléen</span><span class="sxs-lookup"><span data-stu-id="7760e-439">Boolean</span></span> | <span data-ttu-id="7760e-440">La valeur true supprime les invites d’authentification potentielles.</span><span class="sxs-lookup"><span data-stu-id="7760e-440">A value of true suppresses potential authentication prompts.</span></span>  <span data-ttu-id="7760e-441">La valeur false ne supprime pas les invites d’authentification potentielles de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7760e-441">A value of false does not suppress any potential authentication prompts from the user.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-442">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7760e-442">Return value</span></span>**  
      
      <span data-ttu-id="7760e-443">Aucune.</span><span class="sxs-lookup"><span data-stu-id="7760e-443">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-444">Exceptions</span><span class="sxs-lookup"><span data-stu-id="7760e-444">Exceptions</span></span>**  
      
      <span data-ttu-id="7760e-445">Aucune.</span><span class="sxs-lookup"><span data-stu-id="7760e-445">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-446">Remarques</span><span class="sxs-lookup"><span data-stu-id="7760e-446">Remarks</span></span>**  
      
      <span data-ttu-id="7760e-447">La `suppressSubdownloadCredentialPrompts` méthode contrôle si une application supprime les invites d’authentification potentielles pendant le téléchargement des ressources.</span><span class="sxs-lookup"><span data-stu-id="7760e-447">The `suppressSubdownloadCredentialPrompts` method controls whether an app suppresses potential authentication prompts during the download of resources.</span></span>  <span data-ttu-id="7760e-448">Le comportement par défaut consiste à ne pas supprimer les invites d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="7760e-448">The default behavior is to not suppress credential prompts.</span></span>  
      
      `suppressSubdownloadCredentialPrompts` <span data-ttu-id="7760e-449">est destiné à être utilisé par les applications qui peuvent charger un nombre excessif de ressources nécessitant une authentification, telles qu’une application de messagerie \(qui peut contenir un bulletin contenant un certain nombre d’images où chaque image requiert une authentification\).</span><span class="sxs-lookup"><span data-stu-id="7760e-449">is intended for use by apps which may load an excessive number of resources that require authentication, such as a mail app \(which could contain a newsletter containing a number of images where each image requires authentication\).</span></span>  
      
      <span data-ttu-id="7760e-450">Lors de la suppression des invites d’informations d’identification, les boîtes de dialogue d’authentification sur les serveurs ne s’afficheront pas lors de l’accès aux ressources nécessitant une authentification et la ressource ne sera pas téléchargée.</span><span class="sxs-lookup"><span data-stu-id="7760e-450">When suppressing credential prompts, dialogs for authenticating to servers will not be shown when accessing resources that require authentication, and the resource will not be downloaded.</span></span>  <span data-ttu-id="7760e-451">Notez que cela n’a pas d’impact sur les autres invites possibles telles que l’authentification proxy ou les boîtes de dialogue de demande de certification du client, ni sur `suppressSubdownloadCredentialPrompts` XHR.</span><span class="sxs-lookup"><span data-stu-id="7760e-451">Note that `suppressSubdownloadCredentialPrompts` does not impact other possible prompts such as proxy authentication or client certification request dialogs, nor does it impact XHR.</span></span>  
      
      <span data-ttu-id="7760e-452">N’ignorez pas `suppressSubdownloadCredentialPrompts` que cela a un impact sur tout le contenu de l’application, y compris le contenu hébergé dans l’élément. `webview`</span><span class="sxs-lookup"><span data-stu-id="7760e-452">Be aware that `suppressSubdownloadCredentialPrompts` impacts all content in the application, including content hosted in the `webview` element.</span></span>  
      
      > [!IMPORTANT]
      > <span data-ttu-id="7760e-453">Les décisions relatives aux invites d’informations d’identification sont mises en cache.</span><span class="sxs-lookup"><span data-stu-id="7760e-453">Credential prompt decisions are cached.</span></span>  <span data-ttu-id="7760e-454">Par conséquent, bien que la suppression des invites d’informations d’identification prenne effet immédiatement, l’application des invites d’informations d’identification après leur suppression peut avoir besoin d’un rechargement du document pour prendre effet.</span><span class="sxs-lookup"><span data-stu-id="7760e-454">Therefore, while suppressing credential prompts will take effect immediately, allowing credential prompts after suppressing them may need a reload of the document to take effect.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-455">Exemple</span><span class="sxs-lookup"><span data-stu-id="7760e-455">Example</span></span>**  
      
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

### <a name="terminateapp"></a><span data-ttu-id="7760e-456">terminateApp</span><span class="sxs-lookup"><span data-stu-id="7760e-456">terminateApp</span></span>  


:::row:::
   :::column span="":::
      <span data-ttu-id="7760e-457">Met fin à l’application actuelle et génère un rapport d’échec.</span><span class="sxs-lookup"><span data-stu-id="7760e-457">Terminates the current application and generates a failure report.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.terminateApp(error);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-458">Parameters</span><span class="sxs-lookup"><span data-stu-id="7760e-458">Parameters</span></span>**  
      
      `error` <span data-ttu-id="7760e-459">[in]</span><span class="sxs-lookup"><span data-stu-id="7760e-459">[in]</span></span>
      
      | <span data-ttu-id="7760e-460">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-460">Type</span></span> | <span data-ttu-id="7760e-461">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-461">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-462">Erreur</span><span class="sxs-lookup"><span data-stu-id="7760e-462">Error</span></span> | <span data-ttu-id="7760e-463">Objet `Error` que vous pouvez utiliser pour décrire l’erreur qui a déclenché l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="7760e-463">An `Error` object that you can use to describe the error that triggered the termination.</span></span>  <span data-ttu-id="7760e-464">L’objet doit contenir le nombre, la description et les propriétés de pile ; un rapport d’échec ne sera pas généré si l’objet ne contient `Error` pas ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="7760e-464">The `Error` object must contain the number, description, and stack properties; a failure report won't be generated if the object doesn't contain these properties.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-465">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7760e-465">Return value</span></span>**
      
      <span data-ttu-id="7760e-466">Aucune.</span><span class="sxs-lookup"><span data-stu-id="7760e-466">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-467">Exceptions</span><span class="sxs-lookup"><span data-stu-id="7760e-467">Exceptions</span></span>**  
      
      <span data-ttu-id="7760e-468">Aucune.</span><span class="sxs-lookup"><span data-stu-id="7760e-468">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-469">Remarques</span><span class="sxs-lookup"><span data-stu-id="7760e-469">Remarks</span></span>**  
      
      <span data-ttu-id="7760e-470">Si le problème signalé par devient l’un des 5 principaux problèmes de votre application, il s’affiche sur la page Qualité de `terminateApp` l’application.</span><span class="sxs-lookup"><span data-stu-id="7760e-470">If the issue reported by `terminateApp` becomes one of your app's top 5 issues, it will show up on the app's Quality page.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-471">Exemple</span><span class="sxs-lookup"><span data-stu-id="7760e-471">Example</span></span>**  
      
      <span data-ttu-id="7760e-472">Cet exemple appelle `terminateApp` lorsqu’une exception est rencontrée.</span><span class="sxs-lookup"><span data-stu-id="7760e-472">This example calls `terminateApp` when an exception is encountered.</span></span>  <span data-ttu-id="7760e-473">Il utilise `Error` l’objet fourni lorsque vous capturez une exception.</span><span class="sxs-lookup"><span data-stu-id="7760e-473">It uses the `Error` object provided when you catch an exception.</span></span>  
      
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

### <a name="msapp-constants"></a><span data-ttu-id="7760e-474">Constantes MSApp</span><span class="sxs-lookup"><span data-stu-id="7760e-474">MSApp Constants</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="7760e-475">Valeurs de priorité autorisées `execAsyncAtPriority` associées `execAtPriority` à , et `getCurrentPriority` `isTaskScheduldAtPriorityOrHigher` .</span><span class="sxs-lookup"><span data-stu-id="7760e-475">Allowed priority values associated with `execAsyncAtPriority`, `execAtPriority`, `getCurrentPriority`, and `isTaskScheduldAtPriorityOrHigher`.</span></span>  
   :::column-end:::
   :::column span="":::
      #### <a name="current"></a><span data-ttu-id="7760e-476">Actuel</span><span class="sxs-lookup"><span data-stu-id="7760e-476">Current</span></span>  
      
      `current`  
      
      | <span data-ttu-id="7760e-477">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-477">Type</span></span> | <span data-ttu-id="7760e-478">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-478">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-479">DOMString</span><span class="sxs-lookup"><span data-stu-id="7760e-479">DOMString</span></span> | <span data-ttu-id="7760e-480">Lorsqu’elle est utilisée avec la méthode appropriée \(voir aussi section\), la méthode utilise la priorité contextuelle actuelle lors de l’exécution de `current` l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="7760e-480">When `current` is used with the appropriate method \(See also section\), the method will use the current contextual priority when executing the requested operation.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <a name="high"></a><span data-ttu-id="7760e-481">High</span><span class="sxs-lookup"><span data-stu-id="7760e-481">High</span></span>  
      
      `high`  
      
      | <span data-ttu-id="7760e-482">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-482">Type</span></span> | <span data-ttu-id="7760e-483">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-483">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-484">DOMString</span><span class="sxs-lookup"><span data-stu-id="7760e-484">DOMString</span></span> | <span data-ttu-id="7760e-485">Lorsqu’elle est utilisée avec la méthode appropriée \(voir aussi section\), la méthode utilise une priorité supérieure à la normale lors de l’exécution de l’opération demandée et l’exécute avant tout travail de priorité `high` normal existant.</span><span class="sxs-lookup"><span data-stu-id="7760e-485">When `high` is used with the appropriate method \(See also section\), the method will use higher than normal priority when executing the requested operation and will be dispatch the operation before any existing normal priority work.</span></span>  |  
   :::column-end:::
   :::column span="":::
      #### <a name="idle"></a><span data-ttu-id="7760e-486">Inactif</span><span class="sxs-lookup"><span data-stu-id="7760e-486">Idle</span></span>  
      
      `idle`  
      
      | <span data-ttu-id="7760e-487">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-487">Type</span></span> | <span data-ttu-id="7760e-488">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-488">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-489">DOMString</span><span class="sxs-lookup"><span data-stu-id="7760e-489">DOMString</span></span> | <span data-ttu-id="7760e-490">Lorsqu’elle est utilisée avec la méthode appropriée \(voir aussi section\), la méthode utilise une priorité inférieure à la normale lors de l’exécution de l’opération demandée et répartit l’opération après tout travail de priorité `ideal` normale existant.</span><span class="sxs-lookup"><span data-stu-id="7760e-490">When `ideal` is used with the appropriate method \(See also section\), the method will use lower than normal priority when executing the requested operation and will be dispatch the operation after any existing normal priority work.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <a name="normal"></a><span data-ttu-id="7760e-491">Normal</span><span class="sxs-lookup"><span data-stu-id="7760e-491">Normal</span></span>  
      
      `normal`  
      
      | <span data-ttu-id="7760e-492">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-492">Type</span></span> | <span data-ttu-id="7760e-493">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-493">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-494">DOMString</span><span class="sxs-lookup"><span data-stu-id="7760e-494">DOMString</span></span> | <span data-ttu-id="7760e-495">Lorsqu’elle est utilisée avec la méthode appropriée (voir aussi la section), la méthode utilise la priorité normale existante lors de l’exécution de `normal` l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="7760e-495">When `normal` is used with the appropriate method (See also section), the method will use the normal existing priority when executing the requested operation.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-496">Exemple</span><span class="sxs-lookup"><span data-stu-id="7760e-496">Example</span></span>**  
      
      ```javascript
      if (window.MSApp.CURRENT) {
          document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
      }
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-497">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7760e-497">Requirements</span></span>**  
      
      | <span data-ttu-id="7760e-498">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-498">Type</span></span> | <span data-ttu-id="7760e-499">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-499">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-500">IDL</span><span class="sxs-lookup"><span data-stu-id="7760e-500">IDL</span></span> | <span data-ttu-id="7760e-501">Mshtml.idl</span><span class="sxs-lookup"><span data-stu-id="7760e-501">Mshtml.idl</span></span> |  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

## <a name="msappasyncoperation"></a><span data-ttu-id="7760e-502">MSAppAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="7760e-502">MSAppAsyncOperation</span></span>  

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```  

### <a name="start"></a><span data-ttu-id="7760e-503">start</span><span class="sxs-lookup"><span data-stu-id="7760e-503">start</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="7760e-504">Démarre `MSAppAsyncOperation` le .</span><span class="sxs-lookup"><span data-stu-id="7760e-504">Starts the `MSAppAsyncOperation`.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSAppAsyncOperation.start();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="7760e-505">Parameters</span><span class="sxs-lookup"><span data-stu-id="7760e-505">Parameters</span></span>**  
      
      <span data-ttu-id="7760e-506">Aucune.</span><span class="sxs-lookup"><span data-stu-id="7760e-506">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="7760e-507">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7760e-507">Return value</span></span>**
      
      <span data-ttu-id="7760e-508">Aucune.</span><span class="sxs-lookup"><span data-stu-id="7760e-508">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      
      **<span data-ttu-id="7760e-509">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7760e-509">Properties</span></span>**  
      
      `error` <span data-ttu-id="7760e-510">property</span><span class="sxs-lookup"><span data-stu-id="7760e-510">property</span></span>  
      
      | <span data-ttu-id="7760e-511">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-511">Type</span></span> | <span data-ttu-id="7760e-512">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-512">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-513">DOMError</span><span class="sxs-lookup"><span data-stu-id="7760e-513">DOMError</span></span> | <span data-ttu-id="7760e-514">Représente une erreur dans `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="7760e-514">Represents an error in `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.error
      ```  
      
      `oncomplete` <span data-ttu-id="7760e-515">property</span><span class="sxs-lookup"><span data-stu-id="7760e-515">property</span></span>  
      
      | <span data-ttu-id="7760e-516">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-516">Type</span></span> | <span data-ttu-id="7760e-517">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-517">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-518">EventHandler</span><span class="sxs-lookup"><span data-stu-id="7760e-518">EventHandler</span></span> | <span data-ttu-id="7760e-519">Propriété pour la définition d’un handler d’événements à l’achèvement de `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="7760e-519">Property for setting an event handler on completion of `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.oncomplete
      ```  
      
      `onerror` <span data-ttu-id="7760e-520">property</span><span class="sxs-lookup"><span data-stu-id="7760e-520">property</span></span>  
      
      | <span data-ttu-id="7760e-521">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-521">Type</span></span> | <span data-ttu-id="7760e-522">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-522">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-523">EventHandler</span><span class="sxs-lookup"><span data-stu-id="7760e-523">EventHandler</span></span> | <span data-ttu-id="7760e-524">Propriété pour la définition d’un handler d’événements sur une erreur pendant `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="7760e-524">Property for setting an event handler upon an error during `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.onerror
      ```  
      
      `readyState` <span data-ttu-id="7760e-525">property</span><span class="sxs-lookup"><span data-stu-id="7760e-525">property</span></span>  
      
      | <span data-ttu-id="7760e-526">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-526">Type</span></span> | <span data-ttu-id="7760e-527">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-527">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-528">Nombre</span><span class="sxs-lookup"><span data-stu-id="7760e-528">Number</span></span> | <span data-ttu-id="7760e-529">Représente l’état de l’opération asynchrone dans l’application Windows à l’aide de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7760e-529">Represents the state of the asynchronous operation within the Windows app using JavaScript.</span></span>  <span data-ttu-id="7760e-530">Les valeurs sont `Started[0]` les suivantes : , `Completed[1]` , `Error[2]` .</span><span class="sxs-lookup"><span data-stu-id="7760e-530">Values include: `Started[0]`, `Completed[1]`, `Error[2]`.</span></span>  |  
      
      ```javascript
      p = object.readyState
      ```  
      
      `result` <span data-ttu-id="7760e-531">property</span><span class="sxs-lookup"><span data-stu-id="7760e-531">property</span></span>  
      
      | <span data-ttu-id="7760e-532">Type</span><span class="sxs-lookup"><span data-stu-id="7760e-532">Type</span></span> | <span data-ttu-id="7760e-533">Description</span><span class="sxs-lookup"><span data-stu-id="7760e-533">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="7760e-534">Indifférent</span><span class="sxs-lookup"><span data-stu-id="7760e-534">Any</span></span> |<span data-ttu-id="7760e-535">Représente le résultat de `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="7760e-535">Represents the result of `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.result
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
