---
ms.assetid: c4397525-b978-4dc2-89bc-2198b3069742
description: Découvrez comment empaqueter votre extension Microsoft Edge en un clin d’esprit avec ManifoldJS, l’outil d’ouverture de sources Node.js.
title: Utilisation de ManifoldJS pour conditionner les extensions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.custom: seodec18
ms.openlocfilehash: 83aa57ae0e4ae302b1360be50e5158782b6fbb76
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986205"
---
# Utilisation de ManifoldJS pour créer des packages AppX d’extension  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

ManifoldJS est un outil Node.js Open source qui vous permet de créer rapidement et facilement un package que vous pouvez utiliser pour la soumission à la boutique Microsoft.  

Si vous utilisez la messagerie native dans votre extension, vous devez ignorer l’article suivant et accéder à la [messagerie native dans Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) pour obtenir des instructions de Packaging.  

Avant de commencer, vous devez toujours consulter les articles suivants.  

*   [Extensions dans le centre de développement Windows](./extensions-in-the-windows-dev-center.md)  
*   [Localisation des packages d’extension](./localizing-extension-packages.md)  

> [!NOTE]
> Le fait de soumettre une extension Microsoft Edge au Microsoft Store est actuellement une fonctionnalité restreinte.  Une fois que vous avez créé, emballé et testé votre poste, envoyez une demande sur notre [formulaire de soumission d’extension](https://developer.microsoft.com/microsoft-edge/extensions/requests).  

## Installation de Node.js et ManifoldJS  

Pour commencer, il vous suffit de procéder à l’installation [Node.js LTS](https://nodejs.org/en/download).  
Une fois que vous avez nœud, à partir d’une ligne de commande (PowerShell de préférence), exécutez la commande suivante pour installer ManifoldJS.  

```shell
npm install -g manifoldjs
```  

Pour vérifier que vous avez correctement installé ManifoldJS, exécutez `manifoldjs` la commande à partir de la ligne de commande. Si ManifoldJS n’est pas reconnu, ajoutez- `%APPDATA%\npm` le à vos variables PATH.  

## Conditionnement avec ManifoldJS  

Pour démarrer le processus de création de packages, vous devez ouvrir une ligne de commande et remplacer les répertoires par un dossier qui sera la destination de votre extension empaquetée.  

Par exemple:

```shell
cd C:\manifoldJSTest
```  

> [!NOTE]
> La `manifoldjs` commande émet dans le répertoire actif et remplace le contenu.  

Maintenant que vous êtes dans votre dossier de destination, exécutez la commande suivante.  

```shell
manifoldjs -l debug -p edgeextension -f edgeextension -m path\to\manifest.json
```  

La `mainifoldjs` commande peut être scindée en parties suivantes.  

:::row:::
   :::column span="1":::
      `-l debug`  
   :::column-end:::
   :::column span="2":::
      Change le niveau de journal pour `debug` obtenir une impression complète.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-p edgeextension`  
   :::column-end:::
   :::column span="2":::
      Définit la seule plateforme sur laquelle exécuter la conversion `edgeextension` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-f edgeextension`  
   :::column-end:::
   :::column span="2":::
      Indique au programme que le format du manifeste est un `edgeextension` format et ne peut pas être utilisé en cas d’échec de la validation.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-m \path\to\manifest.json`  
   :::column-end:::
   :::column span="2":::
      Chemin d’accès au manifeste d’extension que vous voulez convertir.  
   :::column-end:::
:::row-end:::  

Après l’exécution de ManifoldJS, vous disposez d’un dossier avec le contenu suivant.  

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

Le fichier generationInfo.jsest un journal généré en exécutant ManifoldJS et ne sera pas inclus dans votre package d’extension. Seul le contenu du `manifest` dossier sera empaqueté. Dans le dossier manifeste, le dossier Assets contient les images qui seront utilisées dans l’interface utilisateur de Microsoft Store et de l’interface utilisateur, tandis que le dossier d’extension comporte le contenu de votre extension.  

À présent que vous avez les fichiers appropriés, vous devez modifier le fichier AppXManifest généré dans le `manifest` dossier. Si le manifest.jsde l’extension sur le fichier a une chaîne internationale pour le champ «nom», une fois ManifoldJS exécuté, le nom du dossier de calque le plus haut ne comporte pas de soulignements et ne comprend pas de «MSG».

Par exemple, un manifest.jssur un fichier avec le `"name"` champ suivant.  

```shell
"name" : "__MSG_appName__"
```  

aura un dossier de manifeste en `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest` .  

Dans le fichier AppXManifest, vous devez effectuer les opérations suivantes:  

 *   Remplacez les champs d’identité requis et le champ PublisherDisplayName comme indiqué [ici](./creating-and-testing-extension-packages.md#app-identity-template-values). Notez que si vous n’utilisez que l’emballage à des fins de test ou de distribution d’entreprise, vous pouvez utiliser des valeurs d’espace réservé au lieu de vous inscrire pour un compte du centre de développement Windows.  
 *   Remplacez les icônes d’espaces réservés dans le dossier Assets par des icônes pour votre extension de mêmes tailles (150 x 150, 50 x 50, 44 x 44) et des noms. Pour plus d’informations sur l’utilisation de ces icônes, voir le Guide de [conception](./../design.md#icons-for-packaging) .  
 *   Si votre extension est localisée, suivez le guide complet [Localization Extensions Microsoft Edge](./localizing-extension-packages.md) . S’il n’est pas localisé, lisez uniquement le [nom et la description du paramètre localization dans la section Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) .  

Une fois votre `appxmanifest.xml` fichier trié, exécutez la commande suivante pour créer votre package.  

```shell
manifoldjs -l debug -p edgeextension package <EXTENSION NAME>\edgeextension\manifest\
```  

Votre package se trouvera désormais dans le dossier **package** situé dans le dossier edgeextension Pour plus d’informations sur la charger de votre nouveau package, voir la section [test](./creating-and-testing-extension-packages.md#testing-an-appx-package) de création et de test des packages d’extension.  

Une fois votre package testé, n’hésitez pas à soumettre une demande sur notre [formulaire de soumission de poste](https://aka.ms/extension-request) pour être envisagé pour la publication sur le Microsoft Store.  
