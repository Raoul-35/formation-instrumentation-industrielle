# LEÇON 01 : LE CAPTEUR INDUSTRIEL

## 1. Objectifs pédagogiques

À la fin de cette leçon, nous devons être capables de :

- Définir un capteur industriel.
- Identifier les principaux éléments constitutifs d'un capteur.
- Expliquer son principe de fonctionnement.
- Classer les capteurs selon différents critères.
- Reconnaître les principaux capteurs utilisés dans les installations industrielles.

## 2. Définition du capteur industriel

Un capteur industriel est un dispositif qui détecte une grandeur physique et réagit à ses variations en produisant une réponse exploitable par un système de mesure, de surveillance ou de commande.

Les grandeurs physiques mesurées peuvent être :

- La température ;
- La pression ;
- Le niveau ;
- Le débit ;
- La vibration ;
- La position ;
- La vitesse ;
- L'humidité.

**Exemple industriel :**

Dans un moteur électrique, un capteur de température permet de surveiller l'échauffement des enroulements.

Lorsque la température augmente, le capteur réagit à cette variation et produit une réponse physique ou électrique exploitable par le système de mesure.

## 3. Constitution d'un capteur

Un capteur industriel peut comporter plusieurs éléments.

### 3.1. Élément sensible

C'est la partie du capteur qui réagit directement à la grandeur physique mesurée.

Exemples :
- Résistance en platine pour une PT100.
- Membrane sensible pour certains capteurs de pression.
- Élément piézoélectrique pour certains capteurs de vibration.

### 3.2. Corps ou boîtier

Il protège les composants internes contre les agressions extérieures : poussière, humidité, chocs, vibrations et températures élevées.

### 3.3. Éléments de raccordement

Ils permettent la connexion du capteur au système de mesure ou de commande.

Il peut s'agir de câbles, de connecteurs ou de bornes électriques.

### 3.4. Circuit électronique

Certains capteurs possèdent un circuit électronique intégré permettant notamment de traiter, amplifier ou conditionner la réponse de l'élément sensible.

**Remarque :** tous les capteurs ne possèdent pas nécessairement un circuit électronique intégré.

## 4. Principe de fonctionnement d'un capteur

Le fonctionnement général d'un capteur peut être décrit en quatre étapes :

1. Une grandeur physique agit sur le capteur.
2. L'élément sensible réagit à cette grandeur.
3. Le capteur produit une réponse physique ou électrique.
4. Cette réponse est exploitée directement ou après traitement par un circuit électronique ou un transmetteur.

### 4.1. Exemple : capteur de température PT100

La PT100 est une sonde de température résistive utilisant du platine comme élément sensible.

Son fonctionnement repose sur la variation de la résistance électrique en fonction de la température.

Valeurs caractéristiques d'une PT100 standard :

| Température | Résistance approximative |
|---|---:|
| 0 °C | 100 Ω |
| 25 °C | 109,73 Ω |
| 50 °C | 119,40 Ω |
| 75 °C | 129,00 Ω |
| 100 °C | 138,51 Ω |

Lorsque la température augmente, la résistance de la PT100 augmente également.

**À retenir :**
- Grandeur physique mesurée : température.
- Élément sensible : résistance en platine.
- Réponse électrique : variation de résistance.

### 4.2. Exemple : capteur de pression

Dans un capteur de pression utilisant une membrane sensible :

1. Le fluide exerce une pression sur la membrane.
2. La membrane se déforme.
3. Un élément de mesure détecte cette déformation.
4. La réponse obtenue est exploitée pour déterminer la pression.

Dans un transmetteur de pression, l'électronique traite cette réponse et fournit un signal exploitable, par exemple 4–20 mA.

## 5. Classification des capteurs

Les capteurs peuvent être classés selon plusieurs critères.

### 5.1. Selon la grandeur physique mesurée

| Catégorie | Grandeur mesurée | Exemple |
|---|---|---|
| Thermique | Température | PT100 |
| Mécanique | Pression | Capteur piézorésistif |
| Hydraulique | Niveau | Capteur hydrostatique |
| Fluidique | Débit | Débitmètre électromagnétique |
| Vibratoire | Accélération | Accéléromètre |
| Magnétique | Champ magnétique | Capteur à effet Hall |

### 5.2. Selon le principe physique de fonctionnement

| Type de capteur | Principe général |
|---|---|
| Résistif | Variation d'une résistance électrique |
| Capacitif | Variation d'une capacité électrique |
| Inductif | Variation d'une grandeur liée à l'inductance |
| Piézoélectrique | Production d'une charge électrique sous contrainte mécanique |
| Optique | Exploitation d'un phénomène lumineux |
| Ultrasonique | Exploitation de la propagation des ultrasons |
| Thermoélectrique | Production d'une tension liée à une différence de température |

**Exemple :** la PT100 est un capteur thermique selon la grandeur mesurée et résistif selon son principe de fonctionnement.

## 6. Exemples d'applications industrielles

| Capteur | Installation industrielle | Fonction |
|---|---|---|
| PT100 | Moteur électrique | Mesurer la température des enroulements |
| Capteur de pression | Compresseur | Mesurer la pression de refoulement |
| Capteur de niveau | Cuve | Mesurer le niveau du liquide |
| Débitmètre | Conduite d'eau | Mesurer le débit |
| Accéléromètre | Pompe centrifuge | Mesurer les vibrations |
| Capteur inductif | Convoyeur | Détecter la position d'une pièce métallique |

## 7. Application à la maintenance prédictive

Dans une installation industrielle, les capteurs permettent de surveiller l'état des équipements en fonctionnement.

Pour un moteur électrique, nous pouvons utiliser :

- Une PT100 pour surveiller la température.
- Un capteur de courant pour surveiller la consommation électrique.
- Un accéléromètre pour surveiller les vibrations.

L'analyse combinée de ces mesures permet de détecter certaines anomalies et d'anticiper des défaillances.

Cette approche est notamment utilisée dans notre projet de valise de maintenance prédictive.

## 8. Exercices d'application

### Exercice 1 : Identification d'un capteur

Une PT100 est installée sur un moteur électrique.

Quelle grandeur physique mesure-t-elle ?

A. La résistance électrique.

B. La température du moteur.

C. Le courant électrique.

**Réponse : B.**

Explication : la grandeur mesurée est la température. La résistance électrique est la réponse de l'élément sensible.

### Exercice 2 : Constitution

Dans une PT100, quel élément réagit directement à la variation de température ?

A. Le boîtier métallique.

B. La résistance en platine.

C. Le câble de raccordement.

**Réponse : B.**

### Exercice 3 : Principe de fonctionnement

Dans un transmetteur de pression utilisant une membrane sensible, quel élément réagit directement à la pression du fluide ?

A. La membrane sensible.

B. L'écran d'affichage.

C. Le câble électrique.

**Réponse : A.**

### Exercice 4 : Classification

Une PT100 appartient à quelle famille selon son principe de fonctionnement ?

A. Capteur capacitif.

B. Capteur résistif.

C. Capteur inductif.

**Réponse : B.**

### Exercice 5 : Application industrielle

Un accéléromètre est installé sur le corps d'une pompe centrifuge pour surveiller les vibrations.

Quelle grandeur physique mesure-t-il ?

A. La température.

B. La pression.

C. L'accélération vibratoire.

D. Le débit.

**Réponse : C.**

## 9. Synthèse : les notions essentielles

| Notion | Définition |
|---|---|
| Capteur | Dispositif qui réagit à une grandeur physique pour produire une information exploitable |
| Grandeur physique | Phénomène que nous souhaitons mesurer |
| Élément sensible | Partie du capteur qui réagit à la grandeur mesurée |
| Réponse du capteur | Variation physique ou électrique produite |
| Capteur résistif | Capteur dont le principe repose sur une variation de résistance |
| PT100 | Sonde résistive de température en platine |

### Conclusion

Le capteur constitue un élément fondamental de l'instrumentation industrielle. Il permet de recueillir des informations sur l'état physique des installations et des équipements.

La compréhension de son fonctionnement est indispensable avant d'étudier les détecteurs, les transmetteurs et les systèmes de mesure industriels.
