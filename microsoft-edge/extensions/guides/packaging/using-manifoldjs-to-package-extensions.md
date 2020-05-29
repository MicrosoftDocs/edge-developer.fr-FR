---
ms.assetid: c4397525-b978-4dc2-89bc-2198b3069742
description: Découvrez comment empaqueter votre extension Microsoft Edge en un clin d’esprit avec ManifoldJS, l’outil open source de node. js.
title: Utilisation de ManifoldJS sur les extensions de package
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.custom: seodec18
ms.openlocfilehash: cca83a26c9f80eca6454e3b5b329f72a7491b6e2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565307"
---
# <span data-ttu-id="ef272-104">Utilisation de ManifoldJS pour créer des packages AppX d’extension</span><span class="sxs-lookup"><span data-stu-id="ef272-104">Using ManifoldJS to create extension AppX packages</span></span>  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

<span data-ttu-id="ef272-105">ManifoldJS est un outil nœud d’ouverture de nœud source. js qui vous permet de créer rapidement et facilement un package que vous pouvez utiliser pour la soumission à la boutique Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ef272-105">ManifoldJS is an open source Node.js tool that allows you to quickly and painlessly create a package that you can then use for submission to the Microsoft Store.</span></span>

<span data-ttu-id="ef272-106">Si vous utilisez la messagerie native dans votre extension, vous devez ignorer cette opération et accéder à la [messagerie native dans Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) pour obtenir des instructions de Packaging.</span><span class="sxs-lookup"><span data-stu-id="ef272-106">If you use native messaging in your extension, you should skip this and go to [Native messaging in Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) for packaging instruction.</span></span> 

<span data-ttu-id="ef272-107">Avant de commencer, vous devez toujours consulter les articles suivants:</span><span class="sxs-lookup"><span data-stu-id="ef272-107">Before getting started, you will still need to read up on the following articles:</span></span>

- [<span data-ttu-id="ef272-108">Extensions du centre de développement Windows</span><span class="sxs-lookup"><span data-stu-id="ef272-108">Extensions in the Windows Dev Center</span></span>](./extensions-in-the-windows-dev-center.md)
- [<span data-ttu-id="ef272-109">Localiser des packages d’extension</span><span class="sxs-lookup"><span data-stu-id="ef272-109">Localizing extension packages</span></span>](./localizing-extension-packages.md)

> [!NOTE]
> <span data-ttu-id="ef272-110">Le fait de soumettre une extension Microsoft Edge au Microsoft Store est actuellement une fonctionnalité restreinte.</span><span class="sxs-lookup"><span data-stu-id="ef272-110">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="ef272-111">Une fois que vous avez créé, emballé et testé votre poste, envoyez une demande sur notre [formulaire de soumission d’extension](https://aka.ms/extension-request).</span><span class="sxs-lookup"><span data-stu-id="ef272-111">Once you've created, packaged and tested your extension, please submit a request on our [extension submission form](https://aka.ms/extension-request).</span></span>


## <span data-ttu-id="ef272-112">Installation de node. js et de ManifoldJS</span><span class="sxs-lookup"><span data-stu-id="ef272-112">Installing Node.js and ManifoldJS</span></span>

<span data-ttu-id="ef272-113">Pour commencer, vous devez installer [node. js LTS](https://nodejs.org/en/download/).</span><span class="sxs-lookup"><span data-stu-id="ef272-113">The first things you'll need to do is install [Node.js LTS](https://nodejs.org/en/download/).</span></span>
<span data-ttu-id="ef272-114">Une fois que vous avez nœud, à partir d’une ligne de commande (PowerShell de préférence), exécutez la commande suivante pour installer ManifoldJS:</span><span class="sxs-lookup"><span data-stu-id="ef272-114">Once you have Node, from a command line (preferably PowerShell), run the following command to install ManifoldJS:</span></span>

`npm install -g manifoldjs`

<span data-ttu-id="ef272-115">Pour vérifier que vous avez correctement installé ManifoldJS, exécutez `manifoldjs` la commande à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="ef272-115">To verify that you've correctly installed ManifoldJS, run `manifoldjs` from the command line.</span></span> <span data-ttu-id="ef272-116">Si ManifoldJS n’est pas reconnu, ajoutez- `%APPDATA%\npm` le à vos variables PATH.</span><span class="sxs-lookup"><span data-stu-id="ef272-116">If ManifoldJS wasn't recognized, add `%APPDATA%\npm` to your PATH variables.</span></span>

## <span data-ttu-id="ef272-117">Conditionnement avec ManifoldJS</span><span class="sxs-lookup"><span data-stu-id="ef272-117">Packaging with ManifoldJS</span></span>

<span data-ttu-id="ef272-118">Pour démarrer le processus de création de packages, vous devez ouvrir une ligne de commande et changer de répertoires en un dossier qui sera la destination de votre extension empaquetée.</span><span class="sxs-lookup"><span data-stu-id="ef272-118">To start the packaging process, you'll need to open a command line and change directories to a folder that will be the destination for your packaged extension.</span></span>

<span data-ttu-id="ef272-119">Exemple:</span><span class="sxs-lookup"><span data-stu-id="ef272-119">For example:</span></span>

`cd C:\manifoldJSTest`

> [!NOTE]
> <span data-ttu-id="ef272-120">ManifoldJS s’affiche dans l’annuaire actuel et peut écraser le contenu.</span><span class="sxs-lookup"><span data-stu-id="ef272-120">ManifoldJS will output in the current directory and can overwrite content.</span></span>



<span data-ttu-id="ef272-121">Maintenant que vous êtes dans votre dossier de destination, exécutez la commande suivante:</span><span class="sxs-lookup"><span data-stu-id="ef272-121">Now that you're in your destination folder, run the following command:</span></span>

`manifoldjs -l debug -p edgeextension -f edgeextension -m <EXTENSION LOCATION>\manifest.json`


<span data-ttu-id="ef272-122">Cette commande peut être scindée comme suit:</span><span class="sxs-lookup"><span data-stu-id="ef272-122">This command can be broken down into the following parts:</span></span>
 -    <span data-ttu-id="ef272-123">**-l débogage**: remplace le niveau du journal par «Debug» pour obtenir une impression complète.</span><span class="sxs-lookup"><span data-stu-id="ef272-123">**-l debug**: Changes the log level to "debug" to get a full print out.</span></span>
 -    <span data-ttu-id="ef272-124">**-p edgeextension**: définit la seule plate-forme pour exécuter la conversion sur edgeextension.</span><span class="sxs-lookup"><span data-stu-id="ef272-124">**-p edgeextension**: Sets the only platform to run the conversion on to edgeextension.</span></span>
 -    <span data-ttu-id="ef272-125">**-f edgeextension**: indique au programme que le format du manifeste est un format edgeextension et ne peut pas s’en soucier en cas d’échec de la validation.</span><span class="sxs-lookup"><span data-stu-id="ef272-125">**-f edgeextension**: Tells the program that the format of the manifest is an edgeextension format and not to care if it fails validation.</span></span>
 -    <span data-ttu-id="ef272-126">**-m \ < emplacement de l’extension > \manifest.JSON**: le chemin d’accès au manifeste d’extension que vous voulez convertir.</span><span class="sxs-lookup"><span data-stu-id="ef272-126">**-m \<EXTENSION LOCATION>\manifest.json**: The path to the extension manifest that you want to convert.</span></span>


<span data-ttu-id="ef272-127">Après l’exécution de ManifoldJS, vous disposez d’un dossier contenant les informations suivantes:</span><span class="sxs-lookup"><span data-stu-id="ef272-127">After ManifoldJS has finished running, you'll have a folder with the following contents:</span></span>

    My Extension
        edgeextension
            generationInfo.json
            manifest
                   appxmanifest.xml
                Assets
                    Square150x150Logo.png
                    Square44x44Logo.png
                    StoreLogo.png    
                Extension
                    manifest.json
                    popup.html
                    ...
                ...

<span data-ttu-id="ef272-128">Le fichier generationInfo. JSON est un journal obtenu en exécutant ManifoldJS et ne sera pas inclus dans votre package d’extension.</span><span class="sxs-lookup"><span data-stu-id="ef272-128">The generationInfo.json file is a log produced by running ManifoldJS and won't be included in your extension package.</span></span> <span data-ttu-id="ef272-129">Seul le contenu du dossier **manifeste** sera empaqueté.</span><span class="sxs-lookup"><span data-stu-id="ef272-129">Only the contents of the **manifest** folder will be packaged.</span></span> <span data-ttu-id="ef272-130">Dans le dossier manifeste, le dossier Assets contient les images qui seront utilisées dans l’interface utilisateur de Microsoft Store et de l’interface utilisateur, tandis que le dossier d’extension comporte le contenu de votre extension.</span><span class="sxs-lookup"><span data-stu-id="ef272-130">Within the manifest folder, the Assets folder contains the images that will be used in the Windows and Microsoft Store UI, while the Extension folder has the contents of your extension within it.</span></span>


<span data-ttu-id="ef272-131">À présent que vous avez les fichiers appropriés, vous devez modifier le fichier AppXManifest généré dans le dossier du **manifeste** .</span><span class="sxs-lookup"><span data-stu-id="ef272-131">Now that you have the correct files, you'll need to edit the generated AppXManifest file within the **manifest** folder.</span></span> <span data-ttu-id="ef272-132">Si le fichier manifest. JSON de l’extension possède une chaîne internationale pour le champ «nom», une fois ManifoldJS exécuté, le nom du dossier de calque le plus haut ne comporte pas de soulignements et ne comprend pas de «MSG».</span><span class="sxs-lookup"><span data-stu-id="ef272-132">If the extension’s manifest.json file has an internationalized string for the "name" field, once ManifoldJS is run, the most top layer folder’s name will have no underscores and include "MSG".</span></span>

<span data-ttu-id="ef272-133">Par exemple, un fichier manifest. JSON contenant le `"name"` champ suivant:</span><span class="sxs-lookup"><span data-stu-id="ef272-133">For example, a manifest.json file with the following `"name"` field:</span></span>

`"name" : "__MSG_appName__"`

<span data-ttu-id="ef272-134">aura un dossier de manifeste en `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest` .</span><span class="sxs-lookup"><span data-stu-id="ef272-134">will have a manifest folder that lives in `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest`.</span></span>

<span data-ttu-id="ef272-135">Dans le fichier AppXManifest, vous devez effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="ef272-135">In the AppXManifest file, you'll need to:</span></span>
 -    <span data-ttu-id="ef272-136">Remplacez les champs d’identité requis et le champ PublisherDisplayName comme indiqué [ici](./creating-and-testing-extension-packages.md#app-identity-template-values).</span><span class="sxs-lookup"><span data-stu-id="ef272-136">Replace the required Identity fields and PublisherDisplayName field as outlined [here](./creating-and-testing-extension-packages.md#app-identity-template-values).</span></span> <span data-ttu-id="ef272-137">Notez que si vous n’utilisez que l’emballage à des fins de test ou de distribution d’entreprise, vous pouvez utiliser des valeurs d’espace réservé au lieu de vous inscrire pour un compte du centre de développement Windows.</span><span class="sxs-lookup"><span data-stu-id="ef272-137">Note that if you're only packaging for testing purposes or for enterprise distribution, you can use placeholder values instead of registering for a Windows Dev Center account.</span></span>
 -    <span data-ttu-id="ef272-138">Remplacez les icônes d’espaces réservés dans le dossier Assets par des icônes pour votre extension de mêmes tailles (150 x 150, 50 x 50, 44 x 44) et des noms.</span><span class="sxs-lookup"><span data-stu-id="ef272-138">Replace the placeholder icons in the Assets folder with icons for your extension with the same sizes (150x150, 50x50, 44x44) and names.</span></span> <span data-ttu-id="ef272-139">Pour plus d’informations sur l’utilisation de ces icônes, voir le Guide de [conception](./../design.md#icons-for-packaging) .</span><span class="sxs-lookup"><span data-stu-id="ef272-139">See the [Design](./../design.md#icons-for-packaging) guide for information about where these icons are used.</span></span>
 - <span data-ttu-id="ef272-140">Si votre extension est localisée, suivez le guide complet [Localization Extensions Microsoft Edge](./localizing-extension-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="ef272-140">If your extension is localized, follow the entire [Localizing Microsoft Edge extensions](./localizing-extension-packages.md) guide.</span></span> <span data-ttu-id="ef272-141">Si ce n’est pas le cas, lisez uniquement le [nom et la description de la localisation dans la section Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) .</span><span class="sxs-lookup"><span data-stu-id="ef272-141">If it isn't localized, only read the [Localizing name and description in the Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) section.</span></span>

<span data-ttu-id="ef272-142">Une fois votre fichier appxmanifest. xml trié, exécutez la commande suivante pour créer votre package:</span><span class="sxs-lookup"><span data-stu-id="ef272-142">Once your appxmanifest.xml file is sorted out, run the following command to create your package:</span></span>

`manifoldjs -l debug -p edgeextension package <EXTENSION NAME>\edgeextension\manifest\`

<span data-ttu-id="ef272-143">Votre package se trouvera désormais dans le dossier **package** situé dans le dossier edgeextension</span><span class="sxs-lookup"><span data-stu-id="ef272-143">Your package will now be in the **package** folder located within the edgeextension folder.</span></span> <span data-ttu-id="ef272-144">Pour plus d’informations sur la façon d’charger votre nouveau package, voir Création et test de la section de [test](./creating-and-testing-extension-packages.md#testing-an-appx-package) des packages d’extensions.</span><span class="sxs-lookup"><span data-stu-id="ef272-144">See Creating and testing extension packages' [testing](./creating-and-testing-extension-packages.md#testing-an-appx-package) section for info on how to sideload your new package.</span></span>

<span data-ttu-id="ef272-145">Une fois votre package testé, n’hésitez pas à soumettre une demande sur notre [formulaire de soumission de poste](https://aka.ms/extension-request) pour être envisagé pour la publication sur le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="ef272-145">Once your package has been tested, feel free to submit a request on our [extension submission form](https://aka.ms/extension-request) in order to be considered for publication to the Microsoft Store.</span></span>
