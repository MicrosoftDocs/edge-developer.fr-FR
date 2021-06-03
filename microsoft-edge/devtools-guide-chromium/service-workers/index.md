---
description: Tout sur les améliorations apportées aux services de travail et sur l’utilisation de chacune d’elles.
title: Améliorations apportées aux services de travail
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/19/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, développement web, outils f12, devtools, service de travail, PWA
ms.openlocfilehash: 2f32155d1d28d1e65ad29abfe58a414f3e3c6ed7
ms.sourcegitcommit: 661e8def3f27cea381c59ac38954789e736c18f4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "11387281"
---
# <a name="service-worker-improvements"></a>Améliorations apportées aux services de travail  

Cet article vous explique les améliorations apportées aux outils de développement pour travailler avec les travailleurs du [service][MdnServiceWorkerApi] et les demandes réseau qui passent par chacun d’eux.  Les **améliorations apportées aux services de travail** se font dans les outils **Réseau,** **Application**et **Sources.**  Les améliorations simplifient les tâches suivantes.  

*   Déboguer en fonction des chronologies du service de travail.  
    *   Le début d’une demande et la durée du démarrage.  
    *   Mise à jour de l’inscription du service de travail.  
    *   Runtime d’une demande à l’aide du [handler d’événements fetch.][MdnFetchEvent]  
    *   Runtime de tous les événements de récupération pour le chargement d’un client.  
*   Explorez les détails de l’runtime des handlers d’événements de récupération, installez les handlers d’événements et activez les handlers d’événements.  
*   Entrez et sortez du handler d’événements de récupération avec les [informations de script de page.](#sources)  
    
Les expériences s’étendent sur trois outils de développement différents.  

1.  Outil [Réseau.](#network)  Choisissez une demande réseau qui s’exécute par le biais d’un service de travail et qui accède à la chronologie correspondante du travail de service dans **l’outil de minutage.**  
1.  Outil [Application.](#application)  Pour déboguer les travailleurs du service, accédez à l’outil **Travailleurs de** service.  
1.  Outil [Sources.](#sources)  Accéder aux informations de script de page lors de l’accès aux handlers d’événements de récupération.  
    
## <a name="network"></a>Network  

:::image type="complex" source="../media/sw-network-timeline.msft.png" alt-text="Chronologie du travail de service dans l’outil Réseau" lightbox="../media/sw-network-timeline.msft.png":::
   Affichage réseau  
:::image-end:::  

Pour accéder aux fonctionnalités de débogage du service de travail dans l’outil **Réseau,** effectuer l’une des actions suivantes.  

*   Accédez directement à **l’outil** Réseau.  
*   Démarré dans **l’outil Application.**  
    
### <a name="request-routing"></a>Routage des demandes  

Pour faciliter la visualisation du routage des demandes, les chronologies affichent désormais la start-up du service de travail et les événements `respondWith` de récupération.  Pour déboguer et visualiser une demande réseau transmise via un service de travail, effectuer les actions suivantes.  

1.  Choisissez la demande réseau qui a été passée par un service de travail.  
1.  Ouvrez **l’outil** De minutage.  
    
### <a name="fetch-events"></a>Récupérer des événements  

Pour en savoir plus sur les `respondWith` événements de récupération, sélectionnez la flèche de la flèche vers la gauche du `respondWith` .  Pour plus d’informations **** sur la demande d’origine et la réponse **reçue,** utilisez les flèches de liste rouge correspondantes.  

## <a name="application"></a>Application  

:::image type="complex" source="../media/sw-application-timeline.msft.png" alt-text="Affichage de l’application" lightbox="../media/sw-application-timeline.msft.png":::
   Affichage de l’application  
:::image-end:::  

### <a name="service-worker-update-timeline"></a>Chronologie de mise à jour du service de travail  

L Microsoft Edge’équipe DevTools a ajouté une chronologie dans l’outil **Application** pour refléter le cycle de vie de mise à jour du service de travail.  Il affiche les événements d’installation et d’activation.  Chacun des événements possède une flèche de liste verte correspondante pour vous donner plus de détails.  

### <a name="request-routing-and-fetch-events"></a>Demander des événements de routage et de récupération  

Vous pouvez désormais accéder aux chronologies de travail de service via **l’outil Réseau** dans le caisse de la console.  La fonctionnalité bénéficie de performances, réduit la duplication de l’interface utilisateur et crée une expérience de débogage plus complète.  

1.  Ouvrez le service de travail que vous déboguer.  
1.  Choisissez le **bouton Réseau** pour ouvrir l’expérience [de routage des demandes.](#network)  
1.  Utilisez les dropdowns **respondWith** pour récupérer les informations de demande d’événement et de réponse.  

**L’outil** Réseau affiche les demandes réseau qui ont été passées par le service de travail que vous déboguer.  Le filtre automatique est un moyen de restreindre votre exploration.

## <a name="sources"></a>Sources  

:::image type="complex" source="../media/sw-sources.msft.png" alt-text="Affichage DOM" lightbox="../media/sw-sources.msft.png":::
   Affichage DOM  
:::image-end:::  

Pour trouver plus d’informations sur la pile, définissez un point d’coupure dans le handler d’extraction.  Les détails mènent à l’endroit où la ressource est demandée dans le script de page.  Lorsque le débogger s’interrompt à l’intérieur d’un handler d’extraction, une pile combinée d’informations s’affiche dans le panneau à droite.  Après cela, vous pouvez vous déplacer dans les cadres de pile.  

### <a name="future-work"></a>Travail à venir  

L Microsoft Edge’équipe DevTools prévoit de développer davantage les détails du cache et étudie d’autres façons d’améliorer l’expérience de débogage des travailleurs du service pour les développeurs [d’applications Web][MdnProgressiveWebApps] progressives.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MdnFetchEvent]: https://developer.mozilla.org/docs/Web/API/FetchEvent "FetchEvent | MDN"  
[MdnProgressiveWebApps]: https://developer.mozilla.org/docs/Web/Progressive_web_apps "Applications web progressives (P PWA) | MDN"  
[MdnServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Service Worker API | MDN"  
