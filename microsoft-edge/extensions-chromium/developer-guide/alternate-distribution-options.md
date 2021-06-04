---
description: Découvrez comment distribuer des extensions à l’aide d’autres méthodes qui n’utilisent pas de magasins vérifiés
title: Autre méthode de distribution des extensions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, développement d’extensions, extensions de navigateur, extensions, extensions, centre de partenaires, développeur
ms.openlocfilehash: 3b2c72e13488632e2fadea2a7e8eb95888f67170
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343149"
---
# Autres méthodes de distribution d’extension  

En règle générale, les extensions sont distribuées par le biais Microsoft Edge magasin d’extensions. Dans certains scénarios, les développeurs peuvent avoir besoin de distribuer des extensions à l’aide d’autres méthodes. Par exemple :

1.  L’extension est associée à d’autres logiciels et doit être installée avec le reste du logiciel groupé.   
1.  Les administrateurs réseau souhaitent distribuer une extension dans toute leur organisation.   

Les extensions qui ne sont pas chargées à partir du magasin d’extensions Edge sont appelées extensions installées en externe. La liste suivante fournit d’autres méthodes de distribution des extensions installées en externe. 

*   Utilisez le Windows registre (Windows uniquement).  
*   Utilisez un fichier JSON de préférences (macOS et Linux).  
    
##  <a name="before-you-begin"></a>Avant de commencer  

Veillez à publier votre extension dans le magasin d’extensions Microsoft Edge ou à mettre en package un fichier et assurez-vous qu’il s’installe `.crx` correctement sur votre ordinateur.  Si vous installez le `.crx` fichier à l’aide de la , assurez-vous que vous `update_URL` pouvez accéder à votre extension à cette URL.  

Assurez-vous également que vous avez les informations suivantes.    

1.  Chemin d’accès du `.crx` fichier ou de votre `update_URL` extension.
1.  Version de votre extension.  Les informations de version sont disponibles dans votre fichier manifeste ou dans Microsoft Edge après le chargement de `edge://extensions` l’extension packaisée.   
1.  ID de votre extension.  Les informations d’ID sont disponibles dans Microsoft Edge une fois que `edge://extensions` vous avez chargé l’extension packée.  

> [!NOTE] 
> Les exemples `1.0` suivants utilisent la version et `aaaaaaaaaabbbbbbbbbbcccccccccc` l’ID.  

##  <a name="use-the-windows-registry-(windows-only)"></a>Utiliser le Windows registre (Windows uniquement)  

Pour distribuer votre extension à l’aide Windows registre, effectuez les étapes suivantes.

1.  Recherchez ou créez la clé suivante dans le Registre :  
    *   32 bits Windows : `HKEY_LOCAL_MACHINE\Software\Microsoft\Edge\Extensions` .  
    *   64 bits Windows : `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Edge\Extensions` .  
1.  Créez une clé ou un dossier sous **Extensions** avec le même nom que l’ID de votre extension. Par exemple, créez la clé avec le nom `aaaaaaaaaabbbbbbbbbbcccccccccc` .  
1.  Dans la **clé Extensions,** créez `update_url` la propriété et définissez la valeur sur `https://edge.microsoft.com/extensionwebstorebase/v1/crx` .  La propriété pointe vers le fichier de votre extension dans le `update_url` `.crx` magasin Microsoft Edge modules supplémentaires.  

    ```json
    {
        "update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
    }
    ```  
    
    > [!NOTE]
    > Si vous souhaitez installer une extension à partir du Chrome Web Store, définissez la valeur `update_url` de `https://clients2.google.com/service/update2/crx` .  
  
1.  Vérifiez que votre extension est répertoriée dans Microsoft Edge en naviguant vers `edge://extensions` .  

##  <a name="use-a-preferences-json-file-(macos-and-linux)"></a>Utiliser un fichier JSON de préférences (macOS et Linux)  

Pour distribuer votre extension à l’aide d’un fichier JSON de préférences, effectuez les étapes suivantes.

1.  Lorsque vous utilisez Linux, assurez-vous que votre fichier d’extension est disponible sur l’ordinateur où `.crx` l’extension sera installée. Copiez le fichier d’extension dans un répertoire local ou utilisez un partage réseau `.crx` accessible à partir de l’ordinateur. 
1.  Créez un fichier JSON où le nom du fichier correspond à l’ID de votre extension. Par exemple, créez un fichier JSON avec le nom de fichier `aaaaaaaaaabbbbbbbbbbcccccccccc.json` .  
1.  Selon votre système d’exploitation, enregistrez le fichier JSON dans l’un des dossiers suivants.   
    *   **macOS**  
        *   Spécifiques à l’utilisateur : `~USERNAME/Library/Application Support/Microsoft Edge/External Extensions/`  
        *   Tous les utilisateurs : `/Library/Application Support/Microsoft/Edge/External Extensions/`  
        
        Pour empêcher les utilisateurs non autorisés d’installer des extensions pour tous les utilisateurs, assurez-vous que votre fichier d’extension est en lecture seule. En outre, assurez-vous que les conditions suivantes sont remplies :
        
        *   Chaque répertoire du chemin d’accès appartient à la racine de l’utilisateur.  
        *   Chaque répertoire du chemin d’accès est affecté au `admin` ou au `wheel` groupe.  
        *   Tous les répertoires du chemin d’accès ne sont pas accessibles en création.  
        *   Le chemin d’accès doit également être exempt de liens symboliques.  
        
    *   **Linux**  
        *   Spécifiques à l’utilisateur : `~/.config/microsoft-edge/External Extensions/`  
        *   Tous les utilisateurs : `/usr/share/microsoft-edge/extensions/`  
1.  Selon votre scénario, copiez le code approprié qui suit dans votre fichier JSON. 
    *   S’applique uniquement à Linux. Si vous installez à partir d’un fichier, spécifiez l’emplacement et la version à `external_crx` l’aide et `external_version` .  
            
        ```json
        {
            "external_crx": "/home/share/extension.crx",
            "external_version": "1.0"
        }
        ```  

    *   S’applique à macOS et Linux. Si vous installez à partir `update_URL` d’un , spécifiez l’URL de mise à jour à l’aide `external_update_url` . 
        
        Copiez le code suivant dans votre fichier JSON lors de l’installation à partir de fichiers locaux `.crx` sur Linux uniquement.  
    
        ```json
        {
            "external_update_url": "http://myhost.com/mytestextension/updates.xml"
        }
        ```  
 
    *  Copiez le code suivant dans votre fichier JSON lors de l’installation à partir du magasin Microsoft Edge sur macOS et Linux.
    
        ```json
        {
            "external_update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
        }
        ```  
    
1.  Pour installer des extensions pour des paramètres régionaux spécifiques, listez les paramètres régionaux pris en charge à l’aide `supported_locale` de .  Vous pouvez également spécifier des paramètres régionaux parents pour installer votre extension pour tous les paramètres régionaux de langue qui utilisent ce parent. Par exemple, lorsque vous utilisez les paramètres régionaux parents, votre extension s’installe pour tous les paramètres régionaux anglais, tels `en` que , et ainsi de `en-US` `en-GB` suite.  Lorsque les utilisateurs modifient leurs paramètres régionaux dans leur navigateur, les extensions installées en externe sont désinstallées.  Pour installer votre extension pour tous les paramètres régionaux, n’utilisez pas `supported_locales` .  

    ```json
    {
        "external_update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx",
        "supported_locales": [ "en", "fr", "de" ]
    }
    ```  

1.  Vérifiez que votre extension est installée dans Microsoft Edge en naviguant vers `edge://extensions` .  

##  <a name="update-and-uninstall-externally-installed-extensions"></a>Mettre à jour et désinstaller les extensions installées en externe

Microsoft Edge analyse les entrées de métadonnées dans le Registre chaque fois que le navigateur démarre et modifie les extensions installées en externe.  

Pour mettre à jour votre extension vers une nouvelle version, mettez à jour la version dans le fichier manifeste, puis mettez à jour la version dans le Registre.  

Vous devrez peut-être désinstaller les extensions installées en externe, qui ont été installées dans le cadre d’un ensemble de logiciels précédemment installé sur l’ordinateur.  Pour désinstaller votre extension, supprimez votre fichier JSON de préférences ou supprimez la clé du Registre.   

<!-- links -->  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  La page d’origine se trouve [ici.](https://developer.chrome.com/apps/external_extensions)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
