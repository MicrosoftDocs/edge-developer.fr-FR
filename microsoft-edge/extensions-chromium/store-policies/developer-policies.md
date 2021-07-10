---
description: Stratégies de développement du magasin des extensions Microsoft Edge
title: Stratégies de développement du magasin des extensions Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, développement d’extensions, extensions de navigateur, addons, centre de partenaires, développeur
ms.openlocfilehash: 8b3e537752e1f5e891626f8cd28cb89806295166
ms.sourcegitcommit: 8f37c931ecde4d58223113f7e3b42d37cc3df97f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/10/2021
ms.locfileid: "11643426"
---
# <a name="microsoft-edge-add-ons-store-developer-policies"></a>Stratégies de développement du magasin des extensions Microsoft Edge  

## <a name="introduction-and-objective-of-this-document"></a>Introduction et objectif de ce document  

Nous vous remercions de votre intérêt pour le développement d’extensions pour Microsoft Edge magasin de modules.  Les stratégies de développeur du magasin Microsoft Edge add-ons \(Add-ons store developer policies\) s’appliquent à vos extensions, y compris votre soumission d’extensions par le biais de l’Partner [Center][MicrosoftPartnerCenter] et la mise en service de ces extensions via les extensions Microsoft Edge.  

## <a name="principles"></a>Principes  

Quelques principes pour vous aider à démarrer :  

*   Vous devez offrir une valeur unique et distincte au sein de vos extensions pour Microsoft Edge.  Fournissez une raison intéressante pour télécharger vos extensions à partir du Microsoft Edge de modules Microsoft Edge\).  
*   Vous ne devez pas induire en erreur nos utilisateurs communs concernant les actions de votre extension, les personnes qui l’offrent, etc.  
*   Vous ne devez pas essayer de insérer les utilisateurs, le système ou l’écosystème.  Il n’y a aucune place dans nos modules Microsoft Edge pour tout type de fraude ; que ce soit la manipulation des évaluations et des révisions, la fraude par carte de crédit ou toute autre activité frauduleuse.  
    
Le respect des stratégies de développement Microsoft Edge du magasin de modules Microsoft Edge vous permet de faire des choix qui améliorent l’appel et le public de votre extension.  

Vos extensions sont essentielles à l’expérience de centaines de millions d’utilisateurs.  Nous avons le plaisir de découvrir ce que vous créez et sommes ravis de vous aider à fournir vos extensions au monde entier.  

## <a name="1-product-policies"></a>1. Stratégies de produit  

### <a name="11-distinct-function--value-accurate-representation"></a>1.1 Fonction distincte & valeur ; Représentation précise  

Votre extension et les métadonnées associées doivent refléter précisément et clairement la source, les fonctionnalités et les fonctionnalités que vous décrivez.  

#### <a name="111-extensions-must-have-a-single-purpose"></a>1.1.1 Les extensions doivent avoir un seul objectif  

Votre extension doit avoir un seul objectif avec une fonctionnalité étroite.  

#### <a name="112-describe-your-extension"></a>1.1.2 Décrire votre extension  

Tous les aspects de votre extension doivent décrire avec précision les fonctions, fonctionnalités et limitations importantes de votre extension, y compris les périphériques d’entrée requis ou pris en charge.  La proposition de valeur de votre extension doit être claire lors de la première utilisation.  Votre extension peut ne pas utiliser un nom ou une icône similaire à celui d’autres extensions et ne doit pas revendiquer la représentation d’une société, d’un organisme public ou d’une autre entité si vous n’êtes pas autorisé à effectuer cette représentation.  

#### <a name="113-functionality"></a>1.1.3 Fonctionnalité  

Votre extension doit être entièrement fonctionnelle.  

#### <a name="114-search-and-discovery"></a>1.1.4 Recherche et découverte  

Les termes de recherche ne peuvent pas dépasser sept termes uniques et doivent être pertinents pour votre extension.  

#### <a name="115-provide-appropriate-details"></a>1.1.5 Fournir les détails appropriés  

Vous devez fournir des détails distincts et informatifs sur votre extension et la fonctionnalité de description \(metadata\) de votre extension.  Votre extension doit fournir une expérience utilisateur précieuse et de qualité.  Votre extension doit également avoir une présence active dans Microsoft Edge modules.  

#### <a name="116-stability-and-performance"></a>1.1.6 Stabilité et performances  

Votre extension ne doit pas avoir d’impact négatif sur les performances ou la stabilité des Microsoft Edge.  

#### <a name="117-obfuscation"></a>1.1.7 Obfuscation  

Les extensions avec du code obscurci ne sont pas autorisées.  Cela inclut le code dans votre package d’extension, ainsi que tout code externe ou ressource récupéré à partir du web.  Vous pouvez être invité à refactoriser des parties de votre code s’il n’est pas reviewable.  

#### <a name="118-altering-browser-settings"></a>1.1.8 Modification de la Paramètres  

Votre extension ne doit pas, sans le consentement de l’utilisateur approprié, modifier ou sembler modifier les fonctionnalités ou paramètres du navigateur, y compris, mais sans s’y limiter : le fournisseur de recherche et les suggestions de la barre d’adresses, la page de démarrage ou d’accueil, la page nouvel onglet et l’ajout ou la suppression du favori.  

Toute modification apportée aux paramètres du navigateur doit être explicitement documentée dans la description de votre extension.  

Votre extension peut uniquement réviser les paramètres clés pour remplacer une page web ou un service Microsoft par celui d’un tiers \(par exemple, exiger l’utilisation d’un moteur de recherche tiers ou définir la page d’accueil sur une propriété web tierce\) si vous êtes employé par ou autrement associé à un tel tiers.  

### <a name="12-security"></a>1.2 Sécurité  

Votre extension ne doit pas mettre en danger ou compromettre la sécurité des utilisateurs, ni la sécurité ou les fonctionnalités de l’appareil, du système ou des systèmes associés.  

#### <a name="121-content-security-policies"></a>1.2.1 Stratégies de sécurité du contenu  

> [!NOTE]
> Si vous a apporté des modifications à votre extension au-delà de la fonctionnalité décrite, toutes les modifications apportées au code doivent être conformes à la stratégie de sécurité [Microsoft Edge contenu .][MicrosoftEdgeContentSecurityPolicyRemoteScript]  Par exemple, votre extension ne doit pas télécharger un script distant et exécuter ce script d’une manière qui n’est pas cohérente avec la fonctionnalité décrite.  

#### <a name="122-unwanted-and-malicious-software"></a>1.2.2 Logiciels indésirables et malveillants  

Votre extension ne doit pas contenir ou activer les programmes malveillants tels que définis par les critères De Microsoft pour [les logiciels indésirables et malveillants][MicrosoftIdentifiesMalwareUnwantedApplications].  

#### <a name="123-dependency-on-other-software"></a>1.2.3 Dépendance à d’autres logiciels  

Votre extension peut dépendre de logiciels non intégrés \(par exemple, un autre produit, module ou service\) pour fournir la fonctionnalité principale, à condition que vous divulguiez la dépendance dans la description  

#### <a name="124-extensions-update"></a>1.2.4 Extensions Update  

Sauf autorisation contraire de Microsoft, vos extensions doivent être mises à jour uniquement Microsoft Edge modules.  

### <a name="13-product-is-testable"></a>1.3 Le produit peut être testé  

Votre extension doit être testable.  S’il n’est pas possible de tester votre extension pour une raison quelconque, y compris, mais sans s’y limiter, les éléments ci-dessous, votre extension peut échouer à cette exigence.  

#### <a name="131-user-credentials"></a>1.3.1 Informations d’identification de l’utilisateur  

Si votre extension nécessite des informations d’identification de connexion, fournissez un compte de démonstration de travail à l’aide du `Notes for certification` champ.  

#### <a name="132-availability-of-services"></a>1.3.2 Disponibilité des services  

Si votre extension nécessite un accès à un serveur, le serveur doit être fonctionnel pour vérifier qu’il fonctionne correctement.  

### <a name="14-usability"></a>1.4 Utilisation  

Votre extension doit respecter les Microsoft Edge du magasin d’extensions pour des raisons d’utilisation, y compris, mais sans s’y limiter, celles répertoriées dans les sous-sections ci-dessous.  

#### <a name="141-compatibility-across-platforms"></a>1.4.1 Compatibilité entre les plateformes  

Votre extension doit être compatible avec Microsoft Edge sur tous les appareils et plateformes sur lesquels ils peuvent être téléchargés.  Si une extension est téléchargée sur un appareil avec lequel elle n’est pas compatible, elle doit détecter cela au lancement et afficher un message à l’utilisateur détaillant les exigences que les appareils doivent respecter pour être compatibles avec votre extension.  

#### <a name="142-user-experience"></a>1.4.2 Expérience utilisateur  

Votre extension doit démarrer rapidement et doit rester réactive aux entrées de l’utilisateur.  Votre extension doit continuer à s’exécuter et rester réactive aux entrées de l’utilisateur.  Votre extension doit s’arrêter normalement et ne pas se fermer de manière inattendue.  Votre extension doit gérer les exceptions et rester réactive aux entrées de l’utilisateur une fois l’exception gérée.  

### <a name="15-personal-information"></a>1.5 Informations personnelles  

Les conditions suivantes s’appliquent aux extensions qui accèdent aux informations personnelles.  Les informations personnelles incluent toutes les informations ou données qui identifient ou peuvent être utilisées pour identifier une personne, ou qui sont associées à ces informations ou données.  

#### <a name="151-collect-personal-information-only-when-necessary"></a>1.5.1 Collecter des informations personnelles uniquement si nécessaire  

Votre extension peut collecter, consulter, utiliser ou transmettre des informations personnelles \(y compris l’activité de navigation web\) ; uniquement s’il est requis par et uniquement pour une utilisation dans une fonctionnalité visiblement divulguée par l’utilisateur.  

#### <a name="152-maintain-a-privacy-policy"></a>1.5.2 Maintenir une politique de confidentialité  

Que votre extension accède, collecte ou transmette des informations personnelles ; vous devez fournir une notification importante et vous conformer à votre politique de confidentialité si la loi l’exige.  Votre politique de confidentialité doit informer les utilisateurs des informations personnelles accessibles, collectées ou transmises par votre poste, de la façon dont ces informations sont utilisées, stockées et sécurisées, et d’indiquer les types de parties à qui elles sont divulguées.  Votre politique de confidentialité doit décrire les contrôles que les utilisateurs ont sur l’utilisation et le partage de leurs informations, la façon dont ils accèdent à leurs informations, et elle doit respecter les lois et réglementations applicables.  Votre politique de confidentialité doit être tenue à jour lorsque vous ajoutez de nouvelles fonctionnalités à votre extension.  

Si vous fournissez à Microsoft votre politique de confidentialité, vous acceptez d’autoriser Microsoft à partager cette politique de confidentialité avec les utilisateurs de votre extension.  

#### <a name="153-sharing-data-with-third-parties"></a>1.5.3 Partage de données avec des tiers  

Vous pouvez publier les informations personnelles des utilisateurs de votre extension sur un service externe ou tiers via votre extension ou les métadonnées associées uniquement après avoir obtenu le consentement de ces utilisateurs.  Le consentement de l’utilisateur signifie que les utilisateurs donnent leur autorisation express dans l’interface utilisateur de votre extension pour l’activité demandée, après que vous :  

*   Décrire à vos utilisateurs comment les informations sont accessibles, utilisées ou partagées, et indiquer les types de parties à qui elles sont divulguées, et  
*   Fournissez à vos utilisateurs un mécanisme dans votre interface utilisateur d’extension par le biais duquel ils ont la possibilité d’annuler ultérieurement l’autorisation et de refuser.  
    
#### <a name="154-sharing-information-of-non-users"></a>1.5.4 Partage d’informations d’utilisateurs non-utilisateurs  

Si vous publiez les informations personnelles d’une personne à un service externe ou tiers via votre extension ou les métadonnées, mais que la personne dont les informations sont partagées n’est pas un utilisateur de votre extension ;  

1.  Vous devez obtenir le consentement écrit express pour publier ces informations personnelles.  
1.  Vous devez autoriser la personne dont les informations sont partagées à retirer ce consentement à tout moment.  
1.  Votre politique de confidentialité doit clairement divulguer que vous pouvez collecter des informations personnelles de cette manière.  
1.  Si la loi applicable l’exige, vous devez supprimer les informations personnelles de toute personne sur demande, y compris les personnes dont vous collectez les informations de cette manière.  
1.  Si votre extension permet aux utilisateurs d’accéder aux informations personnelles d’une autre personne, cette exigence s’applique également.  
    
#### <a name="155-transmit-information-securely"></a>1.5.5 Transmettre des informations en toute sécurité  

Si votre extension collecte, stocke ou transmet des informations personnelles ; Il doit le faire en toute sécurité à l’aide de méthodes de chiffrement modernes.  

#### <a name="156-highly-sensitive-information"></a>1.5.6 Informations hautement sensibles  

Votre extension ne doit pas collecter, stocker ou transmettre des informations personnelles hautement sensibles, telles que des données de santé ou financières, sauf si elles sont liées aux fonctionnalités de votre extension.  Votre extension doit également obtenir le consentement de l’utilisateur express avant de collecter, stocker ou transmettre ces informations.  

### <a name="16-permissions"></a>1.6 Autorisations  

Votre extension doit uniquement demander les autorisations nécessaires au fonctionnement.  Vous devez fournir une description du fonctionnement de votre extension.  Votre extension doit uniquement être exécutée comme décrit.  Il se peut que votre extension ne demande pas d’autorisation pour les fonctionnalités qui vont au-delà des fonctionnalités requises pour fonctionner comme déclaré.  

### <a name="17-localization"></a>1.7 Localisation  

Vous devez trouver votre extension pour toutes les langues que votre extension prétend prendre en charge.  Le texte de la description de votre extension doit être localisée dans chaque langue que vous déclarez.  
Si votre extension est localisée de sorte que certaines fonctionnalités ne soient pas disponibles dans une version localisée, vous devez clairement faire état ou afficher les limites de localisation dans la description de votre extension. L’expérience fournie par une extension doit être assez similaire dans toutes les langues qu’elle prend en charge.  

### <a name="18-financial-transactions"></a>1.8 Transactions financières  

Si votre produit inclut des achats in-product, des abonnements, une devise virtuelle, des fonctionnalités de facturation ou capture des informations financières ; les conditions requises dans les sections suivantes s’appliquent.  

#### <a name="181-paid-features"></a>1.8.1 Fonctionnalités payantes  

Votre extension peut permettre aux utilisateurs de consommer du contenu numérique ou des services achetés via un mécanisme d’achat tiers ou une API.  

Vous devez utiliser une API d’achat tierce sécurisée pour les achats de biens physiques ou de services.  Vous devez utiliser une API d’achat tierce sécurisée pour les paiements effectués dans le cadre de tout autre service, y compris les dons de jeux ou de dons réels.  

*   Si votre poste est utilisé pour faciliter ou collecter des contributions ou pour effectuer un bal promotionnel ou un prix, vous devez le faire conformément à la loi applicable.  
*   Vous devez également clairement faire savoir que Microsoft n’est pas le soutien ou le sponsor de la promotion.  
*   Les offres dans le produit vendues dans votre extension ne doivent pas être converties en devise valide légalement \(par exemple, USD, Euro, etc.) ou en biens physiques ou services.  
    
Les conditions suivantes s’appliquent à votre utilisation d’une API d’achat tiers sécurisée :  

*   Au moment de la transaction ou lorsque vous collectez des informations financières ou de paiement auprès de l’utilisateur ; votre extension doit identifier le fournisseur de transactions commerciales, authentifier l’utilisateur et obtenir la confirmation de l’utilisateur pour la transaction.  Un fournisseur de transactions commerciales maintient une plateforme sécurisée pour les échanges financiers.  
*   Votre extension peut offrir aux utilisateurs la possibilité d’enregistrer cette authentification, mais les utilisateurs doivent avoir la possibilité d’exiger une authentification sur chaque transaction ou de désactiver les transactions dans le produit.  
*   Si votre poste collecte des informations de carte de crédit ou utilise un processeur de paiement tiers qui collecte des informations de carte de crédit, le traitement des paiements doit respecter la norme PCI de sécurité des données \(PCI DSS\).  
    
#### <a name="182-disclosing-paid-features"></a>1.8.2 Divulgation des fonctionnalités payantes  

Votre extension et les métadonnées associées doivent fournir des informations sur les types d’achats in-product proposés et la plage de prix.  Vous ne devez pas induire en erreur les utilisateurs et être clair sur la nature de vos offres et promotions in-product, y compris l’étendue et les conditions des expériences d’essai.  Si votre extension limite l’accès au contenu créé par l’utilisateur pendant ou après une version d’essai, vous devez en informer les utilisateurs à l’avance.  En outre, votre extension doit clairement faire savoir aux utilisateurs qu’ils lancent une option d’achat dans votre extension.  

### <a name="19-notifications"></a>1.9 Notifications  

Votre extension doit respecter les paramètres système pour les notifications.  Cela signifie que toute présentation de publicités et de notifications aux utilisateurs doit être cohérente avec les préférences de l’utilisateur, que les notifications soient fournies par le service de notification push de Microsoft \(MPNS\), Windows Push Notification Service \(WNS\) ou tout autre service.  Si l’utilisateur désactive les notifications, que ce soit pour un produit spécifique ou à l’échelle du système, votre extension doit rester fonctionnelle.  

Si votre produit utilise MPNS ou WNS pour transmettre des notifications, il doit respecter les exigences suivantes :  

#### <a name="191-general-guidance"></a>1.9.1 Recommandations générales  

Les notifications fournies par le biais de WNS ou MPNS sont considérées comme du contenu de produit et sont soumises à toutes les stratégies de développement du catalogue de modules ajoutes.  

#### <a name="192-ownership-of-notifications"></a>1.9.2 Propriété des notifications  

Vous ne devez pas masquer ou essayer de masquer la source d’une notification lancée à partir de votre extension.  

#### <a name="193-no-confidential-or-sensitive-information"></a>1.9.3 Aucune information confidentielle ou sensible  

Vous ne devez pas inclure dans une notification des informations que les utilisateurs peuvent raisonnablement considérer comme confidentielles ou sensibles.  

#### <a name="194-purpose-of-notifications"></a>1.9.4 Objectif des notifications  

Les notifications envoyées à partir de votre extension doivent être liées à cette extension ou à d’autres extensions que vous publiez dans le magasin d’extensions Microsoft Edge et ne doivent pas inclure de messages promotionnels d’un type quelconque qui n’est pas lié à vos extensions.  

### <a name="110-advertising-conduct-and-content"></a>1.10 Conduite et contenu publicitaire  

Pour toutes les activités publicitaires, les conditions suivantes s’appliquent :  

#### <a name="1101-purpose"></a>1.10.1 Objectif  

Le contenu principal de votre extension ne doit pas être une publicité, et la publicité doit être clairement distinguer des autres contenus de votre extension.  

#### <a name="1102-policies-and-agreements"></a>1.10.2 Stratégies et accords  

Tout contenu publicitaire affiché par votre extension doit respecter la politique [d’acceptation créative de Microsoft.][MicrosoftAdvertisingCreativeAcceptancePolicies]  
Si votre extension affiche des publicités, tout le contenu [][MicrosoftAppDeveloperAgreement] affiché doit être conforme aux exigences publicitaires du Contrat du développeur d’applications et de la présente stratégie.  

#### <a name="1103-quality-of-advertising"></a>1.10.3 Qualité de la publicité  

*   L’objectif principal de votre extension ne doit pas être d’obtenir des utilisateurs qu’ils cliquent sur des publicités.  
*   Votre extension ne doit rien faire qui interfère avec ou diminue la visibilité, la valeur ou la qualité des publicités qu’elle affiche.  

#### <a name="1104-promotions"></a>1.10.4 Promotions  

Si vous achetez ou créez des campagnes publicitaires pour promouvoir vos extensions par le biais de la fonctionnalité de campagne publicitaire de l’Espace [partenaires,][MicrosoftPartnerCenter]tous les supports publicitaires que vous fournissez à Microsoft, y compris les pages d’accueil associées, doivent être conformes à la stratégie de [spécifications créatives][MicrosoftAdvertisingCreativeSpecifications] de Microsoft et à la stratégie d’acceptation créative [de Microsoft.][MicrosoftAdvertisingCreativeAcceptancePolicies]  

#### <a name="1105-notifying-users-of-opt-out-for-interest-based-advertising"></a>1.10.5 Avertir les utilisateurs de la Opt-Out publicité Interest-Based publicité  

Votre déclaration de confidentialité ou vos conditions d’utilisation doivent informer les utilisateurs que vous envisagez d’envoyer des informations personnelles au fournisseur de services publicitaires et indiquer aux utilisateurs comment ils peuvent refuser les publicités basées sur les intérêts.  

#### <a name="1106-other-guidelines"></a>1.10.6 Autres recommandations  

Si votre extension s’adresse aux enfants de moins de 13 ans, comme défini dans la [children’s Online Privacy Protection Act][FTCChildrensPrivacy]; vous devez informer Microsoft de ce fait dans l’Partner [Center][MicrosoftPartnerCenter] et vous assurer que tout le contenu de la annonce affiché dans votre extension est approprié pour les enfants de moins de 13 ans.  

## <a name="2-content-policies"></a>2 Stratégies de contenu  

Les stratégies suivantes s’appliquent au contenu et aux métadonnées \(y compris le nom de l’éditeur, le nom de l’extension, l’icône d’extension, la description de l’extension, les captures d’écran d’extension, les bandes-annonces d’extension et les miniatures de bande-annonce, et toutes les autres métadonnées d’extension\) proposées pour la distribution dans les extensions Microsoft Edge.  Le contenu signifie les images, les sons, les vidéos et le texte contenus dans votre extension, les vignettes, les notifications, les messages d’erreur ou les publicités exposés via votre extension, et tout ce qui est remis à partir d’un serveur ou auquel votre extension se connecte.  Étant donné que les extensions et Microsoft Edge extensions sont utilisées dans le monde entier, ces exigences sont interprétées et appliquées dans le contexte de normes régionales et culturelles.  

### <a name="21-content-requirements-for-microsoft-edge-addon-catalog-listing"></a>2.1 Exigences de contenu pour la Microsoft Edge catalogue d’ajouts  

Les métadonnées et autres contenus que vous envoyez pour accompagner votre extension peuvent ne pas contenir de contenu mature.  
Les soumissions qui ne répondent pas Microsoft Edge conditions requises pour les listes de la boutique d’modules supplémentaires sont rejetées ou supprimées rapidement.  

### <a name="22-content-including-names-logos-original-and-third-party"></a>2.2 Contenu incluant les noms, les logos, l’original et le tiers  

Tout le contenu de votre extension et des métadonnées associées doit être créé à l’origine par le titulaire d’une licence tierce ou sous licence appropriée et ne doit être utilisé que comme autorisé par le titulaire des droits ou comme autorisé par la loi.  

### <a name="23-risk-of-harm"></a>2.3 Risque de dommages  

#### <a name="231-requirements"></a>2.3.1 Conditions requises  

Votre extension ne doit pas contenir de contenu qui facilite ou favorise les activités du monde réel suivantes : \(a\) violence extrême ou gratuite ; \(b\) violations des droits de l’homme ; \(c\) la création d’armes illégales ; ou \(d\) l’utilisation d’armes contre une personne, un animaux ou une propriété réelle ou personnelle.  

#### <a name="232-responsibility"></a>2.3.2 Responsabilité  

Votre extension ne doit pas : \(a\) poser un risque de sécurité pour, ni entraîner une gêne, une gêne ou tout autre dommage pour les utilisateurs finaux ou toute autre personne ou enfant ; ou \(b\) posent un risque d’endommagement de propriétés réelles ou personnelles ou en entraînent.  Vous êtes le seul responsable de tous les tests de sécurité des extensions, de l’acquisition de certificats et de l’implémentation de toutes les protections de fonctionnalités appropriées.  Vous ne devez pas désactiver les fonctionnalités de sécurité ou de confort de la plateforme et vous devez inclure tous les avertissements, notifications et clauses d’exclusion de responsabilité juridiquement requis et standard applicables dans votre extension.  

### <a name="24-defamatory-libelous-slanderous-and-threatening"></a>2.4 Diffamante, caâmeuse, caculeuse et répante  

Votre extension ne doit pas contenir de contenu diffamant, caculant, caculant ou dangereux.  

### <a name="25-offensive-content"></a>2.5 Contenu choquant  

Votre extension et les métadonnées associées ne doivent pas contenir de contenu potentiellement sensible ou choquant.  Le contenu peut être considéré comme sensible ou choquant dans certains pays/régions en raison des lois locales ou des normes culturelles.  En outre, votre extension et les métadonnées associées ne doivent pas contenir de contenu qui fait la défense de la discrimination, de la violence ou de la violence en fonction des considérations de la course, de l’appartenance à un groupe social, de l’origine nationale, de la langue, du sexe, de l’âge, du handicap, de l’orientation sexuelle, de l’état en tant que travailleur ou de l’appartenance à un autre groupe social.  

### <a name="26-alcohol-tobacco-and-drugs"></a>2.6 Consommation, consommation d’enfants et enfants  

Votre extension ne doit pas contenir de contenu qui facilite ou favorise l’utilisation excessive ou dangereuse de l’antériorisation, des produits ou de la santé.  

### <a name="27-adult-content"></a>2.7 Contenu pour adultes  

Votre extension ne doit pas contenir ou afficher de contenu qu’une personne raisonnable considérerait comme explicite ou explicite.  

### <a name="28-prohibited-content-services-and-activity"></a>2.8 Contenu, services et activité interdits  

Votre extension doit respecter les conditions suivantes.  

*   Votre extension ne doit pas contenir de contenu ni fournir de services qui facilitent les jeux en ligne.  Les jeux en ligne incluent, sans s’y limiter, des jeux en ligne, des jeux de société ou des jeux de compétences qui offrent des billets ou d’autres valeurs.  
*   Votre extension ne doit pas fournir un accès non autorisé au contenu du site web, par exemple en contournant les paywalls ou les restrictions de connexion.  
*   Votre extension ne doit pas fournir, encourager ou activer l’accès non autorisé, le téléchargement ou la diffusion en continu de contenu ou de contenu multimédia protégés par des droits d’auteur.  
*   Votre extension ne doit pas être minée par cryptomonnaie.  
    
### <a name="29-illegal-activity"></a>2.9 Activités illégales  

Votre extension ne doit pas contenir de contenu ou de fonctionnalité qui encourage, facilite ou encourage les activités illégales dans le monde réel.  

### <a name="210-excessive-profanity-and-inappropriate-content"></a>2.10 Blasphème excessif et contenu inapproprié  

*   Votre extension ne doit pas contenir de blasphémité excessive ou gratuite.  
*   Votre extension ne doit pas contenir ou afficher du contenu qu’une personne raisonnable considère comme étant insérable.  
    
### <a name="211-countryregion-specific-requirements"></a>2.11 Exigences spécifiques aux pays/régions  

Le contenu choquant dans n’importe quel pays/région vers lequel votre extension est ciblée n’est pas autorisé.  Le contenu peut être considéré comme choquant dans certains pays/régions en raison des lois locales ou des normes culturelles.  Voici quelques exemples de contenu potentiellement choquant dans certains pays/régions :  

**Chine**  

*   Contenu sexuelle interdit  
*   Références de territoire ou de région en litige  
*   Fourniture ou activation de l’accès au contenu ou aux services qui ne sont pas en vigueur dans le cadre de la loi locale applicable  
    
### <a name="212-age-ratings"></a>2.12 Classification par âge  

#### <a name="2121-mature-content"></a>2.12.1 Contenu mature  

Lorsque vous soumettez votre extension à [l’Partner Center,][MicrosoftPartnerCenter]vous devez indiquer si votre extension affiche le contenu qui doit être marqué comme « Mature ».  Lorsque vous déterminez l’évaluation de votre extension, prenez en compte tout le contenu de votre application, y compris le contenu généré par l’utilisateur et les publicités, ainsi que le contenu lié à votre extension.  Si vous indiquez que votre extension ne contient aucun contenu « mature », vous êtes responsable du maintien de la précision de cette évaluation.  Quelle que soit l’évaluation donnée à votre extension, elle doit toujours respecter toutes les exigences de contenu des stratégies Microsoft Edge développeur de modules supplémentaires  

#### <a name="2122-ratings-change"></a>2.12.2 Modification des évaluations  

Si votre extension fournit du contenu \(tel que le contenu généré par l’utilisateur, la vente au détail ou tout autre contenu web\) qui peut être approprié pour une classification par âge supérieure à la classification attribuée, vous devez obliger les utilisateurs à choisir de recevoir ce contenu à l’aide d’un filtre de contenu ou en se signant avec un compte pré-existant.  

### <a name="213-videos"></a>2.13 Vidéos  

Si vous soumettez une vidéo promotionnelle dans la liste, elle doit respecter toutes les instructions de contenu mentionnées dans cette stratégie.  Si vous choisissez de fournir un lien YouTube, vous devez vous assurer que les publicités sont désactivées pour les vidéos spécifiques que vous souhaitez incorporer.  Pour plus d’informations sur l’option d' turning on ou off ads sur YouTube, accédez à Définir vos [formats de][GoogleYoutubeAnswer2531367Topic7072227] publicité par défaut et les publicités [sur les vidéos incorporées.][GoogleYoutubeAnswer132596]


## <a name="certification-appeal-process"></a>Processus d’appel de certification

Toutes les extensions doivent respecter les stratégies de magasin répertoriées ci-dessus. Si votre extension a échoué dans le processus de révision, consultez les stratégies de magasin pour comprendre la raison de l’échec. Après avoir soumis votre extension à l’aide de l’Partner Center, pour poser une question sur l’état de révision ou de certification de celui-ci, accédez à Nouvelle demande de support [et][MicrosoftSupportSupportrequestformE7a381be9c9aFafbEd76262bc93fd9e4] remplissez le formulaire.

### <a name="microsoft-edge-add-ons-appeal-statistics-for-fy2021"></a>Microsoft Edge Statistiques d’appel des modules add-ons pour l’année 2021

| Principal type de réclamation #1 : appel de l’application | Principal type de réclamation #2 : résultats de certification | Autres types de réclamations | Nombre total de réclamations | Plaintes non reçues |
|:--- |:--- |
| 8 | 2 | 4 | 14 | 0 |


<!-- links -->  

[MicrosoftEdgeContentSecurityPolicyRemoteScript]: ./csp.md#relaxing-the-default-policy "Relâchement de la stratégie par défaut - Stratégie de sécurité du contenu \(CSP\) | Documents Microsoft"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Contrat du développeur d’applications | Documents Microsoft"  
[MicrosoftIdentifiesMalwareUnwantedApplications]: /windows/security/threat-protection/intelligence/criteria "Comment Microsoft identifie les programmes malveillants et les applications potentiellement indésirables | Documents Microsoft"  

[GoogleYoutubeAnswer2531367Topic7072227]: https://support.google.com/youtube/answer/2531367?ref_topic=7072227 "Définir vos formats de publicitaire par défaut - Aide de YouTube"  
[GoogleYoutubeAnswer132596]: https://support.google.com/youtube/answer/132596 "Publicités sur des vidéos incorporées - Aide de YouTube"  
[FTCChildrensPrivacy]: https://www.ftc.gov/tips-advice/business-center/privacy-and-security/children%27s-privacy "Confidentialité des enfants - Commission commerciale fédérale"  

[MicrosoftAdvertisingCreativeAcceptancePolicies]: https://about.ads.microsoft.com/solutions/ad-products/display-advertising/creative-acceptance-policies "Stratégies d’acceptation créative : Microsoft Advertising"  
[MicrosoftAdvertisingCreativeSpecifications]: https://about.ads.microsoft.com/solutions/ad-products/display-advertising/creative-specs "Spécifications créatives - Microsoft Advertising"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  

[MicrosoftSupportSupportrequestformE7a381be9c9aFafbEd76262bc93fd9e4]: https://support.microsoft.com/supportrequestform/e7a381be-9c9a-fafb-ed76-262bc93fd9e4 "Extensions New Support Request | Microsoft Support"