---
description: Guide de mise en place avec WebView2 pour les applications WinUI
title: Mise en place de WebView2 pour les applications WinUI
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, webview, applications winui, winui, edge, CoreWebView2, contrôle de navigateur, edge html, mise en main, mise en main, .NET
ms.openlocfilehash: 5188a735eaf635c3b3bc0eead6f4ee4f3a83f1c4
ms.sourcegitcommit: d89f77d4667dfbc44ed35f2ec7e3ae64ab98bf1a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2021
ms.locfileid: "11306151"
---
# <span data-ttu-id="cc7c8-104">Mise en place de WebView2 dans WinUI 3 (prévisualisation)</span><span class="sxs-lookup"><span data-stu-id="cc7c8-104">Getting started with WebView2 in WinUI 3 (Preview)</span></span>  

<span data-ttu-id="cc7c8-105">Dans cet article, commencer à créer votre première application WebView2 et en savoir plus sur les principales fonctionnalités de [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span><span class="sxs-lookup"><span data-stu-id="cc7c8-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="cc7c8-106">Votre première application WebView2 utilise WinUI3.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-106">Your first WebView2 app uses WinUI3.</span></span>  <span data-ttu-id="cc7c8-107">Pour plus d’informations sur les API individuelles, accédez à la [référence d’API.][GithubMicrosoftUiXamlSpecsWebview2]</span><span class="sxs-lookup"><span data-stu-id="cc7c8-107">For more information on individual APIs, navigate to [API reference][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  

## <span data-ttu-id="cc7c8-108">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="cc7c8-108">Prerequisites</span></span>  

<span data-ttu-id="cc7c8-109">Veillez à installer la liste des conditions préalables suivante avant de poursuivre.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-109">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="cc7c8-110">[WebView2 Runtime][Webview2Installer] ou tout canal [non stable Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] installé sur Windows 10 version 1803 \(build 17134\) ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-110">[WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on Windows 10 version 1803 \(build 17134\) or later.</span></span>  <span data-ttu-id="cc7c8-111">Pour plus d’informations sur Windows 10, accédez [à Windows Update : FAQ][MicrosoftSupport12373].</span><span class="sxs-lookup"><span data-stu-id="cc7c8-111">For more information about Windows 10, navigate to [Windows Update: FAQ][MicrosoftSupport12373].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="cc7c8-112">L’équipe WebView recommande d’utiliser le canal Canary et la version minimale requise est 82.0.488.0.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-112">The WebView team recommends using the Canary channel and the minimum required version is 82.0.488.0.</span></span>  
    
*   <span data-ttu-id="cc7c8-113">[Visual Studio][MicrosoftVisualstudioMain] 2019, version 16.9 Preview.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-113">[Visual Studio][MicrosoftVisualstudioMain] 2019, version 16.9 Preview.</span></span>  <span data-ttu-id="cc7c8-114">Pour plus d’informations, accédez [à Windows UI Library 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].</span><span class="sxs-lookup"><span data-stu-id="cc7c8-114">For more information, navigate to [Windows UI Library 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].</span></span>  
    
    *   <span data-ttu-id="cc7c8-115">Incluez les charges de travail suivantes lorsque vous installez Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-115">Include the following workloads when you install Visual Studio.</span></span>  
        *   <span data-ttu-id="cc7c8-116">.NET Desktop Development \(le programme d’installation installe également .NET 5\)</span><span class="sxs-lookup"><span data-stu-id="cc7c8-116">.NET Desktop Development \(the installer also installs .NET 5\)</span></span>  
        *   <span data-ttu-id="cc7c8-117">Développement de plateforme Windows universelle</span><span class="sxs-lookup"><span data-stu-id="cc7c8-117">Universal Windows Platform development</span></span>  
    *   <span data-ttu-id="cc7c8-118">Pour créer des applications C++, vous devez également inclure les charges de travail suivantes.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-118">To build C++ apps, you must also include the following workloads.</span></span>  
        *   <span data-ttu-id="cc7c8-119">Développement de bureau avec C++</span><span class="sxs-lookup"><span data-stu-id="cc7c8-119">Desktop development with C++</span></span>  
        *   <span data-ttu-id="cc7c8-120">Composant facultatif des outils de plateforme Windows universelle C++ \(v142\) pour la charge de travail de la plateforme Windows universelle.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-120">The C++ \(v142\) Universal Windows Platform tools optional component for the Universal Windows Platform workload.</span></span>  <span data-ttu-id="cc7c8-121">Pour plus d’informations, accédez aux **détails de l’installation** sous la section développement de la plateforme **Windows** universelle, dans le volet droit.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-121">For more information,  navigate to **Installation Details** under the **Universal Windows Platform development** section, on the right pane.</span></span>  
        
## <span data-ttu-id="cc7c8-122">Étape 0 : Visual Studio paramètres</span><span class="sxs-lookup"><span data-stu-id="cc7c8-122">Step 0 - Visual Studio settings</span></span>  

1.  <span data-ttu-id="cc7c8-123">Assurez-vous que votre système dispose d’une source de package NuGet activée pour [nuget.org][NugetHome].  Pour plus d’informations, accédez [aux configurations NuGet communes][NugetConsumePackagesConfiguringNugetBehavior] et à [Windows Community Shared Computer Toolkit][WindowsCommunitytoolkit].</span><span class="sxs-lookup"><span data-stu-id="cc7c8-123">Ensure your system has a NuGet package source enabled for [nuget.org][NugetHome].  For more information, navigate to [Common NuGet configurations][NugetConsumePackagesConfiguringNugetBehavior] and [Windows Community Toolkit][WindowsCommunitytoolkit].</span></span>  
1.  <span data-ttu-id="cc7c8-124">Téléchargez et installez [le package VSIX WinUI 3 Preview 3.][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]</span><span class="sxs-lookup"><span data-stu-id="cc7c8-124">Download and install the [WinUI 3 Preview 3 VSIX package][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates].</span></span>  <span data-ttu-id="cc7c8-125">Le programme d’installation ajoute les modèles de projet WinUI 3 et le package NuGet contenant les bibliothèques WinUI 3 Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-125">The installer adds both the WinUI 3 project templates and the NuGet package containing the WinUI 3 libraries to Visual Studio 2019.</span></span>  
    
    <span data-ttu-id="cc7c8-126">Pour obtenir des instructions sur l’ajout du package à Visual Studio, accédez à Recherche et utilisation `VSIX` [des extensions Visual Studio de recherche.][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox]</span><span class="sxs-lookup"><span data-stu-id="cc7c8-126">For instructions on how to add the `VSIX` package to Visual Studio, navigate to [Finding and Using Visual Studio Extensions][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox].</span></span>
    
1.  <span data-ttu-id="cc7c8-127">Pour accéder à toutes les fonctionnalités spécifiques Visual Studio développeur, activer [le Mode développeur.][WindowsUwpGetStartedEnableYourDeviceForDevelopment]</span><span class="sxs-lookup"><span data-stu-id="cc7c8-127">To access all developer-specific Visual Studio features, turn on [Developer Mode][WindowsUwpGetStartedEnableYourDeviceForDevelopment].</span></span>  
    
## <span data-ttu-id="cc7c8-128">Étape 1 : créer un projet</span><span class="sxs-lookup"><span data-stu-id="cc7c8-128">Step 1 - Create Project</span></span>  

<span data-ttu-id="cc7c8-129">Commencez par un projet de bureau de base qui contient une seule fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-129">Start with a basic desktop project that contains a single main window.</span></span>  

1.  <span data-ttu-id="cc7c8-130">In Visual Studio, choose **Create a new project**.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-130">In Visual Studio, choose **Create a new project**.</span></span>  
1.  <span data-ttu-id="cc7c8-131">Dans la drop-down du projet, choisissez **respectivement C#**, **Windows**et **WinUI.**</span><span class="sxs-lookup"><span data-stu-id="cc7c8-131">In the project drop-down, choose **C#**, **Windows**, and **WinUI** respectively.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Créer un projet WinUI à l’aide Visual Studio" lightbox="./media/winui-gettingstarted-selections.png":::
        <span data-ttu-id="cc7c8-133">Créer un projet WinUI à l’aide Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cc7c8-133">Create a new WinUI project using Visual Studio</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="cc7c8-134">Choose **Blank App, Packaged (WinUI in Desktop)**  >  **Next**.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-134">Choose **Blank App, Packaged (WinUI in Desktop)** > **Next**.</span></span>  
1.  <span data-ttu-id="cc7c8-135">Entrez un nom de projet.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-135">Enter a project name.</span></span>
1.  <span data-ttu-id="cc7c8-136">Choisissez les options selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-136">Choose options as needed.</span></span>  
1.  <span data-ttu-id="cc7c8-137">Choisissez **Créer**.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-137">Choose **Create**.</span></span>  
1.  <span data-ttu-id="cc7c8-138">Dans **le nouveau projet de plateforme Windows**universelle, choisissez les valeurs suivantes, puis choisissez **OK.**</span><span class="sxs-lookup"><span data-stu-id="cc7c8-138">In **New Universal Windows Platform Project**, choose the following values, and then choose **OK**.</span></span>  
    *   <span data-ttu-id="cc7c8-139">**Version cible**:  **Windows 10, version 1903 (build 18362)** ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="cc7c8-139">**Target version**:  **Windows 10, version 1903 (build 18362)** or later</span></span>  
    *   <span data-ttu-id="cc7c8-140">**Version minimale**:  **Windows 10, version 1803 (build 17134)**</span><span class="sxs-lookup"><span data-stu-id="cc7c8-140">**Minimum version**:  **Windows 10, version 1803 (build 17134)**</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="Boîte de dialogue Nouveau projet de plateforme Windows universelle avec les valeurs choisies pour la version cible et la version minimale." lightbox="./media/winui-gettingstarted-projecttype.png":::
       <span data-ttu-id="cc7c8-142">Boîte de dialogue Nouveau projet de plateforme Windows universelle avec les valeurs choisies pour la version cible et la version minimale.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-142">The New Universal Windows Platform Project dialog with chosen values for Target version and Minimum version.</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="cc7c8-143">Dans l’Explorateur de solutions, deux projets sont générés.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-143">In the Solution Explorer, two projects are generated.</span></span>  
    *   <span data-ttu-id="cc7c8-144">**Nom de votre projet (Bureau)**.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-144">**Your project name (Desktop)**.</span></span>  <span data-ttu-id="cc7c8-145">Le projet Bureau contient le code de votre application.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-145">The Desktop project contains the code for your app.</span></span>  <span data-ttu-id="cc7c8-146">Le `App.xaml.cs` fichier définit une classe qui représente `Application` l’instance de votre application.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-146">The `App.xaml.cs` file defines an `Application` class that represents your app instance.</span></span>  <span data-ttu-id="cc7c8-147">Le `MainWindow.xaml.cs` fichier définit une classe qui représente la fenêtre principale affichée par `MainWindow` l’instance de votre application.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-147">The `MainWindow.xaml.cs` file defines a `MainWindow` class that represents the main window displayed by your app instance.</span></span>  <span data-ttu-id="cc7c8-148">Les classes dérivent des types de `Microsoft.UI.Xaml` l’espace de noms WinUI.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-148">The classes derive from types in the `Microsoft.UI.Xaml` namespace of WinUI.</span></span>  
    *   <span data-ttu-id="cc7c8-149">**Nom de votre projet (package).**</span><span class="sxs-lookup"><span data-stu-id="cc7c8-149">**Your project name (Package)**.</span></span>  <span data-ttu-id="cc7c8-150">Le projet package est un projet d’empaquetage d’application Windows qui est configuré pour créer l’application dans un package MSIX pour le déploiement.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-150">The Package project is a Windows Application Packaging Project that is configured to build the app into an MSIX package for deployment.</span></span>  <span data-ttu-id="cc7c8-151">Le projet contient le manifeste du package de votre application et est le projet de démarrage de votre solution par défaut.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-151">The project contains the package manifest for your app, and is the startup project for your solution by default.</span></span>  <span data-ttu-id="cc7c8-152">Pour plus d’informations, accédez à Configurer votre application de bureau pour la mise en package [MSIX][WindowsMsixDesktopToUwpPackagingDotNet] dans Visual Studio et référence du schéma de manifeste de package [pour Windows 10.][UwpSchemasAppxpackageUapmanifestRoot]</span><span class="sxs-lookup"><span data-stu-id="cc7c8-152">For more information, navigate to [Set up your desktop application for MSIX packaging in Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] and [Package manifest schema reference for Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span></span>  
1.  <span data-ttu-id="cc7c8-153">Dans l’Explorateur de solutions, pour afficher le code, ouvrez le `MainWindow.xaml` fichier.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-153">In the Solution Explorer, to display the code, open the `MainWindow.xaml` file.</span></span>  <span data-ttu-id="cc7c8-154">Pour exécuter votre projet et afficher une fenêtre avec un bouton, sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="cc7c8-154">To run your project and display a window with a button, select `F5`.</span></span>  
    
## <span data-ttu-id="cc7c8-155">Étape 2 : ajouter un contrôle WebView2 à votre projet</span><span class="sxs-lookup"><span data-stu-id="cc7c8-155">Step 2 - Add a WebView2 control to your project</span></span>  

<span data-ttu-id="cc7c8-156">Ajoutez un contrôle WebView2 à votre projet.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-156">Add a WebView2 control to your project.</span></span>  

1.  <span data-ttu-id="cc7c8-157">Dans le fichier, pour ajouter l’espace de noms `MainWindow.xaml` XAML WebView2, insérez la ligne suivante à l’intérieur de la `<Window/>` balise.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-157">In the `MainWindow.xaml` file, to add the WebView2 XAML namespace, insert the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    <span data-ttu-id="cc7c8-158">Assurez-vous que votre code `MainWindow.xaml` est similaire à l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-158">Ensure your code in `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="cc7c8-159">Pour ajouter le contrôle WebView2, remplacez les balises par l’extrait de `<StackPanel>` code suivant.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-159">To add the WebView2 control, replace the `<StackPanel>` tags with the following code snippet.</span></span>  <span data-ttu-id="cc7c8-160">La `Source` propriété définit l’URI initial affiché dans le contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-160">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
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
    
1.  <span data-ttu-id="cc7c8-161">Dans le `MainWindow.xaml.cs` fichier, commentez la ligne suivante.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-161">In the `MainWindow.xaml.cs` file, comment out the following line.</span></span>
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  <span data-ttu-id="cc7c8-162">Pour créer et exécuter votre projet, sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="cc7c8-162">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="cc7c8-163">Assurez-vous que votre contrôle WebView2 [https://www.microsoft.com][|::ref1::|Main] s’affiche.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-163">Ensure your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="Le contrôle WebView2 affiche les microsoft.com" lightbox="./media/winui-gettingstarted-part3.png":::
       <span data-ttu-id="cc7c8-165">Le contrôle WebView2 affiche les microsoft.com</span><span class="sxs-lookup"><span data-stu-id="cc7c8-165">WebView2 control displays microsoft.com</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="cc7c8-166">Étape 3 : ajouter des contrôles de navigation</span><span class="sxs-lookup"><span data-stu-id="cc7c8-166">Step 3 - Add navigation controls</span></span>  

<span data-ttu-id="cc7c8-167">Pour permettre aux utilisateurs de contrôler la page web qui s’affiche dans votre contrôle WebView2, ajoutez une barre d’adresse à votre application.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-167">To allow users to control the webpage that is displayed in your WebView2 control, add an address bar to your app.</span></span>  

1.  <span data-ttu-id="cc7c8-168">Dans le fichier, copiez et collez l’extrait de code suivant à l’intérieur de `MainWindow.xaml` `<Grid>` l’élément qui contient `WebView2` l’élément.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-168">In the `MainWindow.xaml` file, copy and paste the following code snippet inside the `<Grid>` element that contains the `WebView2` element.</span></span>  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    <span data-ttu-id="cc7c8-169">`<Grid>`Assurez-vous que votre élément dans le fichier est similaire à `MainWindow.xaml` l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-169">Ensure your `<Grid>` element in the `MainWindow.xaml` file is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="cc7c8-170">Dans le fichier, copiez l’extrait de code suivant dans , qui navigue le contrôle WebView2 vers l’URL entrée `MainWindow.xaml.cs` `myButton_Click` dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-170">In the `MainWindow.xaml.cs` file, copy the following code snippet into `myButton_Click`, which navigates the WebView2 control to the URL entered in the address bar.</span></span>  
    
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
    
    <span data-ttu-id="cc7c8-171">Pour créer et exécuter votre projet, sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="cc7c8-171">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="cc7c8-172">Entrez une nouvelle URL dans la barre d’adresses, puis choisissez **Go**.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-172">Enter a new URL in the address bar, and then choose **Go**.</span></span>  <span data-ttu-id="cc7c8-173">Par exemple, entrez `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="cc7c8-173">For example, enter `https://www.bing.com`.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="cc7c8-174">Veillez à entrer les URL complètes dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-174">Ensure you enter complete URLs in the address bar.</span></span>  `ArgumentException` <span data-ttu-id="cc7c8-175">des exceptions sont lancées si l’URL ne commence pas par `http://` ou `https://` .</span><span class="sxs-lookup"><span data-stu-id="cc7c8-175">exceptions are thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="bing.com" lightbox="./media/winui-gettingstarted-bing.png":::
       <span data-ttu-id="cc7c8-177">bing.com</span><span class="sxs-lookup"><span data-stu-id="cc7c8-177">bing.com</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="cc7c8-178">Étape 4 : événements de navigation</span><span class="sxs-lookup"><span data-stu-id="cc7c8-178">Step 4 - Navigation events</span></span>  

<span data-ttu-id="cc7c8-179">Les applications qui hébergent des contrôles WebView2 écoutent les événements suivants qui sont élevés par les contrôles WebView2 lors de la navigation dans la page web.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-179">Apps that host WebView2 controls listen for the following events that are raised by WebView2 controls during webpage navigation.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

> [!NOTE]
> <span data-ttu-id="cc7c8-180">Si une redirection HTTP se produit, il existe plusieurs `NavigationStarting` événements dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-180">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="cc7c8-181">Pour plus d’informations, accédez à [Événements de navigation.][Webviews2ConceptsNavigationEvents]</span><span class="sxs-lookup"><span data-stu-id="cc7c8-181">For more information, navigate to [Navigation Events][Webviews2ConceptsNavigationEvents].</span></span>  

<span data-ttu-id="cc7c8-182">Lorsque des erreurs se produisent, les événements suivants sont élevés et peuvent accéder à une page web d’erreur.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-182">When errors occur, the following events are raised and may navigate to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
     
<span data-ttu-id="cc7c8-183">À titre d’exemple d’utilisation des événements, inscrivez un responsable pour annuler toutes les demandes `NavigationStarting` non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-183">As an example of how to use the events, register a handler for `NavigationStarting` that cancels any non-HTTPS requests.</span></span>  <span data-ttu-id="cc7c8-184">Dans , modifiez le constructeur pour l’inscrire et ajoutez la fonction afin qu’elle corresponde à l’extrait de `MainWindow.xaml.cs` `EnsureHttps` code `EnsureHttps` suivant.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-184">In `MainWindow.xaml.cs`, modify the constructor to register `EnsureHttps`, and add the `EnsureHttps` function so that it matches the following code snippet.</span></span>  

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

<span data-ttu-id="cc7c8-185">Pour créer et exécuter votre projet, sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="cc7c8-185">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="cc7c8-186">Assurez-vous que la navigation est bloquée sur les sites HTTP et autorisée pour les sites HTTPS.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-186">Ensure navigation is blocked to HTTP sites, and allowed for HTTPS sites.</span></span>  

## <span data-ttu-id="cc7c8-187">Étape 5 : scripts</span><span class="sxs-lookup"><span data-stu-id="cc7c8-187">Step 5 - Scripting</span></span>  

<span data-ttu-id="cc7c8-188">Vous pouvez utiliser des applications hôtes pour injecter du code JavaScript dans des contrôles WebView2 lors de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-188">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="cc7c8-189">Vous pouvez tâcher WebView pour exécuter du javaScript arbitraire ou ajouter des scripts d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-189">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="cc7c8-190">Le javaScript injecté s’applique à tous les nouveaux documents de niveau supérieur et aux images enfants jusqu’à ce que le JavaScript soit supprimé.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-190">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="cc7c8-191">Le javaScript injecté est exécuté avec un minutage spécifique.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-191">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="cc7c8-192">Exécutez-le après la création de l’objet global.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-192">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="cc7c8-193">Exécutez-le avant tout autre script inclus dans le document HTML.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-193">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="cc7c8-194">Par exemple, ajoutez des scripts qui envoient une alerte lorsqu’un utilisateur navigue vers des sites non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-194">As an example, add scripts that send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="cc7c8-195">Modifiez la fonction pour injecter un script dans le contenu web qui `EnsureHttps` utilise [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].</span><span class="sxs-lookup"><span data-stu-id="cc7c8-195">Modify the `EnsureHttps` function to inject a script into the web content that uses [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].</span></span>  

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

<span data-ttu-id="cc7c8-196">Pour créer et exécuter votre projet, sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="cc7c8-196">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="cc7c8-197">Assurez-vous que votre application affiche une alerte lorsque vous accédez à des sites web non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-197">Ensure your app displays an alert when you navigate to any non-HTTPS websites.</span></span>  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="Le contrôle WebView2 affiche une boîte de dialogue d’alerte" lightbox="./media/winui-gettingstarted-script.png":::
   <span data-ttu-id="cc7c8-199">Le contrôle WebView2 affiche une boîte de dialogue d’alerte</span><span class="sxs-lookup"><span data-stu-id="cc7c8-199">WebView2 control displays an alert dialog</span></span>
:::image-end:::  

<span data-ttu-id="cc7c8-200">Félicitations, vous avez créé votre première application WebView2.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-200">Congratulations, you built your first WebView2 app.</span></span>  

## <span data-ttu-id="cc7c8-201">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="cc7c8-201">Next steps</span></span>  

<span data-ttu-id="cc7c8-202">Pour en savoir plus sur WebView2, accédez aux ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-202">To continue learning more about WebView2, navigate to the following resources.</span></span>  

### <span data-ttu-id="cc7c8-203">Voir également</span><span class="sxs-lookup"><span data-stu-id="cc7c8-203">See also</span></span>  

*   <span data-ttu-id="cc7c8-204">Pour obtenir un exemple complet des fonctionnalités WebView2, accédez [à WebView2Samples.][GithubMicrosoftedgeWebview2samplesMain]</span><span class="sxs-lookup"><span data-stu-id="cc7c8-204">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].</span></span>  
*   <span data-ttu-id="cc7c8-205">Pour plus d’informations sur WebView2, accédez [à Ressources WebView2.][Webview2IndexNextSteps]</span><span class="sxs-lookup"><span data-stu-id="cc7c8-205">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="cc7c8-206">L’objet WinRT CoreWebView2 n’est peut-être pas disponible avec la version de l’API WebView2.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-206">The WinRT CoreWebView2 object may not be available with the release of the WebView2 API.</span></span>  <span data-ttu-id="cc7c8-207">Pour comprendre quelles API sont disponibles pour les contrôles WebView2, accédez à [WebView2 Spec][GithubMicrosoftUiXamlSpecsWebview2] pour obtenir la liste des API disponibles.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-207">To understand which APIs are available to WebView2 controls, navigate to [WebView2 Spec][GithubMicrosoftUiXamlSpecsWebview2] for a list of the APIs that are available.</span></span>  
    
*   <span data-ttu-id="cc7c8-208">Pour plus d’informations sur l’API WebView2, accédez aux spécifications [WebView2.][GithubMicrosoftUiXamlSpecsWebview2]</span><span class="sxs-lookup"><span data-stu-id="cc7c8-208">For detailed information about the WebView2 API, navigate to [WebView2 spec][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  
    
## <span data-ttu-id="cc7c8-209">Entrer en contact avec l’équipe Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="cc7c8-209">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: ../index.md "Présentation de Microsoft Edge WebView2 (prévisualisation) | Documents Microsoft"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Étapes suivantes : présentation de Microsoft Edge WebView2 (prévisualisation) | Documents Microsoft"  
[Webviews2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Événements de navigation | Documents Microsoft"  
[Webviews2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.Exeméthode cuteScriptAsync(String) (Microsoft.Web.WebView2.Wpf) | Documents Microsoft"  

[NugetConsumePackagesConfiguringNugetBehavior]: /nuget/consume-packages/configuring-nuget-behavior "Configurations NuGet courantes | Documents Microsoft"  

[UwpSchemasAppxpackageUapmanifestRoot]: /uwp/schemas/appxpackage/uapmanifestschema/schema-root "Référence du schéma de manifeste de package pour Windows 10 | Documents Microsoft"  

[VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox]: /visualstudio/ide/finding-and-using-visual-studio-extensions#install-without-using-the-manage-extensions-dialog-box "Installer sans utiliser la boîte de dialogue Gérer les extensions : gérer les extensions pour Visual Studio | Documents Microsoft"  

[WindowsAppsWinui3ConfigureYourDevEnvironment]: /windows/apps/winui/winui3#configure-your-dev-environment "Configurer votre environnement dev - Bibliothèque d’interface utilisateur Windows 3.0 Preview 1 (mai 2020) | Documents Microsoft"  
[WindowsCommunitytoolkit]: /windows/communitytoolkit "Documentation de Shared Computer Toolkit communauté Windows | Documents Microsoft"  
[WindowsMsixDesktopToUwpPackagingDotNet]: /windows/msix/desktop/desktop-to-uwp-packaging-dot-net "Configurer votre application de bureau pour l’empaquetage MSIX dans Visual Studio | Documents Microsoft"  
[WindowsUwpGetStartedEnableYourDeviceForDevelopment]: /windows/uwp/get-started/enable-your-device-for-development "Activer votre appareil pour le développement | Documents Microsoft"  

[GithubMicrosoftUiXamlSpecsWebview2]: https://github.com/microsoft/microsoft-ui-xaml-specs/blob/master/active/WebView2/WebView2_spec.md "Spécifications WebView2 : microsoft/microsoft-ui-xaml-specs | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires WebView - MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftSupport12373]: https://support.microsoft.com/help/12373 "Windows Update : FAQ"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  

[NugetHome]: https://nuget.org "Accueil | NuGet Gallery"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X86]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe "Télécharger dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X64]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe " dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe"  

[VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]: https://marketplace.visualstudio.com/items?itemName=Microsoft-WinUI.WinUIProjectTemplates "Modèles de projet WinUI 3 | Visual Studio Marketplace"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Programme d’installation WebView2" 
