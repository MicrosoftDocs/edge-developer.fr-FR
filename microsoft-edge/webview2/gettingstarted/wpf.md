---
description: Guide de mise en place avec WebView2 pour les applications WPF
title: Mise en place de WebView2 pour les applications WPF
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, webview, applications wpf, wpf, edge, CoreWebView2, contrôle de navigateur, edge html, mise en main, mise en main, .NET
ms.openlocfilehash: de67b8a2da8cda0339b5e8d0b96cf4c3df260ec6
ms.sourcegitcommit: d89f77d4667dfbc44ed35f2ec7e3ae64ab98bf1a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2021
ms.locfileid: "11306144"
---
# <span data-ttu-id="68337-104">Mise en place de WebView2 dans WPF</span><span class="sxs-lookup"><span data-stu-id="68337-104">Getting started with WebView2 in WPF</span></span>

<span data-ttu-id="68337-105">Dans cet article, commencer à créer votre première application WebView2 et en savoir plus sur les principales fonctionnalités de [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span><span class="sxs-lookup"><span data-stu-id="68337-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="68337-106">Pour plus d’informations sur les API individuelles, accédez à la [référence d’API.][DotnetApiMicrosoftWebWebview2Wpf]</span><span class="sxs-lookup"><span data-stu-id="68337-106">For more information on individual APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2Wpf].</span></span>  

## <span data-ttu-id="68337-107">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="68337-107">Prerequisites</span></span>  

<span data-ttu-id="68337-108">Veillez à installer la liste des conditions préalables suivante avant de poursuivre.</span><span class="sxs-lookup"><span data-stu-id="68337-108">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="68337-109">[WebView2 Runtime][Webview2Installer] ou tout canal [non stable Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] installé sur le système d’exploitation pris en charge \(actuellement Windows 10, Windows 8.1 et Windows 7\).</span><span class="sxs-lookup"><span data-stu-id="68337-109">[WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span></span>  
*   <span data-ttu-id="68337-110">[Visual Studio][MicrosoftVisualstudioMain] 2017 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="68337-110">[Visual Studio][MicrosoftVisualstudioMain] 2017 or later.</span></span>  
    
## <span data-ttu-id="68337-111">Étape 1 : créer une application à fenêtre unique</span><span class="sxs-lookup"><span data-stu-id="68337-111">Step 1 - Create a single-window app</span></span>  

<span data-ttu-id="68337-112">Commencez par un projet de bureau de base qui contient une seule fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="68337-112">Start with a basic desktop project that contains a single main window.</span></span>  

1.  <span data-ttu-id="68337-113">In Visual Studio, choose **WPF .NET Core App** \(or **WPF .NET Framework App**\) > **Next**.</span><span class="sxs-lookup"><span data-stu-id="68337-113">In Visual Studio, choose **WPF .NET Core App** \(or **WPF .NET Framework App**\) > **Next**.</span></span>  
    
    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpfcore.png" alt-text="WPF core":::
             <span data-ttu-id="68337-115">WPF core</span><span class="sxs-lookup"><span data-stu-id="68337-115">WPF core</span></span> :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpffw.png" alt-text="WPF Framework":::
             <span data-ttu-id="68337-117">WPF Framework</span><span class="sxs-lookup"><span data-stu-id="68337-117">WPF Framework</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="68337-118">Entrez des valeurs **pour le nom et l’emplacement** du **projet.**</span><span class="sxs-lookup"><span data-stu-id="68337-118">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="68337-119">Choose **.NET Framework 4.6.2** or later \(or **.NET Core 3.0** or later\).</span><span class="sxs-lookup"><span data-stu-id="68337-119">Choose **.NET Framework 4.6.2** or later \(or **.NET Core 3.0** or later\).</span></span>  
    
    :::row:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createcore.png" alt-text="Créer un cœur":::
                 <span data-ttu-id="68337-121">Créer un cœur</span><span class="sxs-lookup"><span data-stu-id="68337-121">Create core</span></span> :::image-end:::
           :::column-end:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createfw.png" alt-text="Créer une infrastructure":::
                 <span data-ttu-id="68337-123">Créer une infrastructure</span><span class="sxs-lookup"><span data-stu-id="68337-123">Create Framework</span></span> :::image-end:::
           :::column-end:::
        :::row-end:::
    
1.  <span data-ttu-id="68337-124">Pour créer votre projet, choisissez **Créer.**</span><span class="sxs-lookup"><span data-stu-id="68337-124">To create your project, choose **Create**.</span></span>  
    
## <span data-ttu-id="68337-125">Étape 2 : installer le SDK WebView2</span><span class="sxs-lookup"><span data-stu-id="68337-125">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="68337-126">Utilisez NuGet pour ajouter le SDK WebView2 au projet.</span><span class="sxs-lookup"><span data-stu-id="68337-126">Use NuGet to add the WebView2 SDK to the project.</span></span>  

1.  <span data-ttu-id="68337-127">Pointez sur le projet, ouvrez le menu contextuel \(clic droit\), puis choisissez Gérer les **packages NuGet...**.</span><span class="sxs-lookup"><span data-stu-id="68337-127">Hover on the projecty, open the contextual menu \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Gérer des packages NuGet":::
       <span data-ttu-id="68337-129">Gérer des packages NuGet</span><span class="sxs-lookup"><span data-stu-id="68337-129">Manage NuGet packages</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="68337-130">Dans la barre de recherche, `Microsoft.Web.WebView2` tapez > **choisissez Microsoft.Web.WebView2**.</span><span class="sxs-lookup"><span data-stu-id="68337-130">In the search bar, type `Microsoft.Web.WebView2` > choose **Microsoft.Web.WebView2**.</span></span>  
   
    :::image type="complex" source="./media/installnuget.png" alt-text="NuGet" lightbox="./media/installnuget.png":::
       <span data-ttu-id="68337-132">NuGet</span><span class="sxs-lookup"><span data-stu-id="68337-132">NuGet</span></span>  
    :::image-end:::
    
    <span data-ttu-id="68337-133">Prêt à commencer à développer des applications à l’aide de l’API WebView2.</span><span class="sxs-lookup"><span data-stu-id="68337-133">Ready to start developing apps using the WebView2 API.</span></span>  <span data-ttu-id="68337-134">Pour créer et exécuter le projet, sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="68337-134">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="68337-135">Le projet en cours d’exécution affiche une fenêtre vide.</span><span class="sxs-lookup"><span data-stu-id="68337-135">The running project displays an empty window.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-blank.png" alt-text="Application vide":::
       <span data-ttu-id="68337-137">Application vide</span><span class="sxs-lookup"><span data-stu-id="68337-137">Empty app</span></span>
    :::image-end:::  
    
## <span data-ttu-id="68337-138">Étape 3 : créer un seul WebView dans MainWindow.xaml</span><span class="sxs-lookup"><span data-stu-id="68337-138">Step 3 - Create a single WebView in MainWindow.xaml</span></span>  

<span data-ttu-id="68337-139">Ensuite, ajoutez un WebView à votre application.</span><span class="sxs-lookup"><span data-stu-id="68337-139">Next add a WebView to your app.</span></span>  

1.  <span data-ttu-id="68337-140">Dans le fichier, pour ajouter l’espace de noms `MainWindow.xaml` XAML WebView2, insérez la ligne suivante à l’intérieur de la `<Window/>` balise.</span><span class="sxs-lookup"><span data-stu-id="68337-140">In the `MainWindow.xaml` file, to add the WebView2 XAML namespace, insert the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  
    
    <span data-ttu-id="68337-141">Assurez-vous que le code `MainWindow.xaml` dans ressemble à l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="68337-141">Ensure the code in `MainWindow.xaml` looks like the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="68337-142">Pour ajouter le contrôle WebView2, remplacez les balises par l’extrait de `<Grid>` code suivant.</span><span class="sxs-lookup"><span data-stu-id="68337-142">To add the WebView2 control, replace the `<Grid>` tags with the following code snippet.</span></span>  <span data-ttu-id="68337-143">La `Source` propriété définit l’URI initial affiché dans le contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="68337-143">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
    ```xml  
    <DockPanel>
        <wv2:WebView2 Name="webView"
                      Source="https://www.microsoft.com"
        />
    </DockPanel>
    ```  
    
1.  <span data-ttu-id="68337-144">Pour créer et exécuter le projet, sélectionnez `F5` Vérifier que votre contrôle WebView2 s’affiche. [https://www.microsoft.com][|::ref1::|Main]</span><span class="sxs-lookup"><span data-stu-id="68337-144">To build and run the project, select `F5`  Ensure your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-microsoft.png" alt-text="Microsoft.com":::
       <span data-ttu-id="68337-146">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="68337-146">Microsoft.com</span></span>
    :::image-end:::  
    
## <span data-ttu-id="68337-147">Étape 4 : navigation</span><span class="sxs-lookup"><span data-stu-id="68337-147">Step 4 - Navigation</span></span>  

<span data-ttu-id="68337-148">Ajoutez la possibilité d’autoriser les utilisateurs à modifier l’URL affichée par le contrôle WebView2 en ajoutant une barre d’adresse à l’application.</span><span class="sxs-lookup"><span data-stu-id="68337-148">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1.  <span data-ttu-id="68337-149">Dans le fichier, ajoutez une barre d’adresses en copiant et en coller l’extrait de code suivant à l’intérieur de l’écran `MainWindow.xaml` `<DockPanel>` WebView.</span><span class="sxs-lookup"><span data-stu-id="68337-149">In the `MainWindow.xaml` file, add an address bar by copying and pasting the following code snippet inside the `<DockPanel>` that contains the WebView.</span></span>  
    
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
    
    <span data-ttu-id="68337-150">`<DockPanel>`Assurez-vous que la section du fichier correspond à `MainWindow.xaml` l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="68337-150">Ensure the `<DockPanel>` section of the `MainWindow.xaml` file matches the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="68337-151">Dans Visual Studio, dans le fichier, pour ajouter l’espace de noms, insérez l’extrait de code suivant `MainWindow.xaml.cs` `CoreWebView2` en haut.</span><span class="sxs-lookup"><span data-stu-id="68337-151">In Visual Studio, in the `MainWindow.xaml.cs` file, to add the `CoreWebView2` namespace, insert the following code snippet at the top.</span></span>  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```
    
1.  <span data-ttu-id="68337-152">Dans le fichier, copiez l’extrait de code suivant pour créer la méthode, qui navigue dans le WebView jusqu’à l’URL entrée `MainWindow.xaml.cs` `ButtonGo_Click` dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="68337-152">In the `MainWindow.xaml.cs`file, copy the following code snippet to create the `ButtonGo_Click` method, which navigates the WebView to the URL entered in the address bar.</span></span>  
    
    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  
    
    <span data-ttu-id="68337-153">Pour créer et exécuter le projet, sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="68337-153">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="68337-154">Tapez une nouvelle URL dans la barre d’adresses et choisissez **Go**.</span><span class="sxs-lookup"><span data-stu-id="68337-154">Type a new URL in the address bar and choose **Go**.</span></span>  <span data-ttu-id="68337-155">Par exemple, tapez `https://www.bing.com`.</span><span class="sxs-lookup"><span data-stu-id="68337-155">For example, type `https://www.bing.com`.</span></span>  <span data-ttu-id="68337-156">Assurez-vous que le contrôle WebView2 navigue jusqu’à l’URL.</span><span class="sxs-lookup"><span data-stu-id="68337-156">Ensure the WebView2 control navigates to the URL.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="68337-157">Assurez-vous qu’une URL complète est entrée dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="68337-157">Make sure a complete URL is entered in the address bar.</span></span>  <span data-ttu-id="68337-158">Une `ArgumentException` url est lancée si l’URL ne commence pas par ou `http://` `https://` .</span><span class="sxs-lookup"><span data-stu-id="68337-158">An `ArgumentException` is thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-bing.png" alt-text="Bing":::
       <span data-ttu-id="68337-160">bing.com</span><span class="sxs-lookup"><span data-stu-id="68337-160">bing.com</span></span>
    :::image-end:::
    
## <span data-ttu-id="68337-161">Étape 5 : événements de navigation</span><span class="sxs-lookup"><span data-stu-id="68337-161">Step 5 - Navigation events</span></span>  

<span data-ttu-id="68337-162">Lors de la navigation sur la page web, le contrôle WebView2 lève des événements.</span><span class="sxs-lookup"><span data-stu-id="68337-162">During webpage navigation, the WebView2 control raises events.</span></span>  <span data-ttu-id="68337-163">L’application qui héberge les contrôles WebView2 écoute les événements suivants.</span><span class="sxs-lookup"><span data-stu-id="68337-163">The app that hosts WebView2 controls listens for the following events.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

<span data-ttu-id="68337-164">Pour plus d’informations, accédez à [Événements de navigation.][Webview2ConceptsNavigationEvents]</span><span class="sxs-lookup"><span data-stu-id="68337-164">For more information, navigate to [Navigation Events][Webview2ConceptsNavigationEvents].</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Événements de navigation":::
   <span data-ttu-id="68337-166">Événements de navigation</span><span class="sxs-lookup"><span data-stu-id="68337-166">Navigation events</span></span>
:::image-end:::  

<span data-ttu-id="68337-167">Lorsqu’une erreur se produit, les événements suivants sont élevés et peuvent dépendre de la navigation vers une page web d’erreur.</span><span class="sxs-lookup"><span data-stu-id="68337-167">When an error occurs, the following events are raised and may depend on navigation to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

> [!NOTE]
> <span data-ttu-id="68337-168">Si une redirection HTTP se produit, il existe plusieurs `NavigationStarting` événements dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="68337-168">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="68337-169">Pour montrer comment utiliser les événements, inscrivez un responsable pour annuler toutes les demandes `NavigationStarting` non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="68337-169">To demonstrate how to use the events, register a handler for `NavigationStarting` that cancels any non-HTTPS requests.</span></span>  

<span data-ttu-id="68337-170">Dans le fichier, modifiez le constructeur pour qu’il corresponde à l’extrait de code suivant `MainWindow.xaml.cs` et ajoutez la `EnsureHttps` fonction.</span><span class="sxs-lookup"><span data-stu-id="68337-170">In the `MainWindow.xaml.cs` file, modify the constructor to match the following code snippet and add the `EnsureHttps` function.</span></span>  

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

<span data-ttu-id="68337-171">Dans le constructeur, EnsureHttps est inscrit en tant que handler d’événements sur l’événement `NavigationStarting` sur le contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="68337-171">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="68337-172">Pour créer et exécuter le projet, sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="68337-172">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="68337-173">Assurez-vous que lorsque vous naviguez vers un site HTTP, le WebView reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="68337-173">Ensure when navigating to an HTTP site, the WebView remains unchanged.</span></span>  <span data-ttu-id="68337-174">Toutefois, le WebView navigue vers les sites HTTPS.</span><span class="sxs-lookup"><span data-stu-id="68337-174">However, the WebView navigates to HTTPS sites.</span></span>  

## <span data-ttu-id="68337-175">Étape 6 : scripts</span><span class="sxs-lookup"><span data-stu-id="68337-175">Step 6 - Scripting</span></span>  

<span data-ttu-id="68337-176">Vous pouvez utiliser des applications hôtes pour injecter du code JavaScript dans des contrôles WebView2 lors de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="68337-176">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="68337-177">Vous pouvez tâcher WebView pour exécuter du javaScript arbitraire ou ajouter des scripts d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="68337-177">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="68337-178">Le javaScript injecté s’applique à tous les nouveaux documents de niveau supérieur et aux images enfants jusqu’à ce que le JavaScript soit supprimé.</span><span class="sxs-lookup"><span data-stu-id="68337-178">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="68337-179">Le javaScript injecté est exécuté avec un minutage spécifique.</span><span class="sxs-lookup"><span data-stu-id="68337-179">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="68337-180">Exécutez-le après la création de l’objet global.</span><span class="sxs-lookup"><span data-stu-id="68337-180">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="68337-181">Exécutez-le avant tout autre script inclus dans le document HTML.</span><span class="sxs-lookup"><span data-stu-id="68337-181">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="68337-182">Par exemple, ajoutez des scripts qui envoient une alerte lorsqu’un utilisateur navigue vers des sites non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="68337-182">As an example, add scripts that send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="68337-183">Modifiez la fonction pour injecter un script dans le contenu web qui utilise la méthode `EnsureHttps` [ExecuteScriptAsync.](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync)</span><span class="sxs-lookup"><span data-stu-id="68337-183">Modify the `EnsureHttps` function to inject a script into the web content that uses [ExecuteScriptAsync](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync) method.</span></span>  

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

<span data-ttu-id="68337-184">Pour créer et exécuter le projet, sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="68337-184">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="68337-185">Assurez-vous que l’application affiche une alerte lorsque vous accédez à un site web qui n’utilise pas HTTPS.</span><span class="sxs-lookup"><span data-stu-id="68337-185">Ensure the app displays an alert when you navigate to a website that doesn't use HTTPS.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-https.png" alt-text="HTTPS":::
   <span data-ttu-id="68337-187">HTTPS</span><span class="sxs-lookup"><span data-stu-id="68337-187">HTTPS</span></span>
:::image-end:::  

## <span data-ttu-id="68337-188">Étape 7 : communication entre le contenu hôte et le contenu web</span><span class="sxs-lookup"><span data-stu-id="68337-188">Step 7 - Communication between host and web content</span></span>  

<span data-ttu-id="68337-189">Le contenu hôte et web peut communiquer les uns avec les autres à l’aide `postMessage` des données suivantes :</span><span class="sxs-lookup"><span data-stu-id="68337-189">The host and web content may communicate with each other using `postMessage` as follows:</span></span>  

*   <span data-ttu-id="68337-190">Le contenu web d’un contrôle WebView2 peut publier un message à l’hôte à l’aide de `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="68337-190">Web content in a WebView2 control may post a message to the host using `window.chrome.webview.postMessage`.</span></span>  <span data-ttu-id="68337-191">L’hôte gère le message à l’aide de tous les messages `WebMessageReceived` enregistrés sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="68337-191">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
*   <span data-ttu-id="68337-192">Héberge des messages publiés dans du contenu web dans un contrôle WebView2 à l’aide `CoreWebView2.PostWebMessageAsString` ou `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="68337-192">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="68337-193">Ces messages sont capturés par des responsables ajoutés à `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="68337-193">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="68337-194">Le mécanisme de communication transmet les messages du contenu web à l’hôte à l’aide de fonctionnalités natives.</span><span class="sxs-lookup"><span data-stu-id="68337-194">The communication mechanism passes messages from web content to the host using native capabilities.</span></span>  

<span data-ttu-id="68337-195">Dans votre projet, lorsque le contrôle WebView2 navigue vers une URL, il affiche l’URL dans la barre d’adresses et avertit l’utilisateur de l’URL affichée dans le contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="68337-195">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1.  <span data-ttu-id="68337-196">Dans le fichier, mettez à jour votre constructeur et `MainWindow.xaml.cs` créez `InitializeAsync` une fonction pour qu’elle corresponde à l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="68337-196">In the `MainWindow.xaml.cs` file, update your constructor and create an `InitializeAsync` function to match the following code snippet.</span></span>  <span data-ttu-id="68337-197">La `InitializeAsync` fonction attend [EnsureCoreWebView2Async,](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) car l’initialisation est `CoreWebView2` asynchrone.</span><span class="sxs-lookup"><span data-stu-id="68337-197">The `InitializeAsync` function awaits [EnsureCoreWebView2Async](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) because the initialization of `CoreWebView2` is asynchronous.</span></span>  
    
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
    
1.  <span data-ttu-id="68337-198">Une **fois CoreWebView2** initialisé, inscrivez un handler d’événements pour y `WebMessageReceived` répondre.</span><span class="sxs-lookup"><span data-stu-id="68337-198">After **CoreWebView2** is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="68337-199">Dans `MainWindow.xaml.cs` , mettez à jour et `InitializeAsync` `UpdateAddressBar` ajoutez à l’aide de l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="68337-199">In `MainWindow.xaml.cs`, update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="68337-200">Pour que Le WebView envoie et réponde au message web, une fois `CoreWebView2` initialisé, l’hôte :</span><span class="sxs-lookup"><span data-stu-id="68337-200">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host:</span></span>  
    1.  <span data-ttu-id="68337-201">Injecte un script au contenu web qui inscrit un handler pour imprimer un message à partir de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="68337-201">Injects a script to the web content that registers a handler to print message from the host.</span></span>  
    1.  <span data-ttu-id="68337-202">Injecte un script au contenu web qui publie l’URL à l’hôte.</span><span class="sxs-lookup"><span data-stu-id="68337-202">Injects a script to the web content that posts the URL to the host.</span></span>  
        
    <span data-ttu-id="68337-203">Dans le `MainWindow.xaml.cs` fichier, mettez à `InitializeAsync` jour pour correspondre à l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="68337-203">In the `MainWindow.xaml.cs` file, update `InitializeAsync` to match the following code snippet.</span></span>  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
        
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
    }
    ```  
    
    <span data-ttu-id="68337-204">Pour créer et exécuter l’application, sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="68337-204">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="68337-205">À présent, la barre d’adresses affiche l’URI dans le contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="68337-205">Now, the address bar displays the URI in the WebView2 control.</span></span>  <span data-ttu-id="68337-206">Lorsque vous accédez à un nouvel URI, le contrôle WebView2 avertit l’utilisateur de l’URI qui s’affiche dans le contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="68337-206">When you successfully navigate to a new URI, the WebView2 control alerts the user of the URI that's displayed in the WebView2 control.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-searchbar.png" alt-text="addressBar":::
       <span data-ttu-id="68337-208">addressBar</span><span class="sxs-lookup"><span data-stu-id="68337-208">addressBar</span></span>
    :::image-end:::

<span data-ttu-id="68337-209">Félicitations, vous avez créé votre première application WebView2.</span><span class="sxs-lookup"><span data-stu-id="68337-209">Congratulations, you built your first WebView2 app.</span></span>  

## <span data-ttu-id="68337-210">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="68337-210">Next steps</span></span>  

<span data-ttu-id="68337-211">Pour en savoir plus sur WebView2, accédez aux ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="68337-211">To continue learning more about WebView2, navigate to the following resources.</span></span>  

### <span data-ttu-id="68337-212">Voir également</span><span class="sxs-lookup"><span data-stu-id="68337-212">See also</span></span>  

*   <span data-ttu-id="68337-213">Pour obtenir un exemple complet des fonctionnalités WebView2, accédez au référentiel [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain] sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="68337-213">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples repo][GithubMicrosoftedgeWebview2samplesMain] on GitHub.</span></span>  
*   <span data-ttu-id="68337-214">Pour plus d’informations sur l’API WebView2, accédez à la référence [d’API.](/dotnet/api/microsoft.web.webview2.wpf.webview2)</span><span class="sxs-lookup"><span data-stu-id="68337-214">For more detailed information about WebView2 API, navigate to [API reference](/dotnet/api/microsoft.web.webview2.wpf.webview2).</span></span>  
*   <span data-ttu-id="68337-215">Pour plus d’informations sur WebView2, accédez [à Ressources WebView2.](../index.md#next-steps)</span><span class="sxs-lookup"><span data-stu-id="68337-215">For more information about  WebView2, navigate to [WebView2 Resources](../index.md#next-steps).</span></span>  

## <span data-ttu-id="68337-216">Entrer en contact avec l’équipe Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="68337-216">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  
 
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