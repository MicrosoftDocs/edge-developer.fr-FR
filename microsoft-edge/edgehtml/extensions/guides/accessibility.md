---
ms.assetid: c4544a19-de78-4c69-a042-c0415726548f
description: Pour vous assurer que l’icône de votre extension est visible en mode clair et foncé, suivez le Guide d’accessibilité.
title: Accessibilité-extensions (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e6e7dbd2ee66ac785be31eec7189b87e6a6bd91f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233430"
---
# Accessibilité-extensions (EdgeHTML)  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## Création d’icônes d’extension accessibles pour Microsoft Edge

Les développeurs d’extensions tierces sont invités à utiliser des ressources d’image qui répondent aux exigences strictes en matière d’accessibilité de Microsoft de sorte que les icônes soient clairement visibles pour les thèmes clairs et sombres. Nous vous recommandons d’utiliser une 14:1 de rapport entre la couleur d’arrière-plan et la couleur dominante de l’icône.


Les extensions tierces développées par Microsoft appliquent un traitement visuel «d’adhésif» pour répondre à ces exigences.

### Exemples d’une «vignette»

L’objectif principal de «adhésive» est de rendre l’icône visuellement accessible sur une couleur d’arrière-plan. Le rapport couleur recommandé entre le trait blanc et votre icône doit être 14:1 pour prendre en charge les exigences de contraste élevé.

#### Icône bon
Dans le cas d’une vignette, une icône d’ombre est toujours visible sur une couleur d’arrière-plan.


![image de l’icône visible sur une couleur d’arrière-plan](./../media/accessibility-light-to-dark-good.png)

#### Icône incorrecte
Sans aucune vignette, une icône peut être mélangée avec l’arrière-plan et devenir impossible à voir.


![image d’une icône fusionnée en arrière-plan noir](./../media/accessibility-light-to-dark-bad.png)

### Icône «autocollant» dans votre extension

Les cinq étapes suivantes décrivent la méthode de création d’une icône d’extension qui répond aux exigences d’accessibilité de Microsoft:


| Étape1                                       | Étape2                                       | Étape3                                                                                 | Étape4                                                                          | Étape5                                                       |
|:---------------------------------------------|:---------------------------------------------|:---------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|:-------------------------------------------------------------|
| Définissez votre icône dans la grille spécifiée.    | Réduisez la taille de votre icône de 2 pixels.           | Copiez votre icône et collez-la sur place. Créer un trait extérieur de 2 pixels avec des angles arrondis. | Dessinez le contour, relâchez le chemin composé et fusionnez les formes restantes. | Colorez le trait extérieur blanc et l’icône interne comme vous le souhaitez. |
| ![étape](./../media/accessibility-step1.png) | ![étape2](./../media/accessibility-step2.png) | ![step3](./../media/accessibility-step3.png)                                           | ![step4](./../media/accessibility-step4.png)                                    | ![step5](./../media/accessibility-step5.png)                 |

