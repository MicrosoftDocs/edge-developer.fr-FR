---
description: Utilisez l’outil Multimédia pour afficher les informations et déboguer les joueurs multimédias par onglet de navigateur.
title: Afficher et déboguer les informations des joueurs multimédias
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 0d2a60c31d5239a4b47102ae96a713b8bfcf46f3
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564062"
---
<!-- Copyright Jecelyn Yeen

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="view-and-debug-media-players-information"></a>Afficher et déboguer les informations des joueurs multimédias  

Utilisez **l’outil Media** dans Microsoft Edge DevTools pour afficher les informations et déboguer les joueurs multimédias par onglet de navigateur.  

## <a name="open-the-media-tool"></a>Ouvrir l’outil Multimédia  

**L’outil** Media est l’endroit principal dans DevTools pour l’inspection du lecteur multimédia d’une page web.

1.  [Ouvrez DevTools][DevtoolsGuideChromiumOpen].  
1.  Pour ouvrir le **panneau Média,** choisissez **Personnaliser et contrôler les outils DevTools** `...`  >  **More**  >  **Media**.  
    
    :::image type="complex" source="../media/media-panel-empty.msft.png" alt-text="Panneau multimédia" lightbox="../media/media-panel-empty.msft.png":::
       **Panneau** multimédia  
    :::image-end:::  
    
## <a name="view-media-players-information"></a>Afficher les informations des joueurs multimédias  

1.  Accédez à une page web avec un lecteur multimédia, tel que la page web suivante.  
    
    [Optimisation de la productivité avec les outils de développement Edge][BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]  
    
1.  Sous le menu **Joueurs,** un lecteur multimédia s’affiche.  
1.  Choisissez le joueur.  Le **panneau Propriétés** affiche les propriétés du lecteur multimédia.  
    
    :::image type="complex" source="../media/media-panel-view.msft.png" alt-text="Propriétés multimédias" lightbox="../media/media-panel-view.msft.png":::
       Propriétés multimédias  
    :::image-end:::  
    
1.  Pour afficher tous les événements du lecteur multimédia, choisissez le panneau **Événements.**  
    
    :::image type="complex" source="../media/media-panel-events.msft.png" alt-text="Événements multimédias" lightbox="../media/media-panel-events.msft.png":::
       Événements multimédias  
    :::image-end:::  
    
1.  Pour afficher les journaux des messages du lecteur multimédia, sélectionnez le **panneau Messages.**  Vous pouvez filtrer les messages par niveau de journal ou chaîne.  
    
    :::image type="complex" source="../media/media-panel-messages.msft.png" alt-text="Messages multimédias" lightbox="../media/media-panel-messages.msft.png":::
       Messages multimédias  
    :::image-end:::  
    
1.  Dans le **panneau Chronologie,** l’état de la lecture multimédia et de la mémoire tampon est affiché en direct.  
    
    :::image type="complex" source="../media/media-panel-timeline.msft.png" alt-text="Chronologie des médias" lightbox="../media/media-panel-timeline.msft.png":::
       Chronologie des médias  
    :::image-end:::  
    
### <a name="remote-debugging"></a>Débogage à distance  

Affichez les informations des joueurs multimédias sur un appareil Android à partir de Windows ou macOS.  

1.  Pour configurer le débogage à distance, accédez à Commencer avec le [débogage à distance des appareils Android.][DevtoolsGuideChromiumRemoteDebuggingIndex]  
1.  Afficher les informations des joueurs multimédias à distance.  
    
    <!-- TODO: recreate image using an Android device -->  
    <!--  
    :::image type="complex" source="../media/media-panel-remote-debug.msft.png" alt-text="Remote debugging" lightbox="../media/media-panel-remote-debug.msft.png":::
       Remote debugging  
    :::image-end:::  
    -->  
    
## <a name="hide-and-show-media-players"></a>Masquer et afficher les joueurs multimédias  

Parfois, vous exécutez plusieurs lecteur multimédia sur une page web ou utilisez le même onglet de navigateur pour parcourir différentes pages web, chacune avec des lecteur multimédia.

Vous pouvez choisir de masquer \(ou afficher\) chaque lecteur multimédia pour une expérience de débogage plus facile.  

1.  Accédez à plusieurs pages web vidéo différentes à l’aide du même onglet de navigateur.  
1.  Pour masquer les joueurs multimédias, effectuer l’une des actions suivantes.  
    *   Pour masquer un lecteur multimédia, pointez sur un lecteur multimédia, ouvrez le menu contextuel \(clic droit\), puis choisissez **Masquer le lecteur.**  
    *   Pour masquer tous les autres joueurs multimédias, pointez sur un lecteur multimédia, ouvrez le menu contextuel \(clic droit\), puis choisissez **Masquer tous les autres.**  
    
    :::image type="complex" source="../media/media-panel-hide-show.msft.png" alt-text="Masquer les joueurs multimédias" lightbox="../media/media-panel-hide-show.msft.png":::
       Masquer les joueurs multimédias  
    :::image-end:::  
    
## <a name="export-media-player-information"></a>Exporter les informations du lecteur multimédia  

1.  Pour télécharger les informations du lecteur multimédia en tant que fichier JSON, pointez sur un lecteur multimédia, ouvrez le menu contextuel \(clic droit\), puis choisissez Enregistrer les informations **du lecteur.**  
    
    :::image type="complex" source="../media/media-panel-save.msft.png" alt-text="Exporter des informations multimédias" lightbox="../media/media-panel-save.msft.png":::
       Exporter des informations multimédias  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Ouvrez Microsoft Edge (Chromium) DevTools | Documents Microsoft"  

[DevtoolsGuideChromiumRemoteDebuggingIndex]: ../remote-debugging/index.md "Commencer à déboguer à distance les appareils Android | Documents Microsoft"  

[BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]: https://www.bing.com/videos/search?view=detail&mid=DE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8 "Optimisation de la productivité avec les outils de développement Edge | Bing Vidéo"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  

