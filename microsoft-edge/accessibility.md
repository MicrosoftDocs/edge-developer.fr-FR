---
ms.assetid: 1e5c42a7-4604-46ac-ad7b-a65390e5b36a
description: Découvrez comment créer, concevoir et tester des sites Web accessibles dans Microsoft Edge.
title: Accessibilité
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: accessibilité, accessibilité pour les développeurs, sites Web accessibles, Edge, développement Web, ARIA, développeur, UIA, UI Automation
ms.openlocfilehash: 6ad95e9c250aa6a4a61ca09470cea86efd715427
ms.sourcegitcommit: 9169d784485e3cb0b1987a8f395c4bb688bd9b2e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "10583104"
---
# <span data-ttu-id="5d453-104">Accessibilité</span><span class="sxs-lookup"><span data-stu-id="5d453-104">Accessibility</span></span>  

> <span data-ttu-id="5d453-105">«\ [T \] il est radicalement modifié sur le Web, car le Web supprime les obstacles aux communications et aux interactions qu’il rencontre dans le monde physique.»</span><span class="sxs-lookup"><span data-stu-id="5d453-105">"\[T\]he impact of disability is radically changed on the Web because the Web removes barriers to communication and interaction that many people face in the physical world."</span></span> [<span data-ttu-id="5d453-106">(Accessibilité | W3C</span><span class="sxs-lookup"><span data-stu-id="5d453-106">(Accessibility | W3C)</span></span>][W3CAccessibility]  

<span data-ttu-id="5d453-107">L' [Organisation mondiale][WHODisabilities] de l’état de santé définit le handicap comme «une incompatibilité entre les fonctionnalités du corps d’une personne et les fonctionnalités de l’environnement dans lequel elle réside».</span><span class="sxs-lookup"><span data-stu-id="5d453-107">The [World Health Organization][WHODisabilities] defines disability as "a mismatch in interaction between the features of a person's body and the features of the environment in which they live".</span></span>  <span data-ttu-id="5d453-108">Une gamme de handicaps, par exemple une mobilité réduite tout en préservant un bébé ou un éclairage brillant sur un téléphone, à d’autres handicaps physiques, auditifs, visuels ou âges.</span><span class="sxs-lookup"><span data-stu-id="5d453-108">Disabilities range from situational disabilities, like limited mobility while holding a baby or bright sunlight on a phone, to other physical, auditory, visual, or age-related impairments.</span></span>  

<span data-ttu-id="5d453-109">La conception de sites Web et d’autres technologies pour l’inclusion crée une interface agréable pour chaque personne.</span><span class="sxs-lookup"><span data-stu-id="5d453-109">Designing websites and other technologies for inclusion creates an experience enjoyable by every person.</span></span>  <span data-ttu-id="5d453-110">La conception inclusive et l’accessibilité Web permettent à tout le monde d’utiliser le Web.</span><span class="sxs-lookup"><span data-stu-id="5d453-110">Inclusive design and web accessibility empowers and assists everyone to use the web.</span></span>  

<span data-ttu-id="5d453-111">Voici quelques pratiques recommandées, des exemples de code et des ressources supplémentaires pour vous aider à en savoir plus sur la [création][AccessibilityDesign], la [création][AccessibilityBuild]et le [test][AccessibilityTest] de sites Web accessibles dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5d453-111">Here are some best practices, code samples, and further resources for you to learn more about [Designing][AccessibilityDesign], [Building][AccessibilityBuild], and [Testing][AccessibilityTest] accessible websites in Microsoft Edge.</span></span>  

## <span data-ttu-id="5d453-112">Accessibilité dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5d453-112">Accessibility in Microsoft Edge</span></span>  

<span data-ttu-id="5d453-113">Dans Microsoft Edge, nous avons introduit l’API du complément [Automation de l’API][WindowsWin32AutoEntryui] .</span><span class="sxs-lookup"><span data-stu-id="5d453-113">In Microsoft Edge, we introduced modern [UI Automation API][WindowsWin32AutoEntryui] \(UIA API\).</span></span>  <span data-ttu-id="5d453-114">La modification apportée à UIA fut un investissement important dans l’accessibilité du navigateur et repose sur une interface Web plus inclusive pour les utilisateurs qui utilisent la technologie d’assistance dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5d453-114">The change to UIA was a major investment in browser accessibility, and it lays the foundation for a more inclusive web experience for users who depend on assistive technology in Windows 10.</span></span>  <span data-ttu-id="5d453-115">Les utilisateurs bénéficient également du caractère persistant du moteur de chrome.</span><span class="sxs-lookup"><span data-stu-id="5d453-115">Users also benefit from the evergreen nature of the Chromium engine.</span></span>  

<span data-ttu-id="5d453-116">Le système d’accessibilité dans Microsoft Edge prend fondamentalement en charge les normes Web modernes, notamment ARIA, HTML5 et CSS3.</span><span class="sxs-lookup"><span data-stu-id="5d453-116">The accessibility system in Microsoft Edge inherently supports modern web standards including ARIA, HTML5, and CSS3.</span></span>  <span data-ttu-id="5d453-117">Le diagramme suivant du pipeline de navigateur simplifié suit le contenu d’une page Web dans une couche de présentation accessible.</span><span class="sxs-lookup"><span data-stu-id="5d453-117">The following diagram of the simplified browser pipeline follows webpage content into an accessible presentation layer.</span></span>  

:::image type="complex" source="./media/accessibilityarchitecture.png" alt-text="Le contenu converti au modèle du moteur est projeté dans les affichages visuels et d’accessibilité présentés sous forme d’éléments visuels ou accessibles":::
   <span data-ttu-id="5d453-119">Figure1.</span><span class="sxs-lookup"><span data-stu-id="5d453-119">Figure 1.</span></span>  <span data-ttu-id="5d453-120">Le contenu converti au modèle du moteur est projeté dans les affichages visuels et d’accessibilité présentés sous forme d’éléments visuels ou accessibles</span><span class="sxs-lookup"><span data-stu-id="5d453-120">Content transformed to the engine model is projected into visual and accessibility views that are presented either as visual or accessible presentation</span></span>
:::image-end:::

<!--![Figure 1.  Content transformed to the engine model is projected into visual and accessibility views that are presented either as visual or accessible presentation][ImageAccessibilityArchitecture]  -->  

<span data-ttu-id="5d453-121">L’équipe Microsoft Edge travaille en collaboration avec le W3C et d’autres fournisseurs de navigateur de façon continue pour garantir que les nouvelles fonctionnalités de plateforme Web disposent d’une accessibilité intégrée.</span><span class="sxs-lookup"><span data-stu-id="5d453-121">The Microsoft Edge team works with the W3C and other browser vendors on an ongoing basis to ensure that new web platform features have sufficient built-in accessibility.</span></span>  

<span data-ttu-id="5d453-122">Pour plus d’informations sur les nouvelles fonctionnalités de HTML5 accessibly prises en charge par Microsoft Edge, consultez la page [HTML5Accessibility][HTML5Accessibility].</span><span class="sxs-lookup"><span data-stu-id="5d453-122">For information on which new HTML5 features are accessibly supported by Microsoft Edge, visit [HTML5Accessibility][HTML5Accessibility].</span></span>  

## <span data-ttu-id="5d453-123">Ressources</span><span class="sxs-lookup"><span data-stu-id="5d453-123">Resources</span></span>  

#### <span data-ttu-id="5d453-124">Blog Microsoft Windows UI Automation</span><span class="sxs-lookup"><span data-stu-id="5d453-124">Microsoft Windows UI Automation Blog</span></span>  

<span data-ttu-id="5d453-125">Le [blog Microsoft Windows UI Automation][ArchiveBlogsWinuiautomation] comprend des rubriques relatives à l’API Windows Automation.</span><span class="sxs-lookup"><span data-stu-id="5d453-125">The [Microsoft Windows UI Automation blog][ArchiveBlogsWinuiautomation] covers topics related to the Windows Automation API.</span></span>  

#### <span data-ttu-id="5d453-126">Initiative Web Accessibility (WAI)</span><span class="sxs-lookup"><span data-stu-id="5d453-126">Web Accessibility Initiative (WAI)</span></span>  

<span data-ttu-id="5d453-127">L' [initiative Web Accessibility (WAI)][W3CWaiHome] fournie par le W3C est un effort pour améliorer l’accessibilité du Web.</span><span class="sxs-lookup"><span data-stu-id="5d453-127">The [Web Accessibility Initiative (WAI)][W3CWaiHome] provided bt the W3C is an effort to help improve the accessibility of the web.</span></span>  <span data-ttu-id="5d453-128">Ce site fournit diverses ressources pour la [prise en main de l’accessibilité sur le Web][W3CWaiGettingstartedOverview], la [conception d’une inclusion, des][W3CWaiFundamentals] [didacticiels et des présentations][W3CWaiTeachAdvocate], etc.</span><span class="sxs-lookup"><span data-stu-id="5d453-128">The site provides a variety of resources for [Getting Started with Web Accessibility][W3CWaiGettingstartedOverview], [Designing for Inclusion][W3CWaiFundamentals], [tutorials and presentations][W3CWaiTeachAdvocate], and more.</span></span>  


<!-- image links -->  

<!--[ImageAccessibilityArchitecture]: ./media/accessibilityarchitecture.png "Figure 1: Content transformed to the engine model is projected into visual and accessibility views that are presented either as visual or accessible presentation"  -->  

<!-- links -->  

[AccessibilityBuild]: ./accessibility/build.md "Créer des sites Web accessibles"  
[AccessibilityDesign]: ./accessibility/design.md "Conception de sites Web accessibles"  
[AccessibilityTest]: ./accessibility/test.md "Test de l’accessibilité"  

[WindowsWin32AutoEntryui]: /windows/win32/winauto/entry-uiauto-win32 "Automatisation de l’interface utilisateur"  

[ArchiveBlogsWinuiautomation]: /archive/blogs/winuiautomation/ "Blog Microsoft Windows UI Automation"  

[HTML5Accessibility]: https://html5accessibility.com "Accessibilité HTML5"  

[W3CAccessibility]: https://w3.org/standards/webdesign/accessibility "Accessibilité | W3C"  
[W3CWaiFundamentals]: https://w3.org/wai/fundamentals/accessibility-intro "Présentation de l’accessibilité sur le Web | Initiative Web Accessibility (WAI) | W3C"  
[W3CWaiGettingstartedOverview]: https://w3.org/wai/gettingstarted/Overview "Mise en route: rendre un site Web accessible | Initiative Web Accessibility (WAI) | W3C"  
[W3CWaiHome]: https://w3.org/wai "Initiative Web Accessibility (WAI) | W3C"  
[W3CWaiTeachAdvocate]: https://w3.org/wai/teach-advocate "Présentation de l’enseignement et du défenseur | Initiative Web Accessibility (WAI) | W3C"  

[WHODisabilities]: https://who.int/topics/disabilities "Incapacité | EMPLOYÉ"  

