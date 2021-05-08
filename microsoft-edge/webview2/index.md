---
description: Héberger du contenu web dans vos applications Win32, .NET et UWP avec le contrôle Microsoft Edge WebView2
title: Contrôle Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, browser control, edge html, Windows Forms, WinForms, WPF, .NET, WinUI, Project Réunion
ms.openlocfilehash: 154c18a3cc9236a8abd286918d72e1a1968fea38
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535723"
---
# <a name="introduction-to-microsoft-edge-webview2"></a>Présentation de Microsoft Edge WebView2  

Le contrôle Microsoft Edge WebView2 vous permet d’incorporer des technologies web \(HTML, CSS et JavaScript\) dans vos applications natives.  Le contrôle WebView2 utilise [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] comme moteur de rendu pour afficher le contenu web dans les applications natives.  Avec WebView2, vous pouvez incorporer du code web dans différentes parties de votre application native.  Créez l’ensemble de l’application native au sein d’une instance WebView unique.  Pour plus d’informations sur la création d’une application WebView2, accédez [à Démarrer.](#get-started)  

:::image type="complex" source="./media/WebView2/what-webview.png" alt-text="Qu’est-ce que WebView ?" lightbox="./media/WebView2/what-webview.png":::
   Qu’est-ce que WebView ?  
:::image-end:::    

## <a name="hybrid-app-approach"></a>Approche de l’application hybride  

Les développeurs doivent souvent décider entre la création d’une application web ou d’une application native.  La décision porte sur le compromis entre la portée et la puissance.  Les applications web permettent une large portée.  En tant que développeur Web, vous pouvez réutiliser la plupart de votre code sur différentes plateformes.  Pour accéder à toutes les fonctionnalités d’une plateforme native, utilisez une application native.  

:::image type="complex" source="./media/WebView2/web-native.png" alt-text="Web natif" lightbox="./media/WebView2/web-native.png":::
   Web natif  
:::image-end:::    

Les applications hybrides permettent aux développeurs de profiter du meilleur des deux mondes.  Les développeurs d’applications hybrides bénéficient des avantages suivants.  

*   L’omniprésence et la force de la plateforme web.  
*   Puissance et fonctionnalités complètes de la plateforme native.  
    
## <a name="webview2-benefits"></a>Avantages de WebView2   

<!--  
:::image type="complex" source="./media/WebView2/webview-reasons.png" alt-text="WebView reasons" lightbox="./media/WebView2/webview-reasons.png":::
   WebView reasons  
:::image-end:::    
-->  

:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-web-ecosystem-skillset.msft.png":::  
      **Écosystème web \& compétences**  
      Utilisez l’ensemble de la plateforme web, des bibliothèques, des outils et des talents qui existent au sein de l’écosystème web.  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-rapid-innovation.msft.png":::  
      **Innovation rapide**  
      Le développement Web permet un déploiement et une itération plus rapides.  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-windows-7-8-10-support.msft.png":::  
      **Prise en charge de Windows 7, 8 et 10**  
      Prise en charge d’une expérience utilisateur cohérente dans Windows 7, Windows 8 et Windows 10.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-native-capabilities.msft.png":::  
      **Fonctionnalités natives**  
      Accéder à l’ensemble complet des API natives.  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-code-sharing.msft.png":::  
      **Partage de code**  
      L’ajout de code web à votre base de code permet une réutilisation accrue sur plusieurs plateformes.  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-microsoft-support.msft.png":::  
      **Support Microsoft**  
      Microsoft fournit une prise en charge et ajoute de nouvelles demandes de fonctionnalités lorsque WebView2 est publié à la disponibilité générale \(GA\).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-evergreen.msft.png":::  
      **Distribution persistante**  
      Reposez-vous sur une version à jour de Chromium avec des mises à jour de plateforme régulières et des correctifs de sécurité.  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-fixed.msft.png":::  
      **Résolu**  
      \(bientôt disponible\) Choisissez de mettre en package les bits Chromium dans votre application.  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-incremental-adoption.msft.png":::  
      **Adoption incrémentielle**  
      Ajoutez des composants web, pièce par élément, à votre application.  
   :::column-end:::
:::row-end:::  

## <a name="get-started"></a>Prise en main  

Pour créer et tester votre application à l’aide du contrôle WebView2, vous devez avoir <!--both [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] and  -->Le [SDK WebView2][NugetPackagesMicrosoftWebWebView2] est installé.  Sélectionnez l’une des options suivantes pour commencer.  

*   [Mise en place de Win32 C/C++][Webview2GetStartedWin32]  
*   [Mise en place de WPF][Webview2GetStartedWpf]  
*   [Mise en place de WinForms][Webview2GetStartedWinforms]  
*   [Mise en place de WinUI3][Webview2GetStartedWinui]  
    
Le [référentiel WebView2 Samples][GithubMicrosoftedgeWebview2samples] contient des exemples qui montrent toutes les fonctionnalités du SDK WebView2 et les modèles d’utilisation des API.  À mesure que d’autres fonctionnalités sont ajoutées au SDK WebView2, les exemples d’applications sont mis à jour.  

## <a name="supported-platforms"></a>Plateformes prises en charge  

Une version de disponibilité générale \(GA\) ou d’aperçu est disponible dans les environnements de programmation suivants.  

*   Win32 C/C++ \(GA\)  
*   .NET Framework 4.5 ou ultérieure  
*   .NET Core 3.1 ou ultérieur  
*   .NET 5  
*   [WinUI 3.0][UwpToolkitsWinui3] \(Preview\)  
    
Vous pouvez exécuter des applications WebView2 sur les versions suivantes de Windows.  

*   Windows 10  
*   Windows 8.1  
*   Windows 7 \*\*  
*   Windows Server2019  
*   Windows Server2016  
*   WindowsServer2012  
*   WindowsServer2012R2  
*   Windows Server 2008 R2 \*\*  
    
> [!IMPORTANT]
> La prise en charge de WebView2 pour Windows 7 et Windows Server 2008 R2 a le même cycle de prise en charge que Microsoft Edge.  Pour plus d’informations, accédez aux [systèmes d’exploitation pris en charge par Microsoft Edge.][DeployedgeMicrosoftEdgeSupportedOS]  

## <a name="next-steps"></a>Étapes suivantes  

Pour plus d’informations sur la façon de créer et de déployer des applications WebView2, examinez la documentation conceptuelle et les guides de pratiques.  

### <a name="concepts"></a>Concepts  

*   [Comprendre les versions du SDK WebView2][Webview2ConceptsVersioning]  
*   [Distribution d’applications à l’aide de WebView2][Webview2ConceptsDistribution]  
*   [Meilleures pratiques pour le développement d’applications WebView2 sécurisées][Webview2ConceptsSecurity]  
*   [Gérer le dossier de données utilisateur dans les applications WebView2][Webview2ConceptsUserDataFolder]  
 
### <a name="how-to-guides"></a>How-To guides  

*   [Comment déboguer avec WebView2][Webview2HowToDebug]  
*   [Automatisation et test de WebView2 avec le pilote Microsoft Edge][Webview2HowToWebdriver]  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Entrer en contact avec l’équipe Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](./includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[Webview2ConceptsSecurity]: ./concepts/security.md "Meilleures pratiques pour le développement d’applications WebView2 sécurisées | Documents Microsoft"  
[Webview2ConceptsUserDataFolder]: ./concepts/user-data-folder.md "Gérer le dossier de données utilisateur | Documents Microsoft"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Comprendre les versions du SDK WebView2 | Documents Microsoft"  
[Webview2GetStartedWin32]: ./get-started/win32.md "Commencer à prendre en | WebView2 Documents Microsoft"  
[Webview2GetStartedWinforms]: ./get-started/winforms.md "Démarrer avec WebView2 dans les applications Windows Forms (prévisualisation) | Documents Microsoft"  
[Webview2GetStartedWinui]: ./get-started/winui.md "Mise en place de WebView2 dans WinUI3 (prévisualisation) | Documents Microsoft"  
[Webview2GetStartedWpf]: ./get-started/wpf.md "Mise en place de WebView2 dans WPF (prévisualisation) | Documents Microsoft"  
[Webview2HowToDebug]: ./how-to/debug.md "Comment déboguer avec WebView2 | Documents Microsoft"  
[Webview2HowToWebdriver]: ./how-to/webdriver.md "Automatisation et test de WebView2 avec le pilote Microsoft Edge | Documents Microsoft"  
[Webview2ReleaseNotes]: ./release-notes.md "Notes de publication du SDK WebView2 | Documents Microsoft"  

[UwpToolkitsWinui3]: /uwp/toolkits/winui3/index "Windows UI Library 3 Preview 2 (juillet 2020) | Documents Microsoft"  

[DeployedgeMicrosoftEdgeSupportedOS]: /deployedge/microsoft-edge-supported-operating-systems "Systèmes d’exploitation pris en charge par Microsoft Edge | Documents Microsoft"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires WebView - MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftedgeinsiderMain]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger Microsoft Edge Insider"  

[NugetPackagesMicrosoftWebWebView2]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Microsoft.Web.WebView2 | Galerie NuGet"  
