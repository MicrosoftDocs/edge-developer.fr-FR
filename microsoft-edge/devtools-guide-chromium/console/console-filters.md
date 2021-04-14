---
description: Découvrez comment filtrer des messages de console
title: Mise en place du filtrage des messages dans la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: b493bb790b48bc1c4dca0e6802d2f638099b7644
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483429"
---
# <a name="filter-console-messages"></a>Filtrer les messages de la console  

Lorsque vous naviguez sur le web, il se peut que vous trouviez que la **console** est submergée de toutes sortes d'informations.  Souvent, les informations ne sont pas pertinentes pour vous.  Telles que des informations sur le projet en direct qu'un autre développeur a journalisé pendant le débogage.  Ou plus d'informations sur les violations et avertissements concernant les performances du site actuel que vous ne pouvez pas modifier.  Il est logique d'utiliser les options de filtre de **console** pour réduire le bruit.  

## <a name="filter-by-log-level"></a>Filtrer par niveau de journal  

Chaque méthode de l'objet est attachée à un niveau `console` de gravité.  Les niveaux de gravité `Verbose` sont `Info` , ou `Warning` `Error` .  Affichez les niveaux de gravité dans la [documentation de l'API.][DevtoolsConsoleApi]  Par exemple, `console.log()` il s'agit `Info` d'un message de niveau -level, mais `console.error()` `Error` d'un message de niveau -.  

Pour filtrer des messages dans **la console,** utilisez le menu déroulant Log **Level.**  Vous pouvez faire bascule l'état de chaque niveau.  Pour désactiver chaque niveau, supprimez la coche en regard de chaque niveau.  

:::image type="complex" source="../media/console-filter-dropdown.msft.png" alt-text="Le menu déroulant filtre les messages de la console à l'aide du niveau de journal" lightbox="../media/console-filter-dropdown.msft.png":::
    Le menu déroulant filtre les messages **de la console** à l'aide du niveau de journal  
:::image-end:::  

Étant donné qu'aucun filtre n'est appliqué, la figure suivante affiche des dizaines de messages.  Ensuite, réduisez et gérez le nombre de messages.  

:::image type="complex" source="../media/console-filter-displays-all.msft.png" alt-text="Aucun ensemble de filtres signifie que vous pouvez afficher de nombreux messages de console" lightbox="../media/console-filter-displays-all.msft.png":::
    Aucun ensemble de filtres signifie que vous pouvez afficher de nombreux messages de console  
:::image-end:::  

Choisissez de masquer tous les messages de niveau Avertissement pour réduire le bruit.  Accédez à la dropdown **Log Levels** et décochez le `Warnings` niveau.  

:::image type="complex" source="../media/console-filter-hide-warning.msft.png" alt-text="Masquer tous les messages de niveau d'avertissement dans la console pour filtrer une grande partie du bruit" lightbox="../media/console-filter-hide-warning.msft.png":::
    Masquer tous les messages de niveau d'avertissement dans la **console** pour filtrer une grande partie du bruit  
:::image-end:::  

## <a name="filter-by-text"></a>Filtrer par texte  

Si vous souhaitez examiner plus en détail, pour filtrer les messages à l'aide de texte, tapez une chaîne dans la **boîte de** texte Filtrer.  Par exemple, tapez dans la zone pour afficher uniquement les messages concernant le chargement des ressources de blocage `block` du navigateur.

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Affiche les messages qui contiennent le bloc de mots" lightbox="../media/console-filter-text.msft.png":::
    Affiche les messages qui contiennent le mot `block`  
:::image-end:::  

## <a name="filter-by-regular-expression"></a>Filtrer par expression régulière

[Les expressions régulières][MdnDocsWebJavascriptGuideRegularExpressions] sont un moyen puissant de filtrer des messages.  Par exemple, tapez `/^Tracking/` dans la boîte de texte **Filtrer** pour afficher uniquement les messages qui commencent par le terme `Tracking` .  Si vous ne connaissez pas les expressions régulières, [RegExr][|::ref1::|Main] est une excellente ressource pour en savoir plus sur l'utilisation des expressions régulières.

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Affiche les messages qui commencent par le filtre word à l'aide d'une expression régulière dans la boîte de texte Filtrer" lightbox="../media/console-filter-regex.msft.png":::
    Affiche les messages qui commencent par le mot à `filter` l'aide d'une expression régulière dans la **boîte** de texte Filtrer  
:::image-end:::  

## <a name="filter-by-message-source"></a>Filtrer par source de message  

Vous pouvez également définir le type de messages à afficher et l'origine de chacun d'eux à l'aide de la barre latérale **de** la **console.**  Pour ce faire, sélectionnez le bouton Afficher la **barre latérale de la console.**  

:::image type="complex" source="../media/console-filter-sidebar-icon.msft.png" alt-text="Pour ouvrir la barre latérale, sélectionnez l'icône Barre latérale" lightbox="../media/console-filter-sidebar-icon.msft.png":::
    Pour ouvrir la barre **latérale,** choisissez le bouton Afficher la **barre latérale de la console**  
:::image-end:::  

Lorsque la **barre latérale est** ouverte, vous pouvez afficher le nombre global de messages et l'origine de chacun d'eux.  Les options sont `All messages` , , , et `User Messages` `Errors` `Warnings` `Info` `Verbose` .  

:::image type="complex" source="../media/console-filter-sidebar-open.msft.png" alt-text="La barre latérale de la console affiche les différentes sources d'origine des messages" lightbox="../media/console-filter-sidebar-open.msft.png":::
    La **barre latérale de la console** affiche les différentes sources d'origine des messages  
:::image-end:::  

Choisissez l'une des options pour afficher uniquement les messages de ce type.  Par exemple, pour afficher les messages des utilisateurs, choisissez l'option de messages de l'utilisateur pour afficher moins de bruit.

:::image type="complex" source="../media/console-filter-select-user-messages.msft.png" alt-text="Choisir d'afficher uniquement les messages utilisateur dans la console à l'aide du filtre dans la barre latérale" lightbox="../media/console-filter-select-user-messages.msft.png":::
    Choisir d'afficher uniquement les messages utilisateur dans la **console** à l'aide du filtre dans la **barre latérale**  
:::image-end:::  

Pour filtrer davantage et développer le choix, choisissez l'icône de triangle en de côté.  Ainsi, vous obtenez plus de choix pour afficher uniquement les messages provenant d'une source spécifique.  

:::image type="complex" source="../media/console-filter-sidebar-open-arrow.msft.png" alt-text="Choisir l'icône de flèche développe chacune des sections" lightbox="../media/console-filter-sidebar-open-arrow.msft.png":::
    Choisir l'icône de flèche développe chacune des sections  
:::image-end:::  

:::image type="complex" source="../media/console-filter-user-message-by-source.msft.png" alt-text="Choisir l'une des nouvelles options de filtrage à l'aide du type et de la source" lightbox="../media/console-filter-user-message-by-source.msft.png":::
    Choisir l'une des nouvelles options de filtrage à l'aide du type et de la source  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Référence de l'API de console | Documents Microsoft"  

[MdnDocsWebJavascriptGuideRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Expressions régulières | MDN"  

[RegExrMain]: https://regexr.com "RegExr"  
