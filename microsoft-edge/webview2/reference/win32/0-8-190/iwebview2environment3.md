---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2Environment3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: d16a12aae823c48b7dd4b0b5e8225cdd40c1dafc
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878525"
---
# <span data-ttu-id="89d1d-104">0.8.355-interface IWebView2Environment3</span><span class="sxs-lookup"><span data-stu-id="89d1d-104">0.8.355 - interface IWebView2Environment3</span></span> 

> [!NOTE]
> <span data-ttu-id="89d1d-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="89d1d-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="89d1d-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="89d1d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Environment3
  : public IWebView2Environment2
```

<span data-ttu-id="89d1d-107">Fonctionnalités supplémentaires implémentées par l’objet Environment.</span><span class="sxs-lookup"><span data-stu-id="89d1d-107">Additional functionality implemented by the Environment object.</span></span>

## <span data-ttu-id="89d1d-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="89d1d-108">Summary</span></span>

 <span data-ttu-id="89d1d-109">Ses</span><span class="sxs-lookup"><span data-stu-id="89d1d-109">Members</span></span>                        | <span data-ttu-id="89d1d-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="89d1d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="89d1d-111">add_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="89d1d-111">add_NewVersionAvailable</span></span>](#add_newversionavailable) | <span data-ttu-id="89d1d-112">L’événement NewVersionAvailable se déclenche lors de l’installation d’une nouvelle version du navigateur Edge et peut être utilisée via WebView2.</span><span class="sxs-lookup"><span data-stu-id="89d1d-112">The NewVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="89d1d-113">remove_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="89d1d-113">remove_NewVersionAvailable</span></span>](#remove_newversionavailable) | <span data-ttu-id="89d1d-114">Supprimez un gestionnaire d’événements préalablement ajouté à add_NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="89d1d-114">Remove an event handler previously added with add_NewVersionAvailable.</span></span>

<span data-ttu-id="89d1d-115">Pour plus d’informations, consultez l’interface [IWebView2Environment](IWebView2Environment.md) .</span><span class="sxs-lookup"><span data-stu-id="89d1d-115">See the [IWebView2Environment](IWebView2Environment.md) interface for more details.</span></span> <span data-ttu-id="89d1d-116">Vous pouvez QueryInterface pour cette interface à partir de l’objet qui implémente [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="89d1d-116">You can QueryInterface for this interface from the object that implements [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="89d1d-117">Ses</span><span class="sxs-lookup"><span data-stu-id="89d1d-117">Members</span></span>

#### <span data-ttu-id="89d1d-118">add_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="89d1d-118">add_NewVersionAvailable</span></span> 

<span data-ttu-id="89d1d-119">L’événement NewVersionAvailable se déclenche lors de l’installation d’une nouvelle version du navigateur Edge et peut être utilisée via WebView2.</span><span class="sxs-lookup"><span data-stu-id="89d1d-119">The NewVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="89d1d-120">[add_NewVersionAvailable](#add_newversionavailable)par le biais du[mot de passe](IWebView2NewVersionAvailableEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="89d1d-120">public HRESULT [add_NewVersionAvailable](#add_newversionavailable)([IWebView2NewVersionAvailableEventHandler](IWebView2NewVersionAvailableEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="89d1d-121">Pour utiliser la version la plus récente du navigateur, vous devez créer un nouveau [IWebView2Environment](IWebView2Environment.md) et [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="89d1d-121">To use the newer version of the browser you must create a new [IWebView2Environment](IWebView2Environment.md) and [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="89d1d-122">L’événement est déclenché uniquement pour la nouvelle version à partir du canal de périphérie d’exécution du code.</span><span class="sxs-lookup"><span data-stu-id="89d1d-122">Event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="89d1d-123">S’il n’est pas exécuté avec des bords installés, aucun événement n’est déclenché.</span><span class="sxs-lookup"><span data-stu-id="89d1d-123">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="89d1d-124">Dans la mesure où un dossier de données utilisateur ne peut être utilisé que par un seul processus de navigateur à la fois, si vous souhaitez utiliser le même dossier de données utilisateur dans les webaffichages à l’aide de la nouvelle version du navigateur, vous devez d’abord fermer le [IWebView2Environment](IWebView2Environment.md) et IWebView2WebViews qui utilisent l’ancienne version du navigateur.</span><span class="sxs-lookup"><span data-stu-id="89d1d-124">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the [IWebView2Environment](IWebView2Environment.md) and IWebView2WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="89d1d-125">Vous pouvez également demander à l’utilisateur de redémarrer l’application.</span><span class="sxs-lookup"><span data-stu-id="89d1d-125">Or simply prompt the user to restart the app.</span></span>

```cpp
    // After the environment is successfully created,
    // register a handler for the NewVersionAvailable event.
    // This handler tells when there is a new Edge version available on the machine.
    CHECK_FAILURE(m_webViewEnvironment->add_NewVersionAvailable(
        Callback<IWebView2NewVersionAvailableEventHandler>(
            [this](IWebView2Environment* sender, IWebView2NewVersionAvailableEventArgs* args)
                -> HRESULT {
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

#### <span data-ttu-id="89d1d-126">remove_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="89d1d-126">remove_NewVersionAvailable</span></span> 

<span data-ttu-id="89d1d-127">Supprimez un gestionnaire d’événements préalablement ajouté à add_NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="89d1d-127">Remove an event handler previously added with add_NewVersionAvailable.</span></span>

> <span data-ttu-id="89d1d-128">[remove_NewVersionAvailable](#remove_newversionavailable)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="89d1d-128">public HRESULT [remove_NewVersionAvailable](#remove_newversionavailable)(EventRegistrationToken token)</span></span>

