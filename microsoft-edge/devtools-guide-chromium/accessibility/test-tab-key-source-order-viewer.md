---
description: Pour voir rapidement l’ordre de tabulation des sections d’une page, utilisez l’Observateur de commandes source dans l’outil Accessibilité, à droite de l’onglet Styles.
title: Tester la prise en charge du clavier à l’aide de l’Observateur de commandes source
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 7e90221b581280a6eb63cee4d073622a80871903
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597330"
---
# <a name="test-keyboard-support-using-the-source-order-viewer"></a>Tester la prise en charge du clavier à l’aide de l’Observateur de commandes source

L’ordre source d’un document est important pour la technologie d’assistance et peut être différent de l’ordre dans lequel les éléments apparaissent sur la page rendue.  À l’aide de CSS, vous pouvez ré orderer les éléments de page d’une manière visuelle, mais cela ne signifie pas que les technologies d’assistance telles que les lecteurs d’écran représentent les éléments de page dans le même ordre.  

Pour vous assurer que le document possède **** un ordre logique, vous pouvez utiliser l’Observateur de commandes source pour étiqueter différents éléments de page avec des nombres spécifiant l’ordre dans le code source du document.  **L’Observateur de commandes source** se trouve dans **l’onglet** Accessibilité (près de **l’onglet Styles).**


## <a name="analyzing-the-order-of-keyboard-access-through-sections-of-the-page"></a>Analyse de l’ordre d’accès au clavier par le biais de sections de la page

La page web de démonstration de test d’accessibilité a un ordre de tabulation [contre-intuitif,][DevToolsA11yErrorsDemopage] où les utilisateurs du clavier accèdent au menu de navigation de la barre latérale uniquement après avoir effectué une tabulation sur tous les liens **Plus.**  Le menu de navigation de la barre latérale est destiné à être un raccourci pour atteindre le contenu de la page.  Toutefois, étant donné que vous devez passer par la page entière avant d’atteindre le menu de navigation de la barre latérale, ce menu de navigation est inefficace pour les utilisateurs du clavier.

`Tab`L’ordre de clé de la page de démonstration est le suivante :
1. Le **champ** Recherche, puis le **bouton Aller** pour le **champ** De recherche.
1. Bouton **Plus** dans la section **Chats,** pour accéder à une page web « Chats ».  Ensuite, les **autres boutons Plus,** pour les chiens, la chasse, la capacité, puis les espaces alpacas.
1. Les liens bleus du menu de navigation de la barre latérale : **Chats,** **Chats,** **Chats, Chats,** **Rythme,** puis **Alpacas**.
1. La boîte de texte du don dans le formulaire de don.
1. Les boutons dans la barre de navigation supérieure : **Accueil,** Adopter un enfant de **compagnie,** **Sons,** **Travaux,** puis **À propos de nous**.
1. Interface haut de fenêtre du navigateur.

La raison pour laquelle l’ordre des touches est déroutant est que l’ordre utilisé lors de l’utilisation d’un clavier est déterminé par l’ordre `Tab` source du document.  L’ordre utilisé à l’aide d’un clavier peut être modifié à l’aide de l’attribut sur les éléments, ce qui permet de sortir cet élément de `tabindex` l’ordre source.

Dans le code source du document, le menu de navigation de la barre latérale apparaît après le contenu principal de la page web.  CSS a été utilisé pour positionner le menu de navigation de barre latérale au-dessus de la plupart du contenu principal de la page web. 

Vous pouvez tester l’ordre des éléments de page à l’aide de l’Observateur de commandes **source** dans **l’onglet** Accessibilité.  **L’Observateur de commandes source** est une fonctionnalité expérimentale. Pour plus d’informations, accédez à [l’Observateur de commandes source.](../experimental-features/index.md#source-order-viewer)


Pour activer l’Observateur de commandes source :

1.  Dans DevTools, dans le coin supérieur droit, sélectionnez le **bouton Paramètres** \( Paramètres ![ bouton ](../media/settings-button-icon.msft.png) \).  

1.  Sous **Paramètres,** sélectionnez **Expériences.**  

1.  Cochez la **case De l’Observateur de commandes** source.

1.  Dans le coin supérieur droit de la page **Paramètres** page, sélectionnez **X** pour fermer la page Paramètres page.  En haut de DevTools, les paramètres du message Un ou plusieurs ont changé, ce qui nécessite un **rechargement pour prendre effet.** s’affiche.  Sélectionnez **le bouton Recharger DevTools.**



Pour activer et utiliser l’Observateur de commandes source, avec la page de démonstration :

1.  Ouvrez la [page web de démonstration des tests d’accessibilité][DevToolsA11yErrorsDemopage] dans un nouvel onglet.  Sélectionnez **ensuite F12** pour ouvrir DevTools.

1.  Dans **l’outil Éléments,** à droite de l’onglet **Styles,** sélectionnez **l’onglet** Accessibilité.

1.  Dans la section **Visionneuse de commandes** source, cochez la case Afficher la **commande source.**  Dans la page web rendue, des nombres apparaissent, indiquant l’ordre contrôlé par l’ordre des lignes de `Tab` code dans le fichier source.

1.  Dans l’arborescence DOM de **l’outil Elements,** sélectionnez un élément de disposition principal, tel que `header` l’élément.  Les superpositions numériques sont désormais affichées sur les sections de la page rendue, ce qui indique l’ordre source des différents éléments. 

    :::image type="complex" source="../media/a11y-testing-source-order-viewer.msft.png" alt-text="L’activation de l’Afficheur des commandes sources affiche l’ordre des éléments dans la source sous la la mesure où ils sont superposés sur la page" lightbox="../media/a11y-testing-source-order-viewer.msft.png":::
        L’activation de **l’Afficheur** des commandes sources affiche l’ordre des éléments dans la source sous la la mesure où ils sont superposés sur la page
    :::image-end:::
    
1.  Faites défiler la page pour voir toutes les superpositions numériques, y compris dans la section pied de page.


## <a name="see-also"></a>Articles associés

*  [Vue d’ensemble des tests d’accessibilité à l’aide de DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page web de démonstration de test d’accessibilité | GitHub"
