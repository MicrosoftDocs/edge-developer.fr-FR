---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2Environment
ms.openlocfilehash: d1e30c17239eb1b609eb3f2c63e48a3a59616131
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011026"
---
# <span data-ttu-id="0ef26-104">0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="0ef26-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2Environment class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="0ef26-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="0ef26-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="0ef26-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="0ef26-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="0ef26-107">Il s’agit de l’environnement WebView2.</span><span class="sxs-lookup"><span data-stu-id="0ef26-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="0ef26-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="0ef26-108">Summary</span></span>

 <span data-ttu-id="0ef26-109">Ses</span><span class="sxs-lookup"><span data-stu-id="0ef26-109">Members</span></span>                        | <span data-ttu-id="0ef26-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="0ef26-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0ef26-111">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="0ef26-111">BrowserVersionString</span></span>](#browserversionstring) | <span data-ttu-id="0ef26-112">Les informations de la version du navigateur du CoreWebView2Environment actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.</span><span class="sxs-lookup"><span data-stu-id="0ef26-112">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="0ef26-113">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="0ef26-113">NewBrowserVersionAvailable</span></span>](#newbrowserversionavailable) | <span data-ttu-id="0ef26-114">L’événement NewBrowserVersionAvailable se déclenche lors de l’installation d’une nouvelle version du navigateur Edge et peut être utilisée via WebView2.</span><span class="sxs-lookup"><span data-stu-id="0ef26-114">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="0ef26-115">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="0ef26-115">CompareBrowserVersions</span></span>](#comparebrowserversions) | <span data-ttu-id="0ef26-116">Comparez les versions du navigateur correctement pour déterminer la version la plus récente, la plus ancienne ou la plus récente.</span><span class="sxs-lookup"><span data-stu-id="0ef26-116">Compare browser versions correctly to determine which version is newer, older or same.</span></span>
[<span data-ttu-id="0ef26-117">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="0ef26-117">CreateAsync</span></span>](#createasync) | <span data-ttu-id="0ef26-118">Crée un environnement WebView2 persistant à l’aide de la version latérale installée.</span><span class="sxs-lookup"><span data-stu-id="0ef26-118">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="0ef26-119">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="0ef26-119">CreateCoreWebView2CompositionControllerAsync</span></span>](#createcorewebview2compositioncontrollerasync) | <span data-ttu-id="0ef26-120">Créer de manière asynchrone un nouveau WebView à utiliser avec l’hébergement visuel.</span><span class="sxs-lookup"><span data-stu-id="0ef26-120">Asynchronously create a new WebView for use with visual hosting.</span></span>
[<span data-ttu-id="0ef26-121">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="0ef26-121">CreateCoreWebView2ControllerAsync</span></span>](#createcorewebview2controllerasync) | <span data-ttu-id="0ef26-122">Créer de manière asynchrone un nouveau WebView.</span><span class="sxs-lookup"><span data-stu-id="0ef26-122">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="0ef26-123">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="0ef26-123">CreateCoreWebView2PointerInfo</span></span>](#createcorewebview2pointerinfo) | <span data-ttu-id="0ef26-124">Créer un CoreWebView2PointerInfo vide.</span><span class="sxs-lookup"><span data-stu-id="0ef26-124">Create an empty CoreWebView2PointerInfo.</span></span>
[<span data-ttu-id="0ef26-125">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="0ef26-125">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="0ef26-126">Créer un objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="0ef26-126">Create a new web resource response object.</span></span>
[<span data-ttu-id="0ef26-127">GetAvailableBrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="0ef26-127">GetAvailableBrowserVersionString</span></span>](#getavailablebrowserversionstring) | <span data-ttu-id="0ef26-128">Obtenez les informations de la version du navigateur, y compris le nom du canal, s’il ne s’agit pas du canal stable ou du bord intégré.</span><span class="sxs-lookup"><span data-stu-id="0ef26-128">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>
[<span data-ttu-id="0ef26-129">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="0ef26-129">GetProviderForHwnd</span></span>](#getproviderforhwnd) | <span data-ttu-id="0ef26-130">Retourne le fournisseur UI Automation pour le CoreWebView2CompositionController correspondant au HWND donné.</span><span class="sxs-lookup"><span data-stu-id="0ef26-130">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

<span data-ttu-id="0ef26-131">Les webvues créées à partir d’un environnement s’exécutent sur le processus de navigateur spécifié avec des paramètres d’environnement et des objets créés à partir d’un environnement doivent être utilisés dans le même environnement.</span><span class="sxs-lookup"><span data-stu-id="0ef26-131">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="0ef26-132">Il n’est pas garanti que l’utilisation de ce dernier dans d’autres environnements est compatible et risque d’échouer.</span><span class="sxs-lookup"><span data-stu-id="0ef26-132">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="0ef26-133">Ses</span><span class="sxs-lookup"><span data-stu-id="0ef26-133">Members</span></span>

#### <span data-ttu-id="0ef26-134">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="0ef26-134">BrowserVersionString</span></span> 

<span data-ttu-id="0ef26-135">Les informations de la version du navigateur du CoreWebView2Environment actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.</span><span class="sxs-lookup"><span data-stu-id="0ef26-135">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="0ef26-136">[BrowserVersionString](#browserversionstring) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="0ef26-136">public string [BrowserVersionString](#browserversionstring)</span></span>

<span data-ttu-id="0ef26-137">Il correspond au format de l’API GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="0ef26-137">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="0ef26-138">Les noms de canaux sont «bêta», «dev» et «Canaries».</span><span class="sxs-lookup"><span data-stu-id="0ef26-138">Channel names are 'beta', 'dev', and 'canary'.</span></span>

#### <span data-ttu-id="0ef26-139">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="0ef26-139">NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="0ef26-140">L’événement NewBrowserVersionAvailable se déclenche lors de l’installation d’une nouvelle version du navigateur Edge et peut être utilisée via WebView2.</span><span class="sxs-lookup"><span data-stu-id="0ef26-140">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="0ef26-141">événement public EventHandler< objet > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span><span class="sxs-lookup"><span data-stu-id="0ef26-141">public event EventHandler< object > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span></span>

<span data-ttu-id="0ef26-142">Pour utiliser la nouvelle version du navigateur, vous devez créer un environnement et un WebView.</span><span class="sxs-lookup"><span data-stu-id="0ef26-142">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="0ef26-143">Cet événement est déclenché uniquement pour la nouvelle version à partir du canal Edge à partir duquel le code est exécuté.</span><span class="sxs-lookup"><span data-stu-id="0ef26-143">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="0ef26-144">S’il n’est pas exécuté avec des bords installés, aucun événement n’est déclenché.</span><span class="sxs-lookup"><span data-stu-id="0ef26-144">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="0ef26-145">Dans la mesure où un dossier de données utilisateur ne peut être utilisé que par un seul processus de navigateur à la fois, si vous souhaitez utiliser le même dossier de données utilisateur dans les webaffichages à l’aide de la nouvelle version du navigateur, vous devez d’abord fermer l’environnement et les webvues qui utilisent la version antérieure du navigateur.</span><span class="sxs-lookup"><span data-stu-id="0ef26-145">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="0ef26-146">Vous pouvez également demander à l’utilisateur de redémarrer l’application.</span><span class="sxs-lookup"><span data-stu-id="0ef26-146">Or simply prompt the user to restart the app.</span></span>

#### <span data-ttu-id="0ef26-147">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="0ef26-147">CompareBrowserVersions</span></span> 

<span data-ttu-id="0ef26-148">Comparez les versions du navigateur correctement pour déterminer la version la plus récente, la plus ancienne ou la plus récente.</span><span class="sxs-lookup"><span data-stu-id="0ef26-148">Compare browser versions correctly to determine which version is newer, older or same.</span></span>

> <span data-ttu-id="0ef26-149">public static int [CompareBrowserVersions](#comparebrowserversions)(chaîne version1, chaîne version2)</span><span class="sxs-lookup"><span data-stu-id="0ef26-149">public static int [CompareBrowserVersions](#comparebrowserversions)(string version1, string version2)</span></span>

<span data-ttu-id="0ef26-150">Renvoie-1, 0 ou 1 selon que la propriété version1 est inférieure ou égale ou supérieure à version2, respectivement.</span><span class="sxs-lookup"><span data-stu-id="0ef26-150">Returns -1, 0 or 1 depending on whether version1 is less than, equal to or greater than version2, respectively.</span></span>

##### <span data-ttu-id="0ef26-151">Parameters</span><span class="sxs-lookup"><span data-stu-id="0ef26-151">Parameters</span></span>
* `version1` <span data-ttu-id="0ef26-152">Une des chaînes de version à comparer.</span><span class="sxs-lookup"><span data-stu-id="0ef26-152">One of the version strings to compare.</span></span> 

* `version2` <span data-ttu-id="0ef26-153">Autre chaîne de version à comparer.</span><span class="sxs-lookup"><span data-stu-id="0ef26-153">The other version string to compare.</span></span>

#### <span data-ttu-id="0ef26-154">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="0ef26-154">CreateAsync</span></span> 

<span data-ttu-id="0ef26-155">Crée un environnement WebView2 persistant à l’aide de la version latérale installée.</span><span class="sxs-lookup"><span data-stu-id="0ef26-155">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

> <span data-ttu-id="0ef26-156">tâches asynchrones publiques< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [CreateAsync](#createasync)(String browserExecutableFolder, String userDataFolder, CoreWebView2EnvironmentOptions options)</span><span class="sxs-lookup"><span data-stu-id="0ef26-156">public static async Task< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md) > [CreateAsync](#createasync)(string browserExecutableFolder, string userDataFolder, CoreWebView2EnvironmentOptions options)</span></span>

##### <span data-ttu-id="0ef26-157">Parameters</span><span class="sxs-lookup"><span data-stu-id="0ef26-157">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="0ef26-158">Le chemin d’accès relatif au dossier qui contient le bord incorporé.</span><span class="sxs-lookup"><span data-stu-id="0ef26-158">The relative path to the folder that contains the embedded Edge.</span></span> 

* `userDataFolder` <span data-ttu-id="0ef26-159">userDataFolder peut être spécifié pour changer l’emplacement du dossier des données utilisateur par défaut pour WebView2.</span><span class="sxs-lookup"><span data-stu-id="0ef26-159">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> 

* `options` <span data-ttu-id="0ef26-160">Options permettant de créer un environnement WebView2.</span><span class="sxs-lookup"><span data-stu-id="0ef26-160">Options used to create WebView2 Environment.</span></span>

#### <span data-ttu-id="0ef26-161">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="0ef26-161">CreateCoreWebView2CompositionControllerAsync</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="0ef26-162">Créer de manière asynchrone un nouveau WebView à utiliser avec l’hébergement visuel.</span><span class="sxs-lookup"><span data-stu-id="0ef26-162">Asynchronously create a new WebView for use with visual hosting.</span></span>

> <span data-ttu-id="0ef26-163">tâche asynchrone publique< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md)  >  [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr FenêtreParent)</span><span class="sxs-lookup"><span data-stu-id="0ef26-163">public async Task< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md) > [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="0ef26-164">FenêtreParent est le HWND dans lequel l’application relie l’arborescence d’éléments visuels du WebView.</span><span class="sxs-lookup"><span data-stu-id="0ef26-164">parentWindow is the HWND in which the app will connect the visual tree of the WebView.</span></span> <span data-ttu-id="0ef26-165">Il s’agira du HWND que l’application recevra les entrées de pointeur/souris destinées au WebView (et devront utiliser SendMouseInput/SendPointerInput pour transférer).</span><span class="sxs-lookup"><span data-stu-id="0ef26-165">This will be the HWND that the app will receive pointer/ mouse input meant for the WebView (and will need to use SendMouseInput/ SendPointerInput to forward).</span></span> <span data-ttu-id="0ef26-166">Si l’application déplace l’arborescence d’éléments visuels WebView vers une autre fenêtre, elle doit définir CoreWebView2CompositionController. FenêtreParent pour mettre à jour le nouveau HWND parent de l’arborescence d’éléments visuels.</span><span class="sxs-lookup"><span data-stu-id="0ef26-166">If the app moves the WebView visual tree to underneath a different window, then it needs to set CoreWebView2CompositionController.ParentWindow to update the new parent HWND of the visual tree.</span></span>

<span data-ttu-id="0ef26-167">Définissez la propriété RootVisualTarget sur la CoreWebView2CompositionController créée pour fournir un élément visuel permettant d’héberger l’arborescence visuelle du navigateur.</span><span class="sxs-lookup"><span data-stu-id="0ef26-167">Set RootVisualTarget property on the created CoreWebView2CompositionController to provide a visual to host the browser's visual tree.</span></span>

<span data-ttu-id="0ef26-168">Il est recommandé que l’application définisse l’ID du modèle utilisateur de l’application pour le processus ou la fenêtre de l’application.</span><span class="sxs-lookup"><span data-stu-id="0ef26-168">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="0ef26-169">Si aucune n’est définie, lors de la création d’un WebView, un ID de modèle utilisateur de l’application généré est défini sur la fenêtre racine de parentWindow.</span><span class="sxs-lookup"><span data-stu-id="0ef26-169">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="0ef26-170">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="0ef26-170">CreateCoreWebView2ControllerAsync</span></span> 

<span data-ttu-id="0ef26-171">Créer de manière asynchrone un nouveau WebView.</span><span class="sxs-lookup"><span data-stu-id="0ef26-171">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="0ef26-172">tâche asynchrone publique< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr FenêtreParent)</span><span class="sxs-lookup"><span data-stu-id="0ef26-172">public async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md) > [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="0ef26-173">FenêtreParent est le HWND dans lequel le WebView doit être affiché et à partir duquel il est reçu une entrée.</span><span class="sxs-lookup"><span data-stu-id="0ef26-173">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="0ef26-174">Le WebView ajoutera une fenêtre enfant à la fenêtre fournie lors de la création WebView.</span><span class="sxs-lookup"><span data-stu-id="0ef26-174">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="0ef26-175">Ordre de plan et autres éléments concernés par l’ordre des fenêtres frères en conséquence.</span><span class="sxs-lookup"><span data-stu-id="0ef26-175">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="0ef26-176">Il est recommandé que l’application définisse l’ID du modèle utilisateur de l’application pour le processus ou la fenêtre de l’application.</span><span class="sxs-lookup"><span data-stu-id="0ef26-176">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="0ef26-177">Si aucune n’est définie, lors de la création d’un WebView, un ID de modèle utilisateur de l’application généré est défini sur la fenêtre racine de parentWindow.</span><span class="sxs-lookup"><span data-stu-id="0ef26-177">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="0ef26-178">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="0ef26-178">CreateCoreWebView2PointerInfo</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="0ef26-179">Créer un CoreWebView2PointerInfo vide.</span><span class="sxs-lookup"><span data-stu-id="0ef26-179">Create an empty CoreWebView2PointerInfo.</span></span>

> <span data-ttu-id="0ef26-180">public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span><span class="sxs-lookup"><span data-stu-id="0ef26-180">public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span></span>

<span data-ttu-id="0ef26-181">La CoreWebView2PointerInfo renvoyée doit être remplie avec toutes les informations pertinentes avant d’appeler SendPointerInput.</span><span class="sxs-lookup"><span data-stu-id="0ef26-181">The returned CoreWebView2PointerInfo needs to be populated with all of the relevant info before calling SendPointerInput.</span></span>

#### <span data-ttu-id="0ef26-182">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="0ef26-182">CreateWebResourceResponse</span></span> 

<span data-ttu-id="0ef26-183">Créer un objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="0ef26-183">Create a new web resource response object.</span></span>

> <span data-ttu-id="0ef26-184">public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(contenu du flux, StatusCode, int, String ReasonPhrase, en-têtes de chaîne)</span><span class="sxs-lookup"><span data-stu-id="0ef26-184">public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int StatusCode, string ReasonPhrase, string Headers)</span></span>

<span data-ttu-id="0ef26-185">Les en-têtes sont les chaînes d’en-tête de réponse brutes délimitées par NewLine.</span><span class="sxs-lookup"><span data-stu-id="0ef26-185">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="0ef26-186">Il est également possible de créer cet objet avec une chaîne d’en-têtes vide, puis d’utiliser le CoreWebView2HttpResponseHeaders pour créer des en-têtes à l’aide de la fonction ligne.</span><span class="sxs-lookup"><span data-stu-id="0ef26-186">It's also possible to create this object with empty headers string and then use the CoreWebView2HttpResponseHeaders to construct the headers line by line.</span></span> <span data-ttu-id="0ef26-187">Pour plus d’informations sur les autres paramètres, voir CoreWebView2WebResourceResponse.</span><span class="sxs-lookup"><span data-stu-id="0ef26-187">For information on other parameters see CoreWebView2WebResourceResponse.</span></span>

#### <span data-ttu-id="0ef26-188">GetAvailableBrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="0ef26-188">GetAvailableBrowserVersionString</span></span> 

<span data-ttu-id="0ef26-189">Obtenez les informations de la version du navigateur, y compris le nom du canal, s’il ne s’agit pas du canal stable ou du bord intégré.</span><span class="sxs-lookup"><span data-stu-id="0ef26-189">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>

> <span data-ttu-id="0ef26-190">[GetAvailableBrowserVersionString](#getavailablebrowserversionstring)de chaîne statique publique (chaîne browserExecutableFolder)</span><span class="sxs-lookup"><span data-stu-id="0ef26-190">public static string [GetAvailableBrowserVersionString](#getavailablebrowserversionstring)(string browserExecutableFolder)</span></span>

##### <span data-ttu-id="0ef26-191">Parameters</span><span class="sxs-lookup"><span data-stu-id="0ef26-191">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="0ef26-192">Le chemin d’accès relatif au dossier qui contient le bord incorporé.</span><span class="sxs-lookup"><span data-stu-id="0ef26-192">The relative path to the folder that contains the embedded Edge.</span></span>

#### <span data-ttu-id="0ef26-193">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="0ef26-193">GetProviderForHwnd</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="0ef26-194">Retourne le fournisseur UI Automation pour le CoreWebView2CompositionController correspondant au HWND donné.</span><span class="sxs-lookup"><span data-stu-id="0ef26-194">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

> <span data-ttu-id="0ef26-195">[GetProviderForHwnd](#getproviderforhwnd)d’objet public (IntPtr hwnd)</span><span class="sxs-lookup"><span data-stu-id="0ef26-195">public object [GetProviderForHwnd](#getproviderforhwnd)(IntPtr hwnd)</span></span>

