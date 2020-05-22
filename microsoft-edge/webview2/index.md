---
description: Héberger le contenu Web de votre application Win32 avec le contrôle WebView 2 de Microsoft Edge
title: Contrôle Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge, Windows Forms, WinForms, WPF, .NET
ms.openlocfilehash: f17de3bcb7459375617f00aec0cd2897f0859c1d
ms.sourcegitcommit: c579181af051e2855b785263faa4001c672a929b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/22/2020
ms.locfileid: "10673852"
---
# Introduction à Microsoft Edge WebView2 (Preview)  

Le contrôle Microsoft Edge WebView2 vous permet d’incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives.  Le contrôle WebView2 utilise [Microsoft Edge (chrome)](https://www.microsoftedgeinsider.com) comme moteur de rendu pour afficher le contenu Web dans les applications natives.  Avec WebView2, vous pouvez incorporer du code Web dans différentes parties de votre application native, ou générer l’application native entière au sein d’un seul WebView.  Pour plus d’informations sur la création d’une application WebView2, voir [commencer.](./index.md#getting-started)  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="Présentation de WebView":::
   Présentation de WebView  
:::image-end:::  

> [!NOTE]
> La version préliminaire de WebView2 est conçue pour le prototype initial et rassembler des commentaires pour vous aider à établir la forme de l’API.  L’équipe WebView de Microsoft Edge ne recommande pas d’utiliser l’aperçu dans vos applications de production en raison de [modifications éventuelles](./releasenotes.md).  

## Approche hybride des applications  

Les développeurs doivent souvent choisir entre créer une application Web ou une application native.  La décision repose sur le compromis entre la portée et la puissance.  Les applications Web permettent d’offrir une large portée.  En tant que développeur Web, vous pouvez réutiliser la majeure partie de votre code, si ce n’est l’intégralité de votre code, sur toutes les différentes plateformes.  Toutefois, les applications natives utilisent les fonctionnalités de la plateforme Native entière.  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Web natif":::
   Web natif  
:::image-end:::  

Les applications hybrides permettent aux développeurs de profiter au mieux de ces deux mondes.  Les développeurs d’applications hybrides profitent de l’omniprésence et de la puissance de la plateforme Web, ainsi que des fonctionnalités puissantes et complètes de la plateforme native.  

## Avantages de WebView2   

:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="Raisons de WebView":::
   Raisons de WebView  
:::image-end:::  

:::row:::
   :::column span="1":::
      **& compétences du Web**  
      Utiliser l’intégralité de la plateforme Web, des bibliothèques, des outils et des talents qui existent au sein de l’écosystème Web.  
   :::column-end:::
   :::column span="1":::
      **Innovation rapide**  
      Le développement Web permet d’accélérer le déploiement et l’itération.  
   :::column-end:::
   :::column span="1":::
      **Prise en charge de Windows 7, 8 et 10**  
      La prise en charge d’une interface utilisateur homogène dans Windows 7, 8 et 10.  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **Fonctionnalités natives**  
      Accédez à l’ensemble complet d’API natives.  
   :::column-end:::
   :::column span="1":::
      **Partage de code**  
      L’ajout d’un code Web à votre code base permet une réutilisation accrue sur plusieurs plates-formes.  
   :::column-end:::
   :::column span="1":::
      **Support Microsoft**  
      Microsoft prend en charge l’assistance et ajoute de nouvelles demandes de fonctionnalité lorsque WebView2 est commercialisé en tant que GA.  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **Distribution persistant**  
      S’appuyer sur une version de chrome à jour avec les mises à jour de plateforme et les correctifs de sécurité normaux.  
   :::column-end:::
   :::column span="1":::
      **Corrigé** \ (bientôt disponible)  
      Choisissez de conditionner les bits de chrome dans votre application.  
   :::column-end:::
   :::column span="1":::
      **Adoption incrémentielle**  
      Ajoutez des composants WebPart à votre application.  
   :::column-end:::
:::row-end:::  

## Prise en main  

Pour générer et tester votre application à l’aide du contrôle WebView2, vous devez disposer de [Microsoft Edge (chrome)](https://www.microsoftedgeinsider.com/download) et du [SDK WebView2](https://aka.ms/webviewnuget) .  Pour commencer, sélectionnez l’une des options suivantes.  

*   [Commencer à utiliser Win32 C/C++](./gettingstarted/win32.md)  
*   [Mise en route de WPF](./gettingstarted/wpf.md)  
*   [Mise en route de WinForms](./gettingstarted/winforms.md)  

Le référentiel d' [exemples WebView2](https://github.com/MicrosoftEdge/WebView2Samples) contient des exemples qui illustrent l’ensemble des fonctionnalités du SDK WebView2 et des modèles d’utilisation de l’API. À mesure que d’autres fonctionnalités sont ajoutées au SDK WebView2, les exemples d’applications seront mis à jour.   

## Plates-formes prises en charge  

Un aperçu du développeur est disponible sur les environnements de programmation suivants.  

*   Win32 C/C++  
*   .NET Framework 4.6.2 ou version ultérieure  
*   .NET Core 3,0 ou version ultérieure  
*   [WinUI 3,0](/uwp/toolkits/winui3/)  

Vous pouvez exécuter des applications WebView2 sur les versions suivantes de Windows.  

*   Windows 10  
*   Windows 8.1  
*   Windows8  
*   Windows7  
*   Windows Server2016  
*   Windows Server2012  
*   Windows Server 2012R2  
*   Windows Server2008R2  

## Étapes suivantes  

Pour obtenir des informations plus détaillées sur la création et le déploiement d’applications WebView2, consultez la documentation conceptuelle et les guides de procédures.  

#### Concepts  

*   [Kit de développement logiciel (SDK) WebView2 et contrôle de version Microsoft Edge](./concepts/versioning.md)
*   [Distribution d’applications WebView2](./concepts/distribution.md)  
 
#### Guides de procédure  

*   [Débogage de WebView2 avec DevTools et le débogage de script Visual Studio](./howto/debug.md)  
*   [Automatisation et débogage de WebView2 avec Microsoft EdgeDriver](./howto/webdriver.md)  

<!--todo: add how-tos when available  -->  

## Contacter l’équipe WebView2  

Aidez-vous à créer une expérience WebView2 plus riche en partageant vos commentaires.  Rendez-vous sur le site Web de [Commentaires référentiel Samples](https://aka.ms/webviewfeedback) pour envoyer des demandes de fonctionnalité ou des rapports de bogues.  C’est également le bon endroit où rechercher des problèmes connus.  

> [!NOTE]
> Dans le cadre de l’aperçu du développeur, l’équipe WebView Microsoft Edge recueille également des données pour vous aider à créer un meilleur affichage du WebView.  Les utilisateurs peuvent désactiver la collecte des données de WebView en naviguant `edge://settings/privacy` dans le navigateur Microsoft Edge et en désactivant la collecte des données du navigateur.  
