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
# <span data-ttu-id="bec71-104">Création d’un package d’extensions Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bec71-104">Packaging Microsoft Edge extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="bec71-105">Vous avez fini de terminer votre extension et vous êtes prêt à la préparer.</span><span class="sxs-lookup"><span data-stu-id="bec71-105">So you've finally completed your extension and are ready to package it up.</span></span> <span data-ttu-id="bec71-106">Vous vous demandez peut-être quelles sont les étapes suivantes pour l’amener aux utilisateurs potentiels.</span><span class="sxs-lookup"><span data-stu-id="bec71-106">You might be wondering what the next steps are toward getting this in the hands of potential users.</span></span> <span data-ttu-id="bec71-107">Ce guide est destiné à vous apprendre à le faire.</span><span class="sxs-lookup"><span data-stu-id="bec71-107">This guide is intended to teach you how to do just that.</span></span>

<span data-ttu-id="bec71-108">Le Guide d’emballage de l’extension est une présentation complète qui couvre tout ce que vous aimeriez savoir sur l’emballage, même les plus petits détails et les plus petits.</span><span class="sxs-lookup"><span data-stu-id="bec71-108">The extension packaging guide is comprehensive in that it covers everything you'd want to know about packaging, even the finer, nitty gritty details.</span></span> <span data-ttu-id="bec71-109">Si vous ne souhaitez pas découvrir tout ce que vous devez savoir sur la création d’un package pour votre extension, vous avez de la chance.</span><span class="sxs-lookup"><span data-stu-id="bec71-109">If you don't want to learn everything there is to know about packaging your extension, you're in luck.</span></span> <span data-ttu-id="bec71-110">Nous avons ajouté la prise en charge des extensions à ManifoldJS, un outil nœud Open source. js qui occupe la majeure partie de votre Packaging Woes.</span><span class="sxs-lookup"><span data-stu-id="bec71-110">We've added support for extensions to ManifoldJS, an open source Node.js tool that takes the majority of your packaging woes away.</span></span>

> [!NOTE]
> <span data-ttu-id="bec71-111">Le fait de soumettre une extension Microsoft Edge au Microsoft Store est actuellement une fonctionnalité restreinte.</span><span class="sxs-lookup"><span data-stu-id="bec71-111">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="bec71-112">Contactez [-nous](https://aka.ms/extension-request) pour obtenir vos demandes en tant que partie du Microsoft Store et nous vous enverrons une prochaine mise à jour.</span><span class="sxs-lookup"><span data-stu-id="bec71-112">[Reach out to us](https://aka.ms/extension-request) with your requests to be a part of the Microsoft Store, and we’ll consider you for a future update.</span></span>


<span data-ttu-id="bec71-113">Utilisez le plan de processus ci-dessous pour vous connecter à l’aventure de votre emballage.</span><span class="sxs-lookup"><span data-stu-id="bec71-113">Use the process outline below to map out your packaging adventure!</span></span>


## [<span data-ttu-id="bec71-114">Extensions du centre de développement Windows</span><span class="sxs-lookup"><span data-stu-id="bec71-114">Extensions in the Windows Dev Center</span></span>](./packaging/extensions-in-the-windows-dev-center.md)

<span data-ttu-id="bec71-115">Quel que soit l’itinéraire de création de package que vous choisissez, manuel ou ManifoldJS, la première étape consiste à s’inscrire pour obtenir un compte de développeur Windows et à réserver le ou les noms de votre extension.</span><span class="sxs-lookup"><span data-stu-id="bec71-115">No matter which package creation route you choose, manual or ManifoldJS, the first step is registering for a Windows Developer account and reserving the name(s) of your extension.</span></span>

<span data-ttu-id="bec71-116">Une fois cette opération effectuée, vous pouvez passer à la [création et au test de packages d’extension](./packaging/creating-and-testing-extension-packages.md) pour savoir comment AppXs est créé et empaqueter manuellement votre extension, ou vous pouvez accéder à l’itinéraire plus facilement et accéder à [l’utilisation de ManifoldJS dans les extensions de package](./packaging/using-ManifoldJS-to-package-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="bec71-116">Once you've done this, you can either move on to [Creating and testing extension packages](./packaging/creating-and-testing-extension-packages.md) to learn how AppXs are created and manually package your extension, or go the easier route and jump to [Using ManifoldJS to package extensions](./packaging/using-ManifoldJS-to-package-extensions.md).</span></span>

> [!NOTE]
> <span data-ttu-id="bec71-117">Une fois que vous vous avez contacté et que vous avez été approuvé pour pouvoir utiliser votre extension dans la boutique Microsoft, consultez la [liste de vérification de soumission d’application](https://docs.microsoft.com/windows/uwp/publish/app-submissions).</span><span class="sxs-lookup"><span data-stu-id="bec71-117">Once you've reached out to us and have been approved to have your extension in the Microsoft Store, check out the [app submission checklist](https://docs.microsoft.com/windows/uwp/publish/app-submissions).</span></span>


## [<span data-ttu-id="bec71-118">Création et test des packages d’extension</span><span class="sxs-lookup"><span data-stu-id="bec71-118">Creating and testing extension packages</span></span>](./packaging/creating-and-testing-extension-packages.md)

<span data-ttu-id="bec71-119">Cette section du guide décrit la création manuelle d’un package d’extension, une fois [que vous avez configuré votre compte de développeur Windows et que vous avez réservé le ou les noms d’extensions](./packaging/extensions-in-the-windows-Dev-Center.md).</span><span class="sxs-lookup"><span data-stu-id="bec71-119">This section of the guide walks through manual extension package creation once [you've set up your Windows Developer account and reserved your extension name(s)](./packaging/extensions-in-the-windows-Dev-Center.md).</span></span> <span data-ttu-id="bec71-120">Si vous souhaitez obtenir des informations plus détaillées sur la création d’un package d’une extension, faites une lecture.</span><span class="sxs-lookup"><span data-stu-id="bec71-120">If you're curious about the finer details of packaging an extension, give this a read.</span></span>

<span data-ttu-id="bec71-121">Vous trouverez également des informations sur la façon de [tester et de décompresser une extension empaquetée](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package).</span><span class="sxs-lookup"><span data-stu-id="bec71-121">Also included is info on how to [test and unpack a packaged extension](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package).</span></span> <span data-ttu-id="bec71-122">Ces informations sont pertinentes même si vous avez atteint la gamme d’emballage ManifoldJS.</span><span class="sxs-lookup"><span data-stu-id="bec71-122">This info is relevant even if you've gone the ManifoldJS packaging route.</span></span>

## [<span data-ttu-id="bec71-123">Localiser des packages d’extension</span><span class="sxs-lookup"><span data-stu-id="bec71-123">Localizing extension packages</span></span>](./packaging/localizing-extension-packages.md)
<span data-ttu-id="bec71-124">L’étape de la localisation du package se limite à la création de votre fichier appxmanifest. xml et à l’exécution de la commande finale pour empaqueter votre extension.</span><span class="sxs-lookup"><span data-stu-id="bec71-124">The package localization step falls between creating your appxmanifest.xml file and running the final command to package your extension.</span></span>
<span data-ttu-id="bec71-125">Cela vous permet d’indiquer les langues prises en charge par vos extensions dans votre description dans le Windows Store, ainsi que la langue d’affichage du nom de votre extension dans Windows.</span><span class="sxs-lookup"><span data-stu-id="bec71-125">This allows you to indicate which languages your extensions supports in your Microsoft Store listing, and what language your extension's name appears in Windows.</span></span>

<span data-ttu-id="bec71-126">Si votre extension ne prend pas en charge plusieurs langues, vous pouvez accéder au [nom et à la description de la boutique Microsoft](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) dans cette section du guide.</span><span class="sxs-lookup"><span data-stu-id="bec71-126">You can jump to [Localizing name and description for the Microsoft Store](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) in this section of the guide if your extension doesn't support multiple languages.</span></span>

## [<span data-ttu-id="bec71-127">Utilisation de ManifoldJS sur les extensions de package</span><span class="sxs-lookup"><span data-stu-id="bec71-127">Using ManifoldJS to package extensions</span></span>](./packaging/using-ManifoldJS-to-package-extensions.md)

<span data-ttu-id="bec71-128">L’itinéraire des outils d’empaquetage de votre extension, ManifoldJS vous permet de regrouper votre extension en un clin d’esprit avec un minimum d’efforts à la fin.</span><span class="sxs-lookup"><span data-stu-id="bec71-128">The tool route for packaging your extension, ManifoldJS will package up your extension in a snap with minimal effort on your end.</span></span> <span data-ttu-id="bec71-129">Fournissez quelques ressources Windows/Microsoft Store après avoir rempli certaines propriétés de AppXManifest et votre extension sera empaquetée en tout temps.</span><span class="sxs-lookup"><span data-stu-id="bec71-129">Provide a few Windows/Microsoft Store assets after filling out some AppXManifest properties and your extension will be packaged in no time.</span></span>

<span data-ttu-id="bec71-130">Une fois votre extension empaquetée, voir la section [test](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) de création et de test de votre extension Microsoft Edge pour savoir comment charger ou la décompresser.</span><span class="sxs-lookup"><span data-stu-id="bec71-130">Once your extension is packaged, see the [testing](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) section of Creating and testing your Microsoft Edge extension to learn how to sideload or unpack it.</span></span>


## [<span data-ttu-id="bec71-131">Exécution du kit de certification des applications Windows</span><span class="sxs-lookup"><span data-stu-id="bec71-131">Running the Windows App Certification Kit</span></span>](./packaging/running-the-windows-app-certification-kit.md)

<span data-ttu-id="bec71-132">Une fois que vous avez une extension empaquetée, vous pouvez l’exécuter via le kit de certification des applications Windows.</span><span class="sxs-lookup"><span data-stu-id="bec71-132">Once you have a packaged extension, you can then run it through the Windows App Certification Kit.</span></span> <span data-ttu-id="bec71-133">Cette opération permet d’exécuter un certain nombre de tests sur votre package d’extension pour vérifier qu’il est prêt pour le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="bec71-133">Doing so will run a number of tests on your extension package to ensure that it's ready for the Microsoft Store.</span></span>
