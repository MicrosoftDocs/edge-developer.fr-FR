---
ms.assetid: f3560505-e01f-47e5-9ad6-7a419f060fc2
description: Apprenez-en davantage sur la façon dont vous pouvez utiliser la messagerie native pour que votre extension puisse communiquer avec une application UWP.
title: Extensions-Packaging
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.openlocfilehash: 23c97f366db527cae2672d6ad46fa666583f6398
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565325"
---
# Création d’un package d’extensions Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Vous avez fini de terminer votre extension et vous êtes prêt à la préparer. Vous vous demandez peut-être quelles sont les étapes suivantes pour l’amener aux utilisateurs potentiels. Ce guide est destiné à vous apprendre à le faire.

Le Guide d’emballage de l’extension est une présentation complète qui couvre tout ce que vous aimeriez savoir sur l’emballage, même les plus petits détails et les plus petits. Si vous ne souhaitez pas découvrir tout ce que vous devez savoir sur la création d’un package pour votre extension, vous avez de la chance. Nous avons ajouté la prise en charge des extensions à ManifoldJS, un outil nœud Open source. js qui occupe la majeure partie de votre Packaging Woes.

> [!NOTE]
> Le fait de soumettre une extension Microsoft Edge au Microsoft Store est actuellement une fonctionnalité restreinte. Contactez [-nous](https://aka.ms/extension-request) pour obtenir vos demandes en tant que partie du Microsoft Store et nous vous enverrons une prochaine mise à jour.


Utilisez le plan de processus ci-dessous pour vous connecter à l’aventure de votre emballage.


## [Extensions du centre de développement Windows](./packaging/extensions-in-the-windows-dev-center.md)

Quel que soit l’itinéraire de création de package que vous choisissez, manuel ou ManifoldJS, la première étape consiste à s’inscrire pour obtenir un compte de développeur Windows et à réserver le ou les noms de votre extension.

Une fois cette opération effectuée, vous pouvez passer à la [création et au test de packages d’extension](./packaging/creating-and-testing-extension-packages.md) pour savoir comment AppXs est créé et empaqueter manuellement votre extension, ou vous pouvez accéder à l’itinéraire plus facilement et accéder à [l’utilisation de ManifoldJS dans les extensions de package](./packaging/using-ManifoldJS-to-package-extensions.md).

> [!NOTE]
> Une fois que vous vous avez contacté et que vous avez été approuvé pour pouvoir utiliser votre extension dans la boutique Microsoft, consultez la [liste de vérification de soumission d’application](https://docs.microsoft.com/windows/uwp/publish/app-submissions).


## [Création et test des packages d’extension](./packaging/creating-and-testing-extension-packages.md)

Cette section du guide décrit la création manuelle d’un package d’extension, une fois [que vous avez configuré votre compte de développeur Windows et que vous avez réservé le ou les noms d’extensions](./packaging/extensions-in-the-windows-Dev-Center.md). Si vous souhaitez obtenir des informations plus détaillées sur la création d’un package d’une extension, faites une lecture.

Vous trouverez également des informations sur la façon de [tester et de décompresser une extension empaquetée](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package). Ces informations sont pertinentes même si vous avez atteint la gamme d’emballage ManifoldJS.

## [Localiser des packages d’extension](./packaging/localizing-extension-packages.md)
L’étape de la localisation du package se limite à la création de votre fichier appxmanifest. xml et à l’exécution de la commande finale pour empaqueter votre extension.
Cela vous permet d’indiquer les langues prises en charge par vos extensions dans votre description dans le Windows Store, ainsi que la langue d’affichage du nom de votre extension dans Windows.

Si votre extension ne prend pas en charge plusieurs langues, vous pouvez accéder au [nom et à la description de la boutique Microsoft](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) dans cette section du guide.

## [Utilisation de ManifoldJS sur les extensions de package](./packaging/using-ManifoldJS-to-package-extensions.md)

L’itinéraire des outils d’empaquetage de votre extension, ManifoldJS vous permet de regrouper votre extension en un clin d’esprit avec un minimum d’efforts à la fin. Fournissez quelques ressources Windows/Microsoft Store après avoir rempli certaines propriétés de AppXManifest et votre extension sera empaquetée en tout temps.

Une fois votre extension empaquetée, voir la section [test](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) de création et de test de votre extension Microsoft Edge pour savoir comment charger ou la décompresser.


## [Exécution du kit de certification des applications Windows](./packaging/running-the-windows-app-certification-kit.md)

Une fois que vous avez une extension empaquetée, vous pouvez l’exécuter via le kit de certification des applications Windows. Cette opération permet d’exécuter un certain nombre de tests sur votre package d’extension pour vérifier qu’il est prêt pour le Microsoft Store.
