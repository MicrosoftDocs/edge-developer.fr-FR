---
description: Didacticiel sur les fonctionnalités réseau les plus populaires dans Microsoft Edge DevTools.
title: Inspecter l’activité réseau dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 63a0c8dc1d481ee3fba93146c2e2925bbdd07203
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565042"
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
# <a name="inspect-network-activity-in-microsoft-edge-devtools"></a>Inspecter l’activité réseau dans Microsoft Edge DevTools  

Il s’agit d’un didacticiel pratique de certaines des fonctionnalités de DevTools les plus couramment utilisées liées à l’inspection de l’activité réseau d’une page.  

Si vous souhaitez parcourir les fonctionnalités, accédez à [Référence réseau.][DevtoolsNetworkReference]  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## <a name="when-to-use-the-network-panel"></a>Quand utiliser le panneau réseau  

En règle générale, utilisez le panneau Réseau lorsque vous devez vous assurer que les ressources sont téléchargées ou téléchargées comme prévu.  Les cas d’utilisation les plus courants pour le panneau réseau sont :  

*   S’assurer que les ressources sont réellement téléchargées ou téléchargées.  
*   Inspection des propriétés d’une ressource individuelle, telles que les en-têtes HTTP, le contenu, la taille, etc.  
    
Si vous recherchez des moyens d’améliorer les performances de chargement de page, ne **commencez** pas par **l’outil** Réseau.  Il existe de nombreux types de problèmes de performances de charge qui ne sont pas liés à l’activité réseau.  Commencez par le panneau Audits, car il vous propose des suggestions ciblées sur l’amélioration de votre page.  Accédez à [Optimiser la vitesse du site web.][DevtoolsSpeedGetStarted]  

## <a name="open-the-network-panel"></a>Ouvrir le panneau réseau  

Pour obtenir le meilleur de ce didacticiel, ouvrez la démonstration et testez les fonctionnalités sur la page de démonstration.  

1.  Ouvrez [la démonstration Prise en main.][GlitchNetworkGetStarted]  
    
    :::image type="complex" source="../media/network-glitch-inspect-network-activity-demo.msft.png" alt-text="Démonstration" lightbox="../media/network-glitch-inspect-network-activity-demo.msft.png":::
       Démonstration  
    :::image-end:::  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    :::image type="complex" source="../media/network-tutorial/windows.msft.png" alt-text="The demo in one window and this tutorial in a different window" lightbox="../media/network-tutorial/windows.msft.png":::
       The demo in one window and this tutorial in a different window  
    :::image-end:::  
    -->
    
1.  Pour [ouvrir DevTools,][DevToolsOpen]sélectionnez `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).  **L’outil Console** s’ouvre.  
    
    :::image type="complex" source="../media/network-glitch-console.msft.png" alt-text="The Console" lightbox="../media/network-glitch-console.msft.png":::
       Console ****  
    :::image-end:::  
    
    Vous pouvez préférer [ancrer DevTools][DevToolsCustomizePlacement]en bas de votre fenêtre.  
    
    :::image type="complex" source="../media/network-glitch-console-bottom.msft.png" alt-text="DevTools docked to the bottom of the window" lightbox="../media/network-glitch-console-bottom.msft.png":::
       DevTools docked to the bottom of the window  
    :::image-end:::  
    
1.  Ouvrez **l’outil** Réseau.  
    
    :::image type="complex" source="../media/network-glitch-network-bottom.msft.png" alt-text="Outil console dans devTools docked to the bottom of the window" lightbox="../media/network-glitch-network-bottom.msft.png":::
       **Outil** console dans devTools docked to the bottom of the window  
    :::image-end:::  
    
Pour l’instant, **l’outil** Réseau est vide.  DevTools enregistre uniquement l’activité réseau après l’avoir ouverte et aucune activité réseau ne s’est produite depuis que vous avez ouvert DevTools.  

## <a name="log-network-activity"></a>Journal de l’activité réseau  

Pour afficher l’activité réseau qu’une page provoque :  

1.  Actualisez la page web.  Le panneau Réseau enregistre toute l’activité réseau dans le **journal réseau.**  
    
    :::image type="complex" source="../media/network-glitch-network.msft.png" alt-text="Journal réseau" lightbox="../media/network-glitch-network.msft.png":::
       Journal **réseau**  
    :::image-end:::  
    
    Chaque ligne du journal **réseau représente** une ressource.  Par défaut, les ressources sont répertoriées dans l’ordre chronologique.  La ressource supérieure est généralement le document HTML principal.  La ressource inférieure est la dernière ressource demandée.  
    
    Chaque colonne représente des informations sur une ressource.  Dans la figure précédente, les colonnes par défaut sont affichées.  

    *   **État**.  Code d’état HTTP pour la réponse.  
    *   **Type**.  Type de ressource.  
    *   **Initiateur**.  Cause de la demande de ressource.  La mise en place d’un lien dans la colonne Initiateur vous permet d’obtenir le code source à l’origine de la demande.  
    *   **Heure**.  Durée de la demande.  
    *   **Cascade**.  Représentation graphique des différentes étapes de la demande.  Pour afficher une répartition, pointez sur une cascade.  
    
    > [!NOTE]
    > Le graphique au-dessus du journal réseau est appelé Vue d’ensemble.  Vous n’utiliserez pas le graphique Vue d’ensemble dans ce didacticiel, vous pouvez donc le masquer.  Accédez à [Masquer le volet Vue d’ensemble.][DevtoolsReferenceHideOverview]
    
1.  Après avoir ouvert DevTools, il enregistre l’activité réseau dans le journal réseau.  
    Pour le montrer, regardez d’abord le bas du journal réseau et notez la dernière activité. ****  
1.  Sélectionnez maintenant le **bouton Obtenir les** données dans la démonstration.  
1.  Regardez de nouveau le bas du **journal** réseau.  Une nouvelle ressource nommée `getstarted.json` s’affiche.  Pour que la page web demande le fichier, choisissez le **bouton Obtenir des** données.  
    
    :::image type="complex" source="../media/network-glitch-network-new-resource.msft.png" alt-text="Une nouvelle ressource dans le journal réseau" lightbox="../media/network-glitch-network-new-resource.msft.png":::
       Une nouvelle ressource dans le **journal réseau**  
    :::image-end:::  
    
## <a name="show-more-information"></a>Afficher plus d’informations  

Les colonnes du journal réseau sont configurables.  Vous pouvez masquer les colonnes que vous n’utilisez pas.  
Il existe également de nombreuses colonnes qui sont masquées par défaut et qui peuvent vous être utiles.  

1.  Pointez sur l’en-tête de la table Journal réseau, ouvrez le menu contextuel \(clic droit\), puis choisissez **Domaine**.  Le domaine de chaque ressource est maintenant affiché.  
    
    :::image type="complex" source="../media/network-glitch-network-edit-column.msft.png" alt-text="Activer la colonne Domaine" lightbox="../media/network-glitch-network-edit-column.msft.png":::
       Activer la colonne Domaine  
    :::image-end:::  
    
    > [!TIP]
    > Pour passer en revue l’URL complète d’une ressource, pointez sur la cellule dans la **colonne** Nom.  
    
## <a name="simulate-a-slower-network-connection"></a>Simuler une connexion réseau plus lente  

La connexion réseau de l’ordinateur que vous utilisez pour créer des sites est probablement plus rapide que les connexions réseau des appareils mobiles de vos utilisateurs.  En limitation de la page, vous avez une meilleure idée du temps de chargement d’une page sur un appareil mobile.  

1.  Choose the **Throttling** dropdown, which is set to **Online** by default.  
    
    :::image type="complex" source="../media/network-glitch-network-throttling.msft.png" alt-text="Activer la limitation" lightbox="../media/network-glitch-network-throttling.msft.png":::
       Activer la limitation  
    :::image-end:::  
    
1.  Choose **Slow 3G**.  
    
    :::image type="complex" source="../media/network-glitch-network-throttling-slow-3g.msft.png" alt-text="Choose Slow 3G" lightbox="../media/network-glitch-network-throttling-slow-3g.msft.png":::
       Choose Slow 3G  
    :::image-end:::  
    
1.  Appuyez **longuement sur Recharger** \( Rechargez \), puis choisissez ![ Cache vide et ](../media/refresh-icon.msft.png) **Rechargement dur.**  
    
    :::image type="complex" source="../media/network-glitch-empty-cache-and-hard-reset.msft.png" alt-text="Cache vide et rechargement dur" lightbox="../media/network-glitch-empty-cache-and-hard-reset.msft.png":::
       **Cache vide et rechargement dur**  
    :::image-end:::  
    
    Lors des visites répétées, le navigateur sert généralement certains fichiers à partir du [cache,][MDNHTTPCache]ce qui accélère le chargement de la page.  **Le cache vide et le rechargement dur** forcent le navigateur à se rendre sur le réseau pour toutes les ressources.  Utilisez-le pour afficher la façon dont un premier visiteur fait l’expérience d’un chargement de page.  
    
    > [!NOTE]
    > Le **flux de travail Cache vide et Rechargement** dur n’est disponible que lorsque DevTools est ouvert.  
    
## <a name="capture-screenshots"></a>Capture d’écran  

Les captures d’écran affichent l’apparence d’une page web au fil du temps pendant son chargement.  

1.  Choisissez \( ![ Paramètres réseau \) et ](../media/settings-icon.msft.png) cochez la case Capture **d’écran.**
1.  Actualisez la page à l’aide **du cache vide et du flux de travail de rechargement** dur.  Si vous [avez besoin](#simulate-a-slower-network-connection) d’un rappel sur la façon de le faire, accédez à Simuler une connexion plus lente.  
    Le panneau Captures d’écran fournit des miniatures de l’aperçu de la page à différents points pendant le processus de chargement.  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots.msft.png" alt-text="Captures d’écran du chargement de la page" lightbox="../media/network-glitch-network-screenshots.msft.png":::
       Captures d’écran du chargement de la page  
    :::image-end:::  
    
1.  Choisissez la première miniature.  DevTools vous indique l’activité réseau qui se produisait à ce moment-là.  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots-first.msft.png" alt-text="Activité réseau qui s’est produit lors de la première capture d’écran" lightbox="../media/network-glitch-network-screenshots-first.msft.png":::
       Activité réseau qui s’est produit lors de la première capture d’écran  
    :::image-end:::  
    
1.  Sélectionnez de nouveau \( Paramètres réseau \) et cochez la case Capture d’écran pour fermer le ![ ](../media/settings-icon.msft.png) volet Captures d’écran. ****
1.  Actualisez la page.  
    
## <a name="inspect-the-details-of-the-resource"></a>Inspecter les détails de la ressource  

Choisissez une ressource pour en savoir plus à son sujet.  Essayez maintenant :  

1.  Choose `getstarted.html` .  Le **panneau En-têtes** s’affiche.  Utilisez ce panneau pour inspecter les en-têtes HTTP.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-headers.msft.png" alt-text="Panneau En-têtes" lightbox="../media/network-glitch-network-resources-headers.msft.png":::
       Panneau **En-têtes**  
    :::image-end:::  
    
1.  Choisissez le **panneau d’aperçu.**  Un rendu de base du code HTML est affiché.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-preview.msft.png" alt-text="Panneau d’aperçu" lightbox="../media/network-glitch-network-resources-preview.msft.png":::
       Panneau **d’aperçu**  
    :::image-end:::  
    
    Le panneau est utile lorsqu’une API renvoie un code d’erreur au format HTML.  Il peut être plus facile de lire le code HTML rendu que le code source HTML, ou lorsque vous examinez des images.  

1.  Sélectionnez **le panneau de** réponse.  Le code source HTML est affiché.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-response.msft.png" alt-text="Panneau de réponse" lightbox="../media/network-glitch-network-resources-response.msft.png":::
       Panneau **de** réponse  
    :::image-end:::  
    
    > [!TIP]
    > Lorsqu’un fichier est minifié, sélectionnez le bouton **Format** \( Format \) en bas du panneau De réponse pour re-mettre en forme le contenu du fichier pour une ![ ](../media/format-icon.msft.png) **** lisibilité.  
    
1.  Sélectionnez **le panneau De minutage.**  Une répartition de l’activité réseau de la ressource s’affiche.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-timing.msft.png" alt-text="Panneau De minutage" lightbox="../media/network-glitch-network-resources-timing.msft.png":::
       Panneau **De minutage**  
    :::image-end:::  
    
1.  Choisissez **Fermer** \( Fermer \) pour afficher à nouveau ![ le journal ](../media/close-icon.msft.png) réseau.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-close-tabs.msft.png" alt-text="Bouton Fermer" lightbox="../media/network-glitch-network-resources-close-tabs.msft.png":::
       Bouton **** Fermer  
    :::image-end:::  
    
## <a name="search-network-headers-and-responses"></a>En-têtes et réponses du réseau de recherche  

Utilisez le **volet de** recherche lorsque vous devez rechercher dans les en-têtes HTTP et les réponses de toutes les ressources une chaîne ou une expression régulière.  

Par exemple, supposons que vous vouliez vérifier que vos ressources utilisent des stratégies de **cache raisonnables.**  

<!--TODO: add cache policies section when available  -->

1.  Choose **Search** \( ![ Search ](../media/search-icon.msft.png) \).  Le volet Recherche s’ouvre à gauche du journal réseau.  
    
    :::image type="complex" source="../media/network-glitch-network-search-empty.msft.png" alt-text="Volet de recherche" lightbox="../media/network-glitch-network-search-empty.msft.png":::
       Volet **** de recherche  
    :::image-end:::  
    
1.  Tapez `Cache-Control` et sélectionnez `Enter` .  Le volet de recherche répertorie toutes les instances de ce qu’il trouve dans les en-têtes `Cache-Control` ou le contenu des ressources.  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control.msft.png" alt-text="Résultats de la recherche pour Cache-Control" lightbox="../media/network-glitch-network-search-cache-control.msft.png":::
       Résultats de la recherche pour  `Cache-Control`  
    :::image-end:::  
    
1.  Choisissez un résultat pour afficher la ressource dans laquelle le résultat a été trouvé.  Si vous recherchez les détails de la ressource, sélectionnez un résultat pour y aller directement.  Par exemple, si la requête a été trouvée dans un en-tête, le panneau **En-têtes** s’ouvre.   Si la requête a été trouvée dans le contenu, le panneau **Réponse** s’ouvre.  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png" alt-text="Résultat de recherche mis en évidence dans le panneau En-têtes" lightbox="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png":::
       Résultat de recherche mis en évidence dans le panneau **En-têtes**  
    :::image-end:::  
    
1.  Fermez le volet Recherche et le volet **En-têtes.**  
    
    :::image type="complex" source="../media/network-glitch-network-search-close.msft.png" alt-text="Boutons Fermer" lightbox="../media/network-glitch-network-search-close.msft.png":::
       Boutons **Fermer**  
    :::image-end:::  
    
## <a name="filter-resources"></a>Filtrer les ressources  

DevTools fournit de nombreux flux de travail pour filtrer les ressources qui ne sont pas pertinentes pour la tâche en cours.  

:::image type="complex" source="../media/network-glitch-network-filter-empty.msft.png" alt-text="Barre d’outils Filtres" lightbox="../media/network-glitch-network-filter-empty.msft.png":::
   Barre **d’outils Filtres**  
:::image-end:::  

La **barre d’outils** Filtres doit être allumée par défaut.  Si ce n’est pas le cas :  

1.  Choisissez **Filtre** \( ![ Filtre ](../media/filter-icon.msft.png) \) pour l’afficher.  
    
### <a name="filter-by-string-regular-expression-or-property"></a>Filtrer par chaîne, expression régulière ou propriété  

La **zone de** texte Filtre prend en charge différents types de filtrage.  

1.  Tapez `png` dans la zone **de** texte Filtrer.  Seuls les fichiers contenant le texte `png` sont affichés.  Dans ce cas, les seuls fichiers qui correspondent au filtre sont les images PNG.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-png.msft.png" alt-text="Un filtre de chaîne" lightbox="../media/network-glitch-network-filter-png.msft.png":::
       Un filtre de chaîne  
    :::image-end:::  
    
1.  Tapez `/.*\.[cj]s+$/`.  DevTools filtre toutes les ressources dont le nom de fichier ne se termine pas par un ou plusieurs `j` `c` `s` caractères.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-regex.msft.png" alt-text="Filtre d’expression régulière" lightbox="../media/network-glitch-network-filter-regex.msft.png":::
       Filtre d’expression régulière  
    :::image-end:::  
    
1.  Tapez `-main.css`.  DevTools filtre les `main.css` sorties.  Si un fichier correspond au modèle, son sein est également filtré.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-negative-statement.msft.png" alt-text="Un filtre négatif" lightbox="../media/network-glitch-network-filter-negative-statement.msft.png":::
       Un filtre négatif  
    :::image-end:::  
    
1.  Tapez `domain:cdn.glitch.com` dans la zone **de** texte Filtrer.  DevTools filtre toutes les ressources avec une URL qui ne correspond pas à ce domaine.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-property-value.msft.png" alt-text="Un filtre de propriété" lightbox="../media/network-glitch-network-filter-property-value.msft.png":::
       Un filtre de propriété  
    :::image-end:::  
    
    Pour obtenir la liste complète des propriétés filtrables, accédez à [Filtrer les demandes par propriétés.][DevtoolsReferenceProperty]  
    
1.  Effacer la **zone de** texte Filtrer de n’importe quel texte.  
    
### <a name="filter-by-resource-type"></a>Filtrer par type de ressource  

Pour vous concentrer sur un certain type de fichier, comme les feuilles de style :  

1.  Choisissez **CSS**.  Tous les autres types de fichiers sont filtrés.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css.msft.png" alt-text="Afficher uniquement les fichiers CSS" lightbox="../media/network-glitch-network-filter-file-type-css.msft.png":::
       Afficher uniquement les fichiers CSS  
    :::image-end:::  
    
1.  Pour afficher également des scripts, sélectionnez et maintenez `Control` \(Windows, Linux\) ou `Command` \(macOS\), puis choisissez **JS**.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css-js.msft.png" alt-text="Afficher uniquement les fichiers CSS et JS" lightbox="../media/network-glitch-network-filter-file-type-css-js.msft.png":::
       Afficher uniquement les fichiers CSS et JS  
    :::image-end:::  
    
1.  Pour supprimer les filtres et afficher à nouveau toutes les ressources, choisissez **Tout**.  
    
Pour les autres flux de travail de filtrage, accédez à [Filtrer les demandes.][DevtoolsNetworkReferenceFilter]  

## <a name="block-requests"></a>Bloquer les demandes  

Comment se comporte une page lorsque certaines ressources de page ne sont pas disponibles ?  Échoue-t-elle complètement ou est-elle encore quelque peu fonctionnelle ?  Bloquer les demandes pour savoir :  

1.  Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) pour ouvrir le **menu Commande.**  
    
    :::image type="complex" source="../media/network-glitch-network-cli-empty.msft.png" alt-text="Menu Commande" lightbox="../media/network-glitch-network-cli-empty.msft.png":::
       Menu **Commande**  
    :::image-end:::  
    
1.  Tapez `block` , choisissez Afficher le blocage **des**demandes, puis sélectionnez `Enter` .  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block.msft.png" alt-text="Afficher le blocage des demandes" lightbox="../media/network-glitch-network-cli-block.msft.png":::
       **Afficher le blocage des demandes**  
    :::image-end:::  
    
1.  Choose **Add Pattern** \( Add Pattern ![ ](../media/add-icon.msft.png) \).  
1.  Tapez `main.css`.  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-add-pattern.msft.png" alt-text="Blocage de main.css" lightbox="../media/network-glitch-network-cli-block-add-pattern.msft.png":::
       Blocage `main.css`  
    :::image-end:::  
    
1.  Choose **Add**.  
1.  Actualisez la page.  Comme prévu, le style de la page est légèrement décoché car la feuille de style principale a été bloquée.  
    
    > [!NOTE]
    > Ligne `main.css` du journal réseau.  Le texte rouge signifie que la ressource a été bloquée.
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-main-css.msft.png" alt-text="main.css a été bloqué" lightbox="../media/network-glitch-network-cli-block-main-css.msft.png":::
       `main.css` a été bloqué  
    :::image-end:::  
    
1.  Désélectionner la **case à cocher Activer le blocage des** demandes.  

## <a name="conclusion"></a>Conclusion  

Félicitations, vous avez terminé le didacticiel.  Vous savez maintenant comment **** utiliser l’outil Réseau dans le Microsoft Edge DevTools !

Accédez à la [Référence réseau][DevtoolsNetworkReference] pour découvrir d’autres fonctionnalités DevTools liées à l’inspection de l’activité réseau.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: ../customize/placement.md "Modifier Microsoft Edge placement de DevTools | Documents Microsoft"  
[DevtoolsNetworkReference]: ./reference.md "Référence de l’analyse réseau | Documents Microsoft"
[DevtoolsNetworkReferenceFilter]: ./reference.md#filter-requests "Demandes de filtre : référence de l’analyse réseau | Documents Microsoft"  
[DevtoolsReferenceHideOverview]: ./reference.md#hide-the-overview-pane "Masquer le volet Vue d’ensemble - Référence de l’analyse réseau | Documents Microsoft"
[DevtoolsReferenceProperty]: ./reference.md#filter-requests-by-properties "Filtrer les demandes par propriétés : référence de l’analyse réseau | Documents Microsoft"
[DevToolsOpen]: ../open/index.md "Ouvrez Microsoft Edge devTools | Documents Microsoft"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Optimiser la vitesse du site web avec Microsoft Edge devTools | Documents Microsoft"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Inspecter la démonstration de l’activité | Glitch"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Mise en cache HTTP | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/network/index) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
