---
description: Utilisation de webhint dans le code Visual Studio
title: extension de code webhint VS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, code vs, code Visual Studio, webhint
ms.openlocfilehash: ec218fab8cbfb8181a0416c8e0eadc0e00412529
ms.sourcegitcommit: c1b5fdd48d39d874a76c9b8f68309eb1b507fd0b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2020
ms.locfileid: "10695858"
---
# Extension de code webhint vs  

Utilisez [webhint][WebhintMain], un outil de débordement personnalisable pour améliorer l’accessibilité, les performances, la compatibilité entre les navigateurs, la compatibilité de Project Web App et la sécurité de votre site.  Il recherche les meilleures pratiques et les erreurs courantes dans votre code. Ce projet open-source développé au départ par l’équipe Microsoft Edge, fait désormais partie de [OpenJS Foundation][OpenjsFoundation].  L’équipe Microsoft Edge cesse de contribuer à la communauté et aux développeurs Web de la communauté.  

:::image type="complex" source="./media/webhint-extension.png" alt-text="Capture d’écran de l’extension de code webhint VS":::
   Capture d’écran de l’extension de code webhint VS  
:::image-end:::

<!--![Screenshot of webhint VS Code extension][ImageWebhintExtension]  -->  

Identifiez et corrigez les problèmes de votre code HTML, de CSS, de JavaScript, de la machine à écrire et bien plus encore en ajoutant l' [extension webhint pour le code vs][VisualstudioMarketplaceWebhint].  Les indications apparaissent sous forme de soulignements inline et sont synthétisées dans le volet **problèmes** .  

## Configuration  

Cette extension utilise un fichier JSON de [configuration par défaut][GithubWebhintioIndexjson] qui active les indicateurs et les analyseurs pour les fichiers HTML, CSS, de création de modèles \ (jsx/TSX, angulaire, etc.), JavaScript/dactylographié, etc.  

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

Si vous souhaitez contrôler davantage les indicateurs et les analyseurs qui sont activés, créez un `.hintrc` fichier local pour configurer webhint.  Pour obtenir de l’aide sur la sortie d’indications spécifiques, consultez le [Guide d’utilisation de webhint][WebhintDocsUserguideConfiguringSummary].  

## Contacter l’équipe webhint  

Envoyez vos commentaires en [archivant un problème][GithubWebhintioIssuesNew] dans [webhint GitHub référentiel Samples][GithubWebhintio].  

Pour contribuer à l’extension, voir le [Guide de contribution par extension de code webhint vs][GithubWebhintioExtensionVscodeContributing].  

## Voir également  

*   [Accessibilité][AccessibilityIndex]  
*   [VisualStudioCode][VisualstudiocodeIndex]  

<!-- image links -->  

<!--[ImageWebhintExtension]: ./media/webhint-extension.png "Screenshot of webhint VS Code extension"  -->  

<!--links -->  

[AccessibilityIndex]: /microsoft-edge/accessibility "Accessibilité | Documents Microsoft"  

[VisualstudiocodeIndex]: /microsoft-edge/visual-studio-code/index "Code Visual Studio | Documents Microsoft"  

[GithubWebhintio]: https://github.com/webhintio/hint "webhint | GitHub"  
[GithubWebhintioExtensionVscodeContributing]: https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md "Contributeurs: webhint | GitHub"  
[GithubWebhintioIndexjson]: https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json "index. JSON-webhintio/Hint | GitHub"
[GithubWebhintioIssuesNew]: https://github.com/webhintio/hint/issues/new "Nouveaux problèmes-webhintio/Hint | GitHub"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  

[WebhintDocsUserguideConfiguringSummary]: https://webhint.io/docs/user-guide/configuring-webhint/summary "Configuration de webhint | Documentation webhint"  
[WebhintMain]:  https://webhint.io "Astuce"  
