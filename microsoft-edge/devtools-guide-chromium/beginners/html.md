---
description: Prise en main html et le DOM
title: 'DevTools pour les débutants : mise en place du code HTML et du DOM'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, développement web, outils f12, devtools
ms.openlocfilehash: d2893021f5e19ffb714215b27edadba08c8d6f71
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564566"
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
# <a name="devtools-for-beginners-get-started-with-html-and-the-dom"></a><span data-ttu-id="20504-104">DevTools pour les débutants : mise en place du code HTML et du DOM</span><span class="sxs-lookup"><span data-stu-id="20504-104">DevTools for beginners: Get started with HTML and the DOM</span></span>  

<span data-ttu-id="20504-105">Il s’agit du premier d’une série de didacticiels qui vous enseignent les principes de base du développement web.</span><span class="sxs-lookup"><span data-stu-id="20504-105">This is the first in a series of tutorials that teach you the basics of web development.</span></span>  <span data-ttu-id="20504-106">Découvrez un ensemble d’outils de développement web, nommés Microsoft Edge DevTools, qui peuvent augmenter votre productivité.</span><span class="sxs-lookup"><span data-stu-id="20504-106">Learn about a set of web developer tools, named Microsoft Edge DevTools, that may increase your productivity.</span></span>  

<span data-ttu-id="20504-107">Dans ce didacticiel particulier, vous découvrirez le code HTML et le DOM.</span><span class="sxs-lookup"><span data-stu-id="20504-107">In this particular tutorial, you learn about HTML and the DOM.</span></span>  <span data-ttu-id="20504-108">HTML est l’une des technologies de base du développement web.</span><span class="sxs-lookup"><span data-stu-id="20504-108">HTML is one of the core technologies of web development.</span></span>  <span data-ttu-id="20504-109">Il s’agit du langage qui contrôle la structure et le contenu des pages web.</span><span class="sxs-lookup"><span data-stu-id="20504-109">It is the language that controls the structure and content of webpages.</span></span>  <span data-ttu-id="20504-110">Le DOM est également lié à la structure et au contenu des pages web. En savoir plus à ce sujet ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="20504-110">The DOM is also related to the structure and content of webpages, learn more about that later.</span></span>  

## <a name="goals"></a><span data-ttu-id="20504-111">Objectifs</span><span class="sxs-lookup"><span data-stu-id="20504-111">Goals</span></span>  

<span data-ttu-id="20504-112">Vous allez apprendre le développement web en construisant réellement votre propre site web.</span><span class="sxs-lookup"><span data-stu-id="20504-112">You are going to learn web development by actually building your own website.</span></span>  <span data-ttu-id="20504-113">Une fois que vous avez terminé tous les didacticiels de la série **DevTools for Beginners,** votre site terminé peut ressembler à la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="20504-113">By the time you complete all of the tutorials in the **DevTools for Beginners** series, your finished site may look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-html-finished.msft.png" alt-text="Site terminé" lightbox="../media/beginners-html-finished.msft.png":::
   <span data-ttu-id="20504-115">Site terminé</span><span class="sxs-lookup"><span data-stu-id="20504-115">The finished site</span></span>  
:::image-end:::  

<span data-ttu-id="20504-116">À la fin de ce didacticiel, vous devez comprendre les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="20504-116">By the end of this tutorial, you should understand the following topics.</span></span>  

*   <span data-ttu-id="20504-117">Comment le code HTML et le DOM créent le contenu affiché sur les pages web.</span><span class="sxs-lookup"><span data-stu-id="20504-117">How HTML and the DOM create the content that are displayed on webpages.</span></span>  
*   <span data-ttu-id="20504-118">Comment Microsoft Edge DevTools peut vous aider à expérimenter les modifications HTML et DOM.</span><span class="sxs-lookup"><span data-stu-id="20504-118">How Microsoft Edge DevTools may help you experiment with HTML and DOM changes.</span></span>  
*   <span data-ttu-id="20504-119">Différence entre le code HTML et le DOM.</span><span class="sxs-lookup"><span data-stu-id="20504-119">The difference between HTML and the DOM.</span></span>  

<span data-ttu-id="20504-120">Vous avez également un site web réel.</span><span class="sxs-lookup"><span data-stu-id="20504-120">You also have a real website.</span></span>  <span data-ttu-id="20504-121">Vous pouvez utiliser le site pour héberger votre cv ou votre blog.</span><span class="sxs-lookup"><span data-stu-id="20504-121">You may use the site to host your resume or blog.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="20504-122">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="20504-122">Prerequisites</span></span>  

<span data-ttu-id="20504-123">Avant d’essayer ce didacticiel, remplissez les conditions préalables suivantes :</span><span class="sxs-lookup"><span data-stu-id="20504-123">Before attempting this tutorial, complete the following prerequisites:</span></span>  

*   <span data-ttu-id="20504-124">Si vous ne connaissez pas le langage HTML, lisez [La mise en place du code HTML.][MDNGettingStartedHtml]</span><span class="sxs-lookup"><span data-stu-id="20504-124">If you are unfamiliar with HTML, read [Getting Started with HTML][MDNGettingStartedHtml].</span></span>  
*   <span data-ttu-id="20504-125">Téléchargez le [Microsoft Edge][MicrosoftEdgeInsider] navigateur web.</span><span class="sxs-lookup"><span data-stu-id="20504-125">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="20504-126">Ce didacticiel utilise un ensemble d’outils de développement web, appelés Microsoft Edge DevTools, qui sont intégrés Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="20504-126">This tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <a name="set-up-your-code"></a><span data-ttu-id="20504-127">Configurer votre code</span><span class="sxs-lookup"><span data-stu-id="20504-127">Set up your code</span></span>  

<span data-ttu-id="20504-128">Vous allez créer votre site dans un éditeur de code en ligne appelé Glitch.</span><span class="sxs-lookup"><span data-stu-id="20504-128">You are going to build your site in an online code editor called Glitch.</span></span>  

1.  <span data-ttu-id="20504-129">Ouvrez le [code source.][GlitchAlluringShockIndex]</span><span class="sxs-lookup"><span data-stu-id="20504-129">Open the [source code][GlitchAlluringShockIndex].</span></span>  <span data-ttu-id="20504-130">Cet onglet est appelé onglet **Éditeur tout** au long de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="20504-130">This tab is called the **editor tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup1.msft.png" alt-text="Onglet Éditeur" lightbox="../media/beginners-html-setup1.msft.png":::
       <span data-ttu-id="20504-132">Onglet Éditeur</span><span class="sxs-lookup"><span data-stu-id="20504-132">The editor tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="20504-133">Choisissez **alluring-en-préc**.</span><span class="sxs-lookup"><span data-stu-id="20504-133">Choose **alluring-shock**.</span></span>  <span data-ttu-id="20504-134">Le menu Project Options s’ouvre dans le coin supérieur gauche.</span><span class="sxs-lookup"><span data-stu-id="20504-134">The Project Options menu opens in the top-left corner.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup2.msft.png" alt-text="Menu Options Project’équipe" lightbox="../media/beginners-html-setup2.msft.png":::
       <span data-ttu-id="20504-136">Menu Options Project’équipe</span><span class="sxs-lookup"><span data-stu-id="20504-136">The Project Options menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="20504-137">Choisissez **Project**.</span><span class="sxs-lookup"><span data-stu-id="20504-137">Choose **Remix Project**.</span></span>  <span data-ttu-id="20504-138">Glitch crée une copie du projet que vous pouvez modifier et génère de manière aléatoire un nouveau nom pour le projet.</span><span class="sxs-lookup"><span data-stu-id="20504-138">Glitch creates a copy of the project that you may edit and randomly generates a new name for the project.</span></span>  <span data-ttu-id="20504-139">Le contenu est le même qu’auparavant.</span><span class="sxs-lookup"><span data-stu-id="20504-139">The content is the same as before.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup3.msft.png" alt-text="Le projet en cours" lightbox="../media/beginners-html-setup3.msft.png":::
       <span data-ttu-id="20504-141">Le projet en cours</span><span class="sxs-lookup"><span data-stu-id="20504-141">The remixed project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="20504-142">Si vous prévoyez d’effectuer le didacticiel suivant de cette série, choisissez Se connectez et connectez-vous à Glitch avec votre compte GitHub ou Facebook. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="20504-142">If you plan on completing the next tutorial in this series, choose **Sign In** and sign into Glitch with your GitHub or Facebook account.</span></span>  <span data-ttu-id="20504-143">Si vous choisissez de ne pas vous inscrire à votre compte, vous perdez la possibilité de modifier le projet après avoir fermé l’onglet Modification.</span><span class="sxs-lookup"><span data-stu-id="20504-143">If you choose to not sign into your account, you lose the ability to edit the project after you close the editing tab.</span></span>  
1.  <span data-ttu-id="20504-144">Choose **Show** and choose **In a New Window**.</span><span class="sxs-lookup"><span data-stu-id="20504-144">Choose **Show** and choose **In a New Window**.</span></span>  <span data-ttu-id="20504-145">Un nouvel onglet s’ouvre et vous montre la page en direct.</span><span class="sxs-lookup"><span data-stu-id="20504-145">A new tab opens, showing you the live page.</span></span>  <span data-ttu-id="20504-146">Cet onglet est appelé onglet **en direct tout** au long de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="20504-146">This tab is called the **live tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup4.msft.png" alt-text="Onglet en direct" lightbox="../media/beginners-html-setup4.msft.png":::
       <span data-ttu-id="20504-148">Onglet en direct</span><span class="sxs-lookup"><span data-stu-id="20504-148">The live tab</span></span>  
    :::image-end:::  
    
## <a name="add-content"></a><span data-ttu-id="20504-149">Ajouter du contenu</span><span class="sxs-lookup"><span data-stu-id="20504-149">Add content</span></span>  

<span data-ttu-id="20504-150">Votre site est assez vide.</span><span class="sxs-lookup"><span data-stu-id="20504-150">Your site is pretty empty.</span></span>  <span data-ttu-id="20504-151">Suivez les étapes ci-dessous pour y ajouter du contenu.</span><span class="sxs-lookup"><span data-stu-id="20504-151">Follow the steps below to add some content to it.</span></span>  

1.  <span data-ttu-id="20504-152">Dans **l’onglet Éditeur,** `<!-- You're "About Me" will go here.  -->` remplacez par `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="20504-152">In the **editor tab**, replace `<!-- You're "About Me" will go here.  -->` with `<h1>About Me</h1>`.</span></span>  
    
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
          :::image type="complex" source="../media/beginners-html-add1.msft.png" alt-text="Le nouveau code est mis en surbrillant dans l’onglet Éditeur" lightbox="../media/beginners-html-add1.msft.png":::
             <span data-ttu-id="20504-154">Le nouveau code est mis en surbrillant dans l’onglet Éditeur</span><span class="sxs-lookup"><span data-stu-id="20504-154">The new code is highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="20504-155">Affichez vos modifications dans **l’onglet en direct.**  Le texte `About Me` est visible sur la page.</span><span class="sxs-lookup"><span data-stu-id="20504-155">View your changes in the **live tab**.  The text `About Me` is visible on the page.</span></span>  <span data-ttu-id="20504-156">Texte plus grand que le texte qui l’entoure, car `<h1>` l’élément représente un en-tête de section.</span><span class="sxs-lookup"><span data-stu-id="20504-156">The text larger than the surrounding text, because the `<h1>` element represents a section heading.</span></span>  <span data-ttu-id="20504-157">Votre navigateur web styles automatiquement les titres dans des tailles de police plus grandes.</span><span class="sxs-lookup"><span data-stu-id="20504-157">Your web browser automatically styles headings in larger font sizes.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-add2.msft.png" alt-text="Le nouveau titre est visible dans l’onglet en direct" lightbox="../media/beginners-html-add2.msft.png":::
       <span data-ttu-id="20504-159">Le nouveau titre est visible dans l’onglet en direct</span><span class="sxs-lookup"><span data-stu-id="20504-159">The new heading is visible in the live tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="20504-160">De retour dans **l’onglet éditeur**, `<p>I am learning HTML.  Recent accomplishments:</p>` insérez sur la ligne ci-dessous où vous avez placé `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="20504-160">Back in the **editor tab**, insert `<p>I am learning HTML.  Recent accomplishments:</p>` on the line below where you just put `<h1>About Me</h1>`.</span></span>  
    
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
          :::image type="complex" source="../media/beginners-html-add3.msft.png" alt-text="Le code mis à jour est mis en surbrillant dans l’onglet Éditeur" lightbox="../media/beginners-html-add3.msft.png":::
             <span data-ttu-id="20504-162">Le code mis à jour est mis en surbrillant dans l’onglet Éditeur</span><span class="sxs-lookup"><span data-stu-id="20504-162">The updated code is highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="20504-163">Affichez votre modification dans **l’onglet en direct.**</span><span class="sxs-lookup"><span data-stu-id="20504-163">View your change in the **live tab**.</span></span>  
1.  <span data-ttu-id="20504-164">De retour dans **l’onglet Éditeur,** ajoutez une liste de vos réussites :</span><span class="sxs-lookup"><span data-stu-id="20504-164">Back in the **editor tab**, add a list of your accomplishments:</span></span>  
    
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
          :::image type="complex" source="../media/beginners-html-add4.msft.png" alt-text="Le code mis à jour est également mis en surbrillant dans l’onglet Éditeur" lightbox="../media/beginners-html-add4.msft.png":::
             <span data-ttu-id="20504-166">Le code mis à jour est également mis en surbrillant dans l’onglet Éditeur</span><span class="sxs-lookup"><span data-stu-id="20504-166">The updated code is also highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="20504-167">Là encore, revenir à **l’onglet en** direct pour vous assurer que le nouveau contenu s’affiche correctement.</span><span class="sxs-lookup"><span data-stu-id="20504-167">Again, go back to the **live tab** to make sure that the new content is displaying correctly.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-add5.msft.png" alt-text="La nouvelle liste est visible dans l’onglet en direct" lightbox="../media/beginners-html-add5.msft.png":::
       <span data-ttu-id="20504-169">La nouvelle liste est visible dans l’onglet en direct</span><span class="sxs-lookup"><span data-stu-id="20504-169">The new list is visible in the live tab</span></span>  
    :::image-end:::  
    
## <a name="experiment-with-content-changes-in-microsoft-edge-devtools"></a><span data-ttu-id="20504-170">Expérimenter les modifications de contenu dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="20504-170">Experiment with content changes in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="20504-171">Si vous développiez une grande page avec beaucoup de code HTML, il est assez fastidieux de faire des allers-retours entre l’onglet de l’éditeur et l’onglet en direct des centaines de fois pour afficher vos modifications, en particulier si vous ne savez pas exactement ce qu’il faut placer sur la page.</span><span class="sxs-lookup"><span data-stu-id="20504-171">If you were developing a big page with a lot of HTML, it is somewhat tedious to go back-and-forth between the editor tab and the live tab hundreds of times in order to display your changes, especially if you are unsure what exactly to put on the page.</span></span>  <span data-ttu-id="20504-172">Microsoft Edge DevTools vous permet d’expérimenter les modifications de contenu sans quitter **l’onglet en direct.**</span><span class="sxs-lookup"><span data-stu-id="20504-172">Microsoft Edge DevTools helps you experiment with content changes without ever leaving the **live tab**.</span></span>  

### <a name="learn-the-difference-between-html-and-the-dom"></a><span data-ttu-id="20504-173">Découvrez la différence entre le code HTML et le DOM</span><span class="sxs-lookup"><span data-stu-id="20504-173">Learn the difference between HTML and the DOM</span></span>  

<span data-ttu-id="20504-174">Avant de commencer à modifier votre contenu à partir Microsoft Edge DevTools, vous devez comprendre la différence entre HTML et le DOM.</span><span class="sxs-lookup"><span data-stu-id="20504-174">Before you start editing your content from Microsoft Edge DevTools, you should understand the difference between HTML and the DOM.</span></span>  <span data-ttu-id="20504-175">La meilleure façon d’apprendre est par exemple :</span><span class="sxs-lookup"><span data-stu-id="20504-175">The best way to learn is by example:</span></span>  

1.  <span data-ttu-id="20504-176">Accédez à **l’onglet en direct.**  Au bas de votre page, le texte `A new element!?!` s’affiche.</span><span class="sxs-lookup"><span data-stu-id="20504-176">Navigate to the **live tab**.  At the bottom of your page, the text `A new element!?!` is displayed.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom1.msft.png" alt-text="Au bas de la page, le texte A nouvel élément!?! s’affiche" lightbox="../media/beginners-html-dom1.msft.png":::
       <span data-ttu-id="20504-179">Au bas de la page, le `A new element!?!` texte s’affiche</span><span class="sxs-lookup"><span data-stu-id="20504-179">At the bottom of the page the text `A new element!?!` is displayed</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="20504-180">Revenir à **l’onglet Éditeur** et essayer de trouver le texte dans `index.html` .</span><span class="sxs-lookup"><span data-stu-id="20504-180">Go back to the **editor tab** and try to find the text in `index.html`.</span></span>  <span data-ttu-id="20504-181">Le texte n’est pas là.</span><span class="sxs-lookup"><span data-stu-id="20504-181">The text is not there.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom2.msft.png" alt-text="Texte de texte texte A nouvel élément!?! est introuvable dans index.html" lightbox="../media/beginners-html-dom2.msft.png":::
       <span data-ttu-id="20504-184">Le texte du `A new element!?!` texte de texte est introuvable dans</span><span class="sxs-lookup"><span data-stu-id="20504-184">The mystery text `A new element!?!` is nowhere to be found in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="20504-185">Revenir à **l’onglet en**direct, pointez dessus, ouvrez le menu `A new element!?!` contextuel \(clic droit\), puis choisissez **Inspecter**.</span><span class="sxs-lookup"><span data-stu-id="20504-185">Go back to the **live tab**, hover on `A new element!?!`, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom3.msft.png" alt-text="Inspection d’un texte" lightbox="../media/beginners-html-dom3.msft.png":::
       <span data-ttu-id="20504-187">Inspection d’un texte</span><span class="sxs-lookup"><span data-stu-id="20504-187">Inspecting some text</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="20504-188">DevTools s’ouvre à côté de votre page.</span><span class="sxs-lookup"><span data-stu-id="20504-188">DevTools opens up alongside your page.</span></span>  `<div>A new element!?!</div>` <span data-ttu-id="20504-189">est mis en surbrillant en bleu.</span><span class="sxs-lookup"><span data-stu-id="20504-189">is highlighted blue.</span></span>  <span data-ttu-id="20504-190">Bien que cette structure dans DevTools ressemble à votre code HTML, il s’agit en fait de l’arborescence **DOM**.</span><span class="sxs-lookup"><span data-stu-id="20504-190">Although this structure in DevTools looks like your HTML, it is actually the **DOM Tree**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom4.msft.png" alt-text="DevTools est ouvert à côté de la page" lightbox="../media/beginners-html-dom4.msft.png":::
       <span data-ttu-id="20504-192">DevTools est ouvert à côté de la page</span><span class="sxs-lookup"><span data-stu-id="20504-192">DevTools is open alongside the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="20504-193">Lorsque votre page se charge, le navigateur prend votre code HTML pour créer le *contenu initial* de la page.</span><span class="sxs-lookup"><span data-stu-id="20504-193">When your page loads, the browser takes your HTML to create the *initial* content of the page.</span></span>  <span data-ttu-id="20504-194">Le DOM représente le *contenu* actuel de la page, qui peut changer au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="20504-194">The DOM represents the *current* content of the page, which may change over time.</span></span>  <span data-ttu-id="20504-195">Le contenu exclusif est ajouté à votre page en raison de la balise en `<div>A new element!?!</div>` bas de votre code `<script src="new.js"></script>` HTML.</span><span class="sxs-lookup"><span data-stu-id="20504-195">The mysterious `<div>A new element!?!</div>` content is added to your page because of the `<script src="new.js"></script>` tag at the bottom of your HTML.</span></span>  <span data-ttu-id="20504-196">Cette balise entraîne l’exécuter du code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="20504-196">This tag causes some JavaScript code to run.</span></span>  <span data-ttu-id="20504-197">En savoir plus sur JavaScript dans un didacticiel ultérieur, mais pour l’instant, il s’agit d’un langage de programmation qui peut modifier le contenu de votre page.</span><span class="sxs-lookup"><span data-stu-id="20504-197">Learn more about JavaScript in a later tutorial, but for now think of it as a programming language that may change the content of your page.</span></span>  <span data-ttu-id="20504-198">Dans ce cas particulier, du code JavaScript `<div>A new element!?!</div>` s’ajoute à votre page.</span><span class="sxs-lookup"><span data-stu-id="20504-198">In this particular case, JavaScript code adds `<div>A new element!?!</div>` to your page.</span></span>  <span data-ttu-id="20504-199">C’est pourquoi ce texte est visible sur votre page en direct, mais pas dans votre code HTML.</span><span class="sxs-lookup"><span data-stu-id="20504-199">That is why this mystery text is visible on your live page, but not in your HTML.</span></span>  

### <a name="edit-the-dom"></a><span data-ttu-id="20504-200">Modifier le DOM</span><span class="sxs-lookup"><span data-stu-id="20504-200">Edit the DOM</span></span>  

<span data-ttu-id="20504-201">Si vous souhaitez expérimenter rapidement les modifications de contenu sans quitter l’onglet en direct, essayez DevTools.</span><span class="sxs-lookup"><span data-stu-id="20504-201">If you want to quickly experiment with content changes without ever leaving the live tab, try DevTools.</span></span>  

1.  <span data-ttu-id="20504-202">Dans DevTools, pointez sur , ouvrez le `Your site!` menu contextuel \(clic droit\), puis choisissez **Modifier au format HTML.**</span><span class="sxs-lookup"><span data-stu-id="20504-202">In DevTools, hover on `Your site!`, open the contextual menu \(right-click\), and choose **Edit as HTML**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-edit1.msft.png" alt-text="Modification du nœud au format HTML" lightbox="../media/beginners-html-edit1.msft.png":::
       <span data-ttu-id="20504-204">Modification du nœud au format HTML</span><span class="sxs-lookup"><span data-stu-id="20504-204">Editing the node as HTML</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="20504-205">Remplacez `<p>Your site!</p>` par le code ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="20504-205">Replace `<p>Your site!</p>` with the code below.</span></span>  
    
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
          :::image type="complex" source="../media/beginners-html-edit2.msft.png" alt-text="Mise à jour du nœud au format HTML" lightbox="../media/beginners-html-edit2.msft.png":::
             <span data-ttu-id="20504-207">Mise à jour du nœud au format HTML</span><span class="sxs-lookup"><span data-stu-id="20504-207">Updating the node as HTML</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="20504-208">Sélectionnez `Control` + `Enter` \(Windows, Linux\) ou `Command` + `Enter` \(macOS\) pour enregistrer vos modifications, ou choisissez en dehors de la zone.</span><span class="sxs-lookup"><span data-stu-id="20504-208">Select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\) to save your changes, or choose outside of the box.</span></span>  <span data-ttu-id="20504-209">Vos modifications s’afficheront automatiquement dans l’affichage en direct de votre page.</span><span class="sxs-lookup"><span data-stu-id="20504-209">Your changes automatically show up in the live view of your page.</span></span>  <span data-ttu-id="20504-210">Le texte `Your site!` a été remplacé par le nouveau contenu.</span><span class="sxs-lookup"><span data-stu-id="20504-210">The text `Your site!` has been replaced with the new content.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-edit3.msft.png" alt-text="Le nouveau contenu s’affiche immédiatement sur la page" lightbox="../media/beginners-html-edit3.msft.png":::
       <span data-ttu-id="20504-212">Le nouveau contenu s’affiche immédiatement sur la page</span><span class="sxs-lookup"><span data-stu-id="20504-212">The new content shows up immediately on the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="20504-213">Ce flux de travail est uniquement bon pour expérimenter les modifications de contenu.</span><span class="sxs-lookup"><span data-stu-id="20504-213">This workflow is only good for experimenting with content changes.</span></span>  <span data-ttu-id="20504-214">Si vous actualisez la page ou fermez l’onglet, vos modifications ont disparu définitivement.</span><span class="sxs-lookup"><span data-stu-id="20504-214">If you refresh the page or close the tab, your changes are gone forever.</span></span>  <span data-ttu-id="20504-215">Si vous utilisez ce flux de travail et que vous souhaitez enregistrer vos modifications, vous devez copier manuellement ces modifications dans votre code HTML.</span><span class="sxs-lookup"><span data-stu-id="20504-215">If you're using this workflow and you want to save your changes, you need to manually copy those changes over to your HTML.</span></span>  <span data-ttu-id="20504-216">Les deux sections suivantes vous montrent d’autres façons de modifier le contenu à partir de l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="20504-216">The next couple of sections show you some more ways that you may change content from the DOM Tree.</span></span>  

## <a name="reorder-nodes"></a><span data-ttu-id="20504-217">Réordons les nodes</span><span class="sxs-lookup"><span data-stu-id="20504-217">Reorder nodes</span></span>  

<span data-ttu-id="20504-218">Vous pouvez également modifier l’ordre des nodes DOM.</span><span class="sxs-lookup"><span data-stu-id="20504-218">You may also change the order of DOM nodes.</span></span>  <span data-ttu-id="20504-219">Par exemple, sur votre page web, le menu de navigation se trouve près du bas.</span><span class="sxs-lookup"><span data-stu-id="20504-219">For example, on your web page the navigation menu is near the bottom.</span></span>  <span data-ttu-id="20504-220">Pour le déplacer vers le haut :</span><span class="sxs-lookup"><span data-stu-id="20504-220">To move it to the top:</span></span>  

1.  <span data-ttu-id="20504-221">Recherchez `<nav>` le nœud dans l’arborescence **DOM** de DevTools.</span><span class="sxs-lookup"><span data-stu-id="20504-221">Find the `<nav>` node in the **DOM Tree** of DevTools.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-reorder1.msft.png" alt-text="Le nœud de navigation est mis en surbrillade en bleu dans DevTools" lightbox="../media/beginners-html-reorder1.msft.png":::
       <span data-ttu-id="20504-223">Le nœud de navigation est mis en surbrillade en bleu dans DevTools</span><span class="sxs-lookup"><span data-stu-id="20504-223">The nav node is highlighted blue in DevTools</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="20504-224">Faites glisser le nœud vers le haut, afin que le nœud soit `<nav>` le premier enfant du `<body>` nœud.</span><span class="sxs-lookup"><span data-stu-id="20504-224">Drag the `<nav>` node to the top, so that the node is the first child of the `<body>` node.</span></span>  
    
    :::row:::
       :::column span="":::
          &nbsp;  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="20504-225">Le `<nav>` nœud s’affiche maintenant en haut de votre page.</span><span class="sxs-lookup"><span data-stu-id="20504-225">The `<nav>` node is now displaying at the top of your page.</span></span>  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-reorder2.msft.png" alt-text="Faire glisser le nœud de navigation vers le haut" lightbox="../media/beginners-html-reorder2.msft.png":::
             <span data-ttu-id="20504-227">Faire glisser le nœud de navigation vers le haut</span><span class="sxs-lookup"><span data-stu-id="20504-227">Dragging the nav node to the top</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-reorder3.msft.png" alt-text="Le nœud de navigation se trouve en haut de la page" lightbox="../media/beginners-html-reorder3.msft.png":::
             <span data-ttu-id="20504-229">Le nœud de navigation se trouve en haut de la page</span><span class="sxs-lookup"><span data-stu-id="20504-229">The nav node is at the top of the page</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
### <a name="delete-a-node"></a><span data-ttu-id="20504-230">Supprimer un nœud</span><span class="sxs-lookup"><span data-stu-id="20504-230">Delete a node</span></span>  

<span data-ttu-id="20504-231">Vous pouvez également supprimer des nodes de l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="20504-231">You may also remove nodes from the DOM Tree.</span></span>  

1.  <span data-ttu-id="20504-232">Dans **l’arborescence DOM,** choisissez `<div>A new element!?!</div>` .</span><span class="sxs-lookup"><span data-stu-id="20504-232">In the **DOM Tree**, choose `<div>A new element!?!</div>`.</span></span>  <span data-ttu-id="20504-233">DevTools met en évidence le nœud bleu.</span><span class="sxs-lookup"><span data-stu-id="20504-233">DevTools highlights the node blue.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-delete1.msft.png" alt-text="Choisir le nœud à supprimer" lightbox="../media/beginners-html-delete1.msft.png":::
       <span data-ttu-id="20504-235">Choisir le nœud à supprimer</span><span class="sxs-lookup"><span data-stu-id="20504-235">Choose the node to be deleted</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="20504-236">Sélectionnez `Delete` la touche de votre clavier.</span><span class="sxs-lookup"><span data-stu-id="20504-236">Select the `Delete` key on your keyboard.</span></span>  <span data-ttu-id="20504-237">Le `<div>A new element!?!</div>` nœud est supprimé de votre arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="20504-237">The `<div>A new element!?!</div>` node is removed from your DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-delete2.msft.png" alt-text="Le nœud a été supprimé" lightbox="../media/beginners-html-delete2.msft.png":::
       <span data-ttu-id="20504-239">Le nœud a été supprimé</span><span class="sxs-lookup"><span data-stu-id="20504-239">The node has been deleted</span></span>  
    :::image-end:::  
    
## <a name="copy-your-changes"></a><span data-ttu-id="20504-240">Copier vos modifications</span><span class="sxs-lookup"><span data-stu-id="20504-240">Copy your changes</span></span>  

<span data-ttu-id="20504-241">Vous avez presque terminé.</span><span class="sxs-lookup"><span data-stu-id="20504-241">You're almost done.</span></span>  <span data-ttu-id="20504-242">Vous avez apporté quelques modifications à votre page dans DevTools, mais elles ne sont pas encore enregistrées dans votre code source.</span><span class="sxs-lookup"><span data-stu-id="20504-242">You've made a few changes to your page in DevTools, but they're not yet saved to your source code.</span></span>  

1.  <span data-ttu-id="20504-243">Actualisez **votre onglet en direct.**  Les modifications que vous avez apportées dans l’arborescence DOM disparaissent.</span><span class="sxs-lookup"><span data-stu-id="20504-243">Refresh your **live tab**.  The changes that you made in the DOM Tree disappear.</span></span>  <span data-ttu-id="20504-244">En particulier, le texte revient en haut de `Your site!` la page et le texte revient en `A new element!?!` bas.</span><span class="sxs-lookup"><span data-stu-id="20504-244">In particular, the text `Your site!` returns to the top of the page, and the text `A new element!?!` returns to the bottom.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-copy1.msft.png" alt-text="Les modifications que vous avez apportées ont disparu" lightbox="../media/beginners-html-copy1.msft.png":::
       <span data-ttu-id="20504-246">Les modifications que vous avez apportées ont disparu</span><span class="sxs-lookup"><span data-stu-id="20504-246">The changes that you've made are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="20504-247">Copiez le code ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="20504-247">Copy the code below.</span></span>  
    
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
    
1.  <span data-ttu-id="20504-248">Revenir à **l’onglet Éditeur** et remplacer le contenu de votre fichier par le code que vous `index.html` viennent de copier.</span><span class="sxs-lookup"><span data-stu-id="20504-248">Go back to the **editor tab** and replace the contents of your `index.html` file with the code that you just copied.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-copy2.msft.png" alt-text="Apparence de index.htmfichier l" lightbox="../media/beginners-html-copy2.msft.png":::
       <span data-ttu-id="20504-250">Apparence `index.html` de votre fichier</span><span class="sxs-lookup"><span data-stu-id="20504-250">How your `index.html` file should look</span></span>  
    :::image-end:::  
    
## <a name="next-steps"></a><span data-ttu-id="20504-251">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="20504-251">Next steps</span></span>  

*   <span data-ttu-id="20504-252">Complétez le didacticiel suivant de cette série, [Prise en main avec CSS,][DevToolsBeginnersCss]pour apprendre à styler votre page et expérimenter les modifications de style dans Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="20504-252">Complete the next tutorial in this series, [Get Started with CSS][DevToolsBeginnersCss], to learn how to style your page and experiment with style changes in Microsoft Edge DevTools.</span></span>  
*   <span data-ttu-id="20504-253">Lisez [l’introduction au DOM][MDNIntroductionDom] pour en savoir plus sur le DOM.</span><span class="sxs-lookup"><span data-stu-id="20504-253">Read [Introduction to the DOM][MDNIntroductionDom] to learn more about the DOM.</span></span>  
*   <span data-ttu-id="20504-254">Consultez un cours comme [Introduction au développement Web][CourseraIntroductionToWebDevelopment] pour obtenir une expérience de développement web plus pratique.</span><span class="sxs-lookup"><span data-stu-id="20504-254">Check out a course like [Introduction to Web Development][CourseraIntroductionToWebDevelopment] to get more hands-on web development experience.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="20504-255">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="20504-255">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools pour les débutants : Prise en main avec CSS | Documents Microsoft"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Présentation des outils de | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html - alluring-| Glitch"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Mise en place des | HTML MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Présentation de la | DOM MDN"  

> [!NOTE]
> <span data-ttu-id="20504-262">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="20504-262">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="20504-263">La page d’origine a été [trouvée ici](https://developers.google.com/web/tools/chrome-devtools/beginners/html) et a été co-auteure par [Le rédacteur technique Principal \(Interne][KatherineJackson] au rédacteur technique, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="20504-263">The original page was found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/html) and was authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="20504-265">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="20504-265">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors  
