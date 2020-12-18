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
# <span data-ttu-id="fcc49-104">Création et test d’un package AppX d’extension Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="fcc49-104">Creating and testing a Microsoft Edge extension AppX package</span></span>  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

<span data-ttu-id="fcc49-105">Les extensions Microsoft Edge sont empaquetées en tant qu’AppX, de la même façon que les applications Windows universelles.</span><span class="sxs-lookup"><span data-stu-id="fcc49-105">Microsoft Edge extensions are packaged as AppX, similar to how Universal Windows Apps are packaged.</span></span> <span data-ttu-id="fcc49-106">À compter de la mise à jour anniversaire de Windows 10, un nouveau schéma a été introduit pour AppX qui permet à un AppX d’inclure une extension Microsoft Edge en tant que contenu.</span><span class="sxs-lookup"><span data-stu-id="fcc49-106">As of Windows 10 Anniversary Update, a new schema has been introduced for AppX that allows an AppX to include a Microsoft Edge extension as its content.</span></span>

<span data-ttu-id="fcc49-107">Si vous connaissez déjà le mode de création de l’extension Microsoft Edge AppXs, vous pouvez passer à [l’utilisation de ManifoldJS dans l’extension de package](./using-manifoldjs-to-package-extensions.md) pour savoir comment utiliser un outil Node.js pour effectuer toutes les opérations pour vous.</span><span class="sxs-lookup"><span data-stu-id="fcc49-107">If you already know how Microsoft Edge extension AppXs are created, you can skip to [Using ManifoldJS to package extension](./using-manifoldjs-to-package-extensions.md) to learn how to use a Node.js based tool to do all of this for you!</span></span>

> [!NOTE]
> <span data-ttu-id="fcc49-108">Le fait de soumettre une extension Microsoft Edge au Microsoft Store est actuellement une fonctionnalité restreinte.</span><span class="sxs-lookup"><span data-stu-id="fcc49-108">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="fcc49-109">Une fois que vous avez créé, emballé et testé votre poste, envoyez une demande sur notre [formulaire de soumission d’extension](https://aka.ms/extension-request).</span><span class="sxs-lookup"><span data-stu-id="fcc49-109">Once you've created, packaged and tested your extension, please submit a request on our [extension submission form](https://aka.ms/extension-request).</span></span>

## <span data-ttu-id="fcc49-110">Préparation du dossier de soumission</span><span class="sxs-lookup"><span data-stu-id="fcc49-110">Preparing the submission folder</span></span>

<span data-ttu-id="fcc49-111">Pour préparer votre extension pour la soumission, vous devez créer un dossier avec la structure suivante:</span><span class="sxs-lookup"><span data-stu-id="fcc49-111">To prepare your extension for submission, you need to create a folder with the following structure:</span></span>

![image d’une structure de dossiers.](./../../media/packaging_folder-structure.png)

<span data-ttu-id="fcc49-114">À la racine du dossier, vous devez inclure un fichier AppXManifest.xml.</span><span class="sxs-lookup"><span data-stu-id="fcc49-114">At the root of the folder, you should include an AppXManifest.xml file.</span></span> <span data-ttu-id="fcc49-115">Ce fichier est utilisé pour spécifier le contenu et la disposition du package.</span><span class="sxs-lookup"><span data-stu-id="fcc49-115">This file is used to specify the contents and layout of the package.</span></span>

<span data-ttu-id="fcc49-116">Vous devez également disposer d’un dossier de ressources qui contient les ressources d’interface utilisateur à utiliser dans le Microsoft Store et un dossier d’extension qui contient les fichiers de votre extension (scripts, icônes, etc.).</span><span class="sxs-lookup"><span data-stu-id="fcc49-116">You should also have an Assets folder which contains the UI assets to be used in the Microsoft Store, and an Extension folder that contains your extension's files (scripts, icons, etc).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fcc49-117">Vous pouvez créer une structure de dossiers différente pour votre package, mais la structure des dossiers doit correspondre aux valeurs AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="fcc49-117">You can create a different folder structure for your package, but the folder structure must match the AppXManifest values.</span></span>

### <span data-ttu-id="fcc49-118">AppXManifest.xml</span><span class="sxs-lookup"><span data-stu-id="fcc49-118">AppXManifest.xml</span></span>
<span data-ttu-id="fcc49-119">Le fichier AppXManifest est un document XML contenant des informations dont le système a besoin pour déployer, afficher ou mettre à jour une application Windows.</span><span class="sxs-lookup"><span data-stu-id="fcc49-119">The AppXManifest file is an XML document that contains info the system needs to deploy, display, or update a Windows app.</span></span> <span data-ttu-id="fcc49-120">Ce fichier inclut également une identité de package, des fonctionnalités et des éléments visuels.</span><span class="sxs-lookup"><span data-stu-id="fcc49-120">This file also includes package identity, capabilities, and visual elements.</span></span> <span data-ttu-id="fcc49-121">Chaque package d’application doit inclure un fichier AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="fcc49-121">Every app package must include one AppXManifest file.</span></span>

<span data-ttu-id="fcc49-122">Les développeurs peuvent utiliser le modèle suivant pour leur fichier AppXManifest.xml:</span><span class="sxs-lookup"><span data-stu-id="fcc49-122">Developers can use the following template for their AppXManifest.xml file:</span></span>

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

#### <span data-ttu-id="fcc49-123">Valeurs du modèle d’identité de l’application</span><span class="sxs-lookup"><span data-stu-id="fcc49-123">App identity template values</span></span>
<span data-ttu-id="fcc49-124">Après avoir [réservé le nom de votre extension](./extensions-in-the-windows-dev-center.md#name-reservation) par le biais du centre de développement Windows, vous pouvez trouver les informations d’identité de package nécessaires pour remplacer les valeurs suivantes dans AppXManifest.xml:</span><span class="sxs-lookup"><span data-stu-id="fcc49-124">Once you've [reserved the name of your extension](./extensions-in-the-windows-dev-center.md#name-reservation) through the Windows Dev Center, you'll be able to find the necessary package identity information needed to replace the following values in AppXManifest.xml:</span></span>

-   `Name`
-   `Publisher`
-   `DisplayName`
-   `PublisherDisplayName`

<span data-ttu-id="fcc49-125">Vous pouvez accéder à la page identité de votre application en procédant comme suit:</span><span class="sxs-lookup"><span data-stu-id="fcc49-125">You can access your App identity page using the following steps:</span></span>

1.  <span data-ttu-id="fcc49-126">Accédez au [Centre de développement Windows](https://developer.microsoft.com/windows/).</span><span class="sxs-lookup"><span data-stu-id="fcc49-126">Navigate to [Windows Dev Center](https://developer.microsoft.com/windows/).</span></span>
2.  <span data-ttu-id="fcc49-127">Connectez-vous à votre compte de développeur.</span><span class="sxs-lookup"><span data-stu-id="fcc49-127">Sign in to your developer account.</span></span>
3.  <span data-ttu-id="fcc49-128">Accédez au tableau de bord.</span><span class="sxs-lookup"><span data-stu-id="fcc49-128">Navigate to the Dashboard.</span></span>
4.  <span data-ttu-id="fcc49-129">Sélectionnez le nom de votre extension.</span><span class="sxs-lookup"><span data-stu-id="fcc49-129">Select the name of your extension.</span></span>
    
    ![liste extension](./../../media/select-app.png)
    
5.  <span data-ttu-id="fcc49-131">Accédez à la page identité de l’application située sous la section gestion des applications (une fois que vous avez enregistré votre application).</span><span class="sxs-lookup"><span data-stu-id="fcc49-131">Navigate to the App identity page which is under the App management section (after you've registered your app).</span></span>
    
    ![page identité de l’application](./../../media/app-identity.png)
    
<span data-ttu-id="fcc49-133">Vous pouvez maintenant remplir le modèle AppXManifest avec des valeurs de la page identité de l’application, comme indiqué dans le modèle:</span><span class="sxs-lookup"><span data-stu-id="fcc49-133">You can now populate the AppXManifest template with values from the App identity page, as indicated in the template:</span></span>

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

#### <span data-ttu-id="fcc49-134">Valeurs de modèle de manifeste JSON</span><span class="sxs-lookup"><span data-stu-id="fcc49-134">JSON manifest template values</span></span>
<span data-ttu-id="fcc49-135">Certaines valeurs dans le AppXManifest doivent correspondre à celles définies dans le manifeste JSON.</span><span class="sxs-lookup"><span data-stu-id="fcc49-135">Some values in the AppXManifest need to match those that are defined in the JSON manifest.</span></span> <span data-ttu-id="fcc49-136">Mettez à jour les valeurs suivantes dans appxmanifest.xml en fonction du manifeste JSON de votre extension:</span><span class="sxs-lookup"><span data-stu-id="fcc49-136">Please update the following values in appxmanifest.xml based on your extension JSON manifest:</span></span>

-   `Version` <span data-ttu-id="fcc49-137">-Il s’agit de la version répertoriée dans le manifeste JSON de votre extension.</span><span class="sxs-lookup"><span data-stu-id="fcc49-137">- This is the version listed in your extension's JSON manifest.</span></span> <span data-ttu-id="fcc49-138">La chaîne doit correspondre au format X. X. X. X où le dernier entier doit être 0.</span><span class="sxs-lookup"><span data-stu-id="fcc49-138">The string needs to match the X.X.X.X format where the last integer has to be 0.</span></span> <span data-ttu-id="fcc49-139">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="fcc49-139">E.g.</span></span> <span data-ttu-id="fcc49-140">1.2.3.0</span><span class="sxs-lookup"><span data-stu-id="fcc49-140">1.2.3.0</span></span>
    
    ```xml
    <Identity
         Name="37369abigailc.MyExtension"
         Publisher="CN=732F2E5E-B9A6-4243-85F6-A4210F57AA10"
         Version="1.0.0.0" />
    ```  
    
-   `Description` <span data-ttu-id="fcc49-141">-Il s’agit d’une copie de la description dans le manifeste JSON de votre extension.</span><span class="sxs-lookup"><span data-stu-id="fcc49-141">- This is a copy of the description in your extension's JSON manifest.</span></span>
    
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
    
### <span data-ttu-id="fcc49-142">Dossier de ressources</span><span class="sxs-lookup"><span data-stu-id="fcc49-142">Assets folder</span></span>

<span data-ttu-id="fcc49-143">Dans le dossier éléments, vous avez besoin de trois tailles d’icônes différentes.</span><span class="sxs-lookup"><span data-stu-id="fcc49-143">Within the Assets folder you will need three different icon sizes.</span></span> <span data-ttu-id="fcc49-144">Ces icônes seront utilisées dans Microsoft Store et l’interface utilisateur de Windows.</span><span class="sxs-lookup"><span data-stu-id="fcc49-144">These icons will be used in the Microsoft Store and the Windows UI.</span></span> <span data-ttu-id="fcc49-145">Pour plus d’informations sur ces icônes, voir le Guide de [conception](./../design.md#icons-for-packaging) .</span><span class="sxs-lookup"><span data-stu-id="fcc49-145">For more information on these icons, see the [Design](./../design.md#icons-for-packaging) guide.</span></span>

![dossier de ressources contenant trois tailles d’icônes](./../../media/assets-folder.png)

<span data-ttu-id="fcc49-147">Une fois que vous avez créé les ressources d’interface utilisateur nécessaires, mettez à jour AppXManifest.xml pour qu’ils pointent vers les fichiers appropriés:</span><span class="sxs-lookup"><span data-stu-id="fcc49-147">Once you've created the necessary UI assets, update AppXManifest.xml to point to the correct files:</span></span>

-   <span data-ttu-id="fcc49-148">44x44</span><span class="sxs-lookup"><span data-stu-id="fcc49-148">44x44</span></span>
    
    ```xml
    Square44x44Logo="Assets/icon_44.png"
    ```  
    
-   <span data-ttu-id="fcc49-149">50 x 50</span><span class="sxs-lookup"><span data-stu-id="fcc49-149">50x50</span></span>
    
    ```xml
    <Logo>Assets/icon_50.png</Logo>
    ```  
    
-   <span data-ttu-id="fcc49-150">150x150</span><span class="sxs-lookup"><span data-stu-id="fcc49-150">150x150</span></span>
    
    ```xml
    Square150x150Logo="Assets/icon_150.png"
    ```  
    
### <span data-ttu-id="fcc49-151">Dossier d’extension</span><span class="sxs-lookup"><span data-stu-id="fcc49-151">Extension folder</span></span>
<span data-ttu-id="fcc49-152">Copiez vos fichiers d’extension (en laissant la structure de dossiers) dans le dossier extension.</span><span class="sxs-lookup"><span data-stu-id="fcc49-152">Copy your extension files (keeping the folder structure) into the Extension folder.</span></span> <span data-ttu-id="fcc49-153">Assurez `manifest.json` -vous qu’il est à la racine de votre dossier d’extensions.</span><span class="sxs-lookup"><span data-stu-id="fcc49-153">Make sure `manifest.json` is at the root your Extension folder.</span></span>

![dossier extension dans lequel sont stockés tous les fichiers d’extension](./../../media/extension-folder.png)

### <span data-ttu-id="fcc49-155">Prise en charge de plus d’un paramètre régional</span><span class="sxs-lookup"><span data-stu-id="fcc49-155">Supporting more than one locale</span></span>
<span data-ttu-id="fcc49-156">Si votre extension prend en charge plusieurs langues, vous souhaiterez peut-être configurer le package AppX avec tous les paramètres régionaux dont vous avez besoin pour que l’icône localisée et la description appropriées apparaissent dans le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="fcc49-156">If your extension supports more than one language, you may want to configure the AppX package with all the locales that you need so that the correct localized icon and description appear in the Microsoft Store.</span></span> <span data-ttu-id="fcc49-157">Pour plus d’informations, voir [localiser des packages d’extension](./localizing-extension-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="fcc49-157">See [Localizing extension packages](./localizing-extension-packages.md) for more information.</span></span>

### <span data-ttu-id="fcc49-158">Création d’un AppX</span><span class="sxs-lookup"><span data-stu-id="fcc49-158">Creating an Appx</span></span>

<span data-ttu-id="fcc49-159">Pour créer un AppX, vous devez trouver le chemin d’accès pour makeappx.</span><span class="sxs-lookup"><span data-stu-id="fcc49-159">To create an Appx, you'll need to find the path for makeappx.</span></span> <span data-ttu-id="fcc49-160">Ce contenu se trouve généralement à l’emplacement suivant si vous utilisez un ordinateur 64 bits.</span><span class="sxs-lookup"><span data-stu-id="fcc49-160">This is usually located in the following location if you're on a 64-bit machine.</span></span>

`C:\Program Files (x86)\Windows Kits\10\bin\x64`

<span data-ttu-id="fcc49-161">Exécutez la commande suivante pour créer le package AppX pour votre extension:</span><span class="sxs-lookup"><span data-stu-id="fcc49-161">Execute the following command to create the AppX package for your extension:</span></span>

`[Path to makeappx] makeappx pack /h SHA256 /d [Path to package folder created in #1] /p [Path to the appx file that you want to create]`

<span data-ttu-id="fcc49-162">Cela devrait ressembler à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="fcc49-162">This should look something like this once you've filled in the paths:</span></span>

`C:\Program Files (x86)\Windows Kits\10\bin\x64>makeappx.exe pack /h SHA256 /d "C:\Extension\My Extension" /p C:\Extension\MyExtension.appx`

### <span data-ttu-id="fcc49-163">Décompression d’une AppX</span><span class="sxs-lookup"><span data-stu-id="fcc49-163">Unpacking an Appx</span></span>
<span data-ttu-id="fcc49-164">Il est possible que vous souhaitiez décompresser une extension AppX déjà générée et l’utiliser comme point de départ pour l’itération suivante de votre extension ou vérifier que l’AppX a été correctement créé.</span><span class="sxs-lookup"><span data-stu-id="fcc49-164">You may want to unpack a previously generated AppX and use it as a starting point for the next iteration of your extension or to confirm that the AppX was created correctly.</span></span>

<span data-ttu-id="fcc49-165">Pour ce faire, vous pouvez exécuter la commande suivante pour décompresser le package AppX de votre extension Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="fcc49-165">To do this, you can execute the following command to unpack the AppX package of your Microsoft Edge extension:</span></span>

```shell
[Path to makeappx] makeappx unpack /v /p [Path to appx file you want to unpack] /d [Path to the location where you want to create the package folder]
```  

<span data-ttu-id="fcc49-166">Cela devrait ressembler à ce qui suit lorsque vous remplissez:</span><span class="sxs-lookup"><span data-stu-id="fcc49-166">This should look something like this when filled out:</span></span>

```text
C:\Program Files (x86)\Windows Kits\10\bin\x64>makeappx.exe unpack /v /p "C:\Extension\MyExtension.appx" /d "C:\Extension\My Extension"
```  

## <span data-ttu-id="fcc49-167">Test d’un package AppX</span><span class="sxs-lookup"><span data-stu-id="fcc49-167">Testing an AppX package</span></span>

<span data-ttu-id="fcc49-168">Vous pouvez tester votre package AppX de l’extension Microsoft Edge en le chargement indépendant dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="fcc49-168">You can test your Microsoft Edge extension AppX package by sideloading it in Microsoft Edge.</span></span> <span data-ttu-id="fcc49-169">Chargement indépendant le package AppX d’extension est semblable à chargement indépendant une application Windows universelle.</span><span class="sxs-lookup"><span data-stu-id="fcc49-169">Sideloading the extension AppX package is similar to sideloading a Universal Windows app.</span></span> <span data-ttu-id="fcc49-170">Vous devrez créer un certificat pour signer le package, puis ajouter le package à Windows.</span><span class="sxs-lookup"><span data-stu-id="fcc49-170">You will need to create a certificate for signing the package, and then add the package to Windows.</span></span>

### <span data-ttu-id="fcc49-171">Inscrire</span><span class="sxs-lookup"><span data-stu-id="fcc49-171">Signing</span></span>

<span data-ttu-id="fcc49-172">Découvrez [comment créer un certificat de signature de package d’application](https://msdn.microsoft.com/library/windows/desktop/jj835832.aspx) et [Comment signer un package d’application à l’aide de SignTool](https://msdn.microsoft.com/library/windows/desktop/jj835835.aspx) pour plus d’informations sur le processus de signature et de certification des packages.</span><span class="sxs-lookup"><span data-stu-id="fcc49-172">See [How to create an app package signing certificate](https://msdn.microsoft.com/library/windows/desktop/jj835832.aspx) and [How to sign an app package using SignTool](https://msdn.microsoft.com/library/windows/desktop/jj835835.aspx) for info on the signing and certification process for packages.</span></span>

> [!NOTE]
> <span data-ttu-id="fcc49-173">Vous n’avez pas besoin de signer un package d’extension avant de l’envoyer au Microsoft Store; le processus d’intégration au Store s’en charge.</span><span class="sxs-lookup"><span data-stu-id="fcc49-173">You do not need to sign an extension package before submitting it to the Microsoft Store; the Store ingestion process will take care of that for you!</span></span>

<span data-ttu-id="fcc49-174">Après avoir signé le package avec le certificat que vous avez créé, le certificat n’est toujours pas approuvé par l’ordinateur local pour le déploiement des packages d’application tant que vous ne l’avez pas installé dans le magasin de certificats approuvés de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="fcc49-174">After you've signed the package with the certificate that you created, the certificate is still not trusted by the local machine for deployment of app packages until you install it into the trusted certificates store of the local computer.</span></span> <span data-ttu-id="fcc49-175">Pour ce faire, vous pouvez utiliser Certutil.exe, qui est fourni avec Windows.</span><span class="sxs-lookup"><span data-stu-id="fcc49-175">You can use Certutil.exe, which comes with Windows to do this.</span></span>

<span data-ttu-id="fcc49-176">Pour installer des certificats avec WindowsCertutil.exe, exécutez Cmd.exe en tant qu’administrateur et exécutez la commande suivante:</span><span class="sxs-lookup"><span data-stu-id="fcc49-176">To install certificates with WindowsCertutil.exe, run Cmd.exe as administrator and run the following command:</span></span>

```shell
Certutil -addStore TrustedPeople MyKey.cer
```  

<span data-ttu-id="fcc49-177">Lorsque les certificats ne sont plus utilisés, il est recommandé de les supprimer en exécutant la commande suivante à partir d’une invite de commandes administrateur:</span><span class="sxs-lookup"><span data-stu-id="fcc49-177">Once the certificates are no longer in use, it is recommended that you remove them by running the following command from an administrator command prompt:</span></span>

```shell
Certutil -delStore TrustedPeople certID
```  

<span data-ttu-id="fcc49-178">La valeur certID correspond au numéro de série du certificat.</span><span class="sxs-lookup"><span data-stu-id="fcc49-178">The certID is the serial number of the certificate.</span></span> <span data-ttu-id="fcc49-179">Pour déterminer le numéro de série du certificat, exécutez la commande suivante:</span><span class="sxs-lookup"><span data-stu-id="fcc49-179">To determine the certificate serial number, run the following command:</span></span>

```shell
Certutil -store TrustedPeople
```  

### <span data-ttu-id="fcc49-180">Déploiement</span><span class="sxs-lookup"><span data-stu-id="fcc49-180">Deploying</span></span>
<span data-ttu-id="fcc49-181">Vous pouvez déployer le package AppX de l’extension Microsoft Edge en exécutant la commande suivante dans PowerShell (en tant qu’administrateur):</span><span class="sxs-lookup"><span data-stu-id="fcc49-181">You can deploy the Microsoft Edge Extension AppX package by running the following command in PowerShell (as administrator):</span></span>

```powershell
Add-AppxPackage [path to AppX]
```  

## <span data-ttu-id="fcc49-182">Tests automatisés avec WebDriver</span><span class="sxs-lookup"><span data-stu-id="fcc49-182">Automated testing with WebDriver</span></span>

<span data-ttu-id="fcc49-183">Dans le cadre de la mise à jour anniversaire, vous pouvez charger votre extension par programmation dans Microsoft Edge avec WebDriver, ce qui permet le test automatisé d’extensions lorsque Microsoft Edge est lancé en mode WebDriver.</span><span class="sxs-lookup"><span data-stu-id="fcc49-183">As of the Anniversary Update, you can programmatically sideload your extension in Microsoft Edge with WebDriver, enabling automated testing of extensions when Microsoft Edge is launched in WebDriver mode.</span></span> <span data-ttu-id="fcc49-184">Cela vous permet de configurer des tests automatisés pour toutes les extensions qui manipulent du contenu sur une page et de vérifier que le comportement correct est affiché.</span><span class="sxs-lookup"><span data-stu-id="fcc49-184">This will allow you to set up automated tests for any extension that manipulates content on a page and verify that the correct behavior is exhibited.</span></span>

<span data-ttu-id="fcc49-185">Pour charger votre extension pour les tests automatisés, vous devez enregistrer le dossier de votre extension `%LOCALAPPDATA%\Packages\Microsoft.MicrosoftEdge_8wekyb3d8bbwe\LocalState\` .</span><span class="sxs-lookup"><span data-stu-id="fcc49-185">To sideload your extension for automated testing, you'll need to store your extension's folder under `%LOCALAPPDATA%\Packages\Microsoft.MicrosoftEdge_8wekyb3d8bbwe\LocalState\`.</span></span> <span data-ttu-id="fcc49-186">Lorsque votre extension se trouve dans l' `LocalState` annuaire, vous devez créer un [`EdgeOptions`](https://seleniumhq.github.io/selenium/docs/api/dotnet/html/T_OpenQA_Selenium_Edge_EdgeOptions.htm) objet et lui ajouter la `extensionPaths` fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="fcc49-186">Once your extension is in the `LocalState` directory, you'll need to create an [`EdgeOptions`](https://seleniumhq.github.io/selenium/docs/api/dotnet/html/T_OpenQA_Selenium_Edge_EdgeOptions.htm) object, and add the `extensionPaths` capability to it.</span></span> <span data-ttu-id="fcc49-187">La valeur de cette fonctionnalité est un tableau de chemins absolus vers les extensions (dans l' `LocalState` Annuaire) que vous voulez charger sur le site lorsque Microsoft Edge démarre en mode WebDriver.</span><span class="sxs-lookup"><span data-stu-id="fcc49-187">The value of this capability is an array of absolute paths to the extensions (in the `LocalState` directory) you wish to have side loaded when Microsoft Edge starts in WebDriver mode.</span></span>

<span data-ttu-id="fcc49-188">Consultez le [fichier C#](https://github.com/scottlow/Ignite2016/blob/master/Ignite%202016%20WebDriver%20Demo/IgniteWebDriverDemo/Program.cs) suivant pour obtenir un exemple complet d’extensions sur le chargement latéral dans Microsoft Edge avec WebDriver.</span><span class="sxs-lookup"><span data-stu-id="fcc49-188">Check out the following [C# file](https://github.com/scottlow/Ignite2016/blob/master/Ignite%202016%20WebDriver%20Demo/IgniteWebDriverDemo/Program.cs) for a complete sample on side loading extensions in Microsoft Edge with WebDriver.</span></span>
