---
title: Recherchez et corrigez les problèmes liés à l’outil problèmes dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 394ea0e831e3b60a60a149d1281c5cca382a887d
ms.sourcegitcommit: ba9f0ed77e84174b03262b17e62c6a7e26cfeb3d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/30/2020
ms.locfileid: "10688128"
---
<!-- Copyright Sam Dutton 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  





# Recherchez et corrigez les problèmes liés à l’outil problèmes dans Microsoft Edge DevTools   



L’outil **problèmes** dans Microsoft Edge devtools réduit la fatigue et l’encombrement de la **console**.  Utilisez-le pour trouver des solutions aux problèmes détectés par le navigateur, tels que les problèmes liés aux cookies et au contenu mixte.  

> [!NOTE]
> Dans Microsoft Edge 84, l’outil **problèmes** prend en charge trois types de problème:  
> *   [Problèmes de cookie][MDNSameSiteCookies]  
> *   [Contenu mixte][MDNMixedContent]  
> *   [Problèmes COEP][W3CCOEPSpec]
> 
> L’équipe Microsoft Edge DevTools envisage de prendre en charge davantage de types de problèmes dans les futures versions de Microsoft Edge.  

## Ouvrir l’outil de problèmes dans le tiroir DevTools   

1.  Rendez-vous sur une page telle que [samesite-sandbox.glitch.me][GlitchSamesiteSandbox], qui comporte des problèmes de correction.  
1.  [Ouvrez devtools][DevtoolsOpen].  
1.  :::row:::
       :::column span="":::
          Cliquez sur le bouton **accéder aux problèmes** dans la barre d’avertissement jaune.  
          
          :::image type="complex" source="../media/issues-open-issues-tab.msft.png" alt-text="Accéder au bouton problèmes dans la barre d’avertissement jaune lorsque des problèmes sont détectés" lightbox="../media/issues-open-issues-tab.msft.png":::
             Figure1.  Dans la barre d’avertissement jaune, **accédez au bouton accéder aux problèmes** pour détecter des problèmes.  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Vous pouvez également sélectionner **problèmes** dans le menu **autres outils** .  
          
          :::image type="complex" source="../media//issues-more-tools-menu.msft.png" alt-text="Outil problèmes dans le menu plus d’outils" lightbox="../media//issues-more-tools-menu.msft.png":::
             Figure2.  Outil **problèmes** dans le menu **plus d’outils**  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  Cliquez sur le bouton **recharger la page** , si nécessaire.  
    
    :::image type="complex" source="../media/issues-tab-before-refresh.msft.png" alt-text="Outil problèmes dans le tiroir DevTools avec le bouton recharger la page" lightbox="../media/issues-tab-before-refresh.msft.png":::
       Figure3.  Outil **problèmes** dans le tiroir devtools avec le bouton **recharger la page**  
    :::image-end:::  

    Les problèmes signalés dans la **console** sont relativement difficiles à comprendre, tels que les avertissements de cookie dans l’image suivante.  En fonction des problèmes signalés, il est possible que vous n’ayez pas besoin d’effacer ce que vous devez faire.  
    
    :::image type="complex" source="../media/issues-tab-after-refresh.msft.png" alt-text="Outil problèmes dans le tiroir DevTools avec trois problèmes de cookie" lightbox="../media/issues-tab-after-refresh.msft.png":::
       Figure4.  Outil **problèmes** dans le tiroir devtools avec trois problèmes de cookie  
    :::image-end:::  
    
## Afficher les éléments dans l’outil Erreurs   

L’outil de **problèmes** du tiroir devtools présente des avertissements de manière structurée, agrégée et exploitable.  

1.  Pour obtenir des instructions sur la façon de résoudre le problème et de trouver les ressources affectées, sélectionnez un élément dans l’outil **problèmes** .  
    
    :::image type="complex" source="../media/issues-tab-issue-open.msft.png" alt-text="Marquer des cookies intersites comme un problème de sécurité ouvrir dans l’outil problèmes" lightbox="../media/issues-tab-issue-open.msft.png":::
       Figure5.  **Marquer des cookies intersites comme** un problème de sécurité ouvrir dans l’outil **problèmes**  
    :::image-end:::  
    
    Chaque article comporte quatre composants:  
    
    *   Titre décrivant le problème.  
    *   Une description fournissant le contexte et la solution.  
    *   Section **ressources affectées** qui comporte des liens vers des ressources au sein du contexte devtools approprié, tel que le panneau réseau.  
    *   Des liens vers des conseils supplémentaires.  
    
1.  Sélectionnez les éléments des **ressources affectées** pour afficher les détails.  Dans l’exemple suivant, l' **option marquer les cookies intersites comme problème sécurisé** affecte un cookie et deux requêtes.  
    
    :::image type="complex" source="../media/issues-tab-affected-resources.msft.png" alt-text="Les ressources affectées sont ouvertes dans l’onglet tiroir de problèmes" lightbox="../media/issues-tab-affected-resources.msft.png":::
       Figure6.  Ressources concernées ouvertes dans l’outil **problèmes** du tiroir-devtools  
    :::image-end:::  
    
## Afficher les problèmes en contexte   

1.  Sélectionnez un lien vers une ressource pour afficher l’élément dans le contexte approprié dans DevTools.  Dans l’exemple suivant, sélectionnez `samesite-sandbox.glitch.me` sous **demandes** pour afficher les cookies joints à cette demande.  
    
    :::image type="complex" source="../media/issues-tab-view-request.msft.png" alt-text="Afficher le cookie affecté dans le volet réseau de DevTools" lightbox="../media/issues-tab-view-request.msft.png":::
       Figure7.  Afficher le cookie affecté dans le volet réseau de DevTools  
    :::image-end:::  

1.  Faites défiler pour afficher l’élément présentant un problème: pour l’exemple suivant, le `ck02` cookie.  Positionnez le pointeur sur la colonne **SameSite** pour afficher la `None` valeur du problème détecté.  
    
    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="Valeur None dans la colonne SameSite pour le cookie ck02 dans le panneau réseau d’DevTools" lightbox="../media/issues-tab-view-issue.msft.png":::
       Figure8.  `None` la valeur de la colonne **SameSite** pour le `ck02` cookie dans le volet **réseau** devtools  
    :::image-end:::  

<!--## Feedback  -->  



<!-- image links -->  

<!-- links -->  

[DevtoolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  

[GlitchSamesiteSandbox]: https://samesite-sandbox.glitch.me "Tests de cookies SameSite | Problème"  

[MDNSameSiteCookies]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite "Cookies SameSite | MDN"  
[MDNMixedContent]: https://developer.mozilla.org/docs/Web/Security/Mixed_content "Contenu mixte | MDN"  

[W3CCOEPSpec]: https://wicg.github.io/cross-origin-embedder-policy "Stratégie d’intégration d’une origination Groupe de communauté d’incubateur Web"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/issues/index) et est créée par [Sam Dutton][SamDutton] \ (défenseur du développeur \).  
[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[SamDutton]: https://developers.google.com/web/resources/contributors/samdutton  
