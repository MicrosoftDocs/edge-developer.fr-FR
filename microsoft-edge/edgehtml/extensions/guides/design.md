---
description: Découvrez les différents aspects liés à la conception et le comportement de l’interface utilisateur à prendre en compte lors de la création d’extensions Microsoft Edge.
title: Conception d’extensions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, JavaScript, conception, icônes, développeur
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a32223f93baf44d2ca523e92cf9d7584ad9a8333
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233405"
---
# <span data-ttu-id="d5d5d-104">Recommandations en matière de conception pour les extensions Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d5d5d-104">Design Guidelines For Microsoft Edge Extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="d5d5d-105">La page suivante contient divers aspects relatifs à la conception et le comportement de l’interface utilisateur à prendre en compte lors de la création d’extensions Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d5d5d-105">The following page contains various design aspects and UI behavior to consider when creating Microsoft Edge extensions.</span></span>  

## <span data-ttu-id="d5d5d-106">Icônes</span><span class="sxs-lookup"><span data-stu-id="d5d5d-106">Icons</span></span>  

<span data-ttu-id="d5d5d-107">Vous devez créer des icônes pour votre extension à l’aide d’un graphique vectoriel.</span><span class="sxs-lookup"><span data-stu-id="d5d5d-107">You should make the icons of your extension using a vector graphic.</span></span>  <span data-ttu-id="d5d5d-108">Vous devez créer plusieurs tailles de votre icône pour votre extension et trois tailles supplémentaires si vous souhaitez empaqueter votre extension.</span><span class="sxs-lookup"><span data-stu-id="d5d5d-108">You must create a few different sizes of your icon for your extension, and three additional sizes if you want to package your extension.</span></span>  <span data-ttu-id="d5d5d-109">Les extensions Microsoft Edge ne prennent pas en charge les icônes. svg.</span><span class="sxs-lookup"><span data-stu-id="d5d5d-109">Microsoft Edge extensions do not support .svg icons.</span></span>  

<span data-ttu-id="d5d5d-110">Avant de créer votre extension, consultez le Guide de l' [accessibilité][ExtensionsGuidesAccessibility] pour vous assurer que les icônes disposent d’un contraste suffisant et sont visibles dans les thèmes clairs et sombres de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d5d5d-110">Before you create your extension icons, you should review the [accessibility][ExtensionsGuidesAccessibility] guide to ensure that your icons have high enough contrast and are visible in both the light and dark themes of Microsoft Edge.</span></span>  

<span data-ttu-id="d5d5d-111">Même si tout format d’image WebKit est pris en charge, les icônes PNG sont recommandées pour la prise en charge de la transparence.</span><span class="sxs-lookup"><span data-stu-id="d5d5d-111">While any webkit image format is supported, .png icons are recommended for transparency support.</span></span>  

### <span data-ttu-id="d5d5d-112">Icônes pour votre extension</span><span class="sxs-lookup"><span data-stu-id="d5d5d-112">Icons for your extension</span></span>  

<span data-ttu-id="d5d5d-113">Pour votre extension, vous devez créer une taille d’icône pour l’action du navigateur ou une action de page, et une taille d’icône pour le volet **Extensions** .</span><span class="sxs-lookup"><span data-stu-id="d5d5d-113">For your extension, you must create one icon size for the browser action or page action, and one icon size for the **Extensions** pane.</span></span>  <span data-ttu-id="d5d5d-114">Plusieurs tailles pour chacune d’elles pourront être fournies pour prendre en charge des affichages de haute résolution.</span><span class="sxs-lookup"><span data-stu-id="d5d5d-114">More than one size for each may be provided to support high resolution displays.</span></span>  

<span data-ttu-id="d5d5d-115">Une extension doit avoir une action de navigateur ou une icône d’action de page.</span><span class="sxs-lookup"><span data-stu-id="d5d5d-115">An extension should have a browser action or page action icon.</span></span>  <span data-ttu-id="d5d5d-116">Les icônes action du navigateur et action de la page risquent d’être modifiées lors de l’exécution à l’aide de la méthode [browserAction. seticon][MSDApiBrowseractionSeticon] ou [pageAction. seticon][MDNApiPageactionSeticon] .</span><span class="sxs-lookup"><span data-stu-id="d5d5d-116">The browser action and page action icons may be changed at runtime using the [browserAction.setIcon][MSDApiBrowseractionSeticon] method or [pageAction.setIcon][MDNApiPageactionSeticon] method.</span></span>  

#### <span data-ttu-id="d5d5d-117">Action du navigateur</span><span class="sxs-lookup"><span data-stu-id="d5d5d-117">Browser action</span></span>  

<span data-ttu-id="d5d5d-118">Les tailles préférées pour les icônes action du navigateur et action de la page sont `20px` ,, `25px` `30px` et `40px` .</span><span class="sxs-lookup"><span data-stu-id="d5d5d-118">The preferred sizes for browser action and page action icons are `20px`, `25px`, `30px`, and `40px`.</span></span>  <span data-ttu-id="d5d5d-119">Les autres tailles prises en charge sont les suivantes: `19px` `35px` `38px`</span><span class="sxs-lookup"><span data-stu-id="d5d5d-119">Other supported sizes include `19px`, `35px`, and `38px`.</span></span>  

<span data-ttu-id="d5d5d-120">Lemanifest.jssuivant dans l’extrait de fichier montre une icône [ d’action du][ExtensionsApisupportManifestkeys] navigateur standard et haute définition en utilisant la clé [browser_action][MDNManifestjsonBrowserAction] .</span><span class="sxs-lookup"><span data-stu-id="d5d5d-120">The following [manifest.json][ExtensionsApisupportManifestkeys] file snippet shows a standard and high definition browser action icon being specified using the [browser_action][MDNManifestjsonBrowserAction] key.</span></span>  <span data-ttu-id="d5d5d-121">La même syntaxe s’applique à la clé [page_action][MDNManifestjsonPageAction] .</span><span class="sxs-lookup"><span data-stu-id="d5d5d-121">The same syntax applies for the [page_action][MDNManifestjsonPageAction] key.</span></span>  

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

<span data-ttu-id="d5d5d-122">Si l’action du navigateur a été définie par l’extension, celle-ci apparaît dans le menu Actions après avoir sélectionné **plus (...)**, ou à droite de la barre d’adresse si le **bouton afficher en regard de la barre d’adresses** a été activé par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d5d5d-122">If the browser action has been set by the extension, it appears either in the Actions menu after selecting **More(...)**,  or to the right of the address bar if **Show button next to the address bar** has been toggled on by the user.</span></span>  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/actionmenu-browseraction.png" alt-text="Action du navigateur dans le menu d’action":::
         <span data-ttu-id="d5d5d-124">Action du navigateur dans le menu d’action</span><span class="sxs-lookup"><span data-stu-id="d5d5d-124">Browser action in action menu</span></span> :::image-end:::
      
      <!--![browser action in action menu][ImageActionmenuBrowseraction]  -->  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/browseractionicon.png" alt-text="Action du navigateur":::
         <span data-ttu-id="d5d5d-126">Action du navigateur</span><span class="sxs-lookup"><span data-stu-id="d5d5d-126">Browser action</span></span> :::image-end:::
      
      <!--![browser action][ImageBrowserActionIcon]  -->  
   :::column-end:::
:::row-end:::

#### <span data-ttu-id="d5d5d-127">Action de page</span><span class="sxs-lookup"><span data-stu-id="d5d5d-127">Page action</span></span>  

<span data-ttu-id="d5d5d-128">La clé de [page_action][MDNManifestjsonPageAction] a la même syntaxe de manifeste JSON que la clé [browser_action][MDNManifestjsonBrowserAction] .</span><span class="sxs-lookup"><span data-stu-id="d5d5d-128">The [page_action][MDNManifestjsonPageAction] key has the same JSON manifest syntax as the [browser_action][MDNManifestjsonBrowserAction] key.</span></span>  <span data-ttu-id="d5d5d-129">Une action de page a également les mêmes exigences de taille d’icône que l’action du navigateur.</span><span class="sxs-lookup"><span data-stu-id="d5d5d-129">Page action also has the same icon size requirements as browser action.</span></span>  

<span data-ttu-id="d5d5d-130">Si une action de page est spécifiée dans le [manifest.jssur][ExtensionsApisupportManifestkeys] un fichier, elle apparaît dans la barre d’adresses chaque fois que la méthode [pageAction. Show][MDNApiPageactionShow] est utilisée.</span><span class="sxs-lookup"><span data-stu-id="d5d5d-130">If page action is specified in the [manifest.json][ExtensionsApisupportManifestkeys] file, it appears within the address bar whenever the [pageAction.show][MDNApiPageactionShow] method is used.</span></span>  

:::image type="complex" source="../media/pageaction.png" alt-text="Action de page":::
   <span data-ttu-id="d5d5d-132">Action de page</span><span class="sxs-lookup"><span data-stu-id="d5d5d-132">Page action</span></span>
:::image-end:::

<!--![page action][ImagePageaction]  -->  

##### <span data-ttu-id="d5d5d-133">Interface utilisateur de gestion</span><span class="sxs-lookup"><span data-stu-id="d5d5d-133">Management UI</span></span>  

<span data-ttu-id="d5d5d-134">Lorsque les utilisateurs naviguent dans le volet extensions en accédant au menu **plus (...)** et en sélectionnant les **Extensions**, une icône apparaît en regard du nom de l’extension.</span><span class="sxs-lookup"><span data-stu-id="d5d5d-134">When users navigate to the extensions pane by going to the **More(...)** menu and selecting **Extensions**, an icon is displayed next to the name of the extension.</span></span>  

<span data-ttu-id="d5d5d-135">Spécifiez les tailles d’icônes suivantes.</span><span class="sxs-lookup"><span data-stu-id="d5d5d-135">You should specify the following icon sizes.</span></span>  

| <span data-ttu-id="d5d5d-136">Clé</span><span class="sxs-lookup"><span data-stu-id="d5d5d-136">Key</span></span> | <span data-ttu-id="d5d5d-137">Détails</span><span class="sxs-lookup"><span data-stu-id="d5d5d-137">Details</span></span> |  
|:--- |:--- |  
| `48px` | <span data-ttu-id="d5d5d-138">Icône d’affichage de la résolution standard.</span><span class="sxs-lookup"><span data-stu-id="d5d5d-138">Icon for standard resolution displays.</span></span> |  
| `128px` | <span data-ttu-id="d5d5d-139">Icône d’affichage de haute résolution.</span><span class="sxs-lookup"><span data-stu-id="d5d5d-139">Icon for high resolution displays.</span></span> |  
| `176px` | <span data-ttu-id="d5d5d-140">Icône pour afficher une résolution supérieure.</span><span class="sxs-lookup"><span data-stu-id="d5d5d-140">Icon for even higher resolution displays.</span></span> |  


```json
"icons": {
    "48": "images/icon_48.png",
    "128": "images/icon_128.png",
    "176": "images/icon_176.png"
},
```  

:::image type="complex" source="../media/management-ui.png" alt-text="Interface utilisateur de gestion":::
   <span data-ttu-id="d5d5d-142">Interface utilisateur de gestion</span><span class="sxs-lookup"><span data-stu-id="d5d5d-142">Management UI</span></span>
:::image-end:::

<!--![management UI][ImageManagementUi]  -->  

### <span data-ttu-id="d5d5d-143">Icônes pour l’empaquetage</span><span class="sxs-lookup"><span data-stu-id="d5d5d-143">Icons for packaging</span></span>  

<span data-ttu-id="d5d5d-144">Une fois votre extension prête pour l’emballage, trois tailles d’icône supplémentaires doivent être prêtes.</span><span class="sxs-lookup"><span data-stu-id="d5d5d-144">Once your extension is ready for packaging, you must have three additional icon sizes ready.</span></span>  

| <span data-ttu-id="d5d5d-145">Taille</span><span class="sxs-lookup"><span data-stu-id="d5d5d-145">Size</span></span> | <span data-ttu-id="d5d5d-146">Détails</span><span class="sxs-lookup"><span data-stu-id="d5d5d-146">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="d5d5d-147">44px</span><span class="sxs-lookup"><span data-stu-id="d5d5d-147">44px</span></span> | <span data-ttu-id="d5d5d-148">Utilisé dans l’interface utilisateur de Windows (**liste des applications**, paramètres du système de **configuration**  \>  \*\*\*\*  \>  **& fonctionnalités**\).</span><span class="sxs-lookup"><span data-stu-id="d5d5d-148">Used in the Windows UI \(**App List**, **Settings** \> **System** \> **Apps & features**\).</span></span> |  
| <span data-ttu-id="d5d5d-149">pixels</span><span class="sxs-lookup"><span data-stu-id="d5d5d-149">50px</span></span> | <span data-ttu-id="d5d5d-150">Exigence d’emballage \ (non visible n’importe où \).</span><span class="sxs-lookup"><span data-stu-id="d5d5d-150">Packaging requirement \(not visible anywhere\).</span></span> |  
| <span data-ttu-id="d5d5d-151">150px</span><span class="sxs-lookup"><span data-stu-id="d5d5d-151">150px</span></span> | <span data-ttu-id="d5d5d-152">Utilisé comme icône du Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="d5d5d-152">Used as the icon for the Microsoft Store.</span></span> |  


<span data-ttu-id="d5d5d-153">Consultez le [Guide d’emballage manuel][ExtensionsGuidesPackagingCreatingTestingPackagesAssetsFolder] ou le [Guide d’emballage ManifoldJS][ExtensionsGuidesPackagingUsingManifoldjsPackagePackagingManifoldjs] pour déterminer l’emplacement de ces icônes.</span><span class="sxs-lookup"><span data-stu-id="d5d5d-153">See either the [manual packaging guide][ExtensionsGuidesPackagingCreatingTestingPackagesAssetsFolder] or the [ManifoldJS packaging guide][ExtensionsGuidesPackagingUsingManifoldjsPackagePackagingManifoldjs] to determine where these icons is placed.</span></span>  <span data-ttu-id="d5d5d-154">Cette fonction dépend de la méthode d’emballage que vous choisissez.</span><span class="sxs-lookup"><span data-stu-id="d5d5d-154">This depends upon which packaging method you choose.</span></span>  

#### <span data-ttu-id="d5d5d-155">Icône Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="d5d5d-155">Microsoft Store icon</span></span>  

<span data-ttu-id="d5d5d-156">Si l’icône 150px du Microsoft Store a un arrière-plan transparent, la couleur d’accentuation de l’appareil de l’utilisateur apparaît comme la couleur d’arrière-plan de l’icône.</span><span class="sxs-lookup"><span data-stu-id="d5d5d-156">If the 150px icon for the Microsoft Store has a transparent background, the accent color of the user's device appears as the background color of the icon.</span></span>  

<span data-ttu-id="d5d5d-157">Par exemple, si un utilisateur a sélectionné roses comme couleur d’accentuation, l’arrière-plan transparent de votre icône Windows Store est affiché en rose.</span><span class="sxs-lookup"><span data-stu-id="d5d5d-157">For example, if a user has selected pink as the accent color, the transparent background of your store icon is displayed as pink.</span></span>  

:::row:::
   :::column span="1":::
       :::image type="complex" source="../media/windows-accent-color.png" alt-text="Couleur d’accentuation Windows":::
          <span data-ttu-id="d5d5d-159">Couleur d’accentuation Windows</span><span class="sxs-lookup"><span data-stu-id="d5d5d-159">Windows accent color</span></span> :::image-end:::
       
       <!--![Windows accent color][ImageWindowsAccentColor]  -->  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/store-icon-with-transparent-background.png" alt-text="Couleur d’arrière-plan sélectionnée automatiquement":::
         <span data-ttu-id="d5d5d-161">Couleur d’arrière-plan sélectionnée automatiquement</span><span class="sxs-lookup"><span data-stu-id="d5d5d-161">Background color auto selected</span></span> :::image-end:::
      
      <!--![Background color auto selected][ImageStoreIconTransparencyBackground]  -->  
   :::column-end:::
:::row-end:::

<span data-ttu-id="d5d5d-162">Si vous souhaitez sélectionner votre propre couleur d’arrière-plan pour votre Microsoft Store, vous devez rendre l’arrière-plan opaque.</span><span class="sxs-lookup"><span data-stu-id="d5d5d-162">If you want to pick your own background color for your Microsoft Store, you must make the background opaque.</span></span>  

> [!NOTE]
> <span data-ttu-id="d5d5d-163">Le fait de soumettre une extension Microsoft Edge au Microsoft Store est actuellement une fonctionnalité restreinte.</span><span class="sxs-lookup"><span data-stu-id="d5d5d-163">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span>  <span data-ttu-id="d5d5d-164">[Contactez-nous][AkaExtensionRequest] avec vos demandes d’aide pour le Microsoft Store et votre demande est envisagée pour une prochaine mise à jour.</span><span class="sxs-lookup"><span data-stu-id="d5d5d-164">[Contact us][AkaExtensionRequest] with your requests for the Microsoft Store, and your request is considered for a future update.</span></span>  

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
[MDNManifestjsonBrowserAction]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/browser_action "browser_action-manifest.jssur | MDN"  
[MDNManifestjsonPageAction]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/page_action "page_action-manifest.jssur | MDN"  
