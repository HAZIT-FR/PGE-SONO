# Sonorisation du spectacle pyromusical de Champigneulles

**Association Pyrotechnique du Grand Est (PGE)**  
Spectacle du **6 décembre 2026** · Présentation des moyens disponibles et du renfort envisagé

> [!NOTE]
> Ce dossier présente une **évaluation théorique de couverture sonore**, établie à partir du matériel PGE et du plan de tir. Il ne s'agit ni d'une étude acoustique complète ni de mesures effectuées sur site.

## L'essentiel

Pour accompagner le spectacle demandé par la ville de Champigneulles, PGE dispose déjà d'une installation de sonorisation complète : **deux amplificateurs et six enceintes passives**, dont deux caissons de basses.

**Selon les estimations du dossier initial, cette installation paraît adaptée à la zone de public prévue**, d'environ **90 m de long sur 20 m de profondeur**. Toutefois, la répartition du son sera moins homogène aux extrémités, notamment à l'ouest, et la musique peut être moins perceptible pendant les détonations.

**Notre proposition : conserver cette installation et, si possible, lui ajouter deux amplificateurs et quatre enceintes passives.** Ce renfort vise une meilleure couverture du public ; il n'est pas présenté comme une nécessité démontrée par des mesures.

## Ce que PGE peut fournir

| Matériel disponible | Quantité | Utilité |
|---|---:|---|
| Amplificateurs | **2** | Alimenter l'installation actuelle |
| Enceintes passives | **4** | Diffuser la musique et les annonces |
| Caissons de basses de 18″ | **2** | Renforcer les graves |
| Processeur audio numérique (DSP) | **1** | Régler et répartir les signaux |
| Lecteur COBRA AUDIO BOX et table de mixage | **1 ensemble** | Synchroniser la bande-son et gérer les annonces |

Le système comprend donc **six enceintes au total**. Les deux caissons de basses sont regroupés au centre et les autres enceintes sont réparties sur la ligne de diffusion.

Les amplificateurs représentent une **puissance nominale annoncée cumulée de 3 680 W**, pour **1 900 W RMS** d'enceintes. Ces valeurs caractérisent le matériel, **pas le niveau sonore réellement obtenu dans le public**.

[Voir l'inventaire et les puissances détaillées](docs/annexe-technique.md#matériel-de-lassociation).

## Ce que l'installation permet d'envisager

L'étude initiale prévoit **trois points de diffusion** : un à l'ouest, un au centre et un à l'est. La majeure partie de la zone de public décrite sur le plan est estimée à moins de 25 m d'une enceinte.

**Les points favorables :** l'installation existante constitue une base cohérente pour cette zone délimitée. Les enceintes et caissons sont disponibles au sein de l'association, avec leur chaîne audio et leur traitement numérique.

**Les limites :** la musique peut perdre en présence à mesure que le public s'éloigne. Le dossier estime qu'à environ **40 à 50 m**, elle devient surtout un fond sonore, notamment pendant les bombes de 75 et 100 mm. L'extrémité ouest est la zone la moins favorable.

> [!IMPORTANT]
> **À retenir :** nous pouvons raisonnablement envisager la sonorisation de la zone de public identifiée, **sous réserve de validation sur site**. Nous ne garantissons pas la couverture de l'ensemble du parc ni des spectateurs situés hors de cette zone.

[Consulter les implantations et estimations acoustiques](docs/annexe-technique.md#implantation-indicative).

## Pourquoi proposer un renfort ?

L'objectif n'est pas de remplacer le matériel PGE, mais d'**améliorer la répartition de la musique**, en particulier aux extrémités de la zone prévue.

| Avec le matériel actuel | Avec le renfort envisagé |
|---|---|
| **3 points de diffusion** | **7 points de diffusion** |
| Installation complète déjà disponible | Installation conservée et complétée |
| Couverture théoriquement adaptée à la zone prévue | Couverture potentiellement plus régulière |
| Extrémités plus éloignées des enceintes | Diffusion rapprochée des extrémités |

Le processeur actuel possède **quatre sorties audio disponibles**. Elles peuvent servir à piloter quatre enceintes supplémentaires par l'intermédiaire d'amplificateurs adaptés.

~~~mermaid
%%{init: {"flowchart": {"nodeSpacing": 22, "rankSpacing": 38, "htmlLabels": false}, "theme": "base", "themeVariables": {"fontSize": "14px", "lineColor": "#64748b"}}}%%
flowchart TB
  A["Matériel PGE<br/>2 amplificateurs · 6 enceintes"]
  B["Zone de public prévue<br/>environ 90 m × 20 m"]
  C["Renfort proposé<br/>2 amplificateurs · 4 enceintes"]
  A --> B
  C -. "Meilleure répartition recherchée" .-> B
  classDef current fill:#dbeafe,stroke:#2563eb,color:#172b4d;
  classDef proposed fill:#fff2db,stroke:#d97706,color:#7c2d12;
  classDef audience fill:#ecfdf5,stroke:#059669,color:#14532d;
  class A current;
  class B audience;
  class C proposed;
~~~

*Bleu : matériel disponible · Orange : renfort souhaité · Vert : zone visée. Schéma de principe, non à l'échelle.*

## Matériel complémentaire recherché

### Solution privilégiée : amplification et enceintes passives

- [ ] **2 amplificateurs stéréo**, d'au moins **2 × 500 W sous 8 Ω** chacun.
- [ ] **4 enceintes passives de 8 Ω**, avec supports adaptés.
- [ ] Câbles audio XLR et **1 câble Speakon par enceinte**, à dimensionner selon l'implantation (25 à 50 m envisagés).
- [ ] Protections adaptées contre la pluie.

Un prêt partiel d'**un amplificateur et deux enceintes** reste envisageable si le renfort complet n'est pas disponible.

### Alternative : enceintes actives

En l'absence d'amplificateurs supplémentaires, **deux à quatre enceintes actives de 12″ ou 15″** peuvent aussi être envisagées. Elles exigent alors une **alimentation 230 V à chaque emplacement**, ainsi que les câbles XLR, les pieds et les protections météo nécessaires.

[Comparer les deux options et consulter les branchements](docs/annexe-technique.md#extension-proposée).

## Préparation du spectacle

Avant de valider l'extension, il faudra confirmer la disponibilité du matériel prêté, son implantation exacte, l'alimentation électrique, le cheminement des câbles et la protection contre la pluie.

Le dossier prévoit une **prise dédiée 230 V / 16 A** pour le rack et un **essai sonore d'environ 30 minutes** avant la tombée de la nuit. Les réglages du processeur, les éventuels retards entre enceintes et les niveaux réels devront être contrôlés sur site.

## Documentation

- [Annexe technique](docs/annexe-technique.md) — références complètes, puissances, branchements, schémas d'implantation, hypothèses et logistique.
- [Conventions de rédaction](docs/conventions-redaction.md) — choix éditoriaux et références linguistiques et techniques.

---

<sub>Document de travail PGE · Base documentaire : « Sonorisation – Feu d'artifice de Champigneulles 2026 », version du 7 octobre 2026. Les caractéristiques des équipements sont celles consignées dans le dossier source ; les estimations acoustiques et les implantations sont à confirmer sur place.</sub>
