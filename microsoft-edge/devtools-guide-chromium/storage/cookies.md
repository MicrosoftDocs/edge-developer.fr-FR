---
description: Découvrez comment afficher, modifier et supprimer les cookies HTTP pour une page à l’aide de Microsoft Edge DevTools.
title: Afficher, modifier et supprimer des cookies avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: eaaf4663504fc674fd70dc1ca9e0357febb529e0
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993239"
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

# <span data-ttu-id="0eb94-104">Afficher, modifier et supprimer des cookies avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0eb94-104">View, edit, and delete cookies with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="0eb94-105">[Les cookies http][MDNHTTPCookies] sont principalement utilisés pour gérer les sessions utilisateur, stocker les préférences utilisateur de personnalisation et suivre le comportement des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="0eb94-105">[HTTP Cookies][MDNHTTPCookies] are mainly used to manage user sessions, store user personalization preferences, and track user behavior.</span></span>  <span data-ttu-id="0eb94-106">Les cookies sont également à l’origine de tous les types de consentement «cette page utilise des cookies» que vous voyez sur le Web.</span><span class="sxs-lookup"><span data-stu-id="0eb94-106">Cookies are also the cause of all of the annoying "this page uses cookies" consent forms that you see across the web.</span></span>  <span data-ttu-id="0eb94-107">Le guide suivant vous explique comment afficher, modifier et supprimer les cookies HTTP pour une page avec [Microsoft Edge devtools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="0eb94-107">The following guide teaches you how to view, edit, and delete the HTTP cookies for a page with [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="0eb94-108">Ouvrir le volet cookies</span><span class="sxs-lookup"><span data-stu-id="0eb94-108">Open the Cookies pane</span></span>  

1.  <span data-ttu-id="0eb94-109">[Ouvrez devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="0eb94-109">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="0eb94-110">Sélectionnez l’onglet **application** pour ouvrir le volet de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="0eb94-110">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="0eb94-111">Le volet **manifeste** doit être ouvert.</span><span class="sxs-lookup"><span data-stu-id="0eb94-111">The **Manifest** pane should open.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest-empty.msft.png":::
       <span data-ttu-id="0eb94-113">Figure 1: volet manifeste</span><span class="sxs-lookup"><span data-stu-id="0eb94-113">Figure 1:  The Manifest pane</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="0eb94-114">Sous **stockage** , développez **cookies**, puis sélectionnez une origine.</span><span class="sxs-lookup"><span data-stu-id="0eb94-114">Under **Storage** expand **Cookies**, then select an origin.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-cookies-selected.msft.png" alt-text="Volet cookies" lightbox="../media/storage-application-storage-cookies-selected.msft.png":::
       <span data-ttu-id="0eb94-116">Figure 2: volet cookies</span><span class="sxs-lookup"><span data-stu-id="0eb94-116">Figure 2:  The Cookies pane</span></span>  
    :::image-end:::  

## <span data-ttu-id="0eb94-117">Champs</span><span class="sxs-lookup"><span data-stu-id="0eb94-117">Fields</span></span>  

<span data-ttu-id="0eb94-118">La table **cookies** contient les champs suivants.</span><span class="sxs-lookup"><span data-stu-id="0eb94-118">The **Cookies** table contains the following fields.</span></span>  

*   <span data-ttu-id="0eb94-119">**Nom**.</span><span class="sxs-lookup"><span data-stu-id="0eb94-119">**Name**.</span></span>  <span data-ttu-id="0eb94-120">Nom du cookie.</span><span class="sxs-lookup"><span data-stu-id="0eb94-120">The name of the cookie.</span></span>  
*   <span data-ttu-id="0eb94-121">**Valeur**.</span><span class="sxs-lookup"><span data-stu-id="0eb94-121">**Value**.</span></span>  <span data-ttu-id="0eb94-122">Valeur du cookie.</span><span class="sxs-lookup"><span data-stu-id="0eb94-122">The value of the cookie.</span></span>  
*   <span data-ttu-id="0eb94-123">**Domain (domaine**).</span><span class="sxs-lookup"><span data-stu-id="0eb94-123">**Domain**.</span></span>  <span data-ttu-id="0eb94-124">Les hôtes autorisés à recevoir le cookie.</span><span class="sxs-lookup"><span data-stu-id="0eb94-124">The hosts that are allowed to receive the cookie.</span></span>  <span data-ttu-id="0eb94-125">Voir [étendue des cookies][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="0eb94-125">See [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="0eb94-126">**Path**.</span><span class="sxs-lookup"><span data-stu-id="0eb94-126">**Path**.</span></span>  <span data-ttu-id="0eb94-127">URL qui doit exister dans l’URL requise pour envoyer l' `Cookie` en-tête.</span><span class="sxs-lookup"><span data-stu-id="0eb94-127">The URL that must exist in the requested URL in order to send the `Cookie` header.</span></span>  <span data-ttu-id="0eb94-128">Voir [étendue des cookies][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="0eb94-128">See [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="0eb94-129">**Expire/max-age**.</span><span class="sxs-lookup"><span data-stu-id="0eb94-129">**Expires / Max-Age**.</span></span>  <span data-ttu-id="0eb94-130">Date d’expiration ou âge maximum du cookie.</span><span class="sxs-lookup"><span data-stu-id="0eb94-130">The expiration date or maximum age of the cookie.</span></span>  <span data-ttu-id="0eb94-131">Voir [cookies permanents][MDNHTTPCookiesPermanent].</span><span class="sxs-lookup"><span data-stu-id="0eb94-131">See [Permanent cookies][MDNHTTPCookiesPermanent].</span></span>  <span data-ttu-id="0eb94-132">Pour [les cookies de session][MDNHTTPCookiesSession] , cette valeur est toujours `Session` .</span><span class="sxs-lookup"><span data-stu-id="0eb94-132">For [session cookies][MDNHTTPCookiesSession] this value is always `Session`.</span></span>  
*   <span data-ttu-id="0eb94-133">**Taille**.</span><span class="sxs-lookup"><span data-stu-id="0eb94-133">**Size**.</span></span>  <span data-ttu-id="0eb94-134">Taille en octets du cookie.</span><span class="sxs-lookup"><span data-stu-id="0eb94-134">The size, in bytes, of the cookie.</span></span>  
*   <span data-ttu-id="0eb94-135">**Http**.</span><span class="sxs-lookup"><span data-stu-id="0eb94-135">**HTTP**.</span></span>  <span data-ttu-id="0eb94-136">Si la valeur est true, ce champ indique que le cookie doit uniquement être utilisé sur une modification HTTP et JavaScript n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="0eb94-136">If true, this field indicates that the cookie should only be used over HTTP and JavaScript modification is not allowed.</span></span>  <span data-ttu-id="0eb94-137">Voir [cookies HttpOnly][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="0eb94-137">See [HttpOnly cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="0eb94-138">**Sécurisé**.</span><span class="sxs-lookup"><span data-stu-id="0eb94-138">**Secure**.</span></span>  <span data-ttu-id="0eb94-139">Si la valeur est true, ce champ indique que le cookie doit être envoyé au serveur uniquement via une connexion sécurisée HTTPs.</span><span class="sxs-lookup"><span data-stu-id="0eb94-139">If true, this field indicates that the cookie must be sent to the server only over a secure, HTTPS connection.</span></span>  <span data-ttu-id="0eb94-140">Voir [cookies sécurisés][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="0eb94-140">See [Secure cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="0eb94-141">**SameSite**.</span><span class="sxs-lookup"><span data-stu-id="0eb94-141">**SameSite**.</span></span>  <span data-ttu-id="0eb94-142">Contient `strict` ou `lax` si le cookie utilise l’attribut [Samesite][MDNHTTPCookiesSamesite] expérimental.</span><span class="sxs-lookup"><span data-stu-id="0eb94-142">Contains `strict` or `lax` if the cookie is using the experimental [Samesite][MDNHTTPCookiesSamesite] attribute.</span></span>  
*   <span data-ttu-id="0eb94-143">**Priority**.</span><span class="sxs-lookup"><span data-stu-id="0eb94-143">**Priority**.</span></span>  <span data-ttu-id="0eb94-144">Contains `low` , `medium` \ (par défaut \) ou `high` si le cookie utilise l’attribut de [priorité de cookie][ChromiumIssue232693] déconseillé.</span><span class="sxs-lookup"><span data-stu-id="0eb94-144">Contains `low`, `medium` \(default\), or `high` if the cookie is using the deprecated [cookie Priority][ChromiumIssue232693] attribute.</span></span>

## <span data-ttu-id="0eb94-145">Filtrer les cookies</span><span class="sxs-lookup"><span data-stu-id="0eb94-145">Filter cookies</span></span>  

<span data-ttu-id="0eb94-146">Utilisez la zone de texte **filtre** pour filtrer les cookies par **nom** ou par **valeur**.</span><span class="sxs-lookup"><span data-stu-id="0eb94-146">Use the **Filter** text box to filter cookies by **Name** or **Value**.</span></span>  <span data-ttu-id="0eb94-147">Le filtrage par d’autres champs n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="0eb94-147">Filtering by other fields is not supported.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-filter-id.msft.png" alt-text="Filtrage de tout cookie qui ne contient pas l’ID de texte" lightbox="../media/storage-application-storage-cookies-filter-id.msft.png":::
   <span data-ttu-id="0eb94-149">Figure 3: filtrage de tout cookie qui ne contient pas le texte</span><span class="sxs-lookup"><span data-stu-id="0eb94-149">Figure 3:  Filtering out any cookies that do not contain the text</span></span> `ID`  
:::image-end:::  

## <span data-ttu-id="0eb94-150">Modifier un cookie</span><span class="sxs-lookup"><span data-stu-id="0eb94-150">Edit a cookie</span></span>  

<span data-ttu-id="0eb94-151">Les champs **nom**, **valeur**, **domaine**, **chemin d’accès**et **durée d’expiration/maximum** doivent être modifiables.</span><span class="sxs-lookup"><span data-stu-id="0eb94-151">The **Name**, **Value**, **Domain**, **Path**, and **Expires / Max-Age** fields are editable.</span></span>  
<span data-ttu-id="0eb94-152">Double-cliquez sur un champ pour le modifier.</span><span class="sxs-lookup"><span data-stu-id="0eb94-152">Double-click a field to edit it.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-rename.msft.png" alt-text="Définir le nom d’un cookie sur DEVTOOLS!" lightbox="../media/storage-application-storage-cookies-rename.msft.png":::
   <span data-ttu-id="0eb94-154">Figure 4: définition du nom d’un cookie sur</span><span class="sxs-lookup"><span data-stu-id="0eb94-154">Figure 4:  Setting the name of a cookie to</span></span> `DEVTOOLS!`  
:::image-end:::  

## <span data-ttu-id="0eb94-155">Supprimer les cookies</span><span class="sxs-lookup"><span data-stu-id="0eb94-155">Delete cookies</span></span>  

<span data-ttu-id="0eb94-156">Sélectionnez un cookie et sélectionnez **supprimer** ![ la suppression sélectionnée ][ImageDeleteIcon]  pour supprimer le cookie spécifique.</span><span class="sxs-lookup"><span data-stu-id="0eb94-156">Select a cookie and select **Delete Selected** ![Delete Selected][ImageDeleteIcon]  to delete the specific cookie.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-delete-selected.msft.png" alt-text="Suppression d’un cookie spécifique" lightbox="../media/storage-application-storage-cookies-delete-selected.msft.png":::
   <span data-ttu-id="0eb94-158">Figure 5: suppression d’un cookie spécifique</span><span class="sxs-lookup"><span data-stu-id="0eb94-158">Figure 5:  Deleting a specific cookie</span></span>  
:::image-end:::  

<span data-ttu-id="0eb94-159">Pour supprimer tous les cookies, sélectionnez **Effacer tout** ![ Effacer tout ][ImageClearIcon]  .</span><span class="sxs-lookup"><span data-stu-id="0eb94-159">Select **Clear All** ![Clear All][ImageClearIcon]  to delete all cookies.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-clear-all.msft.png" alt-text="Effacement de tous les cookies" lightbox="../media/storage-application-storage-cookies-clear-all.msft.png":::
   <span data-ttu-id="0eb94-161">Figure 6: suppression de tous les cookies</span><span class="sxs-lookup"><span data-stu-id="0eb94-161">Figure 6:  Clearing all cookies</span></span>  
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
> <span data-ttu-id="0eb94-171">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0eb94-171">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0eb94-172">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="0eb94-172">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="0eb94-174">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0eb94-174">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
