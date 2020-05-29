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
# <span data-ttu-id="49893-104">extension de code webhint VS</span><span class="sxs-lookup"><span data-stu-id="49893-104">webhint VS Code extension</span></span>

<span data-ttu-id="49893-105">Utilisez [webhint](https://webhint.io), un outil de débordement personnalisable pour améliorer l’accessibilité, les performances, la compatibilité entre les navigateurs, la compatibilité de Project Web App et la sécurité de votre site.</span><span class="sxs-lookup"><span data-stu-id="49893-105">Use [webhint](https://webhint.io), a customizable linting tool, to improve the accessibility, performance, cross-browser compatibility, PWA compatibility, and security of your site.</span></span> <span data-ttu-id="49893-106">Il recherche les meilleures pratiques et les erreurs courantes dans votre code.</span><span class="sxs-lookup"><span data-stu-id="49893-106">It checks your code for best practices and common errors.</span></span> <span data-ttu-id="49893-107">Ce projet open-source développé au départ par l’équipe Microsoft Edge, fait désormais partie de [OpenJS Foundation](https://openjsf.org/).</span><span class="sxs-lookup"><span data-stu-id="49893-107">This open-source project, initially developed by the Microsoft Edge team, is now part of the [OpenJS Foundation](https://openjsf.org/).</span></span> <span data-ttu-id="49893-108">L’équipe Microsoft Edge cesse de contribuer à la communauté et aux développeurs Web de la communauté.</span><span class="sxs-lookup"><span data-stu-id="49893-108">The Microsoft Edge team continues to contribute to webhint alongside web developers in the community.</span></span>

![Capture d’écran de l’extension de code webhint VS](./media/webhint-extension.png)

<span data-ttu-id="49893-110">Identifiez et corrigez les problèmes de votre code HTML, de CSS, de JavaScript, de la machine à écrire et bien plus encore en ajoutant l' [extension webhint pour le code vs](https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint).</span><span class="sxs-lookup"><span data-stu-id="49893-110">Identify and fix problems in your HTML, CSS, JavaScript, TypeScript, and more by adding the [webhint extension for VS Code](https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint).</span></span> <span data-ttu-id="49893-111">Les indications apparaissent sous forme de soulignements inline et sont synthétisées dans le volet problèmes.</span><span class="sxs-lookup"><span data-stu-id="49893-111">Hints appear as inline underlines and are summarized in the Problems pane.</span></span>

## <span data-ttu-id="49893-112">Configuration</span><span class="sxs-lookup"><span data-stu-id="49893-112">Configuration</span></span>

<span data-ttu-id="49893-113">Cette extension utilise un fichier JSON de [configuration par défaut](https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json) qui active les indicateurs et les analyseurs pour les fichiers HTML, CSS, de création de modèles (jsx/TSX, angulaire, etc.), JavaScript/dactylographié, etc.</span><span class="sxs-lookup"><span data-stu-id="49893-113">This extension uses a [default configuration](https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json) json file that activates hints and parsers for HTML, CSS, templating systems (JSX/TSX, Angular, and so on), JavaScript/TypeScript, and more.</span></span>

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

<span data-ttu-id="49893-114">Si vous souhaitez contrôler davantage les indicateurs et les analyseurs qui sont activés, créez un `.hintrc` fichier local pour configurer webhint.</span><span class="sxs-lookup"><span data-stu-id="49893-114">If you want more control over the hints and parsers that get activated, create a local `.hintrc` file to configure webhint.</span></span> <span data-ttu-id="49893-115">Pour obtenir de l’aide sur la sortie d’indications spécifiques, consultez le [Guide d’utilisation de webhint](https://webhint.io/docs/user-guide/configuring-webhint/summary/).</span><span class="sxs-lookup"><span data-stu-id="49893-115">For help with output from specific hints, see the [webhint user guide](https://webhint.io/docs/user-guide/configuring-webhint/summary/).</span></span>

## <span data-ttu-id="49893-116">Commentaires</span><span class="sxs-lookup"><span data-stu-id="49893-116">Feedback</span></span>

<span data-ttu-id="49893-117">Envoyez-nous vos commentaires en [archivant un problème](https://github.com/webhintio/hint/issues/new) sur le [webhint GitHub référentiel Samples](https://github.com/webhintio/hint).</span><span class="sxs-lookup"><span data-stu-id="49893-117">Send us your feedback by [filing an issue](https://github.com/webhintio/hint/issues/new) on the [webhint GitHub repo](https://github.com/webhintio/hint).</span></span> 

<span data-ttu-id="49893-118">Pour contribuer à l’extension, consultez le [Guide de cotisations webhint vs code](https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md).</span><span class="sxs-lookup"><span data-stu-id="49893-118">To contribute to the extension, please read the [webhint VS Code extension contribution guide](https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md).</span></span>

## <span data-ttu-id="49893-119">Voir également</span><span class="sxs-lookup"><span data-stu-id="49893-119">See also</span></span>
  - [<span data-ttu-id="49893-120">Accessibilité</span><span class="sxs-lookup"><span data-stu-id="49893-120">Accessibility</span></span>](/microsoft-edge/accessibility)
  - [<span data-ttu-id="49893-121">VisualStudioCode</span><span class="sxs-lookup"><span data-stu-id="49893-121">Visual Studio Code</span></span>](/microsoft-edge/visual-studio-code/)
