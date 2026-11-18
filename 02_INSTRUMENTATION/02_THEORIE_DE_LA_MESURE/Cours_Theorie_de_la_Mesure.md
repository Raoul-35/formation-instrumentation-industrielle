# CHAPITRE 02 — THÉORIE DE LA MESURE

## Objectifs du chapitre

À la fin de ce chapitre, l'apprenant doit être capable de :

- Expliquer les fondements théoriques d'une opération de mesure.
- Identifier les éléments qui interviennent dans un processus de mesurage.
- Comprendre les principales méthodes de mesure.
- Expliquer les principes de comparaison et d'équilibre.
- Distinguer correctement la lecture directe et la détermination indirecte.
- Exploiter les lois physiques pour déterminer une grandeur.
- Construire et interpréter un modèle mathématique simple de mesure.
- Appliquer ces connaissances à des situations industrielles.

---

# 1. FONDEMENTS ET PRINCIPES DE LA MESURE

## 1.1. Définition du mesurage

Le mesurage est un processus expérimental qui consiste à déterminer la valeur d'une grandeur physique en la comparant à une référence ou en exploitant une relation physique connue.

Une mesure ne se limite donc pas à lire un nombre sur un appareil. Elle implique plusieurs éléments :

- La grandeur que l'on souhaite déterminer.
- Le phénomène physique mis en œuvre.
- La méthode utilisée.
- Le dispositif de mesure.
- La référence ou l'étalon.
- Les conditions dans lesquelles le mesurage est effectué.
- Le résultat obtenu.

**Exemple industriel : mesure de la température d'un moteur**

Pour déterminer la température d'un palier de moteur électrique, il faut :

1. Définir précisément la température recherchée.
2. Choisir un dispositif de mesure adapté.
3. Placer le dispositif dans une position appropriée.
4. Effectuer le mesurage.
5. Exploiter la valeur obtenue.

La valeur affichée n'a de sens que si l'on sait quelle température a été mesurée, à quel endroit et dans quelles conditions.

## 1.2. Grandeur mesurée et résultat de mesure

Une grandeur mesurée doit être définie sans ambiguïté.

Par exemple, l'expression « température du moteur » est trop générale. Elle peut désigner :

- La température de l'enroulement statorique.
- La température du carter.
- La température du palier avant.
- La température du palier arrière.

Une définition correcte précise donc la nature de la grandeur et les conditions de mesurage.

Un résultat de mesure comporte généralement :

- Une valeur numérique.
- Une unité.
- Une incertitude, lorsque celle-ci est évaluée.

Exemple :

Température mesurée : 72,5 °C.

Incertitude élargie : ± 1,0 °C.

Résultat présenté :

T = (72,5 ± 1,0) °C

Cette présentation indique que la valeur mesurée est accompagnée d'une estimation de l'incertitude associée.

## 1.3. Valeur vraie et valeur mesurée

La valeur vraie correspond à la valeur de la grandeur telle qu'elle existe réellement dans les conditions considérées.

En pratique, cette valeur est généralement inaccessible avec une connaissance parfaite.

La valeur mesurée est celle obtenue à partir du processus expérimental.

Il est donc important de distinguer :

- La valeur vraie, qui constitue une référence théorique.
- La valeur mesurée, qui résulte de l'expérience.
- L'incertitude, qui caractérise le doute associé au résultat.

---

# 2. FORMALISATION MATHÉMATIQUE DU PROCESSUS DE MESURE

## 2.1. Principe général

Un processus de mesure peut être représenté par une relation mathématique entre une grandeur d'entrée et une grandeur de sortie.

On peut écrire :

Y = f(X)

Avec :

- X : grandeur d'entrée.
- Y : grandeur de sortie.
- f : relation mathématique qui décrit le fonctionnement du système.

Dans un appareil de mesure, X représente généralement la grandeur physique recherchée et Y le signal ou l'indication produit par le dispositif.

**Exemple : conversion d'une température en signal électrique**

Un transmetteur de température peut convertir une température en un courant électrique.

La relation entre la température et le courant peut être linéaire :

I = a × T + b

Avec :

- I : courant de sortie.
- T : température mesurée.
- a : coefficient de proportionnalité.
- b : terme constant.

Cette représentation permet de comprendre comment une grandeur physique est associée à une indication exploitable.

## 2.2. Modèle linéaire

Une relation linéaire peut être exprimée sous la forme :

Y = a × X + b

Dans cette expression :

- a représente la pente de la caractéristique.
- b représente l'ordonnée à l'origine.

Si b = 0, la relation devient :

Y = a × X

**Exemple : conversion d'une température en courant**

Considérons un transmetteur configuré pour mesurer une température comprise entre 0 °C et 100 °C et délivrer un courant compris entre 4 mA et 20 mA.

La relation est :

I = 0,16 × T + 4

Avec I exprimé en mA et T en °C.

Pour une température de 50 °C :

I = 0,16 × 50 + 4

I = 8 + 4

I = 12 mA

Le transmetteur délivre donc 12 mA lorsque la température mesurée est de 50 °C.

## 2.3. Détermination de la grandeur à partir du signal

Il est parfois nécessaire de retrouver la grandeur physique à partir du signal délivré par un dispositif.

À partir de :

I = 0,16 × T + 4

On isole T :

T = (I - 4) / 0,16

Si le courant mesuré est de 15,2 mA :

T = (15,2 - 4) / 0,16

T = 11,2 / 0,16

T = 70 °C

Cette opération constitue une exploitation mathématique du signal de mesure.

---

# 3. MÉTHODES ET TECHNIQUES DE MESURE

## 3.1. Méthode par déviation

La méthode par déviation consiste à déterminer une grandeur à partir de la déviation d'un indicateur ou de la variation d'un signal.

Le dispositif réagit à la grandeur mesurée et fournit une indication proportionnelle ou liée à celle-ci.

**Exemples :**

- Un ampèremètre à aiguille indique une intensité par la déviation de son aiguille.
- Un voltmètre numérique affiche une valeur correspondant à la tension mesurée.
- Un transmetteur de pression délivre un courant qui varie en fonction de la pression.

Cette méthode est largement utilisée dans les instruments industriels.

## 3.2. Méthode par zéro

La méthode par zéro consiste à comparer une grandeur inconnue à une grandeur connue jusqu'à obtenir une condition d'équilibre.

À l'équilibre, la différence entre les deux grandeurs est nulle.

On écrit :

ΔX = Xx - Xr

À l'équilibre :

ΔX = 0

Donc :

Xx = Xr

Avec :

- Xx : grandeur inconnue.
- Xr : grandeur de référence.

La grandeur inconnue est alors déterminée à partir de la référence utilisée.

**Exemple :**

Un dispositif de comparaison permet de déterminer une résistance inconnue en ajustant une résistance de référence jusqu'à obtenir une condition d'équilibre.

## 3.3. Méthode par substitution

La méthode par substitution consiste à remplacer une grandeur inconnue par une grandeur connue, dans les mêmes conditions expérimentales.

Le principe est le suivant :

1. On réalise une première mesure avec la grandeur inconnue.
2. On remplace cette grandeur par une référence connue.
3. On ajuste la référence pour retrouver la même indication.
4. On déduit la valeur de la grandeur inconnue.

Cette méthode permet de limiter certaines erreurs liées au dispositif de mesure, puisque les deux grandeurs sont comparées dans des conditions similaires.

---

# 4. MESURES PAR COMPARAISON ET PAR ÉQUILIBRE

## 4.1. Principe de la comparaison

La mesure par comparaison consiste à confronter une grandeur inconnue à une grandeur de référence de même nature.

La différence entre les deux grandeurs peut être exprimée par :

ΔX = Xx - Xr

Si ΔX est positif, la grandeur inconnue est supérieure à la référence.

Si ΔX est négatif, elle est inférieure à la référence.

Si ΔX est nul, les deux grandeurs sont égales.

## 4.2. Pont de Wheatstone

Le pont de Wheatstone est un circuit électrique utilisé pour déterminer une résistance inconnue à partir de résistances connues.

Il est constitué de quatre résistances organisées en deux branches.

Dans la configuration considérée, les résistances sont notées R1, R2, R3 et Rx.

Lorsque le pont est équilibré, la relation est :

R1 / R2 = R3 / Rx

En isolant la résistance inconnue :

Rx = (R2 × R3) / R1

**Application numérique**

On considère :

R1 = 100 Ω

R2 = 200 Ω

R3 = 150 Ω

La résistance inconnue vaut :

Rx = (200 × 150) / 100

Rx = 300 Ω

La résistance inconnue est donc égale à 300 Ω.

Cette relation correspond au repérage des résistances indiqué dans cette section. Le montage doit conserver cette disposition pour que la formule soit applicable.

## 4.3. Application aux jauges de contrainte

Une jauge de contrainte est un élément résistif dont la résistance varie lorsqu'elle subit une déformation mécanique.

La variation relative de résistance est approximativement proportionnelle à la déformation dans le domaine de fonctionnement prévu.

La relation est :

ΔR / R = K × ε

Avec :

- ΔR : variation de résistance.
- R : résistance initiale.
- K : facteur de jauge.
- ε : déformation relative.

La déformation relative est sans unité.

**Exemple industriel :**

Dans un système de pesage industriel, une force appliquée sur une structure provoque une déformation mécanique.

Les jauges de contrainte détectent cette déformation par une variation de résistance.

Un circuit en pont de Wheatstone permet ensuite de convertir cette variation en une tension électrique exploitable.

Ce principe est utilisé dans :

- Les balances industrielles.
- Les cellules de pesage.
- Les systèmes de mesure de force.
- Certains dispositifs de contrôle de contraintes mécaniques.

---

# 5. MESURES DIRECTES ET INDIRECTES

## 5.1. Détermination directe

Dans la pratique instrumentale, on parle de détermination directe lorsque l'appareil fournit directement à l'utilisateur la valeur de la grandeur recherchée.

**Exemples :**

- Un voltmètre affiche une tension en volts.
- Un thermomètre affiche une température en degrés Celsius.
- Un manomètre affiche une pression en bars.

Il faut cependant distinguer la lecture directe de la méthode de comparaison directe à une référence.

Un appareil peut afficher directement une grandeur tout en réalisant intérieurement plusieurs opérations de conversion ou de calcul.

## 5.2. Détermination indirecte

La détermination indirecte consiste à calculer une grandeur recherchée à partir d'autres grandeurs mesurées.

Elle repose sur une relation physique ou mathématique connue.

**Exemple 1 : détermination d'une résistance**

La loi d'Ohm donne :

R = U / I

On mesure :

U = 12 V

I = 2 A

La résistance vaut :

R = 12 / 2

R = 6 Ω

La résistance est déterminée indirectement à partir de la tension et du courant.

**Exemple 2 : détermination d'une puissance électrique**

Pour un circuit monophasé en courant alternatif :

P = U × I × cos φ

Avec :

- P : puissance active en watts.
- U : tension efficace en volts.
- I : courant efficace en ampères.
- cos φ : facteur de puissance.

Pour un réseau triphasé équilibré :

P = √3 × U × I × cos φ

Avec U représentant la tension composée entre phases.

Application :

U = 400 V

I = 10 A

cos φ = 0,85

P = 1,732 × 400 × 10 × 0,85

P ≈ 5 889 W

La puissance active est donc approximativement égale à 5,89 kW.

---

# 6. RELATIONS MATHÉMATIQUES ET LOIS PHYSIQUES APPLIQUÉES À LA MESURE

Les lois physiques permettent de déterminer certaines grandeurs à partir d'autres grandeurs mesurables.

Elles constituent la base de nombreuses méthodes de mesure indirecte.

## 6.1. Loi d'Ohm

Pour un conducteur ohmique :

U = R × I

Avec :

- U : tension en volts.
- R : résistance en ohms.
- I : intensité en ampères.

Les formes dérivées sont :

R = U / I

I = U / R

**Application industrielle :**

La mesure de la tension aux bornes d'un récepteur et du courant qui le traverse permet de déterminer sa résistance électrique, dans les conditions où la loi d'Ohm est applicable.

## 6.2. Puissance électrique

En courant continu ou pour un récepteur résistif :

P = U × I

Pour un circuit monophasé sinusoïdal :

P = U × I × cos φ

Pour un système triphasé équilibré :

P = √3 × U × I × cos φ

Ces relations permettent notamment de calculer la puissance électrique absorbée par un équipement industriel.

## 6.3. Fréquence et période

La fréquence représente le nombre de périodes effectuées par seconde.

La relation entre la fréquence et la période est :

f = 1 / T

Avec :

- f : fréquence en hertz (Hz).
- T : période en secondes (s).

On peut également écrire :

T = 1 / f

**Exemple :**

Pour une alimentation électrique de fréquence 50 Hz :

T = 1 / 50

T = 0,02 s

La période est donc de 20 ms.

## 6.4. Loi de Hooke

Dans le domaine élastique d'un ressort, la force appliquée est proportionnelle à son allongement.

La relation est :

F = k × x

Avec :

- F : force en newtons.
- k : raideur du ressort en N/m.
- x : allongement en mètres.

**Exemple industriel :**

Dans un dispositif de pesage mécanique, la connaissance de la raideur d'un élément élastique permet de déterminer la force appliquée à partir de son déplacement.

## 6.5. Variation de la résistance avec la température

Pour certains conducteurs métalliques et dans une plage de température limitée, la résistance varie approximativement de manière linéaire avec la température.

La relation est :

R(T) = R0 × [1 + α × (T - T0)]

Avec :

- R(T) : résistance à la température T.
- R0 : résistance à la température de référence T0.
- α : coefficient de température du matériau.
- T : température considérée.
- T0 : température de référence.

Cette relation est notamment utilisée pour comprendre le principe des sondes résistives de température.

---

# 7. CONSTRUCTION ET ANALYSE D'UN MODÈLE DE MESURE

## 7.1. Notion de modèle de mesure

Un modèle de mesure représente mathématiquement le lien entre la grandeur recherchée et les indications fournies par un dispositif.

Il permet de comprendre comment les mesures sont transformées en résultats exploitables.

Un modèle simple peut prendre la forme :

Y = a × X + b

Un modèle plus complexe peut comporter plusieurs grandeurs d'entrée :

Y = f(X1, X2, X3, ...)

Dans ce cas, la sortie dépend de plusieurs variables.

## 7.2. Identification des variables

Pour établir un modèle, il faut identifier :

1. La grandeur recherchée.
2. Les grandeurs mesurées.
3. Les paramètres physiques connus.
4. Les relations entre les différentes grandeurs.
5. Les unités utilisées.

**Exemple : détermination de la puissance électrique**

La puissance active d'un récepteur monophasé dépend de trois grandeurs :

P = U × I × cos φ

Les variables sont :

- U : tension.
- I : courant.
- cos φ : facteur de puissance.

Le modèle permet de calculer la puissance à partir de ces trois données.

## 7.3. Vérification de la cohérence d'un modèle

Un modèle doit respecter plusieurs conditions :

- Les relations physiques utilisées doivent être applicables.
- Les unités doivent être cohérentes.
- Les paramètres doivent être correctement identifiés.
- Les résultats doivent être compatibles avec le domaine de fonctionnement étudié.

**Exemple :**

La relation :

R = U / I

donne une résistance en ohms si U est exprimée en volts et I en ampères.

En revanche, utiliser une tension exprimée en kilovolts et un courant exprimé en milliampères sans conversion préalable peut conduire à une erreur d'unité.

## 7.4. Limites d'un modèle

Un modèle mathématique représente une situation physique avec un certain niveau de simplification.

Il peut ne pas tenir compte de certains phénomènes :

- Non-linéarité.
- Échauffement.
- Vieillissement.
- Saturation.
- Variation des propriétés physiques.

Il faut donc toujours vérifier que les hypothèses du modèle sont compatibles avec la situation étudiée.

---

# 8. ÉTUDES DE CAS INDUSTRIELS

## 8.1. Cas 1 : mesure de la puissance d'un moteur triphasé

Un moteur triphasé fonctionne sous les conditions suivantes :

- Tension composée : 400 V.
- Courant : 12 A.
- Facteur de puissance : 0,82.

La puissance active absorbée est :

P = √3 × U × I × cos φ

P = 1,732 × 400 × 12 × 0,82

P ≈ 6 819 W

La puissance active absorbée est donc approximativement égale à 6,82 kW.

Cette valeur peut être utilisée dans le suivi énergétique du moteur.

## 8.2. Cas 2 : détermination de la résistance d'un élément chauffant

Un élément chauffant est alimenté sous une tension de 230 V et absorbe un courant de 10 A.

La résistance équivalente est :

R = U / I

R = 230 / 10

R = 23 Ω

Cette détermination permet de vérifier la cohérence électrique de l'élément chauffant.

## 8.3. Cas 3 : conversion d'un signal de pression

Un transmetteur de pression possède les caractéristiques suivantes :

- Étendue de mesure : 0 à 10 bar.
- Signal de sortie : 4 à 20 mA.

La relation entre la pression et le courant est :

I = 1,6 × P + 4

Avec I en mA et P en bar.

Si le courant mesuré vaut 12 mA :

P = (I - 4) / 1,6

P = (12 - 4) / 1,6

P = 5 bar

La pression correspondante est de 5 bar.

---

# 9. EXERCICES D'APPLICATION

## Exercice 1 : modèle linéaire

Un transmetteur de température mesure une température comprise entre 0 °C et 200 °C et délivre un signal de 4 à 20 mA.

1. Déterminer la pente de la relation.
2. Établir l'équation reliant le courant à la température.
3. Calculer le courant délivré pour une température de 125 °C.
4. Déterminer la température correspondant à un courant de 10 mA.

## Exercice 2 : pont de Wheatstone

Un pont de Wheatstone est équilibré avec les résistances suivantes :

- R1 = 120 Ω.
- R2 = 240 Ω.
- R3 = 180 Ω.

1. Écrire la relation d'équilibre.
2. Déterminer la résistance inconnue Rx.
3. Expliquer le principe physique de cette méthode.

## Exercice 3 : mesure indirecte

Un récepteur monophasé fonctionne sous une tension de 230 V. Le courant mesuré est de 8 A et le facteur de puissance est de 0,9.

1. Écrire la relation de la puissance active.
2. Calculer la puissance active absorbée.
3. Expliquer pourquoi il s'agit d'une détermination indirecte.

## Exercice 4 : loi de Hooke

Un ressort possède une raideur de 2 000 N/m. Il subit un allongement de 5 mm.

1. Convertir l'allongement en mètres.
2. Écrire la relation applicable.
3. Déterminer la force exercée.

## Exercice 5 : fréquence et période

Un signal électrique possède une fréquence de 60 Hz.

1. Écrire la relation entre fréquence et période.
2. Calculer sa période en secondes.
3. Exprimer le résultat en millisecondes.

---

# 10. ÉVALUATION GÉNÉRALE

L'évaluation de ce chapitre doit vérifier la capacité de l'apprenant à :

- Expliquer les fondements d'une opération de mesure.
- Identifier les grandeurs et les paramètres d'un modèle.
- Distinguer les méthodes par déviation, par zéro et par substitution.
- Expliquer le principe d'un montage de comparaison.
- Exploiter les relations mathématiques et les lois physiques.
- Réaliser une détermination directe ou indirecte.
- Vérifier la cohérence des résultats obtenus.
- Appliquer les méthodes étudiées à des situations industrielles.

---

# CONCLUSION DU CHAPITRE

La théorie de la mesure permet de comprendre les principes scientifiques qui se trouvent derrière les opérations de mesurage.

Elle montre qu'une mesure ne se limite pas à l'utilisation d'un instrument : elle repose sur une méthode, une référence, une relation physique et une exploitation rigoureuse des résultats.

Les méthodes de comparaison, d'équilibre, de déviation et de substitution constituent des approches fondamentales de la mesure.

La formalisation mathématique permet quant à elle de relier les grandeurs physiques aux indications fournies par les dispositifs de mesure.

Ces connaissances constituent une base nécessaire pour aborder la modélisation des systèmes de mesure, l'étude de la chaîne de mesure et l'exploitation des résultats en instrumentation industrielle.
