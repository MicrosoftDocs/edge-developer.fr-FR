---
description: Comment utiliser lahint web dans Visual Studio Code
title: extension de code Visual Studio webhint
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, développement web, vs code, visual studio code, webhint
ms.openlocfilehash: 3dfd900bf818d02dbc8123c00e7928e56d9b6ade
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399273"
---
# <a name="webhint-vs-code-extension"></a>Webhint Vs Code Extension  

Utilisez [webhint,][WebhintMain]un outil de linting personnalisable, pour améliorer l’accessibilité, les performances, la compatibilité entre navigateurs, la compatibilité PWA et la sécurité de votre site.  Il vérifie les meilleures pratiques et les erreurs courantes dans votre code. Ce projet open source, initialement développé par l’équipe Microsoft Edge, fait désormais partie [d’OpenJS Foundation.][OpenjsFoundation]  L’équipe Microsoft Edge continue de contribuer à lahint web avec les développeurs web de la communauté.  

:::image type="complex" source="./media/webhint-extension.png" alt-text="Capture d’écran de l’extension Visual Studio code web":::
   Capture d’écran de l’extension Visual Studio code web  
:::image-end:::

<!--![Screenshot of webhint Visual Studio Code extension][ImageWebhintExtension]  -->  

Identifiez et corrigez les problèmes dans votre code HTML, CSS, JavaScript, TypeScript et bien plus encore en ajoutant [l’extension webhint pour Visual Studio Code][VisualstudioMarketplaceWebhint].  Les conseils apparaissent comme des soulignements inline et sont résumés **dans** le volet Problèmes.  

## <a name="configuration"></a>Configuration  

Cette extension utilise un fichier json de [configuration][GithubWebhintioIndexjson] par défaut qui active des conseils et des parseurs pour html, CSS, systèmes de modèles \(JSX/TSX, Angular, etc.), JavaScript/TypeScript, etc.  

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

Si vous souhaitez contrôler davantage les conseils et les outils d’examen activés, créez un fichier local pour configurer `.hintrc` lahint web.  Pour obtenir de l’aide sur la sortie de conseils spécifiques, accédez au [guide de l’utilisateur de lahint][WebhintDocsUserguideConfiguringSummary]web.  

## <a name="getting-in-touch-with-the-webhint-team"></a>Entrer en contact avec l’équipe webhint  

Envoyez vos commentaires en [classant un problème][GithubWebhintioIssuesNew] dans le référentiel [GitHub webhint.][GithubWebhintio]  

Pour contribuer à l’extension, accédez à la Visual Studio [guide de contribution à l’extension de code.][GithubWebhintioExtensionVscodeContributing]  

## <a name="see-also"></a>Voir également  

*   [Accessibilité][AccessibilityIndex]  
*   [VisualStudioCode][VisualstudiocodeIndex]  

<!-- image links -->  

<!--[ImageWebhintExtension]: ./media/webhint-extension.png "Screenshot of webhint Visual Studio Code extension"  -->  

<!--links -->  

[AccessibilityIndex]: /microsoft-edge/accessibility "Accessibilité | Documents Microsoft"  

[VisualstudiocodeIndex]: /microsoft-edge/visual-studio-code/index "Visual Studio code | Documents Microsoft"  

[GithubWebhintio]: https://github.com/webhintio/hint "webhint | GitHub"  
[GithubWebhintioExtensionVscodeContributing]: https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md "Contribution - webhint | GitHub"  
[GithubWebhintioIndexjson]: https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json "index.js- webhintio/hint | GitHub"
[GithubWebhintioIssuesNew]: https://github.com/webhintio/hint/issues/new "New Issues - webhintio/hint | GitHub"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  

[WebhintDocsUserguideConfiguringSummary]: https://webhint.io/docs/user-guide/configuring-webhint/summary "Configuration des | documentation webhint"  
[WebhintMain]:  https://webhint.io "webhint"  
