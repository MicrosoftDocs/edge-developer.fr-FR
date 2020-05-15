---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 2f376cdd7098c512a8c7a0a3a463f5302f0bfbd7
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653690"
---
# <span data-ttu-id="68996-104">interface ICoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="68996-104">interface ICoreWebView2Environment</span></span> 

> [!NOTE]
> <span data-ttu-id="68996-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="68996-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="68996-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="68996-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Environment
  : public IUnknown
```

<span data-ttu-id="68996-107">Il s’agit de l’environnement WebView2.</span><span class="sxs-lookup"><span data-stu-id="68996-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="68996-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="68996-108">Summary</span></span>

 <span data-ttu-id="68996-109">Ses</span><span class="sxs-lookup"><span data-stu-id="68996-109">Members</span></span>                        | <span data-ttu-id="68996-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="68996-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="68996-111">CreateCoreWebView2Host</span><span class="sxs-lookup"><span data-stu-id="68996-111">CreateCoreWebView2Host</span></span>](#createcorewebview2host) | <span data-ttu-id="68996-112">Créer de manière asynchrone un nouveau WebView.</span><span class="sxs-lookup"><span data-stu-id="68996-112">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="68996-113">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="68996-113">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="68996-114">Créer un objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="68996-114">Create a new web resource response object.</span></span>
[<span data-ttu-id="68996-115">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="68996-115">get_BrowserVersionInfo</span></span>](#get_browserversioninfo) | <span data-ttu-id="68996-116">Les informations de la version du navigateur du [ICoreWebView2Environment]()actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.</span><span class="sxs-lookup"><span data-stu-id="68996-116">The browser version info of the current [ICoreWebView2Environment](), including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="68996-117">add_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="68996-117">add_NewBrowserVersionAvailable</span></span>](#add_newbrowserversionavailable) | <span data-ttu-id="68996-118">L’événement NewBrowserVersionAvailable se déclenche lors de l’installation d’une nouvelle version du navigateur Edge et peut être utilisée via WebView2.</span><span class="sxs-lookup"><span data-stu-id="68996-118">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="68996-119">remove_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="68996-119">remove_NewBrowserVersionAvailable</span></span>](#remove_newbrowserversionavailable) | <span data-ttu-id="68996-120">Supprimez un gestionnaire d’événements préalablement ajouté à add_NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="68996-120">Remove an event handler previously added with add_NewBrowserVersionAvailable.</span></span>

<span data-ttu-id="68996-121">Les webvues créées à partir d’un environnement s’exécutent sur le processus de navigateur spécifié avec des paramètres d’environnement et des objets créés à partir d’un environnement doivent être utilisés dans le même environnement.</span><span class="sxs-lookup"><span data-stu-id="68996-121">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="68996-122">Il n’est pas garanti que l’utilisation de ce dernier dans d’autres environnements est compatible et risque d’échouer.</span><span class="sxs-lookup"><span data-stu-id="68996-122">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="68996-123">Ses</span><span class="sxs-lookup"><span data-stu-id="68996-123">Members</span></span>

#### <span data-ttu-id="68996-124">CreateCoreWebView2Host</span><span class="sxs-lookup"><span data-stu-id="68996-124">CreateCoreWebView2Host</span></span> 

<span data-ttu-id="68996-125">Créer de manière asynchrone un nouveau WebView.</span><span class="sxs-lookup"><span data-stu-id="68996-125">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="68996-126">public HRESULT [CreateCoreWebView2Host](#createcorewebview2host)(HWND ParentWindow, gestionnaire[ICoreWebView2CreateCoreWebView2HostCompletedHandler](ICoreWebView2CreateCoreWebView2HostCompletedHandler.md) \*)</span><span class="sxs-lookup"><span data-stu-id="68996-126">public HRESULT [CreateCoreWebView2Host](#createcorewebview2host)(HWND parentWindow,[ICoreWebView2CreateCoreWebView2HostCompletedHandler](ICoreWebView2CreateCoreWebView2HostCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="68996-127">FenêtreParent est le HWND dans lequel le WebView doit être affiché et à partir duquel il est reçu une entrée.</span><span class="sxs-lookup"><span data-stu-id="68996-127">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="68996-128">Le WebView ajoutera une fenêtre enfant à la fenêtre fournie lors de la création WebView.</span><span class="sxs-lookup"><span data-stu-id="68996-128">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="68996-129">Ordre de plan et autres éléments concernés par l’ordre des fenêtres frères en conséquence.</span><span class="sxs-lookup"><span data-stu-id="68996-129">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="68996-130">Il est recommandé que l’application définisse l’ID du modèle utilisateur de l’application pour le processus ou la fenêtre de l’application.</span><span class="sxs-lookup"><span data-stu-id="68996-130">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="68996-131">Si aucune n’est définie, lors de la création d’un WebView, un ID de modèle utilisateur de l’application généré est défini sur la fenêtre racine de parentWindow.</span><span class="sxs-lookup"><span data-stu-id="68996-131">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span> 

```cpp
// Create or recreate the WebView and its environment.
void AppWindow::InitializeWebView()
{
    // To ensure browser switches get applied correctly, we need to close
    // the existing WebView. This will result in a new browser process
    // getting created which will apply the browser switches.
    CloseWebView();

    LPCWSTR subFolder = nullptr;
    LPCWSTR additionalBrowserSwitches = nullptr;
    HRESULT hr = CreateCoreWebView2EnvironmentWithDetails(
        subFolder, nullptr, additionalBrowserSwitches,
        Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
            this, &AppWindow::OnCreateEnvironmentCompleted)
            .Get());
    if (!SUCCEEDED(hr))
    {
        if (hr == HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND))
        {
            MessageBox(
                m_mainWindow,
                L"Couldn't find Edge installation. "
                "Do you have a version installed that's compatible with this "
                "WebView2 SDK version?",
                nullptr, MB_OK);
        }
        else
        {
            ShowFailure(hr, L"Failed to create webview environment");
        }
    }
}

// This is the callback passed to CreateWebViewEnvironmnetWithDetails.
// Here we simply create the WebView.
HRESULT AppWindow::OnCreateEnvironmentCompleted(
    HRESULT result, ICoreWebView2Environment* environment)
{
    CHECK_FAILURE(result);

    CHECK_FAILURE(environment->QueryInterface(IID_PPV_ARGS(&m_webViewEnvironment)));
        CHECK_FAILURE(m_webViewEnvironment->CreateCoreWebView2Host(
            m_mainWindow, Callback<ICoreWebView2CreateCoreWebView2HostCompletedHandler>(
                              this, &AppWindow::OnCreateCoreWebView2HostCompleted)
                              .Get()));
    return S_OK;
}
```

 <span data-ttu-id="68996-132">Il est recommandé que l’application gère les messages du gestionnaire de redémarrage afin qu’elle puisse être redémarrée harmonieusement dans le cas où l’application utilise Edge pour WebView à partir d’une certaine installation et que cette installation est désinstallée.</span><span class="sxs-lookup"><span data-stu-id="68996-132">It is recommended that the application handles restart manager messages so that it can be restarted gracefully in the case when the app is using Edge for webview from a certain installation and that installation is being uninstalled.</span></span> <span data-ttu-id="68996-133">Par exemple, si un utilisateur installe Edge à partir du canal de développement et décide d’utiliser Edge à partir de ce canal pour tester l’application, puis désinstalle le bord du canal sans fermer l’application, l’application est redémarrée pour permettre la réussite de la désinstallation du canal de développement.</span><span class="sxs-lookup"><span data-stu-id="68996-133">For example, if a user installs Edge from Dev channel and opts to use Edge from that channel for testing the app, and then uninstalls Edge from that channel without closing the app, the app will be restarted to allow uninstallation of the dev channel to succeed.</span></span> 

```cpp
    case WM_QUERYENDSESSION:
    {
        // yes, we can shut down
        // Register how we might be restarted
        RegisterApplicationRestart(L"--restore", RESTART_NO_CRASH | RESTART_NO_HANG);
        *result = TRUE;
        return true;
    }
    break;
    case WM_ENDSESSION:
    {
        if (wParam == TRUE)
        {
            // save app state and exit.
            PostQuitMessage(0);
            return true;
        }
    }
    break;
```

#### <span data-ttu-id="68996-134">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="68996-134">CreateWebResourceResponse</span></span> 

<span data-ttu-id="68996-135">Créer un objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="68996-135">Create a new web resource response object.</span></span>

> <span data-ttu-id="68996-136">public HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(IStream \* content, int STATUSCODE, LPCWSTR reasonPhrase, en-têtes LPCWSTR,[ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="68996-136">public HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(IStream \* content,int statusCode,LPCWSTR reasonPhrase,LPCWSTR headers,[ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \*\* response)</span></span>

<span data-ttu-id="68996-137">Les en-têtes sont les chaînes d’en-tête de réponse brutes délimitées par NewLine.</span><span class="sxs-lookup"><span data-stu-id="68996-137">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="68996-138">Il est également possible de créer cet objet avec une chaîne d’en-têtes vide, puis d’utiliser le [ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) pour créer des en-têtes à l’aide de la fonction ligne.</span><span class="sxs-lookup"><span data-stu-id="68996-138">It's also possible to create this object with empty headers string and then use the [ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) to construct the headers line by line.</span></span> <span data-ttu-id="68996-139">Pour plus d’informations sur les autres paramètres, voir [ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md).</span><span class="sxs-lookup"><span data-stu-id="68996-139">For information on other parameters see [ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md).</span></span>

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<ICoreWebView2WebResourceRequestedEventHandler>(
                    [this](
                        ICoreWebView2* sender,
                        ICoreWebView2WebResourceRequestedEventArgs* args) {
                        CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            args->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<ICoreWebView2WebResourceResponse> response;
                        CHECK_FAILURE(m_webViewEnvironment->CreateWebResourceResponse(
                            nullptr, 403 /*NoContent*/, L"Blocked", L"", &response));
                        CHECK_FAILURE(args->put_Response(response.get()));
                        return S_OK;
                    })
                    .Get(),
                &m_webResourceRequestedTokenForImageBlocking));
        }
        else
        {
            CHECK_FAILURE(m_webView->remove_WebResourceRequested(
                m_webResourceRequestedTokenForImageBlocking));
        }
```

#### <span data-ttu-id="68996-140">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="68996-140">get_BrowserVersionInfo</span></span> 

<span data-ttu-id="68996-141">Les informations de la version du navigateur du [ICoreWebView2Environment]()actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.</span><span class="sxs-lookup"><span data-stu-id="68996-141">The browser version info of the current [ICoreWebView2Environment](), including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="68996-142">valeur publique HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* VERSIONINFO)</span><span class="sxs-lookup"><span data-stu-id="68996-142">public HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="68996-143">Il correspond au format de l’API GetCoreWebView2BrowserVersionInfo.</span><span class="sxs-lookup"><span data-stu-id="68996-143">This matches the format of the GetCoreWebView2BrowserVersionInfo API.</span></span> <span data-ttu-id="68996-144">Les noms de canaux sont «bêta», «dev» et «Canaries».</span><span class="sxs-lookup"><span data-stu-id="68996-144">Channel names are 'beta', 'dev', and 'canary'.</span></span>

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionInfo(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

#### <span data-ttu-id="68996-145">add_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="68996-145">add_NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="68996-146">L’événement NewBrowserVersionAvailable se déclenche lors de l’installation d’une nouvelle version du navigateur Edge et peut être utilisée via WebView2.</span><span class="sxs-lookup"><span data-stu-id="68996-146">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="68996-147">[add_NewBrowserVersionAvailable](#add_newbrowserversionavailable)par le biais du[mot de passe](ICoreWebView2NewBrowserVersionAvailableEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="68996-147">public HRESULT [add_NewBrowserVersionAvailable](#add_newbrowserversionavailable)([ICoreWebView2NewBrowserVersionAvailableEventHandler](ICoreWebView2NewBrowserVersionAvailableEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="68996-148">Pour utiliser la nouvelle version du navigateur, vous devez créer un environnement et un WebView.</span><span class="sxs-lookup"><span data-stu-id="68996-148">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="68996-149">Cet événement est déclenché uniquement pour la nouvelle version à partir du canal Edge à partir duquel le code est exécuté.</span><span class="sxs-lookup"><span data-stu-id="68996-149">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="68996-150">S’il n’est pas exécuté avec des bords installés, aucun événement n’est déclenché.</span><span class="sxs-lookup"><span data-stu-id="68996-150">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="68996-151">Dans la mesure où un dossier de données utilisateur ne peut être utilisé que par un seul processus de navigateur à la fois, si vous souhaitez utiliser le même dossier de données utilisateur dans les webaffichages à l’aide de la nouvelle version du navigateur, vous devez d’abord fermer l’environnement et les webvues qui utilisent la version antérieure du navigateur.</span><span class="sxs-lookup"><span data-stu-id="68996-151">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="68996-152">Vous pouvez également demander à l’utilisateur de redémarrer l’application.</span><span class="sxs-lookup"><span data-stu-id="68996-152">Or simply prompt the user to restart the app.</span></span>

```cpp
    // After the environment is successfully created,
    // register a handler for the NewBrowserVersionAvailable event.
    // This handler tells when there is a new Edge version available on the machine.
    CHECK_FAILURE(m_webViewEnvironment->add_NewBrowserVersionAvailable(
        Callback<ICoreWebView2NewBrowserVersionAvailableEventHandler>(
            [this](
                ICoreWebView2Environment* sender,
                ICoreWebView2NewBrowserVersionAvailableEventArgs* args) -> HRESULT {
                // Get the version value from args
                wil::unique_cotaskmem_string newVersion;
                CHECK_FAILURE(args->get_NewVersion(&newVersion));
                std::wstring message = L"We detected there is a new version for the browser.";
                message += L"\n\nVersion number: ";
                message += newVersion.get();
                message += L"\n\n";
                if (m_webView)
                {
                    message += L"Do you want to restart the app? \n\n";
                    message += L"Click No if you only want to re-create the webviews. \n";
                    message += L"Click Cancel for no action. \n";
                }
                int response = MessageBox(
                    m_mainWindow, message.c_str(), L"New available version",
                    m_webView ? MB_YESNOCANCEL : MB_OK);

                if (response == IDYES)
                {
                    RestartApp();
                }
                else if (response == IDNO)
                {
                    ReinitializeWebViewWithNewBrowser();
                }
                else
                {
                    // do nothing
                }

                return S_OK;
            })
            .Get(),
        nullptr));
```

#### <span data-ttu-id="68996-153">remove_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="68996-153">remove_NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="68996-154">Supprimez un gestionnaire d’événements préalablement ajouté à add_NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="68996-154">Remove an event handler previously added with add_NewBrowserVersionAvailable.</span></span>

> <span data-ttu-id="68996-155">[remove_NewBrowserVersionAvailable](#remove_newbrowserversionavailable)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="68996-155">public HRESULT [remove_NewBrowserVersionAvailable](#remove_newbrowserversionavailable)(EventRegistrationToken token)</span></span>

