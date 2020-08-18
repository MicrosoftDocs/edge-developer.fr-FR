---
description: Hébergement de contenu Web dans votre application WinUI avec le contrôle WebView 2 de Microsoft Edge
title: Applications Microsoft Edge WebView2 pour WinUI
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/17/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, WinUI applications, WinUI, Edge, CoreWebView2, contrôle de navigateur, html Edge, mise en route, mise en route, .NET
ms.openlocfilehash: 805655fd27c0b654e1ccb41c615aa21797d6ddf7
ms.sourcegitcommit: ef6d6adae1f4d18a219fa3e17f91b95b40367a40
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/18/2020
ms.locfileid: "10934897"
---
# <span data-ttu-id="fbcf5-104">Commencer à utiliser WebView2 dans WinUI3 (Preview)</span><span class="sxs-lookup"><span data-stu-id="fbcf5-104">Getting started with WebView2 in WinUI3 (Preview)</span></span>  

<span data-ttu-id="fbcf5-105">Dans cet article, vous pouvez commencer à créer votre première application WebView2 à l’aide de WinUI3 et en savoir plus sur les principales fonctionnalités de [Présentation de Microsoft Edge WebView2 (Preview)][Webview2Index].</span><span class="sxs-lookup"><span data-stu-id="fbcf5-105">In this article, get started creating your first WebView2 app with WinUI3 and learn about the main features of [Introduction to Microsoft Edge WebView2 (Preview)][Webview2Index].</span></span>  <span data-ttu-id="fbcf5-106">Pour plus d’informations sur les API individuelles, voir informations de référence sur les [API][GithubMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="fbcf5-106">For more information on individual APIs, see [API reference][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  

## <span data-ttu-id="fbcf5-107">Prérequis</span><span class="sxs-lookup"><span data-stu-id="fbcf5-107">Prerequisites</span></span>  

<span data-ttu-id="fbcf5-108">Vérifiez que vous disposez de la liste des conditions préalables suivantes avant de poursuivre l’article suivant.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-108">Ensure you install the following list of pre-requisites before proceeding with the following article.</span></span>  

*   <span data-ttu-id="fbcf5-109">Windows 10 version 1803 \ (Build 17134 \) ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-109">Windows 10 version 1803 \(build 17134\) or later.</span></span>  <span data-ttu-id="fbcf5-110">Pour plus d’informations, voir [Windows Update: FAQ][MicrosoftSupport12373].</span><span class="sxs-lookup"><span data-stu-id="fbcf5-110">For more information, see [Windows Update: FAQ][MicrosoftSupport12373].</span></span>  
*   <span data-ttu-id="fbcf5-111">[Canal Canaries Microsoft Edge (chrome)][MicrosoftedgeinsiderDownload] sur Windows 10, Windows 8,1 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-111">[Microsoft Edge (Chromium) Canary channel][MicrosoftedgeinsiderDownload] on Windows 10, Windows 8.1, or Windows 7.</span></span>  
*   <span data-ttu-id="fbcf5-112">Visual Studio 2019, version 16,7 Preview 1.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-112">Visual Studio 2019, version 16.7 Preview 1.</span></span>  <span data-ttu-id="fbcf5-113">Pour plus d’informations, reportez-vous à la rubrique [Windows UI Library 3 Preview 2 (2020 de juillet)][WindowsAppsWinui3ConfigureYourDevEnvironment].</span><span class="sxs-lookup"><span data-stu-id="fbcf5-113">For more information, see [Windows UI Library 3 Preview 2 (July 2020)][WindowsAppsWinui3ConfigureYourDevEnvironment].</span></span>  
*   <span data-ttu-id="fbcf5-114">Les versions [x64][WindowsDotnetcliBlobCoreSdk50100Preview4202681X64] et [x86][WindowsDotnetcliBlobCoreSdk50100Preview4202681X86] de .net 5 Preview 4.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-114">Both the [x64][WindowsDotnetcliBlobCoreSdk50100Preview4202681X64] and [x86][WindowsDotnetcliBlobCoreSdk50100Preview4202681X86] versions of .NET 5 Preview 4.</span></span>  
*   <span data-ttu-id="fbcf5-115">Extension de [modèle de projet WinUI 3][VisualstudioMarketplaceWinUiprojecttemplates] pour Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-115">[WinUI 3 Project Templates][VisualstudioMarketplaceWinUiprojecttemplates] extension for Visual Studio 2019.</span></span>  
<span data-ttu-id="fbcf5-116">Assurez-vous d' [activer le mode développeur][WindowsUwpGetStartedEnableYourDeviceForDevelopment] pour vous assurer que vous avez accès à toutes les fonctionnalités de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-116">Ensure you [Enable Developer Mode][WindowsUwpGetStartedEnableYourDeviceForDevelopment] to ensure you have access to all Visual Studio features.</span></span>  

## <span data-ttu-id="fbcf5-117">Étape 1: créer un projet</span><span class="sxs-lookup"><span data-stu-id="fbcf5-117">Step 1 - Create Project</span></span>  

<span data-ttu-id="fbcf5-118">Utiliser un projet de bureau de base contenant une seule fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-118">Start with a basic desktop project containing a single main window.</span></span>  

1.  <span data-ttu-id="fbcf5-119">Dans Visual Studio, sélectionnez **créer un nouveau projet**.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-119">In Visual Studio, select **Create a new project**.</span></span>  
1.  <span data-ttu-id="fbcf5-120">Dans la liste déroulante projet, sélectionnez respectivement **C#**, **Windows**et **WinUI** .</span><span class="sxs-lookup"><span data-stu-id="fbcf5-120">In the project drop-down, select **C#**, **Windows**, and **WinUI** respectively.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Boîte de dialogue de création de projet Visual Studio pour WinUI" lightbox="./media/winui-gettingstarted-selections.png":::
       <span data-ttu-id="fbcf5-122">Boîte de dialogue de création de projet Visual Studio pour WinUI</span><span class="sxs-lookup"><span data-stu-id="fbcf5-122">Visual studio project creation dialog for WinUI</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="fbcf5-123">Sélectionnez **application vide, empaquetée (WinUI dans le bureau)**, puis sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-123">Choose **Blank App, Packaged (WinUI in Desktop)**, and then choose **Next**.</span></span>  
1.  <span data-ttu-id="fbcf5-124">Entrez le nom d’un projet et sélectionnez les autres options souhaitées, puis cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-124">Enter a project name, choose other options as needed, and then select **Create**.</span></span>  
1.  <span data-ttu-id="fbcf5-125">Dans **nouveau projet de plateforme Windows universelle**, sélectionnez les valeurs suivantes, puis cliquez sur **OK**:</span><span class="sxs-lookup"><span data-stu-id="fbcf5-125">In **New Universal Windows Platform Project**, select the following values, and then choose **OK**:</span></span>  
    *   <span data-ttu-id="fbcf5-126">Version cible: **Windows 10, version 1903 (build 18362)** ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-126">Target version: **Windows 10, version 1903 (build 18362)** or later.</span></span>  
    *   <span data-ttu-id="fbcf5-127">Version minimum: **Windows 10, version 1803 (build 17134)**.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-127">Minimum version: **Windows 10, version 1803 (build 17134)**.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="Nouvelle boîte de dialogue projet de plateforme Windows universelle avec les valeurs sélectionnées pour la version cible et version minimum." lightbox="./media/winui-gettingstarted-projecttype.png":::
       <span data-ttu-id="fbcf5-129">Nouvelle boîte de dialogue projet de plateforme Windows universelle avec les valeurs sélectionnées pour la version cible et version minimum.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-129">The New Universal Windows Platform Project dialog with selected values for Target version and Minimum version.</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="fbcf5-130">Dans l’Explorateur de solutions, deux projets sont générés.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-130">In the Solution Explorer, two projects are generated.</span></span>  
    *   <span data-ttu-id="fbcf5-131">**Nom de votre projet (bureau)**.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-131">**Your project name(Desktop)**.</span></span> <span data-ttu-id="fbcf5-132">Ce projet contient le code de votre application.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-132">This project contains the code for your app.</span></span>  <span data-ttu-id="fbcf5-133">**App.Xaml.cs** définit une `Application` classe qui représente votre instance d’application.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-133">**App.xaml.cs** defines an`Application`class that represents your app instance.</span></span> <span data-ttu-id="fbcf5-134">**MainWindow.Xaml.cs** définit une `MainWindow` classe qui représente la fenêtre principale affichée par votre instance d’application.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-134">**MainWindow.xaml.cs** defines a`MainWindow`class that represents the main window displayed by your app instance.</span></span>  <span data-ttu-id="fbcf5-135">Ces classes dérivent de types dans l' `Microsoft.UI.Xaml` espace de noms de l’WinUI.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-135">These classes derive from types in the`Microsoft.UI.Xaml`namespace of WinUI.</span></span>  
    
    *   <span data-ttu-id="fbcf5-136">**Nom de votre projet (package)**.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-136">**Your project name(Package)**.</span></span>  <span data-ttu-id="fbcf5-137">Ce projet est aWindows Application Packaging Projectthat est configuré pour générer l’application dans un package MSIX pour le déploiement.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-137">This project is aWindows Application Packaging Projectthat is configured to build the app into an MSIX package for deployment.</span></span>  <span data-ttu-id="fbcf5-138">Le projet contient thepackage manifestfor votre application et c’est le projet de démarrage de votre solution par défaut.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-138">The project contains thepackage manifestfor your app, and it is the startup project for your solution by default.</span></span> <span data-ttu-id="fbcf5-139">Pour plus d’informations, reportez-vous à [la rubrique Configuration de votre application de bureau pour MSIX Packaging dans Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] et [référence de schéma de manifeste de package pour Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span><span class="sxs-lookup"><span data-stu-id="fbcf5-139">For more information, see [Set up your desktop application for MSIX packaging in Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] and [Package manifest schema reference for Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span></span>
    
1.  <span data-ttu-id="fbcf5-140">Dans l’Explorateur de solutions, ouvrez **MainWindow. Xaml** pour afficher le code.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-140">In the Solution Explorer, open **MainWindow.xaml** to display the code.</span></span>  <span data-ttu-id="fbcf5-141">Sélectionnez `F5` pour exécuter votre projet et afficher une fenêtre avec un bouton.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-141">Select `F5` to run your project and show a window with a button.</span></span>  
    
## <span data-ttu-id="fbcf5-142">Étape 2: ajouter un contrôle WebView2 à votre projet</span><span class="sxs-lookup"><span data-stu-id="fbcf5-142">Step 2 - Add a WebView2 control to your project</span></span>  

<span data-ttu-id="fbcf5-143">Ensuite, ajoutez un contrôle WebView2 à votre projet.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-143">Next add a WebView2 control to your project.</span></span>  

1.  <span data-ttu-id="fbcf5-144">Ouvrir `MainWindow.xaml` .</span><span class="sxs-lookup"><span data-stu-id="fbcf5-144">Open `MainWindow.xaml`.</span></span>  <span data-ttu-id="fbcf5-145">Ajoutez l’espace de noms XAML WebView2 en insérant la ligne suivante dans la `<Window/>` balise.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-145">Add the WebView2 XAML namespace by inserting the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    <span data-ttu-id="fbcf5-146">Vérifiez que votre code `MainWindow.xaml` est semblable à l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-146">Confirm that your code in `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="fbcf5-147">Pour ajouter le contrôle WebView2, remplacez les `<StackPanel>` balises par l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-147">To add the WebView2 control, replace the `<StackPanel>` tags with the following code snippet.</span></span>  <span data-ttu-id="fbcf5-148">La `Source` propriété définit l’URI initial affiché dans le contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-148">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
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
    
1.  <span data-ttu-id="fbcf5-149">Ouvrez `MainWindow.xaml.cs` et mettez en commentaire la ligne suivante.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-149">Open `MainWindow.xaml.cs` and comment out the following line.</span></span>
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  <span data-ttu-id="fbcf5-150">Sélectionnez `F5` pour générer et exécuter votre projet.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-150">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="fbcf5-151">Vérifiez que votre contrôle WebView2 s’affiche [https://www.microsoft.com][|::ref1::|Main] .</span><span class="sxs-lookup"><span data-stu-id="fbcf5-151">Confirm that your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="Contrôle WebView2 affichant le site microsoft.com" lightbox="./media/winui-gettingstarted-part3.png":::
       <span data-ttu-id="fbcf5-153">Un contrôle WebView2 affichant le site microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-153">A WebView2 control displaying the microsoft.com site.</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="fbcf5-154">Étape 3: ajouter des contrôles de navigation</span><span class="sxs-lookup"><span data-stu-id="fbcf5-154">Step 3 - Add navigation controls</span></span>  

<span data-ttu-id="fbcf5-155">Autorisez les utilisateurs à contrôler la page Web affichée dans votre contrôle WebView2 en ajoutant une barre d’adresse à votre application.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-155">Allow users to control the web page that is displayed in your WebView2 control by adding an address bar to your app.</span></span> 

1.  <span data-ttu-id="fbcf5-156">Dans **MainWindow. Xaml**, copiez et collez l’extrait de code suivant à l’intérieur de l' `Grid` élément qui contient l' `WebView2` élément.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-156">In **MainWindow.xaml**, copy and paste the following code snippet inside the `Grid` element that contains the `WebView2` element.</span></span>  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    <span data-ttu-id="fbcf5-157">Vérifiez que votre `Grid` élément `MainWindow.xaml` est semblable à l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-157">Confirm that your `Grid` element of `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="fbcf5-158">Dans **MainWindow.Xaml.cs**, copiez l’extrait de code suivant dans `myButton_Click` , qui parcourt le contrôle WEBVIEW2 sur l’URL entrée dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-158">In **MainWindow.xaml.cs**, copy the following code snippet to `myButton_Click`, which navigates the WebView2 control to the URL entered in the address bar.</span></span>  
    
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
    
    <span data-ttu-id="fbcf5-159">Sélectionnez `F5` pour générer et exécuter votre projet.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-159">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="fbcf5-160">Entrez une nouvelle URL dans la barre d’adresses, puis sélectionnez **atteindre**.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-160">Enter a new URL in the address bar, and then select **Go**.</span></span>  <span data-ttu-id="fbcf5-161">Par exemple, entrez `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="fbcf5-161">For example, enter `https://www.bing.com`.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="fbcf5-162">Vérifiez que vous utilisez les URL complètes dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-162">Ensure you use complete URLs in the address bar.</span></span> `ArgumentException` <span data-ttu-id="fbcf5-163">des exceptions sont levées si l’URL ne commence pas par `http://` ou `https://` .</span><span class="sxs-lookup"><span data-stu-id="fbcf5-163">exceptions are thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="Bing.com" lightbox="./media/winui-gettingstarted-bing.png":::
       <span data-ttu-id="fbcf5-165">Bing.com</span><span class="sxs-lookup"><span data-stu-id="fbcf5-165">Bing.com</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="fbcf5-166">Étape 4: événements de navigation</span><span class="sxs-lookup"><span data-stu-id="fbcf5-166">Step 4 - Navigation events</span></span>  

<span data-ttu-id="fbcf5-167">Les applications qui hébergent des contrôles WebView2 écoutent les événements suivants qui sont déclenchés par des contrôles WebView2 lors de la navigation dans la page Web.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-167">Applications that host WebView2 controls listen for the following events that are raised by WebView2 controls during web page navigation.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

> [!NOTE]
> <span data-ttu-id="fbcf5-168">La redirection HTTP déclenche plusieurs `NavigationStarting` événements.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-168">HTTP redirects raise multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="fbcf5-169">Pour plus d’informations, voir [événements de navigation][Webviews2ConceptsNavigationEvents].</span><span class="sxs-lookup"><span data-stu-id="fbcf5-169">For more information, see [Navigation Events][Webviews2ConceptsNavigationEvents].</span></span>  

<span data-ttu-id="fbcf5-170">Lorsque des erreurs se produisent, les événements suivants sont déclenchés et peuvent accéder à une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-170">When errors occur, the following events are raised and may navigate to an error page.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
     
<span data-ttu-id="fbcf5-171">Pour obtenir un exemple d’utilisation des événements, inscrivez un gestionnaire pour `NavigationStarting` Annuler toutes les demandes qui n’utilisent pas HTTPS.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-171">As an example of how to use the events, register a handler for `NavigationStarting` that cancels any requests that don't use HTTPS.</span></span> <span data-ttu-id="fbcf5-172">Dans `MainWindow.xaml.cs` l’exemple, modifiez le constructeur pour s’inscrire `EnsureHttps` , puis ajoutez la fonction pour qu' `EnsureHttps` il corresponde à l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-172">In `MainWindow.xaml.cs`, modify the constructor to register `EnsureHttps`, and add the `EnsureHttps` function so that it matches the following code snippet.</span></span>  

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

<span data-ttu-id="fbcf5-173">Sélectionnez `F5` pour générer et exécuter votre projet.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-173">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="fbcf5-174">Vérifiez que la navigation est bloquée sur les sites HTTP et qu’elle est autorisée pour les sites HTTPs.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-174">Confirm that navigation is blocked to HTTP sites, and allowed for HTTPS sites.</span></span>  

## <span data-ttu-id="fbcf5-175">Étape 5: création de scripts</span><span class="sxs-lookup"><span data-stu-id="fbcf5-175">Step 5 - Scripting</span></span>  

<span data-ttu-id="fbcf5-176">Les applications hôtes risquent d’injecter du code JavaScript dans les contrôles WebView2 lors de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-176">Host applications may inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="fbcf5-177">Le JavaScript injecté s’applique à tous les nouveaux documents de niveau supérieur ainsi qu’à toute image enfant jusqu’à ce que le JavaScript soit supprimé.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-177">The injected JavaScript applies to all new top level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="fbcf5-178">Le JavaScript injecté est exécuté après la création de l’objet global et avant l’exécution de tout autre script inclus dans le document HTML.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-178">The injected JavaScript is run after creation of the global object, and before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="fbcf5-179">Par exemple, l’ajout de scripts envoie une alerte lorsqu’un utilisateur navigue vers des sites non HTTPs.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-179">As an example, add scripts send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="fbcf5-180">Modifiez la `EnsureHttps` fonction pour injecter un script dans le contenu Web à l’aide de [ExecuteScriptAsync][Webviews2ReferenceWpf09515MicrosoftWebExecutescriptasync].</span><span class="sxs-lookup"><span data-stu-id="fbcf5-180">Modify the `EnsureHttps` function to inject a script into the web content using [ExecuteScriptAsync][Webviews2ReferenceWpf09515MicrosoftWebExecutescriptasync].</span></span>  

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

<span data-ttu-id="fbcf5-181">Sélectionnez `F5` pour générer et exécuter votre projet.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-181">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="fbcf5-182">Vérifiez que votre application affiche une alerte lorsque vous naviguez vers un site qui n’utilise pas HTTPs.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-182">Confirm that your application displays an alert when you navigate to a site that does not use HTTPS.</span></span>  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="Contrôle WebView2 montrant une boîte de dialogue d’alerte" lightbox="./media/winui-gettingstarted-script.png":::
   <span data-ttu-id="fbcf5-184">Contrôle WebView2 montrant une boîte de dialogue d’alerte</span><span class="sxs-lookup"><span data-stu-id="fbcf5-184">WebView2 control showing an alert dialog</span></span>
:::image-end:::  

<span data-ttu-id="fbcf5-185">Félicitations, vous avez créé votre première application WebView2.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-185">Congratulations, you built your first WebView2 app.</span></span>  

## <span data-ttu-id="fbcf5-186">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="fbcf5-186">Next Steps</span></span>  

<span data-ttu-id="fbcf5-187">Notre équipe génère actuellement plus d’API WebView2.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-187">Our team is currently building more WebView2 APIs.</span></span>  <span data-ttu-id="fbcf5-188">Pour plus d’informations sur l’état actuel des API WebView2, voir la [spécification WebView2][GithubMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="fbcf5-188">For more information on the current state of WebView2 APIs, see the [WebView2 spec][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  

> [!NOTE]
> <span data-ttu-id="fbcf5-189">L’objet WinRT CoreWebView2 peut ne pas être disponible au moment où les API WebView2 s’expédient.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-189">The WinRT CoreWebView2 object may not be available at the time the WebView2 APIs ship.</span></span> <span data-ttu-id="fbcf5-190">Pour savoir quelles API sont disponibles pour les contrôles WebView2, voir [WebView2 spec][GithubMicrosoftUiXamlSpecsWebview2] pour obtenir la liste des API disponibles.</span><span class="sxs-lookup"><span data-stu-id="fbcf5-190">To understand which APIs are available to WebView2 controls, see [WebView2 Spec][GithubMicrosoftUiXamlSpecsWebview2] for a list of the APIs that are available.</span></span> 

<span data-ttu-id="fbcf5-191">Pour plus d’informations sur les fonctionnalités d’WebView2, voir [concepts de WebView2 et guides de procédures][Webview2IndexNextSteps], et les [exemples WebView2 référentiel Samples][GithubMicrosoftedgeWebview2samplesMain].</span><span class="sxs-lookup"><span data-stu-id="fbcf5-191">For more information about WebView2 capabilities, see [WebView2 Concepts and How-To guides][Webview2IndexNextSteps], and the [WebView2 samples repo][GithubMicrosoftedgeWebview2samplesMain].</span></span>  

## <span data-ttu-id="fbcf5-192">Contacter l’équipe WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="fbcf5-192">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2Index]: ../index.md "Introduction à Microsoft Edge WebView2 (Preview) | Documents Microsoft"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Étapes suivantes-présentation de Microsoft Edge WebView2 (Preview) | Documents Microsoft"  
[Webviews2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Événements de navigation | Documents Microsoft"  
[Webviews2ReferenceWpf09515MicrosoftWebExecutescriptasync]: ../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#executescriptasync "ExecuteScriptAsync-Microsoft. Web. WebView2. WPF. WebView2 classe | Documents Microsoft"  

[UwpSchemasAppxpackageUapmanifestRoot]: /uwp/schemas/appxpackage/uapmanifestschema/schema-root "Référence du schéma de manifeste de package pour Windows 10 | Documents Microsoft"  

[WindowsAppsWinui3ConfigureYourDevEnvironment]: /windows/apps/winui/winui3#configure-your-dev-environment "Configurer votre environnement de développement-bibliothèque d’interface utilisateur 3,0 Preview 1 (2020) | Documents Microsoft"  
[WindowsMsixDesktopToUwpPackagingDotNet]: /windows/msix/desktop/desktop-to-uwp-packaging-dot-net "Configurer votre application de bureau pour MSIX Packaging dans Visual Studio | Documents Microsoft"  
[WindowsUwpGetStartedEnableYourDeviceForDevelopment]: /windows/uwp/get-started/enable-your-device-for-development "Activer votre appareil pour le développement | Documents Microsoft"  

[GithubMicrosoftUiXamlSpecsWebview2]: https://github.com/microsoft/microsoft-ui-xaml-specs/blob/master/active/WebView2/WebView2_spec.md "WebView2 spec-Microsoft/Microsoft-UI-XAML-spéc. GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Exemples de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftMain]: https://www.microsoft.com "Connaissances"  

[MicrosoftSupport12373]: https://support.microsoft.com/help/12373 "Windows Update: FAQ"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X86]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe "Télécharger dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X64]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe " dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe"  

[VisualstudioMarketplaceWinUiprojecttemplates]: https://marketplace.visualstudio.com/items?itemName=Microsoft-WinUI.WinUIProjectTemplates "Modèles de projet WinUI 3"  
