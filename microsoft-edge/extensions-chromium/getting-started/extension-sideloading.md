---
description: Testez votre extension en la chargement indépendant dans le navigateur
title: Charger votre extension
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-chrome, développement Web, html, CSS, JavaScript, développeur, extensions
ms.openlocfilehash: 7070878b9608e6d239179078390f2315e0b289a1
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104771"
---
# Charger une extension

Pendant le développement, vous pouvez utiliser le navigateur Microsoft Edge \(chrome \) pour exécuter et déboguer votre extension en toute sécurité. Chargement indépendant votre extension locale dans votre navigateur, vous pouvez exécuter et tester votre extension. Cet article explique comment charger les extensions dans Microsoft Edge.

Pour charger votre extension, procédez comme suit.

1.  Ouvrez la `edge://extensions` page en cliquant sur les points de suspension en haut de votre navigateur, puis sélectionnez **Extensions**.

       :::image type="complex" source="./media/part1-threedots.png" alt-text="Ouvrir la page edge://extensions":::
          Ouvrir la page edge://extensions :::image-end:::

1.  Dans la page gestion des extensions à `edge://extensions` , activez le **mode développeur** à l’aide du bouton bascule en bas à gauche de la page.

       :::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Ouvrir la page edge://extensions":::
          Activer le mode développeur :::image-end:::

1.  Lorsque vous installez votre extension pour la première fois, sélectionnez **charger**.  Vous serez invité à entrer le répertoire contenant vos fichiers sources d’extension.  Votre extension est installée dans votre navigateur, de la même façon que dans le Windows Store.  

       :::image type="complex" source="./media/part1-installed-extension.png" alt-text="Ouvrir la page edge://extensions":::
          Page extensions installés montrant une extension chargée :::image-end:::

Pendant le développement, il est possible que vous deviez effectuer les tâches suivantes.
* Mettez à jour l’extension. Accédez à `edge://extensions` , puis sélectionnez **recharger** pour mettre à jour votre extension.  
* Supprimez l’extension de votre navigateur. Accédez à `edge://extensions` , puis sélectionnez `Remove` sur votre extension.