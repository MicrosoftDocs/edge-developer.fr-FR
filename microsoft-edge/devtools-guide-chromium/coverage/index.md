---
description: Découvrez comment rechercher et analyser du code JavaScript et CSS inutilisé dans Microsoft Edge DevTools.
title: Rechercher du code JavaScript et CSS inutilisé avec le panneau Couverture dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 2a2d48bda34daa95b9f500c31a12859a1cb08625
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439197"
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

# <a name="find-unused-javascript-and-css-code-with-the-coverage-panel-in-microsoft-edge-devtools"></a>Rechercher du code JavaScript et CSS inutilisé avec le panneau Couverture dans Microsoft Edge DevTools  

Le **panneau** Couverture de Microsoft Edge DevTools vous permet de trouver du code JavaScript et CSS inutilisé.  La suppression du code inutilisé peut accélérer le chargement de votre page et enregistrer les données cellulaires de vos utilisateurs mobiles.  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage.msft.png" alt-text="Analyse de la couverture du code" lightbox="../media/coverage-sources-resource-drawer-coverage.msft.png":::
   Analyse de la couverture du code  
:::image-end:::  

> [!WARNING]
> Il est relativement facile de trouver du code inutilisé.  Toutefois, il peut être difficile de refactoriser une base de code pour que chaque page n’expédie que les fichiers JavaScript et CSS dont elle a besoin.  Ce guide ne couvre pas la refactoriser une base de code pour éviter le code inutilisé, car ces refactoriseurs dépendent fortement de votre pile technologique.  

## <a name="overview"></a>Vue d'ensemble  

La livraison de fichiers JavaScript ou CSS inutilisés est un problème courant dans le développement web.  Par exemple, supposons que vous souhaitez utiliser le composant bouton [Bootstrap][BootstrapButtons] sur votre page.  Pour utiliser le composant de bouton, vous devez ajouter un lien vers la feuille de style Bootstrap dans votre code HTML, comme ceci :  

```html
...
<head>
    ...
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    ...
</head>
...
```  

Cette feuille de style n’inclut pas uniquement le code du composant de bouton.  Il contient le CSS pour **tous les** composants Bootstrap.  Mais vous n’utilisez aucun des autres composants Bootstrap.  Votre page télécharge donc une série de fichiers CSS dont elle n’a pas besoin.  Cette CSS supplémentaire est un problème pour les raisons suivantes.  

*   Le code supplémentaire ralentit le chargement de votre page.  <!--Navigate to [Render-Blocking CSS][render].  -->  
*   Si un utilisateur accède à la page sur un appareil mobile, le code supplémentaire utilise ses données cellulaires.  
    
<!--[render]: /web/fundamentals/performance/critical-rendering-path/render-blocking-css  -->  

## <a name="open-the-coverage-panel"></a>Ouvrir le panneau Couverture  

1.  [Ouvrez le menu Commande.][DevToolsCommandMenu]  
1.  Commencez à `coverage` taper, sélectionnez **la commande Afficher la** couverture, puis `Enter` sélectionnez pour exécuter la commande.  Le **panneau** Couverture s’ouvre dans le **panneau .**  

    :::image type="complex" source="../media/coverage-console-drawer-coverage-empty.msft.png" alt-text="Panneau Couverture" lightbox="../media/coverage-console-drawer-coverage-empty.msft.png":::
       Panneau **Couverture**  
    :::image-end:::  
    
## <a name="record-code-coverage"></a>Couverture du code d’enregistrement  

1.  Choisissez l’un des boutons suivants dans le **panneau Couverture.**  
    *   Choose **Start Instrumenting Coverage and Reload Page** \( Start ![ Instrumenting Coverage and Reload Page ](../media/reload-icon.msft.png) \) if you want to review what code is needed to load the page.  
    *   Choisissez **Instrument Coverage** \( Instrument Coverage \) si vous souhaitez passer en revue le code utilisé après avoir ![ ](../media/record-icon.msft.png) interagi avec la page.  
1.  Choisissez **Arrêter l’instrumentage de la couverture et afficher les résultats** \( Arrêter l’instrumentage de la couverture et afficher les résultats \) lorsque vous souhaitez arrêter l’enregistrement de ![ la couverture de ](../media/stop-icon.msft.png) code.  
    
## <a name="analyze-code-coverage"></a>Analyser la couverture du code  

Le tableau du panneau **Couverture** affiche les ressources qui ont été analysées et la quantité de code utilisée dans chaque ressource.  Choisissez une ligne pour ouvrir cette ressource dans le panneau **Sources** et examiner une répartition ligne par ligne du code utilisé et du code inutilisé.  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage-selected.msft.png" alt-text="Un rapport de couverture de code" lightbox="../media/coverage-sources-resource-drawer-coverage-selected.msft.png":::
   Un rapport de couverture de code  
:::image-end:::  

*   La **colonne URL** est l’URL de la ressource qui a été analysée.  
*   La **colonne Type** indique si la ressource contient CSS, JavaScript ou les deux.  
*   La **colonne Nombre total d’octets** est la taille totale de la ressource en octets.  
*   La **colonne Octets inutilisés** est le nombre d’octets qui n’ont pas été utilisés.  
*   La dernière colonne sans nom est une visualisation des colonnes **Octets** totaux et **Octets inutilisés.**  La section rouge de la barre est des octets inutilisés.  La section verte est utilisée en octets.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Exécuter des commandes avec le menu DevTools Command de Microsoft Edge | Documents Microsoft"  

[BootstrapButtons]: https://getbootstrap.com/docs/4.3/components/buttons "Boutons - Bootstrap"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/coverage/index) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
