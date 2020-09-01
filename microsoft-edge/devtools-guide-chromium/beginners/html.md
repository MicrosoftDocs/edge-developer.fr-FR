---
title: 'DevTools pour les débutants: commencez à utiliser HTML et au DOM'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 50dfd8595c270a2532f55b71307b42c3636bba3c
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983003"
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

# <span data-ttu-id="9c819-103">DevTools pour les débutants: commencez à utiliser HTML et au DOM</span><span class="sxs-lookup"><span data-stu-id="9c819-103">DevTools for beginners: Get started with HTML and the DOM</span></span>   

<span data-ttu-id="9c819-104">Voici le premier d’une série de didacticiels pour vous apprendre les notions de base du développement Web.</span><span class="sxs-lookup"><span data-stu-id="9c819-104">This is the first in a series of tutorials that teach you the basics of web development.</span></span>  <span data-ttu-id="9c819-105">Vous découvrirez également un ensemble d’outils de développement Web, appelés Microsoft Edge DevTools, qui peuvent augmenter votre productivité.</span><span class="sxs-lookup"><span data-stu-id="9c819-105">You will also learn about a set of web developer tools called Microsoft Edge DevTools that can increase your productivity.</span></span>  

<span data-ttu-id="9c819-106">Dans ce didacticiel, vous allez découvrir HTML et le DOM.</span><span class="sxs-lookup"><span data-stu-id="9c819-106">In this particular tutorial, you learn about HTML and the DOM.</span></span>  <span data-ttu-id="9c819-107">HTML est l’une des technologies fondamentales du développement Web.</span><span class="sxs-lookup"><span data-stu-id="9c819-107">HTML is one of the core technologies of web development.</span></span>  <span data-ttu-id="9c819-108">Il s’agit de la langue qui contrôle la structure et le contenu de pages Web.</span><span class="sxs-lookup"><span data-stu-id="9c819-108">It is the language that controls the structure and content of webpages.</span></span>  <span data-ttu-id="9c819-109">Le DOM est également lié à la structure et au contenu des pages Web, mais vous en saurez plus à ce sujet plus tard.</span><span class="sxs-lookup"><span data-stu-id="9c819-109">The DOM is also related to the structure and content of webpages, but you'll learn more about that later.</span></span>  

## <span data-ttu-id="9c819-110">Définis</span><span class="sxs-lookup"><span data-stu-id="9c819-110">Goals</span></span>   

<span data-ttu-id="9c819-111">Vous allez découvrir le développement Web en créant votre propre site Web.</span><span class="sxs-lookup"><span data-stu-id="9c819-111">You are going to learn web development by actually building your own website.</span></span>  <span data-ttu-id="9c819-112">Au moment où vous effectuez tous les didacticiels de la série *devtools pour les débutants* , votre site fini se présente comme suit.</span><span class="sxs-lookup"><span data-stu-id="9c819-112">By the time you complete all of the tutorials in the *DevTools for Beginners* series, your finished site will look like in the following figure.</span></span>  

:::image type="complex" source="../media/beginners-html-finished.msft.png" alt-text="Le site terminé" lightbox="../media/beginners-html-finished.msft.png":::
   <span data-ttu-id="9c819-114">Le site terminé</span><span class="sxs-lookup"><span data-stu-id="9c819-114">The finished site</span></span>  
:::image-end:::  

<span data-ttu-id="9c819-115">À la fin de ce didacticiel, vous allez comprendre les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="9c819-115">By the end of this tutorial, you will understand:</span></span>  

*   <span data-ttu-id="9c819-116">Le code HTML et le DOM créent le contenu que vous voyez sur les pages Web.</span><span class="sxs-lookup"><span data-stu-id="9c819-116">How HTML and the DOM create the content that you see on webpages.</span></span>  
*   <span data-ttu-id="9c819-117">La façon dont Microsoft Edge DevTools peut vous aider à tester les modifications HTML et DOM.</span><span class="sxs-lookup"><span data-stu-id="9c819-117">How Microsoft Edge DevTools can help you experiment with HTML and DOM changes.</span></span>  
*   <span data-ttu-id="9c819-118">Différence entre HTML et le DOM.</span><span class="sxs-lookup"><span data-stu-id="9c819-118">The difference between HTML and the DOM.</span></span>  

<span data-ttu-id="9c819-119">Vous disposez également d’un site Web réel.</span><span class="sxs-lookup"><span data-stu-id="9c819-119">You'll also have a real website!</span></span>  <span data-ttu-id="9c819-120">Vous pouvez utiliser ce site pour héberger votre c.v. ou votre blog.</span><span class="sxs-lookup"><span data-stu-id="9c819-120">You can use this site to host your resume or blog.</span></span>  

## <span data-ttu-id="9c819-121">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="9c819-121">Prerequisites</span></span>   

<span data-ttu-id="9c819-122">Avant de suivre ce didacticiel, remplissez les conditions préalables suivantes:</span><span class="sxs-lookup"><span data-stu-id="9c819-122">Before attempting this tutorial, complete the following prerequisites:</span></span>  

*   <span data-ttu-id="9c819-123">Si vous n’êtes pas familiarisé avec le format HTML, consultez la rubrique [mise en route de HTML][MDNGettingStartedHtml].</span><span class="sxs-lookup"><span data-stu-id="9c819-123">If you are unfamiliar with HTML, read [Getting Started with HTML][MDNGettingStartedHtml].</span></span>  
*   <span data-ttu-id="9c819-124">Téléchargez le navigateur Web [Microsoft Edge][MicrosoftEdgeInsider] .</span><span class="sxs-lookup"><span data-stu-id="9c819-124">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="9c819-125">Ce didacticiel utilise un ensemble d’outils de développement Web, appelés Microsoft Edge DevTools, qui sont intégrés à Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9c819-125">This tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <span data-ttu-id="9c819-126">Configurer votre code</span><span class="sxs-lookup"><span data-stu-id="9c819-126">Set up your code</span></span>   

<span data-ttu-id="9c819-127">Vous allez créer votre site dans un éditeur de code en ligne appelé erreur.</span><span class="sxs-lookup"><span data-stu-id="9c819-127">You are going to build your site in an online code editor called Glitch.</span></span>  

1.  <span data-ttu-id="9c819-128">Ouvrez le [code source][GlitchAlluringShockIndex].</span><span class="sxs-lookup"><span data-stu-id="9c819-128">Open the [source code][GlitchAlluringShockIndex].</span></span>  <span data-ttu-id="9c819-129">Cet onglet est appelé **onglet Éditeur** tout au long de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="9c819-129">This tab will be called the **editor tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup1.msft.png" alt-text="Onglet Éditeur" lightbox="../media/beginners-html-setup1.msft.png":::
       <span data-ttu-id="9c819-131">Onglet Éditeur</span><span class="sxs-lookup"><span data-stu-id="9c819-131">The editor tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9c819-132">Cliquez sur **alluring-choc**.</span><span class="sxs-lookup"><span data-stu-id="9c819-132">Click **alluring-shock**.</span></span>  <span data-ttu-id="9c819-133">Le menu options de Project s’ouvre dans le coin supérieur gauche.</span><span class="sxs-lookup"><span data-stu-id="9c819-133">The Project Options menu opens in the top-left corner.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup2.msft.png" alt-text="Menu options de Project" lightbox="../media/beginners-html-setup2.msft.png":::
       <span data-ttu-id="9c819-135">Menu options de Project</span><span class="sxs-lookup"><span data-stu-id="9c819-135">The Project Options menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9c819-136">Cliquez sur **Remix Project**.</span><span class="sxs-lookup"><span data-stu-id="9c819-136">Click **Remix Project**.</span></span>  <span data-ttu-id="9c819-137">Le problème crée une copie du projet que vous pouvez modifier et qui génère de manière aléatoire un nouveau nom pour le projet.</span><span class="sxs-lookup"><span data-stu-id="9c819-137">Glitch creates a copy of the project that you can edit and randomly generates a new name for the project.</span></span>  <span data-ttu-id="9c819-138">Le contenu est le même qu’auparavant.</span><span class="sxs-lookup"><span data-stu-id="9c819-138">The content is the same as before.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup3.msft.png" alt-text="Le projet Remixed" lightbox="../media/beginners-html-setup3.msft.png":::
       <span data-ttu-id="9c819-140">Le projet Remixed</span><span class="sxs-lookup"><span data-stu-id="9c819-140">The remixed project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9c819-141">Si vous envisagez de terminer le didacticiel suivant de cette série, cliquez sur **se connecter** , puis connectez-vous à votre compte GitHub ou Facebook.</span><span class="sxs-lookup"><span data-stu-id="9c819-141">If you plan on completing the next tutorial in this series, click **Sign In** and sign in to Glitch with your GitHub or Facebook account.</span></span>  <span data-ttu-id="9c819-142">Si vous ne vous connectez pas, vous perdrez la possibilité de modifier ce projet une fois que vous avez fermé l’onglet modification.</span><span class="sxs-lookup"><span data-stu-id="9c819-142">If you don't sign in you will lose the ability to edit this project once you close the editing tab.</span></span>  
1.  <span data-ttu-id="9c819-143">Cliquez sur **Afficher** et sélectionnez **dans une nouvelle fenêtre**.</span><span class="sxs-lookup"><span data-stu-id="9c819-143">Click **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="9c819-144">Un nouvel onglet s’ouvre et affiche la page dynamique.</span><span class="sxs-lookup"><span data-stu-id="9c819-144">A new tab opens, showing you the live page.</span></span>  <span data-ttu-id="9c819-145">Cet onglet est appelé **onglet dynamique** tout au long de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="9c819-145">This tab will be called the **live tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup4.msft.png" alt-text="Onglet Live" lightbox="../media/beginners-html-setup4.msft.png":::
       <span data-ttu-id="9c819-147">Onglet Live</span><span class="sxs-lookup"><span data-stu-id="9c819-147">The live tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="9c819-148">Ajouter du contenu</span><span class="sxs-lookup"><span data-stu-id="9c819-148">Add content</span></span>   

<span data-ttu-id="9c819-149">Votre site est assez vide.</span><span class="sxs-lookup"><span data-stu-id="9c819-149">Your site is pretty empty.</span></span>  <span data-ttu-id="9c819-150">Pour ajouter du contenu à votre présentation, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="9c819-150">Follow the steps below to add some content to it!</span></span>  

1.  <span data-ttu-id="9c819-151">Dans l' **onglet Éditeur**, remplacez `<!-- You're "About Me" will go here.  -->` par `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="9c819-151">In the **editor tab**, replace `<!-- You're "About Me" will go here.  -->` with `<h1>About Me</h1>`.</span></span>  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add1.msft.png" alt-text="Le nouveau code est mis en surbrillance dans l’onglet Éditeur" lightbox="../media/beginners-html-add1.msft.png":::
             <span data-ttu-id="9c819-153">Le nouveau code est mis en surbrillance dans l’onglet Éditeur</span><span class="sxs-lookup"><span data-stu-id="9c819-153">The new code is highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="9c819-154">Affichez vos modifications sous l' **onglet Live**.  Le texte `About Me` est visible sur la page.</span><span class="sxs-lookup"><span data-stu-id="9c819-154">View your changes in the **live tab**.  The text `About Me` is visible on the page.</span></span>  <span data-ttu-id="9c819-155">Il est plus grand que le reste du texte, car l' `<h1>` élément représente un titre de section.</span><span class="sxs-lookup"><span data-stu-id="9c819-155">It's larger than the rest of the text, because the `<h1>` element represents a section heading.</span></span>  <span data-ttu-id="9c819-156">Dans votre navigateur Web, les titres sont automatiquement appliqués en taille de police plus grande.</span><span class="sxs-lookup"><span data-stu-id="9c819-156">Your web browser automatically styles headings in larger font sizes.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-add2.msft.png" alt-text="Le nouveau titre est affiché dans l’onglet Live" lightbox="../media/beginners-html-add2.msft.png":::
       <span data-ttu-id="9c819-158">Le nouveau titre est affiché dans l’onglet Live</span><span class="sxs-lookup"><span data-stu-id="9c819-158">The new heading is visible in the live tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9c819-159">Dans l' **onglet Éditeur**, insérez `<p>I am learning HTML.  Recent accomplishments:</p>` l’image sur la ligne en dessous de laquelle vous venez d’entrer `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="9c819-159">Back in the **editor tab**, insert `<p>I am learning HTML.  Recent accomplishments:</p>` on the line below where you just put `<h1>About Me</h1>`.</span></span>  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add3.msft.png" alt-text="Le nouveau code est mis en surbrillance dans l’onglet Éditeur" lightbox="../media/beginners-html-add3.msft.png":::
             <span data-ttu-id="9c819-161">Le nouveau code est mis en surbrillance dans l’onglet Éditeur</span><span class="sxs-lookup"><span data-stu-id="9c819-161">The new code is highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="9c819-162">Affichez votre modification sous l' **onglet Live**.</span><span class="sxs-lookup"><span data-stu-id="9c819-162">View your change in the **live tab**.</span></span>  
1.  <span data-ttu-id="9c819-163">Dans l' **onglet Éditeur**, ajoutez la liste de vos réalisations:</span><span class="sxs-lookup"><span data-stu-id="9c819-163">Back in the **editor tab**, add a list of your accomplishments:</span></span>  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add4.msft.png" alt-text="Le nouveau code est mis en surbrillance dans l’onglet Éditeur" lightbox="../media/beginners-html-add4.msft.png":::
             <span data-ttu-id="9c819-165">Le nouveau code est mis en surbrillance dans l’onglet Éditeur</span><span class="sxs-lookup"><span data-stu-id="9c819-165">The new code is highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="9c819-166">Revenez à l' **onglet Live** pour vérifier que le nouveau contenu s’affiche correctement.</span><span class="sxs-lookup"><span data-stu-id="9c819-166">Again, go back to the **live tab** to make sure that the new content is displaying correctly.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-add5.msft.png" alt-text="La nouvelle liste est affichée sous l’onglet Live" lightbox="../media/beginners-html-add5.msft.png":::
       <span data-ttu-id="9c819-168">La nouvelle liste est affichée sous l’onglet Live</span><span class="sxs-lookup"><span data-stu-id="9c819-168">The new list is visible in the live tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="9c819-169">Tester les modifications de contenu dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9c819-169">Experiment with content changes in Microsoft Edge DevTools</span></span>   

<span data-ttu-id="9c819-170">Si vous développez une grande page à l’aide d’un grand nombre de fichiers HTML, vous pouvez imaginer qu’il peut être fastidieux de reculer entre l’onglet Éditeur et l’onglet actif de centaines de fois pour voir vos modifications, en particulier si vous ne savez pas exactement ce que vous voulez faire dans la page.</span><span class="sxs-lookup"><span data-stu-id="9c819-170">If you were developing a big page with a lot of HTML, you can imagine that it might be somewhat tedious to go back-and-forth between the editor tab and the live tab hundreds of times in order to see your changes, especially if you weren't sure what exactly to put on the page.</span></span>  <span data-ttu-id="9c819-171">Microsoft Edge DevTools peut vous aider à tester du contenu sans quitter l’onglet Live.</span><span class="sxs-lookup"><span data-stu-id="9c819-171">Microsoft Edge DevTools can help you experiment with content changes without ever leaving the live tab.</span></span>  

### <span data-ttu-id="9c819-172">Différences entre le format HTML et le DOM</span><span class="sxs-lookup"><span data-stu-id="9c819-172">Learn the difference between HTML and the DOM</span></span>   

<span data-ttu-id="9c819-173">Avant de commencer à modifier votre contenu à partir de Microsoft Edge DevTools, il est utile de comprendre la différence entre le code HTML et le DOM.</span><span class="sxs-lookup"><span data-stu-id="9c819-173">Before you start editing your content from Microsoft Edge DevTools, it's helpful to understand the difference between HTML and the DOM.</span></span>  <span data-ttu-id="9c819-174">Le meilleur moyen d’apprendre est, par exemple:</span><span class="sxs-lookup"><span data-stu-id="9c819-174">The best way to learn is by example:</span></span>  

1.  <span data-ttu-id="9c819-175">Accédez à l' **onglet Live**.  Le texte s’affiche en bas de la page `A new element!?!` .</span><span class="sxs-lookup"><span data-stu-id="9c819-175">Go to the **live tab**.  At the bottom of your page you see the text `A new element!?!`.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom1.msft.png" alt-text="En bas de la page, le texte!?! un nouvel élément est visible" lightbox="../media/beginners-html-dom1.msft.png":::
       <span data-ttu-id="9c819-178">En bas de la page, le texte!?! un nouvel élément</span><span class="sxs-lookup"><span data-stu-id="9c819-178">At the bottom of the page the text A new element!?!</span></span> <span data-ttu-id="9c819-179">est visible</span><span class="sxs-lookup"><span data-stu-id="9c819-179">can be seen</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9c819-180">Revenez à l' **onglet Éditeur** et essayez de Rechercher ce texte dans `index.html` .</span><span class="sxs-lookup"><span data-stu-id="9c819-180">Go back to the **editor tab** and try to find this text in `index.html`.</span></span>  <span data-ttu-id="9c819-181">Ce n’est pas là!</span><span class="sxs-lookup"><span data-stu-id="9c819-181">It's not there!</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom2.msft.png" alt-text="Le texte du mystère est un nouvel élément!?! n’est pas disponible dans index.html" lightbox="../media/beginners-html-dom2.msft.png":::
       <span data-ttu-id="9c819-184">Le texte `A new element!?!` de mystère est introuvable dans</span><span class="sxs-lookup"><span data-stu-id="9c819-184">The mystery text `A new element!?!` is nowhere to be found in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="9c819-185">Revenez à l' **onglet Live**, cliquez avec le bouton droit `A new element!?!` , puis sélectionnez **inspecter**.</span><span class="sxs-lookup"><span data-stu-id="9c819-185">Go back to the **live tab**, right-click `A new element!?!`, and select **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom3.msft.png" alt-text="Inspecter du texte" lightbox="../media/beginners-html-dom3.msft.png":::
       <span data-ttu-id="9c819-187">Inspecter du texte</span><span class="sxs-lookup"><span data-stu-id="9c819-187">Inspecting some text</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="9c819-188">DevTools s’ouvre à côté de votre page.</span><span class="sxs-lookup"><span data-stu-id="9c819-188">DevTools opens up alongside your page.</span></span>  `<div>A new element!?!</div>` <span data-ttu-id="9c819-189">est en surbrillance bleue.</span><span class="sxs-lookup"><span data-stu-id="9c819-189">is highlighted blue.</span></span>  <span data-ttu-id="9c819-190">Même si cette structure dans DevTools ressemble à votre code HTML, il s’agit en réalité de l' **arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="9c819-190">Although this structure in DevTools looks like your HTML, it is actually the **DOM Tree**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom4.msft.png" alt-text="DevTools est ouvert parallèlement à la page" lightbox="../media/beginners-html-dom4.msft.png":::
       <span data-ttu-id="9c819-192">DevTools est ouvert parallèlement à la page</span><span class="sxs-lookup"><span data-stu-id="9c819-192">DevTools is open alongside the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="9c819-193">Lors du chargement de la page, le navigateur utilise votre code HTML pour créer le contenu *initial* de la page.</span><span class="sxs-lookup"><span data-stu-id="9c819-193">When your page loads, the browser takes your HTML to create the *initial* content of the page.</span></span>  <span data-ttu-id="9c819-194">Le DOM représente le contenu *actuel* de la page, qui peut changer au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="9c819-194">The DOM represents the *current* content of the page, which can change over time.</span></span>  <span data-ttu-id="9c819-195">Le `<div>A new element!?!</div>` contenu mystérieux est ajouté à votre page en raison de la `<script src="new.js"></script>` balise située en bas de votre code html.</span><span class="sxs-lookup"><span data-stu-id="9c819-195">The mysterious `<div>A new element!?!</div>` content is added to your page because of the `<script src="new.js"></script>` tag at the bottom of your HTML.</span></span>  <span data-ttu-id="9c819-196">Cette balise entraîne l’exécution du code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9c819-196">This tag causes some JavaScript code to run.</span></span>  <span data-ttu-id="9c819-197">En savoir plus sur JavaScript dans un didacticiel ultérieur, mais pour le considérer comme un langage de programmation qui peut changer le contenu de votre page.</span><span class="sxs-lookup"><span data-stu-id="9c819-197">You'll learn more about JavaScript in a later tutorial, but for now think of it as a programming language that can change the content of your page.</span></span>  <span data-ttu-id="9c819-198">Dans ce cas particulier, le code JavaScript est ajouté `<div>A new element!?!</div>` à votre page.</span><span class="sxs-lookup"><span data-stu-id="9c819-198">In this particular case, JavaScript code adds `<div>A new element!?!</div>` to your page.</span></span>  <span data-ttu-id="9c819-199">C’est la raison pour laquelle ce texte de mystère est visible sur votre page dynamique, mais pas dans votre code HTML.</span><span class="sxs-lookup"><span data-stu-id="9c819-199">That is why this mystery text is visible on your live page, but not in your HTML.</span></span>  

### <span data-ttu-id="9c819-200">Modifier le DOM</span><span class="sxs-lookup"><span data-stu-id="9c819-200">Edit the DOM</span></span>   

<span data-ttu-id="9c819-201">Si vous voulez tester rapidement les changements de contenu sans quitter l’onglet Live, essayez DevTools.</span><span class="sxs-lookup"><span data-stu-id="9c819-201">If you want to quickly experiment with content changes without ever leaving the live tab, try DevTools.</span></span>  

1.  <span data-ttu-id="9c819-202">Dans DevTools, cliquez avec le bouton droit, `Your site!` puis sélectionnez **modifier en HTML**.</span><span class="sxs-lookup"><span data-stu-id="9c819-202">In DevTools, right-click `Your site!` and select **Edit as HTML**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-edit1.msft.png" alt-text="Modification du nœud au format HTML" lightbox="../media/beginners-html-edit1.msft.png":::
       <span data-ttu-id="9c819-204">Modification du nœud au format HTML</span><span class="sxs-lookup"><span data-stu-id="9c819-204">Editing the node as HTML</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9c819-205">Remplacez `<p>Your site!</p>` par le code ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="9c819-205">Replace `<p>Your site!</p>` with the code below.</span></span>  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-edit2.msft.png" alt-text="Modification du nœud au format HTML" lightbox="../media/beginners-html-edit2.msft.png":::
             <span data-ttu-id="9c819-207">Modification du nœud au format HTML</span><span class="sxs-lookup"><span data-stu-id="9c819-207">Editing the node as HTML</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="9c819-208">`Control` + `Enter` `Command` + `Enter` Pour enregistrer vos modifications ou cliquez en dehors de la zone, appuyez sur \ (Windows \) ou \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="9c819-208">Press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to save your changes, or click outside of the box.</span></span>  <span data-ttu-id="9c819-209">Vos modifications apparaissent automatiquement dans le mode en direct de votre page.</span><span class="sxs-lookup"><span data-stu-id="9c819-209">Your changes automatically show up in the live view of your page.</span></span>  <span data-ttu-id="9c819-210">Le texte `Your site!` a été remplacé par le nouveau contenu.</span><span class="sxs-lookup"><span data-stu-id="9c819-210">The text `Your site!` has been replaced with the new content.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-edit3.msft.png" alt-text="Le nouveau contenu apparaît immédiatement sur la page" lightbox="../media/beginners-html-edit3.msft.png":::
       <span data-ttu-id="9c819-212">Le nouveau contenu apparaît immédiatement sur la page</span><span class="sxs-lookup"><span data-stu-id="9c819-212">The new content shows up immediately on the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="9c819-213">Ce flux de travail est uniquement utile pour tester les modifications de contenu.</span><span class="sxs-lookup"><span data-stu-id="9c819-213">This workflow is only good for experimenting with content changes.</span></span>  <span data-ttu-id="9c819-214">Si vous rechargez la page ou que vous fermez l’onglet, vos modifications sont supprimées définitivement.</span><span class="sxs-lookup"><span data-stu-id="9c819-214">If you reload the page or close the tab, your changes will be gone forever.</span></span>  <span data-ttu-id="9c819-215">Si vous utilisez ce flux de travail et que vous voulez enregistrer les modifications, vous devez les copier manuellement dans votre code HTML.</span><span class="sxs-lookup"><span data-stu-id="9c819-215">If you're using this workflow and you want to save your changes, you need to manually copy those changes over to your HTML.</span></span>  <span data-ttu-id="9c819-216">Les deux sections suivantes vous montrent davantage de moyens de changer le contenu de l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="9c819-216">The next couple of sections show you some more ways that you can change content from the DOM Tree.</span></span>  

## <span data-ttu-id="9c819-217">Réorganiser les nœuds</span><span class="sxs-lookup"><span data-stu-id="9c819-217">Reorder nodes</span></span>   

<span data-ttu-id="9c819-218">Vous pouvez également modifier l’ordre des nœuds DOM.</span><span class="sxs-lookup"><span data-stu-id="9c819-218">You can also change the order of DOM nodes.</span></span>  <span data-ttu-id="9c819-219">Par exemple, sur votre page Web, le menu de navigation est proche du bas.</span><span class="sxs-lookup"><span data-stu-id="9c819-219">For example, on your web page the navigation menu is near the bottom.</span></span>  <span data-ttu-id="9c819-220">Pour le déplacer vers le haut:</span><span class="sxs-lookup"><span data-stu-id="9c819-220">To move it to the top:</span></span>  

1.  <span data-ttu-id="9c819-221">Recherchez le `<nav>` nœud dans l' **arborescence DOM** de devtools.</span><span class="sxs-lookup"><span data-stu-id="9c819-221">Find the `<nav>` node in the **DOM Tree** of DevTools.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-reorder1.msft.png" alt-text="Le nœud de navigation est surligné en bleu dans DevTools" lightbox="../media/beginners-html-reorder1.msft.png":::
       <span data-ttu-id="9c819-223">Le nœud de navigation est surligné en bleu dans DevTools</span><span class="sxs-lookup"><span data-stu-id="9c819-223">The nav node is highlighted blue in DevTools</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9c819-224">Faites glisser le `<nav>` nœud vers le haut, de façon à ce qu’il s’agit du premier enfant sous le `<body>` nœud.</span><span class="sxs-lookup"><span data-stu-id="9c819-224">Drag the `<nav>` node to the top, so that it's the first child below the `<body>` node.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-reorder2.msft.png" alt-text="Faire glisser le nœud de navigation vers le haut" lightbox="../media/beginners-html-reorder2.msft.png":::
             <span data-ttu-id="9c819-226">Faire glisser le nœud de navigation vers le haut</span><span class="sxs-lookup"><span data-stu-id="9c819-226">Dragging the nav node to the top</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="9c819-227">Le `<nav>` nœud est désormais affiché en haut de votre page.</span><span class="sxs-lookup"><span data-stu-id="9c819-227">The `<nav>` node is now displaying at the top of your page.</span></span>  
          
          :::image type="complex" source="../media/beginners-html-reorder3.msft.png" alt-text="Le nœud de navigation est en haut de la page" lightbox="../media/beginners-html-reorder3.msft.png":::
             <span data-ttu-id="9c819-229">Le nœud de navigation est en haut de la page</span><span class="sxs-lookup"><span data-stu-id="9c819-229">The nav node is at the top of the page</span></span>  
          :::image-end:::  
       :::column-end:::
   :::row-end:::  
    
### <span data-ttu-id="9c819-230">Supprimer un nœud</span><span class="sxs-lookup"><span data-stu-id="9c819-230">Delete a node</span></span>   

<span data-ttu-id="9c819-231">Vous pouvez également supprimer des nœuds de l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="9c819-231">You can also remove nodes from the DOM Tree.</span></span>  

1.  <span data-ttu-id="9c819-232">Dans l' **arborescence DOM**, cliquez sur `<div>A new element!?!</div>` .</span><span class="sxs-lookup"><span data-stu-id="9c819-232">In the **DOM Tree**, click `<div>A new element!?!</div>`.</span></span>  <span data-ttu-id="9c819-233">DevTools surligne le nœud bleu.</span><span class="sxs-lookup"><span data-stu-id="9c819-233">DevTools highlights the node blue.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-delete1.msft.png" alt-text="Sélection du nœud à supprimer" lightbox="../media/beginners-html-delete1.msft.png":::
       <span data-ttu-id="9c819-235">Sélection du nœud à supprimer</span><span class="sxs-lookup"><span data-stu-id="9c819-235">Selecting the node to be deleted</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9c819-236">Appuyez sur la `Delete` touche de votre clavier.</span><span class="sxs-lookup"><span data-stu-id="9c819-236">Press the `Delete` key on your keyboard.</span></span>  <span data-ttu-id="9c819-237">Le `<div>A new element!?!</div>` nœud est supprimé de votre arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="9c819-237">The `<div>A new element!?!</div>` node is removed from your DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-delete2.msft.png" alt-text="Le nœud a été supprimé." lightbox="../media/beginners-html-delete2.msft.png":::
       <span data-ttu-id="9c819-239">Le nœud a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="9c819-239">The node has been deleted</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="9c819-240">Copiez vos modifications</span><span class="sxs-lookup"><span data-stu-id="9c819-240">Copy your changes</span></span>   

<span data-ttu-id="9c819-241">Vous avez presque terminé.</span><span class="sxs-lookup"><span data-stu-id="9c819-241">You're almost done.</span></span>  <span data-ttu-id="9c819-242">Vous avez apporté des modifications à votre page dans DevTools, mais celles-ci ne sont pas encore enregistrées dans votre code source.</span><span class="sxs-lookup"><span data-stu-id="9c819-242">You've made a few changes to your page in DevTools, but they're not yet saved to your source code.</span></span>  

1.  <span data-ttu-id="9c819-243">Actualisez votre **onglet actif**.  Les modifications que vous avez apportées à l’arborescence DOM disparaissent.</span><span class="sxs-lookup"><span data-stu-id="9c819-243">Refresh your **live tab**.  The changes that you made in the DOM Tree disappear.</span></span>  <span data-ttu-id="9c819-244">Par exemple, le texte `Your site!` revient en haut de la page et le texte `A new element!?!` revient en bas.</span><span class="sxs-lookup"><span data-stu-id="9c819-244">In particular, the text `Your site!` returns to the top of the page, and the text `A new element!?!` returns to the bottom.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-copy1.msft.png" alt-text="Les modifications que vous avez apportées ont disparu" lightbox="../media/beginners-html-copy1.msft.png":::
       <span data-ttu-id="9c819-246">Les modifications que vous avez apportées ont disparu</span><span class="sxs-lookup"><span data-stu-id="9c819-246">The changes that you've made are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9c819-247">Copiez le code ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="9c819-247">Copy the code below.</span></span>  
    
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
    
1.  <span data-ttu-id="9c819-248">Revenez à l' **onglet Éditeur** et remplacez le contenu de votre `index.html` fichier par le code que vous venez de copier.</span><span class="sxs-lookup"><span data-stu-id="9c819-248">Go back to the **editor tab** and replace the contents of your `index.html` file with the code that you just copied.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-copy2.msft.png" alt-text="Aspect de votre fichier index.html" lightbox="../media/beginners-html-copy2.msft.png":::
       <span data-ttu-id="9c819-250">Aspect de votre `index.html` fichier</span><span class="sxs-lookup"><span data-stu-id="9c819-250">How your `index.html` file should look</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="9c819-251">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="9c819-251">Next steps</span></span>   

*   <span data-ttu-id="9c819-252">Suivez les étapes ci-dessous pour découvrir comment appliquer un [style à votre][DevToolsBeginnersCss]page et tester les modifications de style dans Microsoft Edge devtools.</span><span class="sxs-lookup"><span data-stu-id="9c819-252">Complete the next tutorial in this series, [Get Started with CSS][DevToolsBeginnersCss], to learn how to style your page and experiment with style changes in Microsoft Edge DevTools.</span></span>  
*   <span data-ttu-id="9c819-253">Lire [Introduction au DOM][MDNIntroductionDom] pour en savoir plus sur le DOM.</span><span class="sxs-lookup"><span data-stu-id="9c819-253">Read [Introduction to the DOM][MDNIntroductionDom] to learn more about the DOM.</span></span>  
*   <span data-ttu-id="9c819-254">Consultez un cours comme [Introduction au développement Web][CourseraIntroductionToWebDevelopment] pour bénéficier d’une expérience de développement Web plus pratique.</span><span class="sxs-lookup"><span data-stu-id="9c819-254">Check out a course like [Introduction to Web Development][CourseraIntroductionToWebDevelopment] to get more hands-on web development experience.</span></span>  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools pour les débutants: prendre en main CSS | Documents Microsoft"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Présentation du développement Web | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html-alluring-choc | Problème"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Mise en route de HTML | MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introduction au DOM | MDN"  

> [!NOTE]
> <span data-ttu-id="9c819-261">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9c819-261">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9c819-262">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/beginners/html) et est créée par [Katherine Jackson][KatherineJackson] \ (Technical Writer Intern, chrome devtools \).</span><span class="sxs-lookup"><span data-stu-id="9c819-262">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/html) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="9c819-264">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9c819-264">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
