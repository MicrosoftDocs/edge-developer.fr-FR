---
description: Découvrez les meilleures pratiques de développement à utiliser lors du développement de votre application WebView2.
title: Meilleures pratiques de développement WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, webview, edge, meilleures pratiques
ms.openlocfilehash: 7e8c6746e864b474c2987817c521224499a95e1f
ms.sourcegitcommit: 5ae09b1ad6cd576c9fec12538b23cd849861f2b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2021
ms.locfileid: "11627977"
---
# <a name="webview2-development-best-practices"></a>Meilleures pratiques de développement WebView2  

Chaque équipe de développement suit différentes pratiques lors de la création de son application. Lorsque vous créez des applications WebView2, nous vous recommandons de suivre certaines pratiques. Cet article décrit ces recommandations et meilleures pratiques pour vous lors de la création d’applications WebView2 basées sur la production.

## <a name="use-evergreen-webview2-runtime-recommended"></a>Utiliser le runtime WebView2 persistant (recommandé)  

Bien que la version fixe ait des cas d’utilisation pour les applications qui ont des exigences de compatibilité strictes, nous vous recommandons généralement d’utiliser le runtime WebView2 persistant.  Le runtime WebView2 persistant se met à jour automatiquement et inclut les dernières fonctionnalités et correctifs de sécurité disponibles pour votre application WebView2. Le runtime WebView2 persistant nécessite également moins d’espace de stockage sur le disque.

Assurez-vous que le runtime WebView2 persistant est installé avant d’utiliser votre application WebView2.  Pour plus d’informations, [accédez à Déployer le runtime WebView2][Webview2ConceptsDistributionDeployingEvergreenWebview2Runtime]persistant.  

## <a name="run-compatibility-tests-regularly-when-using-the-evergreen-webview2-runtime"></a>Exécuter des tests de compatibilité régulièrement lors de l’utilisation du runtime WebView2 persistant

Lorsque vous utilisez le runtime WebView2 persistant, celui-ci est mis à jour automatiquement, vous devez donc exécuter régulièrement des tests de compatibilité. Testez le contenu web dans le contrôle WebView2 par rapport aux versions non stables de Microsoft Edge, pour vous assurer que votre application WebView2 fonctionne comme prévu.

Ces conseils sont semblables aux instructions que nous donnez aux développeurs web. Pour plus d’informations, accédez [à Rester compatible en mode persistant.][Webview2ConceptsDistributionStayCompatibleEvergreenMode]

## <a name="ensure-apis-are-supported-by-the-installed-webview2-runtime"></a>S’assurer que les API sont pris en charge par le runtime WebView2 installé

Les applications WebView2 ont besoin d’un SDK Webview2 et d’un runtime WebView2 installé sur l’ordinateur pour s’exécuter. Le SDK et le runtime sont tous deux en version. Étant donné que les API sont continuellement ajoutées à WebView2, de nouvelles versions du runtime sont également publiées pour prendre en charge les nouvelles API. Assurez-vous que les API utilisées par votre application WebView2 sont pris en charge par le runtime WebView2 installé sur l’ordinateur. 

Si vous utilisez le runtime WebView2 persistant, il se peut que le runtime ne soit pas mis à jour pour utiliser la dernière version. Par exemple, lorsque les utilisateurs n’ont pas accès à Internet, le runtime n’est pas automatiquement mis à jour dans cet environnement. En outre, l’utilisation de certaines stratégies de groupe interrompt les mises à jour WebView2. Lorsque vous pushez une mise à jour vers votre application WebView2, l’application peut se rompre car elle utilise des API plus nouvelles qui ne sont pas disponibles dans le runtime installé.   
 
Pour résoudre cette situation, vous pouvez tester la disponibilité des API dans le runtime installé, avant que votre code appelle l’API. Ce test pour les nouvelles fonctionnalités est similaire à d’autres meilleures pratiques de développement web qui détectent les fonctionnalités prise en charge avant d’utiliser de nouvelles API web. Pour tester la disponibilité de l’API dans le runtime installé, utilisez :  

*   En `queryinterface` C/C++. 
*   Bloc try/catch dans .NET ou WinUI. 
    
Pour plus d’informations, [accédez à Déterminer la condition d’runtime WebView2.][Webview2ConceptsVersioningDetermineWebview2RuntimeRequirement]  

## <a name="update-the-fixed-version-runtime"></a>Mettre à jour le runtime de version fixe  

Si vous utilisez le runtime de version fixe, veillez à mettre à jour votre runtime régulièrement pour réduire les risques potentiels de sécurité. Lorsque vous utilisez du contenu tiers dans les applications Webview2, pensez toujours au contenu non confiance.  Pour plus d’informations, accédez [au mode de distribution version fixe.][Webview2ConceptsDistributionFixedVersionDistributionMode]  

## <a name="manage-new-versions-of-the-runtime"></a>Gérer les nouvelles versions du runtime  

Lorsqu’une nouvelle version du runtime WebView2 persistant est téléchargée sur l’appareil, toutes les applications WebView2 en cours d’exécution continuent d’utiliser le runtime précédent, jusqu’à ce que le processus du navigateur soit publié.  Ce comportement permet aux applications de s’exécuter en continu et empêche la suppression du runtime précédent.  Pour utiliser la nouvelle version du runtime, vous devez libérer toutes les références aux objets d’environnement WebView2 précédents ou redémarrer votre application.  La prochaine fois que vous créerez un environnement WebView2, il utilisera la nouvelle version.

Lorsqu’une nouvelle version est disponible, vous pouvez prendre automatiquement des mesures, comme avertir l’utilisateur de redémarrer l’application.  Pour détecter qu’une nouvelle version est disponible, vous pouvez utiliser l’événement [add_NewBrowserVersionAvailable(Win32)][Webview2ReferenceaddNewBrowserVersionAvailable] ou [CoreWebView2Environment.NewBrowserVersionAvailable(.NET)][Webview2ReferenceNewBrowserVersionAvailable] dans votre code. Si votre code gère le redémarrage de l’application, envisagez d’enregistrer l’état de l’utilisateur avant la sortie de l’application WebView2.  

## <a name="manage-the-lifetime-of-the-user-data-folder"></a>Gérer la durée de vie du dossier de données utilisateur 
Les applications WebView2 créent un dossier de données utilisateur pour stocker des données telles que les cookies, les informations d’identification et les autorisations.  Après avoir créé le dossier, votre application est responsable de la gestion de la durée de vie du dossier de données utilisateur.  Par exemple, votre application doit faire un nettoyage lorsque l’application est désinstallée.  Pour plus d’informations, [accédez à Gestion du dossier de données utilisateur.][Webview2ConceptsUserDataFolder]  

## <a name="handle-runtime-process-failures"></a>Gérer les échecs de processus d’runtime
Votre application WebView2 doit écouter et gérer l’événement, afin que l’application puisse récupérer des défaillances de processus d’runtime qui gèrent le processus `ProcessFailed` d’application WebView2.

Les applications WebView2 sont pris en charge par une collection de processus d’utilisation qui s’exécutent avec le processus d’application. Ces processus d’exécution de prise en charge peuvent échouer pour diverses raisons, telles que le manque de mémoire ou l’arrêt par l’utilisateur. En cas d’échec d’un processus runtime de prise en charge, WebView2 avertit l’application en augmentant [l’événement ProcessFailed][WebView2ProcessFailedEvent].

## <a name="follow-recommended-webview2-security-best-practices"></a>Respecter les meilleures pratiques recommandées en matière de sécurité WebView2 
Pour n’importe quelle application WebView2, veillez à suivre nos meilleures pratiques recommandées en matière de sécurité WebView2.  Pour plus d’informations, [accédez aux meilleures pratiques pour le développement d’applications WebView2 sécurisées.][Webview2ConceptsSecurity]  

<!-- links -->  

[Webview2ConceptsDistributionDeployingEvergreenWebview2Runtime]: ../concepts/distribution.md#deploying-the-evergreen-webview2-runtime "Déploiement du runtime WebView2 persistant : distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[Webview2ConceptsDistributionFixedVersionDistributionMode]: ../concepts/distribution.md#fixed-version-distribution-mode "Mode de distribution de version fixe : distribution des applications à l’aide de WebView2 | Documents Microsoft"  
[Webview2ConceptsDistributionStayCompatibleEvergreenMode]: ../concepts/distribution.md#stay-compatible-in-evergreen-mode "Restez compatible en mode persistant : distribution des applications à l’aide de WebView2 | Documents Microsoft"  
[Webview2ConceptsSecurity]: ../concepts/security.md "Meilleures pratiques pour le développement d’applications WebView2 sécurisées | Documents Microsoft"  
[Webview2ConceptsUserDataFolder]: ../concepts/user-data-folder.md "Gérer le dossier de données utilisateur | Documents Microsoft"  
[Webview2ConceptsVersioningDetermineWebview2RuntimeRequirement]: ../concepts/versioning.md#determine-webview2-runtime-requirement "Déterminer l’exigence d’runtime WebView2 : comprendre les versions du SDK WebView2 | Documents Microsoft"  
[Webview2GetStartedWin32]: ../get-started/win32.md "Commencer à prendre en | WebView2 Documents Microsoft"  
[Webview2GetStartedWinforms]: ../get-started/winforms.md "Commencer à travailler avec WebView2 dans Windows Forms | Documents Microsoft"  
[Webview2GetStartedWinui]: ../get-started/winui.md "Mise en place de WebView2 dans WinUI 3 (prévisualisation) | Documents Microsoft"  
[Webview2GetStartedWpf]: ../get-started/wpf.md "Mise en place de WebView2 dans WPF | Documents Microsoft"  

[Webview2ReferenceaddNewBrowserVersionAvailable]: /microsoft-edge/webview2/reference/win32/icorewebview2environment#add_newbrowserversionavailable "add_NewBrowserVersionAvailable | Documents Microsoft"  

[Webview2ReferenceNewBrowserVersionAvailable]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.newbrowserversionavailable "Événement CoreWebView2Environment.NewBrowserVersionAvailable | Documents Microsoft"  
[WebView2ProcessFailedEvent]: /microsoft-edge/webview2/reference/win32/icorewebview2processfailedeventargs "ICoreWebView2ProcessFailedEventArgs | Documents Microsoft"  

