# Conventions de rédaction

[← Revenir au dossier de sonorisation](../README.md)

Ces conventions s'appliquent à la documentation de **PGE-SONO**. Elles visent la **lisibilité**, l'**exactitude des termes** et une présentation stable sur GitHub.

## Structure et public

- Le `README.md` répond d'abord aux questions d'un décideur : **ce que PGE apporte**, **ce qui est envisagé**, **pourquoi un renfort est souhaité** et **ce qui reste à valider**.
- Les caractéristiques, branchements, puissances, hypothèses et estimations se trouvent dans des **sections repliables du README.md** : un seul document présente l'ensemble du projet.
- Une hypothèse est toujours nommée comme telle. Une donnée constructeur ne devient pas une mesure terrain.

## Typographie et hiérarchie

- Un seul titre principal `#`, puis des sous-titres `##` et `###` sans saut de niveau.
- Titres généraux en **casse naturelle** : « Capacité de sonorisation », « Renfort souhaité ».
- Rubriques d'inventaire en **majuscules** : « TRAITEMENT ET AMPLIFICATION », « ENCEINTES PASSIVES ».
- **Références matérielles en majuscules dans les tableaux** : « THE T.AMP E-1200 », « BEHRINGER EUROLIVE B1520 PRO ». Il s'agit d'un choix d'identification documentaire, non de la graphie commerciale officielle.
- **Gras parcimonieux**, sur la conclusion principale, les quantités demandées, les totaux et les éléments déterminants. Ne pas mettre en gras chaque modèle ou chaque nombre.
- Italique pour les légendes et précisions secondaires. Pas de couleurs ajoutées dans le corps du texte.

## Français et notations

- Employer « **zone de public** » et « **enceintes passives** », et développer les sigles lors de leur première occurrence.
- Écrire un espace avant les symboles d'unité : **500 W**, **8 Ω**, **95 dB**, **25 m**.
- Employer une virgule décimale en français, et une espace insécable dans les milliers lorsque possible : **3 680 W**.
- Employer un deux-points pour expliquer une relation, des listes pour des besoins et des tableaux seulement pour comparer plusieurs caractéristiques.
- Préférer « **puissance d'amplification annoncée** » à « puissance délivrée » sans mesure correspondante.

## Vocabulaire de certitude

| Expression | Signification dans ce dossier |
|---|---|
| Disponible | Matériel appartenant à PGE et recensé dans le dossier |
| Annoncé / constructeur | Caractéristique fournie dans le dossier technique |
| Estimé / théorique | Résultat prévisionnel non validé par une mesure sur site |
| Envisagé / proposé | Renfort souhaité, non acquis |
| À confirmer | Donnée ou condition restant à vérifier avant exploitation |

Les RFC 2119 et 8174 définissent **MUST**, **SHOULD**, **MAY**, etc., pour certains documents normatifs de l'IETF. **Ils ne s'appliquent pas automatiquement à ce dossier**. Nous préférons des formulations françaises explicites (« nécessaire », « recommandé », « optionnel », « à confirmer ») afin d'éviter toute ambiguïté.

## Diagrammes et tableaux

- Utiliser Mermaid pour les chaînes fonctionnelles, avec une disposition **verticale** et des libellés courts pour limiter le débordement latéral.
- Construire les cadres d'équipements sur **trois niveaux lorsque c'est utile** : **catégorie → fonction → référence**. Exemple : `Amplificateurs<br/>Médiums et aigus<br/>THE T.AMP E-1200`.
- Préférer la **classification acoustique vérifiée** aux rôles subjectifs (« principales », « d'appoint ») : une enceinte couvrant plusieurs bandes reste une **enceinte large bande**, même lorsqu'un processeur limite les fréquences qu'elle reçoit. Préciser, si confirmé, le nombre de voies et le diamètre du haut-parleur.
- Dans les schémas de distribution, donner **la même couleur à chaque exemplaire d'un même modèle** et indiquer la quantité correspondante dans la légende : 2 B1520 PRO, 2 A12, 2 VP1800S. Garder des couleurs distinctes pour les autres familles (commande, traitement, amplificateurs).
- Conserver le **schéma principal visible au début de la section sur le matériel** ; rassembler **toutes les données techniques dans une seule fiche autonome et repliable**, y compris les modèles, quantités, puissances et branchements déjà présents dans le schéma. Éviter les doublons **à l'intérieur** de cette fiche.
- Structurer le dossier technique selon **trois étapes lisibles** : **installation existante (moyens PGE)** → **problématique de couverture à Champigneulles** → **solution de renforcement et conditions de mise en œuvre**. Préférer ces intitulés concrets aux termes scolaires « thèse, antithèse, synthèse » et ne pas multiplier les tableaux de bilan redondants.
- Pour afficher une **capacité de raccordement future non utilisée** sans désaligner l'arbre audio, privilégier un **petit encadré Mermaid séparé, sans lien ni nœud invisible**, immédiatement après le schéma. Utiliser une bordure pointillée et une teinte distincte ; préciser qu'il s'agit d'une réserve, non d'enceintes réellement raccordées.
- **Un retour à la ligne dans un cadre marque un changement de catégorie d'information**, jamais une coupure arbitraire d'un nom de modèle ou d'un numéro de référence. Exemple : `Mixage<br/>JCB NSA 2008`, et non `Mixage · JCB NSA 2008` qui peut être coupé en `JCB NSA / 2008`.
- Dans les blocs Mermaid, utiliser un saut de ligne explicite (`<br/>`) **entre la fonction et la référence** ; conserver l'intégralité du modèle sur une même ligne et prévoir assez de largeur pour éviter les retours automatiques.
- Pour représenter les supports, placer **un seul cadre enfant sous l'équipement qui reçoit directement le support** : « TRÉPIED AU SOL » sous chaque B1520 PRO et « MÂT DE COUPLAGE » sous chaque caisson VP1800S (le mât porte l'A12 correspondante). Ne pas répéter le nom de l'équipement ni multiplier les liens ; utiliser des traits pleins.
- **Un équipement physique distinct = un cadre distinct** lorsque le but est de montrer les branchements : représenter les deux B1520 PRO et les deux A12 séparément, sous leur canal gauche ou droit, plutôt que `2 B1520 PRO + 2 A12` dans un cadre.
- Préférer un **arbre hiérarchique** : source → mixage → traitement → amplificateur → canal → enceinte. Les diagrammes de localisation peuvent regrouper des matériels situés au même emplacement.
- Sur le schéma de câblage, représenter **chaque liaison une seule fois** : flèches **pointillées pour la radio et l'audio**, traits **pleins pour les supports**. Conserver les références techniques **sur une seule ligne dans les cadres**, sans y ajouter les libellés de prises. Pour distinguer **sortie et entrée**, écrire une **étiquette courte directement sur la flèche**, selon le sens du signal : `RCA → LINE 1` ou `REC OUT → INPUT` ; pour des prises de même type des deux côtés, un libellé simple comme `XLR` suffit. Sur les **liaisons finales vers les enceintes**, afficher directement la sortie physique du rack et le côté (`SYSTEM OUT L/R` vers B1520 PRO/TOP, `TOP OUT L/R` vers A12/MID, `SUB OUT L/R` vers VP1800S/SUB). Ne pas répéter ces libellés entre amplificateur et canal. **Aucun nœud intermédiaire invisible ni flèche doublée** : ils augmentent inutilement la taille du diagramme.
- Utiliser les termes compréhensibles par un non-spécialiste : **« poste de tir »** plutôt que « pupitre », et **« télécommunications radio (antenne) »** pour préciser la liaison sans fil.
- Regrouper les éléments techniques sous des sections HTML **`<details>`** avec un titre explicite **`<summary>`**, ouvertes à la demande par chevron GitHub.
- Dans la fiche technique, utiliser quelques **repères de couleur compatibles avec GitHub** dans les titres et, si pertinent, devant les modèles (commande gris, traitement orange, amplification bleu, enceintes vert/jaune/violet). Ils complètent les noms explicites sans remplacer l’information.
- Lorsque plusieurs familles techniques figurent dans la fiche, préférer **un seul tableau façon tableur**, avec des lignes d'en-tête de catégorie sur toute la largeur (`colspan`) et des séparateurs doubles visibles (`═══`) compatibles GitHub. Garder les caractéristiques de chaque équipement dans une seule ligne de tableau et éviter les doublons internes.
- Pour les **valeurs de puissance, d'impédance et de sensibilité**, rendre chaque expression entière insécable dans les cellules HTML (`&nbsp;`, et caractère de liaison `&#8288;` après la barre oblique si nécessaire). Exemple : `2&nbsp;×&nbsp;850&nbsp;W&nbsp;/&#8288;&nbsp;8&nbsp;Ω`. **Ne pas bloquer toute la cellule** lorsqu'elle contient deux caractéristiques distinctes : le retour à la ligne peut intervenir au séparateur `;`, jamais au milieu d'une valeur.
- Dans les en-têtes de tableau, empêcher les coupures des libellés courts avec des **espaces insécables** (exemple : `Détails&nbsp;techniques`).
- **Une information = une ligne visuelle dans la colonne « Détails techniques »** : séparer les fonctions et caractéristiques distinctes par `<br/>` dans la cellule HTML, sans multiplier les lignes du tableau. Exemple : `Poste de tir<br/>Synchronisation radio ↔ COBRA&nbsp;AUDIO&nbsp;BOX`. Garder les références et valeurs techniques entières sur leur ligne, sans les scinder au milieu. Les groupes naturellement liés (ex. types de sortie) peuvent rester sur une même ligne.
- **Largeur et retours à la ligne :** attribuer des largeurs indicatives aux quatre colonnes (équipement 33 %, quantité 7 %, puissance/impédance 25 %, détails 35 %), raccourcir les en-têtes et maintenir chaque **nom complet de modèle sur une même ligne** avec des espaces insécables (`&nbsp;`). Réserver les retours à la ligne volontaires aux informations d'une autre catégorie ; laisser les descriptions longues se répartir naturellement.
- Ne pas ajouter de légende lorsque les libellés des cadres suffisent à comprendre le schéma. Si une légende est nécessaire, elle doit apporter une information non indiquée dans le diagramme ; ne jamais s'appuyer seulement sur les couleurs.
- Écrire les **catégories de la première ligne des cadres en majuscules et en gras** (balise Mermaid HTML `<b>...</b>`, avec `htmlLabels: true`) (ex. `LECTURE AUDIO`, `AMPLIFICATEURS`) et conserver le nom complet du fabricant et du modèle sur la ligne de référence (ex. `BEHRINGER EUROLIVE B1520 PRO`).
- Mentionner « schéma de principe » lorsqu'un diagramme n'est pas à l'échelle.
- Donner au maximum trois ou quatre colonnes aux tableaux visibles dans le README ; placer les données détaillées dans une section repliable au sein du README.
- Mettre les valeurs numériques comparables dans la même colonne et alignées à droite.

## Références éditoriales

Les recommandations citées ne sont pas toutes des règles obligatoires ; elles servent de **référentiel volontaire** pour cette documentation.

1. [OQLF — Majuscule aux titres](https://vitrinelinguistique.oqlf.gouv.qc.ca/21497/la-typographie/majuscules/emploi-de-la-majuscule-pour-des-types-de-denominations/majuscule-aux-titres-doeuvres-et-douvrages).
2. [OQLF — Symboles d'unités de mesure](https://vitrinelinguistique.oqlf.gouv.qc.ca/21401/les-abreviations-et-les-symboles/les-symboles/ecriture-des-symboles-dunites-de-mesure).
3. [BIPM — Brochure sur le SI](https://www.bipm.org/fr/publications/si-brochure).
4. [Google — Rédaction des titres](https://developers.google.com/style/headings) et [des tableaux](https://developers.google.com/style/tables).
5. [GitHub — Tableaux Markdown](https://docs.github.com/fr/get-started/writing-on-github/working-with-advanced-formatting/organizing-information-with-tables) et [diagrammes Mermaid](https://docs.github.com/fr/get-started/writing-on-github/working-with-advanced-formatting/creating-diagrams).
6. [RFC 7322 — RFC Style Guide](https://www.rfc-editor.org/rfc/rfc7322), [RFC 2119](https://www.rfc-editor.org/rfc/rfc2119) et [RFC 8174](https://www.rfc-editor.org/rfc/rfc8174).
