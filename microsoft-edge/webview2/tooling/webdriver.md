---
description: Automatiser et tester le contrôle WebView2 à l’aide du pilote Microsoft Edge
title: Automatisation et test de WebView2 avec le pilote Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Edge, ICoreWebView2, ICoreWebView2Controller, sélénium, pilote Microsoft Edge
ms.openlocfilehash: acee8c1f791fdd4a2604b8f3bfa7664548a164d1
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653293"
---
# Automatisation et test de WebView2 avec le pilote Microsoft Edge

Dans la mesure où WebView2 utilise la plateforme Web de chrome, les développeurs WebView2 peuvent tirer parti d’outils Web standard pour le débogage et l’automatisation. L’un de ces outils est le sélénium, qui implémente l’API [WebDriver](https://www.w3.org/TR/webdriver2/) W3C, qui peut être utilisée pour créer des tests automatisés qui simulent les interactions utilisateur.

Voici comment faire:

## Étape 1: Télécharger l’exemple WebView2API

Si vous n’avez pas de projet WebView2 existant, téléchargez notre [exemple d’application WebView2API](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample#webview2-api-sample), un exemple complet du SDK WebView2 le plus récent. Vérifiez que vous avez satisfait ces [conditions préalables](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample#prerequisites).

Une fois que vous avez cloné le référentiel samples, générez le projet dans Visual Studio. Il doit ressembler à ce qui suit:

![texte de remplacement](../media/webdriver/sample-app.png)

## Étape 2: installer le pilote Microsoft Edge

Suivez les instructions pour installer le [pilote Microsoft Edge](https://docs.microsoft.com/microsoft-edge/webdriver-chromium#download-microsoft-edge-driver) le pilote spécifique au navigateur requis par sélénium pour automatiser et tester WebView2.

Il est important de s’assurer que la version du pilote Microsoft Edge correspond à la version de Microsoft Edge utilisée par l’application. Pour que l’exemple WebView2API fonctionne, assurez-vous que votre version de Microsoft Edge est supérieure ou égale à la version prise en charge de notre dernière version du SDK trouvée [dans nos notes de publication](https://docs.microsoft.com/microsoft-edge/hosting/webview2/releasenotes). Pour savoir quelle version de Microsoft Edge vous utilisez actuellement, chargez `edge://settings/help` dans le navigateur.

## Étape 3: ajouter du sélénium à l’exemple WebView2API

À ce stade, vous devez avoir installé Microsoft Edge, créé un projet WebView2 et installé le pilote Microsoft Edge. Commençons par commencer par sélénium.

> [!NOTE]
> Sélénium prend en charge C#, Java, Python, JavaScript et Ruby. Ce guide sera toutefois en C#.

1. Commencez par créer un projet **.NET Framework C#** dans **Visual Studio**. Dans le coin inférieur droit, cliquez sur **suivant** pour continuer.

![texte de remplacement](../media/webdriver/new-project.png)

2. Donnez un **nom**à votre projet, enregistrez-le dans votre **emplacement**préféré, puis cliquez sur **créer**.

![texte de remplacement](../media/webdriver/app-create.png)

3. Un nouveau projet est créé. Ce guide présente l’intégralité du code dans le fichier **Program.cs** .

![texte de remplacement](../media/webdriver/start-app.png)

4. Nous allons maintenant ajouter **sélénium** au projet. Vous pouvez installer le sélénium via le **package NuGet. WebDriver de sélénium**.

Pour télécharger le **package NuGet. WebDriver du sélénium**, dans **Visual Studio**, survolez le **projet** , puis sélectionnez **Manage NuGet package**. L’écran suivant doit s’afficher:

![texte de remplacement](../media/webdriver/download-nuget.png)

5. Entrez **sélénium. WebDriver** dans la barre de recherche, cliquez sur **sélénium. WebDriver** à partir des résultats, et veillez à activer la case à cocher en regard de **inclure la version préliminaire**. Dans la fenêtre de droite, assurez-vous que la **version** est définie pour **Installer 4.0.0-alpha04** ou version ultérieure, puis cliquez sur **installer**. NuGet télécharge sélénium sur votre ordinateur.

[En savoir plus sur le package NuGet. WebDriver de sélénium.](https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha04)

![texte de remplacement](../media/webdriver/nuget.png)

6. Pour utiliser **OpenQA. sélénium. Edge** , ajoutez l’instruction suivante: ```using OpenQA.Selenium.Edge;``` au début de **Program.cs**

```csharp
using OpenQA.Selenium.Edge;

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## Étape 4: piloter WebView2 avec sélénium et Microsoft EdgeDriver

1. Tout d’abord, créez l' `EdgeOptions` objet en copiant le code ci-dessous:

```csharp
static void Main(string[] args)
{
    // EdgeOptions() requires using OpenQA.Selenium.Edge
    // Construct EdgeOptions with is_legacy = false and the string "webview2"
    EdgeOptions edgeOptions = new EdgeOptions(false, "webview2");
```

L' `EdgeOptions` objet utilise deux paramètres:
\
    **Paramètres**
    1. `is_legacy`: défini sur `false` , qui indique au sélénium que vous dirigez le nouveau navigateur Microsoft Edge basé sur le chrome.
    2. `"webview2"`: chaîne indiquant au sélénium que vous entrainez **WebView2**

2. Ensuite, définissez `edgeOptions.BinaryLocation` le chemin d’accès du fichier exécutable de votre projet WebView2, créez une chaîne appelée `msedgedriverDir` qui fournit le chemin d’accès du fichier à l’endroit où vous avez installé le [pilote Microsoft Edge](https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads), puis créez une chaîne appelée `msedgedriverExe` pour stocker le nom du fichier exécutable du pilote Microsoft Edge. Par défaut, l’exécutable est appelé `"msedgedriver.exe"` . Utilisez ces deux chaînes pour créer l' `EdgeDriverService` objet, comme illustré ci-dessous. Enfin, créez l' `EdgeDriver` objet à l’aide `EdgeDriverService` de et `EdgeOptions` .

Vous pouvez copier et coller le code suivant `edgeOptions` . Veillez à spécifier les chemins d’accès appropriés au fichier exécutable de votre projet et au fichier exécutable du pilote Microsoft Edge sur votre ordinateur.

```csharp
    //Set the BinaryLocation to the filepath of the WebView2API Sample's executable
    edgeOptions.BinaryLocation = @"C:\path\to\your\webview2\project.exe";

    //Set msedgedriverDir to the filepath of the directory housing msedgedriver.exe
    string msedgedriverDir = @"C:\path\to\your\msededriver.exe's\directory";

    //Set msedgedriverExe to the name of the Edge Driver. By default it is:
    string msedgedriverExe = @"msedgedriver.exe";

    // Construct EdgeDriverService with is_legacy = false  
    EdgeDriverService service = EdgeDriverService.CreateDefaultService(msedgedriverDir, msedgedriverExe, false);

    EdgeDriver e = new EdgeDriver(service, edgeOptions);
```

3. À présent, **EdgeDriver** est configuré pour piloter **WebView2** dans votre projet. Par exemple, si vous utilisez l' **exemple WebView2API**, vous pouvez **accéder** à à l’aide d’un <https://microsoft.com> appel ```e.Url = @"https://www.microsoft.com";``` . Vous **pouvez regarder le** pilote d' **WebView2** en définissant un point d’arrêt sur cette ligne et en exécutant le projet.

```csharp
    //The following will Navigate the WebView2API Sample from bing.com to microsoft.com
    e.Url = @"https://www.microsoft.com";

    //This exits the edge driver
    e.Quit();
}
```

![texte de remplacement](../media/webdriver/microsoft.png)

Félicitations! Vous avez correctement automatisé un projet WebView2 et WebView2 piloté par le biais du pilote sélénium et Microsoft Edge.

## Étapes suivantes

Pour en savoir plus:

- Consultez la [documentation du sélénium](https://www.selenium.dev/documentation/en/webdriver/) pour obtenir un aperçu complet des API de sélénium disponibles pour le pilotage de WebView2 ou de Microsoft Edge (chrome)
- En savoir plus sur le contrôle [WebView2](https://docs.microsoft.com/microsoft-edge/hosting/webview2) et son utilisation lors de l’incorporation de contenu Web dans votre application native
- Pour en savoir plus sur l’automatisation de Microsoft Edge (chrome), consultez [la documentation relative au pilote Microsoft Edge](https://docs.microsoft.com/microsoft-edge/webdriver-chromium) .

## Contacter l’équipe WebView2  

Aidez-nous à créer une expérience WebView2 plus riche en partageant vos commentaires! Consultez notre page de [Commentaires référentiel Samples](https://github.com/MicrosoftEdge/WebViewFeedback) pour envoyer des demandes de fonctionnalité ou des rapports de bogues, ou pour rechercher des problèmes connus.
