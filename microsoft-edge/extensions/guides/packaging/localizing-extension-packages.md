---
ms.assetid: c4043c1e-15ac-4210-8851-3804c7708f49
description: Découvrez comment localiser votre package d’extension Microsoft Edge de façon à ce qu’il soit prêt à être utilisé pour plusieurs paramètres régionaux lors de la publication.
title: Localiser des packages d’extension
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.custom: seodec18
ms.openlocfilehash: a6a920b80e915bb14c7ea24abcc54105e5b34eb0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565311"
---
# <span data-ttu-id="5e552-104">Localization des extensions Microsoft Edge pour Windows et de la boutique Microsoft</span><span class="sxs-lookup"><span data-stu-id="5e552-104">Localizing Microsoft Edge extensions for Windows and the Microsoft Store</span></span>  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

<span data-ttu-id="5e552-105">Ce guide décrit comment localiser votre extension Microsoft Edge de manière à ce qu’elle soit prête pour plusieurs paramètres régionaux lors de la publication.</span><span class="sxs-lookup"><span data-stu-id="5e552-105">This guide walks through how to localize your Microsoft Edge extension so that it's ready for multiple locales upon release.</span></span> <span data-ttu-id="5e552-106">Pour localiser entièrement votre extension, vous devez suivre les étapes à suivre pour Windows et le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="5e552-106">To fully localize your extension, you'll need to follow the steps for both Windows and the Microsoft Store.</span></span>

<span data-ttu-id="5e552-107">Si vous souhaitez localiser vos ressources d’extension pour Microsoft Edge, vous pouvez apprendre à utiliser l’infrastructure i18n du [Guide d’internationalisation](../internationalization.md).</span><span class="sxs-lookup"><span data-stu-id="5e552-107">If you want to localize your extension resources for Microsoft Edge, you can learn how to use the i18n framework in the [Internationalization guide](../internationalization.md).</span></span>


> [!NOTE]
> <span data-ttu-id="5e552-108">Si votre extension ne prend pas en charge plusieurs langues, vous pouvez ignorer [le nom et la description de la localisation dans la boutique Microsoft](#localizing-name-and-description-in-the-microsoft-store).</span><span class="sxs-lookup"><span data-stu-id="5e552-108">If your extension doesn't support multiple languages, you can skip to [Localizing name and description in the Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).</span></span>


## <span data-ttu-id="5e552-109">Présentation du processus de localisation</span><span class="sxs-lookup"><span data-stu-id="5e552-109">The localization process overview</span></span>

<span data-ttu-id="5e552-110">La première étape à suivre pour rendre votre extension accessible à un large public consiste à [configurer son AppxManifest](#configuring-the-appxmanifest) pour plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="5e552-110">The first step towards getting your extension available to a wide audience is to [configure its AppxManifest](#configuring-the-appxmanifest) for multiple languages.</span></span> <span data-ttu-id="5e552-111">Dans le Microsoft Store, les utilisateurs indiquent les langues prises en charge par votre extension.</span><span class="sxs-lookup"><span data-stu-id="5e552-111">In the Microsoft Store, this will show users what languages your extension supports.</span></span> <span data-ttu-id="5e552-112">Vous devez également modifier certains champs du AppxManifest si vous voulez que le nom de votre extension soit [localisé dans l’interface utilisateur Windows et dans le Microsoft Store](#localizing-extension-resources-for-windows-and-the-microsoft-store).</span><span class="sxs-lookup"><span data-stu-id="5e552-112">Certain fields in the AppxManifest will also need to be changed if you want the name of your extension to be [localized in the Windows UI and the Microsoft Store](#localizing-extension-resources-for-windows-and-the-microsoft-store).</span></span>


<span data-ttu-id="5e552-113">Une fois votre AppxManifest configuré, vous devez créer des [ressources de chaîne JSON](#creating-json-string-resources) pour les langues que vous avez indiquées comme prises en charge.</span><span class="sxs-lookup"><span data-stu-id="5e552-113">Once your AppxManifest is configured, you'll need to [create JSON string resources](#creating-json-string-resources) for the languages that you indicated as supported.</span></span> <span data-ttu-id="5e552-114">Pour cela, il est nécessaire de créer un fichier. resjson pour chaque langue, dans lequel chaque fichier comporte toutes les chaînes d’interface utilisateur de ce langage.</span><span class="sxs-lookup"><span data-stu-id="5e552-114">This requires creating a .resjson file for each language, where each file has all the UI strings of that language within it.</span></span>


<span data-ttu-id="5e552-115">Une fois les fichiers. resjson pour les langues prises en charge effectuées, [vous devez créer un fichier de ressources. pri](#creating-the-resources-file).</span><span class="sxs-lookup"><span data-stu-id="5e552-115">After the .resjson files for the supported languages have been made, a [.pri resource file will need to be created](#creating-the-resources-file).</span></span> <span data-ttu-id="5e552-116">Cette opération sera créée à l’aide d’un fichier de configuration pour l’outil **MakePRI** inclus dans le [Kit de développement logiciel (SDK) Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span><span class="sxs-lookup"><span data-stu-id="5e552-116">This will be created by using a configuration file to the **MakePRI** tool that comes with the [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span></span> 

> [!NOTE]
> <span data-ttu-id="5e552-117">Si vous téléchargez uniquement le kit de développement logiciel (SDK) Windows 10 pour utiliser l’outil MakePri. exe, vous pouvez sélectionner uniquement les fonctionnalités «outils de signature du SDK Windows pour les applications de bureau» et «SDK Windows pour les applications gérées UWP» pour maintenir le téléchargement plus clair.</span><span class="sxs-lookup"><span data-stu-id="5e552-117">If you are only downloading the Windows 10 SDK to use the MakePri.exe tool, you can select only the "Windows SDK Signing Tools for Desktop Apps" and "Windows SDK for UWP Managed Apps" features to keep the download lighter.</span></span> <span data-ttu-id="5e552-118">L’outil MakePri. exe s’affiche dans les sous-dossiers de C:\Program Files (x86) \Windows Kits\10\bin\10.0.17713.0.</span><span class="sxs-lookup"><span data-stu-id="5e552-118">The MakePri.exe tool will appear in subfolders of C:\Program Files (x86)\Windows Kits\10\bin\10.0.17713.0.</span></span>


<span data-ttu-id="5e552-119">Une fois que vous avez téléchargé votre extension, la dernière étape consiste à [localiser le nom et la description dans le Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).</span><span class="sxs-lookup"><span data-stu-id="5e552-119">Once you've uploaded your extension, the final step is to [localize the name and description in the Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).</span></span>

> [!NOTE]
> <span data-ttu-id="5e552-120">Le fait de soumettre une extension Microsoft Edge au Microsoft Store est actuellement une fonctionnalité restreinte.</span><span class="sxs-lookup"><span data-stu-id="5e552-120">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="5e552-121">Contactez [-nous](https://aka.ms/extension-request) pour obtenir vos demandes en tant que partie du Microsoft Store et nous vous enverrons une prochaine mise à jour.</span><span class="sxs-lookup"><span data-stu-id="5e552-121">[Reach out to us](https://aka.ms/extension-request) with your requests to be a part of the Microsoft Store, and we'll consider you for a future update.</span></span>



## <span data-ttu-id="5e552-122">Configuration du AppXManifest</span><span class="sxs-lookup"><span data-stu-id="5e552-122">Configuring the AppXManifest</span></span>

<span data-ttu-id="5e552-123">La liste des langues prises en charge par votre extension dans le Microsoft Store est générée en fonction de ses valeurs AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="5e552-123">Your extension's "Supported languages" list in the Microsoft Store is generated based on its AppXManifest values.</span></span> <span data-ttu-id="5e552-124">Cette liste est spécifiée à l’aide de l' `Resource` élément.</span><span class="sxs-lookup"><span data-stu-id="5e552-124">This list is specified using the `Resource` element.</span></span>


![image des paramètres](./../../media/language-app-details.png)

<span data-ttu-id="5e552-126">Pour spécifier la liste des langues prises en charge par votre extension, vous pouvez ajouter un `Resource` élément dans le format présenté ci-dessous (cet `Resource` élément indique la prise en charge pour l’anglais, l’allemand et le français dans la boutique Microsoft):</span><span class="sxs-lookup"><span data-stu-id="5e552-126">To specify the list of languages that are supported by your extension, you can add a `Resource` element in the format seen below (this `Resource` element will show support for English, German, and French in the Microsoft Store):</span></span>

```xml
<Resources>
    <Resource Language="en-us"/>
    <Resource Language="de-de"/>
    <Resource Language="fr-fr"/>
</Resources>
```

<span data-ttu-id="5e552-127">Pour plus d’informations sur les langues et les codes de langue pris en charge par le Microsoft Store, voir [langues prises en charge](https://msdn.microsoft.com/windows/uwp/publish/supported-languages) .</span><span class="sxs-lookup"><span data-stu-id="5e552-127">See [Supported languages](https://msdn.microsoft.com/windows/uwp/publish/supported-languages) for info on the languages/language codes that the Microsoft Store supports.</span></span>


<span data-ttu-id="5e552-128">Pour spécifier des chaînes localisées pour tous les éléments visibles publiquement dans le AppxManifest, vous devez utiliser un identificateur de ressource au format de `ms-resource:<resource id>` .</span><span class="sxs-lookup"><span data-stu-id="5e552-128">In order to specify localized strings for all publicly visible elements in the AppxManifest, you'll have to use a resource identifier in the format of `ms-resource:<resource id>`.</span></span>

<span data-ttu-id="5e552-129">Les extraits de niveau suivants constituent un AppxManifest complet.</span><span class="sxs-lookup"><span data-stu-id="5e552-129">The snippets below make a complete AppxManifest.</span></span> <span data-ttu-id="5e552-130">Les valeurs suivantes doivent être extraites des fichiers de ressources localisées:</span><span class="sxs-lookup"><span data-stu-id="5e552-130">The following values should be retrieved from localized resource files:</span></span>

- <span data-ttu-id="5e552-131">Properties\DisplayName</span><span class="sxs-lookup"><span data-stu-id="5e552-131">Properties\DisplayName</span></span>
- <span data-ttu-id="5e552-132">Properties\Description</span><span class="sxs-lookup"><span data-stu-id="5e552-132">Properties\Description</span></span>
- <span data-ttu-id="5e552-133">Properties\PublisherDisplayName</span><span class="sxs-lookup"><span data-stu-id="5e552-133">Properties\PublisherDisplayName</span></span>


```xml
<Properties>
    <DisplayName>ms-resource:DisplayName</DisplayName>
    <Description>ms-resource:Description</Description>
    <Logo>Assets\PackageLogo.png</Logo>
    <PublisherDisplayName>ms-resource:PublisherName</PublisherDisplayName>
</Properties>
```

- <span data-ttu-id="5e552-134">Applications\Application\VisualElements\DisplayName</span><span class="sxs-lookup"><span data-stu-id="5e552-134">Applications\Application\VisualElements\DisplayName</span></span>
- <span data-ttu-id="5e552-135">Applications\Application\VisualElements\Description</span><span class="sxs-lookup"><span data-stu-id="5e552-135">Applications\Application\VisualElements\Description</span></span>
- <span data-ttu-id="5e552-136">Applications\Application\Extensions\Extension\AppExtension\DisplayName</span><span class="sxs-lookup"><span data-stu-id="5e552-136">Applications\Application\Extensions\Extension\AppExtension\DisplayName</span></span>

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


## <span data-ttu-id="5e552-137">Localization des ressources d’extension pour Windows et Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="5e552-137">Localizing extension resources for Windows and the Microsoft Store</span></span>

<span data-ttu-id="5e552-138">À présent que votre AppxManifest est configuré pour plusieurs langues, il existe quelques principales différences que vous devez connaître entre la localisation de l’interface utilisateur dans votre extension et la localisation de votre extension pour Windows et Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="5e552-138">Now that your AppxManifest is configured for multiple languages, there are some key differences you should know between localizing the UI within your extension and localizing your extension for Windows and the Microsoft Store.</span></span>

<span data-ttu-id="5e552-139">Si les extensions Microsoft Edge ne s’exécutent pas en dehors de Microsoft Edge, la gestion de celles-ci peut avoir lieu dans Windows.</span><span class="sxs-lookup"><span data-stu-id="5e552-139">While Microsoft Edge extensions don't run outside of Microsoft Edge, the management of them can occur within Windows.</span></span> <span data-ttu-id="5e552-140">Par exemple, les utilisateurs peuvent gérer leurs extensions dans l’application Paramètres:</span><span class="sxs-lookup"><span data-stu-id="5e552-140">For example, users can manage their extensions in the Settings app:</span></span>


![image des paramètres](./../../media/settings.png)



<span data-ttu-id="5e552-142">Le nom de l’extension qui s’affiche dans l’application paramètres de Windows provient du AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="5e552-142">The name of the extension that shows up in the Settings app in Windows comes from the AppXManifest.</span></span> <span data-ttu-id="5e552-143">Si cette valeur est codée en anglais, la version anglaise du nom s’affichera sur les appareils Windows non anglais.</span><span class="sxs-lookup"><span data-stu-id="5e552-143">If this value is hardcoded in English, the English version of the name will show up on non-English Windows devices.</span></span> <span data-ttu-id="5e552-144">S’il s’agit de la personnalisation de votre extension uniquement en anglais, il est bon de laisser celle-ci en dur.</span><span class="sxs-lookup"><span data-stu-id="5e552-144">If the branding of your extension is English only, it's ok to leave it hardcoded.</span></span>


> [!NOTE]
> <span data-ttu-id="5e552-145">Si vous souhaitez utiliser des noms localisés pour votre extension Microsoft Edge dans Windows, assurez-vous que les noms localisés sont également [disponibles et réservés](./extensions-in-the-windows-dev-center.md#name-reservation) avant d’apporter des modifications dans le fichier AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="5e552-145">If you want to use localized names for your Microsoft Edge Extension in Windows, make sure the localized names are also [available and reserved](./extensions-in-the-windows-dev-center.md#name-reservation) before you make the changes in the AppXManifest file.</span></span> <span data-ttu-id="5e552-146">Si les noms ne sont pas réservés, le message d’erreur suivant apparaît lorsque vous téléchargez le package final dans le centre de développement Windows:</span><span class="sxs-lookup"><span data-stu-id="5e552-146">If the names are not reserved, you'll get the following error when you upload the final package to Windows Dev Center:</span></span></br></br>

![erreur de langue](./../../media/language-error.png)</br></br>


<span data-ttu-id="5e552-148">L’infrastructure de localisation basée sur i18n définie pour les extensions JavaScript s’applique uniquement au sein de l’environnement Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5e552-148">The i18n based localization infrastructure that's defined for JavaScript extensions is only applicable within the Microsoft Edge environment.</span></span>

<span data-ttu-id="5e552-149">Hors de Microsoft Edge, dans Windows et dans la boutique Microsoft, la seule infrastructure de localisation prise en charge est basée sur l’infrastructure de localisation de plateforme Windows universelle (UWP).</span><span class="sxs-lookup"><span data-stu-id="5e552-149">Outside of Microsoft Edge, within Windows and the Microsoft Store, the only supported localization framework is based on the Universal Windows Platform (UWP) localization framework.</span></span>

<span data-ttu-id="5e552-150">Bien que nous puissions prendre en charge les ressources basées sur JSON pour les applications Windows HTML, le schéma des ressources JSON ne correspond pas à celui défini pour les extensions JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5e552-150">While we do support JSON based resources for HTML based Windows apps, the schema for the JSON resources doesn't match the one defined for JavaScript extensions.</span></span>


<span data-ttu-id="5e552-151">Voici les principales différences entre les [applications Windows html](https://msdn.microsoft.com/library/windows/apps/hh465228.aspx):</span><span class="sxs-lookup"><span data-stu-id="5e552-151">The following are the key differences in [HTML based Windows apps](https://msdn.microsoft.com/library/windows/apps/hh465228.aspx):</span></span>
-    <span data-ttu-id="5e552-152">Les ressources sont spécifiées dans des fichiers. resjson au lieu de fichiers. JSON.</span><span class="sxs-lookup"><span data-stu-id="5e552-152">Resources are specified in .resjson files instead of .json files.</span></span>
-    <span data-ttu-id="5e552-153">Les valeurs locales prises en charge doivent être spécifiées dans le fichier AppXManifest, avec les paramètres régionaux par défaut.</span><span class="sxs-lookup"><span data-stu-id="5e552-153">The locales supported should be specified in the AppXManifest file, with the first locale being the default locale.</span></span>
-    <span data-ttu-id="5e552-154">Les ressources basées sur le format HTML des applications Windows utilisent le schéma suivant:</span><span class="sxs-lookup"><span data-stu-id="5e552-154">HTML based Windows apps resources use the following schema:</span></span>
    ```json
    {
        "greeting"              : "Hello",
        "_greeting.comment"     : "A welcome greeting.",

        "farewell"              : "Goodbye",
        "_farewell.comment"     : "A goodbye."
    }
    ```
    <span data-ttu-id="5e552-155">La paire nom/valeur désignée par un trait de soulignement est des commentaires pour la ressource de chaîne correspondante.</span><span class="sxs-lookup"><span data-stu-id="5e552-155">The name/value pair denoted by an underscore are comments for the corresponding string resource.</span></span>
-    <span data-ttu-id="5e552-156">les fichiers. resjson sont compilés dans des fichiers. pri qui doivent être inclus lors de la création du package AppX.</span><span class="sxs-lookup"><span data-stu-id="5e552-156">.resjson files are compiled into .pri files which must be included during AppX package creation.</span></span>


### <span data-ttu-id="5e552-157">Création de ressources de type chaîne JSON</span><span class="sxs-lookup"><span data-stu-id="5e552-157">Creating JSON string resources</span></span>
<span data-ttu-id="5e552-158">Avec un AppxManifest configuré et les différences entre les infrastructures i18n et de localisation UWP mises en évidence, vous pouvez créer vos fichiers de ressources.</span><span class="sxs-lookup"><span data-stu-id="5e552-158">With a configured AppxManifest in hand and the differences between the i18n and UWP localization frameworks highlighted, you're ready to create your resource files.</span></span>

<span data-ttu-id="5e552-159">Une seule chaîne de ressources dans le manifeste s’applique aux packages d’extension Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5e552-159">Only one resource string in the manifest is applicable to Microsoft Edge extension packages.</span></span> <span data-ttu-id="5e552-160">La `DisplayName` chaîne est généralement localisée dans les extensions JavaScript et peut être facilement mappée aux fichiers. resjson attendus par Windows.</span><span class="sxs-lookup"><span data-stu-id="5e552-160">The `DisplayName` string is commonly localized in JavaScript extensions, and can be easily mapped to the .resjson files that Windows expects.</span></span> <span data-ttu-id="5e552-161">En supposant qu’il s’agit de la seule ressource que vous souhaitez localiser, voici un exemple de fichier. resjson qui doit être créé:</span><span class="sxs-lookup"><span data-stu-id="5e552-161">Assuming that this is the only resource that you would like to localize, here is a sample .resjson file that should be created:</span></span>

```json
{
    "DisplayName"              : "Jigsaw",
    "_DisplayName.comment"     : "Name of extension."
}
```

<span data-ttu-id="5e552-162">L’ID de ressource dans chaque fichier. resjson doit correspondre à l’ID utilisé dans AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="5e552-162">The resource ID in each .resjson file needs to match the ID used in the AppXManifest.</span></span> <span data-ttu-id="5e552-163">À l’aide de l’extrait de resjson ci-dessus, l’entrée AppXManifest correspondante doit être:</span><span class="sxs-lookup"><span data-stu-id="5e552-163">Using the example .resjson snippet above, the corresponding AppXManifest entry should be:</span></span>

`DisplayName="ms-resource:DisplayName"`

<span data-ttu-id="5e552-164">Chaque langue prise en charge par votre extension doit comporter un fichier Resources. resjson et être placé dans la structure de dossiers suivante:</span><span class="sxs-lookup"><span data-stu-id="5e552-164">Each language that your extension supports should have a corresponding resources.resjson file and be placed in the following folder structure:</span></span>

![structure de dossiers de langue](./../../media/resources-folder.png)


### <span data-ttu-id="5e552-166">Création du fichier de ressources</span><span class="sxs-lookup"><span data-stu-id="5e552-166">Creating the resources file</span></span>
<span data-ttu-id="5e552-167">Une fois que vous avez créé tous vos fichiers. resjson, vous êtes prêt à créer votre fichier d’index de ressource de package (PRI).</span><span class="sxs-lookup"><span data-stu-id="5e552-167">Once you've created all your .resjson files, you're ready to create your package resource index (PRI) file.</span></span> <span data-ttu-id="5e552-168">Ce fichier stocke les ressources pour toutes les langues prises en charge.</span><span class="sxs-lookup"><span data-stu-id="5e552-168">This file stores the resources for all your supported languages.</span></span> <span data-ttu-id="5e552-169">Pour cela, vous pouvez utiliser l’outil **MakePRI** inclus dans le kit de développement logiciel (SDK) Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5e552-169">To do this you can use the **MakePRI** tool which is included with the Windows 10 SDK.</span></span>


<span data-ttu-id="5e552-170">Tout d’abord, vous devez créer le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="5e552-170">First you'll need to create the configuration file.</span></span> <span data-ttu-id="5e552-171">Ce paramètre définit les qualificateurs et la plateforme par défaut pour les ressources.</span><span class="sxs-lookup"><span data-stu-id="5e552-171">This defines the default qualifiers and platform for the resources.</span></span> <span data-ttu-id="5e552-172">Pour cet exemple, définissez la langue par défaut en anglais (US) et celle de la plateforme Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5e552-172">For this example, make the default language English (US) and the platform Windows 10.</span></span> <span data-ttu-id="5e552-173">Pour ce faire, créez un fichier fichier priconfig. XML avec le contenu suivant dans le dossier [racine du dossier]:</span><span class="sxs-lookup"><span data-stu-id="5e552-173">To do this, create a priconfig.xml file with the following content in the [Root folder]:</span></span>

![fichier priconfig dans un dossier](./../../media/priconfig.png)


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

<span data-ttu-id="5e552-175">Vous pouvez maintenant utiliser le fichier de configuration et l’outil MakePRI pour créer le fichier Resources. pri.</span><span class="sxs-lookup"><span data-stu-id="5e552-175">Now you can use the configuration file and the MakePRI tool to create the resources.pri file.</span></span> <span data-ttu-id="5e552-176">Pour cet exemple, l’emplacement racine du projet sera [dossier racine].</span><span class="sxs-lookup"><span data-stu-id="5e552-176">For this example, the root location for the project will be [Root folder].</span></span>


```cmd
MakePRI new /pr [Root folder] /cf [Root folder]\priconfig.xml /mn [Root folder]\AppxManifest.xml /of [Root folder]\resources.pri /o
```

<span data-ttu-id="5e552-177">Vous devez maintenant disposer d’un fichier Resources. pri dans votre dossier racine:</span><span class="sxs-lookup"><span data-stu-id="5e552-177">You should now have one resources.pri file in your root folder:</span></span>

![dossier ressources](./../../media/resources.png)


## <span data-ttu-id="5e552-179">Nom et description de la localisation dans la boutique Microsoft</span><span class="sxs-lookup"><span data-stu-id="5e552-179">Localizing name and description in the Microsoft Store</span></span>

<span data-ttu-id="5e552-180">Une fois que vous avez essayé de télécharger votre package complet et localisé, le centre de développement Windows détectera la prise en charge de plusieurs langues et vérifier que vous disposez de noms localisés correspondants et de descriptions pour chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="5e552-180">Once you try to upload your complete, localized package, the Windows Dev Center will detect that more than one language is supported and check that you have corresponding localized names and descriptions for each.</span></span> <span data-ttu-id="5e552-181">Si des valeurs localisées sont manquantes, votre soumission est bloquée jusqu’à ce que vous fournissiez les valeurs.</span><span class="sxs-lookup"><span data-stu-id="5e552-181">If any of the localized values are missing, your submission will be blocked until you provide the values.</span></span>

<span data-ttu-id="5e552-182">Si vous souhaitez uniquement fournir un nom et une description localisés pour le Microsoft Store (et non pour Windows), vous pouvez le faire en [réservant tous les noms localisés pour votre extension](./extensions-in-the-windows-dev-center.md#name-reservation).</span><span class="sxs-lookup"><span data-stu-id="5e552-182">If you are only interested in providing a localized name and description for the Microsoft Store (and not Windows), you can do so by [reserving all the localized names for your extension](./extensions-in-the-windows-dev-center.md#name-reservation).</span></span>


<span data-ttu-id="5e552-183">Une fois que vous avez réservé des noms localisés supplémentaires, vous pouvez créer une soumission mise à jour.</span><span class="sxs-lookup"><span data-stu-id="5e552-183">Once you've reserved additional localized names, you can create an updated submission.</span></span> <span data-ttu-id="5e552-184">Dans la section Description, vous pouvez gérer des langues supplémentaires pour votre description dans le Microsoft Store:</span><span class="sxs-lookup"><span data-stu-id="5e552-184">In the description section you can manage additional languages for your Microsoft Store listing:</span></span>

![Description de l’application japonaise](./../../media/manage-description-languages.png)

<span data-ttu-id="5e552-186">Une fois que vous avez sélectionné «gérer les langues supplémentaires», vous pouvez sélectionner les langues que vous voulez ajouter à votre description dans le Windows Store.</span><span class="sxs-lookup"><span data-stu-id="5e552-186">Once you've selected "Manage additional languages", you'll get to select which languages you want to add to your Microsoft Store listing.</span></span> <span data-ttu-id="5e552-187">La nouvelle langue s’affichera en tant que «langue de description supplémentaire» dans la section «Description».</span><span class="sxs-lookup"><span data-stu-id="5e552-187">The new language will show up as 'Additional description language' in the "Description" section.</span></span>

<span data-ttu-id="5e552-188">Vous pouvez cliquer sur le lien individuel dans la section «Description» pour fournir un nom et une description localisés, des notes de publication et des ressources visuelles pour chaque langue.</span><span class="sxs-lookup"><span data-stu-id="5e552-188">You can click on the individual link in the "Description" section to provide a localized name and description, release notes, and visual assets for each language.</span></span> <span data-ttu-id="5e552-189">La description du Microsoft Store n’est pas extraite du AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="5e552-189">The description for the Microsoft Store is not extracted from the AppXManifest.</span></span> <span data-ttu-id="5e552-190">Chaque description localisée doit être entrée manuellement dans le centre de développement Windows:</span><span class="sxs-lookup"><span data-stu-id="5e552-190">Each localized description needs to be manually entered in the Windows Dev Center:</span></span>

![Description de l’application japonaise](./../../media/japanese-app-description.png)

<span data-ttu-id="5e552-192">Une fois les descriptions localisées soumises et l’extension publiée, quiconque accède à une page localisée de l’extension dans le Microsoft Store verra l’interface utilisateur suivante:</span><span class="sxs-lookup"><span data-stu-id="5e552-192">Once the localized descriptions are submitted and the extension is published, anyone accessing a localized page of the extension in the Microsoft Store will see the following UI:</span></span>

![Windows Store japonais](./../../media/japanese-windows-store.png)
 

## <span data-ttu-id="5e552-194">Exemples de AppxManifest</span><span class="sxs-lookup"><span data-stu-id="5e552-194">AppxManifest samples</span></span>

### <span data-ttu-id="5e552-195">AppxManifest non localisé</span><span class="sxs-lookup"><span data-stu-id="5e552-195">Non-localized AppxManifest</span></span>
<span data-ttu-id="5e552-196">L’exemple suivant montre un AppxManifest qui n’est pas localisé et ne prend en charge que les paramètres régionaux «en-US».</span><span class="sxs-lookup"><span data-stu-id="5e552-196">The following example shows an AppxManifest that isn't localized, and only supports the "en-us" locale.</span></span>


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


#### <span data-ttu-id="5e552-197">AppxManifest localisé</span><span class="sxs-lookup"><span data-stu-id="5e552-197">Localized AppxManifest</span></span>
<span data-ttu-id="5e552-198">Cet exemple AppxManifest est localisé pour huit autres paramètres régionaux en plus de «en-US».</span><span class="sxs-lookup"><span data-stu-id="5e552-198">This AppxManifest sample is localized for eight other locales besides "en-us".</span></span> <span data-ttu-id="5e552-199">Notez les `ms-resource:<resource id>` occurrences suivantes:</span><span class="sxs-lookup"><span data-stu-id="5e552-199">Notice the `ms-resource:<resource id>` occurrences:</span></span>


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
