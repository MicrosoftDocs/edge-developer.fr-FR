---
description: Options de distribution lors de la publication d’une application à l’aide de Microsoft Edge WebView2
title: Distribution des applications WebView2 Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: e96ca2b26feb3883b51ad468db1fabe68ed8ad1f
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/15/2020
ms.locfileid: "11118996"
---
# Distribution d’applications à l’aide de WebView2  

Lors de la distribution de votre application WebView2, assurez-vous que la plateforme Web de stockage-le [Runtime WebView2](#understanding-the-webview2-runtime) est présent avant le démarrage de l’application.  Cet article décrit comment les développeurs peuvent installer le runtime  [WebView2 et utiliser](#evergreen-distribution-mode) les deux modes de distribution de votre application WebView2: persistants et [version corrigée](#fixed-version-distribution-mode).  

## Mode de distribution persistant  

> [!NOTE]
> Le mode de distribution persistant est recommandé pour la plupart des développeurs.  

Le mode de distribution persistant garantit que votre application tire parti des dernières fonctionnalités et des mises à jour de sécurité.  Il présente les caractéristiques suivantes.  

*   La plateforme Web sous-jacente \ (WebView2 Runtime \) est mise à jour automatiquement sans aucun effort supplémentaire des développeurs.  
*   Toutes les applications qui utilisent le mode de distribution persistant utilisent une copie partagée du runtime WebView2 persistant, qui économise de l’espace disque.  

### Présentation de la WebView2 Runtime  

WebView2 Runtime est un Runtime redistribuable qui sert de plateforme Web de stockage pour les applications WebView2.  Ce concept est similaire à celui de VC + + ou .NET Runtime pour les applications/.NET C++.  Dans le cadre du coulisse, le runtime est modifié les fichiers binaires Microsoft Edge \ (chrome \) qui sont affiné et testés pour les applications.  Dans le cadre de l’installation, le runtime ne s’affichera pas sous la forme d’un navigateur visible par l’utilisateur lors de l’installation, par exemple, les utilisateurs ne disposeront pas d’un raccourci sur le bureau ou  

Pour le développement et les tests, les développeurs peuvent utiliser le runtime ou un canal de navigateur Microsoft Edge \ (chrome \) non stable pour la plateforme Web de stockage.  Dans les environnements de production, les développeurs doivent s’assurer que le runtime est présent sur des appareils utilisateur avant le démarrage de l’application.  Le canal stable Microsoft Edge n’est pas disponible pour l’utilisation de WebView2 afin d’éviter que les applications ne dépendent du navigateur en production.  

Les développeurs ne doivent pas appliquer de dépendance au navigateur, car:  

*   Le mode de présentation de Microsoft Edge \ (chrome \) n’est pas garanti sur tous les appareils utilisateurs.  Par exemple, les appareils déconnectés de Windows Update ou qui ne sont pas gérés directement par Microsoft (une grande partie du marché entreprise/EDU) ne disposent pas du navigateur.  Permettre aux développeurs de distribuer le runtime WebView2 évite d’adopter une dépendance sur le navigateur en tant qu’éléments préalables pour les applications.
*   Les navigateurs et applications ont des cas d’utilisation différents, et par conséquent, il est possible que les dépendances sur un navigateur aient des effets inattendus sur vos applications.  Par exemple, il est possible que les administrateurs informatiques contrôlent la version du navigateur pour la compatibilité du site Web interne.  WebView2 Runtime permet aux applications de rester persistant lorsque les mises à jour de navigateur sont gérées activement.  
*   Contrairement au navigateur, le runtime est développé et testé pour les scénarios d’application, et dans certains cas, il peut y avoir des corrections de bogues qui ne sont pas encore disponibles dans le navigateur.  

Le runtime WebView2 persistant est prévu d’expédier la boîte de réception dans les futures versions de Windows.  Avant que le runtime ne soit plus universellement disponible, les développeurs sont recommandés pour déployer le runtime en même temps que leur application de production.  

### Déploiement de l’exécutable WebView2 persistant  

Une seule installation de l’exécutable WebView2 persistant est nécessaire pour toutes les applications persistantes sur l’appareil.  Un certain nombre d’outils sont disponibles sur la [page de téléchargement de WebView2 Runtime][Webview2Installer] pour aider les développeurs à déployer le runtime persistant, par exemple:  

*   Le programme d’amorçage du runtime WebView2 (bientôt disponible) est un programme d’installation minuscule \ (approximativement 2 Mo).  Ce programme d’installation télécharge et installe le runtime persistant à partir de serveurs Microsoft qui correspond à l’architecture de l’appareil de l’utilisateur.  
*   Lien pour télécharger le programme d’amorçage (à publier bientôt) est un lien permettant aux développeurs de télécharger le programme d’amorçage par programmation.
*   Le programme d’installation autonome de WebView2 Runtime est un programme d’installation complet qui peut installer le WebView2 Runtime persistant dans les environnements hors connexion.  

Pour le moment, le programme d’amorçage et le programme d’installation autonome prennent uniquement en charge l’installation par machine, qui nécessite une élévation.  Lors de l’exécution sans élévation, une invite contrôle de compte d’utilisateur Windows s’affiche pour demander aux utilisateurs d’élever les autorisations.  

Nous recommandons les flux de travail suivants pour vérifier que le runtime est déjà installé avant le lancement de l’application.  Vous pouvez ajuster votre flux de travail en fonction de votre scénario.  Nous fournissons également un exemple de code à l’avenir.  

#### Déploiement en ligne uniquement  

Si vous avez un scénario de déploiement en ligne uniquement où les utilisateurs finaux sont supposés disposer d’un accès à Internet, procédez comme suit:  

*   Lors de l’installation de votre application, vérifiez si le runtime est déjà installé sur l’ordinateur:  
    *   L’inspection si le contrôle RegKey `pv (REG_SZ)` existe sous `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\ClientState\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}` ou  
    *   Appel de l’API WebView2 [GetAvailableCoreWebView2BrowserVersionString](/microsoft-edge/webview2/reference/win32/webview2-idl#getavailablecorewebview2browserversionstring) , puis vérifier si versionInfo a la valeur null.  
*   Si le runtime n’est pas installé, utilisez le lien par programmation pour télécharger le programme d’amorçage.  
*   Invoquez le programme d’amorçage à partir d’un processus ou d’une invite de commandes avec élévation de privilèges `MicrosoftEdgeWebview2Setup.exe /silent /install` pour une installation silencieuse.  

Ce flux de travail garantit l’installation de la version d’exécution uniquement lorsqu’elle est nécessaire, vous n’êtes pas obligé de empaqueter les programmes d’installation ou de détecter l’architecture des appareils utilisateur, et pouvez installer le runtime en silence.  Vous pouvez également choisir de conditionner le programme de démarrage avec votre application au lieu de la télécharger par programmation à la demande.  

#### Déploiement hors connexion  

Si vous avez un scénario de déploiement hors connexion dans lequel le déploiement de l’application doit fonctionner entièrement hors connexion, procédez comme suit:  

*   Téléchargez le [programme d’installation autonome][Webview2Installer].  
*   Incluez le programme d’installation dans le programme d’installation ou de mise à jour de votre application.  
*   Lors de l’installation de votre application, vérifiez si le runtime est déjà installé sur l’ordinateur:  
    *   L’inspection si le contrôle RegKey `pv (REG_SZ)` existe sous `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\ClientState\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}` ou  
    *   Appel de l’API WebView2 [GetAvailableCoreWebView2BrowserVersionString](/microsoft-edge/webview2/reference/win32/webview2-idl#getavailablecorewebview2browserversionstring) , puis vérifier si versionInfo a la valeur null.  
*   Si le runtime n’est pas installé, invoquez le programme d’installation autonome à partir d’un processus ou d’une invite de commandes avec élévation de privilèges `MicrosoftEdgeWebView2RuntimeInstaller{X64/X86/ARM64}.exe /silent /install` pour une installation silencieuse.  

## Mode de distribution de version fixe  

> [!NOTE]
> Le mode de distribution de la version fixe n’est pas encore disponible.  

Dans le cas d’environnements restreints, il est prévu de prendre en charge une version fixe, auparavant nommée amener à votre propre mode de distribution.  Le mode de distribution de version fixe permet aux développeurs de sélectionner et de empaqueter une version spécifique de l’exécution WebView2.  Le mode de distribution de la version fixe vous permet de contrôler la version de WebView2 Runtime utilisée par votre application, ainsi que la mise à jour des ordinateurs utilisateur.  Le mode de distribution de la version fixe ne reçoit aucune mise à jour automatique, et les développeurs doivent envisager d’appliquer les mises à jour eux-mêmes.  


<!-- links -->  

[ConceptsVersioning]: ./versioning.md "Présentation des versions de navigateur et de WebView2 | Documents Microsoft"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Programme d’installation de WebView2"  
