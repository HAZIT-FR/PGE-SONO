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
- **Un retour à la ligne dans un cadre marque un changement de catégorie d'information**, jamais une coupure arbitraire d'un nom de modèle ou d'un numéro de référence. Exemple : `Mixage<br/>JCB NSA 2008`, et non `Mixage · JCB NSA 2008` qui peut être coupé en `JCB NSA / 2008`.
- Dans les blocs Mermaid, utiliser un saut de ligne explicite (`<br/>`) **entre la fonction et la référence** ; conserver l'intégralité du modèle sur une même ligne et prévoir assez de largeur pour éviter les retours automatiques.
- **Un équipement physique distinct = un cadre distinct** lorsque le but est de montrer les branchements : représenter les deux B1520 PRO et les deux A12 séparément, sous leur canal gauche ou droit, plutôt que `2 B1520 PRO + 2 A12` dans un cadre.
- Préférer un **arbre hiérarchique** : source → mixage → traitement → amplificateur → canal → enceinte. Les diagrammes de localisation peuvent regrouper des matériels situés au même emplacement.
- Utiliser les termes compréhensibles par un non-spécialiste : **« poste de tir »** plutôt que « pupitre », et **« télécommunications radio (antenne) »** pour préciser la liaison sans fil.
- Regrouper les éléments techniques sous des sections HTML **`<details>`** avec un titre explicite **`<summary>`**, ouvertes à la demande par chevron GitHub.
- Expliquer la légende en **texte**, sans s'appuyer seulement sur les couleurs.
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
