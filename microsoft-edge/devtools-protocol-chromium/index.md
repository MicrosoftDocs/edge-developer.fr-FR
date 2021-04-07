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
# <a name="microsoft-edge-chromium-devtools-protocol-overview"></a><span data-ttu-id="d6767-103">Vue d’ensemble du protocole DevTools Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="d6767-103">Microsoft Edge (Chromium) DevTools Protocol overview</span></span>  

<span data-ttu-id="d6767-104">Avec la transition de la plateforme web sous-jacente de Microsoft Edge vers Chromium, le protocole [DevTools de Microsoft Edge (EdgeHTML)](/archive/microsoft-edge/legacy/developer/devtools-protocol/index) ne reçoit aucune mise à jour supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="d6767-104">With the shift in the underlying web platform of Microsoft Edge to Chromium, the [Microsoft Edge (EdgeHTML) DevTools Protocol](/archive/microsoft-edge/legacy/developer/devtools-protocol/index) will not be receiving any further updates.</span></span>  <span data-ttu-id="d6767-105">Le protocole Microsoft Edge \(Chromium\) DevTools correspondra aux API du protocole Chrome DevTools à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="d6767-105">The Microsoft Edge \(Chromium\) DevTools Protocol will match the APIs of the Chrome DevTools Protocol going forward.</span></span>  

<span data-ttu-id="d6767-106">Vous trouverez de la documentation sur ces domaines et méthodes en faisant référence à la visionneuse de protocole [Chrome DevTools.](https://chromedevtools.github.io/devtools-protocol/tot)</span><span class="sxs-lookup"><span data-stu-id="d6767-106">You can find documentation on those domains and methods by referring to the [Chrome DevTools Protocol Viewer](https://chromedevtools.github.io/devtools-protocol/tot).</span></span>  

> [!NOTE]
> <span data-ttu-id="d6767-107">Toutes les méthodes avec préfixe dans le protocole `ms` [DevTools Microsoft Edge (EdgeHTML)](/archive/microsoft-edge/legacy/developer/devtools-protocol/index) ne sont plus pris en charge dans le protocole DevTools Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="d6767-107">Any methods that were prefixed with `ms` in the [Microsoft Edge (EdgeHTML) DevTools Protocol](/archive/microsoft-edge/legacy/developer/devtools-protocol/index) are no longer supported in the Microsoft Edge \(Chromium\) DevTools Protocol.</span></span>  

## <a name="using-the-devtools-protocol"></a><span data-ttu-id="d6767-108">Utilisation du protocole DevTools</span><span class="sxs-lookup"><span data-stu-id="d6767-108">Using the DevTools Protocol</span></span>  

<span data-ttu-id="d6767-109">Voici comment attacher un client d’outils personnalisé au serveur DevTools dans Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="d6767-109">Here's how to attach a custom tooling client to the DevTools Server in Microsoft Edge \(Chromium\).</span></span>  

1.  <span data-ttu-id="d6767-110">Assurez-vous que toutes les instances de Microsoft Edge \(Chromium\) sont fermées.</span><span class="sxs-lookup"><span data-stu-id="d6767-110">Ensure all instances of Microsoft Edge \(Chromium\) are closed.</span></span>  
1.  <span data-ttu-id="d6767-111">Lancez Microsoft Edge \(Chromium\) avec le port de débogage à distance :</span><span class="sxs-lookup"><span data-stu-id="d6767-111">Launch Microsoft Edge \(Chromium\) with the remote debugging port:.</span></span> 
    
    ```shell
    msedge.exe --remote-debugging-port=9222
    ```  
    
1.  <span data-ttu-id="d6767-112">Si vous le souhaitez, vous pouvez démarrer une instance distincte de Edge à l’aide d’un profil utilisateur distinct.</span><span class="sxs-lookup"><span data-stu-id="d6767-112">Optionally, you can start a separate instance of Edge using a distinct user profile if desired.</span></span>  
    
    ```shell
    msedge.exe --user-data-dir=<some directory>
    ```  
    
1.  <span data-ttu-id="d6767-113">Ensuite, utilisez le point de terminaison HTTP `list` pour obtenir la liste des cibles de page attachables.</span><span class="sxs-lookup"><span data-stu-id="d6767-113">Next, use the HTTP `list` endpoint to get a list of attachable page targets.</span></span>  
    
    ```http
    http://localhost:9222/json/list
    ```  
    
1.  <span data-ttu-id="d6767-114">Enfin, connectez-vous à la cible souhaitée et émettre des commandes/s’abonner aux messages d’événement via le serveur `webSocketDebuggerUrl` de socket web DevTools.</span><span class="sxs-lookup"><span data-stu-id="d6767-114">Finally, connect to the `webSocketDebuggerUrl` of the desired target and issue commands/subscribe to event messages through the DevTools web socket server.</span></span>  

## <a name="devtools-protocol-http-endpoints"></a><span data-ttu-id="d6767-115">Points de terminaison HTTP du protocole DevTools</span><span class="sxs-lookup"><span data-stu-id="d6767-115">DevTools Protocol HTTP Endpoints</span></span>  

<span data-ttu-id="d6767-116">Le protocole Microsoft Edge \(Chromium\) DevTools prend en charge les points de terminaison HTTP suivants.</span><span class="sxs-lookup"><span data-stu-id="d6767-116">The Microsoft Edge \(Chromium\) DevTools Protocol supports the following HTTP endpoints.</span></span>  

## <a name="jsonversion"></a><span data-ttu-id="d6767-117">/json/version</span><span class="sxs-lookup"><span data-stu-id="d6767-117">/json/version</span></span>  

<span data-ttu-id="d6767-118">Fournit des informations sur le navigateur de l’ordinateur hôte et sur la version du protocole DevTools qu’il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="d6767-118">Provides information on the browser of the host machine and which version of the DevTools Protocol it supports.</span></span>  

**<span data-ttu-id="d6767-119">Parameters</span><span class="sxs-lookup"><span data-stu-id="d6767-119">Parameters</span></span>**  

**<span data-ttu-id="d6767-120">Aucun(e)</span><span class="sxs-lookup"><span data-stu-id="d6767-120">None</span></span>**  

**<span data-ttu-id="d6767-121">Return, objet</span><span class="sxs-lookup"><span data-stu-id="d6767-121">Return object</span></span>**  

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

## <a name="jsonprotocol"></a><span data-ttu-id="d6767-122">/json/protocol</span><span class="sxs-lookup"><span data-stu-id="d6767-122">/json/protocol</span></span>  

<span data-ttu-id="d6767-123">Fournit l’intégralité de la surface de l’API de protocole sérialisée en tant que JSON.</span><span class="sxs-lookup"><span data-stu-id="d6767-123">Provides the entire protocol API surface serialized as JSON.</span></span>  

**<span data-ttu-id="d6767-124">Parameters</span><span class="sxs-lookup"><span data-stu-id="d6767-124">Parameters</span></span>**  

**<span data-ttu-id="d6767-125">Aucun(e)</span><span class="sxs-lookup"><span data-stu-id="d6767-125">None</span></span>**  

**<span data-ttu-id="d6767-126">Return, objet</span><span class="sxs-lookup"><span data-stu-id="d6767-126">Return object</span></span>**  

<span data-ttu-id="d6767-127">Objet JSON qui représente la surface API disponible pour la version actuelle du protocole.</span><span class="sxs-lookup"><span data-stu-id="d6767-127">JSON object which represents the available API surface for current version of the protocol.</span></span>  

## <a name="jsonlist"></a><span data-ttu-id="d6767-128">/json/list</span><span class="sxs-lookup"><span data-stu-id="d6767-128">/json/list</span></span>  

<span data-ttu-id="d6767-129">Fournit une liste candidate de cibles de page pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="d6767-129">Provides a candidate list of page targets for debugging.</span></span>  

**<span data-ttu-id="d6767-130">Parameters</span><span class="sxs-lookup"><span data-stu-id="d6767-130">Parameters</span></span>**  

**<span data-ttu-id="d6767-131">Aucun(e)</span><span class="sxs-lookup"><span data-stu-id="d6767-131">None</span></span>**  

**<span data-ttu-id="d6767-132">Return, objet</span><span class="sxs-lookup"><span data-stu-id="d6767-132">Return object</span></span>**  

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

## <a name="jsonclose"></a><span data-ttu-id="d6767-133">/json/close</span><span class="sxs-lookup"><span data-stu-id="d6767-133">/json/close</span></span>  

<span data-ttu-id="d6767-134">Ferme le processus cible \(par exemple, dans Microsoft Edge \(Chromium\), ferme l’onglet de page\).</span><span class="sxs-lookup"><span data-stu-id="d6767-134">Closes down the target process \(for example, in Microsoft Edge \(Chromium\), closes the page tab\).</span></span>  

**<span data-ttu-id="d6767-135">Parameters</span><span class="sxs-lookup"><span data-stu-id="d6767-135">Parameters</span></span>**  

<span data-ttu-id="d6767-136">ID cible</span><span class="sxs-lookup"><span data-stu-id="d6767-136">Target ID</span></span>  

**<span data-ttu-id="d6767-137">Return, objet</span><span class="sxs-lookup"><span data-stu-id="d6767-137">Return object</span></span>**  

```
String(“Target is closing”)
```  

## <a name="remote-tools-for-microsoft-edge-beta"></a><span data-ttu-id="d6767-138">Outils à distance pour Microsoft Edge (bêta)</span><span class="sxs-lookup"><span data-stu-id="d6767-138">Remote Tools for Microsoft Edge (Beta)</span></span>  

<span data-ttu-id="d6767-139">Vous pouvez désormais installer les outils à distance [pour Microsoft Edge (bêta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) à partir du [Microsoft Store.](https://www.microsoft.com/store/apps/windows)</span><span class="sxs-lookup"><span data-stu-id="d6767-139">You are now able to install the [Remote Tools for Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) from the [Microsoft Store](https://www.microsoft.com/store/apps/windows).</span></span>  <span data-ttu-id="d6767-140">Cette application vous permet de déboguer à distance Microsoft Edge (Chromium) s’exécutant sur un appareil Windows 10 à partir de votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="d6767-140">This app enables you to remotely debug Microsoft Edge (Chromium) running on a Windows 10 device from your development machine.</span></span>  

<span data-ttu-id="d6767-141">Pour découvrir comment configurer votre appareil Windows 10 et vous y connecter à partir de votre ordinateur de développement, accédez à Démarrer avec le débogage à distance des appareils [Windows 10.](../devtools-guide-chromium/remote-debugging/windows.md)</span><span class="sxs-lookup"><span data-stu-id="d6767-141">To learn how to set up your Windows 10 device and connect to it from your development machine, navigate to [Get Started with Remote Debugging Windows 10 Devices](../devtools-guide-chromium/remote-debugging/windows.md).</span></span>  

<span data-ttu-id="d6767-142">Les outils à distance pour [Microsoft Edge (bêta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) utilisent le même protocole Microsoft Edge (Chromium) [DevTools que devTools](../devtools-guide-chromium/index.md) pour communiquer avec Microsoft Edge en cours d’exécution sur l’appareil Windows 10 que vous souhaitez déboguer.</span><span class="sxs-lookup"><span data-stu-id="d6767-142">The [Remote Tools for Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) uses the same Microsoft Edge (Chromium) DevTools Protocol as the [DevTools](../devtools-guide-chromium/index.md) to communicate with Microsoft Edge running on the Windows 10 device you want to debug.</span></span>  <span data-ttu-id="d6767-143">Cette application est juste précédée d’un ID de processus ( ) avant `/msedge/` `pid` chaque appel au protocole.</span><span class="sxs-lookup"><span data-stu-id="d6767-143">This app just prepends `/msedge/` and a process ID (`pid`) before each call to the protocol.</span></span>  <span data-ttu-id="d6767-144">Il prend en charge les points de terminaison HTTP suivants.</span><span class="sxs-lookup"><span data-stu-id="d6767-144">It supports the following HTTP endpoints.</span></span>  

### <a name="msedgejsonlist"></a><span data-ttu-id="d6767-145">/msedge/json/list</span><span class="sxs-lookup"><span data-stu-id="d6767-145">/msedge/json/list</span></span>  

<span data-ttu-id="d6767-146">Fournit une liste de candidats de tous les processus \(y compris les PVE et tous les onglets dans toutes les instances de Microsoft Edge\) sur l’appareil Windows 10 pour le `msedge.exe` débogage. [](../progressive-web-apps-chromium/index.md)</span><span class="sxs-lookup"><span data-stu-id="d6767-146">Provides a candidate list of all `msedge.exe` processes \(including [PWAs](../progressive-web-apps-chromium/index.md) and all tabs in all instances of Microsoft Edge\) on the Windows 10 device for debugging.</span></span>  

**<span data-ttu-id="d6767-147">Parameters</span><span class="sxs-lookup"><span data-stu-id="d6767-147">Parameters</span></span>**  

**<span data-ttu-id="d6767-148">Aucun(e)</span><span class="sxs-lookup"><span data-stu-id="d6767-148">None</span></span>**  

**<span data-ttu-id="d6767-149">Return, objet</span><span class="sxs-lookup"><span data-stu-id="d6767-149">Return object</span></span>**  

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

### <a name="msedge"></a><span data-ttu-id="d6767-150">/msedge/</span><span class="sxs-lookup"><span data-stu-id="d6767-150">/msedge/</span></span>  

<span data-ttu-id="d6767-151">Fonctionnellement équivalent à [/msedge/json/list](#msedgejsonlist).</span><span class="sxs-lookup"><span data-stu-id="d6767-151">Functionally equivalent to [/msedge/json/list](#msedgejsonlist).</span></span>  

### <a name="msedgepidjsonlist"></a><span data-ttu-id="d6767-152">/msedge/[pid]/json/list</span><span class="sxs-lookup"><span data-stu-id="d6767-152">/msedge/[pid]/json/list</span></span>  

<span data-ttu-id="d6767-153">Fournit une liste candidate de cibles de page pour l’instance de Microsoft Edge qui correspond à celle fournie `[pid]` pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="d6767-153">Provides a candidate list of page targets for the Microsoft Edge instance that matches the provided `[pid]` for debugging.</span></span>  

**<span data-ttu-id="d6767-154">Parameters</span><span class="sxs-lookup"><span data-stu-id="d6767-154">Parameters</span></span>**  

**<span data-ttu-id="d6767-155">Aucun(e)</span><span class="sxs-lookup"><span data-stu-id="d6767-155">None</span></span>**  

**<span data-ttu-id="d6767-156">Return, objet</span><span class="sxs-lookup"><span data-stu-id="d6767-156">Return object</span></span>**  

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

### <a name="msedgepidjsonversion"></a><span data-ttu-id="d6767-157">/msedge/[pid]/json/version</span><span class="sxs-lookup"><span data-stu-id="d6767-157">/msedge/[pid]/json/version</span></span>  

<span data-ttu-id="d6767-158">Fournit des informations sur l’instance de Microsoft Edge qui correspond à la version fournie et la version du protocole `[pid]` DevTools qu’elle prend en charge.</span><span class="sxs-lookup"><span data-stu-id="d6767-158">Provides information about the Microsoft Edge instance that matches the provided `[pid]` and which version of the DevTools Protocol it supports.</span></span>  

**<span data-ttu-id="d6767-159">Parameters</span><span class="sxs-lookup"><span data-stu-id="d6767-159">Parameters</span></span>**  

**<span data-ttu-id="d6767-160">Aucun(e)</span><span class="sxs-lookup"><span data-stu-id="d6767-160">None</span></span>**  

**<span data-ttu-id="d6767-161">Return, objet</span><span class="sxs-lookup"><span data-stu-id="d6767-161">Return object</span></span>**  

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

### <a name="msedgepidjsonprotocol"></a><span data-ttu-id="d6767-162">/msedge/[pid]/json/protocol/</span><span class="sxs-lookup"><span data-stu-id="d6767-162">/msedge/[pid]/json/protocol/</span></span>  

<span data-ttu-id="d6767-163">Fournit l’intégralité de la surface de l’API de protocole sérialisée en tant que JSON pour l’instance de Microsoft Edge qui correspond à la version `[pid]` fournie.</span><span class="sxs-lookup"><span data-stu-id="d6767-163">Provides the entire protocol API surface serialized as JSON for the Microsoft Edge instance that matches the provided `[pid]`.</span></span>  

**<span data-ttu-id="d6767-164">Parameters</span><span class="sxs-lookup"><span data-stu-id="d6767-164">Parameters</span></span>**  

**<span data-ttu-id="d6767-165">Aucun(e)</span><span class="sxs-lookup"><span data-stu-id="d6767-165">None</span></span>**  

**<span data-ttu-id="d6767-166">Return, objet</span><span class="sxs-lookup"><span data-stu-id="d6767-166">Return object</span></span>**  

<span data-ttu-id="d6767-167">Objet JSON qui représente la surface d’API disponible pour la version du protocole que l’instance de Microsoft Edge qui correspond à l’api `[pid]` fournie utilise.</span><span class="sxs-lookup"><span data-stu-id="d6767-167">JSON object which represents the available API surface for the version of the protocol that the Microsoft Edge instance that matches the provided `[pid]` is using.</span></span>  
