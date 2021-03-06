---
description: Hébergez un site sur un serveur web d’ordinateur de développement, puis accédez au contenu à partir d’un appareil Android.
title: Accéder aux serveurs locaux
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 16c9927ce4548d71681d35e643aea0a6c44ec75a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398209"
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

# <a name="access-local-servers"></a>Accéder aux serveurs locaux  

Hébergez un site sur un serveur web d’ordinateur de développement, puis accédez au contenu à partir d’un appareil Android.  

Avec un câble USB et Microsoft Edge DevTools, exécutez un site à partir d’un ordinateur de développement, puis affichez le site sur un appareil Android.  

### <a name="summary"></a>Résumé  

*   Le portage vous permet d’afficher le contenu hébergé par le serveur web s’exécutant sur votre ordinateur de développement sur votre appareil Android.  
*   Si votre serveur web utilise un domaine personnalisé, configurer votre appareil Android pour accéder au contenu de ce domaine avec le mappage de domaine personnalisé.  

## <a name="set-up-port-forwarding"></a>Configurer le forwarding de port  

Le portage permet à votre appareil Android d’accéder au contenu hébergé sur le serveur web en cours d’exécution sur votre ordinateur de développement.  Le portage fonctionne en créant un port TCP d’écoute sur votre appareil Android qui est mappé à un port TCP sur votre ordinateur de développement.  Le trafic entre les ports passe par la connexion USB entre votre appareil Android et votre ordinateur de développement, de sorte que la connexion ne dépend pas de votre configuration réseau.  

Pour activer le portage :  

1.  Configurer le [débogage à distance][RemoteDebuggingGettingStarted] entre votre ordinateur de développement et votre appareil Android.  Lorsque vous avez terminé, votre appareil Android doit s’afficher **** dans le menu gauche de la boîte de dialogue Inspecter les appareils et un **indicateur d’état** Connecté.  
1.  Dans la **boîte de dialogue Inspecter les** appareils dans DevTools, activez le **portage.**  
1.  Choose **Add rule**.  
    
    :::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png" alt-text="Ajout d’une règle de forwarding de port" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png":::
       Ajout d’une règle de forwarding de port  
    :::image-end:::  
    
1.  Dans la **zone de texte** Du port de l’appareil sur la gauche, entrez le numéro de port à partir duquel vous souhaitez pouvoir accéder au site sur votre appareil `localhost` Android.  Par exemple, si vous souhaitez accéder au site à partir `localhost:5000` `5000` d’entrée.  
1.  Dans **** la zone de texte Adresse locale à droite, entrez l’adresse IP ou le nom d’hôte sur lequel votre site est hébergé sur le serveur web en cours d’exécution sur votre ordinateur de développement, suivi du numéro de port.  Par exemple, si votre site est en cours d’exécution lors de `localhost:7331` `localhost:7331` l’entrée.  
1.  Choose **Add**.  
    
Le forwarding de port est maintenant installé.  Examinez l’indicateur d’état du port avant sous l’onglet de votre appareil dans la boîte de dialogue **Inspecter les appareils.**  

:::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png" alt-text="État du port de forwarding" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png":::
   État du port de forwarding  
:::image-end:::  

Pour afficher le contenu, ouvrez Microsoft Edge sur votre appareil Android et allez au port que vous avez spécifié dans le champ `localhost` **Port de l’appareil.**  Par exemple, si vous avez `5000` entré dans le champ, visitez `localhost:5000` .  

## <a name="map-to-custom-local-domains"></a>Ma map to custom local domains  

Le mappage de domaine personnalisé vous permet d’afficher le contenu sur un appareil Android à partir d’un serveur web sur votre ordinateur de développement qui utilise un domaine personnalisé.  

Par exemple, supposons que votre site utilise une bibliothèque JavaScript tierce qui fonctionne uniquement sur le `microsoft-edge.devtools` domaine.  Par exemple, vous créez une entrée dans votre fichier sur votre ordinateur de développement pour ma cartographier ce domaine sur `hosts` `localhost` \(par `127.0.0.1 microsoft-edge.devtools` exemple, \).  Après avoir mis en place le mappage de domaine personnalisé et le forwarding de port, affichez le site sur votre appareil Android à `microsoft-edge.devtools` l’URL.  

### <a name="set-up-port-forwarding-to-proxy-server"></a>Configurer le forwarding de port vers le serveur proxy  

Pour ma cartographier un domaine personnalisé, vous devez exécuter un serveur proxy sur votre ordinateur de développement.  Par exemple, les serveurs proxy [sont Charles][CharlesWebDebuggingProxy], Fiddler et [Fiddler.][FiddlerWebDebuggingProxy] [][SquidOptimisingWebDelivery]  

Pour configurer le port de forwarding vers un proxy :  

1.  Exécutez le serveur proxy et enregistrez le port qu’il utilise.  
    
    > [!NOTE]
    > Le serveur proxy et votre serveur web doivent s’exécuter sur différents ports.  
    
1.  Configurer le [portage vers](#set-up-port-forwarding) votre appareil Android.  Pour le **champ d’adresse** local, entrez suivi du port sur `localhost:` qui votre serveur proxy est en cours d’exécution.  Par exemple, s’il est en cours d’exécution sur le `8000` port, accédez à `localhost:8000` .  Dans le **champ port de l’appareil,** entrez le numéro que vous souhaitez que votre appareil Android écoute, par `3333` exemple.  
    
### <a name="configure-proxy-settings-on-your-device"></a>Configurer les paramètres de proxy sur votre appareil  

Ensuite, vous devez configurer votre appareil Android pour communiquer avec le serveur proxy.  

1.  Sur votre appareil Android, accédez à **Paramètres**  >  **Wi-Fi**.  
1.  Appuyez longuement sur le nom du réseau auquel vous êtes actuellement connecté.  
    
    > [!NOTE]
    > Les paramètres proxy s’appliquent par réseau.  
    
1.  Choose **Modify network**.  
1.  Choisissez **Options avancées.**  Les paramètres du proxy s’affichent.  
1.  Choisissez le menu **proxy** et choisissez **Manuel.**  
1.  Pour le **champ Nom d’hôte proxy,** entrez `localhost` .  
1.  Pour le **champ Port proxy,** entrez le numéro de port que vous avez entré pour le **port** d’appareil dans la section précédente.  
1.  Choose **Save**.  
    
Avec ces paramètres, votre appareil forwarde toutes ses demandes au proxy sur votre ordinateur de développement.  Le proxy effectue des demandes au nom de votre appareil, afin que les demandes à votre domaine local personnalisé soient correctement résolues.  

Accédez maintenant à des domaines personnalisés sur votre appareil Android, comme sur l’ordinateur de développement.  

Si votre serveur web s’exécute hors d’un port non standard, n’oubliez pas de spécifier le port lorsque vous demandez le contenu à partir de votre appareil Android.  Par exemple, si votre serveur web utilise le domaine personnalisé sur le port, lorsque vous affichez le site à partir de votre appareil Android, vous devez utiliser `microsoft-edge.devtools` `7331` l’URL `microsoft-edge.devtools:7331` .  

> [!TIP]
> Pour reprendre la navigation normale, n’oubliez pas de revenir aux paramètres proxy de votre appareil Android après vous être déconnecté de l’ordinateur de développement.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Commencer à déboguer à distance les appareils Android | Documents Microsoft"  

[CharlesWebDebuggingProxy]: https://www.charlesproxy.com "Proxy de débogage Web Charles"  

[SquidOptimisingWebDelivery]: https://www.squid-cache.org "programme d’optimisation de la distribution web"  

[FiddlerWebDebuggingProxy]: https://www.telerik.com/fiddler "Fiddler - Proxy de débogage web gratuit"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est trouvée ici et est co-auteure par [Les Basques DeCénais (Rédacteur][KayceBasques] technique, Chrome DevTools \& Writer\) et [Meggin Kearney][MegginKearney] \(Tech Writer\). [](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
