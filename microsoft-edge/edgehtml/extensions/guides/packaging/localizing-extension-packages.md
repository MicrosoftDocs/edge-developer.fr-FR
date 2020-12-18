---
ms.assetid: c4043c1e-15ac-4210-8851-3804c7708f49
description: Découvrez comment localiser votre package d’extension Microsoft Edge de façon à ce qu’il soit prêt à être utilisé pour plusieurs paramètres régionaux lors de la publication.
title: Localisation des packages d’extension
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.custom: seodec18
ms.date: 12/15/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cfa85eda47fd71099bb5d201d1cf85992931228c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233377"
---
# Localization des extensions Microsoft Edge pour Windows et de la boutique Microsoft  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

Ce guide décrit comment localiser votre extension Microsoft Edge de manière à ce qu’elle soit prête pour plusieurs paramètres régionaux lors de la publication. Pour localiser entièrement votre extension, vous devez suivre les étapes à suivre pour Windows et le Microsoft Store.

Si vous souhaitez localiser vos ressources d’extension pour Microsoft Edge, vous pouvez apprendre à utiliser l’infrastructure i18n du [Guide d’internationalisation](../internationalization.md).


> [!NOTE]
> Si votre extension ne prend pas en charge plusieurs langues, vous pouvez ignorer [le nom et la description de la localisation dans la boutique Microsoft](#localizing-name-and-description-in-the-microsoft-store).


## Présentation du processus de localisation

La première étape à suivre pour rendre votre extension accessible à un large public consiste à [configurer son AppxManifest](#configuring-the-appxmanifest) pour plusieurs langues. Dans le Microsoft Store, les utilisateurs indiquent les langues prises en charge par votre extension. Vous devez également modifier certains champs du AppxManifest si vous voulez que le nom de votre extension soit [localisé dans l’interface utilisateur Windows et dans le Microsoft Store](#localizing-extension-resources-for-windows-and-the-microsoft-store).


Une fois votre AppxManifest configuré, vous devez créer des [ressources de chaîne JSON](#creating-json-string-resources) pour les langues que vous avez indiquées comme prises en charge. Pour cela, il est nécessaire de créer un fichier. resjson pour chaque langue, dans lequel chaque fichier comporte toutes les chaînes d’interface utilisateur de ce langage.


Une fois les fichiers. resjson pour les langues prises en charge effectuées, [vous devez créer un fichier de ressources. pri](#creating-the-resources-file). Cette opération sera créée à l’aide d’un fichier de configuration pour l’outil **MakePRI** inclus dans le [Kit de développement logiciel (SDK) Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk). 

> [!NOTE]
> Si vous téléchargez uniquement le kit de développement logiciel (SDK) Windows 10 pour utiliser l’outil MakePri.exe, vous ne pouvez sélectionner que les fonctionnalités «outils de signature du SDK Windows pour les applications de bureau» et «kit de développement logiciel (SDK) Windows pour les applications gérées UWP» pour maintenir le téléchargement plus clair. L’outil MakePri.exe apparaît dans des sous-dossiers de C:\Program Files (x86) \Windows Kits\10\bin\10.0.17713.0.


Une fois que vous avez téléchargé votre extension, la dernière étape consiste à [localiser le nom et la description dans le Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).

> [!NOTE]
> Le fait de soumettre une extension Microsoft Edge au Microsoft Store est actuellement une fonctionnalité restreinte. Contactez [-nous](https://aka.ms/extension-request) pour obtenir vos demandes en tant que partie du Microsoft Store et nous vous enverrons une prochaine mise à jour.



## Configuration du AppXManifest

La liste des langues prises en charge par votre extension dans le Microsoft Store est générée en fonction de ses valeurs AppXManifest. Cette liste est spécifiée à l’aide de l' `Resource` élément.


![image des paramètres-détails de l’application de langue](./../../media/language-app-details.png)

Pour spécifier la liste des langues prises en charge par votre extension, vous pouvez ajouter un `Resource` élément dans le format présenté ci-dessous (cet `Resource` élément indique la prise en charge pour l’anglais, l’allemand et le français dans la boutique Microsoft):

```xml
<Resources>
    <Resource Language="en-us"/>
    <Resource Language="de-de"/>
    <Resource Language="fr-fr"/>
</Resources>
```

Pour plus d’informations sur les langues et les codes de langue pris en charge par le Microsoft Store, voir [langues prises en charge](https://msdn.microsoft.com/windows/uwp/publish/supported-languages) .


Pour spécifier des chaînes localisées pour tous les éléments visibles publiquement dans le AppxManifest, vous devez utiliser un identificateur de ressource au format de `ms-resource:<resource id>` .

Les extraits de niveau suivants constituent un AppxManifest complet. Les valeurs suivantes doivent être extraites des fichiers de ressources localisées:

- Properties\DisplayName
- Properties\Description
- Properties\PublisherDisplayName


```xml
<Properties>
    <DisplayName>ms-resource:DisplayName</DisplayName>
    <Description>ms-resource:Description</Description>
    <Logo>Assets\PackageLogo.png</Logo>
    <PublisherDisplayName>ms-resource:PublisherName</PublisherDisplayName>
</Properties>
```

- Applications\Application\VisualElements\DisplayName
- Applications\Application\VisualElements\Description
- Applications\Application\Extensions\Extension\AppExtension\DisplayName

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


## Localization des ressources d’extension pour Windows et Microsoft Store

À présent que votre AppxManifest est configuré pour plusieurs langues, il existe quelques principales différences que vous devez connaître entre la localisation de l’interface utilisateur dans votre extension et la localisation de votre extension pour Windows et Microsoft Store.

Si les extensions Microsoft Edge ne s’exécutent pas en dehors de Microsoft Edge, la gestion de celles-ci peut avoir lieu dans Windows. Par exemple, les utilisateurs peuvent gérer leurs extensions dans l’application Paramètres:


![image des paramètres](./../../media/settings.png)



Le nom de l’extension qui s’affiche dans l’application paramètres de Windows provient du AppXManifest. Si cette valeur est codée en anglais, la version anglaise du nom s’affichera sur les appareils Windows non anglais. S’il s’agit de la personnalisation de votre extension uniquement en anglais, il est bon de laisser celle-ci en dur.


> [!NOTE]
> Si vous souhaitez utiliser des noms localisés pour votre extension Microsoft Edge dans Windows, assurez-vous que les noms localisés sont également [disponibles et réservés](./extensions-in-the-windows-dev-center.md#name-reservation) avant d’apporter des modifications dans le fichier AppXManifest. Si les noms ne sont pas réservés, le message d’erreur suivant apparaît lorsque vous téléchargez le package final dans le centre de développement Windows:</br></br>

![erreur de langue](./../../media/language-error.png)</br></br>


L’infrastructure de localisation basée sur i18n définie pour les extensions JavaScript s’applique uniquement au sein de l’environnement Microsoft Edge.

Hors de Microsoft Edge, dans Windows et dans la boutique Microsoft, la seule infrastructure de localisation prise en charge est basée sur l’infrastructure de localisation de plateforme Windows universelle (UWP).

Bien que nous puissions prendre en charge les ressources basées sur JSON pour les applications Windows HTML, le schéma des ressources JSON ne correspond pas à celui défini pour les extensions JavaScript.


Voici les principales différences entre les [applications Windows html](https://msdn.microsoft.com/library/windows/apps/hh465228.aspx):
-    Les ressources sont spécifiées dans des fichiers. resjson au lieu de fichiers. JSON.
-    Les valeurs locales prises en charge doivent être spécifiées dans le fichier AppXManifest, avec les paramètres régionaux par défaut.
-    Les ressources basées sur le format HTML des applications Windows utilisent le schéma suivant:
    ```json
    {
        "greeting"              : "Hello",
        "_greeting.comment"     : "A welcome greeting.",

        "farewell"              : "Goodbye",
        "_farewell.comment"     : "A goodbye."
    }
    ```
    La paire nom/valeur désignée par un trait de soulignement est des commentaires pour la ressource de chaîne correspondante.
-    les fichiers. resjson sont compilés dans des fichiers. pri qui doivent être inclus lors de la création du package AppX.


### Création de ressources de type chaîne JSON
Avec un AppxManifest configuré et les différences entre les infrastructures i18n et de localisation UWP mises en évidence, vous pouvez créer vos fichiers de ressources.

Une seule chaîne de ressources dans le manifeste s’applique aux packages d’extension Microsoft Edge. La `DisplayName` chaîne est généralement localisée dans les extensions JavaScript et peut être facilement mappée aux fichiers. resjson attendus par Windows. En supposant qu’il s’agit de la seule ressource que vous souhaitez localiser, voici un exemple de fichier. resjson qui doit être créé:

```json
{
    "DisplayName"              : "Jigsaw",
    "_DisplayName.comment"     : "Name of extension."
}
```

L’ID de ressource dans chaque fichier. resjson doit correspondre à l’ID utilisé dans AppXManifest. À l’aide de l’extrait de resjson ci-dessus, l’entrée AppXManifest correspondante doit être:

`DisplayName="ms-resource:DisplayName"`

Chaque langue prise en charge par votre extension doit comporter un fichier Resources. resjson et être placé dans la structure de dossiers suivante:

![structure de dossiers de langue](./../../media/resources-folder.png)


### Création du fichier de ressources
Une fois que vous avez créé tous vos fichiers. resjson, vous êtes prêt à créer votre fichier d’index de ressource de package (PRI). Ce fichier stocke les ressources pour toutes les langues prises en charge. Pour cela, vous pouvez utiliser l’outil **MakePRI** inclus dans le kit de développement logiciel (SDK) Windows 10.


Tout d’abord, vous devez créer le fichier de configuration. Ce paramètre définit les qualificateurs et la plateforme par défaut pour les ressources. Pour cet exemple, définissez la langue par défaut en anglais (US) et celle de la plateforme Windows 10. Pour ce faire, créez un fichier priconfig.xml avec le contenu suivant dans le dossier [racine du dossier]:

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

Vous pouvez maintenant utiliser le fichier de configuration et l’outil MakePRI pour créer le fichier Resources. pri. Pour cet exemple, l’emplacement racine du projet sera [dossier racine].


```cmd
MakePRI new /pr [Root folder] /cf [Root folder]\priconfig.xml /mn [Root folder]\AppxManifest.xml /of [Root folder]\resources.pri /o
```

Vous devez maintenant disposer d’un fichier Resources. pri dans votre dossier racine:

![dossier ressources](./../../media/resources.png)


## Nom et description de la localisation dans la boutique Microsoft

Une fois que vous avez essayé de télécharger votre package complet et localisé, le centre de développement Windows détectera la prise en charge de plusieurs langues et vérifier que vous disposez de noms localisés correspondants et de descriptions pour chacun d’eux. Si des valeurs localisées sont manquantes, votre soumission est bloquée jusqu’à ce que vous fournissiez les valeurs.

Si vous souhaitez uniquement fournir un nom et une description localisés pour le Microsoft Store (et non pour Windows), vous pouvez le faire en [réservant tous les noms localisés pour votre extension](./extensions-in-the-windows-dev-center.md#name-reservation).


Une fois que vous avez réservé des noms localisés supplémentaires, vous pouvez créer une soumission mise à jour. Dans la section Description, vous pouvez gérer des langues supplémentaires pour votre description dans le Microsoft Store:

![Description de l’application japonaise-gestion](./../../media/manage-description-languages.png)

Une fois que vous avez sélectionné «gérer les langues supplémentaires», vous pouvez sélectionner les langues que vous voulez ajouter à votre description dans le Windows Store. La nouvelle langue s’affichera en tant que «langue de description supplémentaire» dans la section «Description».

Vous pouvez cliquer sur le lien individuel dans la section «Description» pour fournir un nom et une description localisés, des notes de publication et des ressources visuelles pour chaque langue. La description du Microsoft Store n’est pas extraite du AppXManifest. Chaque description localisée doit être entrée manuellement dans le centre de développement Windows:

![Description de l’application japonaise](./../../media/japanese-app-description.png)

Une fois les descriptions localisées soumises et l’extension publiée, quiconque accède à une page localisée de l’extension dans le Microsoft Store verra l’interface utilisateur suivante:

![Windows Store japonais](./../../media/japanese-windows-store.png)
 

## Exemples de AppxManifest

### AppxManifest non localisé
L’exemple suivant montre un AppxManifest qui n’est pas localisé et ne prend en charge que les paramètres régionaux «en-US».


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


#### AppxManifest localisé
Cet exemple AppxManifest est localisé pour huit autres paramètres régionaux en plus de «en-US». Notez les `ms-resource:<resource id>` occurrences suivantes:


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
