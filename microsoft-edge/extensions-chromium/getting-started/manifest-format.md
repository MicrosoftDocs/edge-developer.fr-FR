---
description: Découvrez le format du fichier manifeste dans un package d’extension.
title: Format de fichier manifeste
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, développement web, html, css, javascript, développeur, extensions, mv2, mv3, manifeste
ms.openlocfilehash: ac2358f8927a762dcef98f9e10cc9f343d8a93f1
ms.sourcegitcommit: afeeeea9fccc3c4c096d7d44c401f4fe87ea2cd7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2021
ms.locfileid: "11599429"
---
# <a name="manifest-file-format-for-extensions"></a><span data-ttu-id="17e58-104">Format de fichier manifeste pour les extensions</span><span class="sxs-lookup"><span data-stu-id="17e58-104">Manifest file format for extensions</span></span>

<span data-ttu-id="17e58-105">Chaque extension de Microsoft Edge (Chromium) possède un fichier manifeste au format JSON, nommé `manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="17e58-105">Every extension for Microsoft Edge (Chromium) has a JSON-formatted manifest file, named `manifest.json`.</span></span>  <span data-ttu-id="17e58-106">Le fichier manifeste est le plan de votre extension.</span><span class="sxs-lookup"><span data-stu-id="17e58-106">The manifest file is the blueprint of your extension.</span></span>  <span data-ttu-id="17e58-107">Le fichier manifeste inclut des informations telles que :</span><span class="sxs-lookup"><span data-stu-id="17e58-107">The manifest file includes information such as:</span></span>

*  <span data-ttu-id="17e58-108">Numéro de version de l’extension.</span><span class="sxs-lookup"><span data-stu-id="17e58-108">The version number of the extension.</span></span>
*  <span data-ttu-id="17e58-109">Titre de l’extension.</span><span class="sxs-lookup"><span data-stu-id="17e58-109">The title of the extension.</span></span>
*  <span data-ttu-id="17e58-110">Autorisations nécessaires à l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="17e58-110">The permissions that are needed for the extension to run.</span></span>

<span data-ttu-id="17e58-111">Le format des extensions est le `manifest.json` passage du manifeste V2 au manifeste V3.</span><span class="sxs-lookup"><span data-stu-id="17e58-111">The format for `manifest.json` for extensions is moving from Manifest V2 to Manifest V3.</span></span>  <span data-ttu-id="17e58-112">Les deux formats sont affichés ici.</span><span class="sxs-lookup"><span data-stu-id="17e58-112">Both formats are shown here.</span></span>  <span data-ttu-id="17e58-113">Pour migrer une extension Manifeste V2 vers le manifeste V3, accédez à Préparer la mise à jour de vos extensions du [manifeste v2 vers la version v3.][MigrateToMV3]</span><span class="sxs-lookup"><span data-stu-id="17e58-113">To migrate a Manifest V2 extension to Manifest V3, navigate to [Prepare to update your extensions from Manifest v2 to v3][MigrateToMV3].</span></span>


## <a name="format-of-manifestjson-for-extensions-using-manifest-v3"></a><span data-ttu-id="17e58-114">Format d'manifest\.jspour les extensions à l’aide du manifeste V3</span><span class="sxs-lookup"><span data-stu-id="17e58-114">Format of manifest\.json for extensions using Manifest V3</span></span>

<span data-ttu-id="17e58-115">Le code suivant présente les champs pris en charge pour `manifest.json` les extensions, pour un package manifeste V3.</span><span class="sxs-lookup"><span data-stu-id="17e58-115">The following code shows the fields that are supported in `manifest.json` for extensions, for a Manifest V3 package.</span></span>

<span data-ttu-id="17e58-116">Pour obtenir des informations de référence sur chaque champ, accédez au format de fichier manifeste [(V3),][ChromeDeveloperDocsExtensionsMv3Manifest] puis sélectionnez les liens sur les champs.</span><span class="sxs-lookup"><span data-stu-id="17e58-116">For reference information about each field, navigate to [Manifest file format (V3)][ChromeDeveloperDocsExtensionsMv3Manifest] and then select the links on the fields.</span></span>

```json
{
  // Required
  "manifest_version": 3,
  "name": "My V3 Extension",
  "version": "versionString",

  // Recommended
  "action": {...},
  "default_locale": "en",
  "description": "A plain-text description",
  "icons": {...},

  // Optional
  "action": ...,
  "author": ...,
  "automation": ...,
  "background": {
    // If `background` is included, `service_ worker` is required
    "service_worker": ...
  },
  "chrome_settings_overrides": {...},
  "chrome_url_overrides": {...},
  "commands": {...},
  "content_capabilities": ...,
  "content_scripts": [{...}],
  "content_security_policy": "policyString",
  "converted_from_user_script": ...,
  "current_locale": ...,
  "declarative_net_request": ...,
  "devtools_page": "devtools.html",
  "differential_fingerprint": ...,
  "event_rules": [{...}],
  "externally_connectable": {
    "matches": ["*://*.contoso.com/*"]
  },
  "file_browser_handlers": [...],
  "file_system_provider_capabilities": {
    "configurable": true,
    "multiple_mounts": true,
    "source": "network"
  },
  "homepage_url": "http://path/to/homepage",
  "host_permissions": [...],
  "import": [{"id": "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa"}],
  "incognito": "spanning, split, or not_allowed",
  "input_components": ...,
  "key": "publicKey",
  "minimum_chrome_version": "versionString",
  "nacl_modules": [...],
  "natively_connectable": ...,
  "oauth2": ...,
  "offline_enabled": true,
  "omnibox": {
    "keyword": "aString"
  },
  "optional_permissions": ["tabs"],
  "options_page": "options.html",
  "options_ui": {
    "chrome_style": true,
    "page": "options.html"
  },
  "permissions": ["tabs"],
  "platforms": ...,
  "replacement_web_app": ...,
  "requirements": {...},
  "sandbox": [...],
  "short_name": "Short Name",
  "storage": {
    "managed_schema": "schema.json"
  },
  "system_indicator": ...,
  "tts_engine": {...},
  "update_url": "http://path/to/updateInfo.xml",
  "version_name": "aString",
  "web_accessible_resources": [...]
}
```

## <a name="format-of-manifestjson-for-extensions-using-manifest-v2"></a><span data-ttu-id="17e58-117">Format d'manifest\.jspour les extensions à l’aide du manifeste V2</span><span class="sxs-lookup"><span data-stu-id="17e58-117">Format of manifest\.json for extensions using Manifest V2</span></span>

<span data-ttu-id="17e58-118">Le code suivant présente les champs pris en charge pour `manifest.json` les extensions, pour un package manifeste V2.</span><span class="sxs-lookup"><span data-stu-id="17e58-118">The following code shows the fields that are supported in `manifest.json` for extensions, for a Manifest V2 package.</span></span>

<span data-ttu-id="17e58-119">Pour obtenir des informations de référence sur chaque champ, accédez au format de fichier manifeste [(V2),][ChromeDeveloperDocsExtensionsMv2Manifest] puis sélectionnez les liens sur les champs.</span><span class="sxs-lookup"><span data-stu-id="17e58-119">For reference information about each field, navigate to [Manifest file format (V2)][ChromeDeveloperDocsExtensionsMv2Manifest] and then select the links on the fields.</span></span>

```json
{
  // Required
  "manifest_version": 2,
  "name": "My V2 Extension",
  "version": "versionString",

  // Recommended
  "default_locale": "en",
  "description": "A plain-text description",
  "icons": {...},

  // Pick one or none
  "browser_action": {...},
  "page_action": {...},

  // Optional
  "action": ...,
  "author": ...,
  "automation": ...,
  "background": {
    // If `background` is included, `persistent` is recommended
    "persistent": false,
    // If `background` is included, `service_worker` is optional
    "service_worker": ...
  },
  "chrome_settings_overrides": {...},
  "chrome_url_overrides": {...},
  "commands": {...},
  "content_capabilities": ...,
  "content_scripts": [{...}],
  "content_security_policy": "policyString",
  "converted_from_user_script": ...,
  "current_locale": ...,
  "declarative_net_request": ...,
  "devtools_page": "devtools.html",
  "differential_fingerprint": ...,
  "event_rules": [{...}],
  "externally_connectable": {
    "matches": ["*://*.contoso.com/*"]
  },
  "file_browser_handlers": [...],
  "file_system_provider_capabilities": {
    "configurable": true,
    "multiple_mounts": true,
    "source": "network"
  },
  "homepage_url": "http://path/to/homepage",
  "host_permissions": ...,
  "import": [{"id": "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa"}],
  "incognito": "spanning, split, or not_allowed",
  "input_components": ...,
  "key": "publicKey",
  "minimum_chrome_version": "versionString",
  "nacl_modules": [...],
  "natively_connectable": ...,
  "oauth2": ...,
  "offline_enabled": true,
  "omnibox": {
    "keyword": "aString"
  },
  "optional_permissions": ["tabs"],
  "options_page": "options.html",
  "options_ui": {
    "chrome_style": true,
    "page": "options.html"
  },
  "permissions": ["tabs"],
  "platforms": ...,
  "replacement_web_app": ...,
  "requirements": {...},
  "sandbox": [...],
  "short_name": "Short Name",
  "storage": {
    "managed_schema": "schema.json"
  },
  "system_indicator": ...,
  "tts_engine": {...},
  "update_url": "http://path/to/updateInfo.xml",
  "version_name": ...,
  "web_accessible_resources": [...]
}
```

> [!NOTE]
> <span data-ttu-id="17e58-120">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="17e58-120">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="17e58-121">La page d’origine se trouve [ici.](https://developer.chrome.com/docs/extensions/mv3/manifest/)</span><span class="sxs-lookup"><span data-stu-id="17e58-121">The original page is found [here](https://developer.chrome.com/docs/extensions/mv3/manifest/).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="17e58-123">Ce travail est sous [licence internationale Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="17e58-123">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies


<!-- links -->
[MigrateToMV3]: ../developer-guide/migrate-your-extension-from-manifest-v2-to-v3.md "Préparez la mise à jour de vos extensions du manifeste v2 vers la version v3 | Documents Microsoft"

[ChromeDeveloperDocsExtensionsMv3Manifest]: https://developer.chrome.com/docs/extensions/mv3/manifest "Format de fichier manifeste (V3) | Développeurs Chrome"
[ChromeDeveloperDocsExtensionsMv2Manifest]: https://developer.chrome.com/docs/extensions/mv2/manifest "Format de fichier manifeste (V2) | Développeurs Chrome"
