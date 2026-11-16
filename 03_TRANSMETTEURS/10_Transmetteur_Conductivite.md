# LEÇON 10 — TRANSMETTEURS DE CONDUCTIVITÉ INDUSTRIELLE

## 1. Objectifs pédagogiques

À la fin de cette leçon, nous devons être capables de :

- Définir la conductivité électrique d'un liquide.
- Faire la différence entre conductivité et résistivité.
- Identifier les principales technologies de mesure.
- Expliquer le rôle de la compensation en température.
- Comprendre le fonctionnement d'un transmetteur de conductivité.
- Interpréter un signal normalisé 4–20 mA.
- Identifier les applications industrielles.
- Comprendre le raccordement à un automate Siemens S7-1200.
- Diagnostiquer les anomalies de mesure.

---

## 2. Définition de la conductivité

La conductivité électrique représente la capacité d'un matériau à laisser circuler le courant électrique.

Dans les liquides, cette capacité dépend principalement de la présence d'ions mobiles.

Un ion est un atome ou un groupe d'atomes qui possède une charge électrique.

### Exemple : eau pure et eau salée

L'eau très pure contient très peu d'ions libres. Sa conductivité est donc très faible.

Lorsqu'on ajoute du sel (NaCl), celui-ci se dissocie en ions :

- Na⁺ : ion sodium ;
- Cl⁻ : ion chlorure.

Ces ions mobiles permettent le transport des charges électriques. L'eau salée devient donc plus conductrice.

### Unités de mesure

Les principales unités utilisées sont :

- S/m : siemens par mètre ;
- mS/cm : millisiemens par centimètre ;
- µS/cm : microsiemens par centimètre.

Conversions importantes :

- 1 mS/cm = 1 000 µS/cm.
- 1 S/m = 10 mS/cm.

### Applications industrielles

La conductivité est notamment surveillée dans :

- Les chaudières industrielles.
- Les installations de traitement d'eau.
- Les systèmes d'osmose inverse.
- Les tours de refroidissement.
- Les industries agroalimentaires.
- Les installations de production d'eau déminéralisée.

---

## 3. Conductivité et résistivité

La conductivité et la résistivité sont deux grandeurs inverses.

La relation mathématique est :

**σ = 1/ρ**

Avec :

- σ : conductivité électrique ;
- ρ : résistivité électrique.

Ainsi :

- Une conductivité élevée correspond à une résistivité faible.
- Une conductivité faible correspond à une résistivité élevée.

En général, lorsque la concentration en ions mobiles augmente, la conductivité augmente.

Attention : la conductivité dépend également de la température et de la nature des ions présents.

---

## 4. Technologies des sondes de conductivité

Il existe principalement deux grandes technologies de mesure.

### 4.1. Sonde à électrodes (mesure par contact)

Cette sonde possède des électrodes en contact direct avec le liquide.

Principe de fonctionnement :

1. Le dispositif applique une tension alternative entre les électrodes.
2. Le liquide permet le passage d'un courant électrique.
3. Le système mesure la réponse électrique.
4. L'électronique calcule la conductivité du liquide.

L'utilisation d'un signal alternatif permet notamment de limiter la polarisation des électrodes et certaines réactions électrochimiques.

On distingue notamment :

- Les sondes à deux électrodes.
- Les sondes à quatre électrodes.

Les sondes à quatre électrodes permettent notamment de mieux maîtriser certains effets de polarisation et de résistance parasite.

### 4.2. Sonde inductive ou toroïdale

Contrairement à la sonde à électrodes, la sonde inductive ne nécessite pas de contact électrique direct entre les électrodes et le liquide.

Elle contient généralement deux bobines :

- Une bobine émettrice.
- Une bobine réceptrice.

Principe de fonctionnement :

1. La bobine émettrice crée un champ électromagnétique.
2. Ce champ induit un courant dans le liquide conducteur.
3. La bobine réceptrice détecte la réponse électromagnétique.
4. L'électronique détermine la conductivité.

Cette technologie est particulièrement adaptée aux liquides :

- Agressifs ou corrosifs.
- Fortement conducteurs.
- Susceptibles d'encrasser les électrodes.

**Remarque :** le choix de la technologie dépend de la conductivité attendue, de la composition du liquide et des conditions du procédé.

---

## 5. Influence de la température

La conductivité d'une solution électrolytique augmente généralement lorsque sa température augmente.

Cela signifie qu'une variation de conductivité ne traduit pas nécessairement une variation de la concentration en ions.

Exemple pédagogique :

| Température | Conductivité mesurée |
|---|---:|
| 20 °C | 500 µS/cm |
| 25 °C | 560 µS/cm |
| 30 °C | 620 µS/cm |

La composition du liquide peut être identique, mais la température modifie la mesure.

### 5.1. Compensation en température

Pour comparer correctement les mesures, les transmetteurs peuvent ramener la conductivité à une température de référence, souvent 25 °C.

La compensation peut utiliser :

- Une sonde de température intégrée.
- Une sonde PT100 ou PT1000 séparée.
- Un coefficient de compensation paramétrable.

Le coefficient doit être adapté au liquide mesuré. Une compensation linéaire standard ne convient pas nécessairement à toutes les solutions.

**Objectif :** éviter de confondre une variation due à la température avec une variation réelle de la composition du liquide.

---

## 6. Fonctionnement d'un transmetteur de conductivité

Un transmetteur de conductivité transforme la mesure réalisée par une sonde en un signal exploitable par un système de contrôle-commande.

### Chaîne de mesure

Sonde de conductivité → Transmetteur → Signal de sortie → Automate programmable → Supervision HMI/SCADA.

### Fonctions principales

Le transmetteur peut assurer :

1. L'acquisition du signal provenant de la sonde.
2. Le traitement électronique de la mesure.
3. La compensation en température.
4. La conversion en unité de conductivité.
5. La transmission de la valeur au système de contrôle.

### Signaux de sortie possibles

Selon le modèle, le transmetteur peut proposer :

- 4–20 mA.
- 0–10 V.
- HART.
- Modbus RTU.
- PROFIBUS ou PROFINET.

Tous les modèles ne possèdent pas nécessairement l'ensemble de ces interfaces.

---

## 7. Signal normalisé 4–20 mA

Le signal 4–20 mA permet de transmettre une mesure analogique à un automate industriel.

Prenons un transmetteur configuré avec :

- LRV = 0 µS/cm.
- URV = 2 000 µS/cm.
- Signal de sortie = 4–20 mA.

LRV signifie Lower Range Value : valeur basse de la plage.

URV signifie Upper Range Value : valeur haute de la plage.

### Correspondance entre courant et conductivité

| Courant | Conductivité |
|---|---:|
| 4 mA | 0 µS/cm |
| 8 mA | 500 µS/cm |
| 12 mA | 1 000 µS/cm |
| 16 mA | 1 500 µS/cm |
| 20 mA | 2 000 µS/cm |

### Formule de conversion

La formule générale est :

C = LRV + ((I - 4) / 16) × (URV - LRV)

Avec :

- C : conductivité calculée ;
- I : courant mesuré en mA ;
- LRV : valeur basse de la plage ;
- URV : valeur haute de la plage.

### Exemple de calcul

Un transmetteur possède une plage de 0 à 2 000 µS/cm et délivre un courant de 14 mA.

C = 0 + ((14 - 4) / 16) × 2 000

C = (10 / 16) × 2 000

**C = 1 250 µS/cm**

La conductivité mesurée est donc de 1 250 µS/cm.

---

## 8. Applications industrielles

### 8.1. Surveillance de l'eau des chaudières

Dans une chaudière industrielle, la conductivité permet de surveiller la concentration des substances dissoutes dans l'eau.

Une concentration excessive peut favoriser :

- La formation de dépôts.
- L'entartrage.
- Certains phénomènes de corrosion.
- La dégradation des performances thermiques.

La mesure peut être utilisée pour piloter une purge de déconcentration.

### 8.2. Installation d'osmose inverse

Dans une installation d'osmose inverse, la conductivité de l'eau produite permet de surveiller la qualité du perméat.

Une augmentation inhabituelle peut signaler :

- Une dégradation des membranes.
- Une fuite interne.
- Une anomalie de fonctionnement.
- Une variation de la qualité de l'eau d'alimentation.

### 8.3. Tour de refroidissement

Dans une tour de refroidissement, une partie de l'eau s'évapore tandis que les sels dissous restent dans le circuit.

La concentration en sels augmente progressivement.

La conductivité permet donc de surveiller cette concentration et d'aider à déterminer le moment où une purge est nécessaire.

Exemple :

Une conductivité qui passe de 1 000 à 2 500 µS/cm peut indiquer une augmentation de la concentration en substances dissoutes.

Si le seuil autorisé par le procédé est dépassé, le système peut commander une purge.

Les seuils doivent être définis en fonction de la qualité de l'eau et des caractéristiques de l'installation.

---

## 9. Intégration avec un automate Siemens S7-1200

### 9.1. Chaîne d'acquisition

Sonde de conductivité → Transmetteur 4–20 mA → Module d'entrée analogique → CPU S7-1200 → HMI/SCADA.

Rôle des équipements :

| Équipement | Fonction |
|---|---|
| Sonde | Mesure la conductivité du liquide |
| Transmetteur | Traite et convertit la mesure |
| Module analogique | Acquiert le signal électrique |
| CPU S7-1200 | Traite la valeur et les seuils |
| HMI/SCADA | Affiche la mesure et les alarmes |

### 9.2. Attention à la compatibilité des entrées analogiques

Sur une CPU S7-1200 standard de type 1214C, les entrées analogiques intégrées sont généralement prévues pour des signaux 0–10 V.

Elles ne doivent donc pas être considérées comme directement compatibles avec un transmetteur 4–20 mA.

Pour recevoir directement ce signal, il faut sélectionner un module d'entrées analogiques compatible 4–20 mA, par exemple une référence appropriée de la gamme SM 1231.

La référence exacte, les caractéristiques et le câblage doivent être vérifiés dans la documentation Siemens du module choisi.

### 9.3. Exemple de surveillance avec l'automate

Supposons les seuils pédagogiques suivants :

| Conductivité | État |
|---|---|
| < 1 500 µS/cm | Normal |
| ≥ 1 500 µS/cm | Préalarme |
| ≥ 1 800 µS/cm | Alarme |

Exemples :

- 1 200 µS/cm : état normal.
- 1 700 µS/cm : préalarme.
- 1 900 µS/cm : alarme.

Ces valeurs sont uniquement illustratives. Les véritables seuils dépendent du procédé industriel.

---

## 10. Diagnostic des défauts

| Anomalie constatée | Causes possibles | Vérifications |
|---|---|---|
| Mesure bloquée | Sonde défectueuse, câble coupé, transmetteur bloqué | Vérifier la sonde, le câblage et le transmetteur |
| Mesure instable | Perturbations électriques, mauvais raccordement, bulles ou écoulement perturbé | Vérifier l'installation et les conditions de mesure |
| Mesure trop élevée | Concentration réellement élevée, compensation incorrecte, sonde encrassée | Vérifier le procédé, la température et la sonde |
| Mesure trop faible | Défaut de sonde, mauvais contact, configuration incorrecte | Vérifier la sonde et les paramètres |
| Absence de signal 4–20 mA | Défaut d'alimentation, câble coupé ou transmetteur défectueux | Vérifier l'alimentation et la boucle de courant |
| Valeur incorrecte sur l'automate | Mauvaise configuration ou mauvaise mise à l'échelle | Vérifier le module et le programme automate |

**Important :** une anomalie de mesure ne permet pas à elle seule d'identifier avec certitude la pièce défectueuse. Le diagnostic doit être progressif.

---

## 11. Exercices d'application

### Exercice 1 — Conversion 4–20 mA

Un transmetteur de conductivité possède une plage de 0 à 1 000 µS/cm.

Calculer la conductivité correspondant à 12 mA.

**Correction :**

C = ((12 - 4) / 16) × 1 000

C = (8 / 16) × 1 000

**C = 500 µS/cm**

### Exercice 2 — Surveillance d'une tour de refroidissement

Une tour de refroidissement possède un seuil de purge fixé à 2 000 µS/cm.

La mesure actuelle est de 2 400 µS/cm.

**Question :** quelle action le système de régulation peut-il envisager ?

**Correction :** la conductivité dépasse le seuil fixé. Le système peut déclencher une purge, selon la stratégie de régulation et les conditions d'exploitation de l'installation.

### Exercice 3 — Diagnostic

La conductivité affichée reste constamment à 800 µS/cm alors que la composition du liquide change.

**Question :** quelles vérifications faut-il effectuer ?

**Correction :**

- Vérifier l'état de la sonde.
- Contrôler son câblage.
- Vérifier le fonctionnement du transmetteur.
- Contrôler l'acquisition analogique par l'automate.
- Vérifier la configuration et la mise à l'échelle.

---

## 12. Synthèse de la leçon

Les transmetteurs de conductivité permettent de surveiller la concentration des substances ioniques dissoutes dans les liquides.

Les points essentiels à retenir sont :

1. La conductivité traduit la capacité d'un liquide à conduire le courant électrique.
2. Elle dépend notamment de la concentration en ions et de la température.
3. Deux grandes technologies sont utilisées : les sondes à électrodes et les sondes inductives toroïdales.
4. La compensation thermique permet de comparer les mesures à une température de référence.
5. Le signal 4–20 mA facilite l'intégration dans les systèmes automatisés.
6. Les applications concernent notamment les chaudières, l'osmose inverse et les tours de refroidissement.
7. Le diagnostic doit tenir compte de la sonde, du transmetteur, du câblage et de l'automate.

---

## 13. Évaluation finale

Résultat obtenu : **5/5 — 100 %**

Les cinq questions de l'évaluation finale ont été correctement traitées.

**Leçon validée.**
