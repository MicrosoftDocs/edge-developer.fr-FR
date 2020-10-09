---
description: Apprenez-en davantage sur les extensions de chrome et sur les principaux concepts de création d’extensions.
title: Architecture et concepts des extensions Microsoft Edge (chrome)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/01/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: Edge-chrome, développement Web, html, CSS, JavaScript, développeur, extensions
ms.openlocfilehash: 8ffdd19e1a1e36a4d10fdd80bd7dd5654d543527
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104727"
---
# Architecture et concepts de l’extension

Cet article fournit une présentation des concepts qui vous aideront lors du développement d’extensions. Pour mieux comprendre les extensions Microsoft Edge \ (chrome), nous avons tout d’abord expliqué le fonctionnement des navigateurs à plusieurs onglets.


## Comprendre le fonctionnement des navigateurs

La liste suivante présente des informations utiles à comprendre avant de créer votre extension.

1.  Chaque onglet de navigateur est isolé de chaque onglet.  Chaque onglet s’exécute dans son propre thread, qui est isolément des autres onglets et threads du navigateur.

    ![Un thread par onglet de navigateur](media/index-image1-browsertabs.png)  

2.  Chaque onglet gère une requête GET.  Chaque onglet utilise une URL pour obtenir un flux unique de données, qui est généralement un document HTML.  Ce flux ou cette page unique inclut des instructions telles que des balises JavaScript, des références d’image, des références CSS, etc.  Toutes les ressources sont téléchargées sur la page d’onglets, et la page est affichée dans l’onglet.  

3.  La communication se produit entre chaque onglet et chaque serveur distant.  Chaque onglet s’exécute dans un environnement isolé. Ils sont toujours connectés à Internet, mais ils sont isolés d’autres onglets.  Les onglets pourront exécuter JavaScript pour communiquer avec des serveurs. Il s’agit du serveur d’origine de la première demande GET entrée dans la barre d’URL de l’onglet.  

4.  Le modèle d’extension utilise un modèle de communication différent.  À l’instar des pages d’onglets, les extensions s’exécutent dans des threads individuels isolés de tous les threads de la page d’onglets.  Les onglets émettent des demandes GET uniques vers des serveurs distants, puis génèrent le rendu de la page. Toutefois, les extensions sont similaires à un serveur distant. L’installation d’extensions dans votre navigateur crée un serveur Web autonome dans le navigateur. L’extension est isolée de toutes les pages d’onglets.  

    ![Les extensions utilisent un modèle de communication différent](media/index-image3-upsidedown.png)  

## Architecture d’extension

La liste suivante présente des informations utiles relatives à l’architecture d’une extension.  

1.  Extension du serveur Web d’extension.  Une extension est un ensemble de ressources Web. Ces ressources Web sont similaires à d’autres ressources que les développeurs Web publient sur des serveurs Web. Les développeurs regroupent ces ressources Web dans un fichier zip lors de la création d’une extension.
    
    Le fichier zip contient les fichiers HTML, CSS, JavaScript et image.  Un fichier supplémentaire est requis à la racine du fichier zip. Ce fichier est le fichier manifeste et est nommé `manifest.json` .  Il s’agit du plan de votre extension et inclut la version de votre extension, le titre, les autorisations nécessaires à l’exécution de l’extension, etc.

2.  Lancement du serveur d’extension.  Les serveurs Web contiennent votre offre Web. Les navigateurs permettent d’accéder aux URL du serveur et de télécharger le fichier à afficher dans le navigateur. Les navigateurs naviguent à l’aide des certificats, des fichiers de configuration, etc.  S’il existe un `index.html` fichier, il est stocké à un emplacement spécial sur le serveur Web.  

    Lorsque nous utilisons des extensions, la page d’onglets de votre navigateur accède au Bundle Web de votre extension à l’aide de l’extension Runtime.  Le runtime de l’extension dessert les fichiers de l’URL `extension://{some-long-unique-identifier}/index.html` qui `{some-long-unique-identifier}` est un identificateur unique attribué à l’extension lorsqu’il est installé.  Chaque extension utilise un identificateur unique différent. Chaque identificateur pointe vers le groupe Web qui est installé dans votre navigateur.   

3.  Les extensions peuvent communiquer avec des onglets et la barre d’outils du navigateur.   Les extensions peuvent interagir avec la barre d’outils de votre navigateur. Chaque extension gère l’exécution des pages d’onglets dans des threads séparés, et la manipulation DOM sur chaque page d’onglet est isolée.  Les extensions utilisent l’API extensions pour communiquer entre les pages de l’extension et de l’onglet.  Cette API d’extension fournit des fonctionnalités supplémentaires, notamment la gestion des notifications, la gestion du stockage, etc.  

    Tout comme les serveurs Web, les extensions attendent des notifications lorsque le navigateur est ouvert.  Les extensions et pages d’onglet s’exécutent dans des threads isolés les uns des autres. Toutefois, les développeurs peuvent utiliser l’API extensions et les autorisations dans le fichier manifeste pour permettre à une extension d’utiliser n’importe quelle page d’onglet.  

4. Les extensions fournissent des autorisations d’inclusion au moment de l’installation.  Les autorisations d’extension sont spécifiées par le développeur du `manifest.json` fichier. Lors de l’installation d’extensions, les utilisateurs ont accès à des informations sur les autorisations requises pour s’exécuter sur l’extension. En fonction du type d’autorisation requis, l’extension pourra extraire et utiliser des informations du navigateur.


## Étapes suivantes

 Pour plus d’informations sur la mise en route des extensions, voir [créer un didacticiel d’extension][CreateAnExtensionPart1]. 



<!-- image links -->  

<!-- links -->  

[CreateAnExtensionPart1]: ./part1-simple-extension.md "Didacticiel de création d’une extension-partie 1 | Documents Microsoft"  