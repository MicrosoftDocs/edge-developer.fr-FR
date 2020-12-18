---
description: La version 0,1 du protocole Microsoft Edge DevTools prend en charge les points de terminaison HTTP suivants.
title: Protocoles de points de terminaison HTTPs DevTools, version 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5fe50122728304de137efdfb25ebed7274c55cee
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232870"
---
# Protocoles de points de terminaison HTTPs DevTools, version 0,1 (EdgeHTML)  

> [!NOTE]
> Le protocole Microsoft Edge DevTools fonctionne uniquement sur les [mises à jour de Windows 10 d’avril 2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) et les versions ultérieures de [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .

**Devtools protocole 0,1** prend en charge les points de terminaison http suivants. Pour plus d’informations sur la connexion au processus de contenu du navigateur et la documentation relative aux [domaines](domains/index.md) pour l’API du protocole devtools sur le Web Sockets, voir [utilisation du protocole](../index.md#using-the-protocol) .

## /json/version
Fournit des informations sur le navigateur de l’ordinateur hôte et la version du protocole DevTools qu’il prend en charge.

**Parameters**

*None*

**Objet renvoyé**

```json
{
    "Browser":"Edge/17.17627",
    "Protocol-Version":"0.1",
    "User-Agent":"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/64.0.3282.140 Safari/537.36 Edge/17.17627"
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
    "id":"000001F5-87EE-4D55-0091-C4C08A1F30C8",
    "title":"Microsoft Edge Developer website - Microsoft Edge Development",
    "type":"Page",
    "url":"https://developer.microsoft.com/microsoft-edge/",
    "webSocketDebuggerUrl":"ws://localhost:9222/target/000001F5-87EE-4D55-0091-C4C08A1F30C8"
}, … ]
```

## /json/close

Fermez le processus cible (par exemple, dans Microsoft Edge, fermez l’onglet de page.)

**Parameters**

ID cible 

**Objet renvoyé**

```
String("Target is closing")
```
