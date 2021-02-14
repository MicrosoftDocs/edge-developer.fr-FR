---
description: Héberger et publier des extensions dans l’entreprise pour Microsoft Edge (Chromium).
title: Publier et mettre à jour des extensions dans le magasin de modules extensions Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, développement d’extensions, extensions de navigateur, addons, centre de partenaires, développeur
ms.openlocfilehash: 91fdd5c2f625890653085e8999da3e513b072348
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327686"
---
# Publier et mettre à jour des extensions dans le magasin de modules extensions Microsoft Edge  

La plupart des extensions sont publiées dans le magasin des [extensions Microsoft Edge][MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions] pour protéger les utilisateurs contre les extensions malveillantes.  

## Options de publication des extensions  

Toutes les extensions sont distribuées aux utilisateurs en tant que fichier d’archive \( `.zip` \) spécial avec `.crx` un suffixe.  Les extensions publiées dans le magasin des extensions Microsoft Edge sont téléchargées en tant que `.zip` fichiers.  Le processus de publication convertit automatiquement le `.zip` fichier en `.crx` fichier.  

Les deux scénarios suivants n’exigent pas que vous publiiez votre extension dans le magasin de modules extensions Microsoft Edge.  

*   Extensions distribuées à l’aide de la stratégie Entreprise.  
*   Utilisation de répertoires d’extension décompressés sur un ordinateur local lorsque Microsoft Edge est en mode développeur.  

## Mises à jour des extensions

Le navigateur Microsoft Edge recherche régulièrement les nouvelles versions des extensions installées et les mises à jour sans intervention de l’utilisateur.  

<!-- links -->  

[MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions]: https://microsoftedge.microsoft.com/insider-addons/category/EdgeExtensions "Extensions - Microsoft Edge Insider Addons | Microsoft"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine se trouve [ici.](https://developer.chrome.com/extensions/hosting)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
