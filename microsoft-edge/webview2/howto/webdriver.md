---
description: Automatiser et tester le contrôle WebView2 à l’aide du pilote Microsoft Edge
title: Automatisation et test de WebView2 avec le pilote Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/24/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Edge, ICoreWebView2, ICoreWebView2Controller, sélénium, pilote Microsoft Edge
ms.openlocfilehash: 6f7f84fa88a57e54d7b5143a489d1138c7426d88
ms.sourcegitcommit: 652c345b46aae8b7e3723eb55a01b71a4ef76bf0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/25/2020
ms.locfileid: "11191449"
---
# <span data-ttu-id="ca223-104">Automatisation et test de WebView2 avec le pilote Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ca223-104">Automating and testing WebView2 with Microsoft Edge Driver</span></span>  

<span data-ttu-id="ca223-105">Dans la mesure où WebView2 utilise la plate-forme Web Microsoft Edge (chrome), les développeurs WebView2 \ (vous \) peuvent tirer parti d’outils Web standard pour le débogage et l’automatisation.</span><span class="sxs-lookup"><span data-stu-id="ca223-105">Because WebView2 uses the Microsoft Edge \(Chromium\) web platform, WebView2 developers \(you\) may take advantage of standard web tooling for debugging and automation.</span></span>  <span data-ttu-id="ca223-106">Le sélénium est un de ces outils.</span><span class="sxs-lookup"><span data-stu-id="ca223-106">Selenium is one such tool.</span></span>  <span data-ttu-id="ca223-107">Il implémente l’API [WebDriver][W3cWebdriver2] W3C.</span><span class="sxs-lookup"><span data-stu-id="ca223-107">It implements the W3C [WebDriver][W3cWebdriver2] API.</span></span>  <span data-ttu-id="ca223-108">Vous pouvez utiliser le sélénium pour créer des tests automatisés pour simuler les interactions utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ca223-108">You may use Selenium to create automated tests to simulate user interactions.</span></span>  

<span data-ttu-id="ca223-109">Familiarisez-vous avec les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="ca223-109">Get started with the following steps.</span></span>  

## <span data-ttu-id="ca223-110">Étape 1: Télécharger l’exemple WebView2API</span><span class="sxs-lookup"><span data-stu-id="ca223-110">Step 1: Download WebView2API Sample</span></span>  

<span data-ttu-id="ca223-111">Si vous n’avez pas de projet WebView2 existant, téléchargez l' [exemple d’application WebView2API][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample], un exemple complet du SDK WebView2 le plus récent.</span><span class="sxs-lookup"><span data-stu-id="ca223-111">If you do not have an existing WebView2 project, download the [WebView2API Sample app][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample], a comprehensive sample of the latest WebView2 SDK.</span></span>  <span data-ttu-id="ca223-112">Vérifiez que vous avez satisfait la [Configuration requise pour l’exemple d’application WebView2API][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites].</span><span class="sxs-lookup"><span data-stu-id="ca223-112">Ensure you have satisfied the [prerequisites for the WebView2API Sample app][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites].</span></span> 

<span data-ttu-id="ca223-113">Une fois que vous avez cloné le référentiel samples, générez le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ca223-113">Once you have cloned the repo, build the project in Visual Studio.</span></span>  <span data-ttu-id="ca223-114">Il doit ressembler à la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="ca223-114">It should look like the following figure.</span></span>  

:::image type="complex" source="../media/webdriver/sample-app.png" alt-text="Exemple d’application WebView2API" lightbox="../media/webdriver/sample-app.png":::
   <span data-ttu-id="ca223-116">Exemple d’application WebView2API</span><span class="sxs-lookup"><span data-stu-id="ca223-116">WebView2API Sample app</span></span>  
:::image-end:::  

## <span data-ttu-id="ca223-117">Étape 2: installer le pilote Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ca223-117">Step 2: Install Microsoft Edge Driver</span></span>  

<span data-ttu-id="ca223-118">Suivez les instructions pour installer le [pilote Microsoft Edge][WebdriverChromiumDownloadMicrosoftEdgeDriver] le pilote spécifique au navigateur requis par sélénium pour automatiser et tester WebView2.</span><span class="sxs-lookup"><span data-stu-id="ca223-118">Follow the instructions to install [Microsoft Edge Driver][WebdriverChromiumDownloadMicrosoftEdgeDriver] the browser-specific driver required by Selenium to automate and test WebView2.</span></span>  

<span data-ttu-id="ca223-119">Assurez-vous que la version du pilote Microsoft Edge correspond à la version de WebView2 Runtime utilisée par votre application.</span><span class="sxs-lookup"><span data-stu-id="ca223-119">Ensure that the version of Microsoft Edge Driver matches the version of WebView2 Runtime that you app uses.</span></span>  <span data-ttu-id="ca223-120">Pour que l’exemple WebView2API fonctionne, assurez-vous que votre version de WebView2 Runtime est supérieure ou égale à la version prise en charge de la version la plus récente du SDK WebView2.</span><span class="sxs-lookup"><span data-stu-id="ca223-120">For the WebView2API Sample to work, make sure that your version of WebView2 Runtime is greater than or equal than the supported version of the latest WebView2 SDK release.</span></span>  <span data-ttu-id="ca223-121">Pour trouver la version la plus récente du SDK WebView2, accédez à [WebView2 notes de publication][Webview2Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="ca223-121">To locate the latest WebView2 SDK release, navigate to [WebView2 release notes][Webview2Releasenotes].</span></span>  <span data-ttu-id="ca223-122">Pour identifier la version de WebView2 Runtime dont vous disposez, accédez à `edge://settings/help` .</span><span class="sxs-lookup"><span data-stu-id="ca223-122">To find out what version of WebView2 Runtime you currently have, navigate to `edge://settings/help`.</span></span>  

## <span data-ttu-id="ca223-123">Étape 3: ajouter du sélénium à l’exemple WebView2API</span><span class="sxs-lookup"><span data-stu-id="ca223-123">Step 3: Add Selenium to the WebView2API Sample</span></span>  

<span data-ttu-id="ca223-124">À ce stade, vous devez disposer de WebView2 Runtime, de la création d’un projet WebView2 et de l’installation d’un pilote Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ca223-124">At this point you should have WebView2 Runtime installed, built a WebView2 project, and installed Microsoft Edge Driver.</span></span>  <span data-ttu-id="ca223-125">À présent, commencez à utiliser sélénium.</span><span class="sxs-lookup"><span data-stu-id="ca223-125">Now, get started using Selenium.</span></span>  

> [!NOTE]
> <span data-ttu-id="ca223-126">Sélénium prend en charge les langages C \ #, Java, Python, JavaScript et Ruby.</span><span class="sxs-lookup"><span data-stu-id="ca223-126">Selenium supports C\#, Java, Python, Javascript, and Ruby.</span></span>  <span data-ttu-id="ca223-127">Toutefois, le guide suivant est écrit en C \ #.</span><span class="sxs-lookup"><span data-stu-id="ca223-127">However, the following guide is written using C\#.</span></span>  

1.  <span data-ttu-id="ca223-128">Commencez par créer un projet **.NET Framework C#** dans **Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="ca223-128">Start by creating a new **C# .NET Framework** project in **Visual Studio**.</span></span>  <span data-ttu-id="ca223-129">Dans le coin inférieur droit, sélectionnez **Next (suivant** ) pour continuer.</span><span class="sxs-lookup"><span data-stu-id="ca223-129">Choose **Next** on the bottom right-hand corner to continue.</span></span>  
    
    :::image type="complex" source="../media/webdriver/new-project.png" alt-text="Create a new project (Créer un projet)" lightbox="../media/webdriver/new-project.png":::
       <span data-ttu-id="ca223-131">Create a new project (Créer un projet)</span><span class="sxs-lookup"><span data-stu-id="ca223-131">Create a new project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ca223-132">Donnez un **nom**à votre projet, enregistrez-le dans votre **emplacement**préféré et sélectionnez **créer**.</span><span class="sxs-lookup"><span data-stu-id="ca223-132">Give your project a **name**, save it to your preferred **location**, and choose **Create**.</span></span>  
    
    :::image type="complex" source="../media/webdriver/app-create.png" alt-text="Configurer votre nouveau projet" lightbox="../media/webdriver/app-create.png":::
       <span data-ttu-id="ca223-134">Configurer votre nouveau projet</span><span class="sxs-lookup"><span data-stu-id="ca223-134">Configure your new project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ca223-135">Un nouveau projet est créé.</span><span class="sxs-lookup"><span data-stu-id="ca223-135">A new project is created.</span></span>  <span data-ttu-id="ca223-136">Dans ce guide, le code est écrit sur le `Program.cs` fichier.</span><span class="sxs-lookup"><span data-stu-id="ca223-136">In this guide, all code is written to the `Program.cs` file.</span></span>  
    
    :::image type="complex" source="../media/webdriver/start-app.png" alt-text="Nouveau projet" lightbox="../media/webdriver/start-app.png":::
       <span data-ttu-id="ca223-138">Nouveau projet</span><span class="sxs-lookup"><span data-stu-id="ca223-138">New project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ca223-139">Ajoutez **sélénium** au projet.</span><span class="sxs-lookup"><span data-stu-id="ca223-139">Now add **Selenium** to the project.</span></span>  <span data-ttu-id="ca223-140">Installez le sélénium en utilisant le **package NuGet. WebDriver de sélénium**.</span><span class="sxs-lookup"><span data-stu-id="ca223-140">Install Selenium using the **Selenium.WebDriver NuGet package**.</span></span>  
    
    <span data-ttu-id="ca223-141">Pour télécharger le **package NuGet. WebDriver de sélénium**, dans **Visual Studio**, placez le pointeur sur **Project**, puis sélectionnez **Manage NuGet package**.</span><span class="sxs-lookup"><span data-stu-id="ca223-141">To download the **Selenium.WebDriver NuGet package**, in **Visual Studio**, hover over **Project**, and choose **Manage NuGet Package**.</span></span>  <span data-ttu-id="ca223-142">L’écran suivant doit apparaître.</span><span class="sxs-lookup"><span data-stu-id="ca223-142">The following screen should appear.</span></span>  
    
    :::image type="complex" source="../media/webdriver/download-nuget.png" alt-text="Télécharger le package NuGet" lightbox="../media/webdriver/download-nuget.png":::
       <span data-ttu-id="ca223-144">Télécharger le package NuGet</span><span class="sxs-lookup"><span data-stu-id="ca223-144">Download NuGet package</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ca223-145">Entrez **sélénium. WebDriver** dans la barre de recherche, sélectionnez **sélénium. WebDriver** dans les résultats, puis activez la case à cocher en regard de **inclure la version préliminaire**.</span><span class="sxs-lookup"><span data-stu-id="ca223-145">Enter **Selenium.WebDriver** in the search bar, choose **Selenium.WebDriver** from the results, and make sure to checkmark the box next to **include pre-release**.</span></span> <span data-ttu-id="ca223-146">Dans la fenêtre de droite, assurez-vous que la **version** est définie pour **Installer 4.0.0-alpha04** ou version ultérieure, puis sélectionnez **installer**.</span><span class="sxs-lookup"><span data-stu-id="ca223-146">On the right-hand side window, ensure the **Version** is set to **install 4.0.0-alpha04** or later and choose **Install**.</span></span>  <span data-ttu-id="ca223-147">NuGet télécharge sélénium sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ca223-147">Nuget downloads Selenium to your machine.</span></span>  
    
    <span data-ttu-id="ca223-148">Pour en savoir plus sur le package NuGet. WebDriver de sélénium, accédez à [sélénium. WebDriver 4.0.0-alpha04][NugetSeleniumWebdriver400Alpha04].</span><span class="sxs-lookup"><span data-stu-id="ca223-148">To learn more about the Selenium.WebDriver NuGet package, navigate to [Selenium.WebDriver 4.0.0-alpha04][NugetSeleniumWebdriver400Alpha04].</span></span>  
    
    :::image type="complex" source="../media/webdriver/nuget.png" alt-text="Gérer le package NuGet" lightbox="../media/webdriver/nuget.png":::
       <span data-ttu-id="ca223-150">Gérer le package NuGet</span><span class="sxs-lookup"><span data-stu-id="ca223-150">Manage NuGet package</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ca223-151">Utilisez `OpenQA.Selenium.Edge` en ajoutant l’instruction suivante:  `using OpenQA.Selenium.Edge;` au début du `Program.cs` fichier.</span><span class="sxs-lookup"><span data-stu-id="ca223-151">Use `OpenQA.Selenium.Edge` by adding the following statement:  `using OpenQA.Selenium.Edge;` at the beginning of `Program.cs` file.</span></span>  
    
    ```csharp
    using OpenQA.Selenium.Edge;
    
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;
    ```  
    
## <span data-ttu-id="ca223-152">Étape 4: piloter WebView2 avec sélénium et pilote Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ca223-152">Step 4: Drive WebView2 with Selenium and Microsoft Edge Driver</span></span>  

1.  <span data-ttu-id="ca223-153">Tout d’abord, créez l' `EdgeOptions` objet en copiant l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="ca223-153">First, create the `EdgeOptions` object, by copying the following code snippet.</span></span>  
    
    ```csharp
    static void Main(string[] args)
    {
        // EdgeOptions() requires using OpenQA.Selenium.Edge
        // Construct EdgeOptions with is_legacy = false and the string "webview2"
        EdgeOptions edgeOptions = new EdgeOptions(false, "webview2");
    ```  
    
    <span data-ttu-id="ca223-154">L' `EdgeOptions` objet accepte les deux paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="ca223-154">The `EdgeOptions` object takes in the following two parameters.</span></span>  
    
    | <span data-ttu-id="ca223-155">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ca223-155">Parameter</span></span> | <span data-ttu-id="ca223-156">Détails</span><span class="sxs-lookup"><span data-stu-id="ca223-156">Details</span></span> |    
    |:--- |:--- |  
    | `is_legacy` | <span data-ttu-id="ca223-157">Définissez la valeur sur `false` , qui indique au sélénium que vous dirigez le nouveau navigateur Microsoft Edge basé sur le chrome.</span><span class="sxs-lookup"><span data-stu-id="ca223-157">Set to `false`, which tells Selenium that you are driving the new Chromium-based Microsoft Edge browser.</span></span> |  
    | `"webview2"` | <span data-ttu-id="ca223-158">Chaîne indiquant au sélénium que vous entrainez WebView2.</span><span class="sxs-lookup"><span data-stu-id="ca223-158">A string that tells Selenium you are driving WebView2.</span></span> |  
    
1.  <span data-ttu-id="ca223-159">Ensuite, définissez `edgeOptions.BinaryLocation` le chemin d’accès de fichier de votre WebView2 Project Runtime, créez une chaîne nommée `msedgedriverDir` qui fournit le chemin d’accès au fichier où vous avez installé le [pilote Microsoft Edge][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads], puis créez une chaîne nommée `msedgedriverExe` pour stocker le nom du runtime du pilote Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ca223-159">Next, set `edgeOptions.BinaryLocation` to the file path of your WebView2 project runtime, create a string named `msedgedriverDir` that provides the file path to where you installed [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads], and create a string named `msedgedriverExe` to store the name of the Microsoft Edge Driver runtime.</span></span>  <span data-ttu-id="ca223-160">Par défaut, le runtime est appelé `msedgedriver.exe` .</span><span class="sxs-lookup"><span data-stu-id="ca223-160">By default, the runtime is named `msedgedriver.exe`.</span></span> <span data-ttu-id="ca223-161">Utilisez ces deux chaînes pour créer l' `EdgeDriverService` objet, comme illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="ca223-161">Use these two strings to construct the `EdgeDriverService` object as shown below.</span></span>  <span data-ttu-id="ca223-162">Enfin, créez l' `EdgeDriver` objet à l’aide `EdgeDriverService` de et `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="ca223-162">Finally, create the `EdgeDriver` object using `EdgeDriverService` and `EdgeOptions`.</span></span>  
    
    <span data-ttu-id="ca223-163">Vous pouvez copier-coller le code suivant `edgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="ca223-163">You may copy and paste the following code underneath `edgeOptions`.</span></span>  <span data-ttu-id="ca223-164">Assurez-vous de spécifier les chemins d’accès aux fichiers appropriés pour le runtime de Project et le runtime du pilote Microsoft Edge sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ca223-164">Ensure you specify the correct file paths to your project runtime and the Microsoft Edge Driver runtime on your machine.</span></span>  
    
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
    
3.  <span data-ttu-id="ca223-165">Maintenant, `EdgeDriver` est configuré pour piloter le WebView2 de votre projet.</span><span class="sxs-lookup"><span data-stu-id="ca223-165">Now, `EdgeDriver` is configured to drive the WebView2 in your project.</span></span>  <span data-ttu-id="ca223-166">Par exemple, si vous utilisez l' **exemple WebView2API**, vous pouvez y accéder `https://microsoft.com` en exécutant la `e.Url = @"https://www.microsoft.com";` commande.</span><span class="sxs-lookup"><span data-stu-id="ca223-166">For example, if you are using the **WebView2API Sample**, you may navigate to `https://microsoft.com` by running the `e.Url = @"https://www.microsoft.com";` command.</span></span>  <span data-ttu-id="ca223-167">Vérifiez le facteur d’WebView2 d’sélénium en définissant un point d’arrêt sur la ligne et en exécutant le projet.</span><span class="sxs-lookup"><span data-stu-id="ca223-167">Verify the Selenium drive WebView2 by setting a breakpoint on the line and running the project.</span></span>  
    
    ```csharp
        //The following navigates the WebView2API Sample from bing.com to microsoft.com
        e.Url = @"https://www.microsoft.com";
        
        //This exits the edge driver
        e.Quit();
    }
    ```  
    
    :::image type="complex" source="../media/webdriver/microsoft.png" alt-text="Sélénium exécutant WebView2" lightbox="../media/webdriver/microsoft.png":::
       <span data-ttu-id="ca223-169">Sélénium exécutant WebView2</span><span class="sxs-lookup"><span data-stu-id="ca223-169">Selenium running WebView2</span></span>  
    :::image-end:::

<span data-ttu-id="ca223-170">Félicitations.</span><span class="sxs-lookup"><span data-stu-id="ca223-170">Congratulations.</span></span>  <span data-ttu-id="ca223-171">Vous avez correctement automatisé un projet WebView2 et WebView2 piloté par le biais du pilote sélénium et Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ca223-171">You have successfully automated a WebView2 project and driven WebView2 using Selenium and Microsoft Edge Driver.</span></span>  

## <span data-ttu-id="ca223-172">Voir également</span><span class="sxs-lookup"><span data-stu-id="ca223-172">See also</span></span>  

*   <span data-ttu-id="ca223-173">Pour obtenir une vue d’ensemble de la façon dont les API sélénium pilotent WebView2 ou Microsoft Edge \ (chrome \), accédez à [la documentation sur le][SeleniumWebdriver] Web pour le sélénium.</span><span class="sxs-lookup"><span data-stu-id="ca223-173">For a comprehensive look at how the APIs Selenium drives WebView2 or Microsoft Edge \(Chromium\), navigate to [WebDriver on Selenium documentation][SeleniumWebdriver]</span></span>   
*   <span data-ttu-id="ca223-174">Pour en savoir plus sur le contrôle WebView2 et son utilisation lors de l’incorporation de contenu Web dans votre application native, accédez à la section [Présentation de Microsoft Edge WebView2][WebViewIndex].</span><span class="sxs-lookup"><span data-stu-id="ca223-174">To learn more about WebView2 control and how to use it when embedding web content in your native app, navigate to [Introduction to Microsoft Edge WebView2][WebViewIndex].</span></span>  
*   <span data-ttu-id="ca223-175">Pour en savoir plus sur l’automatisation de Microsoft Edge \ (chrome \), accédez à la section [utilisation de WebDriver (chrome) pour l’automatisation des tests][WebdriverChromium] .</span><span class="sxs-lookup"><span data-stu-id="ca223-175">To learn more about automating Microsoft Edge \(Chromium\), navigate to [Use WebDriver (Chromium) for test automation][WebdriverChromium]</span></span>   
    
## <span data-ttu-id="ca223-176">Contacter l’équipe WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ca223-176">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WebdriverChromium]: ../../webdriver-chromium.md "Utiliser le WebDriver (chrome) pour l’automatisation des tests | Documents Microsoft"  
[WebdriverChromiumDownloadMicrosoftEdgeDriver]: ../../webdriver-chromium.md#download-microsoft-edge-driver "Télécharger le pilote Microsoft Edge-utiliser le WebDriver (chrome) pour l’automatisation des tests | Documents Microsoft"  
[WebViewIndex]: ../index.md "Introduction à Microsoft Edge WebView2-documentation Microsoft"  
[Webview2Releasenotes]: ../releasenotes.md "Notes de publication pour WebView2 SDK | Documents Microsoft"  

[MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Télécharger WebDriver | Développeur pour Microsoft Edge"  

[GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Exemple d’API WebView2-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample#prerequisites "Prérequis-exemple d’API WebView2 | GitHub"  

[NugetSeleniumWebdriver400Alpha04]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha04 "Sélénium. WebDriver 4.0.0-alpha04 | Galerie NuGet"  

[SeleniumWebdriver]: https://www.selenium.dev/documentation/en/webdriver "Web Driver | Sélénium"  

[W3cWebdriver2]: https://www.w3.org/TR/webdriver2 "Web Driver | W3C"  
