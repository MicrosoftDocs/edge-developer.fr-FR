---
description: L’outil Nouveautés s’appelle à présent Welcome (Bienvenue), éditeur de polices visuelles dans le volet Styles, outils de débogage CSS Flexbox, et bien plus encore.
title: Nouveautés de DevTools (Microsoft Edge89)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.localizationpriority: high
ms.openlocfilehash: ec14d802af52c0bb2e658549f48764279c787f47
ms.sourcegitcommit: de75fda30bb8964e9a184228d068b4402ec59c3e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "11514367"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-89"></a>Nouveautés de DevTools (Microsoft Edge89)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="whats-new-is-now-welcome"></a>Nouveautés s’appelle à présent Welcome (Bienvenue)  

<!--  Title: What's New is now Welcome  -->  
<!--  Subtitle: The What's New tool now has a new appearance and a new name:  Welcome -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

**L’outil Nouveautés** de Microsoft Edge DevTools a à présent une nouvelle apparence et un nouveau nom: **Welcome**.  L’outil **Welcome ** affiche toujours les dernières actualités et mises à jour DevTools.  Il inclut à présent également des liens vers la documentation de Microsoft Edge DevTools, des méthodes d’envoi de commentaires, et bien plus encore.  Pour afficher l’outil **Welcome** après chaque mise à jour de Microsoft Edge, cochez la case en regard de l’**onglet Ouvrir après chaque mise à jour** sous le titre.  Pour fermer **l’outil Welcome,** choisissez le **X** sur le côté droit du titre de l’onglet.  Si vous préférez l’outil **Nouveautés** d’origine, accédez à [Paramètres][DevtoolsCustomizeIndexSettings] > **Expériences**, puis décochez la case en regard de l’option **Enable Welcome tab**.  

:::image type="complex" source="../../media/2021/01/welcome-tool-whats-new-88.msft.png" alt-text="L’outil Welcome apparaît en surbrillance." lightbox="../../media/2021/01/welcome-tool-whats-new-88.msft.png":::
   **L’outil Welcome** apparaît en surbrillance  
:::image-end:::  

## <a name="visual-font-editor-in-the-styles-pane"></a>Éditeur de polices dans le volet Styles  

<!--  Title: Visual font editor in the Styles pane  -->  
<!--  Subtitle: Visual font editor in the Styles pane -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Lorsque vous utilisez des polices dans CSS, utilisez le nouvel [éditeur de polices][DevtoolsInspectStylesEditFonts] visuelles.  Vous pouvez définir des polices de secours, puis utiliser des curseurs pour définir le poids, la taille, la hauteur de ligne et l’espacement de la police.  **L’éditeur de polices** vous permet d’effectuer les actions suivantes.  

*   Basculer entre les unités concernant différentes propriétés de police  
*   Basculer entre les mots clés de différentes propriétés de police  
*   Convertir des unités  
*   Générer un code CSS précis  
    
Pour activer cette expérience, accédez à [Paramètres][DevtoolsCustomizeIndexSettings] > **Expériences**, puis cochez la case à cocher en regard de l’option **Enable new Font Editor tools within Styles pane**.  Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Modifier les styles et paramètres de police CSS dans le volet Styles de DevTools][DevtoolsInspectStylesEditFonts].  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1093229][CR1093229].  

:::image type="complex" source="../../media/2021/01/visual-font-editor.msft.png" alt-text="L’éditeur de polices visuelles apparaît en surbrillance dans le volet Styles" lightbox="../../media/2021/01/visual-font-editor.msft.png":::
   L’éditeur **de polices visuelles** apparaît en surbrillance dans le volet **Styles**  
:::image-end:::  

## <a name="css-flexbox-debugging-tools"></a>Outils de débogage CSS Flexbox  

Les fonctionnalités de débogage Flexbox sont en cours de développement.  Pour activer l’expérience des deux fonctionnalités suivantes, accédez à [Paramètres][DevtoolsCustomizeIndexSettings] > ** Expériences**, puis cochez la case à cocher en regard de l’option **Enable new CSS Flexbox debugging features**.  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez aux problèmes [1136394][CR1136394] et [1139949][CR1139949].  

### <a name="new-flexbox-flex-icon-helps-identify-and-display-flex-containers"></a>La nouvelle icône Flexbox (flex) permet d’identifier, puis d’afficher les conteneurs flex  

<!--  Title: Display Flexbox containers with Flexbox (flex) icon  -->  
<!--  Subtitle: New Flexbox (flex) icon in the Elements tool help you identify Flexbox containers in your code.  When toggled, the adorner displays and hides outlines of the flex container to help you debug the layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Dans l’outil **Éléments**, la nouvelle icône Flexbox (flex) vous permet d’identifier les conteneurs Flexbox dans votre code.  Sélectionnez l’icône Flexbox \(flex\) pour activer ou désactiver l’effet de superposition qui met en relief un conteneur Flexbox.  Vous pouvez personnaliser la couleur de la superposition dans le volet **Layout** (Mise en page) qui se trouve à côté de **Styles** et **Computed** (Calculé).  

:::row:::
   :::column span="":::
      Pour activer et désactiver l’effet de superposition qui met en relief le conteneur Flexbox, choisissez l’icône Flexbox \(`flex`\).  
   :::column-end:::
   :::column span="":::
      Vous pouvez personnaliser la couleur de la superposition dans le volet **Layout** situé à côté de **Styles** et **Computed**.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container.msft.png" alt-text="Icône Flexbox (flex) et page web en surbrillance" lightbox="../../media/2021/01/elements-flex-container.msft.png":::
         Icône **Flexbox** \(`flex`\) et page web en surbrillance :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-layout-flex-container.msft.png" alt-text="Superpositions Flexbox mises en évidence dans le volet Layout" lightbox="../../media/2021/01/elements-layout-flex-container.msft.png":::
         **Superpositions Flexbox mises** en évidence dans le volet **Disposition**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-alignment-icons-and-visual-guides-when-flexbox-layouts-change-using-css-properties"></a>Afficher les icônes d’alignement et les guides visuels lorsque les dispositions de Flexbox changent à l’aide des propriétés CSS  

<!--  Title: Display alignment icons and visual guides for changes to Flexbox layouts from CSS properties  -->  
<!--  Subtitle:  CSS autocomplete in the Styles tool now displays icons next to Flexbox properties to help you review the effect a property has on your Flexbox layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Lorsque vous modifiez des CSS pour votre disposition Flexbox, le menu de remplissage automatique des CSS disponible dans le volet **Styles** affiche à présent des icônes utiles en regard des propriétés Flexbox concernées.  Pour essayer cette nouvelle fonctionnalité, ouvrez l’outil **Éléments**, puis sélectionnez un conteneur flex.  Ensuite, ajoutez ou modifiez une propriété sur ce conteneur dans le volet **Styles**.  

:::row:::
   :::column span="":::
      Le menu de remplissage automatique affiche à présent des icônes qui indiquent l’effet des propriétés d’alignement telles que `align-content` et `align-items`.  
   :::column-end:::
   :::column span="":::
      De plus, DevTools affiche à présent une ligne d’instructions pour vous aider à mieux examiner la propriété CSS `align-items`.  Nous prenons également en charge la propriété CSS `gap`.  Dans la figure suivante, la propriété CSS `gap` est définie sur `gap: 12px;`, et le modèle de hachurage de chaque intervalle s’affiche.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align.msft.png" alt-text="Menu de remplissage automatique mis en surbrillance pour les propriétés CSS qui commencent par align-" lightbox="../../media/2021/01/elements-flex-container-align.msft.png":::
         Menu de remplissage automatique mis en surbrillance pour les propriétés CSS qui commencent par `align-`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png" alt-text="Espace flexbox dans les propriétés CSS et page web en surbrillance" lightbox="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png":::
         Flexbox `gap` dans les propriétés CSS et la page web en surbrillance  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="add-tools-quickly-with-new-more-tools-button"></a>Ajouter rapidement des outils avec le nouveau bouton More Tools (Plus d’outils).  

<!--  Title: Add tools quickly with new More Tools button  -->  
<!--  Subtitle: A convenient way to open new tools in Microsoft Edge DevTools -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Vous avez maintenant une nouvelle façon d’ouvrir d’autres outils dans Microsoft Edge DevTools.  Une fois que vous avez activé cette expérience, l’icône **More Tools** s’affiche sous la forme d’un signe plus (`+`) à droite du panneau principal.  Pour afficher la liste des autres outils à ajouter au panneau principal, sélectionnez l’icône **More Tools** \(`+`\).  Pour activer cette expérience, accédez à [Paramètres][DevtoolsCustomizeIndexSettings] > **Expériences**, puis cochez la case à cocher en regard de l’option **Enable + button tab menus to open more tools**.  

:::image type="complex" source="../../media/2021/01/more-tools.msft.png" alt-text="Autres outils mis en évidence dans DevTools" lightbox="../../media/2021/01/more-tools.msft.png":::
   **Autres outils** mis en évidence dans DevTools  
:::image-end:::  

## <a name="assistive-technologies-now-announce-position-and-count-of-css-suggestions"></a>Les technologies d’assistance annoncent à présent la position et le nombre de suggestions CSS  

<!--  Title: Assistive technologies now announce position and count of CSS suggestions  -->  
<!--  Subtitle: CSS suggestions are now easier to navigate using screen readers -->  

Lorsque vous modifiez des CSS, un menu déroulant de fonctionnalités s’affiche.  Cette fonctionnalité n’était pas disponible pour les utilisateurs de technologies d’assistance, car elle est annoncée dans Microsoft Edge version89.  Un utilisateur de technologies d’assistance peut à présent parcourir les suggestions CSS dans le volet **Styles**.  Dans Microsoft Edge version88 et les versions antérieures, la technologie d’assistance annoncée en tant qu’utilisateur a accédé à la liste des suggestions lors de la modification de CSS dans le volet `Suggestion` **Styles**.  Dans Microsoft Edge version89, un utilisateur de technologie d’assistance entend à présent la position et le nombre de suggestions actuelles.  Le programme annonce chaque suggestion lorsque l’utilisateur navigue dans la liste des suggestions, telles que la suggestion3 sur 5.  Si vous souhaitez en savoir plus sur l’écriture de CSS dans DevTools, veuillez consulter la rubrique [Modifier des CSS][DevtoolsCssReferenceChangeCss].  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1157329][CR1157329].  

Pour visionner une vidéo qui affiche, puis lit à voix haute plusieurs suggestions avec cette expérience activée, accédez à [Voiceover announcing devtools options](https://youtu.be/9TcUpleEwwA) sur YouTube.  

:::image type="complex" source="../../media/2021/01/announce-css-suggestion.msft.png" alt-text="Suggestion mise en évidence dans le volet Styles" lightbox="../../media/2021/01/announce-css-suggestion.msft.png":::
   `suggestion`Liste mise en évidence dans le volet **Styles**  
:::image-end:::  

## <a name="emulate-surface-duo-and-samsung-galaxy-fold"></a>Émuler Surface Duo et Samsung Galaxy Fold  

<!--  Title: Emulate new dual-screen and foldable devices  -->  
<!--  Subtitle: Test the appearance and feel of your website or app with Surface Duo and Samsung Galaxy Fold emulators -->  

Testez l’apparence de votre site web ou de votre application sur les appareils suivants dans Microsoft Edge.  

*   [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo]  
*   [Samsung Galaxy Fold][SamsungUsMobileGalaxyFold]  
    
Activez les **fonctionnalités de plateforme Web expérimentale** pour accéder à la nouvelle [fonctionnalité couvrant l’écran multimédia CSS][DualScreenWebCssMediaSpanning] et à l’[API JavaScript getWindowSegments][DualScreenWebJavascriptGetwindowsegments].  Accédez à `edge://flags`, puis basculez l’indicateur à côté des **fonctionnalités de plateforme Web expérimentale**.  Pour contribuer à améliorer votre site web ou votre application pour les appareils à double écran et pliables, utilisez les fonctionnalités suivantes lors de [l’émulation de l’appareil][DevtoolsDeviceModeIndex].  

*   [Couvrant,][DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices], c’est-à-dire lorsque votre site web \(ou application\) apparaît sur les deux écrans.  
*   [Rendu de la jointure][DualScreenIntroductionHowToWorkWithSeam], à savoir l’espace entre les deux écrans.  
    
Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1054281][CR1054281].  

:::image type="complex" source="../../media/2021/01/emulate-surface-device-surface-duo.msft.png" alt-text="Émuler double écran" lightbox="../../media/2021/01/emulate-surface-device-surface-duo.msft.png":::
   Émuler double écran  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-112"></a>Microsoft Edge Developer Tools pour Visual Studio Code version1.1.2  

L’extension [Microsoft Edge Developer Tools pour Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] version1.1.2 pour Microsoft Visual Studio Code comporte les modifications suivantes depuis la version précédente.  Microsoft Visual Studio Code met automatiquement à jour les extensions.  Pour effectuer manuellement la mise à jour vers la version1.1.2, accédez à [Mettre à jour une extension manuellement][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].  

*   Ajout d’un bouton **Close instance** (Fermer l’instance) à chaque élément de la liste cible \([#248][GithubMicrosoftVscodeEdgeDevtoolsPull248]\)  
*   Passage de [Microsoft Edge DevTools][DevtoolsMain] version84.0.522.63 à la version[85.0.564.40][DevtoolsWhatsNew85] \([#235][GithubMicrosoftVscodeEdgeDevtoolsPull235]\)  
*   Inclusion du [débogueur de Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge] en tant que dépendance \([#233][GithubMicrosoftVscodeEdgeDevtoolsPull233]\)  
*   Implémentation de l’option de paramètres pour modifier les thèmes d’extension \([#229][GithubMicrosoftVscodeEdgeDevtoolsPull229]\)  
    
Vous pouvez signaler des problèmes, puis contribuer à l’extension sur le référentiel [GitHub vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools].  

## <a name="announcements-from-the-chromium-project"></a>Annonces du projet de Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="capture-node-screenshot-beyond-viewport"></a>Capture d’écran du nœud au-delà de la fenêtre d’affichage  

Dans Microsoft Edge version89, les captures d’écran de nœud sont plus précises. Cela permet de capturer le nœud complet même si le contenu du nœud n’est pas visible dans la fenêtre d’affichage.  Dans l’outil **Éléments**, placez le curseur sur un élément, ouvrez le menu contextuel \(clic droit\), puis choisissez **Capture node screenshot** (Capture d’écran du nœud).  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1003629][CR1003629].  

:::image type="complex" source="../../media/2021/01/capture-node-screenshot.msft.png" alt-text="Capture d’écran du nœud mise en évidence dans le menu contextuel de l’outil Éléments" lightbox="../../media/2021/01/capture-node-screenshot.msft.png":::
   **Capture d’écran du nœud** mise en évidence dans le menu contextuel de l’outil **Éléments**  
:::image-end:::  

### <a name="elements-tool-updates"></a>Mises à jour de l’outil Éléments  

#### <a name="support-forcing-the-target-css-state"></a>Prise en charge du forçage de l’état CSS :target (cible)  

Vous pouvez à présent utiliser DevTools pour forcer la pseudo-classe CSS [:target][MdnDocsWebCssTarget].  La pseudo-classe `:target`se déclenche lorsqu’un élément unique \(l’élément cible\) comporte un élément `id` qui correspond à un fragment de l’URL.  Par exemple, l’URL `http://www.example.com/index.html#section1` déclenche la pseudo-classe `:target` sur un élément HTML avec `id="section1"`.  Pour essayer une démonstration avec la section1 mise en évidence, accédez à [CSS :target demo][GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1] (Démo :target CSS).  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1156628][CR1156628].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-none-forced.msft.png" alt-text="Page web en surbrillance sans CSS forcé" lightbox="../../media/2021/01/elements-styles-none-forced.msft.png":::
         Page web mise en surbrillance sans CSS forcé  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-target-forced.msft.png" alt-text="CSS :target forcé et page web mise en surbrillance" lightbox="../../media/2021/01/elements-styles-target-forced.msft.png":::
         `:target` CSS forcé et page web mise en surbrillance  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### <a name="use-duplicate-elements-to-copy-elements"></a>Utiliser des éléments en double pour copier des éléments  

Utilisez le nouveau raccourci **Dupliquer l’élément** pour cloner un élément.  Dans **l’outil Éléments**, placez le curseur sur un élément, ouvrez le menu contextuel \(clic droit\), puis choisissez **Dupliquer l’élément**.  Le programme crée un nouvel élément sous l’élément sélectionné.  Pour dupliquer l’élément avec un raccourci clavier, sélectionnez `Shift` + `Alt` + `Down Arrow` \(Windows/Linux\) ou `Shift` + `Option` + `Down Arrow` \(macOS\).  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1150797][CR1150797].  

:::image type="complex" source="../../media/2021/01/elements-duplicate-element.msft.png" alt-text="L’élément en double apparaît en surbrillance dans le menu contextuel d’un élément de l’outil Éléments" lightbox="../../media/2021/01/elements-duplicate-element.msft.png":::
   L’**élément en double** apparaît en surbrillance dans le menu contextuel d’un élément de l’outil **Éléments**  
:::image-end:::  

#### <a name="color-pickers-for-custom-css-properties"></a>Sélecteurs de couleurs pour les propriétés CSS personnalisées  

Le **volet Styles** affiche à présent les sélecteurs de couleur pour les propriétés CSS personnalisées.  Pour faire défiler les formats RGBA, HSLA et Hex de la valeur de couleur, maintenez la touche `Shift` enfoncée, puis choisissez le sélecteur de couleurs.  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1147016][CR1147016].  

:::image type="complex" source="../../media/2021/01/elements-styles-change-color-format.msft.png" alt-text="Sélecteurs de couleurs pour les propriétés CSS personnalisées" lightbox="../../media/2021/01/elements-styles-change-color-format.msft.png":::
   Sélecteurs de couleurs pour les propriétés CSS personnalisées  
:::image-end:::  

#### <a name="copy-css-classes-and-properties"></a>Copier les classes et propriétés CSS  

Vous pouvez maintenant copier plus rapidement les propriétés CSS avec quelques nouvelles options dans le menu contextuel.  Dans l’outil **Elements**, choisissez un élément.  Pour copier la valeur, dans le volet **Styles**, placez le curseur sur une classe CSS ou une propriété CSS, ouvrez un menu contextuel \(clic droit\), puis choisissez l’option de copie.  

:::row:::
   :::column span="":::
      Options de copie d’une classe CSS.  
      
      | Option | Détails |  
      |:--- |:--- |  
      | **Copy selector (Copier le sélecteur)** | Copiez le nom du sélecteur actuel. |  
      | **Copy rule (Copier la règle)** | Copiez la règle du sélecteur actuel. |  
      | **Copy all declarations (Copier toutes les déclarations)** | Copiez toutes les déclarations sous la règle actuelle, y compris les propriétés non valides et préfixées. |  
   :::column-end:::
   :::column span="":::
      Options de copie d’une propriété CSS.  
      
      | Option | Détails |      
      |:--- |:--- |  
      | **Copy declaration (Copier la déclaration)** | Copiez la déclaration de la ligne actuelle. |  
      | **Copy property (Copier la propriété)** | Copiez la propriété de la ligne actuelle. |  
      | **Copy value (Copier la valeur)** | Copiez la valeur de la ligne actuelle. |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-class.msft.png" alt-text="Options de copie d’une classe CSS dans le menu contextuel" lightbox="../../media/2021/01/copy-css-class.msft.png":::
         Options de copie d’une classe CSS dans le menu contextuel  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-property-cropped.msft.png" alt-text="Options de copie d’une propriété CSS dans le menu contextuel" lightbox="../../media/2021/01/copy-css-property.msft.png":::
         Options de copie d’une propriété CSS dans le menu contextuel  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1152391][CR1152391].  

### <a name="cookies-updates"></a>Mises à jour des cookies  

#### <a name="new-option-to-display-url-decoded-cookies"></a>Nouvelle option d’affichage des cookies décodés par l’URL  

Vous pouvez à présent choisir d’afficher la valeur des cookies décodés par l’URL dans le **volet Cookies**.  Pour afficher le cookie décodé, accédez au volet **Application** > **Cookies**, choisissez un cookie dans la liste, puis cochez la case en regard de l’option **Show URL decoded** (Afficher l’URL décodée).  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au [problème 997625][CR997625].  

:::image type="complex" source="../../media/2021/01/application-cookies-show-url-decoded.msft.png" alt-text="Option d’affichage des cookies décodés par l’URL" lightbox="../../media/2021/01/application-cookies-show-url-decoded.msft.png":::
   Option d’affichage des cookies décodés par l’URL  
:::image-end:::  

#### <a name="filter-and-clear-visible-cookies"></a>Filtrer et effacer les cookies visibles  

Dans Microsoft Edge version88 ou antérieures, l’outil **Application** fournissait uniquement un moyen d’effacer tous les cookies avec le bouton **Clear all cookies** (Effacer tous les cookies).  Dans Microsoft Edge version89, vous pouvez à présent choisir **Clear filtered cookies** (Effacer les cookies filtrés) pour supprimer uniquement les cookies filtrés.  Pour filtrer les cookies, accédez à **Application** > **Cookies**, puis tapez votre texte dans la zone de texte **Filter** (Filtrer).  Pour supprimer les cookies affichés, sélectionnez le bouton **Clear filtered cookies** (Effacer les cookies filtrés).  Pour afficher tous les autres cookies, effacer le texte du filtre.  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [978059][CR978059].  

:::image type="complex" source="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png" alt-text="Effacer uniquement les cookies visibles" lightbox="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png":::
   Effacer uniquement les cookies visibles  
:::image-end:::  

#### <a name="new-option-to-clear-third-party-cookies-in-the-storage-pane"></a>Nouvelle option d’effacement des cookies tiers dans le volet Storage (Stockage)  

DevTools n’efface à présent que les cookies internes par défaut.  Pour effacer uniquement les données de site web et les cookies internes, accédez à **Application** > **Storage** (Stockage), puis choisissez **Clear site data** (Effacer les données du site).  

Pour effacer les données de site web et tous les cookies, accédez à **Application** > **Storage**.  Cochez la case en regard de l’option **including third-party cookies** (même les cookies tiers), puis sélectionnez **Clear site data**.  

Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1012337][CR1012337].  

:::image type="complex" source="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png" alt-text="Option d’effacement des cookies tiers" lightbox="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png":::
   Option d’effacement des cookies tiers  
:::image-end:::  

### <a name="network-tool-updates"></a>Mises à jour de l’outil réseau  

#### <a name="persist-record-network-log-setting"></a>Conserver le paramètre Enregistrer le journal de réseau  

Dans Microsoft Edge version88 ou antérieure, DevTools réinitialise le paramètre **Enregistrer le journal de réseau** lors de l’actualisation d’une page web.  Dans Microsoft Edge version89, DevTools conserve à présent le paramètre **Enregistrer le journal de réseau**.  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1122580][CR1122580].  

:::image type="complex" source="../../media/2021/01/network-log.msft.png" alt-text="Enregistrer le journal de réseau" lightbox="../../media/2021/01/network-log.msft.png":::
   Enregistrer le journal de réseau  
:::image-end:::  

#### <a name="online-option-is-now-no-throttling-option"></a>L’option En ligne est à présent l’option Pas de limitation  

L’option d’émulation du réseau **En ligne** est à présent renommée **No Pas de limitation**.  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1028078][CR1028078].  

:::image type="complex" source="../../media/2021/01/network-no-throttling.msft.png" alt-text="Option Pas de limitation" lightbox="../../media/2021/01/network-no-throttling.msft.png":::
   Option **Pas de limitation**  
:::image-end:::  

### <a name="new-copy-options-in-the-console-tool-sources-tool-and-styles-pane"></a>Nouvelles options de copie de l’outil Console, de l’outil Sources et du volet Styles

#### <a name="copy-object-in-the-console-and-sources-tool"></a>Copier l’objet dans l’outil Console et Sources  

Vous pouvez maintenant copier des valeurs d’objet dans les outils **Console** et **Sources**.  La possibilité de copier des valeurs d’objet est utile lorsque vous travaillez avec des objets de grande taille.  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez aux problèmes [1148353][CR1148353] et [1149859][CR1149859].  

:::row:::
   :::column span="":::
      Dans l’outil **Console**, placez le curseur sur un objet, ouvrez le menu contextuel \(clic droit\), puis choisissez **Copier l’objet**.  
   :::column-end:::
   :::column span="":::
      Dans l’outil **Sources,** sur un point d’arrêt, placez le curseur sur un objet, dans la fenêtre contextuelle **Objet**, surlignez un objet, ouvrez le menu contextuel \(clic droit\), puis choisissez **Copier l’objet**.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/console-copy-object.msft.png" alt-text="Copier l’objet dans la console" lightbox="../../media/2021/01/console-copy-object.msft.png":::
         Copier l’objet dans la **console**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png" alt-text="Copier l’objet dans les sources" lightbox="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png":::
         Copier l’objet dans les **sources**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="copy-file-name-in-the-sources-tool-and-styles-pane"></a>Copier le nom du fichier dans l’outil Sources et le volet Styles  

Vous pouvez à présent copier un nom de fichier à l’aide du menu contextuel.  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez à Problèmes [1155120][CR1155120].  

:::row:::
   :::column span="":::
      Dans l’outil **Sources,**, placez le curseur sur un nom de fichier, ouvrez le menu contextuel \(clic droit\), puis choisissez **Copier le nom du fichier.**  
   :::column-end:::
   :::column span="":::
      Dans l’outil **Éléments** > volet **Styles**, placez le curseur sur un nom de fichier, ouvrez le menu contextuel \(clic droit\), puis choisissez **Copier le nom du fichier**.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-copy-file-name.msft.png" alt-text="Copier le nom du fichier dans les sources" lightbox="../../media/2021/01/sources-copy-file-name.msft.png":::
         Copier le nom du fichier dans les **sources**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-copy-file-name.msft.png" alt-text="Copier le nom du fichier dans le volet Styles" lightbox="../../media/2021/01/elements-styles-copy-file-name.msft.png":::
         Copier le nom du fichier dans le volet **Styles**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="updates-to-frame-details"></a>Mises à jour des détails du cadre  

#### <a name="service-workers-information-in-frame-details"></a>Informations Workers du service dans les détails du cadre  

DevTools répertorie à présent un Worker du service dédié sous le cadre parent.  Dans la figure suivante, les détails du Worker du service s’affichent.  Pour afficher les détails du Worker du service, accédez à **Application** > **Cadres** > `top` > **Workers du service**, puis choisissez un Worker du service.  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1122507][CR1122507].  

:::image type="complex" source="../../media/2021/01/application-frames-service-workers-details.msft.png" alt-text="Informations sur les Workers du service dans les détails de Cadres" lightbox="../../media/2021/01/application-frames-service-workers-details.msft.png":::
   Informations sur les **Workers du service** dans les détails de **Cadres**  
:::image-end:::  

#### <a name="measure-memory-information-in-frame-details"></a>Mesurer les informations de mémoire dans les détails du cadre  

L’état de l’API `performance.measureMemory()` s’affiche à présent sous la section **Disponibilité de l’API**.  La nouvelle API `performance.measureMemory()` estime l’utilisation de la mémoire de la page web entière.  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1139899][CR1139899].  

:::image type="complex" source="../../media/2021/01/application-frames-measure-memory.msft.png" alt-text="Mesurer la mémoire" lightbox="../../media/2021/01/application-frames-measure-memory.msft.png":::
   Mesurer la mémoire  
:::image-end:::  

### <a name="dropped-frames-in-the-performance-tool"></a>Cadres supprimés dans l’outil Performances  

Lorsque vous [analysez les performances de charge dans l’outil Performance][DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance], la section **Cadres** marque à présent les cadres supprimés en rouge.  Pour afficher la fréquence d’images, placez le curseur sur un cadre supprimé.  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1075865][CR1075865].  

:::image type="complex" source="../../media/2021/01/performance-frames-dropped-frames-red.msft.png" alt-text="Cadres supprimés" lightbox="../../media/2021/01/performance-frames-dropped-frames-red.msft.png":::
   Cadres supprimés  
:::image-end:::  

#### <a name="new-color-contrast-calculation---advanced-perceptual-contrast-algorithm-apca"></a>Nouveau calcul de contraste de couleur - Advanced Perceptual Contrast Algorithm (APCA)  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

L’algorithme [Advanced Perceptual Contrast Algorithm (APCA)][GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml] remplace le taux de contraste des recommandations [AA][W3cWaiWcag21QuickrefContrastMinimum]/[AAA][W3cWaiWcag21QuickrefContrastEnhanced] dans le [sélecteur de couleur][DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker].  APCA est une nouvelle manière de calculer le contraste.  Cette méthode est basée sur des recherches modernes sur la perception des couleurs.  Par rapport aux directives AA/AAA, l’algorithme APCA dépend davantage du contexte.  Le contraste se calcule en fonction des propriétés spatiales suivantes du texte, de la couleur et du contexte.  

*   Propriétés spatiales du texte qui incluent le poids et la taille de la police.  
*   Propriétés spatiales de la couleur qui incluent le contraste perçu entre le texte et l’arrière-plan.  
*   Propriétés spatiales de contexte qui incluent la lumière ambiante, l’environnement et l’objectif prévu.  
    
Pour activer cette expérience, accédez à [Paramètres][DevtoolsCustomizeIndexSettings]  >  **Expériences**, puis cochez la cas en regard de l’option **Autoriser la nouvelle fonctionnalité Advanced Perceptual Contrast Algorithm (APCA) à remplacer le taux de contraste et les directives AA/AAA précédentes**.  Pour passer en revue l’historique de cette fonctionnalité dans le projet open source Chromium, accédez au problème [1121900][CR1121900].  

:::image type="complex" source="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png" alt-text="APCA dans le sélecteur de couleurs" lightbox="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png":::
   APCA dans le sélecteur de couleurs  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Télécharger les canaux d’aperçu Microsoft Edge  

Si vous êtes sous Windows, Linux ou macOS, envisagez d'utiliser les [canaux d'aperçu de Microsoft][MicrosoftEdgePreviewChannels] Edge comme navigateur de développement par défaut.  Les canaux de prévisualisation vous donnent accès aux dernières fonctionnalités de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Contacter l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew85]: ../../2020/06/devtools.md "Nouveautés de DevTools (Microsoft Edge85) | Microsoft Docs"  

[DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]: /microsoft-edge/devtools-guide-chromium/accessibility/reference#view-the-contrast-ratio-of-a-text-element-in-the-color-picker "Afficher le coefficient de contraste d’un élément de texte dans le sélecteur de couleurs - Référence d’accessibilité | Microsoft Docs"  
[DevtoolsCssReferenceChangeCss]: /microsoft-edge/devtools-guide-chromium/css/reference#change-css "Modifier des CSS - Référence CSS | Microsoft Docs"  .
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Paramètres - Personnaliser Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personnaliser les raccourcis clavier dans Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/device-mode/dual-screen-and-foldables#testing-on-foldable-and-dual-screen-devices "Test sur les appareils pliables et à double écran- Émuler les appareils à double écran et pliables dans Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Émuler des appareils mobiles dans Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simuler une fenêtre d’affichage mobile - Émuler des appareils mobiles dans Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-load-performance "Enregistrer les performances de charge d’enregistrement - Référence d’analyse des performances | Microsoft Docs"  
[DevtoolsInspectStylesEditFonts]: /microsoft-edge/devtools-guide-chromium/inspect-styles/edit-fonts "Modifier les styles et paramètres de police CSS dans le volet Styles de DevTools | Microsoft Docs"  
[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium/index "Présentation de Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  

[DualScreenIntroductionHowToWorkWithSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Utilisation de la jointure - Introduction aux appareils à double écran | Microsoft Docs"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Fonctionnalité couvrant l’écran multimédia CSS pour la détection à double écran | Microsoft Docs"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "API JavaScript getWindowSegments pour appareils à double écran | Microsoft Docs"  

[GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1]: https://microsoftedge.github.io/DevToolsSamples/whats-new/89/target-css-demo.html#section-1 "Section1 - Démo :target CSS pour les nouveautés de DevTools (Microsoft Edge89) | GitHub"  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull229]: https://github.com/microsoft/vscode-edge-devtools/pull/229 "Extraction229: implémentation du menu déroulant dans les paramètres pour modifier les thèmes | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull233]: https://github.com/microsoft/vscode-edge-devtools/pull/233 "Extraction233: inclure le débogueur pour Microsoft Edge en tant que dépendance | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull235]: https://github.com/microsoft/vscode-edge-devtools/pull/235 "Extraction235: mise à niveau d’Edge DevTools à la version vers 85.0.564.40 | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull248]: https://github.com/microsoft/vscode-edge-devtools/pull/248 "Extraction248: ajouter des boutons de fermeture simple au panneau d’instances | GitHub"  
[GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml]: https://w3c.github.io/silver/guidelines/methods/Method-font-characteristic-contrast.html "Sélectionnez les caractéristiques de police et les couleurs d’arrière-plan pour fournir un contraste suffisant pour la lisibilité | W3C"  
[GithubW3cWebappsecTrustedTypesDistSpec]: https://w3c.github.io/webappsec-trusted-types/dist/spec  "Types approuvés | W3C"  

[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Nouveau Surface Duo | Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux de préversion de Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Mettre à jour une extension manuellement - Extension Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Outils Microsoft Edge pour Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Débogueur pour Microsoft Edge | Visual Studio Marketplace"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bogues Chromium"  
[CR978059]: https://crbug.com/978059 "Problème978059: suppression des cookies lors de leur filtrage; supprimer tous les cookies, et non seulement les cookies filtrés | Bogues Chromium"  
[CR997625]: https://crbug.com/997625 "Problème997625: nouvelle fonctionnalité requise | Option nécessaire pour afficher la valeur décodée par l’URL dans les cookies | Bogues Chromium"  
[CR1003629]: https://crbug.com/1003629 "Problème1003629: le nœud de capture n’effectue plus de capture d’écran du nœud sous le pliage. | Bogues Chromium"  
[CR1012337]: https://crbug.com/1012337 "Problème1012337: l’effacement des données de site détruit une session Google sur des sites autres que Google | Bogues Chromium"  
[CR1028078]: https://crbug.com/1028078 "Problème1028078: placer les options En ligne et Hors ligne l’une à côté de l’autre dans la liste | Bogues Chromium"  
[CR1054281]: https://crbug.com/1054281 "Problème1054281: demande de fonctionnalité: DevTools doit émuler les appareils pliables et à double écran | Bogues Chromium"  
[CR1075865]: https://crbug.com/1075865 "Problème1075865: afficher les cadres supprimés dans la chronologie de Devtools | Bogues Chromium"  
[CR1093229]: https://crbug.com/1093229 "Problème1093229: DevTools: offre une interface utilisateur d’éditeur de police spécialisée | Bogues Chromium"  
[CR1121900]: https://crbug.com/1121900 "Problème1121900: DevTools: mettre à jour la logique de calcul du contraste par nouvelle spécification | Bogues Chromium"  
[CR1122507]: https://crbug.com/1122507 "Problème1122507: Informations sur le travailleur de surface dans l’affichage de l’arborescence de cadre | Bogues Chromium"  
[CR1122580]: https://crbug.com/1122580 "Problème1122580: désolé... Nous n’avons pas pu désactiver l’enregistrement de réseau lors du rechargement | Bogues Chromium"  
[CR1136394]: https://crbug.com/1136394 "Problème1136394: outils Flexbox | Bogues Chromium"  
[CR1139899]: https://crbug.com/1139899 "Problème1139899: signaler la disponibilité des API contrôlées dans l’affichage des détails du cadre | Bogues Chromium"  
[CR1139949]: https://crbug.com/1139949 "Problème1139949: superposition flexbox | Bogues Chromium"  
[CR1147016]: https://crbug.com/1147016 "Problème1147016: le sélectionneur de couleurs ne s’affiche pas dans la fonction var(). | Bogues Chromium"  
[CR1148353]: https://crbug.com/1148353 "Problème1148353: Demande de fonctionnalité: copier l’objet depuis la console devtools | Bogues Chromium"  
[CR1149859]: https://crbug.com/1149859 "Problème1149859: [demande de fonctionnalité][Console] ajouter l’objet copier dans l’élément du Presse-papiers dans le menu contextuel | Bogues Chromium"  
[CR1150797]: https://crbug.com/1150797 "Problème1150797: ajouter un menu contextuel Dupliquer l’élément dans le panneau Éléments | Bogues Chromium"  
[CR1152391]: https://crbug.com/1152391 "Problème1152391: prise en charge du menu contextuel copier CSS dans le panneau de styles | Bogues Chromium"  
[CR1155120]: https://crbug.com/1155120 "Problème1155120: [FR]Nom du fichier de copie de support et numéro de ligne | Bogues Chromium"  
[CR1156628]: https://crbug.com/1156628 "Problème1156628: DevTools : ajouter la prise en charge de la fonctionnalité d’état d’élément :target en force | Bogues Chromium"  
[CR1157329]: https://crbug.com/1157329 "Problème1157329: Accessibilité - Narrateur : le Narrateur n’annonce pas le nombre et la position des suggestions disponibles pour le code dans l’onglet Styles | Bogues Chromium"  

[MdnDocsWebCssTarget]: https://developer.mozilla.org/docs/web/css/:target ":target | MDN"  

[SamsungUsMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Galaxy Fold | Samsung États-Unis"  

[W3cWaiWcag21QuickrefContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref#contrast-enhanced "Contraste (amélioré) - Comment répondre aux exigences WCAG (référence rapide) | W3C"  
[W3cWaiWcag21QuickrefContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref#contrast-minimum "Contraste (minimum) - Comment répondre aux exigences WCAG (référence rapide) | W3C"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developer.chrome.com/blog/new-in-devtools-89) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est sous [licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen

[SpanningPlaceholder]: link-t-b-d "Espace réservé couvrant"  
