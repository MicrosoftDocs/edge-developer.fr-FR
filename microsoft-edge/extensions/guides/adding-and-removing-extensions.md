---
description: Découvrez comment ajouter et supprimer des extensions, et déplacer le bouton d’une extension en regard de la barre d’adresse.
title: Ajout et suppression d’extensions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur, extension
ms.custom: seodec18
localization_priority: Priority
ms.openlocfilehash: fdc6950962e7ce7e0a720d0bafa7e2c63ebd7098
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565364"
---
# Ajout, déplacement et suppression d’extensions pour Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

La prise en charge de Microsoft Edge pour extensions a été introduite dans la **mise à jour anniversaire Windows 10**. Si vous développez une extension Microsoft Edge et que vous souhaitez la charger, ou si vous souhaitez la supprimer maintenant, consultez les étapes ci-dessous.
Vous trouverez également des informations sur la façon de modifier l’emplacement de l’icône d’extension dans le navigateur.

## Ajout d’une extension

1. Ouvrez Microsoft Edge et tapez «à propos de: indicateurs» dans la barre d’adresses.

2. Cochez la case **activer les fonctionnalités de développement d’extensions** .

   ![à propos: indicateurs activez les fonctionnalités de développement](./../media/sideload-aboutflags.png)
   > [!NOTE]
   > Si vous n’avez pas la mise à jour anniversaire Windows 10 ou version ultérieure, cette option n’est pas disponible.

3. Sélectionnez **plus (...)** pour ouvrir le menu.

   ![bouton plus](./../media/morebutton.png)  

4. Sélectionnez **Extensions** dans le menu.

5. Cliquez sur le bouton **charger une extension** .

   ![sélection de l’extension de chargement](./../media/sideload-load-extension.png)

6. Accédez au dossier de votre extension et sélectionnez le bouton **Sélectionner un dossier** .
   ![sélection du dossier d’extension à charger](./../media/sideload-select-extension.png)
   > [!NOTE]
   > Si vous rencontrez un message d’erreur lors du chargement de votre extension, reportez-vous à la page de [résolution des problèmes](./../troubleshooting.md) .


**Voilà, c’est fini! L’extension doit maintenant apparaître dans le volet extension de Microsoft Edge.**

![extension dans le volet extension](./../media/sideload-extension-installed.png)

> [!NOTE]
> Les extensions non signées sont automatiquement désactivées lors du lancement ultérieur de Microsoft Edge. Lorsque le navigateur passe à un état inactif (au bout de 10 secondes d’inactivité), vous verrez la notification suivante en bas de la fenêtre. ![notification risquée ](./../media/riskynotification.png) pour activer les extensions non signées, cliquez sur «Activer quand même».



## Déplacement du bouton extension
En fonction des paramètres de votre extension, il est possible qu’elle apparaisse dans le menu **plus (...)** .

   ![menu actions](./../media/browseraction.png)  


Pour plus d’informations sur le déplacement du menu, voir:

1. Cliquez avec le bouton droit sur le bouton extension.

2. Sélectionner le **bouton afficher en regard de la barre d’adresse**.

   ![menu actions](./../media/browseraction_contextmenu.png)  

Vous pouvez également effectuer cette opération à partir de la page Détails de l’extension:

1. Cliquez sur le bouton extension.
2. Activer/désactiver le **bouton afficher en regard de la barre d’adresse** .

   ![bouton bascule bouton bascule activé](./../media/show-button-toggle.png)

> [!NOTE]
> Vous pouvez toujours déplacer le bouton dans le menu **autres (...)** en cliquant dessus avec le bouton droit et en désélectionnant **afficher en regard de la barre d’adresse** ou en accédant à la page Détails de l’extension et en activant le **bouton afficher en regard de la barre d’adresses** .


## Suppression d’une extension

1. Ouvrez MicrosoftEdge.

2. Sélectionnez **plus (...)** pour ouvrir le menu.

3. Sélectionnez **Extensions** dans le menu.

4. Cliquez avec le bouton droit sur l’extension que vous voulez supprimer, sélectionnez **supprimer**, ou sélectionnez l’extension, puis cliquez sur le bouton **supprimer** .

   ![menu actions](./../media/remove.png)  

**L’extension doit disparaître de la liste dans Microsoft Edge.**
