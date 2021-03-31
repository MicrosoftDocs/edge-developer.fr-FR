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

# <a name="view-edit-and-delete-cookies-with-microsoft-edge-devtools"></a>Afficher, modifier et supprimer des cookies avec Microsoft Edge DevTools  

[Les cookies HTTP sont][MDNHTTPCookies] principalement utilisés pour gérer les sessions utilisateur, stocker les préférences de personnalisation des utilisateurs et suivre le comportement de l’utilisateur.  Les cookies sont également la cause de l’agacement de cette page qui utilise des formulaires de **consentement de cookies** qui sont trouvés sur le web.  Le guide suivant vous apprend à afficher, modifier et supprimer les cookies HTTP d’une page web avec [Microsoft Edge DevTools][MicrosoftEdgeDevTools].  

## <a name="open-the-cookies-pane"></a>Ouvrir le volet Cookies  

1.  [Ouvrez DevTools][DevToolsOpen].  
1.  Choisissez **l’onglet Application** pour ouvrir le **panneau Application.**  Le **volet** Manifeste doit s’ouvrir.  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest-empty.msft.png":::
       Figure 1 : Volet manifeste  
    :::image-end:::  

1.  Sous **Stockage,** **développez Cookies,** puis sélectionnez une origine.  
    
    :::image type="complex" source="../media/storage-application-storage-cookies-selected.msft.png" alt-text="Volet Cookies" lightbox="../media/storage-application-storage-cookies-selected.msft.png":::
       Figure 2 : Volet Cookies  
    :::image-end:::  

## <a name="fields"></a>Champs  

La **table Cookies** contient les champs suivants.  

*   **Nom**.  Nom du cookie.  
*   **Valeur**.  Valeur du cookie.  
*   **Domaine**.  Hôtes autorisés à recevoir le cookie.  Accédez à [l’étendue des cookies.][MDNHTTPCookiesScope]  
*   **Chemin d’accès**.  URL qui doit exister dans l’URL demandée pour envoyer `Cookie` l’en-tête.  Accédez à [l’étendue des cookies.][MDNHTTPCookiesScope]  
*   **Expire / Max-Age**.  Date d’expiration ou âge maximal du cookie.  Accédez [à Cookies permanents.][MDNHTTPCookiesPermanent]  Pour [les cookies de session,][MDNHTTPCookiesSession] cette valeur est toujours `Session` .  
*   **Taille**.  Taille, en octets, du cookie.  
*   **HTTP**.  Si la valeur est True, ce champ indique que le cookie ne doit être utilisé que sur HTTP et que la modification JavaScript n’est pas autorisée.  Accédez [aux cookies HttpOnly.][MDNHTTPCookiesSecure]  
*   **Sécurisé**.  Si la valeur est True, ce champ indique que le cookie doit être envoyé au serveur uniquement sur une connexion HTTPS sécurisée.  Accédez [à Sécuriser les cookies.][MDNHTTPCookiesSecure]  
*   **SameSite**.  Contient `strict` ou si le cookie utilise `lax` l’attribut [expérimental Samesite.][MDNHTTPCookiesSamesite]  
*   **Priorité**.  Contient , \(default\) ou si le cookie utilise l’attribut `low` `medium` `high` Deprecated [cookie Priority.][ChromiumIssue232693]

## <a name="filter-cookies"></a>Filtrer les cookies  

Utilisez la **zone de** texte Filtrer pour filtrer les cookies par **nom ou** **valeur.**  Le filtrage par d’autres champs n’est pas pris en charge.  

:::image type="complex" source="../media/storage-application-storage-cookies-filter-id.msft.png" alt-text="Filtrage des cookies qui ne contiennent pas l’ID de texte" lightbox="../media/storage-application-storage-cookies-filter-id.msft.png":::
   Figure 3 : Filtrage des cookies qui ne contiennent pas le texte `ID`  
:::image-end:::  

## <a name="edit-a-cookie"></a>Modifier un cookie  

Les **champs Nom,** **Valeur,** **Domaine,** Chemin d’accès et **Expires/Max-Age** sont modifiables. ****  
Double-cliquez sur un champ pour le modifier.  

:::image type="complex" source="../media/storage-application-storage-cookies-rename.msft.png" alt-text="Définition du nom d’un cookie sur DEVTOOLS !" lightbox="../media/storage-application-storage-cookies-rename.msft.png":::
   Figure 4 : Définition du nom d’un cookie sur `DEVTOOLS!`  
:::image-end:::  

## <a name="delete-cookies"></a>Supprimer les cookies  

Choisissez un cookie et choisissez **Supprimer sélectionné** \( Supprimer sélectionné ![ ](../media/delete-icon.msft.png) \) pour supprimer le cookie spécifique.  

:::image type="complex" source="../media/storage-application-storage-cookies-delete-selected.msft.png" alt-text="Suppression d’un cookie spécifique" lightbox="../media/storage-application-storage-cookies-delete-selected.msft.png":::
   Figure 5 : Suppression d’un cookie spécifique  
:::image-end:::  

Choisissez **Effacer tout** \( Effacer tout ![ ](../media/clear-icon.msft.png) \) pour supprimer tous les cookies.  

:::image type="complex" source="../media/storage-application-storage-cookies-clear-all.msft.png" alt-text="Effacement de tous les cookies" lightbox="../media/storage-application-storage-cookies-clear-all.msft.png":::
   Figure 6 : Effacement de tous les cookies  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

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
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
