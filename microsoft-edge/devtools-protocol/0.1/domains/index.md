---
description: Liste de références pour les domaines pris en charge dans la version 0,1 du protocole Microsoft Edge DevTools.
title: Domains-protocole DevTools version 0,1
author: pelavall
ms.author: pelavall
ms.date: 12/15/2017
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: b3cf3411a8402b7407012eb789f8bf267b4997a8
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565487"
---
# <span data-ttu-id="7a941-103">Domaines de protocole DevTools</span><span class="sxs-lookup"><span data-stu-id="7a941-103">DevTools Protocol Domains</span></span>
## [<span data-ttu-id="7a941-104">Débogueur</span><span class="sxs-lookup"><span data-stu-id="7a941-104">Debugger</span></span>](debugger.md)
<span data-ttu-id="7a941-105">Le domaine du débogueur expose les fonctionnalités de débogage JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7a941-105">Debugger domain exposes JavaScript debugging capabilities.</span></span> <span data-ttu-id="7a941-106">Elle permet de définir et de supprimer des points d’arrêt, de parcourir l’exécution, d’explorer les traces de pile, etc.</span><span class="sxs-lookup"><span data-stu-id="7a941-106">It allows setting and removing breakpoints, stepping through execution, exploring stack traces, etc.</span></span>
## [<span data-ttu-id="7a941-107">Page</span><span class="sxs-lookup"><span data-stu-id="7a941-107">Page</span></span>](page.md)
<span data-ttu-id="7a941-108">Les actions et événements liés à la page inspectée appartiennent au domaine de la page.</span><span class="sxs-lookup"><span data-stu-id="7a941-108">Actions and events related to the inspected page belong to the page domain.</span></span>
## [<span data-ttu-id="7a941-109">Runtime</span><span class="sxs-lookup"><span data-stu-id="7a941-109">Runtime</span></span>](runtime.md)
<span data-ttu-id="7a941-110">Le domaine d’exécution expose le runtime JavaScript au moyen de l’évaluation à distance et des objets miroirs.</span><span class="sxs-lookup"><span data-stu-id="7a941-110">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="7a941-111">Les résultats d’évaluation sont retournés sous la forme d’un objet miroir exposant le type d’objet, la représentation de chaîne et l’identificateur unique qui peuvent être utilisés pour une référence d’objet supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="7a941-111">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="7a941-112">Les objets d’origine sont conservés en mémoire, sauf s’ils sont explicitement émis.</span><span class="sxs-lookup"><span data-stu-id="7a941-112">Original objects are maintained in memory unless they are either explicitly released.</span></span>
## [<span data-ttu-id="7a941-113">Schéma</span><span class="sxs-lookup"><span data-stu-id="7a941-113">Schema</span></span>](schema.md)
<span data-ttu-id="7a941-114">Fournit des informations sur le schéma de protocole.</span><span class="sxs-lookup"><span data-stu-id="7a941-114">Provides information about the protocol schema.</span></span>