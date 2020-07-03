---
ms.assetid: ''
description: Expérimentez en toute sécurité un laps de temps fixe et envoyez des commentaires sur les nouvelles fonctionnalités de la plateforme.
title: Premières versions d’essai
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, html, CSS, essais d’origine, développeur
ms.openlocfilehash: 470896435ab348419749a7de00adcdb83b784df3
ms.sourcegitcommit: 5cbc9237363b3a8ba212ca128aa03c71a33ec86f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2020
ms.locfileid: "10846525"
---
# Utiliser des essais d’origine dans Microsoft Edge  

Les développeurs peuvent utiliser des essais d’origine pour tester des API expérimentales sur les sites dynamiques pendant une durée limitée.  Lorsque vous utilisez des versions d’évaluation, les utilisateurs de Microsoft Edge qui accèdent à votre site peuvent exécuter du code qui utilise des API expérimentales.  Pour accéder aux API expérimentales de chaque ordinateur utilisateur, vous n’avez pas besoin d' `edge://flags` activer ou de désactiver les indicateurs de fonctionnalités.  Pour plus d’informations, reportez-vous à la rubrique [API expérimentales][DeveloperMicrsoftEdgeOriginTrials].  De plus, vous pouvez fournir des commentaires sur la conception de l’API, de vos cas d’utilisation ou de votre utilisation de l’API aux ingénieurs du navigateur et à la communauté Web standard.  

## Commencer à utiliser les essais d’origine  

Pour plus d’informations sur les API expérimentales disponibles dans Microsoft Edge, consultez la rubrique [Microsoft Edge Origin expérimentation console][DeveloperMicrsoftEdgeOriginTrials].  Veillez à consulter la configuration minimale requise pour la version de Microsoft Edge et la date de fin de la période d’évaluation pour vérifier que vous utilisez les API expérimentales sur votre site Web.  

> [!NOTE]
> Une expérience risque de terminer plus tôt que prévu si l’une des situations suivantes se produit.  
> *   Un incident de sécurité majeur.  
> *   Si des commentaires suffisants sont collectés et indiquent qu’une nouvelle conception est nécessaire pour répondre aux besoins des développeurs Web.  
> Dans les deux cas, un message électronique de notification est envoyé à tous les développeurs actuellement inscrits au cours de l’expérience.  

### S’inscrire à une version d’évaluation d’une API expérimentale  

Procédez comme suit pour vous inscrire à une version d’évaluation d’une API expérimentale.  

1.  Rendez-vous sur la page des [essais d’origine Microsoft Edge][DeveloperMicrsoftEdgeOriginTrials] .  
1.  Cliquez sur le bouton de Registre dans les expériences disponibles.  
1.  Connectez-vous à la console du développeur en utilisant votre nom d’utilisateur et votre mot de passe GitHub.  
1.  Sélectionnez **autoriser MicrosoftEdge**.  
1.  Remplissez le formulaire.  
    
    > [!NOTE]
    > Pour inscrire un ou plusieurs sous-domaines, sélectionnez définir le `Do you need to match all subdomains for the provided origin?` paramètre sur `Yes` .  Par exemple, `https://dev.contoso.com` est un domaine unique et `https://*.contoso.com` utilise un caractère générique pour représenter tous les sous-domaines.  
    
    > [!IMPORTANT]
    > Les formats d’origine suivants ne sont pas autorisés.  
    > *   Spécifiant un sous-dossier dans l’origine.  Par exemple: `https://contoso.com/path/subfolder`  
    > 
    > *   Utilisation d’une Origin avec des paramètres de chaîne de requête.  Par exemple: `https://contoso.com/path/feature?query_parameter=12345`  
    
1.  Sélectionnez **accepter et inscrivez**.  

### Appliquer votre jeton  

Un jeton est généré instantanément et affiché dans la page de la [console développeurs essais d’origine Microsoft Edge][DeveloperMicrsoftEdgeOriginTrials] .  Pour commencer à utiliser la version d’évaluation de votre site Web, appliquez l’une des méthodes suivantes pour appliquer le jeton à votre page.  

*   Ajoutez la `origin-trial` valeur d’attribut et votre jeton à la `meta` balise sur chaque page qui utilise l’API expérimentale.  
    
    ```html
    <meta http-equiv="origin-trial" content="replace-with-your-token">
    ```  
    
*   Ajoutez `Origin-Trial` l’en-tête de réponse http de votre serveur.  
    
    ```json
    Origin-Trial: replace-with-your-token
    ```  
    
> [!NOTE]
> Votre jeton est valide pour 6 semaines.  Avant la fin de la période d’évaluation, vous recevez des messages de rappel qui vous demandent vos commentaires et vous invite à envisager le renouvellement de votre version d’évaluation avant l’expiration de votre jeton.  

### Désactiver une expérience  

Pour désactiver une expérience, utilisez l’une des méthodes suivantes pour supprimer votre jeton.  

*   Supprimez la `meta` balise de chaque page qui a utilisé l’API expérimentale.  
    
    ```html
    <meta http-equiv="origin-trial" content="your-token">
    ```  
    
*   Supprimer `Origin-Trial` de l’en-tête de réponse http de votre serveur.  
    
    ```json
    Origin-Trial: your-token
    ```  
    
### Détecter les fonctionnalités expérimentales et fournir une reprise  

Lorsque vous utilisez des API expérimentales, assurez-vous de fournir une expérience d’utilisation à tous les visiteurs de votre site Web.  Les visiteurs ne pourront pas utiliser les navigateurs qui ne prennent pas en charge les API expérimentales que vous avez ajoutées à votre code.  De plus, si votre jeton expire avant de le renouveler, l’API expérimentale n’est plus disponible, ce qui peut entraîner des erreurs.  Pour éviter ce problème, assurez-vous de détecter les fonctionnalités disponibles dans votre navigateur.  Pour plus d’informations, reportez-vous à implémentation de la [détection de fonctionnalités][MDNImplementingFeatureDetection].

### Introduction aux origines autorisées  

Le portail essais d’origine Microsoft Edge ne prend en charge que les origines SSL, ce qui signifie que les sites Web doivent être implémentés de manière appropriée pour s’inscrire à une expérience.  À l’avenir, les origines sécurisées suivantes sont planifiées.  

*   Enregistrez-vous `http://localhost` comme origine de vos expériences.  Pour utiliser `http://localhost` la version actuelle, accédez à, `edge://flags` puis définissez l’expérience sur **activé**.  
*   Utiliser des extensions avec des `extensions://` origines prédéfinies pour s’inscrire à des expériences.  
    
<!-- links -->  

[DeveloperMicrsoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Microsoft Edge Origin-version d’évaluation console de développement | Documents Microsoft"  

[MDNImplementingFeatureDetection]: https://developer.mozilla.org/docs/learn/tools_and_testing/cross_browser_testing/feature_detection "Mise en œuvre de la détection de fonctionnalités | MDN"  
