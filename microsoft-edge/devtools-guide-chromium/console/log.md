---
title: Commencer à utiliser la journalisation des messages dans la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: c2cf868e6daaf9dd45c7acc90a71c2154261b9c3
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982642"
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





# <span data-ttu-id="2ba34-103">Commencer à utiliser la journalisation des messages dans la console</span><span class="sxs-lookup"><span data-stu-id="2ba34-103">Get Started With Logging Messages In The Console</span></span>   



<span data-ttu-id="2ba34-104">Ce didacticiel interactif vous montre comment consigner et filtrer des messages dans la console [Microsoft Edge devtools][MicrosoftEdgeDevTools] .</span><span class="sxs-lookup"><span data-stu-id="2ba34-104">This interactive tutorial shows you how to log and filter messages in the [Microsoft Edge DevTools][MicrosoftEdgeDevTools] console.</span></span>  

:::image type="complex" source="../media/console-ars-technica-console-onload.msft.png" alt-text="Messages dans la console" lightbox="../media/console-ars-technica-console-onload.msft.png":::
   <span data-ttu-id="2ba34-106">Messages dans la **console**</span><span class="sxs-lookup"><span data-stu-id="2ba34-106">Messages in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="2ba34-107">Ce didacticiel est destiné à être finalisé dans l’ordre.</span><span class="sxs-lookup"><span data-stu-id="2ba34-107">This tutorial is intended to be completed in order.</span></span>  <span data-ttu-id="2ba34-108">Il part du principe que vous comprenez les principes de base du développement Web, notamment comment utiliser JavaScript pour ajouter de l’interactivité à une page.</span><span class="sxs-lookup"><span data-stu-id="2ba34-108">It assumes that you understand the fundamentals of web development, such as how to use JavaScript to add interactivity to a page.</span></span>  

## <span data-ttu-id="2ba34-109">Configurer la démo et DevTools</span><span class="sxs-lookup"><span data-stu-id="2ba34-109">Set up the demo and DevTools</span></span>   

<span data-ttu-id="2ba34-110">Ce didacticiel est conçu pour que vous puissiez ouvrir la démonstration et essayer les flux de travail vous-même.</span><span class="sxs-lookup"><span data-stu-id="2ba34-110">This tutorial is designed so that you are able to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="2ba34-111">Lorsque vous effectuez une suivi physique, il est plus probable de mémoriser les flux de travail.</span><span class="sxs-lookup"><span data-stu-id="2ba34-111">When you physically follow along, you are more likely to remember the workflows later.</span></span>  

1.  <span data-ttu-id="2ba34-112">Maintenez `Control` la touche Windows enfoncée `Command` et cliquez sur les **exemples de journaux** de la console pour l’ouvrir dans un nouvel onglet.</span><span class="sxs-lookup"><span data-stu-id="2ba34-112">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **Console Log Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="2ba34-113">Exemples de journaux de la console</span><span class="sxs-lookup"><span data-stu-id="2ba34-113">Console Log Examples</span></span>][GlitchDevToolsConsoleLogExamples]
    
    <!--
    > [!TIP]
    > Move the demo to a separate window.  
    > 
    > :::image type="complex" source="../media/log-set-up-1.msft.png" alt-text="The tutorial on the left, and the demo on the right" lightbox="../media/log-set-up-1.msft.png":::
    >    The tutorial on the left, and the demo on the right  
    > :::image-end:::  
    -->
    
1.  <span data-ttu-id="2ba34-114">Focalisez la démonstration, puis appuyez sur `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \) pour ouvrir devtools.</span><span class="sxs-lookup"><span data-stu-id="2ba34-114">Focus the demo and then press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to open DevTools.</span></span>  <span data-ttu-id="2ba34-115">Par défaut, DevTools s’ouvre à droite de la démonstration.</span><span class="sxs-lookup"><span data-stu-id="2ba34-115">By default DevTools opens to the right of the demo.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/console-example-devtools-right-console.msft.png" alt-text="DevTools s’ouvre à droite de la démonstration." lightbox="../media/console-example-devtools-right-console.msft.png":::
             <span data-ttu-id="2ba34-117">DevTools s’ouvre à droite de la démonstration.</span><span class="sxs-lookup"><span data-stu-id="2ba34-117">DevTools opens to the right of the demo</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="2ba34-118">[Ancrez devtools en bas de la fenêtre][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="2ba34-118">[Dock DevTools to the bottom of the window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-bottom-console.msft.png" alt-text="DevTools ancré en bas de la démo" lightbox="../media/console-example-devtools-bottom-console.msft.png":::
             <span data-ttu-id="2ba34-120">DevTools ancré en bas de la démo</span><span class="sxs-lookup"><span data-stu-id="2ba34-120">DevTools docked to the bottom of the demo</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="2ba34-121">[Détacher devtools dans une fenêtre séparée][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="2ba34-121">[Undock DevTools into a separate window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-browse.msft.png" alt-text="Navigateur dans une fenêtre séparée" lightbox="../media/console-example-devtools-separate-console-browse.msft.png":::
             <span data-ttu-id="2ba34-123">Navigateur dans une fenêtre séparée</span><span class="sxs-lookup"><span data-stu-id="2ba34-123">Browser in a separate window</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="2ba34-124">[Détacher devtools dans une fenêtre séparée][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="2ba34-124">[Undock DevTools into a separate window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-devtools.msft.png" alt-text="DevTools non ancré dans une fenêtre séparée" lightbox="../media/console-example-devtools-separate-console-devtools.msft.png":::
             <span data-ttu-id="2ba34-126">DevTools non ancré dans une fenêtre séparée</span><span class="sxs-lookup"><span data-stu-id="2ba34-126">DevTools undocked in a separate window</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <span data-ttu-id="2ba34-127">Afficher les messages enregistrés depuis JavaScript</span><span class="sxs-lookup"><span data-stu-id="2ba34-127">View messages logged from JavaScript</span></span>   

<span data-ttu-id="2ba34-128">La plupart des messages que vous voyez dans la console proviennent des développeurs Web qui écrivent le JavaScript de la page.</span><span class="sxs-lookup"><span data-stu-id="2ba34-128">Most messages that you see in the Console come from the web developers who wrote the JavaScript of the page.</span></span>  <span data-ttu-id="2ba34-129">L’objectif de cette section consiste à vous présenter les différents types de messages que vous risquez de voir dans la console et à expliquer la façon dont vous pouvez enregistrer chaque type de message vous-même dans JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2ba34-129">The goal of this section is to introduce you to the different message types that you are likely to see in the Console, and explain how you may log each message type yourself from your own JavaScript.</span></span>  

1.  <span data-ttu-id="2ba34-130">Cliquez sur le bouton **informations du journal** dans la démonstration.</span><span class="sxs-lookup"><span data-stu-id="2ba34-130">Click the **Log Info** button in the demo.</span></span>  `Hello, Console!` <span data-ttu-id="2ba34-131">est connecté à la console.</span><span class="sxs-lookup"><span data-stu-id="2ba34-131">gets logged to the Console.</span></span>
    
    :::image type="complex" source="../media/console-log-info.msft.png" alt-text="La console après avoir cliqué sur informations du journal" lightbox="../media/console-log-info.msft.png":::
       <span data-ttu-id="2ba34-133">La **console** après avoir cliqué sur **informations du journal**</span><span class="sxs-lookup"><span data-stu-id="2ba34-133">The **Console** after clicking **Log Info**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2ba34-134">En regard du `Hello, Console!` message dans la console, cliquez sur **log.js:2**.</span><span class="sxs-lookup"><span data-stu-id="2ba34-134">Next to the `Hello, Console!` message in the Console click **log.js:2**.</span></span>  <span data-ttu-id="2ba34-135">Le panneau sources s’ouvre et met en surbrillance la ligne de code qui a entraîné le message à se connecter à la console.</span><span class="sxs-lookup"><span data-stu-id="2ba34-135">The Sources panel opens and highlights the line of code that caused the message to get logged to the Console.</span></span>  <span data-ttu-id="2ba34-136">Le message a été enregistré lors de l’exécution du code JavaScript de la page `console.log('Hello, Console!')` .</span><span class="sxs-lookup"><span data-stu-id="2ba34-136">The message was logged when the JavaScript of the page ran `console.log('Hello, Console!')`.</span></span>
    
    :::image type="complex" source="../media/console-sources-logjs.msft.png" alt-text="DevTools ouvre le panneau sources après avoir cliqué sur log.js:2" lightbox="../media/console-sources-logjs.msft.png":::
       <span data-ttu-id="2ba34-138">DevTools ouvre le panneau **sources** après avoir cliqué sur</span><span class="sxs-lookup"><span data-stu-id="2ba34-138">DevTools opens the **Sources** panel after you click</span></span> `log.js:2`  
    :::image-end:::  
    
1.  <span data-ttu-id="2ba34-139">Revenez à la **console** à l’aide de l’un des flux de travail suivants:</span><span class="sxs-lookup"><span data-stu-id="2ba34-139">Navigate back to the **Console** using any of the following workflows:</span></span>  
    
    *   <span data-ttu-id="2ba34-140">Cliquez sur l’onglet de la **console** .</span><span class="sxs-lookup"><span data-stu-id="2ba34-140">Click the **Console** tab.</span></span>  
    *   <span data-ttu-id="2ba34-141">Appuyez sur `Control` + `[` \ (Windows \) ou `Command` + `[` \ (MacOS \) jusqu’à ce que le panneau de la console ait le focus.</span><span class="sxs-lookup"><span data-stu-id="2ba34-141">Press `Control`+`[` \(Windows\) or `Command`+`[` \(macOS\) until the Console panel is in focus.</span></span>  
    *   <span data-ttu-id="2ba34-142">[Ouvrez le menu de commandes][DevToolsCommandMenu], commencez à taper `Console` , sélectionnez l’option **afficher le panneau** de la console, puis appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="2ba34-142">[Open the Command Menu][DevToolsCommandMenu], start typing `Console`, select the **Show Console Panel** command, and then press `Enter`.</span></span>  
    
1.  <span data-ttu-id="2ba34-143">Cliquez sur le bouton **Avertissement du journal** dans la démonstration.</span><span class="sxs-lookup"><span data-stu-id="2ba34-143">Click the **Log Warning** button in the demo.</span></span>  `Abandon Hope All Ye Who Enter` <span data-ttu-id="2ba34-144">est connecté à la console.</span><span class="sxs-lookup"><span data-stu-id="2ba34-144">gets logged to the Console.</span></span>  <span data-ttu-id="2ba34-145">Les messages mis en forme comme celui-ci sont des avertissements.</span><span class="sxs-lookup"><span data-stu-id="2ba34-145">Messages formatted like this are warnings.</span></span>  
    
    :::image type="complex" source="../media/console-log-warning.msft.png" alt-text="La console après avoir cliqué sur avertissement du journal" lightbox="../media/console-log-warning.msft.png":::
       <span data-ttu-id="2ba34-147">La **console** après avoir cliqué sur **Avertissement du journal**</span><span class="sxs-lookup"><span data-stu-id="2ba34-147">The **Console** after you click **Log Warning**</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="2ba34-148">Si vous souhaitez voir le code ayant entraîné l’enregistrement d’un message d’une certaine façon, cliquez sur un script (par exemple, `log.js:12` \) pour afficher le code ayant entraîné la mise en forme du message.</span><span class="sxs-lookup"><span data-stu-id="2ba34-148">If you want to see the code that caused a message to get logged a certain way, click on a script \(such as `log.js:12`\) to view the code that caused the message to get formatted.</span></span>  

1.  <span data-ttu-id="2ba34-149">Cliquez sur l’icône **développer** \ ( ![ développer ][ImageExpandIcon] \) devant `Abandon Hope All Ye Who Enter` .</span><span class="sxs-lookup"><span data-stu-id="2ba34-149">Click the **Expand** \(![Expand][ImageExpandIcon]\) icon in front of `Abandon Hope All Ye Who Enter`.</span></span>  <span data-ttu-id="2ba34-150">DevTools affiche la [trace de pile][WikiStackTrace] qui se trouve au début de l’appel.</span><span class="sxs-lookup"><span data-stu-id="2ba34-150">DevTools shows the [stack trace][WikiStackTrace] leading up to the call.</span></span>  
    
    :::image type="complex" source="../media/console-log-warning-expanded.msft.png" alt-text="Une trace de pile" lightbox="../media/console-log-warning-expanded.msft.png":::
       <span data-ttu-id="2ba34-152">Une trace de pile</span><span class="sxs-lookup"><span data-stu-id="2ba34-152">A stack trace</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="2ba34-153">La trace de pile vous indique qu’une fonction nommée `logWarning` a été appelée, qui à son tour appelait une fonction nommée `quoteDante` .</span><span class="sxs-lookup"><span data-stu-id="2ba34-153">The stack trace is telling you that a function named `logWarning` was called, which in turn called a function named `quoteDante`.</span></span>  <span data-ttu-id="2ba34-154">En d’autres termes, l’appel qui s’est produit en premier est en bas de la trace de pile.</span><span class="sxs-lookup"><span data-stu-id="2ba34-154">In other words, the call that happened first is at the bottom of the stack trace.</span></span>  <span data-ttu-id="2ba34-155">Vous pouvez enregistrer des traces de pile à tout moment en les appelant `console.trace()` .</span><span class="sxs-lookup"><span data-stu-id="2ba34-155">You may log stack traces at any time by calling `console.trace()`.</span></span>  

1.  <span data-ttu-id="2ba34-156">Cliquez sur **erreur de connexion**.</span><span class="sxs-lookup"><span data-stu-id="2ba34-156">Click **Log Error**.</span></span>  <span data-ttu-id="2ba34-157">Le message d’erreur suivant s’affiche:</span><span class="sxs-lookup"><span data-stu-id="2ba34-157">The following error message gets logged:</span></span> `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    :::image type="complex" source="../media/console-log-error.msft.png" alt-text="Un message d’erreur" lightbox="../media/console-log-error.msft.png":::
       <span data-ttu-id="2ba34-159">Un message d’erreur</span><span class="sxs-lookup"><span data-stu-id="2ba34-159">An error message</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2ba34-160">Cliquez sur **table du journal**.</span><span class="sxs-lookup"><span data-stu-id="2ba34-160">Click **Log Table**.</span></span>  <span data-ttu-id="2ba34-161">Un tableau sur les artistes célèbres est connecté à la console.</span><span class="sxs-lookup"><span data-stu-id="2ba34-161">A table about famous artists gets logged to the Console.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="2ba34-162">La `birthday` colonne est uniquement remplie pour une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="2ba34-162">The `birthday` column is only populated for one row.</span></span>  <span data-ttu-id="2ba34-163">Révisez le code pour déterminer la raison pour laquelle il s’agit.</span><span class="sxs-lookup"><span data-stu-id="2ba34-163">Review the code to determine why that is.</span></span>
    
    :::image type="complex" source="../media/console-log-table.msft.png" alt-text="Tableau sur la console" lightbox="../media/console-log-table.msft.png":::
       <span data-ttu-id="2ba34-165">Tableau sur la **console**</span><span class="sxs-lookup"><span data-stu-id="2ba34-165">A table in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2ba34-166">Cliquez sur **groupe de journaux**.</span><span class="sxs-lookup"><span data-stu-id="2ba34-166">Click **Log Group**.</span></span>  <span data-ttu-id="2ba34-167">Les noms des 4 plus célèbres et des tortues sont regroupés sous l' `Adolescent Irradiated Espionage Tortoises` étiquette.</span><span class="sxs-lookup"><span data-stu-id="2ba34-167">The names of 4 famous, crime-fighting turtles are grouped under the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  
    
    :::image type="complex" source="../media/console-log-group.msft.png" alt-text="Groupe de messages dans la console" lightbox="../media/console-log-group.msft.png":::
       <span data-ttu-id="2ba34-169">Groupe de messages dans la **console**</span><span class="sxs-lookup"><span data-stu-id="2ba34-169">A group of messages in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2ba34-170">Cliquez sur **journal personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="2ba34-170">Click **Log Custom**.</span></span>  <span data-ttu-id="2ba34-171">Un message avec une bordure rouge et un arrière-plan bleu est connecté à la console.</span><span class="sxs-lookup"><span data-stu-id="2ba34-171">A message with a red border and blue background gets logged to the Console.</span></span>  
    
    :::image type="complex" source="../media/console-log-custom.msft.png" alt-text="Message avec une mise en forme personnalisée dans la console" lightbox="../media/console-log-custom.msft.png":::
       <span data-ttu-id="2ba34-173">Message avec une mise en forme personnalisée dans la **console**</span><span class="sxs-lookup"><span data-stu-id="2ba34-173">A message with custom formatting in the **Console**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="2ba34-174">Le principe principal est le suivant: lorsque vous souhaitez consigner des messages dans la console à partir de votre JavaScript, vous utilisez l’une des `console` méthodes.</span><span class="sxs-lookup"><span data-stu-id="2ba34-174">The main idea here is that when you want to log messages to the Console from your JavaScript, you use one of the `console` methods.</span></span>  <span data-ttu-id="2ba34-175">Chaque méthode met en forme les messages différemment.</span><span class="sxs-lookup"><span data-stu-id="2ba34-175">Each method formats messages differently.</span></span>  

<span data-ttu-id="2ba34-176">Il existe encore plus de méthodes que celles présentées dans cette section.</span><span class="sxs-lookup"><span data-stu-id="2ba34-176">There are even more methods than what has been demonstrated in this section.</span></span>  <span data-ttu-id="2ba34-177">Ce didacticiel vous explique comment découvrir le reste des méthodes.</span><span class="sxs-lookup"><span data-stu-id="2ba34-177">This tutorial shows you how to explore the rest of the methods.</span></span>  

## <span data-ttu-id="2ba34-178">Afficher les messages enregistrés par le navigateur</span><span class="sxs-lookup"><span data-stu-id="2ba34-178">View messages logged by the browser</span></span>   

<span data-ttu-id="2ba34-179">Le navigateur enregistre également les messages sur la console.</span><span class="sxs-lookup"><span data-stu-id="2ba34-179">The browser logs messages to the Console, too.</span></span>  <span data-ttu-id="2ba34-180">Cela se produit généralement lorsque la page rencontre un problème.</span><span class="sxs-lookup"><span data-stu-id="2ba34-180">This usually happens when there is a problem with the page.</span></span>  

1.  <span data-ttu-id="2ba34-181">Cliquez sur **Cause 404**.</span><span class="sxs-lookup"><span data-stu-id="2ba34-181">Click **Cause 404**.</span></span>  <span data-ttu-id="2ba34-182">Le navigateur enregistre un code d’état HTTP d' `404` erreur réseau, car le code JavaScript de la page essayait de récupérer un fichier qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="2ba34-182">The browser logs an HTTP status code of `404` network error because the JavaScript of the page tried to fetch a file that does not exist.</span></span>  
    
    :::image type="complex" source="../media/console-cause-404.msft.png" alt-text="Erreur 404 dans la console" lightbox="../media/console-cause-404.msft.png":::
       <span data-ttu-id="2ba34-184">`404`Erreur dans la **console**</span><span class="sxs-lookup"><span data-stu-id="2ba34-184">A `404` error in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2ba34-185">Cliquez sur **provoquer une erreur**.</span><span class="sxs-lookup"><span data-stu-id="2ba34-185">Click **Cause Error**.</span></span>  <span data-ttu-id="2ba34-186">Le navigateur enregistre une incapture `TypeError` car JavaScript tente de mettre à jour un nœud DOM qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="2ba34-186">The browser logs an uncaught `TypeError` because the JavaScript is trying to update a DOM node that does not exist.</span></span>  
    
    :::image type="complex" source="../media/console-cause-error.msft.png" alt-text="A TypeError dans la console" lightbox="../media/console-cause-error.msft.png":::
       <span data-ttu-id="2ba34-188">A `TypeError` sur la **console**</span><span class="sxs-lookup"><span data-stu-id="2ba34-188">A `TypeError` in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2ba34-189">Cliquez sur la liste déroulante **niveaux du journal** et activez l’option **détaillé** s’il est désactivé.</span><span class="sxs-lookup"><span data-stu-id="2ba34-189">Click the **Log Levels** dropdown and enable the **Verbose** option if it is disabled.</span></span>  <span data-ttu-id="2ba34-190">Pour plus d’informations sur le filtrage, voir la section suivante.</span><span class="sxs-lookup"><span data-stu-id="2ba34-190">You learn more about filtering in the next section.</span></span>  <span data-ttu-id="2ba34-191">Vous devez effectuer cette opération pour vérifier que le message suivant que vous enregistrez est visible.</span><span class="sxs-lookup"><span data-stu-id="2ba34-191">You need to do this to make sure that the next message you log is visible.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="2ba34-192">Si la liste déroulante niveaux par défaut est désactivée, vous devrez peut-être fermer **la barre latérale** .</span><span class="sxs-lookup"><span data-stu-id="2ba34-192">If the Default Levels dropdown is disabled, you may need to close the **Console** Sidebar.</span></span>  <span data-ttu-id="2ba34-193">Filtrer par source de message ci-dessous pour plus d’informations sur la barre latérale de la **console** .</span><span class="sxs-lookup"><span data-stu-id="2ba34-193">Filter by Message Source below for more information about the **Console** Sidebar.</span></span>
    
    :::image type="complex" source="../media/console-cause-error-log-levels.msft.png" alt-text="Activer le niveau de journalisation détaillé" lightbox="../media/console-cause-error-log-levels.msft.png":::
       <span data-ttu-id="2ba34-195">Activer le niveau de journalisation détaillé</span><span class="sxs-lookup"><span data-stu-id="2ba34-195">Enabling the Verbose log level</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2ba34-196">Cliquez sur **provoquer une violation**.</span><span class="sxs-lookup"><span data-stu-id="2ba34-196">Click **Cause Violation**.</span></span>  <span data-ttu-id="2ba34-197">La page cesse de répondre pendant quelques secondes, puis le navigateur enregistre le message `[Violation] 'click' handler took 3000ms` sur la console.</span><span class="sxs-lookup"><span data-stu-id="2ba34-197">The page becomes unresponsive for a few seconds and then the browser logs the message `[Violation] 'click' handler took 3000ms` to the Console.</span></span>  <span data-ttu-id="2ba34-198">La durée exacte est variable.</span><span class="sxs-lookup"><span data-stu-id="2ba34-198">The exact duration may vary.</span></span>  
    
    :::image type="complex" source="../media/console-cause-violation.msft.png" alt-text="Violation dans la console" lightbox="../media/console-cause-violation.msft.png":::
       <span data-ttu-id="2ba34-200">Violation dans la **console**</span><span class="sxs-lookup"><span data-stu-id="2ba34-200">A violation in the **Console**</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="2ba34-201">Filtrer les messages</span><span class="sxs-lookup"><span data-stu-id="2ba34-201">Filter messages</span></span>   

<span data-ttu-id="2ba34-202">Dans certaines pages, la console est inondée de messages.</span><span class="sxs-lookup"><span data-stu-id="2ba34-202">On some pages you see the Console get flooded with messages.</span></span>  <span data-ttu-id="2ba34-203">DevTools offre différentes façons de filtrer les messages qui ne sont pas pertinents pour la tâche en cours.</span><span class="sxs-lookup"><span data-stu-id="2ba34-203">DevTools provides many different ways to filter out messages that are not relevant to the task at hand.</span></span>  

### <span data-ttu-id="2ba34-204">Filtrer par niveau de journal</span><span class="sxs-lookup"><span data-stu-id="2ba34-204">Filter by log level</span></span>   

<span data-ttu-id="2ba34-205">`console`Un niveau de gravité est attribué à chaque méthode: `Verbose` , `Info` , `Warning` ou `Error` .</span><span class="sxs-lookup"><span data-stu-id="2ba34-205">Each `console` method is assigned a severity level: `Verbose`, `Info`, `Warning`, or `Error`.</span></span>  <span data-ttu-id="2ba34-206">Par exemple, `console.log()` il s’agit d’un `Info` message de `console.error()` niveau supérieur `Error` .</span><span class="sxs-lookup"><span data-stu-id="2ba34-206">For example, `console.log()` is an `Info`-level message, whereas `console.error()` is an `Error`-level message.</span></span>  

1.  <span data-ttu-id="2ba34-207">Cliquez sur la liste déroulante **niveaux du journal** et désactivez **Erreurs**.</span><span class="sxs-lookup"><span data-stu-id="2ba34-207">Click the **Log Levels** dropdown and disable **Errors**.</span></span>  <span data-ttu-id="2ba34-208">Un niveau est désactivé quand il n’y a plus de coche en regard de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="2ba34-208">A level is disabled when there is no longer a checkmark next to it.</span></span>  <span data-ttu-id="2ba34-209">Les `Error` messages de niveau disparaissent.</span><span class="sxs-lookup"><span data-stu-id="2ba34-209">The `Error`-level messages disappear.</span></span>  
    
    :::image type="complex" source="../media/console-cause-violation-log-levels.msft.png" alt-text="Désactivation des messages de niveau erreur dans la console" lightbox="../media/console-cause-violation-log-levels.msft.png":::
       <span data-ttu-id="2ba34-211">Désactivation des messages de niveau erreur dans la **console**</span><span class="sxs-lookup"><span data-stu-id="2ba34-211">Disabling Error-level messages in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2ba34-212">Cliquez de nouveau sur la liste déroulante **niveaux du journal** et activez de nouveau les **Erreurs**.</span><span class="sxs-lookup"><span data-stu-id="2ba34-212">Click the **Log Levels** dropdown again and re-enable **Errors**.</span></span>  <span data-ttu-id="2ba34-213">Les `Error` messages de niveau supérieur apparaissent.</span><span class="sxs-lookup"><span data-stu-id="2ba34-213">The `Error`-level messages reappear.</span></span>  

### <span data-ttu-id="2ba34-214">Filtrer par texte</span><span class="sxs-lookup"><span data-stu-id="2ba34-214">Filter by text</span></span>   

<span data-ttu-id="2ba34-215">Lorsque vous souhaitez uniquement afficher les messages qui incluent une chaîne exacte, tapez cette chaîne dans la zone de texte du **filtre** .</span><span class="sxs-lookup"><span data-stu-id="2ba34-215">When you want to only view messages that include an exact string, type that string into the **Filter** text box.</span></span>  

1.  <span data-ttu-id="2ba34-216">Entrez `Dave` dans la zone de texte du **filtre** .</span><span class="sxs-lookup"><span data-stu-id="2ba34-216">Type `Dave` into the **Filter** text box.</span></span>  <span data-ttu-id="2ba34-217">Tous les messages n’incluant pas la chaîne `Dave` sont masqués.</span><span class="sxs-lookup"><span data-stu-id="2ba34-217">All messages that do not include the string `Dave` are hidden.</span></span>  <span data-ttu-id="2ba34-218">Vous pouvez également voir l' `Adolescent Irradiated Espionage Tortoises` étiquette.</span><span class="sxs-lookup"><span data-stu-id="2ba34-218">You might also see the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  <span data-ttu-id="2ba34-219">Il s’agit d’un bogue.</span><span class="sxs-lookup"><span data-stu-id="2ba34-219">That is a bug.</span></span>  
    
    :::image type="complex" source="../media/console-all-messages-text-filter.msft.png" alt-text="Le filtrage des messages n’incluant pas Dave" lightbox="../media/console-all-messages-text-filter.msft.png":::
       <span data-ttu-id="2ba34-221">Filtrage des messages n’incluant pas</span><span class="sxs-lookup"><span data-stu-id="2ba34-221">Filtering out any message that does not include</span></span> `Dave`  
    :::image-end:::  
    
1.  <span data-ttu-id="2ba34-222">Supprimer `Dave` de la zone de texte du **filtre** .</span><span class="sxs-lookup"><span data-stu-id="2ba34-222">Delete `Dave` from the **Filter** text box.</span></span>  <span data-ttu-id="2ba34-223">Tous les messages réapparaissent.</span><span class="sxs-lookup"><span data-stu-id="2ba34-223">All the messages reappear.</span></span>  

### <span data-ttu-id="2ba34-224">Filtrer par expression régulière</span><span class="sxs-lookup"><span data-stu-id="2ba34-224">Filter by regular expression</span></span>   

<span data-ttu-id="2ba34-225">Pour afficher tous les messages qui incluent un modèle de texte plutôt qu’une chaîne spécifique, utilisez une [expression régulière][MDNRegularExpressions].</span><span class="sxs-lookup"><span data-stu-id="2ba34-225">When you want to show all messages that include a pattern of text, rather than a specific string, use a [regular expression][MDNRegularExpressions].</span></span>  

1.  <span data-ttu-id="2ba34-226">Entrez `/^[AH]/` dans la zone de texte du **filtre** .</span><span class="sxs-lookup"><span data-stu-id="2ba34-226">Type `/^[AH]/` into the **Filter** text box.</span></span>  <span data-ttu-id="2ba34-227">Tapez ce modèle dans [Regex][|::ref1::|Main] pour obtenir une explication de ce qu’il fait.</span><span class="sxs-lookup"><span data-stu-id="2ba34-227">Type this pattern into [RegExr][|::ref1::|Main] for an explanation of what it is doing.</span></span>  
    
    :::image type="complex" source="../media/console-all-messages-regex-filter.msft.png" alt-text="Filtrage de tout message ne correspondant à aucun critère" lightbox="../media/console-all-messages-regex-filter.msft.png":::
       <span data-ttu-id="2ba34-229">Filtrage de tout message ne correspondant pas au modèle</span><span class="sxs-lookup"><span data-stu-id="2ba34-229">Filtering out any message that does not match the pattern</span></span> `/^[AH]/`  
    :::image-end:::  
    
1.  <span data-ttu-id="2ba34-230">Supprimer `/^[AH]/` de la zone de texte du **filtre** .</span><span class="sxs-lookup"><span data-stu-id="2ba34-230">Delete `/^[AH]/` from the **Filter** text box.</span></span>  <span data-ttu-id="2ba34-231">Tous les messages sont de nouveau visibles.</span><span class="sxs-lookup"><span data-stu-id="2ba34-231">All messages are visible again.</span></span>  

### <span data-ttu-id="2ba34-232">Filtrer par source de message</span><span class="sxs-lookup"><span data-stu-id="2ba34-232">Filter by message source</span></span>   

<span data-ttu-id="2ba34-233">Pour afficher uniquement les messages provenant d’une URL spécifique, utilisez la **barre latérale**.</span><span class="sxs-lookup"><span data-stu-id="2ba34-233">When you want to only view the messages that came from a certain URL, use the **Sidebar**.</span></span>  

1.  <span data-ttu-id="2ba34-234">Cliquez sur **afficher la barre latérale** de la console ![ ][ImageShowConsoleSidebarIcon] .</span><span class="sxs-lookup"><span data-stu-id="2ba34-234">Click **Show Console Sidebar** \(![Show Console Sidebar][ImageShowConsoleSidebarIcon]\).</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-all-messages.msft.png" alt-text="Barre latérale" lightbox="../media/console-sidebar-all-messages.msft.png":::
       <span data-ttu-id="2ba34-236">Barre latérale</span><span class="sxs-lookup"><span data-stu-id="2ba34-236">The Sidebar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2ba34-237">Cliquez sur l’icône **développer** \ ( ![ développer ][ImageExpandIcon] \) en regard du nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="2ba34-237">Click the **Expand** \(![Expand][ImageExpandIcon]\) icon next to the number of messages.</span></span>  <span data-ttu-id="2ba34-238">Dans l’illustration suivante, le nombre de messages est indiqué par **13 messages**.</span><span class="sxs-lookup"><span data-stu-id="2ba34-238">In the following figure, the number of messages is indicated as **13 Messages**.</span></span>  <span data-ttu-id="2ba34-239">La **barre latérale** affiche une liste des URL ayant entraîné la journalisation des messages.</span><span class="sxs-lookup"><span data-stu-id="2ba34-239">The **Sidebar** shows a list of URLs that caused messages to be logged.</span></span>  <span data-ttu-id="2ba34-240">Par exemple, il `log.js` a généré 11 messages.</span><span class="sxs-lookup"><span data-stu-id="2ba34-240">For example, `log.js` caused 11 messages.</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-expanded-all-messages.msft.png" alt-text="Affichage de la source de messages dans la barre latérale" lightbox="../media/console-sidebar-expanded-all-messages.msft.png":::
       <span data-ttu-id="2ba34-242">Affichage de la source de messages dans la barre latérale</span><span class="sxs-lookup"><span data-stu-id="2ba34-242">Viewing the source of messages in the Sidebar</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="2ba34-243">Filtrer par message utilisateur</span><span class="sxs-lookup"><span data-stu-id="2ba34-243">Filter by user messages</span></span>   

<span data-ttu-id="2ba34-244">Auparavant, lorsque vous cliquiez sur informations sur le **Journal**, un script appelé pour `console.log('Hello, Console!')` consigner le message sur la console.</span><span class="sxs-lookup"><span data-stu-id="2ba34-244">Earlier, when you clicked **Log Info**, a script called `console.log('Hello, Console!')` in order to log the message to the Console.</span></span>  <span data-ttu-id="2ba34-245">Les messages enregistrés depuis JavaScript comme celui-ci s’appelle **messages utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="2ba34-245">Messages logged from JavaScript like this are called **user messages**.</span></span>  <span data-ttu-id="2ba34-246">En revanche, lorsque vous avez cliqué sur **Cause 404**, le navigateur a enregistré un `Error` message de niveau indiquant que la ressource demandée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="2ba34-246">In contrast, when you clicked **Cause 404**, the browser logged an `Error`-level message stating that the requested resource could not be found.</span></span>  <span data-ttu-id="2ba34-247">Les messages comme les **messages du navigateur**.</span><span class="sxs-lookup"><span data-stu-id="2ba34-247">Messages like that are considered **browser messages**.</span></span>  <span data-ttu-id="2ba34-248">Utilisez la **barre latérale** pour filtrer les messages de navigateur et afficher uniquement les messages utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="2ba34-248">Use the **Sidebar** to filter out browser messages and only show user messages.</span></span>  

1.  <span data-ttu-id="2ba34-249">Cliquez sur **9 messages utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="2ba34-249">Click **9 User Messages**.</span></span>  <span data-ttu-id="2ba34-250">Les messages de navigateur sont masqués.</span><span class="sxs-lookup"><span data-stu-id="2ba34-250">The browser messages are hidden.</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-user-messages.msft.png" alt-text="Filtrage des messages de navigateur" lightbox="../media/console-sidebar-user-messages.msft.png":::
       <span data-ttu-id="2ba34-252">Filtrage des messages de navigateur</span><span class="sxs-lookup"><span data-stu-id="2ba34-252">Filtering out browser messages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2ba34-253">Cliquez sur **13 messages** pour afficher de nouveau tous les messages.</span><span class="sxs-lookup"><span data-stu-id="2ba34-253">Click **13 Messages** to show all messages again.</span></span>  

## <span data-ttu-id="2ba34-254">Utiliser la console en même temps que d’autres panneaux</span><span class="sxs-lookup"><span data-stu-id="2ba34-254">Use the Console alongside any other panel</span></span>   

<span data-ttu-id="2ba34-255">Que se passe-t-il si vous modifiez les styles, mais vous avez besoin de consulter rapidement le journal de la console pour obtenir un élément?</span><span class="sxs-lookup"><span data-stu-id="2ba34-255">What if you are editing styles, but you need to quickly check the Console log for something?</span></span> <span data-ttu-id="2ba34-256">Utiliser le tiroir.</span><span class="sxs-lookup"><span data-stu-id="2ba34-256">Use the Drawer.</span></span>  

1.  <span data-ttu-id="2ba34-257">Cliquez sur l’onglet **éléments** .</span><span class="sxs-lookup"><span data-stu-id="2ba34-257">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="2ba34-258">Appuyez sur `Escape` .</span><span class="sxs-lookup"><span data-stu-id="2ba34-258">Press `Escape`.</span></span>  <span data-ttu-id="2ba34-259">L’onglet Console du **tiroir** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="2ba34-259">The Console tab of the **Drawer** opens.</span></span>  <span data-ttu-id="2ba34-260">Toutes les fonctionnalités du panneau de la console que vous avez utilisées tout au long de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="2ba34-260">It has all of the features of the Console panel that you have been using throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/console-elements-drawer-console-sidebar-all-messages.msft.png" alt-text="Onglet Console du tiroir" lightbox="../media/console-elements-drawer-console-sidebar-all-messages.msft.png":::
         <span data-ttu-id="2ba34-262">Onglet **console** du **tiroir**</span><span class="sxs-lookup"><span data-stu-id="2ba34-262">The **Console** tab in the **Drawer**</span></span>  
    :::image-end:::  
    
<!--## Next steps  -->

<!--
*   See [Console Reference][DevToolsConsoleApi] to explore more features and workflows related to the Console UI.
*   See [Console API Reference][DevToolsConsoleReference] to learn more about all of the `console` methods that were demonstrated in [View messages logged from JavaScript(#view-messages-logged-from-javascript) and explore the other `console` methods that were not covered in this tutorial.  
*   See [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  

<!--
 


-->  

<!-- image links -->  

[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge \ (chrome \) | Documents Microsoft"  
[DevToolsCommandMenu]: ../command-menu/index.md "Exécuter des commandes à l’aide du menu de commandes de Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Changer la position de Microsoft Edge DevTools Documents Microsoft"  
[DevToolsConsoleApi]: ./api.md "Référence sur les API de console | Documents Microsoft"  
[DevToolsConsoleReference]: ./reference.md "Référence de la console | Documents Microsoft"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Commencer à utiliser la journalisation des messages | Problème"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Expressions régulières | MDN"  

[RegExrMain]: https://regexr.com "RegEx"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Trace de pile-Wikipédia"  


> [!NOTE]
> <span data-ttu-id="2ba34-272">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2ba34-272">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2ba34-273">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/log) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="2ba34-273">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/log) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="2ba34-275">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2ba34-275">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
