---
description: Découvrez ce qu’est une extension de chrome et développez progressivement une extension d’affichage d’image complète incluant des options, une injection de contenu, des scripts en arrière-plan, un stockage et bien plus encore.
title: Premiers pas avec les extensions Microsoft Edge (chrome)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/29/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-chrome, développement Web, html, CSS, JavaScript, développeur, extensions
ms.openlocfilehash: c2b24dc3d5535beeef6a4255b6fe2439fb67b77d
ms.sourcegitcommit: 19ef1422733ef1fd051d2b4f0263ce191e8d67bc
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/31/2020
ms.locfileid: "10902835"
---
# Mise en route des extensions Microsoft Edge \ (chrome \)  

Si vous souhaitez accéder directement à la création de votre première extension, accédez à la première partie de la création d’une image de NASA de l’extension du jour.  

Si vous n’avez pas l’habitude des concepts et de l’architecture de l’extension, poursuivez votre lecture et découvrez les extensions.  Ces informations vous aideront à créer des extensions bien plus facilement, dans la mesure où vous comprenez les motivations et l’architecture des coulisses.  

## Créer une image de la NASA de l’extension jour  

Le package d’installation source d’extension est alors mentionné dans chaque section.  

*   [Créez une extension simple qui s’affiche avec la NASA image du jour.](part1-simple-extension.md)  
    *   Création d’un manifeste  
    *   Affecter des icônes d’extension  
    *   Affichage d’une fenêtre contextuelle  
    *   Exécutez votre extension localement dans votre navigateur \ (chargement hors Windows \)  

*   [Insérer dynamiquement une image de la NASA sous la balise du corps de la page](part2-content-scripts.md)  
    *   Créer du JavaScript qui insère un script de contenu dynamique  
    *   Définir dans le manifeste les pages qui reçoivent le script de contenu  
    *   Injecter le script de contenu par déclaration  
    *   Ajouter un bouton dans une fenêtre contextuelle pour envoyer un message au script de contenu  
    *   Recevoir un message au sein d’un script de contenu  

## Présentation du navigateur avant l’introduction des extensions  

### Chaque onglet de navigateur est isolé de chaque onglet différent  

Pour mieux comprendre ce qu’est une extension Microsoft Edge (chrome), nous devons tout d’abord comprendre ce qu’est un navigateur à plusieurs onglets, tel que Microsoft Edge.  Pour commencer, chaque onglet de navigateur s’exécute dans un thread individuel qui l’isole d’autres onglets (ou threads \).  

![Un thread par onglet de navigateur](media/index-image1-browsertabs.png)  

### Chaque onglet gère une requête GET  

Chaque onglet utilise essentiellement l’URL \ (également connue sous le nom de Uniform Resource Locator) pour obtenir un flux unique de données qui est généralement un document HTML.  Ce flux unique \ (ou page \) comprend souvent des instructions (comme JavaScript incluent des balises, des références d’image, des références CSS, etc.).  En fin de compte, toutes les ressources nécessaires sont téléchargées sur cette page d’onglets et une visualisation est généralement visible dans l’onglet du navigateur.  

### Toutes les communications de chaque onglet sont vers des serveurs distants  

La compréhension du fonctionnement de chaque onglet dans un environnement isolé implique que ces onglets sont isolés les uns des autres, mais pas la plus grande Internet.  En règle générale, ces onglets, qui exécutent JavaScript comme langage de programmation défini, communiquent avec le serveur par le biais du serveur d’origine pour cette première demande GET entrée dans la barre d’URL située en haut de l’onglet de navigateur.  

## Le modèle d’extension réactive tout ce qui se trouve à l’envers  

Une extension, comme la page d’onglets, s’exécute dans un thread individuel, qui est complètement isolé des threads de la page d’onglets.  Contrairement aux onglets pour lesquels il est généralement possible d’émettre une requête GET unique vers un serveur distant, puis d’afficher une visualisation de ces données dans le navigateur, l’extension, à l’inverse, est le serveur, qui se trouvait auparavant à l’autre extrémité de la connexion Internet réalisée à partir d’un onglet de navigateur.  

![Le modèle d’extension réactive le modèle de serveur à l’envers](media/index-image3-upsidedown.png)  

C’est vraiment important à comprendre.  Une fois que vous avez créé une extension et que vous l’avez installée dans votre navigateur, vous avez créé un serveur Web autonome qui vivre et respirer au sein de votre navigateur tout en étant toujours isolé de chaque page d’onglets qui s’exécutent dans le navigateur.  

### L’ensemble de serveurs Web d’extensions  

Qu’est-ce qu’une extension? Il s’agit d’une offre (ou désignée sous le nom de fichier zip) de ressources Web qui ne sont pas différentes de celles que le développeur Web publie sur un serveur Web.  

Ce fichier zip inclut HTML, CSS, JavaScript, images et tous les éléments nécessaires à la création d’une page Web.  Un fichier supplémentaire est toutefois requis à la racine de ce fichier zip et ce fichier est nommé `manifest.json` .  C’est le plan de votre extension qui inclut des éléments tels que la version de votre extension, le titre, les privilèges qu’il est nécessaire d’exécuter et bien plus encore.  

![Affichage des fichiers dans le fichier zip](media/index-image5-filemanager-view.png)  

### Lancement du serveur d’extension  

Lorsque vous effectuez un déploiement sur un serveur Web, ce serveur Web, qu’il s’agisse d’Apache, d’IIS, de NGINX ou d’une autre application, contient votre offre Web.  Lorsque le navigateur navigue vers une URL sur un serveur, le `index.html` fichier sur le serveur Web est téléchargé.  Navigateur navigué à l’aide de certificats, de fichiers de configuration, etc.  Le `index.html` fichier est stocké à un emplacement spécial sur le serveur Web.   Comment votre extension effectue-t-elle la même chose?  En particulier, en quoi l’onglet de votre navigateur peut-il accéder à ce fichier zip \ (votre extension)?  C’est ce que le runtime de l’extension effectue pour vous.  

L’extension dessert les fichiers de l’URL (Uniform Resource Locator) au nom `extension://{some-long-unique-identifier}/index.html` .  Le nom que vous mettez entre crochets `{some-long-unique-identifier}` est un identificateur unique attribué à l’extension que vous avez installée.  Cela signifie que si 10 extensions uniques sont installées sur votre navigateur, chacune d’elles possède un identificateur unique qui pointe vers le fichier zip \ (ou l’ensemble d’extensions \) installé dans votre navigateur.  

<!--![Unique URLS for Extensions](media/index-image4-uniqueurls.png)  -->  

<!--todo: add image for unique URLs  -->  

### Extensions gérer et communiquer avec les onglets et la barre d’outils du navigateur  

Les extensions interagissent avec la barre d’outils du navigateur, chacune d’elles peut gérer toutes les pages d’onglets actives de façon sécurisée et manipuler le DOM de toutes les pages d’onglets.  Le navigateur intégré au chrome est une API de message permettant de communiquer entre les extensions et les pages d’onglets pour que cela se produise harmonieusement.  Cette API, également connue sous le nom de l’API extensions, offre de nombreuses fonctionnalités, notamment la gestion des notifications, la gestion du stockage, etc.  

Tout comme les serveurs Web, les extensions peuvent exécuter en continu le fonctionnement de \ (ou du mode veille en attente de notifications \) tout le temps que le navigateur exécute.  Vous pouvez considérer une extension comme un Orchestrator pour le navigateur.  Là encore, l’extension s’exécute totalement indépendamment des pages d’onglets, mais par le biais de l’API d’extensions, et des autorisations d’activation accordées à l’extension, chaque extension peut contrôler quasiment tout ou partie des pages d’onglets qui s’exécutent dans le navigateur.  

### Les extensions fournissent une option d’inclusion du modèle de sécurité du moment de l’installation.  

Chaque extension, par le biais d’une déclaration dans le `manifest.json` fichier, permet à la personne d’installer l’extension de lui donner un niveau d’autorité différent.  Cette autorité de certification permet d’utiliser des extensions, lors de l’installation par un utilisateur, pour accepter la possibilité d’extraire des informations et de traiter ces données par le biais de l’extension.  

<!-- image links -->  

<!-- links -->  
