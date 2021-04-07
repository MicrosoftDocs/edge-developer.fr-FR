---
ms.assetid: 1b3ebc25-d023-4f23-bbba-dce066c20de8
description: Découvrir comment les meilleures pratiques et les applications Internet enrichies accessibles (ARIA) peuvent se rassembler pour créer un site web accessible.
title: Créer | Accessibilité
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/06/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: accessibilité, accessibilité pour les développeurs, sites web accessibles, edge, développement web, ARIA, développeur, UIA, UI Automation
ms.custom: seodec18
ms.openlocfilehash: 3bc16450a3a64c06d290d1d3e112a9b2faecbe14
ms.sourcegitcommit: 146072bf606b84e5145a48333abf9c6b892a12d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/07/2021
ms.locfileid: "11480152"
---
# <a name="building-accessible-websites"></a>Création de sites web accessibles

Le site web est rempli de sites web, d’applications et d’interfaces utilisateur dynamiques et complexes créés à l’aide d’une combinaison de code HTML, CSS et JavaScript.  Toutefois, lorsqu’ils sont conçus et créés sans accessibilité à l’esprit, ces sites web complexes sont difficiles à utiliser par les personnes qui s’appuient sur des [technologies](https://webaim.org/articles/motor/assistive) d’assistance pour parcourir le web. La création de sites web accessibles aux personnes présentant un handicap nécessite des informations sémantiques sur l’interface utilisateur. Cela permet aux technologies d’assistance, telles que les lecteurs d’écran, de transmettre les informations nécessaires pour aider les personnes ayant un large éventail de capacités à utiliser le site web.

Visitez [HTML5Accessibility pour](https://html5accessibility.com) obtenir des informations sur les nouvelles fonctionnalités HTML5 qui sont accessibles et pris en charge par Microsoft Edge.

## <a name="how-accessibility-works"></a>Fonctionnement de l’accessibilité

Les technologies d’assistance ajoutent des fonctionnalités que les ordinateurs n’ont généralement pas. Par exemple, un utilisateur malvoyant peut utiliser son clavier en combinaison avec une technologie d’assistance telle qu’un lecteur d’écran, plutôt que d’utiliser directement le navigateur avec la souris et l’écran. Pour les applications sur les plateformes Microsoft et sur le web, la technologie d’assistance interagit avec Microsoft [UI Automation,](https://msdn.microsoft.com/library/windows/desktop/bb892135.aspx)un modèle objet propre à l’application, tel que le modèle DOM (Document Object Model) dans Microsoft Edge, ou une combinaison de ces derniers.

Pour les développeurs web, certains éléments HTML sont mappés à des objets UI Automation. Ainsi, lors de la sélection de ces éléments HTML, le développeur peut utiliser les propriétés d’accessibilité et les événements intégrés à ces éléments. Lors du développement de votre site web, il vous suffit généralement de vous assurer que l’API est correctement écrite (ou que l’élément approprié est spécifié), afin que l’application soit accessible. Pour plus [d’informations, consultez ARIA](./ARIA-and-UI-Automation.md) et UI Automation dans Microsoft Edge.  Pour plus d’informations sur les applications de plateforme Windows universelle (UWP) accessibles, accédez à la rubrique [Accessibilité](https://msdn.microsoft.com/windows/uwp/accessibility/accessibility) du Centre de dév. Windows.

De nombreux problèmes d’accessibilité courants avec le contenu dynamique peuvent être résolus par une bonne pratique de codage, et la documentation [WCAG 2.0](https://go.microsoft.com/fwlink/p/?LinkID=24629) inclut de nombreuses techniques et meilleures pratiques pour vous aider à créer des applications web dynamiques plus accessibles. Toutefois, même lorsqu’il est correctement codé, le contenu dynamique n’est pas nécessairement accessible. [Les applications Internet enrichies accessibles (ARIA)](#aria) permettent de contourner ce problème.  

Pour plus d’informations sur l’accessibilité web, consultez [l’introduction](https://www.w3.org/WAI/intro/accessibility.php) à l’accessibilité web par l’initiative d’accessibilité web [(CAS).](https://www.w3.org/WAI)

## <a name="aria"></a>ARIA

La spécification ARIA [(Accessible Rich Internet Applications)](https://www.w3.org/TR/wai-aria/) de l’Initiative d’accessibilité web du W3C définit comme une syntaxe pour rendre le contenu web dynamique et les interfaces utilisateur personnalisées accessibles à tous. [](https://www.w3.org/WAI/) ARIA étend le code HTML à l’aide d’attributs supplémentaires (rôles, propriétés et états) conçus pour transmettre une sémantique personnalisée. Ces attributs sont utilisés par les navigateurs pour transmettre l’état et le rôle des contrôles à l’API d’accessibilité.

### <a name="roles-properties-and-states"></a>Rôles, propriétés et états

Les rôles ARIA sont définies sur des éléments utilisant l’attribut pour fournir des technologies d’assistance et des API [`role`](https://msdn.microsoft.com/library/cc304102(v=vs.85).aspx) d’accessibilité sur l’élément. Par exemple, l’élément `<li>` ci-dessous est affecté pour signifier `role="menuitem"` qu’il s’agit d’un élément dans un menu.

```html
<li role="menuitem">Home</li>
```

Les états et propriétés ARIA sont des attributs préfixés aria qui fournissent des informations spécifiques sur un objet pour vous aider à définir la nature des rôles. Les propriétés sont des attributs essentiels à la nature d’un objet, comme [`aria-readonly`](https://msdn.microsoft.com/library/cc304089(v=vs.85).aspx) et [`aria-haspopup`](https://msdn.microsoft.com/library/cc304081(v=vs.85).aspx) . La modification d’une propriété affecte la signification de l’objet. Dans l’exemple ci-dessous, la propriété est définie sur un élément de `aria-haspopup="true"` menu pour signifier qu’elle possède une fenêtre `<li>` déroulante.

```html
<li role="menuitem" aria-haspopup="true">Open</li>
```

Les états ne modifient pas la nature de l’objet, mais représentent les informations associées à l’interaction de l’objet ou de l’utilisateur avec l’objet, comme [`aria-hidden`](https://msdn.microsoft.com/library/cc304083(v=vs.85).aspx) ou [`aria-checked`](https://msdn.microsoft.com/library/cc304075(v=vs.85).aspx) . Par exemple, l’état dans l’exemple ci-dessous représente que la case à `aria-checked="false"` cocher n’est pas cochée.

```html
<div role="checkbox" aria-checked="false">Accept</div>
```

Go to [The Roles Model](https://www.w3.org/TR/wai-aria-1.1/#roles) by the W3C to see a full list of roles, properties, and states.

Pour plus d’informations sur ARIA, accédez à ARIA dans la section [Ressources.](#resources)

## <a name="assistive-technology-compatibility-testing"></a>Test de compatibilité des technologies d’assistance  

Vérifier que le site web que vous construisez fonctionne avec des technologies d’assistance réelles est la meilleure façon de garantir une bonne expérience pour vos utilisateurs présentant un handicap.  Étant donné que de nombreuses technologies d’assistance utilisent le clavier, le test de l’accessibilité du clavier de votre site web est un bon point de départ.  [Le test de compatibilité du][W3cPerspectiveVideosKeyboard] clavier valide que les utilisateurs ont accès à tous les contrôles interactifs sans nécessiter de souris.  Microsoft [Accessibility Insights for Web][AccessibilityinsightsWebOverview] est une extension de navigateur pour Microsoft Edge et Chrome qui vous guide et révèle plusieurs problèmes courants.  

Une fois que vous êtes certain que votre site web fonctionne bien avec un clavier, essayez-le avec d’autres technologies d’assistance, telles que les lecteurs d’écran.  Il révèle les problèmes suivants.

*   Votre code HTML, ARIA et CSS.  
*   Niveau de prise en charge d’une technologie d’assistance pour une fonctionnalité ou une technique.  
    
Différents navigateurs peuvent maquer des éléments à des API d’accessibilité de plateforme différemment de Microsoft Edge.  Lors de la création de votre interface, il est important de prendre en compte chaque différence.  

WebAIM effectue des [][WebaimProjectsScreenreadersurvey8] enquêtes avec des lecteurs d’écran et des utilisateurs à faible [vision][WebaimProjectsLowvisionsurvey2] qui vous aident à choisir les technologies d’assistance et les navigateurs que vous souhaitez tester.  

### <a name="learning-how-to-test"></a>Apprendre à tester  

Les technologies d’assistance sont des outils sophistiqués.  Ne supposez pas que vous êtes en mesure de commencer immédiatement les tests avec une technologie d’assistance sans avoir tout d’abord appris comment elle fonctionne.  L’apprentissage du test avec un lecteur d’écran présente une courbe d’apprentissage particulièrement pointée.  Un utilisateur de lecteur d’écran débutant peut supposer qu’un bogue de lecteur d’écran s’est produit alors que le problème est lié à une mauvaise utilisation du lecteur d’écran.  

Pour plus d’informations sur l’apprentissage des technologies d’assistance, accédez à Test avec lecteurs [d’écran][WebaimArticlesScreenreaderTesting] sur WebAIM.  

### <a name="testing-locally"></a>Test local  

La plupart des appareils incluent une technologie d’assistance intégrée au système d’exploitation.  Microsoft Windows inclut le lecteur [d’écran][MicrosoftSupport22798] du Narrateur Windows et la [Loupe Windows.][MicrosoftSupportWindows414948ba8b1cD3bd86150e5e32204198]  Les technologies d’assistance tierces telles que [NVDA,][NvaccessAboutNvda] [FreedomscientificSoftwareJaws]et [ZoomText][FreedomscientificSoftwareZoomtext] sont disponibles en téléchargement.  Apple macOS inclut le [lecteur d’écran VoiceOver.][AppleAccessibilityMacVision]  Et iOS, Android et Linux sont tous en charge de nombreuses technologies d’assistance.  

### <a name="testing-in-virtual-machines-and-emulators"></a>Test dans les machines virtuelles et les émulateurs  

Sous macOS, si vous souhaitez tester une technologie d’assistance uniquement disponible pour Windows, comme le Narrateur Windows ou NVDA, créez une machine virtuelle Windows.  Les machines virtuelles avec Microsoft Edge \(EdgeHTML\) et IE sont disponibles pour VirtualBox et VMWare sur la page de téléchargement [des machines virtuelles.][MicrosoftDeveloperEdgeVms]  

[Android Studio][AndroidDeveloperSdkInstallingStudioHtml] inclut un émulateur qui vous aide à tester les technologies d’assistance dans [la suite d’accessibilité Android.][GooglePlayStoreAndroidAccessibilitySuite]  Suivez les instructions pour configurer un périphérique [virtuel][AndroidDeveloperDevicesManagingAvdsHtml] et démarrer l’émulateur, [][AndroidDeveloperDevicesEmulatorHtml]puis installer la suite [d’accessibilité Android][GooglePlayStoreAndroidAccessibilitySuite] à partir de GooglePlay Store.  

> [!NOTE]
> Le simulateur iOS n’inclut actuellement pas VoiceOver.  

### <a name="cloud-based-testing-tools"></a>Outils de test basés sur le cloud  

Si une technologie d’assistance n’est pas disponible sur votre système d’exploitation ou si vous ne pouvez pas en installer une sur une machine virtuelle ou un émulateur, les outils de test de technologie d’assistance informatique sont la meilleure chose à faire.  

*   [Assistiv Labs (commercial)][AssistivlabsMain] vous permet de tester manuellement des technologies d’assistance via n’importe quel navigateur web moderne.  Choisissez une technologie d’assistance et un navigateur qui vous connecte à un ordinateur virtuel, un émulateur ou un appareil réel avec lequel vous pouvez interagir.  

## <a name="resources"></a>Ressources

### <a name="accessibility-basics"></a>Informations de base sur l’accessibilité

#### [<a name="the-a11y-project"></a>Le projet A11Y](http://a11yproject.com/)

Le projet A11Y est un effort communautaire visant à faciliter l’accessibilité du web. Consultez le site projet [A11Y](https://a11yproject.com/) pour en savoir plus sur les principes [](http://a11yproject.com/resources.html) d’accessibilité de base, leur modèle accessible et la bibliothèque de [widgets,](https://a11yproject.com/patterns)ainsi que leurs ressources sur les logiciels d’accessibilité, les blogs, les livres et les outils.

#### [<a name="web-accessibility-initiative-wai"></a>Initiative d’accessibilité web (CAS)](https://w3.org/WAI/)

L’initiative DNS (Web Accessibility Initiative) W3C est un effort pour améliorer l’accessibilité du site web. Leur site fournit une variété de ressources pour la prise en compte de l’accessibilité [web,](https://www.w3.org/WAI/gettingstarted/Overview.html)la conception pour [l’inclusion,](https://www.w3.org/WAI/users/Overview.html)les [didacticiels et les présentations,](https://www.w3.org/WAI/train.html)et bien plus encore.

### <a name="accessibility-blogs"></a>Blogs sur l’accessibilité

#### [<a name="the-paciello-group"></a>Groupe Paciello](https://www.paciellogroup.com/blog/)

Le groupe Paciello fournit des solutions de conseil et de technologie aux organisations du monde entier pour s’assurer que leurs clients atteignent tous les publics efficacement, tout en respectant les normes gouvernementales et internationales. Leur blog traite de sujets tels que les meilleures pratiques en matière d’accessibilité web, les outils d’accessibilité et les tendances d’accessibilité.

#### [<a name="simply-accessible"></a>Simple accessible](http://simplyaccessible.com/articles/)

Simply Accessible est une équipe de spécialistes de l’accessibilité qui fournit une formation sur l’accessibilité, des conseils et bien plus encore pour modifier la perception de l’accessibilité sur le web. Sa section [Articles](http://simplyaccessible.com/articles/) présente les meilleures pratiques en matière d’accessibilité web, de conception accessible et bien plus encore.

#### [<a name="ssb-bart-group-ssb"></a>SSB PREMIER GROUPE (SSB)](http://www.ssbbartgroup.com/blog/)

Le groupe SSB TELS est une société d’accessibilité numérique qui aide ses clients dans le développement et le déploiement de produits et de services accessibles. Leurs rubriques de blog traitent de sujets tels que les meilleures pratiques ARIA, les tendances d’accessibilité, les webinaires, etc.

### <a name="accessible-examples"></a>Exemples accessibles

#### [<a name="allyjs---tutorials"></a>ally.js - Didacticiels](http://allyjs.io/tutorials/)

Bibliothèque JavaScript pour aider les applications web modernes avec des problèmes d’accessibilité en rendant l’accessibilité plus simple.

#### [<a name="heydonworks---aria-examples"></a>Heydonworks - Exemples ARIA](http://heydonworks.com/practical_aria_examples/)

Exemples d’aria pratiques pour améliorer l’accessibilité de votre application

#### [<a name="openajax-examples"></a>Exemples OpenAjax](http://oaa-accessibility.org/)

Le site web OpenAjax Alliance est une excellente ressource pour vérifier les règles pour LARY-ARIA et fournit un certain nombre d’exemples d’implémentations DE LATN-ARIA.

#### [<a name="patterns"></a>Modèles](http://a11yproject.com/patterns.html)

[Le projet A11Y](http://a11yproject.com/) offre une bibliothèque de widgets et de modèles accessibles, tels que des menus, des boutons, des bulles et bien plus encore.

### <a name="accessibility-techniques--tools"></a>Techniques d’accessibilité & outils

#### [<a name="accessibility-creating-accessible-extension-icons-for-microsoft-edge"></a>Accessibilité : création d’icônes d’extension accessibles pour Microsoft Edge](/archive/microsoft-edge/legacy/developer/extensions/guides/accessibility)

Obtenez des conseils sur la création d’icônes d’extensions accessibles pour Microsoft Edge.

#### [<a name="accessible-name-and-description-computation-and-mappings-11"></a>Nom et description accessibles : Calcul et mappages 1.1](https://www.w3.org/TR/accname-1.1/)

Ce document de mappage W3C explique comment les navigateurs déterminent le nom et les descriptions des objets accessibles à partir de langages de contenu web et les exposent dans les API d’accessibilité.

#### [<a name="accessibility-evaluation-resources"></a>Ressources d’évaluation de l’accessibilité](https://www.w3.org/WAI/eval/Overview.html)

Les ressources d’évaluation de l’accessibilité sont une ressource multi-pages du W3C qui décrit différentes approches d’évaluation des sites web pour l’accessibilité.

#### [<a name="assistive-technology-compatibility-tests"></a>Tests de compatibilité des technologies d’assistance](http://www.powermapper.com/tests/)

Résultats des tests montrant le comportement de différents types de contenu et normes dans les technologies d’assistance (AT) comme les lecteurs d’écran.

#### [<a name="building-accessible-websites-just-got-a-lot-easier"></a>La création de sites web accessibles a été beaucoup plus facile](https://blogs.msdn.microsoft.com/webdev/2016/05/02/building-accessible-websites-just-got-a-lot-easier/)

Ce billet de blog .NET Web Development and Tools décrit l’extension Visual Studio [Web Accessibility Checker](https://go.microsoft.com/fwlink/p/?linkid=841539).

#### [<a name="core-accessibility-api-mappings-11"></a>Mappages des API d’accessibilité principales 1.1](https://www.w3.org/TR/core-aam-1.1/)

Ce document de mappage W3C explique comment la sémantique des langages de contenu web est exposée aux API d’accessibilité.  

#### [<a name="easy-checks--a-first-review-of-web-accessibility"></a>Vérifications faciles : premier examen de l’accessibilité web](https://www.w3.org/WAI/eval/preliminary.html)

Une série de vérifications rapides par la FONCTIONNALITÉ DNS qui vous aident à vérifier l’accessibilité d’une page web.

#### [<a name="how-to-meet-wcag-20"></a>Comment rencontrer WCAG 2.0](https://www.w3.org/WAI/WCAG20/quickref/)

Référence rapide aux exigences et techniques WCAG (Web Content Accessibility Guidelines) 2.0 (critères de réussite).

#### [<a name="html-accessibility-api-mappings-10"></a>Mappages d’API d’accessibilité HTML 1.0](https://www.w3.org/TR/html-aam-1.0/)

Ce document de mappages W3C explique comment les éléments et attributs HTML5.1 sont mappages avec les API d’accessibilité de la plateforme.

#### [<a name="quick-tips"></a>Conseils rapides](http://a11yproject.com/#Quick-tips)

Liste des conseils de développement web rapide pour l’accessibilité par [le projet A11Y](http://a11yproject.com/).

#### [<a name="site-scan"></a>Analyse du site](https://developer.microsoft.com/microsoft-edge/tools/staticscan/)

L’outil Analyse du site du Centre de développement Microsoft Edge recherche les bibliothèques, les problèmes de disposition et d’accessibilité.

#### [<a name="techniques-for-wcag-20"></a>Techniques pour WCAG 2.0](https://www.w3.org/TR/WCAG20-TECHS/Overview.html)

Techniques du W3C qui fournissent des conseils aux développeurs web sur la réunion des critères de réussite [WCAG (Web Content Accessibility Guidelines) 2.0.](https://w3.org/TR/WCAG20/)

#### [<a name="tips-on-developing-for-web-accessibility"></a>Conseils sur le développement pour l’accessibilité web](https://w3.org/WAI/gettingstarted/tips/developing.html)

Conseils du W3C sur le développement de contenu web plus accessible aux personnes présentant un handicap.

#### [<a name="wai-aria-authoring-practices-11"></a>PRATIQUES DE AUTHORING ARIA-ARIA 1.1](http://w3c.github.io/aria-practices/)

Document du W3C qui fournit aux lecteurs une compréhension de l’utilisation de LA FONCTION ARIA 1.1 et recommande des approches pour rendre les widgets, la navigation et les comportements accessibles à l’aide des rôles, états et propriétés DE LA FONCTION ARIA.

#### [<a name="wai-guidelines-and-techniques"></a>Instructions et techniques DE LATS](https://w3.org/WAI/guid-tech.html)

Série d’instructions et de normes d’accessibilité web développées par LASL.  

#### [<a name="web-accessibility-evaluation-tools-list"></a>Liste des outils d’évaluation de l’accessibilité web](https://www.w3.org/WAI/ER/tools/index.html)

Liste des outils d’évaluation de l’accessibilité web pour vous aider à déterminer si les sites web respectent les recommandations en matière d’accessibilité.

#### [<a name="web-accessibility-perspectives-explore-the-impact-and-benefits-for-everyone"></a>Perspectives d’accessibilité web : explorer l’impact et les avantages pour tout le monde](https://w3.org/WAI/perspectives/)

Série de courtes vidéos de situation par le W3C sur l’impact de l’accessibilité et les avantages pour tout le monde.

<!-- links -->  

<!--todo: link updates and acrolinx  -->  

[MicrosoftDeveloperEdgeVms]: https://developer.microsoft.com/microsoft-edge/tools/vms "Machines virtuelles | Développeur Microsoft Edge"  

[MicrosoftSupport22798]: https://support.microsoft.com/help/22798 "Guide complet du narrateur | Microsoft Support"  
[MicrosoftSupportWindows414948ba8b1cD3bd86150e5e32204198]: https://support.microsoft.com/windows/414948ba-8b1c-d3bd-8615-0e5e32204198 "Utilisez la Loupe pour faciliter l’affichage des éléments à l’écran | Microsoft Support"  

[AccessibilityinsightsWebOverview]: https://accessibilityinsights.io/docs/web/overview "Informations sur l’accessibilité pour les | Web Informations sur l’accessibilité"  

[AndroidDeveloperDevicesManagingAvdsHtml]: https://developer.android.com/tools/devices/managing-avds.html "Créer et gérer des périphériques virtuels | Développeurs Android"  
[AndroidDeveloperDevicesEmulatorHtml]: https://developer.android.com/tools/devices/emulator.html "Exécuter des applications sur l’émulateur Android | Développeurs Android"  
[AndroidDeveloperSdkInstallingStudioHtml]: https://developer.android.com/sdk/installing/studio.html "Télécharger android Studio | Développeurs Android"  

[AppleAccessibilityMacVision]: https://www.apple.com/accessibility/mac/vision "Accessibilité de la vision - Mac | pomme"  

[AssistivlabsMain]: https://assistivlabs.com "Assistiv Labs"  

[FreedomscientificSoftwareJaws]: https://www.freedomscientific.com/products/software/jaws "JAWS® | Liberté scientifique"  
[FreedomscientificSoftwareZoomtext]: https://www.freedomscientific.com/products/software/zoomtext "ZoomText | Liberté scientifique"  

[GooglePlayStoreAndroidAccessibilitySuite]: https://play.google.com/store/apps/details?id=com.google.android.marvin.talkback "Android Accessibility Suite | GooglePlay Store"  

[NvaccessAboutNvda]: https://www.nvaccess.org/about-nvda "À propos des | NVDA Accès NV"  

[W3cPerspectiveVideosKeyboard]: https://www.w3.org/WAI/perspective-videos/keyboard "Compatibilité du clavier | W3C"  

[WebaimProjectsLowvisionsurvey2]: https://webaim.org/projects/lowvisionsurvey2 "Enquête auprès des utilisateurs ayant une faible vision \#2 résultats | WebAIM"  
[WebaimProjectsScreenreadersurvey8]: https://webaim.org/projects/screenreadersurvey8 "Screen Reader User Survey \#8 Results | WebAIM"  
[WebaimArticlesScreenreaderTesting]: https://webaim.org/articles/screenreader_testing "Test avec les lecteurs d’écran | WebAIM"  
