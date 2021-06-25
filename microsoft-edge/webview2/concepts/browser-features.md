---
description: Différences de fonctionnalités entre Microsoft Edge web et WebView2
title: Différences de fonctionnalités entre Microsoft Edge web et WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/23/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, WebView2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
no-loc: ["Autofill for Addresses", "Autofill for Passwords", Autofill for Payments", Browser Extensions", "Browser Task Manager", "Collections", "Continue-where-I-left-off prompt", "Downloads", "Edge Shopping", "Family Safety", "Favorites", "Hotkeys", "IE Mode" ,"Immersive Reader", "Intrusive Ads", "Read Aloud", "Smart Screen", "Translate", "Tracking Prevention", "Profile and Identity", "Web Payment API", "Windows Defender Application Guard","edge:// URLs"]  
---
# <a name="feature-differences-between-microsoft-edge-and-webview2"></a>Différences de fonctionnalités entre Microsoft Edge web et WebView2  

WebView2 est basé sur le nouveau Microsoft Edge navigateur.  Vous avez la possibilité d’étendre les fonctionnalités du navigateur aux applications WebView2, ce qui est utile.  Toutefois, étant donné que WebView2 n’est pas limité aux applications de navigateur, certaines fonctionnalités de navigateur doivent être modifiées ou supprimées.  Cet article fournit les informations suivantes.  

*   Fonctionnalités de navigateur modifiées et informations de prise en charge.   
*   Possibilité d’activer ou de désactiver la fonctionnalité.  
*   Recommandations sur les raccourcis clavier.  
    
## <a name="design-guidelines"></a>Recommandations en matière de conception  

Dans le contexte de WebView2, les fonctionnalités de navigateur respectent les instructions de conception suivantes.  

*   La plupart des fonctionnalités fonctionnent de la même manière dans WebView2 et Microsoft Edge.  Si une fonctionnalité n’est pas logique dans le contexte de WebView2 ou pour d’autres raisons, la fonctionnalité est modifiée ou désactivée. 
*   Les fonctionnalités WebView2 n’incluent pas Microsoft Edge de marque.  
    
## <a name="browser-features"></a>Fonctionnalités de navigateur  

Le tableau suivant affiche les fonctionnalités WebView2 qui diffèrent du navigateur Microsoft Edge web.   

*   **L’état** par défaut indique que la fonctionnalité fait partie de l’expérience par défaut sur une nouvelle instance WebView2.  
*   **Configurable** indique que vous pouvez activer ou désactiver la fonctionnalité à l’aide des API WebView2 ou des commutateurs de ligne de commande.  
    
> [!NOTE]  
> Cet article ne traite pas de la modification des fonctionnalités à l’aide de commutateurs de ligne de commande.  Pour plus d’informations sur l’Chromium des fonctionnalités avec les commutateurs de ligne de commande, accédez à La liste des commutateurs de ligne [de commande.][PeterExperimentsChromiumCommandLineSwitches]  
    
| Fonctionnalité | État par défaut | Configurable | Détails |  
|:--- |:--- |:--- | :--- |  
| Autofill for Addresses | Activé | Oui | Cette fonctionnalité est désactivée par défaut, vous pouvez l’activer ou la désactiver à l’aide des API de remplissage automatique WebView2.  |  
| Autofill for Passwords | Activé | Oui | Cette fonctionnalité est désactivée par défaut, vous pouvez l’activer ou la désactiver à l’aide des API de remplissage automatique WebView2.  |  
| Remplissage automatique des paiements | Désactivé | Non | Cette fonctionnalité est désactivée.  |  
| Extensions de navigateur | Désactivé | Non | Cette fonctionnalité est désactivée.  |  
| Browser Task Manager | Désactivé | Non | Cette fonctionnalité est désactivée.  |  
| Collections | Désactivé | Non | Cette fonctionnalité est désactivée.  |  
| Continue-where-I-left-off prompt | Désactivé | Non | Cette fonctionnalité est désactivée.  |  
| Downloads | Activé | Oui | WebView2 fournit une API qui vous permet de personnaliser l’interface utilisateur de téléchargement pour manipuler les téléchargements. Par exemple, vous pouvez bloquer, rediriger, enregistrer, suspendre, etc.  <!--For more information, navigate to [download API][Webview2ReferenceDownloadApi].--> |  
| Edge Shopping | Désactivé | Non | Cette fonctionnalité est désactivée.  |  
| Family Safety | Désactivé | Non | Cette fonctionnalité est désactivée.  |  
| Favorites | Désactivé | Non | Cette fonctionnalité est désactivée.  |  
| IE Mode | Désactivé | Non | Cette fonctionnalité est désactivée. WebView2 ne prend pas en charge le mode IE et présente des différences de comportement par rapport à Internet Internet (par exemple, la prise en charge de MHT ou BIN). |  
| Immersive Reader | Désactivé | Non | Cette fonctionnalité dépend de l’interface utilisateur du navigateur pour l’interaction.  Cette fonctionnalité est désactivée.  |  
| Intrusive Ads | Désactivé | Non | Cette fonctionnalité est désactivée.  |  
| Raccourcis clavier | Examiner les détails | Examiner les détails | Les raccourcis clavier qui sont désactivés par défaut n’ont pas de sens ou provoquent des problèmes dans WebView2.  Vous ne pouvez pas activer ou désactiver ces raccourcis.  Au lieu de cela, vous pouvez écouter une combinaison de touches à l’aide de l’événement `AcceleratorKeyPressed` et créer une réponse personnalisée si nécessaire.  Pour plus d’informations, accédez à [d’autres informations sur les raccourcis clavier.](#additional-keyboard-shortcuts-information) | 
| Read Aloud | Désactivé | Non | Cette fonctionnalité est désactivée.  |  
| Smart Screen | Activé`*` | Non | `*` L’interface utilisateur de cette fonctionnalité a été supprimée, mais la fonctionnalité sous-jacente est toujours disponible.  En outre, vous pouvez désactiver Smart Screen l’utilisation d’un commutateur de ligne de commande.  |  
| Translate | Désactivé | Non | Cette fonctionnalité est désactivée.  |  
| Tracking Prevention | Activé`*` | Non | `*` L’interface utilisateur de cette fonctionnalité a été supprimée, mais la fonctionnalité sous-jacente est toujours disponible.  La prévention du suivi est toujours équilibrée.|  
| Profile and Identity | Désactivé | Non | La fonctionnalité qui synchronise vos favoris, cookies, etc., est désactivée.  | 
| Windows Defender Application Guard | Désactivé | Non | Cette fonctionnalité est désactivée.  |  
| edge:// URLs | Examiner les détails | Non | Paramètres pour le navigateur Microsoft Edge sont sur `edge://` les URL.  Étant donné que la plupart de ces pages web ont une Microsoft Edge ou n’ont pas de sens dans le contexte de WebView2, certaines de ces URL sont désactivées.  Pour plus d’informations, [accédez à URL internes bloquées.](#blocked-internal-urls)  |  

## <a name="web-platform-features"></a>Fonctionnalités de plateforme web

Le tableau suivant affiche les fonctionnalités de la plateforme WebView2 actuellement indisponibles.

| Fonctionnalité | Détails |  
|:--- | :--- |  
| Push Notifications | Cette fonctionnalité n’est pas implémentée dans WebView2. |  
| Web Payment API | Cette fonctionnalité est désactivée. | 

## <a name="blocked-internal-urls"></a>URL internes bloquées  

Les pages web Microsoft Edge paramètres Google Chrome et suivantes ne sont pas disponibles dans WebView2.  

*   `chrome-search://local-ntp/local-ntp.html`  
*   `edge://application-guard-internals`  
*   `edge://apps`  
*   `edge://compat`  
*   `edge://extensions`  
*   `edge://favorites`  
*   `edge://help`  
*   `edge://management`  
*   `edge://network-error`  
*   `edge://new-tab-page`  
*   `edge://newtab`  
*   `edge://omnibox`  
*   `edge://settings`  
*   `edge://supervised-user-internals`  
*   `edge://version`  
    
## <a name="additional-keyboard-shortcuts-information"></a>Informations supplémentaires sur les raccourcis clavier  

Les raccourcis clavier ou les liaisons de touches sont pris en charge dans Microsoft Edge et WebView2. Lorsque Microsoft Edge mises à jour sont mises à jour, les liaisons de touches par défaut peuvent changer.  En outre, un raccourci clavier qui est désactivé par défaut peut s’activer si la fonctionnalité est désormais prise en charge dans WebView2. Pour éviter les modifications apportées à vos raccourcis clavier, vous pouvez définir sur , ce qui permet d’éteindre toutes les touches qui accèdent aux fonctionnalités du navigateur, tout en maintenant tous les raccourcis de déplacement et de modification de texte de base `AreBrowserAcceleratorKeysEnabled` `FALSE` allumés.  

Le tableau suivant répertorie les raccourcis qui sont toujours désactivés dans WebView2.  Un astérisque \( \) indique que le raccourci n’est pas désactivé, mais que la fonctionnalité à partir de celle-ci est désactivée ou ne s’applique pas à `*` WebView2.  

| Action | Windows |  
|:--- |:--- |  
| Ajouter à Favorites | `Ctrl`+`D` |  
| Ajouter tous les onglets à Favorites | `Ctrl`+`Shift`+`D` |  
| Emplacement du focus | `Ctrl`+`L, Alt`+`D` |  
| Coller et aller | `Ctrl`+`Shift`+`L` |  
| Ouvrir un fichier | `Ctrl`+`O` |  
| Read Aloud `*` | `Ctrl`+`Shift`+`U` |  
| Web Capture `*` | `Ctrl`+`Shift`+`S` |  
| Barre latérale `*` | `Ctrl`+`Shift`+`E` |  
| Enregistrer la page | `Ctrl`+`S` |  
| Sélectionner le dernier onglet | `Ctrl`+`9` |  
| Sélectionner l’onglet suivant | `Ctrl`+`Tab` |  
| Sélectionner l’onglet précédent | `Ctrl`+`Shift`+`Tab` |  
| Sélectionner l’onglet \(1 - 8\) | `Ctrl`+`(1-8)` |  
| Afficher Favorites la barre `*` | `Ctrl`+`Shift`+`B` |  
| Help | `F1` |  
| Volet Suivant focus `*` | `F6` |  
| Volet Précédent focus `*` | `Shift`+`F6` |  
| Navigation par caret `*` | `F7` |  
| Lecture `*` | `F9` |  
| Barre de menus Focus | `F10` |  
| Afficher le menu Identité `*` | `Ctrl`+`Shift`+`M` |  
| Browser Task Manager `*` | `Shift`+`Escape` |  
| Commentaires edge `*` | `Shift`+`Alt`+`I` |  
| Désactiver le son de l’onglet `*` | `Ctrl`+`M` |  
| Nouvelle fenêtre Incognito | `Ctrl`+`Shift`+`N` |  
| Nouvel onglet | `Ctrl`+`T` |  
| Nouvelle fenêtre | `Ctrl`+`N` |  
| Restaurer le dernier onglet fermé | `Ctrl`+`Shift`+`T` |  
| Mise au point Favorites | `Alt`+`Shift`+`B` |  
| Focus Inactive Popup | `Alt`+`Shift`+`A` |  
| Recherche de focus | `Ctrl`+`E`, `Ctrl`+`K`, `Search Key` |  
| Onglet en double | `Ctrl`+`Shift`+`K` |  
| Barre d’outils Focus `*` | `Alt`+`Shift`+`T` |  
| Accueil | `Alt`+`Home`, `Browser Home Key` |  
| Afficher le menu de l’application | `Alt`+`E, Alt`+`F` |  
| Afficher Favorites | `Ctrl`+`Shift`+`O` |  
| Afficher Downloads | `Ctrl`+`J` |  
| Afficher l’historique | `Ctrl`+`H` |  
| Afficher la barre du mode lecture `*` | `Shift`+`Alt`+`R` |  
| Afficher Collections `*` | `Ctrl`+`Shift`+`Y` |  

Les raccourcis clavier suivants sont toujours désactivés, sauf dans les fenêtres qui `NewWindowRequested` s’affichent lorsque l’événement n’est pas géré.

| Action | Windows |  
|:--- |:--- |  
| Fermer l’onglet | `Ctrl`+`W, Ctrl`+`F4` |  
| Fermer la fenêtre | `Ctrl`+`Shift`+`W` |  
| Plein écran | `F11` |  

Si vous le `AreBrowserAcceleratorKeysEnabled` `FALSE` définissez, les raccourcis clavier supplémentaires suivants sont désactivés.  

| Action | Windows |  
|:--- |:--- |  
| Stop | `Escape` |  
| Rechercher sur la page | `Ctrl`+`F` |  
| Rechercher suivant | `Ctrl`+`G` |  
| Rechercher précédent | `Ctrl`+`Shift`+`G` |  
| Imprimer | `Ctrl`+`P` |  
| Actualiser | `Ctrl`+`R`, `F5`, `Reload Key` |  
| Actualiser sans cache | `Ctrl`+`Shift`+`R`, `Ctrl`+`F5`, `Shift`+`F5`, `Ctrl`+`Refresh`, `Shift`+`Refresh` |  
| Zoom arrière | `Ctrl`+`-` |  
| Zoom avant | `Ctrl`+`+` |  
| Réinitialiser le zoom | `Ctrl`+`0` |  
| Rechercher suivant | `F3` |  
| Rechercher précédent | `Shift`+`F3` |  
| Back | `Alt`+`Left, Browser Back Key` |  
| Forward | `Alt`+`Right`, `Browser Forward Key` |  
| Imprimer | `Ctrl`+`P` |  
| Ouvrir/fermer DevTools | `Ctrl`+`Shift`+`I` |  
| Ouvrir la console DevTools | `Ctrl`+`Shift`+`J` |  
| Ouvrir DevTools Inspect | `Ctrl`+`Shift`+`C` |  

> [!Note] 
> Pour personnaliser l’une des touches individuellement, utilisez [l’événement AcceleratorKeyPressed.][DotnetApiMicrosoftWebWebview2CoreCorewebview2controllerAcceleratorkeypressedViewWebview2Dotnet1077444]  

## <a name="getting-in-touch-with-the-microsoft-edge-webview2-team"></a>Mise en contact avec l Microsoft Edge WebView2  

[!INCLUDE [contact WebView2 team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

<!--[Webview2ReferenceDownloadApi]: ./download-api.md "download API | Microsoft Docs"  -->  

[DotnetApiMicrosoftWebWebview2CoreCorewebview2controllerAcceleratorkeypressedViewWebview2Dotnet1077444]: /dotnet/api/microsoft.web.webview2.core.corewebview2controller.acceleratorkeypressed?view=webview2-dotnet-1.0.774.44&preserve-view=true "Événement CoreWebView2Controller.AcceleratorKeyPressed | Documents Microsoft"  

[DevtoolsShortcutsIndex]: ../../devtools-guide-chromium/shortcuts/index.md "Microsoft Edge Raccourcis clavier DevTools | Documents Microsoft"  

[GithubMicrosoftedgeWebview2feedbackIssues308]: https://github.com/MicrosoftEdge/WebView2Feedback/issues/308 "Ajouter la prise en charge des api de notification HTML5 (#308) | GitHub"  

[PeterExperimentsChromiumCommandLineSwitches]: https://peter.sh/experiments/chromium-command-line-switches "Liste des commutateurs Chromium ligne de commande | Peter Beverloo"  
