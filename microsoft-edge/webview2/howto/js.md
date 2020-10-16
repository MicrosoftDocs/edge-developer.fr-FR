---
description: Apprenez à utiliser JavaScript dans des scénarios complexes dans les applications WebView2
title: Utiliser JavaScript dans les applications WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/15/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 0fd4e33b7cfc16dcd19a850147b6efbca8922a8e
ms.sourcegitcommit: 442de63da52d00c6dc27fa08ccdb736534127566
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "11120067"
---
# Utiliser JavaScript dans WebView pour des scénarios étendus  

L’utilisation de JavaScript dans les contrôles WebView2 vous permet de personnaliser les applications natives en fonction de vos besoins.  Cet article décrit l’utilisation de JavaScript dans WebView2 et explique comment développer à l’aide des fonctionnalités et fonctionnalités avancées d’WebView2.  

## Avant de commencer  

Cet article part du principe que vous disposez déjà d’un projet actif.  Si vous n’avez pas de projet et voulez suivre, accédez au [Guide de mise en route de WebView2][Webview2GettingstartedWpf].  

## Fonctions WebView2 de base  

Pour commencer à incorporer du JavaScript dans votre application WebView, utilisez les fonctions suivantes.  

| API  | Description  |
|:--- |:--- |  
| [ExecuteScriptAsync][Webview2ReferenceWpfMicrosoftWebExecutescriptasync] | Exécutez JavaScript dans un contrôle WebView. Pour plus d’informations, accédez au didacticiel de mise en route. |
| [OnDocumentCreatedAsync][Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated] | S’exécute lorsque le modèle d’objet de document (DOM) est créé. |
      
## Scénario: exécution d’un fichier de script dédié  

Dans cette section, accédez à un fichier JavaScript dédié depuis votre contrôle WebView2.  

> [!NOTE]
> Même s’il est possible d’écrire du code JavaScript inline dans les commandes JavaScript rapides, vous perdez les thèmes de couleurs JavaScript et la mise en forme de ligne qui complique la rédaction de grandes sections de code dans Visual Studio.  

Pour résoudre le problème, créez un fichier JavaScript distinct avec votre code, puis transmettez une référence à ce fichier à l’aide des `ExecuteScriptAsync` paramètres.  

1.  Créez un `.js` fichier dans votre projet et ajoutez le code JavaScript que vous souhaitez exécuter.  Par exemple, créez un fichier appelé `script.js` .  
1.  Convertissez le fichier JavaScript en une chaîne qui est transmise à `ExecuteScriptAsync` .  
    1.  Pour convertir votre fichier JavaScript en chaîne, copiez l’extrait de code suivant.  
        
        ```csharp
        string text = System.IO.File.ReadAllText(@"C:\PATH_TO_YOUR_FILE\script.js");
        ```  
        
    1.  Collez le code dans `MainWindow.xaml.cs` .  
1.  Transmettez votre variable de texte à l’aide de `ExecuteScriptAsync` .  
    
    ```csharp
    await webView.CoreWebView2.ExecuteScriptAsync(text);
    ```  

## Scénario: supprimer la fonctionnalité de glisser-déplacer  

Dans cette section, utilisez JavaScript pour supprimer la fonctionnalité de glisser-déplacer de votre contrôle WebView2.  

Pour commencer, explorez la fonctionnalité de glisser-déplacer actuelle.  

1.  Créer un `.txt` fichier pour le glisser-déplacer.  Par exemple, vous pouvez créer un fichier nommé `contoso.txt` et y ajouter du texte.  
1.  Exécutez votre projet.  
1.  Faites un glisser-déplacer du `contoso.txt` fichier vers le contrôle WebView.  Une nouvelle fenêtre s’ouvre, qui est le résultat du code de votre exemple de projet.  
    
    :::image type="complex" source="./media/dragtext.png" alt-text="Résultat du glisser-déplacer de contoso.txt" lightbox="./media/dragtext.png":::
       Résultat du glisser-déplacer de contoso.txt  
    :::image-end:::  

À présent, ajoutez du code pour supprimer la fonctionnalité de glisser-déplacer du contrôle WebView2.  

1.  Copiez et collez l’extrait de code suivant dans `InitializeAsync()` in `MainWindow.xaml.cs` .   
            
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('dragover',function(e){e.preventDefault();},false);");
    
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('drop',function(e){" +
    "e.preventDefault();" +
    "console.log(e.dataTransfer);" +
    "console.log(e.dataTransfer.files[0])" +
    "}, false);");
    ```  
          
1.  Exécutez votre projet.  
1.  Essayez de glisser-déplacer `contoso.txt` .  Vérifiez que vous n’êtes pas en mesure de glisser-déplacer.  

## Scénario: suppression du menu contextuel  

Dans cette section, supprimez le menu contextuel par défaut de votre contrôle WebView2.  

Pour commencer, explorez les fonctionnalités de menu contextuel actuelles.  

1.  Exécutez votre projet.  
1.  Positionnez le curseur n’importe où sur le contrôle WebView2 et ouvrez le menu contextuel (cliquez avec le bouton droit sur \).  Le menu contextuel affiche les choix par défaut.  
    
    :::image type="complex" source="./media/contextmenu.png" alt-text="Résultat du glisser-déplacer de contoso.txt" lightbox="./media/contextmenu.png":::
       Menu contextuel affichant les choix par défaut  
    :::image-end:::  
    
Ajoutez désormais du code pour supprimer la fonctionnalité de menu contextuel du contrôle WebView2.  

1.  Copiez et collez l’extrait de code suivant dans `InitializeAsync()` in `MainWindow.xaml.cs` .    
        
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('contextmenu', window => {window.preventDefault();});");
    ```  

1.  Réexécutez le code.  Vérifiez que vous ne pouvez pas ouvrir un menu contextuel (cliquez avec le bouton droit sur \).  
   
## Voir également  

*   Pour plus d’informations sur la mise en route de WebView2, accédez à [WebView2 guides de mise en route][Webview2MainGettingStarted].  
*   Pour obtenir un exemple complet de fonctionnalités WebView2, accédez au référentiel Samples [WebView2Samples][GithubMicrosoftedgeWebview2samples] sur GitHub.  
*   Pour plus d’informations sur les API WebView2, accédez à informations de référence sur les [API][Webview2ApiReference].  
*   Pour plus d’informations sur WebView2, accédez à [ressources WebView2][Webview2MainNextSteps].  

## Contacter l’équipe WebView de Microsoft Edge  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  


[Webview2ApiReference]: ../webview2-api-reference.md "Référence sur l’API Microsoft Edge WebView2 | Documents Microsoft"  
[Webview2GettingstartedWpf]: ../gettingstarted/wpf.md "Commencer à utiliser WebView2 dans WPF (Preview) | Documents Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Mise en route-présentation de Microsoft Edge WebView2 (Preview) | Documents Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Étapes suivantes-présentation de Microsoft Edge WebView2 (Preview) | Documents Microsoft"  
[Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated]: /microsoft-edge/webview2/reference/win32/icorewebview2#addscripttoexecuteondocumentcreated "AddScriptToExecuteOnDocumentCreated-0.9.579-interface ICoreWebView2 | Documents Microsoft"  
[Webview2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.Exeméthode cuteScriptAsync (chaîne) (Microsoft. Web. WebView2. WPF) | Documents Microsoft"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemples de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  
