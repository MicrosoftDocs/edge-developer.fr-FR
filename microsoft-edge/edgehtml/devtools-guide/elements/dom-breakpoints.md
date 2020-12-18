---
description: Utiliser des points d’arrêt DOM pour déboguer visuellement des problèmes de disposition sur votre page
title: Éléments DevTools-points d’arrêt DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, éléments, points d’arrêt DOM et mutation DOM
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cb60fa0497c98c152ca2c5adf28e9dee5d7c9f98
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233074"
---
# <span data-ttu-id="e34d3-104">Points d’arrêt DOM</span><span class="sxs-lookup"><span data-stu-id="e34d3-104">DOM breakpoints</span></span>

<span data-ttu-id="e34d3-105">Gérez vos points d’arrêt de mutation DOM depuis ce volet, y compris la désactivation, la suppression et la reliaison.</span><span class="sxs-lookup"><span data-stu-id="e34d3-105">Manage your DOM mutation breakpoints from this pane, including disabling, deleting and rebinding them.</span></span>

<span data-ttu-id="e34d3-106">Vous pouvez utiliser des points d’arrêt de mutation DOM pour vous arrêter dans le débogueur dès qu’un nœud d’élément sélectionné change.</span><span class="sxs-lookup"><span data-stu-id="e34d3-106">You can use DOM mutation breakpoints to break into the debugger whenever a selected element node changes.</span></span> <span data-ttu-id="e34d3-107">Cela s’avère utile pour identifier le code responsable de l’origine des problèmes visuels liés à votre interface utilisateur, sans avoir à définir des points d’arrêt individuels sur chacune des API 450 + DOM dans *EdgeHTML* qui peut déclencher de telles modifications.</span><span class="sxs-lookup"><span data-stu-id="e34d3-107">This is helpful for tracking down the code responsible for causing visual glitches with your UI without having to set individual breakpoints on each of the 450+ DOM APIs in *EdgeHTML* that can trigger such changes.</span></span> 

<span data-ttu-id="e34d3-108">Pour définir un point d’arrêt DOM, cliquez avec le bouton droit sur un élément dans l' *arborescence html* du panneau **éléments** pour ouvrir le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="e34d3-108">To set a DOM breakpoint, right-click on any element in the **Elements** panel *HTML tree view* to open the context menu.</span></span>

![Menu contextuel des points d’arrêt DOM](../media/elements_dom_breakpoints_contextmenu.png)

<span data-ttu-id="e34d3-110">Vous pouvez définir n’importe quel points d’arrêt suivants:</span><span class="sxs-lookup"><span data-stu-id="e34d3-110">You can set any of the following breakpoints:</span></span>

 - <span data-ttu-id="e34d3-111">**Arrêt du nœud supprimé**: arrêter dans le débogueur lorsque l’élément sélectionné est supprimé du document (arborescence DOM).</span><span class="sxs-lookup"><span data-stu-id="e34d3-111">**Break on Node removed**: Break into the debugger when the selected element is removed from the document (DOM tree).</span></span>

 - <span data-ttu-id="e34d3-112">**Saut de la sous-arborescence modifié**: s’arrête dans le débogueur lorsque l’un des descendants de l’élément sélectionné est modifié (ajouté, supprimé ou ses sous-arbres sont modifiés).</span><span class="sxs-lookup"><span data-stu-id="e34d3-112">**Break on Subtree modified**: Break into the debugger when any of the descendants of the selected element are changed (added, removed, or their subtrees are modified).</span></span> <span data-ttu-id="e34d3-113">Cela ne sera pas interrompu lors de la modification des attributs (Voir l’option suivante).</span><span class="sxs-lookup"><span data-stu-id="e34d3-113">This will not break when attributes are modified (see the next option for that).</span></span>

 - <span data-ttu-id="e34d3-114">**Arrêt sur l’attribut modifié**: s’arrête dans le débogueur lors de l’ajout, de la suppression ou de la modification d’un attribut de l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e34d3-114">**Break on Attribute modified**: Break into the debugger when an attribute of the selected element is added, removed or changed in value.</span></span>

<span data-ttu-id="e34d3-115">Le volet **points d’arrêt DOM** répertorie les éléments sélectionnés (en générant un sélecteur décrivant son emplacement dans le DOM) et les types de points d’arrêt que vous avez définis (*nœud supprimé, sous-arborescence modifié, attribut modifié*).</span><span class="sxs-lookup"><span data-stu-id="e34d3-115">The **DOM breakpoints** pane will then list the selected element (by generating a selector describing its location in the DOM) and the types of breakpoints you have set (*Node removed, Subtree modified, Attribute modified*).</span></span> <span data-ttu-id="e34d3-116">À partir de cet emplacement, vous pouvez également *relier*, *Désactiver*ou *supprimer* vos points d’arrêt, individuellement (à partir du menu contextuel de RT-clic) ou tous à la fois (à l’aide des boutons).</span><span class="sxs-lookup"><span data-stu-id="e34d3-116">From here, you can also *rebind*, *disable*, or *delete* your breakpoints, individually (from the rt-click context menu) or all at once (using the buttons).</span></span>

![Volet points d’arrêt DOM](../media/elements_dom_breakpoints.png)

## <span data-ttu-id="e34d3-118">Persistance de point d’arrêt</span><span class="sxs-lookup"><span data-stu-id="e34d3-118">Breakpoint persistence</span></span>

<span data-ttu-id="e34d3-119">Les points d’arrêt sont stockés (et associés à l’URL de la page dans laquelle ils sont définis) dans le cadre de vos paramètres DevTools.</span><span class="sxs-lookup"><span data-stu-id="e34d3-119">Breakpoints are stored (and scoped to the URL of the page they're set within) as part of your DevTools settings.</span></span> <span data-ttu-id="e34d3-120">Lors du rechargement de la page ou de la fermeture et de la réouverture des outils, DevTools tente de lier vos points d’arrêt aux éléments associés.</span><span class="sxs-lookup"><span data-stu-id="e34d3-120">When the page is reloaded or the tools are closed and reopened, DevTools will attempt to rebind your breakpoints to their associated elements.</span></span>

<span data-ttu-id="e34d3-121">Les points d’arrêt qui ne peuvent pas être automatiquement réliés sont indiqués par une icône d’avertissement sur le cercle de point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="e34d3-121">Breakpoints that couldn't be automatically rebinded are indicated with a warning icon on the breakpoint circle.</span></span> <span data-ttu-id="e34d3-122">Pour ces derniers, vous pouvez attendre de lier de nouveau l’élément manuellement (à l’aide du bouton **rélier le point d’arrêt** et/ou de l’option de menu contextuel) une fois qu’un élément correspondant apparaît dans le DOM (et que l’icône de point d’arrêt n’affiche plus l’indicateur d’avertissement) ou que vous **supprimez** le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="e34d3-122">For these, you can wait to rebind the element manually (using the **Rebind breakpoint** button and/or context menu option) once a corresponding element appears in the DOM (and the breakpoint icon no longer shows the warning indicator), or **Delete** the breakpoint altogether.</span></span>

![Indicateur de point d’arrêt indépendant](../media/elements_dom_breakpoint_unbound.png)

<span data-ttu-id="e34d3-124">Outre ce volet de *points d’arrêt DOM* , vous pouvez également gérer vos [points d’arrêt DOM](../debugger.md#dom-breakpoints) à partir du **débogueur**.</span><span class="sxs-lookup"><span data-stu-id="e34d3-124">In addition to this *DOM breakpoints* pane, you can also manage your [DOM breakpoints](../debugger.md#dom-breakpoints) from within the **Debugger**.</span></span>

## <span data-ttu-id="e34d3-125">Limitations actuelles</span><span class="sxs-lookup"><span data-stu-id="e34d3-125">Current limitations</span></span>

<span data-ttu-id="e34d3-126">Gardez à l’esprit les limitations suivantes relatives au débogage de points d’arrêt DOM dans Edge DevTools:</span><span class="sxs-lookup"><span data-stu-id="e34d3-126">Please be aware of the following limitations of DOM breakpoint debugging in Edge DevTools:</span></span>

- <span data-ttu-id="e34d3-127">Edge DevTools ne prend actuellement pas en charge les points d’arrêt de reliaison au sein de [ `<iframe>` s](https://developer.mozilla.org/docs/Web/HTML/Element/iframe).</span><span class="sxs-lookup"><span data-stu-id="e34d3-127">Edge DevTools don't currently support rebinding breakpoints inside of [`<iframe>`s](https://developer.mozilla.org/docs/Web/HTML/Element/iframe).</span></span> <span data-ttu-id="e34d3-128">Si vous définissez un point d’arrêt dans un IFRAME et fermez le DevTools de bord ou actualisez la page, le point d’arrêt sera perdu.</span><span class="sxs-lookup"><span data-stu-id="e34d3-128">If you set a breakpoint in an iframe and close Edge DevTools or refresh the page, the breakpoint will be lost.</span></span>

- <span data-ttu-id="e34d3-129">Si votre script rencontre un point d’arrêt asynchrone avant la fin de l’exécution du DOM [`readyState`](https://developer.mozilla.org/docs/Web/API/Document/readyState) , vous ne serez pas en mesure de définir un point d’arrêt DOM lorsque le débogueur est suspendu.</span><span class="sxs-lookup"><span data-stu-id="e34d3-129">If your script encounters a synchronously-executed breakpoint before the DOM [`readyState`](https://developer.mozilla.org/docs/Web/API/Document/readyState) is completed, you won't be able to set a DOM breakpoint while the debugger is paused.</span></span> <span data-ttu-id="e34d3-130">En règle générale, vous pouvez résoudre ce problème en définissant les [`defer`](https://developer.mozilla.org/docs/Web/HTML/Element/script#Attributes) attributs ou les [`async`](https://developer.mozilla.org/docs/Web/HTML/Element/script#Attributes) attributs de script.</span><span class="sxs-lookup"><span data-stu-id="e34d3-130">You can typically remedy this situation by setting the [`defer`](https://developer.mozilla.org/docs/Web/HTML/Element/script#Attributes) or [`async`](https://developer.mozilla.org/docs/Web/HTML/Element/script#Attributes) script attributes.</span></span>

- <span data-ttu-id="e34d3-131">Pour les scripts synchrones, nous déclencherons la reliaison automatique des points d’arrêt lorsque l' [`window.onload`](https://developer.mozilla.org/docs/Web/API/GlobalEventHandlers/onload) événement est appelé.</span><span class="sxs-lookup"><span data-stu-id="e34d3-131">For synchronous scripts, we trigger automatic rebinding of breakpoints when the [`window.onload`](https://developer.mozilla.org/docs/Web/API/GlobalEventHandlers/onload) event is called.</span></span> <span data-ttu-id="e34d3-132">Dans le cas présent, il est possible que nous manquerons des points d’arrêt de liaison qui déclenchent la génération initiale du DOM par script.</span><span class="sxs-lookup"><span data-stu-id="e34d3-132">In this case, we may miss binding breakpoints that would trigger during initial script-driven build-up of the DOM.</span></span> <span data-ttu-id="e34d3-133">Pour les scripts asynchrones, nous déclenchons une tentative de reliaison avant que le premier script ne s’exécute, afin que vos points d’arrêt puissent se relier et déclencher le déclenchement souhaité.</span><span class="sxs-lookup"><span data-stu-id="e34d3-133">For asynchronous scripts, we trigger a rebind attempt before the first script executes, so your breakpoints may rebind and trigger as desired.</span></span>
