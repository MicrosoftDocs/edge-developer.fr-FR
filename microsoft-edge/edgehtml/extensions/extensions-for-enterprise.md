---
ms.assetid: 8e2f75c4-fb7f-4892-a6c2-23bac081581a
description: En savoir plus sur les aspects spécifiques à l’entreprise de Microsoft Edge extensions et sur la manière dont ils sont similaires aux applications UWP.
title: Extensions pour les entreprises
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7c23bc24e20b7b00b8779f209dcac8c795067fd5
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233491"
---
# Extensions pour les entreprises  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

Les extensions Microsoft Edge sont dotées d’un flux de travail semblable par rapport à d’autres applications UWP d’entreprise. Les informations ci-dessous détaillent les aspects spécifiques à l’entreprise d’extensions Microsoft Edge.

## Prérequis
Les éléments suivants sont suggérés pour développer, empaqueter et déployer une extension Microsoft Edge pour les entreprises:

+ Compte du portail des développeurs Windows, pour signer et libérer l’extension du magasin privé d’entreprise. Pour plus d’informations, voir [ouverture d’un compte de développeur](/windows/uwp/publish/opening-a-developer-account) .
+ Microsoft Store pour les entreprises ou l’éducation, pour distribuer l’application auprès de l’entreprise. Pour plus d’informations, consultez la [documentation Microsoft Store pour les entreprises et l’éducation](/microsoft-store/) .
+ Identifiez les versions de Windows 10 qui utiliseront l’extension Microsoft Edge. Pour obtenir une liste des versions de Windows 10 existantes, voir les [informations de publication de Windows 10](https://www.microsoft.com/itpro/windows-10/release-information) .

> [!NOTE]
> Les chargement indépendant peuvent être considérées comme une alternative à l’utilisation du portail Windows pour les développeurs pour signer la version de l’extension. Pour plus d’informations, consultez le comportement des extensions chargement indépendant ci-dessous.

## Protection des informations Windows
Pour l’instant, les extensions Microsoft Edge ne respectent pas les paramètres de protection des informations Windows (WIP). Si une entreprise est soucieuse de la protection des données, la prise en charge des extensions ne doit pas être activée pour Microsoft Edge.

Pour désactiver les extensions destinées aux employés, configurez les paramètres de stratégie de groupe et Microsoft Intune. Pour plus d’informations sur les stratégies à configurer, voir [stratégies disponibles pour Microsoft Edge](https://technet.microsoft.com/itpro/microsoft-edge/available-policies).

## Extensions de package
Pour qu’une entreprise puisse distribuer une extension à ses employés, elle doit d’abord être empaquetée. Les instructions sur les extensions de package sont disponibles dans le Guide de création de [packages](./guides/packaging.md) .

> [!TIP]
> Veillez à tester l’installation et l’exécution de votre extension sur toutes les versions de Windows 10 pour vous assurer qu’elle fonctionne correctement avant la distribution.

## Distribution d’extensions
Une fois l’extension empaquetée, elle peut être distribuée aux employés via le Microsoft Store, Microsoft Store pour entreprises ou par chargement indépendant.

Les extensions distribuées via le Microsoft Store entreprise peuvent être affectées à des employés ou ajoutées à un magasin privé dans lequel tous les employés peuvent y accéder. Pour cela, vous pouvez suivre le guide [distribuer des applications métier aux entreprises](https://msdn.microsoft.com/windows/uwp/publish/distribute-lob-apps-to-enterprises) du guide.

Pour charger extensions de périphériques (non gérées ou gérées) doivent être déverrouillées pour chargement indépendant. Pour plus d’informations sur la façon d’charger les extensions empaquetées, voir [charger d’applications métier dans Windows 10](https://technet.microsoft.com/itpro/windows/deploy/sideload-apps-in-windows-10) .

> [!IMPORTANT]
> Si l’entreprise développe et distribue l’extension en interne, l’entreprise nécessite le Microsoft Store pour les entreprises (ou l’éducation) et un compte du portail des développeurs Windows.

### Comportement des extensions chargée
Contrairement aux extensions distribuées via le Microsoft Store (ou le Microsoft Store entreprise), les extensions chargée sont traitées différemment dans Microsoft Edge.

La première différence affecte le comportement des extensions chargée après l’installation. Contrairement aux extensions du Microsoft Store, les extensions chargée n’affichent pas immédiatement la notification «vous avez une nouvelle extension» et doivent être activées manuellement par l’utilisateur.

Pour activer l’extension, ouvrez le menu **autres (...)** , sélectionnez **«Extensions»** et l’extension chargée doit apparaître dans la liste des extensions installées. Cliquez sur l’extension et activez-la.

La deuxième différence affecte le mode d’affichage des extensions chargée dans le navigateur. Par exemple, la notification «vous avez une nouvelle extension» et la liste des extensions installées incluent un avertissement supplémentaire indiquant que l’extension provient d’une source inconnue.

![AVERTISSEMENT 1 charger](./media/sideload-permissionflyout.PNG)

![AVERTISSEMENT 2 charger](./media/sideload-l1warning.PNG)

La troisième et dernière différence influence le comportement des extensions chargée au démarrage du navigateur. Les extensions chargée sur les appareils qui sont activés par le domaine ou pour la gestion des périphériques mobiles seront similaires à celles du Microsoft Store. Toutefois, les extensions chargée sur les appareils qui ne sont pas joints à un domaine ou qui sont activés par le biais de la gestion des périphériques mobiles seront désactivées lors du démarrage du navigateur et nécessitent l’intervention de l’utilisateur.

Peu de temps après le démarrage du navigateur (après 10 secondes d’inactivité), la notification suivante s’affiche dans la partie inférieure de la fenêtre.

![notification charger](./media/sideload-scareUI.PNG)

Chaque fois que Microsoft Edge est lancé, les utilisateurs doivent sélectionner «allumer» de manière à utiliser l’extension.
