---
description: Options de distribution lors de la publication d’une application à l’Microsoft Edge WebView2
title: Distribution de Microsoft Edge applications WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, applications wpf, wpf, edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, edge html
ms.openlocfilehash: 97ede968e066c572bb1b22e10ed7e758e38e3ca4
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535698"
---
# <a name="distribution-of-apps-using-webview2"></a>Distribution d’applications à l’aide de WebView2  

Lors de la distribution de votre application WebView2, assurez-vous que la plateforme web de backing, [WebView2 Runtime,][Webview2Installer]est présente avant le démarrage de l’application.  Cet article décrit comment vous installez le runtime WebView2 et utilisez les deux modes de [](#evergreen-distribution-mode) distribution pour votre application WebView2 : persistant et [fixe.](#fixed-version-distribution-mode)  

## <a name="evergreen-distribution-mode"></a>Mode de distribution persistant  

> [!NOTE]
> Le mode de distribution persistant est recommandé pour la plupart des développeurs.  

Le mode de distribution persistant permet à votre application de tirer parti des dernières fonctionnalités et mises à jour de sécurité.  Il présente les caractéristiques suivantes.  

*   La plateforme web sous-jacente \(WebView2 Runtime\) se met à jour automatiquement sans effort supplémentaire de votre part.  
*   Toutes les applications qui utilisent le mode de distribution persistant utilisent une copie partagée du runtime WebView2 persistant, ce qui permet d’économiser de l’espace disque.  
    
### <a name="understanding-the-webview2-runtime"></a>Comprendre le runtime WebView2  

WebView2 Runtime est un runtime redistribuable et sert de plateforme web de backing pour les applications WebView2.  Le concept est similaire à Visual C++ ou au runtime .NET pour les applications C++/.NET.  Le runtime contient les Microsoft Edge binaires \(Chromium\) modifiés qui sont mis à jour et testés pour les applications.  Le runtime ne s’affiche pas en tant que navigateur visible par l’utilisateur lors de l’installation.  Par exemple, un utilisateur n’a pas de raccourci de bureau de navigateur ou d’entrée de menu Démarrer.  

Pendant le développement et le test, vous pouvez utiliser l’une ou l’autre des plateformes web de backing.  

*   The WebView2 Runtime  
*   Tout canal de navigateur Insider \(non stable\) Microsoft Edge \(Chromium\)  
    
Dans les environnements de production, vous devez vous assurer que le runtime est présent sur les appareils des utilisateurs avant le démarrage de l’application.  Le Microsoft Edge stable n’est pas disponible pour l’utilisation de WebView2.  La décision empêche les applications de dépendre du navigateur en production.

Ne prenez pas de dépendance sur le navigateur car :  

*   Microsoft Edge \(Chromium\) n’est pas garantie d’être présent sur tous les appareils utilisateur.  Par exemple, les appareils déconnectés de Windows Update ou non gérés directement par Microsoft \(une grande partie du marché Enterprise et EDU\) peuvent ne pas avoir le navigateur.  Vous permettre de distribuer WebView2 Runtime évite de prendre une dépendance sur le navigateur comme condition préalable pour les applications.  
*   Les navigateurs et les applications ont des cas d’utilisation différents, de sorte que la prise d’une dépendance sur un navigateur peut avoir des effets secondaires inattendus sur vos applications.  Par exemple, les administrateurs informatiques peuvent contrôler la version du navigateur pour la compatibilité du site web interne.  WebView2 Runtime permet aux applications de rester persistantes pendant que les mises à jour du navigateur sont activement gérées.  
*   Contrairement au navigateur, le runtime est développé et testé pour les scénarios d’application et, dans certains cas, il peut inclure des correctifs de bogues qui ne sont pas encore disponibles dans le navigateur.  
    
À l’avenir, le runtime WebView2 persistant prévoit d’être publié avec les futures Windows.  Déployez le Runtime avec votre application de production jusqu’à ce qu’il soit plus universellement disponible.  

### <a name="deploying-the-evergreen-webview2-runtime"></a>Déploiement du runtime WebView2 persistant  

Une seule installation de l’application WebView2 Runtime persistante est nécessaire pour toutes les applications Persistantes sur l’appareil.  Un certain nombre d’outils sont disponibles sur la [page de téléchargement WebView2 Runtime.][Webview2Installer]  Les outils suivants vous aident à déployer le runtime persistant.  

*   WebView2 Runtime Bootstrapper est un petit programme d’installation \(environ 2 Mo\).  WebView2 Runtime Bootstrapper télécharge et installe le runtime persistant à partir des serveurs Microsoft qui correspond à l’architecture de l’appareil de l’utilisateur.  
*   Utilisez un lien pour télécharger par programme le programme d’a bootstrapper.  
*   Le programme d’installation autonome WebView2 Runtime est un programme d’installation complet qui installe le runtime WebView2 persistant dans les environnements hors connexion.  
    
Actuellement, le programme d’a bootstrapper et le programme d’installation autonome ne peuvent prendre en charge que les installation par ordinateur, ce qui nécessite une élévation.  Si un programme d’installation est exécuté sans élévation, l’utilisateur est invité à élever les autorisations.  

Utilisez les flux de travail suivants pour vous assurer que le runtime est déjà installé avant le lancement de votre application.  Vous pouvez ajuster votre flux de travail en fonction de votre scénario.  L’exemple de code est disponible dans le [repo Exemples.][GitHubMicrosoftedgeWebView2samplesWebview2Deployment]  

#### <a name="online-only-deployment"></a>Déploiement en ligne uniquement  

Si vous avez un scénario de déploiement en ligne uniquement dans lequel les utilisateurs sont supposés avoir accès à Internet, complétez les étapes suivantes.  

1.  Pendant la configuration de votre application, assurez-vous que le runtime est déjà installé.  Pour vérifier, effectuer l’une des actions suivantes.  
    *   Inspectez si la `pv (REG_SZ)` clé de regkey existe et n’est `null` pas ou est vide.  Recherchez  `pv (REG_SZ)` à l’emplacement suivant.  
        
        Sur les Windows 64 bits  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
        Sur les Windows 32 bits  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
    *   Exécutez [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring] et assurez-vous que `versionInfo` le . `NULL`  
1.  Si le runtime n’est pas installé, utilisez le lien pour télécharger par programme le programme d’a bootstrapper.  
1.  Invoke the bootstrapper from an elevated process or command prompt with `MicrosoftEdgeWebview2Setup.exe /silent /install` for silent install.  
    
Le flux de travail précédent présente les avantages suivants.  

*   Installez le runtime uniquement en cas de besoin ou lorsque vous n’êtes pas obligé de packager des programme d’installation.  
*   Le bootstrapper détecte automatiquement l’architecture de l’appareil et installe le runtime correspondant.  
*   Installez le runtime en mode silencieux.  
    
Vous pouvez également choisir de mettre en package le programme d’a bootstrapper avec votre application au lieu de la télécharger par programme à la demande.  

#### <a name="offline-deployment"></a>Déploiement hors connexion  

Si vous avez un scénario de déploiement hors connexion dans lequel le déploiement d’application doit fonctionner entièrement hors connexion, complétez les étapes suivantes.  

1.  Téléchargez [le programme d’installation autonome.][Webview2Installer]  
1.  Incluez le programme d’installation dans le programme d’installation ou le programme d’installation de votre application.  
1.  Pendant la configuration de votre application, assurez-vous que le runtime est déjà installé.  Pour vérifier, effectuer l’une des actions suivantes.  
    *   Inspectez si la `pv (REG_SZ)` clé de regkey existe et n’est `null` pas ou est vide.  Recherchez  `pv (REG_SZ)` à l’emplacement suivant.  
        
        Sur les Windows 64 bits  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
        Sur les Windows 32 bits  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
    *   Exécutez [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring] et assurez-vous que `versionInfo` le . `NULL`  
1.  Si le runtime n’est pas installé, exécutez le programme d’installation autonome.  Si vous souhaitez exécuter une installation en mode silencieux, exécutez le programme d’installation à partir d’un processus élevé ou copiez et exécutez la commande suivante.  
    
    ```shell
    MicrosoftEdgeWebView2RuntimeInstaller{X64/X86/ARM64}.exe /silent /install
    ```  
    
### <a name="stay-compatible-in-evergreen-mode"></a>Restez compatible en mode persistant  

Le Web évolue constamment.  Le runtime WebView2 persistant est tenu à jour pour vous fournir les dernières fonctionnalités et correctifs de sécurité.  Pour vous assurer que votre application reste compatible avec le web, vous devez configurer l’infrastructure de test.  

Les canaux d’Microsoft Edge non stables \(Beta/Dev/Canary\) offrent un aperçu de ce qui est à venir dans WebView2 Runtime.  Tout comme le développement de sites web Microsoft Edge, vous devez tester régulièrement votre application WebView2.  Testez votre application WebView2 par rapport à l’un [][GithubMicrosoftedgeWebviewfeedback] des canaux non stables et mettez à jour votre application ou signalez des problèmes si des problèmes surviennent. En règle générale, Dev et Beta sont les canaux recommandés.  Pour vous aider à déterminer quel canal est le bon, accédez à [Vue d’ensemble Microsoft Edge canaux.][DeployEdgeMicrosoftEdgeChannels]  Vous pouvez télécharger le canal Microsoft Edge non [stable][DownloadNonstableEdge] sur votre environnement de test et utiliser ou des variables d’environnement pour indiquer les préférences de canal pour `regkey` votre application de test.  Pour plus d’informations, [accédez à CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions].  Vous pouvez également utiliser [WebDriver pour][HowToWebdriver] automatiser les tests WebView2.

## <a name="fixed-version-distribution-mode"></a>Mode de distribution de version fixe   

Pour les environnements contraintes avec des exigences de compatibilité strictes, envisagez d’utiliser le mode de distribution de version fixe.  Choisissez et packagez une version spécifique du runtime WebView2 à l’aide du mode de distribution de version fixe.  Vous pouvez spécifier le minutage des mises à jour d’runtime pour votre application.  Le mode de distribution de version fixe ne reçoit aucune mise à jour automatique. Prévoyez de mettre à jour votre application et le runtime.  

> [!NOTE] 
> Le mode de distribution de version fixe était précédemment appelé « apportez-vous-vous-même ».  

Pour utiliser le mode version fixe, effectuer les actions suivantes

1.  [Téléchargez][Webview2Installer] le package version fixe. 
1.  Décompressez le package à l’aide d’une ligne de commande ou d’outils `expand {path to the package} -F:* {path to the destination folder}` tels que WinRAR. Évitez de décompresser dans l’Explorateur de fichiers, car il est possible qu’il ne génère pas la structure de dossiers correcte.  
1.  Incluez les binaires de version fixe décompressés dans votre projet.  
1.  Indiquez le chemin d’accès aux binaires de version fixe lors de la création de l’environnement WebView2.  
    *   Pour Win32 C/C++, vous pouvez créer l’environnement à l’aide de la fonction [CreateCoreWebView2EnvironmentWithOptions.][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions]  Utilisez le `browserExecutableFolder` paramètre pour indiquer le chemin d’accès au dossier contenant `msedgewebview2.exe` .  
    *   Pour .NET, vous pouvez faire l’une des options suivantes pour spécifier l’environnement.  
        
        > [!NOTE]
        > Vous devez spécifier l’environnement avant que la propriété WebView2 `Source` prenne effet.  
        
        *   Définissez `CreationProperties` la propriété \([WPF][ReferenceWpfMicrosoftWebWebview2WpfWebview2Creationproperties] / [WinForms][ReferenceWinFormsMicrosoftWebWebview2WinFormsWebview2]\) sur l’élément WebView2.  Utilisez le `BrowserExecutableFolder` membre dans la classe `CoreWebView2CreationProperties` \([WPF][ReferenceWpfMicrosoftWebWebview2WpfCorewebview2creationpropertiesCorewebview2creationproperties] / [WinForms][ReferenceWinFormsMicrosoftWebWebview2WinForms]\) pour indiquer le chemin d’accès aux binaires de version fixe.  
        *   Utilisez `EnsureCoreWebView2Async` \([WPF][ReferenceWpfMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async] / [WinForms][ReferenceWinformsMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]\) pour spécifier l’environnement.  Utilisez le `browserExecutableFolder` paramètre [dans CoreWebView2Environment.CreateAsync][ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentCreateasync] pour indiquer le chemin d’accès aux binaires de version fixe.  
1.  Packagez et expédiez les binaires de version fixe avec votre application.  Mettez à jour les binaires selon le cas.  
    
### <a name="known-issues-for-fixed-version"></a>Problèmes connus pour la version fixe  

Par rapport au runtime persistant, la version fixe [][MicrosoftPlayReady] ne comprend pas de processus d’installation, ce qui Microsoft PlayReady ne fonctionne pas sans modification.  Vous pouvez atténuer le problème en effectuant les actions suivantes.  

1.  Recherchez le chemin d’accès où vous déployez le package version fixe sur l’appareil de l’utilisateur, par exemple l’emplacement suivant.
    
    ```text
    D:\myapp\Microsoft.WebView2.FixedVersionRuntime.87.0.664.8.x64
    ```  
    
1.  Exécutez les commandes suivantes sur l’appareil de l’utilisateur.

    ```shell
    icacls {Fixed Version path} /grant *S-1-15-2-2:(OI)(CI)(RX)
    icacls {Fixed Version path} /grant *S-1-15-2-1:(OI)(CI)(RX)
    ```  

1.  PlayReady doit fonctionner maintenant sur l’appareil de l’utilisateur.  Dans **l’onglet** Sécurité du **dossier Version fixe,** il doit inclure les autorisations pour `ALL APPLICATION PACKAGES` et `ALL RESTRICTED APPLICATION PACKAGES` .  

    :::image type="complex" source="../media/play-ready-permission.png" alt-text="Autorisation pour PlayReady" lightbox="../media/play-ready-permission.png":::
        Autorisation pour PlayReady  
    :::image-end:::  

<!-- links -->  

[ConceptsVersioning]: ./versioning.md "Comprendre les versions de navigateur et les | WebView2 Documents Microsoft"  
[HowToWebdriver]: ../how-to/webdriver.md "Automatisation et test de WebView2 avec Microsoft Edge driver | Documents Microsoft"  

[ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions : globals | Documents Microsoft"  
[ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring]: /microsoft-edge/webview2/reference/win32/webview2-idl#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString - Globals | Documents Microsoft"  

[DeployEdgeMicrosoftEdgeChannels]: /deployedge/microsoft-edge-channels "Vue d’ensemble des Microsoft Edge de | Documents Microsoft"  

[ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentCreateasync]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.createasync "CreateAsync - Classe Microsoft.Web.WebView2.Core.CoreWebView2Environment | Documents Microsoft"  
[ReferenceWpfMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async "Classe EnsureCoreWebView2Async -Microsoft.Web.WebView2.Wpf.WebView2 | Documents Microsoft"  
[ReferenceWinformsMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.winforms.webview2.ensurecorewebview2async "EnsureCoreWebView2Async - Classe Microsoft.Web.WebView2.WinForms.WebView2 | Documents Microsoft"  
[ReferenceWpfMicrosoftWebWebview2WpfCorewebview2creationpropertiesCorewebview2creationproperties]: /dotnet/api/microsoft.web.webview2.wpf.corewebview2creationproperties "CoreWebView2CreationProperties - Classe Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties | Documents Microsoft"  
[ReferenceWinFormsMicrosoftWebWebview2WinForms]: /dotnet/api/microsoft.web.webview2.winforms "Classe Microsoft.Web.WebView2.WinForms | Documents Microsoft"  
[ReferenceWpfMicrosoftWebWebview2WpfWebview2Creationproperties]: /dotnet/api/microsoft.web.webview2.wpf.webview2.creationproperties "CreationProperties - Classe Microsoft.Web.WebView2.Wpf.WebView2 | Documents Microsoft"  
[ReferenceWinFormsMicrosoftWebWebview2WinFormsWebview2]: /dotnet/api/microsoft.web.webview2.winforms.webview2 "Classe Microsoft.Web.WebView2.WinForms.WebView2 | Documents Microsoft"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2 Installer | Développeur Microsoft"  

[DownloadNonstableEdge]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback | GitHub"  

[GitHubMicrosoftEdgeWebView2SamplesWebview2Deployment]: https://github.com/MicrosoftEdge/WebView2Samples#webview2-deployment "Déploiement WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftPlayReady]: https://www.microsoft.com/playready "Microsoft PlayReady"  
