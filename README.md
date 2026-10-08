# Sonorisation — Champigneulles 2026

**Association Pyrotechnique du Grand Est (PGE)** · Spectacle pyromusical du **6 décembre 2026**

L'association possède une installation de sonorisation complète. D'après les estimations réalisées à partir du plan de tir, elle devrait couvrir la zone de public prévue, mais avec une diffusion moins régulière aux extrémités.

Pour le spectacle demandé par la commune, **nous souhaitons ajouter 2 amplificateurs et 4 enceintes passives**. Le matériel actuel serait conservé.

## 1. Bilan

| Matériel | 🟢 **Disponible chez PGE** | 🟠 **Renfort souhaité** |
|---|---:|---:|
| Amplificateurs | 2 | **+ 2** |
| Enceintes de diffusion | 4 | **+ 4** |
| Caissons de basses | 2 | — |
| Points de diffusion | 3 | **+ 4** |

| Donnée | Estimation |
|---|---|
| Zone de public | Environ **90 × 20 m** |
| Couverture avec le matériel PGE | Adaptée en théorie à cette zone |
| Point le moins favorable | Extrémité ouest |
| Au-delà de 40 à 50 m des enceintes | Musique moins présente, surtout pendant les détonations |
| Apport attendu du renfort | Répartition sonore plus homogène |

Les valeurs de couverture sont **théoriques** : elles ne remplacent pas un essai sur place. Le système n'est pas dimensionné pour sonoriser l'ensemble du parc.

## 2. Matériel disponible chez PGE

### Schéma et branchements audio

La musique est lancée par la **COBRA AUDIO BOX**, synchronisée avec le **poste de tir COBRA 18R2**.

~~~mermaid
%%{init: {"flowchart": {"nodeSpacing": 28, "rankSpacing": 36, "htmlLabels": true, "wrappingWidth": 320}, "theme": "base", "themeVariables": {"fontSize": "13px", "lineColor": "#64748b"}}}%%
flowchart TB
  A["<b>COMMANDE</b><br/>Poste de tir<br/>COBRA 18R2"]
  B["<b>LECTURE AUDIO</b><br/>Bande-son MP3<br/>COBRA AUDIO BOX"]
  C["<b>MIXAGE</b><br/>Table principale<br/>JCB NSA 2008"]
  D["<b>TRAITEMENT</b><br/>Processeur audio<br/>THE T.RACKS FIR DSP 408"]
  E["<b>AMPLIFICATEURS</b><br/>Médiums et aigus<br/>THE T.AMP E-1200<br/>2 × 990 W / 4 Ω"]
  F["<b>AMPLIFICATEURS</b><br/>Graves<br/>THE T.AMP E-1500<br/>2 × 850 W / 8 Ω"]
  LG["<b>CANAL GAUCHE</b><br/>4 Ω"]
  LD["<b>CANAL DROIT</b><br/>4 Ω"]
  FG["<b>CANAL GAUCHE</b><br/>8 Ω"]
  FD["<b>CANAL DROIT</b><br/>8 Ω"]
  BG["<b>ENCEINTE MÉDIUMS/AIGUS</b><br/>2 voies · 15″ · gauche<br/>BEHRINGER EUROLIVE B1520 PRO<br/>300 W RMS"]
  BD["<b>ENCEINTE MÉDIUMS/AIGUS</b><br/>2 voies · 15″ · droite<br/>BEHRINGER EUROLIVE B1520 PRO<br/>300 W RMS"]
  AG["<b>ENCEINTE MÉDIUMS/AIGUS</b><br/>3 voies · 12″ · gauche<br/>AUDIOPHONY A12<br/>250 W RMS"]
  AD["<b>ENCEINTE MÉDIUMS/AIGUS</b><br/>3 voies · 12″ · droite<br/>AUDIOPHONY A12<br/>250 W RMS"]
  SG["<b>ENCEINTE GRAVES</b><br/>18″ · gauche<br/>BEHRINGER EUROLIVE VP1800S<br/>400 W RMS"]
  SD["<b>ENCEINTE GRAVES</b><br/>18″ · droite<br/>BEHRINGER EUROLIVE VP1800S<br/>400 W RMS"]

  TG["<b>TRÉPIED AU SOL</b>"]
  TD["<b>TRÉPIED AU SOL</b>"]
  MG["<b>MÂT DE COUPLAGE</b>"]
  MD["<b>MÂT DE COUPLAGE</b>"]

  %% Points intermédiaires invisibles : deux libellés par câble
  JBC[" "]
  JCD[" "]
  JDE[" "]
  JDF[" "]

  A -. "Télécommunications radio (antenne)" .-> B
  B -. "RCA" .- JBC
  JBC -. "LINE 1" .-> C
  C -. "REC OUT" .- JCD
  JCD -. "INPUT" .-> D
  D -. "SORTIE XLR" .- JDE
  JDE -. "ENTRÉE XLR" .-> E
  D -. "SORTIE XLR" .- JDF
  JDF -. "ENTRÉE XLR" .-> F
  E -. "TOP G" .-> LG
  E -. "TOP D" .-> LD
  F -. "SUB G" .-> FG
  F -. "SUB D" .-> FD
  LG -.-> BG
  LG -.-> AG
  LD -.-> BD
  LD -.-> AD
  FG -.-> SG
  FD -.-> SD

  BG --- TG
  BD --- TD
  SG --- MG
  SD --- MD

  classDef commande fill:#f1f5f9,stroke:#64748b,color:#172b4d;
  classDef processeur fill:#ffedd5,stroke:#d97706,color:#7c2d12;
  classDef amplis fill:#dbeafe,stroke:#2563eb,color:#172b4d;
  classDef canaux fill:#e2e8f0,stroke:#94a3b8,color:#334155;
  classDef principales fill:#ccfbf1,stroke:#0f766e,color:#134e4a;
  classDef appoint fill:#ecfccb,stroke:#65a30d,color:#365314;
  classDef basses fill:#f3e8ff,stroke:#9333ea,color:#581c87;
  classDef support fill:#f8fafc,stroke:#94a3b8,color:#334155;
  classDef junction fill:transparent,stroke:transparent,color:transparent;
  class A,B,C commande;
  class D processeur;
  class E,F amplis;
  class LG,LD,FG,FD canaux;
  class BG,BD principales;
  class AG,AD appoint;
  class SG,SD basses;
  class TG,TD,MG,MD support;
  class JBC,JCD,JDE,JDF junction;
~~~

**Puissances cumulées :** amplificateurs **3 680 W annoncés** · enceintes **1 900 W RMS**.

Le matériel comprend également un rack **THE BOX PRO AMPRACK MK II**.

<details>
<summary><strong>Fiche technique complète — matériel, puissances et raccordements</strong></summary>

<table>
<thead>
<tr><th align="left" width="33%" nowrap="nowrap">Équipement</th><th width="7%" nowrap="nowrap">Qté</th><th align="left" width="25%" nowrap="nowrap">Puissance / Ω</th><th align="left" width="35%" nowrap="nowrap">Détails&nbsp;techniques</th></tr>
</thead>
<tbody>
<tr><th colspan="4" align="left">═══ ⚪ COMMANDE ET MIXAGE ═══</th></tr>
<tr><td nowrap="nowrap">COBRA&nbsp;18R2</td><td align="center">1</td><td>—</td><td>Poste de tir<br/>Synchronisation radio ↔ COBRA&nbsp;AUDIO&nbsp;BOX</td></tr>
<tr><td nowrap="nowrap">COBRA&nbsp;AUDIO&nbsp;BOX</td><td align="center">1</td><td>—</td><td>Lecture MP3 sur clé USB<br/>Sortie casque<br/>Sorties RCA et jack&nbsp;6,35&nbsp;mm</td></tr>
<tr><td nowrap="nowrap">JCB&nbsp;NSA&nbsp;2008</td><td align="center">1</td><td>—</td><td>Mixage principal<br/>6 voies (dont 1 micro)<br/>Volume et annonces</td></tr>
<tr><td nowrap="nowrap">BEHRINGER&nbsp;XENYX&nbsp;302USB</td><td align="center">1</td><td>—</td><td>Table de mixage de secours<br/>5 voies</td></tr>
<tr><th colspan="4" align="left">═══ 🟠 TRAITEMENT AUDIO ═══</th></tr>
<tr><td nowrap="nowrap">THE&nbsp;T.RACKS&nbsp;FIR&nbsp;DSP&nbsp;408</td><td align="center">1</td><td>—</td><td>4 entrées<br/>8 sorties XLR<br/>Traitements : filtres FIR, égalisation, routage, limiteurs<br/>4 sorties utilisées<br/><strong>Sorties 5 à 8 disponibles</strong><br/>Signal non amplifié → amplificateur ou enceinte active</td></tr>
<tr><th colspan="4" align="left">═══ 🔵 AMPLIFICATION ET RACK ═══</th></tr>
<tr><td nowrap="nowrap">THE&nbsp;T.AMP&nbsp;E-1200</td><td align="center">1</td><td><strong>2&nbsp;×&nbsp;990&nbsp;W&nbsp;/&#8288;&nbsp;4&nbsp;Ω</strong><br/>2&nbsp;×&nbsp;680&nbsp;W&nbsp;/&#8288;&nbsp;8&nbsp;Ω</td><td>Amplification médiums/aigus<br/>Classe H</td></tr>
<tr><td nowrap="nowrap">THE&nbsp;T.AMP&nbsp;E-1500</td><td align="center">1</td><td><strong>2&nbsp;×&nbsp;850&nbsp;W&nbsp;/&#8288;&nbsp;8&nbsp;Ω</strong><br/>2&nbsp;×&nbsp;1&nbsp;220&nbsp;W&nbsp;/&#8288;&nbsp;4&nbsp;Ω</td><td>Amplification graves<br/>Classe H</td></tr>
<tr><td nowrap="nowrap">THE&nbsp;BOX&nbsp;PRO&nbsp;AMPRACK&nbsp;MK&nbsp;II</td><td align="center">1</td><td>230 V</td><td>Rack mobile<br/>Entrées et renvois XLR<br/>Sorties Speakon : System / Top / Sub</td></tr>
<tr><th colspan="4" align="left">═══ 🟢 ENCEINTES PASSIVES ═══</th></tr>
<tr><td nowrap="nowrap">🟩&nbsp;BEHRINGER&nbsp;EUROLIVE&nbsp;B1520&nbsp;PRO</td><td align="center">2</td><td><strong>300&nbsp;W&nbsp;RMS&nbsp;/&#8288;&nbsp;8&nbsp;Ω</strong> chacune</td><td>2 voies<br/>15″ + moteur d'aigus&nbsp;1,75″<br/>1&nbsp;200&nbsp;W crête<br/>96&nbsp;dB&nbsp;(1&nbsp;W&nbsp;/&#8288;&nbsp;1&nbsp;m)<br/>27&nbsp;kg</td></tr>
<tr><td nowrap="nowrap">🟨&nbsp;AUDIOPHONY&nbsp;A12</td><td align="center">2</td><td><strong>250&nbsp;W&nbsp;RMS&nbsp;/&#8288;&nbsp;8&nbsp;Ω</strong> chacune</td><td>3 voies<br/>Haut-parleur de 12″<br/>500&nbsp;W crête<br/>99&nbsp;dB&nbsp;(1&nbsp;W&nbsp;/&#8288;&nbsp;1&nbsp;m)<br/>14&nbsp;kg</td></tr>
<tr><td nowrap="nowrap">🟪&nbsp;BEHRINGER&nbsp;EUROLIVE&nbsp;VP1800S</td><td align="center">2</td><td><strong>400&nbsp;W&nbsp;RMS&nbsp;/&#8288;&nbsp;8&nbsp;Ω</strong> chacun</td><td>Caisson 18″<br/>Bande passante : 40–200&nbsp;Hz<br/>1&nbsp;600&nbsp;W crête<br/>100&nbsp;dB&nbsp;(1&nbsp;W&nbsp;/&#8288;&nbsp;1&nbsp;m)<br/>41&nbsp;kg</td></tr>
<tr><th colspan="4" align="left">═══ ⚙️ RACCORDEMENTS ET SUPPORTS ═══</th></tr>
<tr><td nowrap="nowrap">E-1200&nbsp;—&nbsp;gauche&nbsp;/&nbsp;droit</td><td align="center">2 canaux</td><td><strong>4&nbsp;Ω&nbsp;/&#8288;&nbsp;canal</strong></td><td>1 B1520 PRO + 1 A12<br/>Montage en parallèle sur chaque canal</td></tr>
<tr><td nowrap="nowrap">E-1500&nbsp;—&nbsp;gauche&nbsp;/&nbsp;droit</td><td align="center">2 canaux</td><td><strong>8&nbsp;Ω&nbsp;/&#8288;&nbsp;canal</strong></td><td>1 VP1800S par canal</td></tr>
<tr><td nowrap="nowrap">Trépied&nbsp;au&nbsp;sol</td><td align="center">2</td><td>—</td><td>Support indépendant<br/>Pour B1520 PRO (15″)</td></tr>
<tr><td nowrap="nowrap">Mât&nbsp;de&nbsp;couplage</td><td align="center">2</td><td>35 mm</td><td>Inséré dans l'embase du VP1800S<br/>Porte l'A12 (12″)</td></tr>
</tbody>
</table>

**Précision :** les B1520 PRO et A12 sont des enceintes large bande, exploitées ici pour les médiums/aigus selon les filtres du DSP. [B1520 PRO : constructeur](https://www.behringer.com/en/products/0313-AAM) · [A12 : fiche technique Audiofanzine](https://fr.audiofanzine.com/enceinte-sono-full-range/audiophony/A12/).

**Puissances cumulées :** amplificateurs **3 680 W annoncés** · enceintes **1 900 W RMS**.

</details>

## 3. Couverture du public

| Paramètre | Valeur retenue |
|---|---|
| Zone considérée | 90 à 95 m de long ; 15 à 23 m de profondeur |
| Implantation actuelle | **3 points de diffusion** : ouest, centre, est |
| Distance enceinte-public | Moins de 25 m pour la plupart des positions prévues |
| Caissons de basses | 2 regroupés au centre |
| Zone moins bien couverte | Extrémité ouest |
| Sonorisation du parc entier | Non prévue |

<details>
<summary><strong>Implantation actuelle et extension envisagée</strong></summary>

Les points sont présentés d'**ouest en est**, verticalement pour éviter les débordements sur les petits écrans. Les traits indiquent leur succession, pas le câblage. Schémas **non à l'échelle**.

### Installation actuelle : 3 points

~~~mermaid
%%{init: {"flowchart": {"nodeSpacing": 25, "rankSpacing": 26, "htmlLabels": true}, "theme": "base", "themeVariables": {"fontSize": "13px"}}}%%
flowchart TB
  O["Ouest<br/>B1520 PRO"]
  C["Centre<br/>2 VP1800S + 2 A12"]
  E["Est<br/>B1520 PRO"]
  O --- C --- E
  classDef existing fill:#dbeafe,stroke:#2563eb,color:#172b4d;
  class O,C,E existing;
~~~

### Avec renfort : 7 points

~~~mermaid
%%{init: {"flowchart": {"nodeSpacing": 18, "rankSpacing": 20, "htmlLabels": true}, "theme": "base", "themeVariables": {"fontSize": "13px"}}}%%
flowchart TB
  P1["Renfort ouest<br/>P1"]
  O["Ouest<br/>B1520 PRO"]
  P2["Renfort ouest<br/>P2"]
  C["Centre<br/>2 caissons + 2 A12"]
  P3["Renfort est<br/>P3"]
  E["Est<br/>B1520 PRO"]
  P4["Renfort est<br/>P4"]
  P1 --- O --- P2 --- C --- P3 --- E --- P4
  classDef existing fill:#dbeafe,stroke:#2563eb,color:#172b4d;
  classDef proposed fill:#fff2db,stroke:#d97706,color:#7c2d12;
  class O,C,E existing;
  class P1,P2,P3,P4 proposed;
~~~

*Bleu : matériel PGE ; orange : renfort proposé.*

| Positionnement | Prévision |
|---|---|
| Enceintes | 1 à 2 m devant la barrière, côté tir |
| Zones de sécurité | Hors des cercles de 30 m liés au tir bas calibre |
| Hauteur | Environ 2,5 à 3 m, selon les supports |
| Deux caissons au centre | Couplage des graves ; gain théorique évoqué d'environ 6 dB |
| Deux A12 au centre | Orientées vers l'ouest et vers l'est |

L'implantation exacte devra être validée sur le plan de sécurité.

</details>

<details>
<summary><strong>Estimations acoustiques et puissances</strong></summary>

### Puissance nominale

| Circuit | Amplificateurs | Enceintes RMS | Ratio |
|---|---:|---:|---:|
| Médiums/aigus, 2 canaux à 4 Ω | 1 980 W | 1 100 W | × 1,8 |
| Graves, 2 canaux à 8 Ω | 1 700 W | 800 W | × 2,1 |
| **Total** | **3 680 W** | **1 900 W** | **≈ × 1,9** |

Ces ratios ne dispensent pas de régler correctement le filtrage, les limiteurs et les niveaux.

### Niveau théorique d'une B1520 PRO

*Estimation pour une enceinte à pleine puissance, en champ libre ; aucune mesure sur site.*

| Distance | Niveau estimé | Appréciation |
|---|---:|---|
| 5 m | 107 dB | Très élevé pour un premier rang |
| 10 m | 101 dB | Musique très présente |
| 20 à 25 m | 93 à 95 dB | Musique bien présente |
| 50 m | 87 dB | Risque de masquage par les détonations |
| 100 m | 81 dB | Fond sonore |

| Hypothèse du dossier initial | Valeur ou remarque |
|---|---|
| Perte avec la distance | Environ **6 dB** par doublement |
| Incertitude annoncée | **± 3 dB** |
| Contribution de plusieurs enceintes | Peut augmenter le niveau perçu |
| Cible envisagée au milieu du public | Environ **95 dB** |
| Influences extérieures | Foule, humidité, arbres, orientations |
| Référence réglementaire citée | Décret n° 2017-1244 ; 102 dB(A) sur 15 min dans le dossier initial |

La référence réglementaire citée dans le dossier ne suffit pas à établir le régime applicable à cette manifestation. Les niveaux et obligations devront être vérifiés sur place.

</details>

## 4. Matériel complémentaire souhaité

### Solution privilégiée : enceintes passives

| Matériel à obtenir | Quantité | Caractéristiques |
|---|---:|---|
| Amplificateurs stéréo | **2** | Au moins 2 × 500 W sous 8 Ω chacun |
| Enceintes passives | **4** | 8 Ω, avec supports |
| Câbles Speakon | 4 | 1 par enceinte ; 25 à 50 m envisagés |
| Câbles XLR | Selon implantation | DSP vers amplificateurs |
| Protections pluie | Selon implantation | Amplificateurs et enceintes |

**Un prêt partiel de 1 amplificateur et 2 enceintes** reste possible.

### Autre possibilité : enceintes actives

| Matériel à obtenir | Quantité | Caractéristiques |
|---|---:|---|
| Enceintes actives | 2 à 4 | 12″ ou 15″, avec pieds |
| Câbles XLR | 1 par enceinte | 25 à 50 m envisagés |
| Alimentation 230 V | 1 par enceinte | À chaque emplacement |
| Protections pluie | Selon implantation | Matériel installé à l'extérieur |

<details>
<summary><strong>Comparatif et configuration des renforts</strong></summary>

| Point | Passives (privilégiées) | Actives |
|---|---|---|
| Amplification | 1 ou 2 amplis stéréo externes | Intégrée |
| Audio depuis le DSP | XLR vers amplis | XLR vers enceintes |
| Liaison aux enceintes | Speakon | Pas de câble haut-parleur |
| Secteur 230 V | Près des amplificateurs | Près de chaque enceinte |
| Diffusion possible | 2 à 4 enceintes | 2 à 4 enceintes |

Le **FIR DSP 408** dispose de quatre sorties XLR libres (5 à 8). Chaque renfort peut avoir son propre niveau, son égalisation, ses filtres et un retard ajustable.

Dans la configuration passive complète, chaque amplificateur ajouté alimente **deux enceintes de 8 Ω**, une par canal. Le dossier prévoit une même ligne de diffusion, sans retard a priori ; ce point sera confirmé lors des essais selon les distances et les orientations. La configuration DSP devra être préparée avant le spectacle si le matériel de prêt est disponible.

</details>

## 5. Conditions d'installation

| Besoin | Prévision |
|---|---|
| Alimentation du rack | **230 V / 16 A**, ligne dédiée sans buvette ni chauffage |
| Si ajout d'amplificateurs | Seconde ligne électrique adaptée |
| Accès véhicule | Déchargement au plus près |
| Manutention | Caissons de 41 kg ; B1520 PRO de 27 kg |
| Hauteur des enceintes | **2,5 à 3 m**, selon validation de l'implantation |
| Essai sonore | Environ **30 min** avant la tombée de la nuit |
| Protection météo | Rack couvert, housses et protections adaptées |

<details>
<summary><strong>Vérifications avant le spectacle</strong></summary>

- [ ] Confirmer les emplacements avec le plan de tir et les distances de sécurité.
- [ ] Vérifier la disponibilité et la compatibilité du matériel prêté.
- [ ] Prévoir la longueur, le passage et la protection des câbles.
- [ ] Vérifier les alimentations et les protections contre la pluie.
- [ ] Régler les sorties du DSP, les filtres et les limiteurs.
- [ ] Ajuster les niveaux, la couverture et les éventuels retards sur place.
- [ ] Vérifier les niveaux sonores et la réglementation applicable.

</details>

---

*Document de travail établi à partir du dossier PGE du 7 octobre 2026. Puissances et caractéristiques reprises du dossier initial ; implantations et niveaux acoustiques à confirmer sur place.*

[Conventions de rédaction](docs/conventions-redaction.md)
