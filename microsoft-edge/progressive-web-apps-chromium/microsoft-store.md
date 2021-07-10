---
description: Rendez votre PWA plus découvrable en publiant dans le Microsoft Store
title: Publier votre application web progressive sur le Microsoft Store
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: applications web progressives, PWA, Edge, Windows, Microsoft Store
ms.openlocfilehash: 40a6b94412a0788c87f7231025809098c98f18e9
ms.sourcegitcommit: 7cba715ef71cbac4ee0ebe8f07c0c0e4a2c64221
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11643248"
---
# <a name="publish-your-progressive-web-app-to-the-microsoft-store"></a>Publier votre application web progressive sur le Microsoft Store  

La publication de votre application web progressive \(PWA\) sur le [Microsoft Store][WindowsUwpPublishIndex] apporte les avantages suivants.  

:::row:::
   :::column span="1":::
      **Détectabilité**  
   :::column-end:::
   :::column span="2":::
      Les utilisateurs recherchent naturellement des applications dans l’App Store.  Lorsque vous publiez sur le Microsoft Store, des millions Windows utilisateurs peuvent découvrir vos PWA avec d’autres Windows applications.  Le Windows Store présente les applications par le biais de catégories, de collections organisées, etc.  Les portails de découverte d’applications offrent une expérience de navigation et d’achat facile pour les utilisateurs potentiels de votre application.  Vous pouvez même améliorer [votre liste dans][WindowsUwpPublishAppScreenshotsImages] le Store avec des captures d’écran, une image Hero et des bandes-annonces vidéo.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Trustiness**  
   :::column-end:::
   :::column span="2":::
      Windows clients savent qu’ils peuvent faire confiance à leurs achats Microsoft Store et téléchargements, car ils respectent les normes rigoureuses de qualité et [de sécurité de][LegalWindowsAgreementsStorePolicies]Microsoft.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Installation facile**  
   :::column-end:::
   :::column span="2":::
      Le Microsoft Store offre une expérience d’installation cohérente et conviviale dans [toutes les Windows 10 applications.][MicrosoftStoreAppsWindows]  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Analyse de l’application**  
   :::column-end:::
   :::column span="2":::
      Le [tableau Windows de l’Partner Center][WindowsUwpPublishIndex] vous fournit des analyses détaillées sur l’état, l’utilisation et bien plus encore de votre application. [][WindowsUwpPublishAnalytics]  
   :::column-end:::
:::row-end:::  

Pour publier votre PWA sur le Microsoft Store, aucune modification de code n’est requise.  Au lieu de cela, vous créez une réservation d’application, créez un package PWA et soumettez votre package au Store.  Les sections suivantes expliquent les étapes.   

## <a name="create-an-app-reservation"></a>Créer une réservation d’application  

[Windows’Partner Center][MicrosoftPartnerDashboardWindowsOverview] est le hub qui vous permet de soumettre votre application au Microsoft Store.  

Pour créer une réservation d’application, effectuer les actions suivantes.  

1.  Pour afficher vos programmes inscrits, effectuer les actions suivantes.  
    1.  Connectez-Windows l’Partner Center avec votre compte Microsoft et accédez au tableau de bord de [l’Centre partenaires.][MicrosoftPartnerDashboardHome]  
    1.  Accéder à **Windows & Xbox**  
        *   Si **Windows & Xbox** est affichée, votre application est déjà inscrite.  
        *   Si **Windows & Xbox** n’est pas affichée, choisissez Ajouter un **programme.**  
    
    :::image type="complex" source="./media/windows-partner-center-add-program.msft.png" alt-text="Ajouter un programme dans le tableau de bord Windows l’Partner Center" lightbox="./media/windows-partner-center-add-program.msft.png":::
       Ajouter un programme dans le tableau de bord Windows l’Partner Center
    :::image-end:::  
    
1.  Pour vous inscrire au programme pour les développeurs, effectuer les actions suivantes.  
    1.  Accédez à **Windows & Xbox**.  
    1.  Choose **Get started**.  
    1.  Suivez les instructions.  
1.  À présent, votre compte est inscrit au programme pour les développeurs d’applications. Pour créer une réservation d’application, effectuer les actions suivantes.  
    1.  Accédez à **Windows & Xbox**.  
    1.  Choose **Overview**  >  **Create a new app**.  
    1.  Tapez le nom de votre application dans l’invite.  
    1.  Choose `Reserve product name` .  
        
    :::image type="complex" source="./media/windows-partner-center-create-app.msft.png" alt-text="Créer une réservation d’application dans Windows’espace partenaires" lightbox="./media/windows-partner-center-create-app.msft.png":::
       Créer une réservation d’application dans Windows’espace partenaires  
    :::image-end:::  
    
1.  Pour afficher les détails de votre éditeur à utiliser dans la section Package de [votre PWA,](#package-your-pwa-for-the-store) choisissez **Product management**  >  **Product Identity**.  
    
    :::image type="complex" source="./media/windows-partner-center-publisher-info.msft.png" alt-text="Copier les informations de votre éditeur à partir Windows l’Partner Center" lightbox="./media/windows-partner-center-publisher-info.msft.png":::
       Copier les informations de votre éditeur à partir Windows l’Partner Center  
    :::image-end:::  
    
1.  Copiez et enregistrez les valeurs suivantes.  
    *   **Package ID**  
    *   **Publisher ID**  
    *   **Publisher Nom complet**  
        
## <a name="package-your-pwa-for-the-store"></a>Package de votre PWA pour le Store 

Maintenant que vous avez les informations de publication de votre application, générez un package Windows’application pour votre PWA.

Pour générer un package d’application, réalisez les actions suivantes.  

1.  Accédez [à PWA Générateur.][PwabuilderMain]  
1.  Tapez l’URL de votre PWA.  
1.  Choose **Start**  >  **Build My PWA**  >  **Windows**  >  **Options**.  
1.  Collez les valeurs suivantes que vous avez enregistrées dans la section Créer une réservation [d’application.](#create-an-app-reservation)  
    *   **Package ID**  
    *   **Publisher ID**  
    *   **Publisher Nom complet**  
        
    :::image type="complex" source="./media/pwabuilder-publisher-info.msft.png" alt-text="Coller des informations sur l’éditeur dans PWABuilder" lightbox="./media/pwabuilder-publisher-info.msft.png":::
       Coller des informations sur l’éditeur dans PWABuilder  
    :::image-end:::  
    
1.  Choisissez **Terminé**.  
1.  Pour télécharger votre package Windows’application, choisissez **Télécharger.**

Votre téléchargement est une `.zip` archive qui contient un fichier et un `.msixbundle` `.classic.appxbundle` fichier.  Les deux packages d’application permettent à votre PWA de s’exécuter sur un large éventail de versions Windows de l’application.  Pour plus d’informations, accédez à [Qu’est-ce qu’un package classique ?][GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd].  

### <a name="submit-your-app-package-to-the-store"></a>Soumettre votre package d’application au Store  

Pour soumettre votre application au Store, effectuer les actions suivantes.  

1.  Accédez à [Windows l’Partner Center][MicrosoftPartnerDashboardWindowsOverview] 
1.  Choisissez votre application.  
1.  Choisissez **Démarrer votre soumission.**  
    
    :::image type="complex" source="./media/windows-partner-center-start-submission.msft.png" alt-text="Démarrer une nouvelle soumission d’application sur Windows l’Partner Center" lightbox="./media/windows-partner-center-start-submission.msft.png":::
       Démarrer une nouvelle soumission d’application sur Windows l’Partner Center  
    :::image-end:::  
    
1.  Remplissez les invites suivantes pour obtenir des informations sur votre application.
    *   pricing  
    *   classification par âge  
    *   et plus  
        
1.  À **l’invite packages,** choisissez les fichiers que vous avez générés dans la `.msixbundle` `.classic.appxbundle` section [Packages PWA.](#package-your-pwa-for-the-store)  
    
Une fois votre soumission terminée, votre application est examinée, généralement dans un délai de 24 à 48 heures.  Une fois que vous avez reçu l’approbation, votre PWA est disponible dans le Microsoft Store.  

### <a name="measure-usage-of-your-store-installed-pwa"></a>Mesurer l’utilisation de vos PWA

Lors du lancement initial de votre PWA, si le PWA a été installé à partir de l’Microsoft Store, Microsoft Edge inclut l’en-tête suivant avec la demande de la première navigation de votre application `Referer` web.

```
Referer: app-info://platform/microsoft-store
```

Utilisez cette fonctionnalité pour mesurer le trafic distinct de votre PWA.  En fonction du trafic, vous pouvez ajuster le contenu de votre application pour améliorer l’expérience utilisateur.  Cette fonctionnalité est accessible au code client et au code serveur.

Cette fonctionnalité a été introduite dans Microsoft Edge version 91.

## <a name="see-also"></a>Voir également  

PWABuilder fournit plus de documentation pour vous aider à obtenir votre PWA dans la Microsoft Store.  

*   [Testez et soumettez votre package d PWA de messagerie un peu plus complet][GithubPwaBuilderPwabuilderWindowsChromiumDocsNextStepsMd]  
*   [Publier une nouvelle PWA dans le Store][GithubPwaBuilderPwabuilderWindowsChromiumDocsPublishNewAppMd]  
*   [Mettre à jour une application du Store existante vers une PWA][GithubPwaBuilderPwabuilderWindowsChromiumDocsUpdateExistingAppMd]  
*   [Recommandations en matière d’images pour les P PWA dans le Store][GithubPwaBuilderPwabuilderWindowsChromiumDocsImageRecommendationsMd]  
*   [Expliqueur de l’empaquetage d’application][GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd]  

<!-- links -->  

[LegalWindowsAgreementsStorePolicies]: /legal/windows/agreements/store-policies "Microsoft Store Stratégies | Documents Microsoft"  

[WindowsUwpPublishAnalytics]: /windows/uwp/publish/analytics "Analyser les performances de l'| Documents Microsoft"  
[WindowsUwpPublishAppScreenshotsImages]: /windows/uwp/publish/app-screenshots-and-images "Captures d’écran, images et bandes-annonces de l’application | Documents Microsoft"  
[WindowsUwpPublishIndex]: /windows/uwp/publish/index "Publier Windows applications et jeux | Documents Microsoft"  

[MicrosoftPartnerDashboardHome]: https://partner.microsoft.com/dashboard/home "Accueil | Microsoft Partner Center"  
[MicrosoftPartnerDashboardWindowsOverview]: https://partner.microsoft.com/dashboard/windows/overview "Ressources pour les partenaires | Microsoft Partner Center"  

[MicrosoftStoreAppsWindows]: https://www.microsoft.com/store/apps/windows "Windows Applications | Microsoft Store"  

[WindowsBlogWindowsdeveloperHostedAppModel]: https://blogs.windows.com/windowsdeveloper/hosted-app-model "Modèle d’application hébergée | Windows Blog du développeur"  

[GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/classic-package.md "Qu’est-ce qu’un package classique ? | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsImageRecommendationsMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/image-recommendations.md "Recommandations en matière d’image Windows PWA packages | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsNextStepsMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/next-steps.md "Étapes suivantes pour obtenir votre PWA dans la Microsoft Store | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsPublishNewAppMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/publish-new-app.md "Publier une nouvelle application dans le Store | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsUpdateExistingAppMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/update-existing-app.md "Mettre à jour une application existante dans le Store | GitHub"  

[PwabuilderMain]: https://www.pwabuilder.com "PWABuilder"  
