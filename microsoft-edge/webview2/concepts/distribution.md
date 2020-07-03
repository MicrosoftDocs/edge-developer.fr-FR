---
description: Options de distribution lors de la publication d’une application à l’aide de Microsoft Edge WebView2
title: Distribution de l’application Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/01/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: b76ebcd4ebc30e30083e742a5e84075a5c6ef779
ms.sourcegitcommit: bb62099215e4f610f8561250fa943f58a0f836b0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2020
ms.locfileid: "10846016"
---
# Distribution d’applications à l’aide de WebView2  

Le contrôle WebView2 utilise la plate-forme Microsoft Edge (chrome).  Lors du packaging et de la distribution de votre application, assurez-vous qu’une copie de la plateforme ou du runtime WebView2 est présente avant le démarrage de l’application.  La page suivante décrit comment vous \ (le développeur \) est en mesure de s’assurer que le runtime WebView2 est installé et qu’il utilise les deux modes de distribution de votre application WebView2: [persistant](#evergreen-distribution-mode) et [version corrigée](#fixed-version-distribution-mode).  

## Mode de distribution persistant  

Le mode de distribution persistant garantit que votre application tire parti des dernières fonctionnalités et des mises à jour de sécurité.  Le mode de distribution persistant a les caractéristiques suivantes.  

*   La plateforme Web se met à jour automatiquement sans aucun effort supplémentaire de votre part.  
*   Toutes les applications qui exploitent le mode de distribution persistant utilisent une copie partagée des fichiers binaires de la plateforme qui économise de l’espace disque.  

Il existe plusieurs canaux WebView2 que les applications peuvent utiliser en tant que plateforme Web.  Par défaut, WebView2 cible le canal le plus stable disponible sur l’appareil qui répond à la configuration minimale de version du SDK WebView2.  Les canaux suivants sont répertoriés dans l’ordre le plus petit du canal stable.  

1.  WebView2 Runtime \ (Preview \)  
1.  Canal MicrosoftEdge Beta  
1.  Canal MicrosoftEdge Dev  
1.  Canal Microsoft Edge Canary    

> [!NOTE]
> Le modèle de distribution persistant est recommandé pour la plupart des développeurs.  

> [!IMPORTANT]
> Le canal stable Microsoft Edge n’est pas une cible valide pour WebView2 et les raisons sont décrites ultérieurement.  

Pour plus d’informations sur le contrôle de version, voir contrôle de [version][ConceptsVersioning] et [Global][ReferenceWin3209538WebviewIdl].  

### Comprendre le runtime et le programme d’installation WebView2 (Preview)  

Le canal stable Microsoft Edge n’est pas installé sur tous les ordinateurs des utilisateurs dans lesquels votre application s’exécute.  Au lieu de nécessiter que les utilisateurs installent Microsoft Edge, votre application risque d’utiliser le runtime WebView2 et le programme d’installation \ (Preview \).  WebView2 Runtime est une copie personnalisée des fichiers binaires Microsoft Edge utilisés pour exécuter vos applications WebView2.  Lorsque le runtime WebView2 est installé, les utilisateurs ne peuvent pas l’utiliser comme navigateur normal.  Par exemple, il n’y a aucun raccourci sur le bureau, entrée du menu Démarrer, les utilisateurs ne peuvent pas ouvrir une fenêtre de navigateur à l’aide des fichiers binaires d’exécution, et ainsi de suite.  Toutes les applications d’WebView2 persistantes sur l’appareil pourraient utiliser une seule installation de WebView2 Runtime.  

Aujourd’hui, lors de la préversion, le WebView2 d’exécution persistant et le canal de développement Microsoft Edge sont mis à jour en même temps et disposent de la même Build.  À l’avenir, lors de l’aperçu, l’équipe WebView2 est en mesure de mettre à jour le runtime WebView2 et de correspondre à la même build que le canal Microsoft Edge Beta.  À l’avenir, lorsque WebView2 atteint une disponibilité générale (GA \), l’équipe WebView2 a la possibilité de mettre à jour le runtime WebView2 et de faire correspondre la même build que le canal stable Microsoft Edge.  Après disponibilité, les applications doivent utiliser le runtime WebView2 en production.  

> [!IMPORTANT]
> Ne livrez pas d’applications WebView2 en production lors de la préversion.  

Les développeurs sont recommandés pour s’assurer que le runtime WebView2 persistant est installé avant le lancement de l’application. Vous trouverez ci-dessous un exemple de flux de travail.  

1.  Téléchargez la dernière version du [programme d’installation WebView2 Runtime][Webview2Installer].  
1.  Incluez le programme d’installation dans le programme d’installation ou de mise à jour de votre application.  
1.  Lors de l’installation ou de la mise à jour de votre application, vérifiez si le runtime WebView2 persistant est déjà installé sur l’ordinateur de l’utilisateur, en utilisant l’API [GetAvailableCoreWebView2BrowserVersionString](https://docs.microsoft.com/en-us/microsoft-edge/webview2/reference/win32/0-9-538/webview2-idl#getavailablecorewebview2browserversionstring) et en vérifiant si versionInfo a la valeur null. Si ce n’est pas le cas, le programme d’installation/mise à jour de l’application peut appeler en silence le programme d’installation d’exécution à partir d’un processus élevé ou d’une invite de commandes avec `MicrosoftEdgeWebView2RuntimeInstallerX64.exe /silent /install` . 

Selon votre situation, il est possible que vous deviez modifier le flux de travail ci-dessus.  Par exemple, le programme d’installation de votre application risque de télécharger le programme d’installation persistant WebView2 Runtime au lieu de l’inclure dans votre package d’application.  

> [!NOTE]
> Le programme d’installation d’WebView2 et d’WebView2 Runtime est dans Preview.  Le préversion est limité et n’est disponible que dans le cadre d’une installation autonome par machine sur Windows 10 sur x64.  À l’avenir, la prise en charge de Windows 7, x86 et ARM64 est planifiée.  

### Recommandations d’utilisation de WebView2 Runtime et de canaux Microsoft Edge non stables  

Prenez en compte les recommandations suivantes lors de l’aperçu.  

*   Assurez-vous d’utiliser le [programme d’exécution et de WebView2s persistantes][Webview2Installer] pour développer ou tester votre Packaging et votre pipeline de distribution.  À l’avenir, votre application de production doit inclure le programme d’installation.  
*   Pour le développement de votre application, vous pouvez utiliser le runtime WebView2 persistant.  Toutefois, dans la mesure où l’exécution passe du canal de développement au canal bêta ou au canal stable, le numéro de version d’exécution risque de ne pas répondre à la configuration minimale requise pour la version d’évaluation d’WebView2 SDK.  Si vous souhaitez utiliser le kit de développement logiciel (SDK) le plus récent, installez le canal Canaries Microsoft Edge pour vérifier qu’une build compatible est disponible sur l’appareil.  Pour plus d’informations sur le contrôle de version, voir contrôle de [version][ConceptsVersioning].  
*   Pour tester votre contenu Web à des fins de compatibilité avec les modifications apportées à la plateforme qui ne sont pas disponibles dans le canal stable, utilisez le canal non stable approprié.  

## Mode de distribution de version fixe  

> [!NOTE]
> Le modèle de distribution de version fixe n’est pas disponible pour le moment.  

Dans le cas d’environnements restreints, il est prévu de prendre en charge une version fixe \ (auparavant nommée «amener-le-votre-votre») en mode de distribution.  Le mode de distribution de version fixe vous permet de sélectionner et de conditionner une version spécifique de l’exécution de WebView2.  Le mode de distribution de la version fixe vous permet de contrôler la version de WebView2 Runtime utilisée par votre application, ainsi que la mise à jour des ordinateurs utilisateur.  Le mode de distribution de la version fixe ne reçoit aucune mise à jour automatique et vous devez planifier l’application manuelle des mises à jour.  

<!-- links -->  

[ConceptsVersioning]: ./versioning.md "Présentation des versions de navigateur et de WebView2 | Documents Microsoft"  
[ReferenceWin3209538WebviewIdl]: ../reference/win32/0-9-538/webview2-idl.md  "Globales | Documents Microsoft"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Programme d’installation de WebView2"  
