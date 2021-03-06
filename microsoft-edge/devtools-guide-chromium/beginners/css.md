---
description: Mise en place de CSS
title: 'DevTools pour les débutants : mise en place de CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, développement web, outils f12, devtools
ms.openlocfilehash: 7aa33c339a7d130265660e4a4af6f50dde7e3e90
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398398"
---
<!-- Copyright Katherine Jackson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="devtools-for-beginners-get-started-with-css"></a><span data-ttu-id="ef4e1-104">DevTools pour les débutants : mise en place de CSS</span><span class="sxs-lookup"><span data-stu-id="ef4e1-104">DevTools for beginners: Get started with CSS</span></span>  

<span data-ttu-id="ef4e1-105">Dans ce didacticiel, vous allez apprendre à utiliser CSS pour styler une page web.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-105">In this tutorial, you learn how to use CSS to style a web page.</span></span>  <span data-ttu-id="ef4e1-106">Vous apprendrez également à utiliser Microsoft Edge DevTools pour expérimenter les modifications CSS.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-106">You also learn how to use Microsoft Edge DevTools to experiment with CSS changes.</span></span>  

<span data-ttu-id="ef4e1-107">L’article suivant est le deuxième didacticiel d’une série de didacticiels qui vous apprend les principes de base du développement web et de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-107">The following article is the second tutorial in a series of tutorials that teaches you the basics of web development and Microsoft Edge DevTools.</span></span>  <span data-ttu-id="ef4e1-108">Vous gagnez en expérience pratique en construisant votre propre site web.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-108">You gain hands-on experience by actually building your own website.</span></span>  <span data-ttu-id="ef4e1-109">Vous n’avez pas besoin de terminer le premier didacticiel avant de suivre le second.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-109">You do not have to complete the first tutorial before following the second.</span></span>  <span data-ttu-id="ef4e1-110">[La mise en place de votre code](#set-up-your-code) vous montre comment la configurer.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-110">[Set up your code](#set-up-your-code) shows you how to get set up.</span></span>  

> [!NOTE]
> <span data-ttu-id="ef4e1-111">Ce didacticiel est conçu pour les néophytes et se concentre à la fois sur les principes de base du développement **web** et sur les principes de base de l’utilisation de DevTools pour expérimenter CSS.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-111">This tutorial is designed for absolute beginners and focuses on both the **fundamentals of web development** and the basics of using DevTools to experiment with CSS.</span></span>  <span data-ttu-id="ef4e1-112">Si vous souhaitez un didacticiel qui se concentre uniquement sur DevTools, accédez à Démarrer avec l’affichage et la modification [de CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="ef4e1-112">If you want a tutorial that only focuses on DevTools, navigate to [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

<span data-ttu-id="ef4e1-113">Au début du didacticiel, votre site doit ressembler à la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-113">At the beginning of the tutorial, your site should look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-css-intro1.msft.png" alt-text="Apparence actuelle de votre site" lightbox="../media/beginners-css-intro1.msft.png":::
   <span data-ttu-id="ef4e1-115">Apparence actuelle de votre site</span><span class="sxs-lookup"><span data-stu-id="ef4e1-115">What your site currently looks like</span></span>  
:::image-end:::  

<span data-ttu-id="ef4e1-116">Une fois le didacticiel terminé, votre site doit ressembler à la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-116">After you complete the tutorial, you site should look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-css-intro2.msft.png" alt-text="Apparence de votre site à la fin du didacticiel" lightbox="../media/beginners-css-intro2.msft.png":::
   <span data-ttu-id="ef4e1-118">Apparence de votre site à la fin du didacticiel</span><span class="sxs-lookup"><span data-stu-id="ef4e1-118">What your site should look like at the end of the tutorial</span></span>  
:::image-end:::  

## <a name="goals"></a><span data-ttu-id="ef4e1-119">Objectifs</span><span class="sxs-lookup"><span data-stu-id="ef4e1-119">Goals</span></span>  

<span data-ttu-id="ef4e1-120">Suivez ce didacticiel pour mieux comprendre les concepts et tâches suivants.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-120">Follow this tutorial to better understand the following concepts and tasks.</span></span>  

*   <span data-ttu-id="ef4e1-121">Utilisation de CSS pour le style d’une page web.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-121">How to use CSS to style a web page.</span></span>  
*   <span data-ttu-id="ef4e1-122">Comment utiliser Microsoft Edge DevTools pour expérimenter CSS.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-122">How to use Microsoft Edge DevTools to experiment with CSS.</span></span>  
*   <span data-ttu-id="ef4e1-123">Différence entre les infrastructure CSS et CSS.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-123">The difference between CSS and CSS frameworks.</span></span>  

<span data-ttu-id="ef4e1-124">Vous construisez un site web réel.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-124">You are building a real website.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="ef4e1-125">Prérequis</span><span class="sxs-lookup"><span data-stu-id="ef4e1-125">Prerequisites</span></span>  

<span data-ttu-id="ef4e1-126">Avant d’essayer ce didacticiel, remplissez les conditions préalables suivantes.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-126">Before attempting this tutorial, complete the following prerequisites.</span></span>  

*   <span data-ttu-id="ef4e1-127">[Complétez la][DevtoolsBeginnersHtml] mise en place du code HTML et du DOM ou assurez-vous que vous avez une connaissance du code HTML et du DOM semblable à ce qui est appris dans ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-127">Complete [Get Started with HTML and the DOM][DevtoolsBeginnersHtml] or make sure that you have an understanding of HTML and the DOM similar to what is taught in that tutorial.</span></span>  
*   <span data-ttu-id="ef4e1-128">Téléchargez le navigateur web [Microsoft Edge.][MicrosoftEdgeInsider]</span><span class="sxs-lookup"><span data-stu-id="ef4e1-128">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="ef4e1-129">Le didacticiel suivant utilise un ensemble d’outils de développement web, appelés Microsoft Edge DevTools, qui sont intégrés à Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-129">The following tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <a name="set-up-your-code"></a><span data-ttu-id="ef4e1-130">Configurer votre code</span><span class="sxs-lookup"><span data-stu-id="ef4e1-130">Set up your code</span></span>  

<span data-ttu-id="ef4e1-131">Pour créer votre site, vous devez d’abord effectuer les actions suivantes pour configurer votre code.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-131">To create your site, you must first complete the following actions to set up your code.</span></span>  

> [!NOTE]
> <span data-ttu-id="ef4e1-132">Si vous avez déjà terminé le premier didacticiel de la série, passez à la section suivante.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-132">If you have already completed the first tutorial in the series, skip to the next section.</span></span>  <span data-ttu-id="ef4e1-133">Continuez à utiliser votre code du dernier didacticiel, [Get Started with HTML and the DOM][DevtoolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="ef4e1-133">Continue using your code from the last tutorial, [Get Started with HTML and the DOM][DevtoolsBeginnersHtml].</span></span>  

1.  <span data-ttu-id="ef4e1-134">Ouvrez le [code source.][GlitchCookedAmphibianIndex]</span><span class="sxs-lookup"><span data-stu-id="ef4e1-134">Open the [source code][GlitchCookedAmphibianIndex].</span></span>  <span data-ttu-id="ef4e1-135">L’onglet sur le focus de votre navigateur est référencé en tant **qu’onglet d’édition.**</span><span class="sxs-lookup"><span data-stu-id="ef4e1-135">The in-focus tab of your browser is referenced as the **editing tab**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup1.msft.png" alt-text="Onglet Modification" lightbox="../media/beginners-css-setup1.msft.png":::
       <span data-ttu-id="ef4e1-137">Onglet **Modification**</span><span class="sxs-lookup"><span data-stu-id="ef4e1-137">The **editing** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ef4e1-138">Choisissez **l’ombrabe**.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-138">Choose **cooked-amphibian**.</span></span>  <span data-ttu-id="ef4e1-139">Un menu s’insérait.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-139">A menu pops up.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup2.msft.png" alt-text="Menu Options de Projet" lightbox="../media/beginners-css-setup2.msft.png":::
       <span data-ttu-id="ef4e1-141">Menu Options de projet</span><span class="sxs-lookup"><span data-stu-id="ef4e1-141">The Project Options menu</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="ef4e1-142">Sélectionnez **Projet DeNte**.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-142">Choose **Remix Project**.</span></span>  <span data-ttu-id="ef4e1-143">Glitch crée une copie du projet que vous pouvez modifier.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-143">Glitch creates a copy of the project that you are able to edit.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="ef4e1-144">Glitch génère un nom aléatoire pour le nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-144">Glitch generates a random name for the new project.</span></span>  
    
1.  <span data-ttu-id="ef4e1-145">Choose **Show** and choose **In a New Window**.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-145">Choose **Show** and choose **In a New Window**.</span></span>  <span data-ttu-id="ef4e1-146">Un autre onglet s’ouvre avec une vue en direct de votre site.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-146">Another tab opens with a live view of your site.</span></span>  <span data-ttu-id="ef4e1-147">L’onglet sur le focus de votre navigateur est référencé en tant **qu’onglet en direct.**</span><span class="sxs-lookup"><span data-stu-id="ef4e1-147">The in-focus tab of your browser is referenced as the **live tab**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup3.msft.png" alt-text="Onglet en direct" lightbox="../media/beginners-css-setup3.msft.png":::
       <span data-ttu-id="ef4e1-149">Onglet **en direct**</span><span class="sxs-lookup"><span data-stu-id="ef4e1-149">The **live tab**</span></span>  
    :::image-end:::  

## <a name="understand-css"></a><span data-ttu-id="ef4e1-150">Comprendre les CSS</span><span class="sxs-lookup"><span data-stu-id="ef4e1-150">Understand CSS</span></span>  

<span data-ttu-id="ef4e1-151">**CSS est** un langage d’ordinateur qui détermine la disposition et le style des pages web.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-151">**CSS** is a computer language that determines the layout and styling of web pages.</span></span>  <span data-ttu-id="ef4e1-152">La figure suivante est un paragraphe avec une bordure.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-152">The following figure is a paragraph with a border.</span></span>  

:::image type="complex" source="../media/beginners-css-red_paragraph.msft.png" alt-text="Le texte a été mis en forme avec le style CSS" lightbox="../media/beginners-css-red_paragraph.msft.png":::
   <span data-ttu-id="ef4e1-154">Le texte a été mis en forme avec le style CSS</span><span class="sxs-lookup"><span data-stu-id="ef4e1-154">The text has been styled with CSS</span></span>  
:::image-end:::  

<span data-ttu-id="ef4e1-155">L’extrait de code suivant est le code HTML et CSS utilisé pour créer le paragraphe dans la figure précédente.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-155">The following code snippet is the HTML and CSS code used to create the paragraph in the previous figure.</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` <span data-ttu-id="ef4e1-156">vous semble probablement nouveau.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-156">probably looks new to you.</span></span>  <span data-ttu-id="ef4e1-157">Le reste doit paraître familier.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-157">The rest should look familiar.</span></span>  <span data-ttu-id="ef4e1-158">Si ce n’est pas le cas, terminez la mise en place du code HTML et du [DOM][DevtoolsBeginnersHtml] avant d’essayer les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-158">If not, complete [Get Started with HTML and the DOM][DevtoolsBeginnersHtml] before attempting the following sections.</span></span>  

## <a name="add-inline-styles"></a><span data-ttu-id="ef4e1-159">Ajouter des styles inline</span><span class="sxs-lookup"><span data-stu-id="ef4e1-159">Add inline styles</span></span>  

<span data-ttu-id="ef4e1-160">Effectuer les actions suivantes pour utiliser des **styles inline** pour appliquer des styles à un seul élément.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-160">Complete the following actions to use **inline styles** to apply styles to a single element.</span></span>  

1.  <span data-ttu-id="ef4e1-161">Revenir à l’onglet Édition et ouvrir `index.html` .</span><span class="sxs-lookup"><span data-stu-id="ef4e1-161">Go back to the editing tab and open `index.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-inline1.msft.png" alt-text="index.html" lightbox="../media/beginners-css-inline1.msft.png":::
       <span data-ttu-id="ef4e1-163">Ouvrir `index.html` dans l’onglet Modification</span><span class="sxs-lookup"><span data-stu-id="ef4e1-163">Open `index.html` in the editing tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ef4e1-164">Ajoutez `style="background-color: aliceblue;"` à `<nav>` votre .</span><span class="sxs-lookup"><span data-stu-id="ef4e1-164">Add `style="background-color: aliceblue;"` to your `<nav>`.</span></span>  <span data-ttu-id="ef4e1-165">Dans le bloc de code ci-dessous, la quatrième ligne de code est celle que vous devez modifier.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-165">In the code block below, the fourth line of code is the one you need to change.</span></span>  <span data-ttu-id="ef4e1-166">Le reste est là, vous êtes donc en mesure de vous assurer que vous placez le nouveau code au bon endroit.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-166">The rest is just there, so you are able to ensure that you are putting the new code in the right place.</span></span>  
    
    ```html
    <header>
        <p>Welcome to my site!</p>
    </header>
    <nav style="background-color: aliceblue;">
        <ul>
            <li><a href="/">Home</a></li>
            ...
        ...
    ...
    ```  
    
1.  <span data-ttu-id="ef4e1-167">Pour afficher les modifications, accédez à **l’onglet en direct.**  L’arrière-plan `<nav>` de la section est désormais bleu.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-167">To display the changes, navigate to the **live tab**.  The background of the `<nav>` section is now blue.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-inline2.msft.png" alt-text="La couleur d’arrière-plan derrière les liens Accueil et Contact est désormais bleue" lightbox="../media/beginners-css-inline2.msft.png":::
       <span data-ttu-id="ef4e1-169">La couleur d’arrière-plan derrière **les** liens Accueil **et Contact** est désormais bleue</span><span class="sxs-lookup"><span data-stu-id="ef4e1-169">The background color behind the **Home** and **Contact** links is now blue</span></span>  
    :::image-end:::  
    
## <a name="re-use-styles-on-a-single-page-with-internal-stylesheets"></a><span data-ttu-id="ef4e1-170">Ré-utiliser des styles sur une seule page avec des feuilles de style internes</span><span class="sxs-lookup"><span data-stu-id="ef4e1-170">Re-use styles on a single page with internal stylesheets</span></span>  

<span data-ttu-id="ef4e1-171">Dans un extrait de code précédent, un style inline appliquait un style à une seule `<p>` balise.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-171">In a previous code snippet, an inline style applied a style to a single `<p>` tag.</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

<span data-ttu-id="ef4e1-172">Que se passe-t-il si vous souhaitez que tous les éléments de votre page web soient marqués `<p>` de la même manière ?</span><span class="sxs-lookup"><span data-stu-id="ef4e1-172">What if you wanted all of the `<p>` elements on your webpage to be styled the same way?</span></span>  <span data-ttu-id="ef4e1-173">Vous devez copier et coller le code dans chaque balise `<p>` de votre site.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-173">You have to copy and paste the code into every single `<p>` tag on your site.</span></span>  <span data-ttu-id="ef4e1-174">Cela fait beaucoup de temps et d’efforts.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-174">That is a lot of time and effort.</span></span>  <span data-ttu-id="ef4e1-175">Et, si vous avez besoin d’apporter une modification, vous devez modifier à nouveau chaque balise.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-175">And, if you needed to make an edit, you have to change every tag again.</span></span>  <span data-ttu-id="ef4e1-176">Effectuer les actions suivantes pour utiliser une feuille de **style** interne afin d’écrire votre feuille de style CSS une seule fois afin qu’elle s’applique à plusieurs éléments.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-176">Complete the following actions to use an **Internal stylesheet** to write your CSS once so that it applies to multiple elements.</span></span>  

1.  <span data-ttu-id="ef4e1-177">Dans l’onglet en direct, choisissez **Contact** pour accéder à la page de contact.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-177">In the live tab, choose **Contact** to navigate to the contact page.</span></span>  <span data-ttu-id="ef4e1-178">Notez la police de **Famille** et **Contact**.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-178">Notice the font of **Home** and **Contact**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-internal1.msft.png" alt-text="Page Contact" lightbox="../media/beginners-css-internal1.msft.png":::
       <span data-ttu-id="ef4e1-180">Page Contact</span><span class="sxs-lookup"><span data-stu-id="ef4e1-180">The Contact page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ef4e1-181">Dans **l’onglet Éditeur,** ouvrez `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="ef4e1-181">In the **editor tab**, open `contact.html`.</span></span>  
1.  <span data-ttu-id="ef4e1-182">Ajoutez le code suivant à `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="ef4e1-182">Add the following code to `contact.html`.</span></span>  <span data-ttu-id="ef4e1-183">N’oubliez pas que les lignes commençant par et se terminant par ce que vous `<style>` `</style>` devez ajouter.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-183">Remember, the lines starting with `<style>` and ending with `</style>` are what you need to add.</span></span>  <span data-ttu-id="ef4e1-184">L’autre code est là pour vous aider à savoir où placer le nouveau code.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-184">The other code is just there so you know where to put the new code.</span></span>  
    
    ```html
    ...
        <head>
            ...
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <style>
                li a {
                  font-family: 'Courier New', Courier, Serif;
                }
            </style>
            ...
        </head>
        ...
    ...
    ```  
    
1.  <span data-ttu-id="ef4e1-185">Revenir à **l’onglet en direct.**</span><span class="sxs-lookup"><span data-stu-id="ef4e1-185">Go back to the **live tab**.</span></span>  
1.  <span data-ttu-id="ef4e1-186">Sélectionnez **Contact** pour revenir à la page de contact.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-186">Choose **Contact** to go back to the contact page.</span></span>  <span data-ttu-id="ef4e1-187">La police **d’accueil** **et de contact** a changé.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-187">The font of **Home** and **Contact** has changed.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-internal2.msft.png" alt-text="La police des liens Accueil et Contact a changé" lightbox="../media/beginners-css-internal2.msft.png":::
       <span data-ttu-id="ef4e1-189">La police des **liens** Accueil et **Contact** a changé</span><span class="sxs-lookup"><span data-stu-id="ef4e1-189">The font of the **Home** and **Contact** links has changed</span></span>  
    :::image-end:::  
    
### <a name="understand-internal-stylesheets"></a><span data-ttu-id="ef4e1-190">Comprendre les feuilles de style internes</span><span class="sxs-lookup"><span data-stu-id="ef4e1-190">Understand internal stylesheets</span></span>  

<span data-ttu-id="ef4e1-191">Les feuilles de style internes appliquent des styles à **l’aide de sélecteurs.**</span><span class="sxs-lookup"><span data-stu-id="ef4e1-191">Internal stylesheets apply styles using **selectors**.</span></span>  <span data-ttu-id="ef4e1-192">Les sélecteurs sont des modèles qui peuvent s’appliquer à un ou plusieurs éléments HTML.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-192">Selectors are patterns that may apply to one or more HTML elements.</span></span>  <span data-ttu-id="ef4e1-193">L’extrait de code précédent a ajouté le style suivant.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-193">The previous code snippet added the following style.</span></span>  

```html
<style>
    li a {
      font-family: 'Courier New', Courier, Serif;
    }
</style>
```  

`li a` <span data-ttu-id="ef4e1-194">est un sélecteur qui se traduit par « tout `<li>` élément qui contient un élément `<a>` ».</span><span class="sxs-lookup"><span data-stu-id="ef4e1-194">is a selector that translates to "any `<li>` element that contains an `<a>` element".</span></span>  <span data-ttu-id="ef4e1-195">Le navigateur modifie la police des **liens** d’accueil et de **contact,** car chacun des groupes de balises correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-195">The browser changes the font of the **Home** and **Contact** links because each of the tag groups match the pattern.</span></span>  

```html
<li><a href="/">Home</a></li>
<li><a href="/contact.html">Contact</a></li>
```  

`font-family: 'Courier New', Courier, serif` <span data-ttu-id="ef4e1-196">est une **déclaration**.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-196">is a **declaration**.</span></span>  <span data-ttu-id="ef4e1-197">Une déclaration est faite des deux parties suivantes.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-197">A declaration is made of following two parts.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="ef4e1-198">property</span><span class="sxs-lookup"><span data-stu-id="ef4e1-198">property</span></span>**  
   :::column-end:::
   :::column span="1":::
      `font-family`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="ef4e1-199">La propriété décrit une manière générale de modifier le style de l’élément.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-199">The property describes a general way that you are able to change the style of the element.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="ef4e1-200">value</span><span class="sxs-lookup"><span data-stu-id="ef4e1-200">value</span></span>**  
   :::column-end:::
   :::column span="1":::
      `'Courier New', Courier, serif`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="ef4e1-201">La valeur décrit exactement comment le style de l’élément doit changer.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-201">The value describes exactly how the style of the element should change.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="ef4e1-202">Par exemple, `font-family: 'Courier New', Courier, serif` donne au navigateur l’instruction suivante : « Définissez la police des éléments qui correspondent au `li a` modèle `'Courier New'` .</span><span class="sxs-lookup"><span data-stu-id="ef4e1-202">For example, `font-family: 'Courier New', Courier, serif` gives the browser the following instruction:  "Set the font of elements that match the pattern `li a` to `'Courier New'`.</span></span>  <span data-ttu-id="ef4e1-203">Si cette police n’est pas disponible, utilisez `Courier` .</span><span class="sxs-lookup"><span data-stu-id="ef4e1-203">If that font is not available, use `Courier`.</span></span>  <span data-ttu-id="ef4e1-204">Si ce n’est pas disponible, utilisez `serif` . »</span><span class="sxs-lookup"><span data-stu-id="ef4e1-204">If that is not available, use `serif`."</span></span>  

### <a name="add-multiple-selectors-to-a-ruleset"></a><span data-ttu-id="ef4e1-205">Ajouter plusieurs sélecteurs à un jeu de règles</span><span class="sxs-lookup"><span data-stu-id="ef4e1-205">Add multiple selectors to a ruleset</span></span>  

<span data-ttu-id="ef4e1-206">Un bloc de code CSS comme l’extrait de code suivant est appelé un **jeu de règles.**</span><span class="sxs-lookup"><span data-stu-id="ef4e1-206">A block of CSS code like the following code snippet is called a **ruleset**.</span></span>  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

<span data-ttu-id="ef4e1-207">Effectuer les actions suivantes pour utiliser des virgules afin d’ajouter plusieurs sélecteurs à un jeu de règles.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-207">Complete the following actions to use commas to add multiple selectors to a ruleset.</span></span>  

1.  <span data-ttu-id="ef4e1-208">Dans **l’onglet Éditeur,** ouvrez `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="ef4e1-208">In the **editor tab**, open `contact.html`.</span></span>  
1.  <span data-ttu-id="ef4e1-209">Après `li a` le type `, h1` .</span><span class="sxs-lookup"><span data-stu-id="ef4e1-209">After `li a` type `, h1`.</span></span>  
    
    ```html
    <style>
        li a, h1 {
          font-family: 'Courier New', Courier, Serif;
        }
    </style>
    ```  
    
    <span data-ttu-id="ef4e1-210">L’extrait de code précédent indique au navigateur de styler les éléments de la même façon qu’il styles les éléments `<h1>` qui correspondent au modèle `li a` .</span><span class="sxs-lookup"><span data-stu-id="ef4e1-210">The previous code snippet tells the browser to style `<h1>` elements the same way that it styles elements that match the pattern `li a`.</span></span>  
    
1.  <span data-ttu-id="ef4e1-211">Accédez à **l’onglet en direct.**</span><span class="sxs-lookup"><span data-stu-id="ef4e1-211">Navigate to the **live tab**.</span></span>  
1.  <span data-ttu-id="ef4e1-212">Choisissez le **lien de** contact pour revenir à la page de contact.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-212">Choose the **Contact** link to go back to the contact page.</span></span>  <span data-ttu-id="ef4e1-213">À présent, **contactez-moi !**</span><span class="sxs-lookup"><span data-stu-id="ef4e1-213">Now, **Contact Me!**</span></span> <span data-ttu-id="ef4e1-214">a la même police que les liens de navigation.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-214">has the same font as the navigation links.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-multiple1.msft.png" alt-text="Le texte Me contacter !  a maintenant la même police que les liens d’accueil et de contact" lightbox="../media/beginners-css-multiple1.msft.png":::
       <span data-ttu-id="ef4e1-217">Le texte **Me contacter !**</span><span class="sxs-lookup"><span data-stu-id="ef4e1-217">The text **Contact Me!**</span></span> <span data-ttu-id="ef4e1-218">a maintenant la même police que les liens **d’accueil** **et de** contact</span><span class="sxs-lookup"><span data-stu-id="ef4e1-218">now has the same font as the **Home** and **Contact** links</span></span>  
    :::image-end:::  
    
## <a name="experiment-with-devtools"></a><span data-ttu-id="ef4e1-219">Expérimenter Avec DevTools</span><span class="sxs-lookup"><span data-stu-id="ef4e1-219">Experiment with DevTools</span></span>  

<span data-ttu-id="ef4e1-220">Lorsque vous poursuivez votre parcours pour devenir un expert en développement web, il se peut que vous trouviez que CSS est difficile.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-220">As you continue your journey to become an expert in web development, you may find that CSS is tricky.</span></span>  <span data-ttu-id="ef4e1-221">Vous pouvez écrire du CSS et vous attendre à ce qu’il s’affiche dans un sens, mais le navigateur fait quelque chose de complètement différent.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-221">You may write some CSS and expect it to display one way, but the browser does something completely different.</span></span>  <span data-ttu-id="ef4e1-222">Microsoft Edge DevTools facilite l’expérimentation des modifications et l’affichage immédiat de l’impact de ces modifications sur la page.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-222">Microsoft Edge DevTools makes it easy to experiment with changes and immediately display how the changes affect the page.</span></span>  

### <a name="add-a-declaration-to-an-existing-rulest-in-devtools"></a><span data-ttu-id="ef4e1-223">Ajouter une déclaration à un rulest existant dans DevTools</span><span class="sxs-lookup"><span data-stu-id="ef4e1-223">Add a declaration to an existing rulest in DevTools</span></span>  

<span data-ttu-id="ef4e1-224">Complétez les actions suivantes pour itérer sur le style d’un élément existant, ajoutez une déclaration à un jeu de règles existant.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-224">Complete the following actions to iterate on the style of an existing element, add a declaration to an existing ruleset.</span></span>  

1.  <span data-ttu-id="ef4e1-225">Pointez sur le **lien Accueil,** ouvrez le menu contextuel \(clic droit\), puis choisissez **Inspecter**.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-225">Hover on the **Home** link, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add1.msft.png" alt-text="Inspecter le lien Accueil" lightbox="../media/beginners-css-add1.msft.png":::
       <span data-ttu-id="ef4e1-227">Inspecter le lien Accueil</span><span class="sxs-lookup"><span data-stu-id="ef4e1-227">Inspect the Home link</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="ef4e1-228">DevTools s’ouvre à côté de votre page.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-228">DevTools opens up alongside your page.</span></span>  <span data-ttu-id="ef4e1-229">Le code qui représente le lien Accueil est `<a href="/">Home</a>` mis en surbrillant en bleu dans l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-229">The code that represents the Home link, `<a href="/">Home</a>` is highlighted blue in the DOM Tree.</span></span>  <span data-ttu-id="ef4e1-230">L’extrait de code et l’aperçu doivent être familiers à partir de La mise en route avec [HTML et le DOM][DevtoolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="ef4e1-230">The code snippet and preview should be familiar from [Get Started with HTML and the DOM][DevtoolsBeginnersHtml].</span></span>  
    
    :::row:::
       :::column span="":::
          <span data-ttu-id="ef4e1-231">Dans la figure suivante, la déclaration que vous avez précédemment ajoutée s’affiche dans l’onglet Styles sous `font-family: 'Courier New', Courier, serif` `contact.html` l’arborescence DOM. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ef4e1-231">In the following figure, the `font-family: 'Courier New', Courier, serif` declaration that you previously added to `contact.html` is displayed in the **Styles** tab below the DOM Tree.</span></span>  
          
          :::image type="complex" source="../media/beginners-css-add2.msft.png" alt-text="L’onglet Styles se trouve sous l’arborescence DOM" lightbox="../media/beginners-css-add2.msft.png":::
             <span data-ttu-id="ef4e1-233">**L’onglet Styles** se trouve sous l’arborescence DOM</span><span class="sxs-lookup"><span data-stu-id="ef4e1-233">The **Styles** tab is below the DOM Tree</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="ef4e1-234">Si votre fenêtre DevTools est large, l’onglet Styles se trouve à droite de l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-234">If your DevTools window is wide, the Styles tab is to the right of the DOM Tree.</span></span>  
          
          :::image type="complex" source="../media/beginners-css-add3.msft.png" alt-text="L’onglet Styles se trouve à droite de l’arborescence DOM" lightbox="../media/beginners-css-add3.msft.png":::
             <span data-ttu-id="ef4e1-236">**L’onglet Styles** se trouve à droite de l’arborescence DOM</span><span class="sxs-lookup"><span data-stu-id="ef4e1-236">The **Styles** tab is to the right of the DOM Tree</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="ef4e1-237">Choisissez la ligne vide `font-family: 'Courier New', Courier, Serif` ci-dessous pour ajouter une nouvelle déclaration.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-237">Choose the empty line below `font-family: 'Courier New', Courier, Serif` to add a new declaration.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add4.msft.png" alt-text="Ajouter une nouvelle déclaration" lightbox="../media/beginners-css-add4.msft.png":::
       <span data-ttu-id="ef4e1-239">Ajouter une nouvelle déclaration</span><span class="sxs-lookup"><span data-stu-id="ef4e1-239">Add a new declaration</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ef4e1-240">Tapez `color` et sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="ef4e1-240">Type `color` and select `Enter`.</span></span>  <span data-ttu-id="ef4e1-241">L’interface utilisateur de la mise àcomplet automatique suggère des options en cours de taper.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-241">The autocomplete UI suggests options as you type.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add5.msft.png" alt-text="Couleur du type" lightbox="../media/beginners-css-add5.msft.png":::
       <span data-ttu-id="ef4e1-243">Type</span><span class="sxs-lookup"><span data-stu-id="ef4e1-243">Type</span></span> `color`  
    :::image-end:::  
    
1.  <span data-ttu-id="ef4e1-244">Tapez `magenta` et sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="ef4e1-244">Type `magenta` and select `Enter`.</span></span>  <span data-ttu-id="ef4e1-245">Tout le texte de la page de contact est désormais magenta.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-245">All of the text on the contact page is now magenta.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add6.msft.png" alt-text="Type magenta" lightbox="../media/beginners-css-add6.msft.png":::
       <span data-ttu-id="ef4e1-247">Type</span><span class="sxs-lookup"><span data-stu-id="ef4e1-247">Type</span></span> `magenta`  
    :::image-end:::  
    
### <a name="edit-a-declaration-in-devtools"></a><span data-ttu-id="ef4e1-248">Modifier une déclaration dans DevTools</span><span class="sxs-lookup"><span data-stu-id="ef4e1-248">Edit a declaration in DevTools</span></span>  

<span data-ttu-id="ef4e1-249">Effectuer les actions suivantes pour modifier les déclarations existantes dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-249">Complete the following actions to edit existing declarations in DevTools.</span></span>  

1.  <span data-ttu-id="ef4e1-250">Choisissez le carré magenta en côté `magenta` de .</span><span class="sxs-lookup"><span data-stu-id="ef4e1-250">Choose the magenta square next to `magenta`.</span></span>  <span data-ttu-id="ef4e1-251">Un s picker de couleur s’insérait.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-251">A color picker pops up.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-edit1.msft.png" alt-text="S sélectionneur de couleurs" lightbox="../media/beginners-css-edit1.msft.png":::
       <span data-ttu-id="ef4e1-253">S sélectionneur de couleurs</span><span class="sxs-lookup"><span data-stu-id="ef4e1-253">The Color Picker</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ef4e1-254">Utilisez le s sélectionneur de couleurs pour modifier le texte de police en une couleur que vous aimez.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-254">Use the color picker to change the font text to a color that you like.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-edit2.msft.png" alt-text="Modifier la couleur de police en violet avec le s picker de couleurs" lightbox="../media/beginners-css-edit2.msft.png":::
       <span data-ttu-id="ef4e1-256">Modifier la couleur de police en violet avec le s picker de couleurs</span><span class="sxs-lookup"><span data-stu-id="ef4e1-256">Change the font color to purple with the Color Picker</span></span>  
    :::image-end:::  
    
### <a name="add-a-new-ruleset-in-devtools"></a><span data-ttu-id="ef4e1-257">Ajouter un nouveau jeu de règles dans DevTools</span><span class="sxs-lookup"><span data-stu-id="ef4e1-257">Add a new ruleset in DevTools</span></span>  

<span data-ttu-id="ef4e1-258">Pour ajouter de nouveaux jeux de règles dans DevTools, complétez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-258">Complete the following actions to add new rulesets in DevTools.</span></span>  

1.  <span data-ttu-id="ef4e1-259">Choose **New Style Rule** \( New Style Rule ![ ][ImageNewStyleRuleIcon] \) which is next to **.cls**.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-259">Choose **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\) which is next to **.cls**.</span></span>  <span data-ttu-id="ef4e1-260">Un jeu de règles vide apparaît avec `a` le sélecteur.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-260">An empty ruleset appears with `a` as the selector.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule1.msft.png" alt-text="Ajouter une nouvelle règle" lightbox="../media/beginners-css-rule1.msft.png":::
       <span data-ttu-id="ef4e1-262">Ajouter une nouvelle règle</span><span class="sxs-lookup"><span data-stu-id="ef4e1-262">Add a new rule</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ef4e1-263">Remplacez `a` par `a:hover` .</span><span class="sxs-lookup"><span data-stu-id="ef4e1-263">Replace `a` with `a:hover`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule2.msft.png" alt-text="Remplacer une par une : pointer" lightbox="../media/beginners-css-rule2.msft.png":::
       <span data-ttu-id="ef4e1-265">Remplacer `a` par</span><span class="sxs-lookup"><span data-stu-id="ef4e1-265">Replace `a` with</span></span> `a:hover`  
    :::image-end:::  
    
    `:hover` <span data-ttu-id="ef4e1-266">est **une pseudo-classe**.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-266">is a **pseudo-class**.</span></span>  <span data-ttu-id="ef4e1-267">Utilisez des pseudo-classes pour les éléments de style qui peuvent entrer des états spéciaux.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-267">Use pseudo-classes for style elements that may enter special states.</span></span>  <span data-ttu-id="ef4e1-268">Par exemple, le `a:hover` style prend effet uniquement lorsque vous pointez sur un `<a>` élément.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-268">For example, the `a:hover` style only takes effect when you are hovering over an `<a>` element.</span></span>  
    
1.  <span data-ttu-id="ef4e1-269">Choisissez entre les crochets pour ajouter une nouvelle déclaration.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-269">Choose between the brackets to add a new declaration.</span></span>  
1.  <span data-ttu-id="ef4e1-270">Tapez `background-color` le nom de la déclaration et sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="ef4e1-270">Type `background-color` for the declaration name and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule3.msft.png" alt-text="Tapez couleur d’arrière-plan" lightbox="../media/beginners-css-rule3.msft.png":::
       <span data-ttu-id="ef4e1-272">Type</span><span class="sxs-lookup"><span data-stu-id="ef4e1-272">Type</span></span> `background-color`  
    :::image-end:::  
    
1.  <span data-ttu-id="ef4e1-273">Tapez `green` la valeur de déclaration et sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="ef4e1-273">Type `green` for the declaration value and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule4.msft.png" alt-text="Type vert" lightbox="../media/beginners-css-rule4.msft.png":::
       <span data-ttu-id="ef4e1-275">Type</span><span class="sxs-lookup"><span data-stu-id="ef4e1-275">Type</span></span> `green`  
    :::image-end:::  
    
1.  <span data-ttu-id="ef4e1-276">Pointez votre souris sur le **lien Accueil.**</span><span class="sxs-lookup"><span data-stu-id="ef4e1-276">Hover your mouse over the **Home** link.</span></span>  <span data-ttu-id="ef4e1-277">L’arrière-plan du lien devient vert.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-277">The background of the link turns green.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule5.msft.png" alt-text="Pointez sur le lien Accueil pour révéler son arrière-plan vert" lightbox="../media/beginners-css-rule5.msft.png":::
       <span data-ttu-id="ef4e1-279">Pointez sur le lien Accueil pour révéler son arrière-plan vert</span><span class="sxs-lookup"><span data-stu-id="ef4e1-279">Hover on the Home link to reveal its green background</span></span>  
    :::image-end:::  
    
## <a name="re-use-styles-across-pages-with-external-stylesheets"></a><span data-ttu-id="ef4e1-280">Ré-utiliser les styles entre les pages avec des feuilles de style externes</span><span class="sxs-lookup"><span data-stu-id="ef4e1-280">Re-use styles across pages with external stylesheets</span></span>  

<span data-ttu-id="ef4e1-281">Dans une étape précédente, vous avez ajouté l’extrait de code suivant en tant que feuille de style interne à `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="ef4e1-281">In a previous step, you added the following code snippet as an internal stylesheet to `contact.html`.</span></span>  

```html
...
    ...
        ...
        <style>
            li a, h1 {
              font-family: 'Courier New', Courier, Serif;
            }
        </style>
        ...
    ...
...
```  

<span data-ttu-id="ef4e1-282">Que se passe-t-il si vous `index.html` souhaitez un style identique ?</span><span class="sxs-lookup"><span data-stu-id="ef4e1-282">What if you wanted to style `index.html` the same way?</span></span>  <span data-ttu-id="ef4e1-283">Que se passe-t-il si vous avez un grand nombre de pages sur lesquelles vous souhaitez appliquer vos styles ?</span><span class="sxs-lookup"><span data-stu-id="ef4e1-283">What if you had a large number of pages to which you wanted to apply your styles?</span></span>  <span data-ttu-id="ef4e1-284">Vous devez copier et coller la feuille de style interne dans chaque page web de votre site.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-284">You have to copy and paste the internal stylesheet into every single web page on your site.</span></span>  <span data-ttu-id="ef4e1-285">Pour ajouter une feuille de style externe, vous devez effectuer les actions suivantes pour écrire votre feuille de **style** CSS une seule fois et l’appliquer à plusieurs pages.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-285">Complete the following actions to add an **External stylesheet** to allow you to write your CSS once and apply it to multiple pages.</span></span>  

1.  <span data-ttu-id="ef4e1-286">Tout d’abord, actualisez l’onglet en direct pour supprimer les modifications que vous avez apportées dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-286">First, refresh the live tab to remove the changes that you made in DevTools.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external1.msft.png" alt-text=" Une fois que vous avez actualisé la page, les modifications qui ont été apportées dans DevTools ont disparu." lightbox="../media/beginners-css-external1.msft.png":::
        <span data-ttu-id="ef4e1-288">Une fois que vous avez actualisé la page, les modifications qui ont été apportées dans DevTools ont disparu.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-288">After you refresh the page, the changes that were made in DevTools are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ef4e1-289">Revenir à **l’onglet Éditeur et** ouvrir `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="ef4e1-289">Go back to the **editor tab** and open `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external2.msft.png" alt-text="contact.html" lightbox="../media/beginners-css-external2.msft.png":::
       <span data-ttu-id="ef4e1-291">contact.html</span><span class="sxs-lookup"><span data-stu-id="ef4e1-291">contact.html</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ef4e1-292">Supprimez tout ce `<style>` qui est compris entre `</style>` et, y compris et `<style>` `</style>` .</span><span class="sxs-lookup"><span data-stu-id="ef4e1-292">Delete everything between `<style>` and `</style>`, including `<style>` and `</style>`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external3.msft.png" alt-text="La balise de style a été supprimée" lightbox="../media/beginners-css-external3.msft.png":::
       <span data-ttu-id="ef4e1-294">La balise de style a été supprimée</span><span class="sxs-lookup"><span data-stu-id="ef4e1-294">The style tag has been removed</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ef4e1-295">Ouvrez `index.html` et `style="background-color: aliceblue;"` supprimez de la `<nav>` balise.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-295">Open `index.html` and remove `style="background-color: aliceblue;"` from the `<nav>` tag.</span></span>  <span data-ttu-id="ef4e1-296">Vous avez maintenant supprimé toutes les CSS que vous avez précédemment ajoutées à votre site.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-296">You have now removed all of the CSS that you previously added to your site.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external4.msft.png" alt-text="Le style inline a été supprimé de l’élément de navigation" lightbox="../media/beginners-css-external4.msft.png":::
       <span data-ttu-id="ef4e1-298">Le style inline a été supprimé de l’élément de navigation</span><span class="sxs-lookup"><span data-stu-id="ef4e1-298">The inline style has been removed from the nav element</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ef4e1-299">Choose **New File**.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-299">Choose **New File**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external5.msft.png" alt-text="Boîte de dialogue nouveau fichier" lightbox="../media/beginners-css-external5.msft.png":::
       <span data-ttu-id="ef4e1-301">Boîte de dialogue nouveau fichier</span><span class="sxs-lookup"><span data-stu-id="ef4e1-301">The new file dialog</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ef4e1-302">Remplacez `cool-file.js` par et choisissez Ajouter un `style.css` **fichier.**</span><span class="sxs-lookup"><span data-stu-id="ef4e1-302">Replace `cool-file.js` with `style.css` and choose **Add File**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external6.msft.png" alt-text="Type style.css" lightbox="../media/beginners-css-external6.msft.png":::
       <span data-ttu-id="ef4e1-304">Type</span><span class="sxs-lookup"><span data-stu-id="ef4e1-304">Type</span></span> `style.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="ef4e1-305">Ajoutez l’extrait de code suivant à votre `style.css` fichier.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-305">Add the following code snippet to your `style.css` file.</span></span>  
    
    ```css
    li a, h1 {
      font-family: 'Courier New', Courier, Serif;
    }
    a:hover {
      background-color: green;
    }
    nav {
      background-color: aliceblue;
    }
    ```  
    
    :::image type="complex" source="../media/beginners-css-external7.msft.png" alt-text="Ajouter du code à style.css" lightbox="../media/beginners-css-external7.msft.png":::
       <span data-ttu-id="ef4e1-307">Ajouter du code à</span><span class="sxs-lookup"><span data-stu-id="ef4e1-307">Add code to</span></span> `style.css`  
    :::image-end:::  
    
    <span data-ttu-id="ef4e1-308">Assurez-vous que vous avez créé une feuille de style externe.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-308">Ensure that you have created an external stylesheet.</span></span> <span data-ttu-id="ef4e1-309">Votre code HTML ne sait pas qu’il existe.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-309">Your HTML is not aware that it exists.</span></span>  
    
1.  <span data-ttu-id="ef4e1-310">Ouvrez `index.html` .</span><span class="sxs-lookup"><span data-stu-id="ef4e1-310">Open `index.html`.</span></span>  
1.  <span data-ttu-id="ef4e1-311">`<link rel="stylesheet" href="style.css">`Ajoutez-le à votre code HTML.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-311">Add `<link rel="stylesheet" href="style.css">` to your HTML.</span></span>  
    
    ```html
    <head>
        ...
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="style.css">
    </head>
    ```  
    
    :::image type="complex" source="../media/beginners-css-external8.msft.png" alt-text="Lien vers style.css" lightbox="../media/beginners-css-external8.msft.png":::
       <span data-ttu-id="ef4e1-313">Lien vers</span><span class="sxs-lookup"><span data-stu-id="ef4e1-313">Link to</span></span> `style.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="ef4e1-314">Ouvrez `contact.html` le fichier et ajoutez-y le lien.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-314">Open the `contact.html` file and add the link there.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external9.msft.png" alt-text="Lien vers style.css dans contact.html" lightbox="../media/beginners-css-external9.msft.png":::
       <span data-ttu-id="ef4e1-316">Lien vers `style.css` l’in</span><span class="sxs-lookup"><span data-stu-id="ef4e1-316">Link to `style.css` in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="ef4e1-317">Accédez à **l’onglet en direct.**  La page d’accueil possède désormais la même police que dans la dernière section et une section de navigation bleue.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-317">Navigate to the **live tab**.  The home page now has the same font from the last section and a blue navigation section.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external10.msft.png" alt-text="Page d’accueil" lightbox="../media/beginners-css-external10.msft.png":::
       <span data-ttu-id="ef4e1-319">Page d’accueil</span><span class="sxs-lookup"><span data-stu-id="ef4e1-319">The home page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ef4e1-320">Choisissez le **lien Contact** pour accéder à la page de contact.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-320">Choose the **Contact** link to navigate to the contact page.</span></span>  <span data-ttu-id="ef4e1-321">La page de contact a la même mise en forme que la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-321">The contact page has the same formatting as the home page.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external11.msft.png" alt-text="Page de contact" lightbox="../media/beginners-css-external11.msft.png":::
       <span data-ttu-id="ef4e1-323">Page de contact</span><span class="sxs-lookup"><span data-stu-id="ef4e1-323">The contact page</span></span>  
    :::image-end:::  
    
## <a name="use-a-css-framework"></a><span data-ttu-id="ef4e1-324">Utiliser une infrastructure CSS</span><span class="sxs-lookup"><span data-stu-id="ef4e1-324">Use a CSS framework</span></span>  

<span data-ttu-id="ef4e1-325">**Les frameworks CSS** sont des collections de styles conçues par d’autres développeurs qui facilitent la création de sites web attrayants.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-325">**CSS frameworks** are collections of styles built by other developers that make it easier to create attractive web sites.</span></span>  <span data-ttu-id="ef4e1-326">Au lieu de définir vous-même les styles, une infrastructure vous fournit une collection de styles que vous pouvez utiliser sur vos éléments de page.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-326">Instead of defining styles yourself, a framework provides you a collection of styles that you are able to use on your page elements.</span></span>  

1.  <span data-ttu-id="ef4e1-327">Copiez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="ef4e1-327">Copy the following code:</span></span>  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  <span data-ttu-id="ef4e1-328">Ouvrez l’onglet Édition et collez le code dans `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="ef4e1-328">Open the editing tab and paste the code into `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework1.msft.png" alt-text="Lien vers l’infrastructure dans contact.html" lightbox="../media/beginners-css-framework1.msft.png":::
       <span data-ttu-id="ef4e1-330">Lien vers l’infrastructure dans</span><span class="sxs-lookup"><span data-stu-id="ef4e1-330">Link to the framework in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="ef4e1-331">Ouvrez `index.html` le fichier et ajoutez-y le code.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-331">Open the `index.html` file and add the code there.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework2.msft.png" alt-text="Lien vers l’infrastructure dans index.html" lightbox="../media/beginners-css-framework2.msft.png":::
       <span data-ttu-id="ef4e1-333">Lien vers l’infrastructure dans</span><span class="sxs-lookup"><span data-stu-id="ef4e1-333">Link to the framework in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="ef4e1-334">Revenir à l’onglet en direct pour afficher vos modifications.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-334">Go back to the live tab to view your changes.</span></span>  <span data-ttu-id="ef4e1-335">Bien que la couleur d’arrière-plan de l’élément et la police des éléments et des éléments soient identiques, la police des autres éléments `<nav>` `<li>` a `<a>` changé.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-335">While the background color of the `<nav>` element and the font of the `<li>` and `<a>` elements are the same, the font of the other elements has changed.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework3.msft.png" alt-text="Une partie de la police de la page d’accueil a été modifiée en raison de l’infrastructure" lightbox="../media/beginners-css-framework3.msft.png":::
       <span data-ttu-id="ef4e1-337">Une partie de la police de la page d’accueil a été modifiée en raison de l’infrastructure</span><span class="sxs-lookup"><span data-stu-id="ef4e1-337">Some of the font on the home page changed because of the framework</span></span>  
    :::image-end:::  
    
### <a name="use-a-class"></a><span data-ttu-id="ef4e1-338">Utiliser une classe</span><span class="sxs-lookup"><span data-stu-id="ef4e1-338">Use a class</span></span>  

<span data-ttu-id="ef4e1-339">Dans la dernière section, vous avez ajouté Bootstrap à vos pages web, ce qui a modifié les polices de certains éléments de votre site.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-339">In the last section, you added Bootstrap to your web pages, which changed the fonts of some of the elements on your site.</span></span>  <span data-ttu-id="ef4e1-340">Les frameworks CSS vous aident à apporter des modifications majeures à votre page avec très peu de code.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-340">CSS frameworks help you make major changes to your page with very little code.</span></span>  <span data-ttu-id="ef4e1-341">Pour modifier votre en-tête, complétez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-341">Complete the following actions to change your header.</span></span>  

1.  <span data-ttu-id="ef4e1-342">Copiez l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-342">Copy the following code snippet.</span></span>  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  <span data-ttu-id="ef4e1-343">Ajoutez l’extrait de code précédent à votre `<header>` balise dans `index.html` .</span><span class="sxs-lookup"><span data-stu-id="ef4e1-343">Add the previous code snippet to your `<header>` tag in `index.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron1.msft.png" alt-text="Ajouter des classes dans index.html" lightbox="../media/beginners-css-jumbotron1.msft.png":::
       <span data-ttu-id="ef4e1-345">Ajouter des classes dans</span><span class="sxs-lookup"><span data-stu-id="ef4e1-345">Add classes in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="ef4e1-346">Ajoutez le code à `<header>` votre balise dans `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="ef4e1-346">Add the code to your `<header>` tag in `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron2.msft.png" alt-text="Ajouter des classes dans contact.html" lightbox="../media/beginners-css-jumbotron2.msft.png":::
       <span data-ttu-id="ef4e1-348">Ajouter des classes dans</span><span class="sxs-lookup"><span data-stu-id="ef4e1-348">Add classes in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="ef4e1-349">Affichez vos modifications dans l’onglet en direct.  Il y a une grande zone grise autour de votre en-tête.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-349">View your changes in the live tab.  There is a big, grey box around your header.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron3.msft.png" alt-text="L’en-tête est maintenant encadré d’une grande zone grise" lightbox="../media/beginners-css-jumbotron3.msft.png":::
       <span data-ttu-id="ef4e1-351">L’en-tête est maintenant encadré d’une grande zone grise</span><span class="sxs-lookup"><span data-stu-id="ef4e1-351">The header now has a big, grey box around it</span></span>  
    :::image-end:::  
    
### <a name="understand-classes"></a><span data-ttu-id="ef4e1-352">Comprendre les classes</span><span class="sxs-lookup"><span data-stu-id="ef4e1-352">Understand classes</span></span>  

<span data-ttu-id="ef4e1-353">Les classes vous permet d’affecter des collections de styles à des éléments arbitraires.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-353">Classes let you assign collections of styles to arbitrary elements.</span></span>  <span data-ttu-id="ef4e1-354">Utilisez l’extrait de code suivant pour appliquer plusieurs styles à l’élément après avoir définie `<header>` `class` l’attribut sur `jumbotron` .</span><span class="sxs-lookup"><span data-stu-id="ef4e1-354">Use the following code snippet to apply several styles to the `<header>` element after you set the `class` attribute to `jumbotron`.</span></span>  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

<span data-ttu-id="ef4e1-355">L’un des avantages d’une classe est qu’elle vous permet d’appliquer des styles aux éléments de votre souhaitez.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-355">One advantage of a class is that it lets you apply styles to whatever elements you want.</span></span>  <span data-ttu-id="ef4e1-356">Par exemple, supposons que vous vouliez définir la couleur d’arrière-plan de certains éléments sur `<p>` violet, mais pas sur tous les `<p>` éléments.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-356">For example, suppose you want to set the background color of some `<p>` elements to purple, but not all `<p>` elements.</span></span>  <span data-ttu-id="ef4e1-357">Utilisez l’extrait de code suivant pour définir le style dans une classe.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-357">Use the following code snippet to define the style in a class.</span></span>  

```css
.custom-background {
  background-color: purple;
}
```  

<span data-ttu-id="ef4e1-358">Ensuite, appliquez la classe uniquement aux éléments `<p>` que vous souhaitez appliquer au style.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-358">Next, apply the class to only the `<p>` elements that you want to style.</span></span>  

```html
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
```  

### <a name="align-elements"></a><span data-ttu-id="ef4e1-359">Aligner les éléments</span><span class="sxs-lookup"><span data-stu-id="ef4e1-359">Align elements</span></span>  

<span data-ttu-id="ef4e1-360">Effectuer les actions suivantes pour amorcer et fournir des classes pour aligner les éléments.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-360">Complete the following actions to bootstrap and provide classes for aligning elements.</span></span>  

1.  <span data-ttu-id="ef4e1-361">Revenir à l’onglet Éditeur et ouvrir `index.html` .</span><span class="sxs-lookup"><span data-stu-id="ef4e1-361">Go back to the editor tab and open `index.html`.</span></span>  
1.  <span data-ttu-id="ef4e1-362">Ajoutez `class="container-fluid"` à votre `<body>` balise.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-362">Add `class="container-fluid"` to your `<body>` tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align1.msft.png" alt-text="Ajouter la classe fluide conteneur" lightbox="../media/beginners-css-align1.msft.png":::
       <span data-ttu-id="ef4e1-364">Ajouter la `container-fluid` classe</span><span class="sxs-lookup"><span data-stu-id="ef4e1-364">Add the `container-fluid` class</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ef4e1-365">Encapsulez `<nav>` vos éléments et vos `<main>` `<div class="row">` éléments.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-365">Wrap your `<nav>` and `<main>` elements in `<div class="row">`.</span></span>  <span data-ttu-id="ef4e1-366">Veillez à placer `</div>` après afin de fermer correctement la nouvelle `</main>` balise.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-366">Make sure to put `</div>` after `</main>` in order to properly close the new tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align2.msft.png" alt-text="Ajouter une ligne" lightbox="../media/beginners-css-align2.msft.png":::
       <span data-ttu-id="ef4e1-368">Ajouter une ligne</span><span class="sxs-lookup"><span data-stu-id="ef4e1-368">Add a row</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ef4e1-369">`class="col-3"`Ajoutez-la `<nav>` à votre balise et à votre `class="col-9"` `<main>` balise.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-369">Add `class="col-3"` to your `<nav>` tag and `class="col-9"` to your `<main>` tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align3.msft.png" alt-text="Ajouter les classes col-3 et col-9" lightbox="../media/beginners-css-align3.msft.png":::
       <span data-ttu-id="ef4e1-371">Ajouter les `col-3` `col-9` classes et les classes</span><span class="sxs-lookup"><span data-stu-id="ef4e1-371">Add the `col-3` and `col-9` classes</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ef4e1-372">Affichez vos modifications dans l’onglet en direct.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-372">View your changes in the live tab.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align4.msft.png" alt-text="Le contenu de navigation se trouve maintenant à gauche du contenu principal" lightbox="../media/beginners-css-align4.msft.png":::
       <span data-ttu-id="ef4e1-374">Le contenu de navigation se trouve maintenant à gauche du contenu principal</span><span class="sxs-lookup"><span data-stu-id="ef4e1-374">The nav content is now to the left of the main content</span></span>  
    :::image-end:::  
    
## <a name="next-steps"></a><span data-ttu-id="ef4e1-375">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="ef4e1-375">Next steps</span></span>  

<span data-ttu-id="ef4e1-376">Félicitations, vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-376">Congratulations, you are done.</span></span>  

*   <span data-ttu-id="ef4e1-377">La meilleure façon d’améliorer le développement web consiste à créer davantage de sites.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-377">The best way to get better at web development is to build more sites.</span></span>  <span data-ttu-id="ef4e1-378">Ne vous inquiétez pas de la casse.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-378">Do not worry about breaking stuff.</span></span>  <span data-ttu-id="ef4e1-379">Il vous suffit de vous faire plaisir et d’apprendre autant que possible en cours de route.</span><span class="sxs-lookup"><span data-stu-id="ef4e1-379">Just have fun and learn as much as possible along the way.</span></span>  
*   <span data-ttu-id="ef4e1-380">Pour en savoir plus sur le style des pages web, accédez à [Introduction à CSS][MDNCssFirstSteps].</span><span class="sxs-lookup"><span data-stu-id="ef4e1-380">To learn more about styling web pages, navigate to [Introduction to CSS][MDNCssFirstSteps].</span></span>  
*   <span data-ttu-id="ef4e1-381">Pour en savoir plus sur l’utilisation de DevTools pour expérimenter le CSS d’une page, accédez à Démarrer avec l’affichage et la modification [de CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="ef4e1-381">To learn more about how to use DevTools to experiment with the CSS of a page, navigate to [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="ef4e1-382">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="ef4e1-382">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- image links --->  

[ImageNewStyleRuleIcon]: ../media/new-style-rule-icon.msft.png  

<!--- links  --->  

[DevtoolsBeginnersHtml]: ./html.md "DevTools pour les débutants : mise en place du code HTML et du dom | Documents Microsoft"  
[DevtoolsCssIndex]: ../css/index.md "Commencer à afficher et modifier les | Documents Microsoft"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html - | Glitch"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "Premières étapes de la CSS | MDN"  

> [!NOTE]
> <span data-ttu-id="ef4e1-388">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ef4e1-388">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ef4e1-389">La page d’origine est [trouvée ici](https://developers.google.com/web/tools/chrome-devtools/beginners/css) et est co-auteure par [Le Rédacteur technique (Intern),][KatherineJackson] Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="ef4e1-389">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/css) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="ef4e1-391">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ef4e1-391">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
