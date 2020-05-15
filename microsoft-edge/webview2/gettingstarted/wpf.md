---
description: Héberger le contenu Web dans votre application WPF avec le contrôle WebView 2 de Microsoft Edge
title: Applications WebView 2 de Microsoft Edge 2 pour les applications WPF
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, applications WPF, WPF, Edge, CoreWebView2, contrôle de navigateur, html Edge, mise en route, mise en route, .NET
ms.openlocfilehash: 01d92322a85e38dab3c502e8dd76729fef8400b1
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653366"
---
# <span data-ttu-id="7a48b-104">Commencer à utiliser WebView2 dans WPF (Preview)</span><span class="sxs-lookup"><span data-stu-id="7a48b-104">Getting Started with WebView2 in WPF (Preview)</span></span>  

<span data-ttu-id="7a48b-105">Dans cet article, vous allez commencer à créer votre première application WebView2 et à découvrir les principales fonctionnalités de [WebView2 (Preview)](/microsoft-edge/hosting/webview2/index).</span><span class="sxs-lookup"><span data-stu-id="7a48b-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2 (preview)](/microsoft-edge/hosting/webview2/index).</span></span>  <span data-ttu-id="7a48b-106">Pour plus d’informations sur les API individuelles, voir informations de référence sur les [API](../reference/dotnet/0-9-515-reference-webview2.md).</span><span class="sxs-lookup"><span data-stu-id="7a48b-106">For more information on individual APIs, see [API reference](../reference/dotnet/0-9-515-reference-webview2.md).</span></span>  

## <span data-ttu-id="7a48b-107">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="7a48b-107">Prerequisites</span></span>  

<span data-ttu-id="7a48b-108">Vérifiez que vous avez installé la liste des conditions préalables suivantes avant de continuer:</span><span class="sxs-lookup"><span data-stu-id="7a48b-108">Ensure you installed the following list of pre-requisites before proceeding:</span></span>  

* <span data-ttu-id="7a48b-109">[Microsoft Edge (chrome)](https://www.microsoftedgeinsider.com/download/) installé sur Windows 10, Windows 8,1 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7a48b-109">[Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com/download/) installed on Windows 10, Windows 8.1, or Windows 7.</span></span>  <span data-ttu-id="7a48b-110">L’équipe WebView Microsoft Edge recommande d’utiliser le canal Canaries.</span><span class="sxs-lookup"><span data-stu-id="7a48b-110">The Microsoft Edge WebView team recommends using the Canary channel.</span></span>  
* <span data-ttu-id="7a48b-111">[Visual Studio](https://visualstudio.microsoft.com/) 2015 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="7a48b-111">[Visual Studio](https://visualstudio.microsoft.com/) 2015 or later.</span></span>  

## <span data-ttu-id="7a48b-112">Étape 1: créer une application de fenêtre unique</span><span class="sxs-lookup"><span data-stu-id="7a48b-112">Step 1 - Create a single window application</span></span>

<span data-ttu-id="7a48b-113">Utiliser un projet de bureau de base contenant une seule fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="7a48b-113">Start with a basic desktop project containing a single main window.</span></span>  

1. <span data-ttu-id="7a48b-114">Ouvrez **Visual Studio.**</span><span class="sxs-lookup"><span data-stu-id="7a48b-114">Open **Visual Studio.**</span></span>
2. <span data-ttu-id="7a48b-115">Sélectionnez application **WPF .net Core** ou **application WPF .NET Framework**, puis sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="7a48b-115">Choose **WPF .NET Core App** or **WPF .NET Framework App**, and then choose **Next**.</span></span>  

    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpfcore.png" alt-text="Noyau WPF":::
             <span data-ttu-id="7a48b-117">Noyau WPF</span><span class="sxs-lookup"><span data-stu-id="7a48b-117">WPF core</span></span> :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpffw.png" alt-text="Infrastructure WPF":::
             <span data-ttu-id="7a48b-119">Infrastructure WPF</span><span class="sxs-lookup"><span data-stu-id="7a48b-119">WPF Framework</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::

3. <span data-ttu-id="7a48b-120">Entrez des valeurs pour le nom et l' **emplacement**du **projet** .</span><span class="sxs-lookup"><span data-stu-id="7a48b-120">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="7a48b-121">Sélectionnez .NET Framework 4.6.2 ou version ultérieure, ou .NET Core 3,0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="7a48b-121">Select .NET Framework 4.6.2 or later, or .NET Core 3.0 or later.</span></span>  

:::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-createcore.png" alt-text="Créer un cœur":::
             <span data-ttu-id="7a48b-123">Créer un cœur</span><span class="sxs-lookup"><span data-stu-id="7a48b-123">Create core</span></span> :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-createfw.png" alt-text="Créer une infrastructure":::
             <span data-ttu-id="7a48b-125">Créer une infrastructure</span><span class="sxs-lookup"><span data-stu-id="7a48b-125">Create Framework</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::

4. <span data-ttu-id="7a48b-126">Sélectionnez **créer** pour créer votre projet.</span><span class="sxs-lookup"><span data-stu-id="7a48b-126">Choose **Create** to create your project.</span></span>  

## <span data-ttu-id="7a48b-127">Étape 2: installer le SDK WebView2</span><span class="sxs-lookup"><span data-stu-id="7a48b-127">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="7a48b-128">Ajoutez ensuite le kit de développement logiciel (SDK) WebView2 au projet.</span><span class="sxs-lookup"><span data-stu-id="7a48b-128">Next add the WebView2 SDK to the project.</span></span>  <span data-ttu-id="7a48b-129">Pour obtenir un aperçu, installez le kit de développement logiciel (SDK) WebView2 avec NuGet.</span><span class="sxs-lookup"><span data-stu-id="7a48b-129">For the preview, install the WebView2 SDK using Nuget.</span></span>  

1. <span data-ttu-id="7a48b-130">Ouvrez le menu contextuel du projet \ (cliquez avec le bouton droit sur \) et sélectionnez **gérer les packages NuGet...**.</span><span class="sxs-lookup"><span data-stu-id="7a48b-130">Open the context menu on the project \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  

    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="NuGet":::
       <span data-ttu-id="7a48b-132">NuGet</span><span class="sxs-lookup"><span data-stu-id="7a48b-132">Nuget</span></span> :::image-end:::

2. <span data-ttu-id="7a48b-133">Entrez `Microsoft.Web.WebView2` dans la barre de recherche.</span><span class="sxs-lookup"><span data-stu-id="7a48b-133">Enter `Microsoft.Web.WebView2` in the search bar.</span></span>  <span data-ttu-id="7a48b-134">Pour cela, sélectionnez **Microsoft. Web. WebView2** dans les résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="7a48b-134">Choose **Microsoft.Web.WebView2** from the search results.</span></span>  <span data-ttu-id="7a48b-135">Définissez la version du package sur **Pre-Release**, puis sélectionnez **installer**.</span><span class="sxs-lookup"><span data-stu-id="7a48b-135">Set the package version to **pre-release**, and then choose **Install**.</span></span>  

     ![NuGet](./media/installnuget.PNG)

<span data-ttu-id="7a48b-137">Vous êtes prêt à commencer à développer des applications à l’aide de l’API WebView2.</span><span class="sxs-lookup"><span data-stu-id="7a48b-137">You are all set to start developing applications using the WebView2 API.</span></span>  <span data-ttu-id="7a48b-138">Appuyez `F5` pour générer et exécuter le projet.</span><span class="sxs-lookup"><span data-stu-id="7a48b-138">Press `F5` to build and run the project.</span></span>  <span data-ttu-id="7a48b-139">Le projet en cours d’exécution affiche une fenêtre vide.</span><span class="sxs-lookup"><span data-stu-id="7a48b-139">The running project displays an empty window.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-blank.png" alt-text="Application vide":::
   <span data-ttu-id="7a48b-141">Application vide</span><span class="sxs-lookup"><span data-stu-id="7a48b-141">Empty app</span></span>
:::image-end:::

## <span data-ttu-id="7a48b-142">Étape 3: créer un WebView unique dans MainWindow. Xaml</span><span class="sxs-lookup"><span data-stu-id="7a48b-142">Step 3 - Create a single WebView in MainWindow.xaml</span></span>  

<span data-ttu-id="7a48b-143">Ensuite, ajoutez un WebView à votre application.</span><span class="sxs-lookup"><span data-stu-id="7a48b-143">Next add a WebView to your application.</span></span>  

1. <span data-ttu-id="7a48b-144">Ouvrir `MainWindow.xaml` .</span><span class="sxs-lookup"><span data-stu-id="7a48b-144">Open `MainWindow.xaml`.</span></span>  <span data-ttu-id="7a48b-145">Ajoutez l’espace de noms XAML WebView2 en insérant la ligne suivante dans la `<Window/>` balise.</span><span class="sxs-lookup"><span data-stu-id="7a48b-145">Add the WebView2 XAML namespace by inserting the following line inside the `<Window/>` tag.</span></span>  

    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  

    <span data-ttu-id="7a48b-146">Vérifiez que le code `MainWindow.xaml` ressemble à l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="7a48b-146">Confirm that the code in `MainWindow.xaml` looks like the following code snippet.</span></span>  

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
        />
        <Grid>

                </Grid>
    </Window>
    ```  

2. <span data-ttu-id="7a48b-147">Ajoutez le contrôle WebView2 en remplaçant les `<Grid>` balises par l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="7a48b-147">Add the WebView2 control by replacing the `<Grid>` tags, with the following code snippet.</span></span>  <span data-ttu-id="7a48b-148">La `Source` propriété définit l’URI initial affiché dans le contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="7a48b-148">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  

    ```xml  
    <DockPanel>
        <wv2:WebView2 Name="webView"
                      Source="https://www.microsoft.com"
        />
    </DockPanel>
    ```  

3. <span data-ttu-id="7a48b-149">Appuyez `F5` pour générer et exécuter votre projet.</span><span class="sxs-lookup"><span data-stu-id="7a48b-149">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="7a48b-150">Vérifiez que votre contrôle WebView2 s’affiche [https://www.microsoft.com](https://www.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="7a48b-150">Confirm that your WebView2 control displays [https://www.microsoft.com](https://www.microsoft.com).</span></span>  

    :::image type="complex" source="./media/wpf-gettingstarted-microsoft.png" alt-text="Microsoft.com":::
       <span data-ttu-id="7a48b-152">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="7a48b-152">Microsoft.com</span></span> :::image-end:::

## <span data-ttu-id="7a48b-153">Étape 4: navigation</span><span class="sxs-lookup"><span data-stu-id="7a48b-153">Step 4 - Navigation</span></span>  

<span data-ttu-id="7a48b-154">Ajoutez la possibilité d’autoriser les utilisateurs à modifier l’URL d’affichage du contrôle WebView2 en ajoutant une barre d’adresse à l’application.</span><span class="sxs-lookup"><span data-stu-id="7a48b-154">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1. <span data-ttu-id="7a48b-155">Dans **MainWindow. Xaml**, ajoutez une barre d’adresse en copiant et en collant l’extrait de code suivant à l’intérieur du DockPanel qui contient le WebView.</span><span class="sxs-lookup"><span data-stu-id="7a48b-155">In **MainWindow.xaml**, add an address bar by copying and pasting the following code snippet inside the DockPanel that contains the WebView.</span></span>  

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

<span data-ttu-id="7a48b-156">Vérifiez que la `DockPanel` section de l' `MainWindow.xaml` extrait de code suivant ressemble à ceci.</span><span class="sxs-lookup"><span data-stu-id="7a48b-156">Confirm that the `DockPanel` section of `MainWindow.xaml` looks like the following code snippet.</span></span>  

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

2. <span data-ttu-id="7a48b-157">Ouvrir `MainWindow.xaml.cs` dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7a48b-157">Open `MainWindow.xaml.cs` in Visual Studio.</span></span>  <span data-ttu-id="7a48b-158">Ajoutez l' `CoreWebView2` espace de noms en insérant l’extrait de code suivant en haut de `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="7a48b-158">Add the `CoreWebView2` namespace by inserting the following code snippet at the top of `MainWindow.xaml.cs`.</span></span>  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

3. <span data-ttu-id="7a48b-159">Dans **MainWindow.Xaml.cs**, copiez l’extrait de code suivant afin de créer la `ButtonGo_Click` méthode, qui permet d’accéder à l’URL entrée dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="7a48b-159">In **MainWindow.xaml.cs**, copy the following code snippet to create the `ButtonGo_Click` method, which navigates the WebView to the URL entered in the address bar.</span></span>  

    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

<span data-ttu-id="7a48b-160">Appuyez `F5` pour générer et exécuter votre projet.</span><span class="sxs-lookup"><span data-stu-id="7a48b-160">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="7a48b-161">Entrez une nouvelle URL dans la barre d’adresses, puis cliquez sur **atteindre**.</span><span class="sxs-lookup"><span data-stu-id="7a48b-161">Enter a new URL in the address bar, and click **Go**.</span></span>  <span data-ttu-id="7a48b-162">Par exemple, entrez `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="7a48b-162">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="7a48b-163">Vérifiez que le contrôle WebView2 accède à l’URL.</span><span class="sxs-lookup"><span data-stu-id="7a48b-163">Confirm that the WebView2 control navigates to the URL.</span></span>  

> [!NOTE]
> <span data-ttu-id="7a48b-164">Vérifiez qu’une URL complète est entrée dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="7a48b-164">Make sure a complete URL is entered in the address bar.</span></span> <span data-ttu-id="7a48b-165">`ArgumentException`A est levé si l’URL ne commence pas par `http://` ou</span><span class="sxs-lookup"><span data-stu-id="7a48b-165">An `ArgumentException` is thrown if the URL does not start with `http://` or</span></span> `https://`

:::image type="complex" source="./media/wpf-gettingstarted-bing.png" alt-text="Bing":::
   <span data-ttu-id="7a48b-167">Bing</span><span class="sxs-lookup"><span data-stu-id="7a48b-167">Bing</span></span>
:::image-end:::

## <span data-ttu-id="7a48b-168">Étape 5: événements de navigation</span><span class="sxs-lookup"><span data-stu-id="7a48b-168">Step 5 - Navigation events</span></span>  

<span data-ttu-id="7a48b-169">L’application qui héberge les contrôles WebView2 écoute les événements suivants qui sont déclenchés par le contrôle WebView2 lors de la navigation dans les pages Web.</span><span class="sxs-lookup"><span data-stu-id="7a48b-169">The application that hosts WebView2 controls listens to the following events that are raised by the WebView2 control during navigation to web pages.</span></span>  

* `NavigationStarting`  
* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  
* `NavigationCompleted`  

<span data-ttu-id="7a48b-170">Pour plus d’informations, voir [événements de navigation](../reference/win32/0-9-488/icorewebview2.md#navigation-events).</span><span class="sxs-lookup"><span data-stu-id="7a48b-170">For more information, see [Navigation Events](../reference/win32/0-9-488/icorewebview2.md#navigation-events).</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Événements de navigation":::
   <span data-ttu-id="7a48b-172">Événements de navigation</span><span class="sxs-lookup"><span data-stu-id="7a48b-172">Navigation events</span></span>
:::image-end:::

<span data-ttu-id="7a48b-173">Lorsqu’une erreur se produit, les événements suivants sont déclenchés et peut dépendre de la navigation sur une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="7a48b-173">When an error occurs, the following events are raised and may depend on navigation to an error page.</span></span>  

* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  

<span data-ttu-id="7a48b-174">S’il existe une redirection HTTP, il existe plusieurs `NavigationStarting` événements.</span><span class="sxs-lookup"><span data-stu-id="7a48b-174">When there is an HTTP redirect, there are multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="7a48b-175">Pour illustrer l’utilisation de ces événements, commencez par enregistrer un gestionnaire pour `NavigationStarting` cela annule toutes les demandes qui n’utilisent pas HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7a48b-175">To demonstrate how to use these events, start by registering a handler for `NavigationStarting` that cancels any requests that do not use HTTPS.</span></span>  

<span data-ttu-id="7a48b-176">Dans `MainWindow.xaml.cs` , modifiez le constructeur comme illustré ci-dessous, puis ajoutez la `EnsureHttps` fonction.</span><span class="sxs-lookup"><span data-stu-id="7a48b-176">In `MainWindow.xaml.cs`, modify the constructor as shown below and add the `EnsureHttps` function.</span></span>  

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

<span data-ttu-id="7a48b-177">Dans le constructeur, EnsureHttps est enregistré en tant que gestionnaire d’événements sur l' `NavigationStarting` événement sur le contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="7a48b-177">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="7a48b-178">Appuyez `F5` pour générer et exécuter votre projet.</span><span class="sxs-lookup"><span data-stu-id="7a48b-178">Press `F5` to build and run your project.</span></span> <span data-ttu-id="7a48b-179">Confirmez que lorsque vous naviguez vers un site HTTP, le WebView **reste inchangé**.</span><span class="sxs-lookup"><span data-stu-id="7a48b-179">Confirm that when navigating to an HTTP site, the WebView **remains unchanged**.</span></span> <span data-ttu-id="7a48b-180">Toutefois, le WebView accède aux sites HTTPs.</span><span class="sxs-lookup"><span data-stu-id="7a48b-180">However, the WebView will navigate to HTTPS sites.</span></span>

## <span data-ttu-id="7a48b-181">Étape 6: création de scripts</span><span class="sxs-lookup"><span data-stu-id="7a48b-181">Step 6 - Scripting</span></span>  

<span data-ttu-id="7a48b-182">Vous pouvez utiliser des applications hôtes pour injecter du code JavaScript dans les contrôles WebView2 lors de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="7a48b-182">You may use host applications to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="7a48b-183">Le JavaScript injecté s’applique à tous les nouveaux documents de niveau supérieur ainsi qu’à toute image enfant jusqu’à ce que le JavaScript soit supprimé.</span><span class="sxs-lookup"><span data-stu-id="7a48b-183">The injected JavaScript applies to all new top level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="7a48b-184">Le JavaScript injecté est exécuté après la création de l’objet global et avant l’exécution de tout autre script inclus dans le document HTML.</span><span class="sxs-lookup"><span data-stu-id="7a48b-184">The injected JavaScript is run after creation of the global object, and before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="7a48b-185">Vous pouvez utiliser les scripts pour alerter l’utilisateur lorsque vous naviguez vers un site non HTTPs.</span><span class="sxs-lookup"><span data-stu-id="7a48b-185">You can use scripting to alert the user when navigating to a non-HTTPS site.</span></span>  <span data-ttu-id="7a48b-186">Modifiez la `EnsureHttps` fonction de telle sorte qu’elle injecte le script dans le contenu Web à l’aide de la méthode [ExecuteScriptAsync](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#executescriptasync) .</span><span class="sxs-lookup"><span data-stu-id="7a48b-186">Modify the `EnsureHttps` function so that it injects script into the web content using the [ExecuteScriptAsync](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#executescriptasync) method.</span></span>  

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

<span data-ttu-id="7a48b-187">Appuyez `F5` pour générer et exécuter votre projet.</span><span class="sxs-lookup"><span data-stu-id="7a48b-187">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="7a48b-188">Vérifiez que l’application affiche une alerte lorsque vous naviguez vers un site qui n’utilise pas HTTPs.</span><span class="sxs-lookup"><span data-stu-id="7a48b-188">Confirm that the application displays an alert when you navigate to a site that does not use HTTPS.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-https.png" alt-text="HTTPS":::
   <span data-ttu-id="7a48b-190">HTTPS</span><span class="sxs-lookup"><span data-stu-id="7a48b-190">HTTPS</span></span>
:::image-end:::

## <span data-ttu-id="7a48b-191">Étape 7: communication entre l’hôte et le contenu Web</span><span class="sxs-lookup"><span data-stu-id="7a48b-191">Step 7 - Communication between host and web content</span></span>  

<span data-ttu-id="7a48b-192">L’hôte et le contenu Web sont en mesure de communiquer entre eux `postMessage` comme suit:</span><span class="sxs-lookup"><span data-stu-id="7a48b-192">The host and web content may communicate with each other using `postMessage` as follows:</span></span>  

* <span data-ttu-id="7a48b-193">Le contenu Web d’un contrôle WebView2 risque de publier un message destiné à l’hôte à l’aide de `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="7a48b-193">Web content in a WebView2 control may post a message to the host using `window.chrome.webview.postMessage`.</span></span>  <span data-ttu-id="7a48b-194">L’hôte gère le message en utilisant tout inscrit `WebMessageReceived` sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="7a48b-194">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
* <span data-ttu-id="7a48b-195">Héberge les messages dans le contenu Web d’un contrôle WebView2 en utilisant `CoreWebView2.PostWebMessageAsString` ou `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="7a48b-195">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="7a48b-196">Ces messages sont interceptés par des gestionnaires ajoutés à `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="7a48b-196">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="7a48b-197">Ce mécanisme de communication permet au contenu Web de transmettre des messages à l’hôte à l’aide de fonctionnalités natives.</span><span class="sxs-lookup"><span data-stu-id="7a48b-197">This communication mechanism allows web content to pass messages to the host using native capabilities.</span></span>  

<span data-ttu-id="7a48b-198">Dans votre projet, lorsque le contrôle WebView2 navigue vers une URL, il affiche l’URL dans la barre d’adresse et avertit l’utilisateur de l’URL qui s’affiche dans le contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="7a48b-198">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1. <span data-ttu-id="7a48b-199">Dans **MainWindow.Xaml.cs**, mettez à jour votre constructeur et créez une `InitializeAsync` fonction comme illustré dans l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="7a48b-199">In **MainWindow.xaml.cs**, update your constructor and create an `InitializeAsync` function as shown in the following code snippet.</span></span>  <span data-ttu-id="7a48b-200">La `InitializeAsync` fonction est en attente [EnsureCoreWebView2Async](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#ensurecorewebview2async) , car l’initialisation de `CoreWebView2` est asynchrone.</span><span class="sxs-lookup"><span data-stu-id="7a48b-200">The `InitializeAsync` function awaits [EnsureCoreWebView2Async](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#ensurecorewebview2async) because the initialization of `CoreWebView2` is asynchronous.</span></span>  

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

2. <span data-ttu-id="7a48b-201">Une fois **CoreWebView2** initialisé, inscrivez un gestionnaire d’événements pour y répondre `WebMessageReceived` .</span><span class="sxs-lookup"><span data-stu-id="7a48b-201">After **CoreWebView2** is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="7a48b-202">Dans **MainWindow.Xaml.cs** Update `InitializeAsync` et ajoutez `UpdateAddressBar` à l’aide de l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="7a48b-202">In **MainWindow.xaml.cs** update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  

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

3. <span data-ttu-id="7a48b-203">Pour que le WebView envoie un message électronique et y réponde, une fois l' `CoreWebView2` initialisation terminée, l’hôte:</span><span class="sxs-lookup"><span data-stu-id="7a48b-203">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host:</span></span>  

    1. <span data-ttu-id="7a48b-204">Injecte un script dans le contenu Web qui inscrit un gestionnaire pour imprimer le message à partir de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="7a48b-204">Injects a script to the web content that registers a handler to print message from the host.</span></span>  
    2. <span data-ttu-id="7a48b-205">Injecte un script dans le contenu Web qui publie l’URL vers l’hôte.</span><span class="sxs-lookup"><span data-stu-id="7a48b-205">Injects a script to the web content that posts the URL to the host.</span></span>  

<span data-ttu-id="7a48b-206">Dans la `MainWindow.xaml.cs` mise à jour, `InitializeAsync` procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="7a48b-206">In `MainWindow.xaml.cs`, update `InitializeAsync` as follows:</span></span>  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

<span data-ttu-id="7a48b-207">Appuyez `F5` pour générer et exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="7a48b-207">Press `F5` to build and run the app.</span></span>  <span data-ttu-id="7a48b-208">À présent, la barre d’adresses affiche l’URI dans le WebView et, lorsque vous accédez à un nouvel URI, le WebView avertit l’utilisateur de l’URI affiché dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="7a48b-208">Now the address bar displays the URI in the WebView and when you successfully navigate to a new URI, the WebView alerts the user of the URI displayed in the WebView.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-searchbar.png" alt-text="addressBar":::
   <span data-ttu-id="7a48b-210">addressBar</span><span class="sxs-lookup"><span data-stu-id="7a48b-210">addressBar</span></span>
:::image-end:::

<span data-ttu-id="7a48b-211">Félicitations, vous avez créé votre première application WebView2.</span><span class="sxs-lookup"><span data-stu-id="7a48b-211">Congratulations, you built your first WebView2 app!</span></span>  

## <span data-ttu-id="7a48b-212">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="7a48b-212">Next Steps</span></span>  

<span data-ttu-id="7a48b-213">Il existe de nombreuses fonctionnalités WebView2 non traitées dans cette procédure pas à pas.</span><span class="sxs-lookup"><span data-stu-id="7a48b-213">There are plenty of WebView2 functionalities that are not covered in this walkthrough.</span></span>  

<span data-ttu-id="7a48b-214">Pour en savoir plus:</span><span class="sxs-lookup"><span data-stu-id="7a48b-214">To learn more:</span></span>  

* <span data-ttu-id="7a48b-215">Pour plus d’informations sur chaque API, consultez les informations de référence sur les [API](../reference/dotnet/0-9-515-reference-webview2.md) .</span><span class="sxs-lookup"><span data-stu-id="7a48b-215">Please explore [API reference](../reference/dotnet/0-9-515-reference-webview2.md) for detailed information about each API.</span></span>  

## <span data-ttu-id="7a48b-216">Contacter l’équipe WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7a48b-216">Getting in touch with the Microsoft Edge WebView team</span></span>  

<span data-ttu-id="7a48b-217">Aidez-vous à créer une expérience WebView2 plus riche en partageant vos commentaires!</span><span class="sxs-lookup"><span data-stu-id="7a48b-217">Help build a richer WebView2 experience by sharing your feedback!</span></span>  <span data-ttu-id="7a48b-218">Visitez le site Web Microsoft Edge [référentiel Samples](https://aka.ms/webviewfeedback) pour envoyer des demandes de fonctionnalité ou des rapports de bogues, ou pour rechercher des problèmes connus.</span><span class="sxs-lookup"><span data-stu-id="7a48b-218">Visit the Microsoft Edge WebView [feedback repo](https://aka.ms/webviewfeedback) to submit feature requests or bug reports or search for known issues.</span></span>  
