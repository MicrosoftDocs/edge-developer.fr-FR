---
description: Découvrez comment utiliser Microsoft Edge DevTools pour trouver des moyens d’accélérer le chargement de vos sites web.
title: Optimiser la vitesse du site web avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 304cf9e36260b8637af38ed0dfe1ba91f3a56504
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564881"
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
# <a name="optimize-website-speed-with-microsoft-edge-devtools"></a>Optimiser la vitesse du site web avec Microsoft Edge DevTools  

## <a name="goal-of-tutorial"></a>Objectif du didacticiel  

Ce didacticiel vous apprend à utiliser Microsoft Edge DevTools pour trouver des moyens d’accélérer la charge de vos sites web.  

## <a name="prerequisites"></a>Conditions préalables  

*   Vous devez avoir une expérience de développement web de base, semblable à ce qui est appris dans cette [classe Introduction au développement Web.][CourseraIntroductionWebDevelopmentClass]  
*   Vous n’avez rien à savoir sur les performances de chargement.  Vous en apprendrez davantage à ce sujet dans ce didacticiel.  

## <a name="introduction"></a>Introduction  

Il s’agit de Tony.  Tony est très moderne dans la société de chat.  Il a créé un site web pour que ses fans puissent en savoir plus sur son favori.  Ses fans aiment le site, mais Tony ne cesse d’entendre des plaintes concernant le chargement lent du site.  Tony vous a demandé de l’aider à accélérer le site.  

:::image type="complex" source="../media/speed-tony.msft.png" alt-text="Tony le chat" lightbox="../media/speed-tony.msft.png":::
   Tony le chat  
:::image-end:::  

## <a name="step-1-audit-the-site"></a>Étape 1 : Auditer le site  

Chaque fois que vous définissez pour améliorer les performances de charge d’un site, **commencez toujours par un audit.**  
L’audit a 2 fonctions importantes :  

*   Il crée une ligne **de** base pour vous aider à mesurer les modifications ultérieures.  
*   Il vous donne des **conseils actionnables** sur les modifications qui ont le plus d’impact.  
    
### <a name="set-up"></a>Configuration  

Tout d’abord, vous devez configurer le site afin de pouvoir y apporter des modifications ultérieurement.  

1.  [Ouvrez le code source pour le site.](https://glitch.com/edit/#!/tony)  Cet onglet est appelé « onglet **éditeur**».  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js.msft.png" alt-text="Onglet Éditeur" lightbox="../media/speed-glitch-tony-server-js.msft.png":::
       Onglet **Éditeur**  
    :::image-end:::  
    
1.  Choose **tony**.  Un menu s’affiche.  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js-remix-project.msft.png" alt-text="Menu qui s’affiche après le choix de Tony" lightbox="../media/speed-glitch-tony-server-js-remix-project.msft.png":::
       Menu qui s’affiche après le choix de **Tony**  
    :::image-end:::  
    
1.  Choisissez **Project**.  Le nom du projet change de **Tony** à un nom généré de manière aléatoire.  Vous avez maintenant votre propre copie modifiable du code.  Plus tard, vous pouvez apporter des modifications à ce code.  
1.  Choose **Show** and choose **In a New Window**.  La démonstration s’ouvre dans un nouvel onglet.  Cet onglet est appelé « **onglet de démonstration**».  Le chargement du site peut prendre un certain temps.  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live.msft.png" alt-text="Onglet de démonstration" lightbox="../media/speed-glitch-tony-show-live.msft.png":::
       Onglet de démonstration  
    :::image-end:::  
    
1.  Sélectionnez `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).  Microsoft Edge DevTools s’ouvre en même temps que la démonstration.  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live-console.msft.png" alt-text="DevTools et la démonstration" lightbox="../media/speed-glitch-tony-show-live-console.msft.png":::
       DevTools et la démonstration  
    :::image-end:::  
    
Pour le reste des captures d’écran de ce didacticiel, DevTools est affiché dans une fenêtre distincte.  Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) `Undock` **** pour ouvrir le menu Commande, en tapant, puis en sélectionnant Undock dans une fenêtre distincte.  

:::image type="complex" source="../media/speed-console.msft.png" alt-text="DevTools non barraté" lightbox="../media/speed-console.msft.png":::
   DevTools non barraté  
:::image-end:::  

### <a name="establish-a-baseline"></a>Établir une ligne de base  

La ligne de base est un enregistrement de la façon dont le site a été exécuté avant d’apporter des améliorations de performances.  

1.  Choisissez **l’outil Audits.**  Il peut être masqué derrière le **bouton Plus de panneaux** \( ![ Plus de ](../media/more-panels-icon.msft.png) panneaux \).  Ce panneau présente une partie du panneau, car le projet qui alimente le panneau Audits s’appelle **Le Chef d’équipe**.  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    :::image type="complex" source="../media/speed-audits-performance.msft.png" alt-text="Outil Audits" lightbox="../media/speed-audits-performance.msft.png":::
       Outil **Audits**  
    :::image-end:::  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  Correspondez à vos paramètres de configuration d’audit à ceux de la figure précédente.  Voici une explication des différentes options :  
    
    *   **Appareil**.  Définir sur **Mobile** modifie la chaîne de l’agent utilisateur et simule une vue mobile.  Définir sur **Bureau** ne fait que éteindre les **modifications mobiles.**  
    *   **Audits**.  Désactiver une catégorie pour empêcher le panneau **Audits** d’exécution de ces audits et exclut ces audits de votre rapport.  Laissez les autres catégories désactivées si vous souhaitez afficher les types de recommandations fournis.  Désactiver les catégories pour accélérer légèrement le processus d’audit.  
    *   **Limitation**.  Définie sur **Simulated Slow 4G, 4x CPU Slow** simule les conditions de navigation classiques sur un appareil mobile.  Il est nommé « simulé », car le panneau Audits n’est pas réellement limitée pendant le processus d’audit.  Au lieu de cela, il extrapole simplement la durée de chargement de la page dans des conditions mobiles.  En **revanche,** le paramètre Appliqué... permet de limiter votre processeur et votre réseau, avec le compromis d’un processus d’audit plus long.  
    *   **Effacer Stockage**.  Activer la case à cocher pour effacer tout le stockage associé à la page avant chaque audit.  Laissez ce paramètre sur si vous souhaitez auditer la façon dont les visiteurs ront la première expérience de votre site.  Désactiver ce paramètre lorsque vous souhaitez l’expérience de répétition de visite.  
    
1.  Choose **Run Audits**.  Après 10 à 30 **secondes,** le panneau Audits affiche un rapport sur les performances du site.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png" alt-text="Rapport pour le panneau Audits des performances du site" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png":::
       Rapport pour le panneau Audits des performances du site  
    :::image-end:::  
    
#### <a name="handling-report-errors"></a>Gestion des erreurs de rapport  

Si vous obtenez une erreur dans votre rapport du panneau Audits, essayez d’exécutez l’onglet de démonstration à partir d’une fenêtre **InPrivate** sans aucun autre onglet ouvert.  Cela garantit que vous exécutez Microsoft Edge à partir d’un état propre.  Microsoft Edge Les extensions en particulier interfèrent souvent avec le processus d’audit.  

<!--todo: add screen capture for error in audit -->  
<!--
:::image type="complex" source="../media/speed-.msft.png" alt-text="A report that errored" lightbox="../media/speed-.msft.png":::
   A report that errored  
:::image-end:::  
-->  

### <a name="understand-your-report"></a>Comprendre votre rapport  

Le nombre en haut de votre rapport est le score de performances global du site.  Plus tard, au cours des modifications apportées au code, le nombre affiché doit augmenter.  Un score plus élevé signifie de meilleures performances.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png" alt-text="Le score de performances global" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png":::
   Le score de performances global  
:::image-end:::  

La section **Mesures** fournit des mesures quantifias des performances du site.  Chaque métrique fournit un aperçu d’un aspect différent des performances.  Par exemple, **First Contentful Paint** vous indique quand le contenu est peint pour la première fois à l’écran, ce qui est un jalon important dans la perception de l’utilisateur du chargement de la page, tandis que **Time To Interactive** marque le point auquel la page apparaît suffisamment prête pour gérer les interactions utilisateur.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png" alt-text="Section Mesures" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png":::
   Section **Mesures**  
:::image-end:::  

Sélectionnez le bouton bascule mis en surbrillon dans la **** figure suivante pour afficher une description pour chaque métrique, puis choisissez En savoir plus pour lire la documentation à ce sujet.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png" alt-text="Sélectionnez le bouton bascule mis en surbrillon pour développer les éléments Mesures" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png":::
   Sélectionnez le bouton bascule mis en surbrillon pour développer les éléments Mesures  
:::image-end:::  

Les mesures ci-dessous sont une collection de captures d’écran qui vous montrent à quoi ressemble la page telle qu’elle a été chargée.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Captures d’écran de l’aperçu de la page lors du chargement" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   Captures d’écran de l’aperçu de la page lors du chargement  
:::image-end:::  

La section **Opportunités** fournit des conseils spécifiques sur l’amélioration des performances de charge de cette page spécifique.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Section Opportunités" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   Section **Opportunités**  
:::image-end:::  

Choisissez l’opportunité d’en savoir plus à ce sujet.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png" alt-text="Éliminer les opportunités de ressources de blocage de rendu" lightbox="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png":::
   **Éliminer les opportunités de ressources de blocage de rendu**  
:::image-end:::  

Choose **Learn More** to display documentation about why an opportunity is important, and specific recommendations on how to fix it.  

:::image type="complex" source="../media/speed-web-dev-performance-audits.msft.png" alt-text="Documentation relative à l’élimination des ressources de blocage du rendu" lightbox="../media/speed-web-dev-performance-audits.msft.png":::
   Documentation relative à **l’élimination des ressources de blocage du rendu**  
:::image-end:::  

La section **Diagnostics** fournit plus d’informations sur les facteurs qui contribuent au temps de chargement de la page.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png" alt-text="Section Diagnostics" lightbox="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png":::
   Section **Diagnostics**  
:::image-end:::  

La section **Audits passés** vous montre ce que le site fait correctement.  Choisissez de développer la section.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png" alt-text="Section Audits passés" lightbox="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png":::
   Section **Audits passés**  
:::image-end:::  

## <a name="step-2-experiment"></a>Étape 2 : Expérimenter  

La section Opportunités de votre rapport d’audit vous donne des conseils pour améliorer les performances de la page.  Dans cette section, vous implémentez les modifications recommandées sur la base de code, en auditant le site après chaque modification afin de mesurer l’impact sur la vitesse du site.  

### <a name="enable-text-compression"></a>Activer la compression de texte  

Votre rapport indique que le fait d’éviter d’importantes charges utiles réseau est l’une des meilleures opportunités pour améliorer les performances de la page.  L’activation de la compression de texte est une opportunité d’améliorer les performances de la page.  

La compression de texte consiste à réduire ou compresser la taille d’un fichier texte avant de l’envoyer sur le réseau.  Semblable à la façon dont vous pouvez archiver un répertoire avant de l’envoyer pour réduire la taille.  

Avant d’activer la compression, voici quelques méthodes pour vérifier manuellement si les ressources de texte sont compressées.  

1.  Choisissez **l’outil** Réseau.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network.msft.png" alt-text="Panneau réseau" lightbox="../media/speed-glitch-tony-remix-network.msft.png":::
       **L’outil** Réseau  
    :::image-end:::  
    
1.  Sélectionnez **l’icône Paramètre** réseau.  
1.  Cochez **la case Utiliser les lignes De grandes demandes.**  La hauteur des lignes du tableau des demandes réseau augmente.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png" alt-text="Lignes de grande taille dans le tableau des demandes réseau" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png":::
       Lignes de grande taille dans le tableau des demandes réseau  
    :::image-end:::  
    
1.  Si la **colonne Taille** dans le tableau des demandes réseau n’est pas affichée, choisissez l’en-tête de tableau > **Taille**.  

Chaque **cellule Size** affiche deux valeurs.  La valeur supérieure est la taille de la ressource téléchargée.  
La valeur inférieure est la taille de la ressource non compressée.  Si les deux valeurs sont identiques, la ressource n’est pas compressée lorsqu’elle est envoyée sur le réseau.  Par exemple, dans la figure précédente, les valeurs supérieure et inférieure pour `bundle.js` sont `1.2 MB` et `1.2 MB` .  

Vérifiez la compression en inspectant les en-têtes HTTP d’une ressource :  

1.  Choose `bundle.js` .  
1.  Choisissez le **panneau En-têtes.**  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png" alt-text="Panneau En-têtes" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png":::
       Panneau **En-têtes**  
    :::image-end:::  
    
1.  Recherchez **un en-tête dans** la section `content-encoding` En-têtes de réponse.  Un `content-encoding` titre n’est pas affiché, ce qui signifie `bundle.js` qu’il n’a pas été compressé.  Lorsqu’une ressource est compressée, cet en-tête est généralement définie sur `gzip` `deflate` , ou `br` .  Pour obtenir une explication des valeurs, accédez à [Directives][MDNContentEncodingDirectives].  

Suffisamment avec les explications.  Il est temps d’apporter des modifications.  Activez la compression de texte en ajoutant quelques lignes de code :  

1.  Dans l’onglet Éditeur, ** choisissezserver.js**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js.msft.png" alt-text="Modifier server.js" lightbox="../media/speed-glitch-tony-remix-server-js.msft.png":::
       Edit `server.js`  
    :::image-end:::  
    
1.  Ajoutez le code suivant à **server.js**.  Veillez à le `app.use(compression())` placer avant `app.use(express.static('build'))` .  

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
    > En règle générale, vous devez installer le package via quelque chose comme , mais `compression` cela a déjà été fait pour `npm i -S compression` vous.  
    
1.  Attendez que Glitch déploie la nouvelle build du site.  L’animation originale en de côté **des outils** signifie que le site est en cours de reconstruction et de redéploiement.  La modification est prête lorsque l’animation en de côté des **outils** disparaît.  Choose **Show** and choose **In a New Window** again.  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js-edited.msft.png" alt-text="The animation that indicates that the site is getting built" lightbox="../media/speed-glitch-tony-remix-server-js-edited.msft.png":::
       The animation that indicates that the site is getting built  
    :::image-end:::  
    -->  
    
Utilisez les flux de travail que vous avez appris précédemment pour vérifier manuellement que la compression fonctionne :  

1.  Revenir à l’onglet de démonstration et actualiser la page.  La **colonne Taille** doit maintenant afficher 2 valeurs différentes pour les ressources de texte telles que `bundle.js` .  Dans la figure ci-dessous, la valeur supérieure de for est la taille du fichier qui a été envoyé sur le réseau, et la valeur inférieure est la taille du fichier non `256 KB` `bundle.js` `1.2 MB` compressé.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-main.msft.png" alt-text="La colonne Taille affiche désormais 2 valeurs différentes pour les ressources de texte" lightbox="../media/speed-glitch-tony-remix-network-main.msft.png":::
       La **colonne Taille** affiche désormais 2 valeurs différentes pour les ressources de texte  
    :::image-end:::  
    
1.  La section **En-têtes de** `bundle.js` réponse pour doit maintenant inclure un `content-encoding: gzip` en-tête.
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png" alt-text="La section En-têtes de réponse contient désormais un en-tête d’encodage de contenu" lightbox="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png":::
       La section **En-têtes de** réponse contient désormais un en-tête d’encodage de contenu  
    :::image-end:::  
    
Auditer de nouveau la page pour mesurer le type d’impact de la compression de texte sur les performances de charge de la page :  

1.  Choisissez **l’outil Audits.**  
1.  Choose **Perform an audit** \( Perform an audit ![ ](../media/perform-icon.msft.png) \).  
1.  Laissez les paramètres identiques aux paramètres d’avant.  
1.  Choose **Run audit**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png" alt-text="Un rapport Audits après activation de la compression de texte" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png":::
       Un rapport Audits après activation de la compression de texte  
    :::image-end:::  
    
<!--  Woohoo!  That looks like progress.  -->  Votre score de performances global doit avoir augmenté, ce qui signifie que le site devient plus rapide.  

#### <a name="text-compression-in-the-real-world"></a>Compression de texte dans le monde réel  

La plupart des serveurs ont vraiment des correctifs simples comme celui-ci pour activer la compression !  Il vous suffit d’effectuer une recherche sur la configuration du serveur que vous utilisez pour compresser du texte.  

### <a name="resize-images"></a>Resize images  

Votre rapport indique que le fait d’éviter d’importantes charges utiles réseau est l’une des meilleures opportunités pour améliorer les performances de la page.  Le re dimensionnement des images permet de réduire la taille de la charge utile du réseau.  Si votre utilisateur affiche vos images sur un écran d’appareil mobile de 500 pixels de large, l’envoi d’une image de 1 500 pixels ne sert à rien.  Dans l’idéal, vous envoyez une image de 500 pixels au maximum.  

1.  Dans votre rapport, choisissez **d’éviter** les charges utiles réseau importantes pour afficher les images qui doivent être resa capacité.  Il semble que 2 des fichiers jpg font plus de 2 000 Ko, ce qui est plus important que nécessaire.  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png" alt-text="Details about the properly size images opportunity" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png":::
       Details about the properly size images opportunity  
    :::image-end:::  
    -->
    
1.  De retour dans l’onglet Éditeur, ouvrez `src/model.js` .  
1.  Remplacez `const dir = 'big'` par `const dir = 'small'` .  Ce répertoire contient des copies des mêmes images qui ont été reserrées.  
1.  Auditez de nouveau la page pour afficher l’impact de la modification sur les performances de charge.  
    
    :::image type="complex" source="../media/speed-glitch-compression-small-images-audits-performance.msft.png" alt-text="Un rapport Audits après re resserr des images" lightbox="../media/speed-glitch-compression-small-images-audits-performance.msft.png":::
       Un rapport Audits après re resserr des images  
    :::image-end:::  
    
La modification affichée n’a qu’un impact mineur sur le score de performances global.  Toutefois, une chose que le score ne montre pas clairement est la quantité de données réseau que vous économisez vos utilisateurs.  La taille totale des anciennes photos était d’environ 5,3 mégaoctets, alors qu’elle n’est plus qu’environ 0,18 mégaoctets.  

#### <a name="resizing-images-in-the-real-world"></a>Re resizing images in the real world  

Pour une petite application, une telle re taille peut être suffisante.  Mais pour une application de grande taille, ce n’est évidemment pas évolutif.  Voici quelques stratégies de gestion des images dans les applications de grande taille :  

*   Resize images during your build process.  
*   Créez plusieurs tailles de chaque image pendant le processus de création, puis `srcset` utilisez-la dans votre code.  Au moment de l’utilisation, le navigateur s’occupe de choisir la taille la plus grande pour l’appareil.  
    <!--Navigate to [Relative-sized images][relative].  -->
    
<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   Utilisez une image CDN qui vous permet de re tailler dynamiquement une image lorsque vous la demandez.  
*   Au minimum, optimisez chaque image.  Cela peut générer d’importantes économies.  
  L’optimisation consiste à exécuter une image via un programme spécial qui réduit la taille du fichier image.  Pour plus d’informations, accédez à [Optimisation de l’image essentielle.][EssentialImageOptimization]  
    
### <a name="eliminate-render-blocking-resources"></a>Éliminer les ressources de blocage de rendu  

Votre dernier rapport indique que l’élimination des ressources de blocage de rendu est désormais la plus grande opportunité.  

Une ressource de blocage de rendu est un fichier JavaScript ou CSS externe que le navigateur doit télécharger, explorer et exécuter avant d’afficher la page.  L’objectif est d’exécuter uniquement le code CSS et JavaScript principal requis pour afficher la page correctement.  

La première tâche consiste ensuite à trouver le code que vous n’avez pas besoin d’exécuter lors du chargement de la page.  

1.  Choisissez **Éliminer les ressources de blocage de rendu** pour afficher les ressources qui bloquent :  
    `lodash.js` et `jquery.js` .  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png" alt-text="Plus d’informations sur l’opportunité d’éliminer les ressources de blocage de rendu" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png":::
       Plus d’informations sur **l’opportunité d’éliminer les ressources de blocage de rendu**  
    :::image-end:::  
    
1.  Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) `Coverage` **** pour ouvrir le menu Commande, commencer à taper, puis choisissez Afficher la couverture.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png" alt-text="Ouvrir le menu Commande à partir du panneau Audits" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png":::
       Ouvrir le menu Commande à partir du **panneau Audits**  
    :::image-end:::  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png" alt-text="L’outil Couverture" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png":::
       **L’outil Couverture**  
    :::image-end:::  
    
1.  Choose **Refresh** \( ![ Refresh ](../media/reload-icon.msft.png) \).  **L’outil** Couverture fournit une vue d’ensemble de la quantité de code dans , et s’exécute pendant le chargement `bundle.js` de la `jquery.js` `lodash.js` page.  Dans la figure ci-après, environ 76 % et 30 % des fichiers jQuery et Lodash ne sont pas utilisés, respectivement.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png" alt-text="Rapport de couverture" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png":::
       Rapport de couverture  
    :::image-end:::  
    
1.  Choisissez la `jquery.js` ligne.  DevTools ouvre le fichier dans l’outil **Sources.**  Si une ligne de code est en cours d’utilisation, une barre bleue s’affiche à côté de cette ligne.  Une barre rouge signifie que la ligne de code n’a pas été exécuté et n’est absolument pas nécessaire lors du chargement de la page web.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png" alt-text="Affichage du fichier jQuery dans l’outil Sources" lightbox="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png":::
       Affichage du fichier jQuery dans l’outil **Sources**  
    :::image-end:::  
    
1.  Faites défiler le code jQuery.  Certaines des lignes qui s’exécutent ne sont en fait que des commentaires.  Pour bander les commentaires et réduire la taille du fichier, exécutez le code par le biais d’une application ou d’un script de minifier.  

En bref, lorsque vous travaillez avec **** votre propre code, l’outil Couverture vous permet d’analyser votre code, ligne par ligne, et d’expédier uniquement le code nécessaire au chargement de la page.  

Les fichiers `jquery.js` et les `lodash.js` fichiers sont-ils nécessaires pour charger la page ?  **L’outil de blocage** des demandes affiche ce qui se produit lorsque les ressources ne sont pas disponibles.  

1.  Choisissez **l’outil** Réseau.  
1.  Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) pour ouvrir à nouveau le menu commande.  
1.  Commencez à `blocking` taper, puis choisissez **Afficher le blocage des demandes.**  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png" alt-text="Outil de blocage des demandes" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png":::
       Outil **de blocage des** demandes  
    :::image-end:::  
    
1.  Choose **Add Pattern** \( Add Pattern ![ ](../media/add-pattern-icon.msft.png) \), type , and then select `/libs/*` to `Enter` confirm.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png" alt-text="Ajouter un modèle pour bloquer toute demande dans le répertoire libs" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png":::
       Ajouter un modèle pour bloquer toute demande à `libs` l’annuaire  
    :::image-end:::  
    
1.  Actualisez la page.  Les demandes jQuery et Lodash sont rouges, ce qui signifie que les demandes ont été bloquées.   La page se charge toujours et est interactive. Il semble donc que ces ressources ne soient pas nécessaires !  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png" alt-text="Le panneau Réseau indique que les demandes ont été bloquées" lightbox="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png":::
       **L’outil** Réseau indique que les demandes ont été bloquées  
    :::image-end:::  
    
1.  Choose **Remove all patterns** \( ![ Remove all patterns ](../media/remove-icon.msft.png) \) to delete the blocking `/libs/*` pattern.  
    
En règle générale, **l’outil** de blocage des demandes est utile pour simuler le comportement de votre page lorsqu’une ressource donnée n’est pas disponible.  

Maintenant, supprimez les références à ces fichiers du code et auditer à nouveau la page :  

1.  De retour dans l’onglet Éditeur, ouvrez `template.html` .  
1.  Supprimez les éléments `<script src="/libs/lodash.js">` et `<script src="/libs/jquery.js"></script>`.  
1.  Attendez que le site soit re-build et re-déployé.  
1.  Auditer à nouveau la page à partir de **l’outil Audits.**  Votre score global devrait de nouveau avoir été amélioré.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png" alt-text="Un rapport Audits après la suppression des ressources de blocage de rendu" lightbox="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png":::
       Un **rapport Audits** après la suppression des ressources de blocage de rendu  
    :::image-end:::  
    
#### <a name="optimizing-the-critical-rendering-path-in-the-real-world"></a>Optimisation du chemin d’accès de rendu critique dans le monde réel  

Le **chemin d’accès de** rendu critique fait référence au code dont vous avez besoin pour charger une page.  En règle générale, accélèrez le chargement de la page en expédiant uniquement du code critique pendant le chargement de la page, puis en chargeant différée tout le reste.  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   Il est peu probable que vous soyez en mesure de trouver des scripts que vous êtes en mesure de supprimer totalement, mais vous trouverez peut-être de nombreux scripts que vous n’avez pas besoin de demander pendant le chargement de la page et qui peuvent être demandés de manière asynchrone.  <!--Navigate to [Using async or defer][async].  -->  
*   Si vous utilisez une infrastructure, vérifiez si elle dispose d’un mode de production.  Ce mode peut utiliser une fonctionnalité telle que l’arborescence [afin][WebpackTreeShaking] d’éliminer le code inutile qui bloque le rendu critique.  
    
<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### <a name="do-less-main-thread-work"></a>Faire moins de travail de thread principal  

Votre dernier rapport présente quelques économies potentielles mineures dans la section Opportunités, mais si vous examinez la section Diagnostics, il semble que le goulot d’étranglement le plus important soit une activité de thread principale trop importante.  

Le thread principal est l’endroit où le navigateur fait la plupart des travaux nécessaires à l’affichage d’une page, telles que l’affichage et l’exécution de CODE HTML, CSS et JavaScript.  

L’objectif est d’utiliser le panneau Performance pour analyser le travail que le thread principal fait pendant le chargement de la page et trouver des moyens de différer ou de supprimer le travail inutile.  

1.  Choisissez **l’outil Performance.**  
1.  Choose **Capture Paramètres** \( Capture Paramètres ![ ](../media/capture-icon.msft.png) \).  
1.  Définissez **le** réseau **sur le 3G** et le **processeur** **à 6x le ralentissement.**  Les appareils mobiles ont généralement plus de contraintes matérielles que les ordinateurs portables ou les ordinateurs de bureau. Ces paramètres vous offrent donc la même expérience que si vous utilisiez un appareil moins puissant.  
1.  Choose **Refresh** \( ![ Refresh ](../media/reload-icon.msft.png) \).  DevTools actualise la page, puis produit une visualisation de tout le travail effectué afin de charger la page.  Cette visualisation est appelée **suivi**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png" alt-text="Suivi de l’outil Performance du chargement de la page" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png":::
       Suivi **de l’outil** Performance du chargement de la page  
    :::image-end:::  
    
Le suivi montre l’activité dans l’ordre chronologique, de gauche à droite.  Les graphiques FPS, processeur et NET en haut vous donnent une vue d’ensemble des images par seconde, de l’activité processeur et de l’activité réseau.  Bloc de jaune mis en surbrillant dans la figure suivant, l’UC était complètement occupée par l’activité de script.  Il s’agit d’un indice qui vous permet d’accélérer le chargement de la page en faisant moins de travail JavaScript.  

:::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png" alt-text="Section Vue d’ensemble du suivi" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png":::
   Section Vue d’ensemble du suivi  
:::image-end:::  

Examinez la trace pour trouver des méthodes pour faire moins de travail JavaScript :  

1.  Sélectionnez la section **Minutages** pour la développer.  En fonction du fait qu’il [][MDNUserTimingApi] peut y avoir plusieurs mesures de minutage de React, il semble que l’application de Tony utilise le mode de développement de React.  Le passage au mode de production de React peut donner des résultats faciles en terme de performances.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png" alt-text="La section Minutage" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png":::
       La section **Minutage**  
    :::image-end:::  
    
1.  Sélectionnez **de nouveau Minutages** pour réduire cette section.  
1.  Parcourez la section **Principale.**  Cette section présente un journal chronologique de l’activité du thread principal, de gauche à droite.  L’axe y (de haut en bas) indique pourquoi les événements se sont produits.  Par exemple, dans la figure suivante, l’événement a provoqué l’exécuter, ce qui a provoqué l’exécuter, ce qui a provoqué l’exécuter, `Evaluate Script` `(anonymous)` `(anonymous)` `__webpack__require__` etc.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png" alt-text="Section Main" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png":::
       Section **Main**  
    :::image-end:::  
    
1.  Faites défiler vers le bas jusqu’au bas de la section **Main.**  Lorsque vous utilisez une infrastructure, la majeure partie de l’activité supérieure est due à l’infrastructure, qui est généralement hors de votre contrôle.  L’activité provoquée par votre application se trouve généralement en bas.  Dans cette application, il semble qu’une fonction nommée soit à l’origine d’un grand nombre de `App` demandes à une `mineBitcoin` fonction.  Il semble que Tony utilise peut-être les appareils de ses fans pour se servir de la cryptomonnaie...  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png" alt-text="Pointer sur l’activité mineBitcoin" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png":::
       Pointer sur `mineBitcoin` l’activité  
    :::image-end:::  
    
    > [!NOTE]
    > Bien que les demandes que votre infrastructure effectue soient généralement hors de votre contrôle, vous pouvez parfois structurer votre application d’une manière qui entraîne une utilisation inefficace de l’infrastructure.  La réorganisation de votre application afin d’utiliser efficacement l’infrastructure est un moyen de réduire le travail de thread principal.  Toutefois, cela nécessite une connaissance approfondie du fonctionnement de votre infrastructure et du type de modifications que vous a faites dans votre propre code afin d’utiliser l’infrastructure plus efficacement.  
    
1.  Développez la section Bas vers **le** haut.  Cet onglet décompose les activités qui ont pris le plus de temps.  Si rien n’est affiché dans la section Bottom-Up, choisissez l’étiquette de la section **Main.**  La section **Bas vers le haut** affiche uniquement les informations concernant l’activité ou le groupe d’activités que vous avez actuellement sélectionné.  Par exemple, si vous avez choisi l’une des activités, la section Bas vers le haut affiche uniquement les informations `mineBitcoin` de cette activité. ****  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png" alt-text="Onglet Bottom-Up de l’onglet" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png":::
       Onglet **Bas vers le** haut  
    :::image-end:::  
    
La **colonne Temps** libre vous indique le temps passé directement dans chaque activité.  Par exemple, dans la figure suivante, environ 63 % du temps du thread principal a été passé sur la `mineBitcoin` fonction.  

Il est temps de vérifier si l’utilisation du mode production et la réduction de l’activité JavaScript peuvent accélérer le chargement de la page.  Démarrez avec le mode de production :  

1.  Dans l’onglet Éditeur, ouvrez `webpack.config.js` .  
1.  Change `"mode":"development"` to `"mode":"production"` .  
1.  Attendez le déploiement de la nouvelle build.  
1.  Auditer à nouveau la page.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png" alt-text="Un rapport Audits après avoir configuré webpack pour utiliser le mode production" lightbox="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png":::
       Un rapport Audits après avoir configuré webpack pour utiliser le mode production  
    :::image-end:::  
    
Réduisez l’activité JavaScript en supprimant la demande à `mineBitcoin` :  

1.  Dans l’onglet Éditeur, ouvrez `src/App.jsx` .  
1.  Commentez la demande dans `this.mineBitcoin(1500)` `constructor` le .  
1.  Attendez le déploiement de la nouvelle build.  
1.  Auditer à nouveau la page.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png" alt-text="Un rapport Audits après la suppression de travail JavaScript inutile" lightbox="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png":::
       Un rapport Audits après la suppression de travail JavaScript inutile  
    :::image-end:::  
    
Il semble que cette dernière modification a provoqué un saut important des performances !  

> [!NOTE]
> Cette section a présenté brièvement le panneau Performances.  Pour en savoir plus sur l’analyse des performances de page, accédez à [Référence de l’analyse des performances.][DevtoolsEvaluatePerformanceReference]  

<!--todo: add section when available -->  

#### <a name="doing-less-main-thread-work-in-the-real-world"></a>Faire moins de travail de thread principal dans le monde réel  

En règle générale, l’outil **Performance** est le moyen le plus courant de comprendre l’activité que fait votre site pendant son chargement et de trouver des moyens de supprimer les activités inutiles.  

Si vous préférez une approche qui ressemble davantage, l’API de minutage de l’utilisateur vous permet de marquer arbitrairement certaines phases du cycle de vie de votre application, afin de suivre la durée de chacune de ces `console.log()` phases. [][MDNUserTimingApi]  

## <a name="summary"></a>Résumé  

*   Chaque fois que vous définissez pour optimiser les performances de charge d’un site, commencez toujours par un audit.  L’audit établit une ligne de base et vous donne des conseils sur la façon d’améliorer.  
*   A effectuer une modification à la fois et auditer la page web après chaque modification afin d’afficher l’impact de cette modification isolée sur les performances.  

<!--
## Next steps  

*   Run audits on your own site!  If you need help interpreting your report, or finding ways to improve your load performance, check out [Feedback](#feedback) for ways to get help from the DevTools community.  Stack Overflow, the mailing list, or Twitter are probably best for these types of questions.  
*   Please leave [feedback](#feedback) on this tutorial.  I really do use the data to make better tutorials for you.  
-->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: ../evaluate-performance/reference.md "Référence de l’analyse des performances | Documents Microsoft"  

[CourseraIntroductionWebDevelopmentClass]: https://www.coursera.org/learn/web-development#syllabus "Présentation des classes de développement web | Coursera"  

[EssentialImageOptimization]: https://images.guide "Optimisation des images essentielles"  

[MDNContentEncodingDirectives]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Encoding#Directives "Directives : | MDN"  
[MDNUserTimingApi]: https://developer.mozilla.org/docs/Web/API/User_Timing_API "Api de minutage utilisateur | MDN"  

[WebpackTreeShaking]: https://webpack.js.org/guides/tree-shaking "Arborescence de | webpack"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
