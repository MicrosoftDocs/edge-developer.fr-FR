---
description: Notes de publication de la version 0,2 du protocole Microsoft Edge DevTools
title: Notes de publication de la version 0,2 du protocole Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: c4959d2905f95c2bcf98cb78ad67bb88ecfec959
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104741"
---
# <span data-ttu-id="582fc-103">Notes de publication de la version 0,2 du protocole DevTools</span><span class="sxs-lookup"><span data-stu-id="582fc-103">DevTools Protocol Version 0.2 Release Notes</span></span>

> [!NOTE]
> <span data-ttu-id="582fc-104">La version 0,2 du protocole Microsoft Edge DevTools fonctionne uniquement avec la [mise à jour de Windows 10 d’octobre 2018](/windows/uwp/whats-new/windows-10-build-17763) et les versions ultérieures de [Windows Insider Preview](https://insider.windows.com/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="582fc-104">Version 0.2 of the Microsoft Edge DevTools Protocol works only on the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) and later [Windows Insider Preview](https://insider.windows.com/getting-started/) builds.</span></span>

<span data-ttu-id="582fc-105">La version 0,2 du **protocole Microsoft Edge devtools** fournit un aperçu de test de l’instrumentation EdgeHTML et de la version de débogage à distance de base dans la nouvelle application [Microsoft Edge devtools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) autonome.</span><span class="sxs-lookup"><span data-stu-id="582fc-105">Version 0.2 of the Microsoft **Edge DevTools Protocol** provides a preview for testing EdgeHTML instrumentation and basic remote debugging in the new standalone [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) app.</span></span> <span data-ttu-id="582fc-106">C’est pourquoi il est nécessaire d’exécuter la [mise à jour de Windows 10 octobre 2018](/windows/uwp/whats-new/windows-10-build-17763) ou une version ultérieure de [Windows Insider Preview](https://insider.windows.com/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="582fc-106">As such, it requires you to be running the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) or a later [Windows Insider Preview](https://insider.windows.com/getting-started/) build.</span></span>

<span data-ttu-id="582fc-107">Les objectifs situés derrière le protocole DevTools sont à trois volets:</span><span class="sxs-lookup"><span data-stu-id="582fc-107">The goals behind the DevTools Protocol are three-fold:</span></span>

 - <span data-ttu-id="582fc-108">Fournir une API publique pour notre application DevTools à associer à Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="582fc-108">Provide a public API for our DevTools app to attach to Microsoft Edge</span></span>
 - <span data-ttu-id="582fc-109">Développer l’accès à la fonctionnalité DevTools aux clients d’outils externes</span><span class="sxs-lookup"><span data-stu-id="582fc-109">Expand access of DevTools functionality to external tooling clients</span></span>
 - <span data-ttu-id="582fc-110">Activez le débogage à distance sur la gamme d’appareils Windows 10 exécutant Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="582fc-110">Enable remote debugging across the range of Windows 10 devices running Microsoft Edge</span></span> 

<span data-ttu-id="582fc-111">La version 0,2 du protocole DevTools inclut de nouveaux domaines pour le débogage de style et de mise en page (lecture seule) et les API de console, en plus de la fonctionnalité de débogage de script principal introduite dans la version 0,1.</span><span class="sxs-lookup"><span data-stu-id="582fc-111">Version 0.2 of the DevTools Protocol includes new domains for style and layout (read-only) debugging and console APIs, in addition to the core script debugging functionality introduced in Version 0.1.</span></span> <span data-ttu-id="582fc-112">Dans l’interface utilisateur de DevTools Edge, cela se traduit par une fonctionnalité disponible dans les panneaux [**éléments**](../../devtools-guide/elements.md), [**console**](../../devtools-guide/console.md) et [**débogueur**](../../devtools-guide/debugger.md)  .</span><span class="sxs-lookup"><span data-stu-id="582fc-112">In the Edge DevTools UI, this translates to functionality available in the [**Elements**](../../devtools-guide/elements.md), [**Console**](../../devtools-guide/console.md) and [**Debugger**](../../devtools-guide/debugger.md)  panels.</span></span>
