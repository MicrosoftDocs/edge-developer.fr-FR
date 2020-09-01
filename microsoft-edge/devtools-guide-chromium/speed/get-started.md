---
title: Optimiser la vitesse de votre site Web avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 42b742316ccaa64aa35fc1d21c5277e448b2d5b7
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984623"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.  
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.  
   See the License for the specific language governing permissions and
   limitations under the License.  -->  





# Optimiser la vitesse de votre site Web avec Microsoft Edge DevTools   



## Objectif du didacticiel  

Ce didacticiel vous explique comment utiliser Microsoft Edge DevTools pour trouver des méthodes pour accélérer le chargement de vos sites Web.  

## Conditions préalables  

*   Vous devez avoir une connaissance de base du développement Web, semblable à ce qui est enseigné dans cette [Introduction à la classe de développement Web][CourseraIntroductionWebDevelopmentClass].  
*   Vous n’avez aucune information sur les performances du chargement.  Pour plus d’informations, consultez ce didacticiel.  

## Introduction   

C’est Thomas.  Thierry est très célèbre dans la société de chat.  Il a créé un site Web de telle sorte que ses fans puissent en savoir plus sur ses produits préférés.  Ses fans aiment le site, mais Thomas cesse d’entendre que le site se charge lentement.  Thomas vous a demandé de lui permettre d’accélérer le site.  

:::image type="complex" source="../media/speed-tony.msft.png" alt-text="Bernard le chat" lightbox="../media/speed-tony.msft.png":::
   Bernard le chat  
:::image-end:::  

## Étape 1: Auditez le site   

Dès que vous avez fini d’améliorer les performances de chargement d’un site, **Commencez toujours par un audit**.  
L’audit comporte 2 fonctions importantes:  

*   Il crée un **planning de référence** pour vous pour mesurer les changements ultérieurs.  
*   Ce service vous donne des **conseils utiles** sur les modifications qui ont le plus d’impact.  
    
### Configuration   

Tout d’abord, vous devez configurer le site pour pouvoir le modifier ultérieurement.  

1.  [Ouvrez le code source pour le site](https://glitch.com/edit/#!/tony).  Cet onglet est appelé **onglet Éditeur**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js.msft.png" alt-text="Onglet Éditeur" lightbox="../media/speed-glitch-tony-server-js.msft.png":::
       **Onglet Éditeur**  
    :::image-end:::  
    
1.  Sélectionnez **Thomas**.  Un menu s’affiche.  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js-remix-project.msft.png" alt-text="Menu qui apparaît après avoir cliqué sur Thierry" lightbox="../media/speed-glitch-tony-server-js-remix-project.msft.png":::
       Menu qui apparaît après avoir cliqué sur **Thierry**  
    :::image-end:::  
    
1.  Sélectionnez **Remix Project**.  Le nom du projet **passe de Thomas à un** nom généré de manière aléatoire.  Vous disposez maintenant de votre propre copie modifiable du code.  Par la suite, vous pouvez modifier ce code.  
1.  Sélectionner **Afficher** et sélectionner **dans une nouvelle fenêtre**.  La démonstration s’ouvre dans un nouvel onglet.  Cet onglet est appelé **onglet démonstration**.  Le chargement du site risque de prendre un certain temps.  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live.msft.png" alt-text="Onglet démonstration" lightbox="../media/speed-glitch-tony-show-live.msft.png":::
       Onglet démonstration  
    :::image-end:::  
    
1.  Appuyez sur `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \).  Microsoft Edge DevTools s’ouvre à côté de la démonstration.  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live-console.msft.png" alt-text="DevTools et la démo" lightbox="../media/speed-glitch-tony-show-live-console.msft.png":::
       DevTools et la démo  
    :::image-end:::  
    
Pour le reste des captures d’écran de ce didacticiel, DevTools est affiché dans une fenêtre séparée.  Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes, `Undock` puis sélectionnez **détacher dans une fenêtre séparée**.  

:::image type="complex" source="../media/speed-console.msft.png" alt-text="DevTools non attaché" lightbox="../media/speed-console.msft.png":::
   DevTools non attaché  
:::image-end:::  

### Établir un planning de référence   

Le planning de référence est un enregistrement de la façon dont le site a été traité avant d’améliorer ses performances.  

1.  Sélectionnez l’onglet **audits** .  Il est possible qu’il soit masqué derrière le bouton **autres panneaux** \ ( ![ autres panneaux ][ImageMorePanelsIcon] \).  Ce panneau comporte une phare, car le projet qui alimente le panneau d’audit est appelé **phare**.  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    :::image type="complex" source="../media/speed-audits-performance.msft.png" alt-text="Volet d’audit" lightbox="../media/speed-audits-performance.msft.png":::
       Volet **d’audit**  
    :::image-end:::  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  Associez vos paramètres de configuration d’audit à ceux de la figure précédente.  Voici une explication des différentes options disponibles:  
    
    *   **Appareil**.  Définissez sur **mobile** pour modifier la chaîne de l’agent utilisateur et simuler une fenêtre d’affichage mobile.  Le paramétrage sur **Bureau** à peu près empêche uniquement les changements de **mobilité** .  
    *   Les **audits**.  La désactivation d’une catégorie empêche le panneau d’audit d’exécuter ces audits et exclut ces audits de votre rapport.  Laissez les autres catégories activées si vous voulez voir les types de recommandations qui s’offrent à vous.  La désactivation des catégories accélère légèrement le processus d’audit.  
    *   **Limitation**.  Pour simuler la fonction de **4G lente, le ralenti de l’UC 4x** simule les conditions typiques de navigation sur un appareil mobile.  Son nom est «simulé», car le panneau d’audit n’est pas réellement limité lors du processus d’audit.  Au lieu de cela, il s’agit simplement de l’extrapolation du temps nécessaire au chargement de la page dans des conditions mobiles.  En revanche, le paramètre **appliedd...** , qui a pour effet de limiter votre processeur et votre réseau, par le biais d’un processus d’audit plus long.  
    *   **Vider le stockage**.  Activez cette case à cocher pour effacer tout le stockage associé à la page avant chaque audit.  Ne renseignez pas ce paramètre si vous souhaitez vérifier la manière dont les visiteurs de votre site se familiarisent avec la première fois.  Désactivez ce paramètre si vous souhaitez utiliser la répétition d’une visite.  
    
1.  Sélectionnez **exécuter les audits**.  Après 10 à 30 secondes, le volet d’audit affiche un rapport sur les performances de votre site.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png" alt-text="Rapport du volet d’audit des performances du site" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png":::
       Rapport du volet d’audit des performances du site  
    :::image-end:::  
    
#### Gestion des erreurs de rapport   

Si un message d’erreur apparaît dans votre rapport du panneau d’audit, essayez d’exécuter l’onglet démonstration à partir d’une fenêtre **InPrivate** sans afficher d’autres onglets.  Cela garantit que vous exécutez Microsoft Edge à partir de l’État Clean.  Les extensions Microsoft Edge en particulier interfèrent souvent avec le processus d’audit.  

<!--todo: add screen capture for error in audit -->  
<!--
:::image type="complex" source="../media/speed-.msft.png" alt-text="A report that errored" lightbox="../media/speed-.msft.png":::
   A report that errored  
:::image-end:::  
-->  

### Comprendre votre état   

Le nombre situé en haut de votre état correspond au score de performance global du site.  Par la suite, au fur et à mesure que vous apportez des modifications à votre code, vous devriez voir ce numéro augmenter.  Un résultat plus élevé correspond à de meilleures performances.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png" alt-text="Le score de performance global" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png":::
   Le score de performance global  
:::image-end:::  

La section **mesures** fournit des mesures quantitatives des performances du site.  Chaque métrique donne un aperçu d’un aspect différent des performances.  Par exemple, lorsque le contenu est dessiné à l’écran pour **la première fois** , il s’agit d’un jalon important dans la perception de l’utilisateur du chargement de la page, alors que le **temps nécessaire à l’interactivité** correspond au point où la page semble suffisamment prête pour gérer les interactions utilisateur.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png" alt-text="Section mesures" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png":::
   Section **mesures**  
:::image-end:::  

Sélectionnez le bouton bascule surligné dans la figure ci-dessous pour afficher une description de chaque métrique, puis cliquez sur **en savoir plus** pour lire la documentation correspondante.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png" alt-text="Sélectionner le bouton bascule surligné pour développer les éléments métriques" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png":::
   Sélectionner le bouton bascule surligné pour développer les éléments métriques  
:::image-end:::  

Le sous-métrique est une collection de captures d’écran qui vous montrent le mode de chargement de la page.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Captures d’écran illustrant l’apparence de la page en cours de chargement" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   Captures d’écran illustrant l’apparence de la page en cours de chargement  
:::image-end:::  

La section **opportunités** fournit des conseils spécifiques pour améliorer les performances de chargement de cette page spécifique.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Section opportunités" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   Section **opportunités**  
:::image-end:::  

Sélectionnez une opportunité pour en savoir plus à son sujet.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png" alt-text="Éliminer l’opportunité de blocage des ressources de blocage des rendez-vous" lightbox="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png":::
   **Éliminer l’opportunité de blocage des ressources de blocage des rendez-** vous  
:::image-end:::  

Pour plus d’informations sur les raisons de la nécessité d’une opportunité, voir **en savoir plus** sur la résolution des problèmes.  

:::image type="complex" source="../media/speed-web-dev-performance-audits.msft.png" alt-text="Documentation pour l’opportunité de suppression des ressources de blocage de rendu" lightbox="../media/speed-web-dev-performance-audits.msft.png":::
   Documentation pour l’opportunité de **suppression des ressources de blocage de rendu**  
:::image-end:::  

La section **Diagnostics** fournit des informations supplémentaires sur les facteurs qui contribuent au temps de chargement de la page.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png" alt-text="Section Diagnostics" lightbox="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png":::
   Section **Diagnostics**  
:::image-end:::  

La section **contrôles réussis** vous montre le fonctionnement correct du site.  Pour développer la section.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png" alt-text="Section audits transmis" lightbox="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png":::
   Section **audits transmis**  
:::image-end:::  

## Étape 2: expérimenter   

La section opportunités de votre rapport d’audit vous donne des conseils pour améliorer les performances de la page.  Dans cette section, vous implémentez les modifications recommandées sur le code base, puis vous auditez le site après chaque modification pour mesurer la vitesse de votre site.  

### Activer la compression de texte   

Votre rapport déclare qu’il n’est pas l’une des principales opportunités d’améliorer les performances de la page.  L’activation de la compression de texte permet d’améliorer les performances de la page.  

La compression de texte est celle qui consiste à réduire ou compresser la taille d’un fichier texte avant de l’envoyer sur le réseau.  Type semblable à la façon dont vous pouvez Zipper un dossier avant de l’envoyer par courrier électronique afin de réduire la taille.  

Avant d’activer la compression, voici quelques méthodes permettant de vérifier manuellement si les ressources de texte sont comprimées.  

1.  Sélectionnez l’onglet **Network (réseau** ).  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network.msft.png" alt-text="Panneau réseau" lightbox="../media/speed-glitch-tony-remix-network.msft.png":::
       Panneau **réseau**  
    :::image-end:::  
    
1.  Sélectionnez l’icône du **paramètre réseau** .  
1.  Cochez la case **utiliser des lignes de requête volumineuses** .  La hauteur des lignes du tableau de requêtes réseau augmente.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png" alt-text="Lignes de grande taille dans la table requêtes réseau" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png":::
       Lignes de grande taille dans la table requêtes réseau  
    :::image-end:::  
    
1.  Si vous ne voyez pas la colonne **taille** dans le tableau des requêtes réseau, cliquez sur l’en-tête de la table, puis sélectionnez **taille**.  

Chaque cellule **taille** affiche deux valeurs.  La valeur supérieure correspond à la taille de la ressource téléchargée.  
La valeur inférieure correspond à la taille de la ressource non compressée.  Si les deux valeurs sont identiques, la ressource n’est pas compressée lors de son envoi via le réseau.  Par exemple, dans l’illustration précédente, les premières et dernières valeurs de `bundle.js` sont `1.2 MB` et `1.2 MB` .  

Vérifiez la compression en inspectant les en-têtes HTTP d’une ressource:  

1.  Sélectionnez **bundle.js**.  
1.  Sélectionnez l’onglet **en-têtes** .  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png" alt-text="Onglet en-têtes" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png":::
       Onglet **en-têtes**  
    :::image-end:::  
    
1.  Recherchez un en-tête dans la section **en-têtes de réponse** `content-encoding` .  Vous ne devez pas voir l’une d’elles, ce qui signifie qu’elle n' `bundle.js` a pas été compactée.  Lorsqu’une ressource est compressée, cet en-tête est généralement défini sur `gzip` , `deflate` ou `br` .  Pour obtenir une description de ces valeurs, voir [directives][MDNContentEncodingDirectives] .  

C’est suffisant pour les explications.  Le moment est venu d’apporter des modifications.  Autorisez la compression de texte en ajoutant quelques lignes de code:  

1.  Dans l’onglet Éditeur, cliquez sur **server.js**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js.msft.png" alt-text="Modifier server.js" lightbox="../media/speed-glitch-tony-remix-server-js.msft.png":::
       Edit `server.js`  
    :::image-end:::  
    
1.  Ajoutez le code suivant à **server.js**.  Assurez-vous d’entrer `app.use(compression())` auparavant `app.use(express.static('build'))` .  

    ```javascript
    const express = require('express');
    const app = express();
    const fs = require('fs');
    const compression = require('compression');

    app.use(compression());
    app.use(express.static('build'));
    
    const listener = app.listen(process.env.PORT || 1234, function () {
        console.log(`Listening on port ${listener.address().port}`);
    });
    ```  
    
    > [!NOTE]
    > En règle générale, vous devez installer le `compression` package par le biais d’une expression similaire `npm i -S compression` , mais cela a déjà été fait pour vous.  
    
1.  Patientez pendant le déploiement de la nouvelle version du site.  L’animation fantaisie en regard des **Outils** signifie que le site est en cours de recréation et de redéploiement.  La modification est prête lorsque l’animation en regard des **Outils** est en suspens.  Sélectionnez **Afficher** et sélectionnez **de nouveau dans une nouvelle fenêtre** .  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js-edited.msft.png" alt-text="The animation that indicates that the site is getting built" lightbox="../media/speed-glitch-tony-remix-server-js-edited.msft.png":::
       The animation that indicates that the site is getting built  
    :::image-end:::  
    -->  
    
Utilisez les flux de travail que vous avez appris précédemment pour vérifier que la compression fonctionne:  

1.  Revenez à l’onglet démonstration et rechargez la page.  La colonne **taille** doit maintenant afficher 2 valeurs différentes pour les ressources de texte comme `bundle.js` .  Dans l’illustration suivante, la valeur la plus haute de `256 KB` pour `bundle.js` correspond à la taille du fichier envoyé sur le réseau et la valeur inférieure de `1.2 MB` correspond à la taille de fichier non comprimé.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-main.msft.png" alt-text="La colonne taille affiche désormais 2 valeurs différentes pour les ressources de texte" lightbox="../media/speed-glitch-tony-remix-network-main.msft.png":::
       La colonne **taille** affiche désormais 2 valeurs différentes pour les ressources de texte  
    :::image-end:::  
    
1.  La section **en-têtes de réponse** de `bundle.js` devrait désormais inclure un `content-encoding: gzip` en-tête.
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png" alt-text="La section en-têtes de réponse contient désormais un en-tête de codage de contenu" lightbox="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png":::
       La section **en-têtes de réponse** contient désormais un en-tête de codage de contenu  
    :::image-end:::  
    
Auditez de nouveau la page pour mesurer le type de compression de texte d’impact sur les performances de chargement de la page:  

1.  Sélectionnez l’onglet **audits** .  
1.  Sélectionnez **effectuer un audit** \ ( ![ effectuer un audit ][ImagePerformIcon] \).  
1.  Ne modifiez pas les paramètres comme auparavant.  
1.  Sélectionnez **exécuter l’audit**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png" alt-text="Rapport d’audit après l’activation de la compression de texte" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png":::
       Rapport d’audit après l’activation de la compression de texte  
    :::image-end:::  
    
<!--  Woohoo!  That looks like progress.  -->  Le score de performance global doit être plus élevé, ce qui signifie que le site est plus rapide.  

#### Compression de texte dans le monde réel   

La plupart des serveurs possèdent réellement des correctifs simples, comme pour l’activation du compactage.  Il suffit de procéder à une recherche pour configurer le serveur que vous utilisez pour compresser le texte.  

### Redimensionner des images   

Votre rapport indique qu’il est recommandé d’éviter les charges utiles réseau énormes pour améliorer les performances de la page.  Le redimensionnement des images permet de réduire la taille de la charge utile du réseau.  Si votre utilisateur consulte vos images sur un écran d’appareil mobile d’une largeur de 500 pixels, il n’y a rien de plus que d’envoyer une image 1500 à l’échelle des pixels.  Idéalement, vous envoyez une image de 500 pixels, le plus souvent.  

1.  Dans votre rapport, cliquez sur **éviter les charges utiles réseau énormes** pour voir les images qui doivent être redimensionnées.  Il semble que 2 des fichiers jpg dépassent 2000 Ko, ce qui est plus grand que nécessaire.  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png" alt-text="Details about the properly size images opportunity" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png":::
       Details about the properly size images opportunity  
    :::image-end:::  
    -->
    
1.  Dans l’onglet Éditeur, ouvrez `src/model.js` .  
1.  Remplacer `const dir = 'big'` par `const dir = 'small'` .  Ce répertoire contient des copies des mêmes images qui ont été redimensionnées.  
1.  Auditez de nouveau la page pour voir l’incidence de cette modification sur les performances de chargement.  
    
    :::image type="complex" source="../media/speed-glitch-compression-small-images-audits-performance.msft.png" alt-text="Rapport d’audit après le redimensionnement d’images" lightbox="../media/speed-glitch-compression-small-images-audits-performance.msft.png":::
       Rapport d’audit après le redimensionnement d’images  
    :::image-end:::  
    
Il semble que la modification n’ait qu’une incidence mineure sur le score de performance global.  Néanmoins, il n’y a pas de distinction entre le résultat et la quantité de données réseau que vous enregistrez pour vos utilisateurs.  La taille totale de l’ancienne photo a été d’environ 5,3 Mo, alors qu’il n’y a que 0,18 mégaoctets.  

#### Redimensionnement d’images dans le monde réel   

Dans le cas d’une petite application, il est possible de redimensionner une seule fois comme suit.  Néanmoins, dans le cas d’une application de grande taille, cette solution n’est pas évolutive.  Voici quelques stratégies de gestion des images dans les applications volumineuses:  

*   Redimensionnez les images lors de votre processus de génération.  
*   Créez plusieurs tailles de chaque image lors du processus de génération, puis utilisez-la `srcset` dans votre code.  Lors de l’exécution, le navigateur s’occupe de choisir la taille la mieux appropriée pour l’appareil.  
    <!--See [Relative-sized images][relative].  -->
    
<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   Utilisez un CDN d’image qui vous permet de redimensionner dynamiquement une image lorsque vous la demandez.  
*   Optimisez chaque image au moins.  Cela risque de créer des économies considérables.  
  L’optimisation consiste à exécuter une image par le biais d’un programme spécial qui réduit la taille du fichier image.  Pour plus d’informations, voir [optimisation d’image essentielle][EssentialImageOptimization] .  
    
### Éliminer les ressources de blocage des rendez-vous   

Votre dernier État dit qu’il est impossible d’éliminer les ressources de blocage de rendu.  

Une ressource de blocage de rendu est un fichier JavaScript ou CSS externe que le navigateur doit télécharger, analyser et exécuter avant d’afficher la page.  L’objectif est d’exécuter uniquement le code CSS principal et le code JavaScript requis pour afficher la page correctement.  

La première tâche consiste à trouver le code que vous n’avez pas besoin de réexécuter sur le chargement de la page.  

1.  Sélectionnez **éliminer les ressources de blocage de rendu** pour afficher les ressources qui se bloquent:  
    `lodash.js` et `jquery.js` .  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png" alt-text="Plus d’informations sur l’opportunité de suppression des ressources de blocage de rendu" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png":::
       Plus d’informations sur l’opportunité de **suppression des ressources de blocage de rendu**  
    :::image-end:::  
    
1.  Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes, commencez à taper `Coverage` , puis sélectionnez **afficher la couverture**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png" alt-text="Ouvrir le menu de commandes à partir du volet audits" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png":::
       Ouvrir le menu de commandes à partir du volet **audits**  
    :::image-end:::  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png" alt-text="Onglet couverture" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png":::
       Onglet **couverture**  
    :::image-end:::  
    
1.  Sélectionnez **Actualiser** /actualiser ![ ][ImageRefreshIcon] .  L’onglet **couverture** fournit une vue d’ensemble de la quantité de code `bundle.js` `jquery.js` et `lodash.js` s’exécute pendant le chargement de la page.  Dans l’illustration ci-dessous, à propos de 76% et de 30% des fichiers jQuery et Lodash ne sont pas utilisés, respectivement.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png" alt-text="Rapport de couverture" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png":::
       Rapport de couverture  
    :::image-end:::  
    
1.  Sélectionnez la ligne **jquery.js** .  DevTools ouvre le fichier dans le volet sources.  Une ligne de code a été exécutée si une barre bleue est située en regard.  Une barre rouge signifie qu’elle n’a pas été exécutée et qu’elle n’est pas nécessaire sur le chargement de la page.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png" alt-text="Affichage du fichier jQuery dans le panneau sources" lightbox="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png":::
       Affichage du fichier jQuery dans le panneau **sources**  
    :::image-end:::  
    
1.  Parcourez un bit du code jQuery.  Voici quelques-unes des lignes qui s’exécutent uniquement en commentaires.  L’exécution de ce code par le biais d’un Minifier qui tire des commentaires est une autre façon de réduire la taille de ce fichier.  

En résumé, lorsque vous utilisez votre propre code, l’onglet couverture vous permet d’analyser votre code, ligne par ligne, et d’expédier uniquement le code nécessaire au chargement de la page.  

Les fichiers et sont-ils `jquery.js` `lodash.js` même nécessaires pour le chargement de la page?  L’onglet de blocage de requête indique ce qui se produit lorsque les ressources ne sont pas disponibles.  

1.  Sélectionnez l’onglet **Network (réseau** ).  
1.  Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir de nouveau le menu de commandes.  
1.  Commencez à taper `blocking` , puis sélectionnez **afficher le blocage de requête**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png" alt-text="Onglet requête de blocage" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png":::
       Onglet **requête de blocage**  
    :::image-end:::  
    
1.  Sélectionnez **Ajouter un modèle** \ ( ![ Ajouter un modèle ][ImageAddPatternIcon] \), tapez `/libs/*` , puis appuyez sur `Enter` pour confirmer.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png" alt-text="Ajouter un modèle pour bloquer toute demande de l’annuaire de bibliothèques" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png":::
       Ajouter un modèle pour bloquer toute demande de l' `libs` Annuaire  
    :::image-end:::  
    
1.  Actualisez la page.  Les requêtes jQuery et Lodash sont rouges, ce qui signifie que les requêtes ont été bloquées.   Étant donné que la page est toujours chargée et qu’elle est interactive, il semblerait que les ressources suivantes ne soient pas nécessaires.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png" alt-text="Le volet réseau indique que les requêtes ont été bloquées." lightbox="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png":::
       Le volet **réseau** indique que les requêtes ont été bloquées.  
    :::image-end:::  
    
1.  Sélectionnez **Supprimer tous les modèles** \ ( ![ Supprimer tous les modèles ][ImageRemoveIcon] \) pour supprimer le `/libs/*` modèle de blocage.  
    
En règle générale, l’onglet blocage de requête est utile pour simuler le comportement de votre page quand une ressource donnée n’est pas disponible.  

À présent, supprimez les références à ces fichiers du code et auditez de nouveau la page:  

1.  Dans l’onglet Éditeur, ouvrez `template.html` .  
1.  Supprimez les éléments `<script src="/libs/lodash.js">` et `<script src="/libs/jquery.js"></script>`.  
1.  Attendez que le site soit recréé et redéploiement.  
1.  Auditez de nouveau la page à partir du volet **vérifications** .  Votre score global devrait de nouveau s’améliorer.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png" alt-text="Rapport d’audit après la suppression des ressources de blocage de rendu" lightbox="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png":::
       Rapport **d’audit** après la suppression des ressources de blocage de rendu  
    :::image-end:::  
    
#### Optimisation du chemin de rendu critique dans le monde réel   

Le **chemin de rendu critique** fait référence au code dont vous avez besoin pour charger une page.  En règle générale, accélérez le chargement de la page en ne disportant que le code Critical pendant le chargement de la page, puis en chargeant en différé tout le reste.  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   Il est peu probable que vous puissiez retrouver les scripts que vous pouvez supprimer d’un certain temps, mais il se peut que vous trouviez de nombreux scripts que vous n’avez pas besoin de demander pendant le chargement de la page, et qu’ils puissent être demandés de manière asynchrone.  <!--See [Using async or defer][async].  -->  
*   Si vous utilisez un Framework, vérifiez qu’il dispose du mode de production.  Ce mode peut utiliser une fonctionnalité telle que l’agitation de l' [arborescence][WebpackTreeShaking] afin d’éliminer le code inutile qui bloque le rendu critique.  
    
<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### Réduire le fonctionnement du thread principal   

Votre dernier État montre quelques réductions potentielles mineurs dans la section opportunités, mais si vous examinez la section Diagnostics, il semble que le plus grand goulet d’étranglement soit trop important pour le thread principal.  

Le thread principal est l’endroit où le navigateur exécute la majeure partie du processus d’affichage d’une page, telle que l’analyse et l’exécution de HTML, CSS et JavaScript.  

L’objectif consiste à utiliser le panneau performance pour analyser le travail effectué par le thread principal pendant le chargement de la page, et Rechercher des moyens de différer ou de supprimer le travail inutile.  

1.  Sélectionnez l’onglet **performance** .  
1.  Sélectionnez **paramètres de capture** \ ( ![ paramètres de capture ][ImageCaptureIcon] \).  
1.  Définissez **réseau** sur **lente réseau 3G** et **UC** à **6**ralentis.  Les appareils mobiles présentent généralement plus de contraintes matérielles que les ordinateurs portables ou de bureau, de sorte que ces paramètres vous permettent de vous familiariser avec le chargement de la page comme si vous utilisiez un appareil moins puissant.  
1.  Sélectionnez **Actualiser** /actualiser ![ ][ImageRefreshIcon] .  DevTools actualise la page, puis produit une visualisation de tout le temps exécuté pour le chargement de la page.  Cette visualisation est appelée **suivi**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png" alt-text="Suivi du panneau de performance du chargement de la page" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png":::
       Suivi du panneau de **performance** du chargement de la page  
    :::image-end:::  
    
Le suivi des activités est affiché dans un ordre chronologique, de gauche à droite.  Les graphiques FPS, UC et NET en haut offrent une vue d’ensemble des images par seconde, de l’activité de l’UC et de l’activité du réseau.  Le bloc de jaune sélectionné que vous voyez dans la figure après ce qui suit, l’UC était entièrement chargée avec l’activité de script.  C’est une idée qu’il est possible que vous puissiez accélérer le chargement de la page en effectuant moins de tâches JavaScript.  

:::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png" alt-text="Section vue d’ensemble du suivi" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png":::
   Section vue d’ensemble du suivi  
:::image-end:::  

Examinez la trace pour trouver des moyens d’effectuer moins de tâches JavaScript:  

1.  Sélectionnez la section **minutage** pour la développer.  En fonction du fait qu’il est possible qu’il y ait quelques mesures de [temporisation][MDNUserTimingApi] , il semble que l’application Thomas utilise le mode développement de réaction.  Basculer vers le mode de production de réagisser risque de générer un service de performance plus simple.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png" alt-text="Section minutage" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png":::
       Section **minutage**  
    :::image-end:::  
    
1.  Sélectionnez de nouveau **minutages** pour réduire cette section.  
1.  Naviguez dans la section **principale** .  Cette section présente un journal chronologique de l’activité principale du thread, de gauche à droite.  L’axe y (de haut en bas) montre pourquoi des événements s’est produit.  Par exemple, dans le figyre après ce qui suit, l' `Evaluate Script` événement a entraîné l’exécution de la fonction, ce qui a provoqué son exécution, `(anonymous)` `(anonymous)` `__webpack__require__` et ainsi de suite.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png" alt-text="Section principale" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png":::
       Section **principale**  
    :::image-end:::  
    
1.  Faites défiler vers le bas jusqu’en bas de la section **principale** .  Lorsque vous utilisez une infrastructure, la majeure partie de l’activité la plus grande est provoquée par l’infrastructure, qui est généralement hors de votre contrôle.  L’activité générée par votre application est généralement située en bas.  Dans cette application, il semble qu’une fonction nommée `App` génère un grand nombre de requêtes sur une `mineBitcoin` fonction.  Il semble que Thomas utilise les appareils de ses fans pour cryptocurrency...  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png" alt-text="Pointez sur l’activité mineBitcoin" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png":::
       Pointez sur l' `mineBitcoin` activité  
    :::image-end:::  
    
    > [!NOTE]
    > Bien que les requêtes que votre infrastructure effectue généralement hors de votre contrôle, il est possible que vous puissiez structurer votre application de manière à ce que l’infrastructure s’exécute de manière inefficace.  La restructuration de votre application pour qu’elle utilise efficacement l’infrastructure est un moyen de réduire le coût de fonctionnement du thread principal.  Toutefois, cela nécessite une compréhension approfondie du fonctionnement de l’infrastructure et le type de modification que vous effectuez dans votre propre code afin d’utiliser l’infrastructure plus efficacement.  
    
1.  Développez la section **de haut en bas** .  Dans cet onglet, les activités ont duré le plus longtemps.  S’il n’y a aucun élément dans la section de haut en bas, cliquez sur l’étiquette de la section **principale** .  La section **ascendante** affiche uniquement les informations relatives à l’activité, ou au groupe d’activité, que vous avez sélectionné.  Par exemple, si vous avez cliqué sur une des `mineBitcoin` activités, la section de **bas en haut** consiste à afficher les informations relatives à cette activité unique.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png" alt-text="Onglet inférieur" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png":::
       Onglet **inférieur**  
    :::image-end:::  
    
La colonne **temps libre** vous indique le temps passé directement dans chaque activité.  Par exemple, dans l’illustration suivante, environ 63% du temps de thread principal a été dépensé sur la `mineBitcoin` fonction.  

Il est temps de voir si l’utilisation du mode de production et la réduction des activités JavaScript accélèrent le chargement de la page.  Commencer avec le mode production:  

1.  Dans l’onglet Éditeur, ouvrez `webpack.config.js` .  
1.  Remplacez `"mode":"development"` par `"mode":"production"` .  
1.  Attendez la fin du déploiement de la nouvelle Build.  
1.  Auditez de nouveau la page.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png" alt-text="Rapport d’audit après la configuration de WebPack pour utiliser le mode de production" lightbox="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png":::
       Rapport d’audit après la configuration de WebPack pour utiliser le mode de production  
    :::image-end:::  
    
Réduisez les activités JavaScript en supprimant la demande `mineBitcoin` :  

1.  Dans l’onglet Éditeur, ouvrez `src/App.jsx` .  
1.  Transmettez la demande au `this.mineBitcoin(1500)` `constructor` .  
1.  Attendez la fin du déploiement de la nouvelle Build.  
1.  Auditez de nouveau la page.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png" alt-text="Rapport de vérification après suppression du fonctionnement inutile de JavaScript" lightbox="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png":::
       Rapport de vérification après suppression du fonctionnement inutile de JavaScript  
    :::image-end:::  
    
Il semble que le dernier changement ait entraîné un décalage massif de performances.  

> [!NOTE]
> Cette section proposait plutôt une présentation du panneau performance.  Pour en savoir plus sur l’analyse des performances des pages, voir référence sur l' [analyse des performances][DevtoolsEvaluatePerformanceReference] .  

<!--todo: add section when available -->  

#### Exécution moins importante du thread principal dans le monde réel   

En règle générale, le panneau **performance** est le moyen le plus courant de comprendre l’activité que votre site effectue au chargement et les manières de supprimer les activités inutiles.  

Si vous préférez une approche qui ressemble davantage à celle- `console.log()` ci, l' [API de minutage des utilisateurs][MDNUserTimingApi] vous permet de marquer de façon arbitraire certaines phases du cycle de vie de votre application afin d’effectuer le suivi de la durée de chacune de ces phases.  

## Résumé   

*   Dès que vous avez fini d’optimiser les performances de chargement d’un site, commencez toujours par un audit.  L’audit établit un planning de référence et vous donne des conseils sur la manière d’améliorer.  
*   Apportez une modification à la fois, puis auditez la page après chaque modification afin de savoir comment ce changement d’isolement a un impact sur les performances.  

<!--
## Next steps   

*   Run audits on your own site!  If you need help interpreting your report, or finding ways to improve your load performance, check out [Feedback](#feedback) for ways to get help from the DevTools community.  Stack Overflow, the mailing list, or Twitter are probably best for these types of questions.  
*   Please leave [feedback](#feedback) on this tutorial.  I really do use the data to make better tutorials for you.  
-->  

<!--  
  


-->  

<!-- image links -->  

[ImageAddPatternIcon]: ../media/add-pattern-icon.msft.png  
[ImageCaptureIcon]: ../media/capture-icon.msft.png  
[ImageLargeResourceRowsButtonIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageMorePanelsIcon]: ../media/more-panels-icon.msft.png  
[ImagePerformIcon]: ../media/perform-icon.msft.png  
[ImageRefreshIcon]: ../media/reload-icon.msft.png  
[ImageRemoveIcon]: ../media/remove-icon.msft.png  
<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: ../evaluate-performance/reference.md "Référence d’analyse des performances | Documents Microsoft"  

[CourseraIntroductionWebDevelopmentClass]: https://www.coursera.org/learn/web-development#syllabus "Présentation de la classe développement Web | Coursera"  

[EssentialImageOptimization]: https://images.guide "Optimisation d’image essentielle"  

[MDNContentEncodingDirectives]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Encoding#Directives "Directives-Content-Encoding | MDN"  
[MDNUserTimingApi]: https://developer.mozilla.org/docs/Web/API/User_Timing_API "API de minutage des utilisateurs | MDN"  

[WebpackTreeShaking]: https://webpack.js.org/guides/tree-shaking "Faire secousses de l’arborescence | Pack d’intercomposition"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
