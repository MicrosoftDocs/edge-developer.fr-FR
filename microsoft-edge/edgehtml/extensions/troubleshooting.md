---
ms.assetid: 8b7f362f-da09-43db-8a42-cfa128c1808c
description: Obtenez les réponses aux questions fréquemment posées lors du chargement d’extensions décompressées.
title: Extensions-résolution des problèmes
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 74743923000766473a96b56a97d302b6ab79a9e3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233014"
---
# Résolution des problèmes  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

Si vous essayez de charger les extensions décompressées et rencontrez des problèmes, les informations ci-dessous peuvent vous aider:

## 1. le message d’erreur «nous n’avons pas pu charger cette extension» s’affiche

En règle générale, Microsoft Edge ne peut pas accéder au dossier d’extension que vous avez essayé de charger.

Voici un résumé des erreurs possibles qui peuvent se produire:

Message d’erreur | Détails
:--------- | :------------
Erreur d’analyse du manifeste: fichier manifeste manquant ou incorrect. | Le fichier est `"manifest.json"` introuvable dans l’emplacement spécifié ou il y a un problème avec le fichier. Pour résoudre ce problème, assurez-vous que le dossier spécifié contient le manifeste au niveau supérieur, puis vérifiez que vous disposez de points, de guillemets et de crochets.
Erreur d’analyse du manifeste: `"content_scripts"` doit définir un tableau. | Le champ `"content_scripts"` doit être un tableau. Pour résoudre ce problème, vérifiez la syntaxe. Par exemple: `"content_scripts": [{"matches": [...],"css": [...],"js": [...] }]`
Erreur d’analyse du manifeste: `"content_scripts"` doit définir value pour `"matches"` Property. | La propriété `"matches"` est requise. Pour résoudre ce problème, spécifiez la valeur de la propriété à l’aide d’un tableau de chaînes. Par exemple: `"content_scripts": [ {... "matches": ["http://www.bing.com"] ...} ]`
Erreur d’analyse du manifeste: `"content_scripts"` doit référencer au moins un fichier. CSS ou. js. | Au moins une propriété `"css"` `"js"` est requise. Pour résoudre ce problème, spécifiez la valeur de la propriété à l’aide d’un tableau de chaînes. Par exemple: `"content_scripts": [ { ... "js": ["myScript1.js", "myScript2.js"] ...} ]`
Erreur d’analyse du manifeste: `"<field>"` doit définir la valeur de la <property> propriété «». | La propriété du `<property>` champ `<field>` est requise. Pour résoudre ce problème, spécifiez une valeur valide pour `<property>` .
Erreur d’analyse du manifeste: `"content_scripts"` fait référence à la valeur non valide pour le champ «run_at». | La propriété `"run_at"` spécifie une valeur inconnue. Pour résoudre ce problème, spécifiez l’un des `"document_start"` , `"document_end"` ou `"document_idle"` . Par exemple: `"content_scripts": [ {... "run_at": "document_start" ... } ]`
Erreur d’analyse du manifeste: `"<field>"` champ manquant. | Le champ `<field>` est obligatoire. Pour résoudre ce problème, définissez le champ avec une valeur valide.
Erreur d’analyse du manifeste: champ non valide `"<field1>"` détecté dans `"<field2>"` . | Le champ du <field1> champ <field2> spécifie une valeur inconnue. Pour résoudre ce problème, spécifiez une valeur valide pour <field1> .
Erreur d’analyse du manifeste: valeur non valide pour le <field> champ «». | Le champ <field> spécifie une valeur inconnue. Pour résoudre ce problème, spécifiez une valeur valide.
Erreur d’analyse du manifeste: l’extension n’est pas prise en charge par la version actuelle de Microsoft Edge. | La propriété `"minimum_edge_version"` spécifie une version plus récente de Microsoft Edge que celle que vous possédez. Vous pouvez trouver la version actuelle en ouvrant le «...» Menu (plus), puis sélection de «paramètres» (section en bas sur à propos de cette application). Pour résoudre le problème, mettez à jour votre navigateur en utilisant une version plus récente ou modifiez la valeur du manifeste. Par exemple: `"minimum_edge_version": "x.xxxx.xxxx.x"`
Erreur d’analyse du manifeste: `"background"` doit définir la valeur de la propriété «page» ou «scripts». | La propriété «page» ou «scripts» est obligatoire pour le champ «background». Pour résoudre ce problème, spécifiez une chaîne pour «page» ou un tableau de chaînes pour «scripts». Par exemple: `"background": { ... "scripts": ["background.js"] ... }`
Erreur d’analyse du manifeste: `"background"` doit définir value pour `"persistent"` Property. | La propriété `"persistent"` est requise. Pour résoudre ce problème, spécifiez une valeur true ou false. Par exemple: `"background": {... "persistent": true ...}`
Erreur d’analyse du manifeste: seule une `"browser_action"` ou `"page_action"` peut être définie. | Une extension ne peut pas définir une action de page et une action de navigateur en même temps. Pour résoudre ce problème, supprimez l’une des définitions.
Erreur non spécifiée: `<error>` | Message d’erreur Generic Catch-All. `<error>` sera remplacé par l’erreur spécifiée.


## 2. le bouton «charger l’extension» n’apparaît pas
Ce bouton doit être visible par défaut *si* les extensions sont disponibles sur le Microsoft Store. Si vous ouvrez le menu «plus» (...), sélectionnez l’élément de menu «extensions» et le bouton ne s’affiche pas, procédez comme suit:

1. Dans la barre d’adresses, tapez **«à propos** de», puis appuyez sur la touche **«entrée»** .
2. Sous le titre **«paramètres développeur»** , vérifiez que la case à cocher en regard de l’option **activer les fonctionnalités de développement d’extensions** est activée.

   ![à propos des indicateurs](./media/aboutflags.PNG)  

3. Fermez et rouvrez Microsoft Edge et regardez si le bouton **«charger une extension»** est désormais visible.
