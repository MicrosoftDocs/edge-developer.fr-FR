---
ms.assetid: 2bc29371-4f2e-4b59-a588-30b107d751f6
description: Découvrez comment Microsoft Edge fournit un mode lecture pour les pages Web pour permettre la lecture de la version sans ajouter.
title: Mode de lecture-Guide de développement
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.openlocfilehash: 0d2076a63f97ecf2b4699795b0036736d0f95c9c
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941999"
---
# Mode Lecture  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Microsoft Edge fournit un mode lecture pour une connaissance plus rationalisée et plus agréable de la lecture de pages Web, sans la distraction de contenus non liés ou secondaires sur la page.  Le mode lecture peut être activé ou désactivé à partir du bouton **lecture** \ (icône du livre \) sur la barre d’adresse ou avec `Ctrl` + `Shift` + `R` .  Le mode lecture extrait les métadonnées suivantes d’une page:  

*   Title
*   Auteur
*   Date
*   Éditeur
*   Image dominante (s \)
*   Légendes de l’image dominante (s \)
*   Images secondaires
*   Contenu du texte principal de la page
*   Copyright

Les utilisateurs peuvent ensuite ajuster le contraste de la page et la taille de police à partir du panneau **paramètres** de Microsoft Edge.  

## Extraction de métadonnées  

Voici les détails des métadonnées de page rendues en mode lecture.  

### Title  

Pour vous assurer que le mode lecture restitue le titre de votre article, procédez comme suit:  

*   Inclure un `title` élément dans votre en-tête  
*   Ajoutez une balise Meta avec `name="title"`  
*   Faites correspondre le texte du titre dans votre corps d’article à la chaîne de contenu de votre balise meta.  Les canaux \ ( `|` \) dans votre chaîne de contenu empêchent l’affichage du lecteur de lire le contenu, essayez d’utiliser des tirets \ ( `-` \) à la place.  

### Auteur  

Le mode lecture va chercher un élément avec `class = "byline-name"` .  Meilleure pratique consiste à placer le nom de l’auteur après le titre et le corps de l’article.  

```html
<div class="byline-name">Author name</div>
```  

### Date  

Le mode lecture permet d’afficher les informations relatives à l’éditeur et la date sur la même ligne, grâce à un autre style de mise en surbrillance des informations.  La date de publication de l’article s’affiche exactement telle qu’elle apparaît dans la chaîne.  Le mode lecture n’est pas converti dans un format de date spécifique.  

Si vous avez une date dans votre corps d’article et que vous voulez que le mode lecture le rende, assignez l’élément contenant la date au sein de la classe `'dateline'` :  

```html
<div class="dateline"> Wednesday, September 18, 2013 7:38 AM </div>
```  

Si vous n’avez pas de date dans le corps de l’article mais souhaitez que le mode lecture effectue le rendu de la date, utilisez la balise meta `name='displaydate'` :  

```html
<meta name="displaydate" content=" Wednesday, September 18, 2013 7:38 AM ">
```  

### Éditeur  

Le mode lecture va chercher le protocole Open Graph `"og:site_name"` pour afficher les informations de l’éditeur.  Il recherche également les `source_organization` `publisher` attributs et dans n’importe quelle balise HTML en tant qu’indicateur secondaire des informations de l’éditeur dans la page.  Le texte de l’éditeur est lié à l’URL de la page à l’aide du style de lien hypertexte de la page du mode lecture.  

```html
<meta content="Name of organization source" property="og:site_name">
```  

### Images  

Le mode lecture capture la plupart des images brutes avec la largeur >= 400px et les proportions >= 1/3 et =< 3,0.  Les images qui ne satisfont pas ces dimensions peuvent toujours être extraites, telles que les images dont la taille est inférieure à 400px, mais qui comportent des sous-titres.  La première image éligible devient l’image dominante de l’article.  L’image dominante est restituée en tant que première partie du contenu et en fonction de la largeur de colonne complète.  Toutes les images suivantes sont rendues en tant qu’images incorporées dans l’article.  

### Légendes  

Il est recommandé de placer les images dans les balises de [figure](https://developer.mozilla.org/docs/Web/HTML/Element/figure) avec au moins deux balises [figcaption](https://developer.mozilla.org/docs/Web/HTML/Element/figcaption) imbriquées.  

### Body  

Pour vous assurer que tout le texte de la page est capturé par le mode lecture, il est recommandé de conserver la même taille de la police et la même profondeur DOM.  L’algorithme du mode lecture permet d’obtenir un certain écart par rapport à cette règle, de sorte que les éditeurs puissent être libres de mettre l’accent sur des lignes ou des mots.  

### Copyright  

Le mode lecture extrait et affiche les informations de Copyright signalées par des balises meta avec `name = "copyright"` , ou s’il n’existe aucune information de méta-indicateur, un nœud de texte contenant le symbole Copyright \ ( `©` \).  Le mode lecture affiche les informations de Copyright à la fin de l’article principal de l’article, dont le style est inférieur à celui du corps de texte principal.  

```html
<meta name="copyright" content="Your copyright information">
```  

## Désactivation du mode lecture  

Si vous pensez que votre contenu n’est pas adapté au mode lecture, vous pouvez utiliser la balise Meta suivante pour désactiver cette fonctionnalité:  

```html
<meta name="IE_RM_OFF" content="true">
```  

Avec cette balise, le bouton **mode lecture** ne s’affiche pas dans la barre d’adresses lorsque les utilisateurs affichent votre page.  
