---
description: Découvrez comment tester votre site web ou votre application dans Microsoft Edge ou automatiser le navigateur avec WebDriver
title: Utiliser WebDriver (Chromium) pour tester l’automatisation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, développement web, html, css, javascript, développeur, webdriver, selenium, test, outils, automatisation, test
ms.openlocfilehash: b3b8a4ef2174c7f313fe9ee71bedbdf5e2f9b771
ms.sourcegitcommit: f95812c4e1b7277f67c6c4891be2779cc1b5bdf1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/18/2021
ms.locfileid: "11343789"
---
# Utiliser WebDriver (Chromium) pour tester l’automatisation  

WebDriver permet aux développeurs de créer des tests automatisés qui simulent l’interaction utilisateur.  Les tests et simulations WebDriver diffèrent des tests unitaires JavaScript des manières suivantes.  

*   Accède aux fonctionnalités et informations non disponibles pour JavaScript s’exécutant dans les navigateurs.  
*   Simule les événements utilisateur ou au niveau du système d’exploitation plus précisément.  
*   Gère plusieurs fenêtres, onglets et pages web en une seule session de test.  
*   Exécute plusieurs sessions de Microsoft Edge sur un ordinateur spécifique.  
    
La section suivante décrit comment commencer avec WebDriver pour Microsoft Edge \(Chromium\).  

## Installer Microsoft Edge (Chromium)  

Assurez-vous [d’installer Microsoft Edge (Chromium).][MicrosoftEdge]  Pour confirmer que Microsoft Edge \(Chromium\) est installé, accédez à et vérifiez que le numéro de version est `edge://settings/help` la version 75 ou ultérieure.  

## Télécharger le pilote Microsoft Edge  

Pour commencer à automatiser les tests, utilisez les étapes suivantes pour vous assurer que la version WebDriver que vous installez correspond à la version de votre navigateur.  

1.  Pour afficher la version de Microsoft Edge, accédez à `edge://settings/help` .  
    
    :::image type="complex" source="./media/microsoft-edge-version.msft.png" alt-text="Numéro de build de Microsoft Edge Canary le 10 février 2021" lightbox="./media/microsoft-edge-version.msft.png":::
       Numéro de build de Microsoft Edge Canary le 10 février 2021  
    :::image-end:::  
    
1.  Accédez [à Pilote Microsoft Edge,][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]sous la section **Téléchargements,** et téléchargez le WebDriver qui correspond au numéro de version de Microsoft Edge.  
    
    :::image type="complex" source="./media/microsoft-edge-driver-install.msft.png" alt-text="La section Téléchargements sur le pilote Microsoft Edge" lightbox="./media/microsoft-edge-driver-install.msft.png":::
       La section **Téléchargements** sur [le pilote Microsoft Edge][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]  
    :::image-end:::  
    
    <!--  
    > [!NOTE] 
    > For more information about test automation using Microsoft Edge \(EdgeHTML\), navigate to [Microsoft Edge Driver for Microsoft Edge \(EdgeHTML\)][Webdriver].  
    -->  

## Choisir une liaison de langue WebDriver  

Le dernier composant que vous devez télécharger est un pilote client spécifique à la langue pour traduire votre code \(Python, Java, C\#, Ruby, JavaScript\) en commandes que le pilote Microsoft Edge exécute dans Microsoft Edge \(Chromium\).  

[Téléchargez la liaison de langue WebDriver de votre choix.][SeleniumDownloads]  L’équipe Microsoft Edge recommande [Selenium 4.00-alpha07][NugetPackagesSeleniumWebdriver400alpha07] ou version ultérieure, car elle prend en charge Microsoft Edge \(Chromium\).  Toutefois, vous pouvez contrôler Microsoft Edge \(Chromium\) dans toutes les versions antérieures de Selenium, y compris la version stable actuelle de Selenium 3.  

> [!IMPORTANT]
> Si vous avez précédemment automatisé ou testé l’utilisation et les classes de Microsoft Edge \(Chromium\), votre code WebDriver ne s’exécute pas sur `ChromeDriver` `ChromeOptions` Microsoft Edge Version 80 ou ultérieure.  Pour résoudre le problème, mettez à jour vos tests pour utiliser la `EdgeOptions` classe et téléchargez [le pilote Microsoft Edge.][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]  

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

Si votre Java utilise Maven, copiez et collez la dépendance suivante dans votre fichier pour ajouter `pom.xml` [msedge-selenium-tools-java][SonatypeMavenRepositorySearch].  

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

Pour automatiser un navigateur à l’aide de WebDriver, vous devez d’abord démarrer une session WebDriver à l’aide de votre liaison de langue WebDriver préférée.  Une session est une instance en cours d’exécution unique d’un navigateur contrôlée à l’aide des commandes WebDriver.  Démarrez une session WebDriver pour lancer une nouvelle instance de navigateur.  L’instance de navigateur lancée reste ouverte jusqu’à la fermeture de la session WebDriver.  

Le contenu suivant vous aide à utiliser Selenium pour démarrer une session WebDriver avec Microsoft Edge \(Chromium\).  Vous pouvez exécuter les exemples à l’aide de Selenium 3 ou 4.  Pour être utilisé avec Selenium 3, le package [Outils Selenium][GithubMicrosoftEdgeSeleniumTools] pour Microsoft Edge doit être installé.  

### Automatiser Microsoft Edge (Chromium)  

Selenium utilise la `EdgeDriver` classe pour gérer une session Microsoft Edge \(Chromium\).  Pour démarrer une session et automatiser Microsoft Edge \(Chromium\), créez un objet et passez-lui un objet avec la propriété `EdgeDriver` `EdgeOptions` définie sur `UseChromium` `true` .  

#### [C#](#tab/c-sharp/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [Python](#tab/python/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### [Java](#tab/java/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

La classe prend uniquement en charge Microsoft Edge \(Chromium\) et ne prend pas en charge `EdgeDriver` Microsoft Edge \(EdgeHTML\).  Pour une utilisation de base, vous pouvez créer un `EdgeDriver` sans fournir `EdgeOptions` .  

```java
EdgeDriver driver = new EdgeDriver();
```  

#### [JavaScript](#tab/javascript/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> Si votre administrateur informatique a définie la stratégie [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] sur , le pilote Microsoft Edge ne peut pas conduire Microsoft Edge \(Chromium\), car le pilote utilise `2` [Microsoft Edge DevTools.][DevtoolsIndex] [][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]  [Assurez-vous que la stratégie DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] est définie sur ou pour `0` `1` automatiser Microsoft Edge (Chromium).  

### Choisir des binaires de navigateur spécifiques (chrome uniquement)  

Vous pouvez démarrer une session WebDriver avec des binaires Microsoft Edge \(Chromium\) spécifiques.  Par exemple, vous pouvez exécuter des tests à l’aide des canaux [d’aperçu De Microsoft Edge][MicrosoftedgeinsiderDownload] tels que Microsoft Edge Bêta.  

#### [C#](#tab/c-sharp/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [Python](#tab/python/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [Java](#tab/java/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.setBinary("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

EdgeDriver driver = new EdgeDriver(options);
```  

#### [JavaScript](#tab/javascript/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### Personnaliser le service de pilotes Microsoft Edge  

#### [C#](#tab/c-sharp/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Lorsque vous utilisez la classe pour créer une instance de classe, elle crée et lance la classe appropriée pour `EdgeOptions` `EdgeDriver` Microsoft Edge `EdgeDriverService` \(EdgeHTML\) ou Microsoft Edge \(Chromium\).  

Si vous souhaitez créer un , utilisez la méthode pour en créer une configurée pour `EdgeDriverService` `CreateChromiumService()` Microsoft Edge \(Chromium\).  La `CreateChromiumService()` méthode est utile lorsque vous devez ajouter des personnalisations.  Par exemple, le code suivant démarre une sortie détaillée du journal.  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
>Vous n’avez pas besoin de fournir `EdgeOptions` l’objet lorsque vous passez `EdgeDriverService` à `EdgeDriver` l’instance.  La classe utilise les options par défaut pour `EdgeDriver` Microsoft Edge \(EdgeHTML\) ou Microsoft Edge \(Chromium\) en fonction du service que vous fournissez.  
> Toutefois, si vous souhaitez fournir les deux classes, assurez-vous que les deux sont configurés pour la `EdgeDriverService` même version de Microsoft `EdgeOptions` Edge.  Par exemple, vous pouvez utiliser une classe Microsoft Edge \(EdgeHTML\) par défaut et des propriétés `EdgeDriverService` Chromium dans la `EdgeOptions` classe.  La `EdgeDriver` classe envoie une erreur pour empêcher l’utilisation de différentes versions.  

#### [Python](#tab/python/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Lorsque vous utilisez Python, `Edge` l’objet crée et gère le `EdgeService` .  Pour configurer l’objet, passez des arguments supplémentaires à l’objet, comme `EdgeService` indiqué dans le code `Edge` suivant.  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [Java](#tab/java/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Utilisez la `createDefaultService()` méthode pour créer une configuration pour Microsoft Edge `EdgeDriverService` \(Chromium\).  Utilisez Java système pour personnaliser les services de pilotes dans Java.  Par exemple, le code suivant utilise la `"webdriver.edge.verboseLogging"` propriété pour activer la sortie détaillée du journal.  

```java
System.setProperty("webdriver.edge.verboseLogging", "true");
EdgeDriverService service = EdgeDriverService.createDefaultService();
EdgeOptions options = new EdgeOptions();
EdgeDriver driver = new EdgeDriver(service, options);
```  

#### [JavaScript](#tab/javascript/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Lorsque vous utilisez JavaScript, créez et configurez un avec `Service` la `ServiceBuilder` classe.  Si vous le souhaitez, vous pouvez transmettre l’objet à l’objet, qui `Service` `Driver` démarre \(et arrête\) le service pour vous.  
Pour configurer la `Service` méthode , exécutez une autre méthode dans la `ServiceBuilder` classe avant d’utiliser la `build()` méthode.  Passez ensuite le `service` paramètre en tant que paramètre dans la `Driver.createSession()` méthode.  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### Utiliser les Chromium-Specific options  

Si vous définissez la propriété sur , vous pouvez utiliser la classe pour accéder aux mêmes propriétés et méthodes spécifiques à Chromium que lorsque vous automatisez d’autres `UseChromium` `true` `EdgeOptions` navigateurs Chromium. [][WebdriverCapabilitiesEdgeOptions]  

#### [C#](#tab/c-sharp/)  

<a id="use-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [Python](#tab/python/)  

<a id="use-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [Java](#tab/java/)  

<a id="use-chromium-specific-options-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

#### [JavaScript](#tab/javascript/)  

<a id="use-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

* * *  

> [!NOTE]
> Si la propriété est définie sur , vous ne pouvez pas utiliser les propriétés et méthodes `UseChromium` `true` pour Microsoft Edge \(EdgeHTML\).  

## Autres options d’installation webDriver  

### Erzy  

Si vous utilisez [Contrôley comme][Chocolatey] gestionnaire de package, exécutez la commande suivante pour installer le pilote Microsoft Edge.  

```console
choco install selenium-chromium-edge-driver
```  

Pour plus d’informations, [accédez au pilote Edge Selenium Chromium sur Le Site.][ChocolateyPackagesSeleniumChromiumEdgeDriver]  

### Docker  

Si vous utilisez [Docker,][DockerHub]exécutez la commande suivante pour télécharger une image pré-configurée avec Microsoft Edge \(Chromium\) et le pilote [Microsoft Edge][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] préinstallé.  

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

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "WebDriver | Développeur Microsoft"  

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
[SeleniumDocumentation]: https://www.selenium.dev/documentation "Le projet Selenium Browser Automation | Documentation pour Selenium"  
[SeleniumDownloads]: https://selenium.dev/downloads "Téléchargements | Selenium"  

[SonatypeMavenRepositorySearch]: https://search.maven.org/artifact/com.microsoft.edge/msedge-selenium-tools-java/3.141.0/jar "sonatype Maven Central Repository Search | com.microsoft.edge:msedge-selenium-tools-java"

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publier un tweet"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver | W3C"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Navigateur sans | Wikipedia"  
