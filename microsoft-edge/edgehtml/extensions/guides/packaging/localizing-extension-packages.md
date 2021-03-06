---
description: Découvrez comment localiser votre package d’extension Microsoft Edge afin qu’il soit prêt pour plusieurs paramètres régionaux à la publication.
title: Localisation des packages d’extension
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: c4043c1e-15ac-4210-8851-3804c7708f49
keywords: edge, développement web, html, css, javascript, développeur
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d5dd21f82fd746ad619e9d89a1526ff6a511d615
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397719"
---
# <a name="localizing-microsoft-edge-extensions-for-windows-and-the-microsoft-store"></a><span data-ttu-id="87d97-104">Localisation des extensions Microsoft Edge pour Windows et le Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="87d97-104">Localizing Microsoft Edge extensions for Windows and the Microsoft Store</span></span>  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

<span data-ttu-id="87d97-105">Ce guide vous guide tout au long de la localisation de votre extension Microsoft Edge afin qu’elle soit prête pour plusieurs paramètres régionaux à la publication.</span><span class="sxs-lookup"><span data-stu-id="87d97-105">This guide walks through how to localize your Microsoft Edge extension so that it's ready for multiple locales upon release.</span></span>  <span data-ttu-id="87d97-106">Pour trouver entièrement votre extension, vous devez suivre les étapes pour Windows et le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="87d97-106">To fully localize your extension, you'll need to follow the steps for both Windows and the Microsoft Store.</span></span>  

<span data-ttu-id="87d97-107">Si vous souhaitez localiser vos ressources d’extension pour Microsoft Edge, vous pouvez apprendre à utiliser l’infrastructure i18n dans le [guide d’internationalisation.](../internationalization.md)</span><span class="sxs-lookup"><span data-stu-id="87d97-107">If you want to localize your extension resources for Microsoft Edge, you can learn how to use the i18n framework in the [Internationalization guide](../internationalization.md).</span></span>  

> [!NOTE]
> <span data-ttu-id="87d97-108">Si votre extension ne prend pas en charge plusieurs langues, vous pouvez passer à La localisation du nom et de la [description dans le Microsoft Store.](#localizing-name-and-description-in-the-microsoft-store)</span><span class="sxs-lookup"><span data-stu-id="87d97-108">If your extension doesn't support multiple languages, you can skip to [Localizing name and description in the Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).</span></span>  

## <a name="the-localization-process-overview"></a><span data-ttu-id="87d97-109">Vue d’ensemble du processus de localisation</span><span class="sxs-lookup"><span data-stu-id="87d97-109">The localization process overview</span></span>  

<span data-ttu-id="87d97-110">La première étape pour mettre votre extension à la disposition d’un large public consiste à configurer son [AppxManifest](#configuring-the-appxmanifest) pour plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="87d97-110">The first step towards getting your extension available to a wide audience is to [configure its AppxManifest](#configuring-the-appxmanifest) for multiple languages.</span></span>  <span data-ttu-id="87d97-111">Dans le Microsoft Store, cela indique aux utilisateurs les langues que votre extension prend en charge.</span><span class="sxs-lookup"><span data-stu-id="87d97-111">In the Microsoft Store, this will show users what languages your extension supports.</span></span>  <span data-ttu-id="87d97-112">Certains champs dans appxManifest devront également être modifiés si vous souhaitez que le nom de votre extension soit localisée dans l’interface utilisateur windows et le [Microsoft Store.](#localizing-extension-resources-for-windows-and-the-microsoft-store)</span><span class="sxs-lookup"><span data-stu-id="87d97-112">Certain fields in the AppxManifest will also need to be changed if you want the name of your extension to be [localized in the Windows UI and the Microsoft Store](#localizing-extension-resources-for-windows-and-the-microsoft-store).</span></span>  

<span data-ttu-id="87d97-113">Une fois votre AppxManifest configuré, vous devez créer des ressources de chaîne [JSON](#creating-json-string-resources) pour les langues que vous avez indiquées comme étant pris en charge.</span><span class="sxs-lookup"><span data-stu-id="87d97-113">Once your AppxManifest is configured, you'll need to [create JSON string resources](#creating-json-string-resources) for the languages that you indicated as supported.</span></span>  <span data-ttu-id="87d97-114">Cela nécessite la création d’un fichier pour chaque langue, où chaque fichier possède toutes les chaînes d’interface utilisateur de `.resjson` cette langue.</span><span class="sxs-lookup"><span data-stu-id="87d97-114">This requires creating a `.resjson` file for each language, where each file has all the UI strings of that language within it.</span></span>  

<span data-ttu-id="87d97-115">Une fois que les fichiers pour les langues prises en charge ont été créés, un fichier de ressources `.resjson` [.pri doit être créé.](#creating-the-resources-file)</span><span class="sxs-lookup"><span data-stu-id="87d97-115">After the `.resjson` files for the supported languages have been made, a [.pri resource file will need to be created](#creating-the-resources-file).</span></span> <span data-ttu-id="87d97-116">Il sera créé à l’aide d’un fichier de configuration à l’outil MakePRI fourni avec le [SDK Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span><span class="sxs-lookup"><span data-stu-id="87d97-116">This will be created by using a configuration file to the MakePRI tool that comes with the [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span></span>  

> [!NOTE]
> <span data-ttu-id="87d97-117">Si vous téléchargez uniquement le SDK Windows 10 pour utiliser l’outil, vous pouvez sélectionner uniquement les outils de signature du `MakePri.exe` **SDK Windows** pour les applications de bureau et le **SDK Windows** pour les fonctionnalités d’application gérée UWP pour que le téléchargement reste plus léger.</span><span class="sxs-lookup"><span data-stu-id="87d97-117">If you are only downloading the Windows 10 SDK to use the `MakePri.exe` tool, you can select only the **Windows SDK Signing Tools for Desktop Apps** and **Windows SDK for UWP Managed App** features to keep the download lighter.</span></span>  <span data-ttu-id="87d97-118">`MakePri.exe`L’outil s’affiche dans les sous-ensembles de `C:\Program Files (x86)\Windows Kits\10\bin\10.0.17713.0` .</span><span class="sxs-lookup"><span data-stu-id="87d97-118">The `MakePri.exe` tool will appear in subfolders of `C:\Program Files (x86)\Windows Kits\10\bin\10.0.17713.0`.</span></span>  

<span data-ttu-id="87d97-119">Une fois que vous avez chargé votre extension, l’étape finale consiste à trouver le nom et la [description dans le Microsoft Store.](#localizing-name-and-description-in-the-microsoft-store)</span><span class="sxs-lookup"><span data-stu-id="87d97-119">Once you've uploaded your extension, the final step is to [localize the name and description in the Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).</span></span>  

> [!NOTE]
> <span data-ttu-id="87d97-120">L’envoi d’une extension Microsoft Edge au Microsoft Store est actuellement une fonctionnalité restreinte.</span><span class="sxs-lookup"><span data-stu-id="87d97-120">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span>  <span data-ttu-id="87d97-121">**Faites-nous part** de vos demandes pour faire partie du Microsoft Store et nous vous envisagerons pour une prochaine mise à jour.</span><span class="sxs-lookup"><span data-stu-id="87d97-121">**Reach out to us** with your requests to be a part of the Microsoft Store, and we'll consider you for a future update.</span></span>  

## <a name="configuring-the-appxmanifest"></a><span data-ttu-id="87d97-122">Configuration d’AppXManifest</span><span class="sxs-lookup"><span data-stu-id="87d97-122">Configuring the AppXManifest</span></span>  

<span data-ttu-id="87d97-123">La liste des langues de votre extension prise en charge dans le Microsoft Store est générée en fonction de ses valeurs AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="87d97-123">Your extension's Supported languages list in the Microsoft Store is generated based on its AppXManifest values.</span></span>  <span data-ttu-id="87d97-124">Cette liste est spécifiée à l’aide de `Resource` l’élément.</span><span class="sxs-lookup"><span data-stu-id="87d97-124">This list is specified using the `Resource` element.</span></span>  

![Détails de l’application](../../media/language-app-details.png)  

<span data-ttu-id="87d97-126">Pour spécifier la liste des langues qui sont pris en charge par votre extension, vous pouvez ajouter un élément au format ci-dessous \(cet élément affiche la prise en charge de l’anglais, de l’allemand et du français dans le `Resource` `Resource` Microsoft Store\) :</span><span class="sxs-lookup"><span data-stu-id="87d97-126">To specify the list of languages that are supported by your extension, you can add a `Resource` element in the format seen below \(this `Resource` element will show support for English, German, and French in the Microsoft Store\):</span></span>  

```xml
<Resources>
    <Resource Language="en-us"/>
    <Resource Language="de-de"/>
    <Resource Language="fr-fr"/>
</Resources>
```  

<span data-ttu-id="87d97-127">Pour [plus d’informations](/windows/uwp/publish/supported-languages) sur les langues/codes de langue pris en charge par le Microsoft Store, voir Langues pris en charge.</span><span class="sxs-lookup"><span data-stu-id="87d97-127">See [Supported languages](/windows/uwp/publish/supported-languages) for info on the languages/language codes that the Microsoft Store supports.</span></span>  

<span data-ttu-id="87d97-128">Pour spécifier des chaînes localisées pour tous les éléments visibles publiquement dans appxManifest, vous devez utiliser un identificateur de ressource au format `ms-resource:<resource id>` .</span><span class="sxs-lookup"><span data-stu-id="87d97-128">In order to specify localized strings for all publicly visible elements in the AppxManifest, you'll have to use a resource identifier in the format of `ms-resource:<resource id>`.</span></span>  

<span data-ttu-id="87d97-129">Les extraits de code ci-dessous font un AppxManifest complet.</span><span class="sxs-lookup"><span data-stu-id="87d97-129">The snippets below make a complete AppxManifest.</span></span> <span data-ttu-id="87d97-130">Les valeurs suivantes doivent être récupérées à partir de fichiers de ressources localisées :</span><span class="sxs-lookup"><span data-stu-id="87d97-130">The following values should be retrieved from localized resource files:</span></span>  

*   <span data-ttu-id="87d97-131">Properties\DisplayName</span><span class="sxs-lookup"><span data-stu-id="87d97-131">Properties\DisplayName</span></span>  
*   <span data-ttu-id="87d97-132">Propriétés\Description</span><span class="sxs-lookup"><span data-stu-id="87d97-132">Properties\Description</span></span>  
*   <span data-ttu-id="87d97-133">Properties\PublisherDisplayName</span><span class="sxs-lookup"><span data-stu-id="87d97-133">Properties\PublisherDisplayName</span></span>  

```xml
<Properties>
    <DisplayName>ms-resource:DisplayName</DisplayName>
    <Description>ms-resource:Description</Description>
    <Logo>Assets\PackageLogo.png</Logo>
    <PublisherDisplayName>ms-resource:PublisherName</PublisherDisplayName>
</Properties>
```  

*   <span data-ttu-id="87d97-134">Applications\Application\VisualElements\DisplayName</span><span class="sxs-lookup"><span data-stu-id="87d97-134">Applications\Application\VisualElements\DisplayName</span></span>  
*   <span data-ttu-id="87d97-135">Applications\Application\VisualElements\Description</span><span class="sxs-lookup"><span data-stu-id="87d97-135">Applications\Application\VisualElements\Description</span></span>  
*   <span data-ttu-id="87d97-136">Applications\Application\Extensions\Extension\AppExtension\DisplayName</span><span class="sxs-lookup"><span data-stu-id="87d97-136">Applications\Application\Extensions\Extension\AppExtension\DisplayName</span></span>  

```xml
<Applications>
    <Application Id="App">
      <uap:VisualElements
        AppListEntry="none"
            DisplayName="ms-resource:DisplayName"
       Square150x150Logo="Assets\Square150x150Logo.png"
       Square44x44Logo="Assets\Square44x44Logo.png"
            Description="ms-resource:Description"
        BackgroundColor="transparent">
      </uap:VisualElements>
      <Extensions>
      <uap3:Extension Category="windows.appExtension">
        <uap3:AppExtension Name="com.microsoft.edge.extension"
            Id="MicrosoftTranslate"
            PublicFolder="Extension"
            DisplayName="ms-resource:DisplayName">
        </uap3:AppExtension>
      </uap3:Extension>
      </Extensions>
    </Application>
  </Applications>
```  

## <a name="localizing-extension-resources-for-windows-and-the-microsoft-store"></a><span data-ttu-id="87d97-137">Localisation des ressources d’extension pour Windows et le Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="87d97-137">Localizing extension resources for Windows and the Microsoft Store</span></span>  

<span data-ttu-id="87d97-138">Maintenant que votre AppxManifest est configuré pour plusieurs langues, il existe quelques différences clés que vous devez connaître entre la recherche de l’interface utilisateur dans votre extension et la recherche de votre extension pour Windows et le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="87d97-138">Now that your AppxManifest is configured for multiple languages, there are some key differences you should know between localizing the UI within your extension and localizing your extension for Windows and the Microsoft Store.</span></span>  

<span data-ttu-id="87d97-139">Bien que les extensions Microsoft Edge ne s’exécutent pas en dehors de Microsoft Edge, leur gestion peut se faire dans Windows.</span><span class="sxs-lookup"><span data-stu-id="87d97-139">While Microsoft Edge extensions don't run outside of Microsoft Edge, the management of them can occur within Windows.</span></span>  <span data-ttu-id="87d97-140">Par exemple, les utilisateurs peuvent gérer leurs extensions dans l’application Paramètres :</span><span class="sxs-lookup"><span data-stu-id="87d97-140">For example, users can manage their extensions in the Settings app:</span></span>  

![application de paramètres](../../media/settings.png)  

<span data-ttu-id="87d97-142">Le nom de l’extension qui apparaît dans l’application Paramètres dans Windows provient d’AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="87d97-142">The name of the extension that shows up in the Settings app in Windows comes from the AppXManifest.</span></span>  <span data-ttu-id="87d97-143">Si cette valeur est codée en dur en anglais, la version anglaise du nom s’affiche sur les appareils Windows non anglais.</span><span class="sxs-lookup"><span data-stu-id="87d97-143">If this value is hardcoded in English, the English version of the name will show up on non-English Windows devices.</span></span>  <span data-ttu-id="87d97-144">Si la authentification de votre extension est en anglais uniquement, vous ne pourz pas la laisser codée en dur.</span><span class="sxs-lookup"><span data-stu-id="87d97-144">If the branding of your extension is English only, it's ok to leave it hardcoded.</span></span>  

> [!NOTE]
> <span data-ttu-id="87d97-145">Si vous souhaitez utiliser des noms localisées pour votre extension Microsoft [](./extensions-in-the-windows-dev-center.md#name-reservation) Edge dans Windows, assurez-vous que les noms localisées sont également disponibles et réservés avant d’apporter les modifications dans le fichier AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="87d97-145">If you want to use localized names for your Microsoft Edge Extension in Windows, make sure the localized names are also [available and reserved](./extensions-in-the-windows-dev-center.md#name-reservation) before you make the changes in the AppXManifest file.</span></span>  <span data-ttu-id="87d97-146">Si les noms ne sont pas réservés, vous obtenez l’erreur suivante lorsque vous téléchargez le package final dans le Centre de dév. Windows :</span><span class="sxs-lookup"><span data-stu-id="87d97-146">If the names are not reserved, you'll get the following error when you upload the final package to Windows Dev Center:</span></span>  
> 
> ![erreur de langue](../../media/language-error.png)  

<span data-ttu-id="87d97-148">L’infrastructure de localisation basée sur i18n définie pour les extensions JavaScript s’applique uniquement dans l’environnement Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="87d97-148">The i18n based localization infrastructure that's defined for JavaScript extensions is only applicable within the Microsoft Edge environment.</span></span>  

<span data-ttu-id="87d97-149">En dehors de Microsoft Edge, dans Windows et le Microsoft Store, la seule infrastructure de localisation prise en charge est basée sur l’infrastructure de localisation de plateforme Windows universelle (UWP).</span><span class="sxs-lookup"><span data-stu-id="87d97-149">Outside of Microsoft Edge, within Windows and the Microsoft Store, the only supported localization framework is based on the Universal Windows Platform (UWP) localization framework.</span></span>  

<span data-ttu-id="87d97-150">Bien que nous supportions les ressources basées sur JSON pour les applications Windows basées sur HTML, le schéma des ressources JSON ne correspond pas à celui défini pour les extensions JavaScript.</span><span class="sxs-lookup"><span data-stu-id="87d97-150">While we do support JSON based resources for HTML based Windows apps, the schema for the JSON resources doesn't match the one defined for JavaScript extensions.</span></span>  

<span data-ttu-id="87d97-151">Voici les principales différences dans les applications [Windows html](/previous-versions/windows/apps/hh465228(v=win.10)):</span><span class="sxs-lookup"><span data-stu-id="87d97-151">The following are the key differences in [HTML based Windows apps](/previous-versions/windows/apps/hh465228(v=win.10)):</span></span>  

*   <span data-ttu-id="87d97-152">Les ressources sont spécifiées dans `.resjson` les fichiers au lieu des `.json` fichiers.</span><span class="sxs-lookup"><span data-stu-id="87d97-152">Resources are specified in `.resjson` files instead of `.json` files.</span></span>  
*   <span data-ttu-id="87d97-153">Les paramètres régionaux pris en charge doivent être spécifiés dans le fichier AppXManifest, les premiers paramètres régionaux étant les paramètres régionaux par défaut.</span><span class="sxs-lookup"><span data-stu-id="87d97-153">The locales supported should be specified in the AppXManifest file, with the first locale being the default locale.</span></span>  
*   <span data-ttu-id="87d97-154">Les ressources d’applications Windows basées sur HTML utilisent le schéma suivant :</span><span class="sxs-lookup"><span data-stu-id="87d97-154">HTML based Windows apps resources use the following schema:</span></span>  
    
    ```json
    {
        "greeting"              : "Hello",
        "_greeting.comment"     : "A welcome greeting.",

        "farewell"              : "Goodbye",
        "_farewell.comment"     : "A goodbye."
    }
    ```  
    
    <span data-ttu-id="87d97-155">La paire nom/valeur, qui est notée par un trait de soulignement, est un commentaire de la ressource de chaîne correspondante.</span><span class="sxs-lookup"><span data-stu-id="87d97-155">The name/value pair denoted by an underscore are comments for the corresponding string resource.</span></span>  
*   `.resjson` <span data-ttu-id="87d97-156">les fichiers sont compilés en fichiers qui doivent être inclus lors de la création du `.pri` package AppX.</span><span class="sxs-lookup"><span data-stu-id="87d97-156">files are compiled into `.pri` files which must be included during AppX package creation.</span></span>  
    
### <a name="creating-json-string-resources"></a><span data-ttu-id="87d97-157">Création de ressources de chaîne JSON</span><span class="sxs-lookup"><span data-stu-id="87d97-157">Creating JSON string resources</span></span>  

<span data-ttu-id="87d97-158">Une fois appxManifest configuré et les différences entre les infrastructure de localisation i18n et UWP mises en évidence, vous êtes prêt à créer vos fichiers de ressources.</span><span class="sxs-lookup"><span data-stu-id="87d97-158">With a configured AppxManifest in hand and the differences between the i18n and UWP localization frameworks highlighted, you're ready to create your resource files.</span></span>  

<span data-ttu-id="87d97-159">Une seule chaîne de ressource dans le manifeste est applicable aux packages d’extension Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="87d97-159">Only one resource string in the manifest is applicable to Microsoft Edge extension packages.</span></span>  <span data-ttu-id="87d97-160">La chaîne est généralement localisée dans les extensions JavaScript et peut être facilement mappée aux fichiers que `DisplayName` `.resjson` Windows attend.</span><span class="sxs-lookup"><span data-stu-id="87d97-160">The `DisplayName` string is commonly localized in JavaScript extensions, and can be easily mapped to the `.resjson` files that Windows expects.</span></span>  <span data-ttu-id="87d97-161">En supposant qu’il s’agit de la seule ressource que vous souhaitez localiser, voici un exemple de fichier `.resjson` à créer :</span><span class="sxs-lookup"><span data-stu-id="87d97-161">Assuming that this is the only resource that you would like to localize, here is a sample `.resjson` file that should be created:</span></span>  

```json
{
    "DisplayName"              : "Jigsaw",
    "_DisplayName.comment"     : "Name of extension."
}
```  

<span data-ttu-id="87d97-162">L’ID de ressource dans chaque fichier doit correspondre à `.resjson` l’ID utilisé dans AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="87d97-162">The resource ID in each `.resjson` file needs to match the ID used in the AppXManifest.</span></span>  <span data-ttu-id="87d97-163">À l’aide de l’exemple d’extrait de code ci-dessus, l’entrée `.resjson` AppXManifest correspondante doit être :</span><span class="sxs-lookup"><span data-stu-id="87d97-163">Using the example `.resjson` snippet above, the corresponding AppXManifest entry should be:</span></span>  

`DisplayName="ms-resource:DisplayName"`  

<span data-ttu-id="87d97-164">Chaque langue que votre extension prend en charge doit avoir un fichier de ressources correspondant et `.resjson` être placée dans la structure de dossiers suivante :</span><span class="sxs-lookup"><span data-stu-id="87d97-164">Each language that your extension supports should have a corresponding resources `.resjson` file and be placed in the following folder structure:</span></span>  

![structure des dossiers linguistiques](../../media/resources-folder.png)  

### <a name="creating-the-resources-file"></a><span data-ttu-id="87d97-166">Création du fichier de ressources</span><span class="sxs-lookup"><span data-stu-id="87d97-166">Creating the resources file</span></span>  

<span data-ttu-id="87d97-167">Une fois que vous avez créé tous vos fichiers, vous êtes prêt à créer votre fichier d’index de ressource `.resjson` de package \(PRI\).</span><span class="sxs-lookup"><span data-stu-id="87d97-167">Once you've created all your `.resjson` files, you're ready to create your package resource index \(PRI\) file.</span></span>  <span data-ttu-id="87d97-168">Ce fichier stocke les ressources pour toutes les langues que vous avez pris en charge.</span><span class="sxs-lookup"><span data-stu-id="87d97-168">This file stores the resources for all your supported languages.</span></span>  <span data-ttu-id="87d97-169">Pour ce faire, vous pouvez utiliser **l’outil MakePRI** qui est inclus avec le SDK Windows 10.</span><span class="sxs-lookup"><span data-stu-id="87d97-169">To do this you can use the **MakePRI** tool which is included with the Windows 10 SDK.</span></span>  

<span data-ttu-id="87d97-170">Tout d’abord, vous devez créer le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="87d97-170">First you'll need to create the configuration file.</span></span>  <span data-ttu-id="87d97-171">Cela définit les qualificateurs et la plateforme par défaut pour les ressources.</span><span class="sxs-lookup"><span data-stu-id="87d97-171">This defines the default qualifiers and platform for the resources.</span></span>  <span data-ttu-id="87d97-172">Pour cet exemple, faites de la langue par défaut `English (US)` et de la plateforme Windows 10.</span><span class="sxs-lookup"><span data-stu-id="87d97-172">For this example, make the default language `English (US)` and the platform Windows 10.</span></span>  <span data-ttu-id="87d97-173">Pour ce faire, créez `priconfig.xml` un fichier avec le contenu suivant dans `[Root folder]` :</span><span class="sxs-lookup"><span data-stu-id="87d97-173">To do this, create a `priconfig.xml` file with the following content in the `[Root folder]`:</span></span>  

![priconfig dans le dossier](../../media/priconfig.png)  

```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<resources targetOsVersion="10.0.0" majorVersion="1">
    <index root="\" startIndexAt="\">
        <default>
            <qualifier name="Language" value="en-US"/>
            <qualifier name="Contrast" value="standard"/>
            <qualifier name="HomeRegion" value="001"/>
            <qualifier name="TargetSize" value="256"/>
            <qualifier name="LayoutDirection" value="LTR"/>
            <qualifier name="Theme" value="dark"/>
            <qualifier name="AlternateForm" value=""/>
            <qualifier name="DXFeatureLevel" value="DX9"/>
            <qualifier name="Configuration" value=""/>
            <qualifier name="DeviceFamily" value="Universal"/>
            <qualifier name="Custom" value=""/>
        </default>
        <indexer-config type="folder" foldernameAsQualifier="true" filenameAsQualifier="true" qualifierDelimiter="."/>
        <indexer-config type="resw" convertDotsToSlashes="true" initialPath=""/>
        <indexer-config type="resjson" initialPath=""/>
        <indexer-config type="PRI"/>
    </index>
</resources>
```  

<span data-ttu-id="87d97-175">Vous pouvez désormais utiliser le fichier de configuration et l’outil MakePRI pour créer le fichier resources.pri.</span><span class="sxs-lookup"><span data-stu-id="87d97-175">Now you can use the configuration file and the MakePRI tool to create the resources.pri file.</span></span>  <span data-ttu-id="87d97-176">Pour cet exemple, l’emplacement racine du projet sera `[Root folder]` .</span><span class="sxs-lookup"><span data-stu-id="87d97-176">For this example, the root location for the project will be `[Root folder]`.</span></span>  

```cmd
MakePRI new /pr [Root folder] /cf [Root folder]\priconfig.xml /mn [Root folder]\AppxManifest.xml /of [Root folder]\resources.pri /o
```  

<span data-ttu-id="87d97-177">Vous devez maintenant avoir un fichier resources.pri dans votre dossier racine :</span><span class="sxs-lookup"><span data-stu-id="87d97-177">You should now have one resources.pri file in your root folder:</span></span>  

![dossier ressources](../../media/resources.png)  

## <a name="localizing-name-and-description-in-the-microsoft-store"></a><span data-ttu-id="87d97-179">Localisation du nom et de la description dans le Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="87d97-179">Localizing name and description in the Microsoft Store</span></span>  

<span data-ttu-id="87d97-180">Une fois que vous essayez de télécharger votre package complet et localisé, le Centre de développement Windows détecte que plusieurs langues sont pris en charge et vérifie que vous avez des noms et descriptions localisées correspondants pour chacune d’elles.</span><span class="sxs-lookup"><span data-stu-id="87d97-180">Once you try to upload your complete, localized package, the Windows Dev Center will detect that more than one language is supported and check that you have corresponding localized names and descriptions for each.</span></span>  <span data-ttu-id="87d97-181">Si l’une des valeurs localisées est manquante, votre soumission sera bloquée jusqu’à ce que vous fournissiez les valeurs.</span><span class="sxs-lookup"><span data-stu-id="87d97-181">If any of the localized values are missing, your submission will be blocked until you provide the values.</span></span>  

<span data-ttu-id="87d97-182">Si vous souhaitez uniquement fournir un nom et une description localisées pour le Microsoft Store (et non Windows), vous pouvez le faire en réservant tous les noms localisées pour [votre extension](./extensions-in-the-windows-dev-center.md#name-reservation).</span><span class="sxs-lookup"><span data-stu-id="87d97-182">If you are only interested in providing a localized name and description for the Microsoft Store (and not Windows), you can do so by [reserving all the localized names for your extension](./extensions-in-the-windows-dev-center.md#name-reservation).</span></span>  

<span data-ttu-id="87d97-183">Une fois que vous avez réservé d’autres noms localisées, vous pouvez créer une soumission mise à jour.</span><span class="sxs-lookup"><span data-stu-id="87d97-183">Once you've reserved additional localized names, you can create an updated submission.</span></span>  <span data-ttu-id="87d97-184">Dans la section description, vous pouvez gérer des langues supplémentaires pour votre description dans le Microsoft Store :</span><span class="sxs-lookup"><span data-stu-id="87d97-184">In the description section you can manage additional languages for your Microsoft Store listing:</span></span>  

![Gérer les langues de description](../../media/manage-description-languages.png)  

<span data-ttu-id="87d97-186">Une fois que vous avez sélectionné Gérer les **langues**supplémentaires, vous pouvez sélectionner les langues que vous souhaitez ajouter à votre liste du Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="87d97-186">Once you've selected **Manage additional languages**, you'll get to select which languages you want to add to your Microsoft Store listing.</span></span>  <span data-ttu-id="87d97-187">La nouvelle langue s’affiche en tant que **langue de description supplémentaire** dans la section **Description.**</span><span class="sxs-lookup"><span data-stu-id="87d97-187">The new language will show up as **Additional description language** in the **Description** section.</span></span>  

<span data-ttu-id="87d97-188">Vous pouvez cliquer sur le lien individuel dans la section **Description** pour fournir un nom et une description localisées, des notes de publication et des ressources visuelles pour chaque langue.</span><span class="sxs-lookup"><span data-stu-id="87d97-188">You can click on the individual link in the **Description** section to provide a localized name and description, release notes, and visual assets for each language.</span></span>  <span data-ttu-id="87d97-189">La description du Microsoft Store n’est pas extraite du AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="87d97-189">The description for the Microsoft Store is not extracted from the AppXManifest.</span></span>  <span data-ttu-id="87d97-190">Chaque description localisée doit être entrée manuellement dans le Centre de développement Windows :</span><span class="sxs-lookup"><span data-stu-id="87d97-190">Each localized description needs to be manually entered in the Windows Dev Center:</span></span>  

![Description de l’application japonaise](../../media/japanese-app-description.png)  

<span data-ttu-id="87d97-192">Une fois les descriptions localisées envoyées et l’extension publiée, toute personne accédant à une page localisée de l’extension dans le Microsoft Store verra l’interface utilisateur suivante :</span><span class="sxs-lookup"><span data-stu-id="87d97-192">Once the localized descriptions are submitted and the extension is published, anyone accessing a localized page of the extension in the Microsoft Store will see the following UI:</span></span>  

![windows store japonais](../../media/japanese-windows-store.png)  

## <a name="appxmanifest-samples"></a><span data-ttu-id="87d97-194">Exemples AppxManifest</span><span class="sxs-lookup"><span data-stu-id="87d97-194">AppxManifest samples</span></span>  

### <a name="non-localized-appxmanifest"></a><span data-ttu-id="87d97-195">AppxManifest non localisée</span><span class="sxs-lookup"><span data-stu-id="87d97-195">Non-localized AppxManifest</span></span>  

<span data-ttu-id="87d97-196">L’exemple suivant montre un AppxManifest qui n’est pas localisée et prend uniquement en charge les `en-us` paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="87d97-196">The following example shows an AppxManifest that isn't localized, and only supports the `en-us` locale.</span></span>  

```xml
<?xml version="1.0" encoding="utf-8"?>
<Package
    xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10"
    xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10"
    xmlns:uap3="http://schemas.microsoft.com/appx/manifest/uap/windows10/3"
    IgnorableNamespaces="uap3">
    <Identity
        Name="63533cct23.Jigsaw"
        Publisher="CN=932A7C4A-0308-4632-9E2F-5931E8F02B7C"
        Version="1.3.0.0" />

    <Properties>
        <DisplayName>Jigsaw</DisplayName>
        <PublisherDisplayName>cct23</PublisherDisplayName>
        <Logo>Assets\icon-50.png</Logo>
    </Properties>

    <Dependencies>
        <TargetDeviceFamily Name="Windows.Desktop" MinVersion="10.0.14393.0" MaxVersionTested="10.0.14800.0" />
    </Dependencies>

    <Resources>
        <Resource Language="en-us" />
    </Resources>

    <Applications>
        <Application Id="App">
            <uap:VisualElements
                AppListEntry="none"
                DisplayName="Jigsaw"
                Square150x150Logo="Assets\icon-150.png"
                Square44x44Logo="Assets\icon-44.png"
                Description="This is a jigsaw puzzle app"
                BackgroundColor="transparent">
            </uap:VisualElements>
            <Extensions>
                <uap3:Extension Category="windows.appExtension">
                    <uap3:AppExtension
                        Name="com.microsoft.edge.extension"
                        Id="EdgeExtension"
                        PublicFolder="Extension"
                        DisplayName="Jigsaw">
                        <uap3:Properties>
                            <Capabilities>
                                <Capability Name="websiteContent"/>
                                <Capability Name="websiteInfo"/>
                                <Capability Name="browserStorage"/>
                            </Capabilities>
                        </uap3:Properties>
                    </uap3:AppExtension>
                </uap3:Extension>
            </Extensions>
        </Application>
    </Applications>
</Package>
```  

#### <a name="localized-appxmanifest"></a><span data-ttu-id="87d97-197">Localized AppxManifest</span><span class="sxs-lookup"><span data-stu-id="87d97-197">Localized AppxManifest</span></span>  

<span data-ttu-id="87d97-198">Cet exemple AppxManifest est localisé pour huit autres paramètres régionaux en plus de « en-us ».</span><span class="sxs-lookup"><span data-stu-id="87d97-198">This AppxManifest sample is localized for eight other locales besides "en-us".</span></span> <span data-ttu-id="87d97-199">Notez les `ms-resource:<resource id>` occurrences :</span><span class="sxs-lookup"><span data-stu-id="87d97-199">Notice the `ms-resource:<resource id>` occurrences:</span></span>  

```xml
<?xml version="1.0" encoding="utf-8"?>
<Package
    xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10"
    xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10"
    xmlns:uap3="http://schemas.microsoft.com/appx/manifest/uap/windows10/3"
    IgnorableNamespaces="uap3">
    <Identity
        Name="63533cct23.Jigsaw"
        Publisher="CN=932A7C4A-0308-4632-9E2F-5931E8F02B7C"
        Version="1.3.0.0" />

    <Properties>
        <DisplayName>ms-resource:DisplayName</DisplayName>
        <PublisherDisplayName>cct23</PublisherDisplayName>
        <Logo>Assets\icon-50.png</Logo>
    </Properties>

    <Dependencies>
        <TargetDeviceFamily Name="Windows.Desktop" MinVersion="10.0.14393.0" MaxVersionTested="10.0.14800.0" />
    </Dependencies>

    <Resources>
        <Resource Language="en-us" />
        <Resource Language="de" />
        <Resource Language="en" />
        <Resource Language="en-gb" />
        <Resource Language="es" />
        <Resource Language="fr" />
        <Resource Language="it" />
        <Resource Language="ja" />
        <Resource Language="zh-cn" />
    </Resources>

    <Applications>
        <Application Id="App">
            <uap:VisualElements
                AppListEntry="none"
                DisplayName="ms-resource:DisplayName"
                Square150x150Logo="Assets\icon-150.png"
                Square44x44Logo="Assets\icon-44.png"
                Description="ms-resource:Description"
                BackgroundColor="transparent">
            </uap:VisualElements>
            <Extensions>
                <uap3:Extension Category="windows.appExtension">
                    <uap3:AppExtension
                        Name="com.microsoft.edge.extension"
                        Id="EdgeExtension"
                        PublicFolder="Extension"
                        DisplayName="ms-resource:DisplayName">
                        <uap3:Properties>
                            <Capabilities>
                                <Capability Name="websiteContent"/>
                                <Capability Name="websiteInfo"/>
                                <Capability Name="browserStorage"/>
                            </Capabilities>
                        </uap3:Properties>
                    </uap3:AppExtension>
                </uap3:Extension>
            </Extensions>
        </Application>
    </Applications>
</Package>
```  
