---
description: Dernières fonctionnalités expérimentales de Microsoft Edge pour les applications web
title: Fonctionnalités expérimentales | Applications web progressives
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, expérimentation, applications web progressives, applications web, PWA
ms.openlocfilehash: 587797bc8577f1c1aaca42394eecb997d21e9955
ms.sourcegitcommit: f605e4e27fed88aca286f2ae236e27f9a396b517
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "11474961"
---
# <a name="experimental-features-in-progressive-web-apps-pwas"></a>Fonctionnalités expérimentales dans les applications web progressives (P.A.S.)  

Microsoft Edge permet d’accéder aux fonctionnalités expérimentales qui sont toujours en développement.  Pour déterminer si chaque fonctionnalité est prête et quand publier chacune d’elles, testez [et fournissez des commentaires.](#providing-feedback-on-experimental-features)  

Les fonctionnalités expérimentales sont disponibles dans tous les canaux de Microsoft Edge, mais les dernières fonctionnalités expérimentales sont disponibles uniquement dans le canal Canary de Microsoft Edge.  

## <a name="turn-on-experimental-features"></a>Activer les fonctionnalités expérimentales  

Pour activer \(ou désactiver\) les fonctionnalités expérimentales dans Microsoft Edge, complétez les étapes suivantes.  
  
1.  Ouvrez MicrosoftEdge.   
    
    > [!NOTE]
    > Veillez à utiliser une version de Microsoft Edge dont l’expérience est répertoriée dans cet article.  Accédez aux [fonctionnalités expérimentales.](#features-that-are-available-to-test)  
    
1.  Accédez `edge://flags` à .  
1.  Accédez à l’expérience pertinente.  
1.  Choisissez le menu déroulant en face de la description de l’expérience et choisissez `Enabled` .  
    
    :::image type="complex" source="../media/turn-on-experimental-flag.png" alt-text="Choose Enabled to turn on an experiment" lightbox="../media/turn-on-experimental-flag.png":::
       Choose **Enabled** to turn on an experiment  
    :::image-end:::  
    
    > [!NOTE]
    > Chaque expérience possède généralement un menu déroulant pour choisir les valeurs suivantes.  Si une fonctionnalité expérimentale ne dispose pas d’une entrée dans **Expériences,** des instructions sont fournies pour démarrer Microsoft Edge avec cette fonctionnalité à l’aide de la ligne de commande.
    > 
    > *   `Default`  
    > *   `Disabled`  
    > *   `Enabled`  
    
1.  Redémarrez MicrosoftEdge.  
    
### <a name="origin-trials"></a>Versions d’évaluation d’origine  

Microsoft Edge utilise parfois des essais d’origine pour tester des fonctionnalités pour des domaines ou des sites web spécifiques.  Vous pouvez utiliser une version d’essai d’origine pour votre site web afin d’appliquer une fonctionnalité spécifique.  Si vous êtes propriétaire d’un site web, vous pouvez vous inscrire à une version d’essai d’origine.  Une version d’essai d’origine fournit des fonctionnalités à un pourcentage d’utilisateurs de Microsoft Edge qui visitent votre site web.

Pour plus d’informations sur les essais d’origine, accédez à la console du développeur des essais [d’origine De Microsoft Edge.][MicrosoftDeveloperMicrosoftEdgeOriginTrials]  
    
> [!NOTE]
> Les fonctionnalités expérimentales sont constamment mises à jour et peuvent entraîner des problèmes de performances.  Pour désactiver une fonctionnalité expérimentale, accédez à Activer [les](#turn-on-experimental-features)fonctionnalités expérimentales, accédez à l’expérience, puis choisissez `Disabled` .  

## <a name="features-that-are-available-to-test"></a>Fonctionnalités disponibles pour le test  

La liste suivante décrit les nouvelles fonctionnalités expérimentales d’application web disponibles pour le test et la validation sur Microsoft Edge.  

| Fonctionnalité | Version de Microsoft Edge | Plateforme |  
|:--- |:--- |:--- |  
| [Gestion du protocole URI](#uri-protocol-handling) | 91 ou ultérieure | Windows |    
| [Gestion des liens d’URL](#url-link-handling) | 91 ou ultérieure | Windows|  
| [Exécuter sur la connexion au système d’exploitation](#run-on-os-login) | 88 ou ultérieure | Tous |  
| [Raccourcis](#shortcuts) | 87 ou ultérieure | Tous |  
| [Gestion des fichiers](#file-handling) | 83 ou ultérieure | Tous les ordinateurs de bureau |  


## <a name="uri-protocol-handling"></a>Gestion du protocole URI  

Un identificateur de ressource uniforme \(URI\) peut être utilisé pour définir plus que des liens vers des pages web et du contenu web à l’aide du protocole HTTP ou FTP.  Les UR peuvent être utilisés pour décrire les liens vers tout ce que vous codifiez dans un schéma.  Par exemple, le protocole est utilisé pour décrire un lien de messagerie et le système d’exploitation \(OS\) ou le navigateur décide quelle page web ou application doit gérer `mailto://` ce protocole.  

Pour plus d’informations sur la prise en charge existante basée sur le navigateur, accédez aux serveurs de protocole [web.][MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers]  

Cette fonctionnalité vous permet d’effectuer les actions suivantes.  

*   Inscrire votre PWA auprès du système d’exploitation hôte à l’aide du manifeste de votre application web
*   Déclarer qu’un PWA gère un protocole URI spécifique  
     
Après avoir inscrit un PWA en tant que programme de traitement de protocole, lorsqu’un utilisateur choisit un lien hypertexte avec un schéma spécifique tel qu’un navigateur ou une application native, l’application PWA enregistrée est activée par le système d’exploitation et reçoit `mailto://` `web+music://` l’URI.  

Cette fonctionnalité nécessite que vous mettez à jour le manifeste de l’application web pour inclure un tableau, dans le tableau, vous devez `protocol_handlers` spécifier deux champs :  

*   `protocol`: protocole de traitement de la demande, par exemple `mailto` ou `web+jngl` .  
*   `url`: URI HTTPS dans l’étendue de l’application qui gère le protocole.  À l’avenir, l’URI commençant par le schéma de handlers de protocole est prévu pour remplacer le `%s` jeton.  
    
Mettez à jour votre manifeste pour prendre en charge le protocole que vous souhaitez inscrire.  Une fois que vous avez mis en place cette fonctionnalité, Microsoft Edge termine les actions suivantes.  

1.  Détecte les modifications dans le manifeste  
1.  Enregistre l’application pour le protocole  
    
Si plusieurs applications inscrivent un protocole, une invite s’est présentée à l’utilisateur.  L’utilisateur choisit l’application appropriée dans la liste présentée par le système d’exploitation ou le navigateur.  

Pour afficher un aperçu de la gestion [](#turn-on-experimental-features) des protocoles dans Microsoft Edge sur Windows, accédez à Activer les fonctionnalités expérimentales et à activer desktop **Web Apps support Protocol Handlers**.  

Pour plus d’informations sur l’essai d’origine est en cours d’exécution pour les responsables de protocole, accédez à [Register for Web App Protocol Handler Registration][MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration].  

### <a name="example-manifest"></a>Exemple de manifeste

Dans cet exemple, un manifeste d’application web déclare que l’application doit être enregistrée pour gérer les protocoles `web+jngl` et `web+jnglstore` .

```json
{
  "name": "Jungle",
  "description": "A plant encyclopedia",
  "protocol_handlers": [
    {
      "protocol": "web+jngl",
      "url": "/lookup?type=%s"
    },
    {
      "protocol": "web+jnglstore",
      "url": "/shop?for=%s"
    }
  ],
  "icons": [
    {
      "src": "images/icons-192.png",
      "type": "image/png",
      "sizes": "192x192"
    },
  ],
  "background_color": "#007f87",

  "display": "standalone",
  "start_url": "/",
}
```  
 
## <a name="url-link-handling"></a>Gestion des liens d’URL  

Un localisateur de ressources uniforme \(URL\) est un type d’URI.  Créez une expérience plus attrayante lorsque les applications web progressives \(PWAs\) s’inscrivent en tant que handleurs pour les URIs https.  Les URS associés peuvent demander à être lancés lorsque les URIs associés sont activés.  Par exemple, si un utilisateur choisit un lien vers un article d’actualités dans un message électronique.  Un PWA associé pour afficher des articles d’actualités est automatiquement lancé pour gérer l’activation du lien.  

Cette fonctionnalité vous permet d’inscrire un PWA auprès du navigateur à l’aide du manifeste de l’application web et de déclarer que le navigateur gère des liens spécifiques.  Pour inscrire un PWA avec le navigateur, ajoutez le `url_handlers` membre facultatif au fichier manifeste.  Le membre est un groupe qui groupe les origines des `url_handlers` `object[]` URIs que l’application souhaite gérer.  

La gestion des liens est validée par le navigateur à l’aide d’un `web-app-origin-association` fichier JSON situé sur l’origine.  Le fichier d’origine affinera davantage les chemins d’accès inclus ou exclus à l’origine.  Pour obtenir des instructions détaillées sur le test du handler d’URL, accédez à [pwAs en tant que handleurs d’URL.][GithubWicgPwaUrlHandlerBlobMainExplainerMd]  

Pour afficher un aperçu de la gestion [](#turn-on-experimental-features) des liens d’URL dans Microsoft Edge sur Windows, accédez à Activer les fonctionnalités expérimentales et activer la gestion des **URL PWA de bureau.**  

### <a name="example-of-the-url_handlers-in-the-manifest"></a>Exemple de la url_handlers dans le manifeste  

L’extrait de code suivant est un exemple de manifeste d’application web avec le `url_handlers` membre.  

```json 
{
    "name": "Contoso Business App",
    "display": "standalone",
    "icons": [
        {
            "src": "images/icons-144.png",
            "type": "image/png",
            "sizes": "144x144"
        }
    ],
    "capture_links": "existing_client_event",
    "url_handlers" : [
        {
            "origin": "https://contoso.com"
        },
        {
            "origin": "https://conto.so"
        },
        {
            "origin": "https://*.contoso.com"
        }
    ]
}
```  

Un PWA correspond à un URI pour la gestion des URL si l’URI correspond à l’une des chaînes d’origine dans et que le navigateur confirme que l’origine accepte d’autoriser cette application à gérer un tel `url_handlers` URI.  

Le membre contient une origine qui englobe l’étendue, ainsi que d’autres origines non liées `url_handlers` de l’application PWA à l’origine de la demande.  Si vous ne limitez pas les URIs à la même étendue ou domaine que pWA à la demande, vous pouvez utiliser des noms de domaine différents pour le même contenu, mais les gérer avec le même PWA.  

#### <a name="wildcard-matching"></a>Correspondance de caractères génériques  

Utilisez le caractère générique \( `*` \) pour faire correspondre un ou plusieurs caractères.  

Un préfixe générique est utilisé dans les chaînes d’origine du membre à mettre en `url_handlers` correspondance pour différents sous-domaine.  Le préfixe doit être `*.` pour cette utilisation.  Le `https` schéma est supposé lorsque vous utilisez un préfixe générique.  

Par exemple, la `url_handlers` valeur de membre est définie sur `*.contoso.com` correspondances et , mais ne `tenant.contoso.com` correspond pas `www.tenant.contoso.com` `contoso.com` .  

<!-- Hold for future release -->  
<!--  ## Window Controls Overlay for installed desktop web apps  

To create an immersive title bar similar to a native app for your desktop installed web app.  The **Window Controls Overlay** feature  completes the following actions.  
    
1.  Removes the system reserved title bar.  It usually spans the width of the client frame.  
1.  Replaces it with an overlay.  It contains just the critical system required window controls necessary for a user to control the window itself.  
    
After it provides an overlay, the entire web client area is available for you to use.  This feature includes a manifest update.  It provides ways for you to determine the size and position of the overlay to help you arrange content.  
    
### Examples of title bar area customization  

This feature is based on the ability in native apps to customize the title bar.  You may customize a title bar for important app actions or notifications.  Review the following examples for Microsoft Visual Studio Code and Microsoft Teams.  

#### Visual Studio Code  

Microsoft Visual Studio Code is a popular editor built on Electron that ships on multiple desktop platforms.  

The following example displays how Visual Studio Code uses the title bar to maximize available screen real estate to include the current file name and top-level menu structure in the title bar.  

:::image type="complex" source="../media/visual-studio-code-title-customization.png" alt-text="An example of the title bar in Visual Studio Code" lightbox="../media/visual-studio-code-title-customization.png":::
   An example of the title bar in Visual Studio Code  
:::image-end:::  

#### Microsoft Teams  

Workplace collaboration and communication tool Microsoft Teams is also built with Electron and available on multiple desktop platforms.  In the following example, Microsoft Teams displays `back` and `forward` navigation buttons, a search box, and user profile controls.  

:::image type="complex" source="../media/teams-title-customization.png" alt-text="An example of the title bar in Microsoft Teams" lightbox="../media/teams-title-customization.png":::
   An example of the title bar in Microsoft Teams  
:::image-end:::  

### Overlay Window Controls on a Frameless Window  

To provide the maximum addressable area for web content, the browser creates a frameless window, removing all browser UI except for the window controls provided as an overlay.  
The window controls overlay ensures users still minimize, maximize, restore, and close the app.  It also provides access to relevant browser controls using the web app menu.  For Chromium-based browsers, the controls in the overlay.

*   A draggable region the same width and height of each of the window control buttons  
*   The **Settings and more** \(...\) button  
*   The window control buttons minimize, maximize, restore, and close  
    
The following scenarios include when browser displays other content in the controls overlay.  

*   When an installed web app is launched, the origin of the webpage displays to the left of the **Settings and more** \(...\) menu for a few seconds and then disappears.  
*   If a user interacts with an extension using the **Settings and more** \(...\) menu, the icon of the extension displays in the overlay to the left of the three-dot menu.  After you exit any extension dialog, the icon is removed from the overlay.  
    
| Language direction | Overlay location | Details |  
|:--- |:--- |:--- |  
| Left-to-right \(LTR\) | Upper left of the client area | The controls are flipped |  
| Right-to-left \(RTL\) | Upper right corner of the client area |  |  

>[!IMPORTANT]
> The overlay is always on top of the Z-index of the web content and accepts all user input without flowing it through to the web content.  

### Working around the Window Controls Overlay  

Your web content must be aware of the reserved area for the controls overlay.  Ensure the reserved area doesn't expect user interaction.  Query the browser for the bounding rectangle and visibility of the controls overlay.  The information is provided to you through JavaScript APIs and CSS environment variables.  

#### JavaScript APIs  

A new `windowControlsOverlay` object on the `window.navigator` property allows you to query the bounding rectangle of the controls overlay.  

The `windowControlsOverlay` object has the following two objects.  

*   `getBoundingClientRect()` returns a `DOMRect` object.  The `DOMRect` object represents the area under the window controls overlay.  
*   `visible` is a boolean that indicates that the controls overlay is rendered and displayed.  
    
> [!IMPORTANT]
> For privacy reasons, the `windowControlsOverlay` isn't accessible to `iframe` elements in the web content.  

Whenever the overlay is resized, a `geometrychange` event runs on the `navigator.windowControlsOverlay` object to notify the client to recalculate the content layout.  The recalculated content layout is based on the new bounding rectangle of the overlay.  

#### CSS Environment Variables  

Besides the JavaScript API, you may use CSS to query the bounding rectangle of the controls overlay.  Use the following four new CSS environment variables to accomplish to query.  

*   `titlebar-area-x`  
*   `titlebar-area-y`  
*   `titlebar-area-width`  
*   `titlebar-area-height`  
    
### Define Draggable Regions in Web Content  

Users expect to grab and drag the upper region of a window.  To accommodate the expectation, declare specific parts of the web content as draggable.  
To specify an element is draggable, use the webkit proprietary `-webkit-app-region` CSS property.  The CSS working group continues efforts to standardize the `app-region` property.  

To preview this feature in Microsoft Edge for desktop OSs, navigate to [Turn on experimental features](#turn-on-experimental-features) and navigate to **Desktop PWA Window Controls Overlay**.   

### Custom title bar example  

The following example displays how the new features create a web app with a custom title bar.  

:::image type="complex" source="../media/teams-title-customization-example.png" alt-text="Example of a custom title bar in Microsoft Teams" lightbox="../media/teams-title-customization-example.png":::
   Example of a custom title bar in Microsoft Teams  
:::image-end:::  

#### manifest.webmanifest  

In the manifest, set `display_override` array to  `window-controls-overlay`.  Set the `theme_color` to your choice of color for the title bar.  Set the display mode to an appropriate fallback for when either `display_override` or `window-controls-overlay` isn't supported.  

The following code snippet includes the recommended manifest updates.  

```json
{
  "name": "Example PWA",
  "display": "standalone",
  "display_override": [ 
    "window-controls-overlay" 
  ],
  "theme_color": "#254B85"
}
```  

### index.html  

The following IDs represent the two main regions of the webpage.  

*   `titleBarContainer`  
*   `mainContent`  
    
The `div` element with the `titleBar` ID is set to `draggable` and the search box `input` child element is set to `nonDraggable`.  

```html
<div id="titleBar" class=" draggable">
    <span class="draggable">Example PWA</span>
    <input class="nonDraggable" type="text" placeholder="Search"></input>
</div>
```

In the `div` element with the `titleBarContainer` ID, the `div` with the `titleBar` ID represents the visible portion of the title bar area.  

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>Example PWA</title>
    <link rel="stylesheet" href="style.css">
    <link rel="manifest" href="./manifest.webmanifest">
  </head>
  <body>
    <div id="titleBarContainer">
      <div id="titleBar" class=" draggable">
        <span class="draggable">Example PWA</span>
        <input class="nonDraggable" type="text" placeholder="Search"></input>
      </div>
    </div>
    <div id="mainContent">The rest of the webpage</div>
  </body>
</html>
```  

### style.css  

The draggable and non-draggable regions are set using `-webkit-app-region: drag` and `-webkit-app-region: no-drag`.  

```css
.draggable {
    app-region: drag;
    /* Pre-fix app-region during standardization process */
    -webkit-app-region: drag;
}

.nonDraggable {
    app-region: no-drag;
    /* Pre-fix app-region during standardization process */
    -webkit-app-region: no-drag;
}
```  

For the `body` element, margins are set to `0` to ensure the title bar reaches to the edges of the window.  

```css
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
}
```  

The `titleBarContainer` ID uses `position: absolute` and sets the `top` to `titlebar-area-inset-top`, which attaches the container to the top of the webpage.  The `bottom` is set to `titlebar-area-inset-bottom` and falls back to `100% - var(--fallback-title-bar-height)` if the window controls overlay isn't visible.  The background color of the `titleBarContainer` ID is the same as the `theme_color`.  The width is set to `100%`, so that the `div` element fills the width of the webpage and flows under the overlay when it's visible for a contiguous appearance.  

```css
#titleBarContainer {
    position: absolute;
    top: env(titlebar-area-y, 0);
    bottom: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
    width: 100%;
    background-color:#254B85;
}
```  

The `titleBar` ID also uses `position: absolute` and `top: titlebar-area-inset-top` to attaches it to the top of the window.  By default, it consumes the full width of the window.  The `left` and `right` edges are set to `titlebar-area-inset-left` and `titlebar-area-inset-right` respectively, both fall back to `0` when the values aren't set.  It also sets `user-select: none` to prevent any attempts to drag the window consumed instead it highlights text in the `div` element.  

```css
#titleBar {
    position: absolute;
    top: 0;
    display: flex;
    user-select: none;
    height: 100%;
    left: env(titlebar-area-x, 0);
    right: env(titlebar-area-width, 0);
    color: #FFFFFF;
    font-weight: bold;
    text-align: center;
}

#titleBar > span {
    margin: auto;
    padding: 0px 16px 0px 16px;
}

#titleBar > input {
    flex: 1;
    margin: 8px;
    border-radius: 5px;
    border: none;
    padding: 8px;
}
```

The container for the `mainContent` ID is also fixed in place with `position: absolute` and is attached to the bottom of the webpage.  The `height` is set to `titlebar-area-inset-bottom` and falls back to `100% - var(--fallback-titlebar-height)` to fill the remaining space below the title bar.  It sets `overflow-y: scroll` to allow the contents to scroll vertically in the container.  

```css
#mainContent {
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    height: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
    overflow-y: scroll;
}
```

For cases where the browser doesn't support the window controls overlay, a CSS variable is added to set a default height for the title bar.  The bounds of the `titleBarContainer` and `mainContent` IDs are initially set to fill the entire client area, and you don't need to change it if the overlay isn't supported.  

The following code snippet includes all of the recommended css updates.

```css
:root {
  --fallback-title-bar-height: 40px;
}

.draggable {
  app-region: drag;
  /* Pre-fix app-region during standardization process */
  -webkit-app-region: drag;
}

.nonDraggable {
  app-region: no-drag;
  /* Pre-fix app-region during standardization process */
  -webkit-app-region: no-drag;
}

body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  margin: 0;
}

#titleBarContainer {
  position: absolute;
  top: env(titlebar-area-y, 0);
  bottom: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
  width: 100%;
  background-color:#254B85;
}

#titleBar {
  position: absolute;
  top: 0;
  display: flex;
  user-select: none;
  height: 100%;
  left: env(titlebar-area-x, 0);
  right: env(titlebar-area-width, 0);
  color: #FFFFFF;
  font-weight: bold;
  text-align: center;
}

#titleBar > span {
  margin: auto;
  padding: 0px 16px 0px 16px;
}

#titleBar > input {
  flex: 1;
  margin: 8px;
  border-radius: 5px;
  border: none;
  padding: 8px;
}

#mainContent {
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  height: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
  overflow-y: scroll;
}
```  
-->  

## <a name="run-on-os-login"></a>Exécuter sur la connexion au système d’exploitation  

Cette fonctionnalité vous permet de configurer le lancement automatique de votre application lorsque l’utilisateur se connecte à Microsoft Windows.  Plusieurs classes d’applications tirez parti de cette fonctionnalité.  Les classes d’applications incluent la messagerie électronique, la conversation, le tableau de bord de surveillance et les applications d’affichage de données en temps réel.  Cette fonctionnalité permet à un utilisateur d’interagir avec les applications dès qu’il se connecte au système d’exploitation.  Cette fonctionnalité démarre automatiquement PWA de la même façon qu’elle est lancée manuellement.  

> [!IMPORTANT]
> **L’exécuter sur la connexion au** système d’exploitation est une fonctionnalité [puissante.][GithubW3cPermissionsPowerfulFeature]  Les utilisateurs doivent décider d’activer ou non la fonctionnalité pour l’application web installée.  

### <a name="turn-on-run-on-os-login"></a>Activer l’ouverture de session du système d’exploitation  

Pour activer les fonctionnalités **d’ouverture** de session [](#turn-on-experimental-features) du système d’exploitation d’exécuter pour votre application PWA, accédez à Activer les fonctionnalités expérimentales et activer les applications de bureau PWA qui s’exécutent sur la connexion **au système d’exploitation.**  

:::image type="complex" source="../media/desktop-pwas-run-on-os-login-flag.png" alt-text="Activer les applications de bureau de bureau s’exécutent sur l’expérience de connexion au système d’exploitation" lightbox="../media/desktop-pwas-run-on-os-login-flag.png":::
   Activer les applications de bureau de bureau **s’exécutent sur l’expérience de connexion au système d’exploitation**  
:::image-end:::  

### <a name="turn-on-the-feature-for-the-installed-web-app"></a>Activer la fonctionnalité pour l’application web installée  

Pour activer la `Start app when you sign in` fonctionnalité pour un PWA installé, 

1.  Ouvrez MicrosoftEdge.   
1.  Accédez `edge://apps` à .  
1.  Pointez sur votre application.  
1.  Ouvrez le menu contextuel \(clic droit\), puis choisissez **Démarrer l’application lorsque vous vous connectez.**  
    
    :::image type="complex" source="../media/turn-on-run-on-os-login-flag.png" alt-text="Utiliser le menu contextuel pour activer l’application Démarrer lorsque vous vous connectez à la fonctionnalité dans Microsoft Edge" lightbox="../media/turn-on-run-on-os-login-flag.png":::
       Utiliser le menu contextuel pour activer **l’application Démarrer lorsque vous vous connectez** à la fonctionnalité dans Microsoft Edge  
    :::image-end:::  
    
## <a name="shortcuts"></a>Raccourcis  

`Shortcuts` est un nouveau membre du fichier manifeste.  Il vous permet de définir des liens vers des composants, des pages web clés ou des actions dans votre application web.  Microsoft Windows l’intègre en tant **que Jumplists**.  **Les listes de** choix définissent des menus contextuels qui s’affichent lorsque vous êtes sur l’un des éléments d’interface utilisateur suivants et ouvrent un menu contextuel \(clic droit\).  

*   Une vignette dans le menu Démarrer  
*   Icône de la barre des tâches  
    
Lorsqu’un utilisateur appelle un raccourci, il navigue jusqu’à l’adresse spécifiée par le membre `url` du raccourci.  
  
:::image type="complex" source="../media/jumplists-on-windows-10.png" alt-text="Exemple de jumplists sur Windows 10" lightbox="../media/jumplists-on-windows-10.png":::
   Exemple de **jumplists** sur Windows 10  
:::image-end:::  

### <a name="shortcuts-in-the-manifest-file"></a>Raccourcis dans le fichier manifeste  

```json
"shortcuts" : [
  {
    "name": "Today's agenda",
    "url": "/today",
    "description": "List of events planned for today"
  },
  {
    "name": "New event",
    "url": "/create/event"
  },
  {
    "name": "New reminder",
    "url": "/create/reminder"
  }
]
```  

#### <a name="properties-of-shortcuts"></a>Propriétés des raccourcis  

Les propriétés suivantes définissent chaque raccourci.  

| Propriété | Détails |  
|:--- |:--- |  
| `name` | Chaîne qui s’affiche pour l’utilisateur dans **jumplists** ou le menu contextuel. |  
| `short_name` | Chaîne qui s’affiche lorsque l’espace est insuffisant pour afficher le nom complet du raccourci. |  
| `description` | Chaîne qui décrit l’objectif du raccourci.  Il est possible d’y accéder par la technologie d’assistance. |  
| `url` | URI dans l’application web qui s’ouvre lorsque le raccourci est activé. |  
| `icons` | Ensemble d’icônes qui représente le raccourci. |  

## <a name="file-handling"></a>Gestion des fichiers  

La possibilité de s’inscrire en tant que handler de type de fichier est dans la phase d’expérimentation.  Vous pouvez spécifier les types de fichiers gérés par votre application dans une entrée de manifeste.  Lors de l’installation, le système d’exploitation hôte de l’utilisateur inscrit votre application en tant que handleur de fichiers pour les types de fichiers répertoriés.  Assurez-vous que la fonctionnalité existe dans le code de démarrage de vos applications et `launchQueue` qu’elle gère le fichier.  

Les navigateurs basés sur Chromium testent et façonnent cette fonctionnalité.  Pour plus d’informations, y compris des exemples de code, accédez à [Let web applications be file handlers][WebDevFileHandling].  

Pour afficher un aperçu de la gestion des [](#turn-on-experimental-features) fichiers dans Microsoft Edge pour les OS de bureau, accédez à Activer les fonctionnalités expérimentales et activer l’API de **gestion de fichiers.**  
    
## <a name="providing-feedback-on-experimental-features"></a>Commentaires sur les fonctionnalités expérimentales  

Pour fournir des commentaires sur les expériences d’application web Microsoft Edge.  

*   Envoyez vos commentaires à **l’aide de Paramètres et** plus \( `...` \) > **envoyer des commentaires à Microsoft.**  
*   Sélectionnez `Alt` + `Shift` + `I` .  
    
:::image type="complex" source="../media/send-feedback-from-progressive-web-app.png" alt-text="Envoyer des commentaires à partir de votre PWA" lightbox="../media/send-feedback-from-progressive-web-app.png":::
   Envoyer des commentaires à partir de votre PWA  
:::image-end:::  

<!-- links -->  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[MicrosoftDeveloperMicrosoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Essai d’origine | Développeur Microsoft Edge"  
[MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration]: https://developer.microsoft.com/microsoft-edge/origin-trials/web-app-protocol-handler-registration/registration "S’inscrire à l’enregistrement du | Développeur Microsoft"  

[MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers]: https://developer.mozilla.org/docs/Web/API/Navigator/registerProtocolHandler/Web-based_protocol_handlers "Les | MDN"  

[GithubW3cPermissionsPowerfulFeature]: https://w3c.github.io/permissions#powerful-feature "Fonctionnalité puissante : autorisations | GitHub"  

[GithubWicgPwaUrlHandlerBlobMainExplainerMd]: https://github.com/WICG/pwa-url-handler/blob/main/explainer.md "PwAs en tant que | GitHub"  

[WebDevFileHandling]: https://web.dev/file-handling "Que les applications web soient des | web.dev"  
