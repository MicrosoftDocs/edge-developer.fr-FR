---
description: Guide de mise en place avec WebView2 pour les applications WinForms
title: Mise en place de WebView2 pour les applications WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, webview, winforms apps, winforms, edge, CoreWebView2, browser control, edge html, getting started, Getting Started, .NET, windows forms
ms.openlocfilehash: 408d225c6c0abe54483226e7004a386d367d65ab
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536407"
---
# <a name="getting-started-with-webview2-in-windows-forms"></a><span data-ttu-id="779c9-104">Mise en place de WebView2 dans Windows Forms</span><span class="sxs-lookup"><span data-stu-id="779c9-104">Getting started with WebView2 in Windows Forms</span></span>

<span data-ttu-id="779c9-105">Dans cet article, commencer à créer votre première application WebView2 et en savoir plus sur les principales fonctionnalités de [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span><span class="sxs-lookup"><span data-stu-id="779c9-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="779c9-106">Pour plus d’informations sur les API individuelles, accédez à la [référence d’API.][DotnetApiMicrosoftWebWebview2Winforms]</span><span class="sxs-lookup"><span data-stu-id="779c9-106">For more information on individual APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2Winforms].</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="779c9-107">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="779c9-107">Prerequisites</span></span>  

<span data-ttu-id="779c9-108">Veillez à installer la liste des conditions préalables suivante avant de poursuivre.</span><span class="sxs-lookup"><span data-stu-id="779c9-108">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="779c9-109">[WebView2 Runtime][MicrosoftDeveloperMicrosoftEdgeWebview2] ou tout canal [Microsoft Edge (Chromium) non stable][MicrosoftedgeinsiderDownload] installé sur le système d’exploitation pris en charge \(actuellement Windows 10, Windows 8.1 et Windows 7\).</span><span class="sxs-lookup"><span data-stu-id="779c9-109">[WebView2 Runtime][MicrosoftDeveloperMicrosoftEdgeWebview2] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="779c9-110">L’équipe WebView recommande d’utiliser le canal Canary et la version minimale requise est 82.0.488.0.</span><span class="sxs-lookup"><span data-stu-id="779c9-110">The WebView team recommends using the Canary channel and the minimum required version is 82.0.488.0.</span></span>  
    
*   <span data-ttu-id="779c9-111">[Visual Studio][MicrosoftVisualstudioMain] 2017 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="779c9-111">[Visual Studio][MicrosoftVisualstudioMain] 2017 or later.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="779c9-112">WebView2 ne prend actuellement pas en charge les concepteurs .NET 5 et .NET Core.</span><span class="sxs-lookup"><span data-stu-id="779c9-112">WebView2 currently does not support the .NET 5 and .NET Core designers.</span></span>  

## <a name="step-1---create-a-single-window-app"></a><span data-ttu-id="779c9-113">Étape 1 : créer une application à fenêtre unique</span><span class="sxs-lookup"><span data-stu-id="779c9-113">Step 1 - Create a single-window app</span></span>

<span data-ttu-id="779c9-114">Commencez par un projet de bureau de base qui contient une seule fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="779c9-114">Start with a basic desktop project that contains a single main window.</span></span>  

1.  <span data-ttu-id="779c9-115">In Visual Studio, choose **Windows Forms .NET Framework App**  >  **Next**.</span><span class="sxs-lookup"><span data-stu-id="779c9-115">In Visual Studio, choose **Windows Forms .NET Framework App** > **Next**.</span></span>
    
    :::image type="complex" source="./media/winforms-newproject.png" alt-text="Nouveau projet" lightbox="./media/winforms-newproject.png":::
       <span data-ttu-id="779c9-117">Nouveau projet</span><span class="sxs-lookup"><span data-stu-id="779c9-117">New project</span></span>  
    :::image-end:::
    
1.  <span data-ttu-id="779c9-118">Entrez des valeurs **pour Project nom et** **emplacement.**</span><span class="sxs-lookup"><span data-stu-id="779c9-118">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="779c9-119">Choisissez **.NET Framework 4.6.2 ou ultérieure.**</span><span class="sxs-lookup"><span data-stu-id="779c9-119">Choose **.NET Framework 4.6.2** or later.</span></span>  
    
    :::image type="complex" source="./media/winforms-startproj.png" alt-text="Démarrer le projet" lightbox="./media/winforms-startproj.png":::
       <span data-ttu-id="779c9-121">Démarrer le projet</span><span class="sxs-lookup"><span data-stu-id="779c9-121">Start project</span></span>  
    :::image-end:::
    
1.  <span data-ttu-id="779c9-122">Pour créer votre projet, choisissez **Créer.**</span><span class="sxs-lookup"><span data-stu-id="779c9-122">To create your project, choose **Create**.</span></span>
    
## <a name="step-2---install-webview2-sdk"></a><span data-ttu-id="779c9-123">Étape 2 : installer le SDK WebView2</span><span class="sxs-lookup"><span data-stu-id="779c9-123">Step 2 - Install WebView2 SDK</span></span>

<span data-ttu-id="779c9-124">Utilisez NuGet pour ajouter le SDK WebView2 au projet.</span><span class="sxs-lookup"><span data-stu-id="779c9-124">Use NuGet to add the WebView2 SDK to the project.</span></span>  

1.  <span data-ttu-id="779c9-125">Pointez sur le projet, ouvrez le menu contextuel \(clic droit\), puis choisissez **Gérer NuGet packages...**.</span><span class="sxs-lookup"><span data-stu-id="779c9-125">Hover on the project, open the contextual menu \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Gérer NuGet packages":::
       <span data-ttu-id="779c9-127">Gérer NuGet packages</span><span class="sxs-lookup"><span data-stu-id="779c9-127">Manage NuGet Packages</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="779c9-128">Dans la barre de recherche, `Microsoft.Web.WebView2` tapez > **choisissez Microsoft.Web.WebView2**.</span><span class="sxs-lookup"><span data-stu-id="779c9-128">In the search bar, type `Microsoft.Web.WebView2` > choose **Microsoft.Web.WebView2**.</span></span>  
    
    :::image type="complex" source="./media/installnuget.png" alt-text="NuGet" lightbox="./media/installnuget.png":::
       <span data-ttu-id="779c9-130">NuGet</span><span class="sxs-lookup"><span data-stu-id="779c9-130">NuGet</span></span>  
    :::image-end:::
    
    <span data-ttu-id="779c9-131">Commencez à développer des applications à l’aide de l’API WebView2.</span><span class="sxs-lookup"><span data-stu-id="779c9-131">Start developing apps using the WebView2 API.</span></span>  <span data-ttu-id="779c9-132">Pour créer et exécuter le projet, sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="779c9-132">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="779c9-133">Le projet en cours d’exécution affiche une fenêtre vide.</span><span class="sxs-lookup"><span data-stu-id="779c9-133">The running project displays an empty window.</span></span>  
    
    :::image type="complex" source="./media/winforms-emptyapp.png" alt-text="Application vide" lightbox="./media/winforms-emptyapp.png":::
       <span data-ttu-id="779c9-135">Application vide</span><span class="sxs-lookup"><span data-stu-id="779c9-135">Empty app</span></span>  
    :::image-end:::
    
## <a name="step-3---create-a-single-webview"></a><span data-ttu-id="779c9-136">Étape 3 : créer un seul WebView</span><span class="sxs-lookup"><span data-stu-id="779c9-136">Step 3 - Create a single WebView</span></span>  

<span data-ttu-id="779c9-137">Ajoutez un WebView à votre application.</span><span class="sxs-lookup"><span data-stu-id="779c9-137">Add a WebView to your app.</span></span>  

1.  <span data-ttu-id="779c9-138">Ouvrez **le Windows Forms Designer.**</span><span class="sxs-lookup"><span data-stu-id="779c9-138">Open the **Windows Forms Designer**.</span></span>  
1.  <span data-ttu-id="779c9-139">Recherchez **WebView2 dans** la boîte **à outils.**</span><span class="sxs-lookup"><span data-stu-id="779c9-139">Search for **WebView2** in the **Toolbox**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="779c9-140">Si vous utilisez Visual Studio 2017, il se peut que **WebView2** ne s’affiche pas dans la **boîte à outils.**</span><span class="sxs-lookup"><span data-stu-id="779c9-140">If you are using Visual Studio 2017, by default **WebView2** may not display in the **Toolbox**.</span></span>  <span data-ttu-id="779c9-141">Pour activer le comportement, **sélectionnez**  >  **Options**d’outils  >  \*\*\*\* > \*\*\*\* définir le paramètre Boîte à outils Remplir automatiquement sur `True` .</span><span class="sxs-lookup"><span data-stu-id="779c9-141">To enable the behavior, choose **Tools** > **Options** > **General** > set the **Automatically Populate Toolbox** setting to `True`.</span></span>  
    
    <span data-ttu-id="779c9-142">Faites glisser et déposez **le contrôle WebView2** dans l’Windows Forms App.</span><span class="sxs-lookup"><span data-stu-id="779c9-142">Drag and drop the **WebView2** control into the Windows Forms App.</span></span>
    
    :::image type="complex" source="./media/winforms-toolbox.png" alt-text="Boîte à outils affichant WebView2":::
       <span data-ttu-id="779c9-144">Boîte à outils affichant WebView2</span><span class="sxs-lookup"><span data-stu-id="779c9-144">Toolbox displaying WebView2</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="779c9-145">Définissez `(Name)` la propriété sur `webView` .</span><span class="sxs-lookup"><span data-stu-id="779c9-145">Set the `(Name)` property to `webView`.</span></span>
    
    :::image type="complex" source="./media/winforms-properties.png" alt-text="Propriétés du contrôle WebView2":::
       <span data-ttu-id="779c9-147">Propriétés du contrôle WebView2</span><span class="sxs-lookup"><span data-stu-id="779c9-147">Properties of the WebView2 control</span></span>
    :::image-end:::

1.  <span data-ttu-id="779c9-148">La `Source` propriété définit l’URI initial affiché dans le contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="779c9-148">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  <span data-ttu-id="779c9-149">Définissez `Source` la propriété sur `https://www.microsoft.com` .</span><span class="sxs-lookup"><span data-stu-id="779c9-149">Set the `Source` property to `https://www.microsoft.com`.</span></span>  
    
    :::image type="complex" source="./media/winforms-source.png" alt-text="Propriété Source du contrôle WebView2":::
       <span data-ttu-id="779c9-151">Propriété **Source** du contrôle WebView2</span><span class="sxs-lookup"><span data-stu-id="779c9-151">The **Source** property of the WebView2 control</span></span>
    :::image-end:::  

<span data-ttu-id="779c9-152">Pour créer et exécuter votre projet, sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="779c9-152">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="779c9-153">Assurez-vous que votre contrôle WebView2 [https://www.microsoft.com][|::ref1::|Main] s’affiche.</span><span class="sxs-lookup"><span data-stu-id="779c9-153">Ensure your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>

:::image type="complex" source="./media/winforms-hellowebview.png" alt-text="hello webview" lightbox="./media/winforms-hellowebview.png":::
   <span data-ttu-id="779c9-155">hello webview</span><span class="sxs-lookup"><span data-stu-id="779c9-155">hello webview</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="779c9-156">Si vous travaillez sur un moniteur HAUTE DPI, vous de devez configurer votre application Windows Forms pour une prise en charge [haute DPI.][DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]</span><span class="sxs-lookup"><span data-stu-id="779c9-156">If you are working on a high DPI monitor, you may have to [configure your Windows Forms app for high DPI support][DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport].</span></span>  

## <a name="step-4---handle-window-resize-events"></a><span data-ttu-id="779c9-157">Étape 4 : gérer les événements de resize de fenêtre</span><span class="sxs-lookup"><span data-stu-id="779c9-157">Step 4 - Handle Window Resize Events</span></span>  

<span data-ttu-id="779c9-158">Ajoutez quelques contrôles à votre Windows formulaires à partir de la boîte à outils, puis traitez les événements de re resize de fenêtre de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="779c9-158">Add a few more controls to your Windows Forms from the toolbox, and then handle window resize events appropriately.</span></span>  

1.  <span data-ttu-id="779c9-159">Dans le **Windows Forms Designer,** ouvrez la **boîte à outils.**</span><span class="sxs-lookup"><span data-stu-id="779c9-159">In the **Windows Forms Designer**, open the **Toolbox**.</span></span>  
1.  <span data-ttu-id="779c9-160">Faites glisser et déposez **un textbox** dans l’Windows Forms App.</span><span class="sxs-lookup"><span data-stu-id="779c9-160">Drag and Drop a **TextBox** into the Windows Forms App.</span></span>  <span data-ttu-id="779c9-161">Nommez **le textbox dans** `addressBar` **l’onglet Propriétés.**</span><span class="sxs-lookup"><span data-stu-id="779c9-161">Name the **TextBox** `addressBar` in the **Properties Tab**.</span></span>  
1.  <span data-ttu-id="779c9-162">Faites glisser un bouton **vers l’Windows** Forms.</span><span class="sxs-lookup"><span data-stu-id="779c9-162">Drag and Drop a **Button** into the Windows Forms App.</span></span>  <span data-ttu-id="779c9-163">Modifiez le texte du **bouton et** `Go!` nommez-le **dans** `goButton` l’onglet **Propriétés.**</span><span class="sxs-lookup"><span data-stu-id="779c9-163">Change the text in the **Button** to `Go!` and name the **Button** `goButton` in the **Properties Tab**.</span></span>  
    
    <span data-ttu-id="779c9-164">L’application doit ressembler à l’image suivante dans le concepteur.</span><span class="sxs-lookup"><span data-stu-id="779c9-164">The app should look like the following image in the designer.</span></span>  
    
    :::image type="complex" source="./media/winforms-designer.png" alt-text="Concepteur WinForms" lightbox="./media/winforms-designer.png":::
       <span data-ttu-id="779c9-166">Concepteur WinForms</span><span class="sxs-lookup"><span data-stu-id="779c9-166">WinForms designer</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="779c9-167">Dans le `Form1.cs` fichier, `Form_Resize` définissez pour conserver les contrôles en place lorsque la fenêtre de l’application est re resserée.</span><span class="sxs-lookup"><span data-stu-id="779c9-167">In the `Form1.cs` file, define `Form_Resize` to keep the controls in place when the App Window is resized.</span></span>

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

<span data-ttu-id="779c9-168">Pour créer et exécuter votre projet, sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="779c9-168">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="779c9-169">Assurez-vous que l’application s’affiche comme dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="779c9-169">Ensure the app displays similar to the following screenshot.</span></span>

:::image type="complex" source="./media/winforms-app.png" alt-text="application" lightbox="./media/winforms-app.png":::
   <span data-ttu-id="779c9-171">Application</span><span class="sxs-lookup"><span data-stu-id="779c9-171">App</span></span>  
:::image-end:::

## <a name="step-5---navigation"></a><span data-ttu-id="779c9-172">Étape 5 : navigation</span><span class="sxs-lookup"><span data-stu-id="779c9-172">Step 5 - Navigation</span></span>

<span data-ttu-id="779c9-173">Ajoutez la possibilité d’autoriser les utilisateurs à modifier l’URL affichée par le contrôle WebView2 en ajoutant une barre d’adresse à l’application.</span><span class="sxs-lookup"><span data-stu-id="779c9-173">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>  

1.  <span data-ttu-id="779c9-174">Sélectionnez `F5` pour créer et exécuter votre projet.</span><span class="sxs-lookup"><span data-stu-id="779c9-174">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="779c9-175">Confirmez que l’application s’affiche comme dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="779c9-175">Confirm that the app displays similar to the following screenshot.</span></span>  
    
    :::image type="complex" source="./media/winforms-app.png" alt-text="Application WinForms" lightbox="./media/winforms-app.png":::
       <span data-ttu-id="779c9-177">Application WinForms</span><span class="sxs-lookup"><span data-stu-id="779c9-177">WinForms App</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="779c9-178">Dans le `Form1.cs` fichier, pour ajouter l’espace de noms, insérez l’extrait de code suivant `CoreWebView2` en haut.</span><span class="sxs-lookup"><span data-stu-id="779c9-178">In the `Form1.cs`file, to add the `CoreWebView2` namespace, insert the following code snippet at the top.</span></span>  

1.  <span data-ttu-id="779c9-179">In `Form1.cs` add the `CoreWebView2` namespace by inserting the following code snippet at the top of `Form1.cs` .</span><span class="sxs-lookup"><span data-stu-id="779c9-179">In `Form1.cs` add the `CoreWebView2` namespace by inserting the following code snippet at the top of `Form1.cs`.</span></span>  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

1.  <span data-ttu-id="779c9-180">Dans le **Windows Forms Designer,** double-cliquez sur le `Go!` bouton pour créer la méthode dans le `goButton_Click` `Form1.cs` fichier.</span><span class="sxs-lookup"><span data-stu-id="779c9-180">In the **Windows Forms Designer**, double-click on the `Go!` button to create the `goButton_Click` method in the `Form1.cs` file.</span></span>  <span data-ttu-id="779c9-181">Copiez et collez l’extrait de code suivant à l’intérieur de la fonction.</span><span class="sxs-lookup"><span data-stu-id="779c9-181">Copy and paste the following snippet inside the function.</span></span>  <span data-ttu-id="779c9-182">À présent, `goButton_Click` la fonction navigue dans le WebView jusqu’à l’URL entrée dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="779c9-182">Now, the `goButton_Click` function navigates the WebView to the URL entered in the address bar.</span></span>

    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

<span data-ttu-id="779c9-183">Pour créer et exécuter votre projet, sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="779c9-183">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="779c9-184">Entrez une nouvelle URL dans la barre d’adresses, puis sélectionnez **Go**.</span><span class="sxs-lookup"><span data-stu-id="779c9-184">Enter a new URL in the address bar, and select **Go**.</span></span>  <span data-ttu-id="779c9-185">Par exemple, entrez `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="779c9-185">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="779c9-186">Assurez-vous que le contrôle WebView2 navigue jusqu’à l’URL.</span><span class="sxs-lookup"><span data-stu-id="779c9-186">Ensure the WebView2 control navigates to the URL.</span></span>  

> [!NOTE]
> <span data-ttu-id="779c9-187">Assurez-vous qu’une URL complète est entrée dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="779c9-187">Ensure a complete URL is entered in the address bar.</span></span>  <span data-ttu-id="779c9-188">Une `ArgumentException` url est lancée si l’URL ne commence pas par `http://` ou</span><span class="sxs-lookup"><span data-stu-id="779c9-188">An `ArgumentException` is thrown if the URL does not start with `http://` or</span></span> `https://`

:::image type="complex" source="./media/winforms-bing.png" alt-text="bing.com" lightbox="./media/winforms-bing.png":::
   <span data-ttu-id="779c9-190">bing.com</span><span class="sxs-lookup"><span data-stu-id="779c9-190">bing.com</span></span>  
:::image-end:::

## <a name="step-6---navigation-events"></a><span data-ttu-id="779c9-191">Étape 6 : événements de navigation</span><span class="sxs-lookup"><span data-stu-id="779c9-191">Step 6 - Navigation events</span></span>  

<span data-ttu-id="779c9-192">Lors de la navigation sur la page web, le contrôle WebView2 lève des événements.</span><span class="sxs-lookup"><span data-stu-id="779c9-192">During webpage navigation, the WebView2 control raises events.</span></span>  <span data-ttu-id="779c9-193">L’application qui héberge les contrôles WebView2 écoute les événements suivants.</span><span class="sxs-lookup"><span data-stu-id="779c9-193">The app that hosts WebView2 controls listens for the following events.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

<span data-ttu-id="779c9-194">Pour plus d’informations, accédez à [Événements de navigation.][Webview2ConceptsNavigationEvents]</span><span class="sxs-lookup"><span data-stu-id="779c9-194">For more information, navigate to [Navigation Events][Webview2ConceptsNavigationEvents].</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Événements de navigation":::
   <span data-ttu-id="779c9-196">Événements de navigation</span><span class="sxs-lookup"><span data-stu-id="779c9-196">Navigation events</span></span>
:::image-end:::

<span data-ttu-id="779c9-197">Lorsqu’une erreur se produit, les événements suivants sont élevés et peuvent dépendre de la navigation vers une page web d’erreur.</span><span class="sxs-lookup"><span data-stu-id="779c9-197">When an error occurs, the following events are raised and may depend on navigation to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

> [!NOTE]
> <span data-ttu-id="779c9-198">Si une redirection HTTP se produit, il existe plusieurs `NavigationStarting` événements dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="779c9-198">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="779c9-199">Pour montrer comment utiliser les événements, commencez par inscrire un responsable pour annuler toutes les demandes n’utilisant `NavigationStarting` pas HTTPS.</span><span class="sxs-lookup"><span data-stu-id="779c9-199">To demonstrate how to use the events, start by registering a handler for `NavigationStarting` that cancels any requests not using HTTPS.</span></span>  

<span data-ttu-id="779c9-200">Dans le fichier, mettez à jour le constructeur pour qu’il corresponde à l’extrait de code suivant `Form1.cs` et ajoutez la `EnsureHttps` fonction.</span><span class="sxs-lookup"><span data-stu-id="779c9-200">In the `Form1.cs` file, update the constructor to match the following code snippet and add the `EnsureHttps` function.</span></span>  

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

<span data-ttu-id="779c9-201">Dans le constructeur, est inscrit en tant que le `EnsureHttps` handler d’événements sur `NavigationStarting` l’événement sur le contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="779c9-201">In the constructor, `EnsureHttps` is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="779c9-202">Pour créer et exécuter votre projet, sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="779c9-202">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="779c9-203">Assurez-vous que lorsque vous naviguez vers un site HTTP, le WebView reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="779c9-203">Ensure when navigating to an HTTP site, the WebView remains unchanged.</span></span>  <span data-ttu-id="779c9-204">Toutefois, le WebView naviguera vers les sites HTTPS.</span><span class="sxs-lookup"><span data-stu-id="779c9-204">However, the WebView will navigate to HTTPS sites.</span></span>

## <a name="step-7---scripting"></a><span data-ttu-id="779c9-205">Étape 7 : scripts</span><span class="sxs-lookup"><span data-stu-id="779c9-205">Step 7 - Scripting</span></span>  

<span data-ttu-id="779c9-206">Vous pouvez utiliser des applications hôtes pour injecter du code JavaScript dans des contrôles WebView2 lors de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="779c9-206">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="779c9-207">Vous pouvez tâcher WebView pour exécuter du javaScript arbitraire ou ajouter des scripts d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="779c9-207">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="779c9-208">Le javaScript injecté s’applique à tous les nouveaux documents de niveau supérieur et aux images enfants jusqu’à ce que le JavaScript soit supprimé.</span><span class="sxs-lookup"><span data-stu-id="779c9-208">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="779c9-209">Le javaScript injecté est exécuté avec un minutage spécifique.</span><span class="sxs-lookup"><span data-stu-id="779c9-209">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="779c9-210">Exécutez-le après la création de l’objet global.</span><span class="sxs-lookup"><span data-stu-id="779c9-210">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="779c9-211">Exécutez-le avant d’exécuter tout autre script inclus dans le document HTML.</span><span class="sxs-lookup"><span data-stu-id="779c9-211">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="779c9-212">Par exemple, ajoutez des scripts qui envoient une alerte lorsqu’un utilisateur navigue vers des sites non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="779c9-212">As an example, add scripts that send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="779c9-213">Modifiez la fonction pour injecter un script dans le contenu web qui utilise la méthode `EnsureHttps` [ExecuteScriptAsync.][DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync]</span><span class="sxs-lookup"><span data-stu-id="779c9-213">Modify the `EnsureHttps` function to inject a script into the web content that uses [ExecuteScriptAsync][DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync] method.</span></span>  

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

<span data-ttu-id="779c9-214">Pour créer et exécuter votre projet, sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="779c9-214">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="779c9-215">Assurez-vous que l’application affiche une alerte lorsque vous accédez à un site web qui n’utilise pas HTTPS.</span><span class="sxs-lookup"><span data-stu-id="779c9-215">Ensure the app displays an alert when you navigate to a website that doesn't use HTTPS.</span></span>  

:::image type="complex" source="./media/winforms-https.png" alt-text="https" lightbox="./media/winforms-https.png":::
   <span data-ttu-id="779c9-217">https</span><span class="sxs-lookup"><span data-stu-id="779c9-217">https</span></span>  
:::image-end:::

## <a name="step-8---communication-between-host-and-web-content"></a><span data-ttu-id="779c9-218">Étape 8 : communication entre le contenu hôte et le contenu web</span><span class="sxs-lookup"><span data-stu-id="779c9-218">Step 8 - Communication between host and web content</span></span>  

<span data-ttu-id="779c9-219">Le contenu hôte et web peut être utilisé pour communiquer les uns avec les `postMessage` autres comme suit :</span><span class="sxs-lookup"><span data-stu-id="779c9-219">The host and web content may use `postMessage` to communicate with each other as follows:</span></span>  

*   <span data-ttu-id="779c9-220">Le contenu Web d’un contrôle WebView2 peut être `window.chrome.webview.postMessage` utilisé pour publier un message à l’hôte.</span><span class="sxs-lookup"><span data-stu-id="779c9-220">Web content in a WebView2 control may use `window.chrome.webview.postMessage` to post a message to the host.</span></span>  <span data-ttu-id="779c9-221">L’hôte gère le message à l’aide de tous les messages `WebMessageReceived` enregistrés sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="779c9-221">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
*   <span data-ttu-id="779c9-222">Héberge des messages publiés dans du contenu web dans un contrôle WebView2 à l’aide `CoreWebView2.PostWebMessageAsString` ou `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="779c9-222">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="779c9-223">Ces messages sont capturés par des responsables ajoutés à `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="779c9-223">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="779c9-224">Le mécanisme de communication transmet les messages du contenu web à l’hôte à l’aide de fonctionnalités natives.</span><span class="sxs-lookup"><span data-stu-id="779c9-224">The communication mechanism passes messages from web content to the host using native capabilities.</span></span>  

<span data-ttu-id="779c9-225">Dans votre projet, lorsque le contrôle WebView2 navigue vers une URL, il affiche l’URL dans la barre d’adresses et avertit l’utilisateur de l’URL affichée dans le contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="779c9-225">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1.  <span data-ttu-id="779c9-226">Dans le fichier, mettez à jour votre constructeur et `Form1.cs` créez `InitializeAsync` une fonction pour qu’elle corresponde à l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="779c9-226">In the `Form1.cs` file, update your constructor and create an `InitializeAsync` function to match the following code snippet.</span></span>  <span data-ttu-id="779c9-227">La `InitializeAsync` fonction attend [EnsureCoreWebView2Async,][DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async] car l’initialisation est `CoreWebView2` asynchrone.</span><span class="sxs-lookup"><span data-stu-id="779c9-227">The `InitializeAsync` function awaits [EnsureCoreWebView2Async][DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async] because the initialization of `CoreWebView2` is asynchronous.</span></span>  

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

1.  <span data-ttu-id="779c9-228">Après `CoreWebView2` l’initialisation, inscrivez un handler d’événements pour y `WebMessageReceived` répondre.</span><span class="sxs-lookup"><span data-stu-id="779c9-228">After `CoreWebView2` is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="779c9-229">Dans le `Form1.cs` fichier, mettez à jour `InitializeAsync` et ajoutez à `UpdateAddressBar` l’aide de l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="779c9-229">In the `Form1.cs` file, update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  

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

1.  <span data-ttu-id="779c9-230">Pour que Le WebView envoie et réponde au message web, une fois initialisé, l’hôte injecte un script dans le contenu `CoreWebView2` web pour :</span><span class="sxs-lookup"><span data-stu-id="779c9-230">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host injects a script in the web content to:</span></span>  

    1.  <span data-ttu-id="779c9-231">Envoyez l’URL à l’hôte à l’aide `postMessage` de .</span><span class="sxs-lookup"><span data-stu-id="779c9-231">Send the URL to the host using `postMessage`.</span></span>
    1.  <span data-ttu-id="779c9-232">Inscrivez un handler d’événements pour imprimer un message envoyé à partir de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="779c9-232">Register an event handler to print a message sent from the host.</span></span>  

<span data-ttu-id="779c9-233">Dans le `Form1.cs` fichier, mettez à `InitializeAsync` jour pour correspondre à l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="779c9-233">In the `Form1.cs` file, update `InitializeAsync` to match the following code snippet.</span></span>  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

<span data-ttu-id="779c9-234">Pour créer et exécuter l’application, sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="779c9-234">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="779c9-235">À présent, la barre d’adresses affiche l’URI dans le contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="779c9-235">Now, the address bar displays the URI in the WebView2 control.</span></span>  <span data-ttu-id="779c9-236">En outre, lorsque vous accédez à une nouvelle URL, WebView avertit l’utilisateur de l’URL affichée dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="779c9-236">Also, when you successfully navigate to a new URL, the WebView alerts the user of the URL displayed in the WebView.</span></span>  

:::image type="complex" source="./media/winforms-finalapp.png" alt-text="Application finale" lightbox="./media/winforms-finalapp.png":::
   <span data-ttu-id="779c9-238">Application finale</span><span class="sxs-lookup"><span data-stu-id="779c9-238">Final app</span></span>  
:::image-end:::

<span data-ttu-id="779c9-239">Félicitations, vous avez créé votre première application WebView2.</span><span class="sxs-lookup"><span data-stu-id="779c9-239">Congratulations, you built your first WebView2 app.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="779c9-240">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="779c9-240">Next steps</span></span>  

<span data-ttu-id="779c9-241">Pour en savoir plus sur WebView2, accédez aux ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="779c9-241">To continue learning more about WebView2, navigate to the following resources.</span></span>  

*   <span data-ttu-id="779c9-242">Pour en savoir plus sur la création d’applications WebView2, accédez aux meilleures pratiques de développement [WebView2.][WV2BestPractices]</span><span class="sxs-lookup"><span data-stu-id="779c9-242">To learn more about building WebView2 applications, navigate to [WebView2 development best practices][WV2BestPractices].</span></span>  
*   <span data-ttu-id="779c9-243">Pour obtenir un exemple complet des fonctionnalités WebView2, accédez [à WebView2Samples.][GithubMicrosoftedgeWebview2samplesMain]</span><span class="sxs-lookup"><span data-stu-id="779c9-243">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].</span></span>  
*   <span data-ttu-id="779c9-244">Pour plus d’informations sur WebView2, accédez [à Ressources WebView2.][Webview2IndexNextSteps]</span><span class="sxs-lookup"><span data-stu-id="779c9-244">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  
*   <span data-ttu-id="779c9-245">Pour plus d’informations sur l’API WebView2, accédez à la référence [d’API.][DotnetApiMicrosoftWebWebview2WinformsWebview2]</span><span class="sxs-lookup"><span data-stu-id="779c9-245">For detailed information about the WebView2 API, navigate to [API reference][DotnetApiMicrosoftWebWebview2WinformsWebview2].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="779c9-246">Entrer en contact avec l’équipe web Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="779c9-246">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WV2BestPractices]: ../concepts/developer-guide.md "Meilleures pratiques en matière de développement WebView2 | Documents Microsoft"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Étapes suivantes : présentation de Microsoft Edge WebView2 (prévisualisation) | Documents Microsoft"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Événements de navigation | Documents Microsoft"  

[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Espace de noms Microsoft.Web.WebView2.WinForms | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2]: /dotnet/api/microsoft.web.webview2.winforms.webview2 "Classe WebView2 | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.winforms.webview2.ensurecorewebview2async "Méthode WebView2.EnsureCoreWebView2Async(CoreWebView2Environment) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync]: /dotnet/api/microsoft.web.webview2.winforms.webview2.executescriptasync "WebView2.ExecuteScriptAsync(String) Method | Documents Microsoft"  

[DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]: /dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support "Configuration de votre application Forms Windows pour une prise en charge haute de la haute Windows forms | Documents Microsoft"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2 | Microsoft Edge Développeur"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  
