# LEÇON 05 — TRANSMETTEUR DE VITESSE ET DE ROTATION

## 1. Objectifs pédagogiques

À la fin de cette leçon, nous devons être capables de :

- Définir la vitesse de rotation et la vitesse linéaire.

- Expliquer le fonctionnement d'un capteur inductif de vitesse.

- Comprendre le fonctionnement d'un encodeur incrémental.

- Distinguer un tachymètre d'un transmetteur de vitesse.

- Comprendre la transmission d'une mesure de vitesse vers un automate programmable.

- Réaliser des calculs de vitesse à partir d'impulsions ou d'un signal 4–20 mA.

- Identifier les principales anomalies rencontrées en maintenance.

## 2. Vitesse de rotation et vitesse linéaire

### 2.1. Vitesse de rotation

La vitesse de rotation représente le nombre de tours effectués par un arbre ou un équipement pendant une unité de temps.

Son unité courante dans l'industrie est le tour par minute (tr/min ou rpm).

Exemples :

- Moteur électrique : 1 450 tr/min.

- Pompe centrifuge : 2 900 tr/min.

- Ventilateur industriel : 1 500 tr/min.

### 2.2. Vitesse linéaire

La vitesse linéaire représente la distance parcourue par un objet pendant une unité de temps.

Son unité est généralement le mètre par seconde (m/s).

Exemples :

- Vitesse d'un convoyeur.

- Vitesse de déplacement d'un produit sur une bande transporteuse.

- Vitesse de déplacement d'un véhicule.

### 2.3. Relation entre vitesse de rotation et vitesse linéaire

Pour une roue ou un rouleau entraîné directement, sans glissement :

v = 2 × π × R × N / 60

Avec :

- v : vitesse linéaire en m/s.

- R : rayon de la roue en mètres.

- N : vitesse de rotation en tr/min.

- π : constante mathématique approximativement égale à 3,1416.

Exemple :

Un rouleau de convoyeur possède un rayon de 0,1 m et tourne à 120 tr/min.

v = (2 × 3,1416 × 0,1 × 120) / 60

v ≈ 1,256 m/s.

La vitesse linéaire du convoyeur est donc approximativement de 1,256 m/s, en supposant l'absence de glissement.

## 3. Capteur inductif de vitesse

### 3.1. Principe de fonctionnement

Un capteur inductif peut être utilisé pour mesurer la vitesse de rotation d'un arbre.

Il détecte le passage des dents d'une roue métallique dentée placée sur l'arbre.

Chaque dent détectée produit une impulsion électrique.

Plus l'arbre tourne rapidement, plus la fréquence des impulsions augmente.

### 3.2. Calcul de la vitesse

La formule utilisée est :

N = 60 × f / Z

Avec :

- N : vitesse de rotation en tr/min.

- f : fréquence des impulsions en Hz.

- Z : nombre de dents de la roue.

Exemple :

Une roue possède 30 dents. Le capteur détecte 60 impulsions par seconde.

N = (60 × 60) / 30

N = 120 tr/min.

L'arbre tourne donc à 120 tr/min.

### 3.3. Applications industrielles

Le capteur inductif de vitesse peut être utilisé pour :

- Surveiller la vitesse d'un moteur.

- Détecter l'arrêt d'un arbre.

- Surveiller la vitesse d'une pompe.

- Détecter une survitesse.

- Contrôler la rotation d'un convoyeur.

## 4. Encodeur incrémental

### 4.1. Définition

Un encodeur incrémental est un dispositif électromécanique qui transforme la rotation d'un arbre en impulsions électriques.

Il permet notamment de déterminer :

- La vitesse de rotation.

- Le sens de rotation.

- Le déplacement angulaire relatif.

### 4.2. Constitution et fonctionnement

Un encodeur comporte généralement :

- Un disque optique ou magnétique.

- Un élément de détection.

- Une électronique de traitement.

- Des sorties électriques.

Lorsque l'arbre tourne, le dispositif produit une succession d'impulsions.

### 4.3. Voies A et B

Un encodeur incrémental possède généralement deux voies principales : A et B.

Ces deux signaux sont décalés dans le temps, ce qui permet de déterminer le sens de rotation.

- Si A précède B, le sens correspond à une direction.

- Si B précède A, le sens correspond à la direction opposée.

L'interprétation exacte dépend du câblage et de la configuration.

### 4.4. Voie Z ou Index

Certains encodeurs possèdent une troisième voie appelée Z ou Index.

Elle fournit généralement une impulsion de référence par tour.

Cette impulsion peut servir à retrouver une position de référence.

### 4.5. Notion de PPR

PPR signifie Pulses Per Revolution, c'est-à-dire impulsions par tour.

Exemple :

Un encodeur de 1 024 PPR fournit normalement 1 024 impulsions sur sa voie A pour un tour complet, selon la définition du fabricant.

Il faut distinguer :

- Le nombre d'impulsions par tour annoncé par le fabricant.

- Le nombre de fronts réellement comptés par l'automate.

En quadrature, le comptage peut être effectué selon plusieurs modes :

- x1 : comptage d'un front de la voie A.

- x2 : comptage des deux fronts de la voie A.

- x4 : comptage des fronts montants et descendants des voies A et B.

Il faut donc vérifier la convention PPR/CPR utilisée par le fabricant et le mode de comptage configuré.

### 4.6. Exemple de calcul

Un encodeur fournit 500 impulsions par tour.

L'automate compte 10 000 impulsions sur la voie A pendant une minute, en mode x1.

N = 10 000 / 500

N = 20 tr/min.

## 5. Tachymètre

### 5.1. Définition

Le tachymètre est un instrument utilisé pour mesurer la vitesse de rotation d'un équipement.

Il existe principalement deux familles.

### 5.2. Tachymètre à contact

Il possède généralement un embout qui entre en contact avec l'arbre ou une surface tournante.

L'appareil mesure la vitesse à partir de la rotation de son embout.

Attention : cette méthode nécessite des précautions particulières pour éviter tout contact dangereux avec les parties tournantes.

### 5.3. Tachymètre optique ou laser

Il mesure la vitesse sans contact.

On place généralement une bande réfléchissante sur l'arbre. Le tachymètre émet un faisceau lumineux et détecte les réflexions produites par le passage de la bande.

Il calcule ensuite la vitesse de rotation.

Cette méthode est particulièrement utile pour les mesures ponctuelles pendant les opérations de maintenance.

### 5.4. Différence entre tachymètre et transmetteur de vitesse

| **Tachymètre** | **Transmetteur de vitesse** |
| :-: | :-: |
| Généralement utilisé pour une mesure locale | Généralement installé en permanence |
| Affiche directement la vitesse | Transmet une information à un système de contrôle |
| Peut être utilisé pendant une inspection | Peut fonctionner en continu |
| Peut être à contact ou optique | Peut utiliser des impulsions ou un signal normalisé |

Certains tachymètres disposent également de sorties électriques. La distinction porte donc principalement sur leur usage et leur intégration dans le système de contrôle.

## 6. Transmission de la vitesse vers un automate programmable

La vitesse peut être transmise à un automate de plusieurs manières.

### 6.1. Transmission par impulsions

Un capteur inductif ou un encodeur peut envoyer des impulsions électriques à l'automate.

L'automate mesure leur fréquence ou les compte pendant une durée déterminée afin de calculer la vitesse.

Pour les fréquences élevées, il est préférable d'utiliser un compteur rapide (HSC) compatible avec le signal du capteur.

Un cycle de programme automate classique peut manquer certaines impulsions si leur fréquence est trop élevée.

### 6.2. Transmission par signal 4–20 mA

Certains transmetteurs de vitesse convertissent la mesure en un signal analogique normalisé de 4–20 mA.

Exemple : transmetteur configuré entre 0 et 3 000 tr/min.

| **Vitesse** | **Signal** |
| :-: | :-: |
| 0 tr/min | 4 mA |
| 750 tr/min | 8 mA |
| 1 500 tr/min | 12 mA |
| 2 250 tr/min | 16 mA |
| 3 000 tr/min | 20 mA |

### 6.3. Calcul de la vitesse à partir du courant

La formule générale est :

N = LRV + ((I - 4) / 16) × (URV - LRV)

Avec :

- N : vitesse calculée.

- I : courant mesuré en mA.

- LRV : valeur basse de la plage configurée.

- URV : valeur haute de la plage configurée.

Exemple :

Un transmetteur possède une plage de 0 à 3 000 tr/min. L'automate mesure 14 mA.

N = 0 + ((14 - 4) / 16) × 3 000

N = 1 875 tr/min.

La vitesse affichée doit donc être de 1 875 tr/min.

## 7. Intégration avec un automate Siemens S7-1200

L'intégration dépend du type de signal délivré par le capteur ou le transmetteur.

### 7.1. Signal par impulsions

Pour un signal provenant d'un capteur inductif ou d'un encodeur, il faut utiliser une entrée compatible avec la fréquence et les caractéristiques électriques du signal.

Le S7-1200 dispose de fonctions de comptage rapide (HSC), selon la référence de la CPU et les possibilités de configuration.

### 7.2. Signal analogique 4–20 mA

Il faut disposer d'une entrée analogique compatible avec une mesure de courant.

Attention : les entrées analogiques intégrées de la CPU S7-1200 1214C standard mesurent des tensions 0–10 V. Elles ne reçoivent pas directement un signal 4–20 mA.

Un module d'entrées analogiques compatible avec le courant, par exemple une variante appropriée de SM 1231, peut être utilisé.

Le choix du module doit être vérifié à partir de sa référence exacte et de sa documentation Siemens.

## 8. Défauts et diagnostic en maintenance

### 8.1. Vitesse affichée égale à zéro

Causes possibles :

- L'équipement est réellement à l'arrêt.

- Capteur défectueux.

- Absence d'alimentation du capteur.

- Câble coupé.

- Absence d'impulsions.

- Mauvaise configuration de l'entrée automate.

### 8.2. Vitesse instable

Causes possibles :

- Mauvais positionnement du capteur.

- Distance incorrecte entre le capteur et la roue dentée.

- Perturbations électromagnétiques.

- Mauvais blindage ou raccordement du câble.

- Défaut mécanique ou vibrations excessives.

### 8.3. Vitesse affichée trop élevée

Causes possibles :

- Mauvais nombre de dents configuré.

- Mauvais nombre de PPR.

- Mode de comptage incorrect (x1, x2 ou x4).

- Erreur de mise à l'échelle.

- Mauvaise prise en compte d'un rapport mécanique.

### 8.4. Sens de rotation incorrect

Causes possibles :

- Inversion des voies A et B.

- Mauvaise interprétation des signaux.

- Configuration incorrecte de l'encodeur.

### 8.5. Exemple pratique de diagnostic

Un moteur tourne réellement à 1 450 tr/min, mesuré avec un tachymètre laser.

L'IHM affiche 2 900 tr/min.

La valeur affichée est exactement le double de la valeur réelle.

Il faut notamment vérifier :

- Le nombre de dents ou le PPR configuré.

- Le mode de comptage utilisé.

- Le paramétrage du compteur rapide.

- La mise à l'échelle dans le programme automate.

- L'existence éventuelle d'un rapport mécanique.

Il ne faut pas remplacer immédiatement le capteur sans avoir vérifié la configuration.

## 9. Synthèse

| **Équipement** | **Fonction principale** |
| :-: | :-: |
| Capteur inductif de vitesse | Détecte le passage des dents d'une roue métallique |
| Encodeur incrémental | Produit des impulsions permettant de suivre la rotation |
| Tachymètre à contact | Mesure localement une vitesse par contact |
| Tachymètre optique | Mesure localement une vitesse sans contact |
| Transmetteur de vitesse | Transmet une mesure exploitable par un système de contrôle |
| Compteur rapide HSC | Compte les impulsions à fréquence élevée |

### À retenir

- La vitesse de rotation s'exprime généralement en tr/min.

- La vitesse linéaire s'exprime généralement en m/s.

- Un capteur inductif peut mesurer une vitesse en détectant les dents d'une roue.

- Un encodeur incrémental fournit des impulsions et peut permettre de déterminer le sens de rotation.

- Un tachymètre optique permet une mesure ponctuelle sans contact.

- Un transmetteur peut convertir une vitesse en signal 4–20 mA.

- Un automate doit disposer d'une entrée adaptée au signal reçu.

- Le diagnostic doit prendre en compte le capteur, le câblage, le comptage et la mise à l'échelle.

## 10. Évaluation finale

1. Quelle est l'unité courante de la vitesse de rotation ?

2. Une roue possède 30 dents et le capteur détecte 60 impulsions par seconde. Quelle est la vitesse ?

3. Quel est le rôle des voies A et B d'un encodeur incrémental ?

4. Un transmetteur possède une plage de 0 à 3 000 tr/min. Quelle vitesse correspond à 12 mA ?

5. Quel instrument permet de mesurer une vitesse sans contact avec l'arbre ?

**Fin de la leçon 05 — Transmetteur de vitesse et de rotation.**

