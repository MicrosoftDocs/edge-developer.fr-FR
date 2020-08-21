---
ms.assetid: 2ecc762c-11a5-4b16-9aed-22606c1d4994
description: Découvrez comment l’API Web notifications peut être utilisée pour envoyer des notifications aux utilisateurs en dehors du contexte du navigateur Microsoft Edge.
title: API de notifications Web-Guide de développement
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.openlocfilehash: 24b8a7b25fb3e0f0221f6d81b105d5d0374ea423
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941801"
---
# API notifications Web  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

L’API Web notifications permet d’envoyer des notifications aux utilisateurs en dehors du contexte d’une page Web dans le navigateur Microsoft Edge.  Par exemple, une application de messagerie telle que Skype est illustrée dans l’action.  Lorsqu’un utilisateur reçoit un nouveau message, une notification apparaît sur son bureau, lui avertissant son message.  Les notifications Web sont entièrement intégrées à la plate-forme de notification et au centre de notifications dans Windows 10.  

## Création d’une notification  

Le CodePen ci-dessous crée une notification Skype factice en créant un objet [notification](https://msdn.microsoft.com/library/mt710818) avec les options [titre](https://msdn.microsoft.com/library/mt710826), [icône](https://msdn.microsoft.com/library/mt710814)et [corps](https://msdn.microsoft.com/library/mt710811) définies:  

<iframe height='295' scrolling='no' title='Notifications Web' src='//codepen.io/MicrosoftEdgeDocumentation/embed/RGbxWW/?height=295&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Voir les <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'> notifications Web de stylet </a> par Microsoft Edge Docs ( <a href='https://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) sur <a href='https://codepen.io'> CodePen </a> .</iframe>  

Il est vivement recommandé de spécifier une **icône** pour chaque notification.  Cela permet non seulement d’améliorer une notification du point de vue de l’interface utilisateur, mais également d’alerter les utilisateurs à partir desquels le message est envoyé.  

Regardez la vidéo ci-dessous pour obtenir une procédure pas à pas sur la création d’une notification Web et l’affichage du comportement dans Windows 10.  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Implementing-Web-Notifications/player]  

### Propriétés de notification  

Les notifications peuvent être définies avec les propriétés suivantes:  

:::row:::
   :::column span="1":::
      [body](https://developer.mozilla.org/docs/Web/API/Notification/body)  
   :::column-end:::
   :::column span="2":::
      Le texte du corps de la notification.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [dir](https://developer.mozilla.org/docs/Web/API/Notification/dir)  
   :::column-end:::
   :::column span="2":::
      Direction du texte de la notification.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [icon](https://developer.mozilla.org/docs/Web/API/Notification/icon)  
   :::column-end:::
   :::column span="2":::
      URL de la notification utilisée comme icône.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [lang](https://developer.mozilla.org/docs/Web/API/Notification/lang)  
   :::column-end:::
   :::column span="2":::
      Langue de la notification.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [permission](https://developer.mozilla.org/docs/Web/API/Notification/permission)  
   :::column-end:::
   :::column span="2":::
      La notification actuelle s’affiche lorsque l’utilisateur a accordé l’origine actuelle.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [tag](https://developer.mozilla.org/docs/Web/API/Notification/tag)  
   :::column-end:::
   :::column span="2":::
      Balise de la notification.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [title](https://developer.mozilla.org/docs/Web/API/Notification/title)  
   :::column-end:::
   :::column span="2":::
      Titre de la notification.  
   :::column-end:::
:::row-end:::  

### Événements de notification  

Les événements suivants sont utilisés avec l’objet [notification](https://developer.mozilla.org/docs/Web/API/Notification) :  

:::row:::
   :::column span="1":::
      [OnClick](https://developer.mozilla.org/docs/Web/API/Element/click_event)  
   :::column-end:::
   :::column span="2":::
      Est déclenché lorsqu’un utilisateur clique sur une notification.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [aura](https://developer.mozilla.org/docs/Archive/Mozilla/XUL/Events/close_event)  
   :::column-end:::
   :::column span="2":::
      Se déclenche quand une notification est fermée par l’utilisateur ou par un délai d’attente automatique.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [erreur](https://developer.mozilla.org/docs/Web/API/Element/error_event)  
   :::column-end:::
   :::column span="2":::
      Se déclenche quand une erreur se produit lors de la gestion d’une notification.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [onshow](https://developer.mozilla.org/docs/Web/API/Element/show_event)  
   :::column-end:::
   :::column span="2":::
      Se déclenche quand une notification s’affiche.  
   :::column-end:::
:::row-end:::  

### Méthodes de notification  

Les méthodes suivantes sont utilisées avec l’objet [notification](https://developer.mozilla.org/docs/Web/API/Notification) :  

:::row:::
   :::column span="1":::
      [close](https://developer.mozilla.org/docs/Web/API/Notification/close)  
   :::column-end:::
   :::column span="2":::
      Ferme une notification affichée.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [requestPermission](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission)  
   :::column-end:::
   :::column span="2":::
      Demande à l’utilisateur l’autorisation d’afficher les notifications à l’origine actuelle.  
   :::column-end:::
:::row-end:::  

## Autorisations de notification  

Microsoft Edge permet aux utilisateurs de gérer les autorisations de notifications pour chaque domaine de site Web concerné.  C’est à l’utilisateur de sélectionner **Yes** ou **no** lorsque le domaine vous demande de lui permettre d’afficher les notifications.  La méthode [requestPermission](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission) est utilisée pour signaler l’état d’autorisation en tant que `granted` , `denied` , ou `default` .  `default`La valeur indique que l’utilisateur n’a pas effectué de décision, qui est l’équivalent de `denied` .  

## Référence API  

[Notifications Web](https://developer.mozilla.org/docs/Web/API/Notifications_API)  

## Spécifier  

[Notifications Web](https://notifications.spec.whatwg.org)  
