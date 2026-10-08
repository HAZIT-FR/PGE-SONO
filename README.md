# Sonorisation du spectacle pyromusical de Champigneulles

**Association Pyrotechnique du Grand Est (PGE)**  
**6 décembre 2026** · Présentation du système disponible et du renfort souhaité

> [!NOTE]
> Les performances et implantations présentées sont **théoriques** : elles proviennent du dossier PGE du 7 octobre 2026. Il ne s'agit ni de mesures réalisées sur place ni d'une garantie de couverture acoustique.

## 1. Synthèse du projet

PGE dispose déjà d'un système de sonorisation complet pour accompagner le spectacle demandé par la ville de Champigneulles : **2 amplificateurs, 4 enceintes de diffusion et 2 caissons de basses**.

**En théorie, ce système paraît adapté à la zone de public prévue**, d'environ **90 m × 20 m**. Néanmoins, la musique risque d'être moins présente aux extrémités de la zone, notamment à l'ouest, et lors des détonations.

**L'amélioration proposée consiste à ajouter 2 amplificateurs et 4 enceintes passives**, sans remplacer le matériel de l'association. L'objectif est d'obtenir une diffusion **plus régulière**, avec davantage de points de sonorisation.

| | Installation PGE | Avec le renfort envisagé |
|---|---:|---:|
| Amplificateurs | **2** | **4** |
| Enceintes, caissons compris | **6** | **10** |
| Points de diffusion | **3** | **7** |
| Disponibilité | Matériel PGE | Sous réserve de prêt |

> [!IMPORTANT]
> **Position de PGE :** le système actuel pourrait suffire à sonoriser la zone identifiée sur le plan de tir. Le renfort de **2 amplificateurs et 4 enceintes** est **souhaitable pour améliorer la couverture**, et non indispensable sur la seule base des estimations disponibles.

## 2. Matériel actuellement disponible

L'association possède l'ensemble de la chaîne nécessaire : lecture de la bande-son, mixage, traitement du signal, amplification et diffusion.

| Famille | Équipements | Quantité |
|---|---|---:|
| Amplification | THE T.AMP E-1200 et E-1500 | 2 |
| Enceintes de diffusion | BEHRINGER B1520 PRO et AUDIOPHONY A12 | 4 |
| Caissons de basses | BEHRINGER VP1800S, 18″ | 2 |
| Traitement audio | THE T.RACKS FIR DSP 408 | 1 |
| Commande audio | COBRA AUDIO BOX et tables de mixage | Ensemble disponible |

**Puissances annoncées :** 3 680 W d'amplification cumulée pour 1 900 W RMS d'enceintes. Ces puissances sont des caractéristiques nominales du matériel ; elles **ne sont pas des niveaux sonores mesurés dans le public**.

<details>
<summary><strong>Afficher l'inventaire complet et les caractéristiques du matériel</strong></summary>

### TRAITEMENT ET AMPLIFICATION

| Équipement | Qté | Fonction |
|---|---:|---|
| THE BOX PRO AMPRACK MK II | 1 | Rack mobile avec processeur, amplificateurs et connectique |
| THE T.RACKS FIR DSP 408 | 1 | Routage, filtrage FIR, égalisation et limiteurs |
| THE T.AMP E-1200 | 1 | Amplification des médiums et aigus |
| THE T.AMP E-1500 | 1 | Amplification des graves |

| Modèle | Caractéristiques annoncées |
|---|---|
| FIR DSP 408 | 4 entrées, 8 sorties XLR ; **4 sorties utilisées et 4 disponibles** |
| E-1200 | **2 × 990 W sous 4 Ω** ; 2 × 680 W sous 8 Ω ; classe H |
| E-1500 | **2 × 850 W sous 8 Ω** ; 2 × 1 220 W sous 4 Ω ; classe H |
| AMPRACK MK II | 230 V ; entrées et renvois XLR ; sorties Speakon System / Top / Sub |

### ENCEINTES PASSIVES

| Modèle | Qté | RMS | Impédance |
|---|---:|---:|---:|
| BEHRINGER EUROLIVE B1520 PRO | 2 | **300 W** | 8 Ω |
| AUDIOPHONY A12 | 2 | **250 W** | 8 Ω |
| BEHRINGER EUROLIVE VP1800S | 2 | **400 W** | 8 Ω |

| Modèle | Caractéristiques complémentaires |
|---|---|
| B1520 PRO | 15″ + 1,75″ ; 96 dB (1 W / 1 m) ; 1 200 W crête ; 27 kg |
| A12 | 3 voies, 12″ ; 99 dB (1 W / 1 m) ; 500 W crête ; 14 kg |
| VP1800S | Caisson 18″, 40–200 Hz ; 100 dB (1 W / 1 m) ; 1 600 W crête ; 41 kg |

### PILOTAGE ET ACCESSOIRES

| Équipement | Qté | Utilisation |
|---|---:|---|
| COBRA AUDIO BOX | 1 | Lecture MP3 sur clé USB ; synchronisation radio ; sorties casque, RCA et jack 6,35 mm |
| JCB NSA 2008 | 1 | Table de mixage principale, 6 voies dont 1 pour le micro |
| BEHRINGER XENYX 302USB | 1 | Table de mixage de secours, 5 voies |
| TRÉPIEDS ET MÂTS | 4 | Mise en hauteur des enceintes, embase de 35 mm |

</details>

<details>
<summary><strong>Afficher la chaîne audio et les branchements actuels</strong></summary>

La **COBRA AUDIO BOX**, synchronisée par radio avec le pupitre de tir COBRA 18R2, transmet la bande-son à la table de mixage. Le processeur répartit ensuite les graves et les médiums/aigus vers les amplificateurs.

~~~mermaid
%%{init: {"flowchart": {"nodeSpacing": 22, "rankSpacing": 32, "htmlLabels": false}, "theme": "base", "themeVariables": {"fontSize": "13px", "lineColor": "#64748b"}}}%%
flowchart TB
  A["Pupitre COBRA 18R2"]
  B["COBRA AUDIO BOX"]
  C["Table JCB NSA 2008"]
  D["FIR DSP 408"]
  E["E-1200 · médiums et aigus"]
  F["E-1500 · graves"]
  G["2 B1520 PRO + 2 A12"]
  H["2 caissons VP1800S"]
  A -. "Radio" .-> B
  B --> C --> D
  D --> E --> G
  D --> F --> H
  classDef source fill:#f1f5f9,stroke:#64748b,color:#172b4d;
  classDef processing fill:#dbeafe,stroke:#2563eb,color:#172b4d;
  classDef output fill:#ecfdf5,stroke:#059669,color:#14532d;
  class A,B,C source;
  class D,E,F processing;
  class G,H output;
~~~

*Schéma fonctionnel simplifié, non représentatif du cheminement de chaque câble.*

- **E-1200 :** 1 B1520 PRO et 1 A12 en parallèle par canal, soit 4 Ω nominaux par canal.
- **E-1500 :** 1 caisson VP1800S par canal, sous 8 Ω.
- **DSP :** 4 sorties affectées à l'installation actuelle ; sorties **5 à 8 disponibles** pour le renfort.

> [!IMPORTANT]
> Les sorties libres du DSP sont des **sorties de signal** : elles ne peuvent pas alimenter directement des enceintes passives.

</details>

## 3. Capacité de couverture estimée

L'implantation prévue comprend **trois points de diffusion** : deux points latéraux avec les B1520 PRO et un point central avec les deux caissons VP1800S et les deux A12.

La zone de public prise en compte représente environ **90 m de long et 20 m de profondeur** (dimensions variables sur le plan : **90 à 95 m × 15 à 23 m**). D'après le dossier initial, la plupart des spectateurs de cette zone seraient situés à moins de **25 m** d'une enceinte.

**Limite principale :** au-delà d'environ **40 à 50 m**, la musique pourrait devenir un simple fond sonore, surtout pendant les tirs de bombes de **75 et 100 mm**. L'extrémité ouest paraît la moins bien couverte.

<details>
<summary><strong>Afficher les implantations : système actuel et extension proposée</strong></summary>

Les schémas ci-dessous représentent l'ordre des points d'ouest en est, **de haut en bas pour rester lisibles sur téléphone**. Les lignes ne représentent pas des liaisons audio et les distances ne sont pas à l'échelle.

### Installation actuelle — 3 points de diffusion

~~~mermaid
%%{init: {"flowchart": {"nodeSpacing": 25, "rankSpacing": 26, "htmlLabels": false}, "theme": "base", "themeVariables": {"fontSize": "13px"}}}%%
flowchart TB
  O["OUEST · B1520 PRO"]
  C["CENTRE · 2 VP1800S + 2 A12"]
  E["EST · B1520 PRO"]
  O --- C --- E
  classDef installed fill:#dbeafe,stroke:#2563eb,color:#172b4d;
  class O,C,E installed;
~~~

Les **deux caissons regroupés au centre** peuvent se renforcer dans les graves (gain théorique évoqué d'environ **6 dB**). Les A12 sont orientées de part et d'autre du centre.

### Extension souhaitée — 7 points de diffusion

~~~mermaid
%%{init: {"flowchart": {"nodeSpacing": 18, "rankSpacing": 20, "htmlLabels": false}, "theme": "base", "themeVariables": {"fontSize": "13px"}}}%%
flowchart TB
  P1["P1 · renfort ouest"]
  O["B1520 PRO · ouest"]
  P2["P2 · renfort ouest"]
  C["CENTRE · 2 caissons + 2 A12"]
  P3["P3 · renfort est"]
  E["B1520 PRO · est"]
  P4["P4 · renfort est"]
  P1 --- O --- P2 --- C --- P3 --- E --- P4
  classDef installed fill:#dbeafe,stroke:#2563eb,color:#172b4d;
  classDef proposed fill:#fff2db,stroke:#d97706,color:#7c2d12;
  class O,C,E installed;
  class P1,P2,P3,P4 proposed;
~~~

*Bleu : points de diffusion existants. Orange : renforts souhaités P1 à P4.*

L'emplacement des enceintes était envisagé **1 à 2 m devant la barrière**, côté tir, en dehors des cercles de **30 m** du tir bas calibre. **Toute implantation doit être vérifiée et validée au regard du plan de sécurité.**

</details>

<details>
<summary><strong>Afficher les calculs de puissance et les estimations acoustiques</strong></summary>

### Puissances nominales

| Circuit | Amplification annoncée | Enceintes |
|---|---:|---:|
| Médiums et aigus : 2 canaux, 4 Ω | 1 980 W | 1 100 W RMS |
| Graves : 2 canaux, 8 Ω | 1 700 W | 800 W RMS |
| **Total** | **3 680 W** | **1 900 W RMS** |

Les rapports de puissance annoncés sont de **× 1,8** pour les médiums/aigus, de **× 2,1** pour les graves et d'environ **× 1,9** globalement. Cette réserve ne dispense pas d'un réglage correct des **filtres, limiteurs et niveaux**.

### Estimation de niveau sonore avec une B1520 PRO

Les valeurs suivantes proviennent du dossier initial : elles concernent **une enceinte B1520 PRO à pleine puissance, en champ libre**, et non le niveau global du système.

| Distance | Niveau théorique | Interprétation |
|---|---:|---|
| 5 m | **107 dB** | Niveau élevé, à éviter au premier rang |
| 10 m | 101 dB | Musique très présente |
| 20 à 25 m | 93 à 95 dB | Musique bien présente |
| 50 m | 87 dB | Peut être masquée par les détonations |
| 100 m | 81 dB | Fond sonore |

**Hypothèses du dossier :** décroissance approximative de **6 dB par doublement de distance**, contribution éventuelle de plusieurs enceintes, incertitude annoncée de **± 3 dB**. Le dossier mentionne aussi les effets de l'humidité, des arbres et du public.

La cible prévisionnelle mentionnée est d'environ **95 dB au milieu du public**, sans mesure correspondante sur site.

Le dossier d'origine cite une référence de **102 dB(A) sur 15 minutes** au titre du décret n° 2017-1244. Cette mention ne vaut **pas validation du cadre réglementaire applicable** à la manifestation : les obligations et niveaux devront être vérifiés par l'organisateur.

> [!WARNING]
> Ces chiffres sont des **ordres de grandeur théoriques**. Ils ne garantissent pas la couverture de tout le parc ni des spectateurs hors de la zone prévue.

</details>

## 4. Renfort proposé à la commune ou à un partenaire

L'objectif est d'améliorer la **répartition de la musique**, notamment aux extrémités, sans modifier l'architecture du système existant.

### Solution privilégiée — amplificateurs et enceintes passives

- [ ] **2 amplificateurs stéréo**, délivrant au moins **2 × 500 W sous 8 Ω** chacun.
- [ ] **4 enceintes passives de 8 Ω**, avec supports adaptés.
- [ ] Câbles audio XLR et **1 câble Speakon par enceinte** (25 à 50 m selon implantation).
- [ ] Protections contre la pluie pour le matériel.

**Un renfort partiel** avec un amplificateur et deux enceintes reste envisageable.

### Alternative — enceintes actives

Si des amplificateurs et enceintes passives ne sont pas disponibles, il est possible d'envisager **2 à 4 enceintes actives de 12″ ou 15″**, avec pieds, câbles XLR de 25 à 50 m, alimentation 230 V à chaque emplacement et protections contre la pluie.

<details>
<summary><strong>Afficher le comparatif technique des deux solutions</strong></summary>

| Critère | Enceintes passives (privilégié) | Enceintes actives |
|---|---|---|
| Diffusion | 2 à 4 enceintes de 8 Ω | 2 à 4 enceintes de 12″ ou 15″ |
| Amplification | 1 ou 2 amplificateurs stéréo supplémentaires | Intégrée aux enceintes |
| Signal | Sorties DSP vers amplis par XLR | Sorties DSP vers enceintes par XLR |
| Sorties de puissance | Câbles Speakon vers enceintes | Sans objet |
| Électricité | À l'emplacement des amplificateurs | À chaque enceinte |

Le processeur THE T.RACKS FIR DSP 408 offre **quatre sorties XLR disponibles (5 à 8)**. Chacune peut être configurée avec un niveau, une égalisation, des filtres et un retard propres au renfort.

Pour la **solution passive complète**, deux amplificateurs stéréo peuvent alimenter chacun deux enceintes de 8 Ω, à raison d'une enceinte par canal.

Le dossier initial envisageait une diffusion sur une même ligne, sans retard ajouté a priori : **ce paramétrage doit être confirmé sur place** selon les emplacements et les orientations. La configuration DSP et les essais seront préparés en amont si le matériel est disponible.

</details>

## 5. Conditions de mise en œuvre

Pour préparer une installation fonctionnelle, il faudra organiser l'alimentation, le déchargement, la protection météo et les réglages avant le spectacle.

| Besoin | Prévision |
|---|---|
| **Électricité** | 1 prise dédiée **230 V / 16 A** pour le rack ; une seconde ligne adaptée si des amplificateurs sont ajoutés |
| **Accès** | Déchargement au plus près de la zone d'installation |
| **Essais** | Environ **30 minutes** de test sonore avant la tombée de la nuit |
| **Météo** | Rack protégé et housses adaptées aux enceintes |

<details>
<summary><strong>Afficher les contraintes d'installation et la liste de vérification</strong></summary>

- Une ligne électrique dédiée au rack, sans buvette ni chauffage sur cette même ligne.
- Manutention à prévoir pour les caissons de **41 kg** et les B1520 PRO de **27 kg**.
- Mise en hauteur envisagée des enceintes à **2,5 à 3 m**, sous réserve du plan de sécurité.
- Cheminement, longueurs et protection mécanique des câbles à confirmer.
- Vérification de la compatibilité du matériel éventuellement prêté.

**À valider avant exploitation :**

- [ ] Emplacements et distances de sécurité confirmés sur le plan de tir.
- [ ] Matériel prêté et connectique vérifiés.
- [ ] Alimentation électrique disponible et adaptée.
- [ ] Protections contre la pluie installées.
- [ ] Routage DSP, filtrages, égalisation et limiteurs préparés.
- [ ] Retards éventuels et équilibre sonore vérifiés à l'essai.
- [ ] Niveaux acoustiques mesurés et exigences réglementaires confirmées.

</details>

---

[Conventions de rédaction du projet](docs/conventions-redaction.md)

<sub>Source des données : dossier PGE « Sonorisation – Feu d'artifice de Champigneulles 2026 », version du 7 octobre 2026. Les puissances et caractéristiques sont celles consignées dans le dossier d'origine ; implantations et résultats acoustiques sont prévisionnels.</sub>
