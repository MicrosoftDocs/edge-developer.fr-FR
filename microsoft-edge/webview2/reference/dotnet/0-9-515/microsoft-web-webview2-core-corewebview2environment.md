---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 986b1dc2870375243a0ee664262216105edd95a8
ms.sourcegitcommit: 3f8c8a5643e416b0851254833f9771192883ec45
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699499"
---
# <span data-ttu-id="1a134-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="1a134-104">Microsoft.Web.WebView2.Core.CoreWebView2Environment class</span></span> 

> [!NOTE]
> <span data-ttu-id="1a134-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="1a134-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="1a134-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="1a134-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="1a134-107">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="1a134-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="1a134-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="1a134-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="1a134-109">Il s’agit de l’environnement WebView2.</span><span class="sxs-lookup"><span data-stu-id="1a134-109">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="1a134-110">Résumé</span><span class="sxs-lookup"><span data-stu-id="1a134-110">Summary</span></span>

 <span data-ttu-id="1a134-111">Ses</span><span class="sxs-lookup"><span data-stu-id="1a134-111">Members</span></span>                        | <span data-ttu-id="1a134-112">Descriptions</span><span class="sxs-lookup"><span data-stu-id="1a134-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1a134-113">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="1a134-113">BrowserVersionString</span></span>](#browserversionstring) | <span data-ttu-id="1a134-114">Les informations de la version du navigateur du CoreWebView2Environment actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.</span><span class="sxs-lookup"><span data-stu-id="1a134-114">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="1a134-115">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="1a134-115">NewBrowserVersionAvailable</span></span>](#newbrowserversionavailable) | <span data-ttu-id="1a134-116">L’événement NewBrowserVersionAvailable se déclenche lors de l’installation d’une nouvelle version du navigateur Edge et peut être utilisée via WebView2.</span><span class="sxs-lookup"><span data-stu-id="1a134-116">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="1a134-117">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="1a134-117">CreateAsync</span></span>](#createasync) | <span data-ttu-id="1a134-118">Crée un environnement WebView2 persistant à l’aide de la version latérale installée.</span><span class="sxs-lookup"><span data-stu-id="1a134-118">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="1a134-119">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="1a134-119">CreateCoreWebView2ControllerAsync</span></span>](#createcorewebview2controllerasync) | <span data-ttu-id="1a134-120">Créer de manière asynchrone un nouveau WebView.</span><span class="sxs-lookup"><span data-stu-id="1a134-120">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="1a134-121">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="1a134-121">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="1a134-122">Créer un objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="1a134-122">Create a new web resource response object.</span></span>

<span data-ttu-id="1a134-123">Les webvues créées à partir d’un environnement s’exécutent sur le processus de navigateur spécifié avec des paramètres d’environnement et des objets créés à partir d’un environnement doivent être utilisés dans le même environnement.</span><span class="sxs-lookup"><span data-stu-id="1a134-123">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="1a134-124">Il n’est pas garanti que l’utilisation de ce dernier dans d’autres environnements est compatible et risque d’échouer.</span><span class="sxs-lookup"><span data-stu-id="1a134-124">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="1a134-125">Ses</span><span class="sxs-lookup"><span data-stu-id="1a134-125">Members</span></span>

#### <span data-ttu-id="1a134-126">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="1a134-126">BrowserVersionString</span></span> 

<span data-ttu-id="1a134-127">Les informations de la version du navigateur du CoreWebView2Environment actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.</span><span class="sxs-lookup"><span data-stu-id="1a134-127">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="1a134-128">[BrowserVersionString](#browserversionstring) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="1a134-128">public string [BrowserVersionString](#browserversionstring)</span></span>

<span data-ttu-id="1a134-129">Il correspond au format de l’API GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="1a134-129">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="1a134-130">Les noms de canaux sont «bêta», «dev» et «Canaries».</span><span class="sxs-lookup"><span data-stu-id="1a134-130">Channel names are 'beta', 'dev', and 'canary'.</span></span>

#### <span data-ttu-id="1a134-131">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="1a134-131">NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="1a134-132">L’événement NewBrowserVersionAvailable se déclenche lors de l’installation d’une nouvelle version du navigateur Edge et peut être utilisée via WebView2.</span><span class="sxs-lookup"><span data-stu-id="1a134-132">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="1a134-133">événement public EventHandler< objet > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span><span class="sxs-lookup"><span data-stu-id="1a134-133">public event EventHandler< object > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span></span>

<span data-ttu-id="1a134-134">Pour utiliser la nouvelle version du navigateur, vous devez créer un environnement et un WebView.</span><span class="sxs-lookup"><span data-stu-id="1a134-134">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="1a134-135">Cet événement est déclenché uniquement pour la nouvelle version à partir du canal Edge à partir duquel le code est exécuté.</span><span class="sxs-lookup"><span data-stu-id="1a134-135">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="1a134-136">S’il n’est pas exécuté avec des bords installés, aucun événement n’est déclenché.</span><span class="sxs-lookup"><span data-stu-id="1a134-136">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="1a134-137">Dans la mesure où un dossier de données utilisateur ne peut être utilisé que par un seul processus de navigateur à la fois, si vous souhaitez utiliser le même dossier de données utilisateur dans les webaffichages à l’aide de la nouvelle version du navigateur, vous devez d’abord fermer l’environnement et les webvues qui utilisent la version antérieure du navigateur.</span><span class="sxs-lookup"><span data-stu-id="1a134-137">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="1a134-138">Vous pouvez également demander à l’utilisateur de redémarrer l’application.</span><span class="sxs-lookup"><span data-stu-id="1a134-138">Or simply prompt the user to restart the app.</span></span>

#### <span data-ttu-id="1a134-139">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="1a134-139">CreateAsync</span></span> 

<span data-ttu-id="1a134-140">Crée un environnement WebView2 persistant à l’aide de la version latérale installée.</span><span class="sxs-lookup"><span data-stu-id="1a134-140">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

> <span data-ttu-id="1a134-141">tâches asynchrones publiques< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [CreateAsync](#createasync)(String browserExecutableFolder, String userDataFolder, CoreWebView2EnvironmentOptions options)</span><span class="sxs-lookup"><span data-stu-id="1a134-141">public static async Task< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md) > [CreateAsync](#createasync)(string browserExecutableFolder, string userDataFolder, CoreWebView2EnvironmentOptions options)</span></span>

##### <span data-ttu-id="1a134-142">Parameters</span><span class="sxs-lookup"><span data-stu-id="1a134-142">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="1a134-143">Le chemin d’accès relatif au dossier qui contient le bord incorporé.</span><span class="sxs-lookup"><span data-stu-id="1a134-143">The relative path to the folder that contains the embedded Edge.</span></span> 

* `userDataFolder` <span data-ttu-id="1a134-144">userDataFolder peut être spécifié pour changer l’emplacement du dossier des données utilisateur par défaut pour WebView2.</span><span class="sxs-lookup"><span data-stu-id="1a134-144">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> 

* `options` <span data-ttu-id="1a134-145">Options permettant de créer un environnement WebView2.</span><span class="sxs-lookup"><span data-stu-id="1a134-145">Options used to create WebView2 Environment.</span></span>

#### <span data-ttu-id="1a134-146">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="1a134-146">CreateCoreWebView2ControllerAsync</span></span> 

<span data-ttu-id="1a134-147">Créer de manière asynchrone un nouveau WebView.</span><span class="sxs-lookup"><span data-stu-id="1a134-147">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="1a134-148">tâche asynchrone publique< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr FenêtreParent)</span><span class="sxs-lookup"><span data-stu-id="1a134-148">public async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md) > [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="1a134-149">FenêtreParent est le HWND dans lequel le WebView doit être affiché et à partir duquel il est reçu une entrée.</span><span class="sxs-lookup"><span data-stu-id="1a134-149">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="1a134-150">Le WebView ajoutera une fenêtre enfant à la fenêtre fournie lors de la création WebView.</span><span class="sxs-lookup"><span data-stu-id="1a134-150">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="1a134-151">Ordre de plan et autres éléments concernés par l’ordre des fenêtres frères en conséquence.</span><span class="sxs-lookup"><span data-stu-id="1a134-151">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="1a134-152">Il est recommandé que l’application définisse l’ID du modèle utilisateur de l’application pour le processus ou la fenêtre de l’application.</span><span class="sxs-lookup"><span data-stu-id="1a134-152">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="1a134-153">Si aucune n’est définie, lors de la création d’un WebView, un ID de modèle utilisateur de l’application généré est défini sur la fenêtre racine de parentWindow.</span><span class="sxs-lookup"><span data-stu-id="1a134-153">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="1a134-154">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="1a134-154">CreateWebResourceResponse</span></span> 

<span data-ttu-id="1a134-155">Créer un objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="1a134-155">Create a new web resource response object.</span></span>

> <span data-ttu-id="1a134-156">public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(contenu du flux, StatusCode, int, String ReasonPhrase, en-têtes de chaîne)</span><span class="sxs-lookup"><span data-stu-id="1a134-156">public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int StatusCode, string ReasonPhrase, string Headers)</span></span>

<span data-ttu-id="1a134-157">Les en-têtes sont les chaînes d’en-tête de réponse brutes délimitées par NewLine.</span><span class="sxs-lookup"><span data-stu-id="1a134-157">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="1a134-158">Il est également possible de créer cet objet avec une chaîne d’en-têtes vide, puis d’utiliser le CoreWebView2HttpResponseHeaders pour créer des en-têtes à l’aide de la fonction ligne.</span><span class="sxs-lookup"><span data-stu-id="1a134-158">It's also possible to create this object with empty headers string and then use the CoreWebView2HttpResponseHeaders to construct the headers line by line.</span></span> <span data-ttu-id="1a134-159">Pour plus d’informations sur les autres paramètres, voir CoreWebView2WebResourceResponse.</span><span class="sxs-lookup"><span data-stu-id="1a134-159">For information on other parameters see CoreWebView2WebResourceResponse.</span></span>

