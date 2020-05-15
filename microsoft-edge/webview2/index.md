---
description: Héberger le contenu Web de votre application Win32 avec le contrôle WebView 2 de Microsoft Edge
title: Applications WebView 2 de Microsoft Edge 2 pour les applications Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: b1ec0c43b57fb107490ddb34b330bb6ec378ac41
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653359"
---
# Microsoft Edge WebView2 (version préliminaire du développeur)

Le contrôle Microsoft Edge WebView2 vous permet d’héberger le contenu Web de votre application à l’aide de [Microsoft Edge (chrome)](https://www.microsoftedgeinsider.com/) comme moteur de rendu.

Le contrôle WebView2 est actuellement dans la version préliminaire du développeur, au cours de laquelle vous pouvez prototyper vos solutions et partager vos commentaires nous permettant de façonner l’API stable future. Dans certains cas, il est probable que nous ayons modifié l’API lors de la prévisualisation, et dans ce cas, vous devez mettre à jour le kit de développement logiciel (SDK) WebView2 et le navigateur Microsoft Edge (chrome). Les modifications importantes seront mentionnées dans les [notes de publication](./releasenotes.md) du SDK. Cela se verrouille en tant qu’approche WebView2 et stable.

## Plates-formes prises en charge

Un aperçu des développeurs est disponible pour Win32 C/C++ et Windows Forms et WPF sur .NET Framework 4.6.2 ou version ultérieure et .NET Core 3,0 ou version ultérieure sur Windows 10, Windows 8,1, Windows 8, Windows 7, Windows Server 2016, Windows Server 2012/2012R2 et Windows Server 2008 R2. Une version alpha pour WinUI 3,0 est disponible [ici](https://docs.microsoft.com/uwp/toolkits/winui3/).

## Prise en main

Pour générer et tester votre application à l’aide du contrôle WebView2, vous devez disposer de [Microsoft Edge (chrome)](https://www.microsoftedgeinsider.com/download/) et du [SDK WebView2](https://aka.ms/webviewnuget) . Sélectionnez l’une des options ci-dessous pour commencer.

* [Commencer à utiliser Win32 C/C++](./gettingstarted/win32.md)
* [Mise en route de WPF](./gettingstarted/wpf.md)
* [Mise en route de Windows Forms](./gettingstarted/winforms.md)

N’hésitez pas à nous faire part de vos commentaires [WebView2](https://aka.ms/webviewfeedback) référentiel Samples.

## Exemples de WebView2

Le référentiel d' [exemples WebView2](https://github.com/MicrosoftEdge/WebView2Samples) contient des exemples qui décrivent toutes les fonctionnalités du SDK WebView2 et leurs modèles d’utilisation de l’API. À mesure que nous ajoutons des fonctionnalités au kit de développement logiciel (SDK) WebView2, nous mettons à jour régulièrement nos exemples d’applications.

## Distribution de l’application

Le contrôle WebView2 utilise le navigateur Microsoft Edge (chrome). Lors de la distribution de votre application, il est important de veiller à ce que le navigateur Edge soit installé sur tous les ordinateurs des utilisateurs dans lesquels votre application sera exécutée. Vous devez également savoir quelle version et quel canal est installé (par exemple, stable, bêta, dev ou Canaries). Le contrôleur WebView2 utilisera la version la plus stable du navigateur lorsqu’il est installé sur un ordinateur.

### Futures modifications planifiées

Nous sommes conscients du fait que le navigateur Edge n’est peut-être pas disponible sur tous les ordinateurs utilisateur que votre application est conçue pour s’exécuter, ou ce contrôle du processus d’installation du navigateur Edge peut s’avérer difficile. Pour vous assurer que votre application s’exécutera sur tous les ordinateurs, indépendamment de l’état d’installation du navigateur Microsoft Edge du client, nous allons libérer Microsoft Edge WebView2 Runtime. Nous allons mettre à jour WebView2 pour rechercher la version stable du runtime avant de rechercher des versions préliminaires du navigateur installé.

Nous sommes conscients également du bon fonctionnement de certains développeurs d’applications dans les environnements restreints, et de la prise en charge de deux options de distribution, de persistants et de la version corrigée.

L’option persistant est le modèle de distribution recommandé pour la plupart des développeurs. Dans ce mode, les mises à jour de WebView2 Runtime seront entièrement gérées par Microsoft pour vous tenir au courant, sans aucun effort supplémentaire de votre application. Avec ce modèle de mise à jour automatique, vous pouvez être sûr que votre application tire parti des fonctionnalités et des mises à jour de sécurité les plus récentes pour le contenu Web hébergé.

En ce qui concerne les environnements restreints, nous mettrons également en charge un modèle de distribution de version fixe. Dans ce modèle, votre application sélectionne et empaquetait une version WebView2 spécifique. Les mises à jour apportées à la version du WebView seront responsables de l’application et seront indépendantes de tout mécanisme Microsoft Update géré. Vous devez choisir ce modèle s’il est essentiel de pouvoir contrôler en tout lieu la version du navigateur et les durées de mise à jour dont votre application tire parti.

## Microsoft Edge WebView2 Runtime

Microsoft Edge WebView2 Runtime est un ensemble de fichiers binaires de navigateur optimisés pour une utilisation par des applications WebView2. Ce mode fonctionne autonome ou côte à côte à l’aide d’une installation de navigateur côté client. Une installation unique du runtime prend en charge un nombre quelconque d’applications WebView2. L’installation de la version d’exécution ne s’affiche pas sous la forme d’une installation de navigateur pour l’utilisateur final, par exemple, aucun raccourci sur le bureau, entrée du menu Démarrer ou enregistrement du protocole.

Une application utilisant WebView2 doit vérifier que l’installation de Microsoft Edge WebView2 Runtime s’est produite. Au moment de l’installation de l’application, vous devez vérifier l’état d’installation actuel, qui peut être déterminé à l’aide de [GetAvailableCoreWebView2BrowserVersionString](./reference/win32/0-9-488/webview2-idl.md#getavailablecorewebview2browserversionstring). Si le runtime WebView2 n’est pas disponible, vous devez chaîner le programme d’installation de Microsoft Edge WebView2 Runtime dans votre flux d’installation.

## Kit de développement logiciel (SDK) Microsoft Edge WebView2

Pour utiliser WebView2 au sein de votre application, vous devez installer et faire référence au [Kit de développement logiciel (SDK) WebView2](https://aka.ms/webviewnuget) dans votre application. Nos publications NuGet contiendront une version préliminaire. La version commerciale contient les API publiques que nous envisageons actuellement de publier pour une disponibilité générale.

La version préliminaire contient des [API expérimentales](./reference/win32/0-9-488-reference-webview2.md#experimental)supplémentaires. Il s’agit d’API et de fonctionnalités que nous évaluons et pour lesquelles nous aimerions les [Commentaires](https://aka.ms/webviewfeedback) avant de les promouvoir dans la version finale.

## Développement pour les versions à venir

Pour le développement, vous souhaiterez peut-être cibler la version bêta, le dev ou le Canaries pour vous assurer que votre application fonctionne avec les versions à venir ou pour tirer parti des fonctionnalités à venir. Tous les canaux préconfigurés sont fournis par le navigateur Microsoft Edge du client installé. Pour cibler l’un de ces canaux, assurez-vous que le navigateur Edge installé sur votre ordinateur de développement est le canal que vous voulez. Les développeurs peuvent utiliser une clé de registre ou une variable d’environnement pour modifier WebView2 à partir de la version la plus stable qui est la plus stable trouvée. Pour plus d’informations, voir [CreateCoreWebView2EnvironmentWithOptions](./reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithoptions).

## Débogage de WebView2

### DevTools

Vous pouvez utiliser les [outils de développement Microsoft Edge (chrome)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium) pour déboguer le contenu Web affiché dans WebView, comme vous le feriez dans le navigateur. Lorsque vous avez la possibilité de mettre le focus sur la fenêtre WebView, appuyez `F12` ou appuyez sur `Ctrl`  +  `Shift`  +  `I` ou cliquez avec le bouton droit sur le bouton droit `Inspect` pour ouvrir les outils de développement.

:::image type="complex" source="./media/f12.png" alt-text="F12":::
   F12
:::image-end:::  

<!--![F12](./media/f12.png)  -->  

**Remarque lors du débogage d’une application dans Visual Studio avec le débogueur natif en pièce jointe, `F12` il est possible que le débogueur natif se déclenche au lieu des outils de développement. Utiliser `Ctrl`  +  `Shift`  +  `I` , ou cliquer avec le bouton droit + `Inspect` pour éviter les conflits de raccourcis clavier potentiels.**

### Visual Studio

Vous pouvez utiliser le débogueur de script dans Visual Studio 2019 (version minimum 16,4 Preview 2) pour déboguer votre script dans WebView2 directement à partir de l’environnement de développement intégré (IDE). Assurez-vous que le composant de **Diagnostics JavaScript** du **développement de bureau avec charge de** travail en C++ est installé.

:::image type="complex" source="./media/vs-js-diagnostics.jpg" alt-text="Diagnostics JavaScript Visual Studio":::
   Diagnostics JavaScript Visual Studio
:::image-end:::  

<!--![vs-js-diagnostics](./media/vs-js-diagnostics.jpg)  -->  

Cliquez avec le bouton droit sur votre projet, puis sélectionnez **Propriétés**. Sous **Propriétés**  >  **Debugging**  >  de configuration du**type de débogueur**, sélectionnez l’option **JavaScript (WebView2)** pour activer le débogage de script WebView2. Vous pouvez en savoir plus sur le suivi.

:::image type="complex" source="./media/vs-script-debugger.jpg" alt-text="Débogueur de script Visual Studio":::
   Débogueur de script Visual Studio
:::image-end:::  

<!--![vs-script-debugger](./media/vs-script-debugger.jpg)  -->  

### VisualStudioCode

Vous pouvez également utiliser du code Visual Studio pour déboguer votre script dans le WebView2 directement à partir de l’IDE. Pour en savoir plus, cliquez [ici](https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications).

## Contacter l’équipe WebView2  

Aidez-nous à créer une expérience WebView2 plus riche en partageant vos commentaires! Consultez notre page de [Commentaires référentiel Samples](https://aka.ms/webviewfeedback) pour envoyer des demandes de fonctionnalité ou des rapports de bogues.

C’est également le bon endroit pour rechercher des problèmes connus.
Pendant la version préliminaire du développeur, nous recueillerons également des données de télémétrie pour nous aider à créer un meilleur affichage du WebView. Les utilisateurs peuvent désactiver la collecte des données WebView en accédant à edge://settings/privacy dans le navigateur et en désactivant la collecte des données du navigateur.
