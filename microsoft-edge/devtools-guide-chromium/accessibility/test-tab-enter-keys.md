---
description: Vérifiez la prise en charge du clavier à l’aide des touches Tab et Entrée.
title: Vérifier la prise en charge du clavier à l’aide des touches Tab et Entrée
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 48151e16a9059b5ebaadca36f29447d4ad3be8c7
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597329"
---
# <a name="check-for-keyboard-support-by-using-the-tab-and-enter-keys"></a>Vérifier la prise en charge du clavier à l’aide des touches Tab et Entrée


Tous les utilisateurs n’ont pas de pointeur ou d’appareil tactile, et tous les utilisateurs ne peuvent pas voir les projets web que nous créons.  C’est pourquoi il est important que l’interface utilisateur fonctionne au moins avec un clavier.  Assurez-vous que vous pouvez utiliser la clé pour déplacer la mise au point sur chaque contrôle de formulaire sur une page web et assurez-vous que vous pouvez utiliser la clé pour `Tab` `Enter` envoyer des formulaires.

Vous pouvez tester l’utilisation d’une page web pour les utilisateurs de clavier de plusieurs façons :
*  En utilisant le clavier, en particulier `Tab` les `Shift` + `Tab` touches et les `Enter` touches.  Cette approche est décrite dans cet article.
*  Vérifiez la prise en charge du clavier pour un élément individuel à l’aide de **l’outil Inspect.**  La superposition des informations de l’outil Inspect inclut une section **Accessibilité** qui inclut une ligne **focusable au clavier.**  
*  Consultez la **section** **Accessibilité du** rapport problèmes pour les problèmes de prise en charge du clavier.

Pour vérifier la page de démonstration des problèmes d’accessibilité à l’aide d’un clavier plutôt que d’une souris, effectuez les étapes suivantes :

1.  Ouvrez la page web de [démonstration des tests d’accessibilité][DevToolsA11yErrorsDemopage] dans un nouvel onglet du navigateur.

1.  Utilisez un clavier pour parcourir le document de démonstration, en utilisant les touches et les touches pour passer `Tab` `Shift` + `Tab` d’un élément à l’autre.  Sur la page web de démonstration, la touche déplace d’abord `Tab` le focus sur le formulaire de recherche dans la `header` section.

1.  Sélectionnez pour placer le focus sur un bouton, puis cliquez sur `Tab` `Enter` le bouton sélectionné.  Par exemple, dans la page de démonstration, sélectionnez pour mettre le focus sur le champ De recherche, puis sélectionnez `Tab` pour envoyer la **** `Enter` recherche.  Cette approche produit le même résultat que la sélection du **bouton** Aller.  La sélection `Enter` pour envoyer le formulaire **de** recherche fonctionne correctement.

1.  Sélectionnez `Tab` à nouveau.  L’élément suivant sur qui vous mettez le focus est le premier lien **Plus** dans la section de la page web, comme indiqué `content` par un plan.
    
    :::image type="complex" source="../media/a11y-testing-keyboard-focus-on-element.msft.png" alt-text="Navigation dans le document à l’aide du clavier et de la touche « Tab ». Le focus est affiché sur un lien dans le document." lightbox="../media/a11y-testing-keyboard-focus-on-element.msft.png":::
        Navigation dans le document à l’aide du clavier et de la touche de tabulation. Le focus est affiché sur un lien dans le document.
    :::image-end:::
    
1.  Sélectionnez `Tab` plusieurs fois jusqu’à ce que vous passez le dernier **lien** Plus.  La page défile vers le haut et vous semblez être sur un élément de la page, mais il n’existe aucun moyen de savoir de quel élément il s’agit.

1.  Notez l’URL en bas à gauche.  Si vous regardez en bas à gauche de l’écran (ou si vous utilisez un lecteur d’écran), vous réalisez que vous êtes sur le menu de navigation de la barre latérale avec des liens bleus, car le navigateur affiche l’URL vers qui pointe le lien **Chats** ( `#cats` ).

    :::image type="complex" source="../media/a11y-testing-lack-of-focus-style.msft.png" alt-text="En raison d’un manque de style de mise au point, il est impossible de savoir où vous vous trouvez actuellement dans le document. Le seul conseil est l’affichage de la cible du lien dans le coin inférieur gauche de l’écran." lightbox="../media/a11y-testing-lack-of-focus-style.msft.png":::
        En raison d’un manque de style de mise au point, il est impossible de savoir où vous vous trouvez actuellement dans le document. Le seul conseil est l’affichage de la cible du lien dans le coin inférieur gauche de l’écran.
    :::image-end:::

1.  Sélectionnez `Tab` de nouveau pour obtenir le champ d’entrée dans le formulaire de don.  Toutefois, vous ne pouvez pas atteindre les boutons au-dessus de la boîte de texte en sélectionnant `Tab` . Vous ne pouvez pas utiliser le clavier pour mettre le focus sur **les boutons 50,** **100**ou **200,** puis les sélectionner.  En outre, la sélection `Enter` n’envoie pas le formulaire de don.

    :::image type="complex" source="../media/a11y-testing-form-field-with-outline.msft.png" alt-text="Le seul élément accessible au clavier dans le formulaire de don est le champ d’entrée de texte." lightbox="../media/a11y-testing-form-field-with-outline.msft.png":::
        Le seul élément accessible au clavier dans le formulaire de don est le champ d’entrée de texte.
    :::image-end:::
    
1.  La sélection de nouveau met le focus sur la barre de navigation supérieure de la page, avec les boutons de menu pour Accueil, Adopter un enfant `Tab` de compagnie, **Sons,** Travaux **** et **** À propos de **** **nous.**  Sélectionnez `Tab` ou mettez le focus sur un bouton de menu, comme indiqué par un plan de `Shift` + `Tab` focus.  Sélectionnez `Enter` ensuite pour accéder à cette section de la page web.

    :::image type="complex" source="../media/a11y-testing-menu-with-outline.msft.png" alt-text="Le menu principal a une mise en surbrill plan et un plan de mise au point, et est donc accessible au clavier" lightbox="../media/a11y-testing-menu-with-outline.msft.png":::
        Le menu principal a une mise en surbrill plan et un plan de mise au point, et est donc accessible au clavier
    :::image-end:::
    
Sur la base de la walkthrough ci-dessus, nous avons trouvé les problèmes suivants qui doivent être résolus.

*  Lorsque vous utilisez un clavier, les liens bleus du menu de navigation de la barre latérale n’indiquent pas visuellement quel lien a le focus.  Pour plus d’informations, [accédez à Analyser l’absence d’indication](test-analyze-no-focus-indicator.md)du focus du clavier dans un menu de barre latérale.

*  Dans le formulaire de don, les boutons Montant et **Bouton Dente** ne fonctionnent pas avec un clavier.  Pour plus d’informations, [accédez à Analyser l’absence de prise](test-analyze-no-keyboard-support.md)en charge du clavier dans un formulaire.

*  L’ordre d’accès au clavier par le biais des sections de la page n’est pas correct.  Vous naviguez dans tous les **liens Plus** du document avant d’accéder au menu de navigation de la barre latérale.  Au moment où la touche met le focus sur le menu de navigation de la barre latérale, vous avez déjà parcouru tout le contenu `Tab` de la page. Le menu de navigation de la barre latérale était destiné à fournir un accès facile au contenu de la page.  Pour plus d’informations sur la résolution de ce problème, accédez à la prise en charge du clavier test à l’aide de l’Observateur de [commandes source.](test-tab-key-source-order-viewer.md)


## <a name="see-also"></a>Articles associés

*  [Vue d’ensemble des tests d’accessibilité à l’aide de DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page web de démonstration de test d’accessibilité | GitHub"
