---
title: Commencer à utiliser la journalisation des messages dans la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: d3dbec41bc1e53b5e9001551c796e5a495dd331e
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601732"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# <span data-ttu-id="11a49-103">Commencer à utiliser la journalisation des messages dans la console</span><span class="sxs-lookup"><span data-stu-id="11a49-103">Get Started With Logging Messages In The Console</span></span>   



<span data-ttu-id="11a49-104">Ce didacticiel interactif vous montre comment consigner et filtrer des messages dans la console [Microsoft Edge devtools][MicrosoftEdgeDevTools] .</span><span class="sxs-lookup"><span data-stu-id="11a49-104">This interactive tutorial shows you how to log and filter messages in the [Microsoft Edge DevTools][MicrosoftEdgeDevTools] console.</span></span>  

> ##### <span data-ttu-id="11a49-105">Figure1</span><span class="sxs-lookup"><span data-stu-id="11a49-105">Figure 1</span></span>  
> <span data-ttu-id="11a49-106">Messages dans la console</span><span class="sxs-lookup"><span data-stu-id="11a49-106">Messages in the Console</span></span>  
> ![Messages dans la console][ImageLogExample]  

<span data-ttu-id="11a49-108">Ce didacticiel est destiné à être finalisé dans l’ordre.</span><span class="sxs-lookup"><span data-stu-id="11a49-108">This tutorial is intended to be completed in order.</span></span>  <span data-ttu-id="11a49-109">Il part du principe que vous comprenez les principes de base du développement Web, notamment comment utiliser JavaScript pour ajouter de l’interactivité à une page.</span><span class="sxs-lookup"><span data-stu-id="11a49-109">It assumes that you understand the fundamentals of web development, such as how to use JavaScript to add interactivity to a page.</span></span>  

## <span data-ttu-id="11a49-110">Configurer la démo et DevTools</span><span class="sxs-lookup"><span data-stu-id="11a49-110">Set up the demo and DevTools</span></span>   

<span data-ttu-id="11a49-111">Ce didacticiel est conçu pour que vous puissiez ouvrir la démonstration et essayer les flux de travail vous-même.</span><span class="sxs-lookup"><span data-stu-id="11a49-111">This tutorial is designed so that you are able to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="11a49-112">Lorsque vous effectuez une suivi physique, il est plus probable de mémoriser les flux de travail.</span><span class="sxs-lookup"><span data-stu-id="11a49-112">When you physically follow along, you are more likely to remember the workflows later.</span></span>  

1.  <span data-ttu-id="11a49-113">Maintenez `Control` la touche Windows enfoncée `Command` et cliquez sur les **exemples de journaux** de la console pour l’ouvrir dans un nouvel onglet.</span><span class="sxs-lookup"><span data-stu-id="11a49-113">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **Console Log Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="11a49-114">Exemples de journaux de la console</span><span class="sxs-lookup"><span data-stu-id="11a49-114">Console Log Examples</span></span>][GlitchDevToolsConsoleLogExamples]
    
    <!-- > [!TIP]
    > Move the demo to a separate window.  
    > 
    > > ##### old Figure 2  
    > > The tutorial on the left, and the demo on the right  
    > > ![The tutorial on the left, and the demo on the right][ImageLogSetUp1]  -->
    
1.  <span data-ttu-id="11a49-115">Focalisez la démonstration, puis appuyez sur `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \) pour ouvrir devtools.</span><span class="sxs-lookup"><span data-stu-id="11a49-115">Focus the demo and then press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to open DevTools.</span></span>  <span data-ttu-id="11a49-116">Par défaut, DevTools s’ouvre à droite de la démonstration.</span><span class="sxs-lookup"><span data-stu-id="11a49-116">By default DevTools opens to the right of the demo.</span></span>  
    
    > ##### <span data-ttu-id="11a49-117">Figure 2</span><span class="sxs-lookup"><span data-stu-id="11a49-117">Figure 2</span></span>  
    > <span data-ttu-id="11a49-118">DevTools s’ouvre à droite de la démonstration.</span><span class="sxs-lookup"><span data-stu-id="11a49-118">DevTools opens to the right of the demo</span></span>  
    > <span data-ttu-id="11a49-119">! [DevTools s’ouvre à droite de la démonstration] [ImageDevToolsRight]</span><span class="sxs-lookup"><span data-stu-id="11a49-119">![DevTools opens to the right of the demo][ImageDevToolsRight]</span></span>  
    
    > [!TIP]
    > <span data-ttu-id="11a49-120">[Ancrez devtools en bas de la fenêtre ou déverrouillez-la dans une fenêtre séparée][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="11a49-120">[Dock DevTools to the bottom of the window or undock it into a separate window][DevToolsCustomizePlacement].</span></span>  
    
    > ##### <span data-ttu-id="11a49-121">Figure3</span><span class="sxs-lookup"><span data-stu-id="11a49-121">Figure 3</span></span>  
    > <span data-ttu-id="11a49-122">DevTools ancré en bas de la démo</span><span class="sxs-lookup"><span data-stu-id="11a49-122">DevTools docked to the bottom of the demo</span></span>  
    > <span data-ttu-id="11a49-123">! [DevTools ancré en bas de la démonstration] [ImageDevToolsBottom]</span><span class="sxs-lookup"><span data-stu-id="11a49-123">![DevTools docked to the bottom of the demo][ImageDevToolsBottom]</span></span>  
    
    > ##### <span data-ttu-id="11a49-124">Figure 4</span><span class="sxs-lookup"><span data-stu-id="11a49-124">Figure 4</span></span>  
    > <span data-ttu-id="11a49-125">Navigateur dans une fenêtre séparée</span><span class="sxs-lookup"><span data-stu-id="11a49-125">Browser in a separate window</span></span>  
    > <span data-ttu-id="11a49-126">! [Navigateur dans une fenêtre séparée] [ImageDevToolsSeparateBrowse]</span><span class="sxs-lookup"><span data-stu-id="11a49-126">![Browser in a separate window][ImageDevToolsSeparateBrowse]</span></span>  
    
    > ##### <span data-ttu-id="11a49-127">Figure 5</span><span class="sxs-lookup"><span data-stu-id="11a49-127">Figure 5</span></span>  
    > <span data-ttu-id="11a49-128">DevTools non ancré dans une fenêtre séparée</span><span class="sxs-lookup"><span data-stu-id="11a49-128">DevTools undocked in a separate window</span></span>  
    > <span data-ttu-id="11a49-129">! [DevTools pas ancré dans une fenêtre séparée] [ImageDevToolsSeparateDevTools]</span><span class="sxs-lookup"><span data-stu-id="11a49-129">![DevTools undocked in a separate window][ImageDevToolsSeparateDevTools]</span></span>  
    
## <span data-ttu-id="11a49-130">Afficher les messages enregistrés depuis JavaScript</span><span class="sxs-lookup"><span data-stu-id="11a49-130">View messages logged from JavaScript</span></span>   

<span data-ttu-id="11a49-131">La plupart des messages que vous voyez dans la console proviennent des développeurs Web qui écrivent le JavaScript de la page.</span><span class="sxs-lookup"><span data-stu-id="11a49-131">Most messages that you see in the Console come from the web developers who wrote the JavaScript of the page.</span></span>  <span data-ttu-id="11a49-132">L’objectif de cette section consiste à vous présenter les différents types de messages que vous risquez de voir dans la console et à expliquer la façon dont vous pouvez enregistrer chaque type de message vous-même dans JavaScript.</span><span class="sxs-lookup"><span data-stu-id="11a49-132">The goal of this section is to introduce you to the different message types that you are likely to see in the Console, and explain how you may log each message type yourself from your own JavaScript.</span></span>  

1.  <span data-ttu-id="11a49-133">Cliquez sur le bouton **informations du journal** dans la démonstration.</span><span class="sxs-lookup"><span data-stu-id="11a49-133">Click the **Log Info** button in the demo.</span></span>  `Hello, Console!` <span data-ttu-id="11a49-134">est connecté à la console.</span><span class="sxs-lookup"><span data-stu-id="11a49-134">gets logged to the Console.</span></span>
    
    > ##### <span data-ttu-id="11a49-135">Figure 6</span><span class="sxs-lookup"><span data-stu-id="11a49-135">Figure 6</span></span>  
    > <span data-ttu-id="11a49-136">La console après avoir cliqué sur **informations du journal**</span><span class="sxs-lookup"><span data-stu-id="11a49-136">The Console after clicking **Log Info**</span></span>  
    > <span data-ttu-id="11a49-137">! [La console après avoir cliqué sur informations du journal] [ImageLogInfo]</span><span class="sxs-lookup"><span data-stu-id="11a49-137">![The Console after clicking Log Info][ImageLogInfo]</span></span>  
    
1.  <span data-ttu-id="11a49-138">En regard du `Hello, Console!` message dans la console, cliquez sur **log. js: 2**.</span><span class="sxs-lookup"><span data-stu-id="11a49-138">Next to the `Hello, Console!` message in the Console click **log.js:2**.</span></span>  <span data-ttu-id="11a49-139">Le panneau sources s’ouvre et met en surbrillance la ligne de code qui a entraîné le message à se connecter à la console.</span><span class="sxs-lookup"><span data-stu-id="11a49-139">The Sources panel opens and highlights the line of code that caused the message to get logged to the Console.</span></span>  <span data-ttu-id="11a49-140">Le message a été enregistré lors de l’exécution du code JavaScript de la page `console.log('Hello, Console!')` .</span><span class="sxs-lookup"><span data-stu-id="11a49-140">The message was logged when the JavaScript of the page ran `console.log('Hello, Console!')`.</span></span>
    
    > ##### <span data-ttu-id="11a49-141">Figure 7</span><span class="sxs-lookup"><span data-stu-id="11a49-141">Figure 7</span></span>  
    > <span data-ttu-id="11a49-142">DevTools ouvre le panneau sources après que vous avez cliqué sur **log. js: 2**</span><span class="sxs-lookup"><span data-stu-id="11a49-142">DevTools opens the Sources panel after you click **log.js:2**</span></span>  
    > <span data-ttu-id="11a49-143">! [DevTools ouvre le panneau sources après que vous avez cliqué sur log. js: 2] [ImageSourceLog]</span><span class="sxs-lookup"><span data-stu-id="11a49-143">![DevTools opens the Sources panel after you click log.js:2][ImageSourceLog]</span></span>  
    
1.  <span data-ttu-id="11a49-144">Revenez à la console à l’aide de l’un des flux de travail suivants:</span><span class="sxs-lookup"><span data-stu-id="11a49-144">Navigate back to the Console using any of the following workflows:</span></span>  
    
    *   <span data-ttu-id="11a49-145">Cliquez sur l’onglet de la **console** .</span><span class="sxs-lookup"><span data-stu-id="11a49-145">Click the **Console** tab.</span></span>  
    *   <span data-ttu-id="11a49-146">Appuyez sur `Control` + `[` \ (Windows \) ou `Command` + `[` \ (MacOS \) jusqu’à ce que le panneau de la console ait le focus.</span><span class="sxs-lookup"><span data-stu-id="11a49-146">Press `Control`+`[` \(Windows\) or `Command`+`[` \(macOS\) until the Console panel is in focus.</span></span>  
    *   <span data-ttu-id="11a49-147">[Ouvrez le menu de commandes][DevToolsCommandMenu], commencez à taper `Console` , sélectionnez l’option **afficher le panneau** de la console, puis appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="11a49-147">[Open the Command Menu][DevToolsCommandMenu], start typing `Console`, select the **Show Console Panel** command, and then press `Enter`.</span></span>  
    
1.  <span data-ttu-id="11a49-148">Cliquez sur le bouton **Avertissement du journal** dans la démonstration.</span><span class="sxs-lookup"><span data-stu-id="11a49-148">Click the **Log Warning** button in the demo.</span></span>  `Abandon Hope All Ye Who Enter` <span data-ttu-id="11a49-149">est connecté à la console.</span><span class="sxs-lookup"><span data-stu-id="11a49-149">gets logged to the Console.</span></span>  <span data-ttu-id="11a49-150">Les messages mis en forme comme celui-ci sont des avertissements.</span><span class="sxs-lookup"><span data-stu-id="11a49-150">Messages formatted like this are warnings.</span></span>  
    
    > ##### <span data-ttu-id="11a49-151">Figure8</span><span class="sxs-lookup"><span data-stu-id="11a49-151">Figure 8</span></span>  
    > <span data-ttu-id="11a49-152">La console après avoir cliqué sur **Avertissement du journal**</span><span class="sxs-lookup"><span data-stu-id="11a49-152">The Console after clicking **Log Warning**</span></span>  
    > <span data-ttu-id="11a49-153">! [La console après avoir cliqué sur avertissement du journal] [ImageConsoleLogWarning]</span><span class="sxs-lookup"><span data-stu-id="11a49-153">![The Console after clicking Log Warning][ImageConsoleLogWarning]</span></span>  
    
    > [!TIP]
    > <span data-ttu-id="11a49-154">Si vous souhaitez voir le code ayant entraîné l’enregistrement d’un message d’une certaine façon, cliquez sur un script (par exemple, `log.js:12` \) pour afficher le code ayant entraîné la mise en forme du message.</span><span class="sxs-lookup"><span data-stu-id="11a49-154">If you want to see the code that caused a message to get logged a certain way, click on a script \(such as `log.js:12`\) to view the code that caused the message to get formatted.</span></span>  

1.  <span data-ttu-id="11a49-155">Cliquez sur **l'** ![ icône développer ][ImageExpandIcon] `Abandon Hope All Ye Who Enter` .</span><span class="sxs-lookup"><span data-stu-id="11a49-155">Click the **Expand** ![Expand][ImageExpandIcon] icon in front of `Abandon Hope All Ye Who Enter`.</span></span>  <span data-ttu-id="11a49-156">DevTools affiche la [trace de pile][WikiStackTrace] qui se trouve au début de l’appel.</span><span class="sxs-lookup"><span data-stu-id="11a49-156">DevTools shows the [stack trace][WikiStackTrace] leading up to the call.</span></span>  
    
    > ##### <span data-ttu-id="11a49-157">Figure9</span><span class="sxs-lookup"><span data-stu-id="11a49-157">Figure 9</span></span>  
    > <span data-ttu-id="11a49-158">Une trace de pile</span><span class="sxs-lookup"><span data-stu-id="11a49-158">A stack trace</span></span>  
    > <span data-ttu-id="11a49-159">! [Une trace de pile] [ImageStackTrace]</span><span class="sxs-lookup"><span data-stu-id="11a49-159">![A stack trace][ImageStackTrace]</span></span>  
    
    <span data-ttu-id="11a49-160">La trace de pile vous indique qu’une fonction nommée `logWarning` a été appelée, qui à son tour appelait une fonction nommée `quoteDante` .</span><span class="sxs-lookup"><span data-stu-id="11a49-160">The stack trace is telling you that a function named `logWarning` was called, which in turn called a function named `quoteDante`.</span></span>  <span data-ttu-id="11a49-161">En d’autres termes, l’appel qui s’est produit en premier est en bas de la trace de pile.</span><span class="sxs-lookup"><span data-stu-id="11a49-161">In other words, the call that happened first is at the bottom of the stack trace.</span></span>  <span data-ttu-id="11a49-162">Vous pouvez enregistrer des traces de pile à tout moment en les appelant `console.trace()` .</span><span class="sxs-lookup"><span data-stu-id="11a49-162">You may log stack traces at any time by calling `console.trace()`.</span></span>  

1.  <span data-ttu-id="11a49-163">Cliquez sur **erreur de connexion**.</span><span class="sxs-lookup"><span data-stu-id="11a49-163">Click **Log Error**.</span></span>  <span data-ttu-id="11a49-164">Le message d’erreur suivant s’affiche:</span><span class="sxs-lookup"><span data-stu-id="11a49-164">The following error message gets logged:</span></span> `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    > ##### <span data-ttu-id="11a49-165">Figure10</span><span class="sxs-lookup"><span data-stu-id="11a49-165">Figure 10</span></span>  
    > <span data-ttu-id="11a49-166">Un message d’erreur</span><span class="sxs-lookup"><span data-stu-id="11a49-166">An error message</span></span>  
    > <span data-ttu-id="11a49-167">! [Message d’erreur] [ImageLogError]</span><span class="sxs-lookup"><span data-stu-id="11a49-167">![An error message][ImageLogError]</span></span>  
    
1.  <span data-ttu-id="11a49-168">Cliquez sur **table du journal**.</span><span class="sxs-lookup"><span data-stu-id="11a49-168">Click **Log Table**.</span></span>  <span data-ttu-id="11a49-169">Un tableau sur les artistes célèbres est connecté à la console.</span><span class="sxs-lookup"><span data-stu-id="11a49-169">A table about famous artists gets logged to the Console.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="11a49-170">La `birthday` colonne est uniquement remplie pour une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="11a49-170">The `birthday` column is only populated for one row.</span></span>  <span data-ttu-id="11a49-171">Vérifiez le code pour savoir pourquoi c’est.</span><span class="sxs-lookup"><span data-stu-id="11a49-171">Check the code to figure out why that is.</span></span>
    
    > ##### <span data-ttu-id="11a49-172">Figure11</span><span class="sxs-lookup"><span data-stu-id="11a49-172">Figure 11</span></span>  
    > <span data-ttu-id="11a49-173">Tableau sur la console</span><span class="sxs-lookup"><span data-stu-id="11a49-173">A table in the Console</span></span>  
    > <span data-ttu-id="11a49-174">! [Une table dans la console] [ImageConsoleTable]</span><span class="sxs-lookup"><span data-stu-id="11a49-174">![A table in the Console][ImageConsoleTable]</span></span>  
    
1.  <span data-ttu-id="11a49-175">Cliquez sur **groupe de journaux**.</span><span class="sxs-lookup"><span data-stu-id="11a49-175">Click **Log Group**.</span></span>  <span data-ttu-id="11a49-176">Les noms des 4 plus célèbres et des tortues sont regroupés sous l' `Adolescent Irradiated Espionage Tortoises` étiquette.</span><span class="sxs-lookup"><span data-stu-id="11a49-176">The names of 4 famous, crime-fighting turtles are grouped under the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  
    
    > ##### <span data-ttu-id="11a49-177">Figure12</span><span class="sxs-lookup"><span data-stu-id="11a49-177">Figure 12</span></span>  
    > <span data-ttu-id="11a49-178">Groupe de messages dans la console</span><span class="sxs-lookup"><span data-stu-id="11a49-178">A group of messages in the Console</span></span>  
    > <span data-ttu-id="11a49-179">! [Groupe de messages dans la console] [ImageConsoleLogGroup]</span><span class="sxs-lookup"><span data-stu-id="11a49-179">![A group of messages in the Console][ImageConsoleLogGroup]</span></span>  
    
1.  <span data-ttu-id="11a49-180">Cliquez sur **journal personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="11a49-180">Click **Log Custom**.</span></span>  <span data-ttu-id="11a49-181">Un message avec une bordure rouge et un arrière-plan bleu est connecté à la console.</span><span class="sxs-lookup"><span data-stu-id="11a49-181">A message with a red border and blue background gets logged to the Console.</span></span>  
    
    > ##### <span data-ttu-id="11a49-182">Figure13</span><span class="sxs-lookup"><span data-stu-id="11a49-182">Figure 13</span></span>  
    > <span data-ttu-id="11a49-183">Message avec une mise en forme personnalisée dans la console</span><span class="sxs-lookup"><span data-stu-id="11a49-183">A message with custom formatting in the Console</span></span>  
    > <span data-ttu-id="11a49-184">! [Un message avec une mise en forme personnalisée dans la console] [ImageConsoleLogCustomFormatting]</span><span class="sxs-lookup"><span data-stu-id="11a49-184">![A message with custom formatting in the Console][ImageConsoleLogCustomFormatting]</span></span>  
    
<span data-ttu-id="11a49-185">Le principe principal est le suivant: lorsque vous souhaitez consigner des messages dans la console à partir de votre JavaScript, vous utilisez l’une des `console` méthodes.</span><span class="sxs-lookup"><span data-stu-id="11a49-185">The main idea here is that when you want to log messages to the Console from your JavaScript, you use one of the `console` methods.</span></span>  <span data-ttu-id="11a49-186">Chaque méthode met en forme les messages différemment.</span><span class="sxs-lookup"><span data-stu-id="11a49-186">Each method formats messages differently.</span></span>  

<span data-ttu-id="11a49-187">Il existe encore plus de méthodes que celles présentées dans cette section.</span><span class="sxs-lookup"><span data-stu-id="11a49-187">There are even more methods than what has been demonstrated in this section.</span></span>  <span data-ttu-id="11a49-188">Ce didacticiel vous explique comment découvrir le reste des méthodes.</span><span class="sxs-lookup"><span data-stu-id="11a49-188">This tutorial shows you how to explore the rest of the methods.</span></span>  

## <span data-ttu-id="11a49-189">Afficher les messages enregistrés par le navigateur</span><span class="sxs-lookup"><span data-stu-id="11a49-189">View messages logged by the browser</span></span>   

<span data-ttu-id="11a49-190">Le navigateur enregistre également les messages sur la console.</span><span class="sxs-lookup"><span data-stu-id="11a49-190">The browser logs messages to the Console, too.</span></span>  <span data-ttu-id="11a49-191">Cela se produit généralement lorsque la page rencontre un problème.</span><span class="sxs-lookup"><span data-stu-id="11a49-191">This usually happens when there is a problem with the page.</span></span>  

1.  <span data-ttu-id="11a49-192">Cliquez sur **Cause 404**.</span><span class="sxs-lookup"><span data-stu-id="11a49-192">Click **Cause 404**.</span></span>  <span data-ttu-id="11a49-193">Le navigateur enregistre une `404` erreur réseau, car le code JavaScript de la page essayait de récupérer un fichier qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="11a49-193">The browser logs a `404` network error because the JavaScript of the page tried to fetch a file that does not exist.</span></span>  
    
    > ##### <span data-ttu-id="11a49-194">Figure14</span><span class="sxs-lookup"><span data-stu-id="11a49-194">Figure 14</span></span>  
    > <span data-ttu-id="11a49-195">Erreur 404 dans la console</span><span class="sxs-lookup"><span data-stu-id="11a49-195">A 404 error in the Console</span></span>  
    > <span data-ttu-id="11a49-196">! [Erreur 404 dans la console] [ImageConsoleLogError]</span><span class="sxs-lookup"><span data-stu-id="11a49-196">![A 404 error in the Console][ImageConsoleLogError]</span></span>  
    
1.  <span data-ttu-id="11a49-197">Cliquez sur **provoquer une erreur**.</span><span class="sxs-lookup"><span data-stu-id="11a49-197">Click **Cause Error**.</span></span>  <span data-ttu-id="11a49-198">Le navigateur enregistre une incapture `TypeError` car JavaScript tente de mettre à jour un nœud DOM qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="11a49-198">The browser logs an uncaught `TypeError` because the JavaScript is trying to update a DOM node that does not exist.</span></span>  
    
    > ##### <span data-ttu-id="11a49-199">Figure15</span><span class="sxs-lookup"><span data-stu-id="11a49-199">Figure 15</span></span>  
    > <span data-ttu-id="11a49-200">A TypeError dans la console</span><span class="sxs-lookup"><span data-stu-id="11a49-200">A TypeError in the Console</span></span>  
    > <span data-ttu-id="11a49-201">! [A TypeError dans la console] [ImageConsoleLogTypeError]</span><span class="sxs-lookup"><span data-stu-id="11a49-201">![A TypeError in the Console][ImageConsoleLogTypeError]</span></span>  
    
1.  <span data-ttu-id="11a49-202">Cliquez sur la liste déroulante **niveaux du journal** et activez l’option **détaillé** s’il est désactivé.</span><span class="sxs-lookup"><span data-stu-id="11a49-202">Click the **Log Levels** dropdown and enable the **Verbose** option if it is disabled.</span></span>  <span data-ttu-id="11a49-203">Pour plus d’informations sur le filtrage, voir la section suivante.</span><span class="sxs-lookup"><span data-stu-id="11a49-203">You learn more about filtering in the next section.</span></span>  <span data-ttu-id="11a49-204">Vous devez effectuer cette opération pour vérifier que le message suivant que vous enregistrez est visible.</span><span class="sxs-lookup"><span data-stu-id="11a49-204">You need to do this to make sure that the next message you log is visible.</span></span>  
    
    > ##### <span data-ttu-id="11a49-205">Figure16</span><span class="sxs-lookup"><span data-stu-id="11a49-205">Figure 16</span></span>  
    > <span data-ttu-id="11a49-206">Activer le niveau de journalisation **détaillé**</span><span class="sxs-lookup"><span data-stu-id="11a49-206">Enabling the **Verbose** log level</span></span>  
    > <span data-ttu-id="11a49-207">! [Activation du niveau de journalisation détaillé] [ImageVerboseLogLevel]</span><span class="sxs-lookup"><span data-stu-id="11a49-207">![Enabling the Verbose log level][ImageVerboseLogLevel]</span></span>  
    
1.  <span data-ttu-id="11a49-208">Cliquez sur **provoquer une violation**.</span><span class="sxs-lookup"><span data-stu-id="11a49-208">Click **Cause Violation**.</span></span>  <span data-ttu-id="11a49-209">La page cesse de répondre pendant quelques secondes, puis le navigateur enregistre le message `[Violation] 'click' handler took 3000ms` sur la console.</span><span class="sxs-lookup"><span data-stu-id="11a49-209">The page becomes unresponsive for a few seconds and then the browser logs the message `[Violation] 'click' handler took 3000ms` to the Console.</span></span>  <span data-ttu-id="11a49-210">La durée exacte est variable.</span><span class="sxs-lookup"><span data-stu-id="11a49-210">The exact duration may vary.</span></span>  
    
    > ##### <span data-ttu-id="11a49-211">Figure17</span><span class="sxs-lookup"><span data-stu-id="11a49-211">Figure 17</span></span>  
    > <span data-ttu-id="11a49-212">Violation dans la console</span><span class="sxs-lookup"><span data-stu-id="11a49-212">A violation in the Console</span></span>  
    > <span data-ttu-id="11a49-213">! [Violation dans la console] [ImageConsoleLogViolation]</span><span class="sxs-lookup"><span data-stu-id="11a49-213">![A violation in the Console][ImageConsoleLogViolation]</span></span>  
    
## <span data-ttu-id="11a49-214">Filtrer les messages</span><span class="sxs-lookup"><span data-stu-id="11a49-214">Filter messages</span></span>   

<span data-ttu-id="11a49-215">Dans certaines pages, la console est inondée de messages.</span><span class="sxs-lookup"><span data-stu-id="11a49-215">On some pages you see the Console get flooded with messages.</span></span>  <span data-ttu-id="11a49-216">DevTools offre différentes façons de filtrer les messages qui ne sont pas pertinents pour la tâche en cours.</span><span class="sxs-lookup"><span data-stu-id="11a49-216">DevTools provides many different ways to filter out messages that are not relevant to the task at hand.</span></span>  

### <span data-ttu-id="11a49-217">Filtrer par niveau de journal</span><span class="sxs-lookup"><span data-stu-id="11a49-217">Filter by log level</span></span>   

<span data-ttu-id="11a49-218">`console`Un niveau de gravité est attribué à chaque méthode: `Verbose` , `Info` , `Warning` ou `Error` .</span><span class="sxs-lookup"><span data-stu-id="11a49-218">Each `console` method is assigned a severity level: `Verbose`, `Info`, `Warning`, or `Error`.</span></span>  <span data-ttu-id="11a49-219">Par exemple, `console.log()` il s’agit d’un `Info` message de `console.error()` niveau supérieur `Error` .</span><span class="sxs-lookup"><span data-stu-id="11a49-219">For example, `console.log()` is an `Info`-level message, whereas `console.error()` is an `Error`-level message.</span></span>  

1.  <span data-ttu-id="11a49-220">Cliquez sur la liste déroulante **niveaux du journal** et désactivez **Erreurs**.</span><span class="sxs-lookup"><span data-stu-id="11a49-220">Click the **Log Levels** dropdown and disable **Errors**.</span></span>  <span data-ttu-id="11a49-221">Un niveau est désactivé quand il n’y a plus de coche en regard de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="11a49-221">A level is disabled when there is no longer a checkmark next to it.</span></span>  <span data-ttu-id="11a49-222">Les `Error` messages de niveau disparaissent.</span><span class="sxs-lookup"><span data-stu-id="11a49-222">The `Error`-level messages disappear.</span></span>  
    
    > ##### <span data-ttu-id="11a49-223">Figure 18</span><span class="sxs-lookup"><span data-stu-id="11a49-223">Figure 18</span></span>  
    > <span data-ttu-id="11a49-224">Désactivation des `Error` messages de niveau de la console</span><span class="sxs-lookup"><span data-stu-id="11a49-224">Disabling `Error`-level messages in the Console</span></span>  
    > <span data-ttu-id="11a49-225">! [Désactivation des messages de niveau erreur dans la console] [ImageConsoleDisablingLogError]</span><span class="sxs-lookup"><span data-stu-id="11a49-225">![Disabling Error-level messages in the Console][ImageConsoleDisablingLogError]</span></span>  
    
1.  <span data-ttu-id="11a49-226">Cliquez de nouveau sur la liste déroulante **niveaux du journal** et activez de nouveau les **Erreurs**.</span><span class="sxs-lookup"><span data-stu-id="11a49-226">Click the **Log Levels** dropdown again and re-enable **Errors**.</span></span>  <span data-ttu-id="11a49-227">Les `Error` messages de niveau supérieur apparaissent.</span><span class="sxs-lookup"><span data-stu-id="11a49-227">The `Error`-level messages reappear.</span></span>  

### <span data-ttu-id="11a49-228">Filtrer par texte</span><span class="sxs-lookup"><span data-stu-id="11a49-228">Filter by text</span></span>   

<span data-ttu-id="11a49-229">Lorsque vous souhaitez uniquement afficher les messages qui incluent une chaîne exacte, tapez cette chaîne dans la zone de texte du **filtre** .</span><span class="sxs-lookup"><span data-stu-id="11a49-229">When you want to only view messages that include an exact string, type that string into the **Filter** text box.</span></span>  

1.  <span data-ttu-id="11a49-230">Entrez `Dave` dans la zone de texte du **filtre** .</span><span class="sxs-lookup"><span data-stu-id="11a49-230">Type `Dave` into the **Filter** text box.</span></span>  <span data-ttu-id="11a49-231">Tous les messages n’incluant pas la chaîne `Dave` sont masqués.</span><span class="sxs-lookup"><span data-stu-id="11a49-231">All messages that do not include the string `Dave` are hidden.</span></span>  <span data-ttu-id="11a49-232">Vous pouvez également voir l' `Adolescent Irradiated Espionage Tortoises` étiquette.</span><span class="sxs-lookup"><span data-stu-id="11a49-232">You might also see the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  <span data-ttu-id="11a49-233">Il s’agit d’un bogue.</span><span class="sxs-lookup"><span data-stu-id="11a49-233">That is a bug.</span></span>  
    
    > ##### <span data-ttu-id="11a49-234">Figure 19</span><span class="sxs-lookup"><span data-stu-id="11a49-234">Figure 19</span></span>  
    > <span data-ttu-id="11a49-235">Filtrage des messages n’incluant pas</span><span class="sxs-lookup"><span data-stu-id="11a49-235">Filtering out any message that does not include</span></span> `Dave`  
    > <span data-ttu-id="11a49-236">! [Filtrage des messages n’incluant pas Dave] [ImageLogTextFiltering]</span><span class="sxs-lookup"><span data-stu-id="11a49-236">![Filtering out any message that does not include Dave][ImageLogTextFiltering]</span></span>  
    
1.  <span data-ttu-id="11a49-237">Supprimer `Dave` de la zone de texte du **filtre** .</span><span class="sxs-lookup"><span data-stu-id="11a49-237">Delete `Dave` from the **Filter** text box.</span></span>  <span data-ttu-id="11a49-238">Tous les messages réapparaissent.</span><span class="sxs-lookup"><span data-stu-id="11a49-238">All the messages reappear.</span></span>  

### <span data-ttu-id="11a49-239">Filtrer par expression régulière</span><span class="sxs-lookup"><span data-stu-id="11a49-239">Filter by regular expression</span></span>   

<span data-ttu-id="11a49-240">Pour afficher tous les messages qui incluent un modèle de texte plutôt qu’une chaîne spécifique, utilisez une [expression régulière][MDNRegularExpressions].</span><span class="sxs-lookup"><span data-stu-id="11a49-240">When you want to show all messages that include a pattern of text, rather than a specific string, use a [regular expression][MDNRegularExpressions].</span></span>  

1.  <span data-ttu-id="11a49-241">Entrez `/^[AH]/` dans la zone de texte du **filtre** .</span><span class="sxs-lookup"><span data-stu-id="11a49-241">Type `/^[AH]/` into the **Filter** text box.</span></span>  <span data-ttu-id="11a49-242">Tapez ce modèle dans [Regex][|::ref1::|Main] pour obtenir une explication de ce qu’il fait.</span><span class="sxs-lookup"><span data-stu-id="11a49-242">Type this pattern into [RegExr][|::ref1::|Main] for an explanation of what it is doing.</span></span>  
    
    > ##### <span data-ttu-id="11a49-243">Figure 20</span><span class="sxs-lookup"><span data-stu-id="11a49-243">Figure 20</span></span>  
    > <span data-ttu-id="11a49-244">Filtrage de tout message ne correspondant pas au modèle</span><span class="sxs-lookup"><span data-stu-id="11a49-244">Filtering out any message that does not match the pattern</span></span> `/^[AH]/`  
    > <span data-ttu-id="11a49-245">! [En filtrant les messages ne correspondant à aucun modèle] [ImageLogRegExFiltering]</span><span class="sxs-lookup"><span data-stu-id="11a49-245">![Filtering out any message that does not match a pattern][ImageLogRegExFiltering]</span></span>  
    
1.  <span data-ttu-id="11a49-246">Supprimer `/^[AH]/` de la zone de texte du **filtre** .</span><span class="sxs-lookup"><span data-stu-id="11a49-246">Delete `/^[AH]/` from the **Filter** text box.</span></span>  <span data-ttu-id="11a49-247">Tous les messages sont de nouveau visibles.</span><span class="sxs-lookup"><span data-stu-id="11a49-247">All messages are visible again.</span></span>  

### <span data-ttu-id="11a49-248">Filtrer par source de message</span><span class="sxs-lookup"><span data-stu-id="11a49-248">Filter by message source</span></span>   

<span data-ttu-id="11a49-249">Pour afficher uniquement les messages provenant d’une URL spécifique, utilisez la **barre latérale**.</span><span class="sxs-lookup"><span data-stu-id="11a49-249">When you want to only view the messages that came from a certain URL, use the **Sidebar**.</span></span>  

1.  <span data-ttu-id="11a49-250">Cliquez sur Afficher la barre latérale de la **console** ![ ][ImageShowConsoleSidebarIcon] .</span><span class="sxs-lookup"><span data-stu-id="11a49-250">Click **Show Console Sidebar** ![Show Console Sidebar][ImageShowConsoleSidebarIcon].</span></span>  
    
    > ##### <span data-ttu-id="11a49-251">Figure 21</span><span class="sxs-lookup"><span data-stu-id="11a49-251">Figure 21</span></span>  
    > <span data-ttu-id="11a49-252">Barre latérale</span><span class="sxs-lookup"><span data-stu-id="11a49-252">The Sidebar</span></span>  
    > <span data-ttu-id="11a49-253">! [Barre latérale] [ImageConsoleSidebar]</span><span class="sxs-lookup"><span data-stu-id="11a49-253">![The Sidebar][ImageConsoleSidebar]</span></span>  
    
1.  <span data-ttu-id="11a49-254">Cliquez sur **l'** ![ ][ImageExpandIcon] icône de développement située en regard du nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="11a49-254">Click the **Expand** ![Expand][ImageExpandIcon] icon next to the number of messages.</span></span>  <span data-ttu-id="11a49-255">Dans la [figure 21](#figure-21), le nombre de messages est indiqué par **13 messages**.</span><span class="sxs-lookup"><span data-stu-id="11a49-255">In [Figure 21](#figure-21), the number of messages is indicated as **13 Messages**.</span></span>  <span data-ttu-id="11a49-256">La **barre latérale** affiche une liste des URL ayant entraîné la journalisation des messages.</span><span class="sxs-lookup"><span data-stu-id="11a49-256">The **Sidebar** shows a list of URLs that caused messages to be logged.</span></span>  <span data-ttu-id="11a49-257">Par exemple, il `log.js` a généré 11 messages.</span><span class="sxs-lookup"><span data-stu-id="11a49-257">For example, `log.js` caused 11 messages.</span></span>  
    
    > ##### <span data-ttu-id="11a49-258">Figure 22</span><span class="sxs-lookup"><span data-stu-id="11a49-258">Figure 22</span></span>  
    > <span data-ttu-id="11a49-259">Affichage de la source de messages dans la barre latérale</span><span class="sxs-lookup"><span data-stu-id="11a49-259">Viewing the source of messages in the Sidebar</span></span>  
    > <span data-ttu-id="11a49-260">! [Affichage de la source de messages dans la barre latérale] [ImageConsoleSidebarLogSource]</span><span class="sxs-lookup"><span data-stu-id="11a49-260">![Viewing the source of messages in the Sidebar][ImageConsoleSidebarLogSource]</span></span>  
    
### <span data-ttu-id="11a49-261">Filtrer par message utilisateur</span><span class="sxs-lookup"><span data-stu-id="11a49-261">Filter by user messages</span></span>   

<span data-ttu-id="11a49-262">Auparavant, lorsque vous cliquiez sur informations sur le **Journal**, un script appelé pour `console.log('Hello, Console!')` consigner le message sur la console.</span><span class="sxs-lookup"><span data-stu-id="11a49-262">Earlier, when you clicked **Log Info**, a script called `console.log('Hello, Console!')` in order to log the message to the Console.</span></span>  <span data-ttu-id="11a49-263">Les messages enregistrés depuis JavaScript comme celui-ci s’appelle **messages utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="11a49-263">Messages logged from JavaScript like this are called **user messages**.</span></span>  <span data-ttu-id="11a49-264">En revanche, lorsque vous avez cliqué sur **Cause 404**, le navigateur a enregistré un `Error` message de niveau indiquant que la ressource demandée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="11a49-264">In contrast, when you clicked **Cause 404**, the browser logged an `Error`-level message stating that the requested resource could not be found.</span></span>  <span data-ttu-id="11a49-265">Les messages comme les **messages du navigateur**.</span><span class="sxs-lookup"><span data-stu-id="11a49-265">Messages like that are considered **browser messages**.</span></span>  <span data-ttu-id="11a49-266">Utilisez la **barre latérale** pour filtrer les messages de navigateur et afficher uniquement les messages utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="11a49-266">Use the **Sidebar** to filter out browser messages and only show user messages.</span></span>  

1.  <span data-ttu-id="11a49-267">Cliquez sur **9 messages utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="11a49-267">Click **9 User Messages**.</span></span>  <span data-ttu-id="11a49-268">Les messages de navigateur sont masqués.</span><span class="sxs-lookup"><span data-stu-id="11a49-268">The browser messages are hidden.</span></span>  
    
    > ##### <span data-ttu-id="11a49-269">Figure 23</span><span class="sxs-lookup"><span data-stu-id="11a49-269">Figure 23</span></span>  
    > <span data-ttu-id="11a49-270">Filtrage des messages de navigateur</span><span class="sxs-lookup"><span data-stu-id="11a49-270">Filtering out browser messages</span></span>  
    > <span data-ttu-id="11a49-271">! [Filtrage des messages de navigateur] [ImageConsoleLogBrowserFiltering]</span><span class="sxs-lookup"><span data-stu-id="11a49-271">![Filtering out browser messages][ImageConsoleLogBrowserFiltering]</span></span>  
    
1.  <span data-ttu-id="11a49-272">Cliquez sur **13 messages** pour afficher de nouveau tous les messages.</span><span class="sxs-lookup"><span data-stu-id="11a49-272">Click **13 Messages** to show all messages again.</span></span>  

## <span data-ttu-id="11a49-273">Utiliser la console en même temps que d’autres panneaux</span><span class="sxs-lookup"><span data-stu-id="11a49-273">Use the Console alongside any other panel</span></span>   

<span data-ttu-id="11a49-274">Que se passe-t-il si vous modifiez les styles, mais vous avez besoin de consulter rapidement le journal de la console pour obtenir un élément?</span><span class="sxs-lookup"><span data-stu-id="11a49-274">What if you are editing styles, but you need to quickly check the Console log for something?</span></span> <span data-ttu-id="11a49-275">Utiliser le tiroir.</span><span class="sxs-lookup"><span data-stu-id="11a49-275">Use the Drawer.</span></span>  

1.  <span data-ttu-id="11a49-276">Cliquez sur l’onglet **éléments** .</span><span class="sxs-lookup"><span data-stu-id="11a49-276">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="11a49-277">Appuyez sur `Escape` .</span><span class="sxs-lookup"><span data-stu-id="11a49-277">Press `Escape`.</span></span>  <span data-ttu-id="11a49-278">L’onglet Console du **tiroir** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="11a49-278">The Console tab of the **Drawer** opens.</span></span>  <span data-ttu-id="11a49-279">Toutes les fonctionnalités du panneau de la console que vous avez utilisées tout au long de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="11a49-279">It has all of the features of the Console panel that you have been using throughout this tutorial.</span></span>  
    
    > ##### <span data-ttu-id="11a49-280">Figure 24</span><span class="sxs-lookup"><span data-stu-id="11a49-280">Figure 24</span></span>  
    > <span data-ttu-id="11a49-281">Onglet Console du tiroir</span><span class="sxs-lookup"><span data-stu-id="11a49-281">The Console tab in the Drawer</span></span>  
    > <span data-ttu-id="11a49-282">! [L’onglet Console du tiroir] [ImageDrawerConsole]</span><span class="sxs-lookup"><span data-stu-id="11a49-282">![The Console tab in the Drawer][ImageDrawerConsole]</span></span>  
    
<!--## Next steps  -->

<!--
*   See [Console Reference][DevToolsConsoleApi] to explore more features and workflows related to the Console UI.
*   See [Console API Reference][DevToolsConsoleReference] to learn more about all of the `console` methods that were demonstrated in [View messages logged from JavaScript(#view-messages-logged-from-javascript) and explore the other `console` methods that were not covered in this tutorial.  
*   See [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  

 



<!-- image links -->  

[ImageExpandIcon]: /microsoft-edge/devtools-guide-chromium/media/expand-icon.msft.png  
[ImageShowConsoleSidebarIcon]: /microsoft-edge/devtools-guide-chromium/media/show-console-sidebar-icon.msft.png  

[ImageLogExample]: /microsoft-edge/devtools-guide-chromium/media/console-ars-technica-console-onload.msft.png "Figure 1: messages de la console"  
<!--[ImageLogSetUp1]: /microsoft-edge/devtools-guide-chromium/media/log-set-up-1.msft.png "old Figure 2: The tutorial on the left, and the demo on the right"  -->  
[ImageDevToolsRight]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-example-devtools-Right-console.msft.png "figure 2: DevTools s’ouvre à droite de la démonstration"  
[ImageDevToolsBottom]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-example-devtools-Bottom-console.msft.png "figure 3: DevTools ancré en bas de la démonstration"  
[ImageDevToolsSeparateBrowse]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-example-devtools-Separate-console-Browse.msft.png "figure 4: navigateur dans une fenêtre séparée"  
[ImageDevToolsSeparateDevTools]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-example-devtools-Separate-console-devtools.msft.png "figure 5: DevTools non ancré dans une fenêtre séparée"  
[ImageLogInfo]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-log-info.msft.png "figure 6: la console après avoir cliqué sur informations du journal"  
[ImageSourceLog]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-sources-logjs.msft.png "figure 7: DevTools ouvre le panneau sources après que vous avez cliqué sur log. js: 2"  
[ImageConsoleLogWarning]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-log-Warning.msft.png "figure 8: la console après avoir cliqué sur avertissement du journal"  
[ImageStackTrace]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-log-Warning-Expanded.msft.png "figure 9: trace de pile"  
[ImageLogError]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-log-Error.msft.png "figure 10: message d’erreur"  
[ImageConsoleTable]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-log-table.msft.png "figure 11: une table dans la console"  
[ImageConsoleLogGroup]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-log-Group.msft.png "figure 12: un groupe de messages dans la console"  
[ImageConsoleLogCustomFormatting]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-log-Custom.msft.png "figure 13: message avec une mise en forme personnalisée dans la console"  
[ImageConsoleLogError]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-cause-404.msft.png "figure 14: erreur 404 dans la console"  
[ImageConsoleLogTypeError]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-cause-Error.msft.png "figure 15: un TypeError dans la console"  
[ImageVerboseLogLevel]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-cause-Error-Log-Levels.msft.png "figure 16: activer le niveau de journalisation détaillé"  
[ImageConsoleLogViolation]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-cause-violation.msft.png "figure 17: violation dans la console"  
[ImageConsoleDisablingLogError]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-cause-violation-log-Levels.msft.png "figure 18: désactivation des messages de niveau erreur dans la console"  
[ImageLogTextFiltering]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-All-messages-Text-Filter.msft.png "figure 19: filtrage des messages n’incluant pas Dave"  
[ImageLogRegExFiltering]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-All-messages-Regex-Filter.msft.png "figure 20: filtrage de tout message ne correspondant à aucun modèle"  
[ImageConsoleSidebar]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Sidebar-All-messages.msft.png "figure 21: barre latérale"  
[ImageConsoleSidebarLogSource]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Sidebar-Expanded-All-messages.msft.png "figure 22: affichage de la source de messages dans la barre latérale"  
[ImageConsoleLogBrowserFiltering]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Sidebar-user-messages.msft.png "figure 23: filtrage des messages de navigateur"  
[ImageDrawerConsole]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Elements-Drawer-console-Sidebar-All-messages.msft.png "figure 24: onglet de console dans le tiroir"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge \ (chrome \)"  
[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Exécuter des commandes à l’aide du menu de commande de Microsoft Edge DevTools"  
[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Changer la position de Microsoft Edge DevTools (détacher, ancrer en bas, ancrer à gauche)"  
[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Référence sur les API de la console"  
[DevToolsConsoleReference]: /microsoft-edge/devtools-guide-chromium/console/reference "Référence de la console"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Commencer à utiliser la journalisation des messages | Problème"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Expressions régulières | MDN"  

[RegExrMain]: https://regexr.com "RegEx"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Trace de pile-Wikipédia"  


> [!NOTE]
> <span data-ttu-id="11a49-316">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="11a49-316">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="11a49-317">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/log) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="11a49-317">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/log) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="11a49-319">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="11a49-319">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
