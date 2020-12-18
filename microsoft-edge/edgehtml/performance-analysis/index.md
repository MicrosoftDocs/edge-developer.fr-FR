---
description: Utilisez les outils de développement F12 pour analyser les performances générales des sites Web.
title: Analyse des performances
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 7a5f9fd0-90a9-43db-b271-178c06da5896
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.date: 12/15/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e585d07ebae547319c16b6eea579ad26ffb84ce3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233286"
---
# Analyse des performances  

Si vous débutez sur les performances, consultez le [Guide devtools F12](../devtools-guide/index.md).
Les [Outils F12](../devtools-guide/index.md) intégrés à Microsoft Edge peuvent être utilisés pour analyser les performances générales d’un site Web.  Il fournit des fonctionnalités similaires (mais plus limitées) au [Kit de performances Windows](/windows-hardware/test/wpt/index)  

Si vous souhaitez une analyse plus approfondie des performances du navigateur, l’équipe Microsoft Edge utilise le [Kit Windows performance Toolkit](/windows-hardware/test/wpt/index) (WPT).  Le programme WPT a été créé par l’équipe Windows pour effectuer une analyse approfondie des performances du programme.  Il s’entoure des limites entre le site Web JavaScript et le code natif Microsoft Edge, ce qui permet d’afficher les deux dans le même outil.  WPT peut être utilisé pour:  

*   Mesurer le temps UC nécessaire pour que le logiciel fonctionne  
*   Calculer la quantité de mémoire allouée par le logiciel  
*   Afficher les détails du téléchargement de fichiers à partir de serveurs distants  
*   Mesurer la fréquence d’images.  

Pour commencer à utiliser Windows performance Toolkit pour analyser votre site Web, vous devez commencer par Télécharger le kit de [déploiement d’évaluation et de déploiement de Windows 10 (ADK)](https://developer.microsoft.com/windows/hardware/windows-assessment-deployment-kit).  Sélectionnez l’option *Windows performance Toolkit* lors de l’installation:  

![Options d’installation de ADK](./media/adk-installoptions.png)  

Ici, nous allons vous expliquer comment enregistrer et analyser un suivi des performances.  
Pour en savoir plus sur ce qui est inclus dans le kit de performances Windows, consultez la documentation de la fonction [WPT](/windows-hardware/test/wpt/index)complète.  

## Enregistrement d’une trace  

Configurez ensuite votre scénario utilisateur et préparez-vous à recueillir un suivi à l’aide de l’enregistreur de performance Windows.  
Voici comment profiler votre scénario Web avec l' *enregistreur de performance Windows (WPR)*.  

### 1. préparer votre environnement pour collecter une trace de performance  

Fermez autant de programmes en cours d’exécution que possible pour éviter le bruit dans la trace que vous allez enregistrer.  Idéalement, le seul logiciel exécuté sera l’enregistreur de performance Windows (WPR) et le navigateur.  

### 2. lancer l’enregistreur de performance Windows (WPR) et sélectionner des options  

Lancez l’enregistreur de performance Windows et assurez-vous que le bouton bascule **plus d’options** est étendu.  Activez les cases à cocher *navigateur Edge* et analyse du scénario de *réactivité html* .  

![Options d’enregistrement de performance Windows](./media/wprui-options.png)  

#### Conseils et astuces pour la collecte des traces  

*   Tentez de limiter les activités en arrière-plan à un minimum requis minimum.  Les processus en arrière-plan peuvent incliner les performances perçues et les caractéristiques de performance réelles et affecter les résultats.  Idéalement, il n’y a aucune autre application en cours d’exécution en regard de browser et WPR.  
*   Identifiez les scénarios que vous analysez et essayez de les conserver aussi atomiques que possible.  Par exemple, si votre site rencontre des problèmes de performances lors du chargement de la page, du défilement et de la sélection d’un texte dans un tableau, séparez les problèmes en trois circonstances:  
    *   Chargement de la page (du début de la navigation vers la fin du chargement de la page)  
    *   Scroll  
    *   Sélection d’un texte dans le tableau  
*   S’il s’agit d’un scénario impliquant la navigation sur un site, vous pouvez commencer le scénario à propos de: Blank.  À partir de: Blank évite la surcharge de la page précédente.  S’il s’agit de la navigation hors d’un site, accédez à à propos de pour terminer le scénario.  Ainsi, le bruit d’autres sites n’est pas conservé hors du suivi, sauf si l’interaction spécifique entre les sites est le problème faisant l’objet d’une enquête.  

### 3. enregistrer le scénario  

Cliquez sur **Démarrer** pour démarrer l’enregistrement.  L’outil rapportera la taille de mémoire tampon qu’il utilise pour vous aider à prévoir la taille du fichier généré.  Effectuez le scénario d’utilisation que vous voulez mesurer, puis cliquez sur **Enregistrer** pour arrêter l’enregistrement et enregistrer la trace.  L’enregistrement immédiat après la fin de votre scénario permet de réduire la taille du fichier de suivi.  

![Enregistrement de début de l’enregistrement de performance Windows](./media/wprui-recording.png)  

L’outil WPR indiquera que vos informations de suivi ont bien été enregistrées:  

![Début de l’enregistrement de performance Windows-enregistrement terminé](./media/wprui-savecomplete.png)  

## Analyse d’une trace  

À présent que vous avez rassemblé vos données de performance, vous pouvez analyser le suivi à l’aide de Windows Performance Analyzer pour découvrir les optimisations qui peuvent être effectuées.  
Voici comment analyser les données de performances de votre scénario Web.  

### 1. Ouvrez l’analyseur de performance Windows (WAP)  

Lancez Windows Performance Analyzer et ouvrez le `.etl` fichier à analyser (**fichier**  >  **ouvert...**).  

### 2. charger des symboles et appliquer le profil d' *analyse html*  

> [!WARNING]
> Le chargement des symboles pour la première fois nécessite un téléchargement volumineux et prend un certain temps sur une connexion Internet classique.  

Pour charger vos symboles, sélectionnez **tracer**  >  les**symboles de chargement** dans le menu.  Les symboles seront mis en cache sur le disque et les suivis futurs chargeront les symboles beaucoup plus rapidement.  

Vous pouvez charger des symboles considérablement plus rapidement en restreignant le chargement à Microsoft Edge et à l’hôte des applications Web.  Sélectionnez **trace**  >  **configurer les symboles** et limiter les **paramètres de chargement** à uniquement `MicrosoftEdgeCP.exe` et `WWAHost.exe` .  

![Restrictions relatives aux symboles](./media/wpa-symbolrestrictions.png)  

Après le chargement des symboles, appliquez le *Profil html Analysis* (les**profils**  >  **s’appliquent...**  >  ) **Parcourir le catalogue...**  >  **HtmlResponsivenessAnalysis. wpaProfile**)  
Le profil charge plusieurs graphiques et tableaux pour votre analyse.  Pour presque toutes les enquêtes sur le site Web, nous vous recommandons de commencer par ce profil.  

![Image de grande taille](./media/wpa-bigpicture.png)  

#### Profil analyse de réactivité html  

Le profil d’analyse de *réactivité html* fournit quatre onglets:  

**Grande image** : cette fonctionnalité est utile pour confirmer qu’il n’y a pas de sources inattendues d’activité processeur et que le navigateur utilise réellement toutes les ressources disponibles.  Vérifiez l’utilisation de votre UC et assurez-vous qu’aucun processus ne contribue considérablement à l’utilisation du processeur par le biais du navigateur.  

**Analyse de trames** : cette section est utilisée pour une analyse de base.  Le graphique utilisation de l' *UC (attribué)* vous permet d’obtenir un bref aperçu des sous-systèmes responsables de l’utilisation de l’UC.  Le fractionnement des exemples dans le tableau utilisation de l' *UC (échantillonné)* du *thread d’interface utilisateur HTML* est utile pour identifier les goulots d’étranglement de performance critiques.  

**Marqueurs de trace** -cette section présente tous les marqueurs de suivi provenant du navigateur (Microsoft Edge), y compris *msWriteProfilerMark*, qui fournit des points précis pour la mesure du code.  Pour afficher le suivi de *msWriteProfilerMark* , faites défiler vers le bas jusqu’au graphique  *événements génériques* et sélectionnez **HTML msWriteProfilerMark** dans le menu déroulant.  

**Analyse du délai de thread** -cet onglet est souvent utilisé par les développeurs Microsoft Edge pour déterminer quand un thread est bloqué et en attente sur un autre.  Dans de rares occasions, il peut également être utile pour les développeurs Web.  

### 3. Zoom pour supprimer l’arrêt de la trace  

Vous pouvez vous concentrer sur votre analyse en supprimant les sections vides de l' *arrêt du suivi* de la sélection de vos graphiques.  À partir de n’importe quel graphique actuellement affiché:  
*   Cliquez sur le début des données de graphique que vous voulez examiner.  
*   Mettre en attente, faire glisser et relâcher pour sélectionner la zone de votre choix  
*   Cliquez avec le bouton droit, puis sélectionnez **Zoom**  

Le zoom s’applique à tous les graphiques et graphes de l’onglet actif.  

![Zoom de post](./media/wpa-postzoom.png)  

### 4. identifier les cycles UC  

 Dans l’onglet **analyse de trame** , le tableau utilisation de l' **UC** est l’endroit où votre analyse est susceptible de se produire.  Vous pouvez développer les divers processus pour identifier le code JavaScript et le code de navigateur le plus gourmand en calculs.  Dans de nombreux cas, un seul bit de JavaScript est responsable d’un problème de performance, et le fait d’en prendre le temps de l’optimiser peut faire une différence notable.  

### 5. exploration de tout code JavaScript à exécution lente  

L’analyse de l’appel DOM peut s’avérer utile pour identifier les scripts JavaScript responsables de la mise en attente de la plupart du temps.  Cela est particulièrement utile lorsque de nombreux appels de niveau supérieur utilisent les mêmes bibliothèques JavaScript.  

Commencez par examiner la *répartition de l’utilisation du processeur (par exemple) par processus, thread, activité, pile*.  Cliquez sur n’importe quelle cellule dans la colonne de **pile** .  Appuyez sur *Ctrl + F* et recherchez *ExternalFunctionThunk*.  

> [!NOTE] 
> Cela ne fonctionne que si vous avez correctement chargé les symboles.  

![Rechercher ExternalFunctionThunk](./media/wpa-externalfunctionthunk.png)  

Recherchez les lignes avec *ExternalFunctionThunk*.  Il s’agit de l’interface du moteur JavaScript Chakra au moteur Microsoft Edge.  Il indique l’emplacement des ponts de code du navigateur vers l’exécution JavaScript.  Cliquez avec le bouton droit sur la ligne et sélectionnez **afficher les appels**  >  **par module** pour afficher une liste pondérée des fonctions les plus longues de fonctionnement du moteur de navigateur.  

![Afficher les appelants](./media/wpa-viewcallees.png)  

Pour identifier tout le JavaScript appelant une API spécifique, cliquez dessus avec le bouton droit, puis sélectionnez **afficher les appelants**  >  **par fonction** et développez l’arborescence pour afficher et comparer les pondérations relatives.  
