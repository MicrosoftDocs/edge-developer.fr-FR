---
description: Testez votre extension en la chargeant de nouveau dans le navigateur
title: Chargement de version de version secondaire de votre extension
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, développement web, html, css, javascript, développeur, extensions
ms.openlocfilehash: 7070878b9608e6d239179078390f2315e0b289a1
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104771"
---
# Charger une version test d’une extension

Pendant le développement, vous pouvez utiliser le navigateur Microsoft Edge \(Chromium\) pour exécuter et déboguer votre extension en toute sécurité. En chargeant une version test de votre extension localement dans votre navigateur, vous pouvez exécuter et tester votre extension. Cet article explique comment chargement de version de chargement des extensions dans Microsoft Edge.

Pour recharger une version de votre extension, suivez ces étapes.

1.  Ouvrez la page en choisissant les trois points en haut de votre navigateur, puis en sélectionnant `edge://extensions` **Extensions.**

       :::image type="complex" source="./media/part1-threedots.png" alt-text="Ouvrir la page edge://extensions page":::
          Ouvrir la page edge://extensions page :::image-end:::

1.  Dans la page gestion des extensions, dans , activer le mode développeur à l’aide du basculement en `edge://extensions` bas à gauche de la page. ****

       :::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Activer le mode développeur":::
          Activer le mode développeur :::image-end:::

1.  Lors de l’installation de votre extension pour la première fois, choisissez **Charger décompressé.**  You’ll be prompted for the directory with your extension source files.  Votre extension est installée dans votre navigateur, comme les extensions installées à partir du store.  

       :::image type="complex" source="./media/part1-installed-extension.png" alt-text="Page Des extensions installées affichant une extension installée":::
          Page Des extensions installées affichant une extension installée :::image-end:::

Lors du développement, vous devrez peut-être également effectuer les tâches suivantes.
* Mettez à jour l’extension. Accédez `edge://extensions` à , puis sélectionnez **Recharger** pour mettre à jour votre extension.  
* Supprimez l’extension de votre navigateur. Accédez `edge://extensions` à , puis sélectionnez votre `Remove` extension.