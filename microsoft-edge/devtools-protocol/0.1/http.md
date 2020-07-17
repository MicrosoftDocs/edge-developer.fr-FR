---
description: La version 0,1 du protocole Microsoft Edge DevTools prend en charge les points de terminaison HTTP suivants.
title: Protocoles de points de terminaison HTTPs DevTools, version 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: a9d40772b8175790c034ee67236c4887d0831785
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882869"
---
# <span data-ttu-id="82e41-103">Protocoles de points de terminaison HTTPs DevTools, version 0,1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="82e41-103">DevTools Protocol Version 0.1 HTTP Endpoints (EdgeHTML)</span></span>  

> [!NOTE]
> <span data-ttu-id="82e41-104">Le protocole Microsoft Edge DevTools fonctionne uniquement sur les [mises à jour de Windows 10 d’avril 2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) et les versions ultérieures de [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="82e41-104">The Microsoft Edge DevTools Protocol works only on [Windows 10 April 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) and later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) builds.</span></span>

<span data-ttu-id="82e41-105">**Devtools protocole 0,1** prend en charge les points de terminaison http suivants.</span><span class="sxs-lookup"><span data-stu-id="82e41-105">**DevTools Protocol 0.1** supports the following HTTP endpoints.</span></span> <span data-ttu-id="82e41-106">Pour plus d’informations sur la connexion au processus de contenu du navigateur et la documentation relative aux [domaines](domains/index.md) pour l’API du protocole devtools sur le Web Sockets, voir [utilisation du protocole](../index.md#using-the-protocol) .</span><span class="sxs-lookup"><span data-stu-id="82e41-106">See [using the protocol](../index.md#using-the-protocol) for more on connecting to a browser content process and the [Domains](domains/index.md) documentation for the full web sockets-based devtools protocol API.</span></span>

## <span data-ttu-id="82e41-107">/json/version</span><span class="sxs-lookup"><span data-stu-id="82e41-107">/json/version</span></span>
<span data-ttu-id="82e41-108">Fournit des informations sur le navigateur de l’ordinateur hôte et la version du protocole DevTools qu’il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="82e41-108">Provides information on the host machine's browser and which version of the DevTools Protocol it supports.</span></span>

**<span data-ttu-id="82e41-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="82e41-109">Parameters</span></span>**

*<span data-ttu-id="82e41-110">None</span><span class="sxs-lookup"><span data-stu-id="82e41-110">None</span></span>*

**<span data-ttu-id="82e41-111">Objet renvoyé</span><span class="sxs-lookup"><span data-stu-id="82e41-111">Return object</span></span>**

```json
{
    "Browser":"Edge/17.17627",
    "Protocol-Version":"0.1",
    "User-Agent":"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/64.0.3282.140 Safari/537.36 Edge/17.17627"
}
```

## <span data-ttu-id="82e41-112">/json/protocol</span><span class="sxs-lookup"><span data-stu-id="82e41-112">/json/protocol</span></span>

<span data-ttu-id="82e41-113">Fournit la totalité de la surface de l’API de protocole sérialisée en JSON.</span><span class="sxs-lookup"><span data-stu-id="82e41-113">Provides the entire protocol API surface serialized as JSON.</span></span>

**<span data-ttu-id="82e41-114">Parameters</span><span class="sxs-lookup"><span data-stu-id="82e41-114">Parameters</span></span>**

*<span data-ttu-id="82e41-115">None</span><span class="sxs-lookup"><span data-stu-id="82e41-115">None</span></span>*

**<span data-ttu-id="82e41-116">Objet renvoyé</span><span class="sxs-lookup"><span data-stu-id="82e41-116">Return object</span></span>**

<span data-ttu-id="82e41-117">Objet JSON qui représente la surface d’API disponible pour la version actuelle du protocole.</span><span class="sxs-lookup"><span data-stu-id="82e41-117">JSON object which represents the available API surface for current version of the protocol.</span></span>

## <span data-ttu-id="82e41-118">/json/list</span><span class="sxs-lookup"><span data-stu-id="82e41-118">/json/list</span></span>

<span data-ttu-id="82e41-119">Fournit une liste de cibles de pages pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="82e41-119">Provides a candidate list of page targets for debugging.</span></span>

**<span data-ttu-id="82e41-120">Parameters</span><span class="sxs-lookup"><span data-stu-id="82e41-120">Parameters</span></span>**

*<span data-ttu-id="82e41-121">None</span><span class="sxs-lookup"><span data-stu-id="82e41-121">None</span></span>*

**<span data-ttu-id="82e41-122">Objet renvoyé</span><span class="sxs-lookup"><span data-stu-id="82e41-122">Return object</span></span>**

```json
[{
    "id":"000001F5-87EE-4D55-0091-C4C08A1F30C8",
    "title":"Microsoft Edge Developer website - Microsoft Edge Development",
    "type":"Page",
    "url":"https://developer.microsoft.com/microsoft-edge/",
    "webSocketDebuggerUrl":"ws://localhost:9222/target/000001F5-87EE-4D55-0091-C4C08A1F30C8"
}, … ]
```

## <span data-ttu-id="82e41-123">/json/close</span><span class="sxs-lookup"><span data-stu-id="82e41-123">/json/close</span></span>

<span data-ttu-id="82e41-124">Fermez le processus cible (par exemple, dans Microsoft Edge, fermez l’onglet de page.)</span><span class="sxs-lookup"><span data-stu-id="82e41-124">Closes down the target process (e.g., in Microsoft Edge, closes the page tab.)</span></span>

**<span data-ttu-id="82e41-125">Parameters</span><span class="sxs-lookup"><span data-stu-id="82e41-125">Parameters</span></span>**

<span data-ttu-id="82e41-126">ID cible</span><span class="sxs-lookup"><span data-stu-id="82e41-126">Target ID</span></span> 

**<span data-ttu-id="82e41-127">Objet renvoyé</span><span class="sxs-lookup"><span data-stu-id="82e41-127">Return object</span></span>**

```
String("Target is closing")
```
