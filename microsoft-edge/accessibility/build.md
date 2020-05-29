---
ms.assetid: 1b3ebc25-d023-4f23-bbba-dce066c20de8
description: Découvrez comment les meilleures pratiques et les applications Internet enrichies accessibles peuvent être utilisées pour créer un site Web accessible.
title: Accessibilité-version
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: accessibilité, accessibilité pour les développeurs, sites Web accessibles, Edge, développement Web, ARIA, développeur, UIA, UI Automation
ms.custom: seodec18
ms.openlocfilehash: 4412fef6bb78b5a393ccafd5a2cfa79aba223141
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10564678"
---
# Créer des sites Web accessibles
Le Web est rempli par des sites Web, des applications et des interfaces utilisateur dynamiques et complexes, développés à l’aide d’une combinaison de HTML, CSS et JavaScript.  Néanmoins, lors d’une conception et d’une conception sans l’accessibilité, ces sites Web complexes sont difficiles à utiliser par les personnes qui utilisent des [technologies d’assistance](https://webaim.org/articles/motor/assistive) pour naviguer sur le Web. La création de sites Web accessibles aux personnes atteintes de handicaps nécessite des informations sémantiques sur l’interface utilisateur. Cela permet aux technologies d’assistance (par exemple, les lecteurs d’écran) de transmettre les informations nécessaires à des personnes atteintes de capacités d’utilisation du site Web.

Consultez [HTML5Accessibility](https://html5accessibility.com) pour en savoir plus sur les nouvelles fonctionnalités HTML5 prises en charge par Microsoft Edge.

## Fonctionnement de l’accessibilité

Les technologies d’assistance permettent d’ajouter des fonctionnalités qui ne sont généralement pas disponibles sur les ordinateurs. Par exemple, un utilisateur souffrant d’une déficience visuelle peut utiliser son clavier en association avec la technologie d’assistance telle qu’un lecteur d’écran, plutôt que d’utiliser directement le navigateur avec la souris et l’écran. Pour les applications sur les plates-formes Microsoft et sur le Web, la technologie d’assistance interagit avec Microsoft [UI Automation](https://msdn.microsoft.com/library/windows/desktop/bb892135.aspx), un modèle d’objet spécifique à l’application tel que le DOM (Document Object Model) dans Microsoft Edge, ou une combinaison de ces éléments.

Pour les développeurs Web, certains éléments HTML sont mappés aux objets UI Automation, de sorte que la sélection de ces éléments HTML par le développeur peut utiliser les propriétés d’accessibilité et les événements intégrés à ces éléments. Lors du développement de votre site Web, il n’est généralement pas nécessaire de veiller à ce que l’API soit correctement écrite (ou que l’élément approprié soit spécifié), afin que l’application soit accessible. Pour plus d’informations, voir [Aria et UI Automation dans Microsoft Edge](./build/ARIA-and-UI-Automation.md) .  Pour plus d’informations sur les applications de plateforme Windows universelle (UWP) accessibles, voir la rubrique [accessibilité](https://msdn.microsoft.com/windows/uwp/accessibility/accessibility) dans le centre de développement Windows.

De nombreux problèmes d’accessibilité courants liés au contenu dynamique peuvent être corrigés par de bonnes pratiques de programmation, et la documentation de [WCAG 2,0](https://go.microsoft.com/fwlink/p/?LinkID=24629) comporte de nombreuses techniques et meilleures pratiques pour vous aider à créer des applications Web dynamiques plus accessibles. Même s’il est correctement codé, le contenu dynamique n’est pas nécessairement accessible. Les [applications Internet enrichies accessibles](#aria) peuvent résoudre ce problème.  

Pour plus d’informations sur l’accessibilité Web, consultez l’article [Présentation de](https://www.w3.org/WAI/intro/accessibility.php) l’accessibilité Web par l' [initiative de Web Accessibility](https://www.w3.org/WAI/) (WAI).

## ENRICHI
La spécification Aria ( [Rich Internet applications) accessible](https://www.w3.org/TR/wai-aria/) par l' [initiative W3C’s Web Accessibility](https://www.w3.org/WAI/) définit en tant que syntaxe pour rendre le contenu Web dynamique et les interfaces utilisateur personnalisés accessibles à tous les utilisateurs. ARIA étend le code HTML à l’aide d’attributs supplémentaires (rôles, propriétés et États) conçus pour transmettre des sémantiques personnalisées. Ces attributs sont utilisés par les navigateurs pour passer de l’État et du rôle de contrôles à l’API d’accessibilité.

### Rôles, propriétés et États
Les rôles ARIA sont définis sur des éléments à l’aide de l' [`role`](https://msdn.microsoft.com/library/cc304102(v=vs.85).aspx) attribut pour fournir des informations sur les technologies d’assistance et sur l’élément. Par exemple, l' `<li>` élément suivant est assigné `role="menuitem"` pour indiquer qu’il s’agit d’un élément d’un menu.

``` html
<li role="menuitem">Home</li>
```

Les États et propriétés ARIA sont des attributs prédéfinis de Aria qui fournissent des informations spécifiques sur un objet pour faciliter la définition de la nature des rôles. Les propriétés sont des attributs essentiels pour la nature d’un objet, par exemple [`aria-readonly`](https://msdn.microsoft.com/library/cc304089(v=vs.85).aspx) et [`aria-haspopup`](https://msdn.microsoft.com/library/cc304081(v=vs.85).aspx) . Le changement de propriété affecte la signification de l’objet. Dans l’exemple ci-dessous, la propriété `aria-haspopup="true"` est définie sur un `<li>` élément de menu pour signifier qu’il s’agit d’une fenêtre contextuelle.

``` html
<li role="menuitem" aria-haspopup="true">Open</li>
```

Les États ne changent pas la nature de l’objet, mais représentent des informations associées à l’interaction de l’objet ou de l’utilisateur avec l’objet, par exemple [`aria-hidden`](https://msdn.microsoft.com/library/cc304083(v=vs.85).aspx) ou [`aria-checked`](https://msdn.microsoft.com/library/cc304075(v=vs.85).aspx) . Par exemple, l’état `aria-checked="false"` dans l’exemple ci-dessous correspond à la case à cocher non activée.

``` html
<div role="checkbox" aria-checked="false">Accept</div>
```

Accédez au [modèle de rôles](https://www.w3.org/TR/wai-aria-1.1/#roles) par le W3C pour afficher une liste complète des rôles, propriétés et États.

Pour plus d’informations sur ARIA, voir la section «ARIA» dans la section « [ressources](#resources) ».

## Ressources

### Notions de base sur l’accessibilité
#### [Le projet A11Y](http://a11yproject.com/)
Le projet A11Y est un effort axé sur la communauté pour faciliter l’accessibilité Web. Consultez le site de [projet A11Y](https://a11yproject.com/) pour en savoir plus sur les principes d’accessibilité de base, la [bibliothèque](https://a11yproject.com/patterns)de modèles et de gadgets accessibles et leurs [ressources](http://a11yproject.com/resources.html) sur les logiciels d’accessibilité, les blogs, les livres et les outils.

#### [Initiative Web Accessibility (WAI)](https://w3.org/WAI/)
L’initiative Web Accessibility W3C’s (WAI) vous permet d’améliorer l’accessibilité du Web. Son site fournit diverses ressources pour la [prise en main de l’accessibilité Web](https://www.w3.org/WAI/gettingstarted/Overview.html), la [création d’une inclusion, des](https://www.w3.org/WAI/users/Overview.html) [didacticiels et des présentations](https://www.w3.org/WAI/train.html), et bien plus encore.

### Blogs sur l’accessibilité
#### [Le groupe Paciello](https://www.paciellogroup.com/blog/)
Le groupe Paciello fournit des solutions de Conseil et de technologie aux organisations du monde entier pour s’assurer que leurs clients accèdent efficacement à tous les audiences, tout en remplissant les normes gouvernementales et internationales. Leur blog englobe des sujets tels que les meilleures pratiques en matière d’accessibilité Web, les outils d’accessibilité et les tendances en matière d’accessibilité.

#### [Accès simple](http://simplyaccessible.com/articles/)
Le simple accès est une équipe de spécialistes de l’accessibilité qui fournissent une formation sur l’accessibilité, des conseils et plus encore pour modifier la perception de l’accessibilité sur le Web. La section relative à cette rubrique [décrit les meilleures](http://simplyaccessible.com/articles/) pratiques en matière d’accessibilité Web, de conception accessible et plus encore.

#### [Groupe SSB Christian (SSB)](http://www.ssbbartgroup.com/blog/)
Le groupe SSB Christian est une entreprise d’accessibilité numérique qui soutient ses clients lors du développement et du déploiement de produits et services accessibles. Son blog adresse des rubriques telles que les meilleures pratiques ARIA, les tendances d’accessibilité, les webinaires, etc.

### Exemples accessibles
#### [allié. js-didacticiels](http://allyjs.io/tutorials/)
Bibliothèque JavaScript pour aider les applications Web modernes en matière d’accessibilité, rendre l’accessibilité plus simple.

#### [Heydonworks-exemples de ARIA](http://heydonworks.com/practical_aria_examples/)
Exemples pratiques ARIA pour améliorer l’accessibilité de votre application

#### [Exemples de OpenAjax](http://oaa-accessibility.org/)
Le site Web de OpenAjax Alliance est une excellente ressource de vérification des règles pour le WAI-ARIA et fournit plusieurs exemples d’implémentations WAI-ARIA.

#### [Masques](http://a11yproject.com/patterns.html)
[Le projet A11Y](http://a11yproject.com/) propose une bibliothèque de gadgets et de modèles accessibles tels que des menus, des boutons, des info-bulles, etc.

### Techniques d’accessibilité & outils
#### [Accessibilité: création d’icônes d’extension accessibles pour Microsoft Edge](../extensions/guides/accessibility.md)
Obtenez des conseils sur la création d’icônes d’extensions accessibles pour Microsoft Edge.

#### [Nom et description accessibles: calculs et mappages 1,1](https://www.w3.org/TR/accname-1.1/)
Ce document de mappage W3C décrit la façon dont les navigateurs déterminent les noms et descriptions des objets accessibles dans les langages de contenu Web, et les exposent dans les API d’accessibilité.

#### [Ressources d’évaluation de l’accessibilité](https://www.w3.org/WAI/eval/Overview.html)
Les ressources d’évaluation de l’accessibilité sont une ressource de plusieurs pages par le W3C qui souligne les différentes approches d’évaluation des sites Web pour l’accessibilité.

#### [Tests de compatibilité de technologie d’assistance](http://www.powermapper.com/tests/)
Résultats de test montrant le comportement des différents types de contenu et normes dans les technologies d’assistance comme les lecteurs d’écran.

#### [La création de sites Web accessibles est encore plus facile](https://blogs.msdn.microsoft.com/webdev/2016/05/02/building-accessible-websites-just-got-a-lot-easier/)
Ce billet de blog .NET Web Development et Tools décrit le [vérificateur d’accessibilité](https://go.microsoft.com/fwlink/p/?linkid=841539)sur le Web de Visual Studio extensions.

#### [Mappages des API d’accessibilité principales 1,1](https://www.w3.org/TR/core-aam-1.1/)
Ce document de mappage W3C explique comment les sémantiques des langages de contenu Web sont exposées aux API d’accessibilité.  

#### [Vérifications simplifiées: un premier examen de l’accessibilité sur le Web](https://www.w3.org/WAI/eval/preliminary.html)
Séries de contrôles rapide par le WAI qui vous permettent d’identifier l’accessibilité d’une page Web.

#### [Comment respecter les 2,0 de WCAG](https://www.w3.org/WAI/WCAG20/quickref/)
Référence rapide aux instructions d’accessibilité pour le contenu Web (WCAG) 2,0 (critères de réussite) et aux techniques.

#### [Mappages des API d’accessibilité HTML 1,0](https://www.w3.org/TR/html-aam-1.0/)
Ce document relatif aux mappages W3C décrit le mappage des éléments et attributs HTML 5.1 aux API d’accessibilité de la plateforme.


#### [Conseils rapides](http://a11yproject.com/#Quick-tips)
Liste de conseils de développement Web rapide pour l’accessibilité par [le projet A11Y](http://a11yproject.com/).

#### [Analyse du site](https://developer.microsoft.com/microsoft-edge/tools/staticscan/)
L’outil d’analyse de site dans le centre de développement Microsoft Edge recherche les bibliothèques obsolètes, les problèmes de disposition et les problèmes d’accessibilité.

#### [Techniques pour WCAG 2,0](https://www.w3.org/TR/WCAG20-TECHS/Overview.html)
Techniques du W3C qui fournissent des recommandations pour les développeurs Web en matière d’indications sur l' [accessibilité du contenu Web de réunion (WCAG) 2,0](https://w3.org/TR/WCAG20/) critères de réussite.

#### [Conseils en matière de développement pour l’accessibilité sur le Web](https://w3.org/WAI/gettingstarted/tips/developing.html)
Conseils du W3C sur le développement de contenus Web plus accessibles aux personnes atteintes de handicaps.

#### [WAI-ARIA, pratiques de création 1,1](http://w3c.github.io/aria-practices/)
Document par le W3C qui fournit aux lecteurs des informations de savoir comment utiliser WAI-ARIA 1,1 et recommande des approches pour rendre les widgets, la navigation et les comportements accessibles à l’aide des rôles et des propriétés WAI-ARIA.

#### [Recommandations et techniques pour le WAI](https://w3.org/WAI/guid-tech.html)
Série de recommandations et de normes en matière d’accessibilité Web développées par le WAI.  

#### [Liste des outils d’évaluation de l’accessibilité Web](https://www.w3.org/WAI/ER/tools/index.html)
Liste des outils d’évaluation de l’accessibilité du Web permettant de déterminer si les sites Web respectent les recommandations en matière d’accessibilité.

#### [Perspectives d’accessibilité sur le Web: découvrir les avantages et les avantages de tout le monde](https://w3.org/WAI/perspectives/)
Une série de vidéos de courte durée par le W3C sur l’impact de l’accessibilité et les avantages de tout le monde.
