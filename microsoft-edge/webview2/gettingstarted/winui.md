---
description: Guide de mise en place avec WebView2 pour les applications WinUI
title: Mise en place de WebView2 pour les applications WinUI
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/17/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, webview, applications winui, winui, edge, CoreWebView2, contrôle de navigateur, edge html, mise en main, mise en main, .NET
ms.openlocfilehash: 8ecc40a1940bfb656e2dfdc7ab6f57effa90717d
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536409"
---
# <a name="getting-started-with-webview2-in-winui-3-preview"></a>Mise en place de WebView2 dans WinUI 3 (prévisualisation)  

Dans cet article, commencer à créer votre première application WebView2 et en savoir plus sur les principales fonctionnalités de [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].  Votre première application WebView2 utilise WinUI3.  Pour plus d’informations sur les API individuelles, accédez à la [référence d’API.][GithubMicrosoftMicrosoftUiXamlSpecsWebview2]  

## <a name="prerequisites"></a>Conditions préalables  

Veillez à installer la liste des conditions préalables suivante avant de poursuivre.  

*   [WebView2 Runtime][Webview2Installer] ou tout [canal Microsoft Edge (Chromium) non stable][MicrosoftedgeinsiderDownload] installé sur Windows 10 version 1803 \(build 17134\) ou version ultérieure.  Pour plus d’informations sur Windows 10, accédez à [Windows mise à jour : FAQ][MicrosoftSupport12373].  
    
    > [!NOTE]
    > L’équipe WebView recommande d’utiliser le canal Canary et la version minimale requise est 82.0.488.0.  
    
*   [Visual Studio][MicrosoftVisualstudioMain] 2019, version 16.9 Preview.  Pour plus d’informations, [accédez Windows UI Library 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].  
    *   Incluez les charges de travail suivantes lorsque vous installez Visual Studio.  
        *   .NET Desktop Development \(le programme d’installation installe également .NET 5\)  
        *   Développement de plateforme Windows universelle  
    *   Pour créer des applications C++, vous devez également inclure les charges de travail suivantes.  
        *   Développement de bureau avec C++  
        *   Composant facultatif des outils de plateforme Windows universelle \(v142\) C++ \(v142\) pour la charge de travail de la plateforme Windows universelle.  Pour plus d’informations, accédez aux **détails** de l’installation sous la section développement de la plateforme **Windows** universelle, dans le volet droit.  
        
## <a name="step-0---visual-studio-settings"></a>Étape 0 : Visual Studio paramètres  

1.  Assurez-vous que votre système dispose d’NuGet source de package activée pour [nuget.org][NugetHome].  Pour plus d’informations, accédez aux [configurations NuGet et][NugetConsumePackagesConfiguringNugetBehavior] aux [Windows Community Shared Computer Toolkit][WindowsCommunitytoolkit].  
1.  Téléchargez et installez [le package VSIX WinUI 3 Preview 3.][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]  Le programme d’installation ajoute les modèles de projet WinUI 3 et le package NuGet contenant les bibliothèques WinUI 3 à Visual Studio 2019.  
    
    Pour obtenir des instructions sur l’ajout du package à Visual Studio, accédez à Recherche et utilisation `VSIX` [des extensions Visual Studio de recherche.][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox]
    
1.  Pour accéder à toutes les fonctionnalités de Visual Studio spécifiques au développeur, activer [le Mode développeur.][WindowsUwpGetStartedEnableYourDeviceForDevelopment]  
    
## <a name="step-1---create-project"></a>Étape 1 : créer un Project  

Commencez par un projet de bureau de base qui contient une seule fenêtre principale.  

1.  In Visual Studio, choose **Create a new project**.  
1.  Dans la drop-down du projet, choisissez **C#**, **Windows**et **WinUI** respectivement.  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Créer un projet WinUI à l’aide Visual Studio" lightbox="./media/winui-gettingstarted-selections.png":::
        Créer un projet WinUI à l’aide Visual Studio
    :::image-end:::  
    
1.  Choose **Blank App, Packaged (WinUI in Desktop)**  >  **Next**.  
1.  Entrez un nom de projet.
1.  Choisissez les options selon vos besoins.  
1.  Choisissez **Créer**.  
1.  Dans **La nouvelle plateforme Windows universelle Project,** choisissez les valeurs suivantes, puis choisissez **OK.**  
    *   **Version cible**: **Windows 10, version 1903 (build 18362)** ou ultérieure  
    *   **Version minimale**: **Windows 10, version 1803 (build 17134)**  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="Boîte de dialogue Nouvelle plateforme Windows universelle Project avec les valeurs choisies pour la version cible et la version minimale." lightbox="./media/winui-gettingstarted-projecttype.png":::
       Boîte de dialogue Nouvelle plateforme Windows universelle Project avec les valeurs choisies pour la version cible et la version minimale.
    :::image-end:::  
    
1.  Dans l’Explorateur de solutions, deux projets sont générés.  
    *   **Nom de votre projet (Bureau)**.  Le projet Bureau contient le code de votre application.  Le `App.xaml.cs` fichier définit une classe qui représente `Application` l’instance de votre application.  Le `MainWindow.xaml.cs` fichier définit une classe qui représente la fenêtre principale affichée par `MainWindow` l’instance de votre application.  Les classes dérivent des types de `Microsoft.UI.Xaml` l’espace de noms WinUI.  
    *   **Nom de votre projet (package).**  Le projet package est un Windows package d’application Project qui est configuré pour créer l’application dans un package MSIX pour le déploiement.  Le projet contient le manifeste du package de votre application et est le projet de démarrage de votre solution par défaut.  Pour plus d’informations, accédez à Configurer votre application de bureau pour la mise en package [MSIX][WindowsMsixDesktopToUwpPackagingDotNet] dans Visual Studio et référence de schéma de manifeste de package [pour Windows 10][UwpSchemasAppxpackageUapmanifestRoot].  
1.  Dans l’Explorateur de solutions, pour afficher le code, ouvrez le `MainWindow.xaml` fichier.  Pour exécuter votre projet et afficher une fenêtre avec un bouton, sélectionnez `F5` .  
    
## <a name="step-2---add-a-webview2-control-to-your-project"></a>Étape 2 : ajouter un contrôle WebView2 à votre projet  

Ajoutez un contrôle WebView2 à votre projet.  

1.  Dans le fichier, pour ajouter l’espace de noms `MainWindow.xaml` XAML WebView2, insérez la ligne suivante à l’intérieur de la `<Window/>` balise.  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    Assurez-vous que votre code `MainWindow.xaml` est similaire à l’extrait de code suivant.  
    
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
    
1.  Pour ajouter le contrôle WebView2, remplacez les balises par l’extrait de `<StackPanel>` code suivant.  La `Source` propriété définit l’URI initial affiché dans le contrôle WebView2.  
    
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
    
1.  Dans le `MainWindow.xaml.cs` fichier, commentez la ligne suivante.
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  Pour créer et exécuter votre projet, sélectionnez `F5` .  Assurez-vous que votre contrôle WebView2 [https://www.microsoft.com][|::ref1::|Main] s’affiche.  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="Le contrôle WebView2 affiche les microsoft.com" lightbox="./media/winui-gettingstarted-part3.png":::
       Le contrôle WebView2 affiche les microsoft.com  
    :::image-end:::  
    
## <a name="step-3---add-navigation-controls"></a>Étape 3 : ajouter des contrôles de navigation  

Pour permettre aux utilisateurs de contrôler la page web qui s’affiche dans votre contrôle WebView2, ajoutez une barre d’adresse à votre application.  

1.  Dans le fichier, copiez et collez l’extrait de code suivant à l’intérieur de `MainWindow.xaml` `<Grid>` l’élément qui contient `WebView2` l’élément.  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    `<Grid>`Assurez-vous que votre élément dans le fichier est similaire à `MainWindow.xaml` l’extrait de code suivant.  
    
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
    
1.  Dans le fichier, copiez l’extrait de code suivant dans , qui navigue le contrôle WebView2 vers l’URL entrée `MainWindow.xaml.cs` `myButton_Click` dans la barre d’adresses.  
    
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
    
    Pour créer et exécuter votre projet, sélectionnez `F5` .  Entrez une nouvelle URL dans la barre d’adresses, puis choisissez **Go**.  Par exemple, entrez `https://www.bing.com` .  
    
    > [!NOTE]
    > Veillez à entrer les URL complètes dans la barre d’adresses.  `ArgumentException` des exceptions sont lancées si l’URL ne commence pas par `http://` ou `https://` .  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="bing.com" lightbox="./media/winui-gettingstarted-bing.png":::
       bing.com  
    :::image-end:::  
    
## <a name="step-4---navigation-events"></a>Étape 4 : événements de navigation  

Les applications qui hébergent des contrôles WebView2 écoutent les événements suivants qui sont élevés par les contrôles WebView2 lors de la navigation dans la page web.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

> [!NOTE]
> Si une redirection HTTP se produit, il existe plusieurs `NavigationStarting` événements dans une ligne.  

Pour plus d’informations, accédez à [Événements de navigation.][Webviews2ConceptsNavigationEvents]  

Lorsque des erreurs se produisent, les événements suivants sont élevés et peuvent accéder à une page web d’erreur.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
     
À titre d’exemple d’utilisation des événements, inscrivez un responsable pour annuler toutes les demandes `NavigationStarting` non HTTPS.  Dans , modifiez le constructeur pour l’inscrire et ajoutez la fonction afin qu’elle corresponde à l’extrait de `MainWindow.xaml.cs` `EnsureHttps` code `EnsureHttps` suivant.  

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

Pour créer et exécuter votre projet, sélectionnez `F5` .  Assurez-vous que la navigation est bloquée sur les sites HTTP et autorisée pour les sites HTTPS.  

## <a name="step-5---scripting"></a>Étape 5 : scripts  

Vous pouvez utiliser des applications hôtes pour injecter du code JavaScript dans des contrôles WebView2 lors de l’utilisation.  Vous pouvez tâcher WebView pour exécuter du javaScript arbitraire ou ajouter des scripts d’initialisation.  Le javaScript injecté s’applique à tous les nouveaux documents de niveau supérieur et aux images enfants jusqu’à ce que le JavaScript soit supprimé.  Le javaScript injecté est exécuté avec un minutage spécifique.  

*   Exécutez-le après la création de l’objet global.  
*   Exécutez-le avant d’exécuter tout autre script inclus dans le document HTML.  

Par exemple, ajoutez des scripts qui envoient une alerte lorsqu’un utilisateur navigue vers des sites non HTTPS.  Modifiez la fonction pour injecter un script dans le contenu web qui `EnsureHttps` utilise [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].  

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

Pour créer et exécuter votre projet, sélectionnez `F5` .  Assurez-vous que votre application affiche une alerte lorsque vous accédez à des sites web non HTTPS.  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="Le contrôle WebView2 affiche une boîte de dialogue d’alerte" lightbox="./media/winui-gettingstarted-script.png":::
   Le contrôle WebView2 affiche une boîte de dialogue d’alerte
:::image-end:::  

Félicitations, vous avez créé votre première application WebView2.  

## <a name="next-steps"></a>Étapes suivantes  

Pour en savoir plus sur WebView2, accédez aux ressources suivantes.  

*   Pour en savoir plus sur la création d’applications WebView2, accédez aux meilleures pratiques de développement [WebView2.][WV2BestPractices]  
*   Pour obtenir un exemple complet des fonctionnalités WebView2, accédez [à WebView2Samples.][GithubMicrosoftedgeWebview2samplesMain]  
*   Pour plus d’informations sur WebView2, accédez à [Ressources WebView2.][Webview2IndexNextSteps]  
    
    > [!NOTE]
    > L’objet WinRT CoreWebView2 n’est peut-être pas disponible avec la version de l’API WebView2.  Pour comprendre quelles API sont disponibles pour les contrôles WebView2, accédez à [WebView2 Spec][GithubMicrosoftMicrosoftUiXamlSpecsWebview2] pour obtenir la liste des API disponibles.  
    
*   Pour plus d’informations sur l’API WebView2, accédez aux spécifications [WebView2.][GithubMicrosoftMicrosoftUiXamlSpecsWebview2]  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Entrer en contact avec l’équipe web Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

Pour envoyer vos demandes ou bogues de fonctionnalité spécifiques à WinUI, accédez à Problèmes [- microsoft/microsoft-ui-xaml][GithubMicrosoftMicrosoftUiXamlIssues] et choisissez **Nouveau problème.**  

<!-- links -->  
[WV2BestPractices]: ../concepts/developer-guide.md "Meilleures pratiques en matière de développement WebView2 | Documents Microsoft"  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: ../index.md "Présentation des Microsoft Edge WebView2 (prévisualisation) | Documents Microsoft"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Étapes suivantes : présentation de Microsoft Edge WebView2 (prévisualisation) | Documents Microsoft"  
[Webviews2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Événements de navigation | Documents Microsoft"  
[Webviews2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.Exeméthode cuteScriptAsync(String) (Microsoft.Web.WebView2.Wpf) | Documents Microsoft"  

[NugetConsumePackagesConfiguringNugetBehavior]: /nuget/consume-packages/configuring-nuget-behavior "Configurations NuGet courantes | Documents Microsoft"  

[UwpSchemasAppxpackageUapmanifestRoot]: /uwp/schemas/appxpackage/uapmanifestschema/schema-root "Référence du schéma de manifeste de package pour Windows 10 | Documents Microsoft"  

[VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox]: /visualstudio/ide/finding-and-using-visual-studio-extensions#install-without-using-the-manage-extensions-dialog-box "Installer sans utiliser la boîte de dialogue Gérer les extensions : gérer les extensions pour Visual Studio | Documents Microsoft"  

[WindowsAppsWinui3ConfigureYourDevEnvironment]: /windows/apps/winui/winui3#configure-your-dev-environment "Configurer votre environnement de Windows UI Library 3.0 Preview 1 (mai 2020) | Documents Microsoft"  
[WindowsCommunitytoolkit]: /windows/communitytoolkit "Windows Community Shared Computer Toolkit documentation | Documents Microsoft"  
[WindowsMsixDesktopToUwpPackagingDotNet]: /windows/msix/desktop/desktop-to-uwp-packaging-dot-net "Configurer votre application de bureau pour l’empaquetage MSIX dans Visual Studio | Documents Microsoft"  
[WindowsUwpGetStartedEnableYourDeviceForDevelopment]: /windows/uwp/get-started/enable-your-device-for-development "Activer votre appareil pour le développement | Documents Microsoft"  

[GithubMicrosoftMicrosoftUiXamlIssues]: https://github.com/microsoft/microsoft-ui-xaml/issues "Problèmes : microsoft/microsoft-ui-xaml | GitHub"  
[GithubMicrosoftMicrosoftUiXamlSpecsWebview2]: https://github.com/microsoft/microsoft-ui-xaml-specs/blob/master/active/WebView2/WebView2_spec.md "Spécifications WebView2 : microsoft/microsoft-ui-xaml-specs | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires WebView - MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftSupport12373]: https://support.microsoft.com/help/12373 "Windows Mise à jour : FAQ"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  

[NugetHome]: https://nuget.org "Accueil | NuGet Galerie"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X86]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe "Télécharger dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X64]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe " dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe"  

[VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]: https://marketplace.visualstudio.com/items?itemName=Microsoft-WinUI.WinUIProjectTemplates "Modèles de Project WinUI 3 | Visual Studio Marketplace"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Programme d’installation WebView2" 
