---
description: Ouvrez l’outil de rendu et sélectionnez Émuler le support CSS > imprimer.
title: Forcer Microsoft Edge DevTools en mode Aperçu avant impression (type de média d’impression CSS)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 6c49d956a9a7185b162ca8e2996e7b3e715b40ab
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564426"
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
# <a name="force-microsoft-edge-devtools-into-print-preview-mode"></a>Forcer Microsoft Edge DevTools en mode Aperçu avant impression  

La [requête de média d’impression][MDNUsingMediaQueries] contrôle l’apparence de votre page lors de l’impression.  Pour forcer votre page en mode Aperçu avant impression :  

1.  Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) pour ouvrir le **menu Commande.**  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menu Commande" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       Menu **Commande**  
    :::image-end:::  
    
1.  `rendering`Tapez, choisissez Afficher le **rendu,** puis sélectionnez `Enter` .  
1.  Under **Emulate CSS media**, choose **print**.  
    
    :::image type="complex" source="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png" alt-text="Mode Aperçu avant impression" lightbox="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png":::
       Mode Aperçu avant impression  
    :::image-end:::  
    
À partir de là, vous pouvez afficher et modifier votre CSS, comme n’importe quelle autre page web.  Accédez à [Prise en main avec l’affichage et la modification du CSS.][DevToolsCSSGetStarted]  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  
[DevToolsCSSGetStarted]: ./index.md "Commencer à afficher et modifier les | Documents Microsoft"  

[MDNUsingMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Utilisation de requêtes multimédias | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
