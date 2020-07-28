---
title: Accéder aux serveurs locaux
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: daa96b604d5ad48a9de49dd24dc38eab79de9c9b
ms.sourcegitcommit: ad5eb43172280974b8c063867c2097f7c5c0e77d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/27/2020
ms.locfileid: "10898213"
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





# Accéder aux serveurs locaux   




Hébergez un site sur un serveur Web d’ordinateur de développement, puis accédez au contenu d’un appareil Android.  

Avec un câble USB et Microsoft Edge DevTools, exécutez un site à partir d’un ordinateur de développement, puis affichez le site sur un appareil Android.  

### Résumé  

*   Le transfert de port vous permet d’afficher le contenu hébergé par le serveur Web exécuté sur votre ordinateur de développement sur votre appareil Android.  
*   Si votre serveur Web utilise un domaine personnalisé, configurez votre appareil Android pour accéder au contenu de ce domaine avec le mappage de domaine personnalisé.  

## Configurer le transfert de port   

Le transfert de port permet à votre appareil Android d’accéder au contenu hébergé sur le serveur Web exécuté sur votre ordinateur de développement.  Le transfert de port fonctionne en créant un port TCP d’écoute sur votre appareil Android qui mappe vers un port TCP sur votre ordinateur de développement.  Le trafic entre les ports voyage via la connexion USB entre votre appareil et votre machine de développement Android, de sorte que la connexion ne dépend pas de votre configuration réseau.  

Pour activer le transfert de port:  

1.  Configurez le [débogage à distance][RemoteDebuggingGettingStarted] entre votre ordinateur de développement et votre appareil Android.  Lorsque vous avez terminé, vous devriez voir votre appareil Android dans le menu de gauche de la boîte de dialogue **inspecter les appareils** et un témoin de statut **connecté** .  
1.  Dans la boîte de dialogue **inspection des appareils** de devtools, activez le **transfert de port**.  
1.  Sélectionnez **Ajouter une règle**.  
    
    > ##### Figure1  
    > Ajout d’une règle de transfert de port  
    > ![Ajout d’une règle de transfert de port][ImageAddRule]  
    
1.  Dans la zone de texte **port du périphérique** à gauche, entrez le `localhost` numéro de port à partir duquel vous voulez accéder au site sur votre appareil Android.  Par exemple, si vous voulez accéder au site à partir de `localhost:5000` Enter `5000` .  
1.  Dans la zone d' **adresse locale** située à droite, entrez l’adresse IP ou le nom d’hôte sur lequel votre site est hébergé sur le serveur Web exécuté sur votre ordinateur de développement, puis le numéro de port.  Par exemple, si votre site est en cours d’exécution sur `localhost:7331` Enter (entrée) `localhost:7331` .  
1.  Cliquez sur **Ajouter**.  

Le transfert de port est désormais configuré.  Pour afficher l’indicateur d’État du port vers l’avant, accédez à l’onglet de votre appareil dans la boîte de dialogue **inspecter les appareils** .  

> ##### Figure 2  
> État de transfert de port  
> ![État de transfert de port][ImagePortForwardingStatus]  

Pour afficher le contenu, ouvrez Microsoft Edge sur votre appareil Android et accédez au `localhost` port que vous avez spécifié dans le champ **port** de l’appareil.  Par exemple, si vous avez entré `5000` dans le champ, rendez-vous `localhost:5000` .  

## Mapper aux domaines locaux personnalisés   

Le mappage de domaine personnalisé vous permet d’afficher le contenu sur un appareil Android à partir d’un serveur Web sur votre ordinateur de développement qui utilise un domaine personnalisé.  

Par exemple, supposons que votre site utilise une bibliothèque JavaScript tierce qui fonctionne uniquement sur le domaine `microsoft-edge.devtools` .  Par conséquent, vous créez une entrée dans votre `hosts` fichier sur votre ordinateur de développement pour mapper ce domaine à `localhost` \ (par exemple, `127.0.0.1 microsoft-edge.devtools` \).  Après avoir configuré le mappage de domaine personnalisé et le transfert de port, affichez le site sur votre appareil Android à l’URL `microsoft-edge.devtools` .  

### Configurer le transfert de port vers le serveur proxy  

Pour mapper un domaine personnalisé, vous devez exécuter un serveur proxy sur votre ordinateur de développement.  Voici quelques exemples de serveurs proxy: [Charles][CharlesWebDebuggingProxy], [Squid][SquidOptimisingWebDelivery]et [Fiddler][FiddlerWebDebuggingProxy].  

Pour configurer le renvoi de port vers un proxy:  

1.  Exécutez le serveur proxy et enregistrez le port qu’il utilise.  
    
    > [!NOTE]
    > Le serveur proxy et votre serveur Web doivent s’exécuter sur différents ports.  
    
1.  Configurez le [renvoi de port](#set-up-port-forwarding) vers votre appareil Android.  Pour le champ **adresse locale** , entrez `localhost:` suivi du port sur lequel votre serveur proxy s’exécute.  Par exemple, s’il est en cours d’exécution sur le port `8000` , rendez-vous `localhost:8000` .  Dans le champ Port de l' **appareil** , entrez le numéro que vous souhaitez que votre appareil Android écoute, par exemple `3333` .  

### Configurer les paramètres de proxy sur votre appareil  

Ensuite, vous devez configurer votre appareil Android pour communiquer avec le serveur proxy.  

1.  Sur votre appareil Android, accédez à **réglages**  >  **Wi-Fi**.  
1.  Appuyez longuement sur le nom du réseau auquel vous êtes actuellement connecté.  
    
    > [!NOTE]
    > Les paramètres de proxy s’appliquent par réseau.  
    
1.  Sélectionnez **modifier le réseau**.  
1.  Sélectionnez **Options avancées**.  Les paramètres du proxy apparaissent.  
1.  Sélectionnez le menu **proxy** et sélectionnez **Manuel**.  
1.  Pour le champ **nom_hôte du proxy** , entrez `localhost` .  
1.  Pour le champ **port proxy** , entrez le numéro de port que vous avez entré pour **port d’appareil** dans la section précédente.  
1.  Sélectionnez **Enregistrer**.  

À l’aide de ces paramètres, votre appareil transfère toutes les demandes à ce proxy sur votre ordinateur de développement.  Le serveur proxy effectue des demandes de la part de votre appareil, de sorte que les demandes adressées à votre domaine local personnalisé sont correctement résolues.  

Accédez désormais aux domaines personnalisés sur votre appareil Android tout comme sur l’ordinateur de développement.  

Si votre serveur Web est en cours d’exécution sur un port autre qu’un port standard, n’oubliez pas de spécifier le port lors de la demande du contenu à partir de votre appareil Android.  Par exemple, si votre serveur Web utilise le domaine personnalisé `microsoft-edge.devtools` sur le port `7331` , lorsque vous affichez le site à partir de votre appareil Android, vous devez utiliser l’URL `microsoft-edge.devtools:7331` .  

> [!TIP]
> Pour reprendre la navigation normale, n’oubliez pas de rétablir les paramètres de proxy sur votre appareil Android après vous être déconnecté de l’ordinateur de développement.  

<!--  -->  



<!-- image links -->  

[ImageAddRule]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png "Figure 1: ajout d’une règle de transfert de port"  
[ImagePortForwardingStatus]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png "Figure 2: état de transfert de port"  

<!-- links -->  

[RemoteDebuggingGettingStarted]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Découvrir les appareils Android de débogage à distance"  

[CharlesWebDebuggingProxy]: https://www.charlesproxy.com "Proxy de débogage Web Charles"  

[SquidOptimisingWebDelivery]: https://www.squid-cache.org "Squid: optimisation de la remise sur le Web"  

[FiddlerWebDebuggingProxy]: https://www.telerik.com/fiddler "Fiddler-proxy de débogage Web gratuit"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \) et [Meggin Kearney][MegginKearney] \ (Technical Writer \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
