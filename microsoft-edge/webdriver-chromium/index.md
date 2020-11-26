---
description: Découvrez comment tester votre site Web ou votre application dans Microsoft Edge ou automatiser le navigateur à l’aide du Web.
title: WebDriver (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, développement Web, html, CSS, JavaScript, développeur, Web Driver, sélénium, test, outils, Automation, test
ms.openlocfilehash: 3c197a83dbf16c68102ff6e9a4ee6f33b0573af2
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "11192247"
---
# <span data-ttu-id="59647-104">Utiliser le WebDriver (chrome) pour l’automatisation des tests</span><span class="sxs-lookup"><span data-stu-id="59647-104">Use WebDriver (Chromium) for test automation</span></span>  

<span data-ttu-id="59647-105">Le WebDriver vous permet d’effectuer des tests automatisés pour simuler l’interaction de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="59647-105">WebDriver enables you \(developers\) to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="59647-106">Les tests et simulations du lecteur WebPart diffèrent des tests unitaires JavaScript pour les raisons suivantes:</span><span class="sxs-lookup"><span data-stu-id="59647-106">WebDriver tests and simulations differ from JavaScript unit tests because of the following reasons.</span></span>  

*   <span data-ttu-id="59647-107">Accès aux fonctionnalités et informations non disponibles pour JavaScript exécuté dans les navigateurs.</span><span class="sxs-lookup"><span data-stu-id="59647-107">Accesses functionality and information not available to JavaScript running in browsers.</span></span>  
*   <span data-ttu-id="59647-108">Simule des événements utilisateur ou des événements de niveau système d’exploitation plus précisément.</span><span class="sxs-lookup"><span data-stu-id="59647-108">Simulates user events or OS-level events more accurately.</span></span>  
*   <span data-ttu-id="59647-109">Gestion de plusieurs fenêtres, onglets et pages Web dans une seule et même session de test.</span><span class="sxs-lookup"><span data-stu-id="59647-109">Manages multiple windows, tabs, and webpages in a single test session.</span></span>  
*   <span data-ttu-id="59647-110">Exécute plusieurs sessions de Microsoft Edge sur un ordinateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="59647-110">Runs multiple sessions of Microsoft Edge on a specific machine.</span></span>  
    
<span data-ttu-id="59647-111">La section suivante décrit comment prendre en main le WebDriver pour Microsoft Edge \ (chrome \).</span><span class="sxs-lookup"><span data-stu-id="59647-111">The following section describes how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  

## <span data-ttu-id="59647-112">Installer Microsoft Edge (chrome)</span><span class="sxs-lookup"><span data-stu-id="59647-112">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="59647-113">Vérifiez que vous avez installé [Microsoft Edge (chrome)][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="59647-113">Ensure you install [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="59647-114">Pour confirmer l’installation de Microsoft Edge \ (chrome \), accédez à `edge://settings/help` , puis vérifiez que le numéro de version est la version 75 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="59647-114">To confirm that you have Microsoft Edge \(Chromium\) installed, navigate to `edge://settings/help`, and verify the version number is Version 75 or later.</span></span>  

## <span data-ttu-id="59647-115">Télécharger le pilote Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="59647-115">Download Microsoft Edge Driver</span></span>  

<span data-ttu-id="59647-116">Pour commencer à automatiser les tests, procédez comme suit pour vous assurer que la version du WebDriver que vous installez correspond à la version de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="59647-116">To begin automating tests, use the following steps to ensure that the WebDriver version you install matches your browser version.</span></span>  

1.  <span data-ttu-id="59647-117">Accédez à `edge://settings/help` la version de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="59647-117">Navigate to `edge://settings/help` to get the version of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/webdriver-chromium/edge-version.png" alt-text="Numéro de build de l’Canaries Microsoft Edge le 14 janvier 2020" lightbox="../media/webdriver-chromium/edge-version.png":::
       <span data-ttu-id="59647-119">Numéro de build de l’Canaries Microsoft Edge le 14 janvier 2020</span><span class="sxs-lookup"><span data-stu-id="59647-119">The build number for Microsoft Edge Canary on January 14, 2020</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="59647-120">Accédez à la page de [téléchargements de pilotes Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads] et téléchargez le pilote correspondant au numéro de version de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="59647-120">Navigate to the [Microsoft Edge Driver downloads][MicrosoftDeveloperEdgeToolsWebdriverDownloads] page and download the driver that matches the version number of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/webdriver-chromium/edge-driver-install.png" alt-text="Section téléchargements de la page du pilote Microsoft Edge" lightbox="../media/webdriver-chromium/edge-driver-install.png":::
       <span data-ttu-id="59647-122">Section téléchargements de la page du [pilote Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="59647-122">The Downloads section of the [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] page</span></span>  
    :::image-end:::  
    
    > [!NOTE] 
    > <span data-ttu-id="59647-123">Pour plus d’informations sur l’automatisation des tests à l’aide de Microsoft Edge \ (EdgeHTML \), voir [Microsoft WebDriver pour Microsoft Edge (EdgeHTML)][Webdriver].</span><span class="sxs-lookup"><span data-stu-id="59647-123">For more information about test automation using Microsoft Edge \(EdgeHTML\), see [Microsoft WebDriver for Microsoft Edge (EdgeHTML)][Webdriver].</span></span>  
    
## <span data-ttu-id="59647-124">Choisir une liaison de langue du WebDriver</span><span class="sxs-lookup"><span data-stu-id="59647-124">Choose a WebDriver language binding</span></span>  

<span data-ttu-id="59647-125">Le dernier composant que vous devez télécharger est un pilote client propre à la langue, qui permet de traduire votre code \ (Python, Java, C \ #, Rubi, JavaScript \) en commandes exécutées par le pilote Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="59647-125">The last component you must download is a language-specific client driver to translate your code \(Python, Java, C\#, Ruby, JavaScript\) into commands the Microsoft Edge Driver runs in Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="59647-126">[Téléchargez la liaison de langue de votre choix][SeleniumDownloads].</span><span class="sxs-lookup"><span data-stu-id="59647-126">[Download the WebDriver language binding of your choice][SeleniumDownloads].</span></span>  <span data-ttu-id="59647-127">L’équipe Microsoft Edge recommande le [sélénium 4,00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] ou version ultérieure, car il prend en charge Microsoft Edge \ (chrome \).</span><span class="sxs-lookup"><span data-stu-id="59647-127">The Microsoft Edge team recommends [Selenium 4.00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] or later, because it supports Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="59647-128">Toutefois, vous pouvez contrôler Microsoft Edge \ (chrome \) dans toutes les versions plus anciennes de sélénium, y compris la version actuelle de l’sélénium 3D stable.</span><span class="sxs-lookup"><span data-stu-id="59647-128">However, you may control Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="59647-129">Si vous avez précédemment automatisé ou testé Microsoft Edge \ (chrome \) à l’aide de l’application `ChromeDriver` et des `ChromeOptions` classes, votre code WebDriver n’est pas exécuté sur la version 80 de Microsoft Edge ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="59647-129">If you were previously automating or testing Microsoft Edge \(Chromium\) using `ChromeDriver` and `ChromeOptions` classes, your WebDriver code does not run on Microsoft Edge Version 80 or later.</span></span>  <span data-ttu-id="59647-130">Pour résoudre ce problème, mettez à jour vos tests pour utiliser la `EdgeOptions` classe et installer le [pilote Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver].</span><span class="sxs-lookup"><span data-stu-id="59647-130">To solve this problem, update your tests to use the `EdgeOptions` class and install [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver].</span></span>  

### <span data-ttu-id="59647-131">Utiliser le sélénium 3</span><span class="sxs-lookup"><span data-stu-id="59647-131">Use Selenium 3</span></span>  

<span data-ttu-id="59647-132">Si vous utilisez déjà [sélénium 3][|::ref1::|], il est possible que vous ayez des tests de navigateur existants et que vous vouliez ajouter une couverture pour Microsoft Edge \ (chrome \) sans changer votre version de sélénium.</span><span class="sxs-lookup"><span data-stu-id="59647-132">If you already use [Selenium 3][|::ref1::|], you may have existing browser tests and want to add coverage for Microsoft Edge \(Chromium\) without changing your version of Selenium.</span></span>  <span data-ttu-id="59647-133">Pour utiliser le [sélénium 3][|::ref2::|] pour écrire des tests automatisés pour Microsoft Edge \ (EdgeHTML \) et Microsoft Edge \ (chrome \), installez les [outils de sélénium pour le package Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] pour utiliser le pilote mis à jour.</span><span class="sxs-lookup"><span data-stu-id="59647-133">To use [Selenium 3][|::ref2::|] to write automated tests for both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package to use the updated driver.</span></span>  <span data-ttu-id="59647-134">Les `EdgeDriver` `EdgeDriverService` classes et incluses dans les outils sont entièrement compatibles avec les équivalents intégrés d’sélénium 4.</span><span class="sxs-lookup"><span data-stu-id="59647-134">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium 4.</span></span>  

<span data-ttu-id="59647-135">Procédez comme suit pour ajouter les [outils de sélénium pour Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] et [sélénium 3][|::ref3::|] à votre projet.</span><span class="sxs-lookup"><span data-stu-id="59647-135">Use the following steps to add the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] and [Selenium 3][|::ref3::|] to your project.</span></span>

#### [<span data-ttu-id="59647-136">C#</span><span class="sxs-lookup"><span data-stu-id="59647-136">C#</span></span>](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="59647-137">Ajoutez les packages [Microsoft. Edge. SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] et [sélénium. WebDriver][NugetPackagesSeleniumWebdriver31410] à votre projet .net à l’aide de l' [interface CLI][NugetCLI] ou [Visual Studio][VisualStudio]NuGet.</span><span class="sxs-lookup"><span data-stu-id="59647-137">Add the [Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] and [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] packages to your .NET project using the [NuGet CLI][NugetCLI] or [Visual Studio][VisualStudio].</span></span>  

#### [<span data-ttu-id="59647-138">Software</span><span class="sxs-lookup"><span data-stu-id="59647-138">Python</span></span>](#tab/python/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="59647-139">Utilisez [PIP][PythonPip] pour installer le [msedge-sélénium-Tools][PythonSeleniumTools] et les packages de [sélénium][PythonSelenium] .</span><span class="sxs-lookup"><span data-stu-id="59647-139">Use [pip][PythonPip] to install the [msedge-selenium-tools][PythonSeleniumTools] and [selenium][PythonSelenium] packages.</span></span>  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [<span data-ttu-id="59647-140">JavaScript</span><span class="sxs-lookup"><span data-stu-id="59647-140">JavaScript</span></span>](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="59647-141">Utilisez [NPM][JavaScript|::ref4::|] pour installer [Edge-sélénium-Tools][JavaScriptSeleniumTools] et les packages [sélénium-Web Driver][JavaScriptSelenium] .</span><span class="sxs-lookup"><span data-stu-id="59647-141">Use [npm][JavaScript|::ref4::|] to install the [edge-selenium-tools][JavaScriptSeleniumTools] and [selenium-webdriver][JavaScriptSelenium] packages.</span></span>  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## <span data-ttu-id="59647-142">Utiliser Microsoft Edge (chrome) avec WebDriver</span><span class="sxs-lookup"><span data-stu-id="59647-142">Use Microsoft Edge (Chromium) with WebDriver</span></span>

<span data-ttu-id="59647-143">Vous pouvez exécuter les exemples suivants à l’aide de sélénium 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="59647-143">You may run the following examples using either Selenium 3 or 4.</span></span>  <span data-ttu-id="59647-144">Pour une utilisation avec le sélénium 3, les [outils de sélénium pour le package Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] doivent être installés.</span><span class="sxs-lookup"><span data-stu-id="59647-144">To use with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package must be installed.</span></span>  

### <span data-ttu-id="59647-145">Utilisation de base</span><span class="sxs-lookup"><span data-stu-id="59647-145">Basic Usage</span></span>  

<span data-ttu-id="59647-146">Pour utiliser avec Microsoft Edge \ (EdgeHTML \), créez une instance par défaut de la `EdgeDriver` classe.</span><span class="sxs-lookup"><span data-stu-id="59647-146">To use with Microsoft Edge \(EdgeHTML\), create a default instance of the `EdgeDriver` class.</span></span>  

#### [<span data-ttu-id="59647-147">C#</span><span class="sxs-lookup"><span data-stu-id="59647-147">C#</span></span>](#tab/c-sharp/)  

<a id="basic-usage-code"></a>  

```csharp
var driver = new EdgeDriver();
```  

#### [<span data-ttu-id="59647-148">Software</span><span class="sxs-lookup"><span data-stu-id="59647-148">Python</span></span>](#tab/python/)  

<a id="basic-usage-code"></a>  

```python
driver = Edge()
```  

#### [<span data-ttu-id="59647-149">JavaScript</span><span class="sxs-lookup"><span data-stu-id="59647-149">JavaScript</span></span>](#tab/javascript/)  

<a id="basic-usage-code"></a>  

```javascript
let driver = edge.Driver.createSession();
```  

* * *  

### <span data-ttu-id="59647-150">Pilotage de Microsoft Edge (chrome)</span><span class="sxs-lookup"><span data-stu-id="59647-150">Driving Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="59647-151">Pour utiliser avec Microsoft Edge \ (chrome \), créez une nouvelle `EdgeDriver` classe et transmettez-lui l' `EdgeOptions` objet avec la `UseChromium` propriété définie sur `true` .</span><span class="sxs-lookup"><span data-stu-id="59647-151">To use with Microsoft Edge \(Chromium\), create a new `EdgeDriver` class and pass it the `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<span data-ttu-id="59647-152">C#</span><span class="sxs-lookup"><span data-stu-id="59647-152">C#</span></span>](#tab/c-sharp/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="59647-153">Software</span><span class="sxs-lookup"><span data-stu-id="59647-153">Python</span></span>](#tab/python/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### [<span data-ttu-id="59647-154">JavaScript</span><span class="sxs-lookup"><span data-stu-id="59647-154">JavaScript</span></span>](#tab/javascript/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> <span data-ttu-id="59647-155">Si votre administrateur informatique a défini la stratégie [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] sur `2` , le [pilote Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] ne peut pas conduire [Microsoft Edge (chrome)][MicrosoftEdge] , car le pilote utilise [Microsoft Edge devtools][DevToolsMain].</span><span class="sxs-lookup"><span data-stu-id="59647-155">If your IT admin has set the [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] policy to `2`, [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] is not be able to drive [Microsoft Edge (Chromium)][MicrosoftEdge] because the driver uses the [Microsoft Edge DevTools][DevToolsMain].</span></span>  <span data-ttu-id="59647-156">Assurez-vous que la stratégie [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] est définie sur `0` ou `1` pour automatiser [Microsoft Edge (chrome)][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="59647-156">Ensure the [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] policy is set to `0` or `1` to automate [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  

### <span data-ttu-id="59647-157">Choix de fichiers binaires de navigateur spécifiques (chrome uniquement)</span><span class="sxs-lookup"><span data-stu-id="59647-157">Choosing Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="59647-158">Vous pouvez utiliser la `EdgeOptions` classe avec des fichiers binaires de Microsoft Edge \ (chrome \) spécifiques.</span><span class="sxs-lookup"><span data-stu-id="59647-158">You may use the `EdgeOptions` class with specific binaries of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="59647-159">Par exemple, vous pouvez exécuter des tests en utilisant les [canaux Microsoft Edge Preview][MicrosoftedgeinsiderDownload] tels que Microsoft Edge Beta.</span><span class="sxs-lookup"><span data-stu-id="59647-159">For example, you may run tests using the [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<span data-ttu-id="59647-160">C#</span><span class="sxs-lookup"><span data-stu-id="59647-160">C#</span></span>](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="59647-161">Software</span><span class="sxs-lookup"><span data-stu-id="59647-161">Python</span></span>](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [<span data-ttu-id="59647-162">JavaScript</span><span class="sxs-lookup"><span data-stu-id="59647-162">JavaScript</span></span>](#tab/javascript/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <span data-ttu-id="59647-163">Personnalisation du service de pilote Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="59647-163">Customizing the Microsoft Edge Driver Service</span></span>  

#### [<span data-ttu-id="59647-164">C#</span><span class="sxs-lookup"><span data-stu-id="59647-164">C#</span></span>](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="59647-165">Quand une `EdgeDriver` instance de classe est créée à l’aide d’une `EdgeOptions` classe, elle crée et lance la `EdgeDriverService` classe appropriée pour Microsoft Edge \ (EdgeHTML \) ou Microsoft Edge \ (chrome \).</span><span class="sxs-lookup"><span data-stu-id="59647-165">When an `EdgeDriver` class instance is created using `EdgeOptions` class, it creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="59647-166">Si vous souhaitez créer un, créez-en un à l' `EdgeDriverService` aide de la `CreateChromiumService()` méthode.</span><span class="sxs-lookup"><span data-stu-id="59647-166">If you want to create an `EdgeDriverService`, create one configured for Microsoft Edge \(Chromium\) using the `CreateChromiumService()` method.</span></span>  <span data-ttu-id="59647-167">Il peut s’avérer utile pour des personnalisations supplémentaires telles que l’activation de la sortie détaillée du journal dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="59647-167">You may find it useful for additional customizations like enabling verbose log output in the following code.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
><span data-ttu-id="59647-168">Vous n’avez pas besoin de fournir l' `EdgeOptions` objet lors `EdgeDriverService` du passage à l' `EdgeDriver` instance.</span><span class="sxs-lookup"><span data-stu-id="59647-168">You do not need to provide the `EdgeOptions` object when passing `EdgeDriverService` to the `EdgeDriver` instance.</span></span> <span data-ttu-id="59647-169">La `EdgeDriver` classe utilise les options par défaut pour Microsoft Edge \ (EdgeHTML \) ou Microsoft Edge \ (chrome \), en fonction du service que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="59647-169">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) depending on the service you provide.</span></span>  
> <span data-ttu-id="59647-170">Toutefois, si vous souhaitez fournir les deux `EdgeDriverService` `EdgeOptions` classes et, assurez-vous que les deux sont configurées pour la même version de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="59647-170">However, if you want to provide both `EdgeDriverService` and `EdgeOptions` classes, ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="59647-171">Par exemple, il n’est pas possible d’utiliser une classe Microsoft Edge \ (EdgeHTML \) par défaut `EdgeDriverService` dans la `EdgeOptions` classe.</span><span class="sxs-lookup"><span data-stu-id="59647-171">For example, it is not possible to use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="59647-172">La `EdgeDriver` classe lève une erreur pour empêcher l’utilisation de différentes versions.</span><span class="sxs-lookup"><span data-stu-id="59647-172">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<span data-ttu-id="59647-173">Software</span><span class="sxs-lookup"><span data-stu-id="59647-173">Python</span></span>](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="59647-174">Lorsque vous utilisez Python, l' `Edge` objet crée et gère l’objet `EdgeService` .</span><span class="sxs-lookup"><span data-stu-id="59647-174">When using Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="59647-175">Pour configurer le `EdgeService` , passez des arguments supplémentaires à l' `Edge` objet, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="59647-175">To configure the `EdgeService`, pass additional arguments to the `Edge` object as indicated in the following code.</span></span>  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<span data-ttu-id="59647-176">JavaScript</span><span class="sxs-lookup"><span data-stu-id="59647-176">JavaScript</span></span>](#tab/javascript/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="59647-177">Lorsque vous utilisez JavaScript, créez et configurez a `Service` avec la `ServiceBuilder` classe.</span><span class="sxs-lookup"><span data-stu-id="59647-177">When using JavaScript, create and configure a `Service` with the `ServiceBuilder` class.</span></span>  <span data-ttu-id="59647-178">Si vous le souhaitez, vous pouvez transmettre l' `Service` objet à l' `Driver` objet, en commençant par le service.</span><span class="sxs-lookup"><span data-stu-id="59647-178">Optionally, you may pass the `Service` object to the `Driver` object, which starts \(and stops\) the service for you.</span></span>  
<span data-ttu-id="59647-179">Pour configurer le `Service` , exécutez des méthodes supplémentaires dans la `ServiceBuilder` classe avant d’utiliser la `build()` méthode.</span><span class="sxs-lookup"><span data-stu-id="59647-179">To configure the `Service`, run additional methods in the `ServiceBuilder` class before using the `build()` method.</span></span>  <span data-ttu-id="59647-180">Ensuite, transmettez la `service` en tant que paramètre à la `Driver.createSession()` méthode.</span><span class="sxs-lookup"><span data-stu-id="59647-180">Then pass the `service` as a parameter in the `Driver.createSession()` method.</span></span>  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### <span data-ttu-id="59647-181">Utiliser les options de Chromium-Specific</span><span class="sxs-lookup"><span data-stu-id="59647-181">Use Chromium-Specific Options</span></span>  

<span data-ttu-id="59647-182">Si vous définissez la `UseChromium` propriété sur `true` , vous pouvez utiliser la `EdgeOptions` classe pour accéder aux mêmes [Propriétés et méthodes propres au chrome][SeleniumWebDriverChromeoptionsClass] que lorsque vous automatisez d’autres navigateurs de chrome.</span><span class="sxs-lookup"><span data-stu-id="59647-182">If you set the `UseChromium` property to `true`, you may use the `EdgeOptions` class to access the same [Chromium-specific properties and methods][SeleniumWebDriverChromeoptionsClass] as when you automate other Chromium browsers.</span></span>  

#### [<span data-ttu-id="59647-183">C#</span><span class="sxs-lookup"><span data-stu-id="59647-183">C#</span></span>](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<span data-ttu-id="59647-184">Software</span><span class="sxs-lookup"><span data-stu-id="59647-184">Python</span></span>](#tab/python/)  

<a id="using-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<span data-ttu-id="59647-185">JavaScript</span><span class="sxs-lookup"><span data-stu-id="59647-185">JavaScript</span></span>](#tab/javascript/)  

<a id="using-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```

* * *  

> [!NOTE]
> <span data-ttu-id="59647-186">Si la `UseChromium` propriété est définie sur `true` , vous ne pouvez pas utiliser les propriétés et les méthodes pour Microsoft Edge \ (EdgeHTML \).</span><span class="sxs-lookup"><span data-stu-id="59647-186">If the `UseChromium` property is set to `true`, you are not able to use properties and methods for Microsoft Edge \(EdgeHTML\).</span></span>  

## <span data-ttu-id="59647-187">Autres options d’installation d’un Web Driver</span><span class="sxs-lookup"><span data-stu-id="59647-187">Additional WebDriver installation options</span></span>  

### <span data-ttu-id="59647-188">Chocolat</span><span class="sxs-lookup"><span data-stu-id="59647-188">Chocolatey</span></span>  

<span data-ttu-id="59647-189">Si vous utilisez le programme [chocolaté][Chocolatey] en tant que gestionnaire de package, installez le pilote Microsoft Edge en exécutant la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="59647-189">If you use [Chocolatey][Chocolatey] as your package manager, install the Microsoft Edge Driver by running the following command.</span></span>  

```console
choco install selenium-chromium-edge-driver
```  

<span data-ttu-id="59647-190">Pour plus d’informations, voir [pilote de contour de chrome de sélénium au chocolat][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span><span class="sxs-lookup"><span data-stu-id="59647-190">For more information, see [Selenium Chromium Edge Driver on Chocolatey][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span></span>  

### <span data-ttu-id="59647-191">Docker</span><span class="sxs-lookup"><span data-stu-id="59647-191">Docker</span></span>  

<span data-ttu-id="59647-192">Si vous utilisez l' [ancrage][DockerHub], téléchargez une image préconfigurée avec Microsoft Edge \ (chrome \) et le [pilote Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] préinstallé en exécutant la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="59647-192">If you use [Docker][DockerHub], download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] pre-installed by running the following command.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="59647-193">Pour plus d’informations, consultez [conteneur sur le hub de l’ancrage][DockerHubMsedgedriver].</span><span class="sxs-lookup"><span data-stu-id="59647-193">For more information, see [container on Docker Hub][DockerHubMsedgedriver].</span></span>  

## <span data-ttu-id="59647-194">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="59647-194">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="59647-195">L’équipe Microsoft Edge a hâte d’entendre vos commentaires concernant l’utilisation de WebDriver, de sélénium et de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="59647-195">The Microsoft Edge team is eager to hear your feedback about using WebDriver, Selenium, and Microsoft Edge.</span></span>  <span data-ttu-id="59647-196">Pour indiquer à l’équipe votre avis, sélectionnez l’icône **Envoyer des commentaires** dans Microsoft Edge devtools ou envoyez un tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="59647-196">To let the team know what you think, choose the **Send Feedback** icon in the Microsoft Edge DevTools or send a tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Icône Envoyer des commentaires dans Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="59647-198">Icône **Envoyer des commentaires** dans Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="59647-198">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- links -->  

[DevToolsMain]: ../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"
[Webdriver]: ../webdriver.md "Web Driver (EdgeHTML) | Documents Microsoft"  

[DeployedgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability-Microsoft Edge-politiques | Documents Microsoft"  

[Chocolatey]: https://chocolatey.org "Chocolat Programme en chocolat"  
[ChocolateyPackagesSeleniumChromiumEdgeDriver]: https://chocolatey.org/packages/selenium-chromium-edge-driver "Pilote du périphérique de chrome de sélénium Chocolat"  

[DockerHub]: https://hub.docker.com "Hub de l’ancrage"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Hub de l’ancrage"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "Microsoft/Edge-sélénium-Tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SeleniumHQ/sélénium | GitHub"  

[JavaScriptnpm]: https://www.npmjs.com/ "NPM"  
[JavaScriptSeleniumTools]: https://www.npmjs.com/package/@microsoft/edge-selenium-tools "@microsoft/Edge-Selenium-Tools | NPM"  
[JavaScriptSelenium]: https://www.npmjs.com/package/selenium-webdriver "sélénium-Web Driver | NPM"  

[MicrosoftDeveloperEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "Web Driver | Développeur Microsoft"  
[MicrosoftDeveloperEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads "Téléchargements-WebDriver | Développeur Microsoft"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Télécharger le nouveau navigateur Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  

[NugetCLI]:https://www.nuget.org/packages/NuGet.CommandLine/ "NuGet. CommandLine | Galerie NuGet"  
[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft. Edge. SeleniumTools | Galerie NuGet"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Sélénium. WebDriver 3.141.0 | Galerie NuGet"  
[NugetPackagesSeleniumWebdriver400alpha05]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha05 "Sélénium. WebDriver 4.0.0-alpha05 | Galerie NuGet"  

[PythonPip]: https://pypi.org/project/pip/ "PIP | PyPI"  
[PythonSeleniumTools]: https://pypi.org/project/msedge-selenium-tools/ "msedge-sélénium-Tools | PyPI"  
[PythonSelenium]: https://pypi.org/project/selenium/ "sélénium | PyPI"

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDownloads]: https://selenium.dev/downloads "Téléchargements | Sélénium"  
[SeleniumWebDriverChromeoptionsClass]: https://www.selenium.dev/selenium/docs/api/dotnet/?topic=html/T_OpenQA_Selenium_Chrome_ChromeOptions.htm "Classe ChromeOptions-WebDriver | Sélénium"  

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publiez un tweet"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "Web Driver | W3C"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Navigateur headless | Wikipédia"  
