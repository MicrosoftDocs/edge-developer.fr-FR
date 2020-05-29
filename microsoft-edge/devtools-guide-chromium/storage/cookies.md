---
title: Afficher, modifier et supprimer des cookies avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 084c4116cd4c9c5e70b2fe341257fa68ba2c8ae7
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612067"
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





# <span data-ttu-id="de2aa-103">Afficher, modifier et supprimer des cookies avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="de2aa-103">View, Edit, And Delete Cookies With Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="de2aa-104">[Les cookies http][MDNHTTPCookies] sont principalement utilisés pour gérer les sessions utilisateur, stocker les préférences utilisateur de personnalisation et suivre le comportement des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="de2aa-104">[HTTP Cookies][MDNHTTPCookies] are mainly used to manage user sessions, store user personalization preferences, and track user behavior.</span></span>  <span data-ttu-id="de2aa-105">C’est aussi la cause de tous ces types de consentement «cette page utilise des cookies» que vous voyez sur le Web.</span><span class="sxs-lookup"><span data-stu-id="de2aa-105">They are also the cause of all of those annoying "this page uses cookies" consent forms that you see across the web.</span></span>  <span data-ttu-id="de2aa-106">Ce guide vous explique comment afficher, modifier et supprimer les cookies HTTP pour une page avec [Microsoft Edge devtools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="de2aa-106">This guide teaches you how to view, edit, and delete the HTTP cookies for a page with [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="de2aa-107">Ouvrir le volet cookies</span><span class="sxs-lookup"><span data-stu-id="de2aa-107">Open the Cookies pane</span></span>   

1.  <span data-ttu-id="de2aa-108">[Ouvrez devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="de2aa-108">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="de2aa-109">Sélectionnez l’onglet **application** pour ouvrir le volet de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="de2aa-109">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="de2aa-110">Le volet **manifeste** doit être ouvert.</span><span class="sxs-lookup"><span data-stu-id="de2aa-110">The **Manifest** pane should open.</span></span>  
    
    > ##### <span data-ttu-id="de2aa-111">Figure1</span><span class="sxs-lookup"><span data-stu-id="de2aa-111">Figure 1</span></span>  
    > <span data-ttu-id="de2aa-112">Volet manifeste</span><span class="sxs-lookup"><span data-stu-id="de2aa-112">The Manifest pane</span></span>  
    > ![Volet manifeste][ImageManifest]  

1.  <span data-ttu-id="de2aa-114">Sous **stockage** , développez **cookies**, puis sélectionnez une origine.</span><span class="sxs-lookup"><span data-stu-id="de2aa-114">Under **Storage** expand **Cookies**, then select an origin.</span></span>  
    
    > ##### <span data-ttu-id="de2aa-115">Figure 2</span><span class="sxs-lookup"><span data-stu-id="de2aa-115">Figure 2</span></span>  
    > <span data-ttu-id="de2aa-116">Volet cookies</span><span class="sxs-lookup"><span data-stu-id="de2aa-116">The Cookies pane</span></span>  
    > ![Volet cookies][ImageCookies]  

## <span data-ttu-id="de2aa-118">Champs</span><span class="sxs-lookup"><span data-stu-id="de2aa-118">Fields</span></span>   

<span data-ttu-id="de2aa-119">La table **cookies** contient les champs suivants:</span><span class="sxs-lookup"><span data-stu-id="de2aa-119">The **Cookies** table contains the following fields:</span></span>  

*   <span data-ttu-id="de2aa-120">**Nom**.</span><span class="sxs-lookup"><span data-stu-id="de2aa-120">**Name**.</span></span>  <span data-ttu-id="de2aa-121">Nom du cookie.</span><span class="sxs-lookup"><span data-stu-id="de2aa-121">The name of the cookie.</span></span>  
*   <span data-ttu-id="de2aa-122">**Valeur**.</span><span class="sxs-lookup"><span data-stu-id="de2aa-122">**Value**.</span></span>  <span data-ttu-id="de2aa-123">Valeur du cookie.</span><span class="sxs-lookup"><span data-stu-id="de2aa-123">The value of the cookie.</span></span>  
*   <span data-ttu-id="de2aa-124">**Domain (domaine**).</span><span class="sxs-lookup"><span data-stu-id="de2aa-124">**Domain**.</span></span>  <span data-ttu-id="de2aa-125">Les hôtes autorisés à recevoir le cookie.</span><span class="sxs-lookup"><span data-stu-id="de2aa-125">The hosts that are allowed to receive the cookie.</span></span>  <span data-ttu-id="de2aa-126">Voir [étendue des cookies][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="de2aa-126">See [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="de2aa-127">**Path**.</span><span class="sxs-lookup"><span data-stu-id="de2aa-127">**Path**.</span></span>  <span data-ttu-id="de2aa-128">URL qui doit exister dans l’URL requise pour envoyer l' `Cookie` en-tête.</span><span class="sxs-lookup"><span data-stu-id="de2aa-128">The URL that must exist in the requested URL in order to send the `Cookie` header.</span></span>  <span data-ttu-id="de2aa-129">Voir [étendue des cookies][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="de2aa-129">See [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="de2aa-130">**Expire/max-age**.</span><span class="sxs-lookup"><span data-stu-id="de2aa-130">**Expires / Max-Age**.</span></span>  <span data-ttu-id="de2aa-131">Date d’expiration ou âge maximum du cookie.</span><span class="sxs-lookup"><span data-stu-id="de2aa-131">The expiration date or maximum age of the cookie.</span></span>  <span data-ttu-id="de2aa-132">Voir [cookies permanents][MDNHTTPCookiesPermanent].</span><span class="sxs-lookup"><span data-stu-id="de2aa-132">See [Permanent cookies][MDNHTTPCookiesPermanent].</span></span>  <span data-ttu-id="de2aa-133">Pour [les cookies de session][MDNHTTPCookiesSession] , cette valeur est toujours `Session` .</span><span class="sxs-lookup"><span data-stu-id="de2aa-133">For [session cookies][MDNHTTPCookiesSession] this value is always `Session`.</span></span>  
*   <span data-ttu-id="de2aa-134">**Taille**.</span><span class="sxs-lookup"><span data-stu-id="de2aa-134">**Size**.</span></span>  <span data-ttu-id="de2aa-135">Taille en octets du cookie.</span><span class="sxs-lookup"><span data-stu-id="de2aa-135">The size, in bytes, of the cookie.</span></span>  
*   <span data-ttu-id="de2aa-136">**Http**.</span><span class="sxs-lookup"><span data-stu-id="de2aa-136">**HTTP**.</span></span>  <span data-ttu-id="de2aa-137">Si la valeur est true, ce champ indique que le cookie doit uniquement être utilisé sur une modification HTTP et JavaScript n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="de2aa-137">If true, this field indicates that the cookie should only be used over HTTP and JavaScript modification is not allowed.</span></span>  <span data-ttu-id="de2aa-138">Voir [cookies HttpOnly][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="de2aa-138">See [HttpOnly cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="de2aa-139">**Sécurisé**.</span><span class="sxs-lookup"><span data-stu-id="de2aa-139">**Secure**.</span></span>  <span data-ttu-id="de2aa-140">Si la valeur est true, ce champ indique que le cookie doit être envoyé au serveur uniquement via une connexion sécurisée HTTPs.</span><span class="sxs-lookup"><span data-stu-id="de2aa-140">If true, this field indicates that the cookie must be sent to the server only over a secure, HTTPS connection.</span></span>  <span data-ttu-id="de2aa-141">Voir [cookies sécurisés][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="de2aa-141">See [Secure cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="de2aa-142">**SameSite**.</span><span class="sxs-lookup"><span data-stu-id="de2aa-142">**SameSite**.</span></span>  <span data-ttu-id="de2aa-143">Contient `strict` ou `lax` si le cookie utilise l’attribut [Samesite][MDNHTTPCookiesSamesite] expérimental.</span><span class="sxs-lookup"><span data-stu-id="de2aa-143">Contains `strict` or `lax` if the cookie is using the experimental [Samesite][MDNHTTPCookiesSamesite] attribute.</span></span>  

## <span data-ttu-id="de2aa-144">Filtrer les cookies</span><span class="sxs-lookup"><span data-stu-id="de2aa-144">Filter cookies</span></span>   

<span data-ttu-id="de2aa-145">Utilisez la zone de texte **filtre** pour filtrer les cookies par **nom** ou par **valeur**.</span><span class="sxs-lookup"><span data-stu-id="de2aa-145">Use the **Filter** text box to filter cookies by **Name** or **Value**.</span></span>  <span data-ttu-id="de2aa-146">Le filtrage par d’autres champs n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="de2aa-146">Filtering by other fields is not supported.</span></span>  

> ##### <span data-ttu-id="de2aa-147">Figure3</span><span class="sxs-lookup"><span data-stu-id="de2aa-147">Figure 3</span></span>  
> <span data-ttu-id="de2aa-148">Filtrage de tout cookie qui ne contient pas le texte</span><span class="sxs-lookup"><span data-stu-id="de2aa-148">Filtering out any cookies that do not contain the text</span></span> `ID`  
> ![Filtrage de tout cookie qui ne contient pas l’ID de texte][ImageCookiesFilter]  

## <span data-ttu-id="de2aa-150">Modifier un cookie</span><span class="sxs-lookup"><span data-stu-id="de2aa-150">Edit a cookie</span></span>   

<span data-ttu-id="de2aa-151">Les champs **nom**, **valeur**, **domaine**, **chemin d’accès**et **durée d’expiration/maximum** doivent être modifiables.</span><span class="sxs-lookup"><span data-stu-id="de2aa-151">The **Name**, **Value**, **Domain**, **Path**, and **Expires / Max-Age** fields are editable.</span></span>  
<span data-ttu-id="de2aa-152">Double-cliquez sur un champ pour le modifier.</span><span class="sxs-lookup"><span data-stu-id="de2aa-152">Double-click a field to edit it.</span></span>  

> ##### <span data-ttu-id="de2aa-153">Figure 4</span><span class="sxs-lookup"><span data-stu-id="de2aa-153">Figure 4</span></span>  
> <span data-ttu-id="de2aa-154">Définir le nom d’un cookie sur</span><span class="sxs-lookup"><span data-stu-id="de2aa-154">Setting the name of a cookie to</span></span> `DEVTOOLS!`  
> ![Définir le nom d’un cookie sur DEVTOOLS!][ImageEditCookie]  

## <span data-ttu-id="de2aa-156">Supprimer les cookies</span><span class="sxs-lookup"><span data-stu-id="de2aa-156">Delete cookies</span></span>   

<span data-ttu-id="de2aa-157">Sélectionnez un cookie, puis cliquez sur **supprimer** ![ l’option supprimer sélectionnée ][ImageDeleteIcon] pour supprimer ce cookie.</span><span class="sxs-lookup"><span data-stu-id="de2aa-157">Select a cookie and then click **Delete Selected** ![Delete Selected][ImageDeleteIcon]  to delete that one cookie.</span></span>  

> ##### <span data-ttu-id="de2aa-158">Figure 5</span><span class="sxs-lookup"><span data-stu-id="de2aa-158">Figure 5</span></span>  
> <span data-ttu-id="de2aa-159">Suppression d’un cookie spécifique</span><span class="sxs-lookup"><span data-stu-id="de2aa-159">Deleting a specific cookie</span></span>  
> ![Suppression d’un cookie spécifique][ImageDeleteCookie]  

<span data-ttu-id="de2aa-161">Pour supprimer tous les cookies, sélectionnez **Effacer tout** ![ Effacer tout ][ImageClearIcon] .</span><span class="sxs-lookup"><span data-stu-id="de2aa-161">Select **Clear All** ![Clear All][ImageClearIcon]  to delete all cookies.</span></span>  

> ##### <span data-ttu-id="de2aa-162">Figure 6</span><span class="sxs-lookup"><span data-stu-id="de2aa-162">Figure 6</span></span>  
> <span data-ttu-id="de2aa-163">Effacement de tous les cookies</span><span class="sxs-lookup"><span data-stu-id="de2aa-163">Clearing all cookies</span></span>  
> ![Effacement de tous les cookies][ImageClearAllCookies]  

<!--    -->  

  

<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest-empty.msft.png "Figure 1: volet manifeste"  
[ImageCookies]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-cookies-selected.msft.png "Figure 2: volet cookies"  
[ImageCookiesFilter]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-cookies-filter-id.msft.png "Figure 3: filtrage de tout cookie qui ne contient pas l’ID de texte"  
[ImageEditCookie]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-cookies-rename.msft.png "Figure 4: définition du nom d’un cookie sur DEVTOOLS!"  
[ImageDeleteCookie]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-cookies-delete-selected.msft.png "Figure 5: suppression d’un cookie spécifique"  
[ImageClearAllCookies]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-cookies-clear-all.msft.png "Figure 6: suppression de tous les cookies"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome)"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Ouvrir Microsoft Edge DevTools"  

[MDNHTTPCookies]: https://developer.mozilla.org/docs/Web/HTTP/Cookies "Cookies HTTP | MDN"  
[MDNHTTPCookiesPermanent]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Permanent_cookies "Cookies HTTP-cookies permanents | MDN"  
[MDNHTTPCookiesSamesite]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#SameSite_cookies "Cookies HTTP-cookies SameSite | MDN"  
[MDNHTTPCookiesScope]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Scope_of_cookies "Cookies HTTP-étendue des cookies | MDN"  
[MDNHTTPCookiesSecure]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Secure_and_HttpOnly_cookies "Cookies HTTP-cookies sécurisés et HttpOnly | MDN"  
[MDNHTTPCookiesSession]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Session_cookies "Cookies HTTP-cookies de session | MDN"  

> [!NOTE]
> <span data-ttu-id="de2aa-179">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="de2aa-179">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="de2aa-180">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="de2aa-180">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="de2aa-182">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="de2aa-182">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
