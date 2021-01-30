---
description: Découvrez comment tester votre site web ou votre application dans Microsoft Edge ou automatiser le navigateur avec WebDriver.
title: Utiliser WebDriver (Chromium) pour tester l’automatisation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, développement web, html, css, javascript, développeur, webdriver, selenium, test, outils, automatisation, test
ms.openlocfilehash: 295985734d93c5912922be22c0af0c0e33e00a54
ms.sourcegitcommit: 070a60f634908eea0e29e260331f9fc0aa85ee78
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2021
ms.locfileid: "11306247"
---
# <span data-ttu-id="14f6a-104">Utiliser WebDriver (Chromium) pour tester l’automatisation</span><span class="sxs-lookup"><span data-stu-id="14f6a-104">Use WebDriver (Chromium) for test automation</span></span>  

<span data-ttu-id="14f6a-105">WebDriver permet aux développeurs de créer des tests automatisés qui simulent l’interaction utilisateur.</span><span class="sxs-lookup"><span data-stu-id="14f6a-105">WebDriver allows developers to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="14f6a-106">Les tests et simulations WebDriver diffèrent des tests unitaires JavaScript, car WebDriver :</span><span class="sxs-lookup"><span data-stu-id="14f6a-106">WebDriver tests and simulations differ from JavaScript unit tests because WebDriver:</span></span>  

*   <span data-ttu-id="14f6a-107">Accède aux fonctionnalités et informations non disponibles pour JavaScript s’exécutant dans les navigateurs.</span><span class="sxs-lookup"><span data-stu-id="14f6a-107">Accesses functionality and information not available to JavaScript running in browsers.</span></span>  
*   <span data-ttu-id="14f6a-108">Simule les événements utilisateur ou au niveau du système d’exploitation plus précisément.</span><span class="sxs-lookup"><span data-stu-id="14f6a-108">Simulates user events or OS-level events more accurately.</span></span>  
*   <span data-ttu-id="14f6a-109">Gère plusieurs fenêtres, onglets et pages web en une seule session de test.</span><span class="sxs-lookup"><span data-stu-id="14f6a-109">Manages multiple windows, tabs, and webpages in a single test session.</span></span>  
*   <span data-ttu-id="14f6a-110">Exécute plusieurs sessions de Microsoft Edge sur un ordinateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="14f6a-110">Runs multiple sessions of Microsoft Edge on a specific machine.</span></span>  
    
<span data-ttu-id="14f6a-111">La section suivante décrit comment commencer avec WebDriver pour Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="14f6a-111">The following section describes how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  

## <span data-ttu-id="14f6a-112">Installer Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="14f6a-112">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="14f6a-113">Assurez-vous [d’installer Microsoft Edge (Chromium).][MicrosoftEdge]</span><span class="sxs-lookup"><span data-stu-id="14f6a-113">Ensure you install [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="14f6a-114">Pour confirmer que Microsoft Edge \(Chromium\) est installé, accédez à , et vérifiez que le numéro de version est `edge://settings/help` version 75 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="14f6a-114">To confirm that you have Microsoft Edge \(Chromium\) installed, navigate to `edge://settings/help`, and verify the version number is Version 75 or later.</span></span>  

## <span data-ttu-id="14f6a-115">Télécharger le pilote Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="14f6a-115">Download Microsoft Edge Driver</span></span>  

<span data-ttu-id="14f6a-116">Pour commencer à automatiser les tests, utilisez les étapes suivantes pour vous assurer que la version WebDriver que vous installez correspond à la version de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="14f6a-116">To begin automating tests, use the following steps to ensure that the WebDriver version you install matches your browser version.</span></span>  

1.  <span data-ttu-id="14f6a-117">Accédez `edge://settings/help` à la version de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="14f6a-117">Navigate to `edge://settings/help` to get the version of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="./media/edge-version.png" alt-text="Numéro de build de Microsoft Edge Canary le 14 janvier 2020":::
       <span data-ttu-id="14f6a-119">Numéro de build de Microsoft Edge Canary le 14 janvier 2020</span><span class="sxs-lookup"><span data-stu-id="14f6a-119">The build number for Microsoft Edge Canary on January 14, 2020</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="14f6a-120">Accédez à la page [téléchargements][MicrosoftDeveloperEdgeToolsWebdriverDownloads] du pilote Microsoft Edge et téléchargez le pilote qui correspond au numéro de version de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="14f6a-120">Navigate to the [Microsoft Edge Driver downloads][MicrosoftDeveloperEdgeToolsWebdriverDownloads] page and download the driver that matches the version number of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="./media/edge-driver-install.png" alt-text="Section Téléchargements de la page Pilote Microsoft Edge":::
       <span data-ttu-id="14f6a-122">Section Téléchargements de la page [Pilote Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="14f6a-122">The Downloads section of the [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] page</span></span>
    :::image-end:::  
    
    <!--  
    > [!NOTE] 
    > For more information about test automation using Microsoft Edge (EdgeHTML), see [Microsoft WebDriver for Microsoft Edge (EdgeHTML)][Webdriver].  
    -->  

## <span data-ttu-id="14f6a-123">Choisir une liaison de langue WebDriver</span><span class="sxs-lookup"><span data-stu-id="14f6a-123">Choose a WebDriver language binding</span></span>  

<span data-ttu-id="14f6a-124">Le dernier composant que vous devez télécharger est un pilote client propre à une langue pour traduire votre code \(Python, Java, C\#, Ruby, JavaScript\) en commandes que le pilote Microsoft Edge exécute dans Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="14f6a-124">The last component you must download is a language-specific client driver to translate your code \(Python, Java, C\#, Ruby, JavaScript\) into commands the Microsoft Edge Driver runs in Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="14f6a-125">[Téléchargez la liaison de langue WebDriver de votre choix.][SeleniumDownloads]</span><span class="sxs-lookup"><span data-stu-id="14f6a-125">[Download the WebDriver language binding of your choice][SeleniumDownloads].</span></span>  <span data-ttu-id="14f6a-126">L’équipe Microsoft Edge recommande [Selenium 4.00-alpha07][NugetPackagesSeleniumWebdriver400alpha07] ou version ultérieure, car elle prend en charge Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="14f6a-126">The Microsoft Edge team recommends [Selenium 4.00-alpha07][NugetPackagesSeleniumWebdriver400alpha07] or later, because it supports Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="14f6a-127">Toutefois, vous pouvez contrôler Microsoft Edge \(Chromium\) dans toutes les versions antérieures de Selenium, y compris la version stable actuelle de Selenium 3.</span><span class="sxs-lookup"><span data-stu-id="14f6a-127">However, you may control Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="14f6a-128">Si vous automatisiez ou testiez précédemment l’utilisation et les classes de Microsoft Edge \(Chromium\), votre code WebDriver ne s’exécute pas sur `ChromeDriver` `ChromeOptions` Microsoft Edge Version 80 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="14f6a-128">If you were previously automating or testing Microsoft Edge \(Chromium\) using `ChromeDriver` and `ChromeOptions` classes, your WebDriver code does not run on Microsoft Edge Version 80 or later.</span></span>  <span data-ttu-id="14f6a-129">Pour résoudre ce problème, mettez à jour vos tests pour utiliser la `EdgeOptions` classe et téléchargez [le pilote Microsoft Edge.][MicrosoftDeveloperEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="14f6a-129">To solve this problem, update your tests to use the `EdgeOptions` class and download [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver].</span></span>  

### <span data-ttu-id="14f6a-130">Utiliser Selenium 3</span><span class="sxs-lookup"><span data-stu-id="14f6a-130">Use Selenium 3</span></span>  

<span data-ttu-id="14f6a-131">Si vous utilisez déjà [Selenium 3,][|::ref1::|]vous avez peut-être des tests de navigateur existants et souhaitez ajouter une couverture pour Microsoft Edge \(Chromium\) sans modifier votre version de Selenium.</span><span class="sxs-lookup"><span data-stu-id="14f6a-131">If you already use [Selenium 3][|::ref1::|], you may have existing browser tests and want to add coverage for Microsoft Edge \(Chromium\) without changing your version of Selenium.</span></span>  <span data-ttu-id="14f6a-132">Pour utiliser [Selenium 3][|::ref2::|] afin d’écrire des tests automatisés pour Microsoft Edge \(EdgeHTML\) et Microsoft Edge \(Chromium\), installez le package [Outils Selenium][GithubMicrosoftEdgeSeleniumTools] pour Microsoft Edge pour utiliser le pilote mis à jour.</span><span class="sxs-lookup"><span data-stu-id="14f6a-132">To use [Selenium 3][|::ref2::|] to write automated tests for both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package to use the updated driver.</span></span>  <span data-ttu-id="14f6a-133">Les `EdgeDriver` `EdgeDriverService` classes incluses dans les outils sont entièrement compatibles avec les équivalents intégrés dans Selenium 4.</span><span class="sxs-lookup"><span data-stu-id="14f6a-133">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium 4.</span></span>  

<span data-ttu-id="14f6a-134">Utilisez les étapes suivantes pour ajouter les outils [Selenium pour Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] et [Selenium 3][|::ref3::|] à votre projet.</span><span class="sxs-lookup"><span data-stu-id="14f6a-134">Use the following steps to add the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] and [Selenium 3][|::ref3::|] to your project.</span></span>  

#### [<span data-ttu-id="14f6a-135">C#</span><span class="sxs-lookup"><span data-stu-id="14f6a-135">C#</span></span>](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="14f6a-136">Ajoutez les packages [Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] et [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] à votre projet .NET à l’aide de l’CLI [NuGet][NugetCLI] [ou Visual Studio][VisualStudio].</span><span class="sxs-lookup"><span data-stu-id="14f6a-136">Add the [Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] and [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] packages to your .NET project using the [NuGet CLI][NugetCLI] or [Visual Studio][VisualStudio].</span></span>  

#### [<span data-ttu-id="14f6a-137">Python</span><span class="sxs-lookup"><span data-stu-id="14f6a-137">Python</span></span>](#tab/python/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="14f6a-138">Utilisez [pip][PythonPip] pour installer [les packages msedge-selenium-tools][PythonSeleniumTools] et [selenium.][PythonSelenium]</span><span class="sxs-lookup"><span data-stu-id="14f6a-138">Use [pip][PythonPip] to install the [msedge-selenium-tools][PythonSeleniumTools] and [selenium][PythonSelenium] packages.</span></span>  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [<span data-ttu-id="14f6a-139">Java</span><span class="sxs-lookup"><span data-stu-id="14f6a-139">Java</span></span>](#tab/java/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="14f6a-140">Si votre Java utilise Maven, ajoutez [msedge-selenium-tools-java][SonatypeMavenRepositorySearch] en faisant face à la dépendance suivante à votre `pom.xml` fichier :</span><span class="sxs-lookup"><span data-stu-id="14f6a-140">If your Java project uses Maven, add [msedge-selenium-tools-java][SonatypeMavenRepositorySearch] by coping the following dependency to your `pom.xml` file:</span></span>  

```xml
<dependency>
    <groupId>com.microsoft.edge</groupId>
    <artifactId>msedge-selenium-tools-java</artifactId>
    <version>[3.141.0,)</version>
</dependency>
```  

<span data-ttu-id="14f6a-141">Le package Java est également disponible en téléchargement directement sur la [page Outils Selenium pour Microsoft Edge Releases.][GithubMicrosoftEdgeSeleniumToolsReleases]</span><span class="sxs-lookup"><span data-stu-id="14f6a-141">The Java package is also available to download directly on the [Selenium Tools for Microsoft Edge Releases page][GithubMicrosoftEdgeSeleniumToolsReleases].</span></span>  

#### [<span data-ttu-id="14f6a-142">JavaScript</span><span class="sxs-lookup"><span data-stu-id="14f6a-142">JavaScript</span></span>](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="14f6a-143">Utilisez [npm pour][JavaScript|::ref4::|] installer [les packages edge-selenium-tools][JavaScriptSeleniumTools] et [selenium-webdriver.][JavaScriptSelenium]</span><span class="sxs-lookup"><span data-stu-id="14f6a-143">Use [npm][JavaScript|::ref4::|] to install the [edge-selenium-tools][JavaScriptSeleniumTools] and [selenium-webdriver][JavaScriptSelenium] packages.</span></span>  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## <span data-ttu-id="14f6a-144">Automatiser Microsoft Edge (Chromium) avec WebDriver</span><span class="sxs-lookup"><span data-stu-id="14f6a-144">Automate Microsoft Edge (Chromium) with WebDriver</span></span>  

<span data-ttu-id="14f6a-145">Pour automatiser un navigateur à l’aide de WebDriver, vous devez d’abord démarrer une session WebDriver à l’aide de votre liaison de langue WebDriver préférée.</span><span class="sxs-lookup"><span data-stu-id="14f6a-145">To automate a browser using WebDriver, you must first start a WebDriver session using your preferred WebDriver language binding.</span></span>  <span data-ttu-id="14f6a-146">Une session est une instance en cours d’exécution unique d’un navigateur qui peut être contrôlée à l’aide de commandes WebDriver.</span><span class="sxs-lookup"><span data-stu-id="14f6a-146">A session is a single running instance of a browser that can be controlled using WebDriver commands.</span></span>  <span data-ttu-id="14f6a-147">Le démarrage d’une session WebDriver lance une nouvelle instance de navigateur.</span><span class="sxs-lookup"><span data-stu-id="14f6a-147">Starting a WebDriver session launches a new browser instance.</span></span>  <span data-ttu-id="14f6a-148">Le navigateur lancé reste ouvert jusqu’à la fermeture de la session WebDriver.</span><span class="sxs-lookup"><span data-stu-id="14f6a-148">The browser that is launched remains open until you close the WebDriver session.</span></span>  

<span data-ttu-id="14f6a-149">Le contenu suivant vous aide à utiliser Selenium pour démarrer une session WebDriver avec Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="14f6a-149">The following content walks you through using Selenium to start a WebDriver session with Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="14f6a-150">Vous pouvez exécuter ces exemples à l’aide de Selenium 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="14f6a-150">You may run theses examples using either Selenium 3 or 4.</span></span>  <span data-ttu-id="14f6a-151">Pour être utilisé avec Selenium 3, le package [Outils Selenium][GithubMicrosoftEdgeSeleniumTools] pour Microsoft Edge doit être installé.</span><span class="sxs-lookup"><span data-stu-id="14f6a-151">To use with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package must be installed.</span></span>  

### <span data-ttu-id="14f6a-152">Automatisation de Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="14f6a-152">Automating Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="14f6a-153">Selenium utilise la `EdgeDriver` classe pour gérer une session Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="14f6a-153">Selenium uses the `EdgeDriver` class to manage a Microsoft Edge \(Chromium\) session.</span></span> <span data-ttu-id="14f6a-154">Pour démarrer une session et automatiser Microsoft Edge \(Chromium\), créez un objet et passez-lui un objet avec la propriété `EdgeDriver` `EdgeOptions` définie sur `UseChromium` `true` .</span><span class="sxs-lookup"><span data-stu-id="14f6a-154">To start a session and automate Microsoft Edge \(Chromium\), create a new `EdgeDriver` object and pass it an `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<span data-ttu-id="14f6a-155">C#</span><span class="sxs-lookup"><span data-stu-id="14f6a-155">C#</span></span>](#tab/c-sharp/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="14f6a-156">Python</span><span class="sxs-lookup"><span data-stu-id="14f6a-156">Python</span></span>](#tab/python/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### [<span data-ttu-id="14f6a-157">Java</span><span class="sxs-lookup"><span data-stu-id="14f6a-157">Java</span></span>](#tab/java/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

<span data-ttu-id="14f6a-158">La classe prend uniquement en charge Microsoft Edge (Chromium) et ne prend pas en charge `EdgeDriver` Microsoft Edge (EdgeHTML).</span><span class="sxs-lookup"><span data-stu-id="14f6a-158">The `EdgeDriver` class supports Microsoft Edge (Chromium) only, and does not support Microsoft Edge (EdgeHTML).</span></span> <span data-ttu-id="14f6a-159">Pour une utilisation de base, vous pouvez créer un `EdgeDriver` sans fournir `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="14f6a-159">For basic usage, you may create an `EdgeDriver` without providing `EdgeOptions`.</span></span>  

```java
EdgeDriver driver = new EdgeDriver();
```  

#### [<span data-ttu-id="14f6a-160">JavaScript</span><span class="sxs-lookup"><span data-stu-id="14f6a-160">JavaScript</span></span>](#tab/javascript/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> <span data-ttu-id="14f6a-161">Si votre administrateur informatique a définie la stratégie [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] sur , le pilote Microsoft Edge ne peut pas piloter Microsoft Edge (Chromium), car le pilote utilise `2` Microsoft Edge [DevTools.][DevtoolsIndex] [][MicrosoftDeveloperEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="14f6a-161">If your IT admin has set the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy to `2`, [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] is not be able to drive Microsoft Edge (Chromium) because the driver uses the [Microsoft Edge DevTools][DevtoolsIndex].</span></span>  <span data-ttu-id="14f6a-162">[Assurez-vous que la stratégie DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] est définie sur ou pour `0` `1` automatiser Microsoft Edge (Chromium).</span><span class="sxs-lookup"><span data-stu-id="14f6a-162">Ensure the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy is set to `0` or `1` to automate Microsoft Edge (Chromium).</span></span>  

### <span data-ttu-id="14f6a-163">Choix de binaires de navigateur spécifiques (chrome uniquement)</span><span class="sxs-lookup"><span data-stu-id="14f6a-163">Choosing Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="14f6a-164">Vous pouvez démarrer une session WebDriver avec des binaires Microsoft Edge \(Chromium\) spécifiques.</span><span class="sxs-lookup"><span data-stu-id="14f6a-164">You may start a WebDriver session with specific Microsoft Edge \(Chromium\) binaries.</span></span>  <span data-ttu-id="14f6a-165">Par exemple, vous pouvez exécuter des tests à l’aide des canaux [d’aperçu De Microsoft Edge][MicrosoftedgeinsiderDownload] tels que Microsoft Edge Bêta.</span><span class="sxs-lookup"><span data-stu-id="14f6a-165">For example, you may run tests using the [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<span data-ttu-id="14f6a-166">C#</span><span class="sxs-lookup"><span data-stu-id="14f6a-166">C#</span></span>](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="14f6a-167">Python</span><span class="sxs-lookup"><span data-stu-id="14f6a-167">Python</span></span>](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [<span data-ttu-id="14f6a-168">Java</span><span class="sxs-lookup"><span data-stu-id="14f6a-168">Java</span></span>](#tab/java/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.setBinary("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

EdgeDriver driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="14f6a-169">JavaScript</span><span class="sxs-lookup"><span data-stu-id="14f6a-169">JavaScript</span></span>](#tab/javascript/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <span data-ttu-id="14f6a-170">Personnalisation du service de pilote Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="14f6a-170">Customizing the Microsoft Edge Driver Service</span></span>  

#### [<span data-ttu-id="14f6a-171">C#</span><span class="sxs-lookup"><span data-stu-id="14f6a-171">C#</span></span>](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="14f6a-172">Lorsqu’une instance de classe est créée à l’aide d’une classe, elle crée et lance la classe appropriée pour `EdgeDriver` `EdgeOptions` Microsoft Edge `EdgeDriverService` \(EdgeHTML\) ou Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="14f6a-172">When an `EdgeDriver` class instance is created using `EdgeOptions` class, it creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="14f6a-173">Si vous souhaitez créer un , créez-en un configuré pour `EdgeDriverService` Microsoft Edge \(Chromium\) à l’aide de la `CreateChromiumService()` méthode.</span><span class="sxs-lookup"><span data-stu-id="14f6a-173">If you want to create an `EdgeDriverService`, create one configured for Microsoft Edge \(Chromium\) using the `CreateChromiumService()` method.</span></span>  <span data-ttu-id="14f6a-174">Il peut vous être utile d’ajouter des personnalisations.</span><span class="sxs-lookup"><span data-stu-id="14f6a-174">You may find it useful when you need to add customizations.</span></span> <span data-ttu-id="14f6a-175">Par exemple, le code suivant démarre une sortie détaillée du journal.</span><span class="sxs-lookup"><span data-stu-id="14f6a-175">For example, the following code starts verbose log output.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
><span data-ttu-id="14f6a-176">Il n’est pas nécessaire de fournir `EdgeOptions` l’objet lors de la transmission `EdgeDriverService` à `EdgeDriver` l’instance.</span><span class="sxs-lookup"><span data-stu-id="14f6a-176">You do not need to provide the `EdgeOptions` object when passing `EdgeDriverService` to the `EdgeDriver` instance.</span></span>  <span data-ttu-id="14f6a-177">La classe utilise les options par défaut pour `EdgeDriver` Microsoft Edge \(EdgeHTML\) ou Microsoft Edge \(Chromium\) en fonction du service que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="14f6a-177">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) based on the service you provide.</span></span>  
> <span data-ttu-id="14f6a-178">Toutefois, si vous souhaitez fournir les deux classes, assurez-vous que les deux sont configurés pour `EdgeDriverService` la même version de Microsoft `EdgeOptions` Edge.</span><span class="sxs-lookup"><span data-stu-id="14f6a-178">However, if you want to provide both `EdgeDriverService` and `EdgeOptions` classes, ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="14f6a-179">Par exemple, il n’est pas possible d’utiliser une classe Microsoft Edge \(EdgeHTML\) par défaut et des propriétés `EdgeDriverService` Chromium dans la `EdgeOptions` classe.</span><span class="sxs-lookup"><span data-stu-id="14f6a-179">For example, it is not possible to use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="14f6a-180">La `EdgeDriver` classe envoie une erreur pour empêcher l’utilisation de différentes versions.</span><span class="sxs-lookup"><span data-stu-id="14f6a-180">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<span data-ttu-id="14f6a-181">Python</span><span class="sxs-lookup"><span data-stu-id="14f6a-181">Python</span></span>](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="14f6a-182">Lorsque vous utilisez Python, `Edge` l’objet crée et gère le `EdgeService` .</span><span class="sxs-lookup"><span data-stu-id="14f6a-182">When using Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="14f6a-183">Pour configurer le `EdgeService` , passez des arguments supplémentaires à l’objet `Edge` comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="14f6a-183">To configure the `EdgeService`, pass additional arguments to the `Edge` object as indicated in the following code.</span></span>  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<span data-ttu-id="14f6a-184">Java</span><span class="sxs-lookup"><span data-stu-id="14f6a-184">Java</span></span>](#tab/java/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="14f6a-185">Utilisez la `createDefaultService()` méthode pour créer une configuration pour Microsoft Edge `EdgeDriverService` \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="14f6a-185">Use the `createDefaultService()` method to create an `EdgeDriverService` configured for Microsoft Edge \(Chromium\).</span></span> <span data-ttu-id="14f6a-186">Les services de pilotes Java sont personnalisés à l’aide Java propriétés système.</span><span class="sxs-lookup"><span data-stu-id="14f6a-186">Driver services in Java are customized using Java system properties.</span></span> <span data-ttu-id="14f6a-187">Par exemple, le code suivant utilise la `"webdriver.edge.verboseLogging"` propriété pour activer la sortie détaillée du journal.</span><span class="sxs-lookup"><span data-stu-id="14f6a-187">For example, the following code uses the `"webdriver.edge.verboseLogging"` property to enable verbose log output.</span></span>  

```java
System.setProperty("webdriver.edge.verboseLogging", "true");
EdgeDriverService service = EdgeDriverService.createDefaultService();
EdgeOptions options = new EdgeOptions();
EdgeDriver driver = new EdgeDriver(service, options);
```  

#### [<span data-ttu-id="14f6a-188">JavaScript</span><span class="sxs-lookup"><span data-stu-id="14f6a-188">JavaScript</span></span>](#tab/javascript/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="14f6a-189">Lorsque vous utilisez JavaScript, créez et configurez un avec `Service` la `ServiceBuilder` classe.</span><span class="sxs-lookup"><span data-stu-id="14f6a-189">When using JavaScript, create and configure a `Service` with the `ServiceBuilder` class.</span></span>  <span data-ttu-id="14f6a-190">Si vous le souhaitez, vous pouvez transmettre l’objet à l’objet, qui `Service` `Driver` démarre \(et arrête\) le service pour vous.</span><span class="sxs-lookup"><span data-stu-id="14f6a-190">Optionally, you may pass the `Service` object to the `Driver` object, which starts \(and stops\) the service for you.</span></span>  
<span data-ttu-id="14f6a-191">Pour configurer la `Service` méthode, exécutez une autre méthode dans la `ServiceBuilder` classe avant d’utiliser la `build()` méthode.</span><span class="sxs-lookup"><span data-stu-id="14f6a-191">To configure the `Service`, run another method in the `ServiceBuilder` class before using the `build()` method.</span></span>  <span data-ttu-id="14f6a-192">Passez ensuite le `service` paramètre en tant que paramètre dans la `Driver.createSession()` méthode.</span><span class="sxs-lookup"><span data-stu-id="14f6a-192">Then pass the `service` as a parameter in the `Driver.createSession()` method.</span></span>  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### <span data-ttu-id="14f6a-193">Utiliser les Chromium-Specific options</span><span class="sxs-lookup"><span data-stu-id="14f6a-193">Use Chromium-Specific Options</span></span>  

<span data-ttu-id="14f6a-194">Si vous définissez la propriété sur , vous pouvez utiliser la classe pour accéder aux mêmes propriétés et méthodes spécifiques au Chromium qui sont utilisées lors de l’automatisation d’autres `UseChromium` `true` `EdgeOptions` navigateurs Chromium. [][WebdriverCapabilitiesEdgeOptions]</span><span class="sxs-lookup"><span data-stu-id="14f6a-194">If you set the `UseChromium` property to `true`, you may use the `EdgeOptions` class to access the same [Chromium-specific properties and methods][WebdriverCapabilitiesEdgeOptions] that are used when automating other Chromium browsers.</span></span>  

#### [<span data-ttu-id="14f6a-195">C#</span><span class="sxs-lookup"><span data-stu-id="14f6a-195">C#</span></span>](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<span data-ttu-id="14f6a-196">Python</span><span class="sxs-lookup"><span data-stu-id="14f6a-196">Python</span></span>](#tab/python/)  

<a id="using-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<span data-ttu-id="14f6a-197">Java</span><span class="sxs-lookup"><span data-stu-id="14f6a-197">Java</span></span>](#tab/java/)  

<a id="using-chromium-specific-options-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

#### [<span data-ttu-id="14f6a-198">JavaScript</span><span class="sxs-lookup"><span data-stu-id="14f6a-198">JavaScript</span></span>](#tab/javascript/)  

<a id="using-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

* * *  

> [!NOTE]
> <span data-ttu-id="14f6a-199">Si la propriété est définie sur , vous ne pouvez pas utiliser les propriétés et méthodes `UseChromium` `true` pour Microsoft Edge \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="14f6a-199">If the `UseChromium` property is set to `true`, you are not able to use properties and methods for Microsoft Edge \(EdgeHTML\).</span></span>  

## <span data-ttu-id="14f6a-200">Options d’installation WebDriver supplémentaires</span><span class="sxs-lookup"><span data-stu-id="14f6a-200">Additional WebDriver installation options</span></span>  

### <span data-ttu-id="14f6a-201">Erzy</span><span class="sxs-lookup"><span data-stu-id="14f6a-201">Chocolatey</span></span>  

<span data-ttu-id="14f6a-202">Si vous utilisez [Lesy comme][Chocolatey] gestionnaire de package, installez le pilote Microsoft Edge en exécutant la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="14f6a-202">If you use [Chocolatey][Chocolatey] as your package manager, install the Microsoft Edge Driver by running the following command.</span></span>  

```console
choco install selenium-chromium-edge-driver
```  

<span data-ttu-id="14f6a-203">Pour plus d’informations, [voir Pilote Edge Selenium Chromium sur Le Site.][ChocolateyPackagesSeleniumChromiumEdgeDriver]</span><span class="sxs-lookup"><span data-stu-id="14f6a-203">For more information, see [Selenium Chromium Edge Driver on Chocolatey][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span></span>  

### <span data-ttu-id="14f6a-204">Docker</span><span class="sxs-lookup"><span data-stu-id="14f6a-204">Docker</span></span>  

<span data-ttu-id="14f6a-205">Si vous utilisez [Docker][DockerHub], téléchargez une image pré-configurée avec Microsoft Edge \(Chromium\) et le pilote [Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] préinstallés en exécutant la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="14f6a-205">If you use [Docker][DockerHub], download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] pre-installed by running the following command.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="14f6a-206">Pour plus d’informations, accédez au [conteneur msedgedriver sur Docker Hub.][DockerHubMsedgedriver]</span><span class="sxs-lookup"><span data-stu-id="14f6a-206">For more information, navigate to the [msedgedriver container on Docker Hub][DockerHubMsedgedriver].</span></span>  

## <span data-ttu-id="14f6a-207">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="14f6a-207">Next steps</span></span>

<span data-ttu-id="14f6a-208">Pour en savoir plus sur WebDriver et comment écrire des tests WebDriver automatisés à l’aide de Selenium, accédez à la [documentation selenium.][SeleniumDocumentation]</span><span class="sxs-lookup"><span data-stu-id="14f6a-208">To learn more about WebDriver and how to write automated WebDriver tests using Selenium, navigate to the [Selenium documentation][SeleniumDocumentation].</span></span>  

## <span data-ttu-id="14f6a-209">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="14f6a-209">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="14f6a-210">L’équipe Microsoft Edge est impatiente de connaître vos commentaires sur l’utilisation de WebDriver, de Selenium et de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="14f6a-210">The Microsoft Edge team is eager to hear your feedback about using WebDriver, Selenium, and Microsoft Edge.</span></span>  <span data-ttu-id="14f6a-211">Pour envoyer à l’équipe vos \*\*\*\* questions et commentaires, sélectionnez l’icône Envoyer des commentaires dans Microsoft Edge DevTools ou envoyez un tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="14f6a-211">To send the team your questions and comments, choose the **Send Feedback** icon in the Microsoft Edge DevTools or send a tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="L’icône Envoyer des commentaires dans Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="14f6a-213">Icône **Envoyer des commentaires** dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="14f6a-213">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- links -->  

[DevtoolsIndex]: ../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  
[WebdriverCapabilitiesEdgeOptions]: ./capabilities-edge-options.md "Fonctionnalités et fonctionnalités EdgeOptions | Documents Microsoft"  
<!--[Webdriver]: ../edgehtml/webdriver/index.md "WebDriver (EdgeHTML) | Microsoft Docs"  -->  

[DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability - Microsoft Edge - Stratégies | Documents Microsoft"  

[Chocolatey]: https://chocolatey.org "| Logiciels espions"  
[ChocolateyPackagesSeleniumChromiumEdgeDriver]: https://chocolatey.org/packages/selenium-chromium-edge-driver "Pilote Edge Selenium Chromium | Erzy"  

[DockerHub]: https://hub.docker.com "Docker Hub"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Hub Docker"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "microsoft/edge-selenium-tools | GitHub"  
[GithubMicrosoftEdgeSeleniumToolsReleases]: https://github.com/microsoft/edge-selenium-tools/releases "microsoft/edge-selenium-tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SeleniumHQ/selenium | GitHub"  

[JavaScriptnpm]: https://www.npmjs.com/ "npm"  
[JavaScriptSeleniumTools]: https://www.npmjs.com/package/@microsoft/edge-selenium-tools "@microsoft/edge-selenium-tools | npm"  
[JavaScriptSelenium]: https://www.npmjs.com/package/selenium-webdriver "selenium-webdriver | npm"  

[MicrosoftDeveloperEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "WebDriver | Développeur Microsoft"  
[MicrosoftDeveloperEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads "Téléchargements - WebDriver | Développeur Microsoft"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Télécharger le nouveau navigateur Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  

[NugetCLI]:https://www.nuget.org/packages/NuGet.CommandLine/ "NuGet.CommandLine | NuGet Gallery"  
[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft.Edge.SeleniumTools | NuGet Gallery"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Selenium.WebDriver 3.141.0 | NuGet Gallery"  
[NugetPackagesSeleniumWebdriver400alpha07]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha07 "Selenium.WebDriver 4.0.0-alpha07 | NuGet Gallery"  

[PythonPip]: https://pypi.org/project/pip/ "pip | PyPI"  
[PythonSeleniumTools]: https://pypi.org/project/msedge-selenium-tools/ "Msedge-selenium-tools | PyPI"  
[PythonSelenium]: https://pypi.org/project/selenium/ "selenium | PyPI"

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDocumentation]: https://www.selenium.dev/documentation "Le projet Selenium Browser Automation : : documentation pour Selenium"  
[SeleniumDownloads]: https://selenium.dev/downloads "Téléchargements | Selenium"  

[SonatypeMavenRepositorySearch]: https://search.maven.org/artifact/com.microsoft.edge/msedge-selenium-tools-java/3.141.0/jar "sonatype Maven Central Repository Search | com.microsoft.edge:msedge-selenium-tools-java"

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publier un tweet"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver | W3C"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Navigateur sans | Wikipedia"  
