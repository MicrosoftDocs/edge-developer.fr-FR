---
description: Utiliser le volet d’émulation pour tester différents profils de navigateur, tailles d’écran et résolutions, et coordonnées d’emplacement GPS
title: Émulation DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, émulation d’appareil, conception réactive, géolocalisation, résolution
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: af740472f22a8b322c03cb672a3da909ef195fac
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233035"
---
# Émulation  

> [!NOTE]
> Le nouveau Microsoft Edge est conçu à l’aide du chrome et commence à la version 75.  Pour plus d’informations, [Téléchargez le nouveau Microsoft Edge][MicrosoftNewEdge]et testez les nouveaux [outils de développement Microsoft Edge (chrome)][DevtoolsGuideChromium].  
> 
> Pour émuler différents appareils, navigateurs, tailles d’écran et résolutions dans le nouveau DevTools, accédez à la section [émuler des appareils mobiles dans Microsoft Edge \(chrome \) devtools][DevtoolsGuideChromiumDeviceMode].  

Le panneau d' **émulation** facilite les activités suivantes.    

*   Simuler divers [profils d’appareil](#device), [navigateurs](#browser-profile), tailles d' [écran et résolutions](#display)  
*   Tester différents [paramètres et coordonnées de géolocalisation](#geolocation)  

:::image type="complex" source="./media/emulation.png" alt-text="Panneau d’émulation Microsoft Edge DevTools" lightbox="./media/emulation.png":::
   Panneau d' **émulation** Microsoft Edge devtools  
:::image-end:::  

1.  Le bouton **conserver les paramètres d’émulation** vous permet d’enregistrer les modifications que vous avez effectuées à partir des paramètres d’émulation de bureau par défaut, même lorsque vous fermez et rouvrez le devtools.  

1.  Le bouton **Réinitialiser les paramètres d’émulation** rétablit les paramètres d’émulation par défaut du profil du navigateur de bureau et de la chaîne de l’agent utilisateur Microsoft Edge avec le GPS désactivé.  

1.  Lorsque l’une de ces options est modifiée par défaut, l’onglet d' **émulation** affiche une alerte d’information indiquant qu’un aspect du comportement de votre navigateur est émulé.  

## Appareil  

Faites votre choix parmi une liste prédéfinie de profils d’appareils Windows qui configurent automatiquement les autres options d’émulation ou spécifiez votre propre configuration **personnalisée** .  Revenez à la **valeur par défaut** pour réinitialiser tous les outils d’émulation.  

## Mode  

### Profil du navigateur  

Pour simuler une page en cours d’exécution sur un appareil Windows Phone, il est recommandé de changer le paramètre de **Profil du navigateur** sur **Windows Phone**.  

#### Chaîne de l’agent utilisateur  

La modification de la chaîne de l’agent utilisateur pour reproduire un autre navigateur est une bonne première étape du débogage des erreurs qui se produisent uniquement dans Microsoft Edge.  

Les scripts utilisent la chaîne de l’agent utilisateur pour détecter le navigateur utilisé.  Le script est susceptible d’être frontal, principal, principal, frontal et principal.  Même si votre code n’utilise pas la détection de navigateur, votre code peut en hériter à partir d’une bibliothèque JavaScript tierce ou d’un script côté serveur.  

Dans le cas d’une détection de navigateur, vous pouvez mettre à l’échelle les fonctionnalités de votre navigateur (ou changer \) dans votre page Web à l’aide d’hypothèses sur les fonctionnalités du navigateur. À la place, vous devez envisager de détecter les fonctionnalités de votre navigateur.  Un comportement inattendu est susceptible de se produire en raison de l’une des situations suivantes.  

*   Le code ciblé sur Windows Internet Explorer 8 s’exécute différemment dans Microsoft Edge.  
*   Une fonctionnalité prise en charge par votre navigateur est désactivée en raison d’une supposition faite par le développeur.  

Si la modification de la chaîne de l’agent utilisateur permet de résoudre le problème, la détection du navigateur est probablement coupable.  

## Affichage  

Afficher l’émulation pour afficher un aperçu de votre site sur différentes tailles et résolutions d’écran.  

*   écrans de bureau classiques  
*   écrans mobiles plus petits  
*   affichages de haute résolution plus récents  

Les émulations sont adaptées pour essayer de correspondre aux dimensions physiques des écrans émulés.  Les pixels émulés apparaissent comme comprimés ou développés. Il n’est pas recommandé d’utiliser l’émulation si vous avez besoin de tester le positionnement des éléments HTML en pixels.  L’émulation est toutefois bien adaptée aux tests de conception réactive et à l’identification de grands problèmes de positionnement d’éléments.  

### Orientation  

Choisissez le mode **paysage** ou **portrait** .  

### Résolution  

Faites votre choix parmi une liste prédéfinie de résolutions d’appareils populaires ou spécifiez votre propre configuration **personnalisée** .  Les résolutions de 80 pouces et 3820 x 2160 sont prises en charge.  

## Géolocalisation  

Si votre site Web utilise l' [API de géolocalisation][MdnGeolocationUsing] pour fournir des services de géolocalisation, les activités suivantes sont disponibles dans la commodité de votre ordinateur de bureau.  

*   Testez facilement différentes coordonnées GPS  
*   Testez facilement différents États des capteurs  

Les paramètres remplacent toutes les coordonnées GPS réelles et l’état du capteur sur les appareils qui prennent en charge la géolocalisation.  

Votre site Web doit demander l’autorisation d’un utilisateur et l’octroyer avant de l’emplacement de l’appareil.  Testez le comportement de votre site avec et sans autorisation d’emplacement du panneau **paramètres** de Microsoft Edge.  

**...** >  **Paramètres**  >  **Afficher les paramètres avancés**  >  Autorisations de site **Web**  >  **Gestion**  

:::image type="complex" source="./media/settings_manage_permissions.png" alt-text="Gérer les autorisations de site Web à partir du panneau Paramètres de Microsoft Edge" lightbox="./media/settings_manage_permissions.png":::
   Gérer les autorisations de site Web à partir du panneau **paramètres** de Microsoft Edge  
:::image-end:::  

## Raccourcis

| Action  | Raccourci  |  
|:--- |:--- |  
| Réinitialiser les paramètres d’émulation | `Ctrl`+`Shift`+`L` |  

<!-- links -->  


[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  
[DevtoolsGuideChromiumDeviceMode]: /microsoft-edge/devtools-guide-chromium/device-mode "Émuler des appareils mobiles dans Microsoft Edge DevTools | Documents Microsoft"  

[MicrosoftNewEdge]: https://www.microsoft.com/edge "Télécharger le nouveau navigateur Microsoft Edge"  

[MdnGeolocationUsing]: https://developer.mozilla.org/docs/Web/API/Geolocation/Using_geolocation "API de géolocalisation | MDN"  
