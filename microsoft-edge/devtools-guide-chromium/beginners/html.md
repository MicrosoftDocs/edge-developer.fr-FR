---
description: Prise en main html et le DOM
title: 'DevTools pour les débutants : mise en place du code HTML et du DOM'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/01/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, développement web, outils f12, devtools, devtools pour les débutants, devtools HTML pour les débutants, devtools DOM pour les débutants, didacticiel html devtools, didacticiel DOM devtools, didacticiel de modèle objet de document devtools
ms.openlocfilehash: a049ec500e22f89db3ab1e966b55d89c2ad682fe
ms.sourcegitcommit: 8f37c931ecde4d58223113f7e3b42d37cc3df97f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/10/2021
ms.locfileid: "11643492"
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
# <a name="devtools-for-beginners-get-started-with-html-and-the-dom"></a><span data-ttu-id="f8367-104">DevTools pour les débutants : mise en place du code HTML et du DOM</span><span class="sxs-lookup"><span data-stu-id="f8367-104">DevTools for beginners: Get started with HTML and the DOM</span></span>  

<span data-ttu-id="f8367-105">Il s’agit du premier d’une série de didacticiels qui vous enseignent les principes de base du développement web.</span><span class="sxs-lookup"><span data-stu-id="f8367-105">This is the first in a series of tutorials that teach you the basics of web development.</span></span> <span data-ttu-id="f8367-106">Découvrez un ensemble d’outils de développement web, nommés Microsoft Edge DevTools, qui peuvent augmenter votre productivité.</span><span class="sxs-lookup"><span data-stu-id="f8367-106">Learn about a set of web developer tools, named Microsoft Edge DevTools, that may increase your productivity.</span></span>  

<span data-ttu-id="f8367-107">Ce didacticiel décrit le code HTML et le [modèle objet document](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) \(DOM\).</span><span class="sxs-lookup"><span data-stu-id="f8367-107">This tutorial describes HTML and the [Document Object Model](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) \(DOM\).</span></span> <span data-ttu-id="f8367-108">HTML est l’une des technologies de base du développement web.</span><span class="sxs-lookup"><span data-stu-id="f8367-108">HTML is one of the core technologies of web development.</span></span> <span data-ttu-id="f8367-109">Il s’agit du langage qui contrôle la structure et le contenu des pages web.</span><span class="sxs-lookup"><span data-stu-id="f8367-109">It is the language that controls the structure and content of webpages.</span></span> <span data-ttu-id="f8367-110">Le DOM est également lié à la structure et au contenu des pages web, dont nous en apprendreons plus plus ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="f8367-110">The DOM is also related to the structure and content of webpages, which we learn more about later.</span></span>

## <a name="goals"></a><span data-ttu-id="f8367-111">Objectifs</span><span class="sxs-lookup"><span data-stu-id="f8367-111">Goals</span></span>  

<span data-ttu-id="f8367-112">Vous allez apprendre le développement web en construisant un site web.</span><span class="sxs-lookup"><span data-stu-id="f8367-112">You're going to learn web development by building a website.</span></span>  <span data-ttu-id="f8367-113">Une fois que vous avez terminé tous les didacticiels de la série **DevTools for Beginners,** votre site terminé peut ressembler à la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="f8367-113">By the time you complete all of the tutorials in the **DevTools for Beginners** series, your finished site may look like the following figure.</span></span>  

:::image type="complex" source="media/beginners-html-finished.msft.png" alt-text="Site terminé" lightbox="media/beginners-html-finished.msft.png":::
   <span data-ttu-id="f8367-115">Site terminé</span><span class="sxs-lookup"><span data-stu-id="f8367-115">The finished site</span></span>  
:::image-end:::  

<span data-ttu-id="f8367-116">À la fin de ce didacticiel, vous devez comprendre les concepts suivants.</span><span class="sxs-lookup"><span data-stu-id="f8367-116">By the end of this tutorial, you should understand the following concepts.</span></span>  

*   <span data-ttu-id="f8367-117">Comment le code HTML et le DOM créent le contenu affiché sur les pages web.</span><span class="sxs-lookup"><span data-stu-id="f8367-117">How HTML and the DOM create the content displayed on webpages.</span></span>  
*   <span data-ttu-id="f8367-118">Comment Microsoft Edge DevTools peut vous aider à expérimenter les modifications HTML et DOM.</span><span class="sxs-lookup"><span data-stu-id="f8367-118">How Microsoft Edge DevTools may help you experiment with HTML and DOM changes.</span></span>  
*   <span data-ttu-id="f8367-119">Différence entre le code HTML et le DOM.</span><span class="sxs-lookup"><span data-stu-id="f8367-119">The difference between HTML and the DOM.</span></span>  

<span data-ttu-id="f8367-120">Vous aurez également un site web de travail.</span><span class="sxs-lookup"><span data-stu-id="f8367-120">You will also have a working website.</span></span> <span data-ttu-id="f8367-121">Vous pouvez utiliser le site pour héberger votre cv ou votre blog.</span><span class="sxs-lookup"><span data-stu-id="f8367-121">You may use the site to host your resume or blog.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="f8367-122">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="f8367-122">Prerequisites</span></span>  

<span data-ttu-id="f8367-123">Avant d’essayer ce didacticiel, remplissez les conditions préalables suivantes :</span><span class="sxs-lookup"><span data-stu-id="f8367-123">Before attempting this tutorial, complete the following prerequisites:</span></span>  

*   <span data-ttu-id="f8367-124">Si vous ne connaissez pas le langage HTML, lisez [La mise en place du code HTML.][MDNGettingStartedHtml]</span><span class="sxs-lookup"><span data-stu-id="f8367-124">If you are unfamiliar with HTML, read [Getting Started with HTML][MDNGettingStartedHtml].</span></span>  
*   <span data-ttu-id="f8367-125">Téléchargez le [Microsoft Edge][MicrosoftEdgeInsider] navigateur web.</span><span class="sxs-lookup"><span data-stu-id="f8367-125">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="f8367-126">Ce didacticiel utilise un ensemble d’outils de développement web, appelés Microsoft Edge DevTools, qui sont intégrés Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f8367-126">This tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <a name="set-up-your-code"></a><span data-ttu-id="f8367-127">Configurer votre code</span><span class="sxs-lookup"><span data-stu-id="f8367-127">Set up your code</span></span>  

<span data-ttu-id="f8367-128">Vous allez créer un site dans l’éditeur de code Glitch Online.</span><span class="sxs-lookup"><span data-stu-id="f8367-128">You are going to build a site in the Glitch online code editor.</span></span>  

1.  <span data-ttu-id="f8367-129">Ouvrez le [code source.][GlitchAlluringShockIndex]</span><span class="sxs-lookup"><span data-stu-id="f8367-129">Open the [source code][GlitchAlluringShockIndex].</span></span> <span data-ttu-id="f8367-130">Cet onglet est appelé onglet **Éditeur tout** au long de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="f8367-130">This tab is called the **editor tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="media/beginners-html-setup1.msft.png" alt-text="Onglet Éditeur" lightbox="media/beginners-html-setup1.msft.png":::
       <span data-ttu-id="f8367-132">Onglet Éditeur</span><span class="sxs-lookup"><span data-stu-id="f8367-132">The editor tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f8367-133">Choisissez **alluring-en-préc**.</span><span class="sxs-lookup"><span data-stu-id="f8367-133">Choose **alluring-shock**.</span></span> <span data-ttu-id="f8367-134">Le menu **Project Options** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="f8367-134">The **Project Options** menu opens.</span></span>  
    
    :::image type="complex" source="media/beginners-html-setup2.msft.png" alt-text="Menu Options Project’équipe" lightbox="media/beginners-html-setup2.msft.png":::
       <span data-ttu-id="f8367-136">Menu Options Project’équipe</span><span class="sxs-lookup"><span data-stu-id="f8367-136">The Project Options menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f8367-137">Choisissez **Project**.</span><span class="sxs-lookup"><span data-stu-id="f8367-137">Choose **Remix Project**.</span></span> <span data-ttu-id="f8367-138">Glitch crée une copie du projet que vous pouvez modifier et génère de manière aléatoire un nouveau nom pour le projet.</span><span class="sxs-lookup"><span data-stu-id="f8367-138">Glitch creates a copy of the project that you may edit and randomly generates a new name for the project.</span></span> <span data-ttu-id="f8367-139">Le contenu est le même qu’auparavant.</span><span class="sxs-lookup"><span data-stu-id="f8367-139">The content is the same as before.</span></span>  
    
    :::image type="complex" source="media/beginners-html-setup3.msft.png" alt-text="Le projet en cours" lightbox="media/beginners-html-setup3.msft.png":::
       <span data-ttu-id="f8367-141">Le projet en cours</span><span class="sxs-lookup"><span data-stu-id="f8367-141">The remixed project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f8367-142">Si vous prévoyez d’effectuer le didacticiel suivant de cette série, choisissez **Sign In** to Glitch using your Facebook, GitHub, or Google account; ou envoyez-vous un lien magique par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="f8367-142">If you plan to complete the next tutorial in this series, choose **Sign In** to Glitch using your Facebook, GitHub, or Google account; or email yourself a magic link.</span></span> <span data-ttu-id="f8367-143">Si vous choisissez de ne pas vous inscrire à un compte, vous ne pouvez pas modifier le projet après avoir fermé l’onglet Éditeur.</span><span class="sxs-lookup"><span data-stu-id="f8367-143">If you choose not to sign in to an account, you cannot edit the project after closing the editor tab.</span></span>

1.  <span data-ttu-id="f8367-144">Choisissez **Afficher**  \>  **dans une nouvelle fenêtre.**</span><span class="sxs-lookup"><span data-stu-id="f8367-144">Choose **Show** \> **In a New Window**.</span></span>  <span data-ttu-id="f8367-145">Un nouvel onglet s’ouvre et affiche la page en direct.</span><span class="sxs-lookup"><span data-stu-id="f8367-145">A new tab opens, showing the live page.</span></span> <span data-ttu-id="f8367-146">Cet onglet est appelé onglet **en direct tout** au long de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="f8367-146">This tab is called the **live tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="media/beginners-html-setup4.msft.png" alt-text="Onglet en direct" lightbox="media/beginners-html-setup4.msft.png":::
       <span data-ttu-id="f8367-148">Onglet en direct</span><span class="sxs-lookup"><span data-stu-id="f8367-148">The live tab</span></span>  
    :::image-end:::  
    
## <a name="add-content"></a><span data-ttu-id="f8367-149">Ajouter du contenu</span><span class="sxs-lookup"><span data-stu-id="f8367-149">Add content</span></span>  

<span data-ttu-id="f8367-150">Votre site a besoin d’informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="f8367-150">Your site needs more information.</span></span> <span data-ttu-id="f8367-151">Pour ajouter du contenu, complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="f8367-151">Complete the following steps to add some content.</span></span>  

1. <span data-ttu-id="f8367-152">Dans **l’onglet Éditeur,** `<!-- You're "About Me" will go here.  -->` remplacez par `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="f8367-152">In the **editor tab**, replace `<!-- You're "About Me" will go here.  -->` with `<h1>About Me</h1>`.</span></span>  
    
    ```html
        ...
        <body>
            <p> Your site!</p>
                <main>
                    <h1>About Me</h1>
                </main>
        ...
    ```  
    
    :::image type="complex" source="media/beginners-html-add1.msft.png" alt-text="Le nouveau code est mis en surbrillant dans l’onglet Éditeur" lightbox="media/beginners-html-add1.msft.png":::
        <span data-ttu-id="f8367-154">Le nouveau code est mis en surbrillant dans l’onglet Éditeur</span><span class="sxs-lookup"><span data-stu-id="f8367-154">The new code is highlighted in the editor tab</span></span>  
    :::image-end:::  
    
1. <span data-ttu-id="f8367-155">Affichez vos modifications dans **l’onglet en direct.** Le texte `About Me` est visible sur la page.</span><span class="sxs-lookup"><span data-stu-id="f8367-155">View your changes in the **live tab**. The text `About Me` is visible on the page.</span></span> <span data-ttu-id="f8367-156">Le texte est plus grand que le texte qui l’entoure, car `<h1>` l’élément représente un titre 1.</span><span class="sxs-lookup"><span data-stu-id="f8367-156">The text is larger than the surrounding text because the `<h1>` element represents a Heading 1.</span></span>  <span data-ttu-id="f8367-157">Votre navigateur web styles automatiquement les titres dans des tailles de police plus grandes.</span><span class="sxs-lookup"><span data-stu-id="f8367-157">Your web browser automatically styles headings in larger font sizes.</span></span>  
    
    :::image type="complex" source="media/beginners-html-add2.msft.png" alt-text="Le nouveau titre est visible dans l’onglet en direct" lightbox="media/beginners-html-add2.msft.png":::
       <span data-ttu-id="f8367-159">Le nouveau titre est visible dans l’onglet en direct</span><span class="sxs-lookup"><span data-stu-id="f8367-159">The new heading is visible in the live tab</span></span>  
    :::image-end:::  
    
1. <span data-ttu-id="f8367-160">De retour dans **l’onglet Éditeur**, `<p>I am learning web development. Recent accomplishments:</p>` insérez sur la ligne  `<h1>About Me</h1>` ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="f8367-160">Back in the **editor tab**, insert `<p>I am learning web development. Recent accomplishments:</p>` on the line below  `<h1>About Me</h1>`.</span></span>  
    
    ```html
    ...
        <body>
            <p> Your site!</p>
                <main>
                    <h1>About Me</h1>
                    <p>I am learning web development. Recent accomplishments:</p>
                </main>
    ...
    ```  

    :::image type="complex" source="media/beginners-html-add3.msft.png" alt-text="Le code mis à jour est mis en surbrillant dans l’onglet Éditeur" lightbox="media/beginners-html-add3.msft.png":::
        <span data-ttu-id="f8367-162">Le code mis à jour est mis en surbrillant dans l’onglet Éditeur</span><span class="sxs-lookup"><span data-stu-id="f8367-162">The updated code is highlighted in the editor tab</span></span>  
    :::image-end:::  
    
1. <span data-ttu-id="f8367-163">Affichez votre modification dans **l’onglet en direct.**</span><span class="sxs-lookup"><span data-stu-id="f8367-163">View your change in the **live tab**.</span></span>

1. <span data-ttu-id="f8367-164">Dans **l’onglet Éditeur,** ajoutez une liste de vos réussites à l’aide du code suivant.</span><span class="sxs-lookup"><span data-stu-id="f8367-164">Back in the **editor tab**, add a list of your accomplishments using the following code.</span></span>
    
    ```html
    ...
    <p>I am learning web development.  Recent accomplishments:</p>
        <ul>
            <li>Learned how to set up my code in Glitch.</li>
            <li>Added content to my HTML.</li>
            <li>TODO: Learn how to use Microsoft Edge DevTools to experiment with content changes.</li>
            <li>TODO: Learn the difference between HTML and the DOM.</li>
        </ul>
    ...
    ```  

    :::image type="complex" source="media/beginners-html-add4.msft.png" alt-text="Le code mis à jour est également mis en surbrillant dans l’onglet Éditeur" lightbox="media/beginners-html-add4.msft.png":::
        <span data-ttu-id="f8367-166">Le code mis à jour est également mis en surbrillant dans l’onglet Éditeur</span><span class="sxs-lookup"><span data-stu-id="f8367-166">The updated code is also highlighted in the editor tab</span></span>  
    :::image-end:::  

1. <span data-ttu-id="f8367-167">Affichez **l’onglet** en direct pour vous assurer que le nouveau contenu s’affiche correctement.</span><span class="sxs-lookup"><span data-stu-id="f8367-167">View the **live tab** to make sure that the new content displays correctly.</span></span>  
    
    :::image type="complex" source="media/beginners-html-add5.msft.png" alt-text="La nouvelle liste est visible dans l’onglet en direct" lightbox="media/beginners-html-add5.msft.png":::
       <span data-ttu-id="f8367-169">La nouvelle liste est visible dans l’onglet en direct</span><span class="sxs-lookup"><span data-stu-id="f8367-169">The new list is visible in the live tab</span></span>  
    :::image-end:::  
    
## <a name="experiment-with-content-changes-in-microsoft-edge-devtools"></a><span data-ttu-id="f8367-170">Expérimenter les modifications de contenu dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f8367-170">Experiment with content changes in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="f8367-171">Si vous développez une page avec beaucoup de code HTML, il devient fastidieux de faire des allers-retours entre l’onglet éditeur et l’onglet en direct pour voir vos modifications.</span><span class="sxs-lookup"><span data-stu-id="f8367-171">If you are developing a page with a lot of HTML, it becomes tedious to go back-and-forth between the editor tab and the live tab to see your changes.</span></span> <span data-ttu-id="f8367-172">Microsoft Edge DevTools vous permet d’expérimenter les modifications de contenu sans quitter **l’onglet en direct.**</span><span class="sxs-lookup"><span data-stu-id="f8367-172">Microsoft Edge DevTools helps you experiment with content changes without ever leaving the **live tab**.</span></span>  

### <a name="learn-the-difference-between-html-and-the-dom"></a><span data-ttu-id="f8367-173">Découvrez la différence entre le code HTML et le DOM</span><span class="sxs-lookup"><span data-stu-id="f8367-173">Learn the difference between HTML and the DOM</span></span>  

<span data-ttu-id="f8367-174">Avant de modifier le contenu Microsoft Edge DevTools, nous allons comprendre la différence entre html et DOM.</span><span class="sxs-lookup"><span data-stu-id="f8367-174">Before editing content from Microsoft Edge DevTools, let's understand the difference between HTML and the DOM.</span></span> <span data-ttu-id="f8367-175">Procédez comme suit pour apprendre à partir d’un exemple.</span><span class="sxs-lookup"><span data-stu-id="f8367-175">Proceed with the following steps to learn from an example.</span></span>

1. <span data-ttu-id="f8367-176">Accédez à **l’onglet en direct.** Au bas de votre page, le texte `A new element!?!` s’affiche.</span><span class="sxs-lookup"><span data-stu-id="f8367-176">Navigate to the **live tab**. At the bottom of your page, the text `A new element!?!` displays.</span></span>  

    <!--
        :::image type="complex" source="media/beginners-html-dom1.msft.png" alt-text="At the bottom of the page the text A new element!?! displays" lightbox="media/beginners-html-dom1.msft.png":::
        At the bottom of the page the text `A new element!?!` is displays  
        :::image-end:::
    -->
    
1. <span data-ttu-id="f8367-177">Ouvrez **l’onglet** Éditeur et essayez de trouver le texte dans `index.html` .</span><span class="sxs-lookup"><span data-stu-id="f8367-177">Open the **editor tab** and try to find the text in `index.html`.</span></span> <span data-ttu-id="f8367-178">Le texte ne s’affiche pas dans cet affichage.</span><span class="sxs-lookup"><span data-stu-id="f8367-178">The text does not display in this view.</span></span>  

    <!--
        :::image type="complex" source="media/beginners-html-dom2.msft.png" alt-text="The mystery text A new element!?! is not found in index.html" lightbox="media/beginners-html-dom2.msft.png":::
        The mystery text `A new element!?!` is not found in `index.html`  
        :::image-end:::
    -->

1. <span data-ttu-id="f8367-179">Ouvrez **l’onglet en**direct, pointez `A new element!?!` dessus, ouvrez le menu contextuel (clic droit), puis choisissez **Inspecter**.</span><span class="sxs-lookup"><span data-stu-id="f8367-179">Open the **live tab**, hover over `A new element!?!`, open the contextual menu (right-click) and then choose **Inspect**.</span></span>  
    
    :::image type="complex" source="media/beginners-html-dom3.msft.png" alt-text="Inspection d’un texte" lightbox="media/beginners-html-dom3.msft.png":::
       <span data-ttu-id="f8367-181">Inspection d’un texte</span><span class="sxs-lookup"><span data-stu-id="f8367-181">Inspecting some text</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="f8367-182">DevTools s’ouvre à côté de votre page.</span><span class="sxs-lookup"><span data-stu-id="f8367-182">DevTools opens up alongside your page.</span></span> `<div>A new element!?!</div>` <span data-ttu-id="f8367-183">est mis en surbrillant.</span><span class="sxs-lookup"><span data-stu-id="f8367-183">is highlighted.</span></span> <span data-ttu-id="f8367-184">Bien que cette structure dans DevTools ressemble à du code HTML, il s’agit de **l’arborescence DOM**.</span><span class="sxs-lookup"><span data-stu-id="f8367-184">Although this structure in DevTools looks like HTML, it is the **DOM Tree**.</span></span>  
    
    :::image type="complex" source="media/beginners-html-dom4.msft.png" alt-text="DevTools est ouvert à côté de la page" lightbox="media/beginners-html-dom4.msft.png":::
       <span data-ttu-id="f8367-186">DevTools est ouvert à côté de la page</span><span class="sxs-lookup"><span data-stu-id="f8367-186">DevTools is open alongside the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="f8367-187">Lorsque votre page se charge, le navigateur utilise le code HTML pour créer le contenu initial de la page.</span><span class="sxs-lookup"><span data-stu-id="f8367-187">When your page loads, the browser uses the HTML to create the initial content of the page.</span></span> <span data-ttu-id="f8367-188">Le DOM représente le contenu actuel de la page, qui peut changer au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="f8367-188">The DOM represents the current content of the page, which may change over time.</span></span> 

<span data-ttu-id="f8367-189">Le contenu est ajouté à votre page en raison de `<div>A new element!?!</div>` la balise en bas de votre code `<script src="new.js"></script>` HTML.</span><span class="sxs-lookup"><span data-stu-id="f8367-189">The `<div>A new element!?!</div>` content is added to your page because of the `<script src="new.js"></script>` tag at the bottom of your HTML.</span></span> <span data-ttu-id="f8367-190">Cette balise entraîne l’exécuter du code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f8367-190">This tag causes some JavaScript code to run.</span></span> <span data-ttu-id="f8367-191">En savoir plus sur JavaScript dans un [didacticiel ultérieur.](../javascript/index.md)</span><span class="sxs-lookup"><span data-stu-id="f8367-191">Learn more about JavaScript in a [later tutorial](../javascript/index.md).</span></span>

<span data-ttu-id="f8367-192">Pour l’instant, il s’agit d’un langage de script qui peut modifier le contenu de votre page.</span><span class="sxs-lookup"><span data-stu-id="f8367-192">For now, think of it as a scripting language that may change the content of your page.</span></span> <span data-ttu-id="f8367-193">Dans ce cas, du code JavaScript `<div>A new element!?!</div>` s’ajoute à votre page.</span><span class="sxs-lookup"><span data-stu-id="f8367-193">In this case, JavaScript code adds `<div>A new element!?!</div>` to your page.</span></span> <span data-ttu-id="f8367-194">C’est pourquoi ce texte est affiché dans l’onglet **en** direct, mais pas dans le code HTML.</span><span class="sxs-lookup"><span data-stu-id="f8367-194">That is why this text is displayed in the **live** tab, but not in the HTML.</span></span>  

### <a name="edit-the-dom"></a><span data-ttu-id="f8367-195">Modifier le DOM</span><span class="sxs-lookup"><span data-stu-id="f8367-195">Edit the DOM</span></span>  

<span data-ttu-id="f8367-196">Si vous souhaitez expérimenter rapidement les modifications de contenu sans quitter l’onglet en direct, essayez DevTools.</span><span class="sxs-lookup"><span data-stu-id="f8367-196">If you want to quickly experiment with content changes without ever leaving the live tab, try DevTools.</span></span>  

1.  <span data-ttu-id="f8367-197">Dans DevTools, pointez sur , ouvrez le menu contextuel (clic droit) et choisissez `Your site!` Modifier au format **HTML.**</span><span class="sxs-lookup"><span data-stu-id="f8367-197">In DevTools, hover over `Your site!`, open the contextual menu (right-click) and choose **Edit as HTML**.</span></span>  
    
1.  <span data-ttu-id="f8367-198">Remplacez `<p>Your site!</p>` par le code suivant.</span><span class="sxs-lookup"><span data-stu-id="f8367-198">Replace `<p>Your site!</p>` with the following code.</span></span>  

```html
    ...
    <header>
        <p><b>Welcome to my site!</b></p>
        <button>Download my resume</button>
    </header>
    ...
```  

:::image type="complex" source="media/beginners-html-edit2.msft.png" alt-text="Mise à jour du nœud au format HTML" lightbox="media/beginners-html-edit2.msft.png":::
    <span data-ttu-id="f8367-200">Mise à jour du nœud au format HTML</span><span class="sxs-lookup"><span data-stu-id="f8367-200">Updating the node as HTML</span></span>  
<span data-ttu-id="f8367-201">::image-end:::</span><span class="sxs-lookup"><span data-stu-id="f8367-201">::image-end:::</span></span>  

1.  <span data-ttu-id="f8367-202">Sélectionnez `Control` + `Enter` \(Windows, Linux\) ou `Command` + `Enter` \(macOS\) pour enregistrer vos modifications, ou sélectionnez en dehors de la zone.</span><span class="sxs-lookup"><span data-stu-id="f8367-202">Select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\) to save your changes, or select outside the box.</span></span> <span data-ttu-id="f8367-203">Vos modifications s’afficheront automatiquement dans l’affichage en direct de votre page.</span><span class="sxs-lookup"><span data-stu-id="f8367-203">Your changes automatically show up in the live view of your page.</span></span> <span data-ttu-id="f8367-204">Le texte `Your site!` a été remplacé par le nouveau contenu.</span><span class="sxs-lookup"><span data-stu-id="f8367-204">The text `Your site!` has been replaced with the new content.</span></span>  
    
    :::image type="complex" source="media/beginners-html-edit3.msft.png" alt-text="Le nouveau contenu s’affiche immédiatement sur la page" lightbox="media/beginners-html-edit3.msft.png":::
       <span data-ttu-id="f8367-206">Le nouveau contenu s’affiche immédiatement sur la page</span><span class="sxs-lookup"><span data-stu-id="f8367-206">The new content shows up immediately on the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="f8367-207">Ce flux de travail convient uniquement pour expérimenter les modifications de contenu.</span><span class="sxs-lookup"><span data-stu-id="f8367-207">This workflow is only suitable for experimenting with content changes.</span></span> <span data-ttu-id="f8367-208">Si vous actualisez la page ou fermez l’onglet, vos modifications sont perdues.</span><span class="sxs-lookup"><span data-stu-id="f8367-208">If you refresh the page or close the tab, your changes are lost.</span></span> <span data-ttu-id="f8367-209">Si vous souhaitez enregistrer vos modifications, copiez manuellement le code dans votre fichier HTML.</span><span class="sxs-lookup"><span data-stu-id="f8367-209">If you want to save your changes, manually copy the code to your HTML file.</span></span> <span data-ttu-id="f8367-210">Les deux sections suivantes vous montrent d’autres façons de modifier le contenu de l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="f8367-210">The next couple of sections show you some more ways to change content from the DOM Tree.</span></span>  

## <a name="reorder-nodes"></a><span data-ttu-id="f8367-211">Réordons les nodes</span><span class="sxs-lookup"><span data-stu-id="f8367-211">Reorder nodes</span></span>

<span data-ttu-id="f8367-212">Vous pouvez également modifier l’ordre des nodes DOM.</span><span class="sxs-lookup"><span data-stu-id="f8367-212">You may also change the order of DOM nodes.</span></span> <span data-ttu-id="f8367-213">Par exemple, sur votre page web, le menu de navigation se trouve près du bas.</span><span class="sxs-lookup"><span data-stu-id="f8367-213">For example, on your web page the navigation menu is near the bottom.</span></span> <span data-ttu-id="f8367-214">Pour le déplacer vers le haut, effectuez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="f8367-214">To move it to the top, perform the following steps.</span></span>  

1.  <span data-ttu-id="f8367-215">Recherchez `<nav>` le nœud dans l’arborescence **DOM** de DevTools.</span><span class="sxs-lookup"><span data-stu-id="f8367-215">Find the `<nav>` node in the **DOM Tree** of DevTools.</span></span>  
    
    :::image type="complex" source="media/beginners-html-reorder1.msft.png" alt-text="Le nœud de navigation est mis en surbrillade dans DevTools" lightbox="media/beginners-html-reorder1.msft.png":::
       <span data-ttu-id="f8367-217">Le nœud de navigation est mis en surbrillade dans DevTools</span><span class="sxs-lookup"><span data-stu-id="f8367-217">The nav node is highlighted in DevTools</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f8367-218">Faites glisser le nœud vers le haut, afin que le nœud soit le `<nav>` premier enfant après le `<body>` nœud.</span><span class="sxs-lookup"><span data-stu-id="f8367-218">Drag the `<nav>` node to the top, so that the node is the first child after the `<body>` node.</span></span>  
    
    :::image type="complex" source="media/beginners-html-reorder3.msft.png" alt-text="Le nœud de navigation se trouve en haut de la page" lightbox="media/beginners-html-reorder3.msft.png":::
        <span data-ttu-id="f8367-220">Le nœud de navigation se trouve en haut de la page</span><span class="sxs-lookup"><span data-stu-id="f8367-220">The nav node is at the top of the page</span></span>  
    :::image-end:::  
    
### <a name="delete-a-node"></a><span data-ttu-id="f8367-221">Supprimer un nœud</span><span class="sxs-lookup"><span data-stu-id="f8367-221">Delete a node</span></span>

<span data-ttu-id="f8367-222">Vous pouvez également supprimer des nodes de l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="f8367-222">You may also remove nodes from the DOM Tree.</span></span> <span data-ttu-id="f8367-223">Effectuez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="f8367-223">Perform the following steps.</span></span>

1.  <span data-ttu-id="f8367-224">Dans **l’arborescence DOM,** choisissez `<div>A new element!?!</div>` .</span><span class="sxs-lookup"><span data-stu-id="f8367-224">In the **DOM Tree**, choose `<div>A new element!?!</div>`.</span></span> <span data-ttu-id="f8367-225">DevTools met en sur évidence le nœud.</span><span class="sxs-lookup"><span data-stu-id="f8367-225">DevTools highlights the node.</span></span> 
    
1.  <span data-ttu-id="f8367-226">Sélectionnez `Delete` la touche de votre clavier.</span><span class="sxs-lookup"><span data-stu-id="f8367-226">Select the `Delete` key on your keyboard.</span></span>  <span data-ttu-id="f8367-227">Le `<div>A new element!?!</div>` nœud est supprimé de l’arborescence DOM.</span><span class="sxs-lookup"><span data-stu-id="f8367-227">The `<div>A new element!?!</div>` node is removed from the DOM Tree.</span></span>  
    
    :::image type="complex" source="media/beginners-html-delete2.msft.png" alt-text="Le nœud a été supprimé" lightbox="media/beginners-html-delete2.msft.png":::
       <span data-ttu-id="f8367-229">Le nœud a été supprimé</span><span class="sxs-lookup"><span data-stu-id="f8367-229">The node has been deleted</span></span>  
    :::image-end:::  
    
## <a name="copy-your-changes"></a><span data-ttu-id="f8367-230">Copier vos modifications</span><span class="sxs-lookup"><span data-stu-id="f8367-230">Copy your changes</span></span>  

<span data-ttu-id="f8367-231">Vous avez presque terminé.</span><span class="sxs-lookup"><span data-stu-id="f8367-231">You're almost done.</span></span> <span data-ttu-id="f8367-232">Vous avez apporté quelques modifications à la page dans DevTools, mais elles ne sont pas enregistrées dans votre code source.</span><span class="sxs-lookup"><span data-stu-id="f8367-232">You made a few changes to the page in DevTools, but they're not saved to your source code.</span></span>  

1.  <span data-ttu-id="f8367-233">Actualisez **l’onglet en direct.** Les modifications que vous avez apportées dans l’arborescence DOM disparaissent.</span><span class="sxs-lookup"><span data-stu-id="f8367-233">Refresh the **live tab**. The changes that you made in the DOM Tree disappear.</span></span> <span data-ttu-id="f8367-234">En particulier, le texte revient en haut de `Your site!` la page et le texte revient en `A new element!?!` bas.</span><span class="sxs-lookup"><span data-stu-id="f8367-234">In particular, the text `Your site!` returns to the top of the page, and the text `A new element!?!` returns to the bottom.</span></span>  
    
    :::image type="complex" source="media/beginners-html-copy1.msft.png" alt-text="Les modifications que vous avez apportées ont disparu" lightbox="media/beginners-html-copy1.msft.png":::
       <span data-ttu-id="f8367-236">Les modifications que vous avez apportées ont disparu</span><span class="sxs-lookup"><span data-stu-id="f8367-236">The changes that you made are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f8367-237">Copiez le code suivant.</span><span class="sxs-lookup"><span data-stu-id="f8367-237">Copy the following code.</span></span>  
    
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
    
1.  <span data-ttu-id="f8367-238">Revenir à **l’onglet Éditeur** et remplacer le contenu de votre fichier par le code que vous avez `index.html` copié.</span><span class="sxs-lookup"><span data-stu-id="f8367-238">Go back to the **editor tab** and replace the content of your `index.html` file with the code that you copied.</span></span>  
    
    :::image type="complex" source="media/beginners-html-copy2.msft.png" alt-text="Apparence de index.htmfichier l" lightbox="media/beginners-html-copy2.msft.png":::
       <span data-ttu-id="f8367-240">Apparence `index.html` de votre fichier</span><span class="sxs-lookup"><span data-stu-id="f8367-240">How your `index.html` file should look</span></span>  
    :::image-end:::  
    
## <a name="next-steps"></a><span data-ttu-id="f8367-241">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="f8367-241">Next steps</span></span>  

*   <span data-ttu-id="f8367-242">Complétez le didacticiel suivant de cette série, [Prise en main avec CSS,][DevToolsBeginnersCss]pour apprendre à styler votre page et expérimenter les modifications de style dans Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="f8367-242">Complete the next tutorial in this series, [Get Started with CSS][DevToolsBeginnersCss], to learn how to style your page and experiment with style changes in Microsoft Edge DevTools.</span></span>  
*   <span data-ttu-id="f8367-243">Lisez [l’introduction au DOM][MDNIntroductionDom] pour en savoir plus sur le DOM.</span><span class="sxs-lookup"><span data-stu-id="f8367-243">Read [Introduction to the DOM][MDNIntroductionDom] to learn more about the DOM.</span></span>  
*   <span data-ttu-id="f8367-244">Consultez un cours comme [Introduction au développement Web][CourseraIntroductionToWebDevelopment] pour une expérience de développement web pratique.</span><span class="sxs-lookup"><span data-stu-id="f8367-244">Check out a course like [Introduction to Web Development][CourseraIntroductionToWebDevelopment] for more hands-on web development experience.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="f8367-245">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="f8367-245">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools pour les débutants : Prise en main avec CSS | Documents Microsoft"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Présentation des outils de | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html - alluring-| Glitch"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Mise en place des | HTML MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Présentation de la | DOM MDN"  

> [!NOTE]
> <span data-ttu-id="f8367-252">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f8367-252">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f8367-253">La page d’origine a été [trouvée ici](https://developers.google.com/web/tools/chrome-devtools/beginners/html) et a été co-auteure par [Le rédacteur technique Principal \(Interne][KatherineJackson] au rédacteur technique, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="f8367-253">The original page was found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/html) and was authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="f8367-255">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f8367-255">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors  
