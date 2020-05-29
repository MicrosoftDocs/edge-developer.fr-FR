---
description: Utiliser le volet réseau pour contrôler les demandes de ressources de pages et les profils
title: DevTools-réseau
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, réseau, temps de chargement, http, HTTPS, cache du navigateur, QAR
ms.custom: seodec18
ms.openlocfilehash: 0b190f5163f9b7a9f9920877a94577177053e4f6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565530"
---
# <span data-ttu-id="b798b-104">Réseau</span><span class="sxs-lookup"><span data-stu-id="b798b-104">Network</span></span>

<span data-ttu-id="b798b-105">Utilisez le panneau **réseau** pour contrôler, inspecter et profiler les demandes et réponses envoyées sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="b798b-105">Use the **Network** panel to monitor, inspect and profile the requests and responses sent over the wire.</span></span> <span data-ttu-id="b798b-106">Avec ce service, vous pouvez:</span><span class="sxs-lookup"><span data-stu-id="b798b-106">With it, you can:</span></span>

 - <span data-ttu-id="b798b-107">[Parcourir un enregistrement de toutes les demandes de ressources](#network-summary) effectuées par la page</span><span class="sxs-lookup"><span data-stu-id="b798b-107">[Browse a record of all the resource requests](#network-summary) made by the page</span></span>
 - <span data-ttu-id="b798b-108">[Mesurer le temps de chargement de votre site pour le](#summary-bar) nouveau et retourner des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="b798b-108">[Measure the load time of your site](#summary-bar) for new and returning users</span></span> 
 - <span data-ttu-id="b798b-109">[Inspecter les en-têtes, les corps des messages, les paramètres et les cookies](#request-details) échangés entre votre page et le réseau</span><span class="sxs-lookup"><span data-stu-id="b798b-109">[Inspect the headers, message bodies, parameters, and cookies](#request-details) exchanged between your page and the network</span></span>
 - <span data-ttu-id="b798b-110">[Identifier les événements réseau entraînant des goulets d’étranglement](#timings) au moment du chargement de votre site</span><span class="sxs-lookup"><span data-stu-id="b798b-110">[Identify the network events causing bottlenecks](#timings) in the load time of your site</span></span>

![Panneau de configuration du réseau Microsoft Edge DevTools](./media/network.png)

## <span data-ttu-id="b798b-112">Network Summary</span><span class="sxs-lookup"><span data-stu-id="b798b-112">Network summary</span></span>

<span data-ttu-id="b798b-113">Lorsque vous ouvrez DevTools, le profilage réseau est activé par défaut.</span><span class="sxs-lookup"><span data-stu-id="b798b-113">When you open  DevTools, network profiling is turned on by default.</span></span> <span data-ttu-id="b798b-114">Tout le trafic réseau de votre onglet de navigateur actif est enregistré dans la liste Résumé du réseau, même lorsque vous travaillez dans un autre panneau de DevTools que sur le *réseau*.</span><span class="sxs-lookup"><span data-stu-id="b798b-114">All the network traffic from your active browser tab is recorded in the network summary list, even while you are working in a different  DevTools panel than *Network*.</span></span>

![Indicateur de profil de réseau en cours](./media/network_profile_indicator.png)

### <span data-ttu-id="b798b-116">ToolBar</span><span class="sxs-lookup"><span data-stu-id="b798b-116">Toolbar</span></span>

<span data-ttu-id="b798b-117">La barre d’outils fournit des contrôles pour le profilage et le filtrage de l’activité réseau de votre page.</span><span class="sxs-lookup"><span data-stu-id="b798b-117">The toolbar provides controls for profiling and filtering the network activity of your page.</span></span> 

![Barre d’outils Network Profiler](./media/network_toolbar.png)

1. <span data-ttu-id="b798b-119">**Démarrer/arrêter la session de profil**: par défaut, le profilage réseau est activé, et le trafic réseau sera enregistré dans la liste de la liste du [**testeur réseau**](#network-request-list) .</span><span class="sxs-lookup"><span data-stu-id="b798b-119">**Start / Stop profiling session**: By default, network profiling is turned on, and network traffic will be logged in the [**Network profiler**](#network-request-list) list.</span></span> <span data-ttu-id="b798b-120">Vous pouvez désactiver la capture réseau à l’aide du bouton **Stop** ( `Ctrl+E` ).</span><span class="sxs-lookup"><span data-stu-id="b798b-120">You can turn off network capture with the **Stop** (`Ctrl+E`) button.</span></span>

2. <span data-ttu-id="b798b-121">**Exporter au format QAR**: vous pouvez enregistrer la session de profilage réseau actuelle ( `Ctrl+S` ) en tant que fichier d' [Archive http](https://dvcs.w3.org/hg/webperf/raw-file/tip/specs/HAR/Overview.html) au format JSON.</span><span class="sxs-lookup"><span data-stu-id="b798b-121">**Export as HAR**: You can save the current network profiling session (`Ctrl+S`) as a JSON-formatted [HTTP Archive (HAR)](https://dvcs.w3.org/hg/webperf/raw-file/tip/specs/HAR/Overview.html) file.</span></span> 

3. <span data-ttu-id="b798b-122">**Filtre de type de contenu**: filtrez la liste de demandes réseau par demandes de contenu spécifiques (*documents, feuilles de style, images, scripts, médias, polices, XHR, etc*.).</span><span class="sxs-lookup"><span data-stu-id="b798b-122">**Content type filter**: Filter the network request list by specific content requests (*Documents, Style sheets, Images, Scripts, Media, Fonts, XHR, Other*).</span></span> <span data-ttu-id="b798b-123">Par défaut, tous les types de contenus apparaissent.</span><span class="sxs-lookup"><span data-stu-id="b798b-123">By default all content types are shown.</span></span>

4. <span data-ttu-id="b798b-124">**Recherchez**: filtre ( `Ctrl+F` ) la liste de demandes réseau par nom d’entrée (chemins de ressources) contenant une chaîne de recherche spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b798b-124">**Find**: Filter (`Ctrl+F`) the network request list by entry names (resource paths) containing a specified search string.</span></span>

5. <span data-ttu-id="b798b-125">**Toujours actualiser du serveur**: en appuyant sur ce bouton, vous forcez le chargement des ressources de page à partir du réseau plutôt que dans le cache du navigateur.</span><span class="sxs-lookup"><span data-stu-id="b798b-125">**Always refresh from server**: Depressing this button will force page resources to load from the network rather than the browser cache.</span></span> <span data-ttu-id="b798b-126">Vous pouvez actualiser la page à partir du réseau une seule fois en appuyant sur `Ctrl+F5` .</span><span class="sxs-lookup"><span data-stu-id="b798b-126">You can refresh the page from  network a single time by pressing `Ctrl+F5`.</span></span>

6. <span data-ttu-id="b798b-127">**Ignorer le travailleur de service pour toutes les requêtes réseau**: désactiver les travailleurs de services enregistrés en tant que proxys réseau.</span><span class="sxs-lookup"><span data-stu-id="b798b-127">**Bypass Service Worker for all network requests**: Disable your registered service workers as network proxies.</span></span> 

7. <span data-ttu-id="b798b-128">Boutons clairs</span><span class="sxs-lookup"><span data-stu-id="b798b-128">Clear buttons</span></span>

   - <span data-ttu-id="b798b-129">**Vider le cache**: supprime toutes les ressources stockées dans le cache du navigateur (et émule une première utilisation du chargement de la page).</span><span class="sxs-lookup"><span data-stu-id="b798b-129">**Clear cache**: Removes all resources stored in the browser cache (and emulates a first-time experience loading the page).</span></span>
   - <span data-ttu-id="b798b-130">**Effacer les cookies**: supprime tous les cookies pour le domaine donné (et émule une première utilisation du site).</span><span class="sxs-lookup"><span data-stu-id="b798b-130">**Clear cookies**: Removes all cookies for the given domain (and emulates a first-time experience of the site).</span></span>
   - <span data-ttu-id="b798b-131">**Effacer les entrées sur**la navigation: le trafic enregistré est vidé lors de la navigation entre les pages.</span><span class="sxs-lookup"><span data-stu-id="b798b-131">**Clear entries on navigate**: Recorded traffic is cleared upon page navigation.</span></span> <span data-ttu-id="b798b-132">Cette option est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="b798b-132">This is turned on by default.</span></span>
   - <span data-ttu-id="b798b-133">**Effacer une session**: efface toutes les entrées de requête réseau dans la liste **Résumé du réseau** .</span><span class="sxs-lookup"><span data-stu-id="b798b-133">**Clear session**: Clears all network request entries from the **Network summary** list.</span></span>

### <span data-ttu-id="b798b-134">Liste de demande réseau</span><span class="sxs-lookup"><span data-stu-id="b798b-134">Network request list</span></span>

<span data-ttu-id="b798b-135">Tout le trafic réseau est enregistré dans une liste (jusqu’à ce qu’il soit effacé au moment de la navigation, supprimé manuellement ou DevTools est fermé).</span><span class="sxs-lookup"><span data-stu-id="b798b-135">All network traffic is recorded to a list (until cleared upon navigation, manually cleared, or  DevTools are closed).</span></span> <span data-ttu-id="b798b-136">Cliquez sur une entrée pour ouvrir une [vue plus détaillée de celle](#request-details)-ci.</span><span class="sxs-lookup"><span data-stu-id="b798b-136">Clicking on any entry will open a more [detailed view of the request](#request-details).</span></span>

![Liste de demande réseau](./media/network_request_list.png)

<span data-ttu-id="b798b-138">La liste de demandes réseau contient les informations suivantes:</span><span class="sxs-lookup"><span data-stu-id="b798b-138">The network request list includes the following info:</span></span> 

<span data-ttu-id="b798b-139">Colonne</span><span class="sxs-lookup"><span data-stu-id="b798b-139">Column</span></span> | <span data-ttu-id="b798b-140">Description</span><span class="sxs-lookup"><span data-stu-id="b798b-140">Description</span></span> 
:------------ | :------------- 
**<span data-ttu-id="b798b-141">Name</span><span class="sxs-lookup"><span data-stu-id="b798b-141">Name</span></span>** | <span data-ttu-id="b798b-142">Nom et chemin d’URL de la requête</span><span class="sxs-lookup"><span data-stu-id="b798b-142">Name and URL path of the request</span></span>
**<span data-ttu-id="b798b-143">Protocole</span><span class="sxs-lookup"><span data-stu-id="b798b-143">Protocol</span></span>** |  <span data-ttu-id="b798b-144">Type de protocole pour la requête (par exemple *, HTTPS, http/2*)</span><span class="sxs-lookup"><span data-stu-id="b798b-144">Type of protocol for the request (such as *HTTPS, HTTP/2*)</span></span>
**<span data-ttu-id="b798b-145">Méthode</span><span class="sxs-lookup"><span data-stu-id="b798b-145">Method</span></span>** |    <span data-ttu-id="b798b-146">[Méthode http](https://developer.mozilla.org/docs/Web/HTTP/Methods) utilisée pour la requête</span><span class="sxs-lookup"><span data-stu-id="b798b-146">[HTTP method](https://developer.mozilla.org/docs/Web/HTTP/Methods) used for the request</span></span>
**<span data-ttu-id="b798b-147">Résultat</span><span class="sxs-lookup"><span data-stu-id="b798b-147">Result</span></span>** |    <span data-ttu-id="b798b-148">Code d' [État de réponse http](https://developer.mozilla.org/docs/Web/HTTP/Status)</span><span class="sxs-lookup"><span data-stu-id="b798b-148">[HTTP response status](https://developer.mozilla.org/docs/Web/HTTP/Status)  code</span></span>
**<span data-ttu-id="b798b-149">Type de contenu</span><span class="sxs-lookup"><span data-stu-id="b798b-149">Content type</span></span>** |  <span data-ttu-id="b798b-150">Type de média requis ([type MIME](https://en.wikipedia.org/wiki/Media_type))</span><span class="sxs-lookup"><span data-stu-id="b798b-150">Type of media requested ([MIME type](https://en.wikipedia.org/wiki/Media_type))</span></span>
**<span data-ttu-id="b798b-151">Reçu</span><span class="sxs-lookup"><span data-stu-id="b798b-151">Received</span></span>** | <span data-ttu-id="b798b-152">Taille de la réponse telle qu’elle est fournie par le serveur (non calculée pour les réponses mises en cache)</span><span class="sxs-lookup"><span data-stu-id="b798b-152">Size of the response as delivered by the server (not calculated for cached responses)</span></span>
**<span data-ttu-id="b798b-153">Heure</span><span class="sxs-lookup"><span data-stu-id="b798b-153">Time</span></span>** |  <span data-ttu-id="b798b-154">Temps de chargement de la réponse du serveur (non calculé pour les réponses mises en cache)</span><span class="sxs-lookup"><span data-stu-id="b798b-154">Time to load the server response (not calculated for cached responses)</span></span>
**<span data-ttu-id="b798b-155">Initiateur</span><span class="sxs-lookup"><span data-stu-id="b798b-155">Initiator</span></span>** | <span data-ttu-id="b798b-156">Sous-système responsable de l’initiation de la requête (par exemple *, analyseur, redirection, script, etc*.)</span><span class="sxs-lookup"><span data-stu-id="b798b-156">Subsystem responsible for initiating the request (such as *Parser, Redirect, Script, Other*)</span></span>
**<span data-ttu-id="b798b-157">Chronologie</span><span class="sxs-lookup"><span data-stu-id="b798b-157">Timeline</span></span>** | <span data-ttu-id="b798b-158">Chronologie visuelle des événements réseau de la requête (par exemple *, bloqué, RéRésolutions (DNS), connexion (TCP), SSL, envoi, attente (TTFB), téléchargement*).</span><span class="sxs-lookup"><span data-stu-id="b798b-158">Visual timeline for the network events of the request (such as *Stalled, Resolving(DNS), Connecting(TCP), SSL, Sending, Waiting(TTFB), Downloading*).</span></span> <span data-ttu-id="b798b-159">Pointez sur le graphique pour obtenir une répartition plus granulaire des [minutages réseau](#timings).</span><span class="sxs-lookup"><span data-stu-id="b798b-159">Hovering over the chart provides the more granular breakdown of network [network timings](#timings)).</span></span>

### <span data-ttu-id="b798b-160">Barre de synthèse</span><span class="sxs-lookup"><span data-stu-id="b798b-160">Summary bar</span></span>

<span data-ttu-id="b798b-161">La barre située dans la partie inférieure du panneau **réseau** résume le nombre total d’erreurs réseau http, de demandes, de transfert de données et de temps de chargement au cours de la session de profilage réseau (par exemple, depuis l’ouverture et l’enregistrement du trafic réseau).</span><span class="sxs-lookup"><span data-stu-id="b798b-161">The bar at the bottom of **Network** panel summarizes the total number of HTTP network errors, requests, data transfered, and load times during the network profiling session (i.e., since  DevTools were opened and recording network traffic).</span></span>

![Barre de synthèse du réseau](./media/network_summary_bar.png)

<span data-ttu-id="b798b-163">Le **temps écoulé** correspond au temps écoulé entre le début de la session de profilage et au téléchargement de la dernière ressource à partir du réseau.</span><span class="sxs-lookup"><span data-stu-id="b798b-163">**Elapsed time** means the time between the start of the profiling session and when the last resource was downloaded from the network.</span></span> <span data-ttu-id="b798b-164">Les ressources récupérées à partir du cache du navigateur n’allouer pas le temps à ce numéro.</span><span class="sxs-lookup"><span data-stu-id="b798b-164">Resources fetched from the browser cache do not accrue time to this number.</span></span> 

<span data-ttu-id="b798b-165">Le **temps de chargement DOM** correspond au temps écoulé entre le début de la session de profilage et au moment où l’événement [DOMContentLoaded](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded) a été déclenché pour indiquer que la structure du document de page a été chargée et analysée (bien qu’il n’y ait pas nécessairement des feuilles de style, des images ou des sous-blocs).</span><span class="sxs-lookup"><span data-stu-id="b798b-165">**DOM load time** means the time between the start of the profiling session and when the [DOMContentLoaded](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded) event was fired to indicate that the structure of the page document has been loaded and parsed (though not necessarily any stylesheets, images or subframes).</span></span>

<span data-ttu-id="b798b-166">Temps de chargement de la **page** indique le temps entre le début de la session de profilage et le moment où l’événement de [chargement](https://developer.mozilla.org/docs/Web/Events/load) a été déclenché pour indiquer que le document de la page (et toutes ses ressources) a été entièrement chargé.</span><span class="sxs-lookup"><span data-stu-id="b798b-166">**Page load time** time means the time between the start of the profiling session and when the [load](https://developer.mozilla.org/docs/Web/Events/load) event was fired to indicate that the page document (and all its resources) has been fully loaded.</span></span>

## <span data-ttu-id="b798b-167">Demander des détails</span><span class="sxs-lookup"><span data-stu-id="b798b-167">Request details</span></span>

<span data-ttu-id="b798b-168">Cliquer sur une entrée de la liste [**Résumé du réseau**](#network-summary) permet d’ouvrir le volet d’informations sur la [**demande**](#request-details) en incluant des informations supplémentaires dans chacun des onglets suivants.</span><span class="sxs-lookup"><span data-stu-id="b798b-168">Clicking on any entry in the [**Network summary**](#network-summary) list will open the [**Request details**](#request-details) pane with further information in each of the following tabs.</span></span>

![Volet Détails de la demande réseau](./media/network_request_details.png)

### <span data-ttu-id="b798b-170">En-têtes</span><span class="sxs-lookup"><span data-stu-id="b798b-170">Headers</span></span>
<span data-ttu-id="b798b-171">Affiche les [en-têtes http](https://developer.mozilla.org/docs/Web/HTTP/Headers) envoyés et reçus du serveur.</span><span class="sxs-lookup"><span data-stu-id="b798b-171">Displays the [HTTP headers](https://developer.mozilla.org/docs/Web/HTTP/Headers) sent to and received from the server.</span></span> <span data-ttu-id="b798b-172">Cliquez avec le bouton droit sur n’importe quelle entrée d’en-tête pour la copier ( `Ctrl+C` ) dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="b798b-172">Right-click on any header entry to copy it (`Ctrl+C`) to the clipboard.</span></span> <span data-ttu-id="b798b-173">Vous pouvez également sélectionner plusieurs entrées en maintenant la touche enfoncée `Shift` ou en sélectionnant tout ( `Ctrl+A` ).</span><span class="sxs-lookup"><span data-stu-id="b798b-173">You can also multi-select entries by holding down the `Shift` key or select all (`Ctrl+A`).</span></span>

### <span data-ttu-id="b798b-174">Body</span><span class="sxs-lookup"><span data-stu-id="b798b-174">Body</span></span>
<span data-ttu-id="b798b-175">Affiche les données du corps (le cas échéant) des charges utiles de requête et de réponse.</span><span class="sxs-lookup"><span data-stu-id="b798b-175">Displays the body data (if available) of the request and response payloads.</span></span>

<span data-ttu-id="b798b-176">Le contenu d’image est affiché avec les dimensions et les données de taille.</span><span class="sxs-lookup"><span data-stu-id="b798b-176">Image content is displayed with dimensions and size data.</span></span>

<span data-ttu-id="b798b-177">Le contenu du texte s’affiche dans un éditeur (lecture seule) avec des options pour mettre en forme le contenu **minified avec le** renvoi à la ligne à l’aide de la fonction de **Retour à la ligne**</span><span class="sxs-lookup"><span data-stu-id="b798b-177">Text content appears in a (read-only) editor with options to format minified content with **Pretty print** and/or **Word wrap** for easier readability.</span></span>

![Onglet corps du volet de détails de la requête](./media/network_details_body.png)

### <span data-ttu-id="b798b-179">Parameters</span><span class="sxs-lookup"><span data-stu-id="b798b-179">Parameters</span></span>
<span data-ttu-id="b798b-180">Affiche les paramètres de chaîne de requête pour les demandes GET.</span><span class="sxs-lookup"><span data-stu-id="b798b-180">Displays query string parameters for GET requests.</span></span> <span data-ttu-id="b798b-181">Lorsque les paramètres des demandes POST sont envoyés dans les en-têtes, les demandes GET incluent celles-ci dans l’URL.</span><span class="sxs-lookup"><span data-stu-id="b798b-181">While the parameters of POST requests are sent in the headers, GET requests include them in the URL.</span></span> <span data-ttu-id="b798b-182">Ils sont répartis ici pour faciliter la lecture.</span><span class="sxs-lookup"><span data-stu-id="b798b-182">They're broken out here for easier reading.</span></span>

<span data-ttu-id="b798b-183">Cliquez avec le bouton droit sur une ligne pour la copier ( `Ctrl+C` ) dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="b798b-183">Right-click on any row to copy it (`Ctrl+C`) to the clipboard.</span></span> <span data-ttu-id="b798b-184">Vous pouvez également sélectionner plusieurs entrées en maintenant la touche enfoncée `Shift` ou en sélectionnant tout ( `Ctrl+A` ).</span><span class="sxs-lookup"><span data-stu-id="b798b-184">You can also multi-select entries by holding down the `Shift` key or select all (`Ctrl+A`).</span></span>

### <span data-ttu-id="b798b-185">Cookies</span><span class="sxs-lookup"><span data-stu-id="b798b-185">Cookies</span></span>
<span data-ttu-id="b798b-186">Affiche les cookies envoyés ou reçus en tant que paires clé/valeur.</span><span class="sxs-lookup"><span data-stu-id="b798b-186">Displays cookies that are sent or received as key/value pairs.</span></span>

<span data-ttu-id="b798b-187">Cliquez avec le bouton droit sur une ligne pour la copier ( `Ctrl+C` ) dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="b798b-187">Right-click on any row to copy it (`Ctrl+C`) to the clipboard.</span></span> <span data-ttu-id="b798b-188">Vous pouvez également sélectionner plusieurs entrées en maintenant la touche enfoncée `Shift` ou en sélectionnant tout ( `Ctrl+A` ).</span><span class="sxs-lookup"><span data-stu-id="b798b-188">You can also multi-select entries by holding down the `Shift` key or select all (`Ctrl+A`).</span></span>

<span data-ttu-id="b798b-189">Vous pouvez effacer les cookies stockés pour le domaine donné à partir de la [barre d’outils](#network-summary) (bouton**effacer les cookies** ).</span><span class="sxs-lookup"><span data-stu-id="b798b-189">You can clear the stored cookies for the given domain from the [Toolbar](#network-summary) (**Clear cookies** button).</span></span> 

### <span data-ttu-id="b798b-190">Minutage</span><span class="sxs-lookup"><span data-stu-id="b798b-190">Timings</span></span>

<span data-ttu-id="b798b-191">L’onglet **minutages** fournit une chronologie des événements réseau impliqués dans le chargement de la ressource sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="b798b-191">The **Timings** tab provides a timeline of network events involved in the loading of the selected resource.</span></span> <span data-ttu-id="b798b-192">Il s’agit de la même façon que les informations figurant dans la colonne de *chronologie* de la [liste de demandes réseau](#network-request-list), mais inclut également les événements qui conduisent à la demande envoyée sur le réseau, comme le temps passé en attente (*bloqué*) dans la file d’attente de demandes, la résolution DNS et l’établissement de la connexion TCP.</span><span class="sxs-lookup"><span data-stu-id="b798b-192">This is similar to the information found in the *Timeline* column of the [Network request list](#network-request-list), but also includes the events leading up to the request being sent over the wire, such as time spent waiting (*Stalled*) in the request queue, DNS resolution, and establishing the TCP connection.</span></span> 

![Onglet minutages du volet Détails de la requête](./media/network_details_timings.png)

<span data-ttu-id="b798b-194">Les redirections vers/depuis d’autres ressources sont notées, et le fait de cliquer sur le lien définira le focus sur cette ressource dans le volet des détails de la [demande](#request details) réseau.</span><span class="sxs-lookup"><span data-stu-id="b798b-194">Redirections to/from other resources are noted, and clicking on the link will set focus to that resource in the network [request details](#request details) pane.</span></span>

<span data-ttu-id="b798b-195">Les ressources chargées à partir du cache ne sont pas affectées par le *temps* de latence du réseau.</span><span class="sxs-lookup"><span data-stu-id="b798b-195">Resouces loaded from the cache are not affected by network latency, so no network *Timings* chart will display.</span></span>

![Ressource redirigée chargée à partir du cache](./media/network_details_timings_cache_redirect.png)

<span data-ttu-id="b798b-197">Voici les différents événements réseau qui peuvent apparaître pour une ressource donnée, dans l’ordre chronologique:</span><span class="sxs-lookup"><span data-stu-id="b798b-197">Here are the different network events you might see for a given resource, in chronological order:</span></span>

#### <span data-ttu-id="b798b-198">Bloquée</span><span class="sxs-lookup"><span data-stu-id="b798b-198">Stalled</span></span>

<span data-ttu-id="b798b-199">Temps passé à attendre une connexion réseau disponible dans la file d’attente de demandes.</span><span class="sxs-lookup"><span data-stu-id="b798b-199">Time spent waiting for an available network connection in the request queue.</span></span> <span data-ttu-id="b798b-200">Pour HTTP 1.0/1.1, Microsoft Edge autorise un maximum de six (6) connexions TCP simultanées par nom d’hôte.</span><span class="sxs-lookup"><span data-stu-id="b798b-200">For HTTP 1.0/1.1, Microsoft Edge allows a maximum of six (6) simultaneous TCP connections per hostname.</span></span> 

#### <span data-ttu-id="b798b-201">Résolution (DNS)</span><span class="sxs-lookup"><span data-stu-id="b798b-201">Resolving (DNS)</span></span>

<span data-ttu-id="b798b-202">Temps passé à Rechercher l’adresse IP du nom d’hôte de la ressource dans le DNS ([Domain Name System](https://en.wikipedia.org/wiki/Domain_Name_System)).</span><span class="sxs-lookup"><span data-stu-id="b798b-202">Time spent looking up the IP address for the hostname of the resource in the DNS ([Domain Name System](https://en.wikipedia.org/wiki/Domain_Name_System)).</span></span>

#### <span data-ttu-id="b798b-203">Connexion (TCP)</span><span class="sxs-lookup"><span data-stu-id="b798b-203">Connecting (TCP)</span></span>

<span data-ttu-id="b798b-204">Temps passé à établir la connexion TCP ([Transmission Control Protocol](https://en.wikipedia.org/wiki/Transmission_Control_Protocol)).</span><span class="sxs-lookup"><span data-stu-id="b798b-204">Time spent establishing the TCP ([Transmission Control Protocol](https://en.wikipedia.org/wiki/Transmission_Control_Protocol)) connection.</span></span>

#### <span data-ttu-id="b798b-205">TECHNOLOGIE</span><span class="sxs-lookup"><span data-stu-id="b798b-205">SSL</span></span>

<span data-ttu-id="b798b-206">Temps passé à négocier une connexion SSL ([Secure Sockets Layer](https://en.wikipedia.org/wiki/Transport_Layer_Security)) avec le [serveur proxy](https://en.wikipedia.org/wiki/Proxy_server) de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="b798b-206">Time spent negotiating a SSL ([Secure Sockets Layer](https://en.wikipedia.org/wiki/Transport_Layer_Security))  connection with the [proxy server](https://en.wikipedia.org/wiki/Proxy_server) for the host.</span></span>

#### <span data-ttu-id="b798b-207">Émetteur</span><span class="sxs-lookup"><span data-stu-id="b798b-207">Sending</span></span>

<span data-ttu-id="b798b-208">Temps passé à envoyer la demande de ressource.</span><span class="sxs-lookup"><span data-stu-id="b798b-208">Time spent sending the resource request.</span></span>

#### <span data-ttu-id="b798b-209">En attente (TTFB)</span><span class="sxs-lookup"><span data-stu-id="b798b-209">Waiting (TTFB)</span></span>

<span data-ttu-id="b798b-210">Temps passé à patienter avant le premier octet de la réponse du serveur hôte («durée au premier octet» ou *TTFB*).</span><span class="sxs-lookup"><span data-stu-id="b798b-210">Time spent waiting for the first byte of the response from the host server ("time to first byte", or *TTFB*).</span></span>

#### <span data-ttu-id="b798b-211">Entam</span><span class="sxs-lookup"><span data-stu-id="b798b-211">Downloading</span></span>

<span data-ttu-id="b798b-212">Temps passé à lire la réponse à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="b798b-212">Time spent reading the response from the server.</span></span>

## <span data-ttu-id="b798b-213">Associés</span><span class="sxs-lookup"><span data-stu-id="b798b-213">Shortcuts</span></span>

| <span data-ttu-id="b798b-214">Action</span><span class="sxs-lookup"><span data-stu-id="b798b-214">Action</span></span>                         | <span data-ttu-id="b798b-215">Raccourci</span><span class="sxs-lookup"><span data-stu-id="b798b-215">Shortcut</span></span>     |
|:-------------------------------|:-------------|
| <span data-ttu-id="b798b-216">Démarrer/arrêter la session de profilage</span><span class="sxs-lookup"><span data-stu-id="b798b-216">Start / Stop profiling session</span></span> | `Ctrl` + `E` |
| <span data-ttu-id="b798b-217">Exporter au format QAR</span><span class="sxs-lookup"><span data-stu-id="b798b-217">Export as HAR</span></span>                  | `Ctrl` + `S` |
| <span data-ttu-id="b798b-218">Rechercher</span><span class="sxs-lookup"><span data-stu-id="b798b-218">Find</span></span>                           | `Ctrl` + `F` |
| <span data-ttu-id="b798b-219">Copy</span><span class="sxs-lookup"><span data-stu-id="b798b-219">Copy</span></span>                           | `Ctrl` + `C` |

## <span data-ttu-id="b798b-220">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="b798b-220">Known Issues</span></span>

### <span data-ttu-id="b798b-221">Échec du démarrage de l’agent de collection de réseaux.</span><span class="sxs-lookup"><span data-stu-id="b798b-221">The network collection agent failed to start.</span></span>

<span data-ttu-id="b798b-222">Si vous voyez le message d’erreur suivant: **l’agent de collection de réseaux n’a pas réussi à démarrer** dans l’outil réseau, procédez comme suit pour contourner le problème.</span><span class="sxs-lookup"><span data-stu-id="b798b-222">If you see this error message: **The network collection agent failed to start** in the Network tool, follow these steps for a workaround.</span></span>

1. <span data-ttu-id="b798b-223">Appuyez sur `Windows Key`  +  `R` .</span><span class="sxs-lookup"><span data-stu-id="b798b-223">Press `Windows Key` + `R`.</span></span>

2. <span data-ttu-id="b798b-224">Dans la boîte de dialogue Exécuter, entrez **services. msc**.</span><span class="sxs-lookup"><span data-stu-id="b798b-224">In the Run dialog, enter **services.msc**.</span></span>
![problèmes connus-1](./media/known_issues_1.PNG)

3. <span data-ttu-id="b798b-226">Recherchez le **service collecteur standard de Diagnostics Microsoft (R)** et cliquez dessus avec le bouton droit.</span><span class="sxs-lookup"><span data-stu-id="b798b-226">Locate the **Microsoft (R) Diagnostics Hub Standard Collector Service** and right-click it.</span></span>
![problèmes connus-2](./media/known_issues_2.PNG)

4. <span data-ttu-id="b798b-228">Redémarrez le **service de collecteur standard de Diagnostics Microsoft (R)**.</span><span class="sxs-lookup"><span data-stu-id="b798b-228">Restart the **Microsoft (R) Diagnostics Hub Standard Collector Service**.</span></span>
![problèmes connus-3](./media/known_issues_3.PNG)

5. <span data-ttu-id="b798b-230">Fermez les outils de développement Microsoft Edge et l’onglet. Ouvrez un nouvel onglet, accédez à votre page, puis appuyez sur `F12` .</span><span class="sxs-lookup"><span data-stu-id="b798b-230">Close the Microsoft Edge Developer Tools and the tab. Open a new tab, navigate to your page, and press `F12`.</span></span>

6. <span data-ttu-id="b798b-231">Vous devez maintenant voir un badge lire en regard du **réseau** et les requêtes réseau pour votre page Web.</span><span class="sxs-lookup"><span data-stu-id="b798b-231">You should now see a Play badge next to **Network** and the network requests for your webpage.</span></span>
![problèmes connus-4](./media/known_issues_4-network.PNG)

<span data-ttu-id="b798b-233">Vous rencontrez encore des problèmes?</span><span class="sxs-lookup"><span data-stu-id="b798b-233">Still running into problems?</span></span> <span data-ttu-id="b798b-234">Envoyez-nous vos commentaires à l’aide de l’icône d' **envoi de commentaires** !</span><span class="sxs-lookup"><span data-stu-id="b798b-234">Please send us your feedback using the **Send feedback** icon!</span></span> 

![problèmes connus-5](./media/known_issues_5.PNG)

### <span data-ttu-id="b798b-236">L’agent de collection réseau n’a pas pu s’arrêter.</span><span class="sxs-lookup"><span data-stu-id="b798b-236">The network collection agent failed to stop.</span></span>

<span data-ttu-id="b798b-237">Si vous voyez le message d’erreur suivant: **l’agent de collection de réseaux n’a pas pu s’arrêter** dans l’outil réseau, procédez comme suit pour contourner le problème.</span><span class="sxs-lookup"><span data-stu-id="b798b-237">If you see this error message: **The network collection agent failed to stop** in the Network tool, follow these steps for a workaround.</span></span>

1. <span data-ttu-id="b798b-238">Appuyez sur `Windows Key`  +  `R` .</span><span class="sxs-lookup"><span data-stu-id="b798b-238">Press `Windows Key` + `R`.</span></span>

2. <span data-ttu-id="b798b-239">Dans la boîte de dialogue Exécuter, entrez **services. msc**.</span><span class="sxs-lookup"><span data-stu-id="b798b-239">In the Run dialog, enter **services.msc**.</span></span>
![problèmes connus-1](./media/known_issues_1.PNG)

3. <span data-ttu-id="b798b-241">Recherchez le **service collecteur standard de Diagnostics Microsoft (R)** et cliquez dessus avec le bouton droit.</span><span class="sxs-lookup"><span data-stu-id="b798b-241">Locate the **Microsoft (R) Diagnostics Hub Standard Collector Service** and right-click it.</span></span>
![problèmes connus-2](./media/known_issues_2.PNG)

4. <span data-ttu-id="b798b-243">Redémarrez le **service de collecteur standard de Diagnostics Microsoft (R)**.</span><span class="sxs-lookup"><span data-stu-id="b798b-243">Restart the **Microsoft (R) Diagnostics Hub Standard Collector Service**.</span></span>
![problèmes connus-3](./media/known_issues_3.PNG)

5. <span data-ttu-id="b798b-245">Fermez les outils de développement Microsoft Edge et l’onglet. Ouvrez un nouvel onglet, accédez à votre page, puis appuyez sur `F12` .</span><span class="sxs-lookup"><span data-stu-id="b798b-245">Close the Microsoft Edge Developer Tools and the tab. Open a new tab, navigate to your page, and press `F12`.</span></span>

6. <span data-ttu-id="b798b-246">Vous devez maintenant voir un badge lire en regard du **réseau** et les requêtes réseau pour votre page Web.</span><span class="sxs-lookup"><span data-stu-id="b798b-246">You should now see a Play badge next to **Network** and the network requests for your webpage.</span></span>
![problèmes connus-4](./media/known_issues_4-network.PNG)

<span data-ttu-id="b798b-248">Vous rencontrez encore des problèmes?</span><span class="sxs-lookup"><span data-stu-id="b798b-248">Still running into problems?</span></span> <span data-ttu-id="b798b-249">Envoyez-nous vos commentaires à l’aide de l’icône d' **envoi de commentaires** !</span><span class="sxs-lookup"><span data-stu-id="b798b-249">Please send us your feedback using the **Send feedback** icon!</span></span> 

![problèmes connus-5](./media/known_issues_5.PNG)
