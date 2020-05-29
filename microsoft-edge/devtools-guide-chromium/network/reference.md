---
title: Référence d’analyse du réseau
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 460ad05983e7615e8739953ce3cb7d559492bc90
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611839"
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

> ##### Figure1  
> Panneau réseau  
> ![Panneau réseau][ImageNetworkPanel]  

### Arrêter l’enregistrement des requêtes réseau   

Pour arrêter l’enregistrement des demandes:  

*   Pour arrêter l' **enregistrement du journal du réseau** , cliquez sur arrêter l' ![ enregistrement réseau ][ImageRecordOnIcon] dans le panneau **réseau** .  Il devient gris pour indiquer que DevTools n’enregistre plus les demandes.  
*   Appuyez sur `Control` + `E` \ (Windows \) ou `Command` + `E` \ (MacOS \) lorsque le panneau **réseau** a le focus.  

### Supprimer des demandes   

Sélectionnez **Effacer** ![ ][ImageClearIcon] le panneau réseau pour effacer toutes les demandes de la table demandes.  

> ##### Figure 2  
> Bouton Effacer  
> ![Bouton Effacer][ImageClearButton]  

### Enregistrer les demandes lors du chargement de la page   

Pour enregistrer les demandes lors du chargement de la page, activez la case à cocher **conservation du journal** dans le panneau réseau.  DevTools enregistre toutes les demandes jusqu’à ce que vous désactiviez le **Journal de conservation**.  

> ##### Figure3  
> Case à cocher conserver le journal  
> ![Case à cocher conserver le journal][ImagePreserveLogCheckBox]  

### Capture de captures d’écran pendant le chargement de la page   

Capture des captures d’écran pour analyser ce que les utilisateurs voient lorsqu’ils attendent que votre page se charge.  

Pour activer les captures d’écran, sélectionnez **paramètres du réseau** , puis cochez la case **capturer les captures d’écran** dans le panneau **réseau** .  

Rechargez la page lorsque le panneau **réseau** a le focus pour capturer les captures d’écran.  

Après avoir capturé une capture d’écran, vous interagissez comme suit.  

*   Placez le pointeur de la souris sur une capture d’écran pour afficher le point d’acquisition de cette capture d’écran.  Une ligne jaune apparaît dans le volet **vue d’ensemble** .  
*   Sélectionnez la miniature d’un écran pour filtrer toutes les demandes qui se sont produites après la capture de la capture d’écran.  
*   Double-cliquez sur une miniature pour effectuer un zoom sur celle-ci.  

> ##### Figure 4  
> Survol d’une capture d’écran  
> ![Survol d’une capture d’écran][ImageScreenshotHover]  

<!--  ### Replay XHR request   -->

<!--  To replay an XHR request, right-click the request in the Requests table and select **Replay XHR**.  -->

<!--  
> ##### Old Figure 5  
> Selecting Replay XHR  
> ![Selecting Replay XHR][ImageReplayXHR]  
-->  

## Changer le comportement de chargement  

### Émuler un visiteur pour la première fois en désactivant le cache du navigateur   

Pour émuler la façon dont un utilisateur a expériences de votre site pour la première fois, activez la case à cocher **désactiver le cache** .  DevTools désactive le cache du navigateur.  Cela a pour effet d’émuler de façon plus précise une première utilisation de l’utilisateur, car les requêtes sont servies dans le cache du navigateur sur les visites répétées.  

> ##### Figure 5  
> Case à cocher Désactiver le cache  
> ! [Case à cocher Désactiver le cache] [ImageDisableCacheCheckBox]  

#### Désactiver le cache du navigateur dans le tiroir du réseau   

Si vous voulez désactiver le cache lorsque vous travaillez dans d’autres panneaux DevTools, utilisez le tiroir de l’état du réseau.  

1.  Ouvrez le tiroir de **conditions du réseau** .  
1.  Cochez ou décochez la case **désactiver le cache** .  

<!--todo: add network condition section when available -->  

### Vider manuellement le cache du navigateur   

Pour vider manuellement le cache du navigateur à tout moment, cliquez avec le bouton droit n’importe où dans la table demandes et sélectionnez **Vider le cache du navigateur**.  

> ##### Figure 6  
> Sélection de l’option vider le cache du navigateur  
> ! [Sélection de l’option vider le cache du navigateur] [ImageClearBrowserCache]  

### Émuler hors connexion   

Une nouvelle classe d’applications Web, appelée [application Web progressive][DevtoolsProgressiveWebApps], fonctionne en mode hors connexion avec l’aide des **travailleurs de service**.  Vous constaterez peut-être qu’il est utile de simuler rapidement un appareil dépourvu de connexion aux données lors de la création de ce type d’application.  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

Sélectionnez le menu déroulant **en ligne** , Rechercher sous **présélections**, puis sélectionnez **hors ligne** pour simuler une interface réseau entièrement hors connexion.  

> ##### Figure 7  
> Menu déroulant hors connexion  
> ! [Menu déroulant hors ligne] [ImageOfflineDropdown]  

### Émuler une connexion réseau lente   

Émulez des vitesses de connexion 3G, Fast 3G et autres vitesses de connexion dans le menu déroulant **en ligne** .  

> ##### Figure8  
> Menu déroulant limitation  
> ! [Menu déroulant limitation] [ImageNetworkThrottlingMenu]  

Vous pouvez faire votre choix parmi une série de présélections, par exemple, lente 3G ou Fast 3G.  Vous pouvez également ajouter vos propres Présélections personnalisées en ouvrant le menu limitation et **Custom**en sélectionnant  >  **Ajouter**personnalisé.  

DevTools affiche une icône d’avertissement en regard de l’onglet **réseau** pour vous rappeler que la limitation est activée.  

#### Émuler une connexion réseau lente à partir du tiroir du réseau   

Si vous souhaitez limiter la connexion réseau lorsque vous travaillez dans d’autres panneaux DevTools, utilisez le tiroir de l’état du réseau.  

1.  Ouvrez le tiroir de **conditions du réseau** .  
1.  Sélectionnez le débit de connexion souhaité dans le menu **limitation** .  

<!--todo: add network condition section when available -->  

### Effacement manuel des cookies du navigateur   

Pour effacer manuellement les cookies du navigateur à tout moment, cliquez avec le bouton droit n’importe où dans la table demandes, puis sélectionnez **effacer les cookies du navigateur**.  

> ##### Figure9  
> Sélection effacer les cookies du navigateur  
> ! [Sélectionner des cookies de navigateur clairs] [ImageClearBrowserCookies]  

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

> ##### Figure10  
> Zone de texte filtres  
> ! [Zone de texte filtres] [ImageFilterTextBox]  

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

> ##### Figure11  
> Utiliser les filtres de type pour afficher les ressources JS, CSS et document  
> ! [En utilisant les filtres de type pour afficher les ressources JS, CSS et documents] [ImageMultiTypeFilter]  

### Filtrer les demandes par heure   

Sélectionnez et faites glisser vers la gauche ou la droite dans le volet vue d’ensemble pour afficher uniquement les demandes actives au cours de cette période.  Le filtre est inclusive.  Toutes les demandes qui ont été actives pendant la durée en surbrillance apparaissent.  

> ##### Figure12  
> Filtrage des requêtes inactives depuis 300M  
> ! [Filtrage des requêtes inactives depuis 300M] [ImageOverviewFilter]  

### Masquer les URL de données  

Les [URL de données][MDNHTTPDataURIs] sont des petits fichiers incorporés dans d’autres documents.  Toute demande figurant dans la table demandes qui commence par `data:` est une URL de données.  

Cochez la case **Masquer les URL de données** pour masquer ces demandes.  

> ##### Figure13  
> Case à cocher Masquer les URL de données  
> ! [Cases à cocher Masquer les URL de données] [ImageHideDataURLsCheckBox]  

## Demandes de tri  

Par défaut, les requêtes dans la table demandes sont triées par heure de début, mais vous pouvez trier le tableau en utilisant d’autres critères.  

### Trier par colonne   

Sélectionnez l’en-tête de n’importe quelle colonne dans les requêtes pour trier les demandes en se sur cette colonne.  

### Trier par phase d’activité   

Pour modifier la façon dont les demandes de tri en cascade trient, cliquez avec le bouton droit sur l’en-tête de la table demandes, placez le pointeur sur **cascade**, puis sélectionnez l’une des options suivantes.  

*   **Heure de début**.  La première requête lancée est en haut.  
*   **Temps de réponse**.  La première demande qui a démarré le téléchargement est en haut.  
*   **Heure de fin**.  La première demande qui est terminée est en haut.  
*   **Durée totale**.  La requête avec la configuration de connexion la plus courte et la demande/réponse se trouvent dans la partie supérieure.  
*   **Latence**.  La requête qui a attendu le plus court délai d’une réponse est située en haut.  

Ces descriptions présupposent que chaque option respective est classée du plus court au plus long.  La sélection de l’en-tête de la colonne en **cascade** inverse l’ordre.  

> ##### Figure14  
> Le tri des cascades en fonction de la durée totale \ (la partie la plus claire de chaque barre est le temps passé en attente et la partie plus foncée est le temps de télécharger les octets \)  
> ! [Trier les cascade en fonction de la durée totale] [ImageWaterfallTotalDuration]  

## Analyser les requêtes   

Tant que DevTools est ouvert, il enregistre toutes les demandes dans le panneau réseau.  
Utilisez le volet réseau pour analyser les requêtes.  

### Afficher un journal des demandes   

Utilisez le tableau demandes pour afficher un journal de toutes les demandes effectuées lorsque DevTools est ouvert.  La sélection ou le passage de demandes au-dessus révèle des informations supplémentaires sur chaque élément.  

> ##### Figure15  
> Table demandes  
> ! [Table demandes] [ImageRequestsTable]  

La table demandes affiche les colonnes suivantes par défaut:  

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

Cliquez avec le bouton droit sur l’en-tête de la table demandes et sélectionnez une option pour la masquer ou l’afficher.  Les options actuellement affichées disposent de coches en regard de chaque élément.  

> ##### Figure16  
> Ajout d’une colonne dans la table demandes  
> ! [Ajout d’une colonne dans la table demandes] [ImageRequestsTableAddColumn]  

#### Ajouter des colonnes personnalisées   

Pour ajouter une colonne personnalisée à la table demandes, cliquez avec le bouton droit sur l’en-tête de la table demandes et sélectionnez **les en-têtes de réponse**  >  **gérer les colonnes d’en-tête**.  

> ##### Figure17  
> Ajout d’une colonne personnalisée dans la table demandes  
> ! [Ajout d’une colonne personnalisée dans la table demandes] [ImageRequestsTableCustomColumn]  

### Afficher le minutage des requêtes les uns par rapport aux autres   

Utilisez la cascade pour afficher le minutage des requêtes les uns par rapport aux autres.  
Par défaut, la cascade est organisée selon l’heure de début des requêtes.  
Par conséquent, les demandes qui sont plus éloignées de gauche que celles qui sont plus éloignées.  

Pour plus d’options, voir [Trier par phase d’activité](#sort-by-activity-phase) .  

> ##### Figure 18  
> Colonne cascade du volet demandes  
> ! [La colonne cascade du volet demandes] [ImageRequestsTableWaterfallColumn]  

<!-- ### Analyze the frames of a WebSocket Connection   -->

<!--To view the frames of a WebSocket connection:  

1.  Select the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Select the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-click the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
> ##### Old Figure 20  
> The Frames tab  
> ![The Frames tab][ImageFrames]  
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

> ##### Figure 19  
> Onglet Aperçu  
> ! [Onglet Aperçu] [ImagePreview]  

### Afficher le corps de la réponse   

Pour afficher le corps de la réponse à une demande:  

1.  Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.  
1.  Sélectionnez l’onglet **réponse** .  

> ##### Figure 20  
> Onglet réponse  
> ! [Onglet réponse] [ImageResponse]  

### Afficher les en-têtes HTTP   

Pour afficher les données d’en-tête HTTP relatives à une requête:  

1.  Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.  
1.  Sélectionnez l’onglet **en-têtes** .  

> ##### Figure 21  
> Onglet en-têtes  
> ! [Onglet en-têtes] [ImageHeaders]  

#### Afficher une source d’en-tête HTTP   

Par défaut, l’onglet en-têtes affiche les noms des en-têtes par ordre alphabétique.  Pour afficher les noms d’en-tête HTTP dans l’ordre dans lequel ils ont été reçus:  

1.  Ouvrez l’onglet **en-têtes** pour la requête qui vous intéresse.  Voir [afficher les en-têtes http](#view-http-headers).  
1.  Sélectionnez **afficher la source**, en regard de la section en **-tête de requête** ou **en-tête de réponse** .  

### Afficher les paramètres de chaîne de requête   

Pour afficher les paramètres de chaîne de requête d’une URL dans un format lisible par l’utilisateur:  

1.  Ouvrez l’onglet **en-têtes** pour la requête qui vous intéresse.  Voir [afficher les en-têtes http](#view-http-headers).  
1.  Accédez à la section **paramètres de chaîne de requête** .  

> ##### Figure 22  
> Section paramètres de chaîne de requête  
> ! [Section des paramètres de chaîne de requête] [ImageQueryStringParameters]  

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

> ##### Figure 23  
> Onglet cookies  
> ! [Onglet cookies] [ImageCookies]  

### Afficher la répartition du minutage d’une requête   

Pour afficher la répartition du minutage d’une requête:  

1.  Sélectionnez l’URL de la requête dans la colonne **nom** de la table demandes.  
1.  Sélectionnez l’onglet **minutage** .  

Pour plus d’informations sur l’accès à ces données, voir [aperçu d’une répartition du temps](#preview-a-timing-breakdown) .  

Pour plus d’informations sur les différentes phases que vous pouvez voir dans l’onglet Minutage, consultez la rubrique [étapes de répartition du temps](#timing-breakdown-phases-explained) .  

> ##### Figure 24  
> Onglet Minutage  
> ! [Onglet Minutage] [ImageTiming]  

Plus d’informations sur chacune de ces étapes.  

Pour accéder à cet affichage, voir répartition de l' [affichage du minutage](#view-the-timing-breakdown-of-a-request) .  

#### Prévisualiser une répartition de minutage   

Pour afficher un aperçu de la répartition du minutage d’une requête, placez le pointeur sur l’entrée de la requête dans la colonne **cascade** de la table demandes.  

Pour accéder à ces données qui ne nécessitent pas de pointage, voir [afficher la répartition du minutage d’une demande](#view-the-timing-breakdown-of-a-request) .  

> ##### Figure 25  
> Prévisualisation de la répartition du minutage d’une requête  
> ! [Aperçu de la répartition du minutage d’une requête] [ImageWaterfallHover]  

#### Explication des phases de répartition du temps   

Pour plus d’informations sur les différentes phases que vous pouvez voir dans l’onglet Minutage, procédez comme suit:  

*   Mise en **file d’attente**.  Le navigateur met en file d’attente les requêtes dans les cas suivants:  
    *   Il y a des demandes de priorité plus élevées.  
    *   Il existe déjà six connexions TCP ouvertes pour cette origine, qui correspond à la limite.  S’applique uniquement aux protocoles HTTP/1.0 et HTTP/1.1.  
    *   Le navigateur alloue de l’espace dans le cache disque.  
*   **Bloqué**.  La requête peut être bloquée pour l’une des raisons décrites dans la **file d’attente**.  
*   **Recherche DNS**.  Le navigateur résout l’adresse IP pour la requête.  
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

> ##### Figure 26  
> Affichage des déclencheurs et des dépendances d’une requête  
> ! [Affichage des déclencheurs et dépendances d’une requête] [ImageRequestInitiatorsDependencies]  

Lorsque la table requêtes est classée dans un ordre chronologique, la première demande verte au-dessus de celle où vous pointez est l’initiateur de la dépendance.  Si une autre demande verte s’affiche au-dessus de celle-ci, il s’agit de l’initiateur de l’initiateur.  Et ainsi de suite.  

### Afficher les événements de chargement   

DevTools affiche le minutage des `DOMContentLoaded` événements et `load` dans plusieurs emplacements du panneau réseau.  L' `DOMContentLoaded` événement est coloré en bleu et l' `load` événement est rouge.  

> ##### Figure 27  
> Emplacement des `DOMContentLoaded` `load` événements et dans le volet réseau  
> ! [Emplacements des événements DOMContentLoaded et Load sur le panneau réseau] [ImageNetworkPanelDOMContentLoadedLoadEvents]  

### Afficher le nombre total de demandes   

Le nombre total de demandes est répertorié dans le volet Résumé, au bas du panneau réseau.  

> [!CAUTION]
> Ce numéro suit uniquement les requêtes qui ont été enregistrées depuis l’ouverture de DevTools.  Si d’autres requêtes s’est produites avant l’ouverture de DevTools, ces demandes ne sont pas comptabilisées.  

> ##### Figure 28  
> Nombre total de demandes depuis l’ouverture de DevTools  
> ! [Nombre total de demandes depuis l’ouverture de DevTools] [ImageTotalRequests]  

### Affichez la taille totale du téléchargement   

La taille de téléchargement totale des demandes figure dans le volet Résumé, en bas du volet réseau.  

> [!CAUTION]
> Ce numéro suit uniquement les requêtes qui ont été enregistrées depuis l’ouverture de DevTools.  Si d’autres requêtes s’est produites avant l’ouverture de DevTools, ces demandes ne sont pas comptabilisées.  

> ##### Figure 29  
> La taille de téléchargement totale des requêtes  
> ! [Longueur totale du téléchargement de demandes] [ImageTotalSize]  

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

> ##### Figure 30  
> Trace de pile aboutissant à une demande de ressources  
> ! [Trace de pile aboutissant à une demande de ressource] [ImageInitiatorStack]  

### Affichage de la taille de la ressource non compressée   

Activez la case à cocher **utiliser des lignes de requête volumineuses** , puis examinez la valeur inférieure de la colonne **taille** .  

> ##### Figure 31  
> Voici un exemple de ressources non compressées \ (la taille du `jquery-3.3.1.min.js` fichier qui a été envoyée par le biais du réseau était `29.9 KB` alors la taille du fichier non compressé `84.9 KB` ).  
> ! [Exemple de ressources non comprimées] [ImageUncompressedResources]  

## Exporter les données de requête   

### Enregistrer toutes les demandes réseau dans un fichier QAR   

Pour enregistrer toutes les requêtes réseau sur un fichier QAR:  

1.  Cliquez avec le bouton droit sur une requête dans la table demandes.  
1.  Sélectionnez **Save As QAR with content**.  DevTools enregistre toutes les demandes qui se sont produites depuis que vous avez ouvert DevTools sur le fichier.  Il n’est pas possible de filtrer les demandes ou de n’enregistrer qu’une seule demande.  

Lorsque vous enregistrez un fichier QAR, vous pouvez l’importer de nouveau dans DevTools pour analyse.  Il suffit de glisser-déplacer le fichier QAR dans la table demandes.  
<!--See also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

> ##### Figure 32  
> Sélection de l’option Enregistrer sous le contenu de votre fichier  
> ! [Sélection de l’option Enregistrer sous le contenu d’un fichier [ImageSaveAsHAR]  

### Copier une ou plusieurs demandes dans le presse-papiers   

Dans la colonne **nom** de la table demandes, cliquez avec le bouton droit sur une requête, survolez la **copie**, puis sélectionnez l’une des options suivantes:  

*   **Copier l’adresse du lien**.  Copiez l’URL de la requête dans le presse-papiers.  
*   **Copier la réponse**.  Copiez le corps de la réponse dans le presse-papiers.  
*   **Copy As FETCH**.  
*   **Copier comme courbe**.  Copiez la demande en tant que commande en forme de boucle.  
*   **Copy All As FETCH**.  
*   **Tout copier comme courbe**.  Copiez toutes les demandes comme une chaîne de commandes bouclé.  
*   **Copy All As QAR**.  Copiez toutes les demandes en tant que données QAR.  

> ##### Figure 33  
> Sélection de l’option copier la réponse  
> ! [Sélection de l’option copier la réponse] [ImageCopyResponse]  

## Modifier la disposition du panneau réseau  

Vous pouvez développer ou réduire des sections de l’interface utilisateur du panneau réseau pour cibler les informations importantes.  

### Masquer le volet filtres   

Par défaut, DevTools affiche le **volet filtres**.  
Sélectionnez **Filter** ![ filtre ][ImageFilterIcon] de filtre pour le masquer.  

> ##### Figure 34  
> Bouton Masquer les filtres  
> ! [Bouton Masquer les filtres] [ImageHideFiltersButton]  

### Utiliser des lignes de requête volumineuses   

Utilisez des lignes de grande taille si vous voulez plus d’espace dans votre tableau de requêtes réseau.  Certaines colonnes fournissent également quelques informations supplémentaires sur l’utilisation de lignes de grande taille.  Par exemple, la valeur la plus en bas de la colonne **taille** correspond à la taille de requête non compressée.  

> ##### Figure 35  
> Exemple de longues lignes de requête dans le volet requêtes  
> ! [Exemple de grandes lignes de requête dans le volet requêtes] [ImageLargeRequestRows]  

Activez la case à cocher **utiliser des lignes de requête volumineuses** pour activer les lignes de grande taille.  

> ##### Figure 36  
> Case à cocher grandes lignes de requête  
> ! [Case à cocher grandes lignes de requête] [ImageLargeRequestRowsCheckbox]  

### Masquer le volet vue d’ensemble   

Par défaut, DevTools affiche le **volet vue d’ensemble**.  
Désélectionnez la case à cocher **afficher la vue d’ensemble** pour la masquer.  

> ##### Figure 37  
> Case à cocher Afficher la vue d’ensemble  
> ! [La case à cocher Afficher la présentation] [ImageHideOverviewCheckbox]  

<!-->   -->  

  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-requests-icon.msft.png  
[ImageFilterIcon]: /microsoft-edge/devtools-guide-chromium/media/filter-icon.msft.png  
[ImageHideIcon]: /microsoft-edge/devtools-guide-chromium/media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: /microsoft-edge/devtools-guide-chromium/media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: /microsoft-edge/devtools-guide-chromium/media/record-on-icon.msft.png  

[ImageNetworkPanel]: /microsoft-edge/devtools-guide-chromium/media/network-network-panel.msft.png "Figure 1: panneau réseau"  
[ImageClearButton]: /microsoft-edge/devtools-guide-chromium/media/network-network-clear-button.msft.png "Figure 2: bouton Effacer"  
[ImagePreserveLogCheckBox]: /microsoft-edge/devtools-guide-chromium/media/network-network-preserve-log.msft.png "Figure 3: case à cocher conserver le journal"  
[ImageScreenshotHover]: /microsoft-edge/devtools-guide-chromium/media/network-network-screenshot-hover.msft.png "Figure 4: survol d’une capture d’écran"  
<!--[ImageReplayXHR]: /microsoft-edge/devtools-guide-chromium/media/network-replay-xhr.msft.png "Old Figure 5: Selecting Replay XHR"  -->  
[ImageDisableCacheCheckBox]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Disable-cache-CheckBox.msft.png "figure 5: case à cocher Désactiver le cache"  
[ImageClearBrowserCache]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Clear-Browser-cache.msft.png "figure 6: sélectionner vider le cache du navigateur"  
[ImageOfflineDropdown]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Offline-DropDown.msft.png "figure 7: menu déroulant hors ligne"  
[ImageNetworkThrottlingMenu]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-throttling-menu.msft.png "figure 8: menu de limitation du réseau"  
[ImageClearBrowserCookies]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Clear-Browser-cookies.msft.png "figure 9: sélectionnez Effacer les cookies du navigateur"  
[ImageFilterTextBox]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Filters-TextBox.msft.png "figure 10: zone de texte filtres"  
[ImageMultiTypeFilter]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-type-Filters.msft.png "figure 11: utilisation des filtres de type pour afficher JS, CSS et les ressources de documents"  
[ImageOverviewFilter]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Overview-Filter.msft.png "figure 12: filtrage des requêtes inactives depuis 300M"  
[ImageHideDataURLsCheckBox]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Hide-Data-URLs.msft.png "figure 13: cases à cocher Masquer les URL de données"  
[ImageWaterfallTotalDuration]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Waterfall-Total-Duration.msft.png "figure 14: trier les cascade en fonction de la durée totale"  
[ImageRequestsTable]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-table.msft.png "figure 15: la table demandes"  
[ImageRequestsTableAddColumn]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Add-Column.msft.png "figure 16: ajout d’une colonne dans la table demandes"  
[ImageRequestsTableCustomColumn]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Add-Custom.msft.png "figure 17: ajout d’une colonne personnalisée dans la table demandes"  
[ImageRequestsTableWaterfallColumn]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Waterfall.msft.png "figure 18: colonne cascade du volet demandes"  
[ImagePreview]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-preview.msft.png "figure 19: onglet Aperçu"  
<!--[ImageFrames]: /microsoft-edge/devtools-guide-chromium/media/network-frames.msft.png "Old Figure 20: The Frames tab"  -->  
[ImageResponse]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-Response.msft.png "figure 20: onglet réponse"  
[ImageHeaders]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Resources-headers.msft.png "figure 21: onglet en-têtes"  
[ImageQueryStringParameters]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-headers-query-string-Parameters.msft.png "figure 22: section paramètres de chaînes de requête"  
[ImageCookies]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-cookies.msft.png "figure 23: onglet cookies"  
[ImageTiming]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-timing.msft.png "figure 24: onglet Minutage"  
[ImageWaterfallHover]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-Waterfall-Hover.msft.png "figure 25: prévisualisation de l’intervalle de temps d’une requête"  
[ImageRequestInitiatorsDependencies]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-Initiators-Dependencies.msft.png "figure 26: affichage des déclencheurs et dépendances d’une requête"  
[ImageNetworkPanelDOMContentLoadedLoadEvents]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Load-Events.msft.png "figure 27: emplacements des événements DOMContentLoaded et Load sur le panneau réseau"  
[ImageTotalRequests]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-total-requests.msft.png "figure 28: le nombre total de demandes depuis DevTools a été ouverte"  
[ImageTotalSize]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-total-download-size.msft.png "figure 29: taille totale du téléchargement de demandes"  
[ImageInitiatorStack]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Initiator-Stack.msft.png "figure 30: trace de pile aboutissant à une demande de ressource"  
[ImageUncompressedResources]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Uncompressed-compare.msft.png "figure 31: exemple de ressources non comprimées"  
[ImageSaveAsHAR]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Save-har-content.msft.png "figure 32: sélectionnez Enregistrer sous le contenu  
[ImageCopyResponse]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Copy-Response.msft.png "figure 33: sélection de l’option copier la réponse"  
[ImageHideFiltersButton]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-Hide-Filters-Button.msft.png "figure 34: bouton Masquer les filtres"  
[ImageLargeRequestRows]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-large-Request-Rows.msft.png "figure 35: exemple de grandes lignes de requête dans le volet demandes"  
[ImageLargeRequestRowsCheckbox]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-use-large-Request-Rows-on.msft.png "figure 36: case à cocher grandes lignes de requête"  
[ImageHideOverviewCheckbox]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Show-Overview-OFF.msft.png "figure 37: case à cocher Masquer la vue d’ensemble"  

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
