---
description: En savoir plus sur les différents états lors de l’envoi d’extensions au Store
title: États de soumission pour les extensions dans le store
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, développement d’extensions, extensions de navigateur, addons, centre de partenaires, développeur
ms.openlocfilehash: 881166471ec5fabb66367ead650cb86b883cf01d
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343142"
---
# États de soumission pour les extensions dans le magasin de modules extensions Microsoft Edge  

La page vue d’ensemble de l’Partner Center affiche l’état de votre extension dans le flux de soumission global.  Cet article décrit les différents états où votre extension peut se présenter à tout moment pendant le processus de soumission et de certification.  

| # |  État |  Détails |  
|:--- |:--- |:--- |  
| 1 |  Dans le brouillon |  Vous créez votre soumission et enregistrez un brouillon dans votre compte.  Vous n’avez pas soumis votre package d’extension et les détails de votre formulaire de soumission à publier dans le magasin de modules extensions Microsoft Edge.  Votre extension n’est pas disponible pour les utilisateurs dans cet état.  |  
| 2|  En révision |  Vous avez envoyé votre extension.  Votre package d’extension et les détails de votre formulaire d’envoi sont examinés par Microsoft.  Votre extension n’est pas disponible pour les utilisateurs dans cet état.  |  
| 3|  En attente de publication |  Votre soumission est dans cet état une fois la révision de votre extension terminée et votre extension est en cours de préparation pour la publication dans le Microsoft Store.  Cet état est un état intermédiaire entre `In review` `In the store` et .  Cet état n’apparaît peut-être pas pour toutes les soumissions.  |  
| 4|  Dans la boutique |  L’examen est maintenant terminé et votre extension est publiée dans le magasin de modules extensions Microsoft Edge.  Votre extension est disponible sur le Microsoft Store dans les marchés que vous avez spécifiés.  |  
| 5 |  Dans la boutique.  Mise à jour dans la révision |  Votre extension est publiée dans le magasin des extensions Microsoft Edge et vous avez soumis une mise à jour qui est en cours de révision par Microsoft.  |  
| 6 |  Échec de la révision |  Votre envoi est dans cet état si votre extension échoue à un examen.  Un échec de révision peut se produire lors de la révision initiale ou d’une mise à jour.  Vous devez prendre des mesures correctives et resoumettre votre extension.  |  
| 7 |  Indisponible dans le Store |  Il existe trois scénarios possibles lorsque votre extension affiche cet état :  **Unpublished from store**, **Removed from store**et **Blocked**.  La description de chacun des trois états est spécifiée dans 8, 9 et 10.  |  
| 8 |  Non publié à partir du Store |  Vous déspubliez votre extension à partir du magasin de modules extensions Microsoft Edge dans l’Partner Center.  Dans l’Partner Center, vous avez choisi **d’unpublish** sur la page de soumission d’extension.  Après la désinscriture de votre extension, elle n’est plus disponible dans le magasin de modules extensions Microsoft Edge pour les nouveaux utilisateurs à télécharger, mais les utilisateurs existants peuvent continuer à utiliser leurs copies de votre extension.  |  
| 9 |  Supprimé du store |  Si votre extension enfreint les conditions générales du magasin de modules de microsoft Edge, Microsoft peut la supprimer du magasin des extensions Edge et l’état passe à cet état.  <br />  Après la suppression de votre extension par Microsoft, votre extension n’est plus disponible dans le magasin des extensions Microsoft Edge pour les nouveaux utilisateurs à télécharger, mais les utilisateurs existants peuvent continuer à utiliser leurs copies de votre extension.  |  
| 10 |  Élément bloqué |  Si votre extension est malveillante et compromet la sécurité et la confidentialité des utilisateurs, Microsoft a le droit de bloquer votre extension à partir du magasin de modules edge, et l’état passe à cet état.  Si votre extension est bloquée, elle est supprimée du magasin des extensions Edge et de tous les appareils utilisateur.  |  
