---
title: 'DevTools pour les débutants: prendre en main CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/14/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 6e005f4107764a13934f0c8f3b3cde0ab9bf98c2
ms.sourcegitcommit: 054ad92f0b8f9a15da1e3aed32e8f4379b10860f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/15/2020
ms.locfileid: "10931638"
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

# <span data-ttu-id="61816-103">DevTools pour les débutants: prendre en main CSS</span><span class="sxs-lookup"><span data-stu-id="61816-103">DevTools for beginners: Get started with CSS</span></span>  

<span data-ttu-id="61816-104">Dans ce didacticiel, vous allez apprendre à utiliser les feuilles CSS pour appliquer un style à une page Web.</span><span class="sxs-lookup"><span data-stu-id="61816-104">In this tutorial, you learn how to use CSS to style a web page.</span></span>  <span data-ttu-id="61816-105">Vous pouvez également apprendre à utiliser Microsoft Edge DevTools pour tester les changements CSS.</span><span class="sxs-lookup"><span data-stu-id="61816-105">You also learn how to use Microsoft Edge DevTools to experiment with CSS changes.</span></span>  

<span data-ttu-id="61816-106">L’article suivant est le deuxième didacticiel d’une série de didacticiels qui vous explique les notions de base du développement Web et de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="61816-106">The following article is the second tutorial in a series of tutorials that teaches you the basics of web development and Microsoft Edge DevTools.</span></span>  <span data-ttu-id="61816-107">Profitez d’une expérience pratique en créant votre propre site Web.</span><span class="sxs-lookup"><span data-stu-id="61816-107">You gain hands-on experience by actually building your own website.</span></span>  <span data-ttu-id="61816-108">Vous n’avez pas besoin de terminer le premier didacticiel avant de suivre le second.</span><span class="sxs-lookup"><span data-stu-id="61816-108">You do not have to complete the first tutorial before following the second.</span></span>  <span data-ttu-id="61816-109">La [configuration de votre code](#set-up-your-code) vous montre comment procéder à la configuration.</span><span class="sxs-lookup"><span data-stu-id="61816-109">[Set up your code](#set-up-your-code) shows you how to get set up.</span></span>  

> [!NOTE]
> <span data-ttu-id="61816-110">Ce didacticiel est conçu pour les débutants et est axé sur les notions **fondamentales du développement Web** et des notions de base de l’utilisation de devtools pour tester les feuilles CSS.</span><span class="sxs-lookup"><span data-stu-id="61816-110">This tutorial is designed for absolute beginners and focuses on both the **fundamentals of web development** and the basics of using DevTools to experiment with CSS.</span></span>  <span data-ttu-id="61816-111">Si vous avez besoin d’un didacticiel destiné uniquement à DevTools, voir [découvrir comment afficher et modifier des feuilles CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="61816-111">If you want a tutorial that only focuses on DevTools, see [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

<span data-ttu-id="61816-112">Au début du didacticiel, votre site doit ressembler à la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="61816-112">At the beginning of the tutorial, your site should look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-css-intro1.msft.png" alt-text="Aspect de votre site" lightbox="../media/beginners-css-intro1.msft.png":::
   <span data-ttu-id="61816-114">Aspect de votre site</span><span class="sxs-lookup"><span data-stu-id="61816-114">What your site currently looks like</span></span>  
:::image-end:::  

<span data-ttu-id="61816-115">À la fin du didacticiel, vous devez vous présenter comme suit.</span><span class="sxs-lookup"><span data-stu-id="61816-115">After you complete the tutorial, you site should look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-css-intro2.msft.png" alt-text="Aspect de votre site à la fin du didacticiel" lightbox="../media/beginners-css-intro2.msft.png":::
   <span data-ttu-id="61816-117">Aspect de votre site à la fin du didacticiel</span><span class="sxs-lookup"><span data-stu-id="61816-117">What your site should look like at the end of the tutorial</span></span>  
:::image-end:::  

## <span data-ttu-id="61816-118">Définis</span><span class="sxs-lookup"><span data-stu-id="61816-118">Goals</span></span>  

<span data-ttu-id="61816-119">Suivez ce didacticiel pour mieux comprendre les concepts et les tâches suivants.</span><span class="sxs-lookup"><span data-stu-id="61816-119">Follow this tutorial to better understand the following concepts and tasks.</span></span>  

*   <span data-ttu-id="61816-120">Comment utiliser les feuilles CSS pour appliquer un style à une page Web.</span><span class="sxs-lookup"><span data-stu-id="61816-120">How to use CSS to style a web page.</span></span>  
*   <span data-ttu-id="61816-121">Comment utiliser Microsoft Edge DevTools pour tester les feuilles CSS.</span><span class="sxs-lookup"><span data-stu-id="61816-121">How to use Microsoft Edge DevTools to experiment with CSS.</span></span>  
*   <span data-ttu-id="61816-122">Différence entre les infrastructures CSS et CSS.</span><span class="sxs-lookup"><span data-stu-id="61816-122">The difference between CSS and CSS frameworks.</span></span>  

<span data-ttu-id="61816-123">Vous créez un site Web réel.</span><span class="sxs-lookup"><span data-stu-id="61816-123">You are building a real website.</span></span>  

## <span data-ttu-id="61816-124">Prérequis</span><span class="sxs-lookup"><span data-stu-id="61816-124">Prerequisites</span></span>  

<span data-ttu-id="61816-125">Avant de suivre ce didacticiel, remplissez les conditions préalables suivantes.</span><span class="sxs-lookup"><span data-stu-id="61816-125">Before attempting this tutorial, complete the following prerequisites.</span></span>  

*   <span data-ttu-id="61816-126">Complétez-vous [avec HTML et le DOM][DevtoolsBeginnersHtml] ou assurez-vous que vous comprenez bien html et le DOM semblable à ce qui est enseigné dans ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="61816-126">Complete [Get Started with HTML and the DOM][DevtoolsBeginnersHtml] or make sure that you have an understanding of HTML and the DOM similar to what is taught in that tutorial.</span></span>  
*   <span data-ttu-id="61816-127">Téléchargez le navigateur Web [Microsoft Edge][MicrosoftEdgeInsider] .</span><span class="sxs-lookup"><span data-stu-id="61816-127">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="61816-128">Le didacticiel suivant utilise un ensemble d’outils de développement Web, appelés Microsoft Edge DevTools, qui sont intégrés à Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="61816-128">The following tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <span data-ttu-id="61816-129">Configurer votre code</span><span class="sxs-lookup"><span data-stu-id="61816-129">Set up your code</span></span>  

<span data-ttu-id="61816-130">Pour créer votre site, vous devez d’abord effectuer les actions suivantes pour configurer votre code.</span><span class="sxs-lookup"><span data-stu-id="61816-130">To create your site, you must first complete the following actions to set up your code.</span></span>  

> [!NOTE]
> <span data-ttu-id="61816-131">Si vous avez déjà effectué le premier didacticiel de la série, passez à la section suivante.</span><span class="sxs-lookup"><span data-stu-id="61816-131">If you have already completed the first tutorial in the series, skip to the next section.</span></span>  <span data-ttu-id="61816-132">Continuez à utiliser votre code à partir du dernier didacticiel, de [la mise en route de HTML et du DOM][DevtoolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="61816-132">Continue using your code from the last tutorial, [Get Started with HTML and the DOM][DevtoolsBeginnersHtml].</span></span>  

1.  <span data-ttu-id="61816-133">Ouvrez le [code source][GlitchCookedAmphibianIndex].</span><span class="sxs-lookup"><span data-stu-id="61816-133">Open the [source code][GlitchCookedAmphibianIndex].</span></span>  <span data-ttu-id="61816-134">L’onglet d’activation de votre navigateur est référencé en tant qu' **onglet de modification**.</span><span class="sxs-lookup"><span data-stu-id="61816-134">The in-focus tab of your browser is referenced as the **editing tab**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup1.msft.png" alt-text="Onglet édition" lightbox="../media/beginners-css-setup1.msft.png":::
       <span data-ttu-id="61816-136">Onglet **édition**</span><span class="sxs-lookup"><span data-stu-id="61816-136">The **editing** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="61816-137">Sélectionnez **cuit-Amphibian**.</span><span class="sxs-lookup"><span data-stu-id="61816-137">Choose **cooked-amphibian**.</span></span>  <span data-ttu-id="61816-138">Un menu s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="61816-138">A menu pops up.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup2.msft.png" alt-text="Menu options de Project" lightbox="../media/beginners-css-setup2.msft.png":::
       <span data-ttu-id="61816-140">Menu options de Project</span><span class="sxs-lookup"><span data-stu-id="61816-140">The Project Options menu</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="61816-141">Sélectionnez **Remix Project**.</span><span class="sxs-lookup"><span data-stu-id="61816-141">Choose **Remix Project**.</span></span>  <span data-ttu-id="61816-142">Le problème crée une copie du projet que vous pouvez modifier.</span><span class="sxs-lookup"><span data-stu-id="61816-142">Glitch creates a copy of the project that you are able to edit.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="61816-143">Le problème génère un nom aléatoire pour le nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="61816-143">Glitch generates a random name for the new project.</span></span>  
    
1.  <span data-ttu-id="61816-144">Sélectionnez **Afficher** et sélectionner **dans une nouvelle fenêtre**.</span><span class="sxs-lookup"><span data-stu-id="61816-144">Choose **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="61816-145">Un autre onglet s’ouvre en mode en direct de votre site.</span><span class="sxs-lookup"><span data-stu-id="61816-145">Another tab opens with a live view of your site.</span></span>  <span data-ttu-id="61816-146">L’onglet actif de votre navigateur est référencé en tant qu' **onglet actif**.</span><span class="sxs-lookup"><span data-stu-id="61816-146">The in-focus tab of your browser is referenced as the **live tab**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup3.msft.png" alt-text="Onglet Live" lightbox="../media/beginners-css-setup3.msft.png":::
       <span data-ttu-id="61816-148">**Onglet Live**</span><span class="sxs-lookup"><span data-stu-id="61816-148">The **live tab**</span></span>  
    :::image-end:::  

## <span data-ttu-id="61816-149">Comprendre CSS</span><span class="sxs-lookup"><span data-stu-id="61816-149">Understand CSS</span></span>  

<span data-ttu-id="61816-150">**CSS** est un langage informatique qui détermine la disposition et le style des pages Web.</span><span class="sxs-lookup"><span data-stu-id="61816-150">**CSS** is a computer language that determines the layout and styling of web pages.</span></span>  <span data-ttu-id="61816-151">La figure suivante représente un paragraphe avec une bordure.</span><span class="sxs-lookup"><span data-stu-id="61816-151">The following figure is a paragraph with a border.</span></span>  

:::image type="complex" source="../media/beginners-css-red_paragraph.msft.png" alt-text="Le texte est mis en forme à l’aide de feuilles CSS" lightbox="../media/beginners-css-red_paragraph.msft.png":::
   <span data-ttu-id="61816-153">Le texte est mis en forme à l’aide de feuilles CSS</span><span class="sxs-lookup"><span data-stu-id="61816-153">The text has been styled with CSS</span></span>  
:::image-end:::  

<span data-ttu-id="61816-154">L’extrait de code suivant correspond au code HTML et au code CSS utilisé pour créer le paragraphe dans l’illustration précédente.</span><span class="sxs-lookup"><span data-stu-id="61816-154">The following code snippet is the HTML and CSS code used to create the paragraph in the previous figure.</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` <span data-ttu-id="61816-155">C’est probablement une nouveauté.</span><span class="sxs-lookup"><span data-stu-id="61816-155">probably looks new to you.</span></span>  <span data-ttu-id="61816-156">Le reste devrait vous être familier.</span><span class="sxs-lookup"><span data-stu-id="61816-156">The rest should look familiar.</span></span>  <span data-ttu-id="61816-157">Si ce n’est pas le cas, terminez- [le en utilisant le code HTML et le DOM][DevtoolsBeginnersHtml] avant de commencer les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="61816-157">If not, complete [Get Started with HTML and the DOM][DevtoolsBeginnersHtml] before attempting the following sections.</span></span>  

## <span data-ttu-id="61816-158">Ajouter des styles intralignes</span><span class="sxs-lookup"><span data-stu-id="61816-158">Add inline styles</span></span>  

<span data-ttu-id="61816-159">Procédez comme suit pour utiliser des **styles intralignes** et appliquer des styles à un seul élément.</span><span class="sxs-lookup"><span data-stu-id="61816-159">Complete the following actions to use **inline styles** to apply styles to a single element.</span></span>  

1.  <span data-ttu-id="61816-160">Revenez à l’onglet modification et ouvrez `index.html` .</span><span class="sxs-lookup"><span data-stu-id="61816-160">Go back to the editing tab and open `index.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-inline1.msft.png" alt-text="index.html" lightbox="../media/beginners-css-inline1.msft.png":::
       <span data-ttu-id="61816-162">Ouvrir `index.html` dans l’onglet édition</span><span class="sxs-lookup"><span data-stu-id="61816-162">Open `index.html` in the editing tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="61816-163">Ajoutez `style="background-color: aliceblue;"` à votre `<nav>` .</span><span class="sxs-lookup"><span data-stu-id="61816-163">Add `style="background-color: aliceblue;"` to your `<nav>`.</span></span>  <span data-ttu-id="61816-164">Dans le bloc de code ci-dessous, la quatrième ligne de code est celle que vous devez modifier.</span><span class="sxs-lookup"><span data-stu-id="61816-164">In the code block below, the fourth line of code is the one you need to change.</span></span>  <span data-ttu-id="61816-165">Le reste est là pour vous permettre de vérifier que vous avez bien placé le nouveau code au bon endroit.</span><span class="sxs-lookup"><span data-stu-id="61816-165">The rest is just there, so you are able to ensure that you are putting the new code in the right place.</span></span>  
    
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
    
1.  <span data-ttu-id="61816-166">Accédez à l' **onglet Live** pour afficher les modifications.</span><span class="sxs-lookup"><span data-stu-id="61816-166">Go to the **live tab** to see the changes!</span></span>  <span data-ttu-id="61816-167">L’arrière-plan de la `<nav>` section est désormais bleu.</span><span class="sxs-lookup"><span data-stu-id="61816-167">The background of the `<nav>` section is now blue.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-inline2.msft.png" alt-text="La couleur d’arrière-plan derrière les liens accueil et contact est désormais bleue" lightbox="../media/beginners-css-inline2.msft.png":::
       <span data-ttu-id="61816-169">La couleur d’arrière-plan derrière les liens **Accueil** et **contact** est désormais bleue</span><span class="sxs-lookup"><span data-stu-id="61816-169">The background color behind the **Home** and **Contact** links is now blue</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="61816-170">Réutiliser les styles sur une seule page à l’aide de feuilles de style internes</span><span class="sxs-lookup"><span data-stu-id="61816-170">Re-use styles on a single page with internal stylesheets</span></span>  

<span data-ttu-id="61816-171">Dans l’extrait de code précédent, un style intraligne a appliqué un style à une seule `<p>` balise.</span><span class="sxs-lookup"><span data-stu-id="61816-171">In a previous code snippet, an inline style applied a style to a single `<p>` tag.</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

<span data-ttu-id="61816-172">Que faire si vous souhaitez que tous les `<p>` éléments d’une page Web soient stylisés de la même manière?</span><span class="sxs-lookup"><span data-stu-id="61816-172">What if you wanted all of the `<p>` elements on your webpage to be styled the same way?</span></span>  <span data-ttu-id="61816-173">Vous devez copier et coller le code dans chaque `<p>` balise unique de votre site.</span><span class="sxs-lookup"><span data-stu-id="61816-173">You would have to copy and paste the code into every single `<p>` tag on your site.</span></span>  <span data-ttu-id="61816-174">Il s’agit d’un temps considérable.</span><span class="sxs-lookup"><span data-stu-id="61816-174">That is a lot of time and effort.</span></span>  <span data-ttu-id="61816-175">Et si vous avez besoin d’effectuer une modification, vous devrez à nouveau modifier chaque balise.</span><span class="sxs-lookup"><span data-stu-id="61816-175">And, if you needed to make an edit, you would have to change every tag again.</span></span>  <span data-ttu-id="61816-176">Procédez comme suit pour utiliser une **feuille de style interne** pour écrire votre CSS une seule fois, afin qu’elle s’applique à plusieurs éléments.</span><span class="sxs-lookup"><span data-stu-id="61816-176">Complete the following actions to use an **Internal stylesheet** to write your CSS once so that it applies to multiple elements.</span></span>  

1.  <span data-ttu-id="61816-177">Dans l’onglet Live, sélectionnez **contact** pour accéder à la page de contact.</span><span class="sxs-lookup"><span data-stu-id="61816-177">In the live tab, choose **Contact** to go to the contact page.</span></span>  <span data-ttu-id="61816-178">Notez la police **Accueil** et **contact**.</span><span class="sxs-lookup"><span data-stu-id="61816-178">Notice the font of **Home** and **Contact**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-internal1.msft.png" alt-text="Page de contact" lightbox="../media/beginners-css-internal1.msft.png":::
       <span data-ttu-id="61816-180">Page de contact</span><span class="sxs-lookup"><span data-stu-id="61816-180">The Contact page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="61816-181">Dans l' **onglet Éditeur**, accédez à `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="61816-181">In the **editor tab**, go to `contact.html`.</span></span>  
1.  <span data-ttu-id="61816-182">Ajoutez le code suivant à `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="61816-182">Add the following code to `contact.html`.</span></span>  <span data-ttu-id="61816-183">Rappelez-vous que les lignes commençant par `<style>` et se terminant par `</style>` sont celles que vous devez ajouter.</span><span class="sxs-lookup"><span data-stu-id="61816-183">Remember, the lines starting with `<style>` and ending with `</style>` are what you need to add.</span></span>  <span data-ttu-id="61816-184">L’autre code est là pour vous indiquer où placer le nouveau code.</span><span class="sxs-lookup"><span data-stu-id="61816-184">The other code is just there so you know where to put the new code.</span></span>  
    
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
    
1.  <span data-ttu-id="61816-185">Revenir à l' **onglet Live**.</span><span class="sxs-lookup"><span data-stu-id="61816-185">Go back to the **live tab**.</span></span>  
1.  <span data-ttu-id="61816-186">Sélectionnez **contact** pour revenir à la page de contact.</span><span class="sxs-lookup"><span data-stu-id="61816-186">Choose **Contact** to go back to the contact page.</span></span>  <span data-ttu-id="61816-187">La police **Accueil** et **contact** a changé.</span><span class="sxs-lookup"><span data-stu-id="61816-187">The font of **Home** and **Contact** has changed.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-internal2.msft.png" alt-text="La police des liens accueil et contact a changé" lightbox="../media/beginners-css-internal2.msft.png":::
       <span data-ttu-id="61816-189">La police des liens **Accueil** et **contact** a changé</span><span class="sxs-lookup"><span data-stu-id="61816-189">The font of the **Home** and **Contact** links has changed</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="61816-190">Comprendre les feuilles de style internes</span><span class="sxs-lookup"><span data-stu-id="61816-190">Understand internal stylesheets</span></span>  

<span data-ttu-id="61816-191">Les feuilles de style internes s’appliquent aux styles à l’aide de **sélecteurs**.</span><span class="sxs-lookup"><span data-stu-id="61816-191">Internal stylesheets apply styles using **selectors**.</span></span>  <span data-ttu-id="61816-192">Les sélecteurs sont des modèles qui peuvent être appliqués à un ou plusieurs éléments HTML.</span><span class="sxs-lookup"><span data-stu-id="61816-192">Selectors are patterns that may apply to one or more HTML elements.</span></span>  <span data-ttu-id="61816-193">L’extrait de code précédent a ajouté le style suivant.</span><span class="sxs-lookup"><span data-stu-id="61816-193">The previous code snippet added the following style.</span></span>  

```html
<style>
    li a {
      font-family: 'Courier New', Courier, Serif;
    }
</style>
```  

`li a` <span data-ttu-id="61816-194">est un sélecteur qui devient «tout `<li>` élément contenant un `<a>` élément».</span><span class="sxs-lookup"><span data-stu-id="61816-194">is a selector that translates to "any `<li>` element that contains an `<a>` element".</span></span>  <span data-ttu-id="61816-195">Le navigateur modifie la police des liens **Accueil** et **contact** , car chacun des groupes de balises correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="61816-195">The browser changes the font of the **Home** and **Contact** links because each of the tag groups match the pattern.</span></span>  

```html
<li><a href="/">Home</a></li>
<li><a href="/contact.html">Contact</a></li>
```  

`font-family: 'Courier New', Courier, serif` <span data-ttu-id="61816-196">est une **déclaration**.</span><span class="sxs-lookup"><span data-stu-id="61816-196">is a **declaration**.</span></span>  <span data-ttu-id="61816-197">Une déclaration est constituée de deux parties suivies.</span><span class="sxs-lookup"><span data-stu-id="61816-197">A declaration is made of following two parts.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="61816-198">Propriétés</span><span class="sxs-lookup"><span data-stu-id="61816-198">property</span></span>**  
   :::column-end:::
   :::column span="1":::
      `font-family`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="61816-199">La propriété décrit une manière générale que vous êtes en mesure de modifier le style de l’élément.</span><span class="sxs-lookup"><span data-stu-id="61816-199">The property describes a general way that you are able to change the style of the element.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="61816-200">value</span><span class="sxs-lookup"><span data-stu-id="61816-200">value</span></span>**  
   :::column-end:::
   :::column span="1":::
      `'Courier New', Courier, serif`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="61816-201">La valeur décrit exactement le mode de modification du style de l’élément.</span><span class="sxs-lookup"><span data-stu-id="61816-201">The value describes exactly how the style of the element should change.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="61816-202">Par exemple, `font-family: 'Courier New', Courier, serif` donne au navigateur l’instruction suivante: "définissez la police des éléments qui correspondent au modèle `li a` `'Courier New'` .</span><span class="sxs-lookup"><span data-stu-id="61816-202">For example, `font-family: 'Courier New', Courier, serif` gives the browser the following instruction:  "Set the font of elements that match the pattern `li a` to `'Courier New'`.</span></span>  <span data-ttu-id="61816-203">Si cette police n’est pas disponible, utilisez `Courier` .</span><span class="sxs-lookup"><span data-stu-id="61816-203">If that font is not available, use `Courier`.</span></span>  <span data-ttu-id="61816-204">Si ce n’est pas le cas, utilisez `serif` .»</span><span class="sxs-lookup"><span data-stu-id="61816-204">If that is not available, use `serif`."</span></span>  

### <span data-ttu-id="61816-205">Ajouter plusieurs sélecteurs à un groupe de règles</span><span class="sxs-lookup"><span data-stu-id="61816-205">Add multiple selectors to a ruleset</span></span>  

<span data-ttu-id="61816-206">Un bloc de code CSS tel que celui qui apparaît ci-dessous est appelé **RuleSet**.</span><span class="sxs-lookup"><span data-stu-id="61816-206">A block of CSS code like what you see below is called a **ruleset**.</span></span>  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

<span data-ttu-id="61816-207">Effectuez les opérations suivantes pour utiliser des virgules pour ajouter plusieurs sélecteurs à un RuleSet.</span><span class="sxs-lookup"><span data-stu-id="61816-207">Complete the following actions to use commas to add multiple selectors to a ruleset.</span></span>  

1.  <span data-ttu-id="61816-208">Dans l' **onglet Éditeur**, ouvrez `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="61816-208">In the **editor tab**, open `contact.html`.</span></span>  
1.  <span data-ttu-id="61816-209">Après `li a` type `, h1` .</span><span class="sxs-lookup"><span data-stu-id="61816-209">After `li a` type `, h1`.</span></span>  
    
    ```html
    <style>
        li a, h1 {
          font-family: 'Courier New', Courier, Serif;
        }
    </style>
    ```  
    
    <span data-ttu-id="61816-210">L’extrait de code précédent indique au navigateur qu' `<h1>` il s’agit de la même façon que les éléments style qui correspondent au modèle `li a` .</span><span class="sxs-lookup"><span data-stu-id="61816-210">The previous code snippet tells the browser to style `<h1>` elements the same way that it styles elements that match the pattern `li a`.</span></span>  
    
1.  <span data-ttu-id="61816-211">Accédez à l' **onglet Live**.</span><span class="sxs-lookup"><span data-stu-id="61816-211">Go to the **live tab**.</span></span>  
1.  <span data-ttu-id="61816-212">Cliquez sur le lien de **contact** pour revenir à la page de contact.</span><span class="sxs-lookup"><span data-stu-id="61816-212">Choose the **Contact** link to go back to the contact page.</span></span>  <span data-ttu-id="61816-213">Maintenant, **Contactez-moi!**</span><span class="sxs-lookup"><span data-stu-id="61816-213">Now, **Contact Me!**</span></span> <span data-ttu-id="61816-214">a la même police que les liens de navigation.</span><span class="sxs-lookup"><span data-stu-id="61816-214">has the same font as the navigation links.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-multiple1.msft.png" alt-text="Le texte me contacter.  possède désormais la même police que les liens accueil et contact" lightbox="../media/beginners-css-multiple1.msft.png":::
       <span data-ttu-id="61816-217">Le texte **me contacter.**</span><span class="sxs-lookup"><span data-stu-id="61816-217">The text **Contact Me!**</span></span> <span data-ttu-id="61816-218">possède désormais la même police que les liens **Accueil** et **contact**</span><span class="sxs-lookup"><span data-stu-id="61816-218">now has the same font as the **Home** and **Contact** links</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="61816-219">Expérimentez avec DevTools</span><span class="sxs-lookup"><span data-stu-id="61816-219">Experiment with DevTools</span></span>  

<span data-ttu-id="61816-220">Lorsque vous continuez votre voyage pour devenir un expert en développement Web, il est possible que les feuilles de style CSS soient difficiles.</span><span class="sxs-lookup"><span data-stu-id="61816-220">As you continue your journey to become an expert in web development, you may find that CSS is tricky.</span></span>  <span data-ttu-id="61816-221">Vous pouvez écrire du code CSS et vous attendre à ce qu’il s’affiche de façon unique, mais le navigateur a un aspect complètement différent.</span><span class="sxs-lookup"><span data-stu-id="61816-221">You may write some CSS and expect it to display one way, but the browser does something completely different.</span></span>  <span data-ttu-id="61816-222">Microsoft Edge DevTools vous permet d’expérimenter facilement les modifications et de voir immédiatement l’incidence de ces modifications sur la page.</span><span class="sxs-lookup"><span data-stu-id="61816-222">Microsoft Edge DevTools makes it easy to experiment with changes and immediately see how the changes affect the page.</span></span>  

### <span data-ttu-id="61816-223">Ajouter une déclaration à une règle existante dans DevTools</span><span class="sxs-lookup"><span data-stu-id="61816-223">Add a declaration to an existing rulest in DevTools</span></span>  

<span data-ttu-id="61816-224">Procédez comme suit pour effectuer une itération sur le style d’un élément existant, ajouter une déclaration à un RuleSet existant.</span><span class="sxs-lookup"><span data-stu-id="61816-224">Complete the following actions to iterate on the style of an existing element, add a declaration to an existing ruleset.</span></span>  

1.  <span data-ttu-id="61816-225">Positionnez le pointeur sur le lien **Accueil** , ouvrez le menu contextuel, puis cliquez sur **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="61816-225">Hover on the **Home** link, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add1.msft.png" alt-text="Examiner le lien Accueil" lightbox="../media/beginners-css-add1.msft.png":::
       <span data-ttu-id="61816-227">Examiner le lien Accueil</span><span class="sxs-lookup"><span data-stu-id="61816-227">Inspect the Home link</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="61816-228">DevTools s’ouvre à côté de votre page.</span><span class="sxs-lookup"><span data-stu-id="61816-228">DevTools opens up alongside your page.</span></span>  <span data-ttu-id="61816-229">Le code qui représente le lien Accueil `<a href="/">Home</a>` est surligné en bleu dans l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="61816-229">The code that represents the Home link, `<a href="/">Home</a>` is highlighted blue in the DOM Tree.</span></span>  <span data-ttu-id="61816-230">L’extrait de code et l’aperçu doivent être familiers de la mise [en route de HTML et du DOM][DevtoolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="61816-230">The code snippet and preview should be familiar from [Get Started with HTML and the DOM][DevtoolsBeginnersHtml].</span></span>  
    
    :::row:::
       :::column span="":::
          <span data-ttu-id="61816-231">Dans l’illustration suivante, la `font-family: 'Courier New', Courier, serif` déclaration que vous avez précédemment ajoutée `contact.html` s’affiche dans l’onglet **styles** sous l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="61816-231">In the following figure, the `font-family: 'Courier New', Courier, serif` declaration that you previously added to `contact.html` is seen in the **Styles** tab below the DOM Tree.</span></span>  
          
          :::image type="complex" source="../media/beginners-css-add2.msft.png" alt-text="L’onglet styles se trouve sous l’arborescence DOM" lightbox="../media/beginners-css-add2.msft.png":::
             <span data-ttu-id="61816-233">L’onglet **styles** se trouve sous l’arborescence DOM</span><span class="sxs-lookup"><span data-stu-id="61816-233">The **Styles** tab is below the DOM Tree</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="61816-234">Si votre fenêtre DevTools est large, l’onglet styles se trouve à droite de l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="61816-234">If your DevTools window is wide, the Styles tab is to the right of the DOM Tree.</span></span>  
          
          :::image type="complex" source="../media/beginners-css-add3.msft.png" alt-text="Onglet styles à droite de l’arborescence DOM" lightbox="../media/beginners-css-add3.msft.png":::
             <span data-ttu-id="61816-236">Onglet **styles** à droite de l’arborescence DOM</span><span class="sxs-lookup"><span data-stu-id="61816-236">The **Styles** tab is to the right of the DOM Tree</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="61816-237">Sélectionnez la ligne vide ci-dessous `font-family: 'Courier New', Courier, Serif` pour ajouter une nouvelle déclaration.</span><span class="sxs-lookup"><span data-stu-id="61816-237">Choose the empty line below `font-family: 'Courier New', Courier, Serif` to add a new declaration.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add4.msft.png" alt-text="Ajouter une nouvelle déclaration" lightbox="../media/beginners-css-add4.msft.png":::
       <span data-ttu-id="61816-239">Ajouter une nouvelle déclaration</span><span class="sxs-lookup"><span data-stu-id="61816-239">Add a new declaration</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="61816-240">Tapez `color` et sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="61816-240">Type `color` and select `Enter`.</span></span>  <span data-ttu-id="61816-241">L’interface utilisateur de saisie semi-automatique suggère des options au fur et à mesure que vous tapez.</span><span class="sxs-lookup"><span data-stu-id="61816-241">The autocomplete UI suggests options as you type.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add5.msft.png" alt-text="Couleur de type" lightbox="../media/beginners-css-add5.msft.png":::
       <span data-ttu-id="61816-243">Type</span><span class="sxs-lookup"><span data-stu-id="61816-243">Type</span></span> `color`  
    :::image-end:::  
    
1.  <span data-ttu-id="61816-244">Tapez `magenta` et sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="61816-244">Type `magenta` and select `Enter`.</span></span>  <span data-ttu-id="61816-245">Tout le texte de la page de contact est désormais magenta.</span><span class="sxs-lookup"><span data-stu-id="61816-245">All of the text on the contact page is now magenta.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add6.msft.png" alt-text="Taper magenta" lightbox="../media/beginners-css-add6.msft.png":::
       <span data-ttu-id="61816-247">Type</span><span class="sxs-lookup"><span data-stu-id="61816-247">Type</span></span> `magenta`  
    :::image-end:::  
    
### <span data-ttu-id="61816-248">Modifier une déclaration dans DevTools</span><span class="sxs-lookup"><span data-stu-id="61816-248">Edit a declaration in DevTools</span></span>  

<span data-ttu-id="61816-249">Pour modifier des déclarations existantes dans DevTools, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="61816-249">Complete the following actions to edit existing declarations in DevTools.</span></span>  

1.  <span data-ttu-id="61816-250">Choisissez le carré magenta en regard de `magenta` .</span><span class="sxs-lookup"><span data-stu-id="61816-250">Choose the magenta square next to `magenta`.</span></span>  <span data-ttu-id="61816-251">Un sélecteur de couleur apparaît.</span><span class="sxs-lookup"><span data-stu-id="61816-251">A color picker pops up.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-edit1.msft.png" alt-text="Sélecteur de couleurs" lightbox="../media/beginners-css-edit1.msft.png":::
       <span data-ttu-id="61816-253">Sélecteur de couleurs</span><span class="sxs-lookup"><span data-stu-id="61816-253">The Color Picker</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="61816-254">Utilisez le sélecteur de couleurs pour remplacer le texte de la police par une couleur de votre choix.</span><span class="sxs-lookup"><span data-stu-id="61816-254">Use the color picker to change the font text to a color that you like.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-edit2.msft.png" alt-text="Changer la couleur de la police en violet grâce au sélecteur de couleurs" lightbox="../media/beginners-css-edit2.msft.png":::
       <span data-ttu-id="61816-256">Changer la couleur de la police en violet grâce au sélecteur de couleurs</span><span class="sxs-lookup"><span data-stu-id="61816-256">Change the font color to purple with the Color Picker</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="61816-257">Ajouter un nouveau RuleSet dans DevTools</span><span class="sxs-lookup"><span data-stu-id="61816-257">Add a new ruleset in DevTools</span></span>  

<span data-ttu-id="61816-258">Complétez les actions suivantes pour ajouter de nouvelles règles dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="61816-258">Complete the following actions to add new rulesets in DevTools.</span></span>  

1.  <span data-ttu-id="61816-259">Cliquez sur **nouvelle règle de style** \ ( ![ nouvelle règle de style ][ImageNewStyleRuleIcon] \) en regard de **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="61816-259">Choose **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\) which is next to **.cls**.</span></span>  <span data-ttu-id="61816-260">Un RuleSet vide apparaît avec `a` le sélecteur.</span><span class="sxs-lookup"><span data-stu-id="61816-260">An empty ruleset appears with `a` as the selector.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule1.msft.png" alt-text="Ajouter une nouvelle règle" lightbox="../media/beginners-css-rule1.msft.png":::
       <span data-ttu-id="61816-262">Ajouter une nouvelle règle</span><span class="sxs-lookup"><span data-stu-id="61816-262">Add a new rule</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="61816-263">Remplacer `a` par `a:hover` .</span><span class="sxs-lookup"><span data-stu-id="61816-263">Replace `a` with `a:hover`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule2.msft.png" alt-text="Remplacer a par a:hover" lightbox="../media/beginners-css-rule2.msft.png":::
       <span data-ttu-id="61816-265">Remplacer `a` par</span><span class="sxs-lookup"><span data-stu-id="61816-265">Replace `a` with</span></span> `a:hover`  
    :::image-end:::  
    
    `:hover` <span data-ttu-id="61816-266">est une **Pseudo-classe**.</span><span class="sxs-lookup"><span data-stu-id="61816-266">is a **pseudo-class**.</span></span>  <span data-ttu-id="61816-267">Utilisez des Pseudo-classes pour les éléments de style qui pourraient entrer des États spéciaux.</span><span class="sxs-lookup"><span data-stu-id="61816-267">Use pseudo-classes for style elements that may enter special states.</span></span>  <span data-ttu-id="61816-268">Par exemple, le `a:hover` style n’est appliqué que lorsque vous pointez sur un `<a>` élément.</span><span class="sxs-lookup"><span data-stu-id="61816-268">For example, the `a:hover` style only takes effect when you are hovering over an `<a>` element.</span></span>  
    
1.  <span data-ttu-id="61816-269">Choisissez entre les crochets pour ajouter une nouvelle déclaration.</span><span class="sxs-lookup"><span data-stu-id="61816-269">Choose between the brackets to add a new declaration.</span></span>  
1.  <span data-ttu-id="61816-270">Tapez `background-color` le nom de la déclaration et sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="61816-270">Type `background-color` for the declaration name and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule3.msft.png" alt-text="Taper couleur d’arrière-plan" lightbox="../media/beginners-css-rule3.msft.png":::
       <span data-ttu-id="61816-272">Type</span><span class="sxs-lookup"><span data-stu-id="61816-272">Type</span></span> `background-color`  
    :::image-end:::  
    
1.  <span data-ttu-id="61816-273">Tapez `green` la valeur de la déclaration et sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="61816-273">Type `green` for the declaration value and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule4.msft.png" alt-text="Taper en vert" lightbox="../media/beginners-css-rule4.msft.png":::
       <span data-ttu-id="61816-275">Type</span><span class="sxs-lookup"><span data-stu-id="61816-275">Type</span></span> `green`  
    :::image-end:::  
    
1.  <span data-ttu-id="61816-276">Positionnez le pointeur de la souris sur le lien **Accueil** .</span><span class="sxs-lookup"><span data-stu-id="61816-276">Hover your mouse over the **Home** link.</span></span>  <span data-ttu-id="61816-277">L’arrière-plan du lien devient vert.</span><span class="sxs-lookup"><span data-stu-id="61816-277">The background of the link turns green.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule5.msft.png" alt-text="Placez le pointeur de la souris sur le lien Accueil pour afficher son arrière-plan vert" lightbox="../media/beginners-css-rule5.msft.png":::
       <span data-ttu-id="61816-279">Placez le pointeur de la souris sur le lien Accueil pour afficher son arrière-plan vert</span><span class="sxs-lookup"><span data-stu-id="61816-279">Hover over the Home link to reveal its green background</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="61816-280">Réutiliser les styles entre les pages à l’aide de feuilles de style externes</span><span class="sxs-lookup"><span data-stu-id="61816-280">Re-use styles across pages with external stylesheets</span></span>  

<span data-ttu-id="61816-281">Dans une étape précédente, vous avez ajouté l’extrait de code suivant en tant que feuille de style interne à `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="61816-281">In a previous step, you added the following code snippet as an internal stylesheet to `contact.html`.</span></span>  

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

<span data-ttu-id="61816-282">Que faire si vous souhaitez changer de style `index.html` ?</span><span class="sxs-lookup"><span data-stu-id="61816-282">What if you wanted to style `index.html` the same way?</span></span>  <span data-ttu-id="61816-283">Que faire si vous avez un grand nombre de pages auxquelles vous souhaitez appliquer vos styles?</span><span class="sxs-lookup"><span data-stu-id="61816-283">What if you had a large number of pages to which you wanted to apply your styles?</span></span>  <span data-ttu-id="61816-284">Vous devez copier et coller la feuille de style interne dans chaque page Web de votre site.</span><span class="sxs-lookup"><span data-stu-id="61816-284">You would have to copy and paste the internal stylesheet into every single web page on your site.</span></span>  <span data-ttu-id="61816-285">Procédez comme suit pour ajouter une **feuille de style externe** afin de pouvoir écrire votre CSS une seule fois et l’appliquer à plusieurs pages.</span><span class="sxs-lookup"><span data-stu-id="61816-285">Complete the following actions to add an **External stylesheet** to allow you to write your CSS once and apply it to multiple pages.</span></span>  

1.  <span data-ttu-id="61816-286">Tout d’abord, rechargez l’onglet Live pour supprimer les modifications que vous avez apportées dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="61816-286">First, reload the live tab to remove the changes that you made in DevTools.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external1.msft.png" alt-text=" Suite à l’actualisation de la page, les modifications apportées à DevTools ont disparu" lightbox="../media/beginners-css-external1.msft.png":::
        <span data-ttu-id="61816-288">Suite à l’actualisation de la page, les modifications apportées à DevTools ont disparu</span><span class="sxs-lookup"><span data-stu-id="61816-288">After you refresh the page, the changes that were made in DevTools are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="61816-289">Revenez à l' **onglet Éditeur** , puis ouvrez `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="61816-289">Go back to the **editor tab** and open `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external2.msft.png" alt-text="contact.html" lightbox="../media/beginners-css-external2.msft.png":::
       <span data-ttu-id="61816-291">contact.html</span><span class="sxs-lookup"><span data-stu-id="61816-291">contact.html</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="61816-292">Supprimez tous `<style>` les éléments entre et `</style>` , y compris `<style>` et `</style>` .</span><span class="sxs-lookup"><span data-stu-id="61816-292">Delete everything between `<style>` and `</style>`, including `<style>` and `</style>`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external3.msft.png" alt-text="La balise de style a été supprimée" lightbox="../media/beginners-css-external3.msft.png":::
       <span data-ttu-id="61816-294">La balise de style a été supprimée</span><span class="sxs-lookup"><span data-stu-id="61816-294">The style tag has been removed</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="61816-295">Accédez à `index.html` la balise et supprimez- `style="background-color: aliceblue;"` la `<nav>` .</span><span class="sxs-lookup"><span data-stu-id="61816-295">Go to `index.html` and remove `style="background-color: aliceblue;"` from the `<nav>` tag.</span></span>  <span data-ttu-id="61816-296">Vous avez supprimé toutes les feuilles CSS que vous avez précédemment ajoutées à votre site.</span><span class="sxs-lookup"><span data-stu-id="61816-296">You have now removed all of the CSS that you previously added to your site.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external4.msft.png" alt-text="Le style intraligne a été supprimé de l’élément navigation" lightbox="../media/beginners-css-external4.msft.png":::
       <span data-ttu-id="61816-298">Le style intraligne a été supprimé de l’élément navigation</span><span class="sxs-lookup"><span data-stu-id="61816-298">The inline style has been removed from the nav element</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="61816-299">Sélectionnez **nouveau fichier**.</span><span class="sxs-lookup"><span data-stu-id="61816-299">Choose **New File**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external5.msft.png" alt-text="Boîte de dialogue nouveau fichier" lightbox="../media/beginners-css-external5.msft.png":::
       <span data-ttu-id="61816-301">Boîte de dialogue nouveau fichier</span><span class="sxs-lookup"><span data-stu-id="61816-301">The new file dialog</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="61816-302">Remplacez `cool-file.js` par `style.css` et sélectionnez **Ajouter un fichier**.</span><span class="sxs-lookup"><span data-stu-id="61816-302">Replace `cool-file.js` with `style.css` and choose **Add File**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external6.msft.png" alt-text="Type style. CSS" lightbox="../media/beginners-css-external6.msft.png":::
       <span data-ttu-id="61816-304">Type</span><span class="sxs-lookup"><span data-stu-id="61816-304">Type</span></span> `style.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="61816-305">Ajoutez l’extrait de code suivant à votre `style.css` fichier.</span><span class="sxs-lookup"><span data-stu-id="61816-305">Add the following code snippet to your `style.css` file.</span></span>  
    
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
    
    :::image type="complex" source="../media/beginners-css-external7.msft.png" alt-text="Ajouter du code à style. CSS" lightbox="../media/beginners-css-external7.msft.png":::
       <span data-ttu-id="61816-307">Ajouter du code à</span><span class="sxs-lookup"><span data-stu-id="61816-307">Add code to</span></span> `style.css`  
    :::image-end:::  
    
    <span data-ttu-id="61816-308">Vérifiez que vous avez créé une feuille de style externe.</span><span class="sxs-lookup"><span data-stu-id="61816-308">Ensure that you have created an external stylesheet.</span></span> <span data-ttu-id="61816-309">Votre code HTML n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="61816-309">Your HTML is not aware that it exists.</span></span>  
    
1.  <span data-ttu-id="61816-310">Ouvrir `index.html` .</span><span class="sxs-lookup"><span data-stu-id="61816-310">Open `index.html`.</span></span>  
1.  <span data-ttu-id="61816-311">Ajoutez `<link rel="stylesheet" href="style.css">` à votre code html.</span><span class="sxs-lookup"><span data-stu-id="61816-311">Add `<link rel="stylesheet" href="style.css">` to your HTML.</span></span>  
    
    ```html
    <head>
        ...
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="style.css">
    </head>
    ```  
    
    :::image type="complex" source="../media/beginners-css-external8.msft.png" alt-text="Lien vers style. CSS" lightbox="../media/beginners-css-external8.msft.png":::
       <span data-ttu-id="61816-313">Lien vers</span><span class="sxs-lookup"><span data-stu-id="61816-313">Link to</span></span> `style.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="61816-314">Ouvrez le `contact.html` fichier et ajoutez-y le lien.</span><span class="sxs-lookup"><span data-stu-id="61816-314">Open the `contact.html` file and add the link there.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external9.msft.png" alt-text="Lien vers style. CSS dans contact.html" lightbox="../media/beginners-css-external9.msft.png":::
       <span data-ttu-id="61816-316">Lien vers `style.css` dans</span><span class="sxs-lookup"><span data-stu-id="61816-316">Link to `style.css` in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="61816-317">Accédez à l' **onglet Live**.  La page d’accueil possède désormais la même police que la dernière section et une section de navigation bleue.</span><span class="sxs-lookup"><span data-stu-id="61816-317">Go to the **live tab**.  The home page now has the same font from the last section and a blue navigation section.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external10.msft.png" alt-text="Page d’accueil" lightbox="../media/beginners-css-external10.msft.png":::
       <span data-ttu-id="61816-319">Page d’accueil</span><span class="sxs-lookup"><span data-stu-id="61816-319">The home page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="61816-320">Cliquez sur le lien de **contact** pour accéder à la page de contact.</span><span class="sxs-lookup"><span data-stu-id="61816-320">Choose the **Contact** link to go to the contact page.</span></span>  <span data-ttu-id="61816-321">La page de contact a la même mise en forme que la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="61816-321">The contact page has the same formatting as the home page.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external11.msft.png" alt-text="Page de contact" lightbox="../media/beginners-css-external11.msft.png":::
       <span data-ttu-id="61816-323">Page de contact</span><span class="sxs-lookup"><span data-stu-id="61816-323">The contact page</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="61816-324">Utiliser une infrastructure CSS</span><span class="sxs-lookup"><span data-stu-id="61816-324">Use a CSS framework</span></span>  

<span data-ttu-id="61816-325">Les **infrastructures CSS** sont des collections de styles intégrées par d’autres développeurs, qui simplifient la création de sites Web attractifs.</span><span class="sxs-lookup"><span data-stu-id="61816-325">**CSS frameworks** are collections of styles built by other developers that make it easier to create attractive web sites.</span></span>  <span data-ttu-id="61816-326">Au lieu de définir vous-même les styles, une infrastructure vous fournit une collection de styles que vous pouvez utiliser sur les éléments de la page.</span><span class="sxs-lookup"><span data-stu-id="61816-326">Instead of defining styles yourself, a framework provides you a collection of styles that you are able to use on your page elements.</span></span>  

1.  <span data-ttu-id="61816-327">Copiez le code suivant:</span><span class="sxs-lookup"><span data-stu-id="61816-327">Copy the following code:</span></span>  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  <span data-ttu-id="61816-328">Accédez à l’onglet modification et collez le code dans `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="61816-328">Go to the editing tab and paste the code into `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework1.msft.png" alt-text="Lien vers l’infrastructure dans contact.html" lightbox="../media/beginners-css-framework1.msft.png":::
       <span data-ttu-id="61816-330">Lien vers l’infrastructure dans</span><span class="sxs-lookup"><span data-stu-id="61816-330">Link to the framework in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="61816-331">Ouvrez le `index.html` fichier et ajoutez-y le code.</span><span class="sxs-lookup"><span data-stu-id="61816-331">Open the `index.html` file and add the code there.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework2.msft.png" alt-text="Lien vers l’infrastructure dans index.html" lightbox="../media/beginners-css-framework2.msft.png":::
       <span data-ttu-id="61816-333">Lien vers l’infrastructure dans</span><span class="sxs-lookup"><span data-stu-id="61816-333">Link to the framework in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="61816-334">Revenez à l’onglet Live pour afficher vos modifications.</span><span class="sxs-lookup"><span data-stu-id="61816-334">Go back to the live tab to view your changes.</span></span>  <span data-ttu-id="61816-335">Même si la couleur d’arrière-plan de l' `<nav>` élément et la police des `<li>` `<a>` éléments et sont identiques, la police des autres éléments a changé.</span><span class="sxs-lookup"><span data-stu-id="61816-335">While the background color of the `<nav>` element and the font of the `<li>` and `<a>` elements are the same, the font of the other elements has changed.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework3.msft.png" alt-text="Une partie de la police de la page d’accueil a changé en raison de l’infrastructure." lightbox="../media/beginners-css-framework3.msft.png":::
       <span data-ttu-id="61816-337">Une partie de la police de la page d’accueil a changé en raison de l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="61816-337">Some of the font on the home page changed because of the framework</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="61816-338">Utiliser une classe</span><span class="sxs-lookup"><span data-stu-id="61816-338">Use a class</span></span>  

<span data-ttu-id="61816-339">Dans la dernière section, vous avez ajouté des données d’amorçage dans vos pages Web, ce qui a modifié les polices de certains éléments de votre site.</span><span class="sxs-lookup"><span data-stu-id="61816-339">In the last section, you added Bootstrap to your web pages, which changed the fonts of some of the elements on your site.</span></span>  <span data-ttu-id="61816-340">Les infrastructures CSS vous permettent d’apporter des modifications importantes à votre page avec peu de code.</span><span class="sxs-lookup"><span data-stu-id="61816-340">CSS frameworks help you make major changes to your page with very little code.</span></span>  <span data-ttu-id="61816-341">Effectuez les opérations suivantes pour modifier votre en-tête.</span><span class="sxs-lookup"><span data-stu-id="61816-341">Complete the following actions to change your header.</span></span>  

1.  <span data-ttu-id="61816-342">Copiez l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="61816-342">Copy the following code snippet.</span></span>  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  <span data-ttu-id="61816-343">Ajoutez l’extrait de code précédent à votre `<header>` balise dans `index.html` .</span><span class="sxs-lookup"><span data-stu-id="61816-343">Add the previous code snippet to your `<header>` tag in `index.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron1.msft.png" alt-text="Ajouter des classes dans index.html" lightbox="../media/beginners-css-jumbotron1.msft.png":::
       <span data-ttu-id="61816-345">Ajouter des classes dans</span><span class="sxs-lookup"><span data-stu-id="61816-345">Add classes in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="61816-346">Ajoutez le code à votre `<header>` balise dans `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="61816-346">Add the code to your `<header>` tag in `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron2.msft.png" alt-text="Ajouter des classes dans contact.html" lightbox="../media/beginners-css-jumbotron2.msft.png":::
       <span data-ttu-id="61816-348">Ajouter des classes dans</span><span class="sxs-lookup"><span data-stu-id="61816-348">Add classes in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="61816-349">Affichez vos modifications sous l’onglet Live.  Il y a une grande zone grise dans l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="61816-349">View your changes in the live tab.  There is a big, grey box around your header.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron3.msft.png" alt-text="L’en-tête est désormais entouré d’un cadre gris." lightbox="../media/beginners-css-jumbotron3.msft.png":::
       <span data-ttu-id="61816-351">L’en-tête est désormais entouré d’un cadre gris.</span><span class="sxs-lookup"><span data-stu-id="61816-351">The header now has a big, grey box around it</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="61816-352">Comprendre les classes</span><span class="sxs-lookup"><span data-stu-id="61816-352">Understand classes</span></span>  

<span data-ttu-id="61816-353">Les classes vous permettent d’affecter des collections de styles à des éléments arbitraires.</span><span class="sxs-lookup"><span data-stu-id="61816-353">Classes let you assign collections of styles to arbitrary elements.</span></span>  <span data-ttu-id="61816-354">Utilisez l’extrait de code suivant pour appliquer plusieurs styles à l' `<header>` élément après l’avoir défini `class` `jumbotron` .</span><span class="sxs-lookup"><span data-stu-id="61816-354">Use the following code snippet to apply several styles to the `<header>` element after you set the `class` attribute to `jumbotron`.</span></span>  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

<span data-ttu-id="61816-355">L’un des avantages d’une classe réside dans le fait qu’il vous permet d’appliquer des styles à tous les éléments souhaités.</span><span class="sxs-lookup"><span data-stu-id="61816-355">One advantage of a class is that it lets you apply styles to whatever elements you want.</span></span>  <span data-ttu-id="61816-356">Par exemple, supposons que vous vouliez définir la couleur d’arrière-plan de certains `<p>` éléments sur pourpre, mais pas sur tous les `<p>` éléments.</span><span class="sxs-lookup"><span data-stu-id="61816-356">For example, suppose you want to set the background color of some `<p>` elements to purple, but not all `<p>` elements.</span></span>  <span data-ttu-id="61816-357">Utilisez l’extrait de code suivant pour définir le style d’une classe.</span><span class="sxs-lookup"><span data-stu-id="61816-357">Use the following code snippet to define the style in a class.</span></span>  

```css
.custom-background {
  background-color: purple;
}
```  

<span data-ttu-id="61816-358">Ensuite, appliquez la classe uniquement aux `<p>` éléments auxquels vous voulez appliquer un style.</span><span class="sxs-lookup"><span data-stu-id="61816-358">Next, apply the class to only the `<p>` elements that you want to style.</span></span>  

```html
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
```  

### <span data-ttu-id="61816-359">Aligner des éléments</span><span class="sxs-lookup"><span data-stu-id="61816-359">Align elements</span></span>  

<span data-ttu-id="61816-360">Procédez comme suit pour amorcer et fournir des classes permettant d’aligner des éléments.</span><span class="sxs-lookup"><span data-stu-id="61816-360">Complete the following actions to bootstrap and provide classes for aligning elements.</span></span>  

1.  <span data-ttu-id="61816-361">Revenez à l’onglet Éditeur, puis ouvrez `index.html` .</span><span class="sxs-lookup"><span data-stu-id="61816-361">Go back to the editor tab and open `index.html`.</span></span>  
1.  <span data-ttu-id="61816-362">Ajoutez `class="container-fluid"` à votre `<body>` indicateur.</span><span class="sxs-lookup"><span data-stu-id="61816-362">Add `class="container-fluid"` to your `<body>` tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align1.msft.png" alt-text="Ajouter la classe Container-fluidiques" lightbox="../media/beginners-css-align1.msft.png":::
       <span data-ttu-id="61816-364">Ajouter la `container-fluid` classe</span><span class="sxs-lookup"><span data-stu-id="61816-364">Add the `container-fluid` class</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="61816-365">Renvoyez `<nav>` vos `<main>` éléments et `<div class="row">` .</span><span class="sxs-lookup"><span data-stu-id="61816-365">Wrap your `<nav>` and `<main>` elements in `<div class="row">`.</span></span>  <span data-ttu-id="61816-366">Assurez-vous d’entrer `</div>` après pour `</main>` fermer correctement la nouvelle balise.</span><span class="sxs-lookup"><span data-stu-id="61816-366">Make sure to put `</div>` after `</main>` in order to properly close the new tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align2.msft.png" alt-text="Ajouter une ligne" lightbox="../media/beginners-css-align2.msft.png":::
       <span data-ttu-id="61816-368">Ajouter une ligne</span><span class="sxs-lookup"><span data-stu-id="61816-368">Add a row</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="61816-369">Ajoutez `class="col-3"` votre `<nav>` indicateur et `class="col-9"` votre `<main>` indicateur.</span><span class="sxs-lookup"><span data-stu-id="61816-369">Add `class="col-3"` to your `<nav>` tag and `class="col-9"` to your `<main>` tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align3.msft.png" alt-text="Ajouter les classes col-3 et col-9" lightbox="../media/beginners-css-align3.msft.png":::
       <span data-ttu-id="61816-371">Ajouter les `col-3` `col-9` classes et</span><span class="sxs-lookup"><span data-stu-id="61816-371">Add the `col-3` and `col-9` classes</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="61816-372">Affichez vos modifications sous l’onglet Live.</span><span class="sxs-lookup"><span data-stu-id="61816-372">View your changes in the live tab.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align4.msft.png" alt-text="Le contenu de navigation est désormais à gauche du contenu principal" lightbox="../media/beginners-css-align4.msft.png":::
       <span data-ttu-id="61816-374">Le contenu de navigation est désormais à gauche du contenu principal</span><span class="sxs-lookup"><span data-stu-id="61816-374">The nav content is now to the left of the main content</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="61816-375">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="61816-375">Next steps</span></span>  

<span data-ttu-id="61816-376">Félicitations, vous avez réussi.</span><span class="sxs-lookup"><span data-stu-id="61816-376">Congratulations, you are done.</span></span>  

*   <span data-ttu-id="61816-377">La meilleure façon d’optimiser le développement Web consiste à créer des sites supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="61816-377">The best way to get better at web development is to build more sites.</span></span>  <span data-ttu-id="61816-378">Ne vous inquiétez pas de casser votre contenu.</span><span class="sxs-lookup"><span data-stu-id="61816-378">Do not worry about breaking stuff.</span></span>  <span data-ttu-id="61816-379">Amusez-vous et apprenez autant que possible.</span><span class="sxs-lookup"><span data-stu-id="61816-379">Just have fun and learn as much as possible along the way.</span></span>  
*   <span data-ttu-id="61816-380">Pour en savoir plus sur le style de pages Web, voir [Présentation des feuilles CSS][MDNCssFirstSteps].</span><span class="sxs-lookup"><span data-stu-id="61816-380">To learn more about styling web pages, see [Introduction to CSS][MDNCssFirstSteps].</span></span>  
*   <span data-ttu-id="61816-381">Pour en savoir plus sur l’utilisation de DevTools pour tester la feuille de style en cascade d’une page, voir [découvrir comment afficher et modifier des feuilles CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="61816-381">To learn more about how to use DevTools to experiment with the CSS of a page, see [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

<!--- image links --->  

[ImageNewStyleRuleIcon]: ../media/new-style-rule-icon.msft.png  

<!--- links  --->  

[DevtoolsBeginnersHtml]: ./html.md "DevTools pour les débutants: prenez en main HTML et le DOM | Documents Microsoft"  
[DevtoolsCssIndex]: ../css/index.md "Découvrir comment afficher et modifier des feuilles CSS | Documents Microsoft"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html-cuisin-Amphibian | Problème"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "Premiers pas dans la feuille de style CSS | MDN"  

> [!NOTE]
> <span data-ttu-id="61816-387">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="61816-387">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="61816-388">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/beginners/css) et est créée par [Katherine Jackson][KatherineJackson] \ (Technical Writer Intern, chrome devtools \).</span><span class="sxs-lookup"><span data-stu-id="61816-388">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/css) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="61816-390">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="61816-390">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
