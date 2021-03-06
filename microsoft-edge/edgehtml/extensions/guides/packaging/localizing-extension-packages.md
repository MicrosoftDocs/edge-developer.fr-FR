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
# <a name="localizing-microsoft-edge-extensions-for-windows-and-the-microsoft-store"></a>Localisation des extensions Microsoft Edge pour Windows et le Microsoft Store  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

Ce guide vous guide tout au long de la localisation de votre extension Microsoft Edge afin qu’elle soit prête pour plusieurs paramètres régionaux à la publication.  Pour trouver entièrement votre extension, vous devez suivre les étapes pour Windows et le Microsoft Store.  

Si vous souhaitez localiser vos ressources d’extension pour Microsoft Edge, vous pouvez apprendre à utiliser l’infrastructure i18n dans le [guide d’internationalisation.](../internationalization.md)  

> [!NOTE]
> Si votre extension ne prend pas en charge plusieurs langues, vous pouvez passer à La localisation du nom et de la [description dans le Microsoft Store.](#localizing-name-and-description-in-the-microsoft-store)  

## <a name="the-localization-process-overview"></a>Vue d’ensemble du processus de localisation  

La première étape pour mettre votre extension à la disposition d’un large public consiste à configurer son [AppxManifest](#configuring-the-appxmanifest) pour plusieurs langues.  Dans le Microsoft Store, cela indique aux utilisateurs les langues que votre extension prend en charge.  Certains champs dans appxManifest devront également être modifiés si vous souhaitez que le nom de votre extension soit localisée dans l’interface utilisateur windows et le [Microsoft Store.](#localizing-extension-resources-for-windows-and-the-microsoft-store)  

Une fois votre AppxManifest configuré, vous devez créer des ressources de chaîne [JSON](#creating-json-string-resources) pour les langues que vous avez indiquées comme étant pris en charge.  Cela nécessite la création d’un fichier pour chaque langue, où chaque fichier possède toutes les chaînes d’interface utilisateur de `.resjson` cette langue.  

Une fois que les fichiers pour les langues prises en charge ont été créés, un fichier de ressources `.resjson` [.pri doit être créé.](#creating-the-resources-file) Il sera créé à l’aide d’un fichier de configuration à l’outil MakePRI fourni avec le [SDK Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk).  

> [!NOTE]
> Si vous téléchargez uniquement le SDK Windows 10 pour utiliser l’outil, vous pouvez sélectionner uniquement les outils de signature du `MakePri.exe` **SDK Windows** pour les applications de bureau et le **SDK Windows** pour les fonctionnalités d’application gérée UWP pour que le téléchargement reste plus léger.  `MakePri.exe`L’outil s’affiche dans les sous-ensembles de `C:\Program Files (x86)\Windows Kits\10\bin\10.0.17713.0` .  

Une fois que vous avez chargé votre extension, l’étape finale consiste à trouver le nom et la [description dans le Microsoft Store.](#localizing-name-and-description-in-the-microsoft-store)  

> [!NOTE]
> L’envoi d’une extension Microsoft Edge au Microsoft Store est actuellement une fonctionnalité restreinte.  **Faites-nous part** de vos demandes pour faire partie du Microsoft Store et nous vous envisagerons pour une prochaine mise à jour.  

## <a name="configuring-the-appxmanifest"></a>Configuration d’AppXManifest  

La liste des langues de votre extension prise en charge dans le Microsoft Store est générée en fonction de ses valeurs AppXManifest.  Cette liste est spécifiée à l’aide de `Resource` l’élément.  

![Détails de l’application](../../media/language-app-details.png)  

Pour spécifier la liste des langues qui sont pris en charge par votre extension, vous pouvez ajouter un élément au format ci-dessous \(cet élément affiche la prise en charge de l’anglais, de l’allemand et du français dans le `Resource` `Resource` Microsoft Store\) :  

```xml
<Resources>
    <Resource Language="en-us"/>
    <Resource Language="de-de"/>
    <Resource Language="fr-fr"/>
</Resources>
```  

Pour [plus d’informations](/windows/uwp/publish/supported-languages) sur les langues/codes de langue pris en charge par le Microsoft Store, voir Langues pris en charge.  

Pour spécifier des chaînes localisées pour tous les éléments visibles publiquement dans appxManifest, vous devez utiliser un identificateur de ressource au format `ms-resource:<resource id>` .  

Les extraits de code ci-dessous font un AppxManifest complet. Les valeurs suivantes doivent être récupérées à partir de fichiers de ressources localisées :  

*   Properties\DisplayName  
*   Propriétés\Description  
*   Properties\PublisherDisplayName  

```xml
<Properties>
    <DisplayName>ms-resource:DisplayName</DisplayName>
    <Description>ms-resource:Description</Description>
    <Logo>Assets\PackageLogo.png</Logo>
    <PublisherDisplayName>ms-resource:PublisherName</PublisherDisplayName>
</Properties>
```  

*   Applications\Application\VisualElements\DisplayName  
*   Applications\Application\VisualElements\Description  
*   Applications\Application\Extensions\Extension\AppExtension\DisplayName  

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

## <a name="localizing-extension-resources-for-windows-and-the-microsoft-store"></a>Localisation des ressources d’extension pour Windows et le Microsoft Store  

Maintenant que votre AppxManifest est configuré pour plusieurs langues, il existe quelques différences clés que vous devez connaître entre la recherche de l’interface utilisateur dans votre extension et la recherche de votre extension pour Windows et le Microsoft Store.  

Bien que les extensions Microsoft Edge ne s’exécutent pas en dehors de Microsoft Edge, leur gestion peut se faire dans Windows.  Par exemple, les utilisateurs peuvent gérer leurs extensions dans l’application Paramètres :  

![application de paramètres](../../media/settings.png)  

Le nom de l’extension qui apparaît dans l’application Paramètres dans Windows provient d’AppXManifest.  Si cette valeur est codée en dur en anglais, la version anglaise du nom s’affiche sur les appareils Windows non anglais.  Si la authentification de votre extension est en anglais uniquement, vous ne pourz pas la laisser codée en dur.  

> [!NOTE]
> Si vous souhaitez utiliser des noms localisées pour votre extension Microsoft [](./extensions-in-the-windows-dev-center.md#name-reservation) Edge dans Windows, assurez-vous que les noms localisées sont également disponibles et réservés avant d’apporter les modifications dans le fichier AppXManifest.  Si les noms ne sont pas réservés, vous obtenez l’erreur suivante lorsque vous téléchargez le package final dans le Centre de dév. Windows :  
> 
> ![erreur de langue](../../media/language-error.png)  

L’infrastructure de localisation basée sur i18n définie pour les extensions JavaScript s’applique uniquement dans l’environnement Microsoft Edge.  

En dehors de Microsoft Edge, dans Windows et le Microsoft Store, la seule infrastructure de localisation prise en charge est basée sur l’infrastructure de localisation de plateforme Windows universelle (UWP).  

Bien que nous supportions les ressources basées sur JSON pour les applications Windows basées sur HTML, le schéma des ressources JSON ne correspond pas à celui défini pour les extensions JavaScript.  

Voici les principales différences dans les applications [Windows html](/previous-versions/windows/apps/hh465228(v=win.10)):  

*   Les ressources sont spécifiées dans `.resjson` les fichiers au lieu des `.json` fichiers.  
*   Les paramètres régionaux pris en charge doivent être spécifiés dans le fichier AppXManifest, les premiers paramètres régionaux étant les paramètres régionaux par défaut.  
*   Les ressources d’applications Windows basées sur HTML utilisent le schéma suivant :  
    
    ```json
    {
        "greeting"              : "Hello",
        "_greeting.comment"     : "A welcome greeting.",

        "farewell"              : "Goodbye",
        "_farewell.comment"     : "A goodbye."
    }
    ```  
    
    La paire nom/valeur, qui est notée par un trait de soulignement, est un commentaire de la ressource de chaîne correspondante.  
*   `.resjson` les fichiers sont compilés en fichiers qui doivent être inclus lors de la création du `.pri` package AppX.  
    
### <a name="creating-json-string-resources"></a>Création de ressources de chaîne JSON  

Une fois appxManifest configuré et les différences entre les infrastructure de localisation i18n et UWP mises en évidence, vous êtes prêt à créer vos fichiers de ressources.  

Une seule chaîne de ressource dans le manifeste est applicable aux packages d’extension Microsoft Edge.  La chaîne est généralement localisée dans les extensions JavaScript et peut être facilement mappée aux fichiers que `DisplayName` `.resjson` Windows attend.  En supposant qu’il s’agit de la seule ressource que vous souhaitez localiser, voici un exemple de fichier `.resjson` à créer :  

```json
{
    "DisplayName"              : "Jigsaw",
    "_DisplayName.comment"     : "Name of extension."
}
```  

L’ID de ressource dans chaque fichier doit correspondre à `.resjson` l’ID utilisé dans AppXManifest.  À l’aide de l’exemple d’extrait de code ci-dessus, l’entrée `.resjson` AppXManifest correspondante doit être :  

`DisplayName="ms-resource:DisplayName"`  

Chaque langue que votre extension prend en charge doit avoir un fichier de ressources correspondant et `.resjson` être placée dans la structure de dossiers suivante :  

![structure des dossiers linguistiques](../../media/resources-folder.png)  

### <a name="creating-the-resources-file"></a>Création du fichier de ressources  

Une fois que vous avez créé tous vos fichiers, vous êtes prêt à créer votre fichier d’index de ressource `.resjson` de package \(PRI\).  Ce fichier stocke les ressources pour toutes les langues que vous avez pris en charge.  Pour ce faire, vous pouvez utiliser **l’outil MakePRI** qui est inclus avec le SDK Windows 10.  

Tout d’abord, vous devez créer le fichier de configuration.  Cela définit les qualificateurs et la plateforme par défaut pour les ressources.  Pour cet exemple, faites de la langue par défaut `English (US)` et de la plateforme Windows 10.  Pour ce faire, créez `priconfig.xml` un fichier avec le contenu suivant dans `[Root folder]` :  

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

Vous pouvez désormais utiliser le fichier de configuration et l’outil MakePRI pour créer le fichier resources.pri.  Pour cet exemple, l’emplacement racine du projet sera `[Root folder]` .  

```cmd
MakePRI new /pr [Root folder] /cf [Root folder]\priconfig.xml /mn [Root folder]\AppxManifest.xml /of [Root folder]\resources.pri /o
```  

Vous devez maintenant avoir un fichier resources.pri dans votre dossier racine :  

![dossier ressources](../../media/resources.png)  

## <a name="localizing-name-and-description-in-the-microsoft-store"></a>Localisation du nom et de la description dans le Microsoft Store  

Une fois que vous essayez de télécharger votre package complet et localisé, le Centre de développement Windows détecte que plusieurs langues sont pris en charge et vérifie que vous avez des noms et descriptions localisées correspondants pour chacune d’elles.  Si l’une des valeurs localisées est manquante, votre soumission sera bloquée jusqu’à ce que vous fournissiez les valeurs.  

Si vous souhaitez uniquement fournir un nom et une description localisées pour le Microsoft Store (et non Windows), vous pouvez le faire en réservant tous les noms localisées pour [votre extension](./extensions-in-the-windows-dev-center.md#name-reservation).  

Une fois que vous avez réservé d’autres noms localisées, vous pouvez créer une soumission mise à jour.  Dans la section description, vous pouvez gérer des langues supplémentaires pour votre description dans le Microsoft Store :  

![Gérer les langues de description](../../media/manage-description-languages.png)  

Une fois que vous avez sélectionné Gérer les **langues**supplémentaires, vous pouvez sélectionner les langues que vous souhaitez ajouter à votre liste du Microsoft Store.  La nouvelle langue s’affiche en tant que **langue de description supplémentaire** dans la section **Description.**  

Vous pouvez cliquer sur le lien individuel dans la section **Description** pour fournir un nom et une description localisées, des notes de publication et des ressources visuelles pour chaque langue.  La description du Microsoft Store n’est pas extraite du AppXManifest.  Chaque description localisée doit être entrée manuellement dans le Centre de développement Windows :  

![Description de l’application japonaise](../../media/japanese-app-description.png)  

Une fois les descriptions localisées envoyées et l’extension publiée, toute personne accédant à une page localisée de l’extension dans le Microsoft Store verra l’interface utilisateur suivante :  

![windows store japonais](../../media/japanese-windows-store.png)  

## <a name="appxmanifest-samples"></a>Exemples AppxManifest  

### <a name="non-localized-appxmanifest"></a>AppxManifest non localisée  

L’exemple suivant montre un AppxManifest qui n’est pas localisée et prend uniquement en charge les `en-us` paramètres régionaux.  

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

#### <a name="localized-appxmanifest"></a>Localized AppxManifest  

Cet exemple AppxManifest est localisé pour huit autres paramètres régionaux en plus de « en-us ». Notez les `ms-resource:<resource id>` occurrences :  

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
