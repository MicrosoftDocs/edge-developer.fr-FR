---
ms.assetid: 1319a070-c6e3-4592-9f4b-40ce1575851f
description: Découvrez comment porter votre extension chrome vers Microsoft Edge à l’aide du kit de connaissances Microsoft Edge extension.
title: Portage d’extensions de chrome
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.custom: seodec18
ms.openlocfilehash: 38bf1324c2e7e6f7754912177ce0e53d6c15a276
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565304"
---
# <span data-ttu-id="91a71-104">Portage d’une extension de chrome vers Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="91a71-104">Porting an extension from Chrome to Microsoft Edge</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="91a71-105">Le portage d’une extension de chrome vers Microsoft Edge est facilité grâce à l’aide du [Kit de connaissances Microsoft Edge extension](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).</span><span class="sxs-lookup"><span data-stu-id="91a71-105">Porting an extension from Chrome to Microsoft Edge is made easy with the help of the [Microsoft Edge Extension Toolkit](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).</span></span> <span data-ttu-id="91a71-106">Cet outil de développement convertit une extension chrome décompressée en une extension Microsoft Edge décompressée par les API de pontage et signale les erreurs présentes dans votre `manifest.json` fichier.</span><span class="sxs-lookup"><span data-stu-id="91a71-106">This developer tool converts an unpacked Chrome extension to an unpacked Microsoft Edge extension by bridging APIs and surfacing any errors in your `manifest.json` file.</span></span>


### <span data-ttu-id="91a71-107">Ponts d’API</span><span class="sxs-lookup"><span data-stu-id="91a71-107">API bridges</span></span>
<span data-ttu-id="91a71-108">Pour permettre le portage sans interruption d’API de chrome vers des API Microsoft Edge prises en charge, deux scripts sont ajoutés au dossier de votre extension.</span><span class="sxs-lookup"><span data-stu-id="91a71-108">In order to allow for seamless porting of Chrome APIs to supported Microsoft Edge APIs, two scripts are added to your extension's folder.</span></span> <span data-ttu-id="91a71-109">Ces scripts permettent de mettre en avant les API de pont (sous-dépôt le cas échéant), ce qui signifie que vous n’avez pas à vous soucier de la modification du code de votre script en arrière-plan ou des scripts de contenu.</span><span class="sxs-lookup"><span data-stu-id="91a71-109">These scripts bridge APIs (polyfiling where necessary), meaning you won't have to worry about changing any Chrome specific code in your background script or content scripts.</span></span>

<span data-ttu-id="91a71-110">Après la conversion, celles-ci sont incluses dans le fichier manifeste de votre extension avec la `"-ms-preload"` clé:</span><span class="sxs-lookup"><span data-stu-id="91a71-110">After conversion, you will see them included in the manifest file of your extension with the `"-ms-preload"` key:</span></span>

```json
"-ms-preload": {
  "backgroundScript": "backgroundScriptsAPIBridge.js",
  "contentScript": "contentScriptsAPIBridge.js"
}
```

## <span data-ttu-id="91a71-111">Utilisation du kit de connaissances Microsoft Edge extension</span><span class="sxs-lookup"><span data-stu-id="91a71-111">Using the Microsoft Edge Extension Toolkit</span></span>

<span data-ttu-id="91a71-112">Les instructions suivantes décrivent en détail la façon de convertir votre extension chrome pour qu’elle s’exécute sur Microsoft Edge dans l’édition anniversaire Windows 10:</span><span class="sxs-lookup"><span data-stu-id="91a71-112">The following instructions detail how to convert your Chrome extension to run on Microsoft Edge in the Windows 10 Anniversary Update edition:</span></span>

1. <span data-ttu-id="91a71-113">Installez le [Kit de connaissances Microsoft Edge extension](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).</span><span class="sxs-lookup"><span data-stu-id="91a71-113">Install the [Microsoft Edge Extension Toolkit](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).</span></span>
2. <span data-ttu-id="91a71-114">Effectuez une copie du dossier de votre extension chrome pour en assurer la protection.</span><span class="sxs-lookup"><span data-stu-id="91a71-114">Make a copy of your Chrome extension's folder for safe keeping.</span></span> <span data-ttu-id="91a71-115">Le processus de conversion remplacera le code.</span><span class="sxs-lookup"><span data-stu-id="91a71-115">The conversion process will overwrite the code.</span></span> 
3. <span data-ttu-id="91a71-116">Exécutez le kit de connaissances Microsoft Edge extension et chargez la copie de votre extension.</span><span class="sxs-lookup"><span data-stu-id="91a71-116">Run the Microsoft Edge Extension Toolkit and load the copy of your extension.</span></span>  
 ![bouton charger l’extension](./../media/save-folder.png)
4. <span data-ttu-id="91a71-118">Corrigez toutes les erreurs signalées dans l’éditeur de texte de l’outil.</span><span class="sxs-lookup"><span data-stu-id="91a71-118">Correct all the errors that are reported within the tool's text editor.</span></span> <span data-ttu-id="91a71-119">Sélectionnez «re-Validate» pour vérifier les erreurs après avoir effectué des corrections.</span><span class="sxs-lookup"><span data-stu-id="91a71-119">Select "Re-validate" to check for errors after making corrections.</span></span>  
 ![Erreurs de recherche de l’extension Toolkit](./../media/extension-toolkit.png)
5. <span data-ttu-id="91a71-121">Sélectionnez «Enregistrer les fichiers».</span><span class="sxs-lookup"><span data-stu-id="91a71-121">Select "Save files".</span></span>

<span data-ttu-id="91a71-122">Vous pouvez maintenant quitter le kit d’outils et charger votre extension dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="91a71-122">You can now exit out of the toolkit and load your extension in Microsoft Edge!</span></span> 

<span data-ttu-id="91a71-123">Vous pouvez rechercher des problèmes de plateforme connus avec le [suivi des problèmes EdgeHTML](http://issues.microsoftedge.com).</span><span class="sxs-lookup"><span data-stu-id="91a71-123">You can search for known platform issues with the [EdgeHTML issue tracker](http://issues.microsoftedge.com).</span></span> <span data-ttu-id="91a71-124">Si vous pensez que vous avez trouvé une nouveauté, [ouvrez un problème](https://developer.microsoft.com/microsoft-edge/platform/issues/new/)!</span><span class="sxs-lookup"><span data-stu-id="91a71-124">If you think you've found something new, [open an issue](https://developer.microsoft.com/microsoft-edge/platform/issues/new/)!</span></span>
