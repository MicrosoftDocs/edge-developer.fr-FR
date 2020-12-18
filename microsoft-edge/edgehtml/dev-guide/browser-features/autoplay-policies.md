---
description: Garantir le fonctionnement du contenu multimédia sur votre site
title: Stratégies de lecture automatique-Guide de développement
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: bordure, média, vidéo, audio, lecture automatique
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 85b91a8b87d73d6fccc6eac2aa64513f283d7f21
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233084"
---
# Stratégies de lecture automatique  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Microsoft Edge offre aux utilisateurs la possibilité de personnaliser leurs préférences de navigation sur les sites Web qui entourent le son par lecture automatique afin de réduire le nombre de distractions sur le Web et de économiser la bande passante.  Par ailleurs, Microsoft Edge supprime automatiquement la lecture automatique de contenus multimédias dans les onglets d’arrière-plan.  

Les utilisateurs peuvent personnaliser le comportement du contenu multimédia avec les contrôles de lecture automatique [globaux](#global-media-autoplay-settings) et [par site](#per-site-media-autoplay-settings) , qui fournissent les options suivantes:  

*   `Allow`  Par défaut, il continue de lire les vidéos lorsqu’un onglet est d’abord affiché au premier plan, en fonction du site discrétionnaire.  

*   `Limit`  Restreint la lecture automatique pour ne fonctionner que lorsque les vidéos sont en mode muet, afin que les utilisateurs ne soient jamais surpris par le son.  Lorsque l’utilisateur clique n’importe où sur la page, la lecture automatique est réactivée et continue d’être autorisée dans ce domaine sous cet onglet.  

*   `Block`  Interdisez sautoplay sur tous les sites tant que les utilisateurs n’interagissent pas directement avec le contenu multimédia.  

## Paramètres généraux de lecture multimédias  

Les utilisateurs peuvent contrôler le comportement de lecture automatique par défaut pour tous les sites sous **Paramètres avancés**de  >  **lecture automatique de médias**.  

:::image type="complex" source="../media/autoplay_global.png" alt-text="Paramètres généraux de lecture multimédias" lightbox="../media/autoplay_global.png":::
   Paramètres généraux de lecture multimédias  
:::image-end:::  

## Paramètres de lecture automatique de média par site  

Les utilisateurs peuvent contrôler le comportement de la lecture automatique sur une base par site sous la section **autorisations de site Web** du volet informations sur le site Web.  Ce paramètre est disponible en cliquant sur l’icône d’information ou sur l’icône de verrouillage située sur le côté gauche de la barre d’adresse, puis en cliquant sur **paramètres de lecture automatique de média** pour commencer.  

Les paramètres par site remplacent le paramètre global.  Par exemple, si le paramètre global est défini pour un utilisateur et qu’il `Allow` change un paramètre par site `Block` , la lecture automatique est bloquée pour ce site.  

:::image type="complex" source="../media/autoplay_per-site.png" alt-text="Paramètres de lecture automatique de média par site" lightbox="../media/autoplay_per-site.png":::
   Paramètres de lecture automatique de média par site  
:::image-end:::  

## Meilleures pratiques pour les développeurs Web  

Pour garantir une bonne utilisation de l’utilisateur avec le contenu multimédia hébergé sur votre site, procédez comme suit:  

*   Supposez que l’utilisation d’un élément multimédia nécessite un mouvement utilisateur pour démarrer la lecture \ (car les utilisateurs peuvent bloquer la lecture automatique à tout moment \) et planifier en conséquence.  Les stratégies de lecture globale et globales par site s’appliquent à `<audio>` l’ensemble et aux `<video>` éléments, quelle que soit la façon dont ils sont utilisés sur votre site.  

*   Assurez-vous que les contrôles multimédias sont toujours présents sur les éléments multimédias et les contenus publicitaires.  Cela permettra aux utilisateurs de redémarrer la lecture si la lecture automatique est bloquée sur la page.  

*   Évaluez la façon dont la lecture automatique peut affecter l’utilisation des utilisateurs sur votre site Web et envisager d’utiliser la lecture automatique de manière à limiter la lecture de contenu multimédia indésirable.  Si la lecture automatique est une partie essentielle de votre utilisation, envisagez d’utiliser du contenu muet pour commencer et permettre à l’utilisateur d’activer son micro.  Pour que le contenu soit coupé en lecture automatique, la source audio doit être soit explicitement muette soit ne pas être définie.  Dans le cas contraire, l’élément n’est pas considéré comme muet.  

*   Sauf si absolument nécessaire, utilisez les contrôles de navigateur natifs pour la lecture de contenu multimédia.  Cela garantira une connaissance homogène pour les utilisateurs.  Si vous créez des contrôles personnalisés à la place, assurez-vous que les contrôles multimédias sont toujours présents et que vos contrôles réagissent correctement à la suppression de lecture automatique.  

### Délégation iframe  

La lecture automatique dans un `<iframe>` héritera de l’autorisation de lecture automatique de la page parent quelle que soit l’origine du contenu.  Dans un scénario de playlist dans lequel chaque fichier multimédia est hébergé par un autre IFRAME, l’utilisateur ne doit lancer la lecture qu’une seule fois pour l’ensemble de la playlist.  

### Détection de l’autorisation de lecture automatique  

Vous pouvez ajuster vos contrôles de lecture pour afficher l’état correct lorsque la lecture automatique est bloquée en examinant la promesse renvoyée par la `play()` fonction sur l’élément multimédia:  

```javascript
var promise = document.querySelector('video').play();

if (promise !== undefined) { 
    promise.catch(_error => { 
        // Autoplay was blocked
        // Show user media controls to manually start playback
    }).then(() => { 
        // Autoplay started
    }); 
}
```  
