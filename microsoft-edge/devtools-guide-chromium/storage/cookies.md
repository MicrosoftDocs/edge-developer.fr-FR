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





# Afficher, modifier et supprimer des cookies avec Microsoft Edge DevTools   

  

[Les cookies http][MDNHTTPCookies] sont principalement utilisés pour gérer les sessions utilisateur, stocker les préférences utilisateur de personnalisation et suivre le comportement des utilisateurs.  C’est aussi la cause de tous ces types de consentement «cette page utilise des cookies» que vous voyez sur le Web.  Ce guide vous explique comment afficher, modifier et supprimer les cookies HTTP pour une page avec [Microsoft Edge devtools][MicrosoftEdgeDevTools].  

## Ouvrir le volet cookies   

1.  [Ouvrez devtools][DevToolsOpen].  
1.  Sélectionnez l’onglet **application** pour ouvrir le volet de l' **application** .  Le volet **manifeste** doit être ouvert.  
    
    > ##### Figure1  
    > Volet manifeste  
    > ![Volet manifeste][ImageManifest]  

1.  Sous **stockage** , développez **cookies**, puis sélectionnez une origine.  
    
    > ##### Figure 2  
    > Volet cookies  
    > ![Volet cookies][ImageCookies]  

## Champs   

La table **cookies** contient les champs suivants:  

*   **Nom**.  Nom du cookie.  
*   **Valeur**.  Valeur du cookie.  
*   **Domain (domaine**).  Les hôtes autorisés à recevoir le cookie.  Voir [étendue des cookies][MDNHTTPCookiesScope].  
*   **Path**.  URL qui doit exister dans l’URL requise pour envoyer l' `Cookie` en-tête.  Voir [étendue des cookies][MDNHTTPCookiesScope].  
*   **Expire/max-age**.  Date d’expiration ou âge maximum du cookie.  Voir [cookies permanents][MDNHTTPCookiesPermanent].  Pour [les cookies de session][MDNHTTPCookiesSession] , cette valeur est toujours `Session` .  
*   **Taille**.  Taille en octets du cookie.  
*   **Http**.  Si la valeur est true, ce champ indique que le cookie doit uniquement être utilisé sur une modification HTTP et JavaScript n’est pas autorisée.  Voir [cookies HttpOnly][MDNHTTPCookiesSecure].  
*   **Sécurisé**.  Si la valeur est true, ce champ indique que le cookie doit être envoyé au serveur uniquement via une connexion sécurisée HTTPs.  Voir [cookies sécurisés][MDNHTTPCookiesSecure].  
*   **SameSite**.  Contient `strict` ou `lax` si le cookie utilise l’attribut [Samesite][MDNHTTPCookiesSamesite] expérimental.  

## Filtrer les cookies   

Utilisez la zone de texte **filtre** pour filtrer les cookies par **nom** ou par **valeur**.  Le filtrage par d’autres champs n’est pas pris en charge.  

> ##### Figure3  
> Filtrage de tout cookie qui ne contient pas le texte `ID`  
> ![Filtrage de tout cookie qui ne contient pas l’ID de texte][ImageCookiesFilter]  

## Modifier un cookie   

Les champs **nom**, **valeur**, **domaine**, **chemin d’accès**et **durée d’expiration/maximum** doivent être modifiables.  
Double-cliquez sur un champ pour le modifier.  

> ##### Figure 4  
> Définir le nom d’un cookie sur `DEVTOOLS!`  
> ![Définir le nom d’un cookie sur DEVTOOLS!][ImageEditCookie]  

## Supprimer les cookies   

Sélectionnez un cookie, puis cliquez sur **supprimer** ![ l’option supprimer sélectionnée ][ImageDeleteIcon] pour supprimer ce cookie.  

> ##### Figure 5  
> Suppression d’un cookie spécifique  
> ![Suppression d’un cookie spécifique][ImageDeleteCookie]  

Pour supprimer tous les cookies, sélectionnez **Effacer tout** ![ Effacer tout ][ImageClearIcon] .  

> ##### Figure 6  
> Effacement de tous les cookies  
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
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
