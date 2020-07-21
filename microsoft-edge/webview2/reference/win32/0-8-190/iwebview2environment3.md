---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2Environment3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 327a182c5298ed6de6b9e55b407d138857dbe659
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886093"
---
# <span data-ttu-id="8356b-104">0.8.355-interface IWebView2Environment3</span><span class="sxs-lookup"><span data-stu-id="8356b-104">0.8.355 - interface IWebView2Environment3</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Environment3
  : public IWebView2Environment2
```

<span data-ttu-id="8356b-105">Fonctionnalités supplémentaires implémentées par l’objet Environment.</span><span class="sxs-lookup"><span data-stu-id="8356b-105">Additional functionality implemented by the Environment object.</span></span>

## <span data-ttu-id="8356b-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="8356b-106">Summary</span></span>

 <span data-ttu-id="8356b-107">Ses</span><span class="sxs-lookup"><span data-stu-id="8356b-107">Members</span></span>                        | <span data-ttu-id="8356b-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="8356b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8356b-109">add_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="8356b-109">add_NewVersionAvailable</span></span>](#add_newversionavailable) | <span data-ttu-id="8356b-110">L’événement NewVersionAvailable se déclenche lors de l’installation d’une nouvelle version du navigateur Edge et peut être utilisée via WebView2.</span><span class="sxs-lookup"><span data-stu-id="8356b-110">The NewVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="8356b-111">remove_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="8356b-111">remove_NewVersionAvailable</span></span>](#remove_newversionavailable) | <span data-ttu-id="8356b-112">Supprimez un gestionnaire d’événements préalablement ajouté à add_NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="8356b-112">Remove an event handler previously added with add_NewVersionAvailable.</span></span>

<span data-ttu-id="8356b-113">Pour plus d’informations, consultez l’interface [IWebView2Environment](IWebView2Environment.md) .</span><span class="sxs-lookup"><span data-stu-id="8356b-113">See the [IWebView2Environment](IWebView2Environment.md) interface for more details.</span></span> <span data-ttu-id="8356b-114">Vous pouvez QueryInterface pour cette interface à partir de l’objet qui implémente [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="8356b-114">You can QueryInterface for this interface from the object that implements [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="8356b-115">Ses</span><span class="sxs-lookup"><span data-stu-id="8356b-115">Members</span></span>

#### <span data-ttu-id="8356b-116">add_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="8356b-116">add_NewVersionAvailable</span></span> 

<span data-ttu-id="8356b-117">L’événement NewVersionAvailable se déclenche lors de l’installation d’une nouvelle version du navigateur Edge et peut être utilisée via WebView2.</span><span class="sxs-lookup"><span data-stu-id="8356b-117">The NewVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="8356b-118">[add_NewVersionAvailable](#add_newversionavailable)par le biais du[mot de passe](IWebView2NewVersionAvailableEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="8356b-118">public HRESULT [add_NewVersionAvailable](#add_newversionavailable)([IWebView2NewVersionAvailableEventHandler](IWebView2NewVersionAvailableEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="8356b-119">Pour utiliser la version la plus récente du navigateur, vous devez créer un nouveau [IWebView2Environment](IWebView2Environment.md) et [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="8356b-119">To use the newer version of the browser you must create a new [IWebView2Environment](IWebView2Environment.md) and [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="8356b-120">L’événement est déclenché uniquement pour la nouvelle version à partir du canal de périphérie d’exécution du code.</span><span class="sxs-lookup"><span data-stu-id="8356b-120">Event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="8356b-121">S’il n’est pas exécuté avec des bords installés, aucun événement n’est déclenché.</span><span class="sxs-lookup"><span data-stu-id="8356b-121">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="8356b-122">Dans la mesure où un dossier de données utilisateur ne peut être utilisé que par un seul processus de navigateur à la fois, si vous souhaitez utiliser le même dossier de données utilisateur dans les webaffichages à l’aide de la nouvelle version du navigateur, vous devez d’abord fermer le [IWebView2Environment](IWebView2Environment.md) et IWebView2WebViews qui utilisent l’ancienne version du navigateur.</span><span class="sxs-lookup"><span data-stu-id="8356b-122">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the [IWebView2Environment](IWebView2Environment.md) and IWebView2WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="8356b-123">Vous pouvez également demander à l’utilisateur de redémarrer l’application.</span><span class="sxs-lookup"><span data-stu-id="8356b-123">Or simply prompt the user to restart the app.</span></span>

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

#### <span data-ttu-id="8356b-124">remove_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="8356b-124">remove_NewVersionAvailable</span></span> 

<span data-ttu-id="8356b-125">Supprimez un gestionnaire d’événements préalablement ajouté à add_NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="8356b-125">Remove an event handler previously added with add_NewVersionAvailable.</span></span>

> <span data-ttu-id="8356b-126">[remove_NewVersionAvailable](#remove_newversionavailable)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="8356b-126">public HRESULT [remove_NewVersionAvailable](#remove_newversionavailable)(EventRegistrationToken token)</span></span>

