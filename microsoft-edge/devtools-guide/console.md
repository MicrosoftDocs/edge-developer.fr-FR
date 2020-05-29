---
description: Utilisez l’outil console pour le débogage interactif et les tests ad hoc.
title: DevTools-console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, console
ms.custom: seodec18
ms.openlocfilehash: f2733cac57ed5f2364747ee64e669fa83aae41f4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565579"
---
# Console

L’outil de développement de console dans Microsoft Edge enregistre les informations associées à une page Web (par exemple, JavaScript, requêtes réseau et erreurs de sécurité). Vous pouvez utiliser la console pour le débogage interactif et les tests ad hoc. 

Pour ouvrir l’outil console dans Microsoft Edge, appuyez sur la touche F12 pour accéder à la fenêtre de l’outil de développement (ou cliquez avec le bouton droit sur la page, puis sélectionnez **inspecter l’élément**). Ensuite, sélectionnez l’onglet de la **console** en haut de la fenêtre. 

Vous pouvez également utiliser l’outil console pour communiquer avec une page Web en cours d’exécution. Vous pouvez utiliser la console pour:

- Publiez des [codes d’erreur](./console/error-and-status-codes.md) et de statut standard et des messages d’information lors de l’exécution de votre code.
- Générez des journaux de débogage personnalisés à partir des appels d' [API de console](./console/console-api.md) que vous incluez dans votre code.
- Fournissez un affichage [ligne de commande](./console/command-line.md) et arborescence interactive pour inspecter les valeurs de retour actuelles des variables et fonctions clés.

## Éléments de la console

L’image ci-après illustre les principales composantes de la console:

![Console Microsoft Edge DevTools](./media/console.png)

1. **Erreurs**  /  **Avertissements**  /  **Infos**  /  Boutons **journaux** : filtrez la sortie de la console par le type spécifié. Vous pouvez sélectionner plusieurs boutons en maintenant la touche **CTRL** enfoncée. Le bouton **tout** annule tous les filtres.

2. Bouton **Effacer** (**Ctrl + L**): le bouton **Effacer** efface l’affichage actuel de la console.

3. Case à cocher **conserver le journal** : activez la case à cocher **conserver le journal** pour conserver la sortie de votre console sur toutes les mises à jour de la page, puis fermez et rouvrez devtools. L’historique de la console ne s’efface que lorsque vous fermez l’onglet ou vous effacez manuellement la console.

4. **Target**: utilisez le menu déroulant **target** pour basculer vers un autre contexte d’exécution, tel qu’un `<iframe>` dans votre page ou une extension en cours d’exécution. Par défaut, le cadre de niveau supérieur de votre page est sélectionné. Pointez sur une image sélectionnée pour afficher une info-bulle indiquant l’URL complète de cette ressource.

5. **Afficher la console**  /  Bouton **masquer la console** (**CTRL** +  **&grave;** ): outre le panneau de la console, vous pouvez utiliser la console à partir du bas de n’importe quel autre panneau devtools en appuyant sur le bouton **Afficher**la console  /  **Masquer** . Le bouton n’a aucun effet lorsque DevTools est ouvert dans le panneau de la console.
 
6. **Journaux de filtre** (**Ctrl + F**): vous pouvez également filtrer les journaux à l’aide d’une chaîne de texte spécifique dans la zone de recherche.

7. **Débogueur**: sélectionnez n’importe quel lien source bleu pour ouvrir le débogueur devtools à cette ligne de code pour une inspection plus poussée.

## Associés

Action                                            | Raccourci               
:-------------------------------------------------| :----------------------
Lancer DevTools avec la console activée             | **CTRL**  +  **MAJ**  +  **J** 
Basculer vers la console                                 | **CTRL**  +  **2**           
Afficher/masquer la console à partir d’un autre onglet DevTools       | **Ctrl**  +  CTRL **&grave;** (battement du retour)  
Exécuter (commande sur une ligne)                     | **Entrée**                
Saut de ligne sans s’exécuter (commande de plusieurs lignes) | **MAJ**  +  **Entrée** ou **CTRL +**  +  **entrée**      
Effacer la console de tous les messages                 | **CTRL**  +  **L**           
Journaux de filtre (Positionnez le focus sur la zone de recherche)             | **CTRL**  +  **F**           
Accepter la suggestion de saisie semi-automatique (activée) | **Entrée** ou **Tab**       
Suggestion de saisie semi-automatique précédente/suivante          | Touche de direction **haut** / **Touche de direction bas**   


