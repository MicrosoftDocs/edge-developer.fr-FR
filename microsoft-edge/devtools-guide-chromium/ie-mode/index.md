---
description: Mode IE et Microsoft Edge (chrome) DevTools
title: Le mode Internet Explorer et le DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, ie11, Internet Explorer 11, mode IE
ms.openlocfilehash: c88da78e073a75a664561aba899ca5c8ada78477
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232827"
---
# Le mode Internet Explorer et le DevTools  

Cet article décrit comment le mode d’affichage d’Internet Explorer \ (mode IE \) est intégré à Microsoft Edge \ (chrome \) DevTools.  

## Présentation du mode IE  

Le mode IE permet aux entreprises de spécifier une liste de sites Web qui fonctionnent uniquement dans Internet Explorer 11.  Lorsque vous accédez à ces sites Web dans Microsoft Edge \ (chrome \), une instance d’Internet Explorer 11 s’exécute et affiche le site dans un onglet.  Cette fonctionnalité permet aux entreprises de gérer la compatibilité avec des technologies qui ne sont actuellement pas compatibles avec les navigateurs Web modernes.  La prise en charge des technologies suivantes est incluse dans le mode IE.  

*   Modes de document IE  
*   contrôles ActiveX;  
*   autres composants hérités  

Dans le mode IE, le processus de rendu est basé sur Internet Explorer 11.  Le gestionnaire de processus Microsoft Edge \ (chrome \) gère la durée de vie du processus de rendu.  Il est limité à la durée de vie de l’onglet pour un site (ou une application) spécifique.  Lorsqu’un onglet est restitué dans le mode IE, un badge s’affiche dans la barre d’adresses de l’onglet spécifique.  

:::image type="complex" source="../media/ie-mode-badge.msft.png" alt-text="Badge du mode IE dans la barre d’adresses" lightbox="../media/ie-mode-badge.msft.png":::
   Badge du mode IE dans la barre d’adresses  
:::image-end:::  

Le mode IE est actuellement disponible sur Windows 10 version 1903 \ (2019 mise à jour \), mais bientôt disponible sur toutes les plateformes Windows prises en charge.  

## Lancement de DevTools sur un onglet du mode IE  

Si vous essayez d’afficher le mode document d’un site Web dans le mode IE, sélectionnez le badge dans la barre d’adresses.  

:::image type="complex" source="../media/ie-mode-badge-doc-mode.msft.png" alt-text="Afficher le mode document à l’aide du badge du mode IE" lightbox="../media/ie-mode-badge-doc-mode.msft.png":::
   Afficher le mode document à l’aide du badge du mode IE  
:::image-end:::  

Si un onglet utilise le mode IE, le DevTools ne fonctionne pas et les conditions suivantes se produisent.

*   Si vous sélectionnez `F12` ou sélectionnez `Ctrl` + `Shift` + `I` , une instance vide de Microsoft Edge \ (chrome \) devtools est lancée, le message suivant s’affiche.  
    
    ```text
    Developer Tools are not available in Internet Explorer mode.  To debug the page, open it in Internet Explorer 11.
    ```  
    
*   Si vous ouvrez un menu contextuel \ (cliquez avec le bouton droit sur \) et sélectionnez **afficher la source**, le bloc-notes est lancé.  
*   Si vous ouvrez un menu contextuel \ (cliquez avec le bouton droit sur \), l' **élément Inspect** n’est pas visible.  

La raison pour laquelle un certain nombre d’outils à l’intérieur du DevTools \ (comme les outils **réseau** et de **performance** \) ne fonctionne pas, c’est le moteur de rendu qui bascule du chrome vers Internet Explorer 11 en mode IE.  Pour fournir des commentaires, accédez à [l’équipe Microsoft Edge devtools](#getting-in-touch-with-the-microsoft-edge-devtools-team).  

:::image type="complex" source="../media/ie-mode-devtools.msft.png" alt-text="DevTools lancée en mode IE" lightbox="../media/ie-mode-devtools.msft.png":::
   DevTools lancée en mode IE  
:::image-end:::  

Pour tester votre site Web Internet Explorer 11 (ou l’application \) en mode Internet Explorer 11 et IE, procédez comme suit.  

1.  Ouvrez Internet Explorer 11.  
    *   Sur Windows 10, recherchez le raccourci vers Internet Explorer 11.
        1.  **Menu Démarrer**  >  **Accessoires Windows**  >  **Internet Explorer 11**.  
    *   Sur Windows 7, recherchez Internet Explorer 11.
        1.  **Menu Démarrer**  >  **Internet Explorer 11**.  
1.  Ouvrez la même page Web dans Internet Explorer 11.  
1.  Lancez Internet Explorer DevTools.  
    *   Sélectionnez `F12` .  
    *   Positionnez le curseur n’importe où, ouvrez un menu contextuel, puis sélectionnez **inspecter l’élément**.  Pour plus d’informations sur l’utilisation de ces outils, accédez à l' [utilisation des outils de développement F12][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].  

## Débogage à distance et mode IE  

Pour lancer le débogage à distance à partir de l’interface de ligne de commande, lancez Microsoft Edge \ (chrome \).  Dans Visual Studio, le code Visual Studio et d’autres outils de développement, vous pouvez généralement exécuter une commande pour lancer Microsoft Edge.  La commande suivante lance Microsoft Edge avec le port de débogage distant défini sur `9222` .  

```shell
start msedge --remote-debugging-port=9222
```  

Après avoir lancé Microsoft Edge \ (chrome \) à l’aide d’un argument de ligne de commande, le mode IE n’est pas disponible.  Il est possible que vous deviez accéder à des sites Web \ (ou applications \) qui s’affichaient normalement dans le mode IE.  Le contenu du site Web (ou de l’application \) est restitué à l’aide de chrome, et non d’Internet Explorer 11.  Attendez-vous à ce que les parties des pages Web qui s’appuient sur IE11, comme les contrôles ActiveX, ne s’affichent pas correctement.  Le badge du mode IE n’apparaît pas dans la barre d’adresses.  

Le mode IE reste indisponible tant que vous n’avez pas complètement fermé et redémarré Microsoft Edge \ (chrome \).  

## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]: /previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85) "Utiliser les outils de développement F12 | Documents Microsoft"  
