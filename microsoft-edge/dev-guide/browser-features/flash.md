---
description: Offrir une interface utilisateur transparente sur les sites nécessitant Adobe Flash.
title: Guide du développement-Flash
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, Flash
ms.openlocfilehash: b3e2efe142142b7cdf233acfc4e915cd320b556d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10564700"
---
# Flash

Adobe Flash est une partie intégrante du Web pour les décennies, permettant de réaliser des animations et du contenu enrichi dans les navigateurs depuis le lancement de HTML5. Dans les navigateurs modernes, les normes Web pionniers de Microsoft, d’Adobe, de Google, d’Apple, de Mozilla et de nombreux autres personnes permettent désormais aux sites de dépasser les expériences sans flash et de performances et de sécurité améliorées. Si vous collaborez avec d’autres fournisseurs de navigateur et avec Adobe, nous encourageons vivement les développeurs à migrer vers des normes HTML5, notamment les [extensions multimédias chiffrées](https://developer.microsoft.com/microsoft-edge/platform/status/encryptedmediaextensions), les [extensions de sources multimédia](https://developer.microsoft.com/microsoft-edge/platform/status/mediasourceextensions), la [zone de dessin](https://developer.microsoft.com/microsoft-edge/platform/status/canvas), le [son Web](https://developer.microsoft.com/microsoft-edge/platform/status/webaudioapi)et la [communication en temps réel](https://developer.microsoft.com/microsoft-edge/platform/status/webrtcobjectrtcapi).

Avec la version 2018 de Windows 10, Microsoft Edge est en mesure de continuer l’effort de désapprobation du flash que nous avons [couvert](https://blogs.windows.com/msedgedev/2017/07/25/flash-on-windows-timeline/#9mCF959eQEK0poo5.97) dans le cadre de la [fin de la prise en charge d’Adobe](https://theblog.adobe.com/adobe-flash-update/) après 2021. Dans les 2018 de la version d’octobre, les utilisateurs doivent explicitement autoriser l’exécution de flash sur un site pendant la durée de vie de l’onglet. L’option permanent toujours autoriser ne sera plus disponible et les utilisateurs ne seront pas en mesure de gérer les autorisations Flash par site qui englobent les sessions par onglets.

Lorsque vous migrez vers des normes HTML5, il existe quelques opérations simples que vous pouvez effectuer pour vous assurer que vos utilisateurs ont toujours une connaissance positive de votre site Web avec Microsoft Edge dans Windows 10 Creators Update. 

Si flash est utilisé dans la page, mais que l’utilisateur ne l’a pas activé, Microsoft Edge affichera en principe une icône de pièce de puzzle dans la barre d’adresse, comme le montre [ce blog](https://blogs.windows.com/msedgedev/2016/12/14/edge-flash-click-run/#41svu6EMwKIAaigx.97). Si vous ajoutez dynamiquement le contrôle de mémoire après le chargement de la page, il est possible que cette icône de pièce de puzzle ne s’affiche pas, il est préférable de vérifier la présence de Flash et de fournir un lien comme décrit ci-dessous.

Pour vous assurer que tous les utilisateurs disposent d’une bonne interface, continuez à tester la présence de Flash à l’aide de votre mécanisme standard. Si Microsoft Edge signale qu’il n’est pas disponible, présentez le [lien de téléchargement Flash](http://get.adobe.com/flashplayer) et l' [image de téléchargement Flash](http://www.adobe.com/legal/permissions/icons-web-logos.html#flashplayer) à l’utilisateur. Lorsque l’utilisateur clique sur le lien, Microsoft Edge (ainsi que d’autres navigateurs) présente les invites nécessaires à l’activation de Flash Player pour le site. Le lien doit apparaître sur le domaine principal sur lequel vous souhaitez activer le flash. Cela ne fonctionne pas si vous redirigez les utilisateurs vers des pages d’autres domaines.  [Voici une démonstration](https://microsoftedge.github.io/MicrosoftEdge-Documentation/flashclicktorun/) de l’interface suggérée et de l' [exemple de code](https://github.com/MicrosoftEdge/MicrosoftEdge-Documentation/tree/master/docs/flashclicktorun)correspondant.
