# LEÇON 07 — TRANSMETTEURS DE FORCE ET DE PESAGE INDUSTRIEL

## 1. Objectifs pédagogiques

À la fin de cette leçon, nous devons être capables de :

- Distinguer la masse, la force et le poids.
- Expliquer le fonctionnement d'une cellule de pesage.
- Comprendre le rôle des jauges de contrainte.
- Expliquer le fonctionnement du pont de Wheatstone.
- Interpréter un signal exprimé en mV/V.
- Comprendre la conversion du signal de pesage en 4–20 mA.
- Identifier les différents types de cellules de pesage.
- Diagnostiquer les défauts courants d'une installation de pesage.

## 2. Différence entre masse, force et poids

| Grandeur | Définition | Unité |
|---|---|---|
| Masse | Quantité de matière d'un corps | kg |
| Force | Action mécanique exercée sur un corps | Newton (N) |
| Poids | Force gravitationnelle exercée sur un corps | Newton (N) |

Le poids se calcule par :

P = m × g

Avec :
- P : poids en Newtons.
- m : masse en kilogrammes.
- g : accélération de la pesanteur, environ 9,81 m/s² sur Terre.

Exemple :

Pour une masse de 500 kg :

P = 500 × 9,81 = 4 905 N

## 3. La cellule de pesage (Load Cell)

Une cellule de pesage est un capteur qui transforme une force mécanique en un signal électrique exploitable par un système de mesure.

Applications industrielles :
- Balances industrielles.
- Silos de stockage.
- Réservoirs de dosage.
- Trémies de matières premières.
- Systèmes de pesage sur convoyeurs.

### Principe de fonctionnement

1. Une charge est appliquée sur la cellule.
2. Le corps métallique subit une très légère déformation.
3. Les jauges de contrainte détectent cette déformation.
4. Leur résistance électrique varie.
5. Un circuit de mesure transforme cette variation en signal électrique.

## 4. La jauge de contrainte (Strain Gauge)

La jauge de contrainte est un élément sensible fixé sur le corps métallique de la cellule de pesage.

Elle possède généralement une fine grille métallique conductrice fixée sur un support isolant.

### Principe

- En traction, la jauge s'allonge et sa résistance augmente généralement.
- En compression, elle se raccourcit et sa résistance diminue généralement.

La résistance électrique est donnée par :

R = ρ × L / S

Avec :
- R : résistance électrique.
- ρ : résistivité du matériau.
- L : longueur du conducteur.
- S : section du conducteur.

La déformation mécanique entraîne donc une variation de résistance électrique.

## 5. Le pont de Wheatstone

Le pont de Wheatstone est un circuit électrique permettant de détecter de faibles variations de résistance.

Il comporte quatre résistances, qui peuvent être constituées de quatre jauges de contrainte dans une cellule de pesage.

### Fonctionnement

Sans charge, le pont est idéalement équilibré.

Lorsqu'une charge est appliquée :
- Certaines jauges sont étirées.
- D'autres sont comprimées.
- Les résistances changent.
- Le pont se déséquilibre.
- Une tension apparaît à sa sortie.

Cette tension est proportionnelle à la déformation dans la plage de fonctionnement prévue.

## 6. Le signal mV/V

Les cellules de pesage fournissent souvent un signal exprimé en mV/V.

Cette unité représente la tension de sortie par volt d'alimentation du pont de mesure.

Exemple :

Une cellule possède une sensibilité de 2 mV/V et reçoit une alimentation de 10 V.

À pleine charge :

U = 2 × 10 = 20 mV

La cellule fournit donc une tension nominale de 20 mV à pleine charge.

Autre exemple :

Avec une alimentation de 5 V :

U = 2 × 5 = 10 mV

Attention : le signal mV/V est très faible. Il nécessite un appareil de mesure ou un transmetteur adapté.

## 7. Le transmetteur de pesage

Le transmetteur de pesage alimente et traite le signal provenant de la cellule.

Selon le modèle, il peut assurer :
- L'alimentation du pont de jauges.
- L'amplification du signal.
- La conversion analogique-numérique.
- Le réglage du zéro et de la portée.
- La linéarisation et le filtrage.
- La conversion en signal normalisé.
- La communication avec un automate ou un système de supervision.

Les sorties possibles comprennent notamment :
- 4–20 mA.
- 0–10 V.
- Des communications numériques selon le modèle : RS-485, Modbus, PROFIBUS, PROFINET, etc.

Il faut toujours vérifier les caractéristiques du transmetteur avant de choisir le raccordement.

## 8. Conversion du signal 4–20 mA en masse

Exemple :

Une cuve possède une capacité de 1 000 kg.

Le transmetteur est configuré ainsi :

| Masse | Courant |
|---:|---:|
| 0 kg | 4 mA |
| 250 kg | 8 mA |
| 500 kg | 12 mA |
| 750 kg | 16 mA |
| 1 000 kg | 20 mA |

La formule de conversion est :

M = LRV + ((I - 4) / 16) × (URV - LRV)

Avec :
- M : masse calculée.
- I : courant mesuré en mA.
- LRV : valeur basse de mesure.
- URV : valeur haute de mesure.

Pour une plage de 0 à 1 000 kg :

M = ((I - 4) / 16) × 1 000

Exemple avec un courant de 14 mA :

M = ((14 - 4) / 16) × 1 000

M = 625 kg

## 9. Les différents types de cellules de pesage

| Type | Caractéristique | Application |
|---|---|---|
| Simple point | Mesure une charge sur une plateforme | Balance industrielle |
| Cisaillement (Shear Beam) | Mesure une déformation en cisaillement | Cuves et trémies |
| Compression | Mesure une force de compression | Silos et réservoirs |
| Type S | Mesure en traction ou compression | Pesage suspendu |

### Exemple : pesage d'un silo

Un silo repose sur quatre cellules de pesage.

Pour une charge totale de 4 000 kg, avec une répartition parfaitement uniforme :

M par cellule = 4 000 / 4 = 1 000 kg

En pratique, la répartition peut être inégale en raison de la géométrie, de l'installation ou de la position du produit.

## 10. Intégration dans un système automatisé

Exemple d'architecture :

Charge mécanique  
↓  
Cellule de pesage  
↓  
Transmetteur de pesage  
↓  
Signal 4–20 mA  
↓  
Entrée analogique compatible du PLC  
↓  
Traitement de la mesure  
↓  
Affichage sur HMI / WinCC

Le transmetteur réalise la mesure et la conversion du signal.

Le PLC exploite la valeur pour :
- Afficher la masse.
- Déclencher une alarme de surcharge.
- Commander une opération de remplissage.
- Arrêter un dosage lorsque la masse cible est atteinte.
- Enregistrer les données de production.

Attention : le raccordement direct d'une cellule mV/V à une entrée analogique standard d'un automate n'est généralement pas adapté. Il faut un transmetteur ou un module de pesage compatible.

## 11. Défauts et diagnostic

| Symptôme | Causes possibles | Vérifications |
|---|---|---|
| Affichage à zéro | Absence d'alimentation ou cellule déconnectée | Vérifier l'alimentation et le câblage |
| Masse instable | Vibrations, connexions défectueuses, humidité | Contrôler les connexions et les fixations |
| Masse incorrecte | Mauvais étalonnage ou surcharge | Vérifier la calibration |
| Masse négative | Polarité inversée ou mauvais réglage du zéro | Vérifier le câblage et la configuration |
| Affichage bloqué | Défaut du transmetteur ou signal figé | Contrôler le signal de mesure |
| Différence entre cellules | Répartition inégale ou problème mécanique | Vérifier les appuis et les cellules |

### Exemple : cuve vide affichant 350 kg

Une cuve vide affiche 350 kg au lieu de zéro.

Une cause possible est un mauvais réglage du zéro (Zero Calibration).

Avant de corriger le zéro, il faut vérifier :
- Que la cuve est réellement vide.
- Que les cellules ne sont pas bloquées mécaniquement.
- Qu'aucune tuyauterie ne transmet une force parasite.
- Que les cellules et leurs connexions sont en bon état.

## 12. Synthèse

| Élément | Fonction |
|---|---|
| Cellule de pesage | Transforme une force mécanique en signal électrique |
| Jauge de contrainte | Détecte la déformation mécanique |
| Pont de Wheatstone | Convertit les variations de résistance en tension mesurable |
| Signal mV/V | Exprime la sensibilité électrique de la cellule |
| Transmetteur de pesage | Traite et convertit le signal de la cellule |
| Signal 4–20 mA | Transporte la mesure vers un système de contrôle |
| PLC | Traite la mesure et réalise les actions programmées |
| HMI | Affiche les valeurs et les alarmes |

## 13. Évaluation finale

1. Une cellule possède une sensibilité de 2 mV/V et une alimentation de 5 V. Quelle est sa tension de sortie nominale à pleine charge ?

2. Une cuve de 2 000 kg possède un transmetteur configuré de 4 à 20 mA. Quelle masse correspond à 12 mA ?

3. Quel est le rôle du pont de Wheatstone dans une cellule de pesage ?

4. Un silo de 4 800 kg repose sur quatre cellules. Quelle charge supporte chaque cellule si la répartition est uniforme ?

5. Une cellule de 2 mV/V est alimentée sous 10 V. Si elle délivre 10 mV, quel pourcentage de sa capacité nominale représente cette charge ?

**Résultat obtenu à l'évaluation : 5/5 — 100 %.**
