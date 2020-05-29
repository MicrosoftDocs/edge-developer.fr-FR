---
description: Mise à jour du protocole Microsoft Edge DevTools
title: Mise à jour du protocole Microsoft Edge DevTools
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/11/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: f1936a83f948dd17cc76139b7fd67fc73cd692d0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565500"
---
# Protocole DevTools Microsoft Edge (chrome)

Avec le Shift dans la plate-forme Web sous-jacente de Microsoft Edge à chrome, le [protocole devtools de Microsoft Edge (EdgeHTML)](./devtools-protocol/index.md) ne recevra pas de nouvelles mises à jour. Le protocole DevTools de Microsoft Edge (chrome) correspondra aux API du protocole chrome DevTools. 

Vous trouverez des informations sur ces domaines et méthodes en vous référant à la [visionneuse du protocole chrome devtools](https://chromedevtools.github.io/devtools-protocol/tot/).

> [!NOTE]
> Toutes les méthodes qui ont été préfixées `ms` dans le [protocole devtools de Microsoft Edge (EdgeHTML)](./devtools-protocol/index.md) ne sont plus prises en charge dans le protocole devtools Microsoft Edge (chrome).

## Utiliser le protocole DevTools

Voici comment joindre un client d’outillage personnalisé au serveur DevTools dans Microsoft Edge (chrome).

1. Assurez-vous que toutes les instances de Microsoft Edge (chrome) sont fermées.

2. Lancez Microsoft Edge (chrome) avec le port de débogage à distance:

    ```
    msedge.exe --remote-debugging-port=9222
    ```

3. Si vous le souhaitez, vous pouvez démarrer une instance séparée d’Edge à l’aide d’un profil utilisateur distinct, si vous le souhaitez:

    ```
    msedge.exe --user-data-dir=<some directory>
    ```

4. Ensuite, utilisez le `list` point de terminaison HTTP pour obtenir une liste des cibles de page pouvant être attachées:

    ```
    http://localhost:9222/json/list
    ```

5. Enfin, connectez-vous à la `webSocketDebuggerUrl` cible souhaitée et émettez des commandes/souscrivez à des messages d’événements via le serveur de socket Web devtools.

## Points de terminaison HTTPs du protocole DevTools

Le protocole DevTools Microsoft Edge (chrome) prend en charge les points de terminaison HTTP suivants.

## /json/version
Fournit des informations sur le navigateur de l’ordinateur hôte et la version du protocole DevTools qu’il prend en charge.

**Parameters**

*None*

**Objet renvoyé**

```json
{
   "Browser": "Edg/75.0.115.0",
   "Protocol-Version": "1.3",
   "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/75.0.3739.0 Safari/537.36 Edg/75.0.115.0",
   "V8-Version": "7.5.98",
   "WebKit-Version": "537.36 (@68a98f73c7d0f766fb5a013ea7f8dbb41089bc1b)",
   "webSocketDebuggerUrl": "ws://localhost:9222/devtools/browser/a9d0e8cf-476a-4a89-bba9-0fc27ce691cd"
}
```

## /json/protocol

Fournit la totalité de la surface de l’API de protocole sérialisée en JSON.

**Parameters**

*None*

**Objet renvoyé**

Objet JSON qui représente la surface d’API disponible pour la version actuelle du protocole.

## /json/list

Fournit une liste de cibles de pages pour le débogage.

**Parameters**

*None*

**Objet renvoyé**

```json
[{
   "description": "",
   "devtoolsFrontendUrl": "/devtools/inspector.html?ws=localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989",
   "id": "AB07C11A262D1EC8634EB12E2DCA4989",
   "title": "localhost:9222/json/protocol",
   "type": "page",
   "url": "http://localhost:9222/json/list",
   "webSocketDebuggerUrl": "ws://localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989"
}, … ]
```

## /json/close

Ferme le processus cible (par exemple, dans Microsoft Edge (chrome), ferme l’onglet de page.)

**Parameters**

ID cible 

**Objet renvoyé**

```
String(“Target is closing”)
```

## Outils de contrôle à distance pour Microsoft Edge (bêta)

Vous pouvez maintenant installer les [outils de contrôle à distance de Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) à partir du [Microsoft Store](https://www.microsoft.com/store/apps/windows). Cette application vous permet de déboguer à distance Microsoft Edge (chrome) exécuté sur un appareil Windows 10 à partir de votre ordinateur de développement.

Pour découvrir comment configurer votre appareil Windows 10 et y accéder à partir de votre ordinateur de développement, consultez [ce didacticiel](./devtools-guide-chromium/remote-debugging/windows.md).

Les [outils de contrôle à distance de Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) utilisent le même protocole devtools Microsoft Edge (chrome) que le [devtools](./devtools-guide-chromium.md) pour communiquer avec Microsoft Edge exécuté sur l’appareil Windows 10 que vous voulez déboguer. Cette application vient tout juste `/msedge/` d’être un ID de processus ( `pid` ) avant chaque appel au protocole. Il prend en charge les points de terminaison HTTP suivants.

### /msedge/json/list

Fournit une liste de tous les `msedge.exe` processus (y compris les onglets [PWAS](./progressive-web-apps-chromium/index.md) et All dans toutes les instances de Microsoft Edge) sur l’appareil Windows 10 pour le débogage.

**Parameters**

*None*

**Objet renvoyé**

```json
[{
   "description": "",
    "devtoolsFrontendUrl": "http://172.17.75.195:80/msedge/7264/devtools/inspector.html?ws=172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "faviconUrl": "https://docs.microsoft.com/favicon.ico",
    "id": "ED4FFDB4529723A0FAFCBDB9B45851BB",
    "title": "Get Started with Remote Debugging Windows 10 Devices - Microsoft Edge Development | Microsoft Docs",
    "type": "page",
    "url": "https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium/remote-debugging/windows",
    "webSocketDebuggerUrl": "ws://172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "browserProcessId": 7264
}, … ]
```

### /msedge/

Équivalent de la fonction [/msedge/JSON/List](#msedgejsonlist). 

### /msedge/[PID]/JSON/List

Fournit une liste de cibles de pages pour l’instance Microsoft Edge qui correspond à la fournie `[pid]` pour le débogage.

**Parameters**

*None*

**Objet renvoyé**

```json
[{
    "description": "",
    "devtoolsFrontendUrl": "http://172.17.75.195:80/msedge/7264/devtools/inspector.html?ws=172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "faviconUrl": "https://docs.microsoft.com/favicon.ico",
    "id": "ED4FFDB4529723A0FAFCBDB9B45851BB",
    "title": "Get Started with Remote Debugging Windows 10 Devices - Microsoft Edge Development | Microsoft Docs",
    "type": "page",
    "url": "https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium/remote-debugging/windows",
    "webSocketDebuggerUrl": "ws://172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB"
}, … ]
```

### /msedge/[PID]/JSON/version

Fournit des informations sur l’instance Microsoft Edge qui correspond à la `[pid]` version fournie et la version du protocole devtools prise en charge.

**Parameters**

*None*

**Objet renvoyé**

```json
{
    "Browser": "Edg/82.0.452.0",
    "Protocol-Version": "1.3",
    "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/82.0.4080.0 Safari/537.36 Edg/82.0.452.0",
    "V8-Version": "8.2.263",
    "WebKit-Version": "537.36 (@fe0232051787ca94ac8edfc0084c3488b7d9bdb2)",
    "webSocketDebuggerUrl": "172.17.75.195:80/msedge/7264/devtools/browser/7a67c8c4-138b-48e3-bfe0-cb7af34d559a"
}
```

### /msedge/[PID]/JSON/Protocol/

Fournit la totalité de la surface de l’API de protocole sérialisée en JSON pour l’instance Microsoft Edge correspondant au fourni `[pid]` .

**Parameters**

*None*

**Objet renvoyé**

Objet JSON qui représente la surface d’API disponible pour la version du protocole utilisée par l’instance Microsoft Edge correspondant à la fournie `[pid]` .
