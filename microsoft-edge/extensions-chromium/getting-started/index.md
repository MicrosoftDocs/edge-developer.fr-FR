---
description: Découvrez les Chromium extensions et les concepts de base pour créer des extensions.
title: Microsoft Edge (Chromium) Concepts et architecture des extensions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, développement web, html, css, javascript, développeur, extensions
ms.openlocfilehash: 05732287bc1a782ed5830d5e7028cf5580f3b605
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397923"
---
# <a name="extension-concepts-and-architecture"></a>Concepts et architecture de l’extension  

Cet article fournit une brève présentation des concepts qui vous aident à créer une extension.  Pour comprendre Microsoft Edge les extensions \(Chromium\), suivez la marche à suivre pour comprendre le fonctionnement des navigateurs multi-onglets.  

## <a name="understand-how-browsers-work"></a>Comprendre le fonctionnement des navigateurs  

La liste suivante présente les informations utiles à comprendre avant de créer votre extension.  

1.  Chaque onglet de navigateur est isolé des autres onglets.  Chaque onglet s’exécute dans un thread distinct isolé des autres onglets et threads du navigateur.  
    
    :::image type="complex" source="./media/index-image1-browsertabs.png" alt-text="Un thread par onglet de navigateur" lightbox="./media/index-image1-browsertabs.png":::
       Un thread par onglet de navigateur  
    :::image-end:::  
    
1.  Chaque onglet gère une requête GET.  Chaque onglet utilise une URL pour obtenir un seul flux de données, qui est normalement un document HTML.  Cette page ou flux unique inclut des instructions telles que JavaScript incluent des balises, des références d’image, des références CSS, etc.  Toutes les ressources sont téléchargées sur cette page d’onglet, puis la page est restituer dans l’onglet.  
1.  La communication a lieu entre chaque onglet et un serveur distant.  Chaque onglet s’exécute dans un environnement isolé.  Chaque onglet est toujours connecté à Internet, mais chacun est isolé des autres onglets.  Un onglet peut exécuter JavaScript pour communiquer avec un serveur.  Le serveur est le serveur d’origine de la première requête GET entrée dans la barre d’URL de l’onglet.  
1.  Le modèle d’extension utilise un modèle de communication différent.  À l’exemple d’une page d’onglet, une extension s’exécute dans un thread individuel isolé des autres threads de page d’onglets.  Un onglet envoie des requêtes GET à des serveurs distants, puis restituer la page.  Toutefois, une extension fonctionne comme un serveur distant.  L’installation d’une extension dans un navigateur crée un serveur web autonome dans le navigateur.  L’extension est isolée de toutes les pages d’onglets.  
    
    :::image type="complex" source="./media/index-image3-upsidedown.png" alt-text="Les extensions utilisent un modèle de communication différent" lightbox="./media/index-image3-upsidedown.png":::
       Les extensions utilisent un modèle de communication différent  
    :::image-end:::  
    
## <a name="extension-architecture"></a>Architecture d'extension  

La liste suivante présente des informations utiles liées à l’architecture d’une extension.  

1.  Ensemble de serveurs web d’extension.  Une extension est un ensemble de ressources web.  Les ressources web sont similaires aux autres ressources que vous publiez sur les serveurs web .  Vous regroupez les ressources web dans un fichier zip lors de la création d’une extension.  
    
    Le fichier zip inclut les fichiers HTML, CSS, JavaScript et image.  Un fichier de plus est requis à la racine du fichier zip.  L’autre fichier est le fichier manifeste `manifest.json` nommé.  Le fichier manifeste est le plan de votre extension et inclut la version de votre extension, le titre, les autorisations nécessaires à l’utilisation de l’extension, etc.  
    
1.  Lancement du serveur d’extension.  Les serveurs Web contiennent votre offre groupée web.  Un navigateur navigue vers les URL sur le serveur et télécharge le fichier à restituer dans le navigateur.  Un navigateur navigue à l’aide de certificats, de fichiers de configuration, etc.  Si un fichier est spécifié, il est stocké à un `index.html` emplacement spécial sur le serveur web.  
    
    Lorsque vous utilisez une extension, la page d’onglets de votre navigateur obtient le bundle web de votre extension à l’aide du runtime d’extension.  Le runtime d’extension sert les fichiers à partir de l’URL , où est un identificateur unique affecté à `extension://{some-long-unique-identifier}/index.html` `{some-long-unique-identifier}` l’extension lors de l’installation.  Chaque extension utilise un identificateur unique différent.  Chaque identificateur pointe vers le bundle web installé dans votre navigateur.  
    
1.  Une extension peut communiquer avec les onglets et la barre d’outils du navigateur.  Une extension peut interagir avec la barre d’outils de votre navigateur.  Chaque extension gère l’exécution de pages d’onglets dans des threads distincts, et la manipulation DOM sur chaque page d’onglet est isolée.  Une extension utilise l’API d’extensions pour communiquer entre les pages d’extension et d’onglet.  L’API d’extensions fournit des fonctionnalités supplémentaires qui incluent la gestion des notifications, la gestion du stockage, etc.  
    
    Tout comme les serveurs web, une extension attend les notifications lorsque le navigateur est ouvert.  Les pages d’extension et d’onglet s’exécutent dans des threads isolés les uns des autres.  Pour permettre à une extension de fonctionner avec n’importe quelle page d’onglet, utilisez l’API d’extensions et définissez les autorisations dans le fichier manifeste.  
    
1.  Une extension fournit des autorisations d’accès au moment de l’installation.  Vous spécifiez les autorisations d’extension dans le `manifest.json` fichier.  Lorsqu’un utilisateur installe une extension, des informations sur les autorisations nécessaires s’affichent.  En fonction du type d’autorisation requis, l’extension peut extraire et utiliser des informations à partir du navigateur.  
    
## <a name="next-steps"></a>Étapes suivantes  

Pour plus d’informations sur la mise en place de votre extension, accédez [à Créer un didacticiel d’extension.][CreateAnExtensionPart1]  

<!-- links -->  

[CreateAnExtensionPart1]: ./part1-simple-extension.md "Créer un didacticiel d’extension - Partie 1 | Documents Microsoft"  
