---
description: Utilisez l’outil Problèmes pour rechercher et résoudre les problèmes liés à votre site web.
title: Rechercher et résoudre les problèmes liés à Microsoft Edge’outil Problèmes de DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 64954d632416f7d1353269d04c1550ca7a0652b7
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564181"
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
# <a name="find-and-fix-problems-with-the-microsoft-edge-devtools-issues-tool"></a>Rechercher et résoudre les problèmes liés à Microsoft Edge’outil Problèmes de DevTools  

**L’outil Problèmes** dans Microsoft Edge DevTools réduit la fatigue et l’encombrement de la console de **notification.**  Utilisez-le pour rechercher des solutions aux problèmes détectés par le navigateur, tels que les problèmes de cookie et le contenu mixte.  

> [!NOTE]
> Dans Microsoft Edge 84, l’outil **Problèmes** prend en charge trois types de problèmes :  
> *   [Problèmes liés aux cookies][MDNSameSiteCookies]  
> *   [Contenu mixte][MDNMixedContent]  
> *   [Problèmes coEP][W3CCOEPSpec]
> 
> L Microsoft Edge’équipe DevTools prévoit de prendre en charge d’autres types de problèmes dans les futures versions de Microsoft Edge.  

## <a name="open-the-issues-tool-in-the-devtools-drawer"></a>Ouvrir l’outil Problèmes dans le bac DevTools  

1.  Accédez à une page web, telle que [samesite-sandbox.glitch.me][GlitchSamesiteSandbox], qui contient des problèmes à résoudre.  
1.  [Ouvrez DevTools][DevtoolsOpen].  
1.  :::row:::
       :::column span="":::
          Sélectionnez **le bouton Aller aux problèmes** dans la barre d’avertissement jaune.  
          
          :::image type="complex" source="../media/issues-open-issues-tab.msft.png" alt-text="Go to Issues button in yellow warning bar when Issues are detected" lightbox="../media/issues-open-issues-tab.msft.png":::
             Bouton **Go to Issues** (Aller aux problèmes) dans la barre d’avertissement jaune lorsque des problèmes sont détectés.  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Vous pouvez également choisir **Problèmes dans** le menu **Plus d’outils.**  
          
          :::image type="complex" source="../media//issues-more-tools-menu.msft.png" alt-text="Outil Problèmes dans le menu Plus d’outils" lightbox="../media//issues-more-tools-menu.msft.png":::
             **Outil Problèmes dans** le menu **Plus d’outils**  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  Choisissez le **bouton Recharger la page,** si nécessaire.  
    
    :::image type="complex" source="../media/issues-tab-before-refresh.msft.png" alt-text="Outil Problèmes dans le caisse DevTools avec le bouton Recharger la page" lightbox="../media/issues-tab-before-refresh.msft.png":::
       **Outil Problèmes dans** le caisse DevTools avec **le bouton Recharger la page**  
    :::image-end:::  

    Les problèmes signalés dans la **console** sont assez difficiles à comprendre, tels que les avertissements de cookie dans l’image suivante.  En fonction des problèmes signalés, vous ne savez peut-être pas clairement ce que vous devez faire.  
    
    :::image type="complex" source="../media/issues-tab-after-refresh.msft.png" alt-text="Outil Problèmes dans le caisse DevTools avec trois problèmes de cookie" lightbox="../media/issues-tab-after-refresh.msft.png":::
       **Outil Problèmes dans** le caisse DevTools avec trois problèmes de cookie  
    :::image-end:::  
    
## <a name="view-items-in-the-issues-tool"></a>Afficher les éléments dans l’outil Problèmes  

**L’outil Problèmes** du panneau DevTools présente des avertissements de manière structurée, agrégée et actionnable.  

1.  Choisissez un élément dans l’outil Problèmes pour obtenir des **conseils** sur la façon de résoudre le problème et de rechercher les ressources affectées.  
    
    :::image type="complex" source="../media/issues-tab-issue-open.msft.png" alt-text="Marquer les cookies entre sites comme problème sécurisé ouvert dans l’outil Problèmes" lightbox="../media/issues-tab-issue-open.msft.png":::
       **Marquer les cookies entre sites comme problème** sécurisé ouvert dans **l’outil Problèmes**  
    :::image-end:::  
    
    Chaque élément possède quatre composants :  
    
    *   Titre décrivant le problème.  
    *   Description fournissant le contexte et la solution.  
    *   Section **RESSOURCES AFFECTÉEs** qui fait lien vers des ressources dans le contexte DevTools approprié tel que le panneau réseau.  
    *   Liens vers des instructions supplémentaires.  
    
1.  Choisissez des éléments dans **RESSOURCES AFFECTÉEs** pour afficher les détails.  Dans l’exemple suivant, le problème marquer les **cookies** entre sites comme étant sécurisés affecte un cookie et deux demandes.  
    
    :::image type="complex" source="../media/issues-tab-affected-resources.msft.png" alt-text="Ressources affectées ouvertes dans l’outil Problèmes" lightbox="../media/issues-tab-affected-resources.msft.png":::
       Ressources affectées **ouvertes dans l’outil Problèmes** dans le caisse DevTools  
    :::image-end:::  
    
## <a name="view-issues-in-context"></a>Afficher les problèmes en contexte  

1.  Choisissez un lien de ressource pour afficher l’élément dans le contexte approprié dans DevTools.  Dans l’exemple suivant, choisissez `samesite-sandbox.glitch.me` sous **Demandes** pour afficher les cookies joints à cette demande.  
    
    :::image type="complex" source="../media/issues-tab-view-request.msft.png" alt-text="Afficher le cookie affecté dans l’outil Réseau DevTools" lightbox="../media/issues-tab-view-request.msft.png":::
       Afficher le cookie affecté dans l’outil Réseau DevTools ****  
    :::image-end:::  

1.  Faites défiler pour afficher l’élément qui pose problème : pour l’exemple suivant, le `ck02` cookie.  Pointez sur **la colonne SameSite** pour passer en revue la `None` valeur détectée par le problème.  
    
    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="Aucune valeur dans la colonne SameSite pour le cookie ck02 dans l’outil Réseau DevTools" lightbox="../media/issues-tab-view-issue.msft.png":::
       `None` dans la **colonne SameSite** pour le cookie dans l’outil `ck02` Réseau **** DevTools  
    :::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsOpen]: ../open/index.md "Ouvrez Microsoft Edge devTools | Documents Microsoft"  

[GlitchSamesiteSandbox]: https://samesite-sandbox.glitch.me "Tests de cookie SameSite | Glitch"  

[MDNSameSiteCookies]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite "Cookies SameSite | MDN"  
[MDNMixedContent]: https://developer.mozilla.org/docs/Web/Security/Mixed_content "Contenu mixte | MDN"  

[W3CCOEPSpec]: https://wicg.github.io/cross-origin-embedder-policy "Stratégie d’incorporation d’origine croisée | Groupe de Community Web"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est [trouvée ici](https://developers.google.com/web/tools/chrome-devtools/issues/index) et est cochée par [Sam Dutton][SamDutton] \(Developer Advocate\).  
[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[SamDutton]: https://developers.google.com/web/resources/contributors#sam-dutton  
