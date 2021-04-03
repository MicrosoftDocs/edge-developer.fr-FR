---
description: La fonctionnalité Overrides est une fonctionnalité de l’outil Sources de Microsoft Edge DevTools qui vous permet de copier des ressources de page web sur votre disque dur.  Lorsque vous actualisez la page web, DevTools ne charge pas la ressource, mais la remplace par votre copie locale.
title: Remplacer les ressources de page web avec des copies locales à l’aide de Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 7f273f89708e0948e68cd2c7ba79cefb6d7e167c
ms.sourcegitcommit: 2ddfd98d1e871be9c61380a8ca57da398d38bd54
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "11230963"
---
# <a name="override-webpage-resources-with-local-copies-using-microsoft-edge-devtools"></a>Remplacer les ressources de page web avec des copies locales à l’aide de Microsoft Edge DevTools  

Parfois, vous devez résoudre un problème sur une page web à qui vous n’avez pas accès ou les correctifs impliquent un processus de création lent et complexe.  Vous pouvez déboguer et résoudre tous les types de problèmes dans DevTools. Mais le problème est que les modifications ne sont pas persistantes.  Une fois que vous avez actualisé le fichier, tout votre travail a disparu.  

La fonctionnalité Remplacements de l’outil [Sources][DevToolsSourcesTool] vous aide à résoudre ce problème.  

Vous pouvez maintenant prendre une ressource de la page web actuelle et la stocker localement.  Lorsque vous actualisez la page web, le navigateur ne charge pas la ressource à partir du serveur.  Au lieu de cela, le navigateur le remplace par votre copie locale de la ressource.  

## <a name="setting-up-your-local-folder-to-store-overrides"></a>Configuration de votre dossier local pour stocker les remplacements  

1.  Dans **l’outil Sources,** recherchez plusieurs sections sur le côté gauche.  Si **l’option Remplacements** n’est pas affichée, choisissez la <code>&#x0226B;</code><!--`≫`--> pour y arriver.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-overflow-menu.msft.png" alt-text="Outil Sources avec un espace insuffisant pour afficher l’option de remplacements" lightbox="../media/javascript-overrides-overflow-menu.msft.png":::
             **Outil Sources** avec un espace insuffisant pour afficher l’option de remplacements  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-menu.msft.png" alt-text="Choisir l’option remplacements" lightbox="../media/javascript-overrides-menu.msft.png":::
             Choisir l’option remplacements  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Après avoir choisi **l’option Remplacements,** vous devez choisir un dossier sur votre ordinateur local pour stocker les fichiers de ressources que vous souhaitez remplacer.  Choisissez le **dossier + Sélectionner pour les remplacements** pour rechercher un dossier.  
    
    :::image type="complex" source="../media/javascript-overrides-select-folder.msft.png" alt-text="Choisir un dossier à utiliser pour les remplacements" lightbox="../media/javascript-overrides-select-folder.msft.png":::
       Choisir un dossier à utiliser pour les remplacements  
    :::image-end:::  
    
1.  DevTools vous avertit que vous devez avoir un accès total au dossier et que vous ne devez pas révéler d’informations sensibles.  Dans la barre d’avertissement, **sélectionnez Autoriser** l’accès.  
    
    :::image type="complex" source="../media/javascript-overrides-give-access-to-folder.msft.png" alt-text="accorder à DevTools l’accès au dossier ;" lightbox="../media/javascript-overrides-give-access-to-folder.msft.png":::
       Accorder à DevTools l’accès au dossier  
    :::image-end:::  
    
1.  Dans le **volet Remplacements,** une case à cocher doit s’afficher en regard de votre dossier `Enable Local Overrides` remplacements.  Une icône s’affiche en face de celle-ci qui vous permet de supprimer vos paramètres de remplacements locaux.  Vous avez maintenant terminé la configuration de votre dossier et êtes prêt à remplacer les ressources en direct par des ressources locales.
    
    :::image type="complex" source="../media/javascript-overrides-folder-setup-complete.msft.png" alt-text="La mise en place d’un dossier de remplacements a réussi" lightbox="../media/javascript-overrides-folder-setup-complete.msft.png":::
       La mise en place d’un dossier de remplacements a réussi  
    :::image-end:::  
    
## <a name="adding-files-to-your-overrides-folder"></a>Ajout de fichiers à votre dossier Overrides  
  
Pour ajouter des fichiers à votre dossier de remplacements, ouvrez l’outil **Éléments** et examinez la page web.  Pour modifier, choisissez le nom du fichier CSS dans l’inspecteur **de styles.**  

:::image type="complex" source="../media/javascript-overrides-select-css-file.msft.png" alt-text="Choisir un fichier dans l’inspecteur styles" lightbox="../media/javascript-overrides-select-css-file.msft.png":::
   Choisir un fichier dans l’inspecteur **styles**  
:::image-end:::  

Dans l’éditeur **sources,** pointez sur le nom de fichier de votre fichier choisi, ouvrez le menu contextuel \(clic droit\), puis choisissez Enregistrer pour **les remplacements.**  

:::image type="complex" source="../media/javascript-overrides-file-name.msft.png" alt-text="Dans l’éditeur sources, ajoutez le nom du fichier aux substitutions" lightbox="../media/javascript-overrides-file-name.msft.png":::
   Dans **l’éditeur sources,** ajoutez le nom du fichier aux substitutions  
:::image-end:::  

:::image type="complex" source="../media/javascript-overrides-save-for-overrides.msft.png" alt-text="Dans le menu contexto, sélectionnez Enregistrer pour les remplacements" lightbox="../media/javascript-overrides-save-for-overrides.msft.png":::
   Dans le menu contexto, **sélectionnez Enregistrer pour les remplacements**  
:::image-end:::  

Le fichier est stocké dans votre dossier remplacements.  Vérifiez que DevTools crée un dossier nommé à l’aide de l’URL du fichier avec la structure de répertoires correcte.  Le fichier est stocké à l’intérieur.  Le nom de fichier dans l’éditeur affiche désormais également un point violet qui indique que le fichier est local et non en direct.  

:::image type="complex" source="../media/javascript-overrides-file-stored.msft.png" alt-text="Le fichier a été correctement stocké dans votre dossier remplacements" lightbox="../media/javascript-overrides-file-stored.msft.png":::
   Le fichier a été correctement stocké dans votre dossier remplacements  
:::image-end:::  

:::row:::
   :::column span="":::
      Dans l’exemple suivant, vous pouvez maintenant modifier les styles de la page web.  Pour ajouter une bordure rouge autour du fichier, dans l’éditeur **styles,** copiez le style suivant et ajoutez-le à l’élément body.  
      
      ```css
      border: 10px solid firebrick
      ```  
   :::column-end:::
   :::column span="":::
      Le fichier est automatiquement enregistré sur votre ordinateur.  Si vous actualisez le fichier, la bordure s’affiche et aucune partie de votre travail n’est perdue.  
      
      :::image type="complex" source="../media/javascript-overrides-changing-styles.msft.png" alt-text="Modifier les styles de page web de façon permanente en éditant un fichier dans votre dossier Remplacements" lightbox="../media/javascript-overrides-changing-styles.msft.png":::
         Modifier les styles de page web de façon permanente en éditant un fichier dans votre dossier Remplacements  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

:::row:::
   :::column span="":::
      Dans **l’outil Sources,** dans la section **Page,** pointez sur n’importe quel fichier, ouvrez le menu contextuel \(clic droit\) et ajoutez-le aux remplacements.  Là encore, les fichiers déjà dans votre dossier remplacements ont un point violet sur l’icône.  
      
      :::image type="complex" source="../media/javascript-overrides-safe-from-sources.msft.png" alt-text="Choisir un fichier dans l’outil Sources pour les remplacements" lightbox="../media/javascript-overrides-safe-from-sources.msft.png":::
         Choisir un fichier dans **l’outil Sources** pour les remplacements  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Vous pouvez également, sur l’outil **Réseau,** pointer sur n’importe quel fichier, ouvrir le menu contextuel \(clic droit\) et l’ajouter aux remplacements.  Lorsque les substitutions sont en vigueur, les fichiers qui se trouvent sur votre ordinateur et non à partir de la page web en direct.  Lorsque les substitutions sont en vigueur, sur l’outil **Réseau,** recherchez une icône d’avertissement en face du nom de fichier.  
      
      :::image type="complex" source="../media/javascript-overrides-network.msft.png" alt-text="Choisir un fichier dans l’outil Réseau pour les remplacements" lightbox="../media/javascript-overrides-network.msft.png":::
         Choisir un fichier dans **l’outil** Réseau pour les remplacements  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="two-way-interaction-of-overrides"></a>Interaction double des substitutions  

Utilisez l’éditeur fourni avec l’outil **Sources** de DevTools ou tout éditeur que vous souhaitez modifier les fichiers.  Les modifications sont synchronisées entre tous les produits qui accèdent aux fichiers dans le dossier remplacements.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsSourcesTool]: ../sources/index.md "Vue d’ensemble de l’outil Sources | Documents Microsoft"  
