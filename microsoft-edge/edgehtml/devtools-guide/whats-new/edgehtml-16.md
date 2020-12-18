---
description: Fonctionnalités ajoutées au Microsoft Edge DevTools de la mise à jour de Windows 10 pour les créateurs du automne (EdgeHTML 16)
title: DevTools dans EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, edgehtml 16
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2d24b6851e843f491e470b18ccc18d559ed5533d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232878"
---
# DevTools de la mise à jour de reports de Windows 10 (EdgeHTML 16)

Grâce à cette version, nous avons commencé un effort de refactorisation DevTools majeur pour une fiabilité et des performances améliorées, ainsi que les nouvelles fonctionnalités que vous pouvez commencer à utiliser dès maintenant. 

Voici les fonctionnalités de Microsoft Edge DevTools fournies avec la [mise à jour de Windows 10](/windows/uwp/whats-new/windows-10-build-16299) pour les créateurs du automne ([EdgeHTML 16](https://aka.ms/devguide_edgehtml_16)).

## Écouteurs d’événements ancêtres 

Le volet **Events** ajoute désormais l’option d’affichage des écouteurs d’événements inscrits sur n’importe quel ancêtre de l’élément actuellement sélectionné (dans le panneau **éléments** ), en plus de celles de l’élément lui-même. Par ailleurs, vous pouvez regrouper l’affichage d’un écouteur d’événements par *événement* ou *élément*. 

![Volet de vérification de l’écouteur d’événements](../media/elements_ancestor_events.png)

## Points d’arrêt de mutation DOM

Vous pouvez désormais définir des points d’arrêt de mutation DOM pour qu’ils s’arrêtent dans le débogueur dès qu’un nœud d’élément sélectionné change. Dans le panneau **éléments** , cliquez sur n’importe quel élément de l’arborescence DOM et sélectionnez une ou plusieurs des options suivantes:

 - Arrêt du nœud supprimé
 - Saut de la sous-arborescence modifié
 - Arrêt du saut sur l’attribut modifié

Vous pouvez gérer vos points d’arrêt de mutation à partir du volet **points d’arrêt DOM** dans les panneaux **éléments** ou **débogueur** .

![Volet points d’arrêt DOM](../media/elements_dom_breakpoints.png)

## CSS at-Rule support

Les règles CSS «at» (@) sont désormais représentées par d’autres déclarations de règles CSS dans le volet **styles** , y compris les `@keyframes` règles d’animation (actuellement limitées aux lecture seule), les `@supports` requêtes de fonctionnalités et les `@media` requêtes.

![CSS at-inspection-règles du volet style de DevTools](../media/elements_at_rules.png)

## Volet polices CSS

`@font-face`Les règles CSS possèdent désormais leur propre volet **polices** dédiées qui indique l’emplacement de chargement de la police (*locale* ou *réseau*) et le nombre de caractères qui l’utilisent. Si une police est chargée à partir du réseau, DevTools affiche la règle qui s’en est importée avec son alias et son type de police.

![Informations sur la police CSS](../media/elements_fonts.png)

## Prise en charge de Pseudo-éléments CSS

Le volet **styles** permet de regrouper les Pseudo-éléments dans leurs propres titres et de ne pas afficher leur contenu comme barré.

**Avant:**
<br>
![Le contenu généré a été rayé.](../media/gc_before.png)

**Après:**
<br>
![Le contenu généré n’apparaît plus avec un barré](../media/gc_after.png)

## Améliorations de la console

Le panneau de la **console** dispose d’une fonctionnalité d’expérience utilisateur améliorée pour une plus grande convivialité et une expérience IntelliSense plus riche et plus rapide.

**Avant:** 
![ Console précédente](../media/console_old.png)

**Après:** 
![ Nouvelle console](../media/console_new.png)

Nous avons également ajouté les améliorations suivantes:

 -  Utilisez `Shift + Enter` cette option pour ajouter une ligne supplémentaire à une commande avant de l’exécuter `Enter` . (Auparavant, il y a eu une *option de basculement vers le bouton bascule du mode multiligne/ligne unique* .)

 - Les nouvelles API suivantes sont prises en charge:
    - méthode [ **console. table (**_objet_*_)_* ](../console/console-api.md#organizing-log-output)
    - commande [ **getEventListeners (**_objet_*_)_* ](../console/command-line.md#event-listeners)
    - commande [ **Keys (**_objet_*_)_* ](../console/command-line.md#object-inspection)
    - commande [ **valeurs (**_objet_*_)_* ](../console/command-line.md#object-inspection)
    - sélecteur d' [ **$x (**_expression XPath_*_)_* ](../console/command-line.md#dom-selectors)

 - Le paramètre de mise en forme [**% c ()**](../console/console-api.md#logging-custom-messages) est désormais pris en charge

## Amélioration du débogage

Outre une suite de nouvelles fonctionnalités pour le débogage des [travailleurs et du cache de votre service PWA](#progressive-web-app-debugging), le débogueur a ajouté les fonctionnalités suivantes:

### Débogage consolidé des ressources partagées

Même si une ressource, telle qu’un fichier chargé à partir du réseau de distribution de contenu (CDN), est référencée plusieurs fois dans votre code, DevTools fournit désormais une instance de débogage unique pour ce fichier, dans laquelle vous pouvez définir des points d’arrêt communs qui seront pris en compte, quel que soit l’endroit où ce fichier est référencé. (Auparavant, chaque référence de script était considérée comme une ressource unique mappée à un ensemble distinct de points d’arrêt.)

### Modification dynamique JavaScript avec la *modification lors de l’inactivité*

Vous pouvez maintenant modifier votre code JavaScript live lors d’une session de débogage. Cette fonctionnalité a fait l’expérience d’une expérimentation disponible (derrière un drapeau) dans l' [ancienne](https://blogs.windows.com/buildingapps/2017/04/05/windows-10-creators-update-creators-update-sdk-released/#MMhK2OdcrR12Vi6u.97) version (*Windows 10 Creators Update*) et il s’agit maintenant d’une fonctionnalité permanente. Il suffit de sélectionner n’importe quel fichier de script dans le volet **débogueur** , de modifier, puis de cliquer sur **Enregistrer** (ou `Ctrl+S` ) pour tester vos modifications lors de la prochaine exécution de la section de code. 

![Le débogueur vous permet d’apporter des modifications aux scripts et de les différencier](../media/debugger_edit_buttons.png) 

Cliquez sur le bouton **comparer le document à l’original** pour afficher un aperçu de ce que vous avez modifié.

![Vue diff du code modifié dans le débogueur](../media/debugger_edit_code.png) 

Tenez compte des contraintes suivantes:

- La modification des scripts ne fonctionne que dans les fichiers externes *. js* (et non incorporés `<script>` au *format. html*)
- Les modifications sont enregistrées en mémoire et vidées lors du rechargement du document, vous ne pourrez donc pas exécuter de modifications à l’intérieur d’un `DOMContentLoaded` Gestionnaire, par exemple
- Il n’existe actuellement aucune méthode (par exemple, option **Enregistrer sous** ) pour enregistrer vos modifications sur un disque à partir de devtools

## Raccourcis

Vous pouvez à présent lancer DevTools vers le dernier panneau affiché ( `Ctrl+Shift+I` ) ou directement sur la console ( `Ctrl+Shift+J` ) comme sur d’autres navigateurs importants.

## Débogage de l’application Web progressive

Testez la prise en charge expérimentale des applications Web progressives (PWAs) dans Microsoft Edge et DevTools en sélectionnant l’option **activer les travailleurs de service** dans `about:flags` (et en redémarrant Microsoft Edge). Si un site utilise des **travailleurs de service** et/ou l’API de **cache** , les entrées du panneau du **débogueur** seront insérées dans chaque origine, de la même façon que dans le stockage Web et l’inspection des cookies.

Le fait de cliquer sur une entrée de service particulière entraîne l’ouverture de la **vue d’ensemble**du travailleur de service, dans laquelle vous pouvez gérer l’enregistrement du travailleur de service pour l’étendue donnée et forcer une notification de transmission de test. Vous pouvez également **arrêter** / de**lancer** des travailleurs de service individuels et les **inspecter** à partir d’une fenêtre de débogage séparée:

![Volet vue d’ensemble des travailleurs de services](../media/debugger_sw_overview.png)

Veuillez noter ce qui suit le débogage du travailleur de services:

 - Le débogage d’un ouvrier de service lancera une nouvelle instance du DevTools séparée des outils de la page, car les travailleurs de services peuvent être partagés entre plusieurs onglets. 
 - Les [éléments](../elements.md) et les panneaux d' [émulation](../emulation.md) ne sont pas pris en tant que débogueur de service, car ils s’exécutent en arrière-plan et ne contrôlent pas directement le serveur principal de votre application.
 - Pour le moment, le trafic réseau d’un ouvrier de service est uniquement signalé à partir de l’instance de débogage de DevTools pour ce travailleur et non à partir de l’instance centrale de la page elle-même.

Le fait de cliquer sur une entrée de cache spécifique ouvre le gestionnaire de **cache** pour vous permettre d’inspecter et éventuellement de supprimer les entrées de cache (paires de*requête* et de clé de *réponse* /valeur).
