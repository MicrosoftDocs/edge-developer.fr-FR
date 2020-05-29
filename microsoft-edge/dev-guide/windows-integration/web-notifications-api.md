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
# <span data-ttu-id="b045f-104">API Web notifications</span><span class="sxs-lookup"><span data-stu-id="b045f-104">Web Notifications API</span></span>

<span data-ttu-id="b045f-105">L’API Web notifications permet d’envoyer des notifications aux utilisateurs en dehors du contexte d’une page Web dans le navigateur Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b045f-105">The Web Notifications API allows websites to send users notifications outside the context of a webpage within the Microsoft Edge browser.</span></span> <span data-ttu-id="b045f-106">Par exemple, une application de messagerie telle que Skype est illustrée dans l’action.</span><span class="sxs-lookup"><span data-stu-id="b045f-106">An example of this feature in action would be with a messaging application like Skype.</span></span> <span data-ttu-id="b045f-107">Lorsqu’un utilisateur reçoit un nouveau message, une notification apparaît sur son bureau, lui avertissant son message.</span><span class="sxs-lookup"><span data-stu-id="b045f-107">When a user would receive a new message, a notification would appear on their desktop, alerting them of the message.</span></span> <span data-ttu-id="b045f-108">Les notifications Web sont entièrement intégrées à la plate-forme de notification et au centre de notifications dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="b045f-108">Web Notifications are fully integrated with the Notification Platform and the Action Center within Windows 10.</span></span> 

## <span data-ttu-id="b045f-109">Création d’une notification</span><span class="sxs-lookup"><span data-stu-id="b045f-109">Creating a notification</span></span>

<span data-ttu-id="b045f-110">Le CodePen ci-dessous crée une notification Skype fictive en créant un [`Notification`](https://msdn.microsoft.com/library/mt710818) objet avec le [`title`](https://msdn.microsoft.com/library/mt710826) , [`icon`](https://msdn.microsoft.com/library/mt710814) et les [`body`](https://msdn.microsoft.com/library/mt710811) options suivantes:</span><span class="sxs-lookup"><span data-stu-id="b045f-110">The CodePen below creates a mock Skype notification by making a [`Notification`](https://msdn.microsoft.com/library/mt710818) object with the [`title`](https://msdn.microsoft.com/library/mt710826), [`icon`](https://msdn.microsoft.com/library/mt710814), and [`body`](https://msdn.microsoft.com/library/mt710811) options set:</span></span>


<iframe height='295' scrolling='no' title='<span data-ttu-id="b045f-111">Notifications Web</span><span class="sxs-lookup"><span data-stu-id="b045f-111">Web notifications</span></span>' src='//codepen.io/MicrosoftEdgeDocumentation/embed/RGbxWW/?height=295&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'><span data-ttu-id="b045f-112">Voir les <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'> notifications Web de stylet </a> par Microsoft Edge Docs ( <a href='https://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) sur <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="b045f-112">See the Pen <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'>Web notifications</a> by Microsoft Edge Docs (<a href='https://codepen.io/MicrosoftEdgeDocumentation'>@MicrosoftEdgeDocumentation</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span>
</iframe>

<span data-ttu-id="b045f-113">Il est vivement recommandé `icon` de spécifier une valeur pour chaque notification.</span><span class="sxs-lookup"><span data-stu-id="b045f-113">It is strongly recommended that an `icon` be specified for each notification.</span></span> <span data-ttu-id="b045f-114">Cela permet non seulement d’améliorer une notification du point de vue de l’interface utilisateur, mais également d’alerter les utilisateurs à partir desquels le message est envoyé.</span><span class="sxs-lookup"><span data-stu-id="b045f-114">This not only improves a notification from a UI point of view, but also helps alert users of where the notification is being sent from.</span></span>

<span data-ttu-id="b045f-115">Regardez la vidéo ci-dessous pour obtenir une procédure pas à pas sur la création d’une notification Web et l’affichage du comportement dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="b045f-115">Watch the video below for a walkthrough on creating a web notification and to see it's behavior within Windows 10!</span></span>


> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Implementing-Web-Notifications/player]

### <span data-ttu-id="b045f-116">Propriétés de notification</span><span class="sxs-lookup"><span data-stu-id="b045f-116">Notification properties</span></span>

<span data-ttu-id="b045f-117">Les notifications peuvent être définies avec les options suivantes:</span><span class="sxs-lookup"><span data-stu-id="b045f-117">Notifications can be set with the following options:</span></span>

<span data-ttu-id="b045f-118">Propriété</span><span class="sxs-lookup"><span data-stu-id="b045f-118">Property</span></span> | <span data-ttu-id="b045f-119">Description</span><span class="sxs-lookup"><span data-stu-id="b045f-119">Description</span></span>
:-------- | :----------
[<span data-ttu-id="b045f-120">body</span><span class="sxs-lookup"><span data-stu-id="b045f-120">body</span></span>](https://msdn.microsoft.com/library/mt710811) | <span data-ttu-id="b045f-121">Le texte du corps de la notification.</span><span class="sxs-lookup"><span data-stu-id="b045f-121">The body text of the notification.</span></span>
[<span data-ttu-id="b045f-122">dir</span><span class="sxs-lookup"><span data-stu-id="b045f-122">dir</span></span>](https://msdn.microsoft.com/library/mt710813) | <span data-ttu-id="b045f-123">Direction du texte de la notification.</span><span class="sxs-lookup"><span data-stu-id="b045f-123">The direction of the notification's text.</span></span>
[<span data-ttu-id="b045f-124">icon</span><span class="sxs-lookup"><span data-stu-id="b045f-124">icon</span></span>](https://msdn.microsoft.com/library/mt710814) | <span data-ttu-id="b045f-125">URL de la notification utilisée comme icône.</span><span class="sxs-lookup"><span data-stu-id="b045f-125">The notification's URL that is used for its icon.</span></span>
[<span data-ttu-id="b045f-126">lang</span><span class="sxs-lookup"><span data-stu-id="b045f-126">lang</span></span>](https://msdn.microsoft.com/library/mt710815) | <span data-ttu-id="b045f-127">Langue de la notification.</span><span class="sxs-lookup"><span data-stu-id="b045f-127">The language of the notification.</span></span>
[<span data-ttu-id="b045f-128">permission</span><span class="sxs-lookup"><span data-stu-id="b045f-128">permission</span></span>](https://msdn.microsoft.com/library/mt670637) | <span data-ttu-id="b045f-129">La notification actuelle s’affiche lorsque l’utilisateur a accordé l’origine actuelle.</span><span class="sxs-lookup"><span data-stu-id="b045f-129">The current notification display permission the user has granted for the current origin.</span></span>
[<span data-ttu-id="b045f-130">tag</span><span class="sxs-lookup"><span data-stu-id="b045f-130">tag</span></span>](https://msdn.microsoft.com/library/mt710825) | <span data-ttu-id="b045f-131">Balise de la notification.</span><span class="sxs-lookup"><span data-stu-id="b045f-131">The tag of the notification.</span></span>
[<span data-ttu-id="b045f-132">title</span><span class="sxs-lookup"><span data-stu-id="b045f-132">title</span></span>](https://msdn.microsoft.com/library/mt710826) | <span data-ttu-id="b045f-133">Titre de la notification.</span><span class="sxs-lookup"><span data-stu-id="b045f-133">The title of the notification.</span></span>

### <span data-ttu-id="b045f-134">Événements de notification</span><span class="sxs-lookup"><span data-stu-id="b045f-134">Notification events</span></span>

<span data-ttu-id="b045f-135">Les événements suivants sont utilisés avec l' [`Notification`](https://msdn.microsoft.com/library/mt710818) objet:</span><span class="sxs-lookup"><span data-stu-id="b045f-135">The following events are used with the [`Notification`](https://msdn.microsoft.com/library/mt710818) object:</span></span>

<span data-ttu-id="b045f-136">Événement</span><span class="sxs-lookup"><span data-stu-id="b045f-136">Event</span></span> | <span data-ttu-id="b045f-137">Description</span><span class="sxs-lookup"><span data-stu-id="b045f-137">Description</span></span>
:-------- | :----------
[<span data-ttu-id="b045f-138">OnClick</span><span class="sxs-lookup"><span data-stu-id="b045f-138">onclick</span></span>](https://msdn.microsoft.com/library/mt712180) | <span data-ttu-id="b045f-139">Est déclenché lorsqu’un utilisateur clique sur une notification.</span><span class="sxs-lookup"><span data-stu-id="b045f-139">Fires when a notification is clicked by the user.</span></span>
[<span data-ttu-id="b045f-140">aura</span><span class="sxs-lookup"><span data-stu-id="b045f-140">onclose</span></span>](https://msdn.microsoft.com/library/mt712178) | <span data-ttu-id="b045f-141">Se déclenche quand une notification est fermée par l’utilisateur ou par un délai d’attente automatique.</span><span class="sxs-lookup"><span data-stu-id="b045f-141">Fires when a notification is closed by the user or an auto timeout.</span></span>
[<span data-ttu-id="b045f-142">erreur</span><span class="sxs-lookup"><span data-stu-id="b045f-142">onerror</span></span>](https://msdn.microsoft.com/library/mt712181) | <span data-ttu-id="b045f-143">Se déclenche quand une erreur se produit lors de la gestion d’une notification.</span><span class="sxs-lookup"><span data-stu-id="b045f-143">Fires when an error occurs while handling a notification.</span></span>
[<span data-ttu-id="b045f-144">onshow</span><span class="sxs-lookup"><span data-stu-id="b045f-144">onshow</span></span>](https://msdn.microsoft.com/library/mt712182) | <span data-ttu-id="b045f-145">Se déclenche quand une notification s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b045f-145">Fires when a notification is displayed.</span></span>

### <span data-ttu-id="b045f-146">Méthodes de notification</span><span class="sxs-lookup"><span data-stu-id="b045f-146">Notification methods</span></span>

<span data-ttu-id="b045f-147">Les méthodes suivantes sont utilisées avec l' [`Notification`](https://msdn.microsoft.com/library/mt710818) objet:</span><span class="sxs-lookup"><span data-stu-id="b045f-147">The following methods are used with the [`Notification`](https://msdn.microsoft.com/library/mt710818) object:</span></span>

<span data-ttu-id="b045f-148">Méthode</span><span class="sxs-lookup"><span data-stu-id="b045f-148">Method</span></span> | <span data-ttu-id="b045f-149">Description</span><span class="sxs-lookup"><span data-stu-id="b045f-149">Description</span></span>
:-------- | :----------
[<span data-ttu-id="b045f-150">close</span><span class="sxs-lookup"><span data-stu-id="b045f-150">close</span></span>](https://msdn.microsoft.com/library/mt670636) | <span data-ttu-id="b045f-151">Ferme une notification affichée.</span><span class="sxs-lookup"><span data-stu-id="b045f-151">Closes a displayed notification.</span></span>
[<span data-ttu-id="b045f-152">requestPermission</span><span class="sxs-lookup"><span data-stu-id="b045f-152">requestPermission</span></span>](https://msdn.microsoft.com/library/mt710824) | <span data-ttu-id="b045f-153">Demande à l’utilisateur l’autorisation d’afficher les notifications à l’origine actuelle.</span><span class="sxs-lookup"><span data-stu-id="b045f-153">Requests permission from the user to allow notifications to be displayed by the current origin.</span></span>

## <span data-ttu-id="b045f-154">Autorisations de notification</span><span class="sxs-lookup"><span data-stu-id="b045f-154">Notification permissions</span></span>

<span data-ttu-id="b045f-155">Microsoft Edge permet aux utilisateurs de gérer les autorisations de notifications pour chaque domaine de site Web concerné.</span><span class="sxs-lookup"><span data-stu-id="b045f-155">Microsoft Edge allows users to manage notifications permissions for each specific website domain.</span></span> <span data-ttu-id="b045f-156">C’est à l’utilisateur de sélectionner «Oui» ou «non» lorsque le domaine lui demande d’afficher les notifications.</span><span class="sxs-lookup"><span data-stu-id="b045f-156">It's up to the user to either select "Yes" or "No" when asked by the domain to let it show notifications.</span></span> <span data-ttu-id="b045f-157">La [`requestPermission`](https://msdn.microsoft.com/library/mt710824) méthode est utilisée pour signaler l’état d’autorisation en tant que `granted` , `denied` ou `default` .</span><span class="sxs-lookup"><span data-stu-id="b045f-157">The [`requestPermission`](https://msdn.microsoft.com/library/mt710824) method is used to signal the permission state as either `granted`, `denied`, or `default`.</span></span> <span data-ttu-id="b045f-158">`default`La valeur indique que l’utilisateur n’a pas effectué de décision, qui est l’équivalent de `denied` .</span><span class="sxs-lookup"><span data-stu-id="b045f-158">A value of `default` indicates that the user hasn't made a decision, which is seen as the equivalent of `denied`.</span></span>




## <span data-ttu-id="b045f-159">Référence API</span><span class="sxs-lookup"><span data-stu-id="b045f-159">API reference</span></span>

[<span data-ttu-id="b045f-160">Notifications Web</span><span class="sxs-lookup"><span data-stu-id="b045f-160">Web Notifications</span></span>](https://msdn.microsoft.com/library/mt710827)

## <span data-ttu-id="b045f-161">Spécifier</span><span class="sxs-lookup"><span data-stu-id="b045f-161">Specification</span></span>

[<span data-ttu-id="b045f-162">Notifications Web</span><span class="sxs-lookup"><span data-stu-id="b045f-162">Web Notifications</span></span>](https://notifications.spec.whatwg.org)
