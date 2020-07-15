---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2Environment
ms.openlocfilehash: 79bc9908d0fd12d4606311b959cbc6bc0c384c2d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878917"
---
# <span data-ttu-id="39eb9-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="39eb9-104">Microsoft.Web.WebView2.Core.CoreWebView2Environment class</span></span> 

<span data-ttu-id="39eb9-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="39eb9-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="39eb9-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="39eb9-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="39eb9-107">Il s’agit de l’environnement WebView2.</span><span class="sxs-lookup"><span data-stu-id="39eb9-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="39eb9-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="39eb9-108">Summary</span></span>

 <span data-ttu-id="39eb9-109">Ses</span><span class="sxs-lookup"><span data-stu-id="39eb9-109">Members</span></span>                        | <span data-ttu-id="39eb9-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="39eb9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="39eb9-111">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="39eb9-111">BrowserVersionString</span></span>](#browserversionstring) | <span data-ttu-id="39eb9-112">Les informations de la version du navigateur du CoreWebView2Environment actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.</span><span class="sxs-lookup"><span data-stu-id="39eb9-112">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="39eb9-113">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="39eb9-113">NewBrowserVersionAvailable</span></span>](#newbrowserversionavailable) | <span data-ttu-id="39eb9-114">L’événement NewBrowserVersionAvailable se déclenche lors de l’installation d’une nouvelle version du navigateur Edge et peut être utilisée via WebView2.</span><span class="sxs-lookup"><span data-stu-id="39eb9-114">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="39eb9-115">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="39eb9-115">CompareBrowserVersions</span></span>](#comparebrowserversions) | <span data-ttu-id="39eb9-116">Comparez les versions du navigateur correctement pour déterminer la version la plus récente, la plus ancienne ou la plus récente.</span><span class="sxs-lookup"><span data-stu-id="39eb9-116">Compare browser versions correctly to determine which version is newer, older or same.</span></span>
[<span data-ttu-id="39eb9-117">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="39eb9-117">CreateAsync</span></span>](#createasync) | <span data-ttu-id="39eb9-118">Crée un environnement WebView2 persistant à l’aide de la version latérale installée.</span><span class="sxs-lookup"><span data-stu-id="39eb9-118">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="39eb9-119">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="39eb9-119">CreateCoreWebView2CompositionControllerAsync</span></span>](#createcorewebview2compositioncontrollerasync) | <span data-ttu-id="39eb9-120">Créer de manière asynchrone un nouveau WebView à utiliser avec l’hébergement visuel.</span><span class="sxs-lookup"><span data-stu-id="39eb9-120">Asynchronously create a new WebView for use with visual hosting.</span></span>
[<span data-ttu-id="39eb9-121">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="39eb9-121">CreateCoreWebView2ControllerAsync</span></span>](#createcorewebview2controllerasync) | <span data-ttu-id="39eb9-122">Créer de manière asynchrone un nouveau WebView.</span><span class="sxs-lookup"><span data-stu-id="39eb9-122">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="39eb9-123">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="39eb9-123">CreateCoreWebView2PointerInfo</span></span>](#createcorewebview2pointerinfo) | <span data-ttu-id="39eb9-124">Créer un CoreWebView2ExperimentalPointerInfo vide.</span><span class="sxs-lookup"><span data-stu-id="39eb9-124">Create an empty CoreWebView2ExperimentalPointerInfo.</span></span>
[<span data-ttu-id="39eb9-125">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="39eb9-125">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="39eb9-126">Créer un objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="39eb9-126">Create a new web resource response object.</span></span>
[<span data-ttu-id="39eb9-127">GetAvailableBrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="39eb9-127">GetAvailableBrowserVersionString</span></span>](#getavailablebrowserversionstring) | <span data-ttu-id="39eb9-128">Obtenez les informations de la version du navigateur, y compris le nom du canal, s’il ne s’agit pas du canal stable ou du bord intégré.</span><span class="sxs-lookup"><span data-stu-id="39eb9-128">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>
[<span data-ttu-id="39eb9-129">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="39eb9-129">GetProviderForHwnd</span></span>](#getproviderforhwnd) | <span data-ttu-id="39eb9-130">Retourne le fournisseur UI Automation pour le CoreWebView2CompositionController correspondant au HWND donné.</span><span class="sxs-lookup"><span data-stu-id="39eb9-130">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

<span data-ttu-id="39eb9-131">Les webvues créées à partir d’un environnement s’exécutent sur le processus de navigateur spécifié avec des paramètres d’environnement et des objets créés à partir d’un environnement doivent être utilisés dans le même environnement.</span><span class="sxs-lookup"><span data-stu-id="39eb9-131">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="39eb9-132">Il n’est pas garanti que l’utilisation de ce dernier dans d’autres environnements est compatible et risque d’échouer.</span><span class="sxs-lookup"><span data-stu-id="39eb9-132">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="39eb9-133">Ses</span><span class="sxs-lookup"><span data-stu-id="39eb9-133">Members</span></span>

#### <span data-ttu-id="39eb9-134">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="39eb9-134">BrowserVersionString</span></span> 

<span data-ttu-id="39eb9-135">Les informations de la version du navigateur du CoreWebView2Environment actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.</span><span class="sxs-lookup"><span data-stu-id="39eb9-135">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="39eb9-136">[BrowserVersionString](#browserversionstring) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="39eb9-136">public string [BrowserVersionString](#browserversionstring)</span></span>

<span data-ttu-id="39eb9-137">Il correspond au format de l’API GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="39eb9-137">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="39eb9-138">Les noms de canaux sont «bêta», «dev» et «Canaries».</span><span class="sxs-lookup"><span data-stu-id="39eb9-138">Channel names are 'beta', 'dev', and 'canary'.</span></span>

#### <span data-ttu-id="39eb9-139">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="39eb9-139">NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="39eb9-140">L’événement NewBrowserVersionAvailable se déclenche lors de l’installation d’une nouvelle version du navigateur Edge et peut être utilisée via WebView2.</span><span class="sxs-lookup"><span data-stu-id="39eb9-140">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="39eb9-141">événement public EventHandler< objet > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span><span class="sxs-lookup"><span data-stu-id="39eb9-141">public event EventHandler< object > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span></span>

<span data-ttu-id="39eb9-142">Pour utiliser la nouvelle version du navigateur, vous devez créer un environnement et un WebView.</span><span class="sxs-lookup"><span data-stu-id="39eb9-142">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="39eb9-143">Cet événement est déclenché uniquement pour la nouvelle version à partir du canal Edge à partir duquel le code est exécuté.</span><span class="sxs-lookup"><span data-stu-id="39eb9-143">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="39eb9-144">S’il n’est pas exécuté avec des bords installés, aucun événement n’est déclenché.</span><span class="sxs-lookup"><span data-stu-id="39eb9-144">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="39eb9-145">Dans la mesure où un dossier de données utilisateur ne peut être utilisé que par un seul processus de navigateur à la fois, si vous souhaitez utiliser le même dossier de données utilisateur dans les webaffichages à l’aide de la nouvelle version du navigateur, vous devez d’abord fermer l’environnement et les webvues qui utilisent la version antérieure du navigateur.</span><span class="sxs-lookup"><span data-stu-id="39eb9-145">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="39eb9-146">Vous pouvez également demander à l’utilisateur de redémarrer l’application.</span><span class="sxs-lookup"><span data-stu-id="39eb9-146">Or simply prompt the user to restart the app.</span></span>

#### <span data-ttu-id="39eb9-147">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="39eb9-147">CompareBrowserVersions</span></span> 

<span data-ttu-id="39eb9-148">Comparez les versions du navigateur correctement pour déterminer la version la plus récente, la plus ancienne ou la plus récente.</span><span class="sxs-lookup"><span data-stu-id="39eb9-148">Compare browser versions correctly to determine which version is newer, older or same.</span></span>

> <span data-ttu-id="39eb9-149">public static int [CompareBrowserVersions](#comparebrowserversions)(chaîne version1, chaîne version2)</span><span class="sxs-lookup"><span data-stu-id="39eb9-149">public static int [CompareBrowserVersions](#comparebrowserversions)(string version1, string version2)</span></span>

<span data-ttu-id="39eb9-150">Renvoie-1, 0 ou 1 selon que la propriété version1 est inférieure ou égale ou supérieure à version2, respectivement.</span><span class="sxs-lookup"><span data-stu-id="39eb9-150">Returns -1, 0 or 1 depending on whether version1 is less than, equal to or greater than version2, respectively.</span></span>

##### <span data-ttu-id="39eb9-151">Parameters</span><span class="sxs-lookup"><span data-stu-id="39eb9-151">Parameters</span></span>
* `version1` <span data-ttu-id="39eb9-152">Une des chaînes de version à comparer.</span><span class="sxs-lookup"><span data-stu-id="39eb9-152">One of the version strings to compare.</span></span> 

* `version2` <span data-ttu-id="39eb9-153">Autre chaîne de version à comparer.</span><span class="sxs-lookup"><span data-stu-id="39eb9-153">The other version string to compare.</span></span>

#### <span data-ttu-id="39eb9-154">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="39eb9-154">CreateAsync</span></span> 

<span data-ttu-id="39eb9-155">Crée un environnement WebView2 persistant à l’aide de la version latérale installée.</span><span class="sxs-lookup"><span data-stu-id="39eb9-155">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

> <span data-ttu-id="39eb9-156">tâches asynchrones publiques< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [CreateAsync](#createasync)(String browserExecutableFolder, String userDataFolder, CoreWebView2EnvironmentOptions options)</span><span class="sxs-lookup"><span data-stu-id="39eb9-156">public static async Task< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md) > [CreateAsync](#createasync)(string browserExecutableFolder, string userDataFolder, CoreWebView2EnvironmentOptions options)</span></span>

##### <span data-ttu-id="39eb9-157">Parameters</span><span class="sxs-lookup"><span data-stu-id="39eb9-157">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="39eb9-158">Le chemin d’accès relatif au dossier qui contient le bord incorporé.</span><span class="sxs-lookup"><span data-stu-id="39eb9-158">The relative path to the folder that contains the embedded Edge.</span></span> 

* `userDataFolder` <span data-ttu-id="39eb9-159">userDataFolder peut être spécifié pour changer l’emplacement du dossier des données utilisateur par défaut pour WebView2.</span><span class="sxs-lookup"><span data-stu-id="39eb9-159">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> 

* `options` <span data-ttu-id="39eb9-160">Options permettant de créer un environnement WebView2.</span><span class="sxs-lookup"><span data-stu-id="39eb9-160">Options used to create WebView2 Environment.</span></span>

#### <span data-ttu-id="39eb9-161">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="39eb9-161">CreateCoreWebView2CompositionControllerAsync</span></span> 

> [!NOTE]
> <span data-ttu-id="39eb9-162">Il s’agit d’une [API expérimentale](../../../concepts/versioning.md#experimental-apis) fournie avec notre version SDK version [0.9.538-préliminaire](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="39eb9-162">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="39eb9-163">Créer de manière asynchrone un nouveau WebView à utiliser avec l’hébergement visuel.</span><span class="sxs-lookup"><span data-stu-id="39eb9-163">Asynchronously create a new WebView for use with visual hosting.</span></span>

> <span data-ttu-id="39eb9-164">tâche asynchrone publique< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md)  >  [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr FenêtreParent)</span><span class="sxs-lookup"><span data-stu-id="39eb9-164">public async Task< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md) > [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="39eb9-165">FenêtreParent est le HWND dans lequel l’application relie l’arborescence d’éléments visuels du WebView.</span><span class="sxs-lookup"><span data-stu-id="39eb9-165">parentWindow is the HWND in which the app will connect the visual tree of the WebView.</span></span> <span data-ttu-id="39eb9-166">Il s’agira du HWND que l’application recevra les entrées de pointeur/souris destinées au WebView (et devront utiliser SendMouseInput/SendPointerInput pour transférer).</span><span class="sxs-lookup"><span data-stu-id="39eb9-166">This will be the HWND that the app will receive pointer/ mouse input meant for the WebView (and will need to use SendMouseInput/ SendPointerInput to forward).</span></span> <span data-ttu-id="39eb9-167">Si l’application déplace l’arborescence d’éléments visuels WebView vers une autre fenêtre, elle doit définir CoreWebView2CompositionController. FenêtreParent pour mettre à jour le nouveau HWND parent de l’arborescence d’éléments visuels.</span><span class="sxs-lookup"><span data-stu-id="39eb9-167">If the app moves the WebView visual tree to underneath a different window, then it needs to set CoreWebView2CompositionController.ParentWindow to update the new parent HWND of the visual tree.</span></span>

<span data-ttu-id="39eb9-168">Définissez la propriété RootVisualTarget sur la CoreWebView2CompositionController créée pour fournir un élément visuel permettant d’héberger l’arborescence visuelle du navigateur.</span><span class="sxs-lookup"><span data-stu-id="39eb9-168">Set RootVisualTarget property on the created CoreWebView2CompositionController to provide a visual to host the browser's visual tree.</span></span>

<span data-ttu-id="39eb9-169">Il est recommandé que l’application définisse l’ID du modèle utilisateur de l’application pour le processus ou la fenêtre de l’application.</span><span class="sxs-lookup"><span data-stu-id="39eb9-169">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="39eb9-170">Si aucune n’est définie, lors de la création d’un WebView, un ID de modèle utilisateur de l’application généré est défini sur la fenêtre racine de parentWindow.</span><span class="sxs-lookup"><span data-stu-id="39eb9-170">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="39eb9-171">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="39eb9-171">CreateCoreWebView2ControllerAsync</span></span> 

<span data-ttu-id="39eb9-172">Créer de manière asynchrone un nouveau WebView.</span><span class="sxs-lookup"><span data-stu-id="39eb9-172">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="39eb9-173">tâche asynchrone publique< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr FenêtreParent)</span><span class="sxs-lookup"><span data-stu-id="39eb9-173">public async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md) > [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="39eb9-174">FenêtreParent est le HWND dans lequel le WebView doit être affiché et à partir duquel il est reçu une entrée.</span><span class="sxs-lookup"><span data-stu-id="39eb9-174">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="39eb9-175">Le WebView ajoutera une fenêtre enfant à la fenêtre fournie lors de la création WebView.</span><span class="sxs-lookup"><span data-stu-id="39eb9-175">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="39eb9-176">Ordre de plan et autres éléments concernés par l’ordre des fenêtres frères en conséquence.</span><span class="sxs-lookup"><span data-stu-id="39eb9-176">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="39eb9-177">Il est recommandé que l’application définisse l’ID du modèle utilisateur de l’application pour le processus ou la fenêtre de l’application.</span><span class="sxs-lookup"><span data-stu-id="39eb9-177">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="39eb9-178">Si aucune n’est définie, lors de la création d’un WebView, un ID de modèle utilisateur de l’application généré est défini sur la fenêtre racine de parentWindow.</span><span class="sxs-lookup"><span data-stu-id="39eb9-178">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="39eb9-179">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="39eb9-179">CreateCoreWebView2PointerInfo</span></span> 

> [!NOTE]
> <span data-ttu-id="39eb9-180">Il s’agit d’une [API expérimentale](../../../concepts/versioning.md#experimental-apis) fournie avec notre version SDK version [0.9.538-préliminaire](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="39eb9-180">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="39eb9-181">Créer un CoreWebView2ExperimentalPointerInfo vide.</span><span class="sxs-lookup"><span data-stu-id="39eb9-181">Create an empty CoreWebView2ExperimentalPointerInfo.</span></span>

> <span data-ttu-id="39eb9-182">public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span><span class="sxs-lookup"><span data-stu-id="39eb9-182">public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span></span>

<span data-ttu-id="39eb9-183">La CoreWebView2ExperimentalPointerInfo renvoyée doit être remplie avec toutes les informations pertinentes avant d’appeler SendPointerInput.</span><span class="sxs-lookup"><span data-stu-id="39eb9-183">The returned CoreWebView2ExperimentalPointerInfo needs to be populated with all of the relevant info before calling SendPointerInput.</span></span>

#### <span data-ttu-id="39eb9-184">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="39eb9-184">CreateWebResourceResponse</span></span> 

<span data-ttu-id="39eb9-185">Créer un objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="39eb9-185">Create a new web resource response object.</span></span>

> <span data-ttu-id="39eb9-186">public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(contenu du flux, StatusCode, int, String ReasonPhrase, en-têtes de chaîne)</span><span class="sxs-lookup"><span data-stu-id="39eb9-186">public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int StatusCode, string ReasonPhrase, string Headers)</span></span>

<span data-ttu-id="39eb9-187">Les en-têtes sont les chaînes d’en-tête de réponse brutes délimitées par NewLine.</span><span class="sxs-lookup"><span data-stu-id="39eb9-187">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="39eb9-188">Il est également possible de créer cet objet avec une chaîne d’en-têtes vide, puis d’utiliser le CoreWebView2HttpResponseHeaders pour créer des en-têtes à l’aide de la fonction ligne.</span><span class="sxs-lookup"><span data-stu-id="39eb9-188">It's also possible to create this object with empty headers string and then use the CoreWebView2HttpResponseHeaders to construct the headers line by line.</span></span> <span data-ttu-id="39eb9-189">Pour plus d’informations sur les autres paramètres, voir CoreWebView2WebResourceResponse.</span><span class="sxs-lookup"><span data-stu-id="39eb9-189">For information on other parameters see CoreWebView2WebResourceResponse.</span></span>

#### <span data-ttu-id="39eb9-190">GetAvailableBrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="39eb9-190">GetAvailableBrowserVersionString</span></span> 

<span data-ttu-id="39eb9-191">Obtenez les informations de la version du navigateur, y compris le nom du canal, s’il ne s’agit pas du canal stable ou du bord intégré.</span><span class="sxs-lookup"><span data-stu-id="39eb9-191">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>

> <span data-ttu-id="39eb9-192">[GetAvailableBrowserVersionString](#getavailablebrowserversionstring)de chaîne statique publique (chaîne browserExecutableFolder)</span><span class="sxs-lookup"><span data-stu-id="39eb9-192">public static string [GetAvailableBrowserVersionString](#getavailablebrowserversionstring)(string browserExecutableFolder)</span></span>

##### <span data-ttu-id="39eb9-193">Parameters</span><span class="sxs-lookup"><span data-stu-id="39eb9-193">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="39eb9-194">Le chemin d’accès relatif au dossier qui contient le bord incorporé.</span><span class="sxs-lookup"><span data-stu-id="39eb9-194">The relative path to the folder that contains the embedded Edge.</span></span>

#### <span data-ttu-id="39eb9-195">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="39eb9-195">GetProviderForHwnd</span></span> 

> [!NOTE]
> <span data-ttu-id="39eb9-196">Il s’agit d’une [API expérimentale](../../../concepts/versioning.md#experimental-apis) fournie avec notre version SDK version [0.9.538-préliminaire](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="39eb9-196">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="39eb9-197">Retourne le fournisseur UI Automation pour le CoreWebView2CompositionController correspondant au HWND donné.</span><span class="sxs-lookup"><span data-stu-id="39eb9-197">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

> <span data-ttu-id="39eb9-198">[GetProviderForHwnd](#getproviderforhwnd)d’objet public (IntPtr hwnd)</span><span class="sxs-lookup"><span data-stu-id="39eb9-198">public object [GetProviderForHwnd](#getproviderforhwnd)(IntPtr hwnd)</span></span>

