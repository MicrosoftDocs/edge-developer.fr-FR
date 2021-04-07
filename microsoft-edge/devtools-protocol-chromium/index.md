---
description: Mise à jour du protocole Microsoft Edge DevTools
title: Mise à jour du protocole Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/06/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: de7d6c39c09ba321f21b34e6e461ec030f09f6ad
ms.sourcegitcommit: 146072bf606b84e5145a48333abf9c6b892a12d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/07/2021
ms.locfileid: "11480159"
---
# <a name="microsoft-edge-chromium-devtools-protocol-overview"></a>Vue d’ensemble du protocole DevTools Microsoft Edge (Chromium)  

Avec la transition de la plateforme web sous-jacente de Microsoft Edge vers Chromium, le protocole [DevTools de Microsoft Edge (EdgeHTML)](/archive/microsoft-edge/legacy/developer/devtools-protocol/index) ne reçoit aucune mise à jour supplémentaire.  Le protocole Microsoft Edge \(Chromium\) DevTools correspondra aux API du protocole Chrome DevTools à l’avenir.  

Vous trouverez de la documentation sur ces domaines et méthodes en faisant référence à la visionneuse de protocole [Chrome DevTools.](https://chromedevtools.github.io/devtools-protocol/tot)  

> [!NOTE]
> Toutes les méthodes avec préfixe dans le protocole `ms` [DevTools Microsoft Edge (EdgeHTML)](/archive/microsoft-edge/legacy/developer/devtools-protocol/index) ne sont plus pris en charge dans le protocole DevTools Microsoft Edge \(Chromium\).  

## <a name="using-the-devtools-protocol"></a>Utilisation du protocole DevTools  

Voici comment attacher un client d’outils personnalisé au serveur DevTools dans Microsoft Edge \(Chromium\).  

1.  Assurez-vous que toutes les instances de Microsoft Edge \(Chromium\) sont fermées.  
1.  Lancez Microsoft Edge \(Chromium\) avec le port de débogage à distance : 
    
    ```shell
    msedge.exe --remote-debugging-port=9222
    ```  
    
1.  Si vous le souhaitez, vous pouvez démarrer une instance distincte de Edge à l’aide d’un profil utilisateur distinct.  
    
    ```shell
    msedge.exe --user-data-dir=<some directory>
    ```  
    
1.  Ensuite, utilisez le point de terminaison HTTP `list` pour obtenir la liste des cibles de page attachables.  
    
    ```http
    http://localhost:9222/json/list
    ```  
    
1.  Enfin, connectez-vous à la cible souhaitée et émettre des commandes/s’abonner aux messages d’événement via le serveur `webSocketDebuggerUrl` de socket web DevTools.  

## <a name="devtools-protocol-http-endpoints"></a>Points de terminaison HTTP du protocole DevTools  

Le protocole Microsoft Edge \(Chromium\) DevTools prend en charge les points de terminaison HTTP suivants.  

## <a name="jsonversion"></a>/json/version  

Fournit des informations sur le navigateur de l’ordinateur hôte et sur la version du protocole DevTools qu’il prend en charge.  

**Parameters**  

**Aucun(e)**  

**Return, objet**  

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

## <a name="jsonprotocol"></a>/json/protocol  

Fournit l’intégralité de la surface de l’API de protocole sérialisée en tant que JSON.  

**Parameters**  

**Aucun(e)**  

**Return, objet**  

Objet JSON qui représente la surface API disponible pour la version actuelle du protocole.  

## <a name="jsonlist"></a>/json/list  

Fournit une liste candidate de cibles de page pour le débogage.  

**Parameters**  

**Aucun(e)**  

**Return, objet**  

```json
[{
   "description": "",
   "devtoolsFrontendUrl": "/devtools/inspector.html?ws=localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989",
   "id": "AB07C11A262D1EC8634EB12E2DCA4989",
   "title": "localhost:9222/json/protocol",
   "type": "page",
   "url": "http://localhost:9222/json/list",
   "webSocketDebuggerUrl": "ws://localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989"
}, ...  ]
```  

## <a name="jsonclose"></a>/json/close  

Ferme le processus cible \(par exemple, dans Microsoft Edge \(Chromium\), ferme l’onglet de page\).  

**Parameters**  

ID cible  

**Return, objet**  

```
String(“Target is closing”)
```  

## <a name="remote-tools-for-microsoft-edge-beta"></a>Outils à distance pour Microsoft Edge (bêta)  

Vous pouvez désormais installer les outils à distance [pour Microsoft Edge (bêta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) à partir du [Microsoft Store.](https://www.microsoft.com/store/apps/windows)  Cette application vous permet de déboguer à distance Microsoft Edge (Chromium) s’exécutant sur un appareil Windows 10 à partir de votre ordinateur de développement.  

Pour découvrir comment configurer votre appareil Windows 10 et vous y connecter à partir de votre ordinateur de développement, accédez à Démarrer avec le débogage à distance des appareils [Windows 10.](../devtools-guide-chromium/remote-debugging/windows.md)  

Les outils à distance pour [Microsoft Edge (bêta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) utilisent le même protocole Microsoft Edge (Chromium) [DevTools que devTools](../devtools-guide-chromium/index.md) pour communiquer avec Microsoft Edge en cours d’exécution sur l’appareil Windows 10 que vous souhaitez déboguer.  Cette application est juste précédée d’un ID de processus ( ) avant `/msedge/` `pid` chaque appel au protocole.  Il prend en charge les points de terminaison HTTP suivants.  

### <a name="msedgejsonlist"></a>/msedge/json/list  

Fournit une liste de candidats de tous les processus \(y compris les PVE et tous les onglets dans toutes les instances de Microsoft Edge\) sur l’appareil Windows 10 pour le `msedge.exe` débogage. [](../progressive-web-apps-chromium/index.md)  

**Parameters**  

**Aucun(e)**  

**Return, objet**  

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
}, ...  ]
```  

### <a name="msedge"></a>/msedge/  

Fonctionnellement équivalent à [/msedge/json/list](#msedgejsonlist).  

### <a name="msedgepidjsonlist"></a>/msedge/[pid]/json/list  

Fournit une liste candidate de cibles de page pour l’instance de Microsoft Edge qui correspond à celle fournie `[pid]` pour le débogage.  

**Parameters**  

**Aucun(e)**  

**Return, objet**  

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
}, ...  ]
```  

### <a name="msedgepidjsonversion"></a>/msedge/[pid]/json/version  

Fournit des informations sur l’instance de Microsoft Edge qui correspond à la version fournie et la version du protocole `[pid]` DevTools qu’elle prend en charge.  

**Parameters**  

**Aucun(e)**  

**Return, objet**  

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

### <a name="msedgepidjsonprotocol"></a>/msedge/[pid]/json/protocol/  

Fournit l’intégralité de la surface de l’API de protocole sérialisée en tant que JSON pour l’instance de Microsoft Edge qui correspond à la version `[pid]` fournie.  

**Parameters**  

**Aucun(e)**  

**Return, objet**  

Objet JSON qui représente la surface d’API disponible pour la version du protocole que l’instance de Microsoft Edge qui correspond à l’api `[pid]` fournie utilise.  
