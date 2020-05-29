---
title: Nouveautés de EdgeHTML 18
description: Ce guide fournit une vue d’ensemble des normes et fonctionnalités de développement incluses dans Microsoft Edge.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/06/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: edgehtml
keywords: Edge, développement Web, html, CSS, JavaScript, développeur, devtools
ms.custom: RS5
ms.openlocfilehash: b9285be7169f197a687e9f754a20cf67bbde160d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10564706"
---
# Guide du développeur de Microsoft Edge

> [!TIP]
> Nous nous sommes [associés à d'](https://blogs.windows.com/msedgedev/2017/10/18/documenting-web-together-mdn-web-docs/) autres navigateurs et à la communauté Web dans le cadre de l’adoption de [documents Web MDN](https://developer.mozilla.org/) comme endroit définitif dans le cadre de la mise en place d’une documentation indépendante du navigateur pour les technologies Web actuelles et émergeantes. Vous trouverez des informations détaillées sur la prise en charge de l’API EdgeHTML directement dans chaque page de la [bibliothèque de références Web MDN](https://developer.mozilla.org/docs/Web). Pour obtenir les dernières fonctionnalités prises en charge dans Microsoft Edge, consultez l’état de la [plateforme](https://developer.microsoft.com/microsoft-edge/platform/status/?q=edge%3AShipped%20edge%3APrefixed%20edge%3A'Preview%20Release) de Microsoft Edge. 


## Nouveautés de EdgeHTML 18

EdgeHTML 18 inclut les nouvelles fonctionnalités et mises à jour suivantes, fournies dans la version actuelle de la plateforme Microsoft Edge, telle que la [mise à jour de Windows 10 d’octobre 2018](/windows/uwp/whats-new/windows-10-build-17763) (10/2018, Build 17763). Pour plus d’informations sur les builds d’aperçu [Windows Insider](https://insider.windows.com/) spécifiques, voir le Guide de [Microsoft Edge changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog/) et [les nouveautés dans EdgeHTML](./dev-guide/whats-new.md).

Vous trouverez ci-dessous le lien permanent pour la liste des modifications suivante: [https://aka.ms/devguide_edgehtml_18](https://aka.ms/devguide_edgehtml_18) .

## Fonctionnalités nouvelles et mises à jour

### Stratégies de lecture automatique

Avec la mise à jour 2018 de Windows 10 d’octobre, Microsoft Edge fournit aux utilisateurs la possibilité de personnaliser leurs préférences de navigation sur les sites Web avec le son par lecture automatique pour réduire les distractions sur le Web et économiser la bande passante. Les utilisateurs peuvent personnaliser le comportement multimédia avec les contrôles de lecture automatique globaux et par site. Par ailleurs, Microsoft Edge supprime automatiquement la lecture automatique de contenus multimédias dans les onglets d’arrière-plan.

Pour plus d’informations sur l’utilisation du contenu multimédia hébergé sur votre site, consultez le guide [stratégies de lecture automatique](./dev-guide/browser-features/autoplay-policies.md) .

### Améliorations apportées à chakra

EdgeHTML 18 inclut les mises à jour du moteur JavaScript chakra pour prendre en charge les nouvelles fonctionnalités ES et WASM en plus des améliorations apportées aux performances et à l’interopérabilité. Pour plus d’informations, consultez les [notes de publication de ChakraCore 1,11](https://github.com/Microsoft/ChakraCore/wiki/Roadmap#chakracore-111) .

### Mises à jour de CSS

Nous avons effectué de nouvelles opérations *sur l’implémentation* de [masquage de feuilles de style en cascade (CSS](https://developer.mozilla.org/docs/Web/CSS/CSS_Masking) ) pour une prise en charge supplémentaire de Mask [-composite](https://developer.mozilla.org/docs/Web/CSS/mask-composite), de la [position de masque](https://developer.mozilla.org/docs/Web/CSS/mask-position)et de [Mask-REPEAT](https://developer.mozilla.org/docs/Web/CSS/mask-repeat). Pour la compatibilité des sites, Microsoft Edge prend également en charge les suivantes: *WebKit-* Properties:-WebKit-Mask,-WebKit-Mask-composite,-WebKit-Mask-image,-WebKit-Mask-position,-WebKit-Mask-position-x,-WebKit-Mask-position-y

Par ailleurs, Microsoft Edge prend désormais en charge [le renvoi à la ligne de dépassement de capacité et la](https://developer.mozilla.org/docs/Web/CSS/overflow-wrap
) prise en charge partielle du [comportement de dédéfilement](https://developer.mozilla.org/docs/Web/CSS/overscroll-behavior) ( `auto` et des `contain` valeurs).


### Outils de développement

La dernière mise à jour de Microsoft Edge DevTools ajoute un certain nombre de commodités à l’interface utilisateur et au capot, y compris aux nouveaux panneaux dédiés pour les travailleurs de services et le stockage, les outils de recherche de fichiers source dans le débogueur et les API de console et de débogage de type DevTools.

[Devtools la dernière mise à jour de Windows 10 (EdgeHTML 18)](./devtools-guide/whats-new.md) contient tous les détails.

### Écouter vos commentaires

Nous écoutons vos commentaires et avons implémenté la prise en charge de plusieurs API demandées dans EdgeHTML 18, y compris la [`DataTransfer.setDragImage()`](https://developer.mozilla.org/docs/Web/API/DataTransfer/setDragImage) méthode utilisée pour définir une image personnalisée lors du glisser-déplacer, ainsi [`secureConnectionStart`](https://developer.mozilla.org/docs/Web/API/PerformanceResourceTiming/secureConnectionStart) qu’une propriété de l’API de timing des ressources de performance, qui peut être utilisée pour renvoyer une estampille immédiatement avant que le navigateur démarre le processus de transfert pour sécuriser la connexion actuelle. 

Par ailleurs, personne ne doit énumérer la collection Attributes; nous avons donc ajouté une prise en charge pour [`Element.getAttributeNames`](https://developer.mozilla.org/docs/Web/API/Element/getAttributeNames) renvoyer les noms d’attribut de l’élément sous la forme d’un tableau de chaînes, ainsi que le [`Element.toggleAttribute`](https://developer.mozilla.org/docs/Web/API/Element/toggleAttribute) basculement d’un attribut booléen (en supprimant s’il est présent et en l’ajoutant si ce n’est pas le cas).

### Applications web progressives

#### Script d’arrière-plan Lifetime

Les applications JavaScript Windows 10 (applications Web exécutées dans un processus *WWAHost. exe* ) prennent désormais en charge un script en arrière-plan facultatif pour chaque application qui démarre avant que les vues soient activées et s’exécutent pendant la durée du processus. Cela vous permet de surveiller et de modifier des navigations, d’effectuer le suivi de l’État sur les différentes navigations, de surveiller les erreurs de navigation et d’exécuter du code avant l’activation des vues. 

Lorsque ce paramètre est spécifié en tant que [`StartPage`](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) dans le manifeste de votre [application](/uwp/schemas/appxpackage/appx-package-manifest), chacune des vues de l’application (Windows) est exposée au script en tant qu’instances de la nouvelle [`WebUIView`](/uwp/api/windows.ui.webui.webuiview) classe, en fournissant les mêmes événements, propriétés et méthodes qu’une [WebView](/uwp/api/windows.web.ui.iwebviewcontrol)générale (Win32). Votre script peut écouter l' [`NewWebUIViewCreated`](/uwp/api/windows.ui.webui.newwebuiviewcreatedeventargs) événement pour intercepter le contrôle de la navigation pour une nouvelle vue:

```JavaScript
Windows.UI.WebUI.WebUIApplication.addEventListener("newwebuiviewcreated", newWebUIViewCreatedEventHandler);
```

 Toute activation d’une application avec le script en arrière-plan telle que la fonction `StartPage` s’appuiera sur le script proprement dit pour la navigation.

#### Mise à l’échelle du texte

La mise à jour 2018 de Windows 10 octobre présente le paramètre [*augmenter la taille du texte*](https://review.docs.microsoft.com/windows/uwp/design/input/text-scaling?branch=master#user-experience) pour améliorer l’accessibilité des utilisateurs finaux, et PWAS est installé sur Windows (en plus de la plateforme UWP et de la plupart des applications de bureau). Pour les contrôles PWAs et WebView, l’échelle du texte fonctionne de la même façon que la mise à l’échelle PPP. Si un utilisateur modifie à la fois l’échelle de texte et la mise à l’échelle PPP, le résultat est le produit des deux.

 Pour obtenir des conseils sur la conception, voir le guide UWP de [mise à l’échelle du texte](/windows/uwp/design/input/text-scaling) dans le *Centre de développement Windows*.

### Mises à jour des travailleurs de services 

Pour obtenir la liste des travailleurs de services et leur fonctionnement, consultez le résumé de l' [API du travailleur de service]( https://developer.mozilla.org/docs/Web/API/Service_Worker_API) rédigé par nos partenaires sur MDN.  Plusieurs mises à jour apportées au service de support technique Microsoft Edge sont apportées à EdgeHTML 18. Le `fetchEvent` travailleur de service peut utiliser pour promettre [`preloadResponse`]( https://developer.mozilla.org/docs/Web/API/FetchEvent) une réponse et [`resultingClientId`]( https://developer.mozilla.org/docs/Web/API/FetchEvent/clientId) retourner l’ID du client que le travailleur de service actuel contrôle.  
L' [`NavigationPreloadManager`]( https://developer.mozilla.org/docs/Web/API/NavigationPreloadManager) interface fournit des méthodes pour gérer le préchargement des ressources, ce qui vous permet de faire une demande en parallèle pendant le démarrage d’un travailleur de service, ce qui évite tout délai. Consultez les [propriétés d’API récemment prises en charge](#new-apis-in-edgehtml-18) pour la liste des méthodes et propriétés de préchargement des travailleurs de service. 

### Authentification Web

Microsoft Edge prend désormais [en charge la prise en charge du préfixe de la nouvelle API d’authentification Web](https://blogs.windows.com/msedgedev/2018/07/30/introducing-web-authentication-microsoft-edge/) (c’est-à-dire [webauthn](https://w3c.github.io/webauthn/)). L’authentification Web fournit une solution ouverte, évolutive et interopérable pour simplifier l’authentification, afin d’offrir de meilleures expériences utilisateur sécurisées en remplaçant les mots de passe par des informations d’identification matérielles plus puissantes. L’implémentation de Microsoft Edge permet d’utiliser [Windows Hello](https://www.microsoft.com/windows/windows-hello) permettant aux utilisateurs de se connecter à leur visage, à leur empreinte digitale ou à leur code confidentiel, en plus des [authentificateurs externes](https://fidoalliance.org) tels que les clés de sécurité FIDO2 ou les clés de sécurité d’une U2F, pour s’authentifier en toute sécurité sur les sites Web.

Pour en savoir plus, voir le billet de blog [Présentation de l’authentification Web dans Microsoft Edge](https://blogs.windows.com/msedgedev/2018/07/30/introducing-web-authentication-microsoft-edge).

### WebDriver

Le WebDriver est désormais une [fonctionnalité Windows à la demande](https://docs.microsoft.com/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) (DOM) qui vous permet d’automatiser les tests dans Microsoft Edge et de télécharger la version appropriée pour votre appareil. Vous ne devez plus faire correspondre manuellement le Build/la branche/la saveur lors de l’installation du WebDriver, votre [WebDriver](https://www.w3.org/TR/webdriver) sera automatiquement mis à jour pour correspondre aux nouvelles mises à jour de Windows 10. 

Vous pouvez installer WebDriver en activant le mode développeur ou son installation autonome en accédant à paramètres > applications > applications & fonctionnalités > gérer les fonctionnalités facultatives. Pour plus d’informations, consultez le [site Web du blog Windows](https://blogs.windows.com/msedgedev/2018/06/14/webdriver-w3c-recommendation-feature-on-demand).

### Propriétés de notification Web
Quatre nouvelles propriétés sont désormais prises en charge pour les notifications sur le Web:,,, [`actions`](https://developer.mozilla.org/docs/Web/API/notification/actions) [`badge`](https://developer.mozilla.org/docs/Web/API/notification/badge) [`image`](https://developer.mozilla.org/docs/Web/API/notification/image) et `maxActions` améliorent la possibilité de créer des notifications sur le Web compatibles avec les systèmes de notification existants, tout en restant indépendante de la plateforme.

### WebView

#### Travailleurs de service
Les [travailleurs de service](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) sont désormais pris en charge dans le contrôle WebView, en plus du navigateur Microsoft Edge et des applications JavaScript Windows 10. Toutes les versions du WebView de Microsoft Edge ([PWA](/microsoft-edge/hosting/webview), [UWP](/uwp/api/Windows.UI.Xaml.Controls.WebView), [Win32](/windows/communitytoolkit/controls/wpf-winforms/webview)) prennent en charge les travailleurs de service, mais sachez que l' [API de transmission](https://developer.mozilla.org/docs/Web/API/Push_API) n’est pas encore disponible pour les versions UWP et Win32.

les architectures d’applications x64 requièrent des packages de type *neutre* (n’importe quel processeur) ou *x64* , car les travailleurs de services ne sont pas pris en charge dans les processus WOW64. (Pour économiser de l’espace disque, la version de WoW des dll requises n’est pas fournie en natif dans Windows.)

#### Mises à jour de WebView Win32

Les applications EdgeHTML [WebViewControl](/windows/communitytoolkit/controls/wpf-winforms/webview) pour Windows Desktop (Win32) ont été mises à jour à l’aide de plusieurs nouvelles fonctionnalités, notamment la possibilité d’injecter le script lors du chargement de la page avant que tous les autres scripts de la page soient exécutés ( [`AddInitializeScript`](/uwp/api/windows.web.ui.interop.webviewcontrol.addinitializescript) ) et savoir quand un WebViewControl particulier reçoit ou perd le focus ( [`GotFocus`](/uwp/api/windows.web.ui.interop.webviewcontrol.gotfocus) / [`LostFocus`](/uwp/api/windows.web.ui.interop.webviewcontrol.lostfocus) ).

Par ailleurs, vous pouvez désormais créer un WebViewControl comme fenêtre ouverte [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) . L' [`NewWindowRequested`](/uwp/api/windows.web.ui.iwebviewcontrol.newwindowrequested) événement notifie quand même une application lorsque le script est dans la fenêtre d’appels WebViewControl. l’ouverture telle qu’elle n’a pas encore été exécutée, mais avec EdgeHTML 18, il s' [`NewWindowRequestedEventArgs`](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs) agit de la possibilité d’effectuer un report ( [`GetDeferral`](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs.getdeferral) ) pour définir une nouvelle WebViewControl ( [`NewWindow`](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs.newwindow) ) en tant que cible de la fenêtre.

```C#
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

Enfin, les utilisateurs de Power peuvent remarquer que le apppearance de l' *application de bureau Web App* (appelé auparavant *Win32WebViewHost*), une application système interne qui représente le WebView Win32, dans les emplacements suivants:
- Dans le *Centre de notifications Windows 10*. La source de ces notifications doit être comprise dans un WebView hébergé par une application Win32.
- Dans l’interface utilisateur des paramètres d’accès aux appareils (*paramètres->confidentialité->caméra/emplacement/micro*). La désactivation de l’un de ces paramètres interdit l’accès à partir de tous les WebView hébergés dans des applications Win32.

![Paramètres d’accès aux appareils dans la visionneuse Web des applications de bureau](./dev-guide/media/desktop-app-web-viewer.png)


## Fonctionnalités déconseillées

### Filtre XSS désormais supprimé

Avec EdgeHTML 18, nous retirons le filtre XSS dans Microsoft Edge. Nos clients restent protégés grâce aux normes modernes telles que la [stratégie de sécurité du contenu (CSP)](https://developer.mozilla.org/docs/Web/HTTP/CSP), qui fournissent des mécanismes plus puissants, performants et sécurisés pour se protéger contre les attaques par injection de contenu, grâce à une compatibilité élevée entre les navigateurs modernes.

## Nouvelles API dans EdgeHTML 18

Consultez la liste complète des nouvelles API dans EdgeHTML 18. Ils sont répertoriés au format [nom de l’interface]. [nom de l’API].

> [!NOTE] 
> Bien que les API suivantes soient exposées dans le DOM, le comportement de bout en bout de certains peut toujours être en développement et masqué derrière un indicateur expérimental. Reportez-vous à la rubrique [État de plateforme Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/status/) pour le mot officiel sur la prise en charge des fonctionnalités.

<iframe height='580' scrolling='no' title='Nouvelles API dans EdgeHTML 18' src='//codepen.io/MSEdgeDev/embed/5d7be9404d82575162b486e79d0dd58f
/?height=608&theme-id=23401&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Voir le stylet <a href='https://codepen.io/MSEdgeDev/pen/5d7be9404d82575162b486e79d0dd58f'> nouvelles API dans EdgeHTML 18 </a> MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) sur <a href='https://codepen.io'> CodePen </a> .</iframe>

## Versions précédentes de EdgeHTML

[EdgeHTML 13/Windows Build 10586 (11/2015)](https://aka.ms/devguide_edgehtml_13)

[EdgeHTML 14/Windows Build 14393 (8/2016)](https://aka.ms/devguide_edgehtml_14)

[EdgeHTML 15/Windows Build 15063 (4/2017)](https://aka.ms/devguide_edgehtml_15)

[EdgeHTML 16/Windows Build 16299 (10/2017)](https://aka.ms/devguide_edgehtml_16)

[EdgeHTML 17/Windows Build 17134 (04/2018)](https://aka.ms/devguide_edgehtml_17)
