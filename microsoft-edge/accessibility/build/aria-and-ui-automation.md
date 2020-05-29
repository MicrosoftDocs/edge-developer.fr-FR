---
ms.assetid: ffd1bc60-2ef1-4f11-8156-b63544cede77
description: Découvrez comment Microsoft Edge peut reconnaître les informations ARIA, puis l’exposer aux technologies d’assistance qui peuvent alors utiliser les API Microsoft UI Automation.
title: Accessibilité-ARIA et UI Automation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: accessibilité, accessibilité pour les développeurs, sites Web accessibles, Edge, développement Web, ARIA, développeur, UIA, UI Automation
ms.custom: seodec18
ms.openlocfilehash: 2fcc8160c830b5a62d8023a5cb7cc9df376c49ca
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10564675"
---
# ARIA et UI Automation dans Microsoft Edge

Le W3C définit des applications Internet riches accessibles en tant que syntaxe pour rendre le contenu Web dynamique et l’interface utilisateur personnalisée accessibles. Microsoft Edge reconnaît le rôle, l’État et les informations de propriété ARIA et l’expose aux technologies d’assistance, qui à son tour peuvent utiliser les API [Microsoft UI Automation](https://blogs.msdn.microsoft.com/winuiautomation/) pour récupérer les informations.

Consultez [HTML5Accessibility](https://html5accessibility.com) pour en savoir plus sur les nouvelles fonctionnalités HTML5 prises en charge par Microsoft Edge.

Le moteur de rendu Microsoft Edge (EdgeHTML) crée une projection accessible de pages Web, conforme aux spécifications W3C suivantes:

1. La spécification de [mappages d’API d’accessibilité html](https://w3.org/TR/html-aam-1.0/) définit comment les éléments et attributs HTML sont mappés aux objets Aria et UI Automation.
   * [Brouillon](https://w3.org/TR/html-aam-1.0/) de version stable de la spécification
   * [Brouillon de l’éditeur](https://w3c.github.io/html-aam/) -travail en cours. Notez que bien que cette spécification comporte les modifications les plus récentes, il est possible que les modifications ne soient pas encore disponibles dans Microsoft Edge.


2. La spécification de [mappages des API d’accessibilité principales](https://w3.org/TR/core-aam-1.1/) définit les principes généraux de création de l’arborescence d’accessibilité et de mappage des éléments et attributs Aria aux objets UI Automation.
   * [Brouillon](https://w3.org/TR/core-aam-1.1/) de version stable de la spécification
   * [Brouillon de l’éditeur](https://w3c.github.io/core-aam/) -travail en cours. Notez que bien que cette spécification comporte les modifications les plus récentes, il est possible que les modifications ne soient pas encore disponibles dans Microsoft Edge.  

3. [Nom et description accessibles: les spécifications de calculs et de mappages d’API](https://w3.org/TR/accname-aam-1.1/) définissent la façon de calculer le nom et la description d’objets accessibles pour le code HTML et les valeurs d’attributs et d’éléments Aria disponibles pour les éléments accessibles.
   * [Brouillon](https://w3.org/TR/accname-aam-1.1/) de version stable de la spécification  
   * [Brouillon de l’éditeur](https://w3c.github.io/accname/) -travail en cours. Notez que bien que cette spécification comporte les modifications les plus récentes, il est possible que les modifications ne soient pas encore disponibles dans Microsoft Edge.   

Pour plus d’informations sur l’architecture de l’accessibilité dans Microsoft Edge, consultez la rubrique créer un billet de blog sur la [plateforme Web plus accessible](https://blogs.windows.com/msedgedev/2016/04/20/building-a-more-accessible-web-platform/) .  Pour obtenir des exemples sur la façon dont la nouvelle architecture améliore l’utilisation de l’utilisateur final et en particulier la façon dont le balisage définit l’efficacité de la navigation avec les technologies d’assistance telles que les lecteurs d’écran, voir [créer une interface utilisateur plus accessible avec HTML5 et UIA](https://blogs.windows.com/msedgedev/2016/05/12/accessible-ux-with-html5-and-uia/).
