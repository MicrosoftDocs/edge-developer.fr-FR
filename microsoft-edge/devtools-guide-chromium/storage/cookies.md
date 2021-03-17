---
description: Découvrez comment afficher, modifier et supprimer les cookies HTTP d’une page à l’aide de Microsoft Edge DevTools.
title: Afficher, modifier et supprimer des cookies avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: c208ca628fe91ed5922bc36566be2b9bdd20ec0b
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439681"
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

# <a name="view-edit-and-delete-cookies-with-microsoft-edge-devtools"></a><span data-ttu-id="2182c-104">Afficher, modifier et supprimer des cookies avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2182c-104">View, edit, and delete cookies with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="2182c-105">[Les cookies HTTP sont][MDNHTTPCookies] principalement utilisés pour gérer les sessions utilisateur, stocker les préférences de personnalisation des utilisateurs et suivre le comportement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2182c-105">[HTTP Cookies][MDNHTTPCookies] are mainly used to manage user sessions, store user personalization preferences, and track user behavior.</span></span>  <span data-ttu-id="2182c-106">Les cookies sont également la cause de l’agacement de cette page qui utilise des formulaires de **consentement de cookies** qui sont trouvés sur le web.</span><span class="sxs-lookup"><span data-stu-id="2182c-106">Cookies are also the cause of all of the annoying **this page uses cookies** consent forms that are found across the web.</span></span>  <span data-ttu-id="2182c-107">Le guide suivant vous apprend à afficher, modifier et supprimer les cookies HTTP d’une page web avec [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="2182c-107">The following guide teaches you how to view, edit, and delete the HTTP cookies for a webpage with [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <a name="open-the-cookies-pane"></a><span data-ttu-id="2182c-108">Ouvrir le volet Cookies</span><span class="sxs-lookup"><span data-stu-id="2182c-108">Open the Cookies pane</span></span>  

1.  <span data-ttu-id="2182c-109">[Ouvrez DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="2182c-109">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="2182c-110">Choisissez **l’onglet Application** pour ouvrir le **panneau Application.**</span><span class="sxs-lookup"><span data-stu-id="2182c-110">Choose the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="2182c-111">Le **volet** Manifeste doit s’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="2182c-111">The **Manifest** pane should open.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest-empty.msft.png":::
       <span data-ttu-id="2182c-113">Figure 1 : Volet manifeste</span><span class="sxs-lookup"><span data-stu-id="2182c-113">Figure 1:  The Manifest pane</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="2182c-114">Sous **Stockage,** **développez Cookies,** puis sélectionnez une origine.</span><span class="sxs-lookup"><span data-stu-id="2182c-114">Under **Storage** expand **Cookies**, then select an origin.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-cookies-selected.msft.png" alt-text="Volet Cookies" lightbox="../media/storage-application-storage-cookies-selected.msft.png":::
       <span data-ttu-id="2182c-116">Figure 2 : Volet Cookies</span><span class="sxs-lookup"><span data-stu-id="2182c-116">Figure 2:  The Cookies pane</span></span>  
    :::image-end:::  

## <a name="fields"></a><span data-ttu-id="2182c-117">Champs</span><span class="sxs-lookup"><span data-stu-id="2182c-117">Fields</span></span>  

<span data-ttu-id="2182c-118">La **table Cookies** contient les champs suivants.</span><span class="sxs-lookup"><span data-stu-id="2182c-118">The **Cookies** table contains the following fields.</span></span>  

*   <span data-ttu-id="2182c-119">**Nom**.</span><span class="sxs-lookup"><span data-stu-id="2182c-119">**Name**.</span></span>  <span data-ttu-id="2182c-120">Nom du cookie.</span><span class="sxs-lookup"><span data-stu-id="2182c-120">The name of the cookie.</span></span>  
*   <span data-ttu-id="2182c-121">**Valeur**.</span><span class="sxs-lookup"><span data-stu-id="2182c-121">**Value**.</span></span>  <span data-ttu-id="2182c-122">Valeur du cookie.</span><span class="sxs-lookup"><span data-stu-id="2182c-122">The value of the cookie.</span></span>  
*   <span data-ttu-id="2182c-123">**Domaine**.</span><span class="sxs-lookup"><span data-stu-id="2182c-123">**Domain**.</span></span>  <span data-ttu-id="2182c-124">Hôtes autorisés à recevoir le cookie.</span><span class="sxs-lookup"><span data-stu-id="2182c-124">The hosts that are allowed to receive the cookie.</span></span>  <span data-ttu-id="2182c-125">Accédez à [l’étendue des cookies.][MDNHTTPCookiesScope]</span><span class="sxs-lookup"><span data-stu-id="2182c-125">Navigate to [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="2182c-126">**Chemin d’accès**.</span><span class="sxs-lookup"><span data-stu-id="2182c-126">**Path**.</span></span>  <span data-ttu-id="2182c-127">URL qui doit exister dans l’URL demandée pour envoyer `Cookie` l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="2182c-127">The URL that must exist in the requested URL in order to send the `Cookie` header.</span></span>  <span data-ttu-id="2182c-128">Accédez à [l’étendue des cookies.][MDNHTTPCookiesScope]</span><span class="sxs-lookup"><span data-stu-id="2182c-128">Navigate to [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="2182c-129">**Expire / Max-Age**.</span><span class="sxs-lookup"><span data-stu-id="2182c-129">**Expires / Max-Age**.</span></span>  <span data-ttu-id="2182c-130">Date d’expiration ou âge maximal du cookie.</span><span class="sxs-lookup"><span data-stu-id="2182c-130">The expiration date or maximum age of the cookie.</span></span>  <span data-ttu-id="2182c-131">Accédez [à Cookies permanents.][MDNHTTPCookiesPermanent]</span><span class="sxs-lookup"><span data-stu-id="2182c-131">Navigate to [Permanent cookies][MDNHTTPCookiesPermanent].</span></span>  <span data-ttu-id="2182c-132">Pour [les cookies de session,][MDNHTTPCookiesSession] cette valeur est toujours `Session` .</span><span class="sxs-lookup"><span data-stu-id="2182c-132">For [session cookies][MDNHTTPCookiesSession] this value is always `Session`.</span></span>  
*   <span data-ttu-id="2182c-133">**Taille**.</span><span class="sxs-lookup"><span data-stu-id="2182c-133">**Size**.</span></span>  <span data-ttu-id="2182c-134">Taille, en octets, du cookie.</span><span class="sxs-lookup"><span data-stu-id="2182c-134">The size, in bytes, of the cookie.</span></span>  
*   <span data-ttu-id="2182c-135">**HTTP**.</span><span class="sxs-lookup"><span data-stu-id="2182c-135">**HTTP**.</span></span>  <span data-ttu-id="2182c-136">Si la valeur est True, ce champ indique que le cookie ne doit être utilisé que sur HTTP et que la modification JavaScript n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="2182c-136">If true, this field indicates that the cookie should only be used over HTTP and JavaScript modification is not allowed.</span></span>  <span data-ttu-id="2182c-137">Accédez [aux cookies HttpOnly.][MDNHTTPCookiesSecure]</span><span class="sxs-lookup"><span data-stu-id="2182c-137">Navigate to [HttpOnly cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="2182c-138">**Sécurisé**.</span><span class="sxs-lookup"><span data-stu-id="2182c-138">**Secure**.</span></span>  <span data-ttu-id="2182c-139">Si la valeur est True, ce champ indique que le cookie doit être envoyé au serveur uniquement sur une connexion HTTPS sécurisée.</span><span class="sxs-lookup"><span data-stu-id="2182c-139">If true, this field indicates that the cookie must be sent to the server only over a secure, HTTPS connection.</span></span>  <span data-ttu-id="2182c-140">Accédez [à Sécuriser les cookies.][MDNHTTPCookiesSecure]</span><span class="sxs-lookup"><span data-stu-id="2182c-140">Navigate to [Secure cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="2182c-141">**SameSite**.</span><span class="sxs-lookup"><span data-stu-id="2182c-141">**SameSite**.</span></span>  <span data-ttu-id="2182c-142">Contient `strict` ou si le cookie utilise `lax` l’attribut [expérimental Samesite.][MDNHTTPCookiesSamesite]</span><span class="sxs-lookup"><span data-stu-id="2182c-142">Contains `strict` or `lax` if the cookie is using the experimental [Samesite][MDNHTTPCookiesSamesite] attribute.</span></span>  
*   <span data-ttu-id="2182c-143">**Priorité**.</span><span class="sxs-lookup"><span data-stu-id="2182c-143">**Priority**.</span></span>  <span data-ttu-id="2182c-144">Contient , \(default\) ou si le cookie utilise l’attribut `low` `medium` `high` Deprecated [cookie Priority.][ChromiumIssue232693]</span><span class="sxs-lookup"><span data-stu-id="2182c-144">Contains `low`, `medium` \(default\), or `high` if the cookie is using the deprecated [cookie Priority][ChromiumIssue232693] attribute.</span></span>

## <a name="filter-cookies"></a><span data-ttu-id="2182c-145">Filtrer les cookies</span><span class="sxs-lookup"><span data-stu-id="2182c-145">Filter cookies</span></span>  

<span data-ttu-id="2182c-146">Utilisez la **zone de** texte Filtrer pour filtrer les cookies par **nom ou** **valeur.**</span><span class="sxs-lookup"><span data-stu-id="2182c-146">Use the **Filter** text box to filter cookies by **Name** or **Value**.</span></span>  <span data-ttu-id="2182c-147">Le filtrage par d’autres champs n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2182c-147">Filtering by other fields is not supported.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-filter-id.msft.png" alt-text="Filtrage des cookies qui ne contiennent pas l’ID de texte" lightbox="../media/storage-application-storage-cookies-filter-id.msft.png":::
   <span data-ttu-id="2182c-149">Figure 3 : Filtrage des cookies qui ne contiennent pas le texte</span><span class="sxs-lookup"><span data-stu-id="2182c-149">Figure 3:  Filtering out any cookies that do not contain the text</span></span> `ID`  
:::image-end:::  

## <a name="edit-a-cookie"></a><span data-ttu-id="2182c-150">Modifier un cookie</span><span class="sxs-lookup"><span data-stu-id="2182c-150">Edit a cookie</span></span>  

<span data-ttu-id="2182c-151">Les **champs Nom,** **Valeur,** **Domaine,** Chemin d’accès et **Expires/Max-Age** sont modifiables. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2182c-151">The **Name**, **Value**, **Domain**, **Path**, and **Expires / Max-Age** fields are editable.</span></span>  
<span data-ttu-id="2182c-152">Double-cliquez sur un champ pour le modifier.</span><span class="sxs-lookup"><span data-stu-id="2182c-152">Double-click a field to edit it.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-rename.msft.png" alt-text="Définition du nom d’un cookie sur DEVTOOLS !" lightbox="../media/storage-application-storage-cookies-rename.msft.png":::
   <span data-ttu-id="2182c-154">Figure 4 : Définition du nom d’un cookie sur</span><span class="sxs-lookup"><span data-stu-id="2182c-154">Figure 4:  Setting the name of a cookie to</span></span> `DEVTOOLS!`  
:::image-end:::  

## <a name="delete-cookies"></a><span data-ttu-id="2182c-155">Supprimer les cookies</span><span class="sxs-lookup"><span data-stu-id="2182c-155">Delete cookies</span></span>  

<span data-ttu-id="2182c-156">Choisissez un cookie et choisissez **Supprimer sélectionné** \( Supprimer sélectionné ![ ](../media/delete-icon.msft.png) \) pour supprimer le cookie spécifique.</span><span class="sxs-lookup"><span data-stu-id="2182c-156">Choose a cookie and choose **Delete Selected** \(![Delete Selected](../media/delete-icon.msft.png)\) to delete the specific cookie.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-delete-selected.msft.png" alt-text="Suppression d’un cookie spécifique" lightbox="../media/storage-application-storage-cookies-delete-selected.msft.png":::
   <span data-ttu-id="2182c-158">Figure 5 : Suppression d’un cookie spécifique</span><span class="sxs-lookup"><span data-stu-id="2182c-158">Figure 5:  Deleting a specific cookie</span></span>  
:::image-end:::  

<span data-ttu-id="2182c-159">Choisissez **Effacer tout** \( Effacer tout ![ ](../media/clear-icon.msft.png) \) pour supprimer tous les cookies.</span><span class="sxs-lookup"><span data-stu-id="2182c-159">Choose **Clear All** \(![Clear All](../media/clear-icon.msft.png)\) to delete all cookies.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-clear-all.msft.png" alt-text="Effacement de tous les cookies" lightbox="../media/storage-application-storage-cookies-clear-all.msft.png":::
   <span data-ttu-id="2182c-161">Figure 6 : Effacement de tous les cookies</span><span class="sxs-lookup"><span data-stu-id="2182c-161">Figure 6:  Clearing all cookies</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="2182c-162">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="2182c-162">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (Chromium)"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Ouvrir Microsoft Edge DevTools"  

[ChromiumIssue232693]: https://bugs.chromium.org/p/chromium/issues/detail?id=232693 "Problème Chromium 232693 : mise en œuvre du champ de priorité pour les cookies | Bogues Chromium"  

[MDNHTTPCookies]: https://developer.mozilla.org/docs/Web/HTTP/Cookies "Cookies HTTP | MDN"  
[MDNHTTPCookiesPermanent]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Permanent_cookies "Cookies HTTP : cookies permanents | MDN"  
[MDNHTTPCookiesSamesite]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#SameSite_cookies "Cookies HTTP : cookies SameSite | MDN"  
[MDNHTTPCookiesScope]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Scope_of_cookies "Cookies HTTP : étendue des cookies | MDN"  
[MDNHTTPCookiesSecure]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Secure_and_HttpOnly_cookies "Cookies HTTP : les cookies sécurisés et HttpOnly | MDN"  
[MDNHTTPCookiesSession]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Session_cookies "Cookies HTTP : cookies de session | MDN"  

> [!NOTE]
> <span data-ttu-id="2182c-172">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2182c-172">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2182c-173">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="2182c-173">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="2182c-175">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2182c-175">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
