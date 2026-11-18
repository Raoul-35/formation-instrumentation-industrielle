# CHAPITRE 02 — THÉORIE DE LA MESURE

**Formation :** Instrumentation industrielle  
**Niveau :** Licence technologique GEII  
**Module :** 02 — Instrumentation  
**Domaine :** Fondements scientifiques et mathématiques de la mesure

---

# OBJECTIF GÉNÉRAL

Comprendre les fondements physiques, scientifiques et mathématiques qui permettent de réaliser une mesure, d'interpréter un résultat et d'établir une relation entre une grandeur physique et sa valeur mesurée.

# OBJECTIFS SPÉCIFIQUES

À la fin de ce chapitre, l'apprenant devra être capable de :

- Expliquer les principes fondamentaux de la mesure.
- Identifier les éléments intervenant dans un processus de mesure.
- Distinguer les différentes méthodes de mesure.
- Comprendre les principes de comparaison et d'équilibre.
- Établir des relations mathématiques entre grandeurs physiques.
- Analyser les phénomènes physiques intervenant dans une mesure.
- Interpréter les résultats obtenus dans une application industrielle.

# PLAN DU CHAPITRE

1. Fondements et principes de la mesure.
2. Grandeur à mesurer et principe de mesurage.
3. Méthodes et techniques de mesure.
4. Mesures par comparaison et par équilibre.
5. Mesures directes et indirectes.
6. Relations mathématiques et lois physiques appliquées à la mesure.
7. Synthèse générale.
8. Exercices d'application et études de cas industriels.
9. Évaluation générale.

# APPROCHE PÉDAGOGIQUE

Chaque partie comporte des explications théoriques, des relations mathématiques, des démonstrations, des exemples industriels et des exercices progressifs.

---

# PARTIE I — FONDEMENTS ET PRINCIPES DE LA MESURE

## 1.1. Définition de la mesure

La mesure est une opération expérimentale qui consiste à déterminer la valeur d'une grandeur physique en la comparant à une référence de même nature ou en établissant une relation entre cette grandeur et d'autres grandeurs connues.

Elle permet de transformer une observation physique en un résultat quantifiable et exploitable.

Exemples :

- Mesurer la température d'un palier de moteur.
- Déterminer la pression dans une conduite.
- Mesurer le courant absorbé par une pompe.
- Déterminer la résistance électrique d'un enroulement.
- Mesurer la vitesse de rotation d'un arbre.

Une mesure ne consiste donc pas simplement à lire une valeur sur un appareil. Elle repose sur un principe physique, une méthode expérimentale et une interprétation du résultat.

## 1.2. Les éléments fondamentaux d'une mesure

Un processus de mesure fait intervenir plusieurs éléments.

| Élément | Définition |
|---|---|
| Mesurande | Grandeur que l'on cherche à mesurer. |
| Instrument | Dispositif utilisé pour effectuer la mesure. |
| Méthode de mesure | Procédure utilisée pour obtenir le résultat. |
| Référence | Valeur ou étalon servant de base à la comparaison. |
| Conditions de mesure | Conditions dans lesquelles l'opération est réalisée. |
| Résultat | Valeur obtenue à l'issue du processus de mesure. |

Exemple : mesure de la tension aux bornes d'un moteur.

- Mesurande : tension électrique.
- Instrument : voltmètre.
- Méthode : mesure par déviation ou conversion électronique.
- Référence : référence interne de l'instrument, selon son principe de fonctionnement.
- Résultat : valeur affichée en volts.

## 1.3. Principe général de la mesure

Le principe fondamental consiste à établir une relation entre la grandeur inconnue et une référence ou un phénomène physique connu.

On peut représenter le processus de manière générale par :

\[
Y=f(X)
\]

Avec :

- \(X\) : grandeur physique d'entrée.
- \(Y\) : grandeur obtenue à la sortie du processus de mesure.
- \(f\) : relation physique ou mathématique entre les deux grandeurs.

Dans le cas particulier d'une relation linéaire :

\[
Y=aX+b
\]

Où :

- \(a\) représente le coefficient de proportionnalité ou la sensibilité.
- \(b\) représente le décalage ou l'offset.

Cette représentation générale sera approfondie dans le chapitre consacré à la modélisation des systèmes de mesure.

## 1.4. La mesure comme opération expérimentale

Une mesure repose sur une interaction entre un phénomène physique et un dispositif expérimental.

Prenons l'exemple d'une mesure de résistance par méthode voltampèremétrique.

On applique une tension aux bornes d'une résistance inconnue et on mesure le courant qui la traverse.

La relation physique exploitée est la loi d'Ohm :

\[
U=RI
\]

La résistance recherchée peut alors être déterminée par :

\[
R=\frac{U}{I}
\]

La mesure repose ici sur l'exploitation de deux grandeurs électriques observées et d'une loi physique connue.

## 1.5. Les limites de la mesure

Une mesure réelle ne fournit jamais une connaissance absolument parfaite de la grandeur recherchée.

Plusieurs facteurs peuvent influencer le résultat :

- Les limites de l'instrument.
- Les conditions expérimentales.
- La méthode utilisée.
- Les phénomènes physiques exploités.
- Les perturbations extérieures.
- Les interactions entre l'instrument et le phénomène mesuré.

Il faut donc distinguer la valeur recherchée, la valeur obtenue et les limites de confiance associées au résultat.

---

# PARTIE II — GRANDEUR À MESURER ET PRINCIPE DE MESURAGE

## 2.1. Définition du mesurande

Le mesurande est la grandeur particulière que l'on veut mesurer.

Sa définition doit être suffisamment précise pour éviter toute ambiguïté.

Par exemple, dire simplement « mesurer la température du moteur » n'est pas toujours suffisant.

Il faut préciser :

- La partie du moteur concernée.
- Le point de mesure.
- La nature de la grandeur.
- Les conditions de fonctionnement.
- Le moment de la mesure.

Une définition plus rigoureuse serait :

« Température de la surface extérieure du palier avant d'un moteur électrique, exprimée en degrés Celsius, mesurée pendant son fonctionnement normal. »

La précision de cette définition est importante, car deux points différents d'une même machine peuvent présenter des températures différentes.

## 2.2. Nature et caractéristiques du mesurande

Un mesurande peut être caractérisé par plusieurs propriétés.

### A. Sa nature physique

Il peut s'agir d'une grandeur :

- Électrique.
- Thermique.
- Mécanique.
- Hydraulique.
- Chimique.

### B. Son unité

Toute grandeur doit être exprimée dans une unité appropriée.

Exemples :

| Grandeur | Unité |
|---|---|
| Tension | Volt (V) |
| Courant | Ampère (A) |
| Résistance | Ohm (Ω) |
| Température | Degré Celsius (°C) ou kelvin (K) |
| Pression | Pascal (Pa) ou bar |
| Vitesse de rotation | Tour par minute (tr/min) |
| Force | Newton (N) |

### C. Sa localisation

Une grandeur physique peut varier selon la position.

Exemple : la température du palier avant d'un moteur peut être différente de celle du palier arrière.

### D. Son évolution temporelle

Une grandeur peut être constante ou variable dans le temps.

On peut représenter son évolution par une fonction :

\[
X=f(t)
\]

Où \(t\) représente le temps.

## 2.3. Grandeur instantanée et grandeur moyenne

Lorsqu'une grandeur varie dans le temps, il est important de préciser la valeur recherchée.

### A. Valeur instantanée

C'est la valeur de la grandeur à un instant déterminé.

\[
X=X(t)
\]

### B. Valeur moyenne

Pour une grandeur continue sur un intervalle de durée \(T\) :

\[
X_{\text{moy}}=\frac{1}{T}\int_0^T X(t)\,dt
\]

Pour un ensemble de \(n\) mesures discrètes :

\[
X_{\text{moy}}=\frac{1}{n}\sum_{i=1}^{n}X_i
\]

Exemple :

On relève les pressions suivantes dans une conduite :

\[
5;\ 5,5;\ 6;\ 6,5;\ 6\ \text{bar}
\]

La moyenne vaut :

\[
P_{\text{moy}}=\frac{5+5,5+6+6,5+6}{5}
\]

\[
\boxed{P_{\text{moy}}=5,8\ \text{bar}}
\]

La moyenne ne renseigne cependant pas, à elle seule, sur les variations de la pression.

## 2.4. Valeur efficace d'une grandeur périodique

La valeur efficace, ou valeur RMS, est particulièrement importante en électrotechnique.

Elle correspond à la valeur d'une grandeur continue qui produirait le même effet thermique dans une résistance.

Pour un signal périodique \(x(t)\) de période \(T\) :

\[
X_{\text{eff}}=
\sqrt{\frac{1}{T}\int_0^T x^2(t)\,dt}
\]

Pour une tension sinusoïdale :

\[
U_{\text{eff}}=\frac{U_{\max}}{\sqrt{2}}
\]

Ainsi, une tension de 230 V efficaces possède une valeur maximale approximative de :

\[
U_{\max}=230\sqrt{2}
\]

\[
\boxed{U_{\max}\approx325,3\ V}
\]

Cette distinction est essentielle pour interpréter correctement les mesures électriques.

## 2.5. Conditions physiques du mesurande

La valeur d'une grandeur peut dépendre d'autres paramètres physiques.

Exemple : la résistance électrique d'un conducteur métallique dépend de sa température.

Une approximation de cette dépendance est :

\[
R(T)=R_0[1+\alpha(T-T_0)]
\]

Avec :

- \(R(T)\) : résistance à la température \(T\).
- \(R_0\) : résistance à la température de référence \(T_0\).
- \(\alpha\) : coefficient de température de la résistance.

Application : lors d'un contrôle des enroulements d'un moteur, les températures doivent être prises en compte pour comparer correctement les résistances mesurées.

---

# PARTIE III — MÉTHODES ET TECHNIQUES DE MESURE

## 3.1. Méthode par déviation

La méthode par déviation consiste à déterminer une grandeur en observant le déplacement d'un indicateur ou la variation d'un signal de sortie.

Exemples :

- Un ampèremètre analogique.
- Un voltmètre à aiguille.
- Un manomètre à tube de Bourdon.
- Un thermomètre à cadran.

Le déplacement de l'indicateur est lié à la grandeur mesurée.

Pour un instrument idéalement linéaire :

\[
Y=aX+b
\]

La valeur recherchée peut être déterminée à partir de la position de l'indicateur.

**Avantage :** lecture relativement simple et rapide.

**Limite :** la qualité du résultat dépend notamment de la résolution, de la sensibilité et des caractéristiques de l'instrument.

## 3.2. Méthode du zéro

La méthode du zéro consiste à ajuster une grandeur de référence jusqu'à ce que la différence entre la grandeur inconnue et la référence devienne nulle.

On peut écrire :

\[
\Delta X=X_x-X_r
\]

À l'équilibre :

\[
\boxed{\Delta X=0}
\]

Donc :

\[
X_x=X_r
\]

Exemple : dans un pont de Wheatstone, on ajuste une résistance connue jusqu'à obtenir un équilibre électrique.

Lorsque le galvanomètre indique un courant nul, la relation d'équilibre permet de calculer la résistance inconnue.

## 3.3. Méthode de substitution

La méthode de substitution consiste à remplacer une grandeur inconnue par une grandeur de référence réglable, de manière à reproduire le même effet expérimental.

Exemple :

1. On branche une résistance inconnue dans un circuit.
2. On relève une indication de 5 mA.
3. On remplace la résistance inconnue par une résistance étalon réglable.
4. On ajuste cette résistance jusqu'à retrouver exactement 5 mA.
5. La valeur de la résistance étalon permet de déterminer celle de la résistance inconnue, sous réserve que les conditions expérimentales soient identiques.

Cette méthode peut réduire certaines erreurs liées à l'instrumentation, car les deux mesures utilisent le même dispositif dans des conditions comparables.

Elle ne supprime cependant pas toutes les incertitudes.

## 3.4. Comparaison des méthodes

| Méthode | Principe | Exemple |
|---|---|---|
| Déviation | Observation d'une indication | Ampèremètre analogique |
| Zéro | Recherche d'un équilibre | Pont de Wheatstone |
| Substitution | Remplacement par une référence produisant le même effet | Mesure d'une résistance |

---

# PARTIE IV — MESURES PAR COMPARAISON ET PAR ÉQUILIBRE

## 4.1. Principe de comparaison

Une mesure par comparaison consiste à confronter une grandeur inconnue à une grandeur de référence de même nature.

Exemple : déterminer une masse en la comparant à des masses étalons.

L'objectif est d'établir une relation entre la grandeur inconnue et la référence.

## 4.2. Principe d'équilibre

L'équilibre est atteint lorsque les effets associés à deux grandeurs opposées ou comparées se compensent.

Mathématiquement :

\[
\Delta X=X_x-X_r
\]

À l'équilibre :

\[
\Delta X=0
\]

Donc :

\[
X_x=X_r
\]

Ce principe est exploité dans plusieurs dispositifs de mesure.

## 4.3. Application : pont de Wheatstone

Le pont de Wheatstone est un circuit électrique permettant de déterminer une résistance inconnue par équilibre.

Il comporte :

- Quatre résistances disposées en pont.
- Une source d'alimentation.
- Un galvanomètre ou un détecteur de différence de potentiel.

Lorsque le pont est équilibré, le courant dans le galvanomètre est nul.

Pour le montage considéré :

\[
\frac{R_1}{R_2}=\frac{R_3}{R_x}
\]

On en déduit :

\[
\boxed{R_x=\frac{R_2R_3}{R_1}}
\]

### Exemple numérique

Données :

\[
R_1=100\ \Omega
\]

\[
R_2=200\ \Omega
\]

\[
R_3=150\ \Omega
\]

La résistance inconnue vaut :

\[
R_x=\frac{200\times150}{100}
\]

\[
\boxed{R_x=300\ \Omega}
\]

Le résultat est obtenu sans mesurer directement le courant traversant la résistance inconnue.

## 4.4. Application aux capteurs résistifs

Le principe du pont de Wheatstone est également utilisé avec certains éléments résistifs sensibles aux variations physiques.

Exemple : une jauge de contrainte.

Lorsqu'une pièce mécanique subit une déformation, la résistance de la jauge varie.

Cette variation provoque un déséquilibre du pont et fait apparaître une tension différentielle.

La chaîne physique est :

\[
\text{Force}
\rightarrow
\text{Déformation}
\rightarrow
\text{Variation de résistance}
\rightarrow
\text{Déséquilibre du pont}
\rightarrow
\text{Tension électrique}
\]

Applications :

- Cellules de pesage.
- Pesage industriel de silos.
- Bancs d'essai mécaniques.
- Mesure des contraintes sur des structures.

---

# PARTIE V — MESURES DIRECTES ET INDIRECTES

## 5.1. Mesure directe

Dans le sens pratique, une mesure est dite directe lorsque l'instrument fournit directement à l'opérateur la valeur recherchée, sans qu'il ait à effectuer un calcul à partir d'autres mesures.

Exemples :

- Lecture d'une tension sur un voltmètre.
- Lecture d'une pression sur un manomètre.
- Lecture d'une température sur un thermomètre numérique.

Cette notion ne signifie pas que l'instrument ne réalise aucun traitement interne.

Un multimètre numérique peut effectuer des conversions et des calculs électroniques avant d'afficher une résistance.

## 5.2. Mesure indirecte

Une mesure est indirecte lorsque la grandeur recherchée est déterminée par calcul à partir d'autres grandeurs mesurées.

La relation utilisée repose sur une loi physique ou mathématique.

Exemple : détermination d'une résistance par la loi d'Ohm.

\[
R=\frac{U}{I}
\]

Si :

\[
U=24\ V
\]

et :

\[
I=0,4\ A
\]

Alors :

\[
R=\frac{24}{0,4}
\]

\[
\boxed{R=60\ \Omega}
\]

La résistance est obtenue à partir de deux mesures électriques.

## 5.3. Application à la puissance électrique triphasée

Dans un système triphasé équilibré, la puissance active peut être déterminée par :

\[
P=\sqrt{3}UI\cos\varphi
\]

Avec :

- \(P\) : puissance active en watts.
- \(U\) : tension composée en volts.
- \(I\) : courant de ligne en ampères.
- \(\cos\varphi\) : facteur de puissance.

Exemple :

\[
U=400\ V
\]

\[
I=10\ A
\]

\[
\cos\varphi=0,85
\]

Alors :

\[
P=\sqrt{3}\times400\times10\times0,85
\]

\[
\boxed{P\approx5889\ W}
\]

La puissance active est déterminée indirectement à partir de trois grandeurs mesurées.

## 5.4. Différence entre les deux approches

| Critère | Mesure directe | Mesure indirecte |
|---|---|---|
| Principe | Lecture de la grandeur recherchée | Calcul à partir d'autres grandeurs |
| Données | Une indication exploitable | Plusieurs grandeurs mesurées |
| Traitement | Généralement simple pour l'opérateur | Relation mathématique nécessaire |
| Exemple | Tension affichée par un voltmètre | Résistance calculée par \(R=U/I\) |

**Attention :** mesure directe au sens pratique et comparaison directe à un étalon sont deux notions différentes. Il ne faut pas les confondre.

---

# PARTIE VI — RELATIONS MATHÉMATIQUES ET LOIS PHYSIQUES APPLIQUÉES À LA MESURE

## 6.1. Importance des relations physiques

La mesure expérimentale ne se limite pas à obtenir des valeurs numériques.

Elle permet également de vérifier, d'exploiter ou de déterminer des relations entre plusieurs grandeurs physiques.

Ces relations constituent la base de nombreuses méthodes de mesure indirecte.

## 6.2. Loi d'Ohm

La loi d'Ohm établit la relation entre la tension, le courant et la résistance d'un conducteur ohmique dans les conditions où cette loi est applicable.

\[
U=RI
\]

Formes dérivées :

\[
R=\frac{U}{I}
\]

\[
I=\frac{U}{R}
\]

### Application industrielle

On mesure une tension de 48 V aux bornes d'une résistance et un courant de 2 A.

\[
R=\frac{48}{2}
\]

\[
\boxed{R=24\ \Omega}
\]

Cette méthode permet de déterminer une résistance sans utiliser directement un ohmmètre.

## 6.3. Puissance électrique

Pour un circuit électrique continu :

\[
P=UI
\]

Pour un circuit monophasé sinusoïdal :

\[
P=UI\cos\varphi
\]

Pour un système triphasé équilibré :

\[
P=\sqrt{3}UI\cos\varphi
\]

Ces relations permettent de déterminer la puissance à partir de mesures électriques.

## 6.4. Fréquence et période

La fréquence représente le nombre de périodes réalisées pendant une seconde.

\[
f=\frac{1}{T}
\]

Avec :

- \(f\) : fréquence en hertz.
- \(T\) : période en secondes.

Exemple :

Un signal électrique possède une période de :

\[
T=20\ ms=0,020\ s
\]

Sa fréquence vaut :

\[
f=\frac{1}{0,020}
\]

\[
\boxed{f=50\ Hz}
\]

Cette relation est notamment utilisée pour déterminer la fréquence d'un réseau électrique à partir de l'observation de sa période.

## 6.5. Mesure d'une grandeur par effet physique

Certaines méthodes de mesure reposent sur la conversion d'une grandeur physique en une autre grandeur exploitable.

Exemple : mesure d'une force par déformation élastique.

Dans le domaine élastique, la loi de Hooke s'écrit :

\[
F=kx
\]

Avec :

- \(F\) : force appliquée en newtons.
- \(k\) : raideur du ressort en N/m.
- \(x\) : allongement en mètres.

On peut donc déterminer la force à partir de l'allongement :

\[
F=kx
\]

Exemple :

\[
k=2000\ N/m
\]

\[
x=0,005\ m
\]

Alors :

\[
F=2000\times0,005
\]

\[
\boxed{F=10\ N}
\]

Cette relation illustre le principe général d'une mesure indirecte fondée sur une loi physique.

## 6.6. Exploitation des mesures répétées

Lorsqu'une même grandeur est mesurée plusieurs fois dans des conditions comparables, les résultats peuvent être exploités statistiquement.

Pour \(n\) mesures :

\[
x_1,x_2,\ldots,x_n
\]

La moyenne arithmétique est :

\[
\overline{x}=\frac{1}{n}\sum_{i=1}^{n}x_i
\]

L'écart-type expérimental d'un échantillon est :

\[
s=\sqrt{\frac{\sum_{i=1}^{n}(x_i-\overline{x})^2}{n-1}}
\]

Ces calculs permettent notamment de caractériser la dispersion des résultats.

L'étude complète des erreurs, des incertitudes et de leur exploitation a déjà été développée dans le chapitre consacré à la métrologie.

---

# PARTIE VII — SYNTHÈSE GÉNÉRALE

La théorie de la mesure permet de comprendre les principes scientifiques sur lesquels repose toute opération de mesurage.

Les notions fondamentales à retenir sont :

1. Toute mesure repose sur un phénomène physique exploitable.
2. Le mesurande doit être défini avec précision.
3. La méthode expérimentale dépend du phénomène étudié et du résultat recherché.
4. Une mesure peut reposer sur une déviation, un équilibre ou une substitution.
5. La comparaison permet de relier une grandeur inconnue à une référence.
6. Une grandeur peut être déterminée directement ou indirectement.
7. Les lois physiques permettent d'établir des relations mathématiques entre les grandeurs.
8. Les mesures répétées peuvent être exploitées statistiquement.

La théorie de la mesure constitue ainsi une base indispensable pour comprendre la modélisation des systèmes de mesure et la réalisation des chaînes de mesure industrielles.

---

# PARTIE VIII — EXERCICES D'APPLICATION ET ÉTUDES DE CAS INDUSTRIELS

## Exercice 1 — Détermination d'une résistance

Un technicien mesure une tension de 36 V aux bornes d'un composant et un courant de 1,5 A qui le traverse.

1. Déterminer la résistance du composant.
2. Préciser s'il s'agit d'une mesure directe ou indirecte de la résistance.
3. Donner la loi physique utilisée.

## Exercice 2 — Équilibre d'un pont de Wheatstone

Un pont de Wheatstone est équilibré avec les valeurs suivantes :

\[
R_1=120\ \Omega
\]

\[
R_2=240\ \Omega
\]

\[
R_3=180\ \Omega
\]

Déterminer la résistance inconnue \(R_x\).

## Exercice 3 — Puissance triphasée

Un moteur triphasé fonctionne sous les conditions suivantes :

- Tension composée : 400 V.
- Courant de ligne : 12 A.
- Facteur de puissance : 0,82.

1. Calculer la puissance active absorbée.
2. Préciser pourquoi cette détermination est indirecte.

## Exercice 4 — Exploitation d'une série de mesures

Un technicien relève les températures suivantes sur un palier de moteur :

\[
62;\ 64;\ 63;\ 65;\ 66;\ 64\ ^\circ C
\]

1. Calculer la température moyenne.
2. Déterminer la température minimale.
3. Déterminer la température maximale.
4. Calculer l'étendue des mesures.

## Exercice 5 — Détermination d'une fréquence

Un oscilloscope permet de mesurer une période de 16 ms.

1. Convertir cette période en secondes.
2. Calculer la fréquence du signal.
3. Interpréter le résultat.

## Exercice 6 — Application de la loi de Hooke

Un dispositif mécanique possède une raideur de 5000 N/m. Lorsqu'une force est appliquée, son allongement mesuré est de 3 mm.

1. Convertir l'allongement en mètres.
2. Calculer la force appliquée.
3. Identifier la relation physique exploitée.

## Exercice 7 — Étude de cas : contrôle d'un moteur électrique

Lors d'une opération de maintenance, un technicien doit déterminer la résistance électrique d'un enroulement moteur.

Il dispose :
- D'une alimentation continue.
- D'un voltmètre.
- D'un ampèremètre.
- De câbles de raccordement.

Les mesures obtenues sont :

\[
U=24\ V
\]

\[
I=0,8\ A
\]

Questions :

1. Quelle est la grandeur recherchée ?
2. Quelles sont les grandeurs directement observées ?
3. Quelle loi physique doit être utilisée ?
4. Calculer la résistance de l'enroulement.
5. Pourquoi faut-il préciser la température de l'enroulement lors de cette mesure ?

---

# PARTIE IX — ÉVALUATION GÉNÉRALE

## Questions de connaissances

**Question 1 :** Comment définit-on le mesurande ?

**Question 2 :** Quelle est la différence entre une mesure directe au sens pratique et une mesure indirecte ?

**Question 3 :** Quel est le principe fondamental de la méthode du zéro ?

**Question 4 :** Pourquoi utilise-t-on un pont de Wheatstone ?

**Question 5 :** Quelle relation mathématique permet de déterminer une résistance à partir d'une tension et d'un courant ?

## Questions de raisonnement

**Question 6 :** Pourquoi deux mesures de résistance d'un même enroulement peuvent-elles donner des résultats différents si elles sont réalisées à des températures différentes ?

**Question 7 :** Pourquoi la valeur moyenne d'une grandeur variable ne suffit-elle pas toujours à caractériser son comportement ?

**Question 8 :** Un instrument affiche directement une valeur de résistance, mais réalise intérieurement une mesure de tension et de courant. Pourquoi peut-on néanmoins parler de mesure directe au sens pratique ?

## Problème de synthèse

Un moteur triphasé est alimenté sous 400 V. Le courant de ligne mesuré est de 15 A et son facteur de puissance est de 0,80.

1. Calculer la puissance active absorbée.
2. Identifier les grandeurs mesurées.
3. Identifier la grandeur déterminée par calcul.
4. Justifier pourquoi cette détermination constitue une mesure indirecte.

---

# FIN DU CHAPITRE 02 — THÉORIE DE LA MESURE
