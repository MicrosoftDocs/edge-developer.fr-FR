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
# Utiliser WebDriver (Chromium) pour tester l’automatisation  

WebDriver permet aux développeurs de créer des tests automatisés qui simulent l’interaction utilisateur.  Les tests et simulations WebDriver diffèrent des tests unitaires JavaScript, car WebDriver :  

*   Accède aux fonctionnalités et informations non disponibles pour JavaScript s’exécutant dans les navigateurs.  
*   Simule les événements utilisateur ou au niveau du système d’exploitation plus précisément.  
*   Gère plusieurs fenêtres, onglets et pages web en une seule session de test.  
*   Exécute plusieurs sessions de Microsoft Edge sur un ordinateur spécifique.  
    
La section suivante décrit comment commencer avec WebDriver pour Microsoft Edge \(Chromium\).  

## Installer Microsoft Edge (Chromium)  

Assurez-vous [d’installer Microsoft Edge (Chromium).][MicrosoftEdge]  Pour confirmer que Microsoft Edge \(Chromium\) est installé, accédez à , et vérifiez que le numéro de version est `edge://settings/help` version 75 ou ultérieure.  

## Télécharger le pilote Microsoft Edge  

Pour commencer à automatiser les tests, utilisez les étapes suivantes pour vous assurer que la version WebDriver que vous installez correspond à la version de votre navigateur.  

1.  Accédez `edge://settings/help` à la version de Microsoft Edge.  
    
    :::image type="complex" source="./media/edge-version.png" alt-text="Numéro de build de Microsoft Edge Canary le 14 janvier 2020":::
       Numéro de build de Microsoft Edge Canary le 14 janvier 2020
    :::image-end:::  
    
1.  Accédez à la page [téléchargements][MicrosoftDeveloperEdgeToolsWebdriverDownloads] du pilote Microsoft Edge et téléchargez le pilote qui correspond au numéro de version de Microsoft Edge.  
    
    :::image type="complex" source="./media/edge-driver-install.png" alt-text="Section Téléchargements de la page Pilote Microsoft Edge":::
       Section Téléchargements de la page [Pilote Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver]
    :::image-end:::  
    
    <!--  
    > [!NOTE] 
    > For more information about test automation using Microsoft Edge (EdgeHTML), see [Microsoft WebDriver for Microsoft Edge (EdgeHTML)][Webdriver].  
    -->  

## Choisir une liaison de langue WebDriver  

Le dernier composant que vous devez télécharger est un pilote client propre à une langue pour traduire votre code \(Python, Java, C\#, Ruby, JavaScript\) en commandes que le pilote Microsoft Edge exécute dans Microsoft Edge \(Chromium\).  

[Téléchargez la liaison de langue WebDriver de votre choix.][SeleniumDownloads]  L’équipe Microsoft Edge recommande [Selenium 4.00-alpha07][NugetPackagesSeleniumWebdriver400alpha07] ou version ultérieure, car elle prend en charge Microsoft Edge \(Chromium\).  Toutefois, vous pouvez contrôler Microsoft Edge \(Chromium\) dans toutes les versions antérieures de Selenium, y compris la version stable actuelle de Selenium 3.  

> [!IMPORTANT]
> Si vous automatisiez ou testiez précédemment l’utilisation et les classes de Microsoft Edge \(Chromium\), votre code WebDriver ne s’exécute pas sur `ChromeDriver` `ChromeOptions` Microsoft Edge Version 80 ou ultérieure.  Pour résoudre ce problème, mettez à jour vos tests pour utiliser la `EdgeOptions` classe et téléchargez [le pilote Microsoft Edge.][MicrosoftDeveloperEdgeToolsWebdriver]  

### Utiliser Selenium 3  

Si vous utilisez déjà [Selenium 3,][|::ref1::|]vous avez peut-être des tests de navigateur existants et souhaitez ajouter une couverture pour Microsoft Edge \(Chromium\) sans modifier votre version de Selenium.  Pour utiliser [Selenium 3][|::ref2::|] afin d’écrire des tests automatisés pour Microsoft Edge \(EdgeHTML\) et Microsoft Edge \(Chromium\), installez le package [Outils Selenium][GithubMicrosoftEdgeSeleniumTools] pour Microsoft Edge pour utiliser le pilote mis à jour.  Les `EdgeDriver` `EdgeDriverService` classes incluses dans les outils sont entièrement compatibles avec les équivalents intégrés dans Selenium 4.  

Utilisez les étapes suivantes pour ajouter les outils [Selenium pour Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] et [Selenium 3][|::ref3::|] à votre projet.  

#### [C#](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

Ajoutez les packages [Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] et [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] à votre projet .NET à l’aide de l’CLI [NuGet][NugetCLI] [ou Visual Studio][VisualStudio].  

#### [Python](#tab/python/)  

<a id="selenium-tools-install"></a>  

Utilisez [pip][PythonPip] pour installer [les packages msedge-selenium-tools][PythonSeleniumTools] et [selenium.][PythonSelenium]  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [Java](#tab/java/)  

<a id="selenium-tools-install"></a>  

Si votre Java utilise Maven, ajoutez [msedge-selenium-tools-java][SonatypeMavenRepositorySearch] en faisant face à la dépendance suivante à votre `pom.xml` fichier :  

```xml
<dependency>
    <groupId>com.microsoft.edge</groupId>
    <artifactId>msedge-selenium-tools-java</artifactId>
    <version>[3.141.0,)</version>
</dependency>
```  

Le package Java est également disponible en téléchargement directement sur la [page Outils Selenium pour Microsoft Edge Releases.][GithubMicrosoftEdgeSeleniumToolsReleases]  

#### [JavaScript](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

Utilisez [npm pour][JavaScript|::ref4::|] installer [les packages edge-selenium-tools][JavaScriptSeleniumTools] et [selenium-webdriver.][JavaScriptSelenium]  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## Automatiser Microsoft Edge (Chromium) avec WebDriver  

Pour automatiser un navigateur à l’aide de WebDriver, vous devez d’abord démarrer une session WebDriver à l’aide de votre liaison de langue WebDriver préférée.  Une session est une instance en cours d’exécution unique d’un navigateur qui peut être contrôlée à l’aide de commandes WebDriver.  Le démarrage d’une session WebDriver lance une nouvelle instance de navigateur.  Le navigateur lancé reste ouvert jusqu’à la fermeture de la session WebDriver.  

Le contenu suivant vous aide à utiliser Selenium pour démarrer une session WebDriver avec Microsoft Edge \(Chromium\).  Vous pouvez exécuter ces exemples à l’aide de Selenium 3 ou 4.  Pour être utilisé avec Selenium 3, le package [Outils Selenium][GithubMicrosoftEdgeSeleniumTools] pour Microsoft Edge doit être installé.  

### Automatisation de Microsoft Edge (Chromium)  

Selenium utilise la `EdgeDriver` classe pour gérer une session Microsoft Edge \(Chromium\). Pour démarrer une session et automatiser Microsoft Edge \(Chromium\), créez un objet et passez-lui un objet avec la propriété `EdgeDriver` `EdgeOptions` définie sur `UseChromium` `true` .  

#### [C#](#tab/c-sharp/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [Python](#tab/python/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### [Java](#tab/java/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

La classe prend uniquement en charge Microsoft Edge (Chromium) et ne prend pas en charge `EdgeDriver` Microsoft Edge (EdgeHTML). Pour une utilisation de base, vous pouvez créer un `EdgeDriver` sans fournir `EdgeOptions` .  

```java
EdgeDriver driver = new EdgeDriver();
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
> Si votre administrateur informatique a définie la stratégie [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] sur , le pilote Microsoft Edge ne peut pas piloter Microsoft Edge (Chromium), car le pilote utilise `2` Microsoft Edge [DevTools.][DevtoolsIndex] [][MicrosoftDeveloperEdgeToolsWebdriver]  [Assurez-vous que la stratégie DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] est définie sur ou pour `0` `1` automatiser Microsoft Edge (Chromium).  

### Choix de binaires de navigateur spécifiques (chrome uniquement)  

Vous pouvez démarrer une session WebDriver avec des binaires Microsoft Edge \(Chromium\) spécifiques.  Par exemple, vous pouvez exécuter des tests à l’aide des canaux [d’aperçu De Microsoft Edge][MicrosoftedgeinsiderDownload] tels que Microsoft Edge Bêta.  

#### [C#](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [Python](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [Java](#tab/java/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.setBinary("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

EdgeDriver driver = new EdgeDriver(options);
```  

#### [JavaScript](#tab/javascript/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### Personnalisation du service de pilote Microsoft Edge  

#### [C#](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

Lorsqu’une instance de classe est créée à l’aide d’une classe, elle crée et lance la classe appropriée pour `EdgeDriver` `EdgeOptions` Microsoft Edge `EdgeDriverService` \(EdgeHTML\) ou Microsoft Edge \(Chromium\).  

Si vous souhaitez créer un , créez-en un configuré pour `EdgeDriverService` Microsoft Edge \(Chromium\) à l’aide de la `CreateChromiumService()` méthode.  Il peut vous être utile d’ajouter des personnalisations. Par exemple, le code suivant démarre une sortie détaillée du journal.  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
>Il n’est pas nécessaire de fournir `EdgeOptions` l’objet lors de la transmission `EdgeDriverService` à `EdgeDriver` l’instance.  La classe utilise les options par défaut pour `EdgeDriver` Microsoft Edge \(EdgeHTML\) ou Microsoft Edge \(Chromium\) en fonction du service que vous fournissez.  
> Toutefois, si vous souhaitez fournir les deux classes, assurez-vous que les deux sont configurés pour `EdgeDriverService` la même version de Microsoft `EdgeOptions` Edge.  Par exemple, il n’est pas possible d’utiliser une classe Microsoft Edge \(EdgeHTML\) par défaut et des propriétés `EdgeDriverService` Chromium dans la `EdgeOptions` classe.  La `EdgeDriver` classe envoie une erreur pour empêcher l’utilisation de différentes versions.  

#### [Python](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

Lorsque vous utilisez Python, `Edge` l’objet crée et gère le `EdgeService` .  Pour configurer le `EdgeService` , passez des arguments supplémentaires à l’objet `Edge` comme indiqué dans le code suivant.  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [Java](#tab/java/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

Utilisez la `createDefaultService()` méthode pour créer une configuration pour Microsoft Edge `EdgeDriverService` \(Chromium\). Les services de pilotes Java sont personnalisés à l’aide Java propriétés système. Par exemple, le code suivant utilise la `"webdriver.edge.verboseLogging"` propriété pour activer la sortie détaillée du journal.  

```java
System.setProperty("webdriver.edge.verboseLogging", "true");
EdgeDriverService service = EdgeDriverService.createDefaultService();
EdgeOptions options = new EdgeOptions();
EdgeDriver driver = new EdgeDriver(service, options);
```  

#### [JavaScript](#tab/javascript/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

Lorsque vous utilisez JavaScript, créez et configurez un avec `Service` la `ServiceBuilder` classe.  Si vous le souhaitez, vous pouvez transmettre l’objet à l’objet, qui `Service` `Driver` démarre \(et arrête\) le service pour vous.  
Pour configurer la `Service` méthode, exécutez une autre méthode dans la `ServiceBuilder` classe avant d’utiliser la `build()` méthode.  Passez ensuite le `service` paramètre en tant que paramètre dans la `Driver.createSession()` méthode.  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### Utiliser les Chromium-Specific options  

Si vous définissez la propriété sur , vous pouvez utiliser la classe pour accéder aux mêmes propriétés et méthodes spécifiques au Chromium qui sont utilisées lors de l’automatisation d’autres `UseChromium` `true` `EdgeOptions` navigateurs Chromium. [][WebdriverCapabilitiesEdgeOptions]  

#### [C#](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [Python](#tab/python/)  

<a id="using-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [Java](#tab/java/)  

<a id="using-chromium-specific-options-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.addArguments("headless");
options.addArguments("disable-gpu");
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
> Si la propriété est définie sur , vous ne pouvez pas utiliser les propriétés et méthodes `UseChromium` `true` pour Microsoft Edge \(EdgeHTML\).  

## Options d’installation WebDriver supplémentaires  

### Erzy  

Si vous utilisez [Lesy comme][Chocolatey] gestionnaire de package, installez le pilote Microsoft Edge en exécutant la commande suivante.  

```console
choco install selenium-chromium-edge-driver
```  

Pour plus d’informations, [voir Pilote Edge Selenium Chromium sur Le Site.][ChocolateyPackagesSeleniumChromiumEdgeDriver]  

### Docker  

Si vous utilisez [Docker][DockerHub], téléchargez une image pré-configurée avec Microsoft Edge \(Chromium\) et le pilote [Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] préinstallés en exécutant la commande suivante.  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

Pour plus d’informations, accédez au [conteneur msedgedriver sur Docker Hub.][DockerHubMsedgedriver]  

## Étapes suivantes

Pour en savoir plus sur WebDriver et comment écrire des tests WebDriver automatisés à l’aide de Selenium, accédez à la [documentation selenium.][SeleniumDocumentation]  

## Contacter l’équipe DevTools MicrosoftEdge  

L’équipe Microsoft Edge est impatiente de connaître vos commentaires sur l’utilisation de WebDriver, de Selenium et de Microsoft Edge.  Pour envoyer à l’équipe vos **** questions et commentaires, sélectionnez l’icône Envoyer des commentaires dans Microsoft Edge DevTools ou envoyez un tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="L’icône Envoyer des commentaires dans Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   Icône **Envoyer des commentaires** dans Microsoft Edge DevTools  
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
