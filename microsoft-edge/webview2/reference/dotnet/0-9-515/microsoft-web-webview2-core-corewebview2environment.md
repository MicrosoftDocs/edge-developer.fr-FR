---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 305b25c8db209da4f1e2e54169231ce568e9f5cb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885036"
---
# <span data-ttu-id="95159-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="95159-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2Environment class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="95159-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="95159-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="95159-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="95159-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="95159-107">Il s’agit de l’environnement WebView2.</span><span class="sxs-lookup"><span data-stu-id="95159-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="95159-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="95159-108">Summary</span></span>

 <span data-ttu-id="95159-109">Ses</span><span class="sxs-lookup"><span data-stu-id="95159-109">Members</span></span>                        | <span data-ttu-id="95159-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="95159-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="95159-111">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="95159-111">BrowserVersionString</span></span>](#browserversionstring) | <span data-ttu-id="95159-112">Les informations de la version du navigateur du CoreWebView2Environment actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.</span><span class="sxs-lookup"><span data-stu-id="95159-112">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="95159-113">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="95159-113">NewBrowserVersionAvailable</span></span>](#newbrowserversionavailable) | <span data-ttu-id="95159-114">L’événement NewBrowserVersionAvailable se déclenche lors de l’installation d’une nouvelle version du navigateur Edge et peut être utilisée via WebView2.</span><span class="sxs-lookup"><span data-stu-id="95159-114">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="95159-115">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="95159-115">CreateAsync</span></span>](#createasync) | <span data-ttu-id="95159-116">Crée un environnement WebView2 persistant à l’aide de la version latérale installée.</span><span class="sxs-lookup"><span data-stu-id="95159-116">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="95159-117">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="95159-117">CreateCoreWebView2ControllerAsync</span></span>](#createcorewebview2controllerasync) | <span data-ttu-id="95159-118">Créer de manière asynchrone un nouveau WebView.</span><span class="sxs-lookup"><span data-stu-id="95159-118">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="95159-119">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="95159-119">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="95159-120">Créer un objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="95159-120">Create a new web resource response object.</span></span>

<span data-ttu-id="95159-121">Les webvues créées à partir d’un environnement s’exécutent sur le processus de navigateur spécifié avec des paramètres d’environnement et des objets créés à partir d’un environnement doivent être utilisés dans le même environnement.</span><span class="sxs-lookup"><span data-stu-id="95159-121">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="95159-122">Il n’est pas garanti que l’utilisation de ce dernier dans d’autres environnements est compatible et risque d’échouer.</span><span class="sxs-lookup"><span data-stu-id="95159-122">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="95159-123">Ses</span><span class="sxs-lookup"><span data-stu-id="95159-123">Members</span></span>

#### <span data-ttu-id="95159-124">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="95159-124">BrowserVersionString</span></span> 

<span data-ttu-id="95159-125">Les informations de la version du navigateur du CoreWebView2Environment actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.</span><span class="sxs-lookup"><span data-stu-id="95159-125">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="95159-126">[BrowserVersionString](#browserversionstring) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="95159-126">public string [BrowserVersionString](#browserversionstring)</span></span>

<span data-ttu-id="95159-127">Il correspond au format de l’API GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="95159-127">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="95159-128">Les noms de canaux sont «bêta», «dev» et «Canaries».</span><span class="sxs-lookup"><span data-stu-id="95159-128">Channel names are 'beta', 'dev', and 'canary'.</span></span>

#### <span data-ttu-id="95159-129">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="95159-129">NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="95159-130">L’événement NewBrowserVersionAvailable se déclenche lors de l’installation d’une nouvelle version du navigateur Edge et peut être utilisée via WebView2.</span><span class="sxs-lookup"><span data-stu-id="95159-130">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="95159-131">événement public EventHandler< objet > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span><span class="sxs-lookup"><span data-stu-id="95159-131">public event EventHandler< object > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span></span>

<span data-ttu-id="95159-132">Pour utiliser la nouvelle version du navigateur, vous devez créer un environnement et un WebView.</span><span class="sxs-lookup"><span data-stu-id="95159-132">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="95159-133">Cet événement est déclenché uniquement pour la nouvelle version à partir du canal Edge à partir duquel le code est exécuté.</span><span class="sxs-lookup"><span data-stu-id="95159-133">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="95159-134">S’il n’est pas exécuté avec des bords installés, aucun événement n’est déclenché.</span><span class="sxs-lookup"><span data-stu-id="95159-134">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="95159-135">Dans la mesure où un dossier de données utilisateur ne peut être utilisé que par un seul processus de navigateur à la fois, si vous souhaitez utiliser le même dossier de données utilisateur dans les webaffichages à l’aide de la nouvelle version du navigateur, vous devez d’abord fermer l’environnement et les webvues qui utilisent la version antérieure du navigateur.</span><span class="sxs-lookup"><span data-stu-id="95159-135">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="95159-136">Vous pouvez également demander à l’utilisateur de redémarrer l’application.</span><span class="sxs-lookup"><span data-stu-id="95159-136">Or simply prompt the user to restart the app.</span></span>

#### <span data-ttu-id="95159-137">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="95159-137">CreateAsync</span></span> 

<span data-ttu-id="95159-138">Crée un environnement WebView2 persistant à l’aide de la version latérale installée.</span><span class="sxs-lookup"><span data-stu-id="95159-138">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

> <span data-ttu-id="95159-139">tâches asynchrones publiques< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [CreateAsync](#createasync)(String browserExecutableFolder, String userDataFolder, CoreWebView2EnvironmentOptions options)</span><span class="sxs-lookup"><span data-stu-id="95159-139">public static async Task< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md) > [CreateAsync](#createasync)(string browserExecutableFolder, string userDataFolder, CoreWebView2EnvironmentOptions options)</span></span>

##### <span data-ttu-id="95159-140">Parameters</span><span class="sxs-lookup"><span data-stu-id="95159-140">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="95159-141">Le chemin d’accès relatif au dossier qui contient le bord incorporé.</span><span class="sxs-lookup"><span data-stu-id="95159-141">The relative path to the folder that contains the embedded Edge.</span></span> 

* `userDataFolder` <span data-ttu-id="95159-142">userDataFolder peut être spécifié pour changer l’emplacement du dossier des données utilisateur par défaut pour WebView2.</span><span class="sxs-lookup"><span data-stu-id="95159-142">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> 

* `options` <span data-ttu-id="95159-143">Options permettant de créer un environnement WebView2.</span><span class="sxs-lookup"><span data-stu-id="95159-143">Options used to create WebView2 Environment.</span></span>

#### <span data-ttu-id="95159-144">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="95159-144">CreateCoreWebView2ControllerAsync</span></span> 

<span data-ttu-id="95159-145">Créer de manière asynchrone un nouveau WebView.</span><span class="sxs-lookup"><span data-stu-id="95159-145">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="95159-146">tâche asynchrone publique< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr FenêtreParent)</span><span class="sxs-lookup"><span data-stu-id="95159-146">public async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md) > [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="95159-147">FenêtreParent est le HWND dans lequel le WebView doit être affiché et à partir duquel il est reçu une entrée.</span><span class="sxs-lookup"><span data-stu-id="95159-147">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="95159-148">Le WebView ajoutera une fenêtre enfant à la fenêtre fournie lors de la création WebView.</span><span class="sxs-lookup"><span data-stu-id="95159-148">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="95159-149">Ordre de plan et autres éléments concernés par l’ordre des fenêtres frères en conséquence.</span><span class="sxs-lookup"><span data-stu-id="95159-149">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="95159-150">Il est recommandé que l’application définisse l’ID du modèle utilisateur de l’application pour le processus ou la fenêtre de l’application.</span><span class="sxs-lookup"><span data-stu-id="95159-150">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="95159-151">Si aucune n’est définie, lors de la création d’un WebView, un ID de modèle utilisateur de l’application généré est défini sur la fenêtre racine de parentWindow.</span><span class="sxs-lookup"><span data-stu-id="95159-151">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="95159-152">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="95159-152">CreateWebResourceResponse</span></span> 

<span data-ttu-id="95159-153">Créer un objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="95159-153">Create a new web resource response object.</span></span>

> <span data-ttu-id="95159-154">public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(contenu du flux, StatusCode, int, String ReasonPhrase, en-têtes de chaîne)</span><span class="sxs-lookup"><span data-stu-id="95159-154">public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int StatusCode, string ReasonPhrase, string Headers)</span></span>

<span data-ttu-id="95159-155">Les en-têtes sont les chaînes d’en-tête de réponse brutes délimitées par NewLine.</span><span class="sxs-lookup"><span data-stu-id="95159-155">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="95159-156">Il est également possible de créer cet objet avec une chaîne d’en-têtes vide, puis d’utiliser le CoreWebView2HttpResponseHeaders pour créer des en-têtes à l’aide de la fonction ligne.</span><span class="sxs-lookup"><span data-stu-id="95159-156">It's also possible to create this object with empty headers string and then use the CoreWebView2HttpResponseHeaders to construct the headers line by line.</span></span> <span data-ttu-id="95159-157">Pour plus d’informations sur les autres paramètres, voir CoreWebView2WebResourceResponse.</span><span class="sxs-lookup"><span data-stu-id="95159-157">For information on other parameters see CoreWebView2WebResourceResponse.</span></span>

