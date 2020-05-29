---
description: Liste de références pour les domaines pris en charge dans la version 0,2 du protocole Microsoft Edge DevTools.
title: Domains-protocole DevTools version 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 32634df94320e6474170726dfcd6164c5d02631a
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565469"
---
# Domaines de protocole DevTools
## [CSS](css.md)
Ce domaine présente les opérations en lecture/écriture CSS. Tous les objets CSS (feuilles de style, règles et styles) sont associés à des `id` opérations ultérieures sur l’objet associé. Chaque type d’objet possède une `id` structure spécifique et celles-ci ne sont pas interchangeables entre les objets de différents genres. Les objets CSS peuvent être chargés en utilisant les `get*ForNode()` appels (qui acceptent un ID de nœud DOM). Un client peut également suivre les feuilles de style par le biais des `styleSheetAdded` / `styleSheetRemoved` événements, puis charger le contenu de la feuille de style requis au moyen des `getStyleSheet[Text]()` méthodes.
## [DOM](dom.md)
Ce domaine expose les opérations en lecture/écriture DOM. Chaque nœud DOM est représenté avec son objet Mirror contenant un objet `id` . Cela `id` peut être utilisé pour obtenir des informations supplémentaires sur le nœud, le résoudre dans le wrapper d’objet JavaScript, etc. Il est important que le client reçoit les événements DOM uniquement pour les nœuds connus du client. Le principal effectue le suivi des nœuds envoyés au client et n’envoie jamais le même nœud deux fois. Il incombe au client de recueillir des informations sur les nœuds envoyés au client.<p>Notez que les `iframe` éléments de propriétaire renvoient les éléments de document correspondants comme leurs nœuds enfants.</p>
## [DOMDebugger](domdebugger.md)
Le débogage DOM permet de définir des points d’arrêt sur des événements et des événements DOM spécifiques. L’exécution JavaScript s’arrêtera sur ces opérations comme s’il s’agissait d’un jeu de points d’arrêt régulier.
## [Débogueur](debugger.md)
Le domaine du débogueur expose les fonctionnalités de débogage JavaScript. Elle permet de définir et de supprimer des points d’arrêt, de parcourir l’exécution, d’explorer les traces de pile, etc.
## [Superposition](overlay.md)
Le domaine superposé expose des ornements visuels et une interaction de sélection de nœud
## [Page](page.md)
Les actions et événements liés à la page inspectée appartiennent au domaine de la page.
## [Runtime](runtime.md)
Le domaine d’exécution expose le runtime JavaScript au moyen de l’évaluation à distance et des objets miroirs. Les résultats d’évaluation sont retournés sous la forme d’un objet miroir exposant le type d’objet, la représentation de chaîne et l’identificateur unique qui peuvent être utilisés pour une référence d’objet supplémentaire. Les objets d’origine sont conservés en mémoire, sauf s’ils sont explicitement émis.
## [Schéma](schema.md)
Fournit des informations sur le schéma de protocole.