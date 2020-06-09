---
description: Découvrez comment déboguer des contrôles WebView2.
title: Débogage de WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 7e3ee11de443713a14684023fcd90de3cb1d265a
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697748"
---
# Débogage lors du développement avec des contrôles WebView2  

L’objectif du contrôle Microsoft Edge WebView2 combine les fonctionnalités de développement d’applications et les outils de développement d’applications Web et natives.  Cet article présente les différents outils à utiliser pour le développement de contrôles WebView2.  

## Outils Microsoft Edge Dev  

Utilisez les [outils de développement Microsoft Edge (chrome)](/microsoft-edge/devtools-guide-chromium) pour déboguer le contenu Web affiché dans les contrôles WebView2, de la même façon que si vous utilisiez Microsoft Edge.  Pour ouvrir le DevTools, positionnez le focus sur la fenêtre WebView, puis utilisez l’une des options suivantes.  
*   Sélectionnez `F12` .  
*   Sélectionnez `Ctrl` + `Shift` + `I` .  
*   Ouvrez le menu contextuel (cliquez avec le bouton droit sur \) > sélectionnez `Inspect` .  

:::image type="complex" source="../media/f12.png" alt-text="Outils Microsoft Edge Dev":::
   Outils Microsoft Edge Dev  
:::image-end:::  

> [!NOTE]
> Quand vous déboguez votre application dans Visual Studio avec le débogueur natif en pièce jointe, la sélection `F12` de l’application risque de déclencher le débogueur natif au lieu des outils de développement.  Utilisez `Ctrl` + `Shift` + `I` , ou utilisez le menu contextuel (cliquez avec le bouton droit sur \) pour éviter cette situation.  

## Visual Studio  

Utilisez le débogueur de script dans Visual Studio 2019 version 16,4 Preview 2 ou version ultérieure pour déboguer votre script dans Visual Studio.  Vérifiez que le composant de **Diagnostics JavaScript** du **développement de bureau avec charge de** travail en C++ est installé.  

:::image type="complex" source="../media/vs-js-diagnostics.jpg" alt-text="Diagnostics JavaScript Visual Studio":::
   Diagnostics JavaScript Visual Studio  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

Pour activer le débogage de script WebView2, ouvrez le menu contextuel (cliquez avec le bouton droit sur \) dans votre projet > sélectionnez **Propriétés**.  Dans **Propriétés de configuration**, sélectionnez **débogage**.  Dans la propriété **type de débogueur** , choisissez **JavaScript (WebView2)** dans la liste des options. 

:::image type="complex" source="../media/vs-script-debugger.jpg" alt-text="Débogueur JavaScript Visual Studio":::
   Débogueur JavaScript Visual Studio  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

## VisualStudioCode  

Vous pouvez utiliser du code Visual Studio pour déboguer des scripts qui s’exécutent dans des contrôles WebView2.  Pour plus d’informations, reportez-vous à la rubrique [applications WebView de Microsoft Edge (chrome)](https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications).  

<!--todo:  add See also heading  -->  

## Contacter l’équipe WebView de Microsoft Edge  

Aidez-vous à créer une expérience WebView2 plus riche en partageant vos commentaires.  Visitez le site de [Commentaires référentiel Samples](https://aka.ms/webviewfeedback) pour envoyer des demandes de fonctionnalité ou des rapports de bogues.  
