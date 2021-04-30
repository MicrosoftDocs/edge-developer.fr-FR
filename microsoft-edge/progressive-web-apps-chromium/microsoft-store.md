---
description: Rendre votre PWA plus découvrable en publiant dans le Microsoft Store
title: Publier votre application web progressive dans le Microsoft Store
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: applications web progressives, PWA, Edge, Windows, Microsoft Store
ms.openlocfilehash: 5e78e909187408566219ffe80779bb9221b585fa
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2021
ms.locfileid: "11527061"
---
# <a name="publish-your-progressive-web-app-to-the-microsoft-store"></a>Publier votre application web progressive sur le Microsoft Store  

La publication de votre application web progressive \(PWA\) dans le [Microsoft Store][WindowsUwpPublishIndex] offre les avantages suivants.  

:::row:::
   :::column span="1":::
      **Détectabilité**  
   :::column-end:::
   :::column span="2":::
      Les utilisateurs recherchent naturellement des applications dans l'App Store.  Lorsque vous publiez sur le Microsoft Store, des millions d'utilisateurs de Windows peuvent découvrir votre PWA avec d'autres applications Windows.  Le Windows Store présente les applications par le biais de catégories, de collections organisées et bien plus encore.  Les portails de découverte d'applications offrent une expérience de navigation et d'achat facile pour les utilisateurs potentiels de votre application.  Vous pouvez même améliorer [votre liste dans][WindowsUwpPublishAppScreenshotsImages] le Store avec des captures d'écran, une image Hero et des bandes-annonces vidéo.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Trustiness**  
   :::column-end:::
   :::column span="2":::
      Les clients Windows savent qu'ils peuvent faire confiance à leurs achats et téléchargements au Microsoft Store, car ils respectent les normes rigoureuses de qualité [et de sécurité de][LegalWindowsAgreementsStorePolicies]Microsoft.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Installation facile**  
   :::column-end:::
   :::column span="2":::
      Le Microsoft Store offre une expérience d'installation cohérente et conviviale dans toutes [les applications Windows 10.][MicrosoftStoreAppsWindows]  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Analyse de l'application**  
   :::column-end:::
   :::column span="2":::
      Le tableau de bord [][WindowsUwpPublishAnalytics] [de l'Centre][WindowsUwpPublishIndex] partenaires Windows vous fournit des analyses détaillées sur l'état, l'utilisation et bien plus encore de votre application.  
   :::column-end:::
:::row-end:::  

Pour publier votre PWA sur le Microsoft Store, aucune modification de code n'est requise.  Au lieu de cela, vous créez une réservation d'application, créez un package PWA et soumettez votre package au Store.  Les sections suivantes expliquent les étapes.   

## <a name="create-an-app-reservation"></a>Créer une réservation d'application  

[L'Partner Center Windows][MicrosoftPartnerDashboardWindowsOverview] est le hub qui vous permet de soumettre votre application au Microsoft Store.  

Pour créer une réservation d'application, effectuer les actions suivantes.  

1.  Pour afficher vos programmes inscrits, effectuer les actions suivantes.  
    1.  Connectez-vous à l'Partner Center Windows avec votre compte Microsoft et accédez au [tableau de bord de l'Centre partenaires.][MicrosoftPartnerDashboardHome]  
    1.  Accéder à **Windows & Xbox**  
        *   Si **Windows & Xbox** est affiché, votre application est déjà inscrite.  
        *   Si **Windows & Xbox** n'est pas affiché, choisissez Ajouter un **programme.**  
    
    :::image type="complex" source="./media/windows-partner-center-add-program.msft.png" alt-text="Ajouter un programme dans le tableau de bord de l'Centre de partenaires Windows" lightbox="./media/windows-partner-center-add-program.msft.png":::
       Ajouter un programme dans le tableau de bord de l'Centre de partenaires Windows
    :::image-end:::  
    
1.  Pour vous inscrire au programme pour les développeurs, effectuer les actions suivantes.  
    1.  Accédez **à Windows & Xbox**.  
    1.  Choose **Get started**.  
    1.  Suivez les instructions.  
1.  À présent, votre compte est inscrit au programme pour les développeurs d'applications. Pour créer une réservation d'application, effectuer les actions suivantes.  
    1.  Accédez **à Windows & Xbox**.  
    1.  Choose **Overview**  >  **Create a new app**.  
    1.  Tapez le nom de votre application dans l'invite.  
    1.  Choose `Reserve product name` .  
        
    :::image type="complex" source="./media/windows-partner-center-create-app.msft.png" alt-text="Créer une réservation d'application dans l'Espace partenaires Windows" lightbox="./media/windows-partner-center-create-app.msft.png":::
       Créer une réservation d'application dans l'Espace partenaires Windows  
    :::image-end:::  
    
1.  Pour afficher les détails de votre éditeur à utiliser dans la section [Package de votre PWA,](#package-your-pwa-for-the-store) choisissez **Product management**  >  **Product Identity**.  
    
    :::image type="complex" source="./media/windows-partner-center-publisher-info.msft.png" alt-text="Copier les informations de votre éditeur à partir de l'Centre de partenaires Windows" lightbox="./media/windows-partner-center-publisher-info.msft.png":::
       Copier les informations de votre éditeur à partir de l'Centre de partenaires Windows  
    :::image-end:::  
    
1.  Copiez et enregistrez les valeurs suivantes.  
    *   **Package ID**  
    *   **ID de l'éditeur**  
    *   **Nom complet de l'éditeur**  
        
## <a name="package-your-pwa-for-the-store"></a>Package de votre PWA pour le Store 

Maintenant que vous avez les informations de publication de votre application, générez un package d'application Windows pour votre application PWA.

Pour générer un package d'application, réalisez les actions suivantes.  

1.  Accédez au [Générateur PWA.][PwabuilderMain]  
1.  Tapez l'URL de votre PWA.  
1.  Choose **Start**  >  **Build My PWA**  >  **Windows**  >  **Options**.  
1.  Collez les valeurs suivantes que vous avez enregistrées dans la section Créer une réservation [d'application.](#create-an-app-reservation)  
    *   **Package ID**  
    *   **ID de l'éditeur**  
    *   **Nom complet de l'éditeur**  
        
    :::image type="complex" source="./media/pwabuilder-publisher-info.msft.png" alt-text="Coller des informations sur l'éditeur dans PWABuilder" lightbox="./media/pwabuilder-publisher-info.msft.png":::
       Coller des informations sur l'éditeur dans PWABuilder  
    :::image-end:::  
    
1.  Choisissez **Terminé**.  
1.  Pour télécharger votre package d'application Windows, choisissez **Télécharger.**

Votre téléchargement est une `.zip` archive qui contient un fichier et un `.msixbundle` `.classic.appxbundle` fichier.  Les deux packages d'application permettent à votre application PWA de s'exécuter sur un large éventail de versions de Windows.  Pour plus d'informations, accédez à [Qu'est-ce qu'un package classique][GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd]? .  

### <a name="submit-your-app-package-to-the-store"></a>Soumettre votre package d'application au Store  

Pour soumettre votre application au Store, effectuer les actions suivantes.  

1.  Accéder à [l'Centre partenaires Windows][MicrosoftPartnerDashboardWindowsOverview] 
1.  Choisissez votre application.  
1.  Choisissez **Démarrer votre soumission.**  
    
    :::image type="complex" source="./media/windows-partner-center-start-submission.msft.png" alt-text="Démarrer une soumission d'application sur l'Partner Center Windows" lightbox="./media/windows-partner-center-start-submission.msft.png":::
       Démarrer une soumission d'application sur l'Partner Center Windows  
    :::image-end:::  
    
1.  Remplissez les invites suivantes pour obtenir des informations sur votre application.
    *   pricing  
    *   classification par âge  
    *   et plus  
        
1.  À **l'invite packages,** choisissez les fichiers que vous avez générés dans la `.msixbundle` section Package de votre `.classic.appxbundle` [PWA.](#package-your-pwa-for-the-store)  
    
Une fois votre soumission terminée, votre application est examinée, généralement dans un délai de 24 à 48 heures.  Une fois que vous avez reçu l'approbation, votre PWA est disponible dans le Microsoft Store.  

## <a name="see-also"></a>Voir également  

PWABuilder fournit plus de documentation pour vous aider à obtenir votre PWA dans le Microsoft Store.  

*   [Tester et soumettre votre package d'application PWA][GithubPwaBuilderPwabuilderWindowsChromiumDocsNextStepsMd]  
*   [Publier un nouveau PWA dans le Store][GithubPwaBuilderPwabuilderWindowsChromiumDocsPublishNewAppMd]  
*   [Mettre à jour une application du Store existante vers une application PWA][GithubPwaBuilderPwabuilderWindowsChromiumDocsUpdateExistingAppMd]  
*   [Recommandations en matière d'images pour les P PWA dans le Store][GithubPwaBuilderPwabuilderWindowsChromiumDocsImageRecommendationsMd]  
*   [Expliqueur d'empaquetage d'application][GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd]  

<!-- links -->  

[LegalWindowsAgreementsStorePolicies]: /legal/windows/agreements/store-policies "Stratégies du Microsoft Store | Documents Microsoft"  

[WindowsUwpPublishAnalytics]: /windows/uwp/publish/analytics "Analyser les performances de l'| Documents Microsoft"  
[WindowsUwpPublishAppScreenshotsImages]: /windows/uwp/publish/app-screenshots-and-images "Captures d'écran, images et bandes-annonces de l'application | Documents Microsoft"  
[WindowsUwpPublishIndex]: /windows/uwp/publish/index "Publier des applications et des jeux Windows | Documents Microsoft"  

[MicrosoftPartnerDashboardHome]: https://partner.microsoft.com/dashboard/home "Accueil | Microsoft Partner Center"  
[MicrosoftPartnerDashboardWindowsOverview]: https://partner.microsoft.com/dashboard/windows/overview "Ressources pour les partenaires | Microsoft Partner Center"  

[MicrosoftStoreAppsWindows]: https://www.microsoft.com/store/apps/windows "Windows Apps | Microsoft Store"  

[WindowsBlogWindowsdeveloperHostedAppModel]: https://blogs.windows.com/windowsdeveloper/hosted-app-model "Modèle d'application hébergée | Blog des développeurs Windows"  

[GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/classic-package.md "Qu'est-ce qu'un package classique ? | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsImageRecommendationsMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/image-recommendations.md "Recommandations en matière d'image pour les packages Windows PWA | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsNextStepsMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/next-steps.md "Étapes suivantes pour l'obtention de votre PWA dans le Microsoft Store | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsPublishNewAppMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/publish-new-app.md "Publier une nouvelle application dans le Store | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsUpdateExistingAppMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/update-existing-app.md "Mettre à jour une application existante dans le Store | GitHub"  

[PwabuilderMain]: https://www.pwabuilder.com "PWABuilder"  
