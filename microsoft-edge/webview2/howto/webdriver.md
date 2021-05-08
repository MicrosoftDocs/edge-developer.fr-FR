---
description: Automatiser et tester le contrôle WebView2 à l’aide Microsoft Edge pilote
title: Automatisation et test de WebView2 avec Microsoft Edge pilote
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, edge, ICoreWebView2, ICoreWebView2Controller, Selenium, Microsoft Edge Driver
ms.openlocfilehash: c23d639582d4ce550406cf955c96171167bde7c8
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536412"
---
# <a name="automating-and-testing-webview2-with-microsoft-edge-driver"></a>Automatisation et test de WebView2 avec Microsoft Edge pilote  

Étant donné que WebView2 utilise la plateforme web Microsoft Edge \(Chromium\), les développeurs WebView2 \(vous\) peuvent tirer parti des outils web standard pour le débogage et l’automatisation.  Selenium est l’un de ces outils.  Il implémente l’API [WebDriver][W3cWebdriver2] W3C.  Vous pouvez utiliser selenium pour créer des tests automatisés afin de simuler les interactions utilisateur.  

Vous pouvez commencer par les étapes suivantes.  

## <a name="step-1--download-webview2api-sample"></a>Étape 1 : Télécharger l’exemple WebView2API  

Si vous n’avez pas de projet WebView2 existant, téléchargez l’exemple d’application [WebView2API][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample], un exemple complet du dernier SDK WebView2.  Assurez-vous que vous avez satisfait aux [conditions préalables pour l’exemple d’application WebView2API.][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]  

Une fois que vous avez cloné le repo, créez le projet dans Visual Studio.  Elle doit ressembler à la figure suivante.  

:::image type="complex" source="../media/webdriver/sample-app.png" alt-text="Exemple d’application WebView2API" lightbox="../media/webdriver/sample-app.png":::
   Exemple d’application WebView2API  
:::image-end:::  

## <a name="step-2--install-microsoft-edge-driver"></a>Étape 2 : Installer Microsoft Edge pilote  

Suivez les instructions pour installer [Microsoft Edge pilote][WebdriverChromiumDownloadMicrosoftEdgeDriver] spécifique au navigateur requis par Selenium pour automatiser et tester WebView2.  

Assurez-vous que la version Microsoft Edge pilote correspond à la version de WebView2 Runtime que votre application utilise.  Pour que l’exemple WebView2API fonctionne, assurez-vous que votre version de WebView2 Runtime est supérieure ou égale à la version prise en charge de la dernière version du SDK WebView2.  Pour rechercher la dernière version du SDK WebView2, accédez aux notes de [publication webView2.][Webview2Releasenotes]  Pour connaître la version de WebView2 Runtime dont vous disposez actuellement, accédez à `edge://settings/help` .  

## <a name="step-3--add-selenium-to-the-webview2api-sample"></a>Étape 3 : Ajouter du selenium à l’exemple WebView2API  

À ce stade, WebView2 Runtime doit être installé, créé un projet WebView2 et installé Microsoft Edge pilote.  À présent, vous pouvez commencer à utiliser Selenium.  

> [!NOTE]
> Selenium prend en charge C\#, Java, Python, Javascript et Ruby.  Toutefois, le guide suivant est écrit en C\#.  

1.  Commencez par créer un projet **C# .NET Framework** dans **Visual Studio**.  Sélectionnez **Suivant** dans le coin inférieur droit pour continuer.  
    
    :::image type="complex" source="../media/webdriver/new-project.png" alt-text="Create a new project (Créer un projet)" lightbox="../media/webdriver/new-project.png":::
       Create a new project (Créer un projet)  
    :::image-end:::  
    
1.  Donnez un nom **à votre projet,** enregistrez-le à votre emplacement **préféré,** puis choisissez **Créer.**  
    
    :::image type="complex" source="../media/webdriver/app-create.png" alt-text="Configurer votre nouveau projet" lightbox="../media/webdriver/app-create.png":::
       Configurer votre nouveau projet  
    :::image-end:::  
    
1.  Un nouveau projet est créé.  Dans ce guide, tout le code est écrit dans le `Program.cs` fichier.  
    
    :::image type="complex" source="../media/webdriver/start-app.png" alt-text="Nouveau projet" lightbox="../media/webdriver/start-app.png":::
       Nouveau projet  
    :::image-end:::  
    
1.  Maintenant, **ajoutez selenium** au projet.  Installez Selenium à l’aide **du package NuGet Selenium.WebDriver.**  
    
    Pour télécharger le **package NuGet Selenium.WebDriver,** dans **Visual Studio,** pointez sur **Project**et choisissez Gérer **NuGet package.**  L’écran suivant doit apparaître.  
    
    :::image type="complex" source="../media/webdriver/download-nuget.png" alt-text="Télécharger NuGet package" lightbox="../media/webdriver/download-nuget.png":::
       Télécharger NuGet package  
    :::image-end:::  
    
1.  Entrez dans la barre de recherche, choisissez `Selenium.WebDriver` **Selenium.WebDriver** dans les résultats et assurez-vous de cochez la case en regard de la **pré-version.**  Dans la fenêtre de droite, assurez-vous que la **version** est définie pour installer **4.0.0-alpha04 ou** version ultérieure et choisissez **Installer**.  NuGet télécharge Selenium sur votre ordinateur.  
    
    Pour en savoir plus sur le package NuGet Selenium.WebDriver, accédez à [Selenium.WebDriver 4.0.0-alpha04.][NugetSeleniumWebdriver400Alpha04]  
    
    :::image type="complex" source="../media/webdriver/nuget.png" alt-text="Gérer NuGet package" lightbox="../media/webdriver/nuget.png":::
       Gérer NuGet package  
    :::image-end:::  
    
1.  À `OpenQA.Selenium.Edge` utiliser en ajoutant l’instruction suivante : au début du  `using OpenQA.Selenium.Edge;` `Program.cs` fichier.  
    
    ```csharp
    using OpenQA.Selenium.Edge;
    
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;
    ```  
    
## <a name="step-4-drive-webview2-with-selenium-and-microsoft-edge-driver"></a>Étape 4 : Lecteur WebView2 avec selenium et Microsoft Edge pilote  

1.  Tout d’abord, `EdgeOptions` créez l’objet en copiant l’extrait de code suivant.  
    
    ```csharp
    static void Main(string[] args)
    {
        // EdgeOptions() requires using OpenQA.Selenium.Edge
        // Construct EdgeOptions with is_legacy = false and the string "webview2"
        EdgeOptions edgeOptions = new EdgeOptions(false, "webview2");
    ```  
    
    `EdgeOptions`L’objet prend les deux paramètres suivants.  
    
    | Paramètre | Détails |    
    |:--- |:--- |  
    | `is_legacy` | Définissez `false` sur , qui indique à Selenium que vous êtes à la base de Chromium navigateur Microsoft Edge navigateur. |  
    | `"webview2"` | Chaîne qui indique à Selenium que vous êtes au volant de WebView2. |  
    
1.  Ensuite, définissez le chemin d’accès au fichier de votre runtime de projet WebView2, créez une chaîne nommée qui fournit le chemin d’accès du fichier à l’endroit où vous avez installé Microsoft Edge Driver et créez une chaîne nommée pour stocker le nom du runtime du pilote `edgeOptions.BinaryLocation` `msedgedriverDir` [][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads] `msedgedriverExe` Microsoft Edge.  Par défaut, le runtime est nommé `msedgedriver.exe` . Utilisez ces deux chaînes pour construire `EdgeDriverService` l’objet comme illustré ci-dessous.  Enfin, créez `EdgeDriver` l’objet à `EdgeDriverService` l’aide et `EdgeOptions` .  
    
    Vous pouvez copier et coller le code suivant sous `edgeOptions` .  Veillez à spécifier les chemins d’accès aux fichiers corrects pour le runtime de votre projet et le runtime Microsoft Edge pilote sur votre ordinateur.  
    
    ```csharp
    //Set the BinaryLocation to the filepath of the WebView2API Sample runtime
    edgeOptions.BinaryLocation = @"C:\path\to\your\webview2\project.exe";
    
    //Set msedgedriverDir to the filepath of the directory housing msedgedriver.exe
    string msedgedriverDir = @"C:\path\to\your\msededriver.exe's\directory";
    
    //Set msedgedriverExe to the name of the Edge Driver. By default it is:
    string msedgedriverExe = @"msedgedriver.exe";
    
    // Construct EdgeDriverService with is_legacy = false  
    EdgeDriverService service = EdgeDriverService.CreateDefaultService(msedgedriverDir, msedgedriverExe, false);
    
    EdgeDriver e = new EdgeDriver(service, edgeOptions);
    ```
    
3.  À présent, `EdgeDriver` est configuré pour piloter WebView2 dans votre projet.  Par exemple, si vous utilisez l’exemple **WebView2API,** vous pouvez accéder `https://microsoft.com` en exécutant la `e.Url = @"https://www.microsoft.com";` commande.  Vérifiez le lecteur Selenium WebView2 en fixant un point d’arrêt sur la ligne et en exécutant le projet.  
    
    ```csharp
        //The following navigates the WebView2API Sample from bing.com to microsoft.com
        e.Url = @"https://www.microsoft.com";
        
        //This exits the edge driver
        e.Quit();
    }
    ```  
    
    :::image type="complex" source="../media/webdriver/microsoft.png" alt-text="Selenium exécutant WebView2" lightbox="../media/webdriver/microsoft.png":::
       Selenium exécutant WebView2  
    :::image-end:::

Félicitations.  Vous avez réussi à automatiser un projet WebView2 et piloté WebView2 à l’aide de Selenium et Microsoft Edge Driver.  

## <a name="see-also"></a>Voir également  

*   Pour un aperçu complet de la façon dont les API Selenium pilotent WebView2 ou Microsoft Edge \(Chromium\), accédez à WebDriver sur la [documentation Selenium][SeleniumWebdriver]   
*   Pour en savoir plus sur le contrôle WebView2 et comment l’utiliser lors de l’incorporation de contenu web dans votre application native, accédez à Introduction à [Microsoft Edge WebView2][WebViewIndex].  
*   Pour en savoir plus sur l’automatisation Microsoft Edge \(Chromium\), accédez à Utiliser [WebDriver (Chromium)][WebdriverChromium] pour tester l’automatisation   
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Entrer en contact avec l’équipe web Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WebdriverChromium]: ../../webdriver-chromium/index.md "Utiliser WebDriver (Chromium) pour tester l’automatisation | Documents Microsoft"  
[WebdriverChromiumDownloadMicrosoftEdgeDriver]: ../../webdriver-chromium/index.md#download-microsoft-edge-driver "Télécharger Microsoft Edge pilote : utiliser WebDriver (Chromium) pour tester l’automatisation | Documents Microsoft"  
[WebViewIndex]: ../index.md "Présentation de Microsoft Edge WebView2 - Microsoft Docs"  
[Webview2Releasenotes]: ../releasenotes.md "Notes de publication du SDK WebView2 | Documents Microsoft"  

[MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Télécharger la | WebDriver Microsoft Edge Développeur"  

[GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Exemple d’API WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample#prerequisites "Conditions préalables : exemple d’API WebView2 | GitHub"  

[NugetSeleniumWebdriver400Alpha04]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha04 "Selenium.WebDriver 4.0.0-alpha04 | NuGet Galerie"  

[SeleniumWebdriver]: https://www.selenium.dev/documentation/en/webdriver "WebDriver | Selenium"  

[W3cWebdriver2]: https://www.w3.org/TR/webdriver2 "WebDriver | W3C"  
