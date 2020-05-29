---
title: Afficher les ressources de page avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 0977d0a9132c19742c3337f9dc0c3e1240508a3d
ms.sourcegitcommit: 4c24edbd1c591914cb4109511534851570a614cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611916"
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





# Afficher les ressources de page avec Microsoft Edge DevTools   

  

Ce guide vous explique comment utiliser Microsoft Edge DevTools pour afficher les ressources d’une page Web.  Les ressources sont les fichiers nécessaires à une page pour s’afficher correctement.  Les exemples de ressources incluent les fichiers CSS, JavaScript et HTML, ainsi que les images.  

Ce guide suppose que vous êtes familiarisé avec les notions de base du [développement Web][MDNLearnWebDevelopment] et de [Microsoft Edge devtools][MicrosoftEdgeDevTools].  

## Ouvrir les ressources   

Lorsque vous connaissez le nom de la ressource que vous voulez examiner, le **menu de commandes** permet d’ouvrir rapidement la ressource.  

1.  Appuyez sur `Control` + `P` \ (Windows \) ou `Command` + `P` \ (MacOS \).  La boîte de dialogue **ouvrir le fichier** s’ouvre.  
    
    > ##### Figure1  
    > Boîte de dialogue **ouvrir un fichier**  
    > ![Boîte de dialogue Ouvrir un fichier][ImageOpenFile]  
    
1.  Sélectionnez le fichier dans la liste déroulante ou commencez à taper le nom du fichier et appuyez `Enter` une fois que le fichier approprié est mis en surbrillance dans la zone de saisie semi-automatique.  
    
    > ##### Figure 2  
    > Saisie d’un nom de fichier dans la boîte de dialogue **ouvrir un fichier**  
    > ![Saisie d’un nom de fichier dans la boîte de dialogue Ouvrir un fichier][ImageFileSearch]  
    
### Ouvrir ressources dans le panneau réseau   

Voir [inspecter les détails d’une ressource][DevtoolsNetworkInspectDetailsResource].  

> ##### Figure3  
> Examen d’une ressource dans le panneau réseau  
> ![Examen d’une ressource dans le panneau réseau][ImageNetworkResponse]  

### Afficher les ressources dans le panneau réseau à partir d’autres panneaux   

La section [Parcourir les ressources](#browse-resources) ci-dessous vous explique comment afficher les ressources de diverses parties de l’interface utilisateur d’devtools.  Si vous souhaitez inspecter une ressource dans le panneau **réseau** , cliquez avec le bouton droit sur la ressource, puis sélectionnez **afficher dans le panneau réseau**.  

> ##### Figure 4  
> Option **afficher dans le panneau réseau**  
> ![Afficher dans le panneau réseau][ImageRevealNetwork]  

## Parcourir les ressources   

### Parcourir les ressources du panneau réseau   

Voir [enregistrement][DevtoolsNetworkLogActivity]de l’activité du réseau.  

> ##### Figure 5  
> Ressources de page dans le journal réseau  
> ![Ressources de page dans le journal réseau][ImageNetworkLog]  

### Parcourir les répertoires   

Pour afficher les ressources d’une page organisée par annuaire:  

1.  Cliquez sur l’onglet **sources** pour ouvrir le panneau **sources** .  
1.  Cliquez sur l’onglet **page** pour afficher les ressources de la page.  Le volet **page** s’ouvre.  
    
    > ##### Figure 6  
    > Volet **pages**  
    > ![Volet pages][ImagePage]  
    
    Voici une répartition des éléments non évidents de la [figure 6](#figure-6):  
    
    | Élément de page | Description |  
    |:--- |:--- |  
    | `top` | Le contexte de [navigation][MDNInlineFrame]principal du document. |  
    | `airhorner.com` | Le domaine.  Toutes les ressources imbriquées sous celle-ci proviennent du domaine.  Par exemple, il s’agit probablement de l’URL complète du `comlink.global.j` fichier `https://airhorner.com/scripts/comlink.global.js` . |  
    | `scripts` | Un répertoire. |  
    | `(index)` | Le document HTML principal. |  
    | `sw.js` | Contexte du runtime du travailleur de service. |  
    
1.  Cliquez sur une ressource pour l’afficher dans l' **éditeur**.  
    
    > ##### Figure 7  
    > Affichage d’un fichier dans l' **éditeur**  
    > ![Affichage d’un fichier dans l’éditeur][ImageSourcesView]  
    
### Parcourir par nom de fichier   

Par défaut, le volet **page** regroupe les ressources par annuaire.  Pour désactiver ce regroupement et afficher les ressources de chaque domaine sous forme de liste plate:  

1.  Ouvrir le volet de **pages** .  Voir [Parcourir par annuaire](#browse-by-directory).  
1.  Cliquez sur **autres options** `...` et désactivez **l’option regrouper par dossier**.  
    
    > ##### Figure8  
    > Option de **regroupement par dossier**  
    > ![Option de regroupement par dossier][ImageGroupByFolder]  
    
    Les ressources sont organisées par type de fichier.  Dans chaque type de fichier, les ressources sont classées par ordre alphabétique.  
    
    > ##### Figure9  
    > Volet de **page** après la désactivation du **groupe par dossier**  
    > ![Volet de page après la désactivation du groupe par dossier][ImageFileNames]  
    
### Parcourir par type de fichier   

Pour regrouper les ressources en fonction de leur type de fichier:  

1.  Cliquez sur l’onglet **application** .  Le volet de l' **application** s’ouvre.  Par défaut, le volet **manifeste** s’ouvre en premier.  
    
    > ##### Figure10  
    > Panneau **application**  
    > ![Panneau application][ImageApplication]  
    
1.  Faites défiler vers le bas jusqu’au volet **cadres** .  
    
    > ##### Figure11  
    > Volet **cadres**  
    > ![Volet cadres][ImageFrames]  
    
1.  Développez les sections qui vous intéressent.  
1.  Cliquez sur une ressource pour l’afficher.  
    
    > ##### Figure12  
    > Affichage d’une ressource dans le volet de l' **application**  
    > ![Affichage d’une ressource dans le volet de l’application][ImageApplicationView]  

#### Parcourir les fichiers par type dans le panneau réseau   

Voir [Filtrer par type de ressource][DevtoolsNetworkFilterByResourceType].  

> ##### Figure13  
> Filtrage de CSS dans le journal réseau  
> ![Filtrage de CSS dans le journal réseau][ImageCSS]  

<!--  -->  



<!-- image links -->  

[ImageOpenFile]: /microsoft-edge/devtools-guide-chromium/media/resources-command-menu-empty.msft.png "Figure 1: boîte de dialogue Ouvrir un fichier"  
[ImageFileSearch]: /microsoft-edge/devtools-guide-chromium/media/resources-command-menu-file-search.msft.png "Figure 2: saisie d’un nom de fichier dans la boîte de dialogue Ouvrir un fichier"  
[ImageNetworkResponse]: /microsoft-edge/devtools-guide-chromium/media/resources-network-response.msft.png "Figure 3: inspection d’une ressource dans le panneau * * Network * *"  
[ImageRevealNetwork]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-reveal-in-network-panel.msft.png "Figure 4: affichage dans le panneau réseau"  
[ImageNetworkLog]: /microsoft-edge/devtools-guide-chromium/media/resources-network-resources.msft.png "Figure 5: ressources de page dans le journal réseau"  
[ImagePage]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-empty.msft.png "Figure 6: volet pages"  
[ImageSourcesView]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resource.msft.png "Figure 7: affichage d’un fichier dans l’éditeur"  
[ImageGroupByFolder]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resource-group-by-folder.msft.png "Figure 8: option regroupement par dossier"  
[ImageFileNames]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png "Figure 9: volet pages après la désactivation de l’ensemble des dossiers"  
[ImageApplication]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner.msft.png "Figure 10: volet de l’application"  
[ImageFrames]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner-frames-expanded.msft.png "Figure 11: volet cadres"  
[ImageApplicationView]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner-expanded-resources.msft.png "Figure 12: affichage d’une ressource dans le volet de l’application"  
[ImageCSS]: /microsoft-edge/devtools-guide-chromium/media/resources-network-resources-filter-css.msft.png "Figure 13: filtrage de CSS dans le journal réseau"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome)"  
[DevtoolsNetworkFilterByResourceType]: /microsoft-edge/devtools-guide-chromium/network/index#filter-by-resource-type "Filtrer par type de ressource: inspecter l’activité réseau dans Microsoft Edge DevTools"  
[DevtoolsNetworkInspectDetailsResource]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Inspecter les détails de l’activité réseau d’examen des ressources dans Microsoft Edge DevTools"  
[DevtoolsNetworkLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Journalisation de l’activité du réseau-Inspectez l’activité réseau dans Microsoft Edge DevTools"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<iframe>: élément de cadre inséré | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Découvrir le développement Web | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/resources/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
