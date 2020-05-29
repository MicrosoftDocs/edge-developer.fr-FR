---
description: Stratégies développeurs de catalogue Microsoft Edge addons.
title: Stratégies développeurs de catalogue Microsoft Edge addons
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/21/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-chrome, développement d’extensions, extensions de navigateur, compléments, Centre des partenaires, développeur
ms.openlocfilehash: be159491d892c176a8439393573dc23680fac377
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607432"
---
# Stratégies développeurs de catalogue Microsoft Edge addons  

## Introduction et objectif de ce document  

Merci de votre intérêt pour le développement d’extensions pour le catalogue des compléments Microsoft Edge.  Les stratégies de développeur de catalogue Microsoft Edge addons \ (extensions de développeur de catalogue de compléments) s’appliquent à vos extensions, y compris la soumission d’extensions par le biais du [Centre de partenariat][MicrosoftPartnerCenter] et la fourniture de telles extensions par le biais des modules complémentaires Microsoft Edge.  

## Exposés  

Quelques principes pour vous aider à commencer:  

*   Vous devez fournir des valeurs uniques et distinctes dans vos extensions pour Microsoft Edge.  Donnez une raison impérieuse de télécharger vos extensions à partir du catalogue Microsoft Edge addons (Microsoft Edge addons).  
*   Vous ne devez pas induire l’induire de l’induire des utilisateurs de votre poste, et ainsi de suite.  
*   Vous ne devez pas essayer de tricher les utilisateurs, le système ou l’écosystème.  Il n’y a pas d’endroit dans nos compléments Microsoft Edge pour toute nature de fraude. Évaluez les évaluations et les manipulations de cartes de crédit ou autres activités frauduleuses.  

Si vous adhérez à ces compléments, nous vous conseillons de créer des choix qui améliorent le recours et le public de votre extension.  

Vos extensions sont essentielles pour l’interface de centaines de millions d’utilisateurs.  Nous attendons d’avoir à vous présenter ce que vous créez et nous sommes ravis de vous aider à livrer vos extensions au monde.  

## 1. stratégies de produit  

### 1,1 fonction & valeur; Représentation précise  

Votre extension et les métadonnées associées doivent refléter précisément et clairement la source, les fonctionnalités et les fonctionnalités que vous décrivez.  

#### 1.1.1 les extensions doivent avoir un objectif unique  

Votre extension ne doit avoir qu’un objectif unique avec une fonctionnalité étroite.  

#### 1.1.2 décrire votre extension  

Tous les aspects de votre extension doivent décrire précisément les fonctions, les fonctionnalités et les limitations importantes de votre extension, y compris les périphériques d’entrée requis ou pris en charge.  La proposition de valeur de votre extension doit être claire lors de l’utilisation de la première exécution.  Votre extension n’utilise peut-être pas un nom ou une icône similaire à celle d’autres extensions, et ne doit pas prétendre à la représentation d’une entreprise, d’un organisme public ou d’une autre entité si vous n’êtes pas autorisé à le faire.  

#### fonction 1.1.3  

Votre extension doit être entièrement fonctionnelle.  

#### 1.1.4 recherche et découverte  

Les termes de recherche ne peuvent pas dépasser sept conditions d’utilisation uniques et devraient être pertinents pour votre extension.  

#### 1.1.5 fournissent des informations appropriées  

Vous devez fournir des informations distinctes et détaillées sur votre extension ainsi que les fonctionnalités de la liste \ (Metadata \) pour votre extension.  Votre extension doit fournir une qualité d’utilisation appréciable.  Votre extension doit également avoir une présence active dans les modules complémentaires Microsoft Edge.  

#### 1.1.6 stabilité et performances  

Votre extension ne doit pas avoir d’impact négatif sur les performances ou la stabilité de Microsoft Edge.  

#### brouillage 1.1.7  

Les extensions avec du code brouillé ne sont pas autorisées.  Il s’agit du code inclus dans le package d’extension ainsi que de tout code externe ou ressource extrait sur le Web.  Il est possible que vous deviez Refactoriser des parties de votre code s’il ne peut pas être consulté.  

#### 1.1.8 modification des paramètres du navigateur  

Votre extension ne doit **pas, sans le consentement**de l’utilisateur, modifier ou s’afficher pour modifier les paramètres du navigateur, y compris, mais sans s’y limiter: le moteur de recherche de la barre d’adresses et les suggestions, la page de démarrage ou la page d’accueil, la page de nouveau de l’onglet, et ajouter ou supprimer des favoris.  

Toute modification apporte aux paramètres du navigateur doit être documentée de manière explicite dans la description de l’extension.  

Votre extension n’est susceptible de réviser que les paramètres clés de remplacement d’une page Web ou d’un service Microsoft par le biais d’un moteur de recherche tiers (par exemple, l’utilisation d’un moteur de recherche tiers ou la définition de la page d’accueil sur une propriété Web tierce) si vous êtes employé ou associé à un tiers.  

### 1,2 sécurité  

Votre extension ne doit pas mettre en péril ou compromettre la sécurité de l’utilisateur, ou la sécurité ou la fonctionnalité de l’appareil, du système ou des systèmes associés.  

#### 1.2.1 stratégies de sécurité du contenu  

> [!NOTE]
> Si vous apportez des modifications à votre extension au-delà de la fonctionnalité décrite, toute modification apportée au code doit être conforme à la [stratégie de sécurité du contenu Microsoft Edge][MicrosoftEdgeContentSecurityPolicyRemoteScript].  Par exemple: votre extension ne doit pas télécharger un script distant et exécuter par la suite ce script d’une manière qui n’est pas cohérente avec la fonctionnalité décrite.  

#### 1.2.2 logiciel malveillant et indésirable  

Votre extension ne doit pas contenir ou activer un logiciel malveillant en vertu du critère Microsoft pour le [logiciel indésirable et malveillant][MicrosoftIdentifiesMalwareUnwantedApplications].  

#### 1.2.3 dépendance sur d’autres logiciels  

Votre extension risque de dépendre de logiciels non intégrés (par exemple, un autre produit, module ou service) pour fournir la principale fonctionnalité, à condition de divulguer la dépendance dans la description.  

#### 1.2.4 mise à jour des extensions  

Sauf si vous n’êtes pas autorisé par Microsoft, vos extensions doivent être mises à jour uniquement par le biais des modules complémentaires Microsoft Edge.  

### le produit 1,3 est testable  
L’extension doit être testable.  S’il n’est pas possible de tester votre extension pour quelque raison que ce soit, y compris, mais sans s’y limiter, les éléments ci-dessous, votre extension peut échouer.  

#### 1.3.1 informations d’identification de l’utilisateur  
Si votre extension nécessite des informations d’identification pour l’ouverture de session, spécifiez un compte de démonstration en utilisant le champ **Remarques pour la certification** .  

#### 1.3.2 disponibilité des services  

Si votre extension nécessite l’accès à un serveur, le serveur doit être opérationnel pour vérifier qu’elle fonctionne correctement.  

### 1,4 convivialité  

Votre extension doit respecter les normes du magasin d’extensions pour la convivialité, y compris, sans s’y limiter, celles indiquées dans les sous-sections ci-dessous.  

#### 1.4.1 compatibilité entre les plateformes  

Les extensions doivent être compatibles avec Microsoft Edge sur tous les appareils et plateformes sur lesquels ils peuvent être téléchargés.  Si une extension est téléchargée sur un appareil sur lequel elle n’est pas compatible, elle doit détecter au moment du lancement et afficher un message destiné à l’utilisateur en décrivant les exigences auxquelles les appareils doivent répondre afin d’être compatible avec votre extension.  

#### 1.4.2 utilisation de l’utilisateur  

L’extension doit être redémarrée rapidement et doit rester réactive aux entrées de l’utilisateur.  Les extensions doivent continuer à s’exécuter et rester réactive aux entrées de l’utilisateur.  Les extensions doivent s’arrêter harmonieusement et ne pas se fermer de manière inattendue.  L’extension doit gérer les exceptions et rester réactive aux entrées de l’utilisateur après le traitement de l’exception.  

### 1,5 informations personnelles  

Les conditions suivantes s’appliquent aux extensions qui accèdent aux informations personnelles.  Les informations personnelles incluent toutes les informations ou données qui identifient ou peuvent être utilisées pour identifier une personne ou qui est associée à des informations ou des données.  

#### 1.5.1 collecte des informations personnelles uniquement lorsque cela est nécessaire  

Votre extension risque de collecter, consulter, utiliser ou transmettre des informations personnelles (y compris les activités de navigation Web); uniquement s’il est requis uniquement pour une utilisation à des fins bien plus exposées.  

#### 1.5.2 Conservez une politique de confidentialité  

Même si votre extension accède à des informations personnelles, collecte ou transmet des informations personnelles; le cas échéant, vous devez fournir un avis et respecter la politique de confidentialité.  Votre politique de confidentialité doit informer les utilisateurs des informations personnelles consultées, collectées ou transmises par votre poste, de l’utilisation de ces informations, de leur stockage et de leur sécurité, et indiquent les types de parties à qui elles sont divulguées.  Votre politique de confidentialité doit décrire les contrôles utilisés par les utilisateurs sur l’utilisation et le partage de leurs informations, la façon dont ils accèdent à leurs informations, et il doit se conformer aux lois et réglementations en vigueur.  Votre politique de confidentialité doit être tenue à jour à mesure que vous ajoutez de nouvelles fonctionnalités à votre extension.  

Si vous fournissez à Microsoft votre politique de confidentialité, vous vous engagez à autoriser Microsoft à partager cette politique de confidentialité avec les utilisateurs de votre poste.  

#### 1.5.3 de partage de données avec des tiers  

Vous pouvez publier les informations personnelles des utilisateurs de votre poste sur un service externe ou une tierce partie par le biais de votre extension ou de métadonnées associées uniquement après avoir obtenu l’autorisation d’accès de ces utilisateurs.  Le consentement d’adhésion signifie que les utilisateurs accordent leur autorisation expresse dans l’interface utilisateur de votre extension pour l’activité demandée, après:  

*   Expliquez à vos utilisateurs comment les informations sont consultées, utilisées ou partagées et indiquent les types de parties auxquelles ils sont divulgués, et  
*   Fournissez à vos utilisateurs un mécanisme dans l’interface utilisateur de l’extension par le biais duquel ils ont la possibilité de les annuler et de les refuser.  

#### 1.5.4 les informations de partage d’autres utilisateurs  

Si vous publiez les informations personnelles d’une personne à un service externe ou tiers via votre extension ou les métadonnées, mais que la personne dont les informations sont partagées ne correspond pas à un utilisateur de votre extension;  

1.  Vous devez obtenir une autorisation écrite rapide pour publier ces informations personnelles.  
1.  Vous devez autoriser la personne dont les informations sont partagées pour retirer cette consentement à tout moment.  
1.  Votre politique de confidentialité doit indiquer clairement que vous pouvez collecter des informations personnelles de cette manière.  
1.  Le cas échéant, vous devez supprimer les informations personnelles de tout individu à la demande, y compris les personnes dont vous recueillez les informations.  
1.  Si votre extension fournit aux utilisateurs l’accès aux informations personnelles d’une autre personne, cette exigence s’applique également.  

#### 1.5.5 transmet des informations en toute sécurité  

Si votre extension recueille, stocke ou transmet des informations personnelles; Cela doit être sécurisé par le biais de méthodes de cryptographie modernes.  

#### 1.5.6 informations sensibles  

Votre extension ne doit pas collecter, stocker ou transmettre des informations personnelles sensibles, telles que des données médicales ou financières, à moins que ces informations ne soient liées à la fonctionnalité de votre extension.  Votre extension doit également être consentement de l’utilisateur dans le sens de la collecte, du stockage ou de la transmission de ces informations.  

### autorisations 1,6  

Votre extension doit uniquement demander les autorisations nécessaires au fonctionnement.  Vous devez fournir une description du fonctionnement de votre extension.  Votre extension doit être effectuée uniquement comme décrit.  Votre extension ne demande pas des autorisations pour les fonctionnalités qui dépassent les capacités nécessaires à l’exécution et à la fonction de déclaration.  

### localisation 1,7  

Vous devez localiser votre extension pour toutes les langues prises en charge par l’extension.  Le texte de la description de votre extension doit être localisé dans chaque langue que vous déclarez.  
Si votre extension est localisée de telle sorte que certaines fonctionnalités ne sont pas disponibles dans une version localisée, vous devez clairement indiquer ou afficher les limites de localisation dans la description de l’extension. L’interface fournie par une extension doit être raisonnablement similaire dans toutes les langues prises en charge.  

### 1,8 opérations financières  

Si votre produit inclut un achat dans le produit, des abonnements, une devise virtuelle, une fonctionnalité de facturation ou des informations financières; les exigences des sections suivantes s’appliquent.  

#### Fonctions payantes de 1.8.1  

Votre extension est susceptible de permettre aux utilisateurs d’utiliser le contenu numérique ou les services achetés via un mécanisme ou une API tiers d’achat.  

Vous devez utiliser une API d’achat tierce sécurisée pour les achats de produits ou services physiques.  Vous devez utiliser une API d’achat tiers sécurisée pour les paiements effectués dans le cadre de tout autre service, y compris les jeux de hasard ou les dons de niveau réel.  

*   Si votre extension est utilisée pour faciliter ou collecter des dons de bienfaisance ou pour diriger une loterie ou un concours promotionnel, vous devez le faire conformément à la loi en vigueur.  
*   Vous devez également indiquer clairement que Microsoft n’est pas la collecte de fonds ou le sponsor de la promotion.  
*   Les formules de produit vendues dans votre extension ne doivent pas être converties en devises légalement valides (par exemple, USD, euro, etc.) ou des produits ou services physiques.  

Les conditions suivantes s’appliquent à votre utilisation d’une API d’achat tierce sécurisée:  

*   À l’heure de la transaction ou lors de la collecte des informations de paiement ou financières de l’utilisateur; votre extension doit identifier le fournisseur de transaction commerciale, authentifier l’utilisateur et obtenir une confirmation de l’utilisateur pour la transaction.  Un fournisseur de transaction commerciale gère une plate-forme sécurisée pour les échanges financiers.  
*   Votre extension peut permettre aux utilisateurs d’enregistrer cette authentification, mais les utilisateurs doivent avoir la possibilité d’exiger une authentification lors de chaque transaction ou de les désactiver.  
*   Si votre extension recueille des informations de carte de crédit ou utilise un processeur de paiement tiers qui collecte les informations de carte de crédit, le traitement du paiement doit répondre à la norme de sécurité des données PCI actuelle (PCI DSS).  

#### 1.8.2 de la fermeture des fonctions payantes  

Votre extension et les métadonnées associées doivent fournir des informations sur les types d’achats en produits proposés et la gamme de tarifs.  Vous ne devez pas en induire en erreur les utilisateurs et vous devez avoir une clarté quant à la nature des promotions et des offres dans votre produit, y compris dans le cadre et les modalités des expériences d’évaluation.  Si votre extension restreint l’accès au contenu créé par l’utilisateur pendant ou après une période d’évaluation, vous devez avertir les utilisateurs à l’avance.  Par ailleurs, votre extension doit être claire pour les utilisateurs qu’ils initialisent une option d’achat dans l’extension.  

### notifications 1,9  

Votre extension doit respecter les paramètres système pour les notifications.  En d’autres termes, toute présentation des publicités et des notifications aux utilisateurs doit être cohérente avec les préférences de l’utilisateur, qu’il s’agisse de notifications fournies par le service de notifications par Microsoft (MPNS \), du service de notifications d’émission de Windows (WNS \) ou de tout autre service.  Si l’utilisateur désactive les notifications, de manière spécifique au produit ou à l’échelle du système, votre extension doit rester opérationnelle.  

Si votre produit utilise MPNS ou WNS pour transmettre les notifications, il doit respecter les exigences suivantes:  

#### Recommandations générales de 1.9.1  

Les notifications fournies par le biais de WNS ou MPNS sont considérées comme du contenu de produit et sont soumises à toutes les stratégies de développeur de catalogues addons.  

#### propriété 1.9.2 de notifications  

Vous ne devez pas masquer ou essayer de déguiser la source de toute notification lancée depuis votre extension.  

#### 1.9.3 informations confidentielles ou sensibles  

Vous ne devez pas inclure dans une notification les informations que les utilisateurs peuvent raisonnablement considérer comme confidentielles ou sensibles.  

#### 1.9.4 objet de notifications  

Les notifications envoyées à partir de votre extension doivent être associées à cette extension ou à d’autres extensions que vous publiez dans le catalogue Microsoft Edge addons et ne doivent pas inclure de messages publicitaires de tous types qui ne sont pas liés à vos extensions.  

### 1,10 et contenu publicitaire  

Pour toutes les activités publicitaires, les conditions suivantes s’appliquent:  

#### objectif 1.10.1  

Le contenu principal de votre extension ne doit pas être publicitaire et la publicité doit être clairement différenciée d’autres contenus de votre poste.  

#### politiques et accords de 1.10.2  

Tout contenu publicitaire affiché par votre extension doit respecter la [politique d’acceptation Microsoft Creative][MicrosoftAdvertisingCreativeAcceptancePolicies].  
Si votre extension affiche des publicités, tout le contenu affiché doit se conformer aux exigences publicitaires du [contrat du développeur][MicrosoftAppDeveloperAgreement] de l’application et de cette stratégie.  

#### 1.10.3 qualité de publicité  

*   L’objectif principal de votre extension ne doit pas être de faire en sorte que les utilisateurs cliquent sur ads.  
*   Votre extension ne doit pas faire d’action en cas d’interférence ou de diminution de la visibilité, de la valeur ou de la qualité des publicités affichées.  

#### Promotions 1.10.4  

Si vous achetez ou créez des campagnes publicitaires promotionnelles pour promouvoir vos extensions par le biais de la fonctionnalité de campagne de publicité dans le [Centre des partenaires][MicrosoftPartnerCenter], tous les éléments publicitaires que vous fournissez à Microsoft, y compris les pages de destination associées, doivent être conformes à la [politique de Microsoft Creative][MicrosoftAdvertisingCreativeSpecifications] et aux [politiques d’acceptation Microsoft Creative][MicrosoftAdvertisingCreativeAcceptancePolicies].  

#### 1.10.5 avertissant les utilisateurs de l’option refuser pour une publicité basée sur les intérêts  

La déclaration de confidentialité ou les conditions d’utilisation doivent faire savoir aux utilisateurs que vous envisagez d’envoyer des informations personnelles au fournisseur de services de publicité et que vous devez en informer les utilisateurs.  

#### recommandations en matière de 1.10.6  

Si votre extension s’adresse aux enfants de moins de 13 ans, tels que définis dans la [Loi de protection de la vie privée en ligne des enfants][FTCChildrensPrivacy]; vous devez informer Microsoft de ce fait dans le [Centre de partenariat][MicrosoftPartnerCenter] et veiller à ce que le contenu publicitaire affiché dans votre extension soit approprié pour les enfants de moins de 13 ans.  

## 2 stratégies de contenu  

Les stratégies suivantes s’appliquent au contenu et aux métadonnées (y compris le nom de l’éditeur, le nom de l’extension, l’icône de l’extension, la description de l’extension, les captures d’écran de l’extension et les miniatures de la remorque, ainsi que toute autre métadonnée d’extension \) proposée pour distribution dans les modules complémentaires Microsoft Edge.  Le contenu désigne les images, sons, vidéos et textes contenus dans l’extension, les vignettes, les notifications, les messages d’erreur ou les publicités exposées par le biais de votre extension, et tout ce qui est remis à partir d’un serveur ou auquel l’extension est connectée.  Étant donné que les extensions et les modules complémentaires Microsoft Edge sont utilisés partout dans le monde, ces exigences sont interprétées et appliquées dans le cadre des normes régionales et culturelles.  

### 2,1 requis pour le contenu de la liste des catalogues addon Microsoft Edge  

Les métadonnées et le contenu que vous envoyez pour joindre votre extension ne contiennent pas de contenu mûr.  
Les soumissions qui ne respectent pas les exigences relatives aux descriptions du Windows Store sont rejetées ou supprimées.  

### 2,2, xxx xxxxxxxxx xxxxxxxxx xxxxxxxxx  

Tout le contenu de votre extension et les métadonnées associées doivent être créés à l’origine par le biais d’un détenteur de droits tiers ou correctement sous licence et ne peuvent être utilisés que par le détenteur de droits ou conformément à la Loi.  

### 2,3 risques d’atteinte  

#### 2.3.1 Configuration requise  

Votre extension ne doit contenir aucun contenu destiné à faciliter ou glamorizes les activités réelles suivantes: \ (a \) une violence extrême ou gratuite; \ (b \) violations des droits relatifs à l’homme; \ (c) la création d’armes illégales; vous utilisez par le biais d’armes pour une personne, un animal ou une propriété réelle ou personnelle.  

#### 2.3.2 responsabilité  

Votre extension ne doit pas: \ (a \) poser un risque de sécurité, ni entraîner de blessures, de blessures ou tout autre dommage aux utilisateurs finaux ou à tout autre utilisateur ou animal; ou \ (b) présenter un risque ou engendrer l’endommagement d’une propriété réelle ou personnelle.  Vous êtes seul responsable de l’exécution des tests de sécurité des extensions, de l’acquisition des certificats et de l’implémentation de tout contrôle approprié.  Vous ne devez pas désactiver les fonctionnalités de sécurité et de confort de la plateforme, et vous devez inclure dans votre extension toutes les notifications, les avis et les exclusions de responsabilité applicables légalement requises.  

### 2,4 diffamatoire, diffamatoire, slanderous et menaçant  

Votre extension ne doit contenir aucun contenu diffamatoire, diffamatoire, slanderous ou menaçant.  

### 2,5 contenu choquant  

Votre extension et les métadonnées associées ne doivent pas contenir de contenu potentiellement sensible ou offensant.  Le contenu est considéré comme confidentiel ou offensant dans certains pays ou régions en raison de la législation locale ou des normes culturelles.  De plus, votre extension et les métadonnées associées ne doivent pas contenir de contenu qui préconise la discrimination, la haine ou la violence en fonction de considérations de race, d’origine, de religion, de langue, de sexe, d’âge, de handicap, de religion, d’orientation sexuelle, de statut de propriété ou d’appartenance à un autre groupe social.  

### 2,6 alcool, tabac et drogues  

Votre extension ne doit contenir aucun contenu destiné à faciliter ou glamorizes l’utilisation excessive ou irresponsiblee de produits alcooliques ou de tabac.  

### 2,7 pour adultes  

Votre extension ne doit pas contenir ou afficher du contenu qu’une personne raisonnable aurait pu considérer pornographie ou sexuellement explicite.  

### 2,8, XXXXXXXXX, xxx XXXXXXXXX, xxx xxxxxxxxx  

Votre extension doit respecter les conditions suivantes.  

*   Votre extension ne doit pas contenir de contenu ou fournir des services permettant de faciliter les jeux de hasard en ligne.  Les jeux de hasard en ligne incluent, sans s’y limiter, de casinos en ligne, de Paris, de loteries ou de jeux de compétences proposant des primes de trésorerie ou autres valeurs.  
*   Votre extension ne doit pas offrir un accès non autorisé au contenu du site Web, par exemple en cas de contournement de paywalls ou de restrictions de connexion.  
*   Votre extension ne doit pas fournir, encourager ou activer l’accès non autorisé, le téléchargement, le flux de contenu ou les éléments multimédias.  
*   Votre extension ne doit pas cryptocurrency.  

### 2,9 activité illégale  

Votre extension ne doit pas contenir de contenu ou de fonctionnalité qui encourage, favorise ou glamorizes une activité illégale dans le monde réel.  

### 2,10-blasphème excessif et contenu inapproprié  

*   Votre extension ne doit pas contenir de grossièretés excessives ou gratuites.  
*   Votre extension ne doit pas contenir ou afficher du contenu qu’une personne raisonnable estime obscène.  

### 2,11-spécificité du pays/de la région  

Le contenu choquant dans un pays ou une région où votre extension est ciblée n’est pas autorisé.  Le contenu risque d’être considéré comme offensif dans certains pays ou régions en raison de la législation locale ou des normes culturelles.  Vous trouverez ci-dessous des exemples de contenu potentiellement choquant dans certains pays/régions:  

**Chine**  

*   Contenu sexuel interdit  
*   Références de territoire ou de région en litige  
*   Accès à des contenus ou services illégaux conformément au droit local en vigueur  

### 2,12 classification par âge  

#### Contenu mûr 2.12.1  

Lorsque vous soumettrez votre extension au [Centre de partenariat][MicrosoftPartnerCenter], vous devez indiquer si votre extension affiche du contenu qui doit être marqué comme «mature».  Lorsque vous déterminez l’évaluation de votre extension, prenez en considération tout le contenu de votre application, y compris le contenu et les annonces générés par l’utilisateur, ainsi que le contenu lié par votre extension.  Si vous indiquez que votre extension ne contient pas de contenu «mature», vous êtes responsable de la conservation de l’exactitude de cette note.  Quelle que soit l’évaluation fournie avec votre extension, celle-ci doit toujours respecter toutes les exigences de contenu des stratégies de développeur Microsoft Edge addons  

#### Modification des évaluations 2.12.2  

Si votre extension fournit du contenu (par exemple, créé par l’utilisateur, commerciale ou autre contenu Web) qui peut être approprié pour une plus grande note d’âge que le classement affecté, vous devez demander aux utilisateurs d’accepter ce contenu à l’aide d’un filtre de contenu ou en vous connectant à l’aide d’un compte existant.  

### vidéos sur 2,13  

Si vous envoyez une vidéo promotionnelle dans la liste, elle doit suivre toutes les recommandations en matière de contenu mentionnées dans cette politique.  Si vous choisissez de fournir un lien YouTube, vous devez vous assurer que les publicités sont désactivées pour les vidéos spécifiques que vous voulez incorporer.  Pour plus d’informations sur le mode d’activation et de désactivation des publicités sur YouTube, voir [support.google.com/youtube/Answer/2531367?ref_topic=7072227][GoogleYoutubeAnswer2531367Topic7072227] et [support.google.com/youtube/Answer/132596][GoogleYoutubeAnswer132596].  

<!-- image links -->  

<!-- links -->  

[MicrosoftEdgeContentSecurityPolicyRemoteScript]: ./csp.md#relaxing-the-default-policy "Relaxer la stratégie par défaut-stratégie de sécurité du contenu \ (CSP \) | Documents Microsoft"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Contrat du développeur de l’application | Documents Microsoft"  
[MicrosoftIdentifiesMalwareUnwantedApplications]: /windows/security/threat-protection/intelligence/criteria "Comment Microsoft identifie les programmes malveillants et les applications potentiellement indésirables | Documents Microsoft"  

[GoogleYoutubeAnswer2531367Topic7072227]: https://support.google.com/youtube/answer/2531367?ref_topic=7072227 "Définir vos formats publicitaires par défaut-aide YouTube"  
[GoogleYoutubeAnswer132596]: https://support.google.com/youtube/answer/132596 "Publicités sur les vidéos incorporées-aide sur YouTube"  
[FTCChildrensPrivacy]: https://www.ftc.gov/tips-advice/business-center/privacy-and-security/children%27s-privacy "Vie privée des enfants-Federal Trade Commission"  

[MicrosoftAdvertisingCreativeAcceptancePolicies]: https://about.ads.microsoft.com/solutions/ad-products/display-advertising/creative-acceptance-policies "Politiques d’acceptation créative-Microsoft Advertising"  
[MicrosoftAdvertisingCreativeSpecifications]: https://about.ads.microsoft.com/solutions/ad-products/display-advertising/creative-specs "Spécifications créatives-Microsoft Advertising"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Centre de partenariat"  
