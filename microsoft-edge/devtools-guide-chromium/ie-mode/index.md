---
description: Le mode IE et Microsoft Edge (Chromium) DevTools
title: Mode Internet Explorer et DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, développement web, outils f12, devtools, ie11, internet explorer 11, mode ie
ms.openlocfilehash: 070bf970c784b4f2173ebc52e4494fc6807b4a8e
ms.sourcegitcommit: 7cba715ef71cbac4ee0ebe8f07c0c0e4a2c64221
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11643234"
---
# <a name="internet-explorer-mode-and-the-devtools"></a>Mode Internet Explorer et DevTools  

Cet article explique comment le mode Internet Explorer \(IE mode\) s’intègre à l’Microsoft Edge \(Chromium\) DevTools.  

## <a name="understanding-ie-mode"></a>Comprendre le mode IE  

Le mode IE permet aux entreprises de spécifier une liste de sites web qui fonctionnent uniquement dans Internet Explorer 11.  Lorsque vous accédez à ces sites web dans Microsoft Edge \(Chromium\), une instance d’Internet Explorer 11 s’exécute et restituer le site dans un onglet.  Cette fonctionnalité permet aux entreprises de gérer la compatibilité avec les technologies qui ne sont actuellement compatibles avec aucun navigateur web moderne.  La prise en charge des technologies suivantes est incluse en mode IE.  

*   Modes de document d’IE  
*   contrôles ActiveX ;  
*   autres composants hérités  

En mode IE, le processus de rendu est basé sur Internet Explorer 11.  Le Microsoft Edge de processus \(Chromium\) gère la durée de vie du processus de rendu.  Il est limité à la durée de vie de l’onglet pour un site spécifique \(ou une application\).  Lorsqu’un onglet s’affiche en mode IE, un badge apparaît dans la barre d’adresses de l’onglet spécifique.  

:::image type="complex" source="../media/ie-mode-badge.msft.png" alt-text="Badge du mode IE dans la barre d’adresses" lightbox="../media/ie-mode-badge.msft.png":::
   Badge du mode IE dans la barre d’adresses  
:::image-end:::  

Le mode IE est actuellement disponible sur Windows 10 version 1903 \(mise à jour de mai 2019\), mais il sera bientôt disponible pour toutes les plateformes Windows pris en charge.  

## <a name="launching-the-devtools-on-a-tab-in-ie-mode"></a>Lancement de DevTools sur un onglet en mode IE  

Si vous essayez d’afficher le mode document d’un site web en mode IE, choisissez le badge dans la barre d’adresses.  

:::image type="complex" source="../media/ie-mode-badge-doc-mode.msft.png" alt-text="Afficher le mode document à l’aide du badge du mode IE" lightbox="../media/ie-mode-badge-doc-mode.msft.png":::
   Afficher le mode document à l’aide du badge du mode IE  
:::image-end:::  

Si un onglet utilise le mode IE, les DevTools ne fonctionnent pas et les conditions suivantes se produisent.

*   Si vous sélectionnez ou sélectionnez, une instance vide de l’Microsoft Edge `F12` `Ctrl` + `Shift` + `I` \(Chromium\) DevTools est lancée et affiche le message suivant.  
    
    ```text
    Developer Tools are not available in Internet Explorer mode.  To debug the page, open it in Internet Explorer 11.
    ```  
    
*   Si vous ouvrez un menu contextuel \(clic droit\) et choisissez **Afficher la source,** Bloc-notes est lancée.  
*   Si vous ouvrez un menu contextuel \(clic droit\), **l’élément Inspect n’est** pas visible.  

La raison pour laquelle un certain nombre d’outils **** au **** sein de DevTools \(comme les outils réseau et performance\) ne fonctionnent pas est que le moteur de rendu passe de Chromium à Internet Explorer 11 en mode IE.  Pour fournir des commentaires, accédez à La mise en [contact avec l Microsoft Edge devTools.](#getting-in-touch-with-the-microsoft-edge-devtools-team)  

:::image type="complex" source="../media/ie-mode-devtools.msft.png" alt-text="DevTools lancé en mode IE" lightbox="../media/ie-mode-devtools.msft.png":::
   DevTools lancé en mode IE  
:::image-end:::  

Pour tester votre site web Internet Explorer 11 \(ou application\) en mode Internet Explorer 11 et Internet Explorer, effectuez les étapes suivantes.  

1.  Ouvrez Internet Explorer 11.  
    *   Sur Windows 10, recherchez le raccourci pour Internet Explorer 11.
        1.  **Menu Démarrer**  >  **Windows accessoires**  >  **Internet Explorer 11**.  
    *   Sur Windows 7, recherchez Internet Explorer 11.
        1.  **Menu Démarrer**  >  **Internet Explorer 11**.  
1.  Dans Internet Explorer 11, ouvrez la même page web.  
1.  Lancez Internet Explorer DevTools.  
    *   Sélectionnez `F12` .  
    *   Pointez n’importe où, ouvrez un menu contextuel \(clic droit\), puis choisissez **l’élément Inspect**.  Pour plus d’informations sur l’utilisation de ces outils, accédez à Utiliser les outils de [développement F12.][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]  

Si Internet Explorer 11 n’est pas disponible, comme sur Windows 11, vous pouvez utiliser IEChooser pour lancer Internet Explorer DevTools pour déboguer le contenu de vos onglets en mode IE. Pour utiliser IEChooser, effectuez les étapes suivantes.

1.  Ouvrez IEChooser.
    1. Ouvre la boîte de dialogue Exécuter. Par exemple, appuyez sur `Windows logo key`  +  `R` le .
    2. Entrez, `%systemroot%\system32\f12\IEChooser.exe` puis sélectionnez **OK.**
2.  Dans IEChooser, sélectionnez l’entrée de l’onglet mode IE.


## <a name="remote-debugging-and-ie-mode"></a>Débogage à distance et mode IE  

Lancez Microsoft Edge \(Chromium\) avec débogage à distance allumé à partir de l’interface de ligne de commande.  Microsoft Visual Studio, Microsoft Visual Studio Code et d’autres outils de développement exécutent généralement une commande pour lancer Microsoft Edge.  La commande suivante lance Microsoft Edge port de débogage `9222` distant.  

```shell
start msedge --remote-debugging-port=9222
```  

Après avoir lancé Microsoft Edge \(Chromium\) à l’aide d’un argument de ligne de commande, le mode IE n’est pas disponible.  Vous pouvez toujours accéder aux sites web \(ou applications\) qui sont affichés en mode IE.  Le contenu du site web \(ou application\) s’Chromium, et non d’Internet Explorer 11.  Attendez-vous à ce que les parties des pages web qui reposent sur IE11, telles que ActiveX contrôles, ne s’restituer pas correctement.  Le badge du mode IE n’apparaît pas dans la barre d’adresses.  

Le mode IE reste indisponible tant que vous n’avez pas complètement fermé et redémarré Microsoft Edge \(Chromium\).  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]: /previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85) "Utilisation des outils de développement F12 | Documents Microsoft"  
