---
description: Conventions de l’API Win32 C++ WebView2
title: Conventions de l’API Win32 C++ WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: b47e53a4846d4bb662ae108c6445a6c2a615722a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11470857"
---
# <a name="win32-c-webview2-api-conventions"></a><span data-ttu-id="c41b6-104">Conventions de l’API Win32 C++ WebView2</span><span class="sxs-lookup"><span data-stu-id="c41b6-104">Win32 C++ WebView2 API conventions</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="c41b6-105">Plateformes pris en charge :</span><span class="sxs-lookup"><span data-stu-id="c41b6-105">Supported platforms:</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c41b6-106">Win32</span><span class="sxs-lookup"><span data-stu-id="c41b6-106">Win32</span></span>
   :::column-end:::
:::row-end:::  

## <a name="prerequisites"></a><span data-ttu-id="c41b6-107">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="c41b6-107">Prerequisites</span></span>  

*   <span data-ttu-id="c41b6-108">Expérience d’utilisation de l’API Win32</span><span class="sxs-lookup"><span data-stu-id="c41b6-108">Experience using Win32 API</span></span>  

## <a name="async-methods"></a><span data-ttu-id="c41b6-109">Méthodes async</span><span class="sxs-lookup"><span data-stu-id="c41b6-109">Async methods</span></span>  

<span data-ttu-id="c41b6-110">Les méthodes asynchrones dans l’API WebView2 Win32 C++ utilisent une interface déléguée pour vous contacter pour les raisons suivantes.</span><span class="sxs-lookup"><span data-stu-id="c41b6-110">Asynchronous methods in the WebView2 Win32 C++ API use a delegate interface to contact you for the following reasons.</span></span>  

*   <span data-ttu-id="c41b6-111">La méthode async est terminée.</span><span class="sxs-lookup"><span data-stu-id="c41b6-111">The async method has completed.</span></span>  
*   <span data-ttu-id="c41b6-112">Code de réussite ou d’échec.</span><span class="sxs-lookup"><span data-stu-id="c41b6-112">The success or failure code.</span></span>  
*   <span data-ttu-id="c41b6-113">Résultat de la méthode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="c41b6-113">The result of the asynchronous method.</span></span>  

<span data-ttu-id="c41b6-114">Le dernier paramètre de toutes les méthodes asynchrones est un pointeur vers une interface déléguée dont vous fournissez une implémentation.</span><span class="sxs-lookup"><span data-stu-id="c41b6-114">The final parameter for all asynchronous methods is a pointer to a delegate interface of which you provide an implementation.</span></span>  

<span data-ttu-id="c41b6-115">L’interface déléguée possède une méthode unique qui prend comme premier paramètre un code de réussite `Invoke` `HRESULT` ou d’échec.</span><span class="sxs-lookup"><span data-stu-id="c41b6-115">The delegate interface has a single `Invoke` method that takes as a first parameter an `HRESULT` of the success or failure code.</span></span>  <span data-ttu-id="c41b6-116">En outre, il peut y avoir un deuxième paramètre qui est le résultat de la méthode si la méthode a un résultat.</span><span class="sxs-lookup"><span data-stu-id="c41b6-116">Additionally, there may be a second parameter that is the result of the method if the method has a result.</span></span>  <span data-ttu-id="c41b6-117">Par exemple, la [méthode ICoreWebView2::CapturePreview][Webview2ReferenceWin32Icorewebview2CapturePreview] prend comme paramètre final un `ICoreWebView2CapturePreviewCompletedHandler` pointeur.</span><span class="sxs-lookup"><span data-stu-id="c41b6-117">For example, the [ICoreWebView2::CapturePreview][Webview2ReferenceWin32Icorewebview2CapturePreview] method takes as the final parameter an `ICoreWebView2CapturePreviewCompletedHandler` pointer.</span></span>  <span data-ttu-id="c41b6-118">Pour envoyer une `CapturePreview` demande de méthode, vous fournissez une instance du `ICoreWebView2CapturePreviewCompletedHandler` pointeur que vous implémentez.</span><span class="sxs-lookup"><span data-stu-id="c41b6-118">To send a `CapturePreview` method request, you provide an instance of the `ICoreWebView2CapturePreviewCompletedHandler` pointer that you implement.</span></span>  <span data-ttu-id="c41b6-119">L’extrait de code suivant utilise une méthode pour implémenter.</span><span class="sxs-lookup"><span data-stu-id="c41b6-119">The following code snippet uses one method to implement.</span></span>  

```cpp
HRESULT Invoke(HRESULT result)
```  

<span data-ttu-id="c41b6-120">Vous implémentez `Invoke` la méthode et demandez votre méthode lorsque la demande est `CoreWebView2` `Invoke` `CapturePreview` terminée.</span><span class="sxs-lookup"><span data-stu-id="c41b6-120">You implement the `Invoke` method and `CoreWebView2` requests your `Invoke` method when `CapturePreview` request completes.</span></span>  <span data-ttu-id="c41b6-121">Le paramètre unique est le code de réussite ou `HRESULT` d’échec de la `CapturePreview` demande.</span><span class="sxs-lookup"><span data-stu-id="c41b6-121">The single parameter is the `HRESULT` describing the success or failure code of the `CapturePreview` request.</span></span>  

<span data-ttu-id="c41b6-122">Vous pouvez également fournir une instance qui dispose d’une méthode qui vous fournit le code de réussite ou `ICoreWebView2::ExecuteScript` `Invoke` d’échec de la `ExecuteScript` demande.</span><span class="sxs-lookup"><span data-stu-id="c41b6-122">Alternately, for `ICoreWebView2::ExecuteScript`, you provide an instance that has an `Invoke` method that provides you with the success or failure code of the `ExecuteScript` request.</span></span>  <span data-ttu-id="c41b6-123">Fournissez également le deuxième paramètre qui est le JSON du résultat de l’exécution du script.</span><span class="sxs-lookup"><span data-stu-id="c41b6-123">Also provide the second parameter that is the JSON of the result of running the script.</span></span>  

<span data-ttu-id="c41b6-124">Vous pouvez implémenter manuellement les interfaces déléguées, ou vous pouvez utiliser la fonction de rappel `CompleteHandler` [(WRL).][CppCxWrlCallbackFunction]</span><span class="sxs-lookup"><span data-stu-id="c41b6-124">You may manually implement the `CompleteHandler` delegate interfaces, or you may use the [Callback function (WRL)][CppCxWrlCallbackFunction].</span></span>  <span data-ttu-id="c41b6-125">La [fonction de rappel (WRL)][CppCxWrlCallbackFunction] est utilisée dans l’extrait de code WebView2 suivant.</span><span class="sxs-lookup"><span data-stu-id="c41b6-125">The [Callback function (WRL)][CppCxWrlCallbackFunction] is used throughout the following WebView2 code snippet.</span></span>  

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

## <a name="events"></a><span data-ttu-id="c41b6-126">Événements</span><span class="sxs-lookup"><span data-stu-id="c41b6-126">Events</span></span>  

<span data-ttu-id="c41b6-127">Les événements dans l’API C++ Win32 WebView2 utilisent la paire méthode et abonnement pour s’abonner à des événements et `add_EventName` `remove_EventName` s’en désabonner.</span><span class="sxs-lookup"><span data-stu-id="c41b6-127">Events in the WebView2 Win32 C++ API use the `add_EventName` and `remove_EventName` method pair to subscribe and unsubscribe from events.</span></span>  <span data-ttu-id="c41b6-128">La `add_EventName` méthode prend une interface déléguée de handler d’événements et retourne un `EventRegistrationToken` jeton en tant que paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="c41b6-128">The `add_EventName` method takes an event handler delegate interface and gives back an `EventRegistrationToken` token as an output parameter.</span></span>  <span data-ttu-id="c41b6-129">La `remove_EventName` méthode prend un `EventRegistrationToken` jeton et désabonner l’abonnement à l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="c41b6-129">The `remove_EventName` method takes an `EventRegistrationToken` token and unsubscribes the corresponding event subscription.</span></span>  

<span data-ttu-id="c41b6-130">Les interfaces déléguées du handler d’événements fonctionnent de la même manière que les interfaces déléguées de la méthode async terminées.</span><span class="sxs-lookup"><span data-stu-id="c41b6-130">Event handler delegate interfaces work similarly to the async method completed handler delegate interfaces.</span></span>  <span data-ttu-id="c41b6-131">Vous implémentez l’interface déléguée du handler d’événements et envoyez un rappel chaque `CoreWebView2` fois que l’événement s’exécute.</span><span class="sxs-lookup"><span data-stu-id="c41b6-131">You implement the event handler delegate interface and `CoreWebView2` sends a callback whenever the event runs.</span></span>  <span data-ttu-id="c41b6-132">Chaque interface déléguée du handler d’événements possède une seule méthode qui possède un paramètre `Invoke` d’expéditeur suivi d’un paramètre d’rgs d’événement.</span><span class="sxs-lookup"><span data-stu-id="c41b6-132">Every event handler delegate interface has a single `Invoke` method that has a sender parameter followed by an event args parameter.</span></span>  <span data-ttu-id="c41b6-133">L’expéditeur est l’instance de l’objet auquel vous vous êtes abonné pour les événements.</span><span class="sxs-lookup"><span data-stu-id="c41b6-133">The sender is the instance of the object on which you subscribed for events.</span></span>  <span data-ttu-id="c41b6-134">Le paramètre args d’événement est une interface qui contient des informations sur l’événement en cours de tir.</span><span class="sxs-lookup"><span data-stu-id="c41b6-134">The event args parameter is an interface that contains information about the currently firing event.</span></span>  

<span data-ttu-id="c41b6-135">Par exemple, `NavigationCompleted` l’événement sur a la paire méthode et la `ICoreWebView2` `ICoreWebView2::add_NavigationCompleted` `ICoreWebView2::remove_NavigationCompleted` paire.</span><span class="sxs-lookup"><span data-stu-id="c41b6-135">For instance, the `NavigationCompleted` event on `ICoreWebView2` has the `ICoreWebView2::add_NavigationCompleted` and `ICoreWebView2::remove_NavigationCompleted` method pair.</span></span>  <span data-ttu-id="c41b6-136">Lorsque vous envoyez une demande, vous fournissez une instance dans laquelle `ICoreWebView2NavigationCompletedEventHandler` vous avez précédemment implémenté la `Invoke` méthode.</span><span class="sxs-lookup"><span data-stu-id="c41b6-136">When you send a request, you provide an instance of `ICoreWebView2NavigationCompletedEventHandler` in which you previously implemented `Invoke` method.</span></span>  <span data-ttu-id="c41b6-137">Lorsque `NavigationCompleted` l’événement s’exécute, `Invoke` votre méthode est demandée.</span><span class="sxs-lookup"><span data-stu-id="c41b6-137">When the `NavigationCompleted` event runs, your `Invoke` method is requested.</span></span>  <span data-ttu-id="c41b6-138">Le premier paramètre exécute `NavigationCompleted` l’événement.</span><span class="sxs-lookup"><span data-stu-id="c41b6-138">The first parameter runs the `NavigationCompleted` event.</span></span>  <span data-ttu-id="c41b6-139">Le deuxième paramètre contient des informations sur la réussite de la navigation, etc.</span><span class="sxs-lookup"><span data-stu-id="c41b6-139">The second parameter contains information about if the navigation completed successfully and so on.</span></span>  

<span data-ttu-id="c41b6-140">À l’exemple de l’interface déléguée de handler terminée de la méthode async, utilisez l’une des actions suivantes pour la configurer.</span><span class="sxs-lookup"><span data-stu-id="c41b6-140">Similar to the async method completed handler delegate interface, use one of the following actions to set it up.</span></span>  

*   <span data-ttu-id="c41b6-141">Implémentez-le directement.</span><span class="sxs-lookup"><span data-stu-id="c41b6-141">Implement it directly.</span></span>  
*   <span data-ttu-id="c41b6-142">Utilisez la [fonction WRL (Callback Function)][CppCxWrlCallbackFunction] utilisée dans l’extrait de code WebView2 suivant.</span><span class="sxs-lookup"><span data-stu-id="c41b6-142">Use the [Callback function (WRL)][CppCxWrlCallbackFunction] function that is used in the following WebView2 code snippet.</span></span>  

<!-- todo:  what is async method completed handler delegate interface?  Is there a shorter name for it?  -->  

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

## <a name="strings"></a><span data-ttu-id="c41b6-143">Chaînes</span><span class="sxs-lookup"><span data-stu-id="c41b6-143">Strings</span></span>  

<span data-ttu-id="c41b6-144">Les paramètres de sortie de chaîne `LPWSTR` sont des chaînes terminées par null.</span><span class="sxs-lookup"><span data-stu-id="c41b6-144">String output parameters are `LPWSTR` null-terminated strings.</span></span>  <span data-ttu-id="c41b6-145">Le demandeur fournit la chaîne à l’aide `CoTaskMemAlloc` de .</span><span class="sxs-lookup"><span data-stu-id="c41b6-145">The requester provides the string using `CoTaskMemAlloc`.</span></span>  <span data-ttu-id="c41b6-146">La propriété est transférée au demandeur et c’est au demandeur de libérer la mémoire à l’aide `CoTaskMemFree` de .</span><span class="sxs-lookup"><span data-stu-id="c41b6-146">Ownership is transferred to the requester and it is up to the requester to free the memory using `CoTaskMemFree`.</span></span>  

<span data-ttu-id="c41b6-147">Les paramètres d’entrée de chaîne `LPCWSTR` sont des chaînes terminées par null.</span><span class="sxs-lookup"><span data-stu-id="c41b6-147">String input parameters are `LPCWSTR` null-terminated strings.</span></span>  <span data-ttu-id="c41b6-148">Le demandeur s’assure que la chaîne est valide pour la durée de la demande de fonction synchrone.</span><span class="sxs-lookup"><span data-stu-id="c41b6-148">The requester ensures the string is valid for the duration of the synchronous function request.</span></span>  <span data-ttu-id="c41b6-149">Si le récepteur doit stocker la valeur à un certain point une fois la demande de fonction terminée, le récepteur doit fournir une copie associée de la valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="c41b6-149">If the receiver must store the value to some point after the function request completes, the receiver must give an associated copy of the string value.</span></span>  

## <a name="uri-and-json-parsing"></a><span data-ttu-id="c41b6-150">URI et l’doncsiation JSON</span><span class="sxs-lookup"><span data-stu-id="c41b6-150">URI and JSON parsing</span></span>  

<span data-ttu-id="c41b6-151">Diverses méthodes fournissent ou acceptent des URS et JSON sous forme de chaînes.</span><span class="sxs-lookup"><span data-stu-id="c41b6-151">Various methods provide or accept URIs and JSON as strings.</span></span>  <span data-ttu-id="c41b6-152">Utilisez votre bibliothèque préférée pour l’utilisation et la génération des chaînes.</span><span class="sxs-lookup"><span data-stu-id="c41b6-152">Use your preferred library for parsing and generating the strings.</span></span>  

<span data-ttu-id="c41b6-153">Si WinRT est disponible pour votre application, vous pouvez utiliser les méthodes et les méthodes pour parer ou produire des chaînes ou des méthodes JSON pour l' `RuntimeClass_Windows_Data_Json_JsonObject` `IJsonObjectStatics` `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` URIS.</span><span class="sxs-lookup"><span data-stu-id="c41b6-153">If WinRT is available for your app, you may use the `RuntimeClass_Windows_Data_Json_JsonObject` and `IJsonObjectStatics` methods to parse or produce JSON strings or `RuntimeClass_Windows_Foundation_Uri` and `IUriRuntimeClassFactory` methods to parse and produce URIs.</span></span>  <span data-ttu-id="c41b6-154">Les deux méthodes fonctionnent dans les applications Win32.</span><span class="sxs-lookup"><span data-stu-id="c41b6-154">Both of methods work in Win32 apps.</span></span>  

<span data-ttu-id="c41b6-155">Si vous utilisez et pour l’URI, vous pouvez utiliser les indicateurs de création d’URI suivants pour que le comportement corresponde plus étroitement à l’URI de l’URI dans `IUri` `CreateUri` `CreateUri` WebView.</span><span class="sxs-lookup"><span data-stu-id="c41b6-155">If you use `IUri` and `CreateUri` to parse URIs, you may want to use the following URI creation flags to have `CreateUri` behavior more closely match the URI parsing in the WebView.</span></span>  

```json
Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO
```  

## <a name="see-also"></a><span data-ttu-id="c41b6-156">Voir également</span><span class="sxs-lookup"><span data-stu-id="c41b6-156">See also</span></span>  

*   <span data-ttu-id="c41b6-157">To get started using WebView2 Win32 C/C++, navigate to [Getting started with WebView2][Webview2IndexGettingStarted] guides.</span><span class="sxs-lookup"><span data-stu-id="c41b6-157">To get started using WebView2 Win32 C/C++, navigate to [Getting started with WebView2][Webview2IndexGettingStarted] guides.</span></span>  
*   <span data-ttu-id="c41b6-158">Pour plus d’informations sur les API WebView2, accédez à la [référence d’API.][DotnetApiMicrosoftWebWebview2WpfWebview2]</span><span class="sxs-lookup"><span data-stu-id="c41b6-158">For more detailed information about WebView2 APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2WpfWebview2].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="c41b6-159">Entrer en contact avec l’équipe Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="c41b6-159">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2GettingstartedWin32]: ../gettingstarted/win32.md "Getting started with WebView2 | Documents Microsoft"  

[Webview2ReferenceWin32Icorewebview2CapturePreview]: /microsoft-edge/webview2/reference/win32/icorewebview2#capturepreview "CapturePreview - interface ICoreWebView2 | Documents Microsoft"  

[CppCxWrlCallbackFunction]: /cpp/cppcx/wrl/callback-function-wrl "Callback Function (WRL) | Documents Microsoft"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "Classe WebView2 | Documents Microsoft"  
