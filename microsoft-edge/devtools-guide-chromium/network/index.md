---
title: Examiner l’activité réseau dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 267b0113e07085dd565a3ff3437a3fcac2dff9d7
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611811"
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

1.  Ouvrir la [démonstration commencer][GlitchNetworkGetStarted] .  
    
    > ##### Figure1  
    > La démonstration  
    > ![La démonstration][ImagesTutorialDemo]  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    > ##### old Figure 2  
    > The demo in one window and this tutorial in a different window  
    > ![The demo in one window and this tutorial in a different window][ImagesTutorialWindows]  -->

1.  [Ouvrez devtools][DevToolsOpen] en appuyant sur `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \).  Le panneau **console** s’ouvre.  
    
    > ##### Figure 2  
    > La console  
    > ! [La console] [ImagesTutorialConsole]  
    
    Vous pouvez [ancrer devtools en bas de la fenêtre][DevToolsCustomizePlacement].  
    
    > ##### Figure3  
    > DevTools ancré en bas de la fenêtre  
    > ! [DevTools ancré en bas de la fenêtre] [ImagesTutorialDocked]  

1.  Sélectionnez l’onglet **Network (réseau** ).  Le volet réseau s’ouvre.  
    
    > ##### Figure 4  
    > DevTools ancré en bas de la fenêtre  
    > ! [DevTools ancré en bas de la fenêtre] [ImagesTutorialNetwork]  

Pour le moment, le volet réseau est vide.  DevTools uniquement les journaux d’activité réseau après l’ouverture et aucune activité réseau ne s’est produite depuis que vous avez ouvert DevTools.  

## Journalisation de l’activité du réseau   

Pour afficher l’activité réseau provoquée par une page:  

1.  Rechargez la page.  Le panneau réseau enregistre toutes les activités du réseau dans le **Journal du réseau**.  
    
    > ##### Figure 5  
    > Journal du réseau  
    > ! [Journal du réseau] [ImagesTutorialLog]  
    
    Chaque ligne du **Journal réseau** représente une ressource.  Par défaut, les ressources sont répertoriées dans l’ordre chronologique.  La principale ressource correspond généralement au document HTML principal.  Le dernier élément de la ressource est le dernier demandé.  
    
    Chaque colonne représente des informations sur une ressource.  La [**figure 6**](#figure-6) montre les colonnes par défaut:  

    *   **Status**.  Code d’état HTTP de la réponse.  
    *   **Type**.  Type de ressource.  
    *   **Initiator**.  La cause de la demande de ressource.  La sélection d’un lien dans la colonne initiateur vous permet d’accéder au code source à l’origine de la demande.  
    *   **Temps**.  Durée de la requête.  
    *   En **cascade**.  Représentation graphique des différentes étapes de la requête.  
        Placez le pointeur de la souris sur une cascade pour afficher une répartition.  
    
    > [!NOTE]
    > Le graphique au-dessus du journal réseau est appelé vue d’ensemble.  Dans ce didacticiel, vous n’utiliserez pas le graphique de vue d’ensemble et vous pouvez le masquer.  Voir [masquer le volet vue d’ensemble][DevtoolsReferenceHideOverview].
        
1.  Après l’ouverture de DevTools, elle enregistre l’activité réseau dans le journal du réseau.  
    Pour en expliquer le résultat, observez d’abord la partie inférieure du **Journal du réseau** et prenez note de la dernière activité.  
1.  À présent, sélectionnez le bouton **obtenir des données** dans la démonstration.  
1.  Regardez de nouveau le journal du **réseau** .  Une nouvelle ressource doit apparaître `getstarted.json` .  Le fait de sélectionner le bouton **Get Data** a entraîné la demande de ce fichier.  
    
    > ##### Figure 6  
    > Nouvelle ressource dans le journal réseau  
    > ! [Une nouvelle ressource dans le journal du réseau] [ImagesTutorialRuntime]  

## Afficher plus d’informations   

Les colonnes du journal du réseau peuvent être configurées.  Vous pouvez masquer les colonnes que vous n’utilisez pas.  
Il existe également plusieurs colonnes qui sont masquées par défaut, qui peuvent être utiles.  

1.  Cliquez avec le bouton droit sur l’en-tête de la table Journal du réseau et sélectionnez **Domain (domaine**).  Le domaine de chaque ressource est désormais affiché.  
    
    > ##### Figure 7  
    > Activation de la colonne Domain  
    > ! [Activation de la colonne Domain] [ImagesTutorialDomain]  
    
    > [!TIP]
    > Pour afficher l’URL complète d’une ressource, placez le pointeur de la souris sur la cellule de la colonne **nom** .  

## Simuler une connexion réseau plus lente   

La connexion réseau de l’ordinateur que vous utilisez pour créer des sites est probablement plus rapide que les connexions réseau des appareils mobiles de vos utilisateurs.  La limitation de la page vous permet d’obtenir une meilleure idée du temps nécessaire au chargement d’une page sur un appareil mobile.  

1.  Sélectionner la liste déroulante de **limitation** , définie sur **en ligne** par défaut.  
    
    > ##### Figure8  
    > Activation de la limitation  
    > ! [Activation de la limitation] [ImagesTutorialThrottling]  
    
1.  Sélectionnez **3G lente**.  
    
    > ##### Figure9  
    > Sélection du réseau 3G lent  
    > ! [Sélection du réseau 3G lente] [ImagesTutorialSlow3G]  
    
1.  Appuyez de façon prolongée **sur recharger** ![ ][ImageRefreshIcon] et sélectionnez Vider le **cache**.  
    
    > ##### Figure10  
    > Vider le cache et procéder au recharge  
    > ! [Vider le cache et télécharger le matériel] [ImagesTutorialHardReload]  
    
    Lorsque vous révisez les visites, le navigateur fournit généralement certains fichiers du [cache][MDNHTTPCache] , ce qui accélère le chargement de la page.  Le **vidage du cache et du rechargement forcé** force le navigateur à accéder au réseau pour toutes les ressources.  Cette méthode est utile lorsque vous souhaitez voir la façon dont un visiteur commence à se charger de la page.  
    
    > [!NOTE]
    > Le flux **de travail vider le cache et le chargement papier** est uniquement disponible lorsque devtools est ouvert.  

## Capture de captures d’écran   

Les captures d’écran vous permettent de voir l’aspect d’une page au fil du temps pendant son chargement.  

1.  Sélectionnez ![ paramètres ][ImageSettingsIcon] du réseau, puis activez la case à cocher capturer les captures d' **écran** .
1.  Rechargez de nouveau la page par le biais du flux **de travail vider le cache et le chargement papier** .  Pour savoir comment procéder, voir [simuler une connexion plus lente](#simulate-a-slower-network-connection) si vous avez besoin d’un rappel.  
    Le volet capture d’écran fournit des miniatures illustrant la manière dont la page a été recherchée à différents points au cours du processus de chargement.  
    
    > ##### Figure11  
    > Captures d’écran du chargement de la page  
    > ! [Captures d’écran du chargement de la page] [ImagesTutorialAllScreenshots]  

1.  Sélectionnez la première miniature.  DevTools indique l’activité réseau qui se produit à ce moment précis.  
    
    > ##### Figure12  
    > Activité réseau qui se produit pendant la première capture d’écran  
    > ! [Activité réseau qui se produisait pendant la première capture d’écran] [ImagesTutorialFirstScreenshot]  

1.  Cliquez de ![ ][ImageSettingsIcon] nouveau sur paramètres du réseau et désélectionnez la case à cocher capturer les captures d' **écran** pour fermer le volet captures d’écran.
1.  Rechargez la page.  

## Inspecter les détails de la ressource   

Pour plus d’informations à ce sujet, sélectionnez une ressource.  Essayez-le maintenant:  

1.  Sélectionnez `getstarted.html` .  L’onglet **en-têtes** est affiché.  Utilisez cet onglet pour inspecter les en-têtes HTTP.  
    
    > ##### Figure13  
    > Onglet en-têtes  
    > ! [Onglet en-têtes] [ImagesTutorialHeaders]  
    
1.  Sélectionnez l’onglet **Aperçu** .  Un rendu de base du code HTML est affiché.  
    
    > ##### Figure14  
    > Onglet Aperçu  
    > ! [Onglet Aperçu] [ImagesTutorialPreview]  

     Cet onglet est utile lorsqu’une API renvoie un code d’erreur en HTML.  Il est possible que vous puissiez lire le code HTML affiché plus facilement que le code source HTML ou lorsque vous examinez des images.  

1.  Sélectionnez l’onglet **réponse** .  Le code source HTML est affiché.  
    
    > ##### Figure15  
    > Onglet réponse  
    > ! [Onglet réponse] [ImagesTutorialResponse]  
    
    > [!TIP]
    > Lorsqu’un fichier est minified, le fait de sélectionner le bouton format de **mise** ![ en forme ][ImageFormatIcon] en bas de l’onglet **réponse** reformate le contenu du fichier pour faciliter la lecture.  

1.  Sélectionnez l’onglet **minutage** .  Le détail de l’activité réseau de cette ressource est affiché.  
    
    > ##### Figure16  
    > Onglet Minutage  
    > ! [Onglet Minutage] [ImagesTutorialTiming]  

1.  **Close** ![ ][ImageCloseIcon] Pour afficher de nouveau le journal du réseau, sélectionnez Fermer.  
    
    > ##### Figure17  
    > Bouton Fermer  
    > ! [Bouton Fermer] [ImagesTutorialCloseTiming]  

## Effectuer une recherche dans les en-têtes et réponses du réseau   

Le volet de **recherche** vous permet d’effectuer une recherche dans les en-têtes et réponses HTTP de toutes les ressources pour une chaîne ou une expression régulière spécifique.  

Par exemple, supposons que vous vouliez vérifier que vos ressources utilisent des **stratégies de cache**raisonnables.  

<!--TODO: add cache policies section when available  -->

1.  Sélectionnez **Rechercher dans Search** ![ ][ImageSearchIcon] .  Le volet de recherche s’ouvre à gauche du journal du réseau.  
    
    > ##### Figure 18  
    > Le volet de recherche  
    > ! [Volet de recherche] [ImagesTutorialSearch]  

1.  Tapez `Cache-Control` et appuyez sur `Enter` .  Le volet de recherche répertorie toutes les instances `Cache-Control` qu’il recherche dans les en-têtes de ressources ou le contenu.  
    
    > ##### Figure 19  
    > Résultats de la recherche pour  `Cache-Control`  
    > ! [Résultats de recherche pour Cache-Control] [ImagesTutorialResults]  

1.  Sélectionnez un résultat pour afficher la ressource dans laquelle le résultat a été trouvé.  Si vous examinez les détails de la ressource, sélectionnez un résultat pour y accéder directement.  Par exemple, si la requête se trouve dans un en-tête, l’onglet en-têtes s’ouvre.   Si la requête se trouve dans le contenu, l’onglet **réponse** s’ouvre.  
    
    > ##### Figure 20  
    > Résultat de la recherche en surbrillance dans l’onglet en-têtes  
    > ! [Un résultat de recherche en surbrillance dans l’onglet en-têtes] [ImagesTutorialCache]  
    
1.  Fermez le volet de recherche et l’onglet en-têtes.  
    
    > ##### Figure 21  
    > Boutons Fermer  
    > ! [Boutons Fermer] [ImagesTutorialCloseButtons]  
    
## Filtrer les ressources   

DevTools fournit de nombreux flux de travail pour filtrer les ressources qui ne sont pas pertinentes pour la tâche en cours.  

> ##### Figure 22  
> Barre d’outils filtres  
> ! [Barre d’outils filtres] [ImagesTutorialFilters]  

Par défaut, la barre d’outils **filtres** doit être activée.  Si ce n’est pas le cas:  

1.  Sélectionnez **Filter** ![ filtre ][ImageFilterIcon] de filtre pour l’afficher.  

### Filtrer par chaîne, expression régulière ou propriété   

La zone de texte **filtre** prend en charge différents types de filtrage.  

1.  Entrez `png` dans la zone de texte du **filtre** .  Seuls les fichiers qui contiennent le texte `png` sont affichés.  Dans ce cas, les seuls fichiers correspondant au filtre sont les images PNG.  
    
    > ##### Figure 23  
    > Filtre de chaîne  
    > ! [Filtre de chaîne] [ImagesTutorialPNG]  

1.  Entrez `/.*\.[cj]s+$/`.  DevTools filtre les ressources dont le nom ne se termine pas par un `j` ou après `c` suivi de 1 ou plusieurs `s` caractères.  
    
    > ##### Figure 24  
    > Un filtre d’expression régulier  
    > ! [Filtre d’expression régulière] [ImagesTutorialRegEx]  
    
1.  Entrez `-main.css`.  DevTools filtre `main.css` .  Si un autre fichier correspond au modèle, il sera également filtré.  
    
    > ##### Figure 25  
    > Un filtre négatif  
    > ! [Un filtre négatif] [ImagesTutorialNegative]  
    
1.  Entrez `domain:cdn.glitch.com` dans la zone de texte du **filtre** .  DevTools filtre les ressources disposant d’une URL qui ne correspond pas à ce domaine.  
    
    > ##### Figure 26  
    > Filtre de propriétés  
    > ! [Filtre de propriétés] [ImagesTutorialProperty]  

    Pour obtenir la liste complète des propriétés filtrées [, voir filtrer les demandes par propriétés][DevtoolsReferenceProperty] .  
    
    
1.  Effacez la zone de texte du **filtre** d’un texte.  

### Filtrer par type de ressource   

Pour vous concentrer sur un certain type de fichier, tel que les feuilles de style:  

1.  Sélectionnez **CSS**.  Tous les autres types de fichiers sont filtrés.  
    
    > ##### Figure 27  
    > Affichage des fichiers CSS uniquement  
    > ! [Affichage des fichiers CSS uniquement] [ImagesTutorialCSS]  
    
1.  Pour afficher les scripts, vous pouvez également appuyer sur `Control` \ (Windows \) ou `Command` \ (MacOS \), puis sélectionner **js**.  
    
    > ##### Figure 28  
    > Affichage des fichiers CSS et JS uniquement  
    > ! [Affichage des fichiers CSS et JS uniquement] [ImagesTutorialCSSJS]  
    
1.  **Tout** sélectionner pour supprimer les filtres et afficher de nouveau toutes les ressources.  

Pour plus d’autres flux de travail de filtrage, voir [Filtrer les demandes][DevtoolsNetworkReferenceFilter] .  

## Bloquer les demandes   

Quel est l’aspect et le comportement d’une page lorsque certaines ressources de la page ne sont pas disponibles?  Est-ce que l’opération échoue entièrement ou fonctionne-t-elle toujours?  Bloquer les requêtes à Rechercher:  

1.  Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.  
    
    > ##### Figure 29  
    > Menu de commandes  
    > ! [Le menu de commandes] [ImagesTutorialCommandMenu]  
    
1.  Tapez `block` , sélectionnez **afficher le blocage de requête**, puis appuyez sur `Enter` .  
    
    > ##### Figure 30  
    > Afficher le blocage de requête  
    > ! [Afficher une demande de blocage] [ImagesTutorialBlock]  

1.  Sélectionnez **Ajouter** un modèle ajouter un modèle ![ ][ImageAddIcon] .  
1.  Entrez `main.css`.  
    
    > ##### Figure 31  
    > Bloquer `main.css`  
    > ! [Blocage de main. CSS] [ImagesTutorialAddBlock]  
    
1.  Cliquez sur **Ajouter**.  
1.  Rechargez la page.  Comme prévu, le style de la page est légèrement gâché, car la feuille de style principale a été bloquée.  
    
    > [!NOTE]
    > `main.css`Ligne du journal du réseau.  Le texte rouge signifie que la ressource a été bloquée.
    
    > ##### Figure 32  
    > `main.css` a été bloqué  
    > ! [main. CSS a été bloqué] [ImagesTutorialBlockedStyles]  

1.  Désélectionnez la case à cocher **activer le blocage de requête** .  

## Conclusion  

Félicitations, vous avez terminé le didacticiel.  Vous savez maintenant comment utiliser le panneau réseau dans Microsoft Edge DevTools!






Consultez la [référence réseau][DevtoolsNetworkReference] pour découvrir d’autres fonctionnalités devtools liées à l’examen de l’activité du réseau.  

 



<!-- image links -->  

[ImageAddIcon]: /microsoft-edge/devtools-guide-chromium/media/add-icon.msft.png  
[ImageCloseIcon]: /microsoft-edge/devtools-guide-chromium/media/close-icon.msft.png  
[ImageFilterIcon]: /microsoft-edge/devtools-guide-chromium/media/filter-icon.msft.png  
[ImageFormatIcon]: /microsoft-edge/devtools-guide-chromium/media/format-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageScreenshotsIcon]: /microsoft-edge/devtools-guide-chromium/media/screenshots-icon.msft.png  
[ImageSearchIcon]: /microsoft-edge/devtools-guide-chromium/media/search-icon.msft.png  
[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png

[ImagesTutorialDemo]: /microsoft-edge/devtools-guide-chromium/media/network-glitch-inspect-network-activity-demo.msft.png "Figure 1: démonstration"  
<!--[ImagesTutorialWindows]: /microsoft-edge/devtools-guide-chromium/media/network-tutorial/windows.msft.png " old Figure 2: The demo in one window and this tutorial in a different window"  -->  
[ImagesTutorialConsole]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-console.msft.png "figure 2: console"  
[ImagesTutorialDocked]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-console-Bottom.msft.png "figure 3: DevTools ancré en bas de la fenêtre"  
[ImagesTutorialNetwork]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Bottom.msft.png "figure 4: DevTools ancré en bas de la fenêtre"  
[ImagesTutorialLog]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network.msft.png "figure 5: journal réseau"  
[ImagesTutorialRuntime]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-New-Resource.msft.png "figure 6: une nouvelle ressource du journal du réseau"  
[ImagesTutorialDomain]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Edit-Column.msft.png "figure 7: activation de la colonne Domain"  
[ImagesTutorialThrottling]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-throttling.msft.png "figure 8: activation de la limitation"  
[ImagesTutorialSlow3G]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-throttling-Slow-3G.msft.png "figure 9: sélectionner la fonction 3G lente"  
[ImagesTutorialHardReload]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Empty-cache-and-hard-reset.msft.png "figure 10: vider le cache et le recharger"  
[ImagesTutorialAllScreenshots]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-screenshots.msft.png "figure 11: captures d’écran du chargement de la page"  
[ImagesTutorialFirstScreenshot]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-screenshots-First.msft.png "figure 12: activité réseau qui se produit pendant la première capture d’écran"  
[ImagesTutorialHeaders]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Resources-headers.msft.png "figure 13: onglet en-têtes"  
[ImagesTutorialPreview]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Resources-preview.msft.png "figure 14: onglet Aperçu"  
[ImagesTutorialResponse]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Resources-Response.msft.png "figure 15: onglet réponse"  
[ImagesTutorialTiming]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Resources-timing.msft.png "figure 16: onglet Minutage"  
[ImagesTutorialCloseTiming]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Resources-Close-Tabs.msft.png "figure 17: bouton Fermer"  
[ImagesTutorialSearch]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Search-Empty.msft.png "figure 18: volet de recherche"  
[ImagesTutorialResults]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Search-Cache-Control.msft.png "figure 19: résultats de recherche pour Cache-Control"  
[ImagesTutorialCache]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Search-Cache-Control-headers-Response-headers.msft.png "figure 20: un résultat de recherche mis en surbrillance dans l’onglet en-têtes"  
[ImagesTutorialCloseButtons]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Search-Close.msft.png "figure 21: boutons Fermer"  
[ImagesTutorialFilters]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-Empty.msft.png "figure 22: barre d’outils filtres"  
[ImagesTutorialPNG]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-png.msft.png "figure 23: filtre de chaîne"  
[ImagesTutorialRegEx]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-Regex.msft.png "figure 24: filtre d’expression régulière"  
[ImagesTutorialNegative]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-Negative-Statement.msft.png "figure 25: filtre négatif"  
[ImagesTutorialProperty]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-Property-value.msft.png "figure 26: filtre de propriété"  
[ImagesTutorialCSS]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-file-type-CSS.msft.png "figure 27: affichage des fichiers CSS uniquement"  
[ImagesTutorialCSSJS]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-file-type-CSS-js.msft.png "figure 28: affichage des fichiers CSS et JS uniquement"  
[ImagesTutorialCommandMenu]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-CLI-Empty.msft.png "figure 29: menu commande"  
[ImagesTutorialBlock]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-CLI-Block.msft.png "figure 30: afficher le blocage de requête"  
[ImagesTutorialAddBlock]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-CLI-Block-Add-Pattern.msft.png "figure 31: blocage de main. css"  
[ImagesTutorialBlockedStyles]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-CLI-Block-main-CSS.msft.png "figure 32: main. CSS a été bloqué"  

<!-- links -->  


<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Changer la position de Microsoft Edge DevTools (détacher, ancrer en bas, ancrer à gauche)"  
[DevtoolsNetworkReference]: /microsoft-edge/devtools-guide-chromium/network/reference "Référence d’analyse du réseau"
[DevtoolsNetworkReferenceFilter]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests "Demandes de filtre-référence d’analyse du réseau"  
[DevtoolsReferenceHideOverview]: /microsoft-edge/devtools-guide-chromium/network/reference#hide-the-overview-pane "Masquer le volet vue d’ensemble-référence d’analyse du réseau"
[DevtoolsReferenceProperty]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Demandes de filtre par propriétés-référence d’analyse du réseau"
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Ouvrir Microsoft Edge DevTools"  
[DevtoolsSpeedGetStarted]: /microsoft-edge/devtools-guide-chromium/speed/get-started "Optimiser la vitesse de votre site Web avec Microsoft Edge DevTools"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Consulter la démonstration d’activité réseau"  

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
