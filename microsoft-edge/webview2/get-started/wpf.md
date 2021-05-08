---
description: Guide de mise en ligne avec WebView2 pour les applications WPF
title: Mise en place de WebView2 pour les applications WPF
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, webview, applications wpf, wpf, edge, CoreWebView2, contrôle de navigateur, edge html, get started, Get Started, .NET
ms.openlocfilehash: e7ddb3977d34e8150a10354e638226bcf96d610d
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535926"
---
# <a name="get-started-with-webview2-in-wpf"></a>Mise en place de WebView2 dans WPF

Dans cet article, commencer à créer votre première application WebView2 et en savoir plus sur les principales fonctionnalités de [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].  Pour plus d’informations sur les API individuelles, accédez à la [référence d’API.][DotnetApiMicrosoftWebWebview2Wpf]  

## <a name="prerequisites"></a>Conditions préalables  

Veillez à installer la liste des conditions préalables suivante avant de poursuivre.  

*   [WebView2 Runtime][Webview2Installer] ou tout canal [non stable Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] installé sur le système d’exploitation pris en charge \(actuellement Windows 10, Windows 8.1 et Windows 7\).  
*   [Visual Studio][MicrosoftVisualstudioMain] 2017 ou ultérieure.  
    
## <a name="step-1---create-a-single-window-app"></a>Étape 1 : créer une application à fenêtre unique  

Commencez par un projet de bureau de base qui contient une seule fenêtre principale.  

1.  In Visual Studio, choose **WPF .NET Core App** \(or **WPF .NET Framework App**\) > **Next**.  
    
    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-getting-started-wpf-core.png" alt-text="WPF core":::
             WPF core :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-getting-started-wpf-fw.png" alt-text="WPF Framework":::
             WPF Framework :::image-end:::
       :::column-end:::
    :::row-end:::
    
1.  Entrez des valeurs **pour le nom et l’emplacement** du **projet.**  Choisissez **.NET Framework 4.6.2** ou ultérieure \(ou **.NET Core 3.0** ou ultérieur\).  
    
    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-getting-started-create-core.png" alt-text="Créer un cœur":::
             Créer un cœur :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-getting-started-create-fw.png" alt-text="Créer une infrastructure":::
             Créer une infrastructure :::image-end:::
       :::column-end:::
    :::row-end:::
    
1.  Pour créer votre projet, choisissez **Créer.**  
    
## <a name="step-2---install-webview2-sdk"></a>Étape 2 : installer le SDK WebView2  

Utilisez NuGet pour ajouter le SDK WebView2 au projet.  

1.  Pointez sur le projet, ouvrez le menu contextuel \(clic droit\), puis choisissez Gérer les **packages NuGet...**.  
    
    :::image type="complex" source="./media/wpf-getting-started-mng-nuget.png" alt-text="Gérer des packages NuGet" lightbox="./media/wpf-getting-started-mng-nuget.png":::
       Gérer des packages NuGet
    :::image-end:::
    
1.  Dans la barre de recherche, `Microsoft.Web.WebView2` tapez > **choisissez Microsoft.Web.WebView2**.  
    
    :::image type="complex" source="./media/install-nuget.png" alt-text="NuGet" lightbox="./media/install-nuget.png":::
       NuGet  
    :::image-end:::
    
    Prêt à commencer à développer des applications à l’aide de l’API WebView2.  Pour créer et exécuter le projet, sélectionnez `F5` .  Le projet en cours d’exécution affiche une fenêtre vide.  
    
    :::image type="complex" source="./media/winforms-empty-app.png" alt-text="Application vide" lightbox="./media/winforms-empty-app.png":::
       Application vide  
    :::image-end:::  
    
## <a name="step-3---create-a-single-webview"></a>Étape 3 : créer un seul WebView 

Ensuite, ajoutez un WebView à votre application.  

1.  Dans le fichier, pour ajouter l’espace de noms `MainWindow.xaml` XAML WebView2, insérez la ligne suivante à l’intérieur de la `<Window/>` balise.  
    
    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  
    
    Assurez-vous que le code `MainWindow.xaml` dans ressemble à l’extrait de code suivant.  
    
    ```xml
    <Window x:Class="WPF_Getting_Started.MainWindow"
            xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
            xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
            xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
            xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
            xmlns:local="clr-namespace:{YOUR PROJECT NAME}"
            xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
            mc:Ignorable="d"
            Title="MainWindow"
            Height="450"
            Width="800"
    >
        <Grid>
        
        </Grid>
    </Window>
    ```  
    
1.  Pour ajouter le contrôle WebView2, remplacez les balises par l’extrait de `<Grid>` code suivant.  La `Source` propriété définit l’URI initial affiché dans le contrôle WebView2.  
    
    ```xml  
    <DockPanel>
        <wv2:WebView2 Name="webView"
                      Source="https://www.microsoft.com"
        />
    </DockPanel>
    ```  
    
1.  Pour créer et exécuter le projet, sélectionnez `F5` Vérifier que votre contrôle WebView2 s’affiche. [https://www.microsoft.com][|::ref1::|Main]  
    
    :::image type="complex" source="./media/wpf-getting-started-microsoft.png" alt-text="Microsoft.com":::
       Microsoft.com
    :::image-end:::  
    
## <a name="step-4---navigation"></a>Étape 4 : navigation  

Ajoutez la possibilité d’autoriser les utilisateurs à modifier l’URL affichée par le contrôle WebView2 en ajoutant une barre d’adresse à l’application.

1.  Dans le fichier, ajoutez une barre d’adresses en copiant et en coller l’extrait de code suivant à l’intérieur de l’écran `MainWindow.xaml` `<DockPanel>` WebView.  
    
    ```xml
    <DockPanel DockPanel.Dock="Top">
        <Button x:Name="ButtonGo"
                DockPanel.Dock="Right"
                Click="ButtonGo_Click"
                Content="Go"
        />
        <TextBox Name="addressBar"/>
    </DockPanel>
    ```  
    
    `<DockPanel>`Assurez-vous que la section du fichier correspond à `MainWindow.xaml` l’extrait de code suivant.  
    
    ```xml
    <DockPanel>
        <DockPanel DockPanel.Dock="Top">
            <Button x:Name="ButtonGo" DockPanel.Dock="Right" Click="ButtonGo_Click" Content="Go"/>
            <TextBox Name = "addressBar"/>
        </DockPanel>
        <wv2:WebView2 Name = "webView"
                      Source = "https://www.microsoft.com"
        />
    </DockPanel>
    ```  
    
1.  Dans Visual Studio, dans le fichier, pour ajouter l’espace de noms, insérez l’extrait de code suivant `MainWindow.xaml.cs` `CoreWebView2` en haut.  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```
    
1.  Dans le fichier, copiez l’extrait de code suivant pour créer la méthode, qui permet d’accéder à l’URL entrée dans la barre `MainWindow.xaml.cs` `ButtonGo_Click` d’adresses dans le WebView.  
    
    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  
    
    Pour créer et exécuter le projet, sélectionnez `F5` .  Tapez une nouvelle URL dans la barre d’adresses et choisissez **Go**.  Par exemple, tapez `https://www.bing.com`.  Assurez-vous que le contrôle WebView2 navigue jusqu’à l’URL.  
    
    > [!NOTE]
    > Assurez-vous qu’une URL complète est entrée dans la barre d’adresses.  Une `ArgumentException` url est lancée si l’URL ne commence pas par ou `http://` `https://` .  
    
    :::image type="complex" source="./media/wpf-getting-started-bing.png" alt-text="Bing":::
       bing.com
    :::image-end:::
    
## <a name="step-5---navigation-events"></a>Étape 5 : événements de navigation  

Lors de la navigation sur la page web, le contrôle WebView2 lève des événements.  L’application qui héberge les contrôles WebView2 écoute les événements suivants.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  
    
Pour plus d’informations, accédez à [Événements de navigation.][Webview2ConceptsNavigationEvents]  

:::image type="complex" source="../media/navigation-events.png" alt-text="Événements de navigation":::
   Événements de navigation
:::image-end:::  

Lorsqu’une erreur se produit, les événements suivants sont élevés et peuvent dépendre de la navigation vers une page web d’erreur.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
    
> [!NOTE]
> Si une redirection HTTP se produit, il existe plusieurs `NavigationStarting` événements dans une ligne.  

Pour montrer comment utiliser les événements, inscrivez un responsable pour annuler toutes les demandes `NavigationStarting` non HTTPS.  

Dans le fichier, modifiez le constructeur pour qu’il corresponde à l’extrait de code suivant `MainWindow.xaml.cs` et ajoutez la `EnsureHttps` fonction.  

```csharp
public MainWindow()
{
    InitializeComponent();
    webView.NavigationStarting += EnsureHttps;
}

void EnsureHttps(object sender, CoreWebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        args.Cancel = true;
    }
}
```  

Dans le constructeur, est inscrit en tant que le `EnsureHttps` handler d’événements sur `NavigationStarting` l’événement sur le contrôle WebView2.  

Pour créer et exécuter le projet, sélectionnez `F5` .  Assurez-vous que lorsque vous naviguez vers un site HTTP, le WebView reste inchangé.  Toutefois, le WebView navigue vers les sites HTTPS.  

## <a name="step-6---scripting"></a>Étape 6 : écriture de scripts  

Vous pouvez utiliser des applications hôtes pour injecter du code JavaScript dans des contrôles WebView2 lors de l’utilisation.  Vous pouvez tâcher WebView pour exécuter du javaScript arbitraire ou ajouter des scripts d’initialisation.  Le javaScript injecté s’applique à tous les nouveaux documents de niveau supérieur et aux images enfants jusqu’à ce que le JavaScript soit supprimé.  Le javaScript injecté est exécuté avec un minutage spécifique.  

*   Exécutez-le après la création de l’objet global.  
*   Exécutez-le avant d’exécuter tout autre script inclus dans le document HTML.  
    
Par exemple, ajoutez des scripts qui envoient une alerte lorsqu’un utilisateur navigue vers des sites non HTTPS.  Modifiez la fonction pour injecter un script dans le contenu web qui utilise la méthode `EnsureHttps` [ExecuteScriptAsync.](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync)  

```csharp
void EnsureHttps(object sender, CoreWebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        webView.CoreWebView2.ExecuteScriptAsync($"alert('{uri} is not safe, try an https link')");
        args.Cancel = true;
    }
}
```  

Pour créer et exécuter le projet, sélectionnez `F5` .  Assurez-vous que l’application affiche une alerte lorsque vous accédez à un site web qui n’utilise pas HTTPS.  

:::image type="complex" source="./media/wpf-getting-started-https.png" alt-text="HTTPS":::
   HTTPS
:::image-end:::  

## <a name="step-7---communication-between-host-and-web-content"></a>Étape 7 : communication entre le contenu hôte et le contenu web  

Le contenu hôte et web peut communiquer de l’une des manières suivantes à l’aide de `postMessage` .  

*   Le contenu web d’un contrôle WebView2 peut publier un message à l’hôte à l’aide de `window.chrome.webview.postMessage` .  L’hôte gère le message à l’aide de tous les messages `WebMessageReceived` enregistrés sur l’hôte.  
*   Héberge des messages publiés dans du contenu web dans un contrôle WebView2 à l’aide `CoreWebView2.PostWebMessageAsString` ou `CoreWebView2.PostWebMessageAsJSON` .  Les messages sont capturés par des responsables ajoutés à `window.chrome.webview.addEventListener` .  
    
Le mécanisme de communication transmet les messages du contenu web à l’hôte à l’aide de fonctionnalités natives.  

Dans votre projet, lorsque le contrôle WebView2 navigue vers une URL, il affiche l’URL dans la barre d’adresses et avertit l’utilisateur de l’URL affichée dans le contrôle WebView2.  

1.  Dans le fichier, mettez à jour votre constructeur et `MainWindow.xaml.cs` créez `InitializeAsync` une fonction pour qu’elle corresponde à l’extrait de code suivant.  La `InitializeAsync` fonction attend [EnsureCoreWebView2Async,](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) car l’initialisation est `CoreWebView2` asynchrone.  
    
    ```csharp
    public MainWindow()
    {
        InitializeComponent();
        webView.NavigationStarting += EnsureHttps;
        InitializeAsync();
    }
    
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
    }
    ```  
    
1.  Une **fois CoreWebView2** initialisé, inscrivez un handler d’événements pour y `WebMessageReceived` répondre.  Dans `MainWindow.xaml.cs` , mettez à jour et `InitializeAsync` `UpdateAddressBar` ajoutez à l’aide de l’extrait de code suivant.  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
    }
    
    void UpdateAddressBar(object sender, CoreWebView2WebMessageReceivedEventArgs args)
    {
        String uri = args.TryGetWebMessageAsString();
        addressBar.Text = uri;
        webView.CoreWebView2.PostWebMessageAsString(uri);
    }
    ```  
    
1.  Pour que Le WebView envoie et réponde au message web, une fois `CoreWebView2` initialisé, l’hôte :  
    1.  Injecte un script au contenu web qui inscrit un handler pour imprimer un message à partir de l’hôte.  
    1.  Injecte un script au contenu web qui publie l’URL à l’hôte.  
        
    Dans le `MainWindow.xaml.cs` fichier, mettez à `InitializeAsync` jour pour correspondre à l’extrait de code suivant.  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
        
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
    }
    ```  
    
    Pour créer et exécuter l’application, sélectionnez `F5` .  À présent, la barre d’adresses affiche l’URI dans le contrôle WebView2.  Lorsque vous accédez à un nouvel URI, le contrôle WebView2 avertit l’utilisateur de l’URI qui s’affiche dans le contrôle WebView2.  
    
    :::image type="complex" source="./media/wpf-getting-started-searchbar.png" alt-text="addressBar":::
       addressBar
    :::image-end:::
    
Félicitations, vous avez créé votre première application WebView2.  

## <a name="next-steps"></a>Étapes suivantes  

Pour en savoir plus sur WebView2, accédez aux ressources suivantes.  

*   Pour en savoir plus sur la création d’applications WebView2, accédez aux meilleures pratiques de développement [WebView2.][WV2BestPractices]  
*   Pour obtenir un exemple complet des fonctionnalités WebView2, accédez au référentiel [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain] sur GitHub.  
*   Pour plus d’informations sur l’API WebView2, accédez à la référence [d’API.](/dotnet/api/microsoft.web.webview2.wpf.webview2)  
*   Pour plus d’informations sur WebView2, accédez à [Ressources WebView2.](../index.md#next-steps)  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Entrer en contact avec l’équipe Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  
 
[WV2BestPractices]: ../concepts/developer-guide.md "Meilleures pratiques en matière de développement WebView2 | Documents Microsoft"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Événements de navigation | Documents Microsoft"  

[DotnetApiMicrosoftWebWebview2Wpf]: /dotnet/api/microsoft.web.webview2.wpf "Espace de noms Microsoft.Web.WebView2.Wpf | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "Classe WebView2 | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async "Méthode WebView2.EnsureCoreWebView2Async(CoreWebView2Environment) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Executescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.ExecuteScriptAsync(String) Method | Documents Microsoft"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 " WebView2 | Développeur Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftVisualStudioMain]: https://visualstudio.microsoft.com "Microsoft Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Programme d’installation WebView2" 
