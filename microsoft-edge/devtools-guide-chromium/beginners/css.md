---
title: DevTools pour les débutants
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 0064f0427b6bd5689e888cccfe2c650492898bb2
ms.sourcegitcommit: 8bfa239274e7a4856b961b9cf163b08d96463c10
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2020
ms.locfileid: "10581593"
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

# <span data-ttu-id="c3eff-103">DevTools pour les débutants: prendre en main CSS</span><span class="sxs-lookup"><span data-stu-id="c3eff-103">DevTools For Beginners: Get Started with CSS</span></span>   

<span data-ttu-id="c3eff-104">Dans ce didacticiel, vous allez apprendre à utiliser les feuilles CSS pour appliquer un style à une page Web.</span><span class="sxs-lookup"><span data-stu-id="c3eff-104">In this tutorial, you learn how to use CSS to style a web page.</span></span>  <span data-ttu-id="c3eff-105">Vous pouvez également apprendre à utiliser Microsoft Edge DevTools pour tester les changements CSS.</span><span class="sxs-lookup"><span data-stu-id="c3eff-105">You also learn how to use Microsoft Edge DevTools to experiment with CSS changes.</span></span>  

<span data-ttu-id="c3eff-106">Voici le deuxième didacticiel d’une série de didacticiels qui vous explique les notions de base du développement Web et de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="c3eff-106">This is the second tutorial in a series of tutorials that teaches you the basics of web development and Microsoft Edge DevTools.</span></span>  <span data-ttu-id="c3eff-107">Profitez d’une expérience pratique en créant votre propre site Web.</span><span class="sxs-lookup"><span data-stu-id="c3eff-107">You gain hands-on experience by actually building your own website.</span></span>  <span data-ttu-id="c3eff-108">Il n’est pas nécessaire de terminer le premier didacticiel avant de procéder.</span><span class="sxs-lookup"><span data-stu-id="c3eff-108">You don't have to complete the first tutorial before doing this one.</span></span>  <span data-ttu-id="c3eff-109">Vous pouvez commencer ici.</span><span class="sxs-lookup"><span data-stu-id="c3eff-109">You can start here.</span></span>  <span data-ttu-id="c3eff-110">La [configuration de votre code](#set-up-your-code) vous montre comment procéder à la configuration.</span><span class="sxs-lookup"><span data-stu-id="c3eff-110">[Set up your code](#set-up-your-code) shows you how to get set up.</span></span>  

> [!NOTE]
> <span data-ttu-id="c3eff-111">Ce didacticiel est conçu pour les débutants et est axé sur les notions **fondamentales du développement Web** et des notions de base de l’utilisation de devtools pour tester les feuilles CSS.</span><span class="sxs-lookup"><span data-stu-id="c3eff-111">This tutorial is designed for absolute beginners and focuses on both the **fundamentals of web development** and the basics of using DevTools to experiment with CSS.</span></span>  <span data-ttu-id="c3eff-112">Si vous avez besoin d’un didacticiel destiné uniquement à DevTools, voir [découvrir comment afficher et modifier des feuilles CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="c3eff-112">If you want a tutorial that only focuses on DevTools, see [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

<span data-ttu-id="c3eff-113">Votre site se présente actuellement comme suit:</span><span class="sxs-lookup"><span data-stu-id="c3eff-113">Currently your site looks like this:</span></span>  

> ##### <span data-ttu-id="c3eff-114">Figure1</span><span class="sxs-lookup"><span data-stu-id="c3eff-114">Figure 1</span></span>  
> <span data-ttu-id="c3eff-115">Aspect de votre site</span><span class="sxs-lookup"><span data-stu-id="c3eff-115">What your site currently looks like</span></span>  
> ![Aspect de votre site][ImageCssIntro1]  

<span data-ttu-id="c3eff-117">À la fin du didacticiel, il se présente comme suit:</span><span class="sxs-lookup"><span data-stu-id="c3eff-117">After completing the tutorial, it will look like this:</span></span>  

> ##### <span data-ttu-id="c3eff-118">Figure 2</span><span class="sxs-lookup"><span data-stu-id="c3eff-118">Figure 2</span></span>  
> <span data-ttu-id="c3eff-119">Aspect de votre site à la fin du didacticiel</span><span class="sxs-lookup"><span data-stu-id="c3eff-119">What your site will look like at the end of the tutorial</span></span>  
> ![Aspect de votre site à la fin du didacticiel][ImageCssIntro2]  

## <span data-ttu-id="c3eff-121">Définis</span><span class="sxs-lookup"><span data-stu-id="c3eff-121">Goals</span></span>   

<span data-ttu-id="c3eff-122">À la fin de ce didacticiel, vous allez comprendre les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="c3eff-122">By the end of this tutorial, you will understand:</span></span>  

*   <span data-ttu-id="c3eff-123">Comment utiliser les feuilles CSS pour appliquer un style à une page Web.</span><span class="sxs-lookup"><span data-stu-id="c3eff-123">How to use CSS to style a web page.</span></span>  
*   <span data-ttu-id="c3eff-124">Comment utiliser Microsoft Edge DevTools pour tester les feuilles CSS.</span><span class="sxs-lookup"><span data-stu-id="c3eff-124">How to use Microsoft Edge DevTools to experiment with CSS.</span></span>  
*   <span data-ttu-id="c3eff-125">Différence entre les infrastructures CSS et CSS.</span><span class="sxs-lookup"><span data-stu-id="c3eff-125">The difference between CSS and CSS frameworks.</span></span>  

<span data-ttu-id="c3eff-126">Vous disposez également d’un site Web réel.</span><span class="sxs-lookup"><span data-stu-id="c3eff-126">You'll also have a real website!</span></span>  

## <span data-ttu-id="c3eff-127">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="c3eff-127">Prerequisites</span></span>   

<span data-ttu-id="c3eff-128">Avant de suivre ce didacticiel, remplissez les conditions préalables suivantes:</span><span class="sxs-lookup"><span data-stu-id="c3eff-128">Before attempting this tutorial, complete the following prerequisites:</span></span>  

*   <span data-ttu-id="c3eff-129">Pour plus d’informations, [consultez prise en main de HTML et du DOM][DevToolsBeginnersHtml] ou assurez-vous que vous comprenez bien html et le DOM semblable à ce qui est enseigné dans ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="c3eff-129">Complete [Get Started with HTML and the DOM][DevToolsBeginnersHtml] or make sure that you have an understanding of HTML and the DOM similar to what's taught in that tutorial.</span></span>  
*   <span data-ttu-id="c3eff-130">Téléchargez le navigateur Web [Microsoft Edge][MicrosoftEdgeInsider] .</span><span class="sxs-lookup"><span data-stu-id="c3eff-130">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="c3eff-131">Ce didacticiel utilise un ensemble d’outils de développement Web, appelés Microsoft Edge DevTools, qui sont intégrés à Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c3eff-131">This tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <span data-ttu-id="c3eff-132">Configurer votre code</span><span class="sxs-lookup"><span data-stu-id="c3eff-132">Set up your code</span></span>   

<span data-ttu-id="c3eff-133">Pour commencer à créer votre site, vous devez configurer votre code:</span><span class="sxs-lookup"><span data-stu-id="c3eff-133">In order to start creating your site, you need to set up your code:</span></span>  

1.  **<span data-ttu-id="c3eff-134">Si vous avez déjà effectué le premier didacticiel de cette série, ignorez cette section.</span><span class="sxs-lookup"><span data-stu-id="c3eff-134">If you have already completed the first tutorial in this series, skip this section!</span></span>  <span data-ttu-id="c3eff-135">Continuez à utiliser votre code à partir du dernier didacticiel, de [la mise en route de HTML et du DOM][DevToolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="c3eff-135">Continue using your code from the last tutorial, [Get Started with HTML and the DOM][DevToolsBeginnersHtml].</span></span>**  
1.  <span data-ttu-id="c3eff-136">Ouvrez le [code source][GlitchCookedAmphibianIndex].</span><span class="sxs-lookup"><span data-stu-id="c3eff-136">Open the [source code][GlitchCookedAmphibianIndex].</span></span>  <span data-ttu-id="c3eff-137">Cet onglet de votre navigateur sera appelé **onglet édition**.</span><span class="sxs-lookup"><span data-stu-id="c3eff-137">This tab of your browser will be called the **editing tab**.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-138">Figure3</span><span class="sxs-lookup"><span data-stu-id="c3eff-138">Figure 3</span></span>  
    > <span data-ttu-id="c3eff-139">Onglet édition</span><span class="sxs-lookup"><span data-stu-id="c3eff-139">The editing tab</span></span>  
    > ![Onglet édition][ImageCssSetup1]  
    
1.  <span data-ttu-id="c3eff-141">Cliquez sur **cuit-Amphibian**.</span><span class="sxs-lookup"><span data-stu-id="c3eff-141">Click **cooked-amphibian**.</span></span>  <span data-ttu-id="c3eff-142">Un menu s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="c3eff-142">A menu pops up.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-143">Figure 4</span><span class="sxs-lookup"><span data-stu-id="c3eff-143">Figure 4</span></span>  
    > <span data-ttu-id="c3eff-144">Menu options de Project</span><span class="sxs-lookup"><span data-stu-id="c3eff-144">The Project Options menu</span></span>  
    > ![Menu options de Project][ImageCssSetup2]  

1.  <span data-ttu-id="c3eff-146">Cliquez sur **Remix Project**.</span><span class="sxs-lookup"><span data-stu-id="c3eff-146">Click **Remix Project**.</span></span>  <span data-ttu-id="c3eff-147">Le problème crée une copie du projet que vous pouvez modifier.</span><span class="sxs-lookup"><span data-stu-id="c3eff-147">Glitch creates a copy of the project that you can edit.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="c3eff-148">Le problème génère un nom aléatoire pour le nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="c3eff-148">Glitch generates a random name for the new project.</span></span>  
    
1.  <span data-ttu-id="c3eff-149">Cliquez sur **Afficher** et sélectionnez **dans une nouvelle fenêtre**.</span><span class="sxs-lookup"><span data-stu-id="c3eff-149">Click **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="c3eff-150">Un autre onglet s’ouvre en mode en direct de votre site.</span><span class="sxs-lookup"><span data-stu-id="c3eff-150">Another tab opens with a live view of your site.</span></span>  <span data-ttu-id="c3eff-151">L' **onglet Live**de votre navigateur s’appelle.</span><span class="sxs-lookup"><span data-stu-id="c3eff-151">This tab of your browser will be called the **live tab**.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-152">Figure 5</span><span class="sxs-lookup"><span data-stu-id="c3eff-152">Figure 5</span></span>  
    > <span data-ttu-id="c3eff-153">Onglet Live</span><span class="sxs-lookup"><span data-stu-id="c3eff-153">The live tab</span></span>  
    > ![Onglet Live][ImageCssSetup3]  

## <span data-ttu-id="c3eff-155">Comprendre CSS</span><span class="sxs-lookup"><span data-stu-id="c3eff-155">Understand CSS</span></span>   

<span data-ttu-id="c3eff-156">**CSS** est un langage informatique qui détermine la disposition et le style des pages Web.</span><span class="sxs-lookup"><span data-stu-id="c3eff-156">**CSS** is a computer language that determines the layout and styling of web pages.</span></span>  <span data-ttu-id="c3eff-157">Par exemple, voici un paragraphe avec une bordure:</span><span class="sxs-lookup"><span data-stu-id="c3eff-157">For example, here is a paragraph with a border:</span></span>  

> ##### <span data-ttu-id="c3eff-158">Figure 6</span><span class="sxs-lookup"><span data-stu-id="c3eff-158">Figure 6</span></span>  
> <span data-ttu-id="c3eff-159">Style avec CSS</span><span class="sxs-lookup"><span data-stu-id="c3eff-159">This has been styled with CSS</span></span>  
> ![Style avec CSS][ImageCssStyled]  

<span data-ttu-id="c3eff-161">Voici le code HTML et CSS utilisé pour créer ce paragraphe:</span><span class="sxs-lookup"><span data-stu-id="c3eff-161">Here is the HTML and CSS code used to create that paragraph:</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` <span data-ttu-id="c3eff-162">C’est probablement une nouveauté.</span><span class="sxs-lookup"><span data-stu-id="c3eff-162">probably looks new to you.</span></span>  <span data-ttu-id="c3eff-163">Le reste devrait vous être familier.</span><span class="sxs-lookup"><span data-stu-id="c3eff-163">The rest should look familiar.</span></span>  <span data-ttu-id="c3eff-164">Si ce n’est pas le cas, terminez- [le en utilisant le code HTML et le DOM][DevToolsBeginnersHtml] avant d’essayer ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="c3eff-164">If not, complete [Get Started with HTML and the DOM][DevToolsBeginnersHtml] before attempting this tutorial.</span></span>  

## <span data-ttu-id="c3eff-165">Ajouter des styles intralignes</span><span class="sxs-lookup"><span data-stu-id="c3eff-165">Add inline styles</span></span>   

<span data-ttu-id="c3eff-166">Utilisez des **styles intralignes** lorsque vous souhaitez appliquer des styles à un seul élément.</span><span class="sxs-lookup"><span data-stu-id="c3eff-166">Use **inline styles** when you want to apply styles to a single element.</span></span>  <span data-ttu-id="c3eff-167">Essayez-le maintenant:</span><span class="sxs-lookup"><span data-stu-id="c3eff-167">Try it now:</span></span>  

1.  <span data-ttu-id="c3eff-168">Revenez à l’onglet modification et ouvrez `index.html` .</span><span class="sxs-lookup"><span data-stu-id="c3eff-168">Go back to the editing tab and open `index.html`.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-169">Figure 7</span><span class="sxs-lookup"><span data-stu-id="c3eff-169">Figure 7</span></span>  
    > `index.html`  
    > ![index.html][ImageCssInline1]  

1.  <span data-ttu-id="c3eff-171">Ajoutez `style="background-color: aliceblue;"` à votre `<nav>` .</span><span class="sxs-lookup"><span data-stu-id="c3eff-171">Add `style="background-color: aliceblue;"` to your `<nav>`.</span></span>  <span data-ttu-id="c3eff-172">Dans le bloc de code ci-dessous, la quatrième ligne de code est celle que vous devez modifier.</span><span class="sxs-lookup"><span data-stu-id="c3eff-172">In the code block below, the fourth line of code is the one you need to change.</span></span>  <span data-ttu-id="c3eff-173">Le reste est là pour vous permettre de vérifier que vous insérez le nouveau code au bon endroit.</span><span class="sxs-lookup"><span data-stu-id="c3eff-173">The rest is just there so you can be sure that you're putting the new code in the right place.</span></span>  
    
    ```html
    ...
        ...
            <header>
                <p>Welcome to my site!</p>
            </header>
            <nav style="background-color: aliceblue;">
                <ul>
                    <li><a href="/">Home</a></li>
                    ...
                ...
            ...
        ...
    ...
    ```  

1.  <span data-ttu-id="c3eff-174">Accédez à l' **onglet Live** pour afficher les modifications.</span><span class="sxs-lookup"><span data-stu-id="c3eff-174">Go to the **live tab** to see the changes!</span></span>  <span data-ttu-id="c3eff-175">L’arrière-plan de la `<nav>` section est désormais bleu.</span><span class="sxs-lookup"><span data-stu-id="c3eff-175">The background of the `<nav>` section is now blue.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-176">Figure8</span><span class="sxs-lookup"><span data-stu-id="c3eff-176">Figure 8</span></span>  
    > <span data-ttu-id="c3eff-177">La couleur d’arrière-plan derrière les liens accueil et contact est désormais bleue</span><span class="sxs-lookup"><span data-stu-id="c3eff-177">The background color behind the Home and Contact links is now blue</span></span>  
    > ![La couleur d’arrière-plan derrière les liens accueil et contact est désormais bleue][ImageCssInline2]  

## <span data-ttu-id="c3eff-179">Réutiliser les styles sur une seule page à l’aide de feuilles de style internes</span><span class="sxs-lookup"><span data-stu-id="c3eff-179">Re-use styles on a single page with internal stylesheets</span></span>   

<span data-ttu-id="c3eff-180">Auparavant, vous avez vu un style intraligne qui appliquait un style à une `<p>` balise unique comme suit:</span><span class="sxs-lookup"><span data-stu-id="c3eff-180">Earlier, you saw an inline style that applied a style to a single `<p>` tag like this:</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

<span data-ttu-id="c3eff-181">Que faire si vous souhaitez que tous les `<p>` éléments d’une page Web soient stylisés de la même manière?</span><span class="sxs-lookup"><span data-stu-id="c3eff-181">What if you wanted all of the `<p>` elements on your webpage to be styled the same way?</span></span>  <span data-ttu-id="c3eff-182">Vous devez copier et coller le code dans chaque `<p>` balise unique de votre site.</span><span class="sxs-lookup"><span data-stu-id="c3eff-182">You'd have to copy and paste the code into every single `<p>` tag on your site.</span></span>  <span data-ttu-id="c3eff-183">C’est un peu de temps et d’efforts.</span><span class="sxs-lookup"><span data-stu-id="c3eff-183">That's a lot of time and effort.</span></span>  <span data-ttu-id="c3eff-184">Et si vous avez besoin d’effectuer une modification, vous devrez à nouveau modifier chaque balise.</span><span class="sxs-lookup"><span data-stu-id="c3eff-184">And, if you needed to make an edit, you'd have to change every tag again.</span></span>  <span data-ttu-id="c3eff-185">Les **feuilles de style internes** vous permettent d’écrire votre CSS une seule fois pour qu’elle s’applique à plusieurs éléments.</span><span class="sxs-lookup"><span data-stu-id="c3eff-185">**Internal stylesheets** allow you to write your CSS once so that it applies to multiple elements.</span></span>  <span data-ttu-id="c3eff-186">Essayez-le maintenant:</span><span class="sxs-lookup"><span data-stu-id="c3eff-186">Try it now:</span></span>  

1.  <span data-ttu-id="c3eff-187">Dans l’onglet Live, cliquez sur **contact** pour accéder à la page de contact.</span><span class="sxs-lookup"><span data-stu-id="c3eff-187">In the live tab, click **Contact** to go to the contact page.</span></span>  <span data-ttu-id="c3eff-188">Notez la police **Accueil** et **contact**.</span><span class="sxs-lookup"><span data-stu-id="c3eff-188">Notice the font of **Home** and **Contact**.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-189">Figure9</span><span class="sxs-lookup"><span data-stu-id="c3eff-189">Figure 9</span></span>  
    > <span data-ttu-id="c3eff-190">Page de contact</span><span class="sxs-lookup"><span data-stu-id="c3eff-190">The Contact page</span></span>  
    > ![Page de contact][ImageCssInternal1]  

1.  <span data-ttu-id="c3eff-192">Dans l' **onglet Éditeur**, accédez à `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="c3eff-192">In the **editor tab**, go to `contact.html`.</span></span>  
1.  <span data-ttu-id="c3eff-193">Ajoutez le code suivant à `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="c3eff-193">Add the following code to `contact.html`.</span></span>  <span data-ttu-id="c3eff-194">Rappelez-vous que les lignes commençant par `<style>` et se terminant par `</style>` sont celles que vous devez ajouter.</span><span class="sxs-lookup"><span data-stu-id="c3eff-194">Remember, the lines starting with `<style>` and ending with `</style>` are what you need to add.</span></span>  <span data-ttu-id="c3eff-195">L’autre code est là pour vous indiquer où placer le nouveau code.</span><span class="sxs-lookup"><span data-stu-id="c3eff-195">The other code is just there so you know where to put the new code.</span></span>  
    
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
    
1.  <span data-ttu-id="c3eff-196">Revenir à l' **onglet Live**.</span><span class="sxs-lookup"><span data-stu-id="c3eff-196">Go back to the **live tab**.</span></span>  
1.  <span data-ttu-id="c3eff-197">Cliquez sur le **contact** pour revenir à la page de contact.</span><span class="sxs-lookup"><span data-stu-id="c3eff-197">Click **Contact** to go back to the contact page.</span></span>  <span data-ttu-id="c3eff-198">La police **Accueil** et **contact** a changé.</span><span class="sxs-lookup"><span data-stu-id="c3eff-198">The font of **Home** and **Contact** has changed.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-199">Figure10</span><span class="sxs-lookup"><span data-stu-id="c3eff-199">Figure 10</span></span>  
    > <span data-ttu-id="c3eff-200">La police des liens accueil et contact a changé</span><span class="sxs-lookup"><span data-stu-id="c3eff-200">The font of the Home and Contact links has changed</span></span>  
    > ![La police des liens accueil et contact a changé][ImageCssInternal2]  
    
### <span data-ttu-id="c3eff-202">Comprendre les feuilles de style internes</span><span class="sxs-lookup"><span data-stu-id="c3eff-202">Understand internal stylesheets</span></span>   

<span data-ttu-id="c3eff-203">Les feuilles de style internes s’appliquent aux styles à l’aide de **sélecteurs**.</span><span class="sxs-lookup"><span data-stu-id="c3eff-203">Internal stylesheets apply styles using **selectors**.</span></span>  <span data-ttu-id="c3eff-204">Les sélecteurs sont des modèles qui peuvent être appliqués à un ou plusieurs éléments HTML.</span><span class="sxs-lookup"><span data-stu-id="c3eff-204">Selectors are patterns that may apply to one or more HTML elements.</span></span>  <span data-ttu-id="c3eff-205">Par exemple, dans le code précédent:</span><span class="sxs-lookup"><span data-stu-id="c3eff-205">For example, in the previous code:</span></span>  

```html
...
    ...
        ...
        <style>
            li a {
              font-family: 'Courier New', Courier, Serif;
            }
        </style>
        ...
    ...
...
```  

`li a` <span data-ttu-id="c3eff-206">est un sélecteur qui se traduit par «any contenant `<li>` `<a>` ».</span><span class="sxs-lookup"><span data-stu-id="c3eff-206">is a selector that translates to "any `<li>` that contains an `<a>`".</span></span>  <span data-ttu-id="c3eff-207">Le navigateur modifie la police des liens **Accueil** et **contact** , car ils correspondent à ce modèle.</span><span class="sxs-lookup"><span data-stu-id="c3eff-207">The browser changes the font of the **Home** and **Contact** links because they match this pattern.</span></span>  

```html
...
    ...
        ...
            ...
                <li><a href="/">Home</a></li>
                <li><a href="/contact.html">Contact</a></li>
                ...
            ...
        ...
    ...
...
```  

`font-family: 'Courier New', Courier, serif` <span data-ttu-id="c3eff-208">est une **déclaration**.</span><span class="sxs-lookup"><span data-stu-id="c3eff-208">is a **declaration**.</span></span>  <span data-ttu-id="c3eff-209">Une déclaration est constituée de deux parties: une **propriété** et une **valeur**.</span><span class="sxs-lookup"><span data-stu-id="c3eff-209">A declaration is made of two parts: a **property** and a **value**.</span></span>  `font-family` <span data-ttu-id="c3eff-210">est la propriété et `'Courier New', Courier, serif` est la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="c3eff-210">is the property, and `'Courier New', Courier, serif` is the value of that property.</span></span>  <span data-ttu-id="c3eff-211">La propriété décrit une méthode générale permettant de modifier le style de l’élément, et la valeur indique exactement le changement.</span><span class="sxs-lookup"><span data-stu-id="c3eff-211">The property describes a general way that you can change the element's style, and the value says how exactly it should change.</span></span>  <span data-ttu-id="c3eff-212">Par exemple, `font-family: 'Courier New', Courier, serif` donne au navigateur cette instruction: "définissez la police des éléments qui correspondent au modèle `li a` `'Courier New'` .</span><span class="sxs-lookup"><span data-stu-id="c3eff-212">For example, `font-family: 'Courier New', Courier, serif` gives the browser this instruction:  "Set the font of elements that match the pattern `li a` to `'Courier New'`.</span></span>  <span data-ttu-id="c3eff-213">Si cette police n’est pas disponible, utilisez `Courier` .</span><span class="sxs-lookup"><span data-stu-id="c3eff-213">If that font isn't available, use `Courier`.</span></span>  <span data-ttu-id="c3eff-214">Si ce n’est pas le cas, utilisez `serif` .»</span><span class="sxs-lookup"><span data-stu-id="c3eff-214">If that isn't available, use `serif`."</span></span>  

### <span data-ttu-id="c3eff-215">Ajouter plusieurs sélecteurs à un groupe de règles</span><span class="sxs-lookup"><span data-stu-id="c3eff-215">Add multiple selectors to a ruleset</span></span>   

<span data-ttu-id="c3eff-216">Un bloc de code CSS tel que celui qui apparaît ci-dessous est appelé **RuleSet**.</span><span class="sxs-lookup"><span data-stu-id="c3eff-216">A block of CSS code like what you see below is called a **ruleset**.</span></span>  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

<span data-ttu-id="c3eff-217">Utilisez des points-virgules pour ajouter plusieurs sélecteurs à un RuleSet.</span><span class="sxs-lookup"><span data-stu-id="c3eff-217">Use commas to add multiple selectors to a ruleset.</span></span>  <span data-ttu-id="c3eff-218">Essayez-le maintenant:</span><span class="sxs-lookup"><span data-stu-id="c3eff-218">Try it now:</span></span>  

1.  <span data-ttu-id="c3eff-219">Dans l' **onglet Éditeur**, ouvrez `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="c3eff-219">In the **editor tab**, open `contact.html`.</span></span>  
1.  <span data-ttu-id="c3eff-220">Après `li a` type `, h1` .</span><span class="sxs-lookup"><span data-stu-id="c3eff-220">After `li a` type `, h1`.</span></span>  

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

    <span data-ttu-id="c3eff-221">Cela indique au navigateur d' `<h1>` avoir des éléments style de la même manière qu’il s’agit d’éléments qui correspondent au modèle `li a` .</span><span class="sxs-lookup"><span data-stu-id="c3eff-221">This tells the browser to style `<h1>` elements the same way that it styles elements that match the pattern `li a`.</span></span>  
    
1.  <span data-ttu-id="c3eff-222">Accédez à l' **onglet Live**.</span><span class="sxs-lookup"><span data-stu-id="c3eff-222">Go to the **live tab**.</span></span>  
1.  <span data-ttu-id="c3eff-223">Cliquez sur le lien de **contact** pour revenir à la page de contact.</span><span class="sxs-lookup"><span data-stu-id="c3eff-223">Click the **Contact** link to go back to the contact page.</span></span>  <span data-ttu-id="c3eff-224">Maintenant, **Contactez-moi!**</span><span class="sxs-lookup"><span data-stu-id="c3eff-224">Now, **Contact Me!**</span></span> <span data-ttu-id="c3eff-225">a la même police que les liens de navigation.</span><span class="sxs-lookup"><span data-stu-id="c3eff-225">has the same font as the navigation links.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-226">Figure11</span><span class="sxs-lookup"><span data-stu-id="c3eff-226">Figure 11</span></span>  
    > <span data-ttu-id="c3eff-227">Le texte’contactez-moi! '</span><span class="sxs-lookup"><span data-stu-id="c3eff-227">The text 'Contact Me!'</span></span> <span data-ttu-id="c3eff-228">possède désormais la même police que les liens accueil et contact</span><span class="sxs-lookup"><span data-stu-id="c3eff-228">now has the same font as the Home and Contact links</span></span>  
    > ![Le texte me contacter.][ImageCssMultiple1]  

## <span data-ttu-id="c3eff-231">Expérimentez avec DevTools</span><span class="sxs-lookup"><span data-stu-id="c3eff-231">Experiment with DevTools</span></span>   

<span data-ttu-id="c3eff-232">À mesure que vous poursuivez le développement Web principal, vous constaterez que les feuilles CSS peuvent être difficiles à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c3eff-232">As you continue your journey to master web development, you'll find that CSS can be tricky.</span></span>  <span data-ttu-id="c3eff-233">Vous écrirez des feuilles CSS et vous attendez à ce qu’elle s’affiche de façon unique, mais le navigateur effectue une opération totalement différente.</span><span class="sxs-lookup"><span data-stu-id="c3eff-233">You'll write some CSS and expect it to display one way, but the browser does something completely different.</span></span>  <span data-ttu-id="c3eff-234">Microsoft Edge DevTools vous permet d’expérimenter facilement les modifications et de voir immédiatement l’incidence de ces modifications sur la page.</span><span class="sxs-lookup"><span data-stu-id="c3eff-234">Microsoft Edge DevTools makes it easy to experiment with changes and immediately see how those changes affect the page.</span></span>  

### <span data-ttu-id="c3eff-235">Ajouter une déclaration à une règle existante dans DevTools</span><span class="sxs-lookup"><span data-stu-id="c3eff-235">Add a declaration to an existing rulest in DevTools</span></span>   

<span data-ttu-id="c3eff-236">Lorsque vous souhaitez effectuer une itération sur le style d’un élément existant, ajoutez une déclaration à un RuleSet existant.</span><span class="sxs-lookup"><span data-stu-id="c3eff-236">When you want to iterate on the style of an existing element, add a declaration to an existing ruleset.</span></span>  <span data-ttu-id="c3eff-237">Essayez-le maintenant:</span><span class="sxs-lookup"><span data-stu-id="c3eff-237">Try it now:</span></span>  

1.  <span data-ttu-id="c3eff-238">Cliquez avec le bouton droit sur le lien **Accueil** et sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="c3eff-238">Right-click the **Home** link and select **Inspect**.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-239">Figure12</span><span class="sxs-lookup"><span data-stu-id="c3eff-239">Figure 12</span></span>  
    > <span data-ttu-id="c3eff-240">Examen du lien Accueil</span><span class="sxs-lookup"><span data-stu-id="c3eff-240">Inspecting the Home link</span></span>  
    > ![Examen du lien Accueil][ImageCssAdd1]  
    
    <span data-ttu-id="c3eff-242">DevTools s’ouvre à côté de votre page.</span><span class="sxs-lookup"><span data-stu-id="c3eff-242">DevTools opens up alongside your page.</span></span>  <span data-ttu-id="c3eff-243">Le code qui représente le lien Accueil `<a href="/">Home</a>` est surligné en bleu dans l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="c3eff-243">The code that represents the Home link, `<a href="/">Home</a>` is highlighted blue in the DOM Tree.</span></span>  <span data-ttu-id="c3eff-244">Pour cela, vous devez être familiarisé [avec la mise en route de HTML et du DOM][DevToolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="c3eff-244">This should be familiar from [Get Started with HTML and the DOM][DevToolsBeginnersHtml].</span></span>  <span data-ttu-id="c3eff-245">Dans l’onglet **styles** sous l’arborescence DOM, vous pouvez voir la `font-family: 'Courier New', Courier, serif` déclaration que vous avez `contact.html` précédemment ajoutée.</span><span class="sxs-lookup"><span data-stu-id="c3eff-245">In the **Styles** tab below the DOM Tree you can see the `font-family: 'Courier New', Courier, serif` declaration that you added to `contact.html` earlier.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-246">Figure13</span><span class="sxs-lookup"><span data-stu-id="c3eff-246">Figure 13</span></span>  
    > <span data-ttu-id="c3eff-247">L’onglet styles se trouve sous l’arborescence DOM</span><span class="sxs-lookup"><span data-stu-id="c3eff-247">The Styles tab is below the DOM Tree</span></span>  
    > ![L’onglet styles se trouve sous l’arborescence DOM][ImageCssAdd2]  
    
    <span data-ttu-id="c3eff-249">Si votre fenêtre DevTools est large, l’onglet styles se trouve à droite de l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="c3eff-249">If your DevTools window is wide, the Styles tab is to the right of the DOM Tree.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-250">Figure14</span><span class="sxs-lookup"><span data-stu-id="c3eff-250">Figure 14</span></span>  
    > <span data-ttu-id="c3eff-251">Onglet styles à droite de l’arborescence DOM</span><span class="sxs-lookup"><span data-stu-id="c3eff-251">The Styles tab is to the right of the DOM Tree</span></span>  
    > ![Onglet styles à droite de l’arborescence DOM][ImageCssAdd3]  
    
1.  <span data-ttu-id="c3eff-253">Cliquez sur l’espace blanc ci-dessous `font-family: 'Courier New', Courier, Serif` pour ajouter une nouvelle déclaration.</span><span class="sxs-lookup"><span data-stu-id="c3eff-253">Click the whitespace below `font-family: 'Courier New', Courier, Serif` to add a new declaration.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-254">Figure15</span><span class="sxs-lookup"><span data-stu-id="c3eff-254">Figure 15</span></span>  
    > <span data-ttu-id="c3eff-255">Ajout d’une nouvelle déclaration</span><span class="sxs-lookup"><span data-stu-id="c3eff-255">Adding a new declaration</span></span>  
    > ![Ajout d’une nouvelle déclaration][ImageCssAdd4]  
    
1.  <span data-ttu-id="c3eff-257">Tapez `color` , puis appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="c3eff-257">Type `color` and then press `Enter`.</span></span>  <span data-ttu-id="c3eff-258">L’interface utilisateur de saisie semi-automatique suggère des options au fur et à mesure que vous tapez.</span><span class="sxs-lookup"><span data-stu-id="c3eff-258">The autocomplete UI suggests options as you type.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-259">Figure16</span><span class="sxs-lookup"><span data-stu-id="c3eff-259">Figure 16</span></span>  
    > <span data-ttu-id="c3eff-260">Saisie</span><span class="sxs-lookup"><span data-stu-id="c3eff-260">Typing</span></span> `color`  
    > ![Entrer une couleur][ImageCssAdd5]  

1.  <span data-ttu-id="c3eff-262">Tapez `magenta` , puis appuyez de `Enter` nouveau.</span><span class="sxs-lookup"><span data-stu-id="c3eff-262">Type `magenta` and then press `Enter` again.</span></span>  <span data-ttu-id="c3eff-263">Tout le texte de la page de contact est désormais magenta.</span><span class="sxs-lookup"><span data-stu-id="c3eff-263">All of the text on the contact page is now magenta.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-264">Figure17</span><span class="sxs-lookup"><span data-stu-id="c3eff-264">Figure 17</span></span>  
    > <span data-ttu-id="c3eff-265">Saisie</span><span class="sxs-lookup"><span data-stu-id="c3eff-265">Typing</span></span> `magenta`  
    > ![Saisie de magenta][ImageCssAdd6]  
    
### <span data-ttu-id="c3eff-267">Modifier une déclaration dans DevTools</span><span class="sxs-lookup"><span data-stu-id="c3eff-267">Edit a declaration in DevTools</span></span>   

<span data-ttu-id="c3eff-268">Vous pouvez également modifier les déclarations existantes dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="c3eff-268">You can also edit existing declarations in DevTools.</span></span>  <span data-ttu-id="c3eff-269">Essayez-le maintenant:</span><span class="sxs-lookup"><span data-stu-id="c3eff-269">Try it now:</span></span>  

1.  <span data-ttu-id="c3eff-270">Cliquez sur le carré magenta en regard de `magenta` .</span><span class="sxs-lookup"><span data-stu-id="c3eff-270">Click the magenta square next to `magenta`.</span></span>  <span data-ttu-id="c3eff-271">Un sélecteur de couleur apparaît.</span><span class="sxs-lookup"><span data-stu-id="c3eff-271">A color picker pops up.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-272">Figure 18</span><span class="sxs-lookup"><span data-stu-id="c3eff-272">Figure 18</span></span>  
    > <span data-ttu-id="c3eff-273">Sélecteur de couleurs</span><span class="sxs-lookup"><span data-stu-id="c3eff-273">The Color Picker</span></span>  
    > ![Sélecteur de couleurs][ImageCssEdit1]  
    
1.  <span data-ttu-id="c3eff-275">Utilisez le sélecteur de couleurs pour remplacer le texte de la police par une couleur de votre choix.</span><span class="sxs-lookup"><span data-stu-id="c3eff-275">Use the color picker to change the font text to a color that you like.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-276">Figure 19</span><span class="sxs-lookup"><span data-stu-id="c3eff-276">Figure 19</span></span>  
    > <span data-ttu-id="c3eff-277">Modification de la couleur de police en violet grâce au sélecteur de couleurs</span><span class="sxs-lookup"><span data-stu-id="c3eff-277">Changing the font color to purple with the Color Picker</span></span>  
    > ![Modification de la couleur de police en violet grâce au sélecteur de couleurs][ImageCssEdit2]  

### <span data-ttu-id="c3eff-279">Ajouter un nouveau RuleSet dans DevTools</span><span class="sxs-lookup"><span data-stu-id="c3eff-279">Add a new ruleset in DevTools</span></span>   

<span data-ttu-id="c3eff-280">Vous pouvez également ajouter de nouvelles règles dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="c3eff-280">You can also add new rulesets in DevTools.</span></span>  <span data-ttu-id="c3eff-281">Essayez-le maintenant:</span><span class="sxs-lookup"><span data-stu-id="c3eff-281">Try it now:</span></span>  

1.  <span data-ttu-id="c3eff-282">Cliquez sur **nouvelle règle** de style nouvelle règle de ![ style ][ImageNewStyleRuleIcon] en regard de **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="c3eff-282">Click **New Style Rule** ![New Style Rule][ImageNewStyleRuleIcon] which is next to **.cls**.</span></span>  <span data-ttu-id="c3eff-283">Un RuleSet vide apparaît avec `a` le sélecteur.</span><span class="sxs-lookup"><span data-stu-id="c3eff-283">An empty ruleset appears with `a` as the selector.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-284">Figure 20</span><span class="sxs-lookup"><span data-stu-id="c3eff-284">Figure 20</span></span>  
    > <span data-ttu-id="c3eff-285">Ajout d’une nouvelle règle</span><span class="sxs-lookup"><span data-stu-id="c3eff-285">Adding a new rule</span></span>  
    > ![Ajout d’une nouvelle règle][ImageCssRule1]  
    
1.  <span data-ttu-id="c3eff-287">Remplacer `a` par `a:hover` .</span><span class="sxs-lookup"><span data-stu-id="c3eff-287">Replace `a` with `a:hover`.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-288">Figure 21</span><span class="sxs-lookup"><span data-stu-id="c3eff-288">Figure 21</span></span>  
    > <span data-ttu-id="c3eff-289">Remplacement `a` par</span><span class="sxs-lookup"><span data-stu-id="c3eff-289">Replacing `a` with</span></span> `a:hover`  
    > ![Remplacement de a avec a:hover][ImageCssRule2]  
    
    `:hover` <span data-ttu-id="c3eff-291">est une **Pseudo-classe**.</span><span class="sxs-lookup"><span data-stu-id="c3eff-291">is a **pseudo-class**.</span></span>  <span data-ttu-id="c3eff-292">Utilisez des Pseudo-classes pour appliquer des styles aux éléments spécifiques.</span><span class="sxs-lookup"><span data-stu-id="c3eff-292">Use pseudo-classes to style elements when they enter special states.</span></span>  <span data-ttu-id="c3eff-293">Par exemple, le `a:hover` style n’est appliqué que lorsque vous pointez sur un `<a>` élément.</span><span class="sxs-lookup"><span data-stu-id="c3eff-293">For example, the `a:hover` style only takes effect when you're hovering over an `<a>` element.</span></span>  
    
1.  <span data-ttu-id="c3eff-294">Cliquez entre les crochets pour ajouter une nouvelle déclaration.</span><span class="sxs-lookup"><span data-stu-id="c3eff-294">Click between the brackets to add a new declaration.</span></span>  
1.  <span data-ttu-id="c3eff-295">Tapez `background-color` le nom de la déclaration et appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="c3eff-295">Type `background-color` for the declaration name and then press `Enter`.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-296">Figure 22</span><span class="sxs-lookup"><span data-stu-id="c3eff-296">Figure 22</span></span>  
    > <span data-ttu-id="c3eff-297">Saisie</span><span class="sxs-lookup"><span data-stu-id="c3eff-297">Typing</span></span> `background-color`  
    > ![Saisie d’une couleur d’arrière-plan][ImageCssRule3]  
    
1.  <span data-ttu-id="c3eff-299">Tapez `green` la valeur de la déclaration, puis appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="c3eff-299">Type `green` for the declaration value and then press `Enter`.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-300">Figure 23</span><span class="sxs-lookup"><span data-stu-id="c3eff-300">Figure 23</span></span>  
    > <span data-ttu-id="c3eff-301">Saisie</span><span class="sxs-lookup"><span data-stu-id="c3eff-301">Typing</span></span> `green`  
    > ![Saisie de texte vert][ImageCssRule4]  
    
1.  <span data-ttu-id="c3eff-303">Positionnez le pointeur de la souris sur le lien **Accueil** .</span><span class="sxs-lookup"><span data-stu-id="c3eff-303">Hover your mouse over the **Home** link.</span></span>  <span data-ttu-id="c3eff-304">L’arrière-plan du lien devient vert.</span><span class="sxs-lookup"><span data-stu-id="c3eff-304">The background of the link turns green.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-305">Figure 24</span><span class="sxs-lookup"><span data-stu-id="c3eff-305">Figure 24</span></span>  
    > <span data-ttu-id="c3eff-306">Survol du lien Accueil pour afficher son arrière-plan vert</span><span class="sxs-lookup"><span data-stu-id="c3eff-306">Hovering over the Home link to reveal its green background</span></span>  
    > ![Survol du lien Accueil pour afficher son arrière-plan vert][ImageCssRule5]  
    
## <span data-ttu-id="c3eff-308">Réutiliser les styles entre les pages à l’aide de feuilles de style externes</span><span class="sxs-lookup"><span data-stu-id="c3eff-308">Re-use styles across pages with external stylesheets</span></span>   

<span data-ttu-id="c3eff-309">Auparavant, vous avez ajouté cette feuille de style interne aux `contact.html` éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="c3eff-309">Earlier you added this internal stylesheet to `contact.html`:</span></span>  

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

<span data-ttu-id="c3eff-310">Que faire si vous souhaitez changer de style `index.html` ?</span><span class="sxs-lookup"><span data-stu-id="c3eff-310">What if you wanted to style `index.html` the same way?</span></span>  <span data-ttu-id="c3eff-311">Que se passe-t-il si vous aviez un *millier* de pages et que vous souhaitez appliquer ces styles à tous les éléments?</span><span class="sxs-lookup"><span data-stu-id="c3eff-311">What if you had a *thousand* pages and you wanted to apply these styles to all of them?</span></span>  <span data-ttu-id="c3eff-312">Vous devez copier et coller cette feuille de style interne dans chaque page Web de votre site.</span><span class="sxs-lookup"><span data-stu-id="c3eff-312">You'd have to copy and paste this internal stylesheet into every single web page on your site.</span></span>  <span data-ttu-id="c3eff-313">Les **feuilles de style externes** vous permettent d’écrire votre CSS une seule fois sur plusieurs pages.</span><span class="sxs-lookup"><span data-stu-id="c3eff-313">**External stylesheets** allow you to write your CSS once yet apply it to multiple pages.</span></span>  <span data-ttu-id="c3eff-314">Essayez-le maintenant:</span><span class="sxs-lookup"><span data-stu-id="c3eff-314">Try it now:</span></span>  

1.  <span data-ttu-id="c3eff-315">Tout d’abord, rechargez l’onglet Live pour supprimer les modifications que vous avez apportées dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="c3eff-315">First, reload the live tab to remove the changes that you made in DevTools.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-316">Figure 25</span><span class="sxs-lookup"><span data-stu-id="c3eff-316">Figure 25</span></span>  
    >  <span data-ttu-id="c3eff-317">Après le rechargement de la page, les modifications apportées à DevTools ont disparu</span><span class="sxs-lookup"><span data-stu-id="c3eff-317">After reloading the page the changes that were made in DevTools are gone</span></span>  
    > ![ <span data-ttu-id="c3eff-318">Après le rechargement de la page, les modifications apportées à DevTools ont disparu</span><span class="sxs-lookup"><span data-stu-id="c3eff-318">After reloading the page the changes that were made in DevTools are gone</span></span>][ImageCssExternal01]  
    
1.  <span data-ttu-id="c3eff-319">Revenez à l' **onglet Éditeur** , puis ouvrez `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="c3eff-319">Go back to the **editor tab** and open `contact.html`.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-320">Figure 26</span><span class="sxs-lookup"><span data-stu-id="c3eff-320">Figure 26</span></span>  
    > `contact.html`  
    > ![contact. html][ImageCssExternal02]  
    
1.  <span data-ttu-id="c3eff-322">Supprimez tous `<style>` les éléments entre et `</style>` , y compris `<style>` et `</style>` .</span><span class="sxs-lookup"><span data-stu-id="c3eff-322">Delete everything between `<style>` and `</style>`, including `<style>` and `</style>`.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-323">Figure 27</span><span class="sxs-lookup"><span data-stu-id="c3eff-323">Figure 27</span></span>  
    > <span data-ttu-id="c3eff-324">La balise de style a été supprimée</span><span class="sxs-lookup"><span data-stu-id="c3eff-324">The style tag has been removed</span></span>  
    > ![La balise de style a été supprimée][ImageCssExternal03]  
    
1.  <span data-ttu-id="c3eff-326">Accédez à `index.html` la balise et supprimez- `style="background-color: aliceblue;"` la `<nav>` .</span><span class="sxs-lookup"><span data-stu-id="c3eff-326">Go to `index.html` and remove `style="background-color: aliceblue;"` from the `<nav>` tag.</span></span>  <span data-ttu-id="c3eff-327">Vous avez supprimé toutes les feuilles CSS que vous avez précédemment ajoutées à votre site.</span><span class="sxs-lookup"><span data-stu-id="c3eff-327">You have now removed all of the CSS that you previously added to your site.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-328">Figure 28</span><span class="sxs-lookup"><span data-stu-id="c3eff-328">Figure 28</span></span>  
    > <span data-ttu-id="c3eff-329">Le style intraligne a été supprimé de l’élément navigation</span><span class="sxs-lookup"><span data-stu-id="c3eff-329">The inline style has been removed from the nav element</span></span>  
    > ![Le style intraligne a été supprimé de l’élément navigation][ImageCssExternal04]  

1.  <span data-ttu-id="c3eff-331">Cliquez sur **nouveau fichier**.</span><span class="sxs-lookup"><span data-stu-id="c3eff-331">Click **New File**.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-332">Figure 29</span><span class="sxs-lookup"><span data-stu-id="c3eff-332">Figure 29</span></span>  
    > <span data-ttu-id="c3eff-333">Boîte de dialogue nouveau fichier</span><span class="sxs-lookup"><span data-stu-id="c3eff-333">The new file dialog</span></span>  
    > ![Boîte de dialogue nouveau fichier][ImageCssExternal05]  
    
1.  <span data-ttu-id="c3eff-335">Remplacez `cool-file.js` par `style.css` , puis cliquez sur **Ajouter un fichier**.</span><span class="sxs-lookup"><span data-stu-id="c3eff-335">Replace `cool-file.js` with `style.css` and then click **Add File**.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-336">Figure 30</span><span class="sxs-lookup"><span data-stu-id="c3eff-336">Figure 30</span></span>  
    > <span data-ttu-id="c3eff-337">Saisie</span><span class="sxs-lookup"><span data-stu-id="c3eff-337">Typing</span></span> `style.css`  
    > ![Saisie de styles. CSS][ImageCssExternal06]  
    
1.  <span data-ttu-id="c3eff-339">Collez ce code dans les `style.css` éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="c3eff-339">Paste this code into `style.css`:</span></span>  
    
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
    
    > ##### <span data-ttu-id="c3eff-340">Figure 31</span><span class="sxs-lookup"><span data-stu-id="c3eff-340">Figure 31</span></span>  
    > <span data-ttu-id="c3eff-341">Ajouter du code à</span><span class="sxs-lookup"><span data-stu-id="c3eff-341">Adding code to</span></span> `style.css`  
    > ![Ajouter du code à style. CSS][ImageCssExternal07]  
    
    <span data-ttu-id="c3eff-343">À ce stade, vous avez créé une feuille de style externe, mais votre code HTML ne sait pas encore qu’il existe.</span><span class="sxs-lookup"><span data-stu-id="c3eff-343">At this point, you have created an external stylesheet, but your HTML doesn't know that it exists, yet.</span></span>  
    
1.  <span data-ttu-id="c3eff-344">Ouvrir `index.html` .</span><span class="sxs-lookup"><span data-stu-id="c3eff-344">Open `index.html`.</span></span>  
1.  <span data-ttu-id="c3eff-345">Ajoutez `<link rel="stylesheet" href="style.css">` à votre code html.</span><span class="sxs-lookup"><span data-stu-id="c3eff-345">Add `<link rel="stylesheet" href="style.css">` to your HTML.</span></span>  
    
    ```html
    ...
        <head>
            ...
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <link rel="stylesheet" href="style.css">
        </head>
        ...
    ...
    ```  

    > ##### <span data-ttu-id="c3eff-346">Figure 32</span><span class="sxs-lookup"><span data-stu-id="c3eff-346">Figure 32</span></span>  
    > <span data-ttu-id="c3eff-347">Liaison à</span><span class="sxs-lookup"><span data-stu-id="c3eff-347">Linking to</span></span> `style.css`  
    > ![Liaison à style. CSS][ImageCssExternal08]  

1.  <span data-ttu-id="c3eff-349">Accédez à `contact.html` l’emplacement du lien et ajoutez-le.</span><span class="sxs-lookup"><span data-stu-id="c3eff-349">Go to `contact.html` and add the link there, too.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-350">Figure 33</span><span class="sxs-lookup"><span data-stu-id="c3eff-350">Figure 33</span></span>  
    > <span data-ttu-id="c3eff-351">Liaison vers `style.css` dans</span><span class="sxs-lookup"><span data-stu-id="c3eff-351">Linking to `style.css` in</span></span> `contact.html`  
    > ![Liaison vers style. CSS dans le fichier contact. html][ImageCssExternal09]  

1.  <span data-ttu-id="c3eff-353">Accédez à l' **onglet Live**.  La page d’accueil possède désormais la même police que la dernière section et une section de navigation bleue.</span><span class="sxs-lookup"><span data-stu-id="c3eff-353">Go to the **live tab**.  The home page now has the same font from the last section and a blue navigation section.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-354">Figure 34</span><span class="sxs-lookup"><span data-stu-id="c3eff-354">Figure 34</span></span>  
    > <span data-ttu-id="c3eff-355">Page d’accueil</span><span class="sxs-lookup"><span data-stu-id="c3eff-355">The home page</span></span>  
    > ![Page d’accueil][ImageCssExternal10]  
    
1.  <span data-ttu-id="c3eff-357">Cliquez sur le lien de **contact** pour accéder à la page de contact.</span><span class="sxs-lookup"><span data-stu-id="c3eff-357">Click the **Contact** link to go to the contact page.</span></span>  <span data-ttu-id="c3eff-358">La page de contact a la même mise en forme que la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="c3eff-358">The contact page has the same formatting as the home page.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-359">Figure 35</span><span class="sxs-lookup"><span data-stu-id="c3eff-359">Figure 35</span></span>  
    > <span data-ttu-id="c3eff-360">Page de contact</span><span class="sxs-lookup"><span data-stu-id="c3eff-360">The contact page</span></span>  
    > ![Page de contact][ImageCssExternal11]  
    
## <span data-ttu-id="c3eff-362">Utiliser une infrastructure CSS</span><span class="sxs-lookup"><span data-stu-id="c3eff-362">Use a CSS framework</span></span>   

<span data-ttu-id="c3eff-363">Les **infrastructures CSS** sont des collections de styles intégrées par d’autres développeurs, qui simplifient la création de sites Web attractifs.</span><span class="sxs-lookup"><span data-stu-id="c3eff-363">**CSS frameworks** are collections of styles built by other developers that make it easier to create attractive web sites.</span></span>  <span data-ttu-id="c3eff-364">Au lieu de définir vous-même les styles, une infrastructure vous donne une collection de styles que vous pouvez utiliser sur les éléments de la page.</span><span class="sxs-lookup"><span data-stu-id="c3eff-364">Instead of defining styles yourself, a framework gives you a collection of styles that you can use on your page elements.</span></span>  

1.  <span data-ttu-id="c3eff-365">Copiez le code suivant:</span><span class="sxs-lookup"><span data-stu-id="c3eff-365">Copy the following code:</span></span>  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  <span data-ttu-id="c3eff-366">Accédez à l’onglet modification et collez le code dans `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="c3eff-366">Go to the editing tab and paste the code into `contact.html`.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-367">Figure 36</span><span class="sxs-lookup"><span data-stu-id="c3eff-367">Figure 36</span></span>  
    > <span data-ttu-id="c3eff-368">Liaison vers l’infrastructure dans</span><span class="sxs-lookup"><span data-stu-id="c3eff-368">Linking to the framework in</span></span> `contact.html`  
    > ![Liaison vers l’infrastructure dans le fichier contact. html][ImageCssFramework1]  
    
1.  <span data-ttu-id="c3eff-370">Collez également le code `index.html` .</span><span class="sxs-lookup"><span data-stu-id="c3eff-370">Paste the code into `index.html`, as well.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-371">Figure 37</span><span class="sxs-lookup"><span data-stu-id="c3eff-371">Figure 37</span></span>  
    > <span data-ttu-id="c3eff-372">Liaison vers l’infrastructure dans</span><span class="sxs-lookup"><span data-stu-id="c3eff-372">Linking to the framework in</span></span> `index.html`  
    > ![Liaison vers l’infrastructure dans index. html][ImageCssFramework2]  
    
1.  <span data-ttu-id="c3eff-374">Revenez à l’onglet Live pour afficher vos modifications.</span><span class="sxs-lookup"><span data-stu-id="c3eff-374">Go back to the live tab to view your changes.</span></span>  <span data-ttu-id="c3eff-375">Même si la couleur d’arrière-plan de la `<nav>` police et la police des `li a` éléments sont identiques, la police des autres éléments a changé.</span><span class="sxs-lookup"><span data-stu-id="c3eff-375">While the background color of the `<nav>` and the font of the `li a` elements are the same, the font of the other elements has changed.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-376">Figure 38</span><span class="sxs-lookup"><span data-stu-id="c3eff-376">Figure 38</span></span>  
    > <span data-ttu-id="c3eff-377">Une partie de la police de la page d’accueil a changé en raison de l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="c3eff-377">Some of the font on the home page has changed because of the framework</span></span>  
    > ![Une partie de la police de la page d’accueil a changé en raison de l’infrastructure.][ImageCssFramework3]  

### <span data-ttu-id="c3eff-379">Utiliser une classe</span><span class="sxs-lookup"><span data-stu-id="c3eff-379">Use a class</span></span>   

<span data-ttu-id="c3eff-380">Dans la dernière section, vous avez ajouté des données d’amorçage dans vos pages Web, ce qui a modifié les polices de certains éléments de votre site.</span><span class="sxs-lookup"><span data-stu-id="c3eff-380">In the last section, you added Bootstrap to your web pages, which changed the fonts of some of the elements on your site.</span></span>  <span data-ttu-id="c3eff-381">Les infrastructures CSS vous permettent d’apporter des modifications importantes à votre page avec peu de code.</span><span class="sxs-lookup"><span data-stu-id="c3eff-381">CSS frameworks can help you make major changes to your page with very little code.</span></span>  <span data-ttu-id="c3eff-382">Essayez-le maintenant en modifiant votre en-tête:</span><span class="sxs-lookup"><span data-stu-id="c3eff-382">Try it now by changing your header:</span></span>  

1.  <span data-ttu-id="c3eff-383">Copiez ce code:</span><span class="sxs-lookup"><span data-stu-id="c3eff-383">Copy this code:</span></span>  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  <span data-ttu-id="c3eff-384">Ajoutez ce code à votre `<header>` balise dans `index.html` .</span><span class="sxs-lookup"><span data-stu-id="c3eff-384">Add this code to your `<header>` tag in `index.html`.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-385">Figure 39</span><span class="sxs-lookup"><span data-stu-id="c3eff-385">Figure 39</span></span>  
    > <span data-ttu-id="c3eff-386">Ajouter des classes dans</span><span class="sxs-lookup"><span data-stu-id="c3eff-386">Adding classes in</span></span> `index.html`  
    > ![Ajout de classes dans index. html][ImageCssJumbotron1]  
    
1.  <span data-ttu-id="c3eff-388">Ajoutez le code à votre `<header>` balise `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="c3eff-388">Add the code to your `<header>` tag in `contact.html`, too.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-389">Figure 40</span><span class="sxs-lookup"><span data-stu-id="c3eff-389">Figure 40</span></span>  
    > <span data-ttu-id="c3eff-390">Ajouter des classes dans</span><span class="sxs-lookup"><span data-stu-id="c3eff-390">Adding classes in</span></span> `contact.html`  
    > ![Ajout de classes dans contacts. html][ImageCssJumbotron2]  
    
1.  <span data-ttu-id="c3eff-392">Affichez vos modifications sous l’onglet Live.  Il y a une grande zone grise dans votre en-tête.</span><span class="sxs-lookup"><span data-stu-id="c3eff-392">View your changes in the live tab.  There's a big, grey box around your header now.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-393">Figure 41</span><span class="sxs-lookup"><span data-stu-id="c3eff-393">Figure 41</span></span>  
    > <span data-ttu-id="c3eff-394">L’en-tête est désormais entouré d’un cadre gris.</span><span class="sxs-lookup"><span data-stu-id="c3eff-394">The header now has a big, grey box around it</span></span>  
    > ![L’en-tête est désormais entouré d’un cadre gris.][ImageCssJumbotron3]  
    
### <span data-ttu-id="c3eff-396">Comprendre les classes</span><span class="sxs-lookup"><span data-stu-id="c3eff-396">Understand classes</span></span>   

<span data-ttu-id="c3eff-397">Les classes vous permettent d’affecter des collections de styles à des éléments arbitraires.</span><span class="sxs-lookup"><span data-stu-id="c3eff-397">Classes let you assign collections of styles to arbitrary elements.</span></span>  <span data-ttu-id="c3eff-398">Par exemple, en définissant l' `class` attribut des `<header>` balises pour `jumbotron` appliquer les styles suivants aux éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="c3eff-398">For example, setting the `class` attribute of the `<header>` tags to `jumbotron` applied the following styles to them:</span></span>  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

<span data-ttu-id="c3eff-399">L’un des avantages des classes réside dans le fait qu’ils vous permettent d’appliquer des styles à tous les éléments souhaités.</span><span class="sxs-lookup"><span data-stu-id="c3eff-399">One advantage of classes is that they let you apply styles to whatever elements you want.</span></span>  <span data-ttu-id="c3eff-400">Par exemple, supposons que vous vouliez définir la couleur d’arrière-plan de *certains* `<p>` éléments sur pourpre, mais pas sur la *totalité* de ces éléments.</span><span class="sxs-lookup"><span data-stu-id="c3eff-400">For example, suppose you want to set the background color of *some* `<p>` elements to purple, but not *all* of them.</span></span>  <span data-ttu-id="c3eff-401">Vous pouvez définir le style dans une classe:</span><span class="sxs-lookup"><span data-stu-id="c3eff-401">You could define the style in a class:</span></span>  

```css
.custom-background {
  background-color: purple;
}
```  

<span data-ttu-id="c3eff-402">Puis appliquez la classe uniquement aux `<p>` éléments auxquels vous voulez appliquer un style:</span><span class="sxs-lookup"><span data-stu-id="c3eff-402">And then apply the class to only the `<p>` elements that you want to style:</span></span>  

```html
...
    ...
        ...
        <p>This won't be purple.</p>
        <p class="custom-background">This will be purple.</p>
        <p>This won't be purple.</p>
        <p class="custom-background">This will be purple.</p>
        ...
    ...
...
```  

### <span data-ttu-id="c3eff-403">Aligner des éléments</span><span class="sxs-lookup"><span data-stu-id="c3eff-403">Align elements</span></span>   

<span data-ttu-id="c3eff-404">Le bootstrap fournit également des classes permettant d’aligner des éléments.</span><span class="sxs-lookup"><span data-stu-id="c3eff-404">Bootstrap also provides classes for aligning elements.</span></span>  <span data-ttu-id="c3eff-405">Essayez-le maintenant:</span><span class="sxs-lookup"><span data-stu-id="c3eff-405">Try it now:</span></span>  

1.  <span data-ttu-id="c3eff-406">Revenez à l’onglet Éditeur, puis ouvrez `index.html` .</span><span class="sxs-lookup"><span data-stu-id="c3eff-406">Go back to the editor tab and open `index.html`.</span></span>  
1.  <span data-ttu-id="c3eff-407">Ajoutez `class="container-fluid"` à votre `<body>` indicateur.</span><span class="sxs-lookup"><span data-stu-id="c3eff-407">Add `class="container-fluid"` to your `<body>` tag.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-408">Figure 42</span><span class="sxs-lookup"><span data-stu-id="c3eff-408">Figure 42</span></span>  
    > <span data-ttu-id="c3eff-409">Ajout de la `container-fluid` classe</span><span class="sxs-lookup"><span data-stu-id="c3eff-409">Adding the `container-fluid` class</span></span>  
    > ![Ajout de la classe Container-fluidiques][ImageCssAlign1]  

1.  <span data-ttu-id="c3eff-411">Renvoyez `<nav>` vos `<main>` éléments et `<div class="row">` .</span><span class="sxs-lookup"><span data-stu-id="c3eff-411">Wrap your `<nav>` and `<main>` elements in `<div class="row">`.</span></span>  <span data-ttu-id="c3eff-412">Assurez-vous d’entrer `</div>` après pour `</main>` fermer correctement la nouvelle balise.</span><span class="sxs-lookup"><span data-stu-id="c3eff-412">Make sure to put `</div>` after `</main>` in order to properly close the new tag.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-413">Figure 43</span><span class="sxs-lookup"><span data-stu-id="c3eff-413">Figure 43</span></span>  
    > <span data-ttu-id="c3eff-414">Ajout d’une ligne</span><span class="sxs-lookup"><span data-stu-id="c3eff-414">Adding a row</span></span>  
    > ![Ajout d’une ligne][ImageCssAlign2]  
    
1.  <span data-ttu-id="c3eff-416">Ajoutez `class="col-3"` votre `<nav>` indicateur et `class="col-9"` votre `<main>` indicateur.</span><span class="sxs-lookup"><span data-stu-id="c3eff-416">Add `class="col-3"` to your `<nav>` tag and `class="col-9"` to your `<main>` tag.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-417">Figure 44</span><span class="sxs-lookup"><span data-stu-id="c3eff-417">Figure 44</span></span>  
    > <span data-ttu-id="c3eff-418">Ajout des `col-3` `col-9` classes et</span><span class="sxs-lookup"><span data-stu-id="c3eff-418">Adding the `col-3` and `col-9` classes</span></span>  
    > ![Ajout des classes col-3 et col-9][ImageCssAlign3]  
    
1.  <span data-ttu-id="c3eff-420">Affichez vos modifications sous l’onglet Live.</span><span class="sxs-lookup"><span data-stu-id="c3eff-420">View your changes in the live tab.</span></span>  
    
    > ##### <span data-ttu-id="c3eff-421">Figure 45</span><span class="sxs-lookup"><span data-stu-id="c3eff-421">Figure 45</span></span>  
    > <span data-ttu-id="c3eff-422">Le contenu de navigation est désormais à gauche du contenu principal</span><span class="sxs-lookup"><span data-stu-id="c3eff-422">The nav content is now to the left of the main content</span></span>  
    > ![Le contenu de navigation est désormais à gauche du contenu principal][ImageCssAlign4]  
    
## <span data-ttu-id="c3eff-424">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="c3eff-424">Next steps</span></span>   

<span data-ttu-id="c3eff-425">Félicitations!</span><span class="sxs-lookup"><span data-stu-id="c3eff-425">Congratulations!</span></span>  <span data-ttu-id="c3eff-426">C’est terminé!</span><span class="sxs-lookup"><span data-stu-id="c3eff-426">You're done!</span></span>  

*   <span data-ttu-id="c3eff-427">La meilleure façon d’optimiser le développement Web consiste à créer des sites supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="c3eff-427">The best way to get better at web development is to build more sites.</span></span>  <span data-ttu-id="c3eff-428">Ne vous inquiétez pas de casser votre contenu.</span><span class="sxs-lookup"><span data-stu-id="c3eff-428">Don't worry about breaking stuff.</span></span>  <span data-ttu-id="c3eff-429">Amusez-vous et découvrez autant que vous le pouvez.</span><span class="sxs-lookup"><span data-stu-id="c3eff-429">Just have fun and learn as much as you can along the way.</span></span>  
*   <span data-ttu-id="c3eff-430">Pour en savoir plus sur le stylisation des pages Web, voir [Présentation de CSS][MDNCssFirstSteps] .</span><span class="sxs-lookup"><span data-stu-id="c3eff-430">Check out [Introduction to CSS][MDNCssFirstSteps] to learn lots more about styling web pages.</span></span>  
*   <span data-ttu-id="c3eff-431">Pour plus d’informations sur l’utilisation de DevTools dans le cadre d’une feuille de style CSS de page, consultez notre didacticiel sur l' [affichage et la modification][DevtoolsCssIndex] de la feuille de route.</span><span class="sxs-lookup"><span data-stu-id="c3eff-431">Work through our [Get Started with Viewing and Changing CSS][DevtoolsCssIndex] tutorial to learn more about how you can use DevTools to experiment with a page's CSS.</span></span>  

<!--- image links --->  

[ImageNewStyleRuleIcon]: /microsoft-edge/devtools-guide-chromium/media/new-style-rule-icon.msft.png  

[ImageCssIntro1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-intro1.msft.png "Figure 1: à quoi ressemble votre site"  
[ImageCssIntro2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-intro2.msft.png "Figure 2: apparence de votre site à la fin du didacticiel"  
[ImageCssSetup1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup1.msft.png "Figure 3: onglet édition"  
[ImageCssSetup2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup2.msft.png "Figure 4: menu options de Project"  
[ImageCssSetup3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup3.msft.png "Figure 5: onglet Live"  
[ImageCssStyled]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-red_paragraph.msft.png "Figure 6: styles avec CSS"  
[ImageCssInline1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-inline1.msft.png "Figure 7: index. html"  
[ImageCssInline2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-inline2.msft.png "Figure 8: la couleur d’arrière-plan derrière les liens accueil et contact est désormais bleue"  
[ImageCssInternal1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-internal1.msft.png "Figure 9: page de contact"  
[ImageCssInternal2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-internal2.msft.png "Figure 10: la police des liens accueil et contact a changé"  
[ImageCssMultiple1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-multiple1.msft.png "Figure 11: le texte «contactez-moi!» a désormais la même police que les liens accueil et contact."  
[ImageCssAdd1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add1.msft.png "Figure 12: examen du lien Accueil"  
[ImageCssAdd2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add2.msft.png "Figure 13: l’onglet styles se trouve sous l’arborescence DOM"  
[ImageCssAdd3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add3.msft.png "Figure 14: onglet styles à droite de l’arborescence DOM"  
[ImageCssAdd4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add4.msft.png "Figure 15: ajout d’une nouvelle déclaration"
[ImageCssAdd5]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add5.msft.png "Figure 16: couleur de frappe"  
[ImageCssAdd6]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add6.msft.png "Figure 17: saisie de magenta"  
[ImageCssEdit1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-edit1.msft.png "Figure 18: sélecteur de couleurs"  
[ImageCssEdit2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-edit2.msft.png "Figure 19: modification de la couleur de police en violet avec le sélecteur de couleurs"  
[ImageCssRule1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule1.msft.png "Figure 20: ajout d’une nouvelle règle"  
[ImageCssRule2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule2.msft.png "Figure 21: remplacement de a par a:hover"  
[ImageCssRule3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule3.msft.png "Figure 22: saisie de la couleur d’arrière-plan"  
[ImageCssRule4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule4.msft.png "Figure 23: saisie en vert"  
[ImageCssRule5]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule5.msft.png "Figure 24: survol du lien Accueil pour afficher son arrière-plan vert"  
[ImageCssExternal01]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external1.msft.png "Figure 25: après le rechargement de la page, les modifications apportées à DevTools ont disparu"  
[ImageCssExternal02]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external2.msft.png "Figure 26: contact. html"  
[ImageCssExternal03]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external3.msft.png "Figure 27: la balise de style a été supprimée"  
[ImageCssExternal04]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external4.msft.png "Figure 28: le style intraligne a été supprimé de l’élément navigation"  
[ImageCssExternal05]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external5.msft.png "Figure 29: boîte de dialogue nouveau fichier"  
[ImageCssExternal06]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external6.msft.png "Figure 30: saisie de style. CSS"  
[ImageCssExternal07]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external7.msft.png "Figure 31: ajout de code au style. CSS"  
[ImageCssExternal08]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external8.msft.png "Figure 32: création d’un lien vers style. CSS"  
[ImageCssExternal09]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external9.msft.png "Figure 33: création d’un lien vers style. CSS dans le fichier contact. html"  
[ImageCssExternal10]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external10.msft.png "Figure 34: page d’accueil"  
[ImageCssExternal11]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external11.msft.png "Figure 35: page de contact"  
[ImageCssFramework1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework1.msft.png "Figure 36: création d’un lien vers l’infrastructure dans le fichier contact. html"  
[ImageCssFramework2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework2.msft.png "Figure 37: liaisons vers l’infrastructure dans index. html"  
[ImageCssFramework3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework3.msft.png "Figure 38: une partie de la police de la page d’accueil a changé en raison de l’infrastructure"  
[ImageCssJumbotron1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron1.msft.png "Figure 39: ajout de classes dans index. html"  
[ImageCssJumbotron2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron2.msft.png "Figure 40: ajout de classes dans contact. html"  
[ImageCssJumbotron3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron3.msft.png "Figure 41: l’en-tête est désormais entouré d’un cadre gris"  
[ImageCssAlign1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align1.msft.png "Figure 42: ajout de la classe Container-fluidiques"  
[ImageCssAlign2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align2.msft.png "Figure 43: ajout d’une ligne"  
[ImageCssAlign3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align3.msft.png "Figure 44: ajout des classes col-3 et col-9"  
[ImageCssAlign4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align4.msft.png "Figure 45: le contenu de navigation est désormais à gauche du contenu principal"  

<!--- links  --->  

[DevToolsBeginnersHtml]: html.md "DevTools pour les débutants: commencez à utiliser HTML et au DOM"  
[DevtoolsCssIndex]: ../css/index.md "Découvrir comment afficher et modifier des feuilles CSS"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index. html-cuit-Amphibian | Problème"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "Premiers pas dans la feuille de style CSS | MDN"  

> [!NOTE]
> <span data-ttu-id="c3eff-482">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c3eff-482">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c3eff-483">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/beginners/css) et est créée par [Katherine Jackson][KatherineJackson] \ (Technical Writer Intern, chrome devtools \).</span><span class="sxs-lookup"><span data-stu-id="c3eff-483">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/css) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="c3eff-485">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c3eff-485">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
