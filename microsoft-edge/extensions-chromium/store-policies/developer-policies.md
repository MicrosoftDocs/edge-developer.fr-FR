---
description: Stratégies de développeur du catalogue de modules de développement de Microsoft Edge.
title: Stratégies de développeur du catalogue de modules de développement de microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, développement d’extensions, extensions de navigateur, addons, centre de partenaires, développeur
ms.openlocfilehash: 5c2a8dd816a28a35b6e7b725d5106814e401f6ec
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327644"
---
# Stratégies de développeur du catalogue de modules de développement de microsoft Edge  

## Introduction et objectif de ce document  

Merci de votre intérêt pour le développement d’extensions pour le catalogue d’extensions Microsoft Edge.  Les stratégies de développeur du catalogue de modules extensions Microsoft Edge \(Stratégies de développeur de catalogue d’extensions\) s’appliquent à vos extensions, y compris votre envoi d’extensions via l’Partner [Center][MicrosoftPartnerCenter] et la mise en service de ces extensions via les extensions Microsoft Edge.  

## Principes  

Quelques principes pour vous aider à démarrer :  

*   Vous devez offrir une valeur unique et distincte dans vos extensions pour Microsoft Edge.  Fournissez une raison intéressante pour télécharger vos extensions à partir du catalogue d’extensions Microsoft Edge \(Microsoft Edge Add-ons\).  
*   Vous ne devez pas induire en erreur nos utilisateurs communs concernant les actions de votre extension, les personnes qui l’offrent, etc.  
*   Vous ne devez pas essayer de insérer les utilisateurs, le système ou l’écosystème.  Il n’y a pas de place dans nos modules de modules microsoft Edge pour tout type de fraude ; que ce soit la manipulation des évaluations et des révisions, la fraude par carte de crédit ou toute autre activité frauduleuse.  
    
Le respect des stratégies de développement du magasin de modules de développement Microsoft Edge doit vous aider à faire des choix qui améliorent l’appel et le public de votre extension.  

Vos extensions sont essentielles à l’expérience de centaines de millions d’utilisateurs.  Nous avons le plaisir de découvrir ce que vous créez et sommes ravis de vous aider à fournir vos extensions au monde entier.  

## 1. Stratégies de produit  

### 1.1 Fonction distincte & valeur ; Représentation précise  

Votre extension et les métadonnées associées doivent refléter précisément et clairement la source, les fonctionnalités et les fonctionnalités que vous décrivez.  

#### 1.1.1 Les extensions doivent avoir un seul objectif  

Votre extension doit avoir un seul objectif avec une fonctionnalité étroite.  

#### 1.1.2 Décrire votre extension  

Tous les aspects de votre extension doivent décrire avec précision les fonctions, fonctionnalités et limitations importantes de votre extension, y compris les périphériques d’entrée requis ou pris en charge.  La proposition de valeur de votre extension doit être claire lors de la première utilisation.  Votre extension peut ne pas utiliser un nom ou une icône semblable à celui d’autres extensions et ne doit pas revendiquer la représentation d’une société, d’un organisme public ou d’une autre entité si vous n’êtes pas autorisé à effectuer cette représentation.  

#### 1.1.3 Fonctionnalité  

Votre extension doit être entièrement fonctionnelle.  

#### 1.1.4 Recherche et découverte  

Les termes de recherche ne peuvent pas dépasser sept termes uniques et doivent être pertinents pour votre extension.  

#### 1.1.5 Fournir les détails appropriés  

Vous devez fournir des détails distincts et informatifs sur votre extension et la fonctionnalité de description \(metadata\) de votre extension.  Votre extension doit fournir une expérience utilisateur précieuse et de qualité.  Votre extension doit également avoir une présence active dans les extensions Microsoft Edge.  

#### 1.1.6 Stabilité et performances  

Votre extension ne doit pas avoir d’impact négatif sur les performances ou la stabilité de Microsoft Edge.  

#### 1.1.7 Obfuscation  

Les extensions avec du code obscurci ne sont pas autorisées.  Cela inclut le code dans votre package d’extension, ainsi que tout code externe ou ressource récupéré à partir du web.  Vous pouvez être invité à refactoriser des parties de votre code s’il n’est pas reviewable.  

#### 1.1.8 Modification des paramètres du navigateur  

Votre extension ne doit pas, sans le consentement de l’utilisateur approprié, modifier ou sembler modifier les fonctionnalités ou paramètres du navigateur, y compris, mais sans s’y limiter : le fournisseur de recherche et les suggestions de la barre d’adresses, la page de démarrage ou d’accueil, la page nouvel onglet et l’ajout ou la suppression du favori.  

Toute modification apportée aux paramètres du navigateur doit être explicitement documentée dans la description de votre extension.  

Votre extension peut uniquement réviser les paramètres clés pour remplacer une page web ou un service Microsoft par celui d’un tiers \(par exemple, exiger l’utilisation d’un moteur de recherche tiers ou définir la page d’accueil sur une propriété web tierce\) si vous êtes employé par ou autrement associé à un tel tiers.  

### 1.2 Sécurité  

Votre extension ne doit pas mettre en danger ou compromettre la sécurité des utilisateurs, ni la sécurité ou les fonctionnalités de l’appareil, du système ou des systèmes associés.  

#### 1.2.1 Stratégies de sécurité du contenu  

> [!NOTE]
> Si vous a apporté des modifications à votre extension au-delà de la fonctionnalité décrite, toutes les modifications apportées au code doivent être conformes à la stratégie de sécurité de contenu [Microsoft Edge.][MicrosoftEdgeContentSecurityPolicyRemoteScript]  Par exemple, votre extension ne doit pas télécharger un script distant et exécuter ce script d’une manière qui n’est pas cohérente avec la fonctionnalité décrite.  

#### 1.2.2 Logiciels indésirables et malveillants  

Votre extension ne doit pas contenir ou activer les programmes malveillants tels que définis par les critères De Microsoft pour [les logiciels indésirables et malveillants][MicrosoftIdentifiesMalwareUnwantedApplications].  

#### 1.2.3 Dépendance à d’autres logiciels  

Votre extension peut dépendre de logiciels non intégrés \(par exemple, un autre produit, module ou service\) pour fournir la fonctionnalité principale, à condition que vous divulguiez la dépendance dans la description  

#### 1.2.4 Extensions Update  

Sauf autorisation contraire de Microsoft, vos extensions doivent être mises à jour uniquement par le biais des extensions Microsoft Edge.  

### 1.3 Le produit peut être testé  

Votre extension doit être testable.  S’il n’est pas possible de tester votre extension pour une raison quelconque, y compris, mais sans s’y limiter, les éléments ci-dessous, votre extension peut échouer à cette exigence.  

#### 1.3.1 Informations d’identification de l’utilisateur  

Si votre extension nécessite des informations d’identification de connexion, fournissez un compte de démonstration de travail à l’aide du `Notes for certification` champ.  

#### 1.3.2 Disponibilité des services  

Si votre extension nécessite un accès à un serveur, le serveur doit être fonctionnel pour vérifier qu’il fonctionne correctement.  

### 1.4 Utilisation  

Votre extension doit respecter les normes du magasin de modules de microsoft Edge pour la convivialité, y compris, mais sans s’y limiter, celles répertoriées dans les sous-sections ci-dessous.  

#### 1.4.1 Compatibilité entre les plateformes  

Votre extension doit être compatible avec Microsoft Edge sur tous les appareils et plateformes sur lesquels ils peuvent être téléchargés.  Si une extension est téléchargée sur un appareil avec lequel elle n’est pas compatible, elle doit détecter cela au lancement et afficher un message à l’utilisateur détaillant les exigences que les appareils doivent respecter pour être compatibles avec votre extension.  

#### 1.4.2 Expérience utilisateur  

Votre extension doit démarrer rapidement et doit rester réactive aux entrées de l’utilisateur.  Votre extension doit continuer à s’exécuter et rester réactive aux entrées de l’utilisateur.  Votre extension doit s’arrêter normalement et ne pas se fermer de manière inattendue.  Votre extension doit gérer les exceptions et rester réactive aux entrées de l’utilisateur une fois l’exception gérée.  

### 1.5 Informations personnelles  

Les conditions suivantes s’appliquent aux extensions qui accèdent aux informations personnelles.  Les informations personnelles incluent toutes les informations ou données qui identifient ou peuvent être utilisées pour identifier une personne, ou qui sont associées à ces informations ou données.  

#### 1.5.1 Collecter des informations personnelles uniquement si nécessaire  

Votre extension peut collecter, consulter, utiliser ou transmettre des informations personnelles \(y compris l’activité de navigation web\) ; uniquement s’il est requis par et uniquement pour une utilisation dans une fonctionnalité visiblement divulguée par l’utilisateur.  

#### 1.5.2 Maintenir une politique de confidentialité  

Que votre extension accède, collecte ou transmette des informations personnelles ; vous devez fournir une notification importante et vous conformer à votre politique de confidentialité si la loi l’exige.  Votre politique de confidentialité doit informer les utilisateurs des informations personnelles accessibles, collectées ou transmises par votre poste, de la façon dont ces informations sont utilisées, stockées et sécurisées, et d’indiquer les types de parties à qui elles sont divulguées.  Votre politique de confidentialité doit décrire les contrôles que les utilisateurs ont sur l’utilisation et le partage de leurs informations, la façon dont ils accèdent à leurs informations, et elle doit respecter les lois et réglementations applicables.  Votre politique de confidentialité doit être tenue à jour lorsque vous ajoutez de nouvelles fonctionnalités à votre extension.  

Si vous fournissez à Microsoft votre politique de confidentialité, vous acceptez d’autoriser Microsoft à partager cette politique de confidentialité avec les utilisateurs de votre extension.  

#### 1.5.3 Partage de données avec des tiers  

Vous pouvez publier les informations personnelles des utilisateurs de votre extension sur un service externe ou tiers via votre extension ou les métadonnées associées uniquement après avoir obtenu le consentement de ces utilisateurs.  Le consentement de l’utilisateur signifie que les utilisateurs donnent leur autorisation express dans l’interface utilisateur de votre extension pour l’activité demandée, après que vous :  

*   Décrire à vos utilisateurs comment les informations sont accessibles, utilisées ou partagées, et indiquer les types de parties à qui elles sont divulguées, et  
*   Fournissez à vos utilisateurs un mécanisme dans votre interface utilisateur d’extension par le biais duquel ils ont la possibilité d’annuler ultérieurement l’autorisation et de refuser.  
    
#### 1.5.4 Partage d’informations d’utilisateurs non-utilisateurs  

Si vous publiez les informations personnelles d’une personne à un service externe ou tiers via votre extension ou les métadonnées, mais que la personne dont les informations sont partagées n’est pas un utilisateur de votre extension ;  

1.  Vous devez obtenir le consentement écrit express pour publier ces informations personnelles.  
1.  Vous devez autoriser la personne dont les informations sont partagées à retirer ce consentement à tout moment.  
1.  Votre politique de confidentialité doit clairement divulguer que vous pouvez collecter des informations personnelles de cette manière.  
1.  Si la loi applicable l’exige, vous devez supprimer les informations personnelles de toute personne sur demande, y compris les personnes dont vous collectez les informations de cette manière.  
1.  Si votre extension permet aux utilisateurs d’accéder aux informations personnelles d’une autre personne, cette exigence s’applique également.  
    
#### 1.5.5 Transmettre des informations en toute sécurité  

Si votre extension collecte, stocke ou transmet des informations personnelles ; Il doit le faire en toute sécurité à l’aide de méthodes de chiffrement modernes.  

#### 1.5.6 Informations hautement sensibles  

Votre extension ne doit pas collecter, stocker ou transmettre des informations personnelles hautement sensibles, telles que des données de santé ou financières, sauf si elles sont liées aux fonctionnalités de votre extension.  Votre extension doit également obtenir le consentement de l’utilisateur express avant de collecter, stocker ou transmettre ces informations.  

### 1.6 Autorisations  

Votre extension doit uniquement demander les autorisations nécessaires au fonctionnement.  Vous devez fournir une description du fonctionnement de votre extension.  Votre extension doit uniquement être exécutée comme décrit.  Votre extension peut ne pas demander d’autorisation pour les fonctionnalités qui vont au-delà des fonctionnalités requises pour effectuer et fonctionner comme déclaré.  

### 1.7 Localisation  

Vous devez trouver votre extension pour toutes les langues que votre extension prétend prendre en charge.  Le texte de la description de votre extension doit être localisée dans chaque langue que vous déclarez.  
Si votre extension est localisée de sorte que certaines fonctionnalités ne soient pas disponibles dans une version localisée, vous devez clairement faire état ou afficher les limites de localisation dans la description de votre extension. L’expérience fournie par une extension doit être assez similaire dans toutes les langues qu’elle prend en charge.  

### 1.8 Transactions financières  

Si votre produit inclut des achats in-product, des abonnements, une devise virtuelle, des fonctionnalités de facturation ou capture des informations financières ; les conditions requises dans les sections suivantes s’appliquent.  

#### 1.8.1 Fonctionnalités payantes  

Votre extension peut permettre aux utilisateurs de consommer du contenu numérique ou des services achetés via un mécanisme d’achat tiers ou une API.  

Vous devez utiliser une API d’achat tierce sécurisée pour les achats de biens physiques ou de services.  Vous devez utiliser une API d’achat tierce sécurisée pour les paiements effectués dans le cadre de tout autre service, y compris les dons de jeux ou de dons réels.  

*   Si votre poste est utilisé pour faciliter ou collecter des contributions ou pour effectuer un bal promotionnel ou un prix, vous devez le faire conformément à la loi applicable.  
*   Vous devez également clairement faire savoir que Microsoft n’est pas le soutien ou le sponsor de la promotion.  
*   Les offres dans le produit vendues dans votre extension ne doivent pas être converties en devise valide légalement \(par exemple, USD, Euro, etc.) ou en biens physiques ou services.  
    
Les conditions suivantes s’appliquent à votre utilisation d’une API d’achat tiers sécurisée :  

*   Au moment de la transaction ou lorsque vous collectez des informations financières ou de paiement auprès de l’utilisateur ; votre extension doit identifier le fournisseur de transactions commerciales, authentifier l’utilisateur et obtenir la confirmation de l’utilisateur pour la transaction.  Un fournisseur de transactions commerciales maintient une plateforme sécurisée pour les échanges financiers.  
*   Votre extension peut offrir aux utilisateurs la possibilité d’enregistrer cette authentification, mais les utilisateurs doivent avoir la possibilité d’exiger une authentification sur chaque transaction ou de désactiver les transactions dans le produit.  
*   Si votre poste collecte des informations de carte de crédit ou utilise un processeur de paiement tiers qui collecte des informations de carte de crédit, le traitement des paiements doit respecter la norme PCI de sécurité des données \(PCI DSS\).  
    
#### 1.8.2 Divulgation des fonctionnalités payantes  

Votre extension et les métadonnées associées doivent fournir des informations sur les types d’achats in-product proposés et la plage de prix.  Vous ne devez pas induire en erreur les utilisateurs et être clair sur la nature de vos offres et promotions dans le produit, y compris l’étendue et les conditions des expériences d’essai.  Si votre extension limite l’accès au contenu créé par l’utilisateur pendant ou après une version d’essai, vous devez en informer les utilisateurs à l’avance.  En outre, votre extension doit clairement faire savoir aux utilisateurs qu’ils lancent une option d’achat dans votre extension.  

### 1.9 Notifications  

Votre extension doit respecter les paramètres système pour les notifications.  Cela signifie que toute présentation de publicités et de notifications aux utilisateurs doit être cohérente avec les préférences de l’utilisateur, que les notifications soient fournies par le service de notification Push de Microsoft \(MPNS\), le service de notification Push Windows \(WNS\) ou tout autre service.  Si l’utilisateur désactive les notifications, que ce soit pour un produit spécifique ou à l’échelle du système, votre extension doit rester fonctionnelle.  

Si votre produit utilise MPNS ou WNS pour transmettre des notifications, il doit respecter les exigences suivantes :  

#### 1.9.1 Recommandations générales  

Les notifications fournies par le biais de WNS ou MPNS sont considérées comme du contenu de produit et sont soumises à toutes les stratégies de développement du catalogue de modules ajoutes.  

#### 1.9.2 Propriété des notifications  

Vous ne devez pas masquer ou essayer de masquer la source d’une notification lancée à partir de votre extension.  

#### 1.9.3 Aucune information confidentielle ou sensible  

Vous ne devez pas inclure dans une notification des informations que les utilisateurs peuvent raisonnablement considérer comme confidentielles ou sensibles.  

#### 1.9.4 Objectif des notifications  

Les notifications envoyées à partir de votre extension doivent être liées à cette extension ou à d’autres extensions que vous publiez dans le catalogue d’extensions Microsoft Edge et ne doivent pas inclure de messages promotionnels de quelque type que ce soit qui n’est pas lié à vos extensions.  

### 1.10 Conduite et contenu publicitaire  

Pour toutes les activités publicitaires, les conditions suivantes s’appliquent :  

#### 1.10.1 Objectif  

Le contenu principal de votre extension ne doit pas être une publicité, et la publicité doit être clairement distinguer des autres contenus de votre extension.  

#### 1.10.2 Stratégies et accords  

Tout contenu publicitaire affiché par votre extension doit être conforme à la politique [d’acceptation créative de Microsoft.][MicrosoftAdvertisingCreativeAcceptancePolicies]  
Si votre extension affiche des publicités, tout le contenu [][MicrosoftAppDeveloperAgreement] affiché doit être conforme aux exigences publicitaires du Contrat du développeur d’applications et de la présente stratégie.  

#### 1.10.3 Qualité de la publicité  

*   L’objectif principal de votre extension ne doit pas être d’obtenir des utilisateurs qu’ils cliquent sur des publicités.  
*   Votre extension ne doit rien faire qui interfère avec ou diminue la visibilité, la valeur ou la qualité des publicités qu’elle affiche.  

#### 1.10.4 Promotions  

Si vous achetez ou créez des campagnes publicitaires pour promouvoir vos extensions par le biais de la fonctionnalité de campagne publicitaire dans l’Espace [partenaires,][MicrosoftPartnerCenter]tous les supports publicitaires que vous fournissez à Microsoft, y compris les pages d’accueil associées, doivent être conformes à la stratégie de [spécifications créatives][MicrosoftAdvertisingCreativeSpecifications] de Microsoft et à la stratégie d’acceptation créative [de Microsoft.][MicrosoftAdvertisingCreativeAcceptancePolicies]  

#### 1.10.5 Avertir les utilisateurs de la Opt-Out publicité Interest-Based publicité  

Votre déclaration de confidentialité ou vos conditions d’utilisation doivent informer les utilisateurs que vous envisagez d’envoyer des informations personnelles au fournisseur de services publicitaires et indiquer aux utilisateurs comment ils peuvent refuser les publicités basées sur les intérêts.  

#### 1.10.6 Autres recommandations  

Si votre extension s’adresse aux enfants de moins de 13 ans, comme défini dans la [children’s Online Privacy Protection Act][FTCChildrensPrivacy]; vous devez informer Microsoft de ce fait dans l’Partner [Center][MicrosoftPartnerCenter] et vous assurer que tout le contenu de la annonce affiché dans votre extension est approprié pour les enfants de moins de 13 ans.  

## 2 Stratégies de contenu  

Les stratégies suivantes s’appliquent au contenu et aux métadonnées \(y compris le nom de l’éditeur, le nom de l’extension, l’icône d’extension, la description de l’extension, les captures d’écran d’extension, les bandes-annonces d’extension et les miniatures de bande-annonce, et toutes les autres métadonnées d’extension\) proposées pour la distribution dans les extensions Microsoft Edge.  Le contenu signifie les images, les sons, les vidéos et le texte contenus dans votre extension, les vignettes, les notifications, les messages d’erreur ou les publicités exposés via votre extension, et tout ce qui est remis à partir d’un serveur ou auquel votre extension se connecte.  Étant donné que les extensions et les extensions Microsoft Edge sont utilisées dans le monde entier, ces exigences sont interprétées et appliquées dans le contexte de normes régionales et culturelles.  

### 2.1 Exigences en matière de contenu pour la liste des catalogues d’ajouts Microsoft Edge  

Les métadonnées et autres contenus que vous envoyez pour accompagner votre extension peuvent ne pas contenir de contenu mature.  
Les soumissions qui ne répondent pas aux conditions requises pour les listes des magasins de modules supplémentaires Microsoft Edge sont rejetées ou supprimées rapidement.  

### 2.2 Contenu incluant les noms, les logos, l’original et les tiers  

Tout le contenu de votre extension et les métadonnées associées doivent être créés à l’origine par le titulaire d’une licence tierce ou sous licence appropriée et ne doivent être utilisés que comme autorisé par le titulaire des droits ou comme autorisé par la loi.  

### 2.3 Risque de dommages  

#### 2.3.1 Conditions requises  

Votre extension ne doit pas contenir de contenu qui facilite ou favorise les activités du monde réel suivantes : \(a\) violence extrême ou gratuite ; \(b\) violations des droits de l’homme ; \(c\) la création d’armes illégales ; ou \(d\) l’utilisation d’armes contre une personne, un animaux ou une propriété réelle ou personnelle.  

#### 2.3.2 Responsabilité  

Votre poste ne doit pas : \(a\) poser un risque de sécurité pour, ni entraîner une gêne, une gêne ou tout autre dommage pour les utilisateurs finaux ou toute autre personne ou enfant ; ou \(b\) posent un risque de dommages ou de dommages à des propriétés réelles ou personnelles.  Vous êtes le seul responsable des tests de sécurité des extensions, de l’acquisition de certificats et de l’implémentation de toutes les protections de fonctionnalités appropriées.  Vous ne devez pas désactiver les fonctionnalités de sécurité ou de confort de la plateforme et vous devez inclure tous les avertissements, notifications et clauses d’exclusion de responsabilité juridiquement requis et standard applicables dans votre extension.  

### 2.4 Diffamante, caâmeuse, caeuse et répante  

Votre extension ne doit pas contenir de contenu diffamant, caculant, caculant ou dangereux.  

### 2.5 Contenu choquant  

Votre extension et les métadonnées associées ne doivent pas contenir de contenu potentiellement sensible ou choquant.  Le contenu peut être considéré comme sensible ou choquant dans certains pays/régions en raison des lois locales ou des normes culturelles.  En outre, votre extension et les métadonnées associées ne doivent pas contenir de contenu qui fait la défense de la discrimination, de la violence ou de la violence en fonction des considérations de la course, de l’appartenance à un groupe social, de l’origine nationale, de la langue, du sexe, de l’âge, du handicap, de l’orientation sexuelle, de l’état en tant que travailleur ou de l’appartenance à un autre groupe social.  

### 2.6 Consommation, consommation d’enfants et enfants  

Votre extension ne doit pas contenir de contenu qui facilite ou favorise l’utilisation excessive ou dangereuse de l’antériorisation, des produits ou de la santé.  

### 2.7 Contenu pour adultes  

Votre extension ne doit pas contenir ou afficher du contenu qu’une personne raisonnable considère comme explicite ou explicite.  

### 2.8 Contenu, services et activité interdits  

Votre extension doit respecter les conditions suivantes.  

*   Votre extension ne doit pas contenir de contenu ni fournir de services qui facilitent les jeux en ligne.  Les jeux en ligne incluent, sans s’y limiter, des jeux en ligne, des jeux de société ou des jeux de compétences qui offrent des billets ou d’autres valeurs.  
*   Votre extension ne doit pas fournir un accès non autorisé au contenu du site web, par exemple en contournant les paywalls ou les restrictions de connexion.  
*   Votre extension ne doit pas fournir, encourager ou activer l’accès non autorisé, le téléchargement ou la diffusion en continu de contenu ou de contenu multimédia protégés par des droits d’auteur.  
*   Votre extension ne doit pas être minée par cryptomonnaie.  
    
### 2.9 Activités illégales  

Votre extension ne doit pas contenir de contenu ou de fonctionnalité qui encourage, facilite ou encourage les activités illégales dans le monde réel.  

### 2.10 Blasphème excessif et contenu inapproprié  

*   Votre extension ne doit pas contenir de blasphémité excessive ou gratuite.  
*   Votre extension ne doit pas contenir ou afficher du contenu qu’une personne raisonnable considère comme étant insérable.  
    
### 2.11 Exigences spécifiques aux pays/régions  

Le contenu choquant dans n’importe quel pays/région vers lequel votre extension est ciblée n’est pas autorisé.  Le contenu peut être considéré comme choquant dans certains pays/régions en raison des lois locales ou des normes culturelles.  Voici quelques exemples de contenu potentiellement choquant dans certains pays/régions :  

**Chine**  

*   Contenu sexuelle interdit  
*   Références de territoire ou de région en litige  
*   Fourniture ou activation de l’accès au contenu ou aux services qui ne sont pas en vigueur dans le cadre de la loi locale applicable  
    
### 2.12 Classification par âge  

#### 2.12.1 Contenu mature  

Lorsque vous soumettez votre extension à [l’Partner Center,][MicrosoftPartnerCenter]vous devez indiquer si votre extension affiche le contenu qui doit être marqué comme « Mature ».  Lorsque vous déterminez l’évaluation de votre extension, prenez en compte tout le contenu de votre application, y compris le contenu généré par l’utilisateur et les publicités, ainsi que le contenu lié à votre extension.  Si vous indiquez que votre extension ne contient aucun contenu « mature », vous êtes responsable du maintien de la précision de cette évaluation.  Quelle que soit l’évaluation donnée à votre extension, elle doit toujours respecter toutes les exigences de contenu des stratégies de développement des extensions Microsoft Edge  

#### 2.12.2 Modification des évaluations  

Si votre extension fournit du contenu \(tel que le contenu généré par l’utilisateur, la vente au détail ou tout autre contenu web\) qui peut être approprié pour une classification par âge supérieure à la classification attribuée, vous devez obliger les utilisateurs à choisir de recevoir ce contenu à l’aide d’un filtre de contenu ou en se signant avec un compte pré-existant.  

### 2.13 Vidéos  

Si vous soumettez une vidéo promotionnelle dans la liste, elle doit suivre toutes les instructions de contenu mentionnées dans cette stratégie.  Si vous choisissez de fournir un lien YouTube, vous devez vous assurer que les publicités sont désactivées pour les vidéos spécifiques que vous souhaitez incorporer.  Pour plus d’informations sur la façon dont les publicités sont activées et désactivées sur YouTube, voir [support.google.com/youtube/answer/2531367?ref_topic=7072227][GoogleYoutubeAnswer2531367Topic7072227] et [support.google.com/youtube/answer/132596][GoogleYoutubeAnswer132596].  

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
