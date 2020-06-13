---
title: Référence d’analyse du réseau
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: c9d205fb2cc478e9c3f20458f461f004035e85e8
ms.sourcegitcommit: a34858dd3260967ba9699842fa839c7a94775fe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/12/2020
ms.locfileid: "10710398"
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

# Référence d’analyse du réseau  

Découvrez de nouvelles façons d’analyser le chargement de votre page dans cette référence complète des fonctionnalités d’analyse du réseau Microsoft Edge DevTools.  

<!--
> [!NOTE]
> This reference is based on Microsoft Edge 58.  If you use another version of Microsoft Edge, the UI, and features of DevTools may be different.  Check `edge://help` to see what version of Microsoft Edge you are running.  
-->

## Enregistrer les requêtes réseau  

Par défaut, DevTools enregistre toutes les requêtes réseau dans le panneau réseau, tant que DevTools est ouvert.  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-panel.msft.png":::
   Figure 1: panneau **réseau**  
:::image-end:::  

### Arrêter l’enregistrement des requêtes réseau  

Pour arrêter l’enregistrement de demandes, procédez comme suit.  

1.  Pour arrêter l' **enregistrement du journal du réseau** , cliquez sur arrêter l' ![ enregistrement réseau ][ImageRecordOnIcon] dans le panneau **réseau** .  Il devient gris pour indiquer que DevTools n’enregistre plus les demandes.  
1.  Appuyez sur `Control` + `E` \ (Windows \) ou `Command` + `E` \ (MacOS \) lorsque le panneau **réseau** a le focus.  

### Supprimer des demandes  

Sélectionnez **Effacer** ![ ][ImageClearIcon] le panneau réseau pour effacer toutes les demandes de la table demandes.  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Bouton Effacer" lightbox="../media/network-network-clear-button.msft.png":::
   Figure 2: bouton **Effacer**  
:::image-end:::  

### Enregistrer les demandes lors du chargement de la page  

Pour enregistrer les demandes lors du chargement de la page, activez la case à cocher **conservation du journal** dans le panneau réseau.  DevTools enregistre toutes les demandes jusqu’à ce que vous désactiviez le **Journal de conservation**.  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Case à cocher conserver le journal" lightbox="../media/network-network-preserve-log.msft.png":::
   Figure 3: case à cocher **conserver le journal**  
:::image-end:::  

### Capture de captures d’écran pendant le chargement de la page  

Capture des captures d’écran pour analyser ce que les utilisateurs voient lorsqu’ils attendent que votre page se charge.  

Pour activer les captures d’écran, sélectionnez **paramètres du réseau** , puis cochez la case **capturer les captures d’écran** dans le panneau **réseau** .  

Actualisez la page lorsque le panneau **réseau** a le focus pour capturer les captures d’écran.  

Après avoir capturé une capture d’écran, vous interagissez comme suit.  

*   Placez le pointeur de la souris sur une capture d’écran pour afficher le point d’acquisition de cette capture d’écran.  Une ligne jaune apparaît dans le volet **vue d’ensemble** .  
*   Sélectionnez la miniature d’un écran pour filtrer toutes les demandes qui se sont produites après la capture de la capture d’écran.  
*   Double-cliquez sur une miniature pour y effectuer un zoom.  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Survol d’une capture d’écran" lightbox="../media/network-network-screenshot-hover.msft.png":::
   Figure 4: survol d’une capture d’écran  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and select **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Selecting Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Old Figure 5:  Selecting Replay XHR  
:::image-end:::  
-->  

## Changer le comportement de chargement  

### Émuler un visiteur pour la première fois en désactivant le cache du navigateur  

Pour émuler la façon dont un utilisateur a expériences de votre site pour la première fois, activez la case à cocher **désactiver le cache** .  DevTools désactive le cache du navigateur.  Cela a pour effet d’émuler de façon plus précise une première utilisation de l’utilisateur, car les requêtes sont servies dans le cache du navigateur sur les visites répétées.  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Case à cocher Désactiver le cache" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   Figure 5: case à cocher **désactiver le cache**  
:::image-end:::  

#### Désactiver le cache du navigateur dans le tiroir du réseau  

Si vous voulez désactiver le cache lorsque vous travaillez dans d’autres panneaux DevTools, utilisez le tiroir de l’état du réseau.  

1.  Ouvrez le tiroir de **conditions du réseau** .  
1.  Cochez ou décochez la case **désactiver le cache** .  

<!--todo: add network condition section when available -->  

### Vider manuellement le cache du navigateur  

Pour vider manuellement le cache du navigateur à tout moment, ouvrez le menu contextuel (cliquez avec le bouton droit sur \) n’importe où dans la table demandes et sélectionnez **Vider le cache du navigateur**.  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Sélection de l’option vider le cache du navigateur" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   Figure 6: sélectionner **Vider le cache du navigateur**  
:::image-end:::  

### Émuler hors connexion  

Une nouvelle classe d’applications Web, appelées [applications Web progressives][DevtoolsProgressiveWebApps], fonctionne en mode hors connexion avec l’aide des **travailleurs de service**.  Vous constaterez peut-être qu’il est utile de simuler rapidement un appareil dépourvu de connexion aux données lors de la création de ce type d’application.  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

Sélectionnez le menu déroulant **en ligne** , Rechercher sous **présélections**, puis sélectionnez **hors ligne** pour simuler une interface réseau entièrement hors connexion.  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Menu déroulant hors connexion" lightbox="../media/network-network-offline-dropdown.msft.png":::
   Figure 7: menu déroulant **hors connexion**  
:::image-end:::  

### Émuler une connexion réseau lente  

Émulez des vitesses de connexion 3G, Fast 3G et autres vitesses de connexion dans le menu déroulant **en ligne** .  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Menu déroulant limitation" lightbox="../media/network-network-throttling-menu.msft.png":::
   Figure 8: menu déroulant **limitation**  
:::image-end:::  

Vous pouvez faire votre choix parmi une série de présélections, par exemple, lente 3G ou Fast 3G.  Vous pouvez également ajouter vos propres Présélections personnalisées en ouvrant le menu limitation et **Custom**en sélectionnant  >  **Ajouter**personnalisé.  

DevTools affiche une icône d’avertissement en regard de l’onglet **réseau** pour vous rappeler que la limitation est activée.  

#### Émuler une connexion réseau lente à partir du tiroir du réseau  

Si vous souhaitez limiter la connexion réseau lorsque vous travaillez dans d’autres panneaux DevTools, utilisez le tiroir de l’état du réseau.  

1.  Ouvrez le tiroir de **conditions du réseau** .  
1.  Sélectionnez le débit de connexion souhaité dans le menu **limitation** .  

<!--todo: add network condition section when available -->  

### Effacement manuel des cookies du navigateur  

Pour effacer manuellement les cookies du navigateur à tout moment, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \) n’importe où dans la table demandes, puis sélectionnez **effacer les cookies du navigateur**.  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Sélection effacer les cookies du navigateur" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   Figure 9: sélectionnez **effacer les cookies du navigateur**  
:::image-end:::  

### Remplacer l’agent utilisateur  

Pour remplacer manuellement l’agent utilisateur, procédez comme suit:  

1.  Ouvrez le tiroir de **conditions du réseau** .  
1.  Décochez l' **option sélectionner automatiquement**.  
1.  Choisissez une option de l’agent utilisateur dans le menu ou entrez-en un dans la zone de texte.  

<!--todo: add network condition section when available -->  

## Demandes de filtre  

### Filtrer les demandes par propriétés  

Utilisez la zone de texte **filtre** pour filtrer les demandes par propriétés, telles que le domaine ou la taille de la requête.  

Si vous ne voyez pas la zone de texte, le volet filtres est probablement masqué.  
Voir [masquer le volet filtres](#hide-the-filters-pane).  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Zone de texte filtre" lightbox="../media/network-network-filters-textbox.msft.png":::
   Figure 10: zone de texte de **filtre**  
:::image-end:::  

Vous pouvez utiliser plusieurs propriétés simultanément en séparant chaque propriété d’un espace.  Par exemple, `mime-type:image/png larger-than:1K` affiche tous les png dont la taille est supérieure à 1 Ko.  Ces filtres multi-propriété sont équivalents aux `AND` opérations.  `OR` les opérations ne sont actuellement pas prises en charge.  

Liste complète des propriétés prises en charge.  

| Propriété | Détails |  
|:--- | :--- |  
| `domain` | Afficher uniquement les ressources du domaine spécifié.  Vous pouvez utiliser un caractère générique \ ( `*` \) pour inclure plusieurs domaines.  Par exemple, `*.com` affiche les ressources de tous les noms de domaine se terminant par `.com` .  DevTools remplit le menu déroulant de saisie semi-automatique avec tous les domaines qu’il a rencontré. |  
| `has-response-header` | Afficher les ressources qui contiennent l’en-tête de réponse HTTP spécifié.  DevTools remplit la liste déroulante de saisie semi-automatique avec tous les en-têtes de réponse qu’il a rencontré. |  
| `is` | Utiliser `is:running` pour rechercher des `WebSocket` ressources. |  
| `larger-than` | Afficher les ressources dont la taille est supérieure à la taille spécifiée, en octets.  La définition d’une valeur est égale à la valeur `1000` `1k` . |  
| `method` | Afficher les ressources récupérées sur un type de méthode HTTP spécifié.  DevTools remplit la liste déroulante avec toutes les méthodes HTTP qu’il a rencontrées. |  
| `mime-type` | Afficher les ressources d’un type MIME spécifié.  DevTools remplit la liste déroulante avec tous les types MIME qu’il a rencontré. |  
| `mixed-content` | Affichez toutes les ressources de contenu mixte \ ( `mixed-content:all` \) ou uniquement celles actuellement affichées \ ( `mixed-content:displayed` \). |  
| `scheme` | Afficher les ressources récupérées sur une connexion HTTP \ ( `scheme:http` \) ou protégé https \ ( `scheme:https` \). |  
| `set-cookie-domain` | Afficher les ressources qui ont un `Set-Cookie` en-tête avec un `Domain` attribut qui correspond à la valeur spécifiée.  DevTools remplit la saisie semi-automatique avec tous les domaines de cookie qu’il a rencontré. |  
| `set-cookie-name` | Afficher les ressources possédant un `Set-Cookie` en-tête dont le nom correspond à la valeur spécifiée.  DevTools remplit la saisie semi-automatique avec tous les noms de cookie qu’il a rencontré. |  
| `set-cookie-value` | Afficher les ressources dont l' `Set-Cookie` en-tête comporte une valeur qui correspond à la valeur spécifiée.  DevTools remplit la saisie semi-automatique avec toutes les valeurs de cookie qu’il a rencontrées. |  
| `status-code` | Afficher uniquement les ressources pour lesquelles le code d’état HTTP correspond au code spécifié.  DevTools remplit le menu déroulant de saisie semi-automatique avec tous les codes d’État détectés. |  

### Filtrer les demandes par type  

Pour filtrer les demandes par type de requête, sélectionnez les boutons **XHR**, **js**, **CSS**, **img**, **multimédia**, **police**, **doc**, **WS** \ (WebSocket \), **manifeste**ou **autre** (n’importe quel autre type non répertorié ici \) sur le panneau réseau.  

Si vous ne voyez pas ces boutons, le volet filtres est probablement masqué.  
Voir [masquer le volet filtres](#hide-the-filters-pane).  

Pour activer plusieurs filtres de type simultanément, appuyez sur `Control` \ (Windows \) ou `Command` \ (MacOS \), puis sélectionnez.  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Utiliser les filtres de type pour afficher les ressources JS, CSS et document" lightbox="../media/network-network-type-filters.msft.png":::
   Figure 11: utilisation des filtres de type pour afficher les ressources JS, CSS et document  
:::image-end:::  

### Filtrer les demandes par heure  

Sélectionnez et faites glisser vers la gauche ou la droite dans le volet vue d’ensemble pour afficher uniquement les demandes actives au cours de cette période.  Le filtre est inclusive.  Toutes les demandes qui ont été actives pendant la durée en surbrillance apparaissent.  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Filtrage des requêtes inactives depuis 300M" lightbox="../media/network-network-overview-filter.msft.png":::
   Figure 12: filtrage des requêtes inactives depuis 300 m  
:::image-end:::  

### Masquer les URL de données  

Les [URL de données][MDNHTTPDataURIs] sont des petits fichiers incorporés dans d’autres documents.  Toute demande figurant dans la table demandes qui commence par `data:` est une URL de données.  

Cochez la case **Masquer les URL de données** pour masquer les demandes.  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Case à cocher Masquer les URL de données" lightbox="../media/network-network-hide-data-urls.msft.png":::
   Figure 13: cases à cocher **Masquer les URL de données**  
:::image-end:::  

## Demandes de tri  

Par défaut, les requêtes dans la table demandes sont triées par heure de début, mais vous pouvez trier le tableau en utilisant d’autres critères.  

### Trier par colonne  

Sélectionnez l’en-tête de n’importe quelle colonne dans les requêtes pour trier les demandes en se sur cette colonne.  

### Trier par phase d’activité  

Pour modifier la façon dont les demandes de tri d’une cascade sont triées, pointez sur l’en-tête de la table demandes, ouvrez le menu **contextuel, puis**sélectionnez l’une des options suivantes.  

*   **Heure de début**.  La première requête lancée est en haut.  
*   **Temps de réponse**.  La première demande qui a démarré le téléchargement est en haut.  
*   **Heure de fin**.  La première demande qui est terminée est en haut.  
*   **Durée totale**.  La requête avec la configuration de connexion la plus courte et la demande/réponse se trouvent dans la partie supérieure.  
*   **Latence**.  La requête qui a attendu le plus court délai d’une réponse est située en haut.  

Ces descriptions présupposent que chaque option respective est classée du plus court au plus long.  La sélection de l’en-tête de la colonne en **cascade** inverse l’ordre.  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Tri des cascades par durée totale" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   Figure 14: trier les cascades en fonction de la durée totale \ (la partie plus claire de chaque barre représente le temps passé en attente et la partie plus foncée est le temps de télécharger les octets \)  
:::image-end:::  

## Analyser les requêtes  

Tant que DevTools est ouvert, il enregistre toutes les demandes dans le panneau réseau.  
Utilisez le volet réseau pour analyser les requêtes.  

### Afficher un journal des demandes  

Utilisez le tableau demandes pour afficher un journal de toutes les demandes effectuées lorsque DevTools est ouvert.  La sélection ou le passage de demandes au-dessus révèle des informations supplémentaires sur chaque élément.  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Table demandes" lightbox="../media/network-network-requests-table.msft.png":::
   Figure 15: table demandes  
:::image-end:::  

La table demandes affiche les colonnes suivantes par défaut.  

*   **Nom**.  Nom de fichier ou un identificateur pour la ressource.  
*   **Status**.  Code d’état HTTP.  
*   **Type**.  Type MIME de la ressource demandée.  
*   **Initiator**.  Les requêtes d’ouverture des objets ou processus suivants sont les suivantes:  
    *   **Analyseur**.  Analyseur HTML pour Microsoft Edge.  
    *   **Redirect**.  Une redirection HTTP.  
    *   **Script**.  Fonction JavaScript.  
    *   **Autre**.  Un autre processus ou action, comme la navigation vers une page par le biais d’un lien ou la saisie d’une URL dans la barre d’adresses.  
*   **Taille**.  Taille combinée des en-têtes de réponse et du corps de la réponse, tel qu’il est délivré par le serveur.  
*   **Temps**.  Durée totale, entre le début de la demande et la réception de l’octet final dans la réponse.  
*   En [**cascade**](#view-the-timing-of-requests-in-relation-to-one-another).  Répartition visuelle de l’activité pour chaque demande.  

#### Ajouter ou supprimer des colonnes  

Placez le curseur sur l’en-tête de la table demandes, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez une option pour la masquer ou l’afficher.  Les options actuellement affichées disposent de coches en regard de chaque élément.  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Ajout d’une colonne dans la table demandes" lightbox="../media/network-network-requests-add-column.msft.png":::
   Figure 16: ajout d’une colonne dans la table demandes  
:::image-end:::  

#### Ajouter des colonnes personnalisées  

Pour ajouter une colonne personnalisée dans la table demandes, positionnez le curseur sur l’en-tête de la table demandes, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez les **en-têtes de réponse**  >  **gérer les colonnes d’en-tête**.  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Ajout d’une colonne personnalisée dans la table demandes" lightbox="../media/network-network-requests-add-custom.msft.png":::
   Figure 17: ajout d’une colonne personnalisée dans la table demandes  
:::image-end:::  

### Afficher le minutage des requêtes les uns par rapport aux autres  

Utilisez la cascade pour afficher le minutage des requêtes les uns par rapport aux autres.  
Par défaut, la cascade est organisée selon l’heure de début des requêtes.  
Par conséquent, les demandes qui sont plus éloignées de gauche que celles qui sont plus éloignées.  

Pour plus d’options, voir [Trier par phase d’activité](#sort-by-activity-phase) .  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Colonne cascade du volet demandes" lightbox="../media/network-network-requests-waterfall.msft.png":::
   Figure 18: colonne cascade du volet **demandes**  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To view the frames of a WebSocket connection:  

1.  Select the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Select the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-select the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="The Frames tab" lightbox="../media/network-frames.msft.png":::
   Old Figure 20:  The **Frames** tab  
:::image-end:::  
-->

<!--The table contains three columns:  

*   **Data**.  The message payload.  If the message is plain text, it is displayed here.  For binary opcodes, this column displays the name and code of the opcode.  The following opcodes are supported: Continuation Frame, Binary Frame, Connection Close Frame, Ping Frame, and Pong Frame.  
*   **Length**.  The length of the message payload, in bytes.  
*   **Time**.  The time when the message was received or sent.  -->

<!--Messages are color-coded according to their type:  

*   Outgoing text messages are light-green.  
*   Incoming text messages are white.  
*   WebSocket opcodes are light-yellow.  
*   Errors are light-red.  -->

### Afficher un aperçu d’un corps de réponse  

Pour afficher un aperçu d’un corps de réponse:  

1.  Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.  
1.  Sélectionnez l’onglet **Aperçu** .  

Cet onglet est principalement utile pour afficher des images.  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Onglet Aperçu" lightbox="../media/network-network-resources-preview.msft.png":::
   Figure 19: onglet **Aperçu**  
:::image-end:::  

### Afficher le corps de la réponse  

Pour afficher le corps de la réponse à une demande:  

1.  Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.  
1.  Sélectionnez l’onglet **réponse** .  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Onglet réponse" lightbox="../media/network-network-resources-response.msft.png":::
   Figure 20: onglet **réponse**  
:::image-end:::  

### Afficher les en-têtes HTTP  

Pour afficher les données d’en-tête HTTP relatives à une requête:  

1.  Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.  
1.  Sélectionnez l’onglet **en-têtes** .  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Onglet en-têtes" lightbox="../media/network-resources-headers.msft.png":::
   Figure 21: onglet **en-têtes**  
:::image-end:::  

#### Afficher une source d’en-tête HTTP  

Par défaut, l’onglet en-têtes affiche les noms des en-têtes par ordre alphabétique.  Pour afficher les noms d’en-tête HTTP dans l’ordre dans lequel ils ont été reçus:  

1.  Ouvrez l’onglet **en-têtes** pour la requête qui vous intéresse.  Voir [afficher les en-têtes http](#view-http-headers).  
1.  Sélectionnez **afficher la source**, en regard de la section en **-tête de requête** ou **en-tête de réponse** .  

### Afficher les paramètres de chaîne de requête  

Pour afficher les paramètres de chaîne de requête d’une URL dans un format lisible par l’utilisateur:  

1.  Ouvrez l’onglet **en-têtes** pour la requête qui vous intéresse.  Voir [afficher les en-têtes http](#view-http-headers).  
1.  Accédez à la section **paramètres de chaîne de requête** .  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Section paramètres de chaîne de requête" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   Figure 22: section **paramètres de chaînes de requête**  
:::image-end:::  

#### Afficher les paramètres de chaîne de requête source  

Pour afficher la source du paramètre de chaîne de requête d’une requête:  

1.  Accédez à la section paramètres de chaîne de requête.  Voir [afficher les paramètres de chaîne de requête](#view-query-string-parameters).  
1.  Sélectionnez **afficher la source**.  

#### Afficher les paramètres de chaîne de requête codés en URL  

Pour afficher les paramètres de chaîne de requête dans un format lisible par l’utilisateur, mais avec les codages conservés:  

1.  Accédez à la section paramètres de chaîne de requête.  Voir [afficher les paramètres de chaîne de requête](#view-query-string-parameters).  
1.  Sélectionnez **afficher l’URL**.  

### Afficher les cookies  

Pour afficher les cookies envoyés dans l’en-tête HTTP d’une requête:  

1.  Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.  
1.  Sélectionnez l’onglet **cookies** .  

<!--See [Fields][ManageDataCookiesFields] for a description of each of the columns.  -->

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->
<!--TODO: add link when section is available -->

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Onglet cookies" lightbox="../media/network-network-resources-cookies.msft.png":::
   Figure 23: onglet cookies  
:::image-end:::  

### Afficher la répartition du minutage d’une requête  

Pour afficher la répartition du minutage d’une requête:  

1.  Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.  
1.  Sélectionnez l’onglet **minutage** .  

Pour plus d’informations sur l’accès à ces données, voir [aperçu d’une répartition du temps](#preview-a-timing-breakdown) .  

Pour plus d’informations sur les différentes phases que vous pouvez voir dans l’onglet Minutage, consultez la rubrique [étapes de répartition du temps](#timing-breakdown-phases-explained) .  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Onglet Minutage" lightbox="../media/network-network-resources-timing.msft.png":::
   Figure 24: onglet **minutage**  
:::image-end:::  

Plus d’informations sur chacune de ces étapes.  

Pour accéder à cet affichage, voir répartition de l' [affichage du minutage](#view-the-timing-breakdown-of-a-request) .  

#### Prévisualiser une répartition de minutage  

Pour afficher un aperçu de la répartition du minutage d’une requête, placez le pointeur sur l’entrée de la requête dans la colonne **cascade** de la table demandes.  

Pour accéder à ces données qui ne nécessitent pas de pointage, voir [afficher la répartition du minutage d’une demande](#view-the-timing-breakdown-of-a-request) .  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> aperçu de la répartition du minutage d’une requête" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   Figure 25: prévisualisation de la répartition du minutage d’une requête  
:::image-end:::  

#### Explication des phases de répartition du temps  

Plus d’informations sur chacune des phases que vous pouvez voir dans l’onglet **minutage** .  

*   Mise en **file d’attente**.  Le navigateur met en file d’attente les requêtes dans les cas suivants:  
    *   Il y a des demandes de priorité plus élevées.  
    *   Il existe déjà six connexions TCP ouvertes pour cette origine, qui correspond à la limite.  S’applique uniquement aux protocoles HTTP/1.0 et HTTP/1.1.  
    *   Le navigateur alloue de l’espace dans le cache disque.  
*   **Bloqué**.  La requête peut être bloquée pour l’une des raisons décrites dans la **file d’attente**.  
*   **Recherche DNS**.  Le navigateur résout l’adresse IP pour la requête.  
*   **Connexion initiale**.  Le navigateur établit une connexion, notamment les négociations TCP, les tentatives de connexion TCP et la négociation d’une connexion SSL.
*   **Négociation de proxy**.  Le navigateur négocie la requête avec un [serveur proxy][WikiProxyServer].  
*   **Demande envoyée**.  La requête est en cours d’envoi.  
*   **Préparation ServiceWorker**.  Le navigateur démarre le travailleur du service.  
*   **Demander à ServiceWorker**.  La demande est envoyée au travailleur de service.  
*   En **attente \ (TTFB \)**.  Le navigateur attend le premier octet d’une réponse.  
  TTFB représente le temps à l’octet initial.  Ce minutage inclut un aller-retour d’une latence et la durée du serveur pour préparer la réponse.  
*   **Téléchargement du contenu**.  Le navigateur reçoit la réponse.  
*   **Réception**d’une émission.  Le navigateur reçoit des données pour cette réponse via le protocole HTTP/2 Server Poussée.  
*   **Lecture en lecture**.  Le navigateur lit les données locales précédemment reçues.  

### Afficher les initiateurs et les dépendances  

Pour afficher les initiateurs et les dépendances d’une requête, maintenez la touche enfoncée `Shift` et placez le pointeur sur la requête dans la table demandes.  Couleurs de DevTools: les initiateurs apparaissent en vert et les dépendances apparaissent en rouge.  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Affichage des déclencheurs et des dépendances d’une requête" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   Figure 26: affichage des déclencheurs et dépendances d’une requête  
:::image-end:::  

Lorsque la table requêtes est classée dans un ordre chronologique, la première demande verte au-dessus de celle où vous pointez est l’initiateur de la dépendance.  Si une autre demande verte s’affiche au-dessus de celle-ci, il s’agit de l’initiateur de l’initiateur.  Et ainsi de suite.  

### Afficher les événements de chargement  

DevTools affiche le minutage des `DOMContentLoaded` événements et `load` dans plusieurs emplacements du panneau réseau.  L' `DOMContentLoaded` événement est coloré en bleu et l' `load` événement est rouge.  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Emplacements des événements DOMContentLoaded et Load sur le panneau réseau" lightbox="../media/network-network-requests-load-events.msft.png":::
   Figure 27: emplacements des `DOMContentLoaded` `load` événements et sur le panneau réseau  
:::image-end:::  

### Afficher le nombre total de demandes  

Le nombre total de demandes est répertorié dans le volet Résumé, au bas du panneau réseau.  

> [!CAUTION]
> Ce numéro suit uniquement les requêtes qui ont été enregistrées depuis l’ouverture de DevTools.  Si d’autres requêtes s’est produites avant l’ouverture de DevTools, ces demandes ne sont pas comptabilisées.  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Nombre total de demandes depuis l’ouverture de DevTools" lightbox="../media/network-network-total-requests.msft.png":::
   Figure 28: nombre total de demandes depuis l’ouverture de DevTools  
:::image-end:::  

### Affichez la taille totale du téléchargement  

La taille de téléchargement totale des demandes figure dans le volet Résumé, en bas du volet réseau.  

> [!CAUTION]
> Ce numéro suit uniquement les requêtes qui ont été enregistrées depuis l’ouverture de DevTools.  Si d’autres requêtes s’est produites avant l’ouverture de DevTools, les requêtes précédentes ne sont pas comptabilisées.  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="La taille de téléchargement totale des requêtes" lightbox="../media/network-network-total-download-size.msft.png":::
   Figure 29: taille totale du téléchargement de demandes  
:::image-end:::  

Pour afficher [le nombre de ressources de taille décompressées, voir afficher la taille d’une ressource](#view-the-uncompressed-size-of-a-resource) , puis décompresser chaque élément.  

### Afficher la trace de pile ayant entraîné une requête  

Après qu’une instruction JavaScript demande une ressource, placez le pointeur sur la colonne **Initiator** pour afficher la trace de pile qui se trouve au début de la requête.  

<!-- [codepen.io/contoso/pen/yLBrOWa?editors=0010#0](https://codepen.io/contoso/pen/yLBrOWa?editors=0010#0) -->  

<!--
```javascript
function init() {
  getData();
}

function getData() {
  fetch('https:/httpbin.org/get?message=hi');
}

init();
```  
-->  

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="Trace de pile aboutissant à une demande de ressources" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   Figure 30: trace de pile aboutissant à une demande de ressources  
:::image-end:::  

### Affichage de la taille de la ressource non compressée  

Activez la case à cocher **utiliser des lignes de requête volumineuses** , puis examinez la valeur inférieure de la colonne **taille** .  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Exemple de ressources non compressées" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   Figure 31: exemple de ressources non compressées \ (la taille du `jquery-3.3.1.min.js` fichier qui a été envoyée par le biais du réseau était `29.9 KB` , alors que la taille du fichier non compressé était de `84.9 KB` \)  
:::image-end:::  

## Exporter les données de requête  

### Enregistrer toutes les demandes réseau dans un fichier QAR  

Pour enregistrer toutes les demandes réseau dans un fichier QAR, procédez comme suit.  

1.  Positionnez le pointeur sur une requête dans la table demandes et ouvrez le menu contextuel, puis cliquez sur le bouton droit de la souris.  
1.  Sélectionnez **Save As QAR with content**.  DevTools enregistre toutes les demandes qui se sont produites depuis que vous avez ouvert DevTools sur le fichier.  Il n’est pas possible de filtrer les demandes ou de n’enregistrer qu’une seule demande.  

Lorsque vous enregistrez un fichier QAR, vous pouvez l’importer de nouveau dans DevTools pour analyse.  Il suffit de glisser-déplacer le fichier QAR dans la table demandes.  
<!--See also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Sélection de l’option Enregistrer sous le contenu de votre fichier" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   Figure 32: sélection **de l’option Enregistrer sous le contenu de votre fichier** .  
:::image-end:::  

### Copier une ou plusieurs demandes dans le presse-papiers  

Dans la colonne **nom** de la table demandes, positionnez le pointeur sur une requête, ouvrez le menu contextuel **, puis**sélectionnez l’une des options suivantes...  

*   **Copier l’adresse du lien**.  Copiez l’URL de la requête dans le presse-papiers.  
*   **Copier la réponse**.  Copiez le corps de la réponse dans le presse-papiers.  
*   **Copy As FETCH**.  
*   **Copier comme courbe**.  Copiez la demande en tant que commande en forme de boucle.  
*   **Copy All As FETCH**.  
*   **Tout copier comme courbe**.  Copiez toutes les demandes comme une chaîne de commandes bouclé.  
*   **Copy All As QAR**.  Copiez toutes les demandes en tant que données QAR.  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Sélection de l’option copier la réponse" lightbox="../media/network-network-requests-copy-response.msft.png":::
   Figure 33: sélection de l’option **copier la réponse**  
:::image-end:::  

## Modifier la disposition du panneau réseau  

Vous pouvez développer ou réduire des sections de l’interface utilisateur du panneau réseau pour cibler les informations importantes.  

### Masquer le volet filtres  

Par défaut, DevTools affiche le **volet filtres**.  
Sélectionnez **Filter** ![ filtre ][ImageFilterIcon] de filtre pour le masquer.  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Bouton Masquer les filtres" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   Figure 34: bouton Masquer les filtres  
:::image-end:::  

### Utiliser des lignes de requête volumineuses  

Utilisez des lignes de grande taille si vous voulez plus d’espace dans votre tableau de requêtes réseau.  Certaines colonnes fournissent également quelques informations supplémentaires sur l’utilisation de lignes de grande taille.  Par exemple, la valeur la plus en bas de la colonne **taille** correspond à la taille de requête non compressée.  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Exemple de longues lignes de requête dans le volet requêtes" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   Figure 35: exemple de longues lignes de requête dans le volet **requêtes**  
:::image-end:::  

Activez la case à cocher **utiliser des lignes de requête volumineuses** pour activer les lignes de grande taille.  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Case à cocher utiliser de grandes lignes de requête" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   Figure 36: case à cocher **utiliser des lignes de requête volumineuses**  
:::image-end:::  

### Masquer le volet vue d’ensemble  

Par défaut, DevTools affiche le **volet vue d’ensemble**.  Désélectionnez la case à cocher **afficher la vue d’ensemble** pour la masquer.  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Case à cocher Afficher la vue d’ensemble" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   Figure 37: case à cocher **afficher la vue d’ensemble**  
:::image-end:::  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: ../media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: ../media/clear-requests-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageHideIcon]: ../media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: ../media/record-on-icon.msft.png  

<!-- links -->  

[DevtoolsProgressiveWebApps]: /microsoft-edge/devtools-guide-chromium/network/progressive-web-apps "Déboguer des applications Web progressives"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "URL de données | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Serveur proxy-Wikipédia"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/network/reference) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
