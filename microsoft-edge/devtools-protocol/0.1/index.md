---
description: Notes de publication de la version 0,1 du protocole Microsoft Edge DevTools
title: Notes de publication de la version 0,1 du protocole DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 3c0648467c20572a525fe257788068966efd193c
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104734"
---
# <span data-ttu-id="07abf-103">Notes de publication de la version 0,1 du protocole DevTools</span><span class="sxs-lookup"><span data-stu-id="07abf-103">DevTools Protocol Version 0.1 Release Notes</span></span>

> [!NOTE]
> <span data-ttu-id="07abf-104">Le protocole Microsoft Edge DevTools fonctionne uniquement sur les [mises à jour de Windows 10 d’avril 2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) et les versions ultérieures de [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="07abf-104">The Microsoft Edge DevTools Protocol works only on [Windows 10 April 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) and later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) builds.</span></span>

<span data-ttu-id="07abf-105">La version 0,1 du **protocole Microsoft Edge devtools** fournit une version d’évaluation préliminaire pour le test de l’instrumentation EdgeHTML et du débogage à distance de base dans la nouvelle application [Microsoft Edge devtools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) autonome.</span><span class="sxs-lookup"><span data-stu-id="07abf-105">Version 0.1 of the Microsoft **Edge DevTools Protocol** provides an early preview for testing EdgeHTML instrumentation and basic remote debugging in the new standalone [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) app.</span></span> <span data-ttu-id="07abf-106">C’est pourquoi il est nécessaire d’exécuter la [mise à jour de Windows 10 d’avril 2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) ou une version ultérieure de [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="07abf-106">As such, it requires you to be running [Windows 10 April 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) or a later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) build.</span></span>

<span data-ttu-id="07abf-107">Les objectifs situés derrière le protocole DevTools sont à trois volets:</span><span class="sxs-lookup"><span data-stu-id="07abf-107">The goals behind the DevTools Protocol are three-fold:</span></span>

 - <span data-ttu-id="07abf-108">Fournir une API publique pour notre application DevTools à associer à Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="07abf-108">Provide a public API for our DevTools app to attach to Microsoft Edge</span></span>
 - <span data-ttu-id="07abf-109">Développer l’accès à la fonctionnalité DevTools aux clients d’outils externes</span><span class="sxs-lookup"><span data-stu-id="07abf-109">Expand access of DevTools functionality to external tooling clients</span></span>
 - <span data-ttu-id="07abf-110">Activez le débogage à distance sur la gamme d’appareils Windows 10 exécutant Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="07abf-110">Enable remote debugging across the range of Windows 10 devices running Microsoft Edge</span></span> 

<span data-ttu-id="07abf-111">Cette version préliminaire fournit une fonctionnalité de débogage de base, comme la définition de points d’arrêt, l’exécution du code et l’exploration des traces de pile.</span><span class="sxs-lookup"><span data-stu-id="07abf-111">This preliminary release provides core debugging functionality, such as setting breakpoints, stepping through code, and exploring stack traces.</span></span> <span data-ttu-id="07abf-112">Dans l’interface utilisateur de DevTools Edge, cela se traduit par une fonctionnalité disponible dans le volet [**débogueur**](../../devtools-guide/debugger.md) , l’inspection du cache (pour le stockage Web, le travailleur de service, l’API de cache et IndexedDB).</span><span class="sxs-lookup"><span data-stu-id="07abf-112">In the Edge DevTools UI, this translates to functionality available in the [**Debugger**](../../devtools-guide/debugger.md) panel, minus cache inspection (for Web storage, Service worker, Cache API, and IndexedDB).</span></span> 

<span data-ttu-id="07abf-113">Les fonctionnalités de débogueur supplémentaires seront ajoutées dans les versions à venir, suivies de l’instrumentation qui alimente d’autres panneaux [devtools](../../devtools-guide.md) .</span><span class="sxs-lookup"><span data-stu-id="07abf-113">Further debugger functionality will be added in upcoming releases, followed by the instrumentation powering other [DevTools](../../devtools-guide.md) panels.</span></span>
