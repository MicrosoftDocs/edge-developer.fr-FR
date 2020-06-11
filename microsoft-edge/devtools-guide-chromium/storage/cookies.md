---
title: Afficher, modifier et supprimer des cookies avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 4bfd99a36a6a3f8fdf8dbd7787bd54cde87d79da
ms.sourcegitcommit: f010f43604bd4363af6827f79dbc071b9afcb667
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2020
ms.locfileid: "10708930"
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

# <span data-ttu-id="4820a-103">Afficher, modifier et supprimer des cookies avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4820a-103">View, edit, and delete cookies with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="4820a-104">[Les cookies http][MDNHTTPCookies] sont principalement utilisés pour gérer les sessions utilisateur, stocker les préférences utilisateur de personnalisation et suivre le comportement des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="4820a-104">[HTTP Cookies][MDNHTTPCookies] are mainly used to manage user sessions, store user personalization preferences, and track user behavior.</span></span>  <span data-ttu-id="4820a-105">Les cookies sont également à l’origine de tous les types de consentement «cette page utilise des cookies» que vous voyez sur le Web.</span><span class="sxs-lookup"><span data-stu-id="4820a-105">Cookies are also the cause of all of the annoying "this page uses cookies" consent forms that you see across the web.</span></span>  <span data-ttu-id="4820a-106">Le guide suivant vous explique comment afficher, modifier et supprimer les cookies HTTP pour une page avec [Microsoft Edge devtools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="4820a-106">The following guide teaches you how to view, edit, and delete the HTTP cookies for a page with [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="4820a-107">Ouvrir le volet cookies</span><span class="sxs-lookup"><span data-stu-id="4820a-107">Open the Cookies pane</span></span>  

1.  <span data-ttu-id="4820a-108">[Ouvrez devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="4820a-108">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="4820a-109">Sélectionnez l’onglet **application** pour ouvrir le volet de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="4820a-109">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="4820a-110">Le volet **manifeste** doit être ouvert.</span><span class="sxs-lookup"><span data-stu-id="4820a-110">The **Manifest** pane should open.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest-empty.msft.png":::
       <span data-ttu-id="4820a-112">Figure 1: volet manifeste</span><span class="sxs-lookup"><span data-stu-id="4820a-112">Figure 1:  The Manifest pane</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="4820a-113">Sous **stockage** , développez **cookies**, puis sélectionnez une origine.</span><span class="sxs-lookup"><span data-stu-id="4820a-113">Under **Storage** expand **Cookies**, then select an origin.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-cookies-selected.msft.png" alt-text="Volet cookies" lightbox="../media/storage-application-storage-cookies-selected.msft.png":::
       <span data-ttu-id="4820a-115">Figure 2: volet cookies</span><span class="sxs-lookup"><span data-stu-id="4820a-115">Figure 2:  The Cookies pane</span></span>  
    :::image-end:::  

## <span data-ttu-id="4820a-116">Champs</span><span class="sxs-lookup"><span data-stu-id="4820a-116">Fields</span></span>  

<span data-ttu-id="4820a-117">La table **cookies** contient les champs suivants.</span><span class="sxs-lookup"><span data-stu-id="4820a-117">The **Cookies** table contains the following fields.</span></span>  

*   <span data-ttu-id="4820a-118">**Nom**.</span><span class="sxs-lookup"><span data-stu-id="4820a-118">**Name**.</span></span>  <span data-ttu-id="4820a-119">Nom du cookie.</span><span class="sxs-lookup"><span data-stu-id="4820a-119">The name of the cookie.</span></span>  
*   <span data-ttu-id="4820a-120">**Valeur**.</span><span class="sxs-lookup"><span data-stu-id="4820a-120">**Value**.</span></span>  <span data-ttu-id="4820a-121">Valeur du cookie.</span><span class="sxs-lookup"><span data-stu-id="4820a-121">The value of the cookie.</span></span>  
*   <span data-ttu-id="4820a-122">**Domain (domaine**).</span><span class="sxs-lookup"><span data-stu-id="4820a-122">**Domain**.</span></span>  <span data-ttu-id="4820a-123">Les hôtes autorisés à recevoir le cookie.</span><span class="sxs-lookup"><span data-stu-id="4820a-123">The hosts that are allowed to receive the cookie.</span></span>  <span data-ttu-id="4820a-124">Voir [étendue des cookies][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="4820a-124">See [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="4820a-125">**Path**.</span><span class="sxs-lookup"><span data-stu-id="4820a-125">**Path**.</span></span>  <span data-ttu-id="4820a-126">URL qui doit exister dans l’URL requise pour envoyer l' `Cookie` en-tête.</span><span class="sxs-lookup"><span data-stu-id="4820a-126">The URL that must exist in the requested URL in order to send the `Cookie` header.</span></span>  <span data-ttu-id="4820a-127">Voir [étendue des cookies][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="4820a-127">See [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="4820a-128">**Expire/max-age**.</span><span class="sxs-lookup"><span data-stu-id="4820a-128">**Expires / Max-Age**.</span></span>  <span data-ttu-id="4820a-129">Date d’expiration ou âge maximum du cookie.</span><span class="sxs-lookup"><span data-stu-id="4820a-129">The expiration date or maximum age of the cookie.</span></span>  <span data-ttu-id="4820a-130">Voir [cookies permanents][MDNHTTPCookiesPermanent].</span><span class="sxs-lookup"><span data-stu-id="4820a-130">See [Permanent cookies][MDNHTTPCookiesPermanent].</span></span>  <span data-ttu-id="4820a-131">Pour [les cookies de session][MDNHTTPCookiesSession] , cette valeur est toujours `Session` .</span><span class="sxs-lookup"><span data-stu-id="4820a-131">For [session cookies][MDNHTTPCookiesSession] this value is always `Session`.</span></span>  
*   <span data-ttu-id="4820a-132">**Taille**.</span><span class="sxs-lookup"><span data-stu-id="4820a-132">**Size**.</span></span>  <span data-ttu-id="4820a-133">Taille en octets du cookie.</span><span class="sxs-lookup"><span data-stu-id="4820a-133">The size, in bytes, of the cookie.</span></span>  
*   <span data-ttu-id="4820a-134">**Http**.</span><span class="sxs-lookup"><span data-stu-id="4820a-134">**HTTP**.</span></span>  <span data-ttu-id="4820a-135">Si la valeur est true, ce champ indique que le cookie doit uniquement être utilisé sur une modification HTTP et JavaScript n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="4820a-135">If true, this field indicates that the cookie should only be used over HTTP and JavaScript modification is not allowed.</span></span>  <span data-ttu-id="4820a-136">Voir [cookies HttpOnly][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="4820a-136">See [HttpOnly cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="4820a-137">**Sécurisé**.</span><span class="sxs-lookup"><span data-stu-id="4820a-137">**Secure**.</span></span>  <span data-ttu-id="4820a-138">Si la valeur est true, ce champ indique que le cookie doit être envoyé au serveur uniquement via une connexion sécurisée HTTPs.</span><span class="sxs-lookup"><span data-stu-id="4820a-138">If true, this field indicates that the cookie must be sent to the server only over a secure, HTTPS connection.</span></span>  <span data-ttu-id="4820a-139">Voir [cookies sécurisés][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="4820a-139">See [Secure cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="4820a-140">**SameSite**.</span><span class="sxs-lookup"><span data-stu-id="4820a-140">**SameSite**.</span></span>  <span data-ttu-id="4820a-141">Contient `strict` ou `lax` si le cookie utilise l’attribut [Samesite][MDNHTTPCookiesSamesite] expérimental.</span><span class="sxs-lookup"><span data-stu-id="4820a-141">Contains `strict` or `lax` if the cookie is using the experimental [Samesite][MDNHTTPCookiesSamesite] attribute.</span></span>  
*   <span data-ttu-id="4820a-142">**Priority**.</span><span class="sxs-lookup"><span data-stu-id="4820a-142">**Priority**.</span></span>  <span data-ttu-id="4820a-143">Contains `low` , `medium` \ (par défaut \) ou `high` si le cookie utilise l’attribut de [priorité de cookie][ChromiumIssue232693] amorti.</span><span class="sxs-lookup"><span data-stu-id="4820a-143">Contains `low`, `medium` \(default\), or `high` if the cookie is using the depreciated [cookie Priority][ChromiumIssue232693] attribute.</span></span>

## <span data-ttu-id="4820a-144">Filtrer les cookies</span><span class="sxs-lookup"><span data-stu-id="4820a-144">Filter cookies</span></span>  

<span data-ttu-id="4820a-145">Utilisez la zone de texte **filtre** pour filtrer les cookies par **nom** ou par **valeur**.</span><span class="sxs-lookup"><span data-stu-id="4820a-145">Use the **Filter** text box to filter cookies by **Name** or **Value**.</span></span>  <span data-ttu-id="4820a-146">Le filtrage par d’autres champs n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4820a-146">Filtering by other fields is not supported.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-filter-id.msft.png" alt-text="Filtrage de tout cookie qui ne contient pas l’ID de texte" lightbox="../media/storage-application-storage-cookies-filter-id.msft.png":::
   <span data-ttu-id="4820a-148">Figure 3: filtrage de tout cookie qui ne contient pas le texte</span><span class="sxs-lookup"><span data-stu-id="4820a-148">Figure 3:  Filtering out any cookies that do not contain the text</span></span> `ID`  
:::image-end:::  

## <span data-ttu-id="4820a-149">Modifier un cookie</span><span class="sxs-lookup"><span data-stu-id="4820a-149">Edit a cookie</span></span>  

<span data-ttu-id="4820a-150">Les champs **nom**, **valeur**, **domaine**, **chemin d’accès**et **durée d’expiration/maximum** doivent être modifiables.</span><span class="sxs-lookup"><span data-stu-id="4820a-150">The **Name**, **Value**, **Domain**, **Path**, and **Expires / Max-Age** fields are editable.</span></span>  
<span data-ttu-id="4820a-151">Double-cliquez sur un champ pour le modifier.</span><span class="sxs-lookup"><span data-stu-id="4820a-151">Double-click a field to edit it.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-rename.msft.png" alt-text="Définir le nom d’un cookie sur DEVTOOLS!" lightbox="../media/storage-application-storage-cookies-rename.msft.png":::
   <span data-ttu-id="4820a-153">Figure 4: définition du nom d’un cookie sur</span><span class="sxs-lookup"><span data-stu-id="4820a-153">Figure 4:  Setting the name of a cookie to</span></span> `DEVTOOLS!`  
:::image-end:::  

## <span data-ttu-id="4820a-154">Supprimer les cookies</span><span class="sxs-lookup"><span data-stu-id="4820a-154">Delete cookies</span></span>  

<span data-ttu-id="4820a-155">Sélectionnez un cookie et sélectionnez **supprimer** ![ la suppression sélectionnée ][ImageDeleteIcon] pour supprimer le cookie spécifique.</span><span class="sxs-lookup"><span data-stu-id="4820a-155">Select a cookie and select **Delete Selected** ![Delete Selected][ImageDeleteIcon]  to delete the specific cookie.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-delete-selected.msft.png" alt-text="Suppression d’un cookie spécifique" lightbox="../media/storage-application-storage-cookies-delete-selected.msft.png":::
   <span data-ttu-id="4820a-157">Figure 5: suppression d’un cookie spécifique</span><span class="sxs-lookup"><span data-stu-id="4820a-157">Figure 5:  Deleting a specific cookie</span></span>  
:::image-end:::  

<span data-ttu-id="4820a-158">Pour supprimer tous les cookies, sélectionnez **Effacer tout** ![ Effacer tout ][ImageClearIcon] .</span><span class="sxs-lookup"><span data-stu-id="4820a-158">Select **Clear All** ![Clear All][ImageClearIcon]  to delete all cookies.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-clear-all.msft.png" alt-text="Effacement de tous les cookies" lightbox="../media/storage-application-storage-cookies-clear-all.msft.png":::
   <span data-ttu-id="4820a-160">Figure 6: suppression de tous les cookies</span><span class="sxs-lookup"><span data-stu-id="4820a-160">Figure 6:  Clearing all cookies</span></span>  
:::image-end:::  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome)"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Ouvrir Microsoft Edge DevTools"  

[ChromiumIssue232693]: https://bugs.chromium.org/p/chromium/issues/detail?id=232693 "Problème de chrome 232693: application de champ de priorité pour les cookies | Bugs du chrome"  

[MDNHTTPCookies]: https://developer.mozilla.org/docs/Web/HTTP/Cookies "Cookies HTTP | MDN"  
[MDNHTTPCookiesPermanent]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Permanent_cookies "Cookies HTTP-cookies permanents | MDN"  
[MDNHTTPCookiesSamesite]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#SameSite_cookies "Cookies HTTP-cookies SameSite | MDN"  
[MDNHTTPCookiesScope]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Scope_of_cookies "Cookies HTTP-étendue des cookies | MDN"  
[MDNHTTPCookiesSecure]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Secure_and_HttpOnly_cookies "Cookies HTTP-cookies sécurisés et HttpOnly | MDN"  
[MDNHTTPCookiesSession]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Session_cookies "Cookies HTTP-cookies de session | MDN"  

> [!NOTE]
> <span data-ttu-id="4820a-170">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4820a-170">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4820a-171">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="4820a-171">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="4820a-173">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4820a-173">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
