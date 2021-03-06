---
description: Le mode événements de chronologie affiche tous les événements déclenchés lors de l’enregistrement.  Utilisez la référence d’événement de chronologie pour en savoir plus sur chaque type d’événement de chronologie.
title: Référence des événements de chronologie
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 2a166c9eebc980682fa872e5ee8d213f2058b384
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398664"
---
<!-- Copyright Meggin Kearney and Flavio Copes

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="timeline-event-reference"></a>Référence des événements de chronologie  

Le mode événements de chronologie affiche tous les événements déclenchés lors de l’enregistrement.  Utilisez la référence d’événement de chronologie pour en savoir plus sur chaque type d’événement de chronologie.  

## <a name="common-timeline-event-properties"></a>Propriétés courantes des événements de chronologie  

Certains détails sont présents dans les événements de tous types, tandis que d’autres s’appliquent uniquement à certains types d’événements.  Cette section répertorie les propriétés communes aux différents types d’événements.  Les propriétés spécifiques à certains types d’événements sont répertoriées dans les références pour les types d’événements qui suivent.  

| Propriété | Quand s’affiche-t-elle ? |  
|:--- |:--- |  
| Temps agrégé | Pour les événements avec **des événements**imbrmbrés, le temps pris par chaque catégorie d’événements. |  
| Pile des appels | Pour les événements avec **des événements enfants,** le temps pris par chaque catégorie d’événements. |  
| Temps processeur | Temps processeur de l’événement enregistré. |  
| Détails | Autres détails sur l’événement. |  
| Duration \(at time-stamp\) | Combien de temps l’événement a pris avec tous ses enfants pour se terminer ; est l’heure à laquelle l’événement s’est produit, par rapport au début de l’enregistrement. |  
| Temps libre | Durée de l’événement sans aucun de ses enfants. |  
| Taille de tas utilisée | Quantité de mémoire utilisée par l’application lors de l’enregistrement de l’événement, et le delta \(+/-\) change en taille de tas utilisée depuis le dernier échantillonnage. |  

<!--todo: add nested and child events (timelinetool) section when available -->  

## <a name="loading-events"></a>Chargement d’événements  

Cette section répertorie les événements qui appartiennent à la catégorie Loading et leurs propriétés.  

| Événement | Description |  
|:--- |:--- |  
| Code HTML d’parse |  Microsoft Edge a été l’application de l’algorithme d’analyse HTML. |  
| Terminer le chargement |  Demande réseau terminée. |  
| Recevoir des données |  Les données d’une demande ont été reçues.  Il existe un ou plusieurs événements De réception de données. |  
| Recevoir une réponse |  Réponse HTTP initiale d’une requête. |  
| Envoyer une demande |  Une demande réseau a été envoyée. |  

### <a name="loading-event-properties"></a>Chargement des propriétés de l’événement  

| Propriété | Description |  
|:--- |:--- |  
| Ressource | URL de la ressource demandée. |  
| Preview | Aperçu de la ressource demandée \(images uniquement\). |  
| Request, méthode | Méthode HTTP utilisée pour la requête \( `GET` ou `POST` , par exemple\). |  
| Code d’état | Code de réponse HTTP. |  
| MIME Type | Type MIME de la ressource demandée. |  
| Longueur des données codées | Longueur de la ressource demandée en octets. |  

## <a name="scripting-events"></a>Événements de script  

Cette section répertorie les événements qui appartiennent à la catégorie Scripting et leurs propriétés.  

| Événement | Description |  
|:--- |:--- |  
| Image d’animation déclenché | Une image d’animation programmée a été déclenché et son handler de rappel a été appelé. |  
| Annuler un cadre d’animation |  Une image d’animation programmée a été annulée. |  
| GC, événement |  Un garbage collection s’est produit. |  
| DOMContentLoaded |  [L’événement DOMContentLoaded][MDNWindowDOMContentLoadedEvent] a été déclenché par le navigateur.  Cet événement est déclenché lorsque tout le contenu DOM de la page est chargé et l’est également. |  
| Évaluer le script | Un script a été évalué. |  
| Événement | Un événement JavaScript \(par exemple, `mousedown` ou `key` \). |  
| Appel de fonction | Un appel de fonction JavaScript de niveau supérieur a été effectué \(apparaît uniquement lorsque le navigateur entre dans le moteur JavaScript\). |  
| Installer le timer | Un timer a été créé avec [setInterval()][MDNWindowOrWorkerGlobalScopeSetInterval] ou [setTimeout()][MDNWindowOrWorkerGlobalScopeSetTimeout]. |  
| Image d’animation de demande | Un `requestAnimationFrame()` appel a programmé une nouvelle image. |  
| Supprimer le temps | Un timer précédemment créé a été effacé. |  
| Heure |  Script appelé [console.time()][ConsoleApiTime]. |  
| Fin de l’heure | Un script appelé [console.timeEnd()][ConsoleApiTimeEnd]. |  
| Timer Fired | Un timer déclenché qui a été programmé avec `setInterval()` ou `setTimeout()` . |  
| XHR Ready State Change | L’état prêt d’un XMLHTTPRequest a changé. |  
| Charge XHR | Chargement `XMLHTTPRequest` terminé. |  

### <a name="scripting-event-properties"></a>Propriétés des événements de script  

| Propriété | Description |  
|:--- |:--- |  
| Timer ID | ID du timer. |  
| Délai d’expiration dépassé | Délai spécifié par le timer. |  
| Répétitions | Booléen qui spécifie si le timer se répète. |  
| Appel de fonction | Fonction qui a été invoquée. |  

## <a name="rendering-events"></a>Rendu des événements  

Cette section répertorie les événements qui appartiennent à la catégorie Rendering et leurs propriétés.  

| Événement | Description |  
|:--- |:--- |  
| Invalider la disposition | La mise en page a été invalidée par une modification DU DOM. |  
| Disposition | Une mise en page a été effectuée. |  
| Recalculer le style | Styles d’éléments recalculés par Microsoft Edge. |  
| Scroll | Le contenu de l’affichage imbrmbré a été fait défiler. |  

### <a name="rendering-event-properties"></a>Rendu des propriétés d’événement  

| Propriété | Description |  
|:--- |:--- |  
| Disposition non valide | Pour les enregistrements de disposition, la trace de pile du code qui a provoqué l’invalidation de la disposition. |  
| Les nodes qui ont besoin d’une disposition | Pour les enregistrements de disposition, le nombre de nodes qui ont été marqués comme devant être mis en page avant le début du relais.  Il s’agit normalement de ces derniers qui ont été invalidés par le code du développeur, ainsi qu’un chemin vers le haut pour relayer la racine. |  
| Taille de l’arborescence de disposition | Pour les enregistrements de disposition, le nombre total de nœuds sous la racine du relais \(le nœud que Microsoft Edge démarre le relais\). |  
| Étendue de disposition | Les valeurs `Partial` possibles sont \(la limite de disposition est une partie du DOM\) ou `Whole document` . |  
| Éléments affectés | Pour recalculer les enregistrements de style, nombre d’éléments affectés par un recalcul de style. |  
| Styles invalidés | Pour recalculer les enregistrements de style, fournit la trace de pile du code à l’origine de l’invalidation du style. |  

## <a name="painting-events"></a>Événements de dessin  

Cette section répertorie les événements qui appartiennent à la catégorie Painting et leurs propriétés.  

| Événement | Description |  
|:--- |:--- |  
| Couches composites | Couches d’image composites pour le moteur de rendu Microsoft Edge. |  
| Décodage d’image | Une ressource d’image a été décodée. |  
| Resize d’image | Une image a été re dimensionisée à partir de ses dimensions natives. |  
| Paint | Les couches composites ont été peints dans une région de l’affichage.  Le pointage sur un enregistrement Paint met en évidence la région de l’affichage qui a été mis à jour. |  

### <a name="painting-event-properties"></a>Propriétés de l’événement Painting  

| Propriété | Description |  
|:--- |:--- |  
| Emplacement | Pour les événements Paint, les coordonnées x et y du rectangle de couleur. |  
| Dimensions | Pour les événements Paint, la hauteur et la largeur de la région peint. |  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->

[ConsoleApiTime]: /microsoft-edge/devtools-guide-chromium/console/api#time "time - Référence de l’API console"  
[ConsoleApiTimeEnd]: /microsoft-edge/devtools-guide-chromium/console/api#timeend "timeEnd - Référence de l’API de console"  
<!--[EvaluatePerformanceTimelineTool]: timeline-tool "How to Use the Timeline Tool"  -->

[MDNWindowDOMContentLoadedEvent]: https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded "Window : événement DOMContentLoaded | MDN"  
[MDNWindowOrWorkerGlobalScopeSetInterval]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setInterval "WindowOrWorkerGlobalScope.setInterval() | MDN"  
[MDNWindowOrWorkerGlobalScopeSetTimeout]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setTimeout "WindowOrWorkerGlobalScope.setTimeout() | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est trouvée ici et est co-auteure par [Meggin Kearney][MegginKearney] \(Tech Writer\) et [ContrôleioQuets][FlavioCopes] \(Full Stack Developer\). [](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[FlavioCopes]: https://developers.google.com/web/resources/contributors/flaviocopes  
