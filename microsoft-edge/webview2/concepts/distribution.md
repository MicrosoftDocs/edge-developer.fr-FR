---
description: Options de distribution lors de la publication d’une application à l’aide de Microsoft Edge WebView2
title: Distribution des applications WebView2 Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 89e53c43c3550d0a7a3707381cc4c76be111db28
ms.sourcegitcommit: 56cb5821d1b8e96f55bfa14a4ce87a3845b009c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182288"
---
# Distribution d’applications à l’aide de WebView2  

Lors de la distribution de votre application WebView2, assurez-vous que la plateforme Web de stockage, le [Runtime WebView2][Webview2Installer], est présente avant le démarrage de l’application.  Cet article décrit comment vous \ (le développeur \) avez installé le runtime  [WebView2 et utiliser](#evergreen-distribution-mode) les deux modes de distribution pour votre application WebView2: persistants et [version corrigée](#fixed-version-distribution-mode).  

## Mode de distribution persistant  

> [!NOTE]
> Le mode de distribution persistant est recommandé pour la plupart des développeurs.  

Le mode de distribution persistant garantit que votre application tire parti des dernières fonctionnalités et des mises à jour de sécurité.  Il présente les caractéristiques suivantes.  

*   La plateforme Web sous-jacente \ (WebView2 Runtime \) est automatiquement mise à jour sans aucun effort supplémentaire de votre part.  
*   Toutes les applications qui utilisent le mode de distribution persistant utilisent une copie partagée du runtime WebView2 persistant, qui économise de l’espace disque.  
    
### Présentation de la WebView2 Runtime  

WebView2 Runtime est un Runtime redistribuable qui sert de plateforme Web de stockage pour les applications WebView2.  Ce concept est similaire à celui des applications Visual C++ ou .NET Runtime pour C++/.NET.  Le Runtime contient les fichiers binaires Microsoft Edge \ (chrome \) modifiés qui sont affiné et testés pour les applications.  Dans le cadre de l’installation, le runtime n’apparaît pas sous la forme d’un navigateur visible par l’utilisateur.  Par exemple, un utilisateur ne dispose pas d’une entrée de raccourci sur le bureau ou de menu Démarrer.  

Lors du développement et des tests, vous pouvez utiliser la plateforme Web de stockage.  

*   Exécution de WebView2  
*   Tout Insider \ (non stable \) canal de navigateur Microsoft Edge \ (chrome \)  
    
Dans les environnements de production, vous devez vous assurer que le runtime est présent sur les appareils utilisateurs avant le démarrage de l’application.  Le canal stable Microsoft Edge n’est pas disponible pour l’utilisation de WebView2.  La décision empêche les applications d’adopter une dépendance sur le navigateur en production.

Ne prenez pas de dépendance sur le navigateur pour les raisons suivantes:  

*   Il n’est pas garanti que Microsoft Edge \ (chrome \) soit présent sur tous les appareils utilisateurs.  Par exemple, les appareils déconnectés de Windows Update ou qui ne sont pas gérés directement par Microsoft \ (une grande partie du marché entreprise et EDU) ne disposent pas du navigateur.  La possibilité de distribuer le runtime WebView2 évite d’adopter une dépendance sur le navigateur en tant qu’indispensable pour les applications.  
*   Les navigateurs et applications ont des cas d’utilisation différents, et par conséquent, il est possible que les dépendances sur un navigateur aient des effets inattendus sur vos applications.  Par exemple, il est possible que les administrateurs informatiques contrôlent la version du navigateur pour la compatibilité du site Web interne.  Le runtime WebView2 permet aux applications de rester persistantes lorsque les mises à jour de navigateur sont activement gérées.  
*   Contrairement au navigateur, le runtime est développé et testé pour les scénarios d’application, et dans certains cas, il peut y avoir des corrections de bogues qui ne sont pas encore disponibles dans le navigateur.  
    
À l’avenir, les WebView2s d’exécution persistantes à livrer dans de futures versions de Windows.  Déployez le Runtime avec votre application de production jusqu’à ce que le runtime soit plus universellement disponible.  

### Déploiement de l’exécutable WebView2 persistant  

Une seule installation de l’exécutable WebView2 persistant est nécessaire pour toutes les applications persistantes sur l’appareil.  Plusieurs outils sont disponibles sur la [page de téléchargement de WebView2 Runtime][Webview2Installer].  Les outils suivants vous aident à déployer le runtime persistant.  

*   Le programme d’amorçage du runtime WebView2 est un programme d’installation minuscule \ (approximativement 2 Mo).  Le programme d’amorçage du runtime WebView2 télécharge et installe le runtime à partir de serveurs Microsoft qui correspond à l’architecture de l’appareil de l’utilisateur.  
*   Utilisez un lien pour télécharger le programme d’amorçage par programmation.  
*   Le programme d’installation autonome de WebView2 Runtime est un programme d’installation complet qui installe le runtime WebView2 persistant dans les environnements hors connexion.  
    
Pour le moment, le programme d’amorçage et le programme d’installation autonome prennent uniquement en charge les installations par ordinateur qui nécessitent une élévation.  Si un programme d’installation est exécuté sans élévation, l’utilisateur est invité à élever ses autorisations.  

Utilisez les flux de travail suivants pour vérifier que le runtime est déjà installé avant le lancement de l’application.  Vous pouvez ajuster votre flux de travail en fonction de votre scénario.  Un exemple de code est disponible dans le [Samples référentiel Samples] [GitHubMicrosoftedgeWebView2samplesWebview2Deployment].  

#### Déploiement en ligne uniquement  

Si vous avez un scénario de déploiement en ligne uniquement dans lequel les utilisateurs sont supposés disposer d’un accès à Internet, suivez les étapes ci-dessous.  

1.  Lors de la configuration de votre application, assurez-vous que le runtime est déjà installé.  Pour procéder à la vérification, effectuez l’une des actions suivantes.  
    *   Recherchez s' `pv (REG_SZ)` il existe un contrôle RegKey et qu’il n’est pas `null` ou vide.  Accédez  `pv (REG_SZ)` à l’emplacement suivant.  
        
        Sous Windows 64 bits  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
        Sous Windows 32 bits  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
    *   Exécutez [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring] et assurez-vous que le `versionInfo` est `NULL` .  
1.  Si le runtime n’est pas installé, utilisez le lien pour télécharger le programme d’amorçage par programmation.  
1.  Invoquez le programme d’amorçage à partir d’un processus ou d’une invite de commandes avec élévation de privilèges `MicrosoftEdgeWebview2Setup.exe /silent /install` pour une installation silencieuse.  
    
Le flux de travail précédent offre les avantages suivants.  

*   Installez le runtime uniquement quand cela est nécessaire ou que vous n’êtes pas obligé d’installer un package.  
*   Le programme d’amorçage détecte automatiquement l’architecture de l’appareil et installe le runtime correspondant.  
*   Installez le runtime en silence.  
    
Vous pouvez également choisir de conditionner le programme de démarrage avec votre application au lieu de le télécharger par programmation à la demande.  

#### Déploiement hors connexion  

Si vous avez un scénario de déploiement hors connexion dans lequel le déploiement de l’application doit fonctionner entièrement hors connexion, procédez comme suit.  

1.  Téléchargez le [programme d’installation autonome][Webview2Installer].  
1.  Incluez le programme d’installation dans le programme d’installation ou de mise à jour de votre application.  
1.  Lors de la configuration de votre application, assurez-vous que le runtime est déjà installé.  Pour procéder à la vérification, effectuez l’une des actions suivantes.  
    *   Recherchez s' `pv (REG_SZ)` il existe un contrôle RegKey et qu’il n’est pas `null` ou vide.  Accédez  `pv (REG_SZ)` à l’emplacement suivant.  
        
        Sous Windows 64 bits  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
        Sous Windows 32 bits  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
    *   Exécutez [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring] et assurez-vous que le `versionInfo` est `NULL` .  
1.  Si le runtime n’est pas installé, exécutez le programme d’installation autonome.  Si vous voulez exécuter une installation silencieuse, exécutez le programme d’installation à partir d’un processus avec élévation de privilèges ou copiez et exécutez la commande suivante.  
    
    ```shell
    MicrosoftEdgeWebView2RuntimeInstaller{X64/X86/ARM64}.exe /silent /install
    ```  
    
### Restez compatible en mode persistant  

Le Web évolue constamment.  Le runtime WebView2 persistant est mis à jour de manière à vous fournir les fonctionnalités les plus récentes et les correctifs de sécurité.  Pour vous assurer que votre application reste compatible avec le Web, vous devez configurer l’infrastructure de test.  

Les canaux Microsoft Edge non stables \ (bêta/dev/Canaries \) offrent un aperçu de ce qui se passe dans WebView2 Runtime.  Tout comme le développement de sites Web pour Microsoft Edge, nous vous conseillons de tester régulièrement votre application WebView2.  Testez votre application WebView2 sur l’un des canaux non stables et mettez à jour votre application ou [signalez des problèmes][GithubMicrosoftedgeWebviewfeedback] en cas de problème. En règle générale, le développement et la version bêta sont les canaux recommandés.  Pour vous aider à déterminer le canal qui vous convient, accédez à [vue d’ensemble des canaux Microsoft Edge][DeployEdgeMicrosoftEdgeChannels].  Vous pouvez télécharger le [canal Microsoft Edge non stable][DownloadNonstableEdge] sur votre environnement de test et utiliser des `regkey` variables d’environnement pour indiquer les préférences de canal de votre application de test.  Pour plus d’informations, accédez à [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions].  Vous pouvez également utiliser [WebDriver][HowtoWebdriver] pour automatiser les tests WebView2.

## Mode de distribution de version fixe  

> [!NOTE]
> Le mode de distribution de la version fixe est en version publique preview.  

Le mode de distribution de la version fixe a été auparavant appelé «vous-même».  

Pour les environnements restreints ayant des exigences de compatibilité strictes, envisagez d’utiliser le mode de distribution de version fixe.  Choisissez et Empaquetez une version spécifique du runtime WebView2 à l’aide du mode de distribution de version fixe.  Vous pouvez spécifier le minutage des mises à jour de l’exécution de votre application.  Le mode de distribution de la version fixe ne reçoit pas de mises à jour automatiques. Envisagez de mettre à jour votre application et le Runtime.  

Pour utiliser le mode de version fixe, effectuez les actions suivantes:

1.  [Téléchargez][Webview2Installer] le package de la version fixe. 
1.  Décompressez le package à l’aide de la ligne de commande `expand {path to the package} -F:* {path to the destination folder}` ou d’outils tels que WinRAR. Évitez de décompresser les fichiers dans l’Explorateur de fichiers, car il est possible que la structure de dossiers ne soit pas valide.  
1.  Incluez les fichiers binaires de version fixes décompressés dans votre projet.  
1.  Spécifiez le chemin d’accès aux fichiers binaires de version fixe lors de la création de l’environnement WebView2.  
    *   Pour Win32 C/C++, vous pouvez créer l’environnement à l’aide de la fonction [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions] .  Utilisez le `browserExecutableFolder` paramètre pour indiquer le chemin d’accès au dossier contenant `msedgewebview2.exe` .  
    *   Pour .NET, vous pouvez effectuer l’une des options suivantes pour spécifier l’environnement.  
        
        > [!NOTE]
        > Vous devez spécifier l’environnement pour que la `Source` propriété WebView2 prenne effet.  
        
        *   Définissez la `CreationProperties` propriété \ ([WPF][ReferenceWpfMicrosoftWebWebview2WpfWebview2Creationproperties] / [WinForms][ReferenceWinFormsMicrosoftWebWebview2WinFormsWebview2]\) sur l’élément WebView2.  Utilisez le `BrowserExecutableFolder` membre de la `CoreWebView2CreationProperties` classe \ ([WPF][ReferenceWpfMicrosoftWebWebview2WpfCorewebview2creationpropertiesCorewebview2creationproperties] / [WinForms][ReferenceWinFormsMicrosoftWebWebview2WinForms]\) pour indiquer le chemin d’accès aux fichiers binaires de version fixes.  
        *   Utilisez `EnsureCoreWebView2Async` \ ([WPF][ReferenceWpfMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async] / [WinForms][ReferenceWinformsMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]de WPF) pour spécifier l’environnement.  Utilisez le `browserExecutableFolder` paramètre dans [CoreWebView2Environment. CreateAsync][ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentCreateasync] pour indiquer le chemin d’accès aux fichiers binaires de version fixes.  
1.  Empaquetez et expédiez les fichiers binaires de la version fixe avec votre application.  Mettez à jour les fichiers binaires, le cas échéant.  
    
### Problèmes connus de la version corrigée  

Comparé à l’exécution persistantes, la version corrigée n’a pas de processus d’installation, ce qui a pour effet que [Microsoft PlayReady][MicrosoftPlayReady] ne fonctionne pas sans modification.  Vous pouvez limiter le problème en effectuant les opérations suivantes.  

1.  Localisez le chemin d’accès dans lequel vous déployez le package de version fixe sur l’appareil de l’utilisateur, tel que l’emplacement suivant.
    
    ```text
    D:\myapp\Microsoft.WebView2.FixedVersionRuntime.87.0.664.8.x64
    ```  
    
1.  Exécutez les commandes suivantes sur l’appareil de l’utilisateur.

    ```shell
    icacls {Fixed Version path} /grant *S-1-15-2-2:(OI)(CI)(RX)
    icacls {Fixed Version path} /grant *S-1-15-2-1:(OI)(CI)(RX)
    ```  

1.  PlayReady doit être en cours d’exécution sur l’appareil de l’utilisateur.  Dans l’onglet **sécurité** du dossier **version fixe** , vous devez inclure les autorisations pour `ALL APPLICATION PACKAGES` et `ALL RESTRICTED APPLICATION PACKAGES` .  

    :::image type="complex" source="../media/play-ready-permission.png" alt-text="Autorisation pour PlayReady" lightbox="../media/play-ready-permission.png":::
        Autorisation pour PlayReady  
    :::image-end:::  

<!-- links -->  

[ConceptsVersioning]: ./versioning.md "Présentation des versions de navigateur et de WebView2 | Documents Microsoft"  
[HowtoWebdriver]: ../howto/webdriver.md "Automatisation et test de WebView2 avec le pilote Microsoft Edge | Documents Microsoft"  

[ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-global | Documents Microsoft"  
[ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring]: /microsoft-edge/webview2/reference/win32/webview2-idl#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString-global | Documents Microsoft"  

[DeployEdgeMicrosoftEdgeChannels]: /deployedge/microsoft-edge-channels "Vue d’ensemble des canaux Microsoft Edge | Documents Microsoft"  

[ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentCreateasync]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.createasync "CreateAsync-Microsoft. Web. WebView2. Core. CoreWebView2Environment classe | Documents Microsoft"  
[ReferenceWpfMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async "EnsureCoreWebView2Async-Microsoft. Web. WebView2. WPF. WebView2 classe | Documents Microsoft"  
[ReferenceWinformsMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.winforms.webview2.ensurecorewebview2async "EnsureCoreWebView2Async-Microsoft. Web. WebView2. WinForms. WebView2 classe | Documents Microsoft"  
[ReferenceWpfMicrosoftWebWebview2WpfCorewebview2creationpropertiesCorewebview2creationproperties]: /dotnet/api/microsoft.web.webview2.wpf.corewebview2creationproperties "CoreWebView2CreationProperties-Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties classe | Documents Microsoft"  
[ReferenceWinFormsMicrosoftWebWebview2WinForms]: /dotnet/api/microsoft.web.webview2.winforms "Classe Microsoft. Web. WebView2. WinForms | Documents Microsoft"  
[ReferenceWpfMicrosoftWebWebview2WpfWebview2Creationproperties]: /dotnet/api/microsoft.web.webview2.wpf.webview2.creationproperties "CreationProperties-Microsoft. Web. WebView2. WPF. WebView2 classe | Documents Microsoft"  
[ReferenceWinFormsMicrosoftWebWebview2WinFormsWebview2]: /dotnet/api/microsoft.web.webview2.winforms.webview2 "Classe Microsoft. Web. WebView2. WinForms. WebView2 | Documents Microsoft"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Programme d’installation d’WebView2 | Développeur Microsoft"  

[DownloadNonstableEdge]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView | GitHub"  

[GitHubMicrosoftMicrosoftEdgeWebView2SamplesWebview2Deployment]: https://github.com/MicrosoftEdge/WebView2Samples#webview2-deployment "Déploiement de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftPlayReady]: https://www.microsoft.com/playready "Microsoft PlayReady"  
