---
description: Découvrez comment utiliser JavaScript dans des scénarios complexes dans les applications WebView2
title: Utiliser JavaScript dans les applications WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: 8db5c4a5b3709c144240fe88e6f8480445c1659f
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535894"
---
# <a name="use-javascript-in-webview-for-extended-scenarios"></a>Utiliser JavaScript dans WebView pour les scénarios étendus  

L’utilisation de JavaScript dans les contrôles WebView2 vous permet de personnaliser les applications natives pour répondre à vos besoins.  Cet article explique comment utiliser JavaScript dans WebView2 et explique comment développer à l’aide des fonctionnalités WebView2 avancées.  

## <a name="before-you-begin"></a>Avant de commencer  

Cet article suppose que vous avez déjà un projet de travail.  Si vous n’avez pas de projet et que vous souhaitez le suivre, accédez au Guide de Prise en main [WebView2.][Webview2GetStartedWpf]  

## <a name="basic-webview2-functions"></a>Fonctions WebView2 de base  

Utilisez les fonctions suivantes pour commencer à incorporer JavaScript dans votre application WebView.  

| API  | Description  |
|:--- |:--- |  
| [ExecuteScriptAsync][Webview2ReferenceWpfMicrosoftWebExecutescriptasync] | Exécutez JavaScript dans un contrôle WebView. Pour plus d’informations, accédez au didacticiel Prise en main de recherche. |
| [OnDocumentCreatedAsync][Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated] | S’exécute lorsque le modèle objet de document \(DOM\) est créé. |
      
## <a name="scenario--running-a-dedicated-script-file"></a>Scénario : exécution d’un fichier de script dédié  

Dans cette section, accédez à un fichier JavaScript dédié à partir de votre contrôle WebView2.  

> [!NOTE]
> Bien que l’écriture de Code JavaScript en ligne puisse être efficace pour les commandes JavaScript rapides, vous perdez les thèmes de couleur JavaScript et la mise en forme des lignes, ce qui rend difficile l’écriture de grandes sections de code dans Visual Studio.  

Pour résoudre le problème, créez un fichier JavaScript distinct avec votre code, puis passez une référence à ce fichier à l’aide `ExecuteScriptAsync` des paramètres.  

1.  Créez un fichier dans votre projet et ajoutez le `.js` code JavaScript à exécuter.  Par exemple, créez un fichier appelé `script.js` .  
1.  Convertissez le fichier JavaScript en une chaîne qui est transmise à `ExecuteScriptAsync` .  
    1.  Pour convertir votre fichier JavaScript en chaîne, copiez l’extrait de code suivant.  
        
        ```csharp
        string text = System.IO.File.ReadAllText(@"C:\PATH_TO_YOUR_FILE\script.js");
        ```  
        
    1.  Collez le code dans `MainWindow.xaml.cs` .  
1.  Passez votre variable de texte à l’aide `ExecuteScriptAsync` de .  
    
    ```csharp
    await webView.CoreWebView2.ExecuteScriptAsync(text);
    ```  
    
## <a name="scenario--remove-drag-and-drop-functionality"></a>Scénario : supprimer la fonctionnalité glisser-déposer  

Dans cette section, utilisez JavaScript pour supprimer la fonctionnalité glisser-déposer de votre contrôle WebView2.  

Pour commencer, explorez la fonctionnalité de glisser-déposer actuelle.  

1.  Créez `.txt` un fichier pour glisser-déposer.  Par exemple, créez un fichier nommé `contoso.txt` et ajoutez-y du texte.  
1.  Exécutez votre projet.  
1.  Glisser-déposer le `contoso.txt` fichier sur le contrôle WebView.  Une nouvelle fenêtre s’ouvre, qui est le résultat du code dans votre exemple de projet.  
    
    :::image type="complex" source="./media/drag-text.png" alt-text="Résultat d’un glisser-déposer contoso.txt" lightbox="./media/drag-text.png":::
       Résultat d’un glisser-déposer contoso.txt  
    :::image-end:::  
    
À présent, ajoutez du code pour supprimer la fonctionnalité glisser-déposer du contrôle WebView2.  

1.  Copiez et collez l’extrait de code suivant dans `InitializeAsync()` `MainWindow.xaml.cs` .   
    
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('dragover',function(e){e.preventDefault();},false);");
    
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('drop',function(e){" +
    "e.preventDefault();" +
    "console.log(e.dataTransfer);" +
    "console.log(e.dataTransfer.files[0])" +
    "}, false);");
    ```  
    
1.  Exécutez votre projet.  
1.  Essayez de `contoso.txt` glisser-déposer.  Confirmez que vous ne pouvez pas glisser-déposer.  
    
## <a name="scenario--removing-the-context-menu"></a>Scénario : suppression du menu Context  

Dans cette section, supprimez le menu contexté par défaut de votre contrôle WebView2.  

Pour commencer, explorez la fonctionnalité actuelle du menu contextuel.  

1.  Exécutez votre projet.  
1.  Pointez n’importe où sur le contrôle WebView2 et ouvrez le menu contexto \(clic droit\).  Le menu contexté affiche les choix par défaut.  
    
    :::image type="complex" source="./media/context-menu.png" alt-text="Menu contexté affichant les choix par défaut" lightbox="./media/context-menu.png":::
       Menu contexté affichant les choix par défaut  
    :::image-end:::  
    
À présent, ajoutez du code pour supprimer la fonctionnalité de menu contextuel du contrôle WebView2.  

1.  Copiez et collez l’extrait de code suivant dans `InitializeAsync()` `MainWindow.xaml.cs` .    
    
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('contextmenu', window => {window.preventDefault();});");
    ```  
    
1.  Exécutez à nouveau le code.  Confirmez que vous n’êtes pas en mesure d’ouvrir un menu contexto \(clic droit\).  
    
## <a name="see-also"></a>Articles associés  

*   To get started using WebView2, navigate to [WebView2 Prise en main Guides][Webview2MainGetStarted].  
*   Pour obtenir un exemple complet des fonctionnalités WebView2, accédez au repo [WebView2Samples][GithubMicrosoftedgeWebview2samples] GitHub.  
*   Pour plus d’informations sur les API WebView2, accédez à la [référence d’API.][Webview2ApiReference]  
*   Pour plus d’informations sur WebView2, accédez [à Ressources WebView2.][Webview2MainNextSteps]  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Entrer en contact avec l’équipe web Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Microsoft Edge outils de développement (Chromium) | Documents Microsoft"  

[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge Référence de l’API WebView2 | Documents Microsoft"  
[Webview2GetStartedWpf]: ../get-started/wpf.md "Mise en place de WebView2 dans WPF (prévisualisation) | Documents Microsoft"  
[Webview2MainGetStarted]: ../index.md#get-started "Get started - Introduction to Microsoft Edge WebView2 (Preview) | Documents Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Étapes suivantes : présentation de Microsoft Edge WebView2 (prévisualisation) | Documents Microsoft"  

[Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated]: /microsoft-edge/webview2/reference/win32/icorewebview2#addscripttoexecuteondocumentcreated "AddScriptToExecuteOnDocumentCreated - 0.9.579 - interface ICoreWebView2 | Documents Microsoft"  

[Webview2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.Exeméthode cuteScriptAsync(String) (Microsoft.Web.WebView2.Wpf) | Documents Microsoft"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  
