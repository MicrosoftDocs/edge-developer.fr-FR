---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: c3ce6a49be1abf12d66f69da6d2ff6ff9d9f5b68
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653689"
---
# <span data-ttu-id="e511a-104">interface IWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="e511a-104">interface IWebView2Environment</span></span> 

> [!NOTE]
> <span data-ttu-id="e511a-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="e511a-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="e511a-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="e511a-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Environment
  : public IUnknown
```

<span data-ttu-id="e511a-107">Il s’agit de l’environnement WebView2.</span><span class="sxs-lookup"><span data-stu-id="e511a-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="e511a-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="e511a-108">Summary</span></span>

 <span data-ttu-id="e511a-109">Ses</span><span class="sxs-lookup"><span data-stu-id="e511a-109">Members</span></span>                        | <span data-ttu-id="e511a-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="e511a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e511a-111">CreateWebView</span><span class="sxs-lookup"><span data-stu-id="e511a-111">CreateWebView</span></span>](#createwebview) | <span data-ttu-id="e511a-112">Créez de manière asynchrone une nouvelle [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="e511a-112">Asynchronously create a new [IWebView2WebView](IWebView2WebView.md).</span></span>
[<span data-ttu-id="e511a-113">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="e511a-113">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="e511a-114">Créer un objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="e511a-114">Create a new web resource response object.</span></span>

<span data-ttu-id="e511a-115">Les webvues créées à partir d’un environnement s’exécutent sur le processus de navigateur spécifié avec des paramètres d’environnement et des objets créés à partir d’un environnement doivent être utilisés dans le même environnement.</span><span class="sxs-lookup"><span data-stu-id="e511a-115">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="e511a-116">Il n’est pas garanti que l’utilisation de ce dernier dans d’autres environnements est compatible et risque d’échouer.</span><span class="sxs-lookup"><span data-stu-id="e511a-116">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="e511a-117">Ses</span><span class="sxs-lookup"><span data-stu-id="e511a-117">Members</span></span>

#### <span data-ttu-id="e511a-118">CreateWebView</span><span class="sxs-lookup"><span data-stu-id="e511a-118">CreateWebView</span></span> 

<span data-ttu-id="e511a-119">Créez de manière asynchrone une nouvelle [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="e511a-119">Asynchronously create a new [IWebView2WebView](IWebView2WebView.md).</span></span>

> <span data-ttu-id="e511a-120">public HRESULT [CreateWebView](#createwebview)(HWND ParentWindow, gestionnaire[IWebView2CreateWebViewCompletedHandler](IWebView2CreateWebViewCompletedHandler.md) \*)</span><span class="sxs-lookup"><span data-stu-id="e511a-120">public HRESULT [CreateWebView](#createwebview)(HWND parentWindow,[IWebView2CreateWebViewCompletedHandler](IWebView2CreateWebViewCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="e511a-121">FenêtreParent est le HWND dans lequel le WebView doit être affiché et à partir duquel il est reçu une entrée.</span><span class="sxs-lookup"><span data-stu-id="e511a-121">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="e511a-122">Le WebView ajoutera une fenêtre enfant à la fenêtre fournie lors de la création WebView.</span><span class="sxs-lookup"><span data-stu-id="e511a-122">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="e511a-123">Ordre de plan et autres éléments concernés par l’ordre des fenêtres frères en conséquence.</span><span class="sxs-lookup"><span data-stu-id="e511a-123">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="e511a-124">Il est recommandé que l’application définisse l’ID du modèle utilisateur de l’application pour le processus ou la fenêtre de l’application.</span><span class="sxs-lookup"><span data-stu-id="e511a-124">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="e511a-125">Si aucune n’est définie, lors de la création d’un WebView, un ID de modèle utilisateur de l’application généré est défini sur la fenêtre racine de parentWindow.</span><span class="sxs-lookup"><span data-stu-id="e511a-125">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span> 

```cpp
// Create or recreate the WebView and its environment.
void AppWindow::InitializeWebView(InitializeWebViewFlags webviewInitFlags)
{
    m_lastUsedInitFlags = webviewInitFlags;
    // To ensure browser switches get applied correctly, we need to close
    // the existing WebView. This will result in a new browser process
    // getting created which will apply the browser switches.
    CloseWebView();

    LPCWSTR subFolder = nullptr;
    LPCWSTR additionalBrowserSwitches = nullptr;
    HRESULT hr = CreateWebView2EnvironmentWithDetails(
        subFolder, nullptr, additionalBrowserSwitches,
        Callback<IWebView2CreateWebView2EnvironmentCompletedHandler>(
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
    HRESULT result, IWebView2Environment* environment)
{
    CHECK_FAILURE(result);

    CHECK_FAILURE(environment->QueryInterface(IID_PPV_ARGS(&m_webViewEnvironment)));
        CHECK_FAILURE(m_webViewEnvironment->CreateWebView(
            m_mainWindow, Callback<IWebView2CreateWebViewCompletedHandler>(
                              this, &AppWindow::OnCreateWebViewCompleted)
                              .Get()));
    return S_OK;
}
```

 <span data-ttu-id="e511a-126">Il est recommandé que l’application gère les messages du gestionnaire de redémarrage afin qu’elle puisse être redémarrée harmonieusement dans le cas où l’application utilise Edge pour WebView à partir d’une certaine installation et que cette installation est désinstallée.</span><span class="sxs-lookup"><span data-stu-id="e511a-126">It is recommended that the application handles restart manager messages so that it can be restarted gracefully in the case when the app is using Edge for webview from a certain installation and that installation is being uninstalled.</span></span> <span data-ttu-id="e511a-127">Par exemple, si un utilisateur installe Edge à partir du canal de développement et décide d’utiliser Edge à partir de ce canal pour tester l’application, puis désinstalle le bord du canal sans fermer l’application, l’application est redémarrée pour permettre la réussite de la désinstallation du canal de développement.</span><span class="sxs-lookup"><span data-stu-id="e511a-127">For example, if a user installs Edge from Dev channel and opts to use Edge from that channel for testing the app, and then uninstalls Edge from that channel without closing the app, the app will be restarted to allow uninstallation of the dev channel to succeed.</span></span> 

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

#### <span data-ttu-id="e511a-128">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="e511a-128">CreateWebResourceResponse</span></span> 

<span data-ttu-id="e511a-129">Créer un objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="e511a-129">Create a new web resource response object.</span></span>

> <span data-ttu-id="e511a-130">public HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(IStream \* content, int STATUSCODE, LPCWSTR reasonPhrase, en-têtes LPCWSTR,[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="e511a-130">public HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(IStream \* content,int statusCode,LPCWSTR reasonPhrase,LPCWSTR headers,[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*\* response)</span></span>

<span data-ttu-id="e511a-131">Les en-têtes sont les chaînes d’en-tête de réponse brutes délimitées par NewLine.</span><span class="sxs-lookup"><span data-stu-id="e511a-131">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="e511a-132">Il est également possible de créer cet objet avec une chaîne d’en-têtes vide, puis d’utiliser le [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) pour créer des en-têtes à l’aide de la fonction ligne.</span><span class="sxs-lookup"><span data-stu-id="e511a-132">It's also possible to create this object with empty headers string and then use the [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) to construct the headers line by line.</span></span> <span data-ttu-id="e511a-133">Pour plus d’informations sur les autres paramètres, voir [IWebView2WebResourceResponse](IWebView2WebResourceResponse.md).</span><span class="sxs-lookup"><span data-stu-id="e511a-133">For information on other parameters see [IWebView2WebResourceResponse](IWebView2WebResourceResponse.md).</span></span>

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<IWebView2WebResourceRequestedEventHandler>(
                    [this](
                        IWebView2WebView* sender,
                        IWebView2WebResourceRequestedEventArgs* args) {
                        wil::com_ptr<IWebView2WebResourceRequestedEventArgs2>
                            webResourceEventArgs2;
                        args->QueryInterface(IID_PPV_ARGS(&webResourceEventArgs2));
                        WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            webResourceEventArgs2->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<IWebView2WebResourceResponse> response;
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

