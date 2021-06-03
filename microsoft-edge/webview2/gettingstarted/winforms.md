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
# <a name="getting-started-with-webview2-in-windows-forms"></a>Mise en place de WebView2 dans Windows Forms

Dans cet article, commencer à créer votre première application WebView2 et en savoir plus sur les principales fonctionnalités de [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].  Pour plus d’informations sur les API individuelles, accédez à la [référence d’API.][DotnetApiMicrosoftWebWebview2Winforms]  

## <a name="prerequisites"></a>Conditions préalables  

Veillez à installer la liste des conditions préalables suivante avant de poursuivre.  

*   [WebView2 Runtime][MicrosoftDeveloperMicrosoftEdgeWebview2] ou tout canal [Microsoft Edge (Chromium) non stable][MicrosoftedgeinsiderDownload] installé sur le système d’exploitation pris en charge \(actuellement Windows 10, Windows 8.1 et Windows 7\).  
    
    > [!NOTE]
    > L’équipe WebView recommande d’utiliser le canal Canary et la version minimale requise est 82.0.488.0.  
    
*   [Visual Studio][MicrosoftVisualstudioMain] 2017 ou ultérieure.  
    
> [!NOTE]
> WebView2 ne prend actuellement pas en charge les concepteurs .NET 5 et .NET Core.  

## <a name="step-1---create-a-single-window-app"></a>Étape 1 : créer une application à fenêtre unique

Commencez par un projet de bureau de base qui contient une seule fenêtre principale.  

1.  In Visual Studio, choose **Windows Forms .NET Framework App**  >  **Next**.
    
    :::image type="complex" source="./media/winforms-newproject.png" alt-text="Nouveau projet" lightbox="./media/winforms-newproject.png":::
       Nouveau projet  
    :::image-end:::
    
1.  Entrez des valeurs **pour Project nom et** **emplacement.**  Choisissez **.NET Framework 4.6.2 ou ultérieure.**  
    
    :::image type="complex" source="./media/winforms-startproj.png" alt-text="Démarrer le projet" lightbox="./media/winforms-startproj.png":::
       Démarrer le projet  
    :::image-end:::
    
1.  Pour créer votre projet, choisissez **Créer.**
    
## <a name="step-2---install-webview2-sdk"></a>Étape 2 : installer le SDK WebView2

Utilisez NuGet pour ajouter le SDK WebView2 au projet.  

1.  Pointez sur le projet, ouvrez le menu contextuel \(clic droit\), puis choisissez **Gérer NuGet packages...**.  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Gérer NuGet packages":::
       Gérer NuGet packages
    :::image-end:::
    
1.  Dans la barre de recherche, `Microsoft.Web.WebView2` tapez > **choisissez Microsoft.Web.WebView2**.  
    
    :::image type="complex" source="./media/installnuget.png" alt-text="NuGet" lightbox="./media/installnuget.png":::
       NuGet  
    :::image-end:::
    
    Commencez à développer des applications à l’aide de l’API WebView2.  Pour créer et exécuter le projet, sélectionnez `F5` .  Le projet en cours d’exécution affiche une fenêtre vide.  
    
    :::image type="complex" source="./media/winforms-emptyapp.png" alt-text="Application vide" lightbox="./media/winforms-emptyapp.png":::
       Application vide  
    :::image-end:::
    
## <a name="step-3---create-a-single-webview"></a>Étape 3 : créer un seul WebView  

Ajoutez un WebView à votre application.  

1.  Ouvrez **le Windows Forms Designer.**  
1.  Recherchez **WebView2 dans** la boîte **à outils.**  
    
    > [!NOTE]
    > Si vous utilisez Visual Studio 2017, **webView2** n’est peut-être pas affiché par défaut dans la **boîte à outils.**  Pour activer le **** comportement, sélectionnez  >  **Options d’outils**> définir le paramètre Boîte à  >  **** **outils** Remplir automatiquement sur `True` .  
    
    Faites glisser et déposez **le contrôle WebView2** dans l’Windows Forms App.
    
    :::image type="complex" source="./media/winforms-toolbox.png" alt-text="Boîte à outils affichant WebView2":::
       Boîte à outils affichant WebView2  
    :::image-end:::  

1.  Définissez `(Name)` la propriété sur `webView` .
    
    :::image type="complex" source="./media/winforms-properties.png" alt-text="Propriétés du contrôle WebView2":::
       Propriétés du contrôle WebView2
    :::image-end:::

1.  La `Source` propriété définit l’URI initial affiché dans le contrôle WebView2.  Définissez `Source` la propriété sur `https://www.microsoft.com` .  
    
    :::image type="complex" source="./media/winforms-source.png" alt-text="Propriété Source du contrôle WebView2":::
       Propriété **Source** du contrôle WebView2
    :::image-end:::  

Pour créer et exécuter votre projet, sélectionnez `F5` .  Assurez-vous que votre contrôle WebView2 [https://www.microsoft.com][|::ref1::|Main] s’affiche.

:::image type="complex" source="./media/winforms-hellowebview.png" alt-text="hello webview" lightbox="./media/winforms-hellowebview.png":::
   hello webview  
:::image-end:::  

> [!NOTE]
> Si vous travaillez sur un moniteur HAUTE DPI, vous de devez configurer votre application Windows Forms pour une prise en charge [haute DPI.][DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]  

## <a name="step-4---handle-window-resize-events"></a>Étape 4 : gérer les événements de resize de fenêtre  

Ajoutez quelques contrôles à votre Windows formulaires à partir de la boîte à outils, puis traitez les événements de re resize de fenêtre de manière appropriée.  

1.  Dans le **Windows Forms Designer,** ouvrez la **boîte à outils.**  
1.  Faites glisser et déposez **un textbox** dans l’Windows Forms App.  Nommez **le textbox dans** `addressBar` **l’onglet Propriétés.**  
1.  Faites glisser un bouton **vers l’Windows** Forms.  Modifiez le texte du **bouton et** `Go!` nommez-le **dans** `goButton` l’onglet **Propriétés.**  
    
    L’application doit ressembler à l’image suivante dans le concepteur.  
    
    :::image type="complex" source="./media/winforms-designer.png" alt-text="Concepteur WinForms" lightbox="./media/winforms-designer.png":::
       Concepteur WinForms  
    :::image-end:::  

1.  Dans le `Form1.cs` fichier, `Form_Resize` définissez pour conserver les contrôles en place lorsque la fenêtre d’application est re resserée.

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

Pour créer et exécuter votre projet, sélectionnez `F5` .  Assurez-vous que l’application s’affiche comme dans la capture d’écran suivante.

:::image type="complex" source="./media/winforms-app.png" alt-text="application" lightbox="./media/winforms-app.png":::
   Application  
:::image-end:::

## <a name="step-5---navigation"></a>Étape 5 : navigation

Ajoutez la possibilité d’autoriser les utilisateurs à modifier l’URL affichée par le contrôle WebView2 en ajoutant une barre d’adresse à l’application.  

1.  Sélectionnez `F5` pour créer et exécuter votre projet.  Confirmez que l’application s’affiche comme dans la capture d’écran suivante.  
    
    :::image type="complex" source="./media/winforms-app.png" alt-text="Application WinForms" lightbox="./media/winforms-app.png":::
       Application WinForms  
    :::image-end:::  
    
1.  Dans le `Form1.cs` fichier, pour ajouter l’espace de noms, insérez l’extrait de code suivant `CoreWebView2` en haut.  

1.  In `Form1.cs` add the `CoreWebView2` namespace by inserting the following code snippet at the top of `Form1.cs` .  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

1.  Dans le **Windows Forms Designer,** double-cliquez sur le `Go!` bouton pour créer la méthode dans le `goButton_Click` `Form1.cs` fichier.  Copiez et collez l’extrait de code suivant à l’intérieur de la fonction.  À présent, `goButton_Click` la fonction navigue dans le WebView jusqu’à l’URL entrée dans la barre d’adresses.

    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

Pour créer et exécuter votre projet, sélectionnez `F5` .  Entrez une nouvelle URL dans la barre d’adresses, puis sélectionnez **Go**.  Par exemple, entrez `https://www.bing.com` .  Assurez-vous que le contrôle WebView2 navigue jusqu’à l’URL.  

> [!NOTE]
> Assurez-vous qu’une URL complète est entrée dans la barre d’adresses.  Une `ArgumentException` url est lancée si l’URL ne commence pas par `http://` ou `https://`

:::image type="complex" source="./media/winforms-bing.png" alt-text="bing.com" lightbox="./media/winforms-bing.png":::
   bing.com  
:::image-end:::

## <a name="step-6---navigation-events"></a>Étape 6 : événements de navigation  

Lors de la navigation sur la page web, le contrôle WebView2 lève des événements.  L’application qui héberge les contrôles WebView2 écoute les événements suivants.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

Pour plus d’informations, accédez à [Événements de navigation.][Webview2ConceptsNavigationEvents]  

:::image type="complex" source="../media/navigation-events.png" alt-text="Événements de navigation":::
   Événements de navigation
:::image-end:::

Lorsqu’une erreur se produit, les événements suivants sont élevés et peuvent dépendre de la navigation vers une page web d’erreur.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

> [!NOTE]
> Si une redirection HTTP se produit, il existe plusieurs `NavigationStarting` événements dans une ligne.  

Pour montrer comment utiliser les événements, commencez par inscrire un responsable pour annuler toutes les demandes n’utilisant `NavigationStarting` pas HTTPS.  

Dans le fichier, mettez à jour le constructeur pour qu’il corresponde à l’extrait de code suivant `Form1.cs` et ajoutez la `EnsureHttps` fonction.  

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

Dans le constructeur, est inscrit en tant que le `EnsureHttps` handler d’événements sur `NavigationStarting` l’événement sur le contrôle WebView2.  

Pour créer et exécuter votre projet, sélectionnez `F5` .  Assurez-vous que lorsque vous naviguez vers un site HTTP, le WebView reste inchangé.  Toutefois, le WebView naviguera vers les sites HTTPS.

## <a name="step-7---scripting"></a>Étape 7 : scripts  

Vous pouvez utiliser des applications hôtes pour injecter du code JavaScript dans des contrôles WebView2 lors de l’utilisation.  Vous pouvez tâcher WebView pour exécuter du javaScript arbitraire ou ajouter des scripts d’initialisation.  Le javaScript injecté s’applique à tous les nouveaux documents de niveau supérieur et aux images enfants jusqu’à ce que le JavaScript soit supprimé.  Le javaScript injecté est exécuté avec un minutage spécifique.  

*   Exécutez-le après la création de l’objet global.  
*   Exécutez-le avant tout autre script inclus dans le document HTML.  

Par exemple, ajoutez des scripts qui envoient une alerte lorsqu’un utilisateur navigue vers des sites non HTTPS.  Modifiez la fonction pour injecter un script dans le contenu web qui utilise la méthode `EnsureHttps` [ExecuteScriptAsync.][DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync]  

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

Pour créer et exécuter votre projet, sélectionnez `F5` .  Assurez-vous que l’application affiche une alerte lorsque vous accédez à un site web qui n’utilise pas HTTPS.  

:::image type="complex" source="./media/winforms-https.png" alt-text="https" lightbox="./media/winforms-https.png":::
   https  
:::image-end:::

## <a name="step-8---communication-between-host-and-web-content"></a>Étape 8 : communication entre le contenu hôte et le contenu web  

Le contenu hôte et web peut être utilisé pour communiquer les uns avec les `postMessage` autres comme suit :  

*   Le contenu Web d’un contrôle WebView2 peut être `window.chrome.webview.postMessage` utilisé pour publier un message à l’hôte.  L’hôte gère le message à l’aide de tous les messages `WebMessageReceived` enregistrés sur l’hôte.  
*   Héberge des messages publiés dans du contenu web dans un contrôle WebView2 à l’aide `CoreWebView2.PostWebMessageAsString` ou `CoreWebView2.PostWebMessageAsJSON` .  Ces messages sont capturés par des responsables ajoutés à `window.chrome.webview.addEventListener` .  

Le mécanisme de communication transmet les messages du contenu web à l’hôte à l’aide de fonctionnalités natives.  

Dans votre projet, lorsque le contrôle WebView2 navigue vers une URL, il affiche l’URL dans la barre d’adresses et avertit l’utilisateur de l’URL affichée dans le contrôle WebView2.  

1.  Dans le fichier, mettez à jour votre constructeur et `Form1.cs` créez `InitializeAsync` une fonction pour qu’elle corresponde à l’extrait de code suivant.  La `InitializeAsync` fonction attend [EnsureCoreWebView2Async,][DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async] car l’initialisation est `CoreWebView2` asynchrone.  

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

1.  Une `CoreWebView2` fois l’initialisation initialisée, inscrivez un handler d’événements pour y `WebMessageReceived` répondre.  Dans le `Form1.cs` fichier, mettez à jour `InitializeAsync` et ajoutez à `UpdateAddressBar` l’aide de l’extrait de code suivant.  

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

1.  Pour que Le WebView envoie et réponde au message web, une fois initialisé, l’hôte injecte un script dans le contenu `CoreWebView2` web pour :  

    1.  Envoyez l’URL à l’hôte à l’aide `postMessage` de .
    1.  Inscrivez un handler d’événements pour imprimer un message envoyé à partir de l’hôte.  

Dans le `Form1.cs` fichier, mettez à jour `InitializeAsync` pour correspondre à l’extrait de code suivant.  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

Pour créer et exécuter l’application, sélectionnez `F5` .  À présent, la barre d’adresses affiche l’URI dans le contrôle WebView2.  En outre, lorsque vous accédez à une nouvelle URL, WebView avertit l’utilisateur de l’URL affichée dans le WebView.  

:::image type="complex" source="./media/winforms-finalapp.png" alt-text="Application finale" lightbox="./media/winforms-finalapp.png":::
   Application finale  
:::image-end:::

Félicitations, vous avez créé votre première application WebView2.  

## <a name="next-steps"></a>Étapes suivantes  

Pour en savoir plus sur WebView2, accédez aux ressources suivantes.  

*   Pour en savoir plus sur la création d’applications WebView2, accédez aux meilleures pratiques de développement [WebView2.][WV2BestPractices]  
*   Pour obtenir un exemple complet des fonctionnalités WebView2, accédez [à WebView2Samples.][GithubMicrosoftedgeWebview2samplesMain]  
*   Pour plus d’informations sur WebView2, accédez [à Ressources WebView2.][Webview2IndexNextSteps]  
*   Pour plus d’informations sur l’API WebView2, accédez à la référence [d’API.][DotnetApiMicrosoftWebWebview2WinformsWebview2]  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Entrer en contact avec l’équipe web Microsoft Edge WebView  

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
