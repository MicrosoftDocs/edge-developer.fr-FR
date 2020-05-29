---
title: DevTools pour les débutants
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 8695fe1b2c5d78bd074447acd26a1f01a5833b2d
ms.sourcegitcommit: 8bfa239274e7a4856b961b9cf163b08d96463c10
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2020
ms.locfileid: "10581586"
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

# <span data-ttu-id="799b6-103">DevTools pour les débutants: commencez à utiliser HTML et au DOM</span><span class="sxs-lookup"><span data-stu-id="799b6-103">DevTools for Beginners: Get Started with HTML and the DOM</span></span>   

<span data-ttu-id="799b6-104">Voici le premier d’une série de didacticiels pour vous apprendre les notions de base du développement Web.</span><span class="sxs-lookup"><span data-stu-id="799b6-104">This is the first in a series of tutorials that teach you the basics of web development.</span></span>  <span data-ttu-id="799b6-105">Vous découvrirez également un ensemble d’outils de développement Web, appelés Microsoft Edge DevTools, qui peuvent augmenter votre productivité.</span><span class="sxs-lookup"><span data-stu-id="799b6-105">You will also learn about a set of web developer tools called Microsoft Edge DevTools that can increase your productivity.</span></span>  

<span data-ttu-id="799b6-106">Dans ce didacticiel, vous allez découvrir HTML et le DOM.</span><span class="sxs-lookup"><span data-stu-id="799b6-106">In this particular tutorial, you learn about HTML and the DOM.</span></span>  <span data-ttu-id="799b6-107">HTML est l’une des technologies fondamentales du développement Web.</span><span class="sxs-lookup"><span data-stu-id="799b6-107">HTML is one of the core technologies of web development.</span></span>  <span data-ttu-id="799b6-108">Il s’agit de la langue qui contrôle la structure et le contenu de pages Web.</span><span class="sxs-lookup"><span data-stu-id="799b6-108">It is the language that controls the structure and content of webpages.</span></span>  <span data-ttu-id="799b6-109">Le DOM est également lié à la structure et au contenu des pages Web, mais vous en saurez plus à ce sujet plus tard.</span><span class="sxs-lookup"><span data-stu-id="799b6-109">The DOM is also related to the structure and content of webpages, but you'll learn more about that later.</span></span>  

## <span data-ttu-id="799b6-110">Définis</span><span class="sxs-lookup"><span data-stu-id="799b6-110">Goals</span></span>   

<span data-ttu-id="799b6-111">Vous allez découvrir le développement Web en créant votre propre site Web.</span><span class="sxs-lookup"><span data-stu-id="799b6-111">You are going to learn web development by actually building your own website.</span></span>  <span data-ttu-id="799b6-112">Au moment où vous effectuez tous les didacticiels de la série *devtools pour les débutants* , votre site fini se présente comme **figure 1**.</span><span class="sxs-lookup"><span data-stu-id="799b6-112">By the time you complete all of the tutorials in the *DevTools for Beginners* series, your finished site will look like **Figure 1**.</span></span>  

> ##### <span data-ttu-id="799b6-113">Figure1</span><span class="sxs-lookup"><span data-stu-id="799b6-113">Figure 1</span></span>  
> <span data-ttu-id="799b6-114">Le site terminé</span><span class="sxs-lookup"><span data-stu-id="799b6-114">The finished site</span></span>  
> ![Le site terminé][ImageHtmlFinished]  

<span data-ttu-id="799b6-116">À la fin de ce didacticiel, vous allez comprendre les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="799b6-116">By the end of this tutorial, you will understand:</span></span>  

*   <span data-ttu-id="799b6-117">Le code HTML et le DOM créent le contenu que vous voyez sur les pages Web.</span><span class="sxs-lookup"><span data-stu-id="799b6-117">How HTML and the DOM create the content that you see on webpages.</span></span>  
*   <span data-ttu-id="799b6-118">La façon dont Microsoft Edge DevTools peut vous aider à tester les modifications HTML et DOM.</span><span class="sxs-lookup"><span data-stu-id="799b6-118">How Microsoft Edge DevTools can help you experiment with HTML and DOM changes.</span></span>  
*   <span data-ttu-id="799b6-119">Différence entre HTML et le DOM.</span><span class="sxs-lookup"><span data-stu-id="799b6-119">The difference between HTML and the DOM.</span></span>  

<span data-ttu-id="799b6-120">Vous disposez également d’un site Web réel.</span><span class="sxs-lookup"><span data-stu-id="799b6-120">You'll also have a real website!</span></span>  <span data-ttu-id="799b6-121">Vous pouvez utiliser ce site pour héberger votre c.v. ou votre blog.</span><span class="sxs-lookup"><span data-stu-id="799b6-121">You can use this site to host your resume or blog.</span></span>  

## <span data-ttu-id="799b6-122">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="799b6-122">Prerequisites</span></span>   

<span data-ttu-id="799b6-123">Avant de suivre ce didacticiel, remplissez les conditions préalables suivantes:</span><span class="sxs-lookup"><span data-stu-id="799b6-123">Before attempting this tutorial, complete the following prerequisites:</span></span>  

*   <span data-ttu-id="799b6-124">Si vous n’êtes pas familiarisé avec le format HTML, consultez la rubrique [mise en route de HTML][MDNGettingStartedHtml].</span><span class="sxs-lookup"><span data-stu-id="799b6-124">If you're unfamiliar with HTML, read [Getting Started with HTML][MDNGettingStartedHtml].</span></span>  
*   <span data-ttu-id="799b6-125">Téléchargez le navigateur Web [Microsoft Edge][MicrosoftEdgeInsider] .</span><span class="sxs-lookup"><span data-stu-id="799b6-125">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="799b6-126">Ce didacticiel utilise un ensemble d’outils de développement Web, appelés Microsoft Edge DevTools, qui sont intégrés à Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="799b6-126">This tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <span data-ttu-id="799b6-127">Configurer votre code</span><span class="sxs-lookup"><span data-stu-id="799b6-127">Set up your code</span></span>   

<span data-ttu-id="799b6-128">Vous envisagez de générer votre site dans un éditeur de code en ligne appelé erreur.</span><span class="sxs-lookup"><span data-stu-id="799b6-128">You're going to build your site in an online code editor called Glitch.</span></span>  

1.  <span data-ttu-id="799b6-129">Ouvrez le [code source][GlitchAlluringShockIndex].</span><span class="sxs-lookup"><span data-stu-id="799b6-129">Open the [source code][GlitchAlluringShockIndex].</span></span>  <span data-ttu-id="799b6-130">Cet onglet est appelé **onglet Éditeur** tout au long de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="799b6-130">This tab will be called the **editor tab** throughout this tutorial.</span></span>  
    > ##### <span data-ttu-id="799b6-131">Figure 2</span><span class="sxs-lookup"><span data-stu-id="799b6-131">Figure 2</span></span>  
    > <span data-ttu-id="799b6-132">Onglet Éditeur</span><span class="sxs-lookup"><span data-stu-id="799b6-132">The editor tab</span></span>  
    > ![Onglet Éditeur][ImageHtmlSetup1]  

1.  <span data-ttu-id="799b6-134">Cliquez sur **alluring-choc**.</span><span class="sxs-lookup"><span data-stu-id="799b6-134">Click **alluring-shock**.</span></span>  <span data-ttu-id="799b6-135">Le menu options de Project s’ouvre dans le coin supérieur gauche.</span><span class="sxs-lookup"><span data-stu-id="799b6-135">The Project Options menu opens in the top-left corner.</span></span>  
    
    > #### <span data-ttu-id="799b6-136">Figure3</span><span class="sxs-lookup"><span data-stu-id="799b6-136">Figure 3</span></span>  
    > <span data-ttu-id="799b6-137">Menu options de Project</span><span class="sxs-lookup"><span data-stu-id="799b6-137">The Project Options menu</span></span>  
    > ![Menu options de Project][ImageHtmlSetup2]  
    
1.  <span data-ttu-id="799b6-139">Cliquez sur **Remix Project**.</span><span class="sxs-lookup"><span data-stu-id="799b6-139">Click **Remix Project**.</span></span>  <span data-ttu-id="799b6-140">Le problème crée une copie du projet que vous pouvez modifier et qui génère de manière aléatoire un nouveau nom pour le projet.</span><span class="sxs-lookup"><span data-stu-id="799b6-140">Glitch creates a copy of the project that you can edit and randomly generates a new name for the project.</span></span>  <span data-ttu-id="799b6-141">Le contenu est le même qu’auparavant.</span><span class="sxs-lookup"><span data-stu-id="799b6-141">The content is the same as before.</span></span>  
    
    > ##### <span data-ttu-id="799b6-142">Figure 4</span><span class="sxs-lookup"><span data-stu-id="799b6-142">Figure 4</span></span>  
    > <span data-ttu-id="799b6-143">Le projet Remixed</span><span class="sxs-lookup"><span data-stu-id="799b6-143">The remixed project</span></span>  
    > ![Le projet Remixed][ImageHtmlSetup3]  
    
1.  <span data-ttu-id="799b6-145">Si vous envisagez de terminer le didacticiel suivant de cette série, cliquez sur **se connecter** , puis connectez-vous à votre compte GitHub ou Facebook.</span><span class="sxs-lookup"><span data-stu-id="799b6-145">If you plan on completing the next tutorial in this series, click **Sign In** and sign in to Glitch with your GitHub or Facebook account.</span></span>  <span data-ttu-id="799b6-146">Si vous ne vous connectez pas, vous perdrez la possibilité de modifier ce projet une fois que vous avez fermé l’onglet modification.</span><span class="sxs-lookup"><span data-stu-id="799b6-146">If you don't sign in you will lose the ability to edit this project once you close the editing tab.</span></span>  
1.  <span data-ttu-id="799b6-147">Cliquez sur **Afficher** et sélectionnez **dans une nouvelle fenêtre**.</span><span class="sxs-lookup"><span data-stu-id="799b6-147">Click **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="799b6-148">Un nouvel onglet s’ouvre et affiche la page dynamique.</span><span class="sxs-lookup"><span data-stu-id="799b6-148">A new tab opens, showing you the live page.</span></span>  <span data-ttu-id="799b6-149">Cet onglet est appelé **onglet dynamique** tout au long de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="799b6-149">This tab will be called the **live tab** throughout this tutorial.</span></span>  
    
    > ##### <span data-ttu-id="799b6-150">Figure 5</span><span class="sxs-lookup"><span data-stu-id="799b6-150">Figure 5</span></span>  
    > <span data-ttu-id="799b6-151">Onglet Live</span><span class="sxs-lookup"><span data-stu-id="799b6-151">The live tab</span></span>  
    > ![Onglet Live][ImageHtmlSetup4]  
    
## <span data-ttu-id="799b6-153">Ajouter du contenu</span><span class="sxs-lookup"><span data-stu-id="799b6-153">Add content</span></span>   

<span data-ttu-id="799b6-154">Votre site est assez vide.</span><span class="sxs-lookup"><span data-stu-id="799b6-154">Your site is pretty empty.</span></span>  <span data-ttu-id="799b6-155">Pour ajouter du contenu à votre présentation, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="799b6-155">Follow the steps below to add some content to it!</span></span>  

1.  <span data-ttu-id="799b6-156">Dans l' **onglet Éditeur**, remplacez `<!-- You're "About Me" will go here.  -->` par `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="799b6-156">In the **editor tab**, replace `<!-- You're "About Me" will go here.  -->` with `<h1>About Me</h1>`.</span></span>  
    
    ```html
    ...
        ...
        <body>
            <p> Your site!</p>
            <main>
                <h1>About Me</h1>
            </main>
            ...
        ...
    ...
    ```  
    
    > ##### <span data-ttu-id="799b6-157">Figure 6</span><span class="sxs-lookup"><span data-stu-id="799b6-157">Figure 6</span></span>  
    > <span data-ttu-id="799b6-158">Le nouveau code est mis en surbrillance dans l’onglet Éditeur</span><span class="sxs-lookup"><span data-stu-id="799b6-158">The new code is highlighted in the editor tab</span></span>  
    > ![Le nouveau code est mis en surbrillance dans l’onglet Éditeur][ImageHtmlAdd1]  
    
1.  <span data-ttu-id="799b6-160">Affichez vos modifications sous l' **onglet Live**.  Le texte `About Me` est visible sur la page.</span><span class="sxs-lookup"><span data-stu-id="799b6-160">View your changes in the **live tab**.  The text `About Me` is visible on the page.</span></span>  <span data-ttu-id="799b6-161">Il est plus grand que le reste du texte, car l' `<h1>` élément représente un titre de section.</span><span class="sxs-lookup"><span data-stu-id="799b6-161">It's larger than the rest of the text, because the `<h1>` element represents a section heading.</span></span>  <span data-ttu-id="799b6-162">Dans votre navigateur Web, les titres sont automatiquement appliqués en taille de police plus grande.</span><span class="sxs-lookup"><span data-stu-id="799b6-162">Your web browser automatically styles headings in larger font sizes.</span></span>  
    
    > ##### <span data-ttu-id="799b6-163">Figure 7</span><span class="sxs-lookup"><span data-stu-id="799b6-163">Figure 7</span></span>  
    > <span data-ttu-id="799b6-164">Le nouveau titre est affiché dans l’onglet Live</span><span class="sxs-lookup"><span data-stu-id="799b6-164">The new heading is visible in the live tab</span></span>  
    > ![Le nouveau titre est affiché dans l’onglet Live][ImageHtmlAdd2]  
    
1.  <span data-ttu-id="799b6-166">Dans l' **onglet Éditeur**, insérez `<p>I am learning HTML.  Recent accomplishments:</p>` l’image sur la ligne en dessous de laquelle vous venez d’entrer `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="799b6-166">Back in the **editor tab**, insert `<p>I am learning HTML.  Recent accomplishments:</p>` on the line below where you just put `<h1>About Me</h1>`.</span></span>  
    
    ```html
    ...
        ...
        <body>
            <p> Your site!</p>
            <main>
                <h1>About Me</h1>
                <p>I am learning web development.  Recent accomplishments:</p>
            </main>
            ...
        ...
    ...
    ```  

    > ##### <span data-ttu-id="799b6-167">Figure8</span><span class="sxs-lookup"><span data-stu-id="799b6-167">Figure 8</span></span>  
    > <span data-ttu-id="799b6-168">Le nouveau code est mis en surbrillance dans l’onglet Éditeur</span><span class="sxs-lookup"><span data-stu-id="799b6-168">The new code is highlighted in the editor tab</span></span>  
    > ![Le nouveau code est mis en surbrillance dans l’onglet Éditeur][ImageHtmlAdd3]  
    
1.  <span data-ttu-id="799b6-170">Affichez votre modification sous l' **onglet Live**.</span><span class="sxs-lookup"><span data-stu-id="799b6-170">View your change in the **live tab**.</span></span>  
1.  <span data-ttu-id="799b6-171">Dans l' **onglet Éditeur**, ajoutez la liste de vos réalisations:</span><span class="sxs-lookup"><span data-stu-id="799b6-171">Back in the **editor tab**, add a list of your accomplishments:</span></span>  
    
    ```html
    ...
        ...
            ...
            <p>I am learning web development.  Recent accomplishments:</p>
            <ul>
                <li>Learned how to set up my code in Glitch.</li>
                <li>Added content to my HTML.</li>
                <li>TODO: Learn how to use Microsoft Edge DevTools to experiment with content changes.</li>
                <li>TODO: Learn the difference between HTML and the DOM.</li>
            </ul>
            ...
        ...
    ...
    ```  
    
    > ##### <span data-ttu-id="799b6-172">Figure9</span><span class="sxs-lookup"><span data-stu-id="799b6-172">Figure 9</span></span>  
    > <span data-ttu-id="799b6-173">Le nouveau code est mis en surbrillance dans l’onglet Éditeur</span><span class="sxs-lookup"><span data-stu-id="799b6-173">The new code is highlighted in the editor tab</span></span>  
    > ![Le nouveau code est mis en surbrillance dans l’onglet Éditeur][ImageHtmlAdd4]  
    
1.  <span data-ttu-id="799b6-175">Revenez à l' **onglet Live** pour vérifier que le nouveau contenu s’affiche correctement.</span><span class="sxs-lookup"><span data-stu-id="799b6-175">Again, go back to the **live tab** to make sure that the new content is displaying correctly.</span></span>  
    
    > ##### <span data-ttu-id="799b6-176">Figure10</span><span class="sxs-lookup"><span data-stu-id="799b6-176">Figure 10</span></span>  
    > <span data-ttu-id="799b6-177">La nouvelle liste est affichée sous l’onglet Live</span><span class="sxs-lookup"><span data-stu-id="799b6-177">The new list is visible in the live tab</span></span>  
    > ![La nouvelle liste est affichée sous l’onglet Live][ImageHtmlAdd5]  
    
## <span data-ttu-id="799b6-179">Tester les modifications de contenu dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="799b6-179">Experiment with content changes in Microsoft Edge DevTools</span></span>   

<span data-ttu-id="799b6-180">Si vous développez une grande page à l’aide d’un grand nombre de fichiers HTML, vous pouvez imaginer qu’il peut être fastidieux de reculer entre l’onglet Éditeur et l’onglet actif de centaines de fois pour voir vos modifications, en particulier si vous ne savez pas exactement ce que vous voulez faire dans la page.</span><span class="sxs-lookup"><span data-stu-id="799b6-180">If you were developing a big page with a lot of HTML, you can imagine that it might be somewhat tedious to go back-and-forth between the editor tab and the live tab hundreds of times in order to see your changes, especially if you weren't sure what exactly to put on the page.</span></span>  <span data-ttu-id="799b6-181">Microsoft Edge DevTools peut vous aider à tester du contenu sans quitter l’onglet Live.</span><span class="sxs-lookup"><span data-stu-id="799b6-181">Microsoft Edge DevTools can help you experiment with content changes without ever leaving the live tab.</span></span>  

### <span data-ttu-id="799b6-182">Différences entre le format HTML et le DOM</span><span class="sxs-lookup"><span data-stu-id="799b6-182">Learn the difference between HTML and the DOM</span></span>   

<span data-ttu-id="799b6-183">Avant de commencer à modifier votre contenu à partir de Microsoft Edge DevTools, il est utile de comprendre la différence entre le code HTML et le DOM.</span><span class="sxs-lookup"><span data-stu-id="799b6-183">Before you start editing your content from Microsoft Edge DevTools, it's helpful to understand the difference between HTML and the DOM.</span></span>  <span data-ttu-id="799b6-184">Le meilleur moyen d’apprendre est, par exemple:</span><span class="sxs-lookup"><span data-stu-id="799b6-184">The best way to learn is by example:</span></span>  

1.  <span data-ttu-id="799b6-185">Accédez à l' **onglet Live**.  Le texte s’affiche en bas de la page `A new element!?!` .</span><span class="sxs-lookup"><span data-stu-id="799b6-185">Go to the **live tab**.  At the bottom of your page you see the text `A new element!?!`.</span></span>  
    
    > ###### <span data-ttu-id="799b6-186">Figure11</span><span class="sxs-lookup"><span data-stu-id="799b6-186">Figure 11</span></span>  
    > <span data-ttu-id="799b6-187">En bas de la page, vous `A new element!?!` pouvez voir le texte</span><span class="sxs-lookup"><span data-stu-id="799b6-187">At the bottom of the page the text `A new element!?!` can be seen</span></span>  
    > ![En bas de la page, le texte!?! un nouvel élément][ImageHtmlDom1]  
    
1.  <span data-ttu-id="799b6-190">Revenez à l' **onglet Éditeur** et essayez de Rechercher ce texte dans `index.html` .</span><span class="sxs-lookup"><span data-stu-id="799b6-190">Go back to the **editor tab** and try to find this text in `index.html`.</span></span>  <span data-ttu-id="799b6-191">Ce n’est pas là!</span><span class="sxs-lookup"><span data-stu-id="799b6-191">It's not there!</span></span>  
    
    > ##### <span data-ttu-id="799b6-192">Figure12</span><span class="sxs-lookup"><span data-stu-id="799b6-192">Figure 12</span></span>  
    > <span data-ttu-id="799b6-193">Le texte `A new element!?!` de mystère est introuvable dans</span><span class="sxs-lookup"><span data-stu-id="799b6-193">The mystery text `A new element!?!` is nowhere to be found in</span></span> `index.html`  
    > ![Le texte du mystère est un nouvel élément!?!][ImageHtmlDom2]  
    
1.  <span data-ttu-id="799b6-196">Revenez à l' **onglet Live**, cliquez avec le bouton droit `A new element!?!` , puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="799b6-196">Go back to the **live tab**, right-click `A new element!?!`, and select **Inspect**.</span></span>  
    
    > ##### <span data-ttu-id="799b6-197">Figure13</span><span class="sxs-lookup"><span data-stu-id="799b6-197">Figure 13</span></span>  
    > <span data-ttu-id="799b6-198">Inspecter du texte</span><span class="sxs-lookup"><span data-stu-id="799b6-198">Inspecting some text</span></span>  
    > ![Inspecter du texte][ImageHtmlDom3]  
    
    <span data-ttu-id="799b6-200">DevTools s’ouvre à côté de votre page.</span><span class="sxs-lookup"><span data-stu-id="799b6-200">DevTools opens up alongside your page.</span></span>  `<div>A new element!?!</div>` <span data-ttu-id="799b6-201">est en surbrillance bleue.</span><span class="sxs-lookup"><span data-stu-id="799b6-201">is highlighted blue.</span></span>  <span data-ttu-id="799b6-202">Même si cette structure dans DevTools ressemble à votre code HTML, il s’agit en réalité de l' **arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="799b6-202">Although this structure in DevTools looks like your HTML, it is actually the **DOM Tree**.</span></span>  
    
    > ##### <span data-ttu-id="799b6-203">Figure14</span><span class="sxs-lookup"><span data-stu-id="799b6-203">Figure 14</span></span>  
    > <span data-ttu-id="799b6-204">DevTools est ouvert parallèlement à la page</span><span class="sxs-lookup"><span data-stu-id="799b6-204">DevTools is open alongside the page</span></span>  
    > ![DevTools est ouvert parallèlement à la page][ImageHtmlDom4]  
    
<span data-ttu-id="799b6-206">Lors du chargement de la page, le navigateur utilise votre code HTML pour créer le contenu *initial* de la page.</span><span class="sxs-lookup"><span data-stu-id="799b6-206">When your page loads, the browser takes your HTML to create the *initial* content of the page.</span></span>  <span data-ttu-id="799b6-207">Le DOM représente le contenu *actuel* de la page, qui peut changer au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="799b6-207">The DOM represents the *current* content of the page, which can change over time.</span></span>  <span data-ttu-id="799b6-208">Le `<div>A new element!?!</div>` contenu mystérieux est ajouté à votre page en raison de la `<script src="new.js"></script>` balise située en bas de votre code html.</span><span class="sxs-lookup"><span data-stu-id="799b6-208">The mysterious `<div>A new element!?!</div>` content is added to your page because of the `<script src="new.js"></script>` tag at the bottom of your HTML.</span></span>  <span data-ttu-id="799b6-209">Cette balise entraîne l’exécution du code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="799b6-209">This tag causes some JavaScript code to run.</span></span>  <span data-ttu-id="799b6-210">En savoir plus sur JavaScript dans un didacticiel ultérieur, mais pour le considérer comme un langage de programmation qui peut changer le contenu de votre page.</span><span class="sxs-lookup"><span data-stu-id="799b6-210">You'll learn more about JavaScript in a later tutorial, but for now think of it as a programming language that can change the content of your page.</span></span>  <span data-ttu-id="799b6-211">Dans ce cas particulier, le code JavaScript est ajouté `<div>A new element!?!</div>` à votre page.</span><span class="sxs-lookup"><span data-stu-id="799b6-211">In this particular case, JavaScript code adds `<div>A new element!?!</div>` to your page.</span></span>  <span data-ttu-id="799b6-212">C’est la raison pour laquelle ce texte de mystère est visible sur votre page dynamique, mais pas dans votre code HTML.</span><span class="sxs-lookup"><span data-stu-id="799b6-212">That is why this mystery text is visible on your live page, but not in your HTML.</span></span>  

### <span data-ttu-id="799b6-213">Modifier le DOM</span><span class="sxs-lookup"><span data-stu-id="799b6-213">Edit the DOM</span></span>   

<span data-ttu-id="799b6-214">Si vous voulez tester rapidement les changements de contenu sans quitter l’onglet Live, essayez DevTools.</span><span class="sxs-lookup"><span data-stu-id="799b6-214">If you want to quickly experiment with content changes without ever leaving the live tab, try DevTools.</span></span>  

1.  <span data-ttu-id="799b6-215">Dans DevTools, cliquez avec le bouton droit, `Your site!` puis sélectionnez **modifier en HTML**.</span><span class="sxs-lookup"><span data-stu-id="799b6-215">In DevTools, right-click `Your site!` and select **Edit as HTML**.</span></span>  

    > ##### <span data-ttu-id="799b6-216">Figure15</span><span class="sxs-lookup"><span data-stu-id="799b6-216">Figure 15</span></span>  
    > <span data-ttu-id="799b6-217">Modification du nœud au format HTML</span><span class="sxs-lookup"><span data-stu-id="799b6-217">Editing the node as HTML</span></span>  
    > ![Modification du nœud au format HTML][ImageHtmlEdit1]  
    
1.  <span data-ttu-id="799b6-219">Remplacez `<p>Your site!</p>` par le code ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="799b6-219">Replace `<p>Your site!</p>` with the code below.</span></span>  
    
    ```html
    ...
        ...
            ...
            <header>
                <p><b>Welcome to my site!</b></p>
                <button>Download my resume</button>
            </header>
            ...
        ...
    ...
    ```  
    
    > ##### <span data-ttu-id="799b6-220">Figure16</span><span class="sxs-lookup"><span data-stu-id="799b6-220">Figure 16</span></span>  
    > <span data-ttu-id="799b6-221">Modification du nœud au format HTML</span><span class="sxs-lookup"><span data-stu-id="799b6-221">Editing the node as HTML</span></span>  
    > ![Modification du nœud au format HTML][ImageHtmlEdit2]  
    
1.  <span data-ttu-id="799b6-223">`Control` + `Enter` `Command` + `Enter` Pour enregistrer vos modifications ou cliquez en dehors de la zone, appuyez sur \ (Windows \) ou \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="799b6-223">Press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to save your changes, or click outside of the box.</span></span>  <span data-ttu-id="799b6-224">Vos modifications apparaissent automatiquement dans le mode en direct de votre page.</span><span class="sxs-lookup"><span data-stu-id="799b6-224">Your changes automatically show up in the live view of your page.</span></span>  <span data-ttu-id="799b6-225">Le texte `Your site!` a été remplacé par le nouveau contenu.</span><span class="sxs-lookup"><span data-stu-id="799b6-225">The text `Your site!` has been replaced with the new content.</span></span>  
    
    > ##### <span data-ttu-id="799b6-226">Figure17</span><span class="sxs-lookup"><span data-stu-id="799b6-226">Figure 17</span></span>  
    > <span data-ttu-id="799b6-227">Le nouveau contenu apparaît immédiatement sur la page</span><span class="sxs-lookup"><span data-stu-id="799b6-227">The new content shows up immediately on the page</span></span>  
    > ![Le nouveau contenu apparaît immédiatement sur la page][ImageHtmlEdit3]  
    
<span data-ttu-id="799b6-229">Ce flux de travail est uniquement utile pour tester les modifications de contenu.</span><span class="sxs-lookup"><span data-stu-id="799b6-229">This workflow is only good for experimenting with content changes.</span></span>  <span data-ttu-id="799b6-230">Si vous rechargez la page ou que vous fermez l’onglet, vos modifications sont supprimées définitivement.</span><span class="sxs-lookup"><span data-stu-id="799b6-230">If you reload the page or close the tab, your changes will be gone forever.</span></span>  <span data-ttu-id="799b6-231">Si vous utilisez ce flux de travail et que vous voulez enregistrer les modifications, vous devez les copier manuellement dans votre code HTML.</span><span class="sxs-lookup"><span data-stu-id="799b6-231">If you're using this workflow and you want to save your changes, you need to manually copy those changes over to your HTML.</span></span>  <span data-ttu-id="799b6-232">Les deux sections suivantes vous montrent davantage de moyens de changer le contenu de l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="799b6-232">The next couple of sections show you some more ways that you can change content from the DOM Tree.</span></span>  

## <span data-ttu-id="799b6-233">Réorganiser les nœuds</span><span class="sxs-lookup"><span data-stu-id="799b6-233">Reorder nodes</span></span>   

<span data-ttu-id="799b6-234">Vous pouvez également modifier l’ordre des nœuds DOM.</span><span class="sxs-lookup"><span data-stu-id="799b6-234">You can also change the order of DOM nodes.</span></span>  <span data-ttu-id="799b6-235">Par exemple, sur votre page Web, le menu de navigation est proche du bas.</span><span class="sxs-lookup"><span data-stu-id="799b6-235">For example, on your web page the navigation menu is near the bottom.</span></span>  <span data-ttu-id="799b6-236">Pour le déplacer vers le haut:</span><span class="sxs-lookup"><span data-stu-id="799b6-236">To move it to the top:</span></span>  

1.  <span data-ttu-id="799b6-237">Recherchez le `<nav>` nœud dans l' **arborescence DOM** de devtools.</span><span class="sxs-lookup"><span data-stu-id="799b6-237">Find the `<nav>` node in the **DOM Tree** of DevTools.</span></span>  
    
    > ##### <span data-ttu-id="799b6-238">Figure 18</span><span class="sxs-lookup"><span data-stu-id="799b6-238">Figure 18</span></span>  
    > <span data-ttu-id="799b6-239">Le nœud de navigation est surligné en bleu dans DevTools</span><span class="sxs-lookup"><span data-stu-id="799b6-239">The nav node is highlighted blue in DevTools</span></span>  
    > ![Le nœud de navigation est surligné en bleu dans DevTools][ImageHtmlReorder1]  
    
1.  <span data-ttu-id="799b6-241">Faites glisser le `<nav>` nœud vers le haut, de façon à ce qu’il s’agit du premier enfant sous le `<body>` nœud.</span><span class="sxs-lookup"><span data-stu-id="799b6-241">Drag the `<nav>` node to the top, so that it's the first child below the `<body>` node.</span></span>  
    > ##### <span data-ttu-id="799b6-242">Figure 19</span><span class="sxs-lookup"><span data-stu-id="799b6-242">Figure 19</span></span>  
    > <span data-ttu-id="799b6-243">Faire glisser le nœud de navigation vers le haut</span><span class="sxs-lookup"><span data-stu-id="799b6-243">Dragging the nav node to the top</span></span>  
    > ![Faire glisser le nœud de navigation vers le haut][ImageHtmlReorder2]  
    
    <span data-ttu-id="799b6-245">Le `<nav>` nœud est désormais affiché en haut de votre page.</span><span class="sxs-lookup"><span data-stu-id="799b6-245">The `<nav>` node is now displaying at the top of your page.</span></span>  
    
    > ##### <span data-ttu-id="799b6-246">Figure 20</span><span class="sxs-lookup"><span data-stu-id="799b6-246">Figure 20</span></span>  
    > <span data-ttu-id="799b6-247">Le nœud de navigation est en haut de la page</span><span class="sxs-lookup"><span data-stu-id="799b6-247">The nav node is at the top of the page</span></span>  
    > ![Le nœud de navigation est en haut de la page][ImageHtmlReorder3]  
    
### <span data-ttu-id="799b6-249">Supprimer un nœud</span><span class="sxs-lookup"><span data-stu-id="799b6-249">Delete a node</span></span>   

<span data-ttu-id="799b6-250">Vous pouvez également supprimer des nœuds de l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="799b6-250">You can also remove nodes from the DOM Tree.</span></span>  

1.  <span data-ttu-id="799b6-251">Dans l' **arborescence DOM**, cliquez sur `<div>A new element!?!</div>` .</span><span class="sxs-lookup"><span data-stu-id="799b6-251">In the **DOM Tree**, click `<div>A new element!?!</div>`.</span></span>  <span data-ttu-id="799b6-252">DevTools surligne le nœud bleu.</span><span class="sxs-lookup"><span data-stu-id="799b6-252">DevTools highlights the node blue.</span></span>  
    
    > ##### <span data-ttu-id="799b6-253">Figure 21</span><span class="sxs-lookup"><span data-stu-id="799b6-253">Figure 21</span></span>  
    > <span data-ttu-id="799b6-254">Sélection du nœud à supprimer</span><span class="sxs-lookup"><span data-stu-id="799b6-254">Selecting the node to be deleted</span></span>  
    > ![Sélection du nœud à supprimer][ImageHtmlDelete1]  
    
1.  <span data-ttu-id="799b6-256">Appuyez sur la `Delete` touche de votre clavier.</span><span class="sxs-lookup"><span data-stu-id="799b6-256">Press the `Delete` key on your keyboard.</span></span>  <span data-ttu-id="799b6-257">Le `<div>A new element!?!</div>` nœud est supprimé de votre arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="799b6-257">The `<div>A new element!?!</div>` node is removed from your DOM Tree.</span></span>  
    
    > ##### <span data-ttu-id="799b6-258">Figure 22</span><span class="sxs-lookup"><span data-stu-id="799b6-258">Figure 22</span></span>  
    > <span data-ttu-id="799b6-259">Le nœud a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="799b6-259">The node has been deleted</span></span>  
    > ![Le nœud a été supprimé.][ImageHtmlDelete2]  
    
## <span data-ttu-id="799b6-261">Copiez vos modifications</span><span class="sxs-lookup"><span data-stu-id="799b6-261">Copy your changes</span></span>   

<span data-ttu-id="799b6-262">Vous avez presque terminé.</span><span class="sxs-lookup"><span data-stu-id="799b6-262">You're almost done.</span></span>  <span data-ttu-id="799b6-263">Vous avez apporté des modifications à votre page dans DevTools, mais celles-ci ne sont pas encore enregistrées dans votre code source.</span><span class="sxs-lookup"><span data-stu-id="799b6-263">You've made a few changes to your page in DevTools, but they're not yet saved to your source code.</span></span>  

1.  <span data-ttu-id="799b6-264">Actualisez votre **onglet actif**.  Les modifications que vous avez apportées à l’arborescence DOM disparaissent.</span><span class="sxs-lookup"><span data-stu-id="799b6-264">Refresh your **live tab**.  The changes that you made in the DOM Tree disappear.</span></span>  <span data-ttu-id="799b6-265">Par exemple, le texte `Your site!` revient en haut de la page et le texte `A new element!?!` revient en bas.</span><span class="sxs-lookup"><span data-stu-id="799b6-265">In particular, the text `Your site!` returns to the top of the page, and the text `A new element!?!` returns to the bottom.</span></span>  
    
    > ##### <span data-ttu-id="799b6-266">Figure 23</span><span class="sxs-lookup"><span data-stu-id="799b6-266">Figure 23</span></span>  
    > <span data-ttu-id="799b6-267">Les modifications que vous avez apportées ont disparu</span><span class="sxs-lookup"><span data-stu-id="799b6-267">The changes that you've made are gone</span></span>  
    > ![Les modifications que vous avez apportées ont disparu][ImageHtmlCopy1]  

1.  <span data-ttu-id="799b6-269">Copiez le code ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="799b6-269">Copy the code below.</span></span>  
    
    ```html
    <!DOCTYPE html>
    <html lang="en">
        <head>
            <meta charset="utf-8">
            <meta http-equiv="X-UA-Compatible" content="IE=edge">
            <meta name="viewport" content="width=device-width, initial-scale=1">
        </head>
        <body>
            <header>
                <p>Welcome to my site!</p>
            </header>
            <nav>
                <ul>
                    <li><a href="/">Home</a></li>
                    <li><a href="/contact.html">Contact</a></li>
                </ul>
            </nav>
            <main>
                <h1>About Me</h1>
                <p>I am learning web development.  Recent accomplishments:</p>
                <ul>
                    <li>Learned how to set up my code in Glitch.</li>
                    <li>Added content to my HTML.</li>
                    <li>Learned how to use Microsoft Edge DevTools to experiment with content changes.</li>
                    <li>Learned the difference between HTML and the DOM.</li>
                </ul>
            </main>
        </body>
    </html>
    ```  
      
1.  <span data-ttu-id="799b6-270">Revenez à l' **onglet Éditeur** et remplacez le contenu de votre `index.html` fichier par le code que vous venez de copier.</span><span class="sxs-lookup"><span data-stu-id="799b6-270">Go back to the **editor tab** and replace the contents of your `index.html` file with the code that you just copied.</span></span>  
    
    > ##### <span data-ttu-id="799b6-271">Figure 24</span><span class="sxs-lookup"><span data-stu-id="799b6-271">Figure 24</span></span>  
    > <span data-ttu-id="799b6-272">Aspect de votre `index.html` fichier</span><span class="sxs-lookup"><span data-stu-id="799b6-272">How your `index.html` file should look</span></span>  
    > ![Aspect de votre fichier index. html][ImageHtmlCopy2]  
    
## <span data-ttu-id="799b6-274">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="799b6-274">Next steps</span></span>   

*   <span data-ttu-id="799b6-275">Suivez les étapes ci-dessous pour découvrir comment appliquer un [style à votre][DevToolsBeginnersCss]page et tester les modifications de style dans Microsoft Edge devtools.</span><span class="sxs-lookup"><span data-stu-id="799b6-275">Complete the next tutorial in this series, [Get Started with CSS][DevToolsBeginnersCss], to learn how to style your page and experiment with style changes in Microsoft Edge DevTools.</span></span>  
*   <span data-ttu-id="799b6-276">Lire [Introduction au DOM][MDNIntroductionDom] pour en savoir plus sur le DOM.</span><span class="sxs-lookup"><span data-stu-id="799b6-276">Read [Introduction to the DOM][MDNIntroductionDom] to learn more about the DOM.</span></span>  
*   <span data-ttu-id="799b6-277">Consultez un cours comme [Introduction au développement Web][CourseraIntroductionToWebDevelopment] pour bénéficier d’une expérience de développement Web plus pratique.</span><span class="sxs-lookup"><span data-stu-id="799b6-277">Check out a course like [Introduction to Web Development][CourseraIntroductionToWebDevelopment] to get more hands-on web development experience.</span></span>  

<!--- image links --->  

[ImageHtmlFinished]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-finished.msft.png "Figure 1: site terminé"  
[ImageHtmlSetup1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup1.msft.png "Figure 2: onglet Éditeur"  
[ImageHtmlSetup2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup2.msft.png "Figure 3: menu options de Project"  
[ImageHtmlSetup3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup3.msft.png "Figure 4: projet Remixed"  
[ImageHtmlSetup4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup4.msft.png "Figure 5: onglet Live"  
[ImageHtmlAdd1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add1.msft.png "Figure 6: le nouveau code est mis en surbrillance dans l’onglet Éditeur"  
[ImageHtmlAdd2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add2.msft.png "Figure 7: le nouveau titre est affiché dans l’onglet Live"  
[ImageHtmlAdd3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add3.msft.png "Figure 8: le nouveau code est mis en surbrillance dans l’onglet Éditeur"  
[ImageHtmlAdd4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add4.msft.png "Figure 9: le nouveau code est mis en surbrillance dans l’onglet Éditeur"  
[ImageHtmlAdd5]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add5.msft.png "Figure 10: la nouvelle liste est affichée sous l’onglet Live"  
[ImageHtmlDom1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom1.msft.png "Figure 11: en bas de la page le texte!?! un nouvel élément est visible"  
[ImageHtmlDom2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom2.msft.png "Figure 12: le texte du mystère est un nouvel élément!?! est introuvable dans index. html"  
[ImageHtmlDom3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom3.msft.png "Figure 13: examen de texte"  
[ImageHtmlDom4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom4.msft.png "Figure 14: DevTools est ouvert parallèlement à la page"  
[ImageHtmlEdit1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit1.msft.png "Figure 15: modification du nœud au format HTML"  
[ImageHtmlEdit2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit2.msft.png "Figure 16: modification du nœud au format HTML"  
[ImageHtmlEdit3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit3.msft.png "Figure 17: le nouveau contenu apparaît immédiatement sur la page"  
[ImageHtmlReorder1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder1.msft.png "Figure 18: le nœud de navigation est surligné en bleu dans DevTools"  
[ImageHtmlReorder2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder2.msft.png "Figure 19: glissement du nœud de navigation vers le haut"  
[ImageHtmlReorder3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder3.msft.png "Figure 20: le nœud de navigation est en haut de la page"  
[ImageHtmlDelete1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-delete1.msft.png "Figure 21: sélection du nœud à supprimer"  
[ImageHtmlDelete2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-delete2.msft.png "Figure 22: le nœud a été supprimé"  
[ImageHtmlCopy1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-copy1.msft.png "Figure 23: les modifications que vous avez apportées ont disparu"  
[ImageHtmlCopy2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-copy2.msft.png "Figure 24: apparence du fichier index. html"  

<!--- links --->  

[DevToolsBeginnersCss]: /microsoft-edge/devtools-guide-chromium/beginners/css "DevTools pour les débutants: prendre en main CSS"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Présentation du développement Web | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index. html-alluring-choc | Problème"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Mise en route de HTML | MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introduction au DOM | MDN"  

> [!NOTE]
> <span data-ttu-id="799b6-308">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="799b6-308">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="799b6-309">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/beginners/html) et est créée par [Katherine Jackson][KatherineJackson] \ (Technical Writer Intern, chrome devtools \).</span><span class="sxs-lookup"><span data-stu-id="799b6-309">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/html) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="799b6-311">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="799b6-311">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
