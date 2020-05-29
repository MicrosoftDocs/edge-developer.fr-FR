---
description: Utilisez le débogueur pour parcourir votre code et résoudre les problèmes.
title: DevTools-Debugger
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, débogueur, débogage, points d’arrêt, espions, travailleurs de service, API du cache, stockage Web, cookies
ms.custom: seodec18
ms.openlocfilehash: f82fbb057a3ad1027309d89db1a15dbcbea31292
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566374"
---
# Débogueur

Servez-vous du **débogueur** pour parcourir le code, définir des espions et des points d’arrêt, modifier votre code et examiner vos caches. Testez et résolvez votre code en procédant comme suit:

- [Navigation](#resource-picker) et [recherche](#file-search) de code à partir de vos fichiers sources chargés
- [Contrôle du flux d’exécution](#toolbar) au fur et à mesure de votre code
- [Gestion des ressources de stockage de page](./storage.md#cache-manager), y compris des [travailleurs de services et du cache](./service-workers.md), des [cookies](./storage.md#cookies-list) et du [stockage Web](./storage.md#local-and-session-storage-managers)  
- [Définition de points d’arrêt et modification dynamique](#debug-window) de votre code lors de son exécution
- [Suivi et modification des variables locales](#watches) lors du débogage
- [Masquage ou affichage du code asynchrone et du code](#call-stack) de la bibliothèque à partir de votre CallStack selon les besoins
- [Ajouter des points d’arrêt spécialisés](#breakpoints) pour les XMLHttpRequest, les événements et les [mutations DOM](#dom-breakpoints)

![Débogueur Microsoft Edge DevTools](./media/debugger.png)

Il existe trois façons de commencer une session de débogage.

1. **Définissez un point d’arrêt.** Lorsque l’exécution de votre code atteint celle-ci, vous devez entrer le débogueur et être en mesure de parcourir votre code.
2. **Lancer une coupure dans le code.** Cliquez sur le bouton [**saut**](#toolbar) *de la* barre d’outils ou `Ctrl+Shift+B` . Le débogueur s’arrête sur l’instruction d’exécution suivante.
3. **Définir le comportement de l’exception.** Utilisez le menu [**modifier le comportement**](#toolbar) de l’exception ( `Ctrl+Shift+E` ) pour s’arrêter dans le débogueur quand votre code lève une exception. Par défaut, le débogueur est défini de sorte qu’il *ne se bloque jamais sur les exceptions*, mais qu’il est connecté à la console.

## Sélecteur de ressources

Souvent, la première étape du débogage consiste à définir des points d’arrêt dans le code que vous cherchez à résoudre les problèmes. Vous pouvez trouver tous les fichiers de code actuellement chargés par la page à partir du volet *Sélecteur de ressources* , notamment les fichiers *. html,. CSS* et *. js* .

 Le fait de cliquer sur une entrée de fichier permet d’ouvrir un onglet pour ce fichier dans la [fenêtre de débogage](#debug-window) et de mettre en gras le texte du nom de fichier pour indiquer cela (comme le nom du fichier *devtools-Guide* figure dans l’illustration ci-dessus). Vous pouvez ensuite définir des points d’arrêt dans le fichier à partir de la [fenêtre de débogage](#debug-window).

![Sélecteur de ressources de débogueur](./media/debugger_resource_picker.png)

Dans le menu contextuel du *Sélecteur de ressources* , vous pouvez également marquer un fichier en tant que **Code de bibliothèque** ( `Ctrl+L` ), en vous offrant la possibilité d' [ignorer ce code dans le débogueur](#debug-window) et [de le masquer dans le volet **pile d’appels** ](#call-stack). Cliquez de nouveau sur (ou `Ctrl+L` ) pour basculer le fichier à sa valeur précédente *my code* en tant que code ou *Code de bibliothèque*.

### Recherche de fichiers

Utiliser la commande *Rechercher dans les fichiers* ( `Ctrl` + `Shift` + `F` ) lorsque vous avez une chaîne de code spécifique que vous recherchez dans la source. La barre d’outils fournit des options de recherche différentes, y compris des expressions régulières. Le fait de cliquer sur un résultat de recherche a pour effet de mettre au point la *fenêtre de débogage* sur le fichier et la ligne spécifiés.

![Volet recherche de fichiers du débogueur](./media/debugger_file_search.png)

## Fenêtre de débogage

La *fenêtre déboguer* vous permet de définir des points d’arrêt, de parcourir le code et de modifier votre script en temps réel lors du débogage. Cliquez à gauche de n’importe quelle commande de script pour ajouter (ou supprimer) un **point d’arrêt**. Utilisez le menu contextuel ou le volet [**points d’arrêt**](#breakpoints) pour *Ajouter une condition* au point d’arrêt en fournissant une expression logique qui amène le débogueur à être interrompu s’il évalue la *valeur true* à cet emplacement.

![Commandes de fenêtre de débogage](./media/debugger_window.png)

D’autres fonctionnalités de la fenêtre de débogage incluent des contrôles pour:

### 1. édition de code

Vous pouvez modifier votre dynamique JavaScript lors d’une session de débogage. Une fois que vous avez effectué vos modifications, cliquez sur <strong> Enregistrer </strong> ( `Ctrl+S` ) pour tester vos modifications à la prochaine exécution de la section de code. Si vous avez changé de code non enregistré, un astérisque (\ *) s’affiche avant le nom du fichier dans l’onglet *fenêtre de débogage* .

Cliquez sur le bouton **comparer le document à l’original** pour afficher un aperçu de ce que vous avez modifié.

![Vue diff du code modifié dans le débogueur](./media/debugger_edit_code.png)

Tenez compte des contraintes suivantes:

- La modification des scripts ne fonctionne que dans les fichiers externes *. js* (et non incorporés `<script>` au *format. html*)
- Les modifications sont enregistrées en mémoire et vidées lors du rechargement du document, vous ne pourrez donc pas exécuter de modifications à l’intérieur d’un `DOMContentLoaded` Gestionnaire, par exemple
- Il n’existe actuellement aucune méthode (par exemple, option **Enregistrer sous** ) pour enregistrer vos modifications sur le disque à partir du devtools

### 2. mise en forme du code

Utilisez ces contrôles pour mettre en forme le code minified pour une meilleure lisibilité lors du débogage:

#### À imprimer ( `Ctrl+Shift+P` ) 
Ajoute des sauts de ligne et des accolades d’alignement par conventions JavaScript. Même le code compressé qui a été rendu plus lisible avec cette option peut avoir des noms de fonction, de sélecteur et de variables qui sont très différents de ceux de votre code source d’origine. Dans ces cas, l’option [*Afficher/masquer les cartes sources*](#source-maps) peut être disponible.

#### Renvoi du texte à la ligne `Alt+W`
Ajuste le code de sorte qu’il s’adapte aux marges actuelles de la fenêtre de débogage (ce qui évite d’avoir besoin de défilement horizontal).

### 3. étendue du code

Vous pouvez indiquer au débogueur d’ignorer certains fichiers à l’aide du bouton **marquer en tant que code** de la bibliothèque ( `Ctrl+L` ). Par défaut, le bouton [**Déboguer uniquement ma**](#toolbar) barre d’outils est activé, ce qui signifie que le débogueur ignorera les fichiers que vous marquez en tant que *Code de bibliothèque* et qu’ils n’apparaissent pas dans la pile d' [appels](#call-stack)de débogueur. La sélection du bouton (**marquer comme mon code** `Ctrl+L` ) entraîne la suppression de cet indicateur.

Pour effectuer le suivi des bibliothèques au sein des sessions de débogage, vous pouvez modifier ces fichiers pour conserver une liste par défaut ou ajouter des caractères génériques pour un type de fichier ou de domaine:

```JavaScript
%APPDATA%\..\LocalLow\Microsoft\F12\header\MyCode.json and %APPDATA%\..\Local\Microsoft\F12\header\MyCode.json
```

#### Mappages sources

Le bouton **Afficher/masquer les cartes sources** est activé pour le code écrit dans un langage qui est compilé en JavaScript ou CSS et *fournit un mappage de fichier* intermédiaire (mappage de fichier intermédiaire à la source d’origine). Cette option indique au débogueur de présenter la source d’origine à utiliser pour le débogage (plutôt que le fichier compilé qui s’exécute *réellement* dans le navigateur).

Le DevTools vérifie si le compilateur qui a généré le fichier JavaScript a ajouté un commentaire avec le nom du fichier de carte. Par exemple, si un compilateur a compressé *MyFile. js* dans *MyFile. min. js*, il peut également générer un fichier de carte, *MyFile. min. js. map* et inclure un commentaire dans le fichier compressé comme suit:

```JavaScript
//# sourceMappingURL=myfile.min.js.map
```

![Menu contextuel de l’onglet fichier de débogage](./media/debug_file_contextmenu.png)

Si le DevTools ne trouve pas la carte automatiquement, vous pouvez choisir une carte source pour ce fichier. Cliquez avec le bouton droit sur l’onglet du fichier pour accéder à l’option **choisir le mappage source** . 

## ToolBar

Utilisez la *barre d’outils* de débogueur pour contrôler le fonctionnement du code et le code à suivre ou à ignorer. Vous pouvez également effectuer une recherche de texte intégral dans les fichiers de code pour des chaînes spécifiques.

![Barre d’outils de débogage](./media/debugger_toolbar.png)

### 1. continuer ( `F5` )/ATTN ( `Ctrl+Shift+B` )
 **Continue** ( `F5` ) continue l’exécution du code au point d’arrêt suivant. Le fait de maintenir la touche enfoncé `F5` entraîne le déplacement répété des sauts de passe jusqu’à ce que vous relâchiez. 

 **Break** ( `Ctrl+Shift+B` ) s’arrête dans le débogueur après l’exécution de l’instruction Next.

### 2. fonctions d’étape ( `F11` , `Ctrl+F10` , `Shift+F11` )
 **Pas à pas dans** ( `F11` ) étapes dans la fonction appelée. 

 **Pas à pas** ( `Ctrl+F10` ) étapes sur la fonction appelée. 

 **Pas à pas détaillé** ( `Shift+F11` ) étapes de la fonction actuelle et de la fonction d’appel. 

 Le débogueur passe à l’instruction suivante s’il n’y a pas de fonction lors de l’utilisation de ces commandes.

### 3. pause sur le nouveau travailleur ( `Ctrl+Shift+W` )
 S’interrompt lors de la création d’un nouveau [travailleur Web](https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers).

### 4. contrôle d’exception
**Modifier le comportement** d’une exception ( `Ctrl+Shift+E` ) permet d’ouvrir les options permettant de modifier la façon dont le débogueur réagit aux exceptions. Par défaut, il est ignoré par le débogueur et enregistré dans la [**console**](./console.md). Vous pouvez choisir de vous *arrêter sur toutes les exceptions*, ou uniquement celles qui ne sont pas traitées par des `try...catch` instructions dans votre code (*arrêt sur les exceptions non gérées*).

### 5. afficher les résultats de la recherche
(Actuellement désactivée.) **Afficher/masquer les résultats** active ou désactive l’affichage des résultats de recherche [*Rechercher dans les fichiers*](#6-find-in-files-ctrlf) .

### 6. Rechercher dans les fichiers ( `Ctrl+F` )
 **Rechercher dans les fichiers** ( `Ctrl+F` ) exécute une recherche de texte dans tous les fichiers chargés dans le [*Sélecteur de ressources*](#resource-picker). Si le texte est trouvé, il ouvre le premier fichier correspondant à la chaîne de recherche. Le fait d’appuyer sur `Enter` ou `F3` vous permet d’accéder à la correspondance suivante.

### 7. déboguer uniquement mon code ( `Ctrl+J` )
 Le **débogage uniquement mon code** ( `Ctrl+J` ) sert de bouton bascule pour inclure ou exclure tous les fichiers qui ont été marqués comme [Code de bibliothèque](#3-code-scoping) lorsque vous exécutez le débogueur.

### 8. connexion au débogueur
Le **débogueur de débogage/connexion** est essentiellement le commutateur d’activation/désactivation pour le débogueur.

## Observations

Le volet **espions** vous permet de parcourir un catalogue de tous les objets et variables (**locales**), à la fois dans l’étendue locale et globale, à l’aide de l’instruction qui est le focus de la pause actuelle dans le débogueur.

![Volet Espions](./media/debugger_watches.png)

Vous pouvez effectuer le suivi de la valeur de variables spécifiques au fur et à mesure de leur passage en ajoutant une espion (**Ajouter un espion**, `Ctrl+W` ) et modifier les valeurs modifiables en double-cliquant dessus ou en sélectionnant **modifier la valeur** dans le *menu contextuel*. Effacez vos espions à l’aide des boutons **supprimer** ( `Ctrl+D` )/ **Supprimer tout** ou du menu contextuel. 

## Détails

Le volet *Détails* inclut les onglets de [**CallStack**](#call-stack), d' [**arrêt**](#breakpoints) et de [**points d’arrêt DOM**](#dom-breakpoints) .

### Pile d’appels

L’onglet **pile d’appels** affiche la chaîne de fonctions ayant entraîné le point d’exécution actuel. La fonction Current apparaît en haut et les fonctions d’appel s’affichent en dessous dans l’ordre inverse.

![Volet pile d’appels](./media/debugger_callstack.png)

Le bouton **Afficher/masquer les images** de la bibliothèque () permet d' `Ctrl+Shift+J` activer ou de désactiver la sortie du code de la [bibliothèque](#3-code-scoping) . Utilisez l’option de **code** de la bibliothèque ( `Ctrl+L` ) à partir du *menu contextuel* pour marquer (ou démarquer) la source de l’image sélectionnée comme code de bibliothèque. 

Le bouton **Afficher/masquer les trames Async** permet d’activer l’affichage des racines pour les appels de fonction asynchrones.

### Points d’arrêt

À partir de l’onglet **points d’arrêt** , vous pouvez gérer les points d’arrêt et les points de trace des événements, y compris définir des conditions, les désactiver ou les supprimer.

![Onglet points d’arrêt](./media/debugger_breakpoints.png)

Voici un résumé des différents types d’points d’arrêt que vous pouvez utiliser pour le débogage.

Type de point d’arrêt | Description | Comment la configurer
:------------ | :------------ | :--------
**Interruption** | S’arrête dans le débogueur juste avant l’exécution de la ligne de code spécifiée. Les points d’arrêt standard sont plus faciles à définir si vous disposez d’une instruction par ligne. | Dans la [fenêtre de débogage](#debug-window), cliquez dans la marge de gauche en regard d’un numéro de ligne dans le code. Un point rouge apparaît et le point d’arrêt est défini. Vous pouvez accéder à la source de n’importe quel point d’arrêt en cliquant sur son texte en bleu.
**Point d’arrêt conditionnel** | S’interrompt si la condition spécifiée a pour résultat la *valeur vrai*. Il s’agit essentiellement `if(condition)` d’une opération de rupture dans le débogueur.  | Dans l’onglet [points d’arrêt](#breakpoints) , placez le pointeur sur un point d’arrêt existant et cliquez sur le bouton «crayon» (*Ajouter une condition à ce point d’arrêt*), cliquez avec le bouton droit sur un point d’arrêt existant et sélectionnez **condition...** dans le menu contextuel. Spécifiez la condition «if» à évaluer à l’emplacement du point d’arrêt. 
**Point d’arrêt** . | S’interrompt chaque fois qu’une requête XMLHttpRequest (XHR) est satisfaite. Vous pouvez inspecter l' `response` objet XHR à partir du volet [**espions**](#watches) . | À partir de l’onglet [points d’arrêt](#breakpoints) , cliquez sur le bouton point d' *arrêt de XMLHttpRequest* (cercle avec flèches haut/bas). Vous pouvez la convertir en *point d’arrêt conditionnel* comme décrit ci-dessus.
**Trace d’événement** | Appels [`console.log()`](./console/console-api.md#logging-custom-messages) avec une chaîne spécifiée en réponse à un événement spécifique. Utilisez cette information pour les instructions de journalisation de console temporaires que vous ne voulez pas enregistrer directement dans le code de votre gestionnaire d’événements. | Dans l’onglet [points d’arrêt](#breakpoints) , cliquez sur le bouton de point de trace d' *événement* (losange avec éclair). Sélectionnez un type d' **événement** pour le déclencheur et une instruction de **suivi** pour la journalisation.
**Point d’arrêt d’événement** (w/condition facultative) | S’interrompt chaque fois qu’un événement spécifié est déclenché. | Dans l’onglet [points d’arrêt](#breakpoints) , cliquez sur le bouton point d’arrêt de l' *événement* (cercle avec éclair). Sélectionner un type d' **événement** pour le déclencheur et éventuellement spécifier une instruction de **condition** . 
**Point d’arrêt DOM** | S’interrompt chaque fois qu’un élément spécifié de la page est muté, par exemple lorsque sa sous-arborescence est modifiée, ses attributs changent ou lorsqu’il est détaché du DOM. | À partir de l’onglet [éléments](./elements/dom-breakpoints.md) , cliquez avec le bouton droit sur un élément source, puis sélectionnez l’une des options de *points d’arrêt DOM* . Utilisez l’onglet [**points d’arrêt DOM**](#dom-breakpoints) dans le volet *débogueur* ou *éléments* pour gérer vos points d’arrêt. 

Les points d’arrêt et points de trace conditionnels ont accès à toutes les variables locales et globales qui se trouvent actuellement dans l’étendue lorsqu’elles sont arrêtées dans le débogueur.

### Points d’arrêt DOM

Gérez vos points d’arrêt de mutation DOM à partir de l’onglet **points d’arrêt DOM** , y compris la désactivation, la suppression et la reliaison.  Les [points d’arrêt DOM peuvent être définis](./elements/dom-breakpoints.md) dans l' *arborescence html* du panneau **éléments** .

![Onglet points d’arrêt DOM](./media/debugger_dom_breakpoints.png)

L' *onglet points d’arrêt DOM* dans le **débogueur** fournit des fonctionnalités équivalentes à l’onglet *points d’arrêt DOM** du panneau **éléments** .

Voici d’autres informations sur les différents types de [points d’arrêt DOM](./elements/dom-breakpoints.md).

## Associés

### Raccourcis de la barre d’outils

Action | Raccourci
:------------ | :-------------
Rechercher | `Ctrl` + `F`
Continue (à partir du point d’arrêt) | `F5` ou `F8`
Poursuite rapide | Mettre en attente `F5` ou `F8`
Continuer et actualiser | `Ctrl` + `Shift` + `F5`
Conditionnement | `Ctrl` + `Shift` + `B`
Étape | `F11`
Pas à pas | `F10`
Pas à pas détaillé | `Shift` + `F11`
Interruption de nouveau travailleur | `Ctrl` + `Shift` + `W`
Modification du comportement d’une exception (menu ouvert) | `Ctrl` + `Shift` + `E`
Déboguer uniquement mon code | `Ctrl` + `J`

### Raccourcis du sélecteur de ressources

Action | Raccourci
:------------ | :-------------
Marquer comme mon code de code ou de bibliothèque | `Ctrl` + `L`
Ouvrir un fichier | `Ctrl` + `O`, `Ctrl` + `P`
Rechercher dans tous les fichiers | `Ctrl` + `Shift` + `F`

### Raccourcis de la fenêtre de débogage

Action | Raccourci
:------------ | :-------------
Supprimer un point d’arrêt | `F9`
Désactiver le point d’arrêt | `Ctrl` + `F9`
Point d’arrêt conditionnel... | `Alt` + `F9`
Copy | `Ctrl` + `C`
Enregistrer | `Ctrl` + `S`
Accéder à la ligne... | `Ctrl` + `G`
Afficher l’instruction suivante | `Alt` + `Num` + `*`
Exécuter jusqu’au curseur | `Ctrl` + `F10`
Définir l’instruction suivante | `Ctrl` + `Shift` + `F10`
Afficher dans le sélecteur de fichiers | `Ctrl` + `Alt` + `P`
Atteindre la définition dans le fichier | `Ctrl`+`D`
Rechercher des références dans un fichier | `Ctrl` + `Shift` + `D`
Impression conviviale | `Ctrl` + `Shift` + `P`
Retour automatique à la ligne | `Alt` + `W`
Marquer comme mon code de code ou de bibliothèque | `Ctrl` + `L`
Activez/désactivez les onglets de l’éditeur. **Remarque:** si vous utilisez le clavier pour naviguer dans le débogueur, vous ne serez pas en mesure de quitter l’éditeur tant que vous n’avez pas désactivé la touche Tab. | `Ctrl` + `M`

### Raccourcis pour le volet Espions

Action | Raccourci
:------------ | :-------------
Ajouter un espion | `Ctrl` + `W`
Supprimer un espion | `Ctrl` + `D`

### Raccourcis pour le volet d’informations

| Action                             | Raccourci                 |
|:-----------------------------------|:-------------------------|
| Afficher/masquer les trames dans le code de la bibliothèque | `Ctrl` + `Shift` + `J`   |
| Activer tous les points d’arrêt             | `Ctrl` + `Shift` + `F11` |
