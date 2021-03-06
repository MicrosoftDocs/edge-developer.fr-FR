---
description: Utilisez le panneau Application pour inspecter, modifier et déboguer les manifestes d’application web, les travailleurs de service et les caches de travail de service.
title: Débogage d’applications web progressives
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: aea01d25474a030e78ac0eaeaef3954ab7f4539f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398538"
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

# <a name="debug-progressive-web-apps"></a>Débogage d’applications web progressives  

Utilisez le panneau **Application** pour inspecter, modifier et déboguer les manifestes d’application web, les travailleurs de service et les caches de travail de service.  

<!--Related Guides:  

*   [Progressive Web Apps](/web/progressive-web-apps)  -->

<!--TODO:  Link web "Progressive Web Apps" section when available. -->

Ce guide traite uniquement des fonctionnalités Progressive Web App du panneau **Application.**  <!--If you're looking for help on the other panes, check out the last section of this guide, [Other Application panel guides](#other-application-panel-guides).  -->

<!--TODO:  Link to sections when available. -->

### <a name="summary"></a>Résumé  

*   Utilisez le **volet Manifeste** pour inspecter le manifeste de votre application web et déclencher des événements Ajouter à l’écran d’accueil.  
*   Utilisez **** le volet Travailleurs du service pour toute une gamme de tâches liées au travail de service, telles que la désinssion ou la mise à jour d’un service, l’émulation d’événements Push, la mise hors connexion ou l’arrêt d’un service de travail.  
*   Affichez votre cache de travail de service à partir du **volet Stockage** du cache.  
*   Désinsistez un service de travail et désinsérez tout le stockage et les caches à l’aide d’un seul bouton dans le volet Effacer **le** stockage.  
    
## <a name="web-app-manifest"></a>Manifeste d’application web  

Si vous souhaitez que vos utilisateurs puissent ajouter votre application à leurs écrans d’accueil mobiles, vous avez besoin d’un manifeste d’application web.  Le manifeste définit l’apparence de l’application sur l’écran d’accueil, l’endroit où diriger l’utilisateur lors du lancement à partir de l’écran d’accueil et l’apparence de l’application au lancement.  

<!--Related Guides:  

*   [Improve user experiences with a Web App Manifest](/web/fundamentals/web-app-manifest)  
*   [Using App Install Banners](/web/fundamentals/app-install-banners)  -->

<!--TODO:  Link to sections when available. -->

Une fois votre manifeste installé, vous **** pouvez utiliser le volet Manifeste du panneau **Application** pour l’inspecter.  

:::image type="complex" source="../media/manifest-pane.msft.png" alt-text="Volet manifeste" lightbox="../media/manifest-pane.msft.png":::
   Volet **** manifeste  
:::image-end:::  

*   Pour examiner la source du manifeste, choisissez le lien sous l’étiquette **de manifeste** d’application \( `https://airhorner.com/manifest.json` dans la figure précédente\).  
<!-- *   Choose the **Add to homescreen** button to simulate an Add to Homescreen event.  Check out the next section for more information.  -->  
*   Les **sections** **Identité** et Présentation affichent simplement les champs de la source de manifeste dans un affichage plus convivial.  
*   La section **Icônes** affiche chaque icône que vous avez spécifiée.  
    
<!--### Simulate Add to Homescreen events  -->

<!--A web app may only be added to a homescreen when the site is visited at least twice, with at least five minutes between visits.  While developing or debugging your Add to Homescreen workflow, the criteria is potentially inconvenient.  
The **Add to homescreen** button on the **App Manifest** pane lets you simulate Add to Homescreen events whenever you want.  -->

<!--You may test out this feature with the [Microsoft I/O 2016 progressive web app](https://events.alpahabet.com/io2016/), which has proper support for Add to Homescreen.  Choosing on **Add to Homescreen** while the app is open prompts Microsoft Edge to display the "add this site to your shelf" banner, which is the desktop equivalent of the "add to homescreen" banner for mobile devices.  -->

<!--  
:::image type="complex" source="../media/io.msft.png" alt-text="Add to desktop shelf" lightbox="../media/io.msft.png":::
   Add to desktop shelf  
:::image-end:::
-->  

<!--
> [!Tip]
> Keep the **Console** drawer open while simulating Add to Homescreen events.  The Console tells you if your manifest has any issues and logs other information about the Add to Homescreen lifecycle.  -->

<!--The **Add to Homescreen** feature may not yet simulate the workflow for mobile devices.  Notice how the "add to shelf" prompt was triggered in the screenshot above, even though DevTools is in Device Mode.  However, if you may successfully add your app to your desktop shelf, then it works for mobile, too.  -->

<!-- TODO: Rework content after sample app is created. -->

<!--If you want to test out the genuine mobile experience, you may connect a real mobile device to DevTools via **remote debugging**, and then choose the **Add to Homescreen** button \(on DevTools\) to trigger the "add to homescreen" prompt on the connected mobile device.  -->

<!--TODO:  Link Debug "remote debugging" sections when available. -->

## <a name="service-workers"></a>Travailleurs du service  

Les travailleurs de service sont une technologie fondamentale dans la future plateforme web.  Il s’agit de scripts que le navigateur exécute en arrière-plan, séparés d’une page web.  Les scripts vous permettent d’accéder à des fonctionnalités qui n’ont pas besoin d’une page web ou d’une interaction utilisateur, telles que les notifications Push, la synchronisation en arrière-plan et les expériences hors connexion.  

<!--Related Guides:  

*   [Intro to Service Workers](/web/fundamentals/primers/service-worker)  
*   [Push Notifications: Timely, Relevant, and Precise](/web/fundamentals/push-notifications)  -->  
    
<!--TODO:  Link to sections when available. -->  

Le **volet Travailleurs** du service dans le panneau **Application** est l’endroit principal dans DevTools pour inspecter et déboguer les travailleurs du service.  

:::image type="complex" source="../media/service-workers-pane.msft.png" alt-text="Volet Travailleurs du service" lightbox="../media/service-workers-pane.msft.png":::
   Volet **Travailleurs** du service  
:::image-end:::  

*   Si un service de travail est installé sur la page actuellement ouverte, il est répertorié dans ce volet.  Par exemple, dans la figure précédente, un service de travail est installé pour l’étendue de `https://weather-pwa-sample.firebaseapp.com` .  
*   La **case à** cocher Hors connexion place DevTools en mode hors connexion.  Cela équivaut au mode hors connexion disponible à partir de l’outil **Réseau** ou à l’option `Go offline` du menu [Commande.][DevtoolsCommandMenuIndex]  
*   La case à cocher Mise à **jour lors du rechargement** force le service de travail à mettre à jour chaque chargement de page.  
*   La **case à cocher** Contournement du réseau contourne le service de travail et force le navigateur à se rendre sur le réseau pour les ressources demandées.  
*   Le **bouton** Mettre à jour effectue une mise à jour à une seule fois du service de travail spécifié.  
*   Le **bouton Push** émule une notification Push sans charge utile \(également appelée une coche \). ****  
*   Le **bouton Synchroniser** émule un événement de synchronisation en arrière-plan.  
*   Le **bouton Désinsserrement** désinsère le service de travail spécifié.  Consultez [Effacer le stockage](#clear-storage) pour supprimer l’enregistrement d’un service de travail et effacer le stockage et les caches avec un seul bouton.  
*   La **ligne Source** vous indique quand le service de travail en cours d’exécution a été installé.  Le lien est le nom du fichier source du service de travail.  Le choix du lien vous envoie à la source du service de travail.  
*   La **ligne État** vous indique l’état du service de travail.  Le numéro d’ID à côté de l’indicateur d’état vert \( dans la figure précédente\) est pour le service de travail `#36` actif.  En plus de **** l’état, un bouton de démarrage \(si le service de travail est arrêté\) ou un bouton d’arrêt \(si le service de travail est en cours d’exécution\) s’affiche. ****  Les employés de service sont conçus pour être arrêtés et démarrés par le navigateur à tout moment.  L’arrêt explicite de votre service à l’aide du **bouton** d’arrêt peut simuler cela.  L’arrêt de votre service de travail est un excellent moyen de tester le comportement de votre code lorsque le service de travail recommence à le faire.  Il révèle fréquemment des bogues en raison d’hypothèses erronées sur l’état global persistant.  
*   La **ligne Clients** vous indique l’origine de l’étendue du service de travail.  Le **bouton Focus** est principalement utile lorsque vous avez activé la case à cocher Afficher **tout.**  Lorsque cette case à cocher est activée, tous les employés de service inscrits sont répertoriés.  Si vous choisissez sur le **bouton focus** en face d’un service de travail qui s’exécute sous un autre onglet, Microsoft Edge se concentre sur cet onglet.  
    
Si le service de travail provoque des erreurs, une nouvelle étiquette appelée **Erreurs** s’affiche.  

<!--  
:::image type="complex" source="../media/sw-error.msft.png" alt-text="Service worker with errors" lightbox="../media/sw-error.msft.png":::
   Service worker with errors  
:::image-end:::
-->  

<!--TODO:  Capture Service Worker Errors sample when available. -->
<!--TODO:  Link Web "How tickle works" sections when available. -->

## <a name="service-worker-caches"></a>Caches de travail de service  

Le **volet Stockage** du cache fournit une liste en lecture seule des ressources qui ont été mises en cache à l’aide de l’API de [cache][MDNWebCacheAPI]\(service worker\).  

:::image type="complex" source="../media/cache-pane-cache-storage-resources.msft.png" alt-text="Volet de stockage du cache" lightbox="../media/cache-pane-cache-storage-resources.msft.png":::
   Volet **de stockage du** cache  
:::image-end:::  

> [!NOTE]
> La première fois que vous ouvrez un cache et y ajoutez une ressource, DevTools risque de ne pas détecter la modification.  Actualisez la page et affichez le cache.  

Si vous avez au moins deux caches ouverts, les caches s’affichent sous la **liste** de stockage de cache suivante.  

:::image type="complex" source="../media/cache-pane-cache-storage.msft.png" alt-text="La zone de dépôt Stockage du cache" lightbox="../media/cache-pane-cache-storage.msft.png":::
   La zone **de dépôt Stockage** du cache  
:::image-end:::  

## <a name="quota-usage"></a>Utilisation des quotas  

Certaines réponses dans le **volet Stockage** du cache peuvent être marquées comme étant « opaques ».  Cela fait référence à une réponse extraite d’une origine différente, comme à partir d’un **CDN** ou d’une API distante, lorsque [CORS][FetchHttpCorsProtocol] n’est pas activé.  

<!--TODO:  Link Web "CDN" section when available. -->  
<!--TODO:  Link Web "opaque" section when available. -->

Afin d’éviter les fuites d’informations entre domaines, un remplissage important est ajouté à la taille d’une réponse opaque utilisée pour calculer les limites de quota de stockage \(par exemple, si une exception est déclarée\) et signalée par `QuotaExceeded` `navigator.storage` l’API.  

<!--TODO:  Link Estimating "`navigator.storage` API" sections when available. -->

Les détails de ce remplissage varient d’un navigateur à l’autre, mais pour Microsoft Edge, cela signifie que la taille **minimale** de toute réponse opaque mise en cache contribue à l’utilisation globale du stockage est d’environ [7 mégaoctets][ChromiumIssues796060#c17].  N’oubliez pas le remplissage lors de la détermination du nombre de réponses opaques que vous souhaitez mettre en cache, car vous pouvez facilement dépasser les limites de quota de stockage beaucoup plus tôt que prévu en fonction de la taille réelle des ressources opaques.  

Guides connexes :  

*   [Stack Overflow : quelles limitations s’appliquent aux réponses opaques ?][StackOverflowLimitationsForOpaqueResponses]  
<!--*   [Alphabet work container: Understanding Storage Quota](/web/tools/Alphabet-work-container/guides/storage-quota#beware_of_opaque_responses)  -->
    
<!--TODO:  Link Work container storage quota for opaque responses section when available. -->

## <a name="clear-storage"></a>Effacer le stockage  

Le **volet Effacer le** stockage est une fonctionnalité très utile lors du développement d’applications web progressives.  Ce volet vous permet de désinsser les travailleurs du service et d’effacer tous les caches et tous les espaces de stockage en un seul bouton.  <!--Check out the section below to learn more.  -->

<!--Related Guides:  

*   [Clear Storage](/iterate/manage-data/local-storage#clear-storage)  -->
    
<!--TODO:  Link to sections when available. -->

<!--## Other Application panel guides   

Check out the guides below for more help on the other panes of the **Application** panel.  

Related Guides:  

*   [Inspect page resources](/iterate/manage-data/page-resources)  
*   [Inspect and manage local storage and caches](/iterate/manage-data/local-storage)  -->
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Exécuter des commandes avec le menu de commandes Microsoft Edge DevTools | Documents Microsoft"  

[ChromiumIssues796060#c17]: https://bugs.chromium.org/p/chromium/issues/detail?id=796060#c17 "Chromium Issue 796060: Cache Storage value rises on each refresh when Analytics code is in the html"  

[FetchHttpCorsProtocol]: https://fetch.spec.whatwg.org/#http-cors-protocol  

[MDNWebCacheAPI]: https://developer.mozilla.org/docs/Web/API/Cache "Cache : api web | MDN"  

[StackOverflowLimitationsForOpaqueResponses]: https://stackoverflow.com/q/39109789/385997 "Stack Overflow : quelles limitations s’appliquent aux réponses opaques ?"  

<!--[WebEstimatingAvailableStorageSpace]: whats-new/2017/08/estimating-available-storage-space  -->
<!--[RemoteDebugging]: /debug/remote-debugging/remote-debugging  -->

<!--[WebHowPushWorks]: /web/fundamentals/push-notifications/how-push-works  -->  
<!--[WebGlossaryCDN]: /web/fundamentals/glossary#CDN  -->
<!--[WebGlossaryOpaque]: /web/fundamentals/glossary#opaque-response  -->

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
