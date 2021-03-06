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
# <a name="packaging-microsoft-edge-extensions"></a><span data-ttu-id="dd809-104">Empaquetage des extensions Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="dd809-104">Packaging Microsoft Edge extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="dd809-105">Vous avez donc terminé votre extension et êtes prêt à la mettre en package.</span><span class="sxs-lookup"><span data-stu-id="dd809-105">So you've finally completed your extension and are ready to package it up.</span></span> <span data-ttu-id="dd809-106">Vous vous demandez peut-être quelles sont les étapes suivantes à suivre pour les utilisateurs potentiels.</span><span class="sxs-lookup"><span data-stu-id="dd809-106">You might be wondering what the next steps are toward getting this in the hands of potential users.</span></span> <span data-ttu-id="dd809-107">Ce guide est destiné à vous apprendre à faire cela.</span><span class="sxs-lookup"><span data-stu-id="dd809-107">This guide is intended to teach you how to do just that.</span></span>  

<span data-ttu-id="dd809-108">Le guide d’empaquetage d’extension est complet en ce qu’il couvre tout ce que vous souhaitez savoir sur l’empaquetage, même les détails plus fin et détaillés.</span><span class="sxs-lookup"><span data-stu-id="dd809-108">The extension packaging guide is comprehensive in that it covers everything you'd want to know about packaging, even the finer, nitty gritty details.</span></span> <span data-ttu-id="dd809-109">Si vous ne souhaitez pas découvrir tout ce qu’il faut savoir sur l’empaquetage de votre extension, vous êtes en chance.</span><span class="sxs-lookup"><span data-stu-id="dd809-109">If you don't want to learn everything there is to know about packaging your extension, you're in luck.</span></span> <span data-ttu-id="dd809-110">Nous avons ajouté la prise en charge des extensions à ManifoldJS, un outil de Node.js open source qui vous permet de ne plus empaquetage.</span><span class="sxs-lookup"><span data-stu-id="dd809-110">We've added support for extensions to ManifoldJS, an open source Node.js tool that takes the majority of your packaging woes away.</span></span>  

> [!NOTE]
> <span data-ttu-id="dd809-111">L’envoi d’une extension Microsoft Edge au Microsoft Store est actuellement une fonctionnalité restreinte.</span><span class="sxs-lookup"><span data-stu-id="dd809-111">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="dd809-112">[Faites-nous part](https://developer.microsoft.com/en-us/microsoft-edge/extensions/requests) de vos demandes pour faire partie du Microsoft Store et nous vous envisagerons pour une prochaine mise à jour.</span><span class="sxs-lookup"><span data-stu-id="dd809-112">[Reach out to us](https://developer.microsoft.com/en-us/microsoft-edge/extensions/requests) with your requests to be a part of the Microsoft Store, and we’ll consider you for a future update.</span></span>  

<span data-ttu-id="dd809-113">Utilisez le plan de processus ci-dessous pour mettre en avant votre jeu de création de packaging !</span><span class="sxs-lookup"><span data-stu-id="dd809-113">Use the process outline below to map out your packaging adventure!</span></span>  

## [<a name="extensions-in-the-windows-dev-center"></a><span data-ttu-id="dd809-114">Extensions dans le centre de développement Windows</span><span class="sxs-lookup"><span data-stu-id="dd809-114">Extensions in the Windows Dev Center</span></span>](./packaging/extensions-in-the-windows-dev-center.md)  

<span data-ttu-id="dd809-115">Quel que soit l’itinéraire de création de package que vous choisissez, manuel ou ManifoldJS, la première étape consiste à vous inscrire à un compte de développeur Windows et à réserver le ou les noms de votre extension.</span><span class="sxs-lookup"><span data-stu-id="dd809-115">No matter which package creation route you choose, manual or ManifoldJS, the first step is registering for a Windows Developer account and reserving the name(s) of your extension.</span></span>  

<span data-ttu-id="dd809-116">Une fois cette procédure effectuée, vous pouvez passer à la création et au test de [packages d’extension](./packaging/creating-and-testing-extension-packages.md) pour découvrir comment les AppX sont créées et créer manuellement le package de votre extension, ou vous pouvez passer à l’itinéraire plus facile et passer à l’utilisation de [ManifoldJS](./packaging/using-ManifoldJS-to-package-extensions.md)pour créer des extensions de package.</span><span class="sxs-lookup"><span data-stu-id="dd809-116">Once you've done this, you can either move on to [Creating and testing extension packages](./packaging/creating-and-testing-extension-packages.md) to learn how AppXs are created and manually package your extension, or go the easier route and jump to [Using ManifoldJS to package extensions](./packaging/using-ManifoldJS-to-package-extensions.md).</span></span>  

> [!NOTE]
> <span data-ttu-id="dd809-117">Une fois que vous nous avez atteint et que vous avez été approuvé pour que votre extension soit dans le Microsoft Store, consultez la liste de vérification de soumission [d’application.](https://docs.microsoft.com/windows/uwp/publish/app-submissions)</span><span class="sxs-lookup"><span data-stu-id="dd809-117">Once you've reached out to us and have been approved to have your extension in the Microsoft Store, check out the [app submission checklist](https://docs.microsoft.com/windows/uwp/publish/app-submissions).</span></span>  


## [<a name="creating-and-testing-extension-packages"></a><span data-ttu-id="dd809-118">Création et test de packages d’extension</span><span class="sxs-lookup"><span data-stu-id="dd809-118">Creating and testing extension packages</span></span>](./packaging/creating-and-testing-extension-packages.md)  

<span data-ttu-id="dd809-119">Cette section du guide présente la création manuelle de packages d’extension une fois que vous avez installé votre compte de développeur Windows et réservé vos noms [d’extension.](./packaging/extensions-in-the-windows-Dev-Center.md)</span><span class="sxs-lookup"><span data-stu-id="dd809-119">This section of the guide walks through manual extension package creation once [you've set up your Windows Developer account and reserved your extension name(s)](./packaging/extensions-in-the-windows-Dev-Center.md).</span></span> <span data-ttu-id="dd809-120">Si vous souhaitez obtenir plus d’informations sur la empaquetage d’une extension, lisez-la.</span><span class="sxs-lookup"><span data-stu-id="dd809-120">If you're curious about the finer details of packaging an extension, give this a read.</span></span>  

<span data-ttu-id="dd809-121">Des informations sur la façon de tester et de déballer une extension empaqueté sont [également incluses.](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package)</span><span class="sxs-lookup"><span data-stu-id="dd809-121">Also included is info on how to [test and unpack a packaged extension](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package).</span></span> <span data-ttu-id="dd809-122">Ces informations sont pertinentes même si vous avez pris l’itinéraire de packaging ManifoldJS.</span><span class="sxs-lookup"><span data-stu-id="dd809-122">This info is relevant even if you've gone the ManifoldJS packaging route.</span></span>  

## [<a name="localizing-extension-packages"></a><span data-ttu-id="dd809-123">Localisation des packages d’extension</span><span class="sxs-lookup"><span data-stu-id="dd809-123">Localizing extension packages</span></span>](./packaging/localizing-extension-packages.md)  

<span data-ttu-id="dd809-124">L’étape de localisation du package se situe entre la création de votre fichier appxmanifest.xml et l’exécution de la dernière commande pour créer un package de votre extension.</span><span class="sxs-lookup"><span data-stu-id="dd809-124">The package localization step falls between creating your appxmanifest.xml file and running the final command to package your extension.</span></span>  
<span data-ttu-id="dd809-125">Cela vous permet d’indiquer les langues que vos extensions prend en charge dans votre liste du Microsoft Store et la langue dans laquelle le nom de votre extension apparaît dans Windows.</span><span class="sxs-lookup"><span data-stu-id="dd809-125">This allows you to indicate which languages your extensions supports in your Microsoft Store listing, and what language your extension's name appears in Windows.</span></span>  

<span data-ttu-id="dd809-126">Vous pouvez passer à la description et au nom de la localité du [Microsoft Store](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) dans cette section du guide si votre extension ne prend pas en charge plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="dd809-126">You can jump to [Localizing name and description for the Microsoft Store](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) in this section of the guide if your extension doesn't support multiple languages.</span></span>  

## [<a name="using-manifoldjs-to-package-extensions"></a><span data-ttu-id="dd809-127">Utilisation de ManifoldJS pour conditionner les extensions</span><span class="sxs-lookup"><span data-stu-id="dd809-127">Using ManifoldJS to package extensions</span></span>](./packaging/using-ManifoldJS-to-package-extensions.md)  

<span data-ttu-id="dd809-128">L’itinéraire d’outils pour empaqueter votre extension, ManifoldJS empaquetage de votre extension en un clin d’œil avec un effort minimal de votre côté.</span><span class="sxs-lookup"><span data-stu-id="dd809-128">The tool route for packaging your extension, ManifoldJS will package up your extension in a snap with minimal effort on your end.</span></span> <span data-ttu-id="dd809-129">Fournissez quelques ressources Windows/Microsoft Store après avoir rempli certaines propriétés AppXManifest et votre extension sera empaqueté en un rien de temps.</span><span class="sxs-lookup"><span data-stu-id="dd809-129">Provide a few Windows/Microsoft Store assets after filling out some AppXManifest properties and your extension will be packaged in no time.</span></span>  

<span data-ttu-id="dd809-130">Une fois que votre extension est empaqueté, consultez la section [de test](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) de création et de test de votre extension Microsoft Edge pour découvrir comment la recharger de manière test ou la décompresser.</span><span class="sxs-lookup"><span data-stu-id="dd809-130">Once your extension is packaged, see the [testing](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) section of Creating and testing your Microsoft Edge extension to learn how to sideload or unpack it.</span></span>  

## [<a name="running-the-windows-app-certification-kit"></a><span data-ttu-id="dd809-131">Exécution du Kit de certification des applications Windows</span><span class="sxs-lookup"><span data-stu-id="dd809-131">Running the Windows App Certification Kit</span></span>](./packaging/running-the-windows-app-certification-kit.md)  

<span data-ttu-id="dd809-132">Une fois que vous avez une extension empaqueté, vous pouvez l’exécuter via le Kit de certification des applications Windows.</span><span class="sxs-lookup"><span data-stu-id="dd809-132">Once you have a packaged extension, you can then run it through the Windows App Certification Kit.</span></span> <span data-ttu-id="dd809-133">Cela permet d’exécuter un certain nombre de tests sur votre package d’extension pour vous assurer qu’il est prêt pour le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="dd809-133">Doing so will run a number of tests on your extension package to ensure that it's ready for the Microsoft Store.</span></span>  
