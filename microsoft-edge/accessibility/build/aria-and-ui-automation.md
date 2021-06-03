---
ms.assetid: ffd1bc60-2ef1-4f11-8156-b63544cede77
description: Découvrez comment Microsoft Edge peut reconnaître les informations ARIA, puis les exposer aux technologies d’assistance qui peuvent ensuite utiliser les API Microsoft UI Automation.
title: 'Accessibilité : ARIA et automatisation de l’interface utilisateur'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: accessibilité, accessibilité pour les développeurs, sites web accessibles, edge, développement web, ARIA, développeur, UIA, UI Automation
ms.custom: seodec18
ms.openlocfilehash: 2fcc8160c830b5a62d8023a5cb7cc9df376c49ca
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10564675"
---
# ARIA et UI Automation dans Microsoft Edge

Le W3C définit ARIA (Accessible Rich Internet Applications) comme syntaxe pour rendre le contenu web dynamique et l’interface utilisateur personnalisée accessibles. Microsoft Edge reconnaît les informations sur le rôle, l’état et la propriété ARIA et les expose aux technologies d’assistance, qui à leur tour peuvent utiliser les API [Microsoft UI Automation](https://blogs.msdn.microsoft.com/winuiautomation/) pour récupérer les informations.

Visitez [HTML5Accessibility pour](https://html5accessibility.com) obtenir des informations sur les nouvelles fonctionnalités HTML5 qui sont accessibles Microsoft Edge.

Le Microsoft Edge de rendu (EdgeHTML) crée une projection accessible de pages web, conformément aux spécifications W3C suivantes :

1. La [spécification mappages d’API](https://w3.org/TR/html-aam-1.0/) d’accessibilité HTML définit la façon dont les éléments et attributs HTML sont mappages avec les objets ARIA et UI Automation.
   * [Brouillon de travail](https://w3.org/TR/html-aam-1.0/) : version stable de la spécification
   * [Brouillon de l’éditeur](https://w3c.github.io/html-aam/) : travail en cours. Notez que bien que cette spécification ait les dernières modifications, il se peut que les modifications ne soient pas encore disponibles Microsoft Edge.


2. La [spécification Mappages](https://w3.org/TR/core-aam-1.1/) des API d’accessibilité principales définit des principes généraux pour la création de l’arborescence d’accessibilité et le mappage des éléments et attributs ARIA aux objets UI Automation.
   * [Brouillon de travail](https://w3.org/TR/core-aam-1.1/) : version stable de la spécification
   * [Brouillon de l’éditeur](https://w3c.github.io/core-aam/) : travail en cours. Notez que bien que cette spécification ait les dernières modifications, il se peut que les modifications ne soient pas encore disponibles Microsoft Edge.  

3. La spécification [Accessible Name and Description: Computation and API Mappings](https://w3.org/TR/accname-aam-1.1/) définit comment calculer le nom et la description des objets accessibles en fonction du code HTML et des valeurs d’éléments et d’attributs ARIA disponibles pour les éléments accessibles.
   * [Brouillon de travail](https://w3.org/TR/accname-aam-1.1/) : version stable de la spécification  
   * [Brouillon de l’éditeur](https://w3c.github.io/accname/) : travail en cours. Notez que bien que cette spécification ait les dernières modifications, il se peut que les modifications ne soient pas encore disponibles Microsoft Edge.   

Pour plus d’informations sur l’architecture d’accessibilité Microsoft Edge, consultez le billet de blog Création d’une plateforme [web plus accessible.](https://blogs.windows.com/msedgedev/2016/04/20/building-a-more-accessible-web-platform/)  Pour obtenir des exemples de la façon dont la nouvelle architecture améliore l’expérience de l’utilisateur final et plus précisément comment le code définit l’expérience de navigation avec des technologies d’assistance telles que les lecteurs d’écran, visitez La création d’une expérience utilisateur plus accessible avec HTML5 et [UIA](https://blogs.windows.com/msedgedev/2016/05/12/accessible-ux-with-html5-and-uia/).
