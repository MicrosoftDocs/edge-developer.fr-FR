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
# Vue d’ensemble de l’accessibilité  

> «\ [T \] il est radicalement modifié sur le Web, car le Web supprime les obstacles aux communications et aux interactions qu’il rencontre dans le monde physique.» [(Accessibilité | W3C][W3CAccessibility]  

L' [Organisation mondiale][WHODisabilities] de l’état de santé définit le handicap comme «une incompatibilité entre les fonctionnalités du corps d’une personne et les fonctionnalités de l’environnement dans lequel elle réside».  Une gamme de handicaps, par exemple une mobilité réduite tout en préservant un bébé ou un éclairage brillant sur un téléphone, à d’autres handicaps physiques, auditifs, visuels ou âges.  

La conception de sites Web et d’autres technologies pour l’inclusion crée une interface agréable pour chaque personne.  La conception inclusive et l’accessibilité Web permettent à tout le monde d’utiliser le Web.  

Voici quelques pratiques recommandées, des exemples de code et des ressources supplémentaires pour vous aider à en savoir plus sur la [création][AccessibilityDesign], la [création][AccessibilityBuild]et le [test][AccessibilityTest] de sites Web accessibles dans Microsoft Edge.  

## Accessibilité dans Microsoft Edge  

Dans Microsoft Edge, nous avons introduit l’API du complément [Automation de l’API][WindowsWin32AutoEntryui] .  La modification apportée à UIA fut un investissement important dans l’accessibilité du navigateur et repose sur une interface Web plus inclusive pour les utilisateurs qui utilisent la technologie d’assistance dans Windows 10.  Les utilisateurs bénéficient également du caractère persistant du moteur de chrome.  

Le système d’accessibilité dans Microsoft Edge prend fondamentalement en charge les normes Web modernes, notamment ARIA, HTML5 et CSS3.  Le diagramme suivant du pipeline de navigateur simplifié suit le contenu d’une page Web dans une couche de présentation accessible.  

:::image type="complex" source="./media/accessibilityarchitecture.png" alt-text="Le contenu converti au modèle du moteur est projeté dans les affichages visuels et d’accessibilité présentés sous forme d’éléments visuels ou accessibles":::
   Le contenu converti au modèle du moteur est projeté dans les affichages visuels et d’accessibilité présentés sous forme d’éléments visuels ou accessibles  
:::image-end:::  

L’équipe Microsoft Edge travaille en collaboration avec le W3C et d’autres fournisseurs de navigateur de façon continue pour garantir que les nouvelles fonctionnalités de plateforme Web disposent d’une accessibilité intégrée.  

Pour plus d’informations sur les nouvelles fonctionnalités HTML5 prises en charge par Microsoft Edge accessibly, accédez à [HTML5Accessibility][HTML5Accessibility].  

## Ressources  

#### Blog Microsoft Windows UI Automation  

Le [blog Microsoft Windows UI Automation][ArchiveBlogsWinuiautomation] comprend des rubriques relatives à l’API Windows Automation.  

#### Initiative Web Accessibility (WAI)  

L' [initiative Web Accessibility (WAI)][W3CWaiHome] fournie par le W3C est un effort pour améliorer l’accessibilité du Web.  Ce site fournit diverses ressources pour la [prise en main de l’accessibilité sur le Web][W3CWaiGettingstartedOverview], la [conception d’une inclusion, des][W3CWaiFundamentals] [didacticiels et des présentations][W3CWaiTeachAdvocate], etc.  

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

