---
description: Une référence pour les fonctionnalités WebDriver et Microsoft Edge options spécifiques pris en charge par EdgeDriver (Chromium).
title: Fonctionnalités et EdgeOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, développement web, html, css, javascript, développeur, webdriver, selenium, test, outils, automatisation, test
ms.openlocfilehash: 5a48ca34e46b56fa60bcacfade2add23026be144
ms.sourcegitcommit: f95812c4e1b7277f67c6c4891be2779cc1b5bdf1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/18/2021
ms.locfileid: "11343778"
---
# Fonctionnalités et EdgeOptions  

Les fonctionnalités sont des options que vous pouvez utiliser pour personnaliser et configurer une `EdgeDriver` session.  Pour en savoir plus sur le démarrage `EdgeDriver` d’une nouvelle session, accédez à Automatisation [Microsoft Edge][WebdriverIndexAutomateMicrosoftEdgeChromium].  Cet article décrit toutes les fonctionnalités de Microsoft Edge [et][WebdriverIndexInstallMicrosoftEdgeChromium] des détails sur la transmission des fonctionnalités aux `EdgeDriver` sessions.  

Les fonctionnalités sont transmises à une session WebDriver en tant que carte JSON.  Les liaisons de langage WebDriver fournissent généralement des méthodes pratiques sécurisées pour le type, vous n’avez donc pas besoin de configurer vous-même la carte JSON.  Différentes liaisons de langage WebDriver utilisent différents mécanismes pour configurer des fonctionnalités.  Accédez à la documentation de votre [liaison de langue préférée][WebdriverIndexChooseWebdriverLanguageBinding] pour en savoir plus sur la configuration des fonctionnalités.  [Selenium][SeleniumMain] configure les fonctionnalités par le biais de la `EdgeOptions` classe.  

## Utilisation de la classe EdgeOptions  

Créez une instance `EdgeOptions` de , qui fournit des méthodes pratiques pour Microsoft Edge fonctionnalités spécifiques.  Après avoir configuré `EdgeOptions` l’objet, passez `EdgeOptions` au `EdgeDriver` constructeur.  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddExtensions("/path/to/extension.crx");
var driver = new EdgeDriver(options);
```  

Pour utiliser des fonctionnalités qui ne sont pas associées à une méthode pratique, utilisez la `AddAdditionalCapability` méthode.  Vous devez transmettre le nom complet de la fonctionnalité et une valeur avec le type correct.  Pour consulter la liste complète des fonctionnalités acceptées et des types de valeurs, accédez à [l’objet EdgeOptions](#edgeoptions-object).  

```csharp
options.AddAdditionalCapability("wdpAddress", "remotehost:50080");
```  

## Fonctionnalités reconnues  

Pour les fonctionnalités standard qui acceptent, accédez à la documentation Selenium et à la `EdgeDriver` [norme][SharedCapabilitiesSeleniumDocumentation] [W3C WebDriver][CapabilitiesW3cWebdriver].  Cet article répertorie uniquement les fonctionnalités spécifiques Microsoft Edge.  

## Objet EdgeOptions  

La Microsoft Edge fonctionnalités spécifiques sont exposées par le biais de `EdgeOptions` l’objet.  Dans certaines langues, les fonctionnalités sont implémentées par la `EdgeOptions` classe.  Dans d’autres langues, les fonctionnalités sont stockées sous le `ms:edgeOptions` dictionnaire dans `DesiredCapabilities` .  

| Fonctionnalité | Type | Valeur par défaut | Détails |  
|:--- |:--- |:--- |:--- |  
| args | liste de chaînes |  | Liste des arguments de ligne de commande à utiliser au démarrage Microsoft Edge.  Les arguments associés à une valeur doivent être séparés par un `=` signe \(par exemple, `['start-maximized', 'user-data-dir=/tmp/temp_profile']` \). |  
| binary | chaîne |  | Chemin d’accès Microsoft Edge binaire à utiliser \(sur macOS, le chemin d’accès doit être le fichier binaire réel, et pas seulement l’application.  par exemple, `/Applications/Microsoft Edge.app/Contents/MacOS/Microsoft Edge` \). |  
| debuggerAddress | chaîne |  | Adresse d’un serveur débogger auquel se connecter, par `hostname/ip:port` exemple. `127.0.0.1:38947` |
| détacher | booléen | `false` | Si , Microsoft Edge se ferme lorsque le `false` service WebDriver s’arrête, même si l’extrémité locale WebDriver n’a pas fermé la session.  Si , Microsoft Edge quitte uniquement si la fin `true` locale WebDriver ferme la session.  Si `true` , et que l’extrémité locale WebDriver ne ferme pas la session, ne nettoie pas le dossier de données utilisateur temporaires utilisé par l Microsoft Edge `EdgeDriver` instance. |  
| excludeSwitches | liste de chaînes |  | Liste des Microsoft Edge ligne de commande à exclure par défaut de EdgeDriver au démarrage Microsoft Edge.  Évitez `--` le préfixe pour les commutateurs. |  
| extensions | liste de chaînes |  | Liste des extensions à installer au démarrage.  Chaque élément de la liste doit être une extension encodée en base 64 \( `.crx` \). |  
| localState | dictionnaire |  | Dictionnaire avec chaque entrée constituée du nom de la préférence et de la valeur.  Les préférences sont appliquées au fichier d’état local dans le dossier de données utilisateur. |  
| minidumpPath | chaîne |  | Répertoire pour stocker les Microsoft Edge minidumps.  \(Pris en charge uniquement sur Linux.\) |  
| mobileEmulation | dictionnaire |  | Dictionnaire avec une valeur pour `deviceName` , ou des valeurs pour et `deviceMetrics` `userAgent` . |  
| perfLoggingPrefs | dictionnaire |  | Dictionnaire facultatif qui spécifie les préférences de journalisation des performances.  pour plus d’informations, accédez à [l’objet perfLoggingPrefs](#perfloggingprefs-object). |  
| prefs | dictionnaire |  | Dictionnaire avec chaque entrée constituée du nom de la préférence et de la valeur.  Les préférences sont appliquées uniquement au profil utilisateur utilisé.  Pour obtenir des exemples, `Preferences` accédez au fichier dans le dossier de données utilisateur de Microsoft Edge. |  
| wdpAddress | chaîne |  | Adresse d’un Windows Device Portal auquel vous vous connectez, par `hostname/ip:port` `127.0.0.1:50080` exemple.  Pour plus d’informations, accédez [à Débogage à distance - Windows 10 appareils.][DevtoolsRemoteDebuggingWindows] |  
| wdpPassword | chaîne |  | Mot de passe facultatif à utiliser lors de la connexion à un Windows Device Portal.  Obligatoire si l’authentification est activée sur le serveur. |  
| wdpUsername | chaîne |  | Nom d’utilisateur facultatif à utiliser lors de la connexion à un Windows Device Portal.  Obligatoire si l’authentification est activée sur le serveur. |  
| windowsApp | chaîne |  | ID de modèle utilisateur d’une application Microsoft Edge package d’application à lancer, par `Microsoft.MicrosoftEdge.Stable_8wekyb3d8bbwe!MSEDGE` exemple.  À utiliser au lieu de vous connecter à un `windowsApp` Windows 10X ou émulateur à l’aide `binary` Windows Device Portal. |  
| windowTypes | liste de chaînes |  | Liste des types de fenêtre qui sont affichés dans la liste des poignées de fenêtre.  Pour accéder aux éléments WebView Android, `webview` incluez-le dans la liste. |  

## objet perfLoggingPrefs  

Le `perfLoggingPrefs` dictionnaire a le format suivant \(toutes les clés sont facultatives\).  

| Clé | Type | Valeur par défaut | Détails |  
|:--- |:--- |:--- |:--- |  
| bufferUsageReportingInterval | integer positif | 1000 | Nombre demandé de millisecondes entre les événements d’utilisation du tampon de suivi DevTools.  Par exemple, si 1 000, alors une fois par seconde, DevTools indique à quel point la mémoire tampon de suivi est pleine.  Si un rapport indique que l’utilisation de la mémoire tampon est de 100 %, un avertissement est émis. |  
| enableNetwork | booléen | true | Pour collecter des événements \(ou pas collecter\) à partir du domaine réseau. |  
| enablePage | booléen | true | Pour collecter des événements \(ou pas collecter\) à partir du domaine Page. |  
| traceCategories | chaîne | \(empty\) | Chaîne séparée par des virgules Microsoft Edge catégories de suivi pour lesquelles les événements de suivi doivent être collectés.  Une chaîne non spécifiée ou vide désactive le suivi. |  

## Fonctionnalités renvoyées  

La liste suivante contient toutes les fonctionnalités spécifiques Microsoft Edge qui renvoient lorsque `EdgeDriver` vous créez une nouvelle session.  

| Fonctionnalité | Type | Détails |  
|:--- |:--- |:--- |  
| msedge.msedgedriverVersion | chaîne | Version de EdgeDriver. |  
| msedge.userDataDir | chaîne | Chemin d’accès au dossier de données utilisateur utilisé par l’instance Microsoft Edge utilisateur. |  

<!-- links -->  

[DevtoolsRemoteDebuggingWindows]: ../devtools-guide-chromium/remote-debugging/windows.md "Mise en place du débogage à Windows 10 appareils | Documents Microsoft"  
[WebdriverIndexChooseWebdriverLanguageBinding]: ./index.md#choose-a-webdriver-language-binding "Choose a WebDriver language binding - WebDriver (Chromium) | Documents Microsoft"
[WebdriverIndexAutomateMicrosoftEdgeChromium]: ./index.md#automate-microsoft-edge-chromium "Automatiser Microsoft Edge (Chromium) - WebDriver (Chromium) | Documents Microsoft"    
[WebdriverIndexInstallMicrosoftEdgeChromium]: ./index.md#install-microsoft-edge-chromium "Installer Microsoft Edge (Chromium) - WebDriver (Chromium) | Documents Microsoft"  

[SeleniumMain]: https://www.selenium.dev "Automation du navigateur SeleniumHQ"  
[SharedCapabilitiesSeleniumDocumentation]: https://www.selenium.dev/documentation/en/driver_idiosyncrasies/shared_capabilities/ "Fonctionnalités partagées | Selenium Documentation"   

[CapabilitiesW3cWebdriver]: https://www.w3.org/TR/webdriver#capabilities "Fonctionnalités : spécification WebDriver | W3C"   
