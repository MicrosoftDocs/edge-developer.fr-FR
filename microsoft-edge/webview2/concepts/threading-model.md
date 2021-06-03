---
description: Modèle de filetage
title: Modèle de thread | WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, applications wpf, wpf, edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, edge html
ms.openlocfilehash: 9a7ce3d66e53b832d4430afb153e6539d97e5db7
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535607"
---
# <a name="threading-model"></a>Modèle de filetage 

:::row:::
   :::column span="1":::
      Plateformes pris en charge :
   :::column-end:::
   :::column span="2":::
      Win32, Windows Forms, WinUi, WPF
   :::column-end:::
:::row-end:::  

Le contrôle WebView2 est basé sur le modèle com [(Component Object Model)][WindowsWin32ComTheComponentObjectModel] et doit s’exécuter sur un thread [STA (Single Threaded Threaded Thread).][WindowsWin32ComSingleThreadedApartments]  

## <a name="thread-safety"></a>Sécurité des threads  

WebView2 doit être créé sur un thread d’interface utilisateur.  Plus précisément, un fil de discussion avec un message.  Tous les rappels se produisent sur ce thread et les requêtes dans Le WebView2 doivent être faites sur ce thread.  Il n’est pas sûr d’utiliser WebView2 à partir d’un autre thread.  

La seule exception concerne la `Content` propriété de `CoreWebView2WebResourceRequest` .  Le `Content` flux de propriété est lu à partir d’un thread d’arrière-plan.  Le flux doit être agile ou être créé à partir d’un thread STA d’arrière-plan pour empêcher la dégradation des performances sur le thread d’interface utilisateur.  

## <a name="re-entrancy"></a>Ré-entrancy  

Les rappels, y compris les handleurs d’événements et de fin d’exécution, s’exécutent en série.  
Une fois que vous avez exécuté un handler d’événements et que vous avez commencé une boucle de messages, vous ne pouvez exécuter aucun rappel de fin ou de handle d’événement de manière réentrante.  

## <a name="deferrals"></a>Reports  

Certains événements WebView2 lisent les valeurs définies sur les arguments d’événements associés ou démarrent une action une fois que le handler d’événements est terminé.  Si vous devez également exécuter une opération asynchrone de ce type de handler d’événements, utilisez la méthode sur les arguments d’événement `GetDeferral` des événements associés.  L’objet renvoyé garantit que le handler d’événements n’est pas considéré comme étant terminé tant que `Deferral` `Complete` la méthode `Deferral` n’est pas demandée.  

Par exemple, vous pouvez utiliser l’événement pour fournir une fenêtre à connecter en tant qu’enfant `NewWindowRequested` lorsque le handler d’événements se `CoreWebView2` termine.  Mais si vous devez créer de manière asynchrone la `CoreWebView2` , demandez la méthode sur le `GetDeferral` `NewWindowRequestedEventArgs` .  Une fois que vous avez créé de manière asynchrone la propriété et que vous l’avez définie sur l’objet , la requête sur l’objet est renvoyée `CoreWebView2` à `NewWindow` l’aide de la `NewWindowRequestedEventArgs` `Complete` `Deferral` `GetDeferral` méthode.  

## <a name="block-the-ui-thread"></a>Bloquer le thread d’interface utilisateur  

WebView2 s’appuie sur la vision du message du thread d’interface utilisateur pour exécuter des rappels de handler d’événements et des rappels d’achèvement de méthode async.  Si vous utilisez des méthodes qui bloquent le message, telles que ou , vos serveurs `Task.Result` `WaitForSingleObject` d’événements WebView2 et les handles d’achèvement de méthode async ne s’exécutent pas.  Par exemple, le code suivant ne se termine pas, car il arrête le message pendant qu’il `Task.Result` attend `ExecuteScriptAsync` d’être terminé.  Dans la mesure où le message est bloqué, `ExecuteScriptAsync` l’opération n’est pas en mesure de se terminer.   

```csharp
private void Button_Click(object sender, EventArgs e)
{
    string result = webView2Control.CoreWebView2.ExecuteScriptAsync("'test'").Result;
    MessageBox.Show(this, result, "Script Result");
}
```  

Utilisez un mécanisme asynchrone tel que et , qui ne bloque pas le message ou le `await` `async` thread `await` d’interface utilisateur.  

```csharp
private async void Button_Click(object sender, EventArgs e)
{
    string result = await webView2Control.CoreWebView2.ExecuteScriptAsync("'test'");
    MessageBox.Show(this, result, "Script Result");
}
```  

## <a name="see-also"></a>Articles associés  

*   Pour commencer à utiliser WebView2, accédez aux guides de Prise en main [WebView2.][Webview2IndexGetStarted]  
*   Pour obtenir un exemple complet des fonctionnalités WebView2, accédez au [repo WebView2Samples][GithubMicrosoftedgeWebview2samples] GitHub.  
*   Pour plus d’informations sur les API WebView2, accédez à la référence [d’API.][DotnetApiMicrosoftWebWebview2WpfWebview2]  
*   Pour plus d’informations sur WebView2, accédez [à Ressources WebView2.][Webview2IndexNextSteps]  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Entrer en contact avec l’équipe web Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexGetStarted]: ../index.md#get-started "Get started - Introduction to Microsoft Edge WebView2 | Documents Microsoft"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Étapes suivantes : présentation Microsoft Edge WebView2 | Documents Microsoft"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "Classe WebView2 | Documents Microsoft"  

[WindowsWin32ComSingleThreadedApartments]: /windows/win32/com/single-threaded-apartments "Single-Threaded | Documents Microsoft"  
[WindowsWin32ComTheComponentObjectModel]: /windows/win32/com/the-component-object-model "Modèle objet composant | Documents Microsoft"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  
