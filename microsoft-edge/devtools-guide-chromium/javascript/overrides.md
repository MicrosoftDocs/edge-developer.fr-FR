---
description: La fonctionnalité de substitution est une fonctionnalité de l’outil sources de Microsoft Edge DevTools qui vous permet de copier des ressources de pages Web sur votre disque dur.  Lorsque vous actualisez la page Web, DevTools ne chargez pas la ressource, mais remplacez-la par votre copie locale.
title: Remplacer les ressources de pages Web par des copies locales à l’aide de Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 579ebe92dc50571837e7e3caf8fb7c1a9989bc59
ms.sourcegitcommit: 9dcaf598f3930bcfab9f93ff63463beb98274de0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/30/2020
ms.locfileid: "11145155"
---
# Remplacer les ressources de pages Web par des copies locales à l’aide de Microsoft Edge DevTools  

Il peut arriver que vous deviez résoudre un problème sur une page Web à laquelle vous n’avez pas accès ou qui nécessite un processus de génération lent et complexe.  Vous pouvez déboguer et résoudre tout type de problème dans DevTools. Toutefois, le problème ne persiste pas.  Après avoir actualisé le fichier, tout votre bureau a disparu.  

La fonctionnalité de remplacement de l’outil [sources][DevToolsSourcesTool] vous permet de résoudre ce problème.  

Vous pouvez à présent prendre une ressource de la page Web actuelle et la stocker localement.  Lorsque vous actualisez la page Web, le navigateur ne charge pas la ressource à partir du serveur.  Au lieu de cela, le navigateur le remplace par votre copie locale de la ressource.  

## Configuration de votre dossier local pour le stockage des remplacements  

1.  Dans l’outil **sources** , recherchez plusieurs sections sur le côté gauche.  Si l’option **remplacements** ne s’affiche pas, sélectionnez <code>&#x0226B;</code><!--`≫`--> pour y accéder.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-overflow-menu.msft.png" alt-text="Outil sources avec un espace insuffisant pour afficher l’option de remplacement" lightbox="../media/javascript-overrides-overflow-menu.msft.png":::
             Outil **sources** avec un espace insuffisant pour afficher l’option de remplacement  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-menu.msft.png" alt-text="Outil sources avec un espace insuffisant pour afficher l’option de remplacement" lightbox="../media/javascript-overrides-menu.msft.png":::
             Sélectionner l’option remplacements  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Après avoir sélectionné l’option **remplacements** , vous devez choisir un dossier sur votre ordinateur local pour stocker les fichiers de ressources que vous souhaitez remplacer.  Pour rechercher un dossier, sélectionnez le **dossier + Sélectionner pour les remplacements** .  
    
    :::image type="complex" source="../media/javascript-overrides-select-folder.msft.png" alt-text="Outil sources avec un espace insuffisant pour afficher l’option de remplacement" lightbox="../media/javascript-overrides-select-folder.msft.png":::
       Sélectionner un dossier à utiliser pour les remplacements  
    :::image-end:::  
    
1.  DevTools vous avertit que vous devez disposer d’un accès complet au dossier et que vous ne devez pas divulguer d’informations sensibles.  Dans la barre d’avertissement, sélectionnez **autoriser** pour accorder l’accès.  
    
    :::image type="complex" source="../media/javascript-overrides-give-access-to-folder.msft.png" alt-text="Outil sources avec un espace insuffisant pour afficher l’option de remplacement" lightbox="../media/javascript-overrides-give-access-to-folder.msft.png":::
       Accorder à DevTools l’accès au dossier  
    :::image-end:::  
    
1.  Dans le volet **remplacements** , une case à cocher doit s’afficher à côté `Enable Local Overrides` et au dossier de remplacements.  Une icône s’affiche à côté de celle-ci pour vous permettre de supprimer vos paramètres de remplacement locaux.  Vous avez terminé la configuration de votre dossier et vous êtes prêt à remplacer les ressources dynamiques par des ressources locales.
    
    :::image type="complex" source="../media/javascript-overrides-folder-setup-complete.msft.png" alt-text="Outil sources avec un espace insuffisant pour afficher l’option de remplacement" lightbox="../media/javascript-overrides-folder-setup-complete.msft.png":::
       Configuration réussie d’un dossier de remplacement  
    :::image-end:::  
    
## Ajouter des fichiers à votre dossier de remplacement  
  
Pour ajouter des fichiers à votre dossier de remplacements, ouvrez l’outil **éléments** et examinez la page Web.  Pour modifier le fichier CSS, sélectionnez son nom dans l’inspecteur de **styles** .  

:::image type="complex" source="../media/javascript-overrides-select-css-file.msft.png" alt-text="Outil sources avec un espace insuffisant pour afficher l’option de remplacement" lightbox="../media/javascript-overrides-select-css-file.msft.png":::
   Sélectionner un fichier dans l’inspecteur de **styles**  
:::image-end:::  

Dans l’éditeur de **sources** , pointez sur le nom du fichier que vous avez choisi, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez **Enregistrer pour les remplacements**.  

:::image type="complex" source="../media/javascript-overrides-file-name.msft.png" alt-text="Outil sources avec un espace insuffisant pour afficher l’option de remplacement" lightbox="../media/javascript-overrides-file-name.msft.png":::
   Dans l’éditeur de **sources** , ajoutez le nom du fichier aux substitutions.  
:::image-end:::  

:::image type="complex" source="../media/javascript-overrides-save-for-overrides.msft.png" alt-text="Outil sources avec un espace insuffisant pour afficher l’option de remplacement" lightbox="../media/javascript-overrides-save-for-overrides.msft.png":::
   Dans le menu contextuel, cliquez sur **Enregistrer pour les remplacements**  
:::image-end:::  

Le fichier est stocké dans votre dossier Overrides.  Vérifiez que DevTools crée un dossier nommé à l’aide de l’URL du fichier avec la structure de répertoires correcte.  Le fichier est stocké dans.  Le nom de fichier de l’éditeur comporte également un point violet qui indique que le fichier est local et non en cours.  

:::image type="complex" source="../media/javascript-overrides-file-stored.msft.png" alt-text="Outil sources avec un espace insuffisant pour afficher l’option de remplacement" lightbox="../media/javascript-overrides-file-stored.msft.png":::
   Le fichier a été enregistré dans le dossier de remplacements  
:::image-end:::  

:::row:::
   :::column span="":::
      Dans l’exemple suivant, vous pouvez désormais modifier les styles de la page Web.  Pour ajouter une bordure rouge autour du fichier, dans l’éditeur de **styles** , copiez le style suivant et ajoutez-le à l’élément de corps.  
      
      ```css
      border: 10px solid firebrick
      ```  
   :::column-end:::
   :::column span="":::
      Le fichier est enregistré automatiquement sur votre ordinateur.  Si vous actualisez le fichier, la bordure est affichée et aucune de vos tâches ne sera perdue.  
      
      :::image type="complex" source="../media/javascript-overrides-changing-styles.msft.png" alt-text="Outil sources avec un espace insuffisant pour afficher l’option de remplacement" lightbox="../media/javascript-overrides-changing-styles.msft.png":::
         Changer les styles de pages Web de façon permanente en modifiant un fichier dans votre dossier de remplacement  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

:::row:::
   :::column span="":::
      Dans l’outil **sources** , dans la section **page** , pointez sur un fichier, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \) et ajoutez-le à des substitutions.  Là encore, les fichiers qui se trouvent déjà dans votre dossier remplacements sont dotés d’un point violet sur l’icône.  
      
      :::image type="complex" source="../media/javascript-overrides-safe-from-sources.msft.png" alt-text="Outil sources avec un espace insuffisant pour afficher l’option de remplacement" lightbox="../media/javascript-overrides-safe-from-sources.msft.png":::
         Choisir un fichier à partir de l’outil **sources** pour les remplacements  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Vous pouvez également accéder à un fichier à l’aide de l’outil **réseau** , ouvrir le menu contextuel \ (cliquez avec le bouton droit sur \) et l’ajouter aux remplacements.  Lorsque les remplacements sont activés, les fichiers qui se trouvent sur votre ordinateur et non à partir de la page Web dynamique.  Lorsque les remplacements sont activés, dans l’outil **réseau** , recherchez une icône d’avertissement en regard du nom du fichier.  
      
      :::image type="complex" source="../media/javascript-overrides-network.msft.png" alt-text="Outil sources avec un espace insuffisant pour afficher l’option de remplacement" lightbox="../media/javascript-overrides-network.msft.png":::
         Choisir un fichier à partir de l’outil **réseau** pour les remplacements  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Interaction bidirectionnelle des substitutions  

Utilisez l’éditeur fourni avec l’outil **sources** de devtools ou un éditeur pour lequel vous voulez modifier les fichiers.  Les modifications sont synchronisées au sein des différents produits qui accèdent aux fichiers dans le dossier remplacements.  

## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsSourcesTool]: ../sources.md "Présentation de l’outil sources | Documents Microsoft"  
