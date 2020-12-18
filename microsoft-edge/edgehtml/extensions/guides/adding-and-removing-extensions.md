---
description: Découvrez comment ajouter et supprimer des extensions, ainsi que déplacer le bouton d’une extension en regard de la barre d’adresses.
title: Ajout et suppression d’extensions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, développement web, html, css, javascript, développeur, extension
ms.custom: seodec18
ms.date: 12/15/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3473108918ec3cb3945e0999b27873ddea40aa5c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233450"
---
# Ajout, déplacement et suppression d’extensions pour Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

La prise en charge des extensions par Microsoft Edge a été introduite dans la **mise à jour du 10e anniversaire de Windows**. Si vous développez une extension Microsoft Edge et que vous voulez la charger, ou si vous l'avez déjà et que vous voulez maintenant la supprimer, consultez la procédure ci-dessous.
Vous y trouverez également des détails sur la modification de l'emplacement de l'icône de votre extension dans le navigateur.

## Ajout d’une extension

1. Ouvrez Microsoft Edge et tapez «à propos de: indicateurs» dans la barre d’adresses.

2. Activez la case à cocher **Activer les fonctionnalités de développeur d’extension**.

   ![à propos de: indicateurs activer les fonctionnalités de développeur](./../media/sideload-aboutflags.png)
   > [!NOTE]
   > Si vous n’avez pas la mise à jour anniversaire Windows10 ou version ultérieure, cette option n’est pas disponible.

3. Pour ouvrir le menu, sélectionnez **Plus (...)**.

   ![Bouton plus](./../media/morebutton.png)  

4. Dans le menu, sélectionnez **Extensions**.

5. Sélectionnez le bouton **Charger une extension**.

   ![sélection de charger une extension](./../media/sideload-load-extension.png)

6. Accédez au dossier de votre extension, puis sélectionnez le bouton **Sélectionner un dossier**.
   ![sélection du dossier d’extension à charger](./../media/sideload-select-extension.png)
   > [!NOTE]
   > Si vous rencontrez un message d’erreur lors du chargement de votre extension, consultez la page [Résolution des problèmes](./../troubleshooting.md) pour obtenir des instructions.


**Vous avez terminé. Vous devez maintenant voir l’extension répertoriée dans le volet extension de Microsoft Edge.**

![extension dans le volet extension](./../media/sideload-extension-installed.png)

> [!NOTE]
> Les extensions non signées sont automatiquement désactivées lors du lancement ultérieur de Microsoft Edge. Lorsque le navigateur entre dans un état d’inactivité (après environ 10secondes d’inactivité), la notification suivante s’affiche au bas de la fenêtre. ![notification risquée](./../media/riskynotification.png) Pour activer les extensions non signées, cliquez sur «Activer quand même».



## Déplacement du bouton d’extension
Selon les paramètres de votre extension, celui-ci peut s’afficher dans le menu **Plus (...)**.

   ![menu actions-navigateur](./../media/browseraction.png)  


Si vous voulez déplacer le bouton hors du menu pour y accéder plus facilement:

1. Cliquez avec le bouton droit sur le bouton d’extension.

2. Sélectionnez **Afficher le bouton en regard de barre d’adresses**.

   ![menu contextuel du navigateur](./../media/browseraction_contextmenu.png)  

Vous pouvez également effectuer cette opération à partir de la page Détails de l’extension:

1. Cliquez sur le bouton extension.
2. Activer **Afficher le bouton en regard de la barre d’adresses**.

   ![bouton activer/désactiver le bouton bascule](./../media/show-button-toggle.png)

> [!NOTE]
> Vous pouvez toujours déplacer le bouton vers le menu **Plus (...)** en cliquant dessus avec le bouton droit et en désélectionnant la case à cocher **Afficher en regard de la barre d’adresses** ou en accédant à la page Détails de l’extension et en désactivant la case à cocher **Afficher le bouton en regard de la barre d’adresses**.


## Suppression d’une extension

1. Ouvrez MicrosoftEdge.

2. Pour ouvrir le menu, sélectionnez **Plus (...)**.

3. Dans le menu, sélectionnez **Extensions**.

4. Cliquez avec le bouton droit sur l’extension que vous voulez supprimer, puis sélectionnez **Supprimer**, ou sélectionnez l’extension et cliquez sur le bouton **Supprimer**.

   ![menu actions-supprimer](./../media/remove.png)  

**L’extension doit disparaître de la liste dans Microsoft Edge.**
