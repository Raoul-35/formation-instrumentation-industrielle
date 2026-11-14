# LEÇON 06 — TRANSMETTEUR DE POSITION INDUSTRIEL

## 1. Objectifs pédagogiques

À la fin de cette leçon, nous devons être capables de :

- Distinguer position, déplacement et vitesse.
- Expliquer le fonctionnement d'un potentiomètre de position.
- Comprendre le principe de fonctionnement d'un LVDT.
- Distinguer les encodeurs incrémentaux et absolus.
- Comprendre le fonctionnement des capteurs magnétiques de position.
- Identifier les différents signaux de transmission.
- Intégrer une mesure de position dans un automate programmable.
- Diagnostiquer les défauts d'une chaîne de mesure de position.

## 2. Position, déplacement et vitesse

### 2.1. Position

La position indique l'endroit où se trouve un objet par rapport à un point de référence.

Exemple : un vérin hydraulique peut être en position rentrée, à mi-course ou en position sortie.

### 2.2. Déplacement

Le déplacement représente la variation de position entre deux instants.

Formule :

Δx = x₂ - x₁

Exemple :

Un vérin passe de 20 mm à 150 mm.

Δx = 150 - 20 = 130 mm.

Son déplacement est de 130 mm.

### 2.3. Vitesse

La vitesse représente la rapidité avec laquelle un objet change de position.

Formule :

v = Δx / Δt

Avec :
- v : vitesse en m/s.
- Δx : déplacement en mètres.
- Δt : durée en secondes.

Exemple :

Un vérin parcourt 200 mm en 2 secondes.

v = 0,2 / 2 = 0,1 m/s.

## 3. Potentiomètre de position

### 3.1. Définition

Un potentiomètre de position est un capteur qui transforme un déplacement mécanique en variation de résistance électrique.

Il peut mesurer :
- Un déplacement linéaire.
- Un déplacement angulaire.

### 3.2. Constitution

Il comporte principalement :
- Une piste résistive.
- Un curseur mobile.
- Trois bornes électriques.

Lorsque le curseur se déplace sur la piste résistive, la résistance entre certaines bornes varie.

### 3.3. Principe de fonctionnement

Le potentiomètre peut être alimenté sous une tension de référence.

La position du curseur détermine la tension disponible à la sortie.

Exemple avec une sortie linéaire de 0 à 10 V :

| Position | Tension |
|---:|---:|
| 0 % | 0 V |
| 25 % | 2,5 V |
| 50 % | 5 V |
| 75 % | 7,5 V |
| 100 % | 10 V |

Ces valeurs supposent un montage idéal et une sortie correctement conditionnée.

### 3.4. Potentiomètre linéaire

Il mesure un déplacement en ligne droite.

Applications :
- Position d'une tige de vérin.
- Déplacement d'un chariot.
- Position d'un mécanisme mobile.

La grandeur mesurée est généralement exprimée en millimètres.

### 3.5. Potentiomètre rotatif

Il mesure un déplacement angulaire.

Applications :
- Position d'une vanne rotative.
- Angle d'un bras mécanique.
- Position angulaire d'un axe.

La grandeur mesurée est généralement exprimée en degrés.

### 3.6. Avantages et limites

| Avantages | Limites |
|---|---|
| Principe simple | Usure possible du curseur |
| Coût généralement accessible | Sensibilité aux vibrations |
| Mesure continue | Durée de vie liée aux frottements |
| Sortie électrique exploitable | Nécessite un montage adapté |

## 4. LVDT

### 4.1. Définition

LVDT signifie Linear Variable Differential Transformer.

C'est un capteur électromagnétique qui permet de mesurer avec précision un déplacement linéaire.

Contrairement au potentiomètre, il ne nécessite pas de contact électrique glissant entre un curseur et une piste résistive.

### 4.2. Constitution

Un LVDT comporte principalement :
- Un enroulement primaire.
- Deux enroulements secondaires.
- Un noyau magnétique mobile.
- Un circuit électronique de conditionnement.

### 4.3. Principe de fonctionnement

Le primaire est alimenté par un signal alternatif.

Ce signal crée un champ magnétique qui induit des tensions dans les deux secondaires.

Selon la position du noyau :
- Au centre : les tensions secondaires sont égales et leur différence est théoriquement nulle.
- Déplacé vers un côté : la tension d'un secondaire devient supérieure à celle de l'autre.
- Déplacé vers l'autre côté : la situation s'inverse.

Le circuit électronique exploite cette différence pour déterminer le déplacement et son sens par rapport au point central.

### 4.4. Conditionnement du signal

Le signal brut du LVDT est généralement alternatif.

Un circuit de conditionnement permet de produire une sortie exploitable, par exemple :
- 0–10 V.
- 4–20 mA.

### 4.5. Applications industrielles

- Mesure de la course d'un vérin hydraulique.
- Position d'une vanne de régulation.
- Déplacement d'une pièce mécanique.
- Surveillance du déplacement d'un élément de machine.

### 4.6. Comparaison avec le potentiomètre

| Potentiomètre | LVDT |
|---|---|
| Principe résistif | Principe électromagnétique |
| Contact électrique glissant | Pas de contact électrique glissant |
| Usure possible du curseur | Faible usure interne |
| Montage relativement simple | Conditionnement électronique généralement nécessaire |
| Mesure linéaire ou angulaire | Mesure linéaire |

## 5. Encodeurs de position

### 5.1. Définition

Un encodeur est un dispositif qui transforme un déplacement ou une rotation en informations électriques permettant de déterminer une position.

Il existe deux grandes catégories :
- Encodeur incrémental.
- Encodeur absolu.

### 5.2. Encodeur incrémental

Un encodeur incrémental produit des impulsions électriques lorsque son arbre tourne.

L'automate compte ces impulsions pour déterminer le déplacement effectué.

Exemple :

Un encodeur fournit 1 000 impulsions par tour.

Pour un demi-tour :

Nombre d'impulsions = 1 000 × 0,5

Nombre d'impulsions = 500.

L'automate peut ainsi déterminer le déplacement angulaire relatif.

**Limite :** après une coupure d'alimentation, la position doit généralement être retrouvée à partir d'une référence appelée origine ou zéro machine.

### 5.3. Encodeur absolu

Un encodeur absolu associe une valeur numérique à chaque position.

Il peut donc fournir directement une information de position, même après une coupure d'alimentation, sous réserve que l'encodeur et son système de lecture soient correctement alimentés et configurés.

Exemple :
- 0° : position initiale.
- 90° : quart de tour.
- 180° : demi-tour.
- 270° : trois quarts de tour.

### 5.4. Comparaison

| Encodeur incrémental | Encodeur absolu |
|---|---|
| Produit des impulsions | Fournit une valeur de position codée |
| Mesure un déplacement relatif | Indique une position absolue |
| Nécessite généralement une référence après démarrage | Conserve l'information de position sans référencement, selon sa technologie |
| Comptage des impulsions | Lecture d'un code de position |
| Utilisé pour vitesse et déplacement | Utilisé pour positionnement précis |

## 6. Capteurs magnétiques de position

### 6.1. Principe

Un capteur magnétique détecte le champ magnétique produit par un aimant associé à un élément mobile.

Selon sa technologie, il peut détecter une position prédéfinie ou mesurer un déplacement continu.

### 6.2. Application sur un vérin pneumatique

Sur certains vérins pneumatiques, un aimant permanent est intégré au piston.

Des capteurs magnétiques sont fixés à l'extérieur du corps du vérin.

Lorsque le piston arrive devant un capteur, celui-ci détecte le champ magnétique.

On peut ainsi obtenir deux informations :
- Vérin complètement rentré.
- Vérin complètement sorti.

### 6.3. Capteur magnétique TOR et capteur analogique

| Capteur magnétique TOR | Capteur magnétique analogique |
|---|---|
| Détecte une position prédéfinie | Mesure une position sur une plage |
| Sortie généralement 0 ou 1 | Sortie analogique ou numérique |
| Exemple : vérin sorti | Exemple : vérin à 125 mm |

Un capteur magnétique TOR ne fournit donc pas nécessairement la position exacte en millimètres.

## 7. Signaux de transmission de position

### 7.1. Signal analogique 0–10 V

Exemple : course de 0 à 200 mm.

| Position | Tension |
|---:|---:|
| 0 mm | 0 V |
| 50 mm | 2,5 V |
| 100 mm | 5 V |
| 150 mm | 7,5 V |
| 200 mm | 10 V |

### 7.2. Signal analogique 4–20 mA

Pour la même course :

| Position | Courant |
|---:|---:|
| 0 mm | 4 mA |
| 50 mm | 8 mA |
| 100 mm | 12 mA |
| 150 mm | 16 mA |
| 200 mm | 20 mA |

Le signal 4–20 mA présente l'avantage du zéro vivant :
- 4 mA représente le début de la plage de mesure.
- 0 mA peut signaler une coupure de boucle, une perte d'alimentation ou un défaut d'appareil.

### 7.3. Signal numérique

Certains encodeurs transmettent leur position sous forme numérique.

Exemples d'interfaces :
- SSI.
- PROFIBUS.
- PROFINET.
- IO-Link, selon le type de capteur.

Le choix dépend de l'automate, du capteur et de l'architecture de l'installation.

## 8. Calcul de la position à partir d'un signal analogique

Pour un transmetteur configuré de LRV à URV et fournissant un signal de 4 à 20 mA :

Position = LRV + ((I - 4) / 16) × (URV - LRV)

Avec :
- I : courant mesuré en mA.
- LRV : valeur basse de la plage.
- URV : valeur haute de la plage.

### Exemple 1

Course : 0 à 200 mm.

Courant mesuré : 16 mA.

Position = 0 + ((16 - 4) / 16) × 200

Position = 150 mm.

### Exemple 2

Course : 0 à 500 mm.

Courant mesuré : 10,4 mA.

Position = 0 + ((10,4 - 4) / 16) × 500

Position = 200 mm.

La position correspond à 40 % de la course.

### Exemple 3

Course : 0 à 400 mm.

Courant mesuré : 12 mA.

Position = 0 + ((12 - 4) / 16) × 400

Position = 200 mm.

**Astuce :** 12 mA est le milieu de la plage 4–20 mA. La position correspond donc à 50 % de la course.

## 9. Intégration avec un automate Siemens S7-1200

Prenons un vérin hydraulique équipé d'un transmetteur de position 4–20 mA.

La course est de 0 à 200 mm.

La chaîne de mesure est :

Transmetteur de position → Entrée analogique → Programme automate → IHM WinCC.

L'automate reçoit le signal électrique et effectue la mise à l'échelle pour convertir la valeur brute en millimètres.

L'IHM peut ensuite afficher :

Position du vérin : 125 mm.

Taux de sortie : 62,5 %.

**Attention :** les entrées analogiques intégrées de la CPU S7-1200 1214C standard mesurent des tensions 0–10 V. Elles ne reçoivent pas directement un signal 4–20 mA.

Pour recevoir directement un courant, il faut utiliser un module compatible, par exemple une variante appropriée de SM 1231.

Il faut toujours vérifier la référence exacte du module et sa documentation avant de réaliser le câblage.

## 10. Diagnostic des défauts

| Anomalie constatée | Causes possibles |
|---|---|
| Position affichée égale à zéro | Absence d'alimentation, câble coupé, capteur défectueux |
| Position instable | Vibrations, mauvais câblage, perturbations électriques |
| Position incorrecte | Mauvaise mise à l'échelle, mauvais étalonnage |
| Position bloquée | Capteur bloqué, défaut mécanique, signal figé |
| Position inversée | Mauvais sens de montage ou configuration |
| Écart entre position réelle et affichée | Défaut de réglage, usure, problème mécanique |

### Exemple de diagnostic

Un vérin possède une course de 200 mm.

La position réelle est de 100 mm, mais l'IHM affiche 150 mm.

Avant de remplacer le transmetteur, le technicien doit vérifier :

1. La sortie électrique du transmetteur.
2. Le câblage entre le transmetteur et l'automate.
3. La configuration de l'entrée analogique.
4. La mise à l'échelle dans le programme automate.
5. La configuration de l'affichage dans WinCC.

**Principe de maintenance :** identifier à quel niveau apparaît l'erreur avant de remplacer un équipement.

## 11. Synthèse générale

| Instrument | Principe | Application |
|---|---|---|
| Potentiomètre linéaire | Variation de résistance | Position d'un vérin |
| Potentiomètre rotatif | Variation de résistance selon l'angle | Position d'une vanne |
| LVDT | Induction électromagnétique | Mesure précise d'un déplacement |
| Encodeur incrémental | Comptage d'impulsions | Déplacement et rotation |
| Encodeur absolu | Codage de la position | Positionnement d'axes |
| Capteur magnétique TOR | Détection d'un champ magnétique | Fin de course d'un vérin |
| Capteur magnétique analogique | Mesure magnétique du déplacement | Position continue |

### À retenir

1. La position indique où se trouve un objet.
2. Le déplacement représente la variation de position.
3. La vitesse indique la rapidité du déplacement.
4. Un détecteur de position peut fournir une information TOR.
5. Un transmetteur de position fournit une mesure exploitable sur une plage donnée.
6. Les signaux 0–10 V et 4–20 mA peuvent transmettre une mesure analogique.
7. L'automate doit convertir correctement le signal reçu en une valeur physique.
8. Le diagnostic doit porter sur toute la chaîne de mesure.

## 12. Évaluation finale

1. Quel instrument utilise une piste résistive et un curseur mobile pour mesurer une position ?
2. Quel instrument fonctionne par induction électromagnétique sans contact électrique glissant ?
3. Quelle est la différence entre un encodeur incrémental et un encodeur absolu ?
4. Un transmetteur possède une plage de 0 à 400 mm et délivre 12 mA. Quelle est la position ?
5. Deux capteurs magnétiques détectent uniquement les positions rentrée et sortie d'un vérin. Quel type d'information fournissent-ils ?

**Fin de la leçon 06 — Transmetteur de position industriel.**
