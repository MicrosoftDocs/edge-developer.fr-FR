---
description: Guide de mise en route de WebView2 pour les applications WPF
title: Mise en route de WebView2 pour les applications WPF
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, applications WPF, WPF, Edge, CoreWebView2, contrôle de navigateur, html Edge, mise en route, mise en route, .NET
ms.openlocfilehash: e928dae0aa63f15ca5fa21860c83fa5529e905df
ms.sourcegitcommit: fab44f7e183a3c4f12bf925512fc62d84a4d6edc
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182373"
---
# <span data-ttu-id="10d96-104">Commencer à utiliser WebView2 dans WPF</span><span class="sxs-lookup"><span data-stu-id="10d96-104">Getting started with WebView2 in WPF</span></span>

<span data-ttu-id="10d96-105">Dans cet article, vous allez commencer à créer votre première application WebView2 et à découvrir les principales fonctionnalités de [WebView2](../index.md).</span><span class="sxs-lookup"><span data-stu-id="10d96-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2](../index.md).</span></span>  <span data-ttu-id="10d96-106">Pour plus d’informations sur les API individuelles, voir informations de référence sur les [API](/dotnet/api/microsoft.web.webview2.wpf).</span><span class="sxs-lookup"><span data-stu-id="10d96-106">For more information on individual APIs, see [API reference](/dotnet/api/microsoft.web.webview2.wpf).</span></span>  

## <span data-ttu-id="10d96-107">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="10d96-107">Prerequisites</span></span>  

<span data-ttu-id="10d96-108">Vérifiez que vous avez installé la liste des conditions préalables suivantes avant de continuer:</span><span class="sxs-lookup"><span data-stu-id="10d96-108">Ensure you installed the following list of pre-requisites before proceeding:</span></span>  

* <span data-ttu-id="10d96-109">[WebView2 Runtime][Webview2Installer] ou un canal de l’alphabet [Microsoft Edge (chrome) non stable](https://www.microsoftedgeinsider.com/download) installé sur windows 10, Windows 8,1 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="10d96-109">[WebView2 Runtime][Webview2Installer] or any [non-stable Microsoft Edge (Chromium) Canary channel](https://www.microsoftedgeinsider.com/download) installed on Windows 10, Windows 8.1, or Windows 7.</span></span>  
* <span data-ttu-id="10d96-110">[Visual Studio](https://visualstudio.microsoft.com) 2017 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="10d96-110">[Visual Studio](https://visualstudio.microsoft.com) 2017 or later.</span></span>  

## <span data-ttu-id="10d96-111">Étape 1: créer une application de fenêtre unique</span><span class="sxs-lookup"><span data-stu-id="10d96-111">Step 1 - Create a single window application</span></span>  

<span data-ttu-id="10d96-112">Utiliser un projet de bureau de base contenant une seule fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="10d96-112">Start with a basic desktop project containing a single main window.</span></span>  

1.  <span data-ttu-id="10d96-113">Ouvrez **Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="10d96-113">Open **Visual Studio**.</span></span>  
1.  <span data-ttu-id="10d96-114">Sélectionnez application **WPF .net Core** ou **application WPF .NET Framework**, puis sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="10d96-114">Select **WPF .NET Core App** or **WPF .NET Framework App**, and then select **Next**.</span></span>  
    
    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpfcore.png" alt-text="Noyau WPF":::
             <span data-ttu-id="10d96-116">Noyau WPF</span><span class="sxs-lookup"><span data-stu-id="10d96-116">WPF core</span></span> :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpffw.png" alt-text="Infrastructure WPF":::
             <span data-ttu-id="10d96-118">Infrastructure WPF</span><span class="sxs-lookup"><span data-stu-id="10d96-118">WPF Framework</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="10d96-119">Entrez des valeurs pour le nom et l' **emplacement**du **projet** .</span><span class="sxs-lookup"><span data-stu-id="10d96-119">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="10d96-120">Sélectionnez .NET Framework 4.6.2 ou version ultérieure, ou .NET Core 3,0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="10d96-120">Select .NET Framework 4.6.2 or later, or .NET Core 3.0 or later.</span></span>  
    
    :::row:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createcore.png" alt-text="Créer un cœur":::
                 <span data-ttu-id="10d96-122">Créer un cœur</span><span class="sxs-lookup"><span data-stu-id="10d96-122">Create core</span></span> :::image-end:::
           :::column-end:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createfw.png" alt-text="Créer une infrastructure":::
                 <span data-ttu-id="10d96-124">Créer une infrastructure</span><span class="sxs-lookup"><span data-stu-id="10d96-124">Create Framework</span></span> :::image-end:::
           :::column-end:::
        :::row-end:::
    
1.  <span data-ttu-id="10d96-125">Sélectionnez **créer** pour créer votre projet.</span><span class="sxs-lookup"><span data-stu-id="10d96-125">Select **Create** to create your project.</span></span>  
    
## <span data-ttu-id="10d96-126">Étape 2: installer le SDK WebView2</span><span class="sxs-lookup"><span data-stu-id="10d96-126">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="10d96-127">Ensuite, ajoutez le kit de développement logiciel (SDK) WebView2 au projet en utilisant NuGet.</span><span class="sxs-lookup"><span data-stu-id="10d96-127">Next add the WebView2 SDK to the project using NuGet.</span></span>  

1.  <span data-ttu-id="10d96-128">Ouvrez le menu contextuel du projet \ (cliquez avec le bouton droit sur \), puis sélectionnez **gérer les packages NuGet...**.</span><span class="sxs-lookup"><span data-stu-id="10d96-128">Open the context menu on the project \(right-click\), and select **Manage NuGet Packages...**.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="NuGet":::
       <span data-ttu-id="10d96-130">NuGet</span><span class="sxs-lookup"><span data-stu-id="10d96-130">NuGet</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="10d96-131">Entrez `Microsoft.Web.WebView2` dans la barre de recherche.</span><span class="sxs-lookup"><span data-stu-id="10d96-131">Enter `Microsoft.Web.WebView2` in the search bar.</span></span>  <span data-ttu-id="10d96-132">Sélectionnez **Microsoft. Web. WebView2** dans les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="10d96-132">Select **Microsoft.Web.WebView2** from the search results.</span></span>  
   
     ![NuGet](./media/installnuget.PNG)
    
    <span data-ttu-id="10d96-134">Pour commencer à développer des applications à l’aide de l’API WebView2, vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="10d96-134">You're all set to start developing applications using the WebView2 API.</span></span>  <span data-ttu-id="10d96-135">Sélectionnez `F5` pour générer et exécuter le projet.</span><span class="sxs-lookup"><span data-stu-id="10d96-135">Select `F5` to build and run the project.</span></span>  <span data-ttu-id="10d96-136">Le projet en cours d’exécution affiche une fenêtre vide.</span><span class="sxs-lookup"><span data-stu-id="10d96-136">The running project displays an empty window.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-blank.png" alt-text="Application vide":::
       <span data-ttu-id="10d96-138">Application vide</span><span class="sxs-lookup"><span data-stu-id="10d96-138">Empty app</span></span>
    :::image-end:::  
    
## <span data-ttu-id="10d96-139">Étape 3: créer un WebView unique dans MainWindow. Xaml</span><span class="sxs-lookup"><span data-stu-id="10d96-139">Step 3 - Create a single WebView in MainWindow.xaml</span></span>  

<span data-ttu-id="10d96-140">Ensuite, ajoutez un WebView à votre application.</span><span class="sxs-lookup"><span data-stu-id="10d96-140">Next add a WebView to your application.</span></span>  

1.  <span data-ttu-id="10d96-141">Ouvrir `MainWindow.xaml` .</span><span class="sxs-lookup"><span data-stu-id="10d96-141">Open `MainWindow.xaml`.</span></span>  <span data-ttu-id="10d96-142">Ajoutez l’espace de noms XAML WebView2 en insérant la ligne suivante dans la `<Window/>` balise.</span><span class="sxs-lookup"><span data-stu-id="10d96-142">Add the WebView2 XAML namespace by inserting the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  
    
    <span data-ttu-id="10d96-143">Vérifiez que le code `MainWindow.xaml` ressemble à l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="10d96-143">Confirm that the code in `MainWindow.xaml` looks like the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="10d96-144">Ajoutez le contrôle WebView2 en remplaçant les `<Grid>` balises par l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="10d96-144">Add the WebView2 control by replacing the `<Grid>` tags, with the following code snippet.</span></span>  <span data-ttu-id="10d96-145">La `Source` propriété définit l’URI initial affiché dans le contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="10d96-145">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
    ```xml  
    <DockPanel>
        <wv2:WebView2 Name="webView"
                      Source="https://www.microsoft.com"
        />
    </DockPanel>
    ```  
    
1.  <span data-ttu-id="10d96-146">Appuyez `F5` pour générer et exécuter votre projet.</span><span class="sxs-lookup"><span data-stu-id="10d96-146">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="10d96-147">Vérifiez que votre contrôle WebView2 s’affiche [https://www.microsoft.com](https://www.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="10d96-147">Confirm that your WebView2 control displays [https://www.microsoft.com](https://www.microsoft.com).</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-microsoft.png" alt-text="Microsoft.com":::
       <span data-ttu-id="10d96-149">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="10d96-149">Microsoft.com</span></span>
    :::image-end:::  
    
## <span data-ttu-id="10d96-150">Étape 4: navigation</span><span class="sxs-lookup"><span data-stu-id="10d96-150">Step 4 - Navigation</span></span>  

<span data-ttu-id="10d96-151">Ajoutez la possibilité d’autoriser les utilisateurs à modifier l’URL d’affichage du contrôle WebView2 en ajoutant une barre d’adresse à l’application.</span><span class="sxs-lookup"><span data-stu-id="10d96-151">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1.  <span data-ttu-id="10d96-152">Dans **MainWindow. Xaml**, ajoutez une barre d’adresse en copiant et en collant l’extrait de code suivant à l’intérieur du DockPanel qui contient le WebView.</span><span class="sxs-lookup"><span data-stu-id="10d96-152">In **MainWindow.xaml**, add an address bar by copying and pasting the following code snippet inside the DockPanel that contains the WebView.</span></span>  
    
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
    
    <span data-ttu-id="10d96-153">Vérifiez que la `DockPanel` section de l' `MainWindow.xaml` extrait de code suivant ressemble à ceci.</span><span class="sxs-lookup"><span data-stu-id="10d96-153">Confirm that the `DockPanel` section of `MainWindow.xaml` looks like the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="10d96-154">Ouvrir `MainWindow.xaml.cs` dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="10d96-154">Open `MainWindow.xaml.cs` in Visual Studio.</span></span>  <span data-ttu-id="10d96-155">Ajoutez l' `CoreWebView2` espace de noms en insérant l’extrait de code suivant en haut de `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="10d96-155">Add the `CoreWebView2` namespace by inserting the following code snippet at the top of `MainWindow.xaml.cs`.</span></span>  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```
    
1.  <span data-ttu-id="10d96-156">Dans **MainWindow.Xaml.cs**, copiez l’extrait de code suivant afin de créer la `ButtonGo_Click` méthode, qui permet d’accéder à l’URL entrée dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="10d96-156">In **MainWindow.xaml.cs**, copy the following code snippet to create the `ButtonGo_Click` method, which navigates the WebView to the URL entered in the address bar.</span></span>  
    
    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  
    
    <span data-ttu-id="10d96-157">Appuyez `F5` pour générer et exécuter votre projet.</span><span class="sxs-lookup"><span data-stu-id="10d96-157">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="10d96-158">Entrez une nouvelle URL dans la barre d’adresses, puis sélectionnez **atteindre**.</span><span class="sxs-lookup"><span data-stu-id="10d96-158">Enter a new URL in the address bar, and select **Go**.</span></span>  <span data-ttu-id="10d96-159">Par exemple, entrez `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="10d96-159">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="10d96-160">Vérifiez que le contrôle WebView2 accède à l’URL.</span><span class="sxs-lookup"><span data-stu-id="10d96-160">Confirm that the WebView2 control navigates to the URL.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="10d96-161">Vérifiez qu’une URL complète est entrée dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="10d96-161">Make sure a complete URL is entered in the address bar.</span></span>  <span data-ttu-id="10d96-162">`ArgumentException`A est levé si l’URL ne commence pas par `http://` ou `https://` .</span><span class="sxs-lookup"><span data-stu-id="10d96-162">An `ArgumentException` is thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-bing.png" alt-text="Bing":::
       <span data-ttu-id="10d96-164">Bing</span><span class="sxs-lookup"><span data-stu-id="10d96-164">Bing</span></span>
    :::image-end:::
    
## <span data-ttu-id="10d96-165">Étape 5: événements de navigation</span><span class="sxs-lookup"><span data-stu-id="10d96-165">Step 5 - Navigation events</span></span>  

<span data-ttu-id="10d96-166">Lors de la navigation de la page Web, le contrôle WebView2 déclenche des événements.</span><span class="sxs-lookup"><span data-stu-id="10d96-166">During webpage navigation, the WebView2 control raises events.</span></span> <span data-ttu-id="10d96-167">L’application qui héberge les contrôles WebView2 écoute les événements suivants.</span><span class="sxs-lookup"><span data-stu-id="10d96-167">The application that hosts WebView2 controls listens for the following events.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

<span data-ttu-id="10d96-168">Pour plus d’informations, voir [événements de navigation](../concepts/navigation-events.md).</span><span class="sxs-lookup"><span data-stu-id="10d96-168">For more information, see [Navigation Events](../concepts/navigation-events.md).</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Événements de navigation":::
   <span data-ttu-id="10d96-170">Événements de navigation</span><span class="sxs-lookup"><span data-stu-id="10d96-170">Navigation events</span></span>
:::image-end:::  

<span data-ttu-id="10d96-171">Lorsqu’une erreur se produit, les événements suivants sont déclenchés et peut dépendre de la navigation sur une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="10d96-171">When an error occurs, the following events are raised and may depend on navigation to an error page.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

<span data-ttu-id="10d96-172">Lorsqu’il existe une redirection HTTP, il existe plusieurs `NavigationStarting` événements.</span><span class="sxs-lookup"><span data-stu-id="10d96-172">When there's an HTTP redirect, there are multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="10d96-173">Pour illustrer l’utilisation de ces événements, commencez par enregistrer un gestionnaire pour `NavigationStarting` Annuler toutes les demandes qui n’utilisent pas HTTPS.</span><span class="sxs-lookup"><span data-stu-id="10d96-173">To demonstrate how to use these events, start by registering a handler for `NavigationStarting` that cancels any requests that don't use HTTPS.</span></span>  

<span data-ttu-id="10d96-174">Dans `MainWindow.xaml.cs` , modifiez le constructeur comme illustré ci-dessous, puis ajoutez la `EnsureHttps` fonction.</span><span class="sxs-lookup"><span data-stu-id="10d96-174">In `MainWindow.xaml.cs`, modify the constructor as shown below and add the `EnsureHttps` function.</span></span>  

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

<span data-ttu-id="10d96-175">Dans le constructeur, EnsureHttps est enregistré en tant que gestionnaire d’événements sur l' `NavigationStarting` événement sur le contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="10d96-175">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="10d96-176">Appuyez `F5` pour générer et exécuter votre projet.</span><span class="sxs-lookup"><span data-stu-id="10d96-176">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="10d96-177">Confirmez que lorsque vous naviguez vers un site HTTP, le WebView **reste inchangé**.</span><span class="sxs-lookup"><span data-stu-id="10d96-177">Confirm that when navigating to an HTTP site, the WebView **remains unchanged**.</span></span>  <span data-ttu-id="10d96-178">Toutefois, le WebView navigue vers les sites HTTPs.</span><span class="sxs-lookup"><span data-stu-id="10d96-178">However, the WebView navigates to HTTPS sites.</span></span>  

## <span data-ttu-id="10d96-179">Étape 6: création de scripts</span><span class="sxs-lookup"><span data-stu-id="10d96-179">Step 6 - Scripting</span></span>  

<span data-ttu-id="10d96-180">Vous pouvez utiliser des applications hôtes pour injecter du code JavaScript dans les contrôles WebView2 lors de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="10d96-180">You may use host applications to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="10d96-181">Le JavaScript injecté s’applique à tous les nouveaux documents de niveau supérieur ainsi qu’à toute image enfant, jusqu’à ce que le JavaScript soit supprimé.</span><span class="sxs-lookup"><span data-stu-id="10d96-181">The injected JavaScript applies to all new top-level documents and any child frames, until the JavaScript is removed.</span></span>  <span data-ttu-id="10d96-182">Le JavaScript injecté est exécuté après la création de l’objet global et avant les scripts inclus dans le document HTML.</span><span class="sxs-lookup"><span data-stu-id="10d96-182">The injected JavaScript is run after creation of the global object, and before any scripts included in the HTML document.</span></span>  

<span data-ttu-id="10d96-183">Vous pouvez utiliser les scripts pour alerter l’utilisateur lorsque vous naviguez vers un site non HTTPs.</span><span class="sxs-lookup"><span data-stu-id="10d96-183">You can use scripting to alert the user when navigating to a non-HTTPS site.</span></span>  <span data-ttu-id="10d96-184">Modifiez la `EnsureHttps` fonction de telle sorte qu’elle injecte le script dans le contenu Web à l’aide de la méthode [ExecuteScriptAsync](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync) .</span><span class="sxs-lookup"><span data-stu-id="10d96-184">Modify the `EnsureHttps` function so that it injects script into the web content using the [ExecuteScriptAsync](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync) method.</span></span>  

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

<span data-ttu-id="10d96-185">Appuyez `F5` pour générer et exécuter votre projet.</span><span class="sxs-lookup"><span data-stu-id="10d96-185">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="10d96-186">Vérifiez que l’application affiche une alerte lorsque vous naviguez vers un site qui n’utilise pas HTTPs.</span><span class="sxs-lookup"><span data-stu-id="10d96-186">Confirm that the application displays an alert when you navigate to a site that doesn't use HTTPS.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-https.png" alt-text="HTTPS":::
   <span data-ttu-id="10d96-188">HTTPS</span><span class="sxs-lookup"><span data-stu-id="10d96-188">HTTPS</span></span>
:::image-end:::  

## <span data-ttu-id="10d96-189">Étape 7: communication entre l’hôte et le contenu Web</span><span class="sxs-lookup"><span data-stu-id="10d96-189">Step 7 - Communication between host and web content</span></span>  

<span data-ttu-id="10d96-190">L’hôte et le contenu Web sont en mesure de communiquer entre eux `postMessage` comme suit:</span><span class="sxs-lookup"><span data-stu-id="10d96-190">The host and web content may communicate with each other using `postMessage` as follows:</span></span>  

*   <span data-ttu-id="10d96-191">Le contenu Web d’un contrôle WebView2 risque de publier un message destiné à l’hôte à l’aide de `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="10d96-191">Web content in a WebView2 control may post a message to the host using `window.chrome.webview.postMessage`.</span></span>  <span data-ttu-id="10d96-192">L’hôte gère le message en utilisant tout inscrit `WebMessageReceived` sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="10d96-192">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
*   <span data-ttu-id="10d96-193">Héberge les messages dans le contenu Web d’un contrôle WebView2 en utilisant `CoreWebView2.PostWebMessageAsString` ou `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="10d96-193">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="10d96-194">Ces messages sont interceptés par des gestionnaires ajoutés à `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="10d96-194">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="10d96-195">Ce mécanisme de communication permet au contenu Web de transmettre des messages à l’hôte à l’aide de fonctionnalités natives.</span><span class="sxs-lookup"><span data-stu-id="10d96-195">This communication mechanism allows web content to pass messages to the host using native capabilities.</span></span>  

<span data-ttu-id="10d96-196">Dans votre projet, lorsque le contrôle WebView2 navigue vers une URL, il affiche l’URL dans la barre d’adresse et avertit l’utilisateur de l’URL qui s’affiche dans le contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="10d96-196">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1.  <span data-ttu-id="10d96-197">Dans **MainWindow.Xaml.cs**, mettez à jour votre constructeur et créez une `InitializeAsync` fonction comme illustré dans l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="10d96-197">In **MainWindow.xaml.cs**, update your constructor and create an `InitializeAsync` function as shown in the following code snippet.</span></span>  <span data-ttu-id="10d96-198">La `InitializeAsync` fonction est en attente [EnsureCoreWebView2Async](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) , car l’initialisation de `CoreWebView2` est asynchrone.</span><span class="sxs-lookup"><span data-stu-id="10d96-198">The `InitializeAsync` function awaits [EnsureCoreWebView2Async](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) because the initialization of `CoreWebView2` is asynchronous.</span></span>  
    
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
    
1.  <span data-ttu-id="10d96-199">Une fois **CoreWebView2** initialisé, inscrivez un gestionnaire d’événements pour y répondre `WebMessageReceived` .</span><span class="sxs-lookup"><span data-stu-id="10d96-199">After **CoreWebView2** is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="10d96-200">Dans **MainWindow.Xaml.cs**, mettez à jour `InitializeAsync` et ajoutez à `UpdateAddressBar` l’aide de l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="10d96-200">In **MainWindow.xaml.cs**, update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="10d96-201">Pour que le WebView envoie un message électronique et y réponde, une fois l' `CoreWebView2` initialisation terminée, l’hôte:</span><span class="sxs-lookup"><span data-stu-id="10d96-201">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host:</span></span>  
    
    1.  <span data-ttu-id="10d96-202">Injecte un script dans le contenu Web qui inscrit un gestionnaire pour imprimer le message à partir de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="10d96-202">Injects a script to the web content that registers a handler to print message from the host.</span></span>  
    1.  <span data-ttu-id="10d96-203">Injecte un script dans le contenu Web qui publie l’URL vers l’hôte.</span><span class="sxs-lookup"><span data-stu-id="10d96-203">Injects a script to the web content that posts the URL to the host.</span></span>  
    
    <span data-ttu-id="10d96-204">Dans la `MainWindow.xaml.cs` mise à jour, `InitializeAsync` procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="10d96-204">In `MainWindow.xaml.cs`, update `InitializeAsync` as follows:</span></span>  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
        
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
    }
    ```  
    
    <span data-ttu-id="10d96-205">Appuyez `F5` pour générer et exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="10d96-205">Press `F5` to build and run the app.</span></span>  <span data-ttu-id="10d96-206">À présent, la barre d’adresses affiche l’URI dans le contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="10d96-206">Now, the address bar displays the URI in the WebView2 control.</span></span> <span data-ttu-id="10d96-207">Lorsque vous parvenez à un nouvel URI, le contrôle WebView2 avertit l’utilisateur de l’URI affiché dans le contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="10d96-207">When you successfully navigate to a new URI, the WebView2 control alerts the user of the URI that's displayed in the WebView2 control.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-searchbar.png" alt-text="addressBar":::
       <span data-ttu-id="10d96-209">addressBar</span><span class="sxs-lookup"><span data-stu-id="10d96-209">addressBar</span></span>
    :::image-end:::

<span data-ttu-id="10d96-210">Félicitations, vous avez créé votre première application WebView2.</span><span class="sxs-lookup"><span data-stu-id="10d96-210">Congratulations, you built your first WebView2 app!</span></span>  

## <span data-ttu-id="10d96-211">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="10d96-211">Next steps</span></span>  

*   <span data-ttu-id="10d96-212">Pour obtenir un exemple complet de fonctionnalités WebView2, voir [WebView2Samples référentiel Samples](https://github.com/MicrosoftEdge/WebView2Samples) sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="10d96-212">For a comprehensive example of WebView2 capabilities, see [WebView2Samples repo](https://github.com/MicrosoftEdge/WebView2Samples) on GitHub.</span></span>  
*   <span data-ttu-id="10d96-213">Pour plus d’informations sur les API WebView2, voir informations de référence sur les [API](/dotnet/api/microsoft.web.webview2.wpf.webview2).</span><span class="sxs-lookup"><span data-stu-id="10d96-213">For more detailed information about WebView2 APIs, see [API reference](/dotnet/api/microsoft.web.webview2.wpf.webview2).</span></span>  
*   <span data-ttu-id="10d96-214">Pour plus d’informations sur WebView2, voir [ressources WebView2](../index.md#next-steps).</span><span class="sxs-lookup"><span data-stu-id="10d96-214">For more information about  WebView2, see [WebView2 Resources](../index.md#next-steps).</span></span>  

## <span data-ttu-id="10d96-215">Contacter l’équipe WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="10d96-215">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  


<!-- links -->  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Programme d’installation de WebView2" 
