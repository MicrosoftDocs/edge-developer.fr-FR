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
# Portage d’une extension de chrome vers Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Le portage d’une extension de chrome vers Microsoft Edge est facilité grâce à l’aide du [Kit de connaissances Microsoft Edge extension](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb). Cet outil de développement convertit une extension chrome décompressée en une extension Microsoft Edge décompressée par les API de pontage et signale les erreurs présentes dans votre `manifest.json` fichier.


### Ponts d’API
Pour permettre le portage sans interruption d’API de chrome vers des API Microsoft Edge prises en charge, deux scripts sont ajoutés au dossier de votre extension. Ces scripts permettent de mettre en avant les API de pont (sous-dépôt le cas échéant), ce qui signifie que vous n’avez pas à vous soucier de la modification du code de votre script en arrière-plan ou des scripts de contenu.

Après la conversion, celles-ci sont incluses dans le fichier manifeste de votre extension avec la `"-ms-preload"` clé:

```json
"-ms-preload": {
  "backgroundScript": "backgroundScriptsAPIBridge.js",
  "contentScript": "contentScriptsAPIBridge.js"
}
```

## Utilisation du kit de connaissances Microsoft Edge extension

Les instructions suivantes décrivent en détail la façon de convertir votre extension chrome pour qu’elle s’exécute sur Microsoft Edge dans l’édition anniversaire Windows 10:

1. Installez le [Kit de connaissances Microsoft Edge extension](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).
2. Effectuez une copie du dossier de votre extension chrome pour en assurer la protection. Le processus de conversion remplacera le code. 
3. Exécutez le kit de connaissances Microsoft Edge extension et chargez la copie de votre extension.  
 ![bouton charger l’extension](./../media/save-folder.png)
4. Corrigez toutes les erreurs signalées dans l’éditeur de texte de l’outil. Sélectionnez «re-Validate» pour vérifier les erreurs après avoir effectué des corrections.  
 ![Erreurs de recherche de l’extension Toolkit](./../media/extension-toolkit.png)
5. Sélectionnez «Enregistrer les fichiers».

Vous pouvez maintenant quitter le kit d’outils et charger votre extension dans Microsoft Edge. 

Vous pouvez rechercher des problèmes de plateforme connus avec le [suivi des problèmes EdgeHTML](http://issues.microsoftedge.com). Si vous pensez que vous avez trouvé une nouveauté, [ouvrez un problème](https://developer.microsoft.com/microsoft-edge/platform/issues/new/)!
