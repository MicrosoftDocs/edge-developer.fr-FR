---
description: Découvrez comment créer, concevoir et tester des sites web accessibles dans Microsoft Edge.
title: Accessibilité
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 1e5c42a7-4604-46ac-ad7b-a65390e5b36a
keywords: accessibilité, accessibilité pour les développeurs, sites web accessibles, edge, développement web, ARIA, développeur, UIA, UI Automation
ms.openlocfilehash: ae2b0a876b60e0475e283cc52ffd14275fc32aba
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232950"
---
# <span data-ttu-id="5922f-104">Vue d’ensemble de l’accessibilité</span><span class="sxs-lookup"><span data-stu-id="5922f-104">Accessibility overview</span></span>  

> <span data-ttu-id="5922f-105">« L’impact du handicap sur le web est radicalement modifié sur le Web, car le Web supprime les obstacles à la communication et à l’interaction auxquels de nombreuses personnes font face dans le monde physique. »</span><span class="sxs-lookup"><span data-stu-id="5922f-105">"\[T\]he impact of disability is radically changed on the Web because the Web removes barriers to communication and interaction that many people face in the physical world."</span></span> [<span data-ttu-id="5922f-106">(Accessibilité | W3C)</span><span class="sxs-lookup"><span data-stu-id="5922f-106">(Accessibility | W3C)</span></span>][W3CAccessibility]  

<span data-ttu-id="5922f-107">[L’Organisation mondiale de][WHODisabilities] la santé définit le handicap/invalidité comme une « insématisation de l’interaction entre les fonctionnalités du corps d’une personne et les fonctionnalités de l’environnement dans lequel elle habite ».</span><span class="sxs-lookup"><span data-stu-id="5922f-107">The [World Health Organization][WHODisabilities] defines disability as "a mismatch in interaction between the features of a person's body and the features of the environment in which they live".</span></span>  <span data-ttu-id="5922f-108">Les handicaps peuvent aller des handicaps situationnels, tels que la mobilité limitée tout en maintenant un air ou une lumière vive sur un téléphone, à d’autres handicaps physiques, auditeurs, visuels ou liés à l’âge.</span><span class="sxs-lookup"><span data-stu-id="5922f-108">Disabilities range from situational disabilities, like limited mobility while holding a baby or bright sunlight on a phone, to other physical, auditory, visual, or age-related impairments.</span></span>  

<span data-ttu-id="5922f-109">La conception de sites web et d’autres technologies pour l’inclusion crée une expérience agréable pour chaque personne.</span><span class="sxs-lookup"><span data-stu-id="5922f-109">Designing websites and other technologies for inclusion creates an experience enjoyable by every person.</span></span>  <span data-ttu-id="5922f-110">La conception inclusive et l’accessibilité web permettent à tout le monde d’utiliser le web.</span><span class="sxs-lookup"><span data-stu-id="5922f-110">Inclusive design and web accessibility empowers and assists everyone to use the web.</span></span>  

<span data-ttu-id="5922f-111">Voici quelques meilleures pratiques, des exemples de code et d’autres ressources pour en savoir plus sur la [conception,][AccessibilityDesign]la création et le test de sites web [accessibles][AccessibilityTest] dans Microsoft Edge. [][AccessibilityBuild]</span><span class="sxs-lookup"><span data-stu-id="5922f-111">Here are some best practices, code samples, and further resources for you to learn more about [Designing][AccessibilityDesign], [Building][AccessibilityBuild], and [Testing][AccessibilityTest] accessible websites in Microsoft Edge.</span></span>  

## <span data-ttu-id="5922f-112">Accessibilité dans les Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5922f-112">Accessibility in Microsoft Edge</span></span>  

<span data-ttu-id="5922f-113">Dans Microsoft Edge, nous avons introduit [l’API UI Automation][WindowsWin32AutoEntryui] moderne \(API UIA\).</span><span class="sxs-lookup"><span data-stu-id="5922f-113">In Microsoft Edge, we introduced modern [UI Automation API][WindowsWin32AutoEntryui] \(UIA API\).</span></span>  <span data-ttu-id="5922f-114">La modification de l’UIA a été un investissement majeur dans l’accessibilité des navigateurs et elle a été la base d’une expérience web plus inclusive pour les utilisateurs qui dépendent de la technologie d’assistance dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5922f-114">The change to UIA was a major investment in browser accessibility, and it lays the foundation for a more inclusive web experience for users who depend on assistive technology in Windows 10.</span></span>  <span data-ttu-id="5922f-115">Les utilisateurs bénéficient également de la nature persistante du moteur Chromium de recherche.</span><span class="sxs-lookup"><span data-stu-id="5922f-115">Users also benefit from the evergreen nature of the Chromium engine.</span></span>  

<span data-ttu-id="5922f-116">Le système d’accessibilité Microsoft Edge prend en charge les normes web modernes, notamment ARIA, HTML5 et CSS3.</span><span class="sxs-lookup"><span data-stu-id="5922f-116">The accessibility system in Microsoft Edge inherently supports modern web standards including ARIA, HTML5, and CSS3.</span></span>  <span data-ttu-id="5922f-117">Le diagramme suivant du pipeline de navigateur simplifié suit le contenu de la page web dans une couche de présentation accessible.</span><span class="sxs-lookup"><span data-stu-id="5922f-117">The following diagram of the simplified browser pipeline follows webpage content into an accessible presentation layer.</span></span>  

:::image type="complex" source="./media/accessibilityarchitecture.png" alt-text="Le contenu transformé en modèle de moteur est projeté dans des affichages visuels et d’accessibilité présentés en tant que présentation visuelle ou accessible":::
   <span data-ttu-id="5922f-119">Le contenu transformé en modèle de moteur est projeté dans des affichages visuels et d’accessibilité présentés en tant que présentation visuelle ou accessible</span><span class="sxs-lookup"><span data-stu-id="5922f-119">Content transformed to the engine model is projected into visual and accessibility views that are presented either as visual or accessible presentation</span></span>  
:::image-end:::  

<span data-ttu-id="5922f-120">L Microsoft Edge de recherche collabore régulièrement avec le W3C et d’autres fournisseurs de navigateurs pour s’assurer que les nouvelles fonctionnalités de plateforme web ont une accessibilité intégrée suffisante.</span><span class="sxs-lookup"><span data-stu-id="5922f-120">The Microsoft Edge team works with the W3C and other browser vendors on an ongoing basis to ensure that new web platform features have sufficient built-in accessibility.</span></span>  

<span data-ttu-id="5922f-121">Pour plus d’informations sur les nouvelles fonctionnalités HTML5 qui sont accessibles Microsoft Edge, accédez à [HTML5Accessibility][HTML5Accessibility].</span><span class="sxs-lookup"><span data-stu-id="5922f-121">For information on which new HTML5 features are accessibly supported by Microsoft Edge, navigate to [HTML5Accessibility][HTML5Accessibility].</span></span>  

## <span data-ttu-id="5922f-122">Ressources</span><span class="sxs-lookup"><span data-stu-id="5922f-122">Resources</span></span>  

#### <span data-ttu-id="5922f-123">Blog Microsoft Windows UI Automation</span><span class="sxs-lookup"><span data-stu-id="5922f-123">Microsoft Windows UI Automation Blog</span></span>  

<span data-ttu-id="5922f-124">Le [blog Microsoft Windows UI Automation couvre][ArchiveBlogsWinuiautomation] des rubriques relatives à l’API Windows Automation.</span><span class="sxs-lookup"><span data-stu-id="5922f-124">The [Microsoft Windows UI Automation blog][ArchiveBlogsWinuiautomation] covers topics related to the Windows Automation API.</span></span>  

#### <span data-ttu-id="5922f-125">Initiative d’accessibilité web (CAS)</span><span class="sxs-lookup"><span data-stu-id="5922f-125">Web Accessibility Initiative (WAI)</span></span>  

<span data-ttu-id="5922f-126">[L’initiative d’accessibilité web (INSO)][W3CWaiHome] fournie par le W3C vise à améliorer l’accessibilité du site web.</span><span class="sxs-lookup"><span data-stu-id="5922f-126">The [Web Accessibility Initiative (WAI)][W3CWaiHome] provided bt the W3C is an effort to help improve the accessibility of the web.</span></span>  <span data-ttu-id="5922f-127">Le site fournit une variété de ressources pour la mise en place de l’accessibilité [web,][W3CWaiGettingstartedOverview]la conception pour [l’inclusion,][W3CWaiFundamentals]les [didacticiels et les présentations,][W3CWaiTeachAdvocate]et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="5922f-127">The site provides a variety of resources for [Getting Started with Web Accessibility][W3CWaiGettingstartedOverview], [Designing for Inclusion][W3CWaiFundamentals], [tutorials and presentations][W3CWaiTeachAdvocate], and more.</span></span>  

<!-- links -->  

[AccessibilityBuild]: ./build/index.md "Création de sites web accessibles | Microsoft Doc"  
[AccessibilityDesign]: ./design.md "Conception de sites web accessibles | Microsoft Doc"  
[AccessibilityTest]: ./test.md "Test d’accessibilité | Documents Microsoft"  

[WindowsWin32AutoEntryui]: /windows/win32/winauto/entry-uiauto-win32 "UI Automation | Microsoft Doc"  

[ArchiveBlogsWinuiautomation]: /archive/blogs/winuiautomation/ "Blog Microsoft Windows UI Automation | Microsoft Doc"  

[HTML5Accessibility]: https://html5accessibility.com "Accessibilité HTML5"  

[W3CAccessibility]: https://w3.org/standards/webdesign/accessibility "Accessibilité | W3C"  
[W3CWaiFundamentals]: https://w3.org/wai/fundamentals/accessibility-intro "Présentation des fonctionnalités d’accessibilité | Web Accessibility Initiative (|) W3C"  
[W3CWaiGettingstartedOverview]: https://w3.org/wai/gettingstarted/Overview "Mise en place : rendre un site Web accessible | Web Accessibility Initiative (|) W3C"  
[W3CWaiHome]: https://w3.org/wai "Web Accessibility Initiative (|) W3C"  
[W3CWaiTeachAdvocate]: https://w3.org/wai/teach-advocate "Présentation de l’enseignement et de la défense | Web Accessibility Initiative (|) W3C"  

[WHODisabilities]: https://who.int/topics/disabilities "Handicaps | WHO"  

