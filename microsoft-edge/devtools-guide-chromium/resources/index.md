---
description: Organisez les ressources par trame, domaine, type ou autre critère.
title: Afficher les ressources de page avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 415ed45bf650aa6800ab674cce74179f783a82c7
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565070"
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
# <a name="view-page-resources-with-microsoft-edge-devtools"></a>Afficher les ressources de page avec Microsoft Edge DevTools  

Ce guide vous apprend à utiliser Microsoft Edge DevTools pour afficher les ressources d’une page web.  Les ressources sont les fichiers dont une page a besoin pour s’afficher correctement.  Les fichiers CSS, JavaScript et HTML sont des exemples de ressources, ainsi que des images.  

Ce guide suppose que vous êtes familiarisé avec les principes de base du développement [web][MDNLearnWebDevelopment] et Microsoft Edge [DevTools][MicrosoftEdgeDevTools].  

## <a name="open-resources"></a>Ouvrir des ressources  

Lorsque vous connaissez le nom de la ressource que vous souhaitez inspecter, le **menu** Commande fournit un moyen rapide d’ouvrir la ressource.  

1.  Sélectionnez `Control` + `P` \(Windows, Linux\) ou `Command` + `P` \(macOS\).  La **boîte de dialogue Ouvrir** un fichier s’ouvre.  
    
    :::image type="complex" source="../media/resources-command-menu-empty.msft.png" alt-text="Boîte de dialogue Ouvrir un fichier" lightbox="../media/resources-command-menu-empty.msft.png":::
       Boîte **de dialogue Ouvrir un** fichier  
    :::image-end:::  
    
1.  Choisissez le fichier dans la zone de dépôt ou commencez à taper le nom du fichier, puis sélectionnez une fois que le fichier correct est mis en surbrillence dans la `Enter` zone de saisie automatique.  
    
    :::image type="complex" source="../media/resources-command-menu-file-search.msft.png" alt-text="Tapez un nom de fichier dans la boîte de dialogue Ouvrir un fichier" lightbox="../media/resources-command-menu-file-search.msft.png":::
       Tapez un nom de fichier dans la boîte **de dialogue Ouvrir un** fichier  
    :::image-end:::  
    
### <a name="open-resources-in-the-network-tool"></a>Ouvrir des ressources dans l’outil Réseau  

Accédez [à Inspecter les détails d’une ressource.][DevtoolsNetworkInspectDetailsResource]  

:::image type="complex" source="../media/resources-network-response.msft.png" alt-text="Inspecter une ressource dans l’outil Réseau" lightbox="../media/resources-network-response.msft.png":::
   Inspecter une ressource dans **l’outil** Réseau  
:::image-end:::  

### <a name="reveal-resources-in-the-network-tool-from-other-panels"></a>Faire apparaître des ressources dans l’outil Réseau à partir d’autres panneaux  

La section [Parcourir les](#browse-resources) ressources ci-dessous vous montre comment afficher les ressources de différentes parties de l’interface utilisateur DevTools.  Si vous souhaitez inspecter une **** ressource dans l’outil Réseau, pointez sur la ressource, ouvrez le menu contextuel \(clic droit\), puis choisissez Révéler dans le **panneau Réseau.**  

:::image type="complex" source="../media/resources-sources-page-reveal-in-network-panel.msft.png" alt-text="Révéler dans le panneau réseau" lightbox="../media/resources-sources-page-reveal-in-network-panel.msft.png":::
   **Révéler dans le panneau réseau**  
:::image-end:::  

## <a name="browse-resources"></a>Parcourir les ressources  

### <a name="browse-resources-in-the-network-panel"></a>Parcourir les ressources dans le panneau Réseau  

Accédez à [Journal de l’activité réseau.][DevtoolsNetworkLogActivity]  

:::image type="complex" source="../media/resources-network-resources.msft.png" alt-text="Ressources de page dans le journal réseau" lightbox="../media/resources-network-resources.msft.png":::
   Ressources de page dans le **journal** réseau  
:::image-end:::  

### <a name="browse-by-directory"></a>Parcourir par répertoire  

Pour afficher les ressources d’une page web organisée par répertoire :  

1.  Ouvrez DevTools.
1.  Choisissez **l’outil Sources,** puis dans le volet **Navigateur** dans le coin supérieur gauche, choisissez **l’onglet Page.**
1.  Choisissez le **bouton Plus d’options** (...) à droite de l’onglet **Page,** puis choisissez **Grouper par dossier.**
    
    :::image type="complex" source="../media/resources-sources-page-empty.msft.png" alt-text="Onglet Page dans le volet Navigateur de l’outil Sources" lightbox="../media/resources-sources-page-empty.msft.png":::
       Onglet **Page** dans le volet **Navigateur** de l’outil **Sources**  
    :::image-end:::  
    
    Voici une répartition des éléments non évidents dans la figure précédente.  
    
    | Élément de page | Description |  
    |:--- |:--- |  
    | `top` | Contexte de [navigation de document principal.][MDNInlineFrame] |  
    | `airhorner.com` | Le domaine.  Toutes les ressources imbrmbrées sous celui-ci proviennent de ce domaine.  Par exemple, l’URL complète du `comlink.global.j` fichier est probablement `https://airhorner.com/scripts/comlink.global.js` . |  
    | `scripts` | Répertoire. |  
    | `(index)` | Document HTML principal. |  
    | `sw.js` | Contexte d’runtime de travail de service. |  
    
1.  Choisissez une ressource pour l’afficher dans **l’Éditeur.**  
    
    :::image type="complex" source="../media/resources-sources-page-resource.msft.png" alt-text="Afficher un fichier dans l’Éditeur" lightbox="../media/resources-sources-page-resource.msft.png":::
       Afficher un fichier dans **l’Éditeur**  
    :::image-end:::  
    
### <a name="browse-by-filename"></a>Parcourir par nom de fichier  

Par défaut, l’onglet **Page** groupe les ressources par répertoire.  Pour afficher les ressources de chaque domaine en tant que liste plate, au lieu de les grouper par répertoire :

1.  Accédez à **l’outil Sources.**  
1.  Dans le **volet Navigateur** (à gauche), choisissez l’onglet **Page.**  
1.  Choisissez **plus d’options,** `...` puis effacer la coche en regard de **Grouper par dossier.**  
    
    :::image type="complex" source="../media/resources-sources-page-resource-group-by-folder.msft.png" alt-text="Option Grouper par dossier" lightbox="../media/resources-sources-page-resource-group-by-folder.msft.png":::
       Option **Grouper par** dossier  
    :::image-end:::  
    
    Les ressources sont organisées par type de fichier.  Dans chaque type de fichier, les ressources sont organisées par ordre alphabétique.  

    :::image type="complex" source="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png" alt-text="Onglet Page après la suppression de la coche Grouper par dossier" lightbox="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png":::
       Onglet **Page après** la suppression de la coche **Grouper par** dossier  
    :::image-end:::  
    
### <a name="browse-by-file-type"></a>Parcourir par type de fichier  

Pour grouper des ressources en fonction de leur type de fichier :  

1.  Sélectionnez **l’onglet** Application.  **L’outil Application** s’ouvre.  Par défaut, **le volet** Manifeste s’ouvre généralement en premier.  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner.msft.png" alt-text="L’outil Application" lightbox="../media/resources-application-mainfest-airhorner.msft.png":::
       **L’outil Application**  
    :::image-end:::  
    
1.  Faites défiler vers le bas **jusqu’au** volet Cadres.  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png" alt-text="Volet Cadres" lightbox="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png":::
       Volet **Cadres**  
    :::image-end:::  
    
1.  Développez les sections qui vous intéressent.  
1.  Choisissez une ressource pour l’afficher.  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png" alt-text="Afficher une ressource dans le panneau Application" lightbox="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png":::
       Afficher une ressource dans le panneau **Application**  
    :::image-end:::  
    
#### <a name="browse-files-by-type-in-the-network-panel"></a>Parcourir les fichiers par type dans le panneau Réseau  

Accédez à [Filtrer par type de ressource.][DevtoolsNetworkFilterByResourceType]  

:::image type="complex" source="../media/resources-network-resources-filter-css.msft.png" alt-text="Filtre pour CSS dans le journal réseau" lightbox="../media/resources-network-resources-filter-css.msft.png":::
   Filtre pour CSS dans le **journal** réseau  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  
[DevtoolsNetworkFilterByResourceType]: ../network/index.md#filter-by-resource-type "Filtrer par type de ressource : inspecter l’activité réseau dans Microsoft Edge devTools | Documents Microsoft"  
[DevtoolsNetworkInspectDetailsResource]: ../network/index.md#inspect-the-details-of-the-resource "Inspecter les détails de la ressource : inspecter l’activité réseau dans Microsoft Edge de | Documents Microsoft"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity "Journal de l’activité réseau : inspecter l’activité réseau dans Microsoft Edge devTools | Documents Microsoft"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<iframe> : l’élément Inline Frame | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "En savoir plus sur les | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/resources/index) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
