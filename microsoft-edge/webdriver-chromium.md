---
description: Découvrez comment tester votre site Web ou votre application dans Microsoft Edge ou automatiser le navigateur à l’aide du Web.
title: WebDriver (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/08/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, développement Web, html, CSS, JavaScript, développeur, Web Driver, sélénium, test, outils, Automation, test
ms.openlocfilehash: c60095373be337307225f28d320cae19174531a7
ms.sourcegitcommit: 1b5dfc5a2c7130b3abc6b4545fcaaae0b0897148
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2020
ms.locfileid: "10757579"
---
# Utiliser le WebDriver (chrome) pour l’automatisation des tests  

Le WebDriver permet aux développeurs de créer des tests automatisés qui simulent l’interaction de l’utilisateur.  Les tests et simulations du lecteur WebPart diffèrent des tests unitaires JavaScript pour les raisons suivantes: 
*   Accès aux fonctionnalités et informations non disponibles pour JavaScript exécuté dans les navigateurs.  
*   Simule des événements utilisateur ou des événements de niveau système d’exploitation plus précisément.  
*   Gère les tests sur plusieurs fenêtres, onglets et pages Web au sein d’une seule et même session de test.  
*   Exécute plusieurs sessions de Microsoft Edge sur un ordinateur spécifique.  

La section suivante décrit comment prendre en main le WebDriver pour Microsoft Edge \ (chrome \).  

## Installer Microsoft Edge (chrome)  

Vérifiez que vous avez installé [Microsoft Edge (chrome)][MicrosoftEdge].  Pour confirmer l’installation de Microsoft Edge (chrome), accédez à `edge://settings/help` dans le navigateur, puis vérifiez que le numéro de version est la version 75 ou une version ultérieure.  

## Télécharger le pilote Microsoft Edge  

Pour commencer à automatiser les tests, procédez comme suit pour vous assurer que la version du WebDriver que vous installez correspond à la version de votre navigateur.  

1.  Accédez à `edge://settings/help` pour obtenir la version de Edge.  
    
    :::image type="complex" source="./media/webdriver-chromium/edge-version.png" alt-text="Numéro de build de l’Canaries Microsoft Edge le 14 janvier 2020":::
       Figure1.  Numéro de build de l’Canaries Microsoft Edge le 14 janvier 2020
    :::image-end:::  
    
1.  Accédez à la page de [téléchargements de pilotes Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads] et téléchargez le pilote correspondant au numéro de version Edge.  
    
    :::image type="complex" source="./media/webdriver-chromium/edge-driver-install.png" alt-text="Section téléchargements de la page du pilote Microsoft Edge":::
       Figure2.  Section téléchargements de la page du [pilote Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver]
    :::image-end:::  
    
    > [!NOTE] 
    > Pour plus d’informations sur l’Automation de test à l’aide de Microsoft Edge (EdgeHTML), voir [Microsoft WebDriver pour Microsoft Edge (EdgeHTML)][Webdriver].  

## Choisir une liaison de langue du WebDriver  

Le dernier composant que vous devez télécharger est un pilote client propre à la langue, qui permet de traduire votre code \ (Python, Java, C \ #, Rubi, JavaScript \) en commandes exécutées par le pilote Microsoft Edge.  

[Téléchargez la liaison de langue de votre choix][SeleniumDownloads].  L’équipe Microsoft Edge recommande le [sélénium 4,00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] ou version ultérieure, car il prend en charge Microsoft Edge \ (chrome \).  Toutefois, vous pouvez contrôler Microsoft Edge \ (chrome \) dans toutes les versions plus anciennes de sélénium, y compris la version actuelle du sélénium 3D.  

> [!IMPORTANT]
> Si vous avez précédemment automatisé ou testé Microsoft Edge \ (chrome \) à l’aide de l’application `ChromeDriver` et des `ChromeOptions` classes, votre code WebDriver n’est pas exécuté sur la version 80 de Microsoft Edge ou une version ultérieure.  Pour résoudre ce problème, mettez à jour vos tests pour utiliser la `EdgeOptions` classe et installer le [pilote Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver].  

### Utiliser le sélénium 3  

Si vous utilisez déjà [sélénium 3][|::ref1::|], il est possible que vous ayez des tests de navigateur existants et que vous vouliez ajouter une couverture pour Microsoft Edge \ (chrome \) sans changer votre version de sélénium.  Pour utiliser le [sélénium 3][|::ref2::|] pour écrire des tests automatisés pour Microsoft Edge \ (EdgeHTML \) et Microsoft Edge \ (chrome \), installez les [outils de sélénium pour le package Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] pour utiliser le pilote mis à jour.  Les `EdgeDriver` `EdgeDriverService` classes et incluses dans les outils sont entièrement compatibles avec les équivalents intégrés d’sélénium 4.  

Procédez comme suit pour ajouter les [outils de sélénium pour Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] et [sélénium 3][|::ref3::|] à votre projet.

#### [C#](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

Ajoutez les packages [Microsoft. Edge. SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] et [sélénium. WebDriver][NugetPackagesSeleniumWebdriver31410] à votre projet .net à l’aide de l' [interface CLI][NugetCLI] ou [Visual Studio][VisualStudio]NuGet.

#### [Software](#tab/python/)  

<a id="selenium-tools-install"></a>  

Utilisez [PIP][PythonPip] pour installer le [msedge-sélénium-Tools][PythonSeleniumTools] et les packages de [sélénium][PythonSelenium] :

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [JavaScript](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

Utilisez [NPM][JavaScript|::ref4::|] pour installer [Edge-sélénium-Tools][JavaScriptSeleniumTools] et les packages [sélénium-Web Driver][JavaScriptSelenium] :

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## Utiliser Microsoft Edge (chrome) avec WebDriver

Vous pouvez exécuter les exemples suivants à l’aide de sélénium 3 ou 4.  Pour une utilisation avec le sélénium 3, les [outils de sélénium pour le package Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] doivent être installés.  

### Utilisation de base  

Pour utiliser avec Microsoft Edge \ (EdgeHTML \), il vous suffit de créer une instance par défaut de la `EdgeDriver` classe.

#### [C#](#tab/c-sharp/)  

<a id="basic-usage-code"></a>  

```csharp
var driver = new EdgeDriver();
```  

#### [Software](#tab/python/)  

<a id="basic-usage-code"></a>  

```python
driver = Edge()
```  

#### [JavaScript](#tab/javascript/)  

<a id="basic-usage-code"></a>  

```javascript
let driver = edge.Driver.createSession();
```  

* * *  

### Pilotage de Microsoft Edge (chrome)  

Pour utiliser avec Microsoft Edge \ (chrome \), créez une nouvelle `EdgeDriver` classe et transmettez-lui l' `EdgeOptions` objet avec la `UseChromium` propriété définie sur `true` .  

#### [C#](#tab/c-sharp/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [Software](#tab/python/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### [JavaScript](#tab/javascript/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> Si la stratégie [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] est définie sur `2` , le [pilote Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] ne peut pas accéder à [Microsoft Edge (chrome)][MicrosoftEdge] , car le pilote utilise [Microsoft Edge devtools][DevToolsMain].  Assurez-vous de définir la stratégie [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] sur `0` ou `1` pour automatiser [Microsoft Edge (chrome)][MicrosoftEdge].  

### Choix de fichiers binaires de navigateur spécifiques (chrome uniquement)  

Vous pouvez utiliser la `EdgeOptions` classe avec des fichiers binaires de Microsoft Edge (chrome) spécifiques.  Par exemple, vous pouvez exécuter des tests en utilisant les [canaux Microsoft Edge Preview][MicrosoftedgeinsiderDownload] tels que Microsoft Edge Beta.  

#### [C#](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [Software](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [JavaScript](#tab/javascript/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### Personnalisation du service de pilote Microsoft Edge  

#### [C#](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

Quand une `EdgeDriver` instance de classe est créée à l’aide d’une `EdgeOptions` classe, elle crée et lance la `EdgeDriverService` classe appropriée pour Microsoft Edge \ (EdgeHTML \) ou Microsoft Edge \ (chrome \).  

Si vous souhaitez créer un, créez-en un à l' `EdgeDriverService` aide de la `CreateChromiumService()` méthode.  Il peut s’avérer utile pour des personnalisations supplémentaires telles que l’activation de la sortie détaillée du journal dans le code suivant.  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
>Vous n’avez pas besoin de fournir l' `EdgeOptions` objet lors `EdgeDriverService` du passage à l' `EdgeDriver` instance. La `EdgeDriver` classe utilise les options par défaut pour Microsoft Edge \ (EdgeHTML \) ou Microsoft Edge \ (chrome \), en fonction du service que vous fournissez.  
> Toutefois, si vous souhaitez fournir les deux `EdgeDriverService` `EdgeOptions` classes et, assurez-vous que les deux sont configurées pour la même version de Microsoft Edge.  Par exemple, il n’est pas possible d’utiliser une classe Microsoft Edge (EdgeHTML) par défaut `EdgeDriverService` et des propriétés de chrome dans la `EdgeOptions` classe.  La `EdgeDriver` classe lève une erreur pour empêcher l’utilisation de différentes versions.  

#### [Software](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

Lorsque vous utilisez Python, l' `Edge` objet crée et gère l’objet `EdgeService` .  Pour configurer le `EdgeService` , passez des arguments supplémentaires à l' `Edge` objet, comme indiqué dans le code suivant.  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [JavaScript](#tab/javascript/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

Lorsque vous utilisez JavaScript, créez et configurez a `Service` avec la `ServiceBuilder` classe.  Vous pouvez éventuellement transmettre l' `Service` objet à l' `Driver` objet qui démarre et arrête le service pour vous.  
Pour configurer le `Service` , exécutez des méthodes supplémentaires dans la `ServiceBuilder` classe avant d’utiliser la `build()` méthode.  Ensuite, transmettez la `service` en tant que paramètre à la `Driver.createSession()` méthode.  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * * 

### Utiliser des options propres au chrome  

Si vous définissez la `UseChromium` propriété sur `true` , vous pouvez utiliser la `EdgeOptions` classe pour accéder aux mêmes [Propriétés et méthodes propres au chrome][SeleniumWebDriverChromeoptionsClass] que lorsque vous automatisez d’autres navigateurs de chrome.  

#### [C#](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [Software](#tab/python/)  

<a id="using-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [JavaScript](#tab/javascript/)  

<a id="using-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```

* * *  
> [!NOTE]
> Si la `UseChromium` propriété est définie sur `true` , vous ne pouvez pas utiliser les propriétés et les méthodes pour Microsoft Edge \ (EdgeHTML \).  

## Autres options d’installation d’un Web Driver  

### Chocolat  

Si vous utilisez le programme [chocolaté][Chocolatey] en tant que gestionnaire de package, installez le pilote Microsoft Edge en exécutant la commande suivante.  

```console
choco install selenium-chromium-edge-driver
```  

Pour plus d’informations, voir [pilote de contour de chrome de sélénium au chocolat][ChocolateyPackagesSeleniumChromiumEdgeDriver].  

### Docker  

Si vous utilisez l' [ancrage][DockerHub], téléchargez une image préconfigurée avec Microsoft Edge \ (chrome \) et le [pilote Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] préinstallé en exécutant la commande suivante.  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

Pour plus d’informations, consultez [conteneur sur le hub de l’ancrage][DockerHubMsedgedriver].  

## Contacter l’équipe Microsoft Edge DevTools  

L’équipe Microsoft Edge a hâte d’entendre vos commentaires concernant l’utilisation de WebDriver, de sélénium et de Microsoft Edge.  Vous pouvez utiliser l’icône de **Commentaires** dans le Microsoft Edge devtools ou le tweet [@EdgeDevTools][TwitterTweetEdgeDevTools] pour indiquer à l’équipe ce que vous en pensez.  


:::image type="complex" source="./devtools-guide-chromium/media/devtools-feedback.png" alt-text="Icône de commentaires dans le Microsoft Edge DevTools":::
   Icône de **Commentaires** dans le Microsoft Edge devtools  
:::image-end:::  

<!-- image links -->  

<!-- links -->  

[DevToolsMain]: ./devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"
[Webdriver]: ./webdriver.md "Web Driver (EdgeHTML) | Documents Microsoft"  

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

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Navigateur headless | Wikipédia"  
