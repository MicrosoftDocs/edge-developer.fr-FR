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
ms.openlocfilehash: 3865162b8227db2f0cfa051801a5de28ecf4b9d1
ms.sourcegitcommit: 3094c972532bc89dcb429d26880c873809fd1ab8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2021
ms.locfileid: "11599456"
---
# <a name="use-webdriver-chromium-for-test-automation"></a>Utiliser WebDriver (Chromium) pour tester l’automatisation  

WebDriver permet aux développeurs de créer des tests automatisés qui simulent l’interaction utilisateur.  Les tests et simulations WebDriver diffèrent des tests unitaires JavaScript des manières suivantes.  

*   Accède aux fonctionnalités et informations non disponibles pour JavaScript en cours d’exécution dans les navigateurs.  
*   Simule les événements utilisateur ou au niveau du système d’exploitation plus précisément.  
*   Gère plusieurs fenêtres, onglets et pages web en une seule session de test.  
*   Exécute plusieurs sessions de Microsoft Edge sur un ordinateur spécifique.  

## <a name="relationship-between-webdriver-and-other-software"></a>Relation entre WebDriver et d’autres logiciels

Pour automatiser Microsoft Edge webDriver afin de simuler l’interaction utilisateur, vous avez besoin de 3 composants :

*  Microsoft Edge
*  Microsoft Edge Driver
*  Une infrastructure de test WebDriver, telle que Selenium

La relation fonctionnelle entre WebDriver, Microsoft Edge Driver, Selenium et Internet Explorer Driver est la suivante.

| Technologie | Rôle |
|---|---|
| WebDriver | Norme W3C pour un protocole de câblage de plateforme et linguistiquement neutre.  Ce protocole permet aux programmes hors processus d’indiquer à distance le comportement des navigateurs web. |
| Microsoft Edge Driver | Implémentation de Microsoft du protocole WebDriver spécifiquement pour Microsoft Edge. Test authors write tests that use WebDriver commands that Microsoft Edge Driver receives. Microsoft Edge Le pilote est alors chargé de communiquer cette commande au navigateur. |
| Selenium | Infrastructure de test WebDriver populaire que les auteurs de test utilisent pour écrire des tests de bout en bout et automatiser les navigateurs. Le selenium peut être utilisé sur n’importe quelle plateforme et est disponible dans Java, Python, C#, Ruby et JavaScript. |
| Pilote Internet Explorer | Implémentation du protocole WebDriver spécifiquement pour Internet Explorer. Ce produit est maintenu par le projet Selenium. Pour exécuter des tests de bout en bout hérités pour Internet Explorer, nous vous recommandons d’utiliser pilote Internet Explorer. |

Les sections suivantes décrivent comment commencer avec WebDriver pour Microsoft Edge \(Chromium\).  

## <a name="install-microsoft-edge-chromium"></a>Installer Microsoft Edge (Chromium)  

Veillez à installer [Microsoft Edge (Chromium)][MicrosoftEdge].  Pour confirmer que vous avez installé Microsoft Edge \(Chromium\), accédez à et vérifiez que le numéro de version est `edge://settings/help` la version 75 ou ultérieure.  

## <a name="download-microsoft-edge-driver"></a>Télécharger Microsoft Edge Driver  

Pour commencer à automatiser les tests, utilisez les étapes suivantes pour vous assurer que la version WebDriver que vous installez correspond à la version de votre navigateur.  

1.  Recherchez votre version de Microsoft Edge.  
    1.  Naviguez vers`edge://settings/help` .  
        
        :::image type="complex" source="./media/microsoft-edge-version.msft.png" alt-text="Numéro de build Microsoft Edge le 15 avril 2021" lightbox="./media/microsoft-edge-version.msft.png":::
           Numéro de build Microsoft Edge le 15 avril 2021  
        :::image-end:::  
        
1.  Accédez à [Microsoft Edge pilote .][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]  
1.  Accédez à **Obtenir la dernière version.**  
1.  Choisissez la version du canal qui correspond à votre numéro de version de Microsoft Edge.  
    
    :::image type="complex" source="./media/microsoft-edge-driver-install.msft.png" alt-text="Section Obtenir la dernière version de la page web Microsoft Edge Driver" lightbox="./media/microsoft-edge-driver-install.msft.png":::
       Section **Obtenir la dernière version** sur la page web Microsoft Edge [pilote][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]  
    :::image-end:::  
    
    <!--  
    > [!NOTE] 
    > For more information about test automation using Microsoft Edge \(EdgeHTML\), navigate to [Microsoft Edge Driver for Microsoft Edge (EdgeHTML)][Webdriver].  
    -->  
    
## <a name="choose-a-webdriver-language-binding"></a>Choisir une liaison de langue WebDriver  

Le dernier composant que vous devez télécharger est un pilote client propre à une langue pour traduire votre code \(Python, Java, C\#, Ruby, JavaScript\) en commandes que le pilote Microsoft Edge exécute dans Microsoft Edge \(Chromium\).  

[Téléchargez la liaison de langue WebDriver de votre choix.][SeleniumDownloads]  L’Microsoft Edge recommande [Selenium 4.0.0-beta2][NugetPackagesSeleniumWebdriver400beta02] ou version ultérieure, car il prend en charge Microsoft Edge \(Chromium\).  Toutefois, vous pouvez contrôler Microsoft Edge \(Chromium\) dans toutes les versions antérieures de Selenium, y compris la version stable actuelle de Selenium 3.  

> [!IMPORTANT]
> Si vous avez précédemment automatisé ou testé Microsoft Edge \(Chromium\) et des classes, votre code WebDriver ne s’exécute pas sur Microsoft Edge `ChromeDriver` `ChromeOptions` version 80 ou ultérieure.  Pour résoudre le problème, mettez à jour vos tests pour utiliser la classe et `EdgeOptions` téléchargez [Microsoft Edge pilote][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].  

### <a name="using-selenium-4"></a>Utilisation de Selenium 4

Selenium 4 dispose d’une prise en charge intégrée des Microsoft Edge (Chromium).  Pour installer Selenium 4, accédez à [l’installation des bibliothèques Selenium.][SeleniumInstallingLibraries]

Lorsque vous utilisez Selenium 4, vous n’avez pas besoin d’utiliser les outils Selenium pour Microsoft Edge.  Les outils Selenium pour Microsoft Edge uniquement pour le selenium 3.  Si vous essayez d’utiliser Selenium 4 avec les outils Selenium pour Microsoft Edge et que vous essayez de créer une instance, vous obtenez `EdgeDriver` l’erreur suivante : `System.MissingMethodException: 'Method not found: 'OpenQA.Selenium.Remote.DesiredCapabilities OpenQA.Selenium.DriverOptions.GenerateDesiredCapabilities(Boolean)'`  

Si vous utilisez Selenium 4 et obtenez cette erreur, supprimez votre projet et assurez-vous que vous utilisez l’officiel et les classes de `Microsoft.Edge.SeleniumTools` l’espace `EdgeOptions` `EdgeDriver` de `OpenQA.Selenium.Edge` noms.

### <a name="using-selenium-3"></a>Utilisation de Selenium 3  

Si vous utilisez déjà [Selenium 3,][|::ref1::|]vous avez peut-être des tests de navigateur existants et souhaitez ajouter une couverture pour Microsoft Edge \(Chromium\) sans modifier votre version de Selenium.  Pour utiliser [Selenium 3][|::ref2::|] afin d’écrire des tests automatisés pour Microsoft Edge \(EdgeHTML\) et Microsoft Edge \(Chromium\), installez le package [Outils Selenium][GithubMicrosoftEdgeSeleniumTools] pour Microsoft Edge pour utiliser le pilote mis à jour.  Les classes incluses dans les outils sont entièrement compatibles avec les `EdgeDriver` `EdgeDriverService` équivalents intégrés dans Selenium 4.  

Utilisez les étapes suivantes pour ajouter les outils [Selenium pour Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] [et Selenium 3][|::ref3::|] à votre projet.  

#### [<a name="c"></a>C#](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

Ajoutez [les packages Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] et [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] à votre projet .NET à l’aide NuGet [CLI][NugetCLI] ou [Visual Studio][VisualStudio].  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="selenium-tools-install"></a>  

Utilisez [pip][PythonPip] pour installer [les packages msedge-selenium-tools][PythonSeleniumTools] et [selenium.][PythonSelenium]  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="selenium-tools-install"></a>  

Si votre Java utilise Maven, copiez et collez la dépendance suivante dans votre fichier pour ajouter `pom.xml` [msedge-selenium-tools-java][SonatypeMavenRepositorySearch].  

```xml
<dependency>
    <groupId>com.microsoft.edge</groupId>
    <artifactId>msedge-selenium-tools-java</artifactId>
    <version>[3.141.0,)</version>
</dependency>
```  

Le package Java est également disponible en téléchargement direct sur la [page Outils Selenium Microsoft Edge releases.][GithubMicrosoftEdgeSeleniumToolsReleases]  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

Utilisez [npm][JavaScript|::ref4::|] pour installer [les packages edge-selenium-tools][JavaScriptSeleniumTools] et [selenium-webdriver.][JavaScriptSelenium]  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## <a name="automate-microsoft-edge-chromium-with-webdriver"></a>Automatiser Microsoft Edge (Chromium) avec WebDriver  

Pour automatiser un navigateur à l’aide de WebDriver, vous devez d’abord démarrer une session WebDriver à l’aide de votre liaison de langue WebDriver préférée.  Une session est une instance en cours d’exécution unique d’un navigateur contrôlée à l’aide des commandes WebDriver.  Démarrez une session WebDriver pour lancer une nouvelle instance de navigateur.  L’instance de navigateur lancée reste ouverte jusqu’à la fermeture de la session WebDriver.  

Le contenu suivant vous aide à utiliser Selenium pour démarrer une session WebDriver avec Microsoft Edge \(Chromium\).  Vous pouvez exécuter les exemples à l’aide de Selenium 3 ou 4.  Pour être utilisé avec Selenium 3, le package [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package doit être installé.  

### <a name="automate-microsoft-edge-chromium"></a>Automatiser Microsoft Edge (Chromium)  

Selenium utilise la `EdgeDriver` classe pour gérer une session Microsoft Edge \(Chromium\).  Pour démarrer une session et automatiser Microsoft Edge \(Chromium\), créez un objet et passez-lui un objet avec la propriété `EdgeDriver` `EdgeOptions` définie sur `UseChromium` `true` .  

#### [<a name="c"></a>C#](#tab/c-sharp/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options = options)
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

La classe prend uniquement en charge Microsoft Edge \(Chromium\) et ne prend pas en `EdgeDriver` charge Microsoft Edge \(EdgeHTML\).  Pour une utilisation de base, vous pouvez créer un `EdgeDriver` sans fournir `EdgeOptions` .  

```java
EdgeDriver driver = new EdgeDriver();
```  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> Si votre administrateur informatique a définie la stratégie [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] sur , le pilote Microsoft Edge ne peut pas conduire Microsoft Edge \(Chromium\), car le pilote utilise Microsoft Edge `2` [DevTools][DevtoolsIndex]. [][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]  [Assurez-vous que la stratégie DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] est définie sur ou pour automatiser Microsoft Edge `0` `1` (Chromium).  

### <a name="choose-specific-browser-binaries-chromium-only"></a>Choisir des binaires de navigateur spécifiques (Chromium uniquement)  

Vous pouvez démarrer une session WebDriver avec des Microsoft Edge \(Chromium\) spécifiques.  Par exemple, vous pouvez exécuter des tests à [l’aide des canaux Microsoft Edge prévisualisation][MicrosoftedgeinsiderDownload] tels que Microsoft Edge Beta.  

#### [<a name="c"></a>C#](#tab/c-sharp/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options = options)
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.setBinary("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

EdgeDriver driver = new EdgeDriver(options);
```  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <a name="customize-the-microsoft-edge-driver-service"></a>Personnaliser le service Microsoft Edge pilotes de service  

#### [<a name="c"></a>C#](#tab/c-sharp/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Lorsque vous utilisez la classe pour créer une instance de classe, elle crée et lance la classe appropriée pour `EdgeOptions` `EdgeDriver` Microsoft Edge `EdgeDriverService` \(EdgeHTML\) ou Microsoft Edge \(Chromium\).  

Si vous souhaitez créer un , utilisez la méthode pour en créer une configurée `EdgeDriverService` `CreateChromiumService()` pour Microsoft Edge \(Chromium\).  La `CreateChromiumService()` méthode est utile lorsque vous devez ajouter des personnalisations.  Par exemple, le code suivant démarre une sortie détaillée du journal.  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
>Vous n’avez pas besoin de fournir `EdgeOptions` l’objet lorsque vous passez `EdgeDriverService` à `EdgeDriver` l’instance.  La classe utilise les options par défaut pour `EdgeDriver` Microsoft Edge \(EdgeHTML\) ou Microsoft Edge \(Chromium\) en fonction du service que vous fournissez.  
> Toutefois, si vous souhaitez fournir à la fois et des classes, assurez-vous que les deux sont configurés pour la `EdgeDriverService` `EdgeOptions` même version de Microsoft Edge.  Par exemple, vous pouvez utiliser une classe Microsoft Edge \(EdgeHTML\) et Chromium `EdgeDriverService` propriétés dans la `EdgeOptions` classe.  La `EdgeDriver` classe envoie une erreur pour empêcher l’utilisation de différentes versions.  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Lorsque vous utilisez Python, `Edge` l’objet crée et gère le `EdgeService` .  Pour configurer l’objet, passez des arguments supplémentaires à l’objet, comme `EdgeService` indiqué dans le code `Edge` suivant.  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Utilisez la méthode pour créer un Microsoft Edge `createDefaultService()` `EdgeDriverService` \(Chromium\).  Utilisez Java système pour personnaliser les services de pilotes dans Java.  Par exemple, le code suivant utilise la `"webdriver.edge.verboseLogging"` propriété pour activer la sortie détaillée du journal.  

```java
System.setProperty("webdriver.edge.verboseLogging", "true");
EdgeDriverService service = EdgeDriverService.createDefaultService();
EdgeOptions options = new EdgeOptions();
EdgeDriver driver = new EdgeDriver(service, options);
```  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Lorsque vous utilisez JavaScript, créez et configurez un avec `Service` la `ServiceBuilder` classe.  Si vous le souhaitez, vous pouvez transmettre l’objet à l’objet, qui `Service` `Driver` démarre \(et arrête\) le service pour vous.  
Pour configurer la `Service` méthode , exécutez une autre méthode dans la `ServiceBuilder` classe avant d’utiliser la `build()` méthode.  Passez ensuite le `service` paramètre en tant que paramètre dans la `Driver.createSession()` méthode.  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### <a name="use-chromium-specific-options"></a>Utiliser les Chromium-Specific options  

Si vous définissez la propriété sur , vous pouvez utiliser la classe pour accéder aux mêmes propriétés et méthodes propres à Chromium que lorsque vous automatisez d’autres Chromium `UseChromium` `true` `EdgeOptions` navigateurs. [][WebdriverCapabilitiesEdgeOptions]  

#### [<a name="c"></a>C#](#tab/c-sharp/)  

<a id="use-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="use-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="use-chromium-specific-options-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

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

## <a name="other-webdriver-installation-options"></a>Autres options d’installation webDriver  

### <a name="docker"></a>Docker  

Si vous utilisez [Docker,][DockerHub]exécutez la commande suivante pour télécharger une image pré-configurée avec Microsoft Edge \(Chromium\) et [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] préinstallés.  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

Pour plus d’informations, accédez au conteneur [msedgedriver sur Docker Hub.][DockerHubMsedgedriver]  

## <a name="testing-internet-explorer"></a>Test d’Internet Explorer

Même si Microsoft Edge prend en charge le mode IE, vous ne pouvez pas utiliser le pilote Microsoft Edge avec Microsoft Edge pour tester des sites en mode IE.  Pour tester les sites qui nécessitent Internet Explorer, utilisez [Pilote Internet Explorer][GithubSeleniumHqWikiIEDriver] avec Internet Explorer.

## <a name="next-steps"></a>Étapes suivantes  

Pour plus d’informations sur WebDriver et comment écrire des tests WebDriver automatisés à l’aide de Selenium, accédez à la [documentation selenium.][SeleniumDocumentation]  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

L’Microsoft Edge est enthousiaste à l’écoute de vos commentaires sur l’utilisation de WebDriver, selenium et Microsoft Edge.  Pour envoyer à l’équipe vos **** questions et [commentaires,][TwitterTweetEdgeDevTools]sélectionnez l’icône Envoyer des commentaires dans le Microsoft Edge DevTools ou envoyez un tweet @EdgeDevTools .  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="L’icône Envoyer des commentaires dans Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   Icône **Envoyer des commentaires** dans le Microsoft Edge DevTools  
:::image-end:::  

<!-- links -->  

[DevtoolsIndex]: ../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  
[WebdriverCapabilitiesEdgeOptions]: ./capabilities-edge-options.md "Fonctionnalités et fonctionnalités EdgeOptions | Documents Microsoft"  

<!--[Webdriver]: /archive/microsoft-edge/legacy/developer/webdriver/index "WebDriver (EdgeHTML) | Microsoft Docs"  -->  

[DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability - Microsoft Edge - Stratégies | Documents Microsoft"  

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
[SeleniumDownloads]: https://selenium.dev/downloads "Téléchargements | Selenium"  
[SeleniumInstallingLibraries]: https://www.selenium.dev/documentation/en/selenium_installation/installing_selenium_libraries "Installation des bibliothèques Selenium | Selenium"

[SonatypeMavenRepositorySearch]: https://search.maven.org/artifact/com.microsoft.edge/msedge-selenium-tools-java/3.141.0/jar "Recherche dans le référentiel central Sonatype Maven | com.microsoft.edge:msedge-selenium-tools-java"

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publier un tweet"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver | W3C"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Navigateur sans | Wikipedia"  
