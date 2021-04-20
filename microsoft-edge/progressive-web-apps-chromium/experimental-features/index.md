---
description: Dernières fonctionnalités expérimentales de Microsoft Edge pour les applications web
title: Fonctionnalités expérimentales | Applications web progressives
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/19/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, expérimentation, applications web progressives, applications web, PWA
ms.openlocfilehash: 641b6fd5185e7f96289c1de6482764979ee0981d
ms.sourcegitcommit: 9cc54ba3e731ecc8b713c3cf215018848f7405b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/19/2021
ms.locfileid: "11496755"
---
# <a name="experimental-features-in-progressive-web-apps-pwas"></a>Fonctionnalités expérimentales dans les applications web progressives (P PWA)  

Microsoft Edge permet d'accéder aux fonctionnalités expérimentales qui sont toujours en développement.  Pour déterminer si chaque fonctionnalité est prête et quand publier chacune d'elles, testez [et fournissez des commentaires.](#providing-feedback-on-experimental-features)  

Les fonctionnalités expérimentales sont disponibles dans tous les canaux de Microsoft Edge, mais les dernières fonctionnalités expérimentales sont disponibles uniquement dans le canal Canary de Microsoft Edge.  

## <a name="turn-on-experimental-features"></a>Activer les fonctionnalités expérimentales  

Pour activer \(ou désactiver\) les fonctionnalités expérimentales dans Microsoft Edge, complétez les étapes suivantes.  
  
1.  Ouvrez MicrosoftEdge.   
    
    > [!NOTE]
    > Veillez à utiliser une version de Microsoft Edge dont l'expérience est répertoriée dans cet article.  Accédez aux [fonctionnalités expérimentales.](#features-that-are-available-to-test)  
    
1.  Accédez `edge://flags` à .  
1.  Accédez à l'expérience pertinente.  
1.  Choisissez le menu déroulant en face de la description de l'expérience et choisissez `Enabled` .  
    
    :::image type="complex" source="../media/turn-on-experimental-flag.png" alt-text="Choose Enabled to turn on an experiment" lightbox="../media/turn-on-experimental-flag.png":::
       Choose **Enabled** to turn on an experiment  
    :::image-end:::  
    
    > [!NOTE]
    > Chaque expérience possède généralement un menu déroulant pour choisir les valeurs suivantes.  Si une fonctionnalité expérimentale ne dispose pas d'une entrée dans **Expériences,** des instructions sont fournies pour démarrer Microsoft Edge avec cette fonctionnalité à l'aide de la ligne de commande.
    > 
    > *   `Default`  
    > *   `Disabled`  
    > *   `Enabled`  
    
1.  Redémarrez MicrosoftEdge.  
    
### <a name="origin-trials"></a>Versions d’évaluation d’origine  

Microsoft Edge utilise parfois des essais d'origine pour tester des fonctionnalités pour des domaines ou des sites web spécifiques.  Vous pouvez utiliser une version d'essai d'origine pour votre site web afin d'appliquer une fonctionnalité spécifique.  Si vous êtes propriétaire d'un site web, vous pouvez vous inscrire à une version d'essai d'origine.  Une version d'essai d'origine fournit des fonctionnalités à un pourcentage d'utilisateurs de Microsoft Edge qui visitent votre site web.

Pour plus d'informations sur les essais d'origine, accédez à la console du développeur des essais [d'origine De Microsoft Edge.][MicrosoftDeveloperMicrosoftEdgeOriginTrials]  
    
> [!NOTE]
> Les fonctionnalités expérimentales sont constamment mises à jour et peuvent entraîner des problèmes de performances.  Pour désactiver une fonctionnalité expérimentale, accédez à Activer [les](#turn-on-experimental-features)fonctionnalités expérimentales, accédez à l'expérience, puis choisissez `Disabled` .  

## <a name="features-that-are-available-to-test"></a>Fonctionnalités disponibles pour le test  

La liste suivante décrit les nouvelles fonctionnalités d'application web expérimentales disponibles pour le test et la validation sur Microsoft Edge.  

| Fonctionnalité | Version de Microsoft Edge | Plateforme |  
|:--- |:--- |:--- |  
| [Gestion du protocole URI](#uri-protocol-handling) | 91 ou ultérieur | Windows et Linux |    
| [Gestion des liens d'URL](#url-link-handling) | 91 ou ultérieur | Windows|
| [Superposition des contrôles de fenêtre pour les applications de bureau](#window-controls-overlay-for-installed-desktop-web-apps) | 91 ou ultérieur | Windows 10|   
| [Exécuter sur la connexion au système d'exploitation](#run-on-os-login) | 88 ou ultérieure | Tous |  
| [Raccourcis](#shortcuts) | 87 ou ultérieure | Tous |  
| [Gestion des fichiers](#file-handling) | 83 ou ultérieure | Tous les ordinateurs de bureau |  


## <a name="uri-protocol-handling"></a>Gestion du protocole URI  

Un identificateur de ressource uniforme \(URI\) peut être utilisé pour définir plus que des liens vers des pages web et du contenu web à l'aide du protocole HTTP ou FTP.  Les URIs peuvent être utilisés pour décrire les liens vers tout ce que vous codifiez dans un schéma.  Par exemple, le protocole est utilisé pour décrire un lien de messagerie et le système d'exploitation \(OS\) ou le navigateur décide quelle page web ou application doit gérer `mailto://` ce protocole.  

Pour plus d'informations sur la prise en charge existante basée sur le navigateur, accédez aux serveurs de protocole [web.][MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers]  

Cette fonctionnalité vous permet d'effectuer les actions suivantes.  

*   Inscrire votre PWA auprès du système d'exploitation hôte à l'aide du manifeste de votre application web
*   Déclarer qu'un PWA gère un protocole URI spécifique  
     
Après avoir inscrit un PWA en tant que programme de traitement de protocole, lorsqu'un utilisateur choisit un lien hypertexte avec un schéma spécifique, tel qu'un navigateur ou une application native, l'application PWA enregistrée est activée par le système d'exploitation et reçoit `mailto://` `web+music://` l'URI.  

Cette fonctionnalité nécessite que vous mettez à jour le manifeste de l'application web pour inclure un tableau, dans le tableau, vous devez `protocol_handlers` spécifier deux champs :  

*   `protocol`: protocole de traitement de la demande, par exemple `mailto` ou `web+jngl` .  
*   `url`: URI HTTPS dans l'étendue de l'application qui gère le protocole.  À l'avenir, l'URI commençant par le schéma de handlers de protocole est prévu pour remplacer le `%s` jeton.  
    
Mettez à jour votre manifeste pour prendre en charge le protocole que vous souhaitez inscrire.  Une fois que vous avez activer cette fonctionnalité, Microsoft Edge termine les actions suivantes.  

1.  Détecte les modifications dans le manifeste  
1.  Enregistre l'application pour le protocole  
    
Si plusieurs applications inscrivent un protocole, une invite s'est présentée à l'utilisateur.  L'utilisateur choisit l'application appropriée dans la liste présentée par le système d'exploitation ou le navigateur.  

Pour afficher un aperçu de la gestion [](#turn-on-experimental-features) des protocoles dans Microsoft Edge sur Windows, accédez à Activer les fonctionnalités expérimentales et à activer la gestion du protocole **PWA de bureau.**  

Pour plus d'informations sur l'essai d'origine en cours d'exécution pour les responsables de protocole, accédez à [Register for Web App Protocol Handler Registration][MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration].  

### <a name="example-manifest"></a>Exemple de manifeste

Dans cet exemple, un manifeste d'application web déclare que l'application doit être enregistrée pour gérer les protocoles `web+jngl` et `web+jnglstore` .

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
 
## <a name="url-link-handling"></a>Gestion des liens d'URL  

Un localisateur de ressources uniforme \(URL\) est un type d'URI.  Créez une expérience plus attrayante lorsque les applications web progressives \(PWAs\) s'inscrivent en tant que handleurs pour les URIs https.  Les P PWA peuvent demander à se lancer lorsque les URIs associés sont activés.  Par exemple, si un utilisateur choisit un lien vers un article d'actualités dans un message électronique.  Un PWA associé pour afficher des articles d'actualités est automatiquement lancé pour gérer l'activation du lien.  

Cette fonctionnalité vous permet d'inscrire un PWA auprès du navigateur à l'aide du manifeste de l'application web et de déclarer que le navigateur gère des liens spécifiques.  Pour inscrire un PWA avec le navigateur, ajoutez le membre `url_handlers` facultatif au fichier manifeste.  Le membre est un groupe qui groupe les origines des `url_handlers` `object[]` URIs que l'application souhaite gérer.  

La gestion des liens est validée par le navigateur à l'aide d'un `web-app-origin-association` fichier JSON situé sur l'origine.  Le fichier d'origine affinera davantage les chemins d'accès inclus ou exclus à l'origine.  Pour obtenir des instructions détaillées sur le test du handler d'URL, accédez à [pwAs en tant que handleurs d'URL.][GithubWicgPwaUrlHandlerBlobMainExplainerMd]  

Pour afficher un aperçu de la gestion [](#turn-on-experimental-features) des liens d'URL dans Microsoft Edge sur Windows, accédez à Activer les fonctionnalités expérimentales et activer la gestion des **URL PWA de bureau.**  

### <a name="example-of-the-url_handlers-in-the-manifest"></a>Exemple de la url_handlers dans le manifeste  

L'extrait de code suivant est un exemple de manifeste d'application web avec le `url_handlers` membre.  

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

Un PWA correspond à un URI pour la gestion des URL si l'URI correspond à l'une des chaînes d'origine dans et que le navigateur confirme que l'origine accepte d'autoriser cette application à gérer un tel `url_handlers` URI.  

Le membre contient une origine qui englobe l'étendue et d'autres `url_handlers` origines non liées de l'application PWA à l'origine de la demande.  Si vous ne limitez pas les URIs à la même étendue ou domaine que pWA à la demande, vous pouvez utiliser des noms de domaine différents pour le même contenu, mais les gérer avec le même PWA.  

#### <a name="wildcard-matching"></a>Correspondance de caractères génériques  

Utilisez le caractère générique \( `*` \) pour faire correspondre un ou plusieurs caractères.  

Un préfixe générique est utilisé dans les chaînes d'origine du membre à mettre en `url_handlers` correspondance pour différents sous-domaine.  Le préfixe doit être `*.` pour cette utilisation.  Le `https` schéma est supposé lorsque vous utilisez un préfixe générique.  

Par exemple, la `url_handlers` valeur de membre est définie sur `*.contoso.com` correspondances et , mais ne `tenant.contoso.com` correspond pas `www.tenant.contoso.com` `contoso.com` .  

## <a name="window-controls-overlay-for-installed-desktop-web-apps"></a>Superposition des contrôles de fenêtre pour les applications web de bureau installées  

Pour créer une barre de titre immersive comme une application native pour votre application web installée sur le bureau, la fonctionnalité Superposition des contrôles **de fenêtre** permet d'effectuer les actions suivantes.  
    
1.  Supprime la barre de titre réservée système.  Elle s'étend généralement sur la largeur du cadre client.  
1.  La remplace par une superposition.  Il contient uniquement les contrôles de fenêtre nécessaires au système critique nécessaires pour qu'un utilisateur contrôle la fenêtre elle-même.  
    
Une fois qu'elle fournit une superposition, toute la zone du client web est disponible.  Cette fonctionnalité inclut une mise à jour du manifeste.  Il vous permet de déterminer la taille et la position de la superposition pour vous aider à organiser le contenu.  

Pour afficher un aperçu des superpositions de contrôles [](#turn-on-experimental-features) de fenêtre dans Microsoft Edge pour Windows 10, accédez à Activer les fonctionnalités expérimentales et accédez à Superposition des contrôles de fenêtre PWA de **bureau.**   

### <a name="examples-of-title-bar-area-customization"></a>Exemples de personnalisation de la zone de barre de titre  

Cette fonctionnalité est basée sur la possibilité dans les applications natives de personnaliser la barre de titre.  Vous pouvez personnaliser une barre de titre pour les actions ou notifications d'application importantes.  Examinez les exemples suivants pour Microsoft Visual Studio Code et Microsoft Teams.  

#### <a name="visual-studio-code"></a>VisualStudioCode  

Microsoft Visual Studio Code est un éditeur populaire créé sur Le Monde et qui est intégré sur plusieurs plateformes de bureau.  

L'exemple suivant montre comment Visual Studio Code utilise la barre de titre pour optimiser l'espace disponible à l'écran afin d'inclure le nom de fichier actuel et la structure de menu de niveau supérieur dans la barre de titre.  

:::image type="complex" source="../media/visual-studio-code-title-customization.png" alt-text="Exemple de barre de titre dans Visual Studio Code" lightbox="../media/visual-studio-code-title-customization.png":::
   Exemple de barre de titre dans Visual Studio Code  
:::image-end:::  

#### <a name="microsoft-teams"></a>Microsoft Teams  

L'outil de collaboration et de communication de l'espace de travail Microsoft Teams est également conçu avec Le poste de travail et disponible sur plusieurs plateformes de bureau.  Dans l'exemple suivant, Microsoft Teams affiche et les boutons de navigation, une zone de `back` `forward` recherche et les contrôles de profil utilisateur.  

:::image type="complex" source="../media/teams-title-customization.png" alt-text="Exemple de barre de titre dans Microsoft Teams" lightbox="../media/teams-title-customization.png":::
   Exemple de barre de titre dans Microsoft Teams  
:::image-end:::  

### <a name="overlay-window-controls-on-a-frameless-window"></a>Overlay Window Controls on a Frameless Window  

Pour optimiser la zone adressaçable du contenu web, le navigateur crée une fenêtre sans cadre.  Une fenêtre sans cadre supprime toutes les interfaces utilisateur du navigateur, à l'exception des contrôles de fenêtre fournis en tant que superposition.  La fenêtre contrôle la superposition permet aux utilisateurs de réduire, d'optimiser, de restaurer et de fermer l'application.  Il permet également d'accéder aux contrôles de navigateur pertinents à l'aide du menu de l'application web.  Pour les navigateurs basés sur Chromium, la superposition inclut les contrôles suivants.  

*   Zone draggable de la même largeur et hauteur de chacun des boutons de contrôle de fenêtre  
*   Le **bouton Paramètres et plus** \(...\)  
*   Les boutons de contrôle de fenêtre réduisent, agrandissent, restaurent et ferment  
    
Outre les contrôles répertoriés précédemment, l'interface utilisateur affichée dans la superposition est resserée dynamiquement dans les scénarios suivants.  

*   Lorsqu'une application web installée est lancée, l'origine de la page web s'affiche à gauche du menu Paramètres et plus \(...\) pendant quelques **secondes,** puis disparaît.  
*   Si un utilisateur interagit avec une extension à l'aide du menu **Paramètres** et plus \(...\), l'icône de l'extension s'affiche dans la superposition à gauche du menu à trois points.  Une fois que vous avez quitté une boîte de dialogue d'extension, l'icône est supprimée de la superposition.  
    
| Sens de la langue | Emplacement de superposition | Détails |  
|:--- |:--- |:--- |  
| De gauche à droite \(LTR\) | Partie supérieure gauche de la zone cliente | Les contrôles sont retournés |  
| De droite à gauche \(RTL\) | Coin supérieur droit de la zone cliente |  |  

> [!IMPORTANT]
> La superposition se trouve toujours au-dessus de l'index Z du contenu web et accepte toutes les entrées de l'utilisateur sans les faire passer au contenu web.  

### <a name="working-around-the-window-controls-overlay"></a>Contourner la superposition des contrôles de fenêtre  

Votre contenu web doit connaître la zone réservée pour la superposition des contrôles.  Assurez-vous que la zone réservée ne s'attend pas à une interaction de l'utilisateur.  Interrogez le navigateur pour le rectangle de limite et la visibilité de la superposition des contrôles.  Les informations vous sont fournies par le biais des API JavaScript et des variables d'environnement CSS.  

#### <a name="javascript-apis"></a>API JavaScript  

Un nouvel objet sur la propriété vous permet d'interroger le rectangle de `windowControlsOverlay` `window.navigator` limite des contrôles de superposition.  

`windowControlsOverlay`L'objet possède les deux objets suivants.  

*   `getBoundingClientRect()` renvoie un `DOMRect` objet.  `DOMRect`L'objet représente la zone sous la superposition des contrôles de fenêtre.  
*   `visible` est un booléen qui indique que la superposition des contrôles est affichée et affichée.  
    
> [!IMPORTANT]
> Pour des raisons de confidentialité, les éléments du contenu web ne sont pas `windowControlsOverlay` `iframe` accessibles.  

Chaque fois que la superposition est recalculée, un événement s'exécute sur l'objet pour avertir le `geometrychange` `navigator.windowControlsOverlay` client de recalculer la disposition de contenu.  La disposition de contenu recalculée est basée sur le nouveau rectangle de limite de la superposition.  

#### <a name="css-environment-variables"></a>Variables d'environnement CSS  

Outre l'API JavaScript, vous pouvez utiliser CSS pour interroger le rectangle de limite de la superposition des contrôles.  Utilisez les quatre nouvelles variables d'environnement CSS suivantes pour effectuer une requête.  

*   `titlebar-area-x`  
*   `titlebar-area-y`  
*   `titlebar-area-width`  
*   `titlebar-area-height`  
    
### <a name="define-draggable-regions-in-web-content"></a>Définir des régions draggables dans le contenu Web  

Les utilisateurs s'attendent à récupérer et faire glisser la zone supérieure d'une fenêtre.  Pour répondre aux attentes, déclarez des parties spécifiques du contenu web comme pouvant être draggables.  
Pour spécifier qu'un élément peut être draggable, utilisez la propriété CSS propriétaire de `-webkit-app-region` WebKit.  Le groupe de travail CSS poursuit ses efforts pour normaliser la `app-region` propriété.  

### <a name="custom-title-bar-example"></a>Exemple de barre de titre personnalisée  

L'exemple suivant montre comment les nouvelles fonctionnalités créent une application web avec une barre de titre personnalisée.  

:::image type="complex" source="../media/teams-title-customization-example.png" alt-text="Exemple de barre de titre personnalisée dans Microsoft Teams" lightbox="../media/teams-title-customization-example.png":::
   Exemple de barre de titre personnalisée dans Microsoft Teams  
:::image-end:::  

#### <a name="manifestwebmanifest"></a>manifest.webmanifest  

Dans le manifeste, définissez `display_override` le tableau sur  `window-controls-overlay` .  Définissez `theme_color` la couleur de votre choix pour la barre de titre.  Définissez le mode d'affichage sur un mode de retour approprié lorsque `display_override` `window-controls-overlay` l'un ou l'autre n'est pas pris en charge.  

L'extrait de code suivant inclut les mises à jour de manifeste recommandées.  

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

### <a name="indexhtml"></a>index.html  

Les ID suivants représentent les deux principales régions de la page web.  

*   `titleBarContainer`  
*   `mainContent`  
    
`div`L'élément avec `titleBar` l'ID est définie sur et l'élément enfant de la zone de recherche `draggable` est définie sur `input` `nonDraggable` .  

```html
<div id="titleBar" class=" draggable">
    <span class="draggable">Example PWA</span>
    <input class="nonDraggable" type="text" placeholder="Search"></input>
</div>
```

Dans `div` l'élément avec `titleBarContainer` l'ID, l'ID représente la partie visible de la zone de `div` `titleBar` barre de titre.  

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
    <div id="mainContent"><!-- The rest of the webpage --></div>
  </body>
</html>
```  

### <a name="stylecss"></a>style.css  

Les régions draggables et non draggables sont définies à `-webkit-app-region: drag` l'aide et `-webkit-app-region: no-drag` .  

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

Pour l'élément, les marges sont définies pour garantir que la barre de titre atteint les `body` `0` bords de la fenêtre.  

```css
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
}
```  

L'ID utilise et définit le , qui joint le conteneur en `titleBarContainer` haut de la page `position: absolute` `top` `titlebar-area-inset-top` web.  Est `bottom` définie sur et revient à si la fenêtre contrôle la `titlebar-area-inset-bottom` `100% - var(--fallback-title-bar-height)` superposition n'est pas visible.  La couleur d'arrière-plan `titleBarContainer` de l'ID est identique à la `theme_color` couleur .  La largeur est définie sur , de sorte que l'élément remplit la largeur de la page web et se trouve sous la superposition lorsqu'il est visible pour une `100%` `div` apparence contiguë.  

```css
#titleBarContainer {
    position: absolute;
    top: env(titlebar-area-y, 0);
    bottom: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
    width: 100%;
    background-color:#254B85;
}
```  

`titleBar`L'ID `position: absolute` l'utilise `top: titlebar-area-inset-top` également et l'attache en haut de la fenêtre.  Par défaut, elle consomme toute la largeur de la fenêtre.  Les bords et les bords sont respectivement définies sur le moment où les valeurs ne `left` `right` sont pas `titlebar-area-inset-left` `titlebar-area-inset-right` `0` définies.  Il définit également pour empêcher toute tentative de faire glisser la fenêtre consommée à la place, il met en sur `user-select: none` évidence le texte dans l'élément. `div`  

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

Le conteneur de l'ID est également corrigé sur place et attaché `mainContent` au bas de la page `position: absolute` web.  La `height` propriété est définie sur et revient pour remplir `titlebar-area-inset-bottom` `100% - var(--fallback-titlebar-height)` l'espace restant sous la barre de titre.  Il définit `overflow-y: scroll` pour permettre au contenu de défiler verticalement dans le conteneur.  

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

Dans les cas où le navigateur ne prend pas en charge la superposition des contrôles de fenêtre, une variable CSS est ajoutée pour définir une hauteur par défaut pour la barre de titre.  Les limites des ID et des ID sont initialement définies pour remplir l'intégralité de la zone cliente, et vous n'avez pas besoin de la modifier si la superposition `titleBarContainer` `mainContent` n'est pas prise en charge.  

L'extrait de code suivant inclut toutes les mises à jour CSS recommandées.

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

## <a name="run-on-os-login"></a>Exécuter sur la connexion au système d'exploitation  

Cette fonctionnalité vous permet de configurer le lancement automatique de votre application lorsque l'utilisateur se connecte à Microsoft Windows.  Plusieurs classes d'applications tirez parti de cette fonctionnalité.  Les classes d'applications incluent la messagerie électronique, la conversation, le tableau de bord de surveillance et les applications d'affichage de données en temps réel.  Cette fonctionnalité permet à un utilisateur d'interagir avec les applications dès qu'il se connecte au système d'exploitation.  Cette fonctionnalité démarre automatiquement PWA de la même façon qu'elle est lancée manuellement.  

> [!IMPORTANT]
> **L'exécuter sur la connexion au** système d'exploitation est une fonctionnalité [puissante.][GithubW3cPermissionsPowerfulFeature]  Les utilisateurs doivent décider d'activer ou non la fonctionnalité pour l'application web installée.  

### <a name="turn-on-run-on-os-login"></a>Activer l'ouverture de session du système d'exploitation  

Pour afficher un aperçu des fonctionnalités de connexion [](#turn-on-experimental-features) au système d'exploitation **RunOn** pour votre PWA, accédez à Activer les fonctionnalités expérimentales et activer les applications de bureau PWA qui s'exécutent sur la connexion **au système d'exploitation.**  

:::image type="complex" source="../media/desktop-pwas-run-on-os-login-flag.png" alt-text="Activer les applications de bureau de bureau s'exécutent sur l'expérience de connexion au système d'exploitation" lightbox="../media/desktop-pwas-run-on-os-login-flag.png":::
   Activer les applications de bureau de bureau **s'exécutent sur l'expérience de connexion au système d'exploitation**  
:::image-end:::  

### <a name="turn-on-the-feature-for-the-installed-web-app"></a>Activer la fonctionnalité pour l'application web installée  

Pour activer la `Start app when you sign in` fonctionnalité pour un PWA installé, 

1.  Ouvrez MicrosoftEdge.   
1.  Accédez `edge://apps` à .  
1.  Pointez sur votre application.  
1.  Ouvrez le menu contextuel \(clic droit\), puis choisissez **Démarrer l'application lorsque vous vous connectez.**  
    
    :::image type="complex" source="../media/turn-on-run-on-os-login-flag.png" alt-text="Utiliser le menu contextuel pour activer l'application Démarrer lorsque vous vous connectez à la fonctionnalité dans Microsoft Edge" lightbox="../media/turn-on-run-on-os-login-flag.png":::
       Utiliser le menu contextuel pour activer **l'application Démarrer lorsque vous vous connectez** à la fonctionnalité dans Microsoft Edge  
    :::image-end:::  
    
## <a name="shortcuts"></a>Raccourcis  

`Shortcuts` est un nouveau membre du fichier manifeste.  Il vous permet de définir des liens vers des composants, des pages web clés ou des actions dans votre application web.  Microsoft Windows l'intègre en tant **que Jumplists**.  **Les listes de** choix définissent des menus contextuels qui s'affichent lorsque vous êtes sur l'un des éléments d'interface utilisateur suivants et ouvrent un menu contextuel \(clic droit\).  

*   Vignette du menu Démarrer  
*   Icône de la barre des tâches  
    
Lorsqu'un utilisateur appelle un raccourci, il navigue jusqu'à l'adresse spécifiée par le membre `url` du raccourci.  
  
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
| `name` | Chaîne qui s'affiche pour l'utilisateur dans **jumplists** ou le menu contextuel. |  
| `short_name` | Chaîne qui s'affiche lorsque l'espace est insuffisant pour afficher le nom complet du raccourci. |  
| `description` | Chaîne qui décrit l'objectif du raccourci.  Il est possible d'y accéder par la technologie d'assistance. |  
| `url` | URI dans l'application web qui s'ouvre lorsque le raccourci est activé. |  
| `icons` | Ensemble d'icônes qui représente le raccourci. |  

## <a name="file-handling"></a>Gestion des fichiers  

La possibilité de s'inscrire en tant que handler de type de fichier est en phase d'expérimentation.  Vous pouvez spécifier les types de fichiers gérés par votre application dans une entrée de manifeste.  Lors de l'installation, le système d'exploitation hôte de l'utilisateur inscrit votre application en tant que responsable de fichiers pour les types de fichiers répertoriés.  Assurez-vous que la fonctionnalité existe dans le code de démarrage de vos applications et `launchQueue` qu'elle gère le fichier.  

Les navigateurs basés sur Chromium testent et façonnent cette fonctionnalité.  Pour plus d'informations, y compris des exemples de code, accédez à [Let web applications be file handlers][WebDevFileHandling].  

Pour afficher un aperçu de la gestion des [](#turn-on-experimental-features) fichiers dans Microsoft Edge pour Windows 10, accédez à Activer les fonctionnalités expérimentales et activer l'API de **gestion de fichiers.**  
    
## <a name="providing-feedback-on-experimental-features"></a>Commentaires sur les fonctionnalités expérimentales  

Pour fournir des commentaires sur les expériences d'application web Microsoft Edge.  

*   Envoyez vos commentaires à **l'aide de Paramètres et** plus \( `...` \) > **envoyer des commentaires à Microsoft.**  
*   Sélectionnez `Alt` + `Shift` + `I` .  
    
:::image type="complex" source="../media/send-feedback-from-progressive-web-app.png" alt-text="Envoyer des commentaires à partir de votre PWA" lightbox="../media/send-feedback-from-progressive-web-app.png":::
   Envoyer des commentaires à partir de votre PWA  
:::image-end:::  

<!-- links -->  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[MicrosoftDeveloperMicrosoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Essai d'origine | Développeur Microsoft Edge"  
[MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration]: https://developer.microsoft.com/microsoft-edge/origin-trials/web-app-protocol-handler-registration/registration "S'inscrire à l'enregistrement du | Développeur Microsoft"  

[MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers]: https://developer.mozilla.org/docs/Web/API/Navigator/registerProtocolHandler/Web-based_protocol_handlers "Les | MDN"  

[GithubW3cPermissionsPowerfulFeature]: https://w3c.github.io/permissions#powerful-feature "Fonctionnalité puissante : autorisations | GitHub"  

[GithubWicgPwaUrlHandlerBlobMainExplainerMd]: https://github.com/WICG/pwa-url-handler/blob/main/explainer.md "PwAs en tant que | GitHub"  

[WebDevFileHandling]: https://web.dev/file-handling "Que les applications web soient des | web.dev"  
