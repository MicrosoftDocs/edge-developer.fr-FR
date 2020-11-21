---
description: Guide de mise en route de WebView2 pour les applications WinUI
title: Mise en route de WebView2 pour les applications WinUI
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, WinUI applications, WinUI, Edge, CoreWebView2, contrôle de navigateur, html Edge, mise en route, mise en route, .NET
ms.openlocfilehash: a1ccffe332f71ee9d53ff267e8cca6bdbda81703
ms.sourcegitcommit: 02c602379537ab3b9d0a355cea7fcf96fdbd8870
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2020
ms.locfileid: "11182720"
---
# Commencer à utiliser WebView2 dans WinUI 3 (Preview)  

Dans cet article, vous allez découvrir comment créer votre première application WebView2 et découvrir les principales fonctionnalités de [Présentation de Microsoft Edge WebView2 (Preview)][Webview2Index].  Votre première application WebView2 utilise WinUI3.  Pour plus d’informations sur les API individuelles, accédez à informations de référence sur les [API][GithubMicrosoftUiXamlSpecsWebview2].  

## Conditions préalables  

Vérifiez que vous disposez de la liste des conditions préalables suivantes avant de poursuivre l’article suivant.  

1.  Windows 10 version 1803 \ (Build 17134 \) ou version ultérieure.  Pour plus d’informations, accédez à [Windows Update: FAQ][MicrosoftSupport12373].  
1.  [Canal Canaries Microsoft Edge (chrome)][MicrosoftedgeinsiderDownload] sur Windows 10, Windows 8,1 ou Windows 7.  
1.  Visual Studio 2019 version 16,9 preview.  Pour plus d’informations, accédez à la [bibliothèque d’interface utilisateur Windows 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].  
    
    Incluez les charges de travail suivantes lors de l’installation de Visual Studio.  
    
    *   Développement de bureau .NET \ (le programme d’installation installe également .NET 5 \)  
    *   Développement de plateforme Windows universelle  
        
    Pour créer des applications C++, vous devez également inclure les charges de travail suivantes.  
    
    *   Développement de bureau avec C++  
    *   Les outils de plateforme Windows universelle en C++ (V142) pour la charge de travail de la plateforme Windows universelle.  Pour plus d’informations, accédez à détails sur l’installation dans la section développement de plateforme Windows universelle, dans le volet droit.  
        
1.  Assurez-vous que la source du package NuGet est activée sur votre système pour [NuGet.org][NugetHome].  Pour plus d’informations, accédez aux [configurations NuGet communes][NugetConsumePackagesConfiguringNugetBehavior] et au kit de configuration de la [communauté Windows][WindowsCommunitytoolkit].  
1.  Téléchargez et installez le [package VSIX 3 Preview][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]3.  Le programme d’installation ajoute les modèles de projet WinUI 3 et le package NuGet contenant les bibliothèques WinUI 3 à Visual Studio 2019.  
    
    Pour obtenir des instructions sur la façon d’ajouter le package VSIX à Visual Studio, accédez à la section [recherche et utilisation des extensions Visual Studio][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox].
    
1.  Activez le [mode développeur][WindowsUwpGetStartedEnableYourDeviceForDevelopment] pour vous assurer que vous avez accès à toutes les fonctionnalités de Visual Studio spécifiques aux développeurs.  
    
## Étape 1: créer un projet  

Utiliser un projet de bureau de base contenant une seule fenêtre principale.  

1.  Dans Visual Studio, sélectionnez **créer un nouveau projet**.  
1.  Dans la liste déroulante projet, sélectionnez respectivement **C#**, **Windows**et **WinUI** .  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Créer un projet WinUI à l’aide de Visual Studio" lightbox="./media/winui-gettingstarted-selections.png":::
        Créer un projet WinUI à l’aide de Visual Studio
    :::image-end:::  
    
1.  Sélectionnez **application vide, empaquetée (WinUI dans le bureau)**, puis sélectionnez **suivant**.  
1.  Entrez le nom d’un projet et sélectionnez les autres options souhaitées, puis cliquez sur **créer**.  
1.  Dans **nouveau projet de plateforme Windows universelle**, sélectionnez les valeurs suivantes, puis cliquez sur **OK**.  
    *   **Version cible**:  **Windows 10, version 1903 (Build 18362)** ou version ultérieure  
    *   **Version minimum**:  **Windows 10, version 1803 (Build 17134)**  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="Nouvelle boîte de dialogue projet de plateforme Windows universelle avec les valeurs choisies pour la version cible et version minimum." lightbox="./media/winui-gettingstarted-projecttype.png":::
       Nouvelle boîte de dialogue projet de plateforme Windows universelle avec les valeurs choisies pour la version cible et version minimum.
    :::image-end:::  
    
1.  Dans l’Explorateur de solutions, deux projets sont générés.  
    *   **Nom de votre projet (bureau)**.  Ce projet contient le code de votre application.  **App.Xaml.cs** définit une `Application` classe qui représente votre instance d’application.  **MainWindow.Xaml.cs** définit une `MainWindow` classe qui représente la fenêtre principale affichée par votre instance d’application.  Ces classes dérivent de types dans l' `Microsoft.UI.Xaml` espace de noms de l’WinUI.  
    
    *   **Nom de votre projet (package)**.  Ce projet est un projet de création de packages d’application Windows configuré pour générer l’application dans un package MSIX à des fins de déploiement.  Le projet contient le manifeste du package de votre application, et il s’agit du projet de démarrage de votre solution par défaut.  Pour plus d’informations, accédez à [configurer votre application de bureau pour MSIX Packaging dans Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] et [référence de schéma de manifeste de package pour Windows 10][UwpSchemasAppxpackageUapmanifestRoot].
    
1.  Dans l’Explorateur de solutions, pour afficher le code, ouvrez `MainWindow.xaml` file.  Sélectionnez `F5` pour exécuter votre projet et afficher une fenêtre avec un bouton.  
    
## Étape 2: ajouter un contrôle WebView2 à votre projet  

Ensuite, ajoutez un contrôle WebView2 à votre projet.  

1.  Ouvrir `MainWindow.xaml` .  Ajoutez l’espace de noms XAML WebView2 en insérant la ligne suivante dans la `<Window/>` balise.  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    Vérifiez que votre code `MainWindow.xaml` est semblable à l’extrait de code suivant.  
    
    ```xml
    <Window
          x:Class="WinUI_Sample.MainWindow"
          xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
          xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
          xmlns:local="using:WinUI_Sample"
          xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
          xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
          mc:Ignorable="d"
          xmlns:controls="using:Microsoft.UI.Xaml.Controls"
          >
        
          <StackPanel Orientation="Horizontal" HorizontalAlignment="Center" VerticalAlignment="Center">
            <Button x:Name="myButton" Click="myButton_Click">Click Me</Button>
          </StackPanel>
    
    </Window>
    ```  
    
1.  Pour ajouter le contrôle WebView2, remplacez les `<StackPanel>` balises par l’extrait de code suivant.  La `Source` propriété définit l’URI initial affiché dans le contrôle WebView2.  
    
    ```xml  
    <Grid>

        <Grid.RowDefinitions>
            <RowDefinition Height="Auto" />
            <RowDefinition Height="*" />
        </Grid.RowDefinitions>
        <Grid.ColumnDefinitions>
            <ColumnDefinition Width="*" />
            <ColumnDefinition Width="Auto" />
        </Grid.ColumnDefinitions>
        
        <controls:WebView2 x:Name="MyWebView"  Grid.Row="1" Grid.ColumnSpan="2" 
            Source="https://www.microsoft.com" HorizontalAlignment="Stretch" VerticalAlignment="Stretch" />
    
    </Grid>
    ```  
    
1.  Ouvrez `MainWindow.xaml.cs` et mettez en commentaire la ligne suivante.
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  Sélectionnez `F5` pour générer et exécuter votre projet.  Vérifiez que votre contrôle WebView2 s’affiche [https://www.microsoft.com][|::ref1::|Main] .  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="Contrôle WebView2 affichant le site microsoft.com" lightbox="./media/winui-gettingstarted-part3.png":::
       Un contrôle WebView2 affichant le site microsoft.com.  
    :::image-end:::  
    
## Étape 3: ajouter des contrôles de navigation  

Autorisez les utilisateurs à contrôler la page Web affichée dans votre contrôle WebView2 en ajoutant une barre d’adresse à votre application.  

1.  Dans `MainWindow.xaml` , copiez et collez l’extrait de code suivant à l’intérieur de l' `Grid` élément qui contient l' `WebView2` élément.  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    Vérifiez que votre `Grid` élément `MainWindow.xaml` est semblable à l’extrait de code suivant.  
    
    ```xml
    <Grid>
    
        <Grid.RowDefinitions>
            <RowDefinition Height="Auto" />
            <RowDefinition Height="*" />
        </Grid.RowDefinitions>
        <Grid.ColumnDefinitions>
            <ColumnDefinition Width="*" />
            <ColumnDefinition Width="Auto" />
        </Grid.ColumnDefinitions>
    
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
        
        <WebView2 x:Name="MyWebView"  Grid.Row="1" Grid.ColumnSpan="2" 
            Source="https://www.microsoft.com" HorizontalAlignment="Stretch" VerticalAlignment="Stretch" />
    
    </Grid>
    ```  
    
1.  Dans l' `MainWindow.xaml.cs` extrait de code suivant, copiez l’extrait de code suivant `myButton_Click` , qui navigue dans le contrôle WebView2 à l’URL entrée dans la barre d’adresses.  
    
    ```csharp
    private void myButton_Click(object sender, RoutedEventArgs e)
    {
        try
        {
            Uri targetUri = new Uri(addressBar.Text);
            MyWebView.Source = targetUri;
        }
        catch (FormatException ex)
        {
            // Incorrect address entered.
        }
    }
    ```  
    
    Sélectionnez `F5` pour générer et exécuter votre projet.  Entrez une nouvelle URL dans la barre d’adresses, puis sélectionnez **atteindre**.  Par exemple, entrez `https://www.bing.com` .  
    
    > [!NOTE]
    > Vérifiez que vous utilisez les URL complètes dans la barre d’adresses.  `ArgumentException` des exceptions sont levées si l’URL ne commence pas par `http://` ou `https://` .  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="Bing.com" lightbox="./media/winui-gettingstarted-bing.png":::
       Bing.com  
    :::image-end:::  
    
## Étape 4: événements de navigation  

Les applications qui hébergent des contrôles WebView2 écoutent les événements suivants qui sont déclenchés par des contrôles WebView2 lors de la navigation dans la page Web.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

> [!NOTE]
> La redirection HTTP déclenche plusieurs `NavigationStarting` événements.  

Pour plus d’informations, accédez à [événements de navigation][Webviews2ConceptsNavigationEvents].  

Lorsque des erreurs se produisent, les événements suivants sont déclenchés et peuvent accéder à une page d’erreur.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
     
Pour obtenir un exemple d’utilisation des événements, inscrivez un gestionnaire pour `NavigationStarting` annuler toute demande qui n’utilise pas HTTPS.  Dans `MainWindow.xaml.cs` l’exemple, modifiez le constructeur pour s’inscrire `EnsureHttps` , puis ajoutez la fonction pour qu' `EnsureHttps` il corresponde à l’extrait de code suivant.  

```csharp
public MainWindow()
{
    InitializeComponent();
    MyWebView.NavigationStarting += EnsureHttps;
}

private void EnsureHttps(WebView2 sender, WebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        args.Cancel = true;
    }
    else
    {
        addressBar.Text = uri;
    }
}
```  

Sélectionnez `F5` pour générer et exécuter votre projet.  Vérifiez que la navigation est bloquée sur les sites HTTP et qu’elle est autorisée pour les sites HTTPs.  

## Étape 5: création de scripts  

Les applications hôtes risquent d’injecter du code JavaScript dans les contrôles WebView2 lors de l’exécution.  Le JavaScript injecté s’applique à tous les nouveaux documents de niveau supérieur ainsi qu’aux trames enfant jusqu’à ce que le JavaScript soit supprimé.  Le JavaScript injecté s’exécute avec un minutage spécifique.  

*   Exécutez-la après la création de l’objet global.  
*   Exécutez-la avant d’exécuter tout autre script inclus dans le document HTML.  

Par exemple, l’ajout de scripts envoie une alerte lorsqu’un utilisateur navigue vers des sites non HTTPs.  Modifiez la `EnsureHttps` fonction pour injecter un script dans le contenu Web qui utilise [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].  

```csharp
private void EnsureHttps(WebView2 sender, WebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        MyWebView.ExecuteScriptAsync($"alert('{uri} is not safe, try an https link')");
        args.Cancel = true;
    }
    else
    {
        addressBar.Text = uri;
    }
}
```  

Sélectionnez `F5` pour générer et exécuter votre projet.  Vérifiez que votre application affiche une alerte lorsque vous naviguez vers un site qui n’utilise pas HTTPs.  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="Contrôle WebView2 montrant une boîte de dialogue d’alerte" lightbox="./media/winui-gettingstarted-script.png":::
   Contrôle WebView2 montrant une boîte de dialogue d’alerte
:::image-end:::  

Félicitations, vous avez créé votre première application WebView2.  

## Étapes suivantes  

Notre équipe génère actuellement plus d’API WebView2.  Pour plus d’informations sur l’état actuel des API WebView2, accédez à la [spécification WebView2][GithubMicrosoftUiXamlSpecsWebview2].  

> [!NOTE]
> L’objet WinRT CoreWebView2 peut ne pas être disponible au moment où les API WebView2 s’expédient.  Pour comprendre les API disponibles pour les contrôles WebView2, accédez à [WebView2 spec][GithubMicrosoftUiXamlSpecsWebview2] pour obtenir la liste des API disponibles.  

Pour plus d’informations sur les fonctionnalités d’WebView2, accédez à la [WebView2 de concepts et de How-To][Webview2IndexNextSteps] et aux [exemples de WebView2 référentiel Samples][GithubMicrosoftedgeWebview2samplesMain].  

## Contacter l’équipe WebView de Microsoft Edge  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2Index]: ../index.md "Introduction à Microsoft Edge WebView2 (Preview) | Documents Microsoft"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Étapes suivantes-présentation de Microsoft Edge WebView2 (Preview) | Documents Microsoft"  
[Webviews2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Événements de navigation | Documents Microsoft"  
[Webviews2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.Exeméthode cuteScriptAsync (chaîne) (Microsoft. Web. WebView2. WPF) | Documents Microsoft"  

[NugetConsumePackagesConfiguringNugetBehavior]: /nuget/consume-packages/configuring-nuget-behavior "Configurations NuGet communes Documents Microsoft"  

[UwpSchemasAppxpackageUapmanifestRoot]: /uwp/schemas/appxpackage/uapmanifestschema/schema-root "Référence du schéma de manifeste de package pour Windows 10 | Documents Microsoft"  

[VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox]: /visualstudio/ide/finding-and-using-visual-studio-extensions#install-without-using-the-manage-extensions-dialog-box "Installer sans utiliser la boîte de dialogue gérer les extensions-gérer les extensions de Visual Studio | Documents Microsoft"  

[WindowsAppsWinui3ConfigureYourDevEnvironment]: /windows/apps/winui/winui3#configure-your-dev-environment "Configurer votre environnement de développement-bibliothèque d’interface utilisateur 3,0 Preview 1 (2020) | Documents Microsoft"  
[WindowsCommunitytoolkit]: /windows/communitytoolkit "Documentation sur le kit d’outils de la communauté Windows | Documents Microsoft"  
[WindowsMsixDesktopToUwpPackagingDotNet]: /windows/msix/desktop/desktop-to-uwp-packaging-dot-net "Configurer votre application de bureau pour MSIX Packaging dans Visual Studio | Documents Microsoft"  
[WindowsUwpGetStartedEnableYourDeviceForDevelopment]: /windows/uwp/get-started/enable-your-device-for-development "Activer votre appareil pour le développement | Documents Microsoft"  

[GithubMicrosoftUiXamlSpecsWebview2]: https://github.com/microsoft/microsoft-ui-xaml-specs/blob/master/active/WebView2/WebView2_spec.md "WebView2 spec-Microsoft/Microsoft-UI-XAML-spéc. GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Exemples de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftMain]: https://www.microsoft.com "Connaissances"  

[MicrosoftSupport12373]: https://support.microsoft.com/help/12373 "Windows Update: FAQ"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  

[NugetHome]: https://nuget.org "Accueil | Galerie NuGet"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X86]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe "Télécharger dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X64]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe " dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe"  

[VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]: https://marketplace.visualstudio.com/items?itemName=Microsoft-WinUI.WinUIProjectTemplates "Modèles de projet WinUI 3 | Visual Studio Marketplace"  
