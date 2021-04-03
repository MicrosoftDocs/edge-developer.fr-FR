---
description: Automatiser et tester le contrôle WebView2 à l’aide du pilote Microsoft Edge
title: Automatisation et test de WebView2 avec le pilote Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, edge, ICoreWebView2, ICoreWebView2Controller, Selenium, Pilote Microsoft Edge
ms.openlocfilehash: c23d639582d4ce550406cf955c96171167bde7c8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11470829"
---
# <a name="automating-and-testing-webview2-with-microsoft-edge-driver"></a><span data-ttu-id="0ba21-104">Automatisation et test de WebView2 avec le pilote Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0ba21-104">Automating and testing WebView2 with Microsoft Edge Driver</span></span>  

<span data-ttu-id="0ba21-105">Étant donné que WebView2 utilise la plateforme web Microsoft Edge \(Chromium\), les développeurs WebView2 \(vous\) peuvent tirer parti des outils web standard pour le débogage et l’automatisation.</span><span class="sxs-lookup"><span data-stu-id="0ba21-105">Because WebView2 uses the Microsoft Edge \(Chromium\) web platform, WebView2 developers \(you\) may take advantage of standard web tooling for debugging and automation.</span></span>  <span data-ttu-id="0ba21-106">Le selenium est l’un de ces outils.</span><span class="sxs-lookup"><span data-stu-id="0ba21-106">Selenium is one such tool.</span></span>  <span data-ttu-id="0ba21-107">Il implémente l’API [WebDriver][W3cWebdriver2] W3C.</span><span class="sxs-lookup"><span data-stu-id="0ba21-107">It implements the W3C [WebDriver][W3cWebdriver2] API.</span></span>  <span data-ttu-id="0ba21-108">Vous pouvez utiliser selenium pour créer des tests automatisés afin de simuler les interactions utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0ba21-108">You may use Selenium to create automated tests to simulate user interactions.</span></span>  

<span data-ttu-id="0ba21-109">Vous pouvez commencer par les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="0ba21-109">Get started with the following steps.</span></span>  

## <a name="step-1--download-webview2api-sample"></a><span data-ttu-id="0ba21-110">Étape 1 : Télécharger l’exemple WebView2API</span><span class="sxs-lookup"><span data-stu-id="0ba21-110">Step 1:  Download WebView2API Sample</span></span>  

<span data-ttu-id="0ba21-111">Si vous n’avez pas de projet WebView2 existant, téléchargez l’exemple d’application [WebView2API][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample], un exemple complet du dernier SDK WebView2.</span><span class="sxs-lookup"><span data-stu-id="0ba21-111">If you do not have an existing WebView2 project, download the [WebView2API Sample app][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample], a comprehensive sample of the latest WebView2 SDK.</span></span>  <span data-ttu-id="0ba21-112">Assurez-vous que vous avez satisfait aux [conditions préalables pour l’exemple d’application WebView2API.][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]</span><span class="sxs-lookup"><span data-stu-id="0ba21-112">Ensure you have satisfied the [prerequisites for the WebView2API Sample app][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites].</span></span>  

<span data-ttu-id="0ba21-113">Une fois que vous avez cloné le repo, créez le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0ba21-113">Once you have cloned the repo, build the project in Visual Studio.</span></span>  <span data-ttu-id="0ba21-114">Elle doit ressembler à la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="0ba21-114">It should look like the following figure.</span></span>  

:::image type="complex" source="../media/webdriver/sample-app.png" alt-text="Exemple d’application WebView2API" lightbox="../media/webdriver/sample-app.png":::
   <span data-ttu-id="0ba21-116">Exemple d’application WebView2API</span><span class="sxs-lookup"><span data-stu-id="0ba21-116">WebView2API Sample app</span></span>  
:::image-end:::  

## <a name="step-2--install-microsoft-edge-driver"></a><span data-ttu-id="0ba21-117">Étape 2 : Installer le pilote Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0ba21-117">Step 2:  Install Microsoft Edge Driver</span></span>  

<span data-ttu-id="0ba21-118">Suivez les instructions pour installer le pilote [Microsoft Edge][WebdriverChromiumDownloadMicrosoftEdgeDriver] spécifique au navigateur requis par Selenium pour automatiser et tester WebView2.</span><span class="sxs-lookup"><span data-stu-id="0ba21-118">Follow the instructions to install [Microsoft Edge Driver][WebdriverChromiumDownloadMicrosoftEdgeDriver] the browser-specific driver required by Selenium to automate and test WebView2.</span></span>  

<span data-ttu-id="0ba21-119">Assurez-vous que la version du pilote Microsoft Edge correspond à la version de WebView2 Runtime que votre application utilise.</span><span class="sxs-lookup"><span data-stu-id="0ba21-119">Ensure that the version of Microsoft Edge Driver matches the version of WebView2 Runtime that you app uses.</span></span>  <span data-ttu-id="0ba21-120">Pour que l’exemple WebView2API fonctionne, assurez-vous que votre version de WebView2 Runtime est supérieure ou égale à la version prise en charge de la dernière version du SDK WebView2.</span><span class="sxs-lookup"><span data-stu-id="0ba21-120">For the WebView2API Sample to work, make sure that your version of WebView2 Runtime is greater than or equal than the supported version of the latest WebView2 SDK release.</span></span>  <span data-ttu-id="0ba21-121">Pour rechercher la dernière version du SDK WebView2, accédez aux notes de [publication webView2.][Webview2Releasenotes]</span><span class="sxs-lookup"><span data-stu-id="0ba21-121">To locate the latest WebView2 SDK release, navigate to [WebView2 release notes][Webview2Releasenotes].</span></span>  <span data-ttu-id="0ba21-122">Pour connaître la version de WebView2 Runtime dont vous disposez actuellement, accédez à `edge://settings/help` .</span><span class="sxs-lookup"><span data-stu-id="0ba21-122">To find out what version of WebView2 Runtime you currently have, navigate to `edge://settings/help`.</span></span>  

## <a name="step-3--add-selenium-to-the-webview2api-sample"></a><span data-ttu-id="0ba21-123">Étape 3 : Ajouter du selenium à l’exemple WebView2API</span><span class="sxs-lookup"><span data-stu-id="0ba21-123">Step 3:  Add Selenium to the WebView2API Sample</span></span>  

<span data-ttu-id="0ba21-124">À ce stade, WebView2 Runtime doit être installé, créé un projet WebView2 et installé le pilote Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0ba21-124">At this point you should have WebView2 Runtime installed, built a WebView2 project, and installed Microsoft Edge Driver.</span></span>  <span data-ttu-id="0ba21-125">À présent, vous pouvez commencer à utiliser Selenium.</span><span class="sxs-lookup"><span data-stu-id="0ba21-125">Now, get started using Selenium.</span></span>  

> [!NOTE]
> <span data-ttu-id="0ba21-126">Selenium prend en charge C\#, Java, Python, Javascript et Ruby.</span><span class="sxs-lookup"><span data-stu-id="0ba21-126">Selenium supports C\#, Java, Python, Javascript, and Ruby.</span></span>  <span data-ttu-id="0ba21-127">Toutefois, le guide suivant est écrit en C\#.</span><span class="sxs-lookup"><span data-stu-id="0ba21-127">However, the following guide is written using C\#.</span></span>  

1.  <span data-ttu-id="0ba21-128">Commencez par créer un projet **C# .NET Framework** dans **Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="0ba21-128">Start by creating a new **C# .NET Framework** project in **Visual Studio**.</span></span>  <span data-ttu-id="0ba21-129">Sélectionnez **Suivant** dans le coin inférieur droit pour continuer.</span><span class="sxs-lookup"><span data-stu-id="0ba21-129">Choose **Next** on the bottom right-hand corner to continue.</span></span>  
    
    :::image type="complex" source="../media/webdriver/new-project.png" alt-text="Create a new project (Créer un projet)" lightbox="../media/webdriver/new-project.png":::
       <span data-ttu-id="0ba21-131">Create a new project (Créer un projet)</span><span class="sxs-lookup"><span data-stu-id="0ba21-131">Create a new project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0ba21-132">Donnez un nom **à votre projet,** enregistrez-le à votre emplacement **préféré,** puis choisissez **Créer.**</span><span class="sxs-lookup"><span data-stu-id="0ba21-132">Give your project a **name**, save it to your preferred **location**, and choose **Create**.</span></span>  
    
    :::image type="complex" source="../media/webdriver/app-create.png" alt-text="Configurer votre nouveau projet" lightbox="../media/webdriver/app-create.png":::
       <span data-ttu-id="0ba21-134">Configurer votre nouveau projet</span><span class="sxs-lookup"><span data-stu-id="0ba21-134">Configure your new project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0ba21-135">Un nouveau projet est créé.</span><span class="sxs-lookup"><span data-stu-id="0ba21-135">A new project is created.</span></span>  <span data-ttu-id="0ba21-136">Dans ce guide, tout le code est écrit dans le `Program.cs` fichier.</span><span class="sxs-lookup"><span data-stu-id="0ba21-136">In this guide, all code is written to the `Program.cs` file.</span></span>  
    
    :::image type="complex" source="../media/webdriver/start-app.png" alt-text="Nouveau projet" lightbox="../media/webdriver/start-app.png":::
       <span data-ttu-id="0ba21-138">Nouveau projet</span><span class="sxs-lookup"><span data-stu-id="0ba21-138">New project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0ba21-139">Maintenant, **ajoutez Selenium** au projet.</span><span class="sxs-lookup"><span data-stu-id="0ba21-139">Now add **Selenium** to the project.</span></span>  <span data-ttu-id="0ba21-140">Installez Selenium à l’aide **du package NuGet Selenium.WebDriver.**</span><span class="sxs-lookup"><span data-stu-id="0ba21-140">Install Selenium using the **Selenium.WebDriver NuGet package**.</span></span>  
    
    <span data-ttu-id="0ba21-141">Pour télécharger le **package NuGet Selenium.WebDriver,** dans **Visual Studio,** pointez sur **Project**et choisissez Gérer le **package NuGet.**</span><span class="sxs-lookup"><span data-stu-id="0ba21-141">To download the **Selenium.WebDriver NuGet package**, in **Visual Studio**, hover on **Project**, and choose **Manage NuGet Package**.</span></span>  <span data-ttu-id="0ba21-142">L’écran suivant doit apparaître.</span><span class="sxs-lookup"><span data-stu-id="0ba21-142">The following screen should appear.</span></span>  
    
    :::image type="complex" source="../media/webdriver/download-nuget.png" alt-text="Télécharger le package NuGet" lightbox="../media/webdriver/download-nuget.png":::
       <span data-ttu-id="0ba21-144">Télécharger le package NuGet</span><span class="sxs-lookup"><span data-stu-id="0ba21-144">Download NuGet package</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0ba21-145">Entrez dans la barre de recherche, choisissez `Selenium.WebDriver` **Selenium.WebDriver** dans les résultats et assurez-vous de cochez la case en regard de la **pré-version.**</span><span class="sxs-lookup"><span data-stu-id="0ba21-145">Enter `Selenium.WebDriver` in the search bar, choose **Selenium.WebDriver** from the results, and make sure to checkmark the box next to **include pre-release**.</span></span>  <span data-ttu-id="0ba21-146">Dans la fenêtre de droite, assurez-vous que la **version** est définie pour installer **4.0.0-alpha04 ou** version ultérieure et choisissez **Installer**.</span><span class="sxs-lookup"><span data-stu-id="0ba21-146">On the right-hand side window, ensure the **Version** is set to **install 4.0.0-alpha04** or later and choose **Install**.</span></span>  <span data-ttu-id="0ba21-147">NuGet télécharge Selenium sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0ba21-147">NuGet downloads Selenium to your machine.</span></span>  
    
    <span data-ttu-id="0ba21-148">Pour en savoir plus sur le package NuGet Selenium.WebDriver, accédez à [Selenium.WebDriver 4.0.0-alpha04][NugetSeleniumWebdriver400Alpha04].</span><span class="sxs-lookup"><span data-stu-id="0ba21-148">To learn more about the Selenium.WebDriver NuGet package, navigate to [Selenium.WebDriver 4.0.0-alpha04][NugetSeleniumWebdriver400Alpha04].</span></span>  
    
    :::image type="complex" source="../media/webdriver/nuget.png" alt-text="Gérer le package NuGet" lightbox="../media/webdriver/nuget.png":::
       <span data-ttu-id="0ba21-150">Gérer le package NuGet</span><span class="sxs-lookup"><span data-stu-id="0ba21-150">Manage NuGet package</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0ba21-151">À `OpenQA.Selenium.Edge` utiliser en ajoutant l’instruction suivante : au début du  `using OpenQA.Selenium.Edge;` `Program.cs` fichier.</span><span class="sxs-lookup"><span data-stu-id="0ba21-151">Use `OpenQA.Selenium.Edge` by adding the following statement:  `using OpenQA.Selenium.Edge;` at the beginning of `Program.cs` file.</span></span>  
    
    ```csharp
    using OpenQA.Selenium.Edge;
    
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;
    ```  
    
## <a name="step-4-drive-webview2-with-selenium-and-microsoft-edge-driver"></a><span data-ttu-id="0ba21-152">Étape 4 : Lecteur WebView2 avec selenium et pilote Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0ba21-152">Step 4: Drive WebView2 with Selenium and Microsoft Edge Driver</span></span>  

1.  <span data-ttu-id="0ba21-153">Tout d’abord, `EdgeOptions` créez l’objet en copiant l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="0ba21-153">First, create the `EdgeOptions` object, by copying the following code snippet.</span></span>  
    
    ```csharp
    static void Main(string[] args)
    {
        // EdgeOptions() requires using OpenQA.Selenium.Edge
        // Construct EdgeOptions with is_legacy = false and the string "webview2"
        EdgeOptions edgeOptions = new EdgeOptions(false, "webview2");
    ```  
    
    <span data-ttu-id="0ba21-154">`EdgeOptions`L’objet prend les deux paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="0ba21-154">The `EdgeOptions` object takes in the following two parameters.</span></span>  
    
    | <span data-ttu-id="0ba21-155">Paramètre</span><span class="sxs-lookup"><span data-stu-id="0ba21-155">Parameter</span></span> | <span data-ttu-id="0ba21-156">Détails</span><span class="sxs-lookup"><span data-stu-id="0ba21-156">Details</span></span> |    
    |:--- |:--- |  
    | `is_legacy` | <span data-ttu-id="0ba21-157">Définissez sur , qui indique à Selenium que vous êtes au volant du nouveau navigateur Microsoft Edge basé sur `false` Chromium.</span><span class="sxs-lookup"><span data-stu-id="0ba21-157">Set to `false`, which tells Selenium that you are driving the new Chromium-based Microsoft Edge browser.</span></span> |  
    | `"webview2"` | <span data-ttu-id="0ba21-158">Chaîne qui indique à Selenium que vous êtes au volant de WebView2.</span><span class="sxs-lookup"><span data-stu-id="0ba21-158">A string that tells Selenium you are driving WebView2.</span></span> |  
    
1.  <span data-ttu-id="0ba21-159">Ensuite, définissez le chemin d’accès au fichier de votre runtime de projet WebView2, créez une chaîne nommée qui fournit le chemin d’accès du fichier à l’endroit où vous avez installé le pilote Microsoft Edge et créez une chaîne nommée pour stocker le nom du runtime du pilote `edgeOptions.BinaryLocation` `msedgedriverDir` Microsoft [][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads] `msedgedriverExe` Edge.</span><span class="sxs-lookup"><span data-stu-id="0ba21-159">Next, set `edgeOptions.BinaryLocation` to the file path of your WebView2 project runtime, create a string named `msedgedriverDir` that provides the file path to where you installed [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads], and create a string named `msedgedriverExe` to store the name of the Microsoft Edge Driver runtime.</span></span>  <span data-ttu-id="0ba21-160">Par défaut, le runtime est nommé `msedgedriver.exe` .</span><span class="sxs-lookup"><span data-stu-id="0ba21-160">By default, the runtime is named `msedgedriver.exe`.</span></span> <span data-ttu-id="0ba21-161">Utilisez ces deux chaînes pour construire `EdgeDriverService` l’objet comme illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="0ba21-161">Use these two strings to construct the `EdgeDriverService` object as shown below.</span></span>  <span data-ttu-id="0ba21-162">Enfin, créez `EdgeDriver` l’objet à `EdgeDriverService` l’aide et `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="0ba21-162">Finally, create the `EdgeDriver` object using `EdgeDriverService` and `EdgeOptions`.</span></span>  
    
    <span data-ttu-id="0ba21-163">Vous pouvez copier et coller le code suivant sous `edgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="0ba21-163">You may copy and paste the following code underneath `edgeOptions`.</span></span>  <span data-ttu-id="0ba21-164">Veillez à spécifier les chemins d’accès aux fichiers corrects pour le runtime de votre projet et le runtime du pilote Microsoft Edge sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0ba21-164">Ensure you specify the correct file paths to your project runtime and the Microsoft Edge Driver runtime on your machine.</span></span>  
    
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
    
3.  <span data-ttu-id="0ba21-165">À présent, `EdgeDriver` est configuré pour piloter WebView2 dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="0ba21-165">Now, `EdgeDriver` is configured to drive the WebView2 in your project.</span></span>  <span data-ttu-id="0ba21-166">Par exemple, si vous utilisez l’exemple **WebView2API,** vous pouvez accéder `https://microsoft.com` en exécutant la `e.Url = @"https://www.microsoft.com";` commande.</span><span class="sxs-lookup"><span data-stu-id="0ba21-166">For example, if you are using the **WebView2API Sample**, you may navigate to `https://microsoft.com` by running the `e.Url = @"https://www.microsoft.com";` command.</span></span>  <span data-ttu-id="0ba21-167">Vérifiez le lecteur Selenium WebView2 en fixant un point d’arrêt sur la ligne et en exécutant le projet.</span><span class="sxs-lookup"><span data-stu-id="0ba21-167">Verify the Selenium drive WebView2 by setting a breakpoint on the line and running the project.</span></span>  
    
    ```csharp
        //The following navigates the WebView2API Sample from bing.com to microsoft.com
        e.Url = @"https://www.microsoft.com";
        
        //This exits the edge driver
        e.Quit();
    }
    ```  
    
    :::image type="complex" source="../media/webdriver/microsoft.png" alt-text="Selenium exécutant WebView2" lightbox="../media/webdriver/microsoft.png":::
       <span data-ttu-id="0ba21-169">Selenium exécutant WebView2</span><span class="sxs-lookup"><span data-stu-id="0ba21-169">Selenium running WebView2</span></span>  
    :::image-end:::

<span data-ttu-id="0ba21-170">Félicitations.</span><span class="sxs-lookup"><span data-stu-id="0ba21-170">Congratulations.</span></span>  <span data-ttu-id="0ba21-171">Vous avez correctement automatisé un projet WebView2 et piloté WebView2 à l’aide de Selenium et du pilote Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0ba21-171">You have successfully automated a WebView2 project and driven WebView2 using Selenium and Microsoft Edge Driver.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0ba21-172">Voir également</span><span class="sxs-lookup"><span data-stu-id="0ba21-172">See also</span></span>  

*   <span data-ttu-id="0ba21-173">Pour une vue d’ensemble de la façon dont les API Selenium pilotent WebView2 ou Microsoft Edge \(Chromium\), accédez à [WebDriver sur la documentation Selenium][SeleniumWebdriver]</span><span class="sxs-lookup"><span data-stu-id="0ba21-173">For a comprehensive look at how the APIs Selenium drives WebView2 or Microsoft Edge \(Chromium\), navigate to [WebDriver on Selenium documentation][SeleniumWebdriver]</span></span>   
*   <span data-ttu-id="0ba21-174">Pour en savoir plus sur le contrôle WebView2 et comment l’utiliser lors de l’incorporation de contenu web dans votre application native, accédez à [Introduction à Microsoft Edge WebView2][WebViewIndex].</span><span class="sxs-lookup"><span data-stu-id="0ba21-174">To learn more about WebView2 control and how to use it when embedding web content in your native app, navigate to [Introduction to Microsoft Edge WebView2][WebViewIndex].</span></span>  
*   <span data-ttu-id="0ba21-175">Pour en savoir plus sur l’automatisation de Microsoft Edge \(Chromium\), accédez à [Utiliser WebDriver (Chromium)][WebdriverChromium] pour tester l’automatisation</span><span class="sxs-lookup"><span data-stu-id="0ba21-175">To learn more about automating Microsoft Edge \(Chromium\), navigate to [Use WebDriver (Chromium) for test automation][WebdriverChromium]</span></span>   
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="0ba21-176">Entrer en contact avec l’équipe Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="0ba21-176">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WebdriverChromium]: ../../webdriver-chromium/index.md "Utiliser WebDriver (Chromium) pour tester l’automatisation | Documents Microsoft"  
[WebdriverChromiumDownloadMicrosoftEdgeDriver]: ../../webdriver-chromium/index.md#download-microsoft-edge-driver "Télécharger le pilote Microsoft Edge : utiliser WebDriver (Chromium) pour tester l’automatisation | Documents Microsoft"  
[WebViewIndex]: ../index.md "Présentation de Microsoft Edge WebView2 - Documents Microsoft"  
[Webview2Releasenotes]: ../releasenotes.md "Notes de publication du SDK WebView2 | Documents Microsoft"  

[MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Télécharger la | WebDriver Développeur Microsoft Edge"  

[GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Exemple d’API WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample#prerequisites "Conditions préalables : exemple d’API WebView2 | GitHub"  

[NugetSeleniumWebdriver400Alpha04]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha04 "Selenium.WebDriver 4.0.0-alpha04 | Galerie NuGet"  

[SeleniumWebdriver]: https://www.selenium.dev/documentation/en/webdriver "WebDriver | Selenium"  

[W3cWebdriver2]: https://www.w3.org/TR/webdriver2 "WebDriver | W3C"  
