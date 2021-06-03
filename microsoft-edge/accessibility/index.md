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
# Vue d’ensemble de l’accessibilité  

> « L’impact du handicap sur le web est radicalement modifié sur le Web, car le Web supprime les obstacles à la communication et à l’interaction auxquels de nombreuses personnes font face dans le monde physique. » [(Accessibilité | W3C)][W3CAccessibility]  

[L’Organisation mondiale de][WHODisabilities] la santé définit le handicap/invalidité comme une « insématisation de l’interaction entre les fonctionnalités du corps d’une personne et les fonctionnalités de l’environnement dans lequel elle habite ».  Les handicaps peuvent aller des handicaps situationnels, tels que la mobilité limitée tout en maintenant un air ou une lumière vive sur un téléphone, à d’autres handicaps physiques, auditeurs, visuels ou liés à l’âge.  

La conception de sites web et d’autres technologies pour l’inclusion crée une expérience agréable pour chaque personne.  La conception inclusive et l’accessibilité web permettent à tout le monde d’utiliser le web.  

Voici quelques meilleures pratiques, des exemples de code et d’autres ressources pour en savoir plus sur la [conception,][AccessibilityDesign]la création et le test de sites web [accessibles][AccessibilityTest] dans Microsoft Edge. [][AccessibilityBuild]  

## Accessibilité dans les Microsoft Edge  

Dans Microsoft Edge, nous avons introduit [l’API UI Automation][WindowsWin32AutoEntryui] moderne \(API UIA\).  La modification de l’UIA a été un investissement majeur dans l’accessibilité des navigateurs et elle a été la base d’une expérience web plus inclusive pour les utilisateurs qui dépendent de la technologie d’assistance dans Windows 10.  Les utilisateurs bénéficient également de la nature persistante du moteur Chromium de recherche.  

Le système d’accessibilité Microsoft Edge prend en charge les normes web modernes, notamment ARIA, HTML5 et CSS3.  Le diagramme suivant du pipeline de navigateur simplifié suit le contenu de la page web dans une couche de présentation accessible.  

:::image type="complex" source="./media/accessibilityarchitecture.png" alt-text="Le contenu transformé en modèle de moteur est projeté dans des affichages visuels et d’accessibilité présentés en tant que présentation visuelle ou accessible":::
   Le contenu transformé en modèle de moteur est projeté dans des affichages visuels et d’accessibilité présentés en tant que présentation visuelle ou accessible  
:::image-end:::  

L Microsoft Edge de recherche collabore régulièrement avec le W3C et d’autres fournisseurs de navigateurs pour s’assurer que les nouvelles fonctionnalités de plateforme web ont une accessibilité intégrée suffisante.  

Pour plus d’informations sur les nouvelles fonctionnalités HTML5 qui sont accessibles Microsoft Edge, accédez à [HTML5Accessibility][HTML5Accessibility].  

## Ressources  

#### Blog Microsoft Windows UI Automation  

Le [blog Microsoft Windows UI Automation couvre][ArchiveBlogsWinuiautomation] des rubriques relatives à l’API Windows Automation.  

#### Initiative d’accessibilité web (CAS)  

[L’initiative d’accessibilité web (INSO)][W3CWaiHome] fournie par le W3C vise à améliorer l’accessibilité du site web.  Le site fournit une variété de ressources pour la mise en place de l’accessibilité [web,][W3CWaiGettingstartedOverview]la conception pour [l’inclusion,][W3CWaiFundamentals]les [didacticiels et les présentations,][W3CWaiTeachAdvocate]et bien plus encore.  

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

