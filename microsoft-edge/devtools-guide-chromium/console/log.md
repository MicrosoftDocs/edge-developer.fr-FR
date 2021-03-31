---
description: Découvrez comment enregistrer des messages dans la console.
title: Commencer à journalisation des messages dans la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: fb428154b00959db1627096819c565dd5dc11346
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439288"
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

# <a name="get-started-with-logging-messages-in-the-console"></a><span data-ttu-id="f32b8-104">Commencer à journalisation des messages dans la console</span><span class="sxs-lookup"><span data-stu-id="f32b8-104">Get started with logging messages in the Console</span></span>  

<span data-ttu-id="f32b8-105">Ce didacticiel interactif vous montre comment enregistrer et filtrer des messages dans la console [Microsoft Edge DevTools.][MicrosoftEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="f32b8-105">This interactive tutorial shows you how to log and filter messages in the [Microsoft Edge DevTools][MicrosoftEdgeDevTools] console.</span></span>  

:::image type="complex" source="../media/console-ars-technica-console-onload.msft.png" alt-text="Messages dans la console" lightbox="../media/console-ars-technica-console-onload.msft.png":::
   <span data-ttu-id="f32b8-107">Messages dans la **console**</span><span class="sxs-lookup"><span data-stu-id="f32b8-107">Messages in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="f32b8-108">Ce didacticiel est destiné à être terminé dans l’ordre.</span><span class="sxs-lookup"><span data-stu-id="f32b8-108">This tutorial is intended to be completed in order.</span></span>  <span data-ttu-id="f32b8-109">Il part du principe que vous comprenez les principes de base du développement web, comme l’utilisation de JavaScript pour ajouter de l’interactivité à une page.</span><span class="sxs-lookup"><span data-stu-id="f32b8-109">It assumes that you understand the fundamentals of web development, such as how to use JavaScript to add interactivity to a page.</span></span>  

## <a name="set-up-the-demo-and-devtools"></a><span data-ttu-id="f32b8-110">Configurer la démonstration et DevTools</span><span class="sxs-lookup"><span data-stu-id="f32b8-110">Set up the demo and DevTools</span></span>  

<span data-ttu-id="f32b8-111">Ce didacticiel est conçu pour vous permettre d’ouvrir la démonstration et d’essayer tous les flux de travail vous-même.</span><span class="sxs-lookup"><span data-stu-id="f32b8-111">This tutorial is designed so that you are able to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="f32b8-112">Lorsque vous suivez physiquement le processus, vous êtes plus susceptible de mémoriser les flux de travail ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="f32b8-112">When you physically follow along, you are more likely to remember the workflows later.</span></span>  

1.  <span data-ttu-id="f32b8-113">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **Console Log Examples** to open in a new tab.</span><span class="sxs-lookup"><span data-stu-id="f32b8-113">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **Console Log Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="f32b8-114">Exemples de journaux de console</span><span class="sxs-lookup"><span data-stu-id="f32b8-114">Console Log Examples</span></span>][GlitchDevToolsConsoleLogExamples]
    
    <!--
    > [!TIP]
    > Move the demo to a separate window.  
    > 
    > :::image type="complex" source="../media/log-set-up-1.msft.png" alt-text="The tutorial on the left, and the demo on the right" lightbox="../media/log-set-up-1.msft.png":::
    >    The tutorial on the left, and the demo on the right  
    > :::image-end:::  
    -->
    
1.  <span data-ttu-id="f32b8-115">Concentrez la démonstration, puis sélectionnez `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\) pour ouvrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="f32b8-115">Focus the demo and then select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\) to open DevTools.</span></span>  <span data-ttu-id="f32b8-116">Par défaut, DevTools s’ouvre à droite de la démonstration.</span><span class="sxs-lookup"><span data-stu-id="f32b8-116">By default DevTools opens to the right of the demo.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/console-example-devtools-right-console.msft.png" alt-text="DevTools s’ouvre à droite de la démonstration" lightbox="../media/console-example-devtools-right-console.msft.png":::
             <span data-ttu-id="f32b8-118">DevTools s’ouvre à droite de la démonstration</span><span class="sxs-lookup"><span data-stu-id="f32b8-118">DevTools opens to the right of the demo</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="f32b8-119">[Ancrez DevTools en bas de la fenêtre.][DevToolsCustomizePlacement]</span><span class="sxs-lookup"><span data-stu-id="f32b8-119">[Dock DevTools to the bottom of the window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-bottom-console.msft.png" alt-text="DevTools docked to the bottom of the demo" lightbox="../media/console-example-devtools-bottom-console.msft.png":::
             <span data-ttu-id="f32b8-121">DevTools docked to the bottom of the demo</span><span class="sxs-lookup"><span data-stu-id="f32b8-121">DevTools docked to the bottom of the demo</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="f32b8-122">[Undock DevTools dans une fenêtre distincte.][DevToolsCustomizePlacement]</span><span class="sxs-lookup"><span data-stu-id="f32b8-122">[Undock DevTools into a separate window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-browse.msft.png" alt-text="Navigateur dans une fenêtre distincte" lightbox="../media/console-example-devtools-separate-console-browse.msft.png":::
             <span data-ttu-id="f32b8-124">Navigateur dans une fenêtre distincte</span><span class="sxs-lookup"><span data-stu-id="f32b8-124">Browser in a separate window</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="f32b8-125">[Undock DevTools dans une fenêtre distincte.][DevToolsCustomizePlacement]</span><span class="sxs-lookup"><span data-stu-id="f32b8-125">[Undock DevTools into a separate window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-devtools.msft.png" alt-text="DevTools non barraté dans une fenêtre distincte" lightbox="../media/console-example-devtools-separate-console-devtools.msft.png":::
             <span data-ttu-id="f32b8-127">DevTools non barraté dans une fenêtre distincte</span><span class="sxs-lookup"><span data-stu-id="f32b8-127">DevTools undocked in a separate window</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <a name="view-messages-logged-from-javascript"></a><span data-ttu-id="f32b8-128">Afficher les messages enregistrés à partir de JavaScript</span><span class="sxs-lookup"><span data-stu-id="f32b8-128">View messages logged from JavaScript</span></span>  

<span data-ttu-id="f32b8-129">La plupart des messages affichés dans la **console** proviennent des développeurs web qui ont écrit le JavaScript de la page.</span><span class="sxs-lookup"><span data-stu-id="f32b8-129">Most messages that are displayed in the **Console** come from the web developers who wrote the JavaScript of the page.</span></span>  <span data-ttu-id="f32b8-130">L’objectif de cette section est de vous présenter les différents types de messages que vous êtes susceptible de passer en revue dans la **console**et d’expliquer comment vous pouvez enregistrer chaque type de message vous-même à partir de votre propre javaScript.</span><span class="sxs-lookup"><span data-stu-id="f32b8-130">The goal of this section is to introduce you to the different message types that you are likely to review in the **Console**, and explain how you may log each message type yourself from your own JavaScript.</span></span>  

1.  <span data-ttu-id="f32b8-131">Sélectionnez **le bouton Informations sur** le journal dans la démonstration.</span><span class="sxs-lookup"><span data-stu-id="f32b8-131">Choose the **Log Info** button in the demo.</span></span>  `Hello, Console!` <span data-ttu-id="f32b8-132">est consigné dans la console.</span><span class="sxs-lookup"><span data-stu-id="f32b8-132">gets logged to the Console.</span></span>
    
    :::image type="complex" source="../media/console-log-info.msft.png" alt-text="Console après avoir choisi Les informations du journal" lightbox="../media/console-log-info.msft.png":::
       <span data-ttu-id="f32b8-134">Console **après** avoir choisi Les **informations du journal**</span><span class="sxs-lookup"><span data-stu-id="f32b8-134">The **Console** after you choose **Log Info**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f32b8-135">En face du `Hello, Console!` message dans la console, choisissez **log.js:2**.</span><span class="sxs-lookup"><span data-stu-id="f32b8-135">Next to the `Hello, Console!` message in the Console choose **log.js:2**.</span></span>  <span data-ttu-id="f32b8-136">Le panneau Sources s’ouvre et met en évidence la ligne de code à l’origine de la consigner dans la console.</span><span class="sxs-lookup"><span data-stu-id="f32b8-136">The Sources panel opens and highlights the line of code that caused the message to get logged to the Console.</span></span>  <span data-ttu-id="f32b8-137">Le message a été consigné lorsque le JavaScript de la page a été en cours `console.log('Hello, Console!')` d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="f32b8-137">The message was logged when the JavaScript of the page ran `console.log('Hello, Console!')`.</span></span>
    
    :::image type="complex" source="../media/console-sources-logjs.msft.png" alt-text="DevTools ouvre l’outil Sources après avoir choisi log.js:2" lightbox="../media/console-sources-logjs.msft.png":::
       <span data-ttu-id="f32b8-139">DevTools ouvre l’outil **Sources** une fois que vous avez choisi</span><span class="sxs-lookup"><span data-stu-id="f32b8-139">DevTools opens the **Sources** tool after you choose</span></span> `log.js:2`  
    :::image-end:::  
    
1.  <span data-ttu-id="f32b8-140">Revenir à la **console à l’aide** de l’un des flux de travail suivants :</span><span class="sxs-lookup"><span data-stu-id="f32b8-140">Navigate back to the **Console** using any of the following workflows:</span></span>  
    
    *   <span data-ttu-id="f32b8-141">Choisissez **l’outil Console.**</span><span class="sxs-lookup"><span data-stu-id="f32b8-141">Choose the **Console** tool.</span></span>  
    *   <span data-ttu-id="f32b8-142">Sélectionnez `Control` + `[` \(Windows, Linux\) ou `Command` + `[` \(macOS\)  jusqu’à ce que l’outil console soit en focus.</span><span class="sxs-lookup"><span data-stu-id="f32b8-142">Select `Control`+`[` \(Windows, Linux\) or `Command`+`[` \(macOS\) until the **Console** tool is in focus.</span></span>  
    *   <span data-ttu-id="f32b8-143">[Ouvrez le menu Commande,][DevToolsCommandMenu]tapez, choisissez la commande Afficher le panneau de `Console` **console,** puis sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="f32b8-143">[Open the Command Menu][DevToolsCommandMenu], type `Console`, choose the **Show Console Panel** command, and then select `Enter`.</span></span>  
    
1.  <span data-ttu-id="f32b8-144">Sélectionnez le **bouton Avertissement** du journal dans la démonstration.</span><span class="sxs-lookup"><span data-stu-id="f32b8-144">Choose the **Log Warning** button in the demo.</span></span>  `Abandon Hope All Ye Who Enter` <span data-ttu-id="f32b8-145">est consigné dans la **console**.</span><span class="sxs-lookup"><span data-stu-id="f32b8-145">gets logged to the **Console**.</span></span>  <span data-ttu-id="f32b8-146">Les messages formatés comme ceci sont des avertissements.</span><span class="sxs-lookup"><span data-stu-id="f32b8-146">Messages formatted like this are warnings.</span></span>  
    
    :::image type="complex" source="../media/console-log-warning.msft.png" alt-text="Console après avoir choisi Avertissement de journal" lightbox="../media/console-log-warning.msft.png":::
       <span data-ttu-id="f32b8-148">Console **après avoir** choisi Avertissement de **journal**</span><span class="sxs-lookup"><span data-stu-id="f32b8-148">The **Console** after you choose **Log Warning**</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="f32b8-149">Si vous souhaitez afficher le code à l’origine de la journalisé d’un message d’une certaine façon, choisissez un script \(tel que \) pour afficher le code à l’origine de la mise en forme du `log.js:12` message.</span><span class="sxs-lookup"><span data-stu-id="f32b8-149">If you want to display the code that caused a message to get logged a certain way, choose on a script \(such as `log.js:12`\) to view the code that caused the message to get formatted.</span></span>  

1.  <span data-ttu-id="f32b8-150">Choose the **Expand** \( ![ Expand ](../media/expand-icon.msft.png) \) icon in front of `Abandon Hope All Ye Who Enter` .</span><span class="sxs-lookup"><span data-stu-id="f32b8-150">Choose the **Expand** \(![Expand](../media/expand-icon.msft.png)\) icon in front of `Abandon Hope All Ye Who Enter`.</span></span>  <span data-ttu-id="f32b8-151">DevTools affiche la [trace de pile][WikiStackTrace] précédant l’appel.</span><span class="sxs-lookup"><span data-stu-id="f32b8-151">DevTools shows the [stack trace][WikiStackTrace] leading up to the call.</span></span>  
    
    :::image type="complex" source="../media/console-log-warning-expanded.msft.png" alt-text="Une trace de pile" lightbox="../media/console-log-warning-expanded.msft.png":::
       <span data-ttu-id="f32b8-153">Une trace de pile</span><span class="sxs-lookup"><span data-stu-id="f32b8-153">A stack trace</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="f32b8-154">La trace de pile vous dit qu’une fonction nommée est exécuté, qui à son tour `logWarning` exécute une fonction nommée `quoteDante` .</span><span class="sxs-lookup"><span data-stu-id="f32b8-154">The stack trace is telling you that a function named `logWarning` is run, which in turn runs a function named `quoteDante`.</span></span>  <span data-ttu-id="f32b8-155">En d’autres termes, la demande qui s’est produite en premier se trouve en bas de la trace de pile.</span><span class="sxs-lookup"><span data-stu-id="f32b8-155">In other words, the request that happened first is at the bottom of the stack trace.</span></span>  <span data-ttu-id="f32b8-156">Vous pouvez enregistrer les traces de pile à tout moment en exécutant `console.trace()` .</span><span class="sxs-lookup"><span data-stu-id="f32b8-156">You may log stack traces at any time by running `console.trace()`.</span></span>  

1.  <span data-ttu-id="f32b8-157">Choose **Log Error**.</span><span class="sxs-lookup"><span data-stu-id="f32b8-157">Choose **Log Error**.</span></span>  <span data-ttu-id="f32b8-158">Le message d’erreur suivant est consigné :</span><span class="sxs-lookup"><span data-stu-id="f32b8-158">The following error message gets logged:</span></span> `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    :::image type="complex" source="../media/console-log-error.msft.png" alt-text="Message d’erreur" lightbox="../media/console-log-error.msft.png":::
       <span data-ttu-id="f32b8-160">Message d’erreur</span><span class="sxs-lookup"><span data-stu-id="f32b8-160">An error message</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f32b8-161">Choose **Log Table**.</span><span class="sxs-lookup"><span data-stu-id="f32b8-161">Choose **Log Table**.</span></span>  <span data-ttu-id="f32b8-162">Un tableau sur ces derniers est enregistré sur la **console.**</span><span class="sxs-lookup"><span data-stu-id="f32b8-162">A table about famous artists gets logged to the **Console**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f32b8-163">La `birthday` colonne est remplie uniquement pour une ligne.</span><span class="sxs-lookup"><span data-stu-id="f32b8-163">The `birthday` column is only populated for one row.</span></span>  <span data-ttu-id="f32b8-164">Examinez le code pour en déterminer la raison.</span><span class="sxs-lookup"><span data-stu-id="f32b8-164">Review the code to determine why that is.</span></span>
    
    :::image type="complex" source="../media/console-log-table.msft.png" alt-text="Un tableau dans la console" lightbox="../media/console-log-table.msft.png":::
       <span data-ttu-id="f32b8-166">Un tableau dans la **console**</span><span class="sxs-lookup"><span data-stu-id="f32b8-166">A table in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f32b8-167">Choose **Log Group**.</span><span class="sxs-lookup"><span data-stu-id="f32b8-167">Choose **Log Group**.</span></span>  <span data-ttu-id="f32b8-168">Les noms de 4 personnes qui se disputent la violence sont regroupés sous `Adolescent Irradiated Espionage Tortoises` l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="f32b8-168">The names of 4 famous, crime-fighting turtles are grouped under the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  
    
    :::image type="complex" source="../media/console-log-group.msft.png" alt-text="Un groupe de messages dans la console" lightbox="../media/console-log-group.msft.png":::
       <span data-ttu-id="f32b8-170">Un groupe de messages dans la **console**</span><span class="sxs-lookup"><span data-stu-id="f32b8-170">A group of messages in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f32b8-171">Choose **Log Custom**.</span><span class="sxs-lookup"><span data-stu-id="f32b8-171">Choose **Log Custom**.</span></span>  <span data-ttu-id="f32b8-172">Un message avec une bordure rouge et un arrière-plan bleu est enregistré dans la console.</span><span class="sxs-lookup"><span data-stu-id="f32b8-172">A message with a red border and blue background gets logged to the Console.</span></span>  
    
    :::image type="complex" source="../media/console-log-custom.msft.png" alt-text="Message avec mise en forme personnalisée dans la console" lightbox="../media/console-log-custom.msft.png":::
       <span data-ttu-id="f32b8-174">Message avec mise en forme personnalisée dans la **console**</span><span class="sxs-lookup"><span data-stu-id="f32b8-174">A message with custom formatting in the **Console**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="f32b8-175">L’idée principale ici est que lorsque vous souhaitez enregistrer des messages dans la console à partir de votre JavaScript, vous utilisez l’une `console` des méthodes.</span><span class="sxs-lookup"><span data-stu-id="f32b8-175">The main idea here is that when you want to log messages to the Console from your JavaScript, you use one of the `console` methods.</span></span>  <span data-ttu-id="f32b8-176">Chaque méthode formate les messages différemment.</span><span class="sxs-lookup"><span data-stu-id="f32b8-176">Each method formats messages differently.</span></span>  

<span data-ttu-id="f32b8-177">Il existe encore plus de méthodes que celles qui ont été démontrées dans cette section.</span><span class="sxs-lookup"><span data-stu-id="f32b8-177">There are even more methods than what has been demonstrated in this section.</span></span>  <span data-ttu-id="f32b8-178">Ce didacticiel vous montre comment explorer le reste des méthodes.</span><span class="sxs-lookup"><span data-stu-id="f32b8-178">This tutorial shows you how to explore the rest of the methods.</span></span>  

## <a name="view-messages-logged-by-the-browser"></a><span data-ttu-id="f32b8-179">Afficher les messages enregistrés par le navigateur</span><span class="sxs-lookup"><span data-stu-id="f32b8-179">View messages logged by the browser</span></span>  

<span data-ttu-id="f32b8-180">Le navigateur enregistre également les messages dans la console.</span><span class="sxs-lookup"><span data-stu-id="f32b8-180">The browser logs messages to the Console, too.</span></span>  <span data-ttu-id="f32b8-181">Cela se produit généralement en cas de problème avec la page.</span><span class="sxs-lookup"><span data-stu-id="f32b8-181">This usually happens when there is a problem with the page.</span></span>  

1.  <span data-ttu-id="f32b8-182">Choose **Cause 404**.</span><span class="sxs-lookup"><span data-stu-id="f32b8-182">Choose **Cause 404**.</span></span>  <span data-ttu-id="f32b8-183">Le navigateur enregistre un code d’état HTTP d’erreur réseau, car le code JavaScript de la page a tenté d’extraire un fichier qui `404` n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="f32b8-183">The browser logs an HTTP status code of `404` network error because the JavaScript of the page tried to fetch a file that does not exist.</span></span>  
    
    :::image type="complex" source="../media/console-cause-404.msft.png" alt-text="Une erreur 404 dans la console" lightbox="../media/console-cause-404.msft.png":::
       <span data-ttu-id="f32b8-185">Une `404` erreur dans la **console**</span><span class="sxs-lookup"><span data-stu-id="f32b8-185">A `404` error in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f32b8-186">Choose **Cause Error**.</span><span class="sxs-lookup"><span data-stu-id="f32b8-186">Choose **Cause Error**.</span></span>  <span data-ttu-id="f32b8-187">Le navigateur enregistre un non-journal, car javaScript tente de mettre à jour un nœud DOM qui `TypeError` n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="f32b8-187">The browser logs an uncaught `TypeError` because the JavaScript is trying to update a DOM node that does not exist.</span></span>  
    
    :::image type="complex" source="../media/console-cause-error.msft.png" alt-text="Un TypeError dans la console" lightbox="../media/console-cause-error.msft.png":::
       <span data-ttu-id="f32b8-189">A `TypeError` dans la **console**</span><span class="sxs-lookup"><span data-stu-id="f32b8-189">A `TypeError` in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f32b8-190">Sélectionnez **la dropdown Log Levels** (Niveaux du journal) et activez l’option **Verbose** si elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="f32b8-190">Choose the **Log Levels** dropdown and enable the **Verbose** option if it is disabled.</span></span>  <span data-ttu-id="f32b8-191">Pour en savoir plus sur le filtrage, voir la section suivante.</span><span class="sxs-lookup"><span data-stu-id="f32b8-191">You learn more about filtering in the next section.</span></span>  <span data-ttu-id="f32b8-192">Vous devez effectuer cette étape pour vous assurer que le message suivant que vous enregistrez est visible.</span><span class="sxs-lookup"><span data-stu-id="f32b8-192">You need to do this to make sure that the next message you log is visible.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f32b8-193">Si la barre des niveaux par défaut est désactivée, vous devrez peut-être fermer la **barre** latérale de la console.</span><span class="sxs-lookup"><span data-stu-id="f32b8-193">If the Default Levels dropdown is disabled, you may need to close the **Console** Sidebar.</span></span>  <span data-ttu-id="f32b8-194">Filtrez par source de message ci-dessous pour plus d’informations sur la **barre** latérale de la console.</span><span class="sxs-lookup"><span data-stu-id="f32b8-194">Filter by Message Source below for more information about the **Console** Sidebar.</span></span>
    
    :::image type="complex" source="../media/console-cause-error-log-levels.msft.png" alt-text="Activation du niveau de journal détaillé" lightbox="../media/console-cause-error-log-levels.msft.png":::
       <span data-ttu-id="f32b8-196">Activation du niveau de journal détaillé</span><span class="sxs-lookup"><span data-stu-id="f32b8-196">Enabling the Verbose log level</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f32b8-197">Choose **Cause Violation**.</span><span class="sxs-lookup"><span data-stu-id="f32b8-197">Choose **Cause Violation**.</span></span>  <span data-ttu-id="f32b8-198">La page ne répond plus pendant quelques secondes, puis le navigateur enregistre le message `[Violation] 'click' handler took 3000ms` dans la console.</span><span class="sxs-lookup"><span data-stu-id="f32b8-198">The page becomes unresponsive for a few seconds and then the browser logs the message `[Violation] 'click' handler took 3000ms` to the Console.</span></span>  <span data-ttu-id="f32b8-199">La durée exacte peut varier.</span><span class="sxs-lookup"><span data-stu-id="f32b8-199">The exact duration may vary.</span></span>  
    
    :::image type="complex" source="../media/console-cause-violation.msft.png" alt-text="Violation dans la console" lightbox="../media/console-cause-violation.msft.png":::
       <span data-ttu-id="f32b8-201">Violation dans la **console**</span><span class="sxs-lookup"><span data-stu-id="f32b8-201">A violation in the **Console**</span></span>  
    :::image-end:::  
    
## <a name="filter-messages"></a><span data-ttu-id="f32b8-202">Filtrer les messages</span><span class="sxs-lookup"><span data-stu-id="f32b8-202">Filter messages</span></span>  

<span data-ttu-id="f32b8-203">Sur certaines pages web, vous examinez la **console** et vous recevez des messages.</span><span class="sxs-lookup"><span data-stu-id="f32b8-203">On some webpages you review the **Console** get flooded with messages.</span></span>  <span data-ttu-id="f32b8-204">DevTools offre de nombreuses façons différentes de filtrer les messages qui ne sont pas pertinents pour la tâche en cours.</span><span class="sxs-lookup"><span data-stu-id="f32b8-204">DevTools provides many different ways to filter out messages that are not relevant to the task at hand.</span></span>  

### <a name="filter-by-log-level"></a><span data-ttu-id="f32b8-205">Filtrer par niveau de journal</span><span class="sxs-lookup"><span data-stu-id="f32b8-205">Filter by log level</span></span>  

<span data-ttu-id="f32b8-206">Chaque `console` méthode se voit attribuer un niveau de gravité : , , ou `Verbose` `Info` `Warning` `Error` .</span><span class="sxs-lookup"><span data-stu-id="f32b8-206">Each `console` method is assigned a severity level: `Verbose`, `Info`, `Warning`, or `Error`.</span></span>  <span data-ttu-id="f32b8-207">Par exemple, `console.log()` il s’agit `Info` d’un message de niveau -level, tandis `console.error()` qu’il s’agit d’un `Error` message de niveau -.</span><span class="sxs-lookup"><span data-stu-id="f32b8-207">For example, `console.log()` is an `Info`-level message, whereas `console.error()` is an `Error`-level message.</span></span>  

1.  <span data-ttu-id="f32b8-208">Choose the **Log Levels** dropdown and disable **Errors**.</span><span class="sxs-lookup"><span data-stu-id="f32b8-208">Choose the **Log Levels** dropdown and disable **Errors**.</span></span>  <span data-ttu-id="f32b8-209">Un niveau est désactivé lorsqu’il n’y a plus de coche en regard.</span><span class="sxs-lookup"><span data-stu-id="f32b8-209">A level is disabled when there is no longer a checkmark next to it.</span></span>  <span data-ttu-id="f32b8-210">Les `Error` messages de niveau -disparaissent.</span><span class="sxs-lookup"><span data-stu-id="f32b8-210">The `Error`-level messages disappear.</span></span>  
    
    :::image type="complex" source="../media/console-cause-violation-log-levels.msft.png" alt-text="Désactiver les messages de niveau erreur dans la console" lightbox="../media/console-cause-violation-log-levels.msft.png":::
       <span data-ttu-id="f32b8-212">Désactiver les messages de niveau erreur dans la **console**</span><span class="sxs-lookup"><span data-stu-id="f32b8-212">Disable Error-level messages in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f32b8-213">Sélectionnez de nouveau la dropdown **Log Levels** (Niveaux de journal) et ré-activez Errors **(Erreurs).**</span><span class="sxs-lookup"><span data-stu-id="f32b8-213">Choose the **Log Levels** dropdown again and re-enable **Errors**.</span></span>  <span data-ttu-id="f32b8-214">Les `Error` messages de niveau réapparaissent.</span><span class="sxs-lookup"><span data-stu-id="f32b8-214">The `Error`-level messages reappear.</span></span>  

### <a name="filter-by-text"></a><span data-ttu-id="f32b8-215">Filtrer par texte</span><span class="sxs-lookup"><span data-stu-id="f32b8-215">Filter by text</span></span>  

<span data-ttu-id="f32b8-216">Lorsque vous souhaitez afficher uniquement les messages qui incluent une chaîne exacte, tapez cette chaîne dans la **zone de** texte Filtrer.</span><span class="sxs-lookup"><span data-stu-id="f32b8-216">When you want to only view messages that include an exact string, type that string into the **Filter** text box.</span></span>  

1.  <span data-ttu-id="f32b8-217">Tapez `Dave` dans la zone **de** texte Filtrer.</span><span class="sxs-lookup"><span data-stu-id="f32b8-217">Type `Dave` into the **Filter** text box.</span></span>  <span data-ttu-id="f32b8-218">Tous les messages qui n’incluent pas la `Dave` chaîne sont masqués.</span><span class="sxs-lookup"><span data-stu-id="f32b8-218">All messages that do not include the string `Dave` are hidden.</span></span>  <span data-ttu-id="f32b8-219">Vous pouvez également passer en revue `Adolescent Irradiated Espionage Tortoises` l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="f32b8-219">You may also review the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  <span data-ttu-id="f32b8-220">Il s’agit d’un bogue.</span><span class="sxs-lookup"><span data-stu-id="f32b8-220">That is a bug.</span></span>  
    
    :::image type="complex" source="../media/console-all-messages-text-filter.msft.png" alt-text="Filtrer les messages qui n’incluent pas Dave" lightbox="../media/console-all-messages-text-filter.msft.png":::
       <span data-ttu-id="f32b8-222">Filtrer les messages qui n’incluent pas</span><span class="sxs-lookup"><span data-stu-id="f32b8-222">Filter out any message that does not include</span></span> `Dave`  
    :::image-end:::  
    
1.  <span data-ttu-id="f32b8-223">Supprimer `Dave` de la zone **de** texte Filtrer.</span><span class="sxs-lookup"><span data-stu-id="f32b8-223">Delete `Dave` from the **Filter** text box.</span></span>  <span data-ttu-id="f32b8-224">Tous les messages réapparaissent.</span><span class="sxs-lookup"><span data-stu-id="f32b8-224">All the messages reappear.</span></span>  

### <a name="filter-by-regular-expression"></a><span data-ttu-id="f32b8-225">Filtrer par expression régulière</span><span class="sxs-lookup"><span data-stu-id="f32b8-225">Filter by regular expression</span></span>  

<span data-ttu-id="f32b8-226">Lorsque vous souhaitez afficher tous les messages qui incluent un modèle de texte, plutôt qu’une chaîne spécifique, utilisez une [expression régulière][MDNRegularExpressions].</span><span class="sxs-lookup"><span data-stu-id="f32b8-226">When you want to show all messages that include a pattern of text, rather than a specific string, use a [regular expression][MDNRegularExpressions].</span></span>  

1.  <span data-ttu-id="f32b8-227">Tapez `/^[AH]/` dans la zone **de** texte Filtrer.</span><span class="sxs-lookup"><span data-stu-id="f32b8-227">Type `/^[AH]/` into the **Filter** text box.</span></span>  <span data-ttu-id="f32b8-228">Tapez le modèle [dans RegExr][|::ref1::|Main] pour obtenir une explication de ce qu’il fait.</span><span class="sxs-lookup"><span data-stu-id="f32b8-228">Type the pattern into [RegExr][|::ref1::|Main] for an explanation of what it is doing.</span></span>  
    
    :::image type="complex" source="../media/console-all-messages-regex-filter.msft.png" alt-text="Filtrage de tous les messages qui ne correspondent pas à un modèle" lightbox="../media/console-all-messages-regex-filter.msft.png":::
       <span data-ttu-id="f32b8-230">Filtrage de tous les messages qui ne correspondent pas au modèle</span><span class="sxs-lookup"><span data-stu-id="f32b8-230">Filtering out any message that does not match the pattern</span></span> `/^[AH]/`  
    :::image-end:::  
    
1.  <span data-ttu-id="f32b8-231">Supprimer `/^[AH]/` de la zone **de** texte Filtrer.</span><span class="sxs-lookup"><span data-stu-id="f32b8-231">Delete `/^[AH]/` from the **Filter** text box.</span></span>  <span data-ttu-id="f32b8-232">Tous les messages sont de nouveau visibles.</span><span class="sxs-lookup"><span data-stu-id="f32b8-232">All messages are visible again.</span></span>  

### <a name="filter-by-message-source"></a><span data-ttu-id="f32b8-233">Filtrer par source de message</span><span class="sxs-lookup"><span data-stu-id="f32b8-233">Filter by message source</span></span>  

<span data-ttu-id="f32b8-234">Lorsque vous souhaitez afficher uniquement les messages provenant d’une URL spécifique, utilisez la **barre latérale**.</span><span class="sxs-lookup"><span data-stu-id="f32b8-234">When you want to only view the messages that came from a certain URL, use the **Sidebar**.</span></span>  

1.  <span data-ttu-id="f32b8-235">Choose **Show Console Sidebar** \( ![ Show Console Sidebar ](../media/show-console-sidebar-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="f32b8-235">Choose **Show Console Sidebar** \(![Show Console Sidebar](../media/show-console-sidebar-icon.msft.png)\).</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-all-messages.msft.png" alt-text="Barre latérale" lightbox="../media/console-sidebar-all-messages.msft.png":::
       <span data-ttu-id="f32b8-237">Barre latérale</span><span class="sxs-lookup"><span data-stu-id="f32b8-237">The Sidebar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f32b8-238">Sélectionnez **l’icône** Développer \( ![ Développer ](../media/expand-icon.msft.png) \) en de côté du nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="f32b8-238">Choose the **Expand** \(![Expand](../media/expand-icon.msft.png)\) icon next to the number of messages.</span></span>  <span data-ttu-id="f32b8-239">Dans la figure suivante, le nombre de messages est indiqué en tant que **13 Messages**.</span><span class="sxs-lookup"><span data-stu-id="f32b8-239">In the following figure, the number of messages is indicated as **13 Messages**.</span></span>  <span data-ttu-id="f32b8-240">La **barre latérale affiche** la liste des URL à l’origine de la journalologie des messages.</span><span class="sxs-lookup"><span data-stu-id="f32b8-240">The **Sidebar** shows a list of URLs that caused messages to be logged.</span></span>  <span data-ttu-id="f32b8-241">Par exemple, `log.js` 11 messages ont été envoyés.</span><span class="sxs-lookup"><span data-stu-id="f32b8-241">For example, `log.js` caused 11 messages.</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-expanded-all-messages.msft.png" alt-text="Affichage de la source des messages dans la barre latérale" lightbox="../media/console-sidebar-expanded-all-messages.msft.png":::
       <span data-ttu-id="f32b8-243">Affichage de la source des messages dans la barre latérale</span><span class="sxs-lookup"><span data-stu-id="f32b8-243">Viewing the source of messages in the Sidebar</span></span>  
    :::image-end:::  
    
### <a name="filter-by-user-messages"></a><span data-ttu-id="f32b8-244">Filtrer par messages utilisateur</span><span class="sxs-lookup"><span data-stu-id="f32b8-244">Filter by user messages</span></span>  

<span data-ttu-id="f32b8-245">Précédemment, lorsque vous choisissez **Log Info**, un script nommé pour enregistrer le message sur `console.log('Hello, Console!')` la console.</span><span class="sxs-lookup"><span data-stu-id="f32b8-245">Earlier, when you choose **Log Info**, a script named `console.log('Hello, Console!')` in order to log the message to the Console.</span></span>  <span data-ttu-id="f32b8-246">Les messages enregistrés à partir de JavaScript comme celui-ci sont nommés **messages d’utilisateur.**</span><span class="sxs-lookup"><span data-stu-id="f32b8-246">Messages logged from JavaScript like this are named **user messages**.</span></span>  <span data-ttu-id="f32b8-247">En revanche, lorsque vous choisissez **Cause 404,** le navigateur enregistre un message de niveau -indiquant que la ressource demandée `Error` est in trouvée.</span><span class="sxs-lookup"><span data-stu-id="f32b8-247">In contrast, when you choose **Cause 404**, the browser logs an `Error`-level message stating that the requested resource is not found.</span></span>  <span data-ttu-id="f32b8-248">Les messages de ce genre sont considérés comme **des messages de navigateur.**</span><span class="sxs-lookup"><span data-stu-id="f32b8-248">Messages like that are considered **browser messages**.</span></span>  <span data-ttu-id="f32b8-249">Utilisez la **barre latérale pour** filtrer les messages du navigateur et afficher uniquement les messages de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f32b8-249">Use the **Sidebar** to filter out browser messages and only show user messages.</span></span>  

1.  <span data-ttu-id="f32b8-250">Choose **9 User Messages**.</span><span class="sxs-lookup"><span data-stu-id="f32b8-250">Choose **9 User Messages**.</span></span>  <span data-ttu-id="f32b8-251">Les messages du navigateur sont masqués.</span><span class="sxs-lookup"><span data-stu-id="f32b8-251">The browser messages are hidden.</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-user-messages.msft.png" alt-text="Filtrage des messages du navigateur" lightbox="../media/console-sidebar-user-messages.msft.png":::
       <span data-ttu-id="f32b8-253">Filtrage des messages du navigateur</span><span class="sxs-lookup"><span data-stu-id="f32b8-253">Filtering out browser messages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f32b8-254">Choisissez **13 messages** pour afficher à nouveau tous les messages.</span><span class="sxs-lookup"><span data-stu-id="f32b8-254">Choose **13 Messages** to show all messages again.</span></span>  

## <a name="use-the-console-alongside-any-other-tools"></a><span data-ttu-id="f32b8-255">Utiliser la console avec tous les autres outils</span><span class="sxs-lookup"><span data-stu-id="f32b8-255">Use the Console alongside any other tools</span></span>  

<span data-ttu-id="f32b8-256">Si vous modifiez des styles, mais que vous devez rapidement vérifier le journal de la console, utilisez le caisse.</span><span class="sxs-lookup"><span data-stu-id="f32b8-256">If you are editing styles, but you need to quickly check the Console log for something, Use the Drawer.</span></span>  

1.  <span data-ttu-id="f32b8-257">Choisissez **l’outil Éléments.**</span><span class="sxs-lookup"><span data-stu-id="f32b8-257">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="f32b8-258">Sélectionnez `Escape` .</span><span class="sxs-lookup"><span data-stu-id="f32b8-258">Select `Escape`.</span></span>  <span data-ttu-id="f32b8-259">**L’outil Console** dans **le caisse s’ouvre.**</span><span class="sxs-lookup"><span data-stu-id="f32b8-259">The **Console** tool in the **Drawer** opens.</span></span>  <span data-ttu-id="f32b8-260">Il comporte toutes les fonctionnalités du panneau Console que vous utilisez tout au long de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="f32b8-260">It has all of the features of the Console panel that you have been using throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/console-elements-drawer-console-sidebar-all-messages.msft.png" alt-text="Outil Console dans le caisse" lightbox="../media/console-elements-drawer-console-sidebar-all-messages.msft.png":::
         <span data-ttu-id="f32b8-262">Outil **Console** dans le **caisse**</span><span class="sxs-lookup"><span data-stu-id="f32b8-262">The **Console** tool in the **Drawer**</span></span>  
    :::image-end:::  
    
## <a name="see-also"></a><span data-ttu-id="f32b8-263">Voir également</span><span class="sxs-lookup"><span data-stu-id="f32b8-263">See also</span></span>  

*   <span data-ttu-id="f32b8-264">Pour explorer d’autres fonctionnalités et flux de travail liés à l’interface utilisateur de la **console,** accédez à [Référence de console.][DevToolsConsoleApi]</span><span class="sxs-lookup"><span data-stu-id="f32b8-264">To explore more features and workflows related to the **Console** UI,navigate to [Console Reference][DevToolsConsoleApi].</span></span>  
*   <span data-ttu-id="f32b8-265">Pour en savoir plus sur toutes les méthodes démontrées dans Afficher les messages enregistrés à partir de JavaScript et explorer les autres méthodes non couvertes dans cet article, accédez à référence de `console` [](#view-messages-logged-from-javascript) `console` l’API console. [][DevToolsConsoleReference]</span><span class="sxs-lookup"><span data-stu-id="f32b8-265">To learn more about all of the `console` methods demonstrated in [View messages logged from JavaScript](#view-messages-logged-from-javascript) and explore the other `console` methods not covered in this article, navigate to [Console API Reference][DevToolsConsoleReference].</span></span>  
<!--*   Navigate to [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  
     
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="f32b8-266">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="f32b8-266">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge \(Chromium\) | Documents Microsoft"  
[DevToolsCommandMenu]: ../command-menu/index.md "Exécuter des commandes avec le menu DevTools Command de Microsoft Edge | Documents Microsoft"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Modifier le placement de Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsConsoleApi]: ./api.md "Référence de l’API de console | Documents Microsoft"  
[DevToolsConsoleReference]: ./reference.md "Référence de la console | Documents Microsoft"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Mise en place de la journalisation des messages | Glitch"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Expressions régulières | MDN"  

[RegExrMain]: https://regexr.com "RegExr"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Trace de pile : Wikipedia"  
> [!NOTE]
> <span data-ttu-id="f32b8-276">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f32b8-276">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f32b8-277">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/log) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="f32b8-277">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/log) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="f32b8-279">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f32b8-279">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
