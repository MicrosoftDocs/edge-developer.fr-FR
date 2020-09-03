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

# Afficher, modifier et supprimer des cookies avec Microsoft Edge DevTools  

[Les cookies http][MDNHTTPCookies] sont principalement utilisés pour gérer les sessions utilisateur, stocker les préférences utilisateur de personnalisation et suivre le comportement des utilisateurs.  Les cookies sont également à l’origine de tous les types de consentement «cette page utilise des cookies» que vous voyez sur le Web.  Le guide suivant vous explique comment afficher, modifier et supprimer les cookies HTTP pour une page avec [Microsoft Edge devtools][MicrosoftEdgeDevTools].  

## Ouvrir le volet cookies  

1.  [Ouvrez devtools][DevToolsOpen].  
1.  Sélectionnez l’onglet **application** pour ouvrir le volet de l' **application** .  Le volet **manifeste** doit être ouvert.  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest-empty.msft.png":::
       Figure 1: volet manifeste  
    :::image-end:::  

1.  Sous **stockage** , développez **cookies**, puis sélectionnez une origine.  
    
    :::image type="complex" source="../media/storage-application-storage-cookies-selected.msft.png" alt-text="Volet cookies" lightbox="../media/storage-application-storage-cookies-selected.msft.png":::
       Figure 2: volet cookies  
    :::image-end:::  

## Champs  

La table **cookies** contient les champs suivants.  

*   **Nom**.  Nom du cookie.  
*   **Valeur**.  Valeur du cookie.  
*   **Domain (domaine**).  Les hôtes autorisés à recevoir le cookie.  Voir [étendue des cookies][MDNHTTPCookiesScope].  
*   **Path**.  URL qui doit exister dans l’URL requise pour envoyer l' `Cookie` en-tête.  Voir [étendue des cookies][MDNHTTPCookiesScope].  
*   **Expire/max-age**.  Date d’expiration ou âge maximum du cookie.  Voir [cookies permanents][MDNHTTPCookiesPermanent].  Pour [les cookies de session][MDNHTTPCookiesSession] , cette valeur est toujours `Session` .  
*   **Taille**.  Taille en octets du cookie.  
*   **Http**.  Si la valeur est true, ce champ indique que le cookie doit uniquement être utilisé sur une modification HTTP et JavaScript n’est pas autorisée.  Voir [cookies HttpOnly][MDNHTTPCookiesSecure].  
*   **Sécurisé**.  Si la valeur est true, ce champ indique que le cookie doit être envoyé au serveur uniquement via une connexion sécurisée HTTPs.  Voir [cookies sécurisés][MDNHTTPCookiesSecure].  
*   **SameSite**.  Contient `strict` ou `lax` si le cookie utilise l’attribut [Samesite][MDNHTTPCookiesSamesite] expérimental.  
*   **Priority**.  Contains `low` , `medium` \ (par défaut \) ou `high` si le cookie utilise l’attribut de [priorité de cookie][ChromiumIssue232693] déconseillé.

## Filtrer les cookies  

Utilisez la zone de texte **filtre** pour filtrer les cookies par **nom** ou par **valeur**.  Le filtrage par d’autres champs n’est pas pris en charge.  

:::image type="complex" source="../media/storage-application-storage-cookies-filter-id.msft.png" alt-text="Filtrage de tout cookie qui ne contient pas l’ID de texte" lightbox="../media/storage-application-storage-cookies-filter-id.msft.png":::
   Figure 3: filtrage de tout cookie qui ne contient pas le texte `ID`  
:::image-end:::  

## Modifier un cookie  

Les champs **nom**, **valeur**, **domaine**, **chemin d’accès**et **durée d’expiration/maximum** doivent être modifiables.  
Double-cliquez sur un champ pour le modifier.  

:::image type="complex" source="../media/storage-application-storage-cookies-rename.msft.png" alt-text="Définir le nom d’un cookie sur DEVTOOLS!" lightbox="../media/storage-application-storage-cookies-rename.msft.png":::
   Figure 4: définition du nom d’un cookie sur `DEVTOOLS!`  
:::image-end:::  

## Supprimer les cookies  

Sélectionnez un cookie et sélectionnez **supprimer** ![ la suppression sélectionnée ][ImageDeleteIcon]  pour supprimer le cookie spécifique.  

:::image type="complex" source="../media/storage-application-storage-cookies-delete-selected.msft.png" alt-text="Suppression d’un cookie spécifique" lightbox="../media/storage-application-storage-cookies-delete-selected.msft.png":::
   Figure 5: suppression d’un cookie spécifique  
:::image-end:::  

Pour supprimer tous les cookies, sélectionnez **Effacer tout** ![ Effacer tout ][ImageClearIcon]  .  

:::image type="complex" source="../media/storage-application-storage-cookies-clear-all.msft.png" alt-text="Effacement de tous les cookies" lightbox="../media/storage-application-storage-cookies-clear-all.msft.png":::
   Figure 6: suppression de tous les cookies  
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
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
