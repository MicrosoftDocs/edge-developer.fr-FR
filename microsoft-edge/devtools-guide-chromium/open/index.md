---
description: Toutes les façons d’ouvrir le Microsoft Edge DevTools.
title: Ouvrez Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 00bb5a2c11fcadd4a0eba22c29ac5a2652b9edb6
ms.sourcegitcommit: 2b225426e90b017f9766ea8568713b95d267cd6f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2021
ms.locfileid: "11607314"
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
# <a name="open-microsoft-edge-devtools"></a>Ouvrez Microsoft Edge DevTools  

Il existe plusieurs façons d’ouvrir Microsoft Edge DevTools, car différents utilisateurs souhaitent un accès rapide à différentes parties de l’interface utilisateur DevTools.  

## <a name="open-the-elements-panel-to-inspect-the-dom-or-css"></a>Ouvrir le panneau Éléments pour inspecter le DOM ou CSS  

Chacune des tâches suivantes vous permet d’inspecter les styles ou attributs d’un nœud DOM.

*   Pointez sur l’élément, ouvrez le menu contextuel \(clic droit\), puis choisissez **Inspecter**.  
*   Sélectionnez `Control` + `Shift` + `C` \(Windows, Linux\) ou `Command` + `Option` + `C` \(macOS\).  Pour plus d’informations, [accédez Microsoft Edge raccourcis clavier DevTools.][DevtoolsShortcutsIndex]  

:::image type="complex" source="../media/bing-right-click-inspect.msft.png" alt-text="Option Inspecter" lightbox="../media/bing-right-click-inspect.msft.png":::
   Option **Inspecter**  
:::image-end:::  

<!--Navigate to [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## <a name="open-the-console-panel"></a>Ouvrir le panneau console  

Chacune des tâches suivantes vous permet d’ouvrir le volet [Console][DevtoolsConsoleIndex] pour afficher les messages enregistrés ou exécuter JavaScript.  

*   Utilisez les étapes suivantes pour ouvrir [le volet][DevtoolsConsoleIndex] console.  
    
    1.  [Ouvrez DevTools](#open-microsoft-edge-devtools).  
    1.  Choisissez le [volet][DevtoolsConsoleIndex] console.  

*   Pour aller directement dans [le][DevtoolsConsoleIndex] volet console, sélectionnez `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).  Pour plus d’informations, [accédez Microsoft Edge raccourcis clavier DevTools.][DevtoolsShortcutsIndex]  

<!--Navigate to [Get Started With The Console][ConsoleGetStarted].  -->

## <a name="open-the-previous-panel"></a>Ouvrir le panneau précédent  

Pour passer au panneau précédent que vous avez ouvert, sélectionnez `Control` + `Shift` + `I` \(Windows, Linux\) ou `Command` + `Option` + `I` \(macOS\).  Pour plus d’informations, [accédez Microsoft Edge raccourcis clavier DevTools.][DevtoolsShortcutsIndex]  

## <a name="open-microsoft-edge-devtools"></a>Ouvrez Microsoft Edge DevTools  

Pour ouvrir DevTools, utilisez l’une des options suivantes.  

*   Utilisez l’Microsoft Edge’interface utilisateur.  
    
    1.  Sélectionnez **l Paramètres icône** \( \) et plus > Outils de développement `...` ****  >   **Outils de développement .**  
    
*   Utilisez le clavier.  
    *   Sélectionnez `F12` `Control` + `Shift` + `I` ou \(Windows, Linux\) ou `Command` + `Option` + `I` \(macOS\).  

Pour plus d’informations, [accédez Microsoft Edge raccourcis clavier DevTools.][DevtoolsShortcutsIndex]  

:::image type="complex" source="../media/bing-customize-more-tools-developer-tools-transparent.msft.png" alt-text="Ouvrez DevTools à partir Microsoft Edge menu principal" lightbox="../media/bing-customize-more-tools-developer-tools-transparent.msft.png":::
   Ouvrez DevTools à partir Microsoft Edge menu principal  
:::image-end:::  

## <a name="auto-open-devtools-on-every-new-tab"></a>Ouverture automatique de DevTools sur chaque nouvel onglet  

Pour ouvrir automatiquement DevTools sur chaque nouvel onglet, ouvrez Microsoft Edge à partir de la ligne de commande et passez `--auto-open-devtools-for-tabs` l’indicateur.  

### [<a name="cmd-windows"></a>CMD (Windows)](#tab/cmd-Windows/)  

<a id="auto-open-devtools-command-line"></a>  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

### [<a name="powershell-windows"></a>PowerShell (Windows)](#tab/powershell-Windows/)  

<a id="auto-open-devtools-command-line"></a>  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

### [<a name="bash-macos"></a>bash (macOS)](#tab/bash-macos/)  

<a id="auto-open-devtools-command-line"></a>  

```bash
/Applications/Microsoft\ Edge\ Beta.app/Contents/MacOS/Microsoft\ Edge\ Beta --auto-open-devtools-for-tabs
```  

### [<a name="bash-linux"></a>bash (Linux)](#tab/bash-linux/)  

<a id="auto-open-devtools-command-line"></a>  

```bash
microsoft-edge-dev --auto-open-devtools-for-tabs
```  

* * *  

## <a name="toggle-the-f12-keyboard-shortcut-on-or-off"></a>Toggle the F12 keyboard shortcut on or off  

Pour modifier le `F12` paramètre de raccourci clavier qui ouvre DevTools, effectuer les actions suivantes.  

1.  Naviguez vers`edge://settings/system` .  
1.  In `Developer Tools` , choose Open the **DevTools when the F12 key is pressed** to toggle the setting to off or on.  Désévérez le paramètre pour empêcher le raccourci `F12` clavier d’ouvrir DevTools.  
1.  Après avoir éteint le basculement, vérifiez qu’il n’ouvre plus `F12` DevTools.  
    
    > [!NOTE]
    > Après avoir éteint **Ouvrir DevTools**lorsque vous appuyez sur la touche F12, effectuez l’une des actions suivantes pour ouvrir devTools.  
    > 
    > *   Sélectionnez `Ctrl` + `Shift` + `I` .  
    > *   Ouvrez le menu contextuel \(clic droit\) > **Inspect**.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Présentation de la console | Documents Microsoft"  
[DevtoolsShortcutsIndex]: ../shortcuts/index.md "Microsoft Edge Raccourcis clavier DevTools | Documents Microsoft"  

<!--[ConsoleGetStarted]: /microsoft-edge/devtools-guide-chromium/console/get-started ""  -->  
<!--[GetStartedCSS]: /microsoft-edge/devtools-guide-chromium/css "CSS"  -->

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/open) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
