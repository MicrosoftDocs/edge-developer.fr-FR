---
description: En savoir plus sur les améliorations apportées aux travailleurs de services et leur utilisation.
title: Améliorations apportées aux travailleurs de services
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, travailleur de service, PWA
ms.openlocfilehash: 4e1b43235ccd7b108d2aadd1c803aa3276fa1265
ms.sourcegitcommit: 080759f68a0a158f10dc20d20c14e222ace1be84
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "11190029"
---
# Améliorations apportées aux travailleurs de services  

Cet article vous présente les améliorations apportées aux [travailleurs de services][MdnServiceWorkerApi] et aux requêtes réseau qui passent par eux.  Les **améliorations apportées aux travailleurs de services** se trouvent dans les outils **réseau**, **application**et **sources** .  Les améliorations incluent les tâches suivantes.  

*   Déboguer selon les chronologies des travailleurs de service.  
    *   Le début d’une demande et la durée de l’amorce.  
    *   Mise à jour vers l’enregistrement du travailleur de service.  
    *   Exécution d’une requête à l’aide du gestionnaire d' [événements FETCH][MdnFetchEvent] .  
    *   Exécution de tous les événements de récupération pour le chargement d’un client.  
*   Explorez les détails d’exécution des gestionnaires d’événements de récupération, d’installation de gestionnaires d’événements et de gestionnaires d’événements d’activation.  
*   Pas à pas dans le gestionnaire d’événements Fetch et déconnectez-vous avec les [informations de script de page](#sources).  

Ces expériences s’étendent à trois outils de développement différents.  

1.  Outil [réseau](#network) .  Choisissez une requête réseau qui s’exécute par le biais d’un travailleur de service et accédez à la chronologie correspondante du travailleur de service dans l’outil **minutage** .  
1.  Outil de l' [application](#application) .  Pour déboguer les travailleurs de service, accédez à l’outil **travailleurs de service** .  
1.  Outil [sources](#sources) .  Accédez à des informations de script de page lorsque vous accédez à des gestionnaires d’événements Fetch.  

## Network  

:::image type="complex" source="../media/sw-network-timeline.msft.png" alt-text="Chronologie du travailleur de service dans l’outil réseau" lightbox="../media/sw-network-timeline.msft.png":::
   Vue réseau  
:::image-end:::  

Pour accéder aux fonctionnalités de débogage du travailleur de service dans l’outil **réseau** , effectuez l’une des actions suivantes.  

*   Accédez directement à l’outil **réseau** .  
*   Démarré dans l’outil de l' **application** .  
    
### Demander le routage  

Pour faciliter l’affichage du routage de requête, les chronologies affichent désormais le démarrage du travailleur de service et les `respondWith` événements de récupération.  Pour déboguer et visualiser une requête réseau transmise par le biais d’un travailleur de service, procédez comme suit.  

1.  Cliquez sur la demande de réseau qui a été passée par un travailleur de service.  
1.  Ouvrez l’outil **minutage** .  
    
### Extraire des événements  

Pour en savoir plus sur les `respondWith` événements FETCH, cliquez sur la flèche déroulante située à gauche de la zone `respondWith` .  Pour en savoir plus sur la demande et la **réponse** **d’origine** reçues, utilisez les flèches déroulantes correspondantes.  

## Application  

:::image type="complex" source="../media/sw-application-timeline.msft.png" alt-text="Affichage des applications" lightbox="../media/sw-application-timeline.msft.png":::
   Affichage des applications  
:::image-end:::  

### Chronologie des mises à jour de service Worker  

L’équipe Microsoft Edge DevTools a ajouté une chronologie dans l’outil de l' **application** pour refléter le cycle de vie des mises à jour du travailleur de service.  Il affiche les événements d’installation et d’activation.  Chacun des événements dispose d’une flèche déroulante correspondante pour vous fournir des informations supplémentaires.  

### Demander le routage et récupérer des événements  

Vous pouvez maintenant accéder aux chronologies du travailleur de service via l’outil **réseau** du tiroir de la console.  La fonctionnalité présente les performances, réduit la réplication de l’interface utilisateur et crée une connaissance plus complète en matière de débogage.  

1.  Ouvrez le travailleur de service en cours de débogage.  
1.  Cliquez sur le bouton **réseau** pour ouvrir l' [interface de demande de routage](#network).  
1.  Utilisez les listes déroulantes **respondWith** pour récupérer des informations de demande et de réponse à l’événement.  

L’outil **réseau** affiche les requêtes réseau ayant suivi le travailleur de service en cours de débogage.  Le filtre automatique permet de limiter votre exploration.

## Sources  

:::image type="complex" source="../media/sw-sources.msft.png" alt-text="Affichage DOM" lightbox="../media/sw-sources.msft.png":::
   Affichage DOM  
:::image-end:::  

Pour trouver d’autres informations sur la pile, définissez un point d’arrêt dans le gestionnaire de récupération.  Les détails conduisent à l’endroit où la ressource est demandée dans le script de la page.  Lorsque le débogueur s’arrête dans un gestionnaire de récupération, des informations sur la pile combinée apparaissent dans le panneau de droite.  Après cela, vous pouvez vous déplacer dans les frames de pile.  

### Future Work  

L’équipe Microsoft Edge DevTools envisage d’améliorer davantage les détails de la mise en cache et étudie d’autres façons d’améliorer l’interface de débogage du travailleur de services pour les développeurs d' [applications Web progressives][MdnProgressiveWebApps] .  

## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MdnFetchEvent]: https://developer.mozilla.org/docs/Web/API/FetchEvent "FetchEvent | MDN"  
[MdnProgressiveWebApps]: https://developer.mozilla.org/docs/Web/Progressive_web_apps "Applications Web progressives (PWAs) | MDN"  
[MdnServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API du travailleur de service | MDN"  
