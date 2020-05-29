---
title: Ouvrir Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 48f80ea9f85bd3509f2ba3d834f99c25247c0761
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601886"
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

Lorsque vous voulez examiner les styles ou les attributs d’un nœud DOM, cliquez avec le bouton droit sur l’élément, puis sélectionnez **inspecter**.  

> ##### Figure1  
> Option **inspecter**  
> ![Option inspecter][ImageInspectOption]  

Ou appuyez sur `Control` + `Shift` + `C` \ (Windows \) ou `Command` + `Option` + `C` \ (MacOS \).  

<!--See [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## Ouvrir le panneau Console pour afficher les messages enregistrés ou exécuter JavaScript   

`Control` + `Shift` + `J` Pour accéder directement au panneau de la console, appuyez sur \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \). **Console**  

<!--See [Get Started With The Console][ConsoleGetStarted].  -->

## Ouvrir le dernier panneau ouvert   

Appuyez sur `Control` + `Shift` + `I` \ (Windows \) ou `Command` + `Option` + `I` \ (MacOS \).  

## Ouvrez DevTools à partir du menu principal de Microsoft Edge  

Cliquez sur **paramètres, puis sur plus \ (Alt + F \)** `...` et sélectionnez **autres outils**de développement outils de  >  **développement**.  

> ##### Figure 2  
> Ouverture de DevTools à partir du menu principal de Microsoft Edge  
> ![Ouverture de DevTools à partir du menu principal de Microsoft Edge][ImageOpenFromMain]  

## Ouverture automatique DevTools sur chaque nouvel onglet   

Ouvrez Microsoft Edge à partir de la ligne de commande et transmettez l' `--auto-open-devtools-for-tabs` indicateur.  

Windows \ (CMD \):  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

Windows \ (PowerShell \):  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

MacOS  

```bash
/Applications/Microsoft\ Edge\ Beta.app/Contents/MacOS/Microsoft\ Edge\ Beta --auto-open-devtools-for-tabs
```  

 



<!-- image links -->  

[ImagesMainIcon]: /microsoft-edge/devtools-guide-chromium/media/main-menu-icon.msft.png  

[ImageInspectOption]: /microsoft-edge/devtools-guide-chromium/media/bing-right-click-inspect.msft.png "Figure 1: option inspecter"  
[ImageOpenFromMain]: /microsoft-edge/devtools-guide-chromium/media/bing-customize-more-tools-developer-tools-transparent.msft.png "Figure 2: ouverture de DevTools à partir du menu principal de Microsoft Edge"  

<!-- links -->  

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
