---
ms.assetid: 2ecc762c-11a5-4b16-9aed-22606c1d4994
description: Découvrez comment l’API Web notifications peut être utilisée pour envoyer des notifications aux utilisateurs en dehors du contexte du navigateur Microsoft Edge.
title: Guide de développement-API Web notifications
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/18/2017
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.openlocfilehash: da563a333491ef699925adec6f97b3c21d3e54a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565038"
---
# API Web notifications

L’API Web notifications permet d’envoyer des notifications aux utilisateurs en dehors du contexte d’une page Web dans le navigateur Microsoft Edge. Par exemple, une application de messagerie telle que Skype est illustrée dans l’action. Lorsqu’un utilisateur reçoit un nouveau message, une notification apparaît sur son bureau, lui avertissant son message. Les notifications Web sont entièrement intégrées à la plate-forme de notification et au centre de notifications dans Windows 10. 

## Création d’une notification

Le CodePen ci-dessous crée une notification Skype fictive en créant un [`Notification`](https://msdn.microsoft.com/library/mt710818) objet avec le [`title`](https://msdn.microsoft.com/library/mt710826) , [`icon`](https://msdn.microsoft.com/library/mt710814) et les [`body`](https://msdn.microsoft.com/library/mt710811) options suivantes:


<iframe height='295' scrolling='no' title='Notifications Web' src='//codepen.io/MicrosoftEdgeDocumentation/embed/RGbxWW/?height=295&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Voir les <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'> notifications Web de stylet </a> par Microsoft Edge Docs ( <a href='https://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) sur <a href='https://codepen.io'> CodePen </a> .
</iframe>

Il est vivement recommandé `icon` de spécifier une valeur pour chaque notification. Cela permet non seulement d’améliorer une notification du point de vue de l’interface utilisateur, mais également d’alerter les utilisateurs à partir desquels le message est envoyé.

Regardez la vidéo ci-dessous pour obtenir une procédure pas à pas sur la création d’une notification Web et l’affichage du comportement dans Windows 10.


> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Implementing-Web-Notifications/player]

### Propriétés de notification

Les notifications peuvent être définies avec les options suivantes:

Propriété | Description
:-------- | :----------
[body](https://msdn.microsoft.com/library/mt710811) | Le texte du corps de la notification.
[dir](https://msdn.microsoft.com/library/mt710813) | Direction du texte de la notification.
[icon](https://msdn.microsoft.com/library/mt710814) | URL de la notification utilisée comme icône.
[lang](https://msdn.microsoft.com/library/mt710815) | Langue de la notification.
[permission](https://msdn.microsoft.com/library/mt670637) | La notification actuelle s’affiche lorsque l’utilisateur a accordé l’origine actuelle.
[tag](https://msdn.microsoft.com/library/mt710825) | Balise de la notification.
[title](https://msdn.microsoft.com/library/mt710826) | Titre de la notification.

### Événements de notification

Les événements suivants sont utilisés avec l' [`Notification`](https://msdn.microsoft.com/library/mt710818) objet:

Événement | Description
:-------- | :----------
[OnClick](https://msdn.microsoft.com/library/mt712180) | Est déclenché lorsqu’un utilisateur clique sur une notification.
[aura](https://msdn.microsoft.com/library/mt712178) | Se déclenche quand une notification est fermée par l’utilisateur ou par un délai d’attente automatique.
[erreur](https://msdn.microsoft.com/library/mt712181) | Se déclenche quand une erreur se produit lors de la gestion d’une notification.
[onshow](https://msdn.microsoft.com/library/mt712182) | Se déclenche quand une notification s’affiche.

### Méthodes de notification

Les méthodes suivantes sont utilisées avec l' [`Notification`](https://msdn.microsoft.com/library/mt710818) objet:

Méthode | Description
:-------- | :----------
[close](https://msdn.microsoft.com/library/mt670636) | Ferme une notification affichée.
[requestPermission](https://msdn.microsoft.com/library/mt710824) | Demande à l’utilisateur l’autorisation d’afficher les notifications à l’origine actuelle.

## Autorisations de notification

Microsoft Edge permet aux utilisateurs de gérer les autorisations de notifications pour chaque domaine de site Web concerné. C’est à l’utilisateur de sélectionner «Oui» ou «non» lorsque le domaine lui demande d’afficher les notifications. La [`requestPermission`](https://msdn.microsoft.com/library/mt710824) méthode est utilisée pour signaler l’état d’autorisation en tant que `granted` , `denied` ou `default` . `default`La valeur indique que l’utilisateur n’a pas effectué de décision, qui est l’équivalent de `denied` .




## Référence API

[Notifications Web](https://msdn.microsoft.com/library/mt710827)

## Spécifier

[Notifications Web](https://notifications.spec.whatwg.org)
