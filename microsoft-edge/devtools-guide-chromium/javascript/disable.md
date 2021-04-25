---
description: Ouvrez le menu Commande et exécutez la commande « Désactiver JavaScript ».
title: Désactiver JavaScript avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 665181b14e6fa5e86950a27822d52395f49f5b92
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519351"
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

# <a name="disable-javascript-with-microsoft-edge-devtools"></a>Désactiver JavaScript avec Microsoft Edge DevTools  

Pour examiner le rendu de votre page web lorsqu'un navigateur ne prend pas en charge JavaScript, éteinez temporairement JavaScript.

Effectuer les actions suivantes pour examiner la façon dont une page web s'affiche et se comporte lorsque vous éteinez JavaScript.  

1.  [Ouvrez Microsoft Edge DevTools.][DevToolsOpen]  
1.  Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) pour ouvrir le **menu Commande.**  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="Menu Commande" lightbox="../media/javascript-console-command.msft.png":::
       Menu **Commande**  
    :::image-end:::  
    
1.  Commencez à `javascript` taper, choisissez **Désactiver JavaScript,** puis `Enter` sélectionnez pour exécuter la commande.  JavaScript est désormais désactivé.  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="Choose Disable JavaScript in the Command Menu" lightbox="../media/javascript-console-command-javascript.msft.png":::
       Choose **Disable JavaScript** in the **Command Menu**  
    :::image-end:::  
    
    L'icône d'avertissement jaune en de côté **des sources** vous rappelle que JavaScript est désactivé.  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="Icône d'avertissement en de côté des sources" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       Icône d'avertissement en de côté des **sources**  
    :::image-end:::  
    
JavaScript reste désactivé dans l'onglet tant que DevTools est ouvert.  

Vous souhaitez peut-être actualiser la page pour examiner si et comment la page web dépend de JavaScript lors du chargement.  

Pour ré-activer JavaScript, effectuer les actions suivantes.  

*   Ouvrez **de nouveau le menu Commande** et exécutez la `Enable JavaScript` commande.  
*   Fermez DevTools.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpen]: ../open/index.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
