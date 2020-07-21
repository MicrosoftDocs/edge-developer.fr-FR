---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: ab0bacf73e1b354811024cb50927a576bb2505aa
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883811"
---
# <span data-ttu-id="77e7c-104">0.9.515-interface ICoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="77e7c-104">0.9.515 - interface ICoreWebView2Environment</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2Environment
  : public IUnknown
```

<span data-ttu-id="77e7c-105">Il s’agit de l’environnement WebView2.</span><span class="sxs-lookup"><span data-stu-id="77e7c-105">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="77e7c-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="77e7c-106">Summary</span></span>

 <span data-ttu-id="77e7c-107">Ses</span><span class="sxs-lookup"><span data-stu-id="77e7c-107">Members</span></span>                        | <span data-ttu-id="77e7c-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="77e7c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="77e7c-109">add_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="77e7c-109">add_NewBrowserVersionAvailable</span></span>](#add_newbrowserversionavailable) | <span data-ttu-id="77e7c-110">L’événement NewBrowserVersionAvailable se déclenche lors de l’installation d’une nouvelle version du navigateur Edge et peut être utilisée via WebView2.</span><span class="sxs-lookup"><span data-stu-id="77e7c-110">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="77e7c-111">CreateCoreWebView2Controller</span><span class="sxs-lookup"><span data-stu-id="77e7c-111">CreateCoreWebView2Controller</span></span>](#createcorewebview2controller) | <span data-ttu-id="77e7c-112">Créer de manière asynchrone un nouveau WebView.</span><span class="sxs-lookup"><span data-stu-id="77e7c-112">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="77e7c-113">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="77e7c-113">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="77e7c-114">Créer un objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="77e7c-114">Create a new web resource response object.</span></span>
[<span data-ttu-id="77e7c-115">get_BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="77e7c-115">get_BrowserVersionString</span></span>](#get_browserversionstring) | <span data-ttu-id="77e7c-116">Les informations de la version du navigateur du [ICoreWebView2Environment]()actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.</span><span class="sxs-lookup"><span data-stu-id="77e7c-116">The browser version info of the current [ICoreWebView2Environment](), including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="77e7c-117">remove_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="77e7c-117">remove_NewBrowserVersionAvailable</span></span>](#remove_newbrowserversionavailable) | <span data-ttu-id="77e7c-118">Supprimez un gestionnaire d’événements préalablement ajouté à add_NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="77e7c-118">Remove an event handler previously added with add_NewBrowserVersionAvailable.</span></span>

<span data-ttu-id="77e7c-119">Les webvues créées à partir d’un environnement s’exécutent sur le processus de navigateur spécifié avec des paramètres d’environnement et des objets créés à partir d’un environnement doivent être utilisés dans le même environnement.</span><span class="sxs-lookup"><span data-stu-id="77e7c-119">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="77e7c-120">Il n’est pas garanti que l’utilisation de ce dernier dans d’autres environnements est compatible et risque d’échouer.</span><span class="sxs-lookup"><span data-stu-id="77e7c-120">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="77e7c-121">Ses</span><span class="sxs-lookup"><span data-stu-id="77e7c-121">Members</span></span>

#### <span data-ttu-id="77e7c-122">add_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="77e7c-122">add_NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="77e7c-123">L’événement NewBrowserVersionAvailable se déclenche lors de l’installation d’une nouvelle version du navigateur Edge et peut être utilisée via WebView2.</span><span class="sxs-lookup"><span data-stu-id="77e7c-123">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="77e7c-124">[add_NewBrowserVersionAvailable](#add_newbrowserversionavailable)par le biais du[mot de passe](icorewebview2newbrowserversionavailableeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="77e7c-124">public HRESULT [add_NewBrowserVersionAvailable](#add_newbrowserversionavailable)([ICoreWebView2NewBrowserVersionAvailableEventHandler](icorewebview2newbrowserversionavailableeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="77e7c-125">Pour utiliser la nouvelle version du navigateur, vous devez créer un environnement et un WebView.</span><span class="sxs-lookup"><span data-stu-id="77e7c-125">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="77e7c-126">Cet événement est déclenché uniquement pour la nouvelle version à partir du canal Edge à partir duquel le code est exécuté.</span><span class="sxs-lookup"><span data-stu-id="77e7c-126">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="77e7c-127">S’il n’est pas exécuté avec des bords installés, aucun événement n’est déclenché.</span><span class="sxs-lookup"><span data-stu-id="77e7c-127">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="77e7c-128">Dans la mesure où un dossier de données utilisateur ne peut être utilisé que par un seul processus de navigateur à la fois, si vous souhaitez utiliser le même dossier de données utilisateur dans les webaffichages à l’aide de la nouvelle version du navigateur, vous devez d’abord fermer l’environnement et les webvues qui utilisent la version antérieure du navigateur.</span><span class="sxs-lookup"><span data-stu-id="77e7c-128">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="77e7c-129">Vous pouvez également demander à l’utilisateur de redémarrer l’application.</span><span class="sxs-lookup"><span data-stu-id="77e7c-129">Or simply prompt the user to restart the app.</span></span>

```cpp
    // After the environment is successfully created,
    // register a handler for the NewBrowserVersionAvailable event.
    // This handler tells when there is a new Edge version available on the machine.
    CHECK_FAILURE(m_webViewEnvironment->add_NewBrowserVersionAvailable(
        Callback<ICoreWebView2NewBrowserVersionAvailableEventHandler>(
            [this](ICoreWebView2Environment* sender, IUnknown* args) -> HRESULT {
                std::wstring message = L"We detected there is a new version for the browser.";
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

#### <span data-ttu-id="77e7c-130">CreateCoreWebView2Controller</span><span class="sxs-lookup"><span data-stu-id="77e7c-130">CreateCoreWebView2Controller</span></span> 

<span data-ttu-id="77e7c-131">Créer de manière asynchrone un nouveau WebView.</span><span class="sxs-lookup"><span data-stu-id="77e7c-131">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="77e7c-132">public HRESULT [CreateCoreWebView2Controller](#createcorewebview2controller)(HWND ParentWindow, gestionnaire [ICoreWebView2CreateCoreWebView2ControllerCompletedHandler](icorewebview2createcorewebview2controllercompletedhandler.md) \*)</span><span class="sxs-lookup"><span data-stu-id="77e7c-132">public HRESULT [CreateCoreWebView2Controller](#createcorewebview2controller)(HWND parentWindow, [ICoreWebView2CreateCoreWebView2ControllerCompletedHandler](icorewebview2createcorewebview2controllercompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="77e7c-133">FenêtreParent est le HWND dans lequel le WebView doit être affiché et à partir duquel il est reçu une entrée.</span><span class="sxs-lookup"><span data-stu-id="77e7c-133">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="77e7c-134">Le WebView ajoutera une fenêtre enfant à la fenêtre fournie lors de la création WebView.</span><span class="sxs-lookup"><span data-stu-id="77e7c-134">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="77e7c-135">Ordre de plan et autres éléments concernés par l’ordre des fenêtres frères en conséquence.</span><span class="sxs-lookup"><span data-stu-id="77e7c-135">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="77e7c-136">Il est recommandé que l’application définisse l’ID du modèle utilisateur de l’application pour le processus ou la fenêtre de l’application.</span><span class="sxs-lookup"><span data-stu-id="77e7c-136">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="77e7c-137">Si aucune n’est définie, lors de la création d’un WebView, un ID de modèle utilisateur de l’application généré est défini sur la fenêtre racine de parentWindow.</span><span class="sxs-lookup"><span data-stu-id="77e7c-137">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span> 
```cpp
// Create or recreate the WebView and its environment.
void AppWindow::InitializeWebView()
{
    // To ensure browser switches get applied correctly, we need to close
    // the existing WebView. This will result in a new browser process
    // getting created which will apply the browser switches.
    CloseWebView();
    m_dcompDevice = nullptr;
    m_wincompHelper = nullptr;

    LPCWSTR subFolder = nullptr;

    if (m_creationModeId == IDM_CREATION_MODE_VISUAL_DCOMP)
    {
        HRESULT hr = DCompositionCreateDevice2(nullptr, IID_PPV_ARGS(&m_dcompDevice));
        if (!SUCCEEDED(hr))
        {
            MessageBox(
                m_mainWindow,
                L"Attempting to create WebView using DComp Visual is not supported.\r\n"
                "DComp device creation failed.\r\n"
                "Current OS may not support DComp.",
                L"Create with Windowless DComp Visual Failed", MB_OK);
            return;
        }
    }
    else if (m_creationModeId == IDM_CREATION_MODE_VISUAL_WINCOMP)
    {
        HRESULT hr = CreateWinCompCompositor();
        if (!SUCCEEDED(hr))
        {
            MessageBox(
                m_mainWindow,
                L"Attempting to create WebView using WinComp Visual is not supported.\r\n"
                "WinComp compositor creation failed.\r\n"
                "Current OS may not support WinComp.",
                L"Create with Windowless WinComp Visual Failed", MB_OK);
            return;
        }
    }
    auto options = Microsoft::WRL::Make<CoreWebView2EnvironmentOptions>();
    if(!m_language.empty())
        CHECK_FAILURE(options->put_Language(m_language.c_str()));
    HRESULT hr = CreateCoreWebView2EnvironmentWithOptions(
        subFolder, nullptr, options.Get(),
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

// This is the callback passed to CreateWebViewEnvironmentWithOptions.
// Here we simply create the WebView.
HRESULT AppWindow::OnCreateEnvironmentCompleted(
    HRESULT result, ICoreWebView2Environment* environment)
{
    CHECK_FAILURE(result);

    m_webViewEnvironment = environment;

    auto webViewExperimentalEnvironment =
        m_webViewEnvironment.try_query<ICoreWebView2ExperimentalEnvironment>();
    if (webViewExperimentalEnvironment && (m_dcompDevice || m_wincompHelper))
    {
        CHECK_FAILURE(webViewExperimentalEnvironment->CreateCoreWebView2CompositionController(
            m_mainWindow,
            Callback<
                ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler>(
                [this](
                    HRESULT result,
                    ICoreWebView2ExperimentalCompositionController* compositionController) -> HRESULT {
                    auto controller =
                        wil::com_ptr<ICoreWebView2ExperimentalCompositionController>(compositionController)
                            .query<ICoreWebView2Controller>();
                    return OnCreateCoreWebView2ControllerCompleted(result, controller.get());
                })
                .Get()));
    }
    else
    {
        CHECK_FAILURE(m_webViewEnvironment->CreateCoreWebView2Controller(
            m_mainWindow, Callback<ICoreWebView2CreateCoreWebView2ControllerCompletedHandler>(
                              this, &AppWindow::OnCreateCoreWebView2ControllerCompleted)
                              .Get()));
    }

    return S_OK;
}
```
 <span data-ttu-id="77e7c-138">Il est recommandé que l’application gère les messages du gestionnaire de redémarrage afin qu’elle puisse être redémarrée harmonieusement dans le cas où l’application utilise Edge pour WebView à partir d’une certaine installation et que cette installation est désinstallée.</span><span class="sxs-lookup"><span data-stu-id="77e7c-138">It is recommended that the application handles restart manager messages so that it can be restarted gracefully in the case when the app is using Edge for webview from a certain installation and that installation is being uninstalled.</span></span> <span data-ttu-id="77e7c-139">Par exemple, si un utilisateur installe Edge à partir du canal de développement et décide d’utiliser Edge à partir de ce canal pour tester l’application, puis désinstalle le bord du canal sans fermer l’application, l’application est redémarrée pour permettre la réussite de la désinstallation du canal de développement.</span><span class="sxs-lookup"><span data-stu-id="77e7c-139">For example, if a user installs Edge from Dev channel and opts to use Edge from that channel for testing the app, and then uninstalls Edge from that channel without closing the app, the app will be restarted to allow uninstallation of the dev channel to succeed.</span></span> 
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
 <span data-ttu-id="77e7c-140">Lorsque l’application tente de CreateCoreWebView2Controller en cas d’échec, il est recommandé de redémarrer l’application à partir de la création d’un nouvel environnement WebView2.</span><span class="sxs-lookup"><span data-stu-id="77e7c-140">When the application retries CreateCoreWebView2Controller upon failure, it is recommended that the application restarts from creating a new WebView2 Environment.</span></span> <span data-ttu-id="77e7c-141">En cas de mise à jour latérale, la version associée à un environnement WebView2 peut avoir été supprimée et provoquer le fonctionnement de l’objet.</span><span class="sxs-lookup"><span data-stu-id="77e7c-141">If an Edge update happens, the version associated with a WebView2 Environment could have been removed and causing the object to no longer work.</span></span> <span data-ttu-id="77e7c-142">La création d’un nouvel environnement WebView2 fonctionnera comme la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="77e7c-142">Creating a new WebView2 Environment will work as it uses the latest version.</span></span>

<span data-ttu-id="77e7c-143">La création du WebView échoue si une instance est déjà en cours d’exécution en utilisant le même dossier de données utilisateur, et les objets d’environnement ont des EnvironmentOptions différents.</span><span class="sxs-lookup"><span data-stu-id="77e7c-143">WebView creation will fail if there is already a running instance using the same user data folder, and the Environment objects have different EnvironmentOptions.</span></span> <span data-ttu-id="77e7c-144">Par exemple, si un WebView est déjà créé avec une langue, il est possible de créer un WebView avec une autre langue à l’aide du même dossier de données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="77e7c-144">For example, if there is already a WebView created with one language, trying to create a WebView with a different language using the same user data folder will fail.</span></span>

#### <span data-ttu-id="77e7c-145">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="77e7c-145">CreateWebResourceResponse</span></span> 

<span data-ttu-id="77e7c-146">Créer un objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="77e7c-146">Create a new web resource response object.</span></span>

> <span data-ttu-id="77e7c-147">public HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(IStream \* content, int STATUSCODE, LPCWSTR reasonPhrase, en-têtes LPCWSTR, [ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="77e7c-147">public HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(IStream \* content, int statusCode, LPCWSTR reasonPhrase, LPCWSTR headers, [ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

<span data-ttu-id="77e7c-148">Les en-têtes sont les chaînes d’en-tête de réponse brutes délimitées par NewLine.</span><span class="sxs-lookup"><span data-stu-id="77e7c-148">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="77e7c-149">Il est également possible de créer cet objet avec une chaîne d’en-têtes vide, puis d’utiliser le [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) pour créer des en-têtes à l’aide de la fonction ligne.</span><span class="sxs-lookup"><span data-stu-id="77e7c-149">It's also possible to create this object with empty headers string and then use the [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) to construct the headers line by line.</span></span> <span data-ttu-id="77e7c-150">Pour plus d’informations sur les autres paramètres, voir [ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md).</span><span class="sxs-lookup"><span data-stu-id="77e7c-150">For information on other parameters see [ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md).</span></span>

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<ICoreWebView2WebResourceRequestedEventHandler>(
                    [this](
                        ICoreWebView2* sender,
                        ICoreWebView2WebResourceRequestedEventArgs* args) {
                        COREWEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            args->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
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

#### <span data-ttu-id="77e7c-151">get_BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="77e7c-151">get_BrowserVersionString</span></span> 

<span data-ttu-id="77e7c-152">Les informations de la version du navigateur du [ICoreWebView2Environment]()actuel, y compris le nom du canal s’il ne s’agit pas du canal stable.</span><span class="sxs-lookup"><span data-stu-id="77e7c-152">The browser version info of the current [ICoreWebView2Environment](), including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="77e7c-153">valeur publique HRESULT [get_BrowserVersionString](#get_browserversionstring)(LPWSTR \* VERSIONINFO)</span><span class="sxs-lookup"><span data-stu-id="77e7c-153">public HRESULT [get_BrowserVersionString](#get_browserversionstring)(LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="77e7c-154">Il correspond au format de l’API GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="77e7c-154">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="77e7c-155">Les noms de canaux sont «bêta», «dev» et «Canaries».</span><span class="sxs-lookup"><span data-stu-id="77e7c-155">Channel names are 'beta', 'dev', and 'canary'.</span></span>

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionString(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

#### <span data-ttu-id="77e7c-156">remove_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="77e7c-156">remove_NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="77e7c-157">Supprimez un gestionnaire d’événements préalablement ajouté à add_NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="77e7c-157">Remove an event handler previously added with add_NewBrowserVersionAvailable.</span></span>

> <span data-ttu-id="77e7c-158">[remove_NewBrowserVersionAvailable](#remove_newbrowserversionavailable)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="77e7c-158">public HRESULT [remove_NewBrowserVersionAvailable](#remove_newbrowserversionavailable)(EventRegistrationToken token)</span></span>

