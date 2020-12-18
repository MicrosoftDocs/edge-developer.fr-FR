---
description: Utiliser le volet réseau pour contrôler les demandes de ressources de pages et les profils
title: DevTools-réseau
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, réseau, temps de chargement, http, HTTPS, cache du navigateur, QAR
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 261226c7210d978f11290816c81355bb0142dee9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233268"
---
# Network

Utilisez le panneau **réseau** pour contrôler, inspecter et profiler les demandes et réponses envoyées sur le réseau. Avec ce service, vous pouvez:

 - [Parcourir un enregistrement de toutes les demandes de ressources](#network-summary) effectuées par la page
 - [Mesurer le temps de chargement de votre site pour le](#summary-bar) nouveau et retourner des utilisateurs 
 - [Inspecter les en-têtes, les corps des messages, les paramètres et les cookies](#request-details) échangés entre votre page et le réseau
 - [Identifier les événements réseau entraînant des goulets d’étranglement](#timings) au moment du chargement de votre site

![Panneau de configuration du réseau Microsoft Edge DevTools](./media/network.png)

## Network Summary

Lorsque vous ouvrez DevTools, le profilage réseau est activé par défaut. Tout le trafic réseau de votre onglet de navigateur actif est enregistré dans la liste Résumé du réseau, même lorsque vous travaillez dans un autre panneau de DevTools que sur le *réseau*.

![Indicateur de profil de réseau en cours](./media/network_profile_indicator.png)

### ToolBar

La barre d’outils fournit des contrôles pour le profilage et le filtrage de l’activité réseau de votre page. 

![Barre d’outils Network Profiler](./media/network_toolbar.png)

1. **Démarrer/arrêter la session de profil**: par défaut, le profilage réseau est activé, et le trafic réseau sera enregistré dans la liste de la liste du [**testeur réseau**](#network-request-list) . Vous pouvez désactiver la capture réseau à l’aide du bouton **Stop** ( `Ctrl+E` ).

2. **Exporter au format QAR**: vous pouvez enregistrer la session de profilage réseau actuelle ( `Ctrl+S` ) en tant que fichier d' [Archive http](https://dvcs.w3.org/hg/webperf/raw-file/tip/specs/HAR/Overview.html) au format JSON. 

3. **Filtre de type de contenu**: filtrez la liste de demandes réseau par demandes de contenu spécifiques (*documents, feuilles de style, images, scripts, médias, polices, XHR, etc*.). Par défaut, tous les types de contenus apparaissent.

4. **Recherchez**: filtre ( `Ctrl+F` ) la liste de demandes réseau par nom d’entrée (chemins de ressources) contenant une chaîne de recherche spécifiée.

5. **Toujours actualiser du serveur**: en appuyant sur ce bouton, vous forcez le chargement des ressources de page à partir du réseau plutôt que dans le cache du navigateur. Vous pouvez actualiser la page à partir du réseau une seule fois en appuyant sur `Ctrl+F5` .

6. **Ignorer le travailleur de service pour toutes les requêtes réseau**: désactiver les travailleurs de services enregistrés en tant que proxys réseau. 

7. Boutons clairs

   - **Vider le cache**: supprime toutes les ressources stockées dans le cache du navigateur (et émule une première utilisation du chargement de la page).
   - **Effacer les cookies**: supprime tous les cookies pour le domaine donné (et émule une première utilisation du site).
   - **Effacer les entrées sur**la navigation: le trafic enregistré est vidé lors de la navigation entre les pages. Cette option est activée par défaut.
   - **Effacer une session**: efface toutes les entrées de requête réseau dans la liste **Résumé du réseau** .

### Liste de demande réseau

Tout le trafic réseau est enregistré dans une liste (jusqu’à ce qu’il soit effacé au moment de la navigation, supprimé manuellement ou DevTools est fermé). Cliquez sur une entrée pour ouvrir une [vue plus détaillée de celle](#request-details)-ci.

![Liste de demande réseau](./media/network_request_list.png)

La liste de demandes réseau contient les informations suivantes: 

Colonne | Description 
:------------ | :------------- 
**Name** | Nom et chemin d’URL de la requête
**Protocole** |  Type de protocole pour la requête (par exemple *, HTTPS, http/2*)
**Méthode** |    [Méthode http](https://developer.mozilla.org/docs/Web/HTTP/Methods) utilisée pour la requête
**Résultat** |    Code d' [État de réponse http](https://developer.mozilla.org/docs/Web/HTTP/Status)
**Type de contenu** |  Type de média requis ([type MIME](https://en.wikipedia.org/wiki/Media_type))
**Reçu** | Taille de la réponse telle qu’elle est fournie par le serveur (non calculée pour les réponses mises en cache)
**Heure** |  Temps de chargement de la réponse du serveur (non calculé pour les réponses mises en cache)
**Initiateur** | Sous-système responsable de l’initiation de la requête (par exemple *, analyseur, redirection, script, etc*.)
**Chronologie** | Chronologie visuelle des événements réseau de la requête (par exemple *, bloqué, RéRésolutions (DNS), connexion (TCP), SSL, envoi, attente (TTFB), téléchargement*). Pointez sur le graphique pour obtenir une répartition plus granulaire des [minutages réseau](#timings).

### Barre de synthèse

La barre située dans la partie inférieure du panneau **réseau** résume le nombre total d’erreurs réseau http, de demandes, de transfert de données et de temps de chargement au cours de la session de profilage réseau (par exemple, depuis l’ouverture et l’enregistrement du trafic réseau).

![Barre de synthèse du réseau](./media/network_summary_bar.png)

Le **temps écoulé** correspond au temps écoulé entre le début de la session de profilage et au téléchargement de la dernière ressource à partir du réseau. Les ressources récupérées à partir du cache du navigateur n’allouer pas le temps à ce numéro. 

Le **temps de chargement DOM** correspond au temps écoulé entre le début de la session de profilage et au moment où l’événement [DOMContentLoaded](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded) a été déclenché pour indiquer que la structure du document de page a été chargée et analysée (bien qu’il n’y ait pas nécessairement des feuilles de style, des images ou des sous-blocs).

Temps de chargement de la **page** indique le temps entre le début de la session de profilage et le moment où l’événement de [chargement](https://developer.mozilla.org/docs/Web/Events/load) a été déclenché pour indiquer que le document de la page (et toutes ses ressources) a été entièrement chargé.

## Demander des détails

Cliquer sur une entrée de la liste [**Résumé du réseau**](#network-summary) permet d’ouvrir le volet d’informations sur la [**demande**](#request-details) en incluant des informations supplémentaires dans chacun des onglets suivants.

![Volet Détails de la demande réseau](./media/network_request_details.png)

### En-têtes
Affiche les [en-têtes http](https://developer.mozilla.org/docs/Web/HTTP/Headers) envoyés et reçus du serveur. Cliquez avec le bouton droit sur n’importe quelle entrée d’en-tête pour la copier ( `Ctrl+C` ) dans le presse-papiers. Vous pouvez également sélectionner plusieurs entrées en maintenant la touche enfoncée `Shift` ou en sélectionnant tout ( `Ctrl+A` ).

### Body
Affiche les données du corps (le cas échéant) des charges utiles de requête et de réponse.

Le contenu d’image est affiché avec les dimensions et les données de taille.

Le contenu du texte s’affiche dans un éditeur (lecture seule) avec des options pour mettre en forme le contenu **minified avec le** renvoi à la ligne à l’aide de la fonction de **Retour à la ligne**

![Onglet corps du volet de détails de la requête](./media/network_details_body.png)

### Parameters
Affiche les paramètres de chaîne de requête pour les demandes GET. Lorsque les paramètres des demandes POST sont envoyés dans les en-têtes, les demandes GET incluent celles-ci dans l’URL. Ils sont répartis ici pour faciliter la lecture.

Cliquez avec le bouton droit sur une ligne pour la copier ( `Ctrl+C` ) dans le presse-papiers. Vous pouvez également sélectionner plusieurs entrées en maintenant la touche enfoncée `Shift` ou en sélectionnant tout ( `Ctrl+A` ).

### Cookies
Affiche les cookies envoyés ou reçus en tant que paires clé/valeur.

Cliquez avec le bouton droit sur une ligne pour la copier ( `Ctrl+C` ) dans le presse-papiers. Vous pouvez également sélectionner plusieurs entrées en maintenant la touche enfoncée `Shift` ou en sélectionnant tout ( `Ctrl+A` ).

Vous pouvez effacer les cookies stockés pour le domaine donné à partir de la [barre d’outils](#network-summary) (bouton**effacer les cookies** ). 

### Minutage

L’onglet **minutages** fournit une chronologie des événements réseau impliqués dans le chargement de la ressource sélectionnée. Il s’agit de la même façon que les informations figurant dans la colonne de *chronologie* de la [liste de demandes réseau](#network-request-list), mais inclut également les événements qui conduisent à la demande envoyée sur le réseau, comme le temps passé en attente (*bloqué*) dans la file d’attente de demandes, la résolution DNS et l’établissement de la connexion TCP. 

![Onglet minutages du volet Détails de la requête](./media/network_details_timings.png)

Les redirections vers/depuis d’autres ressources sont notées, et le fait de cliquer sur le lien définira le focus sur cette ressource dans le volet des détails de la [demande](#request details) réseau.

Les ressources chargées à partir du cache ne sont pas affectées par le *temps* de latence du réseau.

![Ressource redirigée chargée à partir du cache](./media/network_details_timings_cache_redirect.png)

Voici les différents événements réseau qui peuvent apparaître pour une ressource donnée, dans l’ordre chronologique:

#### Bloquée

Temps passé à attendre une connexion réseau disponible dans la file d’attente de demandes. Pour HTTP 1.0/1.1, Microsoft Edge autorise un maximum de six (6) connexions TCP simultanées par nom d’hôte. 

#### Résolution (DNS)

Temps passé à Rechercher l’adresse IP du nom d’hôte de la ressource dans le DNS ([Domain Name System](https://en.wikipedia.org/wiki/Domain_Name_System)).

#### Connexion (TCP)

Temps passé à établir la connexion TCP ([Transmission Control Protocol](https://en.wikipedia.org/wiki/Transmission_Control_Protocol)).

#### TECHNOLOGIE

Temps passé à négocier une connexion SSL ([Secure Sockets Layer](https://en.wikipedia.org/wiki/Transport_Layer_Security)) avec le [serveur proxy](https://en.wikipedia.org/wiki/Proxy_server) de l’hôte.

#### Émetteur

Temps passé à envoyer la demande de ressource.

#### En attente (TTFB)

Temps passé à patienter avant le premier octet de la réponse du serveur hôte («durée au premier octet» ou *TTFB*).

#### Entam

Temps passé à lire la réponse à partir du serveur.

## Raccourcis

| Action                         | Raccourci     |
|:-------------------------------|:-------------|
| Démarrer/arrêter la session de profilage | `Ctrl` + `E` |
| Exporter au format QAR                  | `Ctrl` + `S` |
| Rechercher                           | `Ctrl` + `F` |
| Copy                           | `Ctrl` + `C` |

## Problèmes connus

### Échec du démarrage de l’agent de collection de réseaux.

Si vous voyez le message d’erreur suivant: **l’agent de collection de réseaux n’a pas réussi à démarrer** dans l’outil réseau, procédez comme suit pour contourner le problème.

1. Appuyez sur `Windows Key`  +  `R` .

2. Dans la boîte de dialogue Exécuter, entrez **services. msc**.
![problèmes connus-1](./media/known_issues_1.PNG)

3. Recherchez le **service collecteur standard de Diagnostics Microsoft (R)** et cliquez dessus avec le bouton droit.
![problèmes connus-2](./media/known_issues_2.PNG)

4. Redémarrez le **service de collecteur standard de Diagnostics Microsoft (R)**.
![problèmes connus-3](./media/known_issues_3.PNG)

5. Fermez les outils de développement Microsoft Edge et l’onglet. Ouvrez un nouvel onglet, accédez à votre page, puis appuyez sur `F12` .

6. Vous devez maintenant voir un badge lire en regard du **réseau** et les requêtes réseau pour votre page Web.
![problèmes connus-4](./media/known_issues_4-network.PNG)

Vous rencontrez encore des problèmes? Envoyez-nous vos commentaires à l’aide de l’icône d' **envoi de commentaires** ! 

![problèmes connus-5](./media/known_issues_5.PNG)

### L’agent de collection réseau n’a pas pu s’arrêter.

Si vous voyez le message d’erreur suivant: **l’agent de collection de réseaux n’a pas pu s’arrêter** dans l’outil réseau, procédez comme suit pour contourner le problème.

1. Appuyez sur `Windows Key`  +  `R` .

2. Dans la boîte de dialogue Exécuter, entrez **services. msc**.
![problèmes connus-1](./media/known_issues_1.PNG)

3. Recherchez le **service collecteur standard de Diagnostics Microsoft (R)** et cliquez dessus avec le bouton droit.
![problèmes connus-2](./media/known_issues_2.PNG)

4. Redémarrez le **service de collecteur standard de Diagnostics Microsoft (R)**.
![problèmes connus-3](./media/known_issues_3.PNG)

5. Fermez les outils de développement Microsoft Edge et l’onglet. Ouvrez un nouvel onglet, accédez à votre page, puis appuyez sur `F12` .

6. Vous devez maintenant voir un badge lire en regard du **réseau** et les requêtes réseau pour votre page Web.
![problèmes connus-4](./media/known_issues_4-network.PNG)

Vous rencontrez encore des problèmes? Envoyez-nous vos commentaires à l’aide de l’icône d' **envoi de commentaires** ! 

![problèmes connus-5](./media/known_issues_5.PNG)
