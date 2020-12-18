---
description: Découvrez comment créer, concevoir et tester des sites Web accessibles dans Microsoft Edge.
title: Accessibilité
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 1e5c42a7-4604-46ac-ad7b-a65390e5b36a
keywords: accessibilité, accessibilité pour les développeurs, sites Web accessibles, Edge, développement Web, ARIA, développeur, UIA, UI Automation
ms.openlocfilehash: ae2b0a876b60e0475e283cc52ffd14275fc32aba
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232950"
---
# <span data-ttu-id="1c8e7-104">Vue d’ensemble de l’accessibilité</span><span class="sxs-lookup"><span data-stu-id="1c8e7-104">Accessibility overview</span></span>  

> <span data-ttu-id="1c8e7-105">«\ [T \] il est radicalement modifié sur le Web, car le Web supprime les obstacles aux communications et aux interactions qu’il rencontre dans le monde physique.»</span><span class="sxs-lookup"><span data-stu-id="1c8e7-105">"\[T\]he impact of disability is radically changed on the Web because the Web removes barriers to communication and interaction that many people face in the physical world."</span></span> [<span data-ttu-id="1c8e7-106">(Accessibilité | W3C</span><span class="sxs-lookup"><span data-stu-id="1c8e7-106">(Accessibility | W3C)</span></span>][W3CAccessibility]  

<span data-ttu-id="1c8e7-107">L' [Organisation mondiale][WHODisabilities] de l’état de santé définit le handicap comme «une incompatibilité entre les fonctionnalités du corps d’une personne et les fonctionnalités de l’environnement dans lequel elle réside».</span><span class="sxs-lookup"><span data-stu-id="1c8e7-107">The [World Health Organization][WHODisabilities] defines disability as "a mismatch in interaction between the features of a person's body and the features of the environment in which they live".</span></span>  <span data-ttu-id="1c8e7-108">Une gamme de handicaps, par exemple une mobilité réduite tout en préservant un bébé ou un éclairage brillant sur un téléphone, à d’autres handicaps physiques, auditifs, visuels ou âges.</span><span class="sxs-lookup"><span data-stu-id="1c8e7-108">Disabilities range from situational disabilities, like limited mobility while holding a baby or bright sunlight on a phone, to other physical, auditory, visual, or age-related impairments.</span></span>  

<span data-ttu-id="1c8e7-109">La conception de sites Web et d’autres technologies pour l’inclusion crée une interface agréable pour chaque personne.</span><span class="sxs-lookup"><span data-stu-id="1c8e7-109">Designing websites and other technologies for inclusion creates an experience enjoyable by every person.</span></span>  <span data-ttu-id="1c8e7-110">La conception inclusive et l’accessibilité Web permettent à tout le monde d’utiliser le Web.</span><span class="sxs-lookup"><span data-stu-id="1c8e7-110">Inclusive design and web accessibility empowers and assists everyone to use the web.</span></span>  

<span data-ttu-id="1c8e7-111">Voici quelques pratiques recommandées, des exemples de code et des ressources supplémentaires pour vous aider à en savoir plus sur la [création][AccessibilityDesign], la [création][AccessibilityBuild]et le [test][AccessibilityTest] de sites Web accessibles dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1c8e7-111">Here are some best practices, code samples, and further resources for you to learn more about [Designing][AccessibilityDesign], [Building][AccessibilityBuild], and [Testing][AccessibilityTest] accessible websites in Microsoft Edge.</span></span>  

## <span data-ttu-id="1c8e7-112">Accessibilité dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1c8e7-112">Accessibility in Microsoft Edge</span></span>  

<span data-ttu-id="1c8e7-113">Dans Microsoft Edge, nous avons introduit l’API du complément [Automation de l’API][WindowsWin32AutoEntryui] .</span><span class="sxs-lookup"><span data-stu-id="1c8e7-113">In Microsoft Edge, we introduced modern [UI Automation API][WindowsWin32AutoEntryui] \(UIA API\).</span></span>  <span data-ttu-id="1c8e7-114">La modification apportée à UIA fut un investissement important dans l’accessibilité du navigateur et repose sur une interface Web plus inclusive pour les utilisateurs qui utilisent la technologie d’assistance dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1c8e7-114">The change to UIA was a major investment in browser accessibility, and it lays the foundation for a more inclusive web experience for users who depend on assistive technology in Windows 10.</span></span>  <span data-ttu-id="1c8e7-115">Les utilisateurs bénéficient également du caractère persistant du moteur de chrome.</span><span class="sxs-lookup"><span data-stu-id="1c8e7-115">Users also benefit from the evergreen nature of the Chromium engine.</span></span>  

<span data-ttu-id="1c8e7-116">Le système d’accessibilité dans Microsoft Edge prend fondamentalement en charge les normes Web modernes, notamment ARIA, HTML5 et CSS3.</span><span class="sxs-lookup"><span data-stu-id="1c8e7-116">The accessibility system in Microsoft Edge inherently supports modern web standards including ARIA, HTML5, and CSS3.</span></span>  <span data-ttu-id="1c8e7-117">Le diagramme suivant du pipeline de navigateur simplifié suit le contenu d’une page Web dans une couche de présentation accessible.</span><span class="sxs-lookup"><span data-stu-id="1c8e7-117">The following diagram of the simplified browser pipeline follows webpage content into an accessible presentation layer.</span></span>  

:::image type="complex" source="./media/accessibilityarchitecture.png" alt-text="Le contenu converti au modèle du moteur est projeté dans les affichages visuels et d’accessibilité présentés sous forme d’éléments visuels ou accessibles":::
   <span data-ttu-id="1c8e7-119">Le contenu converti au modèle du moteur est projeté dans les affichages visuels et d’accessibilité présentés sous forme d’éléments visuels ou accessibles</span><span class="sxs-lookup"><span data-stu-id="1c8e7-119">Content transformed to the engine model is projected into visual and accessibility views that are presented either as visual or accessible presentation</span></span>  
:::image-end:::  

<span data-ttu-id="1c8e7-120">L’équipe Microsoft Edge travaille en collaboration avec le W3C et d’autres fournisseurs de navigateur de façon continue pour garantir que les nouvelles fonctionnalités de plateforme Web disposent d’une accessibilité intégrée.</span><span class="sxs-lookup"><span data-stu-id="1c8e7-120">The Microsoft Edge team works with the W3C and other browser vendors on an ongoing basis to ensure that new web platform features have sufficient built-in accessibility.</span></span>  

<span data-ttu-id="1c8e7-121">Pour plus d’informations sur les nouvelles fonctionnalités HTML5 prises en charge par Microsoft Edge accessibly, accédez à [HTML5Accessibility][HTML5Accessibility].</span><span class="sxs-lookup"><span data-stu-id="1c8e7-121">For information on which new HTML5 features are accessibly supported by Microsoft Edge, navigate to [HTML5Accessibility][HTML5Accessibility].</span></span>  

## <span data-ttu-id="1c8e7-122">Ressources</span><span class="sxs-lookup"><span data-stu-id="1c8e7-122">Resources</span></span>  

#### <span data-ttu-id="1c8e7-123">Blog Microsoft Windows UI Automation</span><span class="sxs-lookup"><span data-stu-id="1c8e7-123">Microsoft Windows UI Automation Blog</span></span>  

<span data-ttu-id="1c8e7-124">Le [blog Microsoft Windows UI Automation][ArchiveBlogsWinuiautomation] comprend des rubriques relatives à l’API Windows Automation.</span><span class="sxs-lookup"><span data-stu-id="1c8e7-124">The [Microsoft Windows UI Automation blog][ArchiveBlogsWinuiautomation] covers topics related to the Windows Automation API.</span></span>  

#### <span data-ttu-id="1c8e7-125">Initiative Web Accessibility (WAI)</span><span class="sxs-lookup"><span data-stu-id="1c8e7-125">Web Accessibility Initiative (WAI)</span></span>  

<span data-ttu-id="1c8e7-126">L' [initiative Web Accessibility (WAI)][W3CWaiHome] fournie par le W3C est un effort pour améliorer l’accessibilité du Web.</span><span class="sxs-lookup"><span data-stu-id="1c8e7-126">The [Web Accessibility Initiative (WAI)][W3CWaiHome] provided bt the W3C is an effort to help improve the accessibility of the web.</span></span>  <span data-ttu-id="1c8e7-127">Ce site fournit diverses ressources pour la [prise en main de l’accessibilité sur le Web][W3CWaiGettingstartedOverview], la [conception d’une inclusion, des][W3CWaiFundamentals] [didacticiels et des présentations][W3CWaiTeachAdvocate], etc.</span><span class="sxs-lookup"><span data-stu-id="1c8e7-127">The site provides a variety of resources for [Getting Started with Web Accessibility][W3CWaiGettingstartedOverview], [Designing for Inclusion][W3CWaiFundamentals], [tutorials and presentations][W3CWaiTeachAdvocate], and more.</span></span>  

<!-- links -->  

[AccessibilityBuild]: ./build/index.md "Créer des sites Web accessibles | Document Microsoft"  
[AccessibilityDesign]: ./design.md "Conception de sites Web accessibles | Document Microsoft"  
[AccessibilityTest]: ./test.md "Test de l’accessibilité | Documents Microsoft"  

[WindowsWin32AutoEntryui]: /windows/win32/winauto/entry-uiauto-win32 "UI Automation | Document Microsoft"  

[ArchiveBlogsWinuiautomation]: /archive/blogs/winuiautomation/ "Blog Microsoft Windows UI Automation | Document Microsoft"  

[HTML5Accessibility]: https://html5accessibility.com "Accessibilité HTML5"  

[W3CAccessibility]: https://w3.org/standards/webdesign/accessibility "Accessibilité | W3C"  
[W3CWaiFundamentals]: https://w3.org/wai/fundamentals/accessibility-intro "Présentation de l’accessibilité sur le Web | Initiative Web Accessibility (WAI) | W3C"  
[W3CWaiGettingstartedOverview]: https://w3.org/wai/gettingstarted/Overview "Mise en route: rendre un site Web accessible | Initiative Web Accessibility (WAI) | W3C"  
[W3CWaiHome]: https://w3.org/wai "Initiative Web Accessibility (WAI) | W3C"  
[W3CWaiTeachAdvocate]: https://w3.org/wai/teach-advocate "Présentation de l’enseignement et du défenseur | Initiative Web Accessibility (WAI) | W3C"  

[WHODisabilities]: https://who.int/topics/disabilities "Incapacité | EMPLOYÉ"  

