---
description: Héberger et publier des extensions dans l’entreprise pour Microsoft Edge (Chromium).
title: Publier et mettre à jour des extensions dans Microsoft Edge magasin de modules extensions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, développement d’extensions, extensions de navigateur, addons, centre de partenaires, développeur
ms.openlocfilehash: 2249462b0a2dac86efa4b775171e2a3229a34431
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461219"
---
# <a name="publish-and-update-extensions-in-the-microsoft-edge-add-ons-store"></a>Publier et mettre à jour des extensions dans Microsoft Edge magasin de modules extensions  

La plupart des extensions sont publiées dans Microsoft Edge magasin d’extensions pour protéger les [utilisateurs][MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions] contre les extensions malveillantes.  

## <a name="publish-options-for-extensions"></a>Options de publication des extensions  

Toutes les extensions sont distribuées aux utilisateurs en tant que fichier d’archive \( `.zip` \) spécial avec `.crx` un suffixe.  Les extensions publiées dans Microsoft Edge magasin de modules extensions sont téléchargées en tant que `.zip` fichiers.  Le processus de publication convertit automatiquement le `.zip` fichier en `.crx` fichier.  

Les deux scénarios suivants n’exigent pas que vous publiiez votre extension dans Microsoft Edge magasin de modules extensions.  

*   Extensions distribuées à l’aide Enterprise stratégie.  
*   Utilisation de répertoires d’extension décompressés sur un ordinateur local lorsque Microsoft Edge est en mode développeur.  

## <a name="updates-to-extensions"></a>Mises à jour des extensions

Le Microsoft Edge recherche automatiquement les nouvelles versions des extensions installées. Les mises à jour sont installées sans intervention de l’utilisateur.  


<!-- image links -->

<!-- links -->  

[MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions]: https://microsoftedge.microsoft.com/insider-addons/category/EdgeExtensions "Extensions : Microsoft Edge les | Microsoft"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine se trouve [ici.](https://developer.chrome.com/extensions/hosting)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
