---
description: Découvrez les nouveautés de la mise à jour de Microsoft Edge DevTools de Windows 10 octobre 2018
title: Nouveautés de Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, edgehtml 18
ms.custom: RS5, seodec18
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2f1d3c6fe5bf061186d5c6593a115a8b6794c0dd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233259"
---
# <span data-ttu-id="eef94-104">DevTools dans la dernière mise à jour de Windows10 (EdgeHTML 18)</span><span class="sxs-lookup"><span data-stu-id="eef94-104">DevTools in the latest Windows 10 update (EdgeHTML 18)</span></span>

<span data-ttu-id="eef94-105">La dernière mise à jour de Microsoft Edge DevTools ajoute un certain nombre de commodités à l’interface utilisateur et au capot, y compris aux nouveaux panneaux dédiés pour les [*travailleurs de services*](#service-workers-panel) et le [*stockage*](#storage-panel), les outils de [recherche de fichiers](#source-file-search-tools) source dans le débogueur et les API de console et de débogage de type [devtools](#edge-devtools-protocol-updates) .</span><span class="sxs-lookup"><span data-stu-id="eef94-105">The latest update to Microsoft Edge DevTools adds a number of conveniences both to the UI and under the hood, including new dedicated panels for [*Service Workers*](#service-workers-panel) and [*Storage*](#storage-panel), source [file search](#source-file-search-tools) tools in the Debugger, and new [Edge DevTools Protocol domains](#edge-devtools-protocol-updates) for style/layout debugging and console APIs.</span></span>

<span data-ttu-id="eef94-106">Voici les dernières fonctionnalités de Microsoft Edge DevTools disponibles désormais dans la [mise à jour de Windows 10 d’octobre 2018](/windows/uwp/whats-new/windows-10-build-17763) ([EdgeHTML 18](https://aka.ms/devguide_edgehtml_18)).</span><span class="sxs-lookup"><span data-stu-id="eef94-106">Here are the latest Microsoft Edge DevTools features available now in the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) ([EdgeHTML 18](https://aka.ms/devguide_edgehtml_18)).</span></span> <span data-ttu-id="eef94-107">En plus de cela, nous avons également résolu un certain nombre de bogues d’accessibilité, de fiabilité et de performance pour améliorer les notions fondamentales.</span><span class="sxs-lookup"><span data-stu-id="eef94-107">In addition to all this, we’ve also fixed a number of accessibility, reliability, and performance bugs to improve fundamentals!</span></span>

## <span data-ttu-id="eef94-108">Application DevTools</span><span class="sxs-lookup"><span data-stu-id="eef94-108">DevTools app</span></span>

<span data-ttu-id="eef94-109">Nous avons mis à jour l' [application Microsoft Edge devtools Preview](./index.md#microsoft-store-app)autonome.</span><span class="sxs-lookup"><span data-stu-id="eef94-109">We've updated the standalone [Microsoft Edge DevTools Preview app](./index.md#microsoft-store-app).</span></span> <span data-ttu-id="eef94-110">La version la plus récente inclut l’accès au débogage à distance aux funtionality principaux dans le [**débogueur**](./debugger.md), les [**éléments**](./elements.md) (pour les opérations en lecture seule) et les panneaux de [**console**](./console.md) .</span><span class="sxs-lookup"><span data-stu-id="eef94-110">The latest release includes remote debugging access to core funtionality in the [**Debugger**](./debugger.md), [**Elements**](./elements.md) (for read-only operations), and [**Console**](./console.md) panels.</span></span>

## <span data-ttu-id="eef94-111">Panneau des travailleurs de services</span><span class="sxs-lookup"><span data-stu-id="eef94-111">Service Workers panel</span></span>

<span data-ttu-id="eef94-112">Le panneau des travailleurs de [**service**](./service-workers.md) dédié est désormais destiné à l’examen, la gestion et le débogage des travailleurs de service de votre site.</span><span class="sxs-lookup"><span data-stu-id="eef94-112">There's now a dedicated [**Service Workers**](./service-workers.md) panel for inspecting, managing, and debugging your site's service workers.</span></span> <span data-ttu-id="eef94-113">Cela fournit les mêmes fonctionnalités qu’auparavant dans le volet *débogueur* (désormais avec une interface utilisateur moins encombrée).</span><span class="sxs-lookup"><span data-stu-id="eef94-113">This provides the same functionality as was previously in the *Debugger* panel (now with a less-crowded UI!).</span></span>

![Panneau des travailleurs de services](./media/service_worker.png)

## <span data-ttu-id="eef94-115">Panneau de stockage</span><span class="sxs-lookup"><span data-stu-id="eef94-115">Storage panel</span></span>

<span data-ttu-id="eef94-116">Nous avons également déplacé tous les inspecteurs de stockage local (*stockage local et de stockage de groupe, IndexedDB, cookies, cache*) auparavant dans le *débogueur* pour leur propre panneau de [**stockage**](./storage.md) dédié.</span><span class="sxs-lookup"><span data-stu-id="eef94-116">We've also moved all the local storage inspectors (*Local and Sesion Storage, IndexedDB, Cookies, Cache*) previously in the *Debugger* to their own dedicated [**Storage**](./storage.md) panel.</span></span>

![Panneau de stockage](./media/storage_cache.png)

## <span data-ttu-id="eef94-118">Outils de recherche de fichiers sources</span><span class="sxs-lookup"><span data-stu-id="eef94-118">Source file search tools</span></span>

<span data-ttu-id="eef94-119">Le [**débogueur**](./debugger.md) comporte désormais un volet de [recherche de fichier source](./debugger.md#file-search) .</span><span class="sxs-lookup"><span data-stu-id="eef94-119">The [**Debugger**](./debugger.md) now has a [source file search](./debugger.md#file-search) pane.</span></span> <span data-ttu-id="eef94-120">Vous pouvez l’ouvrir à l’aide de la commande *Rechercher dans les fichiers* ( `Ctrl` + `Shift` + `F` ) lorsque vous recherchez une chaîne de code spécifique que vous essayez de rechercher dans la source.</span><span class="sxs-lookup"><span data-stu-id="eef94-120">Open it with the *Find in files* command (`Ctrl`+`Shift`+`F`) when you have a specific string of code you're trying to find in the source.</span></span> <span data-ttu-id="eef94-121">La barre d’outils fournit des options de recherche différentes, y compris des expressions régulières.</span><span class="sxs-lookup"><span data-stu-id="eef94-121">The toolbar provides different search options, including regular expressions.</span></span> 

![Recherche de fichier de débogueur](./media/debugger_file_search.png)

<span data-ttu-id="eef94-123">Vous pouvez également ouvrir rapidement tout fichier source chargé à l’aide de la commande *ouvrir le fichier* ( `Ctrl` + `P` ).</span><span class="sxs-lookup"><span data-stu-id="eef94-123">You can also quickly open any loaded source file with the *Open file* (`Ctrl`+`P`) command.</span></span>

![Débogueur-ouvrir un fichier](./media/debugger_open_file.png)

## <span data-ttu-id="eef94-125">Mises à jour du protocole Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="eef94-125">Edge DevTools Protocol updates</span></span>

<span data-ttu-id="eef94-126">La [Version 0,2](../devtools-protocol/0.2/index.md) du protocole devtools fournit de nouveaux domaines pour le débogage de style et de mise en page (lecture seule) et les API de console, en plus de la fonctionnalité de débogage de script principal introduite dans la [version 0,1](../devtools-protocol/0.1/index.md).</span><span class="sxs-lookup"><span data-stu-id="eef94-126">[Version 0.2](../devtools-protocol/0.2/index.md) of the DevTools Protocol provides new domains for style and layout (read-only) debugging and console APIs, in addition to the core script debugging functionality introduced in [Version 0.1](../devtools-protocol/0.1/index.md).</span></span> <span data-ttu-id="eef94-127">Dans l’interface utilisateur de DevTools Edge, cela se traduit par une fonctionnalité disponible dans les [**éléments**](../devtools-guide/elements.md) (pour les opérations en lecture seule), les panneaux de [**console**](../devtools-guide/console.md) et de [**débogueur**](../devtools-guide/debugger.md) .</span><span class="sxs-lookup"><span data-stu-id="eef94-127">In the Edge DevTools UI, this translates to functionality available in the [**Elements**](../devtools-guide/elements.md) (for read-only operations), [**Console**](../devtools-guide/console.md) and [**Debugger**](../devtools-guide/debugger.md) panels.</span></span>
