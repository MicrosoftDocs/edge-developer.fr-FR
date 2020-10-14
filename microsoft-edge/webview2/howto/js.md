---
description: Apprenez à utiliser JavaScript dans des scénarios complexes dans les applications WebView2
title: Utiliser JavaScript dans les applications WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/12/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 5312cf6209e81a1bbcfa33f324e9b8e7ef099cec
ms.sourcegitcommit: aec8d3482465dfb9a4f5f61c5eded1ff6f66d71d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "11117698"
---
# <span data-ttu-id="fb6f6-104">Utiliser JavaScript dans WebView pour des scénarios étendus</span><span class="sxs-lookup"><span data-stu-id="fb6f6-104">Use JavaScript in WebView for extended scenarios</span></span>  

<span data-ttu-id="fb6f6-105">L’utilisation de JavaScript dans les contrôles WebView2 vous permet de personnaliser les applications natives en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-105">Using JavaScript in WebView2 controls allows you to customize native apps to meet your requirements.</span></span>  <span data-ttu-id="fb6f6-106">Cet article décrit l’utilisation de JavaScript dans WebView2 et explique comment développer à l’aide des fonctionnalités et fonctionnalités avancées d’WebView2.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-106">This article explores how to use JavaScript in WebView2, and reviews how to develop using advanced WebView2 features and functionality.</span></span>  

## <span data-ttu-id="fb6f6-107">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="fb6f6-107">Before you begin</span></span>  

<span data-ttu-id="fb6f6-108">Cet article part du principe que vous disposez déjà d’un projet actif.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-108">This article assumes that you already have a working project.</span></span>  <span data-ttu-id="fb6f6-109">Si vous n’avez pas de projet et voulez suivre, accédez au [Guide de mise en route de WebView2][Webview2GettingstartedWpf].</span><span class="sxs-lookup"><span data-stu-id="fb6f6-109">If you do not have a project and want to follow along, navigate to the [WebView2 Getting Started Guide][Webview2GettingstartedWpf].</span></span>  

## <span data-ttu-id="fb6f6-110">Fonctions WebView2 de base</span><span class="sxs-lookup"><span data-stu-id="fb6f6-110">Basic WebView2 Functions</span></span>  

<span data-ttu-id="fb6f6-111">Pour commencer à incorporer du JavaScript dans votre application WebView, utilisez les fonctions suivantes.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-111">Use the following functions to begin embedding JavaScript in your WebView app.</span></span>  

| <span data-ttu-id="fb6f6-112">API</span><span class="sxs-lookup"><span data-stu-id="fb6f6-112">API</span></span>  | <span data-ttu-id="fb6f6-113">Description</span><span class="sxs-lookup"><span data-stu-id="fb6f6-113">Description</span></span>  |
|:--- |:--- |  
| [<span data-ttu-id="fb6f6-114">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="fb6f6-114">ExecuteScriptAsync</span></span>][Webview2ReferenceWpf09515MicrosoftWebExecutescriptasync] | <span data-ttu-id="fb6f6-115">Exécutez JavaScript dans un contrôle WebView.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-115">Run JavaScript in a WebView control.</span></span> <span data-ttu-id="fb6f6-116">Pour plus d’informations, accédez au didacticiel de mise en route.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-116">For more information, navigate to the Getting Started tutorial.</span></span> |
| [<span data-ttu-id="fb6f6-117">OnDocumentCreatedAsync</span><span class="sxs-lookup"><span data-stu-id="fb6f6-117">OnDocumentCreatedAsync</span></span>][Webview2ReferenceWin3209538Icorewebview2Addscripttoexecuteondocumentcreated] | <span data-ttu-id="fb6f6-118">S’exécute lorsque le modèle d’objet de document (DOM) est créé.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-118">Runs when the Document Object Model \(DOM\) is created.</span></span> |
      
## <span data-ttu-id="fb6f6-119">Scénario: exécution d’un fichier de script dédié</span><span class="sxs-lookup"><span data-stu-id="fb6f6-119">Scenario:  Running a dedicated script file</span></span>  

<span data-ttu-id="fb6f6-120">Dans cette section, accédez à un fichier JavaScript dédié depuis votre contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-120">In this section, access a dedicated JavaScript file from your WebView2 control.</span></span>  

> [!NOTE]
> <span data-ttu-id="fb6f6-121">Même s’il est possible d’écrire du code JavaScript inline dans les commandes JavaScript rapides, vous perdez les thèmes de couleurs JavaScript et la mise en forme de ligne qui complique la rédaction de grandes sections de code dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-121">Although writing JavaScript inline may be efficient for quick JavaScript commands, you lose JavaScript color themes and line formatting that makes it difficult to write large sections of code in Visual Studio.</span></span>  

<span data-ttu-id="fb6f6-122">Pour résoudre le problème, créez un fichier JavaScript distinct avec votre code, puis transmettez une référence à ce fichier à l’aide des `ExecuteScriptAsync` paramètres.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-122">To solve the problem, create a separate JavaScript file with your code, and then pass a reference to that file using the `ExecuteScriptAsync` parameters.</span></span>  

1.  <span data-ttu-id="fb6f6-123">Créez un `.js` fichier dans votre projet et ajoutez le code JavaScript que vous souhaitez exécuter.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-123">Create a `.js` file in your project, and add the JavaScript code that you want to run.</span></span>  <span data-ttu-id="fb6f6-124">Par exemple, créez un fichier appelé `script.js` .</span><span class="sxs-lookup"><span data-stu-id="fb6f6-124">For example, create a file called `script.js`.</span></span>  
1.  <span data-ttu-id="fb6f6-125">Convertissez le fichier JavaScript en une chaîne qui est transmise à `ExecuteScriptAsync` .</span><span class="sxs-lookup"><span data-stu-id="fb6f6-125">Convert the JavaScript file to a string that is passed to `ExecuteScriptAsync`.</span></span>  
    1.  <span data-ttu-id="fb6f6-126">Pour convertir votre fichier JavaScript en chaîne, copiez l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-126">To convert your JavaScript file into a string, copy the following code snippet.</span></span>  
        
        ```csharp
        string text = System.IO.File.ReadAllText(@"C:\PATH_TO_YOUR_FILE\script.js");
        ```  
        
    1.  <span data-ttu-id="fb6f6-127">Collez le code dans `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="fb6f6-127">Paste the code into `MainWindow.xaml.cs`.</span></span>  
1.  <span data-ttu-id="fb6f6-128">Transmettez votre variable de texte à l’aide de `ExecuteScriptAsync` .</span><span class="sxs-lookup"><span data-stu-id="fb6f6-128">Pass your text variable using `ExecuteScriptAsync`.</span></span>  
    
    ```csharp
    await webView.CoreWebView2.ExecuteScriptAsync(text);
    ```  

## <span data-ttu-id="fb6f6-129">Scénario: supprimer la fonctionnalité de glisser-déplacer</span><span class="sxs-lookup"><span data-stu-id="fb6f6-129">Scenario:  Remove drag-and-drop functionality</span></span>  

<span data-ttu-id="fb6f6-130">Dans cette section, utilisez JavaScript pour supprimer la fonctionnalité de glisser-déplacer de votre contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-130">In this section, use JavaScript to remove the drag-and-drop functionality from your WebView2 control.</span></span>  

<span data-ttu-id="fb6f6-131">Pour commencer, explorez la fonctionnalité de glisser-déplacer actuelle.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-131">To begin, explore the current drag-and-drop functionality.</span></span>  

1.  <span data-ttu-id="fb6f6-132">Créer un `.txt` fichier pour le glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-132">Create a `.txt` file in order to drag-and-drop.</span></span>  <span data-ttu-id="fb6f6-133">Par exemple, vous pouvez créer un fichier nommé `contoso.txt` et y ajouter du texte.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-133">For example, create a file named `contoso.txt` and add text to it.</span></span>  
1.  <span data-ttu-id="fb6f6-134">Exécutez votre projet.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-134">Run your project.</span></span>  
1.  <span data-ttu-id="fb6f6-135">Faites un glisser-déplacer du `contoso.txt` fichier vers le contrôle WebView.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-135">Drag-and-drop the `contoso.txt` file onto the WebView control.</span></span>  <span data-ttu-id="fb6f6-136">Une nouvelle fenêtre s’ouvre, qui est le résultat du code de votre exemple de projet.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-136">A new window opens, which is the result of the code in your sample project.</span></span>  
    
    :::image type="complex" source="./media/dragtext.png" alt-text="Résultat du glisser-déplacer de contoso.txt" lightbox="./media/dragtext.png":::
       <span data-ttu-id="fb6f6-138">Résultat du glisser-déplacer de contoso.txt</span><span class="sxs-lookup"><span data-stu-id="fb6f6-138">Result of dragging and dropping contoso.txt</span></span>  
    :::image-end:::  

<span data-ttu-id="fb6f6-139">À présent, ajoutez du code pour supprimer la fonctionnalité de glisser-déplacer du contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-139">Now, add code to remove the drag-and-drop functionality from the WebView2 control.</span></span>  

1.  <span data-ttu-id="fb6f6-140">Copiez et collez l’extrait de code suivant dans `InitializeAsync()` in `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="fb6f6-140">Copy and paste the following code snippet into `InitializeAsync()` in `MainWindow.xaml.cs`.</span></span>   
            
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('dragover',function(e){e.preventDefault();},false);");
    
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('drop',function(e){" +
    "e.preventDefault();" +
    "console.log(e.dataTransfer);" +
    "console.log(e.dataTransfer.files[0])" +
    "}, false);");
    ```  
          
1.  <span data-ttu-id="fb6f6-141">Exécutez votre projet.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-141">Run your project.</span></span>  
1.  <span data-ttu-id="fb6f6-142">Essayez de glisser-déplacer `contoso.txt` .</span><span class="sxs-lookup"><span data-stu-id="fb6f6-142">Try to drag-and-drop `contoso.txt`.</span></span>  <span data-ttu-id="fb6f6-143">Vérifiez que vous n’êtes pas en mesure de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-143">Confirm that you are not able to drag-and-drop.</span></span>  

## <span data-ttu-id="fb6f6-144">Scénario: suppression du menu contextuel</span><span class="sxs-lookup"><span data-stu-id="fb6f6-144">Scenario:  Removing the Context Menu</span></span>  

<span data-ttu-id="fb6f6-145">Dans cette section, supprimez le menu contextuel par défaut de votre contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-145">In this section, remove the default context menu from your WebView2 control.</span></span>  

<span data-ttu-id="fb6f6-146">Pour commencer, explorez les fonctionnalités de menu contextuel actuelles.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-146">To begin, explore the current contextual menu functionality.</span></span>  

1.  <span data-ttu-id="fb6f6-147">Exécutez votre projet.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-147">Run your project.</span></span>  
1.  <span data-ttu-id="fb6f6-148">Positionnez le curseur n’importe où sur le contrôle WebView2 et ouvrez le menu contextuel (cliquez avec le bouton droit sur \).</span><span class="sxs-lookup"><span data-stu-id="fb6f6-148">Hover anywhere on the WebView2 control and open the context menu \(right-click\).</span></span>  <span data-ttu-id="fb6f6-149">Le menu contextuel affiche les choix par défaut.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-149">The context menu displays the default choices.</span></span>  
    
    :::image type="complex" source="./media/contextmenu.png" alt-text="Résultat du glisser-déplacer de contoso.txt" lightbox="./media/contextmenu.png":::
       <span data-ttu-id="fb6f6-151">Menu contextuel affichant les choix par défaut</span><span class="sxs-lookup"><span data-stu-id="fb6f6-151">The context menu showing the default choices</span></span>  
    :::image-end:::  
    
<span data-ttu-id="fb6f6-152">Ajoutez désormais du code pour supprimer la fonctionnalité de menu contextuel du contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-152">Now add code to remove the contextual menu functionality from the WebView2 control.</span></span>  

1.  <span data-ttu-id="fb6f6-153">Copiez et collez l’extrait de code suivant dans `InitializeAsync()` in `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="fb6f6-153">Copy and paste the following code snippet into `InitializeAsync()` in `MainWindow.xaml.cs`.</span></span>    
        
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('contextmenu', window => {window.preventDefault();});");
    ```  

1.  <span data-ttu-id="fb6f6-154">Réexécutez le code.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-154">Run the code again.</span></span>  <span data-ttu-id="fb6f6-155">Vérifiez que vous ne pouvez pas ouvrir un menu contextuel (cliquez avec le bouton droit sur \).</span><span class="sxs-lookup"><span data-stu-id="fb6f6-155">Confirm that you're not able to open a context menu \(right-click\).</span></span>  
   
## <span data-ttu-id="fb6f6-156">Voir également</span><span class="sxs-lookup"><span data-stu-id="fb6f6-156">See also</span></span>  

*   <span data-ttu-id="fb6f6-157">Pour plus d’informations sur la mise en route de WebView2, accédez à [WebView2 guides de mise en route][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="fb6f6-157">For more information on getting started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="fb6f6-158">Pour obtenir un exemple complet de fonctionnalités WebView2, accédez au référentiel Samples [WebView2Samples][GithubMicrosoftedgeWebview2samples] sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="fb6f6-158">For a comprehensive example of WebView2 capabilities, navigate to the [WebView2Samples][GithubMicrosoftedgeWebview2samples] repo on GitHub.</span></span>  
*   <span data-ttu-id="fb6f6-159">Pour plus d’informations sur les API WebView2, accédez à informations de référence sur les [API][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="fb6f6-159">For detailed information on WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>  
*   <span data-ttu-id="fb6f6-160">Pour plus d’informations sur WebView2, accédez à [ressources WebView2][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="fb6f6-160">For more information on WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>  

## <span data-ttu-id="fb6f6-161">Contacter l’équipe WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="fb6f6-161">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  


[Webview2ApiReference]: ../webview2-api-reference.md "Référence sur l’API Microsoft Edge WebView2 | Documents Microsoft"  
[Webview2GettingstartedWpf]: ../gettingstarted/wpf.md "Commencer à utiliser WebView2 dans WPF (Preview) | Documents Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Mise en route-présentation de Microsoft Edge WebView2 (Preview) | Documents Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Étapes suivantes-présentation de Microsoft Edge WebView2 (Preview) | Documents Microsoft"  
[Webview2ReferenceWin3209538Icorewebview2Addscripttoexecuteondocumentcreated]: ../reference/win32/0-9-538/icorewebview2.md#addscripttoexecuteondocumentcreated "AddScriptToExecuteOnDocumentCreated-0.9.579-interface ICoreWebView2 | Documents Microsoft"  
[Webview2ReferenceWpf09515MicrosoftWebExecutescriptasync]: ../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#executescriptasync "ExecuteScriptAsync-Microsoft. Web. WebView2. WPF. WebView2 classe | Documents Microsoft"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemples de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  
