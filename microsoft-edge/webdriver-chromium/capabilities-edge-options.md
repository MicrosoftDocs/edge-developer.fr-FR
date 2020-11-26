---
description: Référence pour les fonctionnalités du WebDriver et les options spécifiques à Microsoft Edge prises en charge par EdgeDriver (chrome).
title: Fonctionnalités et EdgeOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, développement Web, html, CSS, JavaScript, développeur, Web Driver, sélénium, test, outils, Automation, test
ms.openlocfilehash: 1f6dca1b7ce3eb4fab3aaaab6450eee7cbf3eae5
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "11192245"
---
# Fonctionnalités et EdgeOptions  

Les fonctionnalités sont des options que vous pouvez utiliser pour personnaliser et configurer une `EdgeDriver` session.  Pour démarrer une `EdgeDriver` session, accédez à [pilotage de Microsoft Edge][DrivingEdgeWebDriverIndex].  Cet article répertorie toutes les fonctionnalités prises en charge par [Microsoft Edge][DownloadEdgeWebDriverIndex] et des détails supplémentaires concernant la transmission des fonctionnalités à une `EdgeDriver` session.  

Les liaisons de langue de Web Driver fournissent des moyens de passer des fonctions `EdgeDriver` .  Le mécanisme exact dépend de la [liaison de langue choisie][ChooseLanguageBindingWebDriverIndex].  Dans le [sélénium][SeleniumMain], les fonctionnalités sont fournies via la `EdgeOptions` classe.  

## Utilisation de la classe EdgeOptions  

Créez une instance de `EdgeOptions` qui dispose de méthodes pratiques pour définir les fonctionnalités propres à Microsoft Edge.  Une fois que vous avez configuré l' `EdgeOptions` objet, transmettez- `EdgeOptions` le au `EdgeDriver` constructeur.  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddExtensions("/path/to/extension.crx");
var driver = new EdgeDriver(options);
```  

Pour les fonctionnalités qui n’ont pas encore de méthode pratique, utilisez la `AddAdditionalCapability` méthode.  Vous devez connaître le nom de la fonctionnalité et le type de valeur acceptée.  Pour passer en revue la liste complète, accédez à l' [objet EdgeOptions](#edgeoptions-object).  

```csharp
options.AddAdditionalCapability("wdpAddress", "remotehost:50080");
```  

## Fonctionnalités reconnues  

Pour plus d’informations sur les fonctionnalités standard qui `EdgeDriver` acceptent, accédez à la [documentation du sélénium][SharedCapabilitiesSeleniumDocumentation] et à la [norme du World Driver W3C][CapabilitiesW3cWebdriver].  Cet article répertorie uniquement les fonctionnalités propres à Microsoft Edge.  

## Objet EdgeOptions  

La plupart des fonctionnalités propres à Microsoft Edge sont exposées par le biais de l' `EdgeOptions` objet.  Dans certaines langues, les fonctionnalités sont implémentées par la `EdgeOptions` classe.  Dans d’autres langues, les fonctionnalités sont stockées sous le `ms:edgeOptions` dictionnaire dans `DesiredCapabilities` .  

| Fonctionnalité | Type | Valeur par défaut | Détails |  
|:--- |:--- |:--- |:--- |  
| args | liste de chaînes |  | Liste des arguments de ligne de commande à utiliser lors du démarrage de Microsoft Edge.  Les arguments ayant une valeur associée doivent être séparés par un `=` signe (par exemple, `['start-maximized', 'user-data-dir=/tmp/temp_profile']` \).  |  
| binaire | chaîne |  | Chemin d’accès au fichier binaire Microsoft Edge à utiliser \ (sur macOS, le chemin doit être le fichier binaire réel et non l’application uniquement.  par exemple, `/Applications/Microsoft Edge.app/Contents/MacOS/Microsoft Edge` \).  |  
| variable | liste de chaînes |  | Liste d’extensions à installer au démarrage.  Chaque élément de la liste doit être une extension compactée en base 64 encodée \ ( `.crx` \).  |  
| localState | dictionnaire |  | Dictionnaire avec chaque entrée composée du nom de la préférence et de sa valeur.  Les préférences sont appliquées au fichier de l’état local dans le dossier données utilisateur.  |  
| pref | dictionnaire |  | Dictionnaire avec chaque entrée composée du nom de la préférence et de sa valeur.  Les préférences s’appliquent uniquement au profil utilisateur utilisé.  Pour consulter des exemples, accédez au `Preferences` fichier dans le répertoire des données utilisateur de Microsoft Edge.  |  
| séparation | booléen | false | Si la valeur est false, Microsoft Edge se ferme dès qu' `EdgeDriver` il se termine, que la session se termine ou non.  Si la valeur est true, Microsoft Edge se ferme uniquement si la session est fermée (ou fermée).  **Remarque**: si la valeur est true et que la session n’est pas fermée, le `EdgeDriver` Répertoire de données utilisateur temporaire utilisé par l’instance Microsoft Edge ne doit pas être nettoyé.  |  
| debuggerAddress | chaîne |  | Adresse d’un serveur du débogueur auquel se connecter, sous la forme de <nom d’hôte/adresse IP:>, par exemple  `127.0.0.1:38947` .  |
| excludeSwitches | liste de chaînes |  | Liste des commutateurs de la ligne de commande Microsoft Edge pour exclure ce EdgeDriver par défaut lors du démarrage de Microsoft Edge.  Ne préfixez pas les commutateurs `--` .  |  
| minidumpPath | chaîne |  | Répertoire de stockage des minidumps Microsoft Edge.  \ (Pris en charge uniquement sur Linux. \) |  
| mobileEmulation | dictionnaire |  | Dictionnaire ayant une valeur pour `deviceName` ou des valeurs pour `deviceMetrics` et `userAgent` .  |  
| perfLoggingPrefs | dictionnaire |  | Dictionnaire facultatif indiquant les préférences de journalisation des performances.  Pour plus d’informations, accédez à l' [objet perfLoggingPrefs](#perfloggingprefs-object).  |  
| windowTypes | liste de chaînes |  | Liste de types de fenêtre qui s’affichent dans la liste des handles de fenêtre.  Pour accéder aux éléments du WebView Android, incluez `webview` dans la liste.  |  
| wdpAddress | chaîne |  | Adresse d’un serveur Windows Device Portal sur lequel vous vous connectez, `hostname/ip:port` par exemple  `127.0.0.1:50080` .  Pour plus d’informations, accédez au [débogage à distance-appareils Windows 10][DevtoolsRemoteDebuggingWindows].  |  
| wdpUsername | chaîne |  | Nom d’utilisateur facultatif à utiliser lors de la connexion à un serveur Windows Device Portal.  Obligatoire si l’authentification du serveur est activée.  |  
| wdpPassword | chaîne |  | Mot de passe facultatif à utiliser lors de la connexion à un serveur Windows Device Portal.  Obligatoire si l’authentification du serveur est activée.  |  
| windowsApp | chaîne |  | ID du modèle utilisateur de l’application à lancer, par exemple `Microsoft.MicrosoftEdge.Stable_8wekyb3d8bbwe!MSEDGE` .  Utiliser `windowsApp` `binary` à la place lors de la connexion à un appareil ou un émulateur Windows 10 à l’aide de Windows Device Portal.  |  

## objet perfLoggingPrefs  

Le `perfLoggingPrefs` dictionnaire a le format suivant \ (toutes les clés sont facultatives \).  

| Clé | Type | Valeur par défaut | Détails |  
|:--- |:--- |:--- |:--- |  
| enableNetwork | booléen | true | Pour collecter des événements \ (ou ne pas collecter \) à partir du domaine du réseau.  |  
| enablePage | booléen | true | Pour collecter des événements \ (ou ne pas recueillir \) à partir du domaine de la page.  |  
| traceCategories | chaîne | \ (vide \) | Une chaîne séparée par des virgules des catégories de suivi Microsoft Edge pour lesquelles les événements de suivi doivent être collectés.  Une chaîne vide ou non spécifiée désactive le suivi.  |  
| bufferUsageReportingInterval | entier positif | 1000 | Le nombre de millisecondes requis entre les événements d’utilisation du tampon de suivi DevTools.  Par exemple, si 1000, une fois par seconde, DevTools signale le nombre de fois que la mémoire tampon de suivi est remplie.  S’il s’agit d’un rapport indiquant que l’utilisation de la mémoire tampon est 100%, un message d’avertissement est émis.  |  

## Fonctions renvoyées  

La liste suivante contient toutes les fonctionnalités propres à Microsoft Edge qui `EdgeDriver` renvoient lorsque vous créez une nouvelle session.  

| Fonctionnalité | Type | Détails |  
|:--- |:--- |:--- |  
| msedge.msedgedriverVersion | chaîne | Version de EdgeDriver. |  
| msedge.userDataDir | chaîne | Chemin d’accès au répertoire des données utilisateur utilisé par l’instance Microsoft Edge. |  

<!-- links -->  

[DevtoolsRemoteDebuggingWindows]: ../devtools-guide-chromium/remote-debugging/windows.md "Commencer à utiliser le débogage à distance des appareils Windows 10 | Documents Microsoft"  
[DrivingEdgeWebDriverIndex]: ./index.md#driving-microsoft-edge-chromium "Pilotage de Microsoft Edge (chrome) | Documents Microsoft"    
[DownloadEdgeWebDriverIndex]: ./index.md#install-microsoft-edge-chromium "Installer Microsoft Edge (chrome) | Documents Microsoft"  
[ChooseLanguageBindingWebDriverIndex]: ./index.md#choose-a-webdriver-language-binding "Choix d’une langue de liaison WebDriver | Documents Microsoft"

[SeleniumMain]: https://www.selenium.dev "Automation du navigateur SeleniumHQ"  
[SharedCapabilitiesSeleniumDocumentation]: https://www.selenium.dev/documentation/en/driver_idiosyncrasies/shared_capabilities/ "Fonctionnalités partagées | Documentation de sélénium"   

[CapabilitiesW3cWebdriver]: https://www.w3.org/TR/webdriver/#capabilities "Fonctionnalités-spécification du WebDriver | W3C"   
