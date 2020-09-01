---
title: Déboguer des applications Web progressives
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 6733d7823348bc02dd6f29ec218a33ab4073dbfc
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984952"
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





# Déboguer des applications Web progressives   



Utilisez le panneau **application** pour inspecter, modifier et déboguer des manifestes de l’application Web, des travailleurs de services et des mises en cache de service.  

<!--Related Guides:  

*   [Progressive Web Apps](/web/progressive-web-apps)  -->

<!--TODO:  Link web "Progressive Web Apps" section when available. -->

Ce guide traite uniquement des fonctionnalités d’application Web progressive du panneau **application** .  <!--If you're looking for help on the other panes, check out the last section of this guide, [Other Application panel guides](#other-application-panel-guides).  -->

<!--TODO:  Link to sections when available. -->

### Résumé  

*   Utilisez le volet **manifeste** pour examiner le manifeste de votre application Web et déclencher l’ajout aux événements écran d’accueil.  
*   Utilisez le volet **travailleurs de services** pour une gamme complète de tâches associées au service, telles que l’annulation de l’inscription ou la mise à jour d’un service, l’émulation des événements de transmission, la mise hors connexion ou l’arrêt d’un service.  
*   Affichez le cache de votre service d’assistance dans le volet **stockage du cache** .  
*   Annulez l’enregistrement d’un ouvrier de services et effacez l’intégralité du stockage et des caches à l’aide d’un seul bouton dans le volet de **stockage clair** .  
    
## Manifeste de l’application Web   

Si vous souhaitez que vos utilisateurs puissent ajouter votre application à leur mobile homescreens, vous avez besoin d’un manifeste d’application Web.  Le manifeste définit la façon dont l’application s’affiche sur le écran d’accueil, où diriger l’utilisateur lors du lancement à partir de écran d’accueil, et l’apparence de l’application au moment du lancement.  

<!--Related Guides:  

*   [Improve user experiences with a Web App Manifest](/web/fundamentals/web-app-manifest)  
*   [Using App Install Banners](/web/fundamentals/app-install-banners)  -->

<!--TODO:  Link to sections when available. -->

Une fois votre manifeste configuré, vous pouvez utiliser le volet **manifeste** du panneau de l' **application** pour l’inspecter.  

:::image type="complex" source="./media/manifest-pane.msft.png" alt-text="Volet manifeste" lightbox="./media/manifest-pane.msft.png":::
   Volet **manifeste**  
:::image-end:::  

*   Pour examiner la source du manifeste, cliquez sur le lien ci-dessous intitulé du manifeste de l' **application** \ ( `https://airhorner.com/manifest.json` dans la figure ci-dessous).  
<!-- *   Press the **Add to homescreen** button to simulate an Add to Homescreen event.  Check out the next section for more information.  -->  
*   Les sections **identité** et **Présentation** affichent simplement les champs de la source du manifeste dans un affichage plus convivial.  
*   La section **icônes** affiche chaque icône que vous avez spécifiée.  
    
<!--### Simulate Add to Homescreen events   -->

<!--A web app can only be added to a homescreen when the site is visited at least twice, with at least five minutes between visits.  While developing or debugging your Add to Homescreen workflow, this criteria can be inconvenient.  
The **Add to homescreen** button on the **App Manifest** pane lets you simulate Add to Homescreen events whenever you want.  -->

<!--You can test out this feature with the [Microsoft I/O 2016 progressive web app](https://events.alpahabet.com/io2016/), which has proper support for Add to Homescreen.  Clicking on **Add to Homescreen** while the app is open prompts Microsoft Edge to display the "add this site to your shelf" banner, which is the desktop equivalent of the "add to homescreen" banner for mobile devices.  -->

<!--  
:::image type="complex" source="./media/io.msft.png" alt-text="Add to desktop shelf" lightbox="./media/io.msft.png":::
   Add to desktop shelf  
:::image-end:::
-->  

<!--
> [!Tip]
> Keep the **Console** drawer open while simulating Add to Homescreen events.  The Console tells you if your manifest has any issues and logs other information about the Add to Homescreen lifecycle.  -->

<!--The **Add to Homescreen** feature cannot yet simulate the workflow for mobile devices.  Notice how the "add to shelf" prompt was triggered in the screenshot above, even though DevTools is in Device Mode.  However, if you can successfully add your app to your desktop shelf, then it'll work for mobile, too.  -->

<!-- TODO: Rework content after sample app is created. -->

<!--If you want to test out the genuine mobile experience, you can connect a real mobile device to DevTools via **remote debugging**, and then click the **Add to Homescreen** button \(on DevTools\) to trigger the "add to homescreen" prompt on the connected mobile device.  -->

<!--TODO:  Link Debug "remote debugging" sections when available. -->

## Travailleurs de service   

Les travailleurs de service constituent une technologie fondamentale dans la prochaine plateforme Web.  Il s’agit de scripts que le navigateur exécute en arrière-plan, séparés d’une page Web.  Ces scripts vous permettent d’accéder aux fonctionnalités qui n’ont pas besoin d’une interaction utilisateur ou page Web, comme les notifications de transmission, la synchronisation en arrière-plan et les expériences hors connexion.  

<!--Related Guides:  

*   [Intro to Service Workers](/web/fundamentals/primers/service-worker)  
*   [Push Notifications: Timely, Relevant, and Precise](/web/fundamentals/push-notifications)  -->  
    
<!--TODO:  Link to sections when available. -->  

Le volet **travailleurs de services** dans le panneau d' **application** est l’endroit principal de devtools pour inspecter et déboguer des travailleurs de service.  

:::image type="complex" source="./media/service-workers-pane.msft.png" alt-text="Volet travailleurs de service" lightbox="./media/service-workers-pane.msft.png":::
   Volet **travailleurs de service**  
:::image-end:::  

*   Si un ouvrier de services est installé sur la page actuellement ouverte, il apparaît dans ce volet.  Par exemple, dans l’illustration précédente, il existe un travailleur de service dont l’étendue est `https://weather-pwa-sample.firebaseapp.com` .  
*   La case à cocher **mode hors connexion** place le devtools en mode hors connexion.  Cela équivaut au mode hors connexion disponible sur le panneau **réseau** ou à l' `Go offline` option dans le [menu de commandes][DevtoolsCommandMenuIndex].  
*   La case à cocher **mettre à jour lors du rechargement** force le travailleur de service à procéder à la mise à jour à chaque chargement.  
*   La case à cocher **contournement pour le réseau** ignore le travailleur du service et force le navigateur à accéder au réseau pour les ressources demandées.  
*   Le bouton **mettre à jour** effectue une mise à jour ponctuelle du travailleur de services spécifié.  
*   Le bouton de **transmission** émule une notification de transmission sans une charge utile (également appelée « **Tickle**»).  
*   Le bouton **synchroniser** émule un événement de synchronisation en arrière-plan.  
*   Le bouton **Annuler l’inscription** annule l’enregistrement du travailleur de service indiqué.  Découvrez comment annuler l' [enregistrement d’un](#clear-storage) employé de service et effacer le stockage et les caches à l’aide d’un seul clic de bouton.  
*   La ligne **source** vous indique lorsque le travailleur de service en cours d’exécution a été installé.  Le lien est le nom du fichier source du travailleur du service.  Cliquer sur le lien vous envoie à la source du travailleur du service.  
*   La ligne de **statut** indique le statut du travailleur de service.  Le numéro d’identification en regard du voyant de statut vert ( `#36` dans la figure précédente \) est destiné au travailleur de service actuellement actif.  En regard du statut, vous verrez un bouton **Démarrer** (si le travailleur a arrêté le service \) ou un bouton d' **arrêt** (si le travailleur du service exécute \).  Les travailleurs de service sont conçus pour s’arrêter et démarrer par le navigateur à tout moment.  L’arrêt explicite de votre travailleur de service à l’aide du bouton **Stop** peut simuler.  L’arrêt de votre travailleur est un excellent moyen de tester le comportement de votre code lors du redémarrage du travailleur du service.  Il révèle fréquemment les bogues causés par des hypothèses incorrectes sur l’état global persistant.  
*   La ligne **clients** indique l’origine à laquelle le travailleur de service est limité.  Le bouton **focus** est principalement utile lorsque vous avez activé la case à cocher **Afficher tout** .  Lorsque cette case est cochée, tous les travailleurs de service inscrits apparaissent.  Si vous cliquez sur le bouton **focus** en regard d’un ouvrier de services en cours d’exécution dans un autre onglet, Microsoft Edge est axé sur cet onglet.  
    
Si le travailleur du service génère des erreurs, une nouvelle étiquette appelée **Erreurs** s’affiche.  

<!--  
:::image type="complex" source="./media/sw-error.msft.png" alt-text="Service worker with errors" lightbox="./media/sw-error.msft.png":::
   Service worker with errors  
:::image-end:::
-->  

<!--TODO:  Capture Service Worker Errors sample when available. -->
<!--TODO:  Link Web "How tickle works" sections when available. -->

## Caches du travailleur de service 

Le volet **stockage du cache** fournit une liste en lecture seule de ressources qui ont été mises en cache à l’aide de l' [API de cache][MDNWebCacheAPI]\ (Service Worker \).  

:::image type="complex" source="./media/cache-pane-cache-storage-resources.msft.png" alt-text="Volet stockage du cache" lightbox="./media/cache-pane-cache-storage-resources.msft.png":::
   Volet **stockage du cache**  
:::image-end:::  

> [!NOTE]
> La première fois que vous ouvrez un cache et y ajoutez une ressource, il est possible que DevTools ne détecte pas la modification.  Rechargez la page et vous devriez voir le cache.  

Si vous avez deux mises en cache ouvertes, celles-ci s’affichent sous la liste déroulante **stockage du cache** .  

:::image type="complex" source="./media/cache-pane-cache-storage.msft.png" alt-text="Liste déroulante stockage du cache" lightbox="./media/cache-pane-cache-storage.msft.png":::
   Liste déroulante **stockage du cache**  
:::image-end:::  

## Utilisation du quota 

Certaines réponses dans le volet **stockage du cache** sont signalées comme «opaques».  Fait référence à une réponse Récupérée à partir d’une autre origine, par exemple à partir d’une API de **réseau de distribution de contenu ou d'** une API distante, lorsque [cors][FetchHttpCorsProtocol] n’est pas activé.  

<!--TODO:  Link Web "CDN" section when available. -->  
<!--TODO:  Link Web "opaque" section when available. -->

Afin d’éviter toute fuite d’information entre domaines, un remplissage important est ajouté à la taille d’une réponse opaque utilisée pour calculer les limites de quota de stockage (par exemple, si une `QuotaExceeded` exception est levée \) et signalée par l' `navigator.storage` API.  

<!--TODO:  Link Estimating "`navigator.storage` API" sections when available. -->

Les détails de ces remplissages varient d’un navigateur à l’autre, mais pour Microsoft Edge, cela signifie que la **taille minimale** d’une seule réponse opaque mise en cache est d' [environ 7 Mo][ChromiumIssues796060#c17].  N’oubliez pas de savoir ce que vous devez faire lorsque vous déterminez le nombre de réponses opaques que vous souhaitez mettre en cache, dans la mesure où vous risquez de dépasser facilement les limitations de quota de stockage de manière plus rapide que si vous vous attendiez en fonction de la taille réelle des ressources opaques.  

Guides connexes:  

*   [Débordement de pile: quelles limitations s’appliquent aux réponses opaques?][StackOverflowLimitationsForOpaqueResponses]  
<!--*   [Alphabet work container: Understanding Storage Quota](/web/tools/Alphabet-work-container/guides/storage-quota#beware_of_opaque_responses)  -->
    
<!--TODO:  Link Work container storage quota for opaque responses section when available. -->

## Effacement du stockage 

Le volet **Vider le stockage** est une fonctionnalité très utile lorsque vous développez des applications Web progressives.  Ce volet vous permet d’annuler l’enregistrement des travailleurs de services et d’effacer tous les caches et stockage avec un seul clic de bouton.  <!--Check out the section below to learn more.  -->

<!--Related Guides:  

*   [Clear Storage](/iterate/manage-data/local-storage#clear-storage)  -->
    
<!--TODO:  Link to sections when available. -->

<!--## Other Application panel guides 

Check out the guides below for more help on the other panes of the **Application** panel.  

Related Guides:  

*   [Inspect page resources](/iterate/manage-data/page-resources)  
*   [Inspect and manage local storage and caches](/iterate/manage-data/local-storage)  -->
    
<!--TODO  -->

<!--  
 


-->  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ./command-menu/index.md "Exécuter des commandes à l’aide du menu de commandes de Microsoft Edge DevTools | Documents Microsoft"  

[ChromiumIssues796060#c17]: https://bugs.chromium.org/p/chromium/issues/detail?id=796060#c17 "Problème de chrome 796060: une valeur de stockage de cache augmente chaque actualisation lorsque le code d’analyse est dans le code html"  

[FetchHttpCorsProtocol]: https://fetch.spec.whatwg.org/#http-cors-protocol  

[MDNWebCacheAPI]: https://developer.mozilla.org/docs/Web/API/Cache "Cache-API Web | MDN"  

[StackOverflowLimitationsForOpaqueResponses]: https://stackoverflow.com/q/39109789/385997 "Débordement de pile: quelles limitations s’appliquent aux réponses opaques?"  

<!--[WebEstimatingAvailableStorageSpace]: whats-new/2017/08/estimating-available-storage-space  -->
<!--[RemoteDebugging]: /debug/remote-debugging/remote-debugging  -->

<!--[WebHowPushWorks]: /web/fundamentals/push-notifications/how-push-works  -->  
<!--[WebGlossaryCDN]: /web/fundamentals/glossary#CDN  -->
<!--[WebGlossaryOpaque]: /web/fundamentals/glossary#opaque-response  -->

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
