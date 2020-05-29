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
# Utilisation de ManifoldJS pour créer des packages AppX d’extension  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

ManifoldJS est un outil nœud d’ouverture de nœud source. js qui vous permet de créer rapidement et facilement un package que vous pouvez utiliser pour la soumission à la boutique Microsoft.

Si vous utilisez la messagerie native dans votre extension, vous devez ignorer cette opération et accéder à la [messagerie native dans Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) pour obtenir des instructions de Packaging. 

Avant de commencer, vous devez toujours consulter les articles suivants:

- [Extensions du centre de développement Windows](./extensions-in-the-windows-dev-center.md)
- [Localiser des packages d’extension](./localizing-extension-packages.md)

> [!NOTE]
> Le fait de soumettre une extension Microsoft Edge au Microsoft Store est actuellement une fonctionnalité restreinte. Une fois que vous avez créé, emballé et testé votre poste, envoyez une demande sur notre [formulaire de soumission d’extension](https://aka.ms/extension-request).


## Installation de node. js et de ManifoldJS

Pour commencer, vous devez installer [node. js LTS](https://nodejs.org/en/download/).
Une fois que vous avez nœud, à partir d’une ligne de commande (PowerShell de préférence), exécutez la commande suivante pour installer ManifoldJS:

`npm install -g manifoldjs`

Pour vérifier que vous avez correctement installé ManifoldJS, exécutez `manifoldjs` la commande à partir de la ligne de commande. Si ManifoldJS n’est pas reconnu, ajoutez- `%APPDATA%\npm` le à vos variables PATH.

## Conditionnement avec ManifoldJS

Pour démarrer le processus de création de packages, vous devez ouvrir une ligne de commande et changer de répertoires en un dossier qui sera la destination de votre extension empaquetée.

Exemple:

`cd C:\manifoldJSTest`

> [!NOTE]
> ManifoldJS s’affiche dans l’annuaire actuel et peut écraser le contenu.



Maintenant que vous êtes dans votre dossier de destination, exécutez la commande suivante:

`manifoldjs -l debug -p edgeextension -f edgeextension -m <EXTENSION LOCATION>\manifest.json`


Cette commande peut être scindée comme suit:
 -    **-l débogage**: remplace le niveau du journal par «Debug» pour obtenir une impression complète.
 -    **-p edgeextension**: définit la seule plate-forme pour exécuter la conversion sur edgeextension.
 -    **-f edgeextension**: indique au programme que le format du manifeste est un format edgeextension et ne peut pas s’en soucier en cas d’échec de la validation.
 -    **-m \ < emplacement de l’extension > \manifest.JSON**: le chemin d’accès au manifeste d’extension que vous voulez convertir.


Après l’exécution de ManifoldJS, vous disposez d’un dossier contenant les informations suivantes:

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

Le fichier generationInfo. JSON est un journal obtenu en exécutant ManifoldJS et ne sera pas inclus dans votre package d’extension. Seul le contenu du dossier **manifeste** sera empaqueté. Dans le dossier manifeste, le dossier Assets contient les images qui seront utilisées dans l’interface utilisateur de Microsoft Store et de l’interface utilisateur, tandis que le dossier d’extension comporte le contenu de votre extension.


À présent que vous avez les fichiers appropriés, vous devez modifier le fichier AppXManifest généré dans le dossier du **manifeste** . Si le fichier manifest. JSON de l’extension possède une chaîne internationale pour le champ «nom», une fois ManifoldJS exécuté, le nom du dossier de calque le plus haut ne comporte pas de soulignements et ne comprend pas de «MSG».

Par exemple, un fichier manifest. JSON contenant le `"name"` champ suivant:

`"name" : "__MSG_appName__"`

aura un dossier de manifeste en `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest` .

Dans le fichier AppXManifest, vous devez effectuer les opérations suivantes:
 -    Remplacez les champs d’identité requis et le champ PublisherDisplayName comme indiqué [ici](./creating-and-testing-extension-packages.md#app-identity-template-values). Notez que si vous n’utilisez que l’emballage à des fins de test ou de distribution d’entreprise, vous pouvez utiliser des valeurs d’espace réservé au lieu de vous inscrire pour un compte du centre de développement Windows.
 -    Remplacez les icônes d’espaces réservés dans le dossier Assets par des icônes pour votre extension de mêmes tailles (150 x 150, 50 x 50, 44 x 44) et des noms. Pour plus d’informations sur l’utilisation de ces icônes, voir le Guide de [conception](./../design.md#icons-for-packaging) .
 - Si votre extension est localisée, suivez le guide complet [Localization Extensions Microsoft Edge](./localizing-extension-packages.md) . Si ce n’est pas le cas, lisez uniquement le [nom et la description de la localisation dans la section Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) .

Une fois votre fichier appxmanifest. xml trié, exécutez la commande suivante pour créer votre package:

`manifoldjs -l debug -p edgeextension package <EXTENSION NAME>\edgeextension\manifest\`

Votre package se trouvera désormais dans le dossier **package** situé dans le dossier edgeextension Pour plus d’informations sur la façon d’charger votre nouveau package, voir Création et test de la section de [test](./creating-and-testing-extension-packages.md#testing-an-appx-package) des packages d’extensions.

Une fois votre package testé, n’hésitez pas à soumettre une demande sur notre [formulaire de soumission de poste](https://aka.ms/extension-request) pour être envisagé pour la publication sur le Microsoft Store.
