---
description: Utilisez le volet média pour afficher des informations et déboguer les lecteurs multimédias par onglet de navigateur.
title: Afficher et déboguer les informations sur les lecteurs multimédias
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: e6259cf573b76df7e281527ad30360b8f473a165
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230949"
---
# Afficher et déboguer les informations sur les lecteurs multimédias  

Utilisez le panneau **multimédia** dans Microsoft Edge devtools pour afficher des informations et déboguer les lecteurs multimédias par onglet de navigateur.  

## Ouvrir le panneau multimédia  

Le panneau **média** est l’emplacement principal de devtools pour l’examen du lecteur multimédia d’une page Web.

1.  [Ouvrez devtools][DevtoolsGuideChromiumOpen].  
1.  Pour ouvrir le panneau **média** , sélectionnez **personnaliser et contrôler devtools** `...`  >  **plus**de  >  **médias**.  
    
    :::image type="complex" source="../media/media-panel-empty.msft.png" alt-text="Panneau multimédia" lightbox="../media/media-panel-empty.msft.png":::
       Panneau **multimédia**  
    :::image-end:::  
    
## Afficher les informations des lecteurs multimédias  

1.  Accédez à une page Web à l’aide d’un lecteur multimédia, tel que le page Web suivant.  
    
    [Optimisation de la productivité grâce aux outils de développement Edge][BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]  
    
1.  Dans le menu des **joueurs** , un lecteur multimédia est affiché.  
1.  Sélectionnez le joueur.  L’onglet **Propriétés** affiche les propriétés du lecteur multimédia.  
    
    :::image type="complex" source="../media/media-panel-view.msft.png" alt-text="Propriétés du média" lightbox="../media/media-panel-view.msft.png":::
       Propriétés du média  
    :::image-end:::  
    
1.  Pour afficher tous les événements du lecteur multimédia, sélectionnez l’onglet **Events (événements** ).  
    
    :::image type="complex" source="../media/media-panel-events.msft.png" alt-text="Événements multimédias" lightbox="../media/media-panel-events.msft.png":::
       Événements multimédias  
    :::image-end:::  
    
1.  Pour afficher les journaux du message du lecteur multimédia, sélectionnez l’onglet **messages** .  Vous pouvez filtrer les messages par niveau de journal ou chaîne.  
    
    :::image type="complex" source="../media/media-panel-messages.msft.png" alt-text="Messages multimédias" lightbox="../media/media-panel-messages.msft.png":::
       Messages multimédias  
    :::image-end:::  
    
1.  Dans l’onglet **chronologie** , la lecture multimédia et l’état de la mémoire tampon sont affichés en temps réel.  
    
    :::image type="complex" source="../media/media-panel-timeline.msft.png" alt-text="Barre de Planning multimédia" lightbox="../media/media-panel-timeline.msft.png":::
       Barre de Planning multimédia  
    :::image-end:::  
    
### Débogage à distance  

Affichez les informations sur les lecteurs multimédias sur un appareil Android à partir de votre ordinateur Windows ou macOS.  

1.  Pour configurer le débogage à distance, accédez à la rubrique mise [en route des appareils Android de débogage à distance][DevtoolsGuideChromiumRemoteDebuggingIndex].  
1.  Affichez les informations sur les lecteurs multimédias à distance.  
    
    <!-- TODO: recreate image using an Android device -->  
    <!--  
    :::image type="complex" source="../media/media-panel-remote-debug.msft.png" alt-text="Remote debugging" lightbox="../media/media-panel-remote-debug.msft.png":::
       Remote debugging  
    :::image-end:::  
    -->  
    
## Masquer et afficher des lecteurs multimédias  

Vous pouvez parfois exécuter plusieurs lecteurs multimédias sur une page Web ou utiliser le même onglet de navigateur pour parcourir les différentes pages Web, chacune avec des lecteurs multimédias.

Il est possible que vous deviez masquer \ (ou afficher \) chaque lecteur multimédia pour faciliter le débogage.  

1.  Naviguez jusqu’à différentes pages Web vidéo à l’aide de l’onglet de navigateur.  
1.  Pour masquer les lecteurs multimédias, effectuez l’une des actions suivantes.  
    *   Pour masquer un lecteur multimédia, pointez sur un lecteur multimédia, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \) et sélectionnez **masquer le joueur**.  
    *   Pour masquer tous les autres lecteurs multimédias, pointez sur un lecteur multimédia, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \) et sélectionnez **masquer tous les autres**.  
    
    :::image type="complex" source="../media/media-panel-hide-show.msft.png" alt-text="Masquer des lecteurs multimédias" lightbox="../media/media-panel-hide-show.msft.png":::
       Masquer des lecteurs multimédias  
    :::image-end:::  
    
## Exporter des informations sur le lecteur multimédia  

1.  Pour télécharger les informations du lecteur multimédia sous forme de fichier JSON, pointez sur un lecteur multimédia, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez **enregistrer les informations du joueur**.  
    
    :::image type="complex" source="../media/media-panel-save.msft.png" alt-text="Exporter des informations sur le média" lightbox="../media/media-panel-save.msft.png":::
       Exporter des informations sur le média  
    :::image-end:::  
    
## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Ouvrir Microsoft Edge (chrome) DevTools | Documents Microsoft"  

[DevtoolsGuideChromiumRemoteDebuggingIndex]: ../remote-debugging/index.md "Commencer à utiliser le débogage à distance des appareils Android | Documents Microsoft"  

[BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]: https://www.bing.com/videos/search?view=detail&mid=DE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8 "Optimisation de la productivité grâce aux outils de développement Edge | Bing Video"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

