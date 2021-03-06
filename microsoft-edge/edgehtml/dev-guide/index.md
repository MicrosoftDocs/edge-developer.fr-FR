---
description: Ce guide fournit une vue d’ensemble des fonctionnalités et normes de développement incluses dans Microsoft Edge.
title: Nouveautés de EdgeHTML 18
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: edgehtml
keywords: edge, développement web, html, css, javascript, développeur, devtools
ms.custom: RS5
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6b53163115ad7db8e5b792cadda0c59b93b6711b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399224"
---
# <a name="microsoft-edge-developer-guide"></a>Guide du développeur Microsoft Edge  

> [!TIP]
> Nous avons [](https://blogs.windows.com/msedgedev/2017/10/18/documenting-web-together-mdn-web-docs/) établi un partenariat avec d’autres navigateurs et la communauté web en adoptant [MDN Web Docs](https://developer.mozilla.org/) comme l’endroit définitif pour la documentation utile, non objective et indépendant du navigateur pour les technologies web actuelles et émergentes basées sur des normes.  Vous trouverez des détails sur la prise en charge de l’API EdgeHTML directement dans chaque page de la bibliothèque de [références web MDN.](https://developer.mozilla.org/docs/Web)  Consultez l’état de [la plateforme de](https://developer.microsoft.com/microsoft-edge/platform/status/?q=edge%3AShipped%20edge%3APrefixed%20edge%3A'Preview%20Release) Microsoft Edge pour obtenir les dernières fonctionnalités prise en charge dans Microsoft Edge.  

## <a name="whats-new-in-edgehtml-18"></a>Nouveautés de EdgeHTML 18  

EdgeHTML 18 inclut les fonctionnalités nouvelles et mises à jour suivantes livrées dans la version actuelle de la plateforme Microsoft Edge, à partir de la mise à jour d’octobre [2018 de Windows 10](/windows/uwp/whats-new/windows-10-build-17763) \(10/2018, build 17763\).  Pour plus d’informations sur les modifications apportées à des builds [Windows Insider](https://insider.windows.com) Preview spécifiques, voir lelog des modifications de [Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/changelog) et les [nouveautés dans EdgeHTML.](./whats-new.md)  

Voici le lien de la liste de modifications suivante [https://docs.microsoft.com/microsoft-edge/dev-guide](#new-apis-in-edgehtml-18) :  

## <a name="new-and-updated-features"></a>Fonctionnalités nouvelles et mises à jour  

### <a name="autoplay-policies"></a>Stratégies d’exécution automatique  

Avec la mise à jour d’octobre 2018 de Windows 10, Microsoft Edge offre aux clients la possibilité de personnaliser leurs préférences de navigation sur les sites web qui l’utilisent pour la lecture automatique de contenu multimédia afin de minimiser les distractions sur le web et d’économiser la bande passante.  Les utilisateurs peuvent personnaliser le comportement des médias avec des contrôles de jeu automatique globaux et par site.  En outre, Microsoft Edge supprime automatiquement laplay automatique des médias dans les onglets d’arrière-plan.  

Consultez le guide [des stratégies](./browser-features/autoplay-policies.md) de jeu automatique pour obtenir des détails et les meilleures pratiques pour garantir une bonne expérience utilisateur avec les médias hébergés sur votre site.  

### <a name="chakra-improvements"></a>Améliorations apportées à Ces améliorations  

EdgeHTML 18 inclut des mises à jour du moteur JavaScript JavaScript pour prendre en charge les nouvelles fonctionnalités ES et WASM, en plus des améliorations des performances et de l’interopérabilité.  Pour plus d’informations, consultez les notes de publication [de ContrôleCore 1.11.](https://github.com/Microsoft/ChakraCore/wiki/Roadmap#chakracore-111)  

### <a name="css-updates"></a>Mises à jour CSS  

Nous avons effectué d’autres progrès sur notre implémentation expérimentale de masquage [CSS](https://developer.mozilla.org/docs/Web/CSS/CSS_Masking) \(derrière l’indicateur Activer le *masquage CSS\)* avec la prise en charge supplémentaire pour le masque [composite,](https://developer.mozilla.org/docs/Web/CSS/mask-composite)la [position](https://developer.mozilla.org/docs/Web/CSS/mask-position)du masque et le [masque-répéter.](https://developer.mozilla.org/docs/Web/CSS/mask-repeat)  Pour la compatibilité des sites, Microsoft Edge prend également en charge les propriétés *-webkit-* suivantes : -webkit-mask, -webkit-mask-composite, -webkit-mask-image, -webkit-mask-position, -webkit-mask-position-x, -webkit-mask-position-y, -webkit-mask-repeat, -webkit-mask-size.  

En outre, Microsoft Edge dispose désormais de la prise en charge de l’enveloppe de [dépassement](https://developer.mozilla.org/docs/Web/CSS/overflow-wrap) de capacité et de la prise en charge partielle du comportement de la [sur-inscription](https://developer.mozilla.org/docs/Web/CSS/overscroll-behavior) \( et `auto` des `contain` valeurs\).  

### <a name="developer-tools"></a>Outils de développement  

La dernière mise à jour de Microsoft Edge DevTools ajoute un certain nombre de commodités à la fois à l’interface utilisateur et sous le capot, y compris de nouveaux panneaux dédiés pour les travailleurs de service et le stockage, les outils de recherche de fichiers source dans le débogueur et les nouveaux domaines de protocole Edge DevTools pour le débogage de style/disposition et les API de console.  

DevTools dans la dernière mise à jour [de Windows 10 (EdgeHTML 18)](./whats-new.md) présente tous les détails.  

### <a name="listening-to-your-feedback"></a>À l’écoute de vos commentaires  

Nous sommes à l’écoute de vos commentaires et avons implémenté la prise en charge de plusieurs API demandées dans EdgeHTML 18, y compris la méthode [DataTransfer.setDragImage()](https://developer.mozilla.org/docs/Web/API/DataTransfer/setDragImage) utilisée pour définir une image personnalisée lors du glisser-déposer, et [secureConnectionStart](https://developer.mozilla.org/docs/Web/API/PerformanceResourceTiming/secureConnectionStart), une propriété de l’API performance de minutage des ressources, qui peut être utilisée pour renvoyer un timestamp juste avant que le navigateur démarre le processus d’établissement d’une liaison pour sécuriser la connexion actuelle.  

En outre, personne n’aime l’éumeration de la collection d’attributs. Nous avons donc ajouté la prise en charge de [Element.getAttributeNames](https://developer.mozilla.org/docs/Web/API/Element/getAttributeNames) pour renvoyer les noms d’attribut de l’élément sous la forme d’un tableau de chaînes, ainsi [que, Element.toggleAttribute](https://developer.mozilla.org/docs/Web/API/Element/toggleAttribute) pour faire bascule un attribut booléen \(suppression si présent et ajout si non\).  

### <a name="progressive-web-apps"></a>Applications web progressives  

#### <a name="lifetime-background-script"></a>Script en arrière-plan de durée de vie  

Les applications JavaScript Windows 10 \(applications web en cours d’exécution dans un processus\) prend désormais en charge un script d’arrière-plan facultatif par application qui démarre avant l’activation des affichages et s’exécute pendant toute la durée du `WWAHost.exe` processus.  Ainsi, vous pouvez surveiller et modifier les navigations, suivre l’état des navigations, surveiller les erreurs de navigation et exécuter le code avant l’activation des affichages.  

Lorsqu’il est [](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) spécifié comme page de démarrage dans le manifeste de votre [application,](/uwp/schemas/appxpackage/appx-package-manifest)chacun des affichages de l’application \(windows\) est exposé au script en tant qu’instances de la nouvelle classe [WebUIView,](/uwp/api/windows.ui.webui.webuiview) fournissant les mêmes événements, propriétés et méthodes qu’un affichage [WebView](/uwp/api/windows.web.ui.iwebviewcontrol)\(Win32\) général.  Votre script peut écouter [l’événement NewWebUIViewCreated](/uwp/api/windows.ui.webui.newwebuiviewcreatedeventargs) pour intercepter le contrôle de la navigation pour une nouvelle vue :  

```javascript
Windows.UI.WebUI.WebUIApplication.addEventListener("newwebuiviewcreated", newWebUIViewCreatedEventHandler);
```  

 Toute activation d’application avec le script en arrière-plan s’appuie `StartPage` sur le script lui-même pour la navigation.  

#### <a name="text-scaling"></a>Mise à l’échelle du texte  

La mise à jour d’octobre 2018 de Windows 10 introduit le paramètre « Agrandir le texte » pour améliorer l’accessibilité des utilisateurs finaux, et les applications de bureau à long terme installées sur Windows \(en plus des applications UWP et de bureau\) la prise en charge automatique de cette fonctionnalité. [](/windows/uwp/design/input/text-scaling#user-experience)  Pour les contrôles PWA et WebView, l’échelle de texte fonctionne de la même manière que la mise à l’échelle DESPI.  Si un utilisateur modifie à la fois l’échelle de texte et l’échelle DEPI, le résultat est le produit des deux.  

 Pour obtenir des conseils de conception, consultez le guide de mise à [l’échelle](/windows/uwp/design/input/text-scaling) du texte UWP sur *le Centre de développement Windows.*  

### <a name="service-worker-updates"></a>Mises à jour du service de travail  

Pour obtenir une actualisation de ce que sont les travailleurs de service et de leur fonctionnement, consultez le résumé de [l’API](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) de travail de service rédigé par nos partenaires sur le site MDN.  Plusieurs mises à jour ont été mises à jour pour les employés de service de prise en charge de Microsoft Edge dans EdgeHTML 18.  Permet au service de travail d’utiliser `fetchEvent` [preloadResponse](https://developer.mozilla.org/docs/Web/API/FetchEvent) [](https://developer.mozilla.org/docs/Web/API/FetchEvent/clientId) pour la promesse d’une réponse et à l’ID du client contrôlé par le service actuel.  
L’interface [NavigationPreloadManager](https://developer.mozilla.org/docs/Web/API/NavigationPreloadManager) fournit des méthodes pour gérer le préchargement des ressources, ce qui vous permet d’effectuer une demande en parallèle pendant le démarrage d’un service, ce qui évite tout délai.  Consultez les [propriétés d’API](#new-apis-in-edgehtml-18) nouvellement prise en charge pour obtenir la liste des méthodes et propriétés de préchargement du service Worker.  

### <a name="web-authentication"></a>Authentification web  

Microsoft Edge inclut désormais une prise en charge sans [préfixe](https://blogs.windows.com/msedgedev/2018/07/30/introducing-web-authentication-microsoft-edge) pour la nouvelle API d’authentification web \(également [appelée WebAuthN](https://w3c.github.io/webauthn)\).  L’authentification web fournit une solution ouverte, évolutive et interopérable pour simplifier l’authentification, ce qui permet de mieux sécuriser les expériences utilisateur en remplaçant les mots de passe par des informations d’identification matérielles plus puissantes.  L’implémentation dans Microsoft Edge permet d’utiliser [Windows Hello](https://www.microsoft.com/windows/windows-hello) pour permettre aux utilisateurs de se connecter avec leur visage, leur empreinte digitale ou leur code confidentiel, en plus des authentifiés [externes](https://fidoalliance.org) tels que les clés de sécurité FIDO2 ou les clés de sécurité FIDO U2F, pour s’authentifier en toute sécurité auprès des sites web.  

Pour plus d’informations, voir le billet de blog [Introducing Web Authentication in Microsoft Edge](https://blogs.windows.com/msedgedev/2018/07/30/introducing-web-authentication-microsoft-edge).  

### <a name="webdriver"></a>WebDriver  

WebDriver est désormais une fonctionnalité [Windows](https://docs.microsoft.com/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) à la demande \(FoD\), ce qui facilite plus que jamais l’automatisation des tests dans Microsoft Edge et l’accès à la version de votre appareil.  Vous n’aurez plus besoin de faire correspondre manuellement la version/branche/version lors de l’installation de WebDriver, votre [WebDriver](https://www.w3.org/TR/webdriver) sera automatiquement mis à jour pour correspondre aux nouvelles mises à jour Windows 10.  

Vous pouvez installer WebDriver en libérant le mode développeur ou en l’installant en mode autonome en passant à Paramètres Applications Applications & fonctionnalités Gérer les **fonctionnalités**  >  ****  >  ****  >  **facultatives.**  Pour plus d’informations, consultez [l’annonce WebDriver sur le site de blog Windows.](https://blogs.windows.com/msedgedev/2018/06/14/webdriver-w3c-recommendation-feature-on-demand)  

### <a name="web-notification-properties"></a>Propriétés de notification web  

Quatre nouvelles propriétés sont désormais prises en charge pour les notifications web :  [actions,](https://developer.mozilla.org/docs/Web/API/notification/actions) [badge,](https://developer.mozilla.org/docs/Web/API/notification/badge) [image](https://developer.mozilla.org/docs/Web/API/notification/image)et , amélioration de notre capacité à créer des notifications sur le web compatibles avec les systèmes de notification existants, tout en restant indépendantes de la  `maxActions` plateforme.  

### <a name="webview"></a>WebView  

#### <a name="service-workers"></a>Travailleurs du service  

[Les travailleurs](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) du service sont désormais pris en charge dans le contrôle WebView, en plus du navigateur Microsoft Edge et des applications JavaScript Windows 10.  Toutes les versions de Microsoft Edge webview \([PWA](/microsoft-edge/hosting/webview), [UWP](/uwp/api/Windows.UI.Xaml.Controls.WebView), [Win32](/windows/communitytoolkit/controls/wpf-winforms/webview)\) prise en charge les travailleurs du service, toutefois, n’hésitez pas à noter que l’API [Push](https://developer.mozilla.org/docs/Web/API/Push_API) n’est pas encore disponible pour les versions UWP et Win32.  

Les architectures d’application x64 nécessitent des packages Neutre \(N’importe quel processeur\) ou x64, car les travailleurs du service ne sont pas pris en charge dans les processus WoW64.  \(Pour économiser de l’espace disque, la version WoW des DLLs requises n’est pas incluse en natif dans Windows.\)  

#### <a name="win32-webview-updates"></a>Mises à jour de Win32 WebView  

Le EdgeHTML [WebViewControl](/windows/communitytoolkit/controls/wpf-winforms/webview) pour les applications de bureau Windows \(Win32\) a été mis à jour avec plusieurs nouvelles fonctionnalités, notamment la possibilité d’injecter un script lors du chargement de la page avant que les autres scripts de la page soient exécutés \([AddInitializeScript](/uwp/api/windows.web.ui.interop.webviewcontrol.addinitializescript)\) et de savoir quand un WebViewControl particulier reçoit ou perd le focus \([GotFocus](/uwp/api/windows.web.ui.interop.webviewcontrol.gotfocus) / [LostFocus](/uwp/api/windows.web.ui.interop.webviewcontrol.lostfocus)\).  

En outre, vous pouvez désormais créer un contrôle WebViewControl en tant que fenêtre ouverte à partir de [window.open](https://developer.mozilla.org/docs/Web/API/Window/open).  L’événement [NewWindowRequested](/uwp/api/windows.web.ui.iwebviewcontrol.newwindowrequested) avertit toujours une application lorsque le script à l’intérieur de WebViewControl appelle window.open comme il l’a toujours fait, mais avec EdgeHTML 18, son [NewWindowRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs) inclut la possibilité de prendre un report \([GetDeferral](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs.getdeferral)\) afin de définir un nouveau Contrôle WebView \([NewWindow](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs.newwindow)\) comme cible pour la fenêtre.open :  

```csharp
WebViewControlProcess wvProc;
WebViewControl webView;

void OnWebViewControlNewWindowRequested(WebViewControl sender, WebViewControlNewWindowRequestedEventArgs args)
{

    if (args.Uri.Domain == "mydomain.com")
    {
        using deferral = args.GetDeferral();
        args.NewWindow = await wvProc.CreateWebViewControlAsync(
            parentWindow, targetWebViewBounds);
        deferral.Complete();
    }
    else
    {
        // Prevent WebView from launching in the default browser.
        args.Handled = true;
    }
}

String htmlContent = "<html><script>window.open('http://mydomain.com')</script><body></body></html>";

webView.NavigateToString(htmlContent);
```  

Enfin, les utilisateurs avec pouvoir peuvent remarquer l’apppearance de la visionneuse web d’application de bureau \(précédemment nommée Win32WebViewHost\), une application système interne représentant win32 WebView, aux endroits suivants :  

*   Dans le Centre de l’action Windows 10.  La source de ces notifications doit être comprise comme provenant d’un WebView hébergé à partir d’une application Win32.  
*   Dans l’interface utilisateur des paramètres d’accès aux appareils \( `Settings`  >  `Privacy`  >  `Camera/Location/Microphone` \).  La désactivation de l’un de ces paramètres refuse l’accès à partir de tous les WebView hébergés dans les applications Win32.  

![Paramètre d’accès à l’appareil de la visionneuse web d’application de bureau](./media/desktop-app-web-viewer.png)  

## <a name="deprecated-features"></a>Fonctionnalités dépréciées  

### <a name="xss-filter-now-retired"></a>Le filtre XSS est maintenant retiré  

Avec EdgeHTML 18, nous retireons le filtre XSS dans Microsoft Edge.  Nos clients restent protégés grâce aux normes modernes telles que la stratégie de sécurité du contenu [(CSP),](https://developer.mozilla.org/docs/Web/HTTP/CSP)qui fournissent des mécanismes plus puissants, performants et sécurisés pour se protéger contre les attaques par injection de contenu, avec une compatibilité élevée entre les navigateurs modernes.  

## <a name="new-apis-in-edgehtml-18"></a>Nouvelles API dans EdgeHTML 18  

Consultez la liste complète des nouvelles API dans EdgeHTML 18.  Ils sont répertoriés au format [nom de l’interface]. [nom de l’api].  

> [!NOTE] 
> Bien que les API suivantes soient exposées dans le DOM, le comportement de bout en bout de certaines d’entre elles est peut-être encore en développement et masqué derrière un indicateur expérimental.  Reportez-vous  [à l’état de la](https://developer.microsoft.com/microsoft-edge/platform/status/) plateforme Microsoft Edge pour le mot officiel sur la prise en charge des fonctionnalités.  

<iframe height='580' scrolling='no' title='Nouvelles API dans EdgeHTML 18' src='//codepen.io/MSEdgeDev/embed/5d7be9404d82575162b486e79d0dd58f
/?height=608&theme-id=23401&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Voir les nouvelles API stylet dans <a href='https://codepen.io/MSEdgeDev/pen/5d7be9404d82575162b486e79d0dd58f'> EdgeHTML 18 </a> par MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev ) sur </a> <a href='https://codepen.io'> CodePen </a> .</iframe>  

## <a name="previous-edgehtml-releases"></a>Versions EdgeHTML précédentes  

[EdgeHTML 13 / Windows build 10586 (11/2015)](./whats-new/edgehtml-13.md)  

[EdgeHTML 14 / Windows build 14393 (8/2016)](./whats-new/edgehtml-14.md)  

[EdgeHTML 15 / Windows build 15063 (4/2017)](./whats-new/edgehtml-15.md)  

[EdgeHTML 16 / Windows build 16299 (10/2017)](./whats-new/edgehtml-16.md)  

[EdgeHTML 17 / Windows build 17134 (04/2018)](https://aka.ms/devguide_edgehtml_17)  
