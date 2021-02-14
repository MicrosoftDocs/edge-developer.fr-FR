---
description: Découvrir les outils de développement Microsoft Edge (Chromium)
title: Outils de développement Microsoft Edge (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 05b757b7cb399815d072b9d6038873cfd118a59d
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327490"
---
# Présentation des outils de développement Microsoft Edge (Chromium)  

Microsoft Edge a adopté le projet open source Chromium.  Le nouveau navigateur Microsoft Edge crée une meilleure compatibilité web et réduit la fragmentation des différentes plateformes web.  La modification doit vous permettre de créer et de tester plus facilement vos pages web dans Microsoft Edge.  Le nouveau Microsoft Edge doit aider vos pages web à fonctionner comme prévu lorsqu’elles sont ouvertes dans d’autres navigateurs basés sur Chromium.  Les navigateurs basés sur Chromium incluent Google Chrome, Chrome, Opera, Firefox et le nouveau Microsoft Edge.  

L’utilisation du web s’est développée dans un tableau toujours plus vaste de types d’appareils.  La complexité et la surcharge impliquées dans le test des pages web ont rapidement augmenté.  Les développeurs Web tels que vous devez tester sur de nombreux systèmes différents.  Pour vous assurer que vos pages web fonctionnent bien sur tous les types d’appareils et navigateurs, il se peut qu’il soit presque impossible, en particulier si vous travaillez dans une petite entreprise.  Le nouveau Microsoft Edge est désormais basé sur Chromium.  L’équipe Microsoft Edge a simplifié la matrice en alignant la plateforme web Microsoft Edge avec d’autres navigateurs basés sur Chromium.  Le nouveau Microsoft Edge offre une expérience de développement de pointe.  L’expérience est accomplie à l’intérieur du navigateur et avec les autres outils de développement que vous utilisez tous les jours, tels que Visual Studio Code.  

En tant que développeur de navigateur basé sur Chromium, vous devez vous sentir à l’aise avec le nouveau navigateur Microsoft Edge.  Microsoft Edge \(Chromium\) DevTools fonctionne comme les outils de développement que vous connaissez et utilisez déjà.  Les outils de développement Microsoft Edge \(Chromium\) sont souvent appelés Microsoft Edge \(Chromium\) DevTools ou DevTools.  Pour plus d’informations, accédez aux nouveautés de [Microsoft Edge (Chromium) DevTools.][DevtoolsGuideChromiumWhatsNewIndex]  

:::image type="complex" source="./media/devtools.png" alt-text="Microsoft Edge (Chromium) DevTools" lightbox="./media/devtools.png":::
   Microsoft Edge (Chromium) DevTools  
:::image-end:::  

Si vous avez précédemment développé pour Microsoft Edge \(EdgeHTML\) et que vous évaluez le nouveau Microsoft Edge, il fournit désormais de nouveaux outils pour créer et tester vos pages web plus facilement et plus rapidement.  

## Ouvrez DevTools  

Microsoft Edge DevTools est un ensemble d’outils intégrés directement au navigateur Microsoft Edge.  DevTools vous permet d’effectuer les tâches suivantes directement dans le navigateur.  

*   Inspecter et apporter des modifications à votre page web HTML  
*   Modifiez CSS et affichez instantanément un aperçu du rendu de votre page web  
*   Passer en revue toutes `console.log()` les instructions de votre code JavaScript frontal  
*   Déboguer votre script, définir des points d’arrêt et passer pas à pas de votre code ligne par ligne  
    
Plus d’exemples de fonctionnalités fournies par DevTools pour faciliter et accélérer la construction et le test de votre page web dans Microsoft Edge.  

Pour ouvrir devTools  

*   Sélectionner `F12` 
*   Sélectionnez `Ctrl` + `Shift` + `I` \(Windows/Linux\) ou `Command` + `Option` + `I` \(macOS\)  
    
Si vous souhaitez voir le code HTML ou CSS d’un élément sur votre site, cliquez avec le bouton droit sur l’élément et choisissez **Inspecter** pour passer à **l’outil Éléments.**  Pour ouvrir devTools en **mode Inspect Element,** sélectionnez `Ctrl` + `Shift` + `C` \(Windows/Linux\) ou `Command` + `Option` + `C` \(macOS\). Le **mode Inspect Element vous** permet de choisir un élément sur la page web et d’afficher le code HTML et CSS dans **l’outil Elements.**  

Si vous souhaitez consulter les journaux à partir de votre code JavaScript frontal ou exécuter rapidement un script, ouvrez la **console.**   Pour lancer **l’outil Console** dans DevTools, sélectionnez `Ctrl` + `Shift` + `J` \(Windows/Linux\) ou `Command` + `Option` + `J` \(macOS\).  

## Outils principaux  

:::image type="complex" source="./media/devtools-core-tools.png" alt-text="Outils principaux de Microsoft Edge (Chromium) DevTools" lightbox="./media/devtools-core-tools.png":::
   Outils principaux de Microsoft Edge (Chromium) DevTools  
:::image-end::: 

Microsoft Edge \(Chromium\) DevTools inclut les outils suivants.  

*   Outil **Elements permettant** de modifier le code HTML et CSS, d’inspecter les propriétés d’accessibilité, d’afficher les écouteurs d’événements et de définir des points d’arrêt de la mutation DOM  
*   Une **console pour** examiner et filtrer les messages du journal, inspecter les objets JavaScript et les nodes DOM, et exécuter JavaScript dans le contexte de la fenêtre ou du cadre sélectionné  
*   Un **outil Sources** pour ouvrir et modifier votre code, définir des points d’arrêt, passer du code pas à pas et afficher l’état de votre page web
*   Outil **réseau permettant** de surveiller et d’inspecter les demandes et les réponses provenant du cache du réseau et du navigateur   
*   Un **outil de** performances pour profiler le temps et les ressources système requis par votre site  
*   Un **outil mémoire pour** mesurer votre utilisation des ressources mémoire et comparer des instantanés de tas à différents états du runtime de code  
*   Outil **d’application** permettant d’inspecter, de modifier et de déboguer des manifestes d’application web, des travailleurs de service et des caches de travail de service.  Vous pouvez également inspecter et gérer le stockage, les bases de données et les caches à partir de **l’outil Application.**  
*   Outil **de** sécurité permettant de déboguer les problèmes de sécurité et de vous assurer que vous avez correctement implémenté HTTPS sur votre page web.  HTTPS fournit une sécurité et une intégrité des données essentielles pour votre site et vos utilisateurs qui fournissent des informations personnelles sur votre site.  
*   Un **outil Audits** \(désormais renommé **Contrôle**\) pour exécuter un audit de votre page web.  Les résultats de l’audit vous aident à améliorer la qualité de votre site des manières suivantes.  
    *   Catch common errors related to making your webpage accessible, secure, performant, and so on.  
    *   Corrigez chaque erreur.  
    *   Créez un PWA.  
        
[!INCLUDE [audits-panel-note](./includes/audits-panel-note.md)]  

Envoyez vos [commentaires et demandes de fonctionnalités.](#getting-in-touch-with-the-microsoft-edge-devtools-team)  

## Extensions  

Vous avez peut-être accédé à DevTools à l’aide d’extensions lorsque vous avez diagnostiquer et déboté des problèmes pendant que vous avez créé vos pages web \(ou applications\). Les extensions Microsoft Edge sont acquises auprès des [extensions Microsoft Edge.][MicrosoftEdgeAddonsExtensions]  Sur [les extensions Microsoft Edge,][MicrosoftEdgeAddonsExtensions]parcourez les extensions DevTools à partir de la catégorie Outils de développement ou recherchez une extension spécifique. ****  

Vous pouvez également ajouter des extensions à partir du [Chrome Web Store.][GoogleChromeWebstoreExtensions]  

:::image type="complex" source="./media/allow-extensions-from-stores.png" alt-text="Chrome Web Store dans Microsoft Edge" lightbox="./media/allow-extensions-from-stores.png":::
   Chrome Web Store dans Microsoft Edge  
:::image-end:::  

Dans la partie supérieure, choisissez **Autoriser les extensions** d’autres magasins, puis sélectionnez **Autoriser** dans la boîte de dialogue qui s’affiche.  

> [!NOTE]
> Les extensions installées à partir de sources autres que le Microsoft Store ne sont pas vérifiées et peuvent affecter les performances du navigateur.  

Choisissez **Ajouter à Chrome** pour ajouter votre extension DevTools à Microsoft Edge.  

:::image type="complex" source="./media/install-extension-from-chrome-store.png" alt-text="Ajouter une extension du Chrome Web Store à Microsoft Edge" lightbox="./media/install-extension-from-chrome-store.png":::
   Ajouter une extension du Chrome Web Store à Microsoft Edge  
:::image-end:::  

## Raccourcis  

Les raccourcis suivants contrôlent la fenêtre principale de DevTools, fonctionnent dans tous les outils ou les deux.  

| Action | Windows/Linux | macOS |  
|:--- |:--- | :--- |  
| Afficher/Masquer DevTools \(s’ouvre au dernier outil vu\) | `F12` ou `Ctrl`+`Shift`+`I` | `Command`+`Option`+`I` |  
| Afficher la console | `Ctrl`+`Shift`+`J` | `Command`+`Option`+`J` |  
| Afficher les DevTools en **mode Inspect Element** qui vous permet de choisir un élément et d’afficher le code HTML et CSS dans l’outil **Elements** | `Ctrl`+`Shift`+`C` | `Command`+`Option`+`C` |  
| Afficher les paramètres | `?` ou `Fn`+`F1` | `?` ou `Fn`+`F1` |  
| Afficher le panneau suivant | `Ctrl`+`]` | `Command`+`]` |  
| Afficher le panneau précédent | `Ctrl`+`[` | `Command`+`[` |  
| Ancrez les DevTools à la dernière position utilisée.  Si les DevTools restent à la position par défaut pour toute la session, le raccourci dissocie les DevTools dans une fenêtre distincte. | `Ctrl`+`Shift`+`D` | `Command`+`Shift`+`D` |  
| Toggle **Device Mode** | `Ctrl`+`Shift`+`M` | `Command`+`Shift`+`M` |  
| Toggle **Inspect Element Mode** that allows to you to choose an element and display the HTML and CSS in the **Elements** tool | `Ctrl`+`Shift`+`C` | `Command`+`Shift`+`C` |  
| Afficher le menu Commande | `Ctrl`+`Shift`+`P` | `Command`+`Shift`+`P` |  
| Afficher/masquer le caisse | `Esc` | `Esc` |  
| Mise.  Actualise la page web à l’aide du cache.  | `F5` ou `Ctrl`+`R` | `Command`+`R` |  
| Actualisation en dur.  Force Microsoft Edge à télécharger à nouveau les ressources et à les recharger.  Les ressources utilisées peuvent être provenant d’une version mise en cache | `Ctrl`+`F5` ou `Ctrl`+`Shift`+`R` | `Command`+`Shift`+`R` |  
| Recherchez du texte dans le panneau actuel.  Non pris en charge dans les outils Audits, Application et Sécurité | `Ctrl`+`F` | `Command`+`F` |  
| Afficher l’outil de recherche dans le caisse, ce qui vous permet de rechercher du texte sur toutes les ressources chargées | `Ctrl`+`Shift`+`F` | `Command`+`Option`+`F` |  
| Ouvrir un fichier dans le panneau Sources | `Ctrl`+`O` ou `Ctrl`+`P` | `Command`+`O` ou `Command`+`P` |  
| Zoom avant | `Ctrl`+`Shift`+`+` | `Command`+`Shift`+`+` |  
| Zoom arrière | `Ctrl`+`-` | `Command`+`-` |  
| Restaurer le niveau de zoom par défaut | `Ctrl`+`0` | `Command`+`0` |  
| Exécuter l’extrait de code | `Ctrl`+`O`ou `Ctrl` + `P` , `!` tapez suivi du nom du script, puis appuyez sur `Enter` | Appuyez `Command` + `O` `Command` + `P` ou , `!` tapez suivi du nom du script, puis appuyez sur `Enter` |  
| Afficher le code source HTML non modifiable dans un nouvel onglet | `Ctrl`+`U` | Non applicable |  

> [!NOTE]
> Si vous déboguer et que vous êtes suspendu à un point d’arrêt, le **raccourci** Actualiser reprend d’abord l’runtime.  

## Voir également  

*   [DevTools pour les débutants : mise en place du code HTML et du DOM][DevtoolsGuideChromiumBeginnersHtml]  
*   [Protocole DevTools Microsoft Edge (Chromium)][DevtoolsProtocolChromiumIndex]  
    
## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

Si vous souhaitez prévisualiser les dernières fonctionnalités à venir dans [DevTools][DevtoolsGuideChromiumWhatsNewIndex], téléchargez [Microsoft Edge Canary][MicrosoftedgeinsiderDownload], qui est builds tous les soirs.  

<!-- links -->  

[DevtoolsGuideChromiumBeginnersHtml]: /microsoft-edge/devtools-guide-chromium/beginners/html "DevTools pour les débutants : mise en place du code HTML et du dom | Documents Microsoft"  
[DevtoolsGuideChromiumWhatsNewIndex]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/11/devtools "Nouveautés de Microsoft Edge (Chromium) DevTools | Documents Microsoft"  
[DevtoolsProtocolChromiumIndex]: /microsoft-edge/devtools-protocol-chromium "Protocole Microsoft Edge (Chromium) DevTools | Documents Microsoft"  

[MicrosoftEdgeAddonsExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Microsoft Edge Add-ons"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  

[GoogleChromeWebstoreExtensions]: https://chrome.google.com/webstore/category/extensions "Extensions | Chrome Web Store"  
