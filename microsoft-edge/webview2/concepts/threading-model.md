---
description: Modèle de thread
title: Modèle de thread | WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: 7b447f5cc5fcce3439166638d47a0b87e5536c0a
ms.sourcegitcommit: 5e218b24fb21fcfa9c82b99f17373fed1ba5a21c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2021
ms.locfileid: "11462042"
---
# <a name="threading-model"></a><span data-ttu-id="285cb-104">Modèle de thread</span><span class="sxs-lookup"><span data-stu-id="285cb-104">Threading model</span></span> 

:::row:::
   :::column span="1":::
      <span data-ttu-id="285cb-105">Plateformes pris en charge :</span><span class="sxs-lookup"><span data-stu-id="285cb-105">Supported platforms:</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="285cb-106">Win32, Windows Forms, WinUi, WPF</span><span class="sxs-lookup"><span data-stu-id="285cb-106">Win32, Windows Forms, WinUi, WPF</span></span>
   :::column-end:::
:::row-end:::  

<span data-ttu-id="285cb-107">Le contrôle WebView2 est basé sur le modèle com [(Component Object Model)][WindowsWin32ComTheComponentObjectModel] et doit s’exécuter sur un thread [STA (Single Threaded Caser).][WindowsWin32ComSingleThreadedApartments]</span><span class="sxs-lookup"><span data-stu-id="285cb-107">The WebView2 control is based on the [Component Object Model (COM)][WindowsWin32ComTheComponentObjectModel] and must run on a [Single Threaded Apartments (STA)][WindowsWin32ComSingleThreadedApartments] thread.</span></span>  

## <a name="thread-safety"></a><span data-ttu-id="285cb-108">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="285cb-108">Thread safety</span></span>  

<span data-ttu-id="285cb-109">WebView2 doit être créé sur un thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="285cb-109">The WebView2 must be created on a UI thread.</span></span>  <span data-ttu-id="285cb-110">Plus précisément, un fil de discussion avec un message.</span><span class="sxs-lookup"><span data-stu-id="285cb-110">Specifically, a thread with a message pump.</span></span>  <span data-ttu-id="285cb-111">Tous les rappels se produisent sur ce thread et les requêtes dans Le WebView2 doivent être faites sur ce thread.</span><span class="sxs-lookup"><span data-stu-id="285cb-111">All callbacks occur on that thread and requests into the WebView2 must be done on that thread.</span></span>  <span data-ttu-id="285cb-112">Il n’est pas sûr d’utiliser WebView2 à partir d’un autre thread.</span><span class="sxs-lookup"><span data-stu-id="285cb-112">It isn't safe to use the WebView2 from another thread.</span></span>  

<span data-ttu-id="285cb-113">La seule exception concerne la `Content` propriété de `CoreWebView2WebResourceRequest` .</span><span class="sxs-lookup"><span data-stu-id="285cb-113">The only exception is for the `Content` property of `CoreWebView2WebResourceRequest`.</span></span>  <span data-ttu-id="285cb-114">Le flux `Content` de propriété est lu à partir d’un thread d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="285cb-114">The `Content` property stream is read from a background thread.</span></span>  <span data-ttu-id="285cb-115">Le flux doit être agile ou être créé à partir d’un thread STA d’arrière-plan pour empêcher la dégradation des performances sur le thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="285cb-115">The stream should be agile or be created from a background STA to prevent performance degradation to the UI thread.</span></span>  

## <a name="re-entrancy"></a><span data-ttu-id="285cb-116">Ré-entrancy</span><span class="sxs-lookup"><span data-stu-id="285cb-116">Re-entrancy</span></span>  

<span data-ttu-id="285cb-117">Les rappels, y compris les handleurs d’événements et de fin d’exécution, s’exécutent en série.</span><span class="sxs-lookup"><span data-stu-id="285cb-117">Callbacks including event handlers and completion handlers run serially.</span></span>  
<span data-ttu-id="285cb-118">Une fois que vous avez exécuté un handler d’événements et commencé une boucle de messages, vous ne pouvez exécuter aucun rappel de fin ou de handle d’événement de manière réentrante.</span><span class="sxs-lookup"><span data-stu-id="285cb-118">After you run an event handler and begin a message loop, you're unable to run any event handler or completion callback in a re-entrant manner.</span></span>  

## <a name="deferrals"></a><span data-ttu-id="285cb-119">Reports</span><span class="sxs-lookup"><span data-stu-id="285cb-119">Deferrals</span></span>  

<span data-ttu-id="285cb-120">Certains événements WebView2 lisent les valeurs définies sur les arguments d’événements associés ou démarrent une action une fois que le handler d’événements est terminé.</span><span class="sxs-lookup"><span data-stu-id="285cb-120">Some WebView2 events read values set on the related event arguments or start some action after the event handler completes.</span></span>  <span data-ttu-id="285cb-121">Si vous devez également exécuter une opération asynchrone de ce type de handler d’événements, utilisez la méthode sur les arguments d’événement `GetDeferral` des événements associés.</span><span class="sxs-lookup"><span data-stu-id="285cb-121">If you also need to run an asynchronous operation such an event handler, use the `GetDeferral` method on the event arguments of the associated events.</span></span>  <span data-ttu-id="285cb-122">L’objet renvoyé garantit que le handler d’événements n’est pas considéré comme étant terminé tant que `Deferral` la méthode de l’objet `Complete` `Deferral` n’est pas demandée.</span><span class="sxs-lookup"><span data-stu-id="285cb-122">The returned `Deferral` object ensures the event handler isn't considered complete until the `Complete` method of the `Deferral` is requested.</span></span>  

<span data-ttu-id="285cb-123">Par exemple, vous pouvez utiliser l’événement pour fournir une fenêtre à connecter en tant qu’enfant `NewWindowRequested` lorsque le handler d’événements se `CoreWebView2` termine.</span><span class="sxs-lookup"><span data-stu-id="285cb-123">For instance, you may use the `NewWindowRequested` event to provide a `CoreWebView2` to connect as a child window when the event handler completes.</span></span>  <span data-ttu-id="285cb-124">Mais si vous devez créer de manière asynchrone la `CoreWebView2` , demandez la méthode sur le `GetDeferral` `NewWindowRequestedEventArgs` .</span><span class="sxs-lookup"><span data-stu-id="285cb-124">But if you need to asynchronously create the `CoreWebView2`, request the `GetDeferral` method on the `NewWindowRequestedEventArgs`.</span></span>  <span data-ttu-id="285cb-125">Une fois que vous avez créé de manière asynchrone la propriété et que vous l’avez définie sur l’objet , la requête sur l’objet est renvoyée `CoreWebView2` à `NewWindow` l’aide de la `NewWindowRequestedEventArgs` `Complete` `Deferral` `GetDeferral` méthode.</span><span class="sxs-lookup"><span data-stu-id="285cb-125">After you've asynchronously created the `CoreWebView2` and set the `NewWindow` property on the `NewWindowRequestedEventArgs`, request `Complete` on the `Deferral` object be returned using the `GetDeferral` method.</span></span>  

## <a name="block-the-ui-thread"></a><span data-ttu-id="285cb-126">Bloquer le thread d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="285cb-126">Block the UI thread</span></span>  

<span data-ttu-id="285cb-127">WebView2 s’appuie sur la vision du message du thread d’interface utilisateur pour exécuter des rappels de handler d’événements et des rappels d’achèvement de méthode async.</span><span class="sxs-lookup"><span data-stu-id="285cb-127">The WebView2 relies on the message pump of the UI thread to run event handler callbacks and async method completion callbacks.</span></span>  <span data-ttu-id="285cb-128">Si vous utilisez des méthodes qui bloquent le message, telles que ou , vos serveurs `Task.Result` `WaitForSingleObject` d’événements WebView2 et les handles d’achèvement de méthode async ne s’exécutent pas.</span><span class="sxs-lookup"><span data-stu-id="285cb-128">If you use methods that block the message pump such as `Task.Result` or `WaitForSingleObject`, then your WebView2 event handlers and async method completion handlers don't run.</span></span>  <span data-ttu-id="285cb-129">Par exemple, le code suivant ne se termine pas, car il arrête le message pendant qu’il `Task.Result` attend `ExecuteScriptAsync` d’être terminé.</span><span class="sxs-lookup"><span data-stu-id="285cb-129">For example, the following code doesn't complete, because `Task.Result` stops the message pump while it waits for `ExecuteScriptAsync` to complete.</span></span>  <span data-ttu-id="285cb-130">Dans la mesure où le message est bloqué, `ExecuteScriptAsync` l’opération n’est pas en mesure de se terminer.</span><span class="sxs-lookup"><span data-stu-id="285cb-130">Since the message pump is blocked, the `ExecuteScriptAsync` isn't able to complete.</span></span>   

```csharp
private void Button_Click(object sender, EventArgs e)
{
    string result = webView2Control.CoreWebView2.ExecuteScriptAsync("'test'").Result;
    MessageBox.Show(this, result, "Script Result");
}
```  

<span data-ttu-id="285cb-131">Utilisez un mécanisme asynchrone tel que et , qui ne bloque pas le message ou le `await` `async` thread `await` d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="285cb-131">Use an asynchronous `await` mechanism such as `async` and `await`, which doesn't block the message pump or the UI thread.</span></span>  

```csharp
private async void Button_Click(object sender, EventArgs e)
{
    string result = await webView2Control.CoreWebView2.ExecuteScriptAsync("'test'");
    MessageBox.Show(this, result, "Script Result");
}
```  

## <a name="see-also"></a><span data-ttu-id="285cb-132">Voir également</span><span class="sxs-lookup"><span data-stu-id="285cb-132">See also</span></span>  

*   <span data-ttu-id="285cb-133">Pour commencer à utiliser WebView2, accédez aux guides de mise en page [WebView2.][Webview2IndexGettingStarted]</span><span class="sxs-lookup"><span data-stu-id="285cb-133">To get started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2IndexGettingStarted] guides.</span></span>  
*   <span data-ttu-id="285cb-134">Pour obtenir un exemple complet des fonctionnalités WebView2, accédez au référentiel [WebView2Samples][GithubMicrosoftedgeWebview2samples] sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="285cb-134">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples repo][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>  
*   <span data-ttu-id="285cb-135">Pour plus d’informations sur les API WebView2, accédez à la [référence d’API.][DotnetApiMicrosoftWebWebview2WpfWebview2]</span><span class="sxs-lookup"><span data-stu-id="285cb-135">For more detailed information about WebView2 APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2WpfWebview2].</span></span>  
*   <span data-ttu-id="285cb-136">Pour plus d’informations sur WebView2, accédez à [Ressources WebView2.][Webview2IndexNextSteps]</span><span class="sxs-lookup"><span data-stu-id="285cb-136">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="285cb-137">Entrer en contact avec l’équipe Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="285cb-137">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexGettingStarted]: ../index.md#getting-started "Getting started - Introduction to Microsoft Edge WebView2 | Documents Microsoft"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Étapes suivantes : présentation de Microsoft Edge WebView2 | Documents Microsoft"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "Classe WebView2 | Documents Microsoft"  

[WindowsWin32ComSingleThreadedApartments]: /windows/win32/com/single-threaded-apartments "Single-Threaded | Documents Microsoft"  
[WindowsWin32ComTheComponentObjectModel]: /windows/win32/com/the-component-object-model "Modèle objet composant | Documents Microsoft"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  
