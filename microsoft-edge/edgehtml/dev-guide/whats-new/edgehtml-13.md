---
description: Cette page fournit une vue d’ensemble des nouveautés de EdgeHTML 13.
title: Nouvelles fonctionnalités et API dans EdgeHTML 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2119e576a637d5f78e073f49a3cb1868a7ce1ca4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233456"
---
# <span data-ttu-id="1f7e3-104">Nouveautés de EdgeHTML 13</span><span class="sxs-lookup"><span data-stu-id="1f7e3-104">What's new in EdgeHTML 13</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="1f7e3-105">Voici les modifications apportées à EdgeHTML 13, le moteur permettant d’alimenter le navigateur Microsoft Edge dans la [première mise à jour majeure](https://blogs.windows.com/windowsexperience/2015/11/12) de Windows 10 \ (11/2015, Build 10586 \).</span><span class="sxs-lookup"><span data-stu-id="1f7e3-105">Here are the changes shipped with EdgeHTML 13, the engine powering the Microsoft Edge browser in the [first major update](https://blogs.windows.com/windowsexperience/2015/11/12) for Windows 10 \(11/2015, Build 10586\).</span></span>  <span data-ttu-id="1f7e3-106">Pour obtenir une vue d’ensemble des modifications apportées au navigateur Microsoft Edge global, voir présentation de la [mise à jour de l’EdgeHTML 13, notre première plate-forme pour Microsoft Edge](https://blogs.windows.com/msedgedev/2015/11/16).</span><span class="sxs-lookup"><span data-stu-id="1f7e3-106">For an overview of changes to the overall Microsoft Edge browser, see [Introducing EdgeHTML 13, our first platform update for Microsoft Edge](https://blogs.windows.com/msedgedev/2015/11/16).</span></span>  

<span data-ttu-id="1f7e3-107">Vous trouverez ci-dessous le lien permanent pour la liste des modifications suivante:  [https://aka.ms/devguide_edgehtml_13](./edgehtml-13.md) .</span><span class="sxs-lookup"><span data-stu-id="1f7e3-107">Here's the permalink for the following list of changes:  [https://aka.ms/devguide_edgehtml_13](./edgehtml-13.md).</span></span>  

## <span data-ttu-id="1f7e3-108">Fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="1f7e3-108">Features</span></span>  

### <span data-ttu-id="1f7e3-109">CSS</span><span class="sxs-lookup"><span data-stu-id="1f7e3-109">CSS</span></span>  

<span data-ttu-id="1f7e3-110">EdgeHTML 13 prend en charge les nouvelles fonctionnalités de CSS, notamment:</span><span class="sxs-lookup"><span data-stu-id="1f7e3-110">EdgeHTML 13 supports new CSS features, including:</span></span>  

*   [<span data-ttu-id="1f7e3-111">Pseudo-classes CSS de la mutabilité</span><span class="sxs-lookup"><span data-stu-id="1f7e3-111">CSS Mutability Pseudo-classes</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/cssmutabilitypseudoclasses)  
*   [<span data-ttu-id="1f7e3-112">Pseudo-classes de la plage CSS</span><span class="sxs-lookup"><span data-stu-id="1f7e3-112">CSS Range Pseudo-classes</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/cssrangepseudoclasses)  
*   <span data-ttu-id="1f7e3-113">Mots-clés CSS [initial](https://developer.microsoft.com/microsoft-edge/platform/status/cssinitialvalue) et [unset](https://developer.microsoft.com/microsoft-edge/platform/status/cssunsetvalue)</span><span class="sxs-lookup"><span data-stu-id="1f7e3-113">CSS [initial](https://developer.microsoft.com/microsoft-edge/platform/status/cssinitialvalue) and [unset](https://developer.microsoft.com/microsoft-edge/platform/status/cssunsetvalue) keywords</span></span>  

### <span data-ttu-id="1f7e3-114">Extensions multimédias chiffrées</span><span class="sxs-lookup"><span data-stu-id="1f7e3-114">Encrypted Media Extensions</span></span>  

<span data-ttu-id="1f7e3-115">Microsoft Edge prend désormais en charge les API d' [extensions de média chiffrées](https://w3.org/TR/encrypted-media) sans préfixe.</span><span class="sxs-lookup"><span data-stu-id="1f7e3-115">Microsoft Edge now supports the new unprefixed [Encrypted Media Extensions](https://w3.org/TR/encrypted-media) APIs.</span></span>  <span data-ttu-id="1f7e3-116">Extensions multimédias chiffrées \ (Encrypted \) étend les éléments vidéo et audio pour activer le contenu protégé par la gestion des droits numériques (DRM) sans utiliser les plug-ins.  En savoir plus sur Encrypted:  [extensions multimédias chiffrées](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API).</span><span class="sxs-lookup"><span data-stu-id="1f7e3-116">Encrypted Media Extensions \(EME\) extends the video and audio elements to enable Digital Rights Management \(DRM\) protected content without using plug-ins.  Read more about EME:  [Encrypted Media Extensions](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API).</span></span>  

### <span data-ttu-id="1f7e3-117">Graphiques</span><span class="sxs-lookup"><span data-stu-id="1f7e3-117">Graphics</span></span>  

<span data-ttu-id="1f7e3-118">EdgeHTML 13 présente les mises à jour graphiques suivantes:</span><span class="sxs-lookup"><span data-stu-id="1f7e3-118">EdgeHTML 13 introduces the following graphics updates:</span></span>  

*   [<span data-ttu-id="1f7e3-119">Ellipse de zone de dessin</span><span class="sxs-lookup"><span data-stu-id="1f7e3-119">Canvas ellipse</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/canvas2dellipse)  
*   [<span data-ttu-id="1f7e3-120">Modes de fusion de canevas</span><span class="sxs-lookup"><span data-stu-id="1f7e3-120">Canvas blending modes</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/compositingandblendingincanvas2d)  
*   [<picture> <span data-ttu-id="1f7e3-121">élément</span><span class="sxs-lookup"><span data-stu-id="1f7e3-121">element</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/pictureelement)  
*   [<span data-ttu-id="1f7e3-122">Contenu externe SVG</span><span class="sxs-lookup"><span data-stu-id="1f7e3-122">SVG external content</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/svgexternalcontent)  

### <span data-ttu-id="1f7e3-123">JavaScript</span><span class="sxs-lookup"><span data-stu-id="1f7e3-123">JavaScript</span></span>  

<span data-ttu-id="1f7e3-124">EdgeHTML 13 inclut des [améliorations majeures et une nouvelle prise en charge des fonctionnalités dans Chakra](https://blogs.windows.com/msedgedev/2015/09/30), le moteur JavaScript permettant d’alimenter Microsoft Edge, notamment:</span><span class="sxs-lookup"><span data-stu-id="1f7e3-124">EdgeHTML 13 includes [major improvements and new feature support in Chakra](https://blogs.windows.com/msedgedev/2015/09/30), the JavaScript engine powering Microsoft Edge, including:</span></span>  

#### <span data-ttu-id="1f7e3-125">Nouvelles fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="1f7e3-125">New features</span></span>  

<span data-ttu-id="1f7e3-126">Activé par défaut</span><span class="sxs-lookup"><span data-stu-id="1f7e3-126">On by default</span></span>  

*   <span data-ttu-id="1f7e3-127">[asm.js](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=asm.js) activé par défaut \ ([billet de blog](https://blogs.windows.com/msedgedev/2015/11/10), [démonstration](https://dev.windows.com/microsoft-edge/testdrive/demos/chess)\)</span><span class="sxs-lookup"><span data-stu-id="1f7e3-127">[asm.js](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=asm.js) enabled by default \([blog post](https://blogs.windows.com/msedgedev/2015/11/10), [demo](https://dev.windows.com/microsoft-edge/testdrive/demos/chess)\)</span></span>  
*   <span data-ttu-id="1f7e3-128">[Cours](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=classes) \ (ES2015 \)</span><span class="sxs-lookup"><span data-stu-id="1f7e3-128">[Classes](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=classes) \(ES2015\)</span></span>  

#### <span data-ttu-id="1f7e3-129">Fonctionnalités JavaScript expérimentales</span><span class="sxs-lookup"><span data-stu-id="1f7e3-129">Experimental JavaScript features</span></span>  

<span data-ttu-id="1f7e3-130">Activé avec</span><span class="sxs-lookup"><span data-stu-id="1f7e3-130">Enabled with</span></span> `about:flags`  

*   <span data-ttu-id="1f7e3-131">[Fonctions Async](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctions/?q=async%20functions) \ (ES2016 \)</span><span class="sxs-lookup"><span data-stu-id="1f7e3-131">[Async functions](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctions/?q=async%20functions) \(ES2016\)</span></span>  
*   <span data-ttu-id="1f7e3-132">[Opérateur d’élévation](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016/?q=exponentiation%20operator) à la puissance \ (ES2016 \)</span><span class="sxs-lookup"><span data-stu-id="1f7e3-132">[Exponentiation operator](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016/?q=exponentiation%20operator) \(ES2016\)</span></span>  
*   <span data-ttu-id="1f7e3-133">[Structuration](https://developer.microsoft.com/microsoft-edge/platform/status/destructuringES2015/?q=destructuring) de \ (ES2015 \)</span><span class="sxs-lookup"><span data-stu-id="1f7e3-133">[Destructuring](https://developer.microsoft.com/microsoft-edge/platform/status/destructuringES2015/?q=destructuring) \(ES2015\)</span></span>  

### <span data-ttu-id="1f7e3-134">Entrée de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="1f7e3-134">User Input</span></span>  

<span data-ttu-id="1f7e3-135">Les fonctionnalités suivantes introduites dans EdgeHTML 13 améliorent l’entrée utilisateur:</span><span class="sxs-lookup"><span data-stu-id="1f7e3-135">The following features introduced in EdgeHTML 13 improve user input:</span></span>  

*   [\<meter\> <span data-ttu-id="1f7e3-136">élément</span><span class="sxs-lookup"><span data-stu-id="1f7e3-136">element</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/meterelement)  
*   [<span data-ttu-id="1f7e3-137">gestionnaire d’événements oninvalid pour le document d’élément et la fenêtre</span><span class="sxs-lookup"><span data-stu-id="1f7e3-137">oninvalid event handler for the element document and window</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/oninvalideventhandler)  

### <span data-ttu-id="1f7e3-138">Verrouillage du pointeur</span><span class="sxs-lookup"><span data-stu-id="1f7e3-138">Pointer Lock</span></span>  

<span data-ttu-id="1f7e3-139">Microsoft Edge prend désormais en charge l’API de verrouillage de pointeur (auparavant appelée le verrouillage de la souris) pour accéder au mouvement brut de la souris, en verrouillant la cible des événements de souris sur un élément unique, ce qui évite de limiter la distance de déplacement de la souris dans une seule direction, et de supprimer le curseur de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="1f7e3-139">Microsoft Edge now supports the Pointer Lock API \(previously called Mouse Lock\) for access to raw mouse movement, locking the target of mouse events to a single element, eliminating limits of how far mouse movement can go in a single direction, and removing the cursor from view.</span></span>  

## <span data-ttu-id="1f7e3-140">Nouvelles API dans EdgeHTML 13</span><span class="sxs-lookup"><span data-stu-id="1f7e3-140">New APIs in EdgeHTML 13</span></span>  

<span data-ttu-id="1f7e3-141">Voici la liste complète des nouvelles API dans EdgeHTML 13.</span><span class="sxs-lookup"><span data-stu-id="1f7e3-141">Here's the full list of new APIs in EdgeHTML 13.</span></span>  <span data-ttu-id="1f7e3-142">Ils sont répertoriés au format de `[interface name].[api name]` .</span><span class="sxs-lookup"><span data-stu-id="1f7e3-142">They are listed in the format of `[interface name].[api name]`.</span></span>  

<iframe height='584' scrolling='no' title='<span data-ttu-id="1f7e3-143">Nouvelles API dans EdgeHTML 13</span><span class="sxs-lookup"><span data-stu-id="1f7e3-143">New APIs in EdgeHTML 13</span></span>' src='//codepen.io/MicrosoftEdgeDocumentation/embed/vmzxEY/?height=584&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width:  100%;'><span data-ttu-id="1f7e3-144">Reportez-vous au stylo <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/vmzxEY/'> nouvelles API dans EdgeHTML 13 </a> par Microsoft Edge Docs ( <a href='http://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) sur <a href='http://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="1f7e3-144">See the Pen <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/vmzxEY/'>New APIs in EdgeHTML 13</a> by Microsoft Edge Docs (<a href='http://codepen.io/MicrosoftEdgeDocumentation'>@MicrosoftEdgeDocumentation</a>) on <a href='http://codepen.io'>CodePen</a>.</span></span></iframe>  
