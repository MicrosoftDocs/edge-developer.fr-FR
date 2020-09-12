---
description: Héberger du contenu Web dans vos applications Win32, .NET et UWP avec le contrôle Microsoft Edge WebView2
title: Contrôle Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/10/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, contrôle de navigateur, HTML de bord, Windows Forms, WinForms, WPF, .NET, WinUI, Project REUNION
ms.openlocfilehash: d3294ce72237a323113ed9f7c8f31e37af43f5e6
ms.sourcegitcommit: efdc6369c48942bfa39e45c713300ed70f0e3655
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2020
ms.locfileid: "11013743"
---
# Introduction à Microsoft Edge WebView2 (Preview)  

Le contrôle Microsoft Edge WebView2 vous permet d’incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives.  Le contrôle WebView2 utilise [Microsoft Edge (chrome)][MicrosoftedgeinsiderMain] comme moteur de rendu pour afficher le contenu Web dans les applications natives.  Avec WebView2, vous pouvez incorporer du code Web dans différentes parties de votre application native, ou générer l’application native entière au sein d’un seul WebView.  Pour plus d’informations sur la création d’une application WebView2, voir [commencer.](#getting-started)  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="Présentation de WebView" lightbox="./media/WebView2/whatwebview.png":::
   Présentation de WebView  
:::image-end:::  

> [!NOTE]
> La version préliminaire de WebView2 est conçue pour le prototype initial et rassembler des commentaires pour vous aider à définir la forme de l’API.  Vous ne devez pas utiliser l’aperçu dans vos applications de production en raison de modifications éventuelles.  Pour plus d’informations, consultez [Webview2Releasenotes].  

## Approche hybride des applications  

Les développeurs doivent souvent choisir entre le bâtiment d’une application Web ou une application native.  La décision repose sur le compromis entre la portée et la puissance.  Les applications Web permettent d’offrir une large portée.  En tant que développeur Web, vous pouvez réutiliser la majeure partie de votre code, si ce n’est l’intégralité de votre code, sur toutes les différentes plateformes.  Toutefois, les applications natives utilisent les fonctionnalités de la plateforme Native entière.  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Web natif" lightbox="./media/WebView2/webnative.png":::
   Web natif  
:::image-end:::  

Les applications hybrides permettent aux développeurs de profiter au mieux de ces deux mondes.  Les développeurs d’applications hybrides profitent de l’omniprésence et de la puissance de la plateforme Web, ainsi que des fonctionnalités puissantes et complètes de la plateforme native.  

## Avantages de WebView2   

:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="Raisons de WebView" lightbox="./media/WebView2/webviewreasons.png":::
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

Pour générer et tester votre application à l’aide du contrôle WebView2, vous devez disposer de [Microsoft Edge (chrome)][MicrosoftedgeinsiderDownload] et du [SDK WebView2][NugetPackagesMicrosoftWebWebView2] .  Pour commencer, sélectionnez l’une des options suivantes.  

*   [Commencer à utiliser Win32 C/C++][Webview2GettingstartedWin32]  
*   [Mise en route de WPF][Webview2GettingstartedWpf]  
*   [Mise en route de WinForms][Webview2GettingstartedWinforms]  
*   [Commencer à utiliser WinUI3][Webview2GettingstartedWinui]  

Le référentiel d' [exemples WebView2][GithubMicrosoftedgeWebview2samples] contient des exemples qui illustrent l’ensemble des fonctionnalités du SDK WebView2 et des modèles d’utilisation de l’API.  À mesure que d’autres fonctionnalités sont ajoutées au SDK WebView2, les exemples d’applications seront mis à jour.  

## Plateformes prises en charge  

Un aperçu du développeur est disponible sur les environnements de programmation suivants.  

*   Win32 C/C++  
*   .NET Framework 4.6.2 ou version ultérieure  
*   .NET Core 3,0 ou version ultérieure  
*   [WinUI 3.0][UwpToolkitsWinui3]  

Vous pouvez exécuter des applications WebView2 sur les versions suivantes de Windows.  

*   Windows10  
*   Windows 8.1  
*   Windows8  
*   Windows7  
*   Windows Server2019  
*   Windows Server2016  
*   Windows Server2012  
*   Windows Server 2012R2  
*   Windows Server2008R2  

## Étapes suivantes  

Pour plus d’informations sur la création et le déploiement d’applications WebView2, voir la documentation conceptuelle et les guides de procédures.  

#### Concepts  

*   [Comprendre les versions de kit de développement logiciel WebView2][Webview2ConceptsVersioning]
*   [Distribution d’applications à l’aide de WebView2][Webview2ConceptsDistribution]  
*   [Recommandations en matière de développement d’applications WebView2 sécurisées][Webview2ConceptsSecurity]
*   [Gérer le dossier des données utilisateur dans les applications WebView2][Webview2ConceptsUserdatafolder]
 
#### Guides de procédure  

*   [Comment déboguer avec WebView2][Webview2HowtoDebug]  
*   [Automatisation et test de WebView2 avec le pilote Microsoft Edge][Webview2HowtoWebdriver]  

## Contacter l’équipe WebView de Microsoft Edge  

[!INCLUDE [contact WebView team note](./includes/contact-webview-team-note.md)]  

> [!NOTE]
> Au cours de l’aperçu, les données collectées permettent de créer un produit de meilleure qualité.  Pour désactiver la collecte de données WebView2, accédez à la collection de données du navigateur et désactivez-la `edge://settings/privacy` .  

<!-- links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[Webview2ConceptsSecurity]: ./concepts/security.md "Recommandations en matière de développement d’applications WebView2 sécurisées | Documents Microsoft"  
[Webview2ConceptsUserdatafolder]: ./concepts/userdatafolder.md "Gestion du dossier de données utilisateur | Documents Microsoft"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Comprendre les versions du SDK WebView2 | Documents Microsoft"  
[Webview2GettingstartedWin32]: ./gettingstarted/win32.md "Mise en route de WebView2 (developer preview) | Documents Microsoft"   
[Webview2GettingstartedWinforms]: ./gettingstarted/winforms.md "Commencer à utiliser WebView2 dans les applications Windows Forms (Preview) | Documents Microsoft"  
[Webview2GettingstartedWinui]: ./gettingstarted/winui.md "Commencer à utiliser WebView2 dans WinUI3 (Preview) | Documents Microsoft"  
[Webview2GettingstartedWpf]: ./gettingstarted/wpf.md "Commencer à utiliser WebView2 dans WPF (Preview) | Documents Microsoft"  
[Webview2HowtoDebug]: ./howto/debug.md "Comment déboguer avec WebView2 | Documents Microsoft"  
[Webview2HowtoWebdriver]: ./howto/webdriver.md "Automatisation et test de WebView2 avec le pilote Microsoft Edge | Documents Microsoft"  
[Webview2Releasenotes]: ./releasenotes.md "Notes de publication sur le Webview2Releasenotes du SDK WebView2 Documents Microsoft"  

[UwpToolkitsWinui3]: ./gettingstarted/winui.md "Windows UI Library 3 Preview 2 (2020 de juillet) | Documents Microsoft"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemples de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub" 

[MicrosoftedgeinsiderMain]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger Microsoft Edge Insider"  

[NugetPackagesMicrosoftWebWebView2]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Microsoft. Web. WebView2 | Galerie NuGet"  
