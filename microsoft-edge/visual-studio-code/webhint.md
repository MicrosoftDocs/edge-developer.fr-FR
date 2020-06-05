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
# <span data-ttu-id="24656-104">Extension de code webhint vs</span><span class="sxs-lookup"><span data-stu-id="24656-104">Webhint Vs Code Extension</span></span>  

<span data-ttu-id="24656-105">Utilisez [webhint][WebhintMain], un outil de débordement personnalisable pour améliorer l’accessibilité, les performances, la compatibilité entre les navigateurs, la compatibilité de Project Web App et la sécurité de votre site.</span><span class="sxs-lookup"><span data-stu-id="24656-105">Use [webhint][WebhintMain], a customizable linting tool, to improve the accessibility, performance, cross-browser compatibility, PWA compatibility, and security of your site.</span></span>  <span data-ttu-id="24656-106">Il recherche les meilleures pratiques et les erreurs courantes dans votre code.</span><span class="sxs-lookup"><span data-stu-id="24656-106">It checks your code for best practices and common errors.</span></span> <span data-ttu-id="24656-107">Ce projet open-source développé au départ par l’équipe Microsoft Edge, fait désormais partie de [OpenJS Foundation][OpenjsFoundation].</span><span class="sxs-lookup"><span data-stu-id="24656-107">This open-source project, initially developed by the Microsoft Edge team, is now part of the [OpenJS Foundation][OpenjsFoundation].</span></span>  <span data-ttu-id="24656-108">L’équipe Microsoft Edge cesse de contribuer à la communauté et aux développeurs Web de la communauté.</span><span class="sxs-lookup"><span data-stu-id="24656-108">The Microsoft Edge team continues to contribute to webhint alongside web developers in the community.</span></span>  

:::image type="complex" source="./media/webhint-extension.png" alt-text="Capture d’écran de l’extension de code webhint VS":::
   <span data-ttu-id="24656-110">Capture d’écran de l’extension de code webhint VS</span><span class="sxs-lookup"><span data-stu-id="24656-110">Screenshot of webhint VS Code extension</span></span>  
:::image-end:::

<!--![Screenshot of webhint VS Code extension][ImageWebhintExtension]  -->  

<span data-ttu-id="24656-111">Identifiez et corrigez les problèmes de votre code HTML, de CSS, de JavaScript, de la machine à écrire et bien plus encore en ajoutant l' [extension webhint pour le code vs][VisualstudioMarketplaceWebhint].</span><span class="sxs-lookup"><span data-stu-id="24656-111">Identify and fix problems in your HTML, CSS, JavaScript, TypeScript, and more by adding the [webhint extension for VS Code][VisualstudioMarketplaceWebhint].</span></span>  <span data-ttu-id="24656-112">Les indications apparaissent sous forme de soulignements inline et sont synthétisées dans le volet **problèmes** .</span><span class="sxs-lookup"><span data-stu-id="24656-112">Hints appear as inline underlines and are summarized in the **Problems** pane.</span></span>  

## <span data-ttu-id="24656-113">Configuration</span><span class="sxs-lookup"><span data-stu-id="24656-113">Configuration</span></span>  

<span data-ttu-id="24656-114">Cette extension utilise un fichier JSON de [configuration par défaut][GithubWebhintioIndexjson] qui active les indicateurs et les analyseurs pour les fichiers HTML, CSS, de création de modèles \ (jsx/TSX, angulaire, etc.), JavaScript/dactylographié, etc.</span><span class="sxs-lookup"><span data-stu-id="24656-114">This extension uses a [default configuration][GithubWebhintioIndexjson] json file that activates hints and parsers for HTML, CSS, templating systems \(JSX/TSX, Angular, and so on\), JavaScript/TypeScript, and more.</span></span>  

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

<span data-ttu-id="24656-115">Si vous souhaitez contrôler davantage les indicateurs et les analyseurs qui sont activés, créez un `.hintrc` fichier local pour configurer webhint.</span><span class="sxs-lookup"><span data-stu-id="24656-115">If you want more control over the hints and parsers that get activated, create a local `.hintrc` file to configure webhint.</span></span>  <span data-ttu-id="24656-116">Pour obtenir de l’aide sur la sortie d’indications spécifiques, consultez le [Guide d’utilisation de webhint][WebhintDocsUserguideConfiguringSummary].</span><span class="sxs-lookup"><span data-stu-id="24656-116">For help with output from specific hints, see [webhint user guide][WebhintDocsUserguideConfiguringSummary].</span></span>  

## <span data-ttu-id="24656-117">Contacter l’équipe webhint</span><span class="sxs-lookup"><span data-stu-id="24656-117">Getting in touch with the webhint team</span></span>  

<span data-ttu-id="24656-118">Envoyez vos commentaires en [archivant un problème][GithubWebhintioIssuesNew] dans [webhint GitHub référentiel Samples][GithubWebhintio].</span><span class="sxs-lookup"><span data-stu-id="24656-118">Send your feedback by [filing an issue][GithubWebhintioIssuesNew] in [webhint GitHub repo][GithubWebhintio].</span></span>  

<span data-ttu-id="24656-119">Pour contribuer à l’extension, voir le [Guide de contribution par extension de code webhint vs][GithubWebhintioExtensionVscodeContributing].</span><span class="sxs-lookup"><span data-stu-id="24656-119">To contribute to the extension, see [webhint VS Code extension contribution guide][GithubWebhintioExtensionVscodeContributing].</span></span>  

## <span data-ttu-id="24656-120">Voir également</span><span class="sxs-lookup"><span data-stu-id="24656-120">See also</span></span>  

*   [<span data-ttu-id="24656-121">Accessibilité</span><span class="sxs-lookup"><span data-stu-id="24656-121">Accessibility</span></span>][AccessibilityIndex]  
*   [<span data-ttu-id="24656-122">VisualStudioCode</span><span class="sxs-lookup"><span data-stu-id="24656-122">Visual Studio Code</span></span>][VisualstudiocodeIndex]  

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
