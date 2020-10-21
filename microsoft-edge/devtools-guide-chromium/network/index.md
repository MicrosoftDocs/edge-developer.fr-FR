---
description: Didacticiel sur les fonctionnalités les plus populaires relatives au réseau dans Microsoft Edge DevTools.
title: Examiner l’activité réseau dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: a55ff05e29817c483cbf13b8713ef37cf96424d5
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125425"
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

# Examiner l’activité réseau dans Microsoft Edge DevTools  

Il s’agit d’un didacticiel d’utilisation des fonctionnalités DevTools les plus fréquemment utilisées associées à l’inspection de l’activité réseau d’une page.  

Pour parcourir les fonctionnalités, voir [référence réseau][DevtoolsNetworkReference] .  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## Quand utiliser le panneau réseau  

En règle générale, utilisez le panneau réseau pour vous assurer que les ressources sont téléchargées ou chargées comme prévu.  Les cas d’utilisation les plus courants du panneau réseau sont les suivants:  

*   Vérifiez que les ressources sont en train d’être chargées ou téléchargées du tout.  
*   Inspecter les propriétés d’une ressource individuelle, par exemple, les en-têtes HTTP, le contenu, la taille, etc.  
    
Si vous cherchez à améliorer les performances de chargement de page, **ne démarrez pas** le panneau réseau.  Il existe de nombreux types de problèmes de performances de chargement qui ne sont pas liés à l’activité réseau.  Commencez avec le panneau audits, car il vous donne des suggestions ciblées sur l’amélioration de votre page.  Voir [optimiser la vitesse du site Web][DevtoolsSpeedGetStarted].  

## Ouvrir le panneau réseau  

Pour tirer le meilleur parti de ce didacticiel, ouvrez la démonstration et testez les fonctionnalités de la page de démonstration.  

1.  Ouvrir la [démonstration commencer][GlitchNetworkGetStarted].  
    
    :::image type="complex" source="../media/network-glitch-inspect-network-activity-demo.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-inspect-network-activity-demo.msft.png":::
       La démonstration  
    :::image-end:::  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    :::image type="complex" source="../media/network-tutorial/windows.msft.png" alt-text="La démonstration" lightbox="../media/network-tutorial/windows.msft.png":::
       The demo in one window and this tutorial in a different window  
    :::image-end:::  
    -->
    
1.  [Ouvrez devtools][DevToolsOpen] en appuyant sur `Control` + `Shift` + `J` \ (Windows, Linux \) ou `Command` + `Option` + `J` \ (MacOS \).  Le panneau **console** s’ouvre.  
    
    :::image type="complex" source="../media/network-glitch-console.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-console.msft.png":::
       La **console**  
    :::image-end:::  
    
    Vous pouvez [ancrer devtools en bas de la fenêtre][DevToolsCustomizePlacement].  
    
    :::image type="complex" source="../media/network-glitch-console-bottom.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-console-bottom.msft.png":::
       DevTools ancré en bas de la fenêtre  
    :::image-end:::  
    
1.  Sélectionnez l’onglet **Network (réseau** ).  Le volet **réseau** s’ouvre.  
    
    :::image type="complex" source="../media/network-glitch-network-bottom.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-bottom.msft.png":::
       Outil **console** dans le devtools ancré en bas de la fenêtre  
    :::image-end:::  
    
Pour le moment, le volet réseau est vide.  DevTools uniquement les journaux d’activité réseau après l’ouverture et aucune activité réseau ne s’est produite depuis que vous avez ouvert DevTools.  

## Journalisation de l’activité du réseau  

Pour afficher l’activité réseau provoquée par une page:  

1.  Rechargez la page.  Le panneau réseau enregistre toutes les activités du réseau dans le **Journal du réseau**.  
    
    :::image type="complex" source="../media/network-glitch-network.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network.msft.png":::
       **Journal du réseau**  
    :::image-end:::  
    
    Chaque ligne du **Journal réseau** représente une ressource.  Par défaut, les ressources sont répertoriées dans l’ordre chronologique.  La principale ressource correspond généralement au document HTML principal.  Le dernier élément de la ressource est le dernier demandé.  
    
    Chaque colonne représente des informations sur une ressource.  Dans la figure précédente, les colonnes par défaut sont affichées.  

    *   **Status**.  Code d’état HTTP de la réponse.  
    *   **Type**.  Type de ressource.  
    *   **Initiator**.  La cause de la demande de ressource.  La sélection d’un lien dans la colonne initiateur vous permet d’accéder au code source à l’origine de la demande.  
    *   **Temps**.  Durée de la requête.  
    *   En **cascade**.  Représentation graphique des différentes étapes de la requête.  Placez le pointeur de la souris sur une cascade pour afficher une répartition.  
    
    > [!NOTE]
    > Le graphique au-dessus du journal réseau est appelé vue d’ensemble.  Dans ce didacticiel, vous n’utiliserez pas le graphique de vue d’ensemble et vous pouvez le masquer.  Voir [masquer le volet vue d’ensemble][DevtoolsReferenceHideOverview].
    
1.  Après l’ouverture de DevTools, elle enregistre l’activité réseau dans le journal du réseau.  
    Pour en expliquer le résultat, observez d’abord la partie inférieure du **Journal du réseau** et prenez note de la dernière activité.  
1.  À présent, sélectionnez le bouton **obtenir des données** dans la démonstration.  
1.  Regardez de nouveau le journal du **réseau** .  Une nouvelle ressource doit apparaître `getstarted.json` .  Le fait de sélectionner le bouton **Get Data** a entraîné la demande de ce fichier.  
    
    :::image type="complex" source="../media/network-glitch-network-new-resource.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-new-resource.msft.png":::
       Nouvelle ressource dans le **Journal réseau**  
    :::image-end:::  
    
## Afficher plus d’informations  

Les colonnes du journal du réseau peuvent être configurées.  Vous pouvez masquer les colonnes que vous n’utilisez pas.  
Il existe également plusieurs colonnes qui sont masquées par défaut, qui peuvent être utiles.  

1.  Cliquez avec le bouton droit sur l’en-tête de la table du journal du réseau et sélectionnez **Domain (domaine**).  Le domaine de chaque ressource est désormais affiché.  
    
    :::image type="complex" source="../media/network-glitch-network-edit-column.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-edit-column.msft.png":::
       Activez la colonne Domain (domaine)  
    :::image-end:::  
    
    > [!TIP]
    > Pour afficher l’URL complète d’une ressource, placez le pointeur de la souris sur la cellule de la colonne **nom** .  
    
## Simuler une connexion réseau plus lente  

La connexion réseau de l’ordinateur que vous utilisez pour créer des sites est probablement plus rapide que les connexions réseau des appareils mobiles de vos utilisateurs.  La limitation de la page vous permet d’obtenir une meilleure idée du temps nécessaire au chargement d’une page sur un appareil mobile.  

1.  Sélectionner la liste déroulante de **limitation** , définie sur **en ligne** par défaut.  
    
    :::image type="complex" source="../media/network-glitch-network-throttling.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-throttling.msft.png":::
       Activer la limitation  
    :::image-end:::  
    
1.  Sélectionnez **3G lente**.  
    
    :::image type="complex" source="../media/network-glitch-network-throttling-slow-3g.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-throttling-slow-3g.msft.png":::
       Sélectionnez 3G lente  
    :::image-end:::  
    
1.  Appuyez longuement sur **rechargez** \ ( ![ Reload ][ImageRefreshIcon] \), puis sélectionnez **Vider le cache et télécharger le matériel**.  
    
    :::image type="complex" source="../media/network-glitch-empty-cache-and-hard-reset.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-empty-cache-and-hard-reset.msft.png":::
       **Vider le cache et procéder au recharge**  
    :::image-end:::  
    
    Lorsque vous révisez les visites, le navigateur fournit généralement certains fichiers du [cache][MDNHTTPCache], ce qui accélère le chargement de la page.  Le **vidage du cache et du rechargement forcé** force le navigateur à accéder au réseau pour toutes les ressources.  Cette méthode est utile lorsque vous souhaitez voir la façon dont un visiteur commence à se charger de la page.  
    
    > [!NOTE]
    > Le flux **de travail vider le cache et le chargement papier** est uniquement disponible lorsque devtools est ouvert.  
    
## Capture de captures d’écran  

Les captures d’écran vous permettent de voir l’aspect d’une page au fil du temps pendant son chargement.  

1.  Sélectionnez \ ( ![ paramètres réseau ][ImageSettingsIcon] \) et cochez la case capturer les captures d' **écran** .
1.  Rechargez de nouveau la page par le biais du flux **de travail vider le cache et le chargement papier** .  Pour savoir comment procéder, voir [simuler une connexion plus lente](#simulate-a-slower-network-connection) si vous avez besoin d’un rappel.  
    Le volet capture d’écran fournit des miniatures illustrant la manière dont la page a été recherchée à différents points au cours du processus de chargement.  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-screenshots.msft.png":::
       Captures d’écran du chargement de la page  
    :::image-end:::  
    
1.  Sélectionnez la première miniature.  DevTools indique l’activité réseau qui se produit à ce moment précis.  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots-first.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-screenshots-first.msft.png":::
       Activité réseau qui se produit pendant la première capture d’écran  
    :::image-end:::  
    
1.  Sélectionnez de nouveau \ ( ![ paramètres réseau ][ImageSettingsIcon] \) et désélectionnez la case à cocher **capture** des captures d’écran pour fermer le volet captures d’écran.
1.  Rechargez la page.  
    
## Inspecter les détails de la ressource  

Pour plus d’informations à ce sujet, sélectionnez une ressource.  Essayez-le maintenant:  

1.  Sélectionnez `getstarted.html` .  L’onglet **en-têtes** est affiché.  Utilisez cet onglet pour inspecter les en-têtes HTTP.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-headers.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-resources-headers.msft.png":::
       Onglet **en-têtes**  
    :::image-end:::  
    
1.  Sélectionnez l’onglet **Aperçu** .  Un rendu de base du code HTML est affiché.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-preview.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-resources-preview.msft.png":::
       Onglet **Aperçu**  
    :::image-end:::  
    
    Cet onglet est utile lorsqu’une API renvoie un code d’erreur en HTML.  Il est possible que vous puissiez lire le code HTML affiché plus facilement que le code source HTML ou lorsque vous examinez des images.  

1.  Sélectionnez l’onglet **réponse** .  Le code source HTML est affiché.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-response.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-resources-response.msft.png":::
       Onglet **réponse**  
    :::image-end:::  
    
    > [!TIP]
    > Lorsqu’un fichier est minified, le fait de sélectionner le bouton **mettre** en forme \ ( ![ format ][ImageFormatIcon] \) en bas de l’onglet **réponse** a reformaté le contenu du fichier pour faciliter la lecture.  
    
1.  Sélectionnez l’onglet **minutage** .  Le détail de l’activité réseau de cette ressource est affiché.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-timing.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-resources-timing.msft.png":::
       Onglet **minutage**  
    :::image-end:::  
    
1.  Sélectionnez **Close** ( ![ fermer ][ImageCloseIcon] ) pour afficher de nouveau le journal du réseau.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-close-tabs.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-resources-close-tabs.msft.png":::
       Bouton **Fermer**  
    :::image-end:::  
    
## Effectuer une recherche dans les en-têtes et réponses du réseau  

Le volet de **recherche** vous permet d’effectuer une recherche dans les en-têtes et réponses HTTP de toutes les ressources pour une chaîne ou une expression régulière spécifique.  

Par exemple, supposons que vous vouliez vérifier que vos ressources utilisent des **stratégies de cache**raisonnables.  

<!--TODO: add cache policies section when available  -->

1.  Sélectionnez **Rechercher** \ ( ![ Rechercher ][ImageSearchIcon] \).  Le volet de recherche s’ouvre à gauche du journal du réseau.  
    
    :::image type="complex" source="../media/network-glitch-network-search-empty.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-search-empty.msft.png":::
       Le volet de **recherche**  
    :::image-end:::  
    
1.  Tapez `Cache-Control` et sélectionnez `Enter` .  Le volet de recherche répertorie toutes les instances `Cache-Control` qu’il recherche dans les en-têtes de ressources ou le contenu.  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-search-cache-control.msft.png":::
       Résultats de la recherche pour  `Cache-Control`  
    :::image-end:::  
    
1.  Sélectionnez un résultat pour afficher la ressource dans laquelle le résultat a été trouvé.  Si vous examinez les détails de la ressource, sélectionnez un résultat pour y accéder directement.  Par exemple, si la requête se trouve dans un en-tête, l’onglet en-têtes s’ouvre.   Si la requête se trouve dans le contenu, l’onglet **réponse** s’ouvre.  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png":::
       Résultat de la recherche en surbrillance dans l’onglet **en-têtes**  
    :::image-end:::  
    
1.  Fermez le volet de recherche et l’onglet en-têtes.  
    
    :::image type="complex" source="../media/network-glitch-network-search-close.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-search-close.msft.png":::
       Boutons **Fermer**  
    :::image-end:::  
    
## Filtrer les ressources  

DevTools fournit de nombreux flux de travail pour filtrer les ressources qui ne sont pas pertinentes pour la tâche en cours.  

:::image type="complex" source="../media/network-glitch-network-filter-empty.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-filter-empty.msft.png":::
   Barre d’outils **filtres**  
:::image-end:::  

Par défaut, la barre d’outils **filtres** doit être activée.  Si ce n’est pas le cas:  

1.  Choisissez **filtre** \ ( ![ filtre ][ImageFilterIcon] \) pour l’afficher.  
    
### Filtrer par chaîne, expression régulière ou propriété  

La zone de texte **filtre** prend en charge différents types de filtrage.  

1.  Entrez `png` dans la zone de texte du **filtre** .  Seuls les fichiers qui contiennent le texte `png` sont affichés.  Dans ce cas, les seuls fichiers correspondant au filtre sont les images PNG.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-png.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-filter-png.msft.png":::
       Filtre de chaîne  
    :::image-end:::  
    
1.  Entrez `/.*\.[cj]s+$/`.  DevTools filtre les ressources dont le nom ne se termine pas par un `j` ou après `c` suivi de 1 ou plusieurs `s` caractères.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-regex.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-filter-regex.msft.png":::
       Un filtre d’expression régulier  
    :::image-end:::  
    
1.  Entrez `-main.css`.  DevTools filtre `main.css` .  Si un autre fichier correspond au modèle, il sera également filtré.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-negative-statement.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-filter-negative-statement.msft.png":::
       Un filtre négatif  
    :::image-end:::  
    
1.  Entrez `domain:cdn.glitch.com` dans la zone de texte du **filtre** .  DevTools filtre les ressources disposant d’une URL qui ne correspond pas à ce domaine.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-property-value.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-filter-property-value.msft.png":::
       Filtre de propriétés  
    :::image-end:::  
    
    Pour obtenir la liste complète des propriétés filtrées [, voir filtrer les demandes par propriétés][DevtoolsReferenceProperty] .  
    
1.  Effacez la zone de texte du **filtre** d’un texte.  
    
### Filtrer par type de ressource  

Pour vous concentrer sur un certain type de fichier, tel que les feuilles de style:  

1.  Sélectionnez **CSS**.  Tous les autres types de fichiers sont filtrés.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-filter-file-type-css.msft.png":::
       Afficher les fichiers CSS uniquement  
    :::image-end:::  
    
1.  Pour afficher également les scripts, appuyez sur `Control` \ (Windows, Linux \) ou `Command` \ (MacOS \), puis sélectionnez **js**.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css-js.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-filter-file-type-css-js.msft.png":::
       Afficher les fichiers CSS et JS uniquement  
    :::image-end:::  
    
1.  Cliquez sur **toutes** pour supprimer les filtres et afficher de nouveau toutes les ressources.  
    
Pour plus d’autres flux de travail de filtrage, voir [Filtrer les demandes][DevtoolsNetworkReferenceFilter] .  

## Bloquer les demandes  

Quel est l’aspect et le comportement d’une page lorsque certaines ressources de la page ne sont pas disponibles?  Est-ce que l’opération échoue entièrement ou fonctionne-t-elle toujours?  Bloquer les requêtes à Rechercher:  

1.  Sélectionnez `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.  
    
    :::image type="complex" source="../media/network-glitch-network-cli-empty.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-cli-empty.msft.png":::
       **Menu de commandes**  
    :::image-end:::  
    
1.  Tapez `block` , sélectionnez **afficher le blocage de requête**, puis sélectionnez `Enter` .  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-cli-block.msft.png":::
       **Afficher le blocage de requête**  
    :::image-end:::  
    
1.  Choisissez **Ajouter un modèle** \ ( ![ Ajouter le modèle ][ImageAddIcon] \).  
1.  Entrez `main.css`.  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-add-pattern.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-cli-block-add-pattern.msft.png":::
       Bloquer `main.css`  
    :::image-end:::  
    
1.  Cliquez sur **Ajouter**.  
1.  Rechargez la page.  Comme prévu, le style de la page est légèrement gâché, car la feuille de style principale a été bloquée.  
    
    > [!NOTE]
    > `main.css`Ligne du journal du réseau.  Le texte rouge signifie que la ressource a été bloquée.
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-main-css.msft.png" alt-text="La démonstration" lightbox="../media/network-glitch-network-cli-block-main-css.msft.png":::
       `main.css` a été bloqué  
    :::image-end:::  
    
1.  Désélectionnez la case à cocher **activer le blocage de requête** .  

## Conclusion  

Félicitations, vous avez terminé le didacticiel.  Vous savez maintenant comment utiliser le panneau **réseau** dans Microsoft Edge devtools!

Accédez à la [référence réseau][DevtoolsNetworkReference] pour découvrir d’autres fonctionnalités devtools liées à l’examen de l’activité du réseau.  

## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddIcon]: ../media/add-icon.msft.png  
[ImageCloseIcon]: ../media/close-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageFormatIcon]: ../media/format-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageScreenshotsIcon]: ../media/screenshots-icon.msft.png  
[ImageSearchIcon]: ../media/search-icon.msft.png  
[ImageSettingsIcon]: ../media/settings-icon.msft.png

<!-- links -->  

<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: ../customize/placement.md "Changer la position de Microsoft Edge DevTools Documents Microsoft"  
[DevtoolsNetworkReference]: ./reference.md "Référence d’analyse du réseau | Documents Microsoft"
[DevtoolsNetworkReferenceFilter]: ./reference.md#filter-requests "Demandes de filtre-référence d’analyse du réseau | Documents Microsoft"  
[DevtoolsReferenceHideOverview]: ./reference.md#hide-the-overview-pane "Masquer le volet vue d’ensemble-référence d’analyse du réseau | Documents Microsoft"
[DevtoolsReferenceProperty]: ./reference.md#filter-requests-by-properties "Demandes de filtre par propriétés-référence d’analyse du réseau | Documents Microsoft"
[DevToolsOpen]: ../open.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Optimiser la vitesse de votre site Web avec Microsoft Edge DevTools | Documents Microsoft"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Examen de la démonstration d’activité réseau | Problème"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Mise en cache HTTP MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/network/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
