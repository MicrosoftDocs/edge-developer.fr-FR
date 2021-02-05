---
description: L’outil Nouveautés est désormais welcome, Visual Font Editor dans le volet Styles, outils de débogage CSS Flexbox, etc.
title: Nouveautés de DevTools (Microsoft Edge 89)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 0a8a5e69281ced9421733059b554bd8cb997c7cd
ms.sourcegitcommit: 085046a5885c68243b763aaf6809fea43452403a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "11313775"
---
# Nouveautés de DevTools (Microsoft Edge 89)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## Nouveautés : bienvenue  

<!--  Title: What's New is now Welcome  -->  
<!--  Subtitle: The What's New tool now has a new appearance and a new name:  Welcome -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

**L’outil Nouveautés** de Microsoft Edge DevTools a désormais une nouvelle apparence et un nouveau nom : **Bienvenue**.  **L’outil Welcome** affiche toujours les dernières actualités et mises à jour DevTools.  Il inclut désormais également des liens vers la documentation DevTools de Microsoft Edge, des méthodes pour envoyer des commentaires, et bien plus encore.  Pour afficher **l’outil d’accueil** après chaque mise à jour de Microsoft Edge, cochez la case en regard de l’onglet Ouvrir après **chaque** mise à jour sous le titre.  Pour fermer **l’outil Bienvenue,** choisissez **le X** sur le côté droit du titre de l’onglet.  Si vous préférez **l’outil Nouveautés d’origine,** accédez à [Expériences][DevtoolsCustomizeIndexSettings]de paramètres et supprimez la case à cocher en regard de  >  **** l’onglet **Activer l’accueil.**  

:::image type="complex" source="../../media/2021/01/welcome-tool-whats-new-88.msft.png" alt-text="L’outil Bienvenue est mis en surbrill" lightbox="../../media/2021/01/welcome-tool-whats-new-88.msft.png":::
   **L’outil Bienvenue** est mis en surbrill  
:::image-end:::  

## Visual Font Editor dans le volet Styles  

<!--  Title: Visual font editor in the Styles pane  -->  
<!--  Subtitle: Visual font editor in the Styles pane -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Lorsque vous utilisez des polices dans CSS, utilisez le nouvel éditeur de [polices visuel.][DevtoolsInspectStylesEditFonts]  Vous pouvez définir des polices de secours et utiliser des curseurs pour définir le poids, la taille, la hauteur de ligne et l’espacement de la police.  **L’éditeur de** polices vous aide à effectuer les actions suivantes.  

*   Basculer entre les unités pour différentes propriétés de police  
*   Basculer entre les mots clés pour différentes propriétés de police  
*   Convertir des unités  
*   Générer un code CSS précis  
    
Pour activer cette expérience, accédez à Expériences de [paramètres][DevtoolsCustomizeIndexSettings]et cochez la case en regard d’Activer les nouveaux outils Éditeur de polices  >  **** dans le **volet Styles.**  Pour plus d’informations, accédez à Modifier les styles et paramètres de police CSS dans le volet [Styles de DevTools.][DevtoolsInspectStylesEditFonts]  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1093229][CR1093229].  

:::image type="complex" source="../../media/2021/01/visual-font-editor.msft.png" alt-text="L’éditeur de police visuel est mis en surbrillon dans le volet Styles" lightbox="../../media/2021/01/visual-font-editor.msft.png":::
   L’éditeur **de police visuel** est mis en surbrillon dans le volet **Styles**  
:::image-end:::  

## Outils de débogage CSS Flexbox  

Les fonctionnalités de débogage Flexbox sont en cours de développement.  Pour activer l’expérience pour les deux [fonctionnalités suivantes,][DevtoolsCustomizeIndexSettings]accédez à Expériences de paramètres et activez la case à cocher en regard de activer les nouvelles fonctionnalités de débogage de la boîte de réception  >  **** **Flexbox CSS.**  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problèmes [1136394][CR1136394] et [1139949][CR1139949].  

### La nouvelle icône Flexbox (flex) permet d’identifier et d’afficher les conteneurs flex  

<!--  Title: Display Flexbox containers with Flexbox (flex) icon  -->  
<!--  Subtitle: New Flexbox (flex) icon in the Elements tool help you identify Flexbox containers in your code.  When toggled, the adorner displays and hides outlines of the flex container to help you debug the layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Dans **l’outil Elements,** la nouvelle icône Flexbox (flex) vous permet d’identifier les conteneurs Flexbox dans votre code.  Sélectionnez l’icône Flexbox \(flex\) pour activer ou désactiver l’effet de superposition qui contoure un conteneur Flexbox.  Vous pouvez personnaliser la couleur de **** la superposition dans le volet De disposition, qui se trouve à côté de **Styles** et **calculé**.  

:::row:::
   :::column span="":::
      Pour activer et désactiver l’effet de superposition qui contoure le conteneur Flexbox, choisissez l’icône Flexbox \( `flex` \).  
   :::column-end:::
   :::column span="":::
      Vous pouvez personnaliser la couleur de **** la superposition dans le volet De disposition en côté de **Styles** et **calculé .**  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container.msft.png" alt-text="Icône Flexbox (flex) et page web mises en surbrill" lightbox="../../media/2021/01/elements-flex-container.msft.png":::
         Icône **Flexbox** \( `flex` \) et page web mises en surbrillion :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-layout-flex-container.msft.png" alt-text="Superpositions Flexbox mises en évidence dans le volet De disposition" lightbox="../../media/2021/01/elements-layout-flex-container.msft.png":::
         **Superpositions Flexbox mises** en évidence dans **le** volet De disposition  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### Afficher les icônes d’alignement et le quadrillage lorsque les dispositions de Flexbox changent à l’aide des propriétés CSS  

<!--  Title: Display alignment icons and gridlines for changes to Flexbox layouts from CSS properties  -->  
<!--  Subtitle:  CSS autocomplete in the Styles tool now displays icons next to Flexbox properties to help you review the effect a property has on your Flexbox layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Lorsque vous modifiez CSS pour votre disposition Flexbox, les mises à jour automatiques CSS dans le volet **Styles** affichent désormais des icônes utiles en plus des propriétés Flexbox pertinentes.  Pour essayer cette nouvelle fonctionnalité, ouvrez **l’outil Éléments** et sélectionnez un conteneur flexible.  Ensuite, ajoutez ou modifiez une propriété sur ce conteneur dans le **volet Styles.**  

:::row:::
   :::column span="":::
      Le menu de la mise à jour automatique affiche désormais des icônes qui indiquent l’effet des propriétés d’alignement telles `align-content` que et `align-items` .  
   :::column-end:::
   :::column span="":::
      De plus, DevTools affiche désormais une ligne de guid pour vous aider à mieux examiner la `align-items` propriété CSS.  La `gap` propriété CSS est également prise en charge.  Dans la figure suivante, la propriété CSS est définie sur et le modèle d’effet de hachage `gap` `gap: 12px;` pour chaque intervalle s’affiche.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align.msft.png" alt-text="Menu de la mise en surbrillence automatique mis en surbrillence pour les propriétés CSS qui commencent par align-" lightbox="../../media/2021/01/elements-flex-container-align.msft.png":::
         Menu de la mise à jour automatique mis en surbrillence pour les propriétés CSS qui commencent par `align-`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png" alt-text="Espace flexbox dans les propriétés CSS et la page web mis en surbrillion" lightbox="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png":::
         Flexbox `gap` dans les propriétés CSS et la page web mises en surbrillion  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Ajouter rapidement des outils avec le nouveau bouton Plus d’outils  

<!--  Title: Add tools quickly with new More Tools button  -->  
<!--  Subtitle: A convenient way to open new tools in Microsoft Edge DevTools -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Vous avez maintenant une nouvelle façon d’ouvrir d’autres outils dans Microsoft Edge DevTools.  Une fois que vous **** avez activer cette expérience, l’icône Plus d’outils s’affiche sous la forme d’un signe plus ( ) à droite `+` du panneau principal.  Pour afficher la liste des autres outils à ajouter au panneau principal, sélectionnez l’icône Plus d’outils **\(** `+` \).  Pour activer cette expérience, accédez à Expériences de [paramètres,][DevtoolsCustomizeIndexSettings]puis activez la case à cocher en regard de l’onglet Activer + bouton pour ouvrir  >  **d’autres****outils.**  

:::image type="complex" source="../../media/2021/01/more-tools.msft.png" alt-text="Autres outils mis en évidence dans DevTools" lightbox="../../media/2021/01/more-tools.msft.png":::
   **Autres outils** mis en évidence dans DevTools  
:::image-end:::  

## Les technologies d’assistance annoncent désormais la position et le nombre de suggestions CSS  

<!--  Title: Assistive technologies now announce position and count of CSS suggestions  -->  
<!--  Subtitle: CSS suggestions are now easier to navigate using screen readers -->  

Lorsque vous modifiez CSS, vous obtenez une dropdown de fonctionnalités.  Cette fonctionnalité n’était pas disponible pour les utilisateurs de technologies d’assistance, car elle est annoncée dans Microsoft Edge version 89.  Un utilisateur de technologies d’assistance peut désormais parcourir les suggestions CSS dans le **volet Styles.**  Dans Microsoft Edge version 88 et versions antérieures, la technologie d’assistance annoncée en tant qu’utilisateur a accédé à la liste des suggestions lors de la modification de CSS dans le volet `Suggestion` **Styles.**  Dans Microsoft Edge version 89, un utilisateur de technologie d’assistance entend désormais la position et le nombre de suggestions actuelles.  Chaque suggestion est annoncée lorsque l’utilisateur navigue dans la liste des suggestions, telles que la suggestion 3 sur 5.  Pour en savoir plus sur l’écriture de CSS dans DevTools, accédez à [Modifier CSS][DevtoolsCssReferenceChangeCss].  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1157329][CR1157329].  

Pour afficher une vidéo qui affiche et lit plusieurs suggestions avec cette expérience, accédez à Voiceover pour annoncer les [options devtools](https://youtu.be/9TcUpleEwwA) sur YouTube.  

:::image type="complex" source="../../media/2021/01/announce-css-suggestion.msft.png" alt-text="Suggestion mise en évidence dans le volet Styles" lightbox="../../media/2021/01/announce-css-suggestion.msft.png":::
   Liste `suggestion` mise en évidence dans le volet **Styles**  
:::image-end:::  

## Émuler Surface Duo et Samsung Samsung Fold  

<!--  Title: Emulate new dual-screen and foldable devices  -->  
<!--  Subtitle: Test the appearance and feel of your website or app with Surface Duo and Samsung Galaxy Fold emulators -->  

Testez l’apparence de votre site web ou de votre application sur les appareils suivants dans Microsoft Edge.  

*   [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo]  
*   [Samsung Galaxy Fold][SamsungUsMobileGalaxyFold]  
    
Activer les **fonctionnalités de** plateforme Web expérimentale pour accéder à la nouvelle fonctionnalité multimédia [CSS][DualScreenWebCssMediaSpanning] couvrant l’écran et à [l’API JavaScript getWindowSegments.][DualScreenWebJavascriptGetwindowsegments]  Accédez à `edge://flags` l’indicateur et basculez-le en de côté des **fonctionnalités de plateforme Web expérimentale.**  Pour améliorer votre site web ou votre application pour les appareils à double écran et pliables, utilisez les fonctionnalités suivantes lors de [l’émulation de l’appareil.][DevtoolsDeviceModeIndex]  

*   [Couvrant,][DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices]c’est-à-dit lorsque votre site web \(ou application\) apparaît sur les deux écrans.  
*   [Rendu de la séam,][DualScreenIntroductionHowToWorkWithSeam]qui est l’espace entre les deux écrans.  
    
Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1054281][CR1054281].  

:::image type="complex" source="../../media/2021/01/emulate-surface-device-surface-duo.msft.png" alt-text="Émuler double écran" lightbox="../../media/2021/01/emulate-surface-device-surface-duo.msft.png":::
   Émuler double écran  
:::image-end:::  

## Outils de développement Microsoft Edge Visual Studio Code version 1.1.2  

Les outils de développement [Microsoft Edge pour Visual Studio l’extension][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] de code version 1.1.2 pour Microsoft Visual Studio Code ont les modifications suivantes depuis la version précédente.  Microsoft Visual Studio code met automatiquement à jour les extensions.  Pour mettre à jour manuellement la version 1.1.2, accédez à Mettre à jour [une extension manuellement.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  

*   Ajout **d’un bouton Fermer l’instance** à chaque élément de la liste cible \([#248][GithubMicrosoftVscodeEdgeDevtoolsPull248]\)  
*   Version de [Microsoft Edge DevTools][DevtoolsMain] déversée de 84.0.522.63 à [85.0.564.40][DevtoolsWhatsNew85] \([#235][GithubMicrosoftVscodeEdgeDevtoolsPull235]\)  
*   [Débogger inclus pour Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge] en tant que dépendance \([#233][GithubMicrosoftVscodeEdgeDevtoolsPull233]\)  
*   Option de paramètres implémentée pour modifier les thèmes d’extension \([#229][GithubMicrosoftVscodeEdgeDevtoolsPull229]\)  
    
Vous pouvez déposer des problèmes et contribuer à l’extension sur le référentiel [GitHub vscode-edge-devtools.][GithubMicrosoftVscodeEdgeDevtools]  

## Annonces du projet de Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Capture d’écran du nœud au-delà de la vue  

Dans Microsoft Edge version 89, les captures d’écran de nœud sont plus précises, ce qui permet de capturer le nœud complet même si le contenu du nœud n’est pas visible dans la vue.  Dans **l’outil Éléments,** pointez sur un élément, ouvrez le menu contextuel \(clic droit\), puis choisissez **Capture d’écran du nœud .**  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1003629][CR1003629].  

:::image type="complex" source="../../media/2021/01/capture-node-screenshot.msft.png" alt-text="Capture d’écran du nœud mis en évidence dans le menu contextique de l’outil Éléments" lightbox="../../media/2021/01/capture-node-screenshot.msft.png":::
   **Capture d’écran du nœud** mis en évidence dans le menu contextique de **l’outil Éléments**  
:::image-end:::  

### Mises à jour de l’outil Éléments  

#### Prise en charge du forçage de l’état CSS cible  

Vous pouvez désormais utiliser DevTools pour forcer [la][MdnDocsWebCssTarget] pseudo-classe CSS cible.  La pseudo-classe est déclenchée lorsqu’un élément unique \(l’élément cible\) a un élément qui correspond à un `:target` `id` fragment de l’URL.  Par exemple, `http://www.example.com/index.html#section1` l’URL déclenche la `:target` pseudo-classe sur un élément HTML avec `id="section1"` .  Pour essayer une démonstration avec la section 1 mise en évidence, accédez à [CSS :target demo][GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1].  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1156628][CR1156628].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-none-forced.msft.png" alt-text="Page web mise en surbrillant sans CSS forcé" lightbox="../../media/2021/01/elements-styles-none-forced.msft.png":::
         Page web mise en surbrillant sans CSS forcé  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-target-forced.msft.png" alt-text=":target CSS forcé et page web mise en surbrill" lightbox="../../media/2021/01/elements-styles-target-forced.msft.png":::
         `:target` CSS forcé et page web mise en surbrill  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### Utiliser des éléments dupliqués pour copier des éléments  

Utilisez le raccourci du nouvel élément **Duplicate** pour cloner un élément.  Dans **l’outil Éléments,** pointez sur un élément, ouvrez le menu contextuel \(clic droit\), choisissez **Élément dupliqué**.  Un nouvel élément est créé sous l’élément sélectionné.  Pour dupliquer l’élément à l’aide d’un raccourci clavier, sélectionnez `Shift` + `Alt` + `Down Arrow` \(Windows/Linux\) ou `Shift` + `Option` + `Down Arrow` \(macOS\).  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1150797][CR1150797].  

:::image type="complex" source="../../media/2021/01/elements-duplicate-element.msft.png" alt-text="L’élément Duplicate est mis en surbrillon dans le menu contextique d’un élément de l’outil Elements" lightbox="../../media/2021/01/elements-duplicate-element.msft.png":::
   **L’élément Duplicate** est mis en surbrillon dans le menu contextique d’un élément de **l’outil Elements**  
:::image-end:::  

#### S sélectionneurs de couleurs pour les propriétés CSS personnalisées  

Le **volet Styles** affiche désormais les soches de couleur pour les propriétés CSS personnalisées.  Pour passer en cycle dans les formats RGBA, HSLA et Hex de la valeur de couleur, maintenez et choisissez le s `Shift` sélectionneur de couleurs.  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1147016.][CR1147016]  

:::image type="complex" source="../../media/2021/01/elements-styles-change-color-format.msft.png" alt-text="S sélectionneurs de couleurs pour les propriétés CSS personnalisées" lightbox="../../media/2021/01/elements-styles-change-color-format.msft.png":::
   S sélectionneurs de couleurs pour les propriétés CSS personnalisées  
:::image-end:::  

#### Copier les classes et propriétés CSS  

Vous pouvez maintenant copier les propriétés CSS plus rapidement avec quelques nouvelles options dans le menu contextuel.  Dans **l’outil Elements,** choisissez un élément.  Pour copier la valeur, dans le volet **Styles,** pointez sur une classe CSS ou une propriété CSS, ouvrez un menu contextuel \(clic droit\), puis choisissez l’option de copie.  

:::row:::
   :::column span="":::
      Copiez les options d’une classe CSS.  
      
      | Option | Détails |  
      |:--- |:--- |  
      | **Sélecteur de copie** | Copiez le nom du sélecteur actuel. |  
      | **Règle de copie** | Copiez la règle du sélecteur actuel. |  
      | **Copier toutes les déclarations** | Copiez toutes les déclarations sous la règle actuelle, y compris les propriétés non valides et préfixées. |  
   :::column-end:::
   :::column span="":::
      Options de copie pour une propriété CSS.  
      
      | Option | Détails |      
      |:--- |:--- |  
      | **Déclaration de copie** | Copiez la déclaration de la ligne actuelle. |  
      | **Copy, propriété** | Copiez la propriété de la ligne actuelle. |  
      | **Valeur de copie** | Copiez la valeur de la ligne actuelle. |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-class.msft.png" alt-text="Copier les options d’une classe CSS dans le menu contextuel" lightbox="../../media/2021/01/copy-css-class.msft.png":::
         Copier les options d’une classe CSS dans le menu contextuel  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-property-cropped.msft.png" alt-text="Copier les options d’une propriété CSS dans le menu contextuel" lightbox="../../media/2021/01/copy-css-property.msft.png":::
         Copier les options d’une propriété CSS dans le menu contextuel  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1152391][CR1152391].  

### Mises à jour des cookies  

#### Nouvelle option pour afficher les cookies décodés par l’URL  

Vous pouvez maintenant choisir d’afficher la valeur des cookies décodés par l’URL dans le **volet Cookies.**  Pour afficher le cookie décodé, accédez au volet Cookies de **l’application,** choisissez un cookie dans la liste, puis cochez la case en regard de  >  **** **l’url décodée.**  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au [problème 997625][CR997625].  

:::image type="complex" source="../../media/2021/01/application-cookies-show-url-decoded.msft.png" alt-text="Option d’affichage des cookies décodés par l’URL" lightbox="../../media/2021/01/application-cookies-show-url-decoded.msft.png":::
   Option d’affichage des cookies décodés par l’URL  
:::image-end:::  

#### Filtrer et effacer les cookies visibles  

Dans Microsoft Edge version 88 ou antérieure, l’outil **Application** fournissait uniquement un moyen d’effacer tous les cookies avec le bouton Effacer **tous les cookies.**  Dans Microsoft Edge version 89, vous pouvez désormais choisir Effacer les **cookies filtrés** pour supprimer uniquement les cookies filtrés.  Pour filtrer les **** cookies, accédez à  >  **Cookies d’application**et tapez dans la **boîte** de texte Filtrer.  Pour supprimer les cookies affichés, sélectionnez le bouton Effacer **les cookies filtrés.**  Pour afficher tous les autres cookies, effacer le texte du filtre.  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au [problème 978059][CR978059].  

:::image type="complex" source="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png" alt-text="Effacer uniquement les cookies visibles" lightbox="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png":::
   Effacer uniquement les cookies visibles  
:::image-end:::  

#### Nouvelle option pour effacer les cookies tiers dans le volet stockage  

DevTools n’effacera désormais que les cookies de première partie par défaut.  Pour effacer les données du site web **** et les cookies de première partie uniquement, accédez au stockage d’applications, puis choisissez  >  **** Effacer les données **de site.**  

Pour effacer les données du site web et tous les cookies, accédez à **Stockage**  >  **d’applications.**  Cochez la case en regard de **l’utilisation de cookies tiers,** puis **sélectionnez Effacer les données du site.**  

Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1012337][CR1012337].  

:::image type="complex" source="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png" alt-text="Option pour effacer les cookies tiers" lightbox="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png":::
   Option pour effacer les cookies tiers  
:::image-end:::  

### Mises à jour de l’outil réseau  

#### Paramètre du journal réseau d’enregistrement persistant  

Dans Microsoft Edge version 88 ou antérieure, DevTools réinitialise le paramètre enregistrer le journal réseau lors de l’actualisation d’une page web. ****  Dans Microsoft Edge version 89, DevTools fait désormais persister le paramètre Enregistrer le **journal réseau.**  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1122580][CR1122580].  

:::image type="complex" source="../../media/2021/01/network-log.msft.png" alt-text="Enregistrer le journal réseau" lightbox="../../media/2021/01/network-log.msft.png":::
   Enregistrer le journal réseau  
:::image-end:::  

#### L’option en ligne n’est plus une option de limitation  

L’option d’émulation réseau **en ligne** est désormais renommée **No Throttling**.  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1028078][CR1028078].  

:::image type="complex" source="../../media/2021/01/network-no-throttling.msft.png" alt-text="Aucune option de limitation" lightbox="../../media/2021/01/network-no-throttling.msft.png":::
   **Aucune** option de limitation  
:::image-end:::  

### Nouvelles options de copie dans l’outil Console, l’outil Sources et le volet Styles

#### Copier un objet dans l’outil Console et Sources  

Vous pouvez maintenant copier des valeurs d’objet dans les outils **Console** **et Sources.**  La possibilité de copier des valeurs d’objet est utile lorsque vous travaillez avec des objets de grande taille.  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problèmes [1148353][CR1148353] et [1149859][CR1149859].  

:::row:::
   :::column span="":::
      Dans **l’outil Console,** pointez sur un objet, ouvrez le menu contextuel \(clic droit\), puis choisissez **Copier l’objet**.  
   :::column-end:::
   :::column span="":::
      Dans l’outil **Sources,** sur un point d’arrêt, pointez sur un objet, dans la fenêtre contextuelle Objet, sélectionnez un objet, ouvrez le menu contextuel \(clic droit\), puis choisissez Copier l’objet **.** ****  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/console-copy-object.msft.png" alt-text="Copier un objet dans la console" lightbox="../../media/2021/01/console-copy-object.msft.png":::
         Copier un objet dans la **console**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png" alt-text="Copier un objet dans les sources" lightbox="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png":::
         Copier un objet dans les **sources**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### Copier le nom de fichier dans l’outil Sources et le volet Styles  

Vous pouvez maintenant copier un nom de fichier à l’aide du menu contextuel.  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problèmes [1155120][CR1155120].  

:::row:::
   :::column span="":::
      Dans **l’outil Sources,** pointez sur un nom de fichier, ouvrez le menu contextuel \(clic droit\), puis choisissez Copier le nom **du fichier.**  
   :::column-end:::
   :::column span="":::
      Dans **le** volet Styles **** de l’outil >, pointez sur un nom de fichier, ouvrez le menu contextuel \(clic droit\), puis choisissez Copier le nom **du fichier.**  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-copy-file-name.msft.png" alt-text="Copier le nom du fichier dans les sources" lightbox="../../media/2021/01/sources-copy-file-name.msft.png":::
         Copier le nom du fichier dans les **sources**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-copy-file-name.msft.png" alt-text="Copier le nom de fichier dans le volet Styles" lightbox="../../media/2021/01/elements-styles-copy-file-name.msft.png":::
         Copier le nom de fichier dans **le volet Styles**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### Mises à jour des détails du cadre  

#### Informations sur les employés de service dans les détails de l’image  

DevTools répertorie désormais un service de travail dédié sous le cadre parent.  Dans la figure suivante, les détails du service de travail sont affichés.  Pour afficher les détails du travail de service, accédez aux travailleurs du service Cadres **d’application,**  >  ****  >  `top`  >  **** puis choisissez un service de travail.  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1122507][CR1122507].  

:::image type="complex" source="../../media/2021/01/application-frames-service-workers-details.msft.png" alt-text="Informations sur les employés de service dans les détails des cadres" lightbox="../../media/2021/01/application-frames-service-workers-details.msft.png":::
   **Informations sur les employés** de service dans les **détails des** cadres  
:::image-end:::  

#### Mesurer les informations de mémoire dans les détails de l’image  

`performance.measureMemory()`L’état de l’API s’affiche désormais sous la section **disponibilité de l’API.**  La nouvelle `performance.measureMemory()` API estime l’utilisation de la mémoire de la page web entière.  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1139899][CR1139899].  

:::image type="complex" source="../../media/2021/01/application-frames-measure-memory.msft.png" alt-text="Mesurer la mémoire" lightbox="../../media/2021/01/application-frames-measure-memory.msft.png":::
   Mesurer la mémoire  
:::image-end:::  

### Images abandonnées dans l’outil Performances  

Lorsque vous [analysez les performances de chargement dans l’outil Performance,][DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]la section **Frames** marque désormais les images abandonnées en rouge.  Pour afficher la fréquence d’images, pointez sur une image abandonnée.  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au [problème 1075865][CR1075865].  

:::image type="complex" source="../../media/2021/01/performance-frames-dropped-frames-red.msft.png" alt-text="Cadres supprimés" lightbox="../../media/2021/01/performance-frames-dropped-frames-red.msft.png":::
   Cadres supprimés  
:::image-end:::  

#### Nouveau calcul de contraste de couleur - Algorithme de contraste perceptif avancé (APCA)  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

[L’algorithme de contraste perceptif avancé (APCA)][GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml] remplace le coefficient de contraste des recommandations [][W3cWaiWcag21QuickrefContrastMinimum] / [AA AAA][W3cWaiWcag21QuickrefContrastEnhanced] dans le [s picker de couleur.][DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]  APCA est une nouvelle façon de calculer le contraste.  Il est basé sur des recherches modernes sur la perception des couleurs.  Par rapport aux directives AA/AAA, APCA dépend davantage du contexte.  Le contraste est calculé en fonction des propriétés spatiales suivantes du texte, de la couleur et du contexte.  

*   Propriétés spatiales du texte qui incluent le poids et la taille de la police.  
*   Propriétés spatiales de couleur qui incluent le contraste perçu entre le texte et l’arrière-plan.  
*   Propriétés spatiales du contexte qui incluent la lumière ambiante, l’environnement et l’objectif prévu.  
    
Pour activer cette expérience, accédez à Expériences de paramètres et cochez la case en regard de Activer le nouvel algorithme de contraste perceptif avancé (APCA) en remplaçant le coefficient de contraste précédent et les [directives][DevtoolsCustomizeIndexSettings]  >  **** **AA/AAA.**  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1121900][CR1121900].  

:::image type="complex" source="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png" alt-text="APCA dans le s picker de couleurs" lightbox="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png":::
   APCA dans le s picker de couleurs  
:::image-end:::  

## Télécharger les canaux d’aperçu Microsoft Edge  

Si vous utilisez Windows, Linux ou macOS, envisagez d’utiliser les canaux d’aperçu [Microsoft Edge][MicrosoftEdgePreviewChannels] comme navigateur de développement par défaut.  Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.  

## Contacter l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew85]: ../../2020/06/devtools.md "Nouveautés de DevTools (Microsoft Edge 85) | Documents Microsoft"  

[DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]: /microsoft-edge/devtools-guide-chromium/accessibility/reference#view-the-contrast-ratio-of-a-text-element-in-the-color-picker "Afficher le coefficient de contraste d’un élément de texte dans le s picker de couleurs - Référence d’accessibilité | Documents Microsoft"  
[DevtoolsCssReferenceChangeCss]: /microsoft-edge/devtools-guide-chromium/css/reference#change-css "Modifier la référence CSS - CSS | Documents Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCustomizeShortcuts]: microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personnaliser les raccourcis clavier dans l'| Microsoft Edge DevTools Documents Microsoft"  
[DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/device-mode/dual-screen-and-foldables#testing-on-foldable-and-dual-screen-devices "Test sur les appareils pliables et à double écran : émuler les appareils à double écran et pliables dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Émuler des appareils mobiles dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simuler une port d’affichage mobile : émuler des appareils mobiles dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-load-performance "Performances de charge d’enregistrement : référence de l’analyse des performances | Documents Microsoft"  
[DevtoolsInspectStylesEditFonts]: /microsoft-edge/devtools-guide-chromium/inspect-styles/edit-fonts "Modifier les styles et paramètres de police CSS dans le volet Styles de DevTools | Documents Microsoft"  
[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium/index "Présentation des outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  

[DualScreenIntroductionHowToWorkWithSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Comment travailler avec le seam : introduction aux appareils à double écran | Documents Microsoft"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Fonctionnalité d’écran multimédia CSS pour la détection à double écran | Documents Microsoft"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "L’API JavaScript getWindowSegments pour les appareils à double écran | Documents Microsoft"  

[GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1]: https://microsoftedge.github.io/DevToolsSamples/whats-new/89/target-css-demo.html#section-1 "Section 1 - Démonstration CSS :target pour les nouveautés de DevTools (Microsoft Edge 89) | GitHub"  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull229]: https://github.com/microsoft/vscode-edge-devtools/pull/229 "Pull 229 : mise en œuvre de la dropdown dans les paramètres pour modifier les thèmes | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull233]: https://github.com/microsoft/vscode-edge-devtools/pull/233 "Pull 233 : inclure le débogger pour Microsoft Edge en tant que | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull235]: https://github.com/microsoft/vscode-edge-devtools/pull/235 "Pull 235 : mise à niveau de la version Edge DevTools vers 85.0.564.40 | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull248]: https://github.com/microsoft/vscode-edge-devtools/pull/248 "Pull 248 : ajouter des boutons de fermeture unique au panneau instances | GitHub"  
[GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml]: https://w3c.github.io/silver/guidelines/methods/Method-font-characteristic-contrast.html "Sélectionnez les caractéristiques de police et les couleurs d’arrière-plan pour fournir un contraste suffisant pour une | W3C"  
[GithubW3cWebappsecTrustedTypesDistSpec]: https://w3c.github.io/webappsec-trusted-types/dist/spec  "Types d'| W3C"  

[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Nouveau modèle Surface Duo | Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux d’aperçu Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Mettre à jour une extension manuellement - Extension Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Outils Microsoft Edge pour Visual Studio code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Débogger pour Microsoft Edge | Visual Studio Marketplace"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bogues Chromium"  
[CR978059]: https://crbug.com/978059 "Problème 978059 : suppression des cookies lors de leur filtrage, supprimez tous les cookies et pas seulement ceux filtrés | Bogues Chromium"  
[CR997625]: https://crbug.com/997625 "Problème 997625 : nouvelle fonctionnalité req | Option nécessaire pour afficher la valeur décodée url dans les cookies | Bogues Chromium"  
[CR1003629]: https://crbug.com/1003629 "Problème 1003629 : le nœud de capture ne capture plus le nœud sous la pliage. | Bogues Chromium"  
[CR1012337]: https://crbug.com/1012337 "Problème 1012337 : effacer les données de site détruit une session Google sur des sites autres que Google | Bogues Chromium"  
[CR1028078]: https://crbug.com/1028078 "Problème 1028078 : Mettre en ligne et hors connexion les uns à côté des autres dans la liste | Bogues Chromium"  
[CR1054281]: https://crbug.com/1054281 "Problème 1054281 : Demande de fonctionnalité : DevTools doit émuler les appareils pliables et à double écran | Bogues Chromium"  
[CR1075865]: https://crbug.com/1075865 "Problème 1075865 : afficher les images abandonnées dans la chronologie des devtools | Bogues Chromium"  
[CR1093229]: https://crbug.com/1093229 "Problème 1093229 : DevTools : offre une interface utilisateur d’éditeur de police spécialisée | Bogues Chromium"  
[CR1121900]: https://crbug.com/1121900 "Problème 1121900 : DevTools : mettre à jour la logique de calcul du contraste par nouvelle spécification | Bogues Chromium"  
[CR1122507]: https://crbug.com/1122507 "Problème 1122507: Informations sur le travailleur de surface dans l’affichage de l’arborescence de cadre | Bogues Chromium"  
[CR1122580]: https://crbug.com/1122580 "Problème 1122580 : Impossible de désactiver l’enregistrement réseau lors du rechargement | Bogues Chromium"  
[CR1136394]: https://crbug.com/1136394 "Problème 1136394: outils Flexbox | Bogues Chromium"  
[CR1139899]: https://crbug.com/1139899 "Problème 1139899: Signaler la disponibilité des API contrôlées dans l’affichage des détails du cadre | Bogues Chromium"  
[CR1139949]: https://crbug.com/1139949 "Problème 1139949 : superposition flexbox | Bogues Chromium"  
[CR1147016]: https://crbug.com/1147016 "Problème 1147016 : le s sélectionneur de couleurs n’est pas affiché dans la fonction var(). | Bogues Chromium"  
[CR1148353]: https://crbug.com/1148353 "Problème 1148353 : Demande de fonctionnalité : copier l’objet à partir de la console devtools | Bogues Chromium"  
[CR1149859]: https://crbug.com/1149859 "Problème 1149859: [feature request][Console] add copy object to clipboard item to contextual menu | Bogues Chromium"  
[CR1150797]: https://crbug.com/1150797 "Problème 1150797 : ajouter un menu contextif d’élément dupliqué dans le panneau d'| Bogues Chromium"  
[CR1152391]: https://crbug.com/1152391 "Problème 1152391 : prise en charge de la copie du menu contextux CSS dans le panneau de styles | Bogues Chromium"  
[CR1155120]: https://crbug.com/1155120 "Problème 1155120 : [FR]Nom du fichier de copie de support et numéro de ligne | Bogues Chromium"  
[CR1156628]: https://crbug.com/1156628 "Problème 1156628 : DevTools : ajoutez la prise en charge de la fonctionnalité d’état d’élément :target en force | Bogues Chromium"  
[CR1157329]: https://crbug.com/1157329 "Problème 1157329 : Accessibilité - Narrateur : le Narrateur n’annonce pas le nombre et la position des suggestions disponibles pour le code dans l’onglet Styles | Bogues Chromium"  

[MdnDocsWebCssTarget]: https://developer.mozilla.org/docs/web/css/:target ":target | MDN"  

[SamsungUsMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "| Samsung (États-Unis)"  

[W3cWaiWcag21QuickrefContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref#contrast-enhanced "Contraste (amélioré) : comment répondre aux exigences WCAG (référence rapide) | W3C"  
[W3cWaiWcag21QuickrefContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref#contrast-minimum "Contraste (minimum) : comment répondre aux exigences WCAG (référence rapide) | W3C"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/updates/2021/01/devtools/index) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen

[SpanningPlaceholder]: link-t-b-d "Espace réservé couvrant"  
