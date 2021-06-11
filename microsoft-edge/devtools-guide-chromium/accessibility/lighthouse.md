---
description: Test de l’accessibilité à l’aide de l’outil DevTools.
title: Tester l’accessibilité à l’aide de l’outil Contrôle d’accès
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: bb158085eb516c8d4ce37a22f6b612784db51461
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597396"
---
<!-- this article was created on 05/11/2021 by moving a section out from the "Accessibility reference" article (reference.md) -->
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

# <a name="test-accessibility-using-lighthouse"></a>Tester l’accessibilité à l’aide de l’outil Contrôle d’accès

Vous pouvez utiliser le Contrôle à partir de DevTools pour auditer l’accessibilité d’une page et générer un rapport. Vous pouvez utiliser l’outil Contrôle d’accès pour déterminer :

*   Si une page est correctement marquée pour les lecteurs d’écran.  
*   Si les éléments de texte d’une page ont des coefficients de contraste suffisants à l’aide du s sélectionneur de couleurs. Pour plus d’informations, accédez à Tester le contraste de couleur du texte à [l’aide du s sélectionneur de couleurs.](color-picker.md)   

> [!NOTE]
> **L’outil Îles** fournit des liens vers du contenu hébergé sur des sites web tiers.  Microsoft n’est pas responsable et n’a aucun contrôle sur le contenu de ces sites et les données qui peuvent être collectées.  

Pour auditer une page à l’aide de l’outil Contrôle d’accès, effectuez les étapes suivantes.

1.  Accédez à l’URL que vous souhaitez auditer.
1.  Dans DevTools, sélectionnez **l’outil** DevTools.  Les options de configuration s’affichent.
    
    :::image type="complex" source="../media/accessibility-lighthouse.msft.png" alt-text="Options de configuration de l’ordinateur" lightbox="../media/accessibility-lighthouse.msft.png":::
       Options de configuration de l’ordinateur
    :::image-end:::  
    
1.  Pour **l’appareil,** **sélectionnez Mobile** si vous souhaitez simuler un appareil mobile.  Cette option modifie la chaîne de votre agent utilisateur et resize laport d’affichage.  Cette option peut affecter les résultats de l’audit.
1.  Dans la section **Catégories,** sélectionnez **Accessibilité.**
1.  Sélectionnez **Générer un rapport.** Après 10 à 30 secondes, DevTools affiche un rapport.  Le rapport fournit des conseils sur la façon d’améliorer l’accessibilité de la page.  
    
    :::image type="complex" source="../media/accessibility-lighthouse-result.msft.png" alt-text="Un rapport de classe pour la catégorie Accessibilité" lightbox="../media/accessibility-lighthouse-result.msft.png":::
       Un rapport de classe pour la **catégorie Accessibilité**
    :::image-end:::  
    
1.  Sélectionnez un élément dans le rapport pour en savoir plus à ce sujet.  
    
    :::image type="complex" source="../media/accessibility-lighthouse-result-issue-expanded.msft.png" alt-text="Un problème développé dans un rapport Dente" lightbox="../media/accessibility-lighthouse-result-issue-expanded.msft.png":::
       Un problème développé dans un rapport Dente
    :::image-end:::  
    
1.  Sélectionnez **le lien En savoir** plus pour afficher la documentation du problème.
    
    :::image type="complex" source="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png" alt-text="Afficher la documentation d’un problème" lightbox="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png":::
       Afficher la documentation d’un problème
    :::image-end:::  

1.  Pour revenir aux options de configuration, dans DevTools, **sélectionnez Effectuer un audit** ( `+` ).    


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est sous [licence internationale Creative Commons Attribution 4.0][CCA4IL].  


<!-- links -->  
[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "axe - Test d’accessibilité web - Chrome Web Store"  
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
