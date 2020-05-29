---
description: Découvrez les différents aspects liés à la conception et le comportement de l’interface utilisateur à prendre en compte lors de la création d’extensions Microsoft Edge.
title: Conception d’extensions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, JavaScript, conception, icônes, développeur
ms.openlocfilehash: 622d72453ea3ecd2897efcf8f67e1b2aa7a0937c
ms.sourcegitcommit: da768193c7ae7b611f4fbb1746f16d9818e42bac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2020
ms.locfileid: "10684063"
---
# Recommandations en matière de conception pour les extensions Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

La page suivante contient divers aspects relatifs à la conception et le comportement de l’interface utilisateur à prendre en compte lors de la création d’extensions Microsoft Edge.  

## Icônes  

Vous devez créer des icônes pour votre extension à l’aide d’un graphique vectoriel.  Vous devez créer plusieurs tailles de votre icône pour votre extension et trois tailles supplémentaires si vous souhaitez empaqueter votre extension.  Les extensions Microsoft Edge ne prennent pas en charge les icônes. svg.  

Avant de créer votre extension, consultez le Guide de l' [accessibilité][ExtensionsGuidesAccessibility] pour vous assurer que les icônes disposent d’un contraste suffisant et sont visibles dans les thèmes clairs et sombres de Microsoft Edge.  

Même si tout format d’image WebKit est pris en charge, les icônes PNG sont recommandées pour la prise en charge de la transparence.  

### Icônes pour votre extension  

Pour votre extension, vous devez créer une taille d’icône pour l’action du navigateur ou une action de page, et une taille d’icône pour le volet **Extensions** .  Plusieurs tailles pour chacune d’elles pourront être fournies pour prendre en charge des affichages de haute résolution.  

Une extension doit avoir une action de navigateur ou une icône d’action de page.  Les icônes action du navigateur et action de la page risquent d’être modifiées lors de l’exécution à l’aide de la méthode [browserAction. seticon][MSDApiBrowseractionSeticon] ou [pageAction. seticon][MDNApiPageactionSeticon] .  

#### Action du navigateur  

Les tailles préférées pour les icônes action du navigateur et action de la page sont `20px` ,, `25px` `30px` et `40px` .  Les autres tailles prises en charge sont les suivantes: `19px` `35px` `38px`  

L’extrait de code de fichier [Manifest. JSON][ExtensionsApisupportManifestkeys] montre une icône d’action du navigateur standard et haute définition en utilisant la clé [browser_action][MDNManifestjsonBrowserAction] .  La même syntaxe s’applique à la clé [page_action][MDNManifestjsonPageAction] .  

```json
"browser_action": {
    "default_icon": {
        "20": "images/icon_20.png",
        "40": "images/icon_40.png"
    },
    "default_title": "Fetch page info",
    "default_popup": "popup.html"
}
```  

Si l’action du navigateur a été définie par l’extension, celle-ci apparaît dans le menu Actions après avoir sélectionné **plus (...)**, ou à droite de la barre d’adresse si le **bouton afficher en regard de la barre d’adresses** a été activé par l’utilisateur.  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/actionmenu-browseraction.png" alt-text="Action du navigateur dans le menu d’action":::
         Action du navigateur dans le menu d’action :::image-end:::
      
      <!--![browser action in action menu][ImageActionmenuBrowseraction]  -->  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/browseractionicon.png" alt-text="Action du navigateur":::
         Action du navigateur :::image-end:::
      
      <!--![browser action][ImageBrowserActionIcon]  -->  
   :::column-end:::
:::row-end:::

#### Action de page  

La clé de [page_action][MDNManifestjsonPageAction] a la même syntaxe de manifeste JSON que la clé [browser_action][MDNManifestjsonBrowserAction] .  Une action de page a également les mêmes exigences de taille d’icône que l’action du navigateur.  

Si l’action page est spécifiée dans le fichier [Manifest. JSON][ExtensionsApisupportManifestkeys] , elle apparaît dans la barre d’adresses chaque fois que la méthode [pageAction. Show][MDNApiPageactionShow] est utilisée.  

:::image type="complex" source="../media/pageaction.png" alt-text="Action de page":::
   Action de page
:::image-end:::

<!--![page action][ImagePageaction]  -->  

##### Interface utilisateur de gestion  

Lorsque les utilisateurs naviguent dans le volet extensions en accédant au menu **plus (...)** et en sélectionnant les **Extensions**, une icône apparaît en regard du nom de l’extension.  

Spécifiez les tailles d’icônes suivantes.  

| Clé | Détails |  
|:--- |:--- |  
| `48px` | Icône d’affichage de la résolution standard. |  
| `128px` | Icône d’affichage de haute résolution. |  
| `176px` | Icône pour afficher une résolution supérieure. |  


```json
"icons": {
    "48": "images/icon_48.png",
    "128": "images/icon_128.png",
    "176": "images/icon_176.png"
},
```  

:::image type="complex" source="../media/management-ui.png" alt-text="Interface utilisateur de gestion":::
   Interface utilisateur de gestion
:::image-end:::

<!--![management UI][ImageManagementUi]  -->  

### Icônes pour l’empaquetage  

Une fois votre extension prête pour l’emballage, trois tailles d’icône supplémentaires doivent être prêtes.  

| Taille | Détails |  
|:--- |:--- |  
| 44px | Utilisé dans l’interface utilisateur de Windows (**liste des applications**, paramètres du système de **configuration**  \>  **System**  \>  **& fonctionnalités**\). |  
| pixels | Exigence d’emballage \ (non visible n’importe où \). |  
| 150px | Utilisé comme icône du Microsoft Store. |  


Consultez le [Guide d’emballage manuel][ExtensionsGuidesPackagingCreatingTestingPackagesAssetsFolder] ou le [Guide d’emballage ManifoldJS][ExtensionsGuidesPackagingUsingManifoldjsPackagePackagingManifoldjs] pour déterminer l’emplacement de ces icônes.  Cette fonction dépend de la méthode d’emballage que vous choisissez.  

#### Icône Microsoft Store  

Si l’icône 150px du Microsoft Store a un arrière-plan transparent, la couleur d’accentuation de l’appareil de l’utilisateur apparaît comme la couleur d’arrière-plan de l’icône.  

Par exemple, si un utilisateur a sélectionné roses comme couleur d’accentuation, l’arrière-plan transparent de votre icône Windows Store est affiché en rose.  

:::row:::
   :::column span="1":::
       :::image type="complex" source="../media/windows-accent-color.png" alt-text="Couleur d’accentuation Windows":::
          Couleur d’accentuation Windows :::image-end:::
       
       <!--![Windows accent color][ImageWindowsAccentColor]  -->  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/store-icon-with-transparent-background.png" alt-text="Couleur d’arrière-plan sélectionnée automatiquement":::
         Couleur d’arrière-plan sélectionnée automatiquement :::image-end:::
      
      <!--![Background color auto selected][ImageStoreIconTransparencyBackground]  -->  
   :::column-end:::
:::row-end:::

Si vous souhaitez sélectionner votre propre couleur d’arrière-plan pour votre Microsoft Store, vous devez rendre l’arrière-plan opaque.  

> [!NOTE]
> Le fait de soumettre une extension Microsoft Edge au Microsoft Store est actuellement une fonctionnalité restreinte.  [Contactez-nous][AkaExtensionRequest] avec vos demandes d’aide pour le Microsoft Store et votre demande est envisagée pour une prochaine mise à jour.  

<!-- image links -->  

<!--[ImageActionmenuBrowseraction]: ../media/actionmenu-browseraction.png "browser action in action menu"  -->  
<!--[ImageBrowserActionIcon]: ../media/browseractionicon.png "browser action"  -->  
<!--[ImagePageaction]: ../media/pageaction.png "page action"  -->  
<!--[ImageManagementUi]: ../media/management-ui.png "management UI"  -->  
<!--[ImageWindowsAccentColor]: ../media/windows-accent-color.png "Windows accent color"  -->  
<!--[ImageStoreIconTransparencyBackground]: ../media/store-icon-with-transparent-background.png "Background color auto selected"  -->  

<!-- links -->  

[ExtensionsGuidesAccessibility]: ./accessibility.md "Accessibilité | Documents Microsoft"  
[ExtensionsGuidesPackagingCreatingTestingPackagesAssetsFolder]: ./packaging/creating-and-testing-extension-packages.md#assets-folder "Dossiers de ressources: création et test d’un package AppX d’extensions Microsoft Edge | Documents Microsoft"  
[ExtensionsGuidesPackagingUsingManifoldjsPackagePackagingManifoldjs]: ./packaging/using-manifoldjs-to-package-extensions.md#packaging-with-manifoldjs "Création d’un package avec ManifoldJS: utilisation de ManifoldJS pour créer des packages AppX d’extension | Documents Microsoft"  

[ExtensionsApisupportManifestkeys]: ../API-support/supported-manifest-keys.md "Clés de manifeste prises en charge | Documents Microsoft"  

[AkaExtensionRequest]: https://aka.ms/extension-request "Contactez-nous"  

[MSDApiBrowseractionSeticon]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/setIcon "browserAction. setIcon ()-API | MDN"  
[MDNApiPageactionSeticon]: https://developer.mozilla.org/Add-ons/WebExtensions/API/pageAction/setIcon "pageAction. setIcon ()-API | MDN"  
[MDNApiPageactionShow]: https://developer.mozilla.org/Add-ons/WebExtensions/API/pageAction/show "pageAction. Show ()-API | MDN"  
[MDNManifestjsonBrowserAction]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/browser_action "browser_action-manifest. JSON | MDN"  
[MDNManifestjsonPageAction]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/page_action "page_action-manifest. JSON | MDN"  
