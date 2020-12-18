---
description: Organisez les ressources par cadre, domaine, type ou d’autres critères.
title: Afficher les ressources de page avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 353c36a9d98dac287c3fdaaa3feed2fe3b17cd07
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230774"
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

1.  Sélectionnez `Control` + `P` \ (Windows, Linux \) ou `Command` + `P` \ (MacOS \).  La boîte de dialogue **ouvrir le fichier** s’ouvre.  
    
    :::image type="complex" source="../media/resources-command-menu-empty.msft.png" alt-text="Boîte de dialogue Ouvrir un fichier" lightbox="../media/resources-command-menu-empty.msft.png":::
       Boîte de dialogue **ouvrir un fichier**  
    :::image-end:::  
    
1.  Sélectionnez le fichier dans la liste déroulante ou commencez à taper le nom du fichier et sélectionnez `Enter` une fois que le fichier approprié est mis en surbrillance dans la zone de saisie semi-automatique.  
    
    :::image type="complex" source="../media/resources-command-menu-file-search.msft.png" alt-text="Tapez un nom de fichier dans la boîte de dialogue Ouvrir un fichier" lightbox="../media/resources-command-menu-file-search.msft.png":::
       Tapez un nom de fichier dans la boîte de dialogue **ouvrir un fichier**  
    :::image-end:::  
    
### Ouvrir ressources dans le panneau réseau  

Accédez à [inspecter les détails d’une ressource][DevtoolsNetworkInspectDetailsResource].  

:::image type="complex" source="../media/resources-network-response.msft.png" alt-text="Inspecter une ressource dans le panneau réseau" lightbox="../media/resources-network-response.msft.png":::
   Inspecter une ressource dans le panneau **réseau**  
:::image-end:::  

### Afficher les ressources dans le panneau réseau à partir d’autres panneaux  

La section [Parcourir les ressources](#browse-resources) ci-dessous vous explique comment afficher les ressources de diverses parties de l’interface utilisateur d’devtools.  Si vous souhaitez inspecter une ressource dans le panneau **réseau** , cliquez avec le bouton droit sur la ressource, puis sélectionnez **afficher dans le panneau réseau**.  

:::image type="complex" source="../media/resources-sources-page-reveal-in-network-panel.msft.png" alt-text="Afficher dans le panneau réseau" lightbox="../media/resources-sources-page-reveal-in-network-panel.msft.png":::
   **Afficher dans le panneau réseau**  
:::image-end:::  

## Parcourir les ressources  

### Parcourir les ressources du panneau réseau  

Naviguez jusqu’à [log Activity Network][DevtoolsNetworkLogActivity].  

:::image type="complex" source="../media/resources-network-resources.msft.png" alt-text="Ressources de page dans le journal réseau" lightbox="../media/resources-network-resources.msft.png":::
   Ressources de page dans le journal **réseau**  
:::image-end:::  

### Parcourir les répertoires  

Pour afficher les ressources d’une page organisée par annuaire:  

1.  Cliquez sur l’onglet **sources** pour ouvrir le panneau **sources** .  
1.  Cliquez sur l’onglet **page** pour afficher les ressources de la page.  Le volet **page** s’ouvre.  
    
    :::image type="complex" source="../media/resources-sources-page-empty.msft.png" alt-text="Le volet des pages" lightbox="../media/resources-sources-page-empty.msft.png":::
       Le volet des **pages**  
    :::image-end:::  
    
    Voici une répartition des éléments non évidents de la figure précédente.  
    
    | Élément de page | Description |  
    |:--- |:--- |  
    | `top` | Le contexte de [navigation][MDNInlineFrame]principal du document. |  
    | `airhorner.com` | Le domaine.  Toutes les ressources imbriquées sous celle-ci proviennent du domaine.  Par exemple, il s’agit probablement de l’URL complète du `comlink.global.j` fichier `https://airhorner.com/scripts/comlink.global.js` . |  
    | `scripts` | Un répertoire. |  
    | `(index)` | Le document HTML principal. |  
    | `sw.js` | Contexte du runtime du travailleur de service. |  
    
1.  Cliquez sur une ressource pour l’afficher dans l' **éditeur**.  
    
    :::image type="complex" source="../media/resources-sources-page-resource.msft.png" alt-text="Afficher un fichier dans l’éditeur" lightbox="../media/resources-sources-page-resource.msft.png":::
       Afficher un fichier dans l' **éditeur**  
    :::image-end:::  
    
### Parcourir par nom de fichier  

Par défaut, le volet **page** regroupe les ressources par annuaire.  Pour désactiver ce regroupement et afficher les ressources de chaque domaine sous forme de liste plate:  

1.  Ouvrir le volet de **pages** .  Naviguez jusqu’à [l’annuaire](#browse-by-directory).  
1.  Cliquez sur **autres options** `...` et désactivez **l’option regrouper par dossier**.  
    
    :::image type="complex" source="../media/resources-sources-page-resource-group-by-folder.msft.png" alt-text="Option de regroupement par dossier" lightbox="../media/resources-sources-page-resource-group-by-folder.msft.png":::
       Option de **regroupement par dossier**  
    :::image-end:::  
    
    Les ressources sont organisées par type de fichier.  Dans chaque type de fichier, les ressources sont classées par ordre alphabétique.  
    
    :::image type="complex" source="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png" alt-text="Volet de page après la désactivation du groupe par dossier" lightbox="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png":::
       Volet de **page** après la désactivation du **groupe par dossier**  
    :::image-end:::  
    
### Parcourir par type de fichier  

Pour regrouper les ressources en fonction de leur type de fichier:  

1.  Cliquez sur l’onglet **application** .  Le volet de l' **application** s’ouvre.  Par défaut, le volet **manifeste** s’ouvre en premier.  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner.msft.png" alt-text="Panneau application" lightbox="../media/resources-application-mainfest-airhorner.msft.png":::
       Panneau **application**  
    :::image-end:::  
    
1.  Faites défiler vers le bas jusqu’au volet **cadres** .  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png" alt-text="Volet cadres" lightbox="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png":::
       Volet **cadres**  
    :::image-end:::  
    
1.  Développez les sections qui vous intéressent.  
1.  Cliquez sur une ressource pour l’afficher.  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png" alt-text="Afficher une ressource dans le volet de l’application" lightbox="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png":::
       Afficher une ressource dans le volet de l' **application**  
    :::image-end:::  
    
#### Parcourir les fichiers par type dans le panneau réseau  

Accédez au [filtre par type de ressource][DevtoolsNetworkFilterByResourceType].  

:::image type="complex" source="../media/resources-network-resources-filter-css.msft.png" alt-text="Filtrer les feuilles CSS dans le journal réseau" lightbox="../media/resources-network-resources-filter-css.msft.png":::
   Filtrer les feuilles CSS dans le journal **réseau**  
:::image-end:::  

## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  
[DevtoolsNetworkFilterByResourceType]: ../network/index.md#filter-by-resource-type "Filtrer par type de ressource: inspecter l’activité réseau dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsNetworkInspectDetailsResource]: ../network/index.md#inspect-the-details-of-the-resource "Inspecter les détails de l’activité du réseau d’examen des ressources dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity "Journalisation de l’activité du réseau-Inspectez l’activité réseau dans Microsoft Edge DevTools | Documents Microsoft"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<iframe>: élément de cadre inséré | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Découvrir le développement Web | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/resources/index) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
