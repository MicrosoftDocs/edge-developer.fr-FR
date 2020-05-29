---
description: Fonctionnalités ajoutées au Microsoft Edge DevTools de la mise à jour 2018 de Windows 10 avril (EdgeHTML 17)
title: DevTools dans EdgeHTML 17
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, edgehtml 17
ms.custom: seodec18
ms.openlocfilehash: cc110071422f858acf840c1eaf100696a6e3cf03
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565501"
---
# DevTools la mise à jour 2018 de Windows 10 avril (EdgeHTML 17)

La version EdgeHTML 17 de DevTools fournit deux méthodes: en tant qu’outils in-browser ( `F12` ) traditionnels pour Microsoft Edge, et en prévisualisation en tant qu' [application Windows 10](#microsoft-edge-devtools-app-preview) autonome à partir du Microsoft Store.

Les outils ont été mis à jour à l’aide de plusieurs fonctionnalités majeures, notamment la prise en charge de base pour le [débogage à distance](../../devtools-guide.md#remote-debugging) (via notre nouveau [protocole devtools](#devtools-protocol)) [, les](#docking-to-the-right-in-microsoft-edge) [fonctionnalités de débogage](#pwa-debugging)de [IndexedDB](#indexeddb-inspection) Nous avons également continué la mise en route globale de la [refactorisation](./edgehtml-16.md) dans le cadre d’investissements en cours de performance et de fiabilité.

Voici les dernières fonctionnalités de Microsoft Edge DevTools fournies dans la [mise à jour 2018 de Windows 10 d’avril](/windows/uwp/whats-new/windows-10-build-17134) ([EdgeHTML 17](https://aka.ms/devguide_edgehtml_17)).

## Aperçu de l’application Microsoft Edge DevTools

![Application Microsoft Edge DevTools](../../devtools-protocol/media/microsoft-edge-devtools.png) 

Les [**devtools Microsoft Edge**](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) sont désormais disponibles pour l’aperçu en tant qu’application Windows 10 autonome sur le Microsoft Store. La version du Windows Store est une fenêtre de *sélection* qui permet de joindre des cibles de page locales et distantes ouvertes et une disposition avec onglets pour faciliter le basculement entre les instances devtools. En outre, l’exclusivité de l’application DevTools est la possibilité de déboguer du contenu Web dans des applications (telles que des compléments pour Office, Cortana, EdgeHTML [WebView](../../webview.md)et [PWAS installés sur Windows](../../progressive-web-apps-edgehtml/windows-features.md)).

Les DevTools Edge sont également disponibles ( `F12` ) dans le navigateur (sans le panneau de sélection).

Le découplage de DevTools à partir du navigateur offre les avantages suivants:

- Le DevTools s’exécute dans un bac à sable distinct de conteneur d’applications de Microsoft Edge, ce qui améliore la fiabilité des deux.
- L’application permet de basculer facilement entre les onglets d’instances de DevTools actifs (plutôt que de basculer entre les onglets Microsoft Edge ouverts)
- Nous sommes en mesure d’instrumenter le moteur de navigateur *EdgeHTML* et de l’ouvrir sur le plus grand écosystème devtools avec des [API à navigateur croisé](https://github.com/WICG/devtools-protocol/).
- Nous pouvons expédier les mises à jour de DevTools indépendamment du cycle de publication Windows (et EdgeHTML).

Consultez le *Guide devtools* pour plus d’informations sur [le débogage local et à distance à l’aide de l’application devtools](../../devtools-guide.md).

## Protocole DevTools

Les outils de développement peuvent utiliser le [**protocole Microsoft Edge devtools**](../../devtools-protocol/index.md) pour inspecter et déboguer le navigateur Microsoft Edge. Il fournit un ensemble de méthodes et d’événements organisés en différents [domaines](../../devtools-protocol/0.1/domains/index.md) d’instrumentation du moteur EdgeHTML.

 Les clients d’outils peuvent appeler ces méthodes et surveiller ces événements par le biais de messages Web Sockets JSON échangés avec le *serveur devtools* hébergé par Microsoft Edge ou [Windows Device Portal](/windows/mixed-reality/using-the-windows-device-portal). 
 
 Microsoft Edge DevTools utilise ce protocole pour activer le [débogage à distance](../../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview) d’un ordinateur hôte exécutant Microsoft Edge à partir du [client autonome devtools](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj) disponible sur le Microsoft Store. Pour le moment, cette prise en charge de la préversion est limitée au débogage JS d’un autre bord sur un autre appareil de bureau ou un autre ordinateur. Au fil du temps, nous ajouterons la prise en charge de l’ensemble complet de DevTools sur n’importe quelle instance EdgeHTML sur tout appareil Windows 10.  
 
 Les dernières builds de [**Visual Studio Preview**](https://www.visualstudio.com/vs/preview/) (visual studio 15,7 Preview 1 ou version ultérieure) utilisez le protocole devtools pour activer le lancement et le débogage de Microsoft Edge (code JavaScript) à partir de l’environnement de développement intégré (IDE) de Visual Studio à partir de n’importe quel projet ASP.net ou .net core.

## Inspection de IndexedDB

Nouveauté du [**débogueur**](../debugger.md) cette version est un [Gestionnaire IndexedDB](../storage.md#indexeddb-manager) avec prise en charge de l’inspection et de l’actualisation de vos magasins d’objets, et de la suppression d’entrées clés individuelles. Encore plus de fonctionnalités dans les versions ultérieures.

## Débogage de Project Web App

La prise en charge du débogage d’applications Web progressives (PWAs) est désormais activée par défaut, qui fournit des onglets d’outil pour les [**travailleurs de service**](../service-workers.md), les [**API de cache**](../storage.md#cache-manager)et la gestion [**IndexedDB**](../storage.md#indexeddb-manager) .

Par ailleurs, la [barre d’outils du panneau réseau](../network.md#toolbar) comporte un nouveau bouton, **ignorer le travailleur de service pour toutes les demandes réseau**pour activer/désactiver les travailleurs de services enregistrés en tant que proxys réseau:

![Bouton réseau de la barre d’outils: ignorer le travailleur de service pour toutes les demandes réseau](../media/network_toolbar_bypass_sw.png)

Vous pouvez déboguer votre [application PWA comme une application Windows 10 installée](../../progressive-web-apps-edgehtml/windows-features.md) en la sélectionnant dans la liste des cibles [**locales**](../../progressive-web-apps-edgehtml/windows-features.md#debug-your-pwa-edgehtml-as-a-windows-app) (onglet de navigateur/PWA/WebView) dans le sélecteur de l' [application autonome devtools](../../devtools-guide.md#microsoft-store-app).  

## Ancrage à droite dans Microsoft Edge

Vous pouvez désormais ancrer le DevTools à droite de la page que vous déboguez à partir de Microsoft Edge, en plus de l’ancrage en bas et de la déconnexion de DevTools à partir de la fenêtre du navigateur. Utilisez le `Ctrl+Shift+D` bouton pour basculer entre la position du Dock, **Undock** **le**haut et le **bas**de l’écran, ou les icônes situées dans le coin supérieur droit du devtools:

![DevTools (dans l’état non ancré) options d’ancrage](../media/docking_buttons.png) 
