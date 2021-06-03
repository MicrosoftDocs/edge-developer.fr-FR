---
description: Comment utiliser webhint dans Visual Studio Code
title: extension de Visual Studio Code webhint
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
# <a name="webhint-vs-code-extension"></a><span data-ttu-id="ef7d6-104">Webhint Vs Code Extension</span><span class="sxs-lookup"><span data-stu-id="ef7d6-104">Webhint Vs Code Extension</span></span>  

<span data-ttu-id="ef7d6-105">Utilisez [webhint,][WebhintMain]un outil de linting personnalisable, pour améliorer l’accessibilité, les performances, la compatibilité entre navigateurs, la compatibilité PWA et la sécurité de votre site.</span><span class="sxs-lookup"><span data-stu-id="ef7d6-105">Use [webhint][WebhintMain], a customizable linting tool, to improve the accessibility, performance, cross-browser compatibility, PWA compatibility, and security of your site.</span></span>  <span data-ttu-id="ef7d6-106">Il vérifie les meilleures pratiques et les erreurs courantes dans votre code.</span><span class="sxs-lookup"><span data-stu-id="ef7d6-106">It checks your code for best practices and common errors.</span></span> <span data-ttu-id="ef7d6-107">Ce projet open source, initialement développé par l’équipe Microsoft Edge, fait désormais partie [d’OpenJS Foundation.][OpenjsFoundation]</span><span class="sxs-lookup"><span data-stu-id="ef7d6-107">This open-source project, initially developed by the Microsoft Edge team, is now part of the [OpenJS Foundation][OpenjsFoundation].</span></span>  <span data-ttu-id="ef7d6-108">L Microsoft Edge de recherche continue de contribuer à lahint web avec les développeurs web de la communauté.</span><span class="sxs-lookup"><span data-stu-id="ef7d6-108">The Microsoft Edge team continues to contribute to webhint alongside web developers in the community.</span></span>  

:::image type="complex" source="./media/webhint-extension.png" alt-text="Capture d’écran de l’extension Visual Studio Code webhint":::
   <span data-ttu-id="ef7d6-110">Capture d’écran de l’extension Visual Studio Code webhint</span><span class="sxs-lookup"><span data-stu-id="ef7d6-110">Screenshot of webhint Visual Studio Code extension</span></span>  
:::image-end:::

<!--![Screenshot of webhint Visual Studio Code extension][ImageWebhintExtension]  -->  

<span data-ttu-id="ef7d6-111">Identifiez et corrigez les problèmes dans votre code HTML, CSS, JavaScript, TypeScript et bien plus encore en ajoutant [l’extension webhint pour Visual Studio Code][VisualstudioMarketplaceWebhint].</span><span class="sxs-lookup"><span data-stu-id="ef7d6-111">Identify and fix problems in your HTML, CSS, JavaScript, TypeScript, and more by adding the [webhint extension for Visual Studio Code][VisualstudioMarketplaceWebhint].</span></span>  <span data-ttu-id="ef7d6-112">Les conseils apparaissent comme des soulignements inline et sont résumés **dans** le volet Problèmes.</span><span class="sxs-lookup"><span data-stu-id="ef7d6-112">Hints appear as inline underlines and are summarized in the **Problems** pane.</span></span>  

## <a name="configuration"></a><span data-ttu-id="ef7d6-113">Configuration</span><span class="sxs-lookup"><span data-stu-id="ef7d6-113">Configuration</span></span>  

<span data-ttu-id="ef7d6-114">Cette extension utilise un fichier json de [configuration][GithubWebhintioIndexjson] par défaut qui active des conseils et des parseurs pour html, CSS, systèmes de modèles \(JSX/TSX, Angular, etc.),JavaScript/TypeScript, etc.</span><span class="sxs-lookup"><span data-stu-id="ef7d6-114">This extension uses a [default configuration][GithubWebhintioIndexjson] json file that activates hints and parsers for HTML, CSS, templating systems \(JSX/TSX, Angular, and so on\), JavaScript/TypeScript, and more.</span></span>  

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

<span data-ttu-id="ef7d6-115">Si vous souhaitez contrôler davantage les conseils et les outils d’examen activés, créez un fichier local pour configurer `.hintrc` lahint web.</span><span class="sxs-lookup"><span data-stu-id="ef7d6-115">If you want more control over the hints and parsers that get activated, create a local `.hintrc` file to configure webhint.</span></span>  <span data-ttu-id="ef7d6-116">Pour obtenir de l’aide sur la sortie de conseils spécifiques, accédez au [guide de l’utilisateur webhint.][WebhintDocsUserguideConfiguringSummary]</span><span class="sxs-lookup"><span data-stu-id="ef7d6-116">For help with output from specific hints, navigate to [webhint user guide][WebhintDocsUserguideConfiguringSummary].</span></span>  

## <a name="getting-in-touch-with-the-webhint-team"></a><span data-ttu-id="ef7d6-117">Mise en contact avec l’équipe webhint</span><span class="sxs-lookup"><span data-stu-id="ef7d6-117">Getting in touch with the webhint team</span></span>  

<span data-ttu-id="ef7d6-118">Envoyez vos commentaires en [classant un problème dans][GithubWebhintioIssuesNew] la GitHub [de dépôt.][GithubWebhintio]</span><span class="sxs-lookup"><span data-stu-id="ef7d6-118">Send your feedback by [filing an issue][GithubWebhintioIssuesNew] in [webhint GitHub repo][GithubWebhintio].</span></span>  

<span data-ttu-id="ef7d6-119">Pour contribuer à l’extension, accédez à la Visual Studio Code [guide de contribution à l’extension.][GithubWebhintioExtensionVscodeContributing]</span><span class="sxs-lookup"><span data-stu-id="ef7d6-119">To contribute to the extension, navigate to [webhint Visual Studio Code extension contribution guide][GithubWebhintioExtensionVscodeContributing].</span></span>  

## <a name="see-also"></a><span data-ttu-id="ef7d6-120">Articles associés</span><span class="sxs-lookup"><span data-stu-id="ef7d6-120">See also</span></span>  

*   [<span data-ttu-id="ef7d6-121">Accessibilité</span><span class="sxs-lookup"><span data-stu-id="ef7d6-121">Accessibility</span></span>][AccessibilityIndex]  
*   [<span data-ttu-id="ef7d6-122">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="ef7d6-122">Visual Studio Code</span></span>][VisualstudiocodeIndex]  

<!-- image links -->  

<!--[ImageWebhintExtension]: ./media/webhint-extension.png "Screenshot of webhint Visual Studio Code extension"  -->  

<!--links -->  

[AccessibilityIndex]: /microsoft-edge/accessibility "Accessibilité | Documents Microsoft"  

[VisualstudiocodeIndex]: /microsoft-edge/visual-studio-code/index "Visual Studio Code | Documents Microsoft"  

[GithubWebhintio]: https://github.com/webhintio/hint "webhint | GitHub"  
[GithubWebhintioExtensionVscodeContributing]: https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md "Contribution - webhint | GitHub"  
[GithubWebhintioIndexjson]: https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json "index.js- webhintio/hint | GitHub"
[GithubWebhintioIssuesNew]: https://github.com/webhintio/hint/issues/new "New Issues - webhintio/hint | GitHub"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  

[WebhintDocsUserguideConfiguringSummary]: https://webhint.io/docs/user-guide/configuring-webhint/summary "Configuration des | documentation webhint"  
[WebhintMain]:  https://webhint.io "webhint"  
