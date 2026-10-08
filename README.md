# Sonorisation — Champigneulles 2026

**Association Pyrotechnique du Grand Est (PGE)** · **Spectacle pyromusical du 6 décembre 2026**

Dossier technique de l'installation PGE, des contraintes de diffusion sur le site de Champigneulles et de la solution envisagée.

## 1. Notre installation — matériel PGE

<details open>
<summary><strong>Afficher le matériel et les branchements</strong></summary>

Le dispositif existant comprend **2 amplificateurs**, **4 enceintes de diffusion** et **2 caissons de graves**, répartis sur **3 points de diffusion**.

### Schéma et branchements audio

La musique est lancée par la **COBRA AUDIO BOX**, synchronisée avec le **poste de tir COBRA 18R2**.

~~~mermaid
%%{init: {"flowchart": {"useMaxWidth": true, "nodeSpacing": 16, "rankSpacing": 24, "htmlLabels": true, "wrappingWidth": 260}, "theme": "base", "themeVariables": {"fontSize": "12px", "lineColor": "#64748b"}}}%%
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

  A -. "Télécommunications radio (antenne)" .-> B
  B -. "RCA → LINE 1" .-> C
  C -. "REC OUT → INPUT" .-> D
  D -. "XLR" .-> E
  D -. "XLR" .-> F
  E -.-> LG
  E -.-> LD
  F -.-> FG
  F -.-> FD
  LG -. "SYSTEM OUT L" .-> BG
  LG -. "TOP OUT L" .-> AG
  LD -. "SYSTEM OUT R" .-> BD
  LD -. "TOP OUT R" .-> AD
  FG -. "SUB OUT L" .-> SG
  FD -. "SUB OUT R" .-> SD

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
  class A,B,C commande;
  class D processeur;
  class E,F amplis;
  class LG,LD,FG,FD canaux;
  class BG,BD principales;
  class AG,AD appoint;
  class SG,SD basses;
  class TG,TD,MG,MD support;
~~~

~~~mermaid
%%{init: {"flowchart": {"diagramPadding": 0, "padding": 5, "htmlLabels": true, "wrappingWidth": 360}, "theme": "base", "themeVariables": {"fontSize": "11px"}}}%%
flowchart LR
  LIBRE["<b>4 SORTIES XLR LIBRES</b><br/>DSP 408 · sorties 5 à 8<br/>2 à 4 enceintes amplifiées<br/>ou ampli + enceintes passives"]
  classDef reserve fill:#eff6ff,stroke:#3b82f6,stroke-width:1px,stroke-dasharray:4 3,color:#1e40af;
  class LIBRE reserve;
~~~

**Puissances cumulées :** amplificateurs **3 680 W annoncés** · enceintes **1 900 W RMS**. Cette réserve de puissance exige des réglages adaptés des filtres et limiteurs.

Le matériel comprend également un rack **THE BOX PRO AMPRACK MK II**.

<details>
<summary>🔹 Fiche technique complète — matériel, puissances et raccordements</summary>

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
<tr><td nowrap="nowrap">E-1200&nbsp;—&nbsp;gauche&nbsp;/&nbsp;droit</td><td align="center">2 canaux</td><td><strong>4&nbsp;Ω&nbsp;/&#8288;&nbsp;canal</strong></td><td>SYSTEM OUT L/R → B1520 PRO (TOP)<br/>TOP OUT L/R → A12 (MID)<br/>1 de chaque en parallèle par canal</td></tr>
<tr><td nowrap="nowrap">E-1500&nbsp;—&nbsp;gauche&nbsp;/&nbsp;droit</td><td align="center">2 canaux</td><td><strong>8&nbsp;Ω&nbsp;/&#8288;&nbsp;canal</strong></td><td>SUB OUT L/R → VP1800S (SUB)<br/>1 caisson par canal</td></tr>
<tr><td nowrap="nowrap">Trépied&nbsp;au&nbsp;sol</td><td align="center">2</td><td>—</td><td>Support indépendant<br/>Pour B1520 PRO (15″)</td></tr>
<tr><td nowrap="nowrap">Mât&nbsp;de&nbsp;couplage</td><td align="center">2</td><td>35 mm</td><td>Inséré dans l'embase du VP1800S<br/>Porte l'A12 (12″)</td></tr>
</tbody>
</table>

**Précision :** les B1520 PRO et A12 sont des enceintes large bande, exploitées ici pour les médiums/aigus selon les filtres du DSP. [B1520 PRO : constructeur](https://www.behringer.com/en/products/0313-AAM) · [A12 : fiche technique Audiofanzine](https://fr.audiofanzine.com/enceinte-sono-full-range/audiophony/A12/).

</details>

</details>

## 2. La problématique — sonorisation du public

<details>
<summary><strong>Afficher l'implantation actuelle et ses limites</strong></summary>

D'après le plan de tir, la plupart des spectateurs de la zone prévue seraient à **moins de 25 m d'une enceinte**. Notre installation semble adaptée à ce périmètre, mais la diffusion pourrait être **moins régulière aux extrémités**, particulièrement à l'ouest. Le dispositif n'est pas destiné à sonoriser l'ensemble du parc.

### Implantation actuelle

![Plan de sonorisation — disposition actuelle des trois points de diffusion](docs/V%20ACTUELLE%20PGE.png)

![Légende de l'implantation actuelle](docs/V%20LEGENDE%20PGE.png)

</details>

## 3. La solution — renforcer la diffusion

<details>
<summary><strong>Afficher l'implantation proposée et les besoins</strong></summary>

Pour améliorer la répartition du son aux extrémités du public, nous proposons de **conserver toute l'installation PGE** et de compléter la diffusion avec **2 amplificateurs et 4 enceintes passives**. Le dispositif passerait ainsi de **3 à 7 points de diffusion**, sans modifier les 2 caissons de graves existants.

### Implantation envisagée

Le plan ci-dessous montre où seraient placés les quatre points supplémentaires par rapport au matériel actuel.

![Plan de sonorisation — implantation avec quatre enceintes passives supplémentaires](docs/V%20PROPOSE%20PGE.png)

![Légende de l'implantation envisagée](docs/V%20LEGENDE%20PGE.png)

*Positionnement et angles de couverture indicatifs, à confirmer sur site.*

### Matériel à mobiliser

La **solution privilégiée** repose sur des enceintes passives, alimentées par des amplificateurs stéréo supplémentaires. Elle permet de conserver la chaîne audio actuelle et d'utiliser les sorties encore libres du processeur.

| Matériel | Quantité | Besoin |
|---|---:|---|
| Amplificateurs stéréo | **2** | Au moins 2 × 500 W sous 8 Ω chacun |
| Enceintes passives | **4** | 8 Ω, avec supports |
| Câbles Speakon | 4 | 1 par enceinte ; 25 à 50 m envisagés |
| Câbles XLR | Selon implantation | Du DSP vers les amplificateurs |
| Protections pluie | Selon implantation | Pour les amplificateurs et les enceintes |

Un **prêt partiel d'un amplificateur et de deux enceintes** reste envisageable : il permettrait un renfort réduit à deux points supplémentaires.

### Raccordement et réglages

Le **THE T.RACKS FIR DSP 408** utilise actuellement 4 de ses 8 sorties. Les **sorties XLR 5 à 8**, situées à l'arrière du processeur dans le rack, permettent d'ajouter des points de diffusion avec des réglages propres de **niveau, égalisation, filtres et retard**. Il faudra accéder à l'arrière du rack et configurer leur affectation.

Avec la solution passive, le signal passe du **DSP en XLR aux amplificateurs**, puis des amplificateurs **aux enceintes en Speakon**. Chaque nouvel amplificateur stéréo alimenterait **deux enceintes de 8 Ω**, une par canal. La même ligne de diffusion est envisagée **sans retard a priori** ; les distances et orientations seront vérifiées lors des essais. Si un prêt est confirmé suffisamment tôt, le câblage et les réglages seront préparés et testés **avant le jour J**.

<details>
<summary>🔹 Alternative : enceintes actives</summary>

Si les amplificateurs et les enceintes passives ne sont pas disponibles, **2 à 4 enceintes actives de 12″ ou 15″**, avec pieds, constituent une autre solution. Elles simplifient l'amplification, mais nécessitent du courant et une protection pluie à chaque emplacement.

| Point | Passives (privilégiées) | Actives |
|---|---|---|
| Amplification | 1 à 2 amplificateurs stéréo externes | Intégrée |
| Câblage depuis le DSP | XLR vers amplis, puis Speakon | XLR par enceinte (25 à 50 m envisagés) |
| Alimentation 230 V | Près des amplificateurs | À chaque enceinte |

</details>

</details>

## 4. Conditions d'installation — sécurité et logistique

<details open>
<summary><strong>Afficher les exigences et les vérifications avant le spectacle</strong></summary>

Quel que soit le renfort choisi, **l'implantation définitive doit être validée sur le plan de sécurité**. La mise en œuvre dépend notamment des distances de sécurité, de l'alimentation électrique et de l'accès au site.

### Implantation et sécurité

Les enceintes sont envisagées à **1 à 2 m devant la barrière**, côté tir, à une hauteur de **2,5 à 3 m**.

Ces positions devront rester **en dehors des cercles de sécurité de 30 m liés au petit calibre** et être confirmées à partir du plan de tir.

### Alimentation et protection météo

Le rack nécessite une **ligne dédiée 230 V / 16 A**, sans buvette ni chauffage sur le même circuit.

Si des amplificateurs supplémentaires sont ajoutés, prévoir **une seconde ligne électrique adaptée**.

En décembre, protéger le **rack**, les **amplificateurs** et les **enceintes** contre la pluie : rack couvert, housses et protections adaptées.

### Accès, manutention et essais

Le véhicule doit pouvoir décharger le matériel **au plus près** des emplacements. La manutention concerne notamment les caissons de **41 kg** et les **B1520 PRO de 27 kg**.

Réserver un créneau d'environ **30 minutes avant la tombée de la nuit** pour les essais sonores et les derniers réglages.

<details>
<summary>🔹 Vérifications avant le spectacle</summary>

- [ ] Confirmer les emplacements avec le plan de tir et les distances de sécurité.
- [ ] Vérifier la disponibilité et la compatibilité du matériel prêté.
- [ ] Prévoir la longueur, le passage et la protection des câbles.
- [ ] Vérifier les alimentations et les protections contre la pluie.
- [ ] Régler les sorties du DSP, les filtres et les limiteurs.
- [ ] Ajuster les niveaux, la couverture et les éventuels retards sur place.
- [ ] Vérifier les niveaux sonores et la réglementation applicable.

</details>

</details>
---

*Document de travail établi à partir du dossier PGE du 7 octobre 2026. Puissances et caractéristiques reprises du dossier initial ; implantations et niveaux acoustiques à confirmer sur place.*

[Conventions de rédaction](docs/conventions-redaction.md)
