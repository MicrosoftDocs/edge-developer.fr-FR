---
description: Référence complète des fonctionnalités Microsoft Edge panneau réseau DevTools.
title: Référence de l’analyse réseau
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: bdb1145e7ee8ed7865b68f9fd632c4b1a30007e9
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564832"
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
# <a name="network-analysis-reference"></a>Référence de l’analyse réseau  

Découvrez de nouvelles façons d’analyser le chargement de votre page dans cette référence complète Microsoft Edge fonctionnalités d’analyse réseau DevTools.  

## <a name="record-network-requests"></a>Enregistrer des demandes réseau  

Par défaut, DevTools enregistre toutes **** les demandes réseau dans l’outil Réseau, tant que DevTools est ouvert.  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Panneau réseau" lightbox="../media/network-network-panel.msft.png":::
   **L’outil** Réseau  
:::image-end:::  

### <a name="stop-recording-network-requests"></a>Arrêter l’enregistrement des demandes réseau  

Pour arrêter l’enregistrement des demandes, complétez les étapes suivantes.  

1.  Dans **l’outil Réseau,** **sélectionnez Arrêter l’enregistrement du journal réseau** \( ![ Arrêter l’enregistrement du journal ](../media/record-on-icon.msft.png) réseau \).  Il devient gris pour indiquer que DevTools n’enregistre plus les demandes.  
1.  Sélectionnez `Control` + `E` \(Windows, Linux\) ou `Command` + `E` \(macOS\) **** lorsque l’outil Réseau est en cours de mise au point.  

### <a name="clear-requests"></a>Effacer les demandes  

Sélectionnez **Effacer** \( ![ Effacer \) sur l’outil Réseau pour effacer toutes les demandes de ](../media/clear-requests-icon.msft.png) la table Requests. ****  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Bouton Effacer" lightbox="../media/network-network-clear-button.msft.png":::
   Bouton **** Effacer  
:::image-end:::  

### <a name="save-requests-across-page-loads"></a>Enregistrer des demandes sur les chargements de page  

Pour enregistrer les demandes sur les chargements de page, sur l’outil **Réseau,** activer la case à cocher Conserver **le journal.**  DevTools enregistre toutes les demandes jusqu’à ce que vous **désactiviez conserver le journal.**  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Case à cocher Conserver le journal" lightbox="../media/network-network-preserve-log.msft.png":::
   Case **à cocher** Conserver le journal  
:::image-end:::  

### <a name="capture-screenshots-during-page-load"></a>Capture d’écran pendant le chargement de la page  

Capturez des captures d’écran pour analyser ce qui s’affiche pour les utilisateurs en attendant le chargement de votre page.  

Pour activer les captures d’écran, **** **sélectionnez Paramètres**réseau et, dans l’outil Réseau, activez la case à cocher Capturer les **captures d’écran.**  

Actualisez la page lorsque **l’outil** Réseau est en cours de mise en place pour capturer des captures d’écran.  

Après avoir capturé une capture d’écran, vous interagissez avec elle des manières suivantes.  

*   Pointez sur une capture d’écran pour afficher le point auquel cette capture d’écran a été capturée.  Une ligne jaune s’affiche dans le **volet** Vue d’ensemble.  
*   Choisissez la miniature d’un écran pour filtrer toutes les demandes qui se sont produites après la capture d’écran.  
*   Double-cliquez sur une miniature pour la zoomer.  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Pointer sur une capture d’écran" lightbox="../media/network-network-screenshot-hover.msft.png":::
   Pointer sur une capture d’écran  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and choose **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Choose Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Choose Replay XHR  
:::image-end:::  
-->  

## <a name="change-loading-behavior"></a>Modifier le comportement de chargement  

### <a name="emulate-a-first-time-visitor-by-disabling-the-browser-cache"></a>Émuler un premier visiteur en désactivant le cache du navigateur  

Pour émuler la façon dont un utilisateur se retrouve pour la première fois sur votre site, cochez la case Désactiver le **cache.**  DevTools désactive le cache du navigateur.  Cette fonctionnalité émule plus précisément l’expérience d’un premier utilisateur, car les demandes sont reçues à partir du cache du navigateur lors de visites répétées.  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Case à cocher Désactiver le cache" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   Case **à cocher** Désactiver le cache  
:::image-end:::  

#### <a name="disable-the-browser-cache-from-the-network-conditions-drawer"></a>Désactiver le cache du navigateur à partir du caisse des conditions réseau  

Si vous souhaitez désactiver le cache tout en travaillant dans d’autres panneaux DevTools, utilisez le panneau Conditions réseau.  

1.  Ouvrez le **caisse des conditions réseau.**  
1.  Activer \(ou désactiver\) la case à cocher Désactiver le **cache.**  

<!--todo: add network condition section when available -->  

### <a name="manually-clear-the-browser-cache"></a>Effacer manuellement le cache du navigateur  

Pour effacer manuellement le cache du navigateur à tout moment, ouvrez le menu contextuel \(clic droit\) n’importe où dans la table Demandes et choisissez Effacer le **cache du navigateur.**  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Choisir Effacer le cache du navigateur" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   Choisir **Effacer le cache du navigateur**  
:::image-end:::  

### <a name="emulate-offline"></a>Émuler hors connexion  

Une nouvelle classe d’applications web, nommée [Progressive Web Apps,][DevtoolsProgressiveWebApps]fonctionne en mode hors connexion à l’aide des travailleurs **du service.**  Il peut s’avérer utile de simuler rapidement un appareil sans connexion de données lorsque vous construisez ce type d’application.  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

Choisissez le menu déroulant **En** ligne, recherchez sous **Presets**et choisissez **Hors** connexion pour simuler une expérience réseau hors connexion.  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Menu déroulant Hors connexion" lightbox="../media/network-network-offline-dropdown.msft.png":::
   Menu **déroulant Hors** connexion  
:::image-end:::  

### <a name="emulate-slow-network-connections"></a>Émuler les connexions réseau lentes  

Émulez les vitesses 3G, 3G rapides et autres vitesses de connexion à partir du menu déroulant **En** ligne.  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Menu déroulant Limitation" lightbox="../media/network-network-throttling-menu.msft.png":::
   Menu **déroulant Limitation**  
:::image-end:::  

Vous pouvez choisir parmi différents prérets, tels que Slow 3G ou Fast 3G.  Pour ajouter vos propres prérets personnalisés, ouvrez le menu Limitation, puis choisissez **Ajouter**  >  **personnalisé.**  

DevTools affiche une icône d’avertissement à côté de l’outil Réseau pour vous rappeler que la limitation est activée. ****  

#### <a name="emulate-slow-network-connections-from-the-network-conditions-drawer"></a>Émuler les connexions réseau lentes à partir du caisse de conditions réseau  

Si vous souhaitez limiter la connexion réseau tout en travaillant dans d’autres panneaux DevTools, utilisez le panneau Conditions réseau.  

1.  Ouvrez le **caisse des conditions réseau.**  
1.  Choisissez votre vitesse de connexion dans le menu **Limitation.**  

<!--todo: add network condition section when available -->  

### <a name="manually-clear-browser-cookies"></a>Effacer manuellement les cookies du navigateur  

Pour effacer manuellement les cookies du navigateur à tout moment, pointez n’importe où dans la table Demandes, ouvrez le menu contextuel \(clic droit\), puis choisissez Effacer les **cookies du navigateur.**  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Choose Clear Browser Cookies" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   Choose **Clear Browser Cookies**  
:::image-end:::  

### <a name="override-the-user-agent"></a>Remplacer l’agent utilisateur  

Pour remplacer manuellement l’agent utilisateur, utilisez les étapes suivantes.  

1.  Ouvrez le **caisse des conditions réseau.**  
1.  Désactiver la case **à cocher Sélectionner** automatiquement.  
1.  Choisissez une option d’agent utilisateur dans le menu ou entrez une option personnalisée dans la zone de texte.  

<!--todo: add network condition section when available -->  

## <a name="filter-requests"></a>Filtrer les demandes  

### <a name="filter-requests-by-properties"></a>Filtrer les demandes par propriétés  

Utilisez la **zone de** texte Filtrer pour filtrer les demandes par propriétés, telles que le domaine ou la taille de la demande.  

Si la zone de texte n’est pas affichée, le volet **Filtres** est probablement masqué.  
Pour plus d’informations, [accédez à Masquer le volet Filtres.](#hide-the-filters-pane)  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Zone de texte Filtrer" lightbox="../media/network-network-filters-textbox.msft.png":::
   Zone **de texte** Filtrer  
:::image-end:::  

Vous pouvez utiliser plusieurs propriétés simultanément en séparant chaque propriété par un espace.  Par exemple, affiche tous les PNG dont la taille `mime-type:image/png larger-than:1K` est supérieure à 1 kilo-octet.  Les filtres multi-propriétés sont équivalents aux `AND` opérations.  `OR` ne sont actuellement pas pris en charge.  

Liste complète des propriétés pris en charge.  

| Propriété | Détails |  
|:--- | :--- |  
| `domain` | Afficher uniquement les ressources du domaine spécifié.  Vous pouvez utiliser un caractère générique \( `*` \) pour inclure plusieurs domaines.  Par exemple, `*.com` affiche les ressources de tous les noms de domaine se terminant par `.com` .  DevTools remplit le menu déroulant de la mise à jour de la mise à jour automatique avec tous les domaines trouvés. |  
| `has-response-header` | Affiche les ressources qui contiennent l’en-tête de réponse HTTP spécifié.  DevTools remplit la zone de mise à jour de la mise à jour automatique avec tous les en-têtes de réponse trouvés. |  
| `is` | À `is:running` utiliser pour rechercher des `WebSocket` ressources. |  
| `larger-than` | Affiche les ressources dont la taille est supérieure à la taille spécifiée, en octets.  Définir une valeur de `1000` . `1k` |  
| `method` | Affiche les ressources qui ont été récupérées sur un type de méthode HTTP spécifié.  DevTools remplit la zone de détail avec toutes les méthodes HTTP trouvées. |  
| `mime-type` | Affiche les ressources d’un type MIME spécifié.  DevTools remplit la zone de détail avec tous les types MIME trouvés. |  
| `mixed-content` | Afficher toutes les ressources de contenu mixte \( \) ou uniquement ceux qui sont `mixed-content:all` actuellement affichés \( `mixed-content:displayed` \). |  
| `scheme` | Affiche les ressources récupérées sur HTTP \( \) ou `scheme:http` HTTPS \( `scheme:https` \) protégé. |  
| `set-cookie-domain` | Affiche les ressources qui ont un `Set-Cookie` en-tête avec un `Domain` attribut qui correspond à la valeur spécifiée.  DevTools remplit la mise à jour automatique avec tous les domaines de cookie trouvés. |  
| `set-cookie-name` | Affiche les ressources qui ont un `Set-Cookie` en-tête dont le nom correspond à la valeur spécifiée.  DevTools remplit la mise à jour automatique avec tous les noms de cookies trouvés. |  
| `set-cookie-value` | Affiche les ressources qui ont un `Set-Cookie` en-tête avec une valeur qui correspond à la valeur spécifiée.  DevTools remplit la mise à jour automatique avec toutes les valeurs de cookie trouvées. |  
| `status-code` | Affiche les ressources qui correspondent au code d’état HTTP spécifique.  DevTools remplit le menu déroulant de lacomplet automatique avec tous les codes d’état trouvés. |  

### <a name="filter-requests-by-type"></a>Filtrer les demandes par type  

Pour filtrer les demandes par type de requête, choisissez l’un des boutons suivants sur **l’outil** Réseau.  

:::row:::
   :::column span="1":::
      **XHR**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **JS**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **CSS**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Img**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Media**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Police**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Doc**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **WS**  
   :::column-end:::
   :::column span="2":::
      WebSocket.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Manifeste**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Other**  
   :::column-end:::
   :::column span="2":::
      Tout autre type non répertorié.  
   :::column-end:::
:::row-end:::  

Si les boutons ne s’affichent pas, le volet **Filtres** peut être masqué.  
Pour plus d’informations, [accédez à Masquer le volet Filtres.](#hide-the-filters-pane)  

Pour activer plusieurs filtres de type simultanément, `Control` maintenez \(Windows, Linux\) ou `Command` \(macOS\), puis choisissez.  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Utiliser les filtres type pour afficher les ressources JS, CSS et Document" lightbox="../media/network-network-type-filters.msft.png":::
   Utiliser les filtres type pour afficher les ressources JS, CSS et Document  
:::image-end:::  

### <a name="filter-requests-by-time"></a>Filtrer les demandes par heure  

Choisissez et faites glisser **** vers la gauche ou la droite dans le volet Vue d’ensemble pour afficher uniquement les demandes qui étaient actives pendant cette période.  Le filtre est inclus.  Toutes les demandes qui étaient actives pendant l’heure en surbrillant sont affichées.  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Filtrer toutes les demandes inactives d’environ 300 ms" lightbox="../media/network-network-overview-filter.msft.png":::
   Filtrer toutes les demandes inactives d’environ 300 ms  
:::image-end:::  

### <a name="hide-data-urls"></a>Masquer les URL de données  

[Les URL de données sont][MDNHTTPDataURIs] de petits fichiers incorporés dans d’autres documents.  Toute demande qui s’affiche dans la table Demandes qui commence par `data:` est une URL de données.  

Pour masquer les demandes, cochez la case Masquer **les URL de** données.  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Case à cocher Masquer les URL de données" lightbox="../media/network-network-hide-data-urls.msft.png":::
   Case **à cocher Masquer les URL de** données  
:::image-end:::  

## <a name="sort-requests"></a>Trier les demandes  

Par défaut, les demandes de la table Requests sont triées par heure d’initiation, mais vous pouvez trier le tableau à l’aide d’autres critères.  

### <a name="sort-by-column"></a>Trier par colonne  

Choisissez l’en-tête d’une colonne dans les demandes de tri des demandes par cette colonne.  

### <a name="sort-by-activity-phase"></a>Trier par phase d’activité  

Pour modifier la façon dont la cascade trie les demandes, pointez sur l’en-tête de la table Requests, ouvrez le menu contextuel \(clic droit\), pointez sur Cascade **et**choisissez l’une des options suivantes.  

:::row:::
   :::column span="1":::
      **Heure de début**  
   :::column-end:::
   :::column span="2":::
      La première demande qui a été lancée se trouve en haut.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Temps de réponse**  
   :::column-end:::
   :::column span="2":::
      La première requête qui a démarré le téléchargement se trouve en haut.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Heure de fin**  
   :::column-end:::
   :::column span="2":::
      La première requête terminée se trouve en haut.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Durée totale**  
   :::column-end:::
   :::column span="2":::
      La demande avec les paramètres de connexion et la demande ou la réponse les plus courts se trouve en haut.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Latence**  
   :::column-end:::
   :::column span="2":::
      La demande qui a attendu le plus court moment pour une réponse se trouve en haut.  
   :::column-end:::
:::row-end:::  

Ces descriptions supposent que chaque option respective est classée du plus court au plus long.  Choisissez l’en-tête de la colonne **Cascade** pour inverser l’ordre.  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Trier la cascade par durée totale" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   Trier la cascade par durée totale \(La partie la plus claire de chaque barre est le temps passé en attente et la partie la plus sombre est le temps consacré au téléchargement d’octets\)  
:::image-end:::  

## <a name="analyze-requests"></a>Analyser les demandes  

Tant que DevTools est ouvert, il enregistre toutes les demandes dans **l’outil** Réseau.  
Utilisez le panneau réseau pour analyser les demandes.  

### <a name="display-a-log-of-requests"></a>Afficher un journal des demandes  

Utilisez la table Requests pour afficher un journal de toutes les demandes réalisées alors que DevTools a été ouvert.  Pour révéler plus d’informations sur chaque élément, choisissez ou pointez sur les demandes.  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Table Requests" lightbox="../media/network-network-requests-table.msft.png":::
   Table Requests  
:::image-end:::  

La table Requests affiche les colonnes suivantes par défaut.  

:::row:::
   :::column span="1":::
      **Nom**  
   :::column-end:::
   :::column span="2":::
      Nom de fichier ou identificateur de la ressource.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Statut**  
   :::column-end:::
   :::column span="2":::
      Code d’état HTTP.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Type**  
   :::column-end:::
   :::column span="2":::
      Type MIME de la ressource demandée.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Initiateur**  
   :::column-end:::
   :::column span="2":::
      Les objets ou processus suivants lancent des demandes.  
      
      *   **Parser**  L’Microsoft Edge HTML.  
      *   **Redirection**  Redirection HTTP.  
      *   **Script**  Fonction JavaScript.  
      *   **Autre**  Un autre processus ou une autre action, comme la navigation vers une page à l’aide d’un lien ou la saisie d’une URL dans la barre d’adresses.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Taille**  
   :::column-end:::
   :::column span="2":::
      Taille combinée des en-têtes de réponse et corps de la réponse, tel qu’il est remis par le serveur.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Heure**  
   :::column-end:::
   :::column span="2":::
      Durée totale, depuis le début de la demande jusqu’à la réception de l’byte final dans la réponse.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Cascade](#display-the-timing-relationship-of-requests)  
   :::column-end:::
   :::column span="2":::
      Répartition visuelle de l’activité pour chaque demande.  
   :::column-end:::
:::row-end:::  

#### <a name="add-or-remove-columns"></a>Ajouter ou supprimer des colonnes  

Pointez sur l’en-tête de la table Requests, ouvrez le menu contextuel \(clic droit\), puis choisissez une option pour le masquer ou l’afficher.  Les options actuellement affichées ont des coches en regard de chaque élément.  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Ajouter une colonne à la table Requests" lightbox="../media/network-network-requests-add-column.msft.png":::
   Ajouter une colonne à la table Requests  
:::image-end:::  

#### <a name="add-custom-columns"></a>Ajouter des colonnes personnalisées  

Pour ajouter une colonne personnalisée à la table Demandes, pointez sur l’en-tête de la **** table Demandes, ouvrez le menu contextuel \(clic droit\), puis choisissez En-têtes de réponse Gérer les colonnes d’en-tête.  >  ****  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Ajouter une colonne personnalisée à la table Requests" lightbox="../media/network-network-requests-add-custom.msft.png":::
   Ajouter une colonne personnalisée à la table Requests  
:::image-end:::  

### <a name="display-the-timing-relationship-of-requests"></a>Afficher la relation de minutage des demandes  

Utilisez la cascade pour afficher les relations de minutage des demandes.  
L’organisation par défaut de la cascade utilise l’heure de début des demandes.  
Ainsi, les demandes qui sont plus à gauche ont commencé plus tôt que les demandes qui sont plus à droite.  

Pour passer en revue les différentes façons de trier la cascade, accédez à [Trier par phase d’activité.](#sort-by-activity-phase)  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Colonne Cascade du volet Demandes" lightbox="../media/network-network-requests-waterfall.msft.png":::
   Colonne Cascade du volet **Demandes**  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To review the frames of a WebSocket connection, use the following steps.  

1.  Choose the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Choose the **Frames** panel.  The table shows the last 100 frames.  

To refresh the table, re-choose the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="The Frames panel" lightbox="../media/network-frames.msft.png":::
   The **Frames** panel  
:::image-end:::  
-->

<!--The table contains the following three columns.  

*   **Data**.  The message payload.  If the message is plain text, it is displayed here.  For binary opcodes, this column displays the name and code of the opcode.  The following opcodes are supported: Continuation Frame, Binary Frame, Connection Close Frame, Ping Frame, and Pong Frame.  
*   **Length**.  The length of the message payload, in bytes.  
*   **Time**.  The time when the message was received or sent.  -->

<!--Messages are color-coded according to each type.  

*   Outgoing text messages are light-green.  
*   Incoming text messages are white.  
*   WebSocket opcodes are light-yellow.  
*   Errors are light-red.  -->

### <a name="display-a-preview-of-a-response-body"></a>Afficher un aperçu du corps d’une réponse  

Pour afficher un aperçu d’un corps de réponse, utilisez les étapes suivantes.  

1.  Choisissez l’URL de la demande, sous la **colonne Nom** de la table Requests.  
1.  Choisissez le **panneau d’aperçu.**  

L’onglet Aperçu est principalement utile pour afficher des images.  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Panneau d’aperçu" lightbox="../media/network-network-resources-preview.msft.png":::
   Panneau **d’aperçu**  
:::image-end:::  

### <a name="display-a-response-body"></a>Afficher un corps de réponse  

Pour afficher le corps de la réponse à une demande, utilisez les étapes suivantes.  

1.  Choisissez l’URL de la demande, sous la **colonne Nom** de la table Requests.  
1.  Sélectionnez **le panneau de** réponse.  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Panneau de réponse" lightbox="../media/network-network-resources-response.msft.png":::
   Panneau **de** réponse  
:::image-end:::  

### <a name="display-http-headers"></a>Afficher les en-têtes HTTP  

Pour afficher les données d’en-tête HTTP relatives à une demande, utilisez les étapes suivantes.  

1.  Choisissez l’URL de la demande, sous la **colonne Nom** de la table Requests.  
1.  Choisissez le **psanel d’en-têtes.**  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Panneau En-têtes" lightbox="../media/network-resources-headers.msft.png":::
   Panneau **En-têtes**  
:::image-end:::  

#### <a name="display-http-header-source"></a>Afficher la source d’en-tête HTTP  

Par défaut, le panneau **En-têtes** affiche les noms d’en-tête par ordre alphabétique.  Pour dsiplay les noms d’en-tête HTTP dans l’ordre reçu, utilisez les étapes suivantes.  

1.  Ouvrez **le panneau En-têtes** pour la demande qui vous intéresse.  Pour plus d’informations, accédez [à Afficher les en-têtes HTTP.](#display-http-headers)  
1.  Choisissez **la source d’affichage,** en regard de la section **En-tête de** demande ou **En-tête de réponse.**  

### <a name="display-query-string-parameters"></a>Afficher les paramètres de chaîne de requête  

Pour afficher les paramètres de chaîne de requête d’une URL dans un format lisible par l’homme, utilisez les étapes suivantes.  

1.  Ouvrez **le panneau En-têtes** pour la demande qui vous intéresse.  Pour plus d’informations, accédez [à Afficher les en-têtes HTTP.](#display-http-headers)  
1.  Accédez à la section **Paramètres de chaîne de requête.**  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Section Paramètres de chaîne de requête" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   Section **Paramètres de chaîne de** requête  
:::image-end:::  

#### <a name="display-query-string-parameters-source"></a>Afficher la source des paramètres de chaîne de requête  

Pour afficher la source du paramètre de chaîne de requête d’une requête, utilisez les étapes suivantes.  

1.  Accédez à la section Paramètres de chaîne de requête.  Pour plus d’informations, [accédez à Afficher les paramètres de chaîne de requête.](#display-query-string-parameters)  
1.  Choisissez **la source d’affichage.**  

#### <a name="display-url-encoded-query-string-parameters"></a>Afficher les paramètres de chaîne de requête codés en URL  

Pour afficher les paramètres de chaîne de requête dans un format lisible par l’homme, mais avec des codages conservés, utilisez les étapes suivantes.  

1.  Accédez à la section Paramètres de chaîne de requête.  Pour plus d’informations, [accédez à Afficher les paramètres de chaîne de requête.](#display-query-string-parameters)  
1.  Choisissez **l’URL d’affichage codée.**  

### <a name="display-cookies"></a>Afficher les cookies  

Pour afficher les cookies envoyés dans l’en-tête HTTP d’une requête, utilisez les étapes suivantes.  

1.  Choisissez l’URL de la demande, sous la **colonne Nom** de la table Requests.  
1.  Choisissez le **panneau Cookies.**  

<!--For more information about each of the columns, navigate to [Fields][ManageDataCookiesFields].  -->  

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->  
<!--TODO: add link when section is available -->  

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Panneau Cookies" lightbox="../media/network-network-resources-cookies.msft.png":::
   Panneau Cookies  
:::image-end:::  

### <a name="display-the-timing-breakdown-of-a-request"></a>Affichage de la répartition du minutage d’une demande  

Pour afficher la répartition du minutage d’une demande, utilisez les étapes suivantes.  

1.  Choisissez l’URL de la demande, sous la **colonne Nom** de la table Requests.  
1.  Sélectionnez **le panneau De minutage.**  

Pour accéder plus rapidement aux données, accédez à l’aperçu [d’une répartition du minutage.](#preview-a-timing-breakdown)  

Pour plus d’informations sur chacune des phases **** qui peuvent être affichées dans le panneau de minutage, accédez aux phases de répartition [du minutage expliquées.](#timing-breakdown-phases-explained)  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Panneau De minutage" lightbox="../media/network-network-resources-timing.msft.png":::
   Panneau **De minutage**  
:::image-end:::  

Plus d’informations sur chacune des phases.  

Pour plus d’informations sur l’accès à l’affichage, accédez à [Afficher la répartition du minutage.](#display-the-timing-breakdown-of-a-request)  

#### <a name="preview-a-timing-breakdown"></a>Afficher un aperçu de la répartition du minutage  

Pour afficher un aperçu de la répartition du minutage d’une demande, dans la colonne **Cascade** de la table Demandes, pointez sur l’entrée de la demande.  

Pour plus d’informations sur l’accès aux données sans pointage, accédez à Afficher la répartition du [minutage d’une demande.](#display-the-timing-breakdown-of-a-request)  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> aperçu de la répartition du minutage d’une demande" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   Afficher un aperçu de la répartition du minutage d’une demande  
:::image-end:::  

#### <a name="timing-breakdown-phases-explained"></a>Phases de répartition du minutage expliquées  

Plus d’informations sur chacune des phases qui peuvent s’afficher dans le **panneau Calendrier.**  

:::row:::
   :::column span="1":::
      **File d’attente**  
   :::column-end:::
   :::column span="2":::
      Le navigateur place les demandes en file d’attente lorsque l’une des valeurs suivantes est vraie.  
      
      *   Des demandes de priorité élevée existent.  
      *   Six connexions TCP sont ouvertes pour la même origine, ce qui est la limite.  S’applique uniquement à HTTP/1.0 et HTTP/1.1.  
      *   Le navigateur alloue brièvement de l’espace dans le cache disque.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Bloqué**  
   :::column-end:::
   :::column span="2":::
      La demande est bloquée pour l’une des raisons décrites dans **la file d’attente.**  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Recherche DNS**  
   :::column-end:::
   :::column span="2":::
      Le navigateur est en cours de résolution de l’adresse IP de la demande.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Connexion initiale**  
   :::column-end:::
   :::column span="2":::
      Le navigateur établit une connexion incluant des liaisons TCP, des tentatives TCP et négocie une couche de socket sécurisée.
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Négociation de proxy**  
   :::column-end:::
   :::column span="2":::
      Le navigateur négocie la demande avec un [serveur proxy.][WikiProxyServer]  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Demande envoyée**  
   :::column-end:::
   :::column span="2":::
      La demande est envoyée.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Préparation de ServiceWorker**  
   :::column-end:::
   :::column span="2":::
      Le navigateur démarre le service de travail.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Demande à ServiceWorker**  
   :::column-end:::
   :::column span="2":::
      La demande est envoyée au service de travail.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Waiting \(TTFB\)**  
   :::column-end:::
   :::column span="2":::
      Le navigateur attend le premier byte d’une réponse.  TTFB signifie « Time To First Byte ».  Ce délai inclut un aller-retour de latence et le temps que le serveur a pris pour préparer la réponse.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Téléchargement de contenu**  
   :::column-end:::
   :::column span="2":::
      Le navigateur reçoit la réponse.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Réception de push**  
   :::column-end:::
   :::column span="2":::
      Le navigateur reçoit des données pour cette réponse via HTTP/2 Server Push.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Lecture push**  
   :::column-end:::
   :::column span="2":::
      Le navigateur lit les données locales reçues précédemment.  
   :::column-end:::
:::row-end:::  

### <a name="display-initiators-and-dependencies"></a>Afficher les initiateurs et les dépendances  

Pour afficher les initiateurs et les dépendances d’une demande, maintenez la demande en attente et pointez dessus `Shift` dans la table Demandes.  Couleurs DevTools : les initiateurs sont affichés en vert et les dépendances en rouge.  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Afficher les initiateurs et les dépendances d’une demande" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   Afficher les initiateurs et les dépendances d’une demande  
:::image-end:::  

Lorsque la table Requests est classé dans l’ordre chronologique, si vous pointez sur une ligne, la ligne qui précède affiche une demande verte.  La demande verte est l’initiateur de la dépendance.  Si une autre demande verte est affichée sur la ligne avant cette ligne, cette demande supérieure est l’initiateur de l’initiateur.  Et ainsi de suite.  

### <a name="display-load-events"></a>Afficher les événements de chargement  

DevTools affiche le minutage des événements à plusieurs endroits `DOMContentLoaded` `load` sur **l’outil** Réseau.  `DOMContentLoaded`L’événement est de couleur bleue et l’événement est `load` rouge.  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Emplacements du DOMContentLoaded et chargement des événements sur le panneau réseau" lightbox="../media/network-network-requests-load-events.msft.png":::
   Emplacements des `DOMContentLoaded` `load` événements et des événements sur **l’outil** Réseau  
:::image-end:::  

### <a name="display-the-total-number-of-requests"></a>Affichage du nombre total de demandes  

Le nombre total de demandes **** est répertorié dans le volet Résumé, en bas de **l’outil** Réseau.  

> [!CAUTION]
> Ce numéro suit uniquement les demandes qui ont été enregistrées depuis l’ouverture de DevTools.  Si d’autres demandes se sont produites avant l’ouverture de DevTools, ces demandes ne sont pas comptabilisées.  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Nombre total de demandes depuis l’ouverture de DevTools" lightbox="../media/network-network-total-requests.msft.png":::
   Nombre total de demandes depuis l’ouverture de DevTools  
:::image-end:::  

### <a name="display-the-total-download-size"></a>Afficher la taille totale du téléchargement  

La taille totale des demandes de **** téléchargement est répertoriée dans le volet Résumé, en bas de **l’outil** Réseau.  

> [!CAUTION]
> Ce numéro suit uniquement les demandes qui ont été enregistrées depuis l’ouverture de DevTools.  Si d’autres demandes se sont produites avant l’ouverture de DevTools, les demandes précédentes ne sont pas comptabilisées.  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="Taille totale des demandes de téléchargement" lightbox="../media/network-network-total-download-size.msft.png":::
   Taille totale des demandes de téléchargement  
:::image-end:::  

Pour vérifier la taille des ressources une fois que le navigateur a décompressé chaque élément, accédez pour afficher la taille non [compressée d’une ressource.](#display-the-uncompressed-size-of-a-resource)  

### <a name="display-the-stack-trace-that-caused-a-request"></a>Afficher la trace de pile à l’origine d’une demande  

Après qu’une instruction JavaScript demande une ressource, pointez sur la colonne **Initiator** pour afficher la trace de pile précédant la demande.  

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

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="Trace de pile menant à une demande de ressource" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   Trace de pile menant à une demande de ressource  
:::image-end:::  

### <a name="display-the-uncompressed-size-of-a-resource"></a>Affichage de la taille non compressée d’une ressource  

Activer la case **à cocher Utiliser les lignes de requête** de grande taille, puis passer en revue la valeur inférieure de la **colonne** Taille.  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Exemple de ressources non compressées" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   Exemple de ressources non compressées \(La taille compressée du fichier envoyé sur le réseau était , alors que la taille non compressée était `jquery-3.3.1.min.js` `29.9 KB` `84.9 KB` \)  
:::image-end:::  

## <a name="export-requests-data"></a>Exporter les données des demandes  

### <a name="save-all-network-requests-to-a-har-file"></a>Enregistrer toutes les demandes réseau dans un fichier HAR  

Pour enregistrer toutes les demandes réseau dans un fichier HAR, complétez les étapes suivantes.  

1.  Pointez sur n’importe quelle demande dans la table Demandes et ouvrez le menu contextuel \(clic droit\).  
1.  Choose **Save as HAR with Content**.  DevTools enregistre toutes les demandes qui se sont produites depuis que vous avez ouvert DevTools dans le fichier HAR.  Vous ne pouvez pas filtrer les demandes.  Vous ne pouvez pas non plus enregistrer une seule requête.  

Une fois que vous enregistrez un fichier HAR, vous pouvez l’importer à nouveau dans DevTools pour analyse.  Il suffit de glisser-déposer le fichier HAR dans la table Requests.  
<!--For more information, navigate to also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Choose Save as HAR with Content" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   Choose **Save as HAR with Content**  
:::image-end:::  

### <a name="copy-one-or-more-requests-to-the-clipboard"></a>Copier une ou plusieurs demandes dans le Presse-papiers  

Sous la **colonne Nom** de la table Demandes, pointez sur une demande, ouvrez le menu contextuel \(clic droit\), pointez sur **Copier**et choisissez l’une des options suivantes.  

| Nom | Détails |  
|:--- |:--- |  
| **Copier l’adresse du lien** | Copiez l’URL de la demande dans le Presse-papiers. |  
| **Copier la réponse** | Copiez le corps de la réponse dans le Presse-papiers. |  
| **Copier en tant que récupération** | &nbsp; |  
| **Copier en tant que cURL** | Copiez la demande en tant que commande cURL. |  
| **Copier tout en tant que récupération** | &nbsp; |  
| **Copier tout en tant que cURL** | Copiez toutes les demandes en tant que chaîne de commandes cURL. |  
| **Copier tout en tant que har** | Copiez toutes les demandes en tant que données HAR. |  

<!--
:::row:::
   :::column span="1":::
      **Copy Link Address**  
   :::column-end:::
   :::column span="2":::
      Copy the URL of the request to the clipboard.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy Response**  
   :::column-end:::
   :::column span="2":::
      Copy the response body to the clipboard.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy as Fetch**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy as cURL**  
   :::column-end:::
   :::column span="2":::
      Copy the request as a cURL command.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as Fetch**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as cURL**  
   :::column-end:::
   :::column span="2":::
      Copy all requests as a chain of cURL commands.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as HAR**  
   :::column-end:::
   :::column span="2":::
      Copy all requests as HAR data.  
   :::column-end:::
:::row-end:::  
-->  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Choose Copy Response" lightbox="../media/network-network-requests-copy-response.msft.png":::
   Choose **Copy Response**  
:::image-end:::  

### <a name="copy-formatted-response-json-to-the-clipboard"></a>Copier la réponse mise en forme JSON dans le Presse-papiers  

Choisissez une demande réseau et accédez au volet **En-têtes.**  Pour copier la valeur JSON d’une réponse, accédez à Charge utile de la **demande,** pointez sur le contenu de la réponse JSON, ouvrez le menu contextuel \(clic droit\), puis choisissez Copier la **valeur**.  

:::row:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-copy-property-value.msft.png" alt-text="Copier la valeur dans le menu contextuel" lightbox="../media/network-header-copy-property-value.msft.png":::
          **Copier la valeur** dans le menu contextuel  
        :::image-end:::  
   :::column-end:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-paste-property-value.msft.png" alt-text="Microsoft Visual Studio Code avec réponse mise en forme JSON" lightbox="../media/network-header-paste-property-value.msft.png":::
          Pasting formatted response JSON in Microsoft Visual Studio Code  
        :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="copy-property-values-from-network-requests-to-your-clipboard"></a>Copier les valeurs des propriétés des demandes réseau dans votre Presse-papiers  

Pour copier les valeurs de propriétés des demandes réseau dans votre Presse-papiers, effectuer les actions suivantes.  

1.  Ouvrez **le volet En-têtes.**  
1.  Ouvrez l’une des sections d’en-tête suivantes.  
    *   Demander la charge utile \(JSON\)  
    *   Données de formulaire  
    *   Paramètres de chaîne de requête  
    *   En-têtes de requête  
    *   En-têtes de réponse  
1.  Ouvrez le menu contextuel \(clic droit\) > **valeur copier.**  Vous pouvez maintenant coller la valeur dans n’importe quel éditeur pour la réviser.  
    
## <a name="change-the-layout-of-the-network-panel"></a>Modifier la disposition du panneau Réseau  

Vous pouvez développer ou réduire **** des sections de l’interface utilisateur de l’outil réseau pour concentrer des informations importantes.  

### <a name="hide-the-filters-pane"></a>Masquer le volet Filtres  

Par défaut, DevTools affiche le volet **Filtres.**  
Choisissez **Filtre** \( ![ Filtre ](../media/filter-icon.msft.png) \) pour le masquer.  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Bouton Masquer les filtres" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   Bouton Masquer les filtres  
:::image-end:::  

### <a name="use-large-request-rows"></a>Utiliser des lignes de requête de grande taille  

Utilisez des lignes de grande taille lorsque vous souhaitez davantage d’espaces dans votre table de demandes réseau.  Certaines colonnes fournissent également un peu plus d’informations lors de l’utilisation de lignes de grande taille.  Par exemple, la valeur inférieure de la colonne **Size** est la taille non compressée d’une demande.  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Exemple de lignes de requête importantes dans le volet Demandes" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   Exemple de lignes de requête importantes dans le **volet Demandes**  
:::image-end:::  

Pour activer les lignes de grande taille, activez la case à cocher Utiliser les **lignes de requête de** grande taille.  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Case à cocher Utiliser les lignes de requête de grande taille" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   Case **à cocher Utiliser les lignes de requête de grande** taille  
:::image-end:::  

### <a name="hide-the-overview-pane"></a>Masquer le volet Vue d’ensemble  

Par défaut, DevTools **** affiche le volet Vue d’ensemble.  Pour le masquer, cochez la case **Afficher la** vue d’ensemble.  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Case à cocher Afficher la vue d’ensemble" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   Case **à cocher Afficher la vue d’ensemble**  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsProgressiveWebApps]: ../progressive-web-apps/index.md "Déboguer les applications web progressives | Documents Microsoft"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions | Microsoft Docs"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "URL de données | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Serveur proxy - Wikipedia"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/network/reference) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
