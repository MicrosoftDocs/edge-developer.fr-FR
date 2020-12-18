---
ms.assetid: 5eefa3d8-8626-4486-bd90-1361400d6468
description: Découvrez comment empaqueter manuellement votre extension Microsoft Edge et la tester pour vérifier qu’elle est correctement empaquetée.
title: Création et test de packages d’extension
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur, empaquetage
ms.custom: seodec18
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 44316f4dd47b3b6b26014ff24673ddfd16a72ddb
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233384"
---
# Création et test d’un package AppX d’extension Microsoft Edge  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

Les extensions Microsoft Edge sont empaquetées en tant qu’AppX, de la même façon que les applications Windows universelles. À compter de la mise à jour anniversaire de Windows 10, un nouveau schéma a été introduit pour AppX qui permet à un AppX d’inclure une extension Microsoft Edge en tant que contenu.

Si vous connaissez déjà le mode de création de l’extension Microsoft Edge AppXs, vous pouvez passer à [l’utilisation de ManifoldJS dans l’extension de package](./using-manifoldjs-to-package-extensions.md) pour savoir comment utiliser un outil Node.js pour effectuer toutes les opérations pour vous.

> [!NOTE]
> Le fait de soumettre une extension Microsoft Edge au Microsoft Store est actuellement une fonctionnalité restreinte. Une fois que vous avez créé, emballé et testé votre poste, envoyez une demande sur notre [formulaire de soumission d’extension](https://aka.ms/extension-request).

## Préparation du dossier de soumission

Pour préparer votre extension pour la soumission, vous devez créer un dossier avec la structure suivante:

![image d’une structure de dossiers. Le dossier extension est AppxManifest.xml, le dossier extension et le dossier ressources](./../../media/packaging_folder-structure.png)

À la racine du dossier, vous devez inclure un fichier AppXManifest.xml. Ce fichier est utilisé pour spécifier le contenu et la disposition du package.

Vous devez également disposer d’un dossier de ressources qui contient les ressources d’interface utilisateur à utiliser dans le Microsoft Store et un dossier d’extension qui contient les fichiers de votre extension (scripts, icônes, etc.).

> [!IMPORTANT]
> Vous pouvez créer une structure de dossiers différente pour votre package, mais la structure des dossiers doit correspondre aux valeurs AppXManifest.

### AppXManifest.xml
Le fichier AppXManifest est un document XML contenant des informations dont le système a besoin pour déployer, afficher ou mettre à jour une application Windows. Ce fichier inclut également une identité de package, des fonctionnalités et des éléments visuels. Chaque package d’application doit inclure un fichier AppXManifest.

Les développeurs peuvent utiliser le modèle suivant pour leur fichier AppXManifest.xml:

```xml
<?xml version="1.0" encoding="utf-8"?>
<Package
  xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10"
  xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10"
  xmlns:uap3="http://schemas.microsoft.com/appx/manifest/uap/windows10/3"
  IgnorableNamespaces="uap3">

  <Identity
    Name="[REPLACE WITH PACKAGE/IDENTITYNAME]"
    Publisher="[REPLACE WITH PACKAGE/IDENTITY/PUBLISHER]"
    Version="[REPLACE WITH PACKAGE VERSION in the form X.X.X.0]"/>

  <Properties>
    <DisplayName>[REPLACE WITH RESERVED STORE NAME]</DisplayName>
    <PublisherDisplayName>[REPLACE WITH PACKAGE/PROPERTIES/PUBLISHERDISPLAYNAME]</PublisherDisplayName>
    <Logo>[REPLACE WITH RELATIVE PATH TO 50x50 ICON]</Logo>
  </Properties>

  <Dependencies>
    <TargetDeviceFamily Name="Windows.Desktop"
      MinVersion="10.0.14393.0"
      MaxVersionTested="10.0.14800.0" />
  </Dependencies>

  <Resources>
    <Resource Language="en-us"/>
  </Resources>

  <Applications>
    <Application Id="App">
      <uap:VisualElements
        AppListEntry="none"
        DisplayName="[REPLACE WITH RESERVED STORE NAME]"
        Square150x150Logo="[REPLACE WITH RELATIVE PATH TO 150x150 ICON]"
        Square44x44Logo="[REPLACE WITH RELATIVE PATH TO 44x44 ICON]"
        Description="This is the description of the extension"
        BackgroundColor="white">
      </uap:VisualElements>
    <Extensions>
    <uap3:Extension Category="windows.appExtension">
    <uap3:AppExtension Name="com.microsoft.edge.extension"
        Id="EdgeExtension"
        PublicFolder="Extension"
      DisplayName="[REPLACE WITH RESERVED STORE NAME]">
    </uap3:AppExtension>
    </uap3:Extension>
    </Extensions>
 </Application>
</Applications>
</Package>
```  

#### Valeurs du modèle d’identité de l’application
Après avoir [réservé le nom de votre extension](./extensions-in-the-windows-dev-center.md#name-reservation) par le biais du centre de développement Windows, vous pouvez trouver les informations d’identité de package nécessaires pour remplacer les valeurs suivantes dans AppXManifest.xml:

-   `Name`
-   `Publisher`
-   `DisplayName`
-   `PublisherDisplayName`

Vous pouvez accéder à la page identité de votre application en procédant comme suit:

1.  Accédez au [Centre de développement Windows](https://developer.microsoft.com/windows/).
2.  Connectez-vous à votre compte de développeur.
3.  Accédez au tableau de bord.
4.  Sélectionnez le nom de votre extension.
    
    ![liste extension](./../../media/select-app.png)
    
5.  Accédez à la page identité de l’application située sous la section gestion des applications (une fois que vous avez enregistré votre application).
    
    ![page identité de l’application](./../../media/app-identity.png)
    
Vous pouvez maintenant remplir le modèle AppXManifest avec des valeurs de la page identité de l’application, comme indiqué dans le modèle:

```xml
<Identity
  Name="37369abigailc.MyExtension"
  Publisher="CN=732F2E5E-B9A6-4243-85F6-A4210F57AA10"
  Version="[REPLACE WITH PACKAGE VERSION in the form X.X.X.0]" />

<Properties>
  <DisplayName>My Extension</DisplayName>
  <PublisherDisplayName>abigailc</PublisherDisplayName>
  <Logo>[REPLACE WITH RELATIVE PATH TO 50x50 ICON]</Logo>
</Properties>
```  

#### Valeurs de modèle de manifeste JSON
Certaines valeurs dans le AppXManifest doivent correspondre à celles définies dans le manifeste JSON. Mettez à jour les valeurs suivantes dans appxmanifest.xml en fonction du manifeste JSON de votre extension:

-   `Version` -Il s’agit de la version répertoriée dans le manifeste JSON de votre extension. La chaîne doit correspondre au format X. X. X. X où le dernier entier doit être 0. Par exemple, 1.2.3.0
    
    ```xml
    <Identity
         Name="37369abigailc.MyExtension"
         Publisher="CN=732F2E5E-B9A6-4243-85F6-A4210F57AA10"
         Version="1.0.0.0" />
    ```  
    
-   `Description` -Il s’agit d’une copie de la description dans le manifeste JSON de votre extension.
    
    ```xml
    <uap:VisualElements
         AppListEntry="none"
         DisplayName="My Extension"
         Square150x150Logo="[REPLACE WITH RELATIVE PATH TO 150x150 ICON]"
         Square44x44Logo="[REPLACE WITH RELATIVE PATH TO 44x44 ICON]"
         Description="This extension will allow you to quickly print by clicking the browser action."
         BackgroundColor="white">
    </uap:VisualElements>
    ```  
    
### Dossier de ressources

Dans le dossier éléments, vous avez besoin de trois tailles d’icônes différentes. Ces icônes seront utilisées dans Microsoft Store et l’interface utilisateur de Windows. Pour plus d’informations sur ces icônes, voir le Guide de [conception](./../design.md#icons-for-packaging) .

![dossier de ressources contenant trois tailles d’icônes](./../../media/assets-folder.png)

Une fois que vous avez créé les ressources d’interface utilisateur nécessaires, mettez à jour AppXManifest.xml pour qu’ils pointent vers les fichiers appropriés:

-   44x44
    
    ```xml
    Square44x44Logo="Assets/icon_44.png"
    ```  
    
-   50 x 50
    
    ```xml
    <Logo>Assets/icon_50.png</Logo>
    ```  
    
-   150x150
    
    ```xml
    Square150x150Logo="Assets/icon_150.png"
    ```  
    
### Dossier d’extension
Copiez vos fichiers d’extension (en laissant la structure de dossiers) dans le dossier extension. Assurez `manifest.json` -vous qu’il est à la racine de votre dossier d’extensions.

![dossier extension dans lequel sont stockés tous les fichiers d’extension](./../../media/extension-folder.png)

### Prise en charge de plus d’un paramètre régional
Si votre extension prend en charge plusieurs langues, vous souhaiterez peut-être configurer le package AppX avec tous les paramètres régionaux dont vous avez besoin pour que l’icône localisée et la description appropriées apparaissent dans le Microsoft Store. Pour plus d’informations, voir [localiser des packages d’extension](./localizing-extension-packages.md) .

### Création d’un AppX

Pour créer un AppX, vous devez trouver le chemin d’accès pour makeappx. Ce contenu se trouve généralement à l’emplacement suivant si vous utilisez un ordinateur 64 bits.

`C:\Program Files (x86)\Windows Kits\10\bin\x64`

Exécutez la commande suivante pour créer le package AppX pour votre extension:

`[Path to makeappx] makeappx pack /h SHA256 /d [Path to package folder created in #1] /p [Path to the appx file that you want to create]`

Cela devrait ressembler à ce qui suit:

`C:\Program Files (x86)\Windows Kits\10\bin\x64>makeappx.exe pack /h SHA256 /d "C:\Extension\My Extension" /p C:\Extension\MyExtension.appx`

### Décompression d’une AppX
Il est possible que vous souhaitiez décompresser une extension AppX déjà générée et l’utiliser comme point de départ pour l’itération suivante de votre extension ou vérifier que l’AppX a été correctement créé.

Pour ce faire, vous pouvez exécuter la commande suivante pour décompresser le package AppX de votre extension Microsoft Edge:

```shell
[Path to makeappx] makeappx unpack /v /p [Path to appx file you want to unpack] /d [Path to the location where you want to create the package folder]
```  

Cela devrait ressembler à ce qui suit lorsque vous remplissez:

```text
C:\Program Files (x86)\Windows Kits\10\bin\x64>makeappx.exe unpack /v /p "C:\Extension\MyExtension.appx" /d "C:\Extension\My Extension"
```  

## Test d’un package AppX

Vous pouvez tester votre package AppX de l’extension Microsoft Edge en le chargement indépendant dans Microsoft Edge. Chargement indépendant le package AppX d’extension est semblable à chargement indépendant une application Windows universelle. Vous devrez créer un certificat pour signer le package, puis ajouter le package à Windows.

### Inscrire

Découvrez [comment créer un certificat de signature de package d’application](https://msdn.microsoft.com/library/windows/desktop/jj835832.aspx) et [Comment signer un package d’application à l’aide de SignTool](https://msdn.microsoft.com/library/windows/desktop/jj835835.aspx) pour plus d’informations sur le processus de signature et de certification des packages.

> [!NOTE]
> Vous n’avez pas besoin de signer un package d’extension avant de l’envoyer au Microsoft Store; le processus d’intégration au Store s’en charge.

Après avoir signé le package avec le certificat que vous avez créé, le certificat n’est toujours pas approuvé par l’ordinateur local pour le déploiement des packages d’application tant que vous ne l’avez pas installé dans le magasin de certificats approuvés de l’ordinateur local. Pour ce faire, vous pouvez utiliser Certutil.exe, qui est fourni avec Windows.

Pour installer des certificats avec WindowsCertutil.exe, exécutez Cmd.exe en tant qu’administrateur et exécutez la commande suivante:

```shell
Certutil -addStore TrustedPeople MyKey.cer
```  

Lorsque les certificats ne sont plus utilisés, il est recommandé de les supprimer en exécutant la commande suivante à partir d’une invite de commandes administrateur:

```shell
Certutil -delStore TrustedPeople certID
```  

La valeur certID correspond au numéro de série du certificat. Pour déterminer le numéro de série du certificat, exécutez la commande suivante:

```shell
Certutil -store TrustedPeople
```  

### Déploiement
Vous pouvez déployer le package AppX de l’extension Microsoft Edge en exécutant la commande suivante dans PowerShell (en tant qu’administrateur):

```powershell
Add-AppxPackage [path to AppX]
```  

## Tests automatisés avec WebDriver

Dans le cadre de la mise à jour anniversaire, vous pouvez charger votre extension par programmation dans Microsoft Edge avec WebDriver, ce qui permet le test automatisé d’extensions lorsque Microsoft Edge est lancé en mode WebDriver. Cela vous permet de configurer des tests automatisés pour toutes les extensions qui manipulent du contenu sur une page et de vérifier que le comportement correct est affiché.

Pour charger votre extension pour les tests automatisés, vous devez enregistrer le dossier de votre extension `%LOCALAPPDATA%\Packages\Microsoft.MicrosoftEdge_8wekyb3d8bbwe\LocalState\` . Lorsque votre extension se trouve dans l' `LocalState` annuaire, vous devez créer un [`EdgeOptions`](https://seleniumhq.github.io/selenium/docs/api/dotnet/html/T_OpenQA_Selenium_Edge_EdgeOptions.htm) objet et lui ajouter la `extensionPaths` fonctionnalité. La valeur de cette fonctionnalité est un tableau de chemins absolus vers les extensions (dans l' `LocalState` Annuaire) que vous voulez charger sur le site lorsque Microsoft Edge démarre en mode WebDriver.

Consultez le [fichier C#](https://github.com/scottlow/Ignite2016/blob/master/Ignite%202016%20WebDriver%20Demo/IgniteWebDriverDemo/Program.cs) suivant pour obtenir un exemple complet d’extensions sur le chargement latéral dans Microsoft Edge avec WebDriver.
