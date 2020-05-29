---
description: Utiliser la ligne de commande console pour interagir avec une page en cours d’exécution
title: DevTools-console-ligne de commande
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, ligne de commande de la console
ms.custom: seodec18
ms.openlocfilehash: c661736e5ea264f60279c89cfa0f9c55361d2288
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566389"
---
# Ligne de commande de la console

Utilisez la ligne de commande console pour afficher et modifier les valeurs d’une page et exécuter du code de débogage à la volée, tout en tirant parti de la saisie semi-automatique de Visual Studio [*IntelliSense*](/visualstudio/ide/javascript-intellisense) . 

Entrez simplement n’importe quel code JavaScript valide à l’invite de la ligne de commande, puis appuyez sur `Enter` exécuter. Pour une entrée multiligne, utilisez `Shift+Enter` la fonction de saut de ligne. Utilisez les `Up` `Down` touches de direction et pour parcourir les commandes de console précédentes que vous avez entrées lors de la session devtools actuelle. Outre le langage JavaScript standard et l' [API console](./console-api.md), la console prend également en charge les commandes suivantes pour:

 - [Sélection d’objets DOM](#dom-selectors)
 - [Inspecter les propriétés de l’objet](#object-inspection)
 - [Recherche de tous les écouteurs d’événements sur un objet donné](#event-listeners)

Le script entré dans la ligne de commande s’exécute dans l' [étendue globale](/scripting/javascript/advanced/variable-scope-javascript) de la fenêtre actuellement sélectionnée, sauf si celle-ci est suspendue à un point d’arrêt. Les commandes de console entrées alors que la page est en pause s’exécutent dans l' [étendue locale](/scripting/javascript/advanced/variable-scope-javascript) de la fonction Current dans la pile d’appels.

La console dispose d’une liste déroulante de contexte d’exécution **cible** juste au-dessus de la zone de sortie de la console. La sélection par défaut est le document de niveau supérieur **_top**. Les iframes du document ou de l’exécution d’extensions apparaissent également sous la forme d’options, ce qui vous permet d’exécuter d’autres commandes dans ces zones.

## Sélecteurs DOM
Ces sélecteurs de console fournissent des raccourcis simples pour accéder rapidement aux objets au sein du DOM:

### $ (*Chaîne de sélecteur CSS*)
Retourne le premier élément dans le document correspondant au [Sélecteur de feuilles de style CSS](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors) spécifié (ou au groupe de sélecteurs de valeurs séparées par des virgules). Sténo pour [document. querySelector ()](https://developer.mozilla.org/docs/Web/API/Document/querySelector).

Par exemple: Ouvrez la console et tapez `$('#main')` pour renvoyer l’objet div `id='main'` sur la page suivante.

![Exemple d’utilisation du sélecteur' $ '](../media/console_cmd_$.png)

### $ $ (*Chaîne de sélecteur CSS*)
Retourne un tableau d’éléments dans le document correspondant au [Sélecteur de feuilles de style CSS](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors) spécifié (ou au groupe de sélecteurs de valeurs séparées par des virgules). Sténo pour [document. querySelectorAll ()](https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll).

Par exemple: Ouvrez la console et tapez `$$('.container')` pour renvoyer tous les objets div with `class='container'` sur cette page.

![Exemple d’utilisation du sélecteur' $ $ '](../media/console_cmd_$$.png)

### $0, $1, $2,...
Renvoie les derniers éléments sélectionnés dans le panneau [**éléments**](../elements.md) , où `$0` représente l’élément sélectionné, `$1` l’élément sélectionné auparavant, etc.

Par exemple: Ouvrez DevTools sur l’onglet **éléments** , appuyez sur `CTRL + B` pour activer l’outil **Sélectionner l’élément** , puis cliquez sur une zone de cette page à l’aide de la souris. Ouvrez ensuite la console et tapez `$0` pour renvoyer l’élément sur lequel vous avez cliqué.

![Exemple d’utilisation du sélecteur' $0 '](../media/console_cmd_$0.png)

### $x (*expression XPath*)
Retourne un tableau d’éléments qui correspond à l’expression [XPath](https://developer.mozilla.org/docs/Introduction_to_using_XPath_in_JavaScript) spécifiée. 

Par exemple: Ouvrez la console et tapez `$x('//script[@defer]')` pour renvoyer tous les `<script>` éléments de cette page qui contiennent un `defer` attribut.

![Exemple d’utilisation du sélecteur de $x](../media/console_cmd_$x.png)

## Inspection d’objets

Ces commandes fournissent des méthodes rapides pour inspecter les propriétés d’un objet. L’objet spécifié doit être défini soit dans l’espace de noms global, soit dans l’étendue actuelle du débogueur.

### dir (*objet*)
Renvoie une liste d’arborescence des propriétés de l’objet spécifié.

Par exemple: Ouvrez la console et tapez `dir(document)` pour afficher les propriétés de l’objet document correspondant à cette page.

![Exemple d’utilisation de la méthode dir](../media/console_cmd_dir.png)

### Keys (*objet*)
Renvoie un tableau de noms de propriété joints à l’objet spécifié.

Par exemple: Ouvrez la console et tapez `keys(window)` pour renvoyer toutes les propriétés définies sur l’objet Window global.

![Exemple d’utilisation de la méthode «Keys»](../media/console_cmd_keys.png)

### valeurs (*objet*)
Retourne un tableau de valeurs de propriété jointes à l’objet spécifié.

Par exemple: Ouvrez la console et tapez `values(window)` pour renvoyer les valeurs de toutes les propriétés (clés) définies sur l’objet fenêtre globale.

![Exemple d’utilisation de la méthode «values»](../media/console_cmd_values.png)

## Écouteurs d’événements

Cette commande vous permet d’inspecter les détecteurs d’événements enregistrés sur un objet donné. L’objet spécifié doit être défini soit dans l’espace de noms global, soit dans l’étendue actuelle du débogueur.

### getEventListeners (*objet*)
Renvoie un objet contenant une clé pour chaque type d’événement inscrit sur l’objet donné. La valeur de chaque clé est un tableau de détecteurs d’événements et leurs informations associées. 

Par exemple: Ouvrez la console et tapez `getEventListeners(document)` pour afficher tous les écouteurs d’événements enregistrés dans l’objet document de cette page.

![Exemple d’utilisation de la méthode «getEventListeners»](../media/console_cmd_getEventListeners.png)
