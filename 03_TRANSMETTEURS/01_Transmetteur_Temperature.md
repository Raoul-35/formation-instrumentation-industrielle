# LEÇON 02 — TRANSMETTEUR DE TEMPÉRATURE INDUSTRIEL

## 1. Définition et rôle

Un transmetteur de température est un instrument qui reçoit l'information d'un capteur de température, la traite et la convertit en un signal exploitable par un système de contrôle-commande.

Les capteurs couramment utilisés sont :
- Les sondes RTD, notamment la PT100.
- Les thermocouples, notamment les types K, J, T et S.

Les sorties possibles comprennent :
- 4–20 mA.
- 0–10 V.
- Des protocoles numériques, selon le modèle.

## 2. Applications industrielles

Les transmetteurs de température sont utilisés pour surveiller :
- Les bobinages des moteurs électriques.
- Les paliers et roulements.
- Les chaudières.
- Les fours industriels.
- Les compresseurs.
- Les circuits de refroidissement.
- Les cuves et réacteurs.

Exemple : une PT100 installée sur le bobinage d'un moteur permet de surveiller son échauffement.

## 3. Chaîne de mesure

Exemple avec une PT100 :

Température du procédé → PT100 → Transmetteur → 4–20 mA → Automate → IHM.

Chaque élément possède un rôle :
- La PT100 détecte la température par variation de résistance.
- Le transmetteur traite cette information et la convertit en signal normalisé.
- L'automate reçoit et exploite le signal.
- L'IHM affiche la température.

## 4. Première technologie : la PT100

La PT100 appartient à la famille des RTD (Resistance Temperature Detector).

Elle utilise un élément sensible en platine dont la résistance électrique varie avec la température.

Son nom signifie :
- PT : platine.
- 100 : résistance nominale de 100 Ω à 0 °C.

### Valeurs indicatives

| Température | Résistance approximative |
|---:|---:|
| 0 °C | 100 Ω |
| 25 °C | 109,73 Ω |
| 50 °C | 119,40 Ω |
| 75 °C | 129,00 Ω |
| 100 °C | 138,51 Ω |
| 150 °C | 157,33 Ω |

La relation entre résistance et température n'est pas parfaitement linéaire sur toute la plage. Les transmetteurs utilisent des caractéristiques normalisées pour convertir correctement la résistance en température.

### Pourquoi le platine ?

Le platine présente notamment :
- Une bonne stabilité.
- Une bonne répétabilité.
- Une caractéristique résistance-température bien définie.
- Une large plage d'utilisation selon la construction de la sonde.

## 5. Raccordement d'une PT100

Il existe plusieurs configurations.

### 5.1. PT100 à deux fils

Deux conducteurs relient la sonde à l'appareil de mesure.

La résistance des câbles s'ajoute à celle de la sonde et peut introduire une erreur.

### 5.2. PT100 à trois fils

Trois conducteurs permettent généralement au transmetteur de compenser la résistance des câbles.

Cette compensation suppose notamment que les résistances des conducteurs soient suffisamment proches.

C'est une configuration très répandue dans l'industrie.

### 5.3. PT100 à quatre fils

Quatre conducteurs permettent une mesure plus précise en séparant les circuits d'excitation et de mesure.

Cette méthode compense efficacement l'influence des résistances des conducteurs.

## 6. Deuxième technologie : le thermocouple

Contrairement à la PT100, le thermocouple ne fonctionne pas par variation de résistance.

Il utilise l'effet Seebeck.

Lorsque deux conducteurs de métaux différents forment un circuit avec des jonctions à des températures différentes, une tension thermoélectrique apparaît.

Cette tension est généralement de l'ordre du millivolt.

### Les deux jonctions

- Jonction de mesure : située au point dont on veut connaître la température.
- Jonction de référence : son influence doit être prise en compte par le dispositif de mesure.

### Compensation de jonction froide

Le transmetteur ou l'appareil de mesure doit tenir compte de la température de référence pour calculer correctement la température de la jonction de mesure.

Cette opération est appelée compensation de jonction froide.

## 7. Les principaux types de thermocouples

| Type | Composition | Applications courantes |
|---|---|---|
| K | Chromel–Alumel | Fours et procédés industriels |
| J | Fer–Constantan | Machines et installations industrielles |
| T | Cuivre–Constantan | Basses températures et réfrigération |
| S | Platine–Rhodium | Fours et applications à haute température |

Les plages d'utilisation dépendent du type, de la construction, de la gaine et des conditions de fonctionnement de la sonde.

Le type K est particulièrement répandu dans l'industrie.

## 8. Différences entre PT100 et thermocouple

| Caractéristique | PT100 | Thermocouple |
|---|---|---|
| Famille | RTD | Thermoélectrique |
| Principe | Variation de résistance | Effet Seebeck |
| Signal brut | Résistance en Ω | Tension en mV |
| Matériau sensible | Platine | Deux métaux différents |
| Raccordement | 2, 3 ou 4 fils | Généralement 2 conducteurs adaptés au type |
| Traitement nécessaire | Mesure de résistance | Mesure de tension et compensation de jonction froide |

La PT100 et le thermocouple ne doivent pas être raccordés à une entrée configurée pour l'autre technologie.

Le transmetteur doit être compatible avec le capteur utilisé.

## 9. Les transmetteurs universels

Certains transmetteurs de température acceptent plusieurs types d'entrées :
- PT100 et autres sondes RTD.
- Thermocouples K, J, T, S, etc.
- Parfois des signaux de résistance ou de tension.

Le technicien doit configurer correctement le type de capteur.

Une mauvaise configuration peut provoquer une mesure incohérente ou un défaut.

## 10. Transmetteur monté en tête

Dans certaines installations, le transmetteur est installé directement dans la tête de raccordement de la sonde.

On parle de transmetteur monté en tête (Head-mounted transmitter).

### Avantages

- Réduction de la longueur des conducteurs transportant le signal brut.
- Conversion du signal près du capteur.
- Transmission d'un signal normalisé sur une plus grande distance.
- Réduction de certaines erreurs et perturbations liées au transport du signal brut.

Exemple :

Une PT100 installée sur un moteur se trouve à 40 mètres de l'armoire électrique.

Un transmetteur monté en tête convertit le signal de la PT100 en 4–20 mA à proximité du capteur. Le signal normalisé est ensuite transmis jusqu'à l'armoire.

## 11. Conversion en signal 4–20 mA

Un transmetteur de température peut être configuré pour une plage de 0 à 200 °C.

| Température | Courant |
|---:|---:|
| 0 °C | 4 mA |
| 50 °C | 8 mA |
| 100 °C | 12 mA |
| 150 °C | 16 mA |
| 200 °C | 20 mA |

Formule de conversion du courant en température :

T = LRV + [(I − 4) / 16] × (URV − LRV)

Avec :
- T : température.
- I : courant mesuré en mA.
- LRV : valeur basse de la plage configurée.
- URV : valeur haute de la plage configurée.

Exemple :

Pour une plage de 0 à 200 °C et un courant de 16 mA :

T = 0 + [(16 − 4) / 16] × 200

T = 150 °C.

## 12. Diagnostic et maintenance

En cas de température incohérente, plusieurs éléments doivent être vérifiés.

### Côté capteur

- PT100 endommagée.
- Thermocouple défectueux.
- Mauvais contact thermique avec le procédé.
- Mauvais type de capteur installé.

### Côté raccordement

- Conducteur coupé.
- Connexion desserrée.
- Mauvaise polarité ou mauvais câblage du thermocouple.
- Mauvais raccordement d'une PT100.

### Côté transmetteur

- Mauvaise configuration du type de capteur.
- Plage LRV/URV incorrecte.
- Défaut d'alimentation.
- Défaut électronique.

### Côté système de contrôle

- Mauvaise configuration de l'entrée analogique.
- Problème de câblage de la boucle.
- Erreur de mise à l'échelle.
- Défaut d'affichage sur l'IHM.

Un courant de sortie nul ne signifie pas nécessairement que la température réelle est nulle. Il faut rechercher un éventuel défaut de boucle, d'alimentation ou de transmetteur.

## 13. Signalisation des défauts

Certains transmetteurs peuvent utiliser des courants inférieurs à 4 mA ou supérieurs à 20 mA pour signaler des défauts.

La recommandation NAMUR NE 43 définit des niveaux de signalisation de défaut utilisés par certains équipements.

À titre d'exemple, certaines configurations utilisent :
- Moins de 3,6 mA : défaut bas.
- Plus de 21 mA : défaut haut.

Les seuils exacts dépendent de l'équipement et de sa configuration. L'entrée analogique doit être configurée pour interpréter correctement ces signaux.

## 14. Synthèse

Un transmetteur de température :
- Reçoit l'information d'une sonde de température.
- Traite la résistance d'une PT100 ou la tension d'un thermocouple.
- Convertit la mesure en un signal exploitable.
- Peut transmettre la température en 4–20 mA.
- Permet la surveillance des équipements et des procédés industriels.

À retenir :

- PT100 : variation de résistance.
- Thermocouple : production d'une tension liée à une différence de température.
- Transmetteur : traitement et conversion du signal.
- Automate : exploitation de la mesure.

## 15. Exercices de révision

**Exercice 1**

Quelle est la résistance nominale d'une PT100 à 0 °C ?

**Exercice 2**

Pourquoi utilise-t-on souvent une PT100 à trois fils en industrie ?

**Exercice 3**

Quel phénomène physique est à l'origine du fonctionnement d'un thermocouple ?

**Exercice 4**

Quelle différence existe-t-il entre le signal brut d'une PT100 et celui d'un thermocouple ?

**Exercice 5**

Un transmetteur est configuré de 0 à 200 °C. Quel courant correspond à 150 °C ?

**Exercice 6**

Pourquoi installe-t-on parfois un transmetteur directement dans la tête de raccordement de la sonde ?

---
**Fin de la leçon 02 — Transmetteur de température**
