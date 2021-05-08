---
description: Héberger du contenu web dans vos applications Win32, .NET et UWP avec le Microsoft Edge WebView2
title: Microsoft Edge Contrôle WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, browser control, edge html, Windows Forms, WinForms, WPF, .NET, WinUI, Project Réunion
ms.openlocfilehash: 9c1aa073294fc649223da19c44850dc4335f6c00
ms.sourcegitcommit: 7f7922dbb6af87ecac1378d18359125770c5b8e5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536833"
---
# <a name="introduction-to-microsoft-edge-webview2"></a>Présentation de Microsoft Edge WebView2  

Le Microsoft Edge WebView2 vous permet d’incorporer des technologies web \(HTML, CSS et JavaScript\) dans vos applications natives.  Le contrôle WebView2 utilise [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] comme moteur de rendu pour afficher le contenu web dans les applications natives.  Avec WebView2, vous pouvez incorporer du code web dans différentes parties de votre application native.  Créez l’ensemble de l’application native au sein d’une instance WebView unique.  Pour plus d’informations sur la création d’une application WebView2, accédez [à Prise en main](#get-started).  

:::image type="complex" source="./media/WebView2/what-webview.png" alt-text="Qu’est-ce que WebView ?" lightbox="./media/WebView2/what-webview.png":::
   Qu’est-ce que WebView ?  
:::image-end:::    

## <a name="hybrid-app-approach"></a>Approche de l’application hybride  

Les développeurs doivent souvent décider entre la création d’une application web ou d’une application native.  La décision s’en va sur le compromis entre la portée et la puissance.  Les applications web permettent une large portée.  En tant que développeur Web, vous pouvez réutiliser la plupart de votre code sur différentes plateformes.  Pour accéder à toutes les fonctionnalités d’une plateforme native, utilisez une application native.  

:::image type="complex" source="./media/WebView2/web-native.png" alt-text="Web natif" lightbox="./media/WebView2/web-native.png":::
   Web natif  
:::image-end:::    

Les applications hybrides permettent aux développeurs de profiter du meilleur des deux mondes.  Les développeurs d’applications hybrides bénéficient des avantages suivants.  

*   L’omniprésence et la force de la plateforme web.  
*   Puissance et fonctionnalités complètes de la plateforme native.  
    
## <a name="webview2-benefits"></a>Avantages de WebView2   

:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-web-ecosystem-skillset-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-rapid-innovation-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-windows-7-8-10-support-small.msft.png":::  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ### <a name="web-ecosystem--skillset"></a>Écosystème web & compétences  
   :::column-end:::
   :::column span="1":::
      ### <a name="rapid-innovation"></a>Innovation rapide  
   :::column-end:::
   :::column span="1":::
      ### <a name="windows-7-8-and-10-support"></a>Windows 7, 8 et 10  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Utilisez l’ensemble de la plateforme web, des bibliothèques, des outils et des talents qui existent au sein de l’écosystème web.  
   :::column-end:::
   :::column span="1":::
      Le développement Web permet un déploiement et une itération plus rapides.  
   :::column-end:::
   :::column span="1":::
      Prise en charge d’une expérience utilisateur cohérente entre Windows 7, Windows 8 et Windows 10.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-native-capabilities-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-code-sharing-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-microsoft-support-small.msft.png":::  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ### <a name="native-capabilities"></a>Fonctionnalités natives  
   :::column-end:::
   :::column span="1":::
      ### <a name="code-sharing"></a>Partage de code  
   :::column-end:::
   :::column span="1":::
      ### <a name="microsoft-support"></a>Support Microsoft  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Accéder à l’ensemble complet des API natives.  
   :::column-end:::
   :::column span="1":::
      L’ajout de code web à votre base de code permet une réutilisation accrue sur plusieurs plateformes.  
   :::column-end:::
   :::column span="1":::
      Microsoft fournit une prise en charge et ajoute de nouvelles demandes de fonctionnalités lorsque WebView2 est publié à la disponibilité générale \(GA\).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-evergreen-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-fixed-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-incremental-adoption-small.msft.png":::  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ### <a name="evergreen-distribution"></a>Distribution persistante  
   :::column-end:::
   :::column span="1":::
      ### <a name="fixed"></a>Résolu  
   :::column-end:::
   :::column span="1":::
      ### <a name="incremental-adoption"></a>Adoption incrémentielle  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Reposez-vous sur une version à jour de Chromium avec des mises à jour de plateforme régulières et des correctifs de sécurité.  
   :::column-end:::
   :::column span="1":::
      \(bientôt disponible\) Choisissez d’Chromium bits dans votre application.  
   :::column-end:::
   :::column span="1":::
      Ajoutez des composants web, pièce par élément, à votre application.  
   :::column-end:::
:::row-end:::  

## <a name="get-started"></a>Prise en main  

Pour créer et tester votre application à l’aide du contrôle WebView2, vous devez avoir <!--both [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] and  -->Le [SDK WebView2][NugetPackagesMicrosoftWebWebView2] est installé.  Sélectionnez l’une des options suivantes pour commencer.  

*   [Prise en main avec Win32 C/C++][Webview2GetStartedWin32]  
*   [Prise en main avec WPF][Webview2GetStartedWpf]  
*   [Prise en main avec WinForms][Webview2GetStartedWinforms]  
*   [Prise en main avec WinUI3][Webview2GetStartedWinui]  
    
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
> La prise en charge de \*\* WebView2 pour Windows 7 et Windows Server 2008 R2 possède le même cycle de prise en charge que Microsoft Edge.  Pour plus d’informations, [accédez à Microsoft Edge systèmes d’exploitation pris en charge.][DeployedgeMicrosoftEdgeSupportedOS]  

## <a name="next-steps"></a>Étapes suivantes  

Pour plus d’informations sur la façon de créer et de déployer des applications WebView2, examinez la documentation conceptuelle et les guides de pratiques.  

### <a name="concepts"></a>Concepts  

*   [Comprendre les versions du SDK WebView2][Webview2ConceptsVersioning]  
*   [Distribution d’applications à l’aide de WebView2][Webview2ConceptsDistribution]  
*   [Meilleures pratiques pour le développement d’applications WebView2 sécurisées][Webview2ConceptsSecurity]  
*   [Gérer le dossier de données utilisateur dans les applications WebView2][Webview2ConceptsUserDataFolder]  
 
### <a name="how-to-guides"></a>How-To guides  

*   [Comment déboguer avec WebView2][Webview2HowToDebug]  
*   [Automatisation et test de WebView2 avec Microsoft Edge pilote][Webview2HowToWebdriver]  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Entrer en contact avec l’équipe web Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](./includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[Webview2ConceptsSecurity]: ./concepts/security.md "Meilleures pratiques pour le développement d’applications WebView2 sécurisées | Documents Microsoft"  
[Webview2ConceptsUserDataFolder]: ./concepts/user-data-folder.md "Gérer le dossier de données utilisateur | Documents Microsoft"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Comprendre les versions du SDK WebView2 | Documents Microsoft"  
[Webview2GetStartedWin32]: ./get-started/win32.md "Commencer à prendre en | WebView2 Documents Microsoft"  
[Webview2GetStartedWinforms]: ./get-started/winforms.md "Mise en place de WebView2 dans Windows Forms (prévisualisation) | Documents Microsoft"  
[Webview2GetStartedWinui]: ./get-started/winui.md "Mise en place de WebView2 dans WinUI3 (prévisualisation) | Documents Microsoft"  
[Webview2GetStartedWpf]: ./get-started/wpf.md "Mise en place de WebView2 dans WPF (prévisualisation) | Documents Microsoft"  
[Webview2HowToDebug]: ./how-to/debug.md "Comment déboguer avec WebView2 | Documents Microsoft"  
[Webview2HowToWebdriver]: ./how-to/webdriver.md "Automatisation et test de WebView2 avec Microsoft Edge driver | Documents Microsoft"  
[Webview2ReleaseNotes]: ./release-notes.md "Notes de publication du SDK WebView2 | Documents Microsoft"  

[UwpToolkitsWinui3]: /uwp/toolkits/winui3/index "Windows UI Library 3 Preview 2 (juillet 2020) | Documents Microsoft"  

[DeployedgeMicrosoftEdgeSupportedOS]: /deployedge/microsoft-edge-supported-operating-systems "Microsoft Edge systèmes d’exploitation pris en charge | Documents Microsoft"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires WebView - MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftedgeinsiderMain]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger Microsoft Edge Insider"  

[NugetPackagesMicrosoftWebWebView2]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Microsoft.Web.WebView2 | NuGet Galerie"  
