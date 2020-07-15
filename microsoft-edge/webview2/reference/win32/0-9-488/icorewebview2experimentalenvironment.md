---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2ExperimentalEnvironment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: d5b41334ad3c46e1a3d2e8642479555f2062c1c2
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880618"
---
# <span data-ttu-id="eb28c-104">0.9.515-interface ICoreWebView2ExperimentalEnvironment</span><span class="sxs-lookup"><span data-stu-id="eb28c-104">0.9.515 - interface ICoreWebView2ExperimentalEnvironment</span></span> 

> [!NOTE]
> <span data-ttu-id="eb28c-105">Cette API expérimentale qui est fournie avec notre version bêta du SDK version 0.9.488.</span><span class="sxs-lookup"><span data-stu-id="eb28c-105">This an experimental API that is shipped with our prerelease SDK version 0.9.488.</span></span>

```
interface ICoreWebView2ExperimentalEnvironment
  : public IUnknown
```

<span data-ttu-id="eb28c-106">Cette interface est une extension du [ICoreWebView2Environment](icorewebview2environment.md).</span><span class="sxs-lookup"><span data-stu-id="eb28c-106">This interface is an extension of the [ICoreWebView2Environment](icorewebview2environment.md).</span></span>

## <span data-ttu-id="eb28c-107">Résumé</span><span class="sxs-lookup"><span data-stu-id="eb28c-107">Summary</span></span>

 <span data-ttu-id="eb28c-108">Ses</span><span class="sxs-lookup"><span data-stu-id="eb28c-108">Members</span></span>                        | <span data-ttu-id="eb28c-109">Descriptions</span><span class="sxs-lookup"><span data-stu-id="eb28c-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="eb28c-110">CreateCoreWebView2CompositionController</span><span class="sxs-lookup"><span data-stu-id="eb28c-110">CreateCoreWebView2CompositionController</span></span>](#createcorewebview2compositioncontroller) | <span data-ttu-id="eb28c-111">Créer de manière asynchrone un nouveau WebView à utiliser avec l’hébergement visuel.</span><span class="sxs-lookup"><span data-stu-id="eb28c-111">Asynchronously create a new WebView for use with visual hosting.</span></span>
[<span data-ttu-id="eb28c-112">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="eb28c-112">CreateCoreWebView2PointerInfo</span></span>](#createcorewebview2pointerinfo) | <span data-ttu-id="eb28c-113">Créer un [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md)vide.</span><span class="sxs-lookup"><span data-stu-id="eb28c-113">Create an empty [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span></span>
[<span data-ttu-id="eb28c-114">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="eb28c-114">GetProviderForHwnd</span></span>](#getproviderforhwnd) | <span data-ttu-id="eb28c-115">Retourne le fournisseur UI Automation pour le ICoreWebView2CompositionController correspondant au HWND donné.</span><span class="sxs-lookup"><span data-stu-id="eb28c-115">Returns the UI Automation Provider for the ICoreWebView2CompositionController that corresponds with the given HWND.</span></span>

<span data-ttu-id="eb28c-116">Un objet qui implémente l’interface [ICoreWebView2ExperimentalEnvironment]() implémente également [ICoreWebView2Environment](icorewebview2environment.md).</span><span class="sxs-lookup"><span data-stu-id="eb28c-116">An object implementing the [ICoreWebView2ExperimentalEnvironment]() interface will also implement [ICoreWebView2Environment](icorewebview2environment.md).</span></span>

## <span data-ttu-id="eb28c-117">Ses</span><span class="sxs-lookup"><span data-stu-id="eb28c-117">Members</span></span>

#### <span data-ttu-id="eb28c-118">CreateCoreWebView2CompositionController</span><span class="sxs-lookup"><span data-stu-id="eb28c-118">CreateCoreWebView2CompositionController</span></span> 

<span data-ttu-id="eb28c-119">Créer de manière asynchrone un nouveau WebView à utiliser avec l’hébergement visuel.</span><span class="sxs-lookup"><span data-stu-id="eb28c-119">Asynchronously create a new WebView for use with visual hosting.</span></span>

> <span data-ttu-id="eb28c-120">public HRESULT [CreateCoreWebView2CompositionController](#createcorewebview2compositioncontroller)(HWND ParentWindow, gestionnaire [ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler](icorewebview2experimentalcreatecorewebview2compositioncontrollercompletedhandler.md) \*)</span><span class="sxs-lookup"><span data-stu-id="eb28c-120">public HRESULT [CreateCoreWebView2CompositionController](#createcorewebview2compositioncontroller)(HWND parentWindow, [ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler](icorewebview2experimentalcreatecorewebview2compositioncontrollercompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="eb28c-121">FenêtreParent est le HWND dans lequel l’application relie l’arborescence d’éléments visuels du WebView.</span><span class="sxs-lookup"><span data-stu-id="eb28c-121">parentWindow is the HWND in which the app will connect the visual tree of the WebView.</span></span> <span data-ttu-id="eb28c-122">Il s’agira du HWND que l’application recevra les entrées de pointeur/souris destinées au WebView (et devront utiliser SendMouseInput/SendPointerInput pour transférer).</span><span class="sxs-lookup"><span data-stu-id="eb28c-122">This will be the HWND that the app will receive pointer/ mouse input meant for the WebView (and will need to use SendMouseInput/ SendPointerInput to forward).</span></span> <span data-ttu-id="eb28c-123">Si l’application déplace l’arborescence d’éléments visuels WebView vers une autre fenêtre, elle doit appeler put_ParentWindow pour mettre à jour le nouveau HWND parent de l’arborescence d’éléments visuels.</span><span class="sxs-lookup"><span data-stu-id="eb28c-123">If the app moves the WebView visual tree to underneath a different window, then it needs to call put_ParentWindow to update the new parent HWND of the visual tree.</span></span>

<span data-ttu-id="eb28c-124">Utilisez put_RootVisualTarget de la CoreWebView2CompositionController créée pour fournir un visuel permettant d’héberger l’arborescence visuelle du navigateur.</span><span class="sxs-lookup"><span data-stu-id="eb28c-124">Use put_RootVisualTarget on the created CoreWebView2CompositionController to provide a visual to host the browser's visual tree.</span></span>

<span data-ttu-id="eb28c-125">Il est recommandé que l’application définisse l’ID du modèle utilisateur de l’application pour le processus ou la fenêtre de l’application.</span><span class="sxs-lookup"><span data-stu-id="eb28c-125">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="eb28c-126">Si aucune n’est définie, lors de la création d’un WebView, un ID de modèle utilisateur de l’application généré est défini sur la fenêtre racine de parentWindow.</span><span class="sxs-lookup"><span data-stu-id="eb28c-126">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span> 
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
 <span data-ttu-id="eb28c-127">Il est recommandé que l’application gère les messages du gestionnaire de redémarrage afin qu’elle puisse être redémarrée harmonieusement dans le cas où l’application utilise Edge pour WebView à partir d’une certaine installation et que cette installation est désinstallée.</span><span class="sxs-lookup"><span data-stu-id="eb28c-127">It is recommended that the application handles restart manager messages so that it can be restarted gracefully in the case when the app is using Edge for webview from a certain installation and that installation is being uninstalled.</span></span> <span data-ttu-id="eb28c-128">Par exemple, si un utilisateur installe Edge à partir du canal de développement et décide d’utiliser Edge à partir de ce canal pour tester l’application, puis désinstalle le bord du canal sans fermer l’application, l’application est redémarrée pour permettre la réussite de la désinstallation du canal de développement.</span><span class="sxs-lookup"><span data-stu-id="eb28c-128">For example, if a user installs Edge from Dev channel and opts to use Edge from that channel for testing the app, and then uninstalls Edge from that channel without closing the app, the app will be restarted to allow uninstallation of the dev channel to succeed.</span></span> 
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

#### <span data-ttu-id="eb28c-129">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="eb28c-129">CreateCoreWebView2PointerInfo</span></span> 

<span data-ttu-id="eb28c-130">Créer un [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md)vide.</span><span class="sxs-lookup"><span data-stu-id="eb28c-130">Create an empty [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span></span>

> <span data-ttu-id="eb28c-131">public HRESULT [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)([ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* \* pointerInfo)</span><span class="sxs-lookup"><span data-stu-id="eb28c-131">public HRESULT [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)([ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \*\* pointerInfo)</span></span>

<span data-ttu-id="eb28c-132">La [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) renvoyée doit être remplie avec toutes les informations pertinentes avant d’appeler SendPointerInput.</span><span class="sxs-lookup"><span data-stu-id="eb28c-132">The returned [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) needs to be populated with all of the relevant info before calling SendPointerInput.</span></span>

#### <span data-ttu-id="eb28c-133">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="eb28c-133">GetProviderForHwnd</span></span> 

<span data-ttu-id="eb28c-134">Retourne le fournisseur UI Automation pour le ICoreWebView2CompositionController correspondant au HWND donné.</span><span class="sxs-lookup"><span data-stu-id="eb28c-134">Returns the UI Automation Provider for the ICoreWebView2CompositionController that corresponds with the given HWND.</span></span>

> <span data-ttu-id="eb28c-135">public HRESULT [GetProviderForHwnd](#getproviderforhwnd)(HWND hWnd, IUnknown \* \* Provider)</span><span class="sxs-lookup"><span data-stu-id="eb28c-135">public HRESULT [GetProviderForHwnd](#getproviderforhwnd)(HWND hwnd, IUnknown \*\* provider)</span></span>

