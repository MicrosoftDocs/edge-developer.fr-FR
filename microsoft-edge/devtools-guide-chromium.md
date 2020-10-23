---
description: Découvrir les outils de développement Microsoft Edge (chrome)
title: Outils de développement Microsoft Edge (chrome)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 9f035df5bc80aa6a1df0464eb326e4185e2205d2
ms.sourcegitcommit: 6e2b26d41a0aa56ac34e6edc7dddd852ddb415b1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/23/2020
ms.locfileid: "11133903"
---
# Outils de développement Microsoft Edge (chrome)  

Microsoft Edge a adopté le projet de source d’ouverture de chrome pour créer une meilleure compatibilité Web et moins de fragmentation pour différentes plateformes Web sous-jacentes.  Cette modification doit simplifier la création et le test de vos sites Web dans Microsoft Edge et garantir que chacune fonctionne comme prévu, même en cas d’affichage dans un autre navigateur de chrome, tel que Google Chrome, Vivaldi, Opera ou en 3D.  

Dans la mesure où le Web s’est passé dans une utilisation importante de types d’appareil, la complexité et la surcharge inhérentes au test des sites Web ont été éclatées. Étant donné que les développeurs Web (en particulier, les petites entreprises doivent effectuer des tests sur autant de systèmes différents), il est possible que vous puissiez constater que les sites fonctionnent correctement sur tous les types d’appareil et tous les navigateurs.  À présent que Microsoft Edge est basé sur chrome, l’équipe Microsoft Edge a simplifié la matrice en alignant la plateforme Web Microsoft Edge avec d’autres navigateurs de chrome et fourni une meilleure interface d’outils de développement, à l’intérieur du navigateur et aux autres outils de développement que vous utilisez tous les jours de la semaine (par exemple, Visual Studio code \).  

Si vous examinez Microsoft Edge et que vous développez essentiellement dans un navigateur en chrome, il est préférable de vous sentir à la maison.  Les outils de développement Microsoft Edge \ (chrome \) fonctionnent de la même manière que les outils de développement que vous connaissez et utilisez déjà.  Pour plus d’informations, reportez-vous à [la section nouveautés de Microsoft Edge (chrome) devtools][DevtoolsGuideChromiumWhatsNewIndex].  

:::image type="complex" source="./devtools-guide-chromium/media/devtools.png" alt-text="DevTools Microsoft Edge (chrome)":::
   DevTools Microsoft Edge (chrome)  
:::image-end:::  

Si vous découvrez la nouvelle version de Microsoft Edge et que vous avez déjà développés dans Microsoft Edge \ (EdgeHTML), vous disposez maintenant de nouveaux outils très pratiques qui vous permettent de créer et tester plus facilement vos sites Web dans Microsoft Edge.  

## Ouvrir le DevTools  

Si vous n’avez jamais utilisé le DevTools auparavant, les outils de développement Microsoft Edge sont un ensemble d’outils intégrés directement dans le navigateur Microsoft Edge.  Avec ces DevTools, vous pouvez effectuer les opérations suivantes.  

*   Inspecter et apporter des modifications à votre site Web HTML  
*   Modification de feuilles CSS et affichage instantané de l’aperçu du rendu de votre site Web  
*   Afficher toutes les `console.log()` instructions de votre code JavaScript frontal  
*   Déboguer votre script en définissant des points d’arrêt et en passant en revue chaque ligne  

directement dans le navigateur.  Vous trouverez ci-dessous des exemples de certaines des fonctionnalités proposées par le DevTools pour vous permettre de créer et tester plus facilement vos sites Web dans Microsoft Edge.  

Pour ouvrir le DevTools  

*   sur `F12` 
*   Appuyez `Ctrl` + `Shift` + `I` sur Windows/Linux \ ( `Command` + `Option` + `I` sur MacOS \)  

Si vous voulez afficher le code HTML ou CSS d’un élément sur votre site, cliquez avec le bouton droit sur l’élément, puis sélectionnez **inspecter** pour accéder au panneau éléments.  Vous pouvez également appuyer `Ctrl` + `Shift` + `C` sur Windows/Linux \ ( `Command` + `Option` + `C` sur MacOS \) pour ouvrir le devtools dans le **mode inspecter l’élément** , ce qui vous permet de sélectionner un élément sur le site et d’afficher le code HTML et CSS dans le panneau **éléments** .  

Si vous voulez afficher les journaux de votre code JavaScript frontal ou exécuter rapidement un script, appuyez `Ctrl` + `Shift` + `J` sur Windows/Linux ou `Command` + `Option` + `J` sur MacOS pour lancer le panneau console dans le devtools.  

## Outils principaux  

:::image type="complex" source="./devtools-guide-chromium/media/devtools-core-tools.png" alt-text="DevTools Microsoft Edge (chrome)":::
   Outils principaux de Microsoft Edge (chrome) DevTools  
:::image-end::: 

Le Microsoft Edge \ (chrome \) DevTools inclut les panneaux suivants.  

*   Un panneau **Éléments** permettant de modifier les codes HTML et CSS, d’inspecter les propriétés d’accessibilité, d’afficher les écouteurs d’événement et de créer des points d’arrêt de mutation DOM  
*   Une **Console** pour afficher et filtrer les messages journaux, examiner les objets JavaScript et les nœuds DOM et exécuter JavaScript dans le contexte de la fenêtre ou du cadre sélectionné.  
*   Panneau **sources** permettant d’ouvrir et de modifier votre code, de définir des points d’arrêt, de parcourir le code et de consulter l’état de votre site Web en JavaScript à la fois  
*   Un panneau **Réseau** permettant de contrôler et d’inspecter les demandes et les réponses à partir du réseau et du cache du navigateur.   
*   Un panneau **Performance** pour profiler l’heure et les ressources système requises par votre site  
*   Un panneau **Mémoire** pour mesurer l’utilisation des ressources de mémoire et comparer les instantanés de tas aux différents états du runtime de code  
*   Panneau d' **application** pour inspecter, modifier et déboguer des manifestes de l’application Web, des travailleurs de services et des mises en cache du travailleur du service.  Vous pouvez également examiner et gérer le stockage, les bases de données et les caches à partir du volet de l' **application** .  
*   Un volet de **sécurité** pour déboguer les problèmes de sécurité et vérifier que vous avez correctement implémenté https sur votre site Web.  HTTPs assure la sécurité et l’intégrité des données critiques de votre site et de vos utilisateurs qui fournissent des informations personnelles sur votre site.  
*   Panneau **d’audit** **\ (** désormais, le changement de nom) pour exécuter un audit de votre site Web.  Les résultats de l’audit vous permettent d’améliorer la qualité de votre site de l’une des manières suivantes.  
    *   Intercepter les erreurs courantes liées à la mise à disposition et la sécurité de votre site Web, etc.  
    *   Corrigez chaque erreur.  
    *   Créer une version de Project.  

[!INCLUDE [audits-panel-note](./devtools-guide-chromium/includes/audits-panel-note.md)]  

Envoyez-nous vos [commentaires et demandes de fonctionnalité](#getting-in-touch-with-the-microsoft-edge-devtools-team).  

## Extensions  

Vous pouvez avoir utilisé les extensions de DevTools pour diagnostiquer et déboguer les problèmes lors de la création de vos sites Web ou applications.  Vous pouvez acquérir des extensions pour Microsoft Edge à partir de la page des [modules complémentaires Microsoft Edge][MicrosoftEdgeAddonsExtensions] .  À partir de la page des [modules complémentaires Microsoft Edge][MicrosoftEdgeAddonsExtensions] , vous pouvez parcourir les extensions devtools de la catégorie **outils de développement** ou rechercher une extension spécifique.  

Vous pouvez également ajouter des extensions à partir du [Web Store chrome][GoogleChromeWebstoreExtensions].  

:::image type="complex" source="./devtools-guide-chromium/media/allow-extensions-from-stores.png" alt-text="DevTools Microsoft Edge (chrome)":::
   Magasin Web chrome dans Microsoft Edge  
:::image-end:::  

Dans la partie supérieure, sélectionnez **autoriser les extensions d’autres magasins** , puis cliquez sur **autoriser** dans la boîte de dialogue qui s’affiche.  

> [!NOTE]
> Les extensions installées à partir de sources autres que le Microsoft Store ne sont pas vérifiées, et peuvent affecter les performances du navigateur.  

Sélectionnez **Ajouter au chrome** pour ajouter votre extension devtools à Microsoft Edge.  

:::image type="complex" source="./devtools-guide-chromium/media/install-extension-from-chrome-store.png" alt-text="DevTools Microsoft Edge (chrome)"  
