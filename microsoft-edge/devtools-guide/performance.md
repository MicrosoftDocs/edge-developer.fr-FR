---
description: Utiliser le volet performance pour analyser le responsivenes de votre page lors de l’interaction utilisateur
title: DevTools-performance
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, performances, profil, fréquence d’images, FPS, utilisation de l’UC, exécution JavaScript
ms.custom: seodec18
ms.openlocfilehash: aecf3cf49592dbf1f24231e76f14ddc2ca1228c3
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565542"
---
# Analyse des performances

Le panneau **performance** propose des outils de profilage et d’analyse de la réactivité de votre interface utilisateur au cours de l’interaction de l’utilisateur. Avec ce service, vous pouvez:

 - [Mesurer les temps d’exécution](#recording-a-profile) des différents composants de votre page 
 - [Explorez vers le bas jusqu’à l’endroit où vous dépenser le plus de cycles d’UC](#timeline-ruler) pour exécuter votre page et l’effet visuel obtenu pour vos utilisateurs.
 - [Obtenir une répartition détaillée des processus utilisant le temps d’exécution de la](#timeline-details) page 
 - [Parcourez vos piles d’appels JavaScript](#javascript-call-stacks) pour identifier les opérations onéreuses, telles que les personnes nécessitant un recalcul de la disposition 

![Panneau performances de DevTools](./media/performance.png)

## Enregistrement d’un profil

Dans le cadre de l’analyse des performances de votre page, la première étape consiste à capturer un profil lorsque vous effectuez un scénario utilisateur particulier, par exemple les étapes de reproduction d’un bogue de performance que vous tentez de résoudre, ou un cas d’utilisation type que vous souhaitez optimiser pour une meilleure expérience utilisateur. 

### ToolBar

Utilisez les **Start**  /  boutons**Stop** de démarrage de la barre d’outils (ou `Ctrl+E` ) pour initier et terminer votre suivi des performances. Un indicateur vert s’affichent sous l’onglet **performance** pour indiquer qu’un enregistrement est en cours. 

![Barre d’outils du panneau performances](./media/performance_toolbar.png)

Un rapport de performance sera généré lors de l’arrêt du profil. Vous pouvez choisir de l’enregistrer sur le disque ( `Ctrl+S` ) et de le recharger ( `Ctrl+O` ) dans devtools plus tard.  Les sessions de diagnostic DevTools sont enregistrées avec l’extension *. diagsession* .

Voici quelques éléments à garder à l’esprit lors de l’enregistrement d’un profil:

- Effectuez le moins d’actions nécessaires pour capturer le scénario que vous essayez d’analyser. Les actions superflues avec la page produiront des données supplémentaires et démêleront vos résultats.

- Le profileur marque automatiquement les événements de cycle de vie d’application principaux dans le rapport, tels que la navigation entre les pages, le [DOMContentLoaded](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded)et le [chargement](https://developer.mozilla.org/docs/Web/Events/load)de la page. Vous pouvez ajouter des marqueurs personnalisés en appelant la méthode [performance. Mark ()](https://developer.mozilla.org/docs/Web/API/Performance/mark) à partir de votre code ou de la console. 

- Si les temps de chargement des pages initiales sont importants pour votre analyse, veillez à effacer le cache de votre navigateur (dans le panneau [réseau](./network.md) ) pour vous assurer que toutes les ressources de la page sont chargées à partir du réseau.

- Il peut parfois être utile d’enregistrer plusieurs sessions et/ou d’échantillonner le même scénario sur différents appareils pour mieux comprendre le problème de performance.

## Règle de chronologie

La chronologie fonctionne comme une règle coulissante. Utilisez-le pour limiter le champ d’application du rapport à la période spécifique (ou à une durée d’événements). Faites glisser les **contrôles de diapositive** noirs pour limiter l’intervalle de temps que vous souhaitez examiner et filtrez les données de profilage superflues des rapports de [chronologie](#timeline-details) et de [piles d’appels JavaScript](#javascript-call-stacks) dans le *volet de détails*inférieur. 

Deux types de marqueurs apparaissent sur la règle:

 - Les **marques de cycle de vie** de l’application dans la chronologie (telles que la navigation entre les pages, les [DOMContentLoadeds](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded)et le [chargement](https://developer.mozilla.org/docs/Web/Events/load)de la page) sont automatiquement enregistrées lors de l’enregistrement d’un profil.

 - Les **marques d’utilisateur** sont des marqueurs personnalisés que vous pouvez choisir d’ajouter aux appels à la méthode [performance. Mark ()](https://developer.mozilla.org/docs/Web/API/Performance/mark) à partir de votre code ou de la [**console**](./console.md)devtools. Vous pouvez regrouper les marques de *début* et de *fin* sous la forme d’une seule et même mesure nommée par la méthode [performance. Measure ()](https://developer.mozilla.org/docs/Web/API/Performance/measure) . 

Une fois que vous avez sélectionné un intervalle de temps, vous pouvez **effectuer un zoom avant** à partir de la barre d’outils ou **Réinitialiser le zoom** et **effacer la sélection** pour revenir à l’affichage complet du suivi des performances (sans plage horaire sélectionnée). Ces contrôles sont également disponibles dans le menu contextuel.

![Chronologie du panneau de performance](./media/performance_timeline.png)

### Utilisation de l’UC

Le graphique temps d’utilisation de l' **UC%** décrit les ressources de traitement consommées par les différents sous-systèmes de navigateur nécessaires à l’exécution de la page, répartis par catégorie:

#### Chargement
Indique le temps consacré à la récupération des ressources de l’application et à l’analyse du code HTML et des feuilles CSS. Cela peut inclure les requêtes réseau. Les événements associés suivants sont enregistrés dans la [chronologie](#timeline-details):

Événement | Description
:------------ | :-------------
CssParsing  | Le nouveau contenu CSS a été détecté et devait être analysé.
HtmlParsing | Un nouveau contenu HTML a été détecté et devait être analysé dans les nœuds et insérés dans le DOM.
HttpRequest | Une ressource distante a été rencontrée dans le DOM ou un XMLHttpRequest a été créé et nécessite une requête HTTP.
HtmlSpeculativeDownloading | Le contenu HTML de la page a été recherché pour les ressources nécessaires et les requêtes HTTP pour celles-ci peuvent être planifiées aussi rapidement que possible.


#### Script
Indique le temps passé à analyser et à exécuter JavaScript. Cela inclut les événements DOM, les minuteurs, l’évaluation de script et les rappels de cadre d’animation. Les événements associés suivants sont enregistrés dans la [chronologie](#timeline-details):

Événement | Description
:------------ | :-------------
DomEvent | Un événement a été déclenché sur un objet DOM.
EvaluatingScript | Un nouvel `<script>` élément a été rencontré dans le DOM et devait être analysé et exécuté.
EventHandler | Un écouteur d’événements enregistré a été déclenché en réponse à un événement DOM déclenché.
Trame | Pendant qu’une nouvelle image a été préparée, un rappel enregistré a été déclenché de sorte qu’elle puisse apporter des modifications visuelles.
Mesure | Un scénario spécifique à l’application a été mesuré à l’aide de la `performance.measure()` méthode.
MediaQueryListener | Une requête multimédia enregistrée a été annulée, ce qui a entraîné l’exécution de ses écouteurs associés.
MutationObserver | Un ou plusieurs éléments DOM observés ont été modifiés, ce qui a entraîné l’exécution du rappel associé à MutationObserver.
TimerFired | Un minuteur planifié qui a entraîné l’exécution du rappel associé.
WindowsRuntimeAsyncCallback | Une opération asynchrone a été effectuée par un objet Windows Runtime qui déclenchait un `Promise` rappel.
WindowsRuntimeEvent | Un événement a été déclenché sur un objet Windows Runtime qui déclenchait un écouteur inscrit.

#### Global
Indique le temps écoulé lors de la collecte de mémoire pour les objets qui ne sont plus utilisés. Les événements associés suivants sont enregistrés dans la [chronologie](#timeline-details):

Événement | Description
:------------ | :-------------
GarbageCollection | Le runtime JavaScript a audité l’utilisation de la mémoire actuelle de l’application afin de déterminer les objets qui ne sont plus référencés et qui pourraient donc être collectés.

#### Stylisation
Indique le temps passé à calculer la présentation et la disposition des éléments. Les événements associés suivants sont enregistrés dans la [chronologie](#timeline-details):

Événement | Description
:------------ | :-------------
AlignedBeat | Les modifications visuelles en attente apportées au DOM étaient traitées de sorte que l’affichage de l’application puisse être mis à jour.
CssCalculation | Des modifications ont été apportées au DOM ou un nouveau contenu CSS a été ajouté, ce qui exige le recalcul des propriétés de style de tous les éléments concernés.
Disposition | Des modifications ont été apportées au DOM pour lequel la taille et/ou la position de tous les éléments concernés doivent être calculées.

#### Restitu
Indique le temps passé dans la peinture de l’écran. Les événements associés suivants sont enregistrés dans la [chronologie](#timeline-details):

Événement | Description
:------------ | :-------------
Paint | Des modifications visuelles ont été apportées au DOM qui exige que toutes les parties affectées de la page soient redessinées.
RenderLayer | Les modifications visuelles ont été apportées à un fragment de rendu indépendant du DOM (appelé calque), qui exige que sa partie respective de la page soit redessinée.

#### Décodage d’image
Indique le temps passé à décompresser et décoder les images. Les événements associés suivants sont enregistrés dans la [chronologie](#timeline-details):

Événement | Description
:------------ | :-------------
ImageDecoded | Une image a été incluse dans le DOM et devrait être décompressée dans son format d’origine dans une image bitmap.

### Débit visuel

Le graphique de **débit visuel (FPS)** indique la fréquence d’images estimée *par seconde* (FPS) au cours du scénario de profilage, où 60 est le taux d’affichage idéal. Les DIP dans la fréquence d’images indiquent des goulets d’étranglement des performances et une fréquence d’images de zéro signifie que les images sont coupées entièrement.

## Détails de la chronologie

Utilisez le volet Détails de lowermost pour obtenir une vue d’ensemble de ce qui est arrivé sur la page. L’onglet Détails de la **chronologie** fournit une répartition des événements qui se sont produits au sein des différents sous-systèmes de navigateur.

![Volet Détails de la chronologie des performances](./media/performance_details_timeline.png)

1. **Contrôle de tri de la liste d’événements**

    Utilisez le contrôle de liste déroulante **Trier par** pour basculer l’ordre de la [liste d’événements](#event-list) entre le *début* et la *durée (inclus*). Cela modifie également l’affichage des [Détails sélectionnés](#selected-timeline-details)de la chronologie.

2. **Regrouper les événements par cadre**

    Utilisez les **événements de niveau supérieur du groupe par image** pour activer ou désactiver les événements de niveau supérieur (*analyse html, disposition, événement DOM,* etc.) en fonction de l’unité de travail correspondante (ou «trame») au cours du laps de temps de réalisation des animations/mises à jour visuelles. Les trames sont traitées comme d’autres événements, de sorte qu’ils peuvent être triés/filtrés et fournissent un résumé du *temps inclusive* lorsque vous cliquez sur la [liste d’événements](#event-list).

3. **Contrôles de filtre de liste d’événements**

    Utilisez le menu **Filtrer les événements** pour configurer les types d’événements indiqués dans les détails de la [chronologie](#timeline-details). 

    ![Contrôle pour filtrer les événements de performance](./media/performance_filter_events.png) 

    Les filtres suivants sont disponibles:

   - **Décodage d’image**: affiche les événements qui se sont produits sur un thread en arrière-plan (par exemple, décodage d’image, CG). 
   - **Trafic réseau**: afficher les requêtes http qui étaient liées au réseau.
   - **Activité de l’interface utilisateur**: afficher des événements qui se sont produits sur le thread d’interface utilisateur et/ou le thread de rendu (par exemple, gestionnaires d’événements DOM, disposition).
   - **Mesures utilisateur**: afficher des événements personnalisés qui indiquent les appels à la méthode performance. Measure ().

     Vous pouvez filtrer davantage les événements de niveau supérieur en fonction de leur durée inclusive.

### Liste d’événements

La *liste des événements* fournit une liste chronologique des [événements de sous-système de navigateur](#cpu-utilization) qui se sont produits pendant la période sélectionnée. 

Cliquez sur n’importe quelle entrée pour remplir le graphique des **Détails d’événements sélectionnés** pour cet élément. Les entrées avec des événements et des fonctions imbriquées affichent leur **inclusive** (temps passé dans l’exécution de la fonction *et* de toutes les autres fonctions appelées) et **exclusif** (le temps passé uniquement dans le corps de la fonction d’appel) est affiché dans le graphique.

Cliquez avec le bouton droit sur n’importe quelle entrée pour ouvrir le menu contextuel et filtrer la chronologie sur cet événement uniquement et afficher le code source responsable de l’événement dans le [**débogueur**](./debugger.md) (ou le panneau d' [**éléments**](./elements.md) , le cas échéant).

### Détails de la chronologie sélectionnée

Les *Détails de la chronologie sélectionnée* fournissent un graphique à barres détaillé des durées de l’événement inclusive/exclusif pendant la période sélectionnée. Lorsque vous triez par *durée (inclusive)* en utilisant le contrôle de tri de la **liste d’événements**, les événements d’exécution les plus longs apparaissent visuellement dans ce graphique. 

### Détails de l’événement sélectionné

Ce rapport fournit des informations supplémentaires sur l’événement sélectionné, notamment l' *heure de début*, le type de thread en cours d’exécution (par exemple, *Télécharger*, *interface*, *rendu*) et d’autres détails contextuels spécifiques au type d’événement spécifique. Par exemple, les types de *détecteurs d’événements* fournissent des liens de débogueur vers la *fonction de rappel* et la pile d' *appels de planification*.

## Piles d’appels JavaScript

![Minutage des performances des piles d’appels JavaScript](./media/performance_details_javascript.png)

L’onglet **piles d’appels JavaScript** fournit les informations d’utilisation de l’UC et le minutage des fonctions de script exécutées pendant la période sélectionnée:

 Colonne | Description
:------------ | :-------------
Nom de la fonction | Nom d’un navigateur ou d’une fonction définie par l’utilisateur.
PROCESSEUR inclusive (%) | Pourcentage de l’activité d’UC sélectionnée dans cette fonction et dans les fonctions appelées par cette fonction.
PROCESSEUR exclusif (%) | Pourcentage d’activité d’UC sélectionnée dans cette fonction, à l’exception de l’activité dans les fonctions appelées par cette fonction.
PROCESSEUR inclusive (MS) | Temps UC passé lors de l’exécution du code dans cette fonction et dans les fonctions appelées par cette fonction.
PROCESSEUR exclusif (MS) | Temps UC passé à exécuter du code dans cette fonction, à l’exception du temps dans les fonctions appelées par cette fonction.
URL | URL (s) dans laquelle le frame de pile s’est produit. Les appels de fonction provenant du navigateur (API Web basées sur des normes) portent le libellé *[DOM]*.

## Associés

| Action                         | Raccourci     |
|:-------------------------------|:-------------|
| Démarrer/arrêter la session de profilage | `Ctrl` + `E` |
| Importer une session de profil       | `Ctrl` + `O` |
| Exporter la session de profilage       | `Ctrl` + `S` |

## Problèmes connus

### Une erreur s’est produite lors du démarrage de la session de profilage

Si vous voyez ce message d’erreur: **une erreur s’est produite lors du démarrage de la session de profilage** dans l’outil performance, procédez comme suit pour contourner le problème.

1. Appuyez sur `Windows Key`  +  `R` .

2. Dans la boîte de dialogue Exécuter, entrez **services. msc**.
![problèmes connus-1](./media/known_issues_1.PNG)

3. Recherchez le **service collecteur standard de Diagnostics Microsoft (R)** et cliquez dessus avec le bouton droit.
![problèmes connus-2](./media/known_issues_2.PNG)

4. Redémarrez le **service de collecteur standard de Diagnostics Microsoft (R)**.
![problèmes connus-3](./media/known_issues_3.PNG)

5. Fermez les outils de développement Microsoft Edge et l’onglet. Ouvrez un nouvel onglet, accédez à votre page, puis appuyez sur `F12` .

6. Vous devriez maintenant être en mesure de commencer le profilage.
![problèmes connus-4](./media/known_issues_4-performance.PNG)

Vous rencontrez encore des problèmes? Envoyez-nous vos commentaires à l’aide de l’icône d' **envoi de commentaires** ! 

![problèmes connus-5](./media/known_issues_5.PNG)

### Une erreur s’est produite lors de l’arrêt de la session de profilage.

Si vous voyez ce message d’erreur: **une erreur s’est produite lors de l’arrêt de la session de profilage** dans l’outil de performance, procédez comme suit pour contourner le problème.

1. Appuyez sur `Windows Key`  +  `R` .

2. Dans la boîte de dialogue Exécuter, entrez **services. msc**.
![problèmes connus-1](./media/known_issues_1.PNG)

3. Recherchez le **service collecteur standard de Diagnostics Microsoft (R)** et cliquez dessus avec le bouton droit.
![problèmes connus-2](./media/known_issues_2.PNG)

4. Redémarrez le **service de collecteur standard de Diagnostics Microsoft (R)**.
![problèmes connus-3](./media/known_issues_3.PNG)

5. Fermez les outils de développement Microsoft Edge et l’onglet. Ouvrez un nouvel onglet, accédez à votre page, puis appuyez sur `F12` .

6. Vous devriez maintenant être en mesure de commencer le profilage.
![problèmes connus-4](./media/known_issues_4-performance.PNG)

Vous rencontrez encore des problèmes? Envoyez-nous vos commentaires à l’aide de l’icône d' **envoi de commentaires** ! 

![problèmes connus-5](./media/known_issues_5.PNG)
