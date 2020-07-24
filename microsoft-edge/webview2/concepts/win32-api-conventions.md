---
description: Conventions d’API de WebView2 C++ Win32
title: Conventions d’API de WebView2 C++ Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: c8792133da2b858cfaa456df5a7dce26c3c65154
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895546"
---
# <span data-ttu-id="4fb01-104">Conventions d’API de WebView2 C++ Win32</span><span class="sxs-lookup"><span data-stu-id="4fb01-104">Win32 C++ WebView2 API conventions</span></span>  

## <span data-ttu-id="4fb01-105">Méthodes Async</span><span class="sxs-lookup"><span data-stu-id="4fb01-105">Async Methods</span></span>  

<span data-ttu-id="4fb01-106">Les méthodes asynchrones dans l’API C++ Win32 WebView2 utilisent une interface de délégué pour indiquer la fin de la méthode Async, le code de réussite ou d’échec, et pour some, le résultat de la méthode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="4fb01-106">Asynchronous methods in the WebView2 Win32 C++ API use a delegate interface to callback to you to indicate when the async method has completed, the success or failure code, and for some, the result of the asynchronous method.</span></span>  <span data-ttu-id="4fb01-107">Le paramètre final de toutes les méthodes asynchrones est un pointeur vers une interface de délégué qui vous permet de fournir une implémentation.</span><span class="sxs-lookup"><span data-stu-id="4fb01-107">The final parameter for all asynchronous methods is a pointer to a delegate interface of which you provide an implementation.</span></span>  

<span data-ttu-id="4fb01-108">L’interface du délégué dispose d’une `Invoke` méthode unique qui utilise comme premier paramètre un `HRESULT` Code de réussite ou d’échec.</span><span class="sxs-lookup"><span data-stu-id="4fb01-108">The delegate interface has a single `Invoke` method that takes as a first parameter an `HRESULT` of the success or failure code.</span></span>  <span data-ttu-id="4fb01-109">Par ailleurs, il peut exister un second paramètre qui est le résultat de la méthode si la méthode a un résultat.</span><span class="sxs-lookup"><span data-stu-id="4fb01-109">Additionally there may be a second parameter that is the result of the method if the method has a result.</span></span>  <span data-ttu-id="4fb01-110">Par exemple, la méthode [ICoreWebView2:: CapturePreview][Webview2ReferenceWin3209538Icorewebview2CapturePreview] utilise le paramètre final comme `ICoreWebView2CapturePreviewCompletedHandler` pointeur.</span><span class="sxs-lookup"><span data-stu-id="4fb01-110">For example, the [ICoreWebView2::CapturePreview][Webview2ReferenceWin3209538Icorewebview2CapturePreview] method takes as the final parameter an `ICoreWebView2CapturePreviewCompletedHandler` pointer.</span></span>  <span data-ttu-id="4fb01-111">Pour envoyer une `CapturePreview` demande de méthode, vous fournissez une instance du `ICoreWebView2CapturePreviewCompletedHandler` pointeur que vous implémentez.</span><span class="sxs-lookup"><span data-stu-id="4fb01-111">To send a `CapturePreview` method request, you provide an instance of the `ICoreWebView2CapturePreviewCompletedHandler` pointer that you implement.</span></span>  <span data-ttu-id="4fb01-112">L’extrait de code suivant utilise une méthode à implémenter.</span><span class="sxs-lookup"><span data-stu-id="4fb01-112">The following code snippet uses one method to implement.</span></span>  

```cpp
HRESULT Invoke(HRESULT result)
```  

<span data-ttu-id="4fb01-113">Vous implémentez la `Invoke` méthode et `CoreWebView2` sollicitez votre `Invoke` méthode lorsque la requête est `CapturePreview` terminée.</span><span class="sxs-lookup"><span data-stu-id="4fb01-113">You implement the `Invoke` method and `CoreWebView2` requests your `Invoke` method when `CapturePreview` request completes.</span></span>  <span data-ttu-id="4fb01-114">Le paramètre unique décrit le `HRESULT` Code de réussite ou d’échec de la `CapturePreview` requête.</span><span class="sxs-lookup"><span data-stu-id="4fb01-114">The single parameter is the `HRESULT` describing the success or failure code of the `CapturePreview` request.</span></span>  

<span data-ttu-id="4fb01-115">Ou `ICoreWebView2::ExecuteScript` bien, vous fournissez une instance de `ICoreWebView2ExecuteScriptCompletedHandler` `Invoke` la méthode qui vous permet d’utiliser le code de réussite ou d’échec de la `ExecuteScript` requête, ainsi que le deuxième paramètre `resultObjectAsJson` qui est le paramètre JSON du résultat de l’exécution du script.</span><span class="sxs-lookup"><span data-stu-id="4fb01-115">Or for `ICoreWebView2::ExecuteScript`, you provide an instance of `ICoreWebView2ExecuteScriptCompletedHandler` which has an `Invoke` method that provides you with the success or failure code of the `ExecuteScript` request as well as the second parameter `resultObjectAsJson` which is the JSON of the result of running the script.</span></span>  

<span data-ttu-id="4fb01-116">Vous pouvez implémenter manuellement les `CompleteHandler` interfaces de délégué ou vous pouvez utiliser la [fonction de rappel WRL][CppCxWrlCallbackFunction].</span><span class="sxs-lookup"><span data-stu-id="4fb01-116">You may manually implement the `CompleteHandler` delegate interfaces, or you may use the [WRL Callback function][CppCxWrlCallbackFunction].</span></span>  <span data-ttu-id="4fb01-117">La fonction callback est utilisée dans l’extrait de code WebView2 suivant.</span><span class="sxs-lookup"><span data-stu-id="4fb01-117">The Callback function is used throughout the following WebView2 code snippet.</span></span>  

```cpp
void ScriptComponent::InjectScript()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Inject Script",
        L"Enter script code:",
        L"Enter the JavaScript code to run in the webview.",
        L"window.getComputedStyle(document.body).backgroundColor");
    if (dialog.confirmed)
    {
        m_webView->ExecuteScript(dialog.input.c_str(),
            Callback<ICoreWebView2ExecuteScriptCompletedHandler>(
                [](HRESULT error, PCWSTR result) -> HRESULT
        {
            if (error != S_OK) {
                ShowFailure(error, L"ExecuteScript failed");
            }
            MessageBox(nullptr, result, L"ExecuteScript Result", MB_OK);
            return S_OK;
        }).Get());
    }
}
```  

## <span data-ttu-id="4fb01-118">Événements</span><span class="sxs-lookup"><span data-stu-id="4fb01-118">Events</span></span>  

<span data-ttu-id="4fb01-119">Les événements de l’API C++ Win32 WebView2 utilisent `add_EventName` la `remove_EventName` paire de méthodes et vous abonner et vous désabonner des événements.</span><span class="sxs-lookup"><span data-stu-id="4fb01-119">Events in the WebView2 Win32 C++ API use the `add_EventName` and `remove_EventName` method pair to subscribe and unsubscribe from events.</span></span>  <span data-ttu-id="4fb01-120">La `add_EventName` méthode prend une interface de délégué de gestionnaire d’événements et remet un `EventRegistrationToken` paramètre out en tant que paramètre out.</span><span class="sxs-lookup"><span data-stu-id="4fb01-120">The `add_EventName` method takes an event handler delegate interface and gives back an `EventRegistrationToken` as an out parameter.</span></span>  <span data-ttu-id="4fb01-121">La `remove_EventName` méthode accepte un `EventRegistrationToken` et annule l’abonnement à l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="4fb01-121">The `remove_EventName` method takes an `EventRegistrationToken` and unsubscribes the corresponding event subscription.</span></span>  

<span data-ttu-id="4fb01-122">Les interfaces de délégué de gestionnaire d’événements fonctionnent de manière très similaire aux interfaces de délégué de gestionnaires terminés de méthode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="4fb01-122">Event handler delegate interfaces work very similarly to the async method completed handler delegate interfaces.</span></span>  <span data-ttu-id="4fb01-123">Vous implémentez l’interface du délégué de gestionnaire d’événements et `CoreWebView2` envoyez un rappel chaque fois que l’événement se déclenche.</span><span class="sxs-lookup"><span data-stu-id="4fb01-123">You implement the event handler delegate interface and `CoreWebView2` sends a callback whenever the event fires.</span></span>  <span data-ttu-id="4fb01-124">Chaque interface de délégué de gestionnaire d’événements possède une `Invoke` méthode unique qui a un paramètre sender suivi d’un paramètre d’arguments d’événement.</span><span class="sxs-lookup"><span data-stu-id="4fb01-124">Every event handler delegate interface has a single `Invoke` method that has a sender parameter followed by an event args parameter.</span></span>  <span data-ttu-id="4fb01-125">L’expéditeur est l’instance de l’objet sur lequel vous avez souscrit un abonnement à des événements.</span><span class="sxs-lookup"><span data-stu-id="4fb01-125">The sender is the instance of the object on which you subscribed for events.</span></span>  <span data-ttu-id="4fb01-126">Le paramètre args est une interface qui contient des informations sur l’événement actuellement en cours de déclenchement.</span><span class="sxs-lookup"><span data-stu-id="4fb01-126">The event args parameter is an interface that contains information about the currently firing event.</span></span>  

<span data-ttu-id="4fb01-127">Par exemple `NavigationCompleted` , l’événement sur `ICoreWebView2` a `ICoreWebView2::add_NavigationCompleted` la `ICoreWebView2::remove_NavigationCompleted` paire de méthodes et.</span><span class="sxs-lookup"><span data-stu-id="4fb01-127">For instance the `NavigationCompleted` event on `ICoreWebView2` has the `ICoreWebView2::add_NavigationCompleted` and `ICoreWebView2::remove_NavigationCompleted` method pair.</span></span>  <span data-ttu-id="4fb01-128">Lorsque vous demandez l’ajout, vous fournissez une instance de `ICoreWebView2NavigationCompletedEventHandler` la méthode que vous avez implémentée précédemment `Invoke` .</span><span class="sxs-lookup"><span data-stu-id="4fb01-128">When you request add you provide an instance of `ICoreWebView2NavigationCompletedEventHandler` in which you previously implemented `Invoke` method.</span></span>  <span data-ttu-id="4fb01-129">Lorsque l' `NavigationCompleted` événement est déclenché, votre `Invoke` méthode est sollicitée.</span><span class="sxs-lookup"><span data-stu-id="4fb01-129">When the `NavigationCompleted` event fires, your `Invoke` method is requested.</span></span>  <span data-ttu-id="4fb01-130">Le premier paramètre est le `ICoreWebView2` qui déclenche l' `NavigationCompleted` événement.</span><span class="sxs-lookup"><span data-stu-id="4fb01-130">The first parameter is the `ICoreWebView2` which is firing the `NavigationCompleted` event.</span></span>  <span data-ttu-id="4fb01-131">Le deuxième paramètre est le `ICoreWebView2NavigationCompletedEventArgs` qui contient des informations sur la réussite de la navigation et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="4fb01-131">The second parameter is the `ICoreWebView2NavigationCompletedEventArgs` which contains information about if the navigation completed successfully and so on.</span></span>  

<span data-ttu-id="4fb01-132">À l’instar de la méthode asynchrone, vous pouvez implémenter vous-même directement, ou vous pouvez utiliser la fonction de rappel WRL utilisée dans l’extrait de code WebView2 suivant.</span><span class="sxs-lookup"><span data-stu-id="4fb01-132">Similarly to the async method completed handler delegate interface you are able to implement it yourself directly, or you may use the WRL Callback function that is used in the following WebView2 code snippet.</span></span>  

```cpp
// Register a handler for the NavigationCompleted event.
// Check whether the navigation succeeded, and if not, do something.
// Also update the Cancel buttons.
CHECK_FAILURE(m_webView->add_NavigationCompleted(
    Callback<ICoreWebView2NavigationCompletedEventHandler>(
        [this](ICoreWebView2* sender, ICoreWebView2NavigationCompletedEventArgs* args)
            -> HRESULT {
            BOOL success;
            CHECK_FAILURE(args->get_IsSuccess(&success));
            if (!success)
            {
                COREWEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                if (webErrorStatus == COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                {
                    // Do something here if you want to handle a specific error case.
                    // In most cases it is not necessary, because the WebView
                    // displays an error page automatically.
                }
            }
            m_toolbar->SetItemEnabled(Toolbar::Item_CancelButton, false);
            m_toolbar->SetItemEnabled(Toolbar::Item_ReloadButton, true);
            return S_OK;
        })
        .Get(),
    &m_navigationCompletedToken));
```  

## <span data-ttu-id="4fb01-133">String</span><span class="sxs-lookup"><span data-stu-id="4fb01-133">Strings</span></span>  

<span data-ttu-id="4fb01-134">Les paramètres de type chaîne se `LPWSTR` terminent par un caractère nul.</span><span class="sxs-lookup"><span data-stu-id="4fb01-134">String out parameters are `LPWSTR` null-terminated strings.</span></span>  <span data-ttu-id="4fb01-135">Le demandeur alloue la chaîne à l’aide de `CoTaskMemAlloc` .</span><span class="sxs-lookup"><span data-stu-id="4fb01-135">The requester allocates the string using `CoTaskMemAlloc`.</span></span>  <span data-ttu-id="4fb01-136">La propriété est transférée à la demande et il appartient au demandeur de libérer de la mémoire en utilisant `CoTaskMemFree` .</span><span class="sxs-lookup"><span data-stu-id="4fb01-136">Ownership is transferred to the requester and it is up to the requester to free the memory using `CoTaskMemFree`.</span></span>  

<span data-ttu-id="4fb01-137">Les valeurs de chaîne dans les paramètres sont des `LPCWSTR` chaînes dont le caractère nul est terminé.</span><span class="sxs-lookup"><span data-stu-id="4fb01-137">String in parameters are `LPCWSTR` null-terminated strings.</span></span>  <span data-ttu-id="4fb01-138">Le demandeur vérifie que la chaîne est valide pour la durée de la demande de fonction synchrone.</span><span class="sxs-lookup"><span data-stu-id="4fb01-138">The requester ensures the string is valid for the duration of the synchronous function request.</span></span>  <span data-ttu-id="4fb01-139">Si le destinataire doit conserver cette valeur à un certain point après la demande de la fonction, le destinataire doit allouer une copie associée de la valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="4fb01-139">If the receiver must retain that value to some point after the function request completes, the receiver must allocate an associated copy of the string value.</span></span>  

## <span data-ttu-id="4fb01-140">D’analyse des URI et de JSON</span><span class="sxs-lookup"><span data-stu-id="4fb01-140">URI and JSON parsing</span></span>  

<span data-ttu-id="4fb01-141">Diverses méthodes fournissent ou acceptent des URI et JSON en tant que chaînes.</span><span class="sxs-lookup"><span data-stu-id="4fb01-141">Various methods provide or accept URIs and JSON as strings.</span></span>  <span data-ttu-id="4fb01-142">Utilisez votre propre bibliothèque préférée pour analyser et générer les chaînes.</span><span class="sxs-lookup"><span data-stu-id="4fb01-142">Please use your own preferred library for parsing and generating the strings.</span></span>  

<span data-ttu-id="4fb01-143">Si WinRT est disponible pour votre application, vous pouvez utiliser les `RuntimeClass_Windows_Data_Json_JsonObject` `IJsonObjectStatics` méthodes et pour analyser ou générer des chaînes JSON ou `RuntimeClass_Windows_Foundation_Uri` des `IUriRuntimeClassFactory` méthodes pour analyser et générer des URI.</span><span class="sxs-lookup"><span data-stu-id="4fb01-143">If WinRT is available for your app, you may use the `RuntimeClass_Windows_Data_Json_JsonObject` and `IJsonObjectStatics` methods to parse or produce JSON strings or `RuntimeClass_Windows_Foundation_Uri` and `IUriRuntimeClassFactory` methods to parse and produce URIs.</span></span>  <span data-ttu-id="4fb01-144">Les deux méthodes fonctionnent dans les applications Win32.</span><span class="sxs-lookup"><span data-stu-id="4fb01-144">Both of methods work in Win32 apps.</span></span>  

<span data-ttu-id="4fb01-145">Si vous utilisez `IUri` et que vous `CreateUri` souhaitez analyser les URI, vous pouvez utiliser les indicateurs de création d’URI suivants pour que le `CreateUri` comportement corresponde plus étroitement à l’analyse de l’URI dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="4fb01-145">If you use `IUri` and `CreateUri` to parse URIs, you may want to use the following URI creation flags to have `CreateUri` behavior more closely match the URI parsing in the WebView.</span></span>  

```json
Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO
```  

<!-- links -->  

[Webview2ReferenceWin3209538Icorewebview2CapturePreview]: ../reference/win32/0-9-538/icorewebview2.md#capturepreview "CapturePreview-interface ICoreWebView2 | Documents Microsoft"  

[CppCxWrlCallbackFunction]: /cpp/cppcx/wrl/callback-function-wrl "Fonction de rappel (WRL) | Documents Microsoft"  
