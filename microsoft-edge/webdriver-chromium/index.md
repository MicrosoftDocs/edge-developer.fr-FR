---
description: Découvrez comment tester votre site web ou votre application dans Microsoft Edge ou automatiser le navigateur avec WebDriver
title: Utiliser WebDriver (Chromium) pour tester l’automatisation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/20/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, développement web, html, css, javascript, développeur, webdriver, selenium, test, outils, automatisation, test
ms.openlocfilehash: 5d30fe14051ac8857c6ea4d64b8c8f1f8e8049ac
ms.sourcegitcommit: a7609b75a94755ed983111af7083a0d3bf64eeac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "11583586"
---
# <a name="use-webdriver-chromium-for-test-automation"></a><span data-ttu-id="d6ec1-104">Utiliser WebDriver (Chromium) pour tester l’automatisation</span><span class="sxs-lookup"><span data-stu-id="d6ec1-104">Use WebDriver (Chromium) for test automation</span></span>  

<span data-ttu-id="d6ec1-105">WebDriver permet aux développeurs de créer des tests automatisés qui simulent l’interaction utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-105">WebDriver allows developers to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="d6ec1-106">Les tests et simulations WebDriver diffèrent des tests unitaires JavaScript des manières suivantes.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-106">WebDriver tests and simulations differ from JavaScript unit tests in the following ways.</span></span>  

*   <span data-ttu-id="d6ec1-107">Accède aux fonctionnalités et informations non disponibles pour JavaScript s’exécutant dans les navigateurs.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-107">Accesses functionality and information not available to JavaScript running in browsers.</span></span>  
*   <span data-ttu-id="d6ec1-108">Simule les événements utilisateur ou au niveau du système d’exploitation plus précisément.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-108">Simulates user events or OS-level events more accurately.</span></span>  
*   <span data-ttu-id="d6ec1-109">Gère plusieurs fenêtres, onglets et pages web en une seule session de test.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-109">Manages multiple windows, tabs, and webpages in a single test session.</span></span>  
*   <span data-ttu-id="d6ec1-110">Exécute plusieurs sessions de Microsoft Edge sur un ordinateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-110">Runs multiple sessions of Microsoft Edge on a specific machine.</span></span>  
    
<span data-ttu-id="d6ec1-111">La section suivante décrit comment commencer avec WebDriver pour Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="d6ec1-111">The following section describes how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  

## <a name="install-microsoft-edge-chromium"></a><span data-ttu-id="d6ec1-112">Installer Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="d6ec1-112">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="d6ec1-113">Veillez à installer [Microsoft Edge (Chromium).][MicrosoftEdge]</span><span class="sxs-lookup"><span data-stu-id="d6ec1-113">Ensure you install [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="d6ec1-114">Pour confirmer que vous avez installé Microsoft Edge \(Chromium\), accédez à et vérifiez que le numéro de version est `edge://settings/help` la version 75 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-114">To confirm that you have Microsoft Edge \(Chromium\) installed, navigate to `edge://settings/help`, and verify the version number is version 75 or later.</span></span>  

## <a name="download-microsoft-edge-driver"></a><span data-ttu-id="d6ec1-115">Télécharger Microsoft Edge Driver</span><span class="sxs-lookup"><span data-stu-id="d6ec1-115">Download Microsoft Edge Driver</span></span>  

<span data-ttu-id="d6ec1-116">Pour commencer à automatiser les tests, utilisez les étapes suivantes pour vous assurer que la version WebDriver que vous installez correspond à la version de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-116">To begin automating tests, use the following steps to ensure that the WebDriver version you install matches your browser version.</span></span>  

1.  <span data-ttu-id="d6ec1-117">Recherchez votre version de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-117">Find your version of Microsoft Edge.</span></span>  
    1.  <span data-ttu-id="d6ec1-118">Naviguez vers`edge://settings/help` .</span><span class="sxs-lookup"><span data-stu-id="d6ec1-118">Navigate to `edge://settings/help`.</span></span>  
        
        :::image type="complex" source="./media/microsoft-edge-version.msft.png" alt-text="Numéro de build de Microsoft Edge le 15 avril 2021" lightbox="./media/microsoft-edge-version.msft.png":::
           <span data-ttu-id="d6ec1-120">Numéro de build de Microsoft Edge le 15 avril 2021</span><span class="sxs-lookup"><span data-stu-id="d6ec1-120">The build number for Microsoft Edge on April 15, 2021</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="d6ec1-121">Accédez à [Microsoft Edge pilote .][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="d6ec1-121">Navigate to [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].</span></span>  
1.  <span data-ttu-id="d6ec1-122">Accédez à **Obtenir la dernière version.**</span><span class="sxs-lookup"><span data-stu-id="d6ec1-122">Navigate to **Get the latest version**.</span></span>  
1.  <span data-ttu-id="d6ec1-123">Choisissez la version du canal qui correspond à votre numéro de version de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-123">Choose the build of channel that matches your version number of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="./media/microsoft-edge-driver-install.msft.png" alt-text="Section Obtenir la dernière version sur la page web Microsoft Edge driver" lightbox="./media/microsoft-edge-driver-install.msft.png":::
       <span data-ttu-id="d6ec1-125">Section **Obtenir la dernière version** sur la page web Microsoft Edge [driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="d6ec1-125">The **Get the latest version** section on the [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] webpage</span></span>  
    :::image-end:::  
    
    <!--  
    > [!NOTE] 
    > For more information about test automation using Microsoft Edge \(EdgeHTML\), navigate to [Microsoft Edge Driver for Microsoft Edge (EdgeHTML)][Webdriver].  
    -->  
    
## <a name="choose-a-webdriver-language-binding"></a><span data-ttu-id="d6ec1-126">Choisir une liaison de langue WebDriver</span><span class="sxs-lookup"><span data-stu-id="d6ec1-126">Choose a WebDriver language binding</span></span>  

<span data-ttu-id="d6ec1-127">Le dernier composant que vous devez télécharger est un pilote client propre à une langue pour traduire votre code \(Python, Java, C\#, Ruby, JavaScript\) en commandes que le pilote Microsoft Edge exécute dans Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="d6ec1-127">The last component you must download is a language-specific client driver to translate your code \(Python, Java, C\#, Ruby, JavaScript\) into commands the Microsoft Edge Driver runs in Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="d6ec1-128">[Téléchargez la liaison de langue WebDriver de votre choix.][SeleniumDownloads]</span><span class="sxs-lookup"><span data-stu-id="d6ec1-128">[Download the WebDriver language binding of your choice][SeleniumDownloads].</span></span>  <span data-ttu-id="d6ec1-129">L’Microsoft Edge recommande [Selenium 4.0.0-beta2][NugetPackagesSeleniumWebdriver400beta02] ou version ultérieure, car il prend en charge Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="d6ec1-129">The Microsoft Edge team recommends [Selenium 4.0.0-beta2][NugetPackagesSeleniumWebdriver400beta02] or later, because it supports Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="d6ec1-130">Toutefois, vous pouvez contrôler Microsoft Edge \(Chromium\) dans toutes les versions antérieures de Selenium, y compris la version stable actuelle de Selenium 3.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-130">However, you can control Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="d6ec1-131">Si vous avez précédemment automatisé ou testé Microsoft Edge \(Chromium\) et des classes, votre code WebDriver ne s’exécute pas sur Microsoft Edge `ChromeDriver` `ChromeOptions` version 80 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-131">If you previously automated or tested Microsoft Edge \(Chromium\) using `ChromeDriver` and `ChromeOptions` classes, your WebDriver code does not run on Microsoft Edge Version 80 or later.</span></span>  <span data-ttu-id="d6ec1-132">Pour résoudre le problème, mettez à jour vos tests pour utiliser la classe `EdgeOptions` et téléchargez [Microsoft Edge pilote][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].</span><span class="sxs-lookup"><span data-stu-id="d6ec1-132">To solve the problem, update your tests to use the `EdgeOptions` class and download [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].</span></span>  

### <a name="using-selenium-4"></a><span data-ttu-id="d6ec1-133">Utilisation de Selenium 4</span><span class="sxs-lookup"><span data-stu-id="d6ec1-133">Using Selenium 4</span></span>

<span data-ttu-id="d6ec1-134">Selenium 4 dispose d’une prise en charge intégrée des Microsoft Edge (Chromium).</span><span class="sxs-lookup"><span data-stu-id="d6ec1-134">Selenium 4 has built-in support for Microsoft Edge (Chromium).</span></span>  <span data-ttu-id="d6ec1-135">Pour installer Selenium 4, accédez à [l’installation des bibliothèques Selenium.][SeleniumInstallingLibraries]</span><span class="sxs-lookup"><span data-stu-id="d6ec1-135">To install Selenium 4, navigate to [Installing Selenium libraries][SeleniumInstallingLibraries].</span></span>

<span data-ttu-id="d6ec1-136">Lorsque vous utilisez Selenium 4, vous n’avez pas besoin d’utiliser les outils Selenium pour Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-136">When you use Selenium 4, you don't need to use Selenium Tools for Microsoft Edge.</span></span>  <span data-ttu-id="d6ec1-137">Outils Selenium pour Microsoft Edge uniquement pour Lelenium 3.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-137">Selenium Tools for Microsoft Edge is for Selenium 3 only.</span></span>  <span data-ttu-id="d6ec1-138">Si vous essayez d’utiliser Selenium 4 avec les outils Selenium pour Microsoft Edge et que vous essayez de créer une instance, vous obtenez `EdgeDriver` l’erreur suivante : `System.MissingMethodException: 'Method not found: 'OpenQA.Selenium.Remote.DesiredCapabilities OpenQA.Selenium.DriverOptions.GenerateDesiredCapabilities(Boolean)'` .</span><span class="sxs-lookup"><span data-stu-id="d6ec1-138">If you try to use Selenium 4 with Selenium Tools for Microsoft Edge and try create a new `EdgeDriver` instance, you get the following error: `System.MissingMethodException: 'Method not found: 'OpenQA.Selenium.Remote.DesiredCapabilities OpenQA.Selenium.DriverOptions.GenerateDesiredCapabilities(Boolean)'`.</span></span>  

<span data-ttu-id="d6ec1-139">Si vous utilisez Selenium 4 et obtenez cette erreur, supprimez votre projet et assurez-vous que vous utilisez l’officiel et les classes de `Microsoft.Edge.SeleniumTools` l’espace `EdgeOptions` `EdgeDriver` de `OpenQA.Selenium.Edge` noms.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-139">If you're using Selenium 4 and get this error, remove `Microsoft.Edge.SeleniumTools` from your project, and make sure you're using the official `EdgeOptions` and `EdgeDriver` classes from the `OpenQA.Selenium.Edge` namespace.</span></span>

### <a name="using-selenium-3"></a><span data-ttu-id="d6ec1-140">Utilisation de Selenium 3</span><span class="sxs-lookup"><span data-stu-id="d6ec1-140">Using Selenium 3</span></span>  

<span data-ttu-id="d6ec1-141">Si vous utilisez déjà [Selenium 3,][|::ref1::|]vous avez peut-être des tests de navigateur existants et souhaitez ajouter une couverture pour Microsoft Edge \(Chromium\) sans modifier votre version de Selenium.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-141">If you already use [Selenium 3][|::ref1::|], you may have existing browser tests and want to add coverage for Microsoft Edge \(Chromium\) without changing your version of Selenium.</span></span>  <span data-ttu-id="d6ec1-142">Pour utiliser [Selenium 3][|::ref2::|] afin d’écrire des tests automatisés pour Microsoft Edge \(EdgeHTML\) et Microsoft Edge \(Chromium\), installez le package [Outils Selenium][GithubMicrosoftEdgeSeleniumTools] pour Microsoft Edge pour utiliser le pilote mis à jour.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-142">To use [Selenium 3][|::ref2::|] to write automated tests for both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package to use the updated driver.</span></span>  <span data-ttu-id="d6ec1-143">Les `EdgeDriver` `EdgeDriverService` classes incluses dans les outils sont entièrement compatibles avec les équivalents intégrés dans Selenium 4.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-143">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium 4.</span></span>  

<span data-ttu-id="d6ec1-144">Utilisez les étapes suivantes pour ajouter les outils [Selenium pour Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] [et Selenium 3][|::ref3::|] à votre projet.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-144">Use the following steps to add the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] and [Selenium 3][|::ref3::|] to your project.</span></span>  

#### [<a name="c"></a><span data-ttu-id="d6ec1-145">C#</span><span class="sxs-lookup"><span data-stu-id="d6ec1-145">C#</span></span>](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="d6ec1-146">Ajoutez les packages [Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] et [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] à votre projet .NET à l’aide NuGet [CLI][NugetCLI] ou [Visual Studio][VisualStudio].</span><span class="sxs-lookup"><span data-stu-id="d6ec1-146">Add the [Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] and [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] packages to your .NET project using the [NuGet CLI][NugetCLI] or [Visual Studio][VisualStudio].</span></span>  

#### [<a name="python"></a><span data-ttu-id="d6ec1-147">Python</span><span class="sxs-lookup"><span data-stu-id="d6ec1-147">Python</span></span>](#tab/python/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="d6ec1-148">Utilisez [pip][PythonPip] pour installer [les packages msedge-selenium-tools][PythonSeleniumTools] et [selenium.][PythonSelenium]</span><span class="sxs-lookup"><span data-stu-id="d6ec1-148">Use [pip][PythonPip] to install the [msedge-selenium-tools][PythonSeleniumTools] and [selenium][PythonSelenium] packages.</span></span>  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [<a name="java"></a><span data-ttu-id="d6ec1-149">Java</span><span class="sxs-lookup"><span data-stu-id="d6ec1-149">Java</span></span>](#tab/java/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="d6ec1-150">Si votre Java utilise Maven, copiez et collez la dépendance suivante dans votre fichier pour ajouter `pom.xml` [msedge-selenium-tools-java][SonatypeMavenRepositorySearch].</span><span class="sxs-lookup"><span data-stu-id="d6ec1-150">If your Java project uses Maven, copy and paste the following dependency to your `pom.xml` file to add [msedge-selenium-tools-java][SonatypeMavenRepositorySearch].</span></span>  

```xml
<dependency>
    <groupId>com.microsoft.edge</groupId>
    <artifactId>msedge-selenium-tools-java</artifactId>
    <version>[3.141.0,)</version>
</dependency>
```  

<span data-ttu-id="d6ec1-151">Le package Java est également disponible en téléchargement directement sur la [page Outils Selenium Microsoft Edge releases.][GithubMicrosoftEdgeSeleniumToolsReleases]</span><span class="sxs-lookup"><span data-stu-id="d6ec1-151">The Java package is also available to download directly on the [Selenium Tools for Microsoft Edge Releases page][GithubMicrosoftEdgeSeleniumToolsReleases].</span></span>  

#### [<a name="javascript"></a><span data-ttu-id="d6ec1-152">JavaScript</span><span class="sxs-lookup"><span data-stu-id="d6ec1-152">JavaScript</span></span>](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="d6ec1-153">Utilisez [npm pour][JavaScript|::ref4::|] installer [les packages edge-selenium-tools][JavaScriptSeleniumTools] et [selenium-webdriver.][JavaScriptSelenium]</span><span class="sxs-lookup"><span data-stu-id="d6ec1-153">Use [npm][JavaScript|::ref4::|] to install the [edge-selenium-tools][JavaScriptSeleniumTools] and [selenium-webdriver][JavaScriptSelenium] packages.</span></span>  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## <a name="automate-microsoft-edge-chromium-with-webdriver"></a><span data-ttu-id="d6ec1-154">Automatiser Microsoft Edge (Chromium) avec WebDriver</span><span class="sxs-lookup"><span data-stu-id="d6ec1-154">Automate Microsoft Edge (Chromium) with WebDriver</span></span>  

<span data-ttu-id="d6ec1-155">Pour automatiser un navigateur à l’aide de WebDriver, vous devez d’abord démarrer une session WebDriver à l’aide de votre liaison de langue WebDriver préférée.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-155">To automate a browser using WebDriver, you must first start a WebDriver session using your preferred WebDriver language binding.</span></span>  <span data-ttu-id="d6ec1-156">Une session est une instance en cours d’exécution unique d’un navigateur contrôlée à l’aide de commandes WebDriver.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-156">A session is a single running instance of a browser controlled using WebDriver commands.</span></span>  <span data-ttu-id="d6ec1-157">Démarrez une session WebDriver pour lancer une nouvelle instance de navigateur.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-157">Start a WebDriver session to launch a new browser instance.</span></span>  <span data-ttu-id="d6ec1-158">L’instance de navigateur lancée reste ouverte jusqu’à la fermeture de la session WebDriver.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-158">The launched browser instance remains open until you close the WebDriver session.</span></span>  

<span data-ttu-id="d6ec1-159">Le contenu suivant vous aide à utiliser Selenium pour démarrer une session WebDriver avec Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="d6ec1-159">The following content walks you through using Selenium to start a WebDriver session with Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="d6ec1-160">Vous pouvez exécuter les exemples à l’aide de Selenium 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-160">You can run the examples using either Selenium 3 or 4.</span></span>  <span data-ttu-id="d6ec1-161">Pour être utilisé avec Selenium 3, le package [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package doit être installé.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-161">To use with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package must be installed.</span></span>  

### <a name="automate-microsoft-edge-chromium"></a><span data-ttu-id="d6ec1-162">Automatiser Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="d6ec1-162">Automate Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="d6ec1-163">Selenium utilise la `EdgeDriver` classe pour gérer une session Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="d6ec1-163">Selenium uses the `EdgeDriver` class to manage a Microsoft Edge \(Chromium\) session.</span></span>  <span data-ttu-id="d6ec1-164">Pour démarrer une session et automatiser Microsoft Edge \(Chromium\), créez un objet et passez-lui un objet avec la propriété `EdgeDriver` `EdgeOptions` définie sur `UseChromium` `true` .</span><span class="sxs-lookup"><span data-stu-id="d6ec1-164">To start a session and automate Microsoft Edge \(Chromium\), create a new `EdgeDriver` object and pass it an `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<a name="c"></a><span data-ttu-id="d6ec1-165">C#</span><span class="sxs-lookup"><span data-stu-id="d6ec1-165">C#</span></span>](#tab/c-sharp/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<a name="python"></a><span data-ttu-id="d6ec1-166">Python</span><span class="sxs-lookup"><span data-stu-id="d6ec1-166">Python</span></span>](#tab/python/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options = options)
```  

#### [<a name="java"></a><span data-ttu-id="d6ec1-167">Java</span><span class="sxs-lookup"><span data-stu-id="d6ec1-167">Java</span></span>](#tab/java/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

<span data-ttu-id="d6ec1-168">La classe prend uniquement en charge Microsoft Edge \(Chromium\) et ne prend pas en `EdgeDriver` charge Microsoft Edge \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="d6ec1-168">The `EdgeDriver` class only supports Microsoft Edge \(Chromium\), and doesn't support Microsoft Edge \(EdgeHTML\).</span></span>  <span data-ttu-id="d6ec1-169">Pour une utilisation de base, vous pouvez créer un `EdgeDriver` sans fournir `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="d6ec1-169">For basic usage, you can create an `EdgeDriver` without providing `EdgeOptions`.</span></span>  

```java
EdgeDriver driver = new EdgeDriver();
```  

#### [<a name="javascript"></a><span data-ttu-id="d6ec1-170">JavaScript</span><span class="sxs-lookup"><span data-stu-id="d6ec1-170">JavaScript</span></span>](#tab/javascript/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> <span data-ttu-id="d6ec1-171">Si votre administrateur informatique a définie la stratégie [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] sur , le pilote Microsoft Edge ne peut pas conduire Microsoft Edge \(Chromium\), car le pilote utilise Microsoft Edge `2` [DevTools][DevtoolsIndex]. [][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="d6ec1-171">If your IT admin has set the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy to `2`,  [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] is blocked from driving Microsoft Edge \(Chromium\), because the driver uses the [Microsoft Edge DevTools][DevtoolsIndex].</span></span>  <span data-ttu-id="d6ec1-172">[Assurez-vous que la stratégie DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] est définie sur ou pour automatiser Microsoft Edge `0` `1` (Chromium).</span><span class="sxs-lookup"><span data-stu-id="d6ec1-172">Ensure the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy is set to `0` or `1` to automate Microsoft Edge (Chromium).</span></span>  

### <a name="choose-specific-browser-binaries-chromium-only"></a><span data-ttu-id="d6ec1-173">Choisir des binaires de navigateur spécifiques (Chromium uniquement)</span><span class="sxs-lookup"><span data-stu-id="d6ec1-173">Choose Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="d6ec1-174">Vous pouvez démarrer une session WebDriver avec des Microsoft Edge binaires \(Chromium\) spécifiques.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-174">You can start a WebDriver session with specific Microsoft Edge \(Chromium\) binaries.</span></span>  <span data-ttu-id="d6ec1-175">Par exemple, vous pouvez exécuter des tests à [l’aide des canaux Microsoft Edge prévisualisation][MicrosoftedgeinsiderDownload] tels que Microsoft Edge Beta.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-175">For example, you can run tests using the [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<a name="c"></a><span data-ttu-id="d6ec1-176">C#</span><span class="sxs-lookup"><span data-stu-id="d6ec1-176">C#</span></span>](#tab/c-sharp/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<a name="python"></a><span data-ttu-id="d6ec1-177">Python</span><span class="sxs-lookup"><span data-stu-id="d6ec1-177">Python</span></span>](#tab/python/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options = options)
```  

#### [<a name="java"></a><span data-ttu-id="d6ec1-178">Java</span><span class="sxs-lookup"><span data-stu-id="d6ec1-178">Java</span></span>](#tab/java/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.setBinary("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

EdgeDriver driver = new EdgeDriver(options);
```  

#### [<a name="javascript"></a><span data-ttu-id="d6ec1-179">JavaScript</span><span class="sxs-lookup"><span data-stu-id="d6ec1-179">JavaScript</span></span>](#tab/javascript/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <a name="customize-the-microsoft-edge-driver-service"></a><span data-ttu-id="d6ec1-180">Personnaliser le service Microsoft Edge pilotes</span><span class="sxs-lookup"><span data-stu-id="d6ec1-180">Customize the Microsoft Edge Driver Service</span></span>  

#### [<a name="c"></a><span data-ttu-id="d6ec1-181">C#</span><span class="sxs-lookup"><span data-stu-id="d6ec1-181">C#</span></span>](#tab/c-sharp/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="d6ec1-182">Lorsque vous utilisez la classe pour créer une instance de classe, elle crée et lance la classe appropriée pour `EdgeOptions` `EdgeDriver` Microsoft Edge `EdgeDriverService` \(EdgeHTML\) ou Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="d6ec1-182">When you use the `EdgeOptions` class to create an `EdgeDriver` class instance, it creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="d6ec1-183">Si vous souhaitez créer un , utilisez la méthode pour en créer une configurée `EdgeDriverService` `CreateChromiumService()` pour Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="d6ec1-183">If you want to create an `EdgeDriverService`, use the `CreateChromiumService()` method to create one configured for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="d6ec1-184">La `CreateChromiumService()` méthode est utile lorsque vous devez ajouter des personnalisations.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-184">The `CreateChromiumService()` method is useful when you need to add customizations.</span></span>  <span data-ttu-id="d6ec1-185">Par exemple, le code suivant démarre une sortie détaillée du journal.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-185">For example, the following code starts verbose log output.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
><span data-ttu-id="d6ec1-186">Vous n’avez pas besoin de fournir `EdgeOptions` l’objet lorsque vous passez `EdgeDriverService` à `EdgeDriver` l’instance.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-186">You do not need to provide the `EdgeOptions` object when you pass `EdgeDriverService` to the `EdgeDriver` instance.</span></span>  <span data-ttu-id="d6ec1-187">La classe utilise les options par défaut pour `EdgeDriver` Microsoft Edge \(EdgeHTML\) ou Microsoft Edge \(Chromium\) en fonction du service que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-187">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) based on the service you provide.</span></span>  
> <span data-ttu-id="d6ec1-188">Toutefois, si vous souhaitez fournir les deux classes, assurez-vous que les deux sont configurées pour la même version de `EdgeDriverService` `EdgeOptions` Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-188">However, if you want to provide both `EdgeDriverService` and `EdgeOptions` classes, ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="d6ec1-189">Par exemple, vous pouvez utiliser une classe Microsoft Edge \(EdgeHTML\) et Chromium `EdgeDriverService` propriétés dans la `EdgeOptions` classe.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-189">For example, you may use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="d6ec1-190">La `EdgeDriver` classe envoie une erreur pour empêcher l’utilisation de différentes versions.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-190">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<a name="python"></a><span data-ttu-id="d6ec1-191">Python</span><span class="sxs-lookup"><span data-stu-id="d6ec1-191">Python</span></span>](#tab/python/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="d6ec1-192">Lorsque vous utilisez Python, `Edge` l’objet crée et gère le `EdgeService` .</span><span class="sxs-lookup"><span data-stu-id="d6ec1-192">When you use Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="d6ec1-193">Pour configurer l’objet, passez des arguments supplémentaires à l’objet, comme `EdgeService` indiqué dans le code `Edge` suivant.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-193">To configure the `EdgeService`, pass extra arguments to the `Edge` object as indicated in the following code.</span></span>  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<a name="java"></a><span data-ttu-id="d6ec1-194">Java</span><span class="sxs-lookup"><span data-stu-id="d6ec1-194">Java</span></span>](#tab/java/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="d6ec1-195">Utilisez la méthode pour créer un Microsoft Edge `createDefaultService()` `EdgeDriverService` \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="d6ec1-195">Use the `createDefaultService()` method to create an `EdgeDriverService` configured for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="d6ec1-196">Utilisez Java système pour personnaliser les services de pilotes dans Java.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-196">Use Java system properties to customize driver services in Java.</span></span>  <span data-ttu-id="d6ec1-197">Par exemple, le code suivant utilise la `"webdriver.edge.verboseLogging"` propriété pour activer la sortie détaillée du journal.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-197">For example, the following code uses the `"webdriver.edge.verboseLogging"` property to turn on verbose log output.</span></span>  

```java
System.setProperty("webdriver.edge.verboseLogging", "true");
EdgeDriverService service = EdgeDriverService.createDefaultService();
EdgeOptions options = new EdgeOptions();
EdgeDriver driver = new EdgeDriver(service, options);
```  

#### [<a name="javascript"></a><span data-ttu-id="d6ec1-198">JavaScript</span><span class="sxs-lookup"><span data-stu-id="d6ec1-198">JavaScript</span></span>](#tab/javascript/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="d6ec1-199">Lorsque vous utilisez JavaScript, créez et configurez un avec `Service` la `ServiceBuilder` classe.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-199">When you use JavaScript, create and configure a `Service` with the `ServiceBuilder` class.</span></span>  <span data-ttu-id="d6ec1-200">Si vous le souhaitez, vous pouvez transmettre l’objet à l’objet, qui `Service` `Driver` démarre \(et arrête\) le service pour vous.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-200">Optionally, you can pass the `Service` object to the `Driver` object, which starts \(and stops\) the service for you.</span></span>  
<span data-ttu-id="d6ec1-201">Pour configurer la `Service` méthode , exécutez une autre méthode dans la `ServiceBuilder` classe avant d’utiliser la `build()` méthode.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-201">To configure the `Service`, run another method in the `ServiceBuilder` class before you use the `build()` method.</span></span>  <span data-ttu-id="d6ec1-202">Passez ensuite le `service` paramètre en tant que paramètre dans la `Driver.createSession()` méthode.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-202">Then pass the `service` as a parameter in the `Driver.createSession()` method.</span></span>  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### <a name="use-chromium-specific-options"></a><span data-ttu-id="d6ec1-203">Utiliser les Chromium-Specific options</span><span class="sxs-lookup"><span data-stu-id="d6ec1-203">Use Chromium-Specific Options</span></span>  

<span data-ttu-id="d6ec1-204">Si vous définissez la propriété sur , vous pouvez utiliser la classe pour accéder aux mêmes propriétés et méthodes propres à Chromium que lorsque vous automatisez d’autres Chromium `UseChromium` `true` `EdgeOptions` navigateurs. [][WebdriverCapabilitiesEdgeOptions]</span><span class="sxs-lookup"><span data-stu-id="d6ec1-204">If you set the `UseChromium` property to `true`, you can use the `EdgeOptions` class to access the same [Chromium-specific properties and methods][WebdriverCapabilitiesEdgeOptions] that are used when you automate other Chromium browsers.</span></span>  

#### [<a name="c"></a><span data-ttu-id="d6ec1-205">C#</span><span class="sxs-lookup"><span data-stu-id="d6ec1-205">C#</span></span>](#tab/c-sharp/)  

<a id="use-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<a name="python"></a><span data-ttu-id="d6ec1-206">Python</span><span class="sxs-lookup"><span data-stu-id="d6ec1-206">Python</span></span>](#tab/python/)  

<a id="use-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<a name="java"></a><span data-ttu-id="d6ec1-207">Java</span><span class="sxs-lookup"><span data-stu-id="d6ec1-207">Java</span></span>](#tab/java/)  

<a id="use-chromium-specific-options-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

#### [<a name="javascript"></a><span data-ttu-id="d6ec1-208">JavaScript</span><span class="sxs-lookup"><span data-stu-id="d6ec1-208">JavaScript</span></span>](#tab/javascript/)  

<a id="use-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

* * *  

> [!NOTE]
> <span data-ttu-id="d6ec1-209">Si la propriété est définie sur , vous ne pouvez pas utiliser les propriétés et méthodes `UseChromium` `true` pour Microsoft Edge \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="d6ec1-209">If the `UseChromium` property is set to `true`, you are not able to use properties and methods for Microsoft Edge \(EdgeHTML\).</span></span>  

## <a name="other-webdriver-installation-options"></a><span data-ttu-id="d6ec1-210">Autres options d’installation webDriver</span><span class="sxs-lookup"><span data-stu-id="d6ec1-210">Other WebDriver installation options</span></span>  

### <a name="docker"></a><span data-ttu-id="d6ec1-211">Docker</span><span class="sxs-lookup"><span data-stu-id="d6ec1-211">Docker</span></span>  

<span data-ttu-id="d6ec1-212">Si vous utilisez [Docker,][DockerHub]exécutez la commande suivante pour télécharger une image pré-configurée avec Microsoft Edge \(Chromium\) et [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] préinstallé.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-212">If you use [Docker][DockerHub], run the following command to download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] pre-installed.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="d6ec1-213">Pour plus d’informations, accédez au [conteneur msedgedriver sur Docker Hub.][DockerHubMsedgedriver]</span><span class="sxs-lookup"><span data-stu-id="d6ec1-213">For more information, navigate to the [msedgedriver container on Docker Hub][DockerHubMsedgedriver].</span></span>  

## <a name="next-steps"></a><span data-ttu-id="d6ec1-214">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="d6ec1-214">Next steps</span></span>  

<span data-ttu-id="d6ec1-215">Pour plus d’informations sur WebDriver et sur la façon d’écrire des tests WebDriver automatisés à l’aide de Selenium, accédez à la [documentation selenium.][SeleniumDocumentation]</span><span class="sxs-lookup"><span data-stu-id="d6ec1-215">For more information about WebDriver and how to write automated WebDriver tests using Selenium, navigate to the [Selenium documentation][SeleniumDocumentation].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="d6ec1-216">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="d6ec1-216">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="d6ec1-217">L Microsoft Edge de l’équipe est enthousiaste à l’écoute de vos commentaires sur l’utilisation de WebDriver, selenium et Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-217">The Microsoft Edge team is eager to hear your feedback about using WebDriver, Selenium, and Microsoft Edge.</span></span>  <span data-ttu-id="d6ec1-218">Pour envoyer à l’équipe vos \*\*\*\* questions et [commentaires,][TwitterTweetEdgeDevTools]sélectionnez l’icône Envoyer des commentaires dans le Microsoft Edge DevTools ou envoyez un tweet @EdgeDevTools .</span><span class="sxs-lookup"><span data-stu-id="d6ec1-218">To send the team your questions and comments, choose the **Send Feedback** icon in the Microsoft Edge DevTools or send a tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="L’icône Envoyer des commentaires dans Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="d6ec1-220">Icône **Envoyer des commentaires** dans le Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="d6ec1-220">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- links -->  

[DevtoolsIndex]: ../devtools-guide-chromium/index.md "Microsoft Edge outils de développement (Chromium) | Documents Microsoft"  
[WebdriverCapabilitiesEdgeOptions]: ./capabilities-edge-options.md "Fonctionnalités et fonctionnalités EdgeOptions | Documents Microsoft"  

<!--[Webdriver]: /archive/microsoft-edge/legacy/developer/webdriver/index "WebDriver (EdgeHTML) | Microsoft Docs"  -->  

[DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability - Microsoft Edge - Stratégies | Documents Microsoft"  

[DockerHub]: https://hub.docker.com "Docker Hub"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Hub Docker"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "microsoft/edge-selenium-tools | GitHub"  
[GithubMicrosoftEdgeSeleniumToolsReleases]: https://github.com/microsoft/edge-selenium-tools/releases "microsoft/edge-selenium-tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SeleniumHQ/selenium | GitHub"  

[JavaScriptnpm]: https://www.npmjs.com/ "npm"  
[JavaScriptSeleniumTools]: https://www.npmjs.com/package/@microsoft/edge-selenium-tools "@microsoft/edge-selenium-tools | npm"  
[JavaScriptSelenium]: https://www.npmjs.com/package/selenium-webdriver "selenium-webdriver | npm"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "Microsoft Edge Pilote | Microsoft Edge Développeur"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Télécharger le nouveau Microsoft Edge navigateur"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  

[NugetCLI]:https://www.nuget.org/packages/NuGet.CommandLine/ "NuGet. CommandLine | NuGet Galerie"  
[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft.Edge.SeleniumTools | NuGet Galerie"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Selenium.WebDriver 3.141.0 | NuGet Galerie"  
[NugetPackagesSeleniumWebdriver400beta02]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-beta2 "Selenium.WebDriver 4.0.0-beta2 | NuGet Galerie"  

[PythonPip]: https://pypi.org/project/pip/ "pip | PyPI"  
[PythonSeleniumTools]: https://pypi.org/project/msedge-selenium-tools/ "Msedge-selenium-tools | PyPI"  
[PythonSelenium]: https://pypi.org/project/selenium/ "selenium | PyPI"

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDocumentation]: https://www.selenium.dev/documentation "Le système d’automatisation du navigateur Selenium Project | Documentation pour Selenium"  
[SeleniumDownloads]: https://selenium.dev/downloads "Téléchargements | Selenium"  
[SeleniumInstallingLibraries]: https://www.selenium.dev/documentation/en/selenium_installation/installing_selenium_libraries "Installation des bibliothèques Selenium | Selenium"

[SonatypeMavenRepositorySearch]: https://search.maven.org/artifact/com.microsoft.edge/msedge-selenium-tools-java/3.141.0/jar "sonatype Maven Central Repository Search | com.microsoft.edge:msedge-selenium-tools-java"

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publier un tweet"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver | W3C"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Navigateur sans | Wikipedia"  
