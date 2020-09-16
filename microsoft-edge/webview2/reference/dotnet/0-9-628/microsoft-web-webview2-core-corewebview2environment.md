---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/11/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2Environment
ms.openlocfilehash: 05b8a10c723ae57b2c95551f4d5043f3336eba3b
ms.sourcegitcommit: 65db518273b3cd69f1b3c528809600719b9b70aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2020
ms.locfileid: "11016325"
---
# <span data-ttu-id="dc488-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="dc488-104">Microsoft.Web.WebView2.Core.CoreWebView2Environment class</span></span> 

<span data-ttu-id="dc488-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="dc488-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="dc488-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="dc488-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="dc488-107">Il s’agit de l’environnement WebView2.</span><span class="sxs-lookup"><span data-stu-id="dc488-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="dc488-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="dc488-108">Summary</span></span>

 <span data-ttu-id="dc488-109">Ses</span><span class="sxs-lookup"><span data-stu-id="dc488-109">Members</span></span>                        | <span data-ttu-id="dc488-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="dc488-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="dc488-111">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="dc488-111">BrowserVersionString</span></span>](#browserversionstring) | <span data-ttu-id="dc488-112">Les informations de la version du navigateur du CoreWebView2Environment actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.</span><span class="sxs-lookup"><span data-stu-id="dc488-112">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="dc488-113">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="dc488-113">NewBrowserVersionAvailable</span></span>](#newbrowserversionavailable) | <span data-ttu-id="dc488-114">NewBrowserVersionAvailable se déclenche quand une nouvelle version du navigateur Edge est installée et disponible pour une utilisation via WebView2.</span><span class="sxs-lookup"><span data-stu-id="dc488-114">NewBrowserVersionAvailable fires when a newer version of the Edge browser is installed and available for use via WebView2.</span></span>
[<span data-ttu-id="dc488-115">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="dc488-115">CompareBrowserVersions</span></span>](#comparebrowserversions) | <span data-ttu-id="dc488-116">Comparez les versions de navigateur pour déterminer si elles sont identiques ou différentes.</span><span class="sxs-lookup"><span data-stu-id="dc488-116">Compare browser versions to determine if they match or are different.</span></span>
[<span data-ttu-id="dc488-117">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="dc488-117">CreateAsync</span></span>](#createasync) | <span data-ttu-id="dc488-118">Crée un environnement WebView2 persistant à l’aide de la version installée de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="dc488-118">Creates an evergreen WebView2 Environment using the installed version of Microsoft Edge.</span></span>
[<span data-ttu-id="dc488-119">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="dc488-119">CreateCoreWebView2CompositionControllerAsync</span></span>](#createcorewebview2compositioncontrollerasync) | <span data-ttu-id="dc488-120">Créer de manière asynchrone un nouveau WebView à utiliser avec l’hébergement visuel.</span><span class="sxs-lookup"><span data-stu-id="dc488-120">Asynchronously create a new WebView for use with visual hosting.</span></span>
[<span data-ttu-id="dc488-121">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="dc488-121">CreateCoreWebView2ControllerAsync</span></span>](#createcorewebview2controllerasync) | <span data-ttu-id="dc488-122">Créer de manière asynchrone un nouveau WebView.</span><span class="sxs-lookup"><span data-stu-id="dc488-122">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="dc488-123">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="dc488-123">CreateCoreWebView2PointerInfo</span></span>](#createcorewebview2pointerinfo) | <span data-ttu-id="dc488-124">Créer un CoreWebView2PointerInfo vide.</span><span class="sxs-lookup"><span data-stu-id="dc488-124">Create an empty CoreWebView2PointerInfo.</span></span>
[<span data-ttu-id="dc488-125">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="dc488-125">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="dc488-126">Créer un objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="dc488-126">Create a new web resource response object.</span></span>
[<span data-ttu-id="dc488-127">GetAvailableBrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="dc488-127">GetAvailableBrowserVersionString</span></span>](#getavailablebrowserversionstring) | <span data-ttu-id="dc488-128">Obtenez les informations de la version du navigateur.</span><span class="sxs-lookup"><span data-stu-id="dc488-128">Get the browser version information.</span></span>
[<span data-ttu-id="dc488-129">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="dc488-129">GetProviderForHwnd</span></span>](#getproviderforhwnd) | <span data-ttu-id="dc488-130">Retourne le fournisseur UI Automation pour le CoreWebView2CompositionController correspondant au HWND donné.</span><span class="sxs-lookup"><span data-stu-id="dc488-130">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

<span data-ttu-id="dc488-131">Les webvues créées à partir d’un environnement s’exécutent sur le processus de navigateur spécifié avec des paramètres d’environnement et des objets créés à partir d’un environnement doivent être utilisés dans le même environnement.</span><span class="sxs-lookup"><span data-stu-id="dc488-131">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="dc488-132">Il n’est pas garanti que l’utilisation de ce dernier dans d’autres environnements est compatible et risque d’échouer.</span><span class="sxs-lookup"><span data-stu-id="dc488-132">Using it in different environments are not guaranteed to be compatible and may fail.</span></span> 

## <span data-ttu-id="dc488-133">Ses</span><span class="sxs-lookup"><span data-stu-id="dc488-133">Members</span></span>

#### <span data-ttu-id="dc488-134">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="dc488-134">BrowserVersionString</span></span> 

<span data-ttu-id="dc488-135">Les informations de la version du navigateur du CoreWebView2Environment actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.</span><span class="sxs-lookup"><span data-stu-id="dc488-135">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="dc488-136">[BrowserVersionString](#browserversionstring) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="dc488-136">public string [BrowserVersionString](#browserversionstring)</span></span>

<span data-ttu-id="dc488-137">Il correspond au format de l’API GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="dc488-137">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="dc488-138">Les noms de canaux sont «bêta», «dev» et «Canaries».</span><span class="sxs-lookup"><span data-stu-id="dc488-138">Channel names are 'beta', 'dev', and 'canary'.</span></span>

#### <span data-ttu-id="dc488-139">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="dc488-139">NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="dc488-140">NewBrowserVersionAvailable se déclenche quand une nouvelle version du navigateur Edge est installée et disponible pour une utilisation via WebView2.</span><span class="sxs-lookup"><span data-stu-id="dc488-140">NewBrowserVersionAvailable fires when a newer version of the Edge browser is installed and available for use via WebView2.</span></span>

> <span data-ttu-id="dc488-141">événement public EventHandler< objet > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span><span class="sxs-lookup"><span data-stu-id="dc488-141">public event EventHandler< object > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span></span>

<span data-ttu-id="dc488-142">Pour utiliser la nouvelle version du navigateur, vous devez créer un environnement et un WebView.</span><span class="sxs-lookup"><span data-stu-id="dc488-142">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="dc488-143">Cet événement est déclenché uniquement pour la nouvelle version à partir du canal Edge à partir duquel le code est exécuté.</span><span class="sxs-lookup"><span data-stu-id="dc488-143">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="dc488-144">S’il n’est pas exécuté avec des bords installés, aucun événement n’est déclenché.</span><span class="sxs-lookup"><span data-stu-id="dc488-144">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="dc488-145">Dans la mesure où un dossier de données utilisateur ne peut être utilisé que par un seul processus de navigateur à la fois, si vous souhaitez utiliser le même dossier de données utilisateur dans les webaffichages à l’aide de la nouvelle version du navigateur, vous devez d’abord fermer l’environnement et les webvues qui utilisent la version antérieure du navigateur.</span><span class="sxs-lookup"><span data-stu-id="dc488-145">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="dc488-146">Vous pouvez également demander à l’utilisateur de redémarrer l’application.</span><span class="sxs-lookup"><span data-stu-id="dc488-146">Or simply prompt the user to restart the app.</span></span>

#### <span data-ttu-id="dc488-147">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="dc488-147">CompareBrowserVersions</span></span> 

<span data-ttu-id="dc488-148">Comparez les versions de navigateur pour déterminer si elles sont identiques ou différentes.</span><span class="sxs-lookup"><span data-stu-id="dc488-148">Compare browser versions to determine if they match or are different.</span></span>

> <span data-ttu-id="dc488-149">public static int [CompareBrowserVersions](#comparebrowserversions)(chaîne version1, chaîne version2)</span><span class="sxs-lookup"><span data-stu-id="dc488-149">public static int [CompareBrowserVersions](#comparebrowserversions)(string version1, string version2)</span></span>

<span data-ttu-id="dc488-150">Renvoie-1, 0 ou 1 selon que la première version est inférieure ou égale ou supérieure à la deuxième version comparée.</span><span class="sxs-lookup"><span data-stu-id="dc488-150">Returns -1, 0 or 1 depending on whether the first version is less than, equal to or greater than the second version being compared.</span></span>

<span data-ttu-id="dc488-151">Les données d’entrée peuvent utiliser directement le versionInfo obtenu à partir de GetAvailableCoreWebView2BrowserVersionString, les informations de canal seront ignorées.</span><span class="sxs-lookup"><span data-stu-id="dc488-151">Input can directly use the versionInfo obtained from GetAvailableCoreWebView2BrowserVersionString, channel info will be ignored.</span></span>

##### <span data-ttu-id="dc488-152">Parameters</span><span class="sxs-lookup"><span data-stu-id="dc488-152">Parameters</span></span>
* `version1` <span data-ttu-id="dc488-153">Première version à comparer.</span><span class="sxs-lookup"><span data-stu-id="dc488-153">The first version to compare.</span></span> 

* `version2` <span data-ttu-id="dc488-154">Seconde version à comparer.</span><span class="sxs-lookup"><span data-stu-id="dc488-154">The second version to compare.</span></span>

#### <span data-ttu-id="dc488-155">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="dc488-155">CreateAsync</span></span> 

<span data-ttu-id="dc488-156">Crée un environnement WebView2 persistant à l’aide de la version installée de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="dc488-156">Creates an evergreen WebView2 Environment using the installed version of Microsoft Edge.</span></span>

> <span data-ttu-id="dc488-157">tâches asynchrones publiques< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [CreateAsync](#createasync)(String browserExecutableFolder, String userDataFolder, CoreWebView2EnvironmentOptions options)</span><span class="sxs-lookup"><span data-stu-id="dc488-157">public static async Task< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md) > [CreateAsync](#createasync)(string browserExecutableFolder, string userDataFolder, CoreWebView2EnvironmentOptions options)</span></span>

##### <span data-ttu-id="dc488-158">Parameters</span><span class="sxs-lookup"><span data-stu-id="dc488-158">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="dc488-159">Le chemin d’accès relatif au dossier qui contient la version fixe de WebView2 Runtime.</span><span class="sxs-lookup"><span data-stu-id="dc488-159">The relative path to the folder that contains the fixed version of the WebView2 Runtime.</span></span> 

* `userDataFolder` <span data-ttu-id="dc488-160">userDataFolder peut être spécifié pour changer l’emplacement du dossier des données utilisateur par défaut pour WebView2.</span><span class="sxs-lookup"><span data-stu-id="dc488-160">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> 

* `options` <span data-ttu-id="dc488-161">Options permettant de créer un environnement WebView2.</span><span class="sxs-lookup"><span data-stu-id="dc488-161">Options used to create WebView2 Environment.</span></span>

#### <span data-ttu-id="dc488-162">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="dc488-162">CreateCoreWebView2CompositionControllerAsync</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="dc488-163">Créer de manière asynchrone un nouveau WebView à utiliser avec l’hébergement visuel.</span><span class="sxs-lookup"><span data-stu-id="dc488-163">Asynchronously create a new WebView for use with visual hosting.</span></span>

> <span data-ttu-id="dc488-164">tâche asynchrone publique< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md)  >  [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr FenêtreParent)</span><span class="sxs-lookup"><span data-stu-id="dc488-164">public async Task< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md) > [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="dc488-165">FenêtreParent est le HWND dans lequel l’application relie l’arborescence d’éléments visuels du WebView.</span><span class="sxs-lookup"><span data-stu-id="dc488-165">parentWindow is the HWND in which the app will connect the visual tree of the WebView.</span></span> <span data-ttu-id="dc488-166">Il s’agira du HWND que l’application recevra les entrées de pointeur/souris destinées au WebView (et devront utiliser SendMouseInput/SendPointerInput pour transférer).</span><span class="sxs-lookup"><span data-stu-id="dc488-166">This will be the HWND that the app will receive pointer/ mouse input meant for the WebView (and will need to use SendMouseInput/ SendPointerInput to forward).</span></span> <span data-ttu-id="dc488-167">Si l’application déplace l’arborescence d’éléments visuels WebView vers une autre fenêtre, elle doit définir CoreWebView2CompositionController. FenêtreParent pour mettre à jour le nouveau HWND parent de l’arborescence d’éléments visuels.</span><span class="sxs-lookup"><span data-stu-id="dc488-167">If the app moves the WebView visual tree to underneath a different window, then it needs to set CoreWebView2CompositionController.ParentWindow to update the new parent HWND of the visual tree.</span></span>

<span data-ttu-id="dc488-168">Définissez la propriété RootVisualTarget sur la CoreWebView2CompositionController créée pour fournir un élément visuel permettant d’héberger l’arborescence visuelle du navigateur.</span><span class="sxs-lookup"><span data-stu-id="dc488-168">Set RootVisualTarget property on the created CoreWebView2CompositionController to provide a visual to host the browser's visual tree.</span></span>

<span data-ttu-id="dc488-169">Il est recommandé que l’application définisse l’ID du modèle utilisateur de l’application pour le processus ou la fenêtre de l’application.</span><span class="sxs-lookup"><span data-stu-id="dc488-169">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="dc488-170">Si aucune n’est définie, lors de la création d’un WebView, un ID de modèle utilisateur de l’application généré est défini sur la fenêtre racine de parentWindow.</span><span class="sxs-lookup"><span data-stu-id="dc488-170">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="dc488-171">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="dc488-171">CreateCoreWebView2ControllerAsync</span></span> 

<span data-ttu-id="dc488-172">Créer de manière asynchrone un nouveau WebView.</span><span class="sxs-lookup"><span data-stu-id="dc488-172">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="dc488-173">tâche asynchrone publique< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr FenêtreParent)</span><span class="sxs-lookup"><span data-stu-id="dc488-173">public async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md) > [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="dc488-174">FenêtreParent est le HWND dans lequel le WebView doit être affiché et à partir duquel il est reçu une entrée.</span><span class="sxs-lookup"><span data-stu-id="dc488-174">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="dc488-175">Le WebView ajoutera une fenêtre enfant à la fenêtre fournie lors de la création WebView.</span><span class="sxs-lookup"><span data-stu-id="dc488-175">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="dc488-176">Ordre de plan et autres éléments concernés par l’ordre des fenêtres frères en conséquence.</span><span class="sxs-lookup"><span data-stu-id="dc488-176">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="dc488-177">Il est recommandé que l’application définisse l’ID du modèle utilisateur de l’application pour le processus ou la fenêtre de l’application.</span><span class="sxs-lookup"><span data-stu-id="dc488-177">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="dc488-178">Si aucune n’est définie, lors de la création d’un WebView, un ID de modèle utilisateur de l’application généré est défini sur la fenêtre racine de parentWindow.</span><span class="sxs-lookup"><span data-stu-id="dc488-178">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="dc488-179">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="dc488-179">CreateCoreWebView2PointerInfo</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="dc488-180">Créer un CoreWebView2PointerInfo vide.</span><span class="sxs-lookup"><span data-stu-id="dc488-180">Create an empty CoreWebView2PointerInfo.</span></span>

> <span data-ttu-id="dc488-181">public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span><span class="sxs-lookup"><span data-stu-id="dc488-181">public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span></span>

<span data-ttu-id="dc488-182">La CoreWebView2PointerInfo renvoyée doit être remplie avec toutes les informations pertinentes avant d’appeler SendPointerInput.</span><span class="sxs-lookup"><span data-stu-id="dc488-182">The returned CoreWebView2PointerInfo needs to be populated with all of the relevant info before calling SendPointerInput.</span></span>

#### <span data-ttu-id="dc488-183">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="dc488-183">CreateWebResourceResponse</span></span> 

<span data-ttu-id="dc488-184">Créer un objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="dc488-184">Create a new web resource response object.</span></span>

> <span data-ttu-id="dc488-185">public [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [CreateWebResourceResponse](#createwebresourceresponse)(contenu du flux, StatusCode, int, String ReasonPhrase, en-têtes de chaîne)</span><span class="sxs-lookup"><span data-stu-id="dc488-185">public [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int StatusCode, string ReasonPhrase, string Headers)</span></span>

<span data-ttu-id="dc488-186">Les en-têtes sont les chaînes d’en-tête de réponse brutes délimitées par NewLine.</span><span class="sxs-lookup"><span data-stu-id="dc488-186">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="dc488-187">Il est également possible de créer cet objet avec une chaîne d’en-têtes vide, puis d’utiliser le CoreWebView2HttpResponseHeaders pour créer des en-têtes à l’aide de la fonction ligne.</span><span class="sxs-lookup"><span data-stu-id="dc488-187">It's also possible to create this object with empty headers string and then use the CoreWebView2HttpResponseHeaders to construct the headers line by line.</span></span> <span data-ttu-id="dc488-188">Pour plus d’informations sur les autres paramètres, voir CoreWebView2WebResourceResponse.</span><span class="sxs-lookup"><span data-stu-id="dc488-188">For information on other parameters see CoreWebView2WebResourceResponse.</span></span>

#### <span data-ttu-id="dc488-189">GetAvailableBrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="dc488-189">GetAvailableBrowserVersionString</span></span> 

<span data-ttu-id="dc488-190">Obtenez les informations de la version du navigateur.</span><span class="sxs-lookup"><span data-stu-id="dc488-190">Get the browser version information.</span></span>

> <span data-ttu-id="dc488-191">[GetAvailableBrowserVersionString](#getavailablebrowserversionstring)de chaîne statique publique (chaîne browserExecutableFolder)</span><span class="sxs-lookup"><span data-stu-id="dc488-191">public static string [GetAvailableBrowserVersionString](#getavailablebrowserversionstring)(string browserExecutableFolder)</span></span>

<span data-ttu-id="dc488-192">Vous obtenez également le nom du canal si le canal n’est pas un canal stable.</span><span class="sxs-lookup"><span data-stu-id="dc488-192">You also get the channel name if the channel is not a stable channel.</span></span> <span data-ttu-id="dc488-193">Si vous utilisez le runtime WebView2, aucun nom de canal n’est retourné.</span><span class="sxs-lookup"><span data-stu-id="dc488-193">If you use the WebView2 Runtime, no channel name is returned.</span></span>

##### <span data-ttu-id="dc488-194">Parameters</span><span class="sxs-lookup"><span data-stu-id="dc488-194">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="dc488-195">Le chemin d’accès relatif au dossier qui contient la version fixe de WebView2 Runtime.</span><span class="sxs-lookup"><span data-stu-id="dc488-195">The relative path to the folder that contains the fixed version of the WebView2 Runtime.</span></span>

#### <span data-ttu-id="dc488-196">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="dc488-196">GetProviderForHwnd</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="dc488-197">Retourne le fournisseur UI Automation pour le CoreWebView2CompositionController correspondant au HWND donné.</span><span class="sxs-lookup"><span data-stu-id="dc488-197">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

> <span data-ttu-id="dc488-198">[GetProviderForHwnd](#getproviderforhwnd)d’objet public (IntPtr hwnd)</span><span class="sxs-lookup"><span data-stu-id="dc488-198">public object [GetProviderForHwnd](#getproviderforhwnd)(IntPtr hwnd)</span></span>
