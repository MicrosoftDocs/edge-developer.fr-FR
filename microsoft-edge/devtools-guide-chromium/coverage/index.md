---
title: Rechercher du code JavaScript et CSS inutilisé avec l’onglet couverture dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 1c03140199b26bca39e69cdfbe33cd1c524257fe
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981857"
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





# Rechercher du code JavaScript et CSS inutilisé avec l’onglet couverture dans Microsoft Edge DevTools   



L’onglet couverture dans Microsoft Edge DevTools vous permet de rechercher du code JavaScript et CSS inutilisé.  La suppression du code inutilisé risque d’accélérer le chargement de la page et d’enregistrer les données cellulaires de vos utilisateurs mobiles.  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage.msft.png" alt-text="Analyser la couverture du code" lightbox="../media/coverage-sources-resource-drawer-coverage.msft.png":::
   Analyser la couverture du code  
:::image-end:::  

> [!WARNING]
> La recherche de code inutilisé est relativement simple.  Toutefois, la refactorisation d’un code base de telle sorte que chaque page expédie uniquement les scripts JavaScript et CSS dont il a besoin risque d’être difficile.  Ce guide ne traite pas de la refactorisation d’un code base pour éviter le code inutilisé, car ces derniers dépendent fortement de votre pile de technologie.  

## Vue d'ensemble   

L’expédition de code JavaScript ou CSS inutilisé est un problème courant du développement Web.  Par exemple, supposons que vous vouliez utiliser le [composant de bouton amorce][BootstrapButtons] sur votre page.  Pour utiliser le composant Button, vous devez ajouter un lien vers la feuille de style bootstrap dans votre code HTML, comme suit:  

```html
...
<head>
    ...
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    ...
</head>
...
```  

Cette feuille de style n’inclut pas uniquement le code du composant Button.  Il contient la feuille de style en cascade (CSS) pour **tous** les composants d’amorce.  Mais vous n’utilisez pas les autres composants d’amorce.  C’est pourquoi votre page télécharge un ensemble de feuilles CSS dont il n’a pas besoin.  Ce code CSS supplémentaire est un problème pour les raisons suivantes.  

*   Le code supplémentaire ralentira le chargement de la page.  <!--See [Render-Blocking CSS][render].  -->  
*   Si un utilisateur accède à la page sur un appareil mobile, le code supplémentaire utilise ses données cellulaires.  
    
<!--[render]: /web/fundamentals/performance/critical-rendering-path/render-blocking-css  -->  

## Ouvrir l’onglet couverture   

1.  [Ouvrir le menu de commandes][DevToolsCommandMenu].  
1.  Commencez `coverage` à taper, sélectionnez la commande **afficher la couverture** , puis appuyez sur `Enter` pour exécuter la commande.  L’onglet **couverture** s’ouvre dans le **tiroir**.  

    :::image type="complex" source="../media/coverage-console-drawer-coverage-empty.msft.png" alt-text="Onglet couverture" lightbox="../media/coverage-console-drawer-coverage-empty.msft.png":::
       Onglet **couverture**  
    :::image-end:::  
    
## Enregistrer la couverture du code   

1.  Cliquez sur l’un des boutons suivants sous l’onglet **couverture** .  
    *   Cliquez sur **Démarrer l’instrumentation, puis rechargez la page** , (démarrez la ![ couverture d’instrumentation et rechargez ][ImageReloadIcon] la page \) si vous souhaitez voir le code nécessaire pour charger la page.  
    *   Cliquez sur couverture de l' **instrument** \ ( ![ couverture de l’instrument ][ImageRecordIcon] \) si vous souhaitez voir le code utilisé après l’interaction avec la page.  
1.  Cliquez sur **arrêter la couverture de l’instrumentation et afficher les résultats** \ ( ![ arrêter l’instrumentation et afficher les résultats ][ImageStopIcon] \) lorsque vous ne souhaitez plus enregistrer la couverture du code.  
    
## Analyser la couverture du code   

La table dans l’onglet **couverture** vous indique les ressources qui ont été analysées et le code utilisé dans chaque ressource.  Cliquez sur une ligne pour ouvrir cette ressource dans le volet **sources** et observez une répartition ligne par ligne du code utilisé et du code inutilisé.  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage-selected.msft.png" alt-text="Rapport de couverture du code" lightbox="../media/coverage-sources-resource-drawer-coverage-selected.msft.png":::
   Rapport de couverture du code  
:::image-end:::  

*   La colonne **URL** correspond à l’URL de la ressource qui a été analysée.  
*   La colonne **type** indique si la ressource contient des éléments CSS ou JavaScript, ou les deux.  
*   La colonne **Total octets** correspond à la taille totale de la ressource en octets.  
*   La colonne **octets inutilisés** correspond au nombre d’octets qui n’ont pas été utilisés.  
*   La dernière colonne sans nom est une visualisation des colonnes **nombre total d’octets** et **octets inutilisés** .  La section rouge de la barre est des octets inutilisés.  La section verte est utilisée en octets.  
    
<!--  
 


-->  

<!-- image links -->  

[ImageReloadIcon]: ../media/reload-icon.msft.png  
[ImageRecordIcon]: ../media/record-icon.msft.png  
[ImageStopIcon]: ../media/stop-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Exécuter des commandes à l’aide du menu de commandes de Microsoft Edge DevTools | Documents Microsoft"  

[BootstrapButtons]: https://getbootstrap.com/docs/4.3/components/buttons "Boutons-démarrage"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/coverage/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
