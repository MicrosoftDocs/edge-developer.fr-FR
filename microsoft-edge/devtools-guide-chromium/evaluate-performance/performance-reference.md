---
title: Référence d’événement de chronologie
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: e5f0807204877ce034fd52ea4535795ea80ba394
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611719"
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





# Référence d’événement de chronologie   




Le mode événements de chronologie affiche tous les événements déclenchés lors de la création d’un enregistrement.  Utilisez la référence d’événement Timeline pour en savoir plus sur chaque type d’événement de chronologie.  

## Propriétés d’événement de barre de Planning courantes  

Certains détails sont présents dans les événements de tous les types, mais certains s’appliquent uniquement à certains types d’événements.  Cette section répertorie les propriétés communes aux différents types d’événements.  Les propriétés spécifiques à certains types d’événements sont répertoriées dans les références pour les types d’événements suivants.  

| Propriété | Quand est-il affiché? |  
|:--- |:--- |  
| Temps agrégé | Pour les événements comportant des **événements imbriqués**, durée de chaque catégorie d’événements. |  
| Pile d’appels | Pour les événements avec des **événements enfants**, temps pris par chaque catégorie d’événements. |  
| Temps UC | Combien de temps processeur l’événement enregistré a duré. |  
| Détails | Autres détails sur l’événement. |  
| Durée \ (au moment de l’horodatage \) | Temps pendant lequel l’événement a duré l’ensemble de ses enfants; horodatage est l’heure à laquelle l’événement s’est produit, par rapport à la date de début de l’enregistrement. |  
| Temps libre | Durée pendant laquelle l’événement a duré sans ses enfants. |  
| Taille du tas utilisée | La quantité de mémoire utilisée par l’application lorsque l’événement a été enregistré et que le delta \ (+/--\) change en taille de segment utilisée depuis le dernier échantillonnage. |  

<!--todo: add nested and child events (timelinetool) section when available -->  

## Chargement des événements  

Cette section répertorie les événements qui appartiennent au chargement d’une catégorie et leurs propriétés.  

| Événement | Description |  
|:--- |:--- |  
| Analyser le code HTML |  Microsoft Edge a exécuté l’algorithme d’analyse HTML. |  
| Fin du chargement |  Demande réseau terminée. |  
| Recevoir des données |  Les données d’une demande ont été reçues.  Il existe un ou plusieurs événements de données de réception. |  
| Recevoir une réponse |  La réponse HTTP initiale d’une demande. |  
| Envoyer la demande |  Une demande de réseau a été envoyée. |  

### Chargement des propriétés d’événement  

| Propriété | Description |  
|:--- |:--- |  
| Ressource | URL de la ressource demandée. |  
| Preview | Préversion de la ressource demandée (images uniquement \). |  
| Méthode de requête | Méthode HTTP utilisée pour la requête ( `GET` ou `POST` , par exemple). |  
| Code d’État | Code de réponse HTTP. |  
| Type MIME | Type MIME de la ressource demandée. |  
| Longueur des données codées | Durée de la ressource demandée en octets. |  

## Événements de script  

Cette section répertorie les événements qui appartiennent à la catégorie script et leurs propriétés.  

| Événement | Description |  
|:--- |:--- |  
| Cadre d’animation déclenché | Un cadre d’animation planifié déclenché et son gestionnaire de rappel appelé. |  
| Annuler le cadre d’une animation |  Un cadre d’animation planifié a été annulé. |  
| Événement GC |  Le nettoyage de la mémoire s’est produit. |  
| DOMContentLoaded |  L' [événement DOMContentLoaded][MDNWindowDOMContentLoadedEvent] a été déclenché par le navigateur.  Cet événement est déclenché lorsque l’ensemble du contenu DOM de la page a été chargé et analysé. |  
| Évaluer le script | Un script a été évalué. |  
| Événement | Un événement JavaScript (par exemple, `mousedown` ou `key` \). |  
| Appel de fonction | Un appel de fonction JavaScript de niveau supérieur a été effectué \ (s’affiche uniquement lorsque le navigateur entre dans le moteur JavaScript \). |  
| Minuteur d’installation | Un minuteur a été créé à l’aide de [setInterval ()][MDNWindowOrWorkerGlobalScopeSetInterval] ou [setTimeout ()][MDNWindowOrWorkerGlobalScopeSetTimeout]. |  
| Demander une image d’animation | Un `requestAnimationFrame()` appel a programmé une nouvelle image. |  
| Supprimer le minuteur | Un minuteur créé précédemment a été effacé. |  
| Heure |  Un script appelé [console. Time ()][ConsoleApiTime]. |  
| Heure de fin | Un script appelé [console. timeEnd ()][ConsoleApiTimeEnd]. |  
| Minuteur déclenché | Un minuteur déclenché qui était programmé avec `setInterval()` ou `setTimeout()` . |  
| Modification de l’état prêt de XHR | L’état prêt d’un XMLHTTPRequest a changé. |  
| Charge XHR | Un `XMLHTTPRequest` chargement fini. |  

### Script de propriétés d’événement  

| Propriété | Description |  
|:--- |:--- |  
| ID du minuteur | ID du minuteur. |  
| Délai d’expiration dépassé | Délai d’expiration spécifié par le minuteur. |  
| Répète | Valeur booléenne qui indique si le minuteur se répète. |  
| Appel de fonction | Fonction qui a été appelée. |  

## Rendu des événements  

Cette section répertorie les événements qui appartiennent à la catégorie de rendu et leurs propriétés.  

| Événement | Description |  
|:--- |:--- |  
| Disposition non valide | La mise en page a été invalidée par un changement DOM. |  
| Disposition | Une mise en page a été effectuée. |  
| Recalculer le style | Styles des éléments recalculés Microsoft Edge. |  
| Scroll | Le contenu du mode imbriqué a été défilé. |  

### Affichage des propriétés d’événement  

| Propriété | Description |  
|:--- |:--- |  
| Disposition invalidée | Pour les enregistrements de disposition, la trace de pile du code ayant entraîné l’invalidation de la disposition. |  
| Nœuds nécessitant une disposition | Pour les enregistrements de disposition, nombre de nœuds marqués comme ayant besoin d’une disposition avant la redisposition.  En règle générale, ces nœuds ont été invalidés par du code de développeur et un chemin d’accès descendant à la racine de réorganisation. |  
| Taille de l’arborescence de disposition | Pour les enregistrements de disposition, le nombre total de nœuds sous la racine de réorganisation \ (le nœud sur lequel Microsoft Edge démarre la redisposition \). |  
| Étendue de la disposition | Les valeurs possibles sont `Partial` \ (la limite de nouvelle disposition est une partie du DOM \) ou `Whole document` . |  
| Éléments affectés | Pour recalculer les enregistrements de style, le nombre d’éléments affectés par un recalcul de style. |  
| Styles invalidés | Pour recalculer les enregistrements de style, fournit la trace de pile du code à l’origine de l’invalidation du style. |  

## Dessin d’événements  

Cette section répertorie les événements qui appartiennent à la catégorie Paint et leurs propriétés.  

| Événement | Description |  
|:--- |:--- |  
| Calques composites | Couches d’image composites pour le moteur de rendu Microsoft Edge. |  
| Décodage d’image | Une ressource d’image a été décodée. |  
| Redimensionnement de l’image | Une image a été redimensionnée à partir de ses dimensions natives. |  
| Paint | Les couches composites ont été peintes dans une zone de l’affichage.  Pointez sur un enregistrement de Paint pour mettre en évidence la région de l’affichage mise à jour. |  

### Propriétés d’événement de dessin  

| Propriété | Description |  
|:--- |:--- |  
| Services de localisation | Pour les événements Paint, les coordonnées x et y du rectangle de peinture. |  
| Analytique | Pour les événements Paint, hauteur et largeur de la zone peinte. |  

 



<!-- image links -->  

<!-- links -->

[ConsoleApiTime]: /microsoft-edge/devtools-guide-chromium/console/api#time "Time-référence d’API de la console"  
[ConsoleApiTimeEnd]: /microsoft-edge/devtools-guide-chromium/console/api#timeend "timeEnd-XXXXXXX XXXXXXX xxx xxxxxxxxx"  
<!--[EvaluatePerformanceTimelineTool]: timeline-tool "How to Use the Timeline Tool"  -->

[MDNWindowDOMContentLoadedEvent]: https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded "Fenêtre: événement DOMContentLoaded | MDN"  
[MDNWindowOrWorkerGlobalScopeSetInterval]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setInterval "WindowOrWorkerGlobalScope. setInterval () | MDN"  
[MDNWindowOrWorkerGlobalScopeSetTimeout]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setTimeout "WindowOrWorkerGlobalScope. setTimeout () | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) et est créée par [Meggin Kearney][MegginKearney] \ (Technical Writer \) et [Flavio][FlavioCopes] configure \ (développeur de pile complète \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[FlavioCopes]: https://developers.google.com/web/resources/contributors/flaviocopes  
