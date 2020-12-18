---
ms.assetid: c4397525-b978-4dc2-89bc-2198b3069742
description: Découvrez comment empaqueter votre extension Microsoft Edge en un clin d’esprit avec ManifoldJS, l’outil d’ouverture de sources Node.js.
title: Utilisation de ManifoldJS pour conditionner les extensions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 151a8b2ababb25e0964a6fbc2696b5fdc059d084
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233369"
---
# <span data-ttu-id="a1295-104">Utilisation de ManifoldJS pour créer des packages AppX d’extension</span><span class="sxs-lookup"><span data-stu-id="a1295-104">Using ManifoldJS to create extension AppX packages</span></span>  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

<span data-ttu-id="a1295-105">ManifoldJS est un outil Node.js Open source qui vous permet de créer rapidement et facilement un package que vous pouvez utiliser pour la soumission à la boutique Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a1295-105">ManifoldJS is an open source Node.js tool that allows you to quickly and painlessly create a package that you can then use for submission to the Microsoft Store.</span></span>  

<span data-ttu-id="a1295-106">Si vous utilisez la messagerie native dans votre extension, vous devez ignorer l’article suivant et accéder à la [messagerie native dans Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) pour obtenir des instructions de Packaging.</span><span class="sxs-lookup"><span data-stu-id="a1295-106">If you use native messaging in your extension, you should skip the following article and go to [Native messaging in Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) for packaging instruction.</span></span>  

<span data-ttu-id="a1295-107">Avant de commencer, vous devez toujours consulter les articles suivants.</span><span class="sxs-lookup"><span data-stu-id="a1295-107">Before getting started, you will still need to read up on the following articles.</span></span>  

*   [<span data-ttu-id="a1295-108">Extensions dans le centre de développement Windows</span><span class="sxs-lookup"><span data-stu-id="a1295-108">Extensions in the Windows Dev Center</span></span>](./extensions-in-the-windows-dev-center.md)  
*   [<span data-ttu-id="a1295-109">Localisation des packages d’extension</span><span class="sxs-lookup"><span data-stu-id="a1295-109">Localizing extension packages</span></span>](./localizing-extension-packages.md)  

> [!NOTE]
> <span data-ttu-id="a1295-110">Le fait de soumettre une extension Microsoft Edge au Microsoft Store est actuellement une fonctionnalité restreinte.</span><span class="sxs-lookup"><span data-stu-id="a1295-110">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span>  <span data-ttu-id="a1295-111">Une fois que vous avez créé, emballé et testé votre poste, envoyez une demande sur notre [formulaire de soumission d’extension](https://developer.microsoft.com/microsoft-edge/extensions/requests).</span><span class="sxs-lookup"><span data-stu-id="a1295-111">Once you have created, packaged and tested your extension, please submit a request on our [extension submission form](https://developer.microsoft.com/microsoft-edge/extensions/requests).</span></span>  

## <span data-ttu-id="a1295-112">Installation de Node.js et ManifoldJS</span><span class="sxs-lookup"><span data-stu-id="a1295-112">Installing Node.js and ManifoldJS</span></span>  

<span data-ttu-id="a1295-113">Pour commencer, il vous suffit de procéder à l’installation [Node.js LTS](https://nodejs.org/en/download).</span><span class="sxs-lookup"><span data-stu-id="a1295-113">The first things you will need to do is install [Node.js LTS](https://nodejs.org/en/download).</span></span>  
<span data-ttu-id="a1295-114">Une fois que vous avez nœud, à partir d’une ligne de commande (PowerShell de préférence), exécutez la commande suivante pour installer ManifoldJS.</span><span class="sxs-lookup"><span data-stu-id="a1295-114">Once you have Node, from a command line (preferably PowerShell), run the following command to install ManifoldJS.</span></span>  

```shell
npm install -g manifoldjs
```  

<span data-ttu-id="a1295-115">Pour vérifier que vous avez correctement installé ManifoldJS, exécutez `manifoldjs` la commande à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="a1295-115">To verify that you have correctly installed ManifoldJS, run `manifoldjs` from the command line.</span></span> <span data-ttu-id="a1295-116">Si ManifoldJS n’est pas reconnu, ajoutez- `%APPDATA%\npm` le à vos variables PATH.</span><span class="sxs-lookup"><span data-stu-id="a1295-116">If ManifoldJS was not recognized, add `%APPDATA%\npm` to your PATH variables.</span></span>  

## <span data-ttu-id="a1295-117">Conditionnement avec ManifoldJS</span><span class="sxs-lookup"><span data-stu-id="a1295-117">Packaging with ManifoldJS</span></span>  

<span data-ttu-id="a1295-118">Pour démarrer le processus de création de packages, vous devez ouvrir une ligne de commande et remplacer les répertoires par un dossier qui sera la destination de votre extension empaquetée.</span><span class="sxs-lookup"><span data-stu-id="a1295-118">To start the packaging process, you will need to open a command line and change directories to a folder that will be the destination for your packaged extension.</span></span>  

<span data-ttu-id="a1295-119">Par exemple:</span><span class="sxs-lookup"><span data-stu-id="a1295-119">For example:</span></span>

```shell
cd C:\manifoldJSTest
```  

> [!NOTE]
> <span data-ttu-id="a1295-120">La `manifoldjs` commande émet dans le répertoire actif et remplace le contenu.</span><span class="sxs-lookup"><span data-stu-id="a1295-120">The `manifoldjs` command outputs in the current directory and overwrites content.</span></span>  

<span data-ttu-id="a1295-121">Maintenant que vous êtes dans votre dossier de destination, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="a1295-121">Now that you are in your destination folder, run the following command.</span></span>  

```shell
manifoldjs -l debug -p edgeextension -f edgeextension -m path\to\manifest.json
```  

<span data-ttu-id="a1295-122">La `mainifoldjs` commande peut être scindée en parties suivantes.</span><span class="sxs-lookup"><span data-stu-id="a1295-122">The `mainifoldjs` command can be broken down into the following parts.</span></span>  

:::row:::
   :::column span="1":::
      `-l debug`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="a1295-123">Change le niveau de journal pour `debug` obtenir une impression complète.</span><span class="sxs-lookup"><span data-stu-id="a1295-123">Changes the log level to `debug` to get a full print out.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-p edgeextension`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="a1295-124">Définit la seule plateforme sur laquelle exécuter la conversion `edgeextension` .</span><span class="sxs-lookup"><span data-stu-id="a1295-124">Sets the only platform to run the conversion on to `edgeextension`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-f edgeextension`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="a1295-125">Indique au programme que le format du manifeste est un `edgeextension` format et ne peut pas être utilisé en cas d’échec de la validation.</span><span class="sxs-lookup"><span data-stu-id="a1295-125">Tells the program that the format of the manifest is an `edgeextension` format and not to care if it fails validation.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-m \path\to\manifest.json`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="a1295-126">Chemin d’accès au manifeste d’extension que vous voulez convertir.</span><span class="sxs-lookup"><span data-stu-id="a1295-126">The path to the extension manifest that you want to convert.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="a1295-127">Après l’exécution de ManifoldJS, vous disposez d’un dossier avec le contenu suivant.</span><span class="sxs-lookup"><span data-stu-id="a1295-127">After ManifoldJS has finished running, you will have a folder with the following contents.</span></span>  

```text
┌ My Extension
└┬ edgeextension
 ├- generationInfo.json
 └┬ manifest
  ├- appxmanifest.xml
  ├┬ Assets
  |├- Square150x150Logo.png
  |├- Square44x44Logo.png
  |└- StoreLogo.png    
  └┬ Extension
   ├- manifest.json
   └- popup.html
```  
<!-- 
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
-->  

<span data-ttu-id="a1295-128">Le fichier generationInfo.jsest un journal généré en exécutant ManifoldJS et ne sera pas inclus dans votre package d’extension.</span><span class="sxs-lookup"><span data-stu-id="a1295-128">The generationInfo.json file is a log produced by running ManifoldJS and will not be included in your extension package.</span></span> <span data-ttu-id="a1295-129">Seul le contenu du `manifest` dossier sera empaqueté.</span><span class="sxs-lookup"><span data-stu-id="a1295-129">Only the contents of the `manifest` folder will be packaged.</span></span> <span data-ttu-id="a1295-130">Dans le dossier manifeste, le dossier Assets contient les images qui seront utilisées dans l’interface utilisateur de Microsoft Store et de l’interface utilisateur, tandis que le dossier d’extension comporte le contenu de votre extension.</span><span class="sxs-lookup"><span data-stu-id="a1295-130">Within the manifest folder, the Assets folder contains the images that will be used in the Windows and Microsoft Store UI, while the Extension folder has the contents of your extension within it.</span></span>  

<span data-ttu-id="a1295-131">À présent que vous avez les fichiers appropriés, vous devez modifier le fichier AppXManifest généré dans le `manifest` dossier.</span><span class="sxs-lookup"><span data-stu-id="a1295-131">Now that you have the correct files, you will need to edit the generated AppXManifest file within the `manifest` folder.</span></span> <span data-ttu-id="a1295-132">Si le manifest.jsde l’extension sur le fichier a une chaîne internationale pour le champ «nom», une fois ManifoldJS exécuté, le nom du dossier de calque le plus haut ne comporte pas de soulignements et ne comprend pas de «MSG».</span><span class="sxs-lookup"><span data-stu-id="a1295-132">If the extension’s manifest.json file has an internationalized string for the "name" field, once ManifoldJS is run, the most top layer folder’s name will have no underscores and include "MSG".</span></span>

<span data-ttu-id="a1295-133">Par exemple, un manifest.jssur un fichier avec le `"name"` champ suivant.</span><span class="sxs-lookup"><span data-stu-id="a1295-133">For example, a manifest.json file with the following `"name"` field.</span></span>  

```shell
"name" : "__MSG_appName__"
```  

<span data-ttu-id="a1295-134">aura un dossier de manifeste en `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest` .</span><span class="sxs-lookup"><span data-stu-id="a1295-134">will have a manifest folder that lives in `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest`.</span></span>  

<span data-ttu-id="a1295-135">Dans le fichier AppXManifest, vous devez effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="a1295-135">In the AppXManifest file, you will need to:</span></span>  

 *   <span data-ttu-id="a1295-136">Remplacez les champs d’identité requis et le champ PublisherDisplayName comme indiqué [ici](./creating-and-testing-extension-packages.md#app-identity-template-values).</span><span class="sxs-lookup"><span data-stu-id="a1295-136">Replace the required Identity fields and PublisherDisplayName field as outlined [here](./creating-and-testing-extension-packages.md#app-identity-template-values).</span></span> <span data-ttu-id="a1295-137">Notez que si vous n’utilisez que l’emballage à des fins de test ou de distribution d’entreprise, vous pouvez utiliser des valeurs d’espace réservé au lieu de vous inscrire pour un compte du centre de développement Windows.</span><span class="sxs-lookup"><span data-stu-id="a1295-137">Note that if you are only packaging for testing purposes or for enterprise distribution, you can use placeholder values instead of registering for a Windows Dev Center account.</span></span>  
 *   <span data-ttu-id="a1295-138">Remplacez les icônes d’espaces réservés dans le dossier Assets par des icônes pour votre extension de mêmes tailles (150 x 150, 50 x 50, 44 x 44) et des noms.</span><span class="sxs-lookup"><span data-stu-id="a1295-138">Replace the placeholder icons in the Assets folder with icons for your extension with the same sizes (150x150, 50x50, 44x44) and names.</span></span> <span data-ttu-id="a1295-139">Pour plus d’informations sur l’utilisation de ces icônes, voir le Guide de [conception](./../design.md#icons-for-packaging) .</span><span class="sxs-lookup"><span data-stu-id="a1295-139">See the [Design](./../design.md#icons-for-packaging) guide for information about where these icons are used.</span></span>  
 *   <span data-ttu-id="a1295-140">Si votre extension est localisée, suivez le guide complet [Localization Extensions Microsoft Edge](./localizing-extension-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="a1295-140">If your extension is localized, follow the entire [Localizing Microsoft Edge extensions](./localizing-extension-packages.md) guide.</span></span> <span data-ttu-id="a1295-141">S’il n’est pas localisé, lisez uniquement le [nom et la description du paramètre localization dans la section Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) .</span><span class="sxs-lookup"><span data-stu-id="a1295-141">If it is not localized, only read the [Localizing name and description in the Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) section.</span></span>  

<span data-ttu-id="a1295-142">Une fois votre `appxmanifest.xml` fichier trié, exécutez la commande suivante pour créer votre package.</span><span class="sxs-lookup"><span data-stu-id="a1295-142">Once your `appxmanifest.xml` file is sorted out, run the following command to create your package.</span></span>  

```shell
manifoldjs -l debug -p edgeextension package <EXTENSION NAME>\edgeextension\manifest\
```  

<span data-ttu-id="a1295-143">Votre package se trouvera désormais dans le dossier **package** situé dans le dossier edgeextension</span><span class="sxs-lookup"><span data-stu-id="a1295-143">Your package will now be in the **package** folder located within the edgeextension folder.</span></span> <span data-ttu-id="a1295-144">Pour plus d’informations sur la charger de votre nouveau package, voir la section [test](./creating-and-testing-extension-packages.md#testing-an-appx-package) de création et de test des packages d’extension.</span><span class="sxs-lookup"><span data-stu-id="a1295-144">For more information about how to sideload your new package, see [testing](./creating-and-testing-extension-packages.md#testing-an-appx-package) section of Creating and testing extension packages.</span></span>  

<span data-ttu-id="a1295-145">Une fois votre package testé, n’hésitez pas à soumettre une demande sur notre [formulaire de soumission de poste](https://aka.ms/extension-request) pour être envisagé pour la publication sur le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="a1295-145">Once your package has been tested, feel free to submit a request on our [extension submission form](https://aka.ms/extension-request) in order to be considered for publication to the Microsoft Store.</span></span>  
