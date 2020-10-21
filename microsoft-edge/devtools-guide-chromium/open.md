---
description: Toutes les méthodes d’ouverture de Microsoft Edge DevTools.
title: Ouvrir Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 298edeebc99d858306938e4a876e8ef03a371f2c
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125404"
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
*   Sélectionnez `Control` + `Shift` + `C` \ (Windows, Linux \) ou `Command` + `Option` + `C` \ (MacOS \).  Pour plus d’informations, accédez à [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].  

:::image type="complex" source="./media/bing-right-click-inspect.msft.png" alt-text="L’option * * Inspect * *" lightbox="./media/bing-right-click-inspect.msft.png":::
   Option **inspecter**  
:::image-end:::  

<!--See [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## Ouvrir l’écran de la console  

Chacune des tâches suivantes vous permet d’ouvrir le volet de [console][DevToolsConsoleIndex] pour afficher les messages enregistrés ou exécuter JavaScript.  

*   Pour ouvrir le volet [console][DevToolsConsoleIndex] , procédez comme suit:  
    
    1.  [Ouvrez devtools](#open-microsoft-edge-devtools).  
    1.  Sélectionnez le volet de la [console][DevToolsConsoleIndex] .  

*   Pour accéder directement au volet de la [console][DevToolsConsoleIndex] , sélectionnez `Control` + `Shift` + `J` \ (Windows, Linux \) ou `Command` + `Option` + `J` \ (MacOS \).  Pour plus d’informations, accédez à [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].  

<!--See [Get Started With The Console][ConsoleGetStarted].  -->

## Ouvrir le panneau précédent  

Pour accéder au panneau précédent que vous avez ouvert, sélectionnez `Control` + `Shift` + `I` \ (Windows, Linux \) ou `Command` + `Option` + `I` \ (MacOS \).  Pour plus d’informations, accédez à [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].  

## Ouvrir Microsoft Edge DevTools  

Chacune des tâches suivantes vous permet d’ouvrir DevTools.  

*   Pour ouvrir Microsoft Edge DevTools, procédez comme suit:  
    
    1.  Sélectionnez l'  `...` icône ( **paramètres et plus** ).  
    1.  Sélectionnez **autres outils**.  
    1.  Choisissez **outils de développement**.  
    
*   Pour ouvrir Microsoft Edge devtools, sélectionnez `F12` ou `Control` + `Shift` + `I` \ (Windows, Linux \) ou `Command` + `Option` + `I` \ (MacOS \).  Pour plus d’informations, accédez à [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].  

:::image type="complex" source="./media/bing-customize-more-tools-developer-tools-transparent.msft.png" alt-text="L’option * * Inspect * *" lightbox="./media/bing-customize-more-tools-developer-tools-transparent.msft.png":::
   Ouvrez DevTools à partir du menu principal de Microsoft Edge  
:::image-end:::  

## Ouverture automatique DevTools sur chaque nouvel onglet  

Pour ouvrir automatiquement DevTools sur chaque nouvel onglet, ouvrez Microsoft Edge à partir de la ligne de commande et transmettez l' `--auto-open-devtools-for-tabs` indicateur.  

#### [CMD (Windows)](#tab/cmd-Windows/)  

<a id="auto-open-devtools-command-line"></a>  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

#### [PowerShell (Windows)](#tab/powershell-Windows/)  

<a id="auto-open-devtools-command-line"></a>  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

#### [bash (macOS)](#tab/bash-macos/)  

<a id="auto-open-devtools-command-line"></a>  

```bash
/Applications/Microsoft\ Edge\ Beta.app/Contents/MacOS/Microsoft\ Edge\ Beta --auto-open-devtools-for-tabs
```  

#### [bash (Linux)](#tab/bash-linux/)  

<a id="auto-open-devtools-command-line"></a>  

```bash
microsoft-edge-dev --auto-open-devtools-for-tabs
```  

* * *  

## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

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
