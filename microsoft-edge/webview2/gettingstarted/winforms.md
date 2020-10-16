---
description: Guide de mise en route de WebView2 pour les applications WinForms
title: Mise en route de WebView2 pour les applications WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/15/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, WinForms applications, WinForms, Edge, CoreWebView2, contrôle de navigateur, html Edge, mise en route, mise en route, .NET, Windows Forms
ms.openlocfilehash: 90d25816b862d6096856faf439436706c98f7dbe
ms.sourcegitcommit: 442de63da52d00c6dc27fa08ccdb736534127566
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "11120087"
---
# <span data-ttu-id="ec023-104">Mise en route de WebView2 dans Windows Forms (Preview)</span><span class="sxs-lookup"><span data-stu-id="ec023-104">Getting started with WebView2 in Windows Forms (Preview)</span></span>  

<span data-ttu-id="ec023-105">Dans cet article, vous allez commencer à créer votre première application WebView2 et à découvrir les principales fonctionnalités de [WebView2 (Preview)](/microsoft-edge/webview2/index).</span><span class="sxs-lookup"><span data-stu-id="ec023-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2 (preview)](/microsoft-edge/webview2/index).</span></span>  <span data-ttu-id="ec023-106">Pour plus d’informations sur les API individuelles, voir informations de référence sur les [API](/dotnet/api/microsoft.web.webview2.winforms).</span><span class="sxs-lookup"><span data-stu-id="ec023-106">For more information on individual APIs, see [API reference](/dotnet/api/microsoft.web.webview2.winforms).</span></span>  

## <span data-ttu-id="ec023-107">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="ec023-107">Prerequisites</span></span>  

<span data-ttu-id="ec023-108">Vérifiez que vous avez installé la liste des conditions préalables suivantes avant de continuer:</span><span class="sxs-lookup"><span data-stu-id="ec023-108">Ensure you installed the following list of pre-requisites before proceeding:</span></span>  

* <span data-ttu-id="ec023-109">[Canal Canaries Microsoft Edge (chrome)](https://www.microsoftedgeinsider.com/download) installé sur Windows 10, Windows 8,1 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ec023-109">[Microsoft Edge (Chromium) Canary channel](https://www.microsoftedgeinsider.com/download) installed on Windows 10, Windows 8.1, or Windows 7.</span></span> 
* <span data-ttu-id="ec023-110">[Visual Studio](https://visualstudio.microsoft.com) 2017 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ec023-110">[Visual Studio](https://visualstudio.microsoft.com) 2017 or later.</span></span>

> [!NOTE]
> <span data-ttu-id="ec023-111">WebView2 ne prend actuellement pas en charge le concepteur de .NET Core 3.0 [(Preview)](https://visualstudio.microsoft.com/vs/preview).</span><span class="sxs-lookup"><span data-stu-id="ec023-111">WebView2 does not currently support the .NET Core 3.0's [designer (preview)](https://visualstudio.microsoft.com/vs/preview).</span></span>

## <span data-ttu-id="ec023-112">Étape 1: créer une application de fenêtre unique</span><span class="sxs-lookup"><span data-stu-id="ec023-112">Step 1 - Create a single window application</span></span>

<span data-ttu-id="ec023-113">Utiliser un projet de bureau de base contenant une seule fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="ec023-113">Start with a basic desktop project containing a single main window.</span></span>  

1. <span data-ttu-id="ec023-114">Ouvrez **Visual Studio.**</span><span class="sxs-lookup"><span data-stu-id="ec023-114">Open **Visual Studio.**</span></span>

1. <span data-ttu-id="ec023-115">Choisissez **application .NET Framework pour Windows Forms** , puis sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ec023-115">Choose **Windows Forms .NET Framework App** and then choose **Next**.</span></span>

    ![NewProject](./media/winforms-newproject.png)

1. <span data-ttu-id="ec023-117">Entrez des valeurs pour le nom et l' **emplacement**du **projet** .</span><span class="sxs-lookup"><span data-stu-id="ec023-117">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="ec023-118">Sélectionnez **.NET Framework 4.6.2** ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ec023-118">Select **.NET Framework 4.6.2** or later.</span></span>  

    ![startproject](./media/winforms-startproj.png)

1. <span data-ttu-id="ec023-120">Sélectionnez **créer** pour créer votre projet.</span><span class="sxs-lookup"><span data-stu-id="ec023-120">Choose **Create** to create your project.</span></span>

## <span data-ttu-id="ec023-121">Étape 2: installer le SDK WebView2</span><span class="sxs-lookup"><span data-stu-id="ec023-121">Step 2 - Install WebView2 SDK</span></span>

<span data-ttu-id="ec023-122">Ajoutez ensuite le kit de développement logiciel (SDK) WebView2 au projet.</span><span class="sxs-lookup"><span data-stu-id="ec023-122">Next add the WebView2 SDK to the project.</span></span>  <span data-ttu-id="ec023-123">Pour obtenir un aperçu, installez le kit de développement logiciel (SDK) WebView2 avec NuGet.</span><span class="sxs-lookup"><span data-stu-id="ec023-123">For the preview, install the WebView2 SDK using Nuget.</span></span>  

1. <span data-ttu-id="ec023-124">Ouvrez le menu contextuel du projet \ (cliquez avec le bouton droit sur \) et sélectionnez **gérer les packages NuGet...**.</span><span class="sxs-lookup"><span data-stu-id="ec023-124">Open the context menu on the project \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  

    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Gérer les packages NuGet":::
       <span data-ttu-id="ec023-126">Gérer les packages NuGet</span><span class="sxs-lookup"><span data-stu-id="ec023-126">Manage NuGet Packages</span></span> :::image-end:::

1. <span data-ttu-id="ec023-127">Entrez `Microsoft.Web.WebView2` dans la barre de recherche.</span><span class="sxs-lookup"><span data-stu-id="ec023-127">Enter `Microsoft.Web.WebView2` in the search bar.</span></span>  <span data-ttu-id="ec023-128">Pour cela, sélectionnez **Microsoft. Web. WebView2** dans les résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="ec023-128">Choose **Microsoft.Web.WebView2** from the search results.</span></span>  

    > [!IMPORTANT]
    > <span data-ttu-id="ec023-129">Assurez-vous que la case à cocher inclure la version **préliminaire**, sélectionnez un package de version préliminaire dans **version**, puis sélectionnez **installer**.</span><span class="sxs-lookup"><span data-stu-id="ec023-129">Ensure you check **Include prerelease**, select a prerelease package in **Version**, and then choose **Install**.</span></span>  

    ![NuGet](./media/installnuget.png)

<span data-ttu-id="ec023-131">Vous êtes prêt à commencer à développer des applications à l’aide de l’API WebView2.</span><span class="sxs-lookup"><span data-stu-id="ec023-131">You are all set to start developing applications using the WebView2 API.</span></span>  <span data-ttu-id="ec023-132">Sélectionnez `F5` pour générer et exécuter le projet.</span><span class="sxs-lookup"><span data-stu-id="ec023-132">Select `F5` to build and run the project.</span></span>  <span data-ttu-id="ec023-133">Le projet en cours d’exécution affiche une fenêtre vide.</span><span class="sxs-lookup"><span data-stu-id="ec023-133">The running project displays an empty window.</span></span>  

![emptyApp](./media/winforms-emptyApp.png)

## <span data-ttu-id="ec023-135">Étape 3: créer un WebView unique</span><span class="sxs-lookup"><span data-stu-id="ec023-135">Step 3 - Create a single WebView</span></span>  

<span data-ttu-id="ec023-136">Ensuite, ajoutez un WebView à votre application.</span><span class="sxs-lookup"><span data-stu-id="ec023-136">Next add a WebView to your application.</span></span>  

1. <span data-ttu-id="ec023-137">Ouvrez le **Concepteur Windows Forms**.</span><span class="sxs-lookup"><span data-stu-id="ec023-137">Open the **Windows Forms Designer**.</span></span>  
1. <span data-ttu-id="ec023-138">Recherchez **WebView2** dans la **boîte à outils**.</span><span class="sxs-lookup"><span data-stu-id="ec023-138">Search for **WebView2** in the **Toolbox**.</span></span> <span data-ttu-id="ec023-139">Faites glisser et déposez le contrôle **WebView2** dans l’application Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="ec023-139">Drag and drop the **WebView2** control into the Windows Forms App.</span></span>
    
    :::image type="complex" source="./media/winforms-toolbox.png" alt-text="Gérer les packages NuGet":::
       <span data-ttu-id="ec023-141">Boîte à outils affichant WebView2</span><span class="sxs-lookup"><span data-stu-id="ec023-141">Toolbox displaying WebView2</span></span> :::image-end:::  

1. <span data-ttu-id="ec023-142">Remplacez la `Name` propriété par `webView` .</span><span class="sxs-lookup"><span data-stu-id="ec023-142">Change the `Name` property to `webView`.</span></span>
    
    :::image type="complex" source="./media/winforms-properties.png" alt-text="Gérer les packages NuGet":::
       <span data-ttu-id="ec023-144">Propriétés du contrôle WebView2</span><span class="sxs-lookup"><span data-stu-id="ec023-144">Properties of the WebView2 control</span></span> :::image-end:::

1. <span data-ttu-id="ec023-145">La `Source` propriété définit l’URI initial affiché dans le contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="ec023-145">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span> <span data-ttu-id="ec023-146">Définissez la propriété source sur</span><span class="sxs-lookup"><span data-stu-id="ec023-146">Set the Source property to</span></span> <https://www.microsoft.com>
    
    :::image type="complex" source="./media/winforms-source.png" alt-text="Gérer les packages NuGet":::
       <span data-ttu-id="ec023-148">Propriété source du contrôle WebView2</span><span class="sxs-lookup"><span data-stu-id="ec023-148">The Source property of the WebView2 control</span></span> :::image-end:::

<span data-ttu-id="ec023-149">Sélectionnez `F5` pour générer et exécuter votre projet.</span><span class="sxs-lookup"><span data-stu-id="ec023-149">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="ec023-150">Vérifiez que votre contrôle WebView2 s’affiche [https://www.microsoft.com](https://www.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="ec023-150">Confirm that your WebView2 control displays [https://www.microsoft.com](https://www.microsoft.com).</span></span>

![hellowebview](./media/winforms-hellowebview.png)

> [!NOTE]
> <span data-ttu-id="ec023-152">Si vous travaillez sur un moniteur haute résolution, il est possible que vous deviez [configurer votre application Windows Forms pour la prise en charge des résolutions élevées](/dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support).</span><span class="sxs-lookup"><span data-stu-id="ec023-152">If you are working on a high DPI monitor, you may have to [configure your Windows Forms app for high DPI support](/dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support).</span></span>

## <span data-ttu-id="ec023-153">Étape 4: gérer les événements de redimensionnement de la fenêtre</span><span class="sxs-lookup"><span data-stu-id="ec023-153">Step 4 - Handle Window Resize Events</span></span>

<span data-ttu-id="ec023-154">Ajoutez quelques contrôles supplémentaires à vos formulaires Windows à partir de la boîte à outils, puis gérez les événements de redimensionnement de fenêtre de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="ec023-154">Add a few more controls to your Windows Forms from the toolbox, and then handle window resize events appropriately.</span></span>

1. <span data-ttu-id="ec023-155">Dans le **Concepteur Windows Forms** , ouvrez la **boîte à outils**</span><span class="sxs-lookup"><span data-stu-id="ec023-155">In the **Windows Forms Designer** open the **Toolbox**</span></span>
1. <span data-ttu-id="ec023-156">Faites glisser et déposez un **contrôle TextBox** dans l’application Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="ec023-156">Drag and Drop a **TextBox** into the Windows Forms App.</span></span> <span data-ttu-id="ec023-157">Nommez le **contrôle TextBox** `addressBar` dans l' **onglet Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="ec023-157">Name the **TextBox** `addressBar` in the **Properties Tab**.</span></span>
1. <span data-ttu-id="ec023-158">Faites glisser et déposez un **bouton** dans l’application Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="ec023-158">Drag and Drop a **Button** into the Windows Forms App.</span></span> <span data-ttu-id="ec023-159">Modifiez le texte du **bouton** `Go!` et nommez-le **Button** `goButton` dans l' **onglet Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="ec023-159">Change the text in the **Button** to `Go!` and name the **Button** `goButton` in the **Properties Tab**.</span></span>

    <span data-ttu-id="ec023-160">Dans le concepteur, l’application doit ressembler à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="ec023-160">The app should look like the following in the designer:</span></span>
    
    ![concepteur](./media/winforms-designer.png)

1. <span data-ttu-id="ec023-162">Dans **Form1.cs** , définissez `Form_Resize` l’emplacement des contrôles lorsque la fenêtre de l’application est redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="ec023-162">In **Form1.cs** define `Form_Resize` to keep the controls in place when the App Window is resized.</span></span>

```csharp
public Form1()
{
    InitializeComponent();
    this.Resize += new System.EventHandler(this.Form_Resize);
}

private void Form_Resize(object sender, EventArgs e)
{
    webView.Size = this.ClientSize - new System.Drawing.Size(webView.Location);
    goButton.Left = this.ClientSize.Width - goButton.Width;
    addressBar.Width = goButton.Left - addressBar.Left;
}
```

<span data-ttu-id="ec023-163">Sélectionnez `F5` pour générer et exécuter votre projet.</span><span class="sxs-lookup"><span data-stu-id="ec023-163">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="ec023-164">Vérifiez que l’application s’affiche comme dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="ec023-164">Confirm that the app displays similar to the following screenshot.</span></span>

![application](./media/winforms-app.png)

## <span data-ttu-id="ec023-166">Étape 5: navigation</span><span class="sxs-lookup"><span data-stu-id="ec023-166">Step 5 - Navigation</span></span>

<span data-ttu-id="ec023-167">Ajoutez la possibilité d’autoriser les utilisateurs à modifier l’URL d’affichage du contrôle WebView2 en ajoutant une barre d’adresse à l’application.</span><span class="sxs-lookup"><span data-stu-id="ec023-167">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1. <span data-ttu-id="ec023-168">Dans `Form1.cs` Ajouter l' `CoreWebView2` espace de noms en insérant l’extrait de code suivant en haut de `Form1.cs` .</span><span class="sxs-lookup"><span data-stu-id="ec023-168">In `Form1.cs` add the `CoreWebView2` namespace by inserting the following code snippet at the top of `Form1.cs`.</span></span>  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

1. <span data-ttu-id="ec023-169">Dans le **Concepteur Windows Forms**, double-cliquez sur le `Go!` bouton pour créer la `goButton_Click` méthode `Form1.cs` .</span><span class="sxs-lookup"><span data-stu-id="ec023-169">In the **Windows Forms Designer**, double-click on the `Go!` button to create the `goButton_Click` method in `Form1.cs`.</span></span> <span data-ttu-id="ec023-170">Copiez et collez l’extrait de code suivant dans la fonction.</span><span class="sxs-lookup"><span data-stu-id="ec023-170">Copy and paste the following snippet inside the function.</span></span> <span data-ttu-id="ec023-171">À présent, la `goButton_Click` fonction navigue vers l’URL entrée dans la barre d’adresses de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="ec023-171">Now, the `goButton_Click` function navigates the WebView to the URL entered in the address bar.</span></span>

    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

<span data-ttu-id="ec023-172">Sélectionnez `F5` pour générer et exécuter votre projet.</span><span class="sxs-lookup"><span data-stu-id="ec023-172">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="ec023-173">Entrez une nouvelle URL dans la barre d’adresses, puis cliquez sur **atteindre**.</span><span class="sxs-lookup"><span data-stu-id="ec023-173">Enter a new URL in the address bar, and click **Go**.</span></span>  <span data-ttu-id="ec023-174">Par exemple, entrez `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="ec023-174">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="ec023-175">Vérifiez que le contrôle WebView2 accède à l’URL.</span><span class="sxs-lookup"><span data-stu-id="ec023-175">Confirm that the WebView2 control navigates to the URL.</span></span>  

> [!NOTE]
> <span data-ttu-id="ec023-176">Vérifiez qu’une URL complète est entrée dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="ec023-176">Ensure a complete URL is entered in the address bar.</span></span> <span data-ttu-id="ec023-177">`ArgumentException`A est levé si l’URL ne commence pas par `http://` ou</span><span class="sxs-lookup"><span data-stu-id="ec023-177">An `ArgumentException` is thrown if the URL does not start with `http://` or</span></span> `https://`

![bing](./media/winforms-bing.png)

## <span data-ttu-id="ec023-179">Étape 6: événements de navigation</span><span class="sxs-lookup"><span data-stu-id="ec023-179">Step 6 - Navigation events</span></span>  

<span data-ttu-id="ec023-180">L’application qui héberge les contrôles WebView2 écoute les événements suivants qui sont déclenchés par le contrôle WebView2 lors de la navigation dans les pages Web.</span><span class="sxs-lookup"><span data-stu-id="ec023-180">The application that hosts WebView2 controls listens to the following events that are raised by the WebView2 control during navigation to web pages.</span></span>  

* `NavigationStarting`  
* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  
* `NavigationCompleted`  

<span data-ttu-id="ec023-181">Pour plus d’informations, voir [événements de navigation](../concepts/navigation-events.md).</span><span class="sxs-lookup"><span data-stu-id="ec023-181">For more information, see [Navigation Events](../concepts/navigation-events.md).</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Gérer les packages NuGet":::
   <span data-ttu-id="ec023-183">Événements de navigation</span><span class="sxs-lookup"><span data-stu-id="ec023-183">Navigation events</span></span>
:::image-end:::

<span data-ttu-id="ec023-184">Lorsqu’une erreur se produit, les événements suivants sont déclenchés et peut dépendre de la navigation sur une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ec023-184">When an error occurs, the following events are raised and may depend on navigation to an error page.</span></span>  

* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  

<span data-ttu-id="ec023-185">S’il existe une redirection HTTP, il existe plusieurs `NavigationStarting` événements.</span><span class="sxs-lookup"><span data-stu-id="ec023-185">When there is an HTTP redirect, there are multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="ec023-186">Pour illustrer l’utilisation de ces événements, commencez par enregistrer un gestionnaire pour `NavigationStarting` cela annule toutes les demandes qui n’utilisent pas HTTPS.</span><span class="sxs-lookup"><span data-stu-id="ec023-186">To demonstrate how to use these events, start by registering a handler for `NavigationStarting` that cancels any requests that do not use HTTPS.</span></span>  

<span data-ttu-id="ec023-187">Dans `Form1.cs` , modifiez le constructeur comme illustré ci-dessous, puis ajoutez la `EnsureHttps` fonction.</span><span class="sxs-lookup"><span data-stu-id="ec023-187">In `Form1.cs`, modify the constructor as shown below and add the `EnsureHttps` function.</span></span>  

```csharp
public Form1()
{
    InitializeComponent();
    this.Resize += new System.EventHandler(this.Form_Resize);

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

<span data-ttu-id="ec023-188">Dans le constructeur, EnsureHttps est enregistré en tant que gestionnaire d’événements sur l' `NavigationStarting` événement sur le contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="ec023-188">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="ec023-189">Sélectionnez `F5` pour générer et exécuter votre projet.</span><span class="sxs-lookup"><span data-stu-id="ec023-189">Select `F5` to build and run your project.</span></span> <span data-ttu-id="ec023-190">Confirmez que lorsque vous naviguez vers un site HTTP, le WebView reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="ec023-190">Confirm that when navigating to an HTTP site, the WebView remains unchanged.</span></span> <span data-ttu-id="ec023-191">Toutefois, le WebView accède aux sites HTTPs.</span><span class="sxs-lookup"><span data-stu-id="ec023-191">However, the WebView will navigate to HTTPS sites.</span></span>

## <span data-ttu-id="ec023-192">Étape 7: création de scripts</span><span class="sxs-lookup"><span data-stu-id="ec023-192">Step 7 - Scripting</span></span>  

<span data-ttu-id="ec023-193">Vous pouvez utiliser des applications hôtes pour injecter du code JavaScript dans les contrôles WebView2 lors de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="ec023-193">You may use host applications to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="ec023-194">Le JavaScript injecté s’applique à tous les nouveaux documents de niveau supérieur ainsi qu’à toute image enfant jusqu’à ce que le JavaScript soit supprimé.</span><span class="sxs-lookup"><span data-stu-id="ec023-194">The injected JavaScript applies to all new top level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="ec023-195">Le JavaScript injecté est exécuté après la création de l’objet global et avant l’exécution de tout autre script inclus dans le document HTML.</span><span class="sxs-lookup"><span data-stu-id="ec023-195">The injected JavaScript is run after creation of the global object, and before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="ec023-196">Vous pouvez utiliser les scripts pour alerter l’utilisateur lorsque vous naviguez vers un site non HTTPs.</span><span class="sxs-lookup"><span data-stu-id="ec023-196">You can use scripting to alert the user when navigating to a non-HTTPS site.</span></span>  <span data-ttu-id="ec023-197">Modifiez la `EnsureHttps` fonction de telle sorte qu’elle injecte le script dans le contenu Web à l’aide de la méthode [ExecuteScriptAsync]() .</span><span class="sxs-lookup"><span data-stu-id="ec023-197">Modify the `EnsureHttps` function so that it injects script into the web content using the [ExecuteScriptAsync]() method.</span></span>  

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

<span data-ttu-id="ec023-198">Sélectionnez `F5` pour générer et exécuter votre projet.</span><span class="sxs-lookup"><span data-stu-id="ec023-198">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="ec023-199">Vérifiez que l’application affiche une alerte lorsque vous naviguez vers un site qui n’utilise pas HTTPs.</span><span class="sxs-lookup"><span data-stu-id="ec023-199">Confirm that the application displays an alert when you navigate to a site that does not use HTTPS.</span></span>  

![https](./media/winforms-https.png)

## <span data-ttu-id="ec023-201">Étape 8: communication entre l’hôte et le contenu Web</span><span class="sxs-lookup"><span data-stu-id="ec023-201">Step 8 - Communication between host and web content</span></span>  

<span data-ttu-id="ec023-202">L’hôte et le contenu Web sont en mesure de communiquer entre eux `postMessage` comme suit:</span><span class="sxs-lookup"><span data-stu-id="ec023-202">The host and web content may communicate with each other using `postMessage` as follows:</span></span>  

* <span data-ttu-id="ec023-203">Le contenu Web d’un contrôle WebView2 risque de publier un message destiné à l’hôte à l’aide de `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="ec023-203">Web content in a WebView2 control may post a message to the host using `window.chrome.webview.postMessage`.</span></span>  <span data-ttu-id="ec023-204">L’hôte gère le message en utilisant tout inscrit `WebMessageReceived` sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="ec023-204">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
* <span data-ttu-id="ec023-205">Héberge les messages dans le contenu Web d’un contrôle WebView2 en utilisant `CoreWebView2.PostWebMessageAsString` ou `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="ec023-205">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="ec023-206">Ces messages sont interceptés par des gestionnaires ajoutés à `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="ec023-206">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="ec023-207">Ce mécanisme de communication permet au contenu Web de transmettre des messages à l’hôte à l’aide de fonctionnalités natives.</span><span class="sxs-lookup"><span data-stu-id="ec023-207">This communication mechanism allows web content to pass messages to the host using native capabilities.</span></span>  

<span data-ttu-id="ec023-208">Dans votre projet, lorsque le contrôle WebView2 navigue vers une URL, il affiche l’URL dans la barre d’adresse et avertit l’utilisateur de l’URL qui s’affiche dans le contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="ec023-208">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1. <span data-ttu-id="ec023-209">Dans **Form1.cs**, mettez à jour votre constructeur et créez une `InitializeAsync` fonction comme illustré dans l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="ec023-209">In **Form1.cs**, update your constructor and create an `InitializeAsync` function as shown in the following code snippet.</span></span>  <span data-ttu-id="ec023-210">La `InitializeAsync` fonction est en attente [EnsureCoreWebView2Async]() , car l’initialisation de `CoreWebView2` est asynchrone.</span><span class="sxs-lookup"><span data-stu-id="ec023-210">The `InitializeAsync` function awaits [EnsureCoreWebView2Async]() because the initialization of `CoreWebView2` is asynchronous.</span></span>  

    ```csharp
    public Form1()
    {
        InitializeComponent();
        this.Resize += new System.EventHandler(this.Form_Resize);
        webView.NavigationStarting += EnsureHttps;
        InitializeAsync();
    }

    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
    }
    ```  

1. <span data-ttu-id="ec023-211">Une fois **CoreWebView2** initialisé, inscrivez un gestionnaire d’événements pour y répondre `WebMessageReceived` .</span><span class="sxs-lookup"><span data-stu-id="ec023-211">After **CoreWebView2** is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="ec023-212">Dans `Form1.cs` Update `InitializeAsync` et ajoutez `UpdateAddressBar` à l’aide de l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="ec023-212">In `Form1.cs` update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  

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

1. <span data-ttu-id="ec023-213">Pour que le WebView envoie le message électronique et y réponde, une fois `CoreWebView2` initialisé, l’hôte injecte un script dans le contenu Web pour:</span><span class="sxs-lookup"><span data-stu-id="ec023-213">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host injects a script in the web content to:</span></span>  

    1. <span data-ttu-id="ec023-214">Envoyez l’URL à l’hôte à l’aide de `postMessage` .</span><span class="sxs-lookup"><span data-stu-id="ec023-214">Send the URL to the host using `postMessage`.</span></span>
    1. <span data-ttu-id="ec023-215">Enregistrez un gestionnaire d’événements pour imprimer un message envoyé à partir de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="ec023-215">Register an event handler to print a message sent from the host.</span></span>  

<span data-ttu-id="ec023-216">Dans `Form1.cs` la mise à jour, `InitializeAsync` procédez comme indiqué dans l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="ec023-216">In `Form1.cs`, update `InitializeAsync` as shown in the following code snippet.</span></span>  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

<span data-ttu-id="ec023-217">Sélectionnez `F5` pour générer et exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="ec023-217">Select `F5` to build and run the app.</span></span>  <span data-ttu-id="ec023-218">Vérifiez que la barre d’adresse affiche l’URL du site affiché dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="ec023-218">Confirm that the address bar displays the URL of the site displayed in the WebView.</span></span> <span data-ttu-id="ec023-219">Par ailleurs, lorsque vous accédez à une nouvelle URL, le WebView avertit l’utilisateur de l’URL affichée dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="ec023-219">Also, when you successfully navigate to a new URL, the WebView alerts the user of the URL displayed in the WebView.</span></span>  

![finalapp](./media/winforms-finalapp.png)

<span data-ttu-id="ec023-221">Félicitations, vous avez créé votre première application WebView2.</span><span class="sxs-lookup"><span data-stu-id="ec023-221">Congratulations, you built your first WebView2 app!</span></span>  

## <span data-ttu-id="ec023-222">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="ec023-222">Next steps</span></span> 

* <span data-ttu-id="ec023-223">Extraire le [référentiel Samples WebView2Samples](https://github.com/MicrosoftEdge/WebView2Samples) pour obtenir un exemple complet de fonctionnalités WebView2's</span><span class="sxs-lookup"><span data-stu-id="ec023-223">Checkout the [WebView2Samples repo](https://github.com/MicrosoftEdge/WebView2Samples) for a comprehensive example of WebView2's capabilities</span></span>
* <span data-ttu-id="ec023-224">Référence sur l' [API](/dotnet/api/microsoft.web.webview2.winforms.webview2) d’extraction pour plus d’informations sur nos API</span><span class="sxs-lookup"><span data-stu-id="ec023-224">Checkout [API reference](/dotnet/api/microsoft.web.webview2.winforms.webview2) for more detailed information about our APIs</span></span>
* <span data-ttu-id="ec023-225">Extraire une liste de [ressources WebView2](../index.md#next-steps) pour en savoir plus sur WebView2</span><span class="sxs-lookup"><span data-stu-id="ec023-225">Checkout a list of [WebView2 Resources](../index.md#next-steps) to learn more about WebView2</span></span>


## <span data-ttu-id="ec023-226">Contacter l’équipe WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ec023-226">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  
