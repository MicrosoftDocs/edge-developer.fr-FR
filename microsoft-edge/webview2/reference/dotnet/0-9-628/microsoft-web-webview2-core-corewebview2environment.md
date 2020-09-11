---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2Environment
ms.openlocfilehash: c6b1f1c62da5aa5ef64693575abb9cb46ac13851
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011898"
---
# <span data-ttu-id="aec64-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="aec64-104">Microsoft.Web.WebView2.Core.CoreWebView2Environment class</span></span> 

<span data-ttu-id="aec64-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="aec64-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="aec64-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="aec64-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="aec64-107">Il s’agit de l’environnement WebView2.</span><span class="sxs-lookup"><span data-stu-id="aec64-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="aec64-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="aec64-108">Summary</span></span>

 <span data-ttu-id="aec64-109">Ses</span><span class="sxs-lookup"><span data-stu-id="aec64-109">Members</span></span>                        | <span data-ttu-id="aec64-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="aec64-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="aec64-111">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="aec64-111">BrowserVersionString</span></span>](#browserversionstring) | <span data-ttu-id="aec64-112">Les informations de la version du navigateur du CoreWebView2Environment actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.</span><span class="sxs-lookup"><span data-stu-id="aec64-112">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="aec64-113">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="aec64-113">NewBrowserVersionAvailable</span></span>](#newbrowserversionavailable) | <span data-ttu-id="aec64-114">NewBrowserVersionAvailable se déclenche quand une nouvelle version du navigateur Edge est installée et disponible pour une utilisation via WebView2.</span><span class="sxs-lookup"><span data-stu-id="aec64-114">NewBrowserVersionAvailable fires when a newer version of the Edge browser is installed and available for use via WebView2.</span></span>
[<span data-ttu-id="aec64-115">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="aec64-115">CreateCoreWebView2CompositionControllerAsync</span></span>](#createcorewebview2compositioncontrollerasync) | <span data-ttu-id="aec64-116">Créer de manière asynchrone un nouveau WebView à utiliser avec l’hébergement visuel.</span><span class="sxs-lookup"><span data-stu-id="aec64-116">Asynchronously create a new WebView for use with visual hosting.</span></span>
[<span data-ttu-id="aec64-117">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="aec64-117">CreateCoreWebView2ControllerAsync</span></span>](#createcorewebview2controllerasync) | <span data-ttu-id="aec64-118">Créer de manière asynchrone un nouveau WebView.</span><span class="sxs-lookup"><span data-stu-id="aec64-118">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="aec64-119">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="aec64-119">CreateCoreWebView2PointerInfo</span></span>](#createcorewebview2pointerinfo) | <span data-ttu-id="aec64-120">Créer un CoreWebView2PointerInfo vide.</span><span class="sxs-lookup"><span data-stu-id="aec64-120">Create an empty CoreWebView2PointerInfo.</span></span>
[<span data-ttu-id="aec64-121">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="aec64-121">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="aec64-122">Créer un objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="aec64-122">Create a new web resource response object.</span></span>
[<span data-ttu-id="aec64-123">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="aec64-123">GetProviderForHwnd</span></span>](#getproviderforhwnd) | <span data-ttu-id="aec64-124">Retourne le fournisseur UI Automation pour le CoreWebView2CompositionController correspondant au HWND donné.</span><span class="sxs-lookup"><span data-stu-id="aec64-124">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

<span data-ttu-id="aec64-125">Les webvues créées à partir d’un environnement s’exécutent sur le processus de navigateur spécifié avec des paramètres d’environnement et des objets créés à partir d’un environnement doivent être utilisés dans le même environnement.</span><span class="sxs-lookup"><span data-stu-id="aec64-125">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="aec64-126">Il n’est pas garanti que l’utilisation de ce dernier dans d’autres environnements est compatible et risque d’échouer.</span><span class="sxs-lookup"><span data-stu-id="aec64-126">Using it in different environments are not guaranteed to be compatible and may fail.</span></span> 

<span data-ttu-id="aec64-127">Les webvues créées à partir d’un environnement s’exécutent sur le processus de navigateur spécifié avec des paramètres d’environnement et des objets créés à partir d’un environnement doivent être utilisés dans le même environnement.</span><span class="sxs-lookup"><span data-stu-id="aec64-127">WebViews created from an environment run on the browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="aec64-128">Il n’est pas garanti que l’utilisation de ce dernier dans d’autres environnements est compatible et risque d’échouer.</span><span class="sxs-lookup"><span data-stu-id="aec64-128">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="aec64-129">Ses</span><span class="sxs-lookup"><span data-stu-id="aec64-129">Members</span></span>

#### <span data-ttu-id="aec64-130">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="aec64-130">BrowserVersionString</span></span> 

<span data-ttu-id="aec64-131">Les informations de la version du navigateur du CoreWebView2Environment actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.</span><span class="sxs-lookup"><span data-stu-id="aec64-131">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="aec64-132">[BrowserVersionString](#browserversionstring) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="aec64-132">public string [BrowserVersionString](#browserversionstring)</span></span>

<span data-ttu-id="aec64-133">Il correspond au format de l’API GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="aec64-133">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="aec64-134">Les noms de canaux sont «bêta», «dev» et «Canaries».</span><span class="sxs-lookup"><span data-stu-id="aec64-134">Channel names are 'beta', 'dev', and 'canary'.</span></span>

#### <span data-ttu-id="aec64-135">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="aec64-135">NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="aec64-136">NewBrowserVersionAvailable se déclenche quand une nouvelle version du navigateur Edge est installée et disponible pour une utilisation via WebView2.</span><span class="sxs-lookup"><span data-stu-id="aec64-136">NewBrowserVersionAvailable fires when a newer version of the Edge browser is installed and available for use via WebView2.</span></span>

> <span data-ttu-id="aec64-137">événement public EventHandler< objet > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span><span class="sxs-lookup"><span data-stu-id="aec64-137">public event EventHandler< object > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span></span>

<span data-ttu-id="aec64-138">Pour utiliser la nouvelle version du navigateur, vous devez créer un environnement et un WebView.</span><span class="sxs-lookup"><span data-stu-id="aec64-138">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="aec64-139">Cet événement est déclenché uniquement pour la nouvelle version à partir du canal Edge à partir duquel le code est exécuté.</span><span class="sxs-lookup"><span data-stu-id="aec64-139">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="aec64-140">S’il n’est pas exécuté avec des bords installés, aucun événement n’est déclenché.</span><span class="sxs-lookup"><span data-stu-id="aec64-140">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="aec64-141">Dans la mesure où un dossier de données utilisateur ne peut être utilisé que par un seul processus de navigateur à la fois, si vous souhaitez utiliser le même dossier de données utilisateur dans les webaffichages à l’aide de la nouvelle version du navigateur, vous devez d’abord fermer l’environnement et les webvues qui utilisent la version antérieure du navigateur.</span><span class="sxs-lookup"><span data-stu-id="aec64-141">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="aec64-142">Vous pouvez également demander à l’utilisateur de redémarrer l’application.</span><span class="sxs-lookup"><span data-stu-id="aec64-142">Or simply prompt the user to restart the app.</span></span>

#### <span data-ttu-id="aec64-143">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="aec64-143">CreateCoreWebView2CompositionControllerAsync</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="aec64-144">Créer de manière asynchrone un nouveau WebView à utiliser avec l’hébergement visuel.</span><span class="sxs-lookup"><span data-stu-id="aec64-144">Asynchronously create a new WebView for use with visual hosting.</span></span>

> <span data-ttu-id="aec64-145">tâche asynchrone publique< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md)  >  [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr FenêtreParent)</span><span class="sxs-lookup"><span data-stu-id="aec64-145">public async Task< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md) > [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="aec64-146">FenêtreParent est le HWND dans lequel l’application relie l’arborescence d’éléments visuels du WebView.</span><span class="sxs-lookup"><span data-stu-id="aec64-146">parentWindow is the HWND in which the app will connect the visual tree of the WebView.</span></span> <span data-ttu-id="aec64-147">Il s’agira du HWND que l’application recevra les entrées de pointeur/souris destinées au WebView (et devront utiliser SendMouseInput/SendPointerInput pour transférer).</span><span class="sxs-lookup"><span data-stu-id="aec64-147">This will be the HWND that the app will receive pointer/ mouse input meant for the WebView (and will need to use SendMouseInput/ SendPointerInput to forward).</span></span> <span data-ttu-id="aec64-148">Si l’application déplace l’arborescence d’éléments visuels WebView vers une autre fenêtre, elle doit définir CoreWebView2CompositionController. FenêtreParent pour mettre à jour le nouveau HWND parent de l’arborescence d’éléments visuels.</span><span class="sxs-lookup"><span data-stu-id="aec64-148">If the app moves the WebView visual tree to underneath a different window, then it needs to set CoreWebView2CompositionController.ParentWindow to update the new parent HWND of the visual tree.</span></span>

<span data-ttu-id="aec64-149">Définissez la propriété RootVisualTarget sur la CoreWebView2CompositionController créée pour fournir un élément visuel permettant d’héberger l’arborescence visuelle du navigateur.</span><span class="sxs-lookup"><span data-stu-id="aec64-149">Set RootVisualTarget property on the created CoreWebView2CompositionController to provide a visual to host the browser's visual tree.</span></span>

<span data-ttu-id="aec64-150">Il est recommandé que l’application définisse l’ID du modèle utilisateur de l’application pour le processus ou la fenêtre de l’application.</span><span class="sxs-lookup"><span data-stu-id="aec64-150">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="aec64-151">Si aucune n’est définie, lors de la création d’un WebView, un ID de modèle utilisateur de l’application généré est défini sur la fenêtre racine de parentWindow.</span><span class="sxs-lookup"><span data-stu-id="aec64-151">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="aec64-152">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="aec64-152">CreateCoreWebView2ControllerAsync</span></span> 

<span data-ttu-id="aec64-153">Créer de manière asynchrone un nouveau WebView.</span><span class="sxs-lookup"><span data-stu-id="aec64-153">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="aec64-154">tâche asynchrone publique< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr FenêtreParent)</span><span class="sxs-lookup"><span data-stu-id="aec64-154">public async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md) > [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="aec64-155">FenêtreParent est le HWND dans lequel le WebView doit être affiché et à partir duquel il est reçu une entrée.</span><span class="sxs-lookup"><span data-stu-id="aec64-155">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="aec64-156">Le WebView ajoutera une fenêtre enfant à la fenêtre fournie lors de la création WebView.</span><span class="sxs-lookup"><span data-stu-id="aec64-156">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="aec64-157">Ordre de plan et autres éléments concernés par l’ordre des fenêtres frères en conséquence.</span><span class="sxs-lookup"><span data-stu-id="aec64-157">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="aec64-158">Il est recommandé que l’application définisse l’ID du modèle utilisateur de l’application pour le processus ou la fenêtre de l’application.</span><span class="sxs-lookup"><span data-stu-id="aec64-158">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="aec64-159">Si aucune n’est définie, lors de la création d’un WebView, un ID de modèle utilisateur de l’application généré est défini sur la fenêtre racine de parentWindow.</span><span class="sxs-lookup"><span data-stu-id="aec64-159">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="aec64-160">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="aec64-160">CreateCoreWebView2PointerInfo</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="aec64-161">Créer un CoreWebView2PointerInfo vide.</span><span class="sxs-lookup"><span data-stu-id="aec64-161">Create an empty CoreWebView2PointerInfo.</span></span>

> <span data-ttu-id="aec64-162">public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span><span class="sxs-lookup"><span data-stu-id="aec64-162">public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span></span>

<span data-ttu-id="aec64-163">La CoreWebView2PointerInfo renvoyée doit être remplie avec toutes les informations pertinentes avant d’appeler SendPointerInput.</span><span class="sxs-lookup"><span data-stu-id="aec64-163">The returned CoreWebView2PointerInfo needs to be populated with all of the relevant info before calling SendPointerInput.</span></span>

#### <span data-ttu-id="aec64-164">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="aec64-164">CreateWebResourceResponse</span></span> 

<span data-ttu-id="aec64-165">Créer un objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="aec64-165">Create a new web resource response object.</span></span>

> <span data-ttu-id="aec64-166">public [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [CreateWebResourceResponse](#createwebresourceresponse)(contenu du flux, StatusCode, int, String ReasonPhrase, en-têtes de chaîne)</span><span class="sxs-lookup"><span data-stu-id="aec64-166">public [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int StatusCode, string ReasonPhrase, string Headers)</span></span>

<span data-ttu-id="aec64-167">Les en-têtes sont les chaînes d’en-tête de réponse brutes délimitées par NewLine.</span><span class="sxs-lookup"><span data-stu-id="aec64-167">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="aec64-168">Il est également possible de créer cet objet avec une chaîne d’en-têtes vide, puis d’utiliser le CoreWebView2HttpResponseHeaders pour créer des en-têtes à l’aide de la fonction ligne.</span><span class="sxs-lookup"><span data-stu-id="aec64-168">It's also possible to create this object with empty headers string and then use the CoreWebView2HttpResponseHeaders to construct the headers line by line.</span></span> <span data-ttu-id="aec64-169">Pour plus d’informations sur les autres paramètres, voir CoreWebView2WebResourceResponse.</span><span class="sxs-lookup"><span data-stu-id="aec64-169">For information on other parameters see CoreWebView2WebResourceResponse.</span></span>

#### <span data-ttu-id="aec64-170">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="aec64-170">GetProviderForHwnd</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="aec64-171">Retourne le fournisseur UI Automation pour le CoreWebView2CompositionController correspondant au HWND donné.</span><span class="sxs-lookup"><span data-stu-id="aec64-171">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

> <span data-ttu-id="aec64-172">[GetProviderForHwnd](#getproviderforhwnd)d’objet public (IntPtr hwnd)</span><span class="sxs-lookup"><span data-stu-id="aec64-172">public object [GetProviderForHwnd](#getproviderforhwnd)(IntPtr hwnd)</span></span>

