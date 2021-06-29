---
description: Découvrez comment tester votre site web ou votre application dans Microsoft Edge ou automatiser le navigateur avec WebDriver
title: Utiliser WebDriver (Chromium) pour tester l’automatisation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/24/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, développement web, html, css, javascript, développeur, webdriver, selenium, test, outils, automatisation, test
ms.openlocfilehash: a1ec308fc1412ead27c4776ce0ccc2e873376652
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624674"
---
# <a name="use-webdriver-chromium-for-test-automation"></a><span data-ttu-id="162ce-104">Utiliser WebDriver (Chromium) pour tester l’automatisation</span><span class="sxs-lookup"><span data-stu-id="162ce-104">Use WebDriver (Chromium) for test automation</span></span>  

<span data-ttu-id="162ce-105">WebDriver permet aux développeurs de créer des tests automatisés qui simulent l’interaction utilisateur.</span><span class="sxs-lookup"><span data-stu-id="162ce-105">WebDriver allows developers to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="162ce-106">Les tests et simulations WebDriver diffèrent des tests unitaires JavaScript des manières suivantes.</span><span class="sxs-lookup"><span data-stu-id="162ce-106">WebDriver tests and simulations differ from JavaScript unit tests in the following ways.</span></span>  

*   <span data-ttu-id="162ce-107">Accède aux fonctionnalités et informations non disponibles pour JavaScript en cours d’exécution dans les navigateurs.</span><span class="sxs-lookup"><span data-stu-id="162ce-107">Accesses functionality and information not available to JavaScript running in browsers.</span></span>  
*   <span data-ttu-id="162ce-108">Simule les événements utilisateur ou au niveau du système d’exploitation plus précisément.</span><span class="sxs-lookup"><span data-stu-id="162ce-108">Simulates user events or OS-level events more accurately.</span></span>  
*   <span data-ttu-id="162ce-109">Gère plusieurs fenêtres, onglets et pages web en une seule session de test.</span><span class="sxs-lookup"><span data-stu-id="162ce-109">Manages multiple windows, tabs, and webpages in a single test session.</span></span>  
*   <span data-ttu-id="162ce-110">Exécute plusieurs sessions de Microsoft Edge sur un ordinateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="162ce-110">Runs multiple sessions of Microsoft Edge on a specific machine.</span></span>  


## <a name="relationship-between-webdriver-and-other-software"></a><span data-ttu-id="162ce-111">Relation entre WebDriver et d’autres logiciels</span><span class="sxs-lookup"><span data-stu-id="162ce-111">Relationship between WebDriver and other software</span></span>

<span data-ttu-id="162ce-112">Pour automatiser Microsoft Edge webdriver pour simuler l’interaction utilisateur, vous avez besoin de trois composants :</span><span class="sxs-lookup"><span data-stu-id="162ce-112">To automate Microsoft Edge with WebDriver to simulate user interaction, you need three components:</span></span>

*  <span data-ttu-id="162ce-113">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="162ce-113">Microsoft Edge</span></span>
*  <span data-ttu-id="162ce-114">Microsoft Edge Driver</span><span class="sxs-lookup"><span data-stu-id="162ce-114">Microsoft Edge Driver</span></span>
*  <span data-ttu-id="162ce-115">Infrastructure de test WebDriver</span><span class="sxs-lookup"><span data-stu-id="162ce-115">A WebDriver testing framework</span></span>

<span data-ttu-id="162ce-116">La relation fonctionnelle entre ces composants est la suivante.</span><span class="sxs-lookup"><span data-stu-id="162ce-116">The functional relationship between these components is as follows.</span></span>

| <span data-ttu-id="162ce-117">Technologie</span><span class="sxs-lookup"><span data-stu-id="162ce-117">Technology</span></span> | <span data-ttu-id="162ce-118">Rôle</span><span class="sxs-lookup"><span data-stu-id="162ce-118">Role</span></span> |
|---|---|
| <span data-ttu-id="162ce-119">WebDriver</span><span class="sxs-lookup"><span data-stu-id="162ce-119">WebDriver</span></span> | <span data-ttu-id="162ce-120">Norme W3C pour un protocole de câblage de plateforme et linguistiquement neutre.</span><span class="sxs-lookup"><span data-stu-id="162ce-120">A W3C standard for a platform- and language-neutral wire protocol.</span></span>  <span data-ttu-id="162ce-121">Ce protocole permet aux programmes hors processus d’indiquer à distance le comportement des navigateurs web.</span><span class="sxs-lookup"><span data-stu-id="162ce-121">This protocol allows out-of-process programs to remotely instruct the behavior of web browsers.</span></span> |
| <span data-ttu-id="162ce-122">Microsoft Edge Driver</span><span class="sxs-lookup"><span data-stu-id="162ce-122">Microsoft Edge Driver</span></span> | <span data-ttu-id="162ce-123">Implémentation de Microsoft du protocole WebDriver spécifiquement pour Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="162ce-123">Microsoft's implementation of the WebDriver protocol specifically for Microsoft Edge.</span></span>  <span data-ttu-id="162ce-124">Test authors write tests that use WebDriver commands that Microsoft Edge Driver receives.</span><span class="sxs-lookup"><span data-stu-id="162ce-124">Test authors write tests that use WebDriver commands that Microsoft Edge Driver receives.</span></span>  <span data-ttu-id="162ce-125">Microsoft Edge Le pilote est alors chargé de communiquer cette commande au navigateur.</span><span class="sxs-lookup"><span data-stu-id="162ce-125">Microsoft Edge Driver is then responsible for communicating that command to the browser.</span></span> |
| <span data-ttu-id="162ce-126">Infrastructure de test WebDriver</span><span class="sxs-lookup"><span data-stu-id="162ce-126">A WebDriver testing framework</span></span> | <span data-ttu-id="162ce-127">Les auteurs de tests utilisent une infrastructure de test pour écrire des tests de bout en bout et automatiser les navigateurs.</span><span class="sxs-lookup"><span data-stu-id="162ce-127">Test authors use a testing framework to write end-to-end tests and automate browsers.</span></span>  <span data-ttu-id="162ce-128">Fournit une interface spécifique à la langue qui traduit votre code en commandes qui Microsoft Edge Pilote s’exécute dans Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="162ce-128">Provides a language-specific interface that translates your code into commands that Microsoft Edge Driver runs in Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="162ce-129">Des frameworks de test WebDriver existent pour toutes les principales plateformes et langues.</span><span class="sxs-lookup"><span data-stu-id="162ce-129">WebDriver testing frameworks exist for all major platforms and languages.</span></span>  <span data-ttu-id="162ce-130">L’une de ces infrastructure est Selenium.</span><span class="sxs-lookup"><span data-stu-id="162ce-130">One such framework is Selenium.</span></span> |
| <span data-ttu-id="162ce-131">Pilote Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="162ce-131">Internet Explorer Driver</span></span> | <span data-ttu-id="162ce-132">Implémentation du protocole WebDriver spécifiquement pour Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="162ce-132">An implementation of the WebDriver protocol specifically for Internet Explorer.</span></span>  <span data-ttu-id="162ce-133">Pour exécuter des tests de bout en bout hérités pour Internet Explorer, nous vous recommandons d’utiliser pilote Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="162ce-133">To run legacy end-to-end tests for Internet Explorer, we recommend using Internet Explorer Driver.</span></span> |

<span data-ttu-id="162ce-134">Les sections suivantes décrivent comment commencer avec WebDriver pour Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="162ce-134">The following sections describe how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  


## <a name="install-microsoft-edge-chromium"></a><span data-ttu-id="162ce-135">Installer Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="162ce-135">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="162ce-136">Veillez à installer [Microsoft Edge (Chromium)][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="162ce-136">Ensure you install [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="162ce-137">Pour confirmer que vous avez installé Microsoft Edge \(Chromium\), accédez à et vérifiez que le numéro de version est `edge://settings/help` 75 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="162ce-137">To confirm that you have Microsoft Edge \(Chromium\) installed, navigate to `edge://settings/help`, and verify that the version number is 75 or later.</span></span>


## <a name="download-microsoft-edge-driver"></a><span data-ttu-id="162ce-138">Télécharger Microsoft Edge Driver</span><span class="sxs-lookup"><span data-stu-id="162ce-138">Download Microsoft Edge Driver</span></span>

<span data-ttu-id="162ce-139">Pour commencer à automatiser les tests, utilisez les étapes suivantes pour vous assurer que la version WebDriver que vous installez correspond à la version de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="162ce-139">To begin automating tests, use the following steps to ensure that the WebDriver version you install matches your browser version.</span></span>  

1.  <span data-ttu-id="162ce-140">Recherchez votre version de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="162ce-140">Find your version of Microsoft Edge.</span></span>  
    1.  <span data-ttu-id="162ce-141">Naviguez vers`edge://settings/help` .</span><span class="sxs-lookup"><span data-stu-id="162ce-141">Navigate to `edge://settings/help`.</span></span>  
        
        :::image type="complex" source="./media/microsoft-edge-version.msft.png" alt-text="Numéro de build Microsoft Edge le 15 avril 2021" lightbox="./media/microsoft-edge-version.msft.png":::
           <span data-ttu-id="162ce-143">Numéro de build Microsoft Edge le 15 avril 2021</span><span class="sxs-lookup"><span data-stu-id="162ce-143">The build number for Microsoft Edge on April 15, 2021</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="162ce-144">Accédez à [Microsoft Edge pilote .][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="162ce-144">Navigate to [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].</span></span>  
1.  <span data-ttu-id="162ce-145">Accédez à **Obtenir la dernière version.**</span><span class="sxs-lookup"><span data-stu-id="162ce-145">Navigate to **Get the latest version**.</span></span>  
1.  <span data-ttu-id="162ce-146">Choisissez la version du canal qui correspond à votre numéro de version de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="162ce-146">Choose the build of channel that matches your version number of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="./media/microsoft-edge-driver-install.msft.png" alt-text="Section Obtenir la dernière version de la page web Microsoft Edge Driver" lightbox="./media/microsoft-edge-driver-install.msft.png":::
       <span data-ttu-id="162ce-148">Section **Obtenir la dernière version** sur la page web Microsoft Edge [pilote][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="162ce-148">The **Get the latest version** section on the [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] webpage</span></span>  
    :::image-end:::  
   
    
## <a name="choose-a-webdriver-testing-framework"></a><span data-ttu-id="162ce-149">Choisir une infrastructure de test WebDriver</span><span class="sxs-lookup"><span data-stu-id="162ce-149">Choose a WebDriver testing framework</span></span>

<span data-ttu-id="162ce-150">Après avoir téléchargé Microsoft Edge pilote, le dernier composant que vous devez télécharger est une infrastructure de test WebDriver.</span><span class="sxs-lookup"><span data-stu-id="162ce-150">After downloading Microsoft Edge Driver, the last component you must download is a WebDriver testing framework.</span></span> <span data-ttu-id="162ce-151">Les auteurs de tests utilisent les frameworks de test WebDriver pour écrire des tests de bout en bout et automatiser les navigateurs.</span><span class="sxs-lookup"><span data-stu-id="162ce-151">Test authors use WebDriver testing frameworks to write end-to-end tests and automate browsers.</span></span> <span data-ttu-id="162ce-152">L’infrastructure fournit une interface spécifique au langage qui traduit votre code (tel que Python, Java, C#, Ruby ou JavaScript) en commandes que Microsoft Edge Driver exécute dans Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="162ce-152">The framework provides a language-specific interface that translates your code (such as Python, Java, C#, Ruby, or JavaScript) into commands that Microsoft Edge Driver runs in Microsoft Edge \(Chromium\).</span></span> <span data-ttu-id="162ce-153">Des frameworks de test WebDriver existent pour toutes les principales plateformes et langues.</span><span class="sxs-lookup"><span data-stu-id="162ce-153">WebDriver testing frameworks exist for all major platforms and languages.</span></span>


<span data-ttu-id="162ce-154">Cet article fournit des instructions sur l’utilisation de l’infrastructure Selenium, mais vous pouvez utiliser n’importe quelle bibliothèque, infrastructure et langage de programmation qui prend en charge WebDriver.</span><span class="sxs-lookup"><span data-stu-id="162ce-154">This article provides instructions for using the Selenium framework, but you can use any library, framework, and programming language that supports WebDriver.</span></span>  <span data-ttu-id="162ce-155">Pour accomplir les mêmes tâches à l’aide d’une infrastructure de test WebDriver autre que Selenium, consultez la documentation officielle de votre choix.</span><span class="sxs-lookup"><span data-stu-id="162ce-155">To accomplish the same tasks using a WebDriver testing framework other than Selenium, consult the official documentation for your framework of choice.</span></span>

<span data-ttu-id="162ce-156">Si vous utilisez Selenium, l’équipe Microsoft Edge recommande [Selenium 4.0.0-beta2][NugetPackagesSeleniumWebdriver400beta02] ou version ultérieure, car cette version de Selenium prend en charge Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="162ce-156">If you are using Selenium, the Microsoft Edge team recommends [Selenium 4.0.0-beta2][NugetPackagesSeleniumWebdriver400beta02] or later, because that version of Selenium supports Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="162ce-157">Toutefois, vous pouvez contrôler Microsoft Edge \(Chromium\) dans toutes les versions antérieures de Selenium, y compris la version stable actuelle de Selenium 3.</span><span class="sxs-lookup"><span data-stu-id="162ce-157">However, you can control Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="162ce-158">Si vous avez précédemment automatisé ou testé Microsoft Edge \(Chromium\) et des classes, votre code WebDriver ne s’exécute pas sur Microsoft Edge `ChromeDriver` `ChromeOptions` version 80 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="162ce-158">If you previously automated or tested Microsoft Edge \(Chromium\) using `ChromeDriver` and `ChromeOptions` classes, your WebDriver code does not run on Microsoft Edge Version 80 or later.</span></span>  <span data-ttu-id="162ce-159">Pour résoudre le problème, mettez à jour vos tests pour utiliser la classe et `EdgeOptions` téléchargez [Microsoft Edge pilote][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].</span><span class="sxs-lookup"><span data-stu-id="162ce-159">To solve the problem, update your tests to use the `EdgeOptions` class and download [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].</span></span>  

### <a name="using-selenium-4"></a><span data-ttu-id="162ce-160">Utilisation de Selenium 4</span><span class="sxs-lookup"><span data-stu-id="162ce-160">Using Selenium 4</span></span>

<span data-ttu-id="162ce-161">L’infrastructure de test Selenium WebDriver peut être utilisée sur n’importe quelle plateforme et est disponible pour Java, Python, C#, Ruby et JavaScript.</span><span class="sxs-lookup"><span data-stu-id="162ce-161">The Selenium WebDriver testing framework can be used on any platform, and is available for Java, Python, C#, Ruby, and JavaScript.</span></span>

<span data-ttu-id="162ce-162">Selenium 4 dispose d’une prise en charge intégrée des Microsoft Edge (Chromium).</span><span class="sxs-lookup"><span data-stu-id="162ce-162">Selenium 4 has built-in support for Microsoft Edge (Chromium).</span></span>  <span data-ttu-id="162ce-163">Pour installer Selenium 4, accédez à [l’installation des bibliothèques Selenium.][SeleniumInstallingLibraries]</span><span class="sxs-lookup"><span data-stu-id="162ce-163">To install Selenium 4, navigate to [Installing Selenium libraries][SeleniumInstallingLibraries].</span></span>

<span data-ttu-id="162ce-164">Si vous utilisez Selenium 4, vous n’avez pas besoin d’utiliser les outils Selenium pour Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="162ce-164">If you use Selenium 4, you don't need to use Selenium Tools for Microsoft Edge.</span></span>  <span data-ttu-id="162ce-165">Les outils Selenium pour Microsoft Edge uniquement pour le selenium 3.</span><span class="sxs-lookup"><span data-stu-id="162ce-165">Selenium Tools for Microsoft Edge are for Selenium 3 only.</span></span>  <span data-ttu-id="162ce-166">Si vous essayez d’utiliser Selenium 4 avec les outils Selenium pour Microsoft Edge et que vous essayez de créer une instance, vous obtenez `EdgeDriver` l’erreur suivante : `System.MissingMethodException: 'Method not found: 'OpenQA.Selenium.Remote.DesiredCapabilities OpenQA.Selenium.DriverOptions.GenerateDesiredCapabilities(Boolean)'`</span><span class="sxs-lookup"><span data-stu-id="162ce-166">If you try to use Selenium 4 with Selenium Tools for Microsoft Edge and try to create a new `EdgeDriver` instance, you get the following error: `System.MissingMethodException: 'Method not found: 'OpenQA.Selenium.Remote.DesiredCapabilities OpenQA.Selenium.DriverOptions.GenerateDesiredCapabilities(Boolean)'`.</span></span>  

<span data-ttu-id="162ce-167">Si vous utilisez Selenium 4 et obtenez cette erreur, supprimez votre projet et assurez-vous que vous utilisez l’officiel et les classes de `Microsoft.Edge.SeleniumTools` l’espace `EdgeOptions` `EdgeDriver` de `OpenQA.Selenium.Edge` noms.</span><span class="sxs-lookup"><span data-stu-id="162ce-167">If you're using Selenium 4 and get this error, remove `Microsoft.Edge.SeleniumTools` from your project, and make sure you're using the official `EdgeOptions` and `EdgeDriver` classes from the `OpenQA.Selenium.Edge` namespace.</span></span>

### <a name="using-selenium-3"></a><span data-ttu-id="162ce-168">Utilisation de Selenium 3</span><span class="sxs-lookup"><span data-stu-id="162ce-168">Using Selenium 3</span></span>  

<span data-ttu-id="162ce-169">Si vous utilisez déjà [Selenium 3,][|::ref1::|]vous avez peut-être des tests de navigateur existants et souhaitez ajouter une couverture pour Microsoft Edge \(Chromium\) sans modifier votre version de Selenium.</span><span class="sxs-lookup"><span data-stu-id="162ce-169">If you already use [Selenium 3][|::ref1::|], you may have existing browser tests and want to add coverage for Microsoft Edge \(Chromium\) without changing your version of Selenium.</span></span>  <span data-ttu-id="162ce-170">Pour utiliser [Selenium 3][|::ref2::|] afin d’écrire des tests automatisés pour Microsoft Edge \(EdgeHTML\) et Microsoft Edge \(Chromium\), installez le package [Outils Selenium][GithubMicrosoftEdgeSeleniumTools] pour Microsoft Edge pour utiliser le pilote mis à jour.</span><span class="sxs-lookup"><span data-stu-id="162ce-170">To use [Selenium 3][|::ref2::|] to write automated tests for both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package to use the updated driver.</span></span>  <span data-ttu-id="162ce-171">Les classes incluses dans les outils sont entièrement compatibles avec les `EdgeDriver` `EdgeDriverService` équivalents intégrés dans Selenium 4.</span><span class="sxs-lookup"><span data-stu-id="162ce-171">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium 4.</span></span>  

<span data-ttu-id="162ce-172">Si vous utilisez Selenium 3, utilisez les étapes suivantes pour ajouter les outils [Selenium][GithubMicrosoftEdgeSeleniumTools] pour Microsoft Edge et [Selenium 3][|::ref3::|] à votre projet.</span><span class="sxs-lookup"><span data-stu-id="162ce-172">If you are using Selenium 3, use the following steps to add the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] and [Selenium 3][|::ref3::|] to your project.</span></span>

#### [<a name="c"></a><span data-ttu-id="162ce-173">C#</span><span class="sxs-lookup"><span data-stu-id="162ce-173">C#</span></span>](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="162ce-174">Ajoutez [les packages Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] et [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] à votre projet .NET à l’aide NuGet [CLI][NugetCLI] ou [Visual Studio][VisualStudio].</span><span class="sxs-lookup"><span data-stu-id="162ce-174">Add the [Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] and [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] packages to your .NET project using the [NuGet CLI][NugetCLI] or [Visual Studio][VisualStudio].</span></span>  

#### [<a name="python"></a><span data-ttu-id="162ce-175">Python</span><span class="sxs-lookup"><span data-stu-id="162ce-175">Python</span></span>](#tab/python/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="162ce-176">Utilisez [pip][PythonPip] pour installer [les packages msedge-selenium-tools][PythonSeleniumTools] et [selenium.][PythonSelenium]</span><span class="sxs-lookup"><span data-stu-id="162ce-176">Use [pip][PythonPip] to install the [msedge-selenium-tools][PythonSeleniumTools] and [selenium][PythonSelenium] packages.</span></span>  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [<a name="java"></a><span data-ttu-id="162ce-177">Java</span><span class="sxs-lookup"><span data-stu-id="162ce-177">Java</span></span>](#tab/java/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="162ce-178">Si votre Java utilise Maven, copiez et collez la dépendance suivante dans votre fichier pour ajouter `pom.xml` [msedge-selenium-tools-java][SonatypeMavenRepositorySearch].</span><span class="sxs-lookup"><span data-stu-id="162ce-178">If your Java project uses Maven, copy and paste the following dependency to your `pom.xml` file to add [msedge-selenium-tools-java][SonatypeMavenRepositorySearch].</span></span>  

```xml
<dependency>
    <groupId>com.microsoft.edge</groupId>
    <artifactId>msedge-selenium-tools-java</artifactId>
    <version>[3.141.0,)</version>
</dependency>
```  

<span data-ttu-id="162ce-179">Le package Java est également disponible en téléchargement direct sur la [page Outils Selenium Microsoft Edge releases.][GithubMicrosoftEdgeSeleniumToolsReleases]</span><span class="sxs-lookup"><span data-stu-id="162ce-179">The Java package is also available to download directly on the [Selenium Tools for Microsoft Edge Releases page][GithubMicrosoftEdgeSeleniumToolsReleases].</span></span>  

#### [<a name="javascript"></a><span data-ttu-id="162ce-180">JavaScript</span><span class="sxs-lookup"><span data-stu-id="162ce-180">JavaScript</span></span>](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="162ce-181">Utilisez [npm][JavaScript|::ref4::|] pour installer [les packages edge-selenium-tools][JavaScriptSeleniumTools] et [selenium-webdriver.][JavaScriptSelenium]</span><span class="sxs-lookup"><span data-stu-id="162ce-181">Use [npm][JavaScript|::ref4::|] to install the [edge-selenium-tools][JavaScriptSeleniumTools] and [selenium-webdriver][JavaScriptSelenium] packages.</span></span>  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  


## <a name="automate-microsoft-edge-chromium-with-webdriver"></a><span data-ttu-id="162ce-182">Automatiser Microsoft Edge (Chromium) avec WebDriver</span><span class="sxs-lookup"><span data-stu-id="162ce-182">Automate Microsoft Edge (Chromium) with WebDriver</span></span>  

<span data-ttu-id="162ce-183">Pour automatiser un navigateur à l’aide de WebDriver, vous devez d’abord démarrer une session WebDriver à l’aide de votre infrastructure de test WebDriver préférée.</span><span class="sxs-lookup"><span data-stu-id="162ce-183">To automate a browser using WebDriver, you must first start a WebDriver session using your preferred WebDriver testing framework.</span></span>  <span data-ttu-id="162ce-184">Une session est une instance en cours d’exécution unique d’un navigateur contrôlée à l’aide des commandes WebDriver.</span><span class="sxs-lookup"><span data-stu-id="162ce-184">A session is a single running instance of a browser controlled using WebDriver commands.</span></span>  <span data-ttu-id="162ce-185">Démarrez une session WebDriver pour lancer une nouvelle instance de navigateur.</span><span class="sxs-lookup"><span data-stu-id="162ce-185">Start a WebDriver session to launch a new browser instance.</span></span>  <span data-ttu-id="162ce-186">L’instance de navigateur lancée reste ouverte jusqu’à la fermeture de la session WebDriver.</span><span class="sxs-lookup"><span data-stu-id="162ce-186">The launched browser instance remains open until you close the WebDriver session.</span></span>  

<span data-ttu-id="162ce-187">Le contenu suivant vous aide à utiliser Selenium pour démarrer une session WebDriver avec Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="162ce-187">The following content walks you through using Selenium to start a WebDriver session with Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="162ce-188">Vous pouvez exécuter ces exemples à l’aide de Selenium 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="162ce-188">You can run these examples using either Selenium 3 or 4.</span></span>  <span data-ttu-id="162ce-189">Pour utiliser WebDriver avec Selenium 3, le package [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package doit être installé.</span><span class="sxs-lookup"><span data-stu-id="162ce-189">To use WebDriver with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package must be installed.</span></span>  

> [!NOTE]
> <span data-ttu-id="162ce-190">Cet article fournit des instructions sur l’utilisation de l’infrastructure Selenium, mais vous pouvez utiliser n’importe quelle bibliothèque, infrastructure et langage de programmation qui prend en charge WebDriver.</span><span class="sxs-lookup"><span data-stu-id="162ce-190">This article provides instructions for using the Selenium framework, but you can use any library, framework, and programming language that supports WebDriver.</span></span>  <span data-ttu-id="162ce-191">Pour accomplir les mêmes tâches à l’aide d’une autre infrastructure, consultez la documentation officielle de votre choix.</span><span class="sxs-lookup"><span data-stu-id="162ce-191">To accomplish the same tasks using another framework, consult the official documentation for your framework of choice.</span></span>

### <a name="automate-microsoft-edge-chromium"></a><span data-ttu-id="162ce-192">Automatiser Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="162ce-192">Automate Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="162ce-193">Selenium utilise la `EdgeDriver` classe pour gérer une session Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="162ce-193">Selenium uses the `EdgeDriver` class to manage a Microsoft Edge \(Chromium\) session.</span></span>  <span data-ttu-id="162ce-194">Pour démarrer une session et automatiser Microsoft Edge \(Chromium\), créez un objet et passez-lui un objet avec la propriété `EdgeDriver` `EdgeOptions` définie sur `UseChromium` `true` .</span><span class="sxs-lookup"><span data-stu-id="162ce-194">To start a session and automate Microsoft Edge \(Chromium\), create a new `EdgeDriver` object and pass it an `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<a name="c"></a><span data-ttu-id="162ce-195">C#</span><span class="sxs-lookup"><span data-stu-id="162ce-195">C#</span></span>](#tab/c-sharp/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<a name="python"></a><span data-ttu-id="162ce-196">Python</span><span class="sxs-lookup"><span data-stu-id="162ce-196">Python</span></span>](#tab/python/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options = options)
```  

#### [<a name="java"></a><span data-ttu-id="162ce-197">Java</span><span class="sxs-lookup"><span data-stu-id="162ce-197">Java</span></span>](#tab/java/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

<span data-ttu-id="162ce-198">La classe prend uniquement en charge Microsoft Edge \(Chromium\) et ne prend pas en `EdgeDriver` charge Microsoft Edge \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="162ce-198">The `EdgeDriver` class only supports Microsoft Edge \(Chromium\), and doesn't support Microsoft Edge \(EdgeHTML\).</span></span>  <span data-ttu-id="162ce-199">Pour une utilisation de base, vous pouvez créer un `EdgeDriver` sans fournir `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="162ce-199">For basic usage, you can create an `EdgeDriver` without providing `EdgeOptions`.</span></span>  

```java
EdgeDriver driver = new EdgeDriver();
```  

#### [<a name="javascript"></a><span data-ttu-id="162ce-200">JavaScript</span><span class="sxs-lookup"><span data-stu-id="162ce-200">JavaScript</span></span>](#tab/javascript/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> <span data-ttu-id="162ce-201">Si votre administrateur informatique a définie la stratégie [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] sur , le pilote Microsoft Edge ne peut pas conduire Microsoft Edge \(Chromium\), car le pilote utilise Microsoft Edge `2` [DevTools][DevtoolsIndex]. [][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="162ce-201">If your IT admin has set the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy to `2`,  [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] is blocked from driving Microsoft Edge \(Chromium\), because the driver uses the [Microsoft Edge DevTools][DevtoolsIndex].</span></span>  <span data-ttu-id="162ce-202">[Assurez-vous que la stratégie DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] est définie sur ou pour automatiser Microsoft Edge `0` `1` (Chromium).</span><span class="sxs-lookup"><span data-stu-id="162ce-202">Ensure the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy is set to `0` or `1` to automate Microsoft Edge (Chromium).</span></span>  

### <a name="choose-specific-browser-binaries-chromium-only"></a><span data-ttu-id="162ce-203">Choisir des binaires de navigateur spécifiques (Chromium uniquement)</span><span class="sxs-lookup"><span data-stu-id="162ce-203">Choose Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="162ce-204">Vous pouvez démarrer une session WebDriver avec des Microsoft Edge \(Chromium\) spécifiques.</span><span class="sxs-lookup"><span data-stu-id="162ce-204">You can start a WebDriver session with specific Microsoft Edge \(Chromium\) binaries.</span></span>  <span data-ttu-id="162ce-205">Par exemple, vous pouvez exécuter des tests à [l’aide des canaux Microsoft Edge prévisualisation][MicrosoftedgeinsiderDownload] tels que Microsoft Edge Beta.</span><span class="sxs-lookup"><span data-stu-id="162ce-205">For example, you can run tests using the [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<a name="c"></a><span data-ttu-id="162ce-206">C#</span><span class="sxs-lookup"><span data-stu-id="162ce-206">C#</span></span>](#tab/c-sharp/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<a name="python"></a><span data-ttu-id="162ce-207">Python</span><span class="sxs-lookup"><span data-stu-id="162ce-207">Python</span></span>](#tab/python/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options = options)
```  

#### [<a name="java"></a><span data-ttu-id="162ce-208">Java</span><span class="sxs-lookup"><span data-stu-id="162ce-208">Java</span></span>](#tab/java/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.setBinary("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

EdgeDriver driver = new EdgeDriver(options);
```  

#### [<a name="javascript"></a><span data-ttu-id="162ce-209">JavaScript</span><span class="sxs-lookup"><span data-stu-id="162ce-209">JavaScript</span></span>](#tab/javascript/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <a name="customize-the-microsoft-edge-driver-service"></a><span data-ttu-id="162ce-210">Personnaliser le service Microsoft Edge pilotes de service</span><span class="sxs-lookup"><span data-stu-id="162ce-210">Customize the Microsoft Edge Driver Service</span></span>  

#### [<a name="c"></a><span data-ttu-id="162ce-211">C#</span><span class="sxs-lookup"><span data-stu-id="162ce-211">C#</span></span>](#tab/c-sharp/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="162ce-212">Lorsque vous utilisez la classe pour créer une instance de classe, elle crée et lance la classe appropriée pour `EdgeOptions` `EdgeDriver` Microsoft Edge `EdgeDriverService` \(EdgeHTML\) ou Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="162ce-212">When you use the `EdgeOptions` class to create an `EdgeDriver` class instance, it creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="162ce-213">Si vous souhaitez créer un , utilisez la méthode pour en créer une configurée `EdgeDriverService` `CreateChromiumService()` pour Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="162ce-213">If you want to create an `EdgeDriverService`, use the `CreateChromiumService()` method to create one configured for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="162ce-214">La `CreateChromiumService()` méthode est utile lorsque vous devez ajouter des personnalisations.</span><span class="sxs-lookup"><span data-stu-id="162ce-214">The `CreateChromiumService()` method is useful when you need to add customizations.</span></span>  <span data-ttu-id="162ce-215">Par exemple, le code suivant démarre une sortie détaillée du journal.</span><span class="sxs-lookup"><span data-stu-id="162ce-215">For example, the following code starts verbose log output.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
><span data-ttu-id="162ce-216">Vous n’avez pas besoin de fournir `EdgeOptions` l’objet lorsque vous passez `EdgeDriverService` à `EdgeDriver` l’instance.</span><span class="sxs-lookup"><span data-stu-id="162ce-216">You do not need to provide the `EdgeOptions` object when you pass `EdgeDriverService` to the `EdgeDriver` instance.</span></span>  <span data-ttu-id="162ce-217">La classe utilise les options par défaut pour `EdgeDriver` Microsoft Edge \(EdgeHTML\) ou Microsoft Edge \(Chromium\) en fonction du service que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="162ce-217">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) based on the service you provide.</span></span>  
> <span data-ttu-id="162ce-218">Toutefois, si vous souhaitez fournir à la fois et des classes, assurez-vous que les deux sont configurés pour la `EdgeDriverService` `EdgeOptions` même version de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="162ce-218">However, if you want to provide both `EdgeDriverService` and `EdgeOptions` classes, ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="162ce-219">Par exemple, vous pouvez utiliser une classe Microsoft Edge \(EdgeHTML\) et Chromium `EdgeDriverService` propriétés dans la `EdgeOptions` classe.</span><span class="sxs-lookup"><span data-stu-id="162ce-219">For example, you may use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="162ce-220">La `EdgeDriver` classe envoie une erreur pour empêcher l’utilisation de différentes versions.</span><span class="sxs-lookup"><span data-stu-id="162ce-220">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<a name="python"></a><span data-ttu-id="162ce-221">Python</span><span class="sxs-lookup"><span data-stu-id="162ce-221">Python</span></span>](#tab/python/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="162ce-222">Lorsque vous utilisez Python, `Edge` l’objet crée et gère le `EdgeService` .</span><span class="sxs-lookup"><span data-stu-id="162ce-222">When you use Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="162ce-223">Pour configurer l’objet, passez des arguments supplémentaires à l’objet, comme `EdgeService` indiqué dans le code `Edge` suivant.</span><span class="sxs-lookup"><span data-stu-id="162ce-223">To configure the `EdgeService`, pass extra arguments to the `Edge` object as indicated in the following code.</span></span>  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<a name="java"></a><span data-ttu-id="162ce-224">Java</span><span class="sxs-lookup"><span data-stu-id="162ce-224">Java</span></span>](#tab/java/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="162ce-225">Utilisez la méthode pour créer un Microsoft Edge `createDefaultService()` `EdgeDriverService` \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="162ce-225">Use the `createDefaultService()` method to create an `EdgeDriverService` configured for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="162ce-226">Utilisez Java système pour personnaliser les services de pilotes dans Java.</span><span class="sxs-lookup"><span data-stu-id="162ce-226">Use Java system properties to customize driver services in Java.</span></span>  <span data-ttu-id="162ce-227">Par exemple, le code suivant utilise la `"webdriver.edge.verboseLogging"` propriété pour activer la sortie détaillée du journal.</span><span class="sxs-lookup"><span data-stu-id="162ce-227">For example, the following code uses the `"webdriver.edge.verboseLogging"` property to turn on verbose log output.</span></span>  

```java
System.setProperty("webdriver.edge.verboseLogging", "true");
EdgeDriverService service = EdgeDriverService.createDefaultService();
EdgeOptions options = new EdgeOptions();
EdgeDriver driver = new EdgeDriver(service, options);
```  

#### [<a name="javascript"></a><span data-ttu-id="162ce-228">JavaScript</span><span class="sxs-lookup"><span data-stu-id="162ce-228">JavaScript</span></span>](#tab/javascript/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="162ce-229">Lorsque vous utilisez JavaScript, créez et configurez un avec `Service` la `ServiceBuilder` classe.</span><span class="sxs-lookup"><span data-stu-id="162ce-229">When you use JavaScript, create and configure a `Service` with the `ServiceBuilder` class.</span></span>  <span data-ttu-id="162ce-230">Si vous le souhaitez, vous pouvez transmettre l’objet à l’objet, qui `Service` `Driver` démarre \(et arrête\) le service pour vous.</span><span class="sxs-lookup"><span data-stu-id="162ce-230">Optionally, you can pass the `Service` object to the `Driver` object, which starts \(and stops\) the service for you.</span></span>  
<span data-ttu-id="162ce-231">Pour configurer la `Service` méthode , exécutez une autre méthode dans la `ServiceBuilder` classe avant d’utiliser la `build()` méthode.</span><span class="sxs-lookup"><span data-stu-id="162ce-231">To configure the `Service`, run another method in the `ServiceBuilder` class before you use the `build()` method.</span></span>  <span data-ttu-id="162ce-232">Passez ensuite le `service` paramètre en tant que paramètre dans la `Driver.createSession()` méthode.</span><span class="sxs-lookup"><span data-stu-id="162ce-232">Then pass the `service` as a parameter in the `Driver.createSession()` method.</span></span>  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### <a name="use-chromium-specific-options"></a><span data-ttu-id="162ce-233">Utiliser les Chromium-Specific options</span><span class="sxs-lookup"><span data-stu-id="162ce-233">Use Chromium-Specific Options</span></span>  

<span data-ttu-id="162ce-234">Si vous définissez la propriété sur , vous pouvez utiliser la classe pour accéder aux mêmes propriétés et méthodes propres à Chromium que lorsque vous automatisez d’autres Chromium `UseChromium` `true` `EdgeOptions` navigateurs. [][WebdriverCapabilitiesEdgeOptions]</span><span class="sxs-lookup"><span data-stu-id="162ce-234">If you set the `UseChromium` property to `true`, you can use the `EdgeOptions` class to access the same [Chromium-specific properties and methods][WebdriverCapabilitiesEdgeOptions] that are used when you automate other Chromium browsers.</span></span>  

#### [<a name="c"></a><span data-ttu-id="162ce-235">C#</span><span class="sxs-lookup"><span data-stu-id="162ce-235">C#</span></span>](#tab/c-sharp/)  

<a id="use-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<a name="python"></a><span data-ttu-id="162ce-236">Python</span><span class="sxs-lookup"><span data-stu-id="162ce-236">Python</span></span>](#tab/python/)  

<a id="use-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<a name="java"></a><span data-ttu-id="162ce-237">Java</span><span class="sxs-lookup"><span data-stu-id="162ce-237">Java</span></span>](#tab/java/)  

<a id="use-chromium-specific-options-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

#### [<a name="javascript"></a><span data-ttu-id="162ce-238">JavaScript</span><span class="sxs-lookup"><span data-stu-id="162ce-238">JavaScript</span></span>](#tab/javascript/)  

<a id="use-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

* * *  

> [!NOTE]
> <span data-ttu-id="162ce-239">Si la propriété est définie sur , vous ne pouvez pas utiliser les propriétés et méthodes `UseChromium` `true` pour Microsoft Edge \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="162ce-239">If the `UseChromium` property is set to `true`, you are not able to use properties and methods for Microsoft Edge \(EdgeHTML\).</span></span>  


## <a name="other-webdriver-installation-options"></a><span data-ttu-id="162ce-240">Autres options d’installation webDriver</span><span class="sxs-lookup"><span data-stu-id="162ce-240">Other WebDriver installation options</span></span>  

### <a name="docker"></a><span data-ttu-id="162ce-241">Docker</span><span class="sxs-lookup"><span data-stu-id="162ce-241">Docker</span></span>  

<span data-ttu-id="162ce-242">Si vous utilisez [Docker,][DockerHub]exécutez la commande suivante pour télécharger une image pré-configurée avec Microsoft Edge \(Chromium\) et [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] préinstallés.</span><span class="sxs-lookup"><span data-stu-id="162ce-242">If you use [Docker][DockerHub], run the following command to download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] pre-installed.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="162ce-243">Pour plus d’informations, accédez au conteneur [msedgedriver sur Docker Hub.][DockerHubMsedgedriver]</span><span class="sxs-lookup"><span data-stu-id="162ce-243">For more information, navigate to the [msedgedriver container on Docker Hub][DockerHubMsedgedriver].</span></span>  


## <a name="testing-internet-explorer"></a><span data-ttu-id="162ce-244">Test d’Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="162ce-244">Testing Internet Explorer</span></span>

<span data-ttu-id="162ce-245">Pour tester les sites qui nécessitent Internet Explorer, utilisez [Pilote Internet Explorer][GithubSeleniumHqWikiIEDriver] avec Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="162ce-245">To test sites that require Internet Explorer, use [Internet Explorer Driver][GithubSeleniumHqWikiIEDriver] with Internet Explorer.</span></span>  <span data-ttu-id="162ce-246">Pilote Internet Explorer est maintenu par le projet Selenium.</span><span class="sxs-lookup"><span data-stu-id="162ce-246">Internet Explorer Driver is maintained by the Selenium project.</span></span>  <span data-ttu-id="162ce-247">Même si Microsoft Edge prend en charge le mode IE, vous ne pouvez pas utiliser le pilote Microsoft Edge avec Microsoft Edge pour tester des sites en mode IE.</span><span class="sxs-lookup"><span data-stu-id="162ce-247">Even though Microsoft Edge supports IE Mode, you can't use Microsoft Edge Driver with Microsoft Edge to test sites in IE Mode.</span></span>


## <a name="application-guard"></a><span data-ttu-id="162ce-248">ApplicationGuard</span><span class="sxs-lookup"><span data-stu-id="162ce-248">Application Guard</span></span>

<span data-ttu-id="162ce-249">Les sites de confiance qui utilisent Protection d’application Microsoft Defender (Application Guard) peuvent être automatisés à l’aide Microsoft Edge pilote.</span><span class="sxs-lookup"><span data-stu-id="162ce-249">Trusted sites that use Microsoft Defender Application Guard (Application Guard) can be automated using Microsoft Edge Driver.</span></span>

<span data-ttu-id="162ce-250">Les sites non confiance qui utilisent Application Guard ne peuvent pas être automatisés ou manipulés à l’aide Microsoft Edge pilote.</span><span class="sxs-lookup"><span data-stu-id="162ce-250">Untrusted sites that use Application Guard cannot be automated or manipulated using Microsoft Edge Driver.</span></span>  <span data-ttu-id="162ce-251">Application Guard lance les sites non confiance dans un conteneur et ce conteneur n’expose pas le port de débogage distant dont Microsoft Edge Driver a besoin pour communiquer avec le site.</span><span class="sxs-lookup"><span data-stu-id="162ce-251">Application Guard launches untrusted sites in a container, and this container doesn't expose the remote debugging port that Microsoft Edge Driver needs to communicate with the site.</span></span>

<span data-ttu-id="162ce-252">Votre administrateur d’entreprise définit les sites de confiance, y compris les ressources cloud et les réseaux internes.</span><span class="sxs-lookup"><span data-stu-id="162ce-252">Your enterprise administrator defines what are trusted sites, including cloud resources and internal networks.</span></span>  <span data-ttu-id="162ce-253">Les sites qui ne sont pas dans la liste des sites de confiance sont considérés comme non fiables.</span><span class="sxs-lookup"><span data-stu-id="162ce-253">Sites that aren't in the trusted sites list are considered untrusted.</span></span>  <span data-ttu-id="162ce-254">Microsoft Edge Le pilote peut automatiser les fenêtres InPrivate et les sites de la liste des sites de confiance.</span><span class="sxs-lookup"><span data-stu-id="162ce-254">Microsoft Edge Driver can automate both InPrivate windows, and sites in the trusted sites list.</span></span>

<span data-ttu-id="162ce-255">Pour plus d’informations sur Application Guard, accédez à :</span><span class="sxs-lookup"><span data-stu-id="162ce-255">For more information about Application Guard, navigate to:</span></span> 

*  [<span data-ttu-id="162ce-256">Prise en charge de Microsoft Edge pour Microsoft Defender Application Guard</span><span class="sxs-lookup"><span data-stu-id="162ce-256">Microsoft Edge support for Microsoft Defender Application Guard</span></span>][DeployedgeMicrosoftEdgeSecurityWindowsDefenderApplicationGuard]
*  [<span data-ttu-id="162ce-257">Protection d’application Microsoft Defender vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="162ce-257">Microsoft Defender Application Guard overview</span></span>][WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10]


## <a name="see-also"></a><span data-ttu-id="162ce-258">Voir également</span><span class="sxs-lookup"><span data-stu-id="162ce-258">See also</span></span>

*  <span data-ttu-id="162ce-259">[Documentation Selenium][SeleniumDocumentation] : informations sur WebDriver dans le contexte de Selenium et comment écrire des tests WebDriver automatisés à l’aide de Selenium.</span><span class="sxs-lookup"><span data-stu-id="162ce-259">[Selenium documentation][SeleniumDocumentation] - Information about WebDriver in the context of Selenium, and how to write automated WebDriver tests using Selenium.</span></span>


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="162ce-260">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="162ce-260">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="162ce-261">L Microsoft Edge de votre entreprise est enthousiaste à l’écoute de vos commentaires sur l’utilisation de WebDriver, des frameworks de test WebDriver (par exemple, selenium) et Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="162ce-261">The Microsoft Edge team is eager to hear your feedback about using WebDriver, WebDriver testing frameworks (such as Selenium), and Microsoft Edge.</span></span>  <span data-ttu-id="162ce-262">Pour envoyer à l’équipe vos \*\*\*\* questions et [commentaires,][TwitterTweetEdgeDevTools]sélectionnez l’icône Envoyer des commentaires dans le Microsoft Edge DevTools ou envoyez un tweet @EdgeDevTools .</span><span class="sxs-lookup"><span data-stu-id="162ce-262">To send the team your questions and comments, choose the **Send Feedback** icon in the Microsoft Edge DevTools or send a tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="L’icône Envoyer des commentaires dans Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="162ce-264">Icône **Envoyer des commentaires** dans le Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="162ce-264">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  


<!-- links -->  
[DevtoolsIndex]: ../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  
[WebdriverCapabilitiesEdgeOptions]: ./capabilities-edge-options.md "Fonctionnalités et fonctionnalités EdgeOptions | Documents Microsoft"  
<!-- external links -->
[DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability - Microsoft Edge - Stratégies | Documents Microsoft"  
[DeployedgeMicrosoftEdgeSecurityWindowsDefenderApplicationGuard]: /deployedge/microsoft-edge-security-windows-defender-application-guard "Microsoft Edge prise en charge des Protection d’application Microsoft Defender | Documents Microsoft"

[WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10]: /windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview "Protection d’application Microsoft Defender (Windows 10) : Windows sécurité | Documents Microsoft"  

[DockerHub]: https://hub.docker.com "Docker Hub"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Hub Docker"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "microsoft/edge-selenium-tools | GitHub"  
[GithubMicrosoftEdgeSeleniumToolsReleases]: https://github.com/microsoft/edge-selenium-tools/releases "microsoft/edge-selenium-tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SeleniumHQ/selenium | GitHub"  
[GithubSeleniumHqWikiIEDriver]: https://github.com/SeleniumHQ/selenium/wiki/InternetExplorerDriver "Pilote Internet Explorer - Selenium | GitHub"

[JavaScriptnpm]: https://www.npmjs.com/ "npm"  
[JavaScriptSeleniumTools]: https://www.npmjs.com/package/@microsoft/edge-selenium-tools "@microsoft/edge-selenium-tools | npm"  
[JavaScriptSelenium]: https://www.npmjs.com/package/selenium-webdriver "selenium-webdriver | npm"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "Microsoft Edge Pilote | Microsoft Edge Développeur"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Télécharger le nouveau navigateur Microsoft Edge navigateur"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  

[NugetCLI]:https://www.nuget.org/packages/NuGet.CommandLine/ "NuGet. CommandLine | NuGet Galerie"  
[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft.Edge.SeleniumTools | NuGet Galerie"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Selenium.WebDriver 3.141.0 | NuGet Galerie"  
[NugetPackagesSeleniumWebdriver400beta02]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-beta2 "Selenium.WebDriver 4.0.0-beta2 | NuGet Galerie"  

[PythonPip]: https://pypi.org/project/pip/ "pip | PyPI"  
[PythonSeleniumTools]: https://pypi.org/project/msedge-selenium-tools/ "msedge-selenium-tools | PyPI"  
[PythonSelenium]: https://pypi.org/project/selenium/ "selenium | PyPI"

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDocumentation]: https://www.selenium.dev/documentation "Le système d’automatisation du navigateur Selenium Project | Documentation pour Selenium"  
[SeleniumInstallingLibraries]: https://www.selenium.dev/documentation/en/selenium_installation/installing_selenium_libraries "Installation des bibliothèques Selenium | Selenium"

[SonatypeMavenRepositorySearch]: https://search.maven.org/artifact/com.microsoft.edge/msedge-selenium-tools-java/3.141.0/jar "Recherche dans le référentiel central Sonatype Maven | com.microsoft.edge:msedge-selenium-tools-java"

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publier un tweet"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver | W3C"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Navigateur sans | Wikipedia"  
