---
description: Utilisation de webhint dans le code Visual Studio
title: extension de code webhint VS
author: hxlnt
ms.author: raweil
ms.date: 03/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, code vs, code Visual Studio, webhint
ms.openlocfilehash: d3102bf4d8d4a8bba9225d8d3f68432197f775ac
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566589"
---
# extension de code webhint VS

Utilisez [webhint](https://webhint.io), un outil de débordement personnalisable pour améliorer l’accessibilité, les performances, la compatibilité entre les navigateurs, la compatibilité de Project Web App et la sécurité de votre site. Il recherche les meilleures pratiques et les erreurs courantes dans votre code. Ce projet open-source développé au départ par l’équipe Microsoft Edge, fait désormais partie de [OpenJS Foundation](https://openjsf.org/). L’équipe Microsoft Edge cesse de contribuer à la communauté et aux développeurs Web de la communauté.

![Capture d’écran de l’extension de code webhint VS](./media/webhint-extension.png)

Identifiez et corrigez les problèmes de votre code HTML, de CSS, de JavaScript, de la machine à écrire et bien plus encore en ajoutant l' [extension webhint pour le code vs](https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint). Les indications apparaissent sous forme de soulignements inline et sont synthétisées dans le volet problèmes.

## Configuration

Cette extension utilise un fichier JSON de [configuration par défaut](https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json) qui active les indicateurs et les analyseurs pour les fichiers HTML, CSS, de création de modèles (jsx/TSX, angulaire, etc.), JavaScript/dactylographié, etc.

```json
{
    "connector": "local",
    "extends": [
        "accessibility",
        "progressive-web-apps"
    ],
    "formatters": [
        "html",
        "summary"
    ],
    "hints": [
        "apple-touch-icons",
        "button-type",
        "compat-api/css",
        "compat-api/html",
        "create-element-svg",
        "css-prefix-order",
        "disown-opener",
        "highest-available-document-mode",
        "manifest-exists",
        "meta-charset-utf-8",
        "meta-viewport",
        "no-bom",
        "no-protocol-relative-urls",
        "scoped-svg-styles",
        "sri",
        "typescript-config/consistent-casing",
        "typescript-config/import-helpers",
        "typescript-config/is-valid",
        "typescript-config/no-comments",
        "typescript-config/strict",
        "typescript-config/target"
    ],
    "hintsTimeout": 10000,
    "parsers": [
        "babel-config",
        "css",
        "html",
        "javascript",
        "jsx",
        "less",
        "sass",
        "typescript",
        "typescript-config",
        "webpack-config"
    ]
}
```

Si vous souhaitez contrôler davantage les indicateurs et les analyseurs qui sont activés, créez un `.hintrc` fichier local pour configurer webhint. Pour obtenir de l’aide sur la sortie d’indications spécifiques, consultez le [Guide d’utilisation de webhint](https://webhint.io/docs/user-guide/configuring-webhint/summary/).

## Commentaires

Envoyez-nous vos commentaires en [archivant un problème](https://github.com/webhintio/hint/issues/new) sur le [webhint GitHub référentiel Samples](https://github.com/webhintio/hint). 

Pour contribuer à l’extension, consultez le [Guide de cotisations webhint vs code](https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md).

## Voir également
  - [Accessibilité](/microsoft-edge/accessibility)
  - [VisualStudioCode](/microsoft-edge/visual-studio-code/)
