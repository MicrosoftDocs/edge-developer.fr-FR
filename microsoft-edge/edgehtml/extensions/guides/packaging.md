---
description: Découvrez comment vous pouvez packager votre extension.
title: 'Extensions : empaquetage'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/28/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: f3560505-e01f-47e5-9ad6-7a419f060fc2
keywords: edge, développement web, html, css, javascript, développeur
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 62c7858c38cf0c06e24c25938a885b10b391fd8f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398496"
---
# <a name="packaging-microsoft-edge-extensions"></a>Empaquetage des extensions Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Vous avez donc terminé votre extension et êtes prêt à la mettre en package. Vous vous demandez peut-être quelles sont les étapes suivantes à suivre pour les utilisateurs potentiels. Ce guide est destiné à vous apprendre à faire cela.  

Le guide d’empaquetage d’extension est complet en ce qu’il couvre tout ce que vous souhaitez savoir sur l’empaquetage, même les détails plus fin et détaillés. Si vous ne souhaitez pas découvrir tout ce qu’il faut savoir sur l’empaquetage de votre extension, vous êtes en chance. Nous avons ajouté la prise en charge des extensions à ManifoldJS, un outil de Node.js open source qui vous permet de ne plus empaquetage.  

> [!NOTE]
> L’envoi d’une extension Microsoft Edge au Microsoft Store est actuellement une fonctionnalité restreinte. [Faites-nous part](https://developer.microsoft.com/en-us/microsoft-edge/extensions/requests) de vos demandes pour faire partie du Microsoft Store et nous vous envisagerons pour une prochaine mise à jour.  

Utilisez le plan de processus ci-dessous pour mettre en avant votre jeu de création de packaging !  

## [<a name="extensions-in-the-windows-dev-center"></a>Extensions dans le centre de développement Windows](./packaging/extensions-in-the-windows-dev-center.md)  

Quel que soit l’itinéraire de création de package que vous choisissez, manuel ou ManifoldJS, la première étape consiste à vous inscrire à un compte de développeur Windows et à réserver le ou les noms de votre extension.  

Une fois cette procédure effectuée, vous pouvez passer à la création et au test de [packages d’extension](./packaging/creating-and-testing-extension-packages.md) pour découvrir comment les AppX sont créées et créer manuellement le package de votre extension, ou vous pouvez passer à l’itinéraire plus facile et passer à l’utilisation de [ManifoldJS](./packaging/using-ManifoldJS-to-package-extensions.md)pour créer des extensions de package.  

> [!NOTE]
> Une fois que vous nous avez atteint et que vous avez été approuvé pour que votre extension soit dans le Microsoft Store, consultez la liste de vérification de soumission [d’application.](https://docs.microsoft.com/windows/uwp/publish/app-submissions)  


## [<a name="creating-and-testing-extension-packages"></a>Création et test de packages d’extension](./packaging/creating-and-testing-extension-packages.md)  

Cette section du guide présente la création manuelle de packages d’extension une fois que vous avez installé votre compte de développeur Windows et réservé vos noms [d’extension.](./packaging/extensions-in-the-windows-Dev-Center.md) Si vous souhaitez obtenir plus d’informations sur la empaquetage d’une extension, lisez-la.  

Des informations sur la façon de tester et de déballer une extension empaqueté sont [également incluses.](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) Ces informations sont pertinentes même si vous avez pris l’itinéraire de packaging ManifoldJS.  

## [<a name="localizing-extension-packages"></a>Localisation des packages d’extension](./packaging/localizing-extension-packages.md)  

L’étape de localisation du package se situe entre la création de votre fichier appxmanifest.xml et l’exécution de la dernière commande pour créer un package de votre extension.  
Cela vous permet d’indiquer les langues que vos extensions prend en charge dans votre liste du Microsoft Store et la langue dans laquelle le nom de votre extension apparaît dans Windows.  

Vous pouvez passer à la description et au nom de la localité du [Microsoft Store](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) dans cette section du guide si votre extension ne prend pas en charge plusieurs langues.  

## [<a name="using-manifoldjs-to-package-extensions"></a>Utilisation de ManifoldJS pour conditionner les extensions](./packaging/using-ManifoldJS-to-package-extensions.md)  

L’itinéraire d’outils pour empaqueter votre extension, ManifoldJS empaquetage de votre extension en un clin d’œil avec un effort minimal de votre côté. Fournissez quelques ressources Windows/Microsoft Store après avoir rempli certaines propriétés AppXManifest et votre extension sera empaqueté en un rien de temps.  

Une fois que votre extension est empaqueté, consultez la section [de test](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) de création et de test de votre extension Microsoft Edge pour découvrir comment la recharger de manière test ou la décompresser.  

## [<a name="running-the-windows-app-certification-kit"></a>Exécution du Kit de certification des applications Windows](./packaging/running-the-windows-app-certification-kit.md)  

Une fois que vous avez une extension empaqueté, vous pouvez l’exécuter via le Kit de certification des applications Windows. Cela permet d’exécuter un certain nombre de tests sur votre package d’extension pour vous assurer qu’il est prêt pour le Microsoft Store.  
