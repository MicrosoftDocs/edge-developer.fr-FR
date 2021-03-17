---
description: Utilisez le protocole Microsoft Edge DevTools pour inspecter et déboguer le navigateur Microsoft Edge (EdgeHTML).
title: Protocole Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 03/16/2021
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: bc95f6c167479e958ffd16137176418aba872a43
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439309"
---
# <a name="microsoft-edge-edgehtml-devtools-protocol"></a>Protocole DevTools Microsoft Edge (EdgeHTML)

> [!NOTE]
> Le protocole Microsoft Edge (EdgeHTML) DevTools fonctionne uniquement sur la mise à jour [d’avril 2018 de Windows 10](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) et les builds ultérieures.

Les outils de développement peuvent utiliser le protocole **DevTools Microsoft Edge (EdgeHTML)** pour inspecter et déboguer le navigateur Microsoft Edge (EdgeHTML). Il fournit un ensemble de méthodes et d’événements [organisés](0.2/domains/index.md) en différents domaines d’instrumentation du moteur EdgeHTML.

 Les clients d’outils peuvent appeler ces méthodes et surveiller ces événements via des messages de socket web JSON échangés avec le serveur *DevTools* hébergé par Microsoft Edge (EdgeHTML) ou Windows Device Portal. Microsoft Edge (EdgeHTML) DevTools utilise [](0.2/clients.md#microsoft-edge-devtools-preview) ce protocole pour activer le débogage à distance d’un ordinateur hôte exécutant Microsoft Edge (EdgeHTML) à partir du client DevTools autonome disponible à partir du [Microsoft Store.](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj)

Le protocole Microsoft Edge (EdgeHTML) DevTools est conçu pour s’aligner étroitement avec le protocole Chrome DevTools (voir [le W3C WICG pour les protocoles DevTools),](https://github.com/WICG/devtools-protocol/)bien qu’il existe des lacunes d’interopérabilité connues dans cette version.

## <a name="using-the-protocol"></a>Utilisation du protocole

Voici comment attacher un client d’outils personnalisé au serveur DevTools dans Microsoft Edge (EdgeHTML). Consultez les instructions [de débogage](0.2/clients.md#microsoft-edge-devtools-preview) à distance si vous utilisez Microsoft Edge DevTools comme client.

1. Lancez Microsoft Edge (EdgeHTML) avec le port de débogage à distance ouvert, en spécifiant l’URL que vous souhaitez ouvrir. Par exemple:

    ```shell
    MicrosoftEdge.exe --devtools-server-port 9222 https://www.bing.com
    ```

    Si Edge est déjà lancé, le paramètre URL est facultatif. Un bouton apparaît à côté de la barre d’adresses du navigateur pour indiquer que le serveur outils de développement **a** démarré :

    ![Serveur des outils de développement](media/developer-tools-server.png) 

2. Utilisez ce [point de terminaison HTTP pour](0.2/http.md) obtenir la liste des cibles de page attachables :

    ```http
    http://localhost:9222/json/list
    ```

3. Connectez-vous à la page répertoriée pour émettre d’autres commandes de protocole et recevoir des messages d’événement par le biais du serveur `webSocketDebuggerUrl` de socket de devtools. [](0.2/domains/index.md)

## <a name="status-and-feedback"></a>État et commentaires

[La version 0.2](0.2/index.md) du protocole DevTools fournit de nouveaux domaines pour le style et la disposition (lecture seule) des API de débogage et de console, en plus de la fonctionnalité de débogage de script principale introduite dans la [version 0.1](0.1/index.md). Dans l’interface utilisateur DevTools de Microsoft Edge, cela se traduit par des fonctionnalités disponibles dans les panneaux [**Éléments,**](../devtools-guide/elements.md) [**Console**](../devtools-guide/console.md) et [**Débogueur.**](../devtools-guide/debugger.md)

Merci d’avoir essayé le protocole Edge DevTools ! Nous aimeriez connaître vos commentaires sur :

<!-- - [**Microsoft Edge Developer UserVoice**](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer?category_id=84475): DevTools feature ideas and requests-->  

 - [**Suivi des problèmes EdgeHTML**](https://developer.microsoft.com/microsoft-edge/platform/issues/): protocole, devTools et problèmes de plateforme EdgeHTML

 - [**Hub de commentaires Microsoft Edge DevTools**](feedback-hub:?referrer=microsoftEdge&tabID=2&newFeedback=true&ContextId=344): problèmes et suggestions relatifs au protocole et à DevTools via l’application Hub de commentaires

## <a name="faq"></a>Forum Aux Questions

#### <a name="can-multiple-clients-connect-to-the-same-devtools-server"></a>Plusieurs clients peuvent-ils se connecter au même serveur DevTools ?
Non, pas simultanément lorsque les clients sont en cours de débogage. Le dernier client à se connecter lancera le précédent. À l’avenir, lorsque des outils supplémentaires seront pris en charge, ceux-ci ront probablement pris en charge les connexions client simultanées.

#### <a name="do-i-have-to-use-9222-as-the-devtools-server-port"></a>Dois-je utiliser le port 9222 comme port DevTools Server ?
Non. Vous pouvez spécifier n’importe quel port, mais n’oubliez pas d’en sélectionner un qui n’est pas déjà utilisé. Le port 9222 pour le débogage à distance est utilisé par convention.

#### <a name="how-do-i-connect-my-custom-tooling-client-to-microsoft-edge-edgehtml-running-the-devtools-server"></a>Comment connecter mon client d’outils personnalisé à Microsoft Edge (EdgeHTML) exécutant le serveur DevTools ?
Voir Utilisation des instructions [*de protocole*](#using-the-protocol) ci-dessus pour l’attachement à Microsoft Edge (EdgeHTML) en cours d’exécution sur l’ordinateur local. Si vous cherchez à prendre en charge le débogage à distance, vous devez concevoir un flux de travail utilisateur pour installer le certificat SSL de l’ordinateur hôte sur le client, par exemple avec une boîte de dialogue d’installation que [Microsoft Edge DevTools Preview](./0.2/clients.md#microsoft-edge-devtools-preview) utilise.

#### <a name="if-im-remote-debugging-using-edge-devtools-do-i-need-to-start-the-host-browser-process-with---devtools-server-port-cmd-line-switch"></a>Si je suis en train de déboguer à distance à l’aide de Edge DevTools, dois-je démarrer le processus du navigateur hôte avec le commutateur de ligne de commande *--devtools-server-port* ? 
Non. Si vous mettez en place le débogage à distance à l’aide de [Microsoft Edge DevTools Preview,](./0.2/clients.md#microsoft-edge-devtools-preview)le commutateur de ligne de commande n’est pas nécessaire pour démarrer `--devtools-server-port` Edge. Dans ce cas, Windows *Device Portal* héberge le serveur DevTools pour le compte du navigateur.

#### <a name="can-i-use-the-edge-devtools-protocol-to-remotely-debug-a-wwahostexe-or-webview-process"></a>Puis-je utiliser le protocole Edge DevTools pour déboguer à distance un processus WWAHost.exe ou webview ?
Le protocole Edge DevTools prend actuellement en charge uniquement les onglets de navigateur. WWAHost.exe et webview ne sont pas pris en charge.
