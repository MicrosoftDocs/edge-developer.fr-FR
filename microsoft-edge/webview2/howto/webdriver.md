---
description: Automatiser et tester le contrôle WebView2 à l’aide du pilote Microsoft Edge
title: Automatisation et test de WebView2 avec le pilote Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Edge, ICoreWebView2, ICoreWebView2Controller, sélénium, pilote Microsoft Edge
ms.openlocfilehash: 2af1ce222abb1dc7a279afc05e87e7e42a45fe9e
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "11191616"
---
# Automatisation et test de WebView2 avec le pilote Microsoft Edge  

Dans la mesure où WebView2 utilise la plate-forme Web Microsoft Edge (chrome), les développeurs WebView2 \ (vous \) peuvent tirer parti d’outils Web standard pour le débogage et l’automatisation.  Le sélénium est un de ces outils.  Il implémente l’API [WebDriver][W3cWebdriver2] W3C.  Vous pouvez utiliser le sélénium pour créer des tests automatisés pour simuler les interactions utilisateur.  

Familiarisez-vous avec les étapes suivantes.  

## Étape 1: Télécharger l’exemple WebView2API  

Si vous n’avez pas de projet WebView2 existant, téléchargez l' [exemple d’application WebView2API][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample], un exemple complet du SDK WebView2 le plus récent.  Vérifiez que vous avez satisfait la [Configuration requise pour l’exemple d’application WebView2API][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites].  

Une fois que vous avez cloné le référentiel samples, générez le projet dans Visual Studio.  Il doit ressembler à la figure suivante.  

:::image type="complex" source="../media/webdriver/sample-app.png" alt-text="Exemple d’application WebView2API" lightbox="../media/webdriver/sample-app.png":::
   Exemple d’application WebView2API  
:::image-end:::  

## Étape 2: installer le pilote Microsoft Edge  

Suivez les instructions pour installer le [pilote Microsoft Edge][WebdriverChromiumDownloadMicrosoftEdgeDriver] le pilote spécifique au navigateur requis par sélénium pour automatiser et tester WebView2.  

Assurez-vous que la version du pilote Microsoft Edge correspond à la version de WebView2 Runtime utilisée par votre application.  Pour que l’exemple WebView2API fonctionne, assurez-vous que votre version de WebView2 Runtime est supérieure ou égale à la version prise en charge de la version la plus récente du SDK WebView2.  Pour trouver la version la plus récente du SDK WebView2, accédez à [WebView2 notes de publication][Webview2Releasenotes].  Pour identifier la version de WebView2 Runtime dont vous disposez, accédez à `edge://settings/help` .  

## Étape 3: ajouter du sélénium à l’exemple WebView2API  

À ce stade, vous devez disposer de WebView2 Runtime, de la création d’un projet WebView2 et de l’installation d’un pilote Microsoft Edge.  À présent, commencez à utiliser sélénium.  

> [!NOTE]
> Sélénium prend en charge les langages C \ #, Java, Python, JavaScript et Ruby.  Toutefois, le guide suivant est écrit en C \ #.  

1.  Commencez par créer un projet **.NET Framework C#** dans **Visual Studio**.  Dans le coin inférieur droit, sélectionnez **Next (suivant** ) pour continuer.  
    
    :::image type="complex" source="../media/webdriver/new-project.png" alt-text="Create a new project (Créer un projet)" lightbox="../media/webdriver/new-project.png":::
       Create a new project (Créer un projet)  
    :::image-end:::  
    
1.  Donnez un **nom**à votre projet, enregistrez-le dans votre **emplacement**préféré et sélectionnez **créer**.  
    
    :::image type="complex" source="../media/webdriver/app-create.png" alt-text="Configurer votre nouveau projet" lightbox="../media/webdriver/app-create.png":::
       Configurer votre nouveau projet  
    :::image-end:::  
    
1.  Un nouveau projet est créé.  Dans ce guide, le code est écrit sur le `Program.cs` fichier.  
    
    :::image type="complex" source="../media/webdriver/start-app.png" alt-text="Nouveau projet" lightbox="../media/webdriver/start-app.png":::
       Nouveau projet  
    :::image-end:::  
    
1.  Ajoutez **sélénium** au projet.  Installez le sélénium en utilisant le **package NuGet. WebDriver de sélénium**.  
    
    Pour télécharger le **package NuGet. WebDriver de sélénium**, dans **Visual Studio**, placez le pointeur sur **Project**, puis sélectionnez **Manage NuGet package**.  L’écran suivant doit apparaître.  
    
    :::image type="complex" source="../media/webdriver/download-nuget.png" alt-text="Télécharger le package NuGet" lightbox="../media/webdriver/download-nuget.png":::
       Télécharger le package NuGet  
    :::image-end:::  
    
1.  Entrez `Selenium.WebDriver` dans la barre de recherche, sélectionnez **sélénium. WebDriver** dans les résultats, puis activez la case à cocher en regard de **inclure la version préliminaire**.  Dans la fenêtre de droite, assurez-vous que la **version** est définie pour **Installer 4.0.0-alpha04** ou version ultérieure, puis sélectionnez **installer**.  NuGet télécharge sélénium sur votre ordinateur.  
    
    Pour en savoir plus sur le package NuGet. WebDriver de sélénium, accédez à [sélénium. WebDriver 4.0.0-alpha04][NugetSeleniumWebdriver400Alpha04].  
    
    :::image type="complex" source="../media/webdriver/nuget.png" alt-text="Gérer le package NuGet" lightbox="../media/webdriver/nuget.png":::
       Gérer le package NuGet  
    :::image-end:::  
    
1.  Utilisez `OpenQA.Selenium.Edge` en ajoutant l’instruction suivante:  `using OpenQA.Selenium.Edge;` au début du `Program.cs` fichier.  
    
    ```csharp
    using OpenQA.Selenium.Edge;
    
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;
    ```  
    
## Étape 4: piloter WebView2 avec sélénium et pilote Microsoft Edge  

1.  Tout d’abord, créez l' `EdgeOptions` objet en copiant l’extrait de code suivant.  
    
    ```csharp
    static void Main(string[] args)
    {
        // EdgeOptions() requires using OpenQA.Selenium.Edge
        // Construct EdgeOptions with is_legacy = false and the string "webview2"
        EdgeOptions edgeOptions = new EdgeOptions(false, "webview2");
    ```  
    
    L' `EdgeOptions` objet accepte les deux paramètres suivants.  
    
    | Paramètre | Détails |    
    |:--- |:--- |  
    | `is_legacy` | Définissez la valeur sur `false` , qui indique au sélénium que vous dirigez le nouveau navigateur Microsoft Edge basé sur le chrome. |  
    | `"webview2"` | Chaîne indiquant au sélénium que vous entrainez WebView2. |  
    
1.  Ensuite, définissez `edgeOptions.BinaryLocation` le chemin d’accès de fichier de votre WebView2 Project Runtime, créez une chaîne nommée `msedgedriverDir` qui fournit le chemin d’accès au fichier où vous avez installé le [pilote Microsoft Edge][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads], puis créez une chaîne nommée `msedgedriverExe` pour stocker le nom du runtime du pilote Microsoft Edge.  Par défaut, le runtime est appelé `msedgedriver.exe` . Utilisez ces deux chaînes pour créer l' `EdgeDriverService` objet, comme illustré ci-dessous.  Enfin, créez l' `EdgeDriver` objet à l’aide `EdgeDriverService` de et `EdgeOptions` .  
    
    Vous pouvez copier-coller le code suivant `edgeOptions` .  Assurez-vous de spécifier les chemins d’accès aux fichiers appropriés pour le runtime de Project et le runtime du pilote Microsoft Edge sur votre ordinateur.  
    
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
    
3.  Maintenant, `EdgeDriver` est configuré pour piloter le WebView2 de votre projet.  Par exemple, si vous utilisez l' **exemple WebView2API**, vous pouvez y accéder `https://microsoft.com` en exécutant la `e.Url = @"https://www.microsoft.com";` commande.  Vérifiez le facteur d’WebView2 d’sélénium en définissant un point d’arrêt sur la ligne et en exécutant le projet.  
    
    ```csharp
        //The following navigates the WebView2API Sample from bing.com to microsoft.com
        e.Url = @"https://www.microsoft.com";
        
        //This exits the edge driver
        e.Quit();
    }
    ```  
    
    :::image type="complex" source="../media/webdriver/microsoft.png" alt-text="Sélénium exécutant WebView2" lightbox="../media/webdriver/microsoft.png":::
       Sélénium exécutant WebView2  
    :::image-end:::

Félicitations.  Vous avez correctement automatisé un projet WebView2 et WebView2 piloté par le biais du pilote sélénium et Microsoft Edge.  

## Voir également  

*   Pour obtenir une vue d’ensemble de la façon dont les API sélénium pilotent WebView2 ou Microsoft Edge \ (chrome \), accédez à [la documentation sur le][SeleniumWebdriver] Web pour le sélénium.   
*   Pour en savoir plus sur le contrôle WebView2 et son utilisation lors de l’incorporation de contenu Web dans votre application native, accédez à la section [Présentation de Microsoft Edge WebView2][WebViewIndex].  
*   Pour en savoir plus sur l’automatisation de Microsoft Edge \ (chrome \), accédez à la section [utilisation de WebDriver (chrome) pour l’automatisation des tests][WebdriverChromium] .   
    
## Contacter l’équipe WebView de Microsoft Edge  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WebdriverChromium]: ../../webdriver-chromium/index.md "Utiliser le WebDriver (chrome) pour l’automatisation des tests | Documents Microsoft"  
[WebdriverChromiumDownloadMicrosoftEdgeDriver]: ../../webdriver-chromium/index.md#download-microsoft-edge-driver "Télécharger le pilote Microsoft Edge-utiliser le WebDriver (chrome) pour l’automatisation des tests | Documents Microsoft"  
[WebViewIndex]: ../index.md "Introduction à Microsoft Edge WebView2-documentation Microsoft"  
[Webview2Releasenotes]: ../releasenotes.md "Notes de publication pour WebView2 SDK | Documents Microsoft"  

[MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Télécharger WebDriver | Développeur pour Microsoft Edge"  

[GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Exemple d’API WebView2-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample#prerequisites "Prérequis-exemple d’API WebView2 | GitHub"  

[NugetSeleniumWebdriver400Alpha04]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha04 "Sélénium. WebDriver 4.0.0-alpha04 | Galerie NuGet"  

[SeleniumWebdriver]: https://www.selenium.dev/documentation/en/webdriver "Web Driver | Sélénium"  

[W3cWebdriver2]: https://www.w3.org/TR/webdriver2 "Web Driver | W3C"  
