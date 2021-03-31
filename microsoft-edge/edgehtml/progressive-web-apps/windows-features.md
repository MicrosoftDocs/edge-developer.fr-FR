---
description: Améliorer progressivement votre PWA pour Windows avec les fonctionnalités d’application natives
title: Personnaliser votre PWA (EdgeHTML) pour Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: applications Web progressives, PWA, Edge, Windows, WinRT, UWP, EdgeHTML
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 59612d8292d4c4d4d7073b843386364d1ac55c5d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233214"
---
# Personnaliser votre PWA (EdgeHTML) pour Windows  

PWAs installé sur Windows 10 Profitez de [tous les avantages de l'][PwaIndexWindows10] utilisation des applications de [plateforme Windows universelle (UWP)][WindowsUWPGetStartedGuide] , notamment la protection de l’application Windows en mode sandbox et un accès complet aux API [Windows Runtime \(WinRT \))][UwpApiIndex] , notamment pour:  

*   Contrôle des fonctionnalités du périphérique (par exemple, caméra, micro, GPS \)  
*   Accès aux ressources utilisateur \(par exemple, calendrier, contacts, documents, musique \)  
*   Lancement/déplacement de votre application par le biais des commandes vocales Cortana  
*   Intégration du système d’exploitation Windows \(via le centre de notifications Windows, de la barre des tâches du bureau et des menus contextuels)  
    
Il ne s’agit que de quelques-unes des possibilités ajoutées pour votre PWA \(EdgeHTML \) sur Windows.  

Cet article vous explique comment installer et exécuter une application Windows 10 (EdgeHTML \) et l’améliorer, tout en garantissant la compatibilité entre navigateur et multiplateforme.  

> [!IMPORTANT]
> Les exemples et étapes de cet article nécessitent Visual Studio 2017. Visual Studio 2019 n’inclut pas le modèle utilisé dans cet article. Pour télécharger Visual Studio 2017, voir [téléchargements Visual Studio-2017, 2015 & les versions précédentes][PreviousVSDownloads] .  


## Prérequis  

*   Une application Web PWA (ou une application Web hébergée) existante, qui est un site Live ou localhost.  Ce guide utilise l’exemple de PWA dans [prise en main des applications Web progressives][PwaGetStarted].  
*   Téléchargez la [communauté 2017 Visual Studio Community][MicrosoftVisualStudio|::ref1::|].  Vous pouvez également utiliser les éditions professionnel, entreprise ou [preview][MicrosoftVisualStudioPreview] .  Dans le programme d’installation de Visual Studio, choisissez les charges de travail suivantes:  
    *   **Développement de plateforme Windows universelle**  
        
## Configuration et exécution de votre application Windows universelle  

Une application PWA \(EdgeHTML \) installée en tant qu’application Windows 10 s’exécute en même temps que le navigateur, dans une fenêtre autonome \( `WWAHost.exe` processus \).  Pour cela, il vous suffit de disposer d’un wrapper d’application léger qui contient votre application Web hébergée, que vous pouvez configurer rapidement à l’aide du modèle de projet Visual Studio `Progressive Web App (Universal Windows)` .  \(Toute la logique de votre application, y compris l’envoi de demandes d’API Windows Runtime natives, a toujours lieu dans le code de votre application Web d’origine. \)  

Configurez votre environnement de développement d’applications Windows dans Visual Studio.  

1.  Dans les paramètres Windows, activez le [mode développeur][WindowsUWPGetStartedEnable].  \(Tapez `developer mode` dans le Searchbar Windows pour le trouver. \)  
1.  Lancez Visual Studio et sélectionnez **créer un nouveau projet...**.  
1.  Choisissez **JavaScript**  >  **Windows Universal** et sélectionnez **application Web progressive (Windows universel)** dans la liste des types de projets dans Visual Studio 2017.  
1.  Sélectionnez la version par défaut de Windows 10 `Target version` \(version la plus récente) et `Minimum version` \(Build 10586 ou version ultérieure) et sélectionnez **OK**.  
    
    ![Boîte de dialogue de sélection Visual Studio pour les builds cibles de projet UWP](media/vs-target-min-version.png)  
    
    Votre nouveau projet se charge avec le concepteur package. appxmanifest ouvert.  C’est ici que vous configurez les détails de votre application, notamment l’identité du package, les dépendances du package, les fonctionnalités requises, les éléments visuels et les points d’extensibilité.  Il s’agit d’une version temporaire facilement configurable du manifeste du package d’application utilisée lors du développement de l’application.  
    Lorsque vous générez votre projet d’application, [Visual Studio génère un fichier AppxManifest.xml][UwpSchemasAppxpackageUapmanifestschemaGeneratePackageManifest] à partir de ces métadonnées, qui est utilisé pour installer et exécuter votre application.  Chaque fois que vous mettez à jour votre `package.appxmanifest` fichier, veillez à régénérer le projet afin que les deux apparaissent dans votre `AppxManifest.xml` Runtime.  
    
1.  Dans le volet de l' **application** Project Designer, entrez l’URL de votre fichier `Start page` .
    
    > [!NOTE]
    > Les travailleurs de service sont pris en charge pour toutes les URL HTTPS \(sécurisées \) spécifiées en tant que `StartPage` .  Par défaut, les travailleurs de services ne sont pas pris en charge pour les applications Web qui spécifient une page d’accueil locale.  Pour permettre la prise en charge du travailleur de service dans ces cas-là, ajoutez une entrée [ApplicationContentUriRules](#set-application-content-uri-rules-acurs) explicite au manifeste, par exemple: `<uap:Rule Match="http://web-platform.test/" Type="include" uap5:ServiceWorker="true"/>`  
    
    ![Panneau application de package. appxmanifest designer](media/vs-manifest-application.png)  
    
    Vous pouvez également modifier le `Display name` et `Description` comme vous le souhaitez.  
1.  Enregistrez ce fichier \(ou une autre image 512x512 de votre choix) sur votre ordinateur de bureau.  
    Dans le panneau **composants visuels** du concepteur de manifeste, cliquez sur le `Source` bouton champ **...** , sélectionnez-le en tant que fichier source, puis cliquez sur **générer**.  \(Puis cliquez sur **OK** pour remplacer les images d’espaces réservés par défaut).  
    
    ![Panneau de ressources visuelles de package. appxmanifest designer](media/vs-manifest-visual-assets.png)  
    
    Cela génère les ressources visuelles de base pour l’installation, l’exécution, le lancement et la distribution de votre application dans le Windows Store.  
    Si vous voyez des erreurs rouges \( `X` \) indiquant des images manquantes, vous pouvez cliquer sur les boutons **...** pour sélectionner manuellement un fichier à partir des images générées.  
1.  Dans le volet des **URI de contenu** du concepteur de manifeste, remplacez `http://example.com` par l’emplacement de votre fichier `Rule`  =  `include` . `WinRT Access`  =  `All`  
    Cela octroie à votre accès à PWA l’autorisation d’envoyer des demandes d’API Windows Runtime Windows en natif lors de l’exécution en tant qu’application Windows 10, qui est abordée plus tard.   Si votre application PWA réelle ne requiert pas l’accès WinRT, vous pouvez basculer la `WinRT Access` valeur vers `None` .  Quelle que soit la méthode utilisée, veillez à désactiver la chaîne par défaut `http://example.com` avec l’URI de votre PWA ou votre application ne peut pas être chargée correctement au moment de l’exécution.  
    Vous pouvez exécuter et déboguer votre PWA en tant qu’application Windows 10.  Si vous utilisez un site localhost pour suivre ce guide, assurez-vous qu’il est en cours d’exécution.  Puis  
1.  Créez \( `Ctrl` + `Shift` + `F5` \) et exécutez \( `F5` \) votre projet Project Web App.  Votre site Web doit maintenant être lancé dans une fenêtre d’application autonome.  Non seulement il s’agit d’une application Web hébergée; Il s’exécute en tant qu’application Web progressive installée sur Windows 10.  
    
    ![PWA exécuté dans une fenêtre de WWAHost.exe](media/wwahost.png)  
    
## Déboguer votre PWA \(EdgeHTML \) en tant qu’application Windows  

Dans la mesure où une application Web hébergée par le biais d’une application Web PWA est simplement améliorée, vous pouvez déboguer votre code côté serveur de la même manière que n’importe quelle application Web, à l’aide de votre IDE et de votre flux de travail habituels.  Les modifications que vous déployez en direct sont reflétées dans votre installation de Project Web App la prochaine fois que vous lancez l’application.

Pour le débogage côté client dans votre application Windows 10, vous devez disposer de l' `Microsoft Edge DevTools Preview` application.  Cette application autonome inclut toutes les fonctionnalités de la version d’origine du navigateur [Microsoft Edge devtools][DevToolsGuide] \(y compris les [Outils PWA][DevToolsGuideServiceWorkers]\), ainsi que la prise en charge des fonctionnalités de [débogage à distance][DevToolsProtocol01ClientsEdgePreview] de base et un [Sélecteur de cibles de débogage][DevToolsGuideMicrosoftStoreApp] pour l’attachement à une instance en cours d’exécution du moteur EdgeHTML, y compris des compléments pour Office, Cortana  

Voici la procédure à suivre pour configurer le débogage pour votre page PWA \(EdgeHTML \).  

1.  Installez l’application [Microsoft Edge devtools Preview][MicrosoftStoreEdgeDevtoolsPreview] à partir du Microsoft Store si vous ne l’avez pas encore.  
1.  Une fois le site de PWA en service opérationnel, lancez l’application DevTools.  
1.  Dans Visual Studio, lancez votre application Windows 10 avec la `Start Without Debugging` `Ctrl` + `F5` commande ().  \(L’application DevTools n’est pas correctement jointe si le débogueur Visual Studio est actif. \)  
1.  Dans l’application DevTools, cliquez sur le bouton **Actualiser** du sélecteur de cibles de débogage local.  Votre site PWA \(EdgeHTML \) doit maintenant être répertorié.  \(S’il s’exécute également dans une fenêtre de navigateur, il s’agit de la dernière instance de ce site dans la liste. \)  
1.  Cliquez sur votre annonce sur votre site Web (EdgeHTML \) pour ouvrir un nouvel onglet d’instance DevTools et démarrer le débogage.  
    
    ![Sélecteur de cibles de débogage local dans l’application Microsoft Edge DevTools](media/devtools-local.png)  
    
1.  Vous pouvez vérifier que DevTools est attaché à votre application PWA-en tant que Windows.  Dans la **console**devtools, tapez:  
    
    ```shell
    window.Windows
    ```  
    
    Cela renvoie l' `Windows Runtime` objet global contenant tous les [espaces de noms WinRT de niveau supérieur](#find-windows-runtime-winrt-apis).  Il s’agit de votre point d’entrée pour la [plateforme Windows universelle][WindowsUWPIndex]qui s’exécute sur votre ordinateur Windows 10, et n’est exposé qu’aux applications Web qui s’exécutent en tant qu’applications Windows 10 (exécutées en dehors du navigateur dans le cadre d’un `WWAHost.exe` processus).  
    
## Rechercher des API Windows Runtime (WinRT)  

Dans le cas d’une application Windows installée, votre application [PWA \(EdgeHTML \) dispose d’un accès complet aux API Windows Runtime natives][WindowsRuntime]; Déterminez ce que vous devez utiliser, obtenez les autorisations requises, puis utilisez la détection de fonctionnalités pour envoyer cette demande d’API dans les environnements pris en charge.  Parcourez ce processus pour ajouter une amélioration progressive aux utilisateurs de bureau Windows de votre ordinateur de bureau Windows.  

Il existe de nombreuses façons d’identifier les API de plateforme Windows universelle dont vous avez besoin pour votre Windows PWA, y compris la recherche dans l’ensemble des API de la plateforme Windows sur le centre de développement Windows, et le téléchargement et l’exécution d' [exemples de code UWP](#uwp-code-samples) avec Visual Studio, ainsi que les extraits de code de navigation pour les tâches courantes pour PWAS sur Windows.

Il existe de nombreuses façons d’identifier les API de plateforme Windows universelle dont vous avez besoin pour votre Windows PWA, y compris la recherche dans l’ensemble des API de la plateforme Windows sur le centre de développement Windows (UWP/API/), le téléchargement et l’exécution d' [exemples de code UWP](#uwp-code-samples) dans Visual Studio, et les extraits de code pour les tâches courantes pour [PWAS sur Windows 10 (EdgeHTML)][PwaIndexWindows10]  

Le fonctionnement global des API WinRT dans JavaScript, de la même manière que dans C#, vous pouvez suivre la [documentation de la plateforme Windows universelle][WindowsUWPIndex] et la [référence d’API][UwpApiIndex] pour l’utilisation.  Notez toutefois les différences suivantes:  

*   Les fonctionnalités WinRT dans JavaScript utilisent  [différentes conventions de casse][ScriptingJsinrtUsingWinRTCasingConventions]  
*   [Les événements sont représentés sous forme de identificateurs de chaîne][ScriptingJsinrtHandlingWinRTEvents] transmis à des `addEventListener` / `removeEventListener` méthodes de classe.  
*   Les [méthodes asynchrones][ScriptingJsinrtUsingWinRT] utilisent le modèle de promesse JavaScript  
*   Les API dans l' `Windows.UI.Xaml` espace de noms ne sont pas prises en charge pour les applications JavaScript, qui utilisent plutôt la pile de rendu Web du moteur [EdgeHTML][DevGuideWhatsNew] \(html, CSS \)  
    
Pour plus d’informations, consultez [utilisation de Windows Runtime en JavaScript][WindowRuntimeUsingJavascript].  

### Exemples de code UWP  

Consultez les exemples de code de la [plateforme Windows universelle (UWP \)][MicrosoftDeveloperWindowsSamples] référentiel samples pour parcourir les exemples JavaScript pour les scénarios d’application Windows 10 courants.  Bien que les versions JS de ces exemples utilisent la bibliothèque [WinJS][GithubWinjsWinjs] pour structurer le modèle d’exemple, WinJS n’est pas requis pour l’envoi des demandes d’API WinRT illustrées dans ces exemples.  

> [!NOTE]
> Si vous devez écouter l' [`activated`][UwpApiWindowsUiWebuiWebapplicationActivated] événement de l’application, vous pouvez le faire à l’aide de l’API WinRT Native suivante:  
> 
> **Utilisez cette**  
> 
> ```javascript
> Windows.UI.WebUI.WebUIApplication.addEventListener("activated", function (activatedEventArgs) {
>     // Check activatedEventArgs.kind and respond as needed
> });
> ```  
> 
> ... Contrairement à ce type de requête WinJS utilisée dans les exemples:  
> 
> **Non**  
> 
> ```javascript
>     var page = WinJS.UI.Pages.define("/html/scenario1-launched.html", {
>         ready: function (element, options) {
>             // Check options.activationKind and respond as needed
>         }
>     });
> ```  

## Envoyer des demandes d’API WinRT à partir de votre PWA (EdgeHTML)  

À ce stade, imaginons que vous vouliez ajouter un menu contextuel personnalisé pour les utilisateurs Windows de notre PWA \(EdgeHTML \) et avoir identifié les API dont vous avez besoin dans l’espace de noms [Windows. UI. Popup][UwpApiWindowsUiPopups] .  

Pour envoyer des demandes d’API WinRT à partir de notre PWA \(EdgeHTML \), vous devez tout d’abord [établir les autorisations requises](#set-application-content-uri-rules-acurs) (ou les règles URI de contenu de l’application \) dans le manifeste du package d’application Windows `.appxmanifest` .  

Si l’une de ces requêtes d’API implique l’accès à des ressources utilisateur telles que des images ou de la musique, ou à des fonctionnalités d’appareil comme la caméra ou le microphone, vous devez également ajouter des [déclarations de fonctionnalités d’application](#app-capability-declarations) au manifeste du package de l’application afin que Windows puisse lui demander une autorisation.  Par la suite, si vous publiez votre version d’Outlook. Outlook sur le Microsoft Store, les [autorisations d’application][MicrosoftSupportWindowsAppPermissions] requises sont également indiquées dans votre description dans le Windows Store.  

#### Définir les règles URI de contenu de l’application (règles acur)  

Par le biais des règles acur, également appelées liste des URL autorisées, vous pouvez donner aux URL de votre PWA \(EdgeHTML \) un accès direct aux API Windows Runtime.  Au niveau du système d’exploitation Windows, des limites de stratégie appropriées ont été définies pour autoriser le code hébergé sur votre serveur Web à envoyer des demandes d’API de la plateforme.  Vous définissez ces limites dans le fichier manifeste du package d’application quand vous spécifiez les URL de Project Web App `ApplicationContentUriRules` .  

Vos règles doivent inclure la page de démarrage de votre application et toutes les autres pages que vous souhaitez inclure en tant que pages de l’application.  Si votre utilisateur navigue vers une URL qui n’est pas incluse dans vos règles, Windows ouvre l’URL cible dans le navigateur Microsoft Edge plutôt que la fenêtre autonome PWA \(EdgeHTML \) `WWAHost.exe` .  Vous pouvez également exclure des URL spécifiques.  

Il existe plusieurs façons de spécifier une URL `Match` dans vos règles:  

*   Nom d’hôte exact  
*   Nom d’hôte sur la base duquel inclure ou exclure tout URI contenant un sous-domaine de ce nom d’hôte.  
*   URI exact  
*   URI exact contenant une propriété de requête  
*   Chemin d’accès partiel et caractère générique permettant d’indiquer une extension de fichier particulière pour une règle d’inclusion.  
*   Chemins d’accès relatifs pour les règles d’exclusion  
    
Voici quelques exemples de règles acur dans un `.appxmanifest` fichier:  

```xml
<Application
Id="App"
StartPage="https://contoso.com/home">
<uap:ApplicationContentUriRules>
    <uap:Rule Type="include" Match="https://contoso.com/" WindowsRuntimeAccess="all" />
    <uap:Rule Type="include" Match="https://*.contoso.com/" WindowsRuntimeAccess="all" />
    <uap:Rule Type="exclude" Match="https://contoso.com/excludethispage.aspx" />
</uap:ApplicationContentUriRules>
```  

Les URL définies dans règles acur pour votre application peuvent être accordées à Windows Runtime par le biais de l' `WindowsRuntimeAccess` attribut, qui accepte les valeurs suivantes:  

*   `all`: Le code JavaScript distant dispose d’un accès à toutes les API WinRT et composants empaquetés locaux.  L’espace de noms [Windows \(WinRT \))][UwpApiIndex] est injecté et présent dans le moteur de script.  
*   `allowForWeb`: L’accès au code JavaScript distant est limité aux composants empaquetés locaux, y compris aux composants C++/C # personnalisés.  
*   `none`Définie.  L’URL spécifiée n’a pas d’accès à la plateforme.  
    
Dans ce didacticiel, vous avez déjà défini la seule forme règles ACUR que vous avez besoin de l’étape 6 de la [configuration précédente et](#set-up-and-run-your-universal-windows-app) de l’exécution de la section \) pour votre application d’une seule page.  Vous pouvez confirmer cela dans le volet des **URI de contenu** du concepteur Visual Studio `package.appxmanifest` .  

![Panneau URI de contenu du concepteur Visual Studio appxmanifest](media/vs-appxmanifest-editor-acurs.png)  

Vous pouvez également afficher le code XML brut de votre manifeste en cliquant avec le bouton droit sur votre `package.appxmanifest` fichier dans l’Explorateur de solutions de Visual Studio et en sélectionnant **afficher le code** \( `F7` \).  Pour basculer vers le mode concepteur, sélectionnez **afficher le concepteur** \( `Shift` + `F7` \).  

#### Déclarations des fonctionnalités d’application  

Si votre application a besoin d’un accès par programme à des ressources utilisateur telles que des images ou de la musique, ou à des appareils tels qu’une caméra ou un microphone, vous devez inclure les [déclarations de fonctionnalités d’application][WindowsUwpPackagingAppCapabilities] correspondantes dans le fichier manifeste de votre package d’application.  Il existe trois catégories de déclaration de fonctionnalités d’application:  

*   Les [fonctionnalités à usage général][WindowsUwpPackagingAppCapabilitiesGeneralUse] qui s’appliquent aux scénarios d’application les plus courants.  
*   Les [fonctionnalités d’appareil][WindowsUwpPackagingAppCapabilitiesDevice] qui permettent à votre application d’accéder à des périphériques et à des dispositifs internes.  
*   [Fonctionnalités à usage spécial][WindowsUwpPackagingAppCapabilitiesSpecialRestricted] qui prennent en charge les scénarios d’entreprise et qui nécessitent un compte d’entreprise Microsoft Store.  Pour plus d’informations sur les comptes d’entreprise, voir [Types de compte, emplacements et frais][WindowsUwpPublishAccountTypesLocationsFees].
    
La page de votre application Microsoft Store répertorie toutes les fonctions que vous déclarez dans le manifeste de votre package d’application, vous devez donc spécifier uniquement les fonctionnalités utilisées réellement par votre application.

Certaines fonctionnalités permettent aux applications d’accéder à des ressources sensibles.  Ces ressources sont considérées comme «sensibles», car chacune peut accéder aux données personnelles de l’utilisateur ou coûter l’argent à l’utilisateur.  Paramètres de confidentialité, gérés par l’application [paramètres][BingResultsWindows10Settings] Windows 10, permet à l’utilisateur de contrôler de façon dynamique l’accès aux ressources sensibles.  Par conséquent, il est important que votre application ne présume pas qu’une ressource sensible est toujours disponible.  Pour plus d’informations sur l’accès aux ressources sensibles, voir [Recommandations en matière d’applications prenant en charge la confidentialité][WindowsUwpSecurityIndex].  

Vous pouvez demander l’accès en déclarant les fonctionnalités dans le manifeste du package de votre application.  Dans Visual Studio, vous pouvez effectuer cette opération à partir du volet **capacités** du concepteur package. appxmanifest.  

![Panneau capacités du concepteur Visual Studio appxmanifest](media/vs-appxmanifest-editor-capabilities.png)  

Dans ce didacticiel, seule la fonctionnalité Internet (client) par défaut est requise, donc aucune action supplémentaire n’est requise.  

### Utiliser la détection de fonctionnalités pour appeler WinRT  

Pour garantir une connaissance de base de qualité pour votre public sur toutes les plateformes, vous améliorez progressivement votre utilisation de Project Web App à l’aide de la fonctionnalité de détection des fonctionnalités WinRT.  De cette façon, vous pouvez être sûr que votre code spécifique à Windows s’exécute uniquement dans un contexte où les API WinRT sont disponibles et applicables.  

Pour détecter les fonctionnalités, il est possible de rechercher en tant qu' `Windows` objet \(le point d’entrée vers l' [espace de noms WinRT][UwpApiIndex]\) comme suit:  

```javascript
if(window.Windows){
    /*Run code that sends Windows API requests */
}
```  

Toutefois, étant donné que toutes les API Windows ne sont pas disponibles sur tous les [types d’appareils Windows 10][UwpExtensionSdkDeviceFamiliesOverview], il est généralement utile d’utiliser une détection de fonctionnalités plus spécifique pour qualifier davantage l’espace de noms de la requête d’API que vous envoyez:  

```javascript
if(window.Windows && Windows.Media.SpeechRecognition){
    /*Run code that sends Windows API requests */
}
```  

Avec cet arrière-plan, vous pouvez ajouter du code WinRT pour implémenter un menu contextuel personnalisé.  Si vous utilisez l’exemple de Project Web App à partir de [prise en main des applications Web progressives][PwaGetStarted]:

1.  Ouvrez Visual Studio pour votre projet de site Project Web App.  
1.  Dans l’Explorateur de solutions, ouvrez le `views\layout.pug` fichier et ajoutez la ligne suivante, juste en dessous de la `script` référence de votre travailleur de service:
    
    ```xml
    script(src='/javascripts/site.js')
    ```  
    
1.  Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le `javascripts` dossier et **Ajoutez**  >  **nouveau fichier...**.
1.  Nommez votre fichier `site.js` , puis copiez-le dans le code suivant:
    
    ```javascript
    if (window.Windows && Windows.UI.Popups) {
        document.addEventListener('contextmenu', function (e) {

            // Build the context menu
            var menu = new Windows.UI.Popups.PopupMenu();
            menu.commands.append(new Windows.UI.Popups.UICommand("Option 1", null, 1));
            menu.commands.append(new Windows.UI.Popups.UICommandSeparator);
            menu.commands.append(new Windows.UI.Popups.UICommand("Option 2", null, 2));

            // Convert from webpage to WinRT coordinates
            function pageToWinRT(pageX, pageY) {
                var zoomFactor = document.documentElement.msContentZoomFactor;
                return {
                    x: (pageX - window.pageXOffset) * zoomFactor,
                    y: (pageY - window.pageYOffset) * zoomFactor
                };
            }

            // When the menu is invoked, execute the requested command
            menu.showAsync(pageToWinRT(e.pageX, e.pageY)).done(function (invokedCommand) {
                if (invokedCommand !== null) {
                    switch (invokedCommand.id) {
                        case 1:
                            console.log('Option 1 selected');
                            // Invoke code for option 1
                            break;
                        case 2:
                            console.log('Option 2 selected');
                            // Invoke code for option 2
                            break;
                        default:
                            break;
                    }
                } else {
                    // The command is null if no command was invoked.
                    console.log("Context menu dismissed");
                }
            });
        }, false);
    }
    ```
    
1.  Comparez le comportement du menu contextuel lors de l’exécution de votre PWA dans le navigateur \( `F5` à partir du projet de site PWA \) plutôt que dans la fenêtre de l’application Windows ( `F5` à partir de votre projet d’application Windows universelle \).  Dans le navigateur, le fait de cliquer avec le bouton droit vous permet d’accéder au menu contextuel de Microsoft Edge par défaut, alors que dans le `WWAHost.exe` processus, votre menu personnalisé apparaît désormais.  
    
    | MicrosoftEdge | Application Windows 10 |  
    |:--- |:---- |  
    | ![Menu contextuel par défaut du navigateur](media/browser-context-menu.png) | ![Menu contextuel personnalisé de l’application](media/app-context-menu.png) |  
    
J’espère que vous avez à présent une base solide pour améliorer votre PWAs sur Windows.  Si vous rencontrez des questions ou quelque chose n’est pas clair, envoyez-nous un commentaire!  

## Aller plus loin

Le [Centre de développement Windows][MicrosoftDeveloperWindowsApps] est votre référence complète pour toutes les phases du bâtiment d’applications Windows, de la [mise][MicrosoftDeveloperWindowsAppsGetStarted]en route à la [conception][MicrosoftDeveloperWindowsAppsDesign], du [développement][MicrosoftDeveloperWindowsAppsDevelop]et de la [publication][MicrosoftDeveloperStorePublishApps] sur le Microsoft Store.  

Pour obtenir une vue d’ensemble générale de la plateforme Windows universelle (UWP) et de la manière de cibler différentes familles d’appareils Windows 10, voir [Présentation de la plateforme Windows universelle][WindowsUWPGetStartedGuide].  

Lorsque vous êtes prêt, voici comment \(et pourquoi! \) pour [transmettre votre document PWA au Microsoft Store](./microsoft-store.md).  

<!-- links -->  

[PwaGetStarted]: ./get-started.md "Découvrir les applications Web progressives | Documents Microsoft"  
[PwaIndexWindows10]: ./index.md#pwas-on-windows-10-edgehtml "PWAs sur Windows 10 (EdgeHTML)-applications Web progressives sur Windows | Documents Microsoft"  
[DevToolsGuide]: ../devtools-guide/index.md "Outils de développement Microsoft Edge (EdgeHTML) | Documents Microsoft"  
[DevToolsGuideMicrosoftStoreApp]: ../devtools-guide/index.md#microsoft-store-app "Application Microsoft Store App-Microsoft Edge (EdgeHTML)-outils de développement | Documents Microsoft"  
[DevToolsGuideServiceWorkers]: ../devtools-guide/service-workers.md "Travailleurs de service | Documents Microsoft"  
[DevToolsProtocol01ClientsEdgePreview]: ../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Microsoft Edge DevTools Preview-clients de protocoles DevTools | Documents Microsoft"  
[DevGuideWhatsNew]: ../dev-guide/whats-new.md "Nouveautés de EdgeHTML | Documents Microsoft"  
[WindowsRuntime]: ../windows-runtime/index.md "Windows Runtime (WinRT) pour JavaScript | Documents Microsoft"  
[WindowRuntimeUsingJavascript]: ../windows-runtime/using-the-windows-runtime-in-javascript.md "Utilisation de Windows Runtime en JavaScript | Documents Microsoft"  

[ScriptingJsinrtHandlingWinRTEvents]: /scripting/jswinrt/handling-windows-runtime-events-in-javascript "Gestion des événements Windows Runtime en JavaScript | Documents Microsoft"  
[ScriptingJsinrtUsingWinRT]: /scripting/jswinrt/using-windows-runtime-asynchronous-methods "Utilisation de méthodes asynchrones Windows Runtime | Documents Microsoft"  
[ScriptingJsinrtUsingWinRTCasingConventions]:  /scripting/jswinrt/using-the-windows-runtime-in-javascript#casing-conventions-with-windows-runtime-features "Conventions de casse avec les fonctionnalités Windows Runtime-utilisation de Windows Runtime en JavaScript | Documents Microsoft"  
[UwpApiIndex]: /uwp/api/index "Espaces de noms UWP Windows | Documents Microsoft"  
[UwpApiWindowsUiPopups]: /uwp/api/windows.ui.popups "Espace de noms Windows. UI. Popup Documents Microsoft"  
[UwpApiWindowsUiWebuiWebapplicationActivated]: /uwp/api/windows.ui.webui.webuiapplication.activated "Événement WebUIApplication. Activated | Documents Microsoft"  
[UwpExtensionSdkDeviceFamiliesOverview]: /uwp/extension-sdks/device-families-overview "Présentation de la famille d’appareils | Documents Microsoft"  
[UwpSchemasAppxpackageUapmanifestschemaGeneratePackageManifest]: /uwp/schemas/appxpackage/uapmanifestschema/generate-package-manifest "Comment Visual Studio génère-il le manifeste du package de l’application | Documents Microsoft"  
[WindowsUWPIndex]: /windows/uwp/index "Documentation de la plateforme Windows universelle | Documents Microsoft"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide "Qu’est-ce qu’une application de plateforme Windows universelle (UWP)? Documents Microsoft"  
[WindowsUWPGetStartedEnable]: /windows/uwp/get-started/enable-your-device-for-development "Activer votre appareil pour le développement | Documents Microsoft"  
[WindowsUwpSecurityIndex]: /windows/uwp/security/index "Sécurité | Documents Microsoft"  
[WindowsUwpPublishAccountTypesLocationsFees]: /windows/uwp/publish/account-types-locations-and-fees "Types de compte, emplacements et frais | Documents Microsoft"  
[WindowsUwpPackagingAppCapabilitiesSpecialRestricted]: /windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities "Fonctionnalités restreintes | Documents Microsoft"  
[WindowsUwpPackagingAppCapabilitiesDevice]: /windows/uwp/packaging/app-capability-declarations#device-capabilities "Fonctionnalités de l’appareil | Documents Microsoft"  
[WindowsUwpPackagingAppCapabilitiesGeneralUse]: /windows/uwp/packaging/app-capability-declarations#general-use-capabilities "Fonctionnalités à usage général | Documents Microsoft"  
[WindowsUwpPackagingAppCapabilities]: /windows/uwp/packaging/app-capability-declarations "Déclarations des fonctionnalités d’application | Documents Microsoft"  

[BingResultsWindows10Settings]: https://binged.it/2lOGSH0 "paramètres Windows 10-Bing"  
[GithubWinjsWinjs]: https://github.com/winjs/winjs "winjs/winjs | GitHub"  
[MicrosoftDeveloperStorePublishApps]: https://developer.microsoft.com/store/publish-apps/index "Publier des applications et des jeux Windows"  
[MicrosoftDeveloperWindowsApps]: https://developer.microsoft.com/windows/apps/index "Documentation de la plateforme Windows universelle"  
[MicrosoftDeveloperWindowsAppsDesign]: https://developer.microsoft.com/windows/apps/design/index "Concevoir et coder des applications Windows"  
[MicrosoftDeveloperWindowsAppsDevelop]: https://developer.microsoft.com/windows/apps/develop/index "Développer des applications UWP"  
[MicrosoftDeveloperWindowsAppsGetStarted]: https://developer.microsoft.com/windows/apps/getstarted/index "Découvrir les applications Windows 10"  
[MicrosoftDeveloperWindowsSamples]: https://developer.microsoft.com/windows/samples "Exemples de code"  
[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Microsoft Edge DevTools preview"  
[MicrosoftSupportWindowsAppPermissions]: https://support.microsoft.com/help/10557/windows-10-app-permissions "Autorisations des applications"  
[MicrosoftVisualStudioDownloads]: https://visualstudio.microsoft.com/downloads "Téléchargements"  
[MicrosoftVisualStudioPreview]: https://visualstudio.microsoft.com/vs/preview "Visual Studio preview"  
[PreviousVSDownloads]: https://visualstudio.microsoft.com/vs/older-downloads/ "Téléchargements Visual Studio"  
