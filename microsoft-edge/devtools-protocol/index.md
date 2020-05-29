---
description: Utilisez le protocole Microsoft Edge DevTools pour inspecter et déboguer le navigateur Microsoft Edge (EdgeHTML).
title: Protocole Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/11/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 8bef24c98dae284f2111f6a16fca4a6f27c89dc4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565458"
---
# Protocole DevTools de Microsoft Edge (EdgeHTML)

> [!NOTE]
> Le protocole DevTools de Microsoft Edge (EdgeHTML) ne fonctionne qu’avec la [mise à jour 2018 d’avril](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) et les versions ultérieures de Windows 10.

Les outils de développement peuvent utiliser le **protocole devtools Microsoft Edge (EdgeHTML)** pour inspecter et déboguer le navigateur Microsoft Edge (EdgeHTML). Il fournit un ensemble de méthodes et d’événements organisés en différents [domaines](0.2/domains/index.md) d’instrumentation du moteur EdgeHTML.

 Les clients d’outils peuvent appeler ces méthodes et surveiller ces événements par le biais de messages Web Sockets JSON échangés avec le *serveur devtools* hébergé par Microsoft Edge (EdgeHTML) ou Windows Device Portal. Microsoft Edge (EdgeHTML) DevTools utilise ce protocole pour activer le [débogage à distance](0.2/clients.md#microsoft-edge-devtools-preview) d’un ordinateur hôte exécutant Microsoft Edge (EdgeHTML) à partir du client autonome devtools disponible sur le [Microsoft Store](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj).

Le protocole DevTools de Microsoft Edge (EdgeHTML) est conçu pour s’aligner étroitement avec le protocole chrome DevTools (voir les [WICG W3C pour les protocoles devtools](https://github.com/WICG/devtools-protocol/)), mais il existe des lacunes d’interopérabilité connues dans cette version.

## Utiliser le protocole

Voici comment associer un client d’outils personnalisé au serveur DevTools dans Microsoft Edge (EdgeHTML). Consultez les instructions de [débogage distantes](0.2/clients.md#microsoft-edge-devtools-preview) si vous utilisez Microsoft Edge devtools comme client.

1. Lancez Microsoft Edge (EdgeHTML) avec le port de débogage distant ouvert, en spécifiant l’URL que vous voulez ouvrir. Exemple:

    ```
    MicrosoftEdge.exe --devtools-server-port 9222 https://www.bing.com
    ```

    Si Edge est déjà démarré, le paramètre URL est facultatif. Un bouton s’affiche à côté de la barre d’adresses du navigateur pour indiquer que le **serveur des outils de développement** a démarré:

    ![Serveur des outils de développement](media/developer-tools-server.png) 

2. Utilisez ce [point de terminaison http](0.2/http.md) pour obtenir une liste des cibles de page pouvant être jointes:

    ```
    http://localhost:9222/json/list
    ```

3. Connectez-vous à la liste `webSocketDebuggerUrl` des pages souhaitées pour générer d’autres [commandes de protocole](0.2/domains/index.md) et recevoir des messages d’événement par le biais du serveur de socket devtools.

## État et commentaires

La [Version 0,2](0.2/index.md) du protocole devtools fournit de nouveaux domaines pour le débogage de style et de mise en page (lecture seule) et les API de console, en plus de la fonctionnalité de débogage de script principal introduite dans la [version 0,1](0.1/index.md). Dans l’interface utilisateur de Microsoft Edge DevTools, cela se traduit par une fonctionnalité disponible dans les panneaux [**éléments**](../devtools-guide/elements.md), [**console**](../devtools-guide/console.md) et [**débogueur**](../devtools-guide/debugger.md) .

Merci d’avoir essayé le protocole Edge DevTools! Nous aimerions entendre vos commentaires à l’adresse suivante:

 - [**Développeur Microsoft Edge**](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer?category_id=84475): idées et demandes de devtools

 - [**EdgeHTML**](https://developer.microsoft.com/microsoft-edge/platform/issues/)des problèmes de suivi des problèmes: protocoles, devtools et problèmes de plateforme EdgeHTML

 - [**Concentrateur de commentaires Microsoft Edge devtools**](feedback-hub:?referrer=microsoftEdge&tabID=2&newFeedback=true&ContextId=344): protocoles et devtools problèmes et suggestions par le biais de l’application Hub de commentaires

## Forum Aux Questions

#### Plusieurs clients peuvent-ils se connecter au même serveur DevTools?
Non, pas simultanément lors du débogage des clients. Le dernier client à connecter va arrêter le précédent. À l’avenir, lorsque d’autres outils sont pris en charge, ceux-ci peuvent prendre en charge des connexions client simultanées.

#### Dois-je utiliser 9222 comme port de serveur DevTools?
Non. Vous pouvez spécifier n’importe quel port, même s’il n’est pas déjà utilisé. Le port 9222 pour le débogage à distance est utilisé par Convention.

#### Comment puis-je connecter mon client d’outils personnalisés à Microsoft Edge (EdgeHTML) exécutant DevTools Server?
Pour en savoir plus sur l’utilisation de l’ordinateur local, voir utilisation des instructions de [*protocole*](#using-the-protocol) ci-dessus. Si vous souhaitez prendre en charge le débogage à distance, vous devez concevoir un flux de travail utilisateur pour l’installation du certificat SSL de l’ordinateur hôte sur le client, par exemple avec une boîte de dialogue d’installation telle que [Microsoft Edge devtools Preview](./0.2/clients.md#microsoft-edge-devtools-preview) utilise.

#### S’il s’agit du débogage à distance à l’aide de Edge DevTools, dois-je lancer le processus de navigateur hôte avec *--devtools-Server-Port* de la ligne de commande? 
Non. Si vous configurez le [débogage à distance à l’aide de Microsoft Edge devtools Preview](./0.2/clients.md#microsoft-edge-devtools-preview), le `--devtools-server-port` commutateur de ligne de commande n’est pas nécessaire pour démarrer Edge. Dans le cas présent, Windows *Device Portal* héberge le serveur devtools pour le compte du navigateur.

#### Est-il possible d’utiliser le protocole Edge DevTools pour déboguer à distance un processus WWAHost. exe ou WebView?
Le protocole Edge DevTools prend actuellement en charge uniquement les onglets du navigateur. Les processus WWAHost. exe et WebView ne sont pas pris en charge.
