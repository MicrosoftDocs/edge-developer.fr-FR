---
ms.assetid: 2ecc762c-11a5-4b16-9aed-22606c1d4994
description: Découvrez comment l’API Web notifications peut être utilisée pour envoyer des notifications aux utilisateurs en dehors du contexte du navigateur Microsoft Edge.
title: API de notifications Web-Guide de développement
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2be201a790c6fca1526c8b6eb13e4203e8e53206
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233270"
---
# <span data-ttu-id="2cb12-104">API notifications Web</span><span class="sxs-lookup"><span data-stu-id="2cb12-104">Web Notifications API</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="2cb12-105">L’API Web notifications permet d’envoyer des notifications aux utilisateurs en dehors du contexte d’une page Web dans le navigateur Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2cb12-105">The Web Notifications API allows websites to send users notifications outside the context of a webpage within the Microsoft Edge browser.</span></span>  <span data-ttu-id="2cb12-106">Par exemple, une application de messagerie telle que Skype est illustrée dans l’action.</span><span class="sxs-lookup"><span data-stu-id="2cb12-106">An example of this feature in action would be with a messaging application like Skype.</span></span>  <span data-ttu-id="2cb12-107">Lorsqu’un utilisateur reçoit un nouveau message, une notification apparaît sur son bureau, lui avertissant son message.</span><span class="sxs-lookup"><span data-stu-id="2cb12-107">When a user would receive a new message, a notification would appear on their desktop, alerting them of the message.</span></span>  <span data-ttu-id="2cb12-108">Les notifications Web sont entièrement intégrées à la plate-forme de notification et au centre de notifications dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2cb12-108">Web Notifications are fully integrated with the Notification Platform and the Action Center within Windows 10.</span></span>  

## <span data-ttu-id="2cb12-109">Création d’une notification</span><span class="sxs-lookup"><span data-stu-id="2cb12-109">Creating a notification</span></span>  

<span data-ttu-id="2cb12-110">Le CodePen ci-dessous crée une notification Skype factice en créant un objet [notification](https://msdn.microsoft.com/library/mt710818) avec les options [titre](https://msdn.microsoft.com/library/mt710826), [icône](https://msdn.microsoft.com/library/mt710814)et [corps](https://msdn.microsoft.com/library/mt710811) définies:</span><span class="sxs-lookup"><span data-stu-id="2cb12-110">The CodePen below creates a mock Skype notification by making a [Notification](https://msdn.microsoft.com/library/mt710818) object with the [title](https://msdn.microsoft.com/library/mt710826), [icon](https://msdn.microsoft.com/library/mt710814), and [body](https://msdn.microsoft.com/library/mt710811) options set:</span></span>  

<iframe height='295' scrolling='no' title='<span data-ttu-id="2cb12-111">Notifications Web</span><span class="sxs-lookup"><span data-stu-id="2cb12-111">Web notifications</span></span>' src='//codepen.io/MicrosoftEdgeDocumentation/embed/RGbxWW/?height=295&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'><span data-ttu-id="2cb12-112">Voir les <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'> notifications Web de stylet </a> par Microsoft Edge Docs ( <a href='https://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) sur <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="2cb12-112">See the Pen <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'>Web notifications</a> by Microsoft Edge Docs (<a href='https://codepen.io/MicrosoftEdgeDocumentation'>@MicrosoftEdgeDocumentation</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

<span data-ttu-id="2cb12-113">Il est vivement recommandé de spécifier une **icône** pour chaque notification.</span><span class="sxs-lookup"><span data-stu-id="2cb12-113">It is strongly recommended that an **icon** be specified for each notification.</span></span>  <span data-ttu-id="2cb12-114">Cela permet non seulement d’améliorer une notification du point de vue de l’interface utilisateur, mais également d’alerter les utilisateurs à partir desquels le message est envoyé.</span><span class="sxs-lookup"><span data-stu-id="2cb12-114">This not only improves a notification from a UI point of view, but also helps alert users of where the notification is being sent from.</span></span>  

<span data-ttu-id="2cb12-115">Regardez la vidéo ci-dessous pour obtenir une procédure pas à pas sur la création d’une notification Web et l’affichage du comportement dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2cb12-115">Watch the video below for a walkthrough on creating a web notification and to see it's behavior within Windows 10!</span></span>  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Implementing-Web-Notifications/player]  

### <span data-ttu-id="2cb12-116">Propriétés de notification</span><span class="sxs-lookup"><span data-stu-id="2cb12-116">Notification properties</span></span>  

<span data-ttu-id="2cb12-117">Les notifications peuvent être définies avec les propriétés suivantes:</span><span class="sxs-lookup"><span data-stu-id="2cb12-117">Notifications can be set with the following properties:</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="2cb12-118">body</span><span class="sxs-lookup"><span data-stu-id="2cb12-118">body</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/body)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2cb12-119">Le texte du corps de la notification.</span><span class="sxs-lookup"><span data-stu-id="2cb12-119">The body text of the notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="2cb12-120">dir</span><span class="sxs-lookup"><span data-stu-id="2cb12-120">dir</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/dir)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2cb12-121">Direction du texte de la notification.</span><span class="sxs-lookup"><span data-stu-id="2cb12-121">The direction of the notification's text.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="2cb12-122">icon</span><span class="sxs-lookup"><span data-stu-id="2cb12-122">icon</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/icon)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2cb12-123">URL de la notification utilisée comme icône.</span><span class="sxs-lookup"><span data-stu-id="2cb12-123">The notification's URL that is used for its icon.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="2cb12-124">lang</span><span class="sxs-lookup"><span data-stu-id="2cb12-124">lang</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/lang)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2cb12-125">Langue de la notification.</span><span class="sxs-lookup"><span data-stu-id="2cb12-125">The language of the notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="2cb12-126">permission</span><span class="sxs-lookup"><span data-stu-id="2cb12-126">permission</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/permission)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2cb12-127">La notification actuelle s’affiche lorsque l’utilisateur a accordé l’origine actuelle.</span><span class="sxs-lookup"><span data-stu-id="2cb12-127">The current notification display permission the user has granted for the current origin.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="2cb12-128">tag</span><span class="sxs-lookup"><span data-stu-id="2cb12-128">tag</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/tag)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2cb12-129">Balise de la notification.</span><span class="sxs-lookup"><span data-stu-id="2cb12-129">The tag of the notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="2cb12-130">title</span><span class="sxs-lookup"><span data-stu-id="2cb12-130">title</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/title)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2cb12-131">Titre de la notification.</span><span class="sxs-lookup"><span data-stu-id="2cb12-131">The title of the notification.</span></span>  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="2cb12-132">Événements de notification</span><span class="sxs-lookup"><span data-stu-id="2cb12-132">Notification events</span></span>  

<span data-ttu-id="2cb12-133">Les événements suivants sont utilisés avec l’objet [notification](https://developer.mozilla.org/docs/Web/API/Notification) :</span><span class="sxs-lookup"><span data-stu-id="2cb12-133">The following events are used with the [Notification](https://developer.mozilla.org/docs/Web/API/Notification) object:</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="2cb12-134">OnClick</span><span class="sxs-lookup"><span data-stu-id="2cb12-134">onclick</span></span>](https://developer.mozilla.org/docs/Web/API/Element/click_event)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2cb12-135">Est déclenché lorsqu’un utilisateur clique sur une notification.</span><span class="sxs-lookup"><span data-stu-id="2cb12-135">Fires when a notification is clicked by the user.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="2cb12-136">aura</span><span class="sxs-lookup"><span data-stu-id="2cb12-136">onclose</span></span>](https://developer.mozilla.org/docs/Archive/Mozilla/XUL/Events/close_event)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2cb12-137">Se déclenche quand une notification est fermée par l’utilisateur ou par un délai d’attente automatique.</span><span class="sxs-lookup"><span data-stu-id="2cb12-137">Fires when a notification is closed by the user or an auto timeout.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="2cb12-138">erreur</span><span class="sxs-lookup"><span data-stu-id="2cb12-138">onerror</span></span>](https://developer.mozilla.org/docs/Web/API/Element/error_event)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2cb12-139">Se déclenche quand une erreur se produit lors de la gestion d’une notification.</span><span class="sxs-lookup"><span data-stu-id="2cb12-139">Fires when an error occurs while handling a notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="2cb12-140">onshow</span><span class="sxs-lookup"><span data-stu-id="2cb12-140">onshow</span></span>](https://developer.mozilla.org/docs/Web/API/Element/show_event)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2cb12-141">Se déclenche quand une notification s’affiche.</span><span class="sxs-lookup"><span data-stu-id="2cb12-141">Fires when a notification is displayed.</span></span>  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="2cb12-142">Méthodes de notification</span><span class="sxs-lookup"><span data-stu-id="2cb12-142">Notification methods</span></span>  

<span data-ttu-id="2cb12-143">Les méthodes suivantes sont utilisées avec l’objet [notification](https://developer.mozilla.org/docs/Web/API/Notification) :</span><span class="sxs-lookup"><span data-stu-id="2cb12-143">The following methods are used with the [Notification](https://developer.mozilla.org/docs/Web/API/Notification) object:</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="2cb12-144">close</span><span class="sxs-lookup"><span data-stu-id="2cb12-144">close</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/close)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2cb12-145">Ferme une notification affichée.</span><span class="sxs-lookup"><span data-stu-id="2cb12-145">Closes a displayed notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="2cb12-146">requestPermission</span><span class="sxs-lookup"><span data-stu-id="2cb12-146">requestPermission</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2cb12-147">Demande à l’utilisateur l’autorisation d’afficher les notifications à l’origine actuelle.</span><span class="sxs-lookup"><span data-stu-id="2cb12-147">Requests permission from the user to allow notifications to be displayed by the current origin.</span></span>  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="2cb12-148">Autorisations de notification</span><span class="sxs-lookup"><span data-stu-id="2cb12-148">Notification permissions</span></span>  

<span data-ttu-id="2cb12-149">Microsoft Edge permet aux utilisateurs de gérer les autorisations de notifications pour chaque domaine de site Web concerné.</span><span class="sxs-lookup"><span data-stu-id="2cb12-149">Microsoft Edge allows users to manage notifications permissions for each specific website domain.</span></span>  <span data-ttu-id="2cb12-150">C’est à l’utilisateur de sélectionner **Yes** ou **no** lorsque le domaine vous demande de lui permettre d’afficher les notifications.</span><span class="sxs-lookup"><span data-stu-id="2cb12-150">It's up to the user to either select **Yes** or **No** when asked by the domain to let it show notifications.</span></span>  <span data-ttu-id="2cb12-151">La méthode [requestPermission](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission) est utilisée pour signaler l’état d’autorisation en tant que `granted` , `denied` , ou `default` .</span><span class="sxs-lookup"><span data-stu-id="2cb12-151">The [requestPermission](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission) method is used to signal the permission state as either `granted`, `denied`, or `default`.</span></span>  <span data-ttu-id="2cb12-152">`default`La valeur indique que l’utilisateur n’a pas effectué de décision, qui est l’équivalent de `denied` .</span><span class="sxs-lookup"><span data-stu-id="2cb12-152">A value of `default` indicates that the user hasn't made a decision, which is seen as the equivalent of `denied`.</span></span>  

## <span data-ttu-id="2cb12-153">Informations de référence sur les API</span><span class="sxs-lookup"><span data-stu-id="2cb12-153">API reference</span></span>  

[<span data-ttu-id="2cb12-154">Notifications Web</span><span class="sxs-lookup"><span data-stu-id="2cb12-154">Web Notifications</span></span>](https://developer.mozilla.org/docs/Web/API/Notifications_API)  

## <span data-ttu-id="2cb12-155">Spécifier</span><span class="sxs-lookup"><span data-stu-id="2cb12-155">Specification</span></span>  

[<span data-ttu-id="2cb12-156">Notifications Web</span><span class="sxs-lookup"><span data-stu-id="2cb12-156">Web Notifications</span></span>](https://notifications.spec.whatwg.org)  
