# <a name="microsoft-edge-documentation"></a>Documentation Microsoft Edge  

## <a name="microsoft-open-source-code-of-conduct"></a>Code de conduite Open Source Microsoft  

Pour plus d’informations sur le code de conduite Open Source de Microsoft, accédez au code de conduite [Open Source de Microsoft.](CODE_OF_CONDUCT.md)  

## <a name="legal-notices"></a>Informations légales  

Microsoft et tous les collaborateurs vous accordent une licence pour accéder à la documentation Microsoft et à d’autres contenus de ce référentiel sous la licence publique internationale [Creative Commons Attribution 4.0,](https://creativecommons.org/licenses/by/4.0/legalcode)accéder au fichier [LICENSE](./LICENSE) et vous octroyer une licence pour tout code dans le référentiel sous la licence [MIT,](https://opensource.org/licenses/MIT)accédez au fichier [LICENSE-CODE.](./LICENSE-CODE)  

Microsoft, Windows, MicrosoftAzure et/ou d’autres produits et services Microsoft référencés dans la présente documentation peuvent être des marques commerciales ou déposées de MicrosoftCorporation aux États-Unis et/ou dans d’autres pays.  
Les licences de ce projet ne vous accordent aucun droit d'utilisation des noms, des logos ou des marques de Microsoft.  
Microsoft general trademark guidelines may be found at [https://go.microsoft.com/fwlink/?LinkID=254653](https://go.microsoft.com/fwlink/?LinkID=254653) .  

Les informations de confidentialité sont disponibles sur [https://privacy.microsoft.com](https://privacy.microsoft.com) .  

Microsoft et tout contributeur se réserve tous les autres droits, en vertu de leurs droits d’auteur, de leurs brevets, ou de leurs marques commerciales respectives, qu'ils soient implicites, par préclusion ou de toute autre manière.  

## <a name="contributing"></a>Contribution  

Il s’agit du référentiel de la documentation Microsoft Edge **hébergée** sur [https://docs.microsoft.com/microsoft-edge](https://docs.microsoft.com/microsoft-edge/index) .  

Si vous souhaitez inclure une nouvelle couverture ou avoir des commentaires, envisagez [de contribuer.](./CONTRIBUTING.md)  Vous pouvez modifier le contenu existant, ajouter un nouveau contenu ou créer de [nouveaux problèmes.](https://github.com/MicrosoftDocs/edge-developer/issues)  L Microsoft Edge’équipe examine vos suggestions et travaille à incorporer ces suggestions dans les documents.  

Recherchez les données de la page web [État](https://developer.microsoft.com/microsoft-edge/status) à l’adresse :  [https://github.com/MicrosoftEdge/Status](https://github.com/MicrosoftEdge/Status) .  La `Status` page web fournit l’état d’implémentation le plus récent et les plans futurs pour les fonctionnalités de plateforme web Microsoft Edge.

### <a name="conventions"></a>Conventions  

*   Lorsque vous ajoutez une page web, vous devez ajouter une entrée pour elle dans [toc.md](./microsoft-edge/toc.yml) pour qu’elle apparaisse.
*   Un répertoire peut contenir d’autres répertoires ou `readme.md` s
*   Les noms de dossier/répertoire sont séparés par des tirets \(par `f12-tools` exemple, \) et minuscules.  Les répertoires sont utilisés dans les URL du `docs.microsoft.com` site.  Évitez d’utiliser des traits de soulignement, des caractères de soulignement ou des caractères camelCase.  

### <a name="other-text-elements"></a>Autres éléments de texte  

Ces autres éléments de texte ont des styles disponibles :  

*   Listes non répertoriées  
*   Avoir des puces régulières  
    *   Vous pouvez également imbribrier des puces.  
    *   Les listes à puces doivent avoir plusieurs entrées.  
*   Disposition standard 
    
1.  Listes ordonnées.  
1.  Utilisez une numérot de style western normal.  
1.  Ne doit être utilisé que lorsqu’une liste a réellement un ordre.  
    
---  

Des règles horizontales sont disponibles.  Utilisez les règles horizontales avec parcimonie pour réduire l’encombrement.  
Évitez d’utiliser des règles horizontales avec des balises de titre ; certains titres utilisent déjà des styles de ligne pour la hiérarchie visuelle.  

### <a name="displaying-code"></a>Affichage du code  

Vous pouvez utiliser la `code` syntaxe inline markdown \(avec les backticks\).  

Vous pouvez également afficher des blocs de code.  L’extrait de code suivant est un exemple css.  

```css
body {
    background: #fff;
}
```  

### <a name="tables"></a>Tableaux  

| Vous pouvez | utiliser des en-têtes | sur les tables |  
|:--- |:--- |:--- |  
| Aligné à gauche | Sauf si un # | 456 |  
| Valeur de texte | Plus de texte | $0.00 |  

### <a name="notes"></a>Remarques  

Utilisez les notes avec parcimonie.  Les blocs sont conçus pour mettre en évidence les informations « à ne pas manquer ».  

Quatre versions de notes différentes sont actuellement styled.  

*   REMARQUE  
*   AVERTISSEMENT  
*   CONSEIL  
*   IMPORTANT  
    
Respectivement, les notes ressemblent aux extraits de code suivants.  

```md
> [!NOTE]
> This is a NOTE  
```  

```md
> [!WARNING]
> This is a WARNING  
```  

```md
> [!TIP]
> This is a TIP  
```  

```md
> [!IMPORTANT]
> This is IMPORTANT  
```  

![Modèles de note](./media/notes.png)

Pour les notes de blockquote à plusieurs lignes, utilisez un caractère supérieur à \( \) devant chaque ligne des notes, tel qu’affiché dans `>` l’exemple suivant.  

```md
> This is a line in a blockquote.  
> My text may wrap to more than one line when the markdown is parsed, but I must include all my information within a single \(sometimes very long line\) in the markdown.  
> This is another line in a blockquote.  
```  

### <a name="images"></a>Images  

Les images doivent être stockées dans un répertoire et référencés avec un `media` chemin d’accès relatif à l’aide d’un script d’image.  

<!--  `![Note patterns](media/notes.png)`  -->  

```md
:::image type="complex" source="./media/notes.png" alt-text="Note patterns" lightbox="./media/notes.png":::
   Note patterns  
:::image-end:::  
```  
