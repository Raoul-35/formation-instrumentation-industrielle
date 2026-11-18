# CHAPITRE 02 — THÉORIE DE LA MESURE

**Formation :** Instrumentation industrielle  
**Niveau :** Licence technologique GEII  
**Module :** 02 — Instrumentation

---

# OBJECTIFS DU CHAPITRE

## Objectif général

Comprendre les fondements physiques, scientifiques et mathématiques de la mesure afin de maîtriser les principes qui permettent de déterminer une grandeur physique, d'interpréter le résultat obtenu et d'établir une relation entre la grandeur recherchée et les observations expérimentales.

## Objectifs spécifiques

À la fin de ce chapitre, l'apprenant doit être capable de :

- Expliquer les principes fondamentaux du mesurage.
- Identifier et caractériser une grandeur à mesurer.
- Expliquer les différentes méthodes de mesure.
- Distinguer les méthodes par déviation, par zéro et par substitution.
- Comprendre les principes de comparaison et d'équilibre.
- Distinguer les déterminations directes et indirectes.
- Établir des relations mathématiques entre les grandeurs physiques.
- Appliquer les lois physiques à des situations de mesure industrielles.
- Interpréter les résultats obtenus lors d'une opération de mesure.

## PLAN DU CHAPITRE

1. Fondements et principes de la mesure.
2. Grandeur à mesurer et principe de mesurage.
3. Méthodes et techniques de mesure.
4. Mesures par comparaison et par équilibre.
5. Mesures directes et indirectes.
6. Relations mathématiques et lois physiques appliquées à la mesure.
7. Synthèse générale.
8. Exercices d'application.
9. Évaluation générale.

---

# 1. FONDEMENTS ET PRINCIPES DE LA MESURE

## 1.1. Définition de la mesure

La mesure est une opération expérimentale qui consiste à établir une relation entre une grandeur physique inconnue et une référence de même nature, afin de déterminer une valeur représentative de cette grandeur.

Par exemple, mesurer une tension électrique consiste à déterminer sa valeur en la comparant, directement ou indirectement, à une référence électrique connue.

La mesure ne consiste donc pas simplement à lire une valeur sur un appareil. Elle repose sur un principe physique, une méthode expérimentale et une relation entre plusieurs grandeurs.

## 1.2. Les éléments fondamentaux d'une opération de mesure

Une opération de mesure comporte plusieurs éléments.

| Élément | Signification | Exemple industriel |
|---|---|---|
| Grandeur à mesurer | Grandeur physique recherchée | Température d'un palier |
| Système de mesure | Ensemble utilisé pour réaliser la mesure | Ensemble capteur et électronique |
| Méthode de mesure | Principe expérimental utilisé | Comparaison ou déviation |
| Instrument | Appareil utilisé pour obtenir une indication | Multimètre |
| Référence | Valeur ou grandeur servant de comparaison | Résistance étalon |
| Résultat | Valeur obtenue à l'issue du mesurage | 12,5 Ω |
| Conditions de mesure | Conditions dans lesquelles la mesure est réalisée | Température ambiante, fonctionnement |

## 1.3. Principe général de la mesure

Le principe fondamental consiste à établir une relation entre la grandeur recherchée et une référence connue.

Cette relation peut être représentée de manière générale par :

\[
Y=f(X)
\]

Avec :

- \(X\) : grandeur physique recherchée ou grandeur d'entrée ;
- \(Y\) : grandeur obtenue ou indication de mesure ;
- \(f\) : relation physique ou mathématique entre les deux grandeurs.

Dans le cas particulier d'une relation linéaire :

\[
Y=aX+b
\]

Où :

- \(a\) représente le coefficient de proportionnalité ou la sensibilité ;
- \(b\) représente le décalage ou l'offset.

**Exemple :**

Un dispositif de mesure de température fournit une tension selon la relation idéale :

\[
U=0,01T
\]

Pour une température de 80 °C :

\[
U=0,01\times80
\]

\[
\boxed{U=0,8\ V}
\]

Cette relation permet de déterminer la température à partir de la tension mesurée.

## 1.4. Le mesurage comme opération expérimentale

Le mesurage désigne l'ensemble des opérations expérimentales permettant d'obtenir un résultat de mesure.

Il comprend notamment :

1. La définition de la grandeur recherchée.
2. Le choix du principe et de la méthode de mesure.
3. La mise en place des conditions expérimentales.
4. L'acquisition des observations.
5. L'exploitation des observations.
6. L'établissement du résultat.

Une erreur dans la définition de la grandeur recherchée ou dans la réalisation de l'expérience peut conduire à un résultat qui ne représente pas correctement le phénomène étudié.

## 1.5. Valeur vraie, valeur conventionnelle et résultat de mesure

### a) Valeur vraie

La valeur vraie est la valeur que possède réellement une grandeur dans des conditions déterminées.

En pratique, elle est généralement impossible à connaître exactement.

### b) Valeur conventionnelle

La valeur conventionnelle est une valeur attribuée à une grandeur et considérée comme suffisamment proche de sa valeur vraie pour un usage donné.

Elle peut notamment être obtenue à partir d'un étalon ou d'une méthode de référence.

### c) Résultat de mesure

Un résultat de mesure comprend généralement une valeur numérique, une unité et, lorsque cela est nécessaire, une indication de l'incertitude associée.

Exemple :

\[
T=(75,2\pm0,5)\ ^\circ C
\]

Cela signifie que le résultat annoncé est de 75,2 °C avec une incertitude de 0,5 °C, selon les conditions et la méthode utilisées pour établir cette incertitude.

Il ne faut pas interpréter cet intervalle comme une garantie absolue que la valeur vraie se trouve obligatoirement entre 74,7 °C et 75,7 °C.

## 1.6. Différence entre erreur et incertitude

Ces deux notions sont liées, mais elles ne désignent pas la même chose.

- **Erreur de mesure :** différence entre une valeur mesurée et une valeur de référence.
- **Incertitude de mesure :** paramètre qui caractérise la dispersion des valeurs pouvant raisonnablement être attribuées au mesurande, compte tenu des informations disponibles.

L'erreur représente un écart par rapport à une référence. L'incertitude exprime le doute associé au résultat.

---

# 2. GRANDEUR À MESURER ET PRINCIPE DE MESURAGE

## 2.1. Définition du mesurande

Le mesurande est la grandeur que l'on souhaite mesurer.

Il ne suffit pas toujours de désigner une grandeur de manière générale. Il faut préciser exactement ce que l'on veut déterminer.

**Exemple industriel :**

Dans le cas d'un moteur électrique, la mention « température du moteur » est insuffisamment précise.

Il est préférable de définir le mesurande comme suit :

« Température de la surface extérieure du palier avant du moteur électrique, exprimée en degrés Celsius, mesurée pendant le fonctionnement normal du moteur. »

Cette définition précise :

- La nature de la grandeur : température.
- L'emplacement : surface extérieure du palier avant.
- L'unité : degré Celsius.
- Les conditions : fonctionnement normal du moteur.

## 2.2. Caractérisation du mesurande

Pour définir correctement une grandeur à mesurer, il faut notamment considérer :

| Caractéristique | Question à se poser |
|---|---|
| Nature | Quelle grandeur veut-on mesurer ? |
| Unité | Dans quelle unité sera exprimée la valeur ? |
| Localisation | À quel endroit réalise-t-on la mesure ? |
| Conditions | Dans quelles conditions réalise-t-on la mesure ? |
| Temps | À quel instant ou pendant quelle durée ? |
| État du système | Le système est-il à l'arrêt, au démarrage ou en régime établi ? |

Deux mesures portant sur une même catégorie de grandeur peuvent donc correspondre à des mesurandes différents.

## 2.3. Représentation mathématique d'une grandeur variable

Certaines grandeurs physiques évoluent avec le temps.

On peut représenter une grandeur variable par une fonction :

\[
X=f(t)
\]

Où :

- \(X\) représente la grandeur étudiée ;
- \(t\) représente le temps.

**Exemple : évolution de la pression dans une conduite.**

| Heure | Pression |
|---|---:|
| 08 h 00 | 6,0 bar |
| 08 h 05 | 6,2 bar |
| 08 h 10 | 6,5 bar |
| 08 h 15 | 6,1 bar |
| 08 h 20 | 5,9 bar |

Ces valeurs permettent de caractériser plusieurs aspects du phénomène.

### a) Valeur instantanée

C'est la valeur de la grandeur à un instant déterminé.

Exemple : à 08 h 10, la pression est de 6,5 bar.

### b) Valeur moyenne

Pour un ensemble de \(n\) observations, la moyenne arithmétique est :

\[
X_{\text{moy}}=\frac{1}{n}\sum_{i=1}^{n}X_i
\]

Pour les cinq valeurs précédentes :

\[
X_{\text{moy}}=\frac{6,0+6,2+6,5+6,1+5,9}{5}
\]

\[
\boxed{X_{\text{moy}}=6,14\ bar}
\]

### c) Valeur maximale et valeur minimale

La valeur maximale est la plus grande valeur observée.

La valeur minimale est la plus petite valeur observée.

Dans notre exemple :

\[
X_{\max}=6,5\ bar
\]

\[
X_{\min}=5,9\ bar
\]

L'étendue des observations est :

\[
E=X_{\max}-X_{\min}
\]

\[
E=6,5-5,9
\]

\[
\boxed{E=0,6\ bar}
\]

## 2.4. Valeur efficace d'une grandeur électrique

Dans les installations électriques, on utilise fréquemment la valeur efficace, notamment pour les tensions et les courants alternatifs.

La valeur efficace d'un signal périodique est définie par :

\[
X_{\text{eff}}=\sqrt{\frac{1}{T}\int_0^T x^2(t)\,dt}
\]

Où :

- \(x(t)\) est la valeur instantanée du signal ;
- \(T\) est sa période ;
- \(X_{\text{eff}}\) est sa valeur efficace.

Pour un signal sinusoïdal :

\[
X_{\text{eff}}=\frac{X_{\max}}{\sqrt{2}}
\]

Ainsi, pour une tension sinusoïdale de valeur efficace 230 V :

\[
U_{\max}=230\sqrt{2}
\]

\[
\boxed{U_{\max}\approx325,3\ V}
\]

La valeur efficace est importante parce qu'elle permet de caractériser l'effet thermique d'un courant alternatif dans une résistance.

---

# 3. MÉTHODES ET TECHNIQUES DE MESURE

Il existe plusieurs méthodes permettant de déterminer la valeur d'une grandeur physique.

Parmi les méthodes classiques, on distingue notamment la méthode par déviation, la méthode par zéro et la méthode par substitution.

## 3.1. Méthode par déviation

La méthode par déviation consiste à déterminer une grandeur à partir de la déviation d'un indicateur.

L'appareil fournit une indication qui varie en fonction de la grandeur mesurée.

**Exemples :**

- Un ampèremètre analogique dont l'aiguille se déplace.
- Un voltmètre analogique.
- Un manomètre à tube de Bourdon.
- Un galvanomètre.

Le déplacement de l'indicateur est associé à une valeur de la grandeur recherchée.

**Principe :**

Grandeur physique → phénomène physique interne → déplacement de l'indicateur → lecture de la valeur.

**Avantage :** la mesure est généralement rapide.

**Limite :** la précision dépend notamment de la graduation, de la lecture et des caractéristiques de l'appareil.

## 3.2. Méthode par zéro

La méthode par zéro consiste à ajuster une grandeur de référence jusqu'à annuler la différence entre cette référence et la grandeur inconnue.

La condition d'équilibre est :

\[
\Delta X=X_x-X_r=0
\]

Donc :

\[
\boxed{X_x=X_r}
\]

Où :

- \(X_x\) est la grandeur inconnue ;
- \(X_r\) est la grandeur de référence.

**Exemple :**

Dans un pont de Wheatstone, on ajuste une résistance jusqu'à ce que le courant dans le galvanomètre devienne nul.

À cet instant, le pont est équilibré et la résistance inconnue peut être calculée.

## 3.3. Méthode par substitution

La méthode par substitution consiste à remplacer la grandeur inconnue par une grandeur de référence réglable, de manière à retrouver la même indication dans le dispositif de mesure.

**Exemple :**

On souhaite déterminer une résistance inconnue.

1. On branche la résistance inconnue dans un circuit.
2. On relève une indication de courant de 5 mA.
3. On retire la résistance inconnue.
4. On installe une résistance étalon réglable.
5. On ajuste cette résistance jusqu'à retrouver une indication de 5 mA.

La valeur de la résistance étalon au moment de l'équivalence permet de déterminer la résistance inconnue, sous réserve que les conditions expérimentales soient suffisamment identiques.

**Intérêt :**

La substitution permet de réduire certaines erreurs liées au dispositif de mesure, car la comparaison est réalisée avec le même système et dans des conditions similaires.

Elle ne supprime toutefois pas toutes les erreurs ni toute l'incertitude.

## 3.4. Comparaison des trois méthodes

| Critère | Déviation | Zéro | Substitution |
|---|---|---|---|
| Principe | Observer une indication | Annuler une différence | Remplacer par une référence |
| Grandeur de référence | Peut être intégrée à l'appareil | Nécessaire | Nécessaire |
| Opération principale | Lire | Équilibrer | Remplacer et ajuster |
| Exemple | Ampèremètre analogique | Pont de Wheatstone | Résistance étalon |
| Particularité | Rapidité | Recherche de l'équilibre | Comparaison par équivalence |

---

# 4. MESURES PAR COMPARAISON ET PAR ÉQUILIBRE

## 4.1. Principe de la comparaison

La comparaison consiste à confronter une grandeur inconnue à une grandeur de référence de même nature.

L'objectif est de déterminer l'écart entre les deux grandeurs ou d'établir une équivalence.

On peut écrire :

\[
\Delta X=X_x-X_r
\]

Avec :

- \(X_x\) : grandeur inconnue ;
- \(X_r\) : grandeur de référence ;
- \(\Delta X\) : différence entre les deux.

Lorsque la différence est nulle, les deux grandeurs sont considérées comme équilibrées dans les conditions de l'expérience.

## 4.2. Principe de l'équilibre

Un système de mesure est en équilibre lorsque la grandeur inconnue et la grandeur de référence produisent des effets équivalents dans le dispositif de comparaison.

La condition idéale est :

\[
X_x-X_r=0
\]

Donc :

\[
X_x=X_r
\]

Cette méthode est particulièrement intéressante lorsque l'on souhaite réduire l'influence de certaines caractéristiques du dispositif indicateur.

## 4.3. Application : pont de Wheatstone

Le pont de Wheatstone est un circuit électrique utilisé pour déterminer une résistance inconnue par une méthode d'équilibre.

Il est constitué de quatre résistances disposées en pont, d'une source d'alimentation et d'un galvanomètre.

Lorsque le pont est équilibré, le courant traversant le galvanomètre est nul.

La relation d'équilibre est :

\[
\frac{R_1}{R_2}=\frac{R_3}{R_x}
\]

En isolant la résistance inconnue :

\[
\boxed{R_x=\frac{R_2R_3}{R_1}}
\]

### Exemple d'application

On dispose des valeurs suivantes :

- \(R_1=100\ \Omega\)
- \(R_2=200\ \Omega\)
- \(R_3=150\ \Omega\)

Déterminons la résistance inconnue.

\[
R_x=\frac{200\times150}{100}
\]

\[
\boxed{R_x=300\ \Omega}
\]

La résistance inconnue vaut donc 300 Ω dans les conditions de l'équilibre.

## 4.4. Application industrielle : mesure de force par jauge de contrainte

Une jauge de contrainte est un élément résistif dont la résistance varie lorsqu'elle subit une déformation mécanique.

Lorsqu'une force est appliquée sur une pièce mécanique, celle-ci se déforme légèrement. Cette déformation entraîne une variation de résistance de la jauge.

Le principe peut être représenté ainsi :

Force appliquée → Déformation mécanique → Variation de résistance → Déséquilibre du pont → Tension électrique mesurable.

Les jauges de contrainte sont notamment utilisées dans :

- Les cellules de pesage.
- Les balances industrielles.
- Les systèmes de pesage de silos.
- Les bancs d'essais mécaniques.
- Les dispositifs de surveillance de structures.

Le pont de Wheatstone permet de transformer de faibles variations de résistance en une tension différentielle exploitable.

---

# 5. MESURES DIRECTES ET INDIRECTES

## 5.1. Détermination directe

Dans le sens pratique courant, une détermination est dite directe lorsque l'appareil fournit directement à l'utilisateur la valeur de la grandeur recherchée.

**Exemples :**

- Un thermomètre affichant 65 °C.
- Un manomètre affichant 7 bar.
- Un multimètre affichant une résistance de 120 Ω.

Il faut cependant distinguer cette utilisation pratique du terme « direct » de la notion de comparaison directe avec un étalon de même nature.

Un appareil peut afficher directement une résistance tout en réalisant intérieurement plusieurs opérations électriques.

## 5.2. Détermination indirecte

Une détermination est indirecte lorsque la grandeur recherchée est calculée à partir d'autres grandeurs mesurées, en utilisant une relation physique ou mathématique.

**Exemple : détermination d'une résistance électrique.**

On mesure :

- Une tension \(U=24\ V\).
- Un courant \(I=2\ A\).

En appliquant la loi d'Ohm :

\[
R=\frac{U}{I}
\]

\[
R=\frac{24}{2}
\]

\[
\boxed{R=12\ \Omega}
\]

La résistance est obtenue par calcul à partir de deux grandeurs mesurées.

## 5.3. Autre exemple : puissance électrique triphasée

Dans un système triphasé équilibré, la puissance active peut être déterminée par :

\[
P=\sqrt{3}\,U\,I\,\cos\varphi
\]

Où :

- \(P\) est la puissance active en watts ;
- \(U\) est la tension composée en volts ;
- \(I\) est le courant de ligne en ampères ;
- \(\cos\varphi\) est le facteur de puissance.

**Exemple :**

Un moteur fonctionne avec :

- \(U=400\ V\)
- \(I=10\ A\)
- \(\cos\varphi=0,85\)

Alors :

\[
P=\sqrt{3}\times400\times10\times0,85
\]

\[
\boxed{P\approx5889\ W}
\]

La puissance active est donc d'environ 5,89 kW.

## 5.4. Comparaison

| Détermination directe | Détermination indirecte |
|---|---|
| L'appareil fournit la grandeur recherchée à l'utilisateur | La grandeur est calculée |
| Lecture directe de l'indication | Utilisation d'une relation mathématique |
| Exemple : thermomètre affichant 65 °C | Exemple : calcul de la résistance avec U et I |
| Résultat généralement disponible rapidement | Nécessite plusieurs données et un calcul |

---

# 6. RELATIONS MATHÉMATIQUES ET LOIS PHYSIQUES APPLIQUÉES À LA MESURE

La mesure industrielle repose fréquemment sur des relations physiques permettant de relier plusieurs grandeurs.

La connaissance de ces relations est indispensable pour comprendre le fonctionnement des systèmes de mesure et exploiter correctement les résultats.

## 6.1. Loi d'Ohm

La loi d'Ohm établit la relation entre la tension, le courant et la résistance d'un conducteur ohmique.

\[
U=R I
\]

On peut également écrire :

\[
I=\frac{U}{R}
\]

\[
R=\frac{U}{I}
\]

**Application :**

Un circuit présente une tension de 48 V et une résistance de 24 Ω.

\[
I=\frac{48}{24}
\]

\[
\boxed{I=2\ A}
\]

Cette relation est utilisée dans les mesures électriques et le diagnostic des circuits industriels.

## 6.2. Puissance électrique

En courant continu ou pour des grandeurs instantanées :

\[
P=U I
\]

Pour un régime alternatif monophasé sinusoïdal :

\[
P=U I\cos\varphi
\]

Pour un système triphasé équilibré :

\[
P=\sqrt{3}\,U I\cos\varphi
\]

Ces relations permettent de déterminer une puissance à partir des grandeurs électriques mesurées.

## 6.3. Relation entre période et fréquence

Pour un phénomène périodique, la fréquence et la période sont liées par :

\[
f=\frac{1}{T}
\]

Et :

\[
T=\frac{1}{f}
\]

Avec :

- \(f\) : fréquence en hertz (Hz) ;
- \(T\) : période en secondes (s).

**Exemple :**

Un signal présente une période de 20 ms.

Conversion :

\[
T=20\times10^{-3}\ s
\]

Donc :

\[
f=\frac{1}{0,020}
\]

\[
\boxed{f=50\ Hz}
\]

Cette relation est notamment utilisée pour vérifier la fréquence d'une alimentation électrique industrielle.

## 6.4. Loi de Hooke : relation entre force et déformation

Dans le domaine élastique d'un ressort, la loi de Hooke s'écrit :

\[
F=kx
\]

Où :

- \(F\) est la force appliquée en newtons ;
- \(k\) est la raideur du ressort en N/m ;
- \(x\) est l'allongement en mètres.

**Exemple :**

Un ressort possède une raideur de 2000 N/m et subit un allongement de 0,01 m.

\[
F=2000\times0,01
\]

\[
\boxed{F=20\ N}
\]

Cette relation constitue un exemple de détermination indirecte d'une force à partir d'un déplacement connu et d'une raideur déterminée.

## 6.5. Relation entre température et résistance électrique

La résistance de certains conducteurs métalliques varie avec la température.

Dans une approximation linéaire autour d'une température de référence :

\[
R(T)=R_0[1+\alpha(T-T_0)]
\]

Où :

- \(R(T)\) est la résistance à la température \(T\) ;
- \(R_0\) est la résistance à la température de référence \(T_0\) ;
- \(\alpha\) est le coefficient de température du matériau.

Cette relation est notamment utile pour comprendre pourquoi la température doit être prise en compte lors de certaines mesures de résistance d'enroulements électriques.

---

# 7. SYNTHÈSE GÉNÉRALE

La théorie de la mesure permet de comprendre les principes scientifiques qui se trouvent derrière toute opération de mesurage.

Les notions essentielles de ce chapitre sont les suivantes :

| Notion | Idée essentielle |
|---|---|
| Mesure | Établir une relation entre une grandeur et une référence |
| Mesurage | Ensemble des opérations expérimentales permettant d'obtenir un résultat |
| Mesurande | Grandeur que l'on souhaite mesurer |
| Résultat de mesure | Valeur accompagnée de son unité et, si nécessaire, de son incertitude |
| Erreur | Écart entre une valeur mesurée et une valeur de référence |
| Incertitude | Paramètre caractérisant le doute associé au résultat |
| Méthode par déviation | Déterminer une grandeur à partir d'une indication |
| Méthode par zéro | Rechercher une condition d'équilibre |
| Méthode par substitution | Remplacer la grandeur inconnue par une référence équivalente |
| Comparaison | Confronter une grandeur inconnue à une référence |
| Détermination indirecte | Calculer une grandeur à partir d'autres grandeurs mesurées |

La maîtrise de ces notions constitue une base indispensable pour aborder la modélisation des systèmes de mesure, la chaîne de mesure et l'exploitation des résultats.

---

# 8. EXERCICES D'APPLICATION

## Exercice 1 — Loi d'Ohm

Un technicien mesure une tension de 24 V aux bornes d'une résistance. Le courant qui la traverse est de 2 A.

1. Déterminer la résistance.
2. Préciser s'il s'agit d'une détermination directe ou indirecte.
3. Donner la relation mathématique utilisée.

## Exercice 2 — Pont de Wheatstone

Un pont de Wheatstone est équilibré avec les valeurs suivantes :

- \(R_1=120\ \Omega\)
- \(R_2=240\ \Omega\)
- \(R_3=180\ \Omega\)

Déterminer la résistance inconnue \(R_x\).

## Exercice 3 — Puissance électrique

Un moteur triphasé équilibré fonctionne sous une tension composée de 400 V. Il absorbe un courant de 12 A avec un facteur de puissance de 0,82.

Déterminer sa puissance active absorbée.

## Exercice 4 — Exploitation de mesures

Un technicien relève les températures suivantes sur un palier :

52 °C ; 54 °C ; 56 °C ; 58 °C ; 60 °C.

1. Calculer la température moyenne.
2. Déterminer la température minimale.
3. Déterminer la température maximale.
4. Calculer l'étendue des mesures.

## Exercice 5 — Période et fréquence

Un signal électrique périodique présente une période de 10 ms.

Déterminer sa fréquence.

## Exercice 6 — Loi de Hooke

Un ressort possède une raideur de 1500 N/m. Il subit un allongement de 0,02 m.

Déterminer la force appliquée.

## Exercice 7 — Étude de cas industrielle

Un technicien doit déterminer la résistance d'un enroulement de moteur électrique.

Il dispose d'un multimètre et d'une alimentation électrique réglable. Il décide d'appliquer une tension connue, de mesurer le courant qui traverse l'enroulement, puis de calculer sa résistance.

1. Quelle méthode de détermination utilise-t-il ?
2. Quelles sont les deux grandeurs directement relevées ?
3. Quelle relation permet de calculer la résistance ?
4. Pourquoi faut-il tenir compte de la température de l'enroulement lors de cette opération ?

---

# 9. ÉVALUATION GÉNÉRALE

**Consigne :** choisir la bonne réponse pour chaque question.

### Question 1

Le mesurande représente :

A. L'appareil utilisé pour mesurer.  
B. La grandeur que l'on souhaite mesurer.  
C. La valeur de référence.  
D. L'erreur de mesure.

### Question 2

Le principe fondamental de la mesure repose sur :

A. La transformation systématique d'une grandeur en température.  
B. La comparaison ou l'établissement d'une relation avec une référence.  
C. L'utilisation obligatoire d'un automate programmable.  
D. La suppression de toutes les erreurs.

### Question 3

Dans la méthode par zéro, on recherche :

A. Une indication maximale.  
B. Une variation de température.  
C. Une différence nulle entre deux grandeurs.  
D. Une valeur minimale de courant.

### Question 4

Le pont de Wheatstone est principalement associé à :

A. La mesure d'une résistance par équilibre.  
B. La mesure directe d'une température.  
C. La mesure d'une fréquence mécanique.  
D. La mesure d'un débit.

### Question 5

Lorsqu'un technicien calcule une résistance à partir d'une tension et d'un courant mesurés, il réalise :

A. Une détermination directe.  
B. Une détermination indirecte.  
C. Une mesure par déviation uniquement.  
D. Une mesure de température.

### Question 6

La relation entre la fréquence et la période est :

A. \(f=T\)  
B. \(f=2T\)  
C. \(f=1/T\)  
D. \(f=T^2\)

### Question 7

Dans une relation linéaire \(Y=aX+b\), le coefficient \(a\) représente :

A. Le décalage initial.  
B. La sensibilité ou le coefficient de proportionnalité.  
C. L'unité de mesure.  
D. L'incertitude.

### Question 8

La méthode par substitution consiste à :

A. Remplacer la grandeur inconnue par une référence produisant une indication équivalente.  
B. Supprimer la référence.  
C. Mesurer uniquement une température.  
D. Faire fonctionner l'appareil sans grandeur d'entrée.

### Question 9

Une tension de 24 V traverse une résistance de 12 Ω. Le courant vaut :

A. 0,5 A.  
B. 1 A.  
C. 2 A.  
D. 12 A.

### Question 10

Une mesure correctement définie doit notamment préciser :

A. Uniquement le nom de l'appareil.  
B. La nature de la grandeur, sa localisation et les conditions de mesure.  
C. Uniquement la marque de l'instrument.  
D. Uniquement la date de fabrication de l'appareil.

---

**FIN DU CHAPITRE 02 — THÉORIE DE LA MESURE**
