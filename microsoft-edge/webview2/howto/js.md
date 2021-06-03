---
description: Découvrez comment utiliser JavaScript dans des scénarios complexes dans les applications WebView2
title: Utiliser JavaScript dans les applications WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: da04d1e24b95dfa7ea477bbd228fd46b64727ec3
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536452"
---
# <a name="use-javascript-in-webview-for-extended-scenarios"></a><span data-ttu-id="e40df-104">Utiliser JavaScript dans WebView pour les scénarios étendus</span><span class="sxs-lookup"><span data-stu-id="e40df-104">Use JavaScript in WebView for extended scenarios</span></span>  

<span data-ttu-id="e40df-105">L’utilisation de JavaScript dans les contrôles WebView2 vous permet de personnaliser les applications natives pour répondre à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="e40df-105">Using JavaScript in WebView2 controls allows you to customize native apps to meet your requirements.</span></span>  <span data-ttu-id="e40df-106">Cet article explique comment utiliser JavaScript dans WebView2 et explique comment développer à l’aide des fonctionnalités WebView2 avancées.</span><span class="sxs-lookup"><span data-stu-id="e40df-106">This article explores how to use JavaScript in WebView2, and reviews how to develop using advanced WebView2 features and functionality.</span></span>  

## <a name="before-you-begin"></a><span data-ttu-id="e40df-107">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="e40df-107">Before you begin</span></span>  

<span data-ttu-id="e40df-108">Cet article suppose que vous avez déjà un projet de travail.</span><span class="sxs-lookup"><span data-stu-id="e40df-108">This article assumes that you already have a working project.</span></span>  <span data-ttu-id="e40df-109">Si vous n’avez pas de projet et que vous souhaitez suivre, accédez au Guide de mise en route [de WebView2.][Webview2GettingstartedWpf]</span><span class="sxs-lookup"><span data-stu-id="e40df-109">If you do not have a project and want to follow along, navigate to the [WebView2 Getting Started Guide][Webview2GettingstartedWpf].</span></span>  

## <a name="basic-webview2-functions"></a><span data-ttu-id="e40df-110">Fonctions WebView2 de base</span><span class="sxs-lookup"><span data-stu-id="e40df-110">Basic WebView2 Functions</span></span>  

<span data-ttu-id="e40df-111">Utilisez les fonctions suivantes pour commencer à incorporer JavaScript dans votre application WebView.</span><span class="sxs-lookup"><span data-stu-id="e40df-111">Use the following functions to begin embedding JavaScript in your WebView app.</span></span>  

| <span data-ttu-id="e40df-112">API</span><span class="sxs-lookup"><span data-stu-id="e40df-112">API</span></span>  | <span data-ttu-id="e40df-113">Description</span><span class="sxs-lookup"><span data-stu-id="e40df-113">Description</span></span>  |
|:--- |:--- |  
| [<span data-ttu-id="e40df-114">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="e40df-114">ExecuteScriptAsync</span></span>][Webview2ReferenceWpfMicrosoftWebExecutescriptasync] | <span data-ttu-id="e40df-115">Exécutez JavaScript dans un contrôle WebView.</span><span class="sxs-lookup"><span data-stu-id="e40df-115">Run JavaScript in a WebView control.</span></span> <span data-ttu-id="e40df-116">Pour plus d’informations, accédez au didacticiel de mise en place.</span><span class="sxs-lookup"><span data-stu-id="e40df-116">For more information, navigate to the Getting Started tutorial.</span></span> |
| [<span data-ttu-id="e40df-117">OnDocumentCreatedAsync</span><span class="sxs-lookup"><span data-stu-id="e40df-117">OnDocumentCreatedAsync</span></span>][Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated] | <span data-ttu-id="e40df-118">S’exécute lorsque le modèle objet de document \(DOM\) est créé.</span><span class="sxs-lookup"><span data-stu-id="e40df-118">Runs when the Document Object Model \(DOM\) is created.</span></span> |
      
## <a name="scenario--running-a-dedicated-script-file"></a><span data-ttu-id="e40df-119">Scénario : exécution d’un fichier de script dédié</span><span class="sxs-lookup"><span data-stu-id="e40df-119">Scenario:  Running a dedicated script file</span></span>  

<span data-ttu-id="e40df-120">Dans cette section, accédez à un fichier JavaScript dédié à partir de votre contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="e40df-120">In this section, access a dedicated JavaScript file from your WebView2 control.</span></span>  

> [!NOTE]
> <span data-ttu-id="e40df-121">Bien que l’écriture de Code JavaScript en ligne puisse être efficace pour les commandes JavaScript rapides, vous perdez les thèmes de couleur JavaScript et la mise en forme des lignes, ce qui rend difficile l’écriture de grandes sections de code dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e40df-121">Although writing JavaScript inline may be efficient for quick JavaScript commands, you lose JavaScript color themes and line formatting that makes it difficult to write large sections of code in Visual Studio.</span></span>  

<span data-ttu-id="e40df-122">Pour résoudre le problème, créez un fichier JavaScript distinct avec votre code, puis passez une référence à ce fichier à l’aide `ExecuteScriptAsync` des paramètres.</span><span class="sxs-lookup"><span data-stu-id="e40df-122">To solve the problem, create a separate JavaScript file with your code, and then pass a reference to that file using the `ExecuteScriptAsync` parameters.</span></span>  

1.  <span data-ttu-id="e40df-123">Créez `.js` un fichier dans votre projet et ajoutez le code JavaScript à exécuter.</span><span class="sxs-lookup"><span data-stu-id="e40df-123">Create a `.js` file in your project, and add the JavaScript code that you want to run.</span></span>  <span data-ttu-id="e40df-124">Par exemple, créez un fichier appelé `script.js` .</span><span class="sxs-lookup"><span data-stu-id="e40df-124">For example, create a file called `script.js`.</span></span>  
1.  <span data-ttu-id="e40df-125">Convertissez le fichier JavaScript en une chaîne qui est transmise à `ExecuteScriptAsync` .</span><span class="sxs-lookup"><span data-stu-id="e40df-125">Convert the JavaScript file to a string that is passed to `ExecuteScriptAsync`.</span></span>  
    1.  <span data-ttu-id="e40df-126">Pour convertir votre fichier JavaScript en chaîne, copiez l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="e40df-126">To convert your JavaScript file into a string, copy the following code snippet.</span></span>  
        
        ```csharp
        string text = System.IO.File.ReadAllText(@"C:\PATH_TO_YOUR_FILE\script.js");
        ```  
        
    1.  <span data-ttu-id="e40df-127">Collez le code dans `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="e40df-127">Paste the code into `MainWindow.xaml.cs`.</span></span>  
1.  <span data-ttu-id="e40df-128">Passez votre variable de texte à l’aide `ExecuteScriptAsync` de .</span><span class="sxs-lookup"><span data-stu-id="e40df-128">Pass your text variable using `ExecuteScriptAsync`.</span></span>  
    
    ```csharp
    await webView.CoreWebView2.ExecuteScriptAsync(text);
    ```  

## <a name="scenario--remove-drag-and-drop-functionality"></a><span data-ttu-id="e40df-129">Scénario : supprimer la fonctionnalité glisser-déposer</span><span class="sxs-lookup"><span data-stu-id="e40df-129">Scenario:  Remove drag-and-drop functionality</span></span>  

<span data-ttu-id="e40df-130">Dans cette section, utilisez JavaScript pour supprimer la fonctionnalité glisser-déposer de votre contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="e40df-130">In this section, use JavaScript to remove the drag-and-drop functionality from your WebView2 control.</span></span>  

<span data-ttu-id="e40df-131">Pour commencer, explorez la fonctionnalité de glisser-déposer actuelle.</span><span class="sxs-lookup"><span data-stu-id="e40df-131">To begin, explore the current drag-and-drop functionality.</span></span>  

1.  <span data-ttu-id="e40df-132">Créez `.txt` un fichier pour glisser-déposer.</span><span class="sxs-lookup"><span data-stu-id="e40df-132">Create a `.txt` file in order to drag-and-drop.</span></span>  <span data-ttu-id="e40df-133">Par exemple, créez un fichier nommé `contoso.txt` et ajoutez-y du texte.</span><span class="sxs-lookup"><span data-stu-id="e40df-133">For example, create a file named `contoso.txt` and add text to it.</span></span>  
1.  <span data-ttu-id="e40df-134">Exécutez votre projet.</span><span class="sxs-lookup"><span data-stu-id="e40df-134">Run your project.</span></span>  
1.  <span data-ttu-id="e40df-135">Glisser-déposer le `contoso.txt` fichier sur le contrôle WebView.</span><span class="sxs-lookup"><span data-stu-id="e40df-135">Drag-and-drop the `contoso.txt` file onto the WebView control.</span></span>  <span data-ttu-id="e40df-136">Une nouvelle fenêtre s’ouvre, qui est le résultat du code dans votre exemple de projet.</span><span class="sxs-lookup"><span data-stu-id="e40df-136">A new window opens, which is the result of the code in your sample project.</span></span>  
    
    :::image type="complex" source="./media/dragtext.png" alt-text="Résultat d’un glisser-déposer contoso.txt" lightbox="./media/dragtext.png":::
       <span data-ttu-id="e40df-138">Résultat d’un glisser-déposer contoso.txt</span><span class="sxs-lookup"><span data-stu-id="e40df-138">Result of dragging and dropping contoso.txt</span></span>  
    :::image-end:::  

<span data-ttu-id="e40df-139">À présent, ajoutez du code pour supprimer la fonctionnalité glisser-déposer du contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="e40df-139">Now, add code to remove the drag-and-drop functionality from the WebView2 control.</span></span>  

1.  <span data-ttu-id="e40df-140">Copiez et collez l’extrait de code suivant dans `InitializeAsync()` `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="e40df-140">Copy and paste the following code snippet into `InitializeAsync()` in `MainWindow.xaml.cs`.</span></span>   
            
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('dragover',function(e){e.preventDefault();},false);");
    
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('drop',function(e){" +
    "e.preventDefault();" +
    "console.log(e.dataTransfer);" +
    "console.log(e.dataTransfer.files[0])" +
    "}, false);");
    ```  
          
1.  <span data-ttu-id="e40df-141">Exécutez votre projet.</span><span class="sxs-lookup"><span data-stu-id="e40df-141">Run your project.</span></span>  
1.  <span data-ttu-id="e40df-142">Essayez de `contoso.txt` glisser-déposer.</span><span class="sxs-lookup"><span data-stu-id="e40df-142">Try to drag-and-drop `contoso.txt`.</span></span>  <span data-ttu-id="e40df-143">Confirmez que vous ne pouvez pas glisser-déposer.</span><span class="sxs-lookup"><span data-stu-id="e40df-143">Confirm that you are not able to drag-and-drop.</span></span>  

## <a name="scenario--removing-the-context-menu"></a><span data-ttu-id="e40df-144">Scénario : suppression du menu Context</span><span class="sxs-lookup"><span data-stu-id="e40df-144">Scenario:  Removing the Context Menu</span></span>  

<span data-ttu-id="e40df-145">Dans cette section, supprimez le menu contexté par défaut de votre contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="e40df-145">In this section, remove the default context menu from your WebView2 control.</span></span>  

<span data-ttu-id="e40df-146">Pour commencer, explorez la fonctionnalité de menu contextuel actuelle.</span><span class="sxs-lookup"><span data-stu-id="e40df-146">To begin, explore the current contextual menu functionality.</span></span>  

1.  <span data-ttu-id="e40df-147">Exécutez votre projet.</span><span class="sxs-lookup"><span data-stu-id="e40df-147">Run your project.</span></span>  
1.  <span data-ttu-id="e40df-148">Pointez n’importe où sur le contrôle WebView2 et ouvrez le menu contextiqué \(clic droit\).</span><span class="sxs-lookup"><span data-stu-id="e40df-148">Hover anywhere on the WebView2 control and open the context menu \(right-click\).</span></span>  <span data-ttu-id="e40df-149">Le menu contexté affiche les choix par défaut.</span><span class="sxs-lookup"><span data-stu-id="e40df-149">The context menu displays the default choices.</span></span>  
    
    :::image type="complex" source="./media/contextmenu.png" alt-text="Menu contexté affichant les choix par défaut" lightbox="./media/contextmenu.png":::
       <span data-ttu-id="e40df-151">Menu contexté affichant les choix par défaut</span><span class="sxs-lookup"><span data-stu-id="e40df-151">The context menu showing the default choices</span></span>  
    :::image-end:::  
    
<span data-ttu-id="e40df-152">À présent, ajoutez du code pour supprimer la fonctionnalité de menu contextuel du contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="e40df-152">Now add code to remove the contextual menu functionality from the WebView2 control.</span></span>  

1.  <span data-ttu-id="e40df-153">Copiez et collez l’extrait de code suivant dans `InitializeAsync()` `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="e40df-153">Copy and paste the following code snippet into `InitializeAsync()` in `MainWindow.xaml.cs`.</span></span>    
        
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('contextmenu', window => {window.preventDefault();});");
    ```  

1.  <span data-ttu-id="e40df-154">Exécutez à nouveau le code.</span><span class="sxs-lookup"><span data-stu-id="e40df-154">Run the code again.</span></span>  <span data-ttu-id="e40df-155">Confirmez que vous n’êtes pas en mesure d’ouvrir un menu contexto \(clic droit\).</span><span class="sxs-lookup"><span data-stu-id="e40df-155">Confirm that you're not able to open a context menu \(right-click\).</span></span>  
   
## <a name="see-also"></a><span data-ttu-id="e40df-156">Articles associés</span><span class="sxs-lookup"><span data-stu-id="e40df-156">See also</span></span>  

*   <span data-ttu-id="e40df-157">Pour plus d’informations sur la mise en place de WebView2, accédez aux guides de mise en page [WebView2.][Webview2MainGettingStarted]</span><span class="sxs-lookup"><span data-stu-id="e40df-157">For more information on getting started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="e40df-158">Pour obtenir un exemple complet des fonctionnalités WebView2, accédez au repo [WebView2Samples][GithubMicrosoftedgeWebview2samples] GitHub.</span><span class="sxs-lookup"><span data-stu-id="e40df-158">For a comprehensive example of WebView2 capabilities, navigate to the [WebView2Samples][GithubMicrosoftedgeWebview2samples] repo on GitHub.</span></span>  
*   <span data-ttu-id="e40df-159">Pour plus d’informations sur les API WebView2, accédez à la [référence d’API.][Webview2ApiReference]</span><span class="sxs-lookup"><span data-stu-id="e40df-159">For detailed information on WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>  
*   <span data-ttu-id="e40df-160">Pour plus d’informations sur WebView2, accédez [à Ressources WebView2.][Webview2MainNextSteps]</span><span class="sxs-lookup"><span data-stu-id="e40df-160">For more information on WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="e40df-161">Entrer en contact avec l’équipe web Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="e40df-161">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Microsoft Edge outils de développement (Chromium) | Documents Microsoft"  


[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge Référence de l’API WebView2 | Documents Microsoft"  
[Webview2GettingstartedWpf]: ../gettingstarted/wpf.md "Getting started with WebView2 in WPF (Preview) | Documents Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Mise en place : présentation de Microsoft Edge WebView2 (prévisualisation) | Documents Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Étapes suivantes : présentation de Microsoft Edge WebView2 (prévisualisation) | Documents Microsoft"  
[Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated]: /microsoft-edge/webview2/reference/win32/icorewebview2#addscripttoexecuteondocumentcreated "AddScriptToExecuteOnDocumentCreated - 0.9.579 - interface ICoreWebView2 | Documents Microsoft"  
[Webview2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.Exeméthode cuteScriptAsync(String) (Microsoft.Web.WebView2.Wpf) | Documents Microsoft"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  
