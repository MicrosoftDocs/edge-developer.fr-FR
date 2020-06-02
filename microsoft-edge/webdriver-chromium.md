---
description: Découvrez comment tester votre site Web ou votre application dans Microsoft Edge ou automatiser le navigateur à l’aide du Web.
title: Web Driver (chrome)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/01/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, développement Web, html, CSS, JavaScript, développeur, Web Driver, sélénium, test, outils, Automation, test
ms.openlocfilehash: 52d1a92df1a0faa21a1f8caa780fe203ad27856e
ms.sourcegitcommit: d39c64e0d439eb0643950248cdf2282383779225
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2020
ms.locfileid: "10689674"
---
# <span data-ttu-id="cdca0-104">Web Driver (chrome)</span><span class="sxs-lookup"><span data-stu-id="cdca0-104">WebDriver (Chromium)</span></span>  

<span data-ttu-id="cdca0-105">L’API du Web [Driver][W3CWebdriver] W3C est une plate-forme et un protocole câblé qui autorisent des programmes ou des scripts à contrôler le comportement d’un navigateur Web, tel que Microsoft Edge \ (chrome \).</span><span class="sxs-lookup"><span data-stu-id="cdca0-105">The W3C [WebDriver][W3CWebdriver] API is a platform and language-neutral interface and wire protocol allowing programs or scripts to control the behavior of a web browser, like Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="cdca0-106">Le WebDriver permet aux développeurs de créer des tests automatisés qui simulent l’interaction de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cdca0-106">WebDriver enables developers to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="cdca0-107">Les tests et simulations du lecteur WebPart diffèrent des tests unitaires JavaScript dans la mesure où le WebDriver a accès aux fonctionnalités et aux informations que JavaScript exécute dans le navigateur ne le fait pas, et qu’il est en mesure de simuler plus précisément des événements utilisateur ou des événements au niveau du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="cdca0-107">WebDriver tests and simulations differ from JavaScript unit tests because WebDriver has access to functionality and information that JavaScript running in the browser does not, and WebDrive is able to more accurately simulate user events or OS-level events.</span></span>  <span data-ttu-id="cdca0-108">Le WebDriver est en mesure de gérer les tests sur plusieurs fenêtres, les onglets et les pages Web au sein d’une seule et même session de test.</span><span class="sxs-lookup"><span data-stu-id="cdca0-108">WebDriver is able to manage testing across multiple windows, tabs and webpages in a single test session.</span></span>  

<span data-ttu-id="cdca0-109">Voici comment prendre en main le WebDriver pour Microsoft Edge \ (chrome \).</span><span class="sxs-lookup"><span data-stu-id="cdca0-109">Here is how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  

## <span data-ttu-id="cdca0-110">Installer Microsoft Edge (chrome)</span><span class="sxs-lookup"><span data-stu-id="cdca0-110">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="cdca0-111">Si ce n’est déjà fait, [Installez Microsoft Edge (chrome)][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="cdca0-111">If you have not already, [install Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="cdca0-112">Si vous utilisez une version préinstallée de Microsoft Edge sur votre ordinateur, vérifiez que vous utilisez Microsoft Edge \ (chrome \) et non Microsoft Edge \ (EdgeHTML \).</span><span class="sxs-lookup"><span data-stu-id="cdca0-112">If you are using a pre-installed version of Microsoft Edge on your machine, verify that you have Microsoft Edge \(Chromium\) and not Microsoft Edge \(EdgeHTML\).</span></span>  <span data-ttu-id="cdca0-113">Une méthode rapide pour vérifier est de charger `edge://settings/help` dans le navigateur et de vérifier que le numéro de version est V75 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="cdca0-113">A quick way to check is to load `edge://settings/help` in the browser and confirm that the version number is v75 or later.</span></span>  

## <span data-ttu-id="cdca0-114">Télécharger le pilote Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="cdca0-114">Download Microsoft Edge Driver</span></span>  

<span data-ttu-id="cdca0-115">Le WebDriver nécessite un pilote spécifique au navigateur pour automatiser chaque navigateur.</span><span class="sxs-lookup"><span data-stu-id="cdca0-115">WebDriver requires a browser-specific driver to automate each browser.</span></span>  <span data-ttu-id="cdca0-116">Pour Microsoft Edge \ (chrome \), le WebDriver nécessite le [pilote Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] approprié pour la build de Microsoft Edge que vous voulez tester ou automatiser.</span><span class="sxs-lookup"><span data-stu-id="cdca0-116">For Microsoft Edge \(Chromium\), WebDriver requires the appropriate [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] for the build of Microsoft Edge you want to test or automate.</span></span>  

<span data-ttu-id="cdca0-117">Pour trouver le numéro de build que vous utilisez, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="cdca0-117">To find your correct build number, use the following steps.</span></span>  

1.  <span data-ttu-id="cdca0-118">Lancer Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="cdca0-118">Launch Microsoft Edge</span></span> 
1.  <span data-ttu-id="cdca0-119">Affichez la version de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="cdca0-119">View the Microsoft Edge \(Chromium\) version.</span></span>  
    *   <span data-ttu-id="cdca0-120">Accédez à</span><span class="sxs-lookup"><span data-stu-id="cdca0-120">Navigate to</span></span> `edge://settings/help`  
    *   <span data-ttu-id="cdca0-121">Sélectionner des `...`  >  **paramètres**  >   **à propos de Microsoft Edge**</span><span class="sxs-lookup"><span data-stu-id="cdca0-121">Select `...` > **Settings** >  **About Microsoft Edge**</span></span>  
1.  <span data-ttu-id="cdca0-122">Assurez-vous que la version correcte du WebDriver est valide pour votre Build, afin qu’elle s’exécute correctement.</span><span class="sxs-lookup"><span data-stu-id="cdca0-122">Verify the correct version of WebDriver for your build ensures, so it runs correctly.</span></span>  

:::image type="complex" source="./media/webdriver-chromium/edge-version.png" alt-text="Numéro de build de l’Canaries Microsoft Edge le 14 janvier 2020":::
   <span data-ttu-id="cdca0-124">Figure1.</span><span class="sxs-lookup"><span data-stu-id="cdca0-124">Figure 1.</span></span>  <span data-ttu-id="cdca0-125">Numéro de build de l’Canaries Microsoft Edge le 14 janvier 2020</span><span class="sxs-lookup"><span data-stu-id="cdca0-125">The build number for Microsoft Edge Canary on January 14, 2020</span></span>  
:::image-end:::  

<span data-ttu-id="cdca0-126">À présent, [Téléchargez la version correspondante du pilote Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads].</span><span class="sxs-lookup"><span data-stu-id="cdca0-126">Now, [download the matching version of Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriverDownloads].</span></span>  

:::image type="complex" source="./media/webdriver-chromium/edge-driver-install.png" alt-text="Section téléchargements de la page du pilote Microsoft Edge":::
   <span data-ttu-id="cdca0-128">Figure2.</span><span class="sxs-lookup"><span data-stu-id="cdca0-128">Figure 2.</span></span>  <span data-ttu-id="cdca0-129">Section téléchargements de la page du [pilote Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads]</span><span class="sxs-lookup"><span data-stu-id="cdca0-129">The Downloads section of the [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriverDownloads] page</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="cdca0-130">Microsoft Edge \ (EdgeHTML \) ne fonctionne pas avec le [pilote Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads].</span><span class="sxs-lookup"><span data-stu-id="cdca0-130">Microsoft Edge \(EdgeHTML\) does not work with [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriverDownloads].</span></span>  <span data-ttu-id="cdca0-131">Pour automatiser Microsoft Edge \ (EdgeHTML), vous devez télécharger [Microsoft WebDriver pour Microsoft Edge \ (EdgeHTML \)][Webdriver].</span><span class="sxs-lookup"><span data-stu-id="cdca0-131">To automate Microsoft Edge \(EdgeHTML\), you must download [Microsoft WebDriver for Microsoft Edge \(EdgeHTML\)][Webdriver].</span></span>  

## <span data-ttu-id="cdca0-132">Choisir une liaison de langue du WebDriver</span><span class="sxs-lookup"><span data-stu-id="cdca0-132">Choose a WebDriver language binding</span></span>  

<span data-ttu-id="cdca0-133">Le dernier composant que vous devez télécharger est un pilote client spécifique à la langue.</span><span class="sxs-lookup"><span data-stu-id="cdca0-133">The last component you must download is a language-specific client driver.</span></span>  <span data-ttu-id="cdca0-134">La liaison de langage traduit le code que vous écrivez dans Python, Java, C \ #, Rubi et JavaScript dans les commandes que le pilote Microsoft Edge que vous avez [téléchargées dans la section précédente](#download-microsoft-edge-driver) est capable de s’exécuter dans Microsoft Edge \ (chrome \).</span><span class="sxs-lookup"><span data-stu-id="cdca0-134">The language binding translates the code you write in Python, Java, C\#, Ruby, and JavaScript into commands that the Microsoft Edge Driver you [downloaded in the previous section](#download-microsoft-edge-driver) is able to run in Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="cdca0-135">[Téléchargez la liaison de langue de votre choix][SeleniumDownloads].</span><span class="sxs-lookup"><span data-stu-id="cdca0-135">[Download the WebDriver language binding of your choice][SeleniumDownloads].</span></span>  <span data-ttu-id="cdca0-136">L’équipe Microsoft Edge recommande fortement le [sélénium 4,00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] ou version ultérieure, car il offre une prise en charge intégrée de Microsoft Edge \ (chrome \).</span><span class="sxs-lookup"><span data-stu-id="cdca0-136">The Microsoft Edge team highly recommends [Selenium 4.00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] or later, since it has built-in support for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="cdca0-137">Toutefois, vous pouvez piloter Microsoft Edge \ (chrome \) dans toutes les versions plus anciennes de sélénium, y compris la version actuelle du sélénium 3D.</span><span class="sxs-lookup"><span data-stu-id="cdca0-137">However, you are able to drive Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="cdca0-138">Si vous avez précédemment automatisé ou testé Microsoft Edge \ (chrome \) en utilisant `ChromeDriver` et `ChromeOptions` , le code de votre lecteur Web ne fonctionne pas correctement avec Microsoft Edge V80 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="cdca0-138">If you were previously automating or testing Microsoft Edge \(Chromium\) by using `ChromeDriver` and `ChromeOptions`, your WebDriver code does not run successfully against Microsoft Edge v80 or later.</span></span>  <span data-ttu-id="cdca0-139">Il s’agit d’un changement majeur et Microsoft Edge \ (chrome \) n’accepte plus les commandes.</span><span class="sxs-lookup"><span data-stu-id="cdca0-139">This is a breaking change and Microsoft Edge \(Chromium\) no longer accepts the commands.</span></span>  <span data-ttu-id="cdca0-140">Vous devez modifier vos tests pour utiliser le `EdgeOptions` pilote de classe et [Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver].</span><span class="sxs-lookup"><span data-stu-id="cdca0-140">You must change your tests to use the `EdgeOptions` class and [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver].</span></span>  

### <span data-ttu-id="cdca0-141">Utilisation de sélénium 3</span><span class="sxs-lookup"><span data-stu-id="cdca0-141">Using Selenium 3</span></span>  

<span data-ttu-id="cdca0-142">[Sélénium 3][|::ref1::|] est la dernière version stable du sélénium.</span><span class="sxs-lookup"><span data-stu-id="cdca0-142">[Selenium 3][|::ref1::|] is the latest stable Selenium release.</span></span>  <span data-ttu-id="cdca0-143">Par défaut, le sélénium 3 pilote l’ancien Microsoft Edge \ (EdgeHTML \) et ne dispose pas de la prise en charge intégrée pour Microsoft Edge \ (chrome \).</span><span class="sxs-lookup"><span data-stu-id="cdca0-143">By default, Selenium 3 drives the old Microsoft Edge \(EdgeHTML\), and does not have built-in support for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="cdca0-144">Pour utiliser le sélénium 3 avec Microsoft Edge \ (chrome \), installez les [outils de sélénium pour le package Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] .</span><span class="sxs-lookup"><span data-stu-id="cdca0-144">To use Selenium 3 with Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package.</span></span>  <span data-ttu-id="cdca0-145">Les outils de sélénium pour Microsoft Edge étendent le sélénium 3 avec un pilote mis à jour pour vous aider à écrire des tests automatisés pour les navigateurs Microsoft Edge \ (EdgeHTML \) et Microsoft Edge \ (chrome \).</span><span class="sxs-lookup"><span data-stu-id="cdca0-145">The Selenium Tools for Microsoft Edge extend Selenium 3 with an updated driver to help you write automated tests for both the Microsoft Edge \(EdgeHTML\) and new Microsoft Edge \(Chromium\) browsers.</span></span>  

<span data-ttu-id="cdca0-146">Les outils de sélénium pour Microsoft Edge sont une solution pour les développeurs préférant conserver le niveau d’un test de navigateur pour les développeurs et vouloir ajouter une couverture pour le nouveau navigateur Microsoft Edge \ (chrome \) sans changer les versions de sélénium.</span><span class="sxs-lookup"><span data-stu-id="cdca0-146">Selenium Tools for Microsoft Edge is a solution for developers who prefer to remain on Selenium 3 and developers who have existing browser tests and want to add coverage for the new Microsoft Edge \(Chromium\) browser without changing Selenium versions.</span></span>  <span data-ttu-id="cdca0-147">Les `EdgeDriver` `EdgeDriverService` classes et incluses dans les outils sont entièrement compatibles avec les équivalents intégrés en sélénium et exécutent Microsoft Edge \ (EdgeHTML \) par défaut, de sorte que les outils puissent être utilisés en tant que remplacement de lâcher en continu pour les classes Edge existantes en sélénium.</span><span class="sxs-lookup"><span data-stu-id="cdca0-147">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium, and run Microsoft Edge \(EdgeHTML\) by default so the tools may be used as a seamless drop-in replacement for the existing Edge classes in Selenium.</span></span>  

<span data-ttu-id="cdca0-148">[Installez les outils de sélénium pour Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] pour commencer à utiliser Microsoft Edge \ (chrome \) avec votre projet sélénium 3.</span><span class="sxs-lookup"><span data-stu-id="cdca0-148">[Install Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] to begin using Microsoft Edge \(Chromium\) with your Selenium 3 project.</span></span>  

## <span data-ttu-id="cdca0-149">Utiliser Microsoft Edge (chrome) avec WebDriver</span><span class="sxs-lookup"><span data-stu-id="cdca0-149">Use Microsoft Edge (Chromium) with WebDriver</span></span>

<span data-ttu-id="cdca0-150">Les exemples suivants sont Runnable en utilisant sélénium 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="cdca0-150">The following examples are runnable using either Selenium 3 or 4.</span></span>  <span data-ttu-id="cdca0-151">Pour les utiliser avec le sélénium 3, les [outils de sélénium pour Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] doivent être installés.</span><span class="sxs-lookup"><span data-stu-id="cdca0-151">To use with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] must be installed.</span></span>  

### <span data-ttu-id="cdca0-152">Utilisation de base</span><span class="sxs-lookup"><span data-stu-id="cdca0-152">Basic Usage</span></span>  

<span data-ttu-id="cdca0-153">Pour utiliser avec Microsoft Edge \ (EdgeHTML \), il vous suffit de créer une instance par défaut de la `EdgeDriver` classe.</span><span class="sxs-lookup"><span data-stu-id="cdca0-153">To use with Microsoft Edge \(EdgeHTML\), simply create a default instance of the `EdgeDriver` class.</span></span>

#### [<span data-ttu-id="cdca0-154">C#</span><span class="sxs-lookup"><span data-stu-id="cdca0-154">C#</span></span>](#tab/c-sharp/)  

<a id="basic-usage-code"></a>  

```csharp
var driver = new EdgeDriver();
```  

#### [<span data-ttu-id="cdca0-155">Software</span><span class="sxs-lookup"><span data-stu-id="cdca0-155">Python</span></span>](#tab/python/)  

<a id="basic-usage-code"></a>  

```python
driver = Edge()
```  

#### [<span data-ttu-id="cdca0-156">JavaScript</span><span class="sxs-lookup"><span data-stu-id="cdca0-156">JavaScript</span></span>](#tab/javascript/)  

<a id="basic-usage-code"></a>  

```javascript
let driver = edge.Driver.createSession();
```  

* * *  

### <span data-ttu-id="cdca0-157">Pilotage de Microsoft Edge (chrome)</span><span class="sxs-lookup"><span data-stu-id="cdca0-157">Driving Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="cdca0-158">Pour utiliser la fonction avec Microsoft Edge \ (chrome \) à la place, créez une nouvelle `EdgeDriver` classe et transmettez-lui l' `EdgeOptions` objet avec la `UseChromium` propriété définie sur `true` .</span><span class="sxs-lookup"><span data-stu-id="cdca0-158">To use with Microsoft Edge \(Chromium\) instead, create a new `EdgeDriver` class and pass it the `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<span data-ttu-id="cdca0-159">C#</span><span class="sxs-lookup"><span data-stu-id="cdca0-159">C#</span></span>](#tab/c-sharp/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="cdca0-160">Software</span><span class="sxs-lookup"><span data-stu-id="cdca0-160">Python</span></span>](#tab/python/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### [<span data-ttu-id="cdca0-161">JavaScript</span><span class="sxs-lookup"><span data-stu-id="cdca0-161">JavaScript</span></span>](#tab/javascript/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

### <span data-ttu-id="cdca0-162">Choix de fichiers binaires de navigateur spécifiques (chrome uniquement)</span><span class="sxs-lookup"><span data-stu-id="cdca0-162">Choosing Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="cdca0-163">Utilisez la `EdgeOptions` classe pour sélectionner un fichier binaire spécifique.</span><span class="sxs-lookup"><span data-stu-id="cdca0-163">Use the `EdgeOptions` class to choose a specific binary.</span></span>  <span data-ttu-id="cdca0-164">Cette fonctionnalité est utile pour tester des [canaux Microsoft Edge Preview][MicrosoftedgeinsiderDownload] tels que Microsoft Edge Beta.</span><span class="sxs-lookup"><span data-stu-id="cdca0-164">It is useful for testing [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<span data-ttu-id="cdca0-165">C#</span><span class="sxs-lookup"><span data-stu-id="cdca0-165">C#</span></span>](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="cdca0-166">Software</span><span class="sxs-lookup"><span data-stu-id="cdca0-166">Python</span></span>](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [<span data-ttu-id="cdca0-167">JavaScript</span><span class="sxs-lookup"><span data-stu-id="cdca0-167">JavaScript</span></span>](#tab/javascript/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <span data-ttu-id="cdca0-168">Personnalisation du service de pilote Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="cdca0-168">Customizing the Microsoft Edge Driver Service</span></span>  

#### [<span data-ttu-id="cdca0-169">C#</span><span class="sxs-lookup"><span data-stu-id="cdca0-169">C#</span></span>](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="cdca0-170">Quand une `EdgeDriver` instance de classe est créée à l’aide d’une `EdgeOptions` classe, elle crée et lance automatiquement la `EdgeDriverService` classe appropriée pour Microsoft Edge \ (EdgeHTML \) ou Microsoft Edge \ (chrome \).</span><span class="sxs-lookup"><span data-stu-id="cdca0-170">When an `EdgeDriver` class instance is created using `EdgeOptions` class, it automatically creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="cdca0-171">Si vous souhaitez créer un, créez-en un à l' `EdgeDriverService` aide de la `CreateChromiumService()` méthode.</span><span class="sxs-lookup"><span data-stu-id="cdca0-171">If you want to create an `EdgeDriverService`, create one configured for Microsoft Edge \(Chromium\) using the `CreateChromiumService()` method.</span></span>  <span data-ttu-id="cdca0-172">Il peut s’avérer utile pour des personnalisations supplémentaires telles que l’activation de la sortie détaillée du journal dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="cdca0-172">You may find it useful for additional customizations like enabling verbose log output in the following code.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE]
> <span data-ttu-id="cdca0-173">Vous n’avez pas besoin de fournir l' `EdgeOptions` objet lors du passage de l' `EdgeDriver` instance de classe `EdgeDriverService` .</span><span class="sxs-lookup"><span data-stu-id="cdca0-173">You do not need to provide the `EdgeOptions` object when passing the `EdgeDriver` class instance the `EdgeDriverService`.</span></span>  <span data-ttu-id="cdca0-174">La `EdgeDriver` classe utilise les options par défaut pour Microsoft Edge \ (EdgeHTML \) ou Microsoft Edge \ (chrome \), en fonction du type de service que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="cdca0-174">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) depending on what kind of service you provide.</span></span>  
> 
> <span data-ttu-id="cdca0-175">Toutefois, si vous souhaitez fournir des `EdgeDriverService` `EdgeOptions` classes et, vous devez vous assurer que les deux sont configurées pour la même version de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="cdca0-175">However, if you want to provide both an `EdgeDriverService` and `EdgeOptions` classes, you must ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="cdca0-176">Par exemple, il n’est pas possible d’utiliser une classe Microsoft Edge \ (EdgeHTML \) par défaut `EdgeDriverService` dans la `EdgeOptions` classe.</span><span class="sxs-lookup"><span data-stu-id="cdca0-176">For example, it is not possible to use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="cdca0-177">La `EdgeDriver` classe lève une erreur pour empêcher l’utilisation de différentes versions.</span><span class="sxs-lookup"><span data-stu-id="cdca0-177">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<span data-ttu-id="cdca0-178">Software</span><span class="sxs-lookup"><span data-stu-id="cdca0-178">Python</span></span>](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="cdca0-179">Lorsque vous utilisez Python, l' `Edge` objet crée et gère l’objet `EdgeService` .</span><span class="sxs-lookup"><span data-stu-id="cdca0-179">When using Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="cdca0-180">Pour configurer le `EdgeService` , passez des arguments supplémentaires à l' `Edge` objet:</span><span class="sxs-lookup"><span data-stu-id="cdca0-180">To configure the `EdgeService`, pass additional arguments to the `Edge` object:</span></span>

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<span data-ttu-id="cdca0-181">JavaScript</span><span class="sxs-lookup"><span data-stu-id="cdca0-181">JavaScript</span></span>](#tab/javascript/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="cdca0-182">Lorsque vous utilisez JavaScript, créez et configurez a `Service` avec la `ServiceBuilder` classe.</span><span class="sxs-lookup"><span data-stu-id="cdca0-182">When using JavaScript, create and configure a `Service` with the `ServiceBuilder` class.</span></span>  <span data-ttu-id="cdca0-183">Vous pouvez éventuellement transmettre l' `Service` objet à l' `Driver` objet qui démarre et arrête le service pour vous.</span><span class="sxs-lookup"><span data-stu-id="cdca0-183">You may optionally pass the `Service` object to the `Driver` object which starts and stops the service for you.</span></span>  

<span data-ttu-id="cdca0-184">Pour configurer le `Service` , exécutez des méthodes supplémentaires dans la `ServiceBuilder` classe avant d’utiliser la méthode, puis `build()` transmettez la `service` en tant que paramètre à la `Driver.createSession()` méthode.</span><span class="sxs-lookup"><span data-stu-id="cdca0-184">To configure the `Service`, run additional methods in the `ServiceBuilder` class before using the `build()` method and  then pass the `service` as a parameter in the `Driver.createSession()` method.</span></span>  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### <span data-ttu-id="cdca0-185">Utilisation des options spécifiques au chrome</span><span class="sxs-lookup"><span data-stu-id="cdca0-185">Using Chromium-Specific Options</span></span>  

<span data-ttu-id="cdca0-186">L’utilisation de la `EdgeOptions` classe avec la `UseChromium` propriété définie pour `true` vous permet d’accéder à toutes les méthodes et propriétés de la classe [ChromeOptions][SeleniumWebDriverChromeoptionsClass] en sélénium.</span><span class="sxs-lookup"><span data-stu-id="cdca0-186">Using the `EdgeOptions` class with the `UseChromium` property set to `true` gives you access to all of the same methods and properties that are available in the [ChromeOptions][SeleniumWebDriverChromeoptionsClass] class in Selenium.</span></span>  <span data-ttu-id="cdca0-187">Par exemple, comme avec d’autres navigateurs de chrome, utilisez la `EdgeOptions.AddArguments()` méthode pour exécuter Microsoft Edge \ (chrome \) en [mode headless][WikiHeadlessBrowser] dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="cdca0-187">For example, just like with other Chromium browsers, use the `EdgeOptions.AddArguments()` method to run Microsoft Edge \(Chromium\) in [headless mode][WikiHeadlessBrowser] in the following code.</span></span>  

#### [<span data-ttu-id="cdca0-188">C#</span><span class="sxs-lookup"><span data-stu-id="cdca0-188">C#</span></span>](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<span data-ttu-id="cdca0-189">Software</span><span class="sxs-lookup"><span data-stu-id="cdca0-189">Python</span></span>](#tab/python/)  

<a id="using-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<span data-ttu-id="cdca0-190">JavaScript</span><span class="sxs-lookup"><span data-stu-id="cdca0-190">JavaScript</span></span>](#tab/javascript/)  

<a id="using-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```
* * *  

> [!NOTE]
> <span data-ttu-id="cdca0-191">Les [méthodes et propriétés spécifiques au chrome][SeleniumWebDriverChromeoptionsClass] sont toujours disponibles, mais n’ont aucun effet si la `UseChromium` propriété n’est pas définie sur `true` .</span><span class="sxs-lookup"><span data-stu-id="cdca0-191">The [Chromium-specific properties and methods][SeleniumWebDriverChromeoptionsClass] are always available but have no effect if the `UseChromium` property is not set to `true`.</span></span>  <span data-ttu-id="cdca0-192">De la même façon, les propriétés existantes et les méthodes destinées à Microsoft Edge \ (EdgeHTML \) n’ont aucun effet si la `UseChromium` propriété a la valeur `true` .</span><span class="sxs-lookup"><span data-stu-id="cdca0-192">Similarly, existing properties and methods meant for Microsoft Edge \(EdgeHTML\) have no effect if `UseChromium` property is set to `true`.</span></span>  

## <span data-ttu-id="cdca0-193">Autres méthodes de configuration de WebDriver</span><span class="sxs-lookup"><span data-stu-id="cdca0-193">Other ways to set up WebDriver</span></span>  

### <span data-ttu-id="cdca0-194">Chocolat</span><span class="sxs-lookup"><span data-stu-id="cdca0-194">Chocolatey</span></span>  

<span data-ttu-id="cdca0-195">Si vous utilisez le programme [chocolaté][Chocolatey] en tant que gestionnaire de package, installez le pilote Microsoft Edge en exécutant la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="cdca0-195">If you are using [Chocolatey][Chocolatey] as your package manager, install the Microsoft Edge Driver by running the following command.</span></span>  

```console
choco install selenium-chromium-edge-driver
```  

<span data-ttu-id="cdca0-196">Pour plus d’informations, voir [pilote de contour de chrome de sélénium au chocolat][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span><span class="sxs-lookup"><span data-stu-id="cdca0-196">For more information, see [Selenium Chromium Edge Driver on Chocolatey][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span></span>  

### <span data-ttu-id="cdca0-197">Docker</span><span class="sxs-lookup"><span data-stu-id="cdca0-197">Docker</span></span>  

<span data-ttu-id="cdca0-198">Si vous utilisez la version d' [arrimateur][DockerHub], téléchargez une image préconfigurée avec Microsoft Edge \ (chrome \) et [pilote Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] déjà installé en exécutant la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="cdca0-198">If you are using [Docker][DockerHub], download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] already installed by running the following command.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="cdca0-199">Pour plus d’informations, consultez [conteneur sur le hub de l’ancrage][DockerHubMsedgedriver].</span><span class="sxs-lookup"><span data-stu-id="cdca0-199">For more information, see [container on Docker Hub][DockerHubMsedgedriver].</span></span>  

## <span data-ttu-id="cdca0-200">Contacter l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="cdca0-200">Getting in touch with the Microsoft Edge DevTools team</span></span>    

<span data-ttu-id="cdca0-201">L’équipe Microsoft Edge a hâte d’entendre vos commentaires concernant l’utilisation de WebDriver, de sélénium et de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="cdca0-201">The Microsoft Edge team is eager to hear your feedback about using WebDriver, Selenium, and Microsoft Edge!</span></span>  <span data-ttu-id="cdca0-202">Vous pouvez utiliser l’icône de **Commentaires** dans le Microsoft Edge devtools ou le tweet [@EdgeDevTools][TwitterTweetEdgeDevTools] pour indiquer à l’équipe ce que vous en pensez.</span><span class="sxs-lookup"><span data-stu-id="cdca0-202">Use the **Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterTweetEdgeDevTools] to let the team know what you think.</span></span>  


:::image type="complex" source="./devtools-guide-chromium/media/devtools-feedback.png" alt-text="Icône de commentaires dans le Microsoft Edge DevTools":::
   <span data-ttu-id="cdca0-204">Icône de **Commentaires** dans le Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="cdca0-204">The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- image links -->  

<!-- links -->  

[Webdriver]: ./webdriver.md "Web Driver (EdgeHTML) | Documents Microsoft"  

[Chocolatey]: https://chocolatey.org "Chocolat Programme en chocolat"  
[ChocolateyPackagesSeleniumChromiumEdgeDriver]: https://chocolatey.org/packages/selenium-chromium-edge-driver "Pilote du périphérique de chrome de sélénium Chocolat"  

[DockerHub]: https://hub.docker.com "Hub de l’ancrage"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Hub de l’ancrage"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "Microsoft/Edge-sélénium-Tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SeleniumHQ/sélénium | GitHub"  

[MicrosoftDeveloperEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "Web Driver | Développeur Microsoft"
[MicrosoftDeveloperEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads "Téléchargements-WebDriver | Développeur Microsoft"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Télécharger le nouveau navigateur Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  

[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft. Edge. SeleniumTools | Galerie NuGet"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Sélénium. WebDriver 3.141.0 | Galerie NuGet"  
[NugetPackagesSeleniumWebdriver400alpha05]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha05 "Sélénium. WebDriver 4.0.0-alpha05 | Galerie NuGet"  

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDownloads]: https://selenium.dev/downloads "Téléchargements | Sélénium"  
[SeleniumWebDriverChromeoptionsClass]: https://www.selenium.dev/selenium/docs/api/dotnet/?topic=html/T_OpenQA_Selenium_Chrome_ChromeOptions.htm "Classe ChromeOptions-WebDriver | Sélénium"  

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publiez un tweet"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Navigateur headless | Wikipédia"  
