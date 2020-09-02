---
description: Découvrir les outils de développement Microsoft Edge
title: Outils de développement Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: edgehtml
keywords: Microsoft Edge, développement web, outils F12, devtools
experimental: false
experiment_id: 51fe4b97-3e55-41
ms.openlocfilehash: 3aee2ab67c6e703a0a31b58b5bf985a23fcbb481
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986219"
---
# Outils de développement Microsoft Edge  

> [!NOTE]
> Les développeurs Microsoft Edge DevTools permettent aux développeurs de créer et de tester des sites Web.  Si vous avez accidentellement ouvert le DevTools, il vous suffit d’appuyer sur `F12` pour le fermer.  

Les applications Microsoft Edge DevTools sont créées [à l’aide de la](https://www.typescriptlang.org/)fonction de création de code, optimisée par une [source ouverte](https://github.com/Microsoft/ChakraCore), optimisée pour les flux de travail frontal modernes et désormais disponibles sous la forme d’une [application Windows 10 autonome](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj) sur le Microsoft Store.

Pour plus d’informations sur les dernières fonctionnalités, consultez [*devtools la dernière mise à jour de Windows 10 (EdgeHTML 17)*](./devtools-guide/whats-new.md).

## Outils principaux

![Outils Microsoft Edge Dev](./devtools-guide/media/devtools.png)

Les DevTools de Microsoft Edge sont les suivants:

 - Panneau d' [**éléments**](./devtools-guide/elements.md) permettant de modifier les propriétés d’accessibilité, d’afficher les détecteurs d’événements et de définir des points d’arrêt de mutation DOM
 - Une [**console**](./devtools-guide/console.md) pour afficher et filtrer des messages de journaux, inspecter des objets JavaScript et des nœuds DOM et exécuter JavaScript dans le contexte de la fenêtre ou du cadre sélectionné.
 - Le [**débogueur**](./devtools-guide/debugger.md) pour parcourir le code, définir des espions et des points d’arrêt, modifier votre code et inspecter les caches de stockage et de cookies Web
 - Panneau [**réseau**](./devtools-guide/network.md) permettant de surveiller et d’inspecter les demandes et les réponses du réseau et du cache du navigateur 
 - Panneau [**performance**](./devtools-guide/performance.md) pour le profil du temps et des ressources système requis par votre site
 - Panneau [**mémoire**](./devtools-guide/memory.md) permettant de mesurer votre utilisation des ressources de mémoire et de comparer les instantanés de tas dans différents États de l’exécution du code
 - Panneau d' [**émulation**](./devtools-guide/emulation.md) pour tester votre site avec différents profils de navigateur, résolutions d’écran et coordonnées d’emplacement GPS

Continuez à envoyer vos [commentaires et demandes de fonctionnalité](#getting-in-touch-with-the-microsoft-edge-devtools-team).

> [!TIP]
> **[Testez gratuitement Microsoft Edge à partir de n’importe quel navigateur](https://developer.microsoft.com/microsoft-edge/tools/remote/)**: nous nous sommes associés à [BrowserStack](https://www.browserstack.com/test-on-microsoft-edge-browser#live-cloud) pour proposer des tests gratuits en temps réel et automatisés sur Microsoft Edge.

## Application du MicrosoftStore

Les **devtools Microsoft Edge** sont [désormais disponibles pour l’aperçu](./devtools-guide/whats-new.md) en tant qu' [application Windows 10 autonome à partir du Microsoft Store](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab), en plus de l’outil de navigation intégré dans le navigateur `F12` . La version store est accompagnée d'un panneau de *Sélecteur* permettant d'associer des cibles de pages locales et distantes ouvertes et d'une mise en page à onglets permettant de passer facilement d'une instance DevTools à l'autre.

### Débogage local

Pour déboguer une page en local, lancez simplement l’application *Microsoft Edge devtools* . Le panneau **local** du sélecteur affiche tous les processus de contenu EdgeHTML actifs, y compris les onglets du navigateur d’ouverture, en cours d’exécution [PWAS](./progressive-web-apps-edgehtml/index.md) (processus de*WWAHost.exe* ) et les contrôles [WebView](./webview.md) . Cliquez sur la cible souhaitée pour joindre et ouvrir une nouvelle instance de l’onglet du DevTools.

![Panneau local de l’application DevTools](./devtools-guide/media/chooser_local.png)

### Débogage à distance

L’application *Microsoft Edge devtools* présente une prise en charge de base pour le débogage de pages sur un ordinateur distant par le biais de notre [**protocole devtools**](./devtools-protocol/index.md)nouvellement publiée. Avec cette version, l’accès distant aux funtionality principaux dans le volet [**débogueur**](./devtools-guide/debugger.md) est l’inspection du cache moins (pour le stockage Web, le travailleur de service, l’API de cache et IndexedDB). Le débogage à distance est limité à *Microsoft Edge* exécutant des hôtes de *Bureau* , avec la prise en charge d’autres hôtes EdgeHTML et des appareils Windows 10 qui arrivent dans les versions ultérieures.

Pour commencer, consultez la section [*DevTools Microsoft Edge*](./devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview) de la documentation sur le [protocole DevTools](./devtools-protocol/index.md).

![Panneau distant de l’application DevTools](./devtools-guide/media/chooser_remote.png)

## Raccourcis généraux

Ces raccourcis contrôlent la fenêtre principale de DevTools et/ou travaillent sur tous les outils.

Action | Raccourci
:------------ | :-------------
Afficher/masquer DevTools (s’ouvre au panneau dernier affichage) | F12, Ctrl + Maj + I
Basculer l’ancrage (détacher/bas/droite) | Ctrl + Maj + D 
Afficher le code source HTML non modifiable dans le débogueur | Ctrl + U
Afficher/masquer la console en bas de tout autre outil  | Ctrl +**`**
Basculer vers des éléments (Explorateur DOM) | CTRL + 1
Basculer vers la console |  CTRL + 2
Basculer vers le débogueur | Ctrl + 3
Basculer vers le réseau | CTRL + 4
Basculer vers les performances | Ctrl + 5
Basculer vers la mémoire | Ctrl + 6
Basculer vers l’émulation | CTRL + 7
Document d’aide | F1
Outil suivant | Ctrl + F6
Outil précédent | CTRL + MAJ + F6
Outil précédent (de l’historique) | Ctrl + Maj + [
Outil suivant (de l’historique) | Ctrl + Maj +]
Sous-cadre suivant    | F6
Sous-cadre précédent | MAJ + F6
Correspondance suivante dans la zone de recherche | F3
Correspondance précédente dans la zone de recherche | Maj + F3
Rechercher dans la zone de recherche | Ctrl+F
Placer le focus sur la console en bas | Alt + Maj + I
Outils d’ancrage/de déconnexion (basculer vers l’ancrage) | Ctrl+P  
Démarrer DevTools à la console | Ctrl + Maj + J
Actualisez la page. **Remarque:** si vous déboguez un point d’arrêt et que vous êtes en pause, l’exécution reprend en premier. | Ctrl + Maj + F5 ou Ctrl + R

## Contacter l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](./devtools-guide-chromium/includes/contact-devtools-team-note.md)]  
