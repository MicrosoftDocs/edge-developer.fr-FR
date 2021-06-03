---
ms.assetid: ''
description: Testez en toute sécurité pendant une période fixe et fournissez des commentaires sur les nouvelles fonctionnalités de la plateforme.
title: Versions d’évaluation d’origine
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, développement web, html, css, essais d’origine, développeur
ms.openlocfilehash: cc03ec556d4b32ca37cebcd4ee7ba155bfe4404b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397544"
---
# <a name="use-origin-trials-in-microsoft-edge"></a>Utiliser les essais d’origine Microsoft Edge  

Les développeurs peuvent utiliser les essais origin pour tester des API expérimentales sur des sites en direct pendant une période limitée.  Lors de l’utilisation des essais originaux, les Microsoft Edge qui visitent votre site peuvent exécuter du code qui utilise des API expérimentales.  Pour accéder aux API expérimentales sur chaque ordinateur utilisateur, vous n’avez pas besoin d’activer et d’activer les `edge://flags` indicateurs de fonctionnalité.  Pour plus d’informations, accédez [aux API expérimentales.][DeveloperMicrsoftEdgeOriginTrials]  En outre, vous pouvez fournir des commentaires sur la conception de l’API, vos cas d’utilisation ou votre expérience d’utilisation des API aux ingénieurs de navigateur et à la communauté web standard.  

## <a name="get-started-using-origin-trials"></a>Commencer à utiliser les essais origin  

Pour plus d’informations sur les API expérimentales disponibles dans Microsoft Edge, accédez à Microsoft Edge Console du développeur des essais [Origin.][DeveloperMicrsoftEdgeOriginTrials]  Veillez à passer en revue la version minimale requise pour Microsoft Edge et la date de fin de la version d’évaluation pour évaluer la pertinence de l’utilisation des API expérimentales sur votre site web.  

> [!NOTE]
> Une expérience peut se terminer plus tôt que prévu si l’une des situations suivantes se produit.  
> *   Incident de sécurité majeur.  
> *   Si des commentaires suffisants sont collectés, cela indique qu’une nouvelle conception majeure est nécessaire pour répondre aux besoins des développeurs web.  
> Dans les deux cas, un e-mail de notification est envoyé à tous les développeurs actuellement inscrits à l’expérience.  

### <a name="register-for-a-trial-of-an-experimental-api"></a>S’inscrire à une version d’essai d’une API expérimentale  

Utilisez les étapes suivantes pour vous inscrire à une version d’essai d’une API expérimentale.  

1.  Visitez la page Microsoft Edge console du développeur [des essais Origin.][DeveloperMicrsoftEdgeOriginTrials]  
1.  Sélectionnez le bouton Enregistrer sur l’une des expériences disponibles.  
1.  Connectez-vous à la console du développeur à l’aide GitHub nom d’utilisateur et mot de passe.  
1.  Choose **Authorize MicrosoftEdge**.  
1.  Remplissez le formulaire.  
    
    > [!NOTE]
    > Pour inscrire un ou tous les sous-domaine, choisissez de définir `Do you need to match all subdomains for the provided origin?` le paramètre sur `Yes` .  Par exemple, `https://dev.contoso.com` est un domaine unique et utilise un caractère générique pour représenter tous les `https://*.contoso.com` sous-domaines.  
    
    > [!IMPORTANT]
    > Les formats d’origine suivants ne sont pas autorisés.  
    > *   Spécification d’un sous-foldeur sur l’origine.  Par exemple : `https://contoso.com/path/subfolder`  
    > 
    > *   Utilisation d’une origine avec des paramètres de chaîne de requête.  Par exemple : `https://contoso.com/path/feature?query_parameter=12345`  
    
1.  Choose **ACCEPT and REGISTER**.  
    
### <a name="apply-your-token"></a>Appliquer votre jeton  

Un jeton est généré instantanément et affiché sur la page Microsoft Edge console du développeur des essais [Origin.][DeveloperMicrsoftEdgeOriginTrials]  Pour commencer à utiliser la version d’essai sur votre site web, utilisez l’une des méthodes suivantes pour appliquer le jeton à votre page.  

*   Ajoutez `origin-trial` la valeur d’attribut et votre jeton à la `meta` balise sur chaque page qui utilise l’API expérimentale.  
    
    ```html
    <meta http-equiv="origin-trial" content="replace-with-your-token">
    ```  
    
*   `Origin-Trial`Ajoutez-le à l’en-tête de réponse HTTP de votre serveur.  
    
    ```json
    Origin-Trial: replace-with-your-token
    ```  
    
> [!NOTE]
> Votre jeton est valide pendant 6 semaines.  Avant la fin de votre version d’évaluation, des e-mails de rappel vous sont envoyés pour vous demander vos commentaires et vous demander de renouveler votre version d’évaluation avant l’expiration de votre jeton.  

### <a name="opt-out-of-an-experiment"></a>Refuser une expérience  

Pour refuser une expérience, utilisez l’une des méthodes suivantes pour supprimer votre jeton.  

*   Supprimez la `meta` balise de chaque page qui utilisait l’API expérimentale.  
    
    ```html
    <meta http-equiv="origin-trial" content="your-token">
    ```  
    
*   Supprimez `Origin-Trial` de l’en-tête de réponse HTTP de votre serveur.  
    
    ```json
    Origin-Trial: your-token
    ```  
    
### <a name="detect-experimental-features-and-provide-a-fallback"></a>Détecter les fonctionnalités expérimentales et fournir un modèle de retour  

Lorsque vous utilisez des API expérimentales, veillez à fournir une expérience de travail à tous les visiteurs de votre site web.  Les visiteurs peuvent utiliser des navigateurs qui ne peuvent pas prendre en charge les API expérimentales que vous avez ajoutées à votre code.  En outre, si votre jeton expire avant de le renouveler, l’API expérimentale n’est plus disponible, ce qui peut entraîner des erreurs.  Pour éviter cette situation, veillez à détecter les fonctionnalités disponibles dans votre navigateur.  Pour plus d’informations, accédez à [Implémenter la détection des fonctionnalités.][MDNImplementingFeatureDetection]

### <a name="roadmap-for-allowed-origins"></a>Feuille de route pour les origines autorisées  

Le Microsoft Edge d’essai Origin aujourd’hui prend uniquement en charge les origines activées SSL, ce qui signifie que le protocole HTTPS doit être correctement implémenté sur les sites web pour s’inscrire à une expérience.  À l’avenir, les origines sécurisées suivantes sont planifiées.  

*   `http://localhost`Inscrivez-vous comme origine de vos expériences.  Pour utiliser `http://localhost` aujourd’hui, `edge://flags` accédez à l’expérience et définissez-la **sur Activé.**  
*   Utilisez des extensions avec `extensions://` des origines préfixées pour vous inscrire à des expériences.  
    
<!-- links -->  

[DeveloperMicrsoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Microsoft Edge Console de développement Origin Trials | Documents Microsoft"  

[MDNImplementingFeatureDetection]: https://developer.mozilla.org/docs/learn/tools_and_testing/cross_browser_testing/feature_detection "Mise en œuvre des fonctionnalités de détection | MDN"  
