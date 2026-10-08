# Annexe technique — sonorisation de Champigneulles 2026

[← Revenir à la synthèse](../README.md)

> [!NOTE]
> **Nature du document :** données matérielles annoncées par les fabricants et estimations reprises du dossier PGE du 7 octobre 2026. Les puissances nominales et niveaux acoustiques ci-dessous **ne constituent pas des mesures sur site**.

Cette annexe regroupe les détails techniques de l'installation existante et du renfort envisagé pour le spectacle pyromusical du **6 décembre 2026**.

## Matériel de l'association

### TRAITEMENT ET AMPLIFICATION

| Équipement | Qté | Fonction |
|---|---:|---|
| THE BOX PRO AMPRACK MK II | 1 | Rack mobile : processeur, amplificateurs et connexions |
| THE T.RACKS FIR DSP 408 | 1 | Filtrage, égalisation, limitation et routage audio |
| THE T.AMP E-1200 | 1 | Amplification des médiums et aigus |
| THE T.AMP E-1500 | 1 | Amplification des graves |

**Caractéristiques retenues :**

| Équipement | Spécification |
|---|---|
| FIR DSP 408 | 4 entrées et 8 sorties XLR ; filtres FIR ; **4 sorties utilisées et 4 disponibles** |
| E-1200 | **2 × 990 W sous 4 Ω** ; 2 × 680 W sous 8 Ω ; classe H |
| E-1500 | **2 × 850 W sous 8 Ω** ; 2 × 1 220 W sous 4 Ω ; classe H |
| AMPRACK MK II | Secteur 230 V ; entrées XLR ; connexions Thru et sorties Speakon System / Top / Sub |

### ENCEINTES PASSIVES

| Modèle | Qté | Puissance RMS | Impédance |
|---|---:|---:|---:|
| BEHRINGER EUROLIVE B1520 PRO | 2 | **300 W** | 8 Ω |
| AUDIOPHONY A12 | 2 | **250 W** | 8 Ω |
| BEHRINGER EUROLIVE VP1800S | 2 | **400 W** | 8 Ω |

<details>
<summary>Caractéristiques complémentaires des enceintes</summary>

| Modèle | Configuration | Sensibilité | Crête | Masse |
|---|---|---:|---:|---:|
| BEHRINGER EUROLIVE B1520 PRO | 15″ + 1,75″ | 96 dB (1 W / 1 m) | 1 200 W | 27 kg |
| AUDIOPHONY A12 | 3 voies, 12″ | 99 dB (1 W / 1 m) | 500 W | 14 kg |
| BEHRINGER EUROLIVE VP1800S | Caisson de 18″, 40 à 200 Hz | 100 dB (1 W / 1 m) | 1 600 W | 41 kg |

</details>

### PILOTAGE ET ACCESSOIRES

| Équipement | Qté | Utilisation |
|---|---:|---|
| COBRA AUDIO BOX | 1 | Lecture MP3 sur clé USB, synchronisée par radio avec le pupitre ; sorties casque, RCA et jack 6,35 mm |
| JCB NSA 2008 | 1 | Table de mixage principale, 6 voies dont 1 micro |
| BEHRINGER XENYX 302USB | 1 | Table de mixage de secours, 5 voies |
| TRÉPIEDS ET MÂTS | 4 | Mise en hauteur des enceintes ; embase de 35 mm |

## Architecture de diffusion actuelle

La **COBRA Audio Box** reçoit la synchronisation radio du pupitre. La bande-son traverse la table de mixage, puis le DSP distribue les fréquences vers les deux amplificateurs.

~~~mermaid
%%{init: {"flowchart": {"nodeSpacing": 20, "rankSpacing": 34, "htmlLabels": false}, "theme": "base", "themeVariables": {"fontSize": "13px", "lineColor": "#64748b"}}}%%
flowchart TB
  A["Pupitre COBRA 18R2"]
  B["COBRA Audio Box"]
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
  classDef proc fill:#dbeafe,stroke:#2563eb,color:#172b4d;
  classDef output fill:#ecfdf5,stroke:#059669,color:#14532d;
  class A,B,C source;
  class D,E,F proc;
  class G,H output;
~~~

*Schéma fonctionnel, non à l'échelle et ne représentant pas chaque câble séparément.*

**Répartition des canaux :**

- **E-1200 :** 1 B1520 PRO et 1 A12 par canal, montées en parallèle, soit une charge nominale de 4 Ω par canal.
- **E-1500 :** 1 caisson VP1800S par canal, sous 8 Ω.
- **DSP :** 4 sorties employées pour les deux canaux médiums/aigus et les deux canaux graves ; **sorties 5 à 8 disponibles** pour une extension.

> [!IMPORTANT]
> Les sorties XLR disponibles sur le DSP sont des sorties **de signal**, pas des sorties de puissance. Le renfort exige des enceintes actives ou des amplificateurs supplémentaires.

## Implantation indicative

Les enceintes sont envisagées côté tir, à environ **1 à 2 m devant la barrière**, et hors des cercles de **30 m** liés au tir bas calibre selon le dossier initial. Le positionnement doit être validé sur le plan de sécurité.

Pour que les schémas restent lisibles sur mobile, la ligne **ouest → centre → est** est représentée de haut en bas. Les traits figurent **l'ordre des points de diffusion**, pas un câblage.

### Installation actuelle : trois points de diffusion

~~~mermaid
%%{init: {"flowchart": {"nodeSpacing": 28, "rankSpacing": 28, "htmlLabels": false}, "theme": "base", "themeVariables": {"fontSize": "13px"}}}%%
flowchart TB
  O["OUEST · 1 B1520 PRO"]
  C["CENTRE · 2 VP1800S + 2 A12"]
  E["EST · 1 B1520 PRO"]
  O --- C --- E
  classDef installed fill:#dbeafe,stroke:#2563eb,color:#172b4d;
  class O,C,E installed;
~~~

Les **deux caissons de basses sont regroupés au centre** pour favoriser leur couplage acoustique. Le dossier estime un gain de l'ordre de 6 dB dans les graves, dépendant des conditions réelles. Les deux A12 sont orientées vers les côtés opposés.

### Extension envisagée : sept points de diffusion

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

**Légende :** bleu = matériel PGE existant ; orange = point de diffusion supplémentaire envisagé. Les emplacements sont des hypothèses et non un plan d'implantation définitif.

Chaque enceinte ajoutée peut bénéficier d'une sortie DSP dédiée : réglage de niveau, filtrage, égalisation et retard ajustable. Le dossier initial envisage une ligne sans retard supplémentaire ; **ce choix doit être vérifié à l'essai**.

## Puissance d'amplification

Ces données correspondent à la **somme des puissances nominales annoncées**, et non à une puissance instantanée effectivement mesurée pendant le spectacle.

| Circuit | Amplification annoncée | Enceintes raccordées |
|---|---:|---:|
| Médiums et aigus, 2 canaux à 4 Ω | **1 980 W** | 1 100 W RMS |
| Graves, 2 canaux à 8 Ω | **1 700 W** | 800 W RMS |
| **Total** | **3 680 W** | **1 900 W RMS** |

- Ratio de puissance nominale annoncé pour les médiums/aigus : **× 1,8**.
- Ratio pour les graves : **× 2,1**.
- Ratio global : **environ × 1,9**.

Cette réserve peut être utile au fonctionnement, mais elle ne remplace pas une configuration correcte des **filtres, limiteurs et niveaux**. Elle ne permet pas à elle seule de déduire le niveau sonore au public.

## Estimations acoustiques et limites

Le dossier initial fournit une **estimation théorique pour une seule B1520 PRO** à pleine puissance, en champ libre :

| Distance | Niveau estimé | Lecture pratique |
|---|---:|---|
| 5 m | **107 dB** | Niveau élevé, à éviter au premier rang |
| 10 m | 101 dB | Musique très présente |
| 20 à 25 m | 93 à 95 dB | Musique bien présente |
| 50 m | 87 dB | Peut être masquée par les détonations |
| 100 m | 81 dB | Fond sonore |

**Hypothèses reprises du dossier d'origine :** décroissance approximative de 6 dB par doublement de distance, contribution éventuelle de plusieurs enceintes et incertitude annoncée de ± 3 dB. Ce sont des **ordres de grandeur**, pas une simulation acoustique du site ni des valeurs garanties.

La zone public considérée est d'environ **90 m de long sur 20 m de profondeur** (variations selon le plan : approximativement 90 à 95 m sur 15 à 23 m). La plupart des emplacements du public figurant sur le plan sont décrits comme situés à moins de 25 m d'une enceinte ; l'**extrémité ouest** est moins favorable.

Le dossier indique également :
- Au-delà d'environ **40 à 50 m**, la musique tend à devenir un fond sonore, notamment pendant les bombes de **75 et 100 mm**.
- L'humidité, les arbres, la foule et l'orientation des enceintes peuvent affecter le résultat.
- Une cible prévisionnelle d'environ **95 dB au milieu du public**.

Le document initial cite **102 dB(A) sur 15 minutes** en référence au décret n° 2017-1244. **Cette mention ne constitue pas une validation du régime réglementaire applicable** au spectacle : l'organisateur doit confirmer les exigences et procéder aux vérifications appropriées.

> [!WARNING]
> **La couverture annoncée n'est pas une garantie.** Elle concerne la zone de public prévue sur le plan, pas l'ensemble du parc ni les spectateurs installés hors de cette zone. Seule l'évaluation sur site peut confirmer l'homogénéité et les niveaux réels.

## Extension proposée

### Option B — amplificateurs et enceintes passives (privilégiée)

| Matériel supplémentaire | Quantité recherchée |
|---|---:|
| Amplificateurs stéréo, au moins 2 × 500 W sous 8 Ω | **2** |
| Enceintes passives de 8 Ω | **4** |
| Câbles Speakon de 25 à 50 m | 1 par enceinte |
| Câblage de signal XLR | À prévoir selon l'emplacement des amplis |
| Protections contre la pluie | Selon implantation |

Un **premier palier** reste possible avec un seul amplificateur et deux enceintes. L'objectif présenté à la commune est bien le **renfort complet de deux amplificateurs et quatre enceintes**.

### Option A — enceintes actives (alternative)

| Matériel supplémentaire | Quantité recherchée |
|---|---:|
| Enceintes amplifiées de 12″ ou 15″ | 2 à 4 |
| Pieds adaptés | 1 par enceinte |
| Câbles XLR de 25 à 50 m | 1 par enceinte |
| Alimentation secteur 230 V | 1 point par enceinte |
| Protections contre la pluie | Selon implantation |

Les quatre sorties disponibles du DSP peuvent servir à piloter les renforts. Leur affectation, le routage, les filtres, les limiteurs, le câblage et les niveaux devront être préparés puis testés avant le spectacle, sous réserve de disponibilité du matériel prêté.

## Logistique et validation

| Point | Prévision |
|---|---|
| Électricité | Prise dédiée 230 V / 16 A pour le rack, sans buvette ni chauffage sur la même ligne |
| Extension passive | Prévoir une seconde alimentation adaptée pour les amplificateurs supplémentaires |
| Manutention | Accès véhicule au plus près ; caissons de 41 kg et B1520 de 27 kg |
| Hauteur | Enceintes à environ 2,5 à 3 m, sous réserve du plan de sécurité |
| Essai | Créneau d'environ 30 minutes avant la tombée de la nuit |
| Météo | Rack couvert et protections adaptées aux enceintes |

**Points à confirmer avant installation :**

- [ ] Emplacements réels et conformité au plan de tir.
- [ ] Disponibilité et compatibilité des amplificateurs et enceintes prêtés.
- [ ] Longueur, cheminement et protection des câbles.
- [ ] Alimentation disponible et protections météo.
- [ ] Configuration du DSP : voies, filtres, limiteurs et égalisation.
- [ ] Réglages, retards éventuels et niveaux sonores mesurés sur site.
- [ ] Exigences réglementaires applicables.

---

<sub>Référence technique : dossier PGE « Sonorisation – Feu d'artifice de Champigneulles 2026 », daté du 7 octobre 2026. Toutes les implantations et valeurs acoustiques restent prévisionnelles.</sub>
