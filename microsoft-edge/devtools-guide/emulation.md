---
description: Utiliser le volet d’émulation pour tester différents profils de navigateur, tailles d’écran et résolutions, et coordonnées d’emplacement GPS
title: Émulation DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, émulation d’appareil, conception réactive, géolocalisation, résolution
ms.custom: seodec18
ms.openlocfilehash: d66646600aeaac279acaf622527f829c69f33286
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565570"
---
# Émulation

Le panneau d' *émulation* vous permet d’effectuer les opérations suivantes:
 - Simuler divers [profils d’appareil](#device), [navigateurs](#browser-profile), tailles d' [écran et résolutions](#display)
 - Tester différents [paramètres et coordonnées de géolocalisation](#geolocation)

![Panneau d’émulation Microsoft Edge DevTools](./media/emulation.png)

1. Le bouton **conserver les paramètres d’émulation** de bureau enregistre les modifications que vous avez effectuées à partir des paramètres d’émulation de bureau par défaut, même lorsque vous fermez et rouvrez le devtools. 

2. Le bouton **Réinitialiser les paramètres d’émulation** rétablit les paramètres d’émulation de votre navigateur de *Bureau* par défaut et de la chaîne de l’agent utilisateur Microsoft Edge pour lesquels le GPS est désactivé.

3. Lorsque l’une de ces options est modifiée par défaut, l’onglet **émulation** affiche une alerte d’information indiquant que l’aspect du comportement de votre navigateur est émulé.

## Appareil

Faites votre choix parmi une liste prédéfinie de profils d’appareils Windows qui configurent automatiquement les autres options d’émulation ou spécifiez votre propre configuration *personnalisée* . Revenez à la *valeur par défaut* pour réinitialiser tous les outils d’émulation.

## Mode

### Profil du navigateur
Pour simuler une page en cours d’exécution sur un appareil Windows Phone, il est recommandé de changer le paramètre de **Profil du navigateur** sur *Windows Phone*.

#### Chaîne de l’agent utilisateur

La modification de la chaîne de l’agent utilisateur pour reproduire un autre navigateur est une bonne première étape du débogage des erreurs qui se produisent uniquement dans Microsoft Edge. 

Les scripts frontal et/ou principal peuvent parfois utiliser une chaîne d’agent utilisateur pour détecter le navigateur que vous utilisez. Même si vous n’utilisez pas la détection de navigateur dans votre propre code, vous utilisez peut-être une bibliothèque JavaScript tierce ou un script côté serveur.

Le problème lié à la détection du navigateur est qu’il est souvent utilisé pour mettre à l’échelle ou changer les fonctionnalités d’une page Web en fonction de ce que votre navigateur peut faire, au lieu de détecter ce que votre navigateur peut faire à l’aide de la détection de fonctionnalités. Cela peut entraîner un comportement inattendu, car le code ciblé sur Windows Internet Explorer 8 peut s’exécuter très différemment dans Microsoft Edge. vous pouvez également désactiver la prise en charge des fonctionnalités de votre navigateur en raison d’une supposition faite par le développeur.

Si la modification de la chaîne de l’agent utilisateur permet de résoudre le problème, la détection du navigateur est probablement coupable.

## Affichage

L’émulation d’affichage vous permet d’afficher un aperçu de votre site sur différentes tailles et résolutions d’écran: des écrans de bureau classiques aux écrans mobiles plus petits ou des écrans de haute résolution plus récents.

Les émulations sont adaptées pour essayer de correspondre aux dimensions physiques des écrans émulés. Les pixels émulés peuvent apparaître comme comprimés ou développés, et l’émulation n’est pas recommandée si vous avez besoin de tester le positionnement des éléments HTML en pixels. L’émulation est toutefois bien adaptée aux tests de conception réactive et à l’identification de grands problèmes de positionnement d’éléments.

### Orientation

Choisissez le mode *paysage* ou *portrait* .

### Résolution

Faites votre choix parmi une liste prédéfinie de résolutions d’appareils populaires ou spécifiez votre propre configuration *personnalisée* . Les résolutions de 80 pouces et 3820 x 2160 sont prises en charge.

## Géolocalisation

Si votre site utilise l' [API de géolocalisation](https://developer.mozilla.org/docs/Web/API/Geolocation/Using_geolocation) pour fournir des services de géolocalisation, vous pouvez facilement tester différentes coordonnées GPS et États de capteur à partir de la commodité de votre ordinateur de bureau. Ces paramètres remplaceront les coordonnées GPS et l’état du capteur sur les ordinateurs qui prennent en charge la géolocalisation. 

Comme pour toute utilisation de données personnelles sur le Web, vos utilisateurs doivent d’abord accorder l’autorisation de votre site à l’utilisation de leur emplacement. Vous pouvez tester le comportement de votre site avec et sans autorisation d’emplacement du panneau *paramètres* de Microsoft Edge:

**...** >  **Paramètres**  >  **Afficher les paramètres avancés**  >  Autorisations de site **Web**  >  **Gestion**

![Gérer les autorisations de site Web à partir du panneau Paramètres de Microsoft Edge](./media/settings_manage_permissions.png)

## Associés

| Action                   | Raccourci               |
|:-------------------------|:-----------------------|
| Réinitialiser les paramètres d’émulation | `CTRL` + `SHIFT` + `L` |
