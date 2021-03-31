---
description: Cette page fournit une vue d’ensemble des nouveautés de EdgeHTML 13.
title: Nouvelles fonctionnalités et API dans EdgeHTML 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2119e576a637d5f78e073f49a3cb1868a7ce1ca4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233456"
---
# Nouveautés de EdgeHTML 13  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Voici les modifications apportées à EdgeHTML 13, le moteur permettant d’alimenter le navigateur Microsoft Edge dans la [première mise à jour majeure](https://blogs.windows.com/windowsexperience/2015/11/12) de Windows 10 \(11/2015, Build 10586 \).  Pour obtenir une vue d’ensemble des modifications apportées au navigateur Microsoft Edge global, voir présentation de la [mise à jour de l’EdgeHTML 13, notre première plate-forme pour Microsoft Edge](https://blogs.windows.com/msedgedev/2015/11/16).  

Vous trouverez ci-dessous le lien permanent pour la liste des modifications suivante:  [https://aka.ms/devguide_edgehtml_13](./edgehtml-13.md) .  

## Fonctionnalités  

### CSS  

EdgeHTML 13 prend en charge les nouvelles fonctionnalités de CSS, notamment:  

*   [Pseudo-classes CSS de la mutabilité](https://developer.microsoft.com/microsoft-edge/platform/status/cssmutabilitypseudoclasses)  
*   [Pseudo-classes de la plage CSS](https://developer.microsoft.com/microsoft-edge/platform/status/cssrangepseudoclasses)  
*   Mots-clés CSS [initial](https://developer.microsoft.com/microsoft-edge/platform/status/cssinitialvalue) et [unset](https://developer.microsoft.com/microsoft-edge/platform/status/cssunsetvalue)  

### Extensions multimédias chiffrées  

Microsoft Edge prend désormais en charge les API d' [extensions de média chiffrées](https://w3.org/TR/encrypted-media) sans préfixe.  Extensions multimédias chiffrées \(Encrypted \) étend les éléments vidéo et audio pour activer le contenu protégé par la gestion des droits numériques (DRM) sans utiliser les plug-ins.  En savoir plus sur Encrypted:  [extensions multimédias chiffrées](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API).  

### Graphiques  

EdgeHTML 13 présente les mises à jour graphiques suivantes:  

*   [Ellipse de zone de dessin](https://developer.microsoft.com/microsoft-edge/platform/status/canvas2dellipse)  
*   [Modes de fusion de canevas](https://developer.microsoft.com/microsoft-edge/platform/status/compositingandblendingincanvas2d)  
*   [<picture> élément](https://developer.microsoft.com/microsoft-edge/platform/status/pictureelement)  
*   [Contenu externe SVG](https://developer.microsoft.com/microsoft-edge/platform/status/svgexternalcontent)  

### JavaScript  

EdgeHTML 13 inclut des [améliorations majeures et une nouvelle prise en charge des fonctionnalités dans Chakra](https://blogs.windows.com/msedgedev/2015/09/30), le moteur JavaScript permettant d’alimenter Microsoft Edge, notamment:  

#### Nouvelles fonctionnalités  

Activé par défaut  

*   [asm.js](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=asm.js) activé par défaut \([billet de blog](https://blogs.windows.com/msedgedev/2015/11/10), [démonstration](https://dev.windows.com/microsoft-edge/testdrive/demos/chess)\)  
*   [Cours](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=classes) \(ES2015 \)  

#### Fonctionnalités JavaScript expérimentales  

Activé avec `about:flags`  

*   [Fonctions Async](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctions/?q=async%20functions) \(ES2016 \)  
*   [Opérateur d’élévation](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016/?q=exponentiation%20operator) à la puissance \(ES2016 \)  
*   [Structuration](https://developer.microsoft.com/microsoft-edge/platform/status/destructuringES2015/?q=destructuring) de \(ES2015 \)  

### Entrée de l’utilisateur  

Les fonctionnalités suivantes introduites dans EdgeHTML 13 améliorent l’entrée utilisateur:  

*   [\<meter\> élément](https://developer.microsoft.com/microsoft-edge/platform/status/meterelement)  
*   [gestionnaire d’événements oninvalid pour le document d’élément et la fenêtre](https://developer.microsoft.com/microsoft-edge/platform/status/oninvalideventhandler)  

### Verrouillage du pointeur  

Microsoft Edge prend désormais en charge l’API de verrouillage de pointeur (auparavant appelée le verrouillage de la souris) pour accéder au mouvement brut de la souris, en verrouillant la cible des événements de souris sur un élément unique, ce qui évite de limiter la distance de déplacement de la souris dans une seule direction, et de supprimer le curseur de l’affichage.  

## Nouvelles API dans EdgeHTML 13  

Voici la liste complète des nouvelles API dans EdgeHTML 13.  Ils sont répertoriés au format de `[interface name].[api name]` .  

<iframe height='584' scrolling='no' title='Nouvelles API dans EdgeHTML 13' src='//codepen.io/MicrosoftEdgeDocumentation/embed/vmzxEY/?height=584&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width:  100%;'>Reportez-vous au stylo <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/vmzxEY/'> nouvelles API dans EdgeHTML 13 </a> par Microsoft Edge Docs ( <a href='http://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) sur <a href='http://codepen.io'> CodePen </a> .</iframe>  
