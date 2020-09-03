---
description: Toutes les méthodes d’ouverture de Microsoft Edge DevTools.
title: Ouvrir Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: ffc05a1eff2cdb7f3020a7dbb853a7520a0502dd
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993596"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License. -->

# Ouvrir Microsoft Edge DevTools  

Il existe de nombreuses façons d’ouvrir Microsoft Edge DevTools, car les utilisateurs différents ont besoin d’un accès rapide à différentes parties de l’interface utilisateur d’DevTools.  

## Ouvrir le panneau des éléments pour vérifier le DOM ou les feuilles CSS  

Chacune des tâches suivantes vous permet d’inspecter les styles ou les attributs d’un nœud DOM.

*   Pointez sur l’élément, ouvrez le menu contextuel, puis cliquez sur **inspecter**.  
*   Appuyez sur `Control` + `Shift` + `C` \ (Windows \) ou `Command` + `Option` + `C` \ (MacOS \).  Pour plus d’informations, reportez-vous à la rubrique [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].  

:::image type="complex" source="./media/bing-right-click-inspect.msft.png" alt-text="L’option * * Inspect * *" lightbox="./media/bing-right-click-inspect.msft.png":::
   Option **inspecter**  
:::image-end:::  

<!--See [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## Ouvrir l’écran de la console  

Chacune des tâches suivantes vous permet d’ouvrir le volet de [console][DevToolsConsoleIndex] pour afficher les messages enregistrés ou exécuter JavaScript.  

*   Pour ouvrir le volet [console][DevToolsConsoleIndex] , procédez comme suit:  
    
    1.  [Ouvrez devtools](#open-microsoft-edge-devtools).  
    1.  Sélectionnez le volet de la [console][DevToolsConsoleIndex] .  

*   Pour accéder directement au volet de la [console][DevToolsConsoleIndex] , appuyez sur `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \).  Pour plus d’informations, reportez-vous à la rubrique [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].  

<!--See [Get Started With The Console][ConsoleGetStarted].  -->

## Ouvrir le panneau précédent  

Pour accéder au panneau précédent que vous avez ouvert, appuyez sur `Control` + `Shift` + `I` \ (Windows \) ou `Command` + `Option` + `I` \ (MacOS \).  Pour plus d’informations, reportez-vous à la rubrique [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].  

## Ouvrir Microsoft Edge DevTools  

Chacune des tâches suivantes vous permet d’ouvrir DevTools.  

*   Pour ouvrir Microsoft Edge DevTools, procédez comme suit:  
    
    1.  Sélectionnez l'  `...` icône ( **paramètres et plus** ).  
    1.  Sélectionnez **autres outils**.  
    1.  Sélectionnez **outils de développement**.  
    
*   Pour ouvrir Microsoft Edge devtools, appuyez `F12` sur `Control` + `Shift` + `I` \ (Windows \) ou `Command` + `Option` + `I` \ (MacOS \).  Pour plus d’informations, reportez-vous à la rubrique [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].  

:::image type="complex" source="./media/bing-customize-more-tools-developer-tools-transparent.msft.png" alt-text="Ouvrez DevTools à partir du menu principal de Microsoft Edge" lightbox="./media/bing-customize-more-tools-developer-tools-transparent.msft.png":::
   Ouvrez DevTools à partir du menu principal de Microsoft Edge  
:::image-end:::  

## Ouverture automatique DevTools sur chaque nouvel onglet  

Pour ouvrir automatiquement DevTools sur chaque nouvel onglet, ouvrez Microsoft Edge à partir de la ligne de commande et transmettez l' `--auto-open-devtools-for-tabs` indicateur.  

#### [CMD (Windows)](#tab/cmd-windows/)  

<a id="selenium-tools-install"></a>  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

#### [PowerShell (Windows)](#tab/powershell-windows/)  

<a id="selenium-tools-install"></a>  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

#### [bash (macOS)](#tab/bash-macos/)  

<a id="selenium-tools-install"></a>  

```bash
/Applications/Microsoft\ Edge\ Beta.app/Contents/MacOS/Microsoft\ Edge\ Beta --auto-open-devtools-for-tabs
```  

* * *  

<!-- links -->  

[DevToolsConsoleIndex]: ./console/index.md "Présentation de la console | Documents Microsoft"  
[DevtoolsShortcuts]: ./shortcuts.md "Raccourcis clavier de Microsoft Edge DevTools-Microsoft documents"  

<!--[ConsoleGetStarted]: /microsoft-edge/devtools-guide-chromium/console/get-started ""  -->  
<!--[GetStartedCSS]: /microsoft-edge/devtools-guide-chromium/css "CSS"  -->

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/open) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
