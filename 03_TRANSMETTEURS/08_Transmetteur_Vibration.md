# LEÇON 08 — TRANSMETTEURS DE VIBRATION INDUSTRIELLE

## 1. Objectifs pédagogiques

À la fin de cette leçon, nous devons être capables de :

- Définir une vibration mécanique.
- Distinguer le déplacement, la vitesse et l'accélération vibratoires.
- Comprendre la valeur efficace RMS.
- Expliquer le fonctionnement d'un accéléromètre piézoélectrique.
- Comprendre les axes de mesure d'un accéléromètre.
- Expliquer le rôle d'un transmetteur de vibration.
- Comprendre la conversion d'un signal vibratoire en 4–20 mA.
- Identifier les principaux défauts mécaniques détectables par analyse vibratoire.
- Comprendre l'intégration d'un transmetteur dans un automate industriel.

## 2. Définition d'une vibration mécanique

Une vibration mécanique est un mouvement répétitif d'un corps autour de sa position d'équilibre.

Exemples industriels :

- Moteur électrique en fonctionnement.
- Pompe centrifuge.
- Ventilateur industriel.
- Roulement défectueux.
- Arbre tournant déséquilibré.

Les vibrations peuvent être normales ou anormales.

Une augmentation anormale des vibrations peut révéler une dégradation mécanique.

## 3. Les trois grandeurs fondamentales des vibrations

En maintenance industrielle, trois grandeurs sont particulièrement importantes.

| Grandeur | Symbole | Unité courante | Signification |
|---|---|---|---|
| Déplacement | x | µm ou mm | Amplitude du mouvement |
| Vitesse vibratoire | v | mm/s | Rapidité du mouvement |
| Accélération | a | m/s² ou g | Variation de la vitesse |

### 3.1. Déplacement vibratoire

Il représente la distance parcourue par un élément mécanique autour de sa position d'équilibre.

Il est notamment utilisé pour mesurer certains mouvements relatifs d'arbres tournants.

### 3.2. Vitesse vibratoire

Elle représente la rapidité du mouvement vibratoire.

Elle est particulièrement utilisée pour évaluer le niveau vibratoire global de nombreuses machines industrielles.

L'unité courante est le mm/s RMS.

### 3.3. Accélération vibratoire

Elle représente la variation de la vitesse au cours du temps.

Elle est particulièrement utile pour détecter certains défauts de roulements et les vibrations de haute fréquence.

Elle s'exprime généralement en m/s² ou en g.

## 4. La valeur RMS

RMS signifie Root Mean Square, ou valeur efficace.

Une vibration oscille généralement dans les deux sens : positif et négatif.

La moyenne arithmétique peut donc être proche de zéro, même lorsque la vibration est importante.

La valeur RMS permet de représenter le niveau efficace d'un signal vibratoire.

Pour un signal sinusoïdal :

V_RMS = V_crête / √2

La valeur RMS est notamment utilisée pour exprimer la vitesse vibratoire globale en mm/s.

Attention : il faut toujours préciser la grandeur mesurée et le type de valeur utilisé : RMS, crête ou crête-à-crête.

## 5. Les capteurs de vibration

Il existe plusieurs technologies de capteurs.

### 5.1. Accéléromètre piézoélectrique

Il utilise l'effet piézoélectrique.

Lorsqu'un matériau piézoélectrique subit une contrainte mécanique, il génère une charge électrique.

Le capteur transforme donc les accélérations mécaniques en signal électrique.

Applications :

- Surveillance des moteurs.
- Analyse des roulements.
- Surveillance des pompes.
- Analyse des vibrations à haute fréquence.

Certains modèles possèdent une électronique intégrée de type IEPE.

Le signal nécessite un conditionnement adapté avant son exploitation.

### 5.2. Capteur de vitesse vibratoire

Il fournit une mesure liée directement à la vitesse de vibration.

Il peut être utilisé pour surveiller les vibrations globales de certaines machines industrielles.

### 5.3. Sonde de proximité

Elle mesure le déplacement relatif d'un arbre par rapport à son support.

Elle est particulièrement utilisée sur les machines tournantes équipées de paliers lisses, notamment certaines turbines et certains compresseurs.

## 6. Les axes de mesure d'un accéléromètre

Un accéléromètre peut mesurer les vibrations suivant un, deux ou trois axes.

| Axe | Direction dans notre exemple | Utilisation |
|---|---|---|
| X | Horizontal | Mesure latérale |
| Y | Vertical | Mesure verticale |
| Z | Axial | Mesure suivant l'arbre |

Attention : les lettres X, Y et Z ne correspondent pas universellement aux directions horizontale, verticale et axiale. Il faut vérifier l'orientation réelle du capteur.

### Exemple sur un moteur

- Une vibration horizontale peut orienter vers certains défauts de déséquilibre ou de rigidité.
- Une vibration verticale peut orienter vers des problèmes de fixation ou de structure.
- Une vibration axiale peut notamment être associée à un désalignement.

Ces observations constituent des pistes de diagnostic et non des conclusions automatiques.

## 7. Le transmetteur de vibration

Un transmetteur de vibration reçoit le signal du capteur, le conditionne et fournit une mesure exploitable par un système de contrôle.

Selon le modèle, il peut assurer :

- Le conditionnement du signal.
- L'amplification.
- Le filtrage.
- Le calcul d'une grandeur vibratoire.
- La conversion en signal normalisé.
- La transmission vers un automate ou un système de supervision.

Les sorties possibles comprennent notamment :

- 4–20 mA.
- 0–10 V.
- Des communications numériques selon le modèle.

Tous les transmetteurs ne mesurent pas nécessairement les mêmes grandeurs. Certains transmettent l'accélération, d'autres la vitesse vibratoire ou le déplacement.

Il faut donc vérifier la fiche technique avant de choisir un appareil.

## 8. Conversion du signal 4–20 mA

Exemple :

Un transmetteur de vibration possède une plage de mesure de 0 à 20 mm/s RMS.

Sa sortie est configurée de 4 à 20 mA.

| Vitesse vibratoire | Courant |
|---:|---:|
| 0 mm/s | 4 mA |
| 5 mm/s | 8 mA |
| 10 mm/s | 12 mA |
| 15 mm/s | 16 mA |
| 20 mm/s | 20 mA |

La formule de conversion est :

V = LRV + ((I - 4) / 16) × (URV - LRV)

Avec :

- V : vitesse vibratoire.
- I : courant mesuré en mA.
- LRV : valeur basse de mesure.
- URV : valeur haute de mesure.

Exemple avec 14 mA :

V = ((14 - 4) / 16) × 20

V = 12,5 mm/s RMS

## 9. Les principaux défauts mécaniques

L'analyse vibratoire permet de détecter plusieurs défauts.

| Défaut | Signification | Exemple |
|---|---|---|
| Déséquilibre | Mauvaise répartition de masse autour de l'axe | Ventilateur encrassé |
| Désalignement | Mauvais alignement des arbres | Ensemble moteur-pompe |
| Défaut de roulement | Détérioration des éléments du roulement | Pompe industrielle |
| Desserrage mécanique | Fixations insuffisantes | Socle moteur |

### 9.1. Déséquilibre

Le rotor possède une répartition inégale de sa masse autour de son axe de rotation.

Il peut provoquer une vibration importante à la fréquence de rotation.

Exemple : un ventilateur dont une pale présente une accumulation de poussière.

### 9.2. Désalignement

L'arbre du moteur et celui de la machine entraînée ne sont pas correctement alignés.

Conséquences possibles :

- Augmentation des vibrations.
- Usure prématurée des roulements.
- Dégradation de l'accouplement.
- Échauffement mécanique.

### 9.3. Défaut de roulement

Il peut concerner :

- Les billes ou rouleaux.
- La bague intérieure.
- La bague extérieure.
- La cage.

Ces défauts peuvent produire des vibrations à des fréquences caractéristiques du roulement.

### 9.4. Desserrage mécanique

Des boulons, supports ou fixations insuffisamment serrés peuvent provoquer des vibrations anormales et accélérer la détérioration mécanique.

## 10. Les seuils d'alarme vibratoire

Un système de surveillance peut utiliser plusieurs niveaux d'alarme.

Exemple pédagogique pour une installation :

| Niveau | Vitesse vibratoire | Action possible |
|---|---:|---|
| Normal | < 4 mm/s | Fonctionnement normal |
| Préalarme | ≥ 4 mm/s | Surveillance renforcée |
| Alarme | ≥ 7 mm/s | Inspection de la machine |
| Critique | ≥ 10 mm/s | Évaluation urgente et décision d'arrêt |

Ces valeurs sont uniquement illustratives.

Les seuils réels doivent être définis selon :

- La puissance de la machine.
- Le type de machine.
- Le montage.
- Les conditions de fonctionnement.
- Les recommandations du fabricant.
- Les normes applicables.

Une alarme vibratoire ne signifie pas automatiquement qu'il faut arrêter le moteur. La décision dépend de la criticité et des consignes de sécurité de l'installation.

## 11. Comparaison entre le MPU6050 et un capteur industriel

Le MPU6050 est un composant MEMS qui possède :

- Un accéléromètre trois axes.
- Un gyroscope trois axes.
- Une communication I²C.

Il permet de mesurer les accélérations et les vitesses angulaires.

| Critère | MPU6050 | Accéléromètre industriel |
|---|---|---|
| Technologie | MEMS | Souvent piézoélectrique |
| Axes | 3 axes | 1, 2 ou 3 axes |
| Communication | I²C | Analogique ou numérique selon modèle |
| Utilisation | Prototype et apprentissage | Surveillance industrielle |
| Calibration | À vérifier selon le besoin | Généralement documentée |
| Analyse vibratoire | Limitée par ses caractéristiques | Adaptée selon le modèle |

Le MPU6050 est intéressant pour les prototypes et l'apprentissage.

Cependant, ses performances, sa bande passante, son bruit et son montage mécanique doivent être évalués avant de l'utiliser pour un diagnostic industriel fiable.

## 12. Intégration dans un système automatisé

Exemple d'architecture :

Machine tournante  
↓  
Capteur de vibration  
↓  
Transmetteur de vibration  
↓  
Signal 4–20 mA  
↓  
Entrée analogique compatible du PLC  
↓  
Traitement de la mesure  
↓  
Supervision HMI / WinCC

Le PLC peut ensuite :

- Afficher la vitesse vibratoire.
- Comparer la mesure aux seuils programmés.
- Déclencher une préalarme.
- Déclencher une alarme.
- Enregistrer les mesures.
- Participer à une stratégie de maintenance prédictive.

Attention : la CPU Siemens S7-1200 1214C standard possède des entrées analogiques intégrées 0–10 V, et non des entrées courant directes 4–20 mA. Un module compatible est nécessaire pour recevoir directement ce courant.

## 13. Diagnostic des défauts

| Symptôme | Causes possibles | Vérifications |
|---|---|---|
| Vibration élevée | Déséquilibre ou désalignement | Contrôle mécanique |
| Vibration instable | Fixations ou connexions défectueuses | Vérifier montage et câblage |
| Augmentation progressive | Dégradation d'un roulement | Analyse vibratoire approfondie |
| Mesure nulle | Défaut d'alimentation ou de capteur | Vérifier alimentation et signal |
| Valeur incohérente | Mauvaise configuration ou mauvais montage | Vérifier orientation et paramétrage |
| Alarme permanente | Seuil mal configuré ou défaut réel | Vérifier seuils et état mécanique |

## 14. Synthèse

| Élément | Fonction |
|---|---|
| Accéléromètre | Mesure l'accélération vibratoire |
| Capteur de vitesse | Mesure la vitesse vibratoire |
| Sonde de proximité | Mesure le déplacement relatif d'un arbre |
| Transmetteur | Conditionne et convertit le signal |
| Signal 4–20 mA | Transporte la mesure vers le système de contrôle |
| PLC | Traite la mesure et gère les alarmes |
| HMI | Affiche les valeurs et les alarmes |

## 15. Évaluation finale

1. Quelle unité peut être utilisée pour exprimer l'accélération vibratoire ?

2. Quel est le rôle principal d'un transmetteur de vibration configuré en 4–20 mA ?

3. Quel défaut mécanique correspond à une mauvaise répartition de la masse autour de l'axe de rotation ?

4. Un transmetteur possède une plage de 0 à 20 mm/s RMS. Quelle valeur correspond à un courant de 16 mA ?

5. Quel capteur permet de mesurer le déplacement relatif d'un arbre par rapport à son support, notamment sur une machine équipée de paliers lisses ?

**Résultat obtenu à l'évaluation : 5/5 — 100 %.**
