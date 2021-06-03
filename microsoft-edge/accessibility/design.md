---
description: Découvrez les ressources pour les meilleures pratiques et les outils de conception inclusive.
title: 'Accessibilité : conception'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/27/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 8468f8e1-9f4a-426c-a969-76eab9419137
keywords: accessibilité, accessibilité pour les développeurs, sites web accessibles, edge, développement web, ARIA, développeur, UIA, UI Automation
ms.openlocfilehash: 8d31f7b32cb92794ff8592c239436f3b101a3859
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230816"
---
# <span data-ttu-id="5a470-104">Conception de sites web accessibles</span><span class="sxs-lookup"><span data-stu-id="5a470-104">Designing Accessible Websites</span></span>  

<span data-ttu-id="5a470-105">La création d’une conception inclusive rend la technologie utilisable par tous les individus, quel que soit leur âge, leur éducation, leur emplacement géographique, leur langue ou leur handicap.</span><span class="sxs-lookup"><span data-stu-id="5a470-105">Creating an inclusive design makes technology usable by all people no matter their age, education, geographic location, language, or disability.</span></span>  <span data-ttu-id="5a470-106">Les utilisateurs de la technologie et de la navigation sur le web ont un large éventail de capacités et de préférences.</span><span class="sxs-lookup"><span data-stu-id="5a470-106">People using technology and browsing the web have a wide range of abilities and preferences.</span></span>  <span data-ttu-id="5a470-107">Lorsque vous concevez votre site web, gardez à l’esprit les scénarios d’accessibilité clés suivants :</span><span class="sxs-lookup"><span data-stu-id="5a470-107">As you design your website, keep in mind the following key accessibility scenarios:</span></span>

*   <span data-ttu-id="5a470-108">Lecteurs d’écran : les utilisateurs non voyants ou malvoyants s’appuient sur les lecteurs d’écran pour interpréter et interagir avec l’interface utilisateur de votre application.</span><span class="sxs-lookup"><span data-stu-id="5a470-108">Screen readers—Users who are blind or visually impaired rely on screen readers to interpret and interact with the UI of your app.</span></span>  <span data-ttu-id="5a470-109">L’interprétation implique la lecture des noms d’éléments d’interface utilisateur, des rôles, des valeurs, etc., et l’interaction avec l’interface utilisateur implique le déplacement du focus d’un élément vers un autre et l’appel de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="5a470-109">Interpreting involves reading the UI element names, roles, values, and so on, and interacting with the UI involves moving the focus from one element to another and invoking functionality.</span></span>
*   <span data-ttu-id="5a470-110">Accessibilité du clavier : de nombreux utilisateurs d’accessibilité s’appuient sur le clavier pour naviguer et utiliser l’interface utilisateur en :</span><span class="sxs-lookup"><span data-stu-id="5a470-110">Keyboard accessibility—Many accessibility users rely on the keyboard to navigate and operate the UI by:</span></span>
    *   <span data-ttu-id="5a470-111">Déplacement du focus entre les éléments à l’aide de la touche tabulation.</span><span class="sxs-lookup"><span data-stu-id="5a470-111">Moving focus among elements by using the Tab key.</span></span>
    *   <span data-ttu-id="5a470-112">Navigation dans des éléments de conteneur tels que des listes, des grilles et des arborescences à l’aide des touches de direction.</span><span class="sxs-lookup"><span data-stu-id="5a470-112">Navigating in container elements such as lists, grids, and tree views by using the arrow keys.</span></span>
    *   <span data-ttu-id="5a470-113">Activation de la fonctionnalité \(appel d’actions\) à l’aide de la touche Entrée ou Espace.</span><span class="sxs-lookup"><span data-stu-id="5a470-113">Activating functionality \(invoking actions\) by using the Enter or Space key.</span></span>
    *   <span data-ttu-id="5a470-114">Utilisation des touches de raccourci pour accéder efficacement aux autres fonctionnalités de l’application.</span><span class="sxs-lookup"><span data-stu-id="5a470-114">Using shortcut keys to efficiently access other app functionality.</span></span>
*   <span data-ttu-id="5a470-115">Expérience visuelle accessible : les utilisateurs malvoyants ont besoin d’un coefficient de contraste de texte suffisant pour le contenu du texte et d’une bonne expérience visuelle avec des thèmes à contraste élevé dans l’ensemble.</span><span class="sxs-lookup"><span data-stu-id="5a470-115">Accessible visual experience—Users who are visually impaired need a sufficient text contrast ratio for text content, and a good visual experience with high contrast themes overall.</span></span>  <span data-ttu-id="5a470-116">Les utilisateurs qui sont daltonien ont besoin que les informations soient transmises d’autres manières que par le biais de la couleur.</span><span class="sxs-lookup"><span data-stu-id="5a470-116">Users who are color blind need information to be conveyed in ways other than through color.</span></span>

<span data-ttu-id="5a470-117">De nombreux problèmes d’accessibilité courants sur le web peuvent être résolus par le biais d’une bonne pratique de codage.</span><span class="sxs-lookup"><span data-stu-id="5a470-117">Many common accessibility issues on the web can be solved through good coding practice.</span></span>  <span data-ttu-id="5a470-118">La documentation [WCAG 2.0 (Web Content Accessibility Guidelines) 2.0](https://www.w3.org/TR/WCAG20) fournit des techniques et des meilleures pratiques pour vous aider à concevoir des applications web dynamiques plus accessibles.</span><span class="sxs-lookup"><span data-stu-id="5a470-118">The [Web Content Accessibility Guidelines (WCAG) 2.0](https://www.w3.org/TR/WCAG20) documentation provides techniques and best practices to help you design more accessible dynamic web applications.</span></span>  <span data-ttu-id="5a470-119">Pour plus d’informations sur la création de sites web accessibles, [accédez à La création de sites web accessibles.](./build/index.md)</span><span class="sxs-lookup"><span data-stu-id="5a470-119">For more information on building accessible websites, navigate to [Building Accessible Websites](./build/index.md) .</span></span>

## <span data-ttu-id="5a470-120">Ressources</span><span class="sxs-lookup"><span data-stu-id="5a470-120">Resources</span></span>  

#### [<span data-ttu-id="5a470-121">Conception de l’inclusion</span><span class="sxs-lookup"><span data-stu-id="5a470-121">Designing for Inclusion</span></span>](https://w3.org/WAI/users/Overview.html)  

<span data-ttu-id="5a470-122">La conception de l’inclusion par l’Initiative d’accessibilité web W3C fournit des ressources pour vous aider à mieux comprendre les utilisateurs souffrant de handicaps et à concevoir votre site web en les ayant à l’esprit.</span><span class="sxs-lookup"><span data-stu-id="5a470-122">Designing for Inclusion by the W3C Web Accessibility Initiative provides resources to help you better understand users with disabilities and how to design your website with them in mind.</span></span>

#### [<span data-ttu-id="5a470-123">Conception de logiciels inclusifs</span><span class="sxs-lookup"><span data-stu-id="5a470-123">Designing inclusive software</span></span>](https://msdn.microsoft.com/windows/uwp/accessibility/designing-inclusive-software)  

<span data-ttu-id="5a470-124">La conception de logiciels inclusifs présente les principes et pratiques de conception de Microsoft pour la plateforme Windows universelle (UWP).</span><span class="sxs-lookup"><span data-stu-id="5a470-124">Designing inclusive software discusses Microsoft design principles and practices for the Universal Windows Platform (UWP).</span></span>

#### [<span data-ttu-id="5a470-125">Utilisation du web par les personnes présentant un handicap</span><span class="sxs-lookup"><span data-stu-id="5a470-125">How People with Disabilities Use the Web</span></span>](https://www.w3.org/WAI/intro/people-use-web/Overview.html)  

<span data-ttu-id="5a470-126">Cette ressource W3C présente comment les personnes présentant un handicap, y compris les personnes souffrant de troubles liés à l’âge, utilisent le Web.</span><span class="sxs-lookup"><span data-stu-id="5a470-126">This resource by the W3C introduces how people with disabilities, including people with age-related impairments, use the Web.</span></span>

#### [<span data-ttu-id="5a470-127">Conception inclusive Shared Computer Toolkit</span><span class="sxs-lookup"><span data-stu-id="5a470-127">Inclusive Design Toolkit</span></span>](https://www.microsoft.com/design/practice#howwemake-section)  

<span data-ttu-id="5a470-128">Microsoft a développé l’Shared Computer Toolkit conception inclusive pour montrer comment la diversité humaine peut créer de meilleures contraintes de conception et comment connecter des solutions semble-t-il à des marchés plus larges.</span><span class="sxs-lookup"><span data-stu-id="5a470-128">Microsoft developed the Inclusive Design Toolkit to show how human diversity can create better design constraints and how to connect seemingly niche solutions to broader markets.</span></span>
