---
description: Informations sur la vérification de la signature GPG pour les outils Selenium pour Microsoft Edge de publication.
title: Vérification des téléchargements des outils Selenium pour Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, développement web, html, css, javascript, développeur, webdriver, selenium, test, outils, automatisation, test
ms.openlocfilehash: cf5889ab3c5f1ca89579a398a232716008144562
ms.sourcegitcommit: 070a60f634908eea0e29e260331f9fc0aa85ee78
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2021
ms.locfileid: "11306270"
---
# Vérifier les téléchargements des outils Selenium pour Microsoft Edge  

Cet article fournit la clé publique à utiliser lors de la vérification de la signature des releases des outils [Selenium pour Microsoft Edge][GithubMicrosoftEdgeSeleniumToolsReleases].  

Les [Java de][MavernSearchArtifactComMicrosoftEdgeMsedgeSeleniumToolsJava] [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumToolsReleases] sont signées à l’aide de [GPG][Gnupg].  

Utilisez les clés suivantes pour vérifier la signature des packages fournis par [l’équipe Microsoft Edge outils de développement.][TwitterEdgeDevTools]  

## Clé publique pour la vérification des outils Selenium pour Microsoft Edge  

*   **ID de clé publique**: Microsoft Edge d’équipe outils [de développement EdgeDevToolsOSS@microsoft.com](mailto:edgedevtoolsoss@microsoft.com)  
*   **Empreinte numérique à clé publique**: `46EE EB3F 4028 B5CE A4E8  E6F5 A6DC D211 6D3A 3A7A`  

```output
-----BEGIN PGP PUBLIC KEY BLOCK-----
Version: BSN Pgp v1.1.0.0

mQENBF+kejUBCADrcWxP0f40IncaJBzQtrmo8n6yXDwiM6eyTBQC4V77n+YWBFkd
qsUhcAJXJ+1wa5TwJaRu0OalLy7A6HD7TdJWNCF0Eaktw8ESWZ61M6VN7/yx/8W6
KAjaCIFQybsZzj5PtR7zYooFHlkZ/rbK19rv4E5v27rbv5w8Awu+F2PMNdsMm/iJ
PMggN2di/gqyOqBOe/9aXgjHAMPp1stbCMEr/i6VF5Ze++Sjfpi2WrrrXFcoyZav
9Ieq9QkeM8gxFiYyO9BL7bUEuBCwyefyBTdrIMoypounxVpylImbSJXyBsUnfGRZ
suYAXo6bSYs9w56/oFNtrz3oxzNTq0Hi63PHABEBAAG0Q01pY3Jvc29mdCBFZGdl
IERldmVsb3BlciBUb29scyBUZWFtIDxFZGdlRGV2VG9vbHNPU1NAbWljcm9zb2Z0
LmNvbT6JATgEEwEIACIFAl+kejUCGwMGCwkIBwMCBhUIAgkKCwQWAgMBAh4BAheA
AAoJEKbc0hFtOjp6Qw8H/j4b8DecNJmiVvK79+jaI2WtAEcLViYj1tCLCZB6UKIi
4fA6PeTtMoevsvcm0iXTNaZFXtBabj1z8efXUbK3qQlmSlkWoK4gv/3Zn+sPbg1t
SjGBmFLmmHIjM2LpomZfHa3zJV1FDE6o8KOQhoQt9G7V//rG0Y5xBdjgSoXK0y/7
4R1vhbSrpbuhzGA+7/ACbrhWpLJ3cJ3BErW/lscTGaCaT6ZizrFJFjIlZxgJHqu3
ptJfPKT84TtqmRoJApBgxAsnD4t4JiuvnHkYHgzAzwcXFiofj2cCeJZf1tzIk6+Z
1lg+9MXF2PDDom1+ieCUBXFdRq6fMKldXM0V7yBOUeY=
=0iMW
-----END PGP PUBLIC KEY BLOCK-----
```  

<!-- links -->  

[GithubMicrosoftEdgeSeleniumToolsReleases]: https://github.com/microsoft/edge-selenium-tools/releases "microsoft/edge-selenium-tools | GitHub"  

[Gnupg]: https://gnupg.org "La protection de la confidentialité GNU | GnuPG"  

[MavernSearchArtifactComMicrosoftEdgeMsedgeSeleniumToolsJava]:https://search.maven.org/artifact/com.microsoft.edge/msedge-selenium-tools-java "com.microsoft.edge:msedge-selenium-tools-java | sonatype Maven Central Repository Search"  

[TwitterEdgeDevTools]: https://twitter.com/edgedevtools "Microsoft Edge DevTools | Twitter"  
